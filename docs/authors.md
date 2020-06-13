# Authors

Your journals has to primary <a name="tp1">audience</a>s, your <a name="tp2">readers</a> and your <a name="tp3">authors</a>.
A scholarly journal
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

This query lists the top 10 most <a name="tp4">prolific authors</a>:

<table>
  <tr>
    <td><b>count</b></td>
    <td><b>author</b></td>
  </tr>
  <tr>
    <td>22</td>
    <td><a href="https://scholia.toolforge.org/Q5111731">Christoph Steinbeck</a> (<a href="http://www.wikidata.org/entity/Q5111731">edit</a>)</td>
  </tr>
  <tr>
    <td>20</td>
    <td><a href="https://scholia.toolforge.org/Q41893354">Matthias Rarey</a> (<a href="http://www.wikidata.org/entity/Q41893354">edit</a>)</td>
  </tr>
  <tr>
    <td>19</td>
    <td><a href="https://scholia.toolforge.org/Q28194918">Evan E. Bolton</a> (<a href="http://www.wikidata.org/entity/Q28194918">edit</a>)</td>
  </tr>
  <tr>
    <td>16</td>
    <td><a href="https://scholia.toolforge.org/Q20895241">Egon Willighagen</a> (<a href="http://www.wikidata.org/entity/Q20895241">edit</a>)</td>
  </tr>
  <tr>
    <td>15</td>
    <td><a href="https://scholia.toolforge.org/Q28379581">Stephen H Bryant</a> (<a href="http://www.wikidata.org/entity/Q28379581">edit</a>)</td>
  </tr>
  <tr>
    <td>15</td>
    <td><a href="https://scholia.toolforge.org/Q4777220">Antony John Williams</a> (<a href="http://www.wikidata.org/entity/Q4777220">edit</a>)</td>
  </tr>
  <tr>
    <td>15</td>
    <td><a href="https://scholia.toolforge.org/Q908710">Peter Murray-Rust</a> (<a href="http://www.wikidata.org/entity/Q908710">edit</a>)</td>
  </tr>
  <tr>
    <td>14</td>
    <td><a href="https://scholia.toolforge.org/Q39934705">Jaroslav Koča</a> (<a href="http://www.wikidata.org/entity/Q39934705">edit</a>)</td>
  </tr>
  <tr>
    <td>13</td>
    <td><a href="https://scholia.toolforge.org/Q27061853">Ola Spjuth</a> (<a href="http://www.wikidata.org/entity/Q27061853">edit</a>)</td>
  </tr>
  <tr>
    <td>13</td>
    <td><a href="https://scholia.toolforge.org/Q28925563">Andreas Bender</a> (<a href="http://www.wikidata.org/entity/Q28925563">edit</a>)</td>
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
