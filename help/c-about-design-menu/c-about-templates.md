---
description: U kunt Malplaatjes gebruiken om uw presentatiemalplaatjes en vervoermalplaatjes te beheren.
seo-description: U kunt Malplaatjes gebruiken om uw presentatiemalplaatjes en vervoermalplaatjes te beheren.
seo-title: Over sjablonen
solution: Target
title: Over sjablonen
topic: Design,Site search and merchandising
uuid: f5805d3e-43bf-4e13-95df-b6bd6b762d11
translation-type: tm+mt
source-git-commit: 60cedaac1846e384a37699a42bf7fda33828e1c0

---


# Over sjablonen{#about-templates}

U kunt gebruiken **[!UICONTROL Templates]** om uw presentatiemalplaatjes en vervoermalplaatjes te beheren.

## Over sjablonen {#concept_06EB481B14864E18A8AE2BCD1D6EF0B5}

<!-- 

c_about_templates.xml

 -->

U kunt, presentatiemalplaatjes en vervoermalplaatjes toevoegen uitgeven, kopiëren, anders noemen of schrappen. Wanneer u een bestaande malplaatjenaam in de lijst van Malplaatjes klikt, wordt het geopend in een redacteur (of kijker) venster waar u uw veranderingen kunt aanbrengen.

U kunt om het even welke veranderingen terugkeren u aan malplaatjes aanbrengt gebruikend de eigenschap van de Geschiedenis van de drop-down lijst van de malplaatjenaam in de lijst van Malplaatjes.

U kunt het paginagewicht van een presentatiemalplaatje verminderen door het overeenkomstige **[!UICONTROL Minimize]** checkbox van de malplaatje in de malplaatjetabel te controleren. Door het paginagewicht van het malplaatje te verminderen, minimaliseert u dynamisch gealigneerde JavaScript en CSS. U verwijdert ook overtollige whitespace in HTML. Het minimaliseren van het paginagewicht van uw presentatiemalplaatje kan helpen om uw onderzoeksresultaten sneller te leveren.

U kunt voorproef de verschijning van het geminimaliseerde malplaatje door de drop-down lijst naast filename te klikken en dan te klikken **[!UICONTROL Preview minimized]**. Als u het belangrijkste presentatiemalplaatje minimaliseert, ben zeker dat u zich herinnert minimaliserend voor inbegrepen (met `guided-include` markering) malplaatjes toe te laten omdat deze optie niet inherent is.

Zelfs als u een presentatiemalplaatje minimaliseert, kunt u de &quot;unminimized&quot;versie van het zelfde malplaatje nog uitgeven.

U kunt de pre-onderzoeksregels, post-onderzoeksregels, en bedrijfsregels gebruiken om te bepalen wanneer te om één van uw andere presentatiemalplaatjes te gebruiken. Het is gemeenschappelijk om een regel zoals &quot;voor elke onderzoek te hebben, plaats het gerichte malplaatje aan xxxx&quot;. Met zulk een regel op zijn plaats, wanneer u het &quot;Standaard&quot;malplaatje in de lijst van Malplaatjes verandert, schijnt het geen effect te hebben.

Zie [over Voorspelregels](../c-about-rules-menu/c-about-pre-search-rules.md#concept_5BF84BB6FACB4645BA9CB7496A01CD1F)voor zoeken.

Zie [Informatie over regels](../c-about-rules-menu/c-about-post-search-rules.md#concept_AF6ADFCC0ADF4A788003964939917FDE)na het zoeken.

Zie [over de bedrijfsregels](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

## Over presentatiesjablonen {#section_ACDDEA5C499E481C828A517C230D4596}

De malplaatjes van de presentatie zijn de malplaatjes van HTML die een klant ziet wanneer zij de resultaten van hun onderzoek op uw website bekijken.

In uw presentatielaag, kunt u één enkel presentatiemalplaatje hebben dat de resultaten van veelvoudige onderzoeken uit diverse bronnen voorstelt. U kunt zo vele presentatiemalplaatjes bepalen aangezien u wilt en zelfs presentatiemalplaatjes bepalen die andere malplaatjes gebruikend `include` bevelen delen. Het presentatiemalplaatje is waar alle componenten van het Ontwerp zoals facetten, menu&#39;s, en broodkruimels, samenkomen. Om de diverse ontwerpcomponenten te tonen, moet u de markeringen van het presentatiemalplaatje gebruiken.

Zie [Presentatiemalplaatmarkeringen](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)

Wanneer u meer dan één presentatiemalplaatje hebt, bepaalt u onder welke voorwaarden de diverse presentatiemalplaatjes worden gebruikt. U kunt selecteren welke presentatiemalplaatje aan gebruik op de inkomende parameters en koekjes van CGI wordt gebaseerd. Of, u kunt schakelen welk presentatiemalplaatje u gebaseerd op het resultaat van een vorige onderzoek gebruikt.

Wanneer u veelvoudige presentatiemalplaatjes gebruikt, ben zeker dat u op welk malplaatje wijst dat u de onderzoeksresultaten aanvankelijk wilt verschijnen. U kunt dit doen gebruikend de **[!UICONTROL Default]** kolom van de lijst van Malplaatjes.

## Over transporttemplates {#section_35FD3E8AAA4E4695A737DB7E00C3258B}

De malplaatjes van het vervoer kunnen of XML of malplaatjes zijn JSON die gegevens van het achterste deelonderzoek tot de Begeleide de presentatielaag van het Onderzoek overgaan.

Door gebrek, wordt uw rekening gevormd om het vervoermalplaatjes van XML te gebruiken. Nochtans, als u verkiest JSON te gebruiken om uw gegevens tot Geleid Onderzoek over te gaan, contacteer het Raadplegen van Adobe die u kan helpen.

In uw presentatielaag, kunt u één enkel presentatiemalplaatje hebben dat de resultaten van veelvoudige onderzoeken voorstelt. Elk onderzoek kan het zelfde vervoermalplaatje of een malplaatje van het douanevervoer gebruiken om de gegevens tot de presentatielaag over te gaan. Omdat het vervoermalplaatje slechts wordt gebruikt om gegevens tot de presentatielaag over te gaan, moet het geen HTML hebben dat wordt gebruikt om de onderzoeksresultaten te tonen. Het malplaatje gebruikt de markeringen van het vervoermalplaatje om de resultaten van het onderzoek en de resultaten over te gaan voor het bevolken van de facetten. Binnen deze markeringen, worden de standaard markeringen van het onderzoeksmalplaatje gebruikt om de daadwerkelijke waarden te tonen.

Zie [Zoeksjabloontags](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4).

**XML Transport Sjabloon-specifieke tags**

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>XML-transportsjabloontag </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;geleid-xml&gt;&lt;/geleide-xml&gt; </span> </p> </td> 
   <td colname="col2"> <p>Dit zijn de markeringen van wortelXML die de presentatielaag gebruikt om te ontdekken wat het uit het vervoermalplaatje moet ontleden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;algemeen&gt;&lt;/general&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze reeks markeringen omringt de markeringen van het onderzoeksmalplaatje die summiere gegevens verstrekken die op de resultaatreeks worden gebaseerd. Typisch, bevatten deze markeringen onderzoeksmarkeringen voor het totale aantal resultaten, het laagste resultaat, en het hoogste resultaat. U kunt om het even welk aantal extra globale gebieden bepalen die u met de <span class="codeph"> algemeen-gebied </span> markering wilt. </p> <p> <b>Voorbeeld</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&lt;general&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;total&gt;&lt;search-total&nbsp;/&gt;&lt;/total&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;lower&gt;&lt;search-lower&nbsp;/&gt;&lt;/lower&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;upper&gt;&lt;search-upper&nbsp;/&gt;&lt;/upper&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;general-field&nbsp;name="my_custom_field"&gt;Some&nbsp;global&nbsp;content&lt;/general-field&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/general&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;resultaten&gt;&lt;/resultaten&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze reeks markeringen wordt verpakt rond de onderzoeksresultaten, zodat Geleid Onderzoek weet waar te om hen te zoeken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;resultaat&gt;&lt;/resultaat&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze reeks markeringen wordt verpakt rond elk onderzoeksresultaat, zodat Geleid Onderzoek erkent waar de inhoud voor één enkel onderzoeksresultaat begint en beëindigt. </p> <p> <b>Voorbeeld</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&lt;results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;search-results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;result&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;index&gt;&lt;search-index&nbsp;/&gt;&lt;/index&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;loc&gt;&lt;search-cdata&gt;&lt;search-url&nbsp;length="500"&nbsp;/&gt;&lt;/search-cdata&gt;&lt;/loc&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/result&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/results&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;attribuut-lijst name="tabelnaam"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze markering laat u door elk punt in een multi-waardelijst voor één enkel resultaat van een lus voorzien. Gebruik de markering slechts binnen een resultaat. Zijn primaire doel is u te laten over attributen herhalen die tot een resultaatgebied behoren. </p> <p> <b>Voorbeeld</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;search-results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;result&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;index&gt;&lt;search-index&nbsp;/&gt;&lt;/index&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;loc&gt;&lt;search-url&nbsp;/&gt;&lt;/loc&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;title&gt;&lt;search-title&nbsp;/&gt;&lt;/title&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;attribute-table&nbsp;name="downloads"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;field&nbsp;name="download_title"&gt;&lt;search-display-field&nbsp;name="download_title"&nbsp;/&gt;&lt;/field&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;field&nbsp;name="download_link"&nbsp;delimiter="|"&gt;&lt;search-display-field&nbsp;name="download_link"&nbsp;/&gt;&lt;/field&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/attribute-table&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/result&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/results&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;facetten&gt;&lt;/facetten&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze reeks markeringen gaat over de resultaten over die de facetten bevolken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;facet name="name"&gt;&lt;/facet&gt; </span> </p> </td> 
   <td colname="col2"> <p>Elke facet moet zijn eigen facetmarkeringen hebben waar de naamparameter de facetnaam aanpast. De markeringen van het onderzoek worden gebruikt binnen de facetmarkeringen voor de facetwaarden. </p> <p>Zie <a href="../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5" type="concept" format="dita" scope="local"> Over Facets </a>. </p> <p> <b>Voorbeeld</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&lt;facets&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;facet&nbsp;name="brand"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;values&gt;&lt;search-field-value-list&nbsp;name="brand"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;counts&gt;&lt;search-field-value-list&nbsp;name="brand"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="counts"&nbsp;sortby="values"&nbsp;/&gt;&lt;/counts&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/facet&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;facet&nbsp;name="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;values&gt;&lt;search-field-value-list&nbsp;name="category"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;counts&gt;&lt;search-field-value-list&nbsp;name="category"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="counts"&nbsp;sortby="values"&nbsp;/&gt;&lt;/counts&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/facet&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/facets&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;suggesties&gt;&lt;/suggesties&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze reeks markeringen verpakt uw Bedoelde u suggesties zodat Geleid Onderzoek erkent welke knopen van XML suggesties bevatten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;suggestie&gt;&lt;/suggestie&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze reeks markeringen verpakte elk Bedoelde u suggestie. </p> <p> <b>Voorbeeld</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&lt;search-if-suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;search-suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;suggestion&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;value&gt;&lt;search-suggestion-text&nbsp;/&gt;&lt;/value&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;count&gt;&lt;search-suggestion-result-count&nbsp;/&gt;&lt;/count&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/suggestion&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-if-suggestions&gt; </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Sjabloonspecifieke JSON-tags voor transport**

Het overgaan van JSON tegenover XML van de onderzoek-motor is gekend om sneller te zijn omdat het kleinere nuttige lading en een snellere syntactische parser is. De zorg van het gebruik, echter, wanneer u JSON gebruikt om ervoor te zorgen dat wat output strikte JSON is omdat de syntactische parser niet vergeeft is.

Als u aan JSON nieuw bent, kunt u de volgende verbindingen en de voorbeelden gebruiken om u te helpen begonnen worden:

* Een inleiding naar JSON. Zie [https://www.json.org/](https://www.json.org/).
* Test uw JSON om ervoor te zorgen dat het geldig is. Zie [https://jsonlint.com/](https://jsonlint.com/).

**Voorbeeld JSON-sjabloon**

```
{ 
 "general": 
 { 
  "total" : "<search-total />", 
  "lower" : "<search-lower />", 
  "upper" : "<search-upper />", 
  "rbt-trigger-list" : "<search-rbta-trigger-id-list>", 
  "fields" :  
  [ 
   { 
    "name" : "seo_search_title", 
    "value" : "<search-include file="seo/seo_search_title.tpl" />" 
   }, 
   { 
    "name" : "seo_search_keywords", 
    "value" : "<search-include file="seo/seo_search_keywords.tpl" />" 
   } 
  ] 
 }, 
 
 <search-if-suggestions> 
 "suggestions": 
  [ 
  <search-suggestions> 
  { 
   "suggestion":"<search-suggestion-text />", 
   "count": "<search-suggestion-result-count>" 
  }<search-if-not-last-suggestion>,</search-if-not-last-suggestion> 
  </search-suggestions> 
 ], 
 </search-if-suggestions> 
 
 "facets" : 
 [ 
  { 
   "name" : "leveli", 
   "values" : [ <search-field-value-list name="leveli" quotes="yes" sortby="values" data="values" encoding="json"/>], 
   "counts" : [<search-field-value-list name="leveli" quotes="no" sortby="values" data="results" />] 
  }, 
  { 
   "name" :"levelii", 
   "values" : [<search-field-value-list name="levelii" quotes="yes" sortby="values" data="values" encoding="json"/>], 
   "counts" : [<search-field-value-list name="levelii" quotes="no" sortby="values" data="results" />] 
  }, 
  { 
   "name" : "brand", 
   "values" : [<search-field-value-list name="brand" quotes="yes" sortby="values" data="values" encoding="json"/>], 
   "counts" : [<search-field-value-list name="brand" quotes="no" sortby="values" data="results" />] 
  }, 
 ], 
 "results" : 
 [ 
  <search-results> 
  { 
   "fields" : 
   [ 
    { 
     "name" : "index", 
     "value" : "<search-index />" 
    }, 
    { 
     "name" : "loc", 
     "value" : "<search-display-field name="url" length="500" encoding="json"/>" 
    }, 
    { 
     "name" : "title", 
     "value" : "<search-display-field name="title" encoding="json"/>" 
    }, 
    { 
     "name" : "img_url_thumbnail", 
     "value" : "<search-display-field name="img_url_thumbnail" encoding="json"/>" 
    }, 
    { 
     "name" : "description", 
     "value" : "<search-display-field name="description" encoding="json"/>" 
    }, 
    { 
     "name" : "mdi", 
     "value" : "<SEARCH-RBTA-DISPLAY-MDI-FIELD>" 
    } 
   ] 
  }<search-if-not-last>,</search-if-not-last>  
  </search-results> 
 ] 
}
```

**Voorbeeld JSON resultaat sectie met een resultatentabel**

```
{ 
 "results" : 
 [ 
  <search-results> 
  { 
   "fields" : 
   [ 
    { 
     "name" : "index", 
     "value" : "<search-index />" 
    }, 
    { 
     "name" : "loc", 
     "value" : "<search-display-field name="url" length="500" encoding="json"/>" 
    } 
   ], 
   "tables" : 
   [ 
    { 
     "name" : "downloads", 
     "fields" : 
     [ 
      { 
       "name" : "download_title", 
       "value" : <search-display-field name="download_title" encoding="json"/> 
      }, 
      { 
       "name" : "download_link", 
       "value" : <search-display-field name="download_link" encoding="json"/> 
      } 
     ] 
    } 
   ] 
  }<search-if-not-last>,</search-if-not-last>  
  </search-results> 
 ] 
}
```

**Voorbeeld JSON Facet sectie voor een facet met bijbehorende gebieden**

```
{ 
 facets" : 
 [ 
  { 
   "name" : "t1", 
   "values" : [<search-field-value-list name="t1" quotes="yes" commas="yes" data="values" sortby="values" encoding="json" />], 
   "counts" : [<search-field-value-list name="t1" quotes="yes" commas="yes" data="results" sortby="values" />], 
   "custom-fields" : 
   [ 
    { 
     "name" : "taxonmyId", 
     "value" : [<search-field-value-list name="tax1" quotes="yes" commas="yes" data="values" sortby="values" encoding="json" />] 
    } 
   ] 
  } 
 ] 
}
```

**Voorbeeld: JSON Facet-sectie voor steekvlakken**

```
{ 
  "facets" : 
  [  
   { 
    "name" : "fvalue0", 
                  "dynamic" : 1, 
                  "display-names" : [<search-field-value-list name="fname0" quotes="yes" commas="yes" data="values" sortby="values" encoding="json" />], 
    "values" : [<search-field-value-list name="fvalue0" quotes="yes" commas="yes" data="values" sortby="values" encoding="json" />], 
    "counts" : [<search-field-value-list name="fvalue0" quotes="no" commas="yes" data="results" sortby="values" />] 
   } 
  ] 
} 
```

## Een nieuw presentatie- of transportsjabloonbestand toevoegen {#task_73199757B6E748CAA604902FF913F012}

U kunt gebruiken **[!UICONTROL Add Template]** om presentatiemalplaatjes (.tmpl) of vervoermalplaatjes (.tpl) aan de [!DNL Templates] pagina toe te voegen.

<!-- 

t_adding_a_new_presentation_or_transport_template_file.xml

 -->

**Om een nieuw presentatie of een dossier van het vervoermalplaatje toe te voegen**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Voor de [!DNL Templates] pagina, klik **[!UICONTROL Add New Template]**.
1. In de [!DNL Add Template] dialoogdoos, plaats de opties die u wilt.

   <!-- 
   
   r_add_template_options.xml
   
   -->

   | Optie | Beschrijving |
   |--- |--- |
   | Nieuwe bestandsnaam | Specificeert de naam van het malplaatje dat u wilt toevoegen. De juiste dossieruitbreiding wordt automatisch toegevoegd aan het dossier - naam, die op het malplaatjetype wordt gebaseerd u selecteert.  De malplaatjes van de presentatie hebben een .tmpl dossieruitbreiding; De malplaatjes van het vervoer hebben een .tpl dossieruitbreiding. |
   | Nieuw sjabloontype | Laat u een presentatie of een vervoermalplaatje kiezen dat u wilt toevoegen.  Zie [over sjablonen](../c-about-design-menu/c-about-templates.md). |

   Zie ook een presentatie of een vervoermalplaatje [](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3)uitgeven.
1. Klik op **[!UICONTROL Add]**.
1. (Facultatief) op de [!DNL Templates] pagina, doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een presentatie of een transportsjabloon bewerken {#task_800E0E2265C34C028C92FEB5A1243EC3}

U kunt de Redacteur van het Malplaatje aan mening gebruiken en de inhoud van uw presentatie en dossiers van het vervoermalplaatje uitgeven.

<!-- 

t_editing_a_template.xml

 -->

U kunt uw gefaseerde presentatie en vervoermalplaatjes uitgeven en testen, terwijl uw websitebezoekers de levende versies van uw malplaatjes blijven gebruiken. U test uw gefaseerde malplaatje gebruikend de gefaseerde versie van uw onderzoeksdomein URL. Bijvoorbeeld, kunt u uw gefaseerd vervoermalplaatje testen door een gefaseerde vraag ( `sp_staged=1`) in werking te stellen met `sp_t` die aan de naam van uw vervoermalplaatje wordt geplaatst. Wanneer u tevreden bent met hoe de lay-out verschijnt, kunt u **[!UICONTROL Push Live]** van binnen de malplaatjedacteur gebruiken om het malplaatje levend te duwen. Nadat het malplaatje levend is, beginnen de bezoekers van de plaats om het te gebruiken.

Gebruik de de markeringsverwijzing van het presentatiemalplaatje leren hoe te om uw presentatiemalplaatje aan de Begeleide componenten van het Onderzoek zoals facetten, broodkruimels, en menu&#39;s omhoog te sluiten.

Zie [Presentatiemalplaatmarkeringen](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)

Gebruik de de markeringsverwijzing van het vervoermalplaatje om meer over de markeringen te leren in vervoermalplaatjes te gebruiken.

Zie [Sjabloontags voor transport](../c-appendices/c-templates.md#reference_227D199F5A7248049BE1D405C0584751)

**[!UICONTROL To edit a presentation or a transport template]**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Voor de [!DNL Templates] pagina, klik een presentatie of een dossier van het vervoermalplaatje - naam.
1. Voor de [!DNL Template Editor] pagina, breng de veranderingen aan u aan de markeringen en de codering wilt.

   Wees voorzichtig met de wijzigingen die u aanbrengt in het [!DNL Template Editor]; er is geen functie Ongedaan maken. Als u een ongewenste verandering aanbrengt en naar de vorige versie van het dossier wilt terugkeren, kunt u klikken **[!UICONTROL Cancel]** om aan de lijst van malplaatjes terug te keren (veronderstellend u om het even welk van uw veranderingen tot dat punt niet opsloeg). Als u reeds uw veranderingen hebt bewaard, kunt u **[!UICONTROL History]** in de redacteur gebruiken om die veranderingen terug te keren.
1. (Facultatief) klik **[!UICONTROL Insert Symbol]** om speciale karakters en symbolen in te gaan die geen overeenkomstige sleutels op Amerikaanse Engelse toetsenborden hebben.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

1. Sluit de pagina van de Redacteur van het Malplaatje wanneer u wordt gebeëindigd; u bent teruggekeerd aan de pagina van Malplaatjes.

## Het kopiëren van een presentatie of een dossier van het vervoermalplaatje {#task_B744AB3384C84DD59C33CD25E18C2C90}

U kunt gebruiken **[!UICONTROL Copy Template]** om tijd te besparen door een bestaand malplaatje van de Presentatie (.tmpl) of malplaatje van het Vervoer (.tpl) te dupliceren en het toe te voegen aan de pagina van Malplaatjes.

<!-- 

t_copying_a_presentation_or_a_transport_template.xml

 -->

U moet de malplaatjenaam, het malplaatjetype, of allebei veranderen. Als u geen veranderingen aanbrengt, wordt het malplaatje niet gekopieerd.

Je moet een template hebben toegevoegd om een template te kunnen kopiëren.

Zie Een nieuw presentatie- of transportsjabloonbestand [](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012)toevoegen.

**Om een presentatie of een dossier van het vervoermalplaatje te kopiëren**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Voor de [!DNL Templates] pagina, in de drop-down lijst naast een malplaatjenaam die u wilt kopiëren, klik **[!UICONTROL Copy]**.
1. In de [!DNL Copy Template] dialoogdoos, plaats één of meerdere van de opties die u wilt.
1. Klik op **[!UICONTROL Copy]**.
1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Het anders noemen van een presentatie of een dossier van het vervoermalplaatje {#task_CC30050FC2DE4898BF44379D8378EB31}

U kunt gebruiken [!DNL Rename Template] om de naam van een bestaand presentatiemalplaatje (.tmpl) of een vervoermalplaatje (.tpl) te veranderen.

<!-- 

t_renaming_a_presentation_or_a_transport_template_file.xml

 -->

U kunt het malplaatjetype ook veranderen, indien gewenst.

U moet een malplaatje hebben reeds wordt toegevoegd om een malplaatje anders te noemen dat.

Zie Een nieuw presentatie- of transportsjabloonbestand [](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012)toevoegen.

**Om een presentatie of een dossier van het vervoermalplaatje anders te noemen**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Voor de [!DNL Templates] pagina, in de drop-down lijst naast een malplaatjenaam die u wilt anders noemen, klik **[!UICONTROL Rename]**.
1. In de [!DNL Rename Template] dialoogdoos, plaats één of meerdere van de opties die u wilt.
1. Klik op **[!UICONTROL Rename]**.
1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Het schrappen van een presentatie of een dossier van het vervoermalplaatje {#task_67E532C2B83A449687737E3B06C5AA58}

U kunt gebruiken **[!UICONTROL Delete Template]** om een bestaand presentatiemalplaatje (.tmpl) of een vervoermalplaatje (.tpl) te verwijderen.

<!-- 

t_deleting_a_presentation_or_a_transport_template_file.xml

 -->

U kunt reeds een overeenkomstige versie van het gefaseerde malplaatje hebben dat levend wordt geduwd. Als zo, ben zeker u het geschrapte malplaatje levend gebruikend duwt **[!UICONTROL Staging]** zodat het ook uit het levende milieu wordt geschrapt. Of, u kunt **[!UICONTROL Push Live]** op de pagina van Malplaatjes gebruiken.

Zie [Over stappen](../c-about-staging.md#concept_08B8F3CA1F4241108F14BA7FC7806CA7)

Zie [Stadsinstellingen pushing live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)

Je moet een template hebben toegevoegd om een template te kunnen verwijderen.

Zie Een nieuw presentatie- of transportsjabloonbestand [toevoegen](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012)

**Om een presentatie of een dossier van het vervoermalplaatje te schrappen**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Voor de [!DNL Templates] pagina, in de drop-down lijst naast een malplaatjenaam die u wilt schrappen, klik **[!UICONTROL Delete]**.
1. Klik in het [!DNL Delete Template] dialoogvenster op **[!UICONTROL Delete.]**
1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Previewing het presentatiemalplaatje geminimaliseerd {#task_1757B6207CC74221AE4BFFE5674D320B}

U kunt gebruiken **[!UICONTROL Preview minimized]** om te zien wat het verminderde paginagewicht van een presentatiemalplaatje als zou kijken als u verkiest om het te minimaliseren.

<!-- 

t_previewing_the_presentation_template_minimized.xml

 -->

Als u het belangrijkste presentatiemalplaatje minimaliseert, ben zeker dat u zich herinnert minimaliserend voor inbegrepen (met geleid-omvat markering) malplaatjes toe te laten omdat deze optie niet inherent is.

Zie Het [paginagewicht van een presentatiemalplaatje verminderen op uw...](../c-about-design-menu/c-about-templates.md#task_B09BB3CE89714DEAAE8D9A899CF3009E)

U moet een malplaatje hebben reeds aan voorproef wordt toegevoegd het geminimaliseerde malplaatje dat.

Zie Een nieuw presentatie- of transportsjabloonbestand [toevoegen](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012)

U kunt voorproef de code van XML van een dossier van het vervoermalplaatje.

Zie [Previewing XML van een dossier van het vervoermalplaatje](../c-about-design-menu/c-about-templates.md#task_58C6C52078E14AD88D2B2F0B3C439AE8)

**Aan voorproef minimaliseerde het presentatiemalplaatje**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Voor de [!DNL Templates] pagina, in de drop-down lijst naast een naam van het presentatiemalplaatje, klik **[!UICONTROL Preview minimized]**.

   Gebruik de **[!UICONTROL Type]** kolom in de lijst van Malplaatjes om de malplaatjes door Presentatie en Vervoer te sorteren.
1. (Facultatief) op de [!DNL Preview Minimized Template] pagina, controleer **[!UICONTROL Wrap lines]** om de markeringen binnen het bepaalde venster te lezen.
1. Klik op **[!UICONTROL Close]**.
1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Het paginagewicht van een presentatiemalplaatje op uw website verminderen {#task_B09BB3CE89714DEAAE8D9A899CF3009E}

U kunt het paginagewicht van een presentatiemalplaatje verminderen door de **[!UICONTROL Minimize]** optie in de malplaatjelijst te gebruiken.

<!-- 

t_reducing_the_page_weight_of_a_presentation_template.xml

 -->

Door het paginagewicht van het malplaatje te verminderen, minimaliseert u dynamisch gealigneerde JavaScript en CSS. U verwijdert ook overtollige whitespace in HTML. Het minimaliseren van het paginagewicht van uw presentatiemalplaatje kan helpen om uw onderzoeksresultaten sneller te leveren.

U kunt ook voorproef de verschijning van het geminimaliseerde presentatiemalplaatje door te gebruiken **[!UICONTROL Preview minimized]**.

Zie [Previewing het geminimaliseerde](../c-about-design-menu/c-about-templates.md#task_1757B6207CC74221AE4BFFE5674D320B)presentatiemalplaatje.

**[!UICONTROL To reduce the page weight of a presentation template on your website]**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Voor de [!DNL Templates] pagina, onder de [!DNL Minimize] kolom, controleer de doos één of meerdere dossiers van het presentatiemalplaatje die u wilt duwen zo minimaliseren op uw website.

   Gebruik de **[!UICONTROL Type]** kolom in de [!DNL Templates] lijst om de malplaatjes door Presentatie en Vervoer te sorteren.
1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Het plaatsen van het dossier van het standaardpresentatiemalplaatje aan gebruik op uw website {#task_C1E8CE817E4D43E096167A347C54DD53}

Wanneer u veelvoudige presentatiemalplaatjes hebt, kunt u wijzen op welk malplaatje aanvankelijk wordt gebruikt om onderzoeksresultaten te tonen.

<!-- 

t_setting_the_default_presentation_template_file_to_use.xml

 -->

U kunt de pre-onderzoeksregels, post-onderzoeksregels, en bedrijfsregels gebruiken om te bepalen wanneer één van uw andere presentatiemalplaatjes zou moeten worden gebruikt.

Zie [over Voorspelregels](../c-about-rules-menu/c-about-pre-search-rules.md#concept_5BF84BB6FACB4645BA9CB7496A01CD1F)voor zoeken.

Zie [Informatie over regels](../c-about-rules-menu/c-about-post-search-rules.md#concept_AF6ADFCC0ADF4A788003964939917FDE)na het zoeken.

Zie [over de bedrijfsregels](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

Het is gemeenschappelijk om een regel zoals &quot;voor elke onderzoek te hebben, plaats het gerichte presentatiemalplaatje aan xxxx.&quot; Met zulk een regel op zijn plaats, zal het veranderen van het &quot;gebrek&quot;malplaatje op de pagina van Malplaatjes schijnen geen effect te hebben.

**[!UICONTROL To set the default presentation template file to use on your website]**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Voor de [!DNL Templates] pagina, onder de [!DNL Default] kolom, klik de radioknoop aan het overeenkomstige dossier van het presentatiemalplaatje dat u als gebrek wilt dienen.

   Gebruik de **[!UICONTROL Type]** kolom in de [!DNL Templates] lijst om de malplaatjes door Presentatie en Vervoer te sorteren.
1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Previewing XML van een dossier van het vervoermalplaatje {#task_58C6C52078E14AD88D2B2F0B3C439AE8}

U kunt gebruiken [!DNL Preview] om XML van een vervoermalplaatje te herzien dat u hebt toegevoegd.

<!-- 

t_previewing_the_xml_of_a_transport_template_file.xml

 -->

U moet een vervoermalplaatje hebben reeds aan voorproef XML van het malplaatje wordt toegevoegd dat.

Zie Een nieuw presentatie- of transportsjabloonbestand [](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012)toevoegen.

U kunt voorproef de geminimaliseerde dossiers van het presentatiemalplaatje om hun verminderd paginagewicht te bekijken.

Zie [Previewing het geminimaliseerde](../c-about-design-menu/c-about-templates.md#task_1757B6207CC74221AE4BFFE5674D320B)presentatiemalplaatje.

**Aan voorproef XML van een dossier van het vervoermalplaatje**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Voor de [!DNL Templates] pagina, in de drop-down lijst naast een naam van het vervoermalplaatje, klik **[!UICONTROL Preview]**.

   Gebruik de **[!UICONTROL Type]** kolom in de [!DNL Templates] lijst om de malplaatjes door Presentatie en Vervoer te sorteren.
1. Sluit het het bekijken venster en terugkeer aan [!DNL site search/merchandising].
1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

