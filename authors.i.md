# Authors

Your journals has to primary <topic>audience</topic>s, your <topic>readers</topic> and your <topic>authors</topic>.
A scholarly journal
is bringing these together. The reviewers are a subset of your readers.

## Prolific authors

One way to learn your authors is to see who wrote articles in your journal. Wikidata
is not complete in this respect, but this gives you some idea:

<sparql>prolificAuthors</sparql>

This query lists the top 10 most <topic>prolific authors</topic>:

<out>prolificAuthors</out>

By removing the LIMIT we can find all authors:

<sparql>prolificAuthorsAll</sparql>
