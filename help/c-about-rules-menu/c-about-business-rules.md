---
description: U kunt de BedrijfsRegels gebruiken om uw onderzoek te ruilen.
solution: Target
title: Informatie over bedrijfsregels
topic: Regels, zoeken en verhandelen van sites
uuid: f2186f54-7a39-4f46-bb29-5115d5a17f07
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '3120'
ht-degree: 0%

---


# Informatie over bedrijfsregels{#about-business-rules}

U kunt de BedrijfsRegels gebruiken om uw onderzoek te ruilen.

## Bedrijfsregels gebruiken {#concept_2A93D76216754D3D8412CDEA00BD26BD}

U kunt bijvoorbeeld configureren wanneer banners worden weergegeven of welke resultaten worden weergegeven en in welke volgorde. U kunt de positie van een punt in uw facet ook vormen, en welke malplaatje voor een bepaalde onderzoek wordt gebruikt. de regels worden uitgevoerd in de volgorde waarin zij zijn vastgesteld; hoger het de ordeaantal van een regel, later het in het proces in werking stelt, die vroegere regels drijven. U kunt de regels slepen en neerzetten om de volgorde te wijzigen, of u kunt de regels opnieuw ordenen door een nieuw nummer in te voeren in het tekstvak voor de regelvolgorde.

Elke bedrijfsregel bestaat uit triggers en acties.

De trigger bepaalt wanneer de regel wordt uitgevoerd. Bijvoorbeeld, wanneer de vraagtermijn &quot;mens&quot;is of wanneer de resultaten meestal hiaten zijn. De trigger bestaat uit meerdere voorwaarden die allemaal moeten zijn, of een van beide moeten true zijn om de algemene trigger true te laten zijn. U kunt de prioriteit opgeven door de triggeroperator te wijzigen.

De actie bepaalt wat gebeurt wanneer aan de trekkervoorwaarde wordt voldaan. Stel bijvoorbeeld de banner in om een bepaald resultaat weer te geven of te verplaatsen naar positie 1. De lijst van regels toont summiere informatie over de regel. U kunt op een regelnaam klikken om deze te openen en aanvullende informatie weer te geven.

De lijst van regels toont een lijst van al uw bedrijfsregels. Standaard worden in de tabel de laatste tien regels weergegeven die zijn toegevoegd, in aflopende volgorde. U kunt op de kolomkoppen in de tabel klikken om de regels in oplopende of aflopende volgorde te sorteren.

De bedrijfsregels kunnen één van drie staten hebben: Goedgekeurd, opgeschort of WIP (Werk in uitvoering)

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
   <td colname="col2"> <p>Goedgekeurde bedrijfsregels worden uitgevoerd in uw live omgeving en in uw gefaseerde omgeving. U keurt een bedrijfsregel in de Geavanceerde Bouwer van de Regel goed. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Onderbroken </p> </td> 
   <td colname="col2"> <p>Opgeschorte bedrijfsregels worden nooit uitgevoerd in uw gefaseerde omgeving of uw live omgeving. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>WIP </p> </td> 
   <td colname="col2"> <p>WIP (Werk in uitvoering) zijn bedrijfsregels die niet zijn goedgekeurd of opgeschort. Dat wil zeggen dat u er misschien nog aan werkt of dat u ze eerst wilt testen voordat u ze goedkeurt. De bedrijfsregels in een staat van WIP lopen slechts in uw gefaseerde milieu. </p> </td> 
  </tr> 
 </tbody> 
</table>

U keurt bedrijfsregels goed en duwt hen levend zodat zij in uw levende milieu lopen. U kunt op dit moment alleen *alle* regels live duwen. Nochtans, kunt u de status van een regel veranderen om controle te hebben over welke regels lopen en niet in uw levende milieu lopen.

Standaard worden regels uitgevoerd wanneer aan de bijbehorende triggers wordt voldaan. Nochtans, kunt u naar keuze een regel plannen om voor een specifieke datum en tijdwaaier te lopen.

Ook, door gebrek, lopen de regels wanneer hun vennoot trekkers voor alle opslag worden voldaan. Als u wilt dat de regel alleen van toepassing is op bepaalde winkels, kunt u het deelvenster Opslag gebruiken om een of meer winkels te selecteren waarop de regel wordt toegepast.

## Nieuwe bedrijfsregel toevoegen {#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7}

U kunt [!DNL Visual Rule Builder] of [!DNL Advanced Rule Builder] gebruiken om bedrijfsregels toe te voegen die de onderzoekservaring van uw klant aanpassen.

**Om een nieuwe bedrijfsregel toe te voegen**

De volgende stappen veronderstellen u de Visuele Bouwer van de Regel gebruikt.

1. Voer een van de volgende handelingen uit:

   * Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Business Rules]**. Klik op [!DNL Business Rules] op de pagina.**[!UICONTROL Add New Rule]**

   * Klik in het productmenu op **[!UICONTROL Simulator]**. Klik op **[!UICONTROL Simulator for Today]** rechts van het vervolgkeuzemenu **[!UICONTROL Options]** op de pagina **[!UICONTROL Add New Rule]**.

      Als de optie **[!UICONTROL Add New Rule]** niet zichtbaar is op de pagina, klikt u in de vervolgkeuzelijst **[!UICONTROL Options]** op **[!UICONTROL Simulate Staged]**.

      ![](assets/Simulator.png)

1. Typ in het tekstveld **[!UICONTROL Name]** de nieuwe naam van de bedrijfsregel.

   Klik **[!UICONTROL Save Rule]** nog niet.
1. (Optioneel) Als u een groot aantal bedrijfsregels beheert, kunt u bedrijfsregels labelen met specifieke labels. Voer in het veld **[!UICONTROL Tags]** een of meer labellabels in, gebruik een komma, tab of Enter als scheidingsteken.

   Gebruik op de pagina [!DNL Business Rules] de functie **[!UICONTROL Filter by tag]** om te filteren op regels die overeenkomen met een bepaald label. 1. Stel op de pagina [!DNL Business Rule Builder] de triggers en handelingen in die u wilt gebruiken.

   **Triggeropties**

   Triggers zijn de voorwaarden waaraan een bedrijfsregel moet voldoen om te kunnen worden uitgevoerd. Wanneer een bedrijfsregel veelvoudige trekkers heeft, kunt u vormen hoe de trekkers antwoorden gebruikend één van de volgende drie methodes:

   * Een reactie waarbij alle triggers true moeten zijn (de standaardinstelling), zoals in het volgende voorbeeld:

      `if a AND b AND c then ...`

   * Een reactie waarbij een van de triggers true moet zijn, zoals in het volgende voorbeeld:

      `if a OR b OR c then ...`

   * Een reactie waarbij een aangepaste combinatie van triggers wordt opgegeven. Met andere woorden, u combineert afzonderlijke triggers of &quot;voorwaarden&quot; met `AND`-operatoren en `OR`-operatoren.

      U kunt de evaluatieprioriteit ook wijzigen door combinaties van haakjes links en rechts toe te voegen, zoals in het volgende voorbeeld:

      `if (a OR b) AND c then ...`

      >[!NOTE]
      >
      >Als u `AND` exploitanten met `OR` exploitanten in een reeks van de Bedrijfs van de Douane combineert, zeker dat u haakjes geschikt specificeert om ervoor te zorgen dat de trekkers in de correcte orde worden geëvalueerd.

      Deze specifieke functie om een combinatie triggers aan te passen, is niet standaard ingeschakeld. Neem contact op met Technische ondersteuning om deze functie te activeren voor gebruik.
   <table> 
      <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Triggers, optie </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Trefwoordovereenkomsten </p> </td> 
      <td colname="col2"> <p>De trekker is waar wanneer de onderzoekstermijn het bepaalde case-sensitive sleutelwoord aanpast. De trigger is true voor zowel het trefwoord als alle synoniemen ervan, zoals gedefinieerd in het Linguistics-woordenboek. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Zoekopdrachten komen overeen </p> </td> 
      <td colname="col2"> <p> De trigger is waar wanneer alle zoekparameters overeenkomen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Resultaatgroep is dominant </p> </td> 
      <td colname="col2"> <p> De trigger is waar wanneer de groep resultaten die door de opgegeven zoekopdracht wordt gedefinieerd, de resultatenset domineert. </p> <p>Standaard wordt de dominantie ingesteld op 50%. Deze instelling is een handelsvoorkeur die u kunt instellen. </p> <p> 
        <!--See <xref href="t_Configuring_Merchandising_preferences.xml#task_7AC7B9F5D9F44E10AB5BC0B8CB31C37A" type="task" format="dita" scope="local">Configuring Merchandising preferences</xref>. --> </p> <p>Deze trigger kan alleen worden ingesteld op true als de hele groep aanwezig is binnen de resultaatset. De resultaatgroep is dynamisch. Ze kunnen na indexbewerkingen wijzigen, afhankelijk van de resultaten die overeenkomen met de oorspronkelijke zoekcriteria. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Resultaatgroep is aanwezig </p> </td> 
      <td colname="col2"> <p> De trigger is waar wanneer de groep resultaten die door de opgegeven zoekopdracht wordt gedefinieerd, aanwezig is in de resultatenset. De gehele groep moet aanwezig zijn binnen de resultaatset om aan deze trigger te voldoen (de resultaten kunnen op elke pagina worden weergegeven). De groep resultaten is dynamisch en kan na indexbewerkingen veranderen, afhankelijk van de resultaten die overeenkomen met de oorspronkelijke zoekcriteria. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Resultaat aanwezig </p> </td> 
      <td colname="col2"> <p> De trigger is waar wanneer het individuele resultaat wordt gevonden binnen de resultaatset. Het resultaat kan overal in de resultaatreeks zijn, het moet niet op de pagina zijn de gebruiker momenteel bekijkt. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **Handelingsopties**

   Wanneer de trekkers van een bedrijfsregel worden voldaan aan, worden de acties die met de regel worden geassocieerd uitgevoerd. Terwijl de Visuele Bouwer van de Regel u de volgende acties laat tot stand brengen, kunt u Geavanceerde Bouwer van de Regel gebruiken om extra soorten acties tot stand te brengen.

   Voor de acties Facet-item verwijderen, Facet-item onthullen, Facet verwijderen, Facet verwijderen en Facet-item één facet in de volgende tabel is een facet vereist. De interface voor het kiezen van een facet is afhankelijk van de configuratie van uw account. Een normale account gebruikt bijvoorbeeld een vervolgkeuzelijst voor het kiezen van facetten. Als uw account echter bepaalde facetten heeft, wordt een automatisch aanvullen tekstvak weergegeven waarin u de naam van een facet kunt invoeren. De functie voor automatisch aanvullen stelt facetten in een vervolgkeuzelijst voor terwijl u de naam van het facet typt. De suggesties omvatten momenteel gedefinieerde facetten. Als uw account een sleufkaart heeft, worden ook bepaalde aspecten voorgesteld.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Handelingen, optie </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Push Group </p> </td> 
      <td colname="col2"> <p> Hiermee wordt de groep met zoekresultaten, zoals gedefinieerd door de opgegeven zoekcriteria, op een specifieke positie geplaatst. </p> <p>Als u een groep met zoekresultaten duwt, wordt de groep niet impliciet toegevoegd. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Groep toevoegen </p> </td> 
      <td colname="col2"> <p> Voeg de groep zoekresultaten toe zoals gedefinieerd door de opgegeven zoekcriteria. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Groep verwijderen </p> </td> 
      <td colname="col2"> <p> Verwijder de groep met zoekresultaten die is gedefinieerd door de opgegeven zoekcriteria. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Enkel schuiven </p> </td> 
      <td colname="col2"> <p> Hiermee plaatst u het afzonderlijke zoekresultaat op de geselecteerde positie. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Enkel toevoegen </p> </td> 
      <td colname="col2"> <p> Hiermee voegt u een afzonderlijk zoekresultaat toe aan de geselecteerde positie. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Enkel verwijderen </p> </td> 
      <td colname="col2"> <p> Hiermee verwijdert u een afzonderlijk zoekresultaat uit de set met zoekresultaten. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Alle resultaten verwijderen </p> </td> 
      <td colname="col2"> <p>Hiermee verwijdert u alle resultaten uit de set met zoekresultaten. </p> <p> 
        <!-- Bug #3331637 The option is meant to be used in conjunction with other rule actions in order to create "canned landing pages" where we want to create a page's content solely by rule actions, and need to completely discard the "natural" results of the search. Given that the other options don't have any kind of "here's how/why you might use this", I don't see much point in breaking that precedent here.--> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Andere banner selecteren </p> </td> 
      <td colname="col2"> <p> Wijzigt de banner in het geselecteerde bannergebied. </p> <p>Deze optie is beschikbaar wanneer u met de rechtermuisknop op een banner klikt in het weergavegebied van de webpagina. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Banneropdrachten toevoegen </p> </td> 
      <td colname="col2"> <p>Alleen van toepassing op Classic Adobe Dynamic Media-sjablonen. </p> <p>Hiermee kunt u de standaardparameters wijzigen die in de bannersjabloon worden gebruikt. </p> <p>Zie de optietabel in <a scope="local" href="../c-about-design-menu/c-about-banners.md#task_AD1E0C00A9E04B1FA819EB93288786B3" type="reference" format="dita"> Een banner toevoegen met Adobe Dynamic Media Classic </a>. </p> <p>Zie ook <a href="../c-about-design-menu/c-about-banners.md#task_C3E782477FBF428ABEA220751781ACA9" type="task" format="dita" scope="local"> Een banner bewerken met Adobe Dynamic Media Classic </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>banner verwijderen </p> </td> 
      <td colname="col2"> <p> Hiermee verwijdert u de banner uit het geselecteerde bannergebied. geen banner wordt getoond tenzij een andere regel die een banner plaatst, deze regel met voeten treedt. </p> <p>Deze optie is beschikbaar wanneer u met de rechtermuisknop op een banner klikt in het weergavegebied van de webpagina. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Item met facet duwen </p> </td> 
      <td colname="col2"> <p> Hiermee wordt een item binnen een facet naar de geselecteerde positie gespoeld. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Zone verwijderen </p> </td> 
      <td colname="col2"> <p> Hiermee verwijdert u een zone uit de pagina met zoekresultaten. </p> <p>Zie ook de actie Remove Facet hieronder. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Zone onthullen </p> </td> 
      <td colname="col2"> <p> Hiermee wordt een zone op de pagina met zoekresultaten onthuld. </p> <p>Zie ook de actie onthullen van Facet hieronder. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Facet-item verwijderen </p> </td> 
      <td colname="col2"> <p> Hiermee wordt een facetitem uit een facet verwijderd. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Facet-item onthullen </p> </td> 
      <td colname="col2"> <p> Geeft een specifiek facetitem weer. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Facet onthullen </p> </td> 
      <td colname="col2"> <p> Geeft een specifiek facet aan. Deze actie heeft de voorkeur boven de actie Zone onthullen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Facet verwijderen </p> </td> 
      <td colname="col2"> <p> Hiermee verwijdert u een specifiek facet. Deze actie heeft de voorkeur boven de actie Zone verwijderen. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   Afhankelijk van het deelvenster van de regelbouwer dat actief (gevouwen) is, kunt u ook het volgende doen om triggers en handelingen in te stellen.

   * Wanneer het **[!UICONTROL Triggers]** paneel wordt ontvouwen - in het gebied van het presentatiesjabloon van de pagina van de Bouwer van de BedrijfsRegel, klik op om het even welk onderzoeksresultaat of onderzoeksfacet met de rechtermuisknop aan, en klik dan **[!UICONTROL Add "result present" trigger]**.

      Klik in het deelvenster Triggers op de X links van een trigger om deze uit de lijst met triggers te verwijderen.

   * Wanneer het **[!UICONTROL Actions]** paneel wordt ontvouwen - in het gebied van het presentatiesjabloon van de pagina van de Bouwer van de BedrijfsRegel, klik op een onderzoeksresultaat met de rechtermuisknop aan. Klik **[!UICONTROL Add Result]**, **[!UICONTROL Remove Result]**, **[!UICONTROL Push to bottom]**, of **[!UICONTROL Push to #`<n>`]** (waarbij `<n>` een cijfer is).


1. (Optioneel) Voer in elk deelvenster Business Rule Builder ( [!DNL Triggers], [!DNL Actions] of [!DNL Schedule]) een van de volgende handelingen uit:

   * Klik in het gedeelte Presentatiesjabloon van het paginagebied Business Rule Builder met de rechtermuisknop op een banner en klik vervolgens op **[!UICONTROL Select different banner]**. Klik op **[!UICONTROL Pick Banner]** op de pagina **[!UICONTROL Pick this banner]** onder de bannerminiatuur om deze toe te voegen aan uw presentatiesjabloon. U kunt alleen banners selecteren die qua grootte en gebied overeenkomen met de originele banner in de presentatiesjabloon.

      De handeling banner toevoegen wordt toegevoegd aan het deelvenster [!DNL Actions].

   * Klik in het gedeelte van de presentatiesjabloon op de pagina [!DNL Business Rule Builder] met de rechtermuisknop op een klassieke sjabloonbanner van Adobe Dynamic Media waarvan u de parameters wilt wijzigen en klik vervolgens op **[!UICONTROL Add banner commands]**. Stel in het dialoogvenster [!DNL Change Parameters] de gewenste parameteropties in.

      Zie de optietabel in [Een banner toevoegen met Adobe Dynamic Media Classic](../c-about-design-menu/c-about-banners.md#task_AD1E0C00A9E04B1FA819EB93288786B3).

      Klik op **[!UICONTROL Save]**.

      De parameterwijzigingen worden toegevoegd aan het [!DNL Actions] paneel.

      Zie ook [Een banner bewerken met Adobe Dynamic Media Classic](../c-about-design-menu/c-about-banners.md#task_C3E782477FBF428ABEA220751781ACA9).

   * Klik in het gedeelte Presentatiesjabloon van de pagina Business Rule Builder met de rechtermuisknop op een banner die u van de pagina wilt verwijderen en klik vervolgens op **[!UICONTROL Remove banner]**. De actie banner verwijderen wordt toegevoegd aan het deelvenster Handelingen.

1. (Optioneel) Voer in het deelvenster **[!UICONTROL Schedule]** een van de volgende handelingen uit:

   * Klik **[!UICONTROL Run Indefinitely]** om de regellooppas te hebben wanneer zijn bijbehorende trekkers worden ontmoet. Dit is de standaardinstelling.
   * Klik **[!UICONTROL Fixed Schedule]**, en specificeer dan de begindatum en de tijd, en de einddatum en de tijd voor de regel om te lopen wanneer zijn bijbehorende trekker wordt ontmoet.

1. Klik op **[!UICONTROL Save Rule]**.
1. (Optioneel) Voer op de pagina [!DNL Business Rules] een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een bedrijfsregel bewerken {#task_375CFA75D1D94D9E92A35DE1228E5087}

U kunt de Visuele Bouwer van de Regel of Geavanceerde Bouwer van de Regel gebruiken om bedrijfsregels uit te geven die u hebt toegevoegd.

**Een nieuwe bedrijfsregel bewerken**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Business Rules]**.
1. Voer op de pagina [!DNL Business Rules] een van de volgende handelingen uit:

   * Klik onder de kolom [!DNL Name] op de naam van een bedrijfsregel die u wilt wijzigen.

      De bedrijfsregel wordt geopend in de standaardinterface die in **[!UICONTROL Settings]** > **[!UICONTROL My Profile]** > **[!UICONTROL My Preferences]** wordt gespecificeerd.

   * Klik in de vervolgkeuzelijst naast de naam van een bedrijfsregel die u wilt bewerken op **[!UICONTROL Edit in advanced mode]** of **[!UICONTROL Edit in visual mode]**.

1. Typ in het tekstveld [!DNL Name] de nieuwe naam van de bedrijfsregel.

   Klik **[!UICONTROL Save Rule]** nog niet. 1. Stel op de pagina [!DNL Business Rule Builder] de triggers en handelingen in die u wilt gebruiken.

   Zie de optietabel onder [Een nieuwe bedrijfsregel toevoegen](../c-about-rules-menu/c-about-business-rules.md#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7).
1. (Optioneel) Voer in elk **[!UICONTROL Business Rule Builder]**-deelvenster ( [!DNL Triggers], [!DNL Actions] of [!DNL Schedule] een van de volgende handelingen uit:

   * Klik in het gedeelte van de presentatiesjabloon op de pagina [!DNL Business Rule Builder] met de rechtermuisknop op een banner en klik vervolgens op **[!UICONTROL Select different banner]**. Klik op [!DNL Pick Banner page] onder de bannerminiatuur om deze toe te voegen aan uw presentatiesjabloon. **[!UICONTROL Pick this banner]** U kunt alleen banners selecteren die qua grootte en gebied overeenkomen met de originele banner in de presentatiesjabloon.

      De handeling banner toevoegen wordt toegevoegd aan het deelvenster [!DNL Actions].

   * Klik in het gedeelte van de presentatiesjabloon op de pagina [!DNL Business Rule Builder] met de rechtermuisknop op een klassieke sjabloonbanner van Adobe Dynamic Media waarvan u de parameters wilt wijzigen en klik vervolgens op **[!UICONTROL Add banner commands]**. Stel in het dialoogvenster [!DNL Change Parameters] de gewenste parameteropties in.

      Zie de optietabel in [Een banner toevoegen met Adobe Dynamic Media Classic](../c-about-design-menu/c-about-banners.md#task_AD1E0C00A9E04B1FA819EB93288786B3).

      Klik op **[!UICONTROL Save]**.

      De parameterwijzigingen worden toegevoegd aan het [!DNL Actions] paneel.

      Zie ook [Een banner bewerken met Adobe Dynamic Media Classic](../c-about-design-menu/c-about-banners.md#task_C3E782477FBF428ABEA220751781ACA9).

   * Klik in het gedeelte van de presentatiesjabloon op de pagina [!DNL Business Rule Builder] met de rechtermuisknop op een banner die u van de pagina wilt verwijderen en klik vervolgens op **[!UICONTROL Remove banner]**. De actie banner verwijderen wordt toegevoegd aan het [!DNL Actions] paneel.

1. (Optioneel) Voer in het deelvenster [!DNL Schedule] een van de volgende handelingen uit:

   * Klik **[!UICONTROL Run Indefinitely]** om de regellooppas te hebben wanneer zijn bijbehorende trekkers worden ontmoet. Dit is de standaardinstelling.
   * Klik **[!UICONTROL Fixed Schedule]**, en specificeer dan de begindatum en de tijd, en de einddatum en de tijd voor de regel om te lopen wanneer zijn bijbehorende trekker worden ontmoet.

1. Klik op **[!UICONTROL Save Rule]**.

   De pagina [!DNL Business Rule Builder] wordt gesloten en u wordt teruggestuurd naar de pagina **[!UICONTROL Business Rule]**. Uw regels worden weergegeven in de tabel. Klik op de kolomkop **[!UICONTROL Modified]** om de regels te sorteren op bewerkingsdatum. 1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een bedrijfsregel kopiëren {#task_89F1879C71A54EE9B7454439302C03EC}

U kunt een bestaande bedrijfsregel kopiëren als basis voor een nieuwe bedrijfsregel te gebruiken die u wilt creëren.

**Een bedrijfsregel kopiëren**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Business Rules]**.
1. Klik op **[!UICONTROL Business Rules]** in de vervolgkeuzelijst naast de naam van een bedrijfsregel die u wilt kopiëren.**[!UICONTROL Copy rule]**
1. Bewerk de gekopieerde bedrijfsregel op de gebruikelijke manier.

   Zie [Een bedrijfsregel bewerken](../c-about-rules-menu/c-about-business-rules.md#task_375CFA75D1D94D9E92A35DE1228E5087).

## Bedrijfsregels goedkeuren {#task_BD569D18BF664272B8692294C162E2C1}

U kunt bedrijfsregels activeren die een status van WIP (Werk in uitvoering) of geschorst hebben.

**Bedrijfsregels goedkeuren**

1. Klik in het productmenu op **[!UICONTROL Rule]** > **[!UICONTROL Business Rules]**.
1. Sorteer op de pagina [!DNL Business Rules] met behulp van de kop van de statuskolom in de kolom [!DNL Status] van de tabel met bedrijfsregels de regels met de status **[!UICONTROL WIP]** of **[!UICONTROL suspended]**.

   Gebruik de kolomkop van het selectievakje aan de linkerkant van de tabel om alle regels te controleren die momenteel op de pagina worden weergegeven of controleer alleen die regels met de status **[!UICONTROL WIP]** of **[!UICONTROL suspended]**. 1. Klik op **[!UICONTROL Approve]** op de menubalk boven aan de pagina.
1. Klik in het dialoogvenster **[!UICONTROL Confirm Action]** op **[!UICONTROL OK]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Opschorting van bedrijfsregels {#task_364E1FFB905141C08E306C8F1794A20E}

U kunt bedrijfsregels opschorten die of een status van WIP (Werk in uitvoering) of goedgekeurd hebben.

Wanneer u een regel hebt opgeschort, geeft u in de gebruikersinterface aan dat u deze tijdelijk inactief hebt gemaakt en dat u alle werkzaamheden aan deze regel voor een andere tijd uitstelt. U kunt een onderbroken regel echter nog steeds bewerken.

**Bedrijfsvoorschriften opschorten**

1. Klik in het productmenu op **[!UICONTROL Rule]** > **[!UICONTROL Business Rules]**.
1. Op [!DNL Business Rules] pagina, gebruikend de status in de kolom van de Status van de lijst van bedrijfsregels, in de uiterst linkerkolom van de lijst, controleer de regels die een status van **[!UICONTROL WIP]**, of **[!UICONTROL approved]** hebben.
1. Klik op **[!UICONTROL Suspend]** op de menubalk boven aan de pagina.
1. Klik in het dialoogvenster **[!UICONTROL Confirm Action]** op **[!UICONTROL OK]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Bedrijfsregels hervatten {#task_E67D678C765B436EA2A3D6ADD7A49ABA}

U kunt bedrijfsregels hervatten om een geschorste regel opnieuw te activeren. Nadat u de bedrijfsregel hervat, wordt zijn status geplaatst aan WIP (Werk lopend).

**Om bedrijfsregels te hervatten**

1. Klik in het productmenu op **[!UICONTROL Rule]** > **[!UICONTROL Business Rules]**.
1. Op [!DNL Business Rules] pagina, gebruikend de status in de kolom van de Status van de lijst van bedrijfsregels, in de uiterst linkerkolom van de lijst, controleer de regels die een status van **[!UICONTROL suspended]** hebben.
1. Klik op **[!UICONTROL Resume]** op de menubalk boven aan de pagina.
1. Klik in het dialoogvenster [!DNL Confirm Action] op **[!UICONTROL OK]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## De volgorde wijzigen waarin bedrijfsregels worden uitgevoerd {#task_FE3B1C17307F49B49050C2EC5A063991}

U kunt bedrijfsregels opnieuw ordenen om de volgorde te wijzigen waarin ze worden uitgevoerd op presentatiesjablonen.

De bedrijfsregels worden uitgevoerd in de volgorde waarin ze zijn gedefinieerd; hoger het de ordeaantal van een regel, later het in het proces in werking stelt, die vroegere regels drijven. U wijzigt de volgorde van de regels door een nieuw nummer in te voeren in de kolom Volgorde van de tabel op de pagina [!DNL Business Rules]. U kunt slepen-en-neerzetten op regels ook gebruiken om hun runtime orde te veranderen.

**Om de orde te veranderen die de bedrijfsregels lopen**

1. Klik in het productmenu op **[!UICONTROL Rule]** > **[!UICONTROL Business Rules]**.
1. Voer op de pagina [!DNL Business Rules] in de tabel een van de volgende handelingen uit:

   * Klik op de kolomkop **[!UICONTROL Order]** om de regels in oplopende of aflopende volgorde te sorteren.
   * Typ in de kolom **[!UICONTROL Order]** in het tekstveld links van de naam van een bedrijfsregel het ordernummer dat u wilt gebruiken voor de regel.
   * Sleep een tabelrij naar de positie waar u de lijn wilt uitvoeren. Alle volgordenummers worden bijgewerkt om de nieuwe volgorde weer te geven waarin de regels worden uitgevoerd.

1. Klik op **[!UICONTROL Save Changes]**.

   Uw bedrijfsregels worden nu uitgevoerd in de volgorde die u hebt opgegeven. De uitzondering is als er een redirect bedrijfsregel wordt gespecificeerd. Als en wanneer de omleidingsbedrijfsregel wordt teweeggebracht of geraakt, houdt de verwerking van de bedrijfsregel op om voor omleiding toe te staan.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Verwijderen van bedrijfsregels {#task_AE37B42412044541BCC6D46CF8793DFF}

U kunt bedrijfsregels schrappen de waarvan status WIP, geschorst of goedgekeurd is, door het Bulk drop-down menu van Acties te gebruiken.

**Bedrijfsregels verwijderen**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Business Rules]**.
1. Voer op de pagina [!DNL Business Rules] een van de volgende handelingen uit:

   * Gebruik de kolomkop van het selectievakje om alle regels te controleren die momenteel op de pagina worden weergegeven.
   * Controle slechts die bedrijfsregels die u wilt schrappen, die op de status in de kolom van de Status van de lijst worden gebaseerd.

1. Klik in de vervolgkeuzelijst [!DNL Bulk Actions] op **[!UICONTROL Delete]**.
1. Klik in het dialoogvenster [!DNL Confirm Action] op **[!UICONTROL OK]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).
