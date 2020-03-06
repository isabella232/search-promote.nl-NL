---
description: ongeldig
seo-description: ongeldig
seo-title: CGI-parameters
solution: Target
title: CGI-parameters
topic: Appendices,Site search and merchandising
uuid: a5f43547-bc15-44aa-ba23-6b8b573e09d2
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a

---


# CGI-parameters{#cgi-parameters}

## CGI-parameters {#concept_F395999090FE4926B38BC73D5E612800}

## CGI-parameters zoeken {#reference_DA27A8B0728246DA94994885E1353890}

De de vormcode van het onderzoek wordt verstrekt dat u in HTML van uw plaats ( **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Form Source]**) kunt kopiëren en kleven.

Zie de HTML-code van het zoekformulier [kopiëren in...](../c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

U kunt de parameters ook plaatsen die of in de onderzoeksvorm zelf, of van een manuscript vermeld zijn. Naast de parameters die hieronder worden vermeld kunt u de parameters van het achterste deelonderzoek ook gebruiken om onderzoek te controleren.

Zie de parameters [van het onderzoek van het](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)Achterste CGI.

De verzoeken van het onderzoek bestaan uit een basis URL. De basis URL wijst op welke rekening de klant zoekt, en een reeks parameters van CGI (zeer belangrijk-waardeparen) die erop wijzen hoe te om de gewenste onderzoeksresultaten voor de bijbehorende rekening terug te keren.

De basis URL wordt geassocieerd met een specifieke rekening en een gefaseerd of levend milieu. U kunt veelvoudige aliassen voor de basis URL van uw rekeningsmanager verzoeken. Bijvoorbeeld, kan een bedrijf genoemd Megacorp twee basisURLs verbonden aan hun rekening hebben: `https://search.megacorp.com` en `https://stage.megacorp.com`. De vroegere URL zoekt hun levende index en laatstgenoemde URL zoekt hun gefaseerde index.

Drie formaten van de Parameters van CGI worden gesteund. Door gebrek wordt uw rekening gevormd om de Parameters van CGI met een puntkomma te scheiden zoals in het volgende voorbeeld:

`https://search.megacorp.com?q=shoes;page=2`

Als u verkiest, kunt u uw rekeningsmanager hebben uw rekening vormen om ampersands te gebruiken om de parameters van CGI zoals in het volgende voorbeeld te scheiden:

`https://search.megacorp.com?q=shoes&page=2`

Een derde formaat, genoemd het formaat SEO, wordt ook gesteund waar een voorwaartse schuine streep in plaats van de separator en het gelijke teken zoals in het volgende voorbeeld `/` wordt gebruikt:

`https://search.megacorp.com/q/shoes/page/2`

Om het even welke tijd wordt het formaat SEO gebruikt om een verzoek te verzenden, zijn alle outputverbindingen teruggekeerd in het zelfde formaat.

| Begeleide zoekparameter | Voorbeeld | Beschrijving |
|--- |--- |--- |
| q | `q=string` | Specificeert het vraagkoord voor het onderzoek. Deze parameter brengt aan de `sp_q` achterste onderzoeksparameter in kaart.  Zie de parameters [van het onderzoek van het](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)Achterste CGI. |
| q# | `q#=string` | De factor (het zoeken binnen een bepaald gebied) wordt gedaan als genummerde q en x parameters.  De parameter q bepaalt de termijn u naar in het facet zoekt zoals die door de overeenkomstige genummerde x parameter wordt aangeduid.<br>Bijvoorbeeld, als u twee facetten hebt die grootte en kleur worden genoemd, kunt u iets als q1=small hebben;x1=size;q2=red;x2=color.  Deze parameter brengt aan de parameters van het `sp_q_exact_#` achterste deelonderzoek in kaart.  <br>Zie de parameters [van het onderzoek van het](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)Achterste CGI. |
| x# | `q#=string` | De factor (het zoeken binnen een bepaald gebied) wordt gedaan als genummerde q en x parameters.  De parameter q bepaalt de termijn u naar in het facet zoekt zoals die door de overeenkomstige genummerde x parameter wordt aangeduid. <br>Bijvoorbeeld, als u twee facetten hebt die grootte en kleur worden genoemd, kunt u iets als q1=small hebben;x1=size;q2=red;x2=color.  Deze parameter brengt aan de parameters van het `sp_x_#` achterste deelonderzoek in kaart.  <br>Zie de parameters [van het onderzoek van het](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)Achterste CGI. |
| collectie | `collection=string` | Specificeert de inzameling voor het onderzoek te gebruiken.  Deze parameter brengt aan de `sp_k` achterste onderzoeksparameter in kaart.  Zie de parameters [van het onderzoek van het](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)Achterste CGI. |
| tellen | `count=number` | Specificeert de totale telling van resultaten die worden getoond.  Het gebrek wordt bepaald in [!UICONTROL Settings ] > [!UICONTROL Searching ] > [!UICONTROL Searches ]. .  Deze parameter brengt aan de `sp_c` achterste onderzoeksparameter in kaart.  Zie de parameters [van het onderzoek van het](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)Achterste CGI. |
| pagina | `page=number` | Specificeert de pagina van resultaten die zijn teruggekeerd. |
| rangschikken | `rank=field` | Specificeert het rangschikkingsgebied voor het statische rangschikken te gebruiken.  Het veld moet een veld van het type Rank zijn met een relevantie groter dan 0.  Deze parameter brengt aan de `sp_sr` achterste deelparameter in kaart.  Zie de parameters [van het onderzoek van het](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)Achterste CGI. |
| sorteren | `sort=number` | Specificeert de soortorde.<br>&quot;0&quot; is de standaardwaarde en is de soort volgens relevantiescore; &quot;1&quot; sorteert naar datum; &quot;-1&quot; sorteert niet.  De gebruikers kunnen een gebiedsnaam voor de waarde van de `sp_s` parameter specificeren.  Bijvoorbeeld, `sp_s=title` sorteert resultaten volgens de waarden die in het titelgebied bevat zijn. Wanneer een veldnaam wordt gebruikt voor de waarde van een ` sp_s ` parameter, worden de resultaten gesorteerd door dat gebied en dan gesubsorteerd door relevantie.  Om deze eigenschap toe te laten, klik [!UICONTROL Settings ] > [!UICONTROL Metadata ] > [!UICONTROL Definitions ]. Voor de pagina van Definities, klik [!UICONTROL Add New Field ] of klik [!UICONTROL Edit ] voor een bepaalde gebiedsnaam. In de [!UICONTROL Sorting ] drop-down lijst, selecteer of [!UICONTROL Ascending ] of [!UICONTROL Descending ]. Deze parameter brengt aan de `sp_s` achterste onderzoeksparameter in kaart. <br>Zie de parameters [van het onderzoek van het]Achterste CGI.(../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8). |

## Backend onderzoek CGI parameters {#reference_582E85C3886740C98FE88CA9DF7918E8}

Typisch staan de klanten met een presentatielaag in wisselwerking genoemd Geleid Onderzoek. Nochtans, is het theoretisch mogelijk om de Geleide laag van het Onderzoek over te slaan en met het onderzoek van de achterste deelkern direct in wisselwerking te staan gebruikend de parameters van CGI die op deze pagina worden beschreven.

U kunt de parameters van het achterste deelonderzoekCGI van de volgende lijst selecteren:
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
   <td colname="col4"> <p>Specificeert het koord van het rekeningsaantal. Deze parameter wordt vereist, en moet een geldig koord van het rekeningsaantal zijn. U kunt uw koord van het rekeningsaantal onder <span class="uicontrol"> Montages </span> &gt; <span class="uicontrol"> de Opties van de Rekening </span> &gt; <span class="uicontrol"> de Montages van de Rekening vinden </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>sp_advanced </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_advanced= 0 of 1 </span> </p> </td> 
   <td colname="col4"> <p>Als <span class="codeph"> sp_advanced=1 met een vraag </span> wordt voorgelegd, dan wordt al code tussen de <span class="codeph"> &lt;search-if-advanced&gt; </span> markering en de <span class="codeph"> &lt;/search-if-advanced&gt; </span> markering in het onderzoeksmalplaatje gebruikt voor de onderzoeksvorm. Alle code tussen de <span class="codeph"> &lt;search-if-not-advanced&gt; </span> tag en de <span class="codeph"> &lt;/search-if-not-advanced&gt; </span> tag wordt genegeerd. Als <span class="codeph"> sp_advanced=0 </span> (of een andere waarde) wordt voorgelegd, dan wordt het &lt;search-if-advanced&gt; malplaatjeblok genegeerd en &lt;search-if-not-advanced&gt; malplaatjeblok wordt gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>sp_c </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_c= aantal </span> </p> </td> 
   <td colname="col4"> <p>Specificeert de totale telling van te tonen resultaten. Het gebrek is 10. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>sp_context_field </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_context_field= <i>field</i> </code> </p> </td> 
   <td colname="col4"> <p>Verzamelt contextuele informatie voor het bepaalde gebied. De verzamelde informatie is output in de onderzoeksresultaten als <span class="codeph"> &lt;search-context&gt; </span> malplaatjemarkering. De standaardwaarde is <span class="codeph"> lichaam </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>5 </p> </td> 
   <td colname="col2"> <p>sp_d </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_d= type </span> </p> </td> 
   <td colname="col4"> <p>Specificeert het type van datumwaaier die om zoekt uit te voeren. Mogelijke waarden voor type zijn om het even welk, zo betekent uitgevoerd geen datumwaaier het zoeken, douane, die erop wijst dat de waarde van <span class="codeph"> sp_date_range </span> zou moeten worden gebruikt om de data te bepalen aan onderzoek, en specifiek, dat erop wijst dat de waarden in <span class="codeph"> sp_start_day </span>, <span class="codeph"> _start_maand </span>, <span class="codeph"> sp_start_year </span>, <span class="codeph"> sp_end_day, </span><span class="codeph"> </span><span class="codeph"> </span> _end_month, en het jaar wordt gebruikt om de datumwaaier aan onderzoek te bepalen. <span class="codeph"> sp_d </span> wordt slechts vereist als uw onderzoeksvorm de optie aan onderzoek of door een douanewaaier (als <span class="codeph"> sp_date_range </span>) bevat, of door een specifieke begin en einddatumwaaier bevat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p> sp_d_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_d_#= type </span> </p> </td> 
   <td colname="col4"> <p>Specificeert het type van datumwaaier die naar de overeenkomstige vraag <span class="codeph"> sp_q_# zoekt uit te voeren </span> . "#"wordt vervangen met een aantal tussen 1 en 16 (bijvoorbeeld, <span class="codeph"> sp_d_8 </span>, is op de genummerde vraag <span class="codeph"> sp_q_8 van toepassing </span>). </p> <p>U kunt type <span class="codeph"> aan om het even welk plaatsen, wat betekent geen datumwaaier het zoeken uitvoert, douane, die erop wijst dat de waarde van </span> sp_date_range_# <span class="codeph"> wordt gebruikt om de data aan onderzoek te bepalen, en specifiek, die erop wijst dat de waarden in </span> sp_q_min_day_# <span class="codeph"> , </span>sp_min_maand_# <span class="codeph"> , </span>sp_q_min_year_#, <span class="codeph"> </span><span class="codeph"> </span><span class="codeph"> </span><span class="codeph"> </span> _q_max_dag_sp_q_max_month_#, sp_q_max_year_# zou moeten worden gebruikt om de datumwaaier te bepalen. Het gebruik van <span class="codeph"> sp_d_# </span> wordt slechts vereist als uw onderzoeksvorm de optie aan onderzoek of door een douanewaaier (als <span class="codeph"> sp_date_range_# </span>) bevat, of door een specifieke begin en einddatumwaaier bevat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>7 </p> </td> 
   <td colname="col2"> <p>sp_date_range </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_date_range= <i>number</i> </code> </p> </td> 
   <td colname="col4"> <p>Specificeert een vooraf bepaalde datumwaaier om op het onderzoek van toepassing te zijn. De waarden groter dan of gelijk aan nul specificeren het aantal dagen aan onderzoek voorafgaand aan vandaag — bijvoorbeeld, specificeert een waarde van "0"vandaag,"een waarde van "1"specificeert "vandaag en gisteren,"een waarde van "30"specificeert "binnen de laatste 30 dagen,"etc. </p> <p>De waarden onder nul specificeren als volgt een douanewaaier: </p> <p>-1 = "niets,"het zelfde als specificerend geen datumwaaier. </p> <p>-2 = "Deze week,"die onderzoeken van Zondag aan Zaterdag van de huidige week. </p> <p>-3 = "Vorige week,"die onderzoeken van Zondag aan Zaterdag van de week voorafgaand aan de huidige week. </p> <p>-4 = "Deze maand,"die data binnen de huidige maand zoekt. </p> <p>-5 = "Vorige maand,"die data binnen de maand voorafgaand aan de huidige maand zoekt. </p> <p>-6 = "Dit jaar,"die onderzoeken data binnen het lopende jaar. </p> <p>-7 = "Vorig jaar,"dat data zoekt binnen het jaar voorafgaand aan het huidige jaar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>8 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_date_range_# </p> </td> 
   <td colname="col3"> <p> <code> sp_date_range_#= <i>number</i> </code> </p> </td> 
   <td colname="col4"> <p>Specificeert een vooraf bepaalde datumwaaier om op de overeenkomstige <span class="codeph"> sp_q_# </span> vraag van toepassing te zijn. "#"wordt vervangen met een aantal tussen 1 en 16 (bijvoorbeeld, <span class="codeph"> sp_date_range_8, is op de genummerde vraag </span>sp_q_8 van toepassing <span class="codeph"> </span>). </p> <p>De waarden groter dan of gelijk aan nul specificeren het aantal dagen aan onderzoek voorafgaand aan vandaag. Bijvoorbeeld, specificeert een waarde van 0 vandaag; een waarde van 1 specificeert vandaag en gisteren; een waarde van 30 specificeert binnen de laatste 30 dagen, etc. </p> <p>De waarden onder nul specificeren als volgt een douanewaaier: </p> <p>-1 = "niets,"het zelfde als specificerend geen datumwaaier. </p> <p>-2 = "Deze week,"die onderzoeken van Zondag aan Zaterdag van de huidige week. </p> <p>-3 = "Vorige week,"die onderzoeken van Zondag aan Zaterdag van de week voorafgaand aan de huidige week. </p> <p>-4 = "Deze maand,"die data binnen de huidige maand zoekt. </p> <p>-5 = "Vorige maand,"die data binnen de maand voorafgaand aan de huidige maand zoekt. </p> <p>-6 = "Dit jaar,"die onderzoeken data binnen het lopende jaar. </p> <p>-7 = "Vorig jaar,"dat data zoekt binnen het jaar voorafgaand aan het huidige jaar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>9 </p> </td> 
   <td colname="col2"> <p>sp_dedupe_field </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_dedupe_field= <i>fieldname</i> </code> </p> </td> 
   <td colname="col4"> <p>Specificeert één enkel gebied om onderzoeksresultaten te dedupliceren op. Alle dubbele resultaten op dat gebied worden verwijderd uit de onderzoeksresultaten. Bijvoorbeeld, als voor <span class="codeph"> sp_dedupe_field=title </span>, slechts het hoogste resultaat voor een bepaalde titel in de onderzoeksresultaten wordt getoond (geen twee resultaten zullen identieke inhoud van het titelgebied hebben). Voor multi-value (sta lijst toe) typevelden, wordt de volledige gebiedsinhoud gebruikt voor vergelijking. Er kan slechts één veld worden opgegeven. Een "lijst-bepalend"wordt niet toegestaan in de gebiedsnaam. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>10 </p> </td> 
   <td colname="col2"> <p>sp_e </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_e= aantal </span> </p> </td> 
   <td colname="col4"> <p>Specificeert dat de automatische vervangingsuitbreiding voor om het even welk woord van het vraagkoord met meer dan aantalkarakters zou moeten plaatsvinden. Met andere woorden, <span class="codeph"> sp_e=5 </span> specificeert dat de woorden met 5 of meer karakters, zoals "vraag"of "aantal", met het vervangingskarakter "*"zouden moeten worden uitgebreid, makend het onderzoek gelijkwaardig aan een onderzoek naar "query*"of "number*". Woorden met minder karakters worden niet uitgebreid, zodat zou een onderzoek naar "woord"geen automatische vervangingsuitbreiding hebben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>11 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p> sp_e_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_e_#= aantal </span> </p> </td> 
   <td colname="col4"> <p>Specificeert dat de automatische vervangingsuitbreiding voor om het even welk woord van het overeenkomstige <span class="codeph"> sp_q_# </span> vraagkoord met meer dan aantalkarakters plaatsvindt. Met andere woorden, <span class="codeph"> sp_e_2=5 </span> specificeert dat de woorden met vijf of meer karakters in het <span class="codeph"> sp_q_2 </span> vraagkoord, zoals "vraag"of "aantal", met het vervangingskarakter " * <span class="codeph"> </span>"zouden moeten worden uitgebreid, makend het onderzoek gelijkwaardig aan een onderzoek naar "query*"of "number*". Woorden met minder karakters worden niet uitgebreid, zodat zou een onderzoek naar "woord"in <span class="codeph"> sp_q_2 geen automatische vervangingsuitbreiding </span> hebben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>12 </p> </td> 
   <td colname="col2"> <p>sp_end_day, sp_end_month, sp_end_year </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_end_day= <i>number</i>,sp_end_month= <i>number</i>, sp_end_year= <i>number</i> </code> </p> </td> 
   <td colname="col4"> <p>Deze drievoud van waarden specificeert de einddatumwaaier voor het onderzoek en moet als reeks worden verstrekt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>13 </p> </td> 
   <td colname="col2"> <p>sp_f </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_f= string </span> </p> </td> 
   <td colname="col4"> <p>Specificeert de karakterreeks van de koorden van de vraagparameter (zoals <span class="codeph"> sp_q </span>). Dit koord moet de karakterreeks van de pagina altijd aanpassen die de onderzoeksvorm bevat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>14 </p> </td> 
   <td colname="col2"> <p>sp_field_table </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_field_ table=table: field,field... </code> </p> </td> 
   <td colname="col4"> <p>Bepaalt een logische gegevenslijst die uit de bepaalde gebieden bestaat. Bijvoorbeeld, zou een lijst genoemd "punten"bestaande uit de gebieden "kleur,"grootte,"en "prijs"als het volgende worden gedefinieerd: </p> <p> <span class="codeph"> sp_field_table=items:kleur, grootte, prijs </span> </p> <p>De logische lijsten zijn het nuttigst samen met gebieden die hebben "staan lijsten"gecontroleerd toe (onder <span class="uicontrol"> Montages </span> &gt; <span class="uicontrol"> Meta-gegevens </span> &gt; <span class="uicontrol"> Definities </span>). Alle parameters van CGI en malplaatjemarkeringen die een gebiedsnaam als waarde nemen kunnen een lijstnaam naar keuze specificeren die door "." wordt gevolgd voorafgaand aan de gebiedsnaam (bijvoorbeeld, <span class="codeph"> sp_x_1=tablename.fieldname </span>). </p> <p>Bijvoorbeeld, om een onderzoek naar documenten uit te voeren die één of meerdere "rode"punten in grootte "groot"bevatten (waar de punten als parallelle rijen van meta-gegevens) worden vertegenwoordigd, kon u het volgende gebruiken: </p> <p> <code> sp_q_exact_1=red&amp;sp_x_1=items.color&amp; sp_q_exact_2=large&amp;sp_x_2=items.size&amp;sp_field_table=items:color,size,price </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>15 </p> </td> 
   <td colname="col2"> sp_i </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_i= <span class="varname"> waarde </span></span> </p> </td> 
   <td colname="col4"> <p>Negeert het onderzoek wanneer u rapporten produceert. </p> <p>Gebruik deze vraag om bepaalde achterste eindonderzoeken, zoals onderzoeken te maskeren die u bedoelde produceert, of onderzoeken die een Beheerder in het lidcentrum produceert. Omdat een eind - de gebruiker produceert deze types van onderzoeken niet, verschijnen zij niet omhoog in diverse het Onderzoek&amp;Promote rapporten van Adobe. </p> <p>De geldige waarden zijn <span class="codeph"> sp_i=1 </span> en <span class="codeph"> sp_i=2 </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>16 </p> </td> 
   <td colname="col2"> <p>sp_k </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_k= string </span> </p> </td> 
   <td colname="col4"> <p> Specificeert de inzameling voor het onderzoek te gebruiken. Het gebrek is geen inzameling, betekenend dat het onderzoek de gehele plaats zou moeten omvatten. </p> <p>Zie <a href="../c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3" type="reference" format="dita" scope="local"> Het Gebruiken van inzamelingen in onderzoeksvormen </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>17 </p> </td> 
   <td colname="col2"> <p>sp_l </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_l= string </span> </p> </td> 
   <td colname="col4"> <p>Specificeert de taal van de koorden van de vraagparameter (zoals <span class="codeph"> sp_q </span>). Het <i><span class="codeph"> koord </span></i> zou een standaardscèneidentiteitskaart moeten zijn die een ISO-639 taalcode bevat naar keuze gevolgd door een ISO-3166 landcode. Bijvoorbeeld, "en" of "en_US" voor het Engels of "ja" of "ja_JP" voor het Japans. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>18 </p> </td> 
   <td colname="col2"> <p>sp_letterlijk </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_literal= 0 of 1 </span> </p> </td> 
   <td colname="col4"> <p> Het plaatsen <span class="codeph"> sp_literal=1 maakt </span> tijdelijk alle eigenschappen onbruikbaar die de woorden in de vraag zouden kunnen interpreteren. Met deze parameter, slechts de letterlijke woorden van de documenten van de vraaggelijke, ongeacht synoniemen, afwisselende woordvormen, en de geluid-gelijkaardige aanpassing. </p> <p>Merk op dat <span class="codeph"> sp_literal=0 geen betekenis </span> heeft, en indien gebruikt genegeerd. </p> <p>Zie <a href="../c-about-linguistics-menu/c-about-dictionaries.md#concept_B8028B71EC8144669614C64578EDB034" type="concept" format="dita" scope="local"> over woordenboeken </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>19 </p> </td> 
   <td colname="col2"> <p>sp_m </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_m= aantal </span> </p> </td> 
   <td colname="col4"> <p> Specificeert of de samenvattingen worden getoond. 1 is ja, 0 is nee. Het gebrek is 1. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>20 </p> </td> 
   <td colname="col2"> <p>sp_n </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_n= aantal </span> </p> </td> 
   <td colname="col4"> <p> Specificeert het aantal van het resultaat dat de onderzoeksresultaten begint. Het gebrek is 1. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>21 </p> </td> 
   <td colname="col2"> <p>sp_not_found_page </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_not_found_page= url </span> </p> </td> 
   <td colname="col4"> <p> Specificeert of om aan gespecificeerde URL opnieuw te richten als er geen onderzoeksresultaten zijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>22 </p> </td> 
   <td colname="col2"> <p>sp_p </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_p= any/all/expression </span> </p> </td> 
   <td colname="col4"> <p> Specificeert het standaardtype van het zoeken om uit te voeren. Het gebruik van <span class="codeph"> om het even welk </span> middel onderzoek naar documenten die om het even welk woord van het vraagkoord bevatten. Het gebruik van <span class="codeph"> al </span> betekent onderzoek naar documenten die alle woorden in het vraagkoord bevatten. Het gebruik van <span class="codeph"> uitdrukking </span> betekent het vraagkoord wordt behandeld alsof het een geciteerde uitdrukking was en alle user-typed citaten worden genegeerd. </p> <p>Voor <span class="codeph"> uitdrukking </span> en <span class="codeph"> allen </span>, is de specificatie van "+" en "-"vóór onderzoekswoorden gehandicapt en die karakters worden genegeerd. Als <span class="codeph"> sp_p niet aanwezig </span> is, of als het aan een lege koord of om het even welk wordt geplaatst, standaard "+"en "-"woordprefixen worden toegestaan. </p> <p>Zie de beschrijving van de Uiteinden van het Onderzoek voor meer informatie over het gebruiken van plus ("+") en minus ("-") in onderzoeken. </p> <p>Zie <a href="../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8" type="concept" format="dita" scope="local"> over zoekopdrachten </a>. </p> <p>Zie de steekproef geavanceerde onderzoeksvorm voor voorbeelden bij het gebruiken van de <span class="codeph"> sp_p </span> parameter. </p> <p>Zie <a href="../c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A" type="reference" format="dita" scope="local"> Voorbeeld van geavanceerd zoekformulier </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>23 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p> sp_p_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_p_#= om het even welk/alle/uitdrukking </span> </p> </td> 
   <td colname="col4"> <p>Specificeert het standaardtype van het zoeken dat met de overeenkomstige <span class="codeph"> sp_q_# </span> vraag moet worden uitgevoerd. "#"wordt vervangen met een aantal tussen 1 en 16 (bijvoorbeeld, is <span class="codeph"> sp_p_8 </span> op de genummerde vraag <span class="codeph"> sp_q_8 van toepassing </span>). Het gebruik van <span class="codeph"> om het even welk </span> middel keert documenten terug die om het even welk woord van het vraagkoord bevatten. Het gebruik van <span class="codeph"> alle </span> middelen terugkeerdocumenten die alle woorden in het vraagkoord bevatten. Het gebruik van <span class="codeph"> uitdrukking </span> betekent om het vraagkoord te behandelen alsof het een volledige uitdrukking was (en alle user-typed citaten worden genegeerd). </p> <p>Als u of <span class="codeph"> alle </span> of <span class="codeph"> uitdrukking specificeert </span>, om het even welke plus en minus tekens alvorens de onderzoekswoorden worden genegeerd. Als <span class="codeph"> sp_p_# </span> wordt weggelaten, of als het aan een leeg koord of om het <span class="codeph"> even welk wordt geplaatst </span>, standaard "+"en "-"prefixen worden toegestaan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>24 </p> </td> 
   <td colname="col2"> <p>sp_pt </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_pt= <i>exact/equivalent/compatible</i> </code> </p> </td> 
   <td colname="col4"> <p> Specificeert het type van doel aanpassing om van toepassing te zijn. Het gebruik van <span class="codeph"> nauwkeurig </span> betekent de gelijken van het opbrengstdoel slechts in documenten die precies het vraagkoord binnen doelinhoud aanpassen. Het gebruik van <span class="codeph"> equivalent </span> is als nauwkeurig, behalve dat is de orde van de woorden niet belangrijk. Het gebruik van <span class="codeph"> compatibele </span> plaatst automatisch het doel aanpassingstype dat op de waarde van de <span class="codeph"> sp_p </span> parameter wordt gebaseerd. Het gebruik van <span class="codeph"> nauwkeurig </span> wordt gebruikt als <span class="codeph"> sp_p </span> alle <span class="codeph"> of </span> uitdrukking is <span class="codeph"> , anders </span>wordt het equivalent <span class="codeph"> </span> gebruikt. De standaardwaarde van <span class="codeph"> sp_pt </span> is <span class="codeph"> compatibel </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>25 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_pt_# </p> </td> 
   <td colname="col3"> <p> <code> sp_pt_#= <i>exact/equivalent/compatible</i> </code> </p> </td> 
   <td colname="col4"> <p>Specificeert het type van doel dat met de overeenkomstige <span class="codeph"> sp_q_# vraag aanpast van toepassing te zijn </span> . "#"wordt vervangen met een aantal tussen 1 en 16 (bijvoorbeeld, is <span class="codeph"> sp_p_8 </span> op de genummerde vraag <span class="codeph"> sp_q_8 van toepassing </span>). Het gebruik van <span class="codeph"> nauwkeurig </span> betekent de gelijken van het opbrengstdoel slechts in documenten die precies het vraagkoord binnen doelinhoud aanpassen. Het gebruik van <span class="codeph"> equivalent </span> is als <span class="codeph"> nauwkeurig </span>, behalve dat is de orde van de woorden niet belangrijk. Het gebruik van <span class="codeph"> compatibele </span> plaatst automatisch het doel aanpassingstype dat op de waarde van de overeenkomstige <span class="codeph"> sp_p_# </span> parameter wordt gebaseerd: <span class="codeph"> nauwkeurig </span> wordt gebruikt als <span class="codeph"> sp_p_# allen of uitdrukking </span> is, anders <span class="codeph"> wordt het equivalent </span> gebruikt. De standaardwaarde van <span class="codeph"> sp_pt_# </span> is <span class="codeph"> compatibel </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>26 </p> </td> 
   <td colname="col2"> <p>sp_q </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q= string </span> </p> </td> 
   <td colname="col4"> <p> Specificeert het vraagkoord voor het onderzoek. Een leeg koord leidt tot geen resultaten die worden getoond. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>27 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_q_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q_#= tekst </span> </p> </td> 
   <td colname="col4"> <p>Deze parameter staat voor de verwezenlijking van veelvoudige vragen op onderzoeksvormen toe. De <span class="codeph"> sp_q_# </span> parameter bevat het vraagkoord in de bepaalde genummerde vraag te gebruiken. Een zoekverzoek kan tot 16 verschillende genummerde vragen ( <span class="codeph"> sp_q_1 </span> aan <span class="codeph"> sp_q_16 </span>) verwijzen. </p> <p>Bijvoorbeeld, keert het voorleggen van de volgende vorm alle documenten terug die de woorden "groot"en "boeken"bevatten. </p> <p> <code class="syntax html"> Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="great"&gt; 
      Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="books"&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>28 </p> </td> 
   <td colname="col2"> <p>sp_q_day, sp_q_month, sp_q_year </p> </td> 
   <td colname="col03"> <p> sp_q _day_#, sp_q_month_#, sp_q _year_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q_day= integer waarde </span> </p> <p> <span class="codeph"> sp_q_month= integer waarde </span> </p> <p> <span class="codeph"> sp_q_year= integer waarde </span> </p> <p> <span class="codeph"> sp_q_day_#= integer waarde </span> </p> <p> <span class="codeph"> sp_q_maand_#= geheelwaarde </span> </p> <p> <span class="codeph"> sp_q_year_#= integer waarde </span> </p> </td> 
   <td colname="col4"> <p>Deze parameters worden gebruikt om een nauwkeurige datum voor een bepaalde vraag te specificeren. De <span class="codeph"> sp_q_day </span>, <span class="codeph"> sp_q_month </span>, en <span class="codeph"> sp_q_year </span> parameters zijn op de belangrijkste vraag van toepassing ( <span class="codeph"> sp_q </span>). </p> <p>De <span class="codeph"> # </span>parameter wordt vervangen met een aantal tussen 1 en 16 (bijvoorbeeld, <span class="codeph"> sp_q_day_6 </span>, die op de genummerde vraag <span class="codeph"> sp_q_6 van toepassing is </span>). Door gebrek, worden alle data gezocht met betrekking tot Greenwich Gemiddelde Tijd. </p> <p>De volgende sectie van code laat een gebruiker naar het woord "oranje"in documenten zoeken gedateerd "Jan. 1st, 2000"op een user-defined gebied genoemd <span class="codeph"> PublishDate </span>: </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="PublishDate"&gt; Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="orange"&gt;On&nbsp;:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_day_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Day&lt;input&nbsp;type="text"&nbsp;name="sp_q_month_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Month &lt;input&nbsp;type="text"&nbsp;name="sp_q_year_1"&nbsp;size="4"&nbsp;value="2000"&gt;&nbsp;Year&nbsp; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>29 </p> </td> 
   <td colname="col2"> <p>sp_q_location </p> </td> 
   <td colname="col03"> <p>sp_q_location_# </p> </td> 
   <td colname="col3"> <p> <code> sp_q_location=<i>latitude/longitude</i> OR <i>areacode</i> OR <i>zipcode</i> </code> </p> <p> <code> sp_q_location_#= <i>latitude/longitude</i> OR <i>areacode</i> OR <i>zipcode</i> </code> </p> </td> 
   <td colname="col4"> <p>Deze parameters associëren een plaats met de belangrijkste of genummerde vraag. Het gebruik van <span class="codeph"> sp_q_location </span> beïnvloedt de belangrijkste vraag, <span class="codeph"> sp_q_location_# </span> (waar <span class="codeph"> # </span> door een aantal van 1 tot 16) wordt vervangen, beïnvloedt de bepaalde genummerde vraag. Deze parameters worden gebruikt om minimum en/of maximumafstandsnabijheidsonderzoeken tegen de plaatsgegevens uit te voeren die voor elke plaatspagina worden geïndexeerd. Het formaat van de waarde bepaalt zijn interpretatie. </p> <p>Een waarde in de vorm DDD (drie cijfers) wordt geïnterpreteerd als een telefoongebied van de V.S.; een waarde in de vorm DDD of DDD-DDDD wordt geïnterpreteerd als postcode van de V.S.; en een waarde in de vorm ±DD.DDDD±DDD.DDDD wordt geïnterpreteerd als breedtegraad/lengtegraad paar. De tekens worden vereist voor elke waarde. Bijvoorbeeld, +38.6317+120.5509 specificeert breedtegraad 38.6317, lengtegraad 120.5509. </p> <p>Zie <a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> Over nabijheidsonderzoek </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>30 </p> </td> 
   <td colname="col2"> <p>sp_q_max_relevant_afstand </p> </td> 
   <td colname="col03"> <p>sp_q_max_relevant_afstand _# </p> </td> 
   <td colname="col3"> <p> <code> sp_q_max_relevant_distance= <i>value</i> </code> </p> <p> <code> sp_q_max_relevant_distance_#= <i>value</i> </code> </p> </td> 
   <td colname="col4"> <p>Deze parameters bepalen de relevantieberekening die op nabijheidsonderzoeken wordt toegepast. Het gebruik van <span class="codeph"> sp_q_max_relevant_distance </span> beïnvloedt de belangrijkste vraag, <span class="codeph"> sp_q_max_relevant_distance_# </span> (waar <span class="codeph"> # </span> door een aantal van 1 tot 16) wordt vervangen, beïnvloedt de bepaalde genummerde vraag. </p> <p>De standaardwaarde van <span class="codeph"> sp_q_max_relevant_distance </span> is 100. </p> <p>Een perfecte relevantiescore voor de nabijheidscomponent zou een afstand van 0 vertegenwoordigen. Een minimum relevantiescore voor de nabijheidscomponent zou een afstand net over de gespecificeerde <span class="codeph"> sp_q_max_relevant_distance_#_ </span> waarde vertegenwoordigen. </p> <p>Zie <a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> Over nabijheidsonderzoek </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>31 </p> </td> 
   <td colname="col2"> <p>sp_q_min_day, sp_q_min_month, sp_q_min_year </p> <p>sp_q_max_day, sp_q_max_maand, sp_q_max_jaar </p> </td> 
   <td colname="col03"> <p>sp_q_min_day_#, sp_q_min_month_#, sp_q_min_year_# </p> <p> sp_q_max_day_#, sp_q_max_maand_#, sp_q_max_year_# </p> </td> 
   <td colname="col3"> <p> <code> sp_q_min_day=<i>integer value</i> </code> </p> <p> <code> sp_q_min_month=<i>integer value</i> </code> </p> <p> <code> sp_q_min_year=<i>integer value</i> </code> </p> <p> <code> sp_q_max_day=<i>integer value</i> </code> </p> <p> <code> sp_q_max_month=<i>integer value</i> </code> </p> <p> <code> sp_q_max_year=<i>integer value</i> </code> </p> <p> <code> sp_q_min_day_#=<i>integer value</i> </code> </p> <p> <code> sp_q_min_month_#=<i>integer value</i> </code> </p> <p> <code> sp_q_min_year_#=<i>integer value</i> </code> </p> <p> <code> sp_q_max_day_#=<i>integer value</i> </code> </p> <p> <code> sp_q_max_month_#=<i>integer value</i> </code> </p> <p> <code> sp_q_max_year_#=<i>integer value</i> </code> </p> </td> 
   <td colname="col4"> <p>Deze parameters worden gebruikt om minimum en maximumdatumwaaiers voor een bepaalde vraag te plaatsen. De <span class="codeph"> sp_q_min_day </span>, <span class="codeph"> sp_q_min_month </span>, <span class="codeph"> sp_q_min_year </span>, <span class="codeph"> sp_q_max_day </span>, <span class="codeph"> sp_q_max_maand </span><i></i> <span class="codeph"> </span>, ensp_q_max_year parameters zijn van toepassing op de belangrijkste vraag (sp_q). </p> <p>Het <span class="codeph"> # </span>in de parameternaam wordt vervangen met een aantal tussen 1 en 16 (bijvoorbeeld, <span class="codeph"> sp_q_min_day_6 </span> is op de genummerde vraag <span class="codeph"> sp_q_6 </span>) van toepassing. </p> <p>Het is wettelijk om slechts een minimumdatum, slechts een maximumdatum, of zowel minimum als maximumdatum te specificeren. Voor een bepaald minimum- of maximumpakket moeten echter alle drie datumparameters worden gespecificeerd (dag, maand en jaar). Door gebrek, worden alle data gezocht met betrekking tot Greenwich Gemiddelde Tijd. </p> <p>De volgende sectie van code laat een gebruikersonderzoek naar het woord "oranje"in documenten met een datum tussen 1st, 2000 en dec. 31st, 2000 op een user-defined gebied genoemd <span class="codeph"> PublishDate </span>: </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="PublishDate"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="orange"&gt;Between:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_min_day_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Start&nbsp;Day&lt;input&nbsp;type="text"&nbsp;name="sp_q_min_month_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Start&nbsp;Month 
      &lt;input&nbsp;type="text"&nbsp;name="sp_q_min_year_1"&nbsp;size="4"&nbsp;value="2000"&gt;&nbsp;Start&nbsp;Year 
      And:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_max_day_1"&nbsp;size="2"&nbsp;value="31"&gt;&nbsp;End&nbsp;Day 
      &lt;input&nbsp;type="text"&nbsp;name="sp_q_max_month_1"&nbsp;size="2"&nbsp;value="12"&gt;&nbsp;End&nbsp;Month 
      &lt;input&nbsp;type="text"&nbsp;name="sp_q_max_year_1"&nbsp;size="4"&nbsp;value="2000"&gt;&nbsp;End&nbsp;Year </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>32 </p> </td> 
   <td colname="col2"> <p>sp_q_min, sp_q_max </p> </td> 
   <td colname="col03"> <p>sp_q_min_#, sp_q_max_#, sp_q_exact_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q_min= waarde </span> </p> <p> <span class="codeph"> sp_q_max= waarde </span> </p> <p> <span class="codeph"> sp_q_min_#= waarde </span> </p> <p> <span class="codeph"> sp_q_max_#= waarde </span> </p> <p> <span class="codeph"> sp_q_exact_#=waarde </span> </p> </td> 
   <td colname="col4"> <p>Deze parameters specificeren een minimum (en/of maximum) waarde om op de belangrijkste of genummerde vraag van toepassing te zijn. Het gebruik van <span class="codeph"> sp_q_min </span>, <span class="codeph"> sp_q_max </span>, en <span class="codeph"> sp_q_exact </span> beïnvloedt de belangrijkste vraag ( <span class="codeph"> sp_q </span>). </p> <p>Vervang <span class="codeph"> # </span>in de parameternaam met een aantal tussen 1 en 16 (bijvoorbeeld, <span class="codeph"> sp_q_min_8 </span> is op de genummerde vraag <span class="codeph"> sp_q_8 van toepassing </span>). </p> <p>Het gebruik van <span class="codeph"> sp_q_exact_# </span> is shorthand voor het specificeren van zowel <span class="codeph"> sp_q_min_# </span> als <span class="codeph"> sp_q_max_# </span> met de zelfde waarde. Als <span class="codeph"> sp_q_exact_# </span> wordt gespecificeerd, worden om het even welke overeenkomstige <span class="codeph"> sp_q_min_# </span> of <span class="codeph"> sp_q_max_# </span> parameters genegeerd. </p> <p>De <span class="codeph"> sp_q_min_# </span>, <span class="codeph"> sp_q_max_# </span> en <span class="codeph"> sp_q_exact_# </span> parameters kunnen veelvoudige "|" gescheiden waarden naar keuze specificeren. Bijvoorbeeld, aan onderzoek naar documenten die de waarde groen of rood binnen het "kleur"gebied bevatten: <span class="codeph"> ...&amp;sp_q_exact_1=groen|rood&amp;sp_x_1=kleur </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>33 </p> </td> 
   <td colname="col2"> <p>sp_q_nocp </p> </td> 
   <td colname="col03"> <p>sp_q _nocp _# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q_nocp= 1 of 0 </span> </p> <p> <span class="codeph"> sp_q_nocp_#= 1 of 0 </span> </p> </td> 
   <td colname="col4"> <p>De standaardwaarde van de standaardparameter is <span class="codeph"> 0 </span> betekenend dat de Gemeenschappelijke uitbreidingen van de Woorden worden uitgevoerd. </p> <p>Wanneer de reeks aan <span class="codeph"> 1 </span> voor de overeenkomstige onderzoeksvraag, de Gemeenschappelijke uitbreidingen van de Zetters niet wordt uitgevoerd. </p> <p>Het gebruiken van <span class="codeph"> sp_q_nocp </span> beïnvloedt de belangrijkste parameter van de onderzoeksvraag <span class="codeph"> sp_q </span>. Om deze parameter op een genummerde onderzoeksvraag toe te passen, vervang <span class="codeph"> # </span> in de parameternaam met het overeenkomstige aantal. Bijvoorbeeld, is <span class="codeph"> sp_q_nocp_8 </span> op de genummerde onderzoeksvraag <span class="codeph"> sp_q_8 van toepassing </span>. </p> <p> 
     <!--See also <xref href="c_about_common_phrases.xml#concept_4946E53586DF492EAEB1B7F757FD440F" format="dita" scope="local">About Common Phrases</xref>--> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>34 </p> </td> 
   <td colname="col2"> <p>sp_q_required </p> </td> 
   <td colname="col03"> <p>sp_q _required _# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q_required= 1 of 0 of -1 </span> </p> <p> <span class="codeph"> sp_q_required_#= 1 of 0 of -1 </span> </p> </td> 
   <td colname="col4"> <p>Deze parameter bepaalt of een gelijke (1) moet (1), kan (0), of moet niet (-1) in de overeenkomstige vraag voorkomen opdat een document op de resultaatpagina moet zijn teruggekeerd. </p> <p>Het gebruik van <span class="codeph"> sp_q_required </span> beïnvloedt de belangrijkste vraag ( <span class="codeph"> sp_q </span>). </p> <p>Om op een genummerde vraag van toepassing te zijn, vervang <span class="codeph"> # </span> in de parameternaam met het overeenkomstige aantal (bijvoorbeeld, <span class="codeph"> sp_q_required_8 </span> is op de genummerde vraag <span class="codeph"> sp_q_8 </span>) van toepassing. De standaardwaarde van de parameter is 1 (moet aanpassen). </p> <p>Om naar documenten te zoeken die het woord "calc"bevatten maar NIET "mac"bevatten, "win"of "allen"op het user-defined "platform"gebied bevatten, kon uw HTML- onderzoeksformulier de volgende lijnen bevatten: </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="platform"&gt; 
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
   <td colname="col4"> <p>Specificeert of om aan het onderzoeksresultaat URL opnieuw te richten als er slechts één onderzoeksresultaat is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>36 </p> </td> 
   <td colname="col2"> <p>sp_referrer </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_referrer= url </span> </p> </td> 
   <td colname="col4"> <p>Specificeert verwijzer URL voor het onderzoek. Nuttig voor onderzoek herschrijf regels waar de onderzoeksresultaten terug naar de zelfde plaats zoals de onderzoeksvorm verbinden. </p> <p>De standaardwaarde is de standaardCGI HTTP_REFERRER waarde die door browser wordt geleverd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>37 </p> </td> 
   <td colname="col2"> <p>sp_ro </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_ro= <span class="varname"> veld </span>: <span class="varname"> relevantie </span></span> </p> </td> 
   <td colname="col4"> <p>Staat facultatieve onderzoekstijd, per gebiedsnaam, relevantiecontrole toe. De <span class="codeph"> of </span> in de parameternaam staat voor "relevantiegrief". De parameter keurt één of meerdere gebiedsnamen goed, die door een dubbelpuntkarakter worden gevolgd, die door een relevantiewaarde van 0-10 wordt gevolgd. </p> <p>Bijvoorbeeld, om de relevantiewaarde voor de gebiedsnaam "lichaam"aan 10 te plaatsen, op het ogenblik een klant een onderzoek uitvoert, zou de parameter als volgt verschijnen: </p> <p> <span class="codeph"> sp_ro=body:10 </span> </p> <p>Of, om veelvoudige gebiedsrelevantie te specificeren treedt in het parameterkoord met voeten, kunt u een pijpafbakening gebruiken. Bijvoorbeeld, om de relevantiewaarde voor de gebiedsnamen "lichaam"en "titel"aan 9 te plaatsen, op het ogenblik een klant een onderzoek uitvoert, zou de parameter als volgt verschijnen: </p> <p> <span class="codeph"> sp_ro=body:9|titel:9 </span> </p> <p> <p>Opmerking:  Het specificeren van een gebied dat niet betrokken bij het bijbehorende onderzoek is heeft geen effect. Bijvoorbeeld, als u <span class="codeph"> sp_ro=title plaatst:10 </span>, maar de <span class="codeph"> titel </span> - gebiedsnaam wordt niet gezocht, heeft de <span class="codeph"> sp_ro </span> parameter geen effect. Met andere woorden, zoekt het specificeren van een gebiedsnaam die de <span class="codeph"> sp_ro </span> parameter gebruikt automatisch niet dat gebied; in plaats daarvan, treedt het slechts de bijbehorende relevantie het plaatsen van dat gebied met voeten. </p> </p> <p>Zie Vooraf gedefinieerde of door de gebruiker gedefinieerde meta-tagvelden <a href="../c-about-settings-menu/c-about-metadata-menu.md#task_0A7657B63596421BB6DB3ED44F827AB3" type="task" format="dita" scope="local"> bewerken </a>. </p> <p>Zie <a href="../c-about-rules-menu/c-about-query-cleaning-rules.md#concept_17F3CDDC3C8A4128AF092A82B777B86C" type="concept" format="dita" scope="local"> over het Schoonmaken van de Vraag Regels </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>38 </p> </td> 
   <td colname="col2"> <p>sp_s </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_s= aantal </span> </p> </td> 
   <td colname="col4"> <p>Specificeert de soortorde. Nul (0) is het gebrek en betekent om door relevantiescore te sorteren. Eén (1) betekent sorteren op datum en -1 betekent niet sorteren. </p> <p>U kunt een gebiedsnaam voor de waarde van de <span class="codeph"> sp_s </span> parameter specificeren. Bijvoorbeeld, <span class="codeph"> sp_s=title </span> sorteert resultaten volgens de waarden die in het titelgebied bevat zijn. Wanneer een gebiedsnaam voor de waarde van een <span class="codeph"> sp_s </span> parameter wordt gebruikt, worden de resultaten gesorteerd door dat gebied en dan gesubsorteerd door relevantie. </p> <p>De vastgestelde Sortering voor het referenced gebied aan of <span class="uicontrol"> die </span> of <span class="uicontrol"> Daling </span> in <span class="uicontrol"> Montages </span> &gt; <span class="uicontrol"> Meta-gegevens </span> &gt; <span class="uicontrol"> Definities stijgen </span> of afnemen om deze eigenschap toe te laten. </p> <p>U kunt verscheidene soortgebieden aan één enkele vraag ook toewijzen door de <span class="codeph"> sp_s </span> parameter verscheidene keren in de onderzoeksvorm te plaatsen. De volgende malplaatjelijnen plaatsen de onderzoeksresultaten die eerst door kunstenaarsnaam, dan door albumnaam, en dan door spoornaam moeten worden gesorteerd. </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="artist"&gt; 
      &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="album"&gt; 
      &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="track"&gt; 
      Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="Music&nbsp;Search"&gt; </code> </p> <p>Het is ook mogelijk op lijst aangepaste gebiedsgegevens te sorteren door een bepalende eigenschap van de lijstnaam voorafgaand aan de gebiedsnaam, bijvoorbeeld, items.price te specificeren. Zie de <span class="codeph"> sp_field_table </span> parameter voor meer informatie over lijst het aanpassen. </p> <p>Als het zoeken door nabijheid, kunt u resultaten volgens nabijheid sorteren door een "gebied van de nabijheidsoutput"te specificeren. </p> <p>Zie <a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> Over nabijheidsonderzoek </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>39 </p> </td> 
   <td colname="col2"> <p>sp_sr </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_sr= veld </span> </p> </td> 
   <td colname="col4"> <p>Specificeert het rangschikkingsgebied voor het statische rangschikken te gebruiken. Het veld moet een veld van het type Rank zijn met een relevantie groter dan 0. Als geen <span class="codeph"> sp_sr </span> parameter voor de vraag wordt verstrekt, wordt een gebied van typeRank automatisch geselecteerd. </p> <p>Om het statische rangschikken voor een bepaalde vraag onbruikbaar te maken, omvat een ONGELDIGE waarde voor <span class="codeph"> sp_sr </span> (bijvoorbeeld, <span class="codeph"> &lt;input type= "verborgen" name="sp_sr" value=""&gt; </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>40 </p> </td> 
   <td colname="col2"> <p>sp_sfvl_field </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_sfvl_field= string </span> </p> </td> 
   <td colname="col4"> <p>Specificeert de naam van een gebied samen met de <span class="codeph"> &lt;zoek-gebied-waarde-lijst&gt; </span> markering in het onderzoeksmalplaatje te gebruiken. </p> <p>U kunt veelvoudige <span class="codeph"> sp_sfvl_field parameters specificeren </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>41 </p> </td> 
   <td colname="col2"> <p> sp_sfvl_df_count </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_sfvl_df_count= <span class="varname"> &lt;integer_value&gt; </span></span> </p> </td> 
   <td colname="col4"> <p> 
     <!--NEW 2/2/2014-->Verzoeken tot <span class="codeph"> &lt;integer_value&gt; <span class="varname"> </span> zoek- </span> field-value-list <span class="codeph"> </span> dynamische-facet velden voor deze zoekopdracht. </p> <p>De standaardwaarde is 0. De maximum toegestane waarde is het huidige aantal dynamisch-facetgebieden, dynamisch-facet-gebied-telling die voor een bepaalde index wordt bepaald. De waarden van het geheel die onder 0 zijn worden behandeld als 0. De hierboven gespecificeerde waarden van het geheel <span class="codeph"> dynamisch-facet-gebied-gebied-telling </span> worden gemaximeerd bij <span class="codeph"> dynamisch-facet-gebied-telling </span>. Niet-geheelwaarden worden genegeerd; zij worden behandeld als de standaardwaarde. </p> <p>Het onderzoek van een bepaald segment is begrensd met een maximum toegestane <span class="codeph"> sp_sfvl_df_count </span> waarde van de <span class="codeph"> dynamische-facet-field-count </span> waarde van deze plak. Wanneer het samenvoegen van plakresultaten, is de efficiënte maximumwaarde van <span class="codeph"> sp_sfvl_df_count </span> de maximum daadwerkelijke <span class="codeph"> sp_sfvl_df_count over alle plakken </span> . </p> <p>Zie dynamische facetten <a href="../c-about-design-menu/c-about-dynamic-facets.md#task_D17F484130E448258100BAC1EEC53F39" format="dita" scope="local"> configureren </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>42 </p> </td> 
   <td colname="col2"> <p> sp_sfvl_df_exclusion </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> </p> <p> <span class="codeph"> sp_sfvl_df_exclu= &lt; <span class="varname"> field_name </span>&gt;[|&lt; <span class="varname"> field_name </span> &gt; </span>|.. </p> </td> 
   <td colname="col4"> <p> Specificeert een lijst van specifieke dynamische facetgebieden om van overweging voor dit onderzoek uit te sluiten. </p> <p>Door gebrek, worden alle dynamische facetgebieden overwogen. </p> <p>Zie dynamische facetten <a href="../c-about-design-menu/c-about-dynamic-facets.md#task_D17F484130E448258100BAC1EEC53F39" format="dita" scope="local"> configureren </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>43 </p> </td> 
   <td colname="col2"> <p> sp_sfvl_df_include </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> </p> <p> <span class="codeph"> sp_sfvl_df_include= &lt; <span class="varname"> field_name </span>&gt;[|&lt; <span class="varname"> field_name </span> &gt; </span>|.. </p> </td> 
   <td colname="col4"> <p> Specificeert een lijst van specifieke dynamische facetgebieden om in de onderzoeksresultaten te omvatten. </p> <p> <p>Opmerking:  De <span class="codeph"> sp_sfvl_df_count parameter bepaalt het totale aantal dynamische facetgebieden om terug te keren, met inbegrip van om het even welk gespecificeerd door </span> sp_sfvl_df_include <span class="codeph"> </span>. Namelijk staat het gebruiken van <span class="codeph"> sp_sfvl_df_include </span> niet de totale telling van teruggekeerde dynamische facetgebieden toe om sp_sfvl_df_count te overschrijden <span class="codeph"> </span>. </p> </p> <p>Zie dynamische facetten <a href="../c-about-design-menu/c-about-dynamic-facets.md#task_D17F484130E448258100BAC1EEC53F39" format="dita" scope="local"> configureren </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>44 </p> </td> 
   <td colname="col2"> <p>sp_gestadig </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_staged= 0 of 1 </span> </p> </td> 
   <td colname="col4"> <p>Als <span class="codeph"> sp_staged=1 </span> met een vraag wordt voorgelegd, is de vraag die in werking wordt gesteld een gefaseerd onderzoek. </p> <p>Een gefaseerd onderzoek gebruikt alle componenten die momenteel met inbegrip van de index en de malplaatjes getrapte zijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>45 </p> </td> 
   <td colname="col2"> <p>sp_start_day, sp_start_month, sp_start_year </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_start_day= aantal </span> </p> <p> <span class="codeph"> sp_start_month= aantal </span> </p> <p> <span class="codeph"> sp_start_year= aantal </span> </p> </td> 
   <td colname="col4"> <p>Dit drievoud van waarden specificeert de beginnende datumwaaier voor het onderzoek en u verstrekt het als reeks. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>46 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_ suggestie _q </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_sug_q= aantal </span> </p> </td> 
   <td colname="col4"> <p>De <span class="codeph"> sp_sug_q </span> parameter bepaalt welke <span class="codeph"> sp_q [_#] </span> parameter om met de dienst van de Samenvatting te gebruiken bepaalt. </p> <p>De standaardwaarde van <span class="codeph"> sp_sug_q </span> is 0, zo betekent het dat de onderzoeksmotor de waarde van <span class="codeph"> sp_q </span> gebruikt om de suggesties te bepalen. </p> <p>Vastgestelde <span class="codeph"> sp_sug_q=1 </span> om de waarde van <span class="codeph"> sp_q_1 te gebruiken </span> om de suggesties te bepalen, etc. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>47 </p> </td> 
   <td colname="col2"> <p>sp_t </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_t= string </span> </p> </td> 
   <td colname="col4"> <p>Specificeert het vervoermalplaatje aan gebruik. </p> <p>Deze parameter is nuttig als u de verschijning van de resultaten van het kernonderzoek over uw website wilt controleren door verschillende malplaatjes van het onderzoeksvervoer voor elk gebied in uw rekening van het Onderzoek te gebruiken. </p> <p>Het standaardvervoermalplaatje is "onderzoek". </p> <p>Zie Meerdere transportsjablonen <a href="../c-appendices/c-templates.md#reference_12AAB3B9F4C74C11956F1DBA95714C2F" type="reference" format="dita" scope="local"> beheren voor uw website </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>48 </p> </td> 
   <td colname="col2"> <p>sp_trace </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_trace= 0 of 1 </span> </p> </td> 
   <td colname="col4"> <p>Wanneer geplaatst als <span class="codeph"> sp_stage=1 </span>, laat het vermogen van het het spoorspoor van het kernonderzoek in Simulator toe. </p> <p>Zie <a href="../c-about-simulator.md#concept_020AA6751E32421A96A3455508364C7E" format="dita" scope="local"> over Simulator </a>. </p> <p> <p>Opmerking:  Als deze parameter niet wordt gespecificeerd, verzamelt het kernonderzoek niet de het vinden informatie en de verwante markeringen van het malplaatje van het kernonderzoek hebben geen output. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>49 </p> </td> 
   <td colname="col2"> <p>sp_w, sp_w_control </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_w= <i>sound-alike-enable</i> </code> </p> <p> <code> sp_w_control=<i>sound-alike-control</i> </code> </p> </td> 
   <td colname="col4"> <p>Specificeert dat de geluid-gelijkaardige aanpassing voor deze bepaalde vraag zou moeten worden toegelaten of worden onbruikbaar gemaakt. </p> <p>sp_w_control voor "Exact"wordt genegeerd. De correcte-gelijkaardige aanpassing is Gehandicapten. </p><p>sp_w_control voor "Alike"is genegeerd. Correct-gelijkaardige aanpassing wordt toegelaten</p><p>sp_w_control voor om het even wat anders is 1. De correcte-gelijkaardige aanpassing is Gehandicapten. </p><p>De sp_w_control voor Iets anders is iets anders. Correct-gelijkaardige aanpassing wordt toegelaten. </p>De <span class="codeph"> sp_w_control </span> parameter laat u een negatief of positief geschreven checkbox voor eindgebruikercontrole van correct-gelijkaardige aanpassing tot stand brengen. </p> <p>Als <span class="codeph"> sp_w_control=0 </span> wordt gebruikt, dan wordt een negatief geschreven checkbox gebruikt om de <span class="codeph"> sp_w </span> parameter zoals in het volgende voorbeeld te plaatsen: </p> <p> <code class="syntax html"> &lt;input&nbsp;type=hidden&nbsp;name="sp_w_control"&nbsp;value="0"&gt;&lt;input&nbsp;type=checkbox&nbsp;name="sp_w"&nbsp;value="exact"&gt;No&nbsp;Sound-Alike&nbsp;matching </code> </p> <p>Als <span class="codeph"> sp_w_control=1 </span> wordt gebruikt, dan wordt een positief geschreven checkbox gebruikt om de <span class="codeph"> sp_w </span> parameter zoals in het volgende te plaatsen: </p> <p> <code class="syntax html"> &lt;input&nbsp;type=hidden&nbsp;name="sp_w_control"&nbsp;value="1"&gt;&lt;input&nbsp;type=checkbox&nbsp;name="sp_w"&nbsp;value="alike"&gt;Sound-Alike&nbsp;matching </code> </p> <p>Zie de steekproef geavanceerde onderzoeksvorm voor meer voorbeelden bij het gebruiken van <span class="codeph"> sp_w_control </span> en <span class="codeph"> sp_w </span> parameters. </p> <p>Zie <a href="../c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A" type="reference" format="dita" scope="local"> Voorbeeld van geavanceerd zoekformulier </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>50 </p> </td> 
   <td colname="col2"> <p>sp_x </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_x= veld </span> </p> </td> 
   <td colname="col4"> <p>Specificeert de gebieden aan onderzoek naar het vraagkoord. om het even welk middel zoek alle gebieden. titel betekent zoekopdracht alleen titelvelden. desc betekent onderzoek slechts documentbeschrijvingsgebieden. sleutels betekent onderzoek slechts documentsleutelwoorden. lichaam betekent onderzoek slechts lichaamstekst. alt betekent onderzoek slechts afwisselende teksten. url betekent onderzoek slechts de waarden URL. doel betekent onderzoek slechts doelwoorden. In elk van deze gevallen worden de gebruikersspecificaties van "text:", "desc:", "keys:", "body:", "alt:", "url:", en "target:" gebiedprefixen binnen de overeenkomstige <span class="codeph"> sp_q </span> parameter genegeerd. Als <span class="codeph"> sp_x </span> niet aanwezig is of als het aan een leeg koord of om het even welk wordt geplaatst, dan worden de standaardprefixen van het gebruikersgebied toegestaan. Zie de beschrijving van de Uiteinden van het Onderzoek voor meer informatie over de gebiedprefixen. </p> <p>Zie <a href="../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8" type="concept" format="dita" scope="local"> over zoekopdrachten </a>. </p> <p>Zie de steekproef Geavanceerde beschrijving van de Vorm van het Onderzoek voor voorbeelden gebruikend de <span class="codeph"> sp_x </span> parameter. </p> <p>Zie <a href="../c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A" type="reference" format="dita" scope="local"> Voorbeeld van geavanceerd zoekformulier </a>. </p> <p>U kunt vragen tot stand brengen die alle gebieden zoeken die aan <span class="uicontrol"> Onderzoek door Gebrek </span> onder <span class="uicontrol"> Opties worden geplaatst &gt; de Meta-gegevens </span> &gt; <span class="uicontrol"> Definities </span> door <span class="uicontrol"> sp_x=any te plaatsen </span> <span class="codeph"> </span>. Zowel pre als user-defined gebieden kunnen als waarde van de <span class="codeph"> sp_x </span> parameter worden gebruikt. </p> <p>U kunt verscheidene gebieden aan één enkele vraag ook toewijzen door de <span class="codeph"> sp_x </span> parameter verscheidene keren te plaatsen. De volgende malplaatjelijnen laten gebruikers zowel de "titel"als "auteur"gebieden voor "Grote Boeken"vragen. </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x"&nbsp;value="title"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x"&nbsp;value="author"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="Great&nbsp;Books"&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>51 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_x_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_x_#= veldnaam </span> </p> </td> 
   <td colname="col4"> <p>Deze parameter specificeert welk gebied aan onderzoek in de overeenkomstige <span class="codeph"> sp_q_# </span> vraag. <span class="codeph"> # <span class="codeph"> </span> wordt vervangen met een aantal tussen 1 en 16 (bijvoorbeeld, </span> sp_x_8 <span class="codeph"> </span>). De veld-naam is om het even welk pre- of user-defined gebied. </p> <p>Als geen <span class="codeph"> sp_x_# </span> parameter voor een bepaalde genummerde vraag wordt verstrekt, worden alle gebieden die als <span class="uicontrol"> Onderzoek door Gebrek </span> worden bepaald zoals die onder <span class="uicontrol"> het Plaatsen </span> &gt; <span class="uicontrol"> Meta-gegevens </span> &gt; <span class="uicontrol"> Definities wordt geplaatst gezocht door die vraag </span> . </p> <p>Bijvoorbeeld, keert het voorleggen van het volgende formulier alle documenten terug die het woord "groot"bevatten die ook het woord "Fitzgerald"op het "auteur"gebied bevatten: </p> <p> <code class="syntax html"> Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="great"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="author"&gt;Search&nbsp;only&nbsp;documents&nbsp;written&nbsp;by:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="Fitzgerald"&gt; </code> </p> <p>U kunt veelvoudige gebiedsnamen met een bepaalde vraag of een genummerde vraag associëren door meer dan één geval van de zelfde <span class="codeph"> sp_x </span> of <span class="codeph"> sp_x_# </span> parameter in één enkel onderzoeksverzoek te verstrekken. </p> <p>Bijvoorbeeld, om naar het woord "bloem"binnen zowel de "lichaam"als "sleutels"gebieden te zoeken, kon u een onderzoeksvorm met de volgende informatie tot stand brengen: </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="body"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="keys"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="flower"&gt; </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Een typisch voorbeeld van het gebruiken van de parameters van het achterste deelonderzoek CGI {#section_260012BBC2514CC9A8E02E53DE8B41EE}

De volgende verbindingsvragen beginnen een onderzoek gebruikend &quot;Muziek&quot;als onderzoeksvraag, en gebruiken alle standaardparameters. Merk op dat URL over twee lijnen voor leesbaarheid wordt verdeeld. In uw HTML, zou deze verbinding allen op één lijn moeten zijn.

```
<a href="https://search.atomz.com/search/?sp_q=Music&sp_a=sp99999999"> 
Testing...</a>
```

De zelfde functionaliteit wordt typisch bepaald met een vorm:

```
<form action="https://search.atomz.com/search/"> 
<input size=12 name="sp_q" value="Music"><br> 
<input type=hidden name="sp_a" value="sp99999999"> 
<input type=submit value="Search"><br> 
</form>
```

U zou standaardparameters typisch moeten gebruiken wanneer het in werking stellen van een onderzoek. Die manier, wordt de eerste pagina getoond, gesorteerd door relevantie, en staat de klant toe om andere pagina&#39;s en andere opties te kiezen. Als de onderzoeksvorm op uw plaats opties voor inzamelingen omvat, ga in de inzamelingsnaam als parameter over.

## Een gedetailleerd voorbeeld van het gebruiken van achterste - eindonderzoekCGI parameters {#section_5FA3C620D5124FB2AB28857F8D8473F6}

De volgende vormvragen tonen `25` resultaten die bij resultaat beginnen `10`. De samenvattingen worden niet getoond, is de soortorde door datum, en de genoemde inzameling `support` wordt gebruikt. Alleen documenten die in de laatste 30 dagen zijn gedateerd, worden teruggestuurd.

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

