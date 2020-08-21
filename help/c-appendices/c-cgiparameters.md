---
description: 'null'
seo-description: 'null'
seo-title: CGI-parameters
solution: Target
title: CGI-parameters
topic: Appendices,Site search and merchandising
uuid: a5f43547-bc15-44aa-ba23-6b8b573e09d2
translation-type: tm+mt
source-git-commit: 9271dce5ed49a2d5d629011c29b60cc33e715c5d
workflow-type: tm+mt
source-wordcount: '1934'
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
   <td colname="col3"> <p> <code>sp_a= string </code> </p> </td> 
   <td colname="col4"> <p>Specifies the account number string. Deze parameter is vereist en moet een geldige tekenreeks voor het accountnummer zijn. U kunt de tekenreeks voor uw accountnummer vinden via <span class="uicontrol"> Instellingen </span> &gt; <span class="uicontrol"> Accountopties </span> &gt; <span class="uicontrol"> Accountinstellingen </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>sp_advanced </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code>sp_advanced= 0 or 1 </code> </p> </td> 
   <td colname="col4"> <p>Als <code>sp_advanced=1 </code> een query wordt verzonden, wordt alle code tussen de <code>&lt;search-if-advanced&gt; </code> tag en de <code>&lt;/search-if-advanced&gt; </code> tag in de zoeksjabloon gebruikt voor het zoekformulier. Alle code tussen de <code>&lt;search-if-not-advanced&gt; </code> tag en de <code>&lt;/search-if-not-advanced&gt; </code> tag wordt genegeerd. Als <code>sp_advanced=0 </code> (of een andere waarde) wordt verzonden, wordt het sjabloonblok &lt;search-if-advanced&gt; genegeerd en wordt het sjabloonblok &lt;search-if-not-advanced&gt; gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>sp_c </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code>sp_c= number </code> </p> </td> 
   <td colname="col4"> <p>Hiermee geeft u het totale aantal resultaten op dat moet worden weergegeven. De standaardwaarde is 10. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>sp_context_field </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_context_field= <i>field</i> </code> </p> </td> 
   <td colname="col4"> <p>Verzamelt contextuele informatie voor het bepaalde gebied. De verzamelde informatie wordt output in de onderzoeksresultaten door de <code>&lt;search-context&gt; </code> malplaatjemarkering. De standaardwaarde is <code>body </code>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>5 </p> </td> 
   <td colname="col2"> <p>sp_d </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code>sp_d= type </code> </p> </td> 
   <td colname="col4"> <p>Hiermee wordt het type datumbereik opgegeven dat wordt gezocht. Mogelijke waarden voor type zijn om het even welk, wat betekent geen het onderzoeken van de datumwaaier uitvoert, die erop wijst dat de waarde van <code>sp_date_range </code> zou moeten worden gebruikt om de te zoeken data te bepalen, en specifiek, die erop wijst dat de waarden in <code>sp_start_day </code>, <code>sp_start_month </code>, <code>sp_start_year </code>, <code>sp_end_day </code>, <code>sp_end_month </code>en <code>sp_end_year </code> worden gebruikt om de datumwaaier te bepalen aan onderzoek. <code>sp_d </code> is alleen vereist als het zoekformulier de optie bevat om te zoeken in een aangepast bereik (als <code>sp_date_range </code>) of in een specifiek begin- en einddatumbereik. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p> sp_d_# </p> </td> 
   <td colname="col3"> <p> <code>sp_d_#= type </code> </p> </td> 
   <td colname="col4"> <p>Geeft het type datumbereik aan dat wordt gezocht voor de bijbehorende <code>sp_q_# </code> query. "#"wordt vervangen met een aantal tussen 1 en 16 (bijvoorbeeld, is van toepassing op de genummerde vraag <code>sp_d_8 </code><code>sp_q_8 </code>). </p> <p>U kunt op om het even welk plaatsen, wat betekent uitvoeren geen het zoeken van de datumwaaier, douane, die erop wijst dat de waarde van <code>type </code> wordt gebruikt om de te zoeken data te bepalen, en specifiek, die erop wijst dat de waarden in <code>sp_date_range_# </code> , <code>sp_q_min_day_# </code>, <code>sp_q_min_month_# </code>, <code>sp_q_min_year_# </code>, <code>sp_q_max_day_# </code><code>sp_q_max_month_# </code><code>sp_q_max_year_# </code> , en zouden moeten worden gebruikt om de datumwaaier te bepalen. Het gebruik van <code>sp_d_# </code> is alleen vereist als uw zoekformulier de optie bevat om te zoeken in een aangepast bereik (als <code>sp_date_range_# </code>) of in een specifiek begin- en einddatumbereik. </p> </td> 
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
   <td colname="col4"> <p>Geeft een vooraf gedefinieerd datumbereik op dat moet worden toegepast op de corresponderende <code>sp_q_# </code> query. "#"wordt vervangen met een aantal tussen 1 en 16 (bijvoorbeeld, is van toepassing op de genummerde vraag <code>sp_date_range_8 </code><code>sp_q_8 </code>). </p> <p>Waarden groter dan of gelijk aan nul geven het aantal dagen aan dat moet worden doorzocht vóór vandaag. De waarde 0 geeft vandaag bijvoorbeeld aan; de waarde 1 geeft vandaag en gisteren aan; een waarde van 30 specificeert binnen de laatste 30 dagen, etc. </p> <p>Waarden onder nul geven als volgt een aangepast bereik op: </p> <p>-1 = "Geen", gelijk aan het opgeven van geen datumbereik. </p> <p>-2 = "Deze week,"die van zondag tot Zaterdag van de huidige week zoekt. </p> <p>-3 = "Vorige week", waarmee wordt gezocht van zondag tot zaterdag van de week voorafgaand aan de huidige week. </p> <p>-4 = "Deze maand,"die data binnen de huidige maand zoekt. </p> <p>-5 = "Vorige maand,"die data binnen de maand voorafgaand aan de huidige maand zoekt. </p> <p>-6 = "Dit jaar,"dat data binnen het huidige jaar zoekt. </p> <p>-7 = "Vorig jaar", dat data zoekt in het jaar voorafgaand aan het lopende jaar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>9 </p> </td> 
   <td colname="col2"> <p>sp_dedupe_field </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_dedupe_field= <i>fieldname</i> </code> </p> </td> 
   <td colname="col4"> <p>Hiermee geeft u één veld op waarin de zoekresultaten moeten worden gededupliceerd. Alle dubbele resultaten in dat veld worden verwijderd uit de zoekresultaten. Als bijvoorbeeld <code>sp_dedupe_field=title </code>alleen het bovenste resultaat voor een bepaalde titel wordt weergegeven in de zoekresultaten (er worden geen twee resultaten weergegeven met dezelfde inhoud van het titelveld). Voor tekstvelden met meerdere waarden (lijst van gewenste personen) wordt de volledige inhoud van het veld gebruikt voor de vergelijking. Er kan slechts één veld worden opgegeven. Een 'table-Qualifier' is niet toegestaan in de veldnaam. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>10 </p> </td> 
   <td colname="col2"> <p>sp_e </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code>sp_e= number </code> </p> </td> 
   <td colname="col4"> <p>Geeft aan dat jokertekens automatisch moeten worden uitgebreid voor elk woord uit de queryreeks met meer dan getaltekens. Met andere woorden, <code>sp_e=5 </code> geeft u op dat woorden met 5 of meer tekens, zoals "query" of "number", moeten worden uitgevouwen met het jokerteken '*', waardoor de zoekopdracht equivalent wordt aan een zoekopdracht naar "query*" of "number*". Woorden met minder tekens worden niet uitgevouwen, dus een zoekopdracht naar "woord" heeft geen automatische uitbreiding van jokertekens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>11 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p> sp_e_# </p> </td> 
   <td colname="col3"> <p> <code>sp_e_#= number </code> </p> </td> 
   <td colname="col4"> <p>Geeft aan dat jokertekens automatisch worden uitgebreid voor elk woord uit de bijbehorende <code>sp_q_# </code> queryreeks met meer dan getaltekens. Met andere woorden, <code>sp_e_2=5 </code> geeft u op dat woorden met vijf of meer tekens in de <code>sp_q_2 </code> queryreeks, zoals "query" of "number", moeten worden uitgevouwen met het jokerteken ' <code>* </code>', waardoor de zoekopdracht gelijk wordt aan een zoekopdracht naar "query*" of "number*". Woorden met minder tekens worden niet uitgevouwen, dus een zoekopdracht naar "woord" in <code>sp_q_2 </code> zou geen automatische uitbreiding van jokertekens hebben. </p> </td> 
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
   <td colname="col3"> <p> <code>sp_f= string </code> </p> </td> 
   <td colname="col4"> <p>Geeft de tekenset van de parametertekenreeksen voor query's op (zoals <code>sp_q </code>). Deze tekenreeks moet altijd overeenkomen met de tekenset van de pagina die het zoekformulier bevat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>14 </p> </td> 
   <td colname="col2"> <p>sp_field_table </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_field_ table=table: field,field... </code> </p> </td> 
   <td colname="col4"> <p>Definieert een logische gegevenstabel die uit de opgegeven velden bestaat. Een tabel met de naam "items", bestaande uit de velden "kleur", "grootte" en "prijs", wordt bijvoorbeeld als volgt gedefinieerd: </p> <p> <code>sp_field_table=items:color,size,price </code> </p> <p>Logische tabellen zijn vooral handig in combinatie met velden waarvoor "Lijsten van gewenste personen" zijn ingeschakeld (onder <span class="uicontrol"> Instellingen </span> &gt; <span class="uicontrol"> Metagegevens </span> &gt; <span class="uicontrol"> Definities </span>). Alle CGI-parameters en sjabloontags die een veldnaam als een waarde hebben, kunnen optioneel een tabelnaam opgeven gevolgd door een "". vóór de veldnaam (bijvoorbeeld <code>sp_x_1=tablename.fieldname </code>). </p> <p>Als u bijvoorbeeld wilt zoeken naar documenten die een of meer "rode" items in grootte "groot" bevatten (items worden weergegeven als parallelle rijen met metagegevens), kunt u het volgende gebruiken: </p> <p> <code> sp_q_exact_1=red&amp;sp_x_1=items.color&amp; sp_q_exact_2=large&amp;sp_x_2=items.size&amp;sp_field_table=items:color,size,price </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>15 </p> </td> 
   <td colname="col2"> sp_i </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> </p></td><td colname="col4"><p></p><p></p><p><code>sp_i=1 </code><code>sp_i=2 </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_k= string </code></p></td><td colname="col4"><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_l= string </code></p></td><td colname="col4"><p><code>sp_q </code><code>string </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_literal= 0 or 1 </code></p></td><td colname="col4"><p><code>sp_literal=1 </code></p><p><code>sp_literal=0 </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_m= number </code></p></td><td colname="col4"><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_n= number </code></p></td><td colname="col4"><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_not_found_page= url </code></p></td><td colname="col4"><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_p= any/all/phrase </code></p></td><td colname="col4"><p><code>any </code><code>all </code><code>phrase </code></p><p><code>phrase </code><code>all </code><code>sp_p </code></p><p></p><p></p><p><code>sp_p </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_p_#= any/all/phrase </code></p></td><td colname="col4"><p><code>sp_q_# </code><code>sp_p_8 </code><code>sp_q_8 </code><code>any </code><code>all </code><code>phrase </code></p><p><code>all </code><code>phrase </code><code>sp_p_# </code><code>any </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code> sp_pt= <i>exact/equivalent/compatible</i> </code></p></td><td colname="col4"><p><code>exact </code><code>equivalent </code><code>compatible </code><code>sp_p </code><code>exact </code><code>sp_p </code><code>all </code><code>phrase </code><code>equivalent </code><code>sp_pt </code><code>compatible </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code> sp_pt_#= <i>exact/equivalent/compatible</i> </code></p></td><td colname="col4"><p><code>sp_q_# </code><code>sp_p_8 </code><code>sp_q_8 </code><code>exact </code><code>equivalent </code><code>exact </code><code>compatible </code><code>sp_p_# </code><code>exact </code><code>sp_p_# </code><code>equivalent </code><code>sp_pt_# </code><code>compatible </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_q= string </code></p></td><td colname="col4"><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_q_#= text </code></p></td><td colname="col4"><p><code>sp_q_# </code><code>sp_q_1 </code><code>sp_q_16 </code></p><p></p><p><code class="syntax html"> Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="great"&gt; 
      Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="books"&gt; </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_q_day= integer value </code></p><p><code>sp_q_month= integer value </code></p><p><code>sp_q_year= integer value </code></p><p><code>sp_q_day_#= integer value </code></p><p><code>sp_q_month_#= integer value </code></p><p><code>sp_q_year_#= integer value </code></p></td><td colname="col4"><p><code>sp_q_day </code><code>sp_q_month </code><code>sp_q_year </code><code>sp_q </code></p><p><code># </code><code>sp_q_day_6 </code><code>sp_q_6 </code></p><p><code>PublishDate </code></p><p><code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="PublishDate"&gt; Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="orange"&gt;On&nbsp;:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_day_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Day&lt;input&nbsp;type="text"&nbsp;name="sp_q_month_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Month &lt;input&nbsp;type="text"&nbsp;name="sp_q_year_1"&nbsp;size="4"&nbsp;value="2000"&gt;&nbsp;Year&nbsp; </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code> sp_q_location=<i>latitude/longitude</i> OR <i>areacode</i> OR <i>zipcode</i> </code></p><p><code> sp_q_location_#= <i>latitude/longitude</i> OR <i>areacode</i> OR <i>zipcode</i> </code></p></td><td colname="col4"><p><code>sp_q_location </code><code>sp_q_location_# </code><code># </code></p><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code> sp_q_max_relevant_distance= <i>value</i> </code></p><p><code> sp_q_max_relevant_distance_#= <i>value</i> </code></p></td><td colname="col4"><p><code>sp_q_max_relevant_distance </code><code>sp_q_max_relevant_distance_# </code><code># </code></p><p><code>sp_q_max_relevant_distance </code></p><p><code>sp_q_max_relevant_distance_# </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p><p></p></td><td colname="col03"><p></p><p></p></td><td colname="col3"><p><code> sp_q_min_day=<i>integer value</i> </code></p><p><code> sp_q_min_month=<i>integer value</i> </code></p><p><code> sp_q_min_year=<i>integer value</i> </code></p><p><code> sp_q_max_day=<i>integer value</i> </code></p><p><code> sp_q_max_month=<i>integer value</i> </code></p><p><code> sp_q_max_year=<i>integer value</i> </code></p><p><code> sp_q_min_day_#=<i>integer value</i> </code></p><p><code> sp_q_min_month_#=<i>integer value</i> </code></p><p><code> sp_q_min_year_#=<i>integer value</i> </code></p><p><code> sp_q_max_day_#=<i>integer value</i> </code></p><p><code> sp_q_max_month_#=<i>integer value</i> </code></p><p><code> sp_q_max_year_#=<i>integer value</i> </code></p></td><td colname="col4"><p><code>sp_q_min_day </code><code>sp_q_min_month </code><code>sp_q_min_year </code><code>sp_q_max_day </code><code>sp_q_max_month </code><code>sp_q </code></p><p><code># </code><code>sp_q_min_day_6 </code><code>sp_q_6 </code></p><p></p><p><code>PublishDate </code></p><p><code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="PublishDate"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="orange"&gt;Between:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_min_day_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Start&nbsp;Day&lt;input&nbsp;type="text"&nbsp;name="sp_q_min_month_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Start&nbsp;Month 
      &lt;input&nbsp;type="text"&nbsp;name="sp_q_min_year_1"&nbsp;size="4"&nbsp;value="2000"&gt;&nbsp;Start&nbsp;Year 
      And:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_max_day_1"&nbsp;size="2"&nbsp;value="31"&gt;&nbsp;End&nbsp;Day 
      &lt;input&nbsp;type="text"&nbsp;name="sp_q_max_month_1"&nbsp;size="2"&nbsp;value="12"&gt;&nbsp;End&nbsp;Month 
      &lt;input&nbsp;type="text"&nbsp;name="sp_q_max_year_1"&nbsp;size="4"&nbsp;value="2000"&gt;&nbsp;End&nbsp;Year </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_q_min= value </code></p><p><code>sp_q_max= value </code></p><p><code>sp_q_min_#= value </code></p><p><code>sp_q_max_#= value </code></p><p><code>sp_q_exact_#=value </code></p></td><td colname="col4"><p><code>sp_q_min </code><code>sp_q_max </code><code>sp_q_exact </code><code>sp_q </code></p><p><code># </code><code>sp_q_min_8 </code><code>sp_q_8 </code></p><p><code>sp_q_exact_# </code><code>sp_q_min_# </code><code>sp_q_max_# </code><code>sp_q_exact_# </code><code>sp_q_min_# </code><code>sp_q_max_# </code></p><p><code>sp_q_min_# </code><code>sp_q_max_# </code><code>sp_q_exact_# </code><code>...&amp;sp_q_exact_1=green|red&amp;sp_x_1=color </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_q_nocp= 1 or 0 </code></p><p><code>sp_q_nocp_#= 1 or 0 </code></p></td><td colname="col4"><p><code>0 </code></p><p><code>1 </code></p><p><code>sp_q_nocp </code><code>sp_q </code><code># </code><code>sp_q_nocp_8 </code><code>sp_q_8 </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_q_required= 1 or 0 or -1 </code></p><p><code>sp_q_required_#= 1 or 0 or -1 </code></p></td><td colname="col4"><p></p><p><code>sp_q_required </code><code>sp_q </code></p><p><code># </code><code>sp_q_required_8 </code><code>sp_q_8 </code></p><p></p><p><code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="platform"&gt; 
      Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="calc"&gt; 
      Exclude:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="mac&nbsp;win&nbsp;all"&gt; 
      &lt;input&nbsp;type="hidden"&nbsp;name="sp_q_required_1"&nbsp;value="-1"&gt; </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code> sp_redirect_ 
      if_one_result= <i>0 or 1</i> </code></p></td><td colname="col4"><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_referrer= url </code></p></td><td colname="col4"><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p></p></td><td colname="col4"><p><code>ro </code></p><p></p><p><code>sp_ro=body:10 </code></p><p></p><p><code>sp_ro=body:9|title:9 </code></p><p><p><code>sp_ro=title:10 </code><code>title </code><code>sp_ro </code><code>sp_ro </code></p></p><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_s= number </code></p></td><td colname="col4"><p></p><p><code>sp_s </code><code>sp_s=title </code><code>sp_s </code></p><p></p><p><code>sp_s </code></p><p><code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="artist"&gt; 
      &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="album"&gt; 
      &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="track"&gt; 
      Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="Music&nbsp;Search"&gt; </code></p><p><code>sp_field_table </code></p><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_sr= field </code></p></td><td colname="col4"><p><code>sp_sr </code></p><p><code>sp_sr </code><code>&lt;input type="hidden" name="sp_sr" value=""&gt; </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_sfvl_field= string </code></p></td><td colname="col4"><p><code>&lt;search-field-value-list&gt; </code></p><p><code>sp_sfvl_field </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p></p></td><td colname="col4"><p><code>search-field-value-list </code></p><p><code>dynamic-facet-field-count </code><code>dynamic-facet-field-count </code></p><p><code>sp_sfvl_df_count </code><code>dynamic-facet-field-count </code><code>sp_sfvl_df_count </code><code>sp_sfvl_df_count </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p></p><p></p></td><td colname="col4"><p></p><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p></p><p></p></td><td colname="col4"><p></p><p><p><code>sp_sfvl_df_count </code><code>sp_sfvl_df_include </code><code>sp_sfvl_df_include </code><code>sp_sfvl_df_count </code></p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_staged= 0 or 1 </code></p></td><td colname="col4"><p><code>sp_staged=1 </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_start_day= number </code></p><p><code>sp_start_month= number </code></p><p><code>sp_start_year= number </code></p></td><td colname="col4"><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_suggest_q= number </code></p></td><td colname="col4"><p><code>sp_suggest_q </code><code>sp_q[_#] </code></p><p><code>sp_suggest_q </code><code>sp_q </code></p><p><code>sp_suggest_q=1 </code><code>sp_q_1 </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_t= string </code></p></td><td colname="col4"><p></p><p></p><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_trace= 0 or 1 </code></p></td><td colname="col4"><p><code>sp_stage=1 </code></p><p></p><p><p></p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code> sp_w= <i>sound-alike-enable</i> </code></p><p><code> sp_w_control=<i>sound-alike-control</i> </code></p></td><td colname="col4"><p></p><p></p><p></p><p></p><p></p><code>sp_w_control </code></p><p><code>sp_w_control=0 </code><code>sp_w </code></p><p><code class="syntax html"> &lt;input&nbsp;type=hidden&nbsp;name="sp_w_control"&nbsp;value="0"&gt;&lt;input&nbsp;type=checkbox&nbsp;name="sp_w"&nbsp;value="exact"&gt;No&nbsp;Sound-Alike&nbsp;matching </code></p><p><code>sp_w_control=1 </code><code>sp_w </code></p><p><code class="syntax html"> &lt;input&nbsp;type=hidden&nbsp;name="sp_w_control"&nbsp;value="1"&gt;&lt;input&nbsp;type=checkbox&nbsp;name="sp_w"&nbsp;value="alike"&gt;Sound-Alike&nbsp;matching </code></p><p><code>sp_w_control </code><code>sp_w </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_x= field </code></p></td><td colname="col4"><p><code>sp_q </code><code>sp_x </code></p><p></p><p><code>sp_x </code></p><p></p><p><code>sp_x=any </code><code>sp_x </code></p><p><code>sp_x </code></p><p><code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x"&nbsp;value="title"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x"&nbsp;value="author"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="Great&nbsp;Books"&gt; </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_x_#= field-name </code></p></td><td colname="col4"><p><code>sp_q_# </code><code> # </code><code>sp_x_8 </code></p><p><code>sp_x_# </code></p><p></p><p><code class="syntax html"> Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="great"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="author"&gt;Search&nbsp;only&nbsp;documents&nbsp;written&nbsp;by:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="Fitzgerald"&gt; </code></p><p><code>sp_x </code><code>sp_x_# </code></p><p></p><p><code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="body"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="keys"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="flower"&gt; </code></p></td></tr></tbody></table>

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

