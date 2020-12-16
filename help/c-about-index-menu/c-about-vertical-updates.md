---
description: U kunt Verticale update gebruiken om delen van uw index snel bij te werken zonder dat u grote hoeveelheden gegevens hoeft te verwerken.
seo-description: U kunt Verticale update gebruiken om delen van uw index snel bij te werken zonder dat u grote hoeveelheden gegevens hoeft te verwerken.
seo-title: Info Verticale update
solution: Target
subtopic: Vertical Update
title: Info Verticale update
topic: Index,Site search and merchandising
uuid: ded09e89-5a52-4e8c-a6f7-3e25b4191183
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 0%

---


# Info over Verticale update{#about-vertical-update}

U kunt Verticale update gebruiken om delen van uw index snel bij te werken zonder dat u grote hoeveelheden gegevens hoeft te verwerken.

## Verticale update {#concept_E65A70C9C2E04804BF24FBE1B3CAD899} gebruiken

Een verticale index duurt slechts seconden om uit te voeren en is nuttig op websites van de eCommerce van grote capaciteit die vele uren aan of volledig of incrementeel index kunnen vergen.

Wanneer u een verticale index genereert, wordt statusinformatie weergegeven, zoals begintijd, verstreken tijd en fouten tijdens het indexeringsproces.

U kunt het verticale indexeringsproces op elk ogenblik stoppen of opnieuw beginnen.

Terwijl de nieuwe verticale index uw live website bijwerkt, kunnen klanten uw site blijven doorzoeken met uw huidige index.

>[!NOTE]
>
>Deze functie is standaard niet ingeschakeld in [!DNL Adobe Search&Promote]. Neem contact op met Technische ondersteuning om de functie voor uw gebruik te activeren.

De verticale Updates zijn specifiek bedoeld om op eCommerce-Stijl [!DNL Adobe Search&Promote] rekeningen worden gebruikt die IndexConnector gebruiken om de inhoud voor de onderzoeksindex te leveren. Doorgaans is de gebruikscase een scenario waarin de [!DNL Adobe Search&Promote]-index een doorzoekbare productcatalogus bevat en waarin het nodig is om snel en vaak veranderende waarden bij te werken, zoals inventarisatie, beschikbaarheid en/of prijs. Een verticale update lijkt enigszins op een incrementele index, behalve dat deze alleen gedeelten van elk document bijwerkt, terwijl een incrementele index hele documenten door nieuwe versies vervangt.

De term &quot;Verticale update&quot; verwijst naar de notie dat een [!DNL Adobe Search&Promote] index als kolomlijst kan worden afgebeeld, met elke kolom die aan een [!DNL Adobe Search&Promote] de gebiedsdefinitie van Meta-gegevens beantwoordt, en elke rij die aan een document beantwoordt. Bij het proces Verticale update worden een of meer kolommen vervangen zonder dat de inhoud van de andere kolommen hoeft te worden gewijzigd.

Waar de hoofdbron voor inhoud, een voer IndexConnector, alle vereiste gegevenselementen nodig bevat om de index tot stand te brengen, is het Verticale voer van de Update een ondergroep van de belangrijkste voer, die het zelfde IndexConnector &quot;schema&quot;gebruikt om de gegevenselementen te bepalen, maar die *slechts* die gegevenspunten bevatten die moeten worden bijgewerkt.

Minstens, moet het Verticale voer van de Update het &quot;primaire zeer belangrijke&quot;element (zoals geïdentificeerd met **Primaire Sleutel** controledoos in de configuratie IndexConnector) en minstens één gegevenselement bevatten dat moet worden bijgewerkt.

Bijvoorbeeld, zou een primaire voer IndexConnector als het volgende (maar gewoonlijk met vele meer gegevenspunten) kunnen kijken:

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

U moet alleen de `<price>`- en `<inventory>`-waarden snel kunnen bijwerken, omdat deze waarden op de locatie van de klant snel kunnen veranderen. Een Verticale update zou als het volgende kunnen kijken:

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

Deze informatie wordt typisch opgeslagen in een afzonderlijk dossier op de server van de klant, en de IndexConnector &quot;Vertical File Path&quot;configuratie het plaatsen richt aan dit dossier. Tijdens het proces Verticale update wordt deze nieuwe inhoud gelezen en wordt de bestaande [!DNL Adobe Search&Promote]-index bijgewerkt. In dit geval worden alleen de waarden voor `<price>` en `<inventory>` bijgewerkt. De volgende zoekopdrachten retourneren de nieuw bijgewerkte inhoud.

>[!NOTE]
In dit voorbeeld moeten de velden `<price>` en `<inventory>` Metagegevens zijn gedefinieerd met de optie **Verticaal updateveld** ingeschakeld.

Zie ook [Informatie over afstandsbediening voor indexering](../c-about-index-menu/c-about-remote-control-for-indexing.md#concept_C79B322190E84106A434E5C6D4A4118F) en [Een nieuw veld voor metatags toevoegen](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).

## Een verticale update van een gefaseerde website configureren {#task_46A367B0786C4C90BFFA5D3F95FD86C0}

U kunt vormen welke bronnen van de Schakelaar van de Index u in uw verticale update wilt omvatten door URLs te specificeren.

**Een verticale update van een gefaseerde website configureren**

1. Klik in het productmenu op **[!UICONTROL Index]** > **[!UICONTROL Vertical Update]** > **[!UICONTROL Configuration]**.
1. Geef op de pagina **[!UICONTROL Vertical Update Configuration]** in het veld URL&#39;s bijwerken de URL&#39;s op van de pagina&#39;s die u wilt indexeren.

   De zoekrobot werkt alleen de documenten bij die zijn geïdentificeerd in de opgegeven indexconnectorbronnen.

   Dit veld mag alleen URL&#39;s voor indexaansluiting bevatten, zoals in het volgende voorbeeld:

   `index:product_catalog`.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Het logboek Verticale update van een actieve of gefaseerde website weergeven {#task_E668E1F1240C476DAA1CA783DC728232}

Wanneer een levende Verticale Update of een gefaseerde Verticale Update volledig is, kunt u zijn bijbehorend logboek bekijken om het even welke fouten problemen op te lossen die kunnen zijn voorgekomen.

U kunt geen logbestanden voor verticale updates exporteren en u kunt ze ook niet opslaan. Het logbestand blijft beschikbaar voor weergave totdat de volgende index plaatsvindt.

**Het logboek Verticale update van een live of gefaseerde website weergeven**

1. Voer een van de volgende handelingen uit in het menu Product:

   * Klik op **[!UICONTROL Index]** > **[!UICONTROL Vertical Update]** > **[!UICONTROL Live Log]**.

   * Klik op **[!UICONTROL Index]** > **[!UICONTROL Vertical Update]** > **[!UICONTROL Staged Log]**.

1. Voer een of meerdere van de volgende handelingen uit op de logpagina, boven of onder:

   * Gebruik de navigatieopties **[!UICONTROL First]**, **[!UICONTROL Prev]**, **[!UICONTROL Next]**, **[!UICONTROL Last]**, of **[!UICONTROL Go to line]** om door het logboek te bewegen.

   * Gebruik de weergaveopties **[!UICONTROL Errors only]**, **[!UICONTROL Wrap line]** of **[!UICONTROL Show]** om te verfijnen wat u ziet.

