---
description: U kunt SEO (de Optimalisering van de Motor van het Onderzoek) meta-markeringen gebruiken helpen bepaalde elementen van uw pagina's aanpassen en daardoor de plaatsing van de onderzoeksmotor verbeteren.
seo-description: U kunt SEO (de Optimalisering van de Motor van het Onderzoek) meta-markeringen gebruiken helpen bepaalde elementen van uw pagina's aanpassen en daardoor de plaatsing van de onderzoeksmotor verbeteren.
seo-title: Over SEO
solution: Target
subtopic: SEO
title: Over SEO
topic: Settings,Site search and merchandising
uuid: 5c5d64f5-fe79-4489-85c6-399d1437f2c4
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a

---


# Over SEO{#about-seo}

U kunt SEO (de Optimalisering van de Motor van het Onderzoek) meta-markeringen gebruiken helpen bepaalde elementen van uw pagina&#39;s aanpassen en daardoor de plaatsing van de onderzoeksmotor verbeteren.

## SEO gebruiken {#concept_C58BFCE720824A2B9B5F5E613CFD4C0B}

U kunt elk dergelijk element als stuk beginnende tekst bepalen die door een lijst van woorden wordt gevolgd. De lijst van woorden kan het volgende omvatten:

* De populaire onderzoeksuitdrukkingen op uw plaats over een geselecteerde tijdspanne (bijvoorbeeld, &quot;vorige maand&quot;), behoudens uw douanevrijstellingen.
* De reeksen van de waarde van één of meerdere gebieden van het onderzoek de pagina kwam van.
* De statische woorden en de uitdrukkingen die u in een lijst bepaalt

De gemeenschappelijkste paginaelementen die de mensen voor SEO gebruiken zijn de paginatitel, en de &quot;sleutelwoorden&quot;en &quot;beschrijving&quot;meta-markeringen. U kunt montages voor deze drie paginaelementen bepalen. Bovendien, kunt u deze drie montages voor elk van de drie types van pagina&#39;s bepalen: De Pagina&#39;s van het Resultaat van het onderzoek, doorbladeren Pagina&#39;s, en de Pagina&#39;s van het Detail van het Punt.

Wanneer u sparen of voorproef uw montages SEO, kleine segmenten van onderzoek (vervoer) malplaatjes wordt geproduceerd die u in uw andere onderzoeksmalplaatjes met de `<search-include>` malplaatjemarkering kunt omvatten. Als voorbeeld, kunt u het gebied van de Titel van de Pagina&#39;s van de Resultaten van het Onderzoek in een ander malplaatje met het volgende omvatten:

```
<search-include file="seo/seo_search_title.tpl" />
```

De negen mogelijke waarden voor de `file` attributen van de `<search-include>` markering voor gebieden SEO zijn de volgende:

* `seo/seo_search_title.tpl`
* `seo/seo_search_description.tpl`
* `seo/seo_search_keywords.tpl`
* `seo/seo_browse_title.tpl`
* `seo/seo_browse_description.tpl`
* `seo/seo_browse_keywords.tpl`
* `seo/seo_item_title.tpl`
* `seo/seo_item_description.tpl`
* `seo/seo_item_keywords.tpl`

Om de gebieden van SEO in een presentatiemalplaatje te gebruiken, voltooit u verscheidene stappen.

Eerst, gebruikt u `<search-include>` zoals hierboven beschreven om de gewenste gebieden in een het onderzoeksmalplaatje van XML, binnen een `<general>` element te omvatten.

Dan, omring elke `<search-include>` markering met `<general-field>` en `</general-field>` markeringen, die de gebiedsnamen in de `name` attributen zoals in het volgende voorbeeld geven:

```
<general> 
    <general-field name="seo_search_title"><search-include file="seo/seo_search_title.tpl" /></general-field> 
    <general-field name="seo_search_description"><search-include file="seo/seo_search_description.tpl" /></general-field> 
    <general-field name="seo_search_keywords"><search-include file="seo/seo_search_keywords.tpl" /></general-field> 
</general>
```

Dan, in uw presentatiemalplaatje, kunt u `<guided-general-field>` markeringen gebruiken om de genoemde gebieden op te nemen waar u zoals in het volgende voorbeeld nodig hebt:

```
<title><guided-general-field gsname="default" field="seo_search_title"></title> 
<meta name="description" content="<guided-general-field gsname="default" field="seo_search_description">"/> 
<meta name="keywords" content="<guided-general-field gsname="default" field="seo_search_keywords">"/>
```

Merk het gebruik van het `gsname` attribuut op om, in dit geval, het &quot;gebrek&quot;onderzoek te specificeren.

Alles bij elkaar, kunt u negen verschillende gebieden bepalen van de ZOO die u in uw Web-pagina&#39;s kunt gebruiken. Zij omvatten het volgende:

* Pagina&#39;s met zoekresultaten - titel, beschrijving en trefwoorden
* Bladeren door pagina&#39;s - titel, beschrijving en trefwoorden
* Details van object - titel, beschrijving en trefwoorden

Alle negen gebieden worden bepaald met gelijkaardige montages. In feite, zijn de namen van de negen gebieden, zoals het &quot;titel&quot;gebied in de Pagina&#39;s van de Resultaten van het Onderzoek&quot;, slechts suggesties van hoe u hen zou kunnen gebruiken. U kunt om het even welke gebieden in om het even welke context in uw presentatiemalplaatjes en onderzoeksmalplaatjes gebruiken.

Zie ook [over Malplaatjes](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5).

Zie ook de malplaatjelags [van de](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)Presentatie.

Zie ook sjabloontags voor [zoekopdrachten](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4).

Zie ook het [Vormen van een het woordlijst](../c-about-settings-menu/c-about-seo.md#task_A459A3734EC04042BA52C81184251DD4)van onderzoeksresultaten.

## Een tekstlijst met zoekresultaten configureren {#task_A459A3734EC04042BA52C81184251DD4}

U kunt de lijst van de woorden en de uitdrukkingen van het onderzoeksresultaat vormen die in paginatitels, beschrijvingen, en sleutelwoorden inbegrepen zijn.

**Om een het woordlijst van onderzoeksresultaten te vormen**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL SEO]** > **[!UICONTROL Search Result Pages]**.
1. Voor de [!DNL SEO Browse Pages Word List] pagina, in de respectieve [!DNL Title], [!DNL Description], en de [!DNL Keywords] groepen, plaats de opties die u wilt.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Optie </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Titel| Beschrijving| Trefwoorden beginnen met </p> </td> 
      <td colname="col2"> <p>De tekst die u voor de woordlijst wilt tonen. </p> <p>Bijvoorbeeld, zou u de lijst van Sleutelwoorden met het woord "Merken"kunnen willen beginnen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Inclusief populaire zoekopdrachten tijdens </p> </td> 
      <td colname="col2"> <p>De periode waarvoor de onderzoeken worden omvat. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Maximum aantal zoekopdrachten </p> </td> 
      <td colname="col2"> <p>Het maximumaantal onderzoeken die inbegrepen zijn. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Veldwaarden opnemen </p> </td> 
      <td colname="col2"> <p>De gebiedswaarden die in de lijst van het resultaatwoord inbegrepen zijn. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Voeg deze Woorden &amp; de Zetters toe </p> </td> 
      <td colname="col2"> <p>Maak een lijst van de woorden die u aan de de paginatitel van de onderzoeksresultaten wilt toevoegen, doorblader paginatitel, of de de paginatitel van het puntdetail. </p> <p>Klik <b>uitgeven</b> om woorden aan de lijst toe te voegen. </p> <p>U kunt één woord of uitdrukking per lijn toevoegen. Wanneer u wordt gebeëindigd, klik <b>sparen Veranderingen</b>, en sluit dan de pagina om aan de belangrijkste SEO pagina terug te keren. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Verwijder deze Woorden &amp; Zetters (behalve uit inbegrepen gebiedswaarden) </p> </td> 
      <td colname="col2"> <p>Maak een lijst van de woorden die u uit de de paginatitel van de onderzoeksresultaten wilt verwijderen, doorblader paginatitel, of de de paginatitel van het puntdetail. </p> <p>Klik op <b>Bewerken</b> om woorden toe te voegen aan de lijst verwijderen. </p> <p>U kunt één woord of uitdrukking per lijn toevoegen. Wanneer u wordt gebeëindigd, klik <b>sparen Veranderingen</b>, en sluit dan de pagina om aan de belangrijkste SEO pagina terug te keren. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. (Facultatief) klik de Output **van de Steekproef van de** Voorproef aan voorproef de resulterende waarden voor de gebieden SEO die u plaatst.

   Zie [Previewing de meta-markeringen van SEO die u vormde](../c-about-settings-menu/c-about-seo.md#task_3F97949E193C4F92A104AD117FE49621).
1. Klik **sparen Veranderingen**.
1. (Facultatief) herbouw uw gefaseerde plaatsindex als u aan voorproef de resultaten wilt.

   Zie [het Vormen van een stijgende index van een gefaseerde website](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Facultatief) op de [!DNL SEO Search Results Word List] pagina, doe om het even welke volgend:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Het vormen doorbladert de lijst van het paginabereik {#task_D7A1D765A92A4D6C94E672B3A86ECB5A}

U kunt de lijst vormen van doorbladeren pagina&#39;s woorden en uitdrukkingen die in paginatitels, beschrijvingen, en sleutelwoorden inbegrepen zijn.

**Om te vormen doorblader pagina&#39;s woordlijst**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL SEO]** > **[!UICONTROL Browse Pages]**.
1. Voor de [!DNL SEO Browse Pages Word List] pagina, in de respectieve [!DNL Title], [!DNL Description], en de [!DNL Keywords] groepen, plaats de opties die u wilt.

   Zie de lijst van opties onder het [Vormen van een het woordlijst](../c-about-settings-menu/c-about-seo.md#task_A459A3734EC04042BA52C81184251DD4)van onderzoeksresultaten.
1. (Facultatief) klik de Output **van de Steekproef van de** Voorproef aan voorproef de resulterende waarden voor de gebieden SEO die u plaatst.

   Zie [Previewing de meta-markeringen van SEO die u vormde](../c-about-settings-menu/c-about-seo.md#task_3F97949E193C4F92A104AD117FE49621).
1. Klik **sparen Veranderingen**.
1. (Facultatief) herbouw uw gefaseerde plaatsindex als u aan voorproef de resultaten wilt.

   Zie [het Vormen van een stijgende index van een gefaseerde website](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Facultatief) op de [!DNL SEO Browse Pages Word List] pagina, doe om het even welke volgend:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Het vormen van een het woordlijst van het puntdetail {#task_761538C519B34164BE189F13C39B2495}

U kunt de lijst van de woorden en de uitdrukkingen van het puntdetail vormen die in paginatitels, beschrijvingen, en sleutelwoorden inbegrepen zijn.

**Om een het woordlijst van het puntdetail te vormen**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL SEO]** > **[!UICONTROL Item Detail Pages]**.
1. Voor de [!DNL SEO Item Detail Word List] pagina, in de respectieve [!DNL Title], [!DNL Description], en de [!DNL Keywords] groepen, plaats de opties die u wilt.

   Zie de lijst van opties onder het [Vormen van een het woordlijst](../c-about-settings-menu/c-about-seo.md#task_A459A3734EC04042BA52C81184251DD4)van onderzoeksresultaten.
1. (Facultatief) klik de Output **van de Steekproef van de** Voorproef aan voorproef de resulterende waarden voor de gebieden SEO die u plaatst.

   Zie [Previewing de meta-markeringen van SEO die u vormde](../c-about-settings-menu/c-about-seo.md#task_3F97949E193C4F92A104AD117FE49621).
1. Klik **sparen Veranderingen**.
1. (Facultatief) herbouw uw gefaseerde plaatsindex als u aan voorproef de resultaten wilt.

   Zie [het Vormen van een stijgende index van een gefaseerde website](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Facultatief) op de [!DNL SEO Item Detail Word List] pagina, doe om het even welke volgend:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Previewing de meta-markeringen van SEO die u vormde {#task_3F97949E193C4F92A104AD117FE49621}

U kunt voorproef de resulterende waarden voor de gebieden van SEO die u plaatst om te zien wat wordt opgenomen waar u hen gebruikt.

De gebieden van SEO kunnen inbegrepen gebiedswaarden bevatten, zodat kunnen de onderzoeksresultaten van de onderzoeksvraag afhangen die u specificeert.

**Aan voorproef de meta-markeringen van SEO die u vormde**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL SEO]** > **[!UICONTROL Search Result Pages]**.
1. Voor de SEO pagina, klik de Output van de Steekproef van de **Voorproef**.
1. Op de [!DNL SEO Preview] pagina, op het [!DNL Enter sample query] gebied, typ de vraagtermijn u wilt zoeken op.
1. Klik op **Zoeken**.

   De resulterende gebieden van de Titel, van de Beschrijving, en van Sleutelwoorden tonen de inhoud die in een pagina wordt opgenomen die op de onderzoeksvraag wordt gebaseerd u enkel inging.
1. Klik op **Sluiten** om terug te keren naar de hoofdpagina van de afkorting SEO.
