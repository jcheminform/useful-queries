# Introduction

[Wikidata](https://wikidata.org/) is a useful resource in the linked data network [<a href="#citeref1">1</a>].
The [Wikicite](http://wikicite.org/) project has picked up the challenge to enter all
scholarly publications (cited in Wikipedia) [<a href="#citeref2">2</a>]. Inspired by
[Scholia](https://scholia.toolforge.org/) [<a href="#citeref3">3</a>], this electronic books collects
a number of queries useful to journal editors.

## Related journals

To sketch the journal eco system in which your journal operates, it can be interested to learn which
journals your authors are citing, and which journals are citing your articles. The following two
subsections list the top 10 journals for both categories, inspired by Scholia queries.

In both cases, you can remove the LIMIT to get the list of all journals.

### Journals cited by your articles

**SPARQL** [sparql/citedJournals.rq](sparql/citedJournals.code.html)
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

These 10 journals that are cited most from the journal are:

<table>
  <tr>
    <td><b>count</b></td>
    <td><b>cited_journal</b></td>
  </tr>
  <tr>
    <td>2009</td>
    <td><a href="https://scholia.toolforge.org/Q3007982">Journal of Chemical Information and Modeling</a> (<a href="http://www.wikidata.org/entity/Q3007982">edit</a>)</td>
  </tr>
  <tr>
    <td>864</td>
    <td><a href="https://scholia.toolforge.org/Q6294930">Journal of Cheminformatics</a> (<a href="http://www.wikidata.org/entity/Q6294930">edit</a>)</td>
  </tr>
  <tr>
    <td>768</td>
    <td><a href="https://scholia.toolforge.org/Q135122">Nucleic Acids Research</a> (<a href="http://www.wikidata.org/entity/Q135122">edit</a>)</td>
  </tr>
  <tr>
    <td>634</td>
    <td><a href="https://scholia.toolforge.org/Q900316">Journal of Medicinal Chemistry</a> (<a href="http://www.wikidata.org/entity/Q900316">edit</a>)</td>
  </tr>
  <tr>
    <td>454</td>
    <td><a href="https://scholia.toolforge.org/Q4914910">Bioinformatics</a> (<a href="http://www.wikidata.org/entity/Q4914910">edit</a>)</td>
  </tr>
  <tr>
    <td>297</td>
    <td><a href="https://scholia.toolforge.org/Q4835939">BMC Bioinformatics</a> (<a href="http://www.wikidata.org/entity/Q4835939">edit</a>)</td>
  </tr>
  <tr>
    <td>292</td>
    <td><a href="https://scholia.toolforge.org/Q15766522">Journal of Computer - Aided Molecular Design</a> (<a href="http://www.wikidata.org/entity/Q15766522">edit</a>)</td>
  </tr>
  <tr>
    <td>275</td>
    <td><a href="https://scholia.toolforge.org/Q3040085">Drug Discovery Today</a> (<a href="http://www.wikidata.org/entity/Q3040085">edit</a>)</td>
  </tr>
  <tr>
    <td>187</td>
    <td><a href="https://scholia.toolforge.org/Q3186908">Journal of Computational Chemistry</a> (<a href="http://www.wikidata.org/entity/Q3186908">edit</a>)</td>
  </tr>
  <tr>
    <td>176</td>
    <td><a href="https://scholia.toolforge.org/Q564954">PLOS ONE</a> (<a href="http://www.wikidata.org/entity/Q564954">edit</a>)</td>
  </tr>
</table>

### Journals citing your articles

**SPARQL** [sparql/citingJournals.rq](sparql/citingJournals.code.html)
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

These 10 journals cited your journal the most:

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

## References

1. <a name="citeref1"></a>Vrandečić D. Wikidata: A New Platform for Collaborative Data Collection. Proceedings of the 21st International Conference on World Wide Web. 2012;1063–4.  doi:[10.1145/2187980.2188242](https://doi.org/10.1145/2187980.2188242) ([Scholia](https://tools.wmflabs.org/scholia/doi/10.1145/2187980.2188242))
2. <a name="citeref2"></a>Taraborelli D, Dugan JM, Pintscher L, Mietchen D, Neylon C. WikiCite 2016 Report [Internet]. Wikimedia Commons. 2016 Nov. Available from: https://upload.wikimedia.org/wikipedia/commons/2/2b/WikiCite_2016_report.pdf doi:[10.6084/M9.FIGSHARE.4042530](https://doi.org/10.6084/M9.FIGSHARE.4042530) ([Scholia](https://tools.wmflabs.org/scholia/doi/10.6084/M9.FIGSHARE.4042530))
3. <a name="citeref3"></a>Nielsen FÅ, Mietchen D, Willighagen E. Scholia, Scientometrics and Wikidata. In: The Semantic Web: ESWC 2017 Satellite Events [Internet]. 2017. p. 237–59. Available from: http://www2.imm.dtu.dk/pubdb/views/edoc_download.php/7010/pdf/imm7010.pdf doi:[10.1007/978-3-319-70407-4_36](https://doi.org/10.1007/978-3-319-70407-4_36) ([Scholia](https://tools.wmflabs.org/scholia/doi/10.1007/978-3-319-70407-4_36))

