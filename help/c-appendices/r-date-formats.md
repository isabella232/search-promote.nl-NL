---
description: U kunt de datumnotaties definiëren die worden gebruikt wanneer een veld met een gegevenstype "date" wordt geparseerd en geïndexeerd.
seo-description: U kunt de datumnotaties definiëren die worden gebruikt wanneer een veld met een gegevenstype "date" wordt geparseerd en geïndexeerd.
seo-title: Datumnotaties
solution: Target
title: Datumnotaties
topic: Appendices,Site search and merchandising
uuid: 148914b5-33ef-41db-8404-67c03f6f0832
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 0%

---


# Datumnotaties{#date-formats}

U kunt de datumnotaties definiëren die worden gebruikt wanneer een veld met een gegevenstype &quot;date&quot; wordt geparseerd en geïndexeerd.

De notatie van de datum en tijd wordt opgegeven met een notatietekenreeks. De indelingstekenreeks bestaat uit nul of meer conversiespecificaties (een conversiespecificatie bestaat uit een procentteken en een ander teken) en gewone tekens. Er wordt een standaardlijst met datumnotatietekenreeksen voor elk datumveld weergegeven.

U hebt volledige controle over deze lijst en kunt deze toevoegen aan of wijzigen om aan de behoeften van uw site te voldoen. De bovenste notatietekenreeks heeft voorrang en volgende indelingstekenreeksen worden alleen gebruikt als het parseren van de inhoud van een metagegevenstag een fout oplevert.

Stel dat u de volgende datumnotaties hebt opgegeven:

<table> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>%B %d, %Y %T %Z </p> <p>%b %d, %Y %T %Z </p> <p>%A %B %d, %Y %T %Z </p> <p>%A %b %d, %Y %T %Z </p> <p>%a %B %d, %Y %T %Z </p> <p>%a %b %d, %Y %T %Z </p> <p>%d %b %Y %T %Z </p> </td> 
  </tr> 
 </tbody> 
</table>

De eerste notatie, &quot;%B %d, %Y %T %Z&quot;, komt overeen met datums als &quot;20 september 2014 13:12:00 PDT&quot;. Als de inhoud van de metagegevenstag niet kan worden geparseerd met deze indelingstekenreeks, wordt de volgende beschikbare indeling &quot;%b %d, %Y %T %Z&quot; geprobeerd. Deze notatie komt overeen met datums als: &quot;20 september 2014 3:12:00 PDT&quot;. Als de inhoud van de metagegevenstag niet met deze indelingstekenreeks kan worden geparseerd, wordt bij het zoeken/verhandelen van de site de lijst met opmaaktekenreeksen omlaag verplaatst totdat een opmaaktekenreeks wordt gevonden die werkt.

In de volgende tabel worden de beschikbare datumnotatietekenreeksen beschreven:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Gegevensindeling </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>%A </p> </td> 
   <td colname="col2"> <p>Komt overeen met de nationale representatie van de volledige weekdagnaam, bijvoorbeeld "maandag". De nationale vertegenwoordiging wordt bepaald door de "Taal"instelling op de "Woorden &amp; Talen"Optie </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%a </p> </td> 
   <td colname="col2"> <p> komt overeen met de nationale representatie van de afgekorte weekdagnaam, waarbij de afkorting de eerste drie tekens is, bijvoorbeeld "Mon." De nationale vertegenwoordiging wordt bepaald door de "Taal"instelling op de "Woorden &amp; Talen"Optie </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%B </p> </td> 
   <td colname="col2"> <p> komt overeen met de nationale vertegenwoordiging van de volledige naam van de maand, bijvoorbeeld "June." De nationale vertegenwoordiging wordt bepaald door de "Taal"instelling op de "Woorden &amp; Talen"Optie </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%b </p> </td> 
   <td colname="col2"> <p> komt overeen met de nationale representatie van de afgekorte naam van de maand, waarbij de afkorting de eerste drie tekens is, bijvoorbeeld "Jun." De nationale vertegenwoordiging wordt bepaald door de "Taal"instelling op de "Woorden &amp; Talen"Optie </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%D </p> </td> 
   <td colname="col2"> <p> komt overeen met "%m/%d/%y", bijvoorbeeld "06/06/01" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%d </p> </td> 
   <td colname="col2"> <p> komt de dag van de maand als decimaal aantal (01-31) overeen </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%e </p> </td> 
   <td colname="col2"> <p> de dag van de maand als een decimaal getal (1-31); enkele cijfers worden voorafgegaan door een lege </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%H </p> </td> 
   <td colname="col2"> <p> komt het uur (24-uurs klok) als decimaal aantal (00-23) overeen </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%h </p> </td> 
   <td colname="col2"> <p> komt overeen met de nationale representatie van de afgekorte naam van de maand, waarbij de afkorting de eerste drie tekens is, bijvoorbeeld "Jun" (gelijk aan %b) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%I </p> </td> 
   <td colname="col2"> <p> komt het uur (12-uurklok) als decimaal aantal (01-12) overeen </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%j </p> </td> 
   <td colname="col2"> <p> komt overeen met de dag van het jaar als een decimaal getal (001-366) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%k </p> </td> 
   <td colname="col2"> <p> het uur (24-uurs klok) als decimaal aantal (0-23) aanpast; enkele cijfers worden voorafgegaan door een lege </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%l </p> </td> 
   <td colname="col2"> <p> het uur (12-uurs klok) als decimaal aantal (1-12) aanpast; enkele cijfers worden voorafgegaan door een lege </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%M </p> </td> 
   <td colname="col2"> <p> komt overeen met de minuut als een decimaal getal (00-59) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%m </p> </td> 
   <td colname="col2"> <p> komt overeen met de maand als een decimaal getal (01-12) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%p </p> </td> 
   <td colname="col2"> <p> komt overeen met de nationale vertegenwoordiging van "ante meridiem" of "post meridiem" naar gelang van het geval, bv. "PM." De nationale vertegenwoordiging wordt bepaald door de "Taal"instelling op de "Woorden &amp; Talen"Optie </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%R </p> </td> 
   <td colname="col2"> <p> is gelijk aan "%H:%M", bijvoorbeeld "13:23" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%r </p> </td> 
   <td colname="col2"> <p> is gelijk aan "%I:%M:%S %p", bijvoorbeeld "01:23:45 PM" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%S </p> </td> 
   <td colname="col2"> <p> komt overeen met de tweede als een decimaal getal (00-60) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%T </p> </td> 
   <td colname="col2"> <p> is gelijk aan "%H:%M:%S", bijvoorbeeld "13:26:47" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%U </p> </td> 
   <td colname="col2"> <p> komt overeen met het weeknummer van het jaar (zondag als de eerste dag van de week) als een decimaal getal (00-53) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%v </p> </td> 
   <td colname="col2"> <p> is gelijk aan "%e-%b-%Y", bijvoorbeeld "6-jun-2001" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%Y </p> </td> 
   <td colname="col2"> <p> komt overeen met het jaar met de eeuw als een decimaal getal, bijvoorbeeld "2001" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%y </p> </td> 
   <td colname="col2"> <p> komt overeen met het jaar zonder eeuw als een decimaal getal (00-99) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%Z </p> </td> 
   <td colname="col2"> <p> komt overeen met de naam van de tijdzone </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%% </p> </td> 
   <td colname="col2"> <p> matches "%" </p> </td> 
  </tr> 
 </tbody> 
</table>

**Standaardindelingsreeksen**

De volgende standaardformaatkoorden worden gebruikt door malplaatjes. U kunt deze lijst uitbreiden of indien nodig bewerken.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Standaardindelingstekenreeks </p> </th> 
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
   <td colname="col2"> <p> zondag 5 september 1999 13:12:00 PDT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%A %b %d, %Y %T %Z </p> </td> 
   <td colname="col2"> <p> 5 september 1999 13:12:00 PDT </p> </td> 
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

