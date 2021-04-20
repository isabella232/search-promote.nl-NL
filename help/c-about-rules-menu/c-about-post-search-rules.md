---
description: U kunt Regels na het Onderzoek gebruiken om de resultaten van een onderzoek te onderzoeken en te bepalen hoe het onderzoek de getoonde inhoud beïnvloedt.
solution: Target
title: Over regels voor achteraf zoeken
topic: Rules,Site search and merchandising
uuid: 312d1e4a-f5b6-4629-8645-17e6f6c09fc4
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '2102'
ht-degree: 0%

---


# Info over Regels voor na het zoeken{#about-post-search-rules}

U kunt Regels na het Onderzoek gebruiken om de resultaten van een onderzoek te onderzoeken en te bepalen hoe het onderzoek de getoonde inhoud beïnvloedt.

## Nazoekregels gebruiken {#concept_AF6ADFCC0ADF4A788003964939917FDE}

Als een zoekopdracht geen resultaten oplevert, kan met een regel Na zoeken naar een vergelijkbaar item worden gezocht. Of er kan een webpagina worden weergegeven waarin andere items worden aanbevolen aan klanten die naar het item zoeken dat niet is gevonden.

Elke regel na het zoeken bestaat uit twee hoofdelementen: het optreden van de regel en de facultatieve voorwaarden ervan. U kunt een onbeperkt aantal regels en voorwaarden opgeven. De orde van deze regels is belangrijk omdat de regel wordt geplaatst door regel-voor-regel. Wanneer de voorwaarden van een regel overeenkomen, worden alle bijbehorende acties uitgevoerd.

U kunt de set zoekresultaten verfijnen tot maximaal drie zoekronden. Hierna wordt alles gebruikt wat momenteel beschikbaar is. Deze grens verhindert oneindige lijnen en zorgt ervoor dat de klant een efficiënte reactie ontvangt. Hoe vaker u een zoekopdracht opnieuw uitvoert, hoe langer het duurt om de zoekresultaten te retourneren. Als geen van de overeenkomende regels een van de zoekopdrachten voor de momenteel gebruikte presentatiesjabloon wijzigt of van de sjabloon overschakelt, wordt de set met zoekresultaten beschouwd als voltooid en wordt de zoekopdracht beëindigd.

De verwerking na het onderzoek bouwt op de vroegere het Schoonmaken van de Vraag van de verwerkingsmodules en de verwerking Pre-Search voort. Daarom zijn om het even welke douanevariabelen die in die modules worden geplaatst beschikbaar voor gebruik in de na onderzoek verwerkingsregels. Op dezelfde manier heeft de voorbezoekverwerking alle sjablonen geïnstantieerd waarin elke benoemde zoekopdracht die aan de presentatiesjabloon is gekoppeld, een eigen lokale kopie van de CGI-parameters heeft. U kunt elke zoekopdracht afzonderlijk aanpassen.

Zie [Informatie over Regels voor het opschonen van query](../c-about-rules-menu/c-about-query-cleaning-rules.md#concept_17F3CDDC3C8A4128AF092A82B777B86C).

Zie [Informatie over regels voor voorzoeken](../c-about-rules-menu/c-about-pre-search-rules.md#concept_5BF84BB6FACB4645BA9CB7496A01CD1F).

## Informatie over voorwaarden voor regels na zoeken {#section_C43EB77CC0AC43B8B9D38569264BF1B5}

Voorwaarden zijn optioneel. Als u opgeeft dat acties voor elke query worden opgegeven, worden de acties altijd uitgevoerd. U kunt voorwaarden op om het even welke CGI vraagparameter, koekje, onderzoeksresultaat, of douanevariabele baseren die een vorige regel heeft geplaatst. U kunt de sjabloon ook baseren op een systeemvoorwaarde, zoals de geselecteerde sjabloon of de laatste zoekopdracht. Wanneer u een voorwaarde bouwt op de resultaten van een onderzoek of een parameter CGI, specificeert u het malplaatje en de naam van het onderzoek.

## Handelingen voor regels na zoeken {#section_0E15FE683A894ECAAA386267EEC7F7C5}

Alle acties in een regel voor na het zoeken die aan de voorwaarden voldoen, worden uitgevoerd. Handelingen bestaan doorgaans uit een bewerking, de gegevens waarop de bewerking moet worden uitgevoerd en de waarde die moet worden gebruikt. De eenvoudigste actie is om te schakelen welk malplaatje van de Presentatie aan gebruik gebaseerd op de voorwaarden van de Regel van de Post-Onderzoek wordt gebaseerd. U kunt geavanceerdere handelingen gebruiken om de parameters te wijzigen voor een zoekopdracht die ertoe leidt dat de zoekopdracht opnieuw wordt uitgevoerd. Wanneer u een bewerking uitvoert op de zoekparameter van een sjabloon, geeft u een presentatiesjabloon en een zoekopdracht op.

## Algemene regels {#section_AEE923988CC748FF9DEF2233FBF333B5}

Bij het uitvoeren van bewerkingen op de zoekparameter van een sjabloon bestaan er twee speciale waarden: *target en *primary voor respectievelijk de presentatiesjabloon en de benoemde zoekopdracht. Gebruik deze waarden om regels op te bouwen die op het huidige gerichte primaire onderzoek van het malplaatje worden gebaseerd. Met deze constructies kunt u algemene regels maken waar u zich geen zorgen hoeft te maken over de naam van de huidige doelsjabloon of primaire zoekopdracht. Als deze pas de eerste door de post-onderzoeksverwerking is, is het gerichte malplaatje wat voorbezoekverwerking het aan plaatst.

## Omleiding {#section_E5669A2F13C240F2968E31C75591CD6A}

Met Direct Hits en omleiding binnen Query Cleaning kunt u een URL doorsturen op basis van de binnenkomende zoektermen. Omleiding binnen regels voor na het zoeken breidt dit idee uit, behalve dat het u laat controleren hoeveel resultaten die het onderzoek terugkwam alvorens te beslissen of u een omleiding wilt plaatsvinden. Met Regels na het Onderzoek, kunt u aan een URL opnieuw richten, waar u douanevariabelen of vraagparameters kunt substitueren. Of u kunt een veld omleiden binnen het eerste resultaat. Wanneer u aan het gebied van een resultaat opnieuw richt, bepaalt u het gebied in het malplaatje van het Vervoer, en het moet een geldige, expliciete URL bevatten, anders wordt omleiding overgeslagen.

Wanneer u het omleidingsmechanisme binnen Regels Post-Onderzoek gebruikt, kunt u ontdekken wanneer een onderzoek één enkel resultaat terugkeert. In plaats van een dergelijk resultaat te retourneren, kunt u omleiden naar de webpagina die aan het resultaat is gekoppeld.

Zie het omleidingsvoorbeeld hieronder voor een voorbeeld om omleidingen met Regels te gebruiken Post-Search.

## Laatste regel {#section_FC1E0050C9324278B171038E98F6C335}

Wanneer aan de voorwaarden voor een regel wordt voldaan die de optie **[!UICONTROL Last Rule]** geplaatst heeft, voert de post verwerkingsmodule geen extra regels na de actie van de passende regel uit. Deze situatie is nuttig wanneer u acties hebt geplaatst die een recentere regel veroorzaken om aan te passen maar u wilt de verwerking ophouden. En, voor die recentere regel om na de volgende ronde van het zoeken potentieel aan te passen.

## Voorbeelden {#section_DDB98383690941F9B44AD00FBA55BB56}

In het volgende voorbeeld gaat u ervan uit dat u twee presentatiesjablonen hebt. Eén sjabloon wordt gebruikt om veel zoekresultaten weer te geven en de andere sjabloon wordt gebruikt om één resultaat weer te geven en een extra zoekopdracht naar accessoires voor de hoofdzoekopdracht. U wilt nagaan wanneer u één resultaat hebt en overschakelen op uw andere presentatiesjabloon. Voor deze taak kunt u de volgende regels gebruiken:

```
On condition: 
  targeted template is default 
  targeted template primary results equal 1 
  not last search 
Perform the following actions: 
  Set targeted template to product_spotlight
```

MegaElectronic is een grote elektronicawinkel. Na het analyseren van hun onderzoeksgegevens, merkt MegaElectronic op dat veel van hun klanten een productonderzoek gebruikend het de deelaantal van een product uitvoeren. In dergelijke gevallen wil MegaElectronic doorverwijzen naar de webpagina die aan het product is gekoppeld, als de klant er direct naar heeft gezocht en er slechts één product is gevonden.

U bereikt dit resultaat door één regel met drie voorwaarden te gebruiken. De eerste voorwaarde controleert dat de teruggekeerde onderzoek slechts één enkel resultaat heeft. De tweede voorwaarde zorgt ervoor dat de vraagtermijn het formaat van het deelaantal van MegaElectronic voor de resultaten aanpast die zij redirect willen veroorzaken. De derde voorwaarde zorgt ervoor dat de klant geen facetten gebruikte om tot één resultaat neer te boren, aangezien het deelaantal een gedeeltelijk deelaantal zou kunnen zijn en meer dan één resultaat zou kunnen terugkeren. De handeling wordt omgeleid naar een veld in het resultaat.

```
On condition: 
  targeted template's primary results equal 1 
  query q matches regular expression ^\D\D\D-\d+ 
  no facet selected ^\D\D\D-\d+ 
Perform the following actions: 
  redirect to result field "loc" in template *targeted for search *primary
```

## Aanbevolen procedures {#section_1BF7DE1BD5664B3BAEC26AA829FDB0BA}

* Om het even welke reeks regels die een nieuwe ronde van het zoeken teweegbrengen zou altijd een voorwaardelijke clausule moeten hebben om te controleren dat dit niet de laatste pas door de module is. Als u het maximumaantal zoekopdrachten al hebt uitgevoerd, kunt u geen zoekopdrachten opnieuw uitvoeren.
* Als u op de laatste pas door de module bent en de resultaten nog slecht zijn, kunt u op een malplaatje &quot;geen resultaten&quot;schakelen.
* U moet het wijzigen van een presentatiesjabloon baseren op het resultaat van een zoekopdracht die mogelijk andere parameters heeft. Als u een malplaatje wilt selecteren dat slechts op de inkomende vraag gebaseerd is, is een pre-onderzoeksregel efficiënter.
* Het ontdoen van gegevens van de vraag wordt gedaan in de module van de Schoonmaak van de Vraag. U kunt naar de aangepaste variabelen verwijzen tijdens de nazoekbewerking.
* Wanneer u een omleiding uitvoert, moet u altijd controleren of de klant geen facetten heeft geselecteerd. De reden is dat het lastig is wanneer een klant naar een facet gaat en plotseling wordt verwijderd van de zoekresultaten. De klant kan de selectie van het facet opheffen wanneer hij of zij ziet dat het ene resultaat niet gewenst is.

## Nieuwe regel voor na het zoeken toevoegen {#task_52F6F9AAD65B45B5ACA1FF245DFFADD9}

U kunt [!DNL Post-Search Rules] gebruiken om te selecteren welke presentatiesjabloon wordt gebruikt om de onderzoeksresultaten te tonen die op de inkomende vraag worden gebaseerd.

**Een nieuwe regel voor na het zoeken toevoegen**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Post-Search Rules]**.
1. Klik op [!DNL Post-Search Rules] op de pagina.**[!UICONTROL Add New Rule]**
1. Typ in het veld [!DNL Name] de naam van de nieuwe regel voor het opschonen van query.
1. Voor de [!DNL Add Post-Search Rule] pagina, gebruik de drop-down lijsten en tekstgebieden om uw vraag te bouwen.

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
      <td colname="col2"> <p>Een HTTP-cookie. Cookie-namen en -waarden moeten zijn gecodeerd als Uniform Resource Identifier. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Aangepaste variabele </p> </td> 
      <td colname="col2"> <p>Een door de gebruiker gedefinieerde variabele. U kunt een onbeperkt aantal aangepaste variabelen toevoegen, verwijderen of instellen. </p> <p>U kunt om het even welke douanevariabelen van verwijzingen voorzien die u in het Schoonmaken van de Vraag en in modules van Regels pre-Onderzoek, binnen Regels Post-Search bepaalde. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Systeemvariabele </p> </td> 
      <td colname="col2"> <p>Alleen-lezen variabelen ingesteld door het interne systeem dat u kunt controleren. De volgende systeemvariabelen worden ondersteund: </p> <p> 
        <ul id="ul_BC17F1637F27424CA4E8F530C28A3245"> 
          <li id="li_C7DF96EFD7AA4A449D00F7EACCAA0EB1"> <span class="uicontrol"> hostnaam  </span> <p>De naam van de serverhost. </p> </li> 
          <li id="li_F85AB1D2B9374A859657D12B8ED6674B"> <span class="uicontrol"> uri  </span> <p>De aangevraagde Uniform Resource Identifier zonder de queryreeks. </p> </li> 
          <li id="li_440149C9EC6E4805B77BBC97BE41542A"> <span class="uicontrol"> args  </span> <p>De volledige queryreeks. </p> </li> 
          <li id="li_F583FC4B0E404858BB3522B33A6F7A0A"> <span class="uicontrol"> milieu  </span> <p>"Stage" of "live", afhankelijk van het feit of de binnenkomende query naar uw gefaseerde omgeving of uw live omgeving is verzonden. </p> </li> 
          <li id="li_15902AA49B144D42A5E95D7E8B0FB1E1"> <span class="uicontrol"> referentie  </span> <p>Het Uniform Resource Locator waar de klant vandaan komt. </p> </li> 
        </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Systeemvariabele </p> </td> 
      <td colname="col2"> <p>Alleen-lezen variabelen die u in voorwaarden kunt gebruiken om de huidige status te bepalen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Zoekfacet van sjabloon </p> </td> 
      <td colname="col2"> <p>Een facet dat lokaal is voor een benoemde zoekopdracht die aan een presentatiesjabloon is gekoppeld. Een facet is in wezen speciale CGI-parameters die worden gebruikt om aan te geven welke waarde binnen een facet een klant heeft geselecteerd. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Zoekparameter van sjabloon </p> </td> 
      <td colname="col2"> <p>Een CGI-parameter die lokaal is aan een benoemde zoekopdracht die aan een presentatiesjabloon is gekoppeld. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Achterste parameter van sjabloon </p> </td> 
      <td colname="col2"> <p>Binnenkomende vraagparameters worden uiteindelijk vertaald in achterste parameters die worden gebruikt om het onderzoek uit te voeren. </p> <p>Zie <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> CGI-parameters voor achtergrondzoekopdrachten </a>. </p> <p>Achterste parameters worden niet weergegeven op navigatie-elementen. Dientengevolge, kunt u om het even welke extra parameters verbergen die u op een onderzoek van uw klanten wilt toepassen. </p> <p>De parameter is lokaal voor een specifieke zoekopdracht in een presentatiesjabloon. Acties betreffende parameters van het achterste deel zijn te laat bindend; dat wil zeggen, ze worden toegepast vlak voordat de zoekopdracht wordt verzonden. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Doelsjabloon </p> </td> 
      <td colname="col2"> <p>Een speciaal geval van een systeem-bepaalde douanevariabele die niet kan worden geschrapt. Deze variabele bevat de huidige doelpresentatiesjabloon. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Rang </p> </td> 
      <td colname="col2"> <p>Hier kunt u opgeven welke rangorderegel u wilt gebruiken in de zoekopdracht. Deze optie wordt alleen weergegeven wanneer u classificatievelden en waarderingsregels hebt gedefinieerd. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Laatste regel </p> </td> 
      <td colname="col2"> <p>Als deze optie is ingeschakeld, voert de verwerkingsmodule na het zoeken geen aanvullende regels uit na de actie van de overeenkomende regel. Deze actie is nuttig voor wanneer u acties hebt geplaatst die een recentere regel veroorzaken om aan te passen maar u wilt niet de recentere regel in werking stellen. </p> </td> 
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

## Een regel voor na het zoeken bewerken {#task_ECB00334C0A74C87AF857DB3EB372119}

U kunt bestaande regels voor na het zoeken bewerken die u hebt toegevoegd aan de pagina [!DNL Post-Search Rules].

**Een regel voor na het zoeken bewerken**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Pre-Search Rules]**.
1. Op [!DNL Post-Search Rules] pagina, onder **[!UICONTROL Actions]** kolom van de lijst, klik **[!UICONTROL Edit]** voor de bijbehorende regel die u wilt uitgeven.
1. Voor de [!DNL Edit Post-Search Rule] pagina, gebruik de drop-down lijsten en tekstgebieden om uw vraag te bouwen.

   Zie de optietabel onder [Een nieuwe regel voor na het zoeken toevoegen](../c-about-rules-menu/c-about-post-search-rules.md#task_52F6F9AAD65B45B5ACA1FF245DFFADD9).
1. Klik op **[!UICONTROL Save Changes]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een regel {#task_0F4653AB20D54B769A4FA8D1491AB4CF} voor na het zoeken verwijderen

U kunt regels voor na het zoeken verwijderen die u niet meer nodig hebt of gebruikt.

Wanneer u een regel schrapt, wordt de orde dat de resterende regels in werking worden gesteld automatisch aangepast aan rekening voor de schrapping.

**Een regel na het zoeken verwijderen**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Post-Search Rules]**.
1. Op [!DNL Post-Search Rules] pagina, onder **[!UICONTROL Actions]** kolom van de lijst, klik **[!UICONTROL Delete]** voor de bijbehorende regel die u wilt schrappen.
1. Klik in het dialoogvenster [!DNL Confirmation] op **[!UICONTROL OK]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## De volgorde wijzigen waarin regels voor na het zoeken worden uitgevoerd {#task_40542FCD32234BBF881A81BF5477F78F}

U kunt regels voor na het zoeken opnieuw ordenen om de volgorde te wijzigen waarin ze worden uitgevoerd op presentatiesjablonen.

Nazoekregels worden uitgevoerd in de volgorde waarin ze zijn gedefinieerd. Hoger het de ordeaantal van een regel, later het in het proces loopt, die vroegere regels beweegt. U wijzigt de volgorde van de regels door een nieuw nummer in te voeren in de kolom Volgorde van de tabel op de pagina [!DNL Post-Search Rules]. U kunt slepen-en-neerzetten op regels ook gebruiken om hun runtime orde te veranderen.

**De volgorde wijzigen waarin regels voor na het zoeken worden uitgevoerd**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Post-Search Rules]**.
1. Voer op de pagina [!DNL Post-Search Rules] een van de volgende handelingen uit:

   * Klik op de kolomkop **[!UICONTROL Order]** om de regels in oplopende of aflopende volgorde te sorteren.
   * Typ in de kolom [!DNL Order] in het tekstveld links van de naam van een regel die aan het zoeken is voorafgegaan het volgordenummer dat de regel moet worden uitgevoerd.
   * Sleep een tabelrij naar de positie waar u de lijn wilt uitvoeren. Alle volgordenummers worden bijgewerkt om de nieuwe volgorde weer te geven waarin de regels worden uitgevoerd.

1. Klik op **[!UICONTROL Save Changes]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).
