---
description: Het opvoeren laat u testen en voorproefveranderingen in uw montages en configuraties zonder uw levende index te beïnvloeden.
seo-description: Het opvoeren laat u testen en voorproefveranderingen in uw montages en configuraties zonder uw levende index te beïnvloeden.
seo-title: Over faseren
solution: Target
title: Over faseren
topic: Staging,Site search and merchandising
uuid: 2e5889a6-2e9c-4ac7-9d6e-d35e7cafda5b
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# Over faseren{#about-staging}

Het opvoeren laat u testen en voorproefveranderingen in uw montages en configuraties zonder uw levende index te beïnvloeden.

## Over faseren {#concept_08B8F3CA1F4241108F14BA7FC7806CA7}

Het opvoeren laat u testen en voorproefveranderingen in uw montages en configuraties zonder uw levende index te beïnvloeden.

Zie ook [Element ID: context_A5783D07C72042EC886F300FFF62C50](c-about-simulator.md#context_A5783D07C72042EC8886F300FFF62C50).

Om het even welke pagina die de het opvoeren opties heeft **[!UICONTROL Push All Live]** of **[!UICONTROL View Live Settings]** betekent dat alle montages op die pagina kunnen worden gefaseerd. De uitzonderingen zijn de Web-pagina&#39;s in Index. De pagina&#39;s op dit gebied zijn of uitdrukkelijk voor de gefaseerde index of de levende index om u direct te laten de twee indexen onafhankelijk controleren.

Je kunt bijna alles opvoeren, inclusief je index. Sommige uitzonderingen omvatten rekening-specifieke montages die zowel uw gefaseerde als levende milieu gelijktijdig en het plannen van het indexeren verrichtingen beïnvloeden. Door gebrek wanneer u sparen om het even welke veranderingen in het plaatsen die kan worden gefaseerd, wordt het automatisch gefaseerd.

Wanneer **[!UICONTROL Push All Live]** of de **[!UICONTROL View Lives Settings]** opties niet (verduisterd) worden toegelaten betekent het dat de gefaseerde montages op die pagina het zelfde als de levende montages zijn.

Voor een punt dat wordt gefaseerd, merk op dat de levende versie van de montages read-only is; het kan slechts worden gemanipuleerd door de gefaseerde montages te duwen levend.

## Over Geschiedenis op pagina&#39;s die nog niet zijn bijgewerkt {#section_5BE780AFF26A450A9EFF4000DE53531B}

De meeste gefaseerde montages hebben een [!DNL History] optie op het hoger-juiste gebied van de pagina. Wanneer u klikt, laat het u om het even welke veranderingen terugkeren die u onlangs aan de bepaalde getrapte pagina hebt aangebracht die u open hebt. **[!UICONTROL History]**

U kunt het Logboek van de Verandering voor een afwisselende mening van Geschiedenis ook bekijken. Telkens als een verandering wordt toegepast, wordt een reserveversie van het onderliggende gegevensdossier gecreeerd. Het logboek van de Verandering toont elke dergelijke herziening, die het versieaantal, het e-mailadres van de gebruiker toont die de veranderingen uitvoerde, en de datum toont waarop de steun werd gemaakt. De ingang met een gewaagde versiewaarde vertegenwoordigt de huidige versie.

Zie het [bekijken van het Logboek](c-about-reports-menu/c-about-reports-menu.md#task_166F1156719F4B3D834BEA8E249C8057)van de Verandering.

## De pagina Stage-Live-instellingen beheren {#section_E72B8CAF516345A5B6B6783CF6E512EE}

Naast het aanbieden van de **[!UICONTROL Push All Live]** en de **[!UICONTROL View Live Settings]** opties direct van binnen een bepaalde pagina, kunt u de **[!UICONTROL Manage Stage-Live Settings]** pagina ook gebruiken om het zelfde ding te doen. De **[!UICONTROL Manage Stage-Live Settings]** pagina, beschikbaar bij het belangrijkste productmenu, is een centrale plaats die u alle montages in uw rekening toont die momenteel gestaveerd zijn. U kunt alle montages drukken levend, duw slechts geselecteerde montages levend, of u kunt montages schrappen. Als beste praktijk, echter, duw altijd alle gefaseerde punten levend om het even welke onderlinge afhankelijkheidskwesties te vermijden.

De montages op de pagina worden gegroepeerd in categorieën. U kunt elke categorie uitbreiden om te tonen welke montages van de pagina worden gefaseerd. Momenteel, worden de gebiedsdelen niet gevolgd binnen de stadiummanager. Daarom wordt geadviseerd dat u alles behalve de index in één keer levend duwt.

U kunt een gefaseerde levende index duwen. Zeker ben dat u eerst controleert dat uw gefaseerde index niet stale of bedorven is. Als u een fout maakt en de gefaseerde levende index duwt kunt u een oude levende index terugrollen. Het duwen van een gefaseerde levende index duurt gewoonlijk minder dan 30 seconden.

## Een gefaseerde instelling of index testen {#section_6800E52D20854A779946EAB600801F12}

Op pagina&#39;s die een testcontrole steunen, kunt u tegen de gefaseerde of levende montages testen. Wanneer u de gefaseerde montages bekijkt, wordt het gefaseerde plaatsen gebruikt voor de test. Op dezelfde manier wanneer u het levende plaatsen bekijkt gebruikt de test de levende montages. In de malplaatjesectie, worden alle tests gedaan tegen de gefaseerde versie van de index. Om een gefaseerde index te zoeken, plaats de parameter van `sp_staged` CGI gelijk aan 1. beurtelings, wijst dit erop dat u de gefaseerde index wilt gebruiken. Als een gefaseerde index niet bestaat, wordt uw levende index gezocht en om het even welke gefaseerde onderzoek-tijd montages worden toegepast zoals aangewezen.

Zie ook de parameters [van het onderzoekCGI van het](c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)Achterste onderzoekCGI.

## Live-instellingen bekijken {#task_401A0EBDB5DB4D4CA933CBA7BECDC10F}

U kunt de levende versie van de montages van om het even welke gefaseerde pagina herzien.

<!-- 

t_viewing_live_settings.xml

 -->

Als de **[!UICONTROL View Live Settings]** optie niet toelaat (verduisterd), betekent het dat de stadiummontages voor die pagina en de levende montages reeds in synch zijn.

**Om levende montages te bekijken**

1. Voor om het even welke pagina die montages heeft gefaseerd, klik **[!UICONTROL View Live Settings]** om de levende versie van de montages te zien.
1. Naar keuze, doe één van het volgende:

   * Klik **[!UICONTROL View]** om de huidige opties te zien die voor het gefaseerde plaatsen worden geselecteerd.
   * Klik **[!UICONTROL View Stage Settings]** om aan het gefaseerde plaatsen terug te keren waar u het plaatsen kunt uitgeven of schrappen.

## De montages van het spoelstadium leven {#task_44306783B4C0408AAA58B471DAF2D9A4}

U kunt montages van om het even welke gefaseerde paginamening of van de centrale **[!UICONTROL Manage Stage-Live Settings]** pagina drukken leven.

<!-- 

t_pushing_live_settings_live.xml

 -->

Wanneer de **[!UICONTROL Push Live]** optie (undimmed) op een pagina wordt toegelaten betekent het dat er het plaatsen is die gestaged is. Of, betekent het dat het plaatsen heeft uitgeeft en wanneer u sparen, wordt het plaatsen gefaseerd. Wanneer u op deze optie klikt, worden alle niet-opgeslagen bewerkingen opgeslagen in het gefaseerde gebied. Als er geen hangende uitgeeft zijn, worden de montages van de pagina onmiddellijk levend geduwd.

**Om gefaseerde montages levend te duwen**

1. Doe één van het volgende:

   * Klik op een pagina waarop &quot;Staand&quot; is geselecteerd als de weergave, op **[!UICONTROL Push Live]**.
   * Klik in het productmenu op **[!UICONTROL Staging]**. Op de **[!UICONTROL Manage Stage-Live Settings]** pagina, doe één van het volgende:

   * Gebruik de montagesboom om slechts die montages te controleren die u levend wilt duwen, en dan klikken **[!UICONTROL Push Selected Live]**.
   * Klik op **[!UICONTROL Push All Live]**.

## Het schrappen van stadium-levende montages van een centrale plaats {#task_B72BEA9269704B1399600A9CA273369B}

Als u vele te schrappen montages hebt, kunt u de **[!UICONTROL Manage Stage-Live Settings]** pagina gebruiken om montages van één, centrale plaats te schrappen.

<!-- 

t_deleting_staged_settings_from_a_central_location.xml

 -->

**Waarschuwing**: Wanneer u klikt **[!UICONTROL Delete Selected]**, worden alle gecontroleerde montages onmiddellijk geschrapt; er is geen doos van de bevestigingsdialoog om te verifiëren dat u werkelijk de geselecteerde montages wilt schrappen. Ook, is er geen eigenschap van de Geschiedenis verbonden aan de pagina. Daarom kunt u uw schrapping niet ongedaan maken.

**Om stadium-levende montages van een centrale plaats te schrappen**

1. Klik in het productmenu op **[!UICONTROL Staging]**.
1. Voor de **[!UICONTROL Manage Stage-Live Settings]** pagina, gebruik de montagesboom om slechts die montages te controleren die u wilt schrappen.
1. Klik op **[!UICONTROL Delete Selected]**.
