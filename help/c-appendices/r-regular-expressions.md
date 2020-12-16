---
description: Een vernieuwingsfunctie voor de syntaxis en regels voor het maken van reguliere expressies.
seo-description: Een vernieuwingsfunctie voor de syntaxis en regels voor het maken van reguliere expressies.
seo-title: Reguliere expressies
solution: Target
title: Reguliere expressies
topic: Appendices,Site search and merchandising
uuid: 369b54f6-372a-41de-bb5d-3ae0bd640199
translation-type: tm+mt
source-git-commit: 7b883870bb16284d8070a21547cdb62cc79d7632
workflow-type: tm+mt
source-wordcount: '1058'
ht-degree: 0%

---


# Gewone uitdrukkingen{#regular-expressions}

Een vernieuwingsfunctie voor de syntaxis en regels voor het maken van reguliere expressies.

Zie ook [Een incrementele index van een gefaseerde website configureren](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Syntaxis van reguliere expressies**

<table> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <b>Tekst</b> </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p>Willekeurig teken </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> [tekens] </p> </td> 
   <td colname="col3"> <p> Tekenklasse: Een teken </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> [^tekens] </p> </td> 
   <td colname="col3"> <p>Tekenklasse: Geen tekens </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> text1|text2 </p> </td> 
   <td colname="col3"> <p> Alternatief: text1 of text2 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Kwantoren</b> </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> ? </p> </td> 
   <td colname="col3"> <p> 0 of 1 van de voorgaande tekst </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> * </p> </td> 
   <td colname="col3"> <p> 0 of N van de voorafgaande tekst (N &gt; 1) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> + </p> </td> 
   <td colname="col3"> <p>1 of N van de voorgaande tekst (N &gt; 1) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Groepering</b> </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> (tekst) </p> </td> 
   <td colname="col3"> <p> Groepering van tekst, of om de grenzen van een alternatief te plaatsen of achterverwijzingen te maken waar de Nth groep op RHS van RewriteRule met $N wordt gebruikt) </p> </td> 
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
   <td colname="col1"> <p> <b>Escaping</b> </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </p> </td> 
   <td colname="col2"> <p>\char </p> </td> 
   <td colname="col3"> <p>Escape het specifieke teken. Als u bijvoorbeeld de tekens "" wilt opgeven.[]()" enzovoort. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Regels voor reguliere expressies**

* Een gewoon teken, niet een van de speciale tekens die hieronder worden beschreven, is een reguliere expressie van één teken die met zichzelf overeenkomt.
* Een backslash (\) gevolgd door een speciaal teken is een reguliere expressie van één teken die overeenkomt met het speciale teken zelf. Speciale tekens zijn onder andere:

   * `.` (punt),  `*` (asterisk),  `?` (vraagteken),  `+` (plusteken),  `[` (vierkant haakje openen),  `|` (verticale pipe) en  `\` (backslash) zijn altijd speciale tekens, behalve wanneer deze tussen vierkante haakjes staan.
   * `^` (invoegpunt of omtrek) is speciaal aan het begin van een reguliere expressie of wanneer deze direct links van een paar vierkante haakjes staat.
   * `$` (dollarteken) is speciaal aan het einde van een reguliere expressie.
   * `.` (punt) is een reguliere expressie van één teken die overeenkomt met elk willekeurig teken, inclusief aanvullende tekens in codesets, met uitzondering van een nieuwe regel.
   * Een niet-lege tekenreeks met tekens tussen `[ ]` (vierkante haakjes links en rechts) is een reguliere expressie van één teken die overeenkomt met één teken in die tekenreeks, inclusief aanvullende codesettekens.

      Als het eerste teken van de tekenreeks echter een `^` (omtrek) is, komt de reguliere expressie van één teken overeen met elk willekeurig teken, inclusief aanvullende tekens voor codesets, met uitzondering van de nieuwe regel en de overige tekens in de tekenreeks.

      De `^` heeft deze speciale betekenis slechts als het eerst in het koord voorkomt. U kunt `-` (minteken) gebruiken om een reeks opeenvolgende tekens aan te geven, inclusief aanvullende tekens in de codeset. [0-9] is bijvoorbeeld gelijk aan [0123456789].

      Tekens die het bereik aangeven, moeten afkomstig zijn uit dezelfde codeset. Wanneer de tekens uit verschillende codesets afkomstig zijn, komt een van de tekens die het bereik aangeven, overeen. De `-` verliest deze speciale betekenis als deze eerst voorkomt (na een eventuele eerste `^`) of als deze zich als laatste in de tekenreeks bevindt. De `]` (vierkant haakje rechts) beëindigt een dergelijke tekenreeks niet wanneer het het eerste teken binnen de tekenreeks is, na een eventuele eerste `^`. `[]a-f]` komt bijvoorbeeld overeen met een `]` (vierkant haakje sluiten) of een van de ASCII-letters a t/m f. De vier tekens die hierboven als speciale tekens worden vermeld, staan voor zichzelf in een dergelijke tekenreeks.

**Regels voor het samenstellen van reguliere expressies op basis van reguliere expressies van één teken**

Met de volgende regels kunt u reguliere expressies maken op basis van reguliere expressies van één teken:

* Een reguliere expressie van één teken is een reguliere expressie die overeenkomt met de reguliere expressie van één teken.
* Een reguliere expressie van één teken, gevolgd door een `*` (sterretje), is een reguliere expressie die overeenkomt met nul of meer exemplaren van de reguliere expressie van één teken. Dit kan een aanvullend teken in de codeset zijn. Als er een keuze is, wordt de langste meest linkse tekenreeks gekozen die een overeenkomst toestaat.
* Een reguliere expressie van één teken, gevolgd door een `?` (vraagteken), is een reguliere expressie die overeenkomt met nul of één keer dat de reguliere expressie van één teken voorkomt. Dit kan een aanvullend teken in de codeset zijn. Als er een keuze is, wordt de langste meest linkse tekenreeks gekozen die een overeenkomst toestaat.
* Een reguliere expressie van één teken, gevolgd door een `+` (plusteken), is een reguliere expressie die overeenkomt met een of meer instanties van de reguliere expressie van één teken. Dit kan een aanvullend teken in de codeset zijn. Als er een keuze is, wordt de langste meest linkse tekenreeks gekozen die een overeenkomst toestaat.
* Een reguliere expressie van één teken, gevolgd door `{m}`, `{m,}` of `{m,n}`, is een reguliere expressie die overeenkomt met een bereik van de reguliere expressie van één teken. De waarden van m en n moeten niet-negatieve gehele getallen van minder dan 256 zijn; `{m}` komt exact overeen met m voorkomen; `{m,}` komt overeen met ten minste m voorkomen; `{m,n}` komt overeen met een willekeurig aantal voorvallen tussen m en n. Wanneer een keuze bestaat, komt de reguliere expressie overeen met zoveel mogelijk keren.
* De samenvoeging van reguliere expressies is een reguliere expressie die overeenkomt met de samenvoeging van de tekenreeksen die door elke component van de reguliere expressie worden aangepast.
* Een reguliere expressie die wordt ingesloten tussen de tekenreeksen ( en ), is een reguliere expressie die overeenkomt met de niet-geordende reguliere expressie.
* Een reguliere expressie gevolgd door een `|` (verticale pipe) gevolgd door een reguliere expressie is een reguliere expressie die ofwel overeenkomt met de eerste reguliere expressie (vóór de verticale pipe) ofwel met de tweede reguliere expressie (na de verticale pipe).

U kunt een reguliere expressie ook beperken tot alleen een eerste of laatste segment van een regel, of beide.

* Een `^` (omtrek) aan het begin van een reguliere expressie beperkt die reguliere expressie tot een eerste segment van een regel.
* Een `$` (dollarteken) aan het eind van een volledige regelmatige uitdrukking beperkt die regelmatige uitdrukking om een definitief segment van een lijn aan te passen.
* De constructie ^reguliere expressie$ beperkt de reguliere expressie tot overeenstemming met de gehele regel.

Er zijn enkele vooraf gedefinieerde tekenklassennamen die u kunt gebruiken in plaats van complexe, tussen haakjes geplaatste reguliere expressies. Een cijfer kan bijvoorbeeld worden vertegenwoordigd door de reguliere expressie [0-9] van één teken of door de reguliere expressie [[:digit:]] van de tekenklasse.

De vooraf gedefinieerde tekenklassen en hun betekenis zijn:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Character, klasse </p> </th> 
   <th colname="col2" class="entry"> <p>Betekenis </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> [[:alnum:]] </p> </td> 
   <td colname="col2"> <p> Een alfabetisch teken of een cijfer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:alpha:]] </p> </td> 
   <td colname="col2"> <p>Een alfabetisch teken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:blank:]] </p> </td> 
   <td colname="col2"> <p>Een spatie of tab. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:cntrl:]] </p> </td> 
   <td colname="col2"> <p> een controlecode; niet-afdrukbaar teken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:digit:]] </p> </td> 
   <td colname="col2"> <p>Een cijfer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:grafiek:]] </p> </td> 
   <td colname="col2"> <p> Elk afdrukteken behalve spatie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:onderste:]] </p> </td> 
   <td colname="col2"> <p>Een alfabetisch teken in kleine letters. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:afdrukken:]] </p> </td> 
   <td colname="col2"> <p> Elk afdrukteken inclusief spatie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:punct:]] </p> </td> 
   <td colname="col2"> <p> Leestekens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:space:]] </p> </td> 
   <td colname="col2"> <p> Witruimte zoals een spatie, een tab of een regeleinde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:bovenste:]] </p> </td> 
   <td colname="col2"> <p> Een alfabetisch teken in hoofdletters. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:xdigit:]] </p> </td> 
   <td colname="col2"> <p> Een hexadecimaal cijfer, hoofdletter of kleine letter. </p> </td> 
  </tr> 
 </tbody> 
</table>

Twee speciale tekenklassenamen komen overeen met de lege ruimte aan het begin en het einde van een woord. Met andere woorden, ze komen niet overeen met een feitelijk teken. Een woord wordt beschouwd als een reeks alfabetische tekens, cijfers of onderstrepingstekens (_).

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Character, klasse </p> </th> 
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

