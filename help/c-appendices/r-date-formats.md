---
description: U kunt de datumformaten bepalen die worden gebruikt wanneer het om het even welk gebied met een type van "datum"gegevens ontleedt en indexeert.
seo-description: U kunt de datumformaten bepalen die worden gebruikt wanneer het om het even welk gebied met een type van "datum"gegevens ontleedt en indexeert.
seo-title: Datumformaten
solution: Target
title: Datumformaten
topic: Appendices,Site search and merchandising
uuid: 148914b5-33ef-41db-8404-67c03f6f0832
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# Datumformaten{#date-formats}

U kunt de datumformaten bepalen die worden gebruikt wanneer het om het even welk gebied met een type van &quot;datum&quot;gegevens ontleedt en indexeert.

Het formaat van de datum en de tijd wordt gespecificeerd met een formaatkoord. Het formaatkoord bestaat uit nul of meer omzettingsspecificaties (een omzettingsspecificatie bestaat uit een percententeken en één ander karakter) en gewone karakters. Een standaardlijst wordt verstrekt van de koorden van het datumformaat voor elk datumgebied.

U hebt volledige controle over deze lijst en kunt aan toevoegen of het wijzigen om de behoeften van uw plaats aan te passen. Het hoogste formaatkoord neemt belangrijkheid en de verdere formaatkoorden worden slechts gebruikt als het ontleden van de inhoud van een bepaalde meta-gegevensmarkering een fout oplevert.

Bijvoorbeeld, veronderstel u de volgende datumformaten hebt gespecificeerd:

<table> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>%B %d, %Y %T %Z </p> <p>%b %d, %Y %T %Z </p> <p>%A %B %d, %Y %T %Z </p> <p>%A %b %d, %Y %T %Z </p> <p>%a %B %d, %Y %T %Z </p> <p>%a %b %d, %Y %T %Z </p> <p>%d %b %Y %T %Z </p> </td> 
  </tr> 
 </tbody> 
</table>

De eerste indeling, &quot;%B %d, %Y %T %Z&quot;, komt overeen met datums als de volgende &quot;20 september 2014 13:12:00 PDT&quot;. Als de inhoud van de meta-gegevensmarkering niet met dit formaatkoord kan worden ontleed, wordt het volgende beschikbare formaat &quot;%b %d, %Y %T %Z&quot;geprobeerd. Dit formaat past data als het volgende aan: &quot;20 sep. 2014 3:12:00 PDT&quot;. Als de inhoud van de meta-gegevensmarkering niet met dit formaatkoord kan worden ontleed, beweegt het plaatsonderzoek/het merchandising zich onderaan de lijst van formaatkoorden tot het een formaatkoord vindt dat werkt.

De volgende lijst beschrijft de beschikbare koorden van het datumformaat:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Gegevensformaat </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>%A </p> </td> 
   <td colname="col2"> <p>Past de nationale vertegenwoordiging van de volledige weekdagnaam aan, bijvoorbeeld, "Maandag." De nationale vertegenwoordiging wordt bepaald aan de hand van de "Taal"-instelling op de optie "Woorden en talen" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%a </p> </td> 
   <td colname="col2"> <p> overeenkomt met de nationale afbeelding van de afgekorte weekdagnaam, waarbij de afkorting de eerste drie tekens is, bijvoorbeeld "Mon." De nationale vertegenwoordiging wordt bepaald aan de hand van de "Taal"-instelling op de optie "Woorden en talen" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%B </p> </td> 
   <td colname="col2"> <p> overeenkomt met de nationale vertegenwoordiging van de volledige naam van de maand, bijvoorbeeld "Juni." De nationale vertegenwoordiging wordt bepaald aan de hand van de "Taal"-instelling op de optie "Woorden en talen" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%b </p> </td> 
   <td colname="col2"> <p> overeenkomt met de nationale afbeelding van de afgekorte naam van de maand, waarbij de afkorting de eerste drie tekens is, bijvoorbeeld "Jun." De nationale vertegenwoordiging wordt bepaald aan de hand van de "Taal"-instelling op de optie "Woorden en talen" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%D </p> </td> 
   <td colname="col2"> <p> komt overeen met "%m/%d/%y", bv. 06-06-01" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%d </p> </td> 
   <td colname="col2"> <p> komt de dag van de maand als decimaal aantal (01-31) overeen </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%e </p> </td> 
   <td colname="col2"> <p> komt overeen met de dag van de maand als decimaal getal (1-31); enkele cijfers worden voorafgegaan door een lege </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%H </p> </td> 
   <td colname="col2"> <p> past het uur (24 uurklok) als decimaal aantal (00-23) aan </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%h </p> </td> 
   <td colname="col2"> <p> overeenkomt met de nationale afbeelding van de afgekorte naam van de maand, waarbij de afkorting de eerste drie tekens is, bijvoorbeeld "Jun" (hetzelfde als %b) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%I </p> </td> 
   <td colname="col2"> <p> past het uur (de klok van 12 uur) als decimaal aantal (01-12) aan </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%j </p> </td> 
   <td colname="col2"> <p> komt overeen met de dag van het jaar als decimaal getal (001-366) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%k </p> </td> 
   <td colname="col2"> <p> past het uur (klok van 24 uur) als decimaal aantal (0-23) aan; enkele cijfers worden voorafgegaan door een lege </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%l </p> </td> 
   <td colname="col2"> <p> past het uur (12 uurklok) als decimaal aantal (1-12) aan; enkele cijfers worden voorafgegaan door een lege </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%M </p> </td> 
   <td colname="col2"> <p> past de minuut als decimaal aantal (00-59) aan </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%m </p> </td> 
   <td colname="col2"> <p> past de maand als decimaal aantal (01-12) aan </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%p </p> </td> 
   <td colname="col2"> <p> overeenkomt met de nationale vertegenwoordiging van "ante meridiem" of "post meridiem", naargelang van het geval, bv. "PM." De nationale vertegenwoordiging wordt bepaald aan de hand van de "Taal"-instelling op de optie "Woorden en talen" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%R </p> </td> 
   <td colname="col2"> <p> komt overeen met "%H:%M", bv. "13:23" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%r </p> </td> 
   <td colname="col2"> <p> is equivalent aan "%I:%M:%S %p", bv. "13:23:45" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%S </p> </td> 
   <td colname="col2"> <p> past de tweede als decimaal aantal (00-60) aan </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%T </p> </td> 
   <td colname="col2"> <p> is equivalent aan "%H:%M:%S", bv. "13:26:47" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%U </p> </td> 
   <td colname="col2"> <p> komt overeen met het weekaantal van het jaar (zondag als eerste dag van de week) als decimaal getal (00-53) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%v </p> </td> 
   <td colname="col2"> <p> komt overeen met "%e-%b-%Y", bv. "6-jun-2001" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%Y </p> </td> 
   <td colname="col2"> <p> komt overeen met het jaar met een decimaal getal, bijvoorbeeld "2001" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%y </p> </td> 
   <td colname="col2"> <p> komt overeen met het jaar zonder eeuw als decimaal getal (00-99) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%Z </p> </td> 
   <td colname="col2"> <p> past de naam van de tijdzone aan </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%% </p> </td> 
   <td colname="col2"> <p> matches "%" </p> </td> 
  </tr> 
 </tbody> 
</table>

**Standaardformaatreeksen**

De volgende standaardformaatkoorden worden gebruikt door malplaatjes. U kunt aan deze lijst toevoegen of het uitgeven zonodig.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Standaardformaattekenreeks </p> </th> 
   <th colname="col2" class="entry"> <p>Resulterend voorbeeld </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>%B %d, %Y %T %Z </p> </td> 
   <td colname="col2"> <p> 5 september 1999 13:12:00 PDT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%b %d, %Y %T %Z </p> </td> 
   <td colname="col2"> <p> 5 sep. 1999 13:12:00 PDT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%A %B %d, %Y %T %Z </p> </td> 
   <td colname="col2"> <p> Zondag 5 september 1999 13:12:00 PDT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%A %b %d, %Y %T %Z </p> </td> 
   <td colname="col2"> <p> Zondag 5 sep. 1999 13:12:00 PDT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%a %B %d, %Y %T %Z </p> </td> 
   <td colname="col2"> <p> Sun September 1999 13:12:00 PDT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%a %b %d, %Y %T %Z </p> </td> 
   <td colname="col2"> <p> Sun Sept 5, 1999 13:12:00 PDT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%d %b %Y %T %Z </p> </td> 
   <td colname="col2"> <p> 5 sep. 1999 13:12:00 PDT </p> </td> 
  </tr> 
 </tbody> 
</table>

