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
  </tr>
  <tr>
    <td>864</td>
    <td><a href="https://scholia.toolforge.org/Q6294930">Journal of Cheminformatics</a> (<a href="http://www.wikidata.org/entity/Q6294930">edit</a>)</td>
  </tr>
  <tr>
    <td>207</td>
    <td><a href="https://scholia.toolforge.org/Q564954">PLOS ONE</a> (<a href="http://www.wikidata.org/entity/Q564954">edit</a>)</td>
  </tr>
  <tr>
    <td>175</td>
    <td><a href="https://scholia.toolforge.org/Q2261792">Scientific Reports</a> (<a href="http://www.wikidata.org/entity/Q2261792">edit</a>)</td>
  </tr>
  <tr>
    <td>157</td>
    <td><a href="https://scholia.toolforge.org/Q135122">Nucleic Acids Research</a> (<a href="http://www.wikidata.org/entity/Q135122">edit</a>)</td>
  </tr>
  <tr>
    <td>152</td>
    <td><a href="https://scholia.toolforge.org/Q3319476">Molecular Informatics</a> (<a href="http://www.wikidata.org/entity/Q3319476">edit</a>)</td>
  </tr>
  <tr>
    <td>140</td>
    <td><a href="https://scholia.toolforge.org/Q15766522">Journal of Computer - Aided Molecular Design</a> (<a href="http://www.wikidata.org/entity/Q15766522">edit</a>)</td>
  </tr>
  <tr>
    <td>124</td>
    <td><a href="https://scholia.toolforge.org/Q4914910">Bioinformatics</a> (<a href="http://www.wikidata.org/entity/Q4914910">edit</a>)</td>
  </tr>
  <tr>
    <td>109</td>
    <td><a href="https://scholia.toolforge.org/Q4835939">BMC Bioinformatics</a> (<a href="http://www.wikidata.org/entity/Q4835939">edit</a>)</td>
  </tr>
  <tr>
    <td>103</td>
    <td><a href="https://scholia.toolforge.org/Q5227381">Database</a> (<a href="http://www.wikidata.org/entity/Q5227381">edit</a>)</td>
  </tr>
  <tr>
    <td>102</td>
    <td><a href="https://scholia.toolforge.org/Q3007982">Journal of Chemical Information and Modeling</a> (<a href="http://www.wikidata.org/entity/Q3007982">edit</a>)</td>
  </tr>
</table>
## Code examples
### curl
```shell
curl -o citingJournals.rq https://raw.githubusercontent.com/jcheminform/useful-queries/master/sparql/citingJournals.rq
curl -H "Accept: text/tab-separated-values" -G https://query.wikidata.org/bigdata/namespace/wdq/sparql --data-urlencode query@citingJournals.rq
```
This SPARQL query is available under CCZero.
