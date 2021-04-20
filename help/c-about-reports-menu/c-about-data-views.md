---
description: In de weergave Gegevens worden de zoekresultaten weergegeven met de metavelden. Elke kolom is een metabeld en elke rij is het resultaat van een zoekopdracht. Pas de Weergaven van Gegevens aan door kolommen te kiezen en opnieuw te rangschikken. Gegevensweergaven kunnen ook aangepaste titels en beschrijvingen hebben.
solution: Target
title: Gegevens
topic: Reports,Site search and merchandising
uuid: 18930551-960d-40c2-b5b7-0807a2e11134
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '1023'
ht-degree: 0%

---


# Informatie over gegevensweergaven{#about-data-views}

In de weergave Gegevens worden de zoekresultaten weergegeven met de metavelden. Elke kolom is een metabeld en elke rij is het resultaat van een zoekopdracht. Pas de Weergaven van Gegevens aan door kolommen te kiezen en opnieuw te rangschikken. Gegevensweergaven kunnen ook aangepaste titels en beschrijvingen hebben.

## Gegevensweergaven gebruiken {#concept_DCA897D074464BC1861AA47B40CC86C3}

Elk account heeft het gemak om meerdere gegevensweergaven te maken. Gebruik de pagina Gegevens weergeven om deze gegevensweergaven te maken en te bewerken.

Nadat u een gegevensweergave hebt toegevoegd, moet u deze bewerken om de weergave te configureren en aan te passen.

Zie [Een gegevensweergave bewerken](../c-about-reports-menu/c-about-data-views.md#task_258A367896C24DD498C755925EA8F516).

U kunt een bestaande gegevensweergave kopiëren en gebruiken als basis voor het maken van een nieuwe gegevensweergave.

Zie [Een gegevensweergave kopiëren](../c-about-reports-menu/c-about-data-views.md#task_78D4C2799BC84677843ED4CA1CD205AF).

## Een gegevensweergave toevoegen {#task_A20FEB2E1CA1444D816D2F5F4B6E5B2D}

U kunt een gegevensweergave toevoegen aan de pagina [!DNL Data Views] om de waarden van elk metabeld met een zoekquery weer te geven.

Nadat u een gegevensweergave hebt toegevoegd, moet u deze bewerken om de weergave te configureren en aan te passen.

Zie [Een gegevensweergave bewerken](../c-about-reports-menu/c-about-data-views.md#task_258A367896C24DD498C755925EA8F516).

**Een gegevensweergave toevoegen**

1. Klik in het productmenu op **[!UICONTROL Reports]** > **[!UICONTROL Data Views]**.
1. Klik op [!DNL Data Views] op de pagina.**[!UICONTROL Add New Data View]**
1. Voer in het dialoogvenster [!DNL Add New Data View] in het veld [!DNL Title] de naam in van de gegevensweergave die u wilt maken.
1. Klik op **[!UICONTROL Add]**.

## Een gegevensweergave bewerken {#task_258A367896C24DD498C755925EA8F516}

Wanneer u een gegevensweergave toevoegt aan de pagina [!DNL Data Views], gebruikt u Bewerken om de naam en beschrijving van de gegevensweergave te wijzigen of om de weergave van elk metaveld te verplaatsen, weer te geven of te verbergen.

U kunt een geselecteerde gegevensweergave ook vergrendelen of ontgrendelen.

Zie [Een gegevensweergave toevoegen](../c-about-reports-menu/c-about-data-views.md#task_A20FEB2E1CA1444D816D2F5F4B6E5B2D).

**Een gegevensweergave bewerken**

1. Klik in het productmenu op **[!UICONTROL Reports]** > **[!UICONTROL Data Views]**.
1. Op [!DNL Data Views] pagina, in [!DNL Actions] kolom van de lijst, klik **[!UICONTROL Edit]** in de rij met de gegevensmening die u wilt veranderen.
1. Stel op de pagina [!DNL Data Views Editor] de gewenste opties in.

   De Redacteur van de Mening van Gegevens heeft alle controles voor het verbergen, tonen, en het bewegen van gebiedskolommen op de pagina van de Mening van Gegevens.

   Als u een gegevensweergave bekijkt, worden in de resulterende tabel ook de volgende extra kolomvelden weergegeven die niet bewerkbaar zijn: Rangschikking, Relevantie en Score (algemeen). Deze drie speciale gebieden vertegenwoordigen de relevantiescore, rangscores, en algemene scores voor elk resultaat.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Titel </p> </td> 
      <td colname="col2"> <p>De naam van de gegevensweergave. De naam wordt in de rechterbovenhoek weergegeven wanneer u de gegevensweergave bekijkt. </p> <p>Zie <a href="../c-about-reports-menu/c-about-data-views.md#task_FD0D2CE53DF84CBD9220AD7CA920011F" type="task" format="dita" scope="local"> Een gegevensweergave bekijken</a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Beschrijving </p> </td> 
      <td colname="col2"> <p>(Optioneel) Bevat een beschrijving van de gegevensweergave. De beschrijving wordt getoond tussen de titelnaam van de gegevensmening en <span class="wintitle"> Nieuw Onderzoek</span> tekstgebied. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Zoekparameters </p> </td> 
      <td colname="col2"> <p>Hier kunt u standaardzoekparameters opgeven. Wanneer de gegevensweergave voor de eerste keer wordt weergegeven, worden deze CGI-parameters automatisch toegevoegd. </p> <p><span class="codeph"> sp_cs</span> of <span class="codeph"> sp_f</span> niet wijzigen of verwijderen. Deze parameters zijn essentieel voor de weergave Gegevens, ongeacht de tekenset van de voorkeur van de account. </p> <p>Zie <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> CGI-parameters voor achtergrondzoekopdrachten</a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Status vergrendelen </p> </td> 
      <td colname="col2"> <p>Hiermee kunt u de gegevensweergave vergrendelen of ontgrendelen. </p> <p>U kunt een vergrendelde gegevensweergave alleen weergeven met een wachtwoord en een gebruikersnaam. De gebruiker moet lid zijn van de account. </p> <p>Een niet-vergrendelde gegevensweergave is toegankelijk zonder wachtwoord of gebruikersaccount. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Volgorde </p> </td> 
      <td colname="col2"> <p> Hiermee kunt u de kolomvolgorde wijzigen door het nummer in het tekstvak <span class="wintitle"> Order</span> te bewerken. U kunt ook een rij slepen en neerzetten om de kolomvolgorde te wijzigen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Inclusief </p> </td> 
      <td colname="col2"> <p> Hiermee kunt u de weergave van de kolom in- of uitschakelen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>URL weergeven als afbeelding </p> </td> 
      <td colname="col2"> <p>Geef miniaturen en afbeeldingen in deze kolom weer als het zoekresultaat voor deze kolom een URL retourneert. </p> <p>De URL wordt van de schemanaam of het protocol gestript alvorens een waarde van het <span class="codeph"> src</span> attribuut van een beeldmarkering te worden. </p> <p>Als het terugkerende onderzoeksresultaat niet als URL aan een beeld kijkt, dan wordt getoond. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Veldlengte </p> </td> 
      <td colname="col2"> <p>Hiermee stelt u het aantal tekens in dat als resultaat in de gegevensweergave wordt weergegeven. </p> <p>De standaardwaarde is 100 tekens. </p> <p>Sommige velden, zoals de rangschikkingsscore en het datumveld, hebben geen aanpasbare veldlengte. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Klik op **[!UICONTROL Save Changes]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een gegevensweergave {#task_78D4C2799BC84677843ED4CA1CD205AF} kopiëren

U kunt een bestaande gegevensweergave op de pagina [!DNL Data Views] kopiëren en deze gebruiken als basis voor het maken van een nieuwe gegevensweergave.

Nadat u een gegevensweergave hebt gekopieerd, kunt u deze verder aanpassen door de weergave te bewerken.

Zie [Een gegevensweergave bewerken](../c-about-reports-menu/c-about-data-views.md#task_258A367896C24DD498C755925EA8F516).

**Een gegevensweergave kopiëren**

1. Klik in het productmenu op **[!UICONTROL Reports]** > **[!UICONTROL Data Views]**.
1. Op [!DNL Data Views] pagina, in [!DNL Actions] kolom van de lijst, klik **[!UICONTROL Copy]** in de rij met de gegevensmening die u wilt kopiëren.
1. Voer op de pagina [!DNL Copy Data View] in het tekstveld [!DNL New Title] de nieuwe naam in die u wilt toewijzen aan de gegevensweergave.
1. Klik op **[!UICONTROL Copy]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een gegevensweergave verwijderen {#task_61C32F8F00A549A5A3E7EDDA6F537098}

U kunt een gegevensweergave op de pagina [!DNL Data Views] verwijderen die u niet meer nodig hebt of gebruikt.

**Een gegevensweergave verwijderen**

1. Klik in het productmenu op **[!UICONTROL Reports]** > **[!UICONTROL Data Views]**.
1. Op [!DNL Data Views] pagina, in [!DNL Actions] kolom van de lijst, klik **[!UICONTROL Delete]** in de rij met de gegevensmening die u wilt verwijderen.
1. Klik op [!DNL Delete Data View] op de pagina **Delete**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een gegevensweergave bekijken {#task_FD0D2CE53DF84CBD9220AD7CA920011F}

U kunt [!DNL View] op [!DNL Data Views] pagina gebruiken om een geselecteerde gegevensmening te tonen.

De gegevensweergave die u selecteert, wordt geopend in een apart browservenster.

**Een gegevensweergave bekijken**

1. Klik in het productmenu op **[!UICONTROL Reports]** > **[!UICONTROL Data Views]**.
1. Voer een van de volgende handelingen uit:

   * Klik op de pagina [!DNL Data Views] in de kolom [!DNL Title] van de tabel op de naam van een gegevensweergave die u wilt openen.

   * Klik op de pagina [!DNL Data Views] in de kolom [!DNL Actions] van de tabel op **[!UICONTROL View]** in de rij met de gegevensweergave die u wilt openen.

