---
description: Een herhaling betreffende de syntaxis en de regels van het construeren van regelmatige uitdrukkingen.
seo-description: Een herhaling betreffende de syntaxis en de regels van het construeren van regelmatige uitdrukkingen.
seo-title: Regelmatige expressies
solution: Target
title: Regelmatige expressies
topic: Appendices,Site search and merchandising
uuid: 369b54f6-372a-41de-bb5d-3ae0bd640199
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# Regelmatige expressies{#regular-expressions}

Een herhaling betreffende de syntaxis en de regels van het construeren van regelmatige uitdrukkingen.

Zie ook het [Vormen van een stijgende index van een gefaseerde website](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Syntaxis van reguliere expressies**

<table> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <b>Tekst</b> </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p>Elk teken </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> [klusjes] </p> </td> 
   <td colname="col3"> <p> Tekenklasse: Een van de krijtjes </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> [^chars] </p> </td> 
   <td colname="col3"> <p>Tekenklasse: Geen tekens </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> text1|text2 </p> </td> 
   <td colname="col3"> <p> Alternatief: text1 of text2 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Kwantitatieve bepalingen</b> </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> ? </p> </td> 
   <td colname="col3"> <p> 0 of 1 van de vorige tekst </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> * </p> </td> 
   <td colname="col3"> <p> 0 of N van de vorige tekst (N &gt; 1) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> + </p> </td> 
   <td colname="col3"> <p>1 of N van de vorige tekst (N &gt; 1) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Groepering</b> </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> (tekst) </p> </td> 
   <td colname="col3"> <p> Groepering van tekst, of om de grenzen van een alternatief te plaatsen of achterverwijzingen te maken waar de Negende groep op RHS van een RewriteRule met $N wordt gebruikt) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Ankers</b> </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> ^ </p> </td> 
   <td colname="col3"> <p> Begin van lijnanker. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> $ </p> </td> 
   <td colname="col3"> <p> Einde van lijnanker. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Escaperen</b> </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </p> </td> 
   <td colname="col2"> <p>\char </p> </td> 
   <td colname="col3"> <p>Vlucht de specifieke klusje. Bijvoorbeeld, om de klusjes " te specificeren.[]()" enzovoort. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Regels voor reguliere expressies**

* Een gewoon karakter-niet één van de speciale hieronder beschreven karakters is een één-karakter regelmatige uitdrukking die zich aanpast.
* Een backslash (\) die door om het even welk speciaal karakter wordt gevolgd is een één-karakter regelmatige uitdrukking die het speciale karakter zelf aanpast. De speciale karakters omvatten het volgende:

   * `.` (punt), `*` (asterisk), `?` (vraagteken), `+` (plus teken), `[` (linkervierkante haakje), `|` (verticale pijp), en `\` (backslash) zijn altijd speciale karakters, behalve wanneer zij binnen vierkante haakjes verschijnen.
   * `^` (inlasteken of omtrek) is speciaal aan het begin van een regelmatige uitdrukking, of wanneer het onmiddellijk links van een paar vierkante haakjes volgt.
   * `$` (dollarteken) is speciaal aan het eind van een regelmatige uitdrukking.
   * `.` (periode) is een regelmatige uitdrukking van één karakter die om het even welk karakter aanpast, met inbegrip van extra codeset karakters met uitzondering van nieuw-lijn.
   * Een niet-lege tekenreeks die in `[ ]` (links en rechts) vierkante haakjes is ingesloten, is een reguliere expressie van één teken die overeenkomt met één teken, inclusief aanvullende tekens van de codereeks, in die tekenreeks.

      Als, echter, het eerste karakter van het koord een `^` (omtrek) is, past de één-karakter regelmatige uitdrukking om het even welk karakter, met inbegrip van de extra codeset karakters, met uitzondering van nieuw-lijn en de resterende karakters in het koord aan.

      De `^` heeft deze speciale betekenis slechts als het eerst in het koord voorkomt. U kunt `-` (minus teken) gebruiken om op een waaier van opeenvolgende karakters, met inbegrip van extra codeset karakters te wijzen. Bijvoorbeeld, is [0-9] gelijkwaardig aan [0123456789].

      De karakters die de waaier specificeren moeten van de zelfde codeset zijn. Wanneer de karakters van verschillende codereeksen zijn, wordt één van de karakters die de waaier specificeren aangepast. Het `-` verliest deze speciale betekenis als het eerst (na een aanvankelijke `^`, als om het even welk) of laatste in het koord voorkomt. De `]` (juiste vierkante steun) beëindigt zulk een koord niet wanneer het het eerste karakter binnen het is, na een aanvankelijke `^`, als om het even welk is. Bijvoorbeeld, past []a-f] of een `]` (juiste vierkante steun) of één van de letters van ASCII a tot en met f aan. De vier karakters die als speciale karakters hierboven worden vermeld staan voor zich binnen zulk een koord van karakters.

**Regels voor het construeren van reguliere expressies uit één teken**

U kunt de volgende regels gebruiken om regelmatige uitdrukkingen van één-karakter regelmatige uitdrukkingen te construeren:

* Een één-karakter regelmatige uitdrukking is een regelmatige uitdrukking die aanpast wat de één-karakter regelmatige uitdrukkingsgelijken aanpast.
* Een één-karakter regelmatige uitdrukking die door een `*` (asterisk) wordt gevolgd is een regelmatige uitdrukking die nul of meer voorkomen van de één-karakter regelmatige uitdrukking aanpast, die een aanvullend karakter van de codeset kan zijn. Als er om het even welke keus is, wordt het langste uiterst linkse koord dat een gelijke toelaat gekozen.
* Een één-karakter regelmatige uitdrukking die door een `?` (vraagteken) wordt gevolgd is een regelmatige uitdrukking die nul of één voorkomen van de één-karakter regelmatige uitdrukking aanpast, die een aanvullend karakter van de codeset kan zijn. Als er om het even welke keus is, wordt het langste uiterst linkse koord dat een gelijke toelaat gekozen.
* Een één-karakter regelmatige uitdrukking die door een `+` (plus teken) wordt gevolgd is een regelmatige uitdrukking die één of meerdere voorkomen van de één-karakter regelmatige uitdrukking aanpast, die een aanvullend karakter van de codeset kan zijn. Als er om het even welke keus is, wordt het langste uiterst linkse koord dat een gelijke toelaat gekozen.
* Een één-karakter regelmatige uitdrukking die door wordt gevolgd, `{m}`of `{m,}``{m,n}` is een regelmatige uitdrukking die een waaier van voorkomen van de één-karakter regelmatige uitdrukking aanpast. De waarden van m en n moeten niet-negatieve gehele getallen van minder dan 256 zijn; precies overeenkomt met m voorkomen; `{m}` `{m,}` overeenkomende met ten minste m voorkomen; `{m,n}` komt overeen met een willekeurig aantal voorvallen tussen m en n inclusief. Wanneer een keus bestaat, past de regelmatige uitdrukkingsgelijken zoveel mogelijk voorkomen aan.
* De aaneenschakeling van regelmatige uitdrukkingen is een regelmatige uitdrukking die de aaneenschakeling van de koorden aanpast die door elke component van de regelmatige uitdrukking worden aangepast.
* Een regelmatige uitdrukking die tussen de karakteropeenvolgingen ( en) wordt ingesloten is een regelmatige uitdrukking die aanpast wat de niet aangepaste regelmatige uitdrukkingsgelijken aanpast.
* Een regelmatige uitdrukking die door een `|` (verticale pijp) wordt gevolgd door een regelmatige uitdrukking is een regelmatige uitdrukking die of de eerste regelmatige uitdrukking (vóór de verticale pijp) of de tweede regelmatige uitdrukking (na de verticale pijp) aanpast.

U kunt een regelmatige uitdrukking ook beperken om slechts een eerste segment of definitief segment van een lijn, of allebei aan te passen.

* Een `^` (omtrek) aan het begin van een regelmatige uitdrukking beperkt die regelmatige uitdrukking om een eerste segment van een lijn aan te passen.
* Een `$` (dollarteken) aan het eind van een volledige regelmatige uitdrukking beperkt die regelmatige uitdrukking om een definitief segment van een lijn aan te passen.
* De bouw ^regular expression$ beperkt de regelmatige uitdrukking om de volledige lijn aan te passen.

Er zijn sommige vooraf bepaalde namen van de karakterklasse die u in plaats van complexe steun kunt gebruiken regelmatige uitdrukkingen. Bijvoorbeeld, kan een cijfer door de één-karakter regelmatige uitdrukking [0-9] of door de karakterklasse worden vertegenwoordigd één-karakter regelmatige uitdrukking [[:cijfer:]].

De vooraf bepaalde karakterklassen en hun betekenissen zijn de volgende:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Tekenklasse </p> </th> 
   <th colname="col2" class="entry"> <p>Betekenis </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> [[:alnum:]] </p> </td> 
   <td colname="col2"> <p> Een alfabetisch karakter of een cijfer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:alfa:]] </p> </td> 
   <td colname="col2"> <p>Een alfabetisch karakter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:blanco:]] </p> </td> 
   <td colname="col2"> <p>Een ruimte of een lusje. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:cntrl:]] </p> </td> 
   <td colname="col2"> <p> een controlecode; niet-afdrukbaar karakter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:cijfer:]] </p> </td> 
   <td colname="col2"> <p>Een cijfer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:grafiek:]] </p> </td> 
   <td colname="col2"> <p> Om het even welk drukkarakter behalve ruimte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:lager:]] </p> </td> 
   <td colname="col2"> <p>Een alfabetisch kleine letter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:afdrukken:]] </p> </td> 
   <td colname="col2"> <p> Om het even welk drukkarakter met inbegrip van ruimte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:punct:]] </p> </td> 
   <td colname="col2"> <p> Punctuatie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:ruimte:]] </p> </td> 
   <td colname="col2"> <p> De witte ruimte zoals een ruimte, een lusje, of een eind-van-lijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:bovenaan:]] </p> </td> 
   <td colname="col2"> <p> Een alfabetisch bovenliggend karakter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:xdigit:]] </p> </td> 
   <td colname="col2"> <p> Een hexadecimaal cijfer, boven of onder-geval. </p> </td> 
  </tr> 
 </tbody> 
</table>

Twee speciale namen van de karakterklasse passen de ongeldige ruimte bij het begin en het eind van een woord aan. Met andere woorden, zij passen geen werkelijk karakter aan. Een woord wordt beschouwd als om het even welke opeenvolging van alfabetische karakters, cijfers, of onderstreept (_).

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Tekenklasse </p> </th> 
   <th colname="col2" class="entry"> <p>Betekenis </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> [[:&lt;:]] </p> </td> 
   <td colname="col2"> <p> begin van een woord </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:&gt;:]] </p> </td> 
   <td colname="col2"> <p>einde van een woord </p> </td> 
  </tr> 
 </tbody> 
</table>

