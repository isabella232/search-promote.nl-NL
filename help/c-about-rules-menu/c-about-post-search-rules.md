---
description: U kunt Post-Onderzoek Regels gebruiken om de resultaten van een onderzoek te onderzoeken en te bepalen hoe het onderzoek de getoonde inhoud beïnvloedt.
seo-description: U kunt Post-Onderzoek Regels gebruiken om de resultaten van een onderzoek te onderzoeken en te bepalen hoe het onderzoek de getoonde inhoud beïnvloedt.
seo-title: Informatie over regels voor postzoekopdrachten
solution: Target
title: Informatie over regels voor postzoekopdrachten
topic: Rules,Site search and merchandising
uuid: 312d1e4a-f5b6-4629-8645-17e6f6c09fc4
translation-type: tm+mt
source-git-commit: d07cdc2c88f93eed4cecb0ee8818f7fdea06ee9d

---


# Informatie over regels voor postzoekopdrachten{#about-post-search-rules}

U kunt Post-Onderzoek Regels gebruiken om de resultaten van een onderzoek te onderzoeken en te bepalen hoe het onderzoek de getoonde inhoud beïnvloedt.

## Postzoekregels gebruiken {#concept_AF6ADFCC0ADF4A788003964939917FDE}

Als een onderzoek geen resultaten heeft, kan een Regel van het Post-Onderzoek een onderzoek naar een gelijkaardig punt uitvoeren. Of, het kan een Web-pagina tonen die andere punten aan klanten adviseert die naar het punt zoeken dat niet werd gevonden.

Elke regel na het zoeken bestaat uit twee hoofdelementen: het optreden van de regeling en de facultatieve voorwaarden ervan. U kunt een onbeperkt aantal regels en voorwaarden specificeren. De orde van deze regels is belangrijk omdat de geplaatste regel door regel-door-regel van een lus wordt voorzien. Wanneer de voorwaarden van een regel aanpassen, worden alle bijbehorende acties uitgevoerd.

U kunt de reeks onderzoeksresultaten voor een maximum van drie ronde van het zoeken raffineren. Daarna, wordt wat momenteel beschikbaar is gebruikt. Deze grens verhindert oneindige lijnen en zorgt ervoor dat de klant een efficiënte reactie ontvangt. Hoe vaker je een zoekopdracht opnieuw uitvoert, hoe langer het duurt om je zoekresultaten terug te geven. Als geen van de aanpassingsregels één van de onderzoeken naar het momenteel gebruikte presentatiemalplaatje verandert of het malplaatje verandert, wordt de reeks onderzoeksresultaten beschouwd als gebeëindigd en post-onderzoek weggaat.

De post-onderzoeksverwerking bouwt op de vroegere het Schoonmaken van de Vraag van de verwerkingsmodules en de verwerking pre-Onderzoek voort. Daarom zijn om het even welke douanevariabelen die in die modules worden geplaatst beschikbaar voor gebruik in de regels van de post-onderzoeksverwerking. Op dezelfde manier heeft de pre-onderzoeksverwerking alle malplaatjes geconcretiseerd waar elke genoemd onderzoek verbonden aan het presentatiemalplaatje zijn eigen lokale exemplaar van de parameters van CGI heeft. Op uw beurt, kunt u elke onderzoek aanpassen individueel.

Zie [over het Schoonmaken van de Vraag Regels](../c-about-rules-menu/c-about-query-cleaning-rules.md#concept_17F3CDDC3C8A4128AF092A82B777B86C).

Zie [over Voorspelregels](../c-about-rules-menu/c-about-pre-search-rules.md#concept_5BF84BB6FACB4645BA9CB7496A01CD1F)voor zoeken.

## Informatie over de voorwaarden voor regel na zoekopdracht {#section_C43EB77CC0AC43B8B9D38569264BF1B5}

De voorwaarden zijn facultatief. Als u specificeert dat de acties voor elke vraag worden gespecificeerd, dan worden de acties altijd genomen. U kunt voorwaarden op om het even welke CGI vraagparameter, koekje, onderzoeksresultaat, of douanevariabele baseren die een vorige regel heeft geplaatst. Of, u kunt het op een systeemvoorwaarde baseren zoals wat het momenteel geselecteerde malplaatje is of als het de laatste onderzoek is. Wanneer u een voorwaarde op de resultaten van een onderzoek of een parameter van CGI bouwt, specificeert u het malplaatje en de naam van het onderzoek.

## Informatie over handelingen voor regel na zoekopdracht {#section_0E15FE683A894ECAAA386267EEC7F7C5}

Alle acties in een Regel van het post-Onderzoek die passende voorwaarden hebben worden uitgeoefend. De acties bestaan typisch uit een verrichting, de gegevens om de handeling uit te voeren, en de waarde aan gebruik. De eenvoudigste actie is om te schakelen welk malplaatje van de Presentatie aan gebruik gebaseerd op de voorwaarden van de Regel van het post-Onderzoek wordt gebaseerd. U kunt geavanceerdere acties gebruiken om de parameters voor een onderzoek te veranderen dat in het onderzoek resulteert dat wordt overgedaan. Wanneer het uitvoeren van een verrichting op de het onderzoeksparameter van een malplaatje, specificeer een malplaatje van de Presentatie en onderzoek.

## Algemene bepalingen {#section_AEE923988CC748FF9DEF2233FBF333B5}

Wanneer het uitvoeren van verrichtingen op de het onderzoeksparameter van een malplaatje, bestaan twee speciale waarden, *target en *primary voor het malplaatje van de Presentatie en het genoemde onderzoek respectievelijk. Gebruik deze waarden om regels te bouwen die op het huidige gerichte primaire onderzoek van het malplaatje worden gebaseerd. Deze concepten laten u generische regels bouwen waar u niet om zich over te hoeven ongerust maken wat het huidige gerichte malplaatje of het primaire onderzoek worden geroepen. Als deze pas de eerste door de post-onderzoeksverwerking is, is het gerichte malplaatje wat de pre-onderzoeksverwerking het aan plaatst.

## Omleiden {#section_E5669A2F13C240F2968E31C75591CD6A}

De directe Hits en richt binnen de Schoonmaak van de Vraag opnieuw om u aan een URL te richten die op de inkomende onderzoekstermijnen wordt gebaseerd. Richt binnen post-onderzoeksregels opnieuw uit breidt dit idee, behalve dat het u laat controleren hoeveel resultaten die het onderzoek terugkwam alvorens te beslissen of wilt u opnieuw richten om plaatsvindt. Met de Regels van het post-Onderzoek, kunt u aan een URL opnieuw richten, waar u douanevariabelen of vraagparameters kunt substitueren. Of, u kunt aan een gebied binnen het eerste resultaat opnieuw richten. Wanneer u aan het gebied van een resultaat opnieuw richt, bepaalt u het gebied in het malplaatje van het Vervoer, en het moet een geldige, expliciete URL bevatten, anders wordt opnieuw gericht overgeslagen.

Wanneer u het herleidingsmechanisme binnen de Regels van het Post-Onderzoek gebruikt, kunt u ontdekken wanneer een onderzoek één enkel resultaat terugkeert. Eerder dan het terugkeren van zulk een resultaat, kunt u aan de Web-pagina opnieuw richten die met het resultaat wordt geassocieerd.

Zie het opnieuw richten voorbeeld hieronder voor een voorbeeld van het gebruiken van opnieuw richt met de Regels van het post-Onderzoek.

## Laatste regel {#section_FC1E0050C9324278B171038E98F6C335}

Wanneer aan de voorwaarden voor een regel wordt voldaan die de optie heeft **[!UICONTROL Last Rule]** geplaatst, voert de post verwerkingsmodule geen extra regels na de actie van de passende regel uit. Deze situatie is nuttig wanneer u acties hebt geplaatst die een recentere regel veroorzaken om aan te passen maar u wilt de verwerking ophouden. En, voor die latere regel om potentieel na de volgende ronde van het zoeken aan te passen.

## Voorbeelden {#section_DDB98383690941F9B44AD00FBA55BB56}

In het volgende voorbeeld, veronderstel dat u twee presentatiemalplaatjes hebt. Één malplaatje wordt gebruikt om vele onderzoeksresultaten te tonen en het andere malplaatje wordt gebruikt om één enkel resultaat en een extra onderzoek naar toebehoren te tonen met betrekking tot het belangrijkste onderzoek. U wilt ontdekken wanneer u één enkel resultaat hebt en op uw ander presentatiemalplaatje overschakelt. Om deze taak te verwezenlijken, kunt u de volgende regels gebruiken:

```
On condition: 
  targeted template is default 
  targeted template primary results equal 1 
  not last search 
Perform the following actions: 
  Set targeted template to product_spotlight
```

MegaElectronic is een grote elektronicawinkel. Na het analyseren van hun onderzoeksgegevens, merkt MegaElectronic op dat veel van hun klanten een productonderzoek uitvoeren gebruikend het deelaantal van een product. In dergelijke gevallen, wil MegaElectronic aan de Web-pagina opnieuw richten die met het product wordt geassocieerd, als de klant rechtstreeks naar het zocht en slechts één enkel product werd gevonden.

Om dit resultaat te bereiken, kunt u één enkele regel met drie voorwaarden gebruiken. De eerste voorwaarde controleert dat het teruggekeerde onderzoek slechts één enkel resultaat heeft. De tweede voorwaarde zorgt ervoor dat de vraagtermijn het formaat van het deelaantal van MegaElectronic voor de resultaten aanpast die zij willen veroorzaken opnieuw richten. De derde voorwaarde zorgt ervoor dat de klant geen facetten gebruikte om neer aan één resultaat te boren, aangezien het deelaantal een gedeeltelijk deelaantal zou kunnen zijn en meer dan één resultaat zou kunnen terugkeren. De actie richt aan een gebied binnen het resultaat opnieuw.

```
On condition: 
  targeted template's primary results equal 1 
  query q matches regular expression ^\D\D\D-\d+ 
  no facet selected ^\D\D\D-\d+ 
Perform the following actions: 
  redirect to result field "loc" in template *targeted for search *primary
```

## Beste praktijken {#section_1BF7DE1BD5664B3BAEC26AA829FDB0BA}

* Om het even welke reeks regels die een nieuwe ronde van het zoeken teweegbrengen zou altijd een voorwaardelijke clausule moeten hebben om te controleren dat dit niet de laatste pas door de module is. Als je het maximum aantal zoekopdrachten al hebt uitgevoerd, kun je geen zoekopdrachten opnieuw uitvoeren.
* Als u op de laatste pas door de module bent en de resultaten nog slecht zijn, kunt u op een malplaatje &quot;geen resultaten&quot;schakelen.
* U zou het veranderen van een presentatiemalplaatje op het resultaat van een onderzoek moeten baseren dat potentieel andere parameters heeft. Als u een malplaatje wilt selecteren dat slechts op de inkomende vraag gebaseerd is, is een pre-onderzoeksregel efficiënter.
* De mijning van gegevens van de vraag wordt gedaan in de het Schonen van de Vraag module. U kunt de douanevariabelen in de post-onderzoeksverwerking van verwijzingen voorzien.
* Wanneer u opnieuw richt, controleer altijd dat de klant geen facetten heeft geselecteerd. De reden is omdat het ongelegen is wanneer een klant in een facet drijft en plotseling van de onderzoeksresultaten wordt verwijderd. De klant kan het facet willen schrappen wanneer zij zien dat het enige resultaat niet is willen zij zocht.

## Een nieuwe regel voor postzoekopdrachten toevoegen {#task_52F6F9AAD65B45B5ACA1FF245DFFADD9}

U kunt gebruiken [!DNL Post-Search Rules] om te selecteren welk presentatiemalplaatje wordt gebruikt om de onderzoeksresultaten te tonen die op de inkomende vraag worden gebaseerd.

**Om een nieuwe regel voor postzoekopdrachten toe te voegen**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Post-Search Rules]**.
1. Voor de [!DNL Post-Search Rules] pagina, klik **[!UICONTROL Add New Rule]**.
1. Op het [!DNL Name] gebied, typ de naam van de nieuwe vraag schoonmaakregel.
1. Voor de [!DNL Add Post-Search Rule] pagina, gebruik de drop-down lijsten en tekstgebieden om uw vraag uit te bouwen.

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
      <td colname="col2"> <p>Een HTTP koekje. De namen en de waarden van het koekje moeten het Uniforme Herkenningsteken van het Middel zijn gecodeerd. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Aangepaste variabele </p> </td> 
      <td colname="col2"> <p>Een user-defined variabele. U kunt, een onbeperkt aantal douanevariabelen toevoegen schrappen of plaatsen. </p> <p>U kunt om het even welke douanevariabelen van verwijzingen voorzien die u in het Schonen van de Vraag en in de modules van Regels van het pre-Onderzoek, binnen de Regels van het post-Onderzoek bepaalde. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Systeemvariabele </p> </td> 
      <td colname="col2"> <p>Alleen-lezen variabelen die zijn ingesteld op het interne systeem dat u kunt controleren. De volgende systeemvariabelen worden ondersteund: </p> <p> 
        <ul id="ul_BC17F1637F27424CA4E8F530C28A3245"> 
          <li id="li_C7DF96EFD7AA4A449D00F7EACCAA0EB1"> <span class="uicontrol"> hostnaam </span> <p>De naam van de servergastheer. </p> </li> 
          <li id="li_F85AB1D2B9374A859657D12B8ED6674B"> <span class="uicontrol"> buik </span> <p>Het gevraagde Eenvormige Herkenningsteken van het Middel zonder het vraagkoord. </p> </li> 
          <li id="li_440149C9EC6E4805B77BBC97BE41542A"> <span class="uicontrol"> arcering </span> <p>Het volledige vraagkoord. </p> </li> 
          <li id="li_F583FC4B0E404858BB3522B33A6F7A0A"> <span class="uicontrol"> milieu </span> <p>"Stadium"of "leef"afhankelijk van of de inkomende vraag werd verzonden naar uw gefaseerde milieu of uw levende milieu. </p> </li> 
          <li id="li_15902AA49B144D42A5E95D7E8B0FB1E1"> <span class="uicontrol"> verwijzende </span> <p>Het Eenvormige Merkteken van het Middel dat de klant kwam van. </p> </li> 
        </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Systeemvariabele </p> </td> 
      <td colname="col2"> <p>Alleen-lezen variabelen die u kunt gebruiken in omstandigheden om de huidige status te bepalen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Zoekfacet van template </p> </td> 
      <td colname="col2"> <p>Een facet dat aan een genoemd onderzoek verbonden aan een presentatiemalplaatje lokaal is. Een facet is hoofdzakelijk speciale parameters van CGI die worden gebruikt om te wijzen op welke waarde binnen een facet een klant heeft geselecteerd. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Zoekparameter van sjabloon </p> </td> 
      <td colname="col2"> <p>Een parameter van CGI die aan een genoemd onderzoek verbonden aan een presentatiemalplaatje lokaal is. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Backend Parameter Sjabloon </p> </td> 
      <td colname="col2"> <p>De inkomende vraagparameters worden uiteindelijk vertaald in achterste deelparameters die worden gebruikt om het onderzoek uit te voeren. </p> <p>Zie <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> Achterste onderzoekCGI parameters </a>. </p> <p>De parameters van de steun verschijnen niet op navigatie elementen. Dientengevolge, kunt u om het even welke extra parameters verbergen die u op een onderzoek van uw klanten wilt toepassen. </p> <p>De parameter is lokaal aan een specifiek onderzoek binnen een presentatiemalplaatje. De acties op achterste deelparameters zijn laat-bindend; dat wil zeggen, ze worden toegepast vlak voordat de zoekopdracht wordt verzonden. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Gerichte template </p> </td> 
      <td colname="col2"> <p>Een speciaal geval van een systeem-bepaalde douanevariabele die niet kan worden geschrapt. Deze variabele bevat het huidige gerichte presentatiemalplaatje. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Rank </p> </td> 
      <td colname="col2"> <p>Laat u specificeren welke rangschikkende regel in het onderzoek te gebruiken. Deze optie verschijnt slechts wanneer u het rangschikken gebieden en het rangschikken regels hebt bepaald. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Laatste regel </p> </td> 
      <td colname="col2"> <p>Wanneer gecontroleerd, voert de post-onderzoeksverwerkingsmodule geen extra regels na de actie van de passende regel uit. Deze actie is nuttig voor wanneer u acties hebt geplaatst die een recentere regel veroorzaken om aan te passen maar u wilt niet de recentere regel lopen. </p> </td> 
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

## Een regel voor postzoekopdrachten bewerken {#task_ECB00334C0A74C87AF857DB3EB372119}

Je kunt bestaande regels voor postzoekopdrachten bewerken die je aan de [!DNL Post-Search Rules] pagina hebt toegevoegd.

**Een regel voor postzoekopdrachten bewerken**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Pre-Search Rules]**.
1. Voor de [!DNL Post-Search Rules] pagina, onder de **[!UICONTROL Actions]** kolom van de lijst, klik **[!UICONTROL Edit]** voor de bijbehorende regel die u wilt uitgeven.
1. Voor de [!DNL Edit Post-Search Rule] pagina, gebruik de drop-down lijsten en tekstgebieden om uw vraag uit te bouwen.

   Zie de lijst van opties onder het [Toevoegen van een nieuwe post-onderzoeksregel](../c-about-rules-menu/c-about-post-search-rules.md#task_52F6F9AAD65B45B5ACA1FF245DFFADD9).
1. Klik op **[!UICONTROL Save Changes]**.
1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een regel voor na het zoeken verwijderen {#task_0F4653AB20D54B769A4FA8D1491AB4CF}

Je kunt regels voor postzoekopdrachten verwijderen die je niet meer nodig hebt of niet meer gebruikt.

Wanneer u een regel schrapt, wordt de orde dat de resterende regels in werking worden gesteld automatisch aangepast om van de schrapping rekenschap te geven.

**Om een regel na het zoeken te schrappen**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Post-Search Rules]**.
1. Voor de [!DNL Post-Search Rules] pagina, onder de **[!UICONTROL Actions]** kolom van de lijst, klik **[!UICONTROL Delete]** voor de bijbehorende regel die u wilt schrappen.
1. Klik in het [!DNL Confirmation] dialoogvenster op **[!UICONTROL OK]**.
1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Het veranderen van de orde dat de regels van het post-onderzoek lopen {#task_40542FCD32234BBF881A81BF5477F78F}

U kunt post-onderzoeksregels opnieuw in orde brengen om de orde te veranderen waarin zij op presentatiemalplaatjes lopen.

De regels van het post-onderzoek lopen in de orde dat zij werden bepaald. Hoger het de ordeaantal van een regel, later loopt het in het proces, die vroegere regels trompelen. U bestelt regels opnieuw door een nieuw aantal in de kolom van de Orde van de lijst op de [!DNL Post-Search Rules] pagina in te gaan. U kunt belemmering-en-daling op regels ook gebruiken om hun looppasorde te veranderen.

**Om de orde te veranderen dat de post-onderzoeksregels lopen**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Post-Search Rules]**.
1. Op de [!DNL Post-Search Rules] pagina, doe één van het volgende:

   * Klik de **[!UICONTROL Order]** kolomkopbal om de regels in stijgende of dalende orde te sorteren.
   * In de [!DNL Order] kolom, op het tekstgebied links van een naam van de pre-onderzoeksregel, typ het ordeaantal dat u de regel wilt lopen.
   * Sleep een lijstrij aan de positie die u de regel wilt in werking stellen. Alle ordeaantallen worden bijgewerkt om op de nieuwe orde te wijzen waarin de regels lopen.

1. Klik op **[!UICONTROL Save Changes]**.
1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).
