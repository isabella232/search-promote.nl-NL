---
description: De broodkruimels zijn een navigatiecontrole die u aan uw website kunt toevoegen. De broodkruimel geeft klanten terugkoppelt op waar zij binnen een reeks van het onderzoeksresultaat zijn. Het helpt hen ook snel terug naar een vorige stap.
seo-description: De broodkruimels zijn een navigatiecontrole die u aan uw website kunt toevoegen. De broodkruimel geeft klanten terugkoppelt op waar zij binnen een reeks van het onderzoeksresultaat zijn. Het helpt hen ook snel terug naar een vorige stap.
seo-title: Over Breadcrumbs
solution: Target
subtopic: Navigation
title: Over Breadcrumbs
topic: Design,Site search and merchandising
uuid: 3e630a72-a631-4f4f-8aa5-adf2882cdf1c
translation-type: tm+mt
source-git-commit: 7f1b5d94e8002992d62ec1e3dce11f9c5605fde8

---


# Over Breadcrumbs{#about-breadcrumbs}

De broodkruimels zijn een navigatiecontrole die u aan uw website kunt toevoegen. De broodkruimel geeft klanten terugkoppelt op waar zij binnen een reeks van het onderzoeksresultaat zijn. Het helpt hen ook snel terug naar een vorige stap.

## Breadcrumbs gebruiken {#concept_FB8A943C594A4A1593B118141DA61F03}

De broodkruimels volgen de termijn waarnaar wordt gezocht en de verdere facetten die werden geselecteerd om onderaan de resultaatreeks te versmallen.

Gebruik de montages van de Breadcrumb om de broodkruimelcontrole van uw laag van de onderzoekspresentatie aan te passen. Als uw presentatielaag meer dan één reeks onderzoeksresultaten heeft, handelt de broodkruimelcontrole op het primaire onderzoek op de pagina.

U kunt een broodkruimel uitgeven om het standaardgedrag, de maximumwaardebreedte, en de waardeuitbreiding te veranderen, en te selecteren of om de vraagtermijn te omvatten.

## Een nieuwe broodkruimel toevoegen {#task_2FFA94F82AE74F10BDDE7367CDCEAE8B}

U kunt een broodkruimelbar toevoegen zodat een klant kan volgen waar zij op uw website zijn.

<!-- 

t_adding_a_new_breadcrumb.xml

 -->

>[!NOTE]
>
>Ben zeker u de broodkruimel in uw presentatiemalplaatje van verwijzingen voorziet zodat het op de website zichtbaar is.

**Om een nieuwe broodkruimel toe te voegen**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Breadcrumbs]**.
1. Voor de [!DNL Breadcrumbs] pagina, klik **[!UICONTROL Add Breadcrumb]**.
1. Voor de [!DNL Add Breadcrumb] pagina, plaats de opties die u wilt.

   Deze montages beïnvloeden zowel het gedrag als de standaardpresentatie van een broodkruimel. U kunt sommige van deze montages als montages van het presentatiemalplaatje met voeten treden.

   <!-- 
   
   r_breadcrumb_options.xml
    
    -->

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Optie </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Naam van broodkruimel </p> </td> 
      <td colname="col2"> <p>De naam van de broodkruimel. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Gedrag </p> </td> 
      <td colname="col2"> <p>Plaatst één van de volgende drie broodkruimelgedrag: </p> <p> 
      <ul id="ul_7E66ACC1DA494B20BEC3B0B2CCAB103A"> 
        <li id="li_D81876660A8B48AFB70D3317063FBF6F"> <span class="uicontrol"> Goto </span> <p>Ga alle broodkruimels na verwijderen die wordt geklikt, en begint een nieuwe onderzoek op dat punt. </p> </li> 
        <li id="li_63AE06B544B64DCAA8C55031B3DFFFF7"> <span class="uicontrol"> Verwijderen </span> <p>Verwijder schrapt uit de weg de broodkruimel die de klant klikte en dan een nieuw onderzoek begint. Dit gedrag is nuttig wanneer u de klant stappen wilt laten ongedaan maken in het boren neer door het onderzoek. </p> </li> 
        <li id="li_EEC810D420FF41498ECE49EBAAB33BE5"> <span class="uicontrol"> neerzetten </span> <p>De daling verwijdert alle broodkruimels. </p> </li> 
      </ul> </p> <p> Bijvoorbeeld, veronderstel u een broodkruimel van 1 &gt; 2 &gt; 3 &gt; 4 hebt. Wanneer een klant op "2"klikt, heeft het de volgende resultaten, die op het gedrag worden gebaseerd u hebt gekozen: </p> <p> 
      <ul id="ul_96FCD8E4C3704B45B59BC18A7A1AC52A"> 
        <li id="li_B880037088DF426F880788EAA3072180">Ga naar - 1 &gt; 2 </li> 
        <li id="li_D0F07A15DCD043EFA4563632ED33A9E2">Verwijderen - 1 &gt; 3 &gt; 4 </li> 
        <li id="li_D848ED44B4E44538AA92010F9F186224"> Daling - De volledige broodkruimel wordt gelaten vallen, die de klant terug naar het punt nemen alvorens zij begonnen te boren neer. </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Maximale toegevoegde waarde </p> </td> 
      <td colname="col2"> <p>Specificeert de lengte van elke waarde in het broodkruimelspoor. U specificeert het plaatsen als aantal karakters. </p> <p>Bijvoorbeeld, betekent het plaatsen van 6 dat het broodkruimelspoor tot 6 lange karakters, met inbegrip van ruimten kan zijn. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Value Extension </p> </td> 
      <td colname="col2"> <p>Specificeert de ellips om te gebruiken wanneer een broodkruimel beknot is. </p> <p>Standaard een "..." (ellipsen) wordt gebruikt. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Omvat de Termijn van de Vraag </p> </td> 
      <td colname="col2"> <p>Controleert de aanwezigheid van vraagtermijn in een broodkruimel. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Laat Gebruiker - bepaalde Crumbs toe </p> </td> 
      <td colname="col2"> <p>Controle om u te laten de Gebruiker - bepaalde punten in broodkruimels gebruiken gebruikend <span class="codeph"> uX=[naam] &amp; [naam]=[waarde] </span> parameters in URL. U kunt verwerkingsregels gebruiken om deze parameters te behandelen de manier u wilt. </p> <p>Bijvoorbeeld, als deze eigenschap wordt toegelaten en u URL hebt, <code> https://search.host.com/?1=category&amp;q1=Clothes&amp;u2= 
          type&amp;type=Men&amp;x3=kind&amp;q3=Sweater </code> in het geval als u facetten <span class="codeph"> categorie <span class="varname"> en </span> soort hebt </span> , zal uw broodkruimel als <span class="codeph"> <span class="varname"> </span> </span><span class="codeph"> </span>Kleren &gt; Mannen &gt; Vader  kijken. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Door de gebruiker gedefinieerde namen van Crumb </p> </td> 
      <td colname="col2"> <p>Een komma-gescheiden lijst van alle mogelijke namen van user-defined broodkruimelpunten. </p> <p>Deze optie is slechts beschikbaar als u controleert <span class="uicontrol"> laat Gebruiker - bepaalde Krumbs toe </span>. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Klik op **[!UICONTROL Add]**.
1. (Facultatief) op de [!DNL Breadcrumbs] pagina, doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een broodkruimel bewerken {#task_583481D9A23E4E0F97AEB18E72CBE13F}

U kunt de montages van om het even welke broodkruimel uitgeven die u hebt toegevoegd.

<!-- 

t_editing_a_breadcrumb.xml

 -->

>[!NOTE]
>
>Ben zeker u de broodkruimel in uw presentatiemalplaatje van verwijzingen voorziet zodat het op de website zichtbaar is.

**Om een broodkruimel uit te geven**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Breadcrumbs]**.
1. Voor de [!DNL Breadcrumbs] pagina, klik **[!UICONTROL Edit]** aan uiterst rechts van een broodkruimelnaam.
1. Voor de [!DNL Edit Breadcrumb] pagina, plaats de opties die u wilt.

   Zie de lijst van opties onder het [Toevoegen van een nieuwe broodkruimel](../c-about-design-menu/c-about-breadcrumbs.md#task_2FFA94F82AE74F10BDDE7367CDCEAE8B).
1. Klik op **[!UICONTROL Save Changes]**.
1. (Facultatief) op de **[!UICONTROL Breadcrumb]** pagina, doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een broodkruimel verwijderen {#task_401C6E481A744284906E15A29E04F757}

U kunt om het even welke broodkruimel schrappen die u hebt toegevoegd.

<!-- 

t_deleting_a_breadcrumb.xml

 -->

**Om een broodkruimel te schrappen**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Breadcrumbs]**.
1. Voor de [!DNL Breadcrumbs] pagina, klik **[!UICONTROL Delete]** aan uiterst rechts van een broodkruimelnaam.
1. Klik in het [!DNL Confirmation] dialoogvenster op **[!UICONTROL OK]**.
1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

