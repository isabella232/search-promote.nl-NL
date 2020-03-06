---
description: Je kunt zakelijke regels gebruiken om je zoekopdracht te verkopen.
seo-description: Je kunt zakelijke regels gebruiken om je zoekopdracht te verkopen.
seo-title: Informatie over bedrijfsregels
solution: Target
title: Informatie over bedrijfsregels
topic: Rules,Site search and merchandising
uuid: f2186f54-7a39-4f46-bb29-5115d5a17f07
translation-type: tm+mt
source-git-commit: 2dd205d3034e8397d88007a1618a121f0b6087a8

---


# Informatie over bedrijfsregels{#about-business-rules}

Je kunt zakelijke regels gebruiken om je zoekopdracht te verkopen.

## Bedrijfsregels gebruiken {#concept_2A93D76216754D3D8412CDEA00BD26BD}

Bijvoorbeeld, kunt u vormen wanneer de banners verschijnen, of welke resultaten verschijnen en in welke orde. U kunt de positie van een punt in uw facet ook vormen, en welk malplaatje wordt gebruikt voor een bepaald onderzoek. De regels lopen in de orde zij werden bepaald; hoger het de ordeaantal van een regel, later loopt het in het proces, dat vroegere regels trompelt. U kunt slepen-en-laten vallen de regels om hun orde te veranderen, of u kunt hen opnieuw in orde brengen door een nieuw aantal in het de tekstvakje van de regelenorde in te gaan.

Elke bedrijfsregel wordt samengesteld uit trekkers en acties.

De trekker bepaalt wanneer de regel loopt. Bijvoorbeeld, wanneer de vraagtermijn &quot;mens&quot;is of wanneer de resultaten meestal haden zijn. De trekker bestaat uit veelvoudige voorwaarden die of allen moeten zijn, of om het even welk van hen waar zijn om de algemene trekker waar te maken. U kunt de belangrijkheid specificeren door de trekkerexploitant te veranderen.

De actie bepaalt wat gebeurt wanneer de trekkervoorwaarde wordt voldaan aan. Bijvoorbeeld, plaatsend de banner aan vertoning of bewegend een bepaald resultaat aan positie 1. De lijst van regels toont summiere informatie over de regel. U kunt een regelnaam klikken om het te openen en extra informatie te zien.

De lijst van regels toont een lijst van al uw bedrijfsregels. Door gebrek, toont de lijst de laatste tien regels die, in dalende orde werden toegevoegd. U kunt de kolomkopballen in de lijst klikken om de regels in stijgende of dalende orde te sorteren.

De bedrijfsregels kunnen één van drie staten hebben: Goedgekeurd, geschorst, of WIP (het Werk lopend)

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Staat van de bedrijfsregel </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Goedgekeurd </p> </td> 
   <td colname="col2"> <p>De goedgekeurde bedrijfsregels worden uitgevoerd in uw live omgeving en in uw gefaseerde omgeving. U keurt een bedrijfsregel in de Geavanceerde Bouwer van de Regel goed. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>geschorst </p> </td> 
   <td colname="col2"> <p>De geschorste bedrijfsregels lopen nooit in uw gefaseerde milieu of uw levende milieu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>WIP </p> </td> 
   <td colname="col2"> <p>WIP (het Werk in Bezig) is bedrijfsregels die noch worden goedgekeurd noch worden opgeschort. Dat wil zeggen, u kunt nog aan hen werken of u kunt hen willen eerst testen alvorens hen goed te keuren. De bedrijfsregels in een staat van WIP lopen slechts in uw gefaseerd milieu. </p> </td> 
  </tr> 
 </tbody> 
</table>

U keurt bedrijfsregels goed en duw hen levend zodat zij in uw levend milieu lopen. Momenteel, kunt u slechts *alle* regels duwen leven. Nochtans, kunt u de status van een regel veranderen om controle te hebben waarover de regels lopen en niet in uw levend milieu lopen.

Door gebrek lopen de regels wanneer hun bijbehorende trekkers worden voldaan aan. Nochtans, kunt u een regel naar keuze plannen om voor een specifieke datum en tijdwaaier te lopen.

Ook, door gebrek, lopen de regels wanneer hun vennoot trekkers voor alle opslag worden ontmoet. Als u de regel slechts voor bepaalde opslag wilt toepassen dan kunt u het paneel van Winkels gebruiken om één of meerdere opslag te selecteren waarop de regel wordt toegepast.

## Het toevoegen van een nieuwe bedrijfsregel {#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7}

U kunt bedrijfsregels gebruiken [!DNL Visual Rule Builder] of [!DNL Advanced Rule Builder] toevoegen die de het onderzoekservaring van uw klant aanpassen.

**Om een nieuwe bedrijfsregel toe te voegen**

De volgende stappen veronderstellen u de Visuele Bouwer van de Regel gebruikt.

1. Doe één van het volgende:

   * Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Business Rules]**. Voor de [!DNL Business Rules] pagina, klik **[!UICONTROL Add New Rule]**.

   * Klik in het productmenu op **[!UICONTROL Simulator]**. Voor de **[!UICONTROL Simulator for Today]** pagina, klik **[!UICONTROL Add New Rule]** rechts van het **[!UICONTROL Options]** drop-down menu.

      Als de **[!UICONTROL Add New Rule]** optie niet zichtbaar op de pagina, op het **[!UICONTROL Options]** drop-down menu is, klik **[!UICONTROL Simulate Staged]**.

      ![](assets/Simulator.png)

1. Op het **[!UICONTROL Name]** tekstgebied, typ de nieuwe naam van de bedrijfsregel.

   Klik **[!UICONTROL Save Rule]** nog niet.
1. (Facultatief) als u een groot aantal bedrijfsregels beheert, kunt u bedrijfsregels met specifieke etiketten etiketteren. Op het **[!UICONTROL Tags]** gebied, ga één of meerdere markeringsetiketten in, gebruik een komma, een Lusje, of ga als afbakening binnen.

   Voor de [!DNL Business Rules] pagina, gebruik de **[!UICONTROL Filter by tag]** eigenschap aan filter voor regels die een bepaald etiket aanpassen. 1. Voor de [!DNL Business Rule Builder] pagina, plaats de trekkers en de acties die u wilt gebruiken.

       **De opties van de trekker**
 de     
     Trekkers zijn de voorwaarden die moeten worden voldaan aan voor een bedrijfsregel te lopen. Wanneer een bedrijfsregel veelvoudige trekkers heeft, kunt u vormen hoe de trekkers gebruikend één van de volgende drie methodes antwoorden:
   
   * Een reactie waar alle trekkers (standaard het plaatsen) zoals in het volgende voorbeeld waar moeten zijn:

      `if a AND b AND c then ...`

   * Een reactie waar om het even welke trekkers zoals in het volgende voorbeeld waar moeten zijn:

      `if a OR b OR c then ...`

   * Een reactie waar een douanecombinatie van trekkers wordt gespecificeerd. Namelijk combineer u individuele trekkers of &quot;voorwaarden&quot;met `AND` exploitanten en `OR` exploitanten.

      U kunt de evaluatiebelangrijkheid ook veranderen door linker en juist-haaktcombinaties toe te voegen zoals in het volgende voorbeeld:

      `if (a OR b) AND c then ...`

      >[!NOTE]
      >
      >Als u `AND` exploitanten met `OR` exploitanten in een de bedrijfsregelreeks van de Douane combineert, ben zeker dat u haakjes geschikt specificeert om ervoor te zorgen dat de trekkers in de correcte orde worden geëvalueerd.

      Deze bepaalde eigenschap van het kunnen een combinatie trekkers aanpassen wordt niet toegelaten door gebrek. Neem contact op met Technische ondersteuning om deze functie voor uw gebruik te activeren.
   <table> 
      <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Optie voor triggers </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Trefwoordmatchen </p> </td> 
      <td colname="col2"> <p>De trekker is waar wanneer de onderzoekstermijn het bepaalde case-sensitive sleutelwoord aanpast. De trekker is waar voor zowel het sleutelwoord als elk van zijn synoniemen, zoals die in het woordenboek van de Taalkunde wordt bepaald. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Zoekopdrachten </p> </td> 
      <td colname="col2"> <p> De trekker is waar wanneer alle onderzoeksparameters aanpassen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> De Groep van het resultaat is Dominant </p> </td> 
      <td colname="col2"> <p> De trekker is waar wanneer de groep resultaten die door de bepaalde die onderzoeksreeks wordt bepaald de resultaatreeks overheerst. </p> <p>Standaard is de dominantie ingesteld op 50%. Dit het plaatsen is een koopwaar voorkeur die u kunt plaatsen. </p> <p> 
        <!--See <xref href="t_Configuring_Merchandising_preferences.xml#task_7AC7B9F5D9F44E10AB5BC0B8CB31C37A" type="task" format="dita" scope="local">Configuring Merchandising preferences</xref>. --> </p> <p>De volledige groep moet aanwezig zijn binnen het resultaat dat wordt geplaatst voor deze trekker om waar te zijn. De groep resultaten is dynamisch. Zij kunnen na indexverrichtingen veranderen, afhankelijk van welke resultaten de originele onderzoekscriteria aanpassen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>De Groep van het resultaat is aanwezig </p> </td> 
      <td colname="col2"> <p> De trekker is waar wanneer de groep resultaten die door het bepaalde onderzoek worden bepaald in de resultaatreeks aanwezig is. De volledige groep moet aanwezig zijn binnen het resultaat dat is ingesteld om aan deze trigger te voldoen (de resultaten kunnen op elke pagina worden weergegeven). De groep van resultaten is dynamisch en kan na indexverrichtingen veranderen afhankelijk van welke resultaten de originele onderzoekscriteria aanpassen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Resultaat aanwezig </p> </td> 
      <td colname="col2"> <p> De trekker is waar wanneer het individuele resultaat binnen de resultaatreeks wordt gevonden. Het resultaat kan overal in de resultaatreeks zijn, moet het niet op de pagina zijn de gebruiker momenteel bekijkt. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **Actiemogelijkheden**

   Wanneer de trekkers van een bedrijfsregel worden ontmoet, worden de acties die met de regel worden geassocieerd uitgevoerd. Terwijl de Visuele Bouwer van de Regel u de volgende acties laat tot stand brengen, kunt u de Geavanceerde Bouwer van de Regel gebruiken om extra soorten acties tot stand te brengen.

   Het verwijder Punt van het Gezicht, openbaart het Punt van het Gezicht, openbaart Gezicht, verwijder Gezicht, de acties van het Punt van het Duw van het Gezicht in de volgende lijst vereisen een facet. De interface voor het kiezen van een facet hangt van af hoe uw rekening wordt gevormd. Bijvoorbeeld, gebruikt een normale rekening een drop-down lijst voor het kiezen van facetten. Als uw account echter bepaalde facetten heeft, wordt een tekstvak met automatische gegevens weergegeven waarin u de naam van een facet kunt invoeren. AutoComplete stelt facetten in een drop-down lijst voor aangezien u de naam van het facet typt. De suggesties omvatten momenteel bepaalde facetten. Als uw account een sleufkaart heeft, worden er ook steekproeven in voorgesteld.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Optie Acties </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Drukgroep </p> </td> 
      <td colname="col2"> <p> Past de groep onderzoeksresultaten zoals die door de gespecificeerde onderzoekscriteria aan een specifieke positie wordt bepaald. </p> <p>Het duwen van een groep onderzoeksresultaten voegt impliciet niet de groep toe. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Groep toevoegen </p> </td> 
      <td colname="col2"> <p> Voeg de groep onderzoeksresultaten toe zoals die door de gespecificeerde onderzoekscriteria wordt bepaald. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Groep verwijderen </p> </td> 
      <td colname="col2"> <p> Verwijder de groep van onderzoeksresultaten die door de gespecificeerde onderzoekscriteria worden bepaald. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Push Single </p> </td> 
      <td colname="col2"> <p> Past het individuele onderzoeksresultaat aan de geselecteerde positie in. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Enkele toevoegen </p> </td> 
      <td colname="col2"> <p> Voegt een individueel onderzoeksresultaat aan de geselecteerde positie toe. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Enkel verwijderen </p> </td> 
      <td colname="col2"> <p> Verwijdert een individueel onderzoeksresultaat uit de reeks van het onderzoeksresultaat. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Alle resultaten verwijderen </p> </td> 
      <td colname="col2"> <p>Verwijdert alle resultaten uit de reeks van het onderzoeksresultaat. </p> <p> 
        <!-- Bug #3331637 The option is meant to be used in conjunction with other rule actions in order to create "canned landing pages" where we want to create a page's content solely by rule actions, and need to completely discard the "natural" results of the search. Given that the other options don't have any kind of "here's how/why you might use this", I don't see much point in breaking that precedent here.--> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Selecteer een andere banner </p> </td> 
      <td colname="col2"> <p> Verandert de banner in het geselecteerde bannergebied. </p> <p>Deze optie is beschikbaar wanneer u op een banner in het Web-pagina het bekijken gebied met de rechtermuisknop klikt. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Voeg banneropdrachten toe </p> </td> 
      <td colname="col2"> <p>Is op de Dynamische Klassieke slechts malplaatjes van Media van Adobe van toepassing. </p> <p>Laat u de standaardparameters veranderen die in het bannermalplaatje worden gebruikt. </p> <p>Zie de lijst van opties in het <a scope="local" href="../c-about-design-menu/c-about-banners.md#task_AD1E0C00A9E04B1FA819EB93288786B3" type="reference" format="dita"> Toevoegen van een banner gebruikend Klassiek de Dynamische Media van Adobe </a>. </p> <p>Zie ook het <a href="../c-about-design-menu/c-about-banners.md#task_C3E782477FBF428ABEA220751781ACA9" type="task" format="dita" scope="local"> Uitgeven van een banner die de Dynamische Klassieke Media van Adobe gebruikt </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>banner verwijderen </p> </td> 
      <td colname="col2"> <p> Verwijdert de banner uit het geselecteerde bannergebied; geen banner wordt getoond tenzij een andere regel die een banner plaatst, deze regel met voeten treedt. </p> <p>Deze optie is beschikbaar wanneer u op een banner in het Web-pagina het bekijken gebied met de rechtermuisknop klikt. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Duw-facetitem </p> </td> 
      <td colname="col2"> <p> Past een punt binnen een facet aan de geselecteerde positie in. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Zone verwijderen </p> </td> 
      <td colname="col2"> <p> Verwijdert een streek uit de pagina van onderzoeksresultaten. </p> <p>Zie ook de Remove Facet actie hieronder. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Vrije zone </p> </td> 
      <td colname="col2"> <p> Hiermee wordt een zone in de pagina met zoekresultaten onthuld. </p> <p>Zie ook de actie van de Facet van het onthaal hieronder. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Object Facet verwijderen </p> </td> 
      <td colname="col2"> <p> Verwijdert een facetpunt uit een facet. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Facultatief object onthullen </p> </td> 
      <td colname="col2"> <p> Geeft een specifiek facetpunt terug. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Facet onthullen </p> </td> 
      <td colname="col2"> <p> Geeft een specifiek facet aan. Deze actie wordt verkozen boven de actie van de Zone van het Openbaar maken. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Facet verwijderen </p> </td> 
      <td colname="col2"> <p> Verwijdert een specifiek facet. Deze actie wordt verkozen over de Remove actie van de Streek. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   Afhankelijk van het paneel van de regelbouwer dat actief is (unfolded), kunt u het volgende ook doen om trekkers en acties te plaatsen.

   * Wanneer het **[!UICONTROL Triggers]** paneel - op het gebied van het presentatiemalplaatje van de pagina van de Bouwer van de Bedrijfs van de Regel wordt gevouwen, klik op om het even welk onderzoeksresultaat of onderzoeksfacet met de rechtermuisknop aan, en klik dan **[!UICONTROL Add "result present" trigger]**.

      In het paneel van Trekkers klik &quot;X&quot;links van een trekker om het uit de lijst van trekkers te verwijderen.

   * Wanneer het **[!UICONTROL Actions]** paneel - in het gebied van het presentatiemalplaatje van de pagina van de Bouwer van de Bedrijfs van de Regel wordt gevouwen, klik op een onderzoeksresultaat met de rechtermuisknop aan. Klik **[!UICONTROL Add Result]**, **[!UICONTROL Remove Result]**, **[!UICONTROL Push to bottom]**, of **[!UICONTROL Push to #`<n>`]** (waar `<n>` een cijfer is).


1. (Facultatief) in om het even welk paneel van de Bouwer van de Bedrijfs van de Regel ( [!DNL Triggers], [!DNL Actions], of [!DNL Schedule]), doe één van het volgende:

   * Op het gebied van het presentatiemalplaatje van het de paginagebied van de Bouwer van de Bedrijfs van de Regel, klik een banner met de rechtermuisknop aan, en klik dan **[!UICONTROL Select different banner]**. Voor de **[!UICONTROL Pick Banner]** pagina, klik **[!UICONTROL Pick this banner]** onder de bannerduimnagel om het aan uw presentatiemalplaatje toe te voegen. Slechts zijn de banners die de grootte en het gebied van de originele banner op het presentatiemalplaatje aanpassen beschikbaar voor u om te plukken.

      Voeg banneractie toe wordt toegevoegd aan het [!DNL Actions] paneel.

   * Op het gebied van het presentatiemalplaatje van de [!DNL Business Rule Builder] pagina, klik op een Klassieke het malplaatjebanner met de rechtermuisknop aan van Adobe de Dynamische Media van wie parameters u wilt veranderen, en dan klikken **[!UICONTROL Add banner commands]**. In de [!DNL Change Parameters] dialoogdoos, plaats de parameteropties die u wilt.

      Zie de lijst van opties in het [Toevoegen van een banner gebruikend de Dynamische Klassieke](../c-about-design-menu/c-about-banners.md#task_AD1E0C00A9E04B1FA819EB93288786B3)Media van Adobe.

      Klik op **[!UICONTROL Save]**.

      De parameterveranderingen worden toegevoegd aan het [!DNL Actions] paneel.

      Zie ook het [Uitgeven van een banner die de Dynamische Klassieke](../c-about-design-menu/c-about-banners.md#task_C3E782477FBF428ABEA220751781ACA9)Media van Adobe gebruikt.

   * Op het gebied van het presentatiemalplaatje van de pagina van de Bouwer van de Bedrijfs van de Regel, klik op een banner met de rechtermuisknop aan die u van de pagina wilt schrappen, en dan klikken **[!UICONTROL Remove banner]**. De verwijder banneractie wordt toegevoegd aan het paneel van Acties.

1. (Facultatief) in het **[!UICONTROL Schedule]** paneel, doe één van het volgende:

   * Klik **[!UICONTROL Run Indefinitely]** om de regellooppas te hebben wanneer zijn bijbehorende trekkers worden ontmoet. Deze optie is het gebrek.
   * Klik **[!UICONTROL Fixed Schedule]**, en specificeer dan de begindatum en de tijd, en de einddatum en de tijd voor de te lopen regel wanneer zijn bijbehorende trekker wordt ontmoet.

1. Klik op **[!UICONTROL Save Rule]**.
1. (Facultatief) op de [!DNL Business Rules] pagina, doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een bedrijfsregel bewerken {#task_375CFA75D1D94D9E92A35DE1228E5087}

U kunt de Visuele Bouwer van de Regel of de Geavanceerde Bouwer van de Regel gebruiken om bedrijfsregels uit te geven die u hebt toegevoegd.

**Om een nieuwe bedrijfsregel uit te geven**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Business Rules]**.
1. Op de [!DNL Business Rules] pagina, doe één van het volgende:

   * Onder de [!DNL Name] kolom, klik de naam van een bedrijfsregel die u wilt veranderen.

      De bedrijfsregel wordt geopend in de standaardinterface die in **[!UICONTROL Settings]** > **[!UICONTROL My Profile]** > **[!UICONTROL My Preferences]** wordt gespecificeerd.

   * In de drop-down lijst, naast een bedrijfsregelnaam die u wilt uitgeven, klikken **[!UICONTROL Edit in advanced mode]** of **[!UICONTROL Edit in visual mode]**.

1. Op het [!DNL Name] tekstgebied, typ de nieuwe naam van de bedrijfsregel.

   Klik **[!UICONTROL Save Rule]** nog niet. 1. Voor de [!DNL Business Rule Builder] pagina, plaats de trekkers en de acties die u wilt gebruiken.

   Zie de lijst van opties onder het [Toevoegen van een nieuwe bedrijfsregel](../c-about-rules-menu/c-about-business-rules.md#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7).
1. (Facultatief) in om het even welk **[!UICONTROL Business Rule Builder]** paneel ( [!DNL Triggers], [!DNL Actions], of [!DNL Schedule], doe om het even welke volgend:

   * In het gebied van het presentatiemalplaatje van de [!DNL Business Rule Builder] pagina, klik een banner met de rechtermuisknop aan, en klik dan **[!UICONTROL Select different banner]**. Voor [!DNL Pick Banner page], klik **[!UICONTROL Pick this banner]** onder de bannerduimnagel om het aan uw presentatiemalplaatje toe te voegen. Slechts zijn de banners die de grootte en het gebied van de originele banner op het presentatiemalplaatje aanpassen beschikbaar voor u om te plukken.

      Voeg banneractie toe wordt toegevoegd aan het [!DNL Actions] paneel.

   * Op het gebied van het presentatiemalplaatje van de [!DNL Business Rule Builder] pagina, klik op een Klassieke het malplaatjebanner met de rechtermuisknop aan van Adobe de Dynamische Media van wie parameters u wilt veranderen, en dan klikken **[!UICONTROL Add banner commands]**. In de [!DNL Change Parameters] dialoogdoos, plaats de parameteropties die u wilt.

      Zie de lijst van opties in het [Toevoegen van een banner gebruikend de Dynamische Klassieke](../c-about-design-menu/c-about-banners.md#task_AD1E0C00A9E04B1FA819EB93288786B3)Media van Adobe.

      Klik op **[!UICONTROL Save]**.

      De parameterveranderingen worden toegevoegd aan het [!DNL Actions] paneel.

      Zie ook het [Uitgeven van een banner die de Dynamische Klassieke](../c-about-design-menu/c-about-banners.md#task_C3E782477FBF428ABEA220751781ACA9)Media van Adobe gebruikt.

   * In het gebied van het presentatiemalplaatje van de [!DNL Business Rule Builder] pagina, klik op een banner met de rechtermuisknop aan die u van de pagina wilt schrappen, en dan klikken **[!UICONTROL Remove banner]**. De verwijder banneractie wordt toegevoegd aan het [!DNL Actions] paneel.

1. (Facultatief) in het [!DNL Schedule] paneel, doe één van het volgende:

   * Klik **[!UICONTROL Run Indefinitely]** om de regellooppas te hebben wanneer zijn bijbehorende trekkers worden ontmoet. Deze optie is het gebrek.
   * Klik **[!UICONTROL Fixed Schedule]**, en specificeer dan de begindatum en de tijd, en de einddatum en de tijd voor de te lopen regel wanneer zijn bijbehorende trekker worden ontmoet.

1. Klik op **[!UICONTROL Save Rule]**.

   De [!DNL Business Rule Builder] pagina sluit, en u wordt teruggegeven aan de **[!UICONTROL Business Rule]** pagina. Uw regels verschijnen in de lijst. Klik de **[!UICONTROL Modified]** kolomkopbal om de regels te sorteren door datum uit te geven. 1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Het kopiëren van een bedrijfsregel {#task_89F1879C71A54EE9B7454439302C03EC}

U kunt een bestaande bedrijfsregel kopiëren om als basis voor een nieuwe bedrijfsregel te gebruiken die u wilt tot stand brengen.

**Om een bedrijfsregel te kopiëren**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Business Rules]**.
1. Voor de **[!UICONTROL Business Rules]** pagina, in de drop-down lijst naast een bedrijfsregelnaam die u wilt kopiëren, klik **[!UICONTROL Copy rule]**.
1. Geef de gekopieerde bedrijfsregel zoals gebruikelijk uit.

   Zie Een [bedrijfsregel](../c-about-rules-menu/c-about-business-rules.md#task_375CFA75D1D94D9E92A35DE1228E5087)bewerken.

## Bedrijfsvoorschriften goedkeuren {#task_BD569D18BF664272B8692294C162E2C1}

U kunt bedrijfsregels activeren die of een status van WIP (het Werk lopend) of opgeschort hebben.

**Om bedrijfsregels goed te keuren**

1. Klik in het productmenu op **[!UICONTROL Rule]** > **[!UICONTROL Business Rules]**.
1. Voor de [!DNL Business Rules] pagina, die de kopbal van de statuskolom in de [!DNL Status] kolom van de lijst van bedrijfsregels gebruikt, sorteer de regels die een status van **[!UICONTROL WIP]** of **[!UICONTROL suspended]** hebben.

   Gebruik de kopbal van de controledoos kolomkolom op de linkerkant van de lijst om alle regels te controleren die momenteel op de pagina worden getoond of slechts die te controleren die een status van **[!UICONTROL WIP]** of **[!UICONTROL suspended]** hebben. 1. Voor de menubar dichtbij de bovenkant van de pagina, klik **[!UICONTROL Approve]**.
1. Klik in het **[!UICONTROL Confirm Action]** dialoogvenster op **[!UICONTROL OK]**.
1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Opschorting van bedrijfsvoorschriften {#task_364E1FFB905141C08E306C8F1794A20E}

U kunt bedrijfsregels opschorten die of een status van WIP (het Werk lopend) hebben of goedgekeurd.

Wanneer u een regel opschortte wijst u in het gebruikersinterface erop dat u tijdelijk het inactief hebt gemaakt en u om het even welk werk aan het voor een andere tijd uitstelt. U kunt, echter, nog een geschorste regel uitgeven.

**Om bedrijfsregels op te schorten**

1. Klik in het productmenu op **[!UICONTROL Rule]** > **[!UICONTROL Business Rules]**.
1. Voor de [!DNL Business Rules] pagina, die de status in de kolom van de Status van de lijst van bedrijfsregels, in de uiterst linkerkolom van de lijst gebruikt, controleer de regels die een status van hebben, of **[!UICONTROL WIP]****[!UICONTROL approved]**.
1. Voor de menubar dichtbij de bovenkant van de pagina, klik **[!UICONTROL Suspend]**.
1. Klik in het **[!UICONTROL Confirm Action]** dialoogvenster op **[!UICONTROL OK]**.
1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Bedrijfsregels hervatten {#task_E67D678C765B436EA2A3D6ADD7A49ABA}

U kunt bedrijfsregels hervatten om een geschorste regel te reactiveren. Nadat u de bedrijfsregel hervat, wordt zijn status geplaatst aan WIP (Werk lopend).

**Om bedrijfsregels te hervatten**

1. Klik in het productmenu op **[!UICONTROL Rule]** > **[!UICONTROL Business Rules]**.
1. Voor de [!DNL Business Rules] pagina, die de status in de kolom van de Status van de lijst van bedrijfsregels, in de uiterst linkerkolom van de lijst gebruikt, controleer de regels die een status van hebben **[!UICONTROL suspended]**.
1. Voor de menubar dichtbij de bovenkant van de pagina, klik **[!UICONTROL Resume]**.
1. Klik in het [!DNL Confirm Action] dialoogvenster op **[!UICONTROL OK]**.
1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Het veranderen van de orde dat de bedrijfsregels lopen {#task_FE3B1C17307F49B49050C2EC5A063991}

U kunt bedrijfsregels opnieuw in orde brengen om de orde te veranderen waarin zij op presentatiemalplaatjes lopen.

De bedrijfsregels lopen in de orde dat zij werden bepaald; hoger het de ordeaantal van een regel, later loopt het in het proces, dat vroegere regels trompelt. U bestelt regels opnieuw door een nieuw aantal in de kolom van de Orde van de lijst op de [!DNL Business Rules] pagina in te gaan. U kunt belemmering-en-daling op regels ook gebruiken om hun looppasorde te veranderen.

**Om de orde te veranderen dat de bedrijfsregels lopen**

1. Klik in het productmenu op **[!UICONTROL Rule]** > **[!UICONTROL Business Rules]**.
1. Op de [!DNL Business Rules] pagina, in de lijst, doe om het even welke volgend:

   * Klik de **[!UICONTROL Order]** kolomkopbal om de regels in stijgende of dalende orde te sorteren.
   * In de **[!UICONTROL Order]** kolom, op het tekstgebied links van een bedrijfsregelnaam, typ het ordeaantal dat u de regel wilt lopen.
   * Sleep een lijstrij aan de positie die u de regel wilt in werking stellen. Alle ordeaantallen worden bijgewerkt om op de nieuwe orde te wijzen waarin de regels lopen.

1. Klik op **[!UICONTROL Save Changes]**.

   Uw bedrijfsregels zullen nu in de orde lopen die u specificeerde. De uitzondering is als er een redirect gespecificeerde bedrijfsregel is. Als en wanneer de omleiding bedrijfsregel wordt teweeggebracht of geraakt, de ophouden van de bedrijfsregelverwerking om voor opnieuw te richten toe te staan.
1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Bedrijfsvoorschriften verwijderen {#task_AE37B42412044541BCC6D46CF8793DFF}

U kunt bedrijfsregels schrappen de waarvan status WIP is, opgeschort, of goedgekeurd, door het Bulk drop-down menu van Acties te gebruiken.

**Om bedrijfsregels te verwijderen**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Business Rules]**.
1. Op de [!DNL Business Rules] pagina, doe één van het volgende:

   * Gebruik de kopbal van de controledoos kolomkolom om alle regels te controleren die momenteel op de pagina worden getoond.
   * Controleer slechts die bedrijfsregels die u wilt schrappen, die op de status in de kolom van de Status van de lijst worden gebaseerd.

1. Voor de [!DNL Bulk Actions] drop-down lijst, klik **[!UICONTROL Delete]**.
1. Klik in het [!DNL Confirm Action] dialoogvenster op **[!UICONTROL OK]**.
1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).
