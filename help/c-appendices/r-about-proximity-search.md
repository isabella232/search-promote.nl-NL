---
description: Met Proximity Search kunt u een unieke locatie koppelen aan elke pagina op uw website en vervolgens de resultaten zoeken en sorteren op afstand (afstand) van een bepaalde locatie.
seo-description: Met Proximity Search kunt u een unieke locatie koppelen aan elke pagina op uw website en vervolgens de resultaten zoeken en sorteren op afstand (afstand) van een bepaalde locatie.
seo-title: Informatie over zoeken op nabijheid
solution: Target
title: Informatie over zoeken op nabijheid
topic: Appendices,Site search and merchandising
uuid: 24fc9265-3400-46a7-b6e0-4de5b049a39a
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e
workflow-type: tm+mt
source-wordcount: '779'
ht-degree: 0%

---


# Info over nabijheidszoekopdracht{#about-proximity-search}

Met Proximity Search kunt u een unieke locatie koppelen aan elke pagina op uw website en vervolgens de resultaten zoeken en sorteren op afstand (afstand) van een bepaalde locatie.

Stel dat u pagina&#39;s op uw website hebt gevuld met metagegevens van postcode in de Verenigde Staten, zoals:

```
<meta name="zipcode" content="84057">
```

Vervolgens configureert u uw account om de metagegevens van uw ZIP-code te indexeren. In **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]** > **[!UICONTROL Add New Field]** stelt u op de pagina [!DNL Add Field] de volgende opties in:

* Veldnaam: `zip`
* Naam/namen metatag: `zipcode`
* Gegevenstype: **[!UICONTROL Location]**
* Sorteren: **[!UICONTROL Ascending]**
* Standaardeenheden: **[!UICONTROL Miles]**

Na het indexeren van uw site voert u de volgende zoekopdracht uit:

```
...&sp_q_location_1=84057&sp_x_1=zip&sp_q_max_1=100&sp_s=zip_proximity
```

De resultatenset bevat alle documenten die zich binnen 100 mijl van postcode 84057 bevinden, gesorteerd in oplopende volgorde van afstand tot deze postcode.

U kunt ook telefoongebiedcodes gebruiken voor locaties in de Verenigde Staten. U kunt ook breedte-/lengteparen gebruiken om locaties op te geven in de metagegevens van uw site en in uw zoekcriteria. Het locatietype wordt automatisch bepaald op basis van de vorm van de gegevens die worden verstrekt.

Waarden voor locaties met drie cijfers (&quot;DDD&quot;, waarbij elke &quot;D&quot; staat voor een decimaal cijfer van 0-9) worden behandeld als een code voor het telefoongebied van de Verenigde Staten.

De vijf of vijf-dash-vier cijferplaatswaarden (&quot;DDD&quot;of &quot;DDDDD-DDDD&quot;) worden behandeld als postcode van de PostZIP van de Verenigde Staten.

Locatiewaarden in de exacte vorm &quot;±DD.DDDD±DDD.DDDD&quot; worden behandeld als breedte-/lengtepaar. De eerste ondertekende numerieke waarde geeft de breedtegraad aan en de tweede ondertekende numerieke waarde geeft de lengtegraad aan.

**Belangrijk**: Als u een positieve breedtewaarde of een positieve lengtewaarde of beide opgeeft, moet het plusteken (+) in de URL als  `%2b`gecodeerd worden. Anders wordt &quot;+&quot; geïnterpreteerd als een spatie en wordt de waarde niet herkend als een geldige locatie. Stel dat u bijvoorbeeld een breedtewaarde van +49,2394 en een lengtewaarde van -123,1892 hebt. Het locatiegedeelte van de URL met &quot;+&quot;-codering ziet er als volgt uit:

```
...&sp_q_location_1=%2b49.2394-123.1892...
```

* Positieve breedtewaarden geven graden ten noorden van de evenaar aan.
* Negatieve breedtewaarden geven graden ten zuiden van de evenaar aan.
* Positieve lengtewaarden geven het oosten van premier Meridian aan.
* Negatieve lengtewaarden geven graden ten westen van premier Meridian aan.

De waarde &quot;+48,8577+002,2950&quot; vertegenwoordigt bijvoorbeeld 48,8577 graden ten noorden van de evenaar, 2,295 graden ten oosten van de eerste Meridiaan, de exacte locatie van de Eiffeltoren in Parijs, Frankrijk. De numerieke tekens en elk cijfer zijn vereist, zelfs de voorloopnullen en volgnullen. De drie waarden &quot;48.8577+2.2950&quot;, &quot;+48.8577+2.2950&quot; en &quot;+48.8577+02.295&quot; zijn bijvoorbeeld geen locaties. Bij de eerste waarde ontbreekt het voorteken op de breedtegraad. In de tweede waarde ontbreken de twee voorloopnullen op de lengtegraad. Bij de derde waarde ontbreekt het navolgende nul op de lengtegraad. Zorg ervoor dat u uw indexlogboek zorgvuldig voor om het even welke plaats-verwante problemen onderzoekt.

Wanneer u op nabijheid zoekt, is er een speciaal &quot;nabijheidsoutputgebied&quot;gecreeerd voor die onderzoek. Het veld wordt gevuld met de relatieve afstand tussen de locatie die is opgegeven in de zoekcriteria en de locatie die is gekoppeld aan elk zoekresultaat. Dit speciale veld krijgt de naam van het veld voor het locatietype dat wordt gebruikt in de zoekcriteria met &quot;_proximity&quot; toegevoegd aan het einde.

In de bovenstaande voorbeeldzoekopdracht worden de resultaten gesorteerd in oplopende volgorde van &quot;zip_proximity&quot;. Dit is de afstand tussen de opgegeven ZIP-code (84057) en de locatie van het ZIP-veld van elk resultaat. U kunt dit speciale &quot;nabijheidsoutputgebied&quot;ook gebruiken om de relatieve afstand voor elk onderzoeksresultaat, in of kilometers of mijlen te tonen, gebruikend `<Search-Display-Field>` de malplaatjemarkering van het Onderzoek.

Zie [Sjabloontags zoeken](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4).

U kunt ook zonder de optie sp_s zoeken. In dat geval, worden de resultaten gesorteerd door score (sp_s=0, wat het gebrek) is.De score wordt beïnvloed door de relatieve afstand van elk resultaat van de nabijheidsonderzoeksplaats die door middel van de sp_q_location[_#] parameter wordt gespecificeerd. Er wordt een nieuwe cgi-parameter sp_q_max_relevant_distance[#] toegevoegd om optioneel de relevantieberekening te bepalen die op nabijheidszoekopdrachten wordt toegepast.

Hier volgt een zoekvoorbeeld dat betrekking heeft op nabijheid:

```
...&sp_q_location_1=84057&sp_x_1=zip&sp_q_max_1=100&sp_q_2=shirt&sp_x_2=title&sp_q_max_relevant_distance_2=50
```

De resultatenset bevat alle documenten die zich binnen 100 mijl van ZIP-code 84057 bevinden en het woord &quot;shirt&quot; in het titelveld bevatten, gesorteerd op scoring die is beïnvloed door nabijheidsrelevantie-scoring. Een perfecte relevantiescore voor de nabijheidscomponent zou een afstand van 0 vertegenwoordigen. Een minimale relevantierescore voor de nabijheidscomponent zou een afstand van iets meer dan 50 mijl vertegenwoordigen.

U kunt meer informatie over nabijheidsonderzoek leren door `sp_location`, `sp_location_#`, `sp_q_min`, `sp_q_min_#`, `sp_q_max`, `sp_q_max_#`, en `sp_s` in het de verwijzingsonderwerp van de Parameters van het Onderzoek CGI te herzien.

Zie [CGI-parameters doorzoeken](../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890).

Zie [Een nieuw metatag toevoegen gebied](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).
