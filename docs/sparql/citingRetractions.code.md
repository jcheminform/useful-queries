# citingRetractions.rq
**Code examples:** [curl](#curl)
### SPARQL
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
### Output
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
## Code examples
### curl
```shell
curl -o citingRetractions.rq https://raw.githubusercontent.com/jcheminform/useful-queries/master/sparql/citingRetractions.rq
curl -H "Accept: text/tab-separated-values" -G https://query.wikidata.org/bigdata/namespace/wdq/sparql --data-urlencode query@citingRetractions.rq
```
