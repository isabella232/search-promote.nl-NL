---
description: U kunt Rollback aan file gebruiken en websiteindexen archiveren die u hebt geproduceerd. U kunt de steun van een index op elk ogenblik ook herstellen.
seo-description: U kunt Rollback aan file gebruiken en websiteindexen archiveren die u hebt geproduceerd. U kunt de steun van een index op elk ogenblik ook herstellen.
seo-title: Ongeveer Terugschroeven van prijzen voor indexen
solution: Target
subtopic: Rollback
title: Ongeveer Terugschroeven van prijzen voor indexen
topic: Index,Site search and merchandising
uuid: abed878a-71b3-4122-9822-7410f4427a9a
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a

---


# Ongeveer Terugschroeven van prijzen voor indexen{#about-rollback-for-indexes}

U kunt [!DNL Rollback] aan file gebruiken en websiteindexen archiveren die u hebt geproduceerd. U kunt de steun van een index op elk ogenblik ook herstellen.

## Het gebruiken van Terugschroeven van prijzen voor indexen {#concept_0BC4BC975DB045A986C3607CF32705D8}

Het archief bevat vier indexen: de huidige plaatsindex, en drie vorige plaatsindexen, die de onderzoeksrobot automatisch archiveert die op de het terugschroeven van prijzenconfiguratie montages wordt gebaseerd. Telkens als uw website wordt geïndexeerd, wordt het archief bijgewerkt. De nieuwere indexen vervangen bestaande gearchiveerde indexen zodat het archief altijd huidig blijft.

Elke gearchiveerde index is vermeld in het archief met de volgende informatie:

* Datum en tijd de index werd voltooid.
* Index leeftijd.
* Aantal geïndexeerde documenten.
* Het indexeren verrichtingstype (volledig, stijgend, etc.).
* De status van de index zoals of de index momenteel actief is, en of het na de volgende index zal worden gehouden of worden verwijderd.

Telkens als uw website wordt geïndexeerd, wordt de nieuwe index toegevoegd aan het archief, en een bestaande gearchiveerde index wordt verwijderd. Merk op, echter, dat de oudste index niet noodzakelijk is die wordt verwijderd. Wanneer een nieuwe index aan het archief wordt toegevoegd, wordt een leeftijdsvergelijking gemaakt van elke gearchiveerde index aan de leeftijd die in de het terugschroeven van prijzenconfiguratie montages wordt gespecificeerd. De index die het verst van het gewenste programma is wordt verwijderd. Bijvoorbeeld, veronderstel configuratie het plaatsen 24.48.72 is en de leeftijd van de bewaarde indexen zijn 5, 23, 47, en 71. De meest recente index (die vijf uur oud is) wordt verwijderd wanneer een nieuwe index aan het archief wordt toegevoegd omdat zijn leeftijd het verst van de montages is. Voor gemak, de archiefnota&#39;s die de index wordt verwijderd wanneer de plaats opnieuw wordt geïndexeerd.

U kunt aan andere gebieden binnen het gebruikersinterface navigeren terwijl een index wordt geactiveerd. Een statusindicator houdt spoor van de activeringsvooruitgang en is beschikbaar wanneer u de [!DNL Rollback] pagina bekijkt. Als een gearchiveerde index wordt hersteld, worden de gebruikers op de hoogte gebracht bij de bovenkant van de Volledige Index, de Stijgende Index, de Scripted Index, en Regenerate pagina&#39;s. Geen indexerende verrichting kan voorkomen terwijl een index wordt hersteld. Als een het terugschroeven van prijzenverrichting met een geplande plaatsindex strijdig is, wordt het geplande indexeren uitgesteld tot het terugschroeven van prijzen heeft gebeëindigd. Als een index reeds lopend is, dan wordt het geannuleerd, op voorwaarde dat de gebruiker bevestigt dat het terugschroeven van prijzen prioriteit ontvangt.

Om de integriteit van het archief te handhaven, werkt de onderzoeksrobot niet het het terugschroeven van prijzenarchief bij als de fouten tijdens kruipend worden gevonden. Er is ook geen update als een gebruiker een het indexeren verrichting annuleert. Als een het indexeren verrichting de maximumtijd, bytes, pagina&#39;s, of documenten overschrijdt, voltooit crawler de index en voegt het aan het archief toe. Bovendien als het minimumaantal pagina&#39;s niet tijdens een het indexeren verrichting wordt voldaan aan, annuleert de kruipper de index en de vorige index blijft actief.

## Het vormen van het terugschroeven van prijzenarchiveringsprogramma van indexen {#task_CD403B9AE2244B13A6B3861B5F9B055C}

U kunt gebruiken [!DNL Configure] om te bepalen welke indexdossiers die u in het het terugschroeven van prijzenarchief wilt opslaan. Het archief kan de huidige index en drie reservesindexen opslaan.

Het **[!UICONTROL Schedule]** gebied bevat drie komma-gescheiden waarden die uren van het heden vertegenwoordigen. Bijvoorbeeld, specificeren de programmawaarden 24.48.72 24 uur van heden of gisteren, 48 uur van heden of twee dagen geleden, en 72 uur van vandaag of drie dagen geleden.

Het onderzoek archiveert voortdurend de plaatsindexen die het dichtst aan één dag, twee dagen, en drie dagen oud zijn. De daadwerkelijke tijden en de data van de gearchiveerde indexen kunnen afhankelijk van het indexerende programma van uw website variëren.

**Om het terugschroeven van prijzenarchiveringsprogramma van indexen te vormen**

1. Klik in het productmenu op **[!UICONTROL Index]** > **[!UICONTROL Rollback]** > **[!UICONTROL Configure]**.
1. Voor de [!DNL Rollback Configuration] pagina, op het **[!UICONTROL Schedule]** gebied, ga een bevel gescheiden lijst van drie indextijden, in uren in. De indexen dichtst bij deze tijden worden bewaard.
1. Klik op **[!UICONTROL Save Changes]**.

## Een gearchiveerde index activeren {#task_5DCE3D660F6F4197993E92AA59227332}

U kunt het Terugschroeven van prijzen gebruiken om een gearchiveerde index te activeren.

Wanneer u klikt **[!UICONTROL Activate]** om een index terug te schroeven, wordt de momenteel actieve index bewogen in het archief.

Na de activering van de gearchiveerde index, wordt u teruggegeven aan de [!DNL Activate Index] pagina. De informatie over het indexterugschroeven van prijzen wordt getoond. Ook, identificeert de [!DNL Activate] kolom in de [!DNL Available Indexes] lijst de gewalste achterindex met de status &quot;Actieve Index&quot;.

1. Klik in het productmenu op **[!UICONTROL Index]** > **[!UICONTROL Rollback]** > **[!UICONTROL Rollback]**.
1. Voor de [!DNL Activate Index] pagina, in de [!DNL Available Indexes] lijst, klik **[!UICONTROL Activate]** voor het bijbehorende gearchiveerde indextype dat u actief wilt maken.

   Gebruik de Datum, de Leeftijd, de Pagina&#39;s, en de kolommen van de Verrichting om u te helpen bepalen welke te activeren index.
1. Voor de [!DNL Verify Rollback] pagina, herzie de indexinformatie om te verifiëren dat u de correcte index hebt geselecteerd, en klik dan **[!UICONTROL Activate Now]**.

## Het bekijken van het logboek van alle indexterugschroeven van prijzen {#task_D2D9AA7203F0465FB5AE0D49212AC41C}

Bekijk de datum en de tijd van alle terugschroeven van prijzen verwante verrichtingen.

**Om het logboek van alle indexterugschroeven van prijzen te bekijken**

1. Voor het productmenu, doe één van het volgende:

   * Klik op **[!UICONTROL Index]** > **[!UICONTROL Re-Rank Index]** > **[!UICONTROL Live Log]**.

   * Klik op **[!UICONTROL Index]** > **[!UICONTROL Re-Rank Index]** > **[!UICONTROL Staged Log]**.

1. Voor de logboekpagina, bij de bovenkant of de bodem, doe om het even welke volgend:

   * Gebruik de navigatieopties **[!UICONTROL First]**, **[!UICONTROL Prev]**, **[!UICONTROL Next]**, **[!UICONTROL Last]**, of **[!UICONTROL Go to line]** om zich door het logboek te bewegen.

   * Gebruik de vertoningsopties **[!UICONTROL Errors only]**, **[!UICONTROL Wrap line]**, of **[!UICONTROL Show]** om te raffineren wat u ziet.

