# Introduction

[Wikidata](https://wikidata.org/) is a useful resource in the linked data network [<cite>Q27042516</cite>].
The [Wikicite](http://wikicite.org/) project has picked up the challenge to enter all
scholarly publications (cited in Wikipedia) [<cite>Q28843308</cite>]. Inspired by
[Scholia](https://tools.wmflabs.org/scholia/) [<cite>Q41799194</cite>], this electronic books collects
a number of queries useful to journal editors.

## Related journals

To sketch the journal eco system in which your journal operates, it can be interested to learn which
journals your authors are citing, and which journals are citing your articles. The following two
subsections list the top 10 journals for both categories, inspired by Scholia queries.

In both cases, you can remove the LIMIT to get the list of all journals.

### Journals cited by your articles

<sparql>citedJournals</sparql>

These 10 journals that are cited most from the journal are:

<out>citedJournals</out>

### Journals citing your articles

<sparql>citingJournals</sparql>

These 10 journals cited your journal the most:

<out>citingJournals</out>

## References

<references/>
