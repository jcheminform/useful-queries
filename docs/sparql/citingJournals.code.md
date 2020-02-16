# citingJournals.rq
**Code examples:** [curl](#curl)
### SPARQL
```sparql
SELECT ?count ?citing_journal ?citing_journalLabel 
WITH {
  SELECT (COUNT(?citing_work) as ?count) ?citing_journal
  WHERE {
    ?work wdt:P1433 wd:Q6294930 .
    ?citing_work wdt:P2860 ?work ;
                 wdt:P1433 ?citing_journal .
  }
  GROUP BY ?citing_journal
  ORDER BY DESC(?count)
  LIMIT 10
} AS %result
WHERE {
  INCLUDE %result
  SERVICE wikibase:label { bd:serviceParam wikibase:language "en" . } 
}
ORDER BY DESC(?count) ?citing_journal
```
### Output
<table>
  <tr>
    <td><b>count</b></td>
    <td><b>citing_journal</b></td>
    <td><b>citing_journalLabel</b></td>
  </tr>
  <tr>
    <td>864</td>
    <td>http://www.wikidata.org/entity/Q6294930</td>
    <td>Journal of Cheminformatics</td>
  </tr>
  <tr>
    <td>207</td>
    <td>http://www.wikidata.org/entity/Q564954</td>
    <td>PLOS ONE</td>
  </tr>
  <tr>
    <td>175</td>
    <td>http://www.wikidata.org/entity/Q2261792</td>
    <td>Scientific Reports</td>
  </tr>
  <tr>
    <td>157</td>
    <td>http://www.wikidata.org/entity/Q135122</td>
    <td>Nucleic Acids Research</td>
  </tr>
  <tr>
    <td>152</td>
    <td>http://www.wikidata.org/entity/Q3319476</td>
    <td>Molecular Informatics</td>
  </tr>
  <tr>
    <td>140</td>
    <td>http://www.wikidata.org/entity/Q15766522</td>
    <td>Journal of Computer - Aided Molecular Design</td>
  </tr>
  <tr>
    <td>124</td>
    <td>http://www.wikidata.org/entity/Q4914910</td>
    <td>Bioinformatics</td>
  </tr>
  <tr>
    <td>109</td>
    <td>http://www.wikidata.org/entity/Q4835939</td>
    <td>BMC Bioinformatics</td>
  </tr>
  <tr>
    <td>103</td>
    <td>http://www.wikidata.org/entity/Q5227381</td>
    <td>Database</td>
  </tr>
  <tr>
    <td>102</td>
    <td>http://www.wikidata.org/entity/Q3007982</td>
    <td>Journal of Chemical Information and Modeling</td>
  </tr>
</table>
## Code examples
### curl
```shell
curl -o citingJournals.rq https://raw.githubusercontent.com/jcheminform/useful-queries/master/sparql/citingJournals.rq
curl -H "Accept: text/tab-separated-values" -G https://query.wikidata.org/bigdata/namespace/wdq/sparql --data-urlencode query@citingJournals.rq
```
