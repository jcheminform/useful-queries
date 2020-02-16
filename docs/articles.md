# Articles

This sections contains a collection of queries related to journal articles.

## Most cited articles

One thing we may be interested in is learning which topics have seen more citations
than others, hopefully reflecting impact, but we cannot decide that from just
citation counts. The following query takes advantage of the [WikiCite](http://wikicite.org/)
ideas:

**SPARQL** [sparql/mostCitedArticles.rq](sparql/mostCitedArticles.code.html)
```sparql
SELECT ?count ?work ?workLabel
WITH {
  SELECT
    (COUNT(?citing_work) AS ?count) ?work
  WHERE {
    ?work wdt:P1433 wd:Q6294930 .
    ?citing_work wdt:P2860 ?work.
  }
  GROUP BY ?work
  ORDER BY DESC(?count)
  LIMIT 10
} AS %result
WHERE {
  INCLUDE %result
  SERVICE wikibase:label { bd:serviceParam wikibase:language "en" . } 
}
ORDER BY DESC(?count) ?work
```

It lists the 10 most cited articles:

<table>
  <tr>
    <td><b>count</b></td>
    <td><b>work</b></td>
    <td><b>workLabel</b></td>
  </tr>
  <tr>
    <td>733</td>
    <td>http://www.wikidata.org/entity/Q21198766</td>
    <td>Open Babel: An open chemical toolbox</td>
  </tr>
  <tr>
    <td>424</td>
    <td>http://www.wikidata.org/entity/Q21092922</td>
    <td>Avogadro: an advanced semantic chemical editor, visualization, and analysis platform</td>
  </tr>
  <tr>
    <td>174</td>
    <td>http://www.wikidata.org/entity/Q27702050</td>
    <td>Organization of GC/MS and LC/MS metabolomics data into chemical libraries</td>
  </tr>
  <tr>
    <td>94</td>
    <td>http://www.wikidata.org/entity/Q27703005</td>
    <td>TCMSP: a database of systems pharmacology for drug discovery from herbal medicines</td>
  </tr>
  <tr>
    <td>82</td>
    <td>http://www.wikidata.org/entity/Q21030547</td>
    <td>InChI - the worldwide chemical structure identifier standard</td>
  </tr>
  <tr>
    <td>79</td>
    <td>http://www.wikidata.org/entity/Q27702054</td>
    <td>Application of the PM6 semi-empirical method to modeling proteins enhances docking accuracy of AutoDock</td>
  </tr>
  <tr>
    <td>58</td>
    <td>http://www.wikidata.org/entity/Q21198771</td>
    <td>Small Molecule Subgraph Detector (SMSD) toolkit</td>
  </tr>
  <tr>
    <td>56</td>
    <td>http://www.wikidata.org/entity/Q27703086</td>
    <td>MOLE 2.0: advanced approach for analysis of biomacromolecular channels</td>
  </tr>
  <tr>
    <td>53</td>
    <td>http://www.wikidata.org/entity/Q24607780</td>
    <td>Linked open drug data for pharmaceutical research and development</td>
  </tr>
  <tr>
    <td>53</td>
    <td>http://www.wikidata.org/entity/Q27702310</td>
    <td>Why is Tanimoto index an appropriate choice for fingerprint-based similarity calculations?</td>
  </tr>
</table>

## Articles citing retracted articles

For example, you may be interested which articles are citing retracted articles.
The following query can be used for this:

**SPARQL** [sparql/citingRetractions.rq](sparql/citingRetractions.code.html)
```sparql
SELECT DISTINCT
  ?retracted_work ?retracted_workLabel
  ?date
  ?citing_work ?citing_workLabel
WITH {
  # Find retracted papers indicated by instance of retracted paper, 
  # by retraction notice property or by significant event
  SELECT DISTINCT ?retracted_work WHERE {
    { ?retracted_work wdt:P31 wd:Q45182324 }
    UNION
    { ?retracted_work wdt:P5824 [] }
    UNION
    { ?retracted_work wdt:P793 wd:Q45203135 }
  }
} AS %retracted_works
WHERE {
  INCLUDE %retracted_works
  ?citing_work wdt:P2860 ?retracted_work ; wdt:P1433 wd:Q6294930 .
  OPTIONAL {
    ?retracted_work wdt:P5824 ?retraction .
    ?retraction wdt:P577 ?retraction_datetime
    FILTER ( ?citing_work != ?retraction )
  }
  MINUS { ?citing_work wdt:P31 wd:Q1348305 }
  OPTIONAL {
    ?retracted_work p:P793 [ ps:P793 wd:Q45203135 ; pq:P585 ?keyevent_datetime ]
  }
  BIND(COALESCE(xsd:date(COALESCE(?retraction_datetime, ?keyevent_datetime)), "Unknown date") AS ?date)
  SERVICE wikibase:label { bd:serviceParam wikibase:language "[AUTO_LANGUAGE],en". }
}
ORDER BY DESC(?date)
```

For the Journal of Cheminformatics, this only gave one hit at the time
of writing:

<table>
  <tr>
    <td><b>retracted_work</b></td>
    <td><b>retracted_workLabel</b></td>
    <td><b>date</b></td>
    <td><b>citing_work</b></td>
    <td><b>citing_workLabel</b></td>
  </tr>
  <tr>
    <td>http://www.wikidata.org/entity/Q34203691</td>
    <td>RETRACTED: Predicting new molecular targets for rhein using network pharmacology.</td>
    <td>2014-09-18</td>
    <td>http://www.wikidata.org/entity/Q37426159</td>
    <td>CVDHD: a cardiovascular disease herbal database for drug discovery and network pharmacology.</td>
  </tr>
</table>



