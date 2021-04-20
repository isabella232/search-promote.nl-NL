---
description: '&Zoeken;amp;Opmerkingen bij de release 15.1.1 promoten.'
solution: Target
title: '&Zoeken;amp;Opmerkingen bij de release 15.1.1 promoten (15-01-2015)'
topic: Release Notes,Site search and merchandising
uuid: 070f9c46-426f-4ca1-80c7-8ca53d40a402
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---


# Opmerkingen bij de release van Search&amp;Promote 15.1.1 (15-01-2015){#search-promote-release-notes}

## Nieuwe functie {#section_2A10EF6B40FC4F2CB2381FFA9FFA64BD}

* Voorheen werden taalkundige kenmerken zoals stammen, synoniemen enzovoort altijd toegepast op trefwoorden in de regels voor zoekopdrachten met instructies. Nu kunt u deze uitbreiding onbruikbaar maken zodat het sleutelwoord wordt gebruikt zoals is.

   Wanneer u triggervoorwaarden wilt toepassen op een bedrijfsregel, selecteert u [!DNL Advanced Rule Builder] in de eerste vervolgkeuzelijst **[!UICONTROL If any/all of the following conditions are met]** in **[!UICONTROL keyword]** en selecteert u vervolgens de nieuwe operator **[!UICONTROL equal exact]** in de tweede vervolgkeuzelijst.

   Zie [Informatie over bedrijfsregels](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

## Oplossingen en verbeteringen {#section_22D1AFC99F394D569898828A0D3C419D}

* [!DNL Visual Rule Builder] en wordt de waarde van het MDI-veld (Merchandising Document ID) niet  [!DNL Advanced Rule Builder] langer ingekort.
* Aan RBTA gerelateerde indexeringsfouten zijn nu opgelost.
* Als u een bestaande bedrijfsregel bewerkt die de status &quot;goedgekeurd&quot; heeft, wordt de status &quot;goedgekeurd&quot; ingetrokken. U moet [!DNL Advanced Rule Builder] gebruiken om de optie **[!UICONTROL Approved]** opnieuw te controleren, en dan sparen de regel zoals gebruikelijk. Als u geen uitgegeven regel opnieuw goedkeurt, wordt de status van de regel automatisch geplaatst aan WIP (Werk Bezig) op de [!DNL Business Rules] pagina.
* Een nieuwe optie **[!UICONTROL Advanced Search]** is nu beschikbaar op [!DNL Business Rules] pagina voor het betere filtreren van regels.
* Voorwaarde **[!UICONTROL contains word]** toegevoegd om regeltriggers in [!DNL Query Cleaning], [!DNL Pre-Search Rules], [!DNL Post Search Rules] en [!DNL Business Rules] toe te voegen, zodat u eenvoudig woordeinden kunt opgeven.
* De verbeteringen die aan bedrijfsregelnota&#39;s zoals worden aangebracht wanneer u een regel bekijkt, kunt u de notitiegeschiedenis voor die regel nu terugwinnen. Notities worden nu ook aangemeld **[!UICONTROL Reports]** > **[!UICONTROL Change Log]**.
* Vragen met niet-nul `sp_i` waarden worden niet meer uitgevoerd door de [!DNL Adobe Analytics] redirector.

   Zie rij 15 in de lijst in [Achterste onderzoek CGI parameters](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8).

