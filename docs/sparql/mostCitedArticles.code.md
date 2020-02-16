# mostCitedArticles.rq
**Code examples:** [curl](#curl)
### SPARQL
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
### Output
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
## Code examples
### curl
```shell
curl -o mostCitedArticles.rq https://raw.githubusercontent.com/jcheminform/useful-queries/master/sparql/mostCitedArticles.rq
curl -H "Accept: text/tab-separated-values" -G https://query.wikidata.org/bigdata/namespace/wdq/sparql --data-urlencode query@mostCitedArticles.rq
```
