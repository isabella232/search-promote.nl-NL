---
description: Gebruik het menu Filteren om scripts te gebruiken waarmee de inhoud van een webdocument wordt gewijzigd voordat het wordt geïndexeerd.
solution: Target
subtopic: Filtering
title: Het menu Filteren
topic-legacy: Settings,Site search and merchandising
uuid: ebb08fa8-4e17-417d-868b-11fc2af9f284
exl-id: 1a1c7b86-a29b-4c17-8743-ff3c2c91b63a
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '4003'
ht-degree: 0%

---

# Informatie over het menu Filteren{#about-the-filtering-menu}

Gebruik het menu Filteren om scripts te gebruiken waarmee de inhoud van een webdocument wordt gewijzigd voordat het wordt geïndexeerd.

## Informatie over het filteren van scripts {#concept_E56B73D625854AB2A899EF2D56CFCB47}

U kunt [!DNL Filtering Script] gebruiken om de inhoud van een document van het Web te veranderen alvorens het wordt geïndexeerd.

U kunt HTML-tags invoegen, irrelevante inhoud verwijderen en zelfs nieuwe HTML-metagegevens maken op basis van de URL, het MIME-type en de bestaande inhoud van een document. Het filterscript is een Perl-script dat krachtige tekenreeksafhandeling en de flexibiliteit van reguliere expressies biedt. U gebruikt het het filtreren manuscript met een initialisatiescript, beëindigingsmanuscript, het maskermanuscript URL, en test URL.

Het filterscript wordt telkens uitgevoerd wanneer een document van uw website wordt gelezen. Het script wordt als een standaardfilter uitgevoerd, met andere woorden, leest gegevens van STDIN, transformeert die gegevens op een of andere manier en schrijft de resultaten naar STDOUT. U kunt het het filtreren manuscript gebruiken om statusberichten van het het filtreren manuscript aan het indexlogboek te drukken. U drukt of de berichten aan STDERR, of als subroutine `_search_debug_log()`.

Sommige GNU-afschuivingsopties die u kunt gebruiken in de modus **[!UICONTROL Expert (diff)]** op de pagina Script-script met gefaseerd filteren, zijn onder andere:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>GNU, optie voor afschuiven </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -b  </span> </p> </td> 
   <td colname="col2"> <p> Hiermee negeert u wijzigingen in de hoeveelheid witruimte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -B  </span> </p> </td> 
   <td colname="col2"> <p> Hiermee worden wijzigingen genegeerd waarmee lege regels worden ingevoegd of verwijderd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -c  </span> </p> </td> 
   <td colname="col2"> <p> Gebruikt de indeling voor contextuitvoer, waarin drie regels context worden weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -C-lijnen  </span> </p> </td> 
   <td colname="col2"> <p> Gebruikt de indeling van de contextuitvoer en geeft regels (een geheel getal) voor context weer, of drie als er geen regels zijn opgegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -i  </span> </p> </td> 
   <td colname="col2"> <p> negeert veranderingen in geval; U kunt instellen dat hoofdletters en kleine letters equivalent zijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -f  </span> </p> </td> 
   <td colname="col2"> <p> Hiermee maakt u uitvoer die er net zo uitziet als een Eed-script, maar die wijzigingen heeft in de volgorde waarin ze in het bestand worden weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -n  </span> </p> </td> 
   <td colname="col2"> <p> Output RCS-formaat verschilt; zoals <span class="codeph"> -f </span> behalve dat specificeert elke bevel het aantal lijnen die worden beïnvloed. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>-u </p> </td> 
   <td colname="col2"> <p> Gebruikt het verenigde outputformaat, dat drie lijnen van context toont. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -U-lijnen  </span> </p> </td> 
   <td colname="col2"> <p> Gebruikt het verenigde outputformaat, dat lijnen (een geheel) van context toont, of drie als geen lijnen wordt gegeven. </p> </td> 
  </tr> 
 </tbody> 
</table>

U kunt lokale variabelen, globale variabelen, of allebei in deze manuscripten gebruiken. Alle algemene variabelen krijgen de voorkeur met de naamruimte &quot;main::&quot;. Wanneer het het filtreren manuscript wordt begonnen, bevat zijn milieu de volgende standaarddossierhandvatten:

* STDIN - niets (retourneert direct EOF bij lezen)
* STDOUT - vervangende HTML (als gegevens worden afgedrukt op STDOUT, wordt deze gebruikt in plaats van het oorspronkelijke document)
* STDERR - gegevens die naar STDERR worden afgedrukt, worden als een fout afgedrukt naar het indexlogboek

Bovendien, kunt u douaneberichten aan het indexlogboek schrijven gebruikend `_search_debug_log()` subroutine, zoals in het volgende voorbeeld:

```
# Log information to the Index Log 
_search_debug_log("Done processing document: " . $main::search_url);
```

Deze berichten verschijnen met het woord `DEBUG` als voorkeur, en niet geregistreerd als fouten.

Hier volgt een voorbeeld van filteren. De Web-pagina `<title>` gebieden beginnen vaak met de bedrijfsnaam. Hoewel deze informatie nuttig is voor plaatsnavigatie doeleinden, is het niet relevant wanneer het zoeken. Als de titels van alle MegaCorp-webpagina&#39;s beginnen met een gemeenschappelijke tekenreeks, zoals:

```
<title>MegaCorp -- meaningful title 
here</title>
```

U moet &quot; `MegaCorp --`&quot; verwijderen aan het begin van elke documenttitel en elk document tellen dat wordt verwerkt met het filterscript. Hiervoor kunt u het volgende script gebruiken:

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

## Algemene variabelen {#global-variables}

U kunt de volgende variabelen in om het even welk filtrerend manuscript gebruiken:

| Variabele | Beschrijving |
|--- |--- |
| `$main::search_crawl_type` | De waarde `$main::search_crawl_type` geeft het type indexbewerking aan dat wordt uitgevoerd.  Vervangen formulier: `$main::ws_crawl_type` De indexbewerkingen en bijbehorende waarden zijn onder andere: <ul><li>Volledige index: Handmatig - `manual`</li><li>Volledige index: Gepland - `auto`</li><li>Volledige index: Afstandsbediening - `CGI`</li><li>Incrementele index: Handmatig - `manual-incremental`</li><li>Incrementele index: Gepland - `auto-incremental` </li><li>Incrementele index: Afstandsbediening - `CGI-incremental`</li><li>Scriptindex: Handmatig - `manual-indexlist.txt` </li><li>Scriptindex: Gepland - `auto-indexlist.txt`</li><li>Scriptindex: Afstandsbediening - `CGI-indexlist.txt`</li><li>Regenereren - `manual-upgrade`</li></ul> |
| `$main::search_clear_cache` | De waarde geeft aan of de indexeringsoptie &quot;Indexcache wissen&quot; is aangevraagd voor de huidige indexbewerking. Als &quot;Clear index cache&quot; is aangevraagd, is de waarde van `$main::search_clear_cache` &quot; `1`&quot;.  Vervangen formulier: `$main::ws_clear_cache` |
| `$main::search_fields` | De waarde bevat een lijst met door tabs gescheiden metagegevensvelden die in de account zijn gedefinieerd. De standaardwaarde is:   `url title desc keys target body alt date charset language` Vervangen vorm: `$main::ws_fields` |
| `$main::search_collections` | De waarde bevat een lijst met door tabs gescheiden verzamelingen die in de account zijn gedefinieerd.  Vervangen formulier: `$main::ws_collections` |
| `$main::search_url` | De waarde is volledig - gekwalificeerde URL van het document.  Vervangen formulier: `$main::ws_url` |
| `$main::search_content_type` | De waarde is het inhoudstype van het document dat wordt opgehaald van de metatag http-equiv. Een typische waarde is &quot;text/html; charset=iso-8859-1&quot;.  Vervangen formulier: `$main::ws_content_type` |
| `$main::search_content_class` | De waarde is de inhoudsklasse van het document, zoals afgeleid van het inhoudstype veld.  Vervangen formulier: `$main::ws_content_class` |
| `$main::search_syntax_check` | De waarde geeft het gebruik van de knop Syntaxis controleren weer. Indien aangeklikt, is de waarde 1 (één); anders is de waarde 0 (nul).  Vervangen formulier: `$main::ws_syntax_check` |
| `$main::search_last_mod_date` | Als deze waarde wordt opgegeven door de webserver, bevat deze de EPUCH-representatie (seconden sinds 1 januari 1970) van de datum waarop het document het laatst is gewijzigd.  U kunt deze waarde opmaken met de bibliotheekaanroep Perl localtime(). |

### Snelle tips {#section_89A5C16911744AF98E232DF608C6A1F5}

* Alle algemene variabelen krijgen de voorkeur met de naamruimte &quot;main:&quot;: `$main::doc_count = 0;`
* Alle lokale variabelen worden gedeclareerd met &quot;my&quot;: `my $i = 0;`
* Subroutines worden bepaald in het initialisatiescript. Ze hebben geen expliciete naamruimte &#39;main:&#39; nodig: `sub my_sub {` `...`

   `}`

* Test `$main::search_content_type` alvorens u veranderingen in een dossier aanbrengt. Testen kan u helpen te voorkomen dat u onophoudelijke wijzigingen aanbrengt in binaire bestanden, zoals SWF-bestanden of PDF-bestanden:

   `if ($main::search_content_type =~ /^text\/html/) { ...`

* De `$main::search_content_type` is de volledige Content-Type header die door uw server wordt geleverd. Het kan soms een eenvoudig MIME-type bevatten, zoals &quot;text/html&quot;. Of het kan een MIME-type bevatten, gevolgd door andere informatie, zoals de codering van de tekenset van het document, zoals &quot;text/html&quot;; charset=iso-8859-1&quot;.
* Voor elk type niet-HTML-document kan `$main::search_content_type` verschillende waarden hebben. Het testen voor elke waarde in uw script wordt omslachtig. Sommige Word-documenten hebben bijvoorbeeld waarden van het inhoudstype &quot;application/msword&quot;, &quot;application/vnd.ms-word&quot; of &quot;application/x-msword&quot;. In dergelijke gevallen kan `$main::search_content_class` de volgende waarden gebruiken:

   * html
   * pdf
   * woord
   * excel
   * powerpoint
   * mp3
   * text

* In het voorbeeld komt het testen van `$main::search_content_class` op &quot;woord&quot; overeen met een van de drie mogelijke waarden voor inhoudstype.
* Als er niets vanaf het filterscript naar STDOUT wordt afgedrukt, wordt het document exact gebruikt zoals het is gedownload. Als u dus niets in een document hoeft te wijzigen, hoeft u STDIN niet naar STDOUT voor dat document te kopiëren.
* Als u alle tekst uit een document wilt verwijderen, drukt u een geldige bestands-STDOUT af. Als u bijvoorbeeld alle tekst volledig wilt verwijderen uit een HTML-document, doet u het volgende: `print "<html></html>";`

## Een filterscript toevoegen {#task_0AB84FD1133F47F9AA069A79BEA13A22}

Het filterscript is een Perl-script dat wordt uitgevoerd voor elk document dat van uw website wordt gedownload.

U gebruikt het het filtreren manuscript in combinatie met een initialisatiescript, beëindigingsmanuscript, en URL maskeringsmanuscript.

Zorg ervoor dat u uw site-index opnieuw genereert zodat de resultaten van uw filterscript zichtbaar zijn voor uw klanten.

Zie [Een incrementele index van een gefaseerde website configureren](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Een filterscript toevoegen**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Filtering]** > **[!UICONTROL Filtering Script]**.
1. (Optioneel) Voer in het veld [!DNL Test URL] op de pagina [!DNL Filtering Script] de URL van een document op uw website in.

   Klik op een testoptie om de wijzigingen in de onbewerkte HTML-tekst weer te geven.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Veld URL testen </p> </td> 
      <td colname="col2"> <p>Hiermee kunt u de URL van een document op uw website invoeren. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Testen </p> </td> 
      <td colname="col2"> <p>Test de URL op basis van de filterscripts en URL-maskers. </p> <p>Het test-URL-document wordt gedownload en vervolgens gebruikt als STDIN-invoer voor het filterscript. De initialisatie, het filtreren, en beëindigingsmanuscripten worden dan in werking gesteld. Als er om het even welke output STDOUT van het het filtreren manuscript is, wordt die output getoond in een nieuw browser venster. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Alleen testen </p> </td> 
      <td colname="col2"> <p>Test alleen de bewerking van het script. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Voorvertoning </p> </td> 
      <td colname="col2"> <p>Hiermee kunt u de pagina weergeven. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Volledig visueel </p> </td> 
      <td colname="col2"> <p>Hiermee genereert u een volledige voor- en Na-tabelweergave van de documenten. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Kort visueel </p> </td> 
      <td colname="col2"> <p>Alleen de verschillen tussen de weergaven Voor en Na worden weergegeven. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Expert (diff) </p> </td> 
      <td colname="col2"> <p>Geeft de onbewerkte uitvoer weer van de GNU-opdracht diff die wordt gebruikt om de bestanden te vergelijken met behulp van de beschikbare opties voor de opdrachtregel. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Script filteren </p> </td> 
      <td colname="col2"> <p>Hiermee kunt u het filterscript in het opgegeven veld plakken. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Wijzigingen opslaan </p> </td> 
      <td colname="col2"> <p>Hiermee slaat u het filterscript op. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Syntaxis controleren </p> </td> 
      <td colname="col2"> <p>Hiermee kunt u een snelle syntaxiscontrole van uw script uitvoeren door de initialisatie-, filter- en beëindigingsscripts uit te voeren. Uw script wordt niet bijgewerkt en opgeslagen. </p> <p>Alle Perl-compilatiefouten en -waarschuwingen en alle STDERR-uitvoer worden afgedrukt. </p> <p>Voordat de effecten van het script zichtbaar zijn voor klanten, moet u de index van de site opnieuw genereren. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **Opties voor GNU-diff-opdrachtregel**

   Sommige GNU-afschuivingsopties die u kunt gebruiken in de modus **[!UICONTROL Expert (diff)]** op de pagina Script-script met gefaseerd filteren, zijn onder andere:

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>GNU diff, opdrachtregeloptie </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -b  </span> </p> </td> 
      <td colname="col2"> <p> Hiermee negeert u wijzigingen in de hoeveelheid witruimte. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -B  </span> </p> </td> 
      <td colname="col2"> <p> Hiermee worden wijzigingen genegeerd waarmee lege regels worden ingevoegd of verwijderd. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -c  </span> </p> </td> 
      <td colname="col2"> <p> Gebruikt de indeling voor contextuitvoer, waarin drie regels context worden weergegeven. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -C-lijnen  </span> </p> </td> 
      <td colname="col2"> <p> Gebruikt de indeling van de contextuitvoer en geeft regels (een geheel getal) voor context weer, of drie als er geen regels zijn opgegeven. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -i  </span> </p> </td> 
      <td colname="col2"> <p> negeert veranderingen in geval; U kunt instellen dat hoofdletters en kleine letters equivalent zijn. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -f  </span> </p> </td> 
      <td colname="col2"> <p> Hiermee maakt u uitvoer die er net zo uitziet als een Eed-script, maar die wijzigingen heeft in de volgorde waarin ze in het bestand worden weergegeven. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -n  </span> </p> </td> 
      <td colname="col2"> <p> Output RCS-formaat verschilt; zoals <span class="codeph"> -f </span> behalve dat specificeert elke bevel het aantal lijnen die worden beïnvloed. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>-u </p> </td> 
      <td colname="col2"> <p> Gebruikt het verenigde outputformaat, dat drie lijnen van context toont. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -U-lijnen  </span> </p> </td> 
      <td colname="col2"> <p> Gebruikt het verenigde outputformaat, dat lijnen (een geheel) van context toont, of drie als geen lijnen wordt gegeven. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Klik **[!UICONTROL Test]** om tegen de het filtreren manuscripten en maskers URL te testen.

   Als u op **[!UICONTROL Test]** klikt, wordt uw filterscript niet bijgewerkt en opgeslagen.
1. Plak het script in het veld [!DNL Filtering Script].
1. (Optioneel) Klik op **[!UICONTROL Check Syntax]** om een snelle syntaxiscontrole van uw script uit te voeren door het filteren, initialiseren en beëindigen van scripts uit te voeren.

   **[!UICONTROL Check Syntax]** werkt het script niet bij en slaat het niet op.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Optioneel) Maak de gefaseerde site-index opnieuw als u een voorvertoning van de resultaten wilt zien.

   Zie [Een incrementele index van een gefaseerde website configureren](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Optioneel) Voer op de pagina [!DNL Filtering Script] een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Informatie over initialisatiescript {#concept_048B4C8BC9F74BE8BB6162C490C201A3}

U kunt [!DNL Initialization Script] gebruiken om de inhoud van een document van het Web te veranderen alvorens het wordt geïndexeerd.

U kunt HTML-tags invoegen, irrelevante inhoud verwijderen en zelfs nieuwe HTML-metagegevens maken op basis van de URL, het MIME-type en de bestaande inhoud van een document. Het initialisatiescript is een manuscript Perl, dat krachtige koordbehandeling en de flexibiliteit van regelmatige uitdrukkingsaanpassing verstrekt. U gebruikt het initialisatiescript met een het filtreren manuscript, beëindigingsmanuscript, URL maskermanuscript, en test URL.

Het initialisatiescript wordt één keer uitgevoerd voordat het indexeren begint. Gebruik dit script om algemene variabelen en subroutines te initialiseren die door uw filterscript worden gebruikt. U kunt het initialisatiescript gebruiken om statusberichten van het het filtreren manuscript aan het indexlogboek te drukken. U of drukt de berichten aan STDERR, of als subroutine `_search_debug_log()`.

Sommige GNU-afschuivingsopties die u kunt gebruiken in de modus **[!UICONTROL Expert (diff)]** op de pagina Script-code voor gefaseerde initialisatie, zijn onder andere:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>GNU, optie voor afschuiven </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -b  </span> </p> </td> 
   <td colname="col2"> <p> Hiermee negeert u wijzigingen in de hoeveelheid witruimte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -B  </span> </p> </td> 
   <td colname="col2"> <p> Hiermee worden wijzigingen genegeerd waarmee lege regels worden ingevoegd of verwijderd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -c  </span> </p> </td> 
   <td colname="col2"> <p> Gebruikt de indeling voor contextuitvoer, waarin drie regels context worden weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -C-lijnen  </span> </p> </td> 
   <td colname="col2"> <p> Gebruikt de indeling van de contextuitvoer en geeft regels (een geheel getal) voor context weer, of drie als er geen regels zijn opgegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -i  </span> </p> </td> 
   <td colname="col2"> <p> negeert veranderingen in geval; U kunt instellen dat hoofdletters en kleine letters equivalent zijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -f  </span> </p> </td> 
   <td colname="col2"> <p> Hiermee maakt u uitvoer die er net zo uitziet als een Eed-script, maar die wijzigingen heeft in de volgorde waarin ze in het bestand worden weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -n  </span> </p> </td> 
   <td colname="col2"> <p> Output RCS-formaat verschilt; zoals <span class="codeph"> -f </span> behalve dat specificeert elke bevel het aantal lijnen die worden beïnvloed. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>-u </p> </td> 
   <td colname="col2"> <p> Gebruikt het verenigde outputformaat, dat drie lijnen van context toont. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -U-lijnen  </span> </p> </td> 
   <td colname="col2"> <p> Gebruikt het verenigde outputformaat, dat lijnen (een geheel) van context toont, of drie als geen lijnen wordt gegeven. </p> </td> 
  </tr> 
 </tbody> 
</table>

U kunt lokale variabelen, globale variabelen, of allebei in deze manuscripten gebruiken. Alle algemene variabelen krijgen de voorkeur met de naamruimte &quot;main::&quot;. Wanneer het initialisatiescript is begonnen, bevat zijn milieu de volgende standaarddossierhandvatten:

* STDIN - niets (retourneert direct EOF bij lezen)
* STDOUT - niets (als de gegevens aan STDOUT worden gedrukt, wordt het verworpen)
* STDERR - gegevens die naar STDERR worden afgedrukt, worden als een fout afgedrukt naar het indexlogboek

Bovendien, kunt u douaneberichten aan het indexlogboek schrijven gebruikend `_search_debug_log()` subroutine, zoals in het volgende voorbeeld:

```
# Log information to the Index Log 
_search_debug_log("Done processing document: " . $main::search_url);
```

Deze berichten verschijnen met het woord `DEBUG` als voorkeur, en niet geregistreerd als fouten.

Een voorbeeld van een initialisatiescript is het volgende:

```
# My subroutine to do something. 
sub my_sub_for_the_filtering_script { 
    my ($param1, $param2) = @_; 
    ... 
} 
 
# Initialize the document counter. 
$main::doc_count = 0;
```

Zie [Globale variabelen](#global-variables)

### Snelle tips {#section_A2CC0302CAF14135BF8EF6171FB184F1}

* Alle algemene variabelen krijgen de voorkeur met de naamruimte &quot;main:&quot;: `$main::doc_count = 0;`
* Alle lokale variabelen worden gedeclareerd met &quot;my&quot;: `my $i = 0;`
* Subroutines worden bepaald in het initialisatiescript. Ze hebben geen expliciete naamruimte &#39;main:&#39; nodig: `sub my_sub {` `...`

   `}`

* Test `$main::search_content_type` alvorens u veranderingen in een dossier aanbrengt. Testen kan u helpen te voorkomen dat u onophoudelijke wijzigingen aanbrengt in binaire bestanden, zoals SWF-bestanden of PDF-bestanden:

   `if ($main::search_content_type =~ /^text\/html/) { ...`

* De `$main::search_content_type` is de volledige Content-Type header die door uw server wordt geleverd. Het kan soms een eenvoudig MIME-type bevatten, zoals &quot;text/html&quot;. Of het kan een MIME-type bevatten, gevolgd door andere informatie, zoals de codering van de tekenset van het document, zoals &quot;text/html&quot;; charset=iso-8859-1&quot;.
* Voor elk type niet-HTML-document kan `$main::search_content_type` verschillende waarden hebben. Het testen voor elke waarde in uw script wordt omslachtig. Sommige Word-documenten hebben bijvoorbeeld waarden van het inhoudstype &quot;application/msword&quot;, &quot;application/vnd.ms-word&quot; of &quot;application/x-msword&quot;. In dergelijke gevallen kan `$main::search_content_class` de volgende waarden gebruiken:

   * html
   * pdf
   * woord
   * excel
   * powerpoint
   * mp3
   * text

* In het voorbeeld komt het testen van `$main::search_content_class` op &quot;woord&quot; overeen met een van de drie mogelijke waarden voor inhoudstype.
* Als er niets vanaf het filterscript naar STDOUT wordt afgedrukt, wordt het document exact gebruikt zoals het is gedownload. Als u dus niets in een document hoeft te wijzigen, hoeft u STDIN niet naar STDOUT voor dat document te kopiëren.
* Als u alle tekst uit een document wilt verwijderen, drukt u een geldige bestands-STDOUT af. Als u bijvoorbeeld alle tekst volledig wilt verwijderen uit een HTML-document, doet u het volgende: `print "<html></html>";`

## Een initialisatiescript {#task_5A03B8D0C46E4674B7CE88203515803B} toevoegen

Het initialisatiescript is een manuscript Perl dat eens in werking wordt gesteld alvorens om het even welke documenten worden geïndexeerd.

U gebruikt het initialisatiescript in combinatie met een het filtreren manuscript, beëindigingsmanuscript, en URL maskers manuscript.

Zorg ervoor dat u uw site-index opnieuw genereert, zodat de resultaten van uw initialisatiescript zichtbaar zijn voor uw klanten.

Zie [Een incrementele index van een gefaseerde website configureren](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Een initialisatiescript toevoegen**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Filtering]** > **[!UICONTROL Initialization Script]**.
1. (Optioneel) Voer in het veld [!DNL Test URL] op de pagina [!DNL Initialization Script] de URL van een document op uw website in.

   Klik op een testoptie om de wijzigingen in de onbewerkte HTML-tekst weer te geven.

   Zie de het filtreren optieslijst onder **Toevoegend een het filtreren manuscript**.

   Klik **[!UICONTROL Test]** om tegen de het filtreren manuscripten en maskers URL te testen.

   Als u op **[!UICONTROL Test]** klikt, wordt het initialisatiescript niet bijgewerkt en opgeslagen.
1. Plak het script in het veld [!DNL Initialization Script].
1. (Optioneel) Klik op **[!UICONTROL Check Syntax]** om een snelle syntaxiscontrole van uw script uit te voeren door het filteren, initialiseren en beëindigen van scripts uit te voeren.

   **[!UICONTROL Check Syntax]** werkt het script niet bij en slaat het niet op.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Optioneel) Maak de gefaseerde site-index opnieuw als u een voorvertoning van de resultaten wilt zien.

   Zie [Een incrementele index van een gefaseerde website configureren](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Optioneel) Voer op de pagina [!DNL Initialization Script] een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Informatie over beëindigingsscript {#concept_AAD6B3B0E7124874AD0947096FC42F47}

U kunt [!DNL Termination Script] gebruiken om de inhoud van een document van het Web te veranderen alvorens het wordt geïndexeerd.

U kunt HTML-tags invoegen, irrelevante inhoud verwijderen en zelfs nieuwe HTML-metagegevens maken op basis van de URL, het MIME-type en de bestaande inhoud van een document. Het initialisatiescript is een manuscript Perl, dat krachtige koordbehandeling en de flexibiliteit van regelmatige uitdrukkingsaanpassing verstrekt. U gebruikt het beëindigingsmanuscript met een initialisatiescript, filtrerend manuscript, beëindigingsmanuscript, URL maskers manuscript, en test URL.

Het beëindigingsmanuscript wordt in werking gesteld eenmaal nadat alle documenten worden geïndexeerd. U kunt het beëindigingsmanuscript gebruiken om statusberichten van het het filtreren manuscript aan het indexlogboek te drukken. U of drukt de berichten aan STDERR, of als subroutine `_search_debug_log()`.

Sommige opties voor GNU diff-opdrachtregels die u kunt gebruiken in de modus **[!UICONTROL Expert (diff)]** op de pagina Script-script voor gefaseerde beëindiging, zijn onder andere:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>GNU diff, opdrachtregeloptie </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -b  </span> </p> </td> 
   <td colname="col2"> <p> Hiermee negeert u wijzigingen in de hoeveelheid witruimte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -B  </span> </p> </td> 
   <td colname="col2"> <p> Hiermee worden wijzigingen genegeerd waarmee lege regels worden ingevoegd of verwijderd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -c  </span> </p> </td> 
   <td colname="col2"> <p> Gebruikt de indeling voor contextuitvoer, waarin drie regels context worden weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -C-lijnen  </span> </p> </td> 
   <td colname="col2"> <p> Gebruikt de indeling van de contextuitvoer en geeft regels (een geheel getal) voor context weer, of drie als er geen regels zijn opgegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -i  </span> </p> </td> 
   <td colname="col2"> <p> negeert veranderingen in geval; U kunt instellen dat hoofdletters en kleine letters equivalent zijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -f  </span> </p> </td> 
   <td colname="col2"> <p> Hiermee maakt u uitvoer die er net zo uitziet als een Eed-script, maar die wijzigingen heeft in de volgorde waarin ze in het bestand worden weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -n  </span> </p> </td> 
   <td colname="col2"> <p> Output RCS-formaat verschilt; zoals <span class="codeph"> -f </span> behalve dat specificeert elke bevel het aantal lijnen die worden beïnvloed. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>-u </p> </td> 
   <td colname="col2"> <p> Gebruikt het verenigde outputformaat, dat drie lijnen van context toont. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -U-lijnen  </span> </p> </td> 
   <td colname="col2"> <p> Gebruikt het verenigde outputformaat, dat lijnen (een geheel) van context toont, of drie als geen lijnen wordt gegeven. </p> </td> 
  </tr> 
 </tbody> 
</table>

U kunt lokale variabelen, globale variabelen, of allebei in deze manuscripten gebruiken. Alle algemene variabelen krijgen de voorkeur met de naamruimte &quot;main::&quot;. Wanneer het beëindigingsmanuscript wordt begonnen, bevat zijn milieu de volgende standaarddossierhandvatten:

* STDIN - niets (retourneert direct EOF bij lezen)
* STDOUT - niets (als de gegevens aan STDOUT worden gedrukt, wordt het verworpen)
* STDERR - gegevens die naar STDERR worden afgedrukt, worden als een fout afgedrukt naar het indexlogboek

Bovendien, kunt u douaneberichten aan het indexlogboek schrijven gebruikend `_search_debug_log()` subroutine, zoals in het volgende voorbeeld:

```
# Log information to the Index Log 
_search_debug_log("Done processing document: " . $main::search_url);
```

Deze berichten verschijnen met het woord `DEBUG` als voorkeur, en niet geregistreerd als fouten.

Om het aantal documenten te tonen die door uw het filtreren manuscript als foutenlijn in het indexlogboek werden verwerkt, kunt u het volgende beëindigingsmanuscript gebruiken:

```
# Print the value of the document counter. 
print STDERR "Total docs: $main::doc_count\n"; 
# Or, using the log subroutine: 
_search_debug_log("Total docs: " . $main::doc_count);
```

Zie [Globale variabelen](#global-variables)

### Snelle tips {#section_5790EA7ACAC046CBA01F759F88E2460F}

* Alle algemene variabelen krijgen de voorkeur met de naamruimte &quot;main:&quot;: `$main::doc_count = 0;`
* Alle lokale variabelen worden gedeclareerd met &quot;my&quot;: `my $i = 0;`
* Subroutines worden bepaald in het initialisatiescript. Ze hebben geen expliciete naamruimte &#39;main:&#39; nodig: `sub my_sub {` `...`

   `}`

* Test `$main::search_content_type` alvorens u veranderingen in een dossier aanbrengt. Testen kan u helpen te voorkomen dat u onophoudelijke wijzigingen aanbrengt in binaire bestanden, zoals SWF-bestanden of PDF-bestanden:

   `if ($main::search_content_type =~ /^text\/html/) { ...`

* De `$main::search_content_type` is de volledige Content-Type header die door uw server wordt geleverd. Het kan soms een eenvoudig MIME-type bevatten, zoals &quot;text/html&quot;. Of het kan een MIME-type bevatten, gevolgd door andere informatie, zoals de codering van de tekenset van het document, zoals &quot;text/html&quot;; charset=iso-8859-1&quot;.
* Voor elk type niet-HTML-document kan `$main::search_content_type` verschillende waarden hebben. Het testen voor elke waarde in uw script wordt omslachtig. Sommige Word-documenten hebben bijvoorbeeld waarden van het inhoudstype &quot;application/msword&quot;, &quot;application/vnd.ms-word&quot; of &quot;application/x-msword&quot;. In dergelijke gevallen kan `$main::search_content_class` de volgende waarden gebruiken:

   * html
   * pdf
   * woord
   * excel
   * powerpoint
   * mp3
   * text

* In het voorbeeld komt het testen van `$main::search_content_class` op &quot;woord&quot; overeen met een van de drie mogelijke waarden voor inhoudstype.
* Als er niets vanaf het filterscript naar STDOUT wordt afgedrukt, wordt het document exact gebruikt zoals het is gedownload. Als u dus niets in een document hoeft te wijzigen, hoeft u STDIN niet naar STDOUT voor dat document te kopiëren.
* Als u alle tekst uit een document wilt verwijderen, drukt u een geldige bestands-STDOUT af. Als u bijvoorbeeld alle tekst volledig wilt verwijderen uit een HTML-document, doet u het volgende: `print "<html></html>";`

## Bezig met toevoegen van beëindigingsscript {#task_F0CFB412871642CFBC88132889C5B6F9}

Het beëindigingsmanuscript is een manuscript Perl dat eenmaal in werking wordt gesteld nadat alle documenten worden geïndexeerd.

U gebruikt het beëindigingsmanuscript in combinatie met een het filtreren manuscript, beëindigingsmanuscript, en URL maskers manuscript.

Zorg ervoor dat u uw site-index opnieuw genereert, zodat de resultaten van uw initialisatiescript zichtbaar zijn voor uw klanten.

Zie [Een incrementele index van een gefaseerde website configureren](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Een beëindigingsscript toevoegen**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Filtering]** > **[!UICONTROL Termination Script]**.
1. (Optioneel) Voer in het veld [!DNL Test URL] op de pagina [!DNL Termination Script] de URL van een document op uw website in.

   Klik op een testoptie om de wijzigingen in de onbewerkte HTML-tekst weer te geven.

   Zie de lijst van het filtreren opties onder **Toevoegend een het filtreren manuscript**.

   Klik **[!UICONTROL Test]** om tegen de het filtreren manuscripten en maskers URL te testen.

   Als u op **[!UICONTROL Test]** klikt, wordt het beëindigingsscript niet bijgewerkt en opgeslagen.
1. Plak het script in het veld [!DNL Termination Script].
1. (Optioneel) Klik op **[!UICONTROL Check Syntax]** om een snelle syntaxiscontrole van uw script uit te voeren door de initialisatie-, filter- en beëindigingsscripts uit te voeren.

   **[!UICONTROL Check Syntax]** werkt het script niet bij en slaat het niet op.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Optioneel) Maak de gefaseerde site-index opnieuw als u een voorvertoning van de resultaten wilt zien.

   Zie [Een incrementele index van een gefaseerde website configureren](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Optioneel) Voer op de pagina [!DNL Termination Script] een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Informatie over het script voor URL-maskers {#concept_384F32EA18F84853A7BA99A04009330B}

Door te filteren kunt u de inhoud van een webdocument wijzigen voordat het wordt geïndexeerd. U kunt HTML-tags invoegen, irrelevante inhoud verwijderen en zelfs nieuwe HTML-metagegevens maken op basis van de URL, het MIME-type en de bestaande inhoud van een document. Het URL-maskerscript is een Perl-script dat krachtige tekenreeksafhandeling en de flexibiliteit van reguliere expressies biedt.

Als u de inhoud wilt wijzigen van documenten die alleen in een specifiek gedeelte van uw website staan, kunt u opgeven of URL-maskers moeten worden opgenomen, URL-maskers moeten worden uitgesloten of beide, om de juiste pagina&#39;s te definiëren.

Als u alleen de documenten onder `"https://www.mysite.com/faqs/"` wilt wijzigen, kunt u de volgende set maskers gebruiken:

```
include https://www.mysite.com/faqs/ 
exclude *
```

U kunt reguliere expressie ook gebruiken in een URL-maskerscript, zoals in het volgende voorbeeld:

```
include regexp ^https://www\.mysite\.com.*/faqs/.*$ 
exclude *
```

Zie [Gewone uitdrukkingen](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

Maskers met scripts voor URL&#39;s worden beschouwd in de volgorde waarin u ze hebt ingevoerd in het veld [!DNL URL Masks]. Wanneer een document-URL overeenkomt met een masker, wordt dat document opgenomen of uitgesloten op basis van het type masker. Als de URL van een document niet overeenkomt met een URL-masker, wordt het document alleen opgenomen als het MIME-type &quot;text/html&quot; is. Alle andere MIME-typen zijn uitgesloten.

## Een URL-maskerscript toevoegen {#task_D18F2A496C1C45C997B5DA650AAF5D59}

Geef voor URL-include-maskers op en sluit maskers uit om de inhoud te wijzigen van documenten die alleen in een specifiek gedeelte van uw website bestaan.

Voordat de effecten van de instellingen voor URL-maskers zichtbaar zijn voor bezoekers, moet u de index van uw site opnieuw samenstellen.

**Een URL-maskerscript toevoegen**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Filtering]** > **[!UICONTROL URL Masks]**.
1. (Optioneel) Typ op de pagina [!DNL URL Masks] in het veld [!DNL Test URL] een URL van een document op uw website en klik vervolgens op **[!UICONTROL Test]** om de URL te testen op basis van de filterscripts en -maskers.

   Het test-URL-document wordt gedownload. Dit wordt gebruikt als STDIN-invoer voor het filterscript. Dan worden het filtreren, initialisatie, en beëindigingsmanuscripten in werking gesteld. Als er om het even welke output STDOUT van het het filtreren manuscript is dat de output in een nieuw browser venster wordt getoond.

   Als u op **[!UICONTROL Test]** klikt, wordt het script niet bijgewerkt en opgeslagen.
1. Voer in het veld [!DNL URL Masks] één URL-masker per regel in.
1. (Optioneel) Klik op **[!UICONTROL Check Syntax]** om een snelle syntaxiscontrole van uw URL-maskers uit te voeren door het filteren, initialiseren en beëindigen van scripts uit te voeren.

   **[!UICONTROL Check Syntax]** werkt het script niet bij en slaat het niet op.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Optioneel) Maak de gefaseerde site-index opnieuw als u een voorvertoning van de resultaten wilt zien.

   Zie [Een incrementele index van een gefaseerde website configureren](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Optioneel) Voer op de pagina [!DNL URL Masks] een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Informatie over inhoudstypen in filters {#concept_E3EFF4A148EA4D21AFD0A5453A00427E}

Hiermee kunt u selecteren welke inhoudstypen u voor dit account wilt filteren.

De tekst die in de geselecteerde inhoudstypen wordt gevonden, wordt omgezet in HTML en vervolgens verwerkt met het script dat is opgegeven in Filtrerend Script.

Zie [Scripts filteren](../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47).

U kunt onder andere de volgende inhoudssoorten selecteren:

* PDF-documenten
* Tekstdocumenten
* Adobe Flash-films
* Microsoft Word-bestanden
* Microsoft Office-bestanden (OpenXML)
* Microsoft Excel-bestanden
* Microsoft PowerPoint-bestanden
* Tekst in MP3-muziekbestanden

Voordat de effecten van de instellingen voor inhoudssoorten of wijzigingen in de instellingen zichtbaar zijn voor klanten, moet u de index van uw site opnieuw genereren.

## De inhoudstypen selecteren die worden gefilterd {#task_C46081FA425A43EC8FDE6EA4A52A170A}

Selecteer de inhoudstypen die u wilt doorgeven aan het script dat is opgegeven in Filterscript.

Zie [Scripts filteren](../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47).

**De inhoudstypen selecteren die worden gefilterd**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Filtering]** > **[!UICONTROL Content Types]**.
1. Controleer op de pagina [!DNL Content Types] de inhoudstypen die u wilt doorgeven aan het filterscript.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Optioneel) Maak de gefaseerde site-index opnieuw als u een voorvertoning van de resultaten wilt zien.

   Zie [Een incrementele index van een gefaseerde website configureren](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Optioneel) Voer op de pagina [!DNL Content Types] een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).
