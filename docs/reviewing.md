# Reviewing

## Reviewers

When looking for <a name="tp1">reviewers</a>, you may be interested in learning of the authors and
reviewers worked together recently. Then this query may be useful
([source](https://chem-bla-ics.blogspot.com/2019/08/finding-potential-reviewers-using.html)):

**SPARQL** [sparql/coauthoring.rq](sparql/coauthoring.code.html)
```sparql
SELECT (
  iri(CONCAT(
    "https://tools.wmflabs.org/scholia/authors/",
    GROUP_CONCAT(SUBSTR(STR(?author),32); separator=",")
  )) AS ?authors) WHERE {
  VALUES ?orcid {
"0000-0002-5959-6190"
"0000-0001-9828-2074"
"0000-0002-4486-3356"
  }
  ?author wdt:P496 ?orcid .
}
```

The resulting link is a Scholia webpage this will show you (recent)
articles the potential reviewer(s) have co-authored with the author(s):

<table>
  <tr>
    <td><b>authors</b></td>
  </tr>
  <tr>
    <td>https://tools.wmflabs.org/scholia/authors/Q28194918,Q32565639,Q57415846</td>
  </tr>
</table>
