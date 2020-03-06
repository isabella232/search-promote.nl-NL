---
description: ongeldig
seo-description: ongeldig
seo-title: Search&amp;Promote 15.1.1 Release Notes (01/15/2015)
solution: Target
title: Search&amp;Promote 15.1.1 Release Notes (01/15/2015)
topic: Release Notes,Site search and merchandising
uuid: 070f9c46-426f-4ca1-80c7-8ca53d40a402
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# Zoeken en promoten: 15.1.1 Opmerkingen bij release (01/15/2015){#search-promote-release-notes}

## Nieuwe functie {#section_2A10EF6B40FC4F2CB2381FFA9FFA64BD}

* Vroeger, werden de taalkunde zoals stammen, synoniemen, enzovoort, altijd toegepast op sleutelwoorden in Geleide Regels van het Onderzoek. Nu kunt u deze uitbreiding onbruikbaar maken zodat het sleutelwoord wordt gebruikt zoals is.

   Wanneer u trekkervoorwaarden op een bedrijfsregel wilt toepassen, in [!DNL Advanced Rule Builder], na **[!UICONTROL If any/all of the following conditions are met]**, in de eerste drop-down lijst, selecteer **[!UICONTROL keyword]**, en selecteer dan de nieuwe exploitant **[!UICONTROL equal exact]** in de tweede drop-down lijst.

   Zie [over de bedrijfsregels](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

## Fixen en verbeteringen {#section_22D1AFC99F394D569898828A0D3C419D}

* [!DNL Visual Rule Builder] en beknot [!DNL Advanced Rule Builder] niet meer de MDI (Merchandising Document ID) gebiedswaarde.
* RBTA-gerelateerde indexeringsmislukkingen zijn nu bevestigd.
* Het uitgeven van een bestaande bedrijfsregel die een status van &quot;goedgekeurd&quot;heeft herroept nu de &quot;goedgekeurde&quot;status. U moet gebruiken [!DNL Advanced Rule Builder] om de optie opnieuw te controleren **[!UICONTROL Approved]**, en dan sparen de regel zoals gebruikelijk. Als u geen uitgegeven regel opnieuw goedkeurt, wordt de status van de regel automatisch geplaatst aan WIP (het Werk lopend) op de [!DNL Business Rules] pagina.
* Een nieuwe **[!UICONTROL Advanced Search]** optie is nu beschikbaar op de [!DNL Business Rules] pagina voor het betere filtreren van regels.
* Toegevoegde **[!UICONTROL contains word]** voorwaarde aan regeltrekkers binnen, [!DNL Query Cleaning], [!DNL Pre-Search Rules], en [!DNL Post Search Rules][!DNL Business Rules], om u te laten woordonderbrekingen gemakkelijk specificeren.
* De verbeteringen die aan bedrijfsregelnota&#39;s worden gemaakt zoals wanneer u een regel bekijkt, kunt u de nota&#39;s geschiedenis voor die regel nu terugwinnen. Ook, worden de nota&#39;s nu het programma geopend **[!UICONTROL Reports]** > **[!UICONTROL Change Log]**.
* De vragen met nonzero `sp_i` waarden worden niet meer in werking gesteld door [!DNL Adobe Analytics] redirector.

   Zie rij 15 in de lijst in de parameters [van het Onderzoek van het](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)Achterste CGI.

