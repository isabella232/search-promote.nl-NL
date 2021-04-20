---
description: Wanneer uw website verandert, kunt u een manuscript of een programma in werking stellen verzoekend dat de onderzoeksrobot een index in werking stelt gebruikend Verre Controle.
solution: Target
title: Over afstandsbediening voor indexering
topic: Index,Site search and merchandising
uuid: 20e230c6-5c1a-4bf4-bff3-b8236d14ab21
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '1042'
ht-degree: 0%

---


# Informatie over afstandsbediening voor indexering{#about-remote-control-for-indexing}

Wanneer uw website verandert, kunt u een manuscript of een programma in werking stellen verzoekend dat de onderzoeksrobot een index in werking stelt gebruikend Verre Controle.

## Afstandsbediening gebruiken voor indexering {#concept_C79B322190E84106A434E5C6D4A4118F}

Het indexeringsverzoek van de afstandsbediening komt typisch uit een manuscript of een programma dat op uw server wordt gevestigd.

De robot voert dezelfde indexeringsstappen uit alsof deze handmatig was gestart in het menu [!DNL Index]. Om een verzoek van de verre controle voor te leggen, vormt u het noodzakelijke wachtwoord en reactietekenreeksen.

## Hoe te om een verre controleverzoek {#section_42FAB2BAB25A4E24BEA69566C6D1C70F} te doen

Als u een verzoek voor een externe besturing wilt indienen, gebruikt u de volgende indelingsvoorbeelden op basis van de locatie van uw datacenter:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Locatie van datacenter </p> </th> 
   <th colname="col2" class="entry"> <p>Voorbeeld </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Londen </p> </td> 
   <td colname="col2"> <p> <code> https://center.lon5.atomz.com/search/cgiindex.tk? <b>sp_a=sp99999999&amp;sp_password=xxxxxx&amp;sp_operation=op</b> </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Noord-Amerika </p> </td> 
   <td colname="col2"> <p> <code> https://center.atomz.com/search/cgiindex.tk? <b>sp_a=sp99999999&amp;sp_password=xxxxxx&amp;sp_operation=op</b> </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Singapore </p> </td> 
   <td colname="col2"> <p> <code> https://center.sin2.atomz.com/search/cgiindex.tk? <b>sp_a=sp99999999&amp;sp_password=xxxxxx&amp;sp_operation=op</b> </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

of

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Tekenreeks en waarde </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_a= sp99999999  </span> </p> </td> 
   <td colname="col2"> <p> Je accountnummer. </p> <p>U kunt uw accountnummer vinden onder <span class="uicontrol"> <b>Instellingen</b> </span> &gt; <span class="uicontrol"> <b>Accountopties</b> </span> &gt; <span class="uicontrol"> <b>Accountinstellingen</b> </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_lines= N  </span> </p> </td> 
   <td colname="col2"> <p>Hiermee kunt u de status van een actieve index horizontaal schuiven. </p> <p> <span class="codeph">  N  </span> is of een positief geheel of  <span class="codeph"> allen  </span>. Als dit een numerieke waarde is, worden de laatste <span class="codeph"> N </span> regels van het corresponderende indexlogbestand opgenomen in het JSON-antwoord. </p> <p>Als de waarde <span class="codeph"> alle </span> is, wordt het volledige dossier teruggekeerd. </p> <p>Als de waarde <span class="codeph"> 0 </span> is, wordt geen logboekinformatie teruggegeven. Deze waarde is de standaardwaarde voor een actieve indexstatusquery. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_operation= op  </span> </p> </td> 
   <td colname="col2"> <p>Hier kunt u een van de volgende indexeringsbewerkingen opgeven die u wilt uitvoeren: </p> <p> 
     <ul id="ul_6CA190AC41694BC293FC7C6BABA629FE"> 
      <li id="li_EFC76E31D47E473F9A56B2EBA8A97CA1"> <span class="codeph"> full_index  </span> <p>De zoekrobot voert een volledige index van uw website uit. </p> </li> 
      <li id="li_A9ACE21718804A21B3DA7B84AB6729D3"> <span class="codeph"> incrementele_index  </span> <p>De zoekrobot voert een incrementele index uit met de configuratie die is ingesteld onder <span class="uicontrol"> <b>Index</b> </span> &gt; <span class="uicontrol"> <b>Incrementele index</b> </span> &gt; <span class="uicontrol"> <b>Configuration</b></span>. </p> </li> 
      <li id="li_722FE409AE454AD48ACE95C4CDC7A00B"> <span class="codeph"> vertical_index  </span> <p>De zoekrobot voert een verticale update uit met behulp van de configuratie die is ingesteld onder <span class="uicontrol"> <b>Index</b> </span> &gt; <span class="uicontrol"> <b>Vertical Update</b> </span> &gt; <span class="uicontrol"> <b>Configuration</b></span>. </p> <p>Zie <a href="../c-about-index-menu/c-about-vertical-updates.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> Verticale update</a>. </p> </li> 
      <li id="li_A40B513CE17043A4925CE3D4DE0B48A4"> <span class="codeph"> script_index  </span> <p>De zoekrobot voert een incrementele index uit met behulp van het tekstbestand dat is opgegeven onder <span class="uicontrol"> <b>Index</b> </span> &gt; <span class="uicontrol"> <b>Scripted Index</b> </span> &gt; <span class="uicontrol"> <b>Configuration</b></span>. </p> </li> 
      <li id="li_A0BC7F1373B14393997BAB7690FD3EF7"> <span class="codeph"> full_staged_index  </span> <p>De zoekrobot voert een volledige gefaseerde index van uw website uit. </p> </li> 
      <li id="li_47753E358457443A95B384A278FACA83"> <span class="codeph"> incrementele_gestaged_index  </span> <p>De zoekrobot voert een incrementele gefaseerde index uit met behulp van de configuratie die is ingesteld onder <span class="uicontrol"> <b>Index</b> </span> &gt; <span class="uicontrol"> <b>Incrementele index</b> </span> &gt; <span class="uicontrol"> <b>Configuration</b></span>. </p> </li> 
      <li id="li_C8B5F8F1208E438ABEFDF9129A6B14A3"> <span class="codeph"> vertical_staged_index  </span> <p>De zoekrobot voert een verticale gefaseerde update uit met behulp van de configuratie die is ingesteld onder <span class="uicontrol"> <b>Index</b> </span> &gt; <span class="uicontrol"> <b>Vertical Update</b> </span> &gt; <span class="uicontrol"> <b>Configuration</b></span>. </p> </li> 
     </ul> </p> <p>Opmerking:  Als u de functie Verticale updates wilt gebruiken, moet u deze mogelijk inschakelen in uw account door uw Adobe-accountvertegenwoordiger of door Adobe Support. </p> <p>Zie <a href="../c-about-index-menu/c-about-vertical-updates.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> Verticale update </a>. </p> <p>U kunt <span class="codeph"> _saved </span> aan om het even welk bovengenoemd <span class="codeph"> sp_operation </span> waarden toevoegen om de onderzoeksrobot te hebben proberen om bewaarde inhoud te gebruiken. U kunt bijvoorbeeld het volgende opgeven: </p> <p> <code class="syntax html"> sp_operation=full_index_saved </code> </p> <p>of </p> <p> <code class="syntax html"> sp_operation=full_staged_index_saved </code> </p> <p>Of u kunt <span class="codeph"> _status </span> aan om het even welk bovengenoemd <span class="codeph"> sp_operation </span> waarden toevoegen om een statusrapport voor de huidige, of meest recente, verrichting te verzoeken. U kunt bijvoorbeeld het volgende opgeven: </p> <p> <code class="syntax html"> sp_operation=full_index_status </code> </p> <p>of </p> <p> <code class="syntax html"> sp_operation=full_staged_index_status </code> </p> <p>en de resultaten worden geretourneerd als een JSON-object. Neem <span class="codeph"> sp_lines=N </span> op om N-regels van het gekoppelde logbestand op te nemen. Als N negatief is, worden de laatste lijnen van N inbegrepen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_operation= push live  </span> </p> </td> 
   <td colname="col2"> <p> Hiermee kunt u live gaan met een gefaseerde index. </p> <p>Elke poging om <span class="codeph"> _saved </span> aan de duw levende verrichting toe te voegen wordt genegeerd. </p> <p>Wanneer u een <span class="codeph"> live </span>-bewerking uitvoert, wordt een teksttekenreeks voor de reactie OK, Priority of Error geretourneerd aan de server. U geeft deze responstekenreeksen op de pagina <span class="wintitle"> Externe besturing </span> op. </p> <p>Zie <a href="../c-about-index-menu/c-about-remote-control-for-indexing.md#task_57C296258404448DA7A5ADC9B7232391" format="dita" scope="local"> Vormende Verre Controle voor het indexeren</a>. </p> <p>Als u live drukt wanneer er geen gefaseerde index is, gebeurt er niets en wordt de antwoordtekenreeks OK geretourneerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_password= xxxxxx  </span> </p> </td> 
   <td colname="col2"> <p>Het wachtwoord voor de afstandsbediening. </p> </td> 
  </tr> 
 </tbody> 
</table>

Met Zoeken worden gegevens geretourneerd in de vorm van een juiste HTTP-reactie. De volledige reactie bestaat uit een HTTP-status, HTTP-antwoordheaders, een lege regel en de antwoordtekenreeks.

Stel dat u de volgende aanvraag voor besturing op afstand uitvoert:

```
https://center.atomz.com/search/cgiindex.tk?sp_a=sp99999999&sp_password=my-password&sp_operation=full_index
```

Hier volgt de reactie van de server:

```
Status: 200 OK 
Content-type: text/plain 
OK
```

Of stel dat u de volgende aanvraag voor de status van de afstandsbediening uitvoert:

```
https://center.atomz.com/search/cgiindex.tk?sp_a=sp99999999&sp_password=my-password&sp_operation=full_index_status
```

De reactie van de server kan er als volgt uitzien:

```
Status: 200 OK 
Content-type: application/json; charset=utf-8 
{ 
    "current_time": "2017-08-27T10:58:58-0700", 
    "start_time": "2017-07-25T16:40:07-0800", 
    "end_time": "2017-07-25T16:40:20-0800", 
    "elapsed_seconds": 13, 
    "elapsed_seconds_fmt": "13s", 
    "state": "finished", 
    "docs_indexed": 3, 
    "depth": 0, 
    "errors": 0, 
    "status": 1, 
    "message": "ok" 
}
```

Om de eerste tien regels van de logboeklijst te krijgen die met deze indexverrichting, samen met zijn status wordt geassocieerd, wordt de volgende vraag gebruikt:

```
https://center.atomz.com/search/cgiindex.tk?sp_a=sp99999999&sp_password=my-password&sp_operation=full_index_status&sp_lines=10
```

De reactie van de server:

```
Status: 200 OK 
Content-type: application/json; charset=utf-8 
{ 
    "current_time": "2017-08-27T10:59:30-0700", 
    "start_time": "2017-07-25T16:40:07-0800", 
    "end_time": "2017-07-25T16:40:20-0800", 
    "elapsed_seconds": 13, 
    "elapsed_seconds_fmt": "13s", 
    "state": "finished", 
    "docs_indexed": 3, 
    "depth": 0, 
    "errors": 0, 
    "offset": 672, 
    "lines": [ 
        "07/25 16:40:07 PST   ======== Starting manual crawl of account sp99999999. ========", 
        "07/25 16:40:08 PST   Loading existing data", 
        "07/25 16:40:08 PST   Downloading entrypoint https://www.atomz.com/", 
        "07/25 16:40:08 PST   Robots.txt exclude mask: https://www.atomz.com/snap", 
        "07/25 16:40:08 PST   Exclude mask: regexp ^https://www.atomz.com/$", 
        "07/25 16:40:08 PST   Include mask: https://www.atomz.com/", 
        "07/25 16:40:08 PST   Downloading https://www.atomz.com/style.css", 
        "07/25 16:40:09 PST   Ignoring https://www.atomz.com/style.css, document type 'text/css'.", 
        "07/25 16:40:09 PST   Downloading https://www.atomz.com/privacy.html", 
        "07/25 16:40:09 PST   Downloading https://www.atomz.com/terms.html" 
    ], 
    "status": 1, 
    "message": "ok" 
}
```

Noteer de waarde `offset`. Deze waarde geeft de positie van de bestandsverschuiving aan in het logbestand waar het lezen is gestopt. Als u de *next* tien regels in het bestand wilt lezen, neemt u in dit voorbeeld `&sp_offset=672` op in het verzoek dat naar de server wordt verzonden.

Met `sp_offset` kunt u effectief door een logbestand bladeren.

Om *last* tien lijnen van het logboek, samen met de status te krijgen, specificeer de telling als negatief aantal. Geef bijvoorbeeld `sp_lines=` op met de waarde `-10`, zoals in het volgende voorbeeld:

```
https://center.atomz.com/search/cgiindex.tk?sp_a=sp99999999&sp_password=my-password&sp_operation=full_index_status&sp_lines=-10
```

De reactie van de server:

```
Status: 200 OK 
Content-type: application/json; charset=utf-8 
{ 
    "current_time": "2017-08-27T11:01:14-0700", 
    "start_time": "2017-07-25T16:40:07-0800", 
    "end_time": "2017-07-25T16:40:20-0800", 
    "elapsed_seconds": 13, 
    "elapsed_seconds_fmt": "13s", 
    "state": "finished", 
    "docs_indexed": 3, 
    "depth": 0, 
    "errors": 0, 
    "lines": [ 
        "07/25 16:40:20 PST   End Time: 07/25/2017 16:40:20 PST", 
        "07/25 16:40:20 PST   Elapsed Time: 13 seconds", 
        "07/25 16:40:20 PST   Pages Crawled: 3 pages", 
        "07/25 16:40:20 PST   Pages Indexed: 3 pages", 
        "07/25 16:40:20 PST   Words/Bytes Indexed: 2373 words/ 20618 bytes", 
        "07/25 16:40:20 PST   Errors: 0", 
        "07/25 16:40:20 PST   *** Index Summary ***", 
        "07/25 16:40:20 PST   Total Pages: 3", 
        "07/25 16:40:20 PST   --------------------------------------------------------------------", 
        "07/25 16:40:20 PST   ======== Finish manual crawl of account sp99999999: Done. ========" 
    ], 
    "status": 1, 
    "message": "ok" 
}
```

Er wordt hier geen `offset`-waarde geretourneerd, aangezien deze bewerking aan het einde van het bestand is voltooid en er geen regels meer zijn om te lezen.

## Het vormen Verre Controle voor het indexeren {#task_57C296258404448DA7A5ADC9B7232391}

Wanneer uw website verandert, kunt u de Controle van de Verre gebruiken om een manuscript of een programma van uw server in werking te stellen, verzoekend dat de onderzoekersrobot een index in werking stelt.

**Om Verre Controle voor het indexeren te vormen**

1. Klik in het productmenu op **[!UICONTROL Index]** > **[!UICONTROL Remote Control]**.
1. Stel op de pagina [!DNL Remote Control] elke optie voor het configuratieveld zo in dat een indexeringsverzoek van uw server automatisch kan worden verzonden om uw website te indexeren.

   <table> 
    <thead> 
    <tr> 
    <th colname="col1" class="entry"> <p>Option </p> </th> 
    <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
    </tr> 
    </thead>
    <tbody> 
    <tr> 
    <td colname="col1"> <p>Wachtwoord voor afstandsbediening </p> </td> 
    <td colname="col2"> <p>Geef het wachtwoord voor de afstandsbediening op. </p> <p> Wachtwoorden zijn hoofdlettergevoelig, hebben ten minste zes tekens en moeten ten minste één letter bevatten. U wordt aangeraden ten minste één nummer op te nemen. </p> <p>Gebruik geen aanmeldingswachtwoord voor het zoeken/verhandelen van uw site. </p> <p>Uw wachtwoord wordt gebruikt in elke aanvraag voor een afstandsbediening. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>REACTIE-tekenreeks OK </p> </td> 
    <td colname="col2"> <p>Hier geeft u een teksttekenreeks op met een OK-antwoord als de gevraagde indexbewerking is geslaagd. In dergelijke gevallen retourneert de zoekrobot de antwoordtekenreeks OK aan de server. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>Reactiereeks prioriteit </p> </td> 
    <td colname="col2"> <p>Als een andere indexeringsbewerking wordt uitgevoerd op het moment dat de externe aanvraag wordt ingediend, kan de zoekrobot de gevraagde index niet uitvoeren. In dergelijke gevallen wordt de tekenreeks voor de prioritaire reactie geretourneerd aan de server. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>Respons fout </p> </td> 
    <td colname="col2"> <p>Hier geeft u een tekstreeks met foutreacties op. Als uw wachtwoord onjuist is of als er een andere fout optreedt. In dergelijke gevallen retourneert de zoekrobot de antwoordtekenreeks Error weer naar de server. </p> </td> 
    </tr> 
    </tbody> 
    </table>

1. Klik op **[!UICONTROL Save Changes]**.
