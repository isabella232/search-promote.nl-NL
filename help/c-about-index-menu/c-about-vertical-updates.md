---
description: U kunt Verticale Update gebruiken om delen van uw index snel bij te werken zonder het moeten grote hoeveelheden gegevens verwerken.
seo-description: U kunt Verticale Update gebruiken om delen van uw index snel bij te werken zonder het moeten grote hoeveelheden gegevens verwerken.
seo-title: Informatie over verticale update
solution: Target
subtopic: Vertical Update
title: Informatie over verticale update
topic: Index,Site search and merchandising
uuid: ded09e89-5a52-4e8c-a6f7-3e25b4191183
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a

---


# Informatie over verticale update{#about-vertical-update}

U kunt Verticale Update gebruiken om delen van uw index snel bij te werken zonder het moeten grote hoeveelheden gegevens verwerken.

## Verticale update gebruiken {#concept_E65A70C9C2E04804BF24FBE1B3CAD899}

Een verticale index neemt slechts seconden om uit te voeren en is nuttig op de websites van de Handel van de grote capaciteit die vele uren aan of volledig of incrementele index kunnen vergen.

Wanneer u een verticale index produceert, wordt de statusinformatie getoond, zoals begintijd, verstreken tijd, en fouten tijdens het het indexeren proces.

U kunt het verticale indexeringsproces op elk ogenblik tegenhouden of opnieuw beginnen.

Terwijl de nieuwe verticale index uw levende website bijwerkt, kunnen de klanten uw plaats blijven zoeken gebruikend uw huidige index.

>[!NOTE]
>
>Deze eigenschap wordt niet toegelaten binnen [!DNL Adobe Search&Promote], door gebrek. Neem contact op met Technische ondersteuning om de functie voor uw gebruik te activeren.

De verticale Updates worden specifiek bedoeld om op eCommerce-Stijl [!DNL Adobe Search&Promote] rekeningen te worden gebruikt die IndexConnector gebruiken om de inhoud voor de onderzoeksindex te leveren. De typische gebruikscase is een waarin de [!DNL Adobe Search&Promote] index een doorzoekbare productcatalogus weergeeft en de noodzaak bestaat om veelvuldig veranderende waarden, zoals voorraad-ter-hand, beschikbaarheid en/of prijs, snel bij te werken. Een verticale Update is enigszins gelijkaardig aan een Stijgende Index, behalve dat werkt het slechts gedeelten van elk document bij, terwijl een Incrementele Index volledige documenten met nieuwe versies vervangt.

De term &quot;Verticale Update&quot;verwijst naar het begrip dat een [!DNL Adobe Search&Promote] index als kolomlijst, met elke kolom kan worden voorgesteld die aan een het gebiedsdefinitie van [!DNL Adobe Search&Promote] Meta-gegevens beantwoordt, en elke rij die aan een document beantwoordt. Het Verticale proces van de Update vervangt één of meerdere kolommen zonder de behoefte om om het even welke inhoud van andere kolommen te veranderen.

Waar de belangrijkste bron voor inhoud, een input IndexConnector, alle vereiste gegevenselementen bevat nodig om de index tot stand te brengen, is het Verticale voer van de Update een ondergroep van het belangrijkste voer, die het zelfde &quot;schema IndexConnector&quot;gebruikt om de gegevenselementen te bepalen, maar die *slechts* die gegevenspunten bevatten die moeten worden bijgewerkt.

Minstens, moet het Verticale voer van de Update het &quot;primaire belangrijkste&quot;element (zoals die met de **Primaire Belangrijkste** controledoos in de configuratie IndexConnector wordt geïdentificeerd) en minstens één gegevenselement bevatten dat moet worden bijgewerkt.

Bijvoorbeeld, zou een primair voer IndexConnector als het volgende (maar gewoonlijk met veel meer gegevenspunten) kunnen kijken:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<products>
<product>
  <id><![CDATA[123]]></id>
  <title><![CDATA[Title for product 123]]></title>
  <description><![CDATA[Description for product 123.]]></description>
  <price>3.99</price>
  <link><![CDATA[https://www.somewhere.com/products/123]]></link>
  <image><![CDATA[https://www.somewher.com/images/products/123.jpg]]></image>
  <label><![CDATA[PROD123]]></label>
  <inventory>100</inventory>
  <brand><![CDATA[brand123]]></brand>
  ...
</product>
<product>
...
</product>
</products>
```

Een vereiste moet alleen de waarden `<price>` `<inventory>` en waarden snel kunnen bijwerken, omdat deze waarden snel kunnen veranderen op de locatie van de klant. Een Verticaal voer van de Update zou dan als het volgende kunnen kijken:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<products>
<product>
  <id><![CDATA[123]]></id>
  <price>3.50</price>
  <inventory>90</inventory>
</product>
<product>
...
</product>
</products>
```

Deze informatie wordt typisch opgeslagen in een afzonderlijk dossier op de server van de klant, en de configuratie die van de &quot;Verticale Weg van het Dossier IndexConnector&quot;punten plaatst aan dit dossier. Het Verticale proces van de Update leest deze nieuwe inhoud en werkt de bestaande [!DNL Adobe Search&Promote] index bij, slechts bijwerkend de waarden voor `<price>` en, in dit geval `<inventory>`. De verdere onderzoeken keren de onlangs bijgewerkte inhoud terug.

>[!NOTE]
In dit voorbeeld, zullen de gebieden `<price>` en van `<inventory>` Meta-gegevens met de Verticale gecontroleerde optie van het Gebied **** van de Update moeten worden bepaald.

Zie ook [Ongeveer Verre Controle voor het Indexeren](../c-about-index-menu/c-about-remote-control-for-indexing.md#concept_C79B322190E84106A434E5C6D4A4118F) en het [Toevoegen van een nieuw meta markeringsgebied](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).

## Een verticale update van een gefaseerde website configureren {#task_46A367B0786C4C90BFFA5D3F95FD86C0}

U kunt vormen welke bronnen van de Schakelaar van de Index u in uw verticale update wilt omvatten door URLs te specificeren.

**Om een Verticale Update van een gefaseerde website te vormen**

1. Klik in het productmenu op **[!UICONTROL Index]** > **[!UICONTROL Vertical Update]** > **[!UICONTROL Configuration]**.
1. Voor de **[!UICONTROL Vertical Update Configuration]** pagina, op het gebied van de Update URLs, specificeer URLs van de pagina&#39;s die u wilt indexeren.

   De onderzoeksrobot werkt slechts de documenten bij die in de gespecificeerde bronnen van de Schakelaar van de Index worden geïdentificeerd.

   Dit gebied moet de Schakelaar URLs van de Index slechts zoals in het volgende voorbeeld bevatten:

   `index:product_catalog`.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Het bekijken van het Verticale logboek van de Update van een levende of gefaseerde website {#task_E668E1F1240C476DAA1CA783DC728232}

Wanneer een levende Verticale Update of een gefaseerde Verticale Update volledig is, kunt u zijn bijbehorend logboek bekijken om het even welke fouten problemen op te lossen die kunnen zijn voorgekomen.

U kunt geen verticale het logboekdossiers van de Update uitvoeren, noch kunt u sparen hen. Het logboekdossier blijft beschikbaar voor het bekijken tot de volgende index voorkomt.

**Om het Verticale logboek van de Update van een levende of gefaseerde website te bekijken**

1. Voor het productmenu, doe één van het volgende:

   * Klik op **[!UICONTROL Index]** > **[!UICONTROL Vertical Update]** > **[!UICONTROL Live Log]**.

   * Klik op **[!UICONTROL Index]** > **[!UICONTROL Vertical Update]** > **[!UICONTROL Staged Log]**.

1. Voor de logboekpagina, bij de bovenkant of de bodem, doe om het even welke volgend:

   * Gebruik de navigatieopties **[!UICONTROL First]**, **[!UICONTROL Prev]**, **[!UICONTROL Next]**, **[!UICONTROL Last]**, of **[!UICONTROL Go to line]** om zich door het logboek te bewegen.

   * Gebruik de vertoningsopties **[!UICONTROL Errors only]**, **[!UICONTROL Wrap line]**, of **[!UICONTROL Show]** om te raffineren wat u ziet.

