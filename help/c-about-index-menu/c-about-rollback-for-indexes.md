---
description: Met Terugdraaien kunt u een back-up maken van door u gegenereerde indexen van websites en deze archiveren. U kunt ook de back-up van een index op elk gewenst moment herstellen.
solution: Target
subtopic: Rollback
title: Over Terugdraaien voor indexen
topic: Index, zoeken en verhandelen van sites
uuid: abed878a-71b3-4122-9822-7410f4427a9a
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%

---


# Info Terugdraaien voor indexen{#about-rollback-for-indexes}

Met [!DNL Rollback] kunt u een back-up maken van door u gegenereerde indexen van websites en deze archiveren. U kunt ook de back-up van een index op elk gewenst moment herstellen.

## Terugdraaien gebruiken voor indexen {#concept_0BC4BC975DB045A986C3607CF32705D8}

Het archief bevat vier indexen: de huidige site-index en drie vorige site-indexen, die de zoekrobot automatisch archiveert op basis van de instellingen voor terugdraaiconfiguratie. Elke keer dat uw website wordt geïndexeerd, wordt het archief bijgewerkt. De nieuwere indexen vervangen bestaande gearchiveerde indexen zodat het archief altijd actueel blijft.

Elke gearchiveerde index wordt met de volgende informatie in het archief weergegeven:

* Datum en tijd waarop de index is voltooid.
* Indexleeftijd.
* Aantal geïndexeerde documenten.
* Type indexeringsbewerking (vol, incrementeel, enzovoort).
* Indexstatus zoals of de index momenteel actief is en of deze na de volgende index wordt behouden of verwijderd.

Elke keer dat uw website wordt geïndexeerd, wordt de nieuwe index aan het archief toegevoegd en wordt een bestaande gearchiveerde index verwijderd. De oudste index hoeft echter niet de index te zijn die wordt verwijderd. Wanneer een nieuwe index aan het archief wordt toegevoegd, wordt een leeftijdsvergelijking gemaakt van elke gearchiveerde index aan de pagina&#39;s die in de terugdraaiingsconfiguratiemontages worden gespecificeerd. De index die het verst van het gewenste schema is verwijderd. Stel dat de configuratie-instelling bijvoorbeeld 24,48,72 is en de leeftijd van de opgeslagen indexen 5, 23, 47 en 71 is. De meest recente index (vijf uur oud) wordt verwijderd wanneer een nieuwe index aan het archief wordt toegevoegd omdat de leeftijd het verst van de instellingen afwijkt. Voor het gemak wordt in het archief aangegeven welke index wordt verwijderd wanneer de site opnieuw wordt geïndexeerd.

U kunt naar andere gebieden binnen de gebruikersinterface navigeren terwijl een index wordt geactiveerd. Een statusindicator houdt de voortgang van de activering bij en is beschikbaar wanneer u de pagina [!DNL Rollback] weergeeft. Als een gearchiveerde index wordt hersteld, worden de gebruikers op de hoogte gesteld bij de bovenkant van de Volledige Index, de Incrementele Index, de Scripted Index, en Regenerate pagina&#39;s. Er kan geen indexeringsbewerking plaatsvinden terwijl een index wordt hersteld. Als een terugdraaibewerking een conflict veroorzaakt met een geplande site-index, wordt de geplande indexering uitgesteld totdat het terugdraaien is voltooid. Als een index al bezig is, dan wordt het geannuleerd, op voorwaarde dat de gebruiker bevestigt dat het terugschroeven van prijzen prioriteit ontvangt.

Om de integriteit van het archief te handhaven, werkt de onderzoeksrobot niet het terugschroeven van prijzen bij als de fouten tijdens kruipend worden gevonden. Er is ook geen update als een gebruiker een indexeringsbewerking annuleert. Als een indexeringsbewerking de maximale tijd, bytes, pagina&#39;s of documenten overschrijdt, voltooit de verkenner de index en voegt deze toe aan het archief. Als tijdens een indexeringsbewerking niet aan het minimale aantal pagina&#39;s wordt voldaan, annuleert de schuifregelaar de index en blijft de vorige index actief.

## Het terugschroeven van prijzenarchiveringsprogramma van indexen {#task_CD403B9AE2244B13A6B3861B5F9B055C} vormen

Met [!DNL Configure] kunt u bepalen welke indexbestanden u wilt opslaan in het terugdraaiarchief. In het archief kunnen de huidige index en drie back-upindexen worden opgeslagen.

Het veld **[!UICONTROL Schedule]** bevat drie door komma&#39;s gescheiden waarden die uren vertegenwoordigen van het heden. De planningswaarden 24,48,72 geven bijvoorbeeld 24 uur op vanaf het heden of gisteren, 48 uur vanaf het heden of twee dagen geleden en 72 uur vanaf het heden of drie dagen geleden.

Met Doorgaan zoeken worden de site-indexen gearchiveerd die het dichtst bij een dag, twee dagen en drie dagen oud liggen. De werkelijke tijden en data van de gearchiveerde indexen kunnen variëren afhankelijk van het indexeringsschema van uw website.

**Om het terugschroeven van prijzenarchiveringsprogramma van indexen te vormen**

1. Klik in het productmenu op **[!UICONTROL Index]** > **[!UICONTROL Rollback]** > **[!UICONTROL Configure]**.
1. Voer op de pagina [!DNL Rollback Configuration] in het veld **[!UICONTROL Schedule]** een door een opdracht gescheiden lijst in met drie indexpagina&#39;s, in uren. De indexen die het dichtst bij deze pagina&#39;s liggen, worden opgeslagen.
1. Klik op **[!UICONTROL Save Changes]**.

## Een gearchiveerde index {#task_5DCE3D660F6F4197993E92AA59227332} activeren

Met Terugdraaien kunt u een gearchiveerde index activeren.

Wanneer u **[!UICONTROL Activate]** klikt om een index terug te draaien, wordt de momenteel actieve index verplaatst naar het archief.

Nadat de gearchiveerde index is geactiveerd, wordt u teruggestuurd naar de pagina [!DNL Activate Index]. De informatie over de indexterugdraaiing wordt getoond. Bovendien identificeert de [!DNL Activate] kolom in [!DNL Available Indexes] lijst de gewalste achterindex met de status &quot;Actieve Index&quot;.

1. Klik in het productmenu op **[!UICONTROL Index]** > **[!UICONTROL Rollback]** > **[!UICONTROL Rollback]**.
1. Op [!DNL Activate Index] pagina, in [!DNL Available Indexes] lijst, klik **[!UICONTROL Activate]** voor het bijbehorende gearchiveerde indextype dat u actief wilt maken.

   Met de kolommen Datum, Pagina&#39;s, en Bewerking kunt u bepalen welke index moet worden geactiveerd.
1. Controleer op de pagina [!DNL Verify Rollback] de indexgegevens om te controleren of u de juiste index hebt geselecteerd en klik vervolgens op **[!UICONTROL Activate Now]**.

## Logbestand van alle indexterugdraaiversies weergeven {#task_D2D9AA7203F0465FB5AE0D49212AC41C}

Bekijk de datum en tijd van alle terugdraaibewerkingen.

**Het logboek van alle indexterugdraaiversies weergeven**

1. Voer een van de volgende handelingen uit in het menu Product:

   * Klik op **[!UICONTROL Index]** > **[!UICONTROL Re-Rank Index]** > **[!UICONTROL Live Log]**.

   * Klik op **[!UICONTROL Index]** > **[!UICONTROL Re-Rank Index]** > **[!UICONTROL Staged Log]**.

1. Voer een of meerdere van de volgende handelingen uit op de logpagina, boven of onder:

   * Gebruik de navigatieopties **[!UICONTROL First]**, **[!UICONTROL Prev]**, **[!UICONTROL Next]**, **[!UICONTROL Last]**, of **[!UICONTROL Go to line]** om door het logboek te bewegen.

   * Gebruik de weergaveopties **[!UICONTROL Errors only]**, **[!UICONTROL Wrap line]** of **[!UICONTROL Show]** om te verfijnen wat u ziet.

