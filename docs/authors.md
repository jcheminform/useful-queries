# Authors

Your journals has to primary audiences, your readers and your authors. A scholarly journal
is bringing these together. The reviewers are a subset of your readers.

## Prolific authors

One way to learn your authors is to see who wrote articles in your journal. Wikidata
is not complete in this respect, but this gives you some idea:

**SPARQL** [sparql/prolificAuthors.rq](sparql/prolificAuthors.code.html)
```sparql
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

This query lists the top 10 most prolific authors:

<table>
  <tr>
    <td><b>count</b></td>
    <td><b>author</b></td>
    <td><b>authorLabel</b></td>
  </tr>
  <tr>
    <td>21</td>
    <td>http://www.wikidata.org/entity/Q5111731</td>
    <td>Christoph Steinbeck</td>
  </tr>
  <tr>
    <td>19</td>
    <td>http://www.wikidata.org/entity/Q28194918</td>
    <td>Evan E. Bolton</td>
  </tr>
  <tr>
    <td>18</td>
    <td>http://www.wikidata.org/entity/Q41893354</td>
    <td>Matthias Rarey</td>
  </tr>
  <tr>
    <td>16</td>
    <td>http://www.wikidata.org/entity/Q20895241</td>
    <td>Egon Willighagen</td>
  </tr>
  <tr>
    <td>15</td>
    <td>http://www.wikidata.org/entity/Q28379581</td>
    <td>Stephen H Bryant</td>
  </tr>
  <tr>
    <td>15</td>
    <td>http://www.wikidata.org/entity/Q4777220</td>
    <td>Antony John Williams</td>
  </tr>
  <tr>
    <td>15</td>
    <td>http://www.wikidata.org/entity/Q908710</td>
    <td>Peter Murray-Rust</td>
  </tr>
  <tr>
    <td>14</td>
    <td>http://www.wikidata.org/entity/Q27061853</td>
    <td>Ola Spjuth</td>
  </tr>
  <tr>
    <td>14</td>
    <td>http://www.wikidata.org/entity/Q28925563</td>
    <td>Andreas Bender</td>
  </tr>
  <tr>
    <td>14</td>
    <td>http://www.wikidata.org/entity/Q39934705</td>
    <td>Jaroslav Koča</td>
  </tr>
</table>

By removing the LIMIT we can find all authors:

**SPARQL** [sparql/prolificAuthorsAll.rq](sparql/prolificAuthorsAll.code.html)
```sparql
SELECT ?count ?author ?authorLabel
WITH {
  SELECT ?author (COUNT(?work) AS ?count)
  WHERE {
    ?work wdt:P50 ?author ;
          wdt:P1433 wd:Q6294930 .
  }
  GROUP BY ?author
} AS %result
WHERE {
  INCLUDE %result 
  SERVICE wikibase:label { bd:serviceParam wikibase:language "en" . } 
}
ORDER BY DESC(?count) ?author
```
