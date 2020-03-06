---
description: Wanneer uw website verandert, kunt u een manuscript of een programma in werking stellen verzoekend dat de onderzoeksrobot een index in werking stelt gebruikend Verre Controle.
seo-description: Wanneer uw website verandert, kunt u een manuscript of een programma in werking stellen verzoekend dat de onderzoeksrobot een index in werking stelt gebruikend Verre Controle.
seo-title: Informatie over afstandsbediening voor indexering
solution: Target
title: Informatie over afstandsbediening voor indexering
topic: Index,Site search and merchandising
uuid: 20e230c6-5c1a-4bf4-bff3-b8236d14ab21
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a

---


# Informatie over afstandsbediening voor indexering{#about-remote-control-for-indexing}

Wanneer uw website verandert, kunt u een manuscript of een programma in werking stellen verzoekend dat de onderzoeksrobot een index in werking stelt gebruikend Verre Controle.

## Het gebruiken van Verre Controle voor het Indexeren {#concept_C79B322190E84106A434E5C6D4A4118F}

Het verre controle indexerende verzoek komt typisch uit een manuscript of een programma dat op uw server wordt gevestigd.

De robot voert de zelfde het indexeren stappen uit alsof het manueel van het [!DNL Index] menu was begonnen. Om een ver controleverzoek voor te leggen, vormt u de noodzakelijke wachtwoord en reactiekoorden.

## Hoe te om een ver controleverzoek te maken {#section_42FAB2BAB25A4E24BEA69566C6D1C70F}

Om een verzoek van de verre controle te maken, gebruik de volgende formaatvoorbeelden die op de plaats van uw gegevenscentrum worden gebaseerd:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Datacenterlocatie </p> </th> 
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
   <th colname="col1" class="entry"> <p>Koord en waarde </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_a= sp9999999 </span> </p> </td> 
   <td colname="col2"> <p> Je rekeningnummer. </p> <p>U kunt uw rekeningnummer vinden onder <span class="uicontrol"> Instellingen <b></b> &gt; </span> Accountopties-opties <span class="uicontrol"> <b>&gt;</b> </span> <span class="uicontrol"> <b></b> </span>Accountinstellingen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_lines= N </span> </p> </td> 
   <td colname="col2"> <p>Laat u controleren het statuut van een lopende index kruipt. </p> <p> <span class="codeph">  N </span> is of een positief geheel of <span class="codeph"> allen </span>. Als dit een numerieke waarde is, zijn de laatste <span class="codeph"> N </span> lijnen van het overeenkomstige dossier van het indexlogboek inbegrepen in de reactie JSON. </p> <p>Als de waarde <span class="codeph"> allen is </span>, is het volledige dossier teruggekeerd. </p> <p>Als de waarde <span class="codeph"> 0 is </span>, dan is geen logboekinformatie teruggekeerd. Deze waarde is het gebrek voor een lopende vraag van de indexstatus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_operation= op </span> </p> </td> 
   <td colname="col2"> <p>Laat u één van de volgende het indexeren verrichtingen specificeren die u wilt lopen: </p> <p> 
     <ul id="ul_6CA190AC41694BC293FC7C6BABA629FE"> 
      <li id="li_EFC76E31D47E473F9A56B2EBA8A97CA1"> <span class="codeph"> full_index </span> <p>De zoekrobot voert een volledige index van je website uit. </p> </li> 
      <li id="li_A9ACE21718804A21B3DA7B84AB6729D3"> <span class="codeph"> incrementele_index </span> <p>De onderzoeksrobot stelt een stijgende index in werking gebruikend de configuratie die onder <span class="uicontrol"> Index <b></b> &gt; de </span> Incrementele Index <span class="uicontrol"> &gt; <b></b> </span> <span class="uicontrol"> <b></b></span>Configuratie wordt geplaatst. </p> </li> 
      <li id="li_722FE409AE454AD48ACE95C4CDC7A00B"> <span class="codeph"> vertical_index </span> <p>De onderzoeksrobot stelt een verticale update in werking gebruikend de configuratie die onder <span class="uicontrol"> Index <b></b> &gt; </span> Verticale Update <span class="uicontrol"> &gt; <b></b> </span> <span class="uicontrol"> <b></b></span>Configuratie wordt geplaatst. </p> <p>Zie <a href="../c-about-index-menu/c-about-vertical-updates.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> Verticale update</a>. </p> </li> 
      <li id="li_A40B513CE17043A4925CE3D4DE0B48A4"> <span class="codeph"> script_index </span> <p>De onderzoeksrobot stelt een stijgende index in werking gebruikend het tekstdossier dat onder <span class="uicontrol"> Index <b></b> &gt; </span> Scripted Index <span class="uicontrol"> &gt; <b></b> </span> <span class="uicontrol"> <b></b></span>Configuratie wordt gespecificeerd. </p> </li> 
      <li id="li_A0BC7F1373B14393997BAB7690FD3EF7"> <span class="codeph"> full_staged_index </span> <p>De zoekrobot voert een volledig gefaseerde index van je website uit. </p> </li> 
      <li id="li_47753E358457443A95B384A278FACA83"> <span class="codeph"> incrementele_gefaseerde_index </span> <p>De onderzoeksrobot stelt een stijgende gefaseerde index in werking gebruikend de configuratie die onder <span class="uicontrol"> Index <b></b> &gt; </span> Incremental Index <span class="uicontrol"> &gt; <b></b> </span> <span class="uicontrol"> <b></b></span>Configuratie wordt geplaatst. </p> </li> 
      <li id="li_C8B5F8F1208E438ABEFDF9129A6B14A3"> <span class="codeph"> vertical_staged_index </span> <p>De onderzoeksrobot stelt een verticale gefaseerde update in werking gebruikend de configuratie die onder <span class="uicontrol"> Index <b></b> &gt; </span> Verticale Update <span class="uicontrol"> &gt; <b></b> </span> <span class="uicontrol"> <b></b></span>Configuratie wordt geplaatst. </p> </li> 
     </ul> </p> <p>Opmerking:  Om Verticale Updates te gebruiken, kunt u het moeten hebben toegelaten in uw rekening door uw de rekeningsvertegenwoordiger van Adobe of door de Steun van Adobe. </p> <p>Zie <a href="../c-about-index-menu/c-about-vertical-updates.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> over Verticale update </a>. </p> <p>U kunt <span class="codeph"> _saved </span> aan om het even welke bovengenoemde <span class="codeph"> sp_operation </span> waarden toevoegen om de onderzoeksrobot te hebben proberen om bewaarde inhoud te gebruiken. Bijvoorbeeld, kon u het volgende specificeren: </p> <p> <code class="syntax html"> sp_operation=full_index_saved </code> </p> <p>of </p> <p> <code class="syntax html"> sp_operation=full_staged_index_saved </code> </p> <p>Of, u kunt <span class="codeph"> _status </span> aan om het even welke bovengenoemde <span class="codeph"> sp_operation </span> waarden toevoegen om een statusrapport voor de huidige, of meest recente, verrichting te verzoeken. Bijvoorbeeld, kon u het volgende specificeren: </p> <p> <code class="syntax html"> sp_operation=full_index_status </code> </p> <p>of </p> <p> <code class="syntax html"> sp_operation=full_staged_index_status </code> </p> <p>en de resultaten zijn teruggekeerd als voorwerp JSON. Omvat <span class="codeph"> sp_lines=N </span> om de lijnen van N van het bijbehorende logboekdossier te omvatten. Als N negatief is, zijn de laatste lijnen van N inbegrepen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_operation= handlive </span> </p> </td> 
   <td colname="col2"> <p> Laat u ver duwen levende een gefaseerde index. </p> <p>Om het even welke poging om <span class="codeph"> _saved </span> aan de duw levende verrichting toe te voegen wordt genegeerd. </p> <p>Wanneer u een <span class="codeph"> buig levende </span> verrichting in werking stelt O.K., Prioriteit, of het koord van de de reactietekst van de Fout is teruggekeerd aan de server. U specificeert deze antwoordkoorden op de <span class="wintitle"> Verre </span> pagina van de Controle. </p> <p>Zie <a href="../c-about-index-menu/c-about-remote-control-for-indexing.md#task_57C296258404448DA7A5ADC9B7232391" format="dita" scope="local"> het Vormen Verre Controle voor het indexeren</a>. </p> <p>Als u levend duwt wanneer er geen gefaseerde index is, gebeurt niets en het O.K. reactiekoord is teruggekeerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_password= xxxxxx </span> </p> </td> 
   <td colname="col2"> <p>Het wachtwoord voor de afstandsbediening. </p> </td> 
  </tr> 
 </tbody> 
</table>

Het onderzoek keert gegevens in de vorm van een juiste reactie van HTTP terug. De volledige reactie is samengesteld uit een HTTP- status, HTTP- reactiekopballen, een lege lijn, en het reactiekoord.

Bijvoorbeeld, veronderstel dat u het volgende verre controleverzoek uitvoert:

```
https://center.atomz.com/search/cgiindex.tk?sp_a=sp99999999&sp_password=my-password&sp_operation=full_index
```

Het volgende is de reactie van de server:

```
Status: 200 OK 
Content-type: text/plain 
OK
```

Of, veronderstel dat u het volgende verzoek van de verre controlestatus uitvoert:

```
https://center.atomz.com/search/cgiindex.tk?sp_a=sp99999999&sp_password=my-password&sp_operation=full_index_status
```

De reactie van de server zou als het volgende kunnen kijken:

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

Om de eerste tien lijnen van de logboeklijst te krijgen die met deze indexverrichting, samen met zijn status wordt geassocieerd, wordt de volgende vraag gebruikt:

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

Noteer de `offset` waarde. Deze waarde identificeert de dossier-compensatie positie in het logboekdossier waar het lezen verliet. Om de *volgende* tien lijnen in het dossier te lezen, zou u, in dit voorbeeld, `&sp_offset=672` in het verzoek omvatten dat naar de server wordt verzonden.

Gebruikend `sp_offset`, kunt u effectief door een logboekdossier pagineren.

Om de *laatste* tien lijnen van het logboek, samen met de status te krijgen, specificeer de telling als negatief aantal. Bijvoorbeeld, specificeer `sp_lines=` met een waarde van `-10` zoals in het volgende:

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

Merk op dat er geen hier teruggekeerde waarde is, aangezien deze verrichting aan het eind van het dossier beëindigde, en er niet meer te lezen lijnen zijn. `offset`

## Vormende Verre Controle voor het indexeren {#task_57C296258404448DA7A5ADC9B7232391}

Wanneer uw website verandert, kunt u Afstandsbediening gebruiken om een manuscript of een programma van uw server in werking te stellen, verzoekend dat de onderzoeksrobot een index in werking stelt.

**Om Verre Controle voor het indexeren te vormen**

1. Klik in het productmenu op **[!UICONTROL Index]** > **[!UICONTROL Remote Control]**.
1. Voor de [!DNL Remote Control] pagina, plaats elke optie van het configuratiegebied om een indexerend verzoek van uw server automatisch te kunnen voorleggen om uw website te indexeren.

   <table> 
    <thead> 
    <tr> 
    <th colname="col1" class="entry"> <p>Optie </p> </th> 
    <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
    </tr> 
    </thead>
    <tbody> 
    <tr> 
    <td colname="col1"> <p>Wachtwoord voor afstandsbediening </p> </td> 
    <td colname="col2"> <p>Specificeer het verre controlewachtwoord. </p> <p> De wachtwoorden zijn hoofdlettergevoelig, minstens zes lange karakters, en moeten minstens één brief omvatten. Het is raadzaam om ook ten minste één nummer op te nemen. </p> <p>Gebruik uw wachtwoord voor aanmelding bij het zoeken naar/verkopen van sites niet. </p> <p>Uw wachtwoord wordt gebruikt in elk verzoek van de verre controle. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>OK-antwoordenreeks </p> </td> 
    <td colname="col2"> <p>Laat u een O.K. koord van de reactietekst specificeren als de gevraagde indexverrichting met succes begint. In dergelijke gevallen, keert de onderzoeksrobot uw O.K. reactiekoord aan de server terug. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>String voor prioritaire respons </p> </td> 
    <td colname="col2"> <p>Als een andere indexerende verrichting lopend is wanneer het verre verzoek wordt gedaan, kan de onderzoeksrobot niet de gevraagde index uitvoeren. In dergelijke gevallen, is uw Prioritaire koord van de reactietekst teruggekeerd aan de server. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>Foutresponskoord </p> </td> 
    <td colname="col2"> <p>Laat u een koord van de reactietekst van de Fout specificeren als uw wachtwoord onjuist is, of als een andere fout voorkomt. In dergelijke gevallen, keert de onderzoeksrobot uw het reactiekoord van de Fout terug naar de server terug. </p> </td> 
    </tr> 
    </tbody> 
    </table>

1. Klik op **[!UICONTROL Save Changes]**.
