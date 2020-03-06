---
description: Het Onderzoek van de nabijheid laat u een unieke plaats met om het even welke pagina op uw website associëren, en dan onderzoek en soortresultaten door nabijheid (afstand) van een bepaalde plaats.
seo-description: Het Onderzoek van de nabijheid laat u een unieke plaats met om het even welke pagina op uw website associëren, en dan onderzoek en soortresultaten door nabijheid (afstand) van een bepaalde plaats.
seo-title: Over nabijheidszoekopdracht
solution: Target
title: Over nabijheidszoekopdracht
topic: Appendices,Site search and merchandising
uuid: 24fc9265-3400-46a7-b6e0-4de5b049a39a
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# Over nabijheidszoekopdracht{#about-proximity-search}

Het Onderzoek van de nabijheid laat u een unieke plaats met om het even welke pagina op uw website associëren, en dan onderzoek en soortresultaten door nabijheid (afstand) van een bepaalde plaats.

Bijvoorbeeld, veronderstel u pagina&#39;s op uw website met de de codemeta-gegevens van het Postadres van de Verenigde Staten zoals het volgende hebt bevolkt:

```
<meta name="zipcode" content="84057">
```

Dan vormt u uw rekening om uw de codemeta-gegevens van het PIT te indexeren. In **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]** > **[!UICONTROL Add New Field]**, op de [!DNL Add Field] pagina, plaatst u de volgende opties:

* Veldnaam: `zip`
* Naam (namen) van de meta-tag: `zipcode`
* Gegevenstype: **[!UICONTROL Location]**
* Sorteren: **[!UICONTROL Ascending]**
* Standaardeenheden: **[!UICONTROL Miles]**

Na het indexeren van uw plaats, voert u het volgende onderzoek uit:

```
...&sp_q_location_1=84057&sp_x_1=zip&sp_q_max_1=100&sp_s=zip_proximity
```

De resultaatreeks bevat om het even welke documenten die binnen 100 mijl van Postcode 84057 worden gevestigd, die in stijgende orde van afstand van deze code van het PIT wordt gesorteerd.

U kunt de codes van het telefoongebied voor de plaatsen van de Verenigde Staten ook gebruiken. Of, u kunt breedte/lengteparen gebruiken om plaatsen in uw plaatsmeta-gegevens en in uw onderzoekscriteria te specificeren. Het plaatstype wordt automatisch bepaald van de vorm van de gegevens die wordt verstrekt.

De waarden van de drie-cijferplaats (&quot;DDD&quot;, waar elke &quot;D&quot;een decimaal cijfer van 0-9 vertegenwoordigt) worden behandeld als code van het de telefoongebied van de Verenigde Staten.

Vijf of vijf-streepje-vier cijferige plaatswaarden (&quot;DDDDD&quot;of &quot;DDD-DDDD&quot;) worden behandeld als postcode van het PIT van de Verenigde Staten.

De waarden van de plaats in de nauwkeurige vorm van &quot;±DD.DDDD±DDD.DDDD&quot;worden behandeld als breedtegraad/lengtegraad paar. De eerste ondertekende numerieke waarde specificeert breedtegraad en de tweede ondertekende numerieke waarde vertegenwoordigt lengtegraad.

**Belangrijk**: Als u een positieve breedtecoëfficiënt, of een positieve lengtewaarde, of allebei specificeert, moet het &quot;+&quot;karakter in URL worden gecodeerd zoals `%2b`. Anders, wordt &quot;+&quot;geïnterpreteerd als ruimte, en de waarde wordt niet erkend als geldige plaats. Bijvoorbeeld, veronderstel u een breedtewaarde van +49.2394 en lengtewaarde van -123.1892 had. Het plaatsgedeelte van URL, met &quot;+&quot;gecodeerd, zou als het volgende kijken:

```
...&sp_q_location_1=%2b49.2394-123.1892...
```

* De positieve breedtegraden vertegenwoordigen graden ten noorden van de evenaar.
* De negatieve latitude-waarden vertegenwoordigen graden ten zuiden van de evenaar.
* De positieve lengtewaarden vertegenwoordigen graden ten oosten van premier Meridian.
* De negatieve lengtewaarden vertegenwoordigen graden ten westen van premier Meridian.

De waarde &quot;+48.8577+002.2950&quot; vertegenwoordigt bijvoorbeeld 48.8577 graden ten noorden van de evenaar, 2.295 graden ten oosten van de eerste Meridiaan, de precieze locatie van de Eiffeltoren in Parijs, Frankrijk. De numerieke tekens en elk cijfer worden vereist, zelfs het leiden en het slepen nul. Bijvoorbeeld, zijn de drie waarden &quot;48.8577+2.2950&quot;, &quot;+48.8577+2.2950&quot;, en &quot;+48.8577+02.295&quot; geen plaatsen. De eerste waarde mist het leidende teken op de breedtegraad. De tweede waarde mist de twee belangrijke nul op de lengtegraad. De derde waarde mist het slepen nul op de lengtegraad. Ben zeker dat u uw indexlogboek zorgvuldig voor om het even welke plaats-verwante problemen onderzoekt.

Wanneer u door nabijheid zoekt is er een speciaal &quot;nabijheidsoutputgebied&quot;gecreeerd voor dat onderzoek. Het gebied is bevolkt met de relatieve afstand tussen de plaats die in de onderzoekscriteria wordt gespecificeerd, en de plaats die met elk onderzoeksresultaat wordt geassocieerd. Dit speciale gebied wordt genoemd voor het plaats-type gebied dat in de onderzoekscriteria met &quot;_proximity&quot;wordt gebruikt dat aan het eind wordt toegevoegd.

In het voorbeeld onderzoek hierboven, worden de resultaten gesorteerd in stijgende orde van &quot;zip_proximity.&quot; Namelijk de afstand tussen de gespecificeerde code van het PIT (84057) en de het gebiedsplaats van elk resultaat &quot;zip&quot;. U kunt dit speciale &quot;nabijheidsoutputgebied&quot;ook gebruiken om de relatieve afstand voor elk onderzoeksresultaat, in of kilometers of mijlen te tonen, gebruikend de het malplaatjemarkering van het `<Search-Display-Field>` Onderzoek.

Zie [Zoeksjabloontags](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4).

U kunt ook zoeken zonder de sp_s optie. In zulk geval, worden de resultaten gesorteerd door score (sp_s=0, die het gebrek is).De score wordt beïnvloed door de relatieve afstand van elk resultaat van de nabijheidsonderzoeksplaats die als parameter sp_q_location[_#] wordt gespecificeerd. Een nieuwe cgi parameter sp_q_max_relevant_distance[#] wordt toegevoegd, om naar keuze de relevantieberekening te controleren die op nabijheidsonderzoeken wordt toegepast.

Het volgende is een nabijheids-relevantie onderzoeksvoorbeeld:

```
...&sp_q_location_1=84057&sp_x_1=zip&sp_q_max_1=100&sp_q_2=shirt&sp_x_2=title&sp_q_max_relevant_distance_2=50
```

De resultaatreeks bevat om het even welke documenten die binnen 100 mijl van code 84057 worden gevestigd van het PIT en bevat het woord &quot;shirt&quot;in titelgebied, die door het noteren wordt gesorteerd die door nabijheid-relevantie het noteren wordt beïnvloed. Een perfecte relevantiescore voor de nabijheidscomponent zou een afstand van 0 vertegenwoordigen. Een minimum relevantiescore voor de nabijheidscomponent zou een afstand net over 50 mijl vertegenwoordigen.

U kunt meer informatie over nabijheidsonderzoek leren door te herzien `sp_location`, `sp_location_#`, `sp_q_min`, `sp_q_min_#`, `sp_q_max`, `sp_q_max_#`, en `sp_s` in het de verwijzingsonderwerp van Parameters van CGI van het Onderzoek te herzien.

Zie CGI-parameters [](../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890)zoeken.

Zie [Een nieuw meta-tagveld](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)toevoegen.
