---
description: 'null'
seo-description: 'null'
seo-title: Sjablonen
solution: Target
title: Sjablonen
topic: Appendices,Site search and merchandising
uuid: 78299032-dc23-4dfe-b68f-cd57b2b6d7d8
translation-type: tm+mt
source-git-commit: ca4156f80d7dbb85d2d56b6caf7c0f560299d86e
workflow-type: tm+mt
source-wordcount: '15139'
ht-degree: 1%

---


# Sjablonen{#templates}

## Sjablonen {#concept_A5CFB6BD805D49459A96219AF1B17842}

## Labels voor presentatiesjablonen {#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64}

Een lijst met tags en kenmerken voor sitemalusjablonen voor het zoeken en verhandelen van sites.


Een presentatiesjabloon is een HTML-bestand dat sjabloontags voor presentaties bevat die door de zoekfunctie/merchandising van de site worden gedefinieerd. Deze tags geven aan hoe de zoekresultaten die klanten zien, zijn opgemaakt.

Zie [Informatie over sjablonen](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5).

U kunt uit de volgende groepen presentatiemarkeringen selecteren:

* [Verklaringen](../c-appendices/c-templates.md#section_82C5CA734D2941EB858FEFE3B695D2EC)
* [Resultaten](../c-appendices/c-templates.md#section_06F249C9F6AE4B0F8C32117E19DCC905)
* [Facetten](../c-appendices/c-templates.md#section_EA4C5678D5864B89BAB4D0DFE62A4624)
* [Broodkruimel](../c-appendices/c-templates.md#section_9B39B71FA6EC49FA8D88AD8A3BA987F7)
* [Menu&#39;s](../c-appendices/c-templates.md#section_1D489ADF041F4351A66E5D5742125CA8)
* [Pagenav](../c-appendices/c-templates.md#section_2EE397635C514BBC8D668278EA314F35)
* [Recente zoekopdrachten](../c-appendices/c-templates.md#section_8CD907521F584257B475595B01A5964B)
* [Bedoelde je](../c-appendices/c-templates.md#section_C1EB3B9D8E1242798A6E04609D1E3543)
* [Automatisch aanvullen](../c-appendices/c-templates.md#section_897316BEE1454E839A56B565CA4AF018)
* [Winkel](../c-appendices/c-templates.md#section_A33E25DB5E67404A823BD9618665B773)
* [Zones](../c-appendices/c-templates.md#section_B9B3179E000C42D492E1541F2FE44CB5)
* [Lus-indicatoren](../c-appendices/c-templates.md#section_387322CA0AA843A2ACF2795C328673E9)
* [Diverse talen](../c-appendices/c-templates.md#section_BFE8DC98E26F4D7BB60FEC54D9A5DC6C)

## Declaraties {#section_82C5CA734D2941EB858FEFE3B695D2EC}

Declaraties zijn speciale labels voor declaraties met instructies die u boven aan een presentatiesjabloon op hoofdniveau kunt instellen. Eventuele volgende declaraties worden genegeerd, inclusief declaraties in opgenomen sjablonen.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-content-type-header content="content-type"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Standaard wordt de presentatiesjabloon teruggestuurd met een mime-type tekst/html. U kunt wijzigen welk inhoudstype wordt gebruikt met deze tag. </p> <p>Declareer deze markering zo hoog mogelijk in uw presentatiesjabloon. Voeg geen andere tekst op dezelfde regel met deze tag toe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-xml-declare&gt; </span> </p> </td> 
   <td colname="col2"> <p> Als u XML retourneert, kunt u dit label gebruiken om de XML-declaratie te maken. Maak van dit label de eerste regel in uw presentatiesjabloon. Wanneer u dit label gebruikt, wordt het inhoudstype automatisch ingesteld op text/xml, tenzij u het in de eerste regel met <span class="codeph"> &lt;guided-content-type-header&gt; </span> overschrijft. Als u geen tekenset opgeeft, wordt standaard UTF-8 gebruikt. Deze tag resulteert in de volgende uitvoer in uw XML-document: </p> <p> <span class="codeph"> &lt;?xml version="1.0" encoding="charset-name" standalone="yes" ?&gt; </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Resultaten {#section_06F249C9F6AE4B0F8C32117E19DCC905}

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng 1/31/13--> <span class="codeph"> &lt;guided-results&gt;&lt;/guided-results&gt; </span> </p> </td> 
   <td colname="col2"> <p>De tag met instructies-resultaten definieert de grenzen van een resultatenlus. Om het even welke reeks resultaten kan worden betreden door een <span class="codeph"> gsname </span> attribuut te specificeren. Als er geen <span class="codeph"> gsname </span> is opgegeven, worden de standaardzoekresultaten weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng 1/31/13--> <span class="codeph"> &lt;guided-result-link&gt;&lt;/guided-result-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Als u een koppeling naar een bepaald resultaat wilt maken, gebruikt u de tag <span class="codeph"> guided-result-link </span>. Als u een <span class="codeph"> gsname </span>-kenmerk definieert, kunt u een veld uit de index gebruiken in plaats van de standaard "loc"-tag die naar de "search-url" verwijst. Andere kenmerken, zoals klasse en doel, kunnen ook worden doorgegeven. Deze worden uitgevoerd in de resulterende ankertag. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng 1/31/13--> <span class="codeph"> &lt;guided-result-img gsname="fieldname"&gt; </span> </p> </td> 
   <td colname="col2"> <p>De <span class="codeph"> &lt;guided-result-img&gt; </span>-tag helpt afbeeldingstags te maken in plaats van variabelen in te sluiten in een onbewerkte <span class="codeph">-tag </span>. </p> <p>Geef het veld op dat moet worden gebruikt voor het afbeeldingspad in het <span class="codeph">-kenmerk gsname </span>. Het resultaat is een <span class="codeph"> img </span>-tag met alle standaard HTML-kenmerken die u hebt gedefinieerd, doorgegeven. In het volgende voorbeeld: </p> <p> <code class="syntax html"> &lt;guided-result-img&nbsp;gsname="thumbnail" 
      &nbsp;class="thumb"&nbsp;border="0"/&gt; </code> </p> <p>wordt: </p> <p> <code class="syntax html"> &lt;img&nbsp;src="prod8172.jpg"&nbsp;class="thumb" 
      &nbsp;border="0"/&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 1/31/13; search-eng version does not have [escape...] Added ijson on 8/28/2015--> <span class="codeph"> &lt;guided-result-field gsname="fieldname"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Alle informatie die in de resultaten wordt weergegeven, wordt weergegeven als een <span class="codeph"> </span>-tag &lt;a1/&gt; (behalve wanneer u automatische genererende tags gebruikt, zoals de <span class="codeph"> &lt;guided-result-img&gt; </span>-tag). </p> <p>Geef de naam van het veld Zoekindex op in <span class="codeph"> gsname </span>. De exacte tekenreeks die wordt doorgegeven, wordt in de sjabloon uitgevoerd. </p> <p>U kunt een vluchtoptie specificeren als u dit gebied op een andere manier van wat in het vervoermalplaatje werd gespecificeerd wilt ontsnapt. </p> <p>Deze codering wordt toegepast boven op de codering die in de transportsjabloon is opgegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <span class="codeph"> &lt;guided-if&gt;&lt;/guided-if-result-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze set voorwaardelijke tags is waar als er inhoud is in het specifieke veld dat moet worden weergegeven. Als er geen inhoud bestaat, is de voorwaarde onwaar. U kunt de labels gebruiken om te bepalen of omringende HTML wordt weergegeven als een waarde niet bestaat, of als een andere afbeelding wordt weergegeven, enzovoort. </p> <p> <code class="syntax html"> &lt;guided-if-result-field&nbsp;gsname="thumbnail"&gt; 
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
   <td colname="col2"> <p>Wanneer het tonen van resultaten in kolommen, wordt dit markering gebruikt om te identificeren of het huidige resultaat het eind van een kolom merkt. </p> <p>Wanneer de Booleaanse voorwaarde waar is, wordt HTML toegevoegd aan het einde van het resultaat om de rij af te maken en een nieuwe te starten. Als dit de laatste rij is, wordt er geen nieuwe rij gestart. </p> <p>Zie <span class="codeph"> &lt;guided-if-not-last&gt; </span> voor meer informatie over die tag. </p> <p> <code class="syntax html"> &lt;guided-if-result-wrap&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/div&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-not-last&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;div&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-not-last&gt; 
      &nbsp;&lt;/guided-if-result-wrap&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version, 1/31/13--> <span class="codeph"> &lt;guided-results-found&gt; </span> </p> </td> 
   <td colname="col2"> <p>Retourneert een 1 als het back-end zoekverzoek resultaten retourneert en 0 als dit niet het geval is. Als geen <span class="codeph"> gsname </span> wordt gespecificeerd, veronderstelt de markering het primaire onderzoek. Deze tag is handig om logica door te geven aan JavaScript-routines. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-results-total&gt; </span> </p> </td> 
   <td colname="col2"> <p>Retourneert het totale aantal resultaten in de opgegeven resultatenset. Veronderstelt het standaardonderzoek wanneer geen <span class="codeph"> gsname </span> wordt gegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-results-lower&gt; </span> </p> </td> 
   <td colname="col2"> <p>Retourneert het resultaatnummer van het onderste resultaat op de pagina voor de opgegeven resultatenset. Veronderstelt het standaardonderzoek wanneer geen <span class="codeph"> gsname </span> wordt gegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-results-upper&gt; </span> </p> </td> 
   <td colname="col2"> <p>Retourneert het resultaatnummer van het bovenste resultaat op de pagina voor de opgegeven resultatenset. Veronderstelt het standaardonderzoek wanneer geen <span class="codeph"> gsname </span> wordt gegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version 1/31/13--> 

    &amp;lt;/guided-if[-not]-results-found&amp;gt;   &lt;/p>  &lt;/td>
<td colname="col2"> <p>Hiermee wordt inhoud weergegeven wanneer resultaten worden gevonden. Of geeft geen HTML-resultaten weer wanneer er geen resultaten worden gevonden. </p> <p> <code class="syntax html"> &lt;guided-if-results-found&nbsp;gsname="products"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-results&nbsp;gsname="products"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;... 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-results&gt; 
      &lt;guided-else-results-found&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;No&nbsp;results&nbsp;were&nbsp;found. 
      &lt;/guided-if-results-found&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-result-title /&gt; </span> </p> </td> 
   <td colname="col2"> <p>De <span class="codeph"> &lt;guided-result-title&gt; </span>-tag geeft de waarde van het sjabloonveld voor titelvervoer dat is opgegeven met <span class="codeph"> &lt;title&gt; </span>-transporttag. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-result-description /&gt; </span> </p> </td> 
   <td colname="col2"> <p>De <span class="codeph"> &lt;guided-result-description&gt; </span>-tag geeft de waarde van een beschrijvingssjabloonveld dat is opgegeven met <span class="codeph"> &lt;description&gt; </span>-transporttag. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-result-loc /&gt; </span> </p> </td> 
   <td colname="col2"> <p>De tag &lt; <span class="codeph"> guided-result-loc&gt; </span> geeft de waarde van het sjabloonveld voor lokaal transport dat is opgegeven met de transporttag <span class="codeph"> &lt;loc&gt; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> 

    &amp;lt;/guided-if-result-field&amp;gt;   &lt;/p>  &lt;/td>
<td colname="col2"> <p>True if there is content in the specific field to display. Als er geen inhoud bestaat, is de voorwaarde onwaar. Gebruik de tags om te bepalen of omringende HTML wordt weergegeven of niet als een waarde niet bestaat, of als een andere afbeelding wordt weergegeven, enzovoort. </p> <p> <code class="syntax html"> &lt;guided-if-result-field&nbsp;gsname="thumbnail"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-result-img&nbsp;gsname="thumbnail"&nbsp;class="thumb"/&gt; 
      &lt;guided-else-result-field&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;img&nbsp;src="nothumb.jpg"&nbsp;class="nothumb"/&gt; 
      &lt;/guided-if-result-field&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-result-attribute-table gsname="tablename"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze markering verstrekt een lijn door attributenlijst die in het vervoermalplaatje met <span class="codeph"> &lt;attribute_table&gt; </span> vervoermarkering wordt bepaald. Er is <span class="codeph"> &lt;guided-result-attribute-table-field&gt; </span> tag voor het weergeven van veldwaarden voor kenmerktabellen. Het is ook mogelijk om onbewerkte <span class="codeph"> guided-result-field </span> markeringsbinnenloop te gebruiken voor het weergeven van andere resultaatvelden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-result-attribute-table-field gsname="fieldname"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Toont het gebied van de attributenlijst zoals die in vervoermalplaatje wordt bepaald. </p> <p> 

    ...
    
    &amp;lt;ul&amp;gt;
    
    &amp;lt;guided-result-attribute-table&amp;nbsp;gsname=&quot;downloads&quot;&amp;gt;
    &amp;nbsp;&amp;nbsp;&amp;lt;li&amp;gt;
    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;lt;a&amp;nbsp;href=&quot;&amp;lt &amp;guided-result-attribute-table-field&amp;nbsp;gsname=&quot;download_link&quot;&amp;nbsp;/&amp;gt;&quot;&amp;gt;
    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;lt;guided-result-attribute-field&amp;nbsp;gsname=&quot;download_title&quot;&amp;nbsp;/&amp;gt;
    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;lt;/a&amp;gt;&amp;nbsp;(&amp;lt;guided-result-field&amp;nbsp;gsname=&quot;title&quot;/&amp;gt;)
    &amp;nbsp;&amp;nbsp;&amp;lt; /li&amp;gt;
    &amp;lt;/guided-result-attribute-table&amp;gt;
    
    &amp;lt;/ul&amp;gt;
    
    ..
    
    &amp;lt;/guided-results&amp;gt;   &lt;/p>  &lt;/td>
</tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW for S&P 8.17.0 release in October 2014--> <span class="codeph"> &lt;guided-trace&gt; </span> </p> </td> 
   <td colname="col2"> <p>Hiermee wordt de traceerinformatie uitgevoerd die wordt gevonden binnen de traceergegevens in het algemene gedeelte van de JSON-gegevensuitvoer door de transportsjabloon voor de opgegeven zoekopdracht. </p> <p>Als er geen zoeknaam wordt gegeven, wordt <span class="codeph"> standaard </span> aangenomen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>19 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW for S&P 8.17.0 release on October 30, 2014)--> <span class="codeph"> &lt;guided-result-trace /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Hiermee wordt de JSON-inhoud uitgevoerd die is gevonden in de resultaten &gt; traceerinformatie van de JSON-gegevensuitvoer via de transportsjabloon voor het huidige zoekresultaat. </p> <p>Deze tag is alleen geldig in de <span class="codeph"> &lt;guided-results&gt;&lt;/guided-results&gt; </span>-lus. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Facetten {#section_EA4C5678D5864B89BAB4D0DFE62A4624}

Facetten zijn navigatiecomponenten waarmee u naar zoekresultaten kunt gaan. U kunt de facetlabels gebruiken om verschillende facetten in uw presentatiesjabloon weer te geven. U verwijst facetten op naam.

Zie [Informatie over facetten](../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5).

Zie [Informatie over facetrails](../c-about-design-menu/c-about-facet-rails.md#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB).

Zie [Informatie over dynamische factoren](../c-about-design-menu/c-about-dynamic-facets.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW 02/27/2014--> <span class="codeph"> &lt;guided-dynamic-facets&gt;&lt;/guided-dynamic-facets&gt; </span> </p> </td> 
   <td colname="col2"> 
    <!--NEW 2/2/2014--> <p>Een luscontext voor om het even welke dynamische facetten voor een bepaalde onderzoek. </p> <p>De <span class="codeph"> &lt;guided-facet&gt; </span> presentatiesjabloontag wordt bewerkt, zodat het kenmerk gsname automatisch wordt verschaft door de <span class="codeph"> </span> herhalingscontext. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-display-name gsname=" <span class="varname"> facetname </span>" /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Retourneert het weergavelabel van het facet. </p> <p>Als de facet de <span class="codeph"> &lt;display-name&gt; </span> markering op het vervoermalplaatje gebruikt, wordt de inhoud van die markering het etiket. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet-rail&gt;&lt;/guided-facet-rail&gt; </span> </p> </td> 
   <td colname="col2"> <p> Definieert een sectie op de presentatiesjabloon die wordt gebruikt als een herhalingspatroon voor elk facet in de facetrails. </p> <p> Elk facet dat tot de facetspoorstaaf behoort gebruikt dit gedeelte om zijn output te evalueren. </p> <p>Hier volgt een voorbeeld van een facetrails: </p> <p> <code class="syntax html"> &lt;guided-facet-rail&gt; 
      &nbsp;&nbsp;&lt;guided-facet&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-display-name/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;... 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet&gt; 
      &nbsp;&nbsp;&lt;/guided-facet-rail&gt; </code> </p> <p>Merk op dat de volgende markeringen <span class="codeph"> gsname </span> geen attribuut nodig hebben wanneer binnen <span class="codeph"> </span> &lt;a3/&gt; markering &lt;a3 als waarde dynamisch bepaald bij onderzoekstijdstip is en behoorlijk substitueert: </p> 
    <ul id="ul_5B5ACAFD2B8848DDB27471AB9DA7BE6E"> 
     <li id="li_5A07E78D51FE4708879DD742C877FFFF">met instructies </li> 
     <li id="li_B875DCACD7AB4FC890A456A6939AB657">guided-facet-display-name </li> 
     <li id="li_B70450749E864DE7BA401E3CD6EF5EB3">met instructies-facet-total-count </li> 
     <li id="li_DECDF5EF6FF7454F86C236D322F2BFEA">guided-facet-undo-link </li> 
     <li id="li_176949227AC14E8CA643A419E10F7B5A">guided-facet-undo-path </li> 
     <li id="li_B32D981281744462BC680F6EFEAC0069">met instructies, gedrag </li> 
    </ul> <p>De sorteercriteria op de pagina <span class="wintitle"> Facet Rail </span> bepalen de positie van de facetten. U kunt de sorteervolgorde kiezen in de vervolgkeuzelijst Methode voor sorteerfactoren. </p> <p> 
     <!--NEW 02/27/2014-->Deze tag kan optioneel een kenmerkwaarde van de naam gsname van  <span class="codeph"> _dynamic_facets accepteren  </span>, die een herhalingscontext biedt voor alle dynamische facetten voor deze zoekopdracht. Deze vooraf gedefinieerde facetrail wordt ook in de Business Rules-gebruikersinterface weergegeven voor actie <span class="codeph"> push facet X in facet rail '_dynamic_facets' naar positie Y </span>. </p> <p>Zie <a href="../c-about-design-menu/c-about-facet-rails.md#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB" format="dita" scope="local"> Info over facetrails </a>. </p> <p>Zie ook <a href="../c-about-design-menu/c-about-dynamic-facets.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> Informatie over dynamische factoren </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match current search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet gsname=" <span class="varname"> facetname </span>" height=" <span class="varname"> 60px </span>" width=" <span class="varname"> 120px </span>"&gt;&lt;/guided-facet&gt; </span> </p> </td> 
   <td colname="col2"> <p>Met de <span class="codeph">-tag met instructies-facet </span> kunt u een gebied definiëren waarbinnen alle facettags betrekking hebben op een bepaald facet. Dit label is ook een Booleaanse tag die alle inhoud verbergt als er geen waarden in het facet bestaan. In dat geval heeft het geen zin de waarden van de facetten uit te voeren. </p> <p>De kenmerken height en width zijn optioneel en de afmetingen worden opgegeven in pixels (px). De Visuele Bouwer van de Regel (VRB) gebruikt deze twee attributen, en toont een gestippelde doos als interactieve placeholder wanneer de facet verborgen is. </p> <p> Wanneer de weergavenaam zich in het facet bevindt en het facet verborgen is, wordt de naam ook verborgen. Als de naam zich echter buiten het facet bevindt, kunt u de naam alleen verbergen als een <span class="codeph"> zone </span>-tag of een <span class="codeph"> geleide-if-facet-visible </span>-tag er omheen is gewikkeld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW, brought in from search-eng version, 1/31/13--> <span class="codeph"> &lt;guided-if&gt;&lt;/guided-if&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze voorwaardelijke tag is waar wanneer het aantal facetwaarden groter is dan de lengte-drempel die in de configuratie is gedefinieerd. Gebruik deze optie om een facet weer te geven als een ander interface-element (zoals een afgekapte lijst of een schuifvak) wanneer de lijst te lang is. </p> <p> <code class="syntax xml"> &lt;guided-facet&nbsp;name="category"&gt; 
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
      &lt;/guided-facet&gt; </code> </p> <p>U kunt deze voorwaarde ook buiten de context van een genoemd <span class="codeph"> Geleide-facet </span> blok gebruiken door een specifiek facet direct door gebruik van <span class="codeph"> gsname </span> attributen van verwijzingen te voorzien. </p> <p> <code class="syntax html"> &lt;guided-if-facet-long&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;The&nbsp;category&nbsp;facet&nbsp;is&nbsp;very&nbsp;long! 
      &lt;/guided-if-facet-long&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW, brought in from search-eng version, 1/31/13--> <span class="codeph"> &lt;guided-if&gt;&lt;/guided-if&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze voorwaardelijke tag is waar wanneer ten minste één keer op het facet wordt geklikt en er momenteel een facetwaarde is geselecteerd. Het wordt gebruikt om HTML- of tags gs weer te geven of te verbergen, afhankelijk van het feit of er op een facet is geklikt. </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;name="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This&nbsp;facet&nbsp;has&nbsp;been&nbsp;selected.&nbsp;&nbsp;You&nbsp;can&nbsp;no&nbsp;longer&nbsp;refine&nbsp;it. 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-value-link&gt;&lt;guided-facet-value&nbsp;/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-selected&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>U kunt deze voorwaarde ook buiten de context van een genoemd <span class="codeph"> Geleide-facet </span> blok gebruiken door een specifiek facet direct door gebruik van <span class="codeph"> gsname </span> attributen van verwijzingen te voorzien. </p> <p> <code> &lt;guided-if-facet-selected&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;The&nbsp;category&nbsp;facet&nbsp;is&nbsp;selected! 
      &lt;/guided-if-facet-selected&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW, brought in from search-eng version, 1/31/13--> <span class="codeph"> &lt;guided-if&gt;&lt;/guided-if&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze voorwaardelijke tag is waar wanneer er slechts één facetwaarde is. Gebruik de tag om de weergave van het facet te wijzigen als het niet mogelijk is de resultaten te verfijnen. </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;name="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-single&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Facet&nbsp;is&nbsp;not&nbsp;refinable. 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-single&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-value-link&gt;&lt;guided-facet-value&nbsp;/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-single&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>U kunt deze voorwaarde ook buiten de context van een genoemd <span class="codeph"> Geleide-facet </span> blok gebruiken door een specifiek facet direct door gebruik van <span class="codeph"> gsname </span> attributen van verwijzingen te voorzien. </p> <p> <code class="syntax html"> &lt;guided-if-facet-single&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;There&nbsp;is&nbsp;only&nbsp;one&nbsp;value&nbsp;in&nbsp;the&nbsp;category&nbsp;facet! 
      &lt;/guided-if-facet-single&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> 
     <!--Added 7/15/2014--> <span class="codeph"> &lt;guided-if&gt;&lt;/guided-if&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze voorwaardelijke tag is waar wanneer het facet meerdere selecties heeft. Gebruik de tag om de weergave van het facet te wijzigen binnen <span class="codeph"> </span>- of <span class="codeph"> </span>-tags &lt;a3/&gt;. </p> <p> 

    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;lt;guided-if-facet-multiselect&amp;gt;
    &amp;nbsp;...
    &amp;nbsp;&amp;lt;guided-else-facet-multiselect&amp;gt;
    &amp;nbsp;...
    &amp;nbsp;&amp;lt;/guided-if-facet-multiselect&amp;gt;
    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;
    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;lt;/guided-facet&amp;gt;
    &amp;nbsp;&amp;nbsp;&amp;lt;/guided-facet-rail&amp;gt;   &lt;/p>  &lt;/td>
</tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet-values&gt; facetname  </span>"]&gt;&lt;/guided-facet-values&gt; </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Dit is de iteratortag van de facetwaardelus. U kunt het binnen de context van een genoemd <span class="codeph"> Geleide-facet </span> blok bepalen, in welk geval u <span class="codeph"> <span class="varname"> gsname </span> </span> kunt weglaten. Of u kunt het buiten elk <span class="codeph">-blok met instructies-facet </span> definiëren, maar u moet het <span class="codeph"> <span class="varname"> gsname </span> </span> &lt;a5/&gt;-kenmerk gebruiken om te bepalen welke set met facetwaarden wordt weergegeven. </p> <p>U kunt deze tag ook gebruiken om de waarden van facetten weer te geven buiten de context van een benoemd <span class="codeph">-blok met instructies-facet </span>. U verwijst rechtstreeks naar een specifiek facet door het <span class="codeph"> <span class="varname"> gsname </span> </span> attribuut te gebruiken. </p> <p> <code class="syntax html"> &lt;script&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;registerFacetValues('category',&nbsp;'&lt;guided-facet-values&nbsp;gsname="category"&gt;&lt;guided-facet-value/&gt;,&lt;/guided-facet-values&gt;'); 
      &lt;/script&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet-value&gt; </span> </p> </td> 
   <td colname="col2"> <p>Geeft als uitvoer de tekenreeks van de huidige facetwaarde. </p> <p>De standaardwaarde is HTML escape. Met de optie Escape kunt u bepalen hoe de waarde wordt beschermd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet-count /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Hiermee geeft u het aantal resultaten weer dat overeenkomt met de huidige waarde van de facet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW, brought in from search-eng version, 1/31/13--> <span class="codeph"> &lt;guided-facet-value-link&gt;&lt;/guided-facet-value-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Hiermee maakt u een koppeling rond de tekenreeks met de facetwaarde waarop de bezoeker van de site moet klikken. Het pad wordt automatisch gegenereerd om de resultaten met de huidige facetwaarde te beperken. Het doorgeven van alle kenmerken rechtstreeks naar de ankertag wordt ondersteund. </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
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
   <td colname="col2"> <p>Hiermee wijzigt u de weergave van de facetwaarde wanneer deze momenteel is geselecteerd. Als het al is gekozen, is het in de meeste gevallen niet langer koppelbaar. </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
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

    &amp;lt;/guided-if[-not]-facet-value-spook&amp;gt;   &lt;/p>  &lt;/td>
<td colname="col2"> <p>Wijzigt de weergave van de waarde van de facet als het een spookwaarde is. Wanneer een waarde van een facet een spookwaarde is, wordt deze doorgaans cursief weergegeven om aan te geven dat de waarde ontbreekt of wordt "gehost". </p> <p>Het volgende codefragment is een voorbeeld van een facetblok: </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
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
   <td colname="col2"> <p>Hiermee wordt een koppeling voor ongedaan maken voor een bepaald facet weergegeven. Als er meerdere facetten zijn, heft deze koppeling de selectie van alle waarden van de desbetreffende facet op. Geef het facet een naam. Als het facet momenteel niet is geselecteerd, is de koppeling het huidige pad. </p> <p>Hieronder ziet u een voorbeeld van het gebruik van deze tag: </p> <p> <code class="syntax html"> &lt;guided-if-facet-selected&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-undo-link&nbsp;gsname="category"&gt;Undo&nbsp;Category&lt;/guided-facet-undo-link&gt; 
      &lt;/guided-if-facet-selected&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-facet-long [gsname="facetname"]&gt; 
      &lt;guided-else-facet-long&gt;&lt;/guided-if-facet-long&gt; </code> </p> </td> 
   <td colname="col2"> <p>Deze voorwaardelijke tag is waar wanneer het aantal facetwaarden groter is dan de lengte-drempel die in de configuratie is gedefinieerd. Gebruik deze optie om een facet weer te geven als een ander interface-element (zoals een afgekapte lijst of een schuifvak) wanneer de lijst te lang is. </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;gsname="category"&gt; 
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
      &nbsp;&lt;/guided-facet&gt; </code> </p> <p>U kunt deze voorwaarde ook buiten de context van een genoemd <span class="codeph"> Geleide-facet </span> blok gebruiken door rechtstreeks naar een specifiek facet te verwijzen door het <span class="codeph"> <span class="varname"> gsname </span> </span> attribuut te gebruiken. </p> <p> <code class="syntax html"> &lt;guided-if-facet-long&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The&nbsp;category&nbsp;facet&nbsp;is&nbsp;very&nbsp;long! 
      &lt;/guided-if-facet-long&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-facet-selected [gsname="facetname"]&gt; 
      &lt;guided-else-facet-selected&gt;&lt;/guided-if-facet-selected&gt; </code> </p> </td> 
   <td colname="col2"> <p>Deze voorwaardelijke tag is waar wanneer ten minste één keer op het facet wordt geklikt en er momenteel een facetwaarde is geselecteerd. Het kan worden gebruikt om HTML- of gs-tags weer te geven of te verbergen, afhankelijk van het feit of op een facet wordt geklikt. </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This&nbsp;facet&nbsp;has&nbsp;been&nbsp;selected.&nbsp;&nbsp;You&nbsp;can&nbsp;no&nbsp;longer&nbsp;refine&nbsp;it. 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-selected&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>U kunt deze voorwaarde ook buiten de context van een genoemd <span class="codeph"> Geleide-facet </span> blok gebruiken door een specifiek facet direct door gebruik van <span class="codeph"> gsname </span> attributen van verwijzingen te voorzien. </p> <p> <code class="syntax html"> &lt;guided-if-facet-selected&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The&nbsp;category&nbsp;facet&nbsp;is&nbsp;selected! 
      &lt;/guided-if-facet-selected&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-facet-single [gsname="facetname"]&gt; 
      &lt;guided-else-facet-single&gt;&lt;/guided-if-facet-single&gt; </code> </p> </td> 
   <td colname="col2"> <p>Deze voorwaardelijke tag is waar wanneer er slechts één facetwaarde is. Deze kan worden gebruikt om de weergave van het facet te wijzigen wanneer de resultaten niet kunnen worden verfijnd. </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-single&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Facet&nbsp;is&nbsp;not&nbsp;refinable. 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-single&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-single&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>U kunt deze voorwaarde ook buiten de context van een genoemd <span class="codeph"> Geleide-facet </span> blok gebruiken door rechtstreeks naar een specifiek facet te verwijzen door het <span class="codeph"> <span class="varname"> gsname </span> </span> attribuut te gebruiken. </p> <p> <code class="syntax html"> &lt;guided-if-facet-single&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;There&nbsp;is&nbsp;only&nbsp;one&nbsp;value&nbsp;in&nbsp;the&nbsp;category&nbsp;facet! 
      &lt;/guided-if-facet-single&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>19 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-facet-has-values [gsname="facetname"]&gt; 
      &lt;guided-else-facet-has-values&gt;&lt;/guided-if-facet-has-values&gt; </code> </p> </td> 
   <td colname="col2"> <p>Met deze voorwaarde kunt u controleren of het opgegeven facet al waarden heeft. U kunt het gebruiken voor het tonen van een ander facet in plaats van een leeg facet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>20 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-total-count gsname=" <span class="varname"> facetname </span>" /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Hiermee wordt het totale aantal resultaten binnen de opgegeven facet uitgevoerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>21 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-value gsname=" <span class="varname"> associated custom facet value </span>"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Hiermee wordt de tekenreeks uitgevoerd van een waarde die aan het facet is gekoppeld. Er kunnen 0 of meer velden zijn gekoppeld aan een facet. Het hebben van bijbehorende gebieden is zeldzaam en om zulk te steunen vormt u het vervoermalplaatje. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>22 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-facet-value gsname=" <span class="varname"> associated custom facet value </span>" /&gt;&lt;guided-else-facet-value&gt;&lt;/guided-if-facet-value&gt; </span> </p> </td> 
   <td colname="col2"> <p>Test of de waarde van de facet een bijbehorende veldwaarde heeft. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>23 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-link&gt; value  </span>"]+&gt;&lt;/guided-facet-link&gt; </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Hiermee maakt u een koppeling rond de tekenreeks met de facetwaarde waarop de klant moet klikken. Het pad wordt automatisch gegenereerd om de resultaten met de huidige facetwaarde te beperken. Het doorgeven van alle kenmerken rechtstreeks naar de ankertag wordt ondersteund. </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&nbsp;class="facetlink"&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt; 
      &lt;/guided-facet-values&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>24 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-value-path&gt; </span> </p> </td> 
   <td colname="col2"> <p>Hiermee maakt u uw eigen koppeling naar een facetwaarde. </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-lt/&gt;a&nbsp;href="&lt;guided-facet-value-path/&gt;"&lt;guided-gt/&gt;&lt;guided-facet-value/&gt;&lt;/a&gt; 
      &lt;/guided-facet-values&gt; </code> </p> <p>De standaardwaarde is URL escape. U kunt echter een andere coderingslaag toevoegen door op te geven welke modus voor escape-tekens u wilt gebruiken met de escape-parameter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>25 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-value-children&gt;&lt;/guided-facet-value-children&gt; </span> </p> </td> 
   <td colname="col2"> <p>Als <span class="codeph"> &lt;guided-facet-values&gt; </span> elke facetwaarde doorloopt, doorloopt deze tag alle onderliggende waarden van een genest facet. Binnen deze tag gebruikt u de typische facettags voor het maken van koppelingen, het maken van koppelingen voor ongedaan maken en het weergeven van facetwaarden. Deze tag moet zich binnen <span class="codeph"> &lt;guided-facet-values&gt; </span> bevinden, omdat de tag wel genest is. </p> <p>Een voorbeeld van het gebruik van deze tag is: </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
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
   <td colname="col2"> <p>Test of de huidige facetwaarde onderliggende waarden heeft. Aanbevolen om te gebruiken alvorens <span class="codeph"> &lt;guided-facet-value-children&gt; </span> markeringen te gebruiken. De component "else" is optioneel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>27 </p> </td> 
   <td colname="col1"> <p> 

    &amp;lt;guided-else[-not]-facet-value-above-length-threshold&amp;gt;
    
    &amp;lt;/guided-if[-not]-facet-value-above-length-threshold&amp;gt;   &lt;/p>  &lt;/td>
<td colname="col2"> <p>Hiermee wordt bepaald of de huidige waarde van de facet binnen de lusbewerking voor waarden boven de lengtedrempel ligt. Deze wordt doorgaans gebruikt om alleen waarden onder de drempelwaarde weer te geven op een lang facet (tenzij de gebruiker eerder een koppeling 'Meer zien' heeft geselecteerd die onder de facet wordt weergegeven). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>28 </p> </td> 
   <td colname="col1"> <p> 

    &amp;lt;guided-else[-not]-facet-value-equals-length-threshold&amp;gt;
    
    &amp;lt;/guided-if[-not]-facet-value-equals-length-threshold&amp;gt;   &lt;/p>  &lt;/td>
<td colname="col2"> <p>Hiermee wordt bepaald of de huidige waarde van de facet binnen de lusbewerking voor waarden gelijk is aan de lengtedrempel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>29 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-value-undo-link&gt;&lt;/guided-facet-value-undo-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Hiermee wordt een koppeling voor ongedaan maken weergegeven voor een bepaalde geselecteerde facetwaarde. Gebruik deze optie om een koppeling voor ongedaan maken weer te geven naast een geselecteerde facetwaarde. Omdat deze koppeling voor ongedaan maken alleen die bepaalde geselecteerde waarde ongedaan maakt, verschilt deze van <span class="codeph"> &lt;guided-facet-undo-link&gt; </span> waarmee alle geselecteerde waarden worden gedeselecteerd. </p> <p> <p>Opmerking:  Als het facet geen multi-select gedrag heeft, dan hebben de twee undo verbindingen het zelfde gedrag. Dat wil zeggen dat het facet slechts één geselecteerde waarde kan hebben. </p> </p> <p>Als het facet momenteel niet is geselecteerd, is de koppeling het huidige pad. Gebruik dit label alleen in een <span class="codeph">-lus met instructies-facet-values </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>30 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-value-undo-path /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Maak uw eigen facetwaarde en maak de koppeling ongedaan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>31 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-undo-path gsname=" <span class="varname"> facetname </span>" /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Maak uw eigen koppeling Ongedaan maken facet. </p> <p> Gelijkaardig aan <span class="codeph"> &lt;guided-facet-undo-link&gt; </span> markering behalve dat geeft het u de ruwe weg om uw eigen te bouwen undo verbinding. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>32 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-facet-value-matches facetname="facetname" value="value"&gt;&lt;guided-else-facet-value-matches&gt; 
      &lt;/guided-if-facet-value-matches&gt; </code> </p> </td> 
   <td colname="col2"> <p>Geef voorwaardelijk HTML weer wanneer het bepaalde facet de geselecteerde of enige waarde "waarde" heeft. Deze reeks labels wordt vaak gebruikt om een facet weer te geven op basis van de waarde die in een ander facet is geselecteerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>33 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-behavior gsname=" <span class="varname"> facetname </span>" /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Bepaal het gedrag van een facet, zoals normaal, kleverig, of multi-select. Het is nuttig voor klanten die de resultaten van XML ontvangen en willen dynamisch veranderen hoe de facet op zijn gedrag wordt getoond. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>34 </p> </td> 
   <td colname="col1"> <p> 

    &amp;lt;/guided-if-facet[-not]-visible&amp;gt;   &lt;/p>  &lt;/td>
<td colname="col2"> <p>De inhoud van deze tag wordt verborgen of onthuld op basis van de zichtbaarheidsstatus van het facet. Als een bedrijfsregel het facet direct verbergt of onthult, wordt alle inhoud binnen het facet verborgen of onthuld. Deze labels hoeven niet om de facet te lopen. </p> <p> Deze tag wordt vaak gebruikt om de weergavenaam te verbergen wanneer de naam zich buiten het facet bevindt. Als u deze tag rondom de weergavenaam plaatst, verdwijnt de naam wanneer het facet verborgen is. </p> <p>Deze tag vervangt de zone en biedt veel van dezelfde prestatievoordelen als het gebruik van zones. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Broodkruimel {#section_9B39B71FA6EC49FA8D88AD8A3BA987F7}

Zie [Informatie over broodkruimels](../c-about-design-menu/c-about-breadcrumbs.md#concept_FB8A943C594A4A1593B118141DA61F03).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-breadcrumb&gt; breadcrumbname  </span>"]&gt;&lt;/guided-breadcrumb&gt; </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>De lustag voor de breadcrumb. Alle inhoud tussen de openingstag en de afsluitende tag wordt herhaald voor elk querynummer van het huidige frame. </p> <p>Als <span class="codeph"> <span class="varname"> gsname </span> </span> wordt weggelaten, wordt de breadcrumb met de naam "default" gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-breadcrumb-link&gt;&lt;/guided-breadcrumb-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Maakt een koppeling in de broodkruimel. Het standaardgedrag is het goto-gedrag. Als de koppeling zich anders gedraagt, gebruikt u het optionele kenmerk <span class="codeph"> <span class="varname"> gsname </span> </span> om "remove" of "drop" op te geven. Kenmerken die in de tag zijn opgenomen, worden doorgegeven aan de resulterende ankertag. </p> <p> <code class="syntax html"> &lt;guided-breadcrumb&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-link&nbsp;gsname="remove"&nbsp;class="bc_link"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-value/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-breadcrumb-link&gt; 
      &lt;/guided-breadcrumb&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-breadcrumb-value /&gt; </span> </p> </td> 
   <td colname="col2"> <p>De waardetag drukt uit de getransformeerde waarde van de huidige broodkruimeliteratie. Het wordt alleen gebruikt in de context van een <span class="codeph">-blok met instructies-breadcrumb </span>. </p> <p> <code class="syntax html"> &lt;guided-breadcrumb&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-value/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-breadcrumb-link&gt; 
      &lt;/guided-breadcrumb&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-breadcrumb-label /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Met de labeltag wordt een label voor een waarde van een breadcrumb weergegeven, waarin wordt aangegeven welke facet is geselecteerd om dat item van de breadcrumb te genereren. Het wordt alleen gebruikt in de context van een <span class="codeph">-blok met instructies-breadcrumb </span>. </p> <p> <code class="syntax html"> &lt;guided-breadcrumb&gt; 
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
   <td colname="col2"> <p>Deze voorwaardelijke tag wordt gebruikt om inhoud voorwaardelijk weer te geven als de huidige breadcrumb-waarde een label heeft. Het wordt alleen gebruikt om labels en bijbehorende inhoud weer te geven wanneer er een label daadwerkelijk bestaat. Het wordt alleen gebruikt in de context van een <span class="codeph">-blok met instructies-breadcrumb </span>. </p> <p> <code class="syntax html"> &lt;guided-breadcrumb&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-breadcrumb-label&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-label/&gt;: 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-breadcrumb-label&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-value/&gt;&lt;/guided-breadcrumb-link&gt; 
      &lt;/guided-breadcrumb&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-breadcrumb-path&gt; </span> </p> </td> 
   <td colname="col2"> <p>Wordt gebruikt om uw eigen broodkruimelkoppeling te maken. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Menu&#39;s {#section_1D489ADF041F4351A66E5D5742125CA8}

Zie [Menu&#39;s](../c-about-design-menu/c-about-menus.md#concept_68123CE5CF4447B59217B5D721424E32).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu gsname="menuname"&gt;&lt;/guided-menu&gt; </span> </p> </td> 
   <td colname="col2"> <p>Dit is de iteratortag van de menumarteruslus. Gebruik het <span class="codeph"> gsname </span> attribuut om te identificeren welke reeks menupunten wordt getoond. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu-item-link&gt;&lt;/guided-menu-item-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Hiermee geeft u de URL voor het verfijnen van de huidige zoekopdracht naar het menu-item. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu-item-option&gt; </span> </p> </td> 
   <td colname="col2"> <p>Gewoonlijk wordt een menu getoond in een uitgezochte controle op een malplaatje. Deze markering maakt het construeren van de uitgezochte controle gemakkelijker omdat het HTML voor het produceren van de optie voor de uitgezochte controle produceert. </p> <p>Het volgende codeblok bijvoorbeeld: </p> <p> <code class="syntax html"> &lt;select&nbsp;name="sort"&nbsp;onchange="gcGo(this);"&gt; 
      &lt;guided-menu&nbsp;gsname="sort"&gt; 
      &lt;guided-menu-item-option/&gt; 
      &lt;/guided-menu&gt; 
      &lt;/select&gt; </code> </p> <p>Kan als volgt HTML genereren: </p> <p> <code class="syntax html"> &lt;select&nbsp;name="sort"&nbsp;onchange="gcGo(this);"&gt; 
      &nbsp;&nbsp;&lt;option&nbsp;value="?sort=relevance;sp_sfvl_field=product-type|category|size;"&nbsp;selected="selected"&gt;Sort&nbsp;by&nbsp;Relevance&lt;/option&gt; 
      &nbsp;&nbsp;&lt;option&nbsp;value="?sort=avail-code;sp_sfvl_field=product-type|category|size;"&gt;Sort&nbsp;by&nbsp;Availability&lt;/option&gt; 
      &nbsp;&nbsp;&lt;option&nbsp;value="?sort=price;sp_sfvl_field=product-type|category|size;"&gt;Sort&nbsp;by&nbsp;Price&lt;/option&gt; 
      &lt;/select&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu-item-value /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Retourneert de tekenreeks van de waarde die aan het menu is gekoppeld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu-item-label /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Retourneert de tekenreeks van het label dat aan het menu is gekoppeld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu-item-path /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Retourneert de padtekenreeks. Gebruik de tag als u een parameter wilt toevoegen aan het pad en een aangepaste koppeling wilt maken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if-menu-item-selected&gt; 
      &lt;guided-else-menu- 
      item-selected&gt; 
      &lt;/guided-if-menu-item-selected&gt; </code> </p> </td> 
   <td colname="col2"> <p>Retourneert een 1 of 0 die aangeeft of het huidige menu-item is geselecteerd. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Pagenav {#section_2EE397635C514BBC8D668278EA314F35}

Met de paginanavigatietags kunt u een set koppelingen maken waarmee een gebruiker door de zoekresultaten kan bladeren.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-pages&gt;&lt;/guided-pages&gt; </span> </p> </td> 
   <td colname="col2"> <p>De lustag voor de paginanavigatie. Alle inhoud tussen de openingstag en de afsluitende tag wordt herhaald voor elke pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-page-link&gt;&lt;/guided-page-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Maakt een koppeling in de paginanavigatie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-page-link gsname="first|prev|next|last|viewall|viewpages"&gt;&lt;/guided-page-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Hiermee maakt u een koppeling naar de eerste, vorige, volgende of laatste pagina. Er kan ook een koppeling worden gemaakt om alle pagina's op één pagina weer te geven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-page-number /&gt; </span> </p> </td> 
   <td colname="col2"> <p> Retourneert een tekenreeks met het huidige paginanummer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if-page-selected&gt; 
      &lt;guided-else-page- 
      selected&gt; 
      &lt;/guided-if-page-selected&gt; </code> </p> </td> 
   <td colname="col2"> <p>Deze set voorwaardelijke tags is waar als de pagina is geselecteerd waarop momenteel wordt herhaald. Het wordt typisch gebruikt om het paginaaantal in de pagina-navigatie controle verschillend te tonen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-page-prev&gt; 
      &lt;guided-else-page- 
      prev&gt; 
      &lt;/guided-if[-not]-page-prev&gt; </code> </p> </td> 
   <td colname="col2"> <p> Deze set voorwaardelijke tags is true als de huidige pagina een vorige pagina heeft. Het wordt doorgaans gebruikt om een vorige koppeling in de paginanavigatie weer te geven wanneer dat zinvol is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-page-next&gt; 
      &lt;guided-else-page- 
      next&gt; 
      &lt;/guided-if[-not]-page-next&gt; </code> </p> </td> 
   <td colname="col2"> <p> Deze set voorwaardelijke tags is true als de huidige pagina een volgende pagina heeft. Het wordt doorgaans gebruikt om een vorige koppeling in de paginanavigatie weer te geven wanneer dat zinvol is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-page-viewall&gt; 
      &lt;guided-else-page- 
      viewall&gt; 
      &lt;/guided-if[-not]-page-viewall&gt; </code> </p> </td> 
   <td colname="col2"> <p> Wanneer een zoekopdracht een grote resultaatset oplevert, wilt u mogelijk niet alle resultaten weergeven. Daarom kunt u deze reeks voorwaardelijke markeringen gebruiken om te bepalen wanneer om de Mening te tonen Al verbinding. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-page-viewpages&gt; 
      &lt;guided-else-page- 
      viewpages&gt; 
      &lt;/guided-if[-not]-page-viewpages&gt; </code> </p> </td> 
   <td colname="col2"> <p>Met deze set voorwaardelijke tags kunt u bepalen wanneer de koppeling Pagina's weergeven wordt weergegeven. Dit wordt doorgaans gebruikt om een klant toe te staan bepaalde pagina's weer te geven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> 

    &amp;lt;guided-else-page-link&amp;gt;
    &amp;lt;/guided-if[-not]-page-link&amp;gt;   &lt;/p>  &lt;/td>
<td colname="col2"> <p>Hiermee wordt getest of de paginanavigatie een eerste pagina, vorige pagina, volgende pagina enzovoort bevat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-page-total /&gt; </span> </p> </td> 
   <td colname="col2"> <p> Retourneert een tekenreeks met het totale aantal pagina's met zoekresultaten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-pagination gsname= 
      "pagination_name"&gt;&lt;/guided-pagination&gt; </code> </p> </td> 
   <td colname="col2"> <p>Gebruik de <span class="codeph">-tag </span> voor met instructies-paginering om een gebied te definiëren waarin alle pagineringstags betrekking hebben op een specifieke pagineringsinstelling voor het geval er weinig instellingen voor paginanavigatie zijn gedefinieerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> 

    next|last|viewall|viewpages]/&amp;gt;   &lt;/p>  &lt;/td>
<td colname="col2"> <p>Hiermee maakt u een eigen koppeling in de paginanavigatie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-page-high-eq-last&gt; 
      &lt;guided-else-page- 
      high-eq-last&gt; 
      &lt;/guided-if-page-high-eq-last&gt; </code> </p> </td> 
   <td colname="col2"> <p>Hiermee wordt getest of de hoogste pagina in de paginanavigatie gelijk is aan het totale aantal pagina's. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-page-low-eq-first&gt; 
      &lt;guided-else-page-low-eq-first&gt; &lt;/guided-if-page-low-eq-first&gt; </code> </p> </td> 
   <td colname="col2"> <p>Hiermee wordt getest of de laagste pagina in de paginanavigatie gelijk is aan de laagste pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-page-is-multipage&gt; &lt;guided-else-page-is-multipage&gt; &lt;/guided-if-page-is-multipage&gt; </span> </p> </td> 
   <td colname="col2"> <p>Test of er één pagina met resultaten of meerdere pagina's met resultaten is. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Recente zoekopdrachten {#section_8CD907521F584257B475595B01A5964B}

U kunt recente zoekcodes gebruiken om een set koppelingen te maken waarmee een gebruiker snel een vorige zoekopdracht kan uitvoeren, zoals in het volgende voorbeeld:

```
<guided-if-recent-searches> 
    <span>Recent Searches</span><br/> 
    <guided-recent-searches> 
        <guided-recent-searches-link><guided-recent-searches-value></guided-recent-searches-link><br/> 
    </guided-recent-searches> 
    <guided-recent-searches-clear-link>Clear Recent Searches</guided-recent-searches-clear-link> 
</guided-if-recent-searches>
```

Zie [Recente zoekopdrachten configureren](../c-about-design-menu/t-configuring-recent-searches.md#task_E9E8ACA04C90484F8AFD5262167B2562).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-recent-searches&gt;&lt;/guided-recent-searches&gt; </span> </p> </td> 
   <td colname="col2"> <p>De lustag voor recente zoekopdrachten. Alle inhoud tussen de openingstag en de afsluitende tag wordt herhaald voor elke pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-recent-searches-link [attr="value"]+&gt; 
      &lt;/guided-recent-searches-link&gt; </code> </p> </td> 
   <td colname="col2"> <p>Hiermee kunt u een koppeling naar een recente zoekopdracht maken. Het ondersteunt het rechtstreeks doorgeven van HTML-kenmerken naar de ankertag. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-recent-searches-path /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Hiermee kunt u het relatieve URL-pad voor een recente zoekopdracht vastleggen in een <span class="codeph">-lus met instructies-recent doorzoeken </span>. Meestal gebruikt u <span class="codeph"> guided-recent-search-link </span>. Als u echter uw eigen koppeling wilt maken, kunt u deze tag gebruiken. Hieronder ziet u een voorbeeld: </p> <p> <code class="syntax html"> &lt;guided-lt/&gt;a&amp;nbsp;href="&lt;guided_recent_searches_path&gt;"&gt;&lt;guided-recent-searches-value&gt;&lt;/a&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-recent-searches-value&gt; </span> </p> </td> 
   <td colname="col2"> <p>Hiermee kunt u de queryterm vastleggen die aan een recente zoekopdracht is gekoppeld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-recent-searches-clear-link&gt;&lt;/guided-recent-searches-clear-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Hiermee kunt u uw klanten de mogelijkheid bieden om onlangs opgeslagen zoekopdrachten te wissen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-recent-searches-clear-path /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Retourneert het pad dat <span class="codeph"> &lt;guided-recent-search-clear-link&gt; </span> gebruikt, zodat u uw eigen koppeling kunt maken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 

    &amp;lt;/guided-if-recent-search&amp;gt;   &lt;/p>  &lt;/td>
<td colname="col2"> <p>Hiermee kunt u de recente zoekopdrachten weergeven wanneer een klant een recente zoekopdracht heeft uitgevoerd. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Bedoelde u {#section_C1EB3B9D8E1242798A6E04609D1E3543}

U kunt de tags Op maat maken gebruiken om een set koppelingen naar suggesties te maken wanneer een zoekopdracht geen resultaten oplevert en de zoekterm niet in het accountwoordenboek staat. Hieronder ziet u een voorbeeld van het gebruik van de labels Do You Mean:

```
<guided-if-suggestions> 
    <span>Did You Mean?</span><br/> 
    <guided-suggestions> 
        <guided-suggestion-link><guided-suggestion/></guided-suggestion-link><br/> 
    </guided-suggestions> 
</guided-if-suggestions>
```

Zie [Bedoelde u](../c-about-linguistics-menu/c-about-did-you-mean.md#concept_7D4F3C29EF184B538B8AE2ECAE0CDC5E).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matches search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-suggestions&gt;&lt;/guided-suggestions&gt; </span> </p> </td> 
   <td colname="col2"> <p>Dit is de lustag voor het doorlopen van de suggesties. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matches search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-suggestion-link&gt;&lt;/guided-suggestion-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Maakt een koppeling naar de opgegeven suggestie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Newly added from search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-suggestion-value /&gt; </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-suggestions&gt;&lt;guided-else[-not]- 
      suggestions&gt;&lt;/guided-if[-not]-suggestions&gt; </code> </p> </td> 
   <td colname="col2"> <p>Hiermee kunt u testen of er suggesties zijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-suggestion-path /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Retourneert de padtekenreeks naar de suggestie. U kunt het gebruiken om uw eigen ankermarkering te bouwen. In plaats daarvan wordt <span class="codeph"> guided-suggestie-link </span> gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-suggestion /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Een suggestie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-suggestion-result-count /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Resultaatbepaling voor de suggestie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-suggestion-autosearch&gt; 
      &lt;guided-else[-not]-suggestion-autosearch&gt; 
      &lt;/guided-if[-not]-suggestion-autosearch&gt; </code> </p> </td> 
   <td colname="col2"> <p>Hiermee kunt u testen of automatisch zoeken op suggestie is uitgevoerd op nul resultaten, voor het geval deze functie is ingeschakeld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-suggestion-original-query /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Retourneert de oorspronkelijke query als autosearch is uitgevoerd. </p> <p>Voorbeeld van het gebruik: </p> <p> <code class="syntax html"> &lt;guided-if-suggestion-autosearch&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;Search&nbsp;for&nbsp;&lt;guided-query-param&nbsp;gsname="q"&nbsp;/&gt;&nbsp;instead&nbsp;of&nbsp;&lt;guided-suggestion-original-query&nbsp;/&gt; 
      &lt;/guided-if-suggestion-autosearch&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-suggestion-low-results&gt; 
      &lt;guided-else[-not]-suggestion-low-results&gt; 
      &lt;/guided-if[-not]-suggestion-low-results&gt; </code> </p> </td> 
   <td colname="col2"> <p>Deze voorwaarde geldt als er suggesties zijn die te wijten zijn aan een laag aantal resultaten, voor het geval deze functie is ingeschakeld. </p> <p>Hieronder ziet u een voorbeeld van het gebruik van deze tag: </p> <p> <code class="syntax html"> &lt;guided-if-suggestion-low-results&gt; 
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

Met de volgende codes kunt u automatisch aanvullen toevoegen aan uw zoekformulier. De kopinhoud en de tags voor de inhoud van het formulier zijn vereist om de functie Automatisch aanvullen correct uit te voeren. U wordt aangeraden de labels te gebruiken in plaats van de automatisch aangevulde JavaScript- en CSS-tags in uw presentatiesjabloon te coderen. De reden hiervoor is dat tags het mogelijk maken dat uw sjablonen nieuwe cache-id&#39;s ophalen wanneer u de instellingen voor automatisch aanvullen wijzigt zonder dat u de sjabloon handmatig hoeft bij te werken.

Zie [Over automatisch aanvullen](../c-about-auto-complete.md#concept_093A9CD754864BA79B456FE4BEB64578).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-autocomplete&gt; &lt;guided-else-autocomplete&gt; &lt;/guided-if-autocomplete&gt; </span> </p> </td> 
   <td colname="col2"> <p>Detecteert of de functie Automatisch aanvullen is ingeschakeld. U kunt de codes gebruiken om desgewenst de kop- en formulierinhoud op te halen die vereist is voor automatisch aanvullen. Hierdoor kunt u de functie in- en uitschakelen en hoeft u de presentatiesjablonen niet te wijzigen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-ac-css /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Wordt gebruikt in de kop van de presentatiesjabloon en wordt vervangen door het desbetreffende CSS-script voor automatisch aanvullen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-ac-form-content /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Wordt gebruikt in het zoekformulier (tussen de <span class="codeph"> &lt;form&gt; </span>- en <span class="codeph"> &lt;/form&gt; </span>-tags) van de presentatiesjabloon in plaats van de automatische aanvulcodes in het formulier op de vaste wijze te coderen. De tags worden vervangen door de juiste HTML die is vereist om automatisch aanvullen te laten werken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-ac-javascript /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Hiermee worden de koppelingen naar JavaScript automatisch aanvullen gegenereerd. Voor de beste prestaties is het raadzaam deze tag onder aan de pagina vóór de afsluitende tag 'body' te plaatsen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## {#section_A33E25DB5E67404A823BD9618665B773} opslaan

Gebruik de volgende labels om de winkel waarin een gebruiker zich momenteel bevindt, te testen en weer te geven.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-store /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Hiermee wordt de huidige winkel uitgevoerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-store-defined&gt; &lt;guided-else-store-defined&gt; &lt;/guided-if-store-defined&gt; </span> </p> </td> 
   <td colname="col2"> <p>Detecteert of de gebruiker zich in een winkel bevindt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-store gsname="store"&gt; &lt;guided-else-store&gt; &lt;/guided-if-store&gt; </span> </p> </td> 
   <td colname="col2"> <p>Detecteert of de gebruiker zich in de opslag bevindt die door de parameter <span class="codeph"> gsname </span> wordt opgegeven. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Gebieden {#section_B9B3179E000C42D492E1541F2FE44CB5}

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-zone gsname="zone area"&gt; </span> </p> </td> 
   <td colname="col2"> <p>U kunt inhoud in zonetags laten omlopen om een zone buiten dat gebied te maken. Dit laat u bedrijfsregels gebruiken om de streek te tonen zoals nodig. Standaard worden zones altijd weergegeven. U kunt de optionele parameters search en facet gebruiken om aan te geven welke zoekopdracht of facet aan de zone is gekoppeld. Met deze functionaliteit kan de software zoekopdrachten of facetten overslaan wanneer een zone verborgen is, waardoor de zoekprestaties verbeteren. De hoogte en breedtekenmerken zijn facultatief en worden gebruikt om te vormen hoe placeholder in de Visuele Bouwer van de Regel wordt getoond wanneer een streek wordt verwijderd. </p> <p> Gebruik, waar mogelijk, de <span class="codeph">-tag met instructies-if-facet[-not]-visible </span> in plaats van de zone. De presentatiesjabloon wordt vereenvoudigd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-zone gsname="zone area"&gt; &lt;guided-else-zone&gt; &lt;/guided-if-zone&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze reeks markeringen laat het testen als een streek momenteel wordt getoond toe. Het is handig als u elders op de pagina inhoud hebt die u alleen wilt weergeven als de zone wordt weergegeven. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Lus-indicatoren {#section_387322CA0AA843A2ACF2795C328673E9}

U kunt elk van de volgende lusindicatoren in om het even welk van deze lusjeblokken gebruiken:

* geleide resultaten
* geleide-facetwaarden
* met instructies-breadcrumb
* menu-items met instructies
* geleide pagina&#39;s

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-first&gt;&lt;guided-else[-not]-first&gt; 
      &lt;/guided-if[-not]-first&gt; </code> </p> </td> 
   <td colname="col2"> <p>Deze voorwaarde is waar wanneer de huidige herhaling de eerste herhaling van de lijn is. Dat betekent niet noodzakelijkerwijs het eerste resultaat of de eerste pagina, maar de eerste weergegeven pagina. Als de sitebezoeker zich op pagina 2 bevindt van een resultatenset van 10 per pagina, is de eerste iteratie resultaat 11. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-last&gt;&lt;guided-else[-not]-last&gt; 
      &lt;/guided-if[-not]-last&gt; </code> </p> </td> 
   <td colname="col2"> <p>Deze voorwaarde is waar wanneer de huidige herhaling de laatste herhaling van de lijn is. Dat betekent niet noodzakelijkerwijs het laatste resultaat of de laatste pagina, maar de laatste die in de huidige context (pagina) wordt getoond. Als de bezoeker van de site zich op pagina 1 bevindt van een resultatenset die 200 resultaten bevat maar slechts 10 resultaten per pagina bevat, is de laatste herhaling resultaat 10 in plaats van resultaat 200. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-odd&gt;&lt;guided-else[-not]-odd&gt; 
      &lt;/guided-if[-not]-odd&gt; </code> </p> </td> 
   <td colname="col2"> <p>Deze voorwaarde is waar wanneer de huidige herhaling een oneven herhaling van de lijn (tegenover een even herhaling) is. Dit is handig voor het weergeven van verschillende rijkleuren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-even&gt;&lt;guided-else[-not]-even&gt; 
      &lt;/guided-if[-not]-even&gt; </code> </p> </td> 
   <td colname="col2"> <p>Deze voorwaarde is waar wanneer de huidige iteratie een even herhaling van de lijn (tegenover een oneven herhaling) is. Dit is handig voor het weergeven van verschillende rijkleuren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-alt&gt;&lt;guided-else[-not]-alt&gt; 
      &lt;/guided-if[-not]-alt&gt; </code> </p> </td> 
   <td colname="col2"> <p>Deze voorwaarde is waar wanneer de huidige herhaling een gelijke herhaling van de lijn is. Dit is handig voor het weergeven van verschillende rijkleuren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-inner&gt;&lt;guided-else[-not]-inner&gt; 
      &lt;/guided-if[-not]-inner&gt; </code> </p> </td> 
   <td colname="col2"> <p>Hiermee neemt u de tekst tussen de koppelingen op als de huidige herhaling noch de eerste, noch de laatste is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-outer&gt;&lt;guided-else[-not]-outer&gt; 
      &lt;/guided-if[-not]-outer&gt; </code> </p> </td> 
   <td colname="col2"> <p>Hiermee neemt u de tekst tussen de koppelingen op als de huidige herhaling de eerste of de laatste is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-loop-index&gt; </span> </p> </td> 
   <td colname="col2"> <p>Een geheel getal (te beginnen bij 0) waarvan de waarde voor elke herhaling van de lus wordt verhoogd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-loop-counter&gt; </span> </p> </td> 
   <td colname="col2"> <p>Een geheel getal (vanaf 1) waarvan de waarde voor elke herhaling van de lus wordt verhoogd. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Diverse talen {#section_BFE8DC98E26F4D7BB60FEC54D9A5DC6C}

De volgende labels zijn beschikbaar zodat u meer geavanceerde dingen kunt doen met uw sjabloon, zoals het bouwen van uw eigen minifacet.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng, 2/1/2013--> <span class="codeph"> &lt;guided-current-path&gt; </span> </p> </td> 
   <td colname="col2"> <p>Geeft u het huidige pad dat wordt gebruikt. Doorgaans wordt het gebruikt om een koppeling te maken die een nieuwe parameter aan de bestaande zoekopdracht toevoegt. Standaard is het pad URL met escape-teken. U kunt opgeven welke modus voor escape-tekens u wilt gebruiken via de parameter escape. </p> <p>Voorbeeld: </p> <p> <code class="syntax html"> &lt;a&nbsp;href="&lt;guided-current-path&nbsp;/&gt;&amp;lang=fr"&gt; 
      French&nbsp;Version </code> </p> <p>In dit voorbeeld gebruikt een regel voor zoekverwerking lang om de Franse versie te selecteren. </p> <p>Het huidige pad heeft altijd ten minste één queryparameter. Als er geen andere queryparameters bestaan, wordt deze ingesteld op <span class="codeph"> q=* </span> om het gemakkelijker te maken om meer parameters toe te voegen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> Basispad  </span> </p> </td> 
   <td colname="col2"> <p> Als u een koppeling wilt maken met behulp van het basispad, gebruikt u <span class="codeph"> / </span> aan het begin van uw <span class="codeph"> href </span> en voegt u parameters toe. </p> <p> <code class="syntax html"> &lt;a&nbsp;href="/"&gt;All&nbsp;Products&lt;/a&gt; 
      Would&nbsp;create&nbsp;a&nbsp;link&nbsp;"All&nbsp;Products"&nbsp;to&nbsp;your 
      basepath,&nbsp;for&nbsp;example&nbsp;https://search.mycompany.com/ 
       </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng, 2/1/2013--> <span class="codeph"> &lt;guided-query-param gsname="query_parameter"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Hiermee kunt u de bestaande waarde ophalen van een queryparameter die zich op de URL bevindt. Als de parameter niet bestaat, wordt met deze tag een lege tekenreeks geretourneerd. Als u geen escape-optie opgeeft, wordt de geretourneerde tekenreeks automatisch als HTML-escape weergegeven, kunt u HTML- of URL-escape opgeven. </p> <p>Voorbeeld: </p> <p> 

    &amp;lt;guided-query-param&amp;nbsp;gsname=&quot;q&quot;&amp;nbsp;/&amp;gt;
    giving&amp;nbsp;u&amp;nbsp;the&amp;nbsp;value&amp;nbsp;broek
    
    &amp;lt;guided-query-param&amp;nbsp;gsname=&quot;lang&quot;&amp;nbsp;/&amp;gt;
    wegens&amp;nbsp;u &amp;nbsp;the&amp;nbsp;value&amp;nbsp;en
    
    &amp;lt;guided-query-param&amp;nbsp;gsname=&quot;test&quot;&amp;nbsp;/&amp;gt;
    geeft&amp;nbsp;u&amp;nbsp;an&amp;nbsp;empty&amp;nbsp;string
    &amp;nbsp;
    &amp;nbsp;&amp;nbsp; &amp;nbsp; nbsp;&amp;nbsp;   &lt;/p>  &lt;/td>
</tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-query-param-name gsname="param#" offset="offset_number" /&gt; </span> </p> </td> 
   <td colname="col2"> <p>De Begeleide Onderzoek heeft het begrip van een vraagaantal, dat in de broodkruimelecontrole wordt gebruikt. <span class="codeph"> Met guided-query-param-name  </span> kunt u parameters definiëren als onderdeel van een koppeling in de presentatiesjabloon waarin Met instructies zoeken het juiste querynummer voor u wordt weergegeven. De <span class="codeph"> gsname </span> heeft een "x"in het, die Geleide Onderzoek met het correcte aantal vervangt. De verschuivingswaarde kan 0 - 15 zijn, waarbij 0 aangeeft dat het volgende beschikbare querynummer wordt gebruikt. A1 geeft aan dat u er 1 aan wilt toevoegen, enzovoort. </p> <p>Gecombineerd met <span class="codeph"> geleide-huidige-weg </span>, kunt u uw eigen mini facetverbinding bouwen of een extra boor-benedenniveau toestaan. </p> <p>Voorbeeld: </p> <p> <code class="syntax html"> &lt;a&nbsp;href="&lt;guided-current-path 
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
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-include gsfile="filename" /&gt; </span> </p> </td> 
   <td colname="col2"> <p> Hiermee kunt u andere sjabloonbestanden opnemen. Deze functionaliteit betekent dat u meerdere sjablonen kunt maken met subsjablonen als modules. </p> <p>In het volgende voorbeeld worden de <span class="filepath"> breadcrumbs </span> en <span class="filepath"> facetten </span> bestanden opgenomen: </p> <p> <code class="syntax html"> &lt;guided-include&nbsp;gsfile='breadcrumbs.tmpl'&nbsp;/&gt; 
      &lt;guided-include&nbsp;gsfile='facets.tmpl'&nbsp;/&gt; </code> </p> <p>Dynamische include-bestanden worden niet ondersteund. Met andere woorden: <span class="codeph"> gsfile </span> kan geen variabele zijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW 1/17/2013--> <span class="codeph"> &lt;guided-search-time&gt; </span> </p> </td> 
   <td colname="col2"> <p> Hiermee wordt aangegeven hoe lang de zoekopdracht heeft geduurd. De geretourneerde waarde voor de zoektijd wordt opgegeven in ms. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW 1/17/2013--> <span class="codeph"> &lt;guided-fall-through-searches&gt; </span> </p> </td> 
   <td colname="col2"> <p> Retourneert het aantal zoekopdrachten in kernen dat wordt gebruikt om de pagina met zoekresultaten samen te stellen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW 1/17/2013--> <span class="codeph"> &lt;guided-if-fall-through-search&gt;&lt;/guided-if-fall-through-search&gt; </span> </p> </td> 
   <td colname="col2"> <p>Test of het aantal kernzoekopdrachten groter is dan één. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-even&gt;&lt;guided-else[-not]-even&gt; 
      &lt;/guided-if[-not]-even&gt; </code> </p> </td> 
   <td colname="col2"> <p>Deze voorwaarde is waar wanneer de huidige iteratie een even herhaling van de lijn (tegenover een oneven herhaling) is. Dit is handig voor het weergeven van verschillende rijkleuren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-alt&gt;&lt;guided-else[-not]-alt&gt; 
      &lt;/guided-if[-not]-alt&gt; </code> </p> </td> 
   <td colname="col2"> <p>Deze voorwaarde is waar wanneer de huidige herhaling een gelijke herhaling van de lijn is. Dit is handig voor het weergeven van verschillende rijkleuren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-inner&gt;&lt;guided-else[-not]-inner&gt; 
      &lt;/guided-if[-not]-inner&gt; </code> </p> </td> 
   <td colname="col2"> <p>Hiermee neemt u de tekst tussen de koppelingen op als de huidige herhaling noch de eerste, noch de laatste is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-outer&gt;&lt;guided-else[-not]-outer&gt; 
      &lt;/guided-if[-not]-outer&gt; </code> </p> </td> 
   <td colname="col2"> <p>Hiermee neemt u de tekst tussen de koppelingen op als de huidige herhaling de eerste of de laatste is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-first-search&gt;&lt;guided-else-first-search&gt; 
      &lt;/guided-if-first-search&gt; </code> </p> </td> 
   <td colname="col2"> <p>Hiermee kunt u controleren of de oorspronkelijke zoekopdracht wordt uitgevoerd (de zoekopdracht is het resultaat van een zoekopdracht in het zoekvak). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-search-url /&gt; </span> </p> </td> 
   <td colname="col2"> <p>U kunt deze tag in de sjabloon gebruiken om de hardcodering van de actie van het zoekformulier te voorkomen. Het detecteert wanneer u zich in de Stage- of Live-omgeving bevindt en wijzigt dienovereenkomstig. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-query-param-defined gsname="query_parameter"&gt; &lt;guided-else-query-param-defined&gt; &lt;/guided-if-query-param-defined&gt; </span> </p> </td> 
   <td colname="col2"> <p>Met deze set labels kunt u testen welke CGI-parameters zijn gedefinieerd in het zoekpad. U kunt de waarden van de parameters alleen testen als deze zijn gedefinieerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-next-query-number&gt; </span> </p> </td> 
   <td colname="col2"> <p>De zoekengine met instructies die de sjabloon aandrijft, heeft het idee van zwevende querynummers waar elke nieuwe koppeling die de engine genereert, het volgende beschikbare querynummer gebruikt. Met deze tag kunt u het volgende querynummer of de volgende verschuivingen ophalen, zodat u aangepaste koppelingen kunt maken die naar de resultatenset gaan. Met Verschuiving kunt u verschuiven naar het volgende querynummer. Bijvoorbeeld, als u één facet hebt geselecteerd, is het volgende vraagaantal 2, met een compensatie van 1 het teruggekeerde vraagaantal is 3. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-custom-var gsname="custom_variable"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Hiermee kunt u de bestaande waarde vastleggen van een aangepaste variabele die uw verwerkingsregels definiëren. Als u geen escape-optie opgeeft, wordt de geretourneerde tekenreeks automatisch HTML escape-teken, kunt u <span class="codeph"> html </span>, <span class="codeph"> url </span>, <span class="codeph"> js </span> of <span class="codeph"> 0 </span> opgeven. Als u een verwerkingsregel gebruikt om een inkomende parameter van CGI aan een douanevariabele te kopiëren en dan die variabele in uw malplaatje te tonen of te gebruiken met ontsnapt aan niets of js wordt geplaatst, dan kunt u een kwetsbaarheid XSS in uw onderzoek tot stand brengen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-custom-var-defined gsname="custom_variable"&gt; &lt;guided-else-custom-var-defined&gt; &lt;/guided-if-custom-var-defined&gt; </span> </p> </td> 
   <td colname="col2"> <p>Laat het testen toe als een douanevariabele in de verwerkingsregels (vraagreiniging, pre-onderzoek verwerking en post-onderzoek verwerking) wordt bepaald. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>19 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-general-field gsname="searchname" field="fieldname"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Hiermee kunt u de inhoud weergeven van een algemeen veld dat is gedefinieerd in de transportsjabloon. Als u geen escape-optie opgeeft, wordt de geretourneerde tekenreeks gecodeerd in de indeling die u in de transportsjabloon voor dat veld hebt opgegeven. Het specificeren van een ontsnappingsoptie is van toepassing bovenop welk formaat u het gebied zoals in uw vervoermalplaatje codeert. U kunt <span class="codeph"> html </span>, <span class="codeph"> url </span>, <span class="codeph"> js </span>, <span class="codeph"> json </span>, of <span class="codeph"> 0 </span> specificeren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>20 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-general-field gsname="searchname" field="fieldname"&gt; &lt;guided-else-general-field&gt; &lt;/guided-if-general-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>Laat het testen toe als de inhoud van een algemeen gebied, zoals die in het vervoermalplaatje wordt bepaald, bestaat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>21 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-cookie-value gsname="cookie_name"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Hiermee kunt u de waarde van een cookie ophalen, ervan uitgaande dat de cookie beschikbaar is. Als u geen escape-optie opgeeft, wordt de tekenreeks automatisch HTML escape-teken geretourneerd, kunt u <span class="codeph"> html </span>, <span class="codeph"> url </span>, <span class="codeph"> js </span>, <span class="codeph"> json </span> of <span class="codeph"> 0 </span> opgeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>22 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-cookie gsname="cookie_name"&gt; &lt;guided-else-cookie&gt; &lt;/guided-if-cookie&gt; </span> </p> </td> 
   <td colname="col2"> <p>Hiermee kunt u testen of een cookie bestaat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>23 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-banner gsname="banner area"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Hiermee wordt de banner voor een bepaald gebied uitgevoerd. De facultatieve breedte en hoogtekenmerken worden gebruikt in de Visuele Bouwer van de Regel om de vertoning van een zinvolle plaats-houder toe te laten om gebruikers een banner te laten selecteren. Standaard worden banners niet beschermd. In plaats daarvan wilt u HTML in de presentatiesjabloon injecteren. Als u echter een JSON-sjabloon maakt, kunt u de optie JS escape gebruiken. </p> <p>Voorbeeld: </p> <p> <code class="syntax html"> &lt;guided-banner&nbsp;gsname="top"&nbsp;width="400px" 
      &nbsp;height="50px"/&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>24 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-banner-set gsname="banner area"&gt; &lt;guided-else-banner-set&gt; &lt;/guided-if-banner-set&gt; </span> </p> </td> 
   <td colname="col2"> <p>Hiermee schakelt u testen in als een bannergebied is ingesteld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>25 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-simulator-mode&gt; &lt;guided-else-simulator-mode&gt; &lt;/guided-if-simulator-mode&gt; </span> </p> </td> 
   <td colname="col2"> <p>Laat u ontdekken wanneer u uw onderzoek in Simulator of de Visuele Bouwer van de Regel bekijkt. Het wordt normaal gebruikt om extra te tonen zuivert informatie voor u. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>26 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-tnt-business-rules&gt; &lt;guided-else-tnt-business-rules&gt; &lt;/guided-if-tnt-business-rules&gt; </span> </p> </td> 
   <td colname="col2"> <p>Hiermee kunt u detecteren of er bedrijfsregels zijn die verwijzen naar een <span class="keyword"> Adobe Target </span>-campagne. Het wordt gewoonlijk gebruikt als onderdeel van de integratie met <span class="keyword"> Adobe Target </span> om te voorkomen dat de <span class="keyword"> Target </span>-servers worden geraakt wanneer dit niet nodig is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>27 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-redirect /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Standaard worden omleidingen automatisch uitgevoerd. Als u echter de zoekfunctie/merchandising van sites hebt geconfigureerd om een XML- of JSON-reactie op uw webtoepassing te retourneren, kunt u de 302/301-reactie parseren in uw webtoepassing of de omleiding laten doorgeven als onderdeel van de resultatenset. Als u de omleiding doorgeeft als onderdeel van de resultatenset, kan deze tag in de sjabloon worden gebruikt om de omleidingslocatie uit te voeren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>28 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-redirect&gt; &lt;guided-else-redirect&gt; &lt;/guided-if-redirect&gt; </span> </p> </td> 
   <td colname="col2"> <p>Wanneer u plaatsonderzoek/handel hebt gevormd om redirects in de resultaatreeks terug te keren, kan deze reeks markeringen worden gebruikt om te bepalen als er redirect aan output is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>29 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-lt /&gt; &lt;guided-gt /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Met deze set tags kunt u Geleide sjabloontags insluiten in HTML-kenmerken. </p> <p>Voorbeeld: </p> <p> <code class="syntax html"> &lt;guided-lt/&gt;div&nbsp;&lt;guided-if-facet-long&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;style="height:&nbsp;125px;&nbsp;overflow: 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;auto;"&lt;/guided-if-facet-long&gt;&lt;guided-gt/&gt; </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Labels {#reference_227D199F5A7248049BE1D405C0584751} voor transportsjablonen

De malplaatjes van het vervoer zijn de malplaatjes van XML die gegevens van het achterste eind onderzoek tot de Geleide presentatielaag van het Onderzoek overgaan.

<!-- 

r_transport_template_tags.xml

 -->

In uw presentatielaag kunt u één presentatiesjabloon gebruiken waarin de resultaten van meerdere zoekopdrachten worden weergegeven. Elke zoekopdracht kan dezelfde transportsjabloon of een aangepaste transportsjabloon gebruiken om de gegevens door te geven aan de presentatielaag.

Omdat het vervoermalplaatje slechts wordt gebruikt om gegevens tot de presentatielaag over te gaan, heeft het geen HTML die met het tonen van de onderzoeksresultaten betrokken is. De vervoermalplaatje gebruikt de markeringen van XML van het vervoermalplaatje om de onderzoeksresultaten voor het bevolken van de Geleide componenten van het Onderzoek, zoals facetten, broodkruimels, en menu&#39;s over te gaan. Binnen deze tags worden standaardtags voor zoeksjablonen gebruikt om de werkelijke waarden weer te geven.

Zie [Een presentatie of een transportsjabloon bewerken](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3).

Zie [Sjabloontags zoeken](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4).

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Tag voor transportsjabloon </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-xml&gt;&lt;/guided-xml&gt; </span> </p> </td> 
   <td colname="col2"> <p>De wortelXML markeringen die de presentatielaag gebruikt om te ontdekken wat uit het vervoermalplaatje wordt ontleed. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;general&gt;&lt;/general&gt; </span> </p> </td> 
   <td colname="col2"> <p>Tags rondom zoekopdrachtsjabloontags met samenvattingsgegevens op basis van de resultatenset. Deze tags bevatten meestal zoekcodes voor het totale aantal resultaten, het lagere resultaat en het hoogste resultaat. U kunt elk gewenst aantal aanvullende globale velden definiëren met de <span class="codeph">-tag general-field </span>, zoals in het volgende voorbeeld: </p> <p> <code class="syntax html"> &lt;general&gt; 
      &nbsp;&nbsp;&lt;total&gt;&lt;search-total&nbsp;/&gt;&lt;/total&gt; 
      &nbsp;&nbsp;&lt;lower&gt;&lt;search-lower&nbsp;/&gt;&lt;/lower&gt; 
      &nbsp;&nbsp;&lt;upper&gt;&lt;search-upper&nbsp;/&gt;&lt;/upper&gt; 
      &nbsp;&nbsp;&lt;general-field&nbsp;name="my_custom_field"&gt;Some&nbsp;global&nbsp;content&lt;/general-field&gt; 
      &lt;/general&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;results&gt;&lt;/results&gt; </span> </p> </td> 
   <td colname="col2"> <p>Tags worden rondom de zoekresultaten geplaatst, zodat de zoekfunctie met instructies weet waar ze naartoe moeten zoeken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;result&gt;&lt;/result&gt; </span> </p> </td> 
   <td colname="col2"> <p>Tags worden rondom elk zoekresultaat geplaatst, zodat met instructies wordt herkend waar de inhoud voor één zoekresultaat begint en eindigt, zoals in het volgende voorbeeld: </p> <code class="syntax html"> &lt;results&gt; 
     &nbsp;&nbsp;&lt;search-results&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;result&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;index&gt;&lt;search-index&nbsp;/&gt;&lt;/index&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;loc&gt;&lt;search-cdata&gt;&lt;search-url&nbsp;length="500"&nbsp;/&gt;&lt;/search-cdata&gt;&lt;/loc&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;/result&gt; 
     &nbsp;&nbsp;&lt;/search-results&gt; 
     &lt;/results&gt; </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;attribute-table name="tablename"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Hiermee kunt u elk item in een lijst met meerdere waarden doorlopen voor één resultaat. Gebruik deze tag alleen binnen een resultaat. Het doel is om u over attributen te laten herhalen die tot een resultaatgebied behoren, zoals in het volgende voorbeeld: </p> <code class="syntax html"> &lt;results&gt; 
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
   <td colname="col1"> <p> <span class="codeph"> &lt;facets&gt;&lt;/facets&gt; </span> </p> </td> 
   <td colname="col2"> <p>Geeft de resultaten door die de facetten vullen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 
     <!--NEW 2/27/2014--> <span class="codeph"> &lt;dynamic-facet&gt;&lt;/dynamic-facet&gt; </span> </p> </td> 
   <td colname="col2"> <p> U kunt een facet aanwijzen als zowel een dynamisch facet als een lid van een facetrail. De behandeling ervan is echter onafhankelijk van de gerelateerde sjablooncodes voor presentaties. </p> <p>Met andere woorden, het nesten van een facetspoorloopingcontext binnen een dynamische facetloopingcontext, of vice versa, is niet toegestaan. </p> <p>Voor facetten die zowel dynamisch als geklonterd zijn, zijn slechts die dynamische facetten die voor een bepaalde onderzoek werden teruggekeerd zichtbaar binnen de facetspoorloopingcontext. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;facet name="name"&gt;&lt;/facet&gt; </span> </p> </td> 
   <td colname="col2"> <p> Elke facet heeft zijn eigen facetmarkeringen waar de naamparameter de facetnaam aanpast. Zoekcodes worden gebruikt binnen de facettags voor de waarden van facetten, zoals in het volgende voorbeeld: </p> <code class="syntax html"> &lt;facets&gt; 
     &nbsp;&nbsp;&lt;facet&nbsp;name="brand"&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;values&gt;&lt;search-field-value-list&nbsp;name="brand"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/values&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;counts&gt;&lt;search-field-value-list&nbsp;name="brand"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="counts"&nbsp;sortby="values"&nbsp;/&gt;&lt;/counts&gt; 
     &nbsp;&nbsp;&lt;/facet&gt; 
     &nbsp;&nbsp;&lt;facet&nbsp;name="category"&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;values&gt;&lt;search-field-value-list&nbsp;name="category"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/values&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;counts&gt;&lt;search-field-value-list&nbsp;name="category"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="counts"&nbsp;sortby="values"&nbsp;/&gt;&lt;/counts&gt; 
     &nbsp;&nbsp;&lt;/facet&gt; 
     &lt;/facets&gt; </code> <p> Voor accounts die gebruikmaken van een steunkleur, kunnen de tag dynamic en de tag display-names worden gebruikt. Beide tags helpen u bij het maken van bedrijfsregels de koppeling tussen bepaalde facetten en echte facetten te vergemakkelijken. </p> <code class="syntax html"> &lt;facets&gt; 
     &nbsp;&nbsp;&lt;facet&nbsp;name="facet_values01"&gt; 
     &nbsp;&lt;dynamic&gt;1&lt;/dynamic&gt; 
     &nbsp;&lt;display-names&gt;&lt;search-field-value-list&nbsp;name="facet_names01"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/display-names&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;values&gt;&lt;search-field-value-list&nbsp;name="facet_values01"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/values&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;counts&gt;&lt;search-field-value-list&nbsp;name="facet_values01"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="counts"&nbsp;sortby="values"&nbsp;/&gt;&lt;/counts&gt; 
     &nbsp;&nbsp;&lt;/facet&gt; </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field separator=","&gt; </span> </p> </td> 
   <td colname="col2"> <p>Met het <span class="codeph">-scheidingsteken </span> kunt u het scheidingsteken wijzigen dat wordt gebruikt wanneer u zoek-display-veldgegevens voor lijsten uitvoert. De standaardwaarde is een komma. </p> <p>Over het algemeen moet het scheidingsteken dat u gebruikt iets zijn dat niet gemakkelijk in de inhoud van het veld wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;suggestions&gt;&lt;/suggestions&gt; </span> </p> </td> 
   <td colname="col2"> <p> Plaats uw Bedoelde u suggesties met markeringen zodat Geleide Onderzoek herkent welke knopen van XML suggesties bevatten. </p> <p>Zie <a href="../c-about-linguistics-menu/c-about-did-you-mean.md#concept_7D4F3C29EF184B538B8AE2ECAE0CDC5E" type="concept" format="dita" scope="local"> Info Bedoelde u</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;suggestion&gt;&lt;/suggestion&gt; </span> </p> </td> 
   <td colname="col2"> <p>Bedoelt u elk met labels, zoals in het volgende voorbeeld: </p> <code class="syntax html"> &lt;search-if-suggestions&gt; 
     &nbsp;&nbsp;&lt;suggestions&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;search-suggestions&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;suggestion&gt;&lt;search-suggestion-text&nbsp;/&gt;&lt;/suggestion&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-suggestions&gt; 
     &nbsp;&nbsp;&lt;/suggestions&gt; 
     &lt;/search-if-suggestions&gt; </code> <p>Zie <a href="../c-about-linguistics-menu/c-about-did-you-mean.md#concept_7D4F3C29EF184B538B8AE2ECAE0CDC5E" type="concept" format="dita" scope="local"> Info Bedoelde u</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Sjabloontags zoeken {#reference_F7AA3FF602314E42842BBC740D2CA1A4}

Een zoeksjabloon is een HTML-bestand dat sjabloontags bevat die worden gedefinieerd door zoeken/verhandelen van sites. Deze tags geven aan hoe de zoekresultaten zijn opgemaakt. De volgende naslaggids bevat een korte beschrijving van elke zoeksjabloontag en de bijbehorende kenmerken.

<!-- 

r_search_template_tags.xml

 -->

>[!NOTE]
>
>Gebruik alleen sjabloontags voor zoekopdrachten in transportsjabloonbestanden (.tpl).

U kunt uit de volgende de markeringsgroepen en verwijzingsmateriaal van het onderzoeksmalplaatje selecteren.

Tags die alleen binnen de resultatenlus geldig zijn, zijn onder andere:

* [Over Resultaten-lustags](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629)
* [Resultaten van reekscodes](../c-appendices/c-templates.md#section_80D68334E8D04A33937A6E58ABAAA320)
* [Resultaten voorwaardelijke tags in lus](../c-appendices/c-templates.md#section_35C367969E384A06A9865E388F1F9360)
* [Resultaten koppelingstags voor herhalen](../c-appendices/c-templates.md#section_C5FAEF520E9E42ADAD1F90651922AA02)
* [Voorwaardelijke tags voor positie herhalen](../c-appendices/c-templates.md#section_E0C29DDA09E043C9A396F36334F05EBB)

Tags die geldig zijn in de gehele sjabloon, zijn onder andere:

* [Lijstlabels voor veldwaarden](../c-appendices/c-templates.md#section_D3298B5F976447DBA0032B883DCC91B1)
* [Lijstlabels voor veldwaarden](../c-appendices/c-templates.md#section_0717FA09F0FC449CB916883B0500A60E)
* [Tags voorstellen](../c-appendices/c-templates.md#section_C28EB8B4F7DC4E278A0F143BCFEEB1AC)
* [Tags voor sjabloonreeksen](../c-appendices/c-templates.md#section_67E3D529661F4F03A1FF469D9D658CAF)
* [Koppelingstags voor sjabloonanker](../c-appendices/c-templates.md#section_3A51D27616C541E2B818CC52B2B856BA)
* [Voorwaardelijke tags sjabloon](../c-appendices/c-templates.md#section_18D9BC66DE484881932FD2F7EA9D170D)
* [Tags voor formulierbeheer](../c-appendices/c-templates.md#section_45AFC414ACA74825B72FEAA8456F8DD2)

Zoeksjabloonverwijzingsonderwerpen

* [Tekenreeksen datumnotatie](../c-appendices/c-templates.md#section_4BBDBBEF2B96414497617CD4B52D96E4)
* [Taalid&#39;s](../c-appendices/c-templates.md#section_0490DECC00E34691ADE5A9ED90A6D911)
* [De HTTP-header van het inhoudstype opgeven](../c-appendices/c-templates.md#section_AEED823E9938448A9EDB2F286D9CFD90)
* [Een tekenset opgeven in een HTML-sjabloon](../c-appendices/c-templates.md#section_E0D1816ABB5846BEBE9C26D5980CCBE6)
* [Een tekenset opgeven in een XML-sjabloon](../c-appendices/c-templates.md#section_17DC31CDCC104F5F8081466B41A96E9D)
* [Een zoeksjabloon opnemen in een andere sjabloon](../c-appendices/c-templates.md#section_7D1FCD3D9E2340C291E354C9720E8BC0)

## Over Resultaten-luscodes {#section_D4DC7B4560144663972E8DBC3369C629}

De resultatenlustag is het werkpaard van het sjabloonsysteem. Wanneer de tag tijdens een zoekopdracht wordt aangetroffen, wordt de HTML herhaald en worden andere tags tussen de tags voor de begin- en eindresultatenlus geplaatst, waarbij eventuele andere tags worden vervangen door uw zoekresultaten.

`<search-results> ... </search-results>`

De resultatenlustags staan rondom de HTML die de zoekresultaten weergeeft. De HTML tussen de labels wordt voor elk resultaat herhaald en wordt op de pagina weergegeven.

De volgende tags zijn alleen geldig in de resultatenlus:

* [Resultaten van reekscodes](../c-appendices/c-templates.md#section_80D68334E8D04A33937A6E58ABAAA320)
* [Resultaten voorwaardelijke tags in lus](../c-appendices/c-templates.md#section_35C367969E384A06A9865E388F1F9360)
* [Resultaten koppelingstags voor herhalen](../c-appendices/c-templates.md#section_C5FAEF520E9E42ADAD1F90651922AA02)
* [Voorwaardelijke tags voor positie herhalen](../c-appendices/c-templates.md#section_E0C29DDA09E043C9A396F36334F05EBB)

## Resultaatreekscodes {#section_80D68334E8D04A33937A6E58ABAAA320}

De volgende labels retourneren een tekenreeks.

Zie [Over Resultaatlustags](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-index&gt; </span> </p> </td> 
   <td colname="col2"> <p>Retourneert de numerieke index van het huidige resultaat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-title length="XX"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Retourneert de paginatitel van het huidige resultaat. Het optionele kenmerk length wordt gebruikt om de lengte van de weergegeven tekenreeksen te beperken, met standaard 80 tekens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-bodytext length="XX" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Retourneert de hoofdtekst vanaf de bovenkant van de pagina. Relevante termen worden vet weergegeven. Het optionele kenmerk length wordt gebruikt om de lengte van de weergegeven tekenreeksen te beperken, met standaard 80 tekens. Het coderingskenmerk is optioneel en kan uitvoertekens coderen met HTML-codering (standaard), Javascript-codering, Perl-codering of geen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-description length="XX" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Retourneert de beschrijving van het huidige resultaat. Als de metatag bestaat en het inhoudskenmerk niet leeg is, wordt die tekst weergegeven. Anders wordt het begin van de hoofdtekst van de pagina weergegeven. Het optionele kenmerk length wordt gebruikt om de lengte van de weergegeven tekenreeksen te beperken, met standaard 80 tekens. </p> <p>Het optionele <span class="codeph">-kenmerk codering </span> bepaalt of de uitvoer wordt gecodeerd als HTML, gecodeerd als JavaScript, gecodeerd als Perl, gecodeerd als URL of niet gecodeerd als uitvoer op de resultatenpagina. De standaardwaarde van <span class="codeph"> het coderen </span> is <span class="codeph"> html </span>. Normaal gesproken hoeft u het coderingskenmerk niet op te geven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-score rank="dynamic/static/dynamic-raw/static-raw/final-raw" precision="XX"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Geeft de score van het huidige resultaat. Dit is een getal 0 - 100. Als u een rangtelveld hebt gedefinieerd onder <span class="uicontrol"> Opties </span> &gt; <span class="uicontrol"> Metagegevens </span> &gt; <span class="uicontrol"> Definities </span>, kunt u de dynamische paginagrande weergeven door het randeattribuut in te stellen op dynamisch ( <span class="codeph"> &lt;search-score rank="dynamic"&gt; </span>). U kunt de statische paginatieregel weergeven door het randeattribuut in te stellen op statisch ( <span class="codeph"> &lt;search-score rank="static"&gt; </span>). U kunt het optionele precisiekenmerk gebruiken om het aantal decimalen op te geven dat moet worden weergegeven. De standaardwaarde is 0, waarmee de gehele-getalscore wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-date length="XX" none="text" date-format="date-format-string" gmt="yes/no" language="0/2/language-id"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Retourneert de datum van het huidige resultaat. De optionele tekstwaarde "none" wordt weergegeven als er geen datum is gekoppeld aan het huidige resultaat. Als de optionele waarde "none" niet wordt gegeven, wordt de tekst "No Date" weergegeven als er geen datum is gekoppeld aan het huidige resultaat. </p> <p>Het kenmerk "date-format" heeft een datumnotatietekenreeks in de UNIX-stijl, zoals "%A, %B %d, %Y" (voor "maandag, 25 juli 2016"). "gmt" is standaard ingesteld op "yes" en bepaalt of het tijdgedeelte van de datumtekenreeks moet worden uitgevoerd in GMT ("yes") of in de tijdzone van de account ("no"). </p> <p>Het kenmerk "language" bestuurt de taal- en landinstellingconventies van de tekenreeks met de uitvoerdatum. "0" (de standaardwaarde) betekent "Account Language gebruiken". "2" betekent "Documenttaal gebruiken". De waarde "taal" "1" is gereserveerd voor toekomstig gebruik. Elke andere "taal"-waarde wordt geïnterpreteerd als een specifieke taal-id, bijvoorbeeld "en_US" betekent "Engels (Verenigde Staten)". </p> <p>Het optionele kenmerk length wordt gebruikt om de lengte van de weergegeven tekenreeksen te beperken, met standaard 80 tekens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-size&gt; </span> </p> </td> 
   <td colname="col2"> <p>Geeft de grootte van het huidige resultaat in bytes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-url length="XX" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Retourneert de URL van het huidige resultaat. </p> <p>Gebruik het optionele <span class="codeph"> length </span> attribuut om de lengte van weergegeven tekenreeksen te beperken, met standaard een onbeperkt aantal tekens. </p> <p>Het <span class="codeph">-coderingskenmerk </span> is optioneel en het kan uitvoertekens coderen met HTML-codering, Javascript-codering, Perl-codering of geen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-url-path-query length="XX"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Retourneert het pad en querydelen inclusief het vraagteken van de URL van het huidige resultaat. </p> <p>Gebruik het optionele <span class="codeph"> length </span> attribuut om de lengte van weergegeven tekenreeksen te beperken, met standaard een onbeperkt aantal tekens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-context length="XX" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Retourneert de volgende regel context voor de zoekterm. Relevante termen worden vet weergegeven. Roep deze tag herhaaldelijk aan om meerdere contextlijnen voor het huidige resultaat weer te geven. </p> <p>Gebruik het optionele <span class="codeph"> length </span> attribuut om de lengte van weergegeven tekenreeksen te beperken, met een standaard van 80 tekens. Het <span class="codeph">-kenmerk length </span> wordt genegeerd als deze tag wordt ingesloten door <span class="codeph"> &lt;search-if-context&gt; </span> of <span class="codeph"> &lt;search-if-any-context&gt; </span>-tagsets die een lengtekenmerk bevatten. </p> <p>Het <span class="codeph">-coderingskenmerk </span> is optioneel en het kan uitvoertekens coderen met HTML-codering (standaard), Javascript-codering, Perl-codering of geen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field name="field-name" length="XX" none="text" date-format="date-format-string" gmt="yes/no" language="0/2/language-id" encoding="html/javascript/json/perl/url/none" quotes="yes/no" commas="yes/no" units="miles/kilometers" separator="|"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Met deze geavanceerde tag wordt de inhoud weergegeven van het metagegevensveld (url, title, desc, keys, target, body, alt, date, charset en taal of velden gedefinieerd onder <span class="uicontrol"> Opties </span> &gt; <span class="uicontrol"> Metagegevens </span> &gt; Definities) opgegeven in het <span class="codeph"> name </span>-kenmerk voor het huidige resultaat. Bijvoorbeeld: </p> <p> <span class="codeph"> &lt;search-display-field name="title" length="70" none="no title"&gt; </span> </p> <p>Hiermee wordt de titel van de pagina uitgevoerd voor een zoekresultaat. Als het optionele <span class="codeph">-kenmerk geen </span> is opgegeven, wordt de waarde ervan alleen op de resultatenpagina weergegeven als er geen inhoud aan het veld is gekoppeld. </p> <p>De <span class="codeph"> datum-notatie </span>, <span class="codeph"> gmt </span> en <span class="codeph"> taal </span> zijn alleen relevant als het inhoudstype van het opgegeven veld <span class="codeph"> datum </span> is. </p> <p>Het <span class="codeph"> date-format </span>-kenmerk heeft een UNIX-stijl datumnotatietekenreeks, zoals <span class="codeph"> %A, %B %d, %Y </span> (voor maandag 25 juli 2016). <span class="codeph"> gmt  </span> blijft  <span class="codeph"> ja  </span> en controleert of het tijdgedeelte van het datumkoord output in GMT (  <span class="codeph"> ja  </span>) of de tijdzone van de rekening (  <span class="codeph"> nee  </span>) is. </p> <p>Zie <a href="../c-appendices/c-templates.md#section_4BBDBBEF2B96414497617CD4B52D96E4" type="section" format="dita" scope="local"> Tekenreeksen datumnotatie</a>. </p> <p>Het <span class="codeph"> taalattribuut </span> controleert de taal en de scèneovereenkomsten van het koord van de outputdatum. <span class="codeph"> 0  </span> (de standaardwaarde) betekent "Account Language gebruiken". <span class="codeph"> 2  </span> betekent "Documenttaal gebruiken". De <span class="codeph"> taal </span> waarde <span class="codeph"> 1 </span> is gereserveerd voor toekomstig gebruik). Elke andere <span class="codeph"> taal </span> waarde wordt geïnterpreteerd als een specifieke taalherkenningsteken, bijvoorbeeld <span class="codeph"> en_US </span> betekent "Engels (Verenigde Staten)". </p> <p>Zie <a href="../c-appendices/c-templates.md#section_0490DECC00E34691ADE5A9ED90A6D911" type="section" format="dita" scope="local"> Taalid's</a>. </p> <p>Het optionele <span class="codeph"> length </span> attribuut wordt gebruikt om de lengte van weergegeven tekenreeksen te beperken, met standaard 80 tekens. </p> <p>Het optionele <span class="codeph">-kenmerk codering </span> bepaalt of de uitvoer wordt gecodeerd als HTML, gecodeerd als JavaScript, gecodeerd als Perl, gecodeerd als URL of niet gecodeerd als uitvoer op de resultatenpagina. De standaardwaarde van <span class="codeph"> het coderen </span> is <span class="codeph"> html </span>. Normaal gesproken hoeft u het coderingskenmerk niet op te geven. </p> <p>Het optionele <span class="codeph">-kenmerk </span> bepaalt of de afzonderlijke items die worden uitgevoerd, worden omringd door dubbele aanhalingstekens (of enkele aanhalingstekens, als <span class="codeph"> encoding=perl </span>). De standaardwaarde van <span class="codeph"> citeert </span> is <span class="codeph"> geen </span>. </p> <p>Het optionele <span class="codeph"> komma's </span> kenmerk bepaalt of de afzonderlijke items die worden uitgevoerd, door komma's worden gescheiden. De standaardwaarde van <span class="codeph"> komma's </span> is <span class="codeph"> ja </span>. Het kenmerk <span class="codeph"> komma's </span> wordt genegeerd voor velden die geen lijsttype zijn. </p> <p>Het optionele <span class="codeph">-kenmerk units </span> bepaalt de afstand-eenheden die worden toegepast op een nabijheidsveld voor zoekopdrachten. De standaardwaarde van <span class="codeph"> eenheden </span> wordt bepaald van het "Standaard plaatsen"plaatsen van het plaats-type gebied verbonden aan het bepaalde gebied van de nabijheidsonderzoek outputonderzoek. </p> <p>Zie <a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> Informatie over nabijheidszoekopdracht</a>. </p> <p>Het optionele <span class="codeph">-scheidingsteken </span> definieert het enkele teken, of scheidingsteken, dat wordt ingevoegd tussen de waarden van de uitvoer voor lijsttekstvelden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field-values name="field-name"&gt; ...&lt;search-display-field-values&gt; </span> </p> </td> 
   <td colname="col2"> <p>Met dit label wordt een lus gemaakt voor het opsommen van waarden in metagegevensvelden (url, title, desc, keys, target, body, alt, date, charset en taal of velden gedefinieerd onder <span class="uicontrol"> Opties </span> &gt; <span class="uicontrol"> Metagegevens </span> &gt; <span class="uicontrol"> Definities </span>) voor het huidige resultaat. Nest deze tag niet in een andere <span class="codeph"> &lt;search-display-field-values&gt; </span>-tag. Het <span class="codeph"> name </span> attribuut specificeert de naam van het gebied dat de te enumereren waarden bevat. Deze tag is vooral handig voor velden waarvoor het <span class="uicontrol">-kenmerk Lijsten van gewenste personen </span> is ingeschakeld (onder <span class="uicontrol"> Opties </span> &gt; <span class="uicontrol"> Metagegevens </span> &gt; <span class="uicontrol"> Definities </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field-value date-format="date-format-string" gmt="yes/no" language="0/language-id" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze tag geeft de waarde van het metagegevensveld weer (url, title, desc, keys, target, body, alt, date, charset en taal of velden gedefinieerd onder <span class="uicontrol"> Opties </span> &gt; <span class="uicontrol"> Metagegevens </span> &gt; <span class="uicontrol"> Definities </span>) voor de huidige <span class="codeph"> &lt;search-display-field-values&gt; </span>. Deze tag is alleen geldig binnen een <span class="codeph"> &lt;search-display-field-values&gt; </span> lus. De <span class="codeph"> datum-notatie </span>, <span class="codeph"> gmt </span> en <span class="codeph"> taal </span> zijn alleen relevant als het inhoudstype van de veldnaam die is opgegeven in de insluitende <span class="codeph"> &lt;search-display-field-values&gt; </span> tag <span class="codeph"> datum </span> is. Het <span class="codeph"> date-format </span>-kenmerk heeft een UNIX-stijl datumnotatietekenreeks zoals <span class="codeph"> "%A </span>, <span class="codeph"> %B </span> <span class="codeph"> %d </span>, <span class="codeph"> %Y </span>" (voor "maandag, juli 25, 2016"). Het <span class="codeph"> gmt </span> attribuut is standaard <span class="codeph"> ja </span> en bepaalt of het tijdgedeelte van de datumtekenreeks wordt uitgevoerd in GMT ( <span class="codeph"> ja </span>) of de tijdzone van de account ( <span class="codeph"> nr </span>). </p> <p>Het <span class="codeph"> taalattribuut </span> controleert de taal en de scèneovereenkomsten van het koord van de outputdatum. <span class="codeph"> 0  </span> (de standaardwaarde) betekent "Account Language gebruiken". Elke andere <span class="codeph"> taal </span> waarde wordt geïnterpreteerd als een specifieke taalherkenningsteken, bijvoorbeeld <span class="codeph"> en_US </span> betekent "Engels (Verenigde Staten)". </p> <p>Het optionele <span class="codeph">-kenmerk codering </span> bepaalt of de uitvoer wordt gecodeerd als HTML, gecodeerd als JavaScript, gecodeerd als Perl, gecodeerd als URL of niet gecodeerd als uitvoer op de resultatenpagina. De standaardwaarde van <span class="codeph"> het coderen </span> is <span class="codeph"> html </span>. Normaal gesproken hoeft u het coderingskenmerk niet op te geven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field-value-count name="field-name"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Geeft als uitvoer het totale aantal waarden in het huidige resultaat voor het metagegevensveld (url, title, desc, keys, target, body, alt, date, charset en taal of velden gedefinieerd onder <span class="uicontrol"> Opties </span> &gt; <span class="uicontrol"> Metagegevens </span> &gt; <span class="uicontrol"> Definities </span>) opgegeven met het naamkenmerk. Deze tag kan overal in de resultatenlus worden weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field-value-counter&gt; </span> </p> </td> 
   <td colname="col2"> <p>Hiermee wordt de ordinale teller (1, 2, 3, enzovoort) uitgevoerd voor de huidige herhaling van de lus <span class="codeph"> &lt;search-display-field-values&gt; </span>. Deze tag is alleen geldig binnen een <span class="codeph"> &lt;search-display-field-values&gt; </span> lus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-dynamic-facet-fields&gt; </span> </p> </td> 
   <td colname="col2"> <p>Begint een het van een lus voorzien context voor om het even welke dynamisch-facet-gebieden die voor dit onderzoek zijn teruggekeerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-dynamic-facet-field-name&gt; </span> </p> </td> 
   <td colname="col2"> <p>Hiermee wordt de naam van het huidige dynamische facet-veld voor deze lusherhaling uitgevoerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW for S&P 8.17.0 release on October 30 2014--> <span class="codeph"> &lt;search-result-trace encoding="html/javascript/ json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Output-informatie met betrekking tot de plaatsing van het huidige resultaat, bijvoorbeeld acties op basis van resultaten die de positie van het resultaat beïnvloedden. </p> <p>De uitvoerindeling van deze tag is JSON, zoals in het volgende voorbeeld: </p> <p> <code> { 
      &nbsp;&nbsp;"sliceID":&nbsp;5, 
      &nbsp;&nbsp;"indexID":&nbsp;5894, 
      &nbsp;&nbsp;"finalScore":&nbsp;98.5, 
      &nbsp;&nbsp;"dynamicScore":&nbsp;15.3, 
      &nbsp;&nbsp;"staticScore":&nbsp;55.456, 
      &nbsp;&nbsp;"position":&nbsp;1, 
      &nbsp;&nbsp;"rbtaActionListID":&nbsp;117, 
      &nbsp;&nbsp;"rbtaActionID":&nbsp;57 
      } </code> </p> 
    <!--<p> Results added to the results set by way of <codeph>rbta</codeph> have a "naturalPosition" value of -1. </p>--> <p>Het <span class="codeph">-coderingskenmerk </span> is optioneel. de standaardwaarde is <span class="codeph"> html </span>. </p> <p> <p>Opmerking:  Deze markering heeft slechts output als <span class="codeph"> sp_trace=1 </span> met de parameters van de kernonderzoeksvraag wordt gespecificeerd. </p> </p> <p>Zie rij 48 in de lijst die in <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" format="dita" scope="local"> wordt gevonden Achterste onderzoek CGI parameters</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Resultaatlus voorwaardelijke tags {#section_35C367969E384A06A9865E388F1F9360}

De volgende tags bevatten onder andere de HTML.

Zie [Over Resultaatlustags](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-title&gt; ...  &lt;/search-if-title&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-title&gt; ...  &lt;/search-if-not-title&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze tags bevatten de HTML tussen de tags als de volgende aanroep van <span class="codeph"> &lt;search-title&gt; </span> tekst uit de documenttitel retourneert (of niet retourneert). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-description length="XX"&gt; ... /search-if-description&gt;  </span> </p> <p> <span class="codeph"> &lt;search-if-not-description&gt; ...  &lt;/search-if-not-description&gt; </span> </p> </td> 
   <td colname="col2"> <p> Deze tags bevatten de HTML tussen de tags als de volgende aanroep van <span class="codeph"> &lt;search-description&gt; </span> tekst uit de documentbeschrijving retourneert (of niet retourneert). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-bodytext&gt; ...  &lt;/search-if-bodytext&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-bodytext&gt; ...  &lt;/search-if-not-bodytext&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze tags bevatten de HTML tussen de tags als de volgende aanroep van <span class="codeph"> &lt;search-body text&gt; </span> tekst uit de hoofdtekst van het document retourneert (of niet retourneert). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-context length="XX"&gt; ...  &lt;/search-if-context&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-context&gt; ...  &lt;/search-if-not-context&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze markeringen omvatten HTML tussen hen als de volgende vraag aan <span class="codeph"> &lt;search-context&gt; </span> een niet-lege contextkoord terugkeert (of niet terugkeert). Het kenmerk length overschrijft het kenmerk length op een omsloten <span class="codeph"> &lt;search-context&gt; </span>-tag. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-any-context length="XX"&gt; ... /search-if-any-context&gt;  </span> </p> <p> <span class="codeph"> &lt;search-if-not-any-context&gt; ...  &lt;/search-if-not-any-context&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze tags bevatten de HTML tussen de tags als er een contexttekenreeks aan het resultaat is gekoppeld (of niet). Het kenmerk length overschrijft het kenmerk length op een omsloten <span class="codeph"> &lt;search-context&gt; </span>-tag. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-score lower="XX" upper="yy" rank="dynamic/static/dynamic-raw/static-raw/final-raw"&gt; ...  &lt;/search-if-score&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-score lower="XX" upper="yy" rank="dynamic/static"&gt; ...  &lt;/search-if-not-score&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze tags bevatten de HTML tussen de tags als de score van het huidige resultaat al dan niet ligt tussen XX en YY. Nuttig voor het toevoegen van opsommingstekens of afbeeldingen om aan te geven hoe relevant het resultaat is. Als u een randetype gebied onder <span class="uicontrol"> Opties </span> &gt; <span class="uicontrol"> Metagegevens </span> &gt; <span class="uicontrol"> Definities </span> hebt gedefinieerd, kunt u de dynamische paginagrate controleren door het randeattribuut in te stellen op dynamisch ( <span class="codeph"> &lt;search-if-score rank="dynamic" lower=XX=YY&gt; </span>). U kunt de statische paginatieregel controleren door het randeattribuut in te stellen op statisch ( <span class="codeph"> &lt;search-if-score rank="static" lower=XX upper=YY&gt; </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-field name="field-name" value="value"&gt; ...  &lt;/search-if-field&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-field name="field-name" value="value"&gt; ...  &lt;/search-if-not-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze geavanceerde tags bevatten de HTML tussen de tags op basis van het feit of het veld dat is opgegeven in het kenmerk "name" inhoud bevat. Als het optionele kenmerk "value" is opgegeven, bevatten de tags de HTML tussen de tags op basis van het feit of de gegeven waarde overeenkomt met (of niet overeenkomt met) de waarde voor het veld in het huidige resultaat. Deze tags werken alleen binnen de resultatenlus (tussen <span class="codeph"> &lt;search-results&gt; </span> en <span class="codeph"> &lt;/search-results&gt; </span>-tags). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Resultaatlus voor ankerkoppelingcodes {#section_C5FAEF520E9E42ADAD1F90651922AA02}

Zie [Over Resultaatlustags](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-link target="frame-name" hbx-enable="yes/no" hbx-linkid-name="field-name" hbx-linkid-none="text" hbx-linkid-length="XX"&gt; ...  &lt;/search-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Dit paar tags maakt een ankerkoppeling rondom de HTML tussen de tags. Wanneer op de koppeling wordt geklikt, wordt de resultatenpagina weergegeven. Een facultatief doelattribuut specificeert het genoemde venster waarin kader-geschikt browsers de resultatenpagina zouden moeten tonen. </p> <p>Stel het kenmerk hbx-enable in op "yes" om te profiteren van de analyses die beschikbaar zijn via HBX. Stel hbx-linchild-name in op de naam van een metagegevensveld dat u wilt bijhouden. Bijvoorbeeld, om onderzoeksresultaten door aantal SKU te volgen, plaats hbx-linchild-name aan de naam van het meta-gegeven gebied dat SKU informatie bevat. </p> <p>Datumtype velden worden momenteel niet ondersteund. De waarde van hbx-linchild-name wordt toegevoegd aan verbindingsidentiteitskaart in het geproduceerde anker. De waarde van het hbx-linchild-none-kenmerk wordt toegevoegd aan de koppelings-id wanneer het benoemde metagegevensveld leeg is. De waarde van hbx-linchild-length beperkt het aantal tekens dat van de tag Meta wordt opgehaald en weergegeven. Het standaardaantal tekens is 12. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-smart-link target="frame-name" hbx-enable="yes/no" hbx-linkid-name="field-name" hbx-linkid-none="text" hbx-linkid-length="XX"&gt; ...  &lt;/search-smart-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Dit paar markeringen is gelijkaardig aan <span class="codeph"> &lt;search-link&gt;.. &lt;/search-link&gt; </span>-tags. Wanneer op de gegenereerde ankerkoppelingen wordt geklikt, wordt de resultatenpagina weergegeven, maar wordt de pagina naar de dichtstbijzijnde ankertag vóór het resultaat geschoven. Voor PDF-koppelingen wordt in de Acrobat-viewer de pagina weergegeven die het resultaat bevat. Een facultatief doelattribuut specificeert het genoemde venster waarin kader-geschikt browsers de resultatenpagina zouden moeten tonen. </p> <p>Stel het kenmerk hbx-enable in op "yes" om te profiteren van de analyses die beschikbaar zijn via HBX. Stel hbx-linchild-name in op de naam van een metagegevensveld dat u wilt bijhouden. Bijvoorbeeld, om onderzoeksresultaten door aantal SKU te volgen, plaats hbx-linchild-name aan de naam van het meta-gegeven gebied dat SKU informatie bevat. </p> <p>Datumtype velden worden momenteel niet ondersteund. De waarde van hbx-linchild-name wordt toegevoegd aan verbindingsidentiteitskaart in het geproduceerde anker. De waarde van het hbx-linchild-none-kenmerk wordt toegevoegd aan de koppelings-id wanneer het benoemde metagegevensveld leeg is. De waarde van hbx-linchild-length beperkt het aantal tekens dat van de tag Meta wordt opgehaald en weergegeven. Het standaardaantal tekens is 12. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-link-extension&gt; ...  &lt;/search-if-link-extension&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-link-extension&gt; ...  &lt;/search-if-not-link-extension&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze tags bevatten de HTML tussen de tags als een waardekenmerk een extensie opgeeft die overeenkomt met het einde van de URL voor het resultaat. Deze tag is handig als u een afbeelding wilt opnemen in de zoekresultaten op basis van de extensie van de koppeling. Het kenmerk value is als volgt een lijst met een of meer extensies (spaties gescheiden): VALUE=".pdf" of VALUE=".html .htm". </p> </td> 
  </tr> 
 </tbody> 
</table>

## Voorwaardelijke tags {#section_E0C29DDA09E043C9A396F36334F05EBB} voor positie herhalen

De volgende labels bevatten voorwaardelijk de tekst tussen de labels. Ze kunnen alleen worden weergegeven binnen de tags &#39;lussen&#39;: &lt; `search-results>` en `<search-field-values>`. Deze worden gebruikt om de positie van het huidige resultaat binnen de resultaatset te testen.

Zie [Over Resultaatlustags](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-first&gt; ...  &lt;/search-if-first&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-first&gt; ...  &lt;/search-if-not-first&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze tags bevatten de tekst tussen de tags als het huidige resultaat het eerste resultaat op de pagina is (wanneer gebruikt binnen <span class="codeph"> &lt;search-results&gt; </span>) of de eerste veldwaarde (wanneer gebruikt binnen <span class="codeph"> &lt;search-field-values&gt; </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-last&gt; ...  &lt;/search-if-last&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-last&gt; ...  &lt;/search-if-not-last&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze tags bevatten de tekst tussen de tags als het huidige resultaat het laatste resultaat op de pagina is (of niet is) (indien gebruikt binnen <span class="codeph"> &lt;search-results&gt; </span>) of de laatste veldwaarde (indien gebruikt binnen <span class="codeph"> &lt;search-field-values&gt; </span>). Met dit label kunt u een scheidingsteken invoegen tussen de resultaten. Hiermee voegt u bijvoorbeeld een <span class="codeph"> &lt;hr&gt; </span>-tag tussen de resultaten in: </p> <p> <code class="syntax html"> &lt;search-results&gt; 
      &nbsp;&nbsp;&nbsp;&lt;search-lt&gt;tr&lt;search-if-alt&gt;&nbsp;class="alt"&lt;/search-if-alt&gt;&lt;search-gt&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;td&gt;&lt;search-url&gt;&lt;/td&gt; 
      &nbsp;&nbsp;&nbsp;&lt;/tr&gt; 
      &lt;/search-results&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-inner&gt; ...  &lt;/search-if-inner&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-inner&gt; ...  &lt;/search-if-not-inner&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze tags bevatten de tekst tussen de tags als het huidige resultaat niet het eerste of laatste resultaat op de pagina is (indien gebruikt binnen <span class="codeph"> &lt;search-results&gt; </span>) of niet de eerste of laatste veldwaarde is (indien gebruikt binnen <span class="codeph"> &lt;search-field-values&gt; </span>). De niet-versie van de tag test of het resultaat het eerste of laatste is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-alt&gt; ...  &lt;/search-if-alt&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-alt&gt; ...  &lt;/search-if-not-alt&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze tags bevatten de tekst tussen de tags als het huidige resultaat een alternatief resultaat op de pagina is (wanneer gebruikt binnen <span class="codeph"> &lt;search-results&gt; </span>) of een alternatieve veldwaarde (wanneer gebruikt binnen <span class="codeph"> &lt;search-field-values&gt; </span>). De "afwisselende"resultaten zijn tweede, vierde, zesde, etc., op de pagina. In dit voorbeeld wordt een andere klasse toegepast op alternatieve tabelrijen. Let op het gebruik van <span class="codeph"> &lt;search-lt&gt; </span> en <span class="codeph"> &lt;search-gt&gt; </span> om toe te staan dat de <span class="codeph"> &lt;search-if-alt&gt; </span> tag "inside" de <span class="codeph"> &lt;tr&gt; </span> tag wordt geplaatst. </p> <p> <code class="syntax html"> &nbsp;&nbsp;&nbsp;&nbsp;&lt;search-results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;search-lt&gt;tr&lt;search-if-alt&gt;&nbsp;class="alt"&lt;/search-if-alt&gt;&lt;search-gt&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;td&gt;&lt;search-url&gt;&lt;/td&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/tr&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-results&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-even&gt; ...  &lt;/search-if-even&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-even&gt; ...  &lt;/search-if-not-even&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze tags bevatten de tekst tussen de tags als het huidige resultaat een even-genummerd resultaat is (wanneer gebruikt binnen <span class="codeph"> &lt;search-results&gt; </span>) of een even-genummerde veldwaarde (wanneer gebruikt binnen <span class="codeph"> &lt;search-field-values&gt; </span>). Een zoekresultaat is even genummerd als de waarde <span class="codeph"> &lt;search-index&gt; </span> gelijk is. Met andere woorden, als de positie binnen de gehele resultaatset gelijk is. Dit kan verschillen van <span class="codeph"> &lt;search-if-alt&gt; </span> die de positie van een resultaat op de pagina test, niet binnen de volledige resultaatreeks. De volgende twee tabellen illustreren het verschil: </p> </td> 
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
   <td colname="col1"> <p>3 </p> </td> 
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
   <td colname="col2"> <p>Leventiende resultaat </p> </td> 
   <td colname="col3"> <p>Nee </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>12 </p> </td> 
   <td colname="col2"> <p>Twaalf resultaten </p> </td> 
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

Ten slotte is `<search-if-even>` altijd hetzelfde als `<search-if-alt>` voor waarden in zoekvelden omdat veldwaarden niet worden geplakt.

## Lijstlabels voor veldwaarden {#section_D3298B5F976447DBA0032B883DCC91B1}

Met de volgende geavanceerde tags worden de uitvoerveldwaarden en verwante gegevens uit de volledige set zoekresultaten weergegeven. Deze markeringen produceren slechts output voor gebieden die door de `sp-sfvl-field` parameters van CGI in de onderzoeksvraag worden gespecificeerd.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value-list name="field-name" quotes="yes/no" commas="yes/no" data="values/counts/results" separator="X" sortby="none/values/counts/results" max-items="XX" date-format="date-format-string" gmt="yes/no" language="0/language-id" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Met dit label geeft u een lijst weer met unieke veldwaarden, tellingen van waarden of tellingen van resultaten binnen de gehele resultaatset. </p> <p>Met deze tag wordt alleen uitvoer gegenereerd voor velden die zijn opgegeven met de CGI-parameters <span class="codeph"> sp_sfvl_field </span> in de zoekquery. Het optionele kenmerk "quotes" bepaalt of de afzonderlijke items die worden uitgevoerd, worden omringd door dubbele aanhalingstekens (of enkele aanhalingstekens, als encoding=perl). De standaardwaarde van "quotes" is "yes". Het optionele kenmerk "komma's" bepaalt of de afzonderlijke items die worden uitgevoerd, door komma's worden gescheiden. De standaardwaarde van "komma's" is "ja". Het optionele kenmerk "data" bepaalt of elke unieke veldwaarde uitvoer is (data="values"), het totale aantal van elke unieke veldwaarde uitvoer is (data="counts") of het aantal resultaten dat elke unieke waarde bevat (data="results") wordt uitgevoerd. De standaardwaarde van "data" is "values". Voor niet-list-type velden zijn data="counts" en data="results" gelijk. Het scheidingskenmerk definieert het ene teken (scheidingsteken) dat tussen de waarden van de uitvoer moet worden ingevoegd. Het optionele kenmerk "sortby" bepaalt de volgorde van de uitvoer. sortby="none" betekent geen bepaalde volgorde, sortby="values" betekent sorteren op veldwaarden (in oplopende of aflopende volgorde volgens de sorteereigenschap van het veld), sortby="counts" betekent sorteren in aflopende volgorde van veldwaardetelling, en sortby="results" betekent sorteren in aflopende volgorde van het aantal resultaten dat elke waarde bevat. </p> <p>Merk op dat sortby="counts" en sortby="resultaten" gelijkwaardig zijn voor niet-list-type gebieden. Het optionele kenmerk "max-items" beperkt het aantal items dat moet worden uitgevoerd. De standaardwaarde van "max-items" is -1, wat betekent "alle items uitvoeren". </p> <p>Er geldt een absolute limiet van 100 voor max-items. De kenmerken "date-format", "gmt" en "language" zijn alleen relevant als het inhoudstype van het opgegeven veld "date" is. Het kenmerk "date-format" heeft een datumnotatietekenreeks in de UNIX-stijl, zoals "%A, %B %d, %Y" (voor "maandag, 25 juli 2016"). "gmt" is standaard ingesteld op "yes" en bepaalt of het tijdgedeelte van de datumtekenreeks moet worden uitgevoerd in GMT ("yes") of in de tijdzone van de account ("no"). </p> <p>Zie <a href="../c-appendices/c-templates.md#section_4BBDBBEF2B96414497617CD4B52D96E4" type="section" format="dita" scope="local"> Tekenreeksen datumnotatie</a>. </p> <p>Het kenmerk "language" bestuurt de taal- en landinstellingconventies van de tekenreeks met de uitvoerdatum. "0" (de standaardwaarde) betekent "Account Language gebruiken". Elke andere "taal"-waarde wordt geïnterpreteerd als een specifieke taal-id, bijvoorbeeld "en_US" betekent "Engels (Verenigde Staten)". Het optionele kenmerk "encoding" bepaalt of de tekens van de uitvoertekenreeks HTML-gecodeerd, JavaScript-gecodeerd, Perl-gecodeerd, URL-gecodeerd of niet gecodeerd zijn voor uitvoer op de resultatenpagina. De standaardwaarde van "encoding" is "html". </p> <p>Zie <a href="../c-appendices/c-templates.md#section_0490DECC00E34691ADE5A9ED90A6D911" type="section" format="dita" scope="local"> Taalid's</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value-list-count name="field-name" value="field-value" results="yes/no"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze markering toont telinformatie voor een bepaalde onderzoek-gebied-waarde-lijst. Er zijn drie verschillende toepassingen voor deze tag. Als alleen het kenmerk "name" wordt opgegeven, geeft deze tag als uitvoer het aantal unieke waarden voor het benoemde veld binnen de volledige resultatenset. Als de kenmerken "name" en "value" beide worden opgegeven, genereert dit label ofwel het totale aantal van de opgegeven waarde binnen de volledige resultatenset (voor results="no"), ofwel het totale aantal resultaten dat de opgegeven waarde bevat in de volledige resultatenset (voor results="yes"). De standaardwaarde van "resultaten" is "nee". Opmerking: Voor niet-list-type velden zijn results="yes" en results="no" gelijk. De waarde van "results" wordt genegeerd als het kenmerk "value" niet wordt opgegeven. Met deze tag wordt alleen uitvoer gegenereerd voor velden die zijn opgegeven door de CGI-parameters </span> sp-sfvl-field &lt;a1/&gt; in de zoekquery.<span class="codeph"> </span></p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-field-value-list-count name="field-name" value="field-value"&gt; ...  &lt;/search-if-field-value-list-count&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-field-value-list-count name="field-name" value="field-value"&gt; ...  &lt;/search-if-not-field-value-list-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze tags geven de HTML tussen de tags weer als de equivalente aanroep van <span class="codeph"> &lt;search-field-value-list-count name="field-name" value="field-value"&gt; </span> met de opgegeven kenmerken een waarde groter dan nul zou (of niet) retourneren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-single-field-value-list-count name="field-name"&gt; ...  &lt;/search-if-single-field-value-list-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze tags geven de inhoud tussen de tags weer als de equivalente aanroep van <span class="codeph"> &lt;search-field-value-list-count name="field-name" value="field-value"&gt; </span> met de opgegeven kenmerken één waarde zou (of niet) retourneren. Dit wordt doorgaans gebruikt wanneer een account sleuven voor facetten gebruikt. Met facetgroeven, wilt u typisch slechts de waarde-groef tonen wanneer de bijbehorende naam-groef één enkel punt heeft. Het uitvoeren van deze controle in het vervoermalplaatje is efficiënter dan het doen van het in de presentatielaag. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Lijstlabels voor veldwaarden {#section_0717FA09F0FC449CB916883B0500A60E}

Met de volgende geavanceerde tags worden waarden van uitvoervelden en verwante gegevens uit de gehele set zoekresultaten opgesomd met behulp van een lusconstructie. Deze markeringen produceren slechts output voor gebieden die door de `sp-sfvl-field` parameters van CGI in de onderzoeksvraag worden gespecificeerd.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-values name="field-name" sortby="none/values/counts/results" max-items="XX"&gt; ...  &lt;/search-field-values&gt; </span> </p> </td> 
   <td colname="col2"> <p>Met deze tag wordt een lus gemaakt voor het opsommen van veldwaarden en verwante gegevens voor een bepaald veld binnen de volledige resultatenset. Nest deze tag niet in een andere <span class="codeph"> &lt;search-field-values&gt; </span>-tag. Het kenmerk "name" geeft de naam op van het veld met de waarden die moeten worden opgesomd. Het optionele kenmerk "sortby" bepaalt de volgorde van de opsommingen: "none" betekent geen bepaalde volgorde, "waarden" betekent sorteren op veldwaarden (in oplopende of aflopende volgorde volgens de eigenschap Sorteren van het veld), sortby="counts" betekent sorteren in aflopende volgorde van veldwaardetelling, en sortby="resultaten" betekent sorteren in aflopende volgorde van het aantal resultaten dat elke waarde bevat. </p> <p>Merk op dat sortby="counts" en sortby="resultaten" gelijkwaardig zijn voor niet-list-type gebieden. . Het optionele kenmerk "max-items" beperkt het aantal herhalingen tot de opgegeven waarde. De standaardwaarde voor "max-items" is -1, wat betekent "alle waarden opsommen". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value date-format="date-format-string" encoding="html/javascript/json/perl/url/none" gmt="yes/no" language="0/language-id"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze tag geeft de veldwaarde weer voor de huidige herhaling van de &lt;search-field-values&gt;-lus. Deze tag is alleen geldig binnen een <span class="codeph"> &lt;search-field-values&gt; </span> lus. De kenmerken "date-format", "gmt" en "language" zijn alleen relevant als het inhoudstype van de veldnaam die is opgegeven in de bijgevoegde tag &lt;search-field-values&gt; "date" is. Het kenmerk "date-format" heeft een datumnotatietekenreeks in de UNIX-stijl, zoals "%A, %B %d, %Y" (voor "maandag, 25 juli 2020"). </p> <p>Zie <a href="../c-appendices/c-templates.md#section_4BBDBBEF2B96414497617CD4B52D96E4" type="section" format="dita" scope="local"> Tekenreeksen datumnotatie</a>. </p> <p>Het optionele kenmerk "encoding" bepaalt of de tekens van de uitvoertekenreeks HTML-gecodeerd, JavaScript-gecodeerd, Perl-gecodeerd, URL-gecodeerd of niet gecodeerd zijn voor uitvoer op de resultatenpagina. De standaardwaarde van "encoding" is "none". Normaal gesproken hoeft u het coderingskenmerk niet op te geven. "gmt" is standaard ingesteld op "yes" en bepaalt of het tijdgedeelte van de datumtekenreeks moet worden uitgevoerd in GMT ("yes") of in de tijdzone van de account ("no"). Het kenmerk "language" bestuurt de taal- en landinstellingconventies van de tekenreeks met de uitvoerdatum. "0" (de standaardwaarde) betekent "Account Language gebruiken". Elke andere "taal"-waarde wordt geïnterpreteerd als een specifieke taal-id, bijvoorbeeld "en_US" betekent "Engels (Verenigde Staten)". </p> <p>Zie <a href="../c-appendices/c-templates.md#section_0490DECC00E34691ADE5A9ED90A6D911" type="section" format="dita" scope="local"> Taalid's</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value-count results="yes/no"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Met deze tag wordt de telling uitgevoerd die is gekoppeld aan de huidige herhaling van de <span class="codeph"> &lt;search-field-values&gt; </span>-lus. De uitvoerwaarde is ofwel het aantal resultaten in de volledige resultatenset die de veldwaarde bevat (results="yes"), ofwel het totale aantal voor de veldwaarde in de volledige resultatenset. De standaardwaarde van "resultaten" is "nee". </p> <p>Voor niet-list-type velden zijn results="yes" en results="no" gelijk. Deze tag is alleen geldig binnen een <span class="codeph"> &lt;search-field-values&gt; </span> lus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value-counter&gt; </span> </p> </td> 
   <td colname="col2"> <p>Met deze tag wordt de rangtellerwaarde voor de huidige herhaling van de <span class="codeph"> &lt;search-field-values&gt; </span>-lus uitgevoerd. Deze tag is alleen geldig binnen een <span class="codeph"> &lt;search-field-values&gt; </span> lus. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Codes {#section_C28EB8B4F7DC4E278A0F143BCFEEB1AC} voorstellen

Suggestie biedt een gebruiksvriendelijke &quot;Bedoelde u?&quot; dienst voor het voorstellen van alternatieve zoektermen. Als een gebruiker bijvoorbeeld een zoekterm verkeerd heeft gespeld, kunt u met Suggestie resultaten vinden door een correcte spelling voor te stellen. Het systeem kan verwante sleutelwoorden ook voorstellen die een gebruiker kunnen helpen resultaten ontdekken. Bij het genereren van suggesties gebruikt de dienst Suggestie twee woordenboeken: een op basis van de accounttaal (ingesteld onder **[!UICONTROL Indexing]** > **[!UICONTROL Words and Languages]** > **[!UICONTROL Language]**) en de andere op basis van de trefwoorden in de accountindex.

>[!NOTE]
>
>De dienst Suggest werkt niet voor Chinees, Japans, of Koreaans.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-suggestions&gt; ...  &lt;/search-if-suggestions&gt; </span> </p> </td> 
   <td colname="col2"> <p>Omring deze tags met 'Suggest'-sjabloontags, zoals <span class="codeph"> &lt;search-suggestie&gt; </span>, <span class="codeph"> &lt;search-suggestie-link&gt; </span> enzovoort. Als de zoekopdracht suggesties genereert, voert de zoekmachine alles uit en verwerkt deze tussen de tag open en close. Als de zoekopdracht geen suggesties oplevert, wordt geen van de geneste inhoud uitgevoerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-suggestions&gt; ...  &lt;/search-suggestions&gt; </span> </p> </td> 
   <td colname="col2"> <p>Met deze tag wordt de lus "Suggest" gegenereerd, die een lijst bevat met voorgestelde zoektermen (bijvoorbeeld "bedoeling", "voorgenomen" en "bedoeling" voor een query die oorspronkelijk is ingevoerd als "bedoeling"). Bij het genereren van de lijst met termen worden geneste HTML- en/of sjabloontags maximaal vijf keer door het zoekprogramma herhaald. Dit is het maximumaantal suggesties. Gebruik het kenmerk Count om het aantal gegenereerde suggesties (tussen 0 en 5) op te geven. </p> <p>De <span class="codeph"> &lt;search-Suggesties&gt; </span>-tag kan meerdere keren op de pagina worden weergegeven om de lijst met suggesties te herhalen. Meerdere suggesties worden gesorteerd op basis van het aantal resultaten dat elk resultaat oplevert. </p> <p>Plaats de <span class="codeph"> &lt;search-Suggesties&gt; </span>-tag tussen open en close <span class="codeph"> &lt;search-if-Suggesties&gt; </span>-tags. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-suggestion-link&gt; ...  &lt;/search-suggestion-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Met deze tag wordt een koppeling naar de oorspronkelijke zoekquery gegenereerd met de geselecteerde voorgestelde zoekterm in plaats van de oorspronkelijke term. De tag accepteert en drukt eenvoudig alle HTML-kenmerken af, zoals klasse, doel en stijl. De tag kan ook een URL-kenmerk accepteren waarvan de waarde wordt gebruikt als basis-URL voor de gegenereerde koppeling. De tags kunnen alleen worden weergegeven in de <span class="codeph"> &lt;search-Suggesties&gt; </span>-lus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-suggestion-text /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Met deze tag wordt de momenteel voorgestelde zoekterm afgedrukt (bijvoorbeeld 'Doel' voor een query die oorspronkelijk is ingevoerd als 'Doel'). De tag heeft geen kenmerken en kan alleen worden weergegeven in de <span class="codeph"> &lt;search-Suggesties&gt; </span>-lus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-not-suggestions&gt; ...  &lt;/search-if-not-suggestions&gt; </span> </p> </td> 
   <td colname="col2"> <p>Als de zoekopdracht geen suggesties genereert, voert de zoekmachine alles uit en verwerkt het tussen de tag open en close. Als de zoekopdracht suggesties genereert, wordt geen van de geneste inhoud uitgevoerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if&gt; ...  &lt;/search-if&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze voorwaardelijke tags bevatten de HTML tussen de tags op basis van het feit of de voorgestelde term de eerste term in de lus Suggest is. De tags moeten tussen de tags open en close <span class="codeph"> &lt;search-suggestie&gt; </span> worden weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if&gt; ...  &lt;/search-if&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze voorwaardelijke tags bevatten de HTML tussen de tags op basis van het feit of de voorgestelde term de laatste term in de lus Suggest is. De tags moeten tussen de tags open en close <span class="codeph"> &lt;search-suggestie&gt; </span> worden weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-suggestion-index&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze tag retourneert de numerieke index van de huidige voorgestelde zoekterm. De tag moet worden weergegeven tussen de tags open en close <span class="codeph"> &lt;search-suggestie&gt; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-suggestion-total&gt; </span> </p> </td> 
   <td colname="col2"> <p>Met dit label wordt het totale aantal gegenereerde voorgestelde zoektermen geretourneerd. De tag moet worden weergegeven tussen de tags open en close <span class="codeph"> &lt;search-suggestie&gt; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-suggestion-result-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>Met deze tag wordt het totale aantal resultaten voor de voorgestelde zoekterm geretourneerd. De tag moet worden weergegeven tussen de tags open en close <span class="codeph"> &lt;search-suggestie&gt; </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Sjabloontekenreekscodes {#section_67E3D529661F4F03A1FF469D9D658CAF}

Met de volgende tags wordt een tekenreeks uitgevoerd naar de HTML op dat punt in de sjabloon.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-body&gt; </span> </p> </td> 
   <td colname="col2"> <p>De HTML-body-tag met de instellingen voor Kleur van koppeling zoeken die de sectie Standaard zoeken onder de koppeling Sjabloon instelt. Voeg een achtergrondkenmerk aan deze tag toe om achtergrondafbeeldingen op de resultatenpagina weer te geven. Alle kleurkenmerken die aan deze tag worden toegevoegd, overschrijven de instellingen in de sectie Standaard zoeken in kleur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-header&gt; </span> </p> </td> 
   <td colname="col2"> <p>De HTML voor de Kopbal van Resultaten van het Onderzoek zoals die in de Basissectie van de Kijker onder de verbinding van het Malplaatje wordt geplaatst. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-cdata&gt; ...  &lt;/search-cdata&gt; </span> </p> </td> 
   <td colname="col2"> <p>De tags search-data worden vervangen door hun XML-equivalenten: <span class="codeph"> &lt;search-data&gt; </span> wordt vervangen door <span class="codeph"> &lt;![CDATA[" en de tag &lt;/search-data&gt; </span> wordt vervangen door " <span class="codeph"> ]]&gt; </span>". Een XML-parser parseert geen informatie tussen de open en close-tag. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-query query-number="XX" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>De query die de bezoeker heeft ingevoerd. Het geavanceerde, optionele kenmerk "query-number" bepaalt welke genummerde querytekenreeks wordt uitgevoerd door deze tag. <span class="codeph"> &lt;search-query-number=1&gt; </span> geeft bijvoorbeeld als uitvoer de inhoud van de cgi-parameter <span class="codeph"> sp_q_1 </span>. Als "vraag-aantal"niet wordt gespecificeerd, of als vraag-aantal "0"is, is de belangrijkste vraag ( <span class="codeph"> sp_q </span>) output. Het optionele kenmerk "encoding" bepaalt of de uitvoer HTML-gecodeerd, JavaScript-gecodeerd, Perl-gecodeerd, URL-gecodeerd of niet gecodeerd is voor uitvoer op de resultatenpagina. De standaardwaarde van "encoding" is "html". Normaal gesproken hoeft u het coderingskenmerk niet op te geven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-total&gt; </span> </p> </td> 
   <td colname="col2"> <p>Het totale aantal resultaten voor deze zoekopdracht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>Het aantal resultaten dat voor deze pagina wordt gerapporteerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-lower&gt; </span> </p> </td> 
   <td colname="col2"> <p>Het nummer van het eerste resultaat dat voor deze pagina wordt gerapporteerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-upper&gt; </span> </p> </td> 
   <td colname="col2"> <p>Het nummer van het laatste resultaat dat voor deze pagina is gerapporteerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-prev-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>Het aantal resultaten dat is gerapporteerd voor de vorige pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-next-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>Het aantal resultaten dat wordt gerapporteerd voor de volgende pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-time&gt; </span> </p> </td> 
   <td colname="col2"> <p>De tijd in seconden voor deze zoekopdracht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-logo&gt; </span> </p> </td> 
   <td colname="col2"> <p>De HTML voor het zoeklogo dat voor uw account is geconfigureerd, indien aanwezig. Dit logo is de afbeelding die krediet biedt voor het zoeken/verhandelen van sites </p> <p>De meeste accounts beschikken momenteel niet over een gekoppeld zoeklogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-collection all="name"&gt; </span> </p> </td> 
   <td colname="col2"> <p>De verzameling van de resultaten voor deze zoekopdracht. Het optionele kenmerk "all" wordt gebruikt om de naam te geven van de verzameling die de gehele website vertegenwoordigt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-form&gt; ...&lt;/search-form&gt; </span> </p> </td> 
   <td colname="col2"> <p>Hiermee voegt u begin- en eindformuliercodes in. Hiermee voegt u de methode- en actiekenmerken in de beginformuliertag in. Accepteert aanvullende kenmerken, zoals het kenmerk dir="RTL" voor taal en JavaScript-gerelateerde "name"- en "onSubmit"-kenmerken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input-account&gt; </span> </p> </td> 
   <td colname="col2"> <p>Hiermee voegt u een formulierinvoertag in die uw accountnummer opgeeft. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input-gallery&gt; </span> </p> </td> 
   <td colname="col2"> <p>Hiermee voegt u een formulierinvoertag in die het galerienummer opgeeft. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input-query query-number="XX"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Hiermee voegt u een formulierinvoertag in die de queryreeks opgeeft. Het geavanceerde, optionele kenmerk "query-number" bepaalt welke genummerde query wordt gebruikt voor de formulierinvoertag. <span class="codeph"> &lt;search-input-query-number=1&gt; </span> geeft bijvoorbeeld een formulierinvoertag uit voor de query <span class="codeph"> sp_q_1 </span>. Als "vraag-aantal"niet wordt gespecificeerd, of als "vraag-aantal""0"is, wordt een inputmarkering voor het belangrijkste <span class="codeph"> sp_q </span> vraag opgenomen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input-collections all="name"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Hiermee voegt u een formulierselectietag en de bijbehorende HTML in waarin het menu voor het selecteren van verzamelingen wordt weergegeven. Het optionele kenmerk "all" wordt gebruikt om de naam te geven van de verzameling die de gehele website vertegenwoordigt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>19 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-lt&gt; </span> </p> </td> 
   <td colname="col2"> <p>Hiermee voegt u de uitvoer van een van de sjabloontags voor zoeken in andere HTML- of sjabloontags in op de resultatenpagina. <span class="codeph"> &lt;search-lt&gt; </span> voegt een kleiner dan teken in. Met <span class="codeph"> &lt;search-lt&gt; </span> en <span class="codeph"> &lt;search-gt&gt; </span> kunt u de definitie van een tag omzeilen, zodat u sjabloontags zoeken als kenmerkwaarden kunt gebruiken. Wanneer de sjabloon wordt weergegeven als reactie op een zoekopdracht, vervangt een kleiner-dan-teken (&lt;) de <span class="codeph"> &lt;search-lt&gt; </span>-tag. <span class="codeph"> &lt;search-link&gt; </span> is bijvoorbeeld gelijk aan <span class="codeph"> &lt;search-lt&gt;a href="&lt;search-url&gt;"&lt;search-gt&gt; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>20 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-gt&gt; </span> </p> </td> 
   <td colname="col2"> <p>Hiermee voegt u de uitvoer van een van de sjabloontags voor zoeken in andere HTML- of sjabloontags in op de resultatenpagina. <span class="codeph"> &lt;search-gt&gt; </span> voegt een groter teken in. Met <span class="codeph"> &lt;search-lt&gt; </span> en <span class="codeph"> &lt;search-gt&gt; </span> kunt u de definitie van een tag omzeilen, zodat u andere sjabloontags kunt gebruiken als kenmerkwaarden. Wanneer de sjabloon wordt weergegeven als reactie op een zoekopdracht, wordt de tag <span class="codeph"> &lt;search-gt&gt; </span> vervangen door een groter dan-teken (&gt;). <span class="codeph"> &lt;search-link&gt; </span> is bijvoorbeeld gelijk aan <span class="codeph"> &lt;search-lt&gt;a href="&lt;search-url&gt;"&lt;search-gt&gt; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>21 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-param name="param-name" length="XX" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Retourneert de waarde van de cgi-parameter met de naam "param-name" in de huidige zoekopdracht. Het optionele kenmerk "encoding" bepaalt of de uitvoer HTML-gecodeerd, JavaScript-gecodeerd, Perl-gecodeerd, URL-gecodeerd of niet gecodeerd is voor uitvoer op de resultatenpagina. De standaardwaarde van "encoding" is "html". Normaal gesproken hoeft u het coderingskenmerk niet op te geven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>22 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW for S&P 8.17.0 release on October 30 2014--> <span class="codeph"> &lt;search-trace encoding="html/javascript/ json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> 
    <!--<p>This global core search template tag outputs a representation of the submitted core search query, including any "fuzzy-search" query term expansions that happen by way of synonyms, sound-alikes, and so forth. </p>--> <p>Het <span class="codeph">-coderingskenmerk </span> is optioneel. de standaardwaarde is <span class="codeph"> json </span>. </p> <p> <p>Opmerking:  Deze markering heeft slechts output als <span class="codeph"> sp_trace=1 </span> met de parameters van de kernonderzoeksvraag wordt gespecificeerd. </p> </p> <p>Zie rij 48 in de lijst die in <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" format="dita" scope="local"> wordt gevonden Achterste onderzoek CGI parameters</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Labels voor sjabloonankerkoppelingen {#section_3A51D27616C541E2B818CC52B2B856BA}

De volgende tags zorgen ervoor dat er een ankerkoppeling wordt aangebracht rondom de HTML tussen de tags. Wanneer op de ankerkoppeling wordt geklikt, wordt een andere pagina met resultaten weergegeven. Het optionele kenmerk &quot;count&quot; vraagt om veel resultaten op de pagina die moet worden weergegeven. Als u geen waarde opgeeft, wordt het aantal dat op de huidige pagina is aangevraagd, gebruikt. Het geavanceerde, optionele kenmerk &quot;URL&quot; bepaalt het domein waarnaar de gekoppelde koppeling wordt geleid. Standaard is het domein `https://search.atomz.com/search/`, maar u kunt dit wijzigen met het kenmerk URL.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-next URL="https://search.yourdomain.com/search/"&gt; ...  &lt;/search-next&gt; </span> </p> <p> <span class="codeph"> &lt;search-prev URL="https://search.yourdomain.com/search/"&gt; ...  &lt;/search-prev&gt; </span> </p> </td> 
   <td colname="col2"> <p>Hiermee geeft u de volgende of vorige pagina van de resultaten weer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-sort-by-date URL="https://search.yourdomain.com/search/"&gt; ...  &lt;/search-sort-by-date&gt; </span> </p> <p> <span class="codeph"> &lt;search-sort-by-score URL="https://search.yourdomain.com/search/"&gt; ...  &lt;/search-sort-by-score&gt; </span> </p> </td> 
   <td colname="col2"> <p>Hiermee sorteert u de resultaten op datum of op relevantie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-show-summaries URL="https://search.yourdomain.com/search/"&gt; ...  &lt;/search-show-summaries&gt; </span> </p> <p> <span class="codeph"> &lt;search-hide-summaries URL="https://search.yourdomain.com/search/"&gt; ...  &lt;/search-hide-summaries&gt; </span> </p> </td> 
   <td colname="col2"> <p>Hiermee toont of verbergt u de overzichten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Voorwaardelijke tags voor sjablonen {#section_18D9BC66DE484881932FD2F7EA9D170D}

Tags waarmee u voorwaardelijk HTML tussen de tags kunt opnemen.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-results&gt; ...  &lt;/search-if-results&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-results&gt; ...&lt;/search-if-not-results&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze tags zijn onder andere HTML als de huidige pagina zoekresultaten bevat (of geen). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-prev-count&gt; ...  &lt;/search-if-prev-count&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-prev-count&gt; ...  &lt;/search-if-not-prev-count&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-next-count&gt; ...  &lt;/search-if-next-count&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-next-count&gt; ...  &lt;/search-if-not-next-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze labels bevatten HTML als er aan de vorige of volgende pagina (of geen) resultaten zijn gekoppeld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-sort-by-score&gt; ...  &lt;/search-if-sort-by-score&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-sort-by-score&gt; ...  &lt;/search-if-not-sort-by-score&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-sort-by-date&gt; ...  &lt;/search-if-sort-by-date&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-sort-by-date&gt; ...  &lt;/search-if-not-sort-by-date&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze labels bevatten HTML als de huidige pagina al dan niet op relevantie of datum is gesorteerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-show-summaries&gt; ...  &lt;/search-if-show-summaries&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-hide-summaries&gt; ...  &lt;/search-if-hide-summaries&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze labels bevatten HTML als op de huidige pagina samenvattingen worden weergegeven of verborgen. U kunt deze tags gebruiken om een gedeelte van het zoekresultaat op te nemen of uit te sluiten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-input-collections&gt; ...  &lt;/search-if-input-collections&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-input-collections&gt; ...  &lt;/search-if-not-input-collections&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze tags bevatten HTML als een verzameling is opgegeven in het genereren van zoekresultaten voor de huidige pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-advanced&gt; ...  &lt;/search-if-advanced&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-advanced&gt; ...  &lt;/search-if-not-advanced&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze markeringen omvatten HTML als <span class="codeph"> sp_advanced=1 </span> CGI parameter voor de onderzoeksvraag werd gespecificeerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-bad-param name="parameter-name"&gt; ...  &lt;/search-if-bad-param&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-bad-param name="parameter-name"&gt; ...  &lt;/search-if-not-bad-param&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze tags bevatten of sluiten de HTML tussen deze tags uit als de opgegeven parameter ongeldig is of niet. </p> <p>Momenteel wordt alleen de <span class="codeph"> sp_q_location[_#] </span>-parameter ondersteund. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-param name="param-name" value="param-value"&gt; ...  &lt;/search-if-param&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-param name="param-name" value="param-value"&gt; ...  &lt;/search-if-not-param&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze geavanceerde tags bevatten de HTML tussen de tags op basis van het feit of de CGI-parameter die is opgegeven in het kenmerk "name" de waarde heeft die is opgegeven in het kenmerk "value". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-sort-by-field name="field-name"&gt; ...  &lt;/search-if-sort-by-field&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-sort-by-field name="field-name"&gt; ...  &lt;/search-if-not-sort-by-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze geavanceerde tags bevatten de HTML tussen de tags als de huidige pagina wordt of niet wordt gesorteerd op de opgegeven veldnaam. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Sjabloonformulierbesturingscodes {#section_45AFC414ACA74825B72FEAA8456F8DD2}

Tags waarmee u de standaardselectiestatus voor selectievakjes, keuzerondjes en keuzelijsten in een `<form>` op de zoeksjabloon kunt bepalen.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input&gt; </span> </p> </td> 
   <td colname="col2"> <p>Wordt gebruikt in een sjabloon in plaats van een <span class="codeph"> &lt;input&gt; </span>-tag. Wanneer de tag naar de browser wordt geschreven, wordt <span class="codeph">-invoer </span> vervangen door <span class="codeph">-zoekinvoer </span> en wordt alle andere informatie in de tag 'as-is' uitgevoerd. Als de <span class="codeph">-naam </span> in de tag als CGI-parameter wordt vermeld en als de <span class="codeph">-waarde </span> in de tag de waarde voor die CGI-parameter is, wordt bovendien het woord <span class="codeph"> gecontroleerd </span> toegevoegd aan het einde van de tag. Op deze manier kunt u automatisch de status van het standaardkeuzerondje of selectievakje in uw zoekresultaat gelijk maken aan die van de huidige query. </p> <p>De HTML-code voor een selectievakje kan er bijvoorbeeld als volgt uitzien: </p> <p> <span class="codeph"> &lt;input type="checkbox" name="sp_w" value="exact"&gt;Geen overeenkomende geluiden  </span> </p> <p>De overeenkomstige malplaatjecode voor dat checkbox is het volgende: </p> <p> <span class="codeph"> &lt;search-input type="checkbox" name="sp_w" value="exact"&gt;Geen overeenkomende geluiden  </span> </p> <p>Als de CGI-parametertekenreeks voor de query <span class="codeph"> sp_w=exact </span> bevat, ziet de tag die naar de browser wordt geschreven met de zoekresultaten er als volgt uit (het woord <span class="codeph"> ingeschakeld </span> wordt ingevoegd aan het einde van de tag): </p> <p> <span class="codeph"> &lt;input type="checkbox" name="sp_w" value="exact" checked=""&gt;Geen overeenkomende geluiden  </span> </p> <p>Als de CGI-parametertekenreeks voor de query geen <span class="codeph"> sp_w=exact </span> bevat, ziet de tag die met de zoekresultaten naar de browser wordt geschreven er als volgt uit (het woord <span class="codeph"> ingeschakeld </span> is niet opgenomen in de tag): </p> <p> <span class="codeph"> &lt;input type="checkbox" name="sp_w" value="exact"&gt;Geen overeenkomende geluiden  </span> </p> <p>De tag <span class="codeph"> &lt;search-input&gt; </span> is handig om selectievakjes en keuzerondjes in uw zoeksjabloon te plaatsen. Als u selectievakjes of keuzerondjes hebt die u aan <span class="codeph"> &lt;form&gt; </span> in uw zoeksjabloon wilt toevoegen, gebruikt u <span class="codeph"> &lt;search-input...&gt; </span> in plaats van <span class="codeph"> &lt;input...&gt; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-select&gt; ...  &lt;/search-select&gt; </span> </p> <p> <span class="codeph"> &lt;search-option&gt; ...  &lt;/search-option&gt; </span> </p> </td> 
   <td colname="col2"> <p>Vervolgkeuzelijsten in een <span class="codeph"> &lt;form&gt; </span>-tag worden gestart met een <span class="codeph"> &lt;select&gt; </span>-tag en eindigen met een <span class="codeph"> &lt;/select&gt; </span>-tag. De <span class="codeph">-naam </span> voor de bijbehorende CGI-parameter wordt vermeld in de <span class="codeph"> &lt;select&gt; </span>-tag. Na de <span class="codeph"> &lt;select&gt; </span>-tag volgt een lijst met <span class="codeph"> &lt;option&gt; </span>-tags die de waarden opgeven die in het lijstvak moeten worden weergegeven. </p> <p>De <span class="codeph"> &lt;search-select&gt; </span>, <span class="codeph"> &lt;/search-select&gt; </span>, <span class="codeph"> &lt;search-option&gt; </span> en <span class="codeph"> &lt;/search-option&gt; </span> &lt;a7/&gt; bieden vergelijkbare functionaliteit als de <span class="codeph"> &lt;search-input&gt; </span>-tag. Het woord <span class="codeph"> geselecteerd </span> wordt dus automatisch toegevoegd aan het einde van de <span class="codeph"> &lt;option&gt; </span>-tag die naar de browser wordt verzonden als de <span class="codeph">-naam </span> in <span class="codeph"> </span> &lt;a7/&gt;-tag als CGI-parameter wordt vermeld en als de <span class="codeph">-waarde </span> van die CGI-parameter is vermeld als <span class="codeph"> waarde </span> in een bepaalde <span class="codeph"> &lt;search-option&gt; </span> markering. Op deze manier kunt u de standaardkeuzelijst in uw zoekresultaat automatisch gelijk maken aan de huidige query. </p> <p>Een keuzelijst die standaard bijvoorbeeld als volgt wordt weergegeven: </p> <p> <code class="syntax html"> &lt;select&nbsp;name="sp_x"&nbsp;size=1&gt; 
      &lt;option&nbsp;value="any"&nbsp;selected&gt;Anywhere&lt;/option&gt; 
      &lt;option&nbsp;value="title"&gt;Title&lt;/option&gt; 
      &lt;option&nbsp;value="desc"&gt;Description&lt;/option&gt; 
      &lt;option&nbsp;value="keys"&gt;Keywords&lt;/option&gt; 
      &lt;option&nbsp;value="body"&gt;Body&lt;/option&gt; 
      &lt;option&nbsp;value="alt"&gt;Alternate&nbsp;text&lt;/option&gt; 
      &lt;option&nbsp;value="url"&gt;URL&lt;/option&gt; 
      &lt;option&nbsp;value="target"&gt;Target&lt;/option&gt; 
      &lt;/select&gt; </code> </p> <p>De bijbehorende sjablooncode voor dat lijstvak is als volgt: </p> <p> <code class="syntax html"> &lt;search-select&nbsp;name="sp_x"&nbsp;size=1&gt; 
      &lt;search-option&nbsp;value="any"&gt;Anywhere&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="title"&gt;Title&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="desc"&gt;Description&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="keys"&gt;Keywords&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="body"&gt;Body&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="alt"&gt;Alternate&nbsp;text&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="url"&gt;URL&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="target"&gt;Target&lt;/search-option&gt; 
      &lt;/search-select&gt; </code> </p> <p>Als u keuzelijsten hebt die u aan <span class="codeph"> &lt;form&gt; </span> in uw onderzoekssjabloon wilt toevoegen, gebruik <span class="codeph"> &lt;search-select...&gt; </span> in plaats van <span class="codeph"> &lt;select...&gt; </span>, <span class="codeph"> &lt;/search-select&gt; </span> <span class="codeph"> &lt;/select&gt; </span>, <span class="codeph"> &lt;search-option...&gt; </span> in plaats van <span class="codeph"> &lt;option..&gt; </span> en <span class="codeph"> &lt;/search-option&gt; </span> in plaats van <span class="codeph"> &lt;/option&gt; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-sort-by-field name="field-name" count="XX"&gt; ...  &lt;/search-sort-by-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze geavanceerde tags maken een ankerkoppeling rondom de HTML. Wanneer op dit anker wordt geklikt, wordt een pagina met resultaten weergegeven die in het opgegeven veld zijn gesorteerd. Het optionele <span class="codeph"> count </span>-kenmerk geeft het aantal resultaten op dat op de resultatenpagina moet worden weergegeven. Als <span class="codeph"> aantal </span> wordt weggelaten, wordt de telling gebruikt die op de huidige pagina wordt gebruikt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Tekenreeksen datumnotatie {#section_4BBDBBEF2B96414497617CD4B52D96E4}

U kunt de volgende omzettingsspecificaties in datumformaatkoorden gebruiken:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Tekenreeks datumnotatie </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>%A </p> </td> 
   <td colname="col2"> <p> Komt overeen met de nationale representatie van de volledige weekdagnaam, bijvoorbeeld "maandag". De instelling in <span class="uicontrol"> Talen </span> &gt; <span class="uicontrol"> Woorden en talen </span> &gt; <span class="uicontrol"> Taal </span> bepaalt de nationale vertegenwoordiging. </p> <p>Zie <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> Woorden en taal</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%a </p> </td> 
   <td colname="col2"> <p> Komt overeen met de nationale representatie van de afgekorte weekdagnaam, waarbij de afkorting de eerste drie tekens is, bijvoorbeeld "Mon". De instelling in <span class="uicontrol"> Talen </span> &gt; <span class="uicontrol"> Woorden en talen </span> &gt; <span class="uicontrol"> Taal </span> bepaalt de nationale vertegenwoordiging. </p> <p>Zie <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> Woorden en taal</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%B </p> </td> 
   <td colname="col2"> <p> Komt overeen met de nationale vertegenwoordiging van de volledige naam van de maand, bijvoorbeeld "June". De instelling in <span class="uicontrol"> Talen </span> &gt; <span class="uicontrol"> Woorden en talen </span> &gt; <span class="uicontrol"> Taal </span> bepaalt de nationale vertegenwoordiging. </p> <p>Zie <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> Woorden en taal</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%b </p> </td> 
   <td colname="col2"> <p> Komt overeen met de nationale representatie van de afgekorte naam van de maand, waarbij de afkorting de eerste drie tekens is, bijvoorbeeld "Jun". De instelling in <span class="uicontrol"> Talen </span> &gt; <span class="uicontrol"> Woorden en talen </span> &gt; <span class="uicontrol"> Taal </span> bepaalt de nationale vertegenwoordiging. </p> <p>Zie <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> Woorden en taal</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%D </p> </td> 
   <td colname="col2"> <p>Gelijk aan "%m/%d/%y", bijvoorbeeld "07/25/13". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%d </p> </td> 
   <td colname="col2"> <p> Komt overeen met de dag van de maand als een decimaal getal (01-31). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%e </p> </td> 
   <td colname="col2"> <p> Komt overeen met de dag van de maand als een decimaal getal (1-31). Een lege waarde komt voor één cijfer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%H </p> </td> 
   <td colname="col2"> <p> Komt de klok van 24 uur als decimaal aantal (00-23) aan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%h </p> </td> 
   <td colname="col2"> <p> Komt overeen met de nationale representatie van de afgekorte naam van de maand, waarbij de afkorting de eerste drie tekens is, bijvoorbeeld "Jun" (gelijk aan %b). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%I </p> </td> 
   <td colname="col2"> <p> Komt de klok van 12 uur als decimaal aantal (01-12) aan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%j </p> </td> 
   <td colname="col2"> <p> Komt overeen met de dag van het jaar als een decimaal getal (001-366). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%k </p> </td> 
   <td colname="col2"> <p> Komt overeen met de (24-uurs klok als decimaal aantal (0-23). Een lege waarde komt voor één cijfer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%l </p> </td> 
   <td colname="col2"> <p> Komt de uurklok van 12 uur als decimaal aantal (1-12) aan. Een lege waarde komt voor één cijfer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%M </p> </td> 
   <td colname="col2"> <p> Komt overeen met de minuut als een decimaal getal (00-59). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%m </p> </td> 
   <td colname="col2"> <p> Komt overeen met de maand als een decimaal getal (01-12). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%p </p> </td> 
   <td colname="col2"> <p> Komt overeen met de nationale vertegenwoordiging van "ante meridiem" of "post meridiem", zoals toepasselijk, bijvoorbeeld "PM". De instelling in <span class="uicontrol"> Talen </span> &gt; <span class="uicontrol"> Woorden en talen </span> &gt; <span class="uicontrol"> Taal </span> bepaalt de nationale vertegenwoordiging. </p> <p>Zie <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> Woorden en taal</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%R </p> </td> 
   <td colname="col2"> <p>Equivalent met "%H:%M", bijvoorbeeld "13:23". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%r </p> </td> 
   <td colname="col2"> <p>Equivalent met "%I:%M:%S %p", bijvoorbeeld "01:23:45 PM". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%S </p> </td> 
   <td colname="col2"> <p> Komt overeen met het tweede getal als een decimaal getal (00-60). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%T </p> </td> 
   <td colname="col2"> <p>Equivalent met "%H:%M:%S", bijvoorbeeld "13:26:47". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%U </p> </td> 
   <td colname="col2"> <p> Komt overeen met het weeknummer van het jaar (zondag als de eerste dag van de week) als een decimaal getal (00-53). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%v </p> </td> 
   <td colname="col2"> <p>Equivalent met "%e-%b-%Y", bijvoorbeeld "25-jul-2013". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%Y </p> </td> 
   <td colname="col2"> <p> Komt overeen met het jaar met eeuw als decimaal getal, bijvoorbeeld "2013". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%y </p> </td> 
   <td colname="col2"> <p> Komt overeen met het jaar zonder eeuw als decimaal getal (00-99). </p> </td> 
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

## Taalid&#39;s {#section_0490DECC00E34691ADE5A9ED90A6D911}

De volgende tabel bevat de taal-id&#39;s voor elke ondersteunde taal. U kunt deze id&#39;s gebruiken als waarden voor het optionele kenmerk &quot;language&quot; in de volgende sjabloontags:

* `search-date` en  `search-display-field`.

   Zie [Resultaatreekstags](../c-appendices/c-templates.md#section_80D68334E8D04A33937A6E58ABAAA320).

* `search-field-value-list` Zie  [Lijstlabels](../c-appendices/c-templates.md#section_D3298B5F976447DBA0032B883DCC91B1) voor veldwaarden.

* `search-field-value` Zie  [Lustags](../c-appendices/c-templates.md#section_0717FA09F0FC449CB916883B0500A60E) in de lijst met veldwaarden.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Taal </p> </th> 
   <th colname="col2" class="entry"> <p>Taalid </p> </th> 
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
   <td colname="col1"> <p>Tsjechisch (Tsjechië) </p> </td> 
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
   <td colname="col2"> <p> en_GB </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Engels (Verenigde Staten) </p> </td> 
   <td colname="col2"> <p> nl_NL </p> </td> 
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
   <td colname="col2"> <p> it_IT </p> </td> 
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
   <td colname="col2"> <p> no_NO </p> </td> 
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
   <td colname="col1"> <p>Russisch (voormalige Sovjet-Unie) </p> </td> 
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

## De HTTP-header van het inhoudstype opgeven {#section_AEED823E9938448A9EDB2F286D9CFD90}

U kunt de HTTP-antwoordheader van het type Content-Type opgeven met behulp van de volgende tag:

`<search-content-type-header [content="MIME-type"] [charset="charset-name"]>`

De kenmerken `content` en `charset` zijn optioneel. Deze tag moet zo vroeg mogelijk in de sjabloon worden weergegeven. Het wordt ook aanbevolen deze vóór `<search-html-meta-charset>` of `<search-xml-decl>` te plaatsen, omdat deze het gedrag van deze tags beïnvloedt.

Als u het `content` attribuut niet specificeert, dan blijft de waarde van `MIME-type` aan de waarde die in **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]** wordt geplaatst. Als u een `content` attribuut specificeert, wordt het gebruikt als standaard `content` attribuut voor `<search-html-meta-charset>` markering.

Als u het `charset` attribuut niet specificeert, dan wordt geen `charset` waarde geschreven aan `content-type` kopbal.

Als u `charset="1"` specificeert dan is de daadwerkelijke waarde voor `charset-name` de waarde van de `sp_f` parameter CGI. Als er bij de zoekopdracht geen `sp_f` CGI-parameter wordt verzonden, wordt de werkelijke waarde voor `charset-name` gelezen uit uw accountinstellingen. U kunt de tekenset die aan uw account is gekoppeld, weergeven of wijzigen onder **[!UICONTROL Settings]** > **[!UICONTROL My Profile]** > **[!UICONTROL Personal Information]** > **[!UICONTROL Character Encoding]**.

Zie [Uw persoonlijke gebruikersinformatie configureren](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6).

U kunt een specifieke naam van een tekenset kiezen door deze als `charset`-waarde op te geven, zoals `charset="iso-8859-1"` of `charset="Shift-JIS"`.

Als u een `charset` attribuut specificeert, dan wordt het gebruikt als standaard `charset` attribuut voor `<search-html-meta-charset>` en `<search-xml-decl>` markeringen, evenals output aan `content-type` kopbal.

## Een tekenset opgeven in een HTML-sjabloon {#section_E0D1816ABB5846BEBE9C26D5980CCBE6}

De standaard HTML-zoekresultaatsjablonen geven de tekenset aan die aan het huidige account is gekoppeld via de volgende tag:

`<search-html-meta-charset [content="MIME-type"] [charset="charset-name"]>`

De kenmerken voor inhoud en tekensets zijn optioneel. Deze tag moet worden weergegeven in de HTML `<head>`-sectie van de sjabloon. Deze tag resulteert in de volgende tag op de HTML-pagina die wordt gegenereerd op basis van de sjabloon:

`<meta http-equiv="content-type" content="MIME-type; charset=charset-name">`

Als u het inhoudskenmerk niet opgeeft, wordt de werkelijke waarde van `MIME-type` standaard ingesteld op een van twee waarden. Als de tag `<search-content-type-header>` een kenmerk `content` heeft opgegeven, wordt die waarde gebruikt. Anders wordt de waarde gebruikt die is ingesteld op het tabblad **[!UICONTROL Templates]** > **[!UICONTROL Settings]** > **[!UICONTROL Content Type]**.

Als u het `charset` attribuut niet specificeert, dan blijft de daadwerkelijke waarde van `charset-name` aan één van twee waarden in gebreke. Als de tag `<search-content-type-header>` een kenmerk `charset` heeft opgegeven, wordt die waarde gebruikt. Anders wordt de werkelijke waarde voor `charset-name` gelezen uit uw accountinstellingen. U kunt de tekenset die aan uw account is gekoppeld, weergeven of wijzigen onder **[!UICONTROL Settings]** > **[!UICONTROL My Profile]** > **[!UICONTROL Personal Information]** > **[!UICONTROL Character Encoding]**.

Zie [Uw persoonlijke gebruikersinformatie configureren](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6).

Als u `charset="1"` specificeert dan is de daadwerkelijke waarde voor `charset-name` de waarde van de `sp_f` parameter CGI. Als er bij de zoekopdracht geen `sp_f` CGI-parameter wordt verzonden, is de werkelijke waarde voor `charset-name` ofwel de waarde die is ingesteld in de tag `<search-content-type-header>` als deze is opgegeven, ofwel de waarde die is ingesteld in de accountinstellingen.

U kunt een specifieke naam van een tekenset opgeven, zoals in `charset="charset-name"`. Bijvoorbeeld `charset="iso-8859-1"` of `charset="Shift-JIS"`.

De tag `<search-html-meta-charset>` is optioneel. Als u het verwijdert, neemt browser de standaardwaarden voor `content-type`, die het volgende is: `content="text/html; charset=ISO-8859-1"`. U kunt er ook voor kiezen om de tag `<search-html-meta-charset>` te vervangen door uw eigen tag `http-equiv`.

## Een tekenset opgeven in een XML-sjabloon {#section_17DC31CDCC104F5F8081466B41A96E9D}

In de standaard XML-zoekresultaatsjabloon wordt de tekenset opgegeven die aan de huidige account is gekoppeld met de volgende tag:

`<search-xml-decl [charset="charset-name"]>`

Het kenmerk `charset` is optioneel. Dit label moet boven aan de sjabloon staan, maar na elke tag `<search-content-type-header>`. Deze tag resulteert in de volgende tag in het XML-document dat wordt gegenereerd op basis van de sjabloon:

`<?xml version="1.0" encoding="charset-name" standalone="yes" ?>`

Als u `charset` niet specificeert, dan blijft de daadwerkelijke waarde van `charset-name` aan één van twee waarden in gebreke. Als `<search-content-type-header>` een `charset` attribuut specificeerde, dan wordt die waarde gebruikt. Anders wordt de werkelijke waarde voor `charset-name` gelezen uit uw accountinstellingen. U kunt de tekenset die aan uw account is gekoppeld, weergeven of wijzigen onder **[!UICONTROL Settings]** > **[!UICONTROL My Profile]** > **[!UICONTROL Personal Information]** > **[!UICONTROL Character Encoding]**.

Zie [Uw persoonlijke gebruikersinformatie configureren](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6).

Als u `charset="1"` specificeert dan is de daadwerkelijke waarde voor `charset-name` de waarde van de `sp_f` parameter CGI. Als er bij de zoekopdracht geen `sp_f` CGI-parameter wordt verzonden, is de werkelijke waarde voor `charset-name` ofwel de waarde die is ingesteld in de `<search-content-type-header>`-tag als deze is opgegeven, ofwel de waarde die is ingesteld in de accountinstellingen.

U kunt desgewenst een specifieke naam voor een tekenset opgeven, zoals in `charset="charset-name"`. Bijvoorbeeld, `charset="iso-8859-1" or charset="Shift-JIS"`.

U kunt de tag `<search-xml-decl>` vervangen door uw eigen tag `?xml`.

## Een zoeksjabloon opnemen in een andere {#section_7D1FCD3D9E2340C291E354C9720E8BC0}

Als u een zoeksjabloon in een andere sjabloon wilt opnemen, gebruikt u de tag `<search-include>`, waarbij u het bestandskenmerk instelt op de naam van het sjabloonbestand dat u wilt opnemen, zoals in het volgende voorbeeld:

`<search-include file="seo/seo_search_title.tpl" />`

Sjabloonsegmenten voor SEO-zoekopdrachten bevinden zich in de submap `seo/` en normale zoeksjablonen bevinden zich in de submap `templates/`. Alleen .tpl-bestanden zijn relevant voor opname in deze context.

## Meerdere transportsjablonen voor uw website beheren {#reference_12AAB3B9F4C74C11956F1DBA95714C2F}

U kunt de weergave van zoekresultaten op uw website bepalen door voor elk gebied verschillende sjablonen voor zoekopdrachten te gebruiken.

<!-- 

r_managing_multiple_templates.xml

 -->

Om dit soort onderzoeksfunctionaliteit te verwezenlijken, kunt u uw vervoermalplaatjes in plaatsonderzoek/handel beheren. Of u kunt uw transportsjablonen beheren in Publiceren. Net als bij het zoeken/verhandelen van sites kunt u met Publiceren meerdere sjablonen voor zoekopdrachten bewerken, voorvertonen en publiceren.

Als u uw zoekformulieren wilt instellen voor het gebruik van een specifieke transportsjabloon (anders dan de standaardsjabloon), gebruikt u de query-parameter `sp_t`. Stel dat u een zoeksjabloon hebt met de naam &quot;klaring&quot; voor het gemarkeerde verkoopgebied van uw website. U gebruikt het standaard HTML-zoekformulier met de volgende aanvullende formuliercode:

`<input type=hidden name="sp_t" value="clearance">`

Wanneer een klant op een standaardformulier klikt dat deze coderegel bevat, wordt de transportsjabloon voor het zoeken naar &#39;klaring&#39; samen met de zoekresultaten weergegeven.

Zie [Verzamelingen gebruiken in zoekformulieren](../c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3).

Zie [Frames gebruiken met formulieren](../c-appendices/c-searchforms.md#reference_82CDDDA1E37042E4849EBF7EA05407C5).

Zie [Voorbeeld van een geavanceerd zoekformulier](../c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A).
