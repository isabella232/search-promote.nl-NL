---
description: U kunt de Stijgende Index gebruiken om "stukken"van uw levende of gefaseerde website, zoals een inzameling van vaak veranderde pagina's te indexeren.
seo-description: U kunt de Stijgende Index gebruiken om "stukken"van uw levende of gefaseerde website, zoals een inzameling van vaak veranderde pagina's te indexeren.
seo-title: Over Incrementele index
solution: Target
subtopic: Incremental Index
title: Over Incrementele index
topic: Index,Site search and merchandising
uuid: b1ee9b08-dcbe-4ffe-b0b4-d379daaac9b5
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a

---


# Over Incrementele index{#about-incremental-index}

U kunt de Stijgende Index gebruiken om &quot;stukken&quot;van uw levende of gefaseerde website, zoals een inzameling van vaak veranderde pagina&#39;s te indexeren.

## Incrementele index gebruiken {#concept_A7770F0552D14C47B3DDB65DB78FFFEE}

Een stijgende index neemt slechts seconden om uit te voeren en is nuttig op grote capaciteitswebsites die vele uren kunnen vergen om volledig te indexeren.

Wanneer u een stijgende index produceert, wordt de statusinformatie getoond, zoals begintijd, verstreken tijd, en fouten tijdens het het indexeren proces. De informatie over het statuut van uw laatste index wordt ook getoond.

U kunt het stijgende indexeringsproces op elk ogenblik tegenhouden of opnieuw beginnen.

Terwijl de nieuwe stijgende index voor uw levende website bouwt, kunnen de klanten uw plaats blijven zoeken gebruikend uw laatste stijgende index.

## Het vormen van een stijgende index van een gefaseerde website {#task_46A367B0786C4C90BFFA5D3F95FD86C0}

U kunt vormen welke websitepagina&#39;s u in uw stijgende Index wilt omvatten door website URLs en maskers te specificeren URLs.

**Om een stijgende index van een gefaseerde website te vormen**

1. Klik in het productmenu op **[!UICONTROL Index]** > **[!UICONTROL Incremental Index]** > **[!UICONTROL Configuration]**.
1. Voor de **[!UICONTROL Incremental Index Configuration]** pagina, gebruik de diverse gebieden om te specificeren welke pagina&#39;s die u wilt indexeren.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Veld </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>URL's toevoegen of bijwerken </p> </td> 
      <td colname="col2"> <p>URL's opgeven. </p> <p>De onderzoeksrobot indexeert slechts de gespecificeerde documenten die sinds de laatste tijd zijn veranderd u indexeerde. </p> <p>Bovendien, volgt de onderzoeksrobot verbindingen die binnen de gespecificeerde documenten en indexen slechts die documenten bevat zijn die zijn veranderd. </p> <p>Dit gebied moet document URLs slechts en niet maskers bevatten zoals in het volgende voorbeeld: </p> <p> 
        <userinput>
          https://www.mydomain.com/products/new.html 
        </userinput> </p> <p>U kunt de volgende sleutelwoorden met URL gebruiken: </p> <p> 
        <ul id="ul_62D1082ACBD547D092B10D72C56A3A1E"> 
          <li id="li_32C2B21DE75C4459908384CC44822F7D"> 
          <userinput>
            noindex 
          </userinput> <p>Als u niet de tekst op de pagina wilt indexeren die een gespecificeerde URL aanpast, maar u wilt de verbindingen van de pagina volgen, voeg toe 
            <userinput>
              noindex 
            </userinput> na URL zoals in het volgende voorbeeld: </p> <p> 
            <userinput>
              https://www.mydomain.com/products/new.html noindex 
            </userinput> </p> <p>Ben zeker u scheidt 
            <userinput>
              noindex 
            </userinput> van URL met een ruimte; een komma is geen geldige scheidingsteken. </p> </li> 
          <li id="li_33AB62B669084BF7B976F4308715E435"> 
          <userinput>
            onopvolgzaam 
          </userinput> <p>Als u de tekst op de pagina wilt indexeren die de gespecificeerde URL aanpast, maar u wilt niet de verbindingen van de pagina volgen, voeg toe 
            <userinput>
              onopvolgzaam 
            </userinput> na URL zoals in het volgende voorbeeld: </p> <p> 
            <userinput>
              https://www.mydomain.com/products/new.html 
            </userinput> </p> <p> Ben zeker u scheidt 
            <userinput>
              onopvolgzaam 
            </userinput> van URL met een ruimte; een komma is geen geldige scheidingsteken. </p> </li> 
        </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>URL-maskers zoeken en bijwerken </p> </td> 
      <td colname="col2"> <p>Specificeer eenvoudige URL maskers-volledige weg, gedeeltelijke weg, of wegen die wilde kaarten of regelmatige uitdrukkingen gebruiken. </p> <p>De onderzoeksrobot vindt alle passende documenten en indexen slechts die documenten die sinds de laatste tijd zijn veranderd u indexeerde. </p> <p>Bovendien, volgt de onderzoeksrobot verbindingen die binnen de passende documenten en indexen slechts die pagina's bevat zijn die zijn veranderd. Bijvoorbeeld: </p> <p> 
      <userinput>
        https://www.mydomain.com/products/household/*.html 
      </userinput> </p> <p>U kunt regelmatige uitdrukkingen zoals in het volgende voorbeeld ook gebruiken: </p> <p> 
      <userinput>
        regexp ^https://www\.mydomain\.com/products/home/.*\.html$ 
      </userinput> </p> <p>Zie <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Regelmatige expressies</a>. </p> <p>U kunt de sleutelwoorden ook gebruiken 
      <userinput>
        onopvolgzaam 
      </userinput> en 
      <userinput>
        noindex 
      </userinput> zoals beschreven in <span class="uicontrol"> Add of Update URLs </span> hierboven. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>URL-maskers opnemen en uitsluiten </p> </td> 
      <td colname="col2"> <p>Specificeer eenvoudig omvatten of sluit URL maskers-volledige weg uit, gedeeltelijke weg, of wegen die wilde kaarten of regelmatige uitdrukkingen gebruiken. </p> <p>De onderzoeksrobot vindt en indexen ("omvat") of negeert ("sluit") documenten uit die op het type van masker worden gebaseerd dat wordt gespecificeerd. </p> <p> Wanneer het indexeren van een plaats, worden de richtingen gevolgd in orde van verschijning. Bijvoorbeeld, de volgende lijst van maskers: </p> <p> 
      <userinput>
        https://www.mydomain.com/products/household/lightbulbs*.html 
      </userinput> </p> <p> 
      <userinput>
        sluit https://www.mydomain.com/products/ uit 
      </userinput> </p> <p>indexeert de pagina's 
      <userinput>
        gloeilampen1.html 
      </userinput> en 
      <userinput>
        bliksem2.html 
      </userinput>. Nochtans, indexeert het geen andere pagina's die onder de productfolder vermeld zijn. </p> <p>Een masker URL dat eerst verschijnt neemt altijd belangrijkheid over die later in de lijst verschijnt. Bovendien, als de onderzoeksrobot een document ontmoet dat zowel aanpast omvat masker en sluit masker uit, neemt het masker dat eerst vermeld is belangrijkheid. </p> <p>U kunt de sleutelwoorden ook gebruiken 
      <userinput>
        onopvolgzaam 
      </userinput> en 
      <userinput>
        noindex 
      </userinput> zoals beschreven in <span class="uicontrol"> Add of Update URLs </span> hierboven. </p> <p>Zie <a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164" type="concept" format="dita" scope="local"> over Maskers</a>URL. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Datummaskers opnemen en uitsluiten </p> </td> 
      <td colname="col2"> <p>Specificeer eenvoudig omvatten of sluit datum maskers-volledige weg, gedeeltelijke weg, of wegen uit die wilde kaarten of regelmatige uitdrukkingen gebruiken. </p> <p>De onderzoeksrobot vindt en indexen ("omvat") of negeert ("sluit") documenten uit die op zowel URL als de datum van documenten worden gebaseerd. </p> <p>U kunt de volgende types van datummaskers gebruiken: </p> <p> 
      <ul id="ul_8958ED54C8EF405AA259236595ED3ABA"> 
      <li id="li_0A7841767E004F088CA6FA42E99B9F32"> 
      <userinput>
        aantal dagen NNN 
      </userinput> <p>De onderzoeksrobot indexeert alle documenten die het gespecificeerde masker URL aanpassen en NNN dagen of meer oud zijn. </p> <p>U kunt het masker URL met één of meer van de volgende sleutelwoorden volgen: 
        <ul id="ul_22A38D5F38B344ABB02B16EB1865813B"> 
        <li id="li_B89CC37DC2A1428185E86FFCB9DDB193">onopvolgzaam </li> 
        <li id="li_C2579B3A338D4AF987C3F518806734B0">noindex </li> 
        <li id="li_0527BF7103F34B83AC3E684069B899F7">serverdatum </li> 
        </ul> </p> <p>Bijvoorbeeld, omvat het volgende masker alle documenten in de /archive/steunomslag die 0 dagen of ouder zijn: </p> <p> 
        <userinput>
          include-days 0 https://www.mydomain.com/archive/support/ 
        </userinput> </p> </li> 
      <li id="li_7663ABED40DD4E159F746E4F92BB6407"> 
      <userinput>
        inclusiedatum JJJJ-MM-DD 
      </userinput> <p>De onderzoeksrobot indexeert alle documenten die het gespecificeerde masker URL aanpassen en is zo oud of ouder dan de datum JJJJ-MM-DD. </p> <p>U kunt het masker URL met één of meer van de volgende sleutelwoorden volgen: </p> <p> 
        <ul id="ul_57BF37A413BB4A4D962863DACE56F395"> 
        <li id="li_88CAB9AB583B4754A5C53478BD1108FF">onopvolgzaam </li> 
        <li id="li_999E1CD34FDE4A1B9C332B4AA8C2887D">noindex </li> 
        <li id="li_05646FACF3524D2A9E201A23770E357F"> serverdatum </li> 
        </ul> </p> <p>Het volgende maskervoorbeeld omvat alle documenten in /archive/omslag die op of vóór 25 Juli, 2011 wordt gedateerd: </p> <p> 
        <userinput>
          datum 2011-07-25 https://www.mydomain.com/archive/ 
        </userinput> </p> </li> 
      <li id="li_172692DEDA8744B3AA492701D24C2D80"> 
      <userinput>
        uitsluitingsdagen NNN 
      </userinput> <p>Maak het indexeren van alle documenten onbruikbaar die het gespecificeerde masker aanpassen URL en NNN dagen of meer oud zijn. </p> <p>Naar keuze, kunt u het masker volgen URL door het sleutelwoord 
        <userinput>
          serverdatum 
        </userinput>. </p> <p>Het volgende maskervoorbeeld sluit alle Pdf- dossiers uit die 90 dagen oud of ouder van uw index zijn: </p> <p> 
        <userinput>
          uitsluitingsdagen 90 *.pdf 
        </userinput> </p> </li> 
      <li id="li_26078517744D4AECBE1351008926CBAE"> 
      <userinput>
        exclusief datum JJJJ-MM-DD 
      </userinput> <p>Maak het indexeren van alle documenten onbruikbaar die het gespecificeerde Url- masker aanpassen en zijn zo oud of ouder dan de datum JJJJ-MM-DD. </p> <p>Naar keuze, kunt u het masker volgen URL door het sleutelwoord 
        <userinput>
          serverdatum 
        </userinput>. </p> <p>Het volgende maskervoorbeeld sluit alle documenten in /archive/folder uit die op of vóór 23 april 2004 wordt gedateerd: </p> <p> 
        <userinput>
          datum 2004-04-23 https://www.mydomain.com/archive/ 
        </userinput> </p> </li> 
      </ul> </p> <p>Zie <a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_F4F1F58A646F4A86B8650EC46FDCEF66" type="concept" format="dita" scope="local"> Datummaskers</a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>URL's verwijderen </p> </td> 
      <td colname="col2"> <p>URL's opgeven. </p> <p>De onderzoeksrobot vindt en schrapt de gespecificeerde documenten van uw onderzoeksindex. Als een gespecificeerde pagina reeds in uw onderzoeksindex is, schrapt de robot het alvorens het toevoegt of een andere pagina's bijwerkt. </p> <p>Dit gebied moet slechts document URLs, en niet maskers bevatten. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>URL-maskers zoeken en verwijderen </p> </td> 
      <td colname="col2"> <p>Specificeer eenvoudige URL maskers-volledige weg, gedeeltelijke weg, of degenen die wilde kaarten of regelmatige uitdrukkingen gebruiken. </p> <p>Als het gespecificeerde masker URL pagina's in uw onderzoeksindex aanpast, schrapt de onderzoeksrobot de pagina's alvorens het toevoegt of een andere pagina's bijwerkt. Bijvoorbeeld: </p> <p> 
      <userinput>
        https://www.mydomain.com/products/1998/household/* 
      </userinput> </p> <p>U kunt regelmatige uitdrukkingen zoals in het volgende voorbeeld ook gebruiken: </p> <p> 
      <userinput>
        regexp ^https://www\.mydomain\.com/products/199[567]/.*$ 
      </userinput> </p> <p>Zie <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Regelmatige expressies</a>. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Klik op **[!UICONTROL Save Changes]**.
1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Het plaatsen van het stijgende indexprogramma voor een levende website {#task_2A46BA189ECC4317A9D5C6E99A336F33}

U kunt de Stijgende frequentie van de Index en de basistijd selecteren die wordt gebruikt om uw stijgende index te kruipen en bij te werken.

De tijd die u selecteert is lokaal volgens de tijdzone die in de Montages van de Rekening wordt gevormd.

Zie [Je accountinstellingen](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)configureren.

De servers van het Web zijn vaak gepland om voor onderhoud in het midden van de nacht neer te gaan. Als uw server tijdens een geplande indextijd neer is, zal het het indexeren proces ontbreken. Zeker ben dat u een tijd van dag selecteert wanneer uw Webserver beschikbaar is.

Het indexprogramma is slechts op uw levende index van toepassing; u kunt gefaseerde indexen niet plannen.

**Om het stijgende indexprogramma voor een levende website te plaatsen**

1. Klik in het productmenu op **[!UICONTROL Index]** > **[!UICONTROL Incremental Index]** > **[!UICONTROL Live Schedule]**.
1. Voor binnen in de **[!UICONTROL Incremental Index Schedule]** pagina, in de **[!UICONTROL Incrementally Index]** drop-down lijst, selecteer de het indexeren frequentie in uren of notulen.
1. In de **[!UICONTROL Base Time]** drop-down lijst, selecteer de beginnende tijd wanneer u een nieuwe stijgende index wilt regenereren.
1. Klik op **[!UICONTROL Save Changes]**.

## Het runnen van een stijgende index van een levende of gefaseerde website {#task_9BFB6157F3884B2FAECB7E0E9CA318CB}

U kunt de Stijgende Index gebruiken om &quot;stukken&quot;van uw levende of gefaseerde website, zoals een inzameling van vaak veranderde pagina&#39;s te indexeren.

**Om een stijgende index van een levende of gefaseerde website in werking te stellen**

1. Voor het productmenu, doe één van het volgende:

   * Klik op **[!UICONTROL Index]** > **[!UICONTROL Incremental Index]** > **[!UICONTROL Live Index]**.

   * Klik op **[!UICONTROL Index]** > **[!UICONTROL Incremental Index]** > **[!UICONTROL Staged Index]**.

1. Klik op **[!UICONTROL Incremental Index Now]**.
1. (Facultatief) als het indexeren fouten voorkwamen, klik **[!UICONTROL View Errors]** om het bijbehorende logboek te bekijken.

## Het bekijken van het stijgende indexlogboek van een levende of gefaseerde website {#task_E668E1F1240C476DAA1CA783DC728232}

Wanneer een levende stijgende index of een gefaseerde stijgende index volledig is, kunt u zijn bijbehorend logboek bekijken om het even welke fouten problemen op te lossen die voorkwamen.


U kunt geen logboeken uitvoeren, noch hen bewaren. Het logboek blijft beschikbaar voor het bekijken tot de nieuwe index voorkomt.

**Om het stijgende indexlogboek van een levende of gefaseerde website te bekijken**

1. Voor het productmenu, doe één van het volgende:

   * Klik op **[!UICONTROL Index]** > **[!UICONTROL Incremental Index]** > **[!UICONTROL Live Log]**.

   * Klik op **[!UICONTROL Index]** > **[!UICONTROL Incremental Index]** > **[!UICONTROL Staged Log]**.

1. Voor de logboekpagina, bij de bovenkant of de bodem, doe om het even welke volgend:

   * Gebruik de navigatieopties **[!UICONTROL First]**, **[!UICONTROL Prev]**, **[!UICONTROL Next]**, **[!UICONTROL Last]**, of **[!UICONTROL Go to line]** om zich door het logboek te bewegen.

   * Gebruik de vertoningsopties **[!UICONTROL Errors only]**, **[!UICONTROL Wrap line]**, of **[!UICONTROL Show]** om te raffineren wat u ziet.

