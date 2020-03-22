# citedJournals.rq
**Code examples:** [curl](#curl)
### SPARQL
```sparql
SELECT
  ?count ?cited_journal ?cited_journalLabel
WITH {
  SELECT (COUNT(?cited_work) AS ?count) ?cited_journal
  WHERE {
    ?work wdt:P1433 wd:Q6294930 .
    ?work wdt:P2860 ?cited_work .
    ?cited_work wdt:P1433 ?cited_journal . 
  }
  GROUP BY ?cited_journal
} AS %result
WHERE {
  INCLUDE %result
  SERVICE wikibase:label { bd:serviceParam wikibase:language "en" . } 
}
ORDER BY DESC(?count) ?cited_journal
LIMIT 10

```
### Output
<table>
  <tr>
    <td><b>count</b></td>
    <td><b>cited_journal</b></td>
  </tr>
  <tr>
    <td>2009</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q3007982">Journal of Chemical Information and Modeling</a> (<a href="http://www.wikidata.org/entity/Q3007982">edit</a>)</td>
  </tr>
  <tr>
    <td>864</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q6294930">Journal of Cheminformatics</a> (<a href="http://www.wikidata.org/entity/Q6294930">edit</a>)</td>
  </tr>
  <tr>
    <td>768</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q135122">Nucleic Acids Research</a> (<a href="http://www.wikidata.org/entity/Q135122">edit</a>)</td>
  </tr>
  <tr>
    <td>634</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q900316">Journal of Medicinal Chemistry</a> (<a href="http://www.wikidata.org/entity/Q900316">edit</a>)</td>
  </tr>
  <tr>
    <td>454</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q4914910">Bioinformatics</a> (<a href="http://www.wikidata.org/entity/Q4914910">edit</a>)</td>
  </tr>
  <tr>
    <td>296</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q4835939">BMC Bioinformatics</a> (<a href="http://www.wikidata.org/entity/Q4835939">edit</a>)</td>
  </tr>
  <tr>
    <td>292</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q15766522">Journal of Computer - Aided Molecular Design</a> (<a href="http://www.wikidata.org/entity/Q15766522">edit</a>)</td>
  </tr>
  <tr>
    <td>275</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q3040085">Drug Discovery Today</a> (<a href="http://www.wikidata.org/entity/Q3040085">edit</a>)</td>
  </tr>
  <tr>
    <td>187</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q3186908">Journal of Computational Chemistry</a> (<a href="http://www.wikidata.org/entity/Q3186908">edit</a>)</td>
  </tr>
  <tr>
    <td>176</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q564954">PLOS ONE</a> (<a href="http://www.wikidata.org/entity/Q564954">edit</a>)</td>
  </tr>
</table>
## Code examples
### curl
```shell
curl -o citedJournals.rq https://raw.githubusercontent.com/jcheminform/useful-queries/master/sparql/citedJournals.rq
curl -H "Accept: text/tab-separated-values" -G https://query.wikidata.org/bigdata/namespace/wdq/sparql --data-urlencode query@citedJournals.rq
```
This SPARQL query is available under CCZero.
