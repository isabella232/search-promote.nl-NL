---
description: Leer hoe u uitvoer in elke op tekst gebaseerde indeling kunt aanpassen, inclusief XML of JSON.
solution: Target
title: Uitvoer van Begeleide zoekfunctie
topic: Bijlagen,zoeken en verhandelen van sites
uuid: 234fd563-f249-42b0-88ca-c89b44f8df77
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '6289'
ht-degree: 0%

---


# Uitvoer met instructies voor zoeken{#guided-search-output}

U kunt uitvoer in elke op tekst gebaseerde indeling aanpassen, waaronder XML of JSON.

## Uitvoer van Bewerken met instructies-zoekopdracht gebruiken {#concept_2A1BA3AD413848A1AC2A3ABC4FFE481F}

Het uitvoerformaat is klantgericht om het facetteren, het sorteren, en andere implementatie-specifieke besluiten te steunen die tijdens het ontwerpproces worden genomen. U kunt het formaat zelf aanpassen om de ontwikkeling van het vooreind van de klant, indien nodig te vereenvoudigen.

De volledige uitvoer bevindt zich binnen `<result>`-tags en de meeste dynamische gegevens worden ingesloten binnen `<![CDATA[ ]]>`-tags. Zo kunnen de resultaten HTML en andere niet-XML-entiteiten bevatten.

Wanneer koppelingen naar andere pagina&#39;s worden opgegeven, worden deze weergegeven in de vorm van een relatieve URL. Dit resultaat omvat ook de parameters van het vraagkoord die worden overgegaan om het gewenste resultaat te produceren.

## Implementatie van Bewerken met instructies-zoekopdracht {#section_95483980930C4325BAB50A40BD47245A}

Wanneer u met een Begeleide implementatie van het Onderzoek begint herinner me dat [!DNL Adobe Search&Promote] voor de Bedrijfslaag verantwoordelijk is. Dat wil zeggen, de logica die omringt welke resultaten en facetten op elk bepaald ogenblik aan een klant worden getoond.

Wanneer u het de toepassingsvooreind van het Web implementeert dat ontleedt en de resultaten als HTML toont, beperkt de functionaliteit tot vertoning slechts. Met andere woorden, om het even welke server-zijlogica die u gebruikt om de Laag van de Presentatie tot stand te brengen neemt niet de besluiten over wat aan een klant voor te stellen, tenzij het noodzakelijk is. De bedrijfsregels werken niet zoals u verwacht als het front-end script de zoekresultaten wijzigt.

[!DNL Adobe Search&Promote] Hiermee behoudt u de gebruikerstoestand van de geselecteerde opties voor het verfijnen van zoekopdrachten aan de hand van de URL-parameters. Alle `<link>` knooppunten bevatten de relevante parameters van de selecties van de klant. Deze parameters kunnen de selectie van breadcrumb, paginering, sortering en facetten omvatten. Indien van toepassing worden `<undolink>` knooppunten geretourneerd om een klant in staat te stellen een selectie &quot;terug&quot; te zetten. Facetten en broodkruimels bieden deze types van verbindingen aan.

## Werken met de zoekserver {#section_8DBEACDECD714E59BDED6315E6041B8D}

Er wordt een REST-achtige API gebruikt waarmee u kunt communiceren om zoekopdrachten uit te voeren en resultaten te ontvangen. De meest gebruikte indelingen voor de resultaten zijn XML of JSON.

De basis-URI is gekoppeld aan een specifieke account en een gefaseerde of live omgeving. U kunt meerdere aliassen voor de basis-URI aanvragen bij uw accountmanager. Bijvoorbeeld, heeft een fictioneel bedrijf genoemd Megacorp de volgende twee basis URLs verbonden aan hun rekening:

* `https://search.megacorp.com `
* `https://stage.megacorp.com`

De eerste URI voert zoekopdrachten uit op basis van hun live index en de laatste URI op basis van hun gefaseerde index.

Zoekverzoeken bestaan uit de basis-URI en een set CGI-parameters of sleutelwaardeparen die de gewenste zoekopdracht aangeven voor de account die aan de basis-URI is gekoppeld.

Er worden drie indelingen van CGI-parameters ondersteund. Standaard is uw account geconfigureerd om CGI-parameters te scheiden met een puntkomma ( `;`), zoals in het volgende voorbeeld:

* `https://search.megacorp.com?q=shoes ;page=2`

Uw accountmanager kan desgewenst uw account zodanig configureren dat ampersands ( `&`) worden gebruikt om de CGI-parameters te scheiden, zoals in het volgende voorbeeld:

* `https://search.megacorp.com?q=shoes &page=2`

Een derde indeling, de zogenaamde SEO-indeling, wordt ook ondersteund wanneer een slash ( `/`) wordt gebruikt in plaats van het scheidingsteken en het gelijkteken om &quot;schone&quot; koppelingen te genereren, zoals in het volgende voorbeeld:

* `https://search.megacorp.com/q/shoes/page/2`

Elke keer dat de SEO-indeling wordt gebruikt om een aanvraag te verzenden, worden alle uitvoerkoppelingen in dezelfde indeling geretourneerd.

## Zoekqueryparameters {#section_7ADA5E130E3040C9BE85D0D68EDD3223}

De volgende lijst beschrijft de standaard &quot;uit-van-de-doos&quot;parameters van de onderzoeksvraag die u kunt gebruiken. De regels van de verwerking en de bedrijfsregels kunnen worden gebouwd gebaseerd op user-defined vraagparameters om douanebedrijfslogica uit te voeren die voor uw bedrijf relevant is. U kunt met het raadplegende team werken om documentatie over die parameters te verkrijgen.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Zoekqueryparameter </p> </th> 
   <th colname="col2" class="entry"> <p>Voorbeeld </p> </th> 
   <th colname="col3" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> q  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> q= string  </span> </p> </td> 
   <td colname="col3"> <p> Geeft de queryreeks voor de zoekopdracht aan. Deze parameter brengt aan de <span class="codeph"> sp_q </span> achterste onderzoeksparameter in kaart. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> q#  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> q#= tekenreeks  </span> </p> </td> 
   <td colname="col3"> <p>De genummerde <span class="codeph"> q </span> en <span class="codeph"> x </span> parameters verwezenlijken facettering, of het zoeken binnen een bepaald gebied. </p> <p>De <span class="codeph"> q </span> parameter bepaalt de termijn u in het facet als overeenkomstige genummerde <span class="codeph"> x </span> parameterpunten zoekt. Als u bijvoorbeeld twee facetten hebt met een naam voor grootte en kleur, kunt u bijvoorbeeld de volgende elementen gebruiken: </p> <p> <span class="codeph"> q1=small;x1=size;q2=red;x2=color  </span> </p> <p>Deze parameter brengt aan de <span class="codeph"> sp_q_exact_# </span> achterste onderzoeksparameters in kaart. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> x#  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> x#= tekenreeks  </span> </p> </td> 
   <td colname="col3"> <p> De genummerde <span class="codeph"> q </span> en <span class="codeph"> x </span> parameters verwezenlijken facettering, of het zoeken binnen een bepaald gebied. </p> <p>De <span class="codeph"> q </span> parameter bepaalt de termijn u in het facet als overeenkomstige genummerde <span class="codeph"> x </span> parameterpunten zoekt. Als u bijvoorbeeld twee facetten hebt met een naam voor grootte en kleur, kunt u bijvoorbeeld de volgende elementen gebruiken: </p> <p> <span class="codeph"> q1=small;x1=size;q2=red;x2=color  </span> </p> <p>Deze parameter brengt aan <span class="codeph"> sp_x_# </span> achterste onderzoeksparameters in kaart. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> collectie  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> collection= string  </span> </p> </td> 
   <td colname="col3"> <p> Geeft de verzameling op die voor de zoekopdracht moet worden gebruikt. Deze parameter brengt aan de <span class="codeph"> sp_k </span> achterste onderzoeksparameter in kaart. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> aantal  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> count= getal  </span> </p> </td> 
   <td colname="col3"> <p> Hiermee geeft u het totale aantal resultaten op dat wordt weergegeven. De standaardwaarde wordt gedefinieerd in <span class="uicontrol"> Instellingen </span> &gt; <span class="uicontrol"> Zoeken </span> &gt; <span class="uicontrol"> Zoekopdrachten </span>. Deze parameter brengt aan de <span class="codeph"> sp_c </span> achterste onderzoeksparameter in kaart. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> page  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> page= number  </span> </p> </td> 
   <td colname="col3"> <p> Geeft de pagina met resultaten aan die worden geretourneerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rangschikken  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> rank= veld  </span> </p> </td> 
   <td colname="col3"> <p> Hiermee geeft u het veld met rangorde op dat u wilt gebruiken voor statische rangschikking. Het veld moet een veld van het type Rank zijn met een relevantie groter dan 0. Deze parameter brengt aan de <span class="codeph"> sp_sr </span> achterste parameter in kaart. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gs_store  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> gs_store= string  </span> </p> </td> 
   <td colname="col3"> <p> Hiermee geeft u de winkel op die u wilt zoeken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sorteren  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> sort= number  </span> </p> </td> 
   <td colname="col3"> <p> Hiermee geeft u de sorteervolgorde op. "0" is de standaardwaarde en sorteert op relevantiescore; "1" sorteert op datum; "-1" wordt niet gesorteerd. </p> <p>Gebruikers kunnen een veldnaam opgeven voor de waarde van de parameter <span class="codeph"> sp_s </span>. Met <span class="codeph"> sp_s=title </span> sorteert u de resultaten bijvoorbeeld op basis van de waarden in het titelveld. Wanneer een gebiedsnaam voor de waarde van een <span class="codeph"> sp_s </span> parameter wordt gebruikt, worden de resultaten gesorteerd door dat gebied en dan gesubsorteerd door relevantie. </p> <p>Ga als volgt te werk om deze functie in te schakelen: </p> 
    <ol id="ol_3894F81EA7BF4827A84DE8662111ABEF"> 
     <li id="li_C040C0B88F174A4885E1A8E721FD032A">Klik in het productmenu op <span class="uicontrol"> Instellingen </span> &gt; <span class="uicontrol"> Metagegevens </span> &gt; <span class="uicontrol"> Definities </span>. </li> 
     <li id="li_2E83C3A46D1B4BF991EABAD9D3E52B7D">Voer op de pagina <span class="wintitle"> Gelaagde definities </span> een van de volgende handelingen uit: 
      <ul id="ul_8018FEE10E0A4C96A74F84A897080580"> 
       <li id="li_E9A7CE43E2734F4D9522A1283CA111FB">Klik <span class="uicontrol"> Nieuw veld toevoegen </span>. </li> 
       <li id="li_9D2434A321924FBD874569CA9AD2EEF7">Klik op <span class="uicontrol"> Bewerken </span> voor een bepaalde veldnaam. </li> 
      </ul> </li> 
     <li id="li_90D5E3F4AC0A4A6189934A5589F69903">Klik in de vervolgkeuzelijst <span class="wintitle"> Sorteren </span> op <span class="uicontrol"> Overlopend </span> of <span class="uicontrol"> Aflopend </span>. <p>Deze parameter brengt aan <span class="codeph"> sp_s </span> achterste onderzoeksparameter in kaart. </p> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

## Integreren met uw systeem {#section_91261B19A44A4E579B3FC9FAB9AD3665}

Hieronder volgen enkele aanbevelingen voor integratie met uw systeem.

* Communiceren met de zoekserver.

   U kunt met de [!DNL Adobe Search&Promote] Webservers communiceren gebruikend HTTP- verzoeken. Uw servers genereren deze aanvragen of op de client wordt een Ajax-aanvraag uitgevoerd.
* De zoekgeschiedenis opslaan.

[!DNL Adobe Search&Promote] is stateless where the entire state is passed in the http request.
* De geretourneerde resultaten parseren.

   Het wordt aanbevolen een op SAX gebaseerde XML-parser te gebruiken om de XML-reactie te parseren. Als u Ajax- verzoek produceert, vorm [!DNL Adobe Search&Promote] om JSON- reacties voor die verzoeken terug te keren om het gemakkelijker te maken om de reactie te ontleden.

## JSON-uitvoer met instructies zoeken {#reference_EB8182A564DE4374BB84158F2AABEF74}

Tabellen die de standaard JSON-responsuitvoer beschrijven.

Zie ook [JSON-uitvoer met instructies zoeken](../c-appendices/c-guidedsearchoutput.md#reference_EB8182A564DE4374BB84158F2AABEF74).

U kunt het JSON-antwoord op de volgende vragen bekijken:

* [Banners](../c-appendices/c-guidedsearchoutput.md#section_88519CAAD25F4BD49D5E517077745B0E)
* [Broodkruimel](../c-appendices/c-guidedsearchoutput.md#section_A7DB0F1DA9ED4CBCAE18395122F3E01E)
* [Facetten](../c-appendices/c-guidedsearchoutput.md#section_65932C95931743A1BFAF1DF16D7E6D92)
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
   <td colname="col2"> <p> Een afzonderlijk bannerknooppunt. U kunt meerdere bannerknooppunten hebben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;area&gt; </span> </p> </td> 
   <td colname="col2"> <p> Het gebied op de webpagina waar de banner wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;content&gt; </span> </p> </td> 
   <td colname="col2"> <p> De HTML-inhoud voor het bannergebied. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Broodkruimel {#section_A7DB0F1DA9ED4CBCAE18395122F3E01E}

In het volgende voorbeeld wordt de selectie toegevoegd aan de broodkruimel telkens wanneer de klant de facetten verder doorloopt. Elk item wordt weergegeven als een `<breadcrumb-item>`.

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
   <th colname="col1" class="entry"> <p>Tags in Breadcrumb </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p> Een relatieve koppeling naar de zoekresultaten die de gewenste weergave toont. Als u op een koppeling breadcrumb klikt, gaat de klant naar een weergave waarin alle verfijningen die erop volgen, worden verwijderd. Er zijn ook andere opties beschikbaar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;value&gt; </span> </p> </td> 
   <td colname="col2"> <p> Klantgerichte tekst voor het broodkruimelitem. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Facetten {#section_65932C95931743A1BFAF1DF16D7E6D92}

Facetten zijn verfijningsopties die klanten de mogelijkheid bieden om op de resultaten te filteren. Facetten worden doorgaans gebruikt voor categorisering, prijsbereiken, kleurselecties en andere kenmerkverfijning. De metagegevens in de index zijn de factoren die de basis vormen.

Het is gebruikelijk om categoriseringsfacetten&#39; te verbergen of te tonen aangezien een klant onderaan door categorisering beweegt. Het hoogste niveau van categorisering (categorie) wordt Tier 1 genoemd. Wanneer een klant op een optie voor Tier 1 klikt, worden de opties voor Tier 2-verfijning (subcategorie) weergegeven en verdwijnen de opties voor Tier 1. Wanneer een klant op een optie voor Tier 2 klikt, worden de opties voor de verfijning voor Tier 3 (subcategorie) weergegeven en verdwijnen de opties voor Tier 2. Zoals hierboven vermeld, zijn deze opties verborgen en weergegeven. De webtoepassing heeft hierop geen invloed.

Elk facet bevindt zich binnen `<facet-item>`-tags. In het volgende voorbeeld wordt één facet weergegeven waarmee de klant de zoekresultaten kan verfijnen met &#39;vakantie&#39;.

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
   <th colname="col1" class="entry"> <p>Labels in facetten </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;facet-title&gt; </span> </p> </td> 
   <td colname="col2"> <p> Klantgerichte titel voor de facet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;label&gt; </span> </p> </td> 
   <td colname="col2"> <p> Klantgericht label voor de facetoptie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p> Relatieve koppeling naar resultaten die door de optie worden verfijnd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;count&gt; </span> </p> </td> 
   <td colname="col2"> <p> Het aantal resultaten in die verfijnde resultaatset. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;undolink&gt; </span> </p> </td> 
   <td colname="col2"> <p> Wanneer een facetwaarde wordt geselecteerd, keert de knoop "undo verbinding"terug die een klant uit de resultaten laat terug. </p> </td> 
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

Deze tags worden samen gebruikt en geven een bericht weer, zoals: &quot;De resultaten 1-16 van 621 voor het nieuwe jaar worden weergegeven.&quot;

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Labels in koptekst en query </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;user-query&gt; </span> </p> </td> 
   <td colname="col2"> <p> De sleutelwoordvraag die met het verzoek wordt voorgelegd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;lower-results&gt; </span> </p> </td> 
   <td colname="col2"> <p> Het objectnummer van het eerste resultaat op deze pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;upper-results&gt; </span> </p> </td> 
   <td colname="col2"> <p> Het objectnummer van het laatste resultaat op deze pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;total-results&gt; </span> </p> </td> 
   <td colname="col2"> <p> Het totale aantal resultaten dat overeenkomt met de gebruikersquery. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;custom-field&gt; </span> </p> </td> 
   <td colname="col2"> <p> Een optioneel veld dat algemeen van toepassing is op de zoekresultaten. </p> </td> 
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
   <th colname="col1" class="entry"> <p>Labels in paginering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;total-pages&gt; </span> </p> </td> 
   <td colname="col2"> <p> Het totale aantal pagina's met resultaten, gebaseerd op het aantal resultaten gedeeld door het aantal resultaten per pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="first"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Bevat een relatieve koppeling naar de eerste pagina in de resultatenset, tenzij de klant pagina 1 al weergeeft. In dat geval is het leeg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="last"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Bevat een relatieve koppeling naar de laatste pagina in de resultatenset, tenzij de klant de laatste pagina bekijkt. In dat geval is het leeg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="previous"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Bevat een relatieve koppeling naar de vorige pagina in de resultatenset, tenzij de klant pagina 1 weergeeft; in dat geval is het leeg . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="next"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Bevat een relatieve koppeling naar de laatste pagina in de resultatenset, tenzij de klant de laatste pagina bekijkt. In dat geval is het leeg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="x"&gt;</span> </p> </td> 
   <td colname="col2"> <p> Bevat een relatieve koppeling naar een bepaald paginanummer. Er worden tien opeenvolgende paginanummers weergegeven. Op pagina 1 zou het pagina 1-10 zijn. Aan het einde van de resultaatset (in dit geval 39) zijn het de bladzijden 30-39. In het midden van de resultatenset, pagina 15, zou het bijvoorbeeld pagina's 11-20 zijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> selected="true"&gt;  </span> </p> </td> 
   <td colname="col2"> <p> Toegepast als kenmerk op de geselecteerde pagina. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Recente zoekopdrachten {#section_525816A0355C48F8970D89B8FC3F1FFF}

Recent zoeken is een op cookies gebaseerde functie die alleen werkt als u de cookie-informatie doorgeeft aan de servers.

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
   <th colname="col1" class="entry"> <p>Tags in recente zoekopdrachten </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;recent-search&gt; </span> </p> </td> 
   <td colname="col2"> <p> Een individueel recent-onderzoek knooppunt. U kunt meerdere knooppunten voor recent zoeken hebben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-term&gt; </span> </p> </td> 
   <td colname="col2"> <p> De term die de klant eerder heeft gezocht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p> Koppelingen naar de vorige zoekopdracht. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Resultaten {#section_41AC56BB0A084BF59379B06C8BEF2157}

De resultaatset is een aanpasbaar gebied van de JSON-reactie. Elke index is uniek in de veld noemende mechanismen van meta-gegevens. Er zijn gemeenschappelijke gebieden die voor elk resultaat zoals titel, beschrijving, en URL zijn teruggekeerd. Maar alle metagegevens die voor een pagina in de index zijn gedefinieerd, kunnen beschikbaar worden voor gebruik in elk resultaatknooppunt. Categorisering, prijzen, kleuren en miniaturen zijn slechts een paar opties die u op een resultaat kunt toepassen om overtuigender zoekresultaten te produceren.

De indeling Resultaten wordt aangepast op basis van de metagegevens die specifiek zijn voor uw implementatie. Hier vindt u alle gegevens per resultaat die in de resultaten worden weergegeven, inclusief URL&#39;s van miniatuurafbeeldingen.

Bovendien is het mogelijk om veelvoudige resultaatstreken binnen de pagina, zoals &quot;Aanbevolen Resultaten&quot;te vormen, of afzonderlijke &quot;Producten&quot;en &quot;Inhoud&quot;resultaatsecties. In deze gevallen worden er meerdere resultaatzones opgegeven in de HTML, hoewel facetten alleen aan de primaire resultaatset zijn gekoppeld.

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
   <th colname="col1" class="entry"> <p>Tags in resultaten </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;index&gt; </span> </p> </td> 
   <td colname="col2"> <p> Het serienummer van het resultaat binnen deze resultatenset. In dit voorbeeld, waar tien resultaten per pagina worden getoond, op pagina 2 van de resultaten, zou het eerste punt een index van 11 hebben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;result-title&gt; </span> </p> </td> 
   <td colname="col2"> <p> De klantgerichte titel voor deze pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;url&gt; </span> </p> </td> 
   <td colname="col2"> <p> De URL voor deze pagina. Het wordt gebruikt om een hyperlink tot stand te brengen die de klant door de resultaten laat klikken. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Formulier {#section_434DA13EA295474C99FFE9F14801CD0E} doorzoeken

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
   <th colname="col1" class="entry"> <p>Tags in zoekformulier </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;include-tnt-mbox&gt; </span> </p> </td> 
   <td colname="col2"> <p> Optioneel. Indien aanwezig in de JSON, geeft de waarde 1 aan dat uw account is gekoppeld aan <span class="keyword"> Test&amp;Target </span> en ten minste één bedrijfsregel bevat die in een A:B-test wordt opgenomen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;autocomplete&gt; </span> </p> </td> 
   <td colname="col2"> <p> Optioneel. Wanneer u auto-complete gebruikt, is dit knooppunt aanwezig om aan te geven dat de CSS en JavaScript aanwezig zijn op de pagina samen met de inhoud in het formulier. Deze velden veranderen alleen als iemand een instelling voor automatisch aanvullen heeft gewijzigd. In dergelijke gevallen, wordt het xxx_cache_ver gebied verhoogd om een ongeldigverklaring van de caching inhoud op browser van uw klant te dwingen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;css&gt; </span> </p> </td> 
   <td colname="col2"> <p> De CSS die is gekoppeld aan automatisch aanvullen. U wordt aangeraden deze tag hoog op de pagina te plaatsen om de rendering van pagina's te verbeteren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;form-content&gt; </span> </p> </td> 
   <td colname="col2"> <p> Inhoud die binnen uw onderzoek-van voor het autocomplete nut wordt vereist om aan de correcte controle te koppelen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;js&gt; </span> </p> </td> 
   <td colname="col2"> <p> Aangepast JavaScript dat vereist is voor Automatisch aanvullen. U wordt aangeraden deze tag laag op de pagina te plaatsen om de rendering van pagina's te verbeteren. JavaScript voor de gebruikersinterface is ook vereist voor automatisch aanvullen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;hidden-parameters&gt; </span> </p> </td> 
   <td colname="col2"> <p> Bevat alle verborgen parameters (naam en waarde) die in het zoekformulier moeten worden opgenomen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## {#section_558853CD376F4D71BACF211D53085D55} sorteren

In het volgende voorbeeld worden de gegevens voor een sorteermenu met drie opties getoond. Met dit menu kan de klant sorteren op relevantie, titel of classificatie. Het momenteel geselecteerde item bevat het kenmerk &quot;selected=true&quot;. &quot;. Bied altijd een relevantie optie aan om een klant toe te staan om op de standaardonderzoeksresultaten terug te komen die oorspronkelijk werden getoond.

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
   <th colname="col1" class="entry"> <p>Labels in menu Sorteren </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;label&gt; </span> </p> </td> 
   <td colname="col2"> <p> De klantgerichte tekst voor de optie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;value&gt; </span> </p> </td> 
   <td colname="col2"> <p> Vertegenwoordigt de waarde van de "soort"parameter van het vraagkoord voor deze optie. Deze tag is niet nodig als de waarde <span class="codeph"> &lt;link&gt; </span> wordt gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p> Voor de niet-geselecteerde opties bevat de <span class="codeph"> &lt;link&gt; </span> parameter de relatieve verbinding die de zelfde resultaatreeks terugkeert, die door de nieuwe soortparameter wordt gesorteerd. Dit veld is leeg voor de geselecteerde sorteeroptie. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Suggesties {#section_6EC104E1DDD94AC799B65E6E61A2FB3C}

Suggesties worden geretourneerd als er slechts een paar resultaten of geen resultaten zijn. Dit knooppunt bevat termen die geen succesvolle query&#39;s opleveren en die kunnen worden weergegeven op een pagina &quot;Geen resultaten&quot;. De verbinding is ook teruggekeerd zodat kan een klant aan de nieuwe vraag springen.

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
   <th colname="col1" class="entry"> <p>Tags in suggesties </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Een relatieve koppeling die wordt gebruikt om een hyperlink te maken naar zoekresultaten voor de suggestieterm. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;word&gt; </span> </p> </td> 
   <td colname="col2"> <p>De voorgestelde term. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Gebieden {#section_AE53A498B440465EAF2286F2AE87D548}

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
   <th colname="col1" class="entry"> <p>Labels in zones </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;zone&gt; </span> </p> </td> 
   <td colname="col2"> <p> Een afzonderlijk knooppunt voor zones. U kunt meerdere streekknooppunten hebben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;name&gt; </span> </p> </td> 
   <td colname="col2"> <p> De naam van de zone. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;display&gt; </span> </p> </td> 
   <td colname="col2"> <p> 1 of 0 om erop te wijzen of de streek of niet wordt getoond. De werkelijke zone-inhoud kan een statisch gebied op uw webpagina of in uw zoekresultaten zijn, zoals beste verkopers of verwante producten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## XML-uitvoer met instructies zoeken {#reference_D93E859A277643068B10AE7A61C973EA}

Tabellen die de standaard XML-responsuitvoer beschrijven.

U kunt de XML-reactie op het volgende controleren:

* [Banners](../c-appendices/c-guidedsearchoutput.md#section_6A19EC26DD3B494194AAA788151B78B5)
* [Broodkruimel](../c-appendices/c-guidedsearchoutput.md#section_E48A71B0EBDB4EDDA7587009AD865488)
* [Facetten](../c-appendices/c-guidedsearchoutput.md#section_5CEB1F966C004FFEA3CF675638966E25)
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
   <td colname="col2"> <p> Een afzonderlijk bannerknooppunt. U kunt meerdere bannerknooppunten hebben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;area&gt; </span> </p> </td> 
   <td colname="col2"> <p> Het gebied op de webpagina waar de banner wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;content&gt; </span> </p> </td> 
   <td colname="col2"> <p> De HTML-inhoud voor het bannergebied. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Broodkruimel {#section_E48A71B0EBDB4EDDA7587009AD865488}

In het volgende voorbeeld wordt de selectie toegevoegd aan de broodkruimel telkens wanneer de klant de facetten verder doorloopt. Elk item wordt weergegeven als een `<breadcrumb-item>`.

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
   <th colname="col1" class="entry"> <p>Tags in Breadcrumb </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p> Een relatieve koppeling naar de zoekresultaten die de gewenste weergave toont. Als u op een koppeling breadcrumb klikt, gaat de klant naar een weergave waarin alle verfijningen die erop volgen, worden verwijderd. Er zijn ook andere opties beschikbaar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;value&gt; </span> </p> </td> 
   <td colname="col2"> <p> Klantgerichte tekst voor het broodkruimelitem. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Facetten {#section_5CEB1F966C004FFEA3CF675638966E25}

Facetten zijn verfijningsopties die klanten de mogelijkheid bieden om op de resultaten te filteren. Facetten worden doorgaans gebruikt voor categorisering, prijsbereiken, kleurselecties en andere kenmerkverfijning. De metagegevens in de index zijn de factoren die de basis vormen.

Het is gebruikelijk om categoriseringsfacetten&#39; te verbergen of te tonen aangezien een klant onderaan door categorisering beweegt. Het hoogste niveau van categorisering (categorie) wordt Tier 1 genoemd. Wanneer een klant op een optie voor Tier 1 klikt, worden de opties voor Tier 2-verfijning (subcategorie) weergegeven en verdwijnen de opties voor Tier 1. Wanneer een klant op een optie voor Tier 2 klikt, worden de opties voor de verfijning voor Tier 3 (subcategorie) weergegeven en verdwijnen de opties voor Tier 2. Zoals hierboven vermeld, zijn deze opties verborgen en weergegeven. De webtoepassing heeft hierop geen invloed.

Elk facet bevindt zich binnen `<facet-item>`-tags. In het volgende voorbeeld wordt één facet weergegeven waarmee de klant de zoekresultaten kan verfijnen met &#39;vakantie&#39;.

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
   <th colname="col1" class="entry"> <p>Labels in facetten </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;facet-title&gt; </span> </p> </td> 
   <td colname="col2"> <p> Klantgerichte titel voor de facet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;label&gt; </span> </p> </td> 
   <td colname="col2"> <p> Klantgericht label voor de facetoptie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p> Relatieve koppeling naar resultaten die door de optie worden verfijnd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;count&gt; </span> </p> </td> 
   <td colname="col2"> <p> Het aantal resultaten in die verfijnde resultaatset. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;undolink&gt; </span> </p> </td> 
   <td colname="col2"> <p> Wanneer een facetwaarde wordt geselecteerd, keert de knoop "undo verbinding"terug die een klant uit de resultaten laat terug. </p> </td> 
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

Deze tags worden samen gebruikt en geven een bericht weer, zoals: &quot;De resultaten 1-16 van 621 voor het nieuwe jaar worden weergegeven.&quot;

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Tags in koptekst en query </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;user-query&gt; </span> </p> </td> 
   <td colname="col2"> <p> De sleutelwoordvraag die met het verzoek wordt voorgelegd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;lower-results&gt; </span> </p> </td> 
   <td colname="col2"> <p> Het objectnummer van het eerste resultaat op deze pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;upper-results&gt; </span> </p> </td> 
   <td colname="col2"> <p> Het objectnummer van het laatste resultaat op deze pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;total-results&gt; </span> </p> </td> 
   <td colname="col2"> <p> Het totale aantal resultaten dat overeenkomt met de gebruikersquery. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;custom-field&gt; </span> </p> </td> 
   <td colname="col2"> <p> Een optioneel veld dat algemeen van toepassing is op de zoekresultaten. </p> </td> 
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
   <th colname="col1" class="entry"> <p>Labels in paginering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;total-pages&gt; </span> </p> </td> 
   <td colname="col2"> <p> Het totale aantal pagina's met resultaten, gebaseerd op het aantal resultaten gedeeld door het aantal resultaten per pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="first"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Bevat een relatieve koppeling naar de eerste pagina in de resultatenset, tenzij de klant pagina 1 al weergeeft. In dat geval is het leeg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="last"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Bevat een relatieve koppeling naar de laatste pagina in de resultatenset, tenzij de klant de laatste pagina bekijkt. In dat geval is het leeg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="previous"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Bevat een relatieve koppeling naar de vorige pagina in de resultatenset, tenzij de klant pagina 1 weergeeft; in dat geval is het leeg . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="next"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Bevat een relatieve koppeling naar de laatste pagina in de resultatenset, tenzij de klant de laatste pagina bekijkt. In dat geval is het leeg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="x"&gt;</span> </p> </td> 
   <td colname="col2"> <p> Bevat een relatieve koppeling naar een bepaald paginanummer. Er worden tien opeenvolgende paginanummers weergegeven. Op pagina 1 zou het pagina 1-10 zijn. Aan het einde van de resultaatset (in dit geval 39) zijn het de bladzijden 30-39. In het midden van de resultatenset, pagina 15, zou het bijvoorbeeld pagina's 11-20 zijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> selected="true"&gt;  </span> </p> </td> 
   <td colname="col2"> <p> Toegepast als kenmerk op de geselecteerde pagina. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Recente zoekopdrachten {#section_BCA2DDD17F264CF6BA11634E1A514E28}

Recent zoeken is een op cookies gebaseerde functie die alleen werkt als u de cookie-informatie doorgeeft aan de servers.

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
   <th colname="col1" class="entry"> <p>Tags in recente zoekopdrachten </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;recent-search&gt; </span> </p> </td> 
   <td colname="col2"> <p> Een individueel recent-onderzoek knooppunt. U kunt meerdere knooppunten voor recent zoeken hebben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-term&gt; </span> </p> </td> 
   <td colname="col2"> <p> De term die de klant eerder heeft gezocht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p> Koppelingen naar de vorige zoekopdracht. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Resultaten {#section_EC496F5CA2634158891455E2F6DF6833}

De resultaatset is een aanpasbaar gebied van de XML-reactie. Elke index is uniek in de veld noemende mechanismen van meta-gegevens. Er zijn gemeenschappelijke gebieden die voor elk resultaat zoals titel, beschrijving, en URL zijn teruggekeerd. Maar alle metagegevens die voor een pagina in de index zijn gedefinieerd, kunnen beschikbaar worden voor gebruik in elk resultaatknooppunt. Categorisering, prijzen, kleuren en miniaturen zijn slechts een paar opties die u op een resultaat kunt toepassen om overtuigender zoekresultaten te produceren.

De indeling Resultaten wordt aangepast op basis van de metagegevens die specifiek zijn voor uw implementatie. Hier vindt u alle gegevens per resultaat die in de resultaten worden weergegeven, inclusief URL&#39;s van miniatuurafbeeldingen.

Bovendien is het mogelijk om veelvoudige resultaatstreken binnen de pagina, zoals &quot;Aanbevolen Resultaten&quot;te vormen, of afzonderlijke &quot;Producten&quot;en &quot;Inhoud&quot;resultaatsecties. In deze gevallen worden er meerdere resultaatzones opgegeven in de HTML, hoewel facetten alleen aan de primaire resultaatset zijn gekoppeld.

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
   <th colname="col1" class="entry"> <p>Tags in resultaten </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;index&gt; </span> </p> </td> 
   <td colname="col2"> <p> Het serienummer van het resultaat binnen deze resultatenset. In dit voorbeeld, waar tien resultaten per pagina worden getoond, op pagina 2 van de resultaten, zou het eerste punt een index van 11 hebben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;result-title&gt; </span> </p> </td> 
   <td colname="col2"> <p> De klantgerichte titel voor deze pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;url&gt; </span> </p> </td> 
   <td colname="col2"> <p> De URL voor deze pagina. Het wordt gebruikt om een hyperlink tot stand te brengen die de klant door de resultaten laat klikken. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Formulier {#section_F92D8C3D37174A10A4E26CAFF3F3DF89} doorzoeken

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
   <th colname="col1" class="entry"> <p>Tags in zoekformulier </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;include-tnt-mbox&gt; </span> </p> </td> 
   <td colname="col2"> <p> Optioneel. Indien aanwezig in XML, geeft een waarde van 1 aan dat uw account is gekoppeld aan <span class="keyword"> Test&amp;Target </span> en ten minste één bedrijfsregel heeft die in een A:B-test staat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;autocomplete&gt; </span> </p> </td> 
   <td colname="col2"> <p> Optioneel. Wanneer u auto-complete gebruikt, is dit knooppunt aanwezig om aan te geven dat de CSS en JavaScript aanwezig zijn op de pagina samen met de inhoud in het formulier. Deze velden veranderen alleen als iemand een instelling voor automatisch aanvullen heeft gewijzigd. In dergelijke gevallen, wordt het xxx_cache_ver gebied verhoogd om een ongeldigverklaring van de caching inhoud op browser van uw klant te dwingen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;css&gt; </span> </p> </td> 
   <td colname="col2"> <p> De CSS die is gekoppeld aan automatisch aanvullen. U wordt aangeraden deze tag hoog op de pagina te plaatsen om de rendering van pagina's te verbeteren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;form-content&gt; </span> </p> </td> 
   <td colname="col2"> <p> Inhoud die binnen uw onderzoek-van voor het autocomplete nut wordt vereist om aan de correcte controle te koppelen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;js&gt; </span> </p> </td> 
   <td colname="col2"> <p> Aangepast JavaScript dat vereist is voor Automatisch aanvullen. U wordt aangeraden deze tag laag op de pagina te plaatsen om de rendering van pagina's te verbeteren. JavaScript voor de gebruikersinterface is ook vereist voor automatisch aanvullen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;hidden-parameters&gt; </span> </p> </td> 
   <td colname="col2"> <p> Bevat alle verborgen parameters (naam en waarde) die in het zoekformulier moeten worden opgenomen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## {#section_32DC50A103BF491BA3665A5CADCCAADE} sorteren

In het volgende voorbeeld worden de gegevens voor een sorteermenu met drie opties getoond. Met dit menu kan de klant sorteren op relevantie, titel of classificatie. Het momenteel geselecteerde item bevat het kenmerk &quot;selected=true&quot;. &quot;. Bied altijd een relevantie optie aan om een klant toe te staan om op de standaardonderzoeksresultaten terug te komen die oorspronkelijk werden getoond.

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
   <th colname="col1" class="entry"> <p>Labels in menu Sorteren </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;label&gt; </span> </p> </td> 
   <td colname="col2"> <p> De klantgerichte tekst voor de optie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;value&gt; </span> </p> </td> 
   <td colname="col2"> <p> Vertegenwoordigt de waarde van de "soort"parameter van het vraagkoord voor deze optie. Deze tag is niet nodig als de waarde <span class="codeph"> &lt;link&gt; </span> wordt gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p> Voor de niet-geselecteerde opties bevat de <span class="codeph"> &lt;link&gt; </span> parameter de relatieve verbinding die de zelfde resultaatreeks terugkeert, die door de nieuwe soortparameter wordt gesorteerd. Dit veld is leeg voor de geselecteerde sorteeroptie. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Suggesties {#section_D81BCE46F0AF443695DF9C4BA084B716}

Suggesties worden geretourneerd als er slechts een paar resultaten of geen resultaten zijn. Dit knooppunt bevat termen die geen succesvolle query&#39;s opleveren en die kunnen worden weergegeven op een pagina &quot;Geen resultaten&quot;. De verbinding is ook teruggekeerd zodat kan een klant aan de nieuwe vraag springen.

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
   <th colname="col1" class="entry"> <p>Tags in suggesties </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Een relatieve koppeling die wordt gebruikt om een hyperlink te maken naar zoekresultaten voor de suggestieterm. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;word&gt; </span> </p> </td> 
   <td colname="col2"> <p>De voorgestelde term. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Gebieden {#section_15D8AA585F3246799968BA88EE2C9FC2}

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
   <th colname="col1" class="entry"> <p>Labels in zones </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;zone&gt; </span> </p> </td> 
   <td colname="col2"> <p> Een afzonderlijk knooppunt voor zones. U kunt meerdere streekknooppunten hebben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;name&gt; </span> </p> </td> 
   <td colname="col2"> <p> De naam van de zone. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;display&gt; </span> </p> </td> 
   <td colname="col2"> <p> 1 of 0 om erop te wijzen of de streek of niet wordt getoond. De werkelijke zone-inhoud kan een statisch gebied op uw webpagina of in uw zoekresultaten zijn, zoals beste verkopers of verwante producten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## XML-uitvoer met instructies voor zoeken in Adobe Experience Manager {#reference_DBE13C606C3A4BB185DE53F88D0D3048}

Tabellen die de standaard XML-responsuitvoer voor AEM (Adobe Experience Manager) beschrijven.

Zie ook . [XML-uitvoer met instructies voor zoeken](../c-appendices/c-guidedsearchoutput.md#reference_D93E859A277643068B10AE7A61C973EA)

U kunt de XML-reactie op het volgende controleren:

* [Banners](../c-appendices/c-guidedsearchoutput.md#section_B16EDC5533FA4494AC9983AA7357CBE3)
* [Broodkruimels](../c-appendices/c-guidedsearchoutput.md#section_49EA7043FBE44315A79A4E738BE30114)
* [Aangepaste velden](../c-appendices/c-guidedsearchoutput.md#section_38DD31AFE5DD4263A63644AFF484E0F4)
* [Facetten](../c-appendices/c-guidedsearchoutput.md#section_BE98990E3DD748A1BD4E0CA322314B79)
* [Koptekst](../c-appendices/c-guidedsearchoutput.md#section_5305B1DC5774439485CA0665DB683F9C)
* [Menu&#39;s en sorteren](../c-appendices/c-guidedsearchoutput.md#section_A34CBB645DBF4C70A12A5B7E81211295)
* [Paginering](../c-appendices/c-guidedsearchoutput.md#section_E52F81C6A6EB4B8F996157B657EC540F)
* [Query](../c-appendices/c-guidedsearchoutput.md#section_3DAA1013F09742869B80F6A361816E6C)
* [Recente zoekopdrachten](../c-appendices/c-guidedsearchoutput.md#section_17F942F6EC07456DABED7A483AC08446)
* [Resultaten](../c-appendices/c-guidedsearchoutput.md#section_155A80B8C4F641678DD9C8F257108412)
* [Zoekformulier](../c-appendices/c-guidedsearchoutput.md#section_9E4B99D4FEDC49629F6C7E866F3A7493)
* [Suggesties](../c-appendices/c-guidedsearchoutput.md#section_2899FACB9AD84F60B3687C1B4EF09E15)
* [Sjabloon](../c-appendices/c-guidedsearchoutput.md#section_1E2BB2F274B04F5491A4CCCC38F507BD)
* [Zones](../c-appendices/c-guidedsearchoutput.md#section_26C4A947E7B1474A8E37D86D9579B93E)

## Banners {#section_B16EDC5533FA4494AC9983AA7357CBE3}

Bij zoeken en verhandelen van sites kunt u de banners van een klant beheren en de banners op verschillende plaatsen op een webpagina aansluiten.

Voorbeeldbanner:

Hieronder ziet u een voorbeeld van een banner die in het gebied van de pagina&#39;s met de naam &quot;top&quot; wordt geplaatst.

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
   <th colname="col1" class="entry"> <p>Knooppunt </p> </th> 
   <th colname="col2" class="entry"> <p>Bovenliggend knooppunt </p> </th> 
   <th colname="col3" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>banners </p> </td> 
   <td colname="col2"> <p>klantresultaten </p> </td> 
   <td colname="col3"> <p>Bevat 0-n bannerknooppunten die elk bannergebied aangeven en de inhoud die in dat gebied is aangesloten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>banner </p> </td> 
   <td colname="col2"> <p>banners </p> </td> 
   <td colname="col3"> <p>Een afzonderlijk bannerknooppunt. U kunt meerdere bannerknooppunten hebben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>gebied </p> </td> 
   <td colname="col2"> <p>banner </p> </td> 
   <td colname="col3"> <p>Het gebied op de webpagina waar de banner wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>content </p> </td> 
   <td colname="col2"> <p>banner </p> </td> 
   <td colname="col3"> <p>De bannerinhoud. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Broodkruimels {#section_49EA7043FBE44315A79A4E738BE30114}

Meerdere broodkruimels worden ondersteund. U kunt broodkruimels en hun overeenkomstige gedrag in **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Breadcrumbs]** bepalen. Ook, moet u een unieke naam voor elke broodkruimel toewijzen die u bepaalt. Het XML-knooppunt breadcrumbs herhaalt alle gedefinieerde broodkruimels. U wordt aangeraden slechts één broodkruimel weer te geven in de zoekresultaten.

In het volgende voorbeeld wordt de selectie toegevoegd aan de broodkruimel telkens wanneer de klant de facetten verder doorloopt. Elk item wordt weergegeven als een `<breadcrumb-item>`.

Voorbeeld van knooppunt breadcrumb:

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
   <th colname="col1" class="entry"> <p>Knooppunt </p> </th> 
   <th colname="col2" class="entry"> <p>Bovenliggend knooppunt </p> </th> 
   <th colname="col3" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>broodkruimels </p> </td> 
   <td colname="col2"> <p>klantresultaten </p> </td> 
   <td colname="col3"> <p> Bevat 0-n breadcrumb knopen die elk breadcrumb bepalen. De meeste klanten hebben slechts één broodkruimel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>broodkruimel </p> </td> 
   <td colname="col2"> <p>broodkruimels </p> </td> 
   <td colname="col3"> <p> Bevat de onderliggende knooppunten die de definitie van een breadcrumb definiëren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>name </p> </td> 
   <td colname="col2"> <p>broodkruimel </p> </td> 
   <td colname="col3"> <p> De naam van het breadcrumb. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>breadcrumb-item </p> </td> 
   <td colname="col2"> <p>Een afzonderlijk item binnen de broodkruimel. Elk item duidt een stap in het verloop aan terwijl de gebruiker de resultatenset afsluit. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>link </p> </td> 
   <td colname="col2"> <p>breadcrumb-item </p> </td> 
   <td colname="col3"> <p> Een relatieve koppeling naar de zoekresultaten die de gewenste weergave toont. Als u op een koppeling breadcrumb klikt, gaat de klant naar een weergave waarin alle verfijningen die erop volgen, worden verwijderd. Er zijn ook andere opties beschikbaar, zoals neerzetten en verwijderen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>value </p> </td> 
   <td colname="col2"> <p>breadcrumb-item </p> </td> 
   <td colname="col3"> <p> Klantgerichte tekst voor het broodkruimelitem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>label </p> </td> 
   <td colname="col2"> <p>breadcrumb-item </p> </td> 
   <td colname="col3"> <p> Met de labeltag wordt een label voor een waarde van een breadcrumb weergegeven, waarin wordt aangegeven welke facet is geselecteerd om dat item van de breadcrumb te genereren. Het wordt alleen gebruikt in de context van een blok met instructies-breadcrumb. Voor de stap van de vraagtermijn is dit leeg. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Aangepaste velden {#section_38DD31AFE5DD4263A63644AFF484E0F4}

Aangepaste velden is een verzameling variabelen met een algemene context. Het wordt doorgaans gebruikt om variabelen voor SEO-doeleinden door te geven die zijn ingesteld in de metagegevens van de pagina met zoekresultaten.

Voorbeeld van knooppunt aangepaste velden:

```xml
    <custom-fields> 
        <custom-field name="seo-search-title"><![CDATA[Geometrixx Search Results]]></custom-field> 
        <custom-field name="seo-search-keywords"><![CDATA[]]></custom-field> 
    </custom-fields> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Knooppunt </p> </th> 
   <th colname="col2" class="entry"> <p>Bovenliggend knooppunt </p> </th> 
   <th colname="col3" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>aangepaste velden </p> </td> 
   <td colname="col2"> <p>klantresultaten </p> </td> 
   <td colname="col3"> <p> Kan onderliggende knooppunten van 0-n bevatten die aangepaste velden definiëren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>aangepast veld </p> </td> 
   <td colname="col2"> <p>aangepaste velden </p> </td> 
   <td colname="col3"> <p> Optioneel. Bevat een waarde voor een bepaald douanegebied dat door het naamattribuut wordt vermeld. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Facetten {#section_BE98990E3DD748A1BD4E0CA322314B79}

Facetten zijn verfijningsopties die klanten de mogelijkheid bieden om op de resultaten te filteren. Facetten worden doorgaans gebruikt voor categorisering, prijsbereiken, kleurselecties en andere kenmerkverfijning. Facetten worden bovenop de meta-gegevens in de index gebouwd.

Het is gebruikelijk om categoriseringsfacetten&#39; te verbergen of te tonen aangezien een klant onderaan door categorisering beweegt. Het hoogste niveau van categorisering (categorie) wordt Tier 1 genoemd. Wanneer een klant op een optie voor Tier 1 klikt, worden de opties voor Tier 2-verfijning (subcategorie) weergegeven en verdwijnen de opties voor Tier 1. Wanneer een klant op een optie voor Tier 2 klikt, worden de opties voor de verfijning van Tier 3 (subcategorie) weergegeven en verdwijnen de opties voor Tier 2. Zoals hierboven vermeld, worden deze opties verborgen en weergegeven. heeft geen invloed op deze toepassingen.

Elk facet bevindt zich binnen `<facet-item>`-tags. In het volgende voorbeeld wordt één facet weergegeven waarmee de klant de zoekresultaten kan verfijnen met &#39;vakantie&#39;.

Voorbeeld van facetblok:

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
   <th colname="col1" class="entry"> <p>Knooppunt </p> </th> 
   <th colname="col2" class="entry"> <p>Bovenliggend knooppunt </p> </th> 
   <th colname="col3" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>facetten </p> </td> 
   <td colname="col2"> <p>klantresultaten </p> </td> 
   <td colname="col3"> <p>De knoop van de containerfacetten die 0-n kindknopen heeft die elke facet vertegenwoordigen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>facet </p> </td> 
   <td colname="col2"> <p>facetten </p> </td> 
   <td colname="col3"> <p> Eén facetinstantie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>facettitel </p> </td> 
   <td colname="col2"> <p>facet </p> </td> 
   <td colname="col3"> <p>Klantgerichte titel voor de facet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>gedrag </p> </td> 
   <td colname="col2"> <p>facet </p> </td> 
   <td colname="col3"> <p>Het gedrag van de facet. Bijvoorbeeld normaal, kleverig of multi-select. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>geselecteerd </p> </td> 
   <td colname="col2"> <p>facet </p> </td> 
   <td colname="col3"> <p>1 als de facet een geselecteerde waarde heeft anders 0. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>undo-link </p> </td> 
   <td colname="col2"> <p>facet </p> </td> 
   <td colname="col3"> <p> Alleen aanwezig als het facet is geselecteerd. De koppeling Ongedaan maken verandert het hele facet. Als het bijvoorbeeld een veelgeselecteerd facet is, worden alle geselecteerde opties voor het facet uitgeschakeld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>facetwaarde </p> </td> 
   <td colname="col2"> <p>facet </p> </td> 
   <td colname="col3"> <p>Bevat alle afzonderlijke facetitems die tot het facet behoren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>geselecteerd </p> </td> 
   <td colname="col2"> <p>facetwaarde </p> </td> 
   <td colname="col3"> <p>Als het huidige item met de facet is geselecteerd, is dit knooppunt aanwezig en ingesteld op "true". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>label </p> </td> 
   <td colname="col2"> <p>facetwaarde </p> </td> 
   <td colname="col3"> <p>Klantgericht label voor de facetoptie. Standaard moet dit al door HTML worden voorkomen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>link </p> </td> 
   <td colname="col2"> <p>facetwaarde </p> </td> 
   <td colname="col3"> <p> Relatieve koppeling naar resultaten die verder worden verfijnd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>aantal </p> </td> 
   <td colname="col2"> <p>facetwaarde </p> </td> 
   <td colname="col3"> <p>Het aantal resultaten in die verfijnde resultaatset. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>undo-link </p> </td> 
   <td colname="col2"> <p>facetwaarde </p> </td> 
   <td colname="col3"> <p>Wanneer een facetwaarde wordt geselecteerd, keert de knoop "undo verbinding"terug die een klant uit het selecteren van die individuele facetselectie laat. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Koptekst {#section_5305B1DC5774439485CA0665DB683F9C}

Voorbeeld:

```xml
xml version="1.0" encoding="utf-8" standalone="yes" 
```

## Menu&#39;s en sorteren {#section_A34CBB645DBF4C70A12A5B7E81211295}

Menu&#39;s voor het sorteren van de resultaten worden ondersteund en het aantal resultaten dat per pagina moet worden geretourneerd, wordt gewijzigd. Het ondersteunt ook een navigatiemenu dat nuttig is voor het gebruik van &quot;zoeken als navigatie&quot;. Een account kan meerdere menu&#39;s van hetzelfde type definiëren en een van de menu&#39;s voor de presentatie gebruiken.

Menu-voorbeeldknooppunt:

In het volgende voorbeeld worden de gegevens voor een sorteermenu met drie opties en een navigatiemenu getoond. Met het sorteermenu kan de klant sorteren op relevantie, titel of classificatie. Het momenteel geselecteerde item bevat het kenmerk &quot;selected=true&quot;. &quot;. Bied altijd een relevantie optie aan om een klant toe te staan om op de standaardonderzoeksresultaten terug te komen die oorspronkelijk werden getoond.

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
   <th colname="col1" class="entry"> <p>Knooppunt </p> </th> 
   <th colname="col2" class="entry"> <p>Bovenliggend knooppunt </p> </th> 
   <th colname="col3" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>menu's </p> </td> 
   <td colname="col2"> <p>klantresultaten </p> </td> 
   <td colname="col3"> <p>Bevat 0-n kindknopen die elk menu bepalen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>menu </p> </td> 
   <td colname="col2"> <p>menu's </p> </td> 
   <td colname="col3"> <p>Eén instantie van een menu (komt overeen met een menu dat is gedefinieerd in <span class="uicontrol"> Ontwerp </span> &gt; <span class="uicontrol"> Navigatie </span> &gt; <span class="uicontrol"> Menu's </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>name </p> </td> 
   <td colname="col2"> <p>menu </p> </td> 
   <td colname="col3"> <p>Naam van het menu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>item </p> </td> 
   <td colname="col2"> <p>menu </p> </td> 
   <td colname="col3"> <p>Hiermee definieert u elk item in het menu. Het geselecteerde optionele kenmerk wordt ingesteld op true als het opgegeven menu-item momenteel is geselecteerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>label </p> </td> 
   <td colname="col2"> <p>item </p> </td> 
   <td colname="col3"> <p>De klantgerichte tekst voor het menupunt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>value </p> </td> 
   <td colname="col2"> <p>item </p> </td> 
   <td colname="col3"> <p>Geeft de waarde van het menu-item aan (de waarde van de queryparameter waarop het menu is ingesteld). Deze tag is niet nodig als de waarde &lt;link&gt; wordt gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>link </p> </td> 
   <td colname="col2"> <p>item </p> </td> 
   <td colname="col3"> <p>Voor de niet-geselecteerde opties bevat de parameter &lt;link&gt; de relatieve koppeling die dezelfde resultatenset retourneert, maar met de toegepaste menuoptie. Dit veld is leeg voor de geselecteerde sorteeroptie. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Paginering {#section_E52F81C6A6EB4B8F996157B657EC540F}

Resultaatsets worden over meerdere pagina&#39;s gesplitst. Meestal geven klanten 10 tot 20 resultaten weer op één pagina. De volgende resultaten worden weergegeven op de volgende pagina. Met de paginering-XML kunt u een set navigatiekoppelingen maken, zodat uw klanten per pagina door de resultaatsets kunnen bladeren. Er zijn vier beschikbare navigatiekoppelingen: eerste, laatste, volgende en vorige. Met elk type koppeling kunnen klanten snel door de pagina&#39;s bladeren, zodat ze eenvoudig kunnen bekijken en verfijnen wat ze zoeken.

In het volgende voorbeeld ziet u de paginering voor een zoekopdracht op de eerste pagina waarvoor de paginering is geconfigureerd om koppelingen naar vijf pagina&#39;s weer te geven.

Voorbeeld van paginering:

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
   <th colname="col1" class="entry"> <p>Knooppunt </p> </th> 
   <th colname="col2" class="entry"> <p>Bovenliggend knooppunt </p> </th> 
   <th colname="col3" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>paginering </p> </td> 
   <td colname="col2"> <p>klantresultaten </p> </td> 
   <td colname="col3"> <p> Het totale aantal pagina's met resultaten, gebaseerd op het aantal resultaten gedeeld door het aantal resultaten per pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>totaal aantal pagina's </p> </td> 
   <td colname="col2"> <p>paginering </p> </td> 
   <td colname="col3"> <p>Het totale aantal pagina's waarover de zoekresultaten worden verspreid. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>pagina's </p> </td> 
   <td colname="col2"> <p>paginering </p> </td> 
   <td colname="col3"> <p>Bevat 0-n paginaknooppunten die elke pagina in de paginering bepalen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>page </p> </td> 
   <td colname="col2"> <p>pagina's </p> </td> 
   <td colname="col3"> <p>Er bestaan vier speciale paginaknooppunten: eerst, last, vorige en volgende. Deze vier pagina's zijn optioneel en worden alleen in de resultatenset weergegeven als ze zinnig zijn. Als u bijvoorbeeld op pagina 1 staat, is er geen koppeling "Vorige". Alle andere pagina's geven een positie aan. Het aantal pagina's dat wordt weergegeven, is afhankelijk van het "aantal koppelingen naar pagina's" dat is geconfigureerd in de gebruikersinterface van de paginering. Het kenmerk "selected" geeft de pagina aan die de klant momenteel heeft. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Query {#section_3DAA1013F09742869B80F6A361816E6C}

Voorbeeldqueryknooppunt:

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
   <th colname="col1" class="entry"> <p>Knooppunt </p> </th> 
   <th colname="col2" class="entry"> <p>Bovenliggend knooppunt </p> </th> 
   <th colname="col3" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>query </p> </td> 
   <td colname="col2"> <p>klantresultaten </p> </td> 
   <td colname="col3"> <p> Een algemeen knooppunt dat een overzicht van de query biedt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>user-query </p> </td> 
   <td colname="col2"> <p>query </p> </td> 
   <td colname="col3"> <p> Het trefwoord waarnaar is gezocht. Als <span class="uicontrol"> Bedoelde u </span> automatisch naar een voorgestelde termijn wegens de originele termijn zoekend die geen resultaten oplevert, wordt het weerspiegeld in het nieuwe sleutelwoord dat werd gezocht (zie de suggesties knoop om het originele sleutelwoord te krijgen). </p> </td> 
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
   <td colname="col1"> <p>totale resultaten </p> </td> 
   <td colname="col2"> <p>query </p> </td> 
   <td colname="col3"> <p> Het totale aantal resultaten dat overeenkomt met de gebruikersquery. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Recente zoekopdrachten {#section_17F942F6EC07456DABED7A483AC08446}

Recent zoeken is een op cookies gebaseerde functie die alleen werkt als u de cookie-informatie doorgeeft aan de zoek- en verkoopservers van de site.

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
   <th colname="col1" class="entry"> <p>Knooppunt </p> </th> 
   <th colname="col2" class="entry"> <p>Bovenliggend knooppunt </p> </th> 
   <th colname="col3" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>recente zoekopdrachten </p> </td> 
   <td colname="col2"> <p>klantresultaten </p> </td> 
   <td colname="col3"> <p>Knooppunt is alleen aanwezig als de zoekopdracht recente zoekopdrachten bevat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>duidelijke koppeling </p> </td> 
   <td colname="col2"> <p>recente zoekopdrachten </p> </td> 
   <td colname="col3"> <p>Het relatieve pad dat alle recente zoekopdrachten van de klant wist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>recent zoeken </p> </td> 
   <td colname="col2"> <p>recente zoekopdrachten </p> </td> 
   <td colname="col3"> <p>Definieert in recente zoekopdrachten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>link </p> </td> 
   <td colname="col2"> <p>recent zoeken </p> </td> 
   <td colname="col3"> <p>Het pad om een koppeling te maken die een zoekopdracht uitvoert die de gebruiker onlangs heeft uitgevoerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>label </p> </td> 
   <td colname="col2"> <p>recent zoeken </p> </td> 
   <td colname="col3"> <p>Klant ziet een weergavelabel voor de recente zoekopdracht. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Resultaten {#section_155A80B8C4F641678DD9C8F257108412}

De resultaatset is een aanpasbaar gebied van de XML-reactie. Elke index is uniek in de veld noemende mechanismen van meta-gegevens. Er zijn gemeenschappelijke gebieden die voor elk resultaat zoals titel, beschrijving, en URL zijn teruggekeerd. Maar alle metagegevens die voor een pagina in de index zijn gedefinieerd, kunnen beschikbaar worden voor gebruik in elk resultaatknooppunt. Categorisering, prijzen, kleuren en miniaturen zijn slechts een paar opties die u op een resultaat kunt toepassen om overtuigender zoekresultaten te produceren.

De resultaatindeling wordt aangepast op basis van de specifieke metagegevens voor uw implementatie. Hier vindt u alle gegevens per resultaat die in de resultaten worden weergegeven, inclusief URL&#39;s van miniatuurafbeeldingen.

Bovendien is het mogelijk om veelvoudige resultaatstreken binnen de pagina, zoals &quot;Aanbevolen Resultaten&quot;te vormen, of afzonderlijke &quot;Producten&quot;en &quot;Inhoud&quot;resultaatsecties. In deze gevallen worden er meerdere resultaatzones opgegeven in de HTML, hoewel facetten alleen aan de primaire resultaatset zijn gekoppeld.

Voorbeeldresultatenknooppunt:

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
   <th colname="col1" class="entry"> <p>Knooppunt </p> </th> 
   <th colname="col2" class="entry"> <p>Bovenliggend knooppunt </p> </th> 
   <th colname="col3" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>resultaten </p> </td> 
   <td colname="col2"> <p>klantresultaten </p> </td> 
   <td colname="col3"> <p>Het containerknooppunt voor resultaatsets van 0-n. Resultaatsets nul betekent dat u zich op een speciale landingspagina zonder resultaten bevindt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>resultaat ingesteld </p> </td> 
   <td colname="col2"> <p>resultaten </p> </td> 
   <td colname="col3"> <p>Een binnenkomende zoekopdracht kan meerdere zoekopdrachten uitvoeren. Elke resultaatset bevat de resultaten voor een specifieke benoemde zoekopdracht die is uitgevoerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>name </p> </td> 
   <td colname="col2"> <p>resultaat ingesteld </p> </td> 
   <td colname="col3"> <p>De naam van de zoekopdracht waartoe de resultatenset behoort. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>resultaat </p> </td> 
   <td colname="col2"> <p>resultaat ingesteld </p> </td> 
   <td colname="col3"> <p>Bevat alle velden die zijn gekoppeld aan een afzonderlijk resultaat voor de resultatenset. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>field </p> </td> 
   <td colname="col2"> <p>resultaat </p> </td> 
   <td colname="col3"> <p>Het kenmerk name definieert de naam van het veld binnen de index die wordt weergegeven. De waarde is de werkelijke waarde voor dat veld. Sommige resultaten kunnen ontbrekende velden bevatten die niet relevant zijn voor dat afzonderlijke resultaat. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Formulier {#section_9E4B99D4FEDC49629F6C7E866F3A7493} doorzoeken

Zoekformulier is opgenomen in de resultatenset zodat klanten hun zoekformulier dynamisch kunnen samenstellen. Deze stap is optioneel. De meeste klanten hebben een vast zoekformulier. Nochtans, staat het klanten toe om te bepalen als de onderzoeksvorm een test&amp;Target doos vereist, die op het hebben van minstens één bedrijfsregel wordt gebaseerd die een test A:B doet. Op dezelfde manier kunnen klanten automatisch de nieuwste automatische aanvulversies van CSS en JavaScript ophalen.

Voorbeeld van XML van zoekformulier:

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
   <th colname="col1" class="entry"> <p>Knooppunt </p> </th> 
   <th colname="col2" class="entry"> <p>Bovenliggend knooppunt </p> </th> 
   <th colname="col3" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>zoekformulier </p> </td> 
   <td colname="col2"> <p>klantresultaten </p> </td> 
   <td colname="col3"> <p>Bevat gegevens voor het besturen van het zoekformulier. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>include-tnt-mbox </p> </td> 
   <td colname="col2"> <p> zoekformulier </p> </td> 
   <td colname="col3"> <p>Technisch gezien hebt u slechts een mbox in het onderzoeksformulier nodig wanneer u minstens één bedrijfsregel hebt die een test A:B test test test Test&amp;Target doet. Dit knooppunt geeft aan of u een box nodig hebt of niet toestaat dat u het aantal treffers op de test&amp;Target-servers verlaagt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>automatisch aanvullen </p> </td> 
   <td colname="col2"> <p>zoekformulier </p> </td> 
   <td colname="col3"> <p>Houses children node related to auto-complete. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>enabled </p> </td> 
   <td colname="col2"> <p>automatisch aanvullen </p> </td> 
   <td colname="col3"> <p>Stel de waarde in op 1 wanneer de zoekaccount automatisch aanvullen gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>css </p> </td> 
   <td colname="col2"> <p> automatisch aanvullen </p> </td> 
   <td colname="col3"> <p> CSS voor automatisch aanvullen. Plaats dit knooppunt zo hoog mogelijk op de pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> form-content </p> </td> 
   <td colname="col2"> <p>automatisch aanvullen </p> </td> 
   <td colname="col3"> <p>Inhoud die in het zoekformulier wordt geïnjecteerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>javascript </p> </td> 
   <td colname="col2"> <p>automatisch aanvullen </p> </td> 
   <td colname="col3"> <p>JavaScript voor automatisch aanvullen. Plaats dit knooppunt zo laag mogelijk op de pagina. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Suggesties {#section_2899FACB9AD84F60B3687C1B4EF09E15}

Klanten kunnen de **[!UICONTROL Did You Mean]**-functionaliteit op drie manieren configureren: doet u suggesties omdat er geen resultaten zijn, zoekt u automatisch naar de eerste suggestie als er geen resultaten zijn of doet u suggesties als gevolg van lage resultaten (als de suggesties een hoger aantal resultaten hebben). Alle suggesties leveren resultaten op.

Dit suggesties knooppunt bevat de termen die geen geslaagde query&#39;s opleveren. De verbinding is ook teruggekeerd zodat kan een klant aan de nieuwe vraag springen.

Voorbeeld van uitvoer voor suggestie vanwege 0 resultaten:

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

Voorbeeld van uitvoer voor automatisch zoeken op basis van een suggestie:

```xml
    <suggestions> 
        <auto-searched>1</auto-searched> 
        <orig-query><![CDATA[arcace]]></orig-query> 
        <suggestions-low-results>0</suggestions-low-results>         
    </suggestions> 
```

Voorbeeld-uitvoer voor suggestie vanwege lage resultaten:

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
   <th colname="col1" class="entry"> <p>Knooppunt </p> </th> 
   <th colname="col2" class="entry"> <p>Bovenliggend knooppunt </p> </th> 
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
   <td colname="col3"> <p> Indien aanwezig, hiermee wordt aangegeven of de zoekopdracht/het verhandelen van de site automatisch is doorzocht op een nieuwe term omdat er geen resultaten zijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>orig-query </p> </td> 
   <td colname="col2"> <p>suggesties </p> </td> 
   <td colname="col3"> <p> Wanneer de plaatsonderzoek/de handel drijft automatisch onderzoek tegen de eerste suggestie, toont de gebruiker-vraag in de vraagknoop het sleutelwoord dat wordt gezocht tegen. Deze knoop toont de originele vraagtermijn. Door deze twee te combineren, kunnen klanten structuren maken zoals "Zoeken naar arcering in plaats van arcering". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>suggesties-lage resultaten </p> </td> 
   <td colname="col2"> <p>suggesties </p> </td> 
   <td colname="col3"> <p>Geeft, indien aanwezig, aan of zoeken/verhandelen van sites suggesties doet vanwege de huidige zoekterm die lage resultaten oplevert en een suggestie die aanzienlijk hogere resultaten oplevert. De twee drempels zijn configureerbaar in <span class="uicontrol"> Bedoelde u </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>suggestie-item </p> </td> 
   <td colname="col2"> <p>suggesties </p> </td> 
   <td colname="col3"> <p>Bevat 0-n knopen die de diverse suggesties wijzen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>link </p> </td> 
   <td colname="col2"> <p>suggestie-item </p> </td> 
   <td colname="col3"> <p>Bevat het pad voor het maken van een koppeling naar de voorgestelde term. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>woord </p> </td> 
   <td colname="col2"> <p>suggestie-item </p> </td> 
   <td colname="col3"> <p> Bevat het voorgestelde woord. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Sjabloon {#section_1E2BB2F274B04F5491A4CCCC38F507BD}

De capaciteit om een ervaring van het klantenonderzoek te schakelen die op de resultaten wordt gebaseerd wordt gesteund. Een deel hiervan is het schakelen tussen verschillende sjablonen met een andere indeling van zoekresultaten. U hebt bijvoorbeeld een sjabloon met een rasterweergave van producten voor wanneer u veel producten hebt. Of u hebt een &#39;spotlight&#39;-sjabloon wanneer u één resultaat weergeeft dat meer details bevat. U kunt ook een sjabloon &#39;Geen resultaten&#39; hebben als een zoekopdracht geen resultaten oplevert. Het sjabloonknooppunt geeft aan welke sjabloon wordt gebruikt om de zoekresultaten weer te geven.

Voorbeeldsjabloon:

```xml
<template><![CDATA[grid]]></template>
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Knooppunt </p> </th> 
   <th colname="col2" class="entry"> <p>Bovenliggend knooppunt </p> </th> 
   <th colname="col3" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>template </p> </td> 
   <td colname="col2"> <p>klantresultaten </p> </td> 
   <td colname="col3"> <p>Hiermee geeft u de naam op van de sjabloon die wordt gebruikt om de zoekresultaten weer te geven. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Gebieden {#section_26C4A947E7B1474A8E37D86D9579B93E}

Gebieden zijn secties van de pagina&#39;s die door bedrijfsregels kunnen worden in- of uitgeschakeld. Een zone kan alle inhoud bevatten, inclusief, maar niet beperkt tot, facetten, zoekopdrachten, broodkruimels, statische inhoud. De zones op de webpagina van de klant moeten worden toegewezen aan dezelfde gebieden als die voor zoeken en verkopen van sites.

Voorbeeld van knooppunten in de zone:

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
   <th colname="col1" class="entry"> <p>Knooppunt </p> </th> 
   <th colname="col2" class="entry"> <p>Bovenliggend knooppunt </p> </th> 
   <th colname="col3" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>zones </p> </td> 
   <td colname="col2"> <p>klantresultaten </p> </td> 
   <td colname="col3"> <p>Bevat 0-n zones. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>zone </p> </td> 
   <td colname="col2"> <p>zones </p> </td> 
   <td colname="col3"> <p> Een afzonderlijk knooppunt voor zones. U kunt meerdere streekknooppunten hebben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>name </p> </td> 
   <td colname="col2"> <p>zone </p> </td> 
   <td colname="col3"> <p>De naam van de zone. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>display </p> </td> 
   <td colname="col2"> <p>1 of 0, die erop wijzen als de streek die aan de streeknaam beantwoordt wordt getoond of verborgen. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Voorbeelden {#reference_64B7D8D228AF4B8D90EDF4DE507B0F84}

Voorbeelduitvoer voor een *-zoekopdracht op een fictieve website met de naam Geometrixx en een voorbeeldpresentatiesjabloon waarmee de voorbeelduitvoer wordt geproduceerd.

* [Voorbeeld-uitvoer](../c-appendices/c-guidedsearchoutput.md#section_515C000A18B847D59097D0A9CCC02636)
* [Voorbeeld van presentatiesjabloon](../c-appendices/c-guidedsearchoutput.md#section_AD42571DFB88491AA7F0FDF0929EBE97)

## Voorbeeld-uitvoer {#section_515C000A18B847D59097D0A9CCC02636}

Voorbeeld van uitvoer voor een *-zoekopdracht op een fictieve website met de naam Geometrixx.

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

## Voorbeeld van presentatiesjabloon {#section_AD42571DFB88491AA7F0FDF0929EBE97}

Hier volgt een voorbeeld van een presentatiesjabloon dat wordt gebruikt om de voorbeelduitvoer hierboven te produceren.

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

