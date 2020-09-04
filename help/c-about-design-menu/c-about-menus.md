---
description: Met menu's kunt u de presentatielaag aanpassen.
seo-description: Met menu's kunt u de presentatielaag aanpassen.
seo-title: Menu's
solution: Target
subtopic: Navigation
title: Menu's
topic: Design,Site search and merchandising
uuid: 011050cd-21b6-4150-9503-18fa3f771626
translation-type: tm+mt
source-git-commit: 552f93f1f630c64bbe3d5c8a87c4f5895ae6868c
workflow-type: tm+mt
source-wordcount: '763'
ht-degree: 1%

---


# Menu&#39;s{#about-menus}

Met menu&#39;s kunt u de presentatielaag aanpassen.

## Menu&#39;s gebruiken {#concept_68123CE5CF4447B59217B5D721424E32}

Voeg menu&#39;s toe die aan montages binnen uw onderzoek in kaart brengen. Elk item in een menu geeft de waarde op voor de instelling van het menu. U kunt de menulabels ook aanpassen.

In uw presentatiesjabloon kunt u verwijzen naar de gedefinieerde menu&#39;s. Vervolgens kunt u ze in elke gewenste HTML-component plaatsen, zoals een selectiecomponent. Met deze combinatie kunnen gebruikers hun zoekresultaten aanpassen. Er worden drie menutypen ondersteund: sorteren, tellen en navigeren.

## Een nieuw menu toevoegen {#task_EE171532D3AE477FAFE8C2F4077A6D73}

U kunt menu&#39;s toevoegen die aan montages binnen uw onderzoeksresultaten in kaart brengen.

<!-- 

t_adding_a_new_menu.xml

 -->

>[!NOTE]
>
>Zorg ervoor dat u naar het menu in uw presentatiesjabloon verwijst, zodat dit op de website zichtbaar is.

**Een nieuw menu toevoegen**

1. Klik in het menu Product op **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Menus]**.
1. Klik op de [!DNL Menus] pagina **[!UICONTROL Add New Menu]**.
1. Stel op de [!DNL Add Menu] pagina de gewenste opties in.

   Deze instellingen zijn van invloed op zowel het gedrag als de standaardpresentatie van een broodkruimel. U kunt enkele van deze instellingen overschrijven met de instellingen van de presentatiesjabloon.

   Zie [Menu&#39;s](../c-about-design-menu/c-about-menus.md#concept_68123CE5CF4447B59217B5D721424E32).

   <!-- 
   r_add_menu_options.xml
   -->

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Menunaam </p> </td> 
      <td colname="col2"> <p>Naam van het menu. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Type menu </p> </td> 
      <td colname="col2"> <p>Hiermee stelt u een van de volgende drie menutypen in: </p> <p> 
      <ul id="ul_7E66ACC1DA494B20BEC3B0B2CCAB103A"> 
      <li id="li_D81876660A8B48AFB70D3317063FBF6F"> <span class="uicontrol"> Sorteren </span> <p>Hiermee ordent u de zoekopdracht op een van de door u gedefinieerde metagegevenstypen. </p> <p>U kunt bijvoorbeeld een sorteermenu definiëren met de volgende typen metagegevens: drie relevante punten; een aangepast metagegevensveld, zoals een beschikbaarheidscode; en prijs. Aan de drie items kunnen respectievelijk de labels "Sorteren op relevantie", "Sorteren op beschikbaarheid" en "Sorteren op prijs" worden toegekend. Wanneer u dit in uw presentatiesjabloon opneemt, kan de klant dit besturingselement gebruiken om de zoekresultaten te sorteren. </p> </li> 
      <li id="li_63AE06B544B64DCAA8C55031B3DFFFF7"> <span class="uicontrol"> Aantal </span> <p>Hiermee definieert u het aantal zoekresultaten dat moet worden weergegeven. Dit menutype is toegewezen aan de cgi-parameter <span class="varname"> sp_c </span>. </p> <p>Zie <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" format="dita" scope="local"> CGI-parameters voor achtergrondzoekopdrachten </a>. </p> </li> 
      <li id="li_EEC810D420FF41498ECE49EBAAB33BE5"> <span class="uicontrol"> Navigatie </span> <p>Hiermee wordt een set statische URL's opgegeven die aan menu-items zijn gekoppeld. Doorgaans wordt een navigatiemenu gebruikt om een navigatiebalk op het hoogste niveau te maken op de pagina met zoekresultaten. </p> <p>U kunt bijvoorbeeld een menu maken met vrouwen, mannen, jongens en meisjes, waarin de menu-items er als volgt uitzien: 
      <code>
        /?q1=womens;x1=gender 
      </code>, 
      <code>
        /?q1=mens;x1=gender 
      </code> </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Merchandising </p> 
        <!--DONT' KNOW WHAT THIS DOES--> </td> 
      <td colname="col2"> <p>Deze optie is alleen beschikbaar als u het menutype <span class="uicontrol"> Sorteren hebt gekozen. </span> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Aantal items in menu </p> </td> 
      <td colname="col2"> <p>Hiermee geeft u het aantal items in een menu op. Als u deze instelling wijzigt, worden velden toegevoegd aan of verwijderd uit het formulier. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Standaarditem </p> </td> 
      <td colname="col2"> <p>Hiermee kunt u selecteren welk menu-item standaard wordt weergegeven. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Itemwaarde </p> </td> 
      <td colname="col2"> <p>De itemwaarde is afhankelijk van het type menu dat u hebt ingesteld. </p> 
        <ul id="ul_2F14E6AA673640578A2D5161FD9D13EF"> 
        <li id="li_5017EC6E4ACB4B8E99E0AA61CBAAFFAE"> Type menu Sorteren <p>Hiermee wordt aangegeven waarop het geselecteerde item in het menu moet worden gesorteerd. De geselecteerde items worden gevuld met velden met sorteerbare metagegevens. </p> <p>Voor één item kunt u op drie metagegevensvelden sorteren. De sortering wordt uitgevoerd in de opgegeven volgorde. </p> </li> 
        <li id="li_CC6BAFBF969C4367A71B55F08E0758D1"> Type menu Tellen <p>Hier kunt u opgeven hoeveel resultaten u wilt retourneren wanneer de klant dit menu-item selecteert. </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Itemlabel </p> </td> 
      <td colname="col2"> <p>Het itemlabel is afhankelijk van het type menu dat u hebt ingesteld. </p> 
        <ul id="ul_957BF01235F84748B5EB7062D6AEAC41"> 
        <li id="li_03FB2E2C96134A2B8E08154F87F0CD55"> Type menu Sorteren <p>Identificeert het douanelabel dat uw klant moet zien wanneer zij dit punt in het menu bekijken. </p> </li> 
        <li id="li_C9FE2BC46D9443FB85FEB837C7CA45E1"> Type menu Tellen <p>Hiermee wordt het aangepaste label aangegeven dat u voor dit menu-item wilt weergeven. </p> </li> 
        </ul> </td> 
      </tr> 
    </tbody> 
    </table>

1. Klik op **[!UICONTROL Add]**.
1. (Optioneel) Voer op de [!DNL Menus] pagina een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om de aangebrachte wijzigingen terug te draaien.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie Live-instellingen [weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)spoelen.

## Een menu bewerken {#task_0770DBFD0C7046169097FB6F771B9114}

U kunt de instellingen van elk menu bewerken dat u hebt toegevoegd.

<!-- 

t_editing_a_menu.xml

 -->

>[!NOTE]
>
>Zorg ervoor dat u naar het menu in uw presentatiesjabloon verwijst, zodat dit op de website zichtbaar is.

**Een menu bewerken**

1. Klik in het menu Product op **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Menus]**.
1. Klik in de [!DNL Menus] pagina helemaal rechts van **[!UICONTROL Edit]** de menunaam.
1. Stel op de [!DNL Edit Menu] pagina de gewenste opties in.

   Zie de optietabel onder [Een nieuw menu](../c-about-design-menu/c-about-menus.md#task_EE171532D3AE477FAFE8C2F4077A6D73)toevoegen.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Optioneel) Voer op de [!DNL Menus] pagina een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om de aangebrachte wijzigingen terug te draaien.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie Live-instellingen [weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)spoelen.

## Een menu verwijderen {#task_645E212311A045CD8D9D906878165F47}

U kunt elk menu verwijderen dat u hebt toegevoegd.

<!-- 

t_deleting_a_menu.xml

 -->

**Een menu verwijderen**

1. Klik in het menu Product op **[!UICONTROL Design]** > **[!UICONTROL Navigation]** **[!UICONTROL Menus]**
1. Klik in de [!DNL Menus] pagina helemaal rechts van **[!UICONTROL Delete]** de menunaam.
1. Klik in het [!DNL Confirmation] dialoogvenster op **[!UICONTROL OK]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om de aangebrachte wijzigingen terug te draaien.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie Live-instellingen [weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)spoelen.

