---
description: 'null'
seo-description: 'null'
seo-title: '&Zoeken;amp;Opmerkingen bij de release 8.13.0 promoten (16-04-2014)'
solution: Target
title: '&Zoeken;amp;Opmerkingen bij de release 8.13.0 promoten (16-04-2014)'
topic: Release Notes,Site search and merchandising
uuid: b3524992-ff00-4a7c-a404-078242456734
translation-type: tm+mt
source-git-commit: 9d5ac055d665b39d09b28063179d74a389d7f830
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 0%

---


# Opmerkingen bij de release van Search&amp;Promote 8.13.0 (16-04-2014){#search-promote-release-notes}

| Nieuwe functie en verbetering | Beschrijving |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dynamische Facturen met volledige ondersteuning voor tabelovereenkomsten | Sommige klanten hadden vele &quot;SKU niveau&quot;attributen die zij wilden selecteren en tonen door middel van Dynamische Facetten. Als dusdanig, kunt u naar keuze elk dynamisch facetgebied met maximaal één lijstnaam in een statische rekeningsconfiguratie associëren. Deze tabelrelaties kunnen vervolgens tijdens de zoektijd worden toegepast op alle dynamische facetvelden die bij de zoekopdracht zijn betrokken. Zie [Informatie over dynamische feiten](../c-about-design-menu/c-about-dynamic-facets.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899). |

**Oplossingen**

* Het veld met de gegevensweergavebeschrijving is gewijzigd en gebruikt nu de tag `<search-display-field>` in plaats van `<search-description>`.
* Een eigenschap in de Schakelaar van de Index werd toegevoegd om tot Primaire Sleutel de aaneenschakeling van twee of meer gebieden te maken.
* Veranderde AttribuutLoader-Regen-Toegelaten manuscript `attributeloader-regen.pl` in niet HTML-codeert waarden.
* Gelijke index-tijd en onderzoek-tijd whitespace behandeling voor &quot;waaier onderzoek&quot;vragen.
* Het toevoegen van een bedrijfsregel resulteerde soms in een fout toen de Dynamische Facetten werd toegelaten.

   Zie [Informatie over bedrijfsregels](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

* Door een JavaScript-fout kon geen definitie worden toegevoegd of bewerkt in **Settings** > **SPIN** > **IndexConnector**.
* Nadat een BedrijfsRegel werd bewaard leek het dat toen de tijd tijdens de verwezenlijking van de Regel van het Bedrijfs werd geselecteerd het aan de tijdzone van GMT in gebreke bleef. Nadat deze was opgeslagen, bleek dat de tijdzone van de account van kracht werd.

   Zie [Informatie over bedrijfsregels](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

* De sortering van bedrijfsregels in Stage werkte niet correct.

   Zie [Informatie over bedrijfsregels](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

* De rapportage over zoekprestaties is verbeterd doordat u rapporten kunt plannen voor verzending via e-mail.
* Het vaste programma van de bedrijfsregel veranderde automatisch in de Tijd van de Besparing van het Daglicht.

   Zie [Informatie over bedrijfsregels](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

* Als een groot aantal dynamische facetvelden is gedefinieerd, hebben gebruikers langzame zoekresponstijden doorgemaakt.
* Er hebben zich fouten voorgedaan in de index van het bereik.
* Dynamic Media Classic access in niet-Noord-Amerikaanse datacenters werd verbroken.
* De validatiefunctie van SPIN XPath heeft een fout geretourneerd die positief is voor false.

* Na SPIN laat/maakt verrichting onbruikbaar, werd de gebruiker opnieuw gericht aan de lid centrum login pagina.

