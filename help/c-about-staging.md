---
description: Met Staging kunt u wijzigingen in de instellingen en configuraties testen en voorvertonen zonder dat dit invloed heeft op de actieve index.
seo-description: Met Staging kunt u wijzigingen in de instellingen en configuraties testen en voorvertonen zonder dat dit invloed heeft op de actieve index.
seo-title: Informatie over Staging
solution: Target
title: Informatie over Staging
topic: Staging,Site search and merchandising
uuid: 2e5889a6-2e9c-4ac7-9d6e-d35e7cafda5b
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e
workflow-type: tm+mt
source-wordcount: '978'
ht-degree: 0%

---


# Info over Staging{#about-staging}

Met Staging kunt u wijzigingen in de instellingen en configuraties testen en voorvertonen zonder dat dit invloed heeft op de actieve index.

## Informatie over staging {#concept_08B8F3CA1F4241108F14BA7FC7806CA7}

Met Staging kunt u wijzigingen in de instellingen en configuraties testen en voorvertonen zonder dat dit invloed heeft op de actieve index.

Zie ook [Element ID:context_A5783D07C72042EC886F300FFF62C50](c-about-simulator.md#context_A5783D07C72042EC8886F300FFF62C50).

Elke pagina met de opmaakopties **[!UICONTROL Push All Live]** of **[!UICONTROL View Live Settings]** betekent dat alle instellingen op die pagina kunnen worden gefaseerd. De uitzonderingen zijn de webpagina&#39;s in Index. De pagina&#39;s in dit gebied zijn expliciet voor de gefaseerde index of de live index, zodat u de twee indexen rechtstreeks onafhankelijk kunt beheren.

U kunt vrijwel alles, inclusief uw index, in het werkgebied opnemen. Sommige uitzonderingen omvatten rekening-specifieke montages die zowel uw gefaseerde als levende milieu gelijktijdig en het plannen van het indexeren verrichtingen beïnvloeden. Wanneer u wijzigingen in een instelling opslaat die in een werkgebied kunnen worden opgeslagen, wordt deze instelling standaard automatisch gefaseerd weergegeven.

Als de **[!UICONTROL Push All Live]**- of **[!UICONTROL View Lives Settings]**-opties niet zijn ingeschakeld (gedimd), betekent dit dat de gefaseerde instellingen op die pagina gelijk zijn aan de live instellingen.

Voor een item dat wordt gefaseerd, moet u bedenken dat de live versie van de instellingen alleen-lezen is. het kan alleen worden gemanipuleerd door de gefaseerde instellingen live te duwen.

## Informatie over Geschiedenis op gefaseerde pagina&#39;s {#section_5BE780AFF26A450A9EFF4000DE53531B}

De meeste gefaseerde instellingen hebben een optie [!DNL History] rechtsboven op de pagina. Wanneer u **[!UICONTROL History]** klikt, kunt u om het even welke veranderingen terugkeren die u onlangs aan de bepaalde gefaseerde pagina hebt aangebracht die u open hebt.

U kunt het Wijzigingslogboek ook weergeven voor een andere weergave van Historie. Telkens wanneer een wijziging wordt toegepast, wordt een back-upversie van het onderliggende gegevensbestand gemaakt. In het Wijzigingslogbestand worden deze wijzigingen weergegeven, met daarin het versienummer, het e-mailadres van de gebruiker die de wijzigingen heeft uitgevoerd en de datum waarop de back-up is gemaakt. De vermelding met een vette versiewaarde vertegenwoordigt de huidige versie.

Zie [Wijzigingslogboek weergeven](c-about-reports-menu/c-about-reports-menu.md#task_166F1156719F4B3D834BEA8E249C8057).

## De pagina Stage-Live-instellingen beheren {#section_E72B8CAF516345A5B6B6783CF6E512EE}

U kunt niet alleen de opties **[!UICONTROL Push All Live]** en **[!UICONTROL View Live Settings]** rechtstreeks vanuit een bepaalde pagina aanbieden, maar ook de pagina **[!UICONTROL Manage Stage-Live Settings]** gebruiken om hetzelfde te doen. De **[!UICONTROL Manage Stage-Live Settings]** pagina, beschikbaar in het hoofdproductmenu, is een centrale plaats die u alle montages in uw rekening toont die momenteel gestadig zijn. U kunt alle instellingen live duwen, alleen geselecteerde instellingen live duwen of instellingen verwijderen. Het is echter aan te raden om altijd live te gaan met alle gefaseerde items om problemen met de onderlinge afhankelijkheid te voorkomen.

De instellingen op de pagina worden gegroepeerd in categorieën. U kunt elke categorie uitvouwen om te tonen welke pagina&#39;s instellingen worden gefaseerd. Op dit moment worden afhankelijkheden niet bijgehouden in de werkgebiedmanager. Daarom wordt aangeraden dat u alles in één keer live drukt, behalve de index.

U kunt een gefaseerde index live duwen. Controleer eerst of de gefaseerde index niet stabiel of beschadigd is. Als u een fout maakt en live gaat met de gefaseerde index, kunt u een oude live index terugdraaien. Een actieve gefaseerde index duurt meestal minder dan 30 seconden.

## Een gefaseerde instelling of index {#section_6800E52D20854A779946EAB600801F12} testen

Op pagina&#39;s die een testbesturingselement ondersteunen, kunt u testen op de instellingen voor gefaseerd of actief. Wanneer u de gefaseerde instellingen bekijkt, wordt de gefaseerde instelling gebruikt voor de test. Op dezelfde manier gebruikt de test de actieve instellingen wanneer u de live instelling bekijkt. In de sjabloonsectie worden alle tests uitgevoerd op de gefaseerde versie van de index. Als u een gefaseerde index wilt doorzoeken, stelt u de CGI-parameter `sp_staged` in op 1. Dit geeft op zijn beurt aan dat u de gefaseerde index wilt gebruiken. Als een gefaseerde index niet bestaat, wordt uw levende index gezocht en om het even welke gefaseerde onderzoek-tijd montages toegepast zoals aangewezen.

Zie ook [CGI-parameters voor achtergrondzoekopdrachten](c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8).

## Live-instellingen {#task_401A0EBDB5DB4D4CA933CBA7BECDC10F} weergeven

U kunt de live versie van de instellingen vanuit elke gefaseerde pagina bekijken.

<!-- 

t_viewing_live_settings.xml

 -->

Als de optie **[!UICONTROL View Live Settings]** niet is ingeschakeld (gedimd), betekent dit dat de werkgebiedinstellingen voor die pagina en de live-instellingen al zijn gesynchroniseerd.

**Live-instellingen weergeven**

1. Voor om het even welke pagina die gefaseerde montages heeft, klik **[!UICONTROL View Live Settings]** om de levende versie van de montages te zien.
1. Voer desgewenst een van de volgende handelingen uit:

   * Klik **[!UICONTROL View]** om de huidige opties te zien die voor het gefaseerde plaatsen worden geselecteerd.
   * Klik op **[!UICONTROL View Stage Settings]** om terug te keren naar de instelling voor het werkgebied waar u de instelling kunt bewerken of verwijderen.

## Werkgebiedinstellingen live {#task_44306783B4C0408AAA58B471DAF2D9A4}

U kunt instellingen live duwen vanuit elke gefaseerde paginaweergave of vanaf de centrale **[!UICONTROL Manage Stage-Live Settings]** pagina.

<!-- 

t_pushing_live_settings_live.xml

 -->

Wanneer de optie **[!UICONTROL Push Live]** is ingeschakeld (niet-gedimd) op een pagina, betekent dit dat er een instelling is die wordt gefaseerd. Of een instelling heeft bewerkingen en wanneer u het bestand opslaat, wordt de instelling gefaseerd. Wanneer u op deze optie klikt, worden niet-opgeslagen bewerkingen in het gefaseerde gebied opgeslagen. Als er geen bewerkingen in behandeling zijn, worden de instellingen van de pagina direct live gedrukt.

**Gelaagde instellingen live duwen**

1. Voer een van de volgende handelingen uit:

   * Voor om het even welke pagina die &quot;Staged&quot;als Mening heeft geselecteerd, klik **[!UICONTROL Push Live]**.
   * Klik in het productmenu op **[!UICONTROL Staging]**. Voer op de pagina **[!UICONTROL Manage Stage-Live Settings]** een van de volgende handelingen uit:

   * Gebruik de instellingenstructuur om alleen die instellingen te controleren die u live wilt duwen en klik vervolgens op **[!UICONTROL Push Selected Live]**.
   * Klik op **[!UICONTROL Push All Live]**.

## Instellingen voor werkgebiedlive verwijderen van een centrale locatie {#task_B72BEA9269704B1399600A9CA273369B}

Als u veel instellingen wilt verwijderen, kunt u de pagina **[!UICONTROL Manage Stage-Live Settings]** gebruiken om instellingen van een centrale locatie te verwijderen.

<!-- 

t_deleting_staged_settings_from_a_central_location.xml

 -->

**Waarschuwing**: Wanneer u klikt  **[!UICONTROL Delete Selected]**, worden alle gecontroleerde montages onmiddellijk geschrapt; er is geen bevestigingsdialoogvenster om te controleren of u de geselecteerde instellingen echt wilt verwijderen. Er is ook geen functie Historie gekoppeld aan de pagina. Daarom kunt u uw verwijdering niet ongedaan maken.

**Instellingen voor werkgebiedlive verwijderen van een centrale locatie**

1. Klik in het productmenu op **[!UICONTROL Staging]**.
1. Gebruik op de pagina **[!UICONTROL Manage Stage-Live Settings]** de instellingenstructuur om alleen de instellingen te controleren die u wilt verwijderen.
1. Klik op **[!UICONTROL Delete Selected]**.
