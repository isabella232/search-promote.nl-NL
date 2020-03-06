---
description: ongeldig
seo-description: ongeldig
seo-title: Sjablonen
solution: Target
title: Sjablonen
topic: Appendices,Site search and merchandising
uuid: 78299032-dc23-4dfe-b68f-cd57b2b6d7d8
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a

---


# Sjablonen{#templates}

## Sjablonen {#concept_A5CFB6BD805D49459A96219AF1B17842}

## Sjabloonlabels voor presentatie {#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64}

Een lijst van plaatsonderzoek/merchandising markeringen en attributen voor presentatiemalplaatjes.


Een presentatiemalplaatje is een HTML- dossier dat de markeringen van het presentatiemalplaatje omvat dat het plaatsonderzoek/het merchandising bepaalt. Deze markeringen wijzen erop hoe de onderzoeksresultaten die de klanten zien geformatteerd zijn.

Zie [over sjablonen](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5).

U kunt uit de volgende groepen van de presentatiemarkering selecteren:

* [Verklaringen](../c-appendices/c-templates.md#section_82C5CA734D2941EB858FEFE3B695D2EC)
* [Resultaten](../c-appendices/c-templates.md#section_06F249C9F6AE4B0F8C32117E19DCC905)
* [Facturen](../c-appendices/c-templates.md#section_EA4C5678D5864B89BAB4D0DFE62A4624)
* [Breadcrumb](../c-appendices/c-templates.md#section_9B39B71FA6EC49FA8D88AD8A3BA987F7)
* [Menus](../c-appendices/c-templates.md#section_1D489ADF041F4351A66E5D5742125CA8)
* [Pagenav](../c-appendices/c-templates.md#section_2EE397635C514BBC8D668278EA314F35)
* [Recente zoekopdrachten](../c-appendices/c-templates.md#section_8CD907521F584257B475595B01A5964B)
* [Bedoelde je](../c-appendices/c-templates.md#section_C1EB3B9D8E1242798A6E04609D1E3543)
* [Automatisch aanvullen](../c-appendices/c-templates.md#section_897316BEE1454E839A56B565CA4AF018)
* [Winkel](../c-appendices/c-templates.md#section_A33E25DB5E67404A823BD9618665B773)
* [Zones](../c-appendices/c-templates.md#section_B9B3179E000C42D492E1541F2FE44CB5)
* [Loop-indicatoren](../c-appendices/c-templates.md#section_387322CA0AA843A2ACF2795C328673E9)
* [Diverse talen](../c-appendices/c-templates.md#section_BFE8DC98E26F4D7BB60FEC54D9A5DC6C)

## Verklaringen {#section_82C5CA734D2941EB858FEFE3B695D2EC}

De verklaringen zijn speciale geleid-verklaar markeringen die u bij de bovenkant van een top-level presentatiemalplaatje kunt plaatsen. Om het even welke verdere verklaringen worden genegeerd, met inbegrip van verklaringen in inbegrepen malplaatjes.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;geleid-tevreden-type-kopbal content="content-type"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Door gebrek wordt het presentatiemalplaatje teruggestuurd met een mime-type van tekst/html. U kunt veranderen wat inhoud-type met deze markering wordt gebruikt. </p> <p>Verklaar deze markering zo hoog mogelijk in uw presentatiemalplaatje. Voeg geen andere tekst op de zelfde lijn met deze markering toe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;geleid-xml-verklaar [charset="charset"]&gt; </span> </p> </td> 
   <td colname="col2"> <p> Als u XML terugkeert, kunt u deze markering gebruiken om de verklaring van XML tot stand te brengen. Maak van deze markering de eerste lijn in uw presentatiemalplaatje. Wanneer u deze markering gebruikt, wordt het inhoud-type automatisch geplaatst aan tekst/xml, tenzij u het met <span class="codeph"> </span> &lt;geleid-inhoud-type-kopbal&gt; in de eerste lijn overheerst. Als u geen charset opgeeft, wordt UTF-8 standaard gebruikt. Deze markering resulteert in de volgende output in uw document van XML: </p> <p> <span class="codeph"> &lt;?xml version="1.0" encoding="charset-name" standalone="yes"?&gt; </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Resultaten {#section_06F249C9F6AE4B0F8C32117E19DCC905}

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng 1/31/13--> <span class="codeph"> &lt;guided-results [gsname="search name"]&gt;&lt;/guided-results&gt; </span> </p> </td> 
   <td colname="col2"> <p>De geleide-resultatenmarkering bepaalt de grenzen van een resultatenlijn. Om het even welke reeks resultaten kan worden betreden door een <span class="codeph"> gsname </span> attribuut te specificeren. Als geen <span class="codeph"> gsname </span> wordt gegeven, dan worden de standaardonderzoeksresultaten getoond. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng 1/31/13--> <span class="codeph"> &lt;guided-result-link [gsname="fieldname"] [attr="value"]+&gt;&lt;/guided-result-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Om een verbinding aan een bepaald resultaat tot stand te brengen, gebruik de <span class="codeph"> geleid-resultaat-verbinding </span> markering. Door een <span class="codeph"> gsname- </span> attribuut te definiëren, kunt u een veld van de index gebruiken in plaats van de standaard "loc"-tag die verwijst naar de "search-url". Om het even welke andere attributen, zoals klasse en doel, kunnen eveneens worden overgegaan, die output in de resulterende ankermarkering zijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng 1/31/13--> <span class="codeph"> &lt;guided result-img gsname="fieldname" [attr="value"]+&gt; </span> </p> </td> 
   <td colname="col2"> <p>De <span class="codeph"> &lt;geleide-resultaat-img&gt; </span> markering helpt beeldmarkeringen tot stand te brengen eerder dan het inbedden variabelen binnen een ruwe <span class="codeph"> img </span> markering. </p> <p>Specificeer het gebied voor de beeldweg in de <span class="codeph"> gsname </span> attributen te gebruiken. Het resultaat is een <span class="codeph"> img- </span> markering met om het even welke standaardattributen van HTML die u bepaalde, door overging. Zo, het volgende voorbeeld: </p> <p> <code class="syntax html"> &lt;guided-result-img&nbsp;gsname="thumbnail" 
      &nbsp;class="thumb"&nbsp;border="0"/&gt; </code> </p> <p>wordt: </p> <p> <code class="syntax html"> &lt;img&nbsp;src="prod8172.jpg"&nbsp;class="thumb" 
      &nbsp;border="0"/&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 1/31/13; search-eng version does not have [escape...] Added ijson on 8/28/2015--> <span class="codeph"> &lt;guided result-field gsname="fieldname" [escape="html|url|js|json|ijson|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p> Om het even welk stuk informatie in de resultaten wordt getoond als <span class="codeph"> &lt;geleid-resultaat-gebied&gt; </span> markering (behalve wanneer het gebruiken van auto-genererende markeringen zoals de <span class="codeph"> &lt;geleid-resultaat-img&gt; </span> markering). </p> <p>Specificeer de naam van het de indexgebied van het Onderzoek in <span class="codeph"> gsname </span>. Het nauwkeurige overgegaane koord is output in het malplaatje. </p> <p>U kunt een ontsnappingsoptie specificeren als u dit gebied wilt ontsnapten verschillend van wat in het vervoermalplaatje werd gespecificeerd. </p> <p>Deze codering wordt toegepast bovenop wat het coderen in het vervoermalplaatje werd gespecificeerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <span class="codeph"> &lt;guided-if[-not]-result-field gsname="fieldname&gt;&lt;/guided-if-resultaat-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze reeks voorwaardelijke markeringen is waar als er inhoud op het specifieke gebied aan vertoning is. Als geen inhoud bestaat, is de voorwaarde vals. U kunt de markeringen gebruiken om te beslissen of het omringende HTML of niet wordt getoond als een waarde niet bestaat, of als een verschillend beeld, etc. wordt getoond. </p> <p> <code class="syntax html"> &lt;guided-if-result-field&nbsp;gsname="thumbnail"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-result-img&nbsp;gsname="thumbnail"&nbsp;class="thumb"&nbsp;/&gt; 
      &lt;guided-else-result-field&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;img&nbsp;src="nothumb.jpg"&nbsp;class="nothumb"&nbsp;/&gt; 
      &lt;/guided-if-result-field&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <code> &lt;guided-if[-not]-result-wrap&gt; 
      &lt;guided-else-result-wrap&gt; 
      &lt;/guided-if[-not]-result-wrap&gt; </code> </p> </td> 
   <td colname="col2"> <p>Wanneer het tonen van resultaten in kolommen, wordt deze markering gebruikt om te identificeren of het huidige resultaat het eind van een kolom merkt. </p> <p>Wanneer de voorwaarde Van Boole waar is, wordt HTML toegevoegd aan het eind van het resultaat om van de rij te eindigen en nieuwe te beginnen. Wanneer het de laatste is, is een nieuwe rij niet begonnen. </p> <p>Zie <span class="codeph"> &lt;geleid-als-niet-laatste&gt; </span> om meer over die markering te leren. </p> <p> <code class="syntax html"> &lt;guided-if-result-wrap&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/div&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-not-last&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;div&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-not-last&gt; 
      &nbsp;&lt;/guided-if-result-wrap&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version, 1/31/13--> <span class="codeph"> &lt;guided-results-found [gsname="search name"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Keert 1 terug als het achterste-eind onderzoeksverzoek resultaten en 0 terugkeerde als het niet deed. Als geen <span class="codeph"> gsname </span> wordt gespecificeerd, veronderstelt de markering het primaire onderzoek. Deze markering is nuttig om logica tot routines over te gaan JavaScript. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;geleid-resultaat-totaal [gsname="zoeknaam"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Keert het totale aantal resultaten in de gespecificeerde resultatenreeks terug. Veronderstelt het standaardonderzoek wanneer geen <span class="codeph"> gsname </span> wordt gegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-results-lower [gsname="search name"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Keert het resultaataantal van het lagere resultaat op de pagina voor de gespecificeerde resultatenreeks terug. Veronderstelt het standaardonderzoek wanneer geen <span class="codeph"> gsname </span> wordt gegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;geleid-resultaat-bovenaan [gsname="zoeknaam"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Keert het resultaataantal van het hogere resultaat op de pagina voor de gespecificeerde resultatenreeks terug. Veronderstelt het standaardonderzoek wanneer geen <span class="codeph"> gsname </span> wordt gegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version 1/31/13--> 

    &amp;lt;/geleid-als[-niet]-resultaat-gevonden&amp;gt; &lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>Toont inhoud wanneer de resultaten worden gevonden. Of, toont geen resultatenHTML wanneer de resultaten niet worden gevonden. </p> <p> <code class="syntax html"> &lt;guided-if-results-found&nbsp;gsname="products"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-results&nbsp;gsname="products"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;... 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-results&gt; 
      &lt;guided-else-results-found&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;No&nbsp;results&nbsp;were&nbsp;found. 
      &lt;/guided-if-results-found&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;geleid resultaat-titel/&gt; </span> </p> </td> 
   <td colname="col2"> <p>De <span class="codeph"> &lt;geleide-resultaat-titel&gt; </span> markering geeft waarde van het gebied van het malplaatje van het titelvervoer dat met <span class="codeph"> &lt;title&gt; </span> vervoermarkering wordt gespecificeerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;beschrijving van het geleide resultaat/&gt; </span> </p> </td> 
   <td colname="col2"> <p>De <span class="codeph"> &lt;geleide-resultaat-beschrijving&gt; </span> markering geeft waarde van het gebied van de beschrijvingsmalplaatje dat met <span class="codeph"> </span> &lt;description&gt; de vervoermarkering wordt gespecificeerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;geleid resultaat-lc/&gt; </span> </p> </td> 
   <td colname="col2"> <p>De &lt; <span class="codeph"> geleide-resultaat-loc&gt; </span> markering geeft waarde van het gebied van het lokale vervoermalplaatje dat met <span class="codeph"> &lt;loc&gt; </span> vervoermarkering wordt gespecificeerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> 

    &amp;lt;/geleid-als-resultaat-gebied&amp;gt; &lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>Waar als er inhoud op het specifieke gebied aan vertoning is. Als geen inhoud bestaat, is de voorwaarde vals. Gebruik de markeringen om te beslissen of omringend HTML of niet wordt getoond als een waarde niet bestaat, of als een verschillend beeld, etc. wordt getoond. </p> <p> <code class="syntax html"> &lt;guided-if-result-field&nbsp;gsname="thumbnail"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-result-img&nbsp;gsname="thumbnail"&nbsp;class="thumb"/&gt; 
      &lt;guided-else-result-field&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;img&nbsp;src="nothumb.jpg"&nbsp;class="nothumb"/&gt; 
      &lt;/guided-if-result-field&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;geleid resultaat-attribuut-lijst gsname="tabelnaam"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze markering verstrekt een lijn door attributenlijst die in het vervoermalplaatje wordt bepaald met <span class="codeph"> &lt;attribuut_table&gt; </span> vervoermarkering. Er is <span class="codeph"> &lt;geleid-resultaat-attribuut-lijst-gebied&gt; </span> markering voor het tonen van het gebiedswaarden van de attributenlijst. Ook is het mogelijk om duidelijke <span class="codeph"> geleid-resultaat-gebied </span> markeringsbinnenlijn te gebruiken voor het tonen van andere resultaatgebieden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided result-attribuut-table-field gsname="fieldname" [escape="html|url|js|json|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Het gebied van de attributenlijst van vertoningen zoals die in vervoermalplaatje wordt bepaald. </p> <p> 

    ...
    
    &amp;lt;ul&amp;gt;
    
    &amp;lt;geleide-resultaat-attribuut-tabel&amp;nbsp;gsname=&quot;downloads&quot;&amp;gt;
    &amp;nbsp;amp;nbsp;&amp;nbsp;&amp;nbsp;
    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;amp;amp;nbsp;&amp;nbsp;&amp;nbsp; sp;&amp;nbsp;&amp;lt;a&amp;nbsp;href=&quot;&amp;lt;guided-result-attribuut-table-field&amp;nbsp;gbsp;sap=&quot;download_link&quot;&amp;nbsp;/&amp;gt;
    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;nbsp;
    &amp;nbsp;
    &amp;nbsp;&amp;nbsp;&amp;bsp;nbsp;&amp;nbsp;nbsp;amp;lt;/a&amp;gt;&amp;nbsp;(&amp;nbsp;lt;geleide-resultaat-veld&amp;nbsp;nbsp;gp=&quot;title&quot;/&amp;gt;
    &amp;nbsp;&amp;nbsp;&amp;lt&amp;;gt;
    
    &amp;lt;/geleid-resultaat-attribuut-attribuut-lijst&amp;gt;
    
    &amp;lt;/ul&amp;gt;...
    
    &amp;lt;/geleide-resultaten&amp;gt; &lt;/code> &lt;/p> &lt;/td>
</tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW for S&P 8.17.0 release in October 2014--> <span class="codeph"> &lt;guided-trace [gsname="zoeknaam"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Output de spoorinformatie die binnen de spoorgegevens binnen de algemene sectie van de JSON gegevensoutput door het vervoermalplaatje voor de bepaalde opsporing wordt gevonden. </p> <p>Als geen onderzoeksnaam wordt gegeven, wordt het <span class="codeph"> gebrek verondersteld </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>19 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW for S&P 8.17.0 release on October 30, 2014)--> <span class="codeph"> &lt;geleid resultaat-spoor/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Output de inhoud JSON die binnen de resultaten &gt; spoorinformatie van de JSON gegevensoutput door het vervoermalplaatje voor het huidige onderzoeksresultaat wordt gevonden. </p> <p>Deze markering is slechts geldig binnen de <span class="codeph"> &lt;geleide-resultaten&gt;&lt;/geleide-resultaten&gt; </span> lijn. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Facturen {#section_EA4C5678D5864B89BAB4D0DFE62A4624}

De gebieden zijn navigatie componenten die u in onderzoeksresultaten laten boren. U kunt de facetmarkeringen gebruiken om diverse facetten op uw presentatiemalplaatje te tonen. U refereert facetten door naam.

Zie [Over Facets](../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5).

Zie [over de facetrails](../c-about-design-menu/c-about-facet-rails.md#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB).

Zie [over Dynamische Facets](../c-about-design-menu/c-about-dynamic-facets.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW 02/27/2014--> <span class="codeph"> &lt;geleide-dynamische-facetten&gt;&lt;/geleide-dynamische-facetten&gt; </span> </p> </td> 
   <td colname="col2"> 
    <!--NEW 2/2/2014--> <p>Een het van een lus voorzien context voor om het even welke dynamische facetten voor een bepaald onderzoek. </p> <p>De markering van het <span class="codeph"> &lt;geleide-facet&gt; </span> van het presentatiemalplaatje wordt uitgegeven zodat het attribuut gsname automatisch door de <span class="codeph"> &lt;geleide-dynamisch-facetten&gt; van een lus voorziende context wordt verstrekt </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-display-name gsname=" <span class="varname"> facetname </span>"/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Keert het vertoningsetiket van het facet terug. </p> <p>Als het facet de <span class="codeph"> &lt;display-name&gt; </span> markering op het vervoermalplaatje gebruikt, wordt de inhoud van die markering het etiket. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;geleidende facet-rail&gt;&lt;/geleide facet-rail&gt; </span> </p> </td> 
   <td colname="col2"> <p> Bepaalt een sectie op het presentatiemalplaatje dat als herhalend patroon voor elk facet in de facetspoorstaaf wordt gebruikt. </p> <p> Elk facet dat tot de facetspoorstaaf behoort gebruikt dit deel om zijn output te evalueren. </p> <p>Het volgende is een voorbeeld van een facetspoorstaaf: </p> <p> <code class="syntax html"> &lt;guided-facet-rail&gt; 
      &nbsp;&nbsp;&lt;guided-facet&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-display-name/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;... 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet&gt; 
      &nbsp;&nbsp;&lt;/guided-facet-rail&gt; </code> </p> <p>Merk op dat de volgende markeringen geen <span class="codeph"> gsname </span> attribuut wanneer binnen <span class="codeph"> </span> &lt;geleid-facet-rail&gt; markering nodig hebben aangezien de waarde dynamisch in onderzoekstijdstip wordt bepaald en behoorlijk wordt gesubstitueerd: </p> 
    <ul id="ul_5B5ACAFD2B8848DDB27471AB9DA7BE6E"> 
     <li id="li_5A07E78D51FE4708879DD742C877FFFF">begeleid facet </li> 
     <li id="li_B875DCACD7AB4FC890A456A6939AB657">begeleide-facet vertoning-naam </li> 
     <li id="li_B70450749E864DE7BA401E3CD6EF5EB3">aantal begeleide facetten </li> 
     <li id="li_DECDF5EF6FF7454F86C236D322F2BFEA">gelaatsverbinding ongedaan maken </li> 
     <li id="li_176949227AC14E8CA643A419E10F7B5A">geleid-facet-undo-weg </li> 
     <li id="li_B32D981281744462BC680F6EFEAC0069">begeleid gedrag </li> 
    </ul> <p>De soortcriteria op de <span class="wintitle"> pagina van de Spoorstaaf van het Gebied </span> bepalen de positie van de facetten. U kunt de soortorde van de drop-down lijst van de Methode van de Facets van de Soort kiezen. </p> <p> 
     <!--NEW 02/27/2014-->Deze markering kan naar keuze een waarde van de gsname attributen van <span class="codeph"> _dynamic_facets goedkeuren </span>, die een het van een lus voorzien context voor om het even welke dynamische facetten voor dit onderzoek verstrekt. Deze vooraf gedefinieerde facetrail wordt ook in de Business Rules user interface voor action <span class="codeph"> push facet X in facet rail '_dynamic_facets' blootgesteld aan positie Y </span>". </p> <p>Zie <a href="../c-about-design-menu/c-about-facet-rails.md#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB" format="dita" scope="local"> over de facetrails </a>. </p> <p>Zie ook <a href="../c-about-design-menu/c-about-dynamic-facets.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> over Dynamische Facets </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match current search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet gsname=" <span class="varname"> facetname </span>" height=" <span class="varname"> 60px </span>" width=" <span class="varname"> 120px </span>"&gt;&lt;/guided-facet&gt; </span> </p> </td> 
   <td colname="col2"> <p>Gebruik de <span class="codeph"> geleide-facet </span> markering om een gebied te bepalen waarin alle facetmarkeringen op een specifiek facet betrekking hebben. Deze markering is ook een markering Van Boole die alle inhoud verbergt als geen waarden in het facet bestaan. In een dergelijk geval heeft het geen zin de facetwaarden uit te dragen). </p> <p>De hoogte en breedteattributen zijn facultatief en de afmetingen worden gespecificeerd in pixel (px). De visuele Bouwer van de Regel (VRB) gebruikt deze twee attributen, en toont een gestippelde doos als interactieve placeholder wanneer het facet verborgen is. </p> <p> Wanneer de vertoningsnaam in het facet is en het facet verborgen is, is de naam ook verborgen. Nochtans, als de naam buiten het facet is, kunt u de naam verbergen slechts als een <span class="codeph"> streekmarkering of een </span> geleid-als-facet-zichtbare <span class="codeph"> </span> markering rond het worden verpakt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW, brought in from search-eng version, 1/31/13--> <span class="codeph"> &lt;guided-if[-not]-facet-long [gsname="facetname"]&gt;&lt;/guided-if[-not]-facet-long&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze voorwaardelijke markering is waar wanneer het aantal facetwaarden over de lengte-drempel is die in de configuratie wordt bepaald. Gebruik het om een facet als verschillend element UI (zoals een beknot lijst of een roldoos) te tonen wanneer de lijst te lang is. </p> <p> <code class="syntax xml"> &lt;guided-facet&nbsp;name="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-long&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;select&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-option&nbsp;/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/select&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-long&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-value-link&gt;&lt;guided-facet-value&nbsp;/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-long&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>U kunt deze voorwaarde buiten de context van een genoemd <span class="codeph"> geleid-facet </span> blok ook gebruiken door een specifiek facet direct door gebruik van de <span class="codeph"> gsname </span> attributen van verwijzingen te voorzien. </p> <p> <code class="syntax html"> &lt;guided-if-facet-long&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;The&nbsp;category&nbsp;facet&nbsp;is&nbsp;very&nbsp;long! 
      &lt;/guided-if-facet-long&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW, brought in from search-eng version, 1/31/13--> <span class="codeph"> &lt;guided-if[-not]-facet-selected [gsname="facetname"]&gt;&lt;/guided-if[-not]-facet-selected&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze voorwaardelijke markering is waar wanneer het facet minstens eens wordt geklikt en een facetwaarde momenteel wordt geselecteerd. Het wordt gebruikt om de markeringen van HTML of van gs te tonen of te verbergen afhankelijk van of een facet werd geklikt. </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;name="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This&nbsp;facet&nbsp;has&nbsp;been&nbsp;selected.&nbsp;&nbsp;You&nbsp;can&nbsp;no&nbsp;longer&nbsp;refine&nbsp;it. 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-value-link&gt;&lt;guided-facet-value&nbsp;/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-selected&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>U kunt deze voorwaarde buiten de context van een genoemd <span class="codeph"> geleid-facet </span> blok ook gebruiken door een specifiek facet direct door gebruik van de <span class="codeph"> gsname </span> attributen van verwijzingen te voorzien. </p> <p> <code> &lt;guided-if-facet-selected&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;The&nbsp;category&nbsp;facet&nbsp;is&nbsp;selected! 
      &lt;/guided-if-facet-selected&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW, brought in from search-eng version, 1/31/13--> <span class="codeph"> &lt;guided-if[-not]-facet-single [gsname="facetname"]&gt;&lt;/guided-if[-not]-facet-single&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze voorwaardelijke markering is waar wanneer er slechts één facetwaarde is. Gebruik de markering om de vertoning van het facet te veranderen wanneer het niet de capaciteit heeft om de resultaten te raffineren. </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;name="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-single&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Facet&nbsp;is&nbsp;not&nbsp;refinable. 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-single&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-value-link&gt;&lt;guided-facet-value&nbsp;/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-single&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>U kunt deze voorwaarde buiten de context van een genoemd <span class="codeph"> geleid-facet </span> blok ook gebruiken door een specifiek facet direct door gebruik van de <span class="codeph"> gsname </span> attributen van verwijzingen te voorzien. </p> <p> <code class="syntax html"> &lt;guided-if-facet-single&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;There&nbsp;is&nbsp;only&nbsp;one&nbsp;value&nbsp;in&nbsp;the&nbsp;category&nbsp;facet! 
      &lt;/guided-if-facet-single&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> 
     <!--Added 7/15/2014--> <span class="codeph"> &lt;guided-if[-not]-facet-multiselect [gsname="facetname"]&gt;&lt;/guided-if[-not]-facet-multiselect&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze voorwaardelijke markering is waar wanneer het facet multi-select is. Gebruik de markering om de vertoning van het facet te veranderen binnen <span class="codeph"> &lt;geleide-facet-rail&gt; </span> of <span class="codeph"> &lt;geleide-dynamisch-facetten&gt; </span> markeringen. </p> <p> 

    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;lt;geleide-if-facet-multiselect&amp;gt;
    &amp;nbsp;....
    &amp;nbsp;&amp;lt;geleid-else-facet-multiselect&amp;gt;
    &amp;nbsp;...
    &amp;nbsp;&amp;lt;/geleide-if-facet-multiselect&amp;gt;
    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;...
    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;lt;/geleide-facet&amp;gt;
    &amp;nbsp;&amp;nbsp;&amp;lt;/geleide-facet-rail&amp;gt; &lt;/code> &lt;/p> &lt;/td>
</tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet-waardes [gsname=" <span class="varname"> facetname </span>"]&gt;&lt;/guided-facet-waardes&gt; </span> </p> </td> 
   <td colname="col2"> <p>Dit is de de iteratormarkering van de gevelwaarde lijn. U kunt het binnen de context van een genoemd <span class="codeph"> geleid-facet </span> blok bepalen, waarbij u <span class="codeph"> gsname kunt weglaten <span class="varname"> </span> </span>. Of, u kunt het buiten om het even welk <span class="codeph"> geleid-facet </span> blok bepalen, maar het zou de <span class="codeph"> <span class="varname"> gsname </span> - </span> attributen vereisen om te identificeren welke reeks facetwaarden worden getoond. </p> <p>U kunt deze markering ook gebruiken om de facetwaarden buiten de context van een genoemd <span class="codeph"> geleid-facetblok te tonen </span> . U verwijst rechtstreeks een specifiek facet door de <span class="codeph"> gsname <span class="varname"> - </span> </span> attributen te gebruiken. </p> <p> <code class="syntax html"> &lt;script&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;registerFacetValues('category',&nbsp;'&lt;guided-facet-values&nbsp;gsname="category"&gt;&lt;guided-facet-value/&gt;,&lt;/guided-facet-values&gt;'); 
      &lt;/script&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet-waarde [escape="html|url|js|json|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Output het koord van de huidige facetwaarde. </p> <p>Door gebrek is de waarde ontsnapte HTML. U kunt de vluchtoptie gebruiken om te veranderen hoe de waarde is ontsnapt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;aantal geleidefacetten/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Output het aantal resultaten die de huidige facetwaarde aanpassen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW, brought in from search-eng version, 1/31/13--> <span class="codeph"> &lt;geleide-facet-waarde-link [attr="waarde"]+&gt;&lt;/geleide-facet-waarde-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Creeert een verbinding rond het koord van de facetwaarde voor de plaatsbezoeker om te klikken. De weg wordt automatisch geproduceerd om de resultaten door de huidige facetwaarde te versmallen. Het steunt het overgaan van om het even welke attributen direct tot de ankermarkering. </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-value-link&nbsp;class="facetlink"&gt;&lt;guided-facet-value&nbsp;/&gt;&lt;/guided-facet-value-link&gt; 
      &lt;/guided-facet-values&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version 1/31/13--> <code> &lt;guided-if-facet-value-selected&gt; 
      &lt;guided-else-facet- 
      value-selected&gt; 
      &lt;/guided-if-facet-value-selected&gt; </code> </p> </td> 
   <td colname="col2"> <p>Verandert de vertoning van de facetwaarde wanneer het momenteel wordt geselecteerd. Als het al is gekozen, is het in de meeste gevallen niet meer met elkaar te verbinden. </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-value-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;b&gt;&lt;guided-facet-value/&gt;&lt;/b&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-value-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt;&nbsp;&nbsp;&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-value-selected&gt; 
      &lt;/guided-facet-values&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version 1/31/13--> 

    &amp;lt;/guided-if[-not]-facet-waarde-spook&amp;gt; &lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>Verandert de vertoning van de facetwaarde wanneer het een spookwaarde is. Wanneer een facetwaarde een spookwaarde is, wordt het typisch getoond in cursieve teksten om erop te wijzen dat de waarde mist of "ghosted". </p> <p>Het volgende codeuittreksel is een voorbeeld van een facetblok: </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-value-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;b&gt;&lt;guided-facet-value&nbsp;/&gt;&nbsp;(&lt;guided-facet-count&nbsp;/&gt;)&lt;/b&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-value-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-value-ghost&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;i&gt;&lt;guided-facet-value&nbsp;/&gt;&nbsp;(0)&lt;/i&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-value-ghost&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&nbsp;class="link"&gt;&lt;guided-facet-value&nbsp;/&gt;&lt;/guided-facet-link&gt;&nbsp;(&lt;guided-facet-count&nbsp;/&gt;) 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-value-ghost&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-value-selected&gt; 
      &lt;/guided-facet-values&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet-undo-link gsname=" <span class="varname"> facetname </span>"&gt;&lt;/guided-facet-undo-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Toont ongedaan maken verbinding voor een bepaald facet. Als er multi-select facetten zijn, schrapt deze verbinding alle waarden van het bepaalde facet. Geef het facet een naam. Als het facet momenteel niet wordt geselecteerd dan is de verbinding de huidige weg. </p> <p>Het volgende is een voorbeeld van het gebruik van deze markering: </p> <p> <code class="syntax html"> &lt;guided-if-facet-selected&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-undo-link&nbsp;gsname="category"&gt;Undo&nbsp;Category&lt;/guided-facet-undo-link&gt; 
      &lt;/guided-if-facet-selected&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <varname></varname> </p> </td> 
   <td colname="col2"> <p>Deze voorwaardelijke markering is waar wanneer het aantal facetwaarden over de lengte-drempel is die in de configuratie wordt bepaald. Gebruik het om een facet als verschillend gebruikersinterfaceelement (zoals een beknot lijst of een roldoos) te tonen wanneer de lijst te lang is. </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-long&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;div&nbsp;class="long_facet"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/div&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-long&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;div&nbsp;class="facet"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/div&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-long&gt; 
      &nbsp;&lt;/guided-facet&gt; </code> </p> <p>U kunt deze voorwaarde buiten de context van een genoemd <span class="codeph"> geleid-facet </span> blok ook gebruiken door een specifiek facet direct door gebruik van de <span class="codeph"> <span class="varname"> gsname </span> - </span> attributen van verwijzingen te voorzien. </p> <p> <code class="syntax html"> &lt;guided-if-facet-long&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The&nbsp;category&nbsp;facet&nbsp;is&nbsp;very&nbsp;long! 
      &lt;/guided-if-facet-long&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-facet-selected [gsname="facetname"]&gt; 
      &lt;guided-else-facet-selected&gt;&lt;/guided-if-facet-selected&gt; </code> </p> </td> 
   <td colname="col2"> <p>Deze voorwaardelijke markering is waar wanneer het facet minstens eens wordt geklikt en een facetwaarde momenteel wordt geselecteerd. Het kan worden gebruikt om de markeringen van HTML of van gs te tonen of te verbergen afhankelijk van of een facet wordt geklikt. </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This&nbsp;facet&nbsp;has&nbsp;been&nbsp;selected.&nbsp;&nbsp;You&nbsp;can&nbsp;no&nbsp;longer&nbsp;refine&nbsp;it. 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-selected&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>U kunt deze voorwaarde buiten de context van een genoemd <span class="codeph"> geleid-facet </span> blok ook gebruiken door een specifiek facet direct door gebruik van de <span class="codeph"> gsname </span> attributen van verwijzingen te voorzien. </p> <p> <code class="syntax html"> &lt;guided-if-facet-selected&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The&nbsp;category&nbsp;facet&nbsp;is&nbsp;selected! 
      &lt;/guided-if-facet-selected&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> <varname></varname> </p> </td> 
   <td colname="col2"> <p>Deze voorwaardelijke markering is waar wanneer er slechts één facetwaarde is. Het kan worden gebruikt om de vertoning van het facet te veranderen wanneer het niet de capaciteit heeft om de resultaten te raffineren. </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-single&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Facet&nbsp;is&nbsp;not&nbsp;refinable. 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-single&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-single&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>U kunt deze voorwaarde buiten de context van een genoemd <span class="codeph"> geleid-facet </span> blok ook gebruiken door een specifiek facet direct door gebruik van de <span class="codeph"> <span class="varname"> gsname </span> - </span> attributen van verwijzingen te voorzien. </p> <p> <code class="syntax html"> &lt;guided-if-facet-single&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;There&nbsp;is&nbsp;only&nbsp;one&nbsp;value&nbsp;in&nbsp;the&nbsp;category&nbsp;facet! 
      &lt;/guided-if-facet-single&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>19 </p> </td> 
   <td colname="col1"> <p> <varname></varname> </p> </td> 
   <td colname="col2"> <p>Deze voorwaarde laat u controleren of heeft het gespecificeerde facet om het even welke waarden bij allen. Je kunt het gebruiken om een ander facet te tonen in plaats van een lege. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>20 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-total-count gsname=" <span class="varname"> facetname </span>"/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Output het totale aantal resultaten die binnen het bepaalde facet zijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>21 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-waarde gsname=" <span class="varname"> geassocieerde waarde van het douanefacet </span>" [escape="html|url|js|json|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Output het koord van een waarde die met het facet wordt geassocieerd. U kunt 0 of meer gebieden hebben verbonden aan een facet. Het hebben van bijbehorende gebieden is zeldzaam en om dergelijke te steunen vormt u het vervoermalplaatje. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>22 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-facet-waarde gsname=" <span class="varname"> bijbehorende waarde van het douanefacet </span>"/&gt;&lt;geleid-anders-facet-waarde&gt;&lt;/geleid-als-facet-waarde&gt; </span> </p> </td> 
   <td colname="col2"> <p>Tests als de facetwaarde een bijbehorende gebiedswaarde heeft. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>23 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-link [attr=" <span class="varname"> value </span>"]+&gt;&lt;/guided-facet-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Creeert een verbinding rond het koord van de facetwaarde voor de klant om te klikken. De weg wordt automatisch geproduceerd om de resultaten door de huidige facetwaarde te versmallen. Het steunt het overgaan van om het even welke attributen direct tot de ankermarkering. </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&nbsp;class="facetlink"&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt; 
      &lt;/guided-facet-values&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>24 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-value-path [escape="html|url|js|json|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Creeert uw eigen verbinding aan een facetwaarde. </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-lt/&gt;a&nbsp;href="&lt;guided-facet-value-path/&gt;"&lt;guided-gt/&gt;&lt;guided-facet-value/&gt;&lt;/a&gt; 
      &lt;/guided-facet-values&gt; </code> </p> <p>Door gebrek, is de waarde ontsnapte URL. U kunt, echter, een andere laag van het coderen toevoegen door te specificeren welke wijze van het ontsnappen u als vluchtparameter wilt gebruiken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>25 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;geleide-facet-waarde-kinderen&gt;&lt;/geleide-facet-waarde-kinderen&gt; </span> </p> </td> 
   <td colname="col2"> <p>Zoals <span class="codeph"> </span> &lt;geleid-facet-waarden&gt; door elke facetwaarde herhalen, herhaalt deze markering door alle kindwaarden van een genesteld facet. Binnen deze markering, gebruik de typische facetmarkeringen voor het creëren van verbindingen, het creëren maak verbindingen ongedaan, en het tonen van facetwaarden ongedaan. Deze markering moet binnen <span class="codeph"> &lt;geleid-facet-waarden&gt; zijn </span> omdat het genestelde van een lus voorzien. </p> <p>Een voorbeeld om deze markering te gebruiken is het volgende: </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&lt;guided-facet-link&nbsp;title='&lt;guided-facet-value&nbsp;/&gt;'&gt;&lt;guided-facet-value&nbsp;/&gt;&nbsp;(&lt;guided-facet-count&nbsp;/&gt;)&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&lt;guided-if-facet-value-has-children&gt; 
      &nbsp;&nbsp;&nbsp;&lt;guided-facet-value-children&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&nbsp;title='&lt;guided-facet-value&nbsp;/&gt;'&gt;&lt;guided-facet-value&nbsp;/&gt;&nbsp;(&lt;guided-facet-count&nbsp;/&gt;)&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&lt;/guided-facet-value-children&gt; 
      &nbsp;&nbsp;&lt;/guided-if-facet-value-has-children&gt; 
      &lt;/guided-facet-values&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>26 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-facet-value-has-children&gt; 
      &lt;guided-else-facet- 
      value-has-children&gt; 
      &lt;/guided-if-facet-value-has-children&gt; </code> </p> </td> 
   <td colname="col2"> <p>Tests als de huidige facetwaarde kindwaarden heeft. Aanbevolen om te gebruiken alvorens de <span class="codeph"> &lt;geleide-facet-waarde-kinderen&gt; </span> markeringen te gebruiken. De "else"clausule is facultatief. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>27 </p> </td> 
   <td colname="col1"> <p> 

    &amp;lt;geleid-else[-not]-facet-waarde-boven-lengte-drempel&amp;gt;
    
    &amp;lt;/geleid-als[-niet]-facet-waarde-boven-lengte-drempel&amp;gt; &lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>Bepaalt als de huidige facetwaarde binnen de facet-waarden lijn, boven de lengtedrempel is. Het wordt typisch gebruikt aan slechts vertoningswaarden onder de drempel op een lang facet (tenzij de gebruiker eerder een "zie meer"verbinding die onder het facet wordt getoond selecteerde). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>28 </p> </td> 
   <td colname="col1"> <p> 

    &amp;lt;geleide-else[-not]-facet-waarde-evenaart-lengte-drempel&amp;gt;
    
    &amp;lt;/geleid-als[-niet]-facet-waarde-evenaart-lengte-drempel&amp;gt; &lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>Bepaalt als de huidige facetwaarde binnen de facet-waarden lijn, aan de lengtedrempel gelijk is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>29 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;geleid-facet-waarde-undo-link&gt;&lt;/geleid-facet-waarde-undo-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Toont ongedaan maken verbinding voor een bepaalde geselecteerde facetwaarde. Gebruik het om te tonen undo verbinding naast een geselecteerde facetwaarde. Omdat deze undo verbinding slechts ongedaan maakt maakt die bepaalde geselecteerde waarde, verschilt het van <span class="codeph"> &lt;geleid-facet-undo-link&gt; </span> die alle geselecteerde waarden schrapt. </p> <p> <p>Opmerking:  Als het facet geen multi-select gedrag heeft dan hebben twee undo verbindingen het zelfde gedrag. Namelijk kan het facet slechts één geselecteerde waarde hebben. </p> </p> <p>Als het facet momenteel niet wordt geselecteerd dan is de verbinding de huidige weg. Gebruik deze markering slechts binnen een <span class="codeph"> geleid-facet-waarden </span> lijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>30 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;geleid-facet-waarde-undo-weg/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Maak je eigen facetwaarde en maak de link ongedaan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>31 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-undo-path gsname=" <span class="varname"> facetname </span>"/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Maak je eigen facet los link. </p> <p> Gelijkaardig aan de <span class="codeph"> &lt;geleid-facet-undo-link&gt; </span> markering behalve dat geeft het u de ruwe weg om uw te bouwen ongedaan maak verbinding ongedaan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>32 </p> </td> 
   <td colname="col1"> <p> <varname></varname> </p> </td> 
   <td colname="col2"> <p>Voorwaardelijk toon HTML wanneer het bepaalde facet de geselecteerde of enige waarde "waarde"heeft. Deze reeks markeringen wordt vaak gebruikt om een facet te tonen dat op de waarde wordt gebaseerd die in een ander facet wordt geselecteerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>33 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-gedrag gsname=" <span class="varname"> facetname </span>"/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Bepaal het gedrag van een facet, zoals normaal, kleverig, of multi-uitgezochte. Het is nuttig voor klanten die de resultaten van XML ontvangen en willen dynamisch veranderen hoe het facet gebaseerd op zijn gedrag wordt getoond. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>34 </p> </td> 
   <td colname="col1"> <p> <varname></varname>

    &amp;lt;/guided-if-facet[-not]-visible&amp;gt; &lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>De inhoud dat deze markeringsomslag of verborgen of onthuld gebaseerd op de zichtstatus van het facet is. Als een bedrijfsregel het facet verbergt of direct openbaart, wordt om het even welke inhoud binnen het facet verborgen of onthuld. Het is niet noodzakelijk dat deze markeringen rond het facet verpakken. </p> <p> Een gemeenschappelijk gebruik voor deze markering moet de vertoningsnaam verbergen wanneer de naam buiten het facet is. Het verpakken van deze markering rond de vertoningsnaam maakt de naam verdwijnen wanneer het facet wordt verborgen. </p> <p>Deze markering vervangt de streek en heeft veel van de zelfde prestatiesvoordelen zoals het gebruiken van streken. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Breadcrumb {#section_9B39B71FA6EC49FA8D88AD8A3BA987F7}

Zie [over Breadcrumbs](../c-about-design-menu/c-about-breadcrumbs.md#concept_FB8A943C594A4A1593B118141DA61F03).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-breadcrumb [gsname=" <span class="varname"> breadcrumbname </span>"]&gt;&lt;/geleide breadcrumb&gt; </span> </p> </td> 
   <td colname="col2"> <p>De lijnmarkering voor de broodkruimel. Om het even welke inhoud binnen tussen de het openen en sluitende markeringen wordt herhaald voor elk vraag-aantal van de huidige staat. </p> <p>Als <span class="codeph"> gsname <span class="varname"> </span> </span> wordt weggelaten, dan wordt de broodkruimel genoemd "gebrek"gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-breadcrumb-link [gsname="goto|remove|drop"] [attr="value"]+&gt;&lt;/geleide-breadcrumb-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Creeert een verbinding in de broodkruimel. Het standaardgedrag is het "goto"gedrag. Als de verbinding zich verschillend gedraagt, gebruik de <span class="codeph"><span class="varname"> facultatieve attributen van de </span> gsname </span> om "te specificeren verwijder"of "daling". Om het even welk attribuut inbegrepen in de markering wordt overgegaan door tot de resulterende ankermarkering. </p> <p> <code class="syntax html"> &lt;guided-breadcrumb&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-link&nbsp;gsname="remove"&nbsp;class="bc_link"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-value/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-breadcrumb-link&gt; 
      &lt;/guided-breadcrumb&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to search-eng version, 2/1/2013--> <span class="codeph"> &lt;geleide-breadcrumb-waarde /&gt; </span> </p> </td> 
   <td colname="col2"> <p>De waardemarkering drukt uit de getransformeerde waarde van de huidige broodkruimeliteratie. Het wordt alleen gebruikt in de context van een <span class="codeph"> geleide-broodkruimelblok </span> . </p> <p> <code class="syntax html"> &lt;guided-breadcrumb&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-value/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-breadcrumb-link&gt; 
      &lt;/guided-breadcrumb&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to search-eng version, 2/1/2013--> <span class="codeph"> &lt;label met rondkorrelige geleiding /&gt; </span> </p> </td> 
   <td colname="col2"> <p>De etiketmarkeringoutput een etiket voor een broodkruimelwaarde detailleert die facet werd geselecteerd om dat broodkruimelpunt te produceren. Het wordt slechts gebruikt in de context van een <span class="codeph"> geleide-broodkruimelblok </span> . </p> <p> <code class="syntax html"> &lt;guided-breadcrumb&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-label/&gt;:&nbsp;&lt;guided-breadcrumb-value/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-breadcrumb-link&gt; 
      &lt;/guided-breadcrumb&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to search-eng version, 2/1/2013--> <code> &lt;guided-if-breadcrumb-label&gt; 
      &lt;guided-else- 
      breadcrumb-label&gt; 
      &lt;guided-if-breadcrumb-label /&gt; </code> </p> </td> 
   <td colname="col2"> <p>Deze voorwaardelijke markering wordt gebruikt om inhoud voorwaardelijk te tonen als de huidige broodkruimelwaarde een etiket heeft. Het wordt gebruikt om etiketten en verwante inhoud slechts te tonen wanneer een etiket daadwerkelijk bestaat. Het wordt slechts gebruikt in de context van een <span class="codeph"> geleide-broodkruimelblok </span> . </p> <p> <code class="syntax html"> &lt;guided-breadcrumb&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-breadcrumb-label&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-label/&gt;: 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-breadcrumb-label&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-value/&gt;&lt;/guided-breadcrumb-link&gt; 
      &lt;/guided-breadcrumb&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-breadcrumb-path [gsname="goto|remove|drop"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Gebruikt om uw eigen broodkruimelverbinding te bouwen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Menus {#section_1D489ADF041F4351A66E5D5742125CA8}

Zie [over menu&#39;s](../c-about-design-menu/c-about-menus.md#concept_68123CE5CF4447B59217B5D721424E32).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu gsname="menuname"&gt;&lt;/guided-menu&gt; </span> </p> </td> 
   <td colname="col2"> <p>Dit is de iteratormarkering van de de lusjelijn van de menuwaarde. Gebruik de <span class="codeph"> gsname- </span> attributen om te identificeren welke reeks menupunten wordt getoond. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu-item-link [attr="value"]+&gt;&lt;/guided-menu-item-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Geeft u URL voor het raffineren van de huidige onderzoek naar het menupunt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu-item-optie [attr="value"]+/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Typisch wordt een menu getoond in een uitgezochte controle op een malplaatje. Deze markering maakt het construeren van de uitgezochte controle gemakkelijker omdat het HTML voor het produceren van de optie voor de uitgezochte controle produceert. </p> <p>Bijvoorbeeld, het volgende codeblok: </p> <p> <code class="syntax html"> &lt;select&nbsp;name="sort"&nbsp;onchange="gcGo(this);"&gt; 
      &lt;guided-menu&nbsp;gsname="sort"&gt; 
      &lt;guided-menu-item-option/&gt; 
      &lt;/guided-menu&gt; 
      &lt;/select&gt; </code> </p> <p>Kan HTML als het volgende produceren: </p> <p> <code class="syntax html"> &lt;select&nbsp;name="sort"&nbsp;onchange="gcGo(this);"&gt; 
      &nbsp;&nbsp;&lt;option&nbsp;value="?sort=relevance;sp_sfvl_field=product-type|category|size;"&nbsp;selected="selected"&gt;Sort&nbsp;by&nbsp;Relevance&lt;/option&gt; 
      &nbsp;&nbsp;&lt;option&nbsp;value="?sort=avail-code;sp_sfvl_field=product-type|category|size;"&gt;Sort&nbsp;by&nbsp;Availability&lt;/option&gt; 
      &nbsp;&nbsp;&lt;option&nbsp;value="?sort=price;sp_sfvl_field=product-type|category|size;"&gt;Sort&nbsp;by&nbsp;Price&lt;/option&gt; 
      &lt;/select&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu-item-waarde /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Keert het koord van de waarde terug die met het menu wordt geassocieerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu-item-label /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Keert het koord van het etiket terug dat met het menu wordt geassocieerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;geleid-menu-item-pad /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Keert het wegkoord terug. Gebruik de markering als u een parameter aan de weg wilt toevoegen en een douaneverbinding tot stand brengen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if-menu-item-selected&gt; 
      &lt;guided-else-menu- 
      item-selected&gt; 
      &lt;/guided-if-menu-item-selected&gt; </code> </p> </td> 
   <td colname="col2"> <p>Keert 1 terug of 0 erop wijst die als het huidige menupunt wordt geselecteerd. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Pagenav {#section_2EE397635C514BBC8D668278EA314F35}

De markeringen van de paginavigatie kunnen worden gebruikt om een reeks verbindingen te bouwen die een gebruiker toestaan om door de onderzoeksresultaten te pagineren.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;leid-pagina's&gt;&lt;/geleide pagina's&gt; </span> </p> </td> 
   <td colname="col2"> <p>De lijnmarkering voor de paginavigatie. Om het even welke inhoud tussen de het openen en sluitende markeringen wordt herhaald voor elke pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;geleid-pagina-verbinding [attr="waarde"]+&gt;&lt;/geleide-pagina-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Creeert een verbinding in de paginavigatie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided page-link gsname="first|prev|next|last|viewall|viewpage" [attr="value"]+&gt;&lt;/guided-page-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Creeert een verbinding aan de eerste, vorige, volgende, of laatste pagina. Het kan een verbinding ook tot stand brengen om alle pagina's op één pagina te bekijken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;nummer van de geleide pagina /&gt; </span> </p> </td> 
   <td colname="col2"> <p> Keert een koord met het huidige paginaaantal terug. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if-page-selected&gt; 
      &lt;guided-else-page- 
      selected&gt; 
      &lt;/guided-if-page-selected&gt; </code> </p> </td> 
   <td colname="col2"> <p>Deze reeks voorwaardelijke markeringen is waar als de pagina die momenteel wordt herhaald over wordt geselecteerd. Het wordt typisch gebruikt om het paginaaantal in de pagina-navigatie controle verschillend te tonen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-page-prev&gt; 
      &lt;guided-else-page- 
      prev&gt; 
      &lt;/guided-if[-not]-page-prev&gt; </code> </p> </td> 
   <td colname="col2"> <p> Deze reeks voorwaardelijke markeringen is waar als de huidige pagina een vorige pagina heeft. Het wordt typisch gebruikt om een vorige verbinding in de paginavigatie te tonen, wanneer het steek houdt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-page-next&gt; 
      &lt;guided-else-page- 
      next&gt; 
      &lt;/guided-if[-not]-page-next&gt; </code> </p> </td> 
   <td colname="col2"> <p> Deze reeks voorwaardelijke markeringen is waar als de huidige pagina een volgende pagina heeft. Het wordt typisch gebruikt om een vorige verbinding in de paginavigatie te tonen, wanneer het steek houdt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-page-viewall&gt; 
      &lt;guided-else-page- 
      viewall&gt; 
      &lt;/guided-if[-not]-page-viewall&gt; </code> </p> </td> 
   <td colname="col2"> <p> Wanneer een onderzoek een grote resultaatreeks terugkeert zou u niet de capaciteit kunnen willen aanbieden om alle resultaten te bekijken. Daarom kunt u deze reeks voorwaardelijke markeringen gebruiken om te bepalen wanneer om de Mening te tonen Al verbinding. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-page-viewpages&gt; 
      &lt;guided-else-page- 
      viewpages&gt; 
      &lt;/guided-if[-not]-page-viewpages&gt; </code> </p> </td> 
   <td colname="col2"> <p>U kunt deze reeks voorwaardelijke markeringen gebruiken om te bepalen wanneer om de verbinding van de Pagina's van de Mening te tonen. Het wordt typisch gebruikt om een klant toe te staan om bepaalde pagina's te bekijken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> 

    &amp;lt;geleid-anders-pagina-pagina-verbinding&amp;gt;
    &amp;lt;/geleid-als[-niet]-pagina-verbinding&amp;gt; &lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>Tests als de paginavigatie een eerste pagina, vorige pagina, volgende pagina, etc. heeft. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;aantal pagina's met begeleiding /&gt; </span> </p> </td> 
   <td colname="col2"> <p> Keert een koord met het totale aantal pagina's van onderzoeksresultaten terug. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-pagination gsname= 
      "pagination_name"&gt;&lt;/guided-pagination&gt; </code> </p> </td> 
   <td colname="col2"> <p>Gebruik de <span class="codeph"> geleide-paginering </span> markering om een gebied te bepalen waarin alle pagineringsmarkeringen op een specifieke paginering betrekking hebben die plaatst voor het geval dat u weinig bepaalde Montages van de Navigatie van de Pagina hebt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> 

    volgende|last|viewall|viewpage]/&amp;gt; &lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>Creeert uw eigen verbinding in de paginavigatie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-page-high-eq-last&gt; 
      &lt;guided-else-page- 
      high-eq-last&gt; 
      &lt;/guided-if-page-high-eq-last&gt; </code> </p> </td> 
   <td colname="col2"> <p>Tests als de hoogste pagina in de paginavigatie aan het totale aantal pagina's gelijk is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-page-low-eq-first&gt; 
      &lt;guided-else-page-low-eq-first&gt; &lt;/guided-if-page-low-eq-first&gt; </code> </p> </td> 
   <td colname="col2"> <p>Tests als de laagste pagina in de paginavigatie aan gelijk is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;geleid-als-pagina-is-meerpagina&gt; &lt;geleid-anders-pagina-is-multipage&gt; &lt;/geleid-als-pagina-is-is-meerpagina&gt; </span> </p> </td> 
   <td colname="col2"> <p>Tests als er één enkele pagina van resultaten of veelvoudige pagina's van resultaten is. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Recente zoekopdrachten {#section_8CD907521F584257B475595B01A5964B}

U kunt recente onderzoeksmarkeringen gebruiken om een reeks verbindingen te bouwen die een gebruiker laat snel een vorig onderzoek, zoals in het volgende voorbeeld in werking stellen:

```
<guided-if-recent-searches> 
    <span>Recent Searches</span><br/> 
    <guided-recent-searches> 
        <guided-recent-searches-link><guided-recent-searches-value></guided-recent-searches-link><br/> 
    </guided-recent-searches> 
    <guided-recent-searches-clear-link>Clear Recent Searches</guided-recent-searches-clear-link> 
</guided-if-recent-searches>
```

Zie recente zoekopdrachten [configureren](../c-about-design-menu/t-configuring-recent-searches.md#task_E9E8ACA04C90484F8AFD5262167B2562).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;geleid-recent-onderzoeken&gt;&lt;/geleid-recent-onderzoeken&gt; </span> </p> </td> 
   <td colname="col2"> <p>De lijnmarkering voor recente onderzoeken. Om het even welke inhoud tussen de het openen en sluitende markeringen wordt herhaald voor elke pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-recent-searches-link [attr="value"]+&gt; 
      &lt;/guided-recent-searches-link&gt; </code> </p> </td> 
   <td colname="col2"> <p>Laat u een verbinding aan een recent onderzoek bouwen. Het steunt het overgaan van om het even welke attributen van HTML rechtstreeks tot de ankermarkering. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;geleid-recent-onderzoeken-weg/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Laat u de relatieve weg URL voor een recent onderzoek, binnen een <span class="codeph"> geleid-recent-onderzoek </span> lijn grijpen. Typisch zou u leiden-recent-onderzoek-verbinding gebruiken <span class="codeph"> </span>. Nochtans, als u uw eigen verbinding wilde bouwen kon u deze markering gebruiken. Het volgende is een voorbeeld: </p> <p> <code class="syntax html"> &lt;guided-lt/&gt;a&amp;nbsp;href="&lt;guided_recent_searches_path&gt;"&gt;&lt;guided-recent-searches-value&gt;&lt;/a&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;geleid-recent-onderzoeken-waarde&gt; </span> </p> </td> 
   <td colname="col2"> <p>Laat u de vraagtermijn grijpen die met een recent onderzoek wordt geassocieerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;geleid-recent-onderzoeken-duidelijk-verbinding [attr="waarde"]+&gt;&lt;/geleid-recent-onderzoeken-duidelijk-verbinding&gt; </span> </p> </td> 
   <td colname="col2"> <p>Laat u uw klanten de capaciteit aanbieden om onlangs bewaarde onderzoeken te ontruimen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;geleid-recent-onderzoeken-duidelijk-weg/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Keert de weg terug die <span class="codeph"> </span> &lt;geleid-recent-onderzoeken-duidelijk-verbinding&gt; gebruikt zodat u uw eigen verbinding kunt bouwen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 

    &amp;lt;/geleid-als-recent-onderzoeken&amp;gt; &lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>Laat u de recente onderzoeken tonen wanneer een klant een recente onderzoek heeft uitgevoerd. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Bedoelde je {#section_C1EB3B9D8E1242798A6E04609D1E3543}

U kunt gebruiken bedoelde markeringen om een reeks verbindingen aan suggesties te bouwen wanneer een onderzoek geen resultaten terugkeert en de termijn van het Onderzoek niet in het woordenboek van de rekening is. Het volgende is een voorbeeld van het gebruiken van Bedoelde markeringen:

```
<guided-if-suggestions> 
    <span>Did You Mean?</span><br/> 
    <guided-suggestions> 
        <guided-suggestion-link><guided-suggestion/></guided-suggestion-link><br/> 
    </guided-suggestions> 
</guided-if-suggestions>
```

Zie [over wat je bedoelt](../c-about-linguistics-menu/c-about-did-you-mean.md#concept_7D4F3C29EF184B538B8AE2ECAE0CDC5E).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matches search-eng version, 2/1/2013--> <span class="codeph"> &lt;geleid suggesties&gt;&lt;/geleide-suggesties&gt; </span> </p> </td> 
   <td colname="col2"> <p>Dit is de lijnmarkering voor het van een lus voorzien over de suggesties. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matches search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-suggestie-link [attr="value"]+&gt;&lt;/guided-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Maakt een link naar de gegeven suggestie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Newly added from search-eng version, 2/1/2013--> <span class="codeph"> &lt;geleide suggestiewaarde /&gt; </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-suggestions&gt;&lt;guided-else[-not]- 
      suggestions&gt;&lt;/guided-if[-not]-suggestions&gt; </code> </p> </td> 
   <td colname="col2"> <p>Laat u testen als er om het even welke suggesties zijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;geleid suggestiepad/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Keert het wegkoord op de suggestie terug. U kunt het gebruiken om uw eigen ankermarkering te bouwen. Typisch, <span class="codeph"> geleid-suggestie-verbinding </span> wordt in plaats daarvan gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided suggestie/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Een suggestie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;geleid suggestie-resultaat-telling/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Resultaat telt mee voor de suggestie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-suggestion-autosearch&gt; 
      &lt;guided-else[-not]-suggestion-autosearch&gt; 
      &lt;/guided-if[-not]-suggestion-autosearch&gt; </code> </p> </td> 
   <td colname="col2"> <p>Laat u testen als autosearch door suggestie op nul resultaten werd uitgevoerd, voor het geval dat deze eigenschap is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;geleid-suggestie-origineel-query/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Keert de originele vraag terug als autosearch werd uitgevoerd. </p> <p>Voorbeeld van het gebruik: </p> <p> <code class="syntax html"> &lt;guided-if-suggestion-autosearch&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;Search&nbsp;for&nbsp;&lt;guided-query-param&nbsp;gsname="q"&nbsp;/&gt;&nbsp;instead&nbsp;of&nbsp;&lt;guided-suggestion-original-query&nbsp;/&gt; 
      &lt;/guided-if-suggestion-autosearch&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-suggestion-low-results&gt; 
      &lt;guided-else[-not]-suggestion-low-results&gt; 
      &lt;/guided-if[-not]-suggestion-low-results&gt; </code> </p> </td> 
   <td colname="col2"> <p>Deze voorwaarde is waar als er suggesties toe te schrijven aan een lage resultaattelling zijn, voor het geval dat deze eigenschap is. </p> <p>Het volgende is een voorbeeld om deze markering te gebruiken: </p> <p> <code class="syntax html"> &lt;guided-if-suggestion-low-results&gt; 
      &nbsp;&nbsp;&nbsp;You&nbsp;have&nbsp;a&nbsp;low&nbsp;result&nbsp;count&nbsp;for&nbsp;&lt;guided-query-param&nbsp;gsname="q"&nbsp;/&gt;. 
      &nbsp;&nbsp;&nbsp;Did&nbsp;you&nbsp;mean:&nbsp;&lt;guided-suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-suggestion-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-suggestion&nbsp;/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-suggestion-link&gt;&lt;guided-if-not-last&gt;,&nbsp;&lt;/guided-if-not-last&gt; 
      &nbsp;&nbsp;&nbsp;&lt;/guided-suggestions&gt; 
      &lt;/guided-if-suggestion-low-results&gt; </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Automatisch aanvullen {#section_897316BEE1454E839A56B565CA4AF018}

De volgende markeringen kunnen worden gebruikt om autocompleteren aan uw onderzoeksvorm toe te voegen. De hoofd-inhoud en vorm-inhoud markeringen worden vereist om autocomplete functie correct te maken. Het wordt geadviseerd u de markeringen in tegenstelling tot hard het coderen van autocomplete Javascript en CSS in uw presentatiemalplaatje gebruikt. De reden is omdat de markeringen uw malplaatjes toelaten om het even welke nieuwe nederlaag geheime voorgeheugen IDs op te nemen wanneer u uw autocomplete montages zonder de behoefte verandert om uw malplaatje manueel bij te werken.

Zie [over auto-Voltooid](../c-about-auto-complete.md#concept_093A9CD754864BA79B456FE4BEB64578).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;geleid-als-autocomplete&gt; &lt;geleid-anders-autocomplete&gt; &lt;/geleid-als-autocomplete&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ontdekt als de autocomplete eigenschap wordt toegelaten. U kon de markeringen gebruiken om naar keuze de hoofd en vorminhoud op te nemen die voor autocompleteren worden vereist. Omgekeerd, laat dit u de eigenschap aan en uit van een knevel voorzien en niet uw presentatiemalplaatjes moeten veranderen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;geleid-ac-css/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Gebruikt in het hoofd van het presentatiemalplaatje en vervangen door het aangewezen CSS manuscript omvat voor autocomplete. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;inhoud van de geleide-ac-vorm/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Gebruikt in de onderzoeksvorm (tussen de <span class="codeph"> &lt;form&gt; </span> en <span class="codeph"> &lt;/form&gt; </span> markeringen) van de presentatiemalplaatje in plaats van de harde codering van de autocomplete markeringen binnen het formulier. De markeringen worden vervangen met aangewezen HTML dat wordt vereist om het autocomplete werk te maken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;geleid-ac-javascript/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Produceert de verbindingen aan Autocomplete JavaScript. Voor beste prestaties is het raadzaam deze tag onder aan de pagina te plaatsen voordat de tag 'body' wordt gesloten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Winkel {#section_A33E25DB5E67404A823BD9618665B773}

Gebruik de volgende markeringen om de opslag te testen en te tonen die een gebruiker momenteel in is.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;geleide-store/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Output de huidige opslag. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;geleid-als-store-defined&gt; &lt;geleid-else-store-defined&gt; &lt;/geleid-if-store-defined&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ontdekt als de gebruiker in een opslag is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;geleid-als-opslag gsname="store"&gt; &lt;mede-else-store&gt; &lt;/guided-if-store&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ontdekt als de gebruiker in de opslag is die de <span class="codeph"> gsname </span> parameter specificeert. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Zones {#section_B9B3179E000C42D492E1541F2FE44CB5}

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided zone gsname="zone area" [search="associated search"] [facet="associated facet"] [width="xx" height="yy"]&gt; </span> </p> </td> 
   <td colname="col2"> <p>U kunt om het even welke inhoud in streekmarkeringen verpakken om een streek uit dat gebied tot stand te brengen. Dit laat u bedrijfsregels gebruiken om de streek te tonen zoals nodig. Door gebrek, worden de streken altijd getoond. U kunt de facultatieve onderzoek en facetparameters gebruiken om te wijzen op welk onderzoek of facet met de streek wordt geassocieerd. Dergelijke functionaliteit laat de softwareskip onderzoeken of facetten wanneer een streek verborgen is, verbeterend onderzoek-tijd prestaties. De hoogte en breedteattributen zijn facultatief en worden gebruikt om te vormen hoe placeholder in de Visuele Bouwer van de Regel wordt getoond wanneer een streek wordt verwijderd. </p> <p> Gebruik de <span class="codeph"> geleide-als-facet [-niet]-zichtbare </span> markering in plaats van de streek waar mogelijk. Het vereenvoudigt het presentatiemalplaatje. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-zone gsname="zone"&gt; &lt;guided-else-zone&gt; &lt;/guided-if-zone&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze reeks markeringen laat het testen toe als een streek momenteel wordt getoond. Het is nuttig wanneer u inhoud elders op de pagina hebt die u slechts wilt tonen wanneer de streek wordt getoond. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Loop-indicatoren {#section_387322CA0AA843A2ACF2795C328673E9}

U kunt elk van de volgende lijnindicatoren in om het even welk van deze lijnblokken gebruiken:

* begeleide resultaten
* geleide-facetwaarden
* begeleide broodkruimel
* menu-items
* begeleide pagina&#39;s

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-first&gt;&lt;guided-else[-not]-first&gt; 
      &lt;/guided-if[-not]-first&gt; </code> </p> </td> 
   <td colname="col2"> <p>Deze voorwaarde is waar wanneer de huidige herhaling de eerste herhaling van de lijn is. Dat betekent niet noodzakelijk het eerste resultaat of de eerste pagina, maar de eerste getoond. Als de bezoeker van de plaats op pagina 2 van een resultaatreeks is die 10 per pagina is, is de eerste herhaling resultaat 11. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-last&gt;&lt;guided-else[-not]-last&gt; 
      &lt;/guided-if[-not]-last&gt; </code> </p> </td> 
   <td colname="col2"> <p>Deze voorwaarde is waar wanneer de huidige herhaling de laatste herhaling van de lijn is. Dat betekent niet noodzakelijk het laatste resultaat of de laatste pagina, maar laatste getoond in de huidige context (pagina). Als de bezoeker van de plaats op pagina 1 van een resultaatreeks is die 200 resultaten maar slechts 10 resultaten per pagina bevat, is de laatste herhaling resultaat 10 in plaats van resultaat 200. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-odd&gt;&lt;guided-else[-not]-odd&gt; 
      &lt;/guided-if[-not]-odd&gt; </code> </p> </td> 
   <td colname="col2"> <p>Deze voorwaarde is waar wanneer de huidige herhaling een oneven herhaling van de lijn (tegenover een gelijke herhaling) is. Dit is nuttig voor het tonen van variërende rijkleuren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-even&gt;&lt;guided-else[-not]-even&gt; 
      &lt;/guided-if[-not]-even&gt; </code> </p> </td> 
   <td colname="col2"> <p>Deze voorwaarde is waar wanneer de huidige herhaling een gelijke herhaling van de lijn (tegenover een oneven herhaling) is. Dit is nuttig voor het tonen van variërende rijkleuren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-alt&gt;&lt;guided-else[-not]-alt&gt; 
      &lt;/guided-if[-not]-alt&gt; </code> </p> </td> 
   <td colname="col2"> <p>Deze voorwaarde is waar wanneer de huidige herhaling een gelijke herhaling van de lijn is. Dit is nuttig voor het tonen van variërende rijkleuren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-inner&gt;&lt;guided-else[-not]-inner&gt; 
      &lt;/guided-if[-not]-inner&gt; </code> </p> </td> 
   <td colname="col2"> <p>Omvat de tekst tussen hen als de huidige herhaling noch de eerste noch de laatste is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-outer&gt;&lt;guided-else[-not]-outer&gt; 
      &lt;/guided-if[-not]-outer&gt; </code> </p> </td> 
   <td colname="col2"> <p>Omvat de tekst tussen hen als de huidige herhaling de eerste of laatste is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-loop-index&gt; </span> </p> </td> 
   <td colname="col2"> <p>Een geheel (beginnend van 0) de waarvan waardetoename voor elke herhaling van de lijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-loop-teller&gt; </span> </p> </td> 
   <td colname="col2"> <p>Een geheel (beginnend van 1) de waarvan waardetoename voor elke herhaling van de lijn. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Diverse talen {#section_BFE8DC98E26F4D7BB60FEC54D9A5DC6C}

De volgende markeringen zijn beschikbaar om u te laten geavanceerdere dingen met uw malplaatje doen, zoals het bouwen van uw eigen mini-facet.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng, 2/1/2013--> <span class="codeph"> &lt;geleid-huidig-weg [escape="html|url|js|json|0"] /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Geeft u de huidige weg die wordt gebruikt. Typisch wordt het gebruikt om een verbinding tot stand te brengen die op een nieuwe parameter aan het bestaande onderzoek toevoegt. Door gebrek is de weg ontsnapte URL. U kunt specificeren welke wijze van het ontsnappen u als vluchtparameter wilt gebruiken. </p> <p>Voorbeeld: </p> <p> <code class="syntax html"> &lt;a&nbsp;href="&lt;guided-current-path&nbsp;/&gt;&amp;lang=fr"&gt; 
      French&nbsp;Version </code> </p> <p>In dit voorbeeld, gebruikt een regel van de onderzoeksverwerking lang om de Franse versie te selecteren. </p> <p>De huidige weg heeft altijd minstens één vraagparameter. Als geen andere vraagparameters bestaan wordt het geplaatst aan <span class="codeph"> q=* </span> makend het gemakkelijker om meer parameters toe te voegen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> Basispad </span> </p> </td> 
   <td colname="col2"> <p> Als u een verbinding wilt tot stand brengen gebruikend basepath, gebruik <span class="codeph"> / </span> bij het begin van uw <span class="codeph"> href </span> en voeg op parameters toe. </p> <p> <code class="syntax html"> &lt;a&nbsp;href="/"&gt;All&nbsp;Products&lt;/a&gt; 
      Would&nbsp;create&nbsp;a&nbsp;link&nbsp;"All&nbsp;Products"&nbsp;to&nbsp;your 
      basepath,&nbsp;for&nbsp;example&nbsp;https://search.mycompany.com/ 
       </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng, 2/1/2013--> <span class="codeph"> &lt;guided-query-param gsname="query_parameter" [escape="html|url"] /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Laat u de bestaande waarde van een vraagparameter grijpen die op URL is. Als uw parameter niet bestaat, keert deze markering een leeg koord terug. Als u geen vluchtoptie specificeert is het teruggekeerde koord automatisch ontsnapte aan HTML, kunt u of HTML of URL specificeren ontsnapend. </p> <p>Voorbeeld: </p> <p> 

    &amp;lt;geleide-query-param&amp;nbsp;gbsp;sap=&quot;q&quot;&amp;nbsp;nbsp;gt;gt;
    geeft&amp;nbsp;u&amp;nbsp;waarde&amp;nbsp;pants
    
    &amp;lt;geleide-query-param&amp;nbsp;gbsp;gpsp;gp=&quot;gps lang&quot;&amp;nbsp;/&amp;gt;
    geeft&amp;nbsp;u&amp;nbsp;nbsp;waarde&amp;nbsp;nbsp;waarde&amp;nbsp;nbsp;nbsp;nbsp;
    
    geeft&amp;
    nbsp;nbsp;nbsp;nbsp;/&amp;gt;u&amp;nbsp;an&amp;nbsp;leeg&amp;nbsp;string
    &amp;nbsp;
    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp; &lt;/code> &lt;/p> &lt;/td>
</tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-query-param-name gsname="param#" offset="offset_number"/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Het geleide Onderzoek heeft het begrip van een vraagaantal, dat in de broodkruimelcontrole wordt gebruikt. <span class="codeph"> geleid-vraag-param-naam </span> laat u parameters als deel van een verbinding in het presentatiemalplaatje bepalen waar de Geleide cijfers van het Onderzoek het correcte vraagaantal voor u uit. De <span class="codeph"> gsname </span> heeft een "x"in het, die Geleide Onderzoek met het correcte aantal vervangt. De compensatiewaarde kan 0 - 15 zijn, waar 0 erop wijst dat het volgende beschikbare vraagaantal wordt gebruikt. A1 wijst erop dat u 1 aan het wilt toevoegen, etc. </p> <p>In combinatie met <span class="codeph"> geleide-huidig-weg </span>, kunt u uw eigen mini facetverbinding bouwen of een extra boor-benedenniveau toestaan. </p> <p>Voorbeeld: </p> <p> <code class="syntax html"> &lt;a&nbsp;href="&lt;guided-current-path 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;&amp;&lt;guided-query-param-name&nbsp;gsname="q#"&nbsp;offset="0" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=mens&amp;&lt;guided-query-param-name&nbsp;gsname="x#"&nbsp;offset="0" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=category"&nbsp;&gt;Category:Men&lt;/a&gt;&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </code> </p> <p> <code class="syntax html"> &lt;a&nbsp;href="&lt;guided-current-path 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;&amp;&lt;guided-query-param-name&nbsp;gsname="sp_q_exact_#"&nbsp;offset="0" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=mens&amp;&lt;guided-query-param-name&nbsp;gsname="sp_x_#"&nbsp;offset="0" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=category&amp;&lt;guided-query-param-name&nbsp;gsname="sp_q_exact_#"&nbsp;offset="1" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=Jeans&amp;&lt;guided-query-param-name&nbsp;gsname="sp_x_#"&nbsp;offset="1" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=product-type"&nbsp;&gt;Cat:Men&nbsp;-&nbsp;Product:Jeans&lt;/a&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;geleid-omvat gsfile="filename" /&gt; </span> </p> </td> 
   <td colname="col2"> <p> Laat u andere malplaatjedossiers omvatten. Deze functionaliteit betekent dat u veelvoudige malplaatjes kunt tot stand brengen gebruikend submalplaatjes als modules. </p> <p>In het volgende voorbeeld, zijn de <span class="filepath"> broodkruimels </span> en de <span class="filepath"> facetten </span> - dossiers inbegrepen: </p> <p> <code class="syntax html"> &lt;guided-include&nbsp;gsfile='breadcrumbs.tmpl'&nbsp;/&gt; 
      &lt;guided-include&nbsp;gsfile='facets.tmpl'&nbsp;/&gt; </code> </p> <p>Dynamisch omvat niet wordt gesteund. Met andere woorden, <span class="codeph"> kan gsfile </span> geen variabele zijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW 1/17/2013--> <span class="codeph"> &lt;tijd voor begeleide zoekopdrachten&gt; </span> </p> </td> 
   <td colname="col2"> <p> Geeft aan hoe lang de zoekopdracht duurde. De teruggekeerde waarde van de onderzoekstijd wordt gespecificeerd in ms. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW 1/17/2013--> <span class="codeph"> &lt;geleid-val-door-onderzoeken&gt; </span> </p> </td> 
   <td colname="col2"> <p> Keert de telling van kernen onderzoeken terug die worden gebruikt om de pagina van onderzoeksresultaten te bouwen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW 1/17/2013--> <span class="codeph"> &lt;geleid-als-val-door-onderzoek&gt;&lt;/geleide-als-door-val-door-onderzoek&gt; </span> </p> </td> 
   <td colname="col2"> <p>Tests als de telling van kernonderzoeken groter is dan één. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-even&gt;&lt;guided-else[-not]-even&gt; 
      &lt;/guided-if[-not]-even&gt; </code> </p> </td> 
   <td colname="col2"> <p>Deze voorwaarde is waar wanneer de huidige herhaling een gelijke herhaling van de lijn (tegenover een oneven herhaling) is. Dit is nuttig voor het tonen van variërende rijkleuren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-alt&gt;&lt;guided-else[-not]-alt&gt; 
      &lt;/guided-if[-not]-alt&gt; </code> </p> </td> 
   <td colname="col2"> <p>Deze voorwaarde is waar wanneer de huidige herhaling een gelijke herhaling van de lijn is. Dit is nuttig voor het tonen van variërende rijkleuren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-inner&gt;&lt;guided-else[-not]-inner&gt; 
      &lt;/guided-if[-not]-inner&gt; </code> </p> </td> 
   <td colname="col2"> <p>Omvat de tekst tussen hen als de huidige herhaling noch de eerste noch de laatste is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-outer&gt;&lt;guided-else[-not]-outer&gt; 
      &lt;/guided-if[-not]-outer&gt; </code> </p> </td> 
   <td colname="col2"> <p>Omvat de tekst tussen hen als de huidige herhaling de eerste of laatste is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-first-search&gt;&lt;guided-else-first-search&gt; 
      &lt;/guided-if-first-search&gt; </code> </p> </td> 
   <td colname="col2"> <p>Laat u controleren of u op het aanvankelijke onderzoek of niet bent (de vraag was het resultaat van een onderzoek van de onderzoeksdoos). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;geleid zoeken-url/&gt; </span> </p> </td> 
   <td colname="col2"> <p>U kunt deze markering in uw malplaatje gebruiken om u te bewaren van het hardcoderen van de actie van de onderzoeksvorm. Het ontdekt wanneer u in het Staged of Levende milieu bent en verandert dienovereenkomstig. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;geleid-als-vraag-param-bepaalde gsname="query_parameter"&gt; &lt;geleid-anders-vraag-param-defined&gt; &lt;/geleid-als-vraag-param-bepaald&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze reeks markeringen laat u testen welke parameters van CGI in de onderzoeksweg worden bepaald. U kunt de waarden van de parameters testen slechts als zij worden bepaald. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-next-query-number [gsname="offset"] /&gt; </span> </p> </td> 
   <td colname="col2"> <p>De geleide motor van het Onderzoek die het malplaatje drijft heeft het begrip van het drijven vraagaantallen waar elke nieuwe verbinding die de motor produceert, het volgende beschikbare vraagaantal gebruikt. Deze markering laat u het volgende vraagaantal of de compensatie grijpen zodat u douaneverbindingen kunt bouwen die in de resultaatreeks boren. De compensatie laat u in het volgende vraagaantal compenseren. Bijvoorbeeld, als u één facet hebt geselecteerd, is het volgende vraagaantal 2, met een compensatie van 1 het teruggekeerde vraagaantal is 3. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;geleid-douane-var gsname="custom_variable" [escape="html|url|js|json|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Laat u de bestaande waarde van een douanevariabele grijpen die uw verwerkingsregels bepalen. Als u geen vluchtoptie specificeert is het teruggekeerde koord automatisch ontsnapte HTML, kunt u of <span class="codeph"> html </span>, <span class="codeph"> url </span>, <span class="codeph"> js </span>, of <span class="codeph"> 0 specificeren </span>. Als u een verwerkingsregel gebruikt om een inkomende parameter van CGI aan een douanevariabele te kopiëren en dan die variabele in uw malplaatje met het ontsnappen te tonen of te gebruiken die aan niets of Js wordt geplaatst, dan kunt u een kwetsbaarheid XSS in uw onderzoek tot stand brengen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;geleid-als-douane-var-defined gsname="custom_variable"&gt; &lt;geleid-anders-douane-var-defined&gt; &lt;/geleid-als-douane-var-defined&gt; </span> </p> </td> 
   <td colname="col2"> <p>Laat het testen toe als een douanevariabele in de verwerkingsregels (vraag het schoonmaken, pre-onderzoeksverwerking en post-onderzoeksverwerking) wordt bepaald. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>19 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-general-field gsname="zoekname" field="fieldname" [escape="html|url|js|json|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Laat u de inhoud van een algemeen gebied tonen dat in het vervoermalplaatje wordt bepaald. Als u geen vluchtoptie specificeert wordt het teruggekeerde koord gecodeerd in het formaat u in het vervoermalplaatje voor dat gebied hebt gespecificeerd. Het specificeren van een vluchtoptie is bovenop van toepassing welk formaat u het gebied zoals in uw vervoermalplaatje codeert. U kunt of <span class="codeph"> html </span>, <span class="codeph"> url </span>, <span class="codeph"> js </span>, <span class="codeph"> json </span>, of <span class="codeph"> 0 specificeren </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>20 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-general-field gsname="search-name" field="fieldname"&gt; &lt;guided-else-general-field&gt; &lt;/guided-if-general-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>Laat het testen toe als de inhoud van een algemeen gebied, zoals die in het vervoermalplaatje wordt bepaald, bestaat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>21 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-cookie-value gsname="cookie_name" [escape="html|url|js|json|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Laat u de waarde van een koekje grijpen, veronderstellend dat het koekje beschikbaar is. Als u geen ontsnappingsoptie specificeert is het teruggekeerde koord automatisch ontsnapte HTML, kunt u of <span class="codeph"> html </span>, <span class="codeph"> url </span>, <span class="codeph"> js </span>, <span class="codeph"> json </span>, of <span class="codeph"> 0 specificeren </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>22 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-cookie gsname="cookie_name"&gt; &lt;guided-else-cookie&gt; &lt;/guided-if-cookie&gt; </span> </p> </td> 
   <td colname="col2"> <p>Laat het testen toe als een koekje bestaat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>23 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;geleid banner gsname="banner area" [escape="html|url|js|json|0"] [width="xx" height="yy"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Output de banner voor een bepaald gebied. De facultatieve breedte en hoogteattributen worden gebruikt in de Visuele Bouwer van de Regel om de vertoning van een zinvolle plaats-houder toe te laten om gebruikers te laten een banner selecteren. Door gebrek zijn de banners niet ontsnapt. In plaats daarvan, wilt u HTML in het presentatiemalplaatje injecteren. Nochtans, als u een malplaatje JSON bouwt denk na gebruikend Js het ontsnappen optie. </p> <p>Voorbeeld: </p> <p> <code class="syntax html"> &lt;guided-banner&nbsp;gsname="top"&nbsp;width="400px" 
      &nbsp;height="50px"/&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>24 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-banner-set gsname="banner area"&gt; &lt;aantal geleide-else-banner-set&gt; &lt;/guided-if-banner-set&gt; </span> </p> </td> 
   <td colname="col2"> <p>Laat het testen toe als een bannergebied wordt geplaatst. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>25 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-simulator-modus&gt; &lt;guided-else-simulator-modus&gt; &lt;/guided-if-simulator-modus&gt; </span> </p> </td> 
   <td colname="col2"> <p>Laat u ontdekken wanneer u uw onderzoek in Simulator of de Visuele Bouwer van de Regel bekijkt. Het wordt normaal gebruikt om extra te tonen zuivert informatie voor u. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>26 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;geleid-als-tnt-zaken-regels&gt; &lt;geleid-anders-tnt-zaken-regels&gt; &lt;/geleid-als-tnt-zaken-regels&gt; </span> </p> </td> 
   <td colname="col2"> <p>Laat u ontdekken als u om het even welke bedrijfsregels hebt die van verwijzingen voorzien een campagne van het Doel van <span class="keyword"> Adobe </span> verwijzen. Het wordt normaal gebruikt als deel van de integratie met het Doel van <span class="keyword"> Adobe </span> om het raken van de <span class="keyword"> </span> servers van het Doel te verhinderen wanneer het niet noodzakelijk is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>27 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;geleid omleiden/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Door gebrek richt automatisch opnieuw wordt uitgevoerd. Nochtans, als u plaatsonderzoek/merchandising hebt gevormd om een reactie van XML of van JSON op uw Web-toepassing terug te keren, kunt u verkiezen om of de reactie 302/301 in uw Web-toepassing te ontleden of te hebben opnieuw richt tot u als deel van de resultaatreeks wordt overgegaan die. Als u doorgeeft richt opnieuw als deel van de resultaatreeks, dan kan deze markering in het malplaatje aan output worden gebruikt de herdirecte plaats. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>28 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;geleid-als-omleiden&gt; &lt;geleid-anders-omleiden&gt; &lt;/geleid-als-omleiden&gt; </span> </p> </td> 
   <td colname="col2"> <p>Wanneer u plaatsonderzoek/merchandising hebt gevormd om in de resultaatreeks opnieuw te richten, kan deze reeks markeringen worden gebruikt om te bepalen als er aan output opnieuw is gericht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>29 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;geleid-lt/&gt; &lt;geleid-bt/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze reeks markeringen laat u geleide malplaatjemarkeringen binnen de attributen van HTML inbedden. </p> <p>Voorbeeld: </p> <p> <code class="syntax html"> &lt;guided-lt/&gt;div&nbsp;&lt;guided-if-facet-long&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;style="height:&nbsp;125px;&nbsp;overflow: 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;auto;"&lt;/guided-if-facet-long&gt;&lt;guided-gt/&gt; </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Labels transportsjabloon {#reference_227D199F5A7248049BE1D405C0584751}

De malplaatjes van het vervoer zijn de malplaatjes van XML die gegevens van het achterste deelonderzoek tot de Begeleide de presentatielaag van het Onderzoek overgaan.

<!-- 

r_transport_template_tags.xml

 -->

In uw presentatielaag, kunt u één enkel presentatiemalplaatje hebben dat de resultaten van veelvoudige onderzoeken voorstelt. Elk onderzoek kon het zelfde vervoermalplaatje of een malplaatje van het douanevervoer gebruiken om de gegevens tot de presentatielaag over te gaan.

Omdat het vervoermalplaatje slechts wordt gebruikt om gegevens tot de presentatielaag over te gaan, heeft het geen HTML dat met het tonen van de onderzoeksresultaten betrokken is. Het vervoermalplaatje gebruikt de markeringen van XML van het vervoermalplaatje om de onderzoeksresultaten over te gaan voor het bevolken van de Geleide componenten van het Onderzoek, zoals facetten, broodkruimels, en menu&#39;s. Binnen deze markeringen worden de standaard markeringen van het onderzoeksmalplaatje gebruikt om de daadwerkelijke waarden te tonen.

Zie Een presentatie [bewerken of een transportsjabloon](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3).

Zie [Zoeksjabloontags](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4).

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Transportsjabloon tag </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;geleid-xml&gt;&lt;/geleide-xml&gt; </span> </p> </td> 
   <td colname="col2"> <p>De markeringen van wortelXML die de presentatielaag gebruikt om te ontdekken wat uit het vervoermalplaatje wordt ontleed. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;algemeen&gt;&lt;/general&gt; </span> </p> </td> 
   <td colname="col2"> <p>De markeringen omringen de markeringen van het onderzoeksmalplaatje die summiere gegevens verstrekken die op de resultaatreeks worden gebaseerd. Typisch, bevatten deze markeringen onderzoeksmarkeringen voor totaal aantal resultaten, lager resultaat, en hoogste resultaat. U kunt om het even welk aantal extra globale gebieden bepalen die u met de <span class="codeph"> algemeen-gebied </span> markering, zoals in het volgende voorbeeld wilt: </p> <p> <code class="syntax html"> &lt;general&gt; 
      &nbsp;&nbsp;&lt;total&gt;&lt;search-total&nbsp;/&gt;&lt;/total&gt; 
      &nbsp;&nbsp;&lt;lower&gt;&lt;search-lower&nbsp;/&gt;&lt;/lower&gt; 
      &nbsp;&nbsp;&lt;upper&gt;&lt;search-upper&nbsp;/&gt;&lt;/upper&gt; 
      &nbsp;&nbsp;&lt;general-field&nbsp;name="my_custom_field"&gt;Some&nbsp;global&nbsp;content&lt;/general-field&gt; 
      &lt;/general&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;resultaten&gt;&lt;/resultaten&gt; </span> </p> </td> 
   <td colname="col2"> <p>De markeringen worden verpakt rond de onderzoeksresultaten, zodat Geleid Onderzoek weet waar te om hen te zoeken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;resultaat&gt;&lt;/resultaat&gt; </span> </p> </td> 
   <td colname="col2"> <p>De markeringen worden verpakt rond elk onderzoeksresultaat, zodat Geleid Onderzoek erkent waar de inhoud voor één enkel onderzoeksresultaat begint en beëindigt, zoals in het volgende voorbeeld beëindigt: </p> <code class="syntax html"> &lt;results&gt; 
     &nbsp;&nbsp;&lt;search-results&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;result&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;index&gt;&lt;search-index&nbsp;/&gt;&lt;/index&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;loc&gt;&lt;search-cdata&gt;&lt;search-url&nbsp;length="500"&nbsp;/&gt;&lt;/search-cdata&gt;&lt;/loc&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;/result&gt; 
     &nbsp;&nbsp;&lt;/search-results&gt; 
     &lt;/results&gt; </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;attribuut-lijst name="tabelnaam"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Laat u door elk punt in een multi-waardelijst voor één enkel resultaat van een lus voorzien. Gebruik deze markering slechts binnen een resultaat. Zijn doel is u te laten over attributen herhalen die tot een resultaatgebied, zoals in het volgende voorbeeld behoren: </p> <code class="syntax html"> &lt;results&gt; 
     &nbsp;&nbsp;&lt;search-results&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;result&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;index&gt;&lt;search-index&nbsp;/&gt;&lt;/index&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;loc&gt;&lt;search-url&nbsp;/&gt;&lt;/loc&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;title&gt;&lt;search-title&nbsp;/&gt;&lt;/title&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;attribute-table&nbsp;name="downloads"&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;field&nbsp;name="download_title"&gt;&lt;search-display-field&nbsp;name="download_title"&nbsp;/&gt;&lt;/field&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;field&nbsp;name="download_link"&nbsp;delimiter="|"&gt;&lt;search-display-field&nbsp;name="download_link"&nbsp;/&gt;&lt;/field&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/attribute-table&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;/result&gt; 
     &nbsp;&nbsp;&lt;/search-results&gt; 
     &lt;/results&gt; </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;facetten&gt;&lt;/facetten&gt; </span> </p> </td> 
   <td colname="col2"> <p>Gaat op de resultaten over die de facetten bevolken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 
     <!--NEW 2/27/2014--> <span class="codeph"> &lt;dynamisch facet&gt;&lt;/dynamic facet&gt; </span> </p> </td> 
   <td colname="col2"> <p> U kunt een facet aanwijzen als zowel een dynamisch facet als een lid van een facetspoorstaaf. De behandeling ervan is echter onafhankelijk van de gerelateerde sjabloontags voor presentaties. </p> <p>Met andere woorden, het nestelen van een facetspoorloopingscontext binnen een dynamische facetloopingscontext, of vice versa, wordt niet toegestaan. </p> <p>Voor facetten die zowel dynamisch als geschraapt zijn, slechts zijn die dynamische facetten die voor een bepaalde opsporing zijn teruggekeerd zichtbaar binnen de van de facetspoorlijnen looping context. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;facet name="name"&gt;&lt;/facet&gt; </span> </p> </td> 
   <td colname="col2"> <p> Elke facet heeft zijn eigen facetmarkeringen waar de naamparameter de facetnaam aanpast. De markeringen van het onderzoek worden gebruikt binnen de facetmarkeringen voor de facetwaarden, zoals in het volgende voorbeeld: </p> <code class="syntax html"> &lt;facets&gt; 
     &nbsp;&nbsp;&lt;facet&nbsp;name="brand"&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;values&gt;&lt;search-field-value-list&nbsp;name="brand"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/values&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;counts&gt;&lt;search-field-value-list&nbsp;name="brand"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="counts"&nbsp;sortby="values"&nbsp;/&gt;&lt;/counts&gt; 
     &nbsp;&nbsp;&lt;/facet&gt; 
     &nbsp;&nbsp;&lt;facet&nbsp;name="category"&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;values&gt;&lt;search-field-value-list&nbsp;name="category"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/values&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;counts&gt;&lt;search-field-value-list&nbsp;name="category"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="counts"&nbsp;sortby="values"&nbsp;/&gt;&lt;/counts&gt; 
     &nbsp;&nbsp;&lt;/facet&gt; 
     &lt;/facets&gt; </code> <p> De rekeningen die vangnetten gebruiken kunnen de dynamische markering en de vertoning-namen markering gebruiken. Beide markeringen helpen de afbeelding tussen sterke facetten en echte facetten te vergemakkelijken terwijl het creëren van bedrijfsregels. </p> <code class="syntax html"> &lt;facets&gt; 
     &nbsp;&nbsp;&lt;facet&nbsp;name="facet_values01"&gt; 
     &nbsp;&lt;dynamic&gt;1&lt;/dynamic&gt; 
     &nbsp;&lt;display-names&gt;&lt;search-field-value-list&nbsp;name="facet_names01"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/display-names&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;values&gt;&lt;search-field-value-list&nbsp;name="facet_values01"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/values&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;counts&gt;&lt;search-field-value-list&nbsp;name="facet_values01"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="counts"&nbsp;sortby="values"&nbsp;/&gt;&lt;/counts&gt; 
     &nbsp;&nbsp;&lt;/facet&gt; </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field separator=","&gt; </span> </p> </td> 
   <td colname="col2"> <p>Het <span class="codeph"> separatorattribuut </span> laat de afbakening veranderen die wordt gebruikt wanneer u output onderzoek-vertoning-gebied gegevens voor lijsten. Het gebrek is een komma. </p> <p>Over het algemeen, zou de afbakening u gebruikt iets moeten zijn dat niet gemakkelijk in uw gebiedsinhoud verschijnt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;suggesties&gt;&lt;/suggesties&gt; </span> </p> </td> 
   <td colname="col2"> <p> Verpak uw Bedoelde u suggesties met markeringen zodat het Begeleide Onderzoek erkent welke knopen van XML suggesties bevatten. </p> <p>Zie <a href="../c-about-linguistics-menu/c-about-did-you-mean.md#concept_7D4F3C29EF184B538B8AE2ECAE0CDC5E" type="concept" format="dita" scope="local"> over wat je bedoelt</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;suggestie&gt;&lt;/suggestie&gt; </span> </p> </td> 
   <td colname="col2"> <p>De omslag elk Bedoelde u suggestie met markeringen, zoals in het volgende voorbeeld: </p> <code class="syntax html"> &lt;search-if-suggestions&gt; 
     &nbsp;&nbsp;&lt;suggestions&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;search-suggestions&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;suggestion&gt;&lt;search-suggestion-text&nbsp;/&gt;&lt;/suggestion&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-suggestions&gt; 
     &nbsp;&nbsp;&lt;/suggestions&gt; 
     &lt;/search-if-suggestions&gt; </code> <p>Zie <a href="../c-about-linguistics-menu/c-about-did-you-mean.md#concept_7D4F3C29EF184B538B8AE2ECAE0CDC5E" type="concept" format="dita" scope="local"> over wat je bedoelt</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Zoeksjabloontags {#reference_F7AA3FF602314E42842BBC740D2CA1A4}

Een onderzoekstemplate is een HTML- dossier dat malplaatjemarkeringen omvat die de plaatsonderzoek/de handel drijven bepaalt. Deze markeringen wijzen erop hoe uw onderzoeksresultaten geformatteerd zijn. De volgende verwijzing bevat een korte beschrijving van elke markering van het onderzoeksmalplaatje en zijn attributen.

<!-- 

r_search_template_tags.xml

 -->

>[!NOTE]
>
>Gebruik slechts de markeringen van het onderzoeksmalplaatje in de dossiers van het vervoermalplaatje (.tpl).

U kunt uit de volgende de markeringsgroepen en verwijzingsmateriaal van het onderzoeksmalplaatje selecteren.

De markeringen die slechts binnen de resultatenlijn geldig zijn omvatten het volgende:

* [Over Resultaatlijnen](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629)
* [Resultaatreeksen](../c-appendices/c-templates.md#section_80D68334E8D04A33937A6E58ABAAA320)
* [Resultaatlus voorwaardelijke tags](../c-appendices/c-templates.md#section_35C367969E384A06A9865E388F1F9360)
* [Resultaatankerkoppelingtags](../c-appendices/c-templates.md#section_C5FAEF520E9E42ADAD1F90651922AA02)
* [Voorwaardelijke tags voor positie laden](../c-appendices/c-templates.md#section_E0C29DDA09E043C9A396F36334F05EBB)

De markeringen die door het malplaatje geldig zijn omvatten het volgende:

* [Labels in lijst met velden](../c-appendices/c-templates.md#section_D3298B5F976447DBA0032B883DCC91B1)
* [Lijstcodes van lijst met velden](../c-appendices/c-templates.md#section_0717FA09F0FC449CB916883B0500A60E)
* [Tags voorstellen](../c-appendices/c-templates.md#section_C28EB8B4F7DC4E278A0F143BCFEEB1AC)
* [Sjabloonreekscodes](../c-appendices/c-templates.md#section_67E3D529661F4F03A1FF469D9D658CAF)
* [Sjabloonankerkoppelingtags](../c-appendices/c-templates.md#section_3A51D27616C541E2B818CC52B2B856BA)
* [Voorwaardelijke tags voor template](../c-appendices/c-templates.md#section_18D9BC66DE484881932FD2F7EA9D170D)
* [Sjabloonformulierbesturingscodes](../c-appendices/c-templates.md#section_45AFC414ACA74825B72FEAA8456F8DD2)

Referentieonderwerpen Zoeksjabloon zoeken

* [Datumformaatstrings](../c-appendices/c-templates.md#section_4BBDBBEF2B96414497617CD4B52D96E4)
* [Taalidentificatie](../c-appendices/c-templates.md#section_0490DECC00E34691ADE5A9ED90A6D911)
* [Het specificeren van de inhoud-type HTTP- kopbal](../c-appendices/c-templates.md#section_AEED823E9938448A9EDB2F286D9CFD90)
* [Het specificeren van een karakter dat in een malplaatje van HTML wordt geplaatst](../c-appendices/c-templates.md#section_E0D1816ABB5846BEBE9C26D5980CCBE6)
* [Het specificeren van een karakter dat in een malplaatje van XML wordt geplaatst](../c-appendices/c-templates.md#section_17DC31CDCC104F5F8081466B41A96E9D)
* [Inclusief een zoekopdrachtsjabloon in een andere](../c-appendices/c-templates.md#section_7D1FCD3D9E2340C291E354C9720E8BC0)

## Over Resultaatlijnen {#section_D4DC7B4560144663972E8DBC3369C629}

De markering van de resultatenlijn is het werkpaard van het malplaatjesysteem. Wanneer de markering tijdens een onderzoek wordt ontmoet, wordt HTML herhaald en andere markeringen tussen het begin en het einde van resultatenlijn markeringen, die een andere markeringen vervangen met uw onderzoeksresultaten.

`<search-results> ... </search-results>`

De codes van de resultatenlijn omringen HTML dat de onderzoeksresultaten toont. HTML tussen de markeringen wordt herhaald voor elk resultaat en op de pagina getoond.

De volgende markeringen zijn geldig slechts binnen de resultatenlijn:

* [Resultaatreeksen](../c-appendices/c-templates.md#section_80D68334E8D04A33937A6E58ABAAA320)
* [Resultaatlus voorwaardelijke tags](../c-appendices/c-templates.md#section_35C367969E384A06A9865E388F1F9360)
* [Resultaatankerkoppelingtags](../c-appendices/c-templates.md#section_C5FAEF520E9E42ADAD1F90651922AA02)
* [Voorwaardelijke tags voor positie laden](../c-appendices/c-templates.md#section_E0C29DDA09E043C9A396F36334F05EBB)

## Resultaatreeksen {#section_80D68334E8D04A33937A6E58ABAAA320}

De volgende markeringen keren een koord terug.

Zie [Over Resultaatlusjes](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-index&gt; </span> </p> </td> 
   <td colname="col2"> <p>Keert de numerieke index van het huidige resultaat terug. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-title length="XX"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Keert de paginatitel van het huidige resultaat terug. Het facultatieve lengteattribuut wordt gebruikt om de lengte van getoonde koorden, met een gebrek van 80 karakters te beperken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-body text length="XX" encoding="html/javascript/json/perl/url/none" &gt; </span> </p> </td> 
   <td colname="col2"> <p>Keert de lichaamstekst terug die van de bovenkant van de pagina begint. Relevante termen worden vetgedrukt weergegeven. Het facultatieve lengteattribuut wordt gebruikt om de lengte van getoonde koorden, met een gebrek van 80 karakters te beperken. Het coderende attribuut is facultatief en het kan outputkarakters met het coderen van HTML (gebrek) coderen, het coderen Javascript, het coderen Perl, of niets coderen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-description length="XX" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Keert de beschrijving van het huidige resultaat terug. Als de meta beschrijvingsmarkering bestaat en het inhoudsattribuut niet leeg is, wordt die tekst getoond. Anders, wordt het begin van de lichaamstekst van de pagina getoond. Het facultatieve lengteattribuut wordt gebruikt om de lengte van getoonde koorden, met een gebrek van 80 karakters te beperken. </p> <p>De facultatieve <span class="codeph"> het coderen </span> attributen controleert of de output gecodeerde HTML is, JavaScript gecodeerd, Perl gecodeerd, URL gecodeerd of niet gecodeerd, voor output op de resultatenpagina wordt gecodeerd. De standaardwaarde van het <span class="codeph"> coderen </span> is <span class="codeph"> html </span>. Normaal, te hoeven u niet om de het coderen attributen te specificeren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;zoekscore rank="dynamisch/statisch/dynamisch-ruw/statisch-ruw/finaal-ruw" precision="XX"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Keert de score van het huidige resultaat terug, dat een aantal 0 - 100 is. Als u een rangschikkingsgebied onder <span class="uicontrol"> Opties </span> &gt; <span class="uicontrol"> Meta-gegevens </span> &gt; <span class="uicontrol"> Definities hebt bepaald </span>, kunt u de dynamische paginagang tonen door de rangtelattributen aan dynamisch te plaatsen ( <span class="codeph"> &lt;search-score rank="dynamic"&gt; </span>). U kunt de statische paginarang tonen door de rangtelattributen aan statisch te plaatsen ( <span class="codeph"> &lt;search-score rank="statisch"&gt; </span>). U kunt de facultatieve precisiekenmerken gebruiken om het aantal decimalen aan vertoning te specificeren. Het gebrek is 0 die de geheelscore toont). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-date length="XX" none="text" date-format="date-format-string" gmt="yes/no" language="0/2/language-id"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Keert de datum van het huidige resultaat terug. De facultatieve "niets"tekstwaarde wordt getoond als er geen datum verbonden aan het huidige resultaat is. Als de facultatieve "niets"waarde niet wordt gegeven, wordt de tekst "Geen Datum"getoond als er geen datum verbonden aan het huidige resultaat is. </p> <p>Het attribuut "date-format" neemt een UNIX-tekenreeks met datumnotatie voor de stijl zoals "%A, %B %d, %Y" (voor "Maandag, 25 juli, 2016"). "gmt" staat in gebreke aan "ja" en controleert of het tijdgedeelte van het datumkoord output in GMT ("ja") of de de tijdzone van de rekening ("neen") zou moeten zijn. </p> <p>Het "taal"attribuut controleert de taal en de scèneovereenkomsten van het koord van de outputdatum. "0" (de standaardinstelling) betekent "Account Language gebruiken". "2" betekent "Documenttaal gebruiken". De waarde "1" voor "taal" is gereserveerd voor toekomstig gebruik. Een andere "taal"-waarde wordt geïnterpreteerd als een specifieke taalidentifier, bijvoorbeeld "en_US" betekent "Engels (Verenigde Staten)". </p> <p>Het facultatieve lengteattribuut wordt gebruikt om de lengte van getoonde koorden, met een gebrek van 80 karakters te beperken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;grootte van zoekopdrachten&gt; </span> </p> </td> 
   <td colname="col2"> <p>Keert de grootte van het huidige resultaat in bytes terug. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-url length="XX" encoding="html/javascript/json/perl/url/none" &gt; </span> </p> </td> 
   <td colname="col2"> <p>Keert URL van het huidige resultaat terug. </p> <p>Gebruik de facultatieve <span class="codeph"> lengteattributen </span> om de lengte van getoonde koorden, met een gebrek van onbeperkte karakters te beperken. </p> <p>Het <span class="codeph"> het coderen </span> attribuut is facultatief en het kan outputkarakters met het coderen van HTML, het coderen Javascript, het coderen Perl coderen, of niets coderen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-url-path-query length="XX"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Keert de weg en vraaggedeelten met inbegrip van het vraagteken van URL van het huidige resultaat terug. </p> <p>Gebruik de facultatieve <span class="codeph"> lengteattributen </span> om de lengte van getoonde koorden, met een gebrek van onbeperkte karakters te beperken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-context length="XX" encoding="html/javascript/json/perl/url/none" &gt; </span> </p> </td> 
   <td colname="col2"> <p>Keert de volgende lijn van context voor de onderzoekstermijn terug. Relevante termen worden vetgedrukt weergegeven. Oproepen deze markering herhaaldelijk om meer dan één contextlijn voor het huidige resultaat te tonen. </p> <p>Gebruik de facultatieve <span class="codeph"> lengteattributen </span> om de lengte van getoonde koorden, met een gebrek van 80 karakters te beperken. Het <span class="codeph"> lengteattribuut wordt </span> genegeerd als deze markering door of <span class="codeph"> &lt;search-if-context&gt; </span> of <span class="codeph"> </span> &lt;search-if-any-context&gt; de markeringsreeksen wordt ingesloten die een lengteattribuut bevatten. </p> <p>Het <span class="codeph"> het coderen </span> attribuut is facultatief en het kan outputkarakters met het coderen van HTML (gebrek) coderen, het coderen Javascript, het coderen Perl, of niets coderen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field name="field-name" length="XX" none="text" date-format="date-format-string" gmt="yes/no" language="0/2/language-id" encoding="html/javascript/json/perl/url/none" quotes="yes/no" commas="yes/no" units="yes/no" units="kilometers="mijlen/kilometers" scheidingsteken="|"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze geavanceerde markering toont de inhoud van het meta-gegevensgebied (url, titel, bureau, sleutels, doel, lichaam, alt, datum, charset, en taal of de gebieden die onder <span class="uicontrol"> Opties worden bepaald &gt; </span> Meta-gegevens <span class="uicontrol"> &gt; Definities) in de </span> naam <span class="codeph"> </span> attributen, voor het huidige resultaat worden gespecificeerd. Bijvoorbeeld: </p> <p> <span class="codeph"> &lt;search-display-field name="title" length="70" none="no title"&gt; </span> </p> <p>Voert de titel van de pagina voor een onderzoeksresultaat uit. Als de optionele <span class="codeph"> none- </span> eigenschap is opgegeven, wordt de waarde alleen weergegeven op de resultatenpagina als er geen inhoud aan het veld is gekoppeld. </p> <p>De <span class="codeph"> datum-formaat </span>, <span class="codeph"> gmt </span> en <span class="codeph"> taal- </span> attributen zijn slechts relevant als het inhoudstype van het gespecificeerde gebied <span class="codeph"> datum is </span>. </p> <p>Het <span class="codeph"> date-format </span> attribuut neemt een koord van het de formaatformaat van de de stijldatum van UNIX zoals <span class="codeph"> %A, %B %d, %Y </span> (voor Maandag, 25 Juli, 2016). <span class="codeph"> gmt </span> blijft aan <span class="codeph"> ja in gebreke </span> en controleert of het tijdgedeelte van het datumkoord output in GMT ( <span class="codeph"> ja </span>) of de tijdzone van de rekening ( <span class="codeph"> neen </span>) is. </p> <p>Zie <a href="../c-appendices/c-templates.md#section_4BBDBBEF2B96414497617CD4B52D96E4" type="section" format="dita" scope="local"> Datumformaatstrings</a>. </p> <p>Het <span class="codeph"> taalattribuut </span> controleert de taal en scèneovereenkomsten van het koord van de outputdatum. <span class="codeph"> 0 </span> (het gebrek) betekent "de Taal van de Rekening van het Gebruik". <span class="codeph"> 2 </span> "Documenttaal gebruiken". De <span class="codeph"> taalwaarde </span> 1 <span class="codeph"> </span> is gereserveerd voor toekomstig gebruik). Een andere <span class="codeph"> taalwaarde wordt </span> geïnterpreteerd als een specifieke taalidentifier, bijvoorbeeld, <span class="codeph"> en_US </span> betekent "Engels (Verenigde Staten)". </p> <p>Zie <a href="../c-appendices/c-templates.md#section_0490DECC00E34691ADE5A9ED90A6D911" type="section" format="dita" scope="local"> Taalkenmerken</a>. </p> <p>Het facultatieve <span class="codeph"> lengteattribuut wordt </span> gebruikt om de lengte van getoonde koorden, met een gebrek van 80 karakters te beperken. </p> <p>De facultatieve <span class="codeph"> het coderen </span> attributen controleert of de output gecodeerde HTML is, JavaScript gecodeerd, Perl gecodeerd, URL gecodeerd of niet gecodeerd, voor output op de resultatenpagina wordt gecodeerd. De standaardwaarde van het <span class="codeph"> coderen </span> is <span class="codeph"> html </span>. Normaal, te hoeven u niet om de het coderen attributen te specificeren. </p> <p>De facultatieve <span class="codeph"> citaten </span> attribuut controleert of de individuele puntenoutput door dubbel-citaten (of enig-citaten, als het <span class="codeph"> coderen=perl </span>) wordt omringd. De standaardwaarde van <span class="codeph"> citaten </span> is <span class="codeph"> neen </span>. </p> <p>De facultatieve <span class="codeph"> komma's </span> attributen controleert of de individuele puntenoutput door komma's wordt gescheiden. De standaardwaarde van <span class="codeph"> komma's </span> is <span class="codeph"> ja </span>. Het <span class="codeph"> komma- </span> attribuut wordt genegeerd voor niet-lijst-type gebieden. </p> <p>Het optionele <span class="codeph"> unit- </span> kenmerk bepaalt de afstand-eenheden die worden toegepast op een veld voor zoekresultaten in de nabijheid. De standaardwaarde van <span class="codeph"> eenheden </span> wordt bepaald van de instelling "Standaardeenheden" van het locatie-type veld dat is gekoppeld aan het gegeven veld voor zoekresultaten in de nabijheid. </p> <p>Zie <a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> over nabijheidsonderzoek</a>. </p> <p>Het facultatieve <span class="codeph"> separatorattribuut </span> bepaalt het enige karakter, of afbakening, dat tussen de waarden van de output voor lijst-type gebieden wordt opgenomen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field-values name="field-name"&gt; ...&lt;zoek-vertoning-gebied-waarden&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze markering leidt tot een lijn voor het opsommen van de waarden van het meta-gegevensgebied (url, titel, bureau, sleutels, doel, lichaam, alt, datum, charset, en taal of gebieden die onder <span class="uicontrol"> Opties </span> &gt; <span class="uicontrol"> Meta-gegevens </span> &gt; <span class="uicontrol"> Definities </span>) worden bepaald voor het huidige resultaat. Nesten deze markering niet binnen een andere <span class="codeph"> &lt;search-display-field-values&gt; </span> markering. Het <span class="codeph"> naam </span> attribuut specificeert de naam van het gebied dat de op te sommen waarden bevat. Deze markering is het nuttigst met gebieden die de <span class="uicontrol"> Allow gecontroleerde attributen van Lijsten hebben (onder </span> Opties <span class="uicontrol"> &gt; </span> Meta-gegevens <span class="uicontrol"> &gt; </span> - Definities <span class="uicontrol"> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field-value date-format="date-format-string" gmt="yes/no" language="0/language-id" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze markering voert de waarde van het meta-gegevensgebied (url, titel, bureau, sleutels, doel, lichaam, alt, datum, charset, en taal of de gebieden uit die onder <span class="uicontrol"> Opties </span> &gt; <span class="uicontrol"> Meta-gegevens </span> &gt; <span class="uicontrol"> Definities </span>) worden bepaald voor de huidige <span class="codeph"> &lt;zoek-vertoning-gebied-waarden&gt; </span> lijnherhaling. Deze markering is slechts geldig binnen een <span class="codeph"> &lt;onderzoek-vertoning-gebied-waarden&gt; </span> lijn. De <span class="codeph"> datum-formaat </span>, <span class="codeph"> gmt </span> en <span class="codeph"> taal </span> attributen zijn slechts relevant als het inhoudstype van de gebiedsnaam die in de bijgevoegde <span class="codeph"> &lt;zoek-vertoning-gebied-waarden&gt; </span> markering wordt gespecificeerd datum is <span class="codeph"> </span>. Het <span class="codeph"> date-format </span> attribuut neemt een koord van het de formaatformaat van de de stijldatum van UNIX zoals <span class="codeph"> "%A </span>, <span class="codeph"> %B </span> %d <span class="codeph"> , </span>%Y <span class="codeph"> </span>" (voor "Maandag, Juli 25, 2016"). Het <span class="codeph"> gmt </span> attribuut blijft aan ja in gebreke <span class="codeph"> en controleert of het tijdgedeelte van het datumkoord output in GMT ( </span> ja <span class="codeph"> ) of de de tijdzone van de rekening ( </span>neen <span class="codeph"> </span>) is. </p> <p>Het <span class="codeph"> taalattribuut </span> controleert de taal en scèneovereenkomsten van het koord van de outputdatum. <span class="codeph"> 0 </span> (het gebrek) betekent "de Taal van de Rekening van het Gebruik". Een andere <span class="codeph"> taalwaarde wordt </span> geïnterpreteerd als een specifieke taalidentifier, bijvoorbeeld, <span class="codeph"> en_US </span> betekent "Engels (Verenigde Staten)". </p> <p>De facultatieve <span class="codeph"> het coderen </span> attributen controleert of de output gecodeerde HTML is, JavaScript gecodeerd, Perl gecodeerd, URL gecodeerd of niet gecodeerd, voor output op de resultatenpagina wordt gecodeerd. De standaardwaarde van het <span class="codeph"> coderen </span> is <span class="codeph"> html </span>. Normaal, te hoeven u niet om de het coderen attributen te specificeren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field-value-count name="field-name"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Output het totale aantal waarden in het huidige resultaat voor het meta-gegevensgebied (url, titel, desc, sleutels, doel, lichaam, alt, datum, charset, en taal of de gebieden die onder <span class="uicontrol"> Opties </span> &gt; <span class="uicontrol"> Meta-gegevens </span> &gt; <span class="uicontrol"> Definities worden bepaald </span>) met de naamattributen worden gespecificeerd. Deze markering kan overal in de resultatenlijn verschijnen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;zoek-display-field-value-teller&gt; </span> </p> </td> 
   <td colname="col2"> <p>Output de rangschikkende teller (1, 2, 3, etc.) voor de huidige <span class="codeph"> &lt;onderzoek-vertoning-gebied-waarden&gt; </span> lijnherhaling. Deze markering is slechts geldig binnen een <span class="codeph"> &lt;onderzoek-vertoning-gebied-waarden&gt; </span> lijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;zoek-dynamisch-facetvelden&gt; </span> </p> </td> 
   <td colname="col2"> <p>Begint een het van een lus voorzien context voor om het even welke dynamisch-facet-gebieden die voor dit onderzoek zijn teruggekeerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;zoek-dynamisch-facet-gebied-naam&gt; </span> </p> </td> 
   <td colname="col2"> <p>Output de naam van het huidige dynamisch-facet-gebied, voor deze lijnherhaling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW for S&P 8.17.0 release on October 30 2014--> <span class="codeph"> &lt;search-result-trace encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>De informatie van de output met betrekking tot de plaatsing van het huidige resultaat, bijvoorbeeld, om het even welke op resultaten-gebaseerde acties die de positie van het resultaat beïnvloedden. </p> <p>Het outputformaat van deze markering is JSON zoals in het volgende voorbeeld: </p> <p> <code> { 
      &nbsp;&nbsp;"sliceID":&nbsp;5, 
      &nbsp;&nbsp;"indexID":&nbsp;5894, 
      &nbsp;&nbsp;"finalScore":&nbsp;98.5, 
      &nbsp;&nbsp;"dynamicScore":&nbsp;15.3, 
      &nbsp;&nbsp;"staticScore":&nbsp;55.456, 
      &nbsp;&nbsp;"position":&nbsp;1, 
      &nbsp;&nbsp;"rbtaActionListID":&nbsp;117, 
      &nbsp;&nbsp;"rbtaActionID":&nbsp;57 
      } </code> </p> 
    <!--<p> Results added to the results set by way of <codeph>rbta</codeph> have a "naturalPosition" value of -1. </p>--> <p>Het <span class="codeph"> het coderen </span> attribuut is facultatief; de standaardwaarde is <span class="codeph"> html </span>. </p> <p> <p>Opmerking:  Deze markering heeft slechts output als <span class="codeph"> sp_trace=1 </span> met de de vraagparameters van het kernonderzoek wordt gespecificeerd. </p> </p> <p>Zie rij 48 in de lijst die in de parameters <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" format="dita" scope="local"> wordt gevonden van het Onderzoek van de</a>Achtergrond CGI. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Resultaatlus voorwaardelijke tags {#section_35C367969E384A06A9865E388F1F9360}

De volgende markeringen omvatten voorwaardelijk HTML tussen hen.

Zie [Over Resultaatlusjes](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-title&gt; ... &lt;/search-if-title&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-title&gt; ... &lt;/search-if-not-title&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze markeringen omvatten HTML tussen hen als de volgende vraag aan <span class="codeph"> &lt;zoek-titel&gt; </span> (of niet terugkeert) tekst van de documenttitel terugkeert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-description length="XX"&gt; ... /search-if-description&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-description&gt; ... &lt;/search-if-not description&gt; </span> </p> </td> 
   <td colname="col2"> <p> Deze markeringen omvatten HTML tussen hen als de volgende vraag aan <span class="codeph"> &lt;zoek-beschrijving&gt; </span> (of niet terugkeert) tekst van de documentbeschrijving terugkeert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-body text&gt; ... &lt;/search-if-body text&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-body text&gt; ... &lt;/search-if-not-body text&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze markeringen omvatten HTML tussen hen als de volgende vraag aan <span class="codeph"> &lt;search-body text&gt; </span> (of niet terugkeert) tekst van het documentlichaam terugkeert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-context length="XX"&gt; ... &lt;/search-if-context&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-context&gt; ... &lt;/search-if-not-context&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze markeringen omvatten HTML tussen hen als de volgende vraag aan <span class="codeph"> &lt;search-context&gt; </span> terugkeert (of niet terugkeert) een niet lege contextkoord. Het lengteattribuut treedt de lengteattributen op om het even welke ingesloten <span class="codeph"> &lt;zoek-context&gt; </span> markering met voeten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-any-context length="XX"&gt; ... /search-if-any-context&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-any-context&gt; ... &lt;/search-if-not-any-context&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze markeringen omvatten HTML tussen hen als er (of niet) een contextkoord verbonden aan het resultaat is. Het lengteattribuut treedt de lengteattributen op om het even welke ingesloten <span class="codeph"> &lt;zoek-context&gt; </span> markering met voeten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-score lower="XX" upper="yy" rank="dynamic/statische/dynamic-raw/statische-raw/final-raw"&gt; ... &lt;/search-if-score&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-score lower=XX upper=yy rank="dynamic/statische"&gt; ... &lt;/search-if-not-score&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze markeringen omvatten HTML tussen hen als de score van het huidige resultaat (of niet) tussen XX en YY is. Nuttig voor het toevoegen van kogels of grafiek om te tonen hoe relevant het resultaat is. Als u een rank-type gebied onder <span class="uicontrol"> Opties </span> &gt; <span class="uicontrol"> Meta-gegevens </span> &gt; <span class="uicontrol"> Definities hebt bepaald </span>, kunt u de dynamische paginagang controleren door de rangtelattributen aan dynamisch te plaatsen ( <span class="codeph"> &lt;search-if-score rank="dynamic" lower=XX upper=YY&gt; </span>). U kunt de statische paginarang controleren door de rangtelattributen aan statisch te plaatsen ( <span class="codeph"> &lt;search-if-score rank="statisch"lower=XX upper=YY&gt; </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-field name="field-name" value="value"&gt; ... &lt;/search-if-veld&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-field name="field-name" value="value"&gt; ... &lt;/search-if-not-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze geavanceerde markeringen omvatten HTML tussen hen gebaseerd op of het gebied dat in het "naam"attribuut wordt gespecificeerd inhoud of niet heeft. Als de optionele "waarde"-eigenschap is opgegeven, wordt de HTML-code tussen de tags gegeven op basis van de vraag of de gegeven waarde overeenkomt (of niet overeenkomt) met de waarde voor het veld in het huidige resultaat. Deze markeringen functioneren slechts binnen de resultatenlijn (tussen <span class="codeph"> &lt;search-results&gt; </span> en <span class="codeph"> &lt;/search-results&gt; </span> markeringen). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Resultaatankerkoppelingtags {#section_C5FAEF520E9E42ADAD1F90651922AA02}

Zie [Over Resultaatlusjes](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-link target="frame-name" hbx-enable="yes/no" hbx-linkid-name="field-name" hbx-linkid-none="text" hbx-linkid-length="XX" &gt;... &lt;/search-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Dit paar markeringen leidt tot een ankerverbinding rond HTML tussen hen. Wanneer de verbinding wordt geklikt, de vertoningen van de resultatenpagina. Een facultatief doelattribuut specificeert het genoemde venster waarin kader-geschikt browsers de resultatenpagina zouden moeten tonen. </p> <p>Plaats hbx-toelaten attributen aan "ja"om uit de analyses voordeel te halen beschikbaar door HBX. De vastgestelde hbx-linkid-naam aan de naam van een meta-gegeven gebied u zou willen volgen. Bijvoorbeeld, om onderzoeksresultaten door aantal van SKU te volgen, plaats hbx-linkid-name aan de naam van het meta-gegeven gebied dat de informatie van SKU bevat. </p> <p>Datumtype velden worden momenteel niet ondersteund. De waarde van hbx-linkid-name wordt toegevoegd aan verbindingsidentiteitskaart in het geproduceerde anker. De waarde van hbx-linkid-none attributen wordt toegevoegd aan verbindingsidentiteitskaart wanneer het genoemde meta-gegeven gebied leeg is. De waarde van hbx-linkid-length beperkt het aantal karakters die van de markering van Meta worden gehaald en worden getoond. Het standaardaantal karakters is 12. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-smart-link target="frame-name" hbx-enable="yes/no" hbx-linkid-name="field-name" hbx-linkid-none="text" hbx-linkid-length="XX"&gt; ... &lt;/search-smart-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Dit paar markeringen is gelijkaardig aan <span class="codeph"> &lt;search-link&gt;.. &lt;/search-link&gt; </span> -tags. Wanneer de geproduceerde ankerverbindingen worden geklikt, de vertoningen van de resultatenpagina, maar met de pagina aan de meest dichtbijgelegen ankermarkering die het resultaat voorafgaat wordt gescrold. Voor verbindingen PDF, toont de kijker van de Acrobaat de pagina die het resultaat bevat. Een facultatief doelattribuut specificeert het genoemde venster waarin kader-geschikt browsers de resultatenpagina zouden moeten tonen. </p> <p>Plaats hbx-toelaten attributen aan "ja"om uit de analyses voordeel te halen beschikbaar door HBX. De vastgestelde hbx-linkid-naam aan de naam van een meta-gegeven gebied u zou willen volgen. Bijvoorbeeld, om onderzoeksresultaten door aantal van SKU te volgen, plaats hbx-linkid-name aan de naam van het meta-gegeven gebied dat de informatie van SKU bevat. </p> <p>Datumtype velden worden momenteel niet ondersteund. De waarde van hbx-linkid-name wordt toegevoegd aan verbindingsidentiteitskaart in het geproduceerde anker. De waarde van hbx-linkid-none attributen wordt toegevoegd aan verbindingsidentiteitskaart wanneer het genoemde meta-gegeven gebied leeg is. De waarde van hbx-linkid-length beperkt het aantal karakters die van de markering van Meta worden gehaald en worden getoond. Het standaardaantal karakters is 12. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-link-extension&gt; ... &lt;/search-if-link-extensie&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-link-extension&gt; ... &lt;/search-if-not-link-extension&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze markeringen omvatten HTML tussen hen als een waardeattribuut een uitbreiding specificeert die het eind van URL voor het resultaat aanpast. Deze markering is nuttig om grafisch in de onderzoeksresultaten te omvatten die op de verbindingsuitbreiding worden gebaseerd. Het waardeattribuut is een lijst van één of meerdere uitbreidingen (gescheiden ruimte) als volgt: VALUE=".pdf" of VALUE=".html .htm". </p> </td> 
  </tr> 
 </tbody> 
</table>

## Voorwaardelijke tags voor positie laden {#section_E0C29DDA09E043C9A396F36334F05EBB}

De volgende markeringen omvatten voorwaardelijk de tekst tussen hen. Zij kunnen slechts binnen de &quot;het van een lus voorzien&quot;markeringen verschijnen: &lt; `search-results>` en `<search-field-values>`. Zij worden gebruikt om de positie van het huidige resultaat binnen de resultaatreeks te testen.

Zie [Over Resultaatlusjes](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-first&gt; ... &lt;/search-if-first&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-first&gt; ... &lt;/search-if-not-first&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze markeringen omvatten de tekst tussen hen als het huidige resultaat (of is niet) het eerste resultaat op de pagina (wanneer gebruikt binnen <span class="codeph"> &lt;zoek-resultaten&gt; </span>) of de eerste gebiedswaarde (wanneer gebruikt binnen <span class="codeph"> &lt;zoek-gebied-waarden&gt; </span>) is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-last&gt; ... &lt;/search-if-last&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-last&gt; ... &lt;/search-if-not-last&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze markeringen omvatten de tekst tussen hen als het huidige resultaat (of is niet) het laatste resultaat op de pagina (wanneer gebruikt binnen <span class="codeph"> &lt;zoek-resultaten&gt; </span>) of de laatste gebiedswaarde (wanneer gebruikt binnen <span class="codeph"> &lt;zoek-gebied-waarden&gt; </span>) is. Deze markering kan worden gebruikt om een separator tussen resultaten op te nemen. Bijvoorbeeld, neemt dit een <span class="codeph"> &lt;hr&gt; </span> markering tussen resultaten op: </p> <p> <code class="syntax html"> &lt;search-results&gt; 
      &nbsp;&nbsp;&nbsp;&lt;search-lt&gt;tr&lt;search-if-alt&gt;&nbsp;class="alt"&lt;/search-if-alt&gt;&lt;search-gt&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;td&gt;&lt;search-url&gt;&lt;/td&gt; 
      &nbsp;&nbsp;&nbsp;&lt;/tr&gt; 
      &lt;/search-results&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-inner&gt; ... &lt;/search-if-inner&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-inner&gt; ... &lt;/search-if-not-inner&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze markeringen omvatten de tekst tussen hen als het huidige resultaat niet het eerste of het laatste resultaat op de pagina (wanneer gebruikt binnen <span class="codeph"> &lt;zoek-resultaten&gt; </span>) is of niet de eerste of laatste gebiedswaarde (wanneer gebruikt binnen <span class="codeph"> &lt;zoek-gebied-waarden&gt; </span>) is. De niet versie van de markeringstests of het resultaat of het eerste of laatste is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-alt&gt; ... &lt;/search-if-alt&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-alt&gt; ... &lt;/search-if-not-alt&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze markeringen omvatten de tekst tussen hen als het huidige resultaat (of is niet) een afwisselend resultaat op de pagina (wanneer gebruikt binnen <span class="codeph"> &lt;zoek-resultaten&gt; </span>) of een afwisselende gebiedswaarde (wanneer gebruikt binnen <span class="codeph"> &lt;zoek-gebied-waarden&gt; </span>) is. De "afwisselende"resultaten zijn tweede, vierde, zesde, etc., op de pagina. Dit voorbeeld past een verschillende klasse op afwisselende lijstrijen toe. Neem nota van het gebruik van <span class="codeph"> &lt;search-lt&gt; </span> en <span class="codeph"> &lt;search-gt&gt; </span> om toe te staan dat de <span class="codeph"> &lt;search-if-alt&gt; </span> markering "binnen"de <span class="codeph"> &lt;tr&gt; </span> markering wordt geplaatst. </p> <p> <code class="syntax html"> &nbsp;&nbsp;&nbsp;&nbsp;&lt;search-results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;search-lt&gt;tr&lt;search-if-alt&gt;&nbsp;class="alt"&lt;/search-if-alt&gt;&lt;search-gt&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;td&gt;&lt;search-url&gt;&lt;/td&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/tr&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-results&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-even&gt; ... &lt;/search-if-even&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-even&gt; ... &lt;/search-if-not-even&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze markeringen omvatten de tekst tussen hen als het huidige resultaat (of niet) een gelijk-genummerd resultaat is (wanneer gebruikt binnen <span class="codeph"> &lt;zoek-resultaten&gt; </span>) of een gelijk-genummerde gebiedswaarde (wanneer gebruikt binnen <span class="codeph"> &lt;zoek-gebied-waarden&gt; </span>). Een onderzoeksresultaat is gelijk-genummerd als zijn <span class="codeph"> &lt;zoek-index&gt; </span> waarde zelfs is. Met andere woorden, als zijn positie binnen de volledige resultaatreeks gelijk is. Dit kan van <span class="codeph"> &lt;search-if-alt&gt; verschillend zijn </span> die de positie van een resultaat op de pagina, niet binnen de volledige resultaatreeks test. De volgende twee lijsten illustreren het verschil: </p> </td> 
  </tr> 
 </tbody> 
</table>

### Eerste pagina, sp_n=1

<table>  
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Index </p> </th> 
   <th colname="col2" class="entry"> <p>Resultaat </p> </th> 
   <th colname="col3" class="entry"> <p>Zelfs? </p> </th> 
   <th colname="col4" class="entry"> <p>Alt? </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>1 </p> </td> 
   <td colname="col2"> <p>Eerste resultaat </p> </td> 
   <td colname="col3"> <p>Nee </p> </td> 
   <td colname="col4"> <p>Nee </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>Tweede resultaat </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>Derde resultaat </p> </td> 
   <td colname="col3"> <p>Nee </p> </td> 
   <td colname="col4"> <p>Nee </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>Vierde resultaat </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>5 </p> </td> 
   <td colname="col2"> <p>Vijfde resultaat </p> </td> 
   <td colname="col3"> <p>Nee </p> </td> 
   <td colname="col4"> <p>Nee </p> </td> 
  </tr> 
 </tbody> 
</table>

### Later pagina, sp_n=10

<table>  
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Index </p> </th> 
   <th colname="col2" class="entry"> <p>Resultaat </p> </th> 
   <th colname="col3" class="entry"> <p>Zelfs? </p> </th> 
   <th colname="col4" class="entry"> <p>Alt? </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>10 </p> </td> 
   <td colname="col2"> <p>Tiende resultaat </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Nee </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>11 </p> </td> 
   <td colname="col2"> <p>Elfde resultaat </p> </td> 
   <td colname="col3"> <p>Nee </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>12 </p> </td> 
   <td colname="col2"> <p>Twaalf resultaat </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Nee </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>13 </p> </td> 
   <td colname="col2"> <p>Dertiende resultaat </p> </td> 
   <td colname="col3"> <p>Nee </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>14 </p> </td> 
   <td colname="col2"> <p>Veertiende resultaat </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Nee </p> </td> 
  </tr> 
 </tbody> 
</table>

Tot slot merk op dat altijd het zelfde als `<search-if-even>` voor de waarden van het onderzoeksgebied `<search-if-alt>` is aangezien de gebiedswaarden niet worden gepagineerd.

## Labels in lijst met velden {#section_D3298B5F976447DBA0032B883DCC91B1}

De volgende geavanceerde waarden van het de gebiedsgebied van de markeringen en verwante gegevens van de volledige reeks onderzoeksresultaten. Deze markeringen brengen slechts output voor gebieden op die door de parameters van CGI in de onderzoeksvraag worden gespecificeerd. `sp-sfvl-field`

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value-list name="field-name" quotes="yes/no" commas="yes/no" data="values/count/results" separator="X" sortby="none/values/results" max-items="XX" date-format="date-format-string" gmt="yes/no" language="0/language-id" encoding="html /javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze markering toont een lijst van unieke gebiedswaarden, waardetellingen, of resultaattellingen binnen de volledige resultaatreeks. </p> <p>Deze markering brengt slechts output voor gebieden op die door de parameters <span class="codeph"> sp_sfvl_field CGI in de onderzoeksvraag worden gespecificeerd </span> . De facultatieve "citaten"attributen controleert of de individuele puntenoutput door dubbel-citaten (of enig-citaten, als het coderen=perl) wordt omringd. De standaardwaarde van "citaten"is "ja". De optionele eigenschap "komma's" bepaalt of de afzonderlijke items die worden uitgevoerd, worden gescheiden door komma's. De standaardwaarde van "komma's"is "ja". De optionele eigenschap "data" bepaalt of elke unieke veldwaarde output is (data="values"), de totale telling van elke unieke veldwaarde output is (data="count"), of het aantal resultaten dat elke unieke waarde bevat (data="results") is output. De standaardwaarde van "gegevens" is "waarden". Voor niet-lijst-type gebieden, zijn data="tellingen"en data="resultaten"gelijkwaardig. Het separatorattribuut bepaalt het enige karakter, of afbakening, dat tussen de waarden van de output moet worden opgenomen. Het optionele "sortby"-kenmerk bepaalt de volgorde van de uitvoer. sortby="none" means no specific order, sortby="values" means sort by field values (in oplopende of aflopende volgorde volgens de sorterende eigenschap van het veld), sortby="count" means sort in dalende volgorde van veldwaardetellingen, and sortby="results" means sort in dalende volgorde van het aantal resultaten dat elke waarde bevat. </p> <p>Merk op dat sortby="tellingen"en sortby="resultaten"voor niet-lijst-type gebieden gelijkwaardig zijn. Het optionele kenmerk "max-items" beperkt het aantal items tot uitvoer. De standaardwaarde van "maximum-punten" is -1, zo betekent "output alle punten". </p> <p>Er is een absolute grens van 100 voor maximum-punten. De attributen "date-format", "gmt" en "language" zijn alleen relevant als het inhoudstype van het gespecificeerde veld "date" is. Het attribuut "date-format" neemt een UNIX-tekenreeks met datumnotatie voor de stijl zoals "%A, %B %d, %Y" (voor "Maandag, 25 juli, 2016"). "gmt" staat in gebreke aan "ja" en controleert of het tijdgedeelte van het datumkoord output in GMT ("ja") of de de tijdzone van de rekening ("neen") zou moeten zijn. </p> <p>Zie <a href="../c-appendices/c-templates.md#section_4BBDBBEF2B96414497617CD4B52D96E4" type="section" format="dita" scope="local"> Datumformaatstrings</a>. </p> <p>Het "taal"attribuut controleert de taal en de scèneovereenkomsten van het koord van de outputdatum. "0" (de standaardinstelling) betekent "Account Language gebruiken". Een andere "taal"-waarde wordt geïnterpreteerd als een specifieke taalidentifier, bijvoorbeeld "en_US" betekent "Engels (Verenigde Staten)". Het optionele kenmerk "coderen" bepaalt of de uitvoertekenreekskarakters HTML-code zijn, JavaScript-code, Perl-gecodeerd, URL-code al dan niet gecodeerd voor uitvoer op de resultatenpagina. De standaardwaarde van "het coderen"is "html". </p> <p>Zie <a href="../c-appendices/c-templates.md#section_0490DECC00E34691ADE5A9ED90A6D911" type="section" format="dita" scope="local"> Taalkenmerken</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value-list-count name="field-name" value="field-value" results="yes/no"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze markering toont tellingsinformatie voor een bepaalde onderzoek-gebied-waarde-lijst. Er zijn drie verschillende toepassingen voor deze markering. Als slechts het "naam"attribuut wordt geleverd, output deze markering het aantal unieke waarden voor het genoemde gebied binnen de volledige resultaatreeks. Als de kenmerken "name" en "waarde" beide worden geleverd, wordt met deze tag ofwel de totale telling van de gegeven waarde binnen de gehele resultatenreeks (voor results="no"), ofwel de totale telling van de resultaten die de gegeven waarde in de volledige resultatenreeks bevatten (voor results="yes") uitgevoerd. De standaardwaarde van "resultaten" is "nee". Opmerking: Voor niet-lijst-type gebieden, zijn de resultaten="ja"en de resultaten="nee"gelijkwaardig. De waarde van "resultaten" wordt genegeerd als het kenmerk "waarde" niet wordt geleverd. Deze markering brengt slechts output voor gebieden op die door de <span class="codeph"> </span> sp-sfvl-gebiedCGI parameters in de onderzoeksvraag worden gespecificeerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-field-value-list-count name="field-name" value="field-value"&gt; ... &lt;/search-if-field-value-list-count&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-field-value-list-count name="field-name" value="field-value"&gt; ... &lt;/search-if-not-field-value-list-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze markeringen tonen HTML tussen hen als de gelijkwaardige vraag aan <span class="codeph"> &lt;search-field-value-count name="field-name" value="field-value" waarde&gt; </span> met de bepaalde attributen (of niet) een waarde groter dan nul zou terugkeren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-single-field-value-list-count name="field-name"&gt; ... &lt;/search-if-single-field-value-list-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze markeringen tonen de inhoud tussen hen als de gelijkwaardige vraag aan <span class="codeph"> &lt;search-field-value-count name="field-name" value="field-value"&gt; </span> met de bepaalde attributen (of niet) één enkele waarde zou terugkeren. Dit wordt typisch gebruikt wanneer een rekening facetgroeven gebruikt. Met gezichtsgroeven, wilt u typisch slechts de waarde-groef tonen wanneer de bijbehorende naam-groef één enkel punt heeft. Het doen van deze controle in het vervoermalplaatje is efficiënter dan het doen van het in de presentatielaag. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Lijstcodes van lijst met velden {#section_0717FA09F0FC449CB916883B0500A60E}

De volgende geavanceerde markeringen somt en de waarden van het outputgebied en verwante gegevens van de volledige reeks onderzoeksresultaten op gebruikend een het van een lus voorzien concept. Deze markeringen brengen slechts output voor gebieden op die door de parameters van CGI in de onderzoeksvraag worden gespecificeerd. `sp-sfvl-field`

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;zoek-gebied-waarden name="gebied-naam"sortby="niets/waarden/tellingen/resultaten" max-items="XX"&gt;.. &lt;/search-field-waarden&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze markering leidt tot een lijn voor het opsommen van gebiedswaarden en verwante gegevens voor een bepaald gebied binnen de volledige resultaatreeks. Nest deze markering niet binnen een andere <span class="codeph"> &lt;zoek-gebied-waarden&gt; </span> markering. Het "naam"attribuut specificeert de naam van het gebied dat de op te sommen waarden bevat. Het facultatieve "sortby"attribuut controleert de opsommingsorde: "niets" betekent geen bepaalde orde, "waarden"betekent soort door gebiedswaarden (in stijgende of dalende orde volgens het het Sorteren bezit van het gebied), sortby="tellingen"betekent soort in dalende orde van de tellingen van de gebiedswaarde, en sortby="resultaten"betekent soort in dalende orde van het aantal resultaten die elke waarde bevatten. </p> <p>Merk op dat sortby="tellingen"en sortby="resultaten"voor niet-lijst-type gebieden gelijkwaardig zijn. . Het optionele kenmerk "max-items" beperkt het aantal iteraties tot de gegeven waarde. De standaardwaarde voor "maximum-punten"is -1, wat betekent "opsommen alle waarden". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value date-format="date-format-string-string" encoding="html/javascript/json/perl/url/none" gmt="yes/no" language="0/language-id"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze markering voert de gebiedswaarde voor de huidige &lt;zoek-gebied-waarden&gt; lusjeriteratie uit. Deze markering is slechts geldig binnen een <span class="codeph"> &lt;zoek-gebied-waarden&gt; </span> lijn. De attributen "date-format", "gmt" en "language" zijn alleen relevant als het inhoudstype van de veldnaam die is opgegeven in de bijgevoegde tag &lt;search-field-waardes&gt; "date" is. Het attribuut "date-format" neemt een UNIX-tekenreeks met datumnotatie voor de stijl zoals "%A, %B %d, %Y" (voor "Maandag, 25 juli, 2020"). </p> <p>Zie <a href="../c-appendices/c-templates.md#section_4BBDBBEF2B96414497617CD4B52D96E4" type="section" format="dita" scope="local"> Datumformaatstrings</a>. </p> <p>Het optionele kenmerk "coderen" bepaalt of de uitvoertekenreekskarakters HTML-code zijn, JavaScript-code, Perl-gecodeerd, URL-code al dan niet gecodeerd voor uitvoer op de resultatenpagina. De standaardwaarde van "het coderen"is "niets". Normaal, te hoeven u niet om de het coderen attributen te specificeren. "gmt" staat in gebreke aan "ja" en controleert of het tijdgedeelte van het datumkoord output in GMT ("ja") of de de tijdzone van de rekening ("neen") zou moeten zijn. Het "taal"attribuut controleert de taal en de scèneovereenkomsten van het koord van de outputdatum. "0" (de standaardinstelling) betekent "Account Language gebruiken". Een andere "taal"-waarde wordt geïnterpreteerd als een specifieke taalidentifier, bijvoorbeeld "en_US" betekent "Engels (Verenigde Staten)". </p> <p>Zie <a href="../c-appendices/c-templates.md#section_0490DECC00E34691ADE5A9ED90A6D911" type="section" format="dita" scope="local"> Taalkenmerken</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value-count results="yes/no"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze markeringsoutput de telling verbonden aan de huidige <span class="codeph"> &lt;zoek-gebied-waarden&gt; </span> lijnherhaling. De outputtelling is of het aantal resultaten in de volledige resultaatreeks die de gebiedswaarde (results="ja") bevat, of de totale telling voor de gebiedswaarde in de volledige resultaatreeks. De standaardwaarde van "resultaten" is "nee". </p> <p>Voor niet-lijst-type gebieden, zijn de resultaten="ja"en de resultaten="nee"gelijkwaardig. Deze markering is slechts geldig binnen een <span class="codeph"> &lt;zoek-gebied-waarden&gt; </span> lijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;zoek-gebied-waarde-teller&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze markeringsoutput de rangschikkende teller voor de huidige <span class="codeph"> &lt;zoek-gebied-waarden&gt; </span> lijnherhaling. Deze markering is slechts geldig binnen een <span class="codeph"> &lt;zoek-gebied-waarden&gt; </span> lijn. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Tags voorstellen {#section_C28EB8B4F7DC4E278A0F143BCFEEB1AC}

Suggest verstrekt een gebruikersvriendelijk &quot;Bedoelde u?&quot; dienst voor het voorstellen van alternatieve onderzoekstermijnen. Als een gebruiker een onderzoekstermijn verkeerd heeft gespeld, bijvoorbeeld, stel voor kan de gebruiker helpen resultaten vinden door een correcte spelling voor te stellen. Het systeem kan verwante sleutelwoorden ook voorstellen die een gebruiker kunnen helpen resultaten ontdekken. Wanneer het produceren van suggesties, gebruikt de dienst van de Samenvatting twee woordenboeken: één gebaseerd op de rekeningstaal (ingesteld onder **[!UICONTROL Indexing]** > **[!UICONTROL Words and Languages]** > **[!UICONTROL Language]**), en de andere op basis van de trefwoorden in de accountindex.

>[!NOTE]
>
>De dienst van de Samenvatting werkt niet voor Chinees, Japanner, of Koreaan.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;zoek-als-suggesties&gt; ... &lt;/search-if-suggesties&gt; </span> </p> </td> 
   <td colname="col2"> <p>Omring deze markeringen met om het even welke "Voorstellen"malplaatjemarkeringen, zoals <span class="codeph"> &lt;zoek-suggestie&gt; </span>, <span class="codeph"> &lt;search-suggestie-verbinding&gt; </span>, etc. Als het onderzoek suggesties produceert, verwerkt de output van de onderzoeksmotor en alles tussen de open en dichte markering. Als het onderzoek geen suggesties produceert, is geen van de genestelde inhoud output. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;zoeksuggesties&gt; ... &lt;/search-suggesties&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze markering produceert de "Suggest"lijn, die een lijst van voorgestelde onderzoekstermijnen bevat (bijvoorbeeld, "voorgenomen", "voorgenomen"en "is van plan", voor een vraag oorspronkelijk ingegaan als "bedoeling"). Wanneer het produceren van de lijst van termijnen, herhaalt de onderzoeksmotor om het even welke genestelde markeringen van HTML en/of van het malplaatje tot vijf keer, dat het maximumaantal suggesties is. Gebruik de tellingsattributen om het aantal geproduceerde suggesties (tussen 0-5) te specificeren. </p> <p>De <span class="codeph"> &lt;zoek-suggesties&gt; </span> markering kan veelvoudige tijden op de pagina verschijnen om de lijst van suggesties te herhalen. De veelvoudige suggesties worden gesorteerd volgens het aantal resultaten elke opbrengst. </p> <p>Nest de <span class="codeph"> &lt;search-suggereer&gt; </span> markering tussen open en dichte <span class="codeph"> &lt;search-if-suggesties&gt; </span> markeringen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;zoek-suggestie-verbinding&gt; ... &lt;/search-suggestie-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze markering produceert een verbinding aan de originele onderzoeksvraag gebruikend de geselecteerde voorgestelde onderzoekstermijn in plaats van de originele termijn. De markering keurt en drukt eenvoudig uit om het even welke attributen van HTML zoals klasse, doel, en stijl goed. De markering kan een attribuut URL ook goedkeuren, waarvan de waarde als basis URL voor de geproduceerde verbinding wordt gebruikt. De markeringen kunnen slechts binnen de <span class="codeph"> &lt;zoek-suggesties&gt; </span> lijn verschijnen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;zoek-suggestie-tekst/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze markering drukt uit de momenteel voorgestelde vraagtermijn (bijvoorbeeld, "van plan"voor een vraag die oorspronkelijk als "bedoeling"was ingegaan). De markering heeft geen attributen en kan slechts binnen de <span class="codeph"> &lt;zoek-suggesties&gt; </span> lijn verschijnen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;zoek-als-niet-suggesties&gt; ... &lt;/search-if-not-suggesties&gt; </span> </p> </td> 
   <td colname="col2"> <p>Als het onderzoek geen suggesties produceert, verwerkt de output van de onderzoeksmotor en alles tussen de open en dichte markering. Als het onderzoek suggesties produceert, is geen van de genestelde inhoud output. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if[-not]-first-suggestie&gt; ... &lt;/search-if[-not]-first suggestie&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze voorwaardelijke markeringen omvatten HTML tussen hen die worden gebaseerd op of de voorgestelde termijn de eerste termijn in de lijn van de Samenvatting is. De markeringen moeten tussen open en dichte <span class="codeph"> &lt;zoek-suggestie&gt; </span> markeringen verschijnen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if[-not]-last-suggestie&gt; ... &lt;/search-if[-not]-last-suggestie&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze voorwaardelijke markeringen omvatten HTML tussen hen die worden gebaseerd op of de voorgestelde termijn de laatste termijn in de lijn van de Samenvatting is. De markeringen moeten tussen open en dichte <span class="codeph"> &lt;zoek-suggestie&gt; </span> markeringen verschijnen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;zoek-suggestie-index&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze markering keert de numerieke index van de huidige voorgestelde onderzoekstermijn terug. De markering moet tussen open en dichte <span class="codeph"> &lt;search-suggestie&gt; </span> markeringen verschijnen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;zoek-suggestie-totaal&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze markering keert het totale aantal geproduceerde voorgestelde onderzoekstermijnen terug. De markering moet tussen open en dichte <span class="codeph"> &lt;search-suggestie&gt; </span> markeringen verschijnen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;zoek-suggestie-resultaat-telling&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze markering keert het totale aantal resultaten voor voorgestelde onderzoekstermijn terug. De markering moet tussen open en dichte <span class="codeph"> &lt;search-suggestie&gt; </span> markeringen verschijnen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Sjabloonreekscodes {#section_67E3D529661F4F03A1FF469D9D658CAF}

De volgende markeringsoutput een koord in HTML op dat punt in het malplaatje.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;zoek-body&gt; </span> </p> </td> 
   <td colname="col2"> <p>De het lichaamsmarkering van HTML met om het even welke montages van de Kleur van de Verbinding van het Onderzoek die de BasisSectie van de Blik onder de verbinding van het Malplaatje plaatst. Voeg een achtergrondattribuut aan deze markering aan vertoningsachtergrondbeelden op de resultatenpagina toe. Om het even welke kleurenattributen die aan deze markering worden toegevoegd treden de montages van de Kleur van de Verbinding van het Onderzoek met voeten die de Basissectie van de Blik plaatst. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;zoekkoptekst&gt; </span> </p> </td> 
   <td colname="col2"> <p>HTML voor de Kopbal van de Resultaten van het Onderzoek zoals die in de Basissectie van de Blik onder de verbinding van het Malplaatje wordt geplaatst. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;zoekgegevens&gt; ... &lt;/search-cdata&gt; </span> </p> </td> 
   <td colname="col2"> <p>De onderzoek-gegevens markeringen worden vervangen met hun equivalenten van XML: <span class="codeph"> &lt;search-cdata&gt; </span> wordt vervangen door <span class="codeph"> &lt;![CDATA[" en de &lt;/search-data&gt;- </span> tag worden vervangen door " <span class="codeph"> ]&gt; </span>". Een syntactische parser van XML ontleedt geen informatie tussen de open en dichte markering. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-query query-number="XX" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>De vraag die de bezoeker inging. De geavanceerde, facultatieve "vraag-aantal"attributencontroles die het genummerde vraagkoord output door deze markering is. Bijvoorbeeld, <span class="codeph"> &lt;search-query-number=1&gt; </span> output de inhoud van de <span class="codeph"> sp_q_1 </span> cgi parameter. Als "vraag-aantal"niet wordt gespecificeerd, of als vraag-aantal "0"is, is de belangrijkste vraag ( <span class="codeph"> sp_q </span>) output. Het optionele kenmerk "coderen" bepaalt of de uitvoer HTML-code is, JavaScript-code, Perl-gecodeerd, URL-code al dan niet gecodeerd voor uitvoer op de resultatenpagina. De standaardwaarde van "het coderen"is "html". Normaal, te hoeven u niet om de het coderen attributen te specificeren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;zoek-totaal&gt; </span> </p> </td> 
   <td colname="col2"> <p>De totale telling van resultaten voor deze onderzoek. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;aantal zoekopdrachten&gt; </span> </p> </td> 
   <td colname="col2"> <p>De telling van resultaten die voor deze pagina worden gemeld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;zoekopdrachtlager&gt; </span> </p> </td> 
   <td colname="col2"> <p>Het aantal van het eerste resultaat dat voor deze pagina wordt gemeld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-upper&gt; </span> </p> </td> 
   <td colname="col2"> <p>Het aantal van het laatste resultaat dat voor deze pagina wordt gemeld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-prev-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>Het aantal resultaten dat voor de vorige pagina wordt gemeld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;zoek-volgende-telling&gt; </span> </p> </td> 
   <td colname="col2"> <p>Het aantal resultaten dat voor de volgende pagina wordt gemeld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;zoektijd&gt; </span> </p> </td> 
   <td colname="col2"> <p>De tijd in seconden voor deze zoekopdracht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-logo&gt; </span> </p> </td> 
   <td colname="col2"> <p>HTML voor het logo van het Onderzoek dat voor uw rekening, als om het even welk wordt gevormd. Dit logo is de afbeelding die krediet biedt voor zoeken/verkopen op de site </p> <p>De meeste accounts hebben momenteel geen gekoppeld zoeklogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-collection all="name"&gt; </span> </p> </td> 
   <td colname="col2"> <p>De inzameling van de resultaten voor dit onderzoek. Het facultatieve "alle"attribuut wordt gebruikt om de naam van de inzameling te geven die de volledige website vertegenwoordigt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;zoekformulier&gt; ...&lt;/zoekformulier&gt; </span> </p> </td> 
   <td colname="col2"> <p>De tussenvoegsels beginnen en beëindigen vormmarkeringen. Neemt de methode en actiekenmerken in de begin vormmarkering op. Accepteert extra attributen met inbegrip van dir="RTL"attributen voor taal evenals op JavaScript betrekking hebbende "naam"en "opSubmit"attributen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;account voor zoekopdrachten-invoer&gt; </span> </p> </td> 
   <td colname="col2"> <p>Neemt een markering van de vorminput op die uw rekeningsaantal specificeert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input-gallery&gt; </span> </p> </td> 
   <td colname="col2"> <p>Neemt een markering van de vorminput op die het galerijaantal specificeert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input-query query-number="XX"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Neemt een markering van de vorminput op die het vraagkoord specificeert. De geavanceerde, facultatieve "vraag-aantal"attributencontroles die de genummerde vraag voor de markering van de vorminput worden gebruikt. Bijvoorbeeld, <span class="codeph"> &lt;search-input-query vraag-number=1&gt; </span> output een markering van de vorminput voor de <span class="codeph"> sp_q_1 </span> vraag. Als "vraag-aantal"niet wordt gespecificeerd, of als "vraag-aantal""0"is, wordt een inputmarkering voor de belangrijkste <span class="codeph"> sp_q vraag </span> opgenomen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input-collecties all="name"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Neemt een vorm uitgezochte markering en bijbehorende HTML op die het menu van de inzamelingsselectie tonen. Het facultatieve "alle"attribuut wordt gebruikt om de naam van de inzameling te geven die de volledige website vertegenwoordigt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>19 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;zoek-lt&gt; </span> </p> </td> 
   <td colname="col2"> <p>Neemt de output van één van de het malplaatjemarkeringen van het Onderzoek binnen andere markeringen van HTML of van het malplaatje op de resultatenpagina op. <span class="codeph"> &lt;search-lt&gt; </span> neemt minder dan karakter op. Het gebruik van <span class="codeph"> &lt;search-lt&gt; </span> en <span class="codeph"> &lt;search-gt&gt; </span> verstrekt een manier om de definitie van een markering te ontsnappen zodat u de het malplaatjemarkeringen van het Onderzoek als attributenwaarden kunt gebruiken. Wanneer het malplaatje in antwoord op een onderzoek wordt teruggegeven, vervangt een minder dan teken (&lt;) de <span class="codeph"> &lt;search-lt&gt; </span> markering. Bijvoorbeeld, <span class="codeph"> &lt;search-link&gt; </span> is gelijkwaardig aan <span class="codeph"> &lt;search-lt&gt;a href="&lt;search-url&gt;"&lt;search-gt&gt; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>20 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;zoek-gt&gt; </span> </p> </td> 
   <td colname="col2"> <p>Neemt de output van één van de het malplaatjemarkeringen van het Onderzoek binnen andere markeringen van HTML of van het malplaatje op de resultatenpagina op. <span class="codeph"> &lt;search-gt&gt; </span> neemt een groter dan karakter op. Het gebruik van <span class="codeph"> &lt;search-lt&gt; </span> en <span class="codeph"> &lt;search-gt&gt; </span> verstrekt een manier om de definitie van een markering te ontsnappen zodat u andere malplaatjemarkeringen als attributenwaarden kunt gebruiken. Wanneer het malplaatje in antwoord op een onderzoek wordt teruggegeven, vervangt een groter-dan teken (&gt;) de <span class="codeph"> &lt;zoek-gt&gt; </span> markering. Bijvoorbeeld, <span class="codeph"> &lt;search-link&gt; </span> is gelijkwaardig aan <span class="codeph"> &lt;search-lt&gt;a href="&lt;search-url&gt;"&lt;search-gt&gt; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>21 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-param name="param-name" length="XX" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Keert de waarde van de cgi parameter genoemd terug "param-name"van het huidige onderzoeksverzoek. Het optionele kenmerk "coderen" bepaalt of de uitvoer HTML-code is, JavaScript-code, Perl-gecodeerd, URL-code al dan niet gecodeerd voor uitvoer op de resultatenpagina. De standaardwaarde van "het coderen"is "html". Normaal, te hoeven u niet om de het coderen attributen te specificeren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>22 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW for S&P 8.17.0 release on October 30 2014--> <span class="codeph"> &lt;search-trace encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> 
    <!--<p>This global core search template tag outputs a representation of the submitted core search query, including any "fuzzy-search" query term expansions that happen by way of synonyms, sound-alikes, and so forth. </p>--> <p>Het <span class="codeph"> het coderen </span> attribuut is facultatief; de standaardwaarde is <span class="codeph"> json </span>. </p> <p> <p>Opmerking:  Deze markering heeft slechts output als <span class="codeph"> sp_trace=1 </span> met de de vraagparameters van het kernonderzoek wordt gespecificeerd. </p> </p> <p>Zie rij 48 in de lijst die in de parameters <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" format="dita" scope="local"> wordt gevonden van het Onderzoek van de</a>Achtergrond CGI. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Sjabloonankerkoppelingtags {#section_3A51D27616C541E2B818CC52B2B856BA}

Het volgende is markeringen die een ankerverbinding veroorzaken om HTML tussen hen te omringen. Wanneer geklikt, verzoekt de ankerverbinding een andere pagina van resultaten aan vertoning. De facultatieve attributen &quot;telling&quot;verzoekt om dat vele resultaten op de pagina aan vertoning. Als gespecificeerd niet, wordt de telling gevraagd op de huidige pagina gebruikt. De geavanceerde, facultatieve &quot;URL&quot;attributen controleert het domein waaraan de bijbehorende verbinding wordt geleid. Door gebrek is het domein `https://search.atomz.com/search/`, maar u kunt dit veranderen gebruikend de attributen URL.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;zoek-volgende URL="https://search.yourdomain.com/search/"&gt; ... &lt;/search-next&gt; </span> </p> <p> <span class="codeph"> &lt;search-prev URL="https://search.yourdomain.com/search/"&gt; ... &lt;/search-prev&gt; </span> </p> </td> 
   <td colname="col2"> <p>Toont de volgende of vorige pagina van de resultaten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-sort-by-date URL="https://search.yourdomain.com/search/"&gt; ... &lt;/search-by-date&gt; </span> </p> <p> <span class="codeph"> &lt;search-by-score URL="https://search.yourdomain.com/search/"&gt; ... &lt;/search-by-score&gt; </span> </p> </td> 
   <td colname="col2"> <p>Sorteert de resultaten door datum of door relevantie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-show-vat URL="https://search.yourdomain.com/search/"&gt;... &lt;/search-show-samenvattingen&gt; </span> </p> <p> <span class="codeph"> &lt;zoek-huid-samenvattingen URL="https://search.yourdomain.com/search/"&gt; ... &lt;/search-hide-samenvattingen&gt; </span> </p> </td> 
   <td colname="col2"> <p>Toont of verbergt de samenvattingen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Voorwaardelijke tags voor template {#section_18D9BC66DE484881932FD2F7EA9D170D}

De markeringen die u voorwaardelijk HTML tussen hen laten omvatten.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-results&gt; ... &lt;/search-if-resultaten&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-results&gt; ...&lt;/search-if-not-results&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze markeringen omvatten HTML als de huidige pagina om het even welke (of geen) onderzoeksresultaten bevat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-prev-count&gt; ... &lt;/search-if-prev-count&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-prev-count&gt; ... &lt;/search-if-not-prev-count&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-next-count&gt; ... &lt;/search-if-next-count&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-next-count&gt; ... &lt;/search-if-not-next-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze markeringen omvatten HTML als de vorige pagina of de volgende pagina om het even welke (of niets) resultaten verbonden aan het hebben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-sort-by-score&gt; ... &lt;/search-if-sort-by-score&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-sort-by-score&gt; ... &lt;/search-if-not-sort-by-score&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-sort-by-date&gt; ... &lt;/search-if-sort-by-date&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-sort-by-date&gt; ... &lt;/search-if-not-sort-by-date&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze markeringen omvatten HTML als de huidige pagina, of niet, gesorteerd op relevantie of door datum is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-show-vat&gt; ... &lt;/search-if-show-samenvattingen&gt; </span> </p> <p> <span class="codeph"> &lt;zoek-als-huid-samenvattingen&gt; ... &lt;/search-if-hide-samenvattingen&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze markeringen omvatten HTML als de huidige pagina samenvattingen toont of verbergt. U kunt deze markeringen gebruiken om het even welk gedeelte van het onderzoeksresultaat te omvatten of uit te sluiten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-input-collecties&gt; ... &lt;/search-if-input-verzamelingen&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-input-collections&gt; ... &lt;/search-if-not-input-collecties&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze markeringen omvatten HTML als een inzameling in de generatie van onderzoeksresultaten voor de huidige pagina werd gespecificeerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-advanced&gt; ... &lt;/search-if-advanced&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-advanced&gt; ... &lt;/search-if-not-advanced&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze markeringen omvatten HTML als de <span class="codeph"> sp_advanced=1 </span> CGI parameter voor de onderzoeksvraag werd gespecificeerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-bad-param name="parameter-naam"&gt; ... &lt;/search-if-bad-param&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-bad-param name="parameter-name"&gt; ... &lt;/search-if-not-bad-param&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze markeringen omvatten of sluiten HTML tussen hen uit als de bepaalde parameter, of niet, ongeldig is. </p> <p>Momenteel slechts wordt de <span class="codeph"> sp_q_location [_#] </span> parameter gesteund. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-param name="param-name" value="param-value"&gt; ... &lt;/search-if-param&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-param name="param-name"value="param-value"&gt; ... &lt;/search-if-not-param&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze geavanceerde markeringen omvatten HTML tussen hen gebaseerd op of de parameter van CGI die in het "naam"attribuut wordt gespecificeerd de waarde heeft die in de "waarde"attributen wordt gespecificeerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-sort-by-field name="field-name"&gt; ... &lt;/search-if-sort-by-field&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-sort-by-field name="field-name"&gt; ... &lt;/search-if-not-sort-by-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze geavanceerde markeringen omvatten HTML tussen hen als de huidige pagina, of niet, gesorteerd door de bepaalde gebied-naam is. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Sjabloonformulierbesturingscodes {#section_45AFC414ACA74825B72FEAA8456F8DD2}

De markeringen die u de standaardselectiestaat voor controledozen, radioknopen, en lijstvakjes binnen een `<form>` op het onderzoeksmalplaatje laten controleren.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;zoek-invoer&gt; </span> </p> </td> 
   <td colname="col2"> <p>Gebruikt in een malplaatje in plaats van een <span class="codeph"> &lt;input&gt; </span> markering. Wanneer de markering aan browser wordt geschreven, <span class="codeph"> vervangt de woordinput </span> onderzoek-input <span class="codeph"> </span> en alle andere informatie in de markering is output zoals-is. Bovendien als de <span class="codeph"> naam die in de markering wordt </span> gespecificeerd als parameter van CGI vermeld is en als de <span class="codeph"> waarde die in de markering wordt </span> gespecificeerd de waarde voor die parameter van CGI is, dan wordt het <span class="codeph"> </span> gecontroleerde woord toegevoegd aan het eind van de markering. Op deze manier, kunt u de standaardradioknoop of checkbox staat in uw onderzoeksresultaat automatisch maken het zelfde als de huidige vraag. </p> <p>Bijvoorbeeld, zou de code van HTML voor een controledoos als het volgende kunnen kijken: </p> <p> <span class="codeph"> &lt;invoertype=checkbox name="sp_w" value="exact"&gt;Geen overeenkomend geluid </span> </p> <p>De overeenkomstige malplaatjecode voor dat checkbox is het volgende: </p> <p> <span class="codeph"> &lt;search-input type=checkbox name="sp_w" value="exact"&gt;Geen overeenkomend geluid </span> </p> <p>Als het CGI parameterkoord voor de vraag <span class="codeph"> sp_w=exact bevat </span>, dan kijkt de markering die aan browser met de onderzoeksresultaten wordt geschreven als het volgende (het <span class="codeph"> gecontroleerde woord </span> wordt opgenomen aan het eind van de markering): </p> <p> <span class="codeph"> &lt;invoertype=checkbox name="sp_w" value="exact" ingeschakeld&gt;Geen overeenkomend geluid </span> </p> <p>Als het CGI parameterkoord voor de vraag niet <span class="codeph"> sp_w=exact bevat </span>, dan kijkt de markering die aan browser met de onderzoeksresultaten wordt geschreven als het volgende (het <span class="codeph"> gecontroleerde woord </span> is niet vermeld in de markering): </p> <p> <span class="codeph"> &lt;invoertype=checkbox name="sp_w" value="exact"&gt;Geen overeenkomend geluid </span> </p> <p>De <span class="codeph"> </span> &lt;search-input&gt; markering is nuttig om controledozen en radioknopen in uw onderzoeksmalplaatje te zetten. Als u controledozen of radioknopen hebt die u aan <span class="codeph"> &lt;form&gt; </span> in uw onderzoeksmalplaatje wilt toevoegen, gebruik <span class="codeph"> &lt;search-input...&gt; </span> in plaats van <span class="codeph"> &lt;input..&gt; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-select&gt; ... &lt;/search-select&gt; </span> </p> <p> <span class="codeph"> &lt;zoek-optie&gt; ... &lt;/search-optie&gt; </span> </p> </td> 
   <td colname="col2"> <p>De drop-down lijstvakjes in een <span class="codeph"> &lt;form&gt; </span> markering worden begonnen met een <span class="codeph"> &lt;select&gt; </span> markering en met een <span class="codeph"> &lt;/select&gt; </span> markering gebeëindigd. De <span class="codeph"> naam </span> voor de bijbehorende parameter van CGI is vermeld binnen de <span class="codeph"> &lt;select&gt; </span> markering. Na de <span class="codeph"> &lt;select&gt; </span> markering is een lijst van <span class="codeph"> &lt;option&gt; </span> markeringen die de waarden specificeren om binnen de lijstdoos te tonen. </p> <p>De <span class="codeph"> &lt;search-select&gt; </span>, <span class="codeph"> &lt;/search-select&gt; </span>, <span class="codeph"> &lt;search-option&gt; </span>, en <span class="codeph"> &lt;/search-option&gt; </span> tags bieden een vergelijkbare functionaliteit als de <span class="codeph"> &lt;search-input&gt; </span> tag. Namelijk wordt het <span class="codeph"> geselecteerde woord </span> automatisch toegevoegd aan het eind van de <span class="codeph"> &lt;option&gt; </span> markering die naar browser wordt verzonden als de <span class="codeph"> naam </span> in de <span class="codeph"> &lt;search-select&gt; </span> markering als parameter van CGI vermeld is en als de <span class="codeph"> waarde </span> <span class="codeph"> </span> <span class="codeph"> </span> van die CGI parameter als waarde  waarde in een bepaalde &lt;search-option&gt;  markering vermeld is. Op deze manier, kunt u de keus van het standaardlijstvakje in uw onderzoeksresultaat automatisch maken het zelfde als de huidige vraag. </p> <p>Bijvoorbeeld, kijkt een typische lijstvakje als het volgende: </p> <p> <code class="syntax html"> &lt;select&nbsp;name="sp_x"&nbsp;size=1&gt; 
      &lt;option&nbsp;value="any"&nbsp;selected&gt;Anywhere&lt;/option&gt; 
      &lt;option&nbsp;value="title"&gt;Title&lt;/option&gt; 
      &lt;option&nbsp;value="desc"&gt;Description&lt;/option&gt; 
      &lt;option&nbsp;value="keys"&gt;Keywords&lt;/option&gt; 
      &lt;option&nbsp;value="body"&gt;Body&lt;/option&gt; 
      &lt;option&nbsp;value="alt"&gt;Alternate&nbsp;text&lt;/option&gt; 
      &lt;option&nbsp;value="url"&gt;URL&lt;/option&gt; 
      &lt;option&nbsp;value="target"&gt;Target&lt;/option&gt; 
      &lt;/select&gt; </code> </p> <p>De overeenkomstige malplaatjecode voor dat lijstvakje is het volgende: </p> <p> <code class="syntax html"> &lt;search-select&nbsp;name="sp_x"&nbsp;size=1&gt; 
      &lt;search-option&nbsp;value="any"&gt;Anywhere&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="title"&gt;Title&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="desc"&gt;Description&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="keys"&gt;Keywords&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="body"&gt;Body&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="alt"&gt;Alternate&nbsp;text&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="url"&gt;URL&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="target"&gt;Target&lt;/search-option&gt; 
      &lt;/search-select&gt; </code> </p> <p>Als u lijstvakjes hebt die u aan <span class="codeph"> &lt;form&gt; </span> in uw onderzoeksmalplaatje wilt toevoegen, gebruik <span class="codeph"> &lt;search-select...&gt; </span> in plaats van <span class="codeph"> &lt;select...&gt; </span>, <span class="codeph"> &lt;/search-select&gt; </span> in plaats van <span class="codeph"> &lt;/select&gt; </span><span class="codeph"> </span> <span class="codeph"> </span><span class="codeph"> </span> <span class="codeph"> </span>&lt;search-option....&gt; in plaats van .............................................................................................................................................................................. optie&gt; </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-sort-by-field name="field-name" count="XX"&gt; ... &lt;/search-by-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze geavanceerde markeringen leiden tot een ankerverbinding rond HTML tussen hen. Wanneer dit anker wordt geklikt, wordt een pagina van resultaten getoond die op het bepaalde gebied worden gesorteerd. Het facultatieve <span class="codeph"> tellingsattribuut </span> specificeert het aantal resultaten aan vertoning op de resultaatpagina. Als de <span class="codeph"> telling </span> wordt weggelaten, wordt de telling die op de huidige pagina wordt gebruikt gebruikt gebruikt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Datumformaatstrings {#section_4BBDBBEF2B96414497617CD4B52D96E4}

U kunt de volgende omzettingsspecificaties in de koorden van het datumformaat gebruiken:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Datumindelingstekenreeks </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>%A </p> </td> 
   <td colname="col2"> <p> Past de nationale vertegenwoordiging van de volledige weekdagnaam aan, bijvoorbeeld, "Maandag." De instelling in <span class="uicontrol"> Taalkunde </span> &gt; <span class="uicontrol"> Woorden &amp; Talen </span> &gt; <span class="uicontrol"> Taal </span> bepaalt de nationale vertegenwoordiging. </p> <p>Zie <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> over woorden en taal</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%a </p> </td> 
   <td colname="col2"> <p> Komt overeen met de nationale afbeelding van de afgekorte weekdagnaam, waarbij de afkorting de eerste drie tekens is, bijvoorbeeld "Mon". De instelling in <span class="uicontrol"> Taalkunde </span> &gt; <span class="uicontrol"> Woorden &amp; Talen </span> &gt; <span class="uicontrol"> Taal </span> bepaalt de nationale vertegenwoordiging. </p> <p>Zie <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> over woorden en taal</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%B </p> </td> 
   <td colname="col2"> <p> Komt overeen met de nationale vertegenwoordiging van de volledige naam van de maand, bijvoorbeeld "June". De instelling in <span class="uicontrol"> Taalkunde </span> &gt; <span class="uicontrol"> Woorden &amp; Talen </span> &gt; <span class="uicontrol"> Taal </span> bepaalt de nationale vertegenwoordiging. </p> <p>Zie <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> over woorden en taal</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%b </p> </td> 
   <td colname="col2"> <p> Komt overeen met de nationale afbeelding van de afgekorte naam van de maand, waarbij de afkorting de eerste drie tekens is, bijvoorbeeld "Jun". De instelling in <span class="uicontrol"> Taalkunde </span> &gt; <span class="uicontrol"> Woorden &amp; Talen </span> &gt; <span class="uicontrol"> Taal </span> bepaalt de nationale vertegenwoordiging. </p> <p>Zie <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> over woorden en taal</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%D </p> </td> 
   <td colname="col2"> <p>Equivalent aan "%m/%d/%y", bijvoorbeeld "07/25/13". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%d </p> </td> 
   <td colname="col2"> <p> Komt de dag van de maand als decimaal aantal (01-31) overeen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%e </p> </td> 
   <td colname="col2"> <p> Komt de dag van maand als decimaal aantal (1-31) overeen. Een lege gaat enige cijfers vooraf. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%H </p> </td> 
   <td colname="col2"> <p> Past de klok van 24 uur als decimaal aantal (00-23) aan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%h </p> </td> 
   <td colname="col2"> <p> Komt overeen met de nationale afbeelding van de afgekorte naam van de maand, waarbij de afkorting de eerste drie tekens is, bijvoorbeeld "Jun" (hetzelfde als %b). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%I </p> </td> 
   <td colname="col2"> <p> Past de klok van 12 uur als decimaal aantal (01-12) aan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%j </p> </td> 
   <td colname="col2"> <p> Komt overeen met de dag van het jaar als decimaal getal (001-366). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%k </p> </td> 
   <td colname="col2"> <p> Past de (24 uurklok als decimaal aantal (0-23) aan. Een lege gaat enige cijfers vooraf. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%l </p> </td> 
   <td colname="col2"> <p> Past de klok van 12 uur als decimaal aantal (1-12) aan. Een lege gaat enige cijfers vooraf. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%M </p> </td> 
   <td colname="col2"> <p> Past de minuut als decimaal aantal (00-59) aan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%m </p> </td> 
   <td colname="col2"> <p> Komt overeen met de maand als decimaal (01-12). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%p </p> </td> 
   <td colname="col2"> <p> Komt overeen met de nationale vertegenwoordiging van "ante meridiem" of "post meridiem", al naargelang het geval, bijvoorbeeld "PM". De instelling in <span class="uicontrol"> Taalkunde </span> &gt; <span class="uicontrol"> Woorden &amp; Talen </span> &gt; <span class="uicontrol"> Taal </span> bepaalt de nationale vertegenwoordiging. </p> <p>Zie <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> over woorden en taal</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%R </p> </td> 
   <td colname="col2"> <p>Equivalent aan "%H:%M", bijvoorbeeld, "13:23". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%r </p> </td> 
   <td colname="col2"> <p>Equivalent aan "%I:%M:%S %p", bijvoorbeeld "01:23:45 PM". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%S </p> </td> 
   <td colname="col2"> <p> Past de tweede als decimaal aantal (00-60) aan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%T </p> </td> 
   <td colname="col2"> <p>Equivalent aan "%H:%M:%S", bijvoorbeeld, "13:26:47". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%U </p> </td> 
   <td colname="col2"> <p> Komt overeen met het weekaantal van het jaar (zondag als de eerste dag van de week) als decimaal getal (00-53). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%v </p> </td> 
   <td colname="col2"> <p>Equivalent aan "%e-%b-%Y", bijvoorbeeld, "25-jul-2013". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%Y </p> </td> 
   <td colname="col2"> <p> Past het jaar met eeuw als decimaal aantal aan, bijvoorbeeld, "2013". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%y </p> </td> 
   <td colname="col2"> <p> Komt overeen met het jaar zonder eeuw als decimaal (00-99). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%Z </p> </td> 
   <td colname="col2"> <p> Komt overeen met de naam van de tijdzone. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%% </p> </td> 
   <td colname="col2"> <p> Komt overeen met "%". </p> </td> 
  </tr> 
 </tbody> 
</table>

## Taalidentificatie {#section_0490DECC00E34691ADE5A9ED90A6D911}

De volgende lijst bevat de taalherkenningstekens voor elke gesteunde taal. U kunt deze herkenningstekens als waarden voor de facultatieve &quot;taal&quot;attributen in de volgende malplaatjemarkeringen gebruiken:

* `search-date` en `search-display-field`.

   Zie [Resultaatreeksen](../c-appendices/c-templates.md#section_80D68334E8D04A33937A6E58ABAAA320).

* `search-field-value-list` Zie [de markeringen](../c-appendices/c-templates.md#section_D3298B5F976447DBA0032B883DCC91B1)van de waardelijst van het Gebied.

* `search-field-value` Zie [de lijnmarkeringen](../c-appendices/c-templates.md#section_0717FA09F0FC449CB916883B0500A60E)van de waardelijst van het Gebied.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Taal </p> </th> 
   <th colname="col2" class="entry"> <p>Taalidentificatiecode </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Bulgaars (Bulgarije) </p> </td> 
   <td colname="col2"> <p> bg_BG </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chinees (China) </p> </td> 
   <td colname="col2"> <p> zh_CN </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chinees (Hongkong) </p> </td> 
   <td colname="col2"> <p> zh_HK </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chinees (Singapore) </p> </td> 
   <td colname="col2"> <p>zh_SG </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chinees (Taiwan) </p> </td> 
   <td colname="col2"> <p> zh_TW </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tsjechië (Tsjechië) </p> </td> 
   <td colname="col2"> <p> cs_CZ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Deens (Denemarken) </p> </td> 
   <td colname="col2"> <p> da_DK </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Nederlands (België) </p> </td> 
   <td colname="col2"> <p> nl_BE </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Nederlands (Nederland) </p> </td> 
   <td colname="col2"> <p> nl_NL </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Engels (Australië) </p> </td> 
   <td colname="col2"> <p> en_AU </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Engels (Canada) </p> </td> 
   <td colname="col2"> <p> en_CA </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Engels (Groot-Brittannië) </p> </td> 
   <td colname="col2"> <p> NL_GB </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Engels (Verenigde Staten) </p> </td> 
   <td colname="col2"> <p> en_US </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Frans (België) </p> </td> 
   <td colname="col2"> <p> fr_BE </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Frans (Canada) </p> </td> 
   <td colname="col2"> <p>fr_CA </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Fins (Finland) </p> </td> 
   <td colname="col2"> <p> fi_FI </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Frans (Frankrijk) </p> </td> 
   <td colname="col2"> <p> fr_FR </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Frans (Zwitserland) </p> </td> 
   <td colname="col2"> <p> fr_CH </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Duits (Oostenrijk) </p> </td> 
   <td colname="col2"> <p> de_AT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Duits (Duitsland) </p> </td> 
   <td colname="col2"> <p> de_DE </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Duits (Zwitserland) </p> </td> 
   <td colname="col2"> <p> de_CH </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Grieks (Griekenland) </p> </td> 
   <td colname="col2"> <p> el_GR </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Irish Gaelic (Ierland) </p> </td> 
   <td colname="col2"> <p> ga_IE </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Italiaans (Italië) </p> </td> 
   <td colname="col2"> <p> IT_IT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Japans (Japan) </p> </td> 
   <td colname="col2"> <p> ja_JP </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Koreaans (Korea) </p> </td> 
   <td colname="col2"> <p> ko_KR </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Noors (Noorwegen) </p> </td> 
   <td colname="col2"> <p> neen_NO </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pools (Polen) </p> </td> 
   <td colname="col2"> <p> pl_PL </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Portugees (Brazilië) </p> </td> 
   <td colname="col2"> <p> pt_BR </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Portugees (Portugal) </p> </td> 
   <td colname="col2"> <p> pt_PT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Russisch (voormalige Sovjetunie) </p> </td> 
   <td colname="col2"> <p> ru_SU </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Slowaaks (Slowakije) </p> </td> 
   <td colname="col2"> <p> sk_SK </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Slowaaks (Slovenië) </p> </td> 
   <td colname="col2"> <p>sl_SI </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Spaans (Mexico) </p> </td> 
   <td colname="col2"> <p> es_MX </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Spaans (Spanje) </p> </td> 
   <td colname="col2"> <p> es_ES </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Zweeds (Zweden) </p> </td> 
   <td colname="col2"> <p> sv_SE </p> </td> 
  </tr> 
 </tbody> 
</table>

## Het specificeren van de inhoud-type HTTP- kopbal {#section_AEED823E9938448A9EDB2F286D9CFD90}

U kunt de tevreden-Type HTTP- reactiekopbal specificeren door de volgende markering te gebruiken:

`<search-content-type-header [content="MIME-type"] [charset="charset-name"]>`

De kenmerken `content` en `charset` kenmerken zijn optioneel. Deze markering zou zo vroeg mogelijk in het malplaatje moeten verschijnen. Het wordt ook geadviseerd dat het vóór of `<search-html-meta-charset>` `<search-xml-decl>`of verschijnt, omdat het het gedrag van die markeringen beïnvloedt.

Als u niet de `content` attributen specificeert, dan blijft de waarde van `MIME-type` gebreken aan de waarde die in **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]** wordt geplaatst. Als u een `content` attribuut specificeert, wordt het gebruikt als standaardattribuut `content` voor de `<search-html-meta-charset>` markering.

Als u niet het `charset` attribuut specificeert, dan wordt geen `charset` waarde geschreven aan de `content-type` kopbal.

Als u `charset="1"` dan specificeert is de daadwerkelijke waarde voor de waarde van de parameter van `charset-name` `sp_f` CGI. Als geen parameter van `sp_f` `charset-name` CGI met het onderzoek wordt voorgelegd, dan wordt de daadwerkelijke waarde voor gelezen van uw rekeningsmontages. U kunt de tekenset bekijken of wijzigen die aan uw account is gekoppeld onder **[!UICONTROL Settings]** > **[!UICONTROL My Profile]** > **[!UICONTROL Personal Information]** > **[!UICONTROL Character Encoding]**.

Zie Je persoonlijke gebruikersgegevens [configureren](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6).

U kunt een specifieke karakter kiezen - vastgestelde naam door het aan te bieden als `charset` waarde, als `charset="iso-8859-1"` of `charset="Shift-JIS"`.

Als u een `charset` attribuut specificeert, dan wordt het gebruikt als standaardattribuut `charset` voor de `<search-html-meta-charset>` en `<search-xml-decl>` markeringen, evenals het zijn output aan de `content-type` kopbal.

## Het specificeren van een karakter dat in een malplaatje van HTML wordt geplaatst {#section_E0D1816ABB5846BEBE9C26D5980CCBE6}

De standaardmalplaatjes van het HTML- onderzoeksresultaat specificeren de karakterreeks verbonden aan de huidige rekening via de volgende markering:

`<search-html-meta-charset [content="MIME-type"] [charset="charset-name"]>`

De inhoud en de charsetattributen zijn facultatief. Deze markering moet in de `<head>` sectie van HTML van het malplaatje verschijnen. Deze markering resulteert in de volgende markering op de HTML- pagina die van het malplaatje wordt geproduceerd:

`<meta http-equiv="content-type" content="MIME-type; charset=charset-name">`

Als u niet de inhoudsattributen specificeert, dan blijft de daadwerkelijke waarde van `MIME-type` gebreken aan één van twee waarden. Als de `<search-content-type-header>` markering een `content` attribuut specificeerde, dan wordt die waarde gebruikt. Anders, is de gebruikte waarde één reeks in **[!UICONTROL Templates]** > **[!UICONTROL Settings]** > **[!UICONTROL Content Type]** tabel.

Als u niet de `charset` attributen specificeert, dan blijft de daadwerkelijke waarde van `charset-name` gebreken aan één van twee waarden. Als de `<search-content-type-header>` markering een `charset` attribuut specificeerde, dan wordt die waarde gebruikt. Anders, wordt de daadwerkelijke waarde voor gelezen van uw rekeningsmontages. `charset-name` U kunt de tekenset bekijken of wijzigen die aan uw account is gekoppeld onder **[!UICONTROL Settings]** > **[!UICONTROL My Profile]** > **[!UICONTROL Personal Information]** > **[!UICONTROL Character Encoding]**.

Zie Je persoonlijke gebruikersgegevens [configureren](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6).

Als u `charset="1"` dan specificeert is de daadwerkelijke waarde voor de waarde van de parameter van `charset-name` `sp_f` CGI. Als geen parameter van `sp_f` CGI met het onderzoek wordt voorgelegd, dan is de daadwerkelijke waarde voor `charset-name` of de waarde die in de `<search-content-type-header>` markering wordt geplaatst als het werd gespecificeerd, of de waarde die in uw rekeningsmontages wordt geplaatst.

U kunt een specifieke karakter specificeren - vastgestelde naam, zoals in `charset="charset-name"`. For example, `charset="iso-8859-1"` or `charset="Shift-JIS"`.

De `<search-html-meta-charset>` tag is optioneel. Als u het verwijdert, browser veronderstelt de standaardwaarden voor, `content-type`die het volgende is: `content="text/html; charset=ISO-8859-1"`. U kunt ook verkiezen om de `<search-html-meta-charset>` markering met uw eigen `http-equiv` markering te vervangen.

## Het specificeren van een karakter dat in een malplaatje van XML wordt geplaatst {#section_17DC31CDCC104F5F8081466B41A96E9D}

Het standaardmalplaatje van het het onderzoeksresultaat van XML specificeert de karakterreeks verbonden aan de huidige rekening als volgende markering:

`<search-xml-decl [charset="charset-name"]>`

Het `charset` kenmerk is optioneel. Deze markering moet bij de bovenkant van het malplaatje, maar na om het even welke `<search-content-type-header>` markering verschijnen. Deze markering resulteert in de volgende markering op het document van XML dat van het malplaatje wordt geproduceerd:

`<?xml version="1.0" encoding="charset-name" standalone="yes" ?>`

Als u niet specificeert `charset`, dan blijft de daadwerkelijke waarde van `charset-name` gebreken aan één van twee waarden. Als `<search-content-type-header>` gespecificeerd een `charset` attribuut, dan wordt die waarde gebruikt. Anders, wordt de daadwerkelijke waarde voor gelezen van uw rekeningsmontages. `charset-name` U kunt de tekenset bekijken of wijzigen die aan uw account is gekoppeld onder **[!UICONTROL Settings]** > **[!UICONTROL My Profile]** > **[!UICONTROL Personal Information]** > **[!UICONTROL Character Encoding]**.

Zie Je persoonlijke gebruikersgegevens [configureren](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6).

Als u `charset="1"` dan specificeert is de daadwerkelijke waarde voor de waarde van de parameter van `charset-name` `sp_f` CGI. Als geen parameter van `sp_f` CGI met het onderzoek wordt voorgelegd, dan is de daadwerkelijke waarde voor `charset-name` of de waarde die in de `<search-content-type-header>` markering wordt geplaatst als het werd gespecificeerd, of de waarde die in uw rekeningsmontages wordt geplaatst.

U kunt een specifieke karakter specificeren - vastgestelde naam, zoals in, `charset="charset-name"`als u dit wenst. Bijvoorbeeld, `charset="iso-8859-1" or charset="Shift-JIS"`.

U kunt verkiezen om de `<search-xml-decl>` markering met uw eigen `?xml` markering te vervangen.

## Inclusief een zoekopdrachtsjabloon in een andere {#section_7D1FCD3D9E2340C291E354C9720E8BC0}

Om één onderzoeksmalplaatje in een andere te omvatten, gebruik de `<search-include>` markering, plaatsend de dossierattributen aan de naam van het malplaatjedossier dat u zoals in het volgende voorbeeld wilt omvatten:

`<search-include file="seo/seo_search_title.tpl" />`

De segmenten van het het onderzoeksmalplaatje van SEO zijn in `seo/` subfolder en de normale onderzoeksmalplaatjes zijn in `templates/` subfolder. Slechts .tpl de dossiers zijn zinvol om in deze context te omvatten.

## Meerdere transportsjablonen beheren voor uw website {#reference_12AAB3B9F4C74C11956F1DBA95714C2F}

U kunt de verschijning van onderzoeksresultaten over uw website controleren door verschillende malplaatjes van het onderzoeksvervoer voor elk gebied te gebruiken.

<!-- 

r_managing_multiple_templates.xml

 -->

Om dit soort onderzoeksfunctionaliteit te verwezenlijken, kunt u uw vervoermalplaatjes in plaatsonderzoek/merchandising beheren. Of, u kunt uw vervoermalplaatjes in Publish beheren. Als plaatsonderzoek/merchandising, publiceer laat u uitgeven, voorproef, en de veelvoudige malplaatjes van het onderzoeksvervoer publiceren.

Aan opstelling gebruikt uw onderzoeksvormen om een specifiek vervoermalplaatje (buiten het gebrek) te gebruiken, de `sp_t` vraagparameter. Bijvoorbeeld, veronderstel u een onderzoeksmalplaatje genoemd &quot;goedkeuring&quot;voor het duidelijk-benedenverkoopgebied van uw website hebt. U gebruikt het standaard HTML-zoekformulier met de volgende aanvullende formuliercode:

`<input type=hidden name="sp_t" value="clearance">`

Wanneer een klant een standaardvorm klikt die deze lijn van code bevat, wordt het malplaatje van het het onderzoeksvervoer van de &quot;klaring&quot;getoond samen met hun onderzoeksresultaten.

Zie [Inzamelingen gebruiken in zoekformulieren](../c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3).

Zie frames [gebruiken met formulieren](../c-appendices/c-searchforms.md#reference_82CDDDA1E37042E4849EBF7EA05407C5).

Zie [Voorbeeld van geavanceerd zoekformulier](../c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A).
