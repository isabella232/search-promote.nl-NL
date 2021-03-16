---
description: U kunt Facets gebruiken om uw presentatielaag aan te passen en uw gebruikers van een Geleide Onderzoek te voorzien die hen neer in hun onderzoeksresultaten laat bogen.
solution: Target
subtopic: Navigation
title: Informatie over facetten
topic: Ontwerpen, zoeken en verhandelen van sites
uuid: 28bc4d4d-a84c-4a77-befb-b0fb3bbdb966
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '3832'
ht-degree: 0%

---


# Info over Facetten{#about-facets}

U kunt Facets gebruiken om uw presentatielaag aan te passen en uw gebruikers van een Geleide Onderzoek te voorzien die hen neer in hun onderzoeksresultaten laat bogen.

## Facetten {#concept_FA912B3B41EE493DB2F492D188457FF5} gebruiken

Stel bijvoorbeeld dat een bezoeker van een website die gereedschappen verkoopt, een zoekopdracht uitvoert naar websites. De onderneming kon gebruik maken van twee factoren: één om alle merken van gevonden kringen te specificeren, en tweede om alle moersleutelgrootte te specificeren. De klant kan op elk merk of elke grootte binnen het juiste facet klikken om de resultaten te verfijnen en snel de juiste moersleutel te vinden.

U kunt een facet op om het even welke bestaande meta-gegevensdefinitie baseren. Als een facet in de metagegevens wordt gedefinieerd als een Date-type, wordt het weergegeven als een datumbereikfacet.

In de tabel op de pagina [!DNL Staged Facets] ziet u een algemeen overzicht van de instellingen waaruit elk toegevoegd facet bestaat. U kunt nieuwe facetten toevoegen en bestaande facetten bewerken of verwijderen. U kunt alle wijzigingen die u aanbrengt in facetten herstellen met **[!UICONTROL History]** in de rechterbovenhoek van de pagina.

Facet-instellingen worden standaard trapsgewijs ingesteld, zodat u wijzigingen kunt testen voordat u ze live gaat.

Zie [Informatie over staging](../c-about-staging.md#concept_08B8F3CA1F4241108F14BA7FC7806CA7).

U kunt **[!UICONTROL View Live Settings]** gebruiken om uw gefaseerde montages met het huidige levende plaatsen te vergelijken. Gebruik **[!UICONTROL View Staged Settings]** om terug te keren naar het testgebied. Voor een item dat wordt gefaseerd, is de live versie van de instellingen alleen-lezen. U kunt de werkbalk dus manipuleren door de instellingen actief te maken. Nadat u tevreden bent met de wijzigingen die u hebt aangebracht in het gefaseerde facet, klikt u op **[!UICONTROL Push Live]** om deze live te zetten.

## Datumbereikfactoren {#section_FEFFF6B5B6534456913189FEF559BA58}

Facetten die in de metagegevens als type Date worden gedefinieerd, worden anders behandeld dan andere facetten. In plaats van te worden behandeld als een reeks waarden, worden ze behandeld als een datumbereik, met een startdatum, een einddatum of beide.

Een datumbereikfacet heeft een waarde van de begindatum, gevolgd door &quot;btw&quot; (voor &quot;tussen&quot;), gevolgd door de einddatum. Datums hebben de volgende twee indelingen:

dd-mm-yyyy

dd/mm/jjjj

Jaar met vier cijfers zijn vereist. Er moet ten minste één begindatum of einddatum zijn, maar beide zijn niet verplicht. &quot;12/1/2007BTW1/4/2009&quot; betekent bijvoorbeeld alle data tussen 1 december 2007 en 4 januari 2009. &quot;1-1-2005BTW&quot; betekent echter alle data sinds 1 januari 2005.

U kunt de sjabloontag `<guided-facet-value/>` van de presentatie gebruiken om de waarde van een datumbereik als een normaal facet op te halen. JavaScript is momenteel vereist om gebruikers de mogelijkheid te bieden datumbereiken in te voeren waarop ze kunnen zoeken. U kunt bijvoorbeeld de invoer uit twee invoervelden halen voor de begin- en einddatum. Vervolgens kunt u de invoer valideren en de waarde van het nieuwe facet (samengesteld uit de twee invoervelden) en de naam van het facet toevoegen aan de bestaande URL.

Zie [Labels voor presentatiesjablonen](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64).

Het volgende codevoorbeeld is een voorbeeld van hoe te om een datumwaaier op een pagina voor te stellen. Als deze optie is geselecteerd, wordt het bestaande datumbereik weergegeven. anders wordt er een eenvoudig invoerformulier weergegeven . Wanneer het formulier wordt verzonden, wordt eenvoudige validatie uitgevoerd. Vervolgens wordt de browser naar een nieuwe URL gestuurd die twee nieuwe parameters bevat:

* `q#` - Geeft het geselecteerde datumbereik aan dat is samengesteld uit de twee invoervelden.
* `x#` - Namen van facet. In dit voorbeeld krijgt de datumbereikfacet de naam &quot;modified&quot;.

De `replace(/%2F/ig, '~2F')` delen in de code zijn nodig omdat Apache `%2F` niet toestaat in URL wegen om veiligheidsredenen, en wanneer het gebruiken van SEO URLs is de vraag in de weg URL. Daarom wordt `/` gecodeerd als `~2F` in plaats van `%2F`, aangezien het normaal in een URL zou zijn.

```
<div class="date_range"> 
 <p>Date Range</p> 
 <guided-if-facet-selected gsname="modified"> 
  <guided-facet-values gsname="modified"> 
   <script> 
   var modified_daterange= '<guided-facet-value />'.split(/BTW/) ; 
   if (modified_daterange[0]=='') modified_daterange[0]= '--/--/----' ; 
   if (modified_daterange[1]=='') modified_daterange[1]= '--/--/----' ; 
   document.write('From: ' + modified_daterange[0]) ; 
   document.write('<br>To: ' + modified_daterange[1]) ; 
   </script> 
  </guided-facet-values> 
 
 <guided-else-facet-selected> 
  <form action="#"> 
   From: <input name="dateFrom" size=10> 
   <br>To: <input name="dateTo" size=10> 
   <br><input type="button" value="Go" onclick="goClick(this.form)"> 
  </form> 
  <script> 
  function goClick(f) { 
   if (f.dateFrom.value=='' && f.dateTo.value=='') { 
    alert('You must enter either a From: date or a To: date.') ; 
    return ; 
   } 
   if ( f.dateFrom.value!='' && !f.dateFrom.value.match(/^\d+[\/\-]\d+[\/\-]\d\d\d\d$/) ) { 
    alert('From: date must be in "mm/dd/yyyy" or "mm-dd-yyyy" format.') ; 
    return ; 
   } 
   if ( f.dateTo.value!='' && !f.dateTo.value.match(/^\d+[\/\-]\d+[\/\-]\d\d\d\d$/) ) { 
    alert('To: date must be in "mm/dd/yyyy" or "mm-dd-yyyy" format.') ; 
    return ; 
   } 
   // Note that "/" is encoded as "~2F" instead of "%2F" to avoid Apache 404 error. 
   var new_url= '<guided-current-path />&<guided-query-param-name gsname="q#" offset="0" />=' 
    + encodeURIComponent(f.dateFrom.value).replace(/%2F/ig, '~2F') + 'BTW' 
    + encodeURIComponent(f.dateTo  .value).replace(/%2F/ig, '~2F') 
    + '&<guided-query-param-name gsname="x#" offset="0" />=modified' ; 
   location.href= new_url ; 
  } 
  </script> 
 </guided-if-facet-selected> 
</div>
```

## Informatie over geneste facetten {#section_6BC77F38DE9F43D5B6911F8CECB15DFC}

Geneste facetten zijn facetten die meerdere niveaus van categorieën weergeven, zoals in het volgende voorbeeld:

![](assets/nestedfacets.png)

De categorieën Weens en Mens staan in het bovenste of bovenliggende facet. De subcategorieën, zoals Accessoires en Schoeisel, bevinden zich in het onderste of onderste facet.

De momenteel ondersteunde geneste facetdiepte is twee, maar deze kan overal in de keuzelijst staan.

Hieronder vindt u het gedrag van verschillende soorten geneste facetten:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Gedrag van geneste vlaktekst </p> </th> 
   <th colname="col2" class="entry"> <p>Gedrag </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Normaal </p> </td> 
   <td colname="col2"> <p>Het gedrag van een normaal geneste facet is dat deze kleiner wordt als andere facetten de zoekopdracht beperken. </p> <p>Als het geneste facet is geselecteerd, wordt het omlaag gekrompen in de richting van de selectie. Als een bovenliggend facet is geselecteerd, wordt alleen dat bovenliggende element weergegeven met alle onderliggende facetten. Als een onderliggend facet is geselecteerd, worden in het facet alleen het geselecteerde bovenliggende facet en het geselecteerde onderliggende facet weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vast </p> </td> 
   <td colname="col2"> <p>Het gedrag van een kleverig genest facet is dat het probeert het facet zo open mogelijk te houden op basis van de staat van andere facetten of zoekcriteria. Als het onderliggende facet is geselecteerd, telt het naar de kleverige diepte toe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Meerdere selecties </p> </td> 
   <td colname="col2"> <p>Het gedrag van een multi-select facet is dat het de facet open houdt. Nieuwe selecties proberen alle andere facetselecties uit te wissen, tenzij het facet een 'bovenliggend element' is van de categorie geneste facet. In dit geval verwijst "bovenliggend element" naar categoriefacetten, niet naar categorieën op hoofdniveau van een geneste facet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Meerdere categorieën selecteren </p> </td> 
   <td colname="col2"> <p>Net als het geneste facettype Multi-Select met de volgende uitzonderingen: </p> 
    <ul id="ul_D5AB6AF3169A483E8F3FC6D2A2EA3A28"> 
     <li id="li_9308156EF2FF43CE9DFB933F13786C58">Alle andere eerder gekozen facetten worden uitgeschakeld als dit facet voor het eerst wordt geselecteerd. </li> 
     <li id="li_DD96D6802A9C479283212A0FD68C6F85">Andere eerder gekozen facetten zijn ook uitgeschakeld als de klant rechtstreeks naar het onderliggende facet gaat zonder op het bovenliggende facet te klikken of als een andere bovenliggende facet op hetzelfde niveau wordt gekozen. </li> 
     <li id="li_8BF58F10969B4743986D5D0E0086AD6C">Ze kunnen ouders hebben in de zin dat facetten van de categorie ouders hebben. Verwar dit gedrag niet met ouder-kind verhoudingen die met alle genestelde facetten worden gevonden. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

Zie ook [Informatie over facetrails](../c-about-design-menu/c-about-facet-rails.md#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB).

## Een nieuw facet toevoegen {#task_FC07BFFA62CA4B718D6CBF4F2855C89B}

U kunt facetten toevoegen om uw presentatielaag aan te passen en uw klanten van een Geleide Onderzoek voorzien dat hen tot in hun onderzoeksresultaten kan boor.

<!-- 

t_adding_a_new_facet.xml

 -->

In de tabel met facetten op de pagina [!DNL Facets] ziet u een fragment van de instellingen die een enkel facet vormen. U kunt nieuwe facetten toevoegen en bestaande facetten bewerken of verwijderen. Wijzigingen die u aanbrengt in facetten, kunnen worden hersteld met de functie Historie.

>[!NOTE]
>
>Zorg ervoor dat u naar het facet in uw presentatiesjabloon verwijst, zodat dit zichtbaar is op de website.

Zie ook [Informatie over facetrails](../c-about-design-menu/c-about-facet-rails.md#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB).

**Een nieuw facet toevoegen**

1. Voordat u een nieuw facet kunt toevoegen, moet u controleren of u het volgende hebt gedaan voordat u verdergaat met de volgende stap:

   * Sommige velden voor metatag zijn al gedefinieerd.

      Zie [Een nieuw metatag toevoegen gebied](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).
   * Injecteer de metagegevens in uw index.
Zie [Veldinjectiedefinities toevoegen](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE).

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Facets.]**
1. Klik op [!DNL Facets] op de pagina.**[!UICONTROL Add New Facet]**
1. Stel op de pagina [!DNL Add Facet] de gewenste opties in.

   Deze instellingen zijn van invloed op zowel het gedrag als de standaardpresentatie van een facet. U kunt enkele van deze instellingen overschrijven met de instellingen van de presentatiesjabloon.

   Als een facet in de metagegevens wordt gedefinieerd als een Date-type, wordt het weergegeven als een datumbereik.

   Zie [Datumbereikfactoren](../c-about-design-menu/c-about-facets.md#section_FEFFF6B5B6534456913189FEF559BA58).

   Afhankelijk van de facetopties die u selecteert, zijn niet alle opties beschikbaar.

   <!-- 
   r_add_facet_options.xml
   -->

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Naam facet </p> </td> 
      <td colname="col2"> <p>Hiermee wordt de naam van een bepaald facet aangegeven. </p> <p> <p>Opmerking:  U kunt alleen een facet hebben op basis van bestaande door de gebruiker gedefinieerde metagegevens. Als de vervolgkeuzelijst geen facetten bevat, moet u eerst enkele metagegevens definiëren. </p> </p> <p>Zie <a href="../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5" type="task" format="dita" scope="local"> Een nieuw metatag toevoegen veld </a>. </p> <p>Als u een facet wilt maken op basis van een veldtabel, gebruikt u de naam van de aangepaste facet en geeft u de tabelnaam van het veld op. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Weergavelabel </p> </td> 
      <td colname="col2"> <p>Hiermee stelt u het label in van een facet dat u vervolgens kunt gebruiken in een breadcrumb in plaats van een metagegevensveldnaam (met de <span class="codeph"> &lt;guided-breadcrumb-label&gt; </span>-tag) of een zelfstandige waarde (met de <span class="codeph"> &lt;guided-facet-display-name&gt; </span>-tag). </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Gedrag </p> </td> 
      <td colname="col2"> <p>Hiermee stelt u een van de drie facetgedragingen in. </p> <p> 
      <ul id="ul_67C19E1C16224B9990F04A0D05BD3D05"> 
      <li id="li_6B232C11A61840B68CA59E1F593405A0"> <span class="uicontrol"> Normaal  </span> <p>Wanneer een klant op een facet klikt waarvan het gedrag is ingesteld op <span class="uicontrol"> Normaal </span>, boort het in de zoekresultaten voor dat item. Daarna kan de klant het aantal zoekresultaten verder verfijnen en beperken. </p> </li> 
      <li id="li_7D7C43A7F7AB4B84A9B0FEF34627605A"> <span class="uicontrol"> Categorie  </span> <p>Categoriefacetten fungeren als navigatie-elementen. Deze facetten zijn facetten op het hoogste niveau die klanten typisch door alvorens facetten met attributenopties te onthullen boren. Categoriefacetten zijn niet smal wanneer andere facetten worden geselecteerd en open blijven. Als u in een categorie-facet op een andere waarde klikt, wordt de selectie van alle andere facetten op de pagina opgeheven, behalve van de bovenliggende elementen van die categorie. </p> </li> 
      <li id="li_01255993D71F40DBA8870AA3FEA7D304"> <span class="uicontrol"> Meerdere categorieën selecteren  </span> <p>facetten zijn categoriefacetten die de selectie van veelvoudige punten van het facet steunen waar de punten "OFed"samen zijn. </p> </li> 
      </ul> 
      <ul id="ul_683F6D3FC8524E65AF303453ADDB6001"> 
        <li id="li_81F504D1D1294666BBBC5EA43B34B712"> <span class="uicontrol"> Vast  </span> <p>Wanneer een klant op een facet klikt waarvan het gedrag is ingesteld op <span class="uicontrol"> Vaste </span>, blijft het facet met de geselecteerde optie open tijdens de boor-down. Deze optie is handig wanneer u een klant een vorige keuze wilt laten wijzigen. </p> </li> 
      </ul> 
      <ul id="ul_8E871D63B09445268C600C8ABC20F6A4"> 
        <li id="li_F88AC5528B0C4751BC4CFE7FA9525857"> <span class="uicontrol"> Meerdere selecties  </span> <p>Hiermee kunt u meerdere items van een facet selecteren, waarbij de items in het facet samen "ORed" zijn. Deze optie is nuttig voor een facet dat een minder belangrijk attribuut zoals kleuren kan tonen en u wilt de klant de capaciteit laten om een vraag te bouwen die hen "toont schoenen in mijn grootte die rood of zwart zijn". </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Altijd tonen </p> </td> 
      <td colname="col2"> <p>Voor een normaal of kleverig facet, plaatst het facet om aan de klant op elk ogenblik zichtbaar te blijven. </p> <p>Deze optie is alleen beschikbaar als u <span class="uicontrol"> Normaal </span>, <span class="uicontrol"> Categorie </span> of <span class="uicontrol"> Nodig </span> in de vervolgkeuzelijst <span class="uicontrol"> Gedrag </span> hebt geselecteerd. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ouders van facet </p> </td> 
      <td colname="col2"> <p>Deze optie is alleen beschikbaar als u <span class="uicontrol"> Categorie </span> of <span class="uicontrol"> Categorie Multi-Select </span> in de vervolgkeuzelijst <span class="uicontrol"> Gedrag </span> hebt geselecteerd. </p> <p>Geeft aan wat de bovenliggende elementen van de categorie zijn. De geselecteerde items in de categorieën bovenliggende elementen worden gebruikt om de opties te beperken die beschikbaar zijn in de huidige categorie-facet. De optie Bovenliggende facetten wordt niet uitgeschakeld wanneer een klant communiceert met de categorie facet. U kunt meerdere door komma's gescheiden bovenliggende elementen opgeven. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Vaste diepte </p> </td> 
      <td colname="col2"> <p>Deze optie is alleen beschikbaar als u <span class="uicontrol"> Nodig </span> in de vervolgkeuzelijst <span class="uicontrol"> Gedrag </span> hebt geselecteerd. </p> <p>Hiermee stelt u het aantal opties in dat open blijft tijdens het indrukken van de boor. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Lengtedrempel </p> </td> 
      <td colname="col2"> <p>Hiermee stelt u de verticale lengte (1-9999) in van het facet dat in het aantal items is gedefinieerd. </p> <p>Als de presentatiesjabloon op de juiste wijze is ingesteld, kunt u deze instelling gebruiken om de tekst 'Meer weergeven..' op te geven. of bepaal wanneer u het facet in een schuifbaar div-element wilt plaatsen, enzovoort. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Drempel voor afknot-lengte </p> </td> 
      <td colname="col2"> <p>Kort het aantal items in een facet na een bepaalde drempel in. </p> <p>Sommige implementaties hebben facetten met duizenden punten in hen. Het kan duur zijn om alle gegevens over de draad te verzenden. U kunt deze instelling gebruiken om de facet tot een beheerbaar niveau bij te snijden. De facet wordt na het sorteren afgekapt. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Max. waardebreedte </p> </td> 
      <td colname="col2"> <p>Geeft een limiet aan voor de lengte van de tekenreeks facetwaarde (1-999). </p> <p>Deze optie is handig wanneer u een facet in een lay-out met vaste breedte wilt plaatsen en tekenreeksen niet door een omloop wilt laten omlopen. Standaard is de tekenreeks ingesteld op 3 tekens korter dan de drempel, zodat een ovaal kan worden toegevoegd. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Waardeextensie </p> </td> 
      <td colname="col2"> <p>Geeft de tekenreeks aan die u wilt gebruiken om aan te geven dat de waarde van een facet wordt afgekapt. Standaard wordt de tekenreeks ".." wordt gebruikt. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Scheidingsteken </p> </td> 
      <td colname="col2"> <p>Hiermee geeft u het scheidingsteken op dat moet worden gebruikt voor elke gescheiden-waardelijst met scheidingstekens die op de facet van toepassing is. </p> <p>Het scheidingsteken dat wordt gebruikt, is hetzelfde als dat is gedefinieerd in de metagegevens waarop het facet is gebaseerd. Het standaardscheidingsteken is een komma. U kunt echter elke XML-compatibele waarde gebruiken. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Sorteren </p> </td> 
      <td colname="col2"> <p>Hiermee geeft u op hoe facetten op uw website moeten worden gesorteerd. U kunt facetten hebben die door het volgende worden gesorteerd. U kunt maximaal vijf soorten combineren. </p> 
      <ul id="ul_12987F4DC7B34C63ABC906B59688A174"> 
      <li id="li_3206C96013DF431D90119F594D93D85D"> <span class="uicontrol"> alpha  </span> <p>Hiermee worden de waarden alfabetisch gesorteerd (0-9, A-Z), inclusief leestekens. </p> </li> 
      <li id="li_304E4A518FBE48D18D9E9EA7339A3481"> <span class="uicontrol"> alpha (alleen alfanumeriek)  </span> <p>Hiermee worden de waarden alfabetisch gesorteerd (0-9, A-Z), waarbij leestekens worden genegeerd. </p> </li> 
      <li id="li_CADB888CC514455F9CA379C8EEE490AA"> <span class="uicontrol"> alpha (niet hoofdlettergevoelig)  </span> <p>Hiermee worden de waarden alfabetisch gesorteerd (0-9, A-Z), waarbij alfabetische tekens worden genegeerd, inclusief leestekens. </p> </li> 
      <li id="li_F61122E79AB5413792DA31F8AB1414BD"> <span class="uicontrol"> alpha (niet hoofdlettergevoelig, alleen alfanumeriek)  </span> <p>Hiermee worden de waarden alfabetisch gesorteerd (0-9, A-Z), waarbij alfabetische tekens worden genegeerd en leestekens worden genegeerd. </p> </li> 
      <li id="li_F50CC298ABF046D0A39D5AE5B1261823"> <span class="uicontrol"> aantal  </span> <p>Sorteert het aantal resultaten dat overeenkomt met elke facetwaarde van het grootst tot het minst. </p> </li> 
      <li id="li_32B6AF39E9534762B39B15181DC5AD01"> <span class="uicontrol"> numeriek  </span> <p>De waarden worden numeriek gesorteerd. Bij het sorteren van getallen is deze optie beter dan een alfasortering, omdat bij een alfasortering 10 wordt weergegeven vóór 2. </p> </li> 
      <li id="li_CF8E76A7B1184E0C8DCC11B53E31A1DC"> <span class="uicontrol"> splitsen  </span> <p>Hiermee verdeelt u de lijst in twee aparte lijsten op basis van de teldrempel. Vlakwaarden boven de drempel worden naar boven verplaatst. De waarden van de facet met tellingen onder de drempel worden bewogen aan de bodem. Er is een gesplitste drempelwaarde vereist wanneer u wilt dat waarden van een bepaald bereik altijd bovenaan staan. </p> </li> 
      <li id="li_4AB8276577384B1099CBA895898205AD"> <span class="uicontrol"> break  </span> <p>Hiermee worden bepaalde waarden boven of onder aan de lijst geplaatst. U wilt bijvoorbeeld altijd de term "Overige" onder aan de lijst plaatsen. Bovenste of onderste waarden zijn vereist wanneer u een breuksortering gebruikt om de expliciete waarden te identificeren die zich boven of onder aan de sortering moeten bevinden. </p> </li> 
      <li id="li_227E96CFED2044FCA2F10B6913B03CFB"> <span class="uicontrol"> geordend  </span> <p>De waarden van facetten moeten altijd in een vaste volgorde staan (een lijst met gescheiden waarden van scheidingstekens die is gedefinieerd in de onderstaande optie <span class="uicontrol"> Volgorde </span>). </p> </li> 
      </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Alias van Facet </p> </td> 
      <td colname="col2"> <p>Als u bestaande zoek-URL's die u in het wild hebt, wilt ondersteunen, kunt u een alias van een facet gebruiken om de naam van een oudere parameter toe te wijzen aan gewijzigd of gewoon een facet met een andere naam te maken. De alias wordt alleen toegepast op binnenkomende aanvragen en wordt niet gebruikt om facetkoppelingen te maken. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Naam facetrails </p> </td> 
      <td colname="col2"> <p>De naam van de facetrail als u besluit om uw facetten alfabetisch, op telling, of door een douanemethode te sorteren. </p> <p>Zie <a href="../c-about-design-menu/c-about-facet-rails.md#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB" format="dita" scope="local"> Info over facetrails </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Volgorde </p> </td> 
      <td colname="col2"> <p>Deze optie is alleen beschikbaar als u <span class="uicontrol"> Besteld </span> in de vervolgkeuzelijst <span class="uicontrol"> Sorteren </span> hebt geselecteerd. </p> <p>Hiermee kunt u een lijst met gescheiden waarden definiëren die de te gebruiken volgorde aangeeft. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Extra's toevoegen </p> </td> 
      <td colname="col2"> <p>Deze optie is alleen beschikbaar als u <span class="uicontrol"> Besteld </span> in de vervolgkeuzelijst <span class="uicontrol"> Sorteren </span> hebt geselecteerd. </p> <p>Als de waarden niet voorkomen in de geordende lijst, worden de waarden toegevoegd aan het eind. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Schimmen tonen </p> </td> 
      <td colname="col2"> <p>Deze optie is alleen beschikbaar als u <span class="uicontrol"> Besteld </span> in de vervolgkeuzelijst <span class="uicontrol"> Sorteren </span> hebt geselecteerd. </p> <p>Als de waarden die worden opgegeven in de geordende lijst ontbreken, wordt elk ontbrekend item in de facet met deze optie gemarkeerd als "spook", zodat de items anders worden weergegeven. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Geneste facet </p> </td> 
      <td colname="col2"> <p>Een geneste facet geeft de categorieën en de categorieën van de onderliggende elementen weer. Het kan slechts een diepte van twee categorieën tonen, maar het kan overal langs boor-down zijn. </p> <p>De gegevens voor dit facet moeten een conventie volgen bij het beschrijven van de twee niveaus van categorieën. Een facetwaarde kan bijvoorbeeld 'schoenen:laarzen' zijn, waarbij de bovenliggende categorie 'schoenen' is en de onderliggende categorie 'laarzen'. Het scheidingsteken ':' wordt gebruikt als scheidingsteken. </p> <p>Zie Geneste scheidingsteken hieronder voor meer informatie over het wijzigen van het scheidingsteken. </p> <p>Als u de gegevens in deze indeling wilt genereren, kunt u een filterscript gebruiken om twee bestaande categorieën te combineren. U kunt gedragingen Normaal, Categorie en Vaste elementen combineren met geneste facetten. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Geneste bovenliggende naam </p> </td> 
      <td colname="col2"> <p>Deze vervolgkeuzelijst is alleen beschikbaar als u <span class="uicontrol"> Geneste facet </span> hebt geselecteerd. </p> <p>Hiermee kunt u kiezen welk veld de bovenliggende categorie vertegenwoordigt. Dit veld wordt tijdens de zoektijd gebruikt in overeenkomende bovenliggende categorieën. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Geneste onderliggende naam </p> </td> 
      <td colname="col2"> <p>Deze vervolgkeuzelijst is alleen beschikbaar als u <span class="uicontrol"> Geneste facet </span> hebt geselecteerd. </p> <p>Hiermee kunt u kiezen welk veld de onderliggende categorie vertegenwoordigt. Dit veld wordt tijdens de zoektijd gebruikt in overeenkomende onderliggende categorieën. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Geneste facetscheidingsteken </p> </td> 
      <td colname="col2"> <p>Deze optie is alleen beschikbaar als u <span class="uicontrol"> Geneste facet </span> hebt geselecteerd. </p> <p>Het hier ingevoerde teken wordt gebruikt om de bovenliggende categorieën en onderliggende categorieën van de gegevens te parseren. </p> <p>Als ':' bijvoorbeeld wordt gebruikt als scheidingsteken en het bovenliggende element 'schoenen' is en het onderliggende element 'laarzen', verwacht het dat de gegevens worden opgemaakt als 'schoenen:laarzen'. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Drempel voor splitsen </p> </td> 
      <td colname="col2"> <p>Deze optie is alleen beschikbaar als u <span class="uicontrol"> </span> hebt gesplitst in de vervolgkeuzelijst <span class="uicontrol"> </span> Sorteren. </p> <p>Wanneer u een gesplitste sortering gebruikt, definieert de gesplitste drempelwaarde het aantal waarbij de facet in twee afzonderlijke lijsten wordt gesplitst. Waarden waarvan het aantal groter dan of gelijk is aan de drempelwaarde, worden bovenaan gehouden en waarden onder de drempelwaarde worden naar onderen verplaatst. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Bovenste waarden </p> </td> 
      <td colname="col2"> <p>Deze optie is alleen beschikbaar als u <span class="uicontrol"> </span> in de vervolgkeuzelijst <span class="uicontrol"> Sorteren </span> hebt geselecteerd. </p> <p>Wanneer u een sortering Break gebruikt, wordt deze gescheiden lijst met waarden altijd boven aan de lijst geplaatst. Het gebruik van reguliere expressies is toegestaan, maar moet tussen accolades of accolades staan, bijvoorbeeld: {^Nieuw.*?},{^Zeer nieuw.*} </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Onderste waarden </p> </td> 
      <td colname="col2"> <p>Deze optie is alleen beschikbaar als u <span class="uicontrol"> </span> in de vervolgkeuzelijst <span class="uicontrol"> Sorteren </span> hebt geselecteerd. </p> <p>Wanneer u een sortering Break gebruikt, wordt deze gescheiden lijst met waarden altijd onder aan de lijst geplaatst. Het gebruik van reguliere expressies is toegestaan, maar moet tussen accolades of accolades staan, zoals in het volgende voorbeeld: {^Oud.*?},{^Zeer oud.*} </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Klik op **[!UICONTROL Add]**.
1. (Optioneel) Voer op de pagina [!DNL Facets] een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een genest facet toevoegen {#task_A132FA7EB7494A6B88E443F2C3FABBBA}

U kunt een genest facet toevoegen om meerdere niveaus van categorieën weer te geven.

<!-- 

t_adding_a_nested_facet.xml

 -->

Houd rekening met het volgende wanneer u een genest facet maakt:

* Voor elk geneste facet is één door de gebruiker gedefinieerd metatag-tagveld vereist.
* Geneste facetten bestaan uit twee andere facetten, de bovenliggende facet en de onderliggende facet. Ze kunnen elementen met één waarde of facetten met meerdere waarden zijn. Het mengen van facetten met één waarde en facetten met meerdere waarden is niet toegestaan.
* U moet bepalen of dit facet in de lijst van het onderzoeksgebied zal worden gebruikt. De veldtabel vereist de geneste facet zelf en de samenstellende facetten ervan.
* Overweeg JSON te gebruiken om geneste facetten te implementeren; het is gemakkelijker .

* [Taak 1 - Een meta-tag toevoegen](../c-about-design-menu/c-about-facets.md#task_6944558325204E749C725DCFEF17EF3D)
* [Taak 2 - voeg een het filtreren manuscript toe om voorgeformatteerde gegevens te produceren](../c-about-design-menu/c-about-facets.md#task_2DFED8BCB87B4067A6CE280945D7CAF4)
* [Taak 3 - Een nieuw facet toevoegen](../c-about-design-menu/c-about-facets.md#task_3C11A4159FC44B9494D48594941AF8CF)
* [Taak 4 - Zoeken met instructies bewerken](../c-about-design-menu/c-about-facets.md#task_E50EFD7BBD0F45729C15759EA4F548D8)
* [Taak 5 - creeer het Malplaatje van het Vervoer](../c-about-design-menu/c-about-facets.md#task_C1FEDEF11D2549DEB1A9C09BFBA64381)
* [Taak 6 - De Presentatiesjabloon maken](../c-about-design-menu/c-about-facets.md#task_4B2ABB37B9CD4F3F8AF8E6874227A995)
* [Taak 7 - Bewerk de Breadcrumb](../c-about-design-menu/c-about-facets.md#task_5E22409528EC4DA284821F82FDCE3438)

>[!NOTE]
>
>Dit onderwerp verwijst naar het geneste facet als facet n1.

## Taak 1 - voeg een meta markering {#task_6944558325204E749C725DCFEF17EF3D} toe

Voeg een nieuw metatag gebied toe dat aan houddatum voor het genestelde facet wordt gewijd. Dit kan een veld met meerdere waarden of een veld met één waarde zijn.

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**.
1. Klik op [!DNL Definitions] op de pagina.**[!UICONTROL Add New Field]**
1. Stel op de pagina [!DNL Add Field] de gewenste opties in.

   Zie [Een nieuw metatag toevoegen gebied](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).
1. Klik op **[!UICONTROL Add]**.
1. (Optioneel) Maak de gefaseerde site-index opnieuw als u een voorvertoning van de resultaten wilt zien.

   Zie [Een incrementele index van een gefaseerde website configureren](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

   De resterende taken verwijzen naar dit veld metatag als **n1**.

## Taak 2 - voeg een het filtreren manuscript toe om voorgeformatteerde gegevens {#task_2DFED8BCB87B4067A6CE280945D7CAF4} te produceren

1. Voeg een filterscript toe om de oorspronkelijke facetten in de volgende indeling te combineren: `<parent_value><nested_delimiter><child_value>`.

   Zie [Een filterscript toevoegen](../c-about-settings-menu/c-about-filtering-menu.md#task_0AB84FD1133F47F9AA069A79BEA13A22).

   Hieronder volgen voorbeelden van waarden voor metatag-tagveld n1 met bovenstaande notatie

   `Womens:Handbags`

   `Womens:Dresses`

   `Mens:Accessories`

   `Mens:Footwear`
1. Nadat u het het filtreren manuscript creeert of uitgeeft, test het manuscript. Als het er goed uitziet, moet u uw account opnieuw indexeren, indien van toepassing. U kunt de index controleren met [!DNL Index Overview].

   In de volgende voorbeelden wordt ervan uitgegaan dat u een aantal standaard consulting bibliotheken hebt die zijn opgenomen met de initialisatie van het filterscript. Herinner dat elk rekening verschillend is, zodat zou uw het filtreren manuscript op de noodzakelijke vereisten voor uw eigen rekening moeten wijzen.

   **Voorbeeld van een filterscript voor meerdere waarden**

   ```
   my $doc; 
   { 
   # Slurp all the data into $doc 
   local $/; 
   undef $/; 
   $doc = <>; 
   } 
    # Create n1 field 
    if ( $doc =~ m{<meta\s+name="t1"\s+content="([^\"]*)"}is ) 
    { 
     my @t1arr = split(/\|/, $1); 
     if (scalar @t1arr > 0) 
     { 
      if ( $doc =~ m{<meta\s+name="t2"\s+content="([^\"]*)"}is ) 
      { 
       my @t2arr = split(/\|/, $1); 
   
       if ( scalar @t2arr > 0 ) 
       { 
        my $max = ((scalar @t1arr) < (scalar @t2arr)) ? (scalar @t1arr) : (scalar @t2arr); 
        for (my $i = 0; $i < $max; $i++) 
        { 
         $t1arr[$i] .= ":" . $t2arr[$i]; 
        } 
       } 
      } 
      my $output = join( '|', @t1arr ); 
      $doc =~ s{</head>}{<meta name="n1" content="$output" />\b</head>}is; 
     } 
    } 
    # END: n1 field
   ```

   **Voorbeeld van een filterscript voor één waarde**

   ```
   # This is a complete example. 
   # This script is designed for index connector where each record 
   # in the XML file is converted into a fake HTML page filled with 
   # meta data tags.  
   my $doc; 
   { 
   # Slurp all the data 
   local $/; 
   undef $/; 
   $doc = <>; 
   } 
   # All legitimate index connector data has key in its URL. 
   # Process the page if and only if it is coming from index connector and 
   # it is not the first entry point page.  Entry point pages don't have key 
   # in the URL. 
   if ($main::search_url =~ /\?key=/) { 
    my $meta = {}; 
    # Mine and scrape the meta fields from the page 
    my @lines = split(/\n/,$doc); 
    foreach my $line (@lines) 
    { 
     if ($line =~ m{<meta name="(.*?)" content="(.*?)" />}) 
     { 
      $meta->{lc($1)} = $2; 
     } 
    } 
    # Combined t1,t2 and t2,t3, and t3,t4 together. 
    # Assign them respectively to n1, n2, and n3. 
    my ($t1, $t2, $t3, $t4); 
    my %meta2; 
    $t1 = $meta->{'t1'}; 
    $t2 = $meta->{'t2'}; 
    $t3 = $meta->{'t3'}; 
    $t4 = $meta->{'t4'}; 
    if (defined $t1 && $t1) { 
     $meta2{'n1'} = $t1; 
     if (defined $t2 && $t2) { 
      $meta2{'n1'} .= ":" . $t2; 
      $meta2{'n2'} = $t2; 
      if (defined $t3 && $t3) { 
      $meta2{'n2'} .= ":" . $t3; 
       $meta2{'n3'} = $t3; 
       if (defined $t4 && $t4) { 
        $meta2{'n3'} .= ":" . $t4; 
       } 
      } 
     } 
    } 
    foreach my $stuff ( keys %meta2 ) 
    { 
     my $v = $meta2{$stuff}; 
     $doc =~ s{</head>}{<meta name="$stuff" content="$v" />\n</head>}; 
    } 
   } 
   
   # Do some ranking stuff here 
   ws_insert_static_rank_meta_tag(\$doc, "RANK"); 
   
   # Prints the entire page back out. 
   print $doc;
   ```

## Taak 3 - voeg een nieuw facet {#task_3C11A4159FC44B9494D48594941AF8CF} toe

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Facets]**.
1. Klik op [!DNL Facets] op de pagina.**[!UICONTROL Add New Facet]**
1. Stel op de pagina [!DNL Add Facet] de volgende opties in:

   * Selecteer in de vervolgkeuzelijst [!DNL Facet Name] het veld voor de metatag dat u in Taak 1 hebt gedefinieerd. Als u de lijsten van het onderzoeksgebied gebruikt, selecteer **[!UICONTROL custom]** in de drop-down lijst, en ga dan de douanenaam van de facet in.

   * Schakel **[!UICONTROL Nested Facet]** in om geneste facetten in te schakelen.
   * Kies in de vervolgkeuzelijsten [!DNL Nested Parent Name] en [!DNL Nested Child Name] de velden voor de metatag die u kunt gebruiken. Als u zoekveldtabellen gebruikt, selecteert u **[!UICONTROL custom]** en voert u de aangepaste naam van de facet in.

   * Geef in het veld [!DNL Nested Facet Delimiter] het scheidingsteken op dat u wilt gebruiken, zoals een &quot;:&quot; (dubbele punt). Verwar dit niet met het scheidingsteken voor meerdere waarden. Beide scheidingstekens moeten van elkaar verschillen.
   * Als u het gedrag van de facet **[!UICONTROL Category]** instelt, kunt u de bovenliggende elementen van de facet opgeven (verwar bovenliggende elementen niet met geneste bovenliggende elementen). In het algemeen gebruikt u nooit de naam van een ander genest facet als bovenliggend element van categorie. Gebruik in plaats daarvan de afzonderlijke facetten waaruit dat geneste facet bestaat.
   * Stel de gewenste andere facetopties in.

   Zie [Een nieuw facet toevoegen](../c-about-design-menu/c-about-facets.md#task_FC07BFFA62CA4B718D6CBF4F2855C89B).
1. Klik op **[!UICONTROL Add]**.

## Taak 4 - Bewerken van zoekopdrachten met instructies {#task_E50EFD7BBD0F45729C15759EA4F548D8}

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Searches]**.
1. Klik op [!DNL Searches] pagina&#39;s op **[!UICONTROL Edit]** van de naam van het zoektype die u wilt bijwerken.
1. `sp_field_table` heeft veld n1, t1 en t2 nodig.

   Als veldtabellen worden gebruikt, moet u de parameter `sp_field_table` bewerken. Of, kunt u dit elders verwezenlijken door vraag het schoonmaken regels of pre-onderzoeksregels te gebruiken.

   Zie [Een regel voor het schoonmaken van query toevoegen](../c-about-rules-menu/c-about-query-cleaning-rules.md#task_47F43988D3D9485F8AE1DFDA7E00BF54).

   Zie [Een nieuwe regel toevoegen voor voorzoeken](../c-about-rules-menu/c-about-pre-search-rules.md#task_182B95918462490D8BDA7F16A81CAC11).
1. Klik op **[!UICONTROL Save Changes]**.

## Taak 5 - creeer het Malplaatje van het Vervoer {#task_C1FEDEF11D2549DEB1A9C09BFBA64381}

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Klik op [!DNL Templates] pagina&#39;s.**[!UICONTROL Add New Template]**
1. Geef in het dialoogvenster [!DNL Add Template] de naam van het transportsjabloonbestand op.
1. Selecteer in de vervolgkeuzelijst [!DNL New Template Type] de optie **[!UICONTROL Transport]**.
1. Klik op **[!UICONTROL Add]**.
1. Voor [!DNL Templates] pagina, klik de naam van het dossier van het vervoermalplaatje u enkel toevoegde.
1. Op [!DNL Template Editor] pagina voor uw vervoermalplaatje, omvat de gegevens die van gebied n1 komen. Zie de volgende voorbeelden.

   **XML-voorbeeld van het retourneren van geneste** facetgegevensIn het XML-voorbeeld moet worden opgegeven welk teken wordt gebruikt als scheidingsteken tussen facetwaarden. In dit geval is het een pijp (|).

   ```
   <facet name="n1"> 
     <values delimiter="|"><search-field-value-list name="n1" quotes="no" separator="|" sortby="values" data="values" /></values> 
     <counts><search-field-value-list name="n1" quotes="no" sortby="values" data="results" /></counts> 
   </facet>
   ```

   **JSON-voorbeeld voor het retourneren van geneste facetgegevens**

   ```
   { 
      "name" : "n1", 
      "values" : [ <search-field-value-list name="n1" quotes="yes" sortby="values" data="values" encoding="json"/>], 
      "counts" : [<search-field-value-list name="n1" quotes="no" sortby="values" data="results" />] 
   },
   ```

## Taak 6 - creeer het Malplaatje van de Presentatie {#task_4B2ABB37B9CD4F3F8AF8E6874227A995}

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Klik op [!DNL Templates] pagina&#39;s.**[!UICONTROL Add New Template]**
1. Geef in het dialoogvenster [!DNL Add Template] de naam op van het sjabloonbestand voor de presentatie.
1. Selecteer in de vervolgkeuzelijst [!DNL New Template Type] de optie **[!UICONTROL Presentation]**.
1. Klik op **[!UICONTROL Add]**.
1. Klik op de pagina [!DNL Templates] op de naam van het sjabloonbestand voor de presentatie dat u zojuist hebt toegevoegd.
1. Voeg op de pagina [!DNL Template Editor] voor uw presentatiesjabloon HTML-opmaak toe die integreert met de verwachte uitvoer.

   U kunt de volgende tags gebruiken om onderliggende tags weer te geven:

* **Als onderliggende items bestaan** `<guided-if-facet-value-has-children><guided-else-facet-value-selected></guided-if-facet-value-has-children>`

* **Onderliggende waardetags** `<guided-facet-value-children></guided-facet-value-children>`

   De onderliggende waardetags gedragen zich niet als normale guided-facet-value-tags. De are wrapper-tags dwingen alle omsluitende `<guided-facet-value>`-tags om de waarden van onderliggende facetten te doorlopen in plaats van de waarden van bovenliggende facetten. Ook andere gelaatstags, zoals de tags voor ongedaan maken, volgen hetzelfde. U kunt deze het beste gebruiken binnen `<guided-if-facet-value-has-children>`-tags.

   Hieronder ziet u een voorbeeld van een presentatiesjabloon met HTML-opmaak.

   ```
   <guided-facet gsname="n1"> 
   <guided-if-facet-selected> 
    <guided-facet-values> 
    <guided-if-facet-value-selected> 
     <li><span class="selected"><guided-facet-value /></span><guided-facet-value-undo-link gsname="n1">X</guided-facet-value-undo-link></li> 
     <guided-if-facet-value-has-children> 
      <ul> 
      <guided-facet-value-children> 
      <guided-if-facet-value-selected> 
       <li><span class="selected"><guided-facet-value /></span><guided-facet-value-undo-link gsname="n1">X</guided-facet-value-undo-link></li> 
      <guided-else-facet-value-selected> 
       <li><guided-facet-link title='<guided-facet-value />'><guided-facet-value /> (<guided-facet-count />)</guided-facet-link> </li> 
      </guided-if-facet-value-selected> 
      </guided-facet-value-children> 
      </ul> 
     </guided-if-facet-value-has-children> 
    <guided-else-facet-value-selected> 
     <li><guided-facet-link title='<guided-facet-value />'><guided-facet-value /> (<guided-facet-count />)</guided-facet-link> </li> 
     <guided-if-facet-value-has-children> 
      <ul> 
      <guided-facet-value-children> 
       <li><guided-facet-link title='<guided-facet-value />'><guided-facet-value /> (<guided-facet-count />)</guided-facet-link> </li> 
      </guided-facet-value-children> 
      </ul> 
     </guided-if-facet-value-has-children> 
    </guided-if-facet-value-selected> 
    </guided-facet-values> 
   <guided-else-facet-selected>  
    <guided-facet-values> 
    <guided-if-facet-value-selected> 
     <li><span class="selected"><guided-facet-value /></span><guided-facet-value-undo-link gsname="n1">X</guided-facet-value-undo-link></li> 
     <guided-if-facet-value-has-children> 
      <ul> 
      <guided-facet-value-children> 
       <li><guided-facet-link title='<guided-facet-value />'><guided-facet-value /> (<guided-facet-count />)</guided-facet-link> </li> 
      </guided-facet-value-children> 
      </ul> 
     </guided-if-facet-value-has-children> 
    <guided-else-facet-value-selected> 
     <li><guided-facet-link title='<guided-facet-value />'><guided-facet-value /> (<guided-facet-count />)</guided-facet-link> </li> 
     <guided-if-facet-value-has-children> 
      <ul> 
      <guided-facet-value-children> 
       <li><guided-facet-link title='<guided-facet-value />'><guided-facet-value /> (<guided-facet-count />)</guided-facet-link> </li> 
      </guided-facet-value-children> 
      </ul> 
     </guided-if-facet-value-has-children> 
    </guided-if-facet-value-selected> 
    </guided-facet-values> 
   </guided-if-facet-selected> 
   </guided-facet>
   ```

## Taak 7 - Bewerk de broodkruimel {#task_5E22409528EC4DA284821F82FDCE3438}

Als u broodkruimels in uw onderzoek gebruikt, moet u het gedrag aan **Ga naar** plaatsen.

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Breadcrumbs]**.
1. Klik op de [!DNL Breadcrumbs] pagina&#39;s **[!UICONTROL Edit]** op de naam van de broodkruimel waarvan u het gedrag wilt bijwerken.
1. Selecteer **Ga naar** in de vervolgkeuzelijst [!DNL Edit Breadcrumb] op de pagina [!DNL Behavior].
1. Klik op **[!UICONTROL Save Changes]**.

## Een facet {#task_457EDC49983F4F7781873703AF574DA5} bewerken

U kunt de instellingen van alle facetten bewerken die u hebt toegevoegd.

<!-- 

t_editing_a_facet.xml

 -->

>[!NOTE]
>
>Zorg ervoor dat u naar het facet in uw presentatiesjabloon verwijst, zodat dit zichtbaar is op de website.

**Een facet bewerken**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Facets.]**
1. Op [!DNL Facets] pagina, klik **[!UICONTROL Edit]** uiterst rechts van een facetnaam.
1. Stel op de pagina [!DNL Edit Facet] de gewenste opties in.

   Zie de optietabel onder [Een nieuw facet toevoegen](../c-about-design-menu/c-about-facets.md#task_FC07BFFA62CA4B718D6CBF4F2855C89B).
1. Klik op **[!UICONTROL Save Changes]**.
1. (Optioneel) Op de [!DNL Facets]-pagina,

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een facet {#task_17756FD66BCC49629325B2217F821BDD} verwijderen

U kunt alle toegevoegde facetten verwijderen.

<!-- 

t_deleting_a_facet.xml

 -->

**Een facet verwijderen**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Facets]**.
1. Op [!DNL Facets] pagina, klik **[!UICONTROL Delete]** uiterst rechts van een facetnaam.
1. Klik in het dialoogvenster [!DNL Confirmation] op **[!UICONTROL OK]**.
1. Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

