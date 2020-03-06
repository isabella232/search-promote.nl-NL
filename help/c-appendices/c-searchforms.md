---
description: ongeldig
seo-description: ongeldig
seo-title: Zoekformulieren
solution: Target
title: Zoekformulieren
topic: Appendices,Site search and merchandising
uuid: 91153e3a-c437-47f3-8c2a-d9ac02965b8c
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a

---


# Zoekformulieren{#search-forms}

## Zoekformulieren {#concept_915FFF20FF644830B7B3C6E00F416BCB}

## Het gebruiken van inzamelingen in onderzoeksvormen {#reference_5A079AEEEFB84457892EF0870D0605C3}

De inzamelingen laten uw klanten specifieke gebieden van uw website zoeken. Afhankelijk van of u een drop-down lijst of een lijst van controledozen uitvoert, kunt u uw klanten laten één enkele inzameling of veelvoudige inzamelingen zoeken.

Zie ook [over Verzamelingen](../c-about-settings-menu/c-about-searching-menu.md#concept_62E42ACE53D54EEE9273433B86259127).

Het volgende voorbeeld toont vier verschillende inzamelingsnamen en de bijbehorende gebieden van de website die zij behandelen:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Naam verzameling </p> </th> 
   <th colname="col2" class="entry"> <p> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Producten </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_7AE70789C0914EBFBCCC7695C6F53B9E"> 
      <li id="li_72525BAA34E2442D86152F2FD8CA83D5"> https://www.mycompany.com/products.htm </li> 
      <li id="li_5CA4152239124BDBB251E6C94B15D45B"> https://www.mycompany.com/publish/ </li> 
      <li id="li_6E266736B3494696A3AFD841C4AFEC57"> https://www.mycompany.com/search/ </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Klanten </p> </td> 
   <td colname="col2"> <p>https://www.mycompany.com/customers/ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Nieuws </p> </td> 
   <td colname="col2"> <p>https://www.mycompany.com/news/ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Over Adobe </p> </td> 
   <td colname="col2"> <p>https://www.mycompany.com/company/ </p> </td> 
  </tr> 
 </tbody> 
</table>

De drop-down interface van de onderzoeksvorm laat gebruikers één inzameling selecteren en kijkt als het volgende:

![](assets/DropdownsearchformUI.png)

De drop-down onderzoeksvorm wordt geproduceerd met de volgende code van HTML:

```
<select name="sp_k"> 
<option value="">All of Adobe</option> 
<option value="Products">Products</option> 
<option value="Customers">Customers</option> 
<option value="News">News</option> 
<option value="About Adobe">About Adobe</option> 
</select>
```

Afwisselend, kon u een groep controledozen in uw onderzoeksvorm gebruiken zodat de bezoekers veelvoudige inzamelingen kunnen selecteren:

![](assets/checkboxes.png)

De vorm van het controlevakje onderzoek wordt geproduceerd met de volgende code van HTML:

```
<input type="checkbox" name="sp_k" value="">All of Adobe<br> 
<input type="checkbox" name="sp_k" value="Products">Products<br> 
<input type="checkbox" name="sp_k" value="Customers">Customers<br> 
<input type="checkbox" name="sp_k" value="News">News<br> 
<input type="checkbox" name="sp_k" value="About Adobe">About Adobe<br>
```

## Zoekresultaten {#section_BBDD5B44E2B349BC88D937F44583D350}

De markering van het onderzoeksmalplaatje `<search-input-collections>` produceert het vakje van de inzamelingslijst HTML in de onderzoeksresultaten en selecteert automatisch de inzameling die in het onderzoek wordt gespecificeerd. Als u controledozen wilt produceren in plaats daarvan, gebruik de `<search-input>` markering in plaats van de `<input>` markering als volgt:

```
<search-input type="checkbox" name="sp_k" value="">All of Adobe<br> 
<search-input type="checkbox" name="sp_k" value="Products">Products<br> 
<search-input type="checkbox" name="sp_k" value="Customers">Customers<br> 
<search-input type="checkbox" name="sp_k" value="News">News<br> 
<search-input type="checkbox" name="sp_k" value="About Adobe">About Adobe<br>
```

De `<search-input>` markeringsoutput een `<input>` markering en omvat de `checked` attributen als de inzameling in het onderzoek werd gespecificeerd.

## Het gebruiken van kaders met vormen {#reference_82CDDDA1E37042E4849EBF7EA05407C5}

U kunt uw framesets vormen om met plaatsonderzoek/merchandising te werken.

Meer over de kaders van HTML en het framesetelement van HTML leren, zie volgende URL:

[https://www.w3schools.com/html/html_frames.asp](https://www.w3schools.com/html/html_frames.asp)

Als uw plaats kaders gebruikt, kunt u een doelkader voor de verbindingen van het onderzoeksresultaat specificeren. Het standaarddoel is _self, dat verbindingen in het huidige kader of browser venster opent. U kunt, in plaats daarvan, plaats-specifieke of browser-gereserveerde doelstellingen specificeren:

* _top (browser-gereserveerd) resultaten open in het huidige browser venster en vervangen alle huidige kaders.
* _blank (browser-gereserveerd) resultaten open in een nieuw browser venster.
* _parent (browser-gereserveerd) resultaten open in het de ouderkader van het huidige kader.
* frame2 (plaats-specifiek) resultaten open in een kader genoemd &quot;frame2&quot;. U kunt de naam van om het even welk kader als waarde (bijvoorbeeld hoofd of inhoud) specificeren.

Als uw plaats geen kaders gebruikt, wilt u waarschijnlijk niet de standaarddoelnaam veranderen.

Als u een malplaatje van de resultaten van het douaneonderzoek voor uw website creeert, kunt u het gespecificeerde plaatsen met voeten treden door de `target` attributen van de `<search-link>` markering te gebruiken.

Het proces om framesets te vormen is als volgt:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Proces </p> </th> 
   <th colname="col02" class="entry"> <p>Procesbeschrijving </p> </th> 
   <th colname="col2" class="entry"> <p>Koppeling </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>1 </p> </td> 
   <td colname="col02"> <p>Voeg de vorm aan het gewenste kader in uw Web-pagina toe. </p> </td> 
   <td colname="col2"> <p> <a href="../c-appendices/c-searchforms.md#section_BAA8A502BB2243F8B5FF9783CDF2BFFD" type="section" format="dita" scope="local"> Het toevoegen van de code van de onderzoeksvorm aan een kader in uw... </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col02"> <p>Plaats het doelkader voor de pagina van onderzoeksresultaten. </p> </td> 
   <td colname="col2"> <p> <a scope="local" href="../c-appendices/c-searchforms.md#section_532CACB90888467093D95EACB64FDFA1" type="section" format="dita"> Het plaatsen van het doelkader voor de pagina van onderzoeksresultaten </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col02"> <p>Plaats het doel voor verbindingen die van de pagina van onderzoeksresultaten worden gemaakt. </p> </td> 
   <td colname="col2"> <p> <a scope="local" href="../c-appendices/c-searchforms.md#section_523248C5AC424D878321C21A23A5CD66" type="section" format="dita"> Het plaatsen van het doel voor verbindingen die van de onderzoeksresultaten worden gemaakt... </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col02"> <p>Geef de pagina's van het navigatiekader uit om hen te verhinderen worden geïndexeerd. </p> </td> 
   <td colname="col2"> <p> <a scope="local" href="../c-appendices/c-searchforms.md#section_C62E5F0EE1294D5EBD97E123E54433FC" type="section" format="dita"> Het uitgeven van de pagina's van het navigatiekader om hen te verhinderen... </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>5 </p> </td> 
   <td colname="col02"> <p>Test de onderzoeksvorm. </p> </td> 
   <td colname="col2"> <p> <a scope="local" href="../c-appendices/c-searchforms.md#section_43D8D4A7BF524DC480DFE5442F6A2E3C" type="section" format="dita"> Het testen van het onderzoeksformulier </a> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Het toevoegen van de code van de onderzoeksvorm aan een kader in uw Web-pagina {#section_BAA8A502BB2243F8B5FF9783CDF2BFFD}

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Form Source]**.

   De code van de HTML- onderzoeksvorm kijkt gelijkaardig aan het volgende:

   ```
   <!-- Adobe Target HTML for [your customer name] --> 
   <form method="get" action="https://search.atomz.com/search/"> 
   <input size=15 name="sp_q"><br> 
   <input type=submit value="Search"> 
   <input type=hidden name="sp_a" value="[your account number]"> 
   </form>
   ```

1. Voor de [!DNL Standard Form Source] pagina, selecteer en kopieer de code van de het onderzoeksvorm van HTML die op het tekstgebied verschijnt.
1. Kleef de code van de onderzoeksvorm in het kader u in uw frameset wilt.

   In het hieronder voorbeeld, wordt de code van de onderzoeksvorm gekleefd in navigatie kader-het smalle verticale kader op de linkerkant van het scherm.

   ![](assets/frames1.gif)

## Het plaatsen van het doelkader voor de pagina van onderzoeksresultaten {#section_532CACB90888467093D95EACB64FDFA1}

Als u uw code van de onderzoeksvorm in het verticale navigatiekader zoals hierboven plaatste, kunt u de onderzoeksresultaten in het grotere, belangrijkste kader tonen. In dit voorbeeld, roept u het belangrijkste kader &quot;lichaam&quot;en plaatst het als doelkader.

![](assets/frames2.gif)

1. Om het doelkader voor de resultatenpagina te specificeren, voeg een doel en een waarde aan de vorm toe door de volgende lijn in de code van de onderzoeksvorm van het volgende te veranderen:

   `<form method="get" action="https://search.atomz.com/search/">`

   op de volgende punten:

   `<form target="body" method="get" action="https://search.atomz.com/search/">`

   Zeker ben dat u citaten rond de waarde van het vormdoel zet.

Wanneer een klant een onderzoek van uw website uitvoert, verschijnen de onderzoeksresultaten in het &quot;lichaam&quot;kader van de Web-pagina.

## Het plaatsen van het doel voor verbindingen die van de pagina van onderzoeksresultaten worden gemaakt {#section_523248C5AC424D878321C21A23A5CD66}

U kunt het bestemmingskader plaatsen door uw malplaatje direct uit te geven.

Als uw onderzoeksresultaten in het &quot;lichaam&quot;kader verschijnen, wilt u waarschijnlijk de verbindingen in het &quot;lichaam&quot;kader openen, ook. Omdat dit het zelfde kader is, de doelwaarde `"_self"` die standaard het plaatsen is, te hoeven u om geen veranderingen aan te brengen.

U kunt het bestemmingskader voor resultatenverbindingen ook plaatsen. Het volgende is verscheidene voorbeelden van wat u kunt doen:

* Specificeer verschillende kaders voor de onderzoeksresultaten en hun verbindingen zodat de onderzoeksresultaten actief in hun eigen kader blijven terwijl elk geklikt resultaat in een afzonderlijk kader opent.
* Specificeer dat de onderzoeksresultaten open in een nieuw leeg venster, zodat uw oud venster actief met zijn originele inhoud blijft, die ook de onderzoeksresultaten bewaart.

De doelnaam kan of de naam van een kader zijn dat in uw HTML wordt gespecificeerd of het kan één van verscheidene van de volgende gebreken van HTML zijn:

* `target="_blank"` Open verbindingen in een nieuw, leeg, naamloos venster.

* `target="_self"` Standaard. Open verbindingen in het zelfde venster waar de onderzoeksresultaten verblijven. In dit geval, het originele venster van onderzoeksresultaten. Gebruik deze optie om een globaal toegewezen basisdoel met voeten te treden.

* `target="_parent"` Open verbindingen in ouderframeset van de verbindingspagina. Als het document geen ouder heeft, dan functioneert dit als `"_self"` door gebrek.

* `target="_top"` Open verbindingen in het volledige venster. Als het document reeds bij de bovenkant is, dan functioneert dit als `"_self"` door gebrek. Gebruik deze optie om uit een willekeurig diep kader het nestelen uit te breken.

Bijvoorbeeld, om het kader van de `_blank` doelbestemming te plaatsen kunt u het malplaatje op de volgende manier uitgeven:

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Templates]**.

1. Voor de [!DNL Staged Templates] pagina, in de lijst, klik de naam van malplaatje met het gerichte bestemmingskader.
1. Zoek de `<search-link>` tag. Your default `<search-link>` tag should look similar to the following:

   `<search-link><search-title length=100></search-link>`

1. Voeg het kaderdoel aan de `<search-link>` markering toe. In het voorbeeld hierboven, ga binnen `target="_blank"`. Zeker ben dat u het onderstreepteken en de citaten rond de doelwaarde omvat.

   De `<search-link>` markering verschijnt nu als het volgende:

   `<search-link target="_blank"><search-title length=100></search-link>`

Wanneer een bezoeker van een site een link met zoekresultaten kiest, wordt de gekoppelde pagina nu geopend in een nieuw, leeg venster.

## Het uitgeven van de pagina&#39;s van het navigatiekader om hen te verhinderen worden geïndexeerd {#section_C62E5F0EE1294D5EBD97E123E54433FC}

Typisch, wilt u uw navigatiekaders uitsluiten van wordt geïndexeerd met uw onderzoeksresultaten. Om deze functionaliteit te verwezenlijken, kunt u meta- markering aan die pagina&#39;s toevoegen. `noindex`

1. Open de de paginabron van HTML voor uw navigatiekader.
1. Voeg de volgende meta-markering binnen de `<head>` sectie van uw HTML toe:

   `<meta name="robots" content="noindex">`

   Bijvoorbeeld:

   ```
   <html> 
   <head> 
   <title>This page is a frameset that I do not want indexed</title> 
   <meta http-equiv="Content-Type" content="text/html; charset=iso-8859-1"> 
   <meta name="robots" content="noindex"> 
   </head>
   ```

## Het testen van het onderzoeksformulier {#section_43D8D4A7BF524DC480DFE5442F6A2E3C}

1. Ga naar uw website en navigeer naar een formulier.
1. Op het onderzoeksgebied, ga een paar onderzoekstermijnen in, en klik dan **[!UICONTROL Search]**.

   Het volgende is waar:

   * De pagina van onderzoeksresultaten verschijnt in het gespecificeerde doelkader.
   * De verbindingen van uw onderzoeksresultaten zijn in het gespecificeerde doelkader.
   * De het kaderresultaten van de navigatie verschijnen niet.
   Als u problemen ondervindt met frames na het testen van het zoekformulier, neemt u contact op met Customer Support.

## Voorbeeld van geavanceerd zoekformulier {#reference_82E1051918744EBA88A01E9E6AE42C4A}

U kunt de geavanceerde vormcode uitgeven om uw ontwerp en inhoudsbehoeften aan te passen, of extra onderzoeksparameters toevoegen of verwijderen.

Uw homepage is een goede plaats om een geavanceerd onderzoeksformulier op te nemen omdat vele klanten verwachten om onderzoeksvermogen daar te vinden. U kunt een HTML- pagina ook tot stand brengen die het onderzoeksformulier en andere nuttige informatie omvat, en dan met die pagina door uw website verbinden.

Als u veilige inhoud indexeert, kunt u de onderzoeksresultaten hebben die van de veilige servers van het Web van het Onderzoek worden gediend. Verander URL in de attributen van de de actieactie van de onderzoeksvorm in: action=&quot;https://search.atomz.com/search/&quot;om dit te doen.

>[!NOTE]
>
>Sommige redacteurs van HTML hebben probleem klevend de code van HTML van andere toepassingen. Als de code van HTML op uw Web-pagina als tekst verschijnt, kopieer en kleef de onderzoekscode in een eenvoudige tekstredacteur, zoals Blocnote op Vensters of Eenvoudige Tekst op MAC, en kopieer en deeg opnieuw dan van de eenvoudige tekstredacteur aan uw redacteur van HTML.

De parameters van het onderzoek worden gebruikt in geavanceerde code van de onderzoeksvorm om radioknopen, controledozen, en lijstvakjes tot stand te brengen die de klanten kunnen gebruiken om individuele onderzoeken aan te passen. De klanten kunnen het aantal getoonde onderzoeksresultaten, bijvoorbeeld, of een datumwaaier specificeren, of of de samenvattingen met onderzoeksresultaten-allen door opties tonen die op de geavanceerde onderzoeksvormen verschijnen.

Gebruikend de volgende steekproef geavanceerde onderzoeksvorm, toont de rest van dit onderwerp u hoe elke optie op de vorm gebruikend onderzoeksparameters wordt gecreeerd.

![](assets/advancedsearchform.png)

U kunt de volledige geavanceerde code van HTML van de onderzoeksvorm van de steekproef hierboven bekijken.

Zie [Geavanceerde HTML-code](../c-appendices/c-searchforms.md#reference_9AAD4A46B68D4D48865508982CB86DB9)voor zoekformulier.

Zie Automatische CSS [configureren](../c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96).

Zie de HTML-code van het zoekformulier [kopiëren in...](../c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

<table> 
 <thead> 
  <tr> 
   <th colname="col2" class="entry"> <p>Locatie op formulier </p> </th> 
   <th colname="col1" class="entry"> <p>Parameter </p> </th> 
   <th colname="col3" class="entry"> <p>HTML-code </p> </th> 
   <th colname="col4" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col2"> <p>Laat de geavanceerde opties van de onderzoeksvorm (verborgen gebied) toe </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> sp_advanced </span> </p> </td> 
   <td colname="col3"> <p> <span class="syntax html codeph"> &lt;invoertype=verborgen name="sp_advanced" waarde=1&gt; </span> </p> </td> 
   <td colname="col4"> <p>Geavanceerde zoekopties in- of uitschakelen. Bijvoorbeeld, kunt u een standaardonderzoeksformulier op uw homepage met een verbinding aan een tweede pagina zetten die een geavanceerde vorm bevat. In dit geval, zou u een exemplaar van uw standaardformulier binnen <span class="codeph"> &lt;search-if-not-advanced&gt; zetten...&lt;/search-if-not-advanced&gt; </span> sjabloontags. </p> <p>Een klant die een onderzoek van het standaardformulier uitvoert ziet een standaardonderzoeksformulier wanneer de onderzoeksresultaten worden getoond. Voor het geavanceerde scherm van de onderzoeksvorm, omvat u de <span class="codeph"> </span> &lt;input type=verborgen name="sp_advanced"waarde=1&gt; markering met de andere geavanceerde vormopties. </p> <p>U omvat ook een exemplaar van de geavanceerde onderzoeksvorm binnen &lt;search-if-advanced&gt;... &lt;/search-if-advanced&gt; sjabloontags. Een klant die een onderzoek van uw geavanceerde onderzoeksvorm uitvoert ziet een geavanceerd onderzoeksformulier wanneer de onderzoeksresultaten worden getoond. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> Pas om het even welk, allen, of uitdrukking aan </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> sp_p </span> </p> <p> </p> </td> 
   <td colname="col3"> <p> <code class="syntax html"> &lt;!--&nbsp;Allow&nbsp;"any,"&nbsp;"all,"&nbsp;or&nbsp;"phrase"&nbsp;--&gt; 
      &lt;input&nbsp;type=radio&nbsp;name="sp_p"&nbsp;value="any"&gt;Any&nbsp;word 
      &lt;input&nbsp;type=radio&nbsp;name="sp_p"&nbsp;value="all"&nbsp;checked&gt;All&nbsp;words 
      &lt;input&nbsp;type=radio&nbsp;name="sp_p"&nbsp;value="phrase"&gt;Exact&nbsp;phrase </code> </p> </td> 
   <td colname="col4"> <p>Sta uw klant toe om te specificeren dat "om het even welk woord,"alle woorden,"of "de nauwkeurige uitdrukking"aanwezig moet zijn voor een document om aan te passen. Wanneer de <span class="codeph"> sp_p </span> parameter wordt gespecificeerd, te hoeven de klanten niet om "+", of "-", of allebei in de onderzoeksvraag te gebruiken. </p> <p> Als de <span class="codeph"> sp_p </span> parameter wordt weggelaten, of als het aan "" of "om het even welk wordt geplaatst,"dan kunnen de klanten nog "+"en "-"specifiers gebruiken. Als de <span class="codeph"> sp_p </span> parameter aan "allen"of "uitdrukking wordt geplaatst,"dan gespecificeerd "+"en "-"wordt genegeerd. </p> <p>Je kunt meer weten over het gebruik van '+' en '-' in een zoekopdracht. </p> <p>Zie <a href="../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8" type="concept" format="dita" scope="local"> over zoekopdrachten </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> Correctie-gelijksoortige aanpassing </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> sp_w </span> </p> <p>en </p> <p> <span class="codeph"> sp_w_control </span> </p> <p> </p> </td> 
   <td colname="col3"> <p> <code class="syntax html"> &lt;!--&nbsp;Checkbox&nbsp;enables&nbsp;sound-alike&nbsp;matching&nbsp;--&gt; 
      &lt;input&nbsp;type=hidden&nbsp;name="sp_w_control"&nbsp;value=1&gt; 
      &lt;input&nbsp;type=checkbox&nbsp;name="sp_w"&nbsp;value="alike"&gt;&nbsp;Sound-alike&nbsp;matching </code> </p> </td> 
   <td colname="col4"> <p>Laat klanten correcte-gelijkaardige aanpassing toelaten of onbruikbaar maken. De correcte-gelijkaardige aanpassing staat verkeerd geschreven onderzoeksvragen toe om woorden aan te passen die "het geluid als"in uw documenten klinkt. </p> <p>Wanneer de <span class="codeph"> sp_w_control </span> parameter aan 1 wordt geplaatst en de <span class="codeph"> sp_w </span> parameter aan "gelijkaardig wordt geplaatst,"wordt de geproduceerde controledoos geselecteerd, toelatend geluid-gelijkaardige aanpassing door gebrek. </p> <p>Als de <span class="codeph"> sp_w </span> parameter aan "" wordt geplaatst, wordt de controledoos niet geselecteerd. </p> <p>Als u geen correcte-gelijkaardige aanpassing tijdens uw meest recente het indexeren verrichting toeliet, dan is de geluid-gelijkaardige aanpassing niet mogelijk en de <span class="codeph"> sp_w </span> parameter wordt genegeerd. Om de correcte-gelijkaardige aanpassing, op het productmenu toe te laten, klik <span class="uicontrol"> Taalkunde </span> &gt; <span class="uicontrol"> Woorden &amp; Taal </span> &gt; <span class="uicontrol"> Correct-Alike Aanpassing </span>. </p> <p>U kunt de parameters <span class="codeph"> sp_w </span> en <span class="codeph"> sp_w_control parameters op de volgende manier ook toewijzen </span> : </p> <p> <code class="syntax html"> &lt;!--&nbsp;Checkbox&nbsp;disables&nbsp;sound-alike&nbsp;matching&nbsp;--&gt; 
      &lt;input&nbsp;type=hidden&nbsp;name="sp_w_control"&nbsp;value=0&gt; 
      &lt;input&nbsp;type=checkbox&nbsp;name="sp_w"&nbsp;value="exact"&gt; 
      No&nbsp;sound-alike&nbsp;matching </code> </p> <p>In dit geval, wanneer de <span class="codeph"> sp_w_control </span> parameter aan 0 wordt geplaatst en de <span class="codeph"> sp_w </span> parameter aan "nauwkeurig wordt geplaatst,"de correcte-gelijkaardige aanpassing is gehandicapt door gebrek. Als de <span class="codeph"> sp_w </span> parameter aan ""dan wordt geplaatst correct-gelijkaardige aanpassing wordt toegelaten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Datumbereik aanpassen </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> sp_d </span> </p> <p> </p> </td> 
   <td colname="col3"> <p> <code class="syntax html"> &lt;!--Specifies&nbsp;type&nbsp;of&nbsp;date&nbsp;range&nbsp;searching&nbsp;to&nbsp;perform.--&gt; 
      &lt;input&nbsp;type=radio&nbsp;name="sp_d"&nbsp;value="custom"&nbsp;checked&gt; 
      &lt;input&nbsp;type=radio&nbsp;name="sp_d"&nbsp;value="specific"&gt; </code> </p> </td> 
   <td colname="col4"> <p>De <span class="codeph"> sp_d </span> parameter specificeert een waaier van douanegegevens die om aanpassen uit te voeren of een specifieke datumwaaier die aan uitvoering aanpassen. </p> <p>Voor de standaard geavanceerde onderzoeksvorm, wordt deze optie voorgesteld als radioknoopgroep met een drop-down lijst van "douane"datumwaaiers zoals geproduceerd met een <span class="codeph"> </span> sp_date_range parameter. Het omvat ook en een groep van "specifieke"begin en einddata die met <span class="codeph"> sp_start_day </span>, <span class="codeph"> sp_start_month </span>, <span class="codeph"> sp_start_year </span>, <span class="codeph"> sp_end_day </span>, <span class="codeph"> sp_end_month </span><span class="codeph"> </span> , en_end_year  parameters worden geproduceerd. </p> <p>Een "douane"datumwaaier is een genoemde waaier van data aan onderzoek. Bijvoorbeeld "Overal," "Vandaag," "Binnen het laatste jaar," etc. </p> <p>Een "specifieke"datumwaaier bestaat uit een begindatum en een einddatum. Bijvoorbeeld van "8 september 2009 tot 18 oktober 2011". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Datumbereik aanpassen: aangepast datumbereik </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> sp_date_range </span> </p> <p> </p> </td> 
   <td colname="col3"> <p> <code class="syntax html"> &lt;!--Selection&nbsp;list&nbsp;for&nbsp;custom&nbsp;date&nbsp;range.--&gt; 
      &lt;select&nbsp;name="sp_date_range"&nbsp;size=1&gt; 
      &lt;option&nbsp;value=-1&nbsp;selected&gt;Anytime&lt;/option&gt; 
      &lt;option&nbsp;value=7&gt;Within&nbsp;the&nbsp;last&nbsp;week&lt;/option&gt; 
      &lt;option&nbsp;value=14&gt;Within&nbsp;the&nbsp;last&nbsp;2&nbsp;weeks&lt;/option&gt; 
      &lt;option&nbsp;value=30&gt;Within&nbsp;the&nbsp;last&nbsp;30&nbsp;days&lt;/option&gt; 
      &lt;option&nbsp;value=60&gt;Within&nbsp;the&nbsp;last&nbsp;60&nbsp;days&lt;/option&gt; 
      &lt;option&nbsp;value=90&gt;Within&nbsp;the&nbsp;last&nbsp;90&nbsp;days&lt;/option&gt; 
      &lt;option&nbsp;value=180&gt;Within&nbsp;the&nbsp;last&nbsp;180&nbsp;days&lt;/option&gt; 
      &lt;option&nbsp;value=365&gt;Within&nbsp;the&nbsp;last&nbsp;year&lt;/option&gt; 
      &lt;option&nbsp;value=730&gt;Within&nbsp;the&nbsp;last&nbsp;two&nbsp;years&lt;/option&gt; 
      &lt;/select&gt; </code> </p> </td> 
   <td colname="col4"> <p>De <span class="codeph"> </span> sp_date_range parameter wordt gebruikt om een "douane"datumwaaier tot stand te brengen. Bijvoorbeeld "Overal," "Vandaag," "Binnen het laatste jaar" enzovoort. </p> <p>De waarden groter dan of gelijk aan nul specificeren het aantal dagen aan onderzoek vóór vandaag. Bijvoorbeeld, specificeert een waarde van 0 "vandaag,"een waarde van "1"specificeert "vandaag en Gisteren,"een waarde van "30"specificeert "binnen de Laatste 30 Dagen,"etc. De waarden minder dan nul specificeren als volgt een douanewaaier: </p> <p> 
     <ul id="ul_E65DDE33883F441F9730F315E485AD98"> 
      <li id="li_83E9466AB9D7438A8544001F6B007186"> <p>-1 = "Altijd,"het zelfde als specificerend geen datumwaaier. </p> </li> 
      <li id="li_38AB8D97179A47F9B860A96EA09119BB"> <p>-2 = "Deze week,"die onderzoeken van Zondag aan Zaterdag van de huidige week. </p> </li> 
      <li id="li_F4C3A8658428418A8A06FBAAB4733C68"> <p>-3 = "Vorige week,"die onderzoeken van Zondag aan Zaterdag van de week vóór de huidige week. </p> </li> 
      <li id="li_DF2D0B043A4E4DE9BE8D82E69A76E793"> <p>-4 = "Deze maand,"die data binnen de huidige maand zoekt. </p> </li> 
      <li id="li_76BC4C2CED574E2A81448158828BFF1B"> <p>-5 = "Vorige maand,"die data binnen de maand vóór de huidige maand zoekt. </p> </li> 
      <li id="li_17FF849384FB46D58AF6FF1D3BC408C8"> <p>-6 = "Dit jaar,"die onderzoeken data binnen het lopende jaar. </p> </li> 
      <li id="li_E2B8B4DFF3914BBDB86D0EB77F52B305"> <p>-7 = "Vorig jaar,"die onderzoeken data binnen het jaar vóór het huidige jaar. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Datumbereik aanpassen: begindatums </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> sp_start_day, sp_start_month, sp_start_year </span> </p> <p> </p> </td> 
   <td colname="col3"> </td> 
   <td colname="col4"> <p>Deze drievoud van numerieke waarden specificeert de begindatum van een specifieke datumwaaier aan onderzoek. Zeker ben dat u alle drie waarden specificeert omdat een gedeeltelijk gespecificeerde datum wordt genegeerd. </p> <p>Het is legaal om enkel de begindatum, enkel de einddatum, of zowel de begin als einddatum te specificeren. Als enkel de begindatum wordt gespecificeerd, omvat het onderzoek passende documenten die op of na de begindatum worden gedateerd. Als alleen de einddatum wordt opgegeven, bevat de zoekopdracht ook overeenkomende documenten op of vóór de einddatum. Als zowel de begindatum als de einddatum worden opgegeven, bevat de zoekopdracht de bijbehorende documenten vanaf de begindatum tot de einddatum. </p> <p>Alle data worden gezocht met betrekking tot Greenwich Mean Time. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> Datumbereik aanpassen: einddatums </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> sp_end_day, sp_end_month, sp_end_year </span> </p> <p> </p> </td> 
   <td colname="col3"> </td> 
   <td colname="col4"> <p>Deze drievoud van numerieke waarden specificeert de einddatum van de specifieke datumwaaier aan onderzoek. Zeker ben dat u alle drie waarden specificeert omdat een gedeeltelijk gespecificeerde datum wordt genegeerd. </p> <p>Het is legaal om enkel de begindatum, enkel de einddatum, of zowel de begin als einddatum te specificeren. Als enkel de begindatum wordt gespecificeerd, omvat het onderzoek passende documenten die op of na de begindatum worden gedateerd. Als alleen de einddatum wordt opgegeven, bevat de zoekopdracht ook overeenkomende documenten op of vóór de einddatum. Als zowel het begin als de einddatum worden gespecificeerd, omvat het onderzoek passende documenten van de begindatum tot de einddatum. </p> <p>Alle data worden gezocht met betrekking tot Greenwich Mean Time. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Binnen zoekveld </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> sp_x </span> </p> </td> 
   <td colname="col3"> <p> <code class="syntax html"> &lt;!--&nbsp;List&nbsp;box&nbsp;selects&nbsp;the&nbsp;search&nbsp;field&nbsp;--&gt; 
      Within&nbsp;&lt;select&nbsp;name="sp_x"&nbsp;size=1&gt; 
      &lt;option&nbsp;value="any"&nbsp;selected&gt;Anywhere&lt;/option&gt; 
      &lt;option&nbsp;value="title"&gt;Title&lt;/option&gt; 
      &lt;option&nbsp;value="desc"&gt;Description&lt;/option&gt; 
      &lt;option&nbsp;value="keys"&gt;Keywords&lt;/option&gt; 
      &lt;option&nbsp;value="body"&gt;Body&lt;/option&gt; 
      &lt;option&nbsp;value="alt"&gt;Alternate&nbsp;text&lt;/option&gt; 
      &lt;option&nbsp;value="url"&gt;URL&lt;/option&gt; 
      &lt;option&nbsp;value="target"&gt;Target&lt;/option&gt; 
      &lt;option&nbsp;value="date"&gt;Date&lt;/option&gt;* 
      &lt;/select&gt; </code> </p> </td> 
   <td colname="col4"> <p>Het <span class="codeph"> sp_x </span> lijstvakje laat uw klanten het gebied specificeren waarin om naar de vraagkoorden te zoeken. </p> <p>De klanten kunnen of alle gebieden, de titel, de documentbeschrijving, de documentsleutelwoorden, het lichaam, afwisselende tekst, URL van het document, datum, of doelsleutelwoorden kiezen. </p> <p>Wanneer de <span class="codeph"> sp_x </span> parameter wordt gebruikt, te hoeven de klanten niet om "titel te specificeren:,"desc:,"sleutels:,"het lichaam:,"alt:,""url:,"en "doel:"in de koorden van de onderzoeksvraag. </p> <p>Als de <span class="codeph"> sp_x </span> parameter wordt weggelaten, of als het aan "" of "om het even welk wordt geplaatst,"dan kunnen de klanten nog de gebied specifier koorden gebruiken. Als de <span class="codeph"> sp_x </span> parameter aan een specifiek gebied wordt geplaatst, worden alle andere gebied specifier koorden genegeerd. </p> <p>Zie <a href="../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8" type="concept" format="dita" scope="local"> over zoekopdrachten </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Resultaattelling weergeven </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> sp_c </span> </p> </td> 
   <td colname="col3"> <p> <code class="syntax html"> &lt;!--&nbsp;List&nbsp;box&nbsp;selects&nbsp;number&nbsp;of&nbsp;results&nbsp;to&nbsp;show&nbsp;per&nbsp;page&nbsp;--&gt; 
      Show&nbsp;&lt;select&nbsp;name="sp_c"&nbsp;size=1&gt; 
      &lt;option&nbsp;value=5&gt;5&lt;/option&gt; 
      &lt;option&nbsp;value=10&nbsp;selected&gt;10&lt;/option&gt; 
      &lt;option&nbsp;value=25&gt;25&lt;/option&gt; 
      &lt;option&nbsp;value=50&gt;50&lt;/option&gt; 
      &lt;option&nbsp;value=100&gt;100&lt;/option&gt; 
      &lt;/select&gt;&nbsp;results </code> </p> </td> 
   <td colname="col4"> <p>Laat klanten het aantal onderzoeksresultaten kiezen die op elke pagina van onderzoeksresultaten worden getoond. </p> <p>U kunt zo veel of zo weinig keuzen in de vorm hebben zoals u wilt. Zorg ervoor de "waarde="waarde de getoonde waarde aanpast. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Samenvattingen weergeven of verbergen </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> sp_m </span> </p> </td> 
   <td colname="col3"> <p> <code class="syntax html"> &lt;!--&nbsp;Show&nbsp;or&nbsp;hide&nbsp;summaries&nbsp;in&nbsp;search&nbsp;results&nbsp;--&gt; 
      &lt;select&nbsp;name="sp_m"&nbsp;size=1&gt; 
      &lt;option&nbsp;value=1&nbsp;selected&gt;with&lt;/option&gt; 
      &lt;option&nbsp;value=0&gt;without&lt;/option&gt; 
      &lt;/select&gt;&nbsp;summaries&nbsp; </code> </p> </td> 
   <td colname="col4"> <p>Laat klanten kiezen of de summiere tekst voor elke gelijke wordt getoond. </p> <p>Plaats de waarde aan 1 als u samenvattingen wilt tonen. Plaats de waarde aan 0 als u samenvattingen wilt verbergen. U kunt de parameter met een reeks radioknopen, zoals in het volgende voorbeeld ook gebruiken: </p> <p> <code class="syntax html"> &lt;!--&nbsp;Show&nbsp;or&nbsp;hide&nbsp;summaries&nbsp;in&nbsp;search&nbsp;results&nbsp;--&gt; 
      &lt;input&nbsp;type=radio&nbsp;name="sp_m"&nbsp;value=1&nbsp;selected&gt;Show&nbsp;summaries 
      &lt;input&nbsp;type=radio&nbsp;name="sp_m"&nbsp;value=0&gt;Hide&nbsp;summaries </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Sorteren op resultaten </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> sp_s </span> </p> </td> 
   <td colname="col3"> <p> <code class="syntax html"> &lt;!--&nbsp;Sort&nbsp;results&nbsp;by&nbsp;relevance&nbsp;or&nbsp;by&nbsp;date&nbsp;--&gt; 
      Sort&nbsp;by&nbsp;&lt;select&nbsp;name="sp_s"&nbsp;size=1&gt; 
      &lt;option&nbsp;value=0&nbsp;selected&gt;relevance&lt;/option&gt; 
      &lt;option&nbsp;value=1&gt;date&lt;/option&gt; 
      &lt;/select&gt; </code> </p> </td> 
   <td colname="col4"> <p>Laat klanten verkiezen of de resultaten in orde van relevantie of datum vermeld zijn. </p> <p>Wanneer de waarde aan 1 wordt geplaatst, zijn de resultaten vermeld van het onlangs veranderde document in het minst onlangs veranderde document. Wanneer de waarde aan 0 wordt geplaatst, zijn de resultaten vermeld van het meest relevant voor het minst relevant. U kunt deze parameter met radioknopen zoals in het volgende voorbeeld ook gebruiken: </p> <p> <code class="syntax html"> &lt;!--&nbsp;Sort&nbsp;results&nbsp;by&nbsp;relevance&nbsp;or&nbsp;by&nbsp;date&nbsp;--&gt; 
      &lt;input&nbsp;type=radio&nbsp;name="sp_s"&nbsp;value=0&nbsp;selected&gt;Sort&nbsp;by&nbsp;relevance 
      &lt;input&nbsp;type=radio&nbsp;name="sp_s"&nbsp;value=1&gt;Sort&nbsp;by&nbsp;date </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Geavanceerde zoekformulier HTML-code {#reference_9AAD4A46B68D4D48865508982CB86DB9}

De de vormcode van HTML die wordt gebruikt om de geavanceerde onderzoeksvorm te veroorzaken die bij de bovenkant van het onderwerp van de Steekproef geavanceerde onderzoeksvorm wordt getoond.

Zie [Voorbeeld van geavanceerd zoekformulier](../c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A).

Als je deze code gebruikt, moet je de `sp_a` waarde van `sp99999999` met je werkelijke rekeningnummer vervangen.

Om uw rekeningsaantal, op het productmenu te vinden, klik **[!UICONTROL Settings]** > **[!UICONTROL Account Options]** > **[!UICONTROL Account Settings]**.

```
<form method="get" action="https://search.atomz.com/search/"> 
<table cellspacing=0 cellpadding=0 border=0> 
<tr><td colspan=4> 
<b>Search For:</b><br> 
<input size=35 name="sp_q"> 
<!-- The "Search" button --> 
<input type=submit value="Search"> 
<input type=hidden name="sp_a" value="sp99999999"> 
<input type=hidden name="sp_f" value="ISO-8859-1"> 
</td></tr> 
<input type=hidden name="sp_advanced" value=1> 
<!-- Allow "any," "all," or "phrase" --> 
<tr><td valign=top> 
<b>Match: </b> 
</td><td colspan=4> 
<input type=radio name="sp_p" value="any">Any word 
<input type=radio name="sp_p" value="all" checked>All words 
<input type=radio name="sp_p" value="phrase">Exact phrase<br> 
<!-- Checkbox enables sound-alike matching --> 
<input type=hidden name="sp_w_control" value=1> 
<input type=checkbox name="sp_w" value="alike" checked> 
Sound-alike matching 
</td></tr> 
<!-- Date range criteria --> 
<tr><td><b>Dated:</b></td><td colspan=4> 
<input type=radio name="sp_d" value="custom" checked> 
<select name="sp_date_range" size=1> 
<option value=-1 selected>Anytime</option> 
<option value=7>Within the last week</option> 
<option value=14>Within the last 2 weeks</option> 
<option value=30>Within the last 30 days</option> 
<option value=60>Within the last 60 days</option> 
<option value=90>Within the last 90 days</option> 
<option value=180>Within the last 180 days</option> 
<option value=365>Within the last year</option> 
<option value=730>Within the last two years</option> 
</select> 
</td></tr> 
<tr><td></td><td rowspan=2> 
<input type=radio name="sp_d" value=specific> 
</td><td align=right>From:</td><td> 
<select name="sp_start_month" size=1> 
<option value=0 selected></option> 
<option value=1>January</option> 
<option value=2>February</option> 
<option value=3>March</option> 
<option value=4>April</option> 
<option value=5>May</option> 
<option value=6>June</option> 
<option value=7>July</option> 
<option value=8>August</option> 
<option value=9>September</option> 
<option value=10>October</option> 
<option value=11>November</option> 
<option value=12>December</option> 
</select> 
<select name="sp_start_day" size=1> 
<option value=0 selected></option> 
<option value=1>1</option> 
<option value=2>2</option> 
<option value=3>3</option> 
<option value=4>4</option> 
<option value=5>5</option> 
<option value=6>6</option> 
<option value=7>7</option> 
<option value=8>8</option> 
<option value=9>9</option> 
<option value=10>10</option> 
<option value=11>11</option> 
<option value=12>12</option> 
<option value=13>13</option> 
<option value=14>14</option> 
<option value=15>15</option> 
<option value=16>16</option> 
<option value=17>17</option> 
<option value=18>18</option> 
<option value=19>19</option> 
<option value=20>20</option> 
<option value=21>21</option> 
<option value=22>22</option> 
<option value=23>23</option> 
<option value=24>24</option> 
<option value=25>25</option> 
<option value=26>26</option> 
<option value=27>27</option> 
<option value=28>28</option> 
<option value=29>29</option> 
<option value=30>30</option> 
<option value=31>31</option> 
</select> 
<!--comma-->, 
<input size=4 name="sp_start_year"> 
</td></tr> 
<tr><td></td> 
<td align=right>To:</td><td> 
<select name="sp_end_month" size=1> 
<option value=0 selected></option> 
<option value=1>January</option> 
<option value=2>February</option> 
<option value=3>March</option> 
<option value=4>April</option> 
<option value=5>May</option> 
<option value=6>June</option> 
<option value=7>July</option> 
<option value=8>August</option> 
<option value=9>September</option> 
<option value=10>October</option> 
<option value=11>November</option> 
<option value=12>December</option> 
</select> 
<select name="sp_end_day" size=1> 
<option value=0 selected></option> 
<option value=1>1</option> 
<option value=2>2</option> 
<option value=3>3</option> 
<option value=4>4</option> 
<option value=5>5</option> 
<option value=6>6</option> 
<option value=7>7</option> 
<option value=8>8</option> 
<option value=9>9</option> 
<option value=10>10</option> 
<option value=11>11</option> 
<option value=12>12</option> 
<option value=13>13</option> 
<option value=14>14</option> 
<option value=15>15</option> 
<option value=16>16</option> 
<option value=17>17</option> 
<option value=18>18</option> 
<option value=19>19</option> 
<option value=20>20</option> 
<option value=21>21</option> 
<option value=22>22</option> 
<option value=23>23</option> 
<option value=24>24</option> 
<option value=25>25</option> 
<option value=26>26</option> 
<option value=27>27</option> 
<option value=28>28</option> 
<option value=29>29</option> 
<option value=30>30</option> 
<option value=31>31</option> 
</select> 
<!--comma-->, 
<input size=4 name="sp_end_year"> 
</td></tr> 
<!-- List box selects the search field --> 
<tr><td valign=top> 
<b>Within: </b> 
</td><td colspan=4><select name="sp_x" size=1> 
<option value="any" selected>Anywhere</option> 
<option value="title">Title</option> 
<option value="desc">Description</option> 
<option value="keys">Keywords</option> 
<option value="body">Body</option> 
<option value="alt">Alternate text</option> 
<option value="url">URL</option> 
<option value="target">Target</option> 
</select> 
</td></tr> 
<!-- List box selects number of results to show per page --> 
<tr><td valign=top> 
<b>Show: </b> 
</td><td colspan=4><select name="sp_c" size=1> 
<option value=5>5</option> 
<option value=10 selected>10</option> 
<option value=25>25</option> 
<option value=50>50</option> 
<option value=100>100</option> 
</select> results  
<!-- Show or hide summaries in search results --> 
<select name="sp_m" size=1> 
<option value=1 selected>with</option> 
<option value=0>without</option> 
</select> summaries<br> 
</td></tr> 
<!-- Sort results by relevance or by date --> 
<tr><td valign=top> 
<b>Sort by: </b> 
</td><td colspan=4><select name="sp_s" size=1> 
<option value=0 selected>relevance</option> 
<option value=1>date</option> 
</select> 
</td></tr> 
</table> 
</form>
```

## Geavanceerde sjablooncode voor zoekformulieren {#reference_D762C22E754E462DBEECD88D2C3FA579}

U kunt de geavanceerde code van HTML van de onderzoeksvorm aan uw malplaatje toevoegen dusdanig dat de standaardkeus voor om het even welke parameter het zelfde als het vorige onderzoek is.

Met andere woorden, als een klant op het **[!UICONTROL Exact phrase]** keuzerondje klikt, kunt u ervoor zorgen dat de keuzerondje standaard is geselecteerd wanneer de zoekresultaten worden weergegeven.

Deze functionaliteit wordt verwezenlijkt door alle &quot;gecontroleerde&quot;of &quot;geselecteerde&quot;specifiers van de standaardmarkeringen van HTML te verwijderen, en dan de volgende markeringen van HTML te vervangen:

* `<input>`
* `<select>`
* `<option>`
* `</option>`
* `</select>`

met de volgende bijbehorende sjabloontags:

* `<search-input>`
* `<search-select>`
* `<search-option>`
* `</search-option>`
* `</search-select>`

Om dit te doen, gebruikt u de volgende code als `<form>` markering op uw onderzoeksmalplaatje.

```
<!-- Adobe Target results section.--> 
 
<!-- Show heading and logo graphic. --> 
<SEARCH-IF-RESULTS> 
<b>SEARCH RESULTS <SEARCH-LOWER> - <SEARCH-UPPER></b> 
of <SEARCH-TOTAL> total results for <b><SEARCH-QUERY></b><br> 
</SEARCH-IF-RESULTS> 
<SEARCH-IF-NOT-RESULTS> 
<b>SEARCH RESULTS</b> for <b><SEARCH-QUERY></b><br> 
</SEARCH-IF-NOT-RESULTS> 
<SEARCH-LOGO><br> 
 
<!-- Display Results. --> 
<SEARCH-RESULTS LENGTH=160> 
<p><b><SEARCH-LINK><SEARCH-TITLE LENGTH=160></SEARCH-LINK></b><br> 
<SEARCH-IF-SHOW-SUMMARIES> 
<SEARCH-IF-CONTEXT LENGTH=240><SEARCH-CONTEXT><br></SEARCH-IF-CONTEXT> 
<font size="-1"><SEARCH-URL LENGTH=60></font><br> 
</SEARCH-IF-SHOW-SUMMARIES> 
</SEARCH-RESULTS> 
 
<!-- If no results, show a message. --> 
<SEARCH-IF-NOT-RESULTS><p> 
Sorry, no matches were found containing <b><SEARCH-QUERY>.</b> 
</SEARCH-IF-NOT-RESULTS> 
<!-- Show By Relevance, By Date links, Show/Hide Summaries links. --> 
<SEARCH-IF-RESULTS><p> 
<SEARCH-IF-SORT-BY-DATE> 
<b><SEARCH-SORT-BY-SCORE COUNT=10>Sort By Relevance</SEARCH-SORT-BY-SCORE></b> 
</SEARCH-IF-SORT-BY-DATE> 
<SEARCH-IF-SORT-BY-SCORE> 
<b><SEARCH-SORT-BY-DATE COUNT=10>Sort By Date</SEARCH-SORT-BY-DATE></b> 
</SEARCH-IF-SORT-BY-SCORE> 
| <b> 
<SEARCH-IF-SHOW-SUMMARIES> 
<SEARCH-HIDE-SUMMARIES COUNT=20>Hide Summaries</SEARCH-HIDE-SUMMARIES> 
</SEARCH-IF-SHOW-SUMMARIES> 
<SEARCH-IF-HIDE-SUMMARIES> 
<SEARCH-SHOW-SUMMARIES COUNT=10>Show Summaries</SEARCH-SHOW-SUMMARIES> 
</SEARCH-IF-HIDE-SUMMARIES> 
</b><br> 
</SEARCH-IF-RESULTS> 
 
<!-- Display Prev & Next links. --> 
<SEARCH-IF-RESULTS> 
<SEARCH-IF-PREV-COUNT> 
<b><SEARCH-PREV>Prev <SEARCH-PREV-COUNT></SEARCH-PREV></b> 
<SEARCH-IF-NEXT-COUNT> | </SEARCH-IF-NEXT-COUNT> 
</SEARCH-IF-PREV-COUNT> 
<SEARCH-IF-NEXT-COUNT> 
<b><SEARCH-NEXT>Next <SEARCH-NEXT-COUNT></SEARCH-NEXT></b><br> 
</SEARCH-IF-NEXT-COUNT><p> 
</SEARCH-IF-RESULTS> 
 
<!-- Put up the next form. --> 
<form method="get" action="https://search.atomz.com/search/"> 
<SEARCH-IF-NOT-ADVANCED> 
<SEARCH-INPUT-ACCOUNT> 
<SEARCH-INPUT-GALLERY> 
<SEARCH-INPUT-QUERY SIZE=25> 
<SEARCH-INPUT type=hidden name=sp_p> 
<input type=submit value="New Search"> 
<SEARCH-IF-INPUT-COLLECTIONS> 
<br><SEARCH-INPUT-COLLECTIONS> 
</SEARCH-IF-INPUT-COLLECTIONS> 
</SEARCH-IF-NOT-ADVANCED> 
<SEARCH-IF-ADVANCED> 
<table cellspacing=0 cellpadding=0 border=0> 
<tr><td colspan=4> 
<b>Search For:</b><br> 
<SEARCH-INPUT-QUERY SIZE=35> 
 
<!-- The "Search" button --> 
<input type=submit value="New Search"> 
<SEARCH-INPUT-ACCOUNT> 
<SEARCH-INPUT-GALLERY> 
</td></tr> 
<SEARCH-IF-INPUT-COLLECTIONS> 
<!-- Collections --> 
<tr><td> 
<b>In: </b> 
</td><td colspan=4> 
<SEARCH-INPUT-COLLECTIONS> 
</td></tr> 
</SEARCH-IF-INPUT-COLLECTIONS> 
<input type=hidden name="sp_advanced" value=1> 
 
<!-- Allow "any," "all," or "phrase" --> 
<tr><td valign=top> 
<b>Match: </b> 
</td><td colspan=4> 
<SEARCH-INPUT type=radio name="sp_p" value="any">Any word 
<SEARCH-INPUT type=radio name="sp_p" value="all">All words 
<SEARCH-INPUT type=radio name="sp_p" value="phrase">Exact phrase<br> 
<!-- Checkbox enables sound-alike matching --> 
<input type=hidden name="sp_w_control" value=1> 
<SEARCH-INPUT type=checkbox name="sp_w" value="alike">Sound-alike matching 
</td></tr> 
 
<!-- Date range section --> 
<tr> 
<td><b>Dated:</b></td> 
<td colspan=3> 
<SEARCH-INPUT type=radio name="sp_d" value="custom"> 
<SEARCH-SELECT name="sp_date_range" size=1> 
<SEARCH-OPTION value=-1>Anytime</SEARCH-OPTION> 
<SEARCH-OPTION value=7>Within the last week</SEARCH-OPTION> 
<SEARCH-OPTION value=14>Within the last 2 weeks</SEARCH-OPTION> 
<SEARCH-OPTION value=30>Within the last 30 days</SEARCH-OPTION> 
<SEARCH-OPTION value=60>Within the last 60 days</SEARCH-OPTION> 
<SEARCH-OPTION value=90>Within the last 90 days</SEARCH-OPTION> 
<SEARCH-OPTION value=180>Within the last 180 days</SEARCH-OPTION> 
<SEARCH-OPTION value=365>Within the last year</SEARCH-OPTION> 
<SEARCH-OPTION value=730>Within the last two years</SEARCH-OPTION> 
</SEARCH-SELECT> 
</td></tr> 
<tr><td></td><td rowspan=2> 
<SEARCH-INPUT type=radio name="sp_d" value=specific></td> 
<td align=right>From:</td><td> 
<SEARCH-SELECT name="sp_start_month" size=1> 
<SEARCH-OPTION value=0></SEARCH-OPTION> 
<SEARCH-OPTION value=1>January</SEARCH-OPTION> 
<SEARCH-OPTION value=2>February</SEARCH-OPTION> 
<SEARCH-OPTION value=3>March</SEARCH-OPTION> 
<SEARCH-OPTION value=4>April</SEARCH-OPTION> 
<SEARCH-OPTION value=5>May</SEARCH-OPTION> 
<SEARCH-OPTION value=6>June</SEARCH-OPTION> 
<SEARCH-OPTION value=7>July</SEARCH-OPTION> 
<SEARCH-OPTION value=8>August</SEARCH-OPTION> 
<SEARCH-OPTION value=9>September</SEARCH-OPTION> 
<SEARCH-OPTION value=10>October</SEARCH-OPTION> 
<SEARCH-OPTION value=11>November</SEARCH-OPTION> 
<SEARCH-OPTION value=12>December</SEARCH-OPTION> 
</SEARCH-SELECT> 
<SEARCH-SELECT name="sp_start_day" size=1> 
<SEARCH-OPTION value=0></SEARCH-OPTION> 
<SEARCH-OPTION value=1>1</SEARCH-OPTION> 
<SEARCH-OPTION value=2>2</SEARCH-OPTION> 
<SEARCH-OPTION value=3>3</SEARCH-OPTION> 
<SEARCH-OPTION value=4>4</SEARCH-OPTION> 
<SEARCH-OPTION value=5>5</SEARCH-OPTION> 
<SEARCH-OPTION value=6>6</SEARCH-OPTION> 
<SEARCH-OPTION value=7>7</SEARCH-OPTION> 
<SEARCH-OPTION value=8>8</SEARCH-OPTION> 
<SEARCH-OPTION value=9>9</SEARCH-OPTION> 
<SEARCH-OPTION value=10>10</SEARCH-OPTION> 
<SEARCH-OPTION value=11>11</SEARCH-OPTION> 
<SEARCH-OPTION value=12>12</SEARCH-OPTION> 
<SEARCH-OPTION value=13>13</SEARCH-OPTION> 
<SEARCH-OPTION value=14>14</SEARCH-OPTION> 
<SEARCH-OPTION value=15>15</SEARCH-OPTION> 
<SEARCH-OPTION value=16>16</SEARCH-OPTION> 
<SEARCH-OPTION value=17>17</SEARCH-OPTION> 
<SEARCH-OPTION value=18>18</SEARCH-OPTION> 
<SEARCH-OPTION value=19>19</SEARCH-OPTION> 
<SEARCH-OPTION value=20>20</SEARCH-OPTION> 
<SEARCH-OPTION value=21>21</SEARCH-OPTION> 
<SEARCH-OPTION value=22>22</SEARCH-OPTION> 
<SEARCH-OPTION value=23>23</SEARCH-OPTION> 
<SEARCH-OPTION value=24>24</SEARCH-OPTION> 
<SEARCH-OPTION value=25>25</SEARCH-OPTION> 
<SEARCH-OPTION value=26>26</SEARCH-OPTION> 
<SEARCH-OPTION value=27>27</SEARCH-OPTION> 
<SEARCH-OPTION value=28>28</SEARCH-OPTION> 
<SEARCH-OPTION value=29>29</SEARCH-OPTION> 
<SEARCH-OPTION value=30>30</SEARCH-OPTION> 
<SEARCH-OPTION value=31>31</SEARCH-OPTION> 
</SEARCH-SELECT><!--comma-->, 
<SEARCH-INPUT size=4 name="sp_start_year"> 
</td></tr> 
<tr><td></td> 
<td align=right>To:</td><td> 
<SEARCH-SELECT name="sp_end_month" size=1> 
<SEARCH-OPTION value=0></SEARCH-OPTION> 
<SEARCH-OPTION value=1>January</SEARCH-OPTION> 
<SEARCH-OPTION value=2>February</SEARCH-OPTION> 
<SEARCH-OPTION value=3>March</SEARCH-OPTION> 
<SEARCH-OPTION value=4>April</SEARCH-OPTION> 
<SEARCH-OPTION value=5>May</SEARCH-OPTION> 
<SEARCH-OPTION value=6>June</SEARCH-OPTION> 
<SEARCH-OPTION value=7>July</SEARCH-OPTION> 
<SEARCH-OPTION value=8>August</SEARCH-OPTION> 
<SEARCH-OPTION value=9>September</SEARCH-OPTION> 
<SEARCH-OPTION value=10>October</SEARCH-OPTION> 
<SEARCH-OPTION value=11>November</SEARCH-OPTION> 
<SEARCH-OPTION value=12>December</SEARCH-OPTION> 
</SEARCH-SELECT> 
<SEARCH-SELECT name="sp_end_day" size=1> 
<SEARCH-OPTION value=0></SEARCH-OPTION> 
<SEARCH-OPTION value=1>1</SEARCH-OPTION> 
<SEARCH-OPTION value=2>2</SEARCH-OPTION> 
<SEARCH-OPTION value=3>3</SEARCH-OPTION> 
<SEARCH-OPTION value=4>4</SEARCH-OPTION> 
<SEARCH-OPTION value=5>5</SEARCH-OPTION> 
<SEARCH-OPTION value=6>6</SEARCH-OPTION> 
<SEARCH-OPTION value=7>7</SEARCH-OPTION> 
<SEARCH-OPTION value=8>8</SEARCH-OPTION> 
<SEARCH-OPTION value=9>9</SEARCH-OPTION> 
<SEARCH-OPTION value=10>10</SEARCH-OPTION> 
<SEARCH-OPTION value=11>11</SEARCH-OPTION> 
<SEARCH-OPTION value=12>12</SEARCH-OPTION> 
<SEARCH-OPTION value=13>13</SEARCH-OPTION> 
<SEARCH-OPTION value=14>14</SEARCH-OPTION> 
<SEARCH-OPTION value=15>15</SEARCH-OPTION> 
<SEARCH-OPTION value=16>16</SEARCH-OPTION> 
<SEARCH-OPTION value=17>17</SEARCH-OPTION> 
<SEARCH-OPTION value=18>18</SEARCH-OPTION> 
<SEARCH-OPTION value=19>19</SEARCH-OPTION> 
<SEARCH-OPTION value=20>20</SEARCH-OPTION> 
<SEARCH-OPTION value=21>21</SEARCH-OPTION> 
<SEARCH-OPTION value=22>22</SEARCH-OPTION> 
<SEARCH-OPTION value=23>23</SEARCH-OPTION> 
<SEARCH-OPTION value=24>24</SEARCH-OPTION> 
<SEARCH-OPTION value=25>25</SEARCH-OPTION> 
<SEARCH-OPTION value=26>26</SEARCH-OPTION> 
<SEARCH-OPTION value=27>27</SEARCH-OPTION> 
<SEARCH-OPTION value=28>28</SEARCH-OPTION> 
<SEARCH-OPTION value=29>29</SEARCH-OPTION> 
<SEARCH-OPTION value=30>30</SEARCH-OPTION> 
<SEARCH-OPTION value=31>31</SEARCH-OPTION> 
</SEARCH-SELECT><!--comma-->, 
<SEARCH-INPUT size=4 name="sp_end_year"> 
</td></tr> 
<!-- List box selects the search field --> 
<tr><td valign=top> 
<b>Within: </b> 
</td><td colspan=4><SEARCH-SELECT name="sp_x" size=1> 
<SEARCH-OPTION value="any">Anywhere</SEARCH-OPTION> 
<SEARCH-OPTION value="title">Title</SEARCH-OPTION> 
<SEARCH-OPTION value="desc">Description</SEARCH-OPTION> 
<SEARCH-OPTION value="keys">Keywords</SEARCH-OPTION> 
<SEARCH-OPTION value="body">Body</SEARCH-OPTION> 
<SEARCH-OPTION value="alt">Alternate text</SEARCH-OPTION> 
<SEARCH-OPTION value="url">URL</SEARCH-OPTION> 
<SEARCH-OPTION value="target">Target</SEARCH-OPTION> 
</SEARCH-SELECT></td></tr> 
<!-- List box selects number of results to show per page --> 
<tr><td valign=top> 
<b>Show:</b> 
</td><td colspan=4><SEARCH-SELECT name="sp_c" size=1> 
<SEARCH-OPTION value=5>5</SEARCH-OPTION> 
<SEARCH-OPTION value=10>10</SEARCH-OPTION> 
<SEARCH-OPTION value=25>25</SEARCH-OPTION> 
<SEARCH-OPTION value=50>50</SEARCH-OPTION> 
<SEARCH-OPTION value=100>100</SEARCH-OPTION> 
</SEARCH-SELECT> results  
<!-- Show or hide summaries in search results --> 
<SEARCH-SELECT name="sp_m" size=1> 
<SEARCH-OPTION value=1>with</SEARCH-OPTION> 
<SEARCH-OPTION value=0>without</SEARCH-OPTION> 
</SEARCH-SELECT> summaries<br></td></tr> 
<!-- Sort results by relevance or by date --> 
<tr><td valign=top> 
<b>Sort by: </b> 
</td><td colspan=4><SEARCH-SELECT name="sp_s" size=1> 
<SEARCH-OPTION value=0>relevance</SEARCH-OPTION> 
<SEARCH-OPTION value=1>date</SEARCH-OPTION> 
</SEARCH-SELECT></td></tr> 
</table> 
</SEARCH-IF-ADVANCED> 
</form>
```

