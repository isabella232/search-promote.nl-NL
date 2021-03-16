---
description: '&Zoeken;amp;Opmerkingen bij de release 15.3.1 promoten.'
solution: Target
title: '&Zoeken;amp;Opmerkingen bij de release 15.3.1 promoten (24-03-2015)'
topic: Opmerkingen bij de release, zoeken en verhandelen op de site
uuid: f02da5a4-2207-4603-aa05-5cff7be16dd5
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---


# Opmerkingen bij de release van Search&amp;Promote 15.3.1 (24-03-2015){#search-promote-release-notes}

## Nieuwe functies en verbeteringen {#section_2A10EF6B40FC4F2CB2381FFA9FFA64BD}

* Getallen van productmodellen zoeken - Er is een nieuwe taalinstelling toegevoegd waarmee u tokens optioneel kunt splitsen op alfabetische numerieke overgangen. Deze functionaliteit maakt flexibelere free-text overeenkomsten op onderdelen of productstijltokens mogelijk.

   Zie **[!UICONTROL Partial Alphanumeric Matching]** in [Configuring how search terms are match to your web content...](../c-about-linguistics-menu/c-about-words-and-language.md#task_351A9144A51F4B41923BDBACDEF3B616).

* Mogelijkheid toegevoegd om resultaten van gegevensweergave te exporteren.

   Zie [Informatie over gegevensweergaven](../c-about-reports-menu/c-about-data-views.md#concept_DCA897D074464BC1861AA47B40CC86C3).

* Dynamisch gegenereerde waaiers voor eigenschappen die automatisch met facetwaarden worden ingevoerd.

   Adobe Systems vereist momenteel dat u inhoud ter identificatie van bereikwaarden opgeeft om dit te doen. Bij een prijs van 10 genereert u bijvoorbeeld een tekenreeks tussen $10 en $20. Of Adobe Systems vereist dat u Filteren met scripts gebruikt. Nieuwe kenmerken toegevoegd aan de definitie van een metagegevensveld, alleen voor `Type=Number`-velden. De nieuwe opties associëren het numerieke gebied met een `Type=Text` gebied, en specificeren configuratieinformatie die beschrijft hoe de waaierbeschrijving wordt gebouwd.

   Zie [Een nieuw metatag toevoegen gebied](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).

## Oplossingen {#section_22D1AFC99F394D569898828A0D3C419D}

* Het dialoogvenster voor het bewerken van facetrails moet gefaseerde facetten bevatten.
* Lege zoekresultaten voor de zoekmodus &quot;ingesloten&quot;, voor een zoekopdracht met Japanse tekens.
* De Tika-omzetting van Word .docx- dossiers bevolkt nu `title` attributen.
* Foutieve &quot;dubbele banner&quot;berichten in **[!UICONTROL Banner]** manager corrigeren.
* [!DNL Dynamic Media Classic] banners zijn nu protocol-agnostisch.
* Het **[!UICONTROL Table Name]**-veldkenmerk was soms verborgen tijdens het bewerken van door de gebruiker gedefinieerde velden in de gebruikersinterface van metagegevens, zelfs als **[!UICONTROL Dynamic Facets]** was ingeschakeld voor de account.
* **[!UICONTROL Recent Searches]** niet-ASCII-tekens niet meer vermenigvuldigen.
* MDI-velden kunnen worden gevuld zonder dat er een scriptfilter moet worden toegepast.
* Onjuiste codering in suggesties.
* trigger &#39;&#39;other facet selected&#39;&#39; werkt nu correct met complexe bedrijfsregels.

