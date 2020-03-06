---
description: De Spoorlijn van het Gezicht van het gebruik om groepen facetten op een Web-pagina weer in orde te brengen.
seo-description: De Spoorlijn van het Gezicht van het gebruik om groepen facetten op een Web-pagina weer in orde te brengen.
seo-title: Over Facet Rail
solution: Target
subtopic: Navigation
title: Over Facet Rail
topic: Design,Site search and merchandising
uuid: 6da2bd67-8c20-4955-9836-bc8ba88546c5
translation-type: tm+mt
source-git-commit: 6b3aa733b0dfaace956f0ffc25f433fefd21e15f

---


# Over Facet Rail{#about-facet-rail}

De Spoorlijn van het Gezicht van het gebruik om groepen facetten op een Web-pagina weer in orde te brengen.

## Facet Rail gebruiken {#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB}

Een facet is een bezit of een kenmerk, is het een manier om de onderzoeksresultaten over het algemeen te categoriseren. Bijvoorbeeld, zouden de fabrikant, de prijs, en de kleur als een groep facetten kunnen worden beschouwd. Elk facet kan veelvoudige beperkingen of waarden hebben. Bijvoorbeeld, als u kleur als gezicht had, konden de &quot;facetwaarden&quot;rood, oranje, geel, groen, blauw, indigo, en viool zijn.

Zie [Over Facets](../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5).

U gebruikt de Spoorlijn van het Gezicht om deze groepen facetten op een Web-pagina opnieuw in orde te brengen. Bijvoorbeeld, veronderstel dat u een sectie van onderzoeksresultaten op de linkerkant van een Web-pagina had. De sectie maakte een lijst van, van boven tot onder, een facet van de Categorie, een facet van het Merk, een facet van de Prijs, en een Populair facet. Met een facetrails kunt u bijvoorbeeld het meest populaire facet boven of onder het categorie-facet laten verschijnen.

De groep facetten die je samen opnieuw wilt ordenen, behoort tot een facetspoortag. Een facet kan slechts tot één facetspoorstaaf behoren. De facetspoorstaaf is een het malplaatjelag van de Presentatie en omvat één enkele vertegenwoordiging van een facet. Alle facetten die deel uitmaken van deze spoorlijn delen die één facetvertegenwoordiging.

Zie [over Malplaatjes](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5) en Facet in de malplaatjemarkeringen [van de](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)Presentatie.

## Een facetrail configureren {#task_561A8FF1CAD1402B9DD33E276BBC6A0E}

U kunt een facetspoorstaaf toevoegen om uw presentatielaag aan te passen. De rails van het gezicht voorzien uw klanten van een Geleid Onderzoek dat hen laat neer in hun onderzoeksresultaten bogen die op de orde van de facetten op uw Web-pagina worden gebaseerd.

<!-- 

t_configuring_facet_rail.xml

-->

Om het even welke veranderingen u aan facetsporen aanbrengt kunnen worden omgekeerd gebruikend de eigenschap van de Geschiedenis.

**Om een facetspoorstaaf te vormen**

1. Voordat u een facetrail kunt configureren, moet u ervoor zorgen dat u al een facet hebt toegevoegd en als onderdeel van die taak een facetspoornaam hebt opgegeven.

   Zie Een nieuw facet [toevoegen](../c-about-design-menu/c-about-facets.md#task_FC07BFFA62CA4B718D6CBF4F2855C89B).
1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Facet Rail.]**
1. Voor de [!DNL Facet Rail] pagina, selecteer de facetten die u in de facetspoorstaaf wilt omvatten, en plaats dan de **[!UICONTROL Sort Facets Method]** optie van de drop-down lijst.

   <!-- 
   r_facet_rail_options.xml
   -->

   | Functie/optie | Beschrijving |
   |--- |--- |
   | Naam facet-rail | Identificeert de naam van de facetspoorstaaf.  U creeert de naam van de facetspoorstaaf toen u het facet toevoegde.  Zie Een nieuw facet [toevoegen](../c-about-design-menu/c-about-facets.md#task_FC07BFFA62CA4B718D6CBF4F2855C89B) |
   | Inbegrepen facetten | Een lijst van mogelijke facetten die u kunt selecteren om aan de facetspoorstaaf toe te voegen.  Als u verkiest om facetten te sorteren gebruikend `Custom`, bepaalt de orde die u hier facetten selecteert de orde dat zij in het `Custom Facet Order` tekstvakje verschijnen. |
   | Methode Sorteerfacetten | Kies uit een van de volgende drie opties in de vervolgkeuzelijst:<ul><li>`Alpha` De facetten worden gesorteerd in alfabetische orde met betrekking tot hun namen, met inbegrip van leestekens.</li><li>`Alpha (not case sensitive)` De facetten worden gesorteerd in alfabetische orde met betrekking tot hun namen, negerend het geval van alfabetische karakters, en met inbegrip van punctuatie karakters. </li><li>`Alpha (alphanumeric only)` De facetten worden gesorteerd in alfabetische orde met betrekking tot hun namen, negerend leestekens. </li><li>`Alpha (not case sensitive, alphanumeric only)` De facetten worden gesorteerd in alfabetische orde met betrekking tot hun namen, negerend het geval van alfabetische karakters, en negerend punctuatiekarakters. </li><li>`Count` De facetten worden gesorteerd basis op telling. </li><li>`Custom` Opent het `Custom Facet Order` tekstvakje dat u de orde van de facetten door de nauwkeurige naam van elk facet in te gaan laat bepalen. Om het even welke facetetiketten die uit worden verlaten worden verwijderd uit de `Custom Facet Order` lijst.</li></ul> |
   | Aangepaste factsorder | Deze optie is slechts beschikbaar als u `Custom` uit de `Sort Facets Method` drop-down lijst selecteerde.  Laat u van facetnamen, of één per lijn, of allen op één lijn en komma-gescheiden een lijst maken. Als de facetetiketten worden bepaald worden zij getoond in de `Facets Included` lijst, die tussen haakjes wordt ingesloten.  Omvat facetetiketten niet in het `Custom Facet Order` tekstvakje.  Wanneer u selecteert of facetten in de `Facets Included` lijst schrapt, wordt het `Custom Facet Order` tekstvakje automatisch bijgewerkt. |

1. Klik op **[!UICONTROL Save Changes]**.
1. (Facultatief) op de [!DNL Facet Rail] pagina, doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

1. Geef het malplaatje van de Presentatie door het volgende uit te doen:.

   * Creeer een &quot;facetmalplaatje&quot;op het presentatiemalplaatje.
   * Omring de &quot;facetmalplaatje&quot;met de `<guided-facet-rail>` markeringen.

      Zie Facets in de sjabloontags voor [presentaties](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64).

      Voorbeeld:

      ```
      <guided-facet-rail>
        <guided-facet>
          <guided-facet-display-name/>
          ...
          </guided-facet>
        </guided-facet-rail>
      ```

      Deze markeringen maken een sectie van het presentatiemalplaatje uit om een herhaalbaar patroon voor elk facet in de facetspoorstaaf te worden. Elk facet dat tot de facetspoorstaaf behoort, gebruikt dit uitgesneden deel om zijn output te evalueren. Slechts één `<guided-facet-rail>` markering kan op het definitieve presentatiemalplaatje verschijnen.

      De volgende markeringen vergen niet de `gsname` attributen binnen `<guided-facet-rail>` omdat de waarde dynamisch in onderzoekstijd wordt bepaald en behoorlijk gesubstitueerd is:

      `<guided-facet>`
      `<guided-facet-display-name>`
      `<guided-facet-total-count>`
      `<guided-facet-undo-link>`
      `<guided-facet-undo-path>`
      `<guided-facet-behavior>`

   * Sparen het presentatiemalplaatje en duw het levend.

      Zie Een presentatie [bewerken of een transportsjabloon](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3).
