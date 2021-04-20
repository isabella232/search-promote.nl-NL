---
description: Broodkruimels zijn navigatiebesturingselementen die u aan uw website kunt toevoegen. De broodkruimel geeft klanten terugkoppelen over waar zij binnen een reeks van onderzoeksresultaten zijn. Het helpt hen ook snel terug naar een vorige stap.
solution: Target
subtopic: Navigation
title: Info Broodkruimels
topic: Design,Site search and merchandising
uuid: 3e630a72-a631-4f4f-8aa5-adf2882cdf1c
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 1%

---


# Info over Broodkruimels{#about-breadcrumbs}

Broodkruimels zijn navigatiebesturingselementen die u aan uw website kunt toevoegen. De broodkruimel geeft klanten terugkoppelen over waar zij binnen een reeks van onderzoeksresultaten zijn. Het helpt hen ook snel terug naar een vorige stap.

## Broodkruimels gebruiken {#concept_FB8A943C594A4A1593B118141DA61F03}

De broodkruimels volgen de term die wordt gezocht naar en de verdere facetten die werden geselecteerd om de resultaatreeks te beperken.

Met de instellingen voor de braadcrumb kunt u het besturingselement voor de broodkruimelaag van de zoekpresentatie aanpassen. Als uw presentatielaag meer dan één reeks onderzoeksresultaten heeft, handelt de broodkruimelcontrole op het primaire onderzoek op de pagina.

U kunt een broodkruimel uitgeven om het standaardgedrag, maximumwaardebreedte, en waardeuitbreiding te veranderen, en te selecteren of om de vraagtermijn te omvatten.

## Een nieuwe broodkruimel {#task_2FFA94F82AE74F10BDDE7367CDCEAE8B} toevoegen

U kunt een bar toevoegen van de broodkruimel zodat een klant kan volgen waar zij op uw website zijn.

<!-- 

t_adding_a_new_breadcrumb.xml

 -->

>[!NOTE]
>
>Zorg ervoor dat u naar de broodkruimel in uw presentatiesjabloon verwijst zodat deze op de website zichtbaar is.

**Een nieuwe broodkruimel toevoegen**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Breadcrumbs]**.
1. Klik op [!DNL Breadcrumbs] op de pagina.**[!UICONTROL Add Breadcrumb]**
1. Stel op de pagina [!DNL Add Breadcrumb] de gewenste opties in.

   Deze instellingen zijn van invloed op zowel het gedrag als de standaardpresentatie van een broodkruimel. U kunt enkele van deze instellingen overschrijven met de instellingen van de presentatiesjabloon.

   <!-- 
   
   r_breadcrumb_options.xml
    
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
      <td colname="col1"> <p>Naam van doorhalingskruimel </p> </td> 
      <td colname="col2"> <p>De naam van het breadcrumb. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Gedrag </p> </td> 
      <td colname="col2"> <p>Hiermee stelt u een van de volgende drie gedragingen voor broodkruimels in: </p> <p> 
      <ul id="ul_7E66ACC1DA494B20BEC3B0B2CCAB103A"> 
        <li id="li_D81876660A8B48AFB70D3317063FBF6F"> <span class="uicontrol"> Ga naar  </span> <p>Ga om alle broodkruimels na te verwijderen die worden geklikt, en een nieuwe onderzoek op dat punt te beginnen. </p> </li> 
        <li id="li_63AE06B544B64DCAA8C55031B3DFFFF7"> <span class="uicontrol"> Verwijderen  </span> <p>Verwijder schrapt uit de weg de broodkruimel die de klant klikte en begint dan een nieuwe onderzoek. Dit gedrag is nuttig wanneer u de klant stappen in het boren neer door het onderzoek wilt ongedaan maken. </p> </li> 
        <li id="li_EEC810D420FF41498ECE49EBAAB33BE5"> <span class="uicontrol"> Neerzetten  </span> <p>Met Droppen verwijdert u alle broodkruimels. </p> </li> 
      </ul> </p> <p> Stel dat u een breadcrumb hebt van 1 &gt; 2 &gt; 3 &gt; 4. Wanneer een klant op "2"klikt, heeft het de volgende resultaten, die op het gedrag worden gebaseerd u hebt gekozen: </p> <p> 
      <ul id="ul_96FCD8E4C3704B45B59BC18A7A1AC52A"> 
        <li id="li_B880037088DF426F880788EAA3072180">Ga naar - 1 &gt; 2 </li> 
        <li id="li_D0F07A15DCD043EFA4563632ED33A9E2">Verwijderen - 1 &gt; 3 &gt; 4 </li> 
        <li id="li_D848ED44B4E44538AA92010F9F186224"> Daling - De volledige breadcrumb wordt weggelaten, waardoor de klant terug naar het punt komt voordat hij of zij naar beneden ging boren. </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Max. waardebreedte </p> </td> 
      <td colname="col2"> <p>Hiermee geeft u de lengte op van elke waarde in het trail breadcrumb. U geeft de instelling op als een aantal tekens. </p> <p>Als u bijvoorbeeld 6 instelt, kan het trail van de broodkruimel maximaal 6 tekens lang zijn, inclusief spaties. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Waardeextensie </p> </td> 
      <td colname="col2"> <p>Geeft aan welke ellipsen moeten worden gebruikt wanneer een breadcrumb wordt afgekapt. </p> <p>Standaard een ".." (ellipsen) wordt gebruikt. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Zoekterm opnemen </p> </td> 
      <td colname="col2"> <p>Controls the presence of query term in a breadcrumb. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Door gebruiker gedefinieerde kruimels inschakelen </p> </td> 
      <td colname="col2"> <p>Schakel deze optie in om de door de gebruiker gedefinieerde items in breadcrumbs te gebruiken met de parameters <span class="codeph"> uX=[name]&amp;[name]=[value] </span> in de URL. U kunt verwerkingsregels gebruiken om deze parameters op de gewenste manier af te handelen. </p> <p>Als deze functie bijvoorbeeld is ingeschakeld en u de URL hebt, <code> https://search.host.com/?1=category&amp;q1=Clothes&amp;u2= 
          type&amp;type=Men&amp;x3=kind&amp;q3=Sweater </code> als u facetten <span class="codeph"> <span class="varname"> categorie </span> </span> en <span class="codeph"> <span class="varname"> soort </span> </span>  hebt, ziet uw breadcrumb eruit als <span class="codeph"> Kleuren &gt; Mannen &gt; Zwevend </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Door gebruiker gedefinieerde mapnamen </p> </td> 
      <td colname="col2"> <p>Een door komma's gescheiden lijst met alle mogelijke namen van door de gebruiker gedefinieerde breadcrumb-items. </p> <p>Deze optie is alleen beschikbaar als u <span class="uicontrol"> Door gebruiker gedefinieerde kruimels inschakelen </span>. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Klik op **[!UICONTROL Add]**.
1. (Optioneel) Voer op de pagina [!DNL Breadcrumbs] een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een broodkruimel {#task_583481D9A23E4E0F97AEB18E72CBE13F} bewerken

U kunt de instellingen bewerken van alle broodkruimels die u hebt toegevoegd.

<!-- 

t_editing_a_breadcrumb.xml

 -->

>[!NOTE]
>
>Zorg ervoor dat u naar de broodkruimel in uw presentatiesjabloon verwijst zodat deze op de website zichtbaar is.

**Een broodkruimel bewerken**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Breadcrumbs]**.
1. Op [!DNL Breadcrumbs] pagina, klik **[!UICONTROL Edit]** aan het uiterste recht van een breadcrumb naam.
1. Stel op de pagina [!DNL Edit Breadcrumb] de gewenste opties in.

   Zie de optietabel onder [Een nieuwe broodkruimel](../c-about-design-menu/c-about-breadcrumbs.md#task_2FFA94F82AE74F10BDDE7367CDCEAE8B) toevoegen.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Optioneel) Voer op de pagina **[!UICONTROL Breadcrumb]** een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een broodkruimel {#task_401C6E481A744284906E15A29E04F757} verwijderen

U kunt alle toegevoegde broodkruimels verwijderen.

<!-- 

t_deleting_a_breadcrumb.xml

 -->

**Een broodkruimel verwijderen**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Breadcrumbs]**.
1. Op [!DNL Breadcrumbs] pagina, klik **[!UICONTROL Delete]** aan het uiterste recht van een breadcrumb naam.
1. Klik in het dialoogvenster [!DNL Confirmation] op **[!UICONTROL OK]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

