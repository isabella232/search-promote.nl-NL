---
description: Gebruik de Verpletterende datum van de menuset en de maskers URL, wachtwoorden, inhoudstypes, verbindingen, vormdefinities, en ingang URL.
seo-description: Gebruik de Verpletterende datum van de menuset en de maskers URL, wachtwoorden, inhoudstypes, verbindingen, vormdefinities, en ingang URL.
seo-title: Informatie over het menu Crawling
solution: Target
subtopic: Crawling
title: Informatie over het menu Crawling
topic: Settings,Site search and merchandising
uuid: a58c03bf-90f7-4b5b-91ff-988b95c246b0
translation-type: tm+mt
source-git-commit: 77a4e88c7bf47b637030e3935a39dfdf4f175e80

---


# Informatie over het menu Crawling{#about-the-crawling-menu}

Gebruik de Verpletterende datum van de menuset en de maskers URL, wachtwoorden, inhoudstypes, verbindingen, vormdefinities, en ingang URL.

## Informatie over URL-invoerpunten {#concept_5D857E3B5C124E85BC0B5AE77A509573}

De meeste websites hebben één primair ingangspunt of homepage dat een klant aanvankelijk bezoekt. Dit belangrijkste ingangspunt is het adres URL waarvan de onderzoeksrobot begint index kruipend te zijn. Nochtans, als uw website veelvoudige domeinen of subdomain heeft, of als de gedeelten van uw plaats niet van het primaire ingangspunt verbonden zijn, kunt u Inschrijvingen URL gebruiken om meer ingangspunten toe te voegen.

Alle webpagina&#39;s onder elk opgegeven URL-instappunt worden geïndexeerd. U kunt Url- ingangspunten met maskers combineren om precies te controleren welke gedeelten van een website die u wilt indexeren. U moet uw websiteindex herbouwen alvorens de gevolgen van de montages van de Ingangen URL aan klanten zichtbaar zijn.

Het belangrijkste ingangspunt is typisch URL van de website die u wilt indexeren en zoeken. U vormt dit belangrijkste ingangspunt in de Montages van de Rekening.

Zie [Je accountinstellingen](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)configureren.

Nadat u het belangrijkste Url- ingangspunt hebt gespecificeerd, kunt u extra ingangspunten naar keuze specificeren die u in orde wilt kruipen. Meestal zult u extra ingangspunten voor Web-pagina&#39;s specificeren die niet van pagina&#39;s onder het belangrijkste ingangspunt verbonden zijn. Specificeer extra ingangspunten wanneer uw website meer dan één domein zoals in het volgende voorbeeld overspant:

`https://www.domain.com/`

`https://www.domain.com/not_linked/but_search_me_too/`

`https://more.domain.com/`

U kwalificeert elk ingangspunt met één of meer van de volgende ruimte-gescheiden sleutelwoorden in de lijst hieronder. Deze sleutelwoorden beïnvloeden hoe de pagina wordt geïndexeerd.

**Belangrijk**: Ben zeker dat u een bepaald sleutelwoord van het ingangspunt en van elkaar door een ruimte scheidt; een komma is geen geldige scheidingsteken.

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
   <td colname="col2"> <p> Als u de tekst niet wilt indexeren op de pagina van het ingangspunt, maar u wilt de verbindingen van de pagina volgen, voeg toe 
     <userinput>
       noindex 
     </userinput> na de ingang. </p> <p>Scheid het sleutelwoord van het ingangspunt met een ruimte zoals in het volgende voorbeeld: </p> <p> <code> https://www.my-additional-domain.com/more_pages/main.html&amp;nbsp;noindex </code> </p> <p>Dit sleutelwoord is gelijkwaardig aan een meta-tag robots met 
     <userinput>
       content="noindex" 
     </userinput>) tussen 
     <userinput>
       &lt;head&gt; 
     </userinput>... 
     <userinput>
       &lt;/head&gt; 
     </userinput> tags van de pagina met entrypunten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>onopvolgzaam </p> </td> 
   <td colname="col2"> <p> Als u de tekst in de pagina van het ingangspunt wilt indexeren maar u wilt geen van de verbindingen van om het even welke pagina volgen, voeg toe 
     <userinput>
       onopvolgzaam 
     </userinput> na de ingang. </p> <p>Scheid het sleutelwoord van het ingangspunt met een ruimte zoals in het volgende voorbeeld: </p> <p> <code> https://www.domain.com/not_linked/directory_listing&amp;nbsp;nofollow </code> </p> <p>Dit sleutelwoord is gelijkwaardig aan een meta-tag robots met 
     <userinput>
       content="nofollow" 
     </userinput> tussen 
     <userinput>
       &lt;head&gt; 
     </userinput>... 
     <userinput>
       &lt;/head&gt; 
     </userinput> markering van een pagina van het ingangspunt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>formulier </p> </td> 
   <td colname="col2"> <p> Wanneer het ingangspunt een login pagina is, 
     <userinput>
       formulier 
     </userinput> wordt typisch gebruikt zodat de onderzoeksrobot het login formulier kan voorleggen en de aangewezen koekjes ontvangen alvorens de website te kruipen. Wanneer het "vorm"sleutelwoord wordt gebruikt, wordt de pagina van het ingangspunt niet geïndexeerd en de onderzoeksrobot merkt niet de pagina van het ingangspunt zoals gekropen. Gebruik 
     <userinput>
       onopvolgzaam 
     </userinput> als je niet wilt dat de zoekrobot de links van de pagina volgt. </p> </td> 
  </tr> 
 </tbody> 
</table>

Zie ook [over inhoudstypen](../c-about-settings-menu/c-about-crawling-menu.md#concept_6FEA1355C0374500B4C53090C34A8A07).

Zie ook [over de Schakelaar](../c-about-settings-menu/c-about-crawling-menu.md#concept_CA6921E2FBF641F9B4F60C92B32AFA84)van de Index.

## Het toevoegen van veelvoudige Url- ingangspunten die u geïndexeerd wilt {#task_2338A47387D74CFDAC4D4EF4A367ED45}

Als uw website veelvoudige domeinen of subdomeinen heeft en u wilt hen kruipt, kunt u de Intrinsichters gebruiken URL om meer URLs toe te voegen.

Om het belangrijkste URL-ingangspunt van uw website in te stellen, gebruikt u Accountinstellingen.

Zie [Je accountinstellingen](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)configureren.

**Om veelvoudige URL ingangspunten toe te voegen die u geïndexeerd wilt**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**.
1. Op de [!DNL URL Entrypoints] pagina, op het [!DNL Entrypoints] gebied, ga één adres URL per lijn in.
1. (Facultatief) in de **[!UICONTROL Add Index Connector Configurations]** drop-down lijst, selecteer een indexschakelaar die u als ingangspunt voor het indexeren wilt toevoegen.

   De drop-down lijst is slechts beschikbaar als u eerder één of meerdere definities van de indexschakelaar hebt toegevoegd.

   ![](assets/url_entrypoints_index_connector.png)

   Zie een definitie [van de Schakelaar van de Index](../c-about-settings-menu/c-about-crawling-menu.md#task_96779B651A654E1F871F55D6DBBC8886)toevoegen.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Facultatief) doe om het even welke volgend:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Informatie over URL-maskers {#concept_8039DFC53FF3410AA494D602F71BA164}

De maskers URL zijn patronen die bepalen welke van uw website de indexen van de onderzoeksrobot of niet indexen documenteert.

Zeker ben dat u uw plaatsindex herbouwt zodat de resultaten van uw maskers URL aan uw klanten zichtbaar zijn.

Zie [het Vormen van een stijgende index van een gefaseerde website](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

Het volgende is twee soorten maskers URL die u kunt gebruiken:

* URL-maskers opnemen
* URL-maskers uitsluiten

Omvat Url- maskers vertellen de onderzoeksrobot om het even welke documenten te indexeren die het patroon van het masker aanpassen.

Sluit URL-maskers uit om de zoekrobot te vertellen dat hij passende documenten indexeert.

Aangezien de onderzoeksrobot van verbinding reist om door uw website te verbinden, ontmoet het URLs en zoekt maskers die die URLs aanpassen. De eerste gelijke bepaalt of om die URL van de index te omvatten of uit te sluiten. Als geen masker een ondervonden URL aanpast, wordt die URL verworpen van de index.

Omvat Url- maskers voor uw entrypoint URLs automatisch worden geproduceerd. Dit gedrag zorgt ervoor dat alle ontmoete documenten op uw website worden geïndexeerd. Het schrapt ook gemakkelijk met verbindingen die uw website &quot;verlaten&quot;. Bijvoorbeeld, als een geïndexeerde pagina met https://www.yahoo.com verbindt, indexeert de onderzoeksrobot niet dat URL omdat het niet aanpast omvat masker automatisch dat door entrypoint URL wordt geproduceerd.

Elk masker URL dat u specificeert moet op een afzonderlijke lijn zijn.

Het masker kan om het even welke volgend specificeren:

* Een volledige weg zoals in `https://www.mydomain.com/products.html`.
* Een gedeeltelijke weg zoals in `https://www.mydomain.com/products`.
* Een URL die wilde kaarten zoals in gebruikt `https://www.mydomain.com/*.html`.
* Een regelmatige uitdrukking (voor geavanceerde gebruikers).

   Om een masker een regelmatige uitdrukking te maken, neem het sleutelwoord `regexp` tussen het maskertype ( `exclude` of `include`) en het masker op URL.

Het volgende is eenvoudig sluit URL maskervoorbeeld uit:

```
exclude https://www.mydomain.com/photos
```

Omdat dit voorbeeld een exclusief masker URL is, wordt om het even welk document dat het patroon aanpast niet geïndexeerd. Het patroon past om het even welk ontmoet punt, zowel dossiers als omslagen aan, zodat `https://www.mydomain.com/photos.html` en `https://www.mydomain.com/photos/index.html`, allebei waarvan sluit URL aan, niet worden geïndexeerd. Om slechts dossiers in de `/photos/` omslag aan te passen, moet het masker URL een het slepen schuine streep zoals in het volgende voorbeeld bevatten:

```
exclude https://www.mydomain.com/photos/
```

Het volgende sluit maskervoorbeeld uit gebruikt een wilde kaart. Het vertelt de onderzoeksrobot om dossiers met de &quot;.pdf&quot;uitbreiding over het hoofd te zien. De onderzoeksrobot voegt deze dossiers niet aan uw index toe.

```
exclude *.pdf
```

Eenvoudig omvat masker URL is het volgende:

```
include https://www.mydomain.com/news/
```

Slechts worden de documenten die door als reeks verbindingen van een entrypoint URL worden verbonden, of die als ingang URL zelf worden gebruikt, geïndexeerd. Als u alleen een URL van een document opneemt als een URL-masker, wordt een niet-gekoppeld document niet geïndexeerd. Om losgemaakte documenten aan uw index toe te voegen, kunt u de eigenschap van de Ingangen URL gebruiken.

Zie [over URL Inschrijvingen](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573).

Omvat maskers en sluit maskers uit kunnen samenwerken. U kunt een groot gedeelte van uw website van indexeren uitsluiten door een exclusief masker te creëren URL nog één of meer van die uitgesloten pagina&#39;s met omvatten een masker URL omvatten. Bijvoorbeeld, veronderstel uw entrypoint URL het volgende is:

```
https://www.mydomain.com/photos/
```

De onderzoeksrobot kruipt en indexeert alle pagina&#39;s onder `/photos/summer/`, `/photos/spring/` en `/photos/fall/` (veronderstellend dat er verbindingen aan minstens één pagina in elke folder van de `photos` omslag zijn). Dit gedrag komt voor omdat de verbindingswegen de onderzoeksrobot toelaten om de documenten in te vinden `/summer/`, `/spring/`en, `/fall/`, passen de omslagen en de omslag URLs het omvatten masker aan dat automatisch door entrypoint URL wordt geproduceerd.

U kunt verkiezen om alle pagina&#39;s in de `/fall/` omslag met uit te sluiten een masker URL zoals in het volgende voorbeeld:

```
exclude https://www.mydomain.com/photos/fall/
```

Of, omvat selectief slechts `/photos/fall/redleaves4.html` als deel van de index met het volgende masker URL:

```
include https://www.mydomain.com/photos/fall/redleaves4.html
```

Voor de bovengenoemde twee maskervoorbeelden om te werken zoals bedoeld, omvat masker is vermeld eerst, zoals in het volgende:

```
include https://www.mydomain.com/photos/fall/redleaves4.html 
exclude https://www.mydomain.com/photos/fall/
```

Omdat de onderzoeksrobot aanwijzingen volgt in de volgorde waarin ze worden vermeld, bevat de zoekrobot eerst `/photos/fall/redleaves4.html`en sluit hij de rest van de bestanden in de `/fall` map uit.

Indien de instructies op de tegenovergestelde manier worden gespecificeerd zoals in het volgende:

```
exclude https://www.mydomain.com/photos/fall/ 
include https://www.mydomain.com/photos/fall/redleaves4.html
```

Dan `/photos/fall/redleaves4.html` is niet inbegrepen, alhoewel het masker specificeert dat het inbegrepen is.

Een masker URL dat eerst verschijnt neemt altijd belangrijkheid over een masker URL dat later in de maskermontages verschijnt. Bovendien, als de onderzoeksrobot een pagina ontmoet die aanpast omvat een masker URL en sluit een masker URL uit, neemt het masker dat eerst vermeld is altijd belangrijkheid.

Zie [het Vormen van een stijgende index van een gefaseerde website](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

## Over het gebruiken van trefwoorden met URL-maskers {#section_7609A7A6D79B482ABCA8900886541AAB}

U kunt elk kwalificeren omvat masker met één of meerdere ruimte-gescheiden sleutelwoorden, die beïnvloeden hoe de aangepaste pagina&#39;s worden geïndexeerd.

Een komma is niet geldig als separator tussen het masker en het sleutelwoord; u kunt slechts ruimten gebruiken.

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
   <td colname="col2"> <p> Als u niet de tekst op de pagina's wilt indexeren die het masker URL aanpassen, maar u wilt de aangepaste paginakoppelingen volgen, voeg toe 
     <userinput>
       noindex 
     </userinput> na omvat masker URL. Ben zeker dat u het sleutelwoord van het masker met een ruimte zoals in het volgende voorbeeld scheidt: </p> <p> <code> include&amp;nbsp;*.swf&amp;nbsp;noindex </code> </p> <p>Het bovenstaande voorbeeld geeft aan dat de zoekrobot alle links van bestanden volgt met de 
     <userinput>
       .swf 
     </userinput> de uitbreiding, maar maakt indexering van al tekst onbruikbaar bevat binnen die dossiers. </p> <p>De 
     <userinput>
       noindex 
     </userinput> trefwoord komt overeen met een meta-tag voor robot met 
     <userinput>
       content="noindex" 
     </userinput> tussen 
     <userinput>
       &lt;kop&gt;...&lt;/head&gt; 
     </userinput> tags van overeenkomende pagina's. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>onopvolgzaam </p> </td> 
   <td colname="col2"> <p> Als u de tekst op de pagina's wilt indexeren die het masker URL aanpassen, maar u wilt niet de aangepaste verbindingen van de pagina volgen, voeg toe 
     <userinput>
       onopvolgzaam 
     </userinput> na omvat masker URL. Ben zeker dat u het sleutelwoord van het masker met een ruimte zoals in het volgende voorbeeld scheidt: </p> <p> <code> include&amp;nbsp;https://www.mydomain.com/photos&amp;nbsp;nofollow </code> </p> <p>De 
     <userinput>
       onopvolgzaam 
     </userinput> trefwoord komt overeen met een meta-tag voor robot met 
     <userinput>
       content="nofollow" 
     </userinput> tussen 
     <userinput>
       &lt;kop&gt;...&lt;/head&gt; 
     </userinput> tags van overeenkomende pagina's. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>regexp </p> </td> 
   <td colname="col2"> <p>Gebruikt voor allebei omvat en sluit maskers uit. </p> <p>Om het even welk Url- masker is voorafgegaan met 
     <userinput>
       regexp 
     </userinput> wordt behandeld als een regelmatige uitdrukking. Als de onderzoeksrobot documenten ontmoet die een exclusief regelmatig uitdrukkingsURL masker aanpassen, worden die documenten niet geïndexeerd. Als de onderzoeksrobot documenten ontmoet die aanpassen en het regelmatige uitdrukkingsURL masker omvatten, worden die documenten geïndexeerd. Bijvoorbeeld, veronderstel u het volgende masker URL hebt: </p> <p> <code> exclude&amp;nbsp;regexp&amp;nbsp;^.*/products/.*\.html$ </code> </p> <p>De onderzoeksrobot sluit passende dossiers zoals uit 
     <userinput>
       https://www.mydomain.com/products/page1.html 
     </userinput> </p> <p>Als u het volgende had sluit regelmatige uitdrukkingURL masker uit: </p> <p> <code> exclude&amp;nbsp;regexp&amp;nbsp;^.*\?..*$ </code> </p> <p>De zoekrobot bevat geen URL die een CGI-parameter bevat, zoals 
     <userinput>
       https://www.mydomain.com/cgi/prog/?arg1=val1&amp;arg2=val2 
     </userinput>. </p> <p>Als u het volgende had omvat het regelmatige uitdrukkingsURL masker: </p> <p> <code> include&amp;nbsp;regexp&amp;nbsp;^.*\.swf$&amp;nbsp;noindex </code> </p> <p>De onderzoeksrobot volgt alle verbindingen van dossiers met de ".swf"uitbreiding. De 
     <userinput>
       noindex 
     </userinput> het sleutelwoord specificeert ook dat de tekst van aangepaste dossiers niet geïndexeerd is. </p> <p>Zie <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Regelmatige expressies </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Het toevoegen van maskers URL aan index of niet indexdelen van uw website {#task_E1AFC17C746048B8843013D979E082C1}

U kunt gebruiken [!DNL URL Masks] om te bepalen welke delen van uw website die u wilt of niet gekropen en geïndexeerd wilt.

Gebruik het gebied van de Maskers van de Test URL om te testen of een document of niet inbegrepen na u index is.

Zeker ben dat u uw plaatsindex herbouwt zodat de resultaten van uw maskers URL aan uw klanten zichtbaar zijn.

Zie [het Vormen van een stijgende index van een gefaseerde website](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Om URL maskers aan index of niet indexdelen van uw website toe te voegen of**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Masks]**.
1. (Facultatief) op de [!DNL URL Masks] pagina, op het **[!UICONTROL Test URL Masks]** gebied, ga een testURL masker van uw website in, en klik dan **[!UICONTROL Test]**.
1. Op het [!DNL URL Masks] gebied, type `include` (om een website toe te voegen die u gekropen en geïndexeerd wilt), of type `exclude` (om een website te blokkeren van gekropen en geïndexeerd), die door het URL maskeradres wordt gevolgd.

   Ga één URL maskeradres per lijn in. Voorbeeld:

   ```
   include https://www.mycompany.com/summer 
   include https://www.mycompany.com/spring 
   exclude regexp .*\.xml 
   exclude https://www.mycompany.com/fall
   ```

1. Klik op **[!UICONTROL Save Changes]**.
1. (Facultatief) doe om het even welke volgend:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Informatie over datummaskers {#concept_F4F1F58A646F4A86B8650EC46FDCEF66}

U kunt de Maskers van de Datum gebruiken om dossiers van uw onderzoeksresultaten te omvatten of uit te sluiten die op de leeftijd van het dossier worden gebaseerd.

Zeker ben dat u uw plaatsindex herbouwt zodat de resultaten van uw maskers URL aan uw klanten zichtbaar zijn.

Zie [het Vormen van een stijgende index van een gefaseerde website](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

Het volgende is twee soorten datummaskers die u kunt gebruiken:

* Datummaskers opnemen (&quot;include-days&quot; en &quot;include-date&quot;)

   Omvat de dossiers van de datummaskers die op of vóór de gespecificeerde datum worden gedateerd.
* Datummaskers uitsluiten (&quot;niet-dagen&quot; en &quot;niet-datum&quot;)

   Sluit de dossiers van de datummaskers uit die op of vóór de gespecificeerde datum worden gedateerd.

Door gebrek, wordt de dossierdatum bepaald van meta markeringsinformatie. Als geen markering van Meta wordt gevonden, wordt de datum van een dossier bepaald van de HTTP- kopbal die van de server wordt ontvangen wanneer de onderzoeksrobot een dossier downloadt.

Elk datummasker dat u specificeert moet op een afzonderlijke lijn zijn.

Het masker kan om het even welke volgend specificeren:

* Een volledige weg zoals in `https://www.mydomain.com/products.html`
* Een gedeeltelijke weg zoals in `https://www.mydomain.com/products`
* Een URL die wilde kaarten gebruikt `https://www.mydomain.com/*.html`
* Een reguliere expressie. Om een masker een regelmatige uitdrukking te maken, neem het sleutelwoord `regexp` vóór URL op.

Beide omvatten en sluiten datummaskers uit kunnen een datum in één van de twee volgende manieren specificeren. De maskers worden slechts toegepast als de overeenkomende dossiers op of vóór de gespecificeerde datum werden gecreeerd:

1. Een aantal dagen. Bijvoorbeeld, veronderstel uw datummasker het volgende is:

   ```
   exclude-days 30 https://www.mydomain.com/docs/archive/)
   ```

   Het aantal opgegeven dagen wordt teruggeteld. Als het dossier op of vóór aangekomen op datum wordt gedateerd, wordt het masker toegepast.

1. Een daadwerkelijke datum die het formaat YYYY-MM-DD gebruikt. Bijvoorbeeld, veronderstel uw datummasker het volgende is:

   ```
   include-date 2011-02-15 https://www.mydomain.com/docs/archive/)
   ```

   Als het aangepaste document op of vóór de gespecificeerde datum wordt gedateerd, wordt het datummasker toegepast.

Het volgende is een eenvoudig sluit datummasker voorbeeld uit:

```
exclude-days 90 https://www.mydomain.com/docs/archive
```

Omdat dit een exclusief datummasker is, wordt om het even welk dossier dat het patroon aanpast niet geïndexeerd en is 90 dagen oud of ouder. Wanneer u een document uitsluit, wordt geen tekst geïndexeerd en geen verbindingen worden gevolgd van dat dossier. Het dossier wordt effectief genegeerd. In dit voorbeeld, zowel zouden de dossiers als de omslagen het gespecificeerde patroon URL kunnen aanpassen. Bericht dat zowel `https://www.mydomain.com/docs/archive.html` als het patroon `https://www.mydomain.com/docs/archive/index.html` aanpassen en niet geïndexeerd zijn als zij 90 dagen oud of ouder zijn. Om slechts dossiers in de `/docs/archive/` omslag aan te passen, moet het datummasker een het slepen schuine streep zoals in het volgende bevatten:

```
exclude-days 90 https://www.mydomain.com/docs/archive/
```

De maskers van de datum kunnen ook met wilde kaarten worden gebruikt. Het volgende sluit masker uit vertelt de onderzoeksrobot om dossiers met de &quot;.pdf&quot;uitbreiding over het hoofd te zien die op of vóór 2011-02-15 gedateerd zijn. De onderzoeksrobot voegt geen gelijke dossiers aan uw index toe.

```
exclude-date 2011-02-15 *.pdf
```

Omvat datummasker kijkt gelijkaardig, slechts worden de aangepaste dossiers toegevoegd aan de index. Het volgende omvat voorbeeld van het datummasker vertelt de onderzoeksrobot om de tekst van om het even welke dossiers te indexeren die nul dagen oud of ouder op het `/docs/archive/manual/` gebied van de website zijn.

```
include-days 0 https://www.mydomain.com/docs/archive/manual/
```

Omvat maskers en sluit maskers uit kunnen samenwerken. Bijvoorbeeld, kunt u een groot gedeelte van uw website van het indexeren uitsluiten door een exclusief datummasker te creëren nog één of meer van die uitgesloten pagina&#39;s met omvatten een masker URL omvatten. Als uw ingang URL het volgende is:

```
https://www.mydomain.com/archive/
```

De onderzoeksrobot kruipt en indexeert alle pagina&#39;s onder `/archive/summer/`, `/archive/spring/`en `/archive/fall/` (veronderstellend dat er verbindingen aan minstens één pagina in elke omslag van de `archive` omslag zijn). Dit gedrag komt voor omdat de verbindingswegen de onderzoeksrobot toelaten om de dossiers in de `/summer/`, `/spring/`, en de `/fall/` omslagen en omslag URLs &quot;te vinden&quot;aanpassen omvat masker automatisch dat door entrypoint URL wordt geproduceerd.

Zie [over URL Inschrijvingen](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573).

Zie [Je accountinstellingen](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)configureren.

U kunt verkiezen om alle pagina&#39;s uit te sluiten over 90 oud in de `/fall/` omslag met een exclusief datummasker zoals in het volgende:

```
exclude-days 90 https://www.mydomain.com/archive/fall/
```

U kunt selectief slechts omvatten `/archive/fall/index.html` (ongeacht hoe oud het is-om het even welk dossier 0 dagen of ouder) als deel van de index met het volgende datummasker wordt aangepast:

```
include-days 0 https://www.mydomain.com/archive/fall/index.html
```

Voor de bovengenoemde twee maskervoorbeelden om te werken zoals bedoeld, moet u van omvatten eerst masker zoals in het volgende een lijst maken:

```
include-days 0 https://www.mydomain.com/archive/fall/index.html 
exclude-days 90 https://www.mydomain.com/archive/fall/
```

Omdat de zoekrobot aanwijzingen volgt in de volgorde waarin ze zijn opgegeven, bevat de zoekrobot eerst de overige bestanden in de `/archive/fall/index.html`map `/fall` en sluit hij de overige bestanden uit.

Indien de instructies op de tegenovergestelde manier worden gespecificeerd zoals in het volgende:

```
exclude-days 90 https://www.mydomain.com/archive/fall/ 
include-days 0 https://www.mydomain.com/archive/fall/index.html 
```

Dan `/archive/fall/index.html` is niet inbegrepen, alhoewel het masker specificeert dat het zou moeten zijn. Een datummasker dat eerst verschijnt neemt altijd belangrijkheid over een datummasker dat later in de maskermontages zou kunnen verschijnen. Bovendien, als de onderzoeksrobot een pagina ontmoet die zowel aanpast omvat datummasker en sluit datummasker uit, neemt het masker dat eerst vermeld is altijd belangrijkheid.

Zie [het Vormen van een stijgende index van een gefaseerde website](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

## Over het gebruiken van trefwoorden met datummaskers {#section_CCBB3E3FDBDE4725B2B571FD6594470C}

U kunt elk kwalificeren omvat masker met één of meerdere ruimte-gescheiden sleutelwoorden, die beïnvloeden hoe de aangepaste pagina&#39;s worden geïndexeerd.

Een komma is niet geldig als separator tussen het masker en het sleutelwoord; u kunt slechts ruimten gebruiken.

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
   <td colname="col2"> <p> Als u niet de tekst op de pagina's wilt indexeren die op of vóór de datum gedateerd zijn die door wordt gespecificeerd omvat masker, voeg toe 
     <userinput>
       noindex 
     </userinput> na omvat datummasker zoals in het volgende: </p> <p> <code> include-days&amp;nbsp;10&amp;nbsp;*.swf&amp;nbsp;noindex </code> </p> <p>Zeker ben u scheidt het sleutelwoord van het masker met een ruimte. </p> <p>Het bovenstaande voorbeeld geeft aan dat de zoekrobot alle links volgt uit bestanden met de extensie ".swf" die 10 dagen oud of ouder zijn. Nochtans, maakt het indexeren van al tekst in die dossiers onbruikbaar. </p> <p>U kunt willen ervoor zorgen dat de tekst voor oudere dossiers niet wordt geïndexeerd maar nog alle verbindingen van die dossiers volgt. In dergelijke gevallen, omvat het gebruik datummasker met het "noindex"sleutelwoord in plaats van het gebruiken van een exclusief datummasker. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>onopvolgzaam </p> </td> 
   <td colname="col2"> <p> Als u de tekst op de pagina's wilt indexeren die op of vóór de datum gedateerd zijn die door wordt gespecificeerd omvat masker, maar u wilt niet de aangepaste verbindingen van de pagina volgen, voeg toe 
     <userinput>
       onopvolgzaam 
     </userinput> na omvat datummasker zoals in het volgende: </p> <p> <code> include-days&amp;nbsp;8&amp;nbsp;https://www.mydomain.com/photos&amp;nbsp;nofollow </code> </p> <p>Zeker ben u scheidt het sleutelwoord van het masker met een ruimte. </p> <p>De 
     <userinput>
       onopvolgzaam 
     </userinput> trefwoord komt overeen met een meta-tag voor robot met 
     <userinput>
       content="nofollow" 
     </userinput> tussen 
     <userinput>
       &lt;kop&gt;...&lt;/head&gt; 
     </userinput> tag van overeenkomende pagina's. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>serverdatum </p> </td> 
   <td colname="col2"> <p>Gebruikt voor allebei omvat en sluit maskers uit. </p> <p>De onderzoeksrobot downloadt en ontleedt over het algemeen elk dossier alvorens de datummaskers te controleren. Dit gedrag komt voor omdat sommige dossiertypes een datum binnen het dossier zelf kunnen specificeren. Bijvoorbeeld, kan een HTML- document meta- markeringen omvatten die de datum van het dossier plaatsen. </p> <p>Als u vele dossiers gaat uitsluiten die op hun datum worden gebaseerd, en u wilt geen onnodige lading op uw servers zetten, kunt u gebruiken 
     <userinput>
       serverdatum 
     </userinput> na URL in het datummasker. </p> <p>Dit sleutelwoord instrueert de onderzoeksrobot om op de datum van het dossier te vertrouwen dat door uw server in plaats van het ontleden van elk dossier is teruggekeerd. Bijvoorbeeld, sluit het volgende datummasker pagina's uit die URL aanpassen als de documenten 90 dagen of ouder zijn, volgens de datum die door de server in de kopballen van HTTP is teruggekeerd: </p> <p> <code> exclude-days&amp;nbsp;90&amp;nbsp;https://www.mydomain.com/docs/archive&amp;nbsp;server-date </code> </p> <p> Als de datum die door de server is teruggekeerd 90 dagen of meer verleden is, 
     <userinput>
       serverdatum 
     </userinput> specificeert dat de uitgesloten documenten niet van uw server worden gedownload. Het resultaat betekent snellere het indexeren tijd voor uw documenten en een verminderde lading die op uw servers wordt geplaatst. Indien 
     <userinput>
       serverdatum 
     </userinput> niet wordt gespecificeerd, negeert de onderzoeksrobot de datum die door de server in de kopballen van HTTP is teruggekeerd. In plaats daarvan, wordt elk dossier gedownload en gecontroleerd om te zien of wordt de datum gespecificeerd. Als geen datum in het dossier wordt gespecificeerd, dan gebruikt de onderzoeksrobot de datum die door de server is teruggekeerd. </p> <p>U mag niet gebruiken 
     <userinput>
       serverdatum 
     </userinput> als uw dossiers bevelen bevatten die de serverdatum met voeten treden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>regexp </p> </td> 
   <td colname="col2"> <p> Het gebruik voor allebei omvat en sluit maskers uit. </p> <p>Om het even welk datummasker dat door wordt voorafgegaan 
     <userinput>
       regexp 
     </userinput> wordt behandeld als een regelmatige uitdrukking. </p> <p>Als de onderzoeksrobot dossiers ontmoet die aanpassen sluit het regelmatige masker van de uitdrukkingsdatum uit, indexeert het niet die dossiers. </p> <p>Als de onderzoeksrobot dossiers ontmoet die aanpassen en het regelmatige masker van de uitdrukkingsdatum omvatten, indexeert het die documenten. </p> <p>Bijvoorbeeld, veronderstel u het volgende datummasker hebt: </p> <p> <code> exclude-days&amp;nbsp;180&amp;nbsp;regexp&amp;nbsp;.*archive.* </code> </p> <p>Het masker vertelt de onderzoeksrobot om passende dossiers uit te sluiten die 180 dagen of ouder zijn. Namelijk dossiers die het woord "archief"in hun URL bevatten. </p> <p>Zie <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Regelmatige expressies </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Het toevoegen van datummaskers aan index of niet indexdelen van uw website {#task_0010543C55F648D2B5DEFEFAD60FAF04}

U kunt de Maskers van de Datum gebruiken om dossiers van de resultaten van het klantenonderzoek te omvatten of uit te sluiten die op de leeftijd van de dossiers worden gebaseerd.

Gebruik de **[!UICONTROL Test Date]** en **[!UICONTROL Test URL]** gebieden om te testen of een dossier of niet inbegrepen na u index is.

Zeker ben dat u uw plaatsindex herbouwt zodat de resultaten van uw maskers URL aan uw klanten zichtbaar zijn.

Zie [het Vormen van een stijgende index van een gefaseerde website](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Om datummaskers aan indexof geen indexdelen van uw website toe te voegen**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Date Masks]**.
1. (Facultatief) op de [!DNL Date Masks] pagina, op het **[!UICONTROL Test Date]** gebied, ga een datum in die als JJJJ-MM-DD (bijvoorbeeld, `2011-07-25`) wordt geformatteerd; op het **[!UICONTROL Test URL]** gebied, ga een masker URL van uw website in, en klik dan **[!UICONTROL Test]**.
1. Op het [!DNL Date Masks] gebied, ga één adres van het datummasker per lijn in.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Facultatief) doe om het even welke volgend:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Over Wachtwoorden {#concept_3EDBD731725D46B891F834D4472774DC}

Om tot gedeelten van uw website toegang te hebben die met de BasisAuthentificatie van HTTP worden beschermd, kunt u één of meerdere wachtwoorden toevoegen.

Alvorens de gevolgen van de montages van het Wachtwoord aan klanten zichtbaar zijn, moet u uw plaatsindex herbouwen.

Zie [het Vormen van een stijgende index van een gefaseerde website](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

Voor de [!DNL Passwords] pagina, typt u elk wachtwoord op één enkele lijn. Het wachtwoord bestaat uit een URL of een domein, een gebruikersnaam, en een wachtwoord, zoals in het volgende voorbeeld:

```
https://www.mydomain.com/ myname mypassword
```

In plaats van het gebruiken van een weg URL, zoals hierboven, kon u een rijk ook specificeren.

Om het correcte te gebruiken domein te bepalen, open een wachtwoord-beschermde Web-pagina met browser en bekijk het de dialoogvakje van het Wachtwoord van het Netwerk &quot;ingaan&quot;.

![](assets/realms.gif)

De naam van het rijk, in dit geval, is &quot;Mijn Realm van de Plaats.&quot;

Gebruikend de gebiedsnaam hierboven, zou uw wachtwoord als het volgende kunnen kijken:

```
My Site Realm myusername mypassword
```

Als uw website veelvoudige gebieden heeft, kunt u veelvoudige wachtwoorden tot stand brengen door een gebruikersnaam en wachtwoord voor elk gebied op een afzonderlijke lijn zoals in het volgende voorbeeld in te gaan:

```
Realm1 name1 password1 
Realm2 name2 password2 
Realm3 name3 password3
```

U kunt wachtwoorden mengen die URLs of gebieden bevatten zodat uw wachtwoordlijst als het volgende zou kunnen kijken:

```
Realm1 name1 password1 
https://www.mysite.com/path1/path2 name2 password2 
Realm3 name3 password3 
Realm4 name4 password4 
https://www.mysite.com/path1/path5 name5 password5 
https://www.mysite.com/path6 name6 password6
```

In de lijst hierboven, wordt het eerste wachtwoord gebruikt dat een gebied of een URL bevat dat de de authentificatieverzoek van de server aanpast. Zelfs als het dossier bij `https://www.mysite.com/path1/path2/index.html` binnen is, `Realm3`bijvoorbeeld, `name2` en `password2` wordt gebruikt omdat het wachtwoord dat met URL wordt bepaald boven wordt vermeld die met het rijk wordt bepaald.

## Het toevoegen van wachtwoorden voor de toegang tot van gebieden van uw website die authentificatie vereisen {#task_DED19D476FF04B48BB6456D5ECB8628A}

U kunt Wachtwoorden gebruiken om tot wachtwoord-beschermde gebieden van uw website voor kruipende en indexerende doeleinden toegang te hebben.

Alvorens de gevolgen van uw wachtwoord toevoegingen zijn zichtbaar aan klanten, ben zeker u herbouwt uw plaatsindex

Zie [het Vormen van een stijgende index van een gefaseerde website](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Om wachtwoorden voor de toegang tot van gebieden van uw website toe te voegen die authentificatie vereisen**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Passwords]**.
1. Voor de [!DNL Passwords] pagina, op het **[!UICONTROL Passwords]** gebied, ga een gebied of een URL, en zijn bijbehorende gebruikersnaam, en wachtwoord in, dat door een ruimte wordt gescheiden.

   Voorbeeld van een rijk wachtwoord en een wachtwoord URL op afzonderlijke lijnen:

   ```
   Realm1 name1 password1 
   https://www.mysite.com/path1/path2 name2 password2
   ```

   Voeg slechts één wachtwoord per lijn toe.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Facultatief) doe om het even welke volgend:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Over inhoudstypen {#concept_6FEA1355C0374500B4C53090C34A8A07}

U kunt gebruiken [!DNL Content Types] om te selecteren welke types van dossiers die u wilt kruipen en indexeren voor deze rekening.

De types van inhoud die u kunt verkiezen om te kruipen en te indexeren omvatten Pdf- documenten, tekstdocumenten, de films van de Flits van Adobe, dossiers van de toepassingen van Microsoft Office zoals Word, Excel, en Powerpoint, en tekst in MP3 dossiers. De tekst die binnen de geselecteerde inhoudstypes wordt gevonden wordt gezocht samen met alle andere tekst op uw website.

Alvorens de gevolgen van de montages van de Types van Inhoud aan klanten zichtbaar zijn, moet u uw plaatsindex herbouwen.

Zie [het Vormen van een stijgende index van een gefaseerde website](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

## Over het indexeren van MP3-muziekbestanden {#section_AD2E28BEEE3E46629E2B05C34A963673}

Als u de optie **[!UICONTROL Text in MP3 Music Files]** op de [!DNL Content Types] pagina selecteert, wordt een MP3 dossier gekropen en in één van twee manieren geïndexeerd. De eerste en gemeenschappelijkste manier is van een href van het anker markering in een HTML- dossier zoals in het volgende:

```
<a href="MP3-file-URL"></a>
```

De tweede manier is URL van het MP3 dossier als ingang in te gaan URL.

Zie [over URL Inschrijvingen](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573).

Een MP3-bestand wordt herkend door het MIME-type &quot;audio/mpeg&quot;.

Me ervan bewust ben dat MP3 de grootte van het muziekdossier vrij groot kan zijn, alhoewel zij gewoonlijk slechts een kleine hoeveelheid tekst bevatten. Bijvoorbeeld, kunnen de MP3 dossiers naar keuze zulke dingen opslaan zoals de albumnaam, de kunstenaarsnaam, de liedtitel, het liedgenre, het jaar van versie, en een commentaar. Deze informatie wordt opgeslagen op het allerlaatste eind van het dossier in wat wordt genoemd TAG. MP3 de dossiers die de informatie bevatten van de TAG worden geïndexeerd op de volgende manier:

* De titel van het lied wordt behandeld als de titel van een HTML- pagina.
* De commentaar wordt behandeld als een beschrijving die voor een HTML- pagina wordt bepaald.
* Het genre wordt behandeld als een sleutelwoord dat voor een HTML- pagina wordt bepaald.
* De kunstenaarsnaam, de albumnaam, en het jaar van versie worden behandeld als het lichaam van een HTML- pagina.

Merk op dat elk MP3 dossier dat is gekropen en op uw website wordt geïndexeerd als één pagina telt.

Als uw website vele grote MP3 dossiers bevat, kunt u de het indexeren bytegrens voor uw rekening overschrijden. Als dit gebeurt, kunt u **[!UICONTROL Text in MP3 Music Files]** op de [!DNL Content Types] pagina schrappen om het indexeren van alle MP3 dossiers op uw website te verhinderen.

Als u slechts het indexeren van bepaalde MP3 dossiers op uw website wilt verhinderen, kunt u één van het volgende doen:

* Omring de ankermarkeringen die met de MP3 dossiers met `<nofollow>` en `</nofollow>` markeringen verbinden. De zoekrobot volgt geen links tussen die tags.

* Voeg URLs van de MP3 dossiers als exclusief maskers toe.

   Zie [over Maskers](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164)URL.

## Het selecteren van inhoudstypes om te kruipen en index {#task_CCAC5C67C8BF4AB7B79D34A1495D5EE8}

U kunt gebruiken [!DNL Content Types] om te selecteren welke types van dossiers die u wilt kruipen en indexeren voor deze rekening.

De types van inhoud die u kunt verkiezen om te kruipen en te indexeren omvatten Pdf- documenten, tekstdocumenten, de films van de Flits van Adobe, dossiers van de toepassingen van Microsoft Office zoals Word, Excel, en Powerpoint, en tekst in MP3 dossiers. De tekst die binnen de geselecteerde inhoudstypes wordt gevonden wordt gezocht samen met alle andere tekst op uw website.

Alvorens de gevolgen van de montages van de Types van Inhoud aan klanten zichtbaar zijn, moet u uw plaatsindex herbouwen.

Zie [het Vormen van een stijgende index van een gefaseerde website](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

Om te kruipen en de Chinese, Japanse, of Koreaanse MP3 dossiers te indexeren, voltooi de hieronder stappen. Dan, in **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Injections]**, specificeer de karakterreeks die wordt gebruikt om de MP3 dossiers te coderen.

Zie [over injecties](../c-about-settings-menu/c-about-metadata-menu.md#concept_DA091920671948A0A893A26B3A2FAAE5).

**Om inhoudstypes te selecteren om te kruipen en te indexeren**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**.
1. Voor de [!DNL Content Types] pagina, controleer de dossiertypes die u wilt kruipen en op uw website indexeren.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Facultatief) doe om het even welke volgend:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Informatie over verbindingen {#concept_E2F3B7E7521147479E5948A94BB3A40B}

U kunt Verbindingen gebruiken om tot tien verbindingen van HTTP toe te voegen die de onderzoeksrobot gebruikt om uw website te indexeren.

Het verhogen van het aantal verbindingen kan de hoeveelheid tijd beduidend verminderen dat het neemt om te voltooien kruipt en index. Nochtans, ben zich ervan bewust dat elke extra verbinding de lading op uw server verhoogt.

## Het toevoegen van verbindingen om het indexeren snelheid te verhogen {#task_3E9B83E43C1842A19066355A15C4A6FB}

U kunt de hoeveelheid tijd verminderen het neemt om uw website te indexeren door Verbindingen te gebruiken om het aantal gelijktijdige verbindingen van HTTP te verhogen die kruippakje gebruikt. U kunt tot tien verbindingen toevoegen.

Me ervan bewust ben dat elke extra verbinding de lading verhoogt die op uw server wordt geplaatst.

**Om verbindingen toe te voegen om het indexeren snelheid te verhogen**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Connections]**.
1. Op de [!DNL Parallel Indexing Connections] pagina, op het **[!UICONTROL Number of Connections]** gebied, ga het aantal verbindingen (1-10) in die u wilt toevoegen.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Facultatief) doe om het even welke volgend:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Informatie over formulierindiening {#concept_CADD5D7CF373497DAA6F8564D7BC8502}

U kunt de Voorlegging van de Vorm gebruiken om u te helpen vormen op uw website herkennen en verwerken.

Tijdens het kruipen en het indexeren van uw website, wordt elk ontmoet formulier vergeleken met de vormdefinities die u hebt toegevoegd. Als een vorm een vormdefinitie aanpast, wordt de vorm voorgelegd voor het indexeren. Als een vorm meer dan één definitie aanpast, wordt de vorm voorgelegd eens voor elke gematchte definitie.

## Formulierdefinities toevoegen voor het indexeren van formulieren op uw website {#task_62FBCE9E6DBE4BDA8D1249233ADFC00F}

U kunt gebruiken [!DNL Form Submission] om procesvormen te helpen die op uw website voor het indexeren doeleinden worden erkend.

Zeker ben dat u uw plaatsindex herbouwt zodat de resultaten van uw veranderingen aan uw klanten zichtbaar zijn.

Zie [het Vormen van een stijgende index van een gefaseerde website](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Om vormdefinities voor het indexeren van vormen op uw website toe te voegen**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Form Submission]**.
1. Voor de [!DNL Form Submission] pagina, klik **[!UICONTROL Add New Form]**.
1. Voor de [!DNL Add Form Definition] pagina, plaats de [!DNL Form Recognition] en de [!DNL Form Submission] opties.

   De vijf opties in de [!DNL Form Recognition] sectie op de [!DNL Form Definition] pagina worden gebruikt om vormen in uw Web-pagina&#39;s te identificeren die proces kunnen zijn.

   De drie opties in de [!DNL Form Submission] sectie worden gebruikt om de parameters en de waarden te specificeren die met een vorm aan uw Webserver worden voorgelegd.

   Voer per regel één herkenning- of indieningsparameter in. Elke parameter moet een naam en een waarde omvatten.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Optie </p> </th> 
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
      <td colname="col2"> <p>Identificeer de Web-pagina of de pagina's die de vorm bevatten. Om een vorm te identificeren die op één enkele pagina verschijnt, ga URL voor die pagina zoals in het volgende voorbeeld in: </p> <p> <code> https://www.mydomain.com/login.html </code> </p> <p>Om vormen te identificeren die op veelvoudige pagina's verschijnen, specificeer een masker URL dat vervangingen gebruikt om de pagina's te beschrijven. Om vormen te identificeren die op om het even welke pagina van het ASPIS onder worden ontmoet, bijvoorbeeld, zou u het volgende specificeren: <code> https://www.mydomain.com/register/ </code> </p> <p> <code> https://www.mydomain.com/register/*.asp&amp;nbsp; </code> </p> <p>U kunt een regelmatige uitdrukking ook gebruiken om veelvoudige pagina's te identificeren. Specificeer enkel 
      <userinput>
        regexp 
      </userinput> sleutelwoord vóór het masker URL zoals in het volgende voorbeeld: </p> <p> <code> regexp&amp;nbsp;^https://www\.mydomain\.com/.*/login\.html$ </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>URL-masker voor actie </p> </td> 
      <td colname="col2"> <p>Identificeert de actiekenmerken van 
      <userinput>
        &lt;formulier&gt; 
      </userinput> -tag. </p> <p>Als het paginaURL masker, kan het actieURL masker de vorm van één enkele URL, een URL met vervangingen, of een regelmatige uitdrukking nemen. </p> <p>Het masker URL kan om het even welke volgend zijn: 
      <ul id="ul_EDFE7688D3DD4C0BBACCE5D4648D8E44"> 
      <li id="li_77550A448D954EF29FF33EE5E8B5E0F5"> Een volledige weg zoals in het volgende: <code> https://www.mydomain.com/products.html </code> </li> 
      <li id="li_F84E25553BBA41419BE153DC0709E011"> Een gedeeltelijke weg zoals in het volgende: <code> https://www.mydomain.com/products </code> </li> 
      <li id="li_8DADA1C8604740FCACBA30B4AAADB2A1"> Een URL die wilde kaarten zoals in het volgende gebruikt: <code> https://www.mydomain.com/*.html </code> </li> 
      <li id="li_1EF637B450654B509AA4B618F7FD3C2B"> Een regelmatige uitdrukking zoals in het volgende: <code> regexp&amp;nbsp^https://www\.mydomain\.com/.*/login\.html$ </code> </li> 
      </ul> </p> <p>Als u niet de tekst op pagina's wilt indexeren die door een masker URL of door een actieURL masker worden geïdentificeerd, of als u geen verbindingen wilt die op die pagina's worden gevolgd, kunt u gebruiken 
      <userinput>
        noindex 
      </userinput> en 
      <userinput>
        onopvolgzaam 
      </userinput> trefwoorden. U kunt deze sleutelwoorden aan uw maskers toevoegen gebruikend maskers URL of ingangen. </p> <p>Zie <a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573" type="concept" format="dita" scope="local"> over URL Inschrijvingen </a>. </p> <p>Zie <a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164" type="concept" format="dita" scope="local"> over Maskers URL </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Formuliernaammasker </p> </td> 
      <td colname="col2"> <p>Identificeert vormen als 
      <userinput>
        &lt;formulier&gt; 
      </userinput> de markeringen in uw Web-pagina's bevatten een naamattribuut. </p> <p>Je kunt een eenvoudige naam gebruiken ( 
      <userinput>
        login_form 
      </userinput>), een naam met een vervanging ( 
      <userinput>
        formulier* 
      </userinput>), of een reguliere expressie ( 
      <userinput>
        regexp ^.*autoriseren.*$ 
      </userinput>). </p> <p>U kunt dit gebied gewoonlijk leeg verlaten omdat de vormen typisch geen naamattributen hebben. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ID-masker formulier </p> </td> 
      <td colname="col2"> <p>Identificeert vormen als 
      <userinput>
        &lt;formulier&gt; 
      </userinput> de markeringen in uw Web-pagina's bevatten een identiteitskaart attribuut. </p> <p>Je kunt een eenvoudige naam gebruiken ( 
      <userinput>
        login_form 
      </userinput>), een naam met een vervanging ( 
      <userinput>
        formulier* 
      </userinput>), of een reguliere expressie ( 
      <userinput>
        regexp ^.*autoriseren.*$ 
      </userinput>). </p> <p>U kunt dit gebied gewoonlijk leeg verlaten omdat de vormen typisch geen naamattributen hebben. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parameters </p> </td> 
      <td colname="col2"> <p>Identificeer vormen die, of bevatten niet, een genoemde parameter of een genoemde parameter met een specifieke waarde bevatten. </p> <p>Bijvoorbeeld, om een vorm te identificeren die een e-mailparameter bevat die aan rick_brough@mydomain.com, een wachtwoordparameter vooraf in wordt gesteld, maar niet een voornaam parameter, zou u de volgende parametermontages, per lijn specificeren: </p> <p> <code> email=rick_brough@mydomain.com password  not&nbsp;first-name </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>Formulierindiening</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Actie-URL overschrijven </p> </td> 
      <td colname="col2"> <p>Specificeer wanneer het doel van de vormvoorlegging verschillend is van wat in de de actiekenattributen van de vorm wordt gespecificeerd. </p> <p>Bijvoorbeeld, zou u deze optie kunnen gebruiken wanneer de vorm als functie JavaScript wordt voorgelegd die een waarde construeert URL die van wat in de vorm verschillend is wordt gevonden. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Methode voor overschrijven </p> </td> 
      <td colname="col2"> <p>Specificeer wanneer het doel van de vormvoorlegging van verschillend is van wat in de de actieattributen van de vorm wordt gebruikt en wanneer het voorleggen JavaScript de methode heeft veranderd. </p> <p>De standaardwaarden voor alle vormparameters ( 
      <userinput>
        &lt;invoer&gt; 
      </userinput> tags, inclusief verborgen velden), de standaard 
      <userinput>
        &lt;option&gt; 
      </userinput> van een 
      <userinput>
        &lt;selecteer&gt; 
      </userinput> markering, en de standaardtekst tussen 
      <userinput>
        &lt;textarea&gt;...&lt;/textarea&gt; 
      </userinput> tags) worden gelezen van de webpagina. Nochtans, wordt om het even welke parameter die in de <span class="wintitle"> sectie van de Voorlegging van de Vorm, op het gebied van </span> Parameters <span class="uicontrol"> </span> vermeld is, vervangen met de vormgebreken. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parameters </p> </td> 
      <td colname="col2"> <p>U kunt de parameters van de vormvoorlegging met vooraf bepalen 
      <userinput>
        niet 
      </userinput> sleutelwoord. </p> <p>Wanneer u een parameter voorstelt met 
      <userinput>
        niet 
      </userinput>, wordt het niet ingediend als onderdeel van de indiening van het formulier. Dit gedrag is nuttig voor controledozen die zouden moeten worden voorgelegd geschrapt. </p> <p>Bijvoorbeeld, veronderstel u de volgende parameters wilt voorleggen: </p> <p> 
      <ul id="ul_962D12BACF464FF189DB12BFAFCC93A6"> 
      <li id="li_830C6C3EC8D2448388A453BB8EDE5940"> De e-mailparameter met de waarde 
      <userinput>
        nobody@mydomain.com 
      </userinput> </li> 
      <li id="li_905497E3FACE472DBDD49392D5B45E01"> De wachtwoordparameter met de waarde 
      <userinput>
        uitproberen 
      </userinput> </li> 
      <li id="li_AAA411708ADC464793EADF0D821E282E"> De mycheckbox parameter zoals geschrapt. </li> 
      <li id="li_0D3DDE641E2B4BEF9F570C03FDB40ED2"> <p>Alle andere 
      <userinput>
        &lt;formulier&gt; 
      </userinput> parameters als hun standaardwaarden </p> </li> 
      </ul> </p> <p>Uw parameter van de vormvoorlegging zou als het volgende kijken: </p> <p> <code> email=nobody@mydomain.com 
        password=tryme 
        not&nbsp;mycheckbox </code> </p> <p>Het methodeattribuut van 
      <userinput>
        &lt;formulier&gt; 
      </userinput> de markering op de Web-pagina wordt gebruikt om te beslissen of wordt het gegeven verzonden naar uw server gebruikend de GET methode of de POST methode. </p> <p>Indien de 
      <userinput>
        &lt;formulier&gt; 
      </userinput> de markering bevat geen methodeattribuut, wordt de vorm voorgelegd gebruikend de GET methode. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Klik op **[!UICONTROL Add]**.
1. (Facultatief) doe om het even welke volgend:

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een formulierdefinitie bewerken {#task_9FB34E9C8A814DFE9BF7F8F8F69BF314}

U kunt een bestaande vormdefinitie uitgeven als een vorm op uw website is veranderd of als u enkel de definitie moet veranderen.

Me ervan bewust ben dat er geen [!DNL History] eigenschap op de [!DNL Form Submission] pagina is om het even welke veranderingen om te keren die u aan een vormdefinitie aanbrengt.

Zeker ben dat u uw plaatsindex herbouwt zodat de resultaten van uw veranderingen aan uw klanten zichtbaar zijn.

Zie [het Vormen van een stijgende index van een gefaseerde website](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Om een vormdefinitie uit te geven**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Form Submission]**.
1. Voor de [!DNL Form Submission] pagina, klik **[!UICONTROL Edit]** rechts van een vormdefinitie die u wilt bijwerken.
1. Voor de [!DNL Edit Form Definition] pagina, plaats de [!DNL Form Recognition] en de [!DNL Form Submission] opties.

   Zie de lijst van opties onder het [Toevoegen van vormdefinities voor het indexeren van vormen op uw website](../c-about-settings-menu/c-about-crawling-menu.md#task_62FBCE9E6DBE4BDA8D1249233ADFC00F).
1. Klik op **[!UICONTROL Save Changes]**.
1. (Facultatief) doe om het even welke volgend:

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een formulierdefinitie verwijderen {#task_C350FC0CDE344F2786215D544C048B5E}

U kunt een bestaande vormdefinitie schrappen als de vorm niet meer op uw website bestaat, of als u niet meer een bepaalde vorm wilt verwerken en indexeren.

Me ervan bewust ben dat er geen [!DNL History] eigenschap op de [!DNL Form Submission] pagina is om het even welke veranderingen om te keren die u aan een vormdefinitie aanbrengt.

Zeker ben dat u uw plaatsindex herbouwt zodat de resultaten van uw veranderingen aan uw klanten zichtbaar zijn.

Zie [het Vormen van een stijgende index van een gefaseerde website](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Om een vormdefinitie te schrappen**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Form Submission]**.
1. Voor de [!DNL Form Submission] pagina, klik **[!UICONTROL Delete]** rechts van een vormdefinitie die u wilt verwijderen.

   Zorg ervoor u de juiste te schrappen vormdefinitie kiest. Er is geen doos van de schrappingsbevestigingsdialoog wanneer u **[!UICONTROL Delete]** in de volgende stap klikt.
1. Voor de [!DNL Delete Form Definition] pagina, klik **[!UICONTROL Delete]**.
1. (Facultatief) doe om het even welke volgend:

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Informatie over Index-connector {#concept_CA6921E2FBF641F9B4F60C92B32AFA84}

Gebruik [!DNL Index Connector] om extra inputbronnen voor het indexeren van de pagina&#39;s van XML of om het even welk soort voer te bepalen.

U kunt een inputbron van de gegevensvoer gebruiken om tot inhoud toegang te hebben die in een vorm wordt opgeslagen die van wat typisch op een website gebruikend één van beschikbaar verschillend is ontdekt kruipt methodes. Elk document dat is gekropen en direct wordt geïndexeerd beantwoordt aan een inhoudspagina op uw website. Nochtans, komt een gegevensvoer of uit een document van XML of uit een komma of een lusje-afgebakend tekstdossier, en bevat de inhoudsinformatie aan index.

Een gegevensbron van XML bestaat uit de normen van XML, of verslagen, die informatie bevatten die aan individuele documenten beantwoordt. Deze individuele documenten worden toegevoegd aan de index. Een voer van tekstgegevens bevat individuele nieuw-lijn-afgebakende verslagen die aan individuele documenten beantwoorden. Deze individuele documenten worden ook toegevoegd aan de index. In één van beide geval, beschrijft een configuratie van de indexschakelaar hoe te om het voer te interpreteren. Elke configuratie beschrijft waar het dossier verblijft en hoe de servers tot het toegang hebben. De configuratie beschrijft ook &quot;afbeelding&quot;informatie. Namelijk hoe de punten van elk verslag worden gebruikt om de meta-gegevensgebieden in de resulterende index te bevolken.

Nadat u een definitie van de Schakelaar van de Index aan de [!DNL Staged Index Connector Definitions] pagina toevoegt, kunt u om het even welke configuratie veranderen die, *behalve* de waarden van de Naam of van het Type plaatst.

De [!DNL Index Connector] pagina toont u de volgende informatie:

* De naam van bepaalde indexschakelaars die u hebt gevormd en toegevoegd.
* Één van de volgende gegevensbrontypes voor elke schakelaar die u hebt toegevoegd:

   * **Tekst** - Eenvoudige &quot;vlakke&quot;dossiers, komma-afgebakend, lusje-afgebakend, of andere constant afgebakende formaten.
   * **Voeder** - XML-feeds.
   * **XML** - Verzamelingen van de documenten van XML.

* Of de schakelaar of niet voor volgende wordt toegelaten kruip en het indexeren gedaan.
* Het adres van de gegevensbron.

Zie ook [over de Schakelaar van de Index](../c-about-settings-menu/c-about-crawling-menu.md#concept_CA6921E2FBF641F9B4F60C92B32AFA84)

## Hoe het indexeringsproces voor de configuraties van de Tekst en van het Diervoer in de Schakelaar van de Index werkt {#section_E059A33D61EE4DB0972A37B8A35E9E16}

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
   <td colname="col3"> <p>Voor de configuraties van de Tekst en van het Diervoer, is het een eenvoudige dossierdownload. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>Onderdeel de gedownloade gegevensbron in individuele pseudo-documenten. </p> </td> 
   <td colname="col3"> <p>Voor <span class="uicontrol"> Tekst </span>, beantwoordt elke newline-afgebakende lijn van tekst aan een individueel document, en ontleed gebruikend de gespecificeerde afbakening, zoals een komma of een tabel. </p> <p>Voor <span class="uicontrol"> diervoeders </span>, worden de gegevens van elk document gehaald gebruikend een regelmatig uitdrukkingspatroon in de volgende vorm: </p> <p> <code> &lt;${Itemtag}&gt;(.*?)&lt;/${Itemtag}&gt; </code> </p> <p>Gebruikend <span class="uicontrol"> Kaart </span> op de <span class="wintitle"> Schakelaar van de Index voeg </span> pagina toe, creeer een caching exemplaar van de gegevens en creeer dan een lijst van verbindingen voor de kruippakje. Het gegeven wordt opgeslagen in een lokaal geheime voorgeheugen en bevolkt met de gevormde gebieden. </p> <p>Het ontlede gegeven wordt geschreven aan het lokale geheime voorgeheugen. </p> <p>Dit geheime voorgeheugen wordt gelezen later om de eenvoudige documenten van HTML tot stand te brengen die de kruippakje nodig heeft. Bijvoorbeeld: </p> <p> <code> &lt;html&gt;&lt;head&gt; 
      &lt;title&gt;{title}&lt;/title&gt; 
      &lt;meta&nbsp;name="{field}"&nbsp;content="{data}"&nbsp;/&gt; 
      ... 
      &lt;/head&gt;&lt;body&gt; 
      {body} 
      &lt;/body&gt;&lt;/html&gt; </code> </p> <p>Het <span class="codeph"> &lt;title&gt; </span> element wordt slechts geproduceerd wanneer een afbeelding aan het de meta-gegevensgebied van de Titel bestaat. Op dezelfde manier wordt het <span class="codeph"> &lt;body&gt; </span> element slechts geproduceerd wanneer een afbeelding aan het de meta-gegevensgebied van het Lichaam bestaat. </p> <p> <b>Belangrijk</b>: Er is geen steun voor de toewijzing van waarden aan de vooraf bepaalde meta markering URL. </p> <p>Voor alle andere afbeeldingen, worden <span class="codeph"> &lt;meta&gt; </span> markeringen geproduceerd voor elk gebied dat gegevens heeft die in het oorspronkelijke document worden gevonden. </p> <p>De gebieden voor elk document worden toegevoegd aan het geheime voorgeheugen. Voor elk document dat aan het geheime voorgeheugen wordt geschreven, wordt een verbinding ook geproduceerd zoals in de volgende voorbeelden: </p> <p> <code> &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      .... </code> </p> <p>De afbeelding van de configuratie moet één gebied hebben dat als Primaire Sleutel wordt geïdentificeerd. Deze afbeelding vormt de sleutel die wordt gebruikt wanneer het gegeven van het geheime voorgeheugen wordt gehaald. </p> <p>crawler herkent de URL- <span class="codeph"> index: </span> de regelprefix, die tot de plaatselijk caching gegevens kan dan toegang hebben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>kruip de caching documentreeks. </p> </td> 
   <td colname="col3"> <p>De <span class="codeph"> index: de </span> verbindingen worden toegevoegd aan de hangende lijst van de kruippakje, en in de normale kruipende opeenvolging verwerkt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>Elk document verwerken. </p> </td> 
   <td colname="col3"> <p>De belangrijkste waarde van elke verbinding beantwoordt aan een ingang in het geheime voorgeheugen, zo kruipend resulteert elke verbinding in de gegevens die van dat document van het geheime voorgeheugen worden gehaald. Het wordt dan "geassembleerd"in een beeld van HTML dat wordt verwerkt en aan de index toegevoegd. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Hoe het indexeren proces voor de configuraties van XML in de Schakelaar van de Index werkt {#section_7F1551EA51854C5C99F284CE260526EB}

Het indexeringsproces voor de configuratie van XML is gelijkaardig aan het proces voor de configuraties van de Tekst en van het Diervoer met de volgende minder belangrijke veranderingen en de uitzonderingen.

Omdat de documenten voor XML kruipt reeds in individuele dossiers worden gescheiden, zijn de stappen 1 en 2 in de lijst hierboven niet direct van toepassing. Als u een URL opgeeft op de **[!UICONTROL Host Address]** en **[!UICONTROL File Path]** velden van de [!DNL Index Connector Add] pagina, wordt deze gedownload en verwerkt als een normaal HTML-document. De verwachting is dat het downloaddocument een inzameling van `<a href="{url}"...` verbindingen bevat, elk waarvan aan een document van XML richt dat wordt verwerkt. Dergelijke verbindingen worden omgezet in de volgende vorm:

```
<a href="index:<ic_config_name>?url="{url}">
```

Bijvoorbeeld, als de opstelling van Adobe de volgende verbindingen terugkeerde:

```
<a href="https://www.adobe.com/somepath/doc1.xml">doc 1</a> 
<a href="https://www.adobe.com/otherpath/doc2.xml">doc 2</a>
```

In de lijst hierboven, is stap 3 niet van toepassing en stap 4 wordt voltooid op het tijdstip van het kruipen en het indexeren.

Afwisselend, kunt u uw documenten van XML met andere documenten intermixen die door het kruipproces van nature werden ontdekt. In dergelijke gevallen, kunt u gebruiken herschrijft regels ( **[!UICONTROL Settings]** > **[!UICONTROL Rewrite Rules]** > **[!UICONTROL Crawl List Retrieve URL Rules]**) om XML te veranderen documenten&#39; URLs om hen aan de Schakelaar van de Index te leiden.

Zie [over kruipende Lijst terugwinnen URL Regels](../c-about-settings-menu/c-about-rewrite-rules-menu.md#concept_EC8E2E48B99A458D8567B526C9827CBA).

Bijvoorbeeld, verondersteld u de volgende herschrijf regel hebt:

```
RewriteRule (^http.*[.]xml$) index:Adobe?key=$1
```

Deze regel vertaalt om het even welke URL die met `.xml` in een verbinding van de Schakelaar van de Index eindigt. De kruipper erkent en herschrijft de regeling `index:` URL. Het downloadproces wordt opnieuw gericht door de server van de Apache van de Schakelaar van de Index op de meester. Elk gedownload document wordt onderzocht gebruikend het zelfde regelmatige uitdrukkingspatroon dat met Vervoersmiddelen wordt gebruikt. In dit geval, echter, wordt het geproduceerde HTML- document niet bewaard in het geheime voorgeheugen. In plaats daarvan, wordt het rechtstreeks overhandigd aan de kruipper voor indexverwerking.

## Meerdere indexconnectors configureren {#section_C2B14C0F06354A57AEF6238FF3814E5D}

U kunt de veelvoudige configuraties van de Schakelaar van de Index voor om het even welke rekening bepalen. De configuraties worden automatisch toegevoegd aan de vervolgkeuzelijst in **[!UICONTROL Settings]** > **[!UICONTROL Crawl]** > **[!UICONTROL URL Entrypoints]** , zoals in de volgende afbeelding wordt getoond:

![](assets/url_entrypoints_index_connector.png)

Het selecteren van een configuratie van de drop-down lijst voegt de waarde aan het eind van de lijst van Url- ingangspunten toe.

>[!NOTE]
>
>Terwijl de gehandicapte configuraties van de Schakelaar van de Index aan de drop-down lijst worden toegevoegd, kunt u niet hen selecteren. Als u de zelfde configuratie van de Schakelaar van de Index een tweede keer selecteert, wordt het toegevoegd aan het eind van de lijst, en de vorige instantie wordt geschrapt.

Om een de ingangspunt van de Schakelaar van de Index voor stijgend te specificeren kruipt, kunt u ingangen toevoegen gebruikend het volgende formaat:

```
index:<indexconnector_configuration_name>
```

De kruippakje verwerkt elke toegevoegde ingang als het op de pagina van de Schakelaars van de Index wordt gevonden en toegelaten.

Opmerking: Omdat URL van elk document gebruikend de de configuratienaam van de Schakelaar van de Index en de primaire sleutel van het document wordt geconstrueerd, zeker ben u de zelfde de configuratienaam van de Schakelaar van de Index wanneer het uitvoeren van de Stijgende updates gebruikt! Het doen dit staat toe [!DNL Adobe Search&Promote] om eerder geïndexeerde documenten correct bij te werken.

Zie ook [over Inschrijvingen URL](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573).

**Het gebruik van de Kaarten van de Opstelling wanneer u een Schakelaar van de Index toevoegt**

Wanneer u een Schakelaar van de Index toevoegt, kunt u de eigenschap naar keuze gebruiken **[!UICONTROL Setup Maps]** om een steekproef van uw gegevensbron te downloaden. De gegevens worden onderzocht op indexeerbaarheid.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Als u het type van de Schakelaar van de Index koos... </p> </th> 
   <th colname="col2" class="entry"> <p>De eigenschap van de Kaarten van de Opstelling... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Tekst </p> </td> 
   <td colname="col2"> <p>Bepaalt de afbakeningswaarde door lusjes eerst te proberen, dan verticaal-bars ( <span class="codeph"> | </span>) en ten slotte komma's ( <span class="codeph"> , </span>). Als u reeds een afbakeningswaarde alvorens u <span class="uicontrol"> de Kaarten van de Opstelling klikte </span>, wordt die waarde gebruikt in plaats daarvan. </p> <p>De best-geschikte regeling resulteert in de gebieden van de Kaart die met gokken bij de aangewezen waarden van de Markering en van het Gebied worden ingevuld. Bovendien, wordt een steekproef van de ontlede gegevens getoond. Ben zeker om <span class="uicontrol"> Kopballen in Eerste Rij te selecteren </span> als u weet dat het dossier een kopbalrij omvat. De opstellingsfunctie gebruikt deze informatie om de resulterende kaartingangen beter te identificeren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Diervoeders </p> </td> 
   <td colname="col2"> <p>Downloadt de gegevensbron en voert het eenvoudige ontleden van XML uit. </p> <p>De resulterende herkenningstekens van XPath worden getoond in de rijen van de Markering van de lijst van de Kaart, en gelijkaardige waarden in Gebieden. Deze rijen identificeren slechts de beschikbare gegevens, en produceren niet de ingewikkeldere definities van XPath. Nochtans, is het nog nuttig omdat het de gegevens van XML beschrijft en de waarden van de Objectmarkering identificeert. </p> <p> <p>Opmerking:  De functie van de Kaarten van de Opstelling downloadt de volledige bron van XML om zijn analyse uit te voeren. Als het dossier groot is, kon deze verrichting uit tijd worden. </p> </p> <p>Wanneer succesvol, identificeert deze functie alle mogelijke punten van XPath, veel waarvan niet wenselijk zijn te gebruiken. Zeker ben dat u de resulterende definities van de Kaart onderzoekt en degenen verwijdert die u niet nodig hebt of wilt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>XML </p> </td> 
   <td colname="col2"> <p>Downloadt URL van een representatief individueel document, niet de hoofdverbindingslijst. Dit enige document wordt ontleed gebruikend het zelfde mechanisme dat met Vervoersmiddelen wordt gebruikt, en de resultaten worden getoond. </p> <p>Alvorens u klikt <span class="uicontrol"> voeg toe </span> om de configuratie te bewaren, ben zeker dat u URL terug naar het hoofddocument van de verbindingslijst verandert. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Belangrijk**: De eigenschap van de Kaarten van de Opstelling kan niet voor grote de gegevensreeksen van XML werken omdat zijn dossiersyntactische parser probeert om het volledige dossier in geheugen te lezen. Als gevolg hiervan kon je een &#39;out-of-memory&#39; aandoening ervaren. Nochtans, wanneer het zelfde document op het tijdstip van het indexeren wordt verwerkt, wordt het niet gelezen in geheugen. In plaats daarvan, worden de grote documenten &quot;onderweg,&quot;verwerkt en niet volledig in geheugen eerst gelezen.

**Het gebruik van Voorproef wanneer u een Schakelaar van de Index toevoegt**

Op het ogenblik dat u een Schakelaar van de Index toevoegt, kunt u de eigenschap naar keuze gebruiken **[!UICONTROL Preview]** om de gegevens te bevestigen, alsof u het opsloeg. Het stelt een test tegen de configuratie in werking, maar zonder de configuratie aan de rekening te bewaren. De test heeft toegang tot de gevormde gegevensbron. Nochtans, schrijft het het downloadgeheime voorgeheugen aan een tijdelijke plaats; het botst niet met de belangrijkste geheim voorgeheugenomslag die het indexeren kruipt gebruikt.

De voorproef verwerkt slechts een gebrek van vijf documenten zoals die door Acct worden gecontroleerd:IndexConnector-Voorproef-Maximum-Documenten. De previewed documenten worden getoond in bronvorm, aangezien zij aan het indexeren kruipper worden voorgesteld. De vertoning is gelijkaardig aan een &quot;Bron van de Mening&quot;eigenschap in browser van het Web. U kunt de documenten in de voorproefreeks navigeren gebruikend standaardnavigatiekoppelingen.

De voorproef steunt de geen configuraties van XML omdat dergelijke documenten direct worden verwerkt en niet aan het geheime voorgeheugen worden gedownload.

## Een definitie voor indexaansluiting toevoegen {#task_96779B651A654E1F871F55D6DBBC8886}

Elke configuratie van de Schakelaar van de Index bepaalt een gegevensbron en afbeeldingen om de gegevenspunten met elkaar in verband te brengen die voor die bron aan meta-gegevensgebieden in de index worden bepaald.

Alvorens de gevolgen van de nieuwe en toegelaten definitie aan klanten zichtbaar zijn, herbouw uw plaatsindex.

**Om een definitie van de Schakelaar van de Index toe te voegen**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. Voor de [!DNL Stage Index Connector Definitions] pagina, klik **[!UICONTROL Add New Index Connector]**.
1. Voor de [!DNL Index Connector Add] pagina, plaats de schakelaaropties die u wilt. De opties die beschikbaar zijn hangen van af **[!UICONTROL Type]** die u selecteerde.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Optie </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Naam </p> </td> 
      <td colname="col2"> <p>De unieke naam van de configuratie van de Schakelaar van de Index. U kunt alfanumerieke karakters gebruiken. De tekens "_" en "-" zijn ook toegestaan. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Type </p> </td> 
      <td colname="col2"> <p>De bron van uw gegevens. Het gegevenstype dat u selecteert beïnvloedt de resulterende opties die op de Schakelaar van de <span class="wintitle"> Index beschikbaar zijn voegt </span> pagina toe. U kunt van het volgende kiezen: </p> <p> 
      <ul id="ul_1ADC3DFBC929467385F7465BE8E13635"> 
      <li id="li_64FCD749F55442BAB316BD474128D4F9"> <span class="uicontrol"> Tekst </span> <p>Eenvoudige vlakke tekstdossiers, komma-afgebakend, lusje-afgebakend, of andere constant afgebakende formaten. Elke newline-afgebakende lijn van tekst beantwoordt aan een individueel document, en ontleed gebruikend de gespecificeerde afbakening. </p> <p>U kunt elke waarde, of kolom, aan een meta-gegevensgebied in kaart brengen, dat door het kolomaantal van verwijzingen wordt voorzien, dat bij 1 (begint). </p> </li> 
      <li id="li_2A4F16CE6DCE4114B7F8E4FE156252BB"> <span class="uicontrol"> Diervoeders </span> <p>Downloadt een hoofddocument van XML dat veelvoudige "rijen"van informatie bevat. </p> </li> 
      <li id="li_5A61C53522D74D4C9A5F65989604BDEF"> <span class="uicontrol"> XML </span> <p>Downloadt een hoofddocument van XML dat verbindingen bevat ( 
      <userinput>
        &lt;a&gt; 
      </userinput>) naar afzonderlijke XML-documenten. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>Type gegevensbron: Tekst</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ingeschakeld </p> </td> 
      <td colname="col2"> <p>Zet de configuratie "aan"om te kruipen en index. Of, u kunt "van"de configuratie uitzetten om kruipend en het indexeren te verhinderen. </p> <p> <b>Opmerking</b>: De gehandicapte configuraties van de Schakelaar van de Index worden genegeerd als zij in een entrypoint lijst worden gevonden. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Hostadres </p> </td> 
      <td colname="col2"> <p>Specificeert het adres van de servergastheer waar uw gegevens worden gevestigd. </p> <p>Indien gewenst, kunt u een volledige weg van URI (het Eenvormige Herkenningsteken van het Middel) aan het gegevensbrondocument specificeren zoals in de volgende voorbeelden: </p> <p> <code> https://www.somewhere.com/some_path/some_file.xml </code> </p> <p>of </p> <p> <code> ftp://user:password@ftpserver.somewhere.com/some_path/some_file.xml </code> </p> <p>URI wordt verdeeld in de aangewezen ingangen voor het Adres van de Gastheer, de Weg van het Dossier, het Protocol, en, naar keuze, Gebruikersbenaming, en de gebieden van het Wachtwoord. </p> <p>Specificeert het IP adres of het adres URL van het gastheersysteem waar het gegevensbrondossier wordt gevonden. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Bestandspad </p> </td> 
      <td colname="col2"> <p>Specificeert de weg aan het eenvoudige vlakke tekstdossier, komma-afgebakend, lusje-afgebakend, of ander constant afgebakend formaatdossier. </p> <p>De weg is met betrekking tot de wortel van het gastheeradres. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Incrementeel bestandspad </p> </td> 
      <td colname="col2"> <p>Specificeert de weg aan het eenvoudige vlakke tekstdossier, komma-afgebakend, lusje-afgebakend, of ander constant afgebakend formaatdossier. </p> <p>De weg is met betrekking tot de wortel van het gastheeradres. </p> <p>Dit dossier, indien gespecificeerd, wordt gedownload en tijdens de Verhoogde verrichtingen van de Index verwerkt. Als geen dossier wordt gespecificeerd, wordt het dossier dat onder de Weg van het Dossier wordt vermeld in plaats daarvan gebruikt. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Verticaal bestandspad </p> </td> 
      <td colname="col2"> <p>Specificeert de weg aan het eenvoudige vlakke tekstdossier, komma-afgebakend, lusje-afgebakend, of ander constant afgebakend formaatdossier dat tijdens een Verticale Update moet worden gebruikt. </p> <p>De weg is met betrekking tot de wortel van het gastheeradres. </p> <p>Dit dossier, indien gespecificeerd, wordt gedownload en tijdens de Verticale verrichtingen van de Update verwerkt. </p> <p> <b>Opmerking</b>: Deze eigenschap wordt niet toegelaten door gebrek. Neem contact op met Technische ondersteuning om de functie voor uw gebruik te activeren. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Bestandspad verwijderen </p> </td> 
      <td colname="col2"> <p>Specificeert de weg aan het eenvoudige vlakke tekstdossier, dat één enkele waarde van het documentherkenningsteken per lijn bevat. </p> <p>De weg is met betrekking tot de wortel van het gastheeradres. </p> <p>Dit dossier, indien gespecificeerd, wordt gedownload en tijdens de Verhoogde verrichtingen van de Index verwerkt. De waarden die in dit dossier worden gevonden worden gebruikt om "schrappings"verzoeken te construeren om eerder geïndexeerde documenten te verwijderen. De waarden in dit dossier moeten aan de waarden beantwoorden die in de Volledige of Stijgende dossiers van de Weg van het Dossier, in de kolom worden gevonden die als <span class="uicontrol"> Primaire Sleutel wordt geïdentificeerd </span>. </p> <p> <b>Opmerking</b>: Deze eigenschap wordt niet toegelaten door gebrek. Neem contact op met Technische ondersteuning om de functie voor uw gebruik te activeren. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocol </p> </td> 
      <td colname="col2"> <p>Specificeert het protocol dat wordt gebruikt om tot het dossier toegang te hebben. U kunt van het volgende kiezen: </p> <p> 
      <ul id="ul_F6BC10FD51CA4A1D855B2B3212838A9C"> 
      <li id="li_79FB7DC65E774ABBB23E57BF98AD9738"> HTTP <p>Indien nodig, kunt u juiste authentificatiegeloofsbrieven ingaan om tot de server van HTTP toegang te hebben. </p> </li> 
      <li id="li_BAA9AD5E4B014E09B3A66C94022B7225"> HTTPS <p>Indien nodig, kunt u juiste authentificatiegeloofsbrieven ingaan om tot de server toegang te hebben HTTPS. </p> </li> 
      <li id="li_E716ABB169DD408BA91F1CA27F445A16"> FTP <p>U moet juiste authentificatiegeloofsbrieven ingaan om tot de server van FTP toegang te hebben. </p> </li> 
      <li id="li_FD7143019C5244C3B8A5B1B5AA84859A"> SFTP <p>U moet juiste authentificatiegeloofsbrieven ingaan om tot de server toegang te hebben SFTP. </p> </li> 
      <li id="li_38E0036C1365419F9D00083CACA34AFB"> Bestand </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Onderbreking </p> </td> 
      <td colname="col2"> <p>Specificeert de onderbreking, in seconden, voor FTP, SFTP, HTTP of verbindingen HTTPS. Deze waarde moet tussen 30 en 300 zijn. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Retries </p> </td> 
      <td colname="col2"> <p>Specificeert het maximumaantal pogingen voor ontbroken verbindingen FTP, SFTP, HTTP of HTTPS opnieuw. Deze waarde moet tussen 0 en 10 zijn. </p> <p>Een waarde van nul (0) zal herhalingspogingen verhinderen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Codering </p> </td> 
      <td colname="col2"> <p>Specificeert het karakter het coderen systeem dat in het gespecificeerde gegevensbrondossier wordt gebruikt. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Afbakening </p> </td> 
      <td colname="col2"> <p>Specificeert het karakter dat u wilt gebruiken om elk gebied in het gespecificeerde gegevensbrondossier te afbakenen. </p> <p>Het komma karakter ( <span class="codeph"> , </span>) is een voorbeeld van een afbakening. De komma doet dienst als gebiedsafbakening die helpt om gegevensgebieden in uw gespecificeerd gegevensbrondossier te scheiden. </p> <p>Selecteer <span class="uicontrol"> Tab? </span> om het horizontale lusjekarakter als afbakening te gebruiken. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Koppen in de Eerste rij </p> </td> 
      <td colname="col2"> <p>Wijst erop dat de eerste rij in het gegevensbrondossier kopbalinformatie slechts, niet gegevens bevat. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Minimumaantal indexeringsdocumenten </p> </td> 
      <td colname="col2"> <p>Als de reeks aan een positieve waarde, dit het minimumaantal verslagen specificeert die in het gedownloade dossier worden verwacht. Als minder verslagen worden ontvangen, wordt de indexverrichting geaborteerd. </p> <p> <b>Opmerking</b>: Deze eigenschap wordt niet toegelaten door gebrek. Neem contact op met Technische ondersteuning om de functie voor uw gebruik te activeren. </p> <p> <b>Opmerking</b>: Deze eigenschap wordt slechts gebruikt tijdens de volledige verrichtingen van de Index. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Kaart </p> </td> 
      <td colname="col2"> <p>Specificeert kolom-aan-meta-gegevensafbeeldingen, gebruikend kolomaantallen. </p> <p> 
      <ul id="ul_981AE2C6D30443BDBFC6575D413732A2"> 
      <li id="li_A42CB9DFFF8C45A7BAC2D471FE96CEBE"> <span class="uicontrol"> Kolom </span> <p> Specificeert een kolomaantal, met de eerste kolom die 1 (één) zijn. Om nieuwe kaartrijen voor elke kolom, onder <span class="wintitle"> Actie toe te voegen </span>, klik <span class="uicontrol"> + </span>. </p> <p>U te hoeven niet om elke kolom in de gegevensbron van verwijzingen te voorzien. In plaats daarvan, kunt u verkiezen om waarden over te slaan. </p> </li> 
      <li id="li_26E8C9554A5D4BC5A5073D6385E3626F"> <span class="uicontrol"> Veld </span> <p>Bepaalt de waarde van de naamattributen die voor elke geproduceerde &lt;meta&gt; markering wordt gebruikt. </p> </li> 
      <li id="li_5DFA514B7F9549B98D6CBC095A66033C"> <span class="uicontrol"> Metagegevens? </span> <p>Veroorzaakt <span class="uicontrol"> Gebied </span> om een drop-down lijst te worden waarvan u bepaalde meta-gegevensgebieden voor de huidige rekening kunt selecteren. </p> <p>De <span class="uicontrol"> waarde van het Gebied </span> kan een niet gedefiniëerd meta-gegevensgebied zijn, indien gewenst. Een niet gedefiniëerd meta-gegevensgebied is soms nuttig om inhoud tot stand te brengen die door Manuscript wordt gebruikt te <span class="wintitle"> filtreren </span>. </p> <p>Zie <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> over Filtrerend Manuscript </a>. </p> <p>Wanneer de Schakelaar van de Index de documenten van XML met veelvoudige klappen op om het even welk kaartgebied verwerkt, worden de veelvoudige waarden aaneengeschakeld in één enkele waarde in het resulterende caching document. Door gebrek, worden deze waarden gecombineerd gebruikend een komma afbakening. Nochtans, veronderstel dat de overeenkomstige <span class="wintitle"> </span> waarde van het Gebied een bepaald meta-gegevensgebied is. Bovendien heeft dat gebied de <span class="wintitle"> Allow reeks van de </span> attributen van Lijsten. In dit geval, wordt de waarde van de Delimiters van de Lijst van het gebied, die de eerste bepaalde afbakening is, gebruikt in de aaneenschakeling. </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892C95"> <span class="uicontrol"> Primaire sleutel? </span> <p>Slechts één kaartdefinitie wordt geïdentificeerd als primaire sleutel. Dit gebied wordt de unieke verwijzing die wordt voorgesteld wanneer dit document aan de index wordt toegevoegd. Deze waarde wordt gebruikt in URL van het document in de Index. </p> <p>De <span class="uicontrol"> Primaire Zeer belangrijke </span> waarden moeten over alle documenten uniek zijn die door de configuratie van de Schakelaar van de Index worden vertegenwoordigd - om het even welke ontmoet duplicaten zullen worden genegeerd. Als uw brondocumenten geen enkele unieke waarde voor gebruik als <span class="uicontrol"> Primaire Sleutel bevatten </span>, maar twee of meer samen genomen gebieden <i>kunnen</i> een uniek herkenningsteken vormen, kunt u de <span class="uicontrol"> Primaire Sleutel bepalen </span> door veelvoudige <span class="uicontrol"> </span> waarden van de Kolom met een verticale bar ("|") te combineren die de waarden afbakenen. </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892D96"> <span class="uicontrol"> HTML strippen? </span> <p>Wanneer deze optie wordt gecontroleerd, worden om het even welke markeringen van HTML die in de gegevens van dit gebied worden gevonden verwijderd. </p> </li> 
      <li id="li_359D2902859B4C5BADB0BA26F0BA4DC0"> <span class="uicontrol"> Actie </span> <p>Laat u rijen aan de kaart toevoegen of rijen verwijderen uit de kaart. De orde van de rijen is niet belangrijk. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>Type gegevensbron: Diervoeders</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ingeschakeld </p> </td> 
      <td colname="col2"> <p>Zet de configuratie "aan"om te kruipen en index. Of, u kunt "van"de configuratie uitzetten om kruipend en het indexeren te verhinderen. </p> <p> <b>Opmerking</b>: De gehandicapte configuraties van de Schakelaar van de Index worden genegeerd als zij in een entrypoint lijst worden gevonden. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Hostadres </p> </td> 
      <td colname="col2"> <p>Specificeert het IP adres of het adres URL van het gastheersysteem waar het gegevensbrondossier wordt gevonden. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Bestandspad </p> </td> 
      <td colname="col2"> <p>Specificeert de weg aan het hoofddocument van XML dat veelvoudige "rijen"van informatie bevat. </p> <p>De weg is met betrekking tot de wortel van het gastheeradres. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Incrementeel bestandspad </p> </td> 
      <td colname="col2"> <p>Specificeert de weg aan het stijgende document van XML dat veelvoudige "rijen"van informatie bevat. </p> <p>De weg is met betrekking tot de wortel van het gastheeradres. </p> <p>Dit dossier, indien gespecificeerd, wordt gedownload en tijdens de Verhoogde verrichtingen van de Index verwerkt. Als geen dossier wordt gespecificeerd, wordt het dossier dat onder de Weg van het Dossier wordt vermeld in plaats daarvan gebruikt. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Verticaal bestandspad </p> </td> 
      <td colname="col2"> <p>Specificeert de weg aan het document van XML dat veelvoudige dunne "rijen"van informatie bevat die tijdens een Verticale Update moet worden gebruikt. </p> <p>De weg is met betrekking tot de wortel van het gastheeradres. </p> <p>Dit dossier, indien gespecificeerd, wordt gedownload en tijdens de Verticale verrichtingen van de Update verwerkt. </p> <p> <b>Opmerking</b>: Deze eigenschap wordt niet toegelaten door gebrek. Neem contact op met Technische ondersteuning om de functie voor uw gebruik te activeren. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Bestandspad verwijderen </p> </td> 
      <td colname="col2"> <p>Specificeert de weg aan het eenvoudige vlakke tekstdossier, dat één enkele waarde van het documentherkenningsteken per lijn bevat. </p> <p>De weg is met betrekking tot de wortel van het gastheeradres. </p> <p>Dit dossier, indien gespecificeerd, wordt gedownload en tijdens de Verhoogde verrichtingen van de Index verwerkt. De waarden die in dit dossier worden gevonden worden gebruikt om "schrappings"verzoeken te construeren om eerder geïndexeerde documenten te verwijderen. De waarden in dit dossier moeten aan de waarden beantwoorden die in de Volledige of Stijgende dossiers van de Weg van het Dossier, in de kolom worden gevonden die als <span class="uicontrol"> Primaire Sleutel wordt geïdentificeerd </span>. </p> <p> <b>Opmerking</b>: Deze eigenschap wordt niet toegelaten door gebrek. Neem contact op met Technische ondersteuning om de functie voor uw gebruik te activeren. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocol </p> </td> 
      <td colname="col2"> <p>Specificeert het protocol dat wordt gebruikt om tot het dossier toegang te hebben. U kunt van het volgende kiezen: </p> <p> 
      <ul id="ul_976A34FD14A841F2B610C1C0CCBB82B9"> 
      <li id="li_05BBA0F670F14431A89AE4178F1A6F94"> HTTP <p>Indien nodig, kunt u juiste authentificatiegeloofsbrieven ingaan om tot de server van HTTP toegang te hebben. </p> </li> 
      <li id="li_100446691F304572B8FC3F083F86A2CB"> HTTPS <p>Indien nodig, kunt u juiste authentificatiegeloofsbrieven ingaan om tot de server toegang te hebben HTTPS. </p> </li> 
      <li id="li_027088A8E30444DAA8CCCC5B0BAA74C1"> FTP <p>U moet juiste authentificatiegeloofsbrieven ingaan om tot de server van FTP toegang te hebben. </p> </li> 
      <li id="li_DCEF9D5C99354990B03E29083C2ED8DC"> SFTP <p>U moet juiste authentificatiegeloofsbrieven ingaan om tot de server toegang te hebben SFTP. </p> </li> 
      <li id="li_44E34FF2AB0D429EB3408106E6FCF780"> Bestand </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Item </p> </td> 
      <td colname="col2"> <p>Identificeert het element van XML dat u kunt gebruiken om de individuele lijnen van XML in het gegevensbrondossier te identificeren dat u specificeerde. </p> <p>Bijvoorbeeld, in het volgende fragment van het Diervoer van een document van Adobe XML, is de waarde van het Punt <span class="codeph"> verslag </span>: </p> <p> <code> &lt;?xml&nbsp;version="1.0"&nbsp;encoding="utf-8"?&gt; 
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
      <td colname="col1"> <p>Minimumaantal indexeringsdocumenten </p> </td> 
      <td colname="col2"> <p>Als de reeks aan een positieve waarde, dit het minimumaantal verslagen specificeert die in het gedownloade dossier worden verwacht. Als minder verslagen worden ontvangen, wordt de indexverrichting geaborteerd. </p> <p> <b>Opmerking</b>: Deze eigenschap wordt niet toegelaten door gebrek. Neem contact op met Technische ondersteuning om de functie voor uw gebruik te activeren. </p> <p> <b>Opmerking</b>: Deze eigenschap wordt slechts gebruikt tijdens de volledige verrichtingen van de Index. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Kaart </p> </td> 
      <td colname="col2"> <p>Laat u XML-element-aan-meta-gegevensafbeeldingen specificeren, gebruikend de uitdrukkingen van XPath. </p> <p> 
      <ul id="ul_604108C0277C4892AE8A40CA39889ABD"> 
      <li id="li_0AF92270AE9F4BA8B2C7EE41FABC0F34"> <span class="uicontrol"> Markering </span> <p>Specificeert een vertegenwoordiging van XPath van de ontlede gegevens van XML. Gebruikend het document van voorbeeldAdobe XML hierboven, onder de optieItem, kon het worden in kaart gebracht gebruikend de volgende syntaxis: </p> <p> <code> /record/@displayurl&nbsp;-&gt;&nbsp;page-url 
      /record/metadata/meta[@name='title']/@content&nbsp;-&gt;&nbsp;title 
      /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;desc 
      /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;body </code> </p> <p>De bovengenoemde syntaxis vertaalt als het volgende: </p> <p> 
      <ul id="ul_6400EBD08D424EADA1612FE4F7EFB640"> 
      <li id="li_9958F9B40D42434195597DBA9F2AF28F"> <code> /record/@displayurl&amp;nbsp;-&gt;&amp;nbsp;page-url </code> <p>Het <span class="codeph"> vertoningsattribuut </span> van het <span class="codeph"> verslag </span> elementenkaarten aan het meta-gegevensgebied pagina-url <span class="codeph"> </span>. </p> </li> 
      <li id="li_759013EA02CD48BE971A55B0A6A11424"> <code> /record/metadata/meta[@name='title']/@content&amp;nbsp;-&gt;&amp;nbsp;title </code> <p>Het <span class="codeph"> inhoudsattribuut </span> van om het even welk <span class="codeph"> meta- </span> element dat binnen een <span class="codeph"> meta-gegevenselement bevat is, dat binnen een </span> verslag- <span class="codeph"> element bevat is, de waarvan naamattribuut </span> titel is, kaarten aan de  titel van het meta-gegevensgebied in kaart brengen <span class="codeph"> </span><span class="codeph"> </span>. </p> </li> 
      <li id="li_E741CA59197D462EB2946EDE874AFDC8"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;desc </code> <p>Het <span class="codeph"> inhoudsattribuut </span> van om het even welk <span class="codeph"> meta- </span> element dat binnen een <span class="codeph"> meta-gegevenselement bevat is, dat binnen het </span> verslag- <span class="codeph"> element bevat is, de waarvan naamattribuut </span> <span class="codeph"> </span><span class="codeph"> </span>beschrijving is, kaarten aan het meta-gegevensgebied desc. </p> </li> 
      <li id="li_E35EAE3D284D46D485D9064D7BB6AB13"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;body </code> <p>Het <span class="codeph"> inhoudsattribuut </span> van om het even welk <span class="codeph"> meta- </span> element dat binnen een <span class="codeph"> meta-gegevenselement bevat is, dat binnen het </span> verslag- <span class="codeph"> element bevat is, de waarvan naam het attribuut </span> beschrijving is, kaarten aan het  lichaam van het meta-gegevensgebied in kaart brengt <span class="codeph"> </span><span class="codeph"> </span>. </p> </li> 
      </ul> </p> <p>XPath is een vrij ingewikkelde aantekening. Meer informatie is beschikbaar op de volgende plaats: </p> <p>Zie <a href="https://www.w3schools.com/xpath/" scope="external" format="html"> https://www.w3schools.com/xpath/ </a> </p> </li> 
      <li id="li_8147075D7ACD4811A7ED335F23FE62A6"> <span class="uicontrol"> Veld </span> <p>Bepaalt de waarde van de naamattributen die voor elke geproduceerde <span class="codeph"> &lt;meta&gt; </span> markering wordt gebruikt. </p> </li> 
      <li id="li_2380199D63BF425A919606D8232FA6E2"> <span class="uicontrol"> Metagegevens? </span> <p>Veroorzaakt <span class="uicontrol"> Gebied </span> om een drop-down lijst te worden waarvan u bepaalde meta-gegevensgebieden voor de huidige rekening kunt selecteren. </p> <p>De <span class="uicontrol"> waarde van het Gebied </span> kan een niet gedefiniëerd meta-gegevensgebied zijn, indien gewenst. Een niet gedefiniëerd meta-gegevensgebied is soms nuttig om inhoud tot stand te brengen die door Manuscript wordt gebruikt te <span class="wintitle"> filtreren </span>. </p> <p>Zie <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> over Filtrerend Manuscript </a>. </p> <p>Wanneer de Schakelaar van de Index de documenten van XML met veelvoudige klappen op om het even welk kaartgebied verwerkt, worden de veelvoudige waarden aaneengeschakeld in één enkele waarde in het resulterende caching document. Door gebrek, worden deze waarden gecombineerd gebruikend een komma afbakening. Nochtans, veronderstel dat de overeenkomstige <span class="wintitle"> </span> waarde van het Gebied een bepaald meta-gegevensgebied is. Bovendien heeft dat gebied de <span class="wintitle"> Allow reeks van de </span> attributen van Lijsten. In dit geval, wordt de waarde van de Delimiters van de Lijst van het gebied, die de eerste bepaalde afbakening is, gebruikt in de aaneenschakeling. </p> </li> 
      <li id="li_DEA24003E97E406DA2510C43CCFDC70E"> <span class="uicontrol"> Primaire sleutel? </span> <p>Slechts één kaartdefinitie wordt geïdentificeerd als primaire sleutel. Dit gebied wordt de unieke verwijzing die wordt voorgesteld wanneer dit document aan de index wordt toegevoegd. Deze waarde wordt gebruikt in URL van het document in de Index. </p> <p>De <span class="uicontrol"> Primaire Zeer belangrijke </span> waarden moeten over alle documenten uniek zijn die door de configuratie van de Schakelaar van de Index worden vertegenwoordigd - om het even welke ontmoet duplicaten zullen worden genegeerd. Als uw brondocumenten geen enkele unieke waarde voor gebruik als <span class="uicontrol"> Primaire Sleutel bevatten </span>, maar twee of meer samen genomen gebieden <i>kunnen</i> een uniek herkenningsteken vormen, kunt u de <span class="uicontrol"> Primaire Sleutel bepalen </span> door veelvoudige <span class="uicontrol"> </span> definities van de Markering met een verticale bar ("|") te combineren die de waarden afbakenen. </p> </li> 
      <li id="li_DEA24003E97E406DA2510C43CCFDC81F"> <span class="uicontrol"> HTML strippen? </span> <p>Wanneer deze optie wordt gecontroleerd, worden om het even welke markeringen van HTML die in de gegevens van dit gebied worden gevonden verwijderd. </p> </li> 
      <li id="li_5E829D1D0DBD4BB7AAB5DB983053D248"> <span class="uicontrol"> Gebruik voor Verwijderen? </span> <p>Wordt alleen gebruikt tijdens incrementele indexbewerkingen. De verslagen die dit patroon van XPath aanpassen identificeren punten voor schrapping. De <span class="uicontrol"> Primaire Belangrijkste </span> waarde voor elk zulk verslag wordt gebruikt om "schrappings"verzoeken te construeren, zoals met de Weg van het Dossier van de Schrapping. </p> <p> <b>Opmerking</b>: Deze eigenschap wordt niet toegelaten door gebrek. Neem contact op met Technische ondersteuning om de functie voor uw gebruik te activeren. </p> </li> 
      <li id="li_D40E2F9AD8AD49FC9AC4B8C75BA31E28"> <span class="uicontrol"> Actie </span> <p>Laat u rijen aan de kaart toevoegen of rijen verwijderen uit de kaart. De orde van de rijen is niet belangrijk. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>Type gegevensbron: XML</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ingeschakeld </p> </td> 
      <td colname="col2"> <p>Zet de configuratie "aan"om te kruipen en index. Of, u kunt "van"de configuratie uitzetten om kruipend en het indexeren te verhinderen. </p> <p> <b>Opmerking</b>: De gehandicapte configuraties van de Schakelaar van de Index worden genegeerd als zij in een entrypoint lijst worden gevonden. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Hostadres </p> </td> 
      <td colname="col2"> <p>Specificeert het adres URL van het gastheersysteem waar het gegevensbrondossier wordt gevonden. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Bestandspad </p> </td> 
      <td colname="col2"> <p>Specificeert de weg aan het hoofddocument van XML dat verbindingen bevat ( 
      <userinput>
        &lt;a&gt; 
      </userinput>) naar afzonderlijke XML-documenten. </p> <p>De weg is met betrekking tot de wortel van het gastheeradres. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocol </p> </td> 
      <td colname="col2"> <p>Specificeert het protocol dat wordt gebruikt om tot het dossier toegang te hebben. U kunt van het volgende kiezen: </p> <p> 
      <ul id="ul_EA4EB7953D68483FAD75753B2EE70E74"> 
      <li id="li_537F24C6B2AB435CB7C14117663D7B3F"> HTTP <p>Indien nodig, kunt u juiste authentificatiegeloofsbrieven ingaan om tot de server van HTTP toegang te hebben. </p> </li> 
      <li id="li_8C13C93C52364FFA8B9B18830CDB223C"> HTTPS <p>Indien nodig, kunt u juiste authentificatiegeloofsbrieven ingaan om tot de server toegang te hebben HTTPS. </p> </li> 
      <li id="li_2F967B5675254C949B31EAB19910751C"> FTP <p>U moet juiste authentificatiegeloofsbrieven ingaan om tot de server van FTP toegang te hebben. </p> </li> 
      <li id="li_C24BE4C1DE79488AA64C7133D78CD3A6"> SFTP <p>U moet juiste authentificatiegeloofsbrieven ingaan om tot de server toegang te hebben SFTP. </p> </li> 
      <li id="li_7581C21CFC104986A361F62BD7A370C1"> Bestand </li> 
      </ul> </p> <p> <b>Opmerking</b>: Het plaatsen van het Protocol wordt slechts gebruikt wanneer er informatie is die op het Adres van de Gastheer en/of de gebieden van de Weg van het Dossier wordt gespecificeerd. De individuele documenten van XML worden gedownload gebruikend of HTTP of HTTPS, volgens hun specificaties URL. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Item </p> </td> 
      <td colname="col2"> <p>Identificeert het element van XML dat een "rij"in het gegevensbrondossier bepaalt dat u specificeerde. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Kaart </p> </td> 
      <td colname="col2"> <p>Laat u kolom-aan-meta-gegevensafbeeldingen specificeren, gebruikend kolomaantallen. </p> <p> 
      <ul id="ul_06F50CBA0AA64C7CB1AFAE076E629A64"> 
      <li id="li_0FA2502869BA40DC93D790B79E15A9D2"> <span class="uicontrol"> Markering </span> <p>Specificeert een vertegenwoordiging van XPath van de ontlede gegevens van XML. Gebruikend het document van voorbeeldAdobe XML hierboven, onder de optieItem, kunt u het in kaart brengen gebruikend de volgende syntaxis: </p> <p> <code> /record/@displayurl&nbsp;-&gt;&nbsp;page-url 
        /record/metadata/meta[@name='title']/@content&nbsp;-&gt;&nbsp;title 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;desc 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;body </code> </p> <p>De bovengenoemde syntaxis vertaalt als het volgende: </p> <p> 
      <ul id="ul_F8C536E6E54546D9AA5B22B879C0AF39"> 
      <li id="li_78A35DFFF1B4496CAC6EDC7B1E991F29"> <code> /record/@displayurl&amp;nbsp;-&gt;&amp;nbsp;page-url </code> <p>Het <span class="codeph"> vertoningsattribuut </span> van het <span class="codeph"> verslag </span> elementenkaarten aan het meta-gegevensgebied pagina-url <span class="codeph"> </span>. </p> </li> 
      <li id="li_FA7DF3D1942248B98660F3D0C82F4563"> <code> /record/metadata/meta[@name='title']/@content&amp;nbsp;-&gt;&amp;nbsp;title </code> <p>Het <span class="codeph"> inhoudsattribuut </span> van om het even welk <span class="codeph"> meta- </span> element dat binnen een <span class="codeph"> meta-gegevenselement bevat is, dat binnen een </span> verslag- <span class="codeph"> element bevat is, de waarvan naamattribuut </span> titel is, kaarten aan de  titel van het meta-gegevensgebied in kaart brengen <span class="codeph"> </span><span class="codeph"> </span>. </p> </li> 
      <li id="li_D8000A116FF84DE59ED19C656DDD3BC1"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;desc </code> <p>Het <span class="codeph"> inhoudsattribuut </span> van om het even welk <span class="codeph"> meta- </span> element dat binnen een <span class="codeph"> meta-gegevenselement bevat is, dat binnen het </span> verslag- <span class="codeph"> element bevat is, de waarvan naamattribuut </span> <span class="codeph"> </span><span class="codeph"> </span>beschrijving is, kaarten aan het meta-gegevensgebied desc. </p> </li> 
      <li id="li_7FA6A53DFD3D42A98B7BA17CC29DDB81"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;body </code> <p>Het <span class="codeph"> inhoudsattribuut </span> van om het even welk <span class="codeph"> meta- </span> element dat binnen een <span class="codeph"> meta-gegevenselement bevat is, dat binnen het </span> verslag- <span class="codeph"> element bevat is, de waarvan naam het attribuut </span> beschrijving is, kaarten aan het  lichaam van het meta-gegevensgebied in kaart brengt <span class="codeph"> </span><span class="codeph"> </span>. </p> </li> 
      </ul> </p> <p>XPath is een vrij ingewikkelde aantekening. Meer informatie is beschikbaar op de volgende plaats: </p> <p>Zie <a href="https://www.w3schools.com/xpath/" scope="external" format="html"> https://www.w3schools.com/xpath/ </a> </p> </li> 
      <li id="li_84999D07E0AE4265BC7928BBB49957B9"> <span class="uicontrol"> Veld </span> <p>Bepaalt de waarde van de naamattributen die voor elke geproduceerde &lt;meta&gt; markering wordt gebruikt. </p> </li> 
      <li id="li_E125788D0F5242958BD790E26A675C20"> <span class="uicontrol"> Metagegevens? </span> <p>Veroorzaakt <span class="uicontrol"> Gebied </span> om een drop-down lijst te worden waarvan u bepaalde meta-gegevensgebieden voor de huidige rekening kunt selecteren. </p> <p>De <span class="uicontrol"> waarde van het Gebied </span> kan een niet gedefiniëerd meta-gegevensgebied zijn, indien gewenst. Een niet gedefiniëerd meta-gegevensgebied is soms nuttig om inhoud tot stand te brengen die door Manuscript wordt gebruikt te <span class="wintitle"> filtreren </span>. </p> <p>Zie <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> over Filtrerend Manuscript </a>. </p> <p>Wanneer de Schakelaar van de Index de documenten van XML met veelvoudige klappen op om het even welk kaartgebied verwerkt, worden de veelvoudige waarden aaneengeschakeld in één enkele waarde in het resulterende caching document. Door gebrek, worden deze waarden gecombineerd gebruikend een komma afbakening. Nochtans, veronderstel dat de overeenkomstige <span class="wintitle"> </span> waarde van het Gebied een bepaald meta-gegevensgebied is. Bovendien heeft dat gebied de <span class="wintitle"> Allow reeks van de </span> attributen van Lijsten. In dit geval, wordt de waarde van de Delimiters van de Lijst van het gebied, die de eerste bepaalde afbakening is, gebruikt in de aaneenschakeling. </p> </li> 
      <li id="li_9F435EFB3EC74B409EC82A851824609F"> <span class="uicontrol"> Primaire sleutel? </span> <p>Slechts één kaartdefinitie wordt geïdentificeerd als primaire sleutel. Dit gebied wordt de unieke verwijzing die wordt voorgesteld wanneer dit document aan de index wordt toegevoegd. Deze waarde wordt gebruikt in URL van het document in de Index. </p> <p>De <span class="uicontrol"> Primaire Zeer belangrijke </span> waarden moeten over alle documenten uniek zijn die door de configuratie van de Schakelaar van de Index worden vertegenwoordigd - om het even welke ontmoet duplicaten zullen worden genegeerd. Als uw brondocumenten geen enkele unieke waarde voor gebruik als <span class="uicontrol"> Primaire Sleutel bevatten </span>, maar twee of meer samen genomen gebieden <i>kunnen</i> een uniek herkenningsteken vormen, kunt u de <span class="uicontrol"> Primaire Sleutel bepalen </span> door veelvoudige <span class="uicontrol"> </span> definities van de Markering met een verticale bar ("|") te combineren die de waarden afbakenen. </p> </li> 
      <li id="li_9F435EFB3EC74B409EC82A851824610G"> <span class="uicontrol"> HTML strippen? </span> <p>Wanneer deze optie wordt gecontroleerd, worden om het even welke markeringen van HTML die in de gegevens van dit gebied worden gevonden verwijderd. </p> </li> 
      <li id="li_6302D18971AD439FBECE27742649C56B"> <span class="uicontrol"> Actie </span> <p>Laat u rijen aan de kaart toevoegen of rijen verwijderen uit de kaart. De orde van de rijen is niet belangrijk. </p> </li> 
      </ul> </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. (Facultatief) klik **[!UICONTROL Setup Maps]** om een steekproef van uw gegevensbron te downloaden. De gegevens worden onderzocht op indexeerbaarheid. Deze eigenschap is beschikbaar voor Tekst en de Types van Diervoeders, slechts.
1. (Facultatief) klik **[!UICONTROL Preview]** om het daadwerkelijke werk van de configuratie te testen. Deze eigenschap is beschikbaar voor Tekst en de Types van Diervoeders, slechts.
1. Klik **[!UICONTROL Add]** om de configuratie aan de [!DNL Index Connector Definitions] pagina en aan de [!DNL Index Connector Configurations] drop-down lijst op de [!DNL URL Entrypoints] pagina toe te voegen.

   Zie [over URL Inschrijvingen](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573).
1. Voor de [!DNL Index Connector Definitions] pagina, klik **[!UICONTROL rebuild your staged site index]**.
1. (Facultatief) op de [!DNL Index Connector Definitions] pagina, doe om het even welke volgend:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een definitie voor indexaansluiting bewerken {#task_DCFC9C6A9964421DB5AB6C25DEE98DE9}

U kunt een bestaande Schakelaar van de Index uitgeven die u hebt bepaald.

>[!NOTE]
>
>Niet zijn alle opties beschikbaar voor u om, zoals de Naam of het Type van de Schakelaar van de Index van de drop-down lijst te veranderen. [!DNL Type]

**Om een definitie van de Schakelaar van de Index uit te geven**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. Voor de [!DNL Index Connector] pagina, onder de [!DNL Actions] kolomrubriek, klik **[!UICONTROL Edit]** voor een de definitienaam van de Schakelaar van de Index de waarvan montages u wilt veranderen.
1. Voor de [!DNL Index Connector Edit] pagina, plaats de opties u wilt.

   Zie de lijst van opties onder het [Toevoegen van een definitie](../c-about-settings-menu/c-about-crawling-menu.md#task_96779B651A654E1F871F55D6DBBC8886)van de Schakelaar van de Index.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Facultatief) op de [!DNL Index Connector Definitions] pagina, klik **[!UICONTROL rebuild your staged site index]**.
1. (Facultatief) op de [!DNL Index Connector Definitions] pagina, doe om het even welke volgend:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Het bekijken van de montages van een definitie van de Schakelaar van de Index {#task_D0B71A7426E54247BDB3468EC576D871}

U kunt de configuratiemontages van een bestaande definitie van de indexschakelaar herzien.

Nadat een definitie van de Schakelaar van de Index aan de [!DNL Index Connector Definitions] pagina wordt toegevoegd, kunt u niet zijn het plaatsen van het Type veranderen. In plaats daarvan, moet u de definitie schrappen en dan nieuwe toevoegen.

**Om de montages van een definitie van de Schakelaar van de Index te bekijken**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. Voor de [!DNL Index Connector] pagina, onder de [!DNL Actions] kolomrubriek, klik **[!UICONTROL Edit]** voor een de definitienaam van de Schakelaar van de Index de waarvan montages u wilt herzien of uitgeven.

## Het kopiëren van een definitie van de Schakelaar van de Index {#task_3AD55DF07FC44A748D0EFDAB7B35699B}

U kunt een bestaande definitie van de Schakelaar van de Index kopiëren om als basis voor een nieuwe Schakelaar van de Index te gebruiken die u wilt tot stand brengen.

Wanneer het kopiëren van een definitie van de Schakelaar van de Index, wordt de gekopieerde definitie onbruikbaar gemaakt door gebrek. Om de definitie in te schakelen of &quot;aan te zetten&quot;, moet u deze bewerken vanaf de [!DNL Index Connector Edit] pagina en selecteren **[!UICONTROL Enable]**.

Zie een definitie [van de Schakelaar van de Index](../c-about-settings-menu/c-about-crawling-menu.md#task_DCFC9C6A9964421DB5AB6C25DEE98DE9)uitgeven.

**Om een definitie van de Schakelaar van de Index te kopiëren**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. Voor de [!DNL Index Connector] pagina, onder de [!DNL Actions] kolomrubriek, klik **[!UICONTROL Copy]** voor een de definitienaam van de Schakelaar van de Index de waarvan montages u wilt dupliceren.
1. Voor de [!DNL Index Connector Copy] pagina, ga de nieuwe naam van de definitie in.
1. Klik op **[!UICONTROL Copy]**.
1. (Facultatief) op de [!DNL Index Connector Definitions] pagina, doe om het even welke volgend:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Het anders noemen van een definitie van de Schakelaar van de Index {#task_5132118FC21B47D99881E0ED425225D7}

U kunt de naam van een bestaande definitie van de Schakelaar van de Index veranderen.

Nadat u de definitie anders noemt, controleer **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**. U wilt ervoor zorgen dat de nieuwe definitienaam in de drop-down lijst op de [!DNL URL Entrypoints] pagina wordt weerspiegeld.

Zie [het Toevoegen van veelvoudige URL ingangspunten die u geïndexeerd](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45)wilt.

**Om een definitie van de Schakelaar van de Index anders te noemen**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. Voor de [!DNL Index Connector] pagina, onder de [!DNL Actions] kolomrubriek, klik **[!UICONTROL Rename]** voor de de definitienaam van de Schakelaar van de Index die u wilt veranderen.
1. Voor de [!DNL Index Connector Rename] pagina, ga de nieuwe naam van de definitie op het [!DNL Name] gebied in.
1. Klik op **[!UICONTROL Rename]**.
1. Klik op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**. Als de naam van de vorige Schakelaar van de Index in de lijst aanwezig is, verwijder het, en voeg de onlangs anders genoemde ingang toe.

   Zie [het Toevoegen van veelvoudige URL ingangspunten die u geïndexeerd](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45)wilt. 1. (Facultatief) op de [!DNL Index Connector Definitions] pagina, doe om het even welke volgend:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een definitie van een indexconnector verwijderen {#task_6B0BD5D0C09F4597A401B0F3AC7C7EA7}

U kunt een bestaande definitie van de Schakelaar van de Index schrappen die u niet meer nodig hebt of gebruikt.

**Om een definitie van de Schakelaar van de Index te schrappen**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. Voor de [!DNL Index Connector Definitions] pagina, onder de [!DNL Actions] kolomrubriek, klik **[!UICONTROL Delete]** voor de de definitienaam van de Schakelaar van de Index u wilt verwijderen.
1. Voor de [!DNL Index Connector Delete] pagina, klik **[!UICONTROL Delete]**.
