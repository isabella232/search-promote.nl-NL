---
description: U kunt SEO-metatags (Search Engine Optimization, optimalisatie van zoekprogramma's) gebruiken om bepaalde elementen van uw pagina's af te stemmen en zo de plaatsing van zoekprogramma's te verbeteren.
seo-description: U kunt SEO-metatags (Search Engine Optimization, optimalisatie van zoekprogramma's) gebruiken om bepaalde elementen van uw pagina's af te stemmen en zo de plaatsing van zoekprogramma's te verbeteren.
seo-title: Info SEO
solution: Target
subtopic: SEO
title: Info SEO
topic: Settings,Site search and merchandising
uuid: 5c5d64f5-fe79-4489-85c6-399d1437f2c4
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a
workflow-type: tm+mt
source-wordcount: '1226'
ht-degree: 0%

---


# Info over SEO{#about-seo}

U kunt SEO-metatags (Search Engine Optimization, optimalisatie van zoekprogramma&#39;s) gebruiken om bepaalde elementen van uw pagina&#39;s af te stemmen en zo de plaatsing van zoekprogramma&#39;s te verbeteren.

## SEO {#concept_C58BFCE720824A2B9B5F5E613CFD4C0B} gebruiken

U kunt elk element definiëren als een stuk begintekst gevolgd door een lijst met woorden. De lijst met woorden kan het volgende bevatten:

* Veelgebruikte zoektermen worden op uw site weergegeven gedurende een geselecteerde tijdsperiode (bijvoorbeeld &#39;vorige maand&#39;), afhankelijk van uw aangepaste uitsluitingen.
* Waardesets van een of meer velden uit de zoekopdracht waaruit de pagina afkomstig is.
* Statische woorden en woordgroepen die u in een lijst definieert

De meest gebruikte pagina-elementen die mensen voor SEO gebruiken, zijn de paginatitel en de metatags &#39;trefwoorden&#39; en &#39;beschrijving&#39;. U kunt instellingen definiëren voor deze drie pagina-elementen. Bovendien kunt u de volgende drie instellingen definiëren voor elk van de drie typen pagina&#39;s: Resultaatpagina&#39;s zoeken, door pagina&#39;s bladeren en pagina&#39;s met itemgegevens zoeken.

Wanneer u sparen of voorproef uw montages SEO, kleine segmenten van onderzoek (vervoer) malplaatjes produceert die u in uw andere onderzoeksmalplaatjes met de `<search-include>` malplaatjemarkering kunt omvatten. U kunt bijvoorbeeld het veld Titel van pagina&#39;s met zoekresultaten als volgt in een andere sjabloon opnemen:

```
<search-include file="seo/seo_search_title.tpl" />
```

De negen mogelijke waarden voor het kenmerk `file` van de tag `<search-include>` voor SEO-velden zijn:

* `seo/seo_search_title.tpl`
* `seo/seo_search_description.tpl`
* `seo/seo_search_keywords.tpl`
* `seo/seo_browse_title.tpl`
* `seo/seo_browse_description.tpl`
* `seo/seo_browse_keywords.tpl`
* `seo/seo_item_title.tpl`
* `seo/seo_item_description.tpl`
* `seo/seo_item_keywords.tpl`

Als u SEO-velden in een presentatiesjabloon wilt gebruiken, voert u verschillende stappen uit.

Eerst gebruikt u `<search-include>` zoals hierboven beschreven om de gewenste velden op te nemen in een XML-zoeksjabloon, binnen een element `<general>`.

Rond vervolgens elke `<search-include>`-tag met `<general-field>`- en `</general-field>`-tags, waarbij de veldnamen in het `name`-kenmerk worden weergegeven zoals in het volgende voorbeeld:

```
<general> 
    <general-field name="seo_search_title"><search-include file="seo/seo_search_title.tpl" /></general-field> 
    <general-field name="seo_search_description"><search-include file="seo/seo_search_description.tpl" /></general-field> 
    <general-field name="seo_search_keywords"><search-include file="seo/seo_search_keywords.tpl" /></general-field> 
</general>
```

Vervolgens kunt u in uw presentatiesjabloon `<guided-general-field>`-tags gebruiken om de benoemde velden op de gewenste plaats in te voegen, zoals in het volgende voorbeeld:

```
<title><guided-general-field gsname="default" field="seo_search_title"></title> 
<meta name="description" content="<guided-general-field gsname="default" field="seo_search_description">"/> 
<meta name="keywords" content="<guided-general-field gsname="default" field="seo_search_keywords">"/>
```

Let op het gebruik van het `gsname`-kenmerk om in dit geval de standaardzoekopdracht op te geven.

In totaal kunt u negen verschillende SEO-velden definiëren die u kunt gebruiken in uw webpagina&#39;s. Deze omvatten:

* Pagina&#39;s met zoekresultaten - titel, beschrijving en trefwoorden
* Door pagina&#39;s bladeren - titel, beschrijving en trefwoorden
* Pagina&#39;s met itemdetails - titel, beschrijving en trefwoorden

Alle negen velden zijn gedefinieerd met vergelijkbare instellingen. In feite zijn de namen van de negen velden, zoals het veld &quot;Titel&quot; in &quot;Pagina&#39;s met zoekresultaten&quot;, slechts suggesties voor het gebruik ervan. U kunt alle velden in elke gewenste context gebruiken in uw presentatiesjablonen en zoeksjablonen.

Zie ook [Informatie over sjablonen](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5).

Zie ook [Labels voor presentatiesjablonen](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64).

Zie ook [Sjabloontags zoeken](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4).

Zie ook [Een woordenlijst met zoekresultaten configureren](../c-about-settings-menu/c-about-seo.md#task_A459A3734EC04042BA52C81184251DD4).

## Een woordenlijst met zoekresultaten configureren {#task_A459A3734EC04042BA52C81184251DD4}

U kunt de lijst met zoekresultaatwoorden en -woordgroepen configureren die worden opgenomen in paginatitels, beschrijvingen en trefwoorden.

**Een woordenlijst met zoekresultaten configureren**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL SEO]** > **[!UICONTROL Search Result Pages]**.
1. Stel op de pagina [!DNL SEO Browse Pages Word List] in de respectievelijke groepen [!DNL Title], [!DNL Description] en [!DNL Keywords] de gewenste opties in.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Titel | Beschrijving | Trefwoorden beginnen met </p> </td> 
      <td colname="col2"> <p>De tekst die u vóór de woordenlijst wilt weergeven. </p> <p>U wilt bijvoorbeeld dat de lijst Trefwoorden begint met het woord ''Merken''. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Inclusief populaire zoekopdrachten tijdens </p> </td> 
      <td colname="col2"> <p>De periode waarvoor zoekopdrachten worden opgenomen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Maximum aantal zoekopdrachten </p> </td> 
      <td colname="col2"> <p>Het maximale aantal zoekopdrachten dat wordt opgenomen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Veldwaarden opnemen </p> </td> 
      <td colname="col2"> <p>De veldwaarden die zijn opgenomen in de woordenlijst van de resultaten. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Deze woorden en woordgroepen toevoegen </p> </td> 
      <td colname="col2"> <p>Geef een lijst op van de woorden die u wilt toevoegen aan de paginatitel van de zoekresultaten, de paginatitel van de bladerpagina of de titel van de detailpagina van het item. </p> <p>Klik <b>Bewerken</b> om woorden aan de lijst toe te voegen. </p> <p>U kunt per regel één woord of woordgroep toevoegen. Wanneer u wordt gebeëindigd, klik <b>sparen Veranderingen</b>, en sluit dan de pagina om aan de belangrijkste SEO pagina terug te keren. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Deze woorden en woordgroepen verwijderen (met uitzondering van opgenomen veldwaarden) </p> </td> 
      <td colname="col2"> <p>Geef een lijst weer van de woorden die u wilt verwijderen uit de paginatitel van de zoekresultaten, de paginatitel van de bladerpagina of de titel van de detailpagina van het item. </p> <p>Klik <b>Bewerken</b> om woorden toe te voegen aan de lijst Verwijderen. </p> <p>U kunt per regel één woord of woordgroep toevoegen. Wanneer u wordt gebeëindigd, klik <b>sparen Veranderingen</b>, en sluit dan de pagina om aan de belangrijkste SEO pagina terug te keren. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. (Optioneel) Klik op **Voorbeeld van voorbeelduitvoer** om een voorvertoning weer te geven van de resulterende waarden voor de SEO-velden die u instelt.

   Zie [Een voorvertoning weergeven van de SEO-metatags die u hebt geconfigureerd](../c-about-settings-menu/c-about-seo.md#task_3F97949E193C4F92A104AD117FE49621).
1. Klik **Wijzigingen opslaan**.
1. (Optioneel) Maak de gefaseerde site-index opnieuw als u een voorvertoning van de resultaten wilt zien.

   Zie [Een incrementele index van een gefaseerde website configureren](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Optioneel) Voer op de pagina [!DNL SEO Search Results Word List] een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Woordenlijst {#task_D7A1D765A92A4D6C94E672B3A86ECB5A} voor een bladerpagina configureren

U kunt de lijst configureren met woorden en woordgroepen op pagina&#39;s die in paginatitels, beschrijvingen en trefwoorden worden opgenomen.

**Een woordenlijst voor bladerpagina&#39;s configureren**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL SEO]** > **[!UICONTROL Browse Pages]**.
1. Stel op de pagina [!DNL SEO Browse Pages Word List] in de respectievelijke groepen [!DNL Title], [!DNL Description] en [!DNL Keywords] de gewenste opties in.

   Zie de lijst van opties onder [Vormend een woordlijst van onderzoeksresultaten](../c-about-settings-menu/c-about-seo.md#task_A459A3734EC04042BA52C81184251DD4).
1. (Optioneel) Klik op **Voorbeeld van voorbeelduitvoer** om een voorvertoning weer te geven van de resulterende waarden voor de SEO-velden die u instelt.

   Zie [Een voorvertoning weergeven van de SEO-metatags die u hebt geconfigureerd](../c-about-settings-menu/c-about-seo.md#task_3F97949E193C4F92A104AD117FE49621).
1. Klik **Wijzigingen opslaan**.
1. (Optioneel) Maak de gefaseerde site-index opnieuw als u een voorvertoning van de resultaten wilt zien.

   Zie [Een incrementele index van een gefaseerde website configureren](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Optioneel) Voer op de pagina [!DNL SEO Browse Pages Word List] een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een woordenlijst met itemdetails configureren {#task_761538C519B34164BE189F13C39B2495}

U kunt de lijst met woorden en woordgroepen met itemdetails configureren die worden opgenomen in paginatitels, beschrijvingen en trefwoorden.

**Om een het woordlijst van het puntdetail te vormen**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL SEO]** > **[!UICONTROL Item Detail Pages]**.
1. Stel op de pagina [!DNL SEO Item Detail Word List] in de respectievelijke groepen [!DNL Title], [!DNL Description] en [!DNL Keywords] de gewenste opties in.

   Zie de lijst van opties onder [Vormend een woordlijst van onderzoeksresultaten](../c-about-settings-menu/c-about-seo.md#task_A459A3734EC04042BA52C81184251DD4).
1. (Optioneel) Klik op **Voorbeeld van voorbeelduitvoer** om een voorvertoning weer te geven van de resulterende waarden voor de SEO-velden die u instelt.

   Zie [Een voorvertoning weergeven van de SEO-metatags die u hebt geconfigureerd](../c-about-settings-menu/c-about-seo.md#task_3F97949E193C4F92A104AD117FE49621).
1. Klik **Wijzigingen opslaan**.
1. (Optioneel) Maak de gefaseerde site-index opnieuw als u een voorvertoning van de resultaten wilt zien.

   Zie [Een incrementele index van een gefaseerde website configureren](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Optioneel) Voer op de pagina [!DNL SEO Item Detail Word List] een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een voorvertoning weergeven van de SEO-metatags die u {#task_3F97949E193C4F92A104AD117FE49621} hebt geconfigureerd

U kunt een voorvertoning weergeven van de resulterende waarden voor de SEO-velden die u instelt om te zien wat er is ingevoegd op de plaats waar u ze gebruikt.

SEO-velden kunnen opgenomen veldwaarden bevatten, zodat de zoekresultaten afhankelijk kunnen zijn van de zoekquery die u opgeeft.

**De door u geconfigureerde SEO-metatags voorvertonen**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL SEO]** > **[!UICONTROL Search Result Pages]**.
1. Klik op de SEO-pagina op **Voorbeeld van voorbeelduitvoer**.
1. Typ op de pagina [!DNL SEO Preview] in het veld [!DNL Enter sample query] de zoekterm die u wilt zoeken.
1. Klik **Zoeken**.

   De resulterende velden Titel, Beschrijving en Trefwoorden geven de inhoud weer die op basis van de zoekquery die u zojuist hebt ingevoerd, op een pagina wordt ingevoegd.
1. Klik **Close** om naar de belangrijkste SEO pagina terug te keren.
