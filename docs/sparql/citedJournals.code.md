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
    <td><b>cited_journalLabel</b></td>
  </tr>
  <tr>
    <td>2009</td>
    <td>http://www.wikidata.org/entity/Q3007982</td>
    <td>Journal of Chemical Information and Modeling</td>
  </tr>
  <tr>
    <td>864</td>
    <td>http://www.wikidata.org/entity/Q6294930</td>
    <td>Journal of Cheminformatics</td>
  </tr>
  <tr>
    <td>768</td>
    <td>http://www.wikidata.org/entity/Q135122</td>
    <td>Nucleic Acids Research</td>
  </tr>
  <tr>
    <td>634</td>
    <td>http://www.wikidata.org/entity/Q900316</td>
    <td>Journal of Medicinal Chemistry</td>
  </tr>
  <tr>
    <td>454</td>
    <td>http://www.wikidata.org/entity/Q4914910</td>
    <td>Bioinformatics</td>
  </tr>
  <tr>
    <td>296</td>
    <td>http://www.wikidata.org/entity/Q4835939</td>
    <td>BMC Bioinformatics</td>
  </tr>
  <tr>
    <td>292</td>
    <td>http://www.wikidata.org/entity/Q15766522</td>
    <td>Journal of Computer - Aided Molecular Design</td>
  </tr>
  <tr>
    <td>275</td>
    <td>http://www.wikidata.org/entity/Q3040085</td>
    <td>Drug Discovery Today</td>
  </tr>
  <tr>
    <td>187</td>
    <td>http://www.wikidata.org/entity/Q3186908</td>
    <td>Journal of Computational Chemistry</td>
  </tr>
  <tr>
    <td>176</td>
    <td>http://www.wikidata.org/entity/Q564954</td>
    <td>PLOS ONE</td>
  </tr>
</table>
## Code examples
### curl
```shell
curl -o citedJournals.rq https://raw.githubusercontent.com/jcheminform/useful-queries/master/sparql/citedJournals.rq
curl -H "Accept: text/tab-separated-values" -G https://query.wikidata.org/bigdata/namespace/wdq/sparql --data-urlencode query@citedJournals.rq
```
