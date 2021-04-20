---
description: '&Zoeken;amp;Opmerkingen bij de release 8.9.4 promoten.'
solution: Target
title: '&Zoeken;amp;Opmerkingen bij de release 8.9.4 promoten (17-01-2013)'
topic: Release Notes,Site search and merchandising
uuid: a9d550f6-0a23-4c71-b123-c31b997e7384
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---


# Opmerkingen bij de release van Search&amp;Promote 8.9.4 (17-01-2013){#search-promote-release-notes}

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nieuwe en verbeterde functies </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Regels </p> </td> 
   <td colname="col2"> <p> Toegevoegd de capaciteit om gealigneerde nota's tot stand te brengen wanneer u de Regels van de Schoonmaak van de Vraag, Regels pre-Onderzoek, en Regels na-Onderzoek creeert. In het veld Notities kunt u de regels documenteren en uitleggen. </p> <p>Zie <a href="../c-about-rules-menu/c-about-query-cleaning-rules.md#concept_17F3CDDC3C8A4128AF092A82B777B86C" format="dita" scope="local"> Info over Regels voor het opschonen van query</a>. </p> <p>Zie <a href="../c-about-rules-menu/c-about-pre-search-rules.md#concept_5BF84BB6FACB4645BA9CB7496A01CD1F" format="dita" scope="local"> Informatie over regels voor voorzoeken</a>. </p> <p>Zie <a href="../c-about-rules-menu/c-about-post-search-rules.md#concept_AF6ADFCC0ADF4A788003964939917FDE" format="dita" scope="local"> Informatie over Post-Search Regels</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Zoeken met instructies </p> </td> 
   <td colname="col2"> <p> Toegevoegde tags voor Zoeken met instructies om de totale tijd aan te geven waarin een zoekopdracht is uitgevoerd. </p> <p> <span class="codeph"> &lt;guided-search-time&gt;</span> - Geeft aan hoe lang de zoekopdracht heeft geduurd. De geretourneerde waarde voor de zoektijd wordt opgegeven in ms. </p> <p> <span class="codeph"> &lt;guided-fall-through-searches&gt;</span> - Geeft als resultaat het aantal zoekopdrachten in de kernen die worden gebruikt om de pagina met zoekresultaten samen te stellen. </p> <p> <span class="codeph"> &lt;guided-if-fall-through-search&gt;</span> - Test of het aantal kernzoekopdrachten groter is dan 1. </p> <p>Zie ook Diverse Taal in <a href="../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64" format="dita" scope="local"> de malplaatjemarkeringen van de Presentatie</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Oplossingen**

* In het rapport Voorwaarden wordt nu het sterretje genegeerd.

   Zie [Het rapport met voorwaarden of het rapport Null-zoektermen weergeven...](../c-about-reports-menu/c-about-reports-menu.md#task_53B7ED1582DD4B0E8376546A7AFC789A).

* Open **[!UICONTROL Reports > Null Search Terms Report]**, selecteer een tijdgroef en bekijk dan het rapport. Klik op één woord in het rapport om de zoekopdracht te openen en klik vervolgens nogmaals op Rapport weergeven. Het aantal zoekopdrachten van het trefwoord waarop u klikte, is tweemaal gestegen. Dit is nu opgelost.

   Zie [Het rapport met voorwaarden of het rapport Null-zoektermen weergeven...](../c-about-reports-menu/c-about-reports-menu.md#task_53B7ED1582DD4B0E8376546A7AFC789A).

* Er is een optimalisatie van de prestaties uitgevoerd wanneer u live gaat met de bedrijfsregels.

   Zie [Informatie over bedrijfsregels](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

* De mogelijkheid om in [!DNL Breadcrumbs] te verwijderen werkte niet de hele tijd.

   Zie [Informatie over broodkruimels](../c-about-design-menu/c-about-breadcrumbs.md#concept_FB8A943C594A4A1593B118141DA61F03).

* Tenzij u opnieuw genereerde, stond de re-rangschikkingseigenschap geen veranderde rangschikkingsregels toe om in onderzoeksresultaten van kracht te worden.

   Zie [Informatie over rangschikkingsregels](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397).

   Zie [Over de index opnieuw plaatsen](../c-about-index-menu/c-about-re-rank-index.md#concept_147B0A9FCD51451787DA898E06F7C692).

