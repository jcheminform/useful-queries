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
  <tr>
    <td>13</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q32565639">Sunghwan Kim</a> (<a href="http://www.wikidata.org/entity/Q32565639">edit</a>)</td>
  </tr>
  <tr>
    <td>12</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q28946543">Robert C Glen</a> (<a href="http://www.wikidata.org/entity/Q28946543">edit</a>)</td>
  </tr>
  <tr>
    <td>12</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q44680976">Radka Svobodová Vařeková</a> (<a href="http://www.wikidata.org/entity/Q44680976">edit</a>)</td>
  </tr>
  <tr>
    <td>12</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q57198570">Andrzej Bojarski</a> (<a href="http://www.wikidata.org/entity/Q57198570">edit</a>)</td>
  </tr>
  <tr>
    <td>11</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q30086276">Gerard J. P. van Westen</a> (<a href="http://www.wikidata.org/entity/Q30086276">edit</a>)</td>
  </tr>
  <tr>
    <td>10</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q26707540">David J. Wild</a> (<a href="http://www.wikidata.org/entity/Q26707540">edit</a>)</td>
  </tr>
  <tr>
    <td>10</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q27061849">Nina Jeliazkova</a> (<a href="http://www.wikidata.org/entity/Q27061849">edit</a>)</td>
  </tr>
  <tr>
    <td>10</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q27902110">Janna Hastings</a> (<a href="http://www.wikidata.org/entity/Q27902110">edit</a>)</td>
  </tr>
  <tr>
    <td>9</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q44682520">Crina-Maria Ionescu</a> (<a href="http://www.wikidata.org/entity/Q44682520">edit</a>)</td>
  </tr>
  <tr>
    <td>9</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q44682699">Stanislav Geidl</a> (<a href="http://www.wikidata.org/entity/Q44682699">edit</a>)</td>
  </tr>
  <tr>
    <td>9</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q53843624">Achim Zielesny</a> (<a href="http://www.wikidata.org/entity/Q53843624">edit</a>)</td>
  </tr>
  <tr>
    <td>8</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q18609784">Jürgen Bajorath</a> (<a href="http://www.wikidata.org/entity/Q18609784">edit</a>)</td>
  </tr>
  <tr>
    <td>8</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q42201848">Gerhard Wolber</a> (<a href="http://www.wikidata.org/entity/Q42201848">edit</a>)</td>
  </tr>
  <tr>
    <td>8</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370829">David Sehnal</a> (<a href="http://www.wikidata.org/entity/Q43370829">edit</a>)</td>
  </tr>
  <tr>
    <td>8</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370883">Ola Engkvist</a> (<a href="http://www.wikidata.org/entity/Q43370883">edit</a>)</td>
  </tr>
  <tr>
    <td>8</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q5727848">Henry S. Rzepa</a> (<a href="http://www.wikidata.org/entity/Q5727848">edit</a>)</td>
  </tr>
  <tr>
    <td>8</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q84287725">Georg Hinselmann</a> (<a href="http://www.wikidata.org/entity/Q84287725">edit</a>)</td>
  </tr>
  <tr>
    <td>7</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q27065426">Rajarshi Guha</a> (<a href="http://www.wikidata.org/entity/Q27065426">edit</a>)</td>
  </tr>
  <tr>
    <td>7</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q27768873">Peter Ertl</a> (<a href="http://www.wikidata.org/entity/Q27768873">edit</a>)</td>
  </tr>
  <tr>
    <td>7</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q28946549">Sam E. Adams</a> (<a href="http://www.wikidata.org/entity/Q28946549">edit</a>)</td>
  </tr>
  <tr>
    <td>7</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q30362344">Igor V. Tetko</a> (<a href="http://www.wikidata.org/entity/Q30362344">edit</a>)</td>
  </tr>
  <tr>
    <td>7</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q51200321">Tingjun Hou</a> (<a href="http://www.wikidata.org/entity/Q51200321">edit</a>)</td>
  </tr>
  <tr>
    <td>7</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q51615601">Gisbert Schneider</a> (<a href="http://www.wikidata.org/entity/Q51615601">edit</a>)</td>
  </tr>
  <tr>
    <td>7</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q56084692">Sabina Smusz</a> (<a href="http://www.wikidata.org/entity/Q56084692">edit</a>)</td>
  </tr>
  <tr>
    <td>7</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q84301537">Sergii Novotarskyi</a> (<a href="http://www.wikidata.org/entity/Q84301537">edit</a>)</td>
  </tr>
  <tr>
    <td>6</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q21031914">Gregor Fels</a> (<a href="http://www.wikidata.org/entity/Q21031914">edit</a>)</td>
  </tr>
  <tr>
    <td>6</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q28540731">Noel O'Boyle</a> (<a href="http://www.wikidata.org/entity/Q28540731">edit</a>)</td>
  </tr>
  <tr>
    <td>6</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q29043209">Sorel Muresan</a> (<a href="http://www.wikidata.org/entity/Q29043209">edit</a>)</td>
  </tr>
  <tr>
    <td>6</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q29389602">Roger Sayle</a> (<a href="http://www.wikidata.org/entity/Q29389602">edit</a>)</td>
  </tr>
  <tr>
    <td>6</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q29460345">Denis Fourches</a> (<a href="http://www.wikidata.org/entity/Q29460345">edit</a>)</td>
  </tr>
  <tr>
    <td>6</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q30013427">Jeremy G. Frey</a> (<a href="http://www.wikidata.org/entity/Q30013427">edit</a>)</td>
  </tr>
  <tr>
    <td>6</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q42716526">Gregory A. Landrum</a> (<a href="http://www.wikidata.org/entity/Q42716526">edit</a>)</td>
  </tr>
  <tr>
    <td>6</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q53841786">Wolf-Dietrich Ihlenfeldt</a> (<a href="http://www.wikidata.org/entity/Q53841786">edit</a>)</td>
  </tr>
  <tr>
    <td>6</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q56509036">Jan A Kors</a> (<a href="http://www.wikidata.org/entity/Q56509036">edit</a>)</td>
  </tr>
  <tr>
    <td>6</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q63676494">Isidro Cortés-Ciriano</a> (<a href="http://www.wikidata.org/entity/Q63676494">edit</a>)</td>
  </tr>
  <tr>
    <td>5</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q21264701">Sonja Herres-Pawlis</a> (<a href="http://www.wikidata.org/entity/Q21264701">edit</a>)</td>
  </tr>
  <tr>
    <td>5</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q28540892">Oliver Fiehn</a> (<a href="http://www.wikidata.org/entity/Q28540892">edit</a>)</td>
  </tr>
  <tr>
    <td>5</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q28796322">John W Mayfield</a> (<a href="http://www.wikidata.org/entity/Q28796322">edit</a>)</td>
  </tr>
  <tr>
    <td>5</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q28865170">Jonathan Alvarsson</a> (<a href="http://www.wikidata.org/entity/Q28865170">edit</a>)</td>
  </tr>
  <tr>
    <td>5</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q28946652">Geoffrey R. Hutchison</a> (<a href="http://www.wikidata.org/entity/Q28946652">edit</a>)</td>
  </tr>
  <tr>
    <td>5</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q29052381">Tobias Kind</a> (<a href="http://www.wikidata.org/entity/Q29052381">edit</a>)</td>
  </tr>
  <tr>
    <td>5</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q29387592">Marcus D. Hanwell</a> (<a href="http://www.wikidata.org/entity/Q29387592">edit</a>)</td>
  </tr>
  <tr>
    <td>5</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q30269285">Ewgenij Proschak</a> (<a href="http://www.wikidata.org/entity/Q30269285">edit</a>)</td>
  </tr>
  <tr>
    <td>5</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q40222626">Adriaan P IJzerman</a> (<a href="http://www.wikidata.org/entity/Q40222626">edit</a>)</td>
  </tr>
  <tr>
    <td>5</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370869">Stefan Mordalski</a> (<a href="http://www.wikidata.org/entity/Q43370869">edit</a>)</td>
  </tr>
  <tr>
    <td>5</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q52083694">Knut Baumann</a> (<a href="http://www.wikidata.org/entity/Q52083694">edit</a>)</td>
  </tr>
  <tr>
    <td>5</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q56247792">Dong-Sheng Cao</a> (<a href="http://www.wikidata.org/entity/Q56247792">edit</a>)</td>
  </tr>
  <tr>
    <td>4</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q28133217">Christopher Southan</a> (<a href="http://www.wikidata.org/entity/Q28133217">edit</a>)</td>
  </tr>
  <tr>
    <td>4</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q28540616">Thomas Hankemeier</a> (<a href="http://www.wikidata.org/entity/Q28540616">edit</a>)</td>
  </tr>
  <tr>
    <td>4</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q28923515">Colin Batchelor</a> (<a href="http://www.wikidata.org/entity/Q28923515">edit</a>)</td>
  </tr>
  <tr>
    <td>4</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q28925903">Valery Tkachenko</a> (<a href="http://www.wikidata.org/entity/Q28925903">edit</a>)</td>
  </tr>
  <tr>
    <td>4</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q28946674">Anna Gaulton</a> (<a href="http://www.wikidata.org/entity/Q28946674">edit</a>)</td>
  </tr>
  <tr>
    <td>4</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q29387575">Arvid Berg</a> (<a href="http://www.wikidata.org/entity/Q29387575">edit</a>)</td>
  </tr>
  <tr>
    <td>4</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q29998906">Oliver Kohlbacher</a> (<a href="http://www.wikidata.org/entity/Q29998906">edit</a>)</td>
  </tr>
  <tr>
    <td>4</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q30045595">Alex M Clark</a> (<a href="http://www.wikidata.org/entity/Q30045595">edit</a>)</td>
  </tr>
  <tr>
    <td>4</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q30104439">John P. Overington</a> (<a href="http://www.wikidata.org/entity/Q30104439">edit</a>)</td>
  </tr>
  <tr>
    <td>4</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q41876113">Frank M. Boeckler</a> (<a href="http://www.wikidata.org/entity/Q41876113">edit</a>)</td>
  </tr>
  <tr>
    <td>4</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q42155173">Junmei Wang</a> (<a href="http://www.wikidata.org/entity/Q42155173">edit</a>)</td>
  </tr>
  <tr>
    <td>4</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q42571511">Wesley Schaal</a> (<a href="http://www.wikidata.org/entity/Q42571511">edit</a>)</td>
  </tr>
  <tr>
    <td>4</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q42719788">Jean-Louis Reymond</a> (<a href="http://www.wikidata.org/entity/Q42719788">edit</a>)</td>
  </tr>
  <tr>
    <td>4</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q42720048">Mahendra Awale</a> (<a href="http://www.wikidata.org/entity/Q42720048">edit</a>)</td>
  </tr>
  <tr>
    <td>4</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370862">Daniel Svozil</a> (<a href="http://www.wikidata.org/entity/Q43370862">edit</a>)</td>
  </tr>
  <tr>
    <td>4</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370904">David Hoksza</a> (<a href="http://www.wikidata.org/entity/Q43370904">edit</a>)</td>
  </tr>
  <tr>
    <td>4</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q53843262">Oliver Koch</a> (<a href="http://www.wikidata.org/entity/Q53843262">edit</a>)</td>
  </tr>
  <tr>
    <td>4</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q55406442">Miquel Rojas-Chertó</a> (<a href="http://www.wikidata.org/entity/Q55406442">edit</a>)</td>
  </tr>
  <tr>
    <td>4</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q61826780">Luc Patiny</a> (<a href="http://www.wikidata.org/entity/Q61826780">edit</a>)</td>
  </tr>
  <tr>
    <td>4</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q64167646">Emilio Benfenati</a> (<a href="http://www.wikidata.org/entity/Q64167646">edit</a>)</td>
  </tr>
  <tr>
    <td>4</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q64167890">Hongming Chen</a> (<a href="http://www.wikidata.org/entity/Q64167890">edit</a>)</td>
  </tr>
  <tr>
    <td>4</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q64869606">Thorsten Meinl</a> (<a href="http://www.wikidata.org/entity/Q64869606">edit</a>)</td>
  </tr>
  <tr>
    <td>3</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q18611251">Stephen R. Heller</a> (<a href="http://www.wikidata.org/entity/Q18611251">edit</a>)</td>
  </tr>
  <tr>
    <td>3</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q19845602">Barbara Zdrazil</a> (<a href="http://www.wikidata.org/entity/Q19845602">edit</a>)</td>
  </tr>
  <tr>
    <td>3</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q19845641">Chris T. Evelo</a> (<a href="http://www.wikidata.org/entity/Q19845641">edit</a>)</td>
  </tr>
  <tr>
    <td>3</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q27863244">Emma L. Schymanski</a> (<a href="http://www.wikidata.org/entity/Q27863244">edit</a>)</td>
  </tr>
  <tr>
    <td>3</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q28194921">Michel Dumontier</a> (<a href="http://www.wikidata.org/entity/Q28194921">edit</a>)</td>
  </tr>
  <tr>
    <td>3</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q29389590">David M Jessop</a> (<a href="http://www.wikidata.org/entity/Q29389590">edit</a>)</td>
  </tr>
  <tr>
    <td>3</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q29389599">Daniel M Lowe</a> (<a href="http://www.wikidata.org/entity/Q29389599">edit</a>)</td>
  </tr>
  <tr>
    <td>3</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q29998084">Vedrin Jeliazkov</a> (<a href="http://www.wikidata.org/entity/Q29998084">edit</a>)</td>
  </tr>
  <tr>
    <td>3</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q30046332">Samuel Lampa</a> (<a href="http://www.wikidata.org/entity/Q30046332">edit</a>)</td>
  </tr>
  <tr>
    <td>3</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q30503825">Roberto Todeschini</a> (<a href="http://www.wikidata.org/entity/Q30503825">edit</a>)</td>
  </tr>
  <tr>
    <td>3</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q30853931">Alan McNaught</a> (<a href="http://www.wikidata.org/entity/Q30853931">edit</a>)</td>
  </tr>
  <tr>
    <td>3</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q30853960">Igor Pletnev</a> (<a href="http://www.wikidata.org/entity/Q30853960">edit</a>)</td>
  </tr>
  <tr>
    <td>3</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q30853976">Dmitrii Tchekhovskoi</a> (<a href="http://www.wikidata.org/entity/Q30853976">edit</a>)</td>
  </tr>
  <tr>
    <td>3</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q30862909">Tim Vandermeersch</a> (<a href="http://www.wikidata.org/entity/Q30862909">edit</a>)</td>
  </tr>
  <tr>
    <td>3</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q33035163">George Papadatos</a> (<a href="http://www.wikidata.org/entity/Q33035163">edit</a>)</td>
  </tr>
  <tr>
    <td>3</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q33035164">Anne Hersey</a> (<a href="http://www.wikidata.org/entity/Q33035164">edit</a>)</td>
  </tr>
  <tr>
    <td>3</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q37611768">Klaus R. Liedl</a> (<a href="http://www.wikidata.org/entity/Q37611768">edit</a>)</td>
  </tr>
  <tr>
    <td>3</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q37611850">Kristina M. Hettne</a> (<a href="http://www.wikidata.org/entity/Q37611850">edit</a>)</td>
  </tr>
  <tr>
    <td>3</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q37611901">Erik M van Mulligen</a> (<a href="http://www.wikidata.org/entity/Q37611901">edit</a>)</td>
  </tr>
  <tr>
    <td>3</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q37829831">Youyong Li</a> (<a href="http://www.wikidata.org/entity/Q37829831">edit</a>)</td>
  </tr>
  <tr>
    <td>3</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q37836608">Wolfgang Sippl</a> (<a href="http://www.wikidata.org/entity/Q37836608">edit</a>)</td>
  </tr>
  <tr>
    <td>3</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q42726535">Tiago Rodrigues</a> (<a href="http://www.wikidata.org/entity/Q42726535">edit</a>)</td>
  </tr>
  <tr>
    <td>3</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370820">Christoph Ruttkies</a> (<a href="http://www.wikidata.org/entity/Q43370820">edit</a>)</td>
  </tr>
  <tr>
    <td>3</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370880">Georgios Drakakis</a> (<a href="http://www.wikidata.org/entity/Q43370880">edit</a>)</td>
  </tr>
  <tr>
    <td>3</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370892">Jakub Galgonek</a> (<a href="http://www.wikidata.org/entity/Q43370892">edit</a>)</td>
  </tr>
  <tr>
    <td>3</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370900">César R García-Jacas</a> (<a href="http://www.wikidata.org/entity/Q43370900">edit</a>)</td>
  </tr>
  <tr>
    <td>3</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370957">Rafał Kurczab</a> (<a href="http://www.wikidata.org/entity/Q43370957">edit</a>)</td>
  </tr>
  <tr>
    <td>3</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43388721">Robert M Hanson</a> (<a href="http://www.wikidata.org/entity/Q43388721">edit</a>)</td>
  </tr>
  <tr>
    <td>3</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q44682790">Tomáš Bouchal</a> (<a href="http://www.wikidata.org/entity/Q44682790">edit</a>)</td>
  </tr>
  <tr>
    <td>3</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q46155617">Jonathan M. Goodman</a> (<a href="http://www.wikidata.org/entity/Q46155617">edit</a>)</td>
  </tr>
  <tr>
    <td>3</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q49740420">Ralph Müller-Pfefferkorn</a> (<a href="http://www.wikidata.org/entity/Q49740420">edit</a>)</td>
  </tr>
  <tr>
    <td>3</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q55406542">Theo Reijmers</a> (<a href="http://www.wikidata.org/entity/Q55406542">edit</a>)</td>
  </tr>
  <tr>
    <td>3</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q55657580">Matthias Bauer</a> (<a href="http://www.wikidata.org/entity/Q55657580">edit</a>)</td>
  </tr>
  <tr>
    <td>3</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q57953722">Nikolay Kochev</a> (<a href="http://www.wikidata.org/entity/Q57953722">edit</a>)</td>
  </tr>
  <tr>
    <td>3</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q60558900">Andreas Karwath</a> (<a href="http://www.wikidata.org/entity/Q60558900">edit</a>)</td>
  </tr>
  <tr>
    <td>3</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q60961322">Jiří Vondrášek</a> (<a href="http://www.wikidata.org/entity/Q60961322">edit</a>)</td>
  </tr>
  <tr>
    <td>3</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q63208429">Sebastian Böcker</a> (<a href="http://www.wikidata.org/entity/Q63208429">edit</a>)</td>
  </tr>
  <tr>
    <td>3</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q65088027">Anne Mai Wassermann</a> (<a href="http://www.wikidata.org/entity/Q65088027">edit</a>)</td>
  </tr>
  <tr>
    <td>3</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q7177718">Peter Willett</a> (<a href="http://www.wikidata.org/entity/Q7177718">edit</a>)</td>
  </tr>
  <tr>
    <td>3</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q7440973">Sean Ekins</a> (<a href="http://www.wikidata.org/entity/Q7440973">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q109081">Johann Gasteiger</a> (<a href="http://www.wikidata.org/entity/Q109081">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q1222879">Dieter Steinhilber</a> (<a href="http://www.wikidata.org/entity/Q1222879">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q126812">Barbara Kirchner</a> (<a href="http://www.wikidata.org/entity/Q126812">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q12788090">Dušanka Janežič</a> (<a href="http://www.wikidata.org/entity/Q12788090">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q15995097">C. Lee Giles</a> (<a href="http://www.wikidata.org/entity/Q15995097">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q16335154">Alfonso Valencia</a> (<a href="http://www.wikidata.org/entity/Q16335154">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q17021355">Jean-Claude Bradley</a> (<a href="http://www.wikidata.org/entity/Q17021355">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q18611260">Guenter Grethe</a> (<a href="http://www.wikidata.org/entity/Q18611260">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q19845653">Stefan Senger</a> (<a href="http://www.wikidata.org/entity/Q19845653">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q24013775">Sereina Riniker</a> (<a href="http://www.wikidata.org/entity/Q24013775">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q28052829">Saulius Gražulis</a> (<a href="http://www.wikidata.org/entity/Q28052829">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q28540435">Jarl Wikberg</a> (<a href="http://www.wikidata.org/entity/Q28540435">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q28541023">Steffen Neumann</a> (<a href="http://www.wikidata.org/entity/Q28541023">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q28541054">Haralambos Sarimveis</a> (<a href="http://www.wikidata.org/entity/Q28541054">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q28747176">Jos Kleinjans</a> (<a href="http://www.wikidata.org/entity/Q28747176">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q28923506">Lars Carlsson</a> (<a href="http://www.wikidata.org/entity/Q28923506">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q29032923">Paula de Matos</a> (<a href="http://www.wikidata.org/entity/Q29032923">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q29389592">Lezan Hawizy</a> (<a href="http://www.wikidata.org/entity/Q29389592">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q29405902">Stefan Kuhn</a> (<a href="http://www.wikidata.org/entity/Q29405902">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q29406424">Kenneth Haug</a> (<a href="http://www.wikidata.org/entity/Q29406424">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q30046697">Jean-Loup Faulon</a> (<a href="http://www.wikidata.org/entity/Q30046697">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q30112600">Obdulia Rabal</a> (<a href="http://www.wikidata.org/entity/Q30112600">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q30347500">Vladimir B. Bajic</a> (<a href="http://www.wikidata.org/entity/Q30347500">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q30503831">João Aires de Sousa</a> (<a href="http://www.wikidata.org/entity/Q30503831">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q38323677">Tudor I Oprea</a> (<a href="http://www.wikidata.org/entity/Q38323677">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q38639158">Chun-Wei Tung</a> (<a href="http://www.wikidata.org/entity/Q38639158">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q39382967">Yovani Marrero-Ponce</a> (<a href="http://www.wikidata.org/entity/Q39382967">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q39484473">Harald H Sitte</a> (<a href="http://www.wikidata.org/entity/Q39484473">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q40403099">Xiaomin Luo</a> (<a href="http://www.wikidata.org/entity/Q40403099">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q40615839">Björn A Grüning</a> (<a href="http://www.wikidata.org/entity/Q40615839">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q41049168">Francisco M. Couto</a> (<a href="http://www.wikidata.org/entity/Q41049168">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q41373025">Viviana Consonni</a> (<a href="http://www.wikidata.org/entity/Q41373025">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q41585873">Daniel Neagu</a> (<a href="http://www.wikidata.org/entity/Q41585873">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q41790698">Koen Augustyns</a> (<a href="http://www.wikidata.org/entity/Q41790698">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q42093041">Ingo Krossing</a> (<a href="http://www.wikidata.org/entity/Q42093041">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q42098378">Florian Nigsch</a> (<a href="http://www.wikidata.org/entity/Q42098378">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q42211866">Matthieu Montes</a> (<a href="http://www.wikidata.org/entity/Q42211866">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q42628458">Dario Greco</a> (<a href="http://www.wikidata.org/entity/Q42628458">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q42873154">Jonathan D. Hirst</a> (<a href="http://www.wikidata.org/entity/Q42873154">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q42912645">Steven M. Bachrach</a> (<a href="http://www.wikidata.org/entity/Q42912645">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43154574">Vladimir Poroikov</a> (<a href="http://www.wikidata.org/entity/Q43154574">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43291987">Stuart J. Chalk</a> (<a href="http://www.wikidata.org/entity/Q43291987">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370243">Kalai Vanii Jayaseelan</a> (<a href="http://www.wikidata.org/entity/Q43370243">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370281">Nico Adams</a> (<a href="http://www.wikidata.org/entity/Q43370281">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370334">Tomáš Pluskal</a> (<a href="http://www.wikidata.org/entity/Q43370334">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370812">Alexey Lagunin</a> (<a href="http://www.wikidata.org/entity/Q43370812">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370813">Cerys Willoughby</a> (<a href="http://www.wikidata.org/entity/Q43370813">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370817">Ben O'Steen</a> (<a href="http://www.wikidata.org/entity/Q43370817">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370827">Jonathan D Tyzack</a> (<a href="http://www.wikidata.org/entity/Q43370827">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370828">Lukáš Pravda</a> (<a href="http://www.wikidata.org/entity/Q43370828">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370845">Andrés Bernal</a> (<a href="http://www.wikidata.org/entity/Q43370845">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370846">Julien Wist</a> (<a href="http://www.wikidata.org/entity/Q43370846">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370855">Panos Kalnis</a> (<a href="http://www.wikidata.org/entity/Q43370855">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370856">Davide Ballabio</a> (<a href="http://www.wikidata.org/entity/Q43370856">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370872">David Marcus</a> (<a href="http://www.wikidata.org/entity/Q43370872">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370876">Nicholas J Mason</a> (<a href="http://www.wikidata.org/entity/Q43370876">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370879">Richard Lewis</a> (<a href="http://www.wikidata.org/entity/Q43370879">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370881">Lewis H Mervin</a> (<a href="http://www.wikidata.org/entity/Q43370881">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370888">José L. Medina-Franco</a> (<a href="http://www.wikidata.org/entity/Q43370888">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370898">Paolo Tosco</a> (<a href="http://www.wikidata.org/entity/Q43370898">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370901">Stephen J. Barigye</a> (<a href="http://www.wikidata.org/entity/Q43370901">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370924">Ines Thiele</a> (<a href="http://www.wikidata.org/entity/Q43370924">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370926">Sérgio Matos</a> (<a href="http://www.wikidata.org/entity/Q43370926">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370931">Jens Thomas</a> (<a href="http://www.wikidata.org/entity/Q43370931">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370955">Mingyue Zheng</a> (<a href="http://www.wikidata.org/entity/Q43370955">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370998">Marco Capuccini</a> (<a href="http://www.wikidata.org/entity/Q43370998">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43371002">Lazaros Mavridis</a> (<a href="http://www.wikidata.org/entity/Q43371002">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43371005">Jochen Junker</a> (<a href="http://www.wikidata.org/entity/Q43371005">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43371010">Robert Günther</a> (<a href="http://www.wikidata.org/entity/Q43371010">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43371017">Francois Berenger</a> (<a href="http://www.wikidata.org/entity/Q43371017">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43371023">Nicole Jung</a> (<a href="http://www.wikidata.org/entity/Q43371023">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43371028">George Van Den Driessche</a> (<a href="http://www.wikidata.org/entity/Q43371028">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43371035">Yufeng J. Tseng</a> (<a href="http://www.wikidata.org/entity/Q43371035">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43371037">Huiyong Sun</a> (<a href="http://www.wikidata.org/entity/Q43371037">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43837602">Kamel Mansouri</a> (<a href="http://www.wikidata.org/entity/Q43837602">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43837665">Andrew D McEachran</a> (<a href="http://www.wikidata.org/entity/Q43837665">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q44682954">Ruben Abagyan</a> (<a href="http://www.wikidata.org/entity/Q44682954">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q46275105">Dmitry Filimonov</a> (<a href="http://www.wikidata.org/entity/Q46275105">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q4720252">Alexander Tropsha</a> (<a href="http://www.wikidata.org/entity/Q4720252">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q47501420">Markus Wagener</a> (<a href="http://www.wikidata.org/entity/Q47501420">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q47508780">Stephen Stein</a> (<a href="http://www.wikidata.org/entity/Q47508780">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q47509086">Uli Fechner</a> (<a href="http://www.wikidata.org/entity/Q47509086">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q4758469">Andrew S.I.D. Lang</a> (<a href="http://www.wikidata.org/entity/Q4758469">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q49409340">Marcus Ennis</a> (<a href="http://www.wikidata.org/entity/Q49409340">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q49740441">Klaus-Dieter Warzecha</a> (<a href="http://www.wikidata.org/entity/Q49740441">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q49740465">André Brinkmann</a> (<a href="http://www.wikidata.org/entity/Q49740465">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q50726329">Jacob de Vlieg</a> (<a href="http://www.wikidata.org/entity/Q50726329">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q50983316">Robert D. Clark</a> (<a href="http://www.wikidata.org/entity/Q50983316">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q51782466">Johannes Kirchmair</a> (<a href="http://www.wikidata.org/entity/Q51782466">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q51878943">Hans De Winter</a> (<a href="http://www.wikidata.org/entity/Q51878943">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q52106301">Bart Lenselink</a> (<a href="http://www.wikidata.org/entity/Q52106301">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q53841690">Nikolaus Stiefl</a> (<a href="http://www.wikidata.org/entity/Q53841690">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q56027760">Christopher M Grulke</a> (<a href="http://www.wikidata.org/entity/Q56027760">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q56084691">Miguel Vazquez</a> (<a href="http://www.wikidata.org/entity/Q56084691">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q56248678">Andrius Merkys</a> (<a href="http://www.wikidata.org/entity/Q56248678">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q56419420">Anders Wallqvist</a> (<a href="http://www.wikidata.org/entity/Q56419420">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q56421877">Jeffrey P Plante</a> (<a href="http://www.wikidata.org/entity/Q56421877">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q57191385">Kai Dührkop</a> (<a href="http://www.wikidata.org/entity/Q57191385">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q57635287">Richard Tzong-Han Tsai</a> (<a href="http://www.wikidata.org/entity/Q57635287">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q58882445">Magbubah Essack</a> (<a href="http://www.wikidata.org/entity/Q58882445">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q59698544">Michal Brylinski</a> (<a href="http://www.wikidata.org/entity/Q59698544">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q60960357">Ludger A Wessjohann</a> (<a href="http://www.wikidata.org/entity/Q60960357">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q63681860">Eoin Fahy</a> (<a href="http://www.wikidata.org/entity/Q63681860">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q64750275">Franca-Maria Klingler</a> (<a href="http://www.wikidata.org/entity/Q64750275">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q64750696">Jean-François Zagury</a> (<a href="http://www.wikidata.org/entity/Q64750696">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q71034096">Karl-Heinz Baringhaus</a> (<a href="http://www.wikidata.org/entity/Q71034096">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q79792135">Rui-Xin Zhu</a> (<a href="http://www.wikidata.org/entity/Q79792135">edit</a>)</td>
  </tr>
  <tr>
    <td>2</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q84287127">Arpana Vaniya</a> (<a href="http://www.wikidata.org/entity/Q84287127">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q11867366">Juha Kere</a> (<a href="http://www.wikidata.org/entity/Q11867366">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q12364748">Ivo Leito</a> (<a href="http://www.wikidata.org/entity/Q12364748">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q1243222">Thomas Lengauer</a> (<a href="http://www.wikidata.org/entity/Q1243222">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q15285878">Cameron Neylon</a> (<a href="http://www.wikidata.org/entity/Q15285878">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q17061967">Nicola Gaston</a> (<a href="http://www.wikidata.org/entity/Q17061967">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q17177501">Pablo Echenique-Robba</a> (<a href="http://www.wikidata.org/entity/Q17177501">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q17386431">Petra Mutzel</a> (<a href="http://www.wikidata.org/entity/Q17386431">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q17489039">Shoba Ranganathan</a> (<a href="http://www.wikidata.org/entity/Q17489039">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q17516035">Jeffrey Skolnick</a> (<a href="http://www.wikidata.org/entity/Q17516035">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q19845608">Daniela Digles</a> (<a href="http://www.wikidata.org/entity/Q19845608">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q19845625">Andra Waagmeester</a> (<a href="http://www.wikidata.org/entity/Q19845625">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q19845639">Jose Brea</a> (<a href="http://www.wikidata.org/entity/Q19845639">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q2000014">John Wilbanks</a> (<a href="http://www.wikidata.org/entity/Q2000014">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q20116474">Christopher A. Lipinski</a> (<a href="http://www.wikidata.org/entity/Q20116474">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q2074784">Peter F. Stadler</a> (<a href="http://www.wikidata.org/entity/Q2074784">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q25975812">Alexandre Hocquet</a> (<a href="http://www.wikidata.org/entity/Q25975812">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q26709023">Klaus-Robert Müller</a> (<a href="http://www.wikidata.org/entity/Q26709023">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q27887604">David S Wishart</a> (<a href="http://www.wikidata.org/entity/Q27887604">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q28122093">Chanin Nantasenamat</a> (<a href="http://www.wikidata.org/entity/Q28122093">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q28320727">Heinrich Sticht</a> (<a href="http://www.wikidata.org/entity/Q28320727">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q28745439">Cristian R. Munteanu</a> (<a href="http://www.wikidata.org/entity/Q28745439">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q28854723">Martin Eklund</a> (<a href="http://www.wikidata.org/entity/Q28854723">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q28854903">Georgia Tsiliki</a> (<a href="http://www.wikidata.org/entity/Q28854903">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q28914636">Matthias Samwald</a> (<a href="http://www.wikidata.org/entity/Q28914636">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q28914639">Eric G. Prud’hommeaux</a> (<a href="http://www.wikidata.org/entity/Q28914639">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q28951592">Martin Paul Brändle</a> (<a href="http://www.wikidata.org/entity/Q28951592">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q29315318">Jens Meiler</a> (<a href="http://www.wikidata.org/entity/Q29315318">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q29405774">Masanori Arita</a> (<a href="http://www.wikidata.org/entity/Q29405774">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q29405912">Barry Hardy</a> (<a href="http://www.wikidata.org/entity/Q29405912">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q29406339">Reza M. Salek</a> (<a href="http://www.wikidata.org/entity/Q29406339">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q30046695">Jérôme Pansanel</a> (<a href="http://www.wikidata.org/entity/Q30046695">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q30046701">Gilleain Torrance</a> (<a href="http://www.wikidata.org/entity/Q30046701">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q30104387">Romualdo Benigni</a> (<a href="http://www.wikidata.org/entity/Q30104387">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q30170265">Hans-Ulrich Demuth</a> (<a href="http://www.wikidata.org/entity/Q30170265">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q30190636">Teresa Carlomagno</a> (<a href="http://www.wikidata.org/entity/Q30190636">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q30225131">Joan-Emma Shea</a> (<a href="http://www.wikidata.org/entity/Q30225131">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q30318445">Sophia Ananiadou</a> (<a href="http://www.wikidata.org/entity/Q30318445">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q30503169">Michael M. Hoffman</a> (<a href="http://www.wikidata.org/entity/Q30503169">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q30503828">Maria Grishina</a> (<a href="http://www.wikidata.org/entity/Q30503828">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q30503970">Walter S Leal</a> (<a href="http://www.wikidata.org/entity/Q30503970">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q30505440">Yong-Yeol Ahn</a> (<a href="http://www.wikidata.org/entity/Q30505440">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q30518653">Neil D. Young</a> (<a href="http://www.wikidata.org/entity/Q30518653">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q30518683">Andreas Hofmann</a> (<a href="http://www.wikidata.org/entity/Q30518683">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q30766768">Anja Jentzsch</a> (<a href="http://www.wikidata.org/entity/Q30766768">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q30828813">Eyke Hüllermeier</a> (<a href="http://www.wikidata.org/entity/Q30828813">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q30863103">Michael Banck</a> (<a href="http://www.wikidata.org/entity/Q30863103">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q32416912">Eileen Socher</a> (<a href="http://www.wikidata.org/entity/Q32416912">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q32634180">George Hripcsak</a> (<a href="http://www.wikidata.org/entity/Q32634180">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q33133975">Susie Stephens</a> (<a href="http://www.wikidata.org/entity/Q33133975">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q3383843">Pierre Baldi</a> (<a href="http://www.wikidata.org/entity/Q3383843">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q37368799">Michal Otyepka</a> (<a href="http://www.wikidata.org/entity/Q37368799">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q37377779">Anna Vulpetti</a> (<a href="http://www.wikidata.org/entity/Q37377779">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q37384288">Matthew D. Krasowski</a> (<a href="http://www.wikidata.org/entity/Q37384288">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q37390028">Christoph Flamm</a> (<a href="http://www.wikidata.org/entity/Q37390028">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q37392250">Manuel C. Peitsch</a> (<a href="http://www.wikidata.org/entity/Q37392250">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q37830599">Ingebrigt Sylte</a> (<a href="http://www.wikidata.org/entity/Q37830599">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q38174461">Michael Berthold</a> (<a href="http://www.wikidata.org/entity/Q38174461">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q38174474">Stephan Beisken</a> (<a href="http://www.wikidata.org/entity/Q38174474">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q38330768">Mauro D'Amato</a> (<a href="http://www.wikidata.org/entity/Q38330768">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q38544936">Olli T Pentikäinen</a> (<a href="http://www.wikidata.org/entity/Q38544936">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q38601597">John F. Wambaugh</a> (<a href="http://www.wikidata.org/entity/Q38601597">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q38641963">José Luís Oliveira</a> (<a href="http://www.wikidata.org/entity/Q38641963">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q38800696">Ahmed M El Kerdawy</a> (<a href="http://www.wikidata.org/entity/Q38800696">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q39049629">Daniel Moser</a> (<a href="http://www.wikidata.org/entity/Q39049629">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q39657849">Anita R Maguire</a> (<a href="http://www.wikidata.org/entity/Q39657849">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q39724540">Lluís Arola</a> (<a href="http://www.wikidata.org/entity/Q39724540">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q39972241">Syed A. Rahman</a> (<a href="http://www.wikidata.org/entity/Q39972241">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q39972290">Gemma L. Holliday</a> (<a href="http://www.wikidata.org/entity/Q39972290">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q40023319">Simon J. Coles</a> (<a href="http://www.wikidata.org/entity/Q40023319">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q40080540">Ferran Sanz</a> (<a href="http://www.wikidata.org/entity/Q40080540">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q40285012">Daan P Geerke</a> (<a href="http://www.wikidata.org/entity/Q40285012">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q40364172">Antonio Rescifina</a> (<a href="http://www.wikidata.org/entity/Q40364172">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q40389326">Oldamur Hollóczki</a> (<a href="http://www.wikidata.org/entity/Q40389326">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q40486468">Csaba Hetényi</a> (<a href="http://www.wikidata.org/entity/Q40486468">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q41048978">Ronald Taylor</a> (<a href="http://www.wikidata.org/entity/Q41048978">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q41049335">Jose A. Seoane</a> (<a href="http://www.wikidata.org/entity/Q41049335">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q41049805">Juan Carlos Mobarec</a> (<a href="http://www.wikidata.org/entity/Q41049805">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q41050128">Antreas Afantitis</a> (<a href="http://www.wikidata.org/entity/Q41050128">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q41099546">Matthew Bashton</a> (<a href="http://www.wikidata.org/entity/Q41099546">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q41602447">Robert Preissner</a> (<a href="http://www.wikidata.org/entity/Q41602447">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q41610209">David W. Ritchie</a> (<a href="http://www.wikidata.org/entity/Q41610209">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q41728407">Mi-hyun Kim</a> (<a href="http://www.wikidata.org/entity/Q41728407">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q41728850">Tomasz Puzyn</a> (<a href="http://www.wikidata.org/entity/Q41728850">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q42201814">Miguel Quirós</a> (<a href="http://www.wikidata.org/entity/Q42201814">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q42228266">Georgia Melagraki</a> (<a href="http://www.wikidata.org/entity/Q42228266">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q42326124">Norbert Haider</a> (<a href="http://www.wikidata.org/entity/Q42326124">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q42326677">Robin B. Gasser</a> (<a href="http://www.wikidata.org/entity/Q42326677">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q42386872">John T Prince</a> (<a href="http://www.wikidata.org/entity/Q42386872">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q42418395">Naomie Salim</a> (<a href="http://www.wikidata.org/entity/Q42418395">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q42425503">José María Gutiérrez</a> (<a href="http://www.wikidata.org/entity/Q42425503">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q42612964">Kirill Okhotnikov</a> (<a href="http://www.wikidata.org/entity/Q42612964">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q42634693">Maciej Wójcikowski</a> (<a href="http://www.wikidata.org/entity/Q42634693">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q42702402">Orazio Nicolotti</a> (<a href="http://www.wikidata.org/entity/Q42702402">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q42716142">Yu-Shi Tian</a> (<a href="http://www.wikidata.org/entity/Q42716142">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q42780467">Eddy Sotelo</a> (<a href="http://www.wikidata.org/entity/Q42780467">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q42783959">Jörg Kurt Wegner</a> (<a href="http://www.wikidata.org/entity/Q42783959">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q42824429">Patrik Rydberg</a> (<a href="http://www.wikidata.org/entity/Q42824429">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q42850572">Heinz Singer</a> (<a href="http://www.wikidata.org/entity/Q42850572">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q42850575">Juliane Hollender</a> (<a href="http://www.wikidata.org/entity/Q42850575">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q42869668">Gerrit Schüürmann</a> (<a href="http://www.wikidata.org/entity/Q42869668">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43086719">Fredrik Svensson</a> (<a href="http://www.wikidata.org/entity/Q43086719">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43185841">Andrew Leach</a> (<a href="http://www.wikidata.org/entity/Q43185841">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43194751">Thibault Charpentier</a> (<a href="http://www.wikidata.org/entity/Q43194751">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43275952">Xavier Lucas</a> (<a href="http://www.wikidata.org/entity/Q43275952">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43356360">Tomas Oberg</a> (<a href="http://www.wikidata.org/entity/Q43356360">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370241">Karol M Langner</a> (<a href="http://www.wikidata.org/entity/Q43370241">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370252">Pantelis Sopasakis</a> (<a href="http://www.wikidata.org/entity/Q43370252">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370275">Janos Hajagos</a> (<a href="http://www.wikidata.org/entity/Q43370275">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370305">Christoph Helma</a> (<a href="http://www.wikidata.org/entity/Q43370305">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370325">Carlos Fernandez-Lozano</a> (<a href="http://www.wikidata.org/entity/Q43370325">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370332">Sajjan S Mehta</a> (<a href="http://www.wikidata.org/entity/Q43370332">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370806">Eva Zurek</a> (<a href="http://www.wikidata.org/entity/Q43370806">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370807">Micha Rautenberg</a> (<a href="http://www.wikidata.org/entity/Q43370807">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370808">Olga Tcheremenskaia</a> (<a href="http://www.wikidata.org/entity/Q43370808">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370814">Thomas A Logothetis</a> (<a href="http://www.wikidata.org/entity/Q43370814">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370816">Peter Sefton</a> (<a href="http://www.wikidata.org/entity/Q43370816">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370818">Venkatesh Muthukrishnan</a> (<a href="http://www.wikidata.org/entity/Q43370818">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370819">Adriano Dekker</a> (<a href="http://www.wikidata.org/entity/Q43370819">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370821">Dávid Bajusz</a> (<a href="http://www.wikidata.org/entity/Q43370821">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370822">Aik Choon Tan</a> (<a href="http://www.wikidata.org/entity/Q43370822">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370823">Jinlong Ru</a> (<a href="http://www.wikidata.org/entity/Q43370823">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370826">Mark J Williamson</a> (<a href="http://www.wikidata.org/entity/Q43370826">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370830">Karel Berka</a> (<a href="http://www.wikidata.org/entity/Q43370830">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370844">Mohamad Mohebifar</a> (<a href="http://www.wikidata.org/entity/Q43370844">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370848">Maude Pupin</a> (<a href="http://www.wikidata.org/entity/Q43370848">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370849">Laurent Noé</a> (<a href="http://www.wikidata.org/entity/Q43370849">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370851">Guillermo Restrepo</a> (<a href="http://www.wikidata.org/entity/Q43370851">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370852">Floriane Montanari</a> (<a href="http://www.wikidata.org/entity/Q43370852">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370853">Gert-Jan Bekker</a> (<a href="http://www.wikidata.org/entity/Q43370853">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370854">Martin Gütlein</a> (<a href="http://www.wikidata.org/entity/Q43370854">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370857">Vishal B. Siramshetty</a> (<a href="http://www.wikidata.org/entity/Q43370857">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370858">Prachi Pradeep</a> (<a href="http://www.wikidata.org/entity/Q43370858">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370859">Sorin Avram</a> (<a href="http://www.wikidata.org/entity/Q43370859">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370860">Simona Funar-Timofei</a> (<a href="http://www.wikidata.org/entity/Q43370860">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370861">Sakari Lätti</a> (<a href="http://www.wikidata.org/entity/Q43370861">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370863">Alex A Freitas</a> (<a href="http://www.wikidata.org/entity/Q43370863">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370864">Alain-Dominique Gorse</a> (<a href="http://www.wikidata.org/entity/Q43370864">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370866">Sarah Preston</a> (<a href="http://www.wikidata.org/entity/Q43370866">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370870">Thommas M. Musyoka</a> (<a href="http://www.wikidata.org/entity/Q43370870">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370871">Paweł Siedlecki</a> (<a href="http://www.wikidata.org/entity/Q43370871">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370873">Axel J. Soto</a> (<a href="http://www.wikidata.org/entity/Q43370873">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370875">Ignacio Ponzoni</a> (<a href="http://www.wikidata.org/entity/Q43370875">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370877">Tailong Lei</a> (<a href="http://www.wikidata.org/entity/Q43370877">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370887">Fernando D. Prieto-Martínez</a> (<a href="http://www.wikidata.org/entity/Q43370887">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370889">Boris L Alperin</a> (<a href="http://www.wikidata.org/entity/Q43370889">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370891">Vladimír Horský</a> (<a href="http://www.wikidata.org/entity/Q43370891">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370894">Samuel Croset</a> (<a href="http://www.wikidata.org/entity/Q43370894">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370895">Lora Mak</a> (<a href="http://www.wikidata.org/entity/Q43370895">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370902">Manuel Pastor</a> (<a href="http://www.wikidata.org/entity/Q43370902">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370903">Radoslav Krivák</a> (<a href="http://www.wikidata.org/entity/Q43370903">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370908">Vincent F. Scalfani</a> (<a href="http://www.wikidata.org/entity/Q43370908">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370915">Marc C Nicklaus</a> (<a href="http://www.wikidata.org/entity/Q43370915">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370916">Mark Davies</a> (<a href="http://www.wikidata.org/entity/Q43370916">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370917">Louisa Bellis</a> (<a href="http://www.wikidata.org/entity/Q43370917">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370918">Robert Petryszak</a> (<a href="http://www.wikidata.org/entity/Q43370918">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370919">Sameer Velankar</a> (<a href="http://www.wikidata.org/entity/Q43370919">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370922">Matthew Smith</a> (<a href="http://www.wikidata.org/entity/Q43370922">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370923">Peter Matthews</a> (<a href="http://www.wikidata.org/entity/Q43370923">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370925">Fidele Ntie-Kang</a> (<a href="http://www.wikidata.org/entity/Q43370925">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370927">Karin Verspoor</a> (<a href="http://www.wikidata.org/entity/Q43370927">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370928">Sven Kochmann</a> (<a href="http://www.wikidata.org/entity/Q43370928">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370932">Jorge Estrada</a> (<a href="http://www.wikidata.org/entity/Q43370932">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370933">Pablo de Castro</a> (<a href="http://www.wikidata.org/entity/Q43370933">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370936">Paul Sherwood</a> (<a href="http://www.wikidata.org/entity/Q43370936">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370938">Alexander Kos</a> (<a href="http://www.wikidata.org/entity/Q43370938">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370939">Ying-Chi Lin</a> (<a href="http://www.wikidata.org/entity/Q43370939">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370942">Giovanni Nastasi</a> (<a href="http://www.wikidata.org/entity/Q43370942">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370944">Hugo López-Fernández</a> (<a href="http://www.wikidata.org/entity/Q43370944">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370945">Miguel Reboiro-Jato</a> (<a href="http://www.wikidata.org/entity/Q43370945">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370946">Daniel Glez-Peña</a> (<a href="http://www.wikidata.org/entity/Q43370946">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370950">Andrew M Walker</a> (<a href="http://www.wikidata.org/entity/Q43370950">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370951">Francesco Napolitano</a> (<a href="http://www.wikidata.org/entity/Q43370951">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370952">Vânia M Moreira</a> (<a href="http://www.wikidata.org/entity/Q43370952">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370953">Diogo Ars Latino</a> (<a href="http://www.wikidata.org/entity/Q43370953">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370956">Bharath Srinivasan</a> (<a href="http://www.wikidata.org/entity/Q43370956">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370958">Lewis Whitehead</a> (<a href="http://www.wikidata.org/entity/Q43370958">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370959">Isabel C. F. R. Ferreira</a> (<a href="http://www.wikidata.org/entity/Q43370959">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370960">Adrian M. Schreyer</a> (<a href="http://www.wikidata.org/entity/Q43370960">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43370999">Brian McMahon</a> (<a href="http://www.wikidata.org/entity/Q43370999">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43371003">Patrick N. Reardon</a> (<a href="http://www.wikidata.org/entity/Q43371003">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43371004">Brendan Howlin</a> (<a href="http://www.wikidata.org/entity/Q43371004">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43371012">Evangelos Kanoulas</a> (<a href="http://www.wikidata.org/entity/Q43371012">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43371014">Saw Simeon</a> (<a href="http://www.wikidata.org/entity/Q43371014">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43371015">Aleksandar Radovanovic</a> (<a href="http://www.wikidata.org/entity/Q43371015">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43371016">Mandeep Kaur</a> (<a href="http://www.wikidata.org/entity/Q43371016">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43371019">Effirul Ikhwan Ramlan</a> (<a href="http://www.wikidata.org/entity/Q43371019">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43371021">Andre O. Falcao</a> (<a href="http://www.wikidata.org/entity/Q43371021">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43371022">João P. Leal</a> (<a href="http://www.wikidata.org/entity/Q43371022">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43371027">Steve O'Hagan</a> (<a href="http://www.wikidata.org/entity/Q43371027">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43371029">Robbie P. Joosten</a> (<a href="http://www.wikidata.org/entity/Q43371029">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43371030">Santiago Garcia-Vallvé</a> (<a href="http://www.wikidata.org/entity/Q43371030">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43371031">Gerard Pujadas</a> (<a href="http://www.wikidata.org/entity/Q43371031">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43371032">Anna Arola-Arnal</a> (<a href="http://www.wikidata.org/entity/Q43371032">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43371033">Christopher J Harris</a> (<a href="http://www.wikidata.org/entity/Q43371033">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43371034">Brandon Bongers</a> (<a href="http://www.wikidata.org/entity/Q43371034">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q43371038">Francesc Solsona</a> (<a href="http://www.wikidata.org/entity/Q43371038">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q44566877">Salvatore La Rosa</a> (<a href="http://www.wikidata.org/entity/Q44566877">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q45296850">Marcel Bermudez</a> (<a href="http://www.wikidata.org/entity/Q45296850">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q45789717">Marc Zimmermann</a> (<a href="http://www.wikidata.org/entity/Q45789717">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q45789729">Mathilde Romberg</a> (<a href="http://www.wikidata.org/entity/Q45789729">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q46547005">Grace Patlewicz</a> (<a href="http://www.wikidata.org/entity/Q46547005">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q47012855">Duncan Hull</a> (<a href="http://www.wikidata.org/entity/Q47012855">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q47087369">Karl Edman</a> (<a href="http://www.wikidata.org/entity/Q47087369">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q47087753">David van der Spoel</a> (<a href="http://www.wikidata.org/entity/Q47087753">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q47098084">Andre Lamurias</a> (<a href="http://www.wikidata.org/entity/Q47098084">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q47160873">Nicole Tegtmeyer</a> (<a href="http://www.wikidata.org/entity/Q47160873">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q47166195">Eko A Rifai</a> (<a href="http://www.wikidata.org/entity/Q47166195">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q47166196">Marc van Dijk</a> (<a href="http://www.wikidata.org/entity/Q47166196">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q47245405">Aurélien Latouche</a> (<a href="http://www.wikidata.org/entity/Q47245405">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q47262336">Jean-Louis Reymond</a> (<a href="http://www.wikidata.org/entity/Q47262336">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q47455639">Jim Downing</a> (<a href="http://www.wikidata.org/entity/Q47455639">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q47455673">Dan W Zaharevitz</a> (<a href="http://www.wikidata.org/entity/Q47455673">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q47474707">Imran Shah</a> (<a href="http://www.wikidata.org/entity/Q47474707">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q47698166">Abid Qureshi</a> (<a href="http://www.wikidata.org/entity/Q47698166">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q47866690">Patarroyo ME</a> (<a href="http://www.wikidata.org/entity/Q47866690">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q48511379">Graham Ladds</a> (<a href="http://www.wikidata.org/entity/Q48511379">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q50029895">Chris de Graaf</a> (<a href="http://www.wikidata.org/entity/Q50029895">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q50281591">Tim Rocktäschel</a> (<a href="http://www.wikidata.org/entity/Q50281591">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q50731316">Andrea Volkamer</a> (<a href="http://www.wikidata.org/entity/Q50731316">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q50731613">Florbela Pereira</a> (<a href="http://www.wikidata.org/entity/Q50731613">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q50731867">Matteo Floris</a> (<a href="http://www.wikidata.org/entity/Q50731867">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q50731930">Thomas Engel</a> (<a href="http://www.wikidata.org/entity/Q50731930">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q51058144">Ulf Norinder</a> (<a href="http://www.wikidata.org/entity/Q51058144">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q51523897">Dmitry I. Osolodkin</a> (<a href="http://www.wikidata.org/entity/Q51523897">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q51751131">Nurul Malim</a> (<a href="http://www.wikidata.org/entity/Q51751131">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q51753160">Ralf Weiskirchen</a> (<a href="http://www.wikidata.org/entity/Q51753160">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q51878942">Gert Thijs</a> (<a href="http://www.wikidata.org/entity/Q51878942">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q52082270">Hitesh Patel</a> (<a href="http://www.wikidata.org/entity/Q52082270">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q52083659">Simone Fulle</a> (<a href="http://www.wikidata.org/entity/Q52083659">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q52115913">Andreas H Göller</a> (<a href="http://www.wikidata.org/entity/Q52115913">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q52116355">Natália Aniceto</a> (<a href="http://www.wikidata.org/entity/Q52116355">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q52125081">Lothar Terfloth</a> (<a href="http://www.wikidata.org/entity/Q52125081">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q5301676">Douglas Kell</a> (<a href="http://www.wikidata.org/entity/Q5301676">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q53345413">Antonio de la Vega de León</a> (<a href="http://www.wikidata.org/entity/Q53345413">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q54234793">Dharmendra K. Yadav</a> (<a href="http://www.wikidata.org/entity/Q54234793">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q54665519">Francesco Luigi Gervasio</a> (<a href="http://www.wikidata.org/entity/Q54665519">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q54859263">Samantha Kanza</a> (<a href="http://www.wikidata.org/entity/Q54859263">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q55095454">Gareth Owen</a> (<a href="http://www.wikidata.org/entity/Q55095454">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q55097518">Priyanka Banerjee</a> (<a href="http://www.wikidata.org/entity/Q55097518">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q55232632">David C. Reutens</a> (<a href="http://www.wikidata.org/entity/Q55232632">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q5550048">Gerard Kleywegt</a> (<a href="http://www.wikidata.org/entity/Q5550048">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q55704462">Hugo Froufe</a> (<a href="http://www.wikidata.org/entity/Q55704462">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q55714836">Agostino Marrazzo</a> (<a href="http://www.wikidata.org/entity/Q55714836">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q56084718">Prasun Dutta</a> (<a href="http://www.wikidata.org/entity/Q56084718">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q56396620">Andrey Yerin</a> (<a href="http://www.wikidata.org/entity/Q56396620">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q56422342">Akanksha Rajput</a> (<a href="http://www.wikidata.org/entity/Q56422342">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q56537163">Ernest Giralt</a> (<a href="http://www.wikidata.org/entity/Q56537163">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q56747874">Richard L Marchese Robinson</a> (<a href="http://www.wikidata.org/entity/Q56747874">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q56798427">Feijun Luo</a> (<a href="http://www.wikidata.org/entity/Q56798427">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q56800381">Gilles Marcou</a> (<a href="http://www.wikidata.org/entity/Q56800381">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q56812232">Vinita Periwal</a> (<a href="http://www.wikidata.org/entity/Q56812232">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q56958506">Yifan Peng</a> (<a href="http://www.wikidata.org/entity/Q56958506">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q56986123">Jian-Yu Shi</a> (<a href="http://www.wikidata.org/entity/Q56986123">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q57012103">Giuseppe Di Fatta</a> (<a href="http://www.wikidata.org/entity/Q57012103">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q57021746">Luca Pireddu</a> (<a href="http://www.wikidata.org/entity/Q57021746">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q57023371">Nicola Marzari</a> (<a href="http://www.wikidata.org/entity/Q57023371">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q57023970">Robert J Allaway</a> (<a href="http://www.wikidata.org/entity/Q57023970">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q57024063">Pascal Rigolet</a> (<a href="http://www.wikidata.org/entity/Q57024063">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q57027586">Mohamed Diwan M AbdulHameed</a> (<a href="http://www.wikidata.org/entity/Q57027586">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q57030289">Florian Mrugalla</a> (<a href="http://www.wikidata.org/entity/Q57030289">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q57056691">Neil Swainston</a> (<a href="http://www.wikidata.org/entity/Q57056691">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q57056698">Pablo Carbonell</a> (<a href="http://www.wikidata.org/entity/Q57056698">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q57151433">Nicolas Bosc</a> (<a href="http://www.wikidata.org/entity/Q57151433">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q57157739">Hai Pham-The</a> (<a href="http://www.wikidata.org/entity/Q57157739">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q57163014">Giuseppe Felice Mangiatordi</a> (<a href="http://www.wikidata.org/entity/Q57163014">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q57206547">Jorge Comas</a> (<a href="http://www.wikidata.org/entity/Q57206547">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q57218547">S Caboche</a> (<a href="http://www.wikidata.org/entity/Q57218547">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q57316555">Daisuke Kihara</a> (<a href="http://www.wikidata.org/entity/Q57316555">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q57394623">Julio C Facelli</a> (<a href="http://www.wikidata.org/entity/Q57394623">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q57415835">Ming Hao</a> (<a href="http://www.wikidata.org/entity/Q57415835">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q57415846">Tiejun Cheng</a> (<a href="http://www.wikidata.org/entity/Q57415846">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q57554928">Christian V Stevens</a> (<a href="http://www.wikidata.org/entity/Q57554928">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q57614093">Eric Quiniou</a> (<a href="http://www.wikidata.org/entity/Q57614093">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q57678540">Giovanni Pizzi</a> (<a href="http://www.wikidata.org/entity/Q57678540">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q57759407">Francisco Belchí Guillamón</a> (<a href="http://www.wikidata.org/entity/Q57759407">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q58059488">Antonino Fiannaca</a> (<a href="http://www.wikidata.org/entity/Q58059488">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q58059503">Alfonso Urso</a> (<a href="http://www.wikidata.org/entity/Q58059503">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q58059510">Riccardo Rizzo</a> (<a href="http://www.wikidata.org/entity/Q58059510">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q58085615">Mauricio Esguerra</a> (<a href="http://www.wikidata.org/entity/Q58085615">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q58226551">Rene Meier</a> (<a href="http://www.wikidata.org/entity/Q58226551">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q58336728">Wan Kyu Kim</a> (<a href="http://www.wikidata.org/entity/Q58336728">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q58423836">Walter Langel</a> (<a href="http://www.wikidata.org/entity/Q58423836">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q58797761">David Salgado</a> (<a href="http://www.wikidata.org/entity/Q58797761">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q58804579">Willem P van Hoorn</a> (<a href="http://www.wikidata.org/entity/Q58804579">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q58890745">Peter E Shaw</a> (<a href="http://www.wikidata.org/entity/Q58890745">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q59194760">Wail Ba Alawi</a> (<a href="http://www.wikidata.org/entity/Q59194760">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q59520206">Mathilde Koch</a> (<a href="http://www.wikidata.org/entity/Q59520206">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q59542599">Nicholas Gibbins</a> (<a href="http://www.wikidata.org/entity/Q59542599">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q59555104">Maria João R.P. Queiroz</a> (<a href="http://www.wikidata.org/entity/Q59555104">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q59668391">Dominique Sydow</a> (<a href="http://www.wikidata.org/entity/Q59668391">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q59689151">Dawid Warszycki</a> (<a href="http://www.wikidata.org/entity/Q59689151">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q60430294">Valérie Leclère</a> (<a href="http://www.wikidata.org/entity/Q60430294">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q60465926">Haruki Nakamura</a> (<a href="http://www.wikidata.org/entity/Q60465926">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q60651741">Francis Atkinson</a> (<a href="http://www.wikidata.org/entity/Q60651741">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q60668160">Despoina Magka</a> (<a href="http://www.wikidata.org/entity/Q60668160">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q61046796">Dieter Jahn</a> (<a href="http://www.wikidata.org/entity/Q61046796">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q61055226">Antanas Vaitkus</a> (<a href="http://www.wikidata.org/entity/Q61055226">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q61108142">Zihu Guo</a> (<a href="http://www.wikidata.org/entity/Q61108142">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q61121954">Ivana Blaženović</a> (<a href="http://www.wikidata.org/entity/Q61121954">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q61142053">Neeraj Kumar Rajput</a> (<a href="http://www.wikidata.org/entity/Q61142053">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q61456437">Lindsey Burggraaff</a> (<a href="http://www.wikidata.org/entity/Q61456437">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q6153626">Janet Thornton</a> (<a href="http://www.wikidata.org/entity/Q6153626">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q61896693">Holger Merlitz</a> (<a href="http://www.wikidata.org/entity/Q61896693">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q62130109">O Anatole von Lilienfeld</a> (<a href="http://www.wikidata.org/entity/Q62130109">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q62676031">Pavel Banáš</a> (<a href="http://www.wikidata.org/entity/Q62676031">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q62676269">Thomas E Cheatham</a> (<a href="http://www.wikidata.org/entity/Q62676269">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q63351119">Yannick Djoumbou Feunang</a> (<a href="http://www.wikidata.org/entity/Q63351119">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q64005393">Martin Dračínský</a> (<a href="http://www.wikidata.org/entity/Q64005393">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q64167432">Wilmer Leal</a> (<a href="http://www.wikidata.org/entity/Q64167432">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q64358327">Franziska Hufsky</a> (<a href="http://www.wikidata.org/entity/Q64358327">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q64517973">Rui Abreu</a> (<a href="http://www.wikidata.org/entity/Q64517973">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q64861765">John Blayney Owen Mitchell</a> (<a href="http://www.wikidata.org/entity/Q64861765">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q64865729">S. Joshua Swamidass</a> (<a href="http://www.wikidata.org/entity/Q64865729">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q65088041">Kathrin Heikamp</a> (<a href="http://www.wikidata.org/entity/Q65088041">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q65088044">Dilyana Dimova</a> (<a href="http://www.wikidata.org/entity/Q65088044">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q65963317">Piotr Zielenkiewicz</a> (<a href="http://www.wikidata.org/entity/Q65963317">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q67166600">Veronika Navrátilová</a> (<a href="http://www.wikidata.org/entity/Q67166600">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q67222611">Thomas Sander</a> (<a href="http://www.wikidata.org/entity/Q67222611">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q67222613">Christian Rufener</a> (<a href="http://www.wikidata.org/entity/Q67222613">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q67222616">Michaël Zasso</a> (<a href="http://www.wikidata.org/entity/Q67222616">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q70965993">Anna Palczewska</a> (<a href="http://www.wikidata.org/entity/Q70965993">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q71033158">Martin Vogt</a> (<a href="http://www.wikidata.org/entity/Q71033158">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q71033415">Britta Nisius</a> (<a href="http://www.wikidata.org/entity/Q71033415">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q75658782">Yehoshua Perl</a> (<a href="http://www.wikidata.org/entity/Q75658782">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q79294479">Tatsuya Akutsu</a> (<a href="http://www.wikidata.org/entity/Q79294479">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q7932748">Vinod Scaria</a> (<a href="http://www.wikidata.org/entity/Q7932748">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q79449903">Rui Alves</a> (<a href="http://www.wikidata.org/entity/Q79449903">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q81507918">Laurent Noé</a> (<a href="http://www.wikidata.org/entity/Q81507918">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q82265650">Viktor Vegh</a> (<a href="http://www.wikidata.org/entity/Q82265650">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q82422361">William W L Wong</a> (<a href="http://www.wikidata.org/entity/Q82422361">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q82621427">Xue Xu</a> (<a href="http://www.wikidata.org/entity/Q82621427">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q82814507">Sarah R Langdon</a> (<a href="http://www.wikidata.org/entity/Q82814507">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q83536319">Hong Kang</a> (<a href="http://www.wikidata.org/entity/Q83536319">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q83826889">Jean-Paul Ebejer</a> (<a href="http://www.wikidata.org/entity/Q83826889">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q84253690">Pablo Conesa</a> (<a href="http://www.wikidata.org/entity/Q84253690">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q84287067">Mona Elbadawi-Sidhu</a> (<a href="http://www.wikidata.org/entity/Q84287067">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q85465277">Robert E Belford</a> (<a href="http://www.wikidata.org/entity/Q85465277">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q85620665">Melanie C Burger</a> (<a href="http://www.wikidata.org/entity/Q85620665">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q85712618">María J Martínez</a> (<a href="http://www.wikidata.org/entity/Q85712618">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q85712622">Mónica F Díaz</a> (<a href="http://www.wikidata.org/entity/Q85712622">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q85712626">Gustavo E Vazquez</a> (<a href="http://www.wikidata.org/entity/Q85712626">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q86029892">Rareş-Petru Moldovan</a> (<a href="http://www.wikidata.org/entity/Q86029892">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q86576635">Chad Hg Allen</a> (<a href="http://www.wikidata.org/entity/Q86576635">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q86993402">Yoann Dufresne</a> (<a href="http://www.wikidata.org/entity/Q86993402">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q86996205">Yung-Chun Chang</a> (<a href="http://www.wikidata.org/entity/Q86996205">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q87674118">Lina Humbeck</a> (<a href="http://www.wikidata.org/entity/Q87674118">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q87725529">Jie Dong</a> (<a href="http://www.wikidata.org/entity/Q87725529">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q87916829">Laeeq Ahmed</a> (<a href="http://www.wikidata.org/entity/Q87916829">edit</a>)</td>
  </tr>
  <tr>
    <td>1</td>
    <td><a href="https://tools.wmflabs.org/scholia/Q88086137">Tobias Brinkjost</a> (<a href="http://www.wikidata.org/entity/Q88086137">edit</a>)</td>
  </tr>
</table>
## Code examples
### curl
```shell
curl -o prolificAuthorsAll.rq https://raw.githubusercontent.com/jcheminform/useful-queries/master/sparql/prolificAuthorsAll.rq
curl -H "Accept: text/tab-separated-values" -G https://query.wikidata.org/bigdata/namespace/wdq/sparql --data-urlencode query@prolificAuthorsAll.rq
```
This SPARQL query is available under CCZero.
