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
  </tr>
  <tr>
    <td>733</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q21198766">Open Babel: An open chemical toolbox</a> (<a href="http://www.wikidata.org/entity/Q21198766">edit</a>)</td>
  </tr>
  <tr>
    <td>424</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q21092922">Avogadro: an advanced semantic chemical editor, visualization, and analysis platform</a> (<a href="http://www.wikidata.org/entity/Q21092922">edit</a>)</td>
  </tr>
  <tr>
    <td>174</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q27702050">Organization of GC/MS and LC/MS metabolomics data into chemical libraries</a> (<a href="http://www.wikidata.org/entity/Q27702050">edit</a>)</td>
  </tr>
  <tr>
    <td>94</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q27703005">TCMSP: a database of systems pharmacology for drug discovery from herbal medicines</a> (<a href="http://www.wikidata.org/entity/Q27703005">edit</a>)</td>
  </tr>
  <tr>
    <td>82</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q21030547">InChI - the worldwide chemical structure identifier standard</a> (<a href="http://www.wikidata.org/entity/Q21030547">edit</a>)</td>
  </tr>
  <tr>
    <td>79</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q27702054">Application of the PM6 semi-empirical method to modeling proteins enhances docking accuracy of AutoDock</a> (<a href="http://www.wikidata.org/entity/Q27702054">edit</a>)</td>
  </tr>
  <tr>
    <td>58</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q21198771">Small Molecule Subgraph Detector (SMSD) toolkit</a> (<a href="http://www.wikidata.org/entity/Q21198771">edit</a>)</td>
  </tr>
  <tr>
    <td>56</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q27703086">MOLE 2.0: advanced approach for analysis of biomacromolecular channels</a> (<a href="http://www.wikidata.org/entity/Q27703086">edit</a>)</td>
  </tr>
  <tr>
    <td>53</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q24607780">Linked open drug data for pharmaceutical research and development</a> (<a href="http://www.wikidata.org/entity/Q24607780">edit</a>)</td>
  </tr>
  <tr>
    <td>53</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q27702310">Why is Tanimoto index an appropriate choice for fingerprint-based similarity calculations?</a> (<a href="http://www.wikidata.org/entity/Q27702310">edit</a>)</td>
  </tr>
</table>
## Code examples
### curl
```shell
curl -o mostCitedArticles.rq https://raw.githubusercontent.com/jcheminform/useful-queries/master/sparql/mostCitedArticles.rq
curl -H "Accept: text/tab-separated-values" -G https://query.wikidata.org/bigdata/namespace/wdq/sparql --data-urlencode query@mostCitedArticles.rq
```
This SPARQL query is available under CCZero.
