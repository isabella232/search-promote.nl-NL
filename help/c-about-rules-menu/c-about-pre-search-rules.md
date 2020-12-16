---
description: Gebruik Regels voor voorzoeken om de binnenkomende query te analyseren en te bepalen welke presentatiesjabloon moet worden gebruikt. Regels voor voorzoeken worden voor elke query op volgorde uitgevoerd. U kunt slepen en neerzetten gebruiken om de volgorde van de regels te wijzigen. De werkelijke volgorde verandert pas wanneer u de volgorde opslaat.
seo-description: Gebruik Regels voor voorzoeken om de binnenkomende query te analyseren en te bepalen welke presentatiesjabloon moet worden gebruikt. Regels voor voorzoeken worden voor elke query op volgorde uitgevoerd. U kunt slepen en neerzetten gebruiken om de volgorde van de regels te wijzigen. De werkelijke volgorde verandert pas wanneer u de volgorde opslaat.
seo-title: Over regels voor vooraf zoeken
solution: Target
title: Over regels voor vooraf zoeken
topic: Rules,Site search and merchandising
uuid: e75f9d9e-e8ca-4184-bf79-b1fdadb5c0fe
translation-type: tm+mt
source-git-commit: d07cdc2c88f93eed4cecb0ee8818f7fdea06ee9d
workflow-type: tm+mt
source-wordcount: '1709'
ht-degree: 0%

---


# Info over Regels vóór zoeken{#about-pre-search-rules}

Gebruik Regels voor voorzoeken om de binnenkomende query te analyseren en te bepalen welke presentatiesjabloon moet worden gebruikt. Regels voor voorzoeken worden voor elke query op volgorde uitgevoerd. U kunt slepen en neerzetten gebruiken om de volgorde van de regels te wijzigen. De werkelijke volgorde verandert pas wanneer u de volgorde opslaat.

## Regels {#concept_5BF84BB6FACB4645BA9CB7496A01CD1F} vóór zoeken gebruiken

Regels vóór zoeken worden doorgaans gebruikt om te selecteren welke presentatiesjabloon de resultaten weergeeft op basis van de binnenkomende query. Geavanceerde functies kunnen worden gebruikt om de query te wijzigen die wordt gebruikt voor een zoekopdracht die wordt uitgevoerd voor een presentatiesjabloon. U kunt de waarde van queryparameters naar wens toevoegen, verwijderen of wijzigen. Voor elke inkomende vraag onderzoekt een pre-onderzoek-verwerkingsmodule de pre-onderzoeksregels om te bepalen als de vraag wordt gewijzigd en welke presentatiesjabloon wordt gebruikt. Elke regel voor voorzoeken bestaat uit twee hoofdelementen: het optreden van de regel en de facultatieve voorwaarden. U kunt een onbeperkt aantal regels en voorwaarden opgeven. De volgorde van deze regels is belangrijk, omdat de regel via regel wordt doorlopen. Wanneer de voorwaarden van een regel worden aangepast, worden alle bijbehorende acties uitgevoerd.

In de module van de Verwerking pre-Onderzoek alle bepaalde malplaatjes en hun bijbehorende genoemde onderzoeken worden geconcretiseerd waar elke onderzoek een lokale kopie van de parameters cgi wordt gegeven. Dientengevolge, kunt u een onderzoek aanpassen door, één van de cgi parameters toe te voegen te schrappen of te veranderen die onderzoeksgebruik zonder een andere genoemd onderzoek te veranderen het malplaatjegebruik of beïnvloedt om het even welke andere malplaatjes. Als u een presentatiesjabloon hebt waarin meerdere resultaten worden weergegeven, kunt u elke zoekopdracht dus afzonderlijk aanpassen. Als u veranderingen op de globale parameters van CGI wilt uitvoeren alvorens zij aan elke onderzoek naar elk malplaatje worden gekopieerd, gebruik de module van de Schoonmaak van de Vraag.

## Voorwaarden voor vooraf zoeken {#section_B5568ADEB28546A280720309498B045D}

Voorwaarden zijn optioneel. Als u ervoor kiest om acties voor elke query op te geven, worden de acties altijd uitgevoerd. Het wordt beschouwd als beste praktijken voor uw eerste regel om voor elke vraag in werking te stellen, waar het uw standaardpresentatiesjabloon selecteert. Op deze manier kunt u er zeker van zijn dat u een presentatiesjabloon voor een worst-case-scenario hebt geselecteerd om te gebruiken, ongeacht wat de binnenkomende query is. De voorwaarden kunnen op om het even welke CGI vraagparameter, koekje, of douanevariabele worden gebaseerd die een vorige regel of een systeemvariabele heeft geplaatst.

## Handelingen voor vooraf zoeken {#section_3B8E19D287554C1C969F5B8D81226981}

Alle handelingen binnen een regel voor voorzoeken met overeenkomende voorwaarden worden uitgevoerd. Handelingen bestaan doorgaans uit een bewerking, de gegevens waarop de bewerking moet worden uitgevoerd en de waarde die moet worden gebruikt. De eenvoudigste actie moet specificeren welk presentatiesjabloon moet worden gebruikt wanneer de vraag de voorwaarden van de Regel pre-Onderzoek aanpast. Stel vervolgens de doelsjabloon in op de naam van de presentatiesjabloon. U kunt complexere handelingen gebruiken om de zoekopdracht te wijzigen die voor een bepaalde sjabloon wordt gebruikt door een bewerking uit te voeren op de zoekparameter van een sjabloon. Wanneer u een bewerking uitvoert op de zoekparameter van een sjabloon, geeft u een presentatiesjabloon en een zoekopdracht op.

## Algemene regels {#section_885ECB9DBF0C4D539C14F82BCAA35B4E}

Wanneer u bewerkingen uitvoert op de zoekparameter van een sjabloon, bestaan er twee speciale waarden: *target en *primary voor de presentatiesjabloon en de genoemde zoekopdracht. Met deze waarden kunt u regels maken op basis van de primaire zoekopdracht van de huidige doelsjabloon. Deze constructies maken het mogelijk generieke regels te maken wanneer u zich geen zorgen hoeft te maken over wat de huidige doelsjabloon of primaire zoekopdracht wordt genoemd. Duidelijk, bepaalt een vorige regel van het pre-Onderzoek wat het huidige gerichte malplaatje is. Anders wordt een eerste presentatiesjabloon voor u geselecteerd, wat ongewenste resultaten oplevert.

## Voorbeelden {#section_EA153A151987454EA44A4A6862466DF6}

Plaats het standaardmalplaatje aan guided.tmpl, wanneer de gebruiker in een cgi parameter genoemd lang overgaat, die aan een bekende taal wordt geplaatst, gebruik het malplaatje van die taal.

```
    On condition: 
      Every Query 
    Perform the following actions: 
      Set targeted template to guided 
 
    On condition: 
      Query lang matches regular expression fr 
    Perform the following actions: 
      Set targeted template to guided_french 
 
    On condition: 
      Query lang matches regular expression de 
    Perform the following actions: 
      Set targeted template to guided_german
```

## Aanbevolen procedures {#section_31EBAE5E54174DEE8986CBB636746A98}

* De eerste regel selecteert een standaardmalplaatje voor elke vraag.
* De ontmijning van gegevens van de vraag wordt gedaan binnen vraag schoonmaakregels. U kunt ernaar verwijzen in de voorbezoekverwerking.
* Voeg om het even welke nieuwe douanevariabelen toe die u in Regels Pre-Search aan een pre-onderzoeksregel introduceerde die voor elke vraag alvorens een andere verwijzing van Regels Pre-Search hen in werking wordt gesteld.

## Nieuwe regel {#task_182B95918462490D8BDA7F16A81CAC11} toevoegen voor voorzoeken

U kunt [!DNL Pre-Search Rules] gebruiken om te selecteren welke presentatiesjabloon wordt gebruikt om de onderzoeksresultaten te tonen die op de inkomende vraag worden gebaseerd.

**Een nieuwe regel voor voorzoeken toevoegen**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Pre-Search Rules]**.
1. Klik op [!DNL Pre-Search Rules] op de pagina.**[!UICONTROL Add New Rule]**
1. Typ in het veld [!DNL Name] de naam van de nieuwe regel voor het opschonen van query.
1. Voor de [!DNL Add Pre-Search Rule] pagina, gebruik de drop-down lijsten en tekstgebieden om uw vraag te bouwen.

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
      <td colname="col2"> <p>Een HTTP-cookie. Naam en waarden van cookies moeten zijn gecodeerd als Uniform Resource Identifier. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Aangepaste variabele </p> </td> 
      <td colname="col2"> <p>Een door de gebruiker gedefinieerde variabele. U kunt een onbeperkt aantal door de gebruiker gedefinieerde variabelen toevoegen, verwijderen of instellen. </p> <p>U kunt om het even welke variabelen van verwijzingen voorzien die u in de module van de Schoonmaak van de Vraag binnen de Regels pre-Onderzoek bepaalde. </p> </td> 
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
        </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Facet </p> </td> 
      <td colname="col2"> <p>Speciale CGI-parameters in de algemene verzameling die aan een bepaald facet zijn gekoppeld. Alle CGI-parameters worden naar elke benoemde zoekopdracht in een sjabloon gekopieerd na Query Cleaning. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Query-parameter </p> </td> 
      <td colname="col2"> <p>CGI-parameter in de algemene verzameling. Deze parameters worden gekopieerd naar elke benoemde zoekopdracht in een sjabloon na Query Cleaning. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Zoekparameter van sjabloon </p> </td> 
      <td colname="col2"> <p>Een CGI-parameter die lokaal is aan een benoemde zoekopdracht die aan een presentatiesjabloon is gekoppeld. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Achterste parameter van sjabloon </p> </td> 
      <td colname="col2"> <p>Binnenkomende vraagparameters worden uiteindelijk vertaald in achterste parameters die worden gebruikt om het onderzoek uit te voeren. </p> <p>Zie <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> CGI-parameters voor achtergrondzoekopdrachten </a>. </p> <p>Achterste parameters worden niet weergegeven op navigatie-elementen. Dientengevolge, kunt u om het even welke extra parameters verbergen die u op een onderzoek van uw klanten wilt toepassen. De parameter is lokaal voor een specifieke zoekopdracht in een presentatiesjabloon. Acties met betrekking tot parameters van het achterste deel zijn te laat bindend; dat wil zeggen, ze worden toegepast vlak voordat de zoekopdracht wordt verzonden. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Doelsjabloon </p> </td> 
      <td colname="col2"> <p>Een speciaal geval van een systeem-bepaalde douanevariabele die niet kan worden geschrapt. Deze variabele bevat de huidige doelpresentatiesjabloon. U kunt deze variabele lezen of plaatsen door de douanevariabele "target_template"te specificeren. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Rang </p> </td> 
      <td colname="col2"> <p>Hier kunt u opgeven welke rangorderegel u wilt gebruiken in de zoekopdracht. Deze optie wordt alleen weergegeven wanneer u classificatievelden en waarderingsregels hebt gedefinieerd. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Winkel </p> </td> 
      <td colname="col2"> <p>Het zoekprogramma detecteert automatisch in welke opslagruimte de klant zich bevindt op basis van de hostnaam of de query-parameter <span class="codeph"> gs_store </span>, waarbij de laatste prioriteit heeft. U kunt voorwaarden buiten de winkel maken. Alleen bij query-reiniging kunt u ook een handeling gebruiken om de huidige winkel te overschrijven. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Laatste regel </p> </td> 
      <td colname="col2"> <p>Als deze optie is ingeschakeld, voert de verwerkingsmodule van de voorzoekopdracht geen aanvullende regels uit na de handeling van de overeenkomende regel. Deze actie is nuttig voor wanneer u acties hebt geplaatst die een recentere regel veroorzaken om aan te passen maar u wilt niet de recentere regel in werking stellen. </p> </td> 
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

## Een regel voor vooraf zoeken bewerken {#task_25F77050C5DA42B29DFD1C9718FB8C64}

U kunt bestaande regels voor vooraf zoeken bewerken die u hebt toegevoegd aan de pagina [!DNL Pre-Search Rules].

**Een regel voor vooraf zoeken bewerken**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Pre-Search Rules]**.
1. Op [!DNL Pre-Search Rules] pagina, onder **[!UICONTROL Actions]** kolom van de lijst, klik **[!UICONTROL Edit]** voor de bijbehorende regel die u wilt uitgeven.
1. Voor de [!DNL Edit Pre-Search Rule] pagina, gebruik de drop-down lijsten en tekstgebieden om uw vraag te bouwen.

   Zie de lijst van opties onder [Toevoegend een nieuwe pre-onderzoeksregel](../c-about-rules-menu/c-about-pre-search-rules.md#task_182B95918462490D8BDA7F16A81CAC11).
1. Klik op **[!UICONTROL Save Changes]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een regel {#task_128B6A79CA6C451C991AEDAD58F51743} voor voorzoeken verwijderen

U kunt regels voor voorzoeken verwijderen die u niet meer nodig hebt of gebruikt.

Wanneer u een regel schrapt, wordt de orde dat de resterende regels in werking worden gesteld automatisch aangepast aan rekening voor de schrapping.

**Een regel voor vooraf zoeken verwijderen**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Pre-Search Rules]**.
1. Op [!DNL Pre-Search Rules] pagina, onder **[!UICONTROL Actions]** kolom van de lijst, klik **[!UICONTROL Delete]** voor de bijbehorende regel die u wilt schrappen.
1. Klik in het dialoogvenster [!DNL Confirmation] op **[!UICONTROL OK]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## De volgorde wijzigen waarin regels voor voorzoeken worden uitgevoerd {#task_C18817276A3C459089C97448076365D1}

U kunt de regels voor voorzoeken opnieuw ordenen om de volgorde te wijzigen waarin ze op presentatiesjablonen worden uitgevoerd.

Regels voor voorzoeken worden uitgevoerd in de volgorde waarin ze zijn gedefinieerd. Hoger het de ordeaantal van een regel, later het in het proces loopt, die vroegere regels beweegt. U wijzigt de volgorde van de regels door een nieuw nummer in te voeren in de kolom Volgorde van de tabel op de pagina [!DNL Pre-Search Rules]. U kunt slepen-en-neerzetten op regels ook gebruiken om hun runtime orde te veranderen.

**De volgorde wijzigen waarin regels voor voorzoeken worden uitgevoerd**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Pre-Search Rules]**.
1. Voer op de pagina [!DNL Pre-Search Rules] een van de volgende handelingen uit:

   * Klik op de kolomkop **[!UICONTROL Order]** om de regels in oplopende of aflopende volgorde te sorteren.
   * Typ in de kolom **[!UICONTROL Order]** in het tekstveld links van de naam van een regel die aan het zoeken is voorafgegaan het volgordenummer dat de regel moet worden uitgevoerd.
   * Sleep een tabelrij naar de positie waar u de lijn wilt uitvoeren. Alle volgordenummers worden bijgewerkt om de nieuwe volgorde weer te geven waarin de regels worden uitgevoerd.

1. Klik op **[!UICONTROL Save Changes]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

