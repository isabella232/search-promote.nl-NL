---
description: U kunt output in om het even welk op tekst-gebaseerd formaat, met inbegrip van XML of JSON aanpassen.
seo-description: U kunt output in om het even welk op tekst-gebaseerd formaat, met inbegrip van XML of JSON aanpassen.
seo-title: Begeleide zoekresultaten
solution: Target
title: Begeleide zoekresultaten
topic: Appendices,Site search and merchandising
uuid: 234fd563-f249-42b0-88ca-c89b44f8df77
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a

---


# Begeleide zoekresultaten{#guided-search-output}

U kunt output in om het even welk op tekst-gebaseerd formaat, met inbegrip van XML of JSON aanpassen.

## Het gebruiken van Geleide output van het Onderzoek {#concept_2A1BA3AD413848A1AC2A3ABC4FFE481F}

Het outputformaat is klantgericht om het facetten, het sorteren, en andere implementatie-specifieke besluiten te steunen die tijdens het ontwerpproces worden gemaakt. U kunt het formaat zelf aanpassen om de ontwikkeling van het vooreind van de klant te vereenvoudigen, indien nodig.

De volledige output is bevat binnen `<result>` markeringen, en de meeste dynamische gegevens zijn ingesloten binnen `<![CDATA[ ]]>` markeringen. Dergelijke organisatie staat de resultaten toe om HTML en andere niet-XML entiteiten te bevatten.

Waar de verbindingen met andere pagina&#39;s worden verstrekt, worden zij voorgesteld in de vorm van een relatieve URL. Dit resultaat omvat ook de parameters van het vraagkoord die worden overgegaan om het gewenste resultaat te produceren.

## Begrijpen van een Begeleide implementatie van het Onderzoek {#section_95483980930C4325BAB50A40BD47245A}

Wanneer u met een Begeleide implementatie van het Onderzoek begint herinner dat voor de BedrijfsLaag verantwoordelijk [!DNL Adobe Search&Promote] is. Namelijk de logica die omringt welke resultaten en facetten aan een klant op elk bepaald ogenblik worden getoond.

Wanneer u het de toepassingsvooreind van het Web uitvoert dat ontleedt en de resultaten als HTML toont, beperk de functionaliteit tot slechts vertoning. Met andere woorden, om het even welke server-zijlogica die u gebruikt om de Laag van de Presentatie tot stand te brengen neemt niet de besluiten over wat om aan een klant voor te stellen, tenzij het noodzakelijk is. De bedrijfsregels zullen niet werken aangezien u verwacht als het front-end manuscript de onderzoeksresultaten verandert.

[!DNL Adobe Search&Promote] handhaaft gebruikersstaat van geselecteerde opties van de onderzoeksraffinage als parameters URL. Alle `<link>` knopen bevatten de relevante parameters van de selecties van de klant. Deze parameters kunnen broodkruimel, paginering, soort, en facetselecties omvatten. Waar van toepassing, worden de `<undolink>` knopen teruggegeven om een klant toe te staan &quot;terug te keren&quot;van een selectie. Facets en broodkruimels bieden dit soort verbindingen aan.

## Werken met de zoekserver {#section_8DBEACDECD714E59BDED6315E6041B8D}

Een REST-als API wordt gebruikt dat u kunt in wisselwerking staan met om onderzoeken uit te voeren en resultaten te ontvangen. De gemeenschappelijkste formaten die voor de resultaten worden gebruikt zijn XML of JSON.

De basis URI wordt geassocieerd met een specifieke rekening en een gefaseerd of levend milieu. U kunt veelvoudige aliassen voor de basis URI van uw rekeningsmanager verzoeken. Bijvoorbeeld, heeft een fictief bedrijf genoemd Megacorp de volgende twee basis URLs verbonden aan hun rekening:

* `https://search.megacorp.com `
* `https://stage.megacorp.com`

Eerder URI voert onderzoeken tegen hun levende index en laatstgenoemde URI tegen hun gefaseerde index uit.

De verzoeken van het onderzoek bestaan uit de basis URI en een reeks parameters van CGI of zeer belangrijk-waardeparen die op het gewenste onderzoek naar de rekening wijzen die met de basis URI wordt geassocieerd.

Drie formaten van de parameters van CGI worden gesteund. Door gebrek wordt uw rekening gevormd om de parameters van CGI met een puntkomma () te scheiden, zoals in het volgende voorbeeld: `;`

* `https://search.megacorp.com?q=shoes ;page=2`

Als u verkiest, kunt u uw rekeningsmanager hebben uw rekening vormen om ampersands ( `&`) te gebruiken om de parameters van CGI, zoals in het volgende voorbeeld te scheiden:

* `https://search.megacorp.com?q=shoes &page=2`

Een derde formaat, genoemd het formaat SEO, wordt ook gesteund waar een voorwaartse schuine streep ( `/`) in plaats van de separator en het gelijke teken wordt gebruikt om &quot;schone&quot;verbindingen te produceren, zoals in het volgende voorbeeld:

* `https://search.megacorp.com/q/shoes/page/2`

Om het even welke tijd wordt het formaat SEO gebruikt om een verzoek te verzenden, zijn alle outputverbindingen teruggekeerd in het zelfde formaat.

## Zoekquery-parameters {#section_7ADA5E130E3040C9BE85D0D68EDD3223}

De volgende lijst beschrijft de standaard &quot;uit-van-de-doos&quot;parameters van de onderzoeksvraag die u kunt gebruiken. De regels van de verwerking en de bedrijfsregels kunnen worden gebouwd gebaseerd van user-defined vraagparameters om douane bedrijfslogica uit te voeren die voor uw bedrijf relevant is. U kunt met het het raadplegen team werken om documentatie over die parameters te verkrijgen.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Zoekquery-parameter </p> </th> 
   <th colname="col2" class="entry"> <p>Voorbeeld </p> </th> 
   <th colname="col3" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> q </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> q= string </span> </p> </td> 
   <td colname="col3"> <p> Specificeert het vraagkoord voor het onderzoek. Deze parameter brengt aan de <span class="codeph"> sp_q </span> achterste onderzoeksparameter in kaart. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> q# </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> q#= string </span> </p> </td> 
   <td colname="col3"> <p>De genummerde <span class="codeph"> q </span> en <span class="codeph"> x </span> - parameters verwezenlijken facetten, of het zoeken binnen een bepaald gebied. </p> <p>De <span class="codeph"> q </span> parameter bepaalt de termijn u naar in het facet als overeenkomstige genummerde <span class="codeph"> x </span> - parameterpunten zoekt. Bijvoorbeeld, als u twee facetten hebt die grootte en kleur worden genoemd, kon u iets als het volgende hebben: </p> <p> <span class="codeph"> q1=klein;x1=grootte;q2=rood;x2=kleur </span> </p> <p>Deze parameter brengt aan de parameters van het <span class="codeph"> sp_q_exact_# </span> achterste deelonderzoek in kaart. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> x# </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> x#= string </span> </p> </td> 
   <td colname="col3"> <p> De genummerde <span class="codeph"> q </span> en <span class="codeph"> x </span> - parameters verwezenlijken facetten, of het zoeken binnen een bepaald gebied. </p> <p>De <span class="codeph"> q </span> parameter bepaalt de termijn u naar in het facet als overeenkomstige genummerde <span class="codeph"> x </span> - parameterpunten zoekt. Bijvoorbeeld, als u twee facetten hebt die grootte en kleur worden genoemd, kon u iets als het volgende hebben: </p> <p> <span class="codeph"> q1=klein;x1=grootte;q2=rood;x2=kleur </span> </p> <p>Deze parameter brengt aan de <span class="codeph"> sp_x_# </span> achterste onderzoeksparameters in kaart. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> collectie </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> collectie= string </span> </p> </td> 
   <td colname="col3"> <p> Specificeert de inzameling voor het onderzoek te gebruiken. Deze parameter brengt aan de <span class="codeph"> sp_k </span> achterste onderzoeksparameter in kaart. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tellen </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> count= aantal </span> </p> </td> 
   <td colname="col3"> <p> Specificeert de totale telling van resultaten die worden getoond. Het gebrek wordt bepaald in <span class="uicontrol"> Montages </span> &gt; <span class="uicontrol"> die </span> &gt; <span class="uicontrol"> Onderzoek zoeken </span>. Deze parameter brengt aan de <span class="codeph"> sp_c </span> achterste onderzoeksparameter in kaart. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> pagina </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> page= aantal </span> </p> </td> 
   <td colname="col3"> <p> Specificeert de pagina van resultaten die zijn teruggekeerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rangschikken </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> rank= veld </span> </p> </td> 
   <td colname="col3"> <p> Specificeert het rangschikkingsgebied voor het statische rangschikken te gebruiken. Het veld moet een veld van het type Rank zijn met een relevantie groter dan 0. Deze parameter brengt aan de <span class="codeph"> sp_sr </span> achterste parameter in kaart. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gs_store </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> gs_store= string </span> </p> </td> 
   <td colname="col3"> <p> Specificeert de opslag aan onderzoek. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sorteren </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> sort= getal </span> </p> </td> 
   <td colname="col3"> <p> Specificeert de soortorde. "0" is de standaardwaarde en is de soort volgens relevantiescore; "1" sorteert naar datum; "-1" sorteert niet. </p> <p>De gebruikers kunnen een gebiedsnaam voor de waarde van de <span class="codeph"> sp_s </span> parameter specificeren. Bijvoorbeeld, <span class="codeph"> sp_s=title </span> sorteert resultaten volgens de waarden die in het titelgebied bevat zijn. Wanneer een gebiedsnaam voor de waarde van een <span class="codeph"> sp_s </span> parameter wordt gebruikt, worden de resultaten gesorteerd door dat gebied en dan gesubsorteerd door relevantie. </p> <p>Om deze eigenschap toe te laten, doe het volgende: </p> 
    <ol id="ol_3894F81EA7BF4827A84DE8662111ABEF"> 
     <li id="li_C040C0B88F174A4885E1A8E721FD032A">Voor het productmenu, klik <span class="uicontrol"> Montages </span> &gt; <span class="uicontrol"> Meta-gegevens </span> &gt; <span class="uicontrol"> Definities </span>. </li> 
     <li id="li_2E83C3A46D1B4BF991EABAD9D3E52B7D">Voor de <span class="wintitle"> Gelaagde </span> pagina van Definities, doe één van het volgende: 
      <ul id="ul_8018FEE10E0A4C96A74F84A897080580"> 
       <li id="li_E9A7CE43E2734F4D9522A1283CA111FB">Klik <span class="uicontrol"> toevoegen Nieuw Gebied </span>. </li> 
       <li id="li_9D2434A321924FBD874569CA9AD2EEF7">Klik <span class="uicontrol"> uitgeven </span> voor een bepaalde gebiedsnaam. </li> 
      </ul> </li> 
     <li id="li_90D5E3F4AC0A4A6189934A5589F69903">In de <span class="wintitle"> Sorterende </span> drop-down lijst, klik of <span class="uicontrol"> die </span> of <span class="uicontrol"> Daling oplopend </span>. <p>Deze parameter brengt aan de <span class="codeph"> sp_s </span> achterste onderzoeksparameter in kaart. </p> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

## Integreren met uw systeem {#section_91261B19A44A4E579B3FC9FAB9AD3665}

Het volgende is aanbevelingen voor integratie met uw systeem.

* Communiceren met de zoekserver.

   U kunt met de [!DNL Adobe Search&Promote] Webservers communiceren gebruikend HTTP KRIJGT verzoeken. Uw servers produceren deze verzoeken of op de cliëntkant die een Ajax- verzoek doen.
* De zoekgeschiedenis opslaan.

[!DNL Adobe Search&Promote] is stateless waar de volledige staat in het HTTP- verzoek wordt overgegaan.
* Het ontleden van de teruggekeerde resultaten.

   Men adviseert dat u een op SAX-Gebaseerde syntactische parser van XML gebruikt om de reactie van XML te ontleden. Als u Ajax- verzoek produceert, vorm [!DNL Adobe Search&Promote] om reacties JSON voor die verzoeken terug te keren om het gemakkelijker te maken om de reactie te ontleden.

## De geleide JSON van het Onderzoek Output {#reference_EB8182A564DE4374BB84158F2AABEF74}

Tabellen die de standaard JSON-responsoutput beschrijven.

Zie ook de Geleide Output van JSON van het Onderzoek van het [Onderzoek](../c-appendices/c-guidedsearchoutput.md#reference_EB8182A564DE4374BB84158F2AABEF74).

U kunt de reactie van JSON voor het volgende herzien:

* [Banners](../c-appendices/c-guidedsearchoutput.md#section_88519CAAD25F4BD49D5E517077745B0E)
* [Breadcrumb](../c-appendices/c-guidedsearchoutput.md#section_A7DB0F1DA9ED4CBCAE18395122F3E01E)
* [Facturen](../c-appendices/c-guidedsearchoutput.md#section_65932C95931743A1BFAF1DF16D7E6D92)
* [Koptekst en query](../c-appendices/c-guidedsearchoutput.md#section_1D57062259CA46E0B4F598FA4EB37065)
* [Paginering](../c-appendices/c-guidedsearchoutput.md#section_504E7AB570BD49AF9839530DC438EE96)
* [Recente zoekopdrachten](../c-appendices/c-guidedsearchoutput.md#section_525816A0355C48F8970D89B8FC3F1FFF)
* [Resultaten](../c-appendices/c-guidedsearchoutput.md#section_41AC56BB0A084BF59379B06C8BEF2157)
* [Zoekformulier](../c-appendices/c-guidedsearchoutput.md#section_434DA13EA295474C99FFE9F14801CD0E)
* [Sorteren](../c-appendices/c-guidedsearchoutput.md#section_558853CD376F4D71BACF211D53085D55)
* [Suggesties](../c-appendices/c-guidedsearchoutput.md#section_6EC104E1DDD94AC799B65E6E61A2FB3C)
* [Zones](../c-appendices/c-guidedsearchoutput.md#section_AE53A498B440465EAF2286F2AE87D548)

## Banners {#section_88519CAAD25F4BD49D5E517077745B0E}

Voorbeeld:

```xml
<banners> 
 <banner> 
  <area><![CDATA[top-left]]></area> 
  <content><![CDATA[<img src="https://www.megacorp.com/discount.gif"/>]]></content> 
 </banner> 
</banners>
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Tags in banners </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;banner&gt; </span> </p> </td> 
   <td colname="col2"> <p> Een individuele bannerknoop. U kunt veelvoudige bannerknopen hebben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;area&gt; </span> </p> </td> 
   <td colname="col2"> <p> Het gebied op de Web-pagina waar de banner wordt getoond. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;content&gt; </span> </p> </td> 
   <td colname="col2"> <p> De inhoud van HTML voor het bannergebied. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Breadcrumb {#section_A7DB0F1DA9ED4CBCAE18395122F3E01E}

In het volgende voorbeeld, telkens als de klant verder door de facetten versmalt, wordt de selectie toegevoegd aan de broodkruimel. Elk punt wordt vertegenwoordigd als `<breadcrumb-item>`.

Voorbeeld:

```xml
 <breadcrumb> 
  <breadcrumb-item> 
   <link><![CDATA[?q=new+year]]></link> 
   <value><![CDATA[new year]]></value> 
  </breadcrumb-item> 
  <breadcrumb-item> 
   <link><![CDATA[?q=new+year;q1=Articles;x1=content-type]]></link> 
   <value><![CDATA[Articles]]></value> 
  </breadcrumb-item> 
 </breadcrumb> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Markeringen in Breadcrumb </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p> Een relatieve verbinding aan onderzoeksresultaten die de gewenste mening toont. Het klikken van een broodkruimelverbinding neemt de klant aan een mening waar alle verdere verfijningen worden verwijderd. Andere opties zijn ook beschikbaar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;waarde&gt; </span> </p> </td> 
   <td colname="col2"> <p> Klant-onder ogen ziende tekst voor het broodkruimelpunt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Facturen {#section_65932C95931743A1BFAF1DF16D7E6D92}

De factoren zijn raffinageopties die klanten de capaciteit geven om op de resultaten te filtreren. De factoren worden algemeen gebruikt voor categorisering, prijswaaiers, kleurenselecties, en andere attributenraffinage. De meta-gegevens in de index is wat aandrijvingsfacetten.

Het is gemeenschappelijk om categoriseringsfacetten&#39; te verbergen of te tonen aangezien een klant zich neer door de categorisatie beweegt. Het hoogste niveau van categorisering (categorie) staat bekend als Tier 1. Wanneer een klant op een Tier 1-optie klikt, worden de opties voor Tier 2-verfijning (subcategorie) weergegeven en verdwijnen de opties voor Tier 1. Wanneer een klant op een optie voor niveau 2 klikt, worden de opties voor de verfijning van niveau 3 (subcategorie) weergegeven en verdwijnen de opties voor niveau 2. Zoals hierboven genoteerd, zijn deze opties verborgen en getoond-uw Webtoepassing wordt niet beïnvloed door hen.

Elk facet is bevat binnen `<facet-item>` markeringen. In het volgende voorbeeld, toont het één facet dat de klant toestaat om de onderzoeksresultaten door &quot;vakantie&quot;te raffineren.

Voorbeeld:

```xml
 <facets> 
  <facet-item> 
   <facet-title><![CDATA[Holidays]]></facet-title> 
   <facet-value> 
    <label><![CDATA[New Year]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=New+Year;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[11]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Christmas]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Christmas;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[7]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Chinese New Year]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Chinese+New+Year;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[2]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Thanksgiving]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Thanksgiving;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[2]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[4th of July]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=4th+of+July;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Father&#39;s Day]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Father's+Day;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Hanukkah]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Hanukkah;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Mother&#39;s Day]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Mother's+Day;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Valentine&#39;s Day]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Valentine's+Day;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
  </facet-item> 
  <facet-item> 
   <facet-title><![CDATA[Seasons]]></facet-title> 
   <facet-value> 
    <label><![CDATA[Winter]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Winter;x1=content-type;x2=seasons]]></link> 
    <count><![CDATA[20]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Summer]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Summer;x1=content-type;x2=seasons]]></link> 
    <count><![CDATA[7]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Autumn]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Autumn;x1=content-type;x2=seasons]]></link> 
    <count><![CDATA[4]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Spring]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Spring;x1=content-type;x2=seasons]]></link> 
    <count><![CDATA[2]]></count> 
   </facet-value> 
  </facet-item> 
 </facets> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Markeringen in facetten </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;facettitel&gt; </span> </p> </td> 
   <td colname="col2"> <p> Klantgerichte titel voor het facet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;label&gt; </span> </p> </td> 
   <td colname="col2"> <p> Klantgericht etiket voor de facetoptie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p> Relatieve verbinding aan resultaten die de optie neer raffineert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;count&gt; </span> </p> </td> 
   <td colname="col2"> <p> Het aantal resultaten in die geraffineerde resultaatreeks. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;undolink&gt; </span> </p> </td> 
   <td colname="col2"> <p> Wanneer een facetwaarde wordt geselecteerd keert de knoop "ongedaan maakt verbinding"terug die een klant uit de resultaten laat terug. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Koptekst en query {#section_1D57062259CA46E0B4F598FA4EB37065}

Voorbeeld:

```xml
<result> 
 <query> 
  <user-query><![CDATA[new year]]></user-query> 
  <lower-results><![CDATA[1]]></lower-results> 
  <upper-results><![CDATA[16]]></upper-results> 
  <total-results><![CDATA[621]]></total-results> 
 </query> 
```

Samen gebruikt, stellen deze markeringen een bericht zoals het volgende voor: &quot;Weergegeven resultaten 1-16 van 621 voor &#39;nieuw jaar&#39;.&quot;

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Markeringen in kopbal en vraag </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;user-query&gt; </span> </p> </td> 
   <td colname="col2"> <p> De sleutelwoordvraag die met het verzoek wordt voorgelegd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;lagere resultaten&gt; </span> </p> </td> 
   <td colname="col2"> <p> Het objectnummer van het eerste resultaat op deze pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;bovenste resultaten&gt; </span> </p> </td> 
   <td colname="col2"> <p> Het objectnummer van het laatste resultaat op deze pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;totale resultaten&gt; </span> </p> </td> 
   <td colname="col2"> <p> Het totale aantal resultaten die de gebruikersvraag aanpassen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;aangepast veld&gt; </span> </p> </td> 
   <td colname="col2"> <p> Een facultatief gebied dat globaal op de onderzoeksresultaten van toepassing is. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Paginering {#section_504E7AB570BD49AF9839530DC438EE96}

Voorbeeld:

```xml
<pagination> 
 <total-pages><39></total-pages> 
 <pages> 
   <page position="first"></page> 
   <page position="last">?i=1;page=39;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="previous"></page> 
   <page position="next">?i=1;page=2;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="1" selected="true">?i=1;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="2">?i=1;page=2;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="3">?i=1;page=3;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="4">?i=1;page=4;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="5">?i=1;page=5;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="6">?i=1;page=6;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="7">?i=1;page=7;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="8">?i=1;page=8;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="9">?i=1;page=9;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="10">?i=1;page=10;q=new+year;q1=Articles;x1=content-type]]></page> 
 </pages> 
</pagination> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Markeringen in Paginering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;totaal aantal pagina's&gt; </span> </p> </td> 
   <td colname="col2"> <p> Totaal aantal bladzijden van de resultaten, op basis van het aantal resultaten gedeeld door het aantal resultaten per pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="first"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Bevat een relatieve verbinding aan de eerste pagina in de resultaatreeks, tenzij de klant reeds pagina 1 bekijkt. In dat geval is het leeg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="last"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Bevat een relatieve verbinding aan de laatste pagina in de resultaatreeks, tenzij de klant de laatste pagina bekijkt. In dat geval is het leeg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="Vorige"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Bevat een relatieve verbinding aan de vorige pagina in de resultaatreeks, tenzij de klant pagina 1 bekijkt; in een dergelijk geval is het blanco . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="next"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Bevat een relatieve verbinding aan de laatste pagina in de resultaatreeks, tenzij de klant de laatste pagina bekijkt. In dat geval is het leeg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="x" </span> </p> </td> 
   <td colname="col2"> <p> Bevat een relatieve verbinding aan een bepaald paginaaantal. Tien aaneengesloten paginaaantallen worden getoond. Op bladzijde 1 zou het pagina 1-10 zijn. Aan het eind van het vastgestelde resultaat (in dit geval, 39), zou het pagina 30-39 zijn. Bijvoorbeeld, in het centrum van de resultaatreeks, pagina 15, zou het pagina 11-20 zijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> selected="true"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Toegepast als attribuut op de momenteel geselecteerde pagina. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Recente zoekopdrachten {#section_525816A0355C48F8970D89B8FC3F1FFF}

Recente zoekopdrachten zijn een cookie-gebaseerde functie die alleen werkt als u de cookie-informatie doorgeeft aan de servers.

Voorbeeld:

```xml
<recent-searches> 
 <recent-search> 
  <search-term><![CDATA[shoes]]></search-term> 
  <link><![CDATA[?q=shoes]]></link> 
 </recent-search> 
</recent-searches> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Markeringen in recente zoekopdrachten </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;recent zoeken&gt; </span> </p> </td> 
   <td colname="col2"> <p> Een individuele recent-onderzoeksknoop. U kunt veelvoudige recent-onderzoeksknopen hebben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;zoekterm&gt; </span> </p> </td> 
   <td colname="col2"> <p> De termijn die de klant eerder zocht naar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p> Links naar de vorige zoekopdracht. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Resultaten {#section_41AC56BB0A084BF59379B06C8BEF2157}

De reeks van Resultaten is een klantgericht gebied van de reactie JSON. Elke index is uniek op de gebied noemende mechanismen van meta-gegevens. Er zijn gemeenschappelijke gebieden die voor elk resultaat zoals titel, beschrijving, en URL zijn teruggekeerd. Maar, om het even welke meta-gegevens die voor een pagina in de index worden bepaald kunnen beschikbaar worden om in elke resultaatknoop te gebruiken. De indeling, de prijzen, de kleuren en de miniaturen zijn slechts een paar opties die u op een resultaat kunt toepassen om meer dwingende zoekresultaten te produceren.

Het formaat van Resultaten wordt aangepast gebaseerd op de meta-gegevens die voor uw implementatie specifiek zijn. Om het even welke per-resultaatgegevens voor vertoning in de resultaten, met inbegrip van duimnagelbeeld URLs, is bevat hier.

Bovendien is het mogelijk om veelvoudige resultaatstreken binnen de pagina, zoals &quot;Getoonde Resultaten&quot;te vormen, of afzonderlijke &quot;Producten&quot;en &quot;Inhoud&quot;resultatensecties te vormen. In deze gevallen, worden de veelvoudige resultaatstreken verstrekt binnen HTML, hoewel de facetten slechts met de primaire resultaatreeks worden geassocieerd.

Voorbeeld:

```xml
 <results> 
  <result> 
    <index><![CDATA[1]]></index> 
    <result-title><![CDATA[New Year's Eve Slumber Party]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/new-years-eve-slumber-party-705199/]]></url> 
    <meta-description><![CDATA[Fun New Year's celebration ideas for your kids]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <small-thumbnail-img><![CDATA[https://mysite.com/assets/cms/parties/new-years-eve-

slumber-party-parties-photo-80-FF1200SLEEPA18.jpg]]></small-thumbnail-img> 
    <large-thumbnail-img><![CDATA[https://mysite.com/assets/cms/parties/new-years-eve- 
slumber-party-parties-photo-160-FF1200SLEEPA18.jpg]]></large-thumbnail-img> 
    <byline><![CDATA[Nancy Mades]]></byline> 
    <blurb><![CDATA[Fun New Year's celebration ideas for your kids]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[2]]></index> 
    <result-title><![CDATA[10 Holiday Traditions to Start This Year]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/10-holiday-traditions-to-start-this-year-704781/]]></url> 
    <meta-description><![CDATA[Reader ideas to make Thanksgiving, Christmas, and New Year's even more magical]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <small-thumbnail-img><![CDATA[https://mysite.com/assets/cms/parties/10-holiday- 
traditions-to-start-this-year-parties-photo-80-FF1107HOLIA01.jpg]]></small-thumbnail-img> 
    <large-thumbnail-img><![CDATA[https://mysite.com/assets/cms/parties/10-holiday- 
traditions-to-start-this-year-parties-photo-160-FF1107HOLIA01.jpg]]></large-thumbnail-img> 
    <byline><![CDATA[Julie Taylor]]></byline> 
    <blurb><![CDATA[Reader ideas to make Thanksgiving, Christmas, and New Year's even more magical]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[3]]></index> 
    <result-title><![CDATA[A Perfect New Year's Eve]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/a-perfect-new-years-eve-705258/]]></url> 
    <meta-description><![CDATA[You can turn New Year's into a celebration for the whole family.]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <byline><![CDATA[Teri Keough]]></byline> 
    <blurb><![CDATA[You can turn New Year's into a celebration for the whole family.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[4]]></index> 
    <result-title><![CDATA[New Year's Fun and Games]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/new-years-fun-and-games-705220/]]></url> 
    <meta-description><![CDATA[Craft, game and food ideas for a New Year's celebration with kids.]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <byline><![CDATA[Charlotte Meryman]]></byline> 
    <blurb><![CDATA[Craft, game and food ideas for a New Year's celebration with kids.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[5]]></index> 
    <result-title><![CDATA[11 Great Ways to Start the New Year]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/11-great-ways-to-start-the-new-year-705552/]]></url> 
    <meta-description><![CDATA[11 New Family Traditions to Start This Year from My Magazine]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <byline><![CDATA[Emily Block]]></byline> 
    <blurb><![CDATA[11 New Family Traditions to Start This Year from My Magazine]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[6]]></index> 
    <result-title><![CDATA[Celebrating Chinese New Year]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/celebrating-chinese-new-year-705260/]]></url> 
    <meta-description><![CDATA[Crafts, food, and games to help you celebrate Chinese New Year.]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Crafts, food, and games to help you celebrate Chinese New Year.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[7]]></index> 
    <result-title><![CDATA[New Year's Eve, Family Style]]></result-title> 
    <url><![CDATA[https://mysite.com/holidays/new-years-eve-family-style-701283/]]></url> 
    <meta-description><![CDATA[Start a family New Year's Eve tradition by having an evening of kid-focused fun at home]]></meta-description> 
    <category><![CDATA[holidays]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Start a family New Year's Eve tradition by having an evening of kid-focused fun at home]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[8]]></index> 
    <result-title><![CDATA[Chinese New Year Activities]]></result-title> 
    <url><![CDATA[https://mysite.com/crafts/chinese-new-year-activities-710345/]]></url> 
    <meta-description><![CDATA[Activities for celebrating Chinese New Year.]]></meta-description> 
    <category><![CDATA[crafts]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Activities for celebrating Chinese New Year.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[9]]></index> 
    <result-title><![CDATA[More Organized in the New Year]]></result-title> 
    <url><![CDATA[https://mysite.com/holidays/more-organized-in-the-new-year-701284/]]></url> 
    <meta-description><![CDATA[Tips for getting your household more organized--and getting the kids to help.]]></meta-description> 
    <category><![CDATA[holidays]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Tips for getting your household more organized--and getting your kids to help out.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[10]]></index> 
    <result-title><![CDATA[Checklists: Year-End Safety Checklist]]></result-title> 
    <url><![CDATA[https://mysite.com/holidays/checklists-year-end-safety-checklist-701352/]]></url> 
    <meta-description><![CDATA[Make sure that your home is safe with our year-end safety checklist!]]></meta-description> 
    <category><![CDATA[holidays]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Make sure that your home is safe with our year-end safety checklist!]]></blurb> 
  </result>   
 </results> 
</customer-result> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Markeringen in resultaten </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;index&gt; </span> </p> </td> 
   <td colname="col2"> <p> Het serienummer van het resultaat binnen deze resultaatreeks. In dit voorbeeld, waar tien resultaten per pagina, op pagina 2 van de resultaten worden getoond, zou het eerste punt een index van 11 hebben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;resultaat-titel&gt; </span> </p> </td> 
   <td colname="col2"> <p> De klant-onder ogen ziende titel voor deze pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;url&gt; </span> </p> </td> 
   <td colname="col2"> <p> URL voor deze pagina. Het wordt gebruikt om een hyperlink tot stand te brengen die de klant door de resultaten laat klikken. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Zoekformulier {#section_434DA13EA295474C99FFE9F14801CD0E}

Voorbeeld:

```xml
<search-form> 
 <include-tnt-mbox>1 </included-tnt-mbox> 
 <autocomplete> 
  <css><![CDATA[<!--link rel="stylesheet" type="te 
        xt/css"href="//content.atomz.com/sp000000a8/publish/autoc 
        omplete_styles.css?sp_css_cache_ver=2" /-->]]> 
  </css> 
  <form-content><![CDATA[<div id="autocomplete"></div>]]> 
  </form-content> 
  <js><![CDATA[<script type="text/javascript" 
   src="//content.atomz.com/sp100491de/publish/autoc 
   omplete_data.js?sp_js_cache_ver=3"></script>]]> 
  </js> 
 </autcomplete> 
 <hidden-parameters> 
  <parameter> 
   <name><![CDATA[store]]></name> 
   <value><![CDATA[mens]]></value> 
  </parameter> 
 </hidden-parameters> 
</search-form>
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Markeringen in zoekformulier </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;include-tnt-mbox&gt; </span> </p> </td> 
   <td colname="col2"> <p> Optioneel. Wanneer aanwezig in JSON, wijst een waarde van 1 het erop dat uw rekening met <span class="keyword"> Test&amp;Target </span> verbonden is en minstens één bedrijfsregel heeft die in een test A:B is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;autocomplete&gt; </span> </p> </td> 
   <td colname="col2"> <p> Optioneel. Wanneer het gebruiken van auto-volledig, is deze knoop aanwezig om erop te wijzen dat CSS en JavaScript op de pagina samen met de inhoud aanwezig is die in de vorm is. Deze gebieden veranderen typisch niet tenzij iemand het autocomplete plaatsen heeft veranderd. In dergelijke gevallen, wordt het xxx_cache_ver gebied verhoogd om een ongeldigverklaring van de caching inhoud op browser van uw klant te dwingen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;css&gt; </span> </p> </td> 
   <td colname="col2"> <p> CSS die met autocomplete wordt geassocieerd. Men adviseert dat u deze markering hoog in de pagina plaatst om pagina het teruggeven te verbeteren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;formulierinhoud&gt; </span> </p> </td> 
   <td colname="col2"> <p> Inhoud die binnen uw onderzoek-van voor het autocomplete nut aan haak-omhoog aan de correcte controle wordt vereist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;js&gt; </span> </p> </td> 
   <td colname="col2"> <p> Aangepaste JavaScript die vereist is voor Automatisch aanvullen. Men adviseert dat u deze markering laag in de pagina plaatst om pagina het teruggeven te verbeteren. YUI JavaScript wordt ook vereist voor autocomplete. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;verborgen parameters&gt; </span> </p> </td> 
   <td colname="col2"> <p> Bevat alle verborgen parameters (naam en waarde) om in de onderzoeksvorm te omvatten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Sorteren {#section_558853CD376F4D71BACF211D53085D55}

Het volgende voorbeeld toont de gegevens voor een menu van de drie-optie soort. Het menu staat de klant toe om door relevantie, titel, of classificatie te sorteren. Het momenteel geselecteerde punt omvat een attribuut &quot;selected=true&quot;. &quot;. Bied altijd een relevantieoptie aan om een klant toe te staan om op de standaardonderzoeksresultaten terug te komen die oorspronkelijk werden getoond.

Voorbeeld:

```xml
 <sort> 
  <sort-item selected="true"> 
   <label><![CDATA[Relevance]]></label> 
   <value><![CDATA[relevance]]></value> 
   <link><![CDATA[]]></link> 
  </sort-item> 
  <sort-item> 
   <label><![CDATA[Title]]></label> 
   <value><![CDATA[title]]></value> 
   <link><![CDATA[?q=new+year;q1=Articles;sort=title;x1=content-type]]></link>     
  </sort-item> 
  <sort-item> 
   <label><![CDATA[Rating]]></label> 
   <value><![CDATA[user-rating]]></value> 
   <link><![CDATA[?q=new+year;q1=Articles;sort=user-rating;x1=content-type]]></link>     
  </sort-item> 
 </sort>
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Markeringen in het menu Sorteren </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;label&gt; </span> </p> </td> 
   <td colname="col2"> <p> De klant-onder ogen ziende tekst voor de optie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;waarde&gt; </span> </p> </td> 
   <td colname="col2"> <p> Vertegenwoordigt de waarde van de "soort"parameter van het vraagkoord voor deze optie. Deze markering is niet nodig als de <span class="codeph"> &lt;link&gt; </span> waarde wordt gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p> Voor de niet-geselecteerde opties, bevat de <span class="codeph"> &lt;link&gt; </span> parameter de relatieve verbinding die de zelfde resultaatreeks terugkeert, die door de nieuwe soortparameter wordt gesorteerd. Dit gebied is leeg voor de momenteel geselecteerde soortoptie. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Suggesties {#section_6EC104E1DDD94AC799B65E6E61A2FB3C}

Suggesties worden teruggegeven als er maar een paar resultaten zijn of geen resultaten. Deze knoop bevat termijnen die succesvolle vragen opbrengen en op een pagina van &quot;Geen Resultaten&quot;kunnen worden getoond. De verbinding is ook teruggekeerd zodat kan een klant aan de nieuwe vraag springen.

Voorbeeld:

```xml
 <suggestions> 
  <suggestion-item> 
   <link><![CDATA[?q=video]]></link> 
   <word><![CDATA[video]]> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Markeringen in suggesties </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Een relatieve verbinding die wordt gebruikt om een hyperlink aan onderzoeksresultaten voor de voorsteltermijn tot stand te brengen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;woord&gt; </span> </p> </td> 
   <td colname="col2"> <p>De voorgestelde termijn. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Zones {#section_AE53A498B440465EAF2286F2AE87D548}

Voorbeeld:

```xml
<zones> 
 <zone> 
  <name><![CDATA[best-sellers]]></name> 
  <display><![CDATA[1]]></display> 
 </zone> 
</zones> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Markeringen in zones </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;zone&gt; </span> </p> </td> 
   <td colname="col2"> <p> Een individuele streekknoop. U kunt veelvoudige streekknopen hebben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;naam&gt; </span> </p> </td> 
   <td colname="col2"> <p> De naam van de zone. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;display&gt; </span> </p> </td> 
   <td colname="col2"> <p> 1 of 0 om erop te wijzen als de streek of niet wordt getoond. De daadwerkelijke streekinhoud kan een statisch gebied op uw Web-pagina of in uw onderzoeksresultaten, zoals beste verkopers of verwante producten zijn. </p> </td> 
  </tr> 
 </tbody> 
</table>

## De geleide Output van XML van het Onderzoek {#reference_D93E859A277643068B10AE7A61C973EA}

Lijsten die de standaardde reactieoutput van XML beschrijven.

U kunt de reactie van XML voor het volgende herzien:

* [Banners](../c-appendices/c-guidedsearchoutput.md#section_6A19EC26DD3B494194AAA788151B78B5)
* [Breadcrumb](../c-appendices/c-guidedsearchoutput.md#section_E48A71B0EBDB4EDDA7587009AD865488)
* [Facturen](../c-appendices/c-guidedsearchoutput.md#section_5CEB1F966C004FFEA3CF675638966E25)
* [Koptekst en query](../c-appendices/c-guidedsearchoutput.md#section_802835E19BCB48239C6770A1B72DFFF8)
* [Paginering](../c-appendices/c-guidedsearchoutput.md#section_72DB86DDE1284B1EA295CFFBC16A3150)
* [Recente zoekopdrachten](../c-appendices/c-guidedsearchoutput.md#section_BCA2DDD17F264CF6BA11634E1A514E28)
* [Resultaten](../c-appendices/c-guidedsearchoutput.md#section_EC496F5CA2634158891455E2F6DF6833)
* [Zoekformulier](../c-appendices/c-guidedsearchoutput.md#section_F92D8C3D37174A10A4E26CAFF3F3DF89)
* [Sorteren](../c-appendices/c-guidedsearchoutput.md#section_32DC50A103BF491BA3665A5CADCCAADE)
* [Suggesties](../c-appendices/c-guidedsearchoutput.md#section_D81BCE46F0AF443695DF9C4BA084B716)
* [Zones](../c-appendices/c-guidedsearchoutput.md#section_15D8AA585F3246799968BA88EE2C9FC2)

## Banners {#section_6A19EC26DD3B494194AAA788151B78B5}

Voorbeeld:

```xml
<banners> 
 <banner> 
  <area><![CDATA[top-left]]></area> 
  <content><![CDATA[<img src="https://www.megacorp.com/discount.gif"/>]]></content> 
 </banner> 
</banners>
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Tags in banners </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;banner&gt; </span> </p> </td> 
   <td colname="col2"> <p> Een individuele bannerknoop. U kunt veelvoudige bannerknopen hebben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;area&gt; </span> </p> </td> 
   <td colname="col2"> <p> Het gebied op de Web-pagina waar de banner wordt getoond. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;content&gt; </span> </p> </td> 
   <td colname="col2"> <p> De inhoud van HTML voor het bannergebied. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Breadcrumb {#section_E48A71B0EBDB4EDDA7587009AD865488}

In het volgende voorbeeld, telkens als de klant verder door de facetten versmalt, wordt de selectie toegevoegd aan de broodkruimel. Elk punt wordt vertegenwoordigd als `<breadcrumb-item>`.

Voorbeeld:

```xml
 <breadcrumb> 
  <breadcrumb-item> 
   <link><![CDATA[?q=new+year]]></link> 
   <value><![CDATA[new year]]></value> 
  </breadcrumb-item> 
  <breadcrumb-item> 
   <link><![CDATA[?q=new+year;q1=Articles;x1=content-type]]></link> 
   <value><![CDATA[Articles]]></value> 
  </breadcrumb-item> 
 </breadcrumb> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Markeringen in Breadcrumb </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p> Een relatieve verbinding aan onderzoeksresultaten die de gewenste mening toont. Het klikken van een broodkruimelverbinding neemt de klant aan een mening waar alle verdere verfijningen worden verwijderd. Andere opties zijn ook beschikbaar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;waarde&gt; </span> </p> </td> 
   <td colname="col2"> <p> Klant-onder ogen ziende tekst voor het broodkruimelpunt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Facturen {#section_5CEB1F966C004FFEA3CF675638966E25}

De factoren zijn raffinageopties die klanten de capaciteit geven om op de resultaten te filtreren. De factoren worden algemeen gebruikt voor categorisering, prijswaaiers, kleurenselecties, en andere attributenraffinage. De meta-gegevens in de index is wat aandrijvingsfacetten.

Het is gemeenschappelijk om categoriseringsfacetten&#39; te verbergen of te tonen aangezien een klant zich neer door de categorisatie beweegt. Het hoogste niveau van categorisering (categorie) staat bekend als Tier 1. Wanneer een klant op een Tier 1-optie klikt, worden de opties voor Tier 2-verfijning (subcategorie) weergegeven en verdwijnen de opties voor Tier 1. Wanneer een klant op een optie voor niveau 2 klikt, worden de opties voor de verfijning van niveau 3 (subcategorie) weergegeven en verdwijnen de opties voor niveau 2. Zoals hierboven genoteerd, zijn deze opties verborgen en getoond-uw Webtoepassing wordt niet beïnvloed door hen.

Elk facet is bevat binnen `<facet-item>` markeringen. In het volgende voorbeeld, toont het één facet dat de klant toestaat om de onderzoeksresultaten door &quot;vakantie&quot;te raffineren.

Voorbeeld:

```xml
 <facets> 
  <facet-item> 
   <facet-title><![CDATA[Holidays]]></facet-title> 
   <facet-value> 
    <label><![CDATA[New Year]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=New+Year;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[11]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Christmas]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Christmas;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[7]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Chinese New Year]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Chinese+New+Year;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[2]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Thanksgiving]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Thanksgiving;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[2]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[4th of July]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=4th+of+July;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Father&#39;s Day]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Father's+Day;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Hanukkah]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Hanukkah;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Mother&#39;s Day]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Mother's+Day;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Valentine&#39;s Day]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Valentine's+Day;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
  </facet-item> 
  <facet-item> 
   <facet-title><![CDATA[Seasons]]></facet-title> 
   <facet-value> 
    <label><![CDATA[Winter]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Winter;x1=content-type;x2=seasons]]></link> 
    <count><![CDATA[20]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Summer]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Summer;x1=content-type;x2=seasons]]></link> 
    <count><![CDATA[7]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Autumn]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Autumn;x1=content-type;x2=seasons]]></link> 
    <count><![CDATA[4]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Spring]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Spring;x1=content-type;x2=seasons]]></link> 
    <count><![CDATA[2]]></count> 
   </facet-value> 
  </facet-item>  
 </facets> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Markeringen in facetten </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;facettitel&gt; </span> </p> </td> 
   <td colname="col2"> <p> Klantgerichte titel voor het facet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;label&gt; </span> </p> </td> 
   <td colname="col2"> <p> Klantgericht etiket voor de facetoptie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p> Relatieve verbinding aan resultaten die de optie neer raffineert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;count&gt; </span> </p> </td> 
   <td colname="col2"> <p> Het aantal resultaten in die geraffineerde resultaatreeks. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;undolink&gt; </span> </p> </td> 
   <td colname="col2"> <p> Wanneer een facetwaarde wordt geselecteerd keert de knoop "ongedaan maakt verbinding"terug die een klant uit de resultaten laat terug. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Koptekst en query {#section_802835E19BCB48239C6770A1B72DFFF8}

Voorbeeld:

```xml
<?xml version="1.0" encoding="utf-8" standalone="yes" ?> 
<result> 
 <query> 
  <user-query><![CDATA[new year]]></user-query> 
  <lower-results><![CDATA[1]]></lower-results> 
  <upper-results><![CDATA[16]]></upper-results> 
  <total-results><![CDATA[621]]></total-results> 
 </query> 
```

Samen gebruikt, stellen deze markeringen een bericht zoals het volgende voor: &quot;Weergegeven resultaten 1-16 van 621 voor &#39;nieuw jaar&#39;.&quot;

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Markeringen in Kopbal en Vraag </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;user-query&gt; </span> </p> </td> 
   <td colname="col2"> <p> De sleutelwoordvraag die met het verzoek wordt voorgelegd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;lagere resultaten&gt; </span> </p> </td> 
   <td colname="col2"> <p> Het objectnummer van het eerste resultaat op deze pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;bovenste resultaten&gt; </span> </p> </td> 
   <td colname="col2"> <p> Het objectnummer van het laatste resultaat op deze pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;totale resultaten&gt; </span> </p> </td> 
   <td colname="col2"> <p> Het totale aantal resultaten die de gebruikersvraag aanpassen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;aangepast veld&gt; </span> </p> </td> 
   <td colname="col2"> <p> Een facultatief gebied dat globaal op de onderzoeksresultaten van toepassing is. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Paginering {#section_72DB86DDE1284B1EA295CFFBC16A3150}

Voorbeeld:

```xml
<pagination> 
 <total-pages><39></total-pages> 
 <pages> 
   <page position="first"></page> 
   <page position="last">?i=1;page=39;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="previous"></page> 
   <page position="next">?i=1;page=2;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="1" selected="true">?i=1;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="2">?i=1;page=2;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="3">?i=1;page=3;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="4">?i=1;page=4;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="5">?i=1;page=5;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="6">?i=1;page=6;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="7">?i=1;page=7;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="8">?i=1;page=8;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="9">?i=1;page=9;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="10">?i=1;page=10;q=new+year;q1=Articles;x1=content-type]]></page> 
 </pages> 
</pagination> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Markeringen in Paginering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;totaal aantal pagina's&gt; </span> </p> </td> 
   <td colname="col2"> <p> Totaal aantal bladzijden van de resultaten, op basis van het aantal resultaten gedeeld door het aantal resultaten per pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="first"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Bevat een relatieve verbinding aan de eerste pagina in de resultaatreeks, tenzij de klant reeds pagina 1 bekijkt. In dat geval is het leeg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="last"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Bevat een relatieve verbinding aan de laatste pagina in de resultaatreeks, tenzij de klant de laatste pagina bekijkt. In dat geval is het leeg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="Vorige"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Bevat een relatieve verbinding aan de vorige pagina in de resultaatreeks, tenzij de klant pagina 1 bekijkt; in een dergelijk geval is het blanco . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="next"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Bevat een relatieve verbinding aan de laatste pagina in de resultaatreeks, tenzij de klant de laatste pagina bekijkt. In dat geval is het leeg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="x" </span> </p> </td> 
   <td colname="col2"> <p> Bevat een relatieve verbinding aan een bepaald paginaaantal. Tien aaneengesloten paginaaantallen worden getoond. Op bladzijde 1 zou het pagina 1-10 zijn. Aan het eind van het vastgestelde resultaat (in dit geval, 39), zou het pagina 30-39 zijn. Bijvoorbeeld, in het centrum van de resultaatreeks, pagina 15, zou het pagina 11-20 zijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> selected="true"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Toegepast als attribuut op de momenteel geselecteerde pagina. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Recente zoekopdrachten {#section_BCA2DDD17F264CF6BA11634E1A514E28}

Recente zoekopdrachten zijn een cookie-gebaseerde functie die alleen werkt als u de cookie-informatie doorgeeft aan de servers.

Voorbeeld:

```xml
<recent-searches> 
 <recent-search> 
  <search-term><![CDATA[shoes]]></search-term> 
  <link><![CDATA[?q=shoes]]></link> 
 </recent-search> 
</recent-searches> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Markeringen in recente zoekopdrachten </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;recent zoeken&gt; </span> </p> </td> 
   <td colname="col2"> <p> Een individuele recent-onderzoeksknoop. U kunt veelvoudige recent-onderzoeksknopen hebben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;zoekterm&gt; </span> </p> </td> 
   <td colname="col2"> <p> De termijn die de klant eerder zocht naar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p> Links naar de vorige zoekopdracht. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Resultaten {#section_EC496F5CA2634158891455E2F6DF6833}

De reeks van Resultaten is een klantgericht gebied van de reactie van XML. Elke index is uniek op de gebied noemende mechanismen van meta-gegevens. Er zijn gemeenschappelijke gebieden die voor elk resultaat zoals titel, beschrijving, en URL zijn teruggekeerd. Maar, om het even welke meta-gegevens die voor een pagina in de index worden bepaald kunnen beschikbaar worden om in elke resultaatknoop te gebruiken. De indeling, de prijzen, de kleuren en de miniaturen zijn slechts een paar opties die u op een resultaat kunt toepassen om meer dwingende zoekresultaten te produceren.

Het formaat van Resultaten wordt aangepast gebaseerd op de meta-gegevens die voor uw implementatie specifiek zijn. Om het even welke per-resultaatgegevens voor vertoning in de resultaten, met inbegrip van duimnagelbeeld URLs, is bevat hier.

Bovendien is het mogelijk om veelvoudige resultaatstreken binnen de pagina, zoals &quot;Getoonde Resultaten&quot;te vormen, of afzonderlijke &quot;Producten&quot;en &quot;Inhoud&quot;resultatensecties te vormen. In deze gevallen, worden de veelvoudige resultaatstreken verstrekt binnen HTML, hoewel de facetten slechts met de primaire resultaatreeks worden geassocieerd.

Voorbeeld:

```xml
 <results> 
  <result> 
    <index><![CDATA[1]]></index> 
    <result-title><![CDATA[New Year's Eve Slumber Party]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/new-years-eve-slumber-party-705199/]]></url> 
    <meta-description><![CDATA[Fun New Year's celebration ideas for your kids]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <small-thumbnail-img><![CDATA[https://mysite.com/assets/cms/parties/new-years-eve-

slumber-party-parties-photo-80-FF1200SLEEPA18.jpg]]></small-thumbnail-img> 
    <large-thumbnail-img><![CDATA[https://mysite.com/assets/cms/parties/new-years-eve- 
slumber-party-parties-photo-160-FF1200SLEEPA18.jpg]]></large-thumbnail-img> 
    <byline><![CDATA[Nancy Mades]]></byline> 
    <blurb><![CDATA[Fun New Year's celebration ideas for your kids]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[2]]></index> 
    <result-title><![CDATA[10 Holiday Traditions to Start This Year]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/10-holiday-traditions-to-start-this-year-704781/]]></url> 
    <meta-description><![CDATA[Reader ideas to make Thanksgiving, Christmas, and New Year's even more magical]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <small-thumbnail-img><![CDATA[https://mysite.com/assets/cms/parties/10-holiday- 
traditions-to-start-this-year-parties-photo-80-FF1107HOLIA01.jpg]]></small-thumbnail-img> 
    <large-thumbnail-img><![CDATA[https://mysite.com/assets/cms/parties/10-holiday- 
traditions-to-start-this-year-parties-photo-160-FF1107HOLIA01.jpg]]></large-thumbnail-img> 
    <byline><![CDATA[Julie Taylor]]></byline> 
    <blurb><![CDATA[Reader ideas to make Thanksgiving, Christmas, and New Year's even more magical]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[3]]></index> 
    <result-title><![CDATA[A Perfect New Year's Eve]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/a-perfect-new-years-eve-705258/]]></url> 
    <meta-description><![CDATA[You can turn New Year's into a celebration for the whole family.]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <byline><![CDATA[Teri Keough]]></byline> 
    <blurb><![CDATA[You can turn New Year's into a celebration for the whole family.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[4]]></index> 
    <result-title><![CDATA[New Year's Fun and Games]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/new-years-fun-and-games-705220/]]></url> 
    <meta-description><![CDATA[Craft, game and food ideas for a New Year's celebration with kids.]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <byline><![CDATA[Charlotte Meryman]]></byline> 
    <blurb><![CDATA[Craft, game and food ideas for a New Year's celebration with kids.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[5]]></index> 
    <result-title><![CDATA[11 Great Ways to Start the New Year]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/11-great-ways-to-start-the-new-year-705552/]]></url> 
    <meta-description><![CDATA[11 New Family Traditions to Start This Year from My Magazine]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <byline><![CDATA[Emily Block]]></byline> 
    <blurb><![CDATA[11 New Family Traditions to Start This Year from My Magazine]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[6]]></index> 
    <result-title><![CDATA[Celebrating Chinese New Year]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/celebrating-chinese-new-year-705260/]]></url> 
    <meta-description><![CDATA[Crafts, food, and games to help you celebrate Chinese New Year.]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Crafts, food, and games to help you celebrate Chinese New Year.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[7]]></index> 
    <result-title><![CDATA[New Year's Eve, Family Style]]></result-title> 
    <url><![CDATA[https://mysite.com/holidays/new-years-eve-family-style-701283/]]></url> 
    <meta-description><![CDATA[Start a family New Year's Eve tradition by having an evening of kid-focused fun at home]]></meta-description> 
    <category><![CDATA[holidays]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Start a family New Year's Eve tradition by having an evening of kid-focused fun at home]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[8]]></index> 
    <result-title><![CDATA[Chinese New Year Activities]]></result-title> 
    <url><![CDATA[https://mysite.com/crafts/chinese-new-year-activities-710345/]]></url> 
    <meta-description><![CDATA[Activities for celebrating Chinese New Year.]]></meta-description> 
    <category><![CDATA[crafts]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Activities for celebrating Chinese New Year.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[9]]></index> 
    <result-title><![CDATA[More Organized in the New Year]]></result-title> 
    <url><![CDATA[https://mysite.com/holidays/more-organized-in-the-new-year-701284/]]></url> 
    <meta-description><![CDATA[Tips for getting your household more organized--and getting the kids to help.]]></meta-description> 
    <category><![CDATA[holidays]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Tips for getting your household more organized--and getting your kids to help out.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[10]]></index> 
    <result-title><![CDATA[Checklists: Year-End Safety Checklist]]></result-title> 
    <url><![CDATA[https://mysite.com/holidays/checklists-year-end-safety-checklist-701352/]]></url> 
    <meta-description><![CDATA[Make sure that your home is safe with our year-end safety checklist!]]></meta-description> 
    <category><![CDATA[holidays]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Make sure that your home is safe with our year-end safety checklist!]]></blurb> 
  </result>   
 </results> 
</customer-result> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Markeringen in resultaten </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;index&gt; </span> </p> </td> 
   <td colname="col2"> <p> Het serienummer van het resultaat binnen deze resultaatreeks. In dit voorbeeld, waar tien resultaten per pagina, op pagina 2 van de resultaten worden getoond, zou het eerste punt een index van 11 hebben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;resultaat-titel&gt; </span> </p> </td> 
   <td colname="col2"> <p> De klant-onder ogen ziende titel voor deze pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;url&gt; </span> </p> </td> 
   <td colname="col2"> <p> URL voor deze pagina. Het wordt gebruikt om een hyperlink tot stand te brengen die de klant door de resultaten laat klikken. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Zoekformulier {#section_F92D8C3D37174A10A4E26CAFF3F3DF89}

Voorbeeld:

```xml
<search-form> 
 <include-tnt-mbox>1 </included-tnt-mbox> 
 <autocomplete> 
  <css><![CDATA[<!--link rel="stylesheet" type="te 
        xt/css"href="//content.atomz.com/sp000000a8/publish/autoc 
        omplete_styles.css?sp_css_cache_ver=2" /-->]]> 
  </css> 
  <form-content><![CDATA[<div id="autocomplete"></div>]]> 
  </form-content> 
  <js><![CDATA[<script type="text/javascript" 
   src="//content.atomz.com/sp100491de/publish/autoc 
   omplete_data.js?sp_js_cache_ver=3"></script>]]> 
  </js> 
 </autcomplete> 
 <hidden-parameters> 
  <parameter> 
   <name><![CDATA[store]]></name> 
   <value><![CDATA[mens]]></value> 
  </parameter> 
 </hidden-parameters> 
</search-form>
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Markeringen in zoekformulier </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;include-tnt-mbox&gt; </span> </p> </td> 
   <td colname="col2"> <p> Optioneel. Wanneer aanwezig in XML, wijst een waarde van 1 het erop dat uw rekening met <span class="keyword"> Test&amp;Target </span> verbonden is en minstens één bedrijfsregel heeft die in een test A:B is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;autocomplete&gt; </span> </p> </td> 
   <td colname="col2"> <p> Optioneel. Wanneer het gebruiken van auto-volledig, is deze knoop aanwezig om erop te wijzen dat CSS en JavaScript op de pagina samen met de inhoud aanwezig is die in de vorm is. Deze gebieden veranderen typisch niet tenzij iemand het autocomplete plaatsen heeft veranderd. In dergelijke gevallen, wordt het xxx_cache_ver gebied verhoogd om een ongeldigverklaring van de caching inhoud op browser van uw klant te dwingen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;css&gt; </span> </p> </td> 
   <td colname="col2"> <p> CSS die met autocomplete wordt geassocieerd. Men adviseert dat u deze markering hoog in de pagina plaatst om pagina het teruggeven te verbeteren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;formulierinhoud&gt; </span> </p> </td> 
   <td colname="col2"> <p> Inhoud die binnen uw onderzoek-van voor het autocomplete nut aan haak-omhoog aan de correcte controle wordt vereist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;js&gt; </span> </p> </td> 
   <td colname="col2"> <p> Aangepaste JavaScript die vereist is voor Automatisch aanvullen. Men adviseert dat u deze markering laag in de pagina plaatst om pagina het teruggeven te verbeteren. YUI JavaScript wordt ook vereist voor autocomplete. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;verborgen parameters&gt; </span> </p> </td> 
   <td colname="col2"> <p> Bevat alle verborgen parameters (naam en waarde) om in de onderzoeksvorm te omvatten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Sorteren {#section_32DC50A103BF491BA3665A5CADCCAADE}

Het volgende voorbeeld toont de gegevens voor een menu van de drie-optie soort. Het menu staat de klant toe om door relevantie, titel, of classificatie te sorteren. Het momenteel geselecteerde punt omvat een attribuut &quot;selected=true&quot;. &quot;. Bied altijd een relevantieoptie aan om een klant toe te staan om op de standaardonderzoeksresultaten terug te komen die oorspronkelijk werden getoond.

Voorbeeld:

```xml
 <sort> 
  <sort-item selected="true"> 
   <label><![CDATA[Relevance]]></label> 
   <value><![CDATA[relevance]]></value> 
   <link><![CDATA[]]></link> 
  </sort-item> 
  <sort-item> 
   <label><![CDATA[Title]]></label> 
   <value><![CDATA[title]]></value> 
   <link><![CDATA[?q=new+year;q1=Articles;sort=title;x1=content-type]]></link>     
  </sort-item> 
  <sort-item> 
   <label><![CDATA[Rating]]></label> 
   <value><![CDATA[user-rating]]></value> 
   <link><![CDATA[?q=new+year;q1=Articles;sort=user-rating;x1=content-type]]></link>     
  </sort-item> 
 </sort>
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Markeringen in het menu Sorteren </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;label&gt; </span> </p> </td> 
   <td colname="col2"> <p> De klant-onder ogen ziende tekst voor de optie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;waarde&gt; </span> </p> </td> 
   <td colname="col2"> <p> Vertegenwoordigt de waarde van de "soort"parameter van het vraagkoord voor deze optie. Deze markering is niet nodig als de <span class="codeph"> &lt;link&gt; </span> waarde wordt gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p> Voor de niet-geselecteerde opties, bevat de <span class="codeph"> &lt;link&gt; </span> parameter de relatieve verbinding die de zelfde resultaatreeks terugkeert, die door de nieuwe soortparameter wordt gesorteerd. Dit gebied is leeg voor de momenteel geselecteerde soortoptie. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Suggesties {#section_D81BCE46F0AF443695DF9C4BA084B716}

Suggesties worden teruggegeven als er maar een paar resultaten zijn of geen resultaten. Deze knoop bevat termijnen die succesvolle vragen opbrengen en op een pagina van &quot;Geen Resultaten&quot;kunnen worden getoond. De verbinding is ook teruggekeerd zodat kan een klant aan de nieuwe vraag springen.

Voorbeeld:

```xml
 <suggestions> 
  <suggestion-item> 
   <link><![CDATA[?q=video]]></link> 
   <word><![CDATA[video]]> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Markeringen in suggesties </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Een relatieve verbinding die wordt gebruikt om een hyperlink aan onderzoeksresultaten voor de voorsteltermijn tot stand te brengen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;woord&gt; </span> </p> </td> 
   <td colname="col2"> <p>De voorgestelde termijn. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Zones {#section_15D8AA585F3246799968BA88EE2C9FC2}

Voorbeeld:

```xml
<zones> 
 <zone> 
  <name><![CDATA[best-sellers]]></name> 
  <display><![CDATA[1]]></display> 
 </zone> 
</zones> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Markeringen in zones </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;zone&gt; </span> </p> </td> 
   <td colname="col2"> <p> Een individuele streekknoop. U kunt veelvoudige streekknopen hebben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;naam&gt; </span> </p> </td> 
   <td colname="col2"> <p> De naam van de zone. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;display&gt; </span> </p> </td> 
   <td colname="col2"> <p> 1 of 0 om erop te wijzen als de streek of niet wordt getoond. De daadwerkelijke streekinhoud kan een statisch gebied op uw Web-pagina of in uw onderzoeksresultaten, zoals beste verkopers of verwante producten zijn. </p> </td> 
  </tr> 
 </tbody> 
</table>

## De geleide Output van XML van het Onderzoek voor de Manager van de Ervaring van Adobe {#reference_DBE13C606C3A4BB185DE53F88D0D3048}

Lijsten die de standaardde reactieoutput van XML voor AEM (de Manager van de Ervaring van Adobe) beschrijven.

Zie ook. [De geleide Output van XML van het Onderzoek](../c-appendices/c-guidedsearchoutput.md#reference_D93E859A277643068B10AE7A61C973EA)

U kunt de reactie van XML voor het volgende herzien:

* [Banners](../c-appendices/c-guidedsearchoutput.md#section_B16EDC5533FA4494AC9983AA7357CBE3)
* [Breadcrumbs](../c-appendices/c-guidedsearchoutput.md#section_49EA7043FBE44315A79A4E738BE30114)
* [Aangepaste velden](../c-appendices/c-guidedsearchoutput.md#section_38DD31AFE5DD4263A63644AFF484E0F4)
* [Facturen](../c-appendices/c-guidedsearchoutput.md#section_BE98990E3DD748A1BD4E0CA322314B79)
* [Koptekst](../c-appendices/c-guidedsearchoutput.md#section_5305B1DC5774439485CA0665DB683F9C)
* [Menus en Sorteren](../c-appendices/c-guidedsearchoutput.md#section_A34CBB645DBF4C70A12A5B7E81211295)
* [Paginering](../c-appendices/c-guidedsearchoutput.md#section_E52F81C6A6EB4B8F996157B657EC540F)
* [Vraag](../c-appendices/c-guidedsearchoutput.md#section_3DAA1013F09742869B80F6A361816E6C)
* [Recente zoekopdrachten](../c-appendices/c-guidedsearchoutput.md#section_17F942F6EC07456DABED7A483AC08446)
* [Resultaten](../c-appendices/c-guidedsearchoutput.md#section_155A80B8C4F641678DD9C8F257108412)
* [Zoekformulier](../c-appendices/c-guidedsearchoutput.md#section_9E4B99D4FEDC49629F6C7E866F3A7493)
* [Suggesties](../c-appendices/c-guidedsearchoutput.md#section_2899FACB9AD84F60B3687C1B4EF09E15)
* [Sjabloon](../c-appendices/c-guidedsearchoutput.md#section_1E2BB2F274B04F5491A4CCCC38F507BD)
* [Zones](../c-appendices/c-guidedsearchoutput.md#section_26C4A947E7B1474A8E37D86D9579B93E)

## Banners {#section_B16EDC5533FA4494AC9983AA7357CBE3}

Het onderzoek/de merchandising van de plaats kunnen de banners van een klant beheren, die de banners in diverse delen op een Web-pagina stoppen.

Voorbeeld banner:

Het volgende is een voorbeeld van een banner die in het gebied van de pagina&#39;s genoemd &quot;bovenkant&quot;wordt geplaatst.

```xml
   <banners> 
       <banner> 
           <area><![CDATA[top]]></area> 
           <content><![CDATA[<div style="color:#70A100">We have custom shipping</div>]]></content> 
       </banner> 
    </banners> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Node </p> </th> 
   <th colname="col2" class="entry"> <p>Ouderlijke node </p> </th> 
   <th colname="col3" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>banners </p> </td> 
   <td colname="col2"> <p>klantresultaten </p> </td> 
   <td colname="col3"> <p>Bevat 0-n bannerknopen die elk bannergebied en de inhoud aanduiden die in dat gebied wordt gestopt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>banner </p> </td> 
   <td colname="col2"> <p>banners </p> </td> 
   <td colname="col3"> <p>Een individuele bannerknoop. U kunt veelvoudige bannerknopen hebben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>gebied </p> </td> 
   <td colname="col2"> <p>banner </p> </td> 
   <td colname="col3"> <p>Het gebied op de Web-pagina waar de banner wordt getoond. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>inhoud </p> </td> 
   <td colname="col2"> <p>banner </p> </td> 
   <td colname="col3"> <p>De bannerinhoud. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Breadcrumbs {#section_49EA7043FBE44315A79A4E738BE30114}

Meerdere broodkruimels worden ondersteund. U kunt broodkruimels en hun overeenkomstig gedrag in **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Breadcrumbs]** bepalen. Ook, moet u een unieke naam voor elke broodkruimel toewijzen die u bepaalt. De knoop van broodkruimelsXML herhaalt over elk van uw bepaalde broodkruimels. Het wordt geadviseerd dat u slechts één broodkruimel in uw onderzoek-resultaten toont.

In het volgende voorbeeld, telkens als de klant verder door de facetten versmalt, wordt de selectie toegevoegd aan de broodkruimel. Elk punt wordt vertegenwoordigd als `<breadcrumb-item>`.

Voorbeeld broodkruimelknooppunt:

```xml
    <breadcrumbs> 
  <breadcrumb> 
            <name><![CDATA[default]]></name> 
     <breadcrumb-item> 
   <link><![CDATA[?i=1;q=mens;sp_cs=UTF-8;view=xml]]></link> 
   <value><![CDATA[mens]]></value> 
                <label><![CDATA[]]></label> 
      </breadcrumb-item> 
     <breadcrumb-item> 
   <link><![CDATA[?i=1;q=mens;q1=Channel;sp_cs=UTF-8;view=xml;x1=brand]]></link> 
   <value><![CDATA[Channel]]></value> 
                <label><![CDATA[brand]]></label> 
      </breadcrumb-item> 
   </breadcrumb> 
    </breadcrumbs> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Node </p> </th> 
   <th colname="col2" class="entry"> <p>Ouderlijke node </p> </th> 
   <th colname="col3" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>broodkruimels </p> </td> 
   <td colname="col2"> <p>klantresultaten </p> </td> 
   <td colname="col3"> <p> Bevat 0-n breadcrumb knopen die elke broodkruimel bepalen. De meeste klanten hebben slechts één broodkruimel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>broodkruimel </p> </td> 
   <td colname="col2"> <p>broodkruimels </p> </td> 
   <td colname="col3"> <p> Bevat de kindknopen die de definitie van een broodkruimel bepalen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>naam </p> </td> 
   <td colname="col2"> <p>broodkruimel </p> </td> 
   <td colname="col3"> <p> De naam van de broodkruimel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>broodkruimel </p> </td> 
   <td colname="col2"> <p>Een individueel punt binnen de broodkruimel. Elk punt wijst op een stap in het spoor aangezien de gebruiker onderaan de resultaatreeks vernauwt. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>koppeling </p> </td> 
   <td colname="col2"> <p>broodkruimel </p> </td> 
   <td colname="col3"> <p> Een relatieve verbinding aan onderzoeksresultaten die de gewenste mening toont. Het klikken van een broodkruimelverbinding neemt de klant aan een mening waar alle verdere verfijningen worden verwijderd. Andere opties zijn ook beschikbaar zoals daling en verwijder. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>waarde </p> </td> 
   <td colname="col2"> <p>broodkruimel </p> </td> 
   <td colname="col3"> <p> Klant-onder ogen ziende tekst voor het broodkruimelpunt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>label </p> </td> 
   <td colname="col2"> <p>broodkruimel </p> </td> 
   <td colname="col3"> <p> De etiketmarkeringoutput een etiket voor een broodkruimelwaarde detailleert die facet werd geselecteerd om dat broodkruimelpunt te produceren. Het wordt slechts gebruikt in de context van een geleid-broodkruimelblok. Voor de stap van de vraagtermijn is dit leeg. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Aangepaste velden {#section_38DD31AFE5DD4263A63644AFF484E0F4}

De gebieden van de douane is een diverse inzameling van variabelen met een globale context. Het wordt typisch gebruikt om over variabelen voor SEO doeleinden over te gaan die in de meta-gegevens van de pagina van onderzoeksresultaten worden geplaatst.

De knoop van de douanegebieden van het voorbeeld:

```xml
    <custom-fields> 
        <custom-field name="seo-search-title"><![CDATA[Geometrixx Search Results]]></custom-field> 
        <custom-field name="seo-search-keywords"><![CDATA[]]></custom-field> 
    </custom-fields> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Node </p> </th> 
   <th colname="col2" class="entry"> <p>Ouderlijke node </p> </th> 
   <th colname="col3" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>aangepaste velden </p> </td> 
   <td colname="col2"> <p>klantresultaten </p> </td> 
   <td colname="col3"> <p> Kan 0-n kindknopen bevatten die douanegebieden bepalen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>aangepast veld </p> </td> 
   <td colname="col2"> <p>aangepaste velden </p> </td> 
   <td colname="col3"> <p> Optioneel. Bevat een waarde voor een bepaald die douanegebied door de naamattributen wordt vermeld. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Facturen {#section_BE98990E3DD748A1BD4E0CA322314B79}

De factoren zijn raffinageopties die klanten de capaciteit geven om op de resultaten te filtreren. De factoren worden algemeen gebruikt voor categorisering, prijswaaiers, kleurenselecties, en andere attributenraffinage. De factoren worden voortgebouwd bovenop de meta-gegevens in de index.

Het is gemeenschappelijk om categoriseringsfacetten&#39; te verbergen of te tonen aangezien een klant zich neer door de categorisatie beweegt. Het hoogste niveau van categorisering (categorie) staat bekend als Tier 1. Wanneer een klant op een Tier 1-optie klikt, worden de opties voor Tier 2-verfijning (subcategorie) weergegeven en verdwijnen de opties voor Tier 1. Wanneer een klant op een Tier 2-optie klikt, worden de opties voor de raffinage van Tier 3 (subcategorie) weergegeven en verdwijnen de opties voor Tier 2. Zoals hierboven vermeld, worden deze opties verborgen en getoond; uw Webtoepassing beïnvloedt hen niet.

Elk facet is bevat binnen `<facet-item>` markeringen. In het volgende voorbeeld, toont het één facet dat de klant de onderzoeksresultaten door &quot;vakantie&quot;laat raffineren.

Voorbeeld van een facetblok:

```xml
<facets>          
     <facet> 
         <facet-title><![CDATA[Department]]></facet-title> 
                <behavior><![CDATA[sticky]]></behavior> 
                <selected>1</selected> 
                <undo-link><![CDATA[?i=1;lang=enus;q=*;q1=Armora+Jeans;sp_staged=1;view=xml;x1=brand]]></undo-link> 
      <facet-value> 
          <selected><![CDATA[true]]></selected> 
              <label><![CDATA[Mens]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Armora+Jeans;q2=Mens;sp_staged=1;view=xml;x1=brand;x2=leveli]]></link> 
       <count><![CDATA[3]]></count> 
                        <undolink><![CDATA[?i=1;lang=enus;q=*;q1=Armora+Jeans;sp_staged=1;view=xml;x1=brand]]></undolink> 
      </facet-value> 
      </facet> 
     <facet> 
         <facet-title><![CDATA[Sub-Category]]></facet-title> 
                <behavior><![CDATA[sticky]]></behavior> 
                <selected>0</selected> 
      <facet-value>           
              <label><![CDATA[Apparel]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans;q3=Apparel;sp_staged=1;view=xml;x1=leveli;x2=brand;x3=levelii]]></link> 
       <count><![CDATA[3]]></count>                         
      </facet-value>   
      </facet>         
     <facet> 
         <facet-title><![CDATA[Brand]]></facet-title> 
                <behavior><![CDATA[multi-select]]></behavior> 
                <selected>1</selected> 
                <undo-link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;sp_staged=1;view=xml;x1=leveli]]></undo-link> 
      <facet-value>        
              <label><![CDATA[Amoura]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans|Amoura;sp_staged=1;view=xml;x1=leveli;x2=brand]]></link> 
       <count><![CDATA[9]]></count>                         
      </facet-value>   
      <facet-value>         
              <label><![CDATA[Armora]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans|Armora;sp_staged=1;view=xml;x1=leveli;x2=brand]]></link> 
       <count><![CDATA[12]]></count>                        
      </facet-value>   
      <facet-value> 
          <selected><![CDATA[true]]></selected> 
              <label><![CDATA[Armora Jeans]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans|Armora+Jeans;sp_staged=1;view=xml;x1=leveli;x2=brand]]></link> 
 
       <count><![CDATA[3]]></count> 
                        <undolink><![CDATA[?i=1;lang=enus;q=*;q1=Mens;sp_staged=1;view=xml;x1=leveli]]></undolink> 
      </facet-value>   
      <facet-value>           
              <label><![CDATA[Art of Grooming]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans|Art+of+Grooming;sp_staged=1;view=xml;x1=leveli;x2=brand]]></link> 
       <count><![CDATA[4]]></count>                         
      </facet-value>   
      <facet-value>          
              <label><![CDATA[Bear Co.]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans|Bear+Co.;sp_staged=1;view=xml;x1=leveli;x2=brand]]></link> 
       <count><![CDATA[1]]></count> 
      </facet-value> 
      <facet-value>      
              <label><![CDATA[Citizens]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans|Citizens;sp_staged=1;view=xml;x1=leveli;x2=brand]]></link> 
       <count><![CDATA[4]]></count> 
      </facet-value> 
      <facet-value> 
              <label><![CDATA[D&amp;B]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans|D%26B;sp_staged=1;view=xml;x1=leveli;x2=brand]]></link> 
       <count><![CDATA[17]]></count> 
      </facet-value> 
      <facet-value> 
              <label><![CDATA[David Yuri]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans|David+Yuri;sp_staged=1;view=xml;x1=leveli;x2=brand]]></link> 
       <count><![CDATA[2]]></count>    
      </facet-value>   
      </facet> 
    </facets> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Node </p> </th> 
   <th colname="col2" class="entry"> <p>Ouderlijke node </p> </th> 
   <th colname="col3" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>facetten </p> </td> 
   <td colname="col2"> <p>klantresultaten </p> </td> 
   <td colname="col3"> <p>De knoop van de containerfacetten die 0-n kindknopen heeft die elk facet vertegenwoordigen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>facet </p> </td> 
   <td colname="col2"> <p>facetten </p> </td> 
   <td colname="col3"> <p> Eén facetinstantie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>facettitel </p> </td> 
   <td colname="col2"> <p>facet </p> </td> 
   <td colname="col3"> <p>Klantgerichte titel voor het facet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>gedrag </p> </td> 
   <td colname="col2"> <p>facet </p> </td> 
   <td colname="col3"> <p>Het gedrag van de facet. Bijvoorbeeld, normaal, kleverig, of multi-uitgezochte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>geselecteerd </p> </td> 
   <td colname="col2"> <p>facet </p> </td> 
   <td colname="col3"> <p>1 als het facet een geselecteerde waarde anders 0 heeft. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>loskoppelen </p> </td> 
   <td colname="col2"> <p>facet </p> </td> 
   <td colname="col3"> <p> Alleen aanwezig wanneer het facet is geselecteerd. De verbinding ongedaan maken keert het gehele facet terug. Bijvoorbeeld, wanneer het een multi-uitgezochte facet is, schrapt het alle geselecteerde opties voor het facet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>facetwaarde </p> </td> 
   <td colname="col2"> <p>facet </p> </td> 
   <td colname="col3"> <p>Bevat alle individuele facetartikelen die tot het facet behoren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>geselecteerd </p> </td> 
   <td colname="col2"> <p>facetwaarde </p> </td> 
   <td colname="col3"> <p>Als het huidige punt met het facet wordt geselecteerd, is deze knoop aanwezig en geplaatst aan "waar". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>label </p> </td> 
   <td colname="col2"> <p>facetwaarde </p> </td> 
   <td colname="col3"> <p>Klantgericht etiket voor de facetoptie. Door gebrek zou dit reeds door HTML-ontsnapt moeten zijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>koppeling </p> </td> 
   <td colname="col2"> <p>facetwaarde </p> </td> 
   <td colname="col3"> <p> Relatieve link naar resultaten die de optie verder verfijnt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>tellen </p> </td> 
   <td colname="col2"> <p>facetwaarde </p> </td> 
   <td colname="col3"> <p>Het aantal resultaten in die geraffineerde resultaatreeks. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>loskoppelen </p> </td> 
   <td colname="col2"> <p>facetwaarde </p> </td> 
   <td colname="col3"> <p>Wanneer een facetwaarde wordt geselecteerd keert de knoop "ongedaan maakt verbinding"terug die een klant uit het selecteren van die individuele facetselectie laat. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Koptekst {#section_5305B1DC5774439485CA0665DB683F9C}

Voorbeeld:

```xml
xml version="1.0" encoding="utf-8" standalone="yes" 
```

## Menus en Sorteren {#section_A34CBB645DBF4C70A12A5B7E81211295}

De menu&#39;s voor het sorteren van de resultaten worden gesteund, en veranderend het aantal resultaten per pagina terug te keren. Het steunt ook een navigatiemenu dat nuttig is om &quot;onderzoek als navigatie&quot;te gebruiken. Een rekening kan veelvoudige menu&#39;s van het zelfde type bepalen en om het even welke menu&#39;s voor hun presentatie gebruiken.

De menusknoop van het voorbeeld:

Het volgende voorbeeld toont de gegevens voor een menu van de drie-optie soort en navigatiemenu. Het soortmenu staat de klant toe om door relevantie, titel, of classificatie te sorteren. Het momenteel geselecteerde punt omvat een attribuut &quot;selected=true&quot;. &quot;. Bied altijd een relevantieoptie aan om een klant toe te staan om op de standaardonderzoeksresultaten terug te komen die oorspronkelijk werden getoond.

```xml
<menus> 
        <menu> 
           <name><![CDATA[sort]]></name>         
             <item selected="true"> 
          <label><![CDATA[Relevance]]></label> 
          <value><![CDATA[relevance]]></value> 
          <link><![CDATA[ ]]></link> 
             </item> 
             <item> 
          <label><![CDATA[Lowest Price]]></label> 
          <value><![CDATA[Price]]></value> 
          <link><![CDATA[?i=1;q=mens;sort=Price;sp_cs=UTF-8;sp_staged=1;view=xml]]></link>     
             </item> 
             <item> 
          <label><![CDATA[Highest Price]]></label> 
          <value><![CDATA[Price_r]]></value> 
          <link><![CDATA[?i=1;q=mens;sort=Price_r;sp_cs=UTF-8;sp_staged=1;view=xml]]></link>     
             </item> 
             <item> 
          <label><![CDATA[Brand]]></label> 
          <value><![CDATA[brand]]></value> 
          <link><![CDATA[?i=1;q=mens;sort=brand;sp_cs=UTF-8;sp_staged=1;view=xml]]></link>     
             </item> 
        </menu> 
        <menu> 
            <name><![CDATA[ss_head_nav]]></name>   
                    <item> 
                        <label><![CDATA[WOMEN'S]]></label> 
          <value><![CDATA[?q1=Womens;sp_sfvl_field=levelii|leveli|brand|leveliii;x=0;x1=leveli;y=0;view=nav;top=1]]></value> 
          <link><![CDATA[?q1=Womens;sp_sfvl_field=levelii|leveli|brand|leveliii;x=0;x1=leveli;y=0;view=nav;top=1;i=1;m_ss_head_nav=WOMEN'S]]></link> 
                    </item> 
                    <item> 
                        <label><![CDATA[MEN'S]]></label> 
          <value><![CDATA[/q1/Mens/x1/leveli/view/nav/top/1/]]></value> 
          <link><![CDATA[/q1/Mens/x1/leveli/view/nav/top/1/]]></link> 
                    </item> 
                    <item> 
                        <label><![CDATA[JEWELRY & ACCESSORIES]]></label> 
          <value><![CDATA[?q1=Jewelry+%26+Accessories&sp_sfvl_field=levelii|leveli|brand|leveliii&x1=leveli&view=nav&top=1]]></value> 
          <link><![CDATA[?q1=Jewelry+%26+Accessories&sp_sfvl_field=levelii|leveli|brand|leveliii&x1=leveli&view=nav&top=1;i=1;m_ss_head_nav=JEWELRY+%26+ACCESSORIES]]></link> 
                    </item> 
                    <item> 
                        <label><![CDATA[BEAUTY & FRAGRANCE]]></label> 
          <value><![CDATA[?q1=Beauty+%26+Fragrance;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1]]></value> 
          <link><![CDATA[?q1=Beauty+%26+Fragrance;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1;i=1;m_ss_head_nav=BEAUTY+%26+FRAGRANCE]]></link> 
                    </item> 
                    <item> 
                        <label><![CDATA[GIFTS & HOME]]></label> 
          <value><![CDATA[?q1=Gifts+%26+Home;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1]]></value> 
          <link><![CDATA[?q1=Gifts+%26+Home;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1;i=1;m_ss_head_nav=GIFTS+%26+HOME]]></link> 
                    </item> 
                    <item> 
                        <label><![CDATA[CHILDREN & TOYS]]></label> 
          <value><![CDATA[?q1=Children+%26+Toys;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1]]></value> 
          <link><![CDATA[?q1=Children+%26+Toys;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1;i=1;m_ss_head_nav=CHILDREN+%26+TOYS]]></link> 
                    </item> 
                    <item> 
                        <label><![CDATA[ELECTRONICS]]></label> 
          <value><![CDATA[?q1=Electronics+%26+Toys;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1]]></value> 
          <link><![CDATA[?q1=Electronics+%26+Toys;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1;i=1;m_ss_head_nav=ELECTRONICS]]></link> 
                    </item> 
        </menu> 
    </menus> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Node </p> </th> 
   <th colname="col2" class="entry"> <p>Ouderlijke node </p> </th> 
   <th colname="col3" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>menus </p> </td> 
   <td colname="col2"> <p>klantresultaten </p> </td> 
   <td colname="col3"> <p>Bevat 0-n kindknopen die elk menu bepalen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>menu </p> </td> 
   <td colname="col2"> <p>menus </p> </td> 
   <td colname="col3"> <p>Enige instantie van een menu (beantwoordt aan een menu dat in <span class="uicontrol"> Ontwerp </span> &gt; <span class="uicontrol"> Navigatie </span> &gt; <span class="uicontrol"> Menu's </span>) wordt bepaald. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>naam </p> </td> 
   <td colname="col2"> <p>menu </p> </td> 
   <td colname="col3"> <p>Naam van het menu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>object </p> </td> 
   <td colname="col2"> <p>menu </p> </td> 
   <td colname="col3"> <p>Bepaalt elk punt in het menu. Het optionele kenmerk is ingesteld op true als het bepaalde menu-item momenteel is geselecteerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>label </p> </td> 
   <td colname="col2"> <p>object </p> </td> 
   <td colname="col3"> <p>De klant-onder ogen ziende tekst voor het menupunt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>waarde </p> </td> 
   <td colname="col2"> <p>object </p> </td> 
   <td colname="col3"> <p>Vertegenwoordigt de waarde van het menupunt (de waarde van de vraagparameter die het menu ook wordt geplaatst). Deze markering is niet nodig als de waarde &lt;link&gt; wordt gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>koppeling </p> </td> 
   <td colname="col2"> <p>object </p> </td> 
   <td colname="col3"> <p>Voor de niet-geselecteerde opties, bevat de &lt;link&gt; parameter de relatieve verbinding die de zelfde resultaatreeks terugkeert, maar met de toegepaste menuoptie. Dit gebied is leeg voor de momenteel geselecteerde soortoptie. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Paginering {#section_E52F81C6A6EB4B8F996157B657EC540F}

De reeksen van resultaten zijn verdeeld over verscheidene pagina&#39;s. Typisch tonen de klanten 10 - 20 resultaten op één enkele pagina. De verdere resultaten worden getoond op de volgende pagina. De paginering XML laat u een reeks navigatiekoppelingen bouwen zodat uw klanten, pagina door pagina, door de resultaatreeksen kunnen doorbladeren. Er zijn vier beschikbare navigatiekoppelingen: eerst, laatste, volgende, en vorige. Elk type van verbinding laat klanten zich snel door de pagina&#39;s bewegen zodat kunnen zij herzien en raffineren wat zij zoeken, gemakkelijk.

Het volgende voorbeeld toont de paginering voor een onderzoek dat op de eerste pagina met de paginering is die wordt gevormd om verbindingen aan vijf pagina&#39;s te tonen.

Voorbeeld pagineren:

```xml
    <pagination> 
        <total-pages><![CDATA[112]]></total-pages> 
        <pages> 
     <page position="first"><![CDATA[]]></page> 
     <page position="last"><![CDATA[?i=1;page=112;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page> 
     <page position="next"><![CDATA[?i=1;page=2;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page> 
            <page position="1" selected="true"><![CDATA[?i=1;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page> 
            <page position="2"><![CDATA[?i=1;page=2;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page> 
            <page position="3"><![CDATA[?i=1;page=3;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page> 
            <page position="4"><![CDATA[?i=1;page=4;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page> 
            <page position="5"><![CDATA[?i=1;page=5;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page> 
        </pages> 
    </pagination> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Node </p> </th> 
   <th colname="col2" class="entry"> <p>Ouderlijke node </p> </th> 
   <th colname="col3" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>paginering </p> </td> 
   <td colname="col2"> <p>klantresultaten </p> </td> 
   <td colname="col3"> <p> Totaal aantal bladzijden van de resultaten, op basis van het aantal resultaten gedeeld door het aantal resultaten per pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>totaal aantal pagina's </p> </td> 
   <td colname="col2"> <p>paginering </p> </td> 
   <td colname="col3"> <p>Het totale aantal pagina's dat de onderzoeksresultaten over worden verspreid. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>pagina's </p> </td> 
   <td colname="col2"> <p>paginering </p> </td> 
   <td colname="col3"> <p>Bevat 0-n paginaknopen die elke pagina in de paginering bepalen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>pagina </p> </td> 
   <td colname="col2"> <p>pagina's </p> </td> 
   <td colname="col3"> <p>Vier speciale paginaknopen bestaan: eerst, laatste, vorige, en volgende. Deze vier pagina's zijn facultatief en verschijnen in de resultaatreeks slechts als zij steek houden. Bijvoorbeeld, als u op pagina 1 bent, is er geen "vorige"verbinding. Alle andere pagina's wijzen op een positie. Het aantal pagina's dat vermeld is hangt van het "aantal verbindingen aan pagina's"af dat in het pagineringsgebruikersinterface wordt gevormd. Het "geselecteerde"attribuut wijst op de pagina de klant momenteel is. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Vraag {#section_3DAA1013F09742869B80F6A361816E6C}

De vraagknoop van het voorbeeld:

```xml
    <query> 
        <user-query><![CDATA[mens]]></user-query> 
 <lower-results><![CDATA[1]]></lower-results> 
 <upper-results><![CDATA[12]]></upper-results> 
 <total-results><![CDATA[265]]></total-results> 
    </query> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Node </p> </th> 
   <th colname="col2" class="entry"> <p>Ouderlijke node </p> </th> 
   <th colname="col3" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>query </p> </td> 
   <td colname="col2"> <p>klantresultaten </p> </td> 
   <td colname="col3"> <p> Een globale knoop die een overzicht van de vraag verstrekt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>gebruikersquery </p> </td> 
   <td colname="col2"> <p>query </p> </td> 
   <td colname="col3"> <p> Het sleutelwoord dat werd gezocht naar. Als <span class="uicontrol"> Bedoelde u </span> automatisch naar een voorgestelde termijn toe te schrijven aan de originele termijn die geen resultaten oplevert, wordt het weerspiegeld in het nieuwe sleutelwoord dat werd gezocht naar (zie de suggesties knoop om het originele sleutelwoord te krijgen). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>lagere resultaten </p> </td> 
   <td colname="col2"> <p>query </p> </td> 
   <td colname="col3"> <p> Het objectnummer van het eerste resultaat op deze pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>bovenste resultaten </p> </td> 
   <td colname="col2"> <p>query </p> </td> 
   <td colname="col3"> <p> Het objectnummer van het laatste resultaat op deze pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>totaalresultaten </p> </td> 
   <td colname="col2"> <p>query </p> </td> 
   <td colname="col3"> <p> Het totale aantal resultaten die de gebruikersvraag aanpassen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Recente zoekopdrachten {#section_17F942F6EC07456DABED7A483AC08446}

Recente zoekopdrachten zijn een cookie-gebaseerde functie die alleen werkt als u de cookie-informatie doorgeeft aan zoekservers/verkopers op de site.

Voorbeeld van recente zoekopdrachten:

```xml
    <recent-searches> 
        <clear-link><![?q=womens&gscr=clear]]></clear-link> 
        <recent-search> 
            <link><![?q=mens]]></link> 
            <label><![CDATA[mens]]></label> 
        <recent-search> 
    </recent-searches> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Node </p> </th> 
   <th colname="col2" class="entry"> <p>Ouderlijke node </p> </th> 
   <th colname="col3" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>recente zoekopdrachten </p> </td> 
   <td colname="col2"> <p>klantresultaten </p> </td> 
   <td colname="col3"> <p>De knoop is slechts aanwezig als het onderzoek recente onderzoeken heeft. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>duidelijke koppeling </p> </td> 
   <td colname="col2"> <p>recente zoekopdrachten </p> </td> 
   <td colname="col3"> <p>De relatieve weg die alle recente onderzoeken van de klant ontruimt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>recent onderzoek </p> </td> 
   <td colname="col2"> <p>recente zoekopdrachten </p> </td> 
   <td colname="col3"> <p>Bepaalt in recente onderzoeken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>koppeling </p> </td> 
   <td colname="col2"> <p>recent onderzoek </p> </td> 
   <td colname="col3"> <p>De weg om een verbinding tot stand te brengen die een onderzoek uitvoert dat de gebruiker onlangs uitvoerde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>label </p> </td> 
   <td colname="col2"> <p>recent onderzoek </p> </td> 
   <td colname="col3"> <p>Klant staat voor weergave-label voor de recente zoekopdracht. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Resultaten {#section_155A80B8C4F641678DD9C8F257108412}

De reeks van Resultaten is een klantgericht gebied van de reactie van XML. Elke index is uniek op de gebied noemende mechanismen van meta-gegevens. Er zijn gemeenschappelijke gebieden die voor elk resultaat zoals titel, beschrijving, en URL zijn teruggekeerd. Maar, om het even welke meta-gegevens die voor een pagina in de index worden bepaald kunnen beschikbaar worden om in elke resultaatknoop te gebruiken. De indeling, de prijzen, de kleuren en de miniaturen zijn slechts een paar opties die u op een resultaat kunt toepassen om meer dwingende zoekresultaten te produceren.

Het resultaatformaat wordt aangepast gebaseerd op de meta-gegevens die voor uw implementatie specifiek zijn. Om het even welke per-resultaatgegevens voor vertoning in de resultaten, met inbegrip van duimnagelbeeld URLs, is bevat hier.

Bovendien is het mogelijk om veelvoudige resultaatstreken binnen de pagina, zoals &quot;Getoonde Resultaten&quot;te vormen, of afzonderlijke &quot;Producten&quot;en &quot;Inhoud&quot;resultatensecties te vormen. In deze gevallen, worden de veelvoudige resultaatstreken verstrekt binnen HTML, hoewel de facetten slechts met de primaire resultaatreeks worden geassocieerd.

De resultatenknoop van het voorbeeld:

```xml
    <results> 
        <result-set> 
            <name><![CDATA[default]]></name> 
         <result> 
                    <field name="index"><![CDATA[1]]></field> 
                    <field name="sku"><![CDATA[200190]]></field> 
                    <field name="pagename"><![CDATA[Relaxed Paint Splattered]]></field> 
 
                    <field name="img_sm_url"><![CDATA[https://geometrixx.com/images/08_geometrixx_icon_men.jpg]]></field> 
      <field name="brand"><![CDATA[Armora Jeans]]></field> 
      <field name="price"><![CDATA[195]]></field> 
      <field name="foundIn"><![CDATA[Mens,  
            Apparel,  
          Denim]]></field> 
         </result>   
         <result> 
                    <field name="index"><![CDATA[2]]></field> 
                    <field name="sku"><![CDATA[200195]]></field> 
                    <field name="pagename"><![CDATA[Tumbled Jeans]]></field> 
 
                    <field name="img_sm_url"><![CDATA[https://geometrixx.com/images/08_geometrixx_icon_men.jpg]]></field> 
      <field name="brand"><![CDATA[Armora Jeans]]></field> 
      <field name="price"><![CDATA[235]]></field> 
      <field name="foundIn"><![CDATA[Mens,  
            Apparel,  
          Denim]]></field> 
         </result>    
         <result> 
                    <field name="index"><![CDATA[3]]></field> 
                    <field name="sku"><![CDATA[200196]]></field> 
                    <field name="pagename"><![CDATA[Montana Relaxed]]></field> 
 
                    <field name="img_sm_url"><![CDATA[https://geometrixx.com/images/08_geometrixx_icon_men.jpg]]></field> 
      <field name="brand"><![CDATA[Armora Jeans]]></field> 
      <field name="price"><![CDATA[220]]></field> 
      <field name="foundIn"><![CDATA[Mens,  
            Apparel,  
          Denim]]></field> 
         </result>         
        </result-set>   
    </results> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Node </p> </th> 
   <th colname="col2" class="entry"> <p>Ouderlijke node </p> </th> 
   <th colname="col3" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>resultaten </p> </td> 
   <td colname="col2"> <p>klantresultaten </p> </td> 
   <td colname="col3"> <p>De containerknoop voor 0-n resultaatreeksen. De nul resultaatreeksen betekent dat u op een speciale geen-resultaten landende pagina bent. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>resultaat-set </p> </td> 
   <td colname="col2"> <p>resultaten </p> </td> 
   <td colname="col3"> <p>Een inkomend onderzoek kan veelvoudige onderzoeken ontslaan. Elke resultaat-reeks bevat de resultaten voor een specifiek genoemd onderzoek dat werd uitgevoerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>naam </p> </td> 
   <td colname="col2"> <p>resultaat-set </p> </td> 
   <td colname="col3"> <p>De naam van het onderzoek dat de resultaatreeks tot behoort. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>resultaat </p> </td> 
   <td colname="col2"> <p>resultaat-set </p> </td> 
   <td colname="col3"> <p>Bevat alle gebieden die met een individueel resultaat voor de resultaatreeks worden geassocieerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>veld </p> </td> 
   <td colname="col2"> <p>resultaat </p> </td> 
   <td colname="col3"> <p>Het naamattribuut bepaalt de naam van het gebied binnen de index die wordt getoond. De waarde is de daadwerkelijke waarde voor dat gebied. Sommige resultaten kunnen ontbrekende gebieden hebben die niet relevant voor dat individuele resultaat zijn. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Zoekformulier {#section_9E4B99D4FEDC49629F6C7E866F3A7493}

De Vorm van het onderzoek is inbegrepen in het resultaat dat wordt geplaatst om klanten te laten hun onderzoeksvorm dynamisch bouwen. Deze stap is facultatief. De meeste klanten hebben een vast onderzoeksformulier. Nochtans, staat het klanten toe om te bepalen als de onderzoeksvorm een Test&amp;Target doos vergt, die op het hebben van minstens één bedrijfsregel wordt gebaseerd die een test A:B doet. Op dezelfde manier staat het klanten toe om de recentste autocomplete CSS en JavaScript automatisch op te nemen.

Voorbeeld van zoekformulier XML:

```xml
    <search-form> 
        <include-tnt-mbox>1</include-tnt-mbox> 
        <autocomplete> 
            <enabled>1</enabled> 
            <css><![CDATA[<link rel="stylesheet" type="text/css" href="https://content.t1.atomz.com/sp10043554/stage/autocomplete_styles.css?sp_js_param=2" /> 
]]></css> 
 
            <form-content><![CDATA[<div id="autocomplete"></div> 
<input type="hidden" name="sp_staged" id="sp_staged" value="1" /> 
]]></form-content> 
            <javascript><![CDATA[<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/yui/2.6.0/build/utilities/utilities.js"></script> 
<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/yui/2.6.0/build/datasource/datasource-min.js"></script> 
<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/yui/2.6.0/build/autocomplete/autocomplete-min.js"></script> 
<script type="text/javascript" src="https://content.t1.atomz.com/sp10043554/stage/autocomplete_data.js?sp_js_param=3"></script>]]></javascript> 
        </autocomplete> 
    </search-form> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Node </p> </th> 
   <th colname="col2" class="entry"> <p>Ouderlijke node </p> </th> 
   <th colname="col3" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>zoekformulier </p> </td> 
   <td colname="col2"> <p>klantresultaten </p> </td> 
   <td colname="col3"> <p>Bevat gegevens voor het drijven van de onderzoeksvorm. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>met inlegdoos </p> </td> 
   <td colname="col2"> <p> zoekformulier </p> </td> 
   <td colname="col3"> <p>Technisch gezien vereist u slechts een doos in de onderzoeksvorm wanneer u minstens één bedrijfsregel hebt die een test&amp;Doel A:B doet test. Deze knoop wijst op als u een doos nodig hebt of niet toestaand u om de aantalklappen op de servers van de Test&amp;Doel te verminderen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>autocompleet </p> </td> 
   <td colname="col2"> <p>zoekformulier </p> </td> 
   <td colname="col3"> <p>Kinderknooppunt van woningen gerelateerd aan autocompleet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ingeschakeld </p> </td> 
   <td colname="col2"> <p>autocompleet </p> </td> 
   <td colname="col3"> <p>Reeks aan 1 wanneer de onderzoeksrekening autocomplete gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>css </p> </td> 
   <td colname="col2"> <p> autocompleet </p> </td> 
   <td colname="col3"> <p> CSS voor autocomplete. Plaats deze knoop zo hoog op de pagina zo hoog mogelijk. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> vorminhoud </p> </td> 
   <td colname="col2"> <p>autocompleet </p> </td> 
   <td colname="col3"> <p>Inhoud die in het zoekformulier wordt geïnjecteerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>javascript </p> </td> 
   <td colname="col2"> <p>autocompleet </p> </td> 
   <td colname="col3"> <p>JavaScript voor autocomplete. Plaats deze knoop zo laag mogelijk op de pagina. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Suggesties {#section_2899FACB9AD84F60B3687C1B4EF09E15}

De klanten kunnen **[!UICONTROL Did You Mean]** functionaliteit op drie manieren vormen: suggesties doen omdat er geen resultaten zijn, automatisch zoeken naar de eerste suggestie als we geen resultaten hebben, of suggesties doen als gevolg van lage resultaten (waar de suggesties een hoger resultaat hebben). Alle suggesties leveren resultaten op.

Deze suggesties knoop bevat de termijnen die succesvolle vragen opbrengen. De verbinding is ook teruggekeerd zodat kan een klant aan de nieuwe vraag springen.

Voorbeeld output voor het doen van suggestie toe te schrijven aan 0 resultaten:

```xml
    <suggestions> 
        <auto-searched>0</auto-searched> 
        <suggestions-low-results>0</suggestions-low-results> 
 <suggestion-item> 
     <link><![CDATA[?i=1;q=arcade;sp_cs=UTF-8;view=xml]]></link> 
     <word><![CDATA[arcade]]></word> 
 </suggestion-item>    
    </suggestions>
```

De output van het voorbeeld voor automatisch het zoeken tegen een suggestie:

```xml
    <suggestions> 
        <auto-searched>1</auto-searched> 
        <orig-query><![CDATA[arcace]]></orig-query> 
        <suggestions-low-results>0</suggestions-low-results>         
    </suggestions> 
```

De output van het voorbeeld voor het doen van suggestie toe te schrijven aan lage resultaten:

```xml
   <suggestions> 
        <auto-searched>0</auto-searched> 
        <suggestions-low-results>1</suggestions-low-results> 
 <suggestion-item> 
     <link><![CDATA[?i=1;q=coffee;sp_cs=UTF-8;view=xml]]></link> 
     <word><![CDATA[coffee]]></word> 
 </suggestion-item>  
    </suggestions> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Node </p> </th> 
   <th colname="col2" class="entry"> <p>Ouderlijke node </p> </th> 
   <th colname="col3" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>suggestie </p> </td> 
   <td colname="col2"> <p>klantresultaten </p> </td> 
   <td colname="col3"> <p> Bevat kindknopen die suggestie bepalen, als om het even welk bestaan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>automatisch doorzocht </p> </td> 
   <td colname="col2"> <p>suggesties </p> </td> 
   <td colname="col3"> <p> Indien aanwezig, wijst erop als de plaatsonderzoek/de handel van de plaats automatisch tegen een nieuwe termijn wegens geen resultaten wordt gezocht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>orig-query </p> </td> 
   <td colname="col2"> <p>suggesties </p> </td> 
   <td colname="col3"> <p> Wanneer de plaatsonderzoek/de handel drijvende automatisch onderzoeken tegen de eerste suggestie, de gebruiker-vraag in de vraagknoop het sleutelwoord toont dat wordt gezocht tegen. Deze knoop toont de originele vraagtermijn. Het combineren van twee laat klanten tot structuren zoals "het zoeken naar plaats in plaats van ruimte"leiden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>met suggesties en lage resultaten </p> </td> 
   <td colname="col2"> <p>suggesties </p> </td> 
   <td colname="col3"> <p>Indien aanwezig, wijst erop als de plaatsonderzoek/de handel van de plaats suggesties toe te schrijven aan de huidige onderzoekstermijn lage resultaten oplevert en een suggestie die aanzienlijk hogere resultaten oplevert. De twee drempels zijn configureerbaar in <span class="uicontrol"> Bedoelde u </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>suggestie-item </p> </td> 
   <td colname="col2"> <p>suggesties </p> </td> 
   <td colname="col3"> <p>Bevat 0-n knopen die de diverse suggesties aanduiden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>koppeling </p> </td> 
   <td colname="col2"> <p>suggestie-item </p> </td> 
   <td colname="col3"> <p>Bevat de weg voor het creëren van een verbinding aan de voorgestelde termijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>woord </p> </td> 
   <td colname="col2"> <p>suggestie-item </p> </td> 
   <td colname="col3"> <p> Bevat het voorgestelde woord. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Sjabloon {#section_1E2BB2F274B04F5491A4CCCC38F507BD}

De capaciteit om een ervaring van het klantenonderzoek te schakelen die op de resultaten wordt gebaseerd wordt gesteund. Een deel van dit impliceert omschakeling tussen verschillende malplaatjes met een verschillende lay-out van onderzoeksresultaten. Bijvoorbeeld, kunt u een malplaatje met een netmening van producten voor hebben wanneer u veel producten hebt. Of, u kunt een &quot;schijnwerper&quot;malplaatje hebben wanneer het tonen van één enkel resultaat dat meer details heeft. Je kunt ook een template zonder resultaten hebben als een zoekopdracht geen resultaten oplevert. De malplaatjeknoop wijst op welk malplaatje wordt gebruikt om de onderzoeksresultaten te tonen.

Voorbeeldsjabloon:

```xml
<template><![CDATA[grid]]></template>
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Node </p> </th> 
   <th colname="col2" class="entry"> <p>Ouderlijke node </p> </th> 
   <th colname="col3" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>sjabloon </p> </td> 
   <td colname="col2"> <p>klantresultaten </p> </td> 
   <td colname="col3"> <p>Wijst op de naam van het malplaatje dat wordt gebruikt om de onderzoeksresultaten te tonen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Zones {#section_26C4A947E7B1474A8E37D86D9579B93E}

De gebieden zijn secties van de pagina&#39;s die door bedrijfsregels kunnen worden aangezet of worden uitgezet. Een streek kan om het even welke inhoud omvatten omvatten, maar niet beperkt tot, facetten, onderzoeken, broodkruimels, statische inhoud. De streken op de klantenWeb-pagina zouden aan de zelfde gebieden moeten in kaart brengen zoals plaatsonderzoek/merchandising.

Voorbeeld van zoneknopen:

```xml
    <zones> 
        <zone> 
            <name><![CDATA[brand-facet]]></name> 
            <display>1</display> 
        </zone> 
    </zones> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Node </p> </th> 
   <th colname="col2" class="entry"> <p>Ouderlijke node </p> </th> 
   <th colname="col3" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>zones </p> </td> 
   <td colname="col2"> <p>klantresultaten </p> </td> 
   <td colname="col3"> <p>Bevat 0-n streken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>zone </p> </td> 
   <td colname="col2"> <p>zones </p> </td> 
   <td colname="col3"> <p> Een individuele streekknoop. U kunt veelvoudige streekknopen hebben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>naam </p> </td> 
   <td colname="col2"> <p>zone </p> </td> 
   <td colname="col3"> <p>De naam van de zone. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>weergeven </p> </td> 
   <td colname="col2"> <p>1 of 0, erop wijzend als de streek die aan de streeknaam beantwoordt wordt getoond of verborgen. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Voorbeelden {#reference_64B7D8D228AF4B8D90EDF4DE507B0F84}

De output van het voorbeeld voor een * onderzoek op een fictieve website genoemd Geometrixx en een malplaatje van de voorbeeldpresentatie dat wordt gebruikt om de voorbeeldoutput te veroorzaken.

* [Voorbeeld van uitvoer](../c-appendices/c-guidedsearchoutput.md#section_515C000A18B847D59097D0A9CCC02636)
* [Voorbeeldpresentatiesjabloon](../c-appendices/c-guidedsearchoutput.md#section_AD42571DFB88491AA7F0FDF0929EBE97)

## Voorbeeld van uitvoer {#section_515C000A18B847D59097D0A9CCC02636}

De output van het voorbeeld voor een * onderzoek op een fictieve website genoemd Geometrixx.

```xml
<?xml version="1.0" encoding="utf-8" standalone="yes" ?> 
<customer-results> 
    <query> 
        <user-query><![CDATA[*]]></user-query> 
 <lower-results><![CDATA[1]]></lower-results> 
 <upper-results><![CDATA[12]]></upper-results> 
 <total-results><![CDATA[1337]]></total-results> 
    </query> 
 
    <custom-fields> 
 
        <custom-field name="seo-search-title"><![CDATA[Geometrixx Search Results]]></custom-field> 
        <custom-field name="seo-search-keywords"><![CDATA[]]></custom-field> 
    </custom-fields> 
 
    <menus> 
 
        <menu> 
           <name>sort</name>

             <item selected="true"> 
 
          <label><![CDATA[Relevance]]></label> 
          <value><![CDATA[relevance]]></value> 
          <link><![CDATA[ ]]></link> 
             </item>

             <item> 
          <label><![CDATA[Lowest Price]]></label> 
          <value><![CDATA[Price]]></value> 
          <link><![CDATA[?i=1;q=*;sort=Price;sp_cs=UTF-8;sp_staged=1;view=xml]]></link>     
             </item>

             <item> 
          <label><![CDATA[Highest Price]]></label> 
          <value><![CDATA[Price_r]]></value> 
          <link><![CDATA[?i=1;q=*;sort=Price_r;sp_cs=UTF-8;sp_staged=1;view=xml]]></link>     
             </item>

             <item> 
          <label><![CDATA[Brand]]></label> 
          <value><![CDATA[brand]]></value> 
          <link><![CDATA[?i=1;q=*;sort=brand;sp_cs=UTF-8;sp_staged=1;view=xml]]></link>     
             </item>

        </menu> 
        <menu> 
            <name><![CDATA[ss_head_nav]]></name>

                    <label><![CDATA[WOMEN'S]]></label> 
      <value><![CDATA[?q1=Womens;sp_sfvl_field=levelii|leveli|brand|leveliii;x=0;x1=leveli;y=0;view=nav;top=1]]></value> 
      <link><![CDATA[?q1=Womens;sp_sfvl_field=levelii|leveli|brand|leveliii;x=0;x1=leveli;y=0;view=nav;top=1;i=1;m_ss_head_nav=WOMEN'S]]></link>

                    <label><![CDATA[MEN'S]]></label> 
      <value><![CDATA[/q1/Mens/x1/leveli/view/nav/top/1/]]></value> 
      <link><![CDATA[/q1/Mens/x1/leveli/view/nav/top/1/]]></link>

                    <label><![CDATA[JEWELRY & ACCESSORIES]]></label> 
      <value><![CDATA[?q1=Jewelry+%26+Accessories&sp_sfvl_field=levelii|leveli|brand|leveliii&x1=leveli&view=nav&top=1]]></value> 
      <link><![CDATA[?q1=Jewelry+%26+Accessories&sp_sfvl_field=levelii|leveli|brand|leveliii&x1=leveli&view=nav&top=1;i=1;m_ss_head_nav=JEWELRY+%26+ACCESSORIES]]></link>

                    <label><![CDATA[BEAUTY & FRAGRANCE]]></label> 
      <value><![CDATA[?q1=Beauty+%26+Fragrance;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1]]></value> 
      <link><![CDATA[?q1=Beauty+%26+Fragrance;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1;i=1;m_ss_head_nav=BEAUTY+%26+FRAGRANCE]]></link>

                    <label><![CDATA[GIFTS & HOME]]></label> 
      <value><![CDATA[?q1=Gifts+%26+Home;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1]]></value> 
      <link><![CDATA[?q1=Gifts+%26+Home;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1;i=1;m_ss_head_nav=GIFTS+%26+HOME]]></link>

                    <label><![CDATA[CHILDREN & TOYS]]></label> 
      <value><![CDATA[?q1=Children+%26+Toys;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1]]></value> 
      <link><![CDATA[?q1=Children+%26+Toys;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1;i=1;m_ss_head_nav=CHILDREN+%26+TOYS]]></link>

                    <label><![CDATA[ELECTRONICS]]></label> 
      <value><![CDATA[?q1=Electronics+%26+Toys;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1]]></value> 
      <link><![CDATA[?q1=Electronics+%26+Toys;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1;i=1;m_ss_head_nav=ELECTRONICS]]></link>

        </menu> 
    </menus> 
 
    <breadcrumbs> 
  <breadcrumb> 
            <name><![CDATA[default]]></name> 
       
  <breadcrumb-item> 
    <link><![CDATA[?i=1;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></link> 
    <value><![CDATA[*]]></value> 
                        <label><![CDATA[]]></label> 
   </breadcrumb-item> 
          
   </breadcrumb> 
 
    </breadcrumbs> 
 
    <suggestions> 
        <auto-searched>0</auto-searched> 
         
        <suggestions-low-results>0</suggestions-low-results> 
         
    </suggestions> 
 
    <pagination> 
        <total-pages><![CDATA[112]]></total-pages> 
 
        <pages> 
     <page position="first"><![CDATA[]]></page> 
     <page position="last"><![CDATA[?i=1;page=112;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page> 
      
     <page position="next"><![CDATA[?i=1;page=2;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page>

                <page position="1" selected="true"><![CDATA[?i=1;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page>

                <page position="2"><![CDATA[?i=1;page=2;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page>

                <page position="3"><![CDATA[?i=1;page=3;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page>

                <page position="4"><![CDATA[?i=1;page=4;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page>

                <page position="5"><![CDATA[?i=1;page=5;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page>

        </pages> 
    </pagination> 
 
    <facets>  
         
     <facet-item> 
         <facet-title><![CDATA[Department]]></facet-title> 
                <selected>0</selected>

      <facet-value> 
           
              <label><![CDATA[Womens]]></label> 
 
       <link><![CDATA[?i=1;q=*;q1=Womens;sp_cs=UTF-8;sp_staged=1;view=xml;x1=leveli]]></link> 
       <count><![CDATA[219]]></count> 
                         
      </facet-value> 
   
      <facet-value> 
           
              <label><![CDATA[Mens]]></label> 
       <link><![CDATA[?i=1;q=*;q1=Mens;sp_cs=UTF-8;sp_staged=1;view=xml;x1=leveli]]></link> 
       <count><![CDATA[202]]></count> 
                         
      </facet-value> 
   
      <facet-value>

              <label><![CDATA[Beauty &amp; Fragrance]]></label> 
       <link><![CDATA[?i=1;q=*;q1=Beauty+%26+Fragrance;sp_cs=UTF-8;sp_staged=1;view=xml;x1=leveli]]></link> 
       <count><![CDATA[169]]></count> 
                         
      </facet-value> 
   
      <facet-value> 
           
              <label><![CDATA[Children &amp; Toys]]></label> 
       <link><![CDATA[?i=1;q=*;q1=Children+%26+Toys;sp_cs=UTF-8;sp_staged=1;view=xml;x1=leveli]]></link> 
       <count><![CDATA[209]]></count> 
                         
      </facet-value>

      <facet-value> 
           
              <label><![CDATA[Electronics &amp; Toys]]></label> 
       <link><![CDATA[?i=1;q=*;q1=Electronics+%26+Toys;sp_cs=UTF-8;sp_staged=1;view=xml;x1=leveli]]></link> 
       <count><![CDATA[200]]></count> 
                         
      </facet-value> 
   
      <facet-value> 
           
              <label><![CDATA[Gifts &amp; Home]]></label> 
       <link><![CDATA[?i=1;q=*;q1=Gifts+%26+Home;sp_cs=UTF-8;sp_staged=1;view=xml;x1=leveli]]></link> 
       <count><![CDATA[156]]></count>

      </facet-value> 
   
      <facet-value> 
           
              <label><![CDATA[Jewelry &amp; Accessories]]></label> 
       <link><![CDATA[?i=1;q=*;q1=Jewelry+%26+Accessories;sp_cs=UTF-8;sp_staged=1;view=xml;x1=leveli]]></link> 
       <count><![CDATA[182]]></count> 
                         
      </facet-value> 
   
      </facet-item> 
  
    </facets> 
 
    <results> 
        <result-set> 
            <name><![CDATA[default]]></name> 
               
         <result> 
                    <field name="index"><![CDATA[1]]></field> 
      <field name="brand"><![CDATA[Citizens]]></field> 
      <field name="price"><![CDATA[149]]></field> 
      <field name="foundIn"><![CDATA[Womens,  
            Apparel,  
          Denim]]></field> 
         </result>   
        
         <result> 
 
                    <field name="index"><![CDATA[2]]></field> 
      <field name="brand"><![CDATA[One For All]]></field> 
      <field name="price"><![CDATA[145]]></field> 
      <field name="foundIn"><![CDATA[Womens,  
            Apparel,  
          Denim]]></field> 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[3]]></field> 
      <field name="brand"><![CDATA[Citizens]]></field> 
      <field name="price"><![CDATA[208]]></field> 
 
      <field name="foundIn"><![CDATA[Womens,  
            Apparel,  
          Denim]]></field> 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[4]]></field> 
      <field name="brand"><![CDATA[Vera Watson]]></field> 
      <field name="price"><![CDATA[850]]></field> 
      <field name="foundIn"><![CDATA[Womens,  
            Dresses,  
          Day]]></field> 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[5]]></field> 
 
      <field name="brand"><![CDATA[Ray Laredo]]></field> 
      <field name="price"><![CDATA[195]]></field> 
      <field name="foundIn"><![CDATA[Children &amp; Toys,  
            Apparel,  
          Boys Toddler (2T-4T)]]></field> 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[6]]></field> 
      <field name="brand"><![CDATA[Ray Laredo]]></field> 
      <field name="price"><![CDATA[80]]></field> 
      <field name="foundIn"><![CDATA[Children &amp; Toys,  
            Apparel,  
          Boys Toddler (2T-4T)]]></field> 
 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[7]]></field> 
      <field name="brand"><![CDATA[Petrol]]></field> 
      <field name="price"><![CDATA[85]]></field> 
      <field name="foundIn"><![CDATA[Children &amp; Toys,  
            Apparel,  
          Boys Toddler (2T-4T)]]></field> 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[8]]></field> 
      <field name="brand"><![CDATA[Woolberry]]></field> 
 
      <field name="price"><![CDATA[280]]></field> 
      <field name="foundIn"><![CDATA[Children &amp; Toys,  
            Apparel,  
          Boys Toddler (2T-4T)]]></field> 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[9]]></field> 
      <field name="brand"><![CDATA[Petrol]]></field> 
      <field name="price"><![CDATA[149]]></field> 
      <field name="foundIn"><![CDATA[Children &amp; Toys,  
            Apparel,  
          Boys Toddler (2T-4T)]]></field> 
         </result>   
        
         <result> 
 
                    <field name="index"><![CDATA[10]]></field> 
      <field name="brand"><![CDATA[Ray Laredo]]></field> 
      <field name="price"><![CDATA[55]]></field> 
      <field name="foundIn"><![CDATA[Children &amp; Toys,  
            Apparel,  
          Boys Toddler (2T-4T)]]></field> 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[11]]></field> 
      <field name="brand"><![CDATA[Petrol]]></field> 
      <field name="price"><![CDATA[45]]></field> 
 
      <field name="foundIn"><![CDATA[Children &amp; Toys,  
            Apparel,  
          Boys Toddler (2T-4T)]]></field> 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[12]]></field> 
      <field name="brand"><![CDATA[Ray Laredo]]></field> 
      <field name="price"><![CDATA[47]]></field> 
      <field name="foundIn"><![CDATA[Children &amp; Toys,  
            Apparel,  
          Boys Toddler (2T-4T)]]></field> 
         </result>   
      
        </result-set>   
    </results>

    <banners> 
         
            <banner> 
                <area><![CDATA[top]]></area> 
                <content><![CDATA[<div style="color:#70A100">We have custom shipping</div>]]></content> 
            </banner>

    </banners> 
 
    <zones> 
        <zone> 
 
            <name><![CDATA[brand-facet]]></name> 
            <display>1</display> 
        </zone> 
    </zones> 
 
    <search-form> 
        <include-tnt-mbox>1</include-tnt-mbox> 
        <autocomplete> 
 
            <enabled>1</enabled> 
            <css><![CDATA[<link rel="stylesheet" type="text/css" href="https://content.t1.atomz.com/sp10043554/stage/autocomplete_styles.css?sp_js_param=2" /> 
]]></css> 
            <form-content><![CDATA[<div id="autocomplete"></div> 
<input type="hidden" name="sp_staged" id="sp_staged" value="1" /> 
]]></form-content> 
            <javascript><![CDATA[<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/yui/2.6.0/build/utilities/utilities.js"></script> 
<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/yui/2.6.0/build/datasource/datasource-min.js"></script> 
<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/yui/2.6.0/build/autocomplete/autocomplete-min.js"></script> 
<script type="text/javascript" src="https://content.t1.atomz.com/sp10043554/stage/autocomplete_data.js?sp_js_param=3"></script>]]></javascript> 
        </autocomplete> 
    </search-form> 
 
</customer-results> 
```

## Voorbeeldpresentatiesjabloon {#section_AD42571DFB88491AA7F0FDF0929EBE97}

Het volgende is een malplaatje van de voorbeeldpresentatie dat wordt gebruikt om de voorbeeldoutput hierboven te veroorzaken.

```xml
<?xml version="1.0" encoding="utf-8" standalone="yes" ?> 
<customer-results> 
    <query> 
        <user-query><![CDATA[<guided-query-param gsname="q" />]]></user-query> 
 <lower-results><![CDATA[<guided-results-lower>]]></lower-results> 
 <upper-results><![CDATA[<guided-results-upper>]]></upper-results> 
 <total-results><![CDATA[<guided-results-total>]]></total-results> 
    </query> 
 
    <custom-fields> 
        <custom-field name="seo-search-title"><![CDATA[Geometrixx Search Results]]></custom-field> 
        <custom-field name="seo-search-keywords"><![CDATA[<guided-general-field gsname="default" field="seo_search_keywords"/>]]></custom-field> 
    </custom-fields> 
 
    <menus> 
 
        <menu> 
           <name>sort</name> 
     <guided-menu gsname="sort"> 
         <guided-if-menu-item-selected> 
             <item selected="true"> 
          <label><![CDATA[<guided-menu-item-label />]]></label> 
          <value><![CDATA[<guided-menu-item-value />]]></value> 
          <link><![CDATA[ ]]></link> 
             </item> 
        <guided-else-menu-item-selected> 
             <item> 
          <label><![CDATA[<guided-menu-item-label />]]></label> 
          <value><![CDATA[<guided-menu-item-value />]]></value> 
          <link><![CDATA[<guided-menu-item-path />]]></link>     
             </item> 
        </guided-if-menu-item-selected> 
    </guided-menu> 
        </menu> 
        <menu> 
            <name><![CDATA[ss_head_nav]]></name> 
            <guided-menu gsname="ss_head_nav"> 
                <guided-if-menu-item-selected> 
                    <item selected="true"> 
                    <label><![CDATA[<guided-menu-item-label />]]></label> 
      <value><![CDATA[<guided-menu-item-value />]]></value> 
      <link><![CDATA[<guided-menu-item-path />]]></link> 
                <guided-else-menu-item-selected> 
                    <label><![CDATA[<guided-menu-item-label />]]></label> 
      <value><![CDATA[<guided-menu-item-value />]]></value> 
      <link><![CDATA[<guided-menu-item-path />]]></link> 
                </guided-if-menu-item-selected> 
            </guided-menu>  
        </menu> 
    </menus> 
 
    <breadcrumbs> 
  <breadcrumb> 
            <name><![CDATA[default]]></name> 
      <guided-breadcrumb gsname="default"> 
  <breadcrumb-item> 
    <link><![CDATA[<guided-breadcrumb-path gsname="goto">]]></link> 
    <value><![CDATA[<guided-breadcrumb-value />]]></value> 
                        <label><![CDATA[<guided-breadcrumb-label>]]></label> 
   </breadcrumb-item> 
         </guided-breadcrumb> 
   </breadcrumb> 
    </breadcrumbs> 
 
    <suggestions> 
        <auto-searched><guided-if-suggestion-autosearch>1<guided-else-suggestion-autosearch>0</guided-if-suggestion-autosearch></auto-searched> 
        <guided-if-suggestion-autosearch><orig-query><![CDATA[<guided-suggestion-original-query/>]]></orig-query></guided-if-suggestion-autosearch> 
        <suggestions-low-results><guided-if-suggestion-low-results>1<guided-else-suggestion-low-results>0</guided-if-suggestion-low-results></suggestions-low-results> 
        <guided-suggestions> 
     <suggestion-item> 
         <link><![CDATA[<guided-suggestion-path />]]></link> 
  <word><![CDATA[<guided-suggestion />]]></word> 
     </suggestion-item> 
 </guided-suggestions> 
    </suggestions> 
 
    <pagination> 
        <total-pages><![CDATA[<guided-page-total />]]></total-pages> 
        <pages> 
     <page position="first"><![CDATA[<guided-page-path gsname="first" />]]></page> 
     <page position="last"><![CDATA[<guided-page-path gsname="last" />]]></page> 
     <guided-if-page-prev><page position="prev"><![CDATA[<guided-page-path gsname="prev" />]]></page></guided-if-page-prev> 
     <guided-if-page-next><page position="next"><![CDATA[<guided-page-path gsname="next" />]]></page></guided-if-page-next> 
     <guided-if-page-viewall><page position="viewall"><![CDATA[<guided-page-path gsname="viewall" />]]></page></guided-if-page-viewall> 
     <guided-if-page-viewpages><page position="viewall"><![CDATA[<guided-page-path gsname="viewpages" />]]></page></guided-if-page-viewpages> 
 
     <guided-pages> 
                <guided-if-page-selected><page position="<guided-page-number />" selected="true"><![CDATA[<guided-page-path />]]></page> 
  <guided-else-page-selected><page position="<guided-page-number />"><![CDATA[<guided-page-path />]]></page> 
  </guided-if-page-selected> 
     </guided-pages> 
        </pages> 
    </pagination> 
 
    <facets>  
        <guided-facet gsname="leveli"> 
     <facet-item> 
         <facet-title><![CDATA[Department]]></facet-title> 
                <selected><guided-if-facet-selected>1<guided-else-facet-selected>0</guided-if-facet-selected></selected> 
                <guided-if-facet-selected><undo-link><![CDATA[<guided-facet-undo-path gsname="leveli">]]></undo-link></guided-if-facet-selected> 
  <guided-facet-values> 
      <facet-value> 
          <guided-if-facet-value-selected><selected><![CDATA[true]]></selected></guided-if-facet-value-selected> 
              <label><![CDATA[<guided-facet-value>]]></label> 
       <link><![CDATA[<guided-facet-value-path />]]></link> 
       <count><![CDATA[<guided-facet-count>]]></count> 
                        <guided-if-facet-value-selected><undolink><![CDATA[<guided-facet-value-undo-path />]]></undolink></guided-if-facet-value-selected> 
      </facet-value> 
  </guided-facet-values> 
      </facet-item> 
 </guided-facet> 
    </facets> 
 
    <results> 
        <result-set> 
            <name><![CDATA[default]]></name> 
            <guided-results gsname="default">   
         <result> 
                    <field name="index"><![CDATA[<guided-result-index />]]></field> 
      <field name="brand"><![CDATA[<guided-result-field gsname="brand" />]]></field> 
      <field name="price"><![CDATA[<guided-result-field gsname="price" />]]></field> 
      <field name="foundIn"><![CDATA[<guided-if-result-field gsname="leveli"><!--tmpl_var name='leveli'-->, </guided-if-result-field> 
            <guided-if-result-field gsname="levelii"><!--tmpl_var name='levelii'-->, </guided-if-result-field> 
          <guided-if-result-field gsname="leveliii"><!--tmpl_var name='leveliii'--></guided-if-result-field>]]></field> 
         </result>   
     </guided-results> 
        </result-set>   
    </results> 
 
    <guided-if-recent-searches> 
    <recent-searches> 
        <clear-link><guided-recent-searches-clear-path/></clear-link> 
        <guided-recent-searches> 
            <recent-search> 
                <link><guided-recent-searches-path></link> 
                <label><guided-recent-searches-value></label> 
            <recent-search> 
        </guided-recent-searches> 
    </recent-searches> 
    </guided-if-recent-searches> 
 
    <banners> 
        <guided-if-banner-set gsname="top"> 
            <banner> 
                <area><![CDATA[top]]></area> 
                <content><![CDATA[<guided-banner gsname="top">]]></content> 
            </banner> 
        </guided-if-banner-set> 
        <guided-if-banner-set gsname="bottom"> 
            <banner> 
                <area><![CDATA[bottom]]></area> 
                <content><![CDATA[<guided-banner gsname="bottom">]]></content> 
            </banner> 
        </guided-if-banner-set> 
    </banners> 
 
    <zones> 
        <zone> 
            <name><![CDATA[brand-facet]]></name> 
            <display><guided-if-zone gsname="brand-facet">1<guided-else-zone>0</guided-if-zone></display> 
        </zone> 
    </zones> 
 
    <search-form> 
        <include-tnt-mbox><guided-if-tnt-business-rules>1<guided-else-tnt-business-rules>0</guided-if-tnt-business-rules></include-tnt-mbox> 
        <autocomplete> 
            <enabled><guided-if-autocomplete>1<guided-else-autocomplete>0</guided-if-autocomplete></enabled> 
            <css><![CDATA[<guided-ac-css/>]]></css> 
            <form-content><![CDATA[<guided-ac-form-content/>]]></form-content> 
            <javascript><![CDATA[<guided-ac-javascript/>]]></javascript> 
        </autocomplete> 
    </search-form> 
 
</customer-results> 
```

