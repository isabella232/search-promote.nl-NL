---
description: Met het menu Crawling stelt u de datum- en URL-maskers, wachtwoorden, inhoudstypen, verbindingen, formulierdefinities en URL-invoerpunten in.
seo-description: Met het menu Crawling stelt u de datum- en URL-maskers, wachtwoorden, inhoudstypen, verbindingen, formulierdefinities en URL-invoerpunten in.
seo-title: Het menu Crawling
solution: Target
subtopic: Crawling
title: Het menu Crawling
topic: Settings,Site search and merchandising
uuid: a58c03bf-90f7-4b5b-91ff-988b95c246b0
translation-type: tm+mt
source-git-commit: e080a61e24a3809beff7c212ff3d088b2a8ad3b6
workflow-type: tm+mt
source-wordcount: '11115'
ht-degree: 0%

---


# Het menu Crawling{#about-the-crawling-menu}

Met het menu Crawling stelt u de datum- en URL-maskers, wachtwoorden, inhoudstypen, verbindingen, formulierdefinities en URL-invoerpunten in.

## Informatie over URL-invoerpunten {#concept_5D857E3B5C124E85BC0B5AE77A509573}

De meeste websites hebben één primair ingangspunt of homepage dat een klant aanvankelijk bezoekt. Dit belangrijkste ingangspunt is het URL adres waarvan de onderzoeksrobot begint indexkruipen. Als uw website echter meerdere domeinen of subdomeinen heeft, of als delen van uw site niet zijn gekoppeld vanuit het primaire ingangspunt, kunt u URL-ingangen gebruiken om meer ingangspunten toe te voegen.

Alle webpagina&#39;s onder elk opgegeven URL-ingangspunt worden geïndexeerd. U kunt URL-ingangspunten combineren met maskers om precies te bepalen welke delen van een website u wilt indexeren. U moet uw website-index opnieuw samenstellen voordat de effecten van de instellingen voor URL-invoerpunten zichtbaar zijn voor klanten.

Het belangrijkste ingangspunt is doorgaans de URL van de website die u wilt indexeren en doorzoeken. U vormt dit belangrijkste ingangspunt in de Montages van de Rekening.

Zie [Uw accountinstellingen](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)configureren.

Nadat u het hoofdURL ingangspunt hebt gespecificeerd, kunt u naar keuze extra ingangspunten specificeren die u in orde wilt kruipen. Meestal zult u extra ingangspunten voor Web-pagina&#39;s specificeren die niet van pagina&#39;s onder het belangrijkste ingangspunt worden verbonden. Geef extra ingangspunten op wanneer uw website meerdere domeinen omvat, zoals in het volgende voorbeeld:

`https://www.domain.com/`

`https://www.domain.com/not_linked/but_search_me_too/`

`https://more.domain.com/`

U kwalificeert elk ingangspunt met één of meerdere van de volgende spatie-gescheiden sleutelwoorden in de lijst hieronder. Deze trefwoorden beïnvloeden de manier waarop de pagina wordt geïndexeerd.

**Belangrijk**: Zorg ervoor dat u een bepaald trefwoord scheidt van het ingangspunt en van elkaar door een spatie. een komma is geen geldig scheidingsteken.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Trefwoord </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>noindex </p> </td> 
   <td colname="col2"> <p> Als u de tekst niet op de pagina met het ingangspunt wilt indexeren, maar u wel de koppelingen op de pagina wilt volgen, voegt u 
     <userinput>
       noindex 
     </userinput> na het ingangspunt. </p> <p>Scheid het sleutelwoord van het ingangspunt met een ruimte zoals in het volgende voorbeeld: </p> <p> <code> https://www.my-additional-domain.com/more_pages/main.html&amp;nbsp;noindex </code> </p> <p>Dit trefwoord is gelijk aan een meta-tag voor robots met 
     <userinput>
       content="noindex" 
     </userinput>) tussen de 
     <userinput>
       &lt;head&gt; 
     </userinput>... 
     <userinput>
       &lt;/head&gt; 
     </userinput> -tags van de pagina met het ingangspunt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>nofollow </p> </td> 
   <td colname="col2"> <p> Als u de tekst op de pagina met het ingangspunt wilt indexeren, maar u wilt de koppelingen op de pagina niet volgen, voegt u 
     <userinput>
       nofollow 
     </userinput> na het ingangspunt. </p> <p>Scheid het sleutelwoord van het ingangspunt met een ruimte zoals in het volgende voorbeeld: </p> <p> <code> https://www.domain.com/not_linked/directory_listing&amp;nbsp;nofollow </code> </p> <p>Dit trefwoord is gelijk aan een meta-tag voor robots met 
     <userinput>
       content="nofollow" 
     </userinput> tussen de 
     <userinput>
       &lt;head&gt; 
     </userinput>... 
     <userinput>
       &lt;/head&gt; 
     </userinput> -tag van een pagina met invoerpunten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>formulier </p> </td> 
   <td colname="col2"> <p> Wanneer het ingangspunt een login pagina is, 
     <userinput>
       formulier 
     </userinput> wordt doorgaans gebruikt, zodat de zoekrobot het aanmeldingsformulier kan verzenden en de juiste cookies kan ontvangen voordat hij naar de website gaat. Wanneer het trefwoord "form" wordt gebruikt, wordt de pagina met het ingangspunt niet geïndexeerd en markeert de zoekrobot de pagina met het ingangspunt niet als gesleept. Gebruiken 
     <userinput>
       nofollow 
     </userinput> als u niet wilt dat de zoekrobot de koppelingen op de pagina volgt. </p> </td> 
  </tr> 
 </tbody> 
</table>

Zie ook [Informatie over inhoudstypen](../c-about-settings-menu/c-about-crawling-menu.md#concept_6FEA1355C0374500B4C53090C34A8A07).

Zie ook [Informatie over Indexconnector](../c-about-settings-menu/c-about-crawling-menu.md#concept_CA6921E2FBF641F9B4F60C92B32AFA84).

## Meerdere URL-ingangspunten toevoegen die u wilt indexeren {#task_2338A47387D74CFDAC4D4EF4A367ED45}

Als uw website meerdere domeinen of subdomeinen heeft en u wilt dat deze doorlopen, kunt u URL-invoerpunten gebruiken om meer URL&#39;s toe te voegen.

Als u het URL-ingangspunt van de URL van uw website wilt instellen, gebruikt u Accountinstellingen.

Zie [Uw accountinstellingen](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)configureren.

**Meerdere URL-ingangspunten toevoegen die u wilt indexeren**

1. Klik in het menu Product op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**.
1. Voer op de [!DNL URL Entrypoints] pagina in het [!DNL Entrypoints] veld één URL-adres per regel in.
1. (Optioneel) Selecteer in de **[!UICONTROL Add Index Connector Configurations]** vervolgkeuzelijst een indexaansluiting die u wilt toevoegen als ingangspunt voor indexering.

   De vervolgkeuzelijst is alleen beschikbaar als u eerder een of meer indexconnectordefinities hebt toegevoegd.

   ![](assets/url_entrypoints_index_connector.png)

   Zie [Een definitie](../c-about-settings-menu/c-about-crawling-menu.md#task_96779B651A654E1F871F55D6DBBC8886)voor indexaansluiting toevoegen.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om de aangebrachte wijzigingen terug te draaien.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie Live-instellingen [weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)spoelen.

## Informatie over URL-maskers {#concept_8039DFC53FF3410AA494D602F71BA164}

URL-maskers zijn patronen die bepalen welke van uw website documenten de zoekrobot indexeert of niet.

Zorg ervoor dat u uw site-index opnieuw genereert, zodat de resultaten van uw URL-maskers zichtbaar zijn voor uw klanten.

Zie Een incrementele index van een gefaseerde website [](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)configureren.

Hieronder vindt u twee soorten URL-maskers die u kunt gebruiken:

* Inclusief URL-maskers
* URL-maskers uitsluiten

Met URL-maskers worden alle documenten die overeenkomen met het patroon van het masker geïndexeerd door de zoekrobot.

Met URL-maskers uitsluiten wordt de zoekrobot gevraagd overeenkomstige documenten te indexeren.

Terwijl de zoekrobot van de koppeling naar de koppeling via uw website reist, vindt deze URL&#39;s en zoekt hij naar maskers die overeenkomen met die URL&#39;s. De eerste overeenkomst bepaalt of om die URL van de index te omvatten of uit te sluiten. Als er geen masker overeenkomt met een aangetroffen URL, wordt die URL uit de index verwijderd.

Neem URL-maskers op voor uw toegangspunt-URL&#39;s worden automatisch gegenereerd. Dit gedrag zorgt ervoor dat alle aangetroffen documenten op uw website worden geïndexeerd. Het verwijdert ook gemakkelijk koppelingen die uw website &quot;verlaten&quot;. Als een geïndexeerde pagina bijvoorbeeld koppelingen naar https://www.yahoo.com maakt, indexeert de zoekrobot die URL niet omdat deze niet overeenkomt met het include-masker dat automatisch wordt gegenereerd door de URL van het ingangspunt.

Elk URL-masker dat u opgeeft, moet op een aparte regel staan.

Het masker kan het volgende opgeven:

* Een volledig pad zoals in `https://www.mydomain.com/products.html`.
* Een gedeeltelijk pad zoals in `https://www.mydomain.com/products`.
* Een URL die jokertekens gebruikt zoals in `https://www.mydomain.com/*.html`.
* Een reguliere expressie (voor geavanceerde gebruikers).

   Als u een masker wilt omzetten in een reguliere expressie, voegt u het trefwoord in `regexp` tussen het maskertype ( `exclude` of `include`) en het URL-masker.

Hier volgt een eenvoudig voorbeeld van een URL-masker uitsluiten:

```
exclude https://www.mydomain.com/photos
```

Omdat dit voorbeeld een URL-masker uitsluiten is, wordt elk document dat overeenkomt met het patroon niet geïndexeerd. Het patroon komt overeen met elk aangetroffen item, zowel bestanden als mappen, zodat `https://www.mydomain.com/photos.html` en `https://www.mydomain.com/photos/index.html`, die beide overeenkomen met de URL voor uitsluiten, niet worden geïndexeerd. Als u alleen bestanden in de `/photos/` map wilt afstemmen, moet het URL-masker een schuine streep aan het einde bevatten, zoals in het volgende voorbeeld:

```
exclude https://www.mydomain.com/photos/
```

In het volgende voorbeeld voor uitsluitingsmaskers wordt een jokerkaart gebruikt. De zoekrobot krijgt de opdracht om bestanden met de extensie &quot;.pdf&quot; te negeren. De zoekrobot voegt deze bestanden niet toe aan uw index.

```
exclude *.pdf
```

Een eenvoudig include-URL-masker is het volgende:

```
include https://www.mydomain.com/news/
```

Alleen documenten die via een reeks koppelingen van een URL-ingangspunt zijn gekoppeld of die als een URL-ingangspunt zelf worden gebruikt, worden geïndexeerd. Als u alleen de URL van een document aanbiedt als een include-URL-masker, wordt geen ongekoppeld document geïndexeerd. Als u ongekoppelde documenten aan de index wilt toevoegen, gebruikt u de functie URL-invoerpunten.

Zie [Informatie over URL-invoerpunten](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573).

Het opnemen van maskers en het uitsluiten van maskers kan samenwerken. U kunt een groot gedeelte van uw website uitsluiten van indexering door een URL-masker voor uitsluiten te maken en toch een of meer van deze uitgesloten pagina&#39;s met een include-URL-masker op te nemen. Stel dat de URL van het ingangspunt als volgt is:

```
https://www.mydomain.com/photos/
```

De zoekrobot crawt en indexeert alle pagina&#39;s onder `/photos/summer/`, `/photos/spring/` en `/photos/fall/` (ervan uitgaande dat er koppelingen zijn naar ten minste één pagina in elke map van de `photos` map). Dit gedrag treedt op omdat de koppelingspaden de zoekrobot in staat stellen de documenten in de mappen `/summer/`, `/spring/`en `/fall/`, en de map-URL&#39;s te zoeken, overeenkomen met het include-masker dat automatisch wordt gegenereerd door de URL van het ingangspunt.

U kunt desgewenst alle pagina&#39;s in de `/fall/` map uitsluiten met een URL-masker, zoals in het volgende voorbeeld:

```
exclude https://www.mydomain.com/photos/fall/
```

U kunt ook alleen selectief opnemen `/photos/fall/redleaves4.html` als onderdeel van de index met het volgende URL-masker:

```
include https://www.mydomain.com/photos/fall/redleaves4.html
```

Voor de bovengenoemde twee maskervoorbeelden om te werken zoals bedoeld, is omvat masker eerst vermeld, zoals in het volgende:

```
include https://www.mydomain.com/photos/fall/redleaves4.html 
exclude https://www.mydomain.com/photos/fall/
```

Omdat de zoekrobot aanwijzingen volgt in de volgorde waarin ze worden weergegeven, bevat de zoekrobot eerst `/photos/fall/redleaves4.html`en worden de overige bestanden in de `/fall` map uitgesloten.

Indien de instructies op de tegenovergestelde wijze als in het volgende worden gespecificeerd:

```
exclude https://www.mydomain.com/photos/fall/ 
include https://www.mydomain.com/photos/fall/redleaves4.html
```

Dan `/photos/fall/redleaves4.html` is niet inbegrepen, alhoewel het masker specificeert dat het inbegrepen is.

Een URL-masker dat als eerste wordt weergegeven, heeft altijd voorrang op een URL-masker dat later in de maskerinstellingen wordt weergegeven. Als de zoekrobot bovendien een pagina tegenkomt die overeenkomt met een include-URL-masker en een exclude-URL-masker, heeft het masker dat als eerste wordt vermeld altijd voorrang.

Zie Een incrementele index van een gefaseerde website [](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)configureren.

## Trefwoorden gebruiken met URL-maskers {#section_7609A7A6D79B482ABCA8900886541AAB}

U kunt elk include-masker kwalificeren met een of meer gereserveerde woorden met spaties die bepalen hoe de overeenkomende pagina&#39;s worden geïndexeerd.

Een komma is niet geldig als scheidingsteken tussen het masker en het trefwoord. u kunt alleen spaties gebruiken.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Trefwoord </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>noindex </p> </td> 
   <td colname="col2"> <p> Als u de tekst niet wilt indexeren op de pagina's die overeenkomen met het URL-masker, maar u wel de koppelingen voor de overeenkomende pagina's wilt volgen, voegt u 
     <userinput>
       noindex 
     </userinput> na het include-URL-masker. Zorg ervoor dat u het trefwoord scheidt van het masker met een spatie, zoals in het volgende voorbeeld: </p> <p> <code> include&amp;nbsp;*.swf&amp;nbsp;noindex </code> </p> <p>In het bovenstaande voorbeeld wordt opgegeven dat de zoekrobot alle koppelingen volgt vanuit bestanden met de 
     <userinput>
       .swf 
     </userinput> , maar schakelt het indexeren van alle tekst in die bestanden uit. </p> <p>De 
     <userinput>
       noindex 
     </userinput> trefwoord is gelijk aan een meta-tag voor robot met 
     <userinput>
       content="noindex" 
     </userinput> tussen de 
     <userinput>
       &lt;head&gt;..&lt;/head&gt; 
     </userinput> codes van overeenkomende pagina's. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>nofollow </p> </td> 
   <td colname="col2"> <p> Als u de tekst wilt indexeren op de pagina's die overeenkomen met het URL-masker, maar u de koppelingen op de overeenkomende pagina niet wilt volgen, voegt u 
     <userinput>
       nofollow 
     </userinput> na het include-URL-masker. Zorg ervoor dat u het trefwoord scheidt van het masker met een spatie, zoals in het volgende voorbeeld: </p> <p> <code> include&amp;nbsp;https://www.mydomain.com/photos&amp;nbsp;nofollow </code> </p> <p>De 
     <userinput>
       nofollow 
     </userinput> trefwoord is gelijk aan een meta-tag voor robot met 
     <userinput>
       content="nofollow" 
     </userinput> tussen de 
     <userinput>
       &lt;head&gt;..&lt;/head&gt; 
     </userinput> codes van overeenkomende pagina's. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>regexp </p> </td> 
   <td colname="col2"> <p>Wordt gebruikt voor zowel include- als exclude-maskers. </p> <p>Willekeurig URL-masker voorafgegaan door 
     <userinput>
       regexp 
     </userinput> wordt behandeld als een reguliere expressie. Als de zoekrobot documenten aantreft die overeenkomen met een expressie-URL-masker zonder reguliere expressie, worden deze documenten niet geïndexeerd. Als de zoekrobot documenten aantreft die overeenkomen met een regulier expressie-URL-masker, worden deze documenten geïndexeerd. Stel dat u het volgende URL-masker hebt: </p> <p> <code> exclude&amp;nbsp;regexp&amp;nbsp;^.*/products/.*\.html$ </code> </p> <p>De zoekrobot sluit overeenkomende bestanden uit, zoals 
     <userinput>
       https://www.mydomain.com/products/page1.html 
     </userinput> </p> <p>Als u het volgende masker voor reguliere expressie-URL had: </p> <p> <code> exclude&amp;nbsp;regexp&amp;nbsp;^.*\?..*$ </code> </p> <p>De zoekrobot bevat geen URL die een CGI-parameter bevat, zoals 
     <userinput>
       https://www.mydomain.com/cgi/prog/?arg1=val1&amp;arg2=val2 
     </userinput>. </p> <p>Als het volgende URL-masker voor reguliere expressie moet worden opgenomen: </p> <p> <code> include&amp;nbsp;regexp&amp;nbsp;^.*\.swf$&amp;nbsp;noindex </code> </p> <p>De zoekrobot volgt alle koppelingen van bestanden met de extensie ".swf". De 
     <userinput>
       noindex 
     </userinput> trefwoord geeft ook aan dat de tekst van overeenkomende bestanden niet wordt geïndexeerd. </p> <p>Zie <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Reguliere expressies </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## URL-maskers toevoegen om delen van uw website te indexeren of niet {#task_E1AFC17C746048B8843013D979E082C1}

U kunt gebruiken [!DNL URL Masks] om te bepalen welke delen van uw website u wilt of niet wilt kruipen en indexeren.

Met het veld URL-maskers testen kunt u testen of een document al dan niet wordt opgenomen na de index.

Zorg ervoor dat u uw site-index opnieuw genereert, zodat de resultaten van uw URL-maskers zichtbaar zijn voor uw klanten.

Zie Een incrementele index van een gefaseerde website [](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)configureren.

**URL-maskers toevoegen om delen van uw website te indexeren of niet**

1. Klik in het menu Product op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Masks]**.
1. (Optioneel) Voer in het [!DNL URL Masks] veld op de **[!UICONTROL Test URL Masks]** pagina een test-URL-masker van uw website in en klik op **[!UICONTROL Test]**.
1. Typ in het [!DNL URL Masks] veld `include` (om een website toe te voegen die u wilt knipperen en indexeren) of typ `exclude` (om te voorkomen dat een website wordt gekropen en geïndexeerd), gevolgd door het adres van het URL-masker.

   Voer één URL-maskeradres per regel in. Voorbeeld:

   ```
   include https://www.mycompany.com/summer 
   include https://www.mycompany.com/spring 
   exclude regexp .*\.xml 
   exclude https://www.mycompany.com/fall
   ```

1. Klik op **[!UICONTROL Save Changes]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om de aangebrachte wijzigingen terug te draaien.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie Live-instellingen [weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)spoelen.

## Datummaskers {#concept_F4F1F58A646F4A86B8650EC46FDCEF66}

U kunt Datummaskers gebruiken om bestanden op te nemen in of uit te sluiten van uw zoekresultaten op basis van de leeftijd van het bestand.

Zorg ervoor dat u uw site-index opnieuw genereert, zodat de resultaten van uw URL-maskers zichtbaar zijn voor uw klanten.

Zie Een incrementele index van een gefaseerde website [](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)configureren.

Hieronder ziet u twee soorten datummaskers die u kunt gebruiken:

* Datummaskers opnemen (&quot;include-days&quot; en &quot;include-date&quot;)

   Indexbestanden met datummaskers opnemen die op of voor de opgegeven datum worden gedateerd.
* Datummaskers uitsluiten (&quot;exclude-days&quot; en &quot;exclude-date&quot;)

   Met datummaskers kunt u indexbestanden uitsluiten die dateren van of voor de opgegeven datum.

Standaard wordt de bestandsdatum bepaald door de metatag. Als er geen Meta-tag wordt gevonden, wordt de datum van een bestand bepaald door de HTTP-header die van de server wordt ontvangen wanneer de zoekrobot een bestand downloadt.

Elk datummasker dat u opgeeft, moet op een aparte regel staan.

Het masker kan het volgende opgeven:

* Een volledig pad als in `https://www.mydomain.com/products.html`
* Een gedeeltelijk pad zoals in `https://www.mydomain.com/products`
* Een URL die jokertekens gebruikt `https://www.mydomain.com/*.html`
* Een reguliere expressie. Als u van een masker een reguliere expressie wilt maken, voegt u het trefwoord in `regexp` vóór de URL.

Met beide opties kunt u datummaskers voor opnemen en uitsluiten een datum op een van de volgende twee manieren opgeven. De maskers worden alleen toegepast als de overeenkomende bestanden zijn gemaakt op of vóór de opgegeven datum:

1. Een aantal dagen. Stel dat uw datummasker bijvoorbeeld als volgt is:

   ```
   exclude-days 30 https://www.mydomain.com/docs/archive/)
   ```

   Het aantal opgegeven dagen wordt teruggeteld. Als het bestand op of voor de aangezochte datum gedateerd is, wordt het masker toegepast.

1. Een werkelijke datum met de notatie YYYY-MM-DD. Stel dat uw datummasker bijvoorbeeld als volgt is:

   ```
   include-date 2011-02-15 https://www.mydomain.com/docs/archive/)
   ```

   Als het overeenkomende document dateert van of voor de opgegeven datum, wordt het datummasker toegepast.

Hier volgt een eenvoudig voorbeeld van een datummasker voor uitsluiten:

```
exclude-days 90 https://www.mydomain.com/docs/archive
```

Omdat dit een datummasker voor uitsluiten is, wordt elk bestand dat overeenkomt met het patroon niet geïndexeerd en is het 90 dagen oud of ouder. Wanneer u een document uitsluit, wordt er geen tekst geïndexeerd en worden er geen koppelingen van dat bestand gevolgd. Het bestand wordt genegeerd. In dit voorbeeld kunnen zowel bestanden als mappen overeenkomen met het opgegeven URL-patroon. Merk op dat zowel `https://www.mydomain.com/docs/archive.html` als `https://www.mydomain.com/docs/archive/index.html` het patroon en niet geïndexeerd zijn als zij 90 dagen oud of ouder zijn. Als u alleen bestanden in de `/docs/archive/` map wilt afstemmen, moet het datummasker een schuine streep aan het einde van de map bevatten, zoals in het volgende voorbeeld:

```
exclude-days 90 https://www.mydomain.com/docs/archive/
```

Datummaskers kunnen ook worden gebruikt met jokerkaarten. Met het volgende exclude-masker wordt aan de zoekrobot doorgegeven dat bestanden met de extensie &quot;.pdf&quot; die op of voor 2011-02-15 zijn gedateerd, moeten worden genegeerd. De zoekrobot voegt geen overeenkomende bestanden toe aan uw index.

```
exclude-date 2011-02-15 *.pdf
```

Datummasker opnemen ziet er ongeveer hetzelfde uit. Alleen overeenkomende bestanden worden toegevoegd aan de index. In het volgende voorbeeld met een datummasker wordt de zoekrobot gevraagd de tekst te indexeren uit bestanden die nul dagen oud of ouder zijn in het `/docs/archive/manual/` gebied van de website.

```
include-days 0 https://www.mydomain.com/docs/archive/manual/
```

Het opnemen van maskers en het uitsluiten van maskers kan samenwerken. U kunt bijvoorbeeld een groot deel van uw website uitsluiten van indexering door een datummasker voor uitsluiten te maken en toch een of meer van deze uitgesloten pagina&#39;s met een include-URL-masker op te nemen. Als uw ingangspunt URL het volgende is:

```
https://www.mydomain.com/archive/
```

De zoekrobot crawt en indexeert alle pagina&#39;s onder `/archive/summer/`, `/archive/spring/`en `/archive/fall/` (ervan uitgaande dat er koppelingen zijn naar ten minste één pagina in elke map van de `archive` map). Dit gedrag treedt op omdat de koppelingspaden de zoekrobot in staat stellen de bestanden in de mappen `/summer/`, `/spring/`en `/fall/` mappen te zoeken en de map-URL&#39;s overeenkomen met het include-masker dat automatisch wordt gegenereerd door de entrypunt-URL.

Zie [Informatie over URL-invoerpunten](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573).

Zie [Uw accountinstellingen](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)configureren.

U kunt desgewenst alle pagina&#39;s ouder dan 90 dagen in de `/fall/` map met een datummasker voor uitsluiten uitsluiten, zoals in het volgende voorbeeld:

```
exclude-days 90 https://www.mydomain.com/archive/fall/
```

U kunt alleen selectief `/archive/fall/index.html` (ongeacht hoe oud het is - elk bestand van 0 dagen of ouder wordt aangepast) opnemen als onderdeel van de index met het volgende datummasker:

```
include-days 0 https://www.mydomain.com/archive/fall/index.html
```

Als u de twee bovenstaande maskervoorbeelden wilt laten werken zoals bedoeld, moet u eerst het include-masker vermelden, zoals in het volgende voorbeeld:

```
include-days 0 https://www.mydomain.com/archive/fall/index.html 
exclude-days 90 https://www.mydomain.com/archive/fall/
```

Omdat de zoekrobot aanwijzingen volgt in de volgorde waarin deze is opgegeven, bevat de zoekrobot eerst `/archive/fall/index.html`en worden de overige bestanden in de `/fall` map uitgesloten.

Indien de instructies op de tegenovergestelde wijze als in het volgende worden gespecificeerd:

```
exclude-days 90 https://www.mydomain.com/archive/fall/ 
include-days 0 https://www.mydomain.com/archive/fall/index.html 
```

Dan `/archive/fall/index.html` is niet inbegrepen, alhoewel het masker specificeert dat het zou moeten zijn. Een datummasker dat als eerste verschijnt, heeft altijd voorrang op een datummasker dat later in de maskerinstellingen wordt weergegeven. Als de zoekrobot bovendien een pagina tegenkomt die overeenkomt met zowel een include-datummasker als een uitvullingsdatummasker, heeft het masker dat als eerste wordt vermeld altijd voorrang.

Zie Een incrementele index van een gefaseerde website [](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)configureren.

## Trefwoorden gebruiken met datummaskers {#section_CCBB3E3FDBDE4725B2B571FD6594470C}

U kunt elk include-masker kwalificeren met een of meer gereserveerde woorden met spaties die bepalen hoe de overeenkomende pagina&#39;s worden geïndexeerd.

Een komma is niet geldig als scheidingsteken tussen het masker en het trefwoord. u kunt alleen spaties gebruiken.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Trefwoord </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>noindex </p> </td> 
   <td colname="col2"> <p> Als u de tekst niet wilt indexeren op de pagina's die gedateerd zijn op of vóór de datum die is opgegeven door het include-masker, voegt u 
     <userinput>
       noindex 
     </userinput> na het include-datummasker, zoals in het volgende voorbeeld: </p> <p> <code> include-days&amp;nbsp;10&amp;nbsp;*.swf&amp;nbsp;noindex </code> </p> <p>Zorg ervoor dat u het trefwoord met een spatie scheidt van het masker. </p> <p>In het bovenstaande voorbeeld wordt opgegeven dat de zoekrobot alle koppelingen volgt van bestanden met de extensie ".swf" die 10 dagen oud of ouder zijn. Het indexeren van alle tekst in die bestanden wordt echter uitgeschakeld. </p> <p>Mogelijk wilt u dat de tekst voor oudere bestanden niet wordt geïndexeerd, maar wel alle koppelingen uit die bestanden volgt. In dergelijke gevallen gebruikt u een include-datummasker met het trefwoord "noindex" in plaats van een exclude-datummasker. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>nofollow </p> </td> 
   <td colname="col2"> <p> Als u de tekst wilt indexeren op de pagina's die gedateerd zijn op of vóór de datum die is opgegeven door het include-masker, maar u wilt de koppelingen van de overeenkomende pagina niet volgen, voegt u 
     <userinput>
       nofollow 
     </userinput> na het include-datummasker, zoals in het volgende voorbeeld: </p> <p> <code> include-days&amp;nbsp;8&amp;nbsp;https://www.mydomain.com/photos&amp;nbsp;nofollow </code> </p> <p>Zorg ervoor dat u het trefwoord met een spatie scheidt van het masker. </p> <p>De 
     <userinput>
       nofollow 
     </userinput> trefwoord is gelijk aan een meta-tag voor robot met 
     <userinput>
       content="nofollow" 
     </userinput> tussen de 
     <userinput>
       &lt;head&gt;..&lt;/head&gt; 
     </userinput> tag van overeenkomende pagina's. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>serverdatum </p> </td> 
   <td colname="col2"> <p>Wordt gebruikt voor zowel include- als exclude-maskers. </p> <p>De zoekrobot downloadt en parseert doorgaans elk bestand voordat de datummaskers worden gecontroleerd. Dit gedrag treedt op omdat sommige bestandstypen een datum in het bestand zelf kunnen opgeven. Een HTML-document kan bijvoorbeeld metatags bevatten waarmee de datum van het bestand wordt ingesteld. </p> <p>Als u veel bestanden wilt uitsluiten op basis van de datum waarop ze zijn gemaakt, en u wilt geen onnodige belasting op de servers plaatsen, kunt u 
     <userinput>
       serverdatum 
     </userinput> na de URL in het datummasker. </p> <p>Dit sleutelwoord draagt de onderzoekersrobot op om de datum van het dossier te vertrouwen dat door uw server in plaats van het ontleden van elk dossier is teruggekeerd. In het volgende datummasker voor uitsluiten worden bijvoorbeeld pagina's genegeerd die overeenkomen met de URL als de documenten 90 dagen of ouder zijn, afhankelijk van de datum die door de server wordt geretourneerd in de HTTP-headers: </p> <p> <code> exclude-days&amp;nbsp;90&amp;nbsp;https://www.mydomain.com/docs/archive&amp;nbsp;server-date </code> </p> <p> Als de datum die door de server wordt geretourneerd 90 dagen of langer is, 
     <userinput>
       serverdatum 
     </userinput> Hiermee geeft u op dat de uitgesloten documenten niet van uw server mogen worden gedownload. Het resultaat is een snellere indexering van uw documenten en een lagere belasting op uw servers. Indien 
     <userinput>
       serverdatum 
     </userinput> niet wordt opgegeven, negeert de zoekrobot de datum die door de server in de HTTP-headers wordt geretourneerd. In plaats daarvan wordt elk bestand gedownload en gecontroleerd om te zien of de datum is opgegeven. Als er geen datum in het bestand is opgegeven, gebruikt de zoekrobot de datum die door de server wordt geretourneerd. </p> <p>U mag het niet gebruiken 
     <userinput>
       serverdatum 
     </userinput> als uw bestanden opdrachten bevatten die de serverdatum overschrijven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>regexp </p> </td> 
   <td colname="col2"> <p> Wordt gebruikt voor zowel include- als exclude-maskers. </p> <p>Datummasker dat wordt voorafgegaan door 
     <userinput>
       regexp 
     </userinput> wordt behandeld als een reguliere expressie. </p> <p>Als de zoekrobot bestanden aantreft die overeenkomen met een reguliere-expressiedatummasker, worden deze bestanden niet geïndexeerd. </p> <p>Als de zoekrobot bestanden aantreft die overeenkomen met een regulier expressiedatummasker, worden deze documenten geïndexeerd. </p> <p>Stel dat u het volgende datummasker hebt: </p> <p> <code> exclude-days&amp;nbsp;180&amp;nbsp;regexp&amp;nbsp;.*archive.* </code> </p> <p>Het masker vertelt de zoekrobot om overeenkomende bestanden van 180 dagen of ouder uit te sluiten. Dat wil zeggen, bestanden die het woord "archief" in hun URL bevatten. </p> <p>Zie <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Reguliere expressies </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Datummaskers toevoegen om delen van uw website te indexeren of niet {#task_0010543C55F648D2B5DEFEFAD60FAF04}

U kunt Datummaskers gebruiken om bestanden op te nemen in of uit te sluiten van zoekresultaten van klanten op basis van de leeftijd van de bestanden.

Met de velden **[!UICONTROL Test Date]** en **[!UICONTROL Test URL]** velden kunt u testen of een bestand al dan niet wordt opgenomen na de index.

Zorg ervoor dat u uw site-index opnieuw genereert, zodat de resultaten van uw URL-maskers zichtbaar zijn voor uw klanten.

Zie Een incrementele index van een gefaseerde website [](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)configureren.

**Datummaskers toevoegen om delen van uw website te indexeren of niet**

1. Klik in het menu Product op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Date Masks]**.
1. (Optioneel) Voer in het [!DNL Date Masks] veld op de **[!UICONTROL Test Date]** pagina een datum in die is opgemaakt als JJJJ-MM-DD (bijvoorbeeld `2011-07-25`); Voer in het **[!UICONTROL Test URL]** veld een URL-masker van uw website in en klik op **[!UICONTROL Test]**.
1. Voer in het [!DNL Date Masks] veld één datummaskeradres per regel in.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om de aangebrachte wijzigingen terug te draaien.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie Live-instellingen [weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)spoelen.

## Over wachtwoorden {#concept_3EDBD731725D46B891F834D4472774DC}

Als u toegang wilt tot gedeelten van uw website die zijn beveiligd met HTTP Basic-verificatie, kunt u een of meer wachtwoorden toevoegen.

Voordat de effecten van de instellingen voor wachtwoorden zichtbaar zijn voor klanten, moet u de index van uw site opnieuw genereren.

Zie Een incrementele index van een gefaseerde website [](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)configureren.

Op de [!DNL Passwords] pagina typt u elk wachtwoord op één regel. Het wachtwoord bestaat uit een URL of domein, een gebruikersnaam en een wachtwoord, zoals in het volgende voorbeeld:

```
https://www.mydomain.com/ myname mypassword
```

In plaats van een URL-pad te gebruiken, zoals hierboven, kunt u ook een domein opgeven.

Als u wilt bepalen welk gebied u wilt gebruiken, opent u een webpagina die met een wachtwoord is beveiligd met een browser en bekijkt u het dialoogvenster Netwerkwachtwoord invoeren.

![](assets/realms.gif)

De naam van het domein is in dit geval &quot;Mijn site-domein&quot;.

Met de bovenstaande domeinnaam ziet uw wachtwoord er als volgt uit:

```
My Site Realm myusername mypassword
```

Als uw website meerdere domeinen heeft, kunt u meerdere wachtwoorden maken door een gebruikersnaam en wachtwoord voor elk domein op een aparte regel in te voeren, zoals in het volgende voorbeeld:

```
Realm1 name1 password1 
Realm2 name2 password2 
Realm3 name3 password3
```

U kunt wachtwoorden die URL&#39;s of gebieden bevatten onderling mixen zodat uw wachtwoordlijst er als volgt zou kunnen uitzien:

```
Realm1 name1 password1 
https://www.mysite.com/path1/path2 name2 password2 
Realm3 name3 password3 
Realm4 name4 password4 
https://www.mysite.com/path1/path5 name5 password5 
https://www.mysite.com/path6 name6 password6
```

In de bovenstaande lijst wordt het eerste wachtwoord gebruikt dat een domein of URL bevat die overeenkomt met de verificatieaanvraag van de server. Zelfs als het bestand in `https://www.mysite.com/path1/path2/index.html` zich bevindt `Realm3`, bijvoorbeeld `name2` en `password2` wordt gebruikt omdat het wachtwoord dat met de URL is gedefinieerd, boven het wachtwoord staat dat met het domein is gedefinieerd.

## Wachtwoorden toevoegen voor toegang tot gebieden van uw website die verificatie vereisen {#task_DED19D476FF04B48BB6456D5ECB8628A}

U kunt Wachtwoorden gebruiken om met een wachtwoord beveiligde gebieden van uw website te openen en te indexeren.

Voordat de effecten van uw wachtwoord zichtbaar zijn voor klanten, moet u de index van uw site opnieuw samenstellen

Zie Een incrementele index van een gefaseerde website [](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)configureren.

**Wachtwoorden toevoegen voor toegang tot gebieden van uw website die verificatie vereisen**

1. Klik in het menu Product op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Passwords]**.
1. Voer op de [!DNL Passwords] pagina in het **[!UICONTROL Passwords]** veld een domein of URL in, evenals de bijbehorende gebruikersnaam en het bijbehorende wachtwoord, gescheiden door een spatie.

   Voorbeeld van een realm-wachtwoord en een URL-wachtwoord op aparte regels:

   ```
   Realm1 name1 password1 
   https://www.mysite.com/path1/path2 name2 password2
   ```

   Voeg slechts één wachtwoord per regel toe.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om de aangebrachte wijzigingen terug te draaien.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie Live-instellingen [weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)spoelen.

## Over inhoudstypen {#concept_6FEA1355C0374500B4C53090C34A8A07}

U kunt gebruiken [!DNL Content Types] om te selecteren welke bestandstypen u wilt kruipen en indexeren voor dit account.

De inhoudstypes die u kunt verkiezen om te kruipen en te indexeren omvatten documenten PDF, tekstdocumenten, de films van de Flits van Adobe, dossiers van de toepassingen van Microsoft Office zoals Word, Excel, en Powerpoint, en tekst in MP3 dossiers. De tekst die binnen de geselecteerde inhoudstypen wordt gevonden, wordt samen met alle andere tekst op uw website doorzocht.

Voordat de effecten van de instellingen voor inhoudstypen zichtbaar zijn voor klanten, moet u de index van uw site opnieuw genereren.

Zie Een incrementele index van een gefaseerde website [](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)configureren.

## MP3-muziekbestanden indexeren {#section_AD2E28BEEE3E46629E2B05C34A963673}

Als u de optie **[!UICONTROL Text in MP3 Music Files]** op de [!DNL Content Types] pagina selecteert, wordt een MP3-bestand gekropen en op twee manieren geïndexeerd. De eerste en meest gebruikelijke manier is van een href-ankertag in een HTML-bestand, zoals hieronder:

```
<a href="MP3-file-URL"></a>
```

De tweede manier is om de URL van het MP3-bestand in te voeren als een URL-ingangspunt.

Zie [Informatie over URL-invoerpunten](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573).

Een MP3-bestand wordt herkend door het MIME-type &quot;audio/mpeg&quot;.

Houd er rekening mee dat de grootte van MP3-muziekbestanden tamelijk groot kan zijn, ook al bevatten deze meestal slechts een kleine hoeveelheid tekst. In MP3-bestanden kunnen bijvoorbeeld optioneel bijvoorbeeld de albumnaam, de artiest, de titel van het nummer, het genre van het nummer, het jaar van de release en een opmerking worden opgeslagen. Deze informatie wordt opgeslagen helemaal aan het eind van het dossier in wat wordt genoemd TAG. MP3-bestanden met TAG-informatie worden als volgt geïndexeerd:

* De titel van het nummer wordt behandeld als de titel van een HTML-pagina.
* De opmerking wordt behandeld als een beschrijving die is gedefinieerd voor een HTML-pagina.
* Het genre wordt behandeld als een sleutelwoord dat voor een HTML- pagina wordt bepaald.
* De naam van de artiest, de albumnaam en het jaar van uitgave worden beschouwd als de hoofdtekst van een HTML-pagina.

Elk MP3-bestand dat op uw website is gekropen en geïndexeerd, telt als één pagina.

Als uw website veel grote MP3-bestanden bevat, overschrijdt u mogelijk de limiet voor indexbytes voor uw account. Als dit gebeurt, kunt u de selectie **[!UICONTROL Text in MP3 Music Files]** op de [!DNL Content Types] pagina opheffen om te voorkomen dat alle MP3-bestanden op uw website worden geïndexeerd.

Als u alleen wilt voorkomen dat bepaalde MP3-bestanden op uw website worden geïndexeerd, kunt u een van de volgende handelingen uitvoeren:

* Omring de ankerlabels die aan de MP3-bestanden zijn gekoppeld met `<nofollow>` en `</nofollow>` -tags. De zoekrobot volgt de koppelingen tussen deze tags niet.

* Voeg de URL&#39;s van de MP3-bestanden toe als uitsluitingsmaskers.

   Zie [Informatie over URL-maskers](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164).

## Inhoudstypen selecteren om door te bladeren en te indexeren {#task_CCAC5C67C8BF4AB7B79D34A1495D5EE8}

U kunt gebruiken [!DNL Content Types] om te selecteren welke bestandstypen u wilt kruipen en indexeren voor dit account.

De inhoudstypes die u kunt verkiezen om te kruipen en te indexeren omvatten documenten PDF, tekstdocumenten, de films van de Flits van Adobe, dossiers van de toepassingen van Microsoft Office zoals Word, Excel, en Powerpoint, en tekst in MP3 dossiers. De tekst die binnen de geselecteerde inhoudstypen wordt gevonden, wordt samen met alle andere tekst op uw website doorzocht.

Voordat de effecten van de instellingen voor inhoudstypen zichtbaar zijn voor klanten, moet u de index van uw site opnieuw genereren.

Zie Een incrementele index van een gefaseerde website [](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)configureren.

Voer de onderstaande stappen uit om te doorlopen en Chinese, Japanse of Koreaanse MP3-bestanden te indexeren. Geef vervolgens bij **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Injections]** de tekenset op die wordt gebruikt om de MP3-bestanden te coderen.

Zie [Informatie over injecties](../c-about-settings-menu/c-about-metadata-menu.md#concept_DA091920671948A0A893A26B3A2FAAE5).

**Om inhoudstypes te selecteren om te kruipen en te indexeren**

1. Klik in het menu Product op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**.
1. Controleer op de [!DNL Content Types] pagina de bestandstypen die u wilt verkennen en indexeren op uw website.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om de aangebrachte wijzigingen terug te draaien.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie Live-instellingen [weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)spoelen.

## Informatie over verbindingen {#concept_E2F3B7E7521147479E5948A94BB3A40B}

Met Verbindingen kunt u maximaal tien HTTP-verbindingen toevoegen die de zoekrobot gebruikt om uw website te indexeren.

Verhoog het aantal verbindingen om de hoeveelheid tijd beduidend te verminderen die het neemt om te voltooien kruipt en index. Houd er echter rekening mee dat elke aanvullende verbinding de belasting op de server verhoogt.

## Verbindingen toevoegen om de indexsnelheid te verhogen {#task_3E9B83E43C1842A19066355A15C4A6FB}

U kunt de hoeveelheid tijd verminderen het duurt om uw website te indexeren door Verbindingen te gebruiken om het aantal gelijktijdige verbindingen van HTTP te verhogen die de kruipper gebruikt. U kunt maximaal tien verbindingen toevoegen.

Houd er rekening mee dat elke extra verbinding de belasting verhoogt die op de server wordt geplaatst.

**Verbindingen toevoegen om de indexsnelheid te verhogen**

1. Klik in het menu Product op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Connections]**.
1. Voer op de [!DNL Parallel Indexing Connections] pagina in het **[!UICONTROL Number of Connections]** veld het aantal verbindingen (1-10) in dat u wilt toevoegen.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om de aangebrachte wijzigingen terug te draaien.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie Live-instellingen [weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)spoelen.

## Formulierverzending {#concept_CADD5D7CF373497DAA6F8564D7BC8502}

Met Formulierverzending kunt u formulieren op uw website herkennen en verwerken.

Tijdens het horizontaal schuiven en indexeren van uw website wordt elk aangetroffen formulier vergeleken met de formulierdefinities die u hebt toegevoegd. Als een formulier overeenkomt met een formulierdefinitie, wordt het formulier verzonden voor indexering. Als een formulier met meerdere definities overeenkomt, wordt het formulier één keer verzonden voor elke overeenkomende definitie.

## Formulierdefinities toevoegen voor het indexeren van formulieren op uw website {#task_62FBCE9E6DBE4BDA8D1249233ADFC00F}

U kunt formulieren verwerken die op uw website worden herkend voor indexeringsdoeleinden. [!DNL Form Submission]

Zorg ervoor dat u de site-index opnieuw genereert, zodat de resultaten van de wijzigingen zichtbaar zijn voor uw klanten.

Zie Een incrementele index van een gefaseerde website [](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)configureren.

**Formulierdefinities toevoegen voor het indexeren van formulieren op uw website**

1. Klik in het menu Product op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Form Submission]**.
1. Klik op de [!DNL Form Submission] pagina **[!UICONTROL Add New Form]**.
1. Stel op de [!DNL Add Form Definition] pagina de [!DNL Form Recognition] en [!DNL Form Submission] opties in.

   De vijf opties in de [!DNL Form Recognition] sectie op de [!DNL Form Definition] pagina worden gebruikt om formulieren in uw webpagina&#39;s te identificeren die kunnen worden verwerkt.

   De drie opties in de [!DNL Form Submission] sectie worden gebruikt om de parameters en waarden op te geven die met een formulier naar uw webserver worden verzonden.

   Voer één herkenning- of verzendingsparameter per regel in. Elke parameter moet een naam en een waarde bevatten.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p> <b>Formulierherkenning</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Pagina-URL-masker </p> </td> 
      <td colname="col2"> <p>Identificeer de webpagina of pagina's die het formulier bevatten. Als u een formulier wilt identificeren dat op één pagina wordt weergegeven, voert u de URL voor die pagina in, zoals in het volgende voorbeeld: </p> <p> <code> https://www.mydomain.com/login.html </code> </p> <p>Als u formulieren wilt identificeren die op meerdere pagina's voorkomen, geeft u een URL-masker op dat jokertekens gebruikt om de pagina's te beschrijven. Als u formulieren wilt identificeren die op een willekeurige ASP-pagina worden aangetroffen, geeft u bijvoorbeeld het volgende op: <code> https://www.mydomain.com/register/ </code> </p> <p> <code> https://www.mydomain.com/register/*.asp&amp;nbsp; </code> </p> <p>U kunt ook een reguliere expressie gebruiken om meerdere pagina's te identificeren. Geef de 
      <userinput>
        regexp 
      </userinput> trefwoord vóór het URL-masker, zoals in het volgende voorbeeld: </p> <p> <code> regexp&amp;nbsp;^https://www\.mydomain\.com/.*/login\.html$ </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Handeling-URL-masker </p> </td> 
      <td colname="col2"> <p>Identificeert het actiekenmerk van 
      <userinput>
        &lt;form&gt; 
      </userinput> tag. </p> <p>Net als het pagina-URL-masker kan het actie-URL-masker de vorm aannemen van één URL, een URL met jokertekens of een reguliere expressie. </p> <p>Het URL-masker kan een van de volgende items zijn: 
      <ul id="ul_EDFE7688D3DD4C0BBACCE5D4648D8E44"> 
      <li id="li_77550A448D954EF29FF33EE5E8B5E0F5"> Een volledig pad zoals in het volgende voorbeeld: <code> https://www.mydomain.com/products.html </code> </li> 
      <li id="li_F84E25553BBA41419BE153DC0709E011"> Een gedeeltelijk pad zoals in het volgende voorbeeld: <code> https://www.mydomain.com/products </code> </li> 
      <li id="li_8DADA1C8604740FCACBA30B4AAADB2A1"> Een URL die jokertekens gebruikt zoals in het volgende voorbeeld: <code> https://www.mydomain.com/*.html </code> </li> 
      <li id="li_1EF637B450654B509AA4B618F7FD3C2B"> Een reguliere expressie zoals in het volgende voorbeeld: <code> regexp&amp;nbsp^https://www\.mydomain\.com/.*/login\.html$ </code> </li> 
      </ul> </p> <p>Als u de tekst niet wilt indexeren op pagina's die worden geïdentificeerd door een URL-masker of door een actie-URL-masker, of als u geen koppelingen op die pagina's wilt laten volgen, kunt u de opdracht 
      <userinput>
        noindex 
      </userinput> en 
      <userinput>
        nofollow 
      </userinput> trefwoorden. U kunt deze trefwoorden aan uw maskers toevoegen met behulp van URL-maskers of ingangspunten. </p> <p>Zie <a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573" type="concept" format="dita" scope="local"> Informatie over URL-invoerpunten </a>. </p> <p>Zie <a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164" type="concept" format="dita" scope="local"> Informatie over URL-maskers </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Masker voor formuliernaam </p> </td> 
      <td colname="col2"> <p>Identificeert formulieren als de 
      <userinput>
        &lt;form&gt; 
      </userinput> -tags op uw webpagina's bevatten een naamkenmerk. </p> <p>U kunt een eenvoudige naam gebruiken ( 
      <userinput>
        login_form 
      </userinput>), een naam met een jokerteken ( 
      <userinput>
        formulier* 
      </userinput>), of een reguliere expressie ( 
      <userinput>
        regexp ^.*autoriseren.*$ 
      </userinput>). </p> <p>U kunt dit veld gewoonlijk leeg laten, omdat formulieren doorgaans geen naamkenmerk hebben. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Formulier-id-masker </p> </td> 
      <td colname="col2"> <p>Identificeert formulieren als de 
      <userinput>
        &lt;form&gt; 
      </userinput> -tags op uw webpagina's bevatten een id-kenmerk. </p> <p>U kunt een eenvoudige naam gebruiken ( 
      <userinput>
        login_form 
      </userinput>), een naam met een jokerteken ( 
      <userinput>
        formulier* 
      </userinput>), of een reguliere expressie ( 
      <userinput>
        regexp ^.*autoriseren.*$ 
      </userinput>). </p> <p>U kunt dit veld gewoonlijk leeg laten, omdat formulieren doorgaans geen naamkenmerk hebben. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parameters </p> </td> 
      <td colname="col2"> <p>Identificeer formulieren die een benoemde parameter of een benoemde parameter met een specifieke waarde bevatten of deze niet bevatten. </p> <p>Als u bijvoorbeeld een formulier wilt identificeren dat een e-mailparameter bevat die vooraf is ingesteld op rick_brough@mydomain.com, een wachtwoordparameter, maar geen voornaamparameter, geeft u de volgende parameterinstellingen op, één per regel: </p> <p> <code> email=rick_brough@mydomain.com password  not&nbsp;first-name </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>Formulierverzending</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>URL handeling negeren </p> </td> 
      <td colname="col2"> <p>Geef op wanneer het doel van het verzenden van het formulier afwijkt van wat is opgegeven in het actiekenmerk van het formulier. </p> <p>U kunt deze optie bijvoorbeeld gebruiken wanneer het formulier wordt verzonden door middel van een JavaScript-functie die een URL-waarde bouwt die afwijkt van wat in het formulier wordt gevonden. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Overschrijvingsmethode </p> </td> 
      <td colname="col2"> <p>Geef op wanneer het doel van het verzenden van het formulier afwijkt van wat wordt gebruikt in het actiekenmerk van het formulier en wanneer het verzenden van JavaScript de methode heeft gewijzigd. </p> <p>De standaardwaarden voor alle formulierparameters ( 
      <userinput>
        &lt;input&gt; 
      </userinput> -tags, inclusief verborgen velden), de standaardinstelling 
      <userinput>
        &lt;option&gt; 
      </userinput> van een 
      <userinput>
        &lt;select&gt; 
      </userinput> en de standaardtekst tussen 
      <userinput>
        &lt;textarea&gt;..&lt;/textarea&gt; 
      </userinput> -tags) worden gelezen van de webpagina. Elke parameter die in de sectie <span class="wintitle"> Formulierverzending </span> in het <span class="uicontrol"> veld </span> Parameters wordt vermeld, wordt echter vervangen door de standaardwaarden van het formulier. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parameters </p> </td> 
      <td colname="col2"> <p>U kunt parameters voor het verzenden van formulieren vooraf instellen op 
      <userinput>
        niet 
      </userinput> trefwoord. </p> <p>Wanneer u een parameter voorstelt met 
      <userinput>
        niet 
      </userinput>, wordt het niet ingediend als onderdeel van de indiening van het formulier. Dit gedrag is handig voor selectievakjes die moeten worden verzonden zonder selectie. </p> <p>Stel dat u de volgende parameters wilt verzenden: </p> <p> 
      <ul id="ul_962D12BACF464FF189DB12BFAFCC93A6"> 
      <li id="li_830C6C3EC8D2448388A453BB8EDE5940"> De parameter e-mail met de waarde 
      <userinput>
        nobody@mydomain.com 
      </userinput> </li> 
      <li id="li_905497E3FACE472DBDD49392D5B45E01"> De parameter password met de waarde 
      <userinput>
        testament 
      </userinput> </li> 
      <li id="li_AAA411708ADC464793EADF0D821E282E"> De parameter mycheckbox is uitgeschakeld. </li> 
      <li id="li_0D3DDE641E2B4BEF9F570C03FDB40ED2"> <p>Alle andere 
      <userinput>
        &lt;form&gt; 
      </userinput> parameters als standaardwaarden </p> </li> 
      </ul> </p> <p>Uw parameter voor het verzenden van formulieren ziet er als volgt uit: </p> <p> <code> email=nobody@mydomain.com 
        password=tryme 
        not&nbsp;mycheckbox </code> </p> <p>Het methodeattribuut van 
      <userinput>
        &lt;form&gt; 
      </userinput> -tag op de webpagina wordt gebruikt om te bepalen of de gegevens naar uw server worden verzonden met de methode GET of de methode POST. </p> <p>Als de 
      <userinput>
        &lt;form&gt; 
      </userinput> tag bevat geen methodekenmerk, het formulier wordt verzonden met de GET-methode. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Klik op **[!UICONTROL Add]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik op **[!UICONTROL Live]**.

      Zie Live-instellingen [weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)spoelen.

## Een formulierdefinitie bewerken {#task_9FB34E9C8A814DFE9BF7F8F8F69BF314}

U kunt een bestaande formulierdefinitie bewerken als een formulier op uw website is gewijzigd of als u alleen de definitie hoeft te wijzigen.

Houd er rekening mee dat er geen [!DNL History] functie op de [!DNL Form Submission] pagina aanwezig is om wijzigingen in een formulierdefinitie te herstellen.

Zorg ervoor dat u de site-index opnieuw genereert, zodat de resultaten van de wijzigingen zichtbaar zijn voor uw klanten.

Zie Een incrementele index van een gefaseerde website [](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)configureren.

**Een formulierdefinitie bewerken**

1. Klik in het menu Product op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Form Submission]**.
1. Klik rechts van een formulierdefinitie die u wilt bijwerken [!DNL Form Submission] op de **[!UICONTROL Edit]** pagina.
1. Stel op de [!DNL Edit Form Definition] pagina de [!DNL Form Recognition] en [!DNL Form Submission] opties in.

   Zie de optietabel onder Formulierdefinities [toevoegen voor het indexeren van formulieren op uw website](../c-about-settings-menu/c-about-crawling-menu.md#task_62FBCE9E6DBE4BDA8D1249233ADFC00F).
1. Klik op **[!UICONTROL Save Changes]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik op **[!UICONTROL Live]**.

      Zie Live-instellingen [weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)spoelen.

## Een formulierdefinitie verwijderen {#task_C350FC0CDE344F2786215D544C048B5E}

U kunt een bestaande formulierdefinitie verwijderen als het formulier niet meer op uw website staat of als u een bepaald formulier niet meer wilt verwerken en indexeren.

Houd er rekening mee dat er geen [!DNL History] functie op de [!DNL Form Submission] pagina aanwezig is om wijzigingen in een formulierdefinitie te herstellen.

Zorg ervoor dat u de site-index opnieuw genereert, zodat de resultaten van de wijzigingen zichtbaar zijn voor uw klanten.

Zie Een incrementele index van een gefaseerde website [](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)configureren.

**Een formulierdefinitie verwijderen**

1. Klik in het menu Product op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Form Submission]**.
1. Klik rechts van een formulierdefinitie [!DNL Form Submission] die u wilt verwijderen op de **[!UICONTROL Delete]** pagina.

   Zorg ervoor dat u de juiste formulierdefinitie kiest die u wilt verwijderen. Er is geen dialoogvenster voor bevestiging van verwijderen wanneer u **[!UICONTROL Delete]** in de volgende stap klikt.
1. Klik op de [!DNL Delete Form Definition] pagina **[!UICONTROL Delete]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik op **[!UICONTROL Live]**.

      Zie Live-instellingen [weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)spoelen.

## Info over Indexaansluiting {#concept_CA6921E2FBF641F9B4F60C92B32AFA84}

Gebruik deze optie [!DNL Index Connector] om aanvullende invoerbronnen te definiëren voor het indexeren van XML-pagina&#39;s of een feed.

U kunt een invoerbron voor gegevensinvoer gebruiken om toegang te krijgen tot inhoud die is opgeslagen in een formulier dat afwijkt van wat normaal gesproken op een website wordt ontdekt met een van de beschikbare verkenningsmethoden. Elk document dat is gekropen en geïndexeerd, komt direct overeen met een inhoudspagina op uw website. Een gegevensfeed is echter afkomstig uit een XML-document of uit een komma- of tabgescheiden tekstbestand en bevat de inhoudsgegevens die moeten worden geïndexeerd.

Een XML-gegevensbron bestaat uit XML-standaarden of -records die informatie bevatten die correspondeert met afzonderlijke documenten. Deze afzonderlijke documenten worden toegevoegd aan de index. Een tekstgegevensfeed bevat afzonderlijke records met een nieuwe-regelindeling die overeenkomen met afzonderlijke documenten. Deze afzonderlijke documenten worden ook toegevoegd aan de index. In beide gevallen beschrijft een configuratie van de indexconnector hoe de feed moet worden geïnterpreteerd. Elke configuratie beschrijft waar het dossier verblijft en hoe de servers tot het toegang hebben. De configuratie beschrijft ook &quot;afbeelding&quot;informatie. Met andere woorden, hoe de items van elke record worden gebruikt om de metagegevensvelden in de resulterende index te vullen.

Nadat u een definitie van de Schakelaar van de Index aan de [!DNL Staged Index Connector Definitions] pagina toevoegt, kunt u om het even welke configuratie het plaatsen, *behalve* de waarden van de Naam of van het Type veranderen.

Op de [!DNL Index Connector] pagina ziet u de volgende informatie:

* De naam van bepaalde indexschakelaars die u hebt gevormd en toegevoegd.
* Één van de volgende gegevensbrontypes voor elke schakelaar die u hebt toegevoegd:

   * **Tekst** - Eenvoudige &quot;platte&quot; bestanden, komma&#39;s, tabs-afgebakende of andere consistent gescheiden indelingen.
   * **Feed** - XML-feeds.
   * **XML** - Verzamelingen van XML-documenten.

* Of de schakelaar of niet voor volgende wordt toegelaten kruipt en het indexeren gereed.
* Het adres van de gegevensbron.

Zie ook [Informatie over Indexaansluiting](../c-about-settings-menu/c-about-crawling-menu.md#concept_CA6921E2FBF641F9B4F60C92B32AFA84)

## Hoe het indexeringsproces voor Tekst en Diervoeders configuraties in de Schakelaar van de Index werkt {#section_E059A33D61EE4DB0972A37B8A35E9E16}

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Stap </p> </th> 
   <th colname="col2" class="entry"> <p>Proces </p> </th> 
   <th colname="col3" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>1 </p> </td> 
   <td colname="col2"> <p>Download de gegevensbron. </p> </td> 
   <td colname="col3"> <p>Voor configuraties met tekst en feed is het een eenvoudige bestandsdownload. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>Verdeel de gedownloade gegevensbron in afzonderlijke pseudo-documenten. </p> </td> 
   <td colname="col3"> <p>Voor <span class="uicontrol"> Tekst </span>, beantwoordt elke nieuwe lijn-afgebakende lijn van tekst aan een individueel document, en geparseerd gebruikend het gespecificeerde afbakening, zoals een komma of een lusje. </p> <p>Voor <span class="uicontrol"> feed </span>worden de gegevens van elk document geëxtraheerd met een regulier expressiepatroon in de volgende vorm: </p> <p> <code> &lt;${Itemtag}&gt;(.*?)&lt;/${Itemtag}&gt; </code> </p> <p>Gebruikend <span class="uicontrol"> Kaart </span> op de Schakelaar van de <span class="wintitle"> Index voegt </span> pagina toe, creeer een caching exemplaar van de gegevens en creeer dan een lijst van verbindingen voor de kruipper. De gegevens worden opgeslagen in een lokaal geheime voorgeheugen en met de gevormde gebieden bevolkt. </p> <p>De geparseerde gegevens worden naar de lokale cache geschreven. </p> <p>Deze cache wordt later gelezen om de eenvoudige HTML-documenten te maken die de crawler nodig heeft. Bijvoorbeeld: </p> <p> <code> &lt;html&gt;&lt;head&gt; 
      &lt;title&gt;{title}&lt;/title&gt; 
      &lt;meta&nbsp;name="{field}"&nbsp;content="{data}"&nbsp;/&gt; 
      ... 
      &lt;/head&gt;&lt;body&gt; 
      {body} 
      &lt;/body&gt;&lt;/html&gt; </code> </p> <p>Het <span class="codeph"> &lt;title&gt;- </span> element wordt alleen gegenereerd wanneer een toewijzing bestaat voor het metagegevensveld Titel. Op dezelfde manier wordt het <span class="codeph"> &lt;body&gt;- </span> element alleen gegenereerd wanneer er een toewijzing bestaat aan het metagegevensveld Body. </p> <p> <b>Belangrijk</b>: De toewijzing van waarden aan de vooraf gedefinieerde metatag voor URL wordt niet ondersteund. </p> <p>Voor alle andere toewijzingen worden <span class="codeph"> &lt;meta&gt;- </span> tags gegenereerd voor elk veld dat gegevens bevat die in het oorspronkelijke document zijn gevonden. </p> <p>De velden voor elk document worden toegevoegd aan de cache. Voor elk document dat naar het geheime voorgeheugen wordt geschreven, wordt een verbinding ook geproduceerd zoals in de volgende voorbeelden: </p> <p> <code> &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      .... </code> </p> <p>Voor de toewijzing van de configuratie moet één veld zijn geïdentificeerd als primaire sleutel. Deze toewijzing vormt de sleutel die wordt gebruikt wanneer de gegevens van het geheime voorgeheugen worden gehaald. </p> <p>De schuifregelaar herkent de URL- <span class="codeph"> index: </span> schema prefix, die tot de plaatselijk caching gegevens kan dan toegang hebben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>De documentset in de cache horizontaal schuiven. </p> </td> 
   <td colname="col3"> <p>De <span class="codeph"> index: </span> de verbindingen worden toegevoegd aan de kruipende lijst van de kruipler in behandeling, en in de normale kruipende opeenvolging verwerkt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>Verwerk elk document. </p> </td> 
   <td colname="col3"> <p>De sleutelwaarde van elke verbinding beantwoordt aan een ingang in het geheime voorgeheugen, zo het kruipen van elke verbinding resulteert in de gegevens van dat document die van het geheime voorgeheugen worden gehaald. Vervolgens wordt de afbeelding 'geassembleerd' in een HTML-afbeelding die wordt verwerkt en aan de index wordt toegevoegd. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Hoe het indexeringsproces voor de configuraties van XML in de Schakelaar van de Index werkt {#section_7F1551EA51854C5C99F284CE260526EB}

Het indexeringsproces voor de configuratie van XML is gelijkaardig aan het proces voor de configuraties van de Tekst en van de Dia met de volgende kleine veranderingen en de uitzonderingen.

Aangezien de documenten voor XML-crawls al zijn gescheiden in afzonderlijke bestanden, zijn de stappen 1 en 2 in de bovenstaande tabel niet rechtstreeks van toepassing. Als u een URL opgeeft in de **[!UICONTROL Host Address]** en **[!UICONTROL File Path]** velden van de [!DNL Index Connector Add] pagina, wordt deze gedownload en verwerkt als een normaal HTML-document. De verwachting is dat het downloaddocument een inzameling van `<a href="{url}"...` verbindingen bevat, elk waarvan aan een document van XML richt dat wordt verwerkt. Dergelijke koppelingen worden geconverteerd naar het volgende formulier:

```
<a href="index:<ic_config_name>?url="{url}">
```

Als de Adobe-instelling bijvoorbeeld de volgende koppelingen retourneert:

```
<a href="https://www.adobe.com/somepath/doc1.xml">doc 1</a> 
<a href="https://www.adobe.com/otherpath/doc2.xml">doc 2</a>
```

In de bovenstaande tabel is stap 3 niet van toepassing en wordt stap 4 voltooid op het moment van horizontaal schuiven en indexeren.

Afwisselend, kunt u uw documenten van XML met andere documenten mengen die door het kruipen proces van nature werden ontdekt. In dergelijke gevallen kunt u de herschrijfregels ( **[!UICONTROL Settings]** > **[!UICONTROL Rewrite Rules]** > **[!UICONTROL Crawl List Retrieve URL Rules]**) gebruiken om de URL&#39;s van de XML-documenten te wijzigen en deze naar Indexconnector te sturen.

Zie [Info over Crawl List Win URL Rules](../c-about-settings-menu/c-about-rewrite-rules-menu.md#concept_EC8E2E48B99A458D8567B526C9827CBA).

Stel dat u de volgende herschrijfregel hebt:

```
RewriteRule (^http.*[.]xml$) index:Adobe?key=$1
```

Deze regel zet om het even welke URL die met `.xml` in een verbinding van de Schakelaar van de Index beëindigt. De krawler herkent en herschrijft het `index:` URL-schema. Het downloadproces wordt omgeleid via de Index Connector Apache server op de primaire server. Elk gedownload document wordt gecontroleerd gebruikend het zelfde regelmatige uitdrukkingspatroon dat met Beelden wordt gebruikt. In dit geval wordt het gefabriceerde HTML-document echter niet in de cache opgeslagen. In plaats daarvan, wordt het direct overhandigd aan de kruipler voor indexverwerking.

## Hoe te om veelvoudige Verbindingen van de Index te vormen {#section_C2B14C0F06354A57AEF6238FF3814E5D}

U kunt veelvoudige configuraties van de Schakelaar van de Index voor om het even welke rekening bepalen. De configuraties worden automatisch toegevoegd aan de vervolgkeuzelijst in **[!UICONTROL Settings]** > **[!UICONTROL Crawl]** > **[!UICONTROL URL Entrypoints]** , zoals in de volgende afbeelding wordt getoond:

![](assets/url_entrypoints_index_connector.png)

Als u een configuratie in de vervolgkeuzelijst selecteert, wordt de waarde aan het einde van de lijst met URL-ingangspunten toegevoegd.

>[!NOTE]
>
>Terwijl de gehandicapte configuraties van de Schakelaar van de Index aan de drop-down lijst worden toegevoegd, kunt u niet hen selecteren. Als u de zelfde configuratie van de Verbinding van de Index een tweede keer selecteert, wordt het toegevoegd aan het eind van de lijst, en de vorige instantie wordt geschrapt.

Om een de ingangspunt van de Schakelaar van de Index voor stijgend te specificeren kruipt, kunt u ingangen toevoegen gebruikend het volgende formaat:

```
index:<indexconnector_configuration_name>
```

De kruipper verwerkt elk toegevoegd punt als het op de pagina van de Verbindingen van de Index wordt gevonden en toegelaten.

Opmerking: Omdat de URL van elk document wordt samengesteld met de configuratienaam van de Verbinding van de Index en de primaire sleutel van het document, zeker ben u de zelfde configuratienaam van de Verbinding van de Index wanneer het uitvoeren van Incrementele updates gebruikt! Hierdoor kunnen eerder geïndexeerde documenten correct [!DNL Adobe Search&Promote] worden bijgewerkt.

Zie ook [Informatie over URL-invoerpunten](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573).

**Het gebruik van de Kaarten van de Opstelling wanneer u een Schakelaar van de Index toevoegt**

Op het moment dat u een Indexconnector toevoegt, kunt u desgewenst de functie gebruiken **[!UICONTROL Setup Maps]** om een voorbeeld van uw gegevensbron te downloaden. De gegevens worden onderzocht op indexeerbaarheid.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Als u het type van de Schakelaar van de Index kiest... </p> </th> 
   <th colname="col2" class="entry"> <p>De functie Kaarten instellen... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Tekst </p> </td> 
   <td colname="col2"> <p>Hiermee bepaalt u de waarde van het scheidingsteken door eerst tabs en vervolgens verticale balken ( <span class="codeph"> | </span>) en ten slotte komma's ( <span class="codeph"> , </span>). Als u al een scheidingstekenwaarde hebt opgegeven voordat u op <span class="uicontrol"> Setup Maps hebt geklikt </span>, wordt die waarde gebruikt. </p> <p>Het best-geschikte schema resulteert in de gebieden van de Kaart die met gokken bij de aangewezen waarden van de Markering en van het Gebied worden ingevuld. Bovendien wordt een sampling van de geparseerde gegevens weergegeven. Selecteer <span class="uicontrol"> Kopteksten in eerste rij </span> als u weet dat het bestand een koptekstrij bevat. De opstellingsfunctie gebruikt deze informatie om de resulterende kaartingangen beter te identificeren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Feed </p> </td> 
   <td colname="col2"> <p>Downloadt de gegevensbron en voert het eenvoudige ontleden van XML uit. </p> <p>De resulterende XPath-id's worden weergegeven in de tagrijen van de tabel Kaart en vergelijkbare waarden in velden. Deze rijen identificeren slechts de beschikbare gegevens, en produceren niet de meer gecompliceerde definities van XPath. Het is echter nog steeds handig omdat het de XML-gegevens beschrijft en itemtagwaarden identificeert. </p> <p> <p>Opmerking:  De functie van Kaarten van de Opstelling downloadt de volledige bron van XML om zijn analyse uit te voeren. Als het bestand groot is, kan deze bewerking time-out veroorzaken. </p> </p> <p>Wanneer succesvol, identificeert deze functie alle mogelijke punten XPath, die vele niet wenselijk zijn te gebruiken. Zorg ervoor dat u de resulterende definities van de Kaart onderzoekt en degenen verwijdert die u niet nodig hebt of wilt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>XML </p> </td> 
   <td colname="col2"> <p>Hiermee downloadt u de URL van een representatief afzonderlijk document, niet de primaire koppelingenlijst. Dit ene document wordt geparseerd met hetzelfde mechanisme als bij feeds en de resultaten worden weergegeven. </p> <p>Voordat u op <span class="uicontrol"> Toevoegen klikt </span> om de configuratie op te slaan, moet u de URL opnieuw instellen op het primaire document met de koppelingenlijst. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Belangrijk**: De functie Kaarten instellen werkt mogelijk niet voor grote XML-gegevenssets omdat de bestandsparser het gehele bestand in het geheugen probeert te lezen. Dit heeft tot gevolg dat u een toestand van onvoldoende geheugen kunt ervaren. Wanneer hetzelfde document echter wordt verwerkt op het moment van indexering, wordt het niet in het geheugen gelezen. In plaats daarvan worden grote documenten onderweg verwerkt en niet helemaal in het geheugen gelezen.

**Het gebruik van Voorvertoning wanneer u een Indexconnector toevoegt**

Op het moment dat u een Indexconnector toevoegt, kunt u optioneel de functie gebruiken **[!UICONTROL Preview]** om de gegevens te valideren, alsof u deze opslaat. Het stelt een test tegen de configuratie in werking, maar zonder de configuratie aan de rekening op te slaan. De test heeft toegang tot de geconfigureerde gegevensbron. De downloadcache wordt echter naar een tijdelijke locatie geschreven. er is geen conflict met de hoofdcachemap die door de indexerende crawler wordt gebruikt.

De voorproef verwerkt slechts een gebrek van vijf documenten zoals die door Acct:IndexConnector-Voorproef-Max-Documenten worden gecontroleerd. De voorvertoonde documenten worden getoond in bronvorm, aangezien zij aan de indexerende kruipper worden voorgesteld. De vertoning is gelijkaardig aan een &quot;Bron van de Mening&quot;eigenschap in browser van het Web. U kunt met standaardnavigatiekoppelingen door de documenten in de voorvertoningsset navigeren.

Voorvertoning ondersteunt geen XML-configuraties omdat dergelijke documenten rechtstreeks worden verwerkt en niet naar de cache worden gedownload.

## Een definitie van een indexaansluiting toevoegen {#task_96779B651A654E1F871F55D6DBBC8886}

Elke configuratie van de Verbinding van de Index bepaalt een gegevensbron en afbeeldingen om de gegevenspunten met elkaar in verband te brengen die voor die bron aan meta-gegevensgebieden in de index worden bepaald.

Voordat de effecten van de nieuwe en ingeschakelde definitie zichtbaar zijn voor klanten, moet u de index van uw site opnieuw samenstellen.

**Om een definitie van de Verbinding van de Index toe te voegen**

1. Klik in het menu Product op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. Klik op de [!DNL Stage Index Connector Definitions] pagina **[!UICONTROL Add New Index Connector]**.
1. Stel op de [!DNL Index Connector Add] pagina de gewenste verbindingsopties in. Welke opties beschikbaar zijn, is afhankelijk van de **[!UICONTROL Type]** optie die u hebt geselecteerd.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Naam </p> </td> 
      <td colname="col2"> <p>De unieke naam van de configuratie van de Verbinding van de Index. U kunt alfanumerieke tekens gebruiken. De tekens "_" en "-" zijn ook toegestaan. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Type </p> </td> 
      <td colname="col2"> <p>De bron van uw gegevens. Het gegevensbrontype dat u selecteert beïnvloedt de resulterende opties die op de <span class="wintitle"> Schakelaar van de Index beschikbaar zijn voegt </span> pagina toe. U kunt uit het volgende kiezen: </p> <p> 
      <ul id="ul_1ADC3DFBC929467385F7465BE8E13635"> 
      <li id="li_64FCD749F55442BAB316BD474128D4F9"> <span class="uicontrol"> Tekst </span> <p>Eenvoudige, platte tekstbestanden, komma-afgebakende, tabgescheiden of andere consistent gescheiden indelingen. Elke nieuwe regel tekst die door een nieuwe regel wordt gescheiden, komt overeen met een afzonderlijk document en wordt met het opgegeven scheidingsteken geparseerd. </p> <p>U kunt elke waarde of kolom toewijzen aan een metagegevensveld waarnaar wordt verwezen door het kolomnummer, te beginnen bij 1 (één). </p> </li> 
      <li id="li_2A4F16CE6DCE4114B7F8E4FE156252BB"> <span class="uicontrol"> Feed </span> <p>Downloadt een primair XML-document dat meerdere "rijen" met informatie bevat. </p> </li> 
      <li id="li_5A61C53522D74D4C9A5F65989604BDEF"> <span class="uicontrol"> XML </span> <p>Hiermee wordt een primair XML-document gedownload dat koppelingen bevat ( 
      <userinput>
        &lt;a&gt; 
      </userinput>) aan afzonderlijke XML-documenten. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>Type gegevensbron: Tekst</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ingeschakeld </p> </td> 
      <td colname="col2"> <p>Zet de configuratie "aan"om te kruipen en index. Of, kunt u "van"de configuratie "uitzetten"om het kruipen en het indexeren te verhinderen. </p> <p> <b>Opmerking</b>: De uitgeschakelde configuraties van de Verbinding van de Index worden genegeerd als zij in een ingangspunt lijst worden gevonden. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Adres van gastheer </p> </td> 
      <td colname="col2"> <p>Hier geeft u het adres op van de serverhost waarop de gegevens zich bevinden. </p> <p>U kunt desgewenst een volledig URI-pad (Uniform Resource Identifier) opgeven naar het gegevensbrondocument, zoals in de volgende voorbeelden: </p> <p> <code> https://www.somewhere.com/some_path/some_file.xml </code> </p> <p>of </p> <p> <code> ftp://user:password@ftpserver.somewhere.com/some_path/some_file.xml </code> </p> <p>URI wordt verdeeld in de aangewezen ingangen voor het Adres van de Gastheer, de Weg van het Dossier, het Protocol, en, naar keuze, de gebieden van de Gebruikersnaam, en van het Wachtwoord. </p> <p>Hier geeft u het IP-adres of het URL-adres op van het hostsysteem waar het gegevensbronbestand zich bevindt. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Bestandspad </p> </td> 
      <td colname="col2"> <p>Hiermee geeft u het pad op naar het eenvoudige, platte tekstbestand, een kommagescheiden bestand met tabs of een ander op consistente wijze gescheiden opmaakbestand. </p> <p>Het pad is relatief ten opzichte van de hoofdmap van het hostadres. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Incrementeel bestandspad </p> </td> 
      <td colname="col2"> <p>Hiermee geeft u het pad op naar het eenvoudige, platte tekstbestand, een kommagescheiden bestand met tabs of een ander op consistente wijze gescheiden opmaakbestand. </p> <p>Het pad is relatief ten opzichte van de hoofdmap van het hostadres. </p> <p>Dit bestand wordt, indien opgegeven, gedownload en verwerkt tijdens incrementele indexbewerkingen. Als er geen bestand is opgegeven, wordt in plaats daarvan het bestand onder Bestandspad gebruikt. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Verticaal bestandspad </p> </td> 
      <td colname="col2"> <p>Hiermee geeft u het pad op naar het eenvoudige, platte tekstbestand, een kommagescheiden bestand met tabs of een ander indelingsbestand met een vaste scheidingstekens dat tijdens een verticale update moet worden gebruikt. </p> <p>Het pad is relatief ten opzichte van de hoofdmap van het hostadres. </p> <p>Dit bestand wordt, indien opgegeven, gedownload en verwerkt tijdens bewerkingen voor verticale update. </p> <p> <b>Opmerking</b>: Deze functie is niet standaard ingeschakeld. Neem contact op met Technische ondersteuning om de functie voor uw gebruik te activeren. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Verwijdert bestandspad </p> </td> 
      <td colname="col2"> <p>Hiermee geeft u het pad op naar het eenvoudige platte tekstbestand, met één id-waarde per regel voor het document. </p> <p>Het pad is relatief ten opzichte van de hoofdmap van het hostadres. </p> <p>Dit bestand wordt, indien opgegeven, gedownload en verwerkt tijdens incrementele indexbewerkingen. De waarden in dit bestand worden gebruikt voor het samenstellen van verwijderingsverzoeken om eerder geïndexeerde documenten te verwijderen. De waarden in dit bestand moeten overeenkomen met de waarden in de bestanden met het volledige of incrementele bestandspad in de kolom die als <span class="uicontrol"> primaire sleutel wordt aangeduid </span>. </p> <p> <b>Opmerking</b>: Deze functie is niet standaard ingeschakeld. Neem contact op met Technische ondersteuning om de functie voor uw gebruik te activeren. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocol </p> </td> 
      <td colname="col2"> <p>Hiermee geeft u het protocol op dat wordt gebruikt voor toegang tot het bestand. U kunt uit het volgende kiezen: </p> <p> 
      <ul id="ul_F6BC10FD51CA4A1D855B2B3212838A9C"> 
      <li id="li_79FB7DC65E774ABBB23E57BF98AD9738"> HTTP <p>Indien nodig kunt u de juiste verificatiegegevens invoeren om toegang te krijgen tot de HTTP-server. </p> </li> 
      <li id="li_BAA9AD5E4B014E09B3A66C94022B7225"> HTTPS <p>Indien nodig kunt u de juiste verificatiegegevens invoeren om toegang te krijgen tot de HTTPS-server. </p> </li> 
      <li id="li_E716ABB169DD408BA91F1CA27F445A16"> FTP <p>U moet de juiste verificatiereferenties invoeren om toegang te krijgen tot de FTP-server. </p> </li> 
      <li id="li_FD7143019C5244C3B8A5B1B5AA84859A"> SFTP <p>U moet de juiste verificatiereferenties invoeren om toegang te krijgen tot de SFTP-server. </p> </li> 
      <li id="li_38E0036C1365419F9D00083CACA34AFB"> Bestand </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Time-out </p> </td> 
      <td colname="col2"> <p>Hiermee wordt de time-out in seconden opgegeven voor FTP-, SFTP-, HTTP- of HTTPS-verbindingen. Deze waarde moet liggen tussen 30 en 300. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Opnieuw </p> </td> 
      <td colname="col2"> <p>Hiermee wordt het maximale aantal pogingen opgegeven voor mislukte FTP-, SFTP-, HTTP- of HTTPS-verbindingen. Deze waarde moet tussen 0 en 10 liggen. </p> <p>De waarde nul (0) voorkomt pogingen opnieuw uit te voeren. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Codering </p> </td> 
      <td colname="col2"> <p>Geeft het tekencoderingssysteem aan dat wordt gebruikt in het opgegeven gegevensbronbestand. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Scheidingsteken </p> </td> 
      <td colname="col2"> <p>Hiermee geeft u het teken op dat u wilt gebruiken om elk veld in het opgegeven gegevensbronbestand af te bakenen. </p> <p>Het komma ( <span class="codeph"> , </span>) is een voorbeeld van een scheidingsteken. De komma fungeert als een veldscheidingsteken waarmee gegevensvelden in het opgegeven gegevensbronbestand kunnen worden gescheiden. </p> <p>Tab selecteren <span class="uicontrol"> ? </span> Hiermee gebruikt u het teken voor de horizontale tab als scheidingsteken. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Kopteksten in eerste rij </p> </td> 
      <td colname="col2"> <p>Geeft aan dat de eerste rij in het gegevensbronbestand alleen koptekstinformatie bevat, niet gegevens. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Minimumaantal documenten voor indexering </p> </td> 
      <td colname="col2"> <p>Als de waarde positief is, geeft dit het minimale aantal records op dat in het gedownloade bestand wordt verwacht. Als er minder records worden ontvangen, wordt de indexbewerking afgebroken. </p> <p> <b>Opmerking</b>: Deze functie is niet standaard ingeschakeld. Neem contact op met Technische ondersteuning om de functie voor uw gebruik te activeren. </p> <p> <b>Opmerking</b>: Deze functie wordt alleen gebruikt tijdens volledige indexbewerkingen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Kaart </p> </td> 
      <td colname="col2"> <p>Hiermee geeft u kolomtoewijzingen aan metagegevens op met behulp van kolomnummers. </p> <p> 
      <ul id="ul_981AE2C6D30443BDBFC6575D413732A2"> 
      <li id="li_A42CB9DFFF8C45A7BAC2D471FE96CEBE"> <span class="uicontrol"> Kolom </span> <p> Hiermee geeft u een kolomnummer op, waarbij de eerste kolom 1 (één) is. Als u nieuwe kaartrijen wilt toevoegen voor elke kolom, klikt u onder <span class="wintitle"> Actie </span>op <span class="uicontrol"> + </span>. </p> <p>U hoeft niet naar elke kolom in de gegevensbron te verwijzen. In plaats daarvan kunt u ervoor kiezen waarden over te slaan. </p> </li> 
      <li id="li_26E8C9554A5D4BC5A5073D6385E3626F"> <span class="uicontrol"> Veld </span> <p>Definieert de waarde van het naamkenmerk die wordt gebruikt voor elke gegenereerde &lt;meta&gt;-tag. </p> </li> 
      <li id="li_5DFA514B7F9549B98D6CBC095A66033C"> <span class="uicontrol"> Metagegevens? </span> <p>Hiermee wordt <span class="uicontrol"> Veld een vervolgkeuzelijst </span> waarin u gedefinieerde metagegevensvelden voor de huidige account kunt selecteren. </p> <p>De <span class="uicontrol"> </span> veldwaarde kan desgewenst een ongedefinieerd metagegevensveld zijn. Een niet-gedefinieerd metagegevensveld is soms handig om inhoud te maken die wordt gebruikt door Script <span class="wintitle"> filteren </span>. </p> <p>Zie <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> Scripts filteren </a>. </p> <p>Wanneer de Schakelaar van de Index de documenten van XML met veelvoudige klappen op om het even welk kaartgebied verwerkt, worden de veelvoudige waarden samengevoegd in één enkele waarde in het resulterende caching document. Deze waarden worden standaard gecombineerd met een komma-scheidingsteken. Stel echter dat de corresponderende <span class="wintitle"> </span> veldwaarde een gedefinieerd metagegevensveld is. Bovendien is voor dat veld het <span class="wintitle"> kenmerk Lijsten </span> toestaan ingesteld. In dit geval wordt de waarde van Lijstscheidingstekens van het veld (het eerste gedefinieerde scheidingsteken) gebruikt bij de samenvoeging. </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892C95"> <span class="uicontrol"> Primaire sleutel? </span> <p>Slechts één kaartdefinitie wordt geïdentificeerd als primaire sleutel. Dit veld wordt de unieke referentie die wordt weergegeven wanneer dit document aan de index wordt toegevoegd. Deze waarde wordt gebruikt in de URL van het document in de index. </p> <p>De <span class="uicontrol"> Primaire Zeer belangrijke </span> waarden moeten over alle documenten uniek zijn die door de configuratie van de Schakelaar van de Index worden vertegenwoordigd - om het even welke gevonden duplicaten zullen worden genegeerd. Als uw brondocumenten geen unieke waarde voor gebruik als <span class="uicontrol"> Primaire Sleutel bevatten </span>, maar twee of meer velden samen <i>kunnen</i> een unieke identificatie vormen, kunt u de <span class="uicontrol"> Primaire Sleutel bepalen </span> door de veelvoudige waarden van de <span class="uicontrol"> </span> Kolom met een verticale bar ("|") te combineren die de waarden afbakenen. </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892D96"> <span class="uicontrol"> HTML verwijderen? </span> <p>Als deze optie is ingeschakeld, worden alle HTML-tags in de gegevens van dit veld verwijderd. </p> </li> 
      <li id="li_359D2902859B4C5BADB0BA26F0BA4DC0"> <span class="uicontrol"> Handeling </span> <p>Hiermee kunt u rijen toevoegen aan de kaart of rijen verwijderen van de kaart. De volgorde van de rijen is niet belangrijk. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>Type gegevensbron: Feed</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ingeschakeld </p> </td> 
      <td colname="col2"> <p>Zet de configuratie "aan"om te kruipen en index. Of, kunt u "van"de configuratie "uitzetten"om het kruipen en het indexeren te verhinderen. </p> <p> <b>Opmerking</b>: De uitgeschakelde configuraties van de Verbinding van de Index worden genegeerd als zij in een ingangspunt lijst worden gevonden. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Adres van gastheer </p> </td> 
      <td colname="col2"> <p>Hier geeft u het IP-adres of het URL-adres op van het hostsysteem waar het gegevensbronbestand zich bevindt. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Bestandspad </p> </td> 
      <td colname="col2"> <p>Hiermee geeft u het pad op naar het primaire XML-document dat meerdere rijen met informatie bevat. </p> <p>Het pad is relatief ten opzichte van de hoofdmap van het hostadres. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Incrementeel bestandspad </p> </td> 
      <td colname="col2"> <p>Hiermee geeft u het pad op naar het incrementele XML-document dat meerdere "rijen" met informatie bevat. </p> <p>Het pad is relatief ten opzichte van de hoofdmap van het hostadres. </p> <p>Dit bestand wordt, indien opgegeven, gedownload en verwerkt tijdens incrementele indexbewerkingen. Als er geen bestand is opgegeven, wordt in plaats daarvan het bestand onder Bestandspad gebruikt. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Verticaal bestandspad </p> </td> 
      <td colname="col2"> <p>Hiermee geeft u het pad naar het XML-document op dat meerdere kleine 'rijen' met informatie bevat die tijdens een verticale update moet worden gebruikt. </p> <p>Het pad is relatief ten opzichte van de hoofdmap van het hostadres. </p> <p>Dit bestand wordt, indien opgegeven, gedownload en verwerkt tijdens bewerkingen voor verticale update. </p> <p> <b>Opmerking</b>: Deze functie is niet standaard ingeschakeld. Neem contact op met Technische ondersteuning om de functie voor uw gebruik te activeren. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Verwijdert bestandspad </p> </td> 
      <td colname="col2"> <p>Hiermee geeft u het pad op naar het eenvoudige platte tekstbestand, met één id-waarde per regel voor het document. </p> <p>Het pad is relatief ten opzichte van de hoofdmap van het hostadres. </p> <p>Dit bestand wordt, indien opgegeven, gedownload en verwerkt tijdens incrementele indexbewerkingen. De waarden in dit bestand worden gebruikt voor het samenstellen van verwijderingsverzoeken om eerder geïndexeerde documenten te verwijderen. De waarden in dit bestand moeten overeenkomen met de waarden in de bestanden met het volledige of incrementele bestandspad in de kolom die als <span class="uicontrol"> primaire sleutel wordt aangeduid </span>. </p> <p> <b>Opmerking</b>: Deze functie is niet standaard ingeschakeld. Neem contact op met Technische ondersteuning om de functie voor uw gebruik te activeren. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocol </p> </td> 
      <td colname="col2"> <p>Hiermee geeft u het protocol op dat wordt gebruikt voor toegang tot het bestand. U kunt uit het volgende kiezen: </p> <p> 
      <ul id="ul_976A34FD14A841F2B610C1C0CCBB82B9"> 
      <li id="li_05BBA0F670F14431A89AE4178F1A6F94"> HTTP <p>Indien nodig kunt u de juiste verificatiegegevens invoeren om toegang te krijgen tot de HTTP-server. </p> </li> 
      <li id="li_100446691F304572B8FC3F083F86A2CB"> HTTPS <p>Indien nodig kunt u de juiste verificatiegegevens invoeren om toegang te krijgen tot de HTTPS-server. </p> </li> 
      <li id="li_027088A8E30444DAA8CCCC5B0BAA74C1"> FTP <p>U moet de juiste verificatiereferenties invoeren om toegang te krijgen tot de FTP-server. </p> </li> 
      <li id="li_DCEF9D5C99354990B03E29083C2ED8DC"> SFTP <p>U moet de juiste verificatiereferenties invoeren om toegang te krijgen tot de SFTP-server. </p> </li> 
      <li id="li_44E34FF2AB0D429EB3408106E6FCF780"> Bestand </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Itemtag </p> </td> 
      <td colname="col2"> <p>Identificeert het element van XML dat u kunt gebruiken om individuele lijnen van XML in het gegevensbrondossier te identificeren dat u specificeerde. </p> <p>In het volgende fragment Feed van een Adobe XML-document is de waarde ItemTag bijvoorbeeld <span class="codeph"> record </span>: </p> <p> <code> &lt;?xml&nbsp;version="1.0"&nbsp;encoding="utf-8"?&gt; 
        &lt;!DOCTYPE&nbsp;gsafeed&nbsp;PUBLIC&nbsp;"-//Google//DTD&nbsp;GSA&nbsp;Feeds//EN"&nbsp;""&gt; &lt;gsafeed&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;header&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;datasource&gt;marketplace&lt;/datasource&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;feedtype&gt;incremental&lt;/feedtype&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/header&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;group&nbsp;action="add"&gt; 
        &lt;record&nbsp;url=https://www.adobe.com/cfusion/marketplace_gsa
        index.cfm?event=marketplace.home&amp;amp;marketplaceid=1&nbsp;action="add"&nbsp;mimetype="text/html"displayurl="https://www.adobe.com/cfusion/marketplace/index.cfm?event=marketplace.home&amp;amp;marketplaceid=1"&gt;&lt;metadata&gt; 
        &lt;meta&nbsp;name="mp_mkt"&nbsp;content="1"/&gt; 
        &lt;meta&nbsp;name="mp_logo"&nbsp;content="/images/marketplace/ 
        dbreferenced/marketplaceicons/icn_air.png"/&gt; 
        &lt;meta&nbsp;name="title"&nbsp;content="Adobe&nbsp;AIR&nbsp;Marketplace"/&gt; 
        &lt;meta&nbsp;name="description"&nbsp;content="Discover&nbsp;new&nbsp;applications&nbsp;..."/&gt; &lt;/metadata&gt; 
        &lt;content&gt;&lt;![CDATA[&lt;html&gt;&lt;head&gt;&lt;title&gt;Adobe&nbsp;AIR&nbsp;Marketplace&lt;/title&gt;&lt;/head&gt;&lt;body&gt;Discover&nbsp;new&nbsp;applications&nbsp;...&lt;/body&gt;&lt;/html&gt;]]&gt;&lt;/cntent&gt; 
        &lt;/record&gt; 
        &lt;record&nbsp;url=https://www.adobe.com/cfusion/marketplace_gsa/
        index.cfm?event=marketplace.home&amp;amp;marketplaceid=2&nbsp;action="add"&nbsp;mimetype="text/html"&nbsp;displayurl="https://www.adobe.com/cfusion/ 
        marketplace/index.cfm?event=marketplace.home&amp;amp;marketplaceid=2"&gt; 
        &lt;metadata&gt; 
        &lt;meta&nbsp;name="mp_mkt"&nbsp;content="2"/&gt; 
        &lt;meta&nbsp;name="mp_logo"&nbsp;content="/images/marketplace/ 
        dbreferenced/marketplaceicons/icn_photoshop.png"/&gt;         &lt;meta&nbsp;name="title"&nbsp;content="Adobe&nbsp;Photoshop&nbsp;Marketplace"/&gt;         &lt;meta&nbsp;name="description"&nbsp;content="Extend&nbsp;your&nbsp;creative&nbsp;possibilities&nbsp;..."/&gt; 
        &lt;/metadata&gt;         &lt;content&gt;&lt;![CDATA[&lt;html&gt;&lt;head&gt;&lt;title&gt;Adobe&nbsp;Photoshop&nbsp;Marketplace&lt;/title&gt;&lt;/head&gt;&lt;body&gt;Extend&nbsp;your&nbsp;creative&nbsp;possibilities&nbsp;...&lt;/body&gt;&lt;/html&gt;]]&gt;/content&gt; 
        &lt;/record&gt; 
        ... 
        &lt;record&gt; 
        ... 
        &lt;/record&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/group&gt; 
        &lt;/gsafeed&gt; 
        </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Minimumaantal documenten voor indexering </p> </td> 
      <td colname="col2"> <p>Als de waarde positief is, geeft dit het minimale aantal records op dat in het gedownloade bestand wordt verwacht. Als er minder records worden ontvangen, wordt de indexbewerking afgebroken. </p> <p> <b>Opmerking</b>: Deze functie is niet standaard ingeschakeld. Neem contact op met Technische ondersteuning om de functie voor uw gebruik te activeren. </p> <p> <b>Opmerking</b>: Deze functie wordt alleen gebruikt tijdens volledige indexbewerkingen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Kaart </p> </td> 
      <td colname="col2"> <p>Hiermee kunt u XML-element-aan-metagegevenstoewijzingen opgeven met XPath-expressies. </p> <p> 
      <ul id="ul_604108C0277C4892AE8A40CA39889ABD"> 
      <li id="li_0AF92270AE9F4BA8B2C7EE41FABC0F34"> <span class="uicontrol"> Tag </span> <p>Hiermee wordt een XPath-representatie van de geparseerde XML-gegevens opgegeven. Met behulp van het voorbeeld van het Adobe XML-document hierboven, onder de optie Item-tag, kan deze worden toegewezen met behulp van de volgende syntaxis: </p> <p> <code> /record/@displayurl&nbsp;-&gt;&nbsp;page-url 
      /record/metadata/meta[@name='title']/@content&nbsp;-&gt;&nbsp;title 
      /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;desc 
      /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;body </code> </p> <p>De bovenstaande syntaxis wordt als volgt vertaald: </p> <p> 
      <ul id="ul_6400EBD08D424EADA1612FE4F7EFB640"> 
      <li id="li_9958F9B40D42434195597DBA9F2AF28F"> <code> /record/@displayurl&amp;nbsp;-&gt;&amp;nbsp;page-url </code> <p>Het <span class="codeph"> displayurl- </span> kenmerk van het <span class="codeph"> record- </span> element wordt toegewezen aan het metagegevensveld <span class="codeph"> page-url </span>. </p> </li> 
      <li id="li_759013EA02CD48BE971A55B0A6A11424"> <code> /record/metadata/meta[@name='title']/@content&amp;nbsp;-&gt;&amp;nbsp;title </code> <p>Het <span class="codeph"> inhoudskenmerk </span> van een willekeurig <span class="codeph"> meta- </span> element dat zich in een <span class="codeph"> metagegevenselement bevindt, dat zich in een </span> record- <span class="codeph"> element bevindt, waarvan het naamkenmerk </span> titel is <span class="codeph"> </span><span class="codeph"> </span>, verwijst naar de  titel van het metagegevensveld. </p> </li> 
      <li id="li_E741CA59197D462EB2946EDE874AFDC8"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;desc </code> <p>Het <span class="codeph"> inhoudskenmerk </span> van een willekeurig <span class="codeph"> meta- </span> element dat zich in een <span class="codeph"> metagegevenselement bevindt, dat zich in het </span> record- <span class="codeph"> element bevindt, waarvan het naamkenmerk een </span> beschrijving is <span class="codeph"> </span><span class="codeph"> </span>, wijst toe aan het metagegevensveld c. </p> </li> 
      <li id="li_E35EAE3D284D46D485D9064D7BB6AB13"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;body </code> <p>Het <span class="codeph"> inhoudskenmerk </span> van een willekeurig <span class="codeph"> meta- </span> element dat zich in een <span class="codeph"> metagegevenselement bevindt, dat zich in het </span> record- <span class="codeph"> element bevindt, waarvan het naamkenmerk een </span> beschrijving is <span class="codeph"> </span><span class="codeph"> </span>, wijst toe aan de  tekst van het metagegevensveld. </p> </li> 
      </ul> </p> <p>XPath is een relatief gecompliceerde notatie. Meer informatie is beschikbaar op de volgende locatie: </p> <p>Zie <a href="https://www.w3schools.com/xpath/" scope="external" format="html"> https://www.w3schools.com/xpath/ </a> </p> </li> 
      <li id="li_8147075D7ACD4811A7ED335F23FE62A6"> <span class="uicontrol"> Veld </span> <p>Definieert de waarde van het naamkenmerk die wordt gebruikt voor elke gegenereerde <span class="codeph"> &lt;meta&gt;- </span> tag. </p> </li> 
      <li id="li_2380199D63BF425A919606D8232FA6E2"> <span class="uicontrol"> Metagegevens? </span> <p>Hiermee wordt <span class="uicontrol"> Veld een vervolgkeuzelijst </span> waarin u gedefinieerde metagegevensvelden voor de huidige account kunt selecteren. </p> <p>De <span class="uicontrol"> </span> veldwaarde kan desgewenst een ongedefinieerd metagegevensveld zijn. Een niet-gedefinieerd metagegevensveld is soms handig om inhoud te maken die wordt gebruikt door Script <span class="wintitle"> filteren </span>. </p> <p>Zie <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> Scripts filteren </a>. </p> <p>Wanneer de Schakelaar van de Index de documenten van XML met veelvoudige klappen op om het even welk kaartgebied verwerkt, worden de veelvoudige waarden samengevoegd in één enkele waarde in het resulterende caching document. Deze waarden worden standaard gecombineerd met een komma-scheidingsteken. Stel echter dat de corresponderende <span class="wintitle"> </span> veldwaarde een gedefinieerd metagegevensveld is. Bovendien is voor dat veld het <span class="wintitle"> kenmerk Lijsten </span> toestaan ingesteld. In dit geval wordt de waarde van Lijstscheidingstekens van het veld (het eerste gedefinieerde scheidingsteken) gebruikt bij de samenvoeging. </p> </li> 
      <li id="li_DEA24003E97E406DA2510C43CCFDC70E"> <span class="uicontrol"> Primaire sleutel? </span> <p>Slechts één kaartdefinitie wordt geïdentificeerd als primaire sleutel. Dit veld wordt de unieke referentie die wordt weergegeven wanneer dit document aan de index wordt toegevoegd. Deze waarde wordt gebruikt in de URL van het document in de index. </p> <p>De <span class="uicontrol"> Primaire Zeer belangrijke </span> waarden moeten over alle documenten uniek zijn die door de configuratie van de Schakelaar van de Index worden vertegenwoordigd - om het even welke gevonden duplicaten zullen worden genegeerd. Als uw brondocumenten geen enkele unieke waarde voor gebruik als <span class="uicontrol"> primaire sleutel bevatten </span>, maar twee of meer velden samen een unieke id <i>kunnen</i> vormen, kunt u de <span class="uicontrol"> primaire sleutel definiëren </span> door meerdere <span class="uicontrol"> </span> tagdefinities te combineren met een verticale balk ("|") die de waarden afbakent. </p> </li> 
      <li id="li_DEA24003E97E406DA2510C43CCFDC81F"> <span class="uicontrol"> HTML verwijderen? </span> <p>Als deze optie is ingeschakeld, worden alle HTML-tags in de gegevens van dit veld verwijderd. </p> </li> 
      <li id="li_5E829D1D0DBD4BB7AAB5DB983053D248"> <span class="uicontrol"> Gebruiken voor Verwijderen? </span> <p>Wordt alleen gebruikt tijdens incrementele indexbewerkingen. Records die overeenkomen met dit XPath-patroon identificeren items voor verwijdering. De <span class="uicontrol"> Primaire Zeer belangrijke </span> waarde voor elk dergelijk verslag wordt gebruikt om "schrapping"verzoeken, zoals met de Weg van het Dossier van de Schrapping te construeren. </p> <p> <b>Opmerking</b>: Deze functie is niet standaard ingeschakeld. Neem contact op met Technische ondersteuning om de functie voor uw gebruik te activeren. </p> </li> 
      <li id="li_D40E2F9AD8AD49FC9AC4B8C75BA31E28"> <span class="uicontrol"> Handeling </span> <p>Hiermee kunt u rijen toevoegen aan de kaart of rijen verwijderen van de kaart. De volgorde van de rijen is niet belangrijk. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>Type gegevensbron: XML</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ingeschakeld </p> </td> 
      <td colname="col2"> <p>Zet de configuratie "aan"om te kruipen en index. Of, kunt u "van"de configuratie "uitzetten"om het kruipen en het indexeren te verhinderen. </p> <p> <b>Opmerking</b>: De uitgeschakelde configuraties van de Verbinding van de Index worden genegeerd als zij in een ingangspunt lijst worden gevonden. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Adres van gastheer </p> </td> 
      <td colname="col2"> <p>Hier geeft u het URL-adres op van het hostsysteem waar het gegevensbronbestand wordt gevonden. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Bestandspad </p> </td> 
      <td colname="col2"> <p>Hiermee wordt het pad opgegeven naar het primaire XML-document dat koppelingen bevat ( 
      <userinput>
        &lt;a&gt; 
      </userinput>) aan afzonderlijke XML-documenten. </p> <p>Het pad is relatief ten opzichte van de hoofdmap van het hostadres. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocol </p> </td> 
      <td colname="col2"> <p>Hiermee geeft u het protocol op dat wordt gebruikt voor toegang tot het bestand. U kunt uit het volgende kiezen: </p> <p> 
      <ul id="ul_EA4EB7953D68483FAD75753B2EE70E74"> 
      <li id="li_537F24C6B2AB435CB7C14117663D7B3F"> HTTP <p>Indien nodig kunt u de juiste verificatiegegevens invoeren om toegang te krijgen tot de HTTP-server. </p> </li> 
      <li id="li_8C13C93C52364FFA8B9B18830CDB223C"> HTTPS <p>Indien nodig kunt u de juiste verificatiegegevens invoeren om toegang te krijgen tot de HTTPS-server. </p> </li> 
      <li id="li_2F967B5675254C949B31EAB19910751C"> FTP <p>U moet de juiste verificatiereferenties invoeren om toegang te krijgen tot de FTP-server. </p> </li> 
      <li id="li_C24BE4C1DE79488AA64C7133D78CD3A6"> SFTP <p>U moet de juiste verificatiereferenties invoeren om toegang te krijgen tot de SFTP-server. </p> </li> 
      <li id="li_7581C21CFC104986A361F62BD7A370C1"> Bestand </li> 
      </ul> </p> <p> <b>Opmerking</b>: De instelling Protocol wordt alleen gebruikt als er informatie is opgegeven in de velden Hostadres en/of Bestandspad. Afzonderlijke XML-documenten worden gedownload via HTTP of HTTPS, volgens hun URL-specificaties. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Itemtag </p> </td> 
      <td colname="col2"> <p>Identificeert het XML-element dat een "rij" definieert in het gegevensbronbestand dat u hebt opgegeven. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Kaart </p> </td> 
      <td colname="col2"> <p>Hiermee kunt u kolom-naar-metagegevenstoewijzingen opgeven met behulp van kolomnummers. </p> <p> 
      <ul id="ul_06F50CBA0AA64C7CB1AFAE076E629A64"> 
      <li id="li_0FA2502869BA40DC93D790B79E15A9D2"> <span class="uicontrol"> Tag </span> <p>Hiermee wordt een XPath-representatie van de geparseerde XML-gegevens opgegeven. Met behulp van het bovenstaande voorbeeld van het Adobe XML-document kunt u het document onder de optie Item-tag toewijzen met behulp van de volgende syntaxis: </p> <p> <code> /record/@displayurl&nbsp;-&gt;&nbsp;page-url 
        /record/metadata/meta[@name='title']/@content&nbsp;-&gt;&nbsp;title 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;desc 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;body </code> </p> <p>De bovenstaande syntaxis wordt als volgt vertaald: </p> <p> 
      <ul id="ul_F8C536E6E54546D9AA5B22B879C0AF39"> 
      <li id="li_78A35DFFF1B4496CAC6EDC7B1E991F29"> <code> /record/@displayurl&amp;nbsp;-&gt;&amp;nbsp;page-url </code> <p>Het <span class="codeph"> displayurl- </span> kenmerk van het <span class="codeph"> record- </span> element wordt toegewezen aan het metagegevensveld <span class="codeph"> page-url </span>. </p> </li> 
      <li id="li_FA7DF3D1942248B98660F3D0C82F4563"> <code> /record/metadata/meta[@name='title']/@content&amp;nbsp;-&gt;&amp;nbsp;title </code> <p>Het <span class="codeph"> inhoudskenmerk </span> van een willekeurig <span class="codeph"> meta- </span> element dat zich in een <span class="codeph"> metagegevenselement bevindt, dat zich in een </span> record- <span class="codeph"> element bevindt, waarvan het naamkenmerk </span> titel is <span class="codeph"> </span><span class="codeph"> </span>, verwijst naar de  titel van het metagegevensveld. </p> </li> 
      <li id="li_D8000A116FF84DE59ED19C656DDD3BC1"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;desc </code> <p>Het <span class="codeph"> inhoudskenmerk </span> van een willekeurig <span class="codeph"> meta- </span> element dat zich in een <span class="codeph"> metagegevenselement bevindt, dat zich in het </span> record- <span class="codeph"> element bevindt, waarvan het naamkenmerk een </span> beschrijving is <span class="codeph"> </span><span class="codeph"> </span>, wijst toe aan het metagegevensveld c. </p> </li> 
      <li id="li_7FA6A53DFD3D42A98B7BA17CC29DDB81"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;body </code> <p>Het <span class="codeph"> inhoudskenmerk </span> van een willekeurig <span class="codeph"> meta- </span> element dat zich in een <span class="codeph"> metagegevenselement bevindt, dat zich in het </span> record- <span class="codeph"> element bevindt, waarvan het naamkenmerk een </span> beschrijving is <span class="codeph"> </span><span class="codeph"> </span>, wijst toe aan de  tekst van het metagegevensveld. </p> </li> 
      </ul> </p> <p>XPath is een relatief gecompliceerde notatie. Meer informatie is beschikbaar op de volgende locatie: </p> <p>Zie <a href="https://www.w3schools.com/xpath/" scope="external" format="html"> https://www.w3schools.com/xpath/ </a> </p> </li> 
      <li id="li_84999D07E0AE4265BC7928BBB49957B9"> <span class="uicontrol"> Veld </span> <p>Definieert de waarde van het naamkenmerk die wordt gebruikt voor elke gegenereerde &lt;meta&gt;-tag. </p> </li> 
      <li id="li_E125788D0F5242958BD790E26A675C20"> <span class="uicontrol"> Metagegevens? </span> <p>Hiermee wordt <span class="uicontrol"> Veld een vervolgkeuzelijst </span> waarin u gedefinieerde metagegevensvelden voor de huidige account kunt selecteren. </p> <p>De <span class="uicontrol"> </span> veldwaarde kan desgewenst een ongedefinieerd metagegevensveld zijn. Een niet-gedefinieerd metagegevensveld is soms handig om inhoud te maken die wordt gebruikt door Script <span class="wintitle"> filteren </span>. </p> <p>Zie <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> Scripts filteren </a>. </p> <p>Wanneer de Schakelaar van de Index de documenten van XML met veelvoudige klappen op om het even welk kaartgebied verwerkt, worden de veelvoudige waarden samengevoegd in één enkele waarde in het resulterende caching document. Deze waarden worden standaard gecombineerd met een komma-scheidingsteken. Stel echter dat de corresponderende <span class="wintitle"> </span> veldwaarde een gedefinieerd metagegevensveld is. Bovendien is voor dat veld het <span class="wintitle"> kenmerk Lijsten </span> toestaan ingesteld. In dit geval wordt de waarde van Lijstscheidingstekens van het veld (het eerste gedefinieerde scheidingsteken) gebruikt bij de samenvoeging. </p> </li> 
      <li id="li_9F435EFB3EC74B409EC82A851824609F"> <span class="uicontrol"> Primaire sleutel? </span> <p>Slechts één kaartdefinitie wordt geïdentificeerd als primaire sleutel. Dit veld wordt de unieke referentie die wordt weergegeven wanneer dit document aan de index wordt toegevoegd. Deze waarde wordt gebruikt in de URL van het document in de index. </p> <p>De <span class="uicontrol"> Primaire Zeer belangrijke </span> waarden moeten over alle documenten uniek zijn die door de configuratie van de Schakelaar van de Index worden vertegenwoordigd - om het even welke gevonden duplicaten zullen worden genegeerd. Als uw brondocumenten geen enkele unieke waarde voor gebruik als <span class="uicontrol"> primaire sleutel bevatten </span>, maar twee of meer velden samen een unieke id <i>kunnen</i> vormen, kunt u de <span class="uicontrol"> primaire sleutel definiëren </span> door meerdere <span class="uicontrol"> </span> tagdefinities te combineren met een verticale balk ("|") die de waarden afbakent. </p> </li> 
      <li id="li_9F435EFB3EC74B409EC82A851824610G"> <span class="uicontrol"> HTML verwijderen? </span> <p>Als deze optie is ingeschakeld, worden alle HTML-tags in de gegevens van dit veld verwijderd. </p> </li> 
      <li id="li_6302D18971AD439FBECE27742649C56B"> <span class="uicontrol"> Handeling </span> <p>Hiermee kunt u rijen toevoegen aan de kaart of rijen verwijderen van de kaart. De volgorde van de rijen is niet belangrijk. </p> </li> 
      </ul> </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. (Optioneel) Klik **[!UICONTROL Setup Maps]** om een voorbeeld van uw gegevensbron te downloaden. De gegevens worden onderzocht op indexeerbaarheid. Deze functie is alleen beschikbaar voor Tekst- en Feed-typen.
1. (Optioneel) Klik **[!UICONTROL Preview]** om de werking van de configuratie zelf te testen. Deze functie is alleen beschikbaar voor Tekst- en Feed-typen.
1. Klik **[!UICONTROL Add]** om de configuratie aan de [!DNL Index Connector Definitions] pagina en aan de [!DNL Index Connector Configurations] drop-down lijst op de [!DNL URL Entrypoints] pagina toe te voegen.

   Zie [Informatie over URL-invoerpunten](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573).
1. Klik op de [!DNL Index Connector Definitions] pagina **[!UICONTROL rebuild your staged site index]**.
1. (Optioneel) Voer op de [!DNL Index Connector Definitions] pagina een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om de aangebrachte wijzigingen terug te draaien.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie Live-instellingen [weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)spoelen.

## Een definitie van een indexaansluiting bewerken {#task_DCFC9C6A9964421DB5AB6C25DEE98DE9}

U kunt een bestaande Indexconnector bewerken die u hebt gedefinieerd.

>[!NOTE]
>
>U kunt niet alle opties wijzigen, zoals de naam of het type van de indexaansluiting in de [!DNL Type] vervolgkeuzelijst.

**Om een definitie van de Verbinding van de Index uit te geven**

1. Klik in het menu Product op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. Voor de [!DNL Index Connector] pagina, onder de [!DNL Actions] kolomrubriek, klik **[!UICONTROL Edit]** voor een de definitienaam van de Schakelaar van de Index waarvan montages u wilt veranderen.
1. Stel op de [!DNL Index Connector Edit] pagina de gewenste opties in.

   Zie de optietabel onder [Een definitie](../c-about-settings-menu/c-about-crawling-menu.md#task_96779B651A654E1F871F55D6DBBC8886)voor indexaansluiting toevoegen.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Optioneel) Klik op de [!DNL Index Connector Definitions] pagina **[!UICONTROL rebuild your staged site index]**.
1. (Optioneel) Voer op de [!DNL Index Connector Definitions] pagina een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om de aangebrachte wijzigingen terug te draaien.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie Live-instellingen [weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)spoelen.

## De instellingen van een definitie van een indexaansluiting weergeven {#task_D0B71A7426E54247BDB3468EC576D871}

U kunt de configuratiemontages van een bestaande definitie van de indexschakelaar herzien.

Nadat een definitie van de Schakelaar van de Index aan de [!DNL Index Connector Definitions] pagina wordt toegevoegd, kunt u niet zijn het Type plaatsen veranderen. In plaats daarvan moet u de definitie verwijderen en vervolgens een nieuwe definitie toevoegen.

**De instellingen van de definitie van een indexaansluiting weergeven**

1. Klik in het menu Product op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. Voor de [!DNL Index Connector] pagina, onder de [!DNL Actions] kolomrubriek, klik **[!UICONTROL Edit]** voor een de definitienaam van de Schakelaar van de Index waarvan montages u wilt herzien of uitgeven.

## Een definitie van een indexaansluiting kopiëren {#task_3AD55DF07FC44A748D0EFDAB7B35699B}

U kunt een bestaande definitie van de Schakelaar van de Index kopiëren om als basis voor een nieuwe Schakelaar van de Index te gebruiken die u wilt tot stand brengen.

Wanneer het kopiëren van een definitie van de Schakelaar van de Index, wordt de gekopieerde definitie onbruikbaar gemaakt door gebrek. Als u de definitie wilt in- of inschakelen, moet u deze bewerken vanaf de [!DNL Index Connector Edit] pagina en vervolgens **[!UICONTROL Enable]** selecteren.

Zie [Een definitie](../c-about-settings-menu/c-about-crawling-menu.md#task_DCFC9C6A9964421DB5AB6C25DEE98DE9)voor indexaansluiting bewerken.

**Om een definitie van de Verbinding van de Index te kopiëren**

1. Klik in het menu Product op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. Voor de [!DNL Index Connector] pagina, onder de [!DNL Actions] kolomrubriek, klik **[!UICONTROL Copy]** voor een de definitienaam van de Schakelaar van de Index waarvan montages u wilt dupliceren.
1. Voer op de [!DNL Index Connector Copy] pagina de nieuwe naam van de definitie in.
1. Klik op **[!UICONTROL Copy]**.
1. (Optioneel) Voer op de [!DNL Index Connector Definitions] pagina een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om de aangebrachte wijzigingen terug te draaien.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie Live-instellingen [weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)spoelen.

## De naam van een indexverbindingsdefinitie wijzigen {#task_5132118FC21B47D99881E0ED425225D7}

U kunt de naam van een bestaande definitie van de Verbinding van de Index veranderen.

Nadat u de naam van de definitie hebt gewijzigd, kiest u **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**. U wilt ervoor zorgen dat de nieuwe definitienaam in de drop-down lijst op de [!DNL URL Entrypoints] pagina wordt weerspiegeld.

Zie Meerdere URL-ingangspunten [toevoegen die u wilt indexeren](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45).

**De naam van een indexverbindingsdefinitie wijzigen**

1. Klik in het menu Product op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. Voor de [!DNL Index Connector] pagina, onder de [!DNL Actions] kolomrubriek, klik **[!UICONTROL Rename]** voor de definitienaam van de Schakelaar van de Index die u wilt veranderen.
1. Voer op de [!DNL Index Connector Rename] pagina de nieuwe naam van de definitie in het [!DNL Name] veld in.
1. Klik op **[!UICONTROL Rename]**.
1. Klik op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**. Als de naam van de vorige Index-connector in de lijst voorkomt, verwijdert u deze en voegt u het item met de nieuwe naam toe.

   Zie Meerdere URL-ingangspunten [toevoegen die u wilt indexeren](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45). 1. (Optioneel) Voer op de [!DNL Index Connector Definitions] pagina een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om de aangebrachte wijzigingen terug te draaien.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie Live-instellingen [weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)spoelen.

## Een definitie van een indexaansluiting verwijderen {#task_6B0BD5D0C09F4597A401B0F3AC7C7EA7}

U kunt een bestaande definitie van de Verbinding van de Index schrappen die u niet meer nodig hebt of gebruikt.

**Om een definitie van de Verbinding van de Index te schrappen**

1. Klik in het menu Product op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. Voor de [!DNL Index Connector Definitions] pagina, onder de [!DNL Actions] kolomrubriek, klik **[!UICONTROL Delete]** voor de de definitienaam van de Schakelaar van de Index u wilt verwijderen.
1. Klik op de [!DNL Index Connector Delete] pagina **[!UICONTROL Delete]**.
