---
description: U kunt Sjablonen gebruiken om uw presentatiesjablonen en transportsjablonen te beheren.
seo-description: U kunt Sjablonen gebruiken om uw presentatiesjablonen en transportsjablonen te beheren.
seo-title: Informatie over sjablonen
solution: Target
title: Informatie over sjablonen
topic: Design,Site search and merchandising
uuid: f5805d3e-43bf-4e13-95df-b6bd6b762d11
translation-type: tm+mt
source-git-commit: 60cedaac1846e384a37699a42bf7fda33828e1c0
workflow-type: tm+mt
source-wordcount: '2661'
ht-degree: 0%

---


# Info over Sjablonen{#about-templates}

Met **[!UICONTROL Templates]** kunt u presentatiesjablonen en transportsjablonen beheren.

## Informatie over sjablonen {#concept_06EB481B14864E18A8AE2BCD1D6EF0B5}

<!-- 

c_about_templates.xml

 -->

U kunt presentatiesjablonen en transportsjablonen toevoegen, bewerken, kopiëren, hernoemen of verwijderen. Wanneer u op een bestaande sjabloonnaam in de tabel Sjablonen klikt, wordt deze geopend in een bewerkingsvenster (of viewer) waarin u uw wijzigingen kunt aanbrengen.

U kunt alle wijzigingen die u aanbrengt in sjablonen herstellen met de functie Historie uit de vervolgkeuzelijst met sjabloonnamen in de tabel Sjablonen.

U kunt het paginagewicht van een presentatiesjabloon verlagen door het overeenkomstige selectievakje **[!UICONTROL Minimize]** in de sjabloontabel in te schakelen. Door het paginagewicht van de sjabloon te verlagen, minimaliseert u inline JavaScript en CSS dynamisch. U verwijdert ook overbodige witruimte in de HTML. Door het paginagewicht van uw presentatiesjabloon te minimaliseren, kunt u sneller zoekresultaten behalen.

U kunt de weergave van de geminimaliseerde sjabloon voorvertonen door te klikken op de vervolgkeuzelijst naast de bestandsnaam en vervolgens te klikken op **[!UICONTROL Preview minimized]**. Als u de hoofdpresentatiesjabloon minimaliseert, moet u ervoor zorgen dat u minimaliseren voor opgenomen sjablonen (met de tag `guided-include`) inschakelt, omdat deze optie niet overerfbaar is.

Zelfs als u een presentatiesjabloon minimaliseert, kunt u nog steeds de &quot;niet-geminimaliseerde&quot; versie van dezelfde sjabloon bewerken.

U kunt de regels voor voorzoeken, regels voor postzoekopdrachten en bedrijfsregels gebruiken om te bepalen wanneer u een van uw andere presentatiesjablonen wilt gebruiken. Het is gebruikelijk om een regel te hebben zoals &quot;Voor elke onderzoek, plaats het gerichte malplaatje aan xxxx&quot;. Als een dergelijke regel is ingesteld en u de sjabloon Standaard in de tabel Sjablonen wijzigt, lijkt deze geen effect te hebben.

Zie [Informatie over regels voor voorzoeken](../c-about-rules-menu/c-about-pre-search-rules.md#concept_5BF84BB6FACB4645BA9CB7496A01CD1F).

Zie [Informatie over Post-Search Regels](../c-about-rules-menu/c-about-post-search-rules.md#concept_AF6ADFCC0ADF4A788003964939917FDE).

Zie [Informatie over bedrijfsregels](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

## Presentatiesjablonen {#section_ACDDEA5C499E481C828A517C230D4596}

Presentatiesjablonen zijn HTML-sjablonen die een klant ziet wanneer hij of zij de resultaten van zijn zoekopdracht op uw website bekijkt.

In uw presentatielaag kunt u één presentatiesjabloon gebruiken waarin de resultaten van meerdere zoekopdrachten uit verschillende bronnen worden weergegeven. U kunt zo veel presentatiesjablonen definiëren als u wilt en zelfs presentatiesjablonen definiëren die door andere sjablonen worden gedeeld met de opdrachten `include`. In de presentatiesjabloon komen alle ontwerpcomponenten, zoals facetten, menu&#39;s en broodkruimels, samen. Als u de verschillende ontwerpcomponenten wilt weergeven, moet u sjabloonlabels voor presentaties gebruiken.

Zie [Labels voor presentatiesjabloon](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)

Als u meerdere presentatiesjablonen hebt, bepaalt u onder welke voorwaarden de verschillende presentatiesjablonen worden gebruikt. U kunt selecteren welke presentatiesjabloon u wilt gebruiken op basis van de inkomende CGI-parameters en cookies. U kunt ook wisselen welke presentatiesjabloon u gebruikt op basis van het resultaat van een vorige zoekopdracht.

Als u meerdere presentatiesjablonen gebruikt, moet u opgeven welke sjabloon u de zoekresultaten eerst wilt laten weergeven. U kunt dit doen gebruikend de **[!UICONTROL Default]** kolom van de lijst van Malplaatjes.

## Informatie over transportsjablonen {#section_35FD3E8AAA4E4695A737DB7E00C3258B}

De malplaatjes van het vervoer kunnen of malplaatjes XML of JSON zijn die gegevens van het achterste-eindonderzoek tot de Geleide presentatielaag van het Onderzoek overgaan.

Standaard is uw account geconfigureerd voor het gebruik van XML-transportsjablonen. Als u echter liever JSON gebruikt om uw gegevens door te geven aan de functie Zoeken met instructies, neemt u contact op met Adobe Consulting voor hulp.

In uw presentatielaag kunt u één presentatiesjabloon gebruiken waarin de resultaten van meerdere zoekopdrachten worden weergegeven. Elke zoekopdracht kan dezelfde transportsjabloon of een aangepaste transportsjabloon gebruiken om de gegevens door te geven aan de presentatielaag. Omdat het vervoermalplaatje slechts wordt gebruikt om gegevens tot de presentatielaag over te gaan, moet het geen HTML hebben die wordt gebruikt om de onderzoeksresultaten te tonen. De sjabloon gebruikt transportsjabloontags om de resultaten van de zoekopdracht en de resultaten door te geven om de facetten te vullen. Binnen deze tags worden standaardtags voor zoeksjablonen gebruikt om de werkelijke waarden weer te geven.

Zie [Sjabloontags zoeken](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4).

**Specifieke labels voor XML-transportsjablonen**

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>XML-transportsjabloontag </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-xml&gt;&lt;/guided-xml&gt; </span> </p> </td> 
   <td colname="col2"> <p>Dit zijn de wortelXML markeringen die de presentatielaag gebruikt om te ontdekken wat het uit het vervoermalplaatje moet ontleden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;general&gt;&lt;/general&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze reeks markeringen rond de markeringen van het onderzoeksmalplaatje die summiere gegevens verstrekken die op de resultaatreeks worden gebaseerd. Deze tags bevatten meestal zoekcodes voor het totale aantal resultaten, het laagste resultaat en het hoogste resultaat. U kunt elk gewenst aantal aanvullende globale velden definiëren met de <span class="codeph">-tag general-field </span>. </p> <p> <b>Voorbeeld</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&lt;general&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;total&gt;&lt;search-total&nbsp;/&gt;&lt;/total&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;lower&gt;&lt;search-lower&nbsp;/&gt;&lt;/lower&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;upper&gt;&lt;search-upper&nbsp;/&gt;&lt;/upper&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;general-field&nbsp;name="my_custom_field"&gt;Some&nbsp;global&nbsp;content&lt;/general-field&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/general&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;results&gt;&lt;/results&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze set tags wordt rond de zoekresultaten geplaatst, zodat de zoekfunctie met instructies weet waar ze naartoe moeten zoeken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;result&gt;&lt;/result&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze set tags wordt rond elk zoekresultaat geplaatst, zodat met instructies wordt herkend waar de inhoud voor één zoekresultaat begint en eindigt. </p> <p> <b>Voorbeeld</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&lt;results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;search-results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;result&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;index&gt;&lt;search-index&nbsp;/&gt;&lt;/index&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;loc&gt;&lt;search-cdata&gt;&lt;search-url&nbsp;length="500"&nbsp;/&gt;&lt;/search-cdata&gt;&lt;/loc&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/result&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/results&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;attribute-table name="tablename"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Met dit label kunt u elk item in een lijst met meerdere waarden doorlopen voor één resultaat. Gebruik de tag alleen binnen een resultaat. Het hoofddoel is om u te laten doorlopen over kenmerken die tot een resultaatveld behoren. </p> <p> <b>Voorbeeld</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;results&gt; 
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
   <td colname="col1"> <p> <span class="codeph"> &lt;facets&gt;&lt;/facets&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze reeks labels geeft de resultaten door die de facetten vullen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;facet name="name"&gt;&lt;/facet&gt; </span> </p> </td> 
   <td colname="col2"> <p>Elk facet moet zijn eigen facetmarkeringen hebben waar de naamparameter de facetnaam aanpast. Zoekcodes worden binnen de facettags voor de waarden van facetten gebruikt. </p> <p>Zie <a href="../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5" type="concept" format="dita" scope="local"> Informatie over facetten </a>. </p> <p> <b>Voorbeeld</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&lt;facets&gt; 
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
   <td colname="col1"> <p> <span class="codeph"> &lt;suggestions&gt;&lt;/suggestions&gt; </span> </p> </td> 
   <td colname="col2"> <p>Met deze set labels loopt u uw Bedoelde suggesties om te zien welke XML-knooppunten suggesties bevatten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;suggestion&gt;&lt;/suggestion&gt; </span> </p> </td> 
   <td colname="col2"> <p>Deze reeks markeringen verpakt elk Bedoelde u suggestie. </p> <p> <b>Voorbeeld</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&lt;search-if-suggestions&gt; 
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

**JSON-transportsjabloonspecifieke tags**

Het doorgeven van JSON versus XML van de zoekmachine is bekend sneller omdat het een kleinere lading en een snellere parser is. Wees echter voorzichtig wanneer u JSON gebruikt om ervoor te zorgen dat de uitvoer strikt JSON is, omdat de parser niet vergeeft is.

Als u nog niet eerder met JSON werkt, kunt u de volgende koppelingen en voorbeelden gebruiken om aan de slag te gaan:

* Een inleiding tot JSON. Zie [https://www.json.org/](https://www.json.org/).
* Test uw JSON om te controleren of deze geldig is. Zie [https://jsonlint.com/](https://jsonlint.com/).

**Voorbeeld-JSON-sjabloon**

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

**Voorbeeld van JSON-resultaatsectie met een tabel voor resultaatkenmerken**

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

**Voorbeeld-JSON-facetsectie voor een facet met gekoppelde velden**

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

**Voorbeeld van de sectie JSON Facet voor steunende facetten**

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

## Een nieuw presentatie- of transportsjabloonbestand {#task_73199757B6E748CAA604902FF913F012} toevoegen

Met **[!UICONTROL Add Template]** kunt u presentatiesjablonen (.tmpl) of transportsjablonen (.tpl) toevoegen aan de pagina [!DNL Templates].

<!-- 

t_adding_a_new_presentation_or_transport_template_file.xml

 -->

**Een nieuwe presentatie of een nieuw transportsjabloonbestand toevoegen**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Klik op [!DNL Templates] op de pagina.**[!UICONTROL Add New Template]**
1. Stel in het dialoogvenster [!DNL Add Template] de gewenste opties in.

   <!-- 
   
   r_add_template_options.xml
   
   -->

   | Option | Beschrijving |
   |--- |--- |
   | Nieuwe bestandsnaam | Hier geeft u de naam op van de sjabloon die u wilt toevoegen. De juiste bestandsextensie wordt automatisch toegevoegd aan de bestandsnaam op basis van het sjabloontype dat u selecteert.  Presentatiesjablonen hebben de extensie .tmpl. De malplaatjes van het vervoer hebben een .tpl- dossieruitbreiding. |
   | Nieuw sjabloontype | Hiermee kunt u een presentatie of een transportsjabloon kiezen die u wilt toevoegen.  Zie [Informatie over sjablonen](../c-about-design-menu/c-about-templates.md). |

   Zie ook [Een presentatie of een transportsjabloon bewerken](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3).
1. Klik op **[!UICONTROL Add]**.
1. (Optioneel) Voer op de pagina [!DNL Templates] een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een presentatie of een transportsjabloon {#task_800E0E2265C34C028C92FEB5A1243EC3} bewerken

U kunt de Redacteur van het Malplaatje gebruiken om de inhoud van uw presentatie en vervoermalplaatjedossiers te bekijken en uit te geven.

<!-- 

t_editing_a_template.xml

 -->

U kunt uw gefaseerde presentatie en vervoermalplaatjes uitgeven en testen, terwijl uw websitebezoekers de levende versies van uw malplaatjes blijven gebruiken. U test uw gefaseerde sjabloon met behulp van de gefaseerde versie van de URL van het zoekdomein. Bijvoorbeeld, kunt u uw gefaseerde vervoermalplaatje testen door een gefaseerde vraag ( `sp_staged=1`) met `sp_t` in werking te stellen die aan de naam van uw vervoermalplaatje wordt geplaatst. Wanneer u tevreden bent over de manier waarop de lay-out wordt weergegeven, kunt u **[!UICONTROL Push Live]** vanuit de sjablooneditor gebruiken om de sjabloon live te zetten. Nadat de sjabloon live is, beginnen sitebezoekers deze te gebruiken.

Gebruik de tagverwijzing van de presentatiesjabloon om te leren hoe u de presentatiesjabloon koppelt aan componenten van de functie Zoeken met instructies, zoals facetten, broodkruimels en menu&#39;s.

Zie [Labels voor presentatiesjabloon](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)

Gebruik de de markeringsverwijzing van het vervoermalplaatje om meer over de markeringen te leren in vervoermalplaatjes te gebruiken.

Zie [Sjablooncodes voor vervoer](../c-appendices/c-templates.md#reference_227D199F5A7248049BE1D405C0584751)

**[!UICONTROL To edit a presentation or a transport template]**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Klik op de pagina [!DNL Templates] op een presentatie of een bestandsnaam voor een transportsjabloon.
1. Breng op de pagina [!DNL Template Editor] de gewenste wijzigingen aan in de codes en de codering.

   Wees voorzichtig met de wijzigingen die u aanbrengt in [!DNL Template Editor]; er is geen functie Ongedaan maken. Als u een ongewenste verandering aanbrengt en naar de vorige versie van het dossier wilt terugkeren, kunt u **[!UICONTROL Cancel]** klikken om aan de lijst van malplaatjes terug te keren (veronderstellend u om het even welke veranderingen tot dat punt niet opslaat). Als u uw wijzigingen al hebt opgeslagen, kunt u **[!UICONTROL History]** in de editor gebruiken om die wijzigingen terug te draaien.
1. (Optioneel) Klik op **[!UICONTROL Insert Symbol]** om speciale tekens en symbolen in te voeren die geen overeenkomende toetsen hebben op Amerikaanse toetsenborden.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

1. Sluit de pagina van de Redacteur van het Malplaatje wanneer u wordt gebeëindigd; u bent teruggekeerd aan de pagina van Malplaatjes.

## Een presentatie of een transportsjabloonbestand {#task_B744AB3384C84DD59C33CD25E18C2C90} kopiëren

U kunt **[!UICONTROL Copy Template]** gebruiken om tijd te besparen door een bestaand malplaatje van de Presentatie (.tmpl) of malplaatje van het Vervoer (.tpl) te dupliceren en het toe te voegen aan de pagina van Malplaatjes.

<!-- 

t_copying_a_presentation_or_a_transport_template.xml

 -->

U moet de sjabloonnaam, het sjabloontype of beide wijzigen. Als u geen wijzigingen aanbrengt, wordt de sjabloon niet gekopieerd.

Er moet al een sjabloon zijn toegevoegd om een sjabloon te kunnen kopiëren.

Zie [Een nieuw presentatie- of transportsjabloonbestand toevoegen](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012).

**Een presentatie of een transportsjabloonbestand kopiëren**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Klik op [!DNL Templates] op de pagina in de vervolgkeuzelijst naast de sjabloonnaam die u wilt kopiëren.**[!UICONTROL Copy]**
1. Stel in het dialoogvenster [!DNL Copy Template] een of meer van de gewenste opties in.
1. Klik op **[!UICONTROL Copy]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## De naam van een presentatie of een transportsjabloonbestand {#task_CC30050FC2DE4898BF44379D8378EB31} wijzigen

Met [!DNL Rename Template] kunt u de naam wijzigen van een bestaande presentatiesjabloon (.tmpl) of een transportsjabloon (.tpl).

<!-- 

t_renaming_a_presentation_or_a_transport_template_file.xml

 -->

U kunt desgewenst ook het sjabloontype wijzigen.

Er moet al een sjabloon zijn toegevoegd om de naam van een sjabloon te wijzigen.

Zie [Een nieuw presentatie- of transportsjabloonbestand toevoegen](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012).

**De naam van een presentatie of een transportsjabloonbestand wijzigen**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Klik op [!DNL Templates] in de vervolgkeuzelijst naast de naam van een sjabloon waarvan u de naam wilt wijzigen op **[!UICONTROL Rename]**.
1. Stel in het dialoogvenster [!DNL Rename Template] een of meer van de gewenste opties in.
1. Klik op **[!UICONTROL Rename]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een presentatie of een transportsjabloonbestand {#task_67E532C2B83A449687737E3B06C5AA58} verwijderen

Met **[!UICONTROL Delete Template]** kunt u een bestaande presentatiesjabloon (.tmpl) of een transportsjabloon (.tpl) verwijderen.

<!-- 

t_deleting_a_presentation_or_a_transport_template_file.xml

 -->

Mogelijk hebt u al een corresponderende versie van de gefaseerde sjabloon die live wordt geduwd. Als dat het geval is, moet u de verwijderde sjabloon live gebruiken met **[!UICONTROL Staging]**, zodat deze ook uit de live omgeving wordt verwijderd. U kunt ook **[!UICONTROL Push Live]** gebruiken op de pagina Sjablonen.

Zie [Staging](../c-about-staging.md#concept_08B8F3CA1F4241108F14BA7FC7806CA7)

Zie [Werkgebiedinstellingen live spoelen](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)

Er moet al een sjabloon zijn toegevoegd om een sjabloon te kunnen verwijderen.

Zie [Een nieuw presentatie- of transportsjabloonbestand toevoegen](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012)

**Een presentatie of een transportsjabloonbestand verwijderen**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Klik op [!DNL Templates] in de vervolgkeuzelijst naast de sjabloonnaam die u wilt verwijderen op **[!UICONTROL Delete]**.
1. Klik in het dialoogvenster [!DNL Delete Template] op **[!UICONTROL Delete.]**
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Voorvertoning van de presentatiesjabloon geminimaliseerd {#task_1757B6207CC74221AE4BFFE5674D320B}

Met **[!UICONTROL Preview minimized]** kunt u zien hoe het verlaagde paginagewicht van een presentatiesjabloon eruitziet als u dit tot een minimum beperkt.

<!-- 

t_previewing_the_presentation_template_minimized.xml

 -->

Als u de hoofdpresentatiesjabloon minimaliseert, dient u minimaliseren voor opgenomen sjablonen (met de tag Met instructies-include) in te schakelen, omdat deze optie niet overerfbaar is.

Zie [Het paginagewicht van een presentatiesjabloon op uw pagina verminderen..](../c-about-design-menu/c-about-templates.md#task_B09BB3CE89714DEAAE8D9A899CF3009E)

Er moet al een sjabloon zijn toegevoegd om een voorbeeld van de sjabloon te kunnen bekijken.

Zie [Een nieuw presentatie- of transportsjabloonbestand toevoegen](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012)

U kunt de XML-code van een transportsjabloonbestand voorvertonen.

Zie [De XML van een dossier van het vervoermalplaatje bekijken](../c-about-design-menu/c-about-templates.md#task_58C6C52078E14AD88D2B2F0B3C439AE8)

**Een voorvertoning weergeven van de presentatiesjabloon geminimaliseerd**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Klik op [!DNL Templates] in de vervolgkeuzelijst naast de naam van een presentatiesjabloon op **[!UICONTROL Preview minimized]**.

   Gebruik de **[!UICONTROL Type]** kolom in de lijst van Malplaatjes om de malplaatjes door Presentatie en Vervoer te sorteren.
1. (Optioneel) Controleer [!DNL Preview Minimized Template] op de pagina **[!UICONTROL Wrap lines]** om de codes in het gedefinieerde venster te lezen.
1. Klik op **[!UICONTROL Close]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Het paginagewicht van een presentatiesjabloon op uw website {#task_B09BB3CE89714DEAAE8D9A899CF3009E} verkleinen

U kunt het paginagewicht van een presentatiesjabloon verlagen met de optie **[!UICONTROL Minimize]** in de sjabloontabel.

<!-- 

t_reducing_the_page_weight_of_a_presentation_template.xml

 -->

Door het paginagewicht van de sjabloon te verlagen, minimaliseert u inline JavaScript en CSS dynamisch. U verwijdert ook overbodige witruimte in de HTML. Door het paginagewicht van uw presentatiesjabloon te minimaliseren, kunt u sneller zoekresultaten behalen.

U kunt de weergave van de geminimaliseerde presentatiesjabloon ook voorvertonen met **[!UICONTROL Preview minimized]**.

Zie [Voorvertoning van de presentatiesjabloon geminimaliseerd](../c-about-design-menu/c-about-templates.md#task_1757B6207CC74221AE4BFFE5674D320B).

**[!UICONTROL To reduce the page weight of a presentation template on your website]**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Schakel op de pagina [!DNL Templates] onder de kolom [!DNL Minimize] het vakje in voor een of meer presentatiesjabloonbestanden die u zo klein mogelijk wilt maken op uw website.

   Gebruik de **[!UICONTROL Type]** kolom in [!DNL Templates] lijst om de malplaatjes door Presentatie en Vervoer te sorteren.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Het standaardsjabloonbestand voor presentaties instellen dat op uw website wordt gebruikt {#task_C1E8CE817E4D43E096167A347C54DD53}

Als u meerdere presentatiesjablonen hebt, kunt u aangeven welke sjabloon in eerste instantie wordt gebruikt voor het weergeven van zoekresultaten.

<!-- 

t_setting_the_default_presentation_template_file_to_use.xml

 -->

U kunt de regels voor vooraf zoeken, regels voor na het zoeken en de bedrijfsregels gebruiken om te bepalen wanneer een van uw andere presentatiesjablonen moet worden gebruikt.

Zie [Informatie over regels voor voorzoeken](../c-about-rules-menu/c-about-pre-search-rules.md#concept_5BF84BB6FACB4645BA9CB7496A01CD1F).

Zie [Informatie over Post-Search Regels](../c-about-rules-menu/c-about-post-search-rules.md#concept_AF6ADFCC0ADF4A788003964939917FDE).

Zie [Informatie over bedrijfsregels](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

Het is gebruikelijk om een regel te hebben zoals &quot;Voor elke onderzoek, plaats het gerichte presentatiesjabloon aan xxxx.&quot; Als een dergelijke regel is ingesteld, lijkt het alsof het wijzigen van de standaardsjabloon op de pagina Sjablonen geen effect heeft.

**[!UICONTROL To set the default presentation template file to use on your website]**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Klik op de pagina [!DNL Templates] onder de kolom [!DNL Default] op het keuzerondje naar het bijbehorende sjabloonbestand voor de presentatie dat u als standaard wilt gebruiken.

   Gebruik de **[!UICONTROL Type]** kolom in [!DNL Templates] lijst om de malplaatjes door Presentatie en Vervoer te sorteren.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een voorbeeld weergeven van de XML van een transportsjabloonbestand {#task_58C6C52078E14AD88D2B2F0B3C439AE8}

U kunt [!DNL Preview] gebruiken om XML van een vervoermalplaatje te herzien dat u hebt toegevoegd.

<!-- 

t_previewing_the_xml_of_a_transport_template_file.xml

 -->

Er moet al een transportsjabloon zijn toegevoegd om een voorvertoning van de XML van de sjabloon weer te geven.

Zie [Een nieuw presentatie- of transportsjabloonbestand toevoegen](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012).

U kunt sjabloonbestanden voor geminimaliseerde presentaties voorvertonen om het gereduceerde paginagewicht weer te geven.

Zie [Voorvertoning van de presentatiesjabloon geminimaliseerd](../c-about-design-menu/c-about-templates.md#task_1757B6207CC74221AE4BFFE5674D320B).

**Een voorbeeld bekijken van de XML van een transportsjabloonbestand**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Voor [!DNL Templates] pagina, in de drop-down lijst naast een naam van het vervoermalplaatje, klik **[!UICONTROL Preview]**.

   Gebruik de **[!UICONTROL Type]** kolom in [!DNL Templates] lijst om de malplaatjes door Presentatie en Vervoer te sorteren.
1. Sluit het weergavevenster en ga terug naar [!DNL site search/merchandising].
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

