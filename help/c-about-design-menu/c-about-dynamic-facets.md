---
description: De Dynamische Facets van het gebruik om nieuwe waaierselecties automatisch tot stand te brengen op het tijdstip van onderzoek. U kunt elk dynamisch facetgebied met maximaal één lijstnaam in uw Onderzoek&amp van Adobe naar keuze associëren;amp;Promote rekening. U past die lijstverhoudingen op onderzoek-tijd voor om het even welke dynamische facetgebieden toe betrokken bij het onderzoek.
seo-description: De Dynamische Facets van het gebruik om nieuwe waaierselecties automatisch tot stand te brengen op het tijdstip van onderzoek. U kunt elk dynamisch facetgebied met maximaal één lijstnaam in uw Onderzoek&amp van Adobe naar keuze associëren;amp;Promote rekening. U past die lijstverhoudingen op onderzoek-tijd voor om het even welke dynamische facetgebieden toe betrokken bij het onderzoek.
seo-title: Informatie over dynamische factoren
solution: Target
subtopic: Navigation
title: Informatie over dynamische factoren
topic: Design,Site search and merchandising
uuid: 1ea91c22-dcc2-4173-aa50-ce618ad0a99c
translation-type: tm+mt
source-git-commit: 4270ea66ba645ad0f71c9c8b5c2a1fcc6eb02ad2

---


# Informatie over dynamische factoren{#about-dynamic-facets}

De Dynamische Facets van het gebruik om nieuwe waaierselecties automatisch tot stand te brengen op het tijdstip van onderzoek. U kunt elk dynamisch facetgebied met maximaal één lijstnaam in uw Adobe Search&amp;Promote rekening naar keuze associëren. U past die lijstverhoudingen op onderzoek-tijd voor om het even welke dynamische facetgebieden toe betrokken bij het onderzoek.

## Dynamische factoren gebruiken {#concept_E65A70C9C2E04804BF24FBE1B3CAD899}

>[!NOTE]
>
>Deze eigenschap wordt niet toegelaten binnen [!DNL Adobe Search&Promote], door gebrek. Neem contact op met Technische ondersteuning om de functie voor uw gebruik te activeren.

Zonder het gebruik van Dynamische Facets, moest u verwante attributen in &quot;groeven&quot;samenvoegen, en slechts de groeven tonen die voor een bepaalde onderzoek homogeen waren. Namelijk konden zij slechts één logische waarden van attributen, zoals &quot;schoengrootte&quot;of &quot;ringsgrootte&quot;bevatten. Deze methode verstrekte adequate onderzoek-tijd prestaties met een grote reeks unieke attributen.

Wanneer het Dynamische Faceting wordt gebruikt, echter, plaatst het geen grens op het aantal facetten dat het kernonderzoek kan efficiënt volgen. U kunt honderden dynamische facetten bepalen, waarvan het kernonderzoek de &quot;hoogste `N` dynamische facetten&quot;voor een bepaald onderzoek kan terugkeren, waar typisch een bescheidener waarde van 10-20 of minder `N` is. Deze methode elimineert de behoefte om de attributen te plaatsen-u kunt nu een uniek dynamisch facet voor attributen over uw website tot stand brengen.

## Welke facetten moet je dynamisch maken? {#section_254EE034BCAD4250A5D09FBF6158C4A5}

Facets die dunbevolkt zijn op uw website en alleen verschijnen voor een subset zoekopdrachten zijn goede kandidaten om dynamisch te worden. Bijvoorbeeld, kan een facet genoemd &quot;voorpootbreedte&quot;slechts worden bevolkt wanneer het zoeken naar schoenen of laarzen. Terwijl een ander facet genoemd &quot;de Numerieke Stijl van het Gezicht&quot;, met mogelijke waarden van &quot;Roman&quot;en &quot;Arabisch&quot;, slechts kan verschijnen wanneer het zoeken naar horloges of klokken.

Als uw rekening een groot aantal dergelijke facetten heeft, verbetert het onderzoeksprestaties om dynamische facetten te gebruiken in plaats van altijd het selecteren van de volledige reeks mogelijke facetten voor elke onderzoek. Generieke facetten zoals &quot;SKU&quot; of &quot;merk&quot;, die normaal gesproken geschikt zijn om met de resultaten van elke zoekopdracht weer te geven, zijn doorgaans niet geschikt als dynamische facetten.

## Verband tussen facetten en meta-tagvelden {#section_2869E5FCDA8B431A87BC6E5573F2B0A0}

De gebieden worden gebouwd bovenop de gebieden van de meta- markering. Een meta markeringsgebied is een laag-vlakke, eigenschap van de de laag van het kernonderzoek van [!DNL Adobe Search&Promote]. De facetten, anderzijds maken deel uit van GS (Geleid Onderzoek) - de high-level, presentatielaag van het Onderzoek&amp;Promote van Adobe. Facets eigen meta markeringsgebieden, echter, weten de meta markeringsgebieden niets over facetten. Wanneer u dynamische facetten vormt, voegt u eerst facetten toe en voegt dan de gebieden van de meta- markering met de Dynamische optie van het Gebied toe die wordt geselecteerd om het geïdentificeerde die facet te plaatsen om dynamisch te zijn.

>[!NOTE]
>
>Er is geen &quot;Dynamisch Facet&quot;plaatsend binnen **[!UICONTROL Design > Navigation > Facets]**. Wat een facet &quot;dynamisch&quot;maakt is dat zijn onderliggend &quot;gebied van de meta- markering&quot;dynamisch is zoals die in wordt geplaatst **[!UICONTROL Settings > Metadata > Definitions]**.

## Voorbeelden van dynamische facetten in actie {#section_BC699A05E2E742EF94D41679163ACE84}

Voorbeeld van dynamische facetten die na een onderzoek naar &quot;laarzen&quot;worden getoond:

![](assets/dynamicfacets_boots.png)

Een ander voorbeeld van dynamische facetten die na een onderzoek naar &quot;horloges&quot;worden getoond:

![](assets/dynamicfacets_watches.png)

Zie ook

* [Backend onderzoek CGI parameters](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)
* [Sjabloonlabels voor presentatie](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)
* [Labels transportsjabloon](../c-appendices/c-templates.md#reference_227D199F5A7248049BE1D405C0584751)

## Het vormen dynamische facetten {#task_D17F484130E448258100BAC1EEC53F39}

De Dynamische Facets van de vestiging in Onderzoek&amp;Promote.

<!-- 

t_configuring_dynamic_facets.xml

 -->

>[!NOTE]
>
>Deze eigenschap wordt niet toegelaten in het Onderzoek&amp;Promote van Adobe, door gebrek. Neem contact op met Technische ondersteuning om de functie voor uw gebruik te activeren.

Alvorens de gevolgen van uw dynamische facetten aan klanten zichtbaar zijn, moet u uw plaatsindex herbouwen.

Zie ook

* [Backend onderzoek CGI parameters](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)
* [Sjabloonlabels voor presentatie](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)
* [Labels transportsjabloon](../c-appendices/c-templates.md#reference_227D199F5A7248049BE1D405C0584751)

**Om dynamische facetten te vormen**

1. Zorg ervoor u reeds facetten hebt toegevoegd.

   Zie Een nieuw facet [toevoegen](../c-about-design-menu/c-about-facets.md#task_FC07BFFA62CA4B718D6CBF4F2855C89B).
1. Nadat uw facetten worden toegevoegd, zorg ervoor dat u de facetten aan nieuwe user-defined meta- markeringsgebieden hebt toegevoegd.

   Zie [Een nieuw meta-tagveld](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)toevoegen.
1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions.]**
1. Voor de [!DNL Definitions] pagina, in de [!DNL User-defined fields] lijst, in de [!DNL Actions] kolom, klik het potloodpictogram (geef uit) in de rij van de naam van het meta- markeringsgebied verbonden aan het facet dat u dynamisch wilt maken.
1. Op de [!DNL Edit Field] pagina, controleer **[!UICONTROL Dynamic Facet]**.

   Zie de lijst van opties in het [Toevoegen van een nieuw gebied](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)van de meta- markering.
1. Klik op **[!UICONTROL Save Changes]**.
1. Klik **regenereren uw gefaseerde plaatsindex** in de blauwe doos om uw gefaseerde websiteindex snel te herbouwen.

   Zie ook [Regenerating de index van een levende of gefaseerde website](../c-about-index-menu/c-about-regenerate-index.md#task_B28DE40C0E9A475ABCBCBC4FF993AACD).
1. Bepaal het aantal dynamische facetten om voor een bepaald onderzoek te selecteren. U verwezenlijkt deze taak door één van beiden van het volgende te doen:

   * Creeer een vraag schoonmaakregel met om het even welke gewenste voorwaarden, die de actie uitvoert, `set`, `backend parameter`om te waarderen `sp_sfvl_df_count` , waar `X`het gewenste aantal dynamische facetten is om op het tijdstip van onderzoek te verzoeken, en dan te klikken `X` **[!UICONTROL Add]**.
   ![](assets/querycleaningrule_dynamicfacets.png)

   Zie [het Toevoegen van een vraag schoonmaakregel](../c-about-rules-menu/c-about-query-cleaning-rules.md#task_47F43988D3D9485F8AE1DFDA7E00BF54).

   Zie ook de parameters [van het Onderzoek CGI van het](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)Backend, rij 40 in de lijst voor verdere verklaring van `sp_sfvl_df_count`.

   * Voeg een onderzoek toe en plaats de &quot;douane&quot; `sp_sfvl_df_count` parameter aan de gewenste waarde, en klik **[!UICONTROL Add]**.
   ![](assets/gs_addsearch_dynamic_facets.png)

   Zie [Een nieuwe zoekdefinitie](../c-about-settings-menu/c-about-searching-menu.md#task_98D3A168AB5D4F30A1ADB6E0D48AB648)toevoegen.

   Zie ook de parameters [van het Onderzoek CGI van het](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)Backend, rij 40 in de lijst voor verdere verklaring van `sp_sfvl_df_count`.

1. Geef het aangewezen vervoermalplaatje aan output uit de dynamische facetten die het kernonderzoek terugkeert.

   Zie Een presentatie [bewerken of een transportsjabloon](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3).

   Bijvoorbeeld, veronderstel dat uw vervoermalplaatje wordt genoemd `guided.tpl`. In zulk geval, op het productmenu, klik **[!UICONTROL Design > Templates]**. Voor de [!DNL Templates] pagina, bepaal de plaats `guided.tpl` in de lijst. en klik dan **[!UICONTROL Edit]** aan uiterst rechts van de naam. Voor de het Uitgeven pagina, voeg het volgende codeblok aan het eind van toe `</facets>`: JSON-uitvoer:

   ```
   ... 
   }<search-dynamic-facet-fields>, 
           { 
               "name" : "<search-dynamic-facet-field-name>", 
               "dynamic-facet" : 1, 
               "values" : [<search-field-value-list quotes="yes" commas="yes" data="values" sortby="values" encoding="json" />], 
               "counts" : [<search-field-value-list quotes="yes" commas="yes" data="results" sortby="values" />] 
   
           }</search-dynamic-facet-fields> 
   ...
   ```

1. Geef het aangewezen presentatiemalplaatje of de malplaatjes uit om de dynamische facetten uit te voeren.

   Zie Een presentatie [bewerken of een transportsjabloon](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3).

   Bijvoorbeeld, veronderstel dat u een malplaatje genoemd hebt `sim.tmpl` dat aan outputinhoud in de Simulator wordt gebruikt. Om dat malplaatje, op het productmenu uit te geven, klik **[!UICONTROL Design > Templates]**. Voor de [!DNL Templates] pagina, bepaal de plaats `sim.tmpl` in de lijst. en klik dan **[!UICONTROL Edit]** aan uiterst rechts van de naam. Voor de het Uitgeven pagina, voeg het volgende binnen het gebied van de facetvertoning van het malplaatje toe:

   ```
   <h6>DF RAIL</h6> 
   <guided-facet-rail gsname="__dynamic_facets"> 
               <guided-facet ><!-- behavior=Normal --> 
               <div class="facet-block" id="facet"> 
               <p><b><guided-facet-display-name /></b></p> 
               <ul> 
                   <guided-facet-values> 
                       <guided-if-facet-value-equals-length-threshold> 
               </ul> 
               <ul id="brand" style="display:none"> 
                       </guided-if-facet-value-equals-length-threshold> 
                       <guided-if-facet-value-selected> 
                           <li><guided-facet-value> [<guided-lt>a href="<guided-facet-value-undo-path />"<guided-gt>X</a>]</li> 
                       <guided-else-facet-value-selected> 
                           <li><guided-facet-link><guided-facet-value></guided-facet-link> (<guided-facet-count>) </li> 
                       </guided-if-facet-value-selected> 
                   </guided-facet-values> 
               </ul> 
               <guided-if-facet-long> 
                 <br /><guided-lt />a href="#" onclick="moreless(this,'brand');return false;" <guided-gt /><button style="font-size:10px;">VIEW MORE</button></a> 
               </guided-if-facet-long> 
               </div> 
               </guided-facet> 
   </guided-facet-rail> 
   <h6>/DF RAIL</h6>
   ```

   U zou een gelijkaardige wijziging aan andere malplaatjes van de Presentatie, zoals nodig ook aanbrengen `json.tmpl`.

   Zeker ben dat u `__dynamic_facets` voor `gsname` in de `guided-facet-rail` markering specificeert. Deze markering is een vooraf bepaalde facetspoorstaaf die voor het outputs van om het even welke dynamische facetten wordt gereserveerd die voor een bepaalde onderzoek zijn teruggekeerd.

   U kunt deze speciale facetspoorstaaf als Regels > BedrijfsRegels, en het gebruiken van de Geavanceerde Bouwer van de Regel ook naar keuze uitgeven zoals hieronder wordt gezien.

   ![](assets/dynamicfacetrail_businessrule.png)

   Zie ook [Een nieuwe bedrijfsregel toevoegen](../c-about-rules-menu/c-about-business-rules.md#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7)
