---
description: De Regels van de Schoonmaak van de Vraag van het gebruik om de inkomende vraag te analyseren en te wijzigen.
solution: Target
title: Info over Regels voor het opschonen van query's
topic: Regels, zoeken en verhandelen van sites
uuid: 683af81f-f7c0-45f8-9212-e5e7cb82ccca
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '1601'
ht-degree: 0%

---


# Info over Regels voor het opschonen van query{#about-query-cleaning-rules}

De Regels van de Schoonmaak van de Vraag van het gebruik om de inkomende vraag te analyseren en te wijzigen.

## Het gebruiken van de Regels van het Schoonmaken van de Vraag {#concept_17F3CDDC3C8A4128AF092A82B777B86C}

Deze functie wordt vaak gebruikt wanneer u het zoeken/verhandelen van sites wilt wijzigen. U kunt bijvoorbeeld een lege zoekopdracht wijzigen in een populair trefwoord in plaats van een &quot;*&quot;-zoekopdracht, zodat u een populair product kunt promoten. U kunt query-reinigingsregels ook gebruiken om een directe hit uit te voeren, waarbij u doorstuurt naar een URL. Dit kan bijzonder nuttig zijn wanneer u ontdekt dat iemand naar productSKU zoekt en u het onderzoek wilt overslaan en aan de pagina van dat product opnieuw richten. Het Schoonmaken van de vraag kan de vraag ook ontmijnen en douanevariabelen plaatsen die in recentere stappen van de verwerkingsstroom kunnen worden gebruikt. De het schoonmaken van de vraag regels worden uitgevoerd in opeenvolging voor elke vraag. U kunt slepen en neerzetten gebruiken om de volgorde van de regels te wijzigen. De daadwerkelijke orde wordt niet veranderd tot u het opslaat.

De vraag schoonmaakregels in een vraag schoonmaakmodule worden onderzocht om te bepalen als om het even welke vraagparameters moeten worden gewijzigd of als om het even welke douanevariabelen moeten worden geplaatst. Elke regel voor het schoonmaken van query bestaat uit twee hoofdelementen: het optreden van de regel en de facultatieve voorwaarden. Er kan een onbeperkt aantal regels en voorwaarden worden opgegeven. De orde van deze regels is belangrijk, aangezien het plaatsonderzoek/het merchandising lijnen door de regel door regel wordt geplaatst. Wanneer de voorwaarden van een regel overeenkomen, worden alle bijbehorende acties uitgevoerd.

Nadat de vraag wordt schoongemaakt, worden de resulterende parameters CGI gebruikt vooruit. Alle aangepaste variabelen die zijn ingesteld, kunnen later in de verwerkingsflow worden gebruikt. Standaard verwijdert het systeem automatisch de regelafstand en de witruimte aan het einde van de zoekterm.

## Info over Voorwaarden voor Query Cleaning {#section_BF6F25F94FED4DDEA8600D921EA43A66}

Voorwaarden zijn optioneel. Als u besluit dat de acties voor elke vraag worden gespecificeerd, worden de acties altijd genomen. De voorwaarden kunnen op om het even welke CGI vraagparameter, bestaand koekje, of douanevariabele worden gebaseerd die een vorige regel heeft geplaatst. Het wordt beschouwd als &quot;beste praktijken&quot;voor de eerste vraag schoonmaakregel voor elke vraag in werking te stellen, waar het bepaalt en alle douanevariabelen initialiseert u van plan bent te gebruiken.

## Informatie over handelingen voor het opschonen van query&#39;s {#section_78F74A9B48DE484191CDA95F5B4E7154}

Alle acties binnen een regel van de vraagschoonmaak die passende voorwaarden heeft worden uitgeoefend. Handelingen bestaan doorgaans uit een bewerking, de gegevens waarop de bewerking moet worden uitgevoerd en de waarde die moet worden gebruikt.

Zie de lijst van opties in [Toevoegend een vraag schoonmaakregel](../c-about-rules-menu/c-about-query-cleaning-rules.md#task_47F43988D3D9485F8AE1DFDA7E00BF54).

## Informatie over omleidingen {#section_597481E6194440C0A7B9E6FC901A81C0}

Met de interface Direct-Hits kunt u een set omleidingen definiëren op basis van de binnenkomende queryterm. Dit idee wordt uitgebreid met omleidingen binnen Query Cleaning. Omleiding geeft u echter een fijnere granulariteit op wanneer omleiding plaatsvindt via het opgeven van voorwaarden. U kunt omleiden naar een dynamische URL in plaats van een statische URL. Wanneer u de omleidingsactie selecteert, wordt de rij bijgewerkt om een tekstvakje te hebben waar u URL specificeert u aan wilt opnieuw richten. In de URL kunt u variabelen of parameters opgeven die u wilt vervangen door deze tussen dubbele accolades te plaatsen. Aangepaste variabelen hebben een hogere prioriteit dan CGI-parameters in de vervanging.

## Voorbeelden {#section_DB5047CC38FB4A57B15CAAF9848073E3}

Stel dat u een kledingwinkel hebt met een website. Als de gebruiker op Zoeken klikt zonder zoektermen, wilt u een zoekopdracht retourneren tegen jeans, omdat dat uw internationale reputatie is. U wilt ook de vraagtermijn voor een geslacht ontleden zodat u een regel kunt tot stand brengen pre-onderzoek later, die op de douanevariabele wordt gebaseerd die een verschillend presentatiemalplaatje voor elk geslacht gebruikt.

```
On condition: 
  query q equal 
Perform the following actions: 
  Set query parameter q to value jeans 
 
On condition: 
  Query q matches regular expression wom[e|a]n[s]|girl[s] 
Perform the following actions: 
  Add custom variable gender 
  Set custom variable gender to value female 
 
On condition: 
  Query q matches regular expression men[s]|boy[s] 
Perform the following actions: 
  Add custom variable gender 
  Set custom variable gender to value male
```

MegaElectronic is een grote elektronicawinkel. Door hun zoekgegevens te analyseren, heeft MegaElectronic opgemerkt dat veel van hun meedogenloze klanten vaak zoeken naar een product met behulp van de SKU van het product, in plaats van een zoekresultaat voor het ene product te retourneren, wil MegaElectronic graag doorverwijzen naar de webpagina die bij die SKU hoort.

```
On condition: 
  query q matches regular expression ^\D\D\D-\d\d\d\d$ 
Perform the following actions: 
  redirect to https://www.megaelectronic.com/?sku={{q}}
```

## Een queryreinigingsregel {#task_47F43988D3D9485F8AE1DFDA7E00BF54} toevoegen

U kunt regels definiëren die de binnenkomende zoekquery van een klant opschonen of bewerken.

U kunt alleen sjablonen selecteren die op dat moment bestaan. Als u geen sjablonen hebt, moet u deze eerst definiëren.

Zie [Informatie over sjablonen](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5).

**Een regel voor het opschonen van query&#39;s toevoegen**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Query Cleaning]**.
1. Klik op [!DNL Query Cleaning Rules] op de pagina.**[!UICONTROL Add New Rule]**
1. Typ in het veld [!DNL Name] de naam van de nieuwe regel voor het opschonen van query.
1. Voor de [!DNL Add Query Cleaning Rule] pagina, gebruik de drop-down lijsten en tekstgebieden om uw vraag te bouwen.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Cookie </p> </td> 
      <td colname="col2"> <p>Een HTTP-cookie. U kunt voorwaarden definiëren op basis van cookies die aan uw domein zijn gekoppeld. U kunt ook een cookie instellen die met de uitgaande zoekresultaten wordt geschreven. Naam en waarden van cookies moeten zijn gecodeerd als Uniform Resource Identifier. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Aangepaste variabele </p> </td> 
      <td colname="col2"> <p>Een door de gebruiker gedefinieerde variabele. U kunt een onbeperkt aantal door de gebruiker gedefinieerde variabelen toevoegen, verwijderen of instellen. U kunt door de gebruiker gedefinieerde variabelen hier weergeven in Regels voor voorzoeken en Regels voor achteraf zoeken. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Systeemvariabele </p> </td> 
      <td colname="col2"> <p>Alleen-lezen variabelen ingesteld door het interne systeem dat u kunt controleren. De volgende systeemvariabelen worden ondersteund: </p> <p> 
        <ul id="ul_BC17F1637F27424CA4E8F530C28A3245"> 
          <li id="li_C7DF96EFD7AA4A449D00F7EACCAA0EB1"> <span class="uicontrol"> hostnaam  </span> <p>De naam van de serverhost. </p> </li> 
          <li id="li_F85AB1D2B9374A859657D12B8ED6674B"> <span class="uicontrol"> uri  </span> <p>De aangevraagde uri zonder de querytekenreeks. </p> </li> 
          <li id="li_440149C9EC6E4805B77BBC97BE41542A"> <span class="uicontrol"> args  </span> <p>De volledige queryreeks. </p> </li> 
          <li id="li_F583FC4B0E404858BB3522B33A6F7A0A"> <span class="uicontrol"> milieu  </span> <p>"Stage" of "live", afhankelijk van het feit of de binnenkomende query naar uw gefaseerde of live omgeving is verzonden. </p> </li> 
          <li id="li_15902AA49B144D42A5E95D7E8B0FB1E1"> <span class="uicontrol"> referentie  </span> <p>De URL waar de klant vandaan komt. </p> </li> 
          <li id="li_6FEE352DB7A842FCB2EBE1398AD03666"> <span class="uicontrol"> gebruikersagent  </span> <p>De "user-agent"koord van browser van de klant. </p> </li> 
        </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Query-parameter </p> </td> 
      <td colname="col2"> <p>CGI-parameters die aan de query zijn doorgegeven. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Backend-parameter </p> </td> 
      <td colname="col2"> <p>Binnenkomende vraagparameters worden uiteindelijk vertaald in achterste parameters die worden gebruikt om het onderzoek uit te voeren. </p> <p>Zie <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> CGI-parameters voor achtergrondzoekopdrachten </a>. </p> <p>Achterste parameters worden niet weergegeven op navigatie-elementen. Dientengevolge, kunt u om het even welke extra parameters verbergen die u op een onderzoek van uw klanten wilt toepassen. Acties betreffende parameters van het achterste deel zijn te laat bindend; dat wil zeggen, ze worden toegepast vlak voordat de zoekopdracht wordt verzonden. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Facet </p> </td> 
      <td colname="col2"> <p>Speciale CGI-parameters die aan een bepaalde facet zijn gekoppeld. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Rang </p> </td> 
      <td colname="col2"> <p>Hier kunt u opgeven welke rangorderegel u wilt gebruiken in de zoekopdracht. Deze optie wordt alleen weergegeven wanneer u een aantal waarderingsvelden en waarderingsregels hebt gedefinieerd. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Winkel </p> </td> 
      <td colname="col2"> <p>De zoekmachine detecteert automatisch in welke opslag de gebruiker zich bevindt op basis van de hostnaam of de <span class="codeph"> gs_store </span>-queryparameter, waarbij de laatste voorrang heeft. U kunt voorwaarden buiten de winkel maken. Alleen bij query-reiniging kunt u ook een handeling gebruiken om de huidige winkel te overschrijven. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Laatste regel </p> </td> 
      <td colname="col2"> <p>Wanneer de voorwaarden voor een regel worden voldaan die laatste regelreeks heeft, voert de vraag zuiveringsverwerkingsmodule geen extra regels na de actie van de passende regel uit. Dit is handig wanneer u handelingen hebt ingesteld die ertoe leiden dat een latere regel overeenkomt, maar u niet wilt dat de latere regel wordt geactiveerd. Merk op dat, als de actie van een regel redirect moet uitvoeren, het opnieuw richten onmiddellijk plaatsvindt, zodat doet het hoofdzakelijk alsof de laatste regel werd geplaatst. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Onderbreken </p> </td> 
      <td colname="col2"> <p>Hiermee schakelt u het uitvoeren van de regel uit, maar wordt de regel niet verwijderd. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Klik op **[!UICONTROL Add]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een query-reinigingsregel {#task_FA2FF1A7E2634350AD703485CBC27CB3} bewerken

U kunt bestaande regels van de vraagschoonmaak uitgeven die u aan de pagina van de Regels van de Schoonmaak van de Vraag hebt toegevoegd.

**Een regel voor het opruimen van query&#39;s bewerken**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Query Cleaning]**.
1. Op [!DNL Query Cleaning Rules] pagina, onder **[!UICONTROL Actions]** kolom van de lijst, klik **[!UICONTROL Edit]** voor de bijbehorende regel die u wilt uitgeven.
1. Voor de [!DNL Edit Query Cleaning Rule] pagina, gebruik de drop-down lijsten en tekstgebieden om uw vraag te bouwen.

   Zie de lijst van opties onder [Toevoegend een vraag schoonmaakregel](../c-about-rules-menu/c-about-query-cleaning-rules.md#task_47F43988D3D9485F8AE1DFDA7E00BF54).
1. Klik op **[!UICONTROL Save Changes]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een query-reinigingsregel {#task_C52D17226B824590B087CAB6970CBB01} verwijderen

U kunt de regels voor het schoonmaken van query&#39;s verwijderen die u niet meer nodig hebt of gebruikt.

Wanneer u een regel schrapt, wordt de orde dat de resterende regels in werking worden gesteld automatisch aangepast aan rekening voor de schrapping.

**Een regel voor het opschonen van query&#39;s verwijderen**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Query Cleaning]**.
1. Op [!DNL Query Cleaning Rules] pagina, onder **[!UICONTROL Actions]** kolom van de lijst, klik **[!UICONTROL Delete]** voor de bijbehorende regel die u wilt schrappen.
1. Klik in het dialoogvenster [!DNL Confirmation] op **[!UICONTROL OK]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Het veranderen van de orde die de vraag schoonmaakregels {#task_C24012C45A4445468A7FD998017388CA} in werking stellen

U kunt de regels voor het schoonmaken van query&#39;s opnieuw ordenen om de volgorde te wijzigen waarin ze op presentatiesjablonen worden uitgevoerd.

Schoonmaakregels voor query&#39;s worden uitgevoerd in de volgorde waarin ze zijn gedefinieerd. Hoger het de ordeaantal van een regel, later het in het proces loopt, die vroegere regels beweegt. U wijzigt de volgorde van de regels door een nieuw nummer in te voeren in de kolom Volgorde van de tabel op de pagina [!DNL Query Cleaning Rules]. U kunt slepen-en-neerzetten op regels ook gebruiken om hun runtime orde te veranderen.

**Om de orde te veranderen die de vraag zuiveringsregels in werking stelt**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Query Cleaning]**.
1. Voer op de pagina [!DNL Query Cleaning Rules] een van de volgende handelingen uit:

   * Klik op de kolomkop [!DNL Order] om de regels in oplopende of aflopende volgorde te sorteren.
   * In [!DNL Order] kolom, op het tekstgebied links van een naam van de vraagschoonmaakregel, typ het ordeaantal dat u de regel wilt in werking stellen.
   * Sleep een tabelrij naar de positie waar u de lijn wilt uitvoeren. Alle volgordenummers worden bijgewerkt om de nieuwe volgorde weer te geven waarin de regels worden uitgevoerd.

1. Klik op **[!UICONTROL Save Changes]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

