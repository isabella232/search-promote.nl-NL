---
description: Gebruik Facet Rail om groepen facetten op een webpagina opnieuw te ordenen.
solution: Target
subtopic: Navigation
title: Info over Facet Rail
topic: Ontwerpen, zoeken en verhandelen van sites
uuid: 6da2bd67-8c20-4955-9836-bc8ba88546c5
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '781'
ht-degree: 0%

---


# Info over Facet Rail{#about-facet-rail}

Gebruik Facet Rail om groepen facetten op een webpagina opnieuw te ordenen.

## Facet Rail {#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB} gebruiken

Een facet is een eigenschap of kenmerk. Dit is een manier om de zoekresultaten in algemene zin te categoriseren. Fabrikant, prijs en kleur kunnen bijvoorbeeld worden beschouwd als een groep facetten. Elke facet kan meerdere beperkingen of waarden hebben. Als u bijvoorbeeld kleur als facet had, kunnen de &quot;waarden van het facet&quot; rood, oranje, geel, groen, blauw, indigo en violet zijn.

Zie [Informatie over facetten](../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5).

U gebruikt Facet Rail om deze groepen facetten op een webpagina opnieuw te ordenen. Stel dat u aan de linkerkant van een webpagina een sectie met zoekresultaten hebt. De sectie die van boven naar beneden wordt vermeld, een facet van de Categorie, een facet van het Merk, een facet van de Prijs, en een Populair facet. Met een facetrails kunt u bijvoorbeeld de meest populaire facet boven of onder het categorie-facet weergeven.

De groep facetten die u samen wilt herschikken, behoren tot een facetspoortag. Een facet kan slechts tot één facetspoorstaaf behoren. De facetrails zijn een code van het presentatiesjabloon en bevatten één weergave van een facet. Alle facetten die bij dit spoor horen, delen die ene facetrepresentatie.

Zie [Informatie over sjablonen](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5) en Facet in [Labels voor presentatiesjablonen](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64).

## Een facetrail {#task_561A8FF1CAD1402B9DD33E276BBC6A0E} configureren

U kunt een facetrails toevoegen om de presentatielaag aan te passen. Facet-rails bieden uw klanten een functie met instructies waarmee ze naar hun zoekresultaten kunnen gaan op basis van de volgorde van de facetten op uw webpagina.

<!-- 

t_configuring_facet_rail.xml

-->

Wijzigingen die u aanbrengt in de facetrails, kunnen worden hersteld met de functie Historie.

**Een facetrails configureren**

1. Voordat u een facetrails kunt configureren, moet u controleren of u al een facet hebt toegevoegd en, als onderdeel van die taak, een facetspoornaam opgeven.

   Zie [Een nieuw facet toevoegen](../c-about-design-menu/c-about-facets.md#task_FC07BFFA62CA4B718D6CBF4F2855C89B).
1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Facet Rail.]**
1. Selecteer op de pagina [!DNL Facet Rail] de facetten die u wilt opnemen in de facetrails en stel vervolgens de optie **[!UICONTROL Sort Facets Method]** in de vervolgkeuzelijst in.

   <!-- 
   r_facet_rail_options.xml
   -->

   | Functie/optie | Beschrijving |
   |--- |--- |
   | Naam facetrails | Hiermee wordt de naam van de facetrails aangegeven.  U maakt de naam van de facetrails op het moment dat u de facet toevoegt.  Zie [Een nieuw facet toevoegen](../c-about-design-menu/c-about-facets.md#task_FC07BFFA62CA4B718D6CBF4F2855C89B) |
   | Opgenomen factoren | Een lijst met mogelijke facetten die u kunt selecteren om toe te voegen aan de facetrails.  Als u ervoor kiest om facetten te sorteren met `Custom`, bepaalt de volgorde die u hier facetten selecteert de volgorde waarin ze in het tekstvak `Custom Facet Order` worden weergegeven. |
   | Methode Sorteerfactoren | Kies een van de volgende drie opties in de vervolgkeuzelijst:<ul><li>`Alpha` De facetten worden in alfabetische volgorde gesorteerd ten opzichte van hun namen, inclusief leestekens.</li><li>`Alpha (not case sensitive)` De facetten worden alfabetisch gesorteerd op naam, waarbij alfabetische tekens worden genegeerd, inclusief leestekens. </li><li>`Alpha (alphanumeric only)` De facetten worden in alfabetische volgorde gesorteerd ten opzichte van hun namen, waarbij leestekens worden genegeerd. </li><li>`Alpha (not case sensitive, alphanumeric only)` De facetten worden alfabetisch gesorteerd op naam, waarbij alfabetische tekens worden genegeerd en leestekens worden genegeerd. </li><li>`Count` De facetten worden gesorteerd op basis van aantal. </li><li>`Custom` Hiermee opent u het  `Custom Facet Order` tekstvak waarin u de volgorde van de facetten kunt definiëren door de exacte naam van elk facet in te voeren. Alle onbewerkte facetlabels worden uit de lijst `Custom Facet Order` verwijderd.</li></ul> |
   | Aangepaste volgorde van gezichten | Deze optie is alleen beschikbaar als u `Custom` hebt geselecteerd in de vervolgkeuzelijst `Sort Facets Method`.  Hiermee kunt u lettertypenamen weergeven, één per regel of alle namen op één regel en door komma&#39;s gescheiden. Als er facetlabels zijn gedefinieerd, worden deze weergegeven in de lijst `Facets Included`, tussen haakjes.  Plaats geen facetlabels in het tekstvak `Custom Facet Order`.  Wanneer u facetten in de `Facets Included` lijst selecteert of deselecteert, wordt het `Custom Facet Order` tekstvakje automatisch bijgewerkt. |

1. Klik op **[!UICONTROL Save Changes]**.
1. (Optioneel) Voer op de pagina [!DNL Facet Rail] een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

1. Voer de volgende handelingen uit om de presentatiesjabloon te bewerken:

   * Maak een &quot;facetsjabloon&quot; in de presentatiesjabloon.
   * omring de &quot;facetsjabloon&quot; met de `<guided-facet-rail>`-tags.

      Zie Facets in [Presentatiesjabloonlabels](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64).

      Voorbeeld:

      ```
      <guided-facet-rail>
        <guided-facet>
          <guided-facet-display-name/>
          ...
          </guided-facet>
        </guided-facet-rail>
      ```

      Met deze labels wordt een gedeelte van het presentatiesjabloon uitgesneden tot een herhaalbaar patroon voor elk facet in de facetrails. Elk facet dat tot de facetrail behoort, gebruikt dit uitgesneden gedeelte om zijn output te evalueren. Er kan slechts één `<guided-facet-rail>`-tag op de uiteindelijke presentatiesjabloon verschijnen.

      Voor de volgende tags is het kenmerk `gsname` in `<guided-facet-rail>` niet nodig omdat de waarde tijdens het zoeken dynamisch wordt bepaald en correct wordt vervangen:

      `<guided-facet>`
      `<guided-facet-display-name>`
      `<guided-facet-total-count>`
      `<guided-facet-undo-link>`
      `<guided-facet-undo-path>`
      `<guided-facet-behavior>`

   * Sla de presentatiesjabloon op en druk deze live.

      Zie [Een presentatie of een transportsjabloon bewerken](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3).
