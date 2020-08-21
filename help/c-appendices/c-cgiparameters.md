---
description: 'null'
seo-description: 'null'
seo-title: CGI-parameters
solution: Target
title: CGI-parameters
topic: Appendices,Site search and merchandising
uuid: a5f43547-bc15-44aa-ba23-6b8b573e09d2
translation-type: tm+mt
source-git-commit: 7b883870bb16284d8070a21547cdb62cc79d7632
workflow-type: tm+mt
source-wordcount: '5490'
ht-degree: 0%

---


# CGI-parameters{#cgi-parameters}

## CGI-parameters {#concept_F395999090FE4926B38BC73D5E612800}

## CGI-parameters doorzoeken {#reference_DA27A8B0728246DA94994885E1353890}

U kunt de code van het formulier doorzoeken. U kunt deze code kopiëren en plakken in de HTML van uw site ( **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Form Source]**).

Zie De HTML-code van het zoekformulier [kopiëren naar...](../c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

U kunt ook de parameters instellen die in het zoekformulier zelf of vanuit een script worden weergegeven. Naast de parameters die hieronder worden vermeld kunt u ook de achtergrondzoekparameters gebruiken om het zoeken te besturen.

Zie CGI-parameters voor [achtergrondzoekopdrachten](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8).

Zoekverzoeken bestaan uit een basis-URL. De basis-URL geeft aan welke account de klant zoekt en een set CGI-parameters (sleutel-waardeparen) die aangeven hoe de gewenste zoekresultaten voor de gekoppelde account moeten worden geretourneerd.

De basis-URL is gekoppeld aan een specifieke account en een gefaseerde of live omgeving. U kunt meerdere aliassen voor de basis-URL aanvragen bij uw accountmanager. Een bedrijf met de naam Megacorp kan bijvoorbeeld twee basis-URL&#39;s hebben gekoppeld aan het bijbehorende account: `https://search.megacorp.com` en `https://stage.megacorp.com`. De eerste URL zoekt naar hun live index en de laatste URL zoekt naar hun gefaseerde index.

Er worden drie indelingen van CGI-parameters ondersteund. Standaard is uw account geconfigureerd om CGI-parameters te scheiden met een puntkomma, zoals in het volgende voorbeeld:

`https://search.megacorp.com?q=shoes;page=2`

Indien gewenst, kunt uw accountmanager uw account zo configureren dat deze ampersands gebruikt om de CGI-parameters te scheiden, zoals in het volgende voorbeeld:

`https://search.megacorp.com?q=shoes&page=2`

Een derde indeling, de zogenaamde SEO-indeling, wordt ook ondersteund wanneer een slash `/` wordt gebruikt in plaats van het scheidingsteken en het gelijkteken, zoals in het volgende voorbeeld:

`https://search.megacorp.com/q/shoes/page/2`

Elke keer dat de SEO-indeling wordt gebruikt om een aanvraag te verzenden, worden alle uitvoerkoppelingen in dezelfde indeling geretourneerd.

| De parameter Begeleide zoekopdracht | Voorbeeld | Beschrijving |
|--- |--- |--- |
| q | `q=string` | Geeft de queryreeks voor de zoekopdracht aan. Deze parameter verwijst naar de zoekparameter voor `sp_q` achterwaarts zoeken.  Zie CGI-parameters voor [achtergrondzoekopdrachten](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8). |
| q# | `q#=string` | Facultatief (het zoeken binnen een bepaald gebied) wordt gedaan door genummerde parameters q en x.  De parameter q definieert de term waarnaar u zoekt in het facet, zoals aangegeven door de overeenkomstige parameter numbered x.<br>Bijvoorbeeld, als u twee facetten hebt die grootte en kleur worden genoemd, kunt u iets zoals q1=small;x1=size;q2=red;x2=color hebben.  Deze parameter verwijst naar de zoekparameters voor de `sp_q_exact_#` achterkant.  <br>Zie CGI-parameters voor [achtergrondzoekopdrachten](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8). |
| x# | `q#=string` | Facultatief (het zoeken binnen een bepaald gebied) wordt gedaan door genummerde parameters q en x.  De parameter q definieert de term waarnaar u zoekt in het facet, zoals aangegeven door de overeenkomstige parameter numbered x. <br>Bijvoorbeeld, als u twee facetten hebt die grootte en kleur worden genoemd, kunt u iets zoals q1=small;x1=size;q2=red;x2=color hebben.  Deze parameter verwijst naar de zoekparameters voor de `sp_x_#` achterkant.  <br>Zie CGI-parameters voor [achtergrondzoekopdrachten](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8). |
| collectie | `collection=string` | Geeft de verzameling op die voor de zoekopdracht moet worden gebruikt.  Deze parameter verwijst naar de zoekparameter voor `sp_k` achterwaarts zoeken.  Zie CGI-parameters voor [achtergrondzoekopdrachten](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8). |
| aantal | `count=number` | Hiermee geeft u het totale aantal resultaten op dat wordt weergegeven.  De standaardwaarde wordt gedefinieerd in [!UICONTROL Settings ] > [!UICONTROL Searching ] > [!UICONTROL Searches ]. .  Deze parameter verwijst naar de zoekparameter voor `sp_c` achterwaarts zoeken.  Zie CGI-parameters voor [achtergrondzoekopdrachten](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8). |
| page | `page=number` | Geeft de pagina met resultaten aan die worden geretourneerd. |
| rangschikken | `rank=field` | Hiermee geeft u het rangtelveld op dat moet worden gebruikt voor statische waarderingen.  Het veld moet een veld van het type Rank zijn met een relevantie groter dan 0.  Deze parameter verwijst naar de parameter `sp_sr` backend.  Zie CGI-parameters voor [achtergrondzoekopdrachten](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8). |
| sorteren | `sort=number` | Hiermee geeft u de sorteervolgorde op.<br>&quot;0&quot; is de standaardwaarde en sorteert op relevantiescore; &quot;1&quot; sorteert op datum; &quot;-1&quot; wordt niet gesorteerd.  Gebruikers kunnen een veldnaam voor de waarde van de `sp_s` parameter opgeven.  Hiermee sorteert u bijvoorbeeld de resultaten op basis van de waarden in het titelveld. `sp_s=title` Wanneer een veldnaam wordt gebruikt voor de waarde van een ` sp_s ` parameter, worden de resultaten gesorteerd op dat veld en vervolgens gesubsorteerd op relevantie.  Klik op [!UICONTROL Settings ] > [!UICONTROL Metadata ] > [!UICONTROL Definitions ]. Klik op de pagina Definities op [!UICONTROL Add New Field ] of klik op [!UICONTROL Edit ] een bepaalde veldnaam. Selecteer in de [!UICONTROL Sorting ] vervolgkeuzelijst een [!UICONTROL Ascending ] of [!UICONTROL Descending ]. Deze parameter verwijst naar de zoekparameter voor `sp_s` achterwaarts zoeken. <br>Zie CGI-parameters voor [achtergrondzoekopdrachten].(../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8). |

## CGI-parameters voor achtergrondzoekopdrachten {#reference_582E85C3886740C98FE88CA9DF7918E8}

Klanten hebben doorgaans interactie met een presentatielaag, de zogenaamde Guided Search. Het is echter theoretisch mogelijk om de laag met instructies-zoekopdrachten over te slaan en rechtstreeks met de achterste zoekopdracht te werken aan de hand van de CGI-parameters die op deze pagina worden beschreven.

U kunt de parameters van het achterste onderzoekCGI van de volgende lijst selecteren:
<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> </th> 
   <th colname="col2" class="entry"> <p>Ondersteuning voor één query </p> </th> 
   <th colname="col03" class="entry"> <p>Ondersteuning voor meerdere query's </p> </th> 
   <th colname="col3" class="entry"> <p>Voorbeelden </p> </th> 
   <th colname="col4" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>1 </p> </td> 
   <td colname="col2"> <p>sp_a </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_a= string </span> </p> </td> 
   <td colname="col4"> <p>Specifies the account number string. Deze parameter is vereist en moet een geldige tekenreeks voor het accountnummer zijn. U kunt de tekenreeks voor uw accountnummer vinden via <span class="uicontrol"> Instellingen </span> &gt; <span class="uicontrol"> Accountopties </span> &gt; <span class="uicontrol"> Accountinstellingen </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>sp_advanced </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_advanced= 0 of 1 </span> </p> </td> 
   <td colname="col4"> <p>Als <span class="codeph"> sp_advanced=1 met een vraag </span> wordt voorgelegd, dan wordt al code tussen de <span class="codeph"> &lt;search-if-advanced&gt; </span> markering en de <span class="codeph"> &lt;/search-if-advanced&gt; </span> markering in het onderzoeksmalplaatje gebruikt voor het onderzoeksvorm. Alle code tussen de <span class="codeph"> &lt;search-if-not-advanced&gt;- </span> tag en de <span class="codeph"> &lt;/search-if-not-advanced&gt;- </span> tag wordt genegeerd. Als <span class="codeph"> sp_advanced=0 </span> (of een andere waarde) wordt verzonden, wordt het sjabloonblok &lt;search-if-advanced&gt; genegeerd en wordt het sjabloonblok &lt;search-if-not-advanced&gt; gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>sp_c </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_c= number </span> </p> </td> 
   <td colname="col4"> <p>Hiermee geeft u het totale aantal resultaten op dat moet worden weergegeven. De standaardwaarde is 10. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>sp_context_field </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_context_field= <i>field</i> </code> </p> </td> 
   <td colname="col4"> <p>Verzamelt contextuele informatie voor het bepaalde gebied. Verzamelde informatie wordt in de zoekresultaten uitgevoerd met de sjabloontag <span class="codeph"> &lt;search-context&gt; </span> . De standaardwaarde is <span class="codeph"> body </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>5 </p> </td> 
   <td colname="col2"> <p>sp_d </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_d= type </span> </p> </td> 
   <td colname="col4"> <p>Hiermee wordt het type datumbereik opgegeven dat wordt gezocht. Mogelijke waarden voor type zijn om het even welk, wat betekent geen databereik het zoeken uitvoert, douane, die erop wijst dat de waarde van <span class="codeph"> sp_date_range </span> zou moeten worden gebruikt om de data te bepalen te zoeken, en specifiek, die erop wijst dat de waarden in <span class="codeph"> _start_day </span>, <span class="codeph"> sp_start_month </span>, <span class="codeph"> sp_start_year </span>, <span class="codeph"> </span><span class="codeph"> </span><span class="codeph"> </span> _end_end_month worden gebruikt en ssp_end_year om het datumbereik te bepalen waarnaar moet worden gezocht. <span class="codeph"> sp_d </span> wordt slechts vereist als uw onderzoeksvorm de optie bevat om of door een douanewaaier (als <span class="codeph"> sp_date_range </span>), of door een specifieke begin en einddatumwaaier te zoeken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p> sp_d_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_d_#= type </span> </p> </td> 
   <td colname="col4"> <p>Specificeert het type van datumwaaier die voor de overeenkomstige <span class="codeph"> sp_q_# </span> vraag zoekt uit te voeren. "#"wordt vervangen met een aantal tussen 1 en 16 (bijvoorbeeld, <span class="codeph"> sp_d_8 </span>, is op de genummerde vraag <span class="codeph"> sp_q_8 van toepassing </span>). </p> <p>U kunt <span class="codeph"> type aan om het even welk plaatsen, wat betekent geen het zoeken van de datumwaaier uitvoeren, douane, die erop wijst dat de waarde van </span> sp_date_range_# <span class="codeph"> wordt gebruikt om de data te bepalen te zoeken, en specifiek, die erop wijst dat de waarden in </span> sp_q_min_day_# <span class="codeph"> , </span>sp_q_min_month_# <span class="codeph"> , </span><span class="codeph"> </span><span class="codeph"> </span><span class="codeph"> </span><span class="codeph"> </span> sp_q_min_year_#, SP_sp_q_max_month_#, en sp_q_max_year_# zou moeten worden gebruikt om de datumwaaier te bepalen. Het gebruik van <span class="codeph"> sp_d_# </span> wordt slechts vereist als uw onderzoeksvorm de optie bevat om of door een douanewaaier (als <span class="codeph"> sp_date_range_# </span>), of door een specifieke begin en einddatumwaaier te zoeken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>7 </p> </td> 
   <td colname="col2"> <p>sp_date_range </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_date_range= <i>number</i> </code> </p> </td> 
   <td colname="col4"> <p>Hiermee geeft u een vooraf gedefinieerd datumbereik op dat u wilt toepassen op de zoekopdracht. Waarden groter dan of gelijk aan nul geven het aantal dagen op dat moet worden doorzocht vóór vandaag. De waarde "0" geeft bijvoorbeeld "vandaag" aan, de waarde "1" geeft "vandaag en gisteren" aan, de waarde "30" geeft "binnen de laatste 30 dagen" enzovoort. </p> <p>Waarden onder nul geven als volgt een aangepast bereik op: </p> <p>-1 = "Geen", gelijk aan het opgeven van geen datumbereik. </p> <p>-2 = "Deze week,"die van zondag tot Zaterdag van de huidige week zoekt. </p> <p>-3 = "Vorige week", waarmee wordt gezocht van zondag tot zaterdag van de week voorafgaand aan de huidige week. </p> <p>-4 = "Deze maand,"die data binnen de huidige maand zoekt. </p> <p>-5 = "Vorige maand,"die data binnen de maand voorafgaand aan de huidige maand zoekt. </p> <p>-6 = "Dit jaar,"dat data binnen het huidige jaar zoekt. </p> <p>-7 = "Vorig jaar", dat data zoekt in het jaar voorafgaand aan het lopende jaar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>8 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_date_range_# </p> </td> 
   <td colname="col3"> <p> <code> sp_date_range_#= <i>number</i> </code> </p> </td> 
   <td colname="col4"> <p>Specificeert een vooraf bepaalde datumwaaier om op de overeenkomstige <span class="codeph"> sp_q_# </span> vraag van toepassing te zijn. "#"wordt vervangen met een aantal tussen 1 en 16 (bijvoorbeeld, <span class="codeph"> sp_date_range_8 </span>, is op genummerde vraag <span class="codeph"> sp_q_8 van toepassing </span>). </p> <p>Waarden groter dan of gelijk aan nul geven het aantal dagen aan dat moet worden doorzocht vóór vandaag. De waarde 0 geeft vandaag bijvoorbeeld aan; de waarde 1 geeft vandaag en gisteren aan; een waarde van 30 specificeert binnen de laatste 30 dagen, etc. </p> <p>Waarden onder nul geven als volgt een aangepast bereik op: </p> <p>-1 = "Geen", gelijk aan het opgeven van geen datumbereik. </p> <p>-2 = "Deze week,"die van zondag tot Zaterdag van de huidige week zoekt. </p> <p>-3 = "Vorige week", waarmee wordt gezocht van zondag tot zaterdag van de week voorafgaand aan de huidige week. </p> <p>-4 = "Deze maand,"die data binnen de huidige maand zoekt. </p> <p>-5 = "Vorige maand,"die data binnen de maand voorafgaand aan de huidige maand zoekt. </p> <p>-6 = "Dit jaar,"dat data binnen het huidige jaar zoekt. </p> <p>-7 = "Vorig jaar", dat data zoekt in het jaar voorafgaand aan het lopende jaar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>9 </p> </td> 
   <td colname="col2"> <p>sp_dedupe_field </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_dedupe_field= <i>fieldname</i> </code> </p> </td> 
   <td colname="col4"> <p>Hiermee geeft u één veld op waarin de zoekresultaten moeten worden gededupliceerd. Alle dubbele resultaten in dat veld worden verwijderd uit de zoekresultaten. Als voor <span class="codeph"> sp_dedupe_field=title bijvoorbeeld </span>, alleen het bovenste resultaat voor een bepaalde titel wordt weergegeven in de zoekresultaten (geen twee resultaten hebben dezelfde inhoud van het titelveld). Voor tekstvelden met meerdere waarden (lijst van gewenste personen) wordt de volledige inhoud van het veld gebruikt voor de vergelijking. Er kan slechts één veld worden opgegeven. Een 'table-Qualifier' is niet toegestaan in de veldnaam. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>10 </p> </td> 
   <td colname="col2"> <p>sp_e </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_e= number </span> </p> </td> 
   <td colname="col4"> <p>Geeft aan dat jokertekens automatisch moeten worden uitgebreid voor elk woord uit de queryreeks met meer dan getaltekens. Met andere woorden, <span class="codeph"> sp_e=5 </span> specificeert dat de woorden met 5 of meer karakters, zoals "vraag"of "aantal", met het vervangingskarakter '*' zouden moeten worden uitgebreid, makend het onderzoek gelijkwaardig aan een onderzoek naar "vraag*" of "aantal*". Woorden met minder tekens worden niet uitgevouwen, dus een zoekopdracht naar "woord" heeft geen automatische uitbreiding van jokertekens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>11 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p> sp_e_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_e_#= number </span> </p> </td> 
   <td colname="col4"> <p>Specificeert dat de automatische vervangingsuitbreiding voor om het even welk woord van het overeenkomstige <span class="codeph"> sp_q_# </span> vraagkoord met meer dan aantalkarakters plaatsvindt. Met andere woorden, <span class="codeph"> sp_e_2=5 </span> specificeert dat de woorden met vijf of meer karakters in <span class="codeph"> sp_q_2 </span> vraagkoord, zoals "vraag"of "aantal", met het vervangingskarakter ' <span class="codeph"> * </span>' zouden moeten worden uitgebreid, makend het onderzoek gelijkwaardig aan een onderzoek naar "vraag*" of "aantal*". Woorden met minder tekens worden niet uitgevouwen, dus een zoekopdracht naar "woord" in <span class="codeph"> sp_q_2 </span> zou geen automatische uitbreiding van jokertekens hebben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>12 </p> </td> 
   <td colname="col2"> <p>sp_end_day, sp_end_month, sp_end_year </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_end_day= <i>number</i>,sp_end_month= <i>number</i>, sp_end_year= <i>number</i> </code> </p> </td> 
   <td colname="col4"> <p>Dit drievoudige van waarden specificeert de einddatumwaaier voor het onderzoek en moet als reeks worden verstrekt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>13 </p> </td> 
   <td colname="col2"> <p>sp_f </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_f= string </span> </p> </td> 
   <td colname="col4"> <p>Specificeert de karakterreeks van de koorden van de vraagparameter (zoals <span class="codeph"> sp_q </span>). Deze tekenreeks moet altijd overeenkomen met de tekenset van de pagina die het zoekformulier bevat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>14 </p> </td> 
   <td colname="col2"> <p>sp_field_table </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_field_ table=table: field,field... </code> </p> </td> 
   <td colname="col4"> <p>Definieert een logische gegevenstabel die uit de opgegeven velden bestaat. Een tabel met de naam "items", bestaande uit de velden "kleur", "grootte" en "prijs", wordt bijvoorbeeld als volgt gedefinieerd: </p> <p> <span class="codeph"> sp_field_table=items:color,size,price </span> </p> <p>Logische tabellen zijn vooral handig in combinatie met velden waarvoor "Lijsten van gewenste personen" zijn ingeschakeld (onder <span class="uicontrol"> Instellingen </span> &gt; <span class="uicontrol"> Metagegevens </span> &gt; <span class="uicontrol"> Definities </span>). Alle CGI-parameters en sjabloontags die een veldnaam als een waarde hebben, kunnen optioneel een tabelnaam opgeven gevolgd door een "". vóór de veldnaam (bijvoorbeeld <span class="codeph"> sp_x_1=tablename.fieldName </span>). </p> <p>Als u bijvoorbeeld wilt zoeken naar documenten die een of meer "rode" items in grootte "groot" bevatten (items worden weergegeven als parallelle rijen met metagegevens), kunt u het volgende gebruiken: </p> <p> <code> sp_q_exact_1=red&amp;sp_x_1=items.color&amp; sp_q_exact_2=large&amp;sp_x_2=items.size&amp;sp_field_table=items:color,size,price </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>15 </p> </td> 
   <td colname="col2"> sp_i </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_i= <span class="varname"> waarde </span> </span> </p> </td> 
   <td colname="col4"> <p>Hiermee negeert u de zoekopdracht wanneer u rapporten genereert. </p> <p>Gebruik deze query om bepaalde zoekopdrachten op de achtergrond te maskeren, zoals zoekopdrachten die u hebt bedoeld, genereren of zoekopdrachten die een beheerder in het lidcentrum genereert. Omdat een eindgebruiker deze soorten onderzoeken niet produceert, verschijnen zij niet in diverse rapporten van de Search&amp;Promote van Adobe. </p> <p>Geldige waarden zijn <span class="codeph"> sp_i=1 </span> en <span class="codeph"> sp_i=2 </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>16 </p> </td> 
   <td colname="col2"> <p>sp_k </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_k= string </span> </p> </td> 
   <td colname="col4"> <p> Geeft de verzameling op die voor de zoekopdracht moet worden gebruikt. Het gebrek is geen inzameling, betekenend dat het onderzoek de gehele plaats zou moeten omvatten. </p> <p>Zie <a href="../c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3" type="reference" format="dita" scope="local"> Verzamelingen gebruiken in zoekformulieren </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>17 </p> </td> 
   <td colname="col2"> <p>sp_l </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_l= string </span> </p> </td> 
   <td colname="col4"> <p>Specificeert de taal van de koorden van de vraagparameter (zoals <span class="codeph"> sp_q </span>). De <i><span class="codeph"> tekenreeks </span></i> moet een standaard landinstellings-id zijn met een ISO-639-taalcode, optioneel gevolgd door een ISO-3166-landcode. Bijvoorbeeld "en" of "en_US" voor Engels of "ja" of "ja_JP" voor Japans. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>18 </p> </td> 
   <td colname="col2"> <p>sp_literal </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_literal= 0 of 1 </span> </p> </td> 
   <td colname="col4"> <p> Het plaatsen <span class="codeph"> sp_literal=1 maakt </span> tijdelijk alle eigenschappen onbruikbaar die de woorden in de vraag zouden kunnen interpreteren. Met deze parameter komen alleen de letterlijke woorden van de query overeen met documenten, ongeacht synoniemen, alternatieve tekstformulieren en overeenkomsten op basis van geluid. </p> <p>Merk op dat <span class="codeph"> sp_literal=0 geen betekenis </span> heeft, en indien gebruikt genegeerd. </p> <p>Zie <a href="../c-about-linguistics-menu/c-about-dictionaries.md#concept_B8028B71EC8144669614C64578EDB034" type="concept" format="dita" scope="local"> Informatie over woordenboeken </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>19 </p> </td> 
   <td colname="col2"> <p>sp_m </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_m= number </span> </p> </td> 
   <td colname="col4"> <p> Hiermee bepaalt u of overzichten worden weergegeven. 1 is ja, 0 is nee. De standaardwaarde is 1. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>20 </p> </td> 
   <td colname="col2"> <p>sp_n </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_n= number </span> </p> </td> 
   <td colname="col4"> <p> Hier geeft u het nummer op van het resultaat waarmee de zoekresultaten worden gestart. De standaardwaarde is 1. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>21 </p> </td> 
   <td colname="col2"> <p>sp_not_found_page </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_not_found_page= url </span> </p> </td> 
   <td colname="col4"> <p> Geeft aan of naar de opgegeven URL moet worden omgeleid als er geen zoekresultaten zijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>22 </p> </td> 
   <td colname="col2"> <p>sp_p </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_p= any/all/express </span> </p> </td> 
   <td colname="col4"> <p> Hiermee geeft u het standaardtype zoeken op dat moet worden uitgevoerd. Het gebruik van <span class="codeph"> om het even welke </span> middelen onderzoek naar documenten die om het even welk woord van het vraagkoord bevatten. Het gebruik van <span class="codeph"> alles </span> betekent onderzoek naar documenten die alle woorden in het vraagkoord bevatten. Het gebruik van <span class="codeph"> uitdrukking </span> betekent het vraagkoord wordt behandeld alsof het een geciteerde uitdrukking was en alle user-typed citaten worden genegeerd. </p> <p>Voor <span class="codeph"> woordgroepen </span> en <span class="codeph"> alle </span>woorden is de specificatie "+" en "-" voor zoekwoorden uitgeschakeld en worden deze tekens genegeerd. Als <span class="codeph"> sp_p niet aanwezig </span> is, of als het aan een leeg koord of om het even welk wordt geplaatst, worden de standaard "+"en "-"woordprefixen toegestaan. </p> <p>Zie de beschrijving van Zoektips voor meer informatie over het gebruik van plus ("+") en min ("-") in zoekopdrachten. </p> <p>Zie <a href="../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8" type="concept" format="dita" scope="local"> Over zoekopdrachten </a>. </p> <p>Zie het voorbeeld geavanceerde onderzoeksvorm voor voorbeelden bij het gebruiken van de <span class="codeph"> sp_p </span> parameter. </p> <p>Zie <a href="../c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A" type="reference" format="dita" scope="local"> Voorbeeld van een geavanceerd zoekformulier </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>23 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p> sp_p_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_p_#= enige/alle/woordgroep </span> </p> </td> 
   <td colname="col4"> <p>Specificeert het standaardtype van het zoeken dat met de overeenkomstige <span class="codeph"> sp_q_# </span> vraag moet worden uitgevoerd. "#"wordt vervangen met een aantal tussen 1 en 16 (bijvoorbeeld, is <span class="codeph"> sp_p_8 </span> op de genummerde vraag <span class="codeph"> sp_q_8 </span>) van toepassing. Het gebruik van <span class="codeph"> om het even welke </span> middelen terugkeerdocumenten die om het even welk woord van het vraagkoord bevatten. Het gebruik van <span class="codeph"> alle </span> betekent terugkeerdocumenten die alle woorden in het vraagkoord bevatten. Het gebruik van <span class="codeph"> woordgroepen </span> betekent dat de queryreeks wordt behandeld als een volledige woordgroep (en alle door de gebruiker getypte aanhalingstekens worden genegeerd). </p> <p>Als u <span class="codeph"> alle </span> of <span class="codeph"> </span>woordgroepen opgeeft, worden alle plus- en mintekens vóór zoekwoorden genegeerd. Als <span class="codeph"> sp_p_# </span> wordt weggelaten, of als het aan een leeg koord of <span class="codeph"> om het even welke </span>, standaard "+"en "-"prefixen wordt geplaatst worden toegestaan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>24 </p> </td> 
   <td colname="col2"> <p>sp_pt </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_pt= <i>exact/equivalent/compatible</i> </code> </p> </td> 
   <td colname="col4"> <p> Geeft het type doelovereenkomst aan dat moet worden toegepast. Het gebruik van <span class="codeph"> exact </span> betekent dat de doelen van het rendement alleen overeenkomen met documenten die exact overeenkomen met de querytekenreeks binnen de doelinhoud. Het gebruik van <span class="codeph"> equivalent </span> is vergelijkbaar met exact, behalve dat de volgorde van de woorden niet belangrijk is. Het gebruik van <span class="codeph"> compatibel </span> plaatst automatisch het doel aanpassingstype dat op de waarde van de <span class="codeph"> sp_p </span> parameter wordt gebaseerd. Het gebruik van <span class="codeph"> exact </span> wordt gebruikt als <span class="codeph"> sp_p </span> <span class="codeph"> alle </span> of <span class="codeph"> woordgroepen is </span>, anders <span class="codeph"> wordt er equivalent </span> gebruikt. De standaardwaarde van <span class="codeph"> sp_pt </span> is <span class="codeph"> compatibel </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>25 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_pt_# </p> </td> 
   <td colname="col3"> <p> <code> sp_pt_#= <i>exact/equivalent/compatible</i> </code> </p> </td> 
   <td colname="col4"> <p>Specificeert het type van doel aanpassing om met de overeenkomstige <span class="codeph"> sp_q_# </span> vraag toe te passen. "#"wordt vervangen met een aantal tussen 1 en 16 (bijvoorbeeld, is <span class="codeph"> sp_p_8 </span> op de genummerde vraag <span class="codeph"> sp_q_8 </span>) van toepassing. Het gebruik van <span class="codeph"> exact </span> betekent dat de doelen van het rendement alleen overeenkomen met documenten die exact overeenkomen met de querytekenreeks binnen de doelinhoud. Het gebruik van <span class="codeph"> equivalent </span> is net als <span class="codeph"> exact </span>, maar de volgorde van de woorden is niet belangrijk. Het gebruik van <span class="codeph"> compatibel </span> plaatst automatisch het doel aanpassingstype dat op de waarde van de overeenkomstige <span class="codeph"> sp_p_# </span> parameter wordt gebaseerd: <span class="codeph"> exact </span> wordt gebruikt als <span class="codeph"> sp_p_# alle </span> woorden of woordgroepen zijn, anders wordt <span class="codeph"> equivalent </span> gebruikt. De standaardwaarde van <span class="codeph"> sp_pt_# </span> is <span class="codeph"> compatibel </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>26 </p> </td> 
   <td colname="col2"> <p>sp_q </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q= string </span> </p> </td> 
   <td colname="col4"> <p> Geeft de queryreeks voor de zoekopdracht aan. Een lege tekenreeks leidt ertoe dat er geen resultaten worden weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>27 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_q_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q_#= text </span> </p> </td> 
   <td colname="col4"> <p>Met deze parameter kunt u meerdere query's maken op zoekformulieren. De <span class="codeph"> sp_q_# </span> parameter bevat het vraagkoord in de bepaalde genummerde vraag te gebruiken. Een onderzoeksverzoek kan tot 16 verschillende genummerde vragen ( <span class="codeph"> sp_q_1 </span> aan <span class="codeph"> sp_q_16 </span>) van verwijzingen voorzien. </p> <p>Als u bijvoorbeeld het volgende formulier verzendt, worden alle documenten geretourneerd die de woorden "geweldig" en "boek" bevatten. </p> <p> <code class="syntax html"> Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="great"&gt; 
      Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="books"&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>28 </p> </td> 
   <td colname="col2"> <p>sp_q_day, sp_q_month, sp_q_year </p> </td> 
   <td colname="col03"> <p> sp_q_day_#, sp_q_month_#, sp_q_year_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q_day= integer waarde </span> </p> <p> <span class="codeph"> sp_q_month= integer waarde </span> </p> <p> <span class="codeph"> sp_q_year= integer waarde </span> </p> <p> <span class="codeph"> sp_q_day_#= geheel getal </span> </p> <p> <span class="codeph"> sp_q_month_#= integer waarde </span> </p> <p> <span class="codeph"> sp_q_year_#= integer waarde </span> </p> </td> 
   <td colname="col4"> <p>Deze parameters worden gebruikt om een nauwkeurige datum voor een bepaalde vraag te specificeren. De <span class="codeph"> sp_q_day </span>, <span class="codeph"> sp_q_month </span>, en <span class="codeph"> sp_q_year </span> parameters zijn op de belangrijkste vraag ( <span class="codeph"> sp_q </span>) van toepassing. </p> <p>De <span class="codeph"> # </span>parameter wordt vervangen door een aantal tussen 1 en 16 (bijvoorbeeld, <span class="codeph"> sp_q_day_6 </span>, die op de genummerde vraag <span class="codeph"> sp_q_6 </span>) van toepassing is. Standaard worden alle datums gezocht ten opzichte van Greenwich Mean Time. </p> <p>In de volgende sectie met code kan een gebruiker zoeken naar het woord "oranje" in documenten met de datum "Jan. 1st, 2000"in een user-defined gebied genoemd <span class="codeph"> PublishDate </span>: </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="PublishDate"&gt; Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="orange"&gt;On&nbsp;:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_day_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Day&lt;input&nbsp;type="text"&nbsp;name="sp_q_month_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Month &lt;input&nbsp;type="text"&nbsp;name="sp_q_year_1"&nbsp;size="4"&nbsp;value="2000"&gt;&nbsp;Year&nbsp; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>29 </p> </td> 
   <td colname="col2"> <p>sp_q_location </p> </td> 
   <td colname="col03"> <p>sp_q_location_# </p> </td> 
   <td colname="col3"> <p> <code> sp_q_location=<i>latitude/longitude</i> OR <i>areacode</i> OR <i>zipcode</i> </code> </p> <p> <code> sp_q_location_#= <i>latitude/longitude</i> OR <i>areacode</i> OR <i>zipcode</i> </code> </p> </td> 
   <td colname="col4"> <p>Deze parameters koppelen een locatie aan de hoofd- of genummerde query. Het gebruik van <span class="codeph"> sp_q_location </span> beïnvloedt de belangrijkste vraag, <span class="codeph"> sp_q_location_# </span> (waar <span class="codeph"> # </span> door een aantal van 1 tot 16) wordt vervangen, beïnvloedt de bepaalde genummerde vraag. Deze parameters worden gebruikt om minimale en/of maximale afstand nabijheidsonderzoeken tegen de plaatsgegevens uit te voeren die voor elke plaatspagina worden geïndexeerd. De opmaak van de waarde bepaalt de interpretatie ervan. </p> <p>Een waarde in de vorm DDD (drie cijfers) wordt geïnterpreteerd als een telefoongebied van de V.S.; een waarde in de vorm DDD of DDD-DDDD wordt geïnterpreteerd als Amerikaanse postcode; en een waarde in de notatie ±DD.DDDD±DDD wordt geïnterpreteerd als een breedte-/lengtepaar. De tekens zijn vereist voor elke waarde. Zo geeft +38,6317+120,5509 bijvoorbeeld de breedtegraad 38,6317 en de lengtegraad 120,5509 aan. </p> <p>Zie <a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> Informatie over nabijheid zoeken </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>30 </p> </td> 
   <td colname="col2"> <p>sp_q_max_relevant_distance </p> </td> 
   <td colname="col03"> <p>sp_q_max_relevant_afstand _# </p> </td> 
   <td colname="col3"> <p> <code> sp_q_max_relevant_distance= <i>value</i> </code> </p> <p> <code> sp_q_max_relevant_distance_#= <i>value</i> </code> </p> </td> 
   <td colname="col4"> <p>Deze parameters bepalen de relevantieberekening die wordt toegepast op nabijheidszoekopdrachten. Het gebruik van <span class="codeph"> sp_q_max_relevant_distance </span> beïnvloedt de belangrijkste vraag, <span class="codeph"> sp_q_max_relevant_distance_# </span> (waar <span class="codeph"> # </span> door een aantal van 1 tot 16) wordt vervangen, beïnvloedt de bepaalde genummerde vraag. </p> <p>De standaardwaarde van <span class="codeph"> sp_q_max_relevant_distance </span> is 100. </p> <p>Een perfecte relevantiescore voor de nabijheidscomponent zou een afstand van 0 vertegenwoordigen. Een minimum relevantiescore voor de nabijheidscomponent zou een afstand net over de gespecificeerde <span class="codeph"> sp_q_max_relevant_distance_# </span> waarde vertegenwoordigen. </p> <p>Zie <a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> Informatie over nabijheid zoeken </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>31 </p> </td> 
   <td colname="col2"> <p>sp_q_min_day, sp_q_min_month, sp_q_min_year </p> <p>sp_q_max_day, sp_q_max_month, sp_q_max_year </p> </td> 
   <td colname="col03"> <p>sp_q_min_day_#, sp_q_min_month_#, sp_q_min_year_# </p> <p> sp_q_max_day_#, sp_q_max_month_#, sp_q_max_year_# </p> </td> 
   <td colname="col3"> <p> <code> sp_q_min_day=<i>integer value</i> </code> </p> <p> <code> sp_q_min_month=<i>integer value</i> </code> </p> <p> <code> sp_q_min_year=<i>integer value</i> </code> </p> <p> <code> sp_q_max_day=<i>integer value</i> </code> </p> <p> <code> sp_q_max_month=<i>integer value</i> </code> </p> <p> <code> sp_q_max_year=<i>integer value</i> </code> </p> <p> <code> sp_q_min_day_#=<i>integer value</i> </code> </p> <p> <code> sp_q_min_month_#=<i>integer value</i> </code> </p> <p> <code> sp_q_min_year_#=<i>integer value</i> </code> </p> <p> <code> sp_q_max_day_#=<i>integer value</i> </code> </p> <p> <code> sp_q_max_month_#=<i>integer value</i> </code> </p> <p> <code> sp_q_max_year_#=<i>integer value</i> </code> </p> </td> 
   <td colname="col4"> <p>Deze parameters worden gebruikt om minimum en maximumdatumwaaiers voor een bepaalde vraag te plaatsen. De <span class="codeph"> sp_q_min_day </span>, <span class="codeph"> sp_q_min_month </span>, <span class="codeph"> sp_q_min_year </span>, <span class="codeph"> sp_q_max_day </span>, <span class="codeph"> sp_q_max_month </span><i></i> <span class="codeph"> </span>, ensp_q_max_year parameters zijn van toepassing op de belangrijkste vraag ( sp_q). </p> <p>De <span class="codeph"> # </span>in de parameternaam wordt vervangen door een aantal tussen 1 en 16 (bijvoorbeeld, <span class="codeph"> sp_q_min_day_6 </span> is op genummerde vraag <span class="codeph"> sp_q_6 van toepassing </span>). </p> <p>Het is toegestaan alleen een minimumdatum, alleen een maximumdatum of zowel een minimum- als een maximumdatum op te geven. Voor een bepaald minimum- of maximumgehalte moeten echter alle drie de datumparameters worden opgegeven (dag, maand en jaar). Standaard worden alle datums gezocht ten opzichte van Greenwich Mean Time. </p> <p>In de volgende sectie met code kan een gebruiker het woord "oranje" zoeken in documenten met een datum tussen 1 januari 2000 en 31 december 2000 in een door de gebruiker gedefinieerd veld met de naam <span class="codeph"> PublishDate </span>: </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="PublishDate"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="orange"&gt;Between:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_min_day_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Start&nbsp;Day&lt;input&nbsp;type="text"&nbsp;name="sp_q_min_month_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Start&nbsp;Month 
      &lt;input&nbsp;type="text"&nbsp;name="sp_q_min_year_1"&nbsp;size="4"&nbsp;value="2000"&gt;&nbsp;Start&nbsp;Year 
      And:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_max_day_1"&nbsp;size="2"&nbsp;value="31"&gt;&nbsp;End&nbsp;Day 
      &lt;input&nbsp;type="text"&nbsp;name="sp_q_max_month_1"&nbsp;size="2"&nbsp;value="12"&gt;&nbsp;End&nbsp;Month 
      &lt;input&nbsp;type="text"&nbsp;name="sp_q_max_year_1"&nbsp;size="4"&nbsp;value="2000"&gt;&nbsp;End&nbsp;Year </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>32 </p> </td> 
   <td colname="col2"> <p>sp_q_min, sp_q_max </p> </td> 
   <td colname="col03"> <p>sp_q_min_#, sp_q_max_#, sp_q_exact_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q_min= value </span> </p> <p> <span class="codeph"> sp_q_max= value </span> </p> <p> <span class="codeph"> sp_q_min_#= waarde </span> </p> <p> <span class="codeph"> sp_q_max_#= waarde </span> </p> <p> <span class="codeph"> sp_q_exact_#=value </span> </p> </td> 
   <td colname="col4"> <p>Deze parameters geven een minimale (en/of maximale) waarde op die moet worden toegepast op de hoofd- of genummerde query. Het gebruik van <span class="codeph"> sp_q_min </span>, <span class="codeph"> sp_q_max </span>, en <span class="codeph"> sp_q_exact </span> beïnvloedt de belangrijkste vraag ( <span class="codeph"> sp_q </span>). </p> <p>Vervang <span class="codeph"> # </span>in de parameternaam met een aantal tussen 1 en 16 (bijvoorbeeld, is <span class="codeph"> sp_q_min_8 </span> op genummerde vraag <span class="codeph"> sp_q_8 </span>) van toepassing. </p> <p>Het gebruik van <span class="codeph"> sp_q_exact_# </span> is verkort voor het specificeren van zowel <span class="codeph"> sp_q_min_# </span> als <span class="codeph"> sp_q_max_# </span> met de zelfde waarde. Als <span class="codeph"> sp_q_exact_# </span> wordt gespecificeerd, worden om het even welke overeenkomstige <span class="codeph"> sp_q_min_# </span> of <span class="codeph"> sp_q_max_# </span> parameters genegeerd. </p> <p>De <span class="codeph"> sp_q_min_# </span>, <span class="codeph"> sp_q_max_# </span> en <span class="codeph"> sp_q_exact_# </span> parameters kunnen naar keuze veelvoudige "|"gescheiden waarden specificeren. Als u bijvoorbeeld wilt zoeken naar documenten die de waarde groen of rood bevatten in het veld "kleur": <span class="codeph"> ...&amp;sp_q_exact_1=green|red&amp;sp_x_1=color </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>33 </p> </td> 
   <td colname="col2"> <p>sp_q_nocp </p> </td> 
   <td colname="col03"> <p>sp_q_nocp _# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q_nocp= 1 of 0 </span> </p> <p> <span class="codeph"> sp_q_nocp_#= 1 of 0 </span> </p> </td> 
   <td colname="col4"> <p>De standaardwaarde voor de parameter is <span class="codeph"> </span> 0. Dit betekent dat algemene uitbreiden van woordgroepen worden uitgevoerd. </p> <p>Wanneer reeks aan <span class="codeph"> 1 </span> voor de overeenkomstige onderzoeksvraag, worden de Gemeenschappelijke Uitbreidingen van Punten niet uitgevoerd. </p> <p>Het gebruiken van <span class="codeph"> sp_q_nocp </span> beïnvloedt de belangrijkste parameter van de onderzoeksvraag <span class="codeph"> sp_q </span>. Om deze parameter op een genummerde onderzoeksvraag toe te passen, vervang <span class="codeph"> # </span> in de parameternaam met het overeenkomstige aantal. Bijvoorbeeld, is <span class="codeph"> sp_q_nocp_8 </span> op de genummerde onderzoeksvraag <span class="codeph"> sp_q_8 van toepassing </span>. </p> <p> 
     <!--See also <xref href="c_about_common_phrases.xml#concept_4946E53586DF492EAEB1B7F757FD440F" format="dita" scope="local">About Common Phrases</xref>--> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>34 </p> </td> 
   <td colname="col2"> <p>sp_q_required </p> </td> 
   <td colname="col03"> <p>sp_q _required _# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q_required= 1, 0 of -1 </span> </p> <p> <span class="codeph"> sp_q_required_#= 1 of 0 of -1 </span> </p> </td> 
   <td colname="col4"> <p>Deze parameter bepaalt of een gelijke (1), kan (0), of moet niet (-1) in de overeenkomstige vraag voorkomen opdat een document op de resultaatpagina wordt teruggekeerd. </p> <p>Het gebruik van <span class="codeph"> sp_q_required </span> beïnvloedt de belangrijkste vraag ( <span class="codeph"> sp_q </span>). </p> <p>Om op een genummerde vraag van toepassing te zijn, vervang <span class="codeph"> # </span> in de parameternaam met het overeenkomstige aantal (bijvoorbeeld, <span class="codeph"> sp_q_required_8 </span> is op genummerde vraag <span class="codeph"> sp_q_8 </span>) van toepassing. De standaardwaarde van de parameter is 1 (moet overeenkomen). </p> <p>Als u wilt zoeken naar documenten die het woord "calc" bevatten maar GEEN "mac", "win" of "all" bevatten in het door de gebruiker gedefinieerde veld "platform", kan uw HTML-zoekformulier de volgende regels bevatten: </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="platform"&gt; 
      Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="calc"&gt; 
      Exclude:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="mac&nbsp;win&nbsp;all"&gt; 
      &lt;input&nbsp;type="hidden"&nbsp;name="sp_q_required_1"&nbsp;value="-1"&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>35 </p> </td> 
   <td colname="col2"> <p>sp_redirect_if_one_result </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_redirect_ 
      if_one_result= <i>0 or 1</i> </code> </p> </td> 
   <td colname="col4"> <p>Geeft aan of de URL van het zoekresultaat moet worden doorgestuurd als er slechts één zoekresultaat is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>36 </p> </td> 
   <td colname="col2"> <p>sp_reference </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_reference= url </span> </p> </td> 
   <td colname="col4"> <p>Hier geeft u de referentie-URL voor de zoekopdracht op. Nuttig voor regels voor het herschrijven van zoekopdrachten waarbij de zoekresultaten weer worden gekoppeld aan dezelfde site als het zoekformulier. </p> <p>De standaardwaarde is de standaard CGI HTTP_REFERRER-waarde die door de browser wordt geleverd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>37 </p> </td> 
   <td colname="col2"> <p>sp_ro </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_ro= <span class="varname"> veld </span>: <span class="varname"> relevantie </span> </span> </p> </td> 
   <td colname="col4"> <p>Hiermee wordt optionele zoektijd per veldnaam en relevantie toegestaan. De <span class="codeph"> ro </span> in de parameternaam staat voor "relevantie override". De parameter accepteert een of meer veldnamen, gevolgd door een dubbele punt, gevolgd door een relevantiewaarde van 0-10. </p> <p>Als u bijvoorbeeld de relevantiewaarde voor de veldnaam "body" wilt instellen op 10, wordt de parameter als volgt weergegeven op het moment dat een klant een zoekopdracht uitvoert: </p> <p> <span class="codeph"> sp_ro=body:10 </span> </p> <p>U kunt ook een verticale scheidingsteken gebruiken om meerdere veldrelevantie-overschrijvingen in de parametertekenreeks op te geven. Als u bijvoorbeeld de relevantiewaarde voor de veldnamen "body" en "title" wilt instellen op 9, wordt de parameter als volgt weergegeven op het moment dat een klant een zoekopdracht uitvoert: </p> <p> <span class="codeph"> sp_ro=body:9|title:9 </span> </p> <p> <p>Opmerking:  Het opgeven van een veld dat niet is betrokken bij de bijbehorende zoekopdracht heeft geen effect. Als u bijvoorbeeld <span class="codeph"> sp_ro=title:10 instelt </span>, maar de naam van het <span class="codeph"> titelveld </span> niet wordt doorzocht, heeft de <span class="codeph"> sp_ro- </span> parameter geen effect. Met andere woorden, als u een veldnaam opgeeft met behulp van de <span class="codeph"> sp_ro- </span> parameter, wordt dat veld niet automatisch doorzocht. in plaats daarvan wordt alleen de bijbehorende relevantie-instelling van dat veld genegeerd. </p> </p> <p>Zie <a href="../c-about-settings-menu/c-about-metadata-menu.md#task_0A7657B63596421BB6DB3ED44F827AB3" type="task" format="dita" scope="local"> Vooraf gedefinieerde of door de gebruiker gedefinieerde metatag-tagvelden bewerken </a>. </p> <p>Zie <a href="../c-about-rules-menu/c-about-query-cleaning-rules.md#concept_17F3CDDC3C8A4128AF092A82B777B86C" type="concept" format="dita" scope="local"> Informatie over regels voor het opschonen van query's </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>38 </p> </td> 
   <td colname="col2"> <p>sp_s </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_s= number </span> </p> </td> 
   <td colname="col4"> <p>Hiermee geeft u de sorteervolgorde op. Nul (0) is het gebrek en middel om op relevantiescore te sorteren. Eén (1) betekent sorteren op datum en -1 betekent niet sorteren. </p> <p>U kunt een gebiedsnaam voor de waarde van de <span class="codeph"> sp_s </span> parameter specificeren. Zo sorteert <span class="codeph"> </span> sp_s=title de resultaten op basis van de waarden in het titelveld. Wanneer een veldnaam wordt gebruikt voor de waarde van een <span class="codeph"> sp_s- </span> parameter, worden de resultaten gesorteerd op dat veld en vervolgens gesubsorteerd op relevantie. </p> <p>Stel Sorteren voor het veld waarnaar wordt verwezen in op <span class="uicontrol"> Oplopend </span> of <span class="uicontrol"> Aflopend </span> in Instellingen <span class="uicontrol"> &gt; </span> Metagegevens <span class="uicontrol"> &gt; </span> Definities <span class="uicontrol"> </span> om deze functie in te schakelen. </p> <p>U kunt ook verschillende sorteervelden aan één query toewijzen door de parameter <span class="codeph"> </span> sp_s meerdere keren in te stellen in het zoekformulier. In de volgende sjabloonregels worden de zoekresultaten eerst gesorteerd op naam van de artiest, vervolgens op naam van album en vervolgens op naam van track. </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="artist"&gt; 
      &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="album"&gt; 
      &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="track"&gt; 
      Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="Music&nbsp;Search"&gt; </code> </p> <p>Het is ook mogelijk om op lijst aangepaste gebiedsgegevens te sorteren door een kwalificatiecode van de lijstnaam voorafgaand aan de gebiedsnaam, bijvoorbeeld, items.price te specificeren. Zie de <span class="codeph"> sp_field_table </span> parameter voor meer informatie over lijst aanpassing. </p> <p>Als u op nabijheid zoekt, kunt u de resultaten sorteren op nabijheid door een "nabijheidsuitvoerveld" op te geven. </p> <p>Zie <a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> Informatie over nabijheid zoeken </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>39 </p> </td> 
   <td colname="col2"> <p>sp_sr </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_sr= field </span> </p> </td> 
   <td colname="col4"> <p>Hiermee geeft u het rangtelveld op dat moet worden gebruikt voor statische waarderingen. Het veld moet een veld van het type Rank zijn met een relevantie groter dan 0. Als geen <span class="codeph"> sp_sr </span> parameter voor de vraag wordt verstrekt, wordt een gebied van type Rank automatisch geselecteerd. </p> <p>Om statische rangschikking voor een bepaalde vraag onbruikbaar te maken, omvat een ONGELDIGE waarde voor <span class="codeph"> sp_sr </span> (bijvoorbeeld, <span class="codeph"> &lt;input type="verborgen" name="sp_sr" value=""&gt; </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>40 </p> </td> 
   <td colname="col2"> <p>sp_sfvl_field </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_sfvl_field= string </span> </p> </td> 
   <td colname="col4"> <p>Hiermee geeft u de naam op van een veld dat moet worden gebruikt in combinatie met de tag <span class="codeph"> &lt;search-field-value-list&gt; </span> in de zoeksjabloon. </p> <p>U kunt veelvoudige <span class="codeph"> sp_sfvl_field </span> parameters specificeren. </p> </td> 
  </tr> 
  <tr>
   <td colname="col1"> <p>41 </p> </td> 
   <td colname="col2"> <p> sp_sfvl_df_count </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_sfvl_df_count= <span class="varname"> &lt;integer_value&gt; </span> </span> </p> </td> 
   <td colname="col4"> <p> Vraagt tot <span class="codeph"> &lt;integer_value&gt; <span class="varname"> </span></span> search-field-value-list dynamisch-facet velden <span class="codeph"> </span> voor deze zoekopdracht. </p> <p>De standaardwaarde is 0. De maximaal toegestane waarde is het huidige aantal dynamische-facetvelden, dynamic-facet-field-count dat voor een bepaalde index is gedefinieerd. Gehele waarden onder 0 worden behandeld als 0. De waarden voor het gehele getal die hierboven zijn opgegeven, <span class="codeph"> dynamic-facet-field-count, </span> worden beperkt tot het <span class="codeph"> dynamic-facet-field-count </span>. Niet-gehele waarden worden genegeerd; zij worden beschouwd als de standaardwaarde. </p> <p>De zoekopdracht van een segment is beperkt tot de maximaal toegestane <span class="codeph"> sp_sfvl_df_count- </span> waarde van de <span class="codeph"> dynamic-facet-field-count van dit segment </span> . Wanneer het samenvoegen van segmentresultaten, is de efficiënte maximumwaarde van <span class="codeph"> sp_sfvl_df_count de maximum daadwerkelijke </span> sp_sfvl_df_count over alle plakken <span class="codeph"> </span> . </p> <p>Zie Dynamische facetten <a href="../c-about-design-menu/c-about-dynamic-facets.md#task_D17F484130E448258100BAC1EEC53F39" format="dita" scope="local"> configureren </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>42 </p> </td> 
   <td colname="col2"> <p> sp_sfvl_df_exclude </p> </td> 
   <td colname="col03"> <p> </p> </td>
   <td colname="col3"> <p> </p> <p> <span class="codeph"> sp_sfvl_df_exclude= &lt; <span class="varname"> field_name </span>&gt;[|&lt; <span class="varname"> field_name </span> </span>&gt;|.. </p> </td> 
   <td colname="col4"> <p> Hiermee geeft u een lijst op met specifieke dynamische facetvelden die voor deze zoekopdracht buiten beschouwing moeten worden gelaten. </p> <p>Standaard worden alle dynamische facetvelden in aanmerking genomen. </p> <p>Zie Dynamische facetten <a href="../c-about-design-menu/c-about-dynamic-facets.md#task_D17F484130E448258100BAC1EEC53F39" format="dita" scope="local"> configureren </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>43 </p> </td> 
   <td colname="col2"> <p> sp_sfvl_df_include </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> </p> <p> <span class="codeph"> sp_sfvl_df_include= &lt; <span class="varname"> field_name </span>&gt;[|&lt; <span class="varname"> field_name </span> </span>&gt;|.. </p> </td> 
   <td colname="col4"> <p> Hiermee geeft u een lijst op met specifieke dynamische facetvelden die moeten worden opgenomen in de zoekresultaten. </p> <p> <p>Opmerking:  De <span class="codeph"> sp_sfvl_df_count </span> parameter bepaalt het totale aantal dynamische facetgebieden om terug te keren, met inbegrip van om het even welk gespecificeerd door middel van <span class="codeph"> sp_sfvl_df_include </span>. Dat wil zeggen, dat het gebruiken van <span class="codeph"> sp_sfvl_df_include </span> niet het totale aantal teruggekeerde dynamische facetgebieden toestaat om sp_sfvl_df_count te overschrijden <span class="codeph"> </span>. </p> </p> <p>Zie Dynamische facetten <a href="../c-about-design-menu/c-about-dynamic-facets.md#task_D17F484130E448258100BAC1EEC53F39" format="dita" scope="local"> configureren </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>44 </p> </td> 
   <td colname="col2"> <p>sp_getrapt </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_staged= 0 of 1 </span> </p> </td> 
   <td colname="col4"> <p>Als <span class="codeph"> sp_staged=1 met een vraag </span> wordt voorgelegd, is de vraag die in werking wordt gesteld een gefaseerde onderzoek. </p> <p>Een gefaseerde zoekopdracht gebruikt alle componenten die momenteel gefaseerd zijn, inclusief de index en sjablonen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>45 </p> </td> 
   <td colname="col2"> <p>sp_start_day, sp_start_month, sp_start_year </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_start_day= number </span> </p> <p> <span class="codeph"> sp_start_month= number </span> </p> <p> <span class="codeph"> sp_start_year= number </span> </p> </td> 
   <td colname="col4"> <p>Dit drievoudige van waarden specificeert de beginnende datumwaaier voor het onderzoek en u verstrekt het als reeks. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>46 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_suggestie _q </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_proposed_q= number </span> </p> </td> 
   <td colname="col4"> <p>De <span class="codeph"> sp_proposed_q </span> parameter bepaalt welke <span class="codeph"> sp_q[_#] </span> parameter met de dienst van de Samenvatting te gebruiken. </p> <p>De standaardwaarde van <span class="codeph"> sp_proposed_q </span> is 0, zo betekent het dat de onderzoeksmotor de waarde van <span class="codeph"> sp_q gebruikt </span> om de suggesties te bepalen. </p> <p>Plaats <span class="codeph"> sp_proposed_q=1 </span> om de waarde van <span class="codeph"> sp_q_1 </span> te gebruiken om de suggesties te bepalen, etc. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>47 </p> </td> 
   <td colname="col2"> <p>sp_t </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_t= string </span> </p> </td> 
   <td colname="col4"> <p>Specificeert het vervoermalplaatje aan gebruik. </p> <p>Deze parameter is handig als u de weergave van de belangrijkste zoekresultaten op uw website wilt bepalen door verschillende zoektransportsjablonen te gebruiken voor elk gebied in uw zoekaccount. </p> <p>Het standaardvervoermalplaatje is "onderzoek". </p> <p>Zie <a href="../c-appendices/c-templates.md#reference_12AAB3B9F4C74C11956F1DBA95714C2F" type="reference" format="dita" scope="local"> Meerdere transportsjablonen voor uw website beheren </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>48 </p> </td> 
   <td colname="col2"> <p>sp_trace </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_trace= 0 of 1 </span> </p> </td> 
   <td colname="col4"> <p>Wanneer geplaatst als <span class="codeph"> sp_stage=1 </span>, laat het kernonderzoekspoor vermogen in Simulator toe. </p> <p>Zie <a href="../c-about-simulator.md#concept_020AA6751E32421A96A3455508364C7E" format="dita" scope="local"> Informatie over Simulator </a>. </p> <p> <p>Opmerking:  Als deze parameter niet wordt gespecificeerd, verzamelt het kernonderzoek niet de het vinden informatie en de verwante markeringen van het kernonderzoekssjabloon hebben geen output. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>49 </p> </td> 
   <td colname="col2"> <p>sp_w, sp_w_control </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_w= <i>sound-alike-enable</i> </code> </p> <p> <code> sp_w_control=<i>sound-alike-control</i> </code> </p> </td> 
   <td colname="col4"> <p>Geeft op dat voor deze query overeenkomende geluiden moeten worden in- of uitgeschakeld. </p> <p>sp_w_control voor "Exact"wordt genegeerd. Overeenkomende geluiden worden uitgeschakeld. </p><p>De sp_w_control voor "als ` wordt genegeerd. Overeenkomende geluiden worden ingeschakeld</p><p>sp_w_control voor om het even wat anders is 1. Overeenkomende geluiden worden uitgeschakeld. </p><p>sp_w_control voor om het even wat anders is om het even wat. Overeenkomende geluiden worden ingeschakeld. </p>Met de <span class="codeph"> sp_w_control- </span> parameter kunt u een negatief of positief geformuleerd selectievakje voor eindgebruikercontrole van overeenkomsten op basis van geluid maken. </p> <p>Als <span class="codeph"> sp_w_control=0 </span> wordt gebruikt, dan wordt een negatief worded checkbox gebruikt om de <span class="codeph"> sp_w </span> parameter zoals in het volgende voorbeeld te plaatsen: </p> <p> <code class="syntax html"> &lt;input&nbsp;type=hidden&nbsp;name="sp_w_control"&nbsp;value="0"&gt;&lt;input&nbsp;type=checkbox&nbsp;name="sp_w"&nbsp;value="exact"&gt;No&nbsp;Sound-Alike&nbsp;matching </code> </p> <p>Als <span class="codeph"> sp_w_control=1 </span> wordt gebruikt, dan wordt een positief gewoordd checkbox gebruikt om de <span class="codeph"> sp_w </span> parameter zoals in het volgende te plaatsen: </p> <p> <code class="syntax html"> &lt;input&nbsp;type=hidden&nbsp;name="sp_w_control"&nbsp;value="1"&gt;&lt;input&nbsp;type=checkbox&nbsp;name="sp_w"&nbsp;value="alike"&gt;Sound-Alike&nbsp;matching </code> </p> <p>Zie de steekproef geavanceerde onderzoeksvorm voor meer voorbeelden bij het gebruiken van <span class="codeph"> sp_w_control </span> en <span class="codeph"> sp_w </span> parameters. </p> <p>Zie <a href="../c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A" type="reference" format="dita" scope="local"> Voorbeeld van een geavanceerd zoekformulier </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>50 </p> </td> 
   <td colname="col2"> <p>sp_x </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_x= field </span> </p> </td> 
   <td colname="col4"> <p>Hiermee geeft u de velden op die u wilt zoeken naar de queryreeks. alle middelen zoeken in alle velden. titel betekent alleen titelvelden zoeken. desc: alleen in documentbeschrijvingsvelden zoeken. sleutels betekent alleen zoeken in documenttrefwoorden. hoofdtekst: alleen tekst in de hoofdtekst zoeken. alt betekent alleen alternatieve tekst zoeken. url betekent dat alleen de URL-waarden worden doorzocht. doel: alleen doeltrefwoorden zoeken. In elk van deze gevallen worden de gebruikersspecificaties van de veldvoorvoegsels "text:", "desc:", "keys:", "body:", "alt:", "url:" en "target:" in de overeenkomstige <span class="codeph"> sp_q- </span> parameter genegeerd. Als <span class="codeph"> sp_x niet aanwezig </span> is of als het aan een leeg koord of om het even welk wordt geplaatst, dan worden de standaardvoorvoegsels van het gebruikersgebied toegestaan. Zie de beschrijving van Zoektips voor meer informatie over de voorvoegsels van velden. </p> <p>Zie <a href="../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8" type="concept" format="dita" scope="local"> Over zoekopdrachten </a>. </p> <p>Zie het voorbeeld Geavanceerde beschrijving van het Formulier van het Onderzoek voor voorbeelden gebruikend de <span class="codeph"> sp_x </span> parameter. </p> <p>Zie <a href="../c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A" type="reference" format="dita" scope="local"> Voorbeeld van een geavanceerd zoekformulier </a>. </p> <p>U kunt query's maken waarmee wordt gezocht in alle velden die zijn ingesteld op Standaard <span class="uicontrol"> zoeken </span> onder <span class="uicontrol"> Opties </span> &gt; <span class="uicontrol"> Metagegevens </span> &gt; <span class="uicontrol"> Definities </span> door sp_x=om het even welk in te stellen <span class="codeph"> </span>. Zowel pre als user-defined gebieden kunnen als waarde van de <span class="codeph"> sp_x </span> parameter worden gebruikt. </p> <p>U kunt verscheidene gebieden aan één enkele vraag ook toewijzen door de <span class="codeph"> sp_x </span> parameter verscheidene tijden te plaatsen. Met de volgende sjabloonregels kunnen gebruikers zowel de velden "title" als "auteur" opvragen voor "Great Books". </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x"&nbsp;value="title"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x"&nbsp;value="author"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="Great&nbsp;Books"&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>51 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_x_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_x_#= field-name </span> </p> </td> 
   <td colname="col4"> <p>Deze parameter specificeert welk gebied in de overeenkomstige <span class="codeph"> sp_q_# </span> vraag te zoeken. Het <span class="codeph"> # <span class="codeph"> </span> wordt vervangen door een getal tussen 1 en 16 (bijvoorbeeld </span> sp_x_8 <span class="codeph"> </span>). De veldnaam is een door de gebruiker gedefinieerd veld. </p> <p>Als geen <span class="codeph"> sp_x_# </span> parameter voor een bepaalde genummerde vraag wordt verstrekt, worden alle gebieden die als <span class="uicontrol"> Onderzoek door Gebrek worden bepaald </span> zoals die onder <span class="uicontrol"> het Plaatsen </span> &gt; <span class="uicontrol"> Meta-gegevens </span> &gt; <span class="uicontrol"> </span> Definities wordt geplaatst gezocht door die vraag. </p> <p>Als u bijvoorbeeld het volgende formulier verzendt, worden alle documenten geretourneerd die het woord "geweldig" bevatten en die ook het woord "Fitzgerald" in het veld "auteur" bevatten: </p> <p> <code class="syntax html"> Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="great"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="author"&gt;Search&nbsp;only&nbsp;documents&nbsp;written&nbsp;by:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="Fitzgerald"&gt; </code> </p> <p>U kunt veelvoudige gebiedsnamen met een bepaalde vraag of genummerde vraag associëren door meer dan één geval van de zelfde <span class="codeph"> sp_x </span> of <span class="codeph"> sp_x_# </span> parameter in één enkel onderzoeksverzoek te verstrekken. </p> <p>Als u bijvoorbeeld het woord "bloem" wilt zoeken in de velden "Hoofdtekst" en "Sleutels", kunt u een zoekformulier maken met de volgende informatie: </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="body"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="keys"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="flower"&gt; </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Een typisch voorbeeld van het gebruiken van backend onderzoekCGI parameters {#section_260012BBC2514CC9A8E02E53DE8B41EE}

De volgende verbindingsvragen beginnen een onderzoek gebruikend &quot;Muziek&quot;als onderzoeksvraag, en gebruikt alle standaardparameters. De URL wordt voor leesbaarheid over twee regels gesplitst. In uw HTML moet deze koppeling zich op één regel bevinden.

```
<a href="https://search.atomz.com/search/?sp_q=Music&sp_a=sp99999999"> 
Testing...</a>
```

Dezelfde functionaliteit wordt meestal gedefinieerd met een formulier:

```
<form action="https://search.atomz.com/search/"> 
<input size=12 name="sp_q" value="Music"><br> 
<input type=hidden name="sp_a" value="sp99999999"> 
<input type=submit value="Search"><br> 
</form>
```

Normaal gesproken moet u standaardparameters gebruiken wanneer u een zoekopdracht start. Op die manier wordt de eerste pagina weergegeven, gesorteerd op relevantie, en kan de klant andere pagina&#39;s en andere opties kiezen. Als het onderzoeksformulier op uw plaats opties voor inzamelingen omvat, ga in de inzamelingsnaam als parameter over.

## Een gedetailleerd voorbeeld van het gebruik van CGI-parameters voor backend-zoekopdrachten {#section_5FA3C620D5124FB2AB28857F8D8473F6}

De volgende formulierquery&#39;s geven `25` resultaten weer die beginnen bij het resultaat `10`. Samenvattingen worden niet weergegeven, de sorteervolgorde is op datum en de benoemde verzameling `support` wordt gebruikt. Alleen documenten die in de laatste 30 dagen zijn gedateerd, worden geretourneerd.

```
<form action="https://search.atomz.com/search/"> 
<input size=12 name="sp_q"><br> 
<input type=hidden name="sp_a" value="sp99999999"> 
<input type=submit value="Search"><br> 
<input type=hidden name=sp_n value=10> 
<input type=hidden name=sp_c value=25> 
<input type=hidden name=sp_m value=0> 
<input type=hidden name=sp_s value=1> 
<input type=hidden name=sp_k value="support"> 
<input type=hidden name=sp_date_range value=30> 
</form>
```

