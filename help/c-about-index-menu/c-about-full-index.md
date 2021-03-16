---
description: Met Volledige index kunt u alle pagina's van uw gefaseerde of live website indexeren. Indexering helpt uw klanten gemakkelijker te vinden wat zij zoeken of wat zij wanneer zij een onderzoek uitvoeren nodig hebben.
solution: Target
subtopic: Full Index
title: Info over Volledige index
topic: Index, zoeken en verhandelen van sites
uuid: dce1eafd-5aea-4945-8305-8f9e7dc392df
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 0%

---


# Info over Volledige index{#about-full-index}

Met Volledige index kunt u alle pagina&#39;s van uw gefaseerde of live website indexeren. Indexering helpt uw klanten gemakkelijker te vinden wat zij zoeken of wat zij wanneer zij een onderzoek uitvoeren nodig hebben.

## Volledige index {#concept_C69BD21863FD4856B49326F35DB570D3} gebruiken

Wanneer u een volledige index genereert, wordt statusinformatie weergegeven, zoals begintijd, verstreken tijd en fouten tijdens het indexeringsproces. Er wordt ook informatie weergegeven over de status van de laatste index.

Als u een account-instelling hebt gewijzigd waarvoor een index opnieuw moet worden gegenereerd, wordt in de status mogelijk &quot;Regenerating&quot; weergegeven. Tijdens het opnieuw genereren worden accountinstellingen toegepast om een bijgewerkte site-index te maken.

U kunt het indexeringsproces op elk gewenst moment stoppen of opnieuw starten.

Terwijl de nieuwe index is gemaakt voor een live website, kunnen klanten uw site blijven doorzoeken met behulp van uw laatste index. Er wordt ook informatie weergegeven over de status van de laatste index.

## Het volledige indexschema voor een live website instellen {#task_6760F3256D004A228B38968DF15421F0}

U kunt de tijd en de dagen opgeven waarop u uw website wilt kruipen en de index wilt bijwerken.

De tijd die u selecteert is lokaal volgens de tijdzone die in de Montages van de Rekening wordt gevormd.

Zie [Uw accountinstellingen configureren](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9).

Webservers zullen vaak halverwege de nacht naar beneden gaan voor onderhoud. Als uw server tijdens een geplande indextijd neer is, zal het indexeren proces ontbreken. Zorg ervoor dat u een tijdstip van de dag selecteert waarop uw webserver beschikbaar is.

Het indexschema is alleen van toepassing op uw live index. u kunt gefaseerde indexen niet plannen.

**Het volledige indexschema voor een live website instellen**

1. Klik in het productmenu op **[!UICONTROL Index]** > **[!UICONTROL Full Index]** > **[!UICONTROL Live Schedule]**.
1. Selecteer in de vervolgkeuzelijst **[!UICONTROL Time]** het uur waarop u de volledige indexering wilt starten.
1. Selecteer een of meer dagen waarop u de volledige indexering wilt uitvoeren.
1. Klik op **[!UICONTROL Save Changes]**.

## Een volledige index van een actieve of gefaseerde website uitvoeren {#task_F7FE04D8A1654A7787FCCA31B45EB42D}

Met Volledige index kunt u alle pagina&#39;s van uw gefaseerde of live website indexeren. Indexering helpt uw klanten gemakkelijker te vinden wat zij zoeken of wat zij wanneer zij een onderzoek uitvoeren nodig hebben.

**Een volledige index van een actieve of gefaseerde website uitvoeren**

1. Voer een van de volgende handelingen uit in het menu Product:

   * Klik op **[!UICONTROL Index]** > **[!UICONTROL Full Index]** > **[!UICONTROL Live Index]**.

   * Klik op **[!UICONTROL Index]** > **[!UICONTROL Full Index]** > **[!UICONTROL Staged Index]**.

1. Stel de gewenste indexeringsopties in.

   <table> 
    <thead> 
    <tr> 
    <th colname="col1" class="entry"> <p>Option </p> </th> 
    <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
    </tr> 
    </thead>
    <tbody> 
    <tr> 
    <td colname="col1"> <p>Indexcache wissen </p> </td> 
    <td colname="col2"> <p>Hiermee worden alle documenten verwijderd uit de indexcache. </p> <p>Als deze optie is geselecteerd, wordt elke websitepagina gedownload van uw server. Als deze instelling is ingeschakeld en uitgeschakeld, wordt de cache van uw account gewist telkens wanneer een volledige index wordt uitgevoerd. Voor sommige eerder gewijzigde accountinstellingen is nu een volledige index vereist. </p> <p>Als deze optie is uitgeschakeld, blijven alle geïndexeerde pagina's in de index totdat de webserver zegt dat de pagina niet meer bestaat. Deze situatie geldt ook als koppelingen naar die pagina worden verwijderd. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>Regenereren in wachtrij </p> </td> 
    <td colname="col2"> <p>Selecteer Als u wijzigingen hebt aangebracht in uw accountinstellingen die de inhoud van uw index aanzienlijk hebben gewijzigd. Voorbeelden van belangrijke wijzigingen zijn het aanbrengen van wijzigingen in: 
    <ul id="ul_4EB8FF692FEB47BBB9A64D61299380D1"> 
    <li id="li_7CF8D286512F4210BEA3DB9F0EFA097A">Synoniemen </li> 
    <li id="li_8178ABC342BB4365B3927E20433756E3">Verzamelingen </li> 
    <li id="li_57C8BD06BFA64AFAA2C9EF2CC59520EF">Metagegevens </li> 
    <li id="li_C4B6A7DA023B4A43991D03EC592170C9">Uitgesloten woorden </li> 
    <li id="li_9E0AD4B6DDC24A5A8FB5C2C1CCD5348A">Accounttaal </li> 
    <li id="li_338F107547DF48AAA0EF90F4AD8664A5">Rangorde </li> 
    <li id="li_7F49B86D94974E79AAD381A64A1400F2">Hoofdlettergevoelig zoeken in-/uitschakelen </li> 
    <li id="li_E8FE6EE240A840AC826ADF4294AAC6F6">Diakritische ondersteuning in-/uitschakelen </li> 
    <li id="li_51763D482DCB4ED0972966F492B8C0F2">Nummerindexering in-/uitschakelen </li> 
    </ul> </p> <p>Voordat een andere kruipt plaatsvindt, worden alle indexgegevens snel doorgegeven om ervoor te zorgen dat deze voldoen aan de nieuwe accountinstellingen. </p> <p>Deze optie is alleen beschikbaar als u een volledige index van een gefaseerde website uitvoert. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>Alle pagina's tellen </p> </td> 
    <td colname="col2"> <p>Hiermee kunt u door de pagina's van websites bladeren, zelfs nadat u de paginalimiet voor uw account hebt bereikt. </p> <p>Er worden geen extra pagina's toegevoegd aan de index, maar u kunt wel het totale aantal documenten op uw website controleren. </p> </td> 
    </tr> 
    </tbody> 
    </table>

1. Klik op **[!UICONTROL Full Index Now]**.
1. (Optioneel) Als er indexatiefouten zijn opgetreden, klikt u op **[!UICONTROL View Errors]** om het gekoppelde logboek weer te geven.

## Het volledige indexlogboek van een live of gefaseerde website weergeven {#task_02E5E944C56B4EB19CC1FF321F3221B8}

Wanneer een levende volledige index of een gefaseerde volledige index volledig is, kunt u zijn bijbehorend logboek bekijken om het even welke fouten problemen op te lossen die voorkwamen.

U kunt logboeken niet exporteren of opslaan. Het logboek blijft beschikbaar voor weergave totdat de nieuwe index wordt weergegeven.

**Het volledige indexlogboek van een live of gefaseerde website weergeven**

1. Voer een van de volgende handelingen uit in het menu Product:

   * Klik op **[!UICONTROL Index]** > **[!UICONTROL Full Index]** > **[!UICONTROL Live Log]**.

   * Klik op **[!UICONTROL Index]** > **[!UICONTROL Full Index]** > **[!UICONTROL Staged Log]**.

1. Voer een of meerdere van de volgende handelingen uit op de logpagina, boven of onder:

   * Gebruik de navigatieopties **[!UICONTROL First]**, **[!UICONTROL Prev]**, **[!UICONTROL Next]**, **[!UICONTROL Last]**, of **[!UICONTROL Go to line]** om door het logboek te bewegen.

   * Gebruik de weergaveopties **[!UICONTROL Errors only]**, **[!UICONTROL Wrap line]** of **[!UICONTROL Show]** om te verfijnen wat u ziet.

