---
description: ongeldig
seo-description: ongeldig
seo-title: Search&amp;Promote 8.9.4 Release Notes (01/17/2013)
solution: Target
title: Search&amp;Promote 8.9.4 Release Notes (01/17/2013)
topic: Release Notes,Site search and merchandising
uuid: a9d550f6-0a23-4c71-b123-c31b997e7384
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# Zoeken en promoten: 8.9.4 releasenota&#39;s (01/17/2013){#search-promote-release-notes}

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nieuwe functies en verbeteringen </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Regels </p> </td> 
   <td colname="col2"> <p> Toegevoegd de capaciteit om gealigneerde nota's tot stand te brengen wanneer u de Regels van de Schoonmaak van de Vraag, Vooraf-Onderzoek Regels, en de Regels van het post-Onderzoek creeert. Het notitiegebied laat u de regels documenteren en verklaren. </p> <p>Zie <a href="../c-about-rules-menu/c-about-query-cleaning-rules.md#concept_17F3CDDC3C8A4128AF092A82B777B86C" format="dita" scope="local"> over het Schoonmaken van de Vraag Regels</a>. </p> <p>Zie <a href="../c-about-rules-menu/c-about-pre-search-rules.md#concept_5BF84BB6FACB4645BA9CB7496A01CD1F" format="dita" scope="local"> Voorspelregels</a>. </p> <p>Zie <a href="../c-about-rules-menu/c-about-post-search-rules.md#concept_AF6ADFCC0ADF4A788003964939917FDE" format="dita" scope="local"> Informatie over regels</a>na het zoeken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Begeleide zoekopdracht </p> </td> 
   <td colname="col2"> <p> Toegevoegde Geleide markeringen van het Onderzoek om op de totale tijd te wijzen die een onderzoek nam. </p> <p> <span class="codeph"> &lt;geleide-onderzoek-tijd&gt;</span> - identificeert hoe lang het onderzoek nam. De teruggekeerde waarde van de onderzoekstijd wordt gespecificeerd in ms. </p> <p> <span class="codeph"> &lt;guided-fall-through-search&gt;</span> - Geeft de telling van cores onderzoeken terug die worden gebruikt om de pagina van onderzoeksresultaten te bouwen. </p> <p> <span class="codeph"> &lt;geleid-als-val-door-onderzoek&gt;</span> - test als de telling van kernonderzoeken groter is dan 1. </p> <p>Zie ook Diverse Taal in de malplaatjemarkeringen <a href="../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64" format="dita" scope="local"> van de</a>Presentatie. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Fixes**

* Het Rapport van Termen negeert nu het asteriskkarakter.

   Zie het [Bekijken van het Rapport van Termen of het Volledige Rapport van de Termijnen van het Onderzoek...](../c-about-reports-menu/c-about-reports-menu.md#task_53B7ED1582DD4B0E8376546A7AFC789A).

* Open Rapporten > het Volledige Rapport van de Termijnen van het Onderzoek, selecteer een tijdgroef en bekijk dan het rapport. Klik één woord in het rapport om het onderzoek te openen, en dan het Rapport van de Mening opnieuw te klikken. De onderzoekstelling van het sleutelwoord u klikte steeg tweemaal. Dit is nu opgelost.

   Zie het [Bekijken van het Rapport van Termen of het Volledige Rapport van de Termijnen van het Onderzoek...](../c-about-reports-menu/c-about-reports-menu.md#task_53B7ED1582DD4B0E8376546A7AFC789A).

* Een prestatiesoptimalisering werd gemaakt voor wanneer u BedrijfsRegels levend duwt.

   Zie [over de bedrijfsregels](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

* Het vermogen om in Breadcrumbs te verwijderen werkte niet de hele tijd.

   Zie [over Breadcrumbs](../c-about-design-menu/c-about-breadcrumbs.md#concept_FB8A943C594A4A1593B118141DA61F03).

* Tenzij u Regenerate gebruikte, liet de Re-rank eigenschap geen veranderde Rangschikkende Regels toe om in onderzoeksresultaten van kracht te worden.

   Zie [over rangschikkingsregels](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397).

   Zie [over Re-Rank Index](../c-about-index-menu/c-about-re-rank-index.md#concept_147B0A9FCD51451787DA898E06F7C692).

