---
description: Gebruik het Filtrerende menu om manuscripten te gebruiken die de inhoud van een Webdocument veranderen alvorens het wordt geïndexeerd.
seo-description: Gebruik het Filtrerende menu om manuscripten te gebruiken die de inhoud van een Webdocument veranderen alvorens het wordt geïndexeerd.
seo-title: Ongeveer het Filtreren menu
solution: Target
subtopic: Filtering
title: Ongeveer het Filtreren menu
topic: Settings,Site search and merchandising
uuid: ebb08fa8-4e17-417d-868b-11fc2af9f284
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a

---


# Ongeveer het Filtreren menu{#about-the-filtering-menu}

Gebruik het Filtrerende menu om manuscripten te gebruiken die de inhoud van een Webdocument veranderen alvorens het wordt geïndexeerd.

## Over filteren script {#concept_E56B73D625854AB2A899EF2D56CFCB47}

U kunt gebruiken [!DNL Filtering Script] om de inhoud van een document van het Web te veranderen alvorens het wordt geïndexeerd.

U kunt de markeringen van HTML opnemen, irrelevante inhoud verwijderen, en zelfs nieuwe meta-gegevens van HTML tot stand brengen die op URL van een document, MIME type, en bestaande inhoud worden gebaseerd. Het het filtreren manuscript is een Perl manuscript, dat krachtige koord behandeling en de flexibiliteit van regelmatige uitdrukking aanpassing verstrekt. U gebruikt het filtrerende manuscript met een initialiseringsmanuscript, beëindigingsmanuscript, URL maskermanuscript, en test URL.

Het filtrerende manuscript wordt in werking gesteld telkens als een document van uw website wordt gelezen. Het manuscript loopt als standaardfilter, met andere woorden, leest gegevens van STDIN, transformeert die gegevens op één of andere manier, en schrijft de resultaten aan STDOUT. U kunt het het filtreren manuscript gebruiken om statusberichten van het het filtreren manuscript aan het indexlogboek te drukken. U of druk de berichten aan STDERR, of als `_search_debug_log()` subroutine.

Sommige opties van de afscheiding van GNU die u kunt gebruiken terwijl op **[!UICONTROL Expert (diff)]** wijze op de Gelaagde het Filtreren pagina van het Manuscript, omvatten het volgende:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>GNU-afdiff, optie </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -b </span> </p> </td> 
   <td colname="col2"> <p> Negeert veranderingen in hoeveelheid witte ruimte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -B </span> </p> </td> 
   <td colname="col2"> <p> Negeert veranderingen die opnemen of lege lijnen schrappen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -c </span> </p> </td> 
   <td colname="col2"> <p> Gebruikt het formaat van de contextoutput, tonend drie lijnen van context. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -C-lijnen </span> </p> </td> 
   <td colname="col2"> <p> Gebruikt het formaat van de contextoutput, tonend lijnen (een geheel) van context, of drie als de lijnen niet worden gegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -i </span> </p> </td> 
   <td colname="col2"> <p> negeert veranderingen in het geval; overweeg in hoofdletters en kleine letters equivalent. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -f </span> </p> </td> 
   <td colname="col2"> <p> Maakt output die als een ed manuscript gelijkaardig kijkt maar veranderingen in de orde heeft dat zij in het dossier verschijnen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -n </span> </p> </td> 
   <td colname="col2"> <p> RCS-formaat van de output verschilt; als <span class="codeph"> - f </span> behalve dat specificeert elk bevel het aantal lijnen die worden beïnvloed. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>-u </p> </td> 
   <td colname="col2"> <p> Gebruikt het verenigde outputformaat, dat drie lijnen van context toont. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -U-lijnen </span> </p> </td> 
   <td colname="col2"> <p> Gebruikt het verenigde outputformaat, tonend lijnen (een geheel) van context, of drie als de lijnen niet worden gegeven. </p> </td> 
  </tr> 
 </tbody> 
</table>

U kunt lokale variabelen, globale variabelen, of allebei in deze manuscripten gebruiken. Alle globale variabelen worden geprefacteerd met namespace &quot;belangrijkste::&quot;. Wanneer het het filtreren manuscript is begonnen, bevat zijn milieu de volgende standaarddossierhandvatten:

* STDIN - niets (keert onmiddellijk EOF terug wanneer gelezen)
* STDOUT - vervangingsHTML (als het gegeven aan STDOUT wordt gedrukt, wordt het gebruikt in plaats van het oorspronkelijke document)
* STDERR - de gegevens die aan STDERR worden gedrukt zijn gedrukt gedrukt aan het Logboek van de Index als fout

Bovendien, kunt u douaneberichten aan het indexlogboek schrijven gebruikend de `_search_debug_log()` subroutine, zoals in het volgende voorbeeld:

```
# Log information to the Index Log 
_search_debug_log("Done processing document: " . $main::search_url);
```

Deze berichten verschijnen met het woord `DEBUG` als voorwoord, en niet geregistreerd als fouten.

Het volgende is een voorbeeld van het filtreren. De `<title>` gebieden van de Web-pagina beginnen vaak met de bedrijfnaam. Hoewel deze informatie nuttig is voor plaatsnavigatie doeleinden, is het niet relevant wanneer het zoeken. Als de titels van alle Web-pagina&#39;s MegaCorp met een gemeenschappelijk koord, zoals het volgende beginnen:

```
<title>MegaCorp -- meaningful title 
here</title>
```

U zou &quot; `MegaCorp --`&quot;uit het begin van elke documenttitel moeten verwijderen en elk document tellen dat met het het filtreren manuscript wordt verwerkt. Om dit te doen, kunt u het volgende manuscript gebruiken:

```
# Make sure this is an HTML document. 
if ($main::ws_content_type =~ /^text\/html/) { 
    # Read the entire document into a local scalar variable. 
    my @docarray = <>; 
    my $doc = join("", @docarray); 
 
    # Remove "MegaCorp -- " from the title. 
    $doc =~ s/(<TITLE>)MegaCorp -- /$1/gis; 
 
    # Print the resulting document. 
    print $doc; 
 
    # Count that we've filtered one more document. 
    $main::doc_count++; 
}
```

## Globale variabelen {#global-variables}

U kunt de volgende variabelen in om het even welk het filtreren manuscript gebruiken:

| Variabel | Beschrijving |
|--- |--- |
| `$main::search_crawl_type` | De waarde van `$main::search_crawl_type` wijst op het type van indexverrichting lopend.  Afgekeurde vorm: `$main::ws_crawl_type` De indexverrichtingen en de bijbehorende waarden omvatten het volgende: <ul><li>Volledige index: Handmatig - `manual`</li><li>Volledige index: Gepland - `auto`</li><li>Volledige index: Afstandsbediening - `CGI`</li><li>Incrementele index: Handmatig - `manual-incremental`</li><li>Incrementele index: Gepland - `auto-incremental` </li><li>Incrementele index: Afstandsbediening - `CGI-incremental`</li><li>Scripted Index: Handmatig - `manual-indexlist.txt` </li><li>Scripted Index: Gepland - `auto-indexlist.txt`</li><li>Scripted Index: Afstandsbediening - `CGI-indexlist.txt`</li><li>Regenereren - `manual-upgrade`</li></ul> |
| `$main::search_clear_cache` | De waarde wijst erop of het &quot;Duidelijke indexgeheime voorgeheugen&quot;indexerende optie voor de huidige indexverrichting werd gevraagd. Als &quot;Duidelijk indexgeheime voorgeheugen&quot;werd gevraagd, is de waarde van &quot; `$main::search_clear_cache` `1`&quot;.  Afgekeurde vorm: `$main::ws_clear_cache` |
| `$main::search_fields` | De waarde bevat een lusje-gescheiden lijst van de meta-gegevensgebieden die in de rekening worden bepaald. Door gebrek, is de waarde:   `url title desc keys target body alt date charset language` Afgekeurde vorm: `$main::ws_fields` |
| `$main::search_collections` | De waarde bevat een tab-gescheiden lijst van de Inzamelingen die in de rekening worden bepaald.  Afgekeurde vorm: `$main::ws_collections` |
| `$main::search_url` | De waarde is volledig - gekwalificeerde URL van het document.  Afgekeurde vorm: `$main::ws_url` |
| `$main::search_content_type` | De waarde is het inhoud-type van het document zoals die van de http-equiv meta markering wordt gehaald. Een typische waarde is &quot;tekst/html; charset=iso-8859-1&quot;.  Afgekeurde vorm: `$main::ws_content_type` |
| `$main::search_content_class` | De waarde is de inhoudsklasse van het document, zoals die uit het tevreden-type gebied wordt afgeleid.  Afgekeurde vorm: `$main::ws_content_class` |
| `$main::search_syntax_check` | De waarde wijst op het gebruik van de knoop van de &quot;Syntaxis van de Controle&quot;. Indien geklikt, is de waarde 1 (één); anders, is zijn waarde 0 (nul).  Afgekeurde vorm: `$main::ws_syntax_check` |
| `$main::search_last_mod_date` | Indien verstrekt door de Webserver, bevat deze waarde de vertegenwoordiging van de Epoch (seconden sinds 1 Januari, 1970) van de laatste gewijzigde datum van het document.  U kunt deze waarde formatteren door de Perl localtime() bibliotheekaanroep te gebruiken. |

### Snelle tips {#section_89A5C16911744AF98E232DF608C6A1F5}

* Alle globale variabelen worden geprefacteerd met namespace &quot;belangrijkste:&quot;: `$main::doc_count = 0;`
* Alle lokale variabelen worden gedeclareerd met &quot;my&quot;: `my $i = 0;`
* De subroutines worden bepaald in het initialiseringsmanuscript. Zij hebben geen expliciete &quot;leiding nodig:&quot;namespace: `sub my_sub {`  `...`

   `}`

* Test `$main::search_content_type` alvorens u veranderingen in een dossier aanbrengt. Het testen kan u helpen vermijden makend onzorgvuldige veranderingen in binaire dossiers, zoals Swf- dossiers of Pdf- dossiers:

   `if ($main::search_content_type =~ /^text\/html/) { ...`

* De `$main::search_content_type` is de volledige tevreden-Type kopbal die door uw server wordt geleverd. Het kan een eenvoudig type MIME, zoals &quot;tekst/html&quot;soms bevatten. Of, kan het een MIME type bevatten dat door andere informatie wordt gevolgd, zoals het karakter van het document - reeks het coderen, zoals &quot;tekst/html; charset=iso-8859-1&quot;.
* Voor elk type van niet-HTML- document, `$main::search_content_type` kan diverse waarden nemen. Het testen voor elke waarde in uw manuscript wordt omslachtig. Bijvoorbeeld, hebben sommige documenten van Word inhoudstype waarden van &quot;toepassing/msword&quot;, &quot;application/vnd.ms-woord&quot;of &quot;application/x-msword&quot;. In dergelijke gevallen, `$main::search_content_class` kan de volgende waarden nemen:

   * html
   * pdf
   * woord
   * uitblinken
   * powerpoint
   * mp3
   * tekst

* In het voorbeeld, zou het testen `$main::search_content_class` voor &quot;woord&quot;om het even welke drie mogelijke tevreden-type waarden aanpassen.
* Als niets aan STDOUT van het het filtreren manuscript wordt gedrukt, dan wordt het document gebruikt precies aangezien het werd gedownload. Namelijk als u te hoeven om niets in een document te veranderen, dan te hoeven u niet om STDIN aan STDOUT voor dat document te kopiëren.
* Als u alle tekst uit een document wilt verwijderen, druk een geldig dossier STDOUT. Bijvoorbeeld, om al tekst uit een HTML- document volledig te verwijderen, doet u het volgende: `print "<html></html>";`

## Een filterscript toevoegen {#task_0AB84FD1133F47F9AA069A79BEA13A22}

Het het filtreren manuscript is een manuscript Perl dat voor elk document in werking wordt gesteld dat van uw website wordt gedownload.

U gebruikt het filtrerende manuscript samen met een initialiseringsmanuscript, beëindigingsmanuscript, en URL maskermanuscript.

Zeker ben dat u uw plaatsindex herbouwt zodat de resultaten van uw het filtreren manuscript aan uw klanten zichtbaar zijn.

Zie [het Vormen van een stijgende index van een gefaseerde website](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Om een filtrerend manuscript toe te voegen**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Filtering]** > **[!UICONTROL Filtering Script]**.
1. (Facultatief) op de [!DNL Filtering Script] pagina, op het [!DNL Test URL] gebied, ga URL van een document op uw website in.

   Klik een het testen optie om veranderingen in de ruwe HTML- tekst te zien.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Optie </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>URL-veld testen </p> </td> 
      <td colname="col2"> <p>Laat u URL van een document op uw website ingaan. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Test </p> </td> 
      <td colname="col2"> <p>Tests URL tegen de het filtreren manuscripten en maskers URL. </p> <p>Het testURL document wordt gedownload, dat dan als input STDIN aan het het filtreren manuscript wordt gebruikt. De initialisering, het filtreren, en de beëindigingsmanuscripten worden dan in werking gesteld. Als er om het even welke output STDOUT van het het filtreren manuscript is, wordt die output getoond in een nieuw browser venster. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Alleen testen </p> </td> 
      <td colname="col2"> <p>Tests de verrichting van het manuscript slechts. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Voorbeeld </p> </td> 
      <td colname="col2"> <p>Laat u de pagina bekijken. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Volledig visueel </p> </td> 
      <td colname="col2"> <p>Produceert een volledige voor-en-na lijstmening van de documenten. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Kort visueel </p> </td> 
      <td colname="col2"> <p>Toont slechts de verschillen tussen de voor en na meningen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Deskundige (diff) </p> </td> 
      <td colname="col2"> <p>Toont de ruwe output van het diff bevel GNU dat wordt gebruikt om de dossiers te vergelijken, gebruikend de geleverde opties van de bevellijn. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Filtrerend Manuscript </p> </td> 
      <td colname="col2"> <p>Laat u uw het filtreren manuscript op het verstrekte gebied kleven. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Wijzigingen opslaan </p> </td> 
      <td colname="col2"> <p>Bewaart het het filtreren manuscript. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Syntaxis controleren </p> </td> 
      <td colname="col2"> <p>Laat u een snelle syntaxiscontrole van uw manuscript door de initialisering, het filtreren, en beëindigingsmanuscripten in werking te stellen doen. Het werkt en slaat uw manuscript niet bij. </p> <p>Alle Perl compilerfouten en waarschuwingen, en alle output STDERR worden gedrukt. </p> <p>Alvorens de gevolgen van het manuscript aan klanten zichtbaar zijn, moet u uw plaatsindex herbouwen. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **De opties van de diff van de bevellijn van GNU**

   Sommige opties van de afscheiding van GNU die u kunt gebruiken terwijl op **[!UICONTROL Expert (diff)]** wijze op de Gelaagde het Filtreren pagina van het Manuscript, omvatten het volgende:

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>De optie van de diff van de bevellijn van GNU </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -b </span> </p> </td> 
      <td colname="col2"> <p> Negeert veranderingen in hoeveelheid witte ruimte. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -B </span> </p> </td> 
      <td colname="col2"> <p> Negeert veranderingen die opnemen of lege lijnen schrappen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -c </span> </p> </td> 
      <td colname="col2"> <p> Gebruikt het formaat van de contextoutput, tonend drie lijnen van context. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -C-lijnen </span> </p> </td> 
      <td colname="col2"> <p> Gebruikt het formaat van de contextoutput, tonend lijnen (een geheel) van context, of drie als de lijnen niet worden gegeven. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -i </span> </p> </td> 
      <td colname="col2"> <p> negeert veranderingen in het geval; overweeg in hoofdletters en kleine letters equivalent. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -f </span> </p> </td> 
      <td colname="col2"> <p> Maakt output die als een ed manuscript gelijkaardig kijkt maar veranderingen in de orde heeft dat zij in het dossier verschijnen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -n </span> </p> </td> 
      <td colname="col2"> <p> RCS-formaat van de output verschilt; als <span class="codeph"> - f </span> behalve dat specificeert elk bevel het aantal lijnen die worden beïnvloed. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>-u </p> </td> 
      <td colname="col2"> <p> Gebruikt het verenigde outputformaat, dat drie lijnen van context toont. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -U-lijnen </span> </p> </td> 
      <td colname="col2"> <p> Gebruikt het verenigde outputformaat, tonend lijnen (een geheel) van context, of drie als de lijnen niet worden gegeven. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Klik **[!UICONTROL Test]** om tegen de het filtreren manuscripten en maskers te testen URL.

   Het klikken werkt en bewaart **[!UICONTROL Test]** niet uw het filtreren manuscript bij.
1. Op het [!DNL Filtering Script] gebied, kleef uw manuscript.
1. (Facultatief) klik **[!UICONTROL Check Syntax]** om een snelle syntaxiscontrole van uw manuscript uit te voeren door het filtreren, initialisering, en beëindigingsmanuscripten in werking te stellen.

   **[!UICONTROL Check Syntax]** werkt uw manuscript bij en bewaart niet.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Facultatief) herbouw uw gefaseerde plaatsindex als u aan voorproef de resultaten wilt.

   Zie [het Vormen van een stijgende index van een gefaseerde website](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Facultatief) op de [!DNL Filtering Script] pagina, doe om het even welke volgend:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Over initialisatiescript {#concept_048B4C8BC9F74BE8BB6162C490C201A3}

U kunt gebruiken [!DNL Initialization Script] om de inhoud van een document van het Web te veranderen alvorens het wordt geïndexeerd.

U kunt de markeringen van HTML opnemen, irrelevante inhoud verwijderen, en zelfs nieuwe meta-gegevens van HTML tot stand brengen die op URL van een document, MIME type, en bestaande inhoud worden gebaseerd. Het initialiseringsmanuscript is een Perl manuscript, dat krachtige koord behandeling en de flexibiliteit van regelmatige uitdrukking aanpassing verstrekt. U gebruikt het initialiseringsmanuscript met een het filtreren manuscript, beëindigingsmanuscript, URL maskermanuscript, en test URL.

Het initialiseringsmanuscript wordt in werking gesteld eens alvorens het indexeren begint. Gebruik dit manuscript om het even welke globale variabelen en subroutines te initialiseren die door uw het filtreren manuscript worden gebruikt. U kunt het initialiseringsmanuscript gebruiken om statusberichten van het het filtreren manuscript aan het indexlogboek te drukken. U of drukt de berichten aan STDERR, of als `_search_debug_log()` subroutine.

Sommige opties van de afscheiding GNU die u kunt gebruiken terwijl op **[!UICONTROL Expert (diff)]** wijze op de Staged pagina van het Manuscript van de Initialisatie, omvatten het volgende:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>GNU-afdiff, optie </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -b </span> </p> </td> 
   <td colname="col2"> <p> Negeert veranderingen in hoeveelheid witte ruimte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -B </span> </p> </td> 
   <td colname="col2"> <p> Negeert veranderingen die opnemen of lege lijnen schrappen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -c </span> </p> </td> 
   <td colname="col2"> <p> Gebruikt het formaat van de contextoutput, tonend drie lijnen van context. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -C-lijnen </span> </p> </td> 
   <td colname="col2"> <p> Gebruikt het formaat van de contextoutput, tonend lijnen (een geheel) van context, of drie als de lijnen niet worden gegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -i </span> </p> </td> 
   <td colname="col2"> <p> negeert veranderingen in het geval; overweeg in hoofdletters en kleine letters equivalent. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -f </span> </p> </td> 
   <td colname="col2"> <p> Maakt output die als een ed manuscript gelijkaardig kijkt maar veranderingen in de orde heeft dat zij in het dossier verschijnen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -n </span> </p> </td> 
   <td colname="col2"> <p> RCS-formaat van de output verschilt; als <span class="codeph"> - f </span> behalve dat specificeert elk bevel het aantal lijnen die worden beïnvloed. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>-u </p> </td> 
   <td colname="col2"> <p> Gebruikt het verenigde outputformaat, dat drie lijnen van context toont. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -U-lijnen </span> </p> </td> 
   <td colname="col2"> <p> Gebruikt het verenigde outputformaat, tonend lijnen (een geheel) van context, of drie als de lijnen niet worden gegeven. </p> </td> 
  </tr> 
 </tbody> 
</table>

U kunt lokale variabelen, globale variabelen, of allebei in deze manuscripten gebruiken. Alle globale variabelen worden geprefacteerd met namespace &quot;belangrijkste::&quot;. Wanneer het initialiseringsmanuscript is begonnen, bevat zijn milieu de volgende standaarddossierhandvatten:

* STDIN - niets (keert onmiddellijk EOF terug wanneer gelezen)
* STDOUT - niets (als het gegeven aan STDOUT wordt gedrukt, wordt het verworpen)
* STDERR - de gegevens die aan STDERR worden gedrukt zijn gedrukt gedrukt aan het Logboek van de Index als fout

Bovendien, kunt u douaneberichten aan het indexlogboek schrijven gebruikend de `_search_debug_log()` subroutine, zoals in het volgende voorbeeld:

```
# Log information to the Index Log 
_search_debug_log("Done processing document: " . $main::search_url);
```

Deze berichten verschijnen met het woord `DEBUG` als voorwoord, en niet geregistreerd als fouten.

Een voorbeeld van een initialiseringsmanuscript is het volgende:

```
# My subroutine to do something. 
sub my_sub_for_the_filtering_script { 
    my ($param1, $param2) = @_; 
    ... 
} 
 
# Initialize the document counter. 
$main::doc_count = 0;
```

Zie [globale variabelen](#global-variables)

### Snelle tips {#section_A2CC0302CAF14135BF8EF6171FB184F1}

* Alle globale variabelen worden geprefacteerd met namespace &quot;belangrijkste:&quot;: `$main::doc_count = 0;`
* Alle lokale variabelen worden gedeclareerd met &quot;my&quot;: `my $i = 0;`
* De subroutines worden bepaald in het initialiseringsmanuscript. Zij hebben geen expliciete &quot;leiding nodig:&quot;namespace: `sub my_sub {`  `...`

   `}`

* Test `$main::search_content_type` alvorens u veranderingen in een dossier aanbrengt. Het testen kan u helpen vermijden makend onzorgvuldige veranderingen in binaire dossiers, zoals Swf- dossiers of Pdf- dossiers:

   `if ($main::search_content_type =~ /^text\/html/) { ...`

* De `$main::search_content_type` is de volledige tevreden-Type kopbal die door uw server wordt geleverd. Het kan een eenvoudig type MIME, zoals &quot;tekst/html&quot;soms bevatten. Of, kan het een MIME type bevatten dat door andere informatie wordt gevolgd, zoals het karakter van het document - reeks het coderen, zoals &quot;tekst/html; charset=iso-8859-1&quot;.
* Voor elk type van niet-HTML- document, `$main::search_content_type` kan diverse waarden nemen. Het testen voor elke waarde in uw manuscript wordt omslachtig. Bijvoorbeeld, hebben sommige documenten van Word inhoudstype waarden van &quot;toepassing/msword&quot;, &quot;application/vnd.ms-woord&quot;of &quot;application/x-msword&quot;. In dergelijke gevallen, `$main::search_content_class` kan de volgende waarden nemen:

   * html
   * pdf
   * woord
   * uitblinken
   * powerpoint
   * mp3
   * tekst

* In het voorbeeld, zou het testen `$main::search_content_class` voor &quot;woord&quot;om het even welke drie mogelijke tevreden-type waarden aanpassen.
* Als niets aan STDOUT van het het filtreren manuscript wordt gedrukt, dan wordt het document gebruikt precies aangezien het werd gedownload. Namelijk als u te hoeven om niets in een document te veranderen, dan te hoeven u niet om STDIN aan STDOUT voor dat document te kopiëren.
* Als u alle tekst uit een document wilt verwijderen, druk een geldig dossier STDOUT. Bijvoorbeeld, om al tekst uit een HTML- document volledig te verwijderen, doet u het volgende: `print "<html></html>";`

## Een initialisatiescript toevoegen {#task_5A03B8D0C46E4674B7CE88203515803B}

Het initialiseringsmanuscript is een Perl manuscript dat eens wordt in werking gesteld alvorens om het even welke documenten worden geïndexeerd.

U gebruikt het initialiseringsmanuscript samen met een het filtreren manuscript, beëindigingsmanuscript, en URL maskermanuscript.

Ben zeker dat u uw plaatsindex herbouwt zodat de resultaten van uw initialiseringsmanuscript aan uw klanten zichtbaar zijn.

Zie [het Vormen van een stijgende index van een gefaseerde website](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Om een initialiseringsmanuscript toe te voegen**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Filtering]** > **[!UICONTROL Initialization Script]**.
1. (Facultatief) op de [!DNL Initialization Script] pagina, op het [!DNL Test URL] gebied, ga URL van een document op uw website in.

   Klik een het testen optie om veranderingen in de ruwe HTML- tekst te zien.

   Zie de het filtreren optieslijst onder het **Toevoegen van een het filtreren manuscript**.

   Klik **[!UICONTROL Test]** om tegen de het filtreren manuscripten en maskers te testen URL.

   Het klikken werkt **[!UICONTROL Test]** niet en bewaart uw initialiseringsmanuscript bij.
1. Op het [!DNL Initialization Script] gebied, kleef uw manuscript.
1. (Facultatief) klik **[!UICONTROL Check Syntax]** om een snelle syntaxiscontrole van uw manuscript uit te voeren door het filtreren, initialisering, en beëindigingsmanuscripten in werking te stellen.

   **[!UICONTROL Check Syntax]** werkt uw manuscript bij en bewaart niet.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Facultatief) herbouw uw gefaseerde plaatsindex als u aan voorproef de resultaten wilt.

   Zie [het Vormen van een stijgende index van een gefaseerde website](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Facultatief) op de [!DNL Initialization Script] pagina, doe om het even welke volgend:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Over het script Beëindiging {#concept_AAD6B3B0E7124874AD0947096FC42F47}

U kunt gebruiken [!DNL Termination Script] om de inhoud van een document van het Web te veranderen alvorens het wordt geïndexeerd.

U kunt de markeringen van HTML opnemen, irrelevante inhoud verwijderen, en zelfs nieuwe meta-gegevens van HTML tot stand brengen die op URL van een document, MIME type, en bestaande inhoud worden gebaseerd. Het initialiseringsmanuscript is een Perl manuscript, dat krachtige koord behandeling en de flexibiliteit van regelmatige uitdrukking aanpassing verstrekt. U gebruikt het beëindigingsmanuscript met een initialiseringsmanuscript, filtrerend manuscript, beëindigingsmanuscript, URL maskermanuscript, en test URL.

Het beëindigingsmanuscript wordt in werking gesteld eens nadat alle documenten worden geïndexeerd. U kunt het beëindigingsmanuscript gebruiken om statusberichten van het het filtreren manuscript aan het indexlogboek te drukken. U of drukt de berichten aan STDERR, of als `_search_debug_log()` subroutine.

Sommige opties van de diff bevellijn van GNU die u kunt gebruiken terwijl op **[!UICONTROL Expert (diff)]** wijze op de Staged pagina van het Manuscript van de Beëindiging, omvatten het volgende:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>De optie van de diff van de bevellijn van GNU </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -b </span> </p> </td> 
   <td colname="col2"> <p> Negeert veranderingen in hoeveelheid witte ruimte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -B </span> </p> </td> 
   <td colname="col2"> <p> Negeert veranderingen die opnemen of lege lijnen schrappen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -c </span> </p> </td> 
   <td colname="col2"> <p> Gebruikt het formaat van de contextoutput, tonend drie lijnen van context. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -C-lijnen </span> </p> </td> 
   <td colname="col2"> <p> Gebruikt het formaat van de contextoutput, tonend lijnen (een geheel) van context, of drie als de lijnen niet worden gegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -i </span> </p> </td> 
   <td colname="col2"> <p> negeert veranderingen in het geval; overweeg in hoofdletters en kleine letters equivalent. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -f </span> </p> </td> 
   <td colname="col2"> <p> Maakt output die als een ed manuscript gelijkaardig kijkt maar veranderingen in de orde heeft dat zij in het dossier verschijnen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -n </span> </p> </td> 
   <td colname="col2"> <p> RCS-formaat van de output verschilt; als <span class="codeph"> - f </span> behalve dat specificeert elk bevel het aantal lijnen die worden beïnvloed. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>-u </p> </td> 
   <td colname="col2"> <p> Gebruikt het verenigde outputformaat, dat drie lijnen van context toont. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -U-lijnen </span> </p> </td> 
   <td colname="col2"> <p> Gebruikt het verenigde outputformaat, tonend lijnen (een geheel) van context, of drie als de lijnen niet worden gegeven. </p> </td> 
  </tr> 
 </tbody> 
</table>

U kunt lokale variabelen, globale variabelen, of allebei in deze manuscripten gebruiken. Alle globale variabelen worden geprefacteerd met namespace &quot;belangrijkste::&quot;. Wanneer het beëindigingsmanuscript is begonnen, bevat zijn milieu de volgende standaarddossierhandvatten:

* STDIN - niets (keert onmiddellijk EOF terug wanneer gelezen)
* STDOUT - niets (als het gegeven aan STDOUT wordt gedrukt, wordt het verworpen)
* STDERR - de gegevens die aan STDERR worden gedrukt zijn gedrukt gedrukt aan het indexlogboek als fout

Bovendien, kunt u douaneberichten aan het indexlogboek schrijven gebruikend de `_search_debug_log()` subroutine, zoals in het volgende voorbeeld:

```
# Log information to the Index Log 
_search_debug_log("Done processing document: " . $main::search_url);
```

Deze berichten verschijnen met het woord `DEBUG` als voorwoord, en niet geregistreerd als fouten.

Om het aantal documenten te tonen die door uw het filtreren manuscript als foutenlijn in het indexlogboek werden verwerkt, kunt u het volgende beëindigingsmanuscript gebruiken:

```
# Print the value of the document counter. 
print STDERR "Total docs: $main::doc_count\n"; 
# Or, using the log subroutine: 
_search_debug_log("Total docs: " . $main::doc_count);
```

Zie [globale variabelen](#global-variables)

### Snelle tips {#section_5790EA7ACAC046CBA01F759F88E2460F}

* Alle globale variabelen worden geprefacteerd met namespace &quot;belangrijkste:&quot;: `$main::doc_count = 0;`
* Alle lokale variabelen worden gedeclareerd met &quot;my&quot;: `my $i = 0;`
* De subroutines worden bepaald in het initialiseringsmanuscript. Zij hebben geen expliciete &quot;leiding nodig:&quot;namespace: `sub my_sub {`  `...`

   `}`

* Test `$main::search_content_type` alvorens u veranderingen in een dossier aanbrengt. Het testen kan u helpen vermijden makend onzorgvuldige veranderingen in binaire dossiers, zoals Swf- dossiers of Pdf- dossiers:

   `if ($main::search_content_type =~ /^text\/html/) { ...`

* De `$main::search_content_type` is de volledige tevreden-Type kopbal die door uw server wordt geleverd. Het kan een eenvoudig type MIME, zoals &quot;tekst/html&quot;soms bevatten. Of, kan het een MIME type bevatten dat door andere informatie wordt gevolgd, zoals het karakter van het document - reeks het coderen, zoals &quot;tekst/html; charset=iso-8859-1&quot;.
* Voor elk type van niet-HTML- document, `$main::search_content_type` kan diverse waarden nemen. Het testen voor elke waarde in uw manuscript wordt omslachtig. Bijvoorbeeld, hebben sommige documenten van Word inhoudstype waarden van &quot;toepassing/msword&quot;, &quot;application/vnd.ms-woord&quot;of &quot;application/x-msword&quot;. In dergelijke gevallen, `$main::search_content_class` kan de volgende waarden nemen:

   * html
   * pdf
   * woord
   * uitblinken
   * powerpoint
   * mp3
   * tekst

* In het voorbeeld, zou het testen `$main::search_content_class` voor &quot;woord&quot;om het even welke drie mogelijke tevreden-type waarden aanpassen.
* Als niets aan STDOUT van het het filtreren manuscript wordt gedrukt, dan wordt het document gebruikt precies aangezien het werd gedownload. Namelijk als u te hoeven om niets in een document te veranderen, dan te hoeven u niet om STDIN aan STDOUT voor dat document te kopiëren.
* Als u alle tekst uit een document wilt verwijderen, druk een geldig dossier STDOUT. Bijvoorbeeld, om al tekst uit een HTML- document volledig te verwijderen, doet u het volgende: `print "<html></html>";`

## Een beëindigingsmanuscript toevoegen {#task_F0CFB412871642CFBC88132889C5B6F9}

Het beëindigingsmanuscript is een Perl manuscript dat in werking wordt gesteld zodra alle documenten worden geïndexeerd.

U gebruikt het beëindigingsmanuscript samen met een het filtreren manuscript, beëindigingsmanuscript, en URL maskermanuscript.

Ben zeker dat u uw plaatsindex herbouwt zodat de resultaten van uw initialiseringsmanuscript aan uw klanten zichtbaar zijn.

Zie [het Vormen van een stijgende index van een gefaseerde website](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Om een beëindigingsmanuscript toe te voegen**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Filtering]** > **[!UICONTROL Termination Script]**.
1. (Facultatief) op de [!DNL Termination Script] pagina, op het [!DNL Test URL] gebied, ga URL van een document op uw website in.

   Klik een het testen optie om veranderingen in de ruwe HTML- tekst te zien.

   Zie de lijst van het filtreren opties onder het **Toevoegen van een het filtreren manuscript**.

   Klik **[!UICONTROL Test]** om tegen de het filtreren manuscripten en maskers te testen URL.

   Het klikken werkt en bewaart **[!UICONTROL Test]** niet uw beëindigingsmanuscript bij.
1. Op het [!DNL Termination Script] gebied, kleef uw manuscript.
1. (Facultatief) klik **[!UICONTROL Check Syntax]** om een snelle syntaxiscontrole van uw manuscript uit te voeren door de initialisering, het filtreren, en beëindigingsmanuscripten in werking te stellen.

   **[!UICONTROL Check Syntax]** werkt uw manuscript bij en bewaart niet.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Facultatief) herbouw uw gefaseerde plaatsindex als u aan voorproef de resultaten wilt.

   Zie [het Vormen van een stijgende index van een gefaseerde website](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Facultatief) op de [!DNL Termination Script] pagina, doe om het even welke volgend:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Ongeveer URL Maskers manuscript {#concept_384F32EA18F84853A7BA99A04009330B}

Met het filtreren, kunt u de inhoud van een Webdocument veranderen alvorens het wordt geïndexeerd. U kunt de markeringen van HTML opnemen, irrelevante inhoud verwijderen, en zelfs nieuwe meta-gegevens van HTML tot stand brengen die op URL van een document, MIME type, en bestaande inhoud worden gebaseerd. Het URL maskermanuscript is een Perl manuscript dat krachtige koordbehandeling en de flexibiliteit van regelmatige uitdrukkingsaanpassing verstrekt.

Om de inhoud van documenten te veranderen die slechts in een specifiek gedeelte van uw website bestaan, kunt u specificeren omvat maskers URL, sluit maskers URL, of allebei uit, om de aangewezen pagina&#39;s te bepalen.

Als u slechts de documenten onder wilt veranderen, kunt u de volgende reeks maskers gebruiken `"https://www.mysite.com/faqs/"`:

```
include https://www.mysite.com/faqs/ 
exclude *
```

U kunt regelmatige uitdrukking in een URL maskermanuscript zoals in het volgende voorbeeld ook gebruiken:

```
include regexp ^https://www\.mysite\.com.*/faqs/.*$ 
exclude *
```

Zie [Regelmatige expressies](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

De maskers van Scripted URL worden overwogen in de orde dat u hen op het [!DNL URL Masks] gebied inging. Wanneer een document URL een masker aanpast, is dat document inbegrepen of uitgesloten gebaseerd op het type van masker. Als URL van een document geen Url- masker aanpast, is het document inbegrepen slechts als zijn MIME type &quot;tekst/html&quot;is. Alle andere MIME types zijn uitgesloten.

## Een URL-maskerscript toevoegen {#task_D18F2A496C1C45C997B5DA650AAF5D59}

Specificeer URL omvat maskers en sluit maskers uit om de inhoud van documenten te veranderen die slechts in een specifiek gedeelte van uw website bestaan.

Alvorens de gevolgen van de montages van Maskers URL aan bezoekers zichtbaar zijn, herbouw uw plaatsindex.

**Om een URL maskermanuscript toe te voegen**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Filtering]** > **[!UICONTROL URL Masks]**.
1. (Facultatief) op de [!DNL URL Masks] pagina, op het [!DNL Test URL] gebied, ga een URL van een document op uw website in, en klik dan **[!UICONTROL Test]** om URL tegen de het filtreren manuscripten en maskers te testen.

   Het testURL document wordt gedownload, dat als input STDIN aan het filtrerende manuscript wordt gebruikt. Dan worden het filtreren, de initialisering, en de beëindigingsmanuscripten in werking gesteld. Als er om het even welke output STDOUT van het het filtreren manuscript is dat de output in een nieuw browser venster wordt getoond.

   Het klikken werkt **[!UICONTROL Test]** niet bij en bewaart uw manuscript.
1. Op het [!DNL URL Masks] gebied, ga één masker URL per lijn in.
1. (Facultatief) klik **[!UICONTROL Check Syntax]** om een snelle syntaxiscontrole van uw maskers uit te voeren URL door het filtreren, initialisering, en beëindigingsmanuscripten in werking te stellen.

   **[!UICONTROL Check Syntax]** werkt uw manuscript bij en bewaart niet.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Facultatief) herbouw uw gefaseerde plaatsindex als u aan voorproef de resultaten wilt.

   Zie [het Vormen van een stijgende index van een gefaseerde website](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Facultatief) op de [!DNL URL Masks] pagina, doe om het even welke volgend:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Ongeveer de Types van Inhoud in het Filtreren {#concept_E3EFF4A148EA4D21AFD0A5453A00427E}

Laat u selecteren welke inhoudstypes die u voor deze rekening wilt filteren.

De tekst die binnen de geselecteerde inhoudstypes wordt gevonden wordt omgezet in HTML en dan verwerkt gebruikend het manuscript dat in het Filtreren Manuscript wordt gespecificeerd.

Zie [over Filtrerend Manuscript](../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47).

De inhoudstypes die u kunt selecteren omvatten het volgende:

* PDF-documenten
* Tekstdocumenten
* Adobe Flash-films
* Microsoft Word-bestanden
* Microsoft Office-bestanden (OpenXML)
* Microsoft Excel-bestanden
* Microsoft PowerPoint-bestanden
* Tekst in MP3-muziekbestanden

Alvorens de gevolgen van de montages van de Types van Inhoud of de veranderingen in de montages aan klanten zichtbaar zijn, moet u uw plaatsindex herbouwen.

## Het selecteren van de inhoudstypes die worden gefiltreerd {#task_C46081FA425A43EC8FDE6EA4A52A170A}

Selecteer de inhoudstypes die u tot het manuscript wilt overgaan dat in het Filtrerende Manuscript wordt gespecificeerd.

Zie [over Filtrerend Manuscript](../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47).

**Om de inhoudstypes te selecteren die worden gefiltreerd**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Filtering]** > **[!UICONTROL Content Types]**.
1. Voor de [!DNL Content Types] pagina, controleer de inhoudstypes die u tot het filtermanuscript wilt overgaan.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Facultatief) herbouw uw gefaseerde plaatsindex als u aan voorproef de resultaten wilt.

   Zie [het Vormen van een stijgende index van een gefaseerde website](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Facultatief) op de [!DNL Content Types] pagina, doe om het even welke volgend:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).
