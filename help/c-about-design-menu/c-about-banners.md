---
description: Met Banners kunt u de banneradvertenties op uw website beheren.
solution: Target
title: Informatie over banners
topic: Ontwerpen, zoeken en verhandelen van sites
uuid: 653b567d-5cf3-41a0-a260-a6912d0fd20d
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '4801'
ht-degree: 0%

---


# Informatie over banners {#about-banners}

Met Banners kunt u de banneradvertenties beheren die zich op uw website bevinden.

## Banners {#concept_5BBE01FEC6134393B43CC917C8CC64DA} gebruiken

<!-- 

c_about_banners.xml

 -->

U kunt twee methoden gebruiken om banneradvertenties aan uw website toe te voegen.

De eerste methode is banners als Doel toe te voegen, Search&amp;Promote. De banners zijn HTML-codefragmenten die worden weergegeven op het moment dat een klant uw website doorzoekt. Uw banner kan tekst of een afbeelding in GIF-, JPEG- of PNG-indeling of een combinatie van beide bevatten. U kunt kiezen uit vooraf ingestelde grootten of uw eigen aangepaste afmetingen definiëren die op uw pagina passen. Met de HTML-code die u gebruikt om de banner weer te geven, kunt u bijvoorbeeld de lettertypestijl en de rand opgeven. Deze methode om een banner toe te voegen biedt basisfunctionaliteit en vereist geen extra software.

De tweede methode is het gebruik van Adobe Dynamic Media Classic, een dynamisch mediabeheer en publicatieservice. Met een geldig Adobe Dynamic Media Classic-account kunt u bannerinhoud rechtstreeks aan Target, Search&amp;Promote, beheren en leveren met gebruik van Dynamic Media Classic. Bij het zoeken/verhandelen van sites configureert u toegang tot uw Dynamic Media Classic-account. Vervolgens opent u de Dynamic Media Classic-mediabrowser en kiest u een dynamisch mediabestand dat u als banner wilt gebruiken.

>[!NOTE]
>
>Voordat u dynamische media-elementen kunt gebruiken als banners bij het zoeken/verhandelen van sites, worden de elementen eerst geüpload en voorbereid voor publicatie in het Scene7 Publishing System. U kunt elementen uploaden vanuit de zoekfunctie/merchandising op de site en deze automatisch laten voorbereiden voor publicatie door het Scene7 Publishing System. U kunt ook elementen uploaden en publiceren vanuit het Scene7 Publishing System.

## Integratie van banners met Adobe Scene7 Publishing System {#section_D4D7ADEA6A6348E68EDA138E184FE579}

U kunt Klassieke Dynamic Media-elementtypen gebruiken als banners bij het zoeken/verhandelen van sites, zoals afbeeldingen, dynamische banners en sjablonen, zoals afbeeldingssjablonen of Flash-sjablonen.

Sjablonen worden dynamisch gemaakt en adresseerbare gelaagde afbeeldingsbestanden, zoals gelaagde bestanden, in beeldbewerkingstoepassingen zoals Adobe Photoshop®. In tegenstelling tot een statisch afbeeldingsbestand kan een sjabloon parameters bevatten. Aan de hand van parameters kunt u de eigenschappen van een variabele afbeelding en de inhoud van de afbeelding aanpassen.

>[!NOTE]
>
>U kunt ook sjablonen maken op basis van lay-outontwerpen met behulp van Sjabloonpublicatie in Scene7 Publishing System en bestanden uit Adobe Illustrator en Adobe InDesign.

Zie [Sjabloonpublicatie](https://help.adobe.com/en_US/scene7/using/WSFBFBAD30-2694-4b18-B7CE-894F9FC5CDDF.html) in de Dynamic Media Classic (Scene7) User Guide.

Een sjabloon kan een willekeurig aantal afbeeldingslagen en tekstlagen bevatten. U kunt een statisch bestand met lagen, zoals een gelaagd PSD-bestand, converteren naar een sjabloon of sjablonen maken in Dynamic Media Classic. U kunt tekstlagen in sjablonen maken met lettertypen die u naar het Scene7 Publishing System hebt geüpload. Nadat u tekst aan een sjabloon hebt toegevoegd, kunt u deze opmaken door de uitvulling, lettertypen, tekengrootte en kleur ervan te wijzigen.

Met het scherm Parameters in Dynamic Media Classic kunt u elk aspect van een sjabloon omzetten in een adresseerbare parameter. Op deze manier kunt u wijzigen welke gelaagde afbeelding moet worden gebruikt of welke tekstwaarde in de sjabloon moet worden gebruikt. De parameters worden overgegaan met het koord URL, toestaand u om het even welke parameter te veranderen om het antwoordbeeld dynamisch aan te passen dat van de beeldserver wordt geproduceerd.

U kunt meer leren over hoe u Dynamic Media Classic kunt gebruiken om sjablonen te maken en de parameters van de eigenschappen op de lagen te bepalen, zodat u deze in banners kunt gebruiken.

Zie [Sjabloonbeginselen](https://help.adobe.com/en_US/scene7/using/WS60B68844-9054-4099-BF69-3DC998A04D3C.html) in de Dynamic Media Classic (Scene7) User Guide.

**Uploaden en publiceren van middelen**

U moet middelen in Dynamic Media Classic uploaden en publiceren alvorens u hen voor banners in plaatsonderzoek/koophandel kunt gebruiken. Deze voorwaarde geldt ook voor alle elementen die een afbeeldingssjabloon of een Flash-sjabloon gebruikt. Gebruik uw Dynamic Media Classic-account om digitale middelen te uploaden en te publiceren. Of u kunt zoeken naar of winkelen op de site gebruiken om een digitaal middel te uploaden en het vervolgens automatisch door Dynamic Media Classic laten publiceren op basis van uw uploadinstellingen. Als u een element probeert te kiezen dat nog niet is geüpload en gepubliceerd, wordt u hiervan op de hoogte gesteld in de gebruikersinterface en krijgt u de mogelijkheid om het te uploaden voordat u verdergaat.

Meer informatie over het uploaden en publiceren van digitale elementen via het Scene7 Publishing System vindt u op de website.

Zie [Elementen uploaden en publiceren](https://help.adobe.com/en_US/scene7/using/WS3673AD39-098B-4f08-8A24-CA51261B7366.html) in de Dynamic Media Classic (Scene7) gebruikershandleiding.

>[!NOTE]
>
>Als u de uploadfunctionaliteit wilt gebruiken in de Dynamic Media Classic Asset Viewer, moet u ervoor zorgen dat de rol &quot;SPS Company Admin&quot; al is ingesteld op het Klassieke Dynamic Media-account dat u gebruikt.

Zie [Beheerinstellingen](https://help.adobe.com/en_US/scene7/using/WS662101DF-D697-47a7-A7D8-B52FD8E94438.html) in de Dynamic Media Classic (Scene7) User Guide.

**Dynamic Media Classic Template Parameters in een Banner wijzigen met Business Rules**

Als u een dynamisch Media Classic element als een banner hebt toegevoegd, kunt u [!DNL Visual Rule Builder] in [!DNL Business Rules] gebruiken om het aan een bannergebied op uw website toe te voegen. U voegt bijvoorbeeld de banner toe aan de pagina&#39;s met zoekresultaten, net als bij andere banners. U kunt de standaardparameterwaarden in de Klassieke malplaatjes van Dynamic Media ook met voeten treden door hen aan uw specifieke behoeften aan te passen. Met dit soort functionaliteit kunt u Klassieke Dynamic Media-sjablonen aanpassen met verschillende marketingberichten en hyperlinks naar verschillende eindpunten.

Zie ook [Een nieuwe bedrijfsregel toevoegen](../c-about-rules-menu/c-about-business-rules.md#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7).

Zie ook [Een bedrijfsregel bewerken](../c-about-rules-menu/c-about-business-rules.md#task_375CFA75D1D94D9E92A35DE1228E5087).

## Een banner {#task_549D02B5F73B4158B105A94E39D937B7} toevoegen

Met [!DNL Banners] kunt u de banneradvertenties beheren en bepalen waar deze op uw website worden geplaatst. Wanneer u een banner toevoegt, verwijst u extern naar de afbeelding door middel van HTML-codefragmenten die tijdens het zoeken worden weergegeven.

<!-- 

t_adding_a_new_banner.xml

 -->

Als u een geldig Adobe Dynamic Media Classic-account hebt, kunt u banneradvertenties toevoegen via het Scene7 Publishing System.

Zie [Een banner toevoegen met Adobe Dynamic Media Classic](../c-about-design-menu/c-about-banners.md#task_AD1E0C00A9E04B1FA819EB93288786B3).

Zie [Toegang tot uw Adobe Dynamic Media Classic-account configureren](../c-about-settings-menu/c-about-account-options-menu.md#task_CEFF88C2033D41D0B2FE86C435EDAC6D).

**Een banner toevoegen**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Banners]**.
1. Selecteer **[!UICONTROL HTML code]** op de pagina [!DNL Banners] in de vervolgkeuzelijst **[!UICONTROL Add Banner]**.
1. Stel in het dialoogvenster [!DNL Add Banner] de gewenste opties in.

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
      <td colname="col2"> <p>Vereist. Hiermee wordt de naam van uw banner aangegeven. De naam wordt gebruikt om naar de banner te verwijzen wanneer u het in de Visuele Bouwer van de Regel in BedrijfsRegels toevoegt. De naam wordt niet weergegeven in de banner zelf. </p> <p>Zie <a href="../c-about-rules-menu/c-about-business-rules.md#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7" type="task" format="dita" scope="local"> Een nieuwe bedrijfsregel toevoegen.</a> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Banner-HTML </p> </td> 
      <td colname="col2"> <p> Hiermee kunt u de HTML-code plakken die aan de banner is gekoppeld. </p> <p>Elke HTML-code is acceptabel, inclusief CSS-code die wordt omringd door 
        <code>
          &lt;style&gt; 
        </code>-tags of JavaScript-code die wordt omgeven door 
        <code>
          &lt;script&gt; 
        </code>-tags. Het volgende codeblok is bijvoorbeeld voor een tekstbanner van het type Horizontal top: <code> &lt;div&nbsp;style="width:&nbsp;684px;&nbsp;background-image:&nbsp;url('https://www.brough.com/blackb.gif');&nbsp; 
          padding-top:&nbsp;10px;&nbsp;padding-bottom:&nbsp;10px;&nbsp;color:&nbsp;white;&nbsp;font-family:&nbsp;verdana;&nbsp; 
          text-align:&nbsp;center;&nbsp;font-size:&nbsp;20px;"&gt;&nbsp;Sound&nbsp;Study&nbsp;ships&nbsp;free!&nbsp;&lt;/div&gt; </code>In het volgende voorbeeld is het codeblok voor een volledige welkomstafbeelding: <code> &lt;img&amp;nbsp;src='https://geometrixx.com/images/GEOAds/geometrixx-beauty-home-01.jpg'&amp;nbsp;border="0"&amp;nbsp;/&gt; </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Type </p> </td> 
      <td colname="col2"> <p>Hiermee geeft u de volgende typen banners op: 
        <ul id="ul_6423AEDB9E664049989EB529D63C4A62"> 
          <li id="li_BF6CD60B3ED748D49CFFB9C5D607661C"> <span class="uicontrol"> [nieuw type]  </span> <p>Hier kunt u het gewenste type banner opgeven, inclusief de afmetingen en de naam. </p> </li> 
          <li id="li_1A29AB22AD644E60A12298187B5E898E"> <span class="uicontrol"> Volledige splash  </span> <p>De ingestelde afmeting van dit type banner is 680 pixels breed en 650 pixels hoog. U kunt optioneel de naam van het type opgeven of de standaardnaam accepteren die de naam is van het bannertype zelf. </p> </li> 
          <li id="li_2BE06D013CB54DDE851051BFC038BB57"> <span class="uicontrol"> Horizontaal boven  </span> <p> De banner wordt in het bovenste gebied van uw website geplaatst. Dit type is handig als u hyperlinks links links of rechts van de banner wilt toevoegen. De ingestelde afmeting van dit type banner is 468 pixels breed en 60 pixels hoog. U kunt optioneel de naam van het type opgeven of de standaardnaam accepteren die de naam is van het bannertype zelf. </p> </li> 
          <li id="li_EC35AB92234749F08AA8A9BD26D0EA8D"> <span class="uicontrol"> Horizontaal boven - Volledige breedte  </span> <p>Dit type is het standaardtype wanneer u een nieuwe banner toevoegt. De banner wordt over het bovenste gebied van uw website geplaatst en neemt de volledige breedte van de pagina in beslag. De ingestelde afmeting van dit type banner is 670 pixels breed en 150 pixels hoog. U kunt optioneel de naam van het type opgeven of de standaardnaam accepteren die de naam is van het bannertype zelf. </p> </li> 
        </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Tags </p> </td> 
      <td colname="col2"> <p>Hiermee voegt u tags of trefwoorden toe die u aan de banner wilt koppelen. Als u veel banners gebruikt, kunt u door tags toe te voegen uw bannerzoekopdracht verfijnen, zodat u snel alleen de juiste banner kunt vinden. U kunt ook alle tags verwijderen die u hebt toegevoegd. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Klik op **[!UICONTROL Save]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een banner {#task_D4081083BE7B40F5A003D1A2F1435AEA} bewerken

Gebruik [!DNL Edit Banner] om zaken zoals de bannernaam, banner HTML, het bannertype, en om het even welke bijbehorende markeringen te veranderen.

<!-- 

t_editing_a_banner.xml

 -->

Als u een banner hebt toegevoegd met de functie voor zoeken/winkelen op de site, kunt u de banner ook bewerken met Adobe Dynamic Media Classic.

Zie ook [Een banner bewerken met Adobe Dynamic Media Classic](../c-about-design-menu/c-about-banners.md#task_C3E782477FBF428ABEA220751781ACA9).

**Een banner bewerken**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Banners]**.
1. Klik op [!DNL Banners] op de pagina.![](assets/icon_edit_16.gif)

   boven een bannerminiatuur die u wilt bewerken.
1. Stel op de pagina [!DNL Edit Banner] de gewenste opties in.

   Zie de optietabel onder [Een banner toevoegen](../c-about-design-menu/c-about-banners.md#task_549D02B5F73B4158B105A94E39D937B7).
1. Wanneer u klaar bent met het bewerken van de banner, klikt u op **[!UICONTROL Save]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een banner toevoegen met Adobe Dynamic Media Classic {#task_AD1E0C00A9E04B1FA819EB93288786B3}

Met [!DNL Banners] kunt u de banneradvertenties op uw website beheren. Wanneer u een banner toevoegt met Adobe Dynamic Media Classic, kunt u kiezen uit alle digitale elementen die u naar het Scene7 Publishing System hebt geüpload.

<!-- 

t_adding_a_banner_using_adobe_scene7.xml

 -->

Als u een banner wilt toevoegen met Adobe Dynamic Media Classic, moet u ervoor zorgen dat u toegang tot uw geldige Dynamic Media Classic-account hebt geconfigureerd.

Zie [Toegang tot uw Adobe Dynamic Media Classic-account configureren](../c-about-settings-menu/c-about-account-options-menu.md#task_CEFF88C2033D41D0B2FE86C435EDAC6D).

**Een banner toevoegen met Adobe Dynamic Media Classic**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Banners.]**
1. Klik op de pagina [!DNL Banners] in de vervolgkeuzelijst **[!UICONTROL Add Banner]** op **[!UICONTROL Adobe Scene7]**.
1. In het [!DNL Pick an Asset] dialoogvakje, in de linkerruit, gebruik de navigatieopties in het gebruikersinterface om van de omslag de plaats te bepalen die de digitale activa bevat die u voor een banner wilt gebruiken.

   Met uitzondering van de opties voor middelennavigatie zijn alle andere opties afhankelijk van het digitale element dat u hebt geselecteerd om toe te voegen of te bewerken.

   Gebruik de opties voor middelennavigatie om te zoeken naar een element dat u voor een nieuwe banner wilt gebruiken in het zoeken/verhandelen van sites. De navigatieopties zijn van toepassing op alle typen geselecteerde digitale elementen.

   >[!NOTE]
   >
   >De opties voor elementnavigatie worden niet weergegeven wanneer u de banner bewerkt in het dialoogvenster [!DNL Change Parameters].

   Zie [Een banner bewerken met Adobe Dynamic Media Classic](../c-about-design-menu/c-about-banners.md#task_C3E782477FBF428ABEA220751781ACA9).

   **Opties voor middelennavigatie**

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Navigatie, optie </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/S7_folders.png"> </p> </td> 
      <td colname="col2"> <p>Hiermee kunt u het Dynamic Media Classic-account voor uw specifieke bedrijf selecteren in de vervolgkeuzelijst en ook door de mappen met digitale middelen in dat account navigeren. </p> <p>Wanneer u een map selecteert, worden in het rechterdeelvenster van het dialoogvenster <span class="wintitle"> Een element kiezen </span> alle beschikbare digitale elementen weergegeven die zich in die map bevinden. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_folderhistory.png"> </p> </td> 
      <td colname="col2"> <p>Hiermee kunt u de navigatiegeschiedenis van de map vooruit of achteruit doorlopen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_reloadfolder.png"> </p> </td> 
      <td colname="col2"> <p>Hiermee vernieuwt u de lijst met digitale elementen die voor een geselecteerde map worden weergegeven. </p> <p>Mogelijk moet u op dit besturingselement klikken als u een geselecteerd element verplaatst, verwijdert of hernoemt met de vervolgkeuzelijst <span class="uicontrol"> Handelingen </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_list_or_grid.png"> </p> </td> 
      <td colname="col2"> <p>Hiermee geeft u digitale elementen weer in een lijstweergave. In de lijst staan het pictogram of de miniatuurafbeelding van elk element, de bestandsnaam, het type digitaal element, de afmetingen (indien van toepassing) en de datum waarop het voor het laatst is bewerkt. </p> <p>In de rasterweergave worden digitale elementen in de geselecteerde map weergegeven als pictogrammen, miniaturen of beide. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_actionsdropdown.png"> </p> </td> 
      <td colname="col2"> <p>In de lijstweergave kunt u een geselecteerd digitaal element verplaatsen, verwijderen of hernoemen. </p> <p>In de rasterweergave kunt u een of meer geselecteerde digitale elementen verplaatsen of verwijderen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_upload.png"> </p> </td> 
      <td colname="col2"> <p>Hiermee opent u het dialoogvenster <span class="wintitle"> </span> uploaden om een geselecteerd digitaal element van uw bureaublad of van een externe server te uploaden, zodat u het als een banner kunt gebruiken. </p> <p>Nadat u het element hebt geüpload, wordt er automatisch een publicatietaak voor u gepland in Scene7 Publishing System. </p> <p>Zie de optietabel in <a href="../c-about-design-menu/c-about-banners.md#task_AD1E0C00A9E04B1FA819EB93288786B3" type="reference" format="dita" scope="local"> Een banner toevoegen met Adobe Dynamic Media Classic </a>. </p> <p>Meer informatie over het uploaden en publiceren van digitale elementen via het Scene7 Publishing System vindt u op de website. </p> <p>Zie <a href="https://help.adobe.com/en_US/scene7/using/WS3673AD39-098B-4f08-8A24-CA51261B7366.html" scope="external" format="html"> Elementen uploaden en publiceren </a> in de gebruikershandleiding van het Scene7 Publishing System. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_searchfield.png"> </p> </td> 
      <td colname="col2"> <p>Hiermee kunt u naar een digitaal element zoeken op trefwoord of op bestandslocatie zoeken in de geselecteerde map en de bijbehorende submappen. </p> <p>Wanneer u op het zoekveld klikt, wordt automatisch een optioneel filterveld voor u toegevoegd. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_addfilter.png"> </p> </td> 
      <td colname="col2"> <p>Hiermee voegt u een ander elementfilter toe, zodat u de lijst met weergegeven digitale elementen verder kunt verfijnen op type of op een bepaalde datum. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_Kindfilter.png"> </p> </td> 
      <td colname="col2"> <p>Verfijn de lijst met weergegeven digitale elementen om alleen die van een bepaald type weer te geven, zoals Flash, Afbeelding, Sjabloon of Willekeurig. </p> <p>Klik <img src="assets/s7_deletefilter.png"> om de filter van het onderzoek te schrappen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_datefilter.png"> </p> </td> 
      <td colname="col2"> <p>Verfijn de lijst met weergegeven digitale elementen om alleen die te tonen die vóór een bepaalde datum of na een bepaalde datum zijn gemaakt of bewerkt. </p> <p>Klik <img src="assets/s7_deletefilter.png" /> om de filter van het onderzoek te schrappen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_assetzoom.png"> </p> </td> 
      <td colname="col2"> <p>Hiermee kunt u de schuifregelaar naar links of rechts slepen om respectievelijk de volledige weergave van het deelvenster met digitale elementen te verkleinen of te vergroten. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **Eigenschappen, opties**

   De opties van Eigenschappen verschijnen als u een Flash malplaatje, beeldmalplaatje, of een beeld koos. Afhankelijk van het digitale element dat u hebt gekozen, zijn niet alle opties beschikbaar.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Eigenschappen, optie </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Naam </p> </td> 
      <td colname="col2"> <p>De beschrijvende naam van de sjabloon of afbeelding, zonder spaties. U kunt desgewenst de specificatie voor de afbeeldingsgrootte in de naam opnemen om gebruikers te helpen het element beter te identificeren. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Indeling </p> </td> 
      <td colname="col2"> <p>Hiermee geeft u de indeling van de afbeelding of afbeeldingssjabloon aan. </p> <p>U kunt kiezen uit de volgende indelingen: </p> 
        <ul id="ul_9A19421BCC424CF585645049DCB87F10"> 
        <li id="li_A4913D783BD547F9AFA1A259C56EC2B3">jpeg </li> 
        <li id="li_66237D7BE8754FB0B0088CE5A02C0214">png </li> 
        <li id="li_4EDDFD7C8AB04677BEC20EFC9AEBBF1F">png-alpha </li> 
        <li id="li_4FCB03C29AE647ACBAF5105016DF7579">gif </li> 
        <li id="li_B884BD7DFF1845FAA9C58EF09B888A77">gif-alpha </li> 
        </ul> <p>Deze optie is niet van toepassing op Flash-sjablonen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Kwaliteit </p> </td> 
      <td colname="col2"> <p>Hiermee bepaalt u het compressieniveau van JPEG- of GIF-afbeeldingen. Deze instelling is van invloed op zowel de bestandsgrootte als de afbeeldingskwaliteit. De kwaliteitsschaal is 1-100. </p> <p>Wanneer u de schuifregelaar naar links of rechts sleept, wordt de afbeelding in het voorvertoningsvenster bijgewerkt met de kwaliteitswijziging. </p> <p>Deze optie is niet van toepassing op Flash-sjablonen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Breedte </p> </td> 
      <td colname="col2"> <p>Hiermee geeft u de breedte van het digitale element op, in pixels. Deze dimensie is de breedte waarmee het middel wordt bekeken door klanten die uw website bezoeken. </p> <p>Deze optie is niet van toepassing op Flash-sjablonen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Hoogte </p> </td> 
      <td colname="col2"> <p>Hiermee geeft u de hoogte van het digitale element op, in pixels. Deze dimensie is de hoogte waarop het middel wordt gezien door klanten die uw website bezoeken. </p> <p>Deze optie is niet van toepassing op Flash-sjablonen. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **Opties voor bannerkoppeling**

   De opties voor bannerkoppeling worden alleen weergegeven als u een afbeelding of een afbeeldingssjabloon voor uw banner hebt gekozen.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Bannerkoppeling, optie </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Koppelings-URL </p> </td> 
      <td colname="col2"> <p>Hiermee geeft u het URL-adres op waarnaar de banner moet worden gekoppeld wanneer een klant op de afbeelding klikt. </p> <p>Laat het veld URL koppelen leeg als u niet wilt dat de banner een koppeling tot stand brengt. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Doel </p> </td> 
      <td colname="col2"> <p>Geeft aan waar de gekoppelde banner moet worden geopend, zoals een nieuw browservenster of een nieuw tabblad. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **Koppelingen wijzigen, optie**

   De optie Koppelingen wijzigen wordt alleen weergegeven als u een Flash-sjabloon voor de banner hebt gekozen.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Koppelingen wijzigen, optie </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p> <img placement="inline" id="image_EBB8159690C74D4692B5DF945B045E0B" src="assets/icon_edit_16.gif" /> </p> </td> 
      <td colname="col2"> <p>Hiermee kunt u het veld URL-koppeling bewerken dat wordt gebruikt in de sjabloon Flash. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **Opties voor Tekst vervangen**

   De opties voor Tekst vervangen worden alleen weergegeven als u een Flash-sjabloon kiest voor uw banner die bewerkbare tekstlagen heeft.

   Wijzigingen die u aanbrengt in tekst in de sjabloon Flash, worden weergegeven in het voorvertoningsvenster.

   >[!NOTE]
   >
   >Als u een zoek- en vervangopdracht toevoegt om &quot;koe&quot; te vervangen door &quot;appel&quot; en vervolgens een tweede opdracht maakt om &quot;appel&quot; te vervangen door &quot;oranje&quot;, heeft de tweede opdracht geen invloed.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Tekst vervangen, optie </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_addfilter.png"> </p> </td> 
      <td colname="col2"> <p>Hiermee voegt u een veld voor zoeken en vervangen toe. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_deletefilter.png"> </p> </td> 
      <td colname="col2"> <p>Hiermee verwijdert u een veld Zoeken en vervangen en herstelt u de eerder gebruikte tekst. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Zoeken </p> </td> 
      <td colname="col2"> <p>Hiermee kunt u een zoekterm voor niet-gekoppelde tekst invoeren in de lagen van de Flash-sjabloon. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Vervangen </p> </td> 
      <td colname="col2"> <p>Hier kunt u de tekst opgeven die u wilt invoegen in plaats van de tekst waarnaar u zoekt. </p> <p>Wanneer u in dit veld op <span class="uicontrol"> Enter </span> drukt, wordt het voorvertoningsvenster bijgewerkt met de vervangende tekst. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **Parameters, opties**

   Parameters worden alleen weergegeven als u een afbeeldingssjabloon of een Flash-sjabloon voor de banner hebt gekozen. De daadwerkelijke parameteropties variëren afhankelijk van hoe het malplaatje in het Uitgevers Systeem van Scene7 werd gecreeerd en werd bepaald. In uw sjabloon kunnen bijvoorbeeld velden met parameters worden ingesteld waarmee u tekst, lettertypestijl, prijs, speciale codes voor gratis verzending, de grootte van de afbeelding binnen de banner kunt wijzigen of zelfs naar een andere afbeelding kunt bladeren.

   >[!NOTE]
   >
   >Houd er rekening mee dat wijzigingen die u aanbrengt in parameters kunnen worden overschreven door bedrijfsregels. De parameters dienen slechts als gebreken wanneer geen bedrijfsregels worden gecreeerd die anders de parameters zouden veranderen.

   Zie [Een nieuwe bedrijfsregel toevoegen](../c-about-rules-menu/c-about-business-rules.md#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7).

   Zie [Een bedrijfsregel bewerken](../c-about-rules-menu/c-about-business-rules.md#task_375CFA75D1D94D9E92A35DE1228E5087).

   **Zichtbaarheidsopties laag in-/uitschakelen**

   De optie Laagzichtbaarheid in-/uitschakelen is alleen van toepassing als u een Flash-sjabloon voor de banner hebt gekozen.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Zichtbaarheid laag in-/uitschakelen, optie </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_togglelayervisibility.png"> </p> </td> 
      <td colname="col2"> <p>Hiermee kunt u de zichtbaarheid van de verschillende lagen waaruit het sjabloonbestand voor Flash bestaat in- of uitschakelen. </p> <p>Telkens wanneer u de zichtbaarheid van een laag in- of uitschakelt, wordt het voorvertoningsvenster vernieuwd om de weergave bij te werken. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   (Optioneel) Als het digitale element dat u voor een banner wilt gebruiken niet beschikbaar is in de geselecteerde map, moet u het wellicht uploaden. Klik op **[!UICONTROL Upload]** en selecteer het gewenste bestand en de gewenste opties. Het bestand wordt geüpload naar de geselecteerde map.

   >[!NOTE]
   >
   >Als u de uploadfunctionaliteit wilt gebruiken in de Scene7 Asset Viewer, moet u ervoor zorgen dat de rol van &quot;SPS Company Admin&quot; al is ingesteld voor de Scene7-account die u gebruikt.

   Zie [Beheerinstellingen](https://help.adobe.com/en_US/scene7/using/WS662101DF-D697-47a7-A7D8-B52FD8E94438.html) in de gebruikershandleiding van het Scene7 Publishing System.

   **Basisopties**

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Bladeren </p> </td> 
      <td colname="col2"> <p> Hiermee kunt u bladeren naar het bestand dat u wilt uploaden, publiceren en vervolgens selecteren voor gebruik als banner. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Overschrijven </p> </td> 
      <td colname="col2"> <p>Bestanden die u uploadt, vervangen bestaande bestanden met dezelfde bestandsnaam in de geselecteerde map. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>E-mailvoorkeur </p> </td> 
      <td colname="col2"> <p> Hiermee kunt u kiezen welk e-mailbericht u ontvangt voor het uploaden, of u kunt ervoor kiezen om geen melding te ontvangen voor iets dat betrekking heeft op de uploadtaak. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **Geavanceerde opties**

   Wanneer u PostScript- (EPS) of Illustrator-afbeeldingsbestanden (AI) uploadt, kunt u deze op verschillende manieren opmaken. U kunt de bestanden rasteren, omzetten in FXG voor Sjabloonpublicatie, de transparante achtergrond behouden, een resolutie kiezen en een kleurruimte kiezen.

   PSD (Photoshop Document files) worden meestal gebruikt in Dynamic Media Classic om sjablonen te maken. Wanneer u een PSD-bestand uploadt, kunt u automatisch een klassieke Dynamic Media-sjabloon maken vanuit het bestand (selecteer de optie **[!UICONTROL Create Template]**).

   Scene7 Publishing System maakt meerdere afbeeldingen van een PSD-bestand met lagen als u het bestand gebruikt om een sjabloon te maken. er wordt één afbeelding voor elke laag gemaakt.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Naam van instellingengroep </p> </th> 
      <th colname="col02" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Opties voor kleurprofiel </p> </td> 
      <td colname="col02"> <p>Kleurprofiel </p> </td> 
      <td colname="col2"> <p> Hiermee kunt u uit de volgende opties kiezen: </p> 
        <ul id="ul_6927BC08CA2647EDB2C85DAD2B82AE31"> 
        <li id="li_CA3F44FF9C0F4CE987DCB0AF9303C2E4"> <span class="uicontrol"> Omzetten in SRGB  </span> <p>Converteert naar SRGB (standaard rood-groen blauw). SRGB is de aanbevolen kleurruimte voor het weergeven van afbeeldingen op webpagina's. </p> </li> 
        <li id="li_FCCEE6B14CCD4246ADA152932010ABF1"> <span class="uicontrol"> Oorspronkelijke kleurruimte behouden  </span> <p>Behoudt de oorspronkelijke kleurruimte. </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Beeldbewerkingsopties </p> </td> 
      <td colname="col02"> <p>Masker maken van uitknippad </p> </td> 
      <td colname="col2"> <p>Maak een masker voor de afbeelding op basis van de gegevens over het uitknippad. Deze optie is van toepassing op afbeeldingen die zijn gemaakt met beeldbewerkingstoepassingen waarin een uitknippad is gemaakt. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>PostScript-opties </p> <p>Illustrator-opties </p> </td> 
      <td colname="col02"> <p>Verwerking </p> </td> 
      <td colname="col2"> <p> <span class="uicontrol"> Met de  </span> optie Rasteren zet u vectorafbeeldingen in het bestand om in de bitmapindeling. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> PostScript-opties </p> <p>Illustrator-opties </p> </td> 
      <td colname="col02"> <p> Resolutie </p> </td> 
      <td colname="col2"> <p> Hiermee bepaalt u de resolutie-instelling. Deze instelling bepaalt hoeveel pixels per inch in het bestand worden weergegeven. De standaardwaarde is 150. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> PostScript-opties </p> <p>Illustrator-opties </p> </td> 
      <td colname="col02"> <p> Kleurruimte </p> </td> 
      <td colname="col2"> <p>Hiermee kunt u een kleurruimte kiezen voor het Illustrator-bestand. De RGB-kleurruimte heeft de voorkeur voor onlineweergave. </p> <p>U kunt uit de volgende opties voor kleurruimte kiezen: </p> 
        <ul id="ul_0E83E2762A574480B243F963A7FB2ACD"> 
        <li id="li_B9FEC7D220D04CCABACD30839051DAE4"> <span class="uicontrol"> Automatisch detecteren  </span> <p> Hiermee behoudt u de kleurruimte van het PDF-bestand. </p> </li> 
        <li id="li_ED0EB3B12BCF41C7AFC435447010B6FF"> <span class="uicontrol"> Als RGB forceren  </span> <p> Zet om in de RGB-kleurruimte. </p> </li> 
        <li id="li_3FB5DD8887C540BC97148A4D63B38F72"> <span class="uicontrol"> Krachten als CMYK  </span> <p> Zet om in de CMYK-kleurruimte. </p> </li> 
        <li id="li_6C018D3A4B254880AD41896E9F4AF3D9"> <span class="uicontrol"> Krachtig maken als grijswaarden  </span> <p> Zet om in de grijswaardenkleurruimte. </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> PostScript-opties </p> <p>Illustrator-opties </p> </td> 
      <td colname="col02"> <p> Transparante achtergrond behouden </p> </td> 
      <td colname="col2"> <p>Hiermee blijft de achtergrondtransparantie van het bestand behouden. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Photoshop-opties </p> </td> 
      <td colname="col02"> <p> Lagen behouden </p> </td> 
      <td colname="col2"> <p>Hiermee worden de lagen in de PSD (indien aanwezig) naar afzonderlijke elementen verplaatst. De elementlagen blijven gekoppeld aan de PSD. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Photoshop-opties </p> </td> 
      <td colname="col02"> <p>Sjabloon maken </p> </td> 
      <td colname="col2"> <p> Hiermee maakt u een sjabloon op basis van de lagen in het PSD-bestand. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Photoshop-opties </p> </td> 
      <td colname="col02"> <p> Tekst extraheren </p> </td> 
      <td colname="col2"> <p> Extraheert de tekst zodat klanten naar trefwoorden in een banner kunnen zoeken. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Photoshop-opties </p> </td> 
      <td colname="col02"> <p> Lagen uitbreiden </p> </td> 
      <td colname="col2"> <p>Hiermee vergroot u de grootte van de uitgesneden afbeeldingslagen tot de grootte van de achtergrondlaag. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Photoshop-opties </p> </td> 
      <td colname="col02"> <p> Laagnaamgeving </p> </td> 
      <td colname="col2"> <p>Lagen in het PSD-bestand worden geüpload als afzonderlijke afbeeldingen. U kunt uit de volgende opties kiezen om te bepalen hoe u deze afbeeldingen in het Scene7 Publishing System een naam wilt geven: </p> 
        <ul id="ul_C2A25177A07740CA90B32C638304D39F"> 
        <li id="li_477D5BFF7238454BBF0E04B22DE378F7"> <span class="uicontrol"> Laagnaam uit PSD-bestand gebruiken  </span> <p>De afbeeldingen krijgen een naam na de namen van de lagen in het PSD-bestand. Een laag met de naam <span class="codeph"> Prijstag </span> in het oorspronkelijke PSD-bestand wordt bijvoorbeeld een afbeelding met de naam <span class="codeph"> Prijscode </span>. Als de laagnamen in het PSD-bestand echter standaard Photoshop-laagnamen zijn (Achtergrond, Laag 1, Laag 2, enzovoort), krijgen de afbeeldingen een naam na hun laagnummers in het PSD-bestand, niet na hun standaardlaagnamen. </p> </li> 
        <li id="li_EB4173B884FC41328CFBDE27DA6D43AA"> <span class="uicontrol"> PSD-bestandsnaam en -bijvoegnummer gebruiken  </span> <p>De afbeeldingen krijgen een naam na hun laagnummer in het PSD-bestand, waarbij de namen van de oorspronkelijke lagen worden genegeerd. Afbeeldingen krijgen de naam Photoshop en een toegevoegd laagnummer. De tweede laag van een bestand met de naam <span class="codeph"> Spring Ad.psd </span> krijgt bijvoorbeeld de naam <span class="codeph"> Spring Ad_2 </span>, zelfs als het bestand een niet-standaardnaam had in Photoshop. </p> </li> 
        <li id="li_10B2D2DE2FD24BD08DB56D1D95ABA53D"> <span class="uicontrol"> PSD-bestandsnaam en -naam of -nummer gebruiken  </span> <p>De afbeeldingen krijgen een naam na het PSD-bestand, gevolgd door de laagnaam of het laagnummer. Het laagnummer wordt gebruikt als de laagnamen in het PSD-bestand standaard Photoshop-laagnamen zijn. Een laag met de naam <span class="codeph"> Price Tag </span> in een PSD-bestand met de naam <span class="codeph"> SpringAd </span> krijgt bijvoorbeeld de naam <span class="codeph"> Spring Ad_Price Tag </span>. Een laag met de standaardnaam <span class="codeph"> Laag 2 </span> wordt genoemd <span class="codeph"> Lente Ad_2 </span>. </p> </li> 
        <li id="li_5E57AC0719D4484B9C9BD14DB42B4455"> <span class="uicontrol"> Map maken op basis van de PSD-bestandsnaam  </span> <p>Hiermee maakt u een map voor de laagafbeeldingen met de bestandsnaam van de PSD. </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Photoshop-opties </p> </td> 
      <td colname="col02"> <p>Anker </p> </td> 
      <td colname="col2"> <p>Geef op hoe afbeeldingen worden verankerd in sjablonen die worden gegenereerd op basis van de laagcompositie die uit het PSD-bestand is samengesteld. </p> <p>Standaard is het anker het middelpunt. Met een middelste anker kunnen vervangende afbeeldingen dezelfde ruimte het beste vullen, ongeacht de hoogte-breedteverhouding van de vervangende afbeelding. Afbeeldingen met een ander aspect dat deze afbeelding vervangt, nemen bij het verwijzen naar de sjabloon en het gebruik van parametervervanging in feite dezelfde ruimte in. Schakel over naar een andere instelling als de vervangende afbeeldingen de toegewezen ruimte in de sjabloon moeten vullen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>PDF-opties </p> </td> 
      <td colname="col02"> <p>Verwerking </p> </td> 
      <td colname="col2"> <p> <span class="uicontrol"> Met de  </span> optie Rasteren worden de pagina's in het PDF-bestand gewist en worden vectorafbeeldingen naar bitmapafbeeldingen geconverteerd.  
        <!--Choose this option to create an eCatalog. (This option is thedefault.)--> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>PDF-opties </p> </td> 
      <td colname="col02"> <p> Resolutie </p> </td> 
      <td colname="col2"> <p>Hiermee bepaalt u de resolutie-instelling. Deze instelling bepaalt hoeveel pixels per inch in het PDF-bestand worden weergegeven. De standaardwaarde is 150. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>PDF-opties </p> </td> 
      <td colname="col02"> <p> Kleurruimte </p> </td> 
      <td colname="col2"> <p>Hiermee kunt u een kleurruimte kiezen voor het PDF-bestand. De meeste PDF-bestanden hebben zowel RGB- als CMYK-kleurenafbeeldingen. De RGB-kleurruimte heeft de voorkeur voor onlineweergave. </p> <p>U kunt uit de volgende opties voor kleurruimte kiezen: </p> 
        <ul id="ul_44A8C39DEB21473F9375E3962F14D3C6"> 
        <li id="li_1046FA0017934C5EB7C0100F8F78507D"> <span class="uicontrol"> Automatisch detecteren  </span> <p> Hiermee behoudt u de kleurruimte van het PDF-bestand. </p> </li> 
        <li id="li_561CCF705EDD451993D2DA2EB33F05F7"> <span class="uicontrol"> Als RGB forceren  </span> <p> Zet om in de RGB-kleurruimte. </p> </li> 
        <li id="li_D9E8CF61C40140979484EDEF7DAD2C44"> <span class="uicontrol"> Krachten als CMYK  </span> <p> Zet om in de CMYK-kleurruimte. </p> </li> 
        <li id="li_F3606B45C0F84BA594263EA12243F67A"> <span class="uicontrol"> Krachtig maken als grijswaarden  </span> <p> Zet om in de grijswaardenkleurruimte. </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>PDF-opties </p> </td> 
      <td colname="col02"> <p>E-catalogus automatisch genereren op basis van PDF van meerdere pagina's </p> </td> 
      <td colname="col2"> <p> Er wordt automatisch een eCatalog gemaakt van het PDF-bestand. De eCatalog wordt genoemd naar het Pdf- dossier u uploadde. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> PDF-opties </p> </td> 
      <td colname="col02"> <p>Trefwoorden extraheren </p> </td> 
      <td colname="col2"> <p>Extraheert woorden uit het PDF-bestand, zodat het bestand doorzoekbaar is op trefwoorden. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Klik in het rechterdeelvenster op de gewenste afbeelding, sjabloon of Flash-bestand.

   Het pop-upvenster [!DNL Pick An Asset] wordt weergegeven.
1. (Optioneel) Voer in het pop-upvenster [!DNL Pick An Asset] in de vervolgkeuzelijst [!DNL Actions] een van de volgende handelingen uit:

   * Klik op **[!UICONTROL Move]**. Selecteer in het dialoogvenster [!DNL Select a folder to move to] de map waarin u het digitale element wilt verplaatsen. Klik op **[!UICONTROL Move]**.

      U kunt ook meerdere digitale elementen selecteren die u naar een andere map wilt verplaatsen.

   * Klik op **[!UICONTROL Delete]**. Klik in het dialoogvenster [!DNL Delete Selected Assets] op **[!UICONTROL Delete]**.

      U kunt ook meerdere digitale elementen selecteren die u uit de map wilt verwijderen.

   * Klik op **[!UICONTROL Rename]**. Typ in het dialoogvenster [!DNL Enter a new name for] een nieuwe naam voor het digitale element in het tekstveld. Klik op **[!UICONTROL Rename]**.

1. (Optioneel) Afhankelijk van het digitale element dat u hebt geselecteerd, stelt u in het linkerdeelvenster van het pop-upvenster [!DNL Pick an Asset] de gewenste opties in.
1. Klik op het element om het te selecteren voor gebruik als banner.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een banner bewerken met Adobe Dynamic Media Classic {#task_C3E782477FBF428ABEA220751781ACA9}

Gebruik [!DNL Edit Banner] om de eigenschappen en parameters te wijzigen van een banner die u hebt toegevoegd met gebruik van Adobe Dynamic Media Classic.

<!-- 

t_editing_a_banner_using_adobe_scene7.xml

 -->

Als u een banner hebt toegevoegd door HTML-code toe te voegen, kunt u de banner bewerken met de functie voor zoeken/verhandelen van sites.

Zie ook [Een banner bewerken](../c-about-design-menu/c-about-banners.md#task_D4081083BE7B40F5A003D1A2F1435AEA).

**Een banner bewerken met Adobe Dynamic Media Classic**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Banners]**.
1. Klik op [!DNL Banners] op de pagina ![](assets/icon_edit_16.gif) boven een bannerminiatuur met een S7-pictogram in de linkerbenedenhoek van het bannervenster.
1. Stel op de pagina [!DNL Change Parameter] de gewenste opties in.
1. Wanneer u klaar bent met het bewerken van de banner, klikt u op **[!UICONTROL Save]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Bezig met verwijderen van banners {#task_32F3BADC481E4E8984B2AA04B96052EB}

U kunt gefaseerde banners verwijderen die u niet meer nodig hebt of wilt gebruiken, of een banners tegelijk, of als groep.

<!-- 

t_deleting_banners.xml

 -->

**banners verwijderen**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Banners]**.
1. (Optioneel) Voer een of meer van de volgende handelingen uit:

   * Selecteer op de pagina [!DNL Banners] het bannertype dat u wilt zoeken in de vervolgkeuzelijst **[!UICONTROL Find banner of type]**. Geef desgewenst een labelnaam op in het tekstveld **[!UICONTROL with tag]** of een naam voor een bannertype in het tekstveld **[!UICONTROL with name]**. Klik op **[!UICONTROL Find.]**

   * Selecteer in de vervolgkeuzelijst **[!UICONTROL Sort]** hoe u de lijst met banners wilt rangschikken.
   * Selecteer in de vervolgkeuzelijst **[!UICONTROL Show]** het aantal banners dat u in de huidige pagina wilt laden die u bekijkt.

1. Voer een van de volgende handelingen uit:

   * Klik in de linkerbovenhoek van een bannervak op het selectievakje van elke banner die u wilt verwijderen.
   * Controleer **[!UICONTROL Select all]** op de bovenste balk van de pagina [!DNL Banners] om elke banner te selecteren die op de momenteel weergegeven pagina is geladen.

1. Klik in de vervolgkeuzelijst **[!UICONTROL Bulk Actions]** op **[!UICONTROL Delete]**.
1. Klik in het dialoogvenster [!DNL Confirmation Action] op **[!UICONTROL OK]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Voorvertoning van banners {#task_6AB1F81A984A4DC2ACACD1FE030545E2}

U kunt door banners bladeren die u aan de [!DNL Banners] pagina hebt toegevoegd om hun volledige grootte te bekijken. CSS in de sjabloon die invloed heeft op de banner, wordt niet weergegeven.

<!-- 

t_previewing_banners.xml

 -->

**Een voorvertoning van banners weergeven**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Banners]**.
1. (Optioneel) Voer een of meer van de volgende handelingen uit:

   * Selecteer op de pagina [!DNL Banners] het bannertype dat u wilt zoeken in de vervolgkeuzelijst **[!UICONTROL Find banner of type]**. Geef desgewenst een labelnaam op in het tekstveld **[!UICONTROL with tag]** of een naam voor een bannertype in het tekstveld **[!UICONTROL with name]**. Klik op **[!UICONTROL Find.]**

   * Selecteer in de vervolgkeuzelijst **[!UICONTROL Sort]** hoe u de lijst met banners wilt rangschikken.
   * Selecteer in de vervolgkeuzelijst **[!UICONTROL Show]** het aantal banners dat u in de huidige pagina wilt laden die u bekijkt.

1. Klik op de pagina [!DNL Banners] op een bannerminiatuur om de volledige grootte weer te geven.
1. Voer een van de volgende handelingen uit:

   * Klik in het dialoogvenster voor de bannervoorvertoning op de pijl naar links of naar rechts om door de banners op volledige grootte te navigeren en deze weer te geven.
   * Klik op de sluitknop om het dialoogvenster met de bannervoorvertoning te sluiten en terug te keren naar de pagina [!DNL Banners].

## Bewegende banners live {#task_161F4FEC8362474296A566E64BF05B97}

U kunt een of meer geselecteerde banners live naar uw website duwen.

<!-- 

t_pushing_banners_live.xml

 -->

U kunt desgewenst ook alle wijzigingen in elke banner live uitvoeren met de optie **[!UICONTROL Push Live]** onder aan de pagina [!DNL Banners].

Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

**Banners live duwen**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Banners]**.
1. (Optioneel) Voer een of meer van de volgende handelingen uit:

   * Selecteer op de pagina [!DNL Banners] het bannertype dat u wilt zoeken in de vervolgkeuzelijst **[!UICONTROL Find banner of type]**. Geef desgewenst een labelnaam op in het tekstveld **[!UICONTROL with tag]** of een naam voor een bannertype in het tekstveld **[!UICONTROL with name]**. Klik op **[!UICONTROL Find]**.

   * Selecteer in de vervolgkeuzelijst **[!UICONTROL Sort]** hoe u de lijst met banners wilt rangschikken.
   * Selecteer in de vervolgkeuzelijst **[!UICONTROL Show]** het aantal banners dat u in de huidige pagina wilt laden die u bekijkt.

1. Voer een van de volgende handelingen uit:

   * Klik in de linkerbovenhoek van een bannervak op het selectievakje van elke banner die u wilt verwijderen.
   * Controleer **[!UICONTROL Select all]** op de bovenste balk van de pagina [!DNL Banner] om elke banner te selecteren die op de momenteel weergegeven pagina is geladen.

1. Klik in de vervolgkeuzelijst **[!UICONTROL Bulk Actions]** op **[!UICONTROL Push live]**.
1. Klik in het dialoogvenster [!DNL Confirmation Action] op **[!UICONTROL OK]**.
1. (Optioneel) Klik op de pagina [!DNL Banners] om de aangebrachte wijzigingen te herstellen.**[!UICONTROL History]**

   Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).
