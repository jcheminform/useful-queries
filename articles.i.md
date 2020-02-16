# Articles

This sections contains a collection of queries related to journal <topic>article</topic>s.

## Most cited articles

One thing we may be interested in is learning which topics have seen more citations
than others, hopefully reflecting impact, but we cannot decide that from just
citation counts. The following query takes advantage of the [WikiCite](http://wikicite.org/)
ideas:

<sparql>mostCitedArticles</sparql>

It lists the 10 <topic>most cited</topic> articles:

<out>mostCitedArticles</out>

## Articles citing retracted articles

For example, you may be interested which articles are citing <topic>retracted article</topic>s.
The following query can be used for this:

<sparql>citingRetractions</sparql>

For the Journal of Cheminformatics, this only gave one hit at the time
of writing:

<out>citingRetractions</out>
