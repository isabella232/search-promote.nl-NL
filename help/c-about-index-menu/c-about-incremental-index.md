---
description: Met Incrementele index kunt u "stukken" van uw actieve of gefaseerde website indexeren, zoals een verzameling pagina's die vaak worden gewijzigd.
seo-description: Met Incrementele index kunt u "stukken" van uw actieve of gefaseerde website indexeren, zoals een verzameling pagina's die vaak worden gewijzigd.
seo-title: Informatie over incrementele index
solution: Target
subtopic: Incremental Index
title: Informatie over incrementele index
topic: Index,Site search and merchandising
uuid: b1ee9b08-dcbe-4ffe-b0b4-d379daaac9b5
translation-type: tm+mt
source-git-commit: 552f93f1f630c64bbe3d5c8a87c4f5895ae6868c
workflow-type: tm+mt
source-wordcount: '1377'
ht-degree: 0%

---


# Info incrementele index{#about-incremental-index}

Met Incrementele index kunt u &quot;stukken&quot; van uw actieve of gefaseerde website indexeren, zoals een verzameling pagina&#39;s die vaak worden gewijzigd.

## Incrementele index {#concept_A7770F0552D14C47B3DDB65DB78FFFEE} gebruiken

Een incrementele index duurt slechts seconden en is handig voor websites met grote capaciteit die vele uren kunnen duren om volledig te indexeren.

Wanneer u een incrementele index genereert, wordt statusinformatie weergegeven, zoals begintijd, verstreken tijd en fouten tijdens het indexeringsproces. Er wordt ook informatie weergegeven over de status van de laatste index.

U kunt het incrementele indexeringsproces op elk gewenst moment stoppen of opnieuw starten.

Terwijl de nieuwe incrementele index voor uw live website wordt gegenereerd, kunnen klanten uw site blijven doorzoeken met uw laatste incrementele index.

## Een incrementele index van een gefaseerde website configureren {#task_46A367B0786C4C90BFFA5D3F95FD86C0}

U kunt configureren welke websitepagina&#39;s u in uw incrementele index wilt opnemen door URL&#39;s van websites en URL-maskers op te geven.

**Een incrementele index van een gefaseerde website configureren**

1. Klik in het productmenu op **[!UICONTROL Index]** > **[!UICONTROL Incremental Index]** > **[!UICONTROL Configuration]**.
1. Gebruik op de pagina **[!UICONTROL Incremental Index Configuration]** de verschillende velden om op te geven welke pagina&#39;s u wilt indexeren.

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
      <td colname="col2"> <p>Geef URL's op. </p> <p>De zoekrobot indexeert alleen de opgegeven documenten die zijn gewijzigd sinds de laatste keer dat u hebt geïndexeerd. </p> <p>Bovendien volgt de zoekrobot koppelingen die zich in de opgegeven documenten bevinden en indexeert deze alleen de documenten die zijn gewijzigd. </p> <p>Dit veld mag alleen document-URL's bevatten en geen maskers zoals in het volgende voorbeeld: </p> <p> 
        <code>
          https://www.mydomain.com/products/new.html 
        </code> </p> <p>U kunt de volgende trefwoorden gebruiken met de URL: </p> <p> 
        <ul id="ul_62D1082ACBD547D092B10D72C56A3A1E"> 
          <li id="li_32C2B21DE75C4459908384CC44822F7D"> 
          <code>
            noindex 
          </code> <p>Als u niet de tekst op de pagina wilt indexeren die overeenkomt met een opgegeven URL, maar u de koppelingen op de pagina wilt volgen, voegt u 
            <code>
              noindex 
            </code> na URL zoals in het volgende voorbeeld: </p> <p> 
            <code>
              https://www.mydomain.com/products/new.html noindex 
            </code> </p> <p>Zorg ervoor dat u scheidt 
            <code>
              noindex 
            </code> vanaf de URL met een spatie; een komma is geen geldig scheidingsteken. </p> </li> 
          <li id="li_33AB62B669084BF7B976F4308715E435"> 
          <code>
            nofollow 
          </code> <p>Als u de tekst op de pagina wilt indexeren die overeenkomt met de opgegeven URL, maar u de koppelingen op de pagina niet wilt volgen, voegt u 
            <code>
              nofollow 
            </code> na URL zoals in het volgende voorbeeld: </p> <p> 
            <code>
              https://www.mydomain.com/products/new.html nofollow 
            </code> </p> <p> Zorg ervoor dat u scheidt 
            <code>
              nofollow 
            </code> vanaf de URL met een spatie; een komma is geen geldig scheidingsteken. </p> </li> 
        </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>URL-maskers zoeken en bijwerken </p> </td> 
      <td colname="col2"> <p>Geef eenvoudige URL-maskers op: volledig pad, gedeeltelijk pad of paden die gebruikmaken van wilde kaarten of reguliere expressies. </p> <p>De zoekrobot zoekt alle overeenkomstige documenten en indexeert alleen de documenten die zijn gewijzigd sinds de laatste keer dat u hebt geïndexeerd. </p> <p>Bovendien volgt de zoekrobot koppelingen in de overeenkomende documenten en indexeert deze alleen de pagina's die zijn gewijzigd. Bijvoorbeeld: </p> <p> 
      <code>
        https://www.mydomain.com/products/household/*.html 
      </code> </p> <p>U kunt ook reguliere expressies gebruiken, zoals in het volgende voorbeeld: </p> <p> 
      <code>
        regexp ^https://www\.mydomain\.com/products/household/.*\.html$ 
      </code> </p> <p>Zie <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Reguliere expressies</a>. </p> <p>U kunt ook de trefwoorden gebruiken 
      <code>
        nofollow 
      </code> en 
      <code>
        noindex 
      </code> zoals hierboven beschreven in <span class="uicontrol"> URL's toevoegen of bijwerken </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>URL-maskers opnemen en uitsluiten </p> </td> 
      <td colname="col2"> <p>Geef eenvoudig URL-maskers op: volledig pad, gedeeltelijk pad of paden die gebruikmaken van wilde kaarten of reguliere expressies. </p> <p>De zoekrobot zoekt en indexeert ("include") of negeert ("exclude") documenten op basis van het opgegeven type masker. </p> <p> Bij het indexeren van een site worden de aanwijzingen in volgorde van weergave gevolgd. De volgende lijst met maskers is bijvoorbeeld: </p> <p> 
      <code>
        include https://www.mydomain.com/products/household/lightbulbs*.html 
      </code> </p> <p> 
      <code>
        exclude https://www.mydomain.com/products/ 
      </code> </p> <p>indexeert de pagina's 
      <code>
        lightbulbs1.html 
      </code> en 
      <code>
        lightbulbs2.html 
      </code>. Er worden echter geen andere pagina's geïndexeerd die onder de productmap staan. </p> <p>Een URL-masker dat als eerste wordt weergegeven, heeft altijd voorrang op een masker dat later in de lijst wordt weergegeven. Als de zoekrobot bovendien een document aantreft dat overeenkomt met zowel een include-masker als een exclude-masker, krijgt het masker dat als eerste wordt vermeld voorrang. </p> <p>U kunt ook de trefwoorden gebruiken 
      <code>
        nofollow 
      </code> en 
      <code>
        noindex 
      </code> zoals hierboven beschreven in <span class="uicontrol"> URL's toevoegen of bijwerken </span>. </p> <p>Zie <a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164" type="concept" format="dita" scope="local"> Informatie over URL-maskers</a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Datummaskers opnemen en uitsluiten </p> </td> 
      <td colname="col2"> <p>Geef eenvoudige datummaskers op, zoals een volledig pad, een gedeeltelijk pad of paden die gebruikmaken van wilde kaarten of reguliere expressies. </p> <p>De zoekrobot zoekt en indexeert ("include") of negeert ("exclude") documenten op basis van zowel de URL als de datum van documenten. </p> <p>U kunt de volgende typen datummaskers gebruiken: </p> <p> 
      <ul id="ul_8958ED54C8EF405AA259236595ED3ABA"> 
      <li id="li_0A7841767E004F088CA6FA42E99B9F32"> 
      <code>
        include-days NNN 
      </code> <p>De zoekrobot indexeert alle documenten die overeenkomen met het opgegeven URL-masker en die NNN days of ouder zijn. </p> <p>U kunt het URL-masker volgen met een of meer van de volgende trefwoorden: 
        <ul id="ul_22A38D5F38B344ABB02B16EB1865813B"> 
        <li id="li_B89CC37DC2A1428185E86FFCB9DDB193">nofollow </li> 
        <li id="li_C2579B3A338D4AF987C3F518806734B0">noindex </li> 
        <li id="li_0527BF7103F34B83AC3E684069B899F7">serverdatum </li> 
        </ul> </p> <p>Het volgende masker bevat bijvoorbeeld alle documenten in de map /archive/support die 0 dagen of ouder zijn: </p> <p> 
        <code>
          include-days 0 https://www.mydomain.com/archive/support/ 
        </code> </p> </li> 
      <li id="li_7663ABED40DD4E159F746E4F92BB6407"> 
      <code>
        include-date YYYY-MM-DD 
      </code> <p>De zoekrobot indexeert alle documenten die overeenkomen met het opgegeven URL-masker en die even oud of ouder zijn dan de datum JJJJ-MM-DD. </p> <p>U kunt het URL-masker volgen met een of meer van de volgende trefwoorden: </p> <p> 
        <ul id="ul_57BF37A413BB4A4D962863DACE56F395"> 
        <li id="li_88CAB9AB583B4754A5C53478BD1108FF">nofollow </li> 
        <li id="li_999E1CD34FDE4A1B9C332B4AA8C2887D">noindex </li> 
        <li id="li_05646FACF3524D2A9E201A23770E357F"> serverdatum </li> 
        </ul> </p> <p>Het volgende maskervoorbeeld omvat alle documenten in /archive/ omslag gedateerd op of vóór 25 juli 2011: </p> <p> 
        <code>
          include-date 2011-07-25 https://www.mydomain.com/archive/ 
        </code> </p> </li> 
      <li id="li_172692DEDA8744B3AA492701D24C2D80"> 
      <code>
        exclude-days NNN 
      </code> <p>Hiermee kunt u de indexering uitschakelen van alle documenten die overeenkomen met het opgegeven URL-masker en die NNN days of ouder zijn. </p> <p>U kunt het URL-masker optioneel volgen op het trefwoord 
        <code>
          server-date 
        </code>. </p> <p>In het volgende maskervoorbeeld worden alle PDF-bestanden die 90 dagen oud of ouder zijn, van de index uitgesloten: </p> <p> 
        <code>
          exclude-days 90 *.pdf 
        </code> </p> </li> 
      <li id="li_26078517744D4AECBE1351008926CBAE"> 
      <code>
        exclude-date YYYY-MM-DD 
      </code> <p>Hiermee kunt u de indexering uitschakelen van alle documenten die overeenkomen met het opgegeven URL-masker en die zo oud of ouder zijn dan de datum JJJJ-MM-DD. </p> <p>U kunt het URL-masker optioneel volgen op het trefwoord 
        <code>
          server-date 
        </code>. </p> <p>In het volgende maskervoorbeeld worden alle documenten in de map /archive/ die op of vóór 23 april 2004 zijn gedateerd, uitgesloten: </p> <p> 
        <code>
          exclude-date 2004-04-23 https://www.mydomain.com/archive/ 
        </code> </p> </li> 
      </ul> </p> <p>Zie <a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_F4F1F58A646F4A86B8650EC46FDCEF66" type="concept" format="dita" scope="local"> Datummaskers</a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>URL's verwijderen </p> </td> 
      <td colname="col2"> <p>Geef URL's op. </p> <p>De zoekrobot zoekt en verwijdert de opgegeven documenten uit uw zoekindex. Als een opgegeven pagina al in de zoekindex staat, verwijdert de robot deze voordat deze andere pagina's toevoegt of bijwerkt. </p> <p>Dit veld mag alleen document-URL's bevatten en geen maskers. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>URL-maskers zoeken en verwijderen </p> </td> 
      <td colname="col2"> <p>Geef eenvoudige URL-maskers op: volledig pad, gedeeltelijk pad of maskers die gebruikmaken van wilde kaarten of reguliere expressies. </p> <p>Als het opgegeven URL-masker overeenkomt met de pagina's in uw zoekindex, verwijdert de zoekrobot de pagina's voordat deze andere pagina's toevoegt of bijwerkt. Bijvoorbeeld: </p> <p> 
      <code>
        https://www.mydomain.com/products/1998/household/* 
      </code> </p> <p>U kunt ook reguliere expressies gebruiken, zoals in het volgende voorbeeld: </p> <p> 
      <code>
        regexp ^https://www\.mydomain\.com/products/199[567]/.*$ 
      </code> </p> <p>Zie <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Reguliere expressies</a>. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Klik op **[!UICONTROL Save Changes]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Het incrementele indexschema voor een live website instellen {#task_2A46BA189ECC4317A9D5C6E99A336F33}

U kunt de Incrementele frequentie van de Index en de basistijd selecteren die wordt gebruikt om te kruipen en uw stijgende index bij te werken.

De tijd die u selecteert is lokaal volgens de tijdzone die in de Montages van de Rekening wordt gevormd.

Zie [Uw accountinstellingen configureren](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9).

Webservers zullen vaak halverwege de nacht naar beneden gaan voor onderhoud. Als uw server tijdens een geplande indextijd neer is, zal het indexeren proces ontbreken. Zorg ervoor dat u een tijdstip van de dag selecteert waarop uw webserver beschikbaar is.

Het indexschema is alleen van toepassing op uw live index. u kunt gefaseerde indexen niet plannen.

**Het incrementele indexschema voor een live website instellen**

1. Klik in het productmenu op **[!UICONTROL Index]** > **[!UICONTROL Incremental Index]** > **[!UICONTROL Live Schedule]**.
1. Selecteer in de vervolgkeuzelijst **[!UICONTROL Incremental Index Schedule]** op de pagina In de indexeringsfrequentie in uren of minuten.**[!UICONTROL Incrementally Index]**
1. Selecteer in de vervolgkeuzelijst **[!UICONTROL Base Time]** de begintijd wanneer u een nieuwe incrementele index opnieuw wilt genereren.
1. Klik op **[!UICONTROL Save Changes]**.

## Een incrementele index van een actieve of gefaseerde website uitvoeren {#task_9BFB6157F3884B2FAECB7E0E9CA318CB}

Met Incrementele index kunt u &quot;stukken&quot; van uw actieve of gefaseerde website indexeren, zoals een verzameling pagina&#39;s die vaak worden gewijzigd.

**Een incrementele index van een actieve of gefaseerde website uitvoeren**

1. Voer een van de volgende handelingen uit in het menu Product:

   * Klik op **[!UICONTROL Index]** > **[!UICONTROL Incremental Index]** > **[!UICONTROL Live Index]**.

   * Klik op **[!UICONTROL Index]** > **[!UICONTROL Incremental Index]** > **[!UICONTROL Staged Index]**.

1. Klik op **[!UICONTROL Incremental Index Now]**.
1. (Optioneel) Als er indexatiefouten zijn opgetreden, klikt u op **[!UICONTROL View Errors]** om het gekoppelde logboek weer te geven.

## Het incrementele indexlogboek van een live of gefaseerde website weergeven {#task_E668E1F1240C476DAA1CA783DC728232}

Wanneer een actieve incrementele index of een gefaseerde incrementele index voltooid is, kunt u het bijbehorende logboek weergeven om eventuele fouten op te lossen.


U kunt logboeken niet exporteren of opslaan. Het logboek blijft beschikbaar voor weergave totdat de nieuwe index wordt weergegeven.

**Het incrementele indexlogboek van een live of gefaseerde website weergeven**

1. Voer een van de volgende handelingen uit in het menu Product:

   * Klik op **[!UICONTROL Index]** > **[!UICONTROL Incremental Index]** > **[!UICONTROL Live Log]**.

   * Klik op **[!UICONTROL Index]** > **[!UICONTROL Incremental Index]** > **[!UICONTROL Staged Log]**.

1. Voer een of meerdere van de volgende handelingen uit op de logpagina, boven of onder:

   * Gebruik de navigatieopties **[!UICONTROL First]**, **[!UICONTROL Prev]**, **[!UICONTROL Next]**, **[!UICONTROL Last]**, of **[!UICONTROL Go to line]** om door het logboek te bewegen.

   * Gebruik de weergaveopties **[!UICONTROL Errors only]**, **[!UICONTROL Wrap line]** of **[!UICONTROL Show]** om te verfijnen wat u ziet.

