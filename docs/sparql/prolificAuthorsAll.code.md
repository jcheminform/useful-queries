# prolificAuthorsAll.rq
**Code examples:** [curl](#curl)
### SPARQL
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
### Output
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
  <tr>
    <td>13</td>
    <td>http://www.wikidata.org/entity/Q32565639</td>
    <td>Sunghwan Kim</td>
  </tr>
  <tr>
    <td>12</td>
    <td>http://www.wikidata.org/entity/Q28946543</td>
    <td>Robert C Glen</td>
  </tr>
  <tr>
    <td>12</td>
    <td>http://www.wikidata.org/entity/Q44680976</td>
    <td>Radka Svobodová Vařeková</td>
  </tr>
  <tr>
    <td>12</td>
    <td>http://www.wikidata.org/entity/Q57198570</td>
    <td>Andrzej Bojarski</td>
  </tr>
  <tr>
    <td>11</td>
    <td>http://www.wikidata.org/entity/Q30086276</td>
    <td>Gerard J. P. van Westen</td>
  </tr>
  <tr>
    <td>10</td>
    <td>http://www.wikidata.org/entity/Q26707540</td>
    <td>David J. Wild</td>
  </tr>
  <tr>
    <td>10</td>
    <td>http://www.wikidata.org/entity/Q27061849</td>
    <td>Nina Jeliazkova</td>
  </tr>
  <tr>
    <td>10</td>
    <td>http://www.wikidata.org/entity/Q27902110</td>
    <td>Janna Hastings</td>
  </tr>
  <tr>
    <td>9</td>
    <td>http://www.wikidata.org/entity/Q44682699</td>
    <td>Stanislav Geidl</td>
  </tr>
  <tr>
    <td>9</td>
    <td>http://www.wikidata.org/entity/Q53843624</td>
    <td>Achim Zielesny</td>
  </tr>
  <tr>
    <td>8</td>
    <td>http://www.wikidata.org/entity/Q18609784</td>
    <td>Jürgen Bajorath</td>
  </tr>
  <tr>
    <td>8</td>
    <td>http://www.wikidata.org/entity/Q42201848</td>
    <td>Gerhard Wolber</td>
  </tr>
  <tr>
    <td>8</td>
    <td>http://www.wikidata.org/entity/Q43370829</td>
    <td>David Sehnal</td>
  </tr>
  <tr>
    <td>8</td>
    <td>http://www.wikidata.org/entity/Q43370883</td>
    <td>Ola Engkvist</td>
  </tr>
  <tr>
    <td>8</td>
    <td>http://www.wikidata.org/entity/Q5727848</td>
    <td>Henry S. Rzepa</td>
  </tr>
  <tr>
    <td>8</td>
    <td>http://www.wikidata.org/entity/Q84287725</td>
    <td>Georg Hinselmann</td>
  </tr>
  <tr>
    <td>7</td>
    <td>http://www.wikidata.org/entity/Q27065426</td>
    <td>Rajarshi Guha</td>
  </tr>
  <tr>
    <td>7</td>
    <td>http://www.wikidata.org/entity/Q27768873</td>
    <td>Peter Ertl</td>
  </tr>
  <tr>
    <td>7</td>
    <td>http://www.wikidata.org/entity/Q28946549</td>
    <td>Sam E. Adams</td>
  </tr>
  <tr>
    <td>7</td>
    <td>http://www.wikidata.org/entity/Q30362344</td>
    <td>Igor V. Tetko</td>
  </tr>
  <tr>
    <td>7</td>
    <td>http://www.wikidata.org/entity/Q51200321</td>
    <td>Tingjun Hou</td>
  </tr>
  <tr>
    <td>7</td>
    <td>http://www.wikidata.org/entity/Q51615601</td>
    <td>Gisbert Schneider</td>
  </tr>
  <tr>
    <td>7</td>
    <td>http://www.wikidata.org/entity/Q56084692</td>
    <td>Sabina Smusz</td>
  </tr>
  <tr>
    <td>7</td>
    <td>http://www.wikidata.org/entity/Q84301537</td>
    <td>Sergii Novotarskyi</td>
  </tr>
  <tr>
    <td>6</td>
    <td>http://www.wikidata.org/entity/Q21031914</td>
    <td>Gregor Fels</td>
  </tr>
  <tr>
    <td>6</td>
    <td>http://www.wikidata.org/entity/Q28540731</td>
    <td>Noel O'Boyle</td>
  </tr>
  <tr>
    <td>6</td>
    <td>http://www.wikidata.org/entity/Q29043209</td>
    <td>Sorel Muresan</td>
  </tr>
  <tr>
    <td>6</td>
    <td>http://www.wikidata.org/entity/Q29389602</td>
    <td>Roger Sayle</td>
  </tr>
  <tr>
    <td>6</td>
    <td>http://www.wikidata.org/entity/Q29460345</td>
    <td>Denis Fourches</td>
  </tr>
  <tr>
    <td>6</td>
    <td>http://www.wikidata.org/entity/Q30013427</td>
    <td>Jeremy G. Frey</td>
  </tr>
  <tr>
    <td>6</td>
    <td>http://www.wikidata.org/entity/Q42716526</td>
    <td>Gregory A. Landrum</td>
  </tr>
  <tr>
    <td>6</td>
    <td>http://www.wikidata.org/entity/Q53841786</td>
    <td>Wolf-Dietrich Ihlenfeldt</td>
  </tr>
  <tr>
    <td>6</td>
    <td>http://www.wikidata.org/entity/Q56509036</td>
    <td>Jan A Kors</td>
  </tr>
  <tr>
    <td>5</td>
    <td>http://www.wikidata.org/entity/Q21264701</td>
    <td>Sonja Herres-Pawlis</td>
  </tr>
  <tr>
    <td>5</td>
    <td>http://www.wikidata.org/entity/Q28540892</td>
    <td>Oliver Fiehn</td>
  </tr>
  <tr>
    <td>5</td>
    <td>http://www.wikidata.org/entity/Q28796322</td>
    <td>John W Mayfield</td>
  </tr>
  <tr>
    <td>5</td>
    <td>http://www.wikidata.org/entity/Q28865170</td>
    <td>Jonathan Alvarsson</td>
  </tr>
  <tr>
    <td>5</td>
    <td>http://www.wikidata.org/entity/Q28946652</td>
    <td>Geoffrey R. Hutchison</td>
  </tr>
  <tr>
    <td>5</td>
    <td>http://www.wikidata.org/entity/Q29052381</td>
    <td>Tobias Kind</td>
  </tr>
  <tr>
    <td>5</td>
    <td>http://www.wikidata.org/entity/Q29387592</td>
    <td>Marcus D. Hanwell</td>
  </tr>
  <tr>
    <td>5</td>
    <td>http://www.wikidata.org/entity/Q30269285</td>
    <td>Ewgenij Proschak</td>
  </tr>
  <tr>
    <td>5</td>
    <td>http://www.wikidata.org/entity/Q40222626</td>
    <td>Adriaan P IJzerman</td>
  </tr>
  <tr>
    <td>5</td>
    <td>http://www.wikidata.org/entity/Q43370869</td>
    <td>Stefan Mordalski</td>
  </tr>
  <tr>
    <td>5</td>
    <td>http://www.wikidata.org/entity/Q52083694</td>
    <td>Knut Baumann</td>
  </tr>
  <tr>
    <td>5</td>
    <td>http://www.wikidata.org/entity/Q56247792</td>
    <td>Dong-Sheng Cao</td>
  </tr>
  <tr>
    <td>5</td>
    <td>http://www.wikidata.org/entity/Q63676494</td>
    <td>Isidro Cortés-Ciriano</td>
  </tr>
  <tr>
    <td>4</td>
    <td>http://www.wikidata.org/entity/Q28133217</td>
    <td>Christopher Southan</td>
  </tr>
  <tr>
    <td>4</td>
    <td>http://www.wikidata.org/entity/Q28540616</td>
    <td>Thomas Hankemeier</td>
  </tr>
  <tr>
    <td>4</td>
    <td>http://www.wikidata.org/entity/Q28923515</td>
    <td>Colin Batchelor</td>
  </tr>
  <tr>
    <td>4</td>
    <td>http://www.wikidata.org/entity/Q28925903</td>
    <td>Valery Tkachenko</td>
  </tr>
  <tr>
    <td>4</td>
    <td>http://www.wikidata.org/entity/Q28946674</td>
    <td>Anna Gaulton</td>
  </tr>
  <tr>
    <td>4</td>
    <td>http://www.wikidata.org/entity/Q29387575</td>
    <td>Arvid Berg</td>
  </tr>
  <tr>
    <td>4</td>
    <td>http://www.wikidata.org/entity/Q29998906</td>
    <td>Oliver Kohlbacher</td>
  </tr>
  <tr>
    <td>4</td>
    <td>http://www.wikidata.org/entity/Q30045595</td>
    <td>Alex M Clark</td>
  </tr>
  <tr>
    <td>4</td>
    <td>http://www.wikidata.org/entity/Q30104439</td>
    <td>John P. Overington</td>
  </tr>
  <tr>
    <td>4</td>
    <td>http://www.wikidata.org/entity/Q41876113</td>
    <td>Frank M. Boeckler</td>
  </tr>
  <tr>
    <td>4</td>
    <td>http://www.wikidata.org/entity/Q42155173</td>
    <td>Junmei Wang</td>
  </tr>
  <tr>
    <td>4</td>
    <td>http://www.wikidata.org/entity/Q42571511</td>
    <td>Wesley Schaal</td>
  </tr>
  <tr>
    <td>4</td>
    <td>http://www.wikidata.org/entity/Q42719788</td>
    <td>Jean-Louis Reymond</td>
  </tr>
  <tr>
    <td>4</td>
    <td>http://www.wikidata.org/entity/Q42720048</td>
    <td>Mahendra Awale</td>
  </tr>
  <tr>
    <td>4</td>
    <td>http://www.wikidata.org/entity/Q43370862</td>
    <td>Daniel Svozil</td>
  </tr>
  <tr>
    <td>4</td>
    <td>http://www.wikidata.org/entity/Q43370904</td>
    <td>David Hoksza</td>
  </tr>
  <tr>
    <td>4</td>
    <td>http://www.wikidata.org/entity/Q53843262</td>
    <td>Oliver Koch</td>
  </tr>
  <tr>
    <td>4</td>
    <td>http://www.wikidata.org/entity/Q55406442</td>
    <td>Miquel Rojas-Chertó</td>
  </tr>
  <tr>
    <td>4</td>
    <td>http://www.wikidata.org/entity/Q61826780</td>
    <td>Luc Patiny</td>
  </tr>
  <tr>
    <td>4</td>
    <td>http://www.wikidata.org/entity/Q64167646</td>
    <td>Emilio Benfenati</td>
  </tr>
  <tr>
    <td>4</td>
    <td>http://www.wikidata.org/entity/Q64167890</td>
    <td>Hongming Chen</td>
  </tr>
  <tr>
    <td>4</td>
    <td>http://www.wikidata.org/entity/Q64869606</td>
    <td>Thorsten Meinl</td>
  </tr>
  <tr>
    <td>3</td>
    <td>http://www.wikidata.org/entity/Q18611251</td>
    <td>Stephen R. Heller</td>
  </tr>
  <tr>
    <td>3</td>
    <td>http://www.wikidata.org/entity/Q18611260</td>
    <td>Guenter Grethe</td>
  </tr>
  <tr>
    <td>3</td>
    <td>http://www.wikidata.org/entity/Q19845602</td>
    <td>Barbara Zdrazil</td>
  </tr>
  <tr>
    <td>3</td>
    <td>http://www.wikidata.org/entity/Q19845641</td>
    <td>Chris T. Evelo</td>
  </tr>
  <tr>
    <td>3</td>
    <td>http://www.wikidata.org/entity/Q27863244</td>
    <td>Emma L. Schymanski</td>
  </tr>
  <tr>
    <td>3</td>
    <td>http://www.wikidata.org/entity/Q28194921</td>
    <td>Michel Dumontier</td>
  </tr>
  <tr>
    <td>3</td>
    <td>http://www.wikidata.org/entity/Q29389590</td>
    <td>David M Jessop</td>
  </tr>
  <tr>
    <td>3</td>
    <td>http://www.wikidata.org/entity/Q29389599</td>
    <td>Daniel M Lowe</td>
  </tr>
  <tr>
    <td>3</td>
    <td>http://www.wikidata.org/entity/Q29998084</td>
    <td>Vedrin Jeliazkov</td>
  </tr>
  <tr>
    <td>3</td>
    <td>http://www.wikidata.org/entity/Q30046332</td>
    <td>Samuel Lampa</td>
  </tr>
  <tr>
    <td>3</td>
    <td>http://www.wikidata.org/entity/Q30503825</td>
    <td>Roberto Todeschini</td>
  </tr>
  <tr>
    <td>3</td>
    <td>http://www.wikidata.org/entity/Q30853931</td>
    <td>Alan McNaught</td>
  </tr>
  <tr>
    <td>3</td>
    <td>http://www.wikidata.org/entity/Q30853960</td>
    <td>Igor Pletnev</td>
  </tr>
  <tr>
    <td>3</td>
    <td>http://www.wikidata.org/entity/Q30853976</td>
    <td>Dmitrii Tchekhovskoi</td>
  </tr>
  <tr>
    <td>3</td>
    <td>http://www.wikidata.org/entity/Q30862909</td>
    <td>Tim Vandermeersch</td>
  </tr>
  <tr>
    <td>3</td>
    <td>http://www.wikidata.org/entity/Q33035163</td>
    <td>George Papadatos</td>
  </tr>
  <tr>
    <td>3</td>
    <td>http://www.wikidata.org/entity/Q33035164</td>
    <td>Anne Hersey</td>
  </tr>
  <tr>
    <td>3</td>
    <td>http://www.wikidata.org/entity/Q37611768</td>
    <td>Klaus R. Liedl</td>
  </tr>
  <tr>
    <td>3</td>
    <td>http://www.wikidata.org/entity/Q37611850</td>
    <td>Kristina M. Hettne</td>
  </tr>
  <tr>
    <td>3</td>
    <td>http://www.wikidata.org/entity/Q37611901</td>
    <td>Erik M van Mulligen</td>
  </tr>
  <tr>
    <td>3</td>
    <td>http://www.wikidata.org/entity/Q37829831</td>
    <td>Youyong Li</td>
  </tr>
  <tr>
    <td>3</td>
    <td>http://www.wikidata.org/entity/Q37836608</td>
    <td>Wolfgang Sippl</td>
  </tr>
  <tr>
    <td>3</td>
    <td>http://www.wikidata.org/entity/Q42726535</td>
    <td>Tiago Rodrigues</td>
  </tr>
  <tr>
    <td>3</td>
    <td>http://www.wikidata.org/entity/Q43370820</td>
    <td>Christoph Ruttkies</td>
  </tr>
  <tr>
    <td>3</td>
    <td>http://www.wikidata.org/entity/Q43370880</td>
    <td>Georgios Drakakis</td>
  </tr>
  <tr>
    <td>3</td>
    <td>http://www.wikidata.org/entity/Q43370892</td>
    <td>Jakub Galgonek</td>
  </tr>
  <tr>
    <td>3</td>
    <td>http://www.wikidata.org/entity/Q43370900</td>
    <td>César R García-Jacas</td>
  </tr>
  <tr>
    <td>3</td>
    <td>http://www.wikidata.org/entity/Q43370957</td>
    <td>Rafał Kurczab</td>
  </tr>
  <tr>
    <td>3</td>
    <td>http://www.wikidata.org/entity/Q43388721</td>
    <td>Robert M Hanson</td>
  </tr>
  <tr>
    <td>3</td>
    <td>http://www.wikidata.org/entity/Q44682520</td>
    <td>Crina-Maria Ionescu</td>
  </tr>
  <tr>
    <td>3</td>
    <td>http://www.wikidata.org/entity/Q44682790</td>
    <td>Tomáš Bouchal</td>
  </tr>
  <tr>
    <td>3</td>
    <td>http://www.wikidata.org/entity/Q49740420</td>
    <td>Ralph Müller-Pfefferkorn</td>
  </tr>
  <tr>
    <td>3</td>
    <td>http://www.wikidata.org/entity/Q55406542</td>
    <td>Theo Reijmers</td>
  </tr>
  <tr>
    <td>3</td>
    <td>http://www.wikidata.org/entity/Q57953722</td>
    <td>Nikolay Kochev</td>
  </tr>
  <tr>
    <td>3</td>
    <td>http://www.wikidata.org/entity/Q60558900</td>
    <td>Andreas Karwath</td>
  </tr>
  <tr>
    <td>3</td>
    <td>http://www.wikidata.org/entity/Q60961322</td>
    <td>Jiří Vondrášek</td>
  </tr>
  <tr>
    <td>3</td>
    <td>http://www.wikidata.org/entity/Q63208429</td>
    <td>Sebastian Böcker</td>
  </tr>
  <tr>
    <td>3</td>
    <td>http://www.wikidata.org/entity/Q65088027</td>
    <td>Anne Mai Wassermann</td>
  </tr>
  <tr>
    <td>3</td>
    <td>http://www.wikidata.org/entity/Q7177718</td>
    <td>Peter Willett</td>
  </tr>
  <tr>
    <td>3</td>
    <td>http://www.wikidata.org/entity/Q7440973</td>
    <td>Sean Ekins</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q109081</td>
    <td>Johann Gasteiger</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q1222879</td>
    <td>Dieter Steinhilber</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q12788090</td>
    <td>Dušanka Janežič</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q15995097</td>
    <td>C. Lee Giles</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q16335154</td>
    <td>Alfonso Valencia</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q17021355</td>
    <td>Jean-Claude Bradley</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q19845653</td>
    <td>Stefan Senger</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q24013775</td>
    <td>Sereina Riniker</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q28052829</td>
    <td>Saulius Gražulis</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q28540435</td>
    <td>Jarl Wikberg</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q28541023</td>
    <td>Steffen Neumann</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q28541054</td>
    <td>Haralambos Sarimveis</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q28747176</td>
    <td>Jos Kleinjans</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q28923506</td>
    <td>Lars Carlsson</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q29032923</td>
    <td>Paula de Matos</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q29389592</td>
    <td>Lezan Hawizy</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q29405902</td>
    <td>Stefan Kuhn</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q29406424</td>
    <td>Kenneth Haug</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q30046697</td>
    <td>Jean-Loup Faulon</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q30112600</td>
    <td>Obdulia Rabal</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q30347500</td>
    <td>Vladimir B. Bajic</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q30503831</td>
    <td>João Aires de Sousa</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q38323677</td>
    <td>Tudor I Oprea</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q38639158</td>
    <td>Chun-Wei Tung</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q39382967</td>
    <td>Yovani Marrero-Ponce</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q39484473</td>
    <td>Harald H Sitte</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q40403099</td>
    <td>Xiaomin Luo</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q40615839</td>
    <td>Björn A Grüning</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q41049168</td>
    <td>Francisco M. Couto</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q41373025</td>
    <td>Viviana Consonni</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q41585873</td>
    <td>Daniel Neagu</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q42093041</td>
    <td>Ingo Krossing</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q42098378</td>
    <td>Florian Nigsch</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q42211866</td>
    <td>Matthieu Montes</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q42628458</td>
    <td>Dario Greco</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q42873154</td>
    <td>Jonathan D. Hirst</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q42912645</td>
    <td>Steven M. Bachrach</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q43154574</td>
    <td>Vladimir Poroikov</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q43291987</td>
    <td>Stuart J. Chalk</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q43370243</td>
    <td>Kalai Vanii Jayaseelan</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q43370281</td>
    <td>Nico Adams</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q43370334</td>
    <td>Tomáš Pluskal</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q43370812</td>
    <td>Alexey Lagunin</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q43370813</td>
    <td>Cerys Willoughby</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q43370817</td>
    <td>Ben O'Steen</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q43370827</td>
    <td>Jonathan D Tyzack</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q43370828</td>
    <td>Lukáš Pravda</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q43370845</td>
    <td>Andrés Bernal</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q43370846</td>
    <td>Julien Wist</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q43370855</td>
    <td>Panos Kalnis</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q43370856</td>
    <td>Davide Ballabio</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q43370872</td>
    <td>David Marcus</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q43370876</td>
    <td>Nicholas J Mason</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q43370879</td>
    <td>Richard Lewis</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q43370881</td>
    <td>Lewis H Mervin</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q43370888</td>
    <td>José L. Medina-Franco</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q43370898</td>
    <td>Paolo Tosco</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q43370901</td>
    <td>Stephen J. Barigye</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q43370924</td>
    <td>Ines Thiele</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q43370926</td>
    <td>Sérgio Matos</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q43370931</td>
    <td>Jens Thomas</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q43370955</td>
    <td>Mingyue Zheng</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q43370998</td>
    <td>Marco Capuccini</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q43371002</td>
    <td>Lazaros Mavridis</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q43371005</td>
    <td>Jochen Junker</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q43371010</td>
    <td>Robert Günther</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q43371017</td>
    <td>Francois Berenger</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q43371023</td>
    <td>Nicole Jung</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q43371028</td>
    <td>George Van Den Driessche</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q43371035</td>
    <td>Yufeng J. Tseng</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q43371037</td>
    <td>Huiyong Sun</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q43837602</td>
    <td>Kamel Mansouri</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q43837665</td>
    <td>Andrew D McEachran</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q44682954</td>
    <td>Ruben Abagyan</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q46155617</td>
    <td>Jonathan M. Goodman</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q46275105</td>
    <td>Dmitry Filimonov</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q4720252</td>
    <td>Alexander Tropsha</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q47501420</td>
    <td>Markus Wagener</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q47508780</td>
    <td>Stephen Stein</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q47509086</td>
    <td>Uli Fechner</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q4758469</td>
    <td>Andrew S.I.D. Lang</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q49409340</td>
    <td>Marcus Ennis</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q49740441</td>
    <td>Klaus-Dieter Warzecha</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q49740465</td>
    <td>André Brinkmann</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q50726329</td>
    <td>Jacob de Vlieg</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q50983316</td>
    <td>Robert D. Clark</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q51782466</td>
    <td>Johannes Kirchmair</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q51878943</td>
    <td>Hans De Winter</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q52106301</td>
    <td>Bart Lenselink</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q53841690</td>
    <td>Nikolaus Stiefl</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q56084691</td>
    <td>Miguel Vazquez</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q56248678</td>
    <td>Andrius Merkys</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q56419420</td>
    <td>Anders Wallqvist</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q56421877</td>
    <td>Jeffrey P Plante</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q57191385</td>
    <td>Kai Dührkop</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q58882445</td>
    <td>Magbubah Essack</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q59698544</td>
    <td>Michal Brylinski</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q60960357</td>
    <td>Ludger A Wessjohann</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q63681860</td>
    <td>Eoin Fahy</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q64750275</td>
    <td>Franca-Maria Klingler</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q64750696</td>
    <td>Jean-François Zagury</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q71034096</td>
    <td>Karl-Heinz Baringhaus</td>
  </tr>
  <tr>
    <td>2</td>
    <td>http://www.wikidata.org/entity/Q84287127</td>
    <td>Arpana Vaniya</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q11867366</td>
    <td>Juha Kere</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q12364748</td>
    <td>Ivo Leito</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q1243222</td>
    <td>Thomas Lengauer</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q15285878</td>
    <td>Cameron Neylon</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q17061967</td>
    <td>Nicola Gaston</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q17177501</td>
    <td>Pablo Echenique-Robba</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q17386431</td>
    <td>Petra Mutzel</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q17489039</td>
    <td>Shoba Ranganathan</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q17516035</td>
    <td>Jeffrey Skolnick</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q19845608</td>
    <td>Daniela Digles</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q19845625</td>
    <td>Andra Waagmeester</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q19845639</td>
    <td>Jose Brea</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q2000014</td>
    <td>John Wilbanks</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q20116474</td>
    <td>Christopher A. Lipinski</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q2074784</td>
    <td>Peter F. Stadler</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q25975812</td>
    <td>Alexandre Hocquet</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q26709023</td>
    <td>Klaus-Robert Müller</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q27887604</td>
    <td>David S Wishart</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q28122093</td>
    <td>Chanin Nantasenamat</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q28320727</td>
    <td>Heinrich Sticht</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q28745439</td>
    <td>Cristian R. Munteanu</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q28854723</td>
    <td>Martin Eklund</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q28854903</td>
    <td>Georgia Tsiliki</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q28914636</td>
    <td>Matthias Samwald</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q28914639</td>
    <td>Eric G. Prud’hommeaux</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q28951592</td>
    <td>Martin Paul Brändle</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q29315318</td>
    <td>Jens Meiler</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q29405774</td>
    <td>Masanori Arita</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q29405912</td>
    <td>Barry Hardy</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q29406339</td>
    <td>Reza M. Salek</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q30046695</td>
    <td>Jérôme Pansanel</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q30046701</td>
    <td>Gilleain Torrance</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q30104387</td>
    <td>Romualdo Benigni</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q30170265</td>
    <td>Hans-Ulrich Demuth</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q30190636</td>
    <td>Teresa Carlomagno</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q30225131</td>
    <td>Joan-Emma Shea</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q30318445</td>
    <td>Sophia Ananiadou</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q30503169</td>
    <td>Michael M. Hoffman</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q30503828</td>
    <td>Maria Grishina</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q30505440</td>
    <td>Yong-Yeol Ahn</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q30518653</td>
    <td>Neil D. Young</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q30518683</td>
    <td>Andreas Hofmann</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q30766768</td>
    <td>Anja Jentzsch</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q30828813</td>
    <td>Eyke Hüllermeier</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q30863103</td>
    <td>Michael Banck</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q32416912</td>
    <td>Eileen Socher</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q32634180</td>
    <td>George Hripcsak</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q33133975</td>
    <td>Susie Stephens</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q3383843</td>
    <td>Pierre Baldi</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q37368799</td>
    <td>Michal Otyepka</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q37377779</td>
    <td>Anna Vulpetti</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q37384288</td>
    <td>Matthew D. Krasowski</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q37390028</td>
    <td>Christoph Flamm</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q37392250</td>
    <td>Manuel C. Peitsch</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q37830599</td>
    <td>Ingebrigt Sylte</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q38174461</td>
    <td>Michael Berthold</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q38174474</td>
    <td>Stephan Beisken</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q38330768</td>
    <td>Mauro D'Amato</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q38544936</td>
    <td>Olli T Pentikäinen</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q38601597</td>
    <td>John F. Wambaugh</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q38641963</td>
    <td>José Luís Oliveira</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q39049629</td>
    <td>Daniel Moser</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q39657849</td>
    <td>Anita R Maguire</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q39724540</td>
    <td>Lluís Arola</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q39972241</td>
    <td>Syed A. Rahman</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q39972290</td>
    <td>Gemma L. Holliday</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q40023319</td>
    <td>Simon J. Coles</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q40080540</td>
    <td>Ferran Sanz</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q40285012</td>
    <td>Daan P Geerke</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q40364172</td>
    <td>Antonio Rescifina</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q40389326</td>
    <td>Oldamur Hollóczki</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q40486468</td>
    <td>Csaba Hetényi</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q41048978</td>
    <td>Ronald Taylor</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q41049335</td>
    <td>Jose A. Seoane</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q41049805</td>
    <td>Juan Carlos Mobarec</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q41050128</td>
    <td>Antreas Afantitis</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q41099546</td>
    <td>Matthew Bashton</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q41602447</td>
    <td>Robert Preissner</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q41610209</td>
    <td>David W. Ritchie</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q41728407</td>
    <td>Mi-hyun Kim</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q41728850</td>
    <td>Tomasz Puzyn</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q41790698</td>
    <td>Koen Augustyns</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q42201814</td>
    <td>Miguel Quirós</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q42228266</td>
    <td>Georgia Melagraki</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q42326124</td>
    <td>Norbert Haider</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q42326677</td>
    <td>Robin B. Gasser</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q42386872</td>
    <td>John T Prince</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q42418395</td>
    <td>Naomie Salim</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q42425503</td>
    <td>José María Gutiérrez</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q42612964</td>
    <td>Kirill Okhotnikov</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q42634693</td>
    <td>Maciej Wójcikowski</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q42702402</td>
    <td>Orazio Nicolotti</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q42716142</td>
    <td>Yu-Shi Tian</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q42780467</td>
    <td>Eddy Sotelo</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q42783959</td>
    <td>Jörg Kurt Wegner</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q42824429</td>
    <td>Patrik Rydberg</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q42850572</td>
    <td>Heinz Singer</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q42850575</td>
    <td>Juliane Hollender</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q42869668</td>
    <td>Gerrit Schüürmann</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43086719</td>
    <td>Fredrik Svensson</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43185841</td>
    <td>Andrew Leach</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43194751</td>
    <td>Thibault Charpentier</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43275952</td>
    <td>Xavier Lucas</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43356360</td>
    <td>Tomas Oberg</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370241</td>
    <td>Karol M Langner</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370252</td>
    <td>Pantelis Sopasakis</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370275</td>
    <td>Janos Hajagos</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370305</td>
    <td>Christoph Helma</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370325</td>
    <td>Carlos Fernandez-Lozano</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370332</td>
    <td>Sajjan S Mehta</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370806</td>
    <td>Eva Zurek</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370807</td>
    <td>Micha Rautenberg</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370808</td>
    <td>Olga Tcheremenskaia</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370814</td>
    <td>Thomas A Logothetis</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370816</td>
    <td>Peter Sefton</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370818</td>
    <td>Venkatesh Muthukrishnan</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370819</td>
    <td>Adriano Dekker</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370821</td>
    <td>Dávid Bajusz</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370822</td>
    <td>Aik Choon Tan</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370823</td>
    <td>Jinlong Ru</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370825</td>
    <td>Peng Li</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370826</td>
    <td>Mark J Williamson</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370830</td>
    <td>Karel Berka</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370844</td>
    <td>Mohamad Mohebifar</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370848</td>
    <td>Maude Pupin</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370849</td>
    <td>Laurent Noé</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370850</td>
    <td>Carlos F. Suárez</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370851</td>
    <td>Guillermo Restrepo</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370852</td>
    <td>Floriane Montanari</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370853</td>
    <td>Gert-Jan Bekker</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370854</td>
    <td>Martin Gütlein</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370857</td>
    <td>Vishal B. Siramshetty</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370858</td>
    <td>Prachi Pradeep</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370859</td>
    <td>Sorin Avram</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370860</td>
    <td>Simona Funar-Timofei</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370861</td>
    <td>Sakari Lätti</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370863</td>
    <td>Alex A Freitas</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370864</td>
    <td>Alain-Dominique Gorse</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370866</td>
    <td>Sarah Preston</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370870</td>
    <td>Thommas M. Musyoka</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370871</td>
    <td>Paweł Siedlecki</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370873</td>
    <td>Axel J. Soto</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370875</td>
    <td>Ignacio Ponzoni</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370877</td>
    <td>Tailong Lei</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370887</td>
    <td>Fernando D. Prieto-Martínez</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370889</td>
    <td>Boris L Alperin</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370891</td>
    <td>Vladimír Horský</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370894</td>
    <td>Samuel Croset</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370895</td>
    <td>Lora Mak</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370902</td>
    <td>Manuel Pastor</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370903</td>
    <td>Radoslav Krivák</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370908</td>
    <td>Vincent F. Scalfani</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370915</td>
    <td>Marc C Nicklaus</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370916</td>
    <td>Mark Davies</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370917</td>
    <td>Louisa Bellis</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370918</td>
    <td>Robert Petryszak</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370919</td>
    <td>Sameer Velankar</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370922</td>
    <td>Matthew Smith</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370923</td>
    <td>Peter Matthews</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370925</td>
    <td>Fidele Ntie-Kang</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370927</td>
    <td>Karin Verspoor</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370928</td>
    <td>Sven Kochmann</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370932</td>
    <td>Jorge Estrada</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370933</td>
    <td>Pablo de Castro</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370936</td>
    <td>Paul Sherwood</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370938</td>
    <td>Alexander Kos</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370939</td>
    <td>Ying-Chi Lin</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370942</td>
    <td>Giovanni Nastasi</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370944</td>
    <td>Hugo López-Fernández</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370945</td>
    <td>Miguel Reboiro-Jato</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370946</td>
    <td>Daniel Glez-Peña</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370950</td>
    <td>Andrew M Walker</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370951</td>
    <td>Francesco Napolitano</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370952</td>
    <td>Vânia M Moreira</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370953</td>
    <td>Diogo Ars Latino</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370956</td>
    <td>Bharath Srinivasan</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370958</td>
    <td>Lewis Whitehead</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370959</td>
    <td>Isabel C. F. R. Ferreira</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370960</td>
    <td>Adrian M. Schreyer</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43370999</td>
    <td>Brian McMahon</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43371003</td>
    <td>Patrick N. Reardon</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43371004</td>
    <td>Brendan Howlin</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43371012</td>
    <td>Evangelos Kanoulas</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43371014</td>
    <td>Saw Simeon</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43371015</td>
    <td>Aleksandar Radovanovic</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43371016</td>
    <td>Mandeep Kaur</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43371019</td>
    <td>Effirul Ikhwan Ramlan</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43371021</td>
    <td>Andre O. Falcao</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43371022</td>
    <td>João P. Leal</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43371027</td>
    <td>Steve O'Hagan</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43371029</td>
    <td>Robbie P. Joosten</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43371030</td>
    <td>Santiago Garcia-Vallvé</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43371031</td>
    <td>Gerard Pujadas</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43371032</td>
    <td>Anna Arola-Arnal</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43371033</td>
    <td>Christopher J Harris</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43371034</td>
    <td>Brandon Bongers</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q43371038</td>
    <td>Francesc Solsona</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q44566877</td>
    <td>Salvatore La Rosa</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q45296850</td>
    <td>Marcel Bermudez</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q45789717</td>
    <td>Marc Zimmermann</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q45789729</td>
    <td>Mathilde Romberg</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q46547005</td>
    <td>Grace Patlewicz</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q47012855</td>
    <td>Duncan Hull</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q47087369</td>
    <td>Karl Edman</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q47087753</td>
    <td>David van der Spoel</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q47098084</td>
    <td>Andre Lamurias</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q47160873</td>
    <td>Nicole Tegtmeyer</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q47166195</td>
    <td>Eko A Rifai</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q47166196</td>
    <td>Marc van Dijk</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q47245405</td>
    <td>Aurélien Latouche</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q47262336</td>
    <td>Jean-Louis Reymond</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q47455639</td>
    <td>Jim Downing</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q47455673</td>
    <td>Dan W Zaharevitz</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q47474707</td>
    <td>Imran Shah</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q47698166</td>
    <td>Abid Qureshi</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q48511379</td>
    <td>Graham Ladds</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q50029895</td>
    <td>Chris de Graaf</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q50281591</td>
    <td>Tim Rocktäschel</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q50731316</td>
    <td>Andrea Volkamer</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q50731613</td>
    <td>Florbela Pereira</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q50731867</td>
    <td>Matteo Floris</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q50731930</td>
    <td>Thomas Engel</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q51058144</td>
    <td>Ulf Norinder</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q51523897</td>
    <td>Dmitry I. Osolodkin</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q51751131</td>
    <td>Nurul Malim</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q51753160</td>
    <td>Ralf Weiskirchen</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q52082270</td>
    <td>Hitesh Patel</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q52083659</td>
    <td>Simone Fulle</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q52115913</td>
    <td>Andreas H Göller</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q52116355</td>
    <td>Natália Aniceto</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q52125081</td>
    <td>Lothar Terfloth</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q5301676</td>
    <td>Douglas Kell</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q53345413</td>
    <td>Antonio de la Vega de León</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q54234793</td>
    <td>Dharmendra K. Yadav</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q54665519</td>
    <td>Francesco Luigi Gervasio</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q54859263</td>
    <td>Samantha Kanza</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q55095454</td>
    <td>Gareth Owen</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q55097518</td>
    <td>Priyanka Banerjee</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q55232632</td>
    <td>David C. Reutens</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q5550048</td>
    <td>Gerard Kleywegt</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q55657580</td>
    <td>Matthias Bauer</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q55704462</td>
    <td>Hugo Froufe</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q55714836</td>
    <td>Agostino Marrazzo</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q56027760</td>
    <td>Christopher M Grulke</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q56084718</td>
    <td>Prasun Dutta</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q56396620</td>
    <td>Andrey Yerin</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q56422342</td>
    <td>Akanksha Rajput</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q56537163</td>
    <td>Ernest Giralt</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q56747874</td>
    <td>Richard L Marchese Robinson</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q56798427</td>
    <td>Feijun Luo</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q56800381</td>
    <td>Gilles Marcou</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q56812232</td>
    <td>Vinita Periwal</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q56986123</td>
    <td>Jian-Yu Shi</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q57012103</td>
    <td>Giuseppe Di Fatta</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q57021746</td>
    <td>Luca Pireddu</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q57023371</td>
    <td>Nicola Marzari</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q57023970</td>
    <td>Robert J Allaway</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q57027586</td>
    <td>Mohamed Diwan M AbdulHameed</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q57030289</td>
    <td>Florian Mrugalla</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q57056691</td>
    <td>Neil Swainston</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q57056698</td>
    <td>Pablo Carbonell</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q57151433</td>
    <td>Nicolas Bosc</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q57157739</td>
    <td>Hai Pham-The</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q57163014</td>
    <td>Giuseppe Felice Mangiatordi</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q57206547</td>
    <td>Jorge Comas</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q57316555</td>
    <td>Daisuke Kihara</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q57394623</td>
    <td>Julio C Facelli</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q57415835</td>
    <td>Ming Hao</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q57415846</td>
    <td>Tiejun Cheng</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q57635287</td>
    <td>Richard Tzong-Han Tsai</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q57678540</td>
    <td>Giovanni Pizzi</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q57759407</td>
    <td>Francisco Belchí Guillamón</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q58059488</td>
    <td>Antonino Fiannaca</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q58059503</td>
    <td>Alfonso Urso</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q58059510</td>
    <td>Riccardo Rizzo</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q58085615</td>
    <td>Mauricio Esguerra</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q58226551</td>
    <td>Rene Meier</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q58336728</td>
    <td>Wan Kyu Kim</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q58797761</td>
    <td>David Salgado</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q58804579</td>
    <td>Willem P van Hoorn</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q58890745</td>
    <td>Peter E Shaw</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q59520206</td>
    <td>Mathilde Koch</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q59542599</td>
    <td>Nicholas Gibbins</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q59555104</td>
    <td>Maria João R.P. Queiroz</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q59668391</td>
    <td>Dominique Sydow</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q59689151</td>
    <td>Dawid Warszycki</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q60465926</td>
    <td>Haruki Nakamura</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q60651741</td>
    <td>Francis Atkinson</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q60668160</td>
    <td>Despoina Magka</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q61046796</td>
    <td>Dieter Jahn</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q61055226</td>
    <td>Antanas Vaitkus</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q61121954</td>
    <td>Ivana Blaženović</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q61142053</td>
    <td>Neeraj Kumar Rajput</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q61456437</td>
    <td>Lindsey Burggraaff</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q6153626</td>
    <td>Janet Thornton</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q61896693</td>
    <td>Holger Merlitz</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q62130109</td>
    <td>O Anatole von Lilienfeld</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q62676031</td>
    <td>Pavel Banáš</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q62676269</td>
    <td>Thomas E Cheatham</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q63351119</td>
    <td>Yannick Djoumbou Feunang</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q64167432</td>
    <td>Wilmer Leal</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q64358327</td>
    <td>Franziska Hufsky</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q64517973</td>
    <td>Rui Abreu</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q64865729</td>
    <td>S. Joshua Swamidass</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q65088041</td>
    <td>Kathrin Heikamp</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q65088044</td>
    <td>Dilyana Dimova</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q65963317</td>
    <td>Piotr Zielenkiewicz</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q67166600</td>
    <td>Veronika Navrátilová</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q67222611</td>
    <td>Thomas Sander</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q67222613</td>
    <td>Christian Rufener</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q67222616</td>
    <td>Michaël Zasso</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q70965993</td>
    <td>Anna Palczewska</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q71033158</td>
    <td>Martin Vogt</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q71033415</td>
    <td>Britta Nisius</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q75658782</td>
    <td>Yehoshua Perl</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q79294479</td>
    <td>Tatsuya Akutsu</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q7932748</td>
    <td>Vinod Scaria</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q82422361</td>
    <td>William W L Wong</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q82814507</td>
    <td>Sarah R Langdon</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q84253690</td>
    <td>Pablo Conesa</td>
  </tr>
  <tr>
    <td>1</td>
    <td>http://www.wikidata.org/entity/Q84287067</td>
    <td>Mona Elbadawi-Sidhu</td>
  </tr>
</table>
## Code examples
### curl
```shell
curl -o prolificAuthorsAll.rq https://raw.githubusercontent.com/jcheminform/useful-queries/master/sparql/prolificAuthorsAll.rq
curl -H "Accept: text/tab-separated-values" -G https://query.wikidata.org/bigdata/namespace/wdq/sparql --data-urlencode query@prolificAuthorsAll.rq
```
