# prolificAuthors.rq
**Code examples:** [curl](#curl)
### SPARQL
```sparql
# Prolific authors for a specific journal
SELECT ?count ?author ?authorLabel
WITH {
  # Count the number of works author by the author publishing in the journal
  SELECT
    ?author
    (COUNT(?work) AS ?count)
  WHERE {
    ?work wdt:P50 ?author ;
          wdt:P1433 wd:Q6294930 .
  }
  GROUP BY ?author
} AS %result
WHERE {
  INCLUDE %result 
  # Label the results
  SERVICE wikibase:label { bd:serviceParam wikibase:language "en" . } 
}
ORDER BY DESC(?count) ?author
LIMIT 10
```
### Output
<table>
  <tr>
    <td><b>count</b></td>
    <td><b>author</b></td>
  </tr>
  <tr>
    <td>21</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q5111731">Christoph Steinbeck</a> (<a href="http://www.wikidata.org/entity/Q5111731">edit</a>)</td>
  </tr>
  <tr>
    <td>19</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q28194918">Evan E. Bolton</a> (<a href="http://www.wikidata.org/entity/Q28194918">edit</a>)</td>
  </tr>
  <tr>
    <td>18</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q41893354">Matthias Rarey</a> (<a href="http://www.wikidata.org/entity/Q41893354">edit</a>)</td>
  </tr>
  <tr>
    <td>16</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q20895241">Egon Willighagen</a> (<a href="http://www.wikidata.org/entity/Q20895241">edit</a>)</td>
  </tr>
  <tr>
    <td>15</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q28379581">Stephen H Bryant</a> (<a href="http://www.wikidata.org/entity/Q28379581">edit</a>)</td>
  </tr>
  <tr>
    <td>15</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q4777220">Antony John Williams</a> (<a href="http://www.wikidata.org/entity/Q4777220">edit</a>)</td>
  </tr>
  <tr>
    <td>15</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q908710">Peter Murray-Rust</a> (<a href="http://www.wikidata.org/entity/Q908710">edit</a>)</td>
  </tr>
  <tr>
    <td>14</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q27061853">Ola Spjuth</a> (<a href="http://www.wikidata.org/entity/Q27061853">edit</a>)</td>
  </tr>
  <tr>
    <td>14</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q28925563">Andreas Bender</a> (<a href="http://www.wikidata.org/entity/Q28925563">edit</a>)</td>
  </tr>
  <tr>
    <td>14</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q39934705">Jaroslav Koča</a> (<a href="http://www.wikidata.org/entity/Q39934705">edit</a>)</td>
  </tr>
</table>
## Code examples
### curl
```shell
curl -o prolificAuthors.rq https://raw.githubusercontent.com/jcheminform/useful-queries/master/sparql/prolificAuthors.rq
curl -H "Accept: text/tab-separated-values" -G https://query.wikidata.org/bigdata/namespace/wdq/sparql --data-urlencode query@prolificAuthors.rq
```
This SPARQL query is available under CCZero.
