---
description: ongeldig
seo-description: ongeldig
seo-title: Search&amp;Promote 8.13.0 Release Notes (04/16/2014)
solution: Target
title: Search&amp;Promote 8.13.0 Release Notes (04/16/2014)
topic: Release Notes,Site search and merchandising
uuid: b3524992-ff00-4a7c-a404-078242456734
translation-type: tm+mt
source-git-commit: 9d5ac055d665b39d09b28063179d74a389d7f830

---


# Zoeken en promoten: 8.13.0 Release Notes (04/16/2014){#search-promote-release-notes}

| Nieuwe functie en uitbreiding | Beschrijving |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dynamische Facturen met volledige steun van de lijstgelijke | Sommige klanten hadden vele &quot;het niveau van SKU&quot;attributen die zij wilden selecteren en tonen als Dynamische Facets. Als dusdanig, kunt u elk dynamisch facetgebied met maximaal één lijstnaam in een statische rekeningsconfiguratie naar keuze nu associëren. Die lijstverhoudingen kunnen dan op onderzoek-tijd voor om het even welke dynamische facetgebieden worden toegepast betrokken bij het onderzoek. Zie [over dynamische feiten](../c-about-design-menu/c-about-dynamic-facets.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899). |

**Fixes**

* Veranderde het de beschrijvingsgebied van de gegevensmening om de markering `<search-display-field>` in plaats van te gebruiken `<search-description>`.
* Toegevoegd een eigenschap in de Schakelaar van de Index om de Primaire Sleutel tot de aaneenschakeling van twee of meer gebieden te maken.
* Veranderde het attribuutLoader-Geegene-Toegelaten manuscript `attributeloader-regen.pl` aan niet HTML-codewaarden.
* De aangepaste index-tijd en de onderzoek-tijd whitespace behandeling voor &quot;waaieronderzoek&quot;vragen.
* Het toevoegen van een bedrijfsregel resulteerde soms in een fout toen de Dynamische Facets werd toegelaten.

   Zie [over de bedrijfsregels](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

* Een fout Javascript verhinderde toevoegend of het uitgeven van een definitie in **Montages** > **SPIN** > **IndexConnector**.
* Nadat een BedrijfsRegel werd bewaard leek het dat toen de tijd tijdens de verwezenlijking van de Regel van het Bedrijfs werd geselecteerd het aan de GMT tijdzone in gebreke bleef. Nadat het werd bewaard, bleek dat de Tijdzone van de Rekening toen van kracht werd.

   Zie [over de bedrijfsregels](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

* Het sorteren van bedrijfsregels in Stadium werkte niet correct.

   Zie [over de bedrijfsregels](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

* De prestatiesrapportering van het onderzoek was verbetering door u de capaciteit te geven om rapporten voor e-maillevering te plannen.
* De bedrijfsregel bevestigde planning was automatisch veranderend in de Tijd van de Besparing van het Daglicht.

   Zie [over de bedrijfsregels](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

* Als een groot aantal dynamische facetgebieden werden bepaald, ervaren de gebruikers de langzame tijden van de kernonderzoeksreactie.
* De vervalste fouten van de waaierindex kwamen voor.
* De dynamische Klassieke toegang van Media in niet-Noord-Amerikaanse datacenters werd gebroken.
* De de bevestigingsfunctie van SPIN XPath kwam een fout-positieve fout terug.

* Nadat SPIN toelaat/maak verrichting onbruikbaar, werd de gebruiker opnieuw gericht aan de login van het lidcentrum pagina.

