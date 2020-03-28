---
description: 'null'
seo-description: 'null'
seo-title: '&Zoeken;amp;Opmerkingen bij de release 8.16.0 promoten (18-9-2014)'
solution: Target
title: '&Zoeken;amp;Opmerkingen bij de release 8.16.0 promoten (18-9-2014)'
topic: Release Notes,Site search and merchandising
uuid: 0a59858b-213b-40d6-aea1-d085c4d6d2fa
translation-type: tm+mt
source-git-commit: ffdec2cfcb30e733c664a7d1ca23868b7a9a9aa5

---


# Opmerkingen bij de release 8.16.0 opzoeken en promoten (18-9-2014){#search-promote-release-notes}

## Opmerkingen bij de release 8.16.0 opzoeken en promoten (18-9-2014) {#topic_5BECD3F66C684987828F6AE65E62DA29}

## Nieuwe functies {#section_2A10EF6B40FC4F2CB2381FFA9FFA64BD}

* In cache plaatsen van zoekresultaten in Zoeken met instructies 3 (GS3) - Neem contact op met de technische accountmanager van Adobe om deze aangepaste functie zo in te stellen dat u deze in uw account kunt gebruiken.
* Verticale updates voor velden die vaak worden gewijzigd - U kunt nu snel alle waarden voor een set metagegevensvelden bijwerken zonder dat u de inhoud volledig opnieuw hoeft te indexeren.

   Zie de optie Verticaal updateveld in de tabel in [Een nieuw metatag-tagveld](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5) toevoegen en [Info over Verticaal bijwerken](../c-about-index-menu/c-about-vertical-updates.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899).

   Deze functie kan alleen worden gebruikt voor [!DNL Adobe Search&Promote] accounts die Indexconnector gebruiken. Neem contact op met de technische accountmanager van Adobe als u deze aangepaste functie zo wilt instellen dat u deze kunt gebruiken in uw account.

## Oplossingen en verbeteringen {#section_22D1AFC99F394D569898828A0D3C419D}

* Correcteerde het ontleden van de Schakelaar van de Index van het voer van XML dat `?>` koord bevatte.
* Vaste SFTP van de Schakelaar van de Index voer toen het minimum documentaantal werd afgedwongen.
* De uitvoer van het rapport naar Microsoft Excel steunt nu UTF8.
* Zoeken met instructies: facetten werden langzaam gecompileerd.
* Kenmerklader: geaggregeerde gegevens hadden dubbele sleutels.
* Probleem verholpen met verkeerde uitvoeringsvolgorde van de bedrijfsregel wanneer een individuele regel live wordt gedrukt.
* De onjuiste facet Undo verbindingen werd geproduceerd door Geleide Onderzoek.
* Nieuwe bewerking voor besturing op afstand is toegevoegd ( `sp_lines=N`) waarmee u de voortgang en status van een index die momenteel wordt uitgevoerd, kunt controleren.

   Zie [Informatie over afstandsbediening voor indexering](../c-about-index-menu/c-about-remote-control-for-indexing.md#concept_C79B322190E84106A434E5C6D4A4118F).

* De behoefte om auteinformatie te verzenden wanneer het halen schrapt informatie tijdens stijgende de Schakelaar van de Index.
* Het [!DNL Change Log] rapport identificeert nu de gebruiker die een handindexverrichting in werking stelt.

   Zie Het logbestand [wijzigen](../c-about-reports-menu/c-about-reports-menu.md#task_166F1156719F4B3D834BEA8E249C8057)weergeven.

* Wanneer u een [!DNL Terms Report]object exporteert, kunt u niet langer maximaal 500 items in het rapport opnemen.

   Zie [Het rapport met voorwaarden of het rapport Null-zoektermen weergeven...](../c-about-reports-menu/c-about-reports-menu.md#task_53B7ED1582DD4B0E8376546A7AFC789A).

* De **[!UICONTROL Strip HTML]** instelling Indexaansluiting werd altijd weergegeven als ingeschakeld.
* Er zijn inconsistente zoekresultaten aangetroffen met de **[!UICONTROL Common Phrases]** functie.
* De vertoning van attributennamen werd afgebroken in de lijstsamenvattingen van de Regel.
* Het duwen van een individuele bedrijfsregel levend duwde alle bedrijfsregels.

