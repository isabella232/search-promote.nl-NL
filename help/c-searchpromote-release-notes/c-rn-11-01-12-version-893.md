---
description: 'null'
seo-description: 'null'
seo-title: '&Zoeken;amp;Opmerkingen bij de release 8.9.3 promoten (11/01/2012)'
solution: Target
title: '&Zoeken;amp;Opmerkingen bij de release 8.9.3 promoten (11/01/2012)'
topic: Release Notes,Site search and merchandising
uuid: 7bc7bcb6-f47f-4e05-94e5-a22a13a187b7
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---


# Opmerkingen bij de release van Search&amp;Promote 8.9.3 (11/01/2012){#search-promote-release-notes}

## Opmerkingen bij de release van Search&amp;Promote 8.9.3 (11/01/2012) {#concept_85F5B4B4C40C43FEA3AD63E6EA5593CF}

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nieuwe en verbeterde functies </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Facet Rail </p> </td> 
   <td colname="col2"> <p> 
     <!--3309390--> De nieuwe optie  <span class="uicontrol"> Facet </span> Railsysteem toegevoegd om u te helpen meer controle over de volgorde van facetfamilies en facetnamen (door telling, alfabetisch) geven. </p> <p>Zie <a href="../c-about-design-menu/c-about-facet-rails.md#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB" format="dita" scope="local"> Informatie over facetrails</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Geneste facetten </p> </td> 
   <td colname="col2"> <p> Toegevoegde ondersteuning voor alternatieve sortering van geneste facetten. </p> <p>Zie <a href="../c-about-design-menu/c-about-facet-rails.md#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB" format="dita" scope="local"> Informatie over facetrails</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Notities in de rangorde </p> </td> 
   <td colname="col2"> <p> 
     <!--3063772--> Er is een veld  <span class="wintitle"> </span> Notities met meerdere regels toegevoegd aan het dialoogvenster  <span class="wintitle"> Willekeurige </span> metrieke tekens toevoegen en het dialoogvenster  <span class="wintitle"> Metrieke volgorde </span> bewerken voor het rangschikken van regels en definities van regelgroepen. </p> <p>De rangschikkende regelnota's worden getoond op <span class="wintitle"> bepaalt het Rangschikken Regels</span> pagina. De groepsnota's van de regel verschijnen wanneer u de definitie uitgeeft. </p> <p>Zie <a href="../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397" format="dita" scope="local"> Info over Rangschikkende Regels</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Bedrijfsvoorschriften </p> </td> 
   <td colname="col2"> <p> 
     <!--3331637--> Verbeterde ondersteuning voor landingspagina's door natuurlijke resultaten te verwijderen uit een bedrijfsregel met de nieuwe optie  <span class="uicontrol"> Alle resultaten </span> verwijderen. </p> <p>Gebruik deze nieuwe optie in combinatie met andere handelingen voor bedrijfsregels om 'bestemmingspagina's in blik' te maken. Dat wil zeggen dat u de inhoud van een pagina uitsluitend wilt maken door handelingen met bedrijfsregels en dat u de "natuurlijke" resultaten van de zoekopdracht moet negeren. </p> <p>Zie <a href="../c-about-rules-menu/c-about-business-rules.md#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7" format="dita" scope="local"> Een nieuwe bedrijfsregel toevoegen</a> of <a href="../c-about-rules-menu/c-about-business-rules.md#task_375CFA75D1D94D9E92A35DE1228E5087" format="dita" scope="local"> Een bedrijfsregel bewerken</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Banners en bedrijfsregels </p> </td> 
   <td colname="col2"> <p> Er is een supportoptie toegevoegd waarbij u banners voorwaardelijk kunt uitsluiten wanneer de bedrijfsregel die verwijst naar de banner live wordt gedrukt. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Oplossingen**

* De bedrijfsregels werkten inconsistent toen er een [!DNL Stage] index was.
* Autoranking rules are now applied to canned landing pages.

   Zie de optietabel in [Een rangschikkingsregel toevoegen](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A).

* [!DNL promosearch.cgi] heeft geen aanbiedingen geretourneerd.

   Zie [Informatie over zoekopdrachten](../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8).

* Pushing rules that referenced many banners soms failed.

   Zie [Informatie over banners](../c-about-design-menu/c-about-banners.md#concept_5BBE01FEC6134393B43CC917C8CC64DA).

* **[!UICONTROL Did You Mean]** zoekquery in cache plaatsen is nu uitgeschakeld.

   Zie [Bedoelde u](../c-about-linguistics-menu/c-about-did-you-mean.md#concept_7D4F3C29EF184B538B8AE2ECAE0CDC5E).

