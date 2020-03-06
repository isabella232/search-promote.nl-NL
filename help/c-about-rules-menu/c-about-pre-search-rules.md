---
description: De Regels van het gebruik pre-Onderzoek om de inkomende vraag te analyseren en te bepalen welk presentatiemalplaatje aan gebruik. De Regels van het pre-Onderzoek worden uitgevoerd opeenvolging voor elke vraag. Om de orde van uw regels te veranderen kunt u belemmering-en-daling gebruiken. De daadwerkelijke orde verandert niet tot u bewaart het.
seo-description: De Regels van het gebruik pre-Onderzoek om de inkomende vraag te analyseren en te bepalen welk presentatiemalplaatje aan gebruik. De Regels van het pre-Onderzoek worden uitgevoerd opeenvolging voor elke vraag. Om de orde van uw regels te veranderen kunt u belemmering-en-daling gebruiken. De daadwerkelijke orde verandert niet tot u bewaart het.
seo-title: Informatie over regels voor voorzoeken
solution: Target
title: Informatie over regels voor voorzoeken
topic: Rules,Site search and merchandising
uuid: e75f9d9e-e8ca-4184-bf79-b1fdadb5c0fe
translation-type: tm+mt
source-git-commit: d07cdc2c88f93eed4cecb0ee8818f7fdea06ee9d

---


# Informatie over regels voor voorzoeken{#about-pre-search-rules}

De Regels van het gebruik pre-Onderzoek om de inkomende vraag te analyseren en te bepalen welk presentatiemalplaatje aan gebruik. De Regels van het pre-Onderzoek worden uitgevoerd opeenvolging voor elke vraag. Om de orde van uw regels te veranderen kunt u belemmering-en-daling gebruiken. De daadwerkelijke orde verandert niet tot u bewaart het.

## Voorspelregels gebruiken {#concept_5BF84BB6FACB4645BA9CB7496A01CD1F}

De Regels van het pre-Onderzoek worden typisch gebruikt om te selecteren welke presentatiemalplaatvertoningen de resultaten die op de inkomende vraag worden gebaseerd. De geavanceerdere eigenschappen kunnen worden gebruikt om de vraag te veranderen die voor een onderzoek wordt gebruikt dat voor een presentatiemalplaatje wordt gedaan. U kunt, de waarde van vraagparameters toevoegen schrappen of veranderen zoals nodig. Voor elke inkomende vraag onderzoekt een pre-onderzoek-verwerkende module de pre-onderzoeksregels om te bepalen als de vraag wordt gewijzigd en welk presentatiemalplaatje wordt gebruikt. Elke regel voor voorzoeken bestaat uit twee hoofdelementen: het optreden van de regel en de facultatieve voorwaarden. U kunt een onbeperkt aantal regels en voorwaarden specificeren. De orde van deze regels is belangrijk, omdat de regelreeks door regel door van een lus wordt voorzien. Wanneer de voorwaarden van een regel worden aangepast, worden alle bijbehorende acties uitgevoerd.

In de module van de Verwerking van het pre-Onderzoek worden alle bepaalde malplaatjes en hun bijbehorende genoemde onderzoeken geconcretiseerd waar elk onderzoek een lokaal exemplaar van de cgi parameters wordt gegeven. Dientengevolge, kunt u een onderzoek aanpassen door, één van de cgi parameters toe te voegen te schrappen of te veranderen die onderzoek gebruikt zonder een ander genoemd onderzoek te veranderen het malplaatjegebruik of beïnvloedt om het even welke andere malplaatjes. Dientengevolge, als u een presentatiemalplaatje hebt dat meer dan één resultaatreeks toont, kunt u elk onderzoek aanpassen individueel. Als u veranderingen op de globale parameters van CGI wilt uitvoeren alvorens zij aan elk onderzoek naar elk malplaatje worden gekopieerd, gebruik de het Schoonmaken van de Vraag module.

## Voorwaarden voor voorzoekregels {#section_B5568ADEB28546A280720309498B045D}

De voorwaarden zijn facultatief. Als u verkiest om acties te hebben voor elke vraag worden gespecificeerd dan de acties altijd genomen die. Het wordt beschouwd als beste praktijken voor uw eerste regel om voor elke vraag te lopen, waar het uw standaardpresentatiemalplaatje selecteert. Deze manier u kan worden verzekerd dat, ongeacht wat de inkomende vraag is, u een worst-case malplaatje van de scenariopresentatie aan gebruik hebt geselecteerd. De voorwaarden kunnen op om het even welke de vraagparameter van CGI, koekje, of douanevariabele worden gebaseerd die een vorige regel of een systeemvariabele heeft geplaatst.

## Vooraf doorzogen-regelacties {#section_3B8E19D287554C1C969F5B8D81226981}

Alle acties binnen een Regel van het pre-Onderzoek die passende voorwaarden heeft worden uitgeoefend. De acties bestaan typisch uit een verrichting, de gegevens om de handeling uit te voeren, en de waarde aan gebruik. De eenvoudigste actie moet specificeren welk presentatiemalplaatje aan gebruik wanneer de vraag de voorwaarden van de Regel van het pre-Onderzoek aanpast. Dan plaats het gerichte malplaatje aan de naam van het presentatiemalplaatje. De ingewikkeldere acties kunnen worden gebruikt om het onderzoek te veranderen dat voor een bepaalde malplaatje door een verrichting op de het onderzoeksparameter van een malplaatje uit te voeren wordt gebruikt. Wanneer het uitvoeren van een verrichting op de het onderzoeksparameter van een malplaatje, specificeert u een presentatiemalplaatje en een onderzoek.

## Algemene regels {#section_885ECB9DBF0C4D539C14F82BCAA35B4E}

Wanneer het uitvoeren van verrichtingen op de onderzoeksparameter van een malplaatje, bestaan twee speciale waarden: *target en *primary voor het presentatiemalplaatje en het genoemde onderzoek respectievelijk. Met deze waarden, kunt u regels bouwen die op het huidige gerichte primaire onderzoek van het malplaatje worden gebaseerd. Deze concepten staan voor de bouw van generische regels toe waar u niet zich over wat het huidige gerichte malplaatje of het primaire onderzoek moet ongerust maken worden geroepen. Duidelijk, bepaalt een vorige Regel van het pre-Onderzoek wat het huidige gerichte malplaatje is. Anders, wordt een aanvankelijke presentatiemalplaatje geselecteerd voor u, die ongewenste resultaten veroorzaakt.

## Voorbeelden {#section_EA153A151987454EA44A4A6862466DF6}

Plaats het standaardmalplaatje aan geleide.tmpl, wanneer de gebruiker in een cgi parameter genoemd lang overgaat, die aan een bekende taal wordt geplaatst, gebruik het malplaatje van die taal.

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

## Beste praktijken {#section_31EBAE5E54174DEE8986CBB636746A98}

* De eerste regel selecteert een standaardmalplaatje voor elke vraag.
* De mijning van gegevens van de vraag wordt gedaan binnen vraag schoonmaakregels. U kunt hen in de pre-onderzoeksverwerking van verwijzingen voorzien.
* Voeg om het even welke nieuwe douanevariabelen toe die u in de Regels van het pre-Onderzoek aan een pre-onderzoeksregel introduceerde die voor elke vraag vóór een andere verwijzing van de Regels van het pre-Onderzoek hen in werking wordt gesteld.

## Het toevoegen van een nieuwe pre-onderzoeksregel {#task_182B95918462490D8BDA7F16A81CAC11}

U kunt gebruiken [!DNL Pre-Search Rules] om te selecteren welk presentatiemalplaatje wordt gebruikt om de onderzoeksresultaten te tonen die op de inkomende vraag worden gebaseerd.

**Om een nieuwe voorzoekregel toe te voegen**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Pre-Search Rules]**.
1. Voor de [!DNL Pre-Search Rules] pagina, klik **[!UICONTROL Add New Rule]**.
1. Op het [!DNL Name] gebied, typ de naam van de nieuwe vraag schoonmaakregel.
1. Voor de [!DNL Add Pre-Search Rule] pagina, gebruik de drop-down lijsten en tekstgebieden om uw vraag uit te bouwen.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Optie </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Cookie </p> </td> 
      <td colname="col2"> <p>Een HTTP koekje. De naam en de waarden van koekjes moeten het Uniforme Herkenningsteken van het Middel zijn gecodeerd. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Aangepaste variabele </p> </td> 
      <td colname="col2"> <p>Een user-defined variabele. Voeg, schrap, of plaats een onbeperkte hoeveelheid user-defined variabelen toe. </p> <p>U kunt om het even welke variabelen van verwijzingen voorzien die u in de de Schoonmaakmodule van de Vraag binnen de Regels van het pre-Onderzoek bepaalde. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Systeemvariabele </p> </td> 
      <td colname="col2"> <p>Alleen-lezen variabelen die zijn ingesteld op het interne systeem dat u kunt controleren. De volgende systeemvariabelen worden ondersteund: </p> <p> 
        <ul id="ul_BC17F1637F27424CA4E8F530C28A3245"> 
          <li id="li_C7DF96EFD7AA4A449D00F7EACCAA0EB1"> <span class="uicontrol"> hostnaam </span> <p>De naam van de servergastheer. </p> </li> 
          <li id="li_F85AB1D2B9374A859657D12B8ED6674B"> <span class="uicontrol"> buik </span> <p>De gevraagde uri zonder het vraagkoord. </p> </li> 
          <li id="li_440149C9EC6E4805B77BBC97BE41542A"> <span class="uicontrol"> arcering </span> <p>Het volledige vraagkoord. </p> </li> 
          <li id="li_F583FC4B0E404858BB3522B33A6F7A0A"> <span class="uicontrol"> milieu </span> <p>"Stadium"of "leef"afhankelijk van of de inkomende vraag naar uw gefaseerde of levende milieu werd verzonden. </p> </li> 
          <li id="li_15902AA49B144D42A5E95D7E8B0FB1E1"> <span class="uicontrol"> verwijzende </span> <p>URL die de klant kwam van. </p> </li> 
        </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Gezicht </p> </td> 
      <td colname="col2"> <p>Speciale parameters van CGI in de globale inzameling die met een bepaald facet worden geassocieerd. Alle parameters van CGI worden gekopieerd aan elk genoemd onderzoek binnen een malplaatje na het Schonen van de Vraag. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Query-parameter </p> </td> 
      <td colname="col2"> <p>CGI-parameter in de wereldwijde verzameling. Deze parameters worden gekopieerd aan elk genoemd onderzoek binnen een malplaatje na het Schonen van de Vraag. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Zoekparameter van sjabloon </p> </td> 
      <td colname="col2"> <p>Een parameter van CGI die aan een genoemd onderzoek verbonden aan een presentatiemalplaatje lokaal is. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Backend Parameter Sjabloon </p> </td> 
      <td colname="col2"> <p>De inkomende vraagparameters worden uiteindelijk vertaald in achterste deelparameters die worden gebruikt om het onderzoek uit te voeren. </p> <p>Zie <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> Achterste onderzoekCGI parameters </a>. </p> <p>De parameters van de steun verschijnen niet op navigatie elementen. Dientengevolge, kunt u om het even welke extra parameters verbergen die u op een onderzoek van uw klanten wilt toepassen. De parameter is lokaal aan een specifiek onderzoek binnen een presentatiemalplaatje. De acties op achterste deelparameters zijn laat-bindend; dat wil zeggen, ze worden toegepast vlak voordat de zoekopdracht wordt verzonden. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Gerichte template </p> </td> 
      <td colname="col2"> <p>Een speciaal geval van een systeem-bepaalde douanevariabele die niet kan worden geschrapt. Deze variabele bevat het huidige gerichte presentatiemalplaatje. U kunt deze variabele lezen of plaatsen door de douanevariabele "target_template"te specificeren. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Rank </p> </td> 
      <td colname="col2"> <p>Laat u specificeren welke rangschikkende regel in het onderzoek te gebruiken. Deze optie verschijnt slechts wanneer u het rangschikken gebieden en het rangschikken regels hebt bepaald. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Winkel </p> </td> 
      <td colname="col2"> <p>De onderzoeksmotor ontdekt automatisch welke opslag de klant binnen gebaseerd op de gastheernaam of de <span class="codeph"> gs_store </span> vraagparameter is, met de laatstgenoemde die belangrijkheid hebben is. U kunt voorwaarden van de opslag tot stand brengen. In vraag het reinigen slechts, kunt u een actie ook gebruiken om de huidige opslag over-ride te nemen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Laatste regel </p> </td> 
      <td colname="col2"> <p>Wanneer gecontroleerd, voert de presearch verwerkingsmodule geen extra regels na de actie van de aanpassingsregel uit. Deze actie is nuttig voor wanneer u acties hebt geplaatst die een recentere regel veroorzaken om aan te passen maar u wilt niet de recentere regel lopen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Opschorten </p> </td> 
      <td colname="col2"> <p>Zet het lopen van de regel uit maar schrapt niet de regel. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Klik op **[!UICONTROL Add]**.
1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een voorzoekregel bewerken {#task_25F77050C5DA42B29DFD1C9718FB8C64}

U kunt bestaande regels bewerken die u aan de [!DNL Pre-Search Rules] pagina hebt toegevoegd.

**Een regel voor voorzoeken bewerken**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Pre-Search Rules]**.
1. Voor de [!DNL Pre-Search Rules] pagina, onder de **[!UICONTROL Actions]** kolom van de lijst, klik **[!UICONTROL Edit]** voor de bijbehorende regel die u wilt uitgeven.
1. Voor de [!DNL Edit Pre-Search Rule] pagina, gebruik de drop-down lijsten en tekstgebieden om uw vraag uit te bouwen.

   Zie de lijst van opties onder het [Toevoegen van een nieuwe pre-onderzoeksregel](../c-about-rules-menu/c-about-pre-search-rules.md#task_182B95918462490D8BDA7F16A81CAC11).
1. Klik op **[!UICONTROL Save Changes]**.
1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een voorzoekregel verwijderen {#task_128B6A79CA6C451C991AEDAD58F51743}

U kunt pre-onderzoeksregels schrappen die u niet meer nodig hebt of gebruikt.

Wanneer u een regel schrapt, wordt de orde dat de resterende regels in werking worden gesteld automatisch aangepast om van de schrapping rekenschap te geven.

**Om een regel voor vooronderzoek te schrappen**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Pre-Search Rules]**.
1. Voor de [!DNL Pre-Search Rules] pagina, onder de **[!UICONTROL Actions]** kolom van de lijst, klik **[!UICONTROL Delete]** voor de bijbehorende regel die u wilt schrappen.
1. Klik in het [!DNL Confirmation] dialoogvenster op **[!UICONTROL OK]**.
1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Het veranderen van de orde dat de regels van het vooronderzoek lopen {#task_C18817276A3C459089C97448076365D1}

U kunt pre-onderzoeksregels opnieuw in orde brengen om de orde te veranderen waarin zij op presentatiemalplaatjes lopen.

De regels van het pre-onderzoek lopen in de orde dat zij werden bepaald. Hoger het de ordeaantal van een regel, later loopt het in het proces, die vroegere regels trompelen. U bestelt regels opnieuw door een nieuw aantal in de kolom van de Orde van de lijst op de [!DNL Pre-Search Rules] pagina in te gaan. U kunt belemmering-en-daling op regels ook gebruiken om hun looppasorde te veranderen.

**Om de orde te veranderen die de regels van het pre-onderzoek lopen**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Pre-Search Rules]**.
1. Op de [!DNL Pre-Search Rules] pagina, doe één van het volgende:

   * Klik de **[!UICONTROL Order]** kolomkopbal om de regels in stijgende of dalende orde te sorteren.
   * In de **[!UICONTROL Order]** kolom, op het tekstgebied links van een naam van de pre-onderzoeksregel, typ het ordeaantal dat u de regel wilt lopen.
   * Sleep een lijstrij aan de positie die u de regel wilt in werking stellen. Alle ordeaantallen worden bijgewerkt om op de nieuwe orde te wijzen waarin de regels lopen.

1. Klik op **[!UICONTROL Save Changes]**.
1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

