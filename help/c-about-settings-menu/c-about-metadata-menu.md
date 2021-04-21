---
description: Gebruik het menu Metagegevens om zoekdefinities en indexinjecties aan te passen.
solution: Target
subtopic: Metadata
title: Het menu Metagegevens
topic-legacy: Settings,Site search and merchandising
uuid: f12fc863-a140-45e8-b219-3dbfdef099cd
exl-id: 53d62da9-c5bd-4c4a-bb89-743704f66f7f
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '8024'
ht-degree: 0%

---

# Informatie over het menu Metagegevens{#about-the-metadata-menu}

Gebruik het menu Metagegevens om zoekdefinities en indexinjecties aan te passen.

## Informatie over definities {#concept_AE48035C210145169BE067D396975620}

U kunt [!DNL Definitions] gebruiken om de inhoud en de relevantie van de HTML en meta-gegevensgebieden aan te passen die worden overwogen wanneer een klant een onderzoeksvraag voorlegt.

U kunt de velden bewerken die al vooraf zijn gedefinieerd. U kunt ook nieuwe door de gebruiker gedefinieerde velden maken op basis van de inhoud van de metagegevenstag. Elke definitie wordt weergegeven op één regel op de pagina [!DNL Staged Definitions].

Zie ook [Informatie over gegevensweergaven](../c-about-reports-menu/c-about-data-views.md#concept_DCA897D074464BC1861AA47B40CC86C3).

## Een nieuw metatag veld {#task_6DF188C0FC7F4831A4444CA9AFA615E5} toevoegen

U kunt uw eigen velden voor metagegevenstag definiëren en toevoegen.

Voordat de effecten van de nieuwe definitie van de meta-tag zichtbaar zijn voor klanten, moet u de index van de site opnieuw genereren.

**Een nieuw meta-tagveld toevoegen**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**.
1. Klik op [!DNL Definitions] op de pagina.**[!UICONTROL Add New Field]**
1. Stel op de pagina [!DNL Add Field] de gewenste opties in.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Veldnaam </p> </td> 
      <td colname="col2"> <p>Hiermee geeft u een naam op die wordt gebruikt om naar het veld te verwijzen. </p> <p>De veldnaam moet aan de volgende regels voldoen: </p> <p> 
      <ul id="ul_D39D09CD7E7D41A59ECB6C5A6F4F263D"> 
      <li id="li_11CE852BE3C64CEF90FEC7A6E1079E13"> De naam mag alleen alfanumerieke tekens bevatten. </li> 
      <li id="li_7FC340E7C58545C88CE9AF4AF09AD7AD"> De naam mag streepjes bevatten, maar geen spaties. </li> 
      <li id="li_996FF38457AB4C6DB22B15850A0830CC"> U kunt een naam van maximaal 20 tekens invoeren. </li> 
      <li id="li_C1019E587995444D9587D5EA495D719E"> De naam is niet hoofdlettergevoelig, maar wordt exact weergegeven en opgeslagen terwijl u de naam typt. </li> 
      <li id="li_E55404D6CE354EC89CFFEB1048A11F44"> U kunt niet de namen gebruiken die in de vooraf bepaalde gebieden zoals die in de lijst op <span class="wintitle"> Geleide Definities </span> pagina bestaan. </li> 
      <li id="li_7CE328AE3B5F45A8A09E2DA7ECB62551"> U kunt het woord "om het even welk"niet als waarde van een user-defined gebiedsnaam gebruiken. </li> 
      <li id="li_9B8287EED1784E79BFCBBBA956705CD2"> U kunt de namen van vooraf gedefinieerde velden niet bewerken. </li> 
      </ul> </p> <p> Voorbeelden van veldnamen: </p> <p> 
      <ul id="ul_5881669913D04E35A6D4A6D31BEE7DF3"> 
        <li id="li_0AFFB8B516FE40F8A615C2F578F2CEA3"> auteur </li> 
        <li id="li_7F0ADFBFB21E4B84ACA8A1CEBFE344D1"> PublishDate </li> 
        <li id="li_6D1BEB3D19AC499E9227EC115AEB6296"> iets wild </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Naam/namen metatag </p> </td> 
      <td colname="col2"> <p>Bepaalt de inhoud die aan het gedefinieerde veld is gekoppeld. </p> <p>De lijst met namen kan maximaal 255 tekens lang zijn. En naam kan alle tekens bevatten die zijn toegestaan in het naamkenmerk van een HTML-metatag. </p> <p>U kunt meerdere metatags opgeven in één velddefinitie. </p> <p>Meerdere waarden moeten door komma's van elkaar worden gescheiden en de naam van de meest linkse meta-tag die op een bepaalde webpagina wordt gevonden, krijgt voorrang. </p> <p>Stel dat u een veld met de naam "auth" hebt gedefinieerd. De veldnaam heeft de bijbehorende metatags "auteur, dc.auteur". In dit geval wordt de inhoud van de metatag "auteur" geïndexeerd en wordt deze doorzocht op die van "dc.auteur" als beide metatags op een webpagina worden weergegeven. </p> <p>Door de gebruiker gedefinieerde velden moeten minstens één metatag-tagnaam in hun definitie hebben. Vooraf gedefinieerde velden hoeven geen bijbehorende metatag te hebben. Als er echter een of meer metatags zijn opgegeven, heeft de inhoud van de metatags voorrang op de huidige gegevensbron voor elke tag. </p> <p>Als de metatag 'dc.title' bijvoorbeeld is gekoppeld aan het vooraf gedefinieerde veld 'title', wordt de inhoud van de metatag 'dc.title' geïndexeerd op die van de metatag 
      <code>
        &lt;title&gt; 
      </code> tag voor een bepaald document. </p> <p>Voorbeelden zijn: </p> <p> 
      <ul id="ul_0132E15FC19E4C0CA13CD5A12EA3BBEC"> 
      <li id="li_ECD3B194FECB4C2090CAEC8449320D3F"> dc.date </li> 
      <li id="li_09C76BC7AC7348859D01989697212E31"> beschrijving </li> 
      <li id="li_9230C0450F9D424087D1F127048DA311"> proprietarytag </li> 
      </ul> </p> </td> 
    </tr> 
      <tr> 
      <td colname="col1"> <p>Gegevenstype </p> </td> 
      <td colname="col2"> <p>Elk veld heeft een bijbehorend gegevenstype, zoals tekst, nummer, datum, versie, rang of locatie. Dit gegevenstype bepaalt hoe de inhoud van het veld wordt geïndexeerd, doorzocht en optioneel gesorteerd. </p> <p>U kunt het gegevenstype niet wijzigen nadat u de velddefinitie hebt gemaakt. </p> <p>Gebruik de volgende informatie om het gegevenstype te selecteren dat relevant is voor de informatie die het veld bevat. </p> <p> 
      <ul id="ul_A3AD5A0CF354410F836311F39151B8A6"> 
      <li id="li_9F412DA7D9EF497BA6E65F9CE10F3046"> <span class="uicontrol"> Tekstgegevenstypevelden worden behandeld als tekenreeksen.  </span>  </li> 
      <li id="li_AD78B75644AE40208F0239311015611F"> <span class="uicontrol"> Getaltypevelden  </span> worden behandeld als numerieke waarden met gehele getallen of drijvende komma. </li> 
      <li id="li_0B46975C589148E9A7C32A8D250487B7"> <span class="uicontrol"> Datumgegevenstypevelden worden behandeld als datum-/tijdspecificaties.  </span> U kunt de toegestane datum-/tijdnotaties aanpassen wanneer u het nieuwe veld toevoegt of bewerkt. </li> 
      <li id="li_BB68CB1DBE0543AC9000B3DEDFB28E7E"> <span class="uicontrol"> Velden met  </span> versietypen worden behandeld als numerieke gegevens in vrije vorm. 1.2.3 sorteert bijvoorbeeld vóór 1.2.2. </li> 
      <li id="li_0BA895B4DADA46528A7A4161EEB1521E"> <span class="uicontrol"> Rank  </span> gegevenstype velden worden op dezelfde manier behandeld als velden van het type "Number", behalve dat ze daarnaast de rangorde-/relevantieberekeningen in de zoekresultaten beïnvloeden. <p>Zie <a href="../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397" type="concept" format="dita" scope="local"> Informatie over rangschikkingsregels </a>. </p> </li> 
      <li id="li_459405DA437049AD88AA1FAC28F04720"> <span class="uicontrol"> Velden met  </span> locatiegegevens worden overal ter wereld beschouwd als een fysieke locatie. De toegestane plaatsformaten omvatten het volgende: <p> 
      <ul id="ul_D2CEBFA1A5504AA996BA2F7641AFB7F3"> 
      <li id="li_5283A2F2D5D84840B3D920C08D43654C"> ZIP-codes van 5 of 9 cijfers in de vorm van DDD of DDD-DDDD, waarbij elke "D" een cijfer van 0-9 is. </li> 
      <li id="li_A5CD4DFC90164BC68183DB7D10603B7C"> Driecijferige gebiedscodes in de vorm van DDD. </li> 
      <li id="li_9DAEAE64BC7F4902B25043D998C8F56D"> De paren van Latitude/lengtegraad in de vorm ±DD.DDDD±DDD.DDDD, waarbij het eerste getal de breedtegraad aangeeft en het tweede getal de lengtegraad. </li> 
      </ul> </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>lijsten van gewenste personen </p> </td> 
      <td colname="col2"> <p>Alleen beschikbaar als het gegevenstype <span class="uicontrol"> Tekst </span> of <span class="uicontrol"> Nummer </span> is geselecteerd. </p> <p>Door indexering gescheiden waarden in de metagegevensinhoud van dit veld. </p> <p>De inhoud "Rood, Geel, Groen, Blauw" wordt bijvoorbeeld behandeld als vier aparte waarden in plaats van één als "Lijsten van gewenste personen" is geselecteerd. Deze behandeling is vooral handig bij het zoeken naar bereiken (met 
      <code>
        sp_q_min 
      </code>, 
      <code>
        sp_q_max 
      </code>, of 
      <code>
        sp_q_exact 
      </code>) en met de 
      <code>
        &lt;search-field-value-list&gt; 
      </code>, 
      <code>
        &lt;search-field-values&gt; 
      </code>, en 
      <code>
        &lt;search-display-field-values&gt; 
      </code>. </p> <p>Niet beschikbaar als het gegevenstype Versie is geselecteerd. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Dynamisch facet </p> </td> 
      <td colname="col2"> <p> 
        <!--NEW 2/2/2014--> <p>Opmerking:  Deze functie is niet standaard ingeschakeld. Neem contact op met Technische ondersteuning om deze te activeren voor gebruik. Nadat deze is geactiveerd, wordt deze weergegeven in de gebruikersinterface. </p> </p> <p>Hiermee wordt het geïdentificeerde facet ingesteld op dynamisch. </p> <p>Facetten worden boven op metatag-tagvelden gebouwd. Een metatag etiketgebied is een laag-vlakke, kernonderzoekslaag van Adobe Search&amp;Promote. Facetten daarentegen maken deel uit van GS (Guided Search) - de presentatielaag op hoog niveau van Adobe Search&amp;Promote. Facetten hebben echter eigen velden voor metatags, maar velden voor metatags weten niets over facetten. </p> <p>Zie <a href="../c-about-design-menu/c-about-dynamic-facets.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> Informatie over dynamische factoren </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Dedupe toestaan </p> </td> 
      <td colname="col2"> <p>Schakel deze optie in als u deduplicatie wilt inschakelen voor dit veld. Dat wil zeggen dat dit veld tijdens het zoeken kan worden opgegeven met de opdracht 
        <code>
          sp_dedupe_field 
        </code> CGI-parameter zoeken. </p> <p>Zie <a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> CGI-parameters doorzoeken </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Tabelnaam </p> </td> 
      <td colname="col2"> <p>Koppelt het opgegeven veld permanent aan de opgegeven tabelnaam. </p> <p>Telkens wanneer een dergelijk veld wordt vermeld binnen een CGI-kernzoekparameter of een sjabloontag, wordt de tabelnaam automatisch opgegeven. Met deze functie kunt u dynamische facetten selecteren via tabelovereenkomsten, maar u kunt deze desgewenst ook gebruiken voor niet-dynamische facetvelden. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Lijstscheidingstekens </p> </td> 
      <td colname="col2"> <p>Alleen beschikbaar als <span class="uicontrol"> Lijsten van gewenste personen </span> is geselecteerd. </p> <p>Geeft aan welke tekens afzonderlijke lijstwaarden scheiden. U kunt meerdere tekens opgeven, die elk als waardescheidingsteken worden behandeld. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Standaard zoeken </p> </td> 
      <td colname="col2"> <p>Als deze optie is geselecteerd, wordt de inhoud van het veld doorzocht, zelfs als het veld niet expliciet is opgegeven in een bepaalde zoekopdracht. Als u deze optie uitschakelt, wordt alleen op verzoek naar het veld gezocht. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Verticaal updateveld </p> </td> 
      <td colname="col2"> <p> <p>Opmerking:  Deze functie is niet standaard ingeschakeld. Neem contact op met Technische ondersteuning om deze te activeren voor gebruik. Nadat deze is geactiveerd, wordt deze weergegeven in de gebruikersinterface. </p> </p> <p>Hiermee wordt ingesteld dat het opgegeven veld een veld Verticale update is. </p> <p>Verticale updatevelden zijn kandidaten die moeten worden bijgewerkt via het Verticale updateproces ( <span class="uicontrol"> Index </span> &gt; <span class="uicontrol"> Verticale update </span>). Vanwege de manier waarop Verticale updates worden uitgevoerd, kan de inhoud van deze velden niet worden doorzocht in vrije-tekstzoekopdrachten. Als u deze optie inschakelt, wordt de inhoud van dit veld tijdens enige indexbewerking niet toegevoegd aan de index van het woord. Het laat ook de update van dit gebied tijdens een Verticale Update verrichting toe. </p> <p>Voor meer over Verticale Updates, zie <a href="../c-about-index-menu/c-about-vertical-updates.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> over Verticale Update </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Relevantie </p> </td> 
      <td colname="col2"> <p>U kunt de relevantie van vooraf gedefinieerde en door de gebruiker gedefinieerde velden bewerken. </p> <p>Relevantie wordt opgegeven op schaal 1-10. Een bepaling van 1 betekent dat het de minst relevante en 10 het meest relevant is. Met deze waarden wordt rekening gehouden wanneer de software de vraaggelijken op elk gebied overweegt. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Sorteren </p> </td> 
      <td colname="col2"> <p>Hiermee geeft u aan wanneer de resultaten op het benoemde veld worden gesorteerd via de optie 
        <code>
          sp_s 
        </code> CGI-parameter zoeken. </p> <p>Zie <a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> CGI-parameters doorzoeken </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Taal </p> </td> 
      <td colname="col2"> <p>Alleen beschikbaar als het gegevenstype <span class="uicontrol"> Rank </span>, <span class="uicontrol"> Number </span> of <span class="uicontrol"> Date </span> is geselecteerd. </p> <p>Hiermee bepaalt u de taal en de landinstellingen die worden toegepast bij het indexeren van de datum-, getal- en rangtelwaarden voor dit veld. </p> <p>U kunt de accounttaal toepassen (Taalkundige opties &gt; Woorden en talen). U kunt ook de taal toepassen die is gekoppeld aan het document dat elk nummer of datumwaarde bevat, of een specifieke taal. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Datumnotatie(s) </p> </td> 
      <td colname="col2"> <p>Alleen beschikbaar als het gegevenstype <span class="uicontrol"> Datum </span> is geselecteerd. </p> <p>Bepaalt de datumnotaties die worden herkend bij het indexeren van datumwaarden voor dit veld. </p> <p>Voor elk datumveld wordt een standaardlijst met datumnotatietekenreeksen weergegeven. U kunt de lijst aan de lijst toevoegen of de lijst aan de behoeften van uw eigen site aanpassen. </p> <p>Zie <a href="../c-appendices/r-date-formats.md#reference_4D1FC1F6B9F44857967188496D8D335B" type="reference" format="dita" scope="local"> Datumnotaties </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Datumnotaties testen </p> </td> 
      <td colname="col2"> <p>Alleen beschikbaar als het gegevenstype <span class="uicontrol"> Datum </span> is geselecteerd als gegevenstype. </p> <p>Hiermee kunt u een voorvertoning weergeven van de datumnotaties die u hebt opgegeven om ervoor te zorgen dat deze correct zijn opgemaakt. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Tijdzone </p> </td> 
      <td colname="col2"> <p>Alleen beschikbaar als het gegevenstype <span class="uicontrol"> Datum </span> is geselecteerd als gegevenstype. </p> <p>Bepaalt de veronderstelde tijdzone die wordt toegepast bij het indexeren van datumwaarden voor dit veld dat geen tijdzone opgeeft. </p> <p>Als de tijdzone van uw account bijvoorbeeld is ingesteld op "America/Los Angeles" en u <span class="uicontrol"> Accounttijdzone </span> gebruiken selecteert, wordt de volgende metadatumwaarde, die geen opgegeven tijdzone heeft, behandeld als Pacific Time, waarbij rekening wordt gehouden met zomertijd: </p> <p>&lt;meta name="dc.date" content="Mon, 05 Sep 201213:12:00"&gt; </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Minste belangrijke Rankwaarde </p> </td> 
      <td colname="col2"> <p>Alleen beschikbaar als het gegevenstype <span class="uicontrol"> Rank </span> is geselecteerd als gegevenstype. </p> <p>Hiermee bepaalt u de randewaarde die de minimumrang van een document vertegenwoordigt. </p> <p>Als de rangschikking in het document varieert van 0 voor de laagste rang tot 10 voor de hoogste rang, stelt u deze waarde in op 0. </p> <p>Als de rangschikking in het document varieert van 1 voor de hoogste rang tot 10 voor de laagste rang, stelt u deze waarde in op 10. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Standaardwaarde voor Rank </p> </td> 
      <td colname="col2"> <p>Alleen beschikbaar als het gegevenstype <span class="uicontrol"> Rank </span> is geselecteerd als gegevenstype. </p> <p>Controls the rank value that is used if a document does not contain any of meta tags that are defined for this rank field. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Belangrijkste Rank-waarde </p> </td> 
      <td colname="col2"> <p>Alleen beschikbaar als het gegevenstype <span class="uicontrol"> Rank </span> is geselecteerd als gegevenstype. </p> <p>Hiermee bepaalt u de randewaarde die de maximumhoek van een document vertegenwoordigt. </p> <p>Als de rangschikking in het document varieert van 0 voor de laagste rang tot 10 voor de hoogste rang, stelt u deze waarde in op 10. </p> <p>Als de rangschikking in het document varieert van 1 voor de hoogste rang tot 10 voor de laagste rang, stelt u deze waarde in op 1. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Standaardeenheden </p> </td> 
      <td colname="col2"> <p>Alleen beschikbaar als het gegevenstype <span class="uicontrol"> Locatie </span> is geselecteerd als gegevenstype. </p> <p>Bepaalt de behandeling van afstandswaarden voor zoeken in nabijheid. </p> <p>Als u de standaardeenheden op <span class="uicontrol"> Miles </span> plaatst, dan om het even welke nabijheidsonderzoek minimum/maximumafstandscriteria die op dit gebied (als 
      <code>
        sp_q_min[_#] 
      </code> of de 
      <code>
        sp_q_max[_#] 
      </code> CGI-zoekparameters) wordt beschouwd als mijlen, anders als kilometers. </p> <p>Met deze optie stelt u ook de standaardafstandseenheden in die worden toegepast op de uitvoer van het dialoogvenster 
      Sjabloontag voor zoekresultaten <code>
        &lt;Search-Display-Field&gt; 
      </code> wanneer toegepast op een nabijheidsveld voor zoekresultaten. </p> <p>Zie <a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> Info over nabijheidszoekopdracht </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Bereik omschrijven? </p> </td> 
      <td colname="col2"> <p>Alleen beschikbaar als <span class="uicontrol"> Nummer </span> is geselecteerd als gegevenstype. </p> <p>Bepaalt het automatisch maken van veldbereikbeschrijvingen voor gebruik met <span class="uicontrol"> Ontwerp </span> &gt; <span class="uicontrol"> Navigatie </span> &gt; <span class="uicontrol"> Facets </span>. </p> <p>Zie <a href="../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5" format="dita" scope="local"> Informatie over facetten </a>. </p> <p> <p>Opmerking:  Als voor dit veld <span class="uicontrol"> Verticaal updateveld </span> is ingeschakeld, wordt het gegenereerde veld met de beschrijving van het veldbereik bijgewerkt tijdens een verticale update. Het wordt echter aanbevolen dat in het veld <span class="uicontrol"> Bereik </span> ook <span class="uicontrol"> Verticaal updateveld </span> is ingeschakeld. </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Bereik </p> </td> 
      <td colname="col2"> <p>Deze optie is alleen beschikbaar als <span class="uicontrol"> Beschrijving van bereik maken </span> is ingeschakeld. </p> <p>Het veld <span class="uicontrol"> Tekst </span> dat moet worden bijgewerkt met bereikbeschrijvingen voor het huidige veld. Deze lijst bevat alle <span class="uicontrol"> tekstvelden </span> die nog niet worden gebruikt met andere velden voor het genereren van veldbereik. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Bereik waarden </p> </td> 
      <td colname="col2"> <p>Alleen beschikbaar als <span class="uicontrol"> Beschrijving bereik maken </span> is ingeschakeld en een <span class="uicontrol">-veld </span> item is geselecteerd. </p> <p>Een door lege waarden gescheiden lijst met gegevenspunten die moet worden gebruikt bij het maken van de beschrijvingen voor veldbereik. Bijvoorbeeld: </p> <code> 10&amp;nbsp;20&amp;nbsp;50&amp;nbsp;100&amp;nbsp;1000 </code> <p>U kunt deze waarden in elke gewenste volgorde invoeren. De waarden worden gesorteerd en duplicaten worden verwijderd voordat deze worden opgeslagen. U kunt ook negatieve en niet-gehele waarden opgeven. </p> <p>Voor elk van de waarden in dit veld: 
      <ul id="ul_C4B41AF5AADF4B84B9C489CE82FF7075"> 
      <li id="li_90736394A5AE4F5CA6B47687BCB627AA">als de waarde kleiner is dan (&lt;) de kleinste waarde in <span class="uicontrol"> Range Values </span>, wordt <span class="uicontrol"> "Minder dan" Format </span> gebruikt </li> 
      <li id="li_A5C272B2D26A468CA07EB2046B2EA8A7">als de waarde groter dan of gelijk aan (&gt;=) de grootste waarde in <span class="uicontrol"> de Waarden van het Bereik </span> is, wordt <span class="uicontrol"> "Groter dan"Formaat </span> gebruikt. </li> 
      <li id="li_9DDFB70E1E824CF4819C57450C1A6DD2">anders wordt een "bereik" gevonden wanneer de veldwaarde tussen twee opeenvolgende <span class="uicontrol"> Range Values </span> (groter dan (&gt;) de kleinere waarde en kleiner dan of gelijk aan (&lt;=) de grotere waarde) valt, en wordt <span class="uicontrol"> Intermediate Format </span> gebruikt. </li> 
    </ul> </p> <p>In de bovenstaande voorbeeldset met waarden wordt bijvoorbeeld een set beschrijvingen voor waarden gedefinieerd: 
    <ul id="ul_03ED30D5A19346AB8E6809BDD186A9A9"> 
      <li id="li_F97A6B3763954EFE9B6751F472AF7D20">minder dan 10 </li> 
      <li id="li_12B6F636A6444B8292E0BFE4F55032DF">groter dan of gelijk aan 10 en kleiner dan 20 </li> 
      <li id="li_545A2EAF5BD046B5AD59B77DB43DCD14">groter dan of gelijk aan 20 en kleiner dan 50 </li> 
      <li id="li_26A8CD2422524D2CBD36794C6908572A">groter dan of gelijk aan 50 en kleiner dan 100 </li> 
      <li id="li_05EBEEE68DC348E0821F1CC16D04D69C">groter dan of gelijk aan 100 en kleiner dan 10000 </li> 
      <li id="li_9513A6B519394780A6A41B80762A0370">groter dan of gelijk aan 10000 </li> 
      </ul> </p> <p>Zie <span class="uicontrol"> Testen met Groter dan? </span> de wijze waarop deze tests worden uitgevoerd te wijzigen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Indeling voor "kleiner dan" </p> </td> 
      <td colname="col2"> <p>Alleen beschikbaar als <span class="uicontrol"> Beschrijving bereik maken </span> is ingeschakeld en een <span class="uicontrol">-veld </span> item is geselecteerd. </p> <p>Dit is het malplaatje wordt gebruikt om de waaierbeschrijving voor waarden te specificeren minder dan de kleinste waarde die in <span class="uicontrol"> de Waarden van de Waaier </span> wordt gevonden. De kleinste waarde wordt weergegeven met de numerieke placeholder token <span class="uicontrol"> ~N~ </span>. Bijvoorbeeld: </p> <code> Less&amp;nbsp;than&amp;nbsp;~N~ </code> <p>of: </p> <code> ~N~&amp;nbsp;and&amp;nbsp;below </code> <p>Normaal gesproken wordt de waarde "as-is" opgemaakt. Bij een <span class="uicontrol">-definitie van "5 10 20" en een opgegeven waarde van 1 zou de gegenereerde bereikbeschrijving simpelweg "Minder dan 5" zijn. </span> Als u in plaats daarvan "4.99 en hieronder"wilt hebben, plaats <span class="uicontrol"> Precisie </span> aan <span class="uicontrol"> 2 </span> en gebruik dit formaat: </p> <code> ~n~&amp;nbsp;and&amp;nbsp;below </code> <p>In <span class="uicontrol"> "Minder dan"Formaat </span>, zal het kleine geval <span class="uicontrol"> ~n~ </span> ertoe leiden dat de waarde <i>down</i> volgens <span class="uicontrol"> Precision </span> plaatsen wordt afgerond. </p> <p>Opmerking: om een numerieke plaatsaanduiding in de bereikbeschrijving op te nemen, zoals ook het geval is, geeft u een backslash (\)-voorvoegsel op, bijvoorbeeld <span class="uicontrol"> \~N~ </span> of <span class="uicontrol"> \~n~ </span>. Als u een backslash-teken wilt opnemen, geeft u dit op met een andere backslash, bijvoorbeeld <span class="uicontrol"> \\ </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Intermediaire indeling </p> </td> 
      <td colname="col2"> <p>Alleen beschikbaar als <span class="uicontrol"> Beschrijving bereik maken </span> is ingeschakeld en een <span class="uicontrol">-veld </span> item is geselecteerd. </p> <p>Dit is het malplaatje wordt gebruikt om de waaierbeschrijving voor waarden te specificeren die tussen de kleinste en grootste waarden vallen die in <span class="uicontrol"> de Waarden van de Waaier </span> worden gevonden. Voor het opgegeven bereik wordt de onderste bereikwaarde weergegeven met de numerieke placeholder token <span class="uicontrol"> ~L~ </span>, en de hogere bereikwaarde wordt weergegeven met de token <span class="uicontrol"> ~H~ </span>. Bijvoorbeeld: </p> <code> ~L~&amp;nbsp;to&amp;nbsp;~H~ </code> <p>of: </p> <code> Between&amp;nbsp;~L~&amp;nbsp;and&amp;nbsp;~H~ </code> <p>of: </p> <code> Less&amp;nbsp;than&amp;nbsp;~H~&amp;nbsp;and&amp;nbsp;greater&amp;nbsp;than&amp;nbsp;~L~ </code> <p>Normaal gesproken worden de waarden opgemaakt als 'as-is' - d.w.z. voor een <span class="uicontrol">-definitie van "5 10 20" en een opgegeven waarde van 8 zou de gegenereerde bereikbeschrijving simpelweg iets zijn als "Tussen 5 en 10". </span> Als u in plaats daarvan het "tussen 5 en 9.99"zou willen hebben, met de hogere waarde aangepast <i>onderwaarts </i>, plaats <span class="uicontrol"> Precisie </span> aan <span class="uicontrol"> 2 </span> en gebruik dit formaat: </p> <code> Between&amp;nbsp;~L~&amp;nbsp;and&amp;nbsp;~h~ </code> <p>Op dezelfde manier kan <span class="uicontrol"> ~L~ </span> worden vervangen door <span class="uicontrol"> ~l~ </span> om de lagere waarde te laten aanpassen <i>opwaarts</i>, ook volgens de instelling <span class="uicontrol"> Precisie </span>. Dit betekent dat een definitie als: </p> <code> Between&amp;nbsp;~l~&amp;nbsp;and&amp;nbsp;~H~ </code> <p>met een <span class="uicontrol"> precisie </span> waarde van <span class="uicontrol"> 2 </span> zou "tussen 5.01 en 10"tot stand brengen. </p> <p>De kleine letter <span class="uicontrol"> ~l~ </span> zorgt ervoor dat de lagere waarde <i>up</i> wordt afgerond volgens de <span class="uicontrol"> Precision </span>-instelling, en de kleine letter <span class="uicontrol"> ~h~ </span> zorgt ervoor dat de hogere waarde <i>down</i> wordt afgerond. </p> <p>Opmerking: om een numerieke plaatsaanduiding in de bereikbeschrijving op te nemen, zoals ook het geval is, geeft u een backslash (\)-voorvoegsel op, bijvoorbeeld <span class="uicontrol"> \~L~ </span> of <span class="uicontrol"> \~h~ </span>. Als u een backslash-teken wilt opnemen, geeft u dit op met een andere backslash, bijvoorbeeld <span class="uicontrol"> \\ </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Indeling "Groter dan" </p> </td> 
      <td colname="col2"> <p>Alleen beschikbaar als <span class="uicontrol"> Beschrijving bereik maken </span> is ingeschakeld en een <span class="uicontrol">-veld </span> item is geselecteerd. </p> <p>Dit is het malplaatje wordt gebruikt om de waaierbeschrijving voor waarden te specificeren groter dan de grootste waarde die in <span class="uicontrol"> de Waarden van de Waaier </span> wordt gevonden. De grootste waarde wordt weergegeven met de numerieke placeholder token <span class="uicontrol"> ~N~ </span>. Bijvoorbeeld: </p> <code> Greater&amp;nbsp;than&amp;nbsp;~N~ </code> <p>of: </p> <code> ~N~&amp;nbsp;and&amp;nbsp;above </code> <p>Normaal gesproken wordt de waarde "as-is" opgemaakt. Bij een <span class="uicontrol">-definitie van "5 10 20" en een opgegeven waarde van 30 zou de gegenereerde bereikbeschrijving simpelweg "Groter dan 20" zijn. </span> Als u in plaats daarvan het "20.01 en hierboven"wilt hebben, plaats <span class="uicontrol"> Precisie </span> aan <span class="uicontrol"> 2 </span> en gebruik dit formaat: </p> <code> ~n~&amp;nbsp;and&amp;nbsp;above </code> <p>In <span class="uicontrol"> "Groter dan"formaat </span>, zal het kleine geval <span class="uicontrol"> ~n~ </span> de waarde veroorzaken om <i>up</i> volgens <span class="uicontrol"> Precision </span> plaatsen worden rond gemaakt. </p> <p>Opmerking: om een numerieke plaatsaanduiding in de bereikbeschrijving op te nemen, zoals ook het geval is, geeft u een backslash (\)-voorvoegsel op, bijvoorbeeld <span class="uicontrol"> \~N~ </span> of <span class="uicontrol"> \~n~ </span>. Als u een backslash-teken wilt opnemen, geeft u dit op met een andere backslash, bijvoorbeeld <span class="uicontrol"> \\ </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Precisie </p> </td> 
      <td colname="col2"> <p>Alleen beschikbaar als <span class="uicontrol"> Beschrijving bereik maken </span> is ingeschakeld en een <span class="uicontrol">-veld </span> item is geselecteerd. </p> <p>Een geheel getal dat het aantal cijfers rechts van een decimaalteken opgeeft. Dit heeft ook betrekking op afrondingsbewerkingen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Strip leading zeros? </p> </td> 
      <td colname="col2"> <p>Alleen beschikbaar als <span class="uicontrol"> Beschrijving van bereik maken </span> is ingeschakeld, is een <span class="uicontrol">-veld </span> geselecteerd en is een waarde <span class="uicontrol"> Precisie </span> ingesteld die niet gelijk is aan nul. </p> <p>Moeten we "0,50" weergeven als ".50"? </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Strip volgnullen? </p> </td> 
      <td colname="col2"> <p>Alleen beschikbaar als <span class="uicontrol"> Beschrijving van bereik maken </span> is ingeschakeld, is een <span class="uicontrol">-veld </span> geselecteerd en is een waarde <span class="uicontrol"> Precisie </span> ingesteld die niet gelijk is aan nul. </p> <p>Moeten we '10.00' weergeven als '10'? </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Duizenden scheidingstekens tonen? </p> </td> 
      <td colname="col2"> <p>Alleen beschikbaar als <span class="uicontrol"> Beschrijving bereik maken </span> is ingeschakeld en een <span class="uicontrol">-veld </span> item is geselecteerd. </p> <p>Moeten we "10000" weergeven als "10.000"? Er worden landspecifieke waarden gebruikt. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nulwaarden aanpassen? </p> </td> 
      <td colname="col2"> <p>Alleen beschikbaar als <span class="uicontrol"> Beschrijving bereik maken </span> is ingeschakeld en een <span class="uicontrol">-veld </span> item is geselecteerd. </p> <p>Als afgeronde nulwaarden worden weergegeven, moeten deze naar boven of beneden worden afgerond volgens de <span class="uicontrol"> Precision </span>-instelling? d.w.z. "0.01" weergeven? </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Testen met Groter dan? </p> </td> 
      <td colname="col2"> <p>Alleen beschikbaar als <span class="uicontrol"> Beschrijving bereik maken </span> is ingeschakeld en een <span class="uicontrol">-veld </span> item is geselecteerd. </p> <p>Aangezien elke waarde tegen de waarden in <span class="uicontrol"> Waarden van de Waaier </span> wordt vergeleken, die in <i><b>dalende </b></i> orde worden verwerkt, wordt het, door gebrek, vergeleken gebruikend Groter dan of Gelijk (&gt;=) exploitant, die stopt zodra deze test slaagt. Dit betekent dat met een reeks van <span class="uicontrol"> Waarden </span> als "10 20 50 100 1000"zal de waarde 100 in de waaier 100 tot 1000 vallen, aangezien 100 inderdaad &gt;= 100 is. Als u liever hebt dat het binnen het bereik 50 tot 100 valt, controleert u deze optie, zodat de vergelijkingen in plaats daarvan de operator Groter dan (&gt;) gebruiken. </p> <p>Als deze optie bijvoorbeeld is ingeschakeld, geldt voor elk van de waarden in dit veld het volgende: 
      <ul id="ul_969621B1BD914FA5BD73ED21F8841010"> 
      <li id="li_157BEFDA7D0E44C481F4E4BC9046EF24">als de waarde kleiner dan of gelijk is aan (&lt;=) de kleinste waarde in <span class="uicontrol"> Range Values </span>, zal <span class="uicontrol"> "Minder dan"Formaat </span> worden gebruikt </li> 
      <li id="li_737EE666CA6243A8864E17A311CF3ACC">Als de waarde groter is dan (&gt;) de grootste waarde in <span class="uicontrol"> Waarden van bereik </span>, zal <span class="uicontrol"> "Groter dan"Formaat </span> worden gebruikt </li> 
      <li id="li_353A9820F7F74CCCBB3281EC4CB48734">anders zal een waaier worden gevonden waar de gebiedswaarde tussen twee opeenvolgende <span class="uicontrol"> Waarden </span> (groter dan of gelijk aan (&gt;=) de kleinere waarde en minder dan (&lt;) de grotere waarde) valt, en <span class="uicontrol"> Tussenliggende Formaat </span> zal worden gebruikt </li> 
    </ul> </p> <p>en, indien uitgeschakeld: 
    <ul id="ul_945844C33C2E4D95A598C4876E15F211"> 
      <li id="li_653B6E2934574DA3B4BCEF07D0A84527">als de waarde kleiner is dan (&lt;) de kleinste waarde in <span class="uicontrol"> Range Values </span>, wordt <span class="uicontrol"> "Minder dan" Format </span> gebruikt </li> 
      <li id="li_AECA6880002F40FAB1820B37237550A7">als de waarde groter dan of gelijk is aan (&gt;=) de grootste waarde in <span class="uicontrol"> Waarden van bereik </span>, zal <span class="uicontrol"> "Groter dan"Formaat </span> worden gebruikt </li> 
      <li id="li_ECB2DF7CA592497298E9ADC708220366">anders zal een waaier worden gevonden waar de gebiedswaarde tussen twee opeenvolgende <span class="uicontrol"> Waarden </span> (groter dan (&gt;) de kleinere waarde en minder dan of gelijk aan (&lt;=) de grotere waarde) valt, en <span class="uicontrol"> Tussenliggende Formaat </span> zal worden gebruikt </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Testen </p> </td> 
      <td colname="col2"> <p>Alleen beschikbaar als <span class="uicontrol"> Beschrijving bereik maken </span> is ingeschakeld en een <span class="uicontrol">-veld </span> item is geselecteerd. </p> <p>Geef een numerieke voorbeeldwaarde op en druk op de knop <span class="uicontrol"> Testen </span> om te zien hoe het veld Bereik wordt gemaakt. De gegenereerde beschrijving van het bereik wordt in het venster weergegeven. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   Zie ook [Een nieuw metatag toevoegen gebied](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).
1. Klik op **[!UICONTROL Add]**.
1. (Optioneel) Maak de gefaseerde site-index opnieuw als u een voorvertoning van de resultaten wilt zien.

   Zie [Een incrementele index van een gefaseerde website configureren](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Optioneel) Voer op de pagina [!DNL Definitions] een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Vooraf gedefinieerde of door de gebruiker gedefinieerde metatag-tagvelden {#task_0A7657B63596421BB6DB3ED44F827AB3} bewerken

U kunt alleen bepaalde velden in vooraf gedefinieerde metatags bewerken of alle velden in metatags bewerken die door de gebruiker zijn gedefinieerd.

Voordat de effecten van de wijzigingen in de metatag zichtbaar zijn voor klanten, moet u de index van de site opnieuw genereren.

**Vooraf gedefinieerde of door de gebruiker gedefinieerde metatagvelden bewerken**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**.
1. Klik op de pagina [!DNL Definitions] in de kolom [!DNL Actions] van de tabel op **[!UICONTROL Edit]** in de rij van de veldnaam van de metatag die u wilt wijzigen.
1. Op [!DNL Pinned Keyword Results Manager] pagina, in de lijst, klik **[!UICONTROL Edit]** in de rij van het sleutelwoord dat u wilt veranderen.
1. Stel op de pagina [!DNL Edit Field] de gewenste opties in.

   Als u wijzigingen wilt aanbrengen in een vooraf gedefinieerd metatag, moet u er rekening mee houden dat niet alle velden bewerkbaar zijn.

   Zie de optietabel onder [Een nieuw metatag toevoegen gebied](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).
1. Klik op **[!UICONTROL Save Changes]**.
1. (Optioneel) Maak de gefaseerde site-index opnieuw als u een voorvertoning van de resultaten wilt zien.

   Zie [Een incrementele index van een gefaseerde website configureren](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Optioneel) Voer op de pagina [!DNL Definitions] een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een door de gebruiker gedefinieerd metatag-tagveld {#task_9361EF38B5E743038B6672FA6CF70FD3} verwijderen

U kunt een door de gebruiker gedefinieerd meta-tagveld verwijderen dat u niet meer nodig hebt of gebruikt.

U kunt vooraf gedefinieerde velden voor metatags niet verwijderen. U kunt bepaalde velden echter wel bewerken.

Zie [Vooraf gedefinieerde of door de gebruiker gedefinieerde metatagvelden bewerken](../c-about-settings-menu/c-about-metadata-menu.md#task_0A7657B63596421BB6DB3ED44F827AB3).

Voordat de effecten van de meta-tag delete zichtbaar zijn voor klanten, moet u de index van de site opnieuw genereren.

**Een door de gebruiker gedefinieerd meta-tagveld verwijderen**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**.
1. Klik op de pagina [!DNL Definitions] in de sectie [!DNL User-defined fields] van de tabel op **[!UICONTROL Delete]** in de rij van de veldnaam van de metatag die u wilt verwijderen.
1. Klik in het dialoogvenster Bevestiging op **[!UICONTROL OK]**.
1. (Optioneel) Maak de gefaseerde site-index opnieuw als u een voorvertoning van de resultaten wilt zien.

   Zie [Een incrementele index van een gefaseerde website configureren](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Optioneel) Voer op de pagina [!DNL Definitions] een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Informatie over injecties {#concept_DA091920671948A0A893A26B3A2FAAE5}

Met [!DNL Injections] kunt u inhoud invoegen in uw webpagina&#39;s zonder dat u de pagina&#39;s zelf hoeft te bewerken.

U kunt inhoud toevoegen aan specifieke geïndexeerde velden, zoals &quot;doel&quot; of &quot;tekst&quot;, of geïndexeerde inhoud vervangen door nieuwe waarden. Als u bijvoorbeeld nieuwe inhoud hebt ingevoegd in het metatag &#39;target&#39; veld, wordt deze informatie op dezelfde manier behandeld als de inhoud van een pagina met harde code. U kunt de inhoud van elk vooraf gedefinieerd metatag-tagveld bewerken, ongeacht of uw sitepagina&#39;s de bijbehorende inhoud bevatten. U kunt bijvoorbeeld de inhoud van de volgende vooraf gedefinieerde veldnamen voor metatags bewerken:

* alt
* lichaam
* charset
* date
* desc
* toetsen
* taal
* target
* titel
* url

## Werken met testveldinjecties {#section_74939EA9E6EA4D2A92E8066B3B11CF92}

U kunt optioneel **[!UICONTROL Test]** op de [!DNL Staged Injections] pagina gebruiken. U voert een naam van een testveld in (bijvoorbeeld &quot;titel&quot; of &quot;tekst&quot;), de oorspronkelijke veldwaarde (bijvoorbeeld &quot;Startpagina&quot;) en een test-URL van uw website. De resulterende waarde wordt weergegeven ter referentie. De huidige waarden worden tijdens de test niet gewijzigd.

## Werken met veldinjectiedefinities {#section_C1BBF19DE8EF4A6F8CC3ED691F3953A9}

Injectiedefinities hebben de volgende vorm:

```
append|replace field [regexp] URL value
```

De `append|replace`, `field`, `URL`. en `value` items zijn verplicht. U voert één injectiedefinitie per regel in. Het volgende voorbeeld bevat zes verschillende injectiedefinities.

```
replace title  https://www.yoursite.com/company/contactus.html Adobe: Contact Us 
append body https://www.yoursite.com/products/* On Sale Now! 
append target https://www.yoursite.com/news/bob_white/ Regular Weekly Feature 
append target regexp https://www.yoursite.com/travel/mr_travel/.*\column.html$ Regular Weekly Feature 
replace charset https://www.yoursite.com/japanese/intro.txt shift-jis 
replace language https://www.yoursite.com/japanese/intro.txt ja_JP
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Injectiedefinitie </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> toevoegen|vervangen  </span> </p> </td> 
   <td colname="col2"> <p>Kies "toevoegen" om de waarde van de injectiedefinitie toe te voegen ("Adobe: Contact opnemen of Nu verkopen in de bovenstaande voorbeelden) aan de inhoud van bestaande velden. Kies "vervangen" om bestaande veldinhoud te overschrijven met de gedefinieerde waarde. Als een veld momenteel geen inhoud bevat, wordt de gedefinieerde waarde automatisch toegevoegd, ongeacht welke optie (toevoegen of vervangen) wordt gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> field  </span> </p> </td> 
   <td colname="col2"> <p>Een veldnaam is vereist. Hier volgen tien vooraf gedefinieerde veldnamen die u kunt gebruiken: </p> <p> 
     <ul id="ul_B9336FA53023474EAEE399116E7FC972"> 
      <li id="li_C621203DCD2B4875A54A1DD19F0B5B90"> <span class="codeph"> alt  </span> </li> 
      <li id="li_9217E6A037254BEDBB8D006B70D7670D"> <span class="codeph"> lichaam  </span> </li> 
      <li id="li_DCDC50F93F224F02897419B745E09399"> <span class="codeph"> charset  </span> </li> 
      <li id="li_D95668236B6547B99966668C82B302AB"> <span class="codeph"> date  </span> </li> 
      <li id="li_D2071681274345C3B97E9ADA6D223271"> <span class="codeph"> desc  </span> </li> 
      <li id="li_26683A9209454A438D811187FB929482"> <span class="codeph"> toetsen  </span> </li> 
      <li id="li_A5E19F81B872402CA62B5AB9497E030D"> <span class="codeph"> taal  </span> </li> 
      <li id="li_FD0B1CD9E6304B18B9D7F57E61015107"> <span class="codeph"> target  </span> </li> 
      <li id="li_400D7E3F3E9B47EFB2FF5C0D278DB573"> <span class="codeph"> titel  </span> </li> 
      <li id="li_449BCBEE4F64424BB69F780C10F5956C"> <span class="codeph"> url  </span> </li> 
     </ul> </p> <p>Elke veldnaam komt overeen met elementen op uw sitepagina's. Als u bijvoorbeeld de veldnaam <span class="codeph"> desc </span> opgeeft, kunt u de injectiedefinitiewaarde toevoegen aan het veld dat overeenkomt met de beschrijving van de Meta-tags op uw sitepagina's. </p> <p>Als er geen beschrijvende Meta-tag op uw pagina's voorkomt, maakt de gedefinieerde inhoud de tag voor u. De inhoud die in een <span class="codeph"> desc </span>-injectie wordt opgegeven, wordt op de resultatenpagina weergegeven, net als de inhoud van de harde metagegevens. </p> <p>U kunt ook meerdere definities met dezelfde veldnaam maken. Bijvoorbeeld, verondersteld u de volgende injecties hebt: </p> <p> <code> replace&nbsp; <b>title</b>&nbsp;https://www.mysite.com/&nbsp;Welcome&nbsp;to&nbsp;My&nbsp;Site </code> </p> <p> <code> replace&nbsp; <b>title</b>&nbsp;https://www.mysite.com/company/*.html&nbsp;My&nbsp;Site:&nbsp;Contact </code> </p> <p>Alle sitepagina's in het bovenstaande voorbeeld krijgen de titel "Welkom bij Mijn site". Pagina's in de map "/company/" worden geïnjecteerd met de nieuwe titel "Mijn site: Neem contact met ons op" dat de vorige vervangt. </p> <p>Injecties worden aangebracht in de volgorde waarin ze voorkomen in het tekstvak <span class="wintitle"> Definities veldinjectie </span>. Als hetzelfde veld ("titel" in dit voorbeeld) meerdere keren is gedefinieerd voor pagina's op dezelfde locatie, krijgt de latere definitie voorrang. </p> <p> <span class="codeph"> [regexp]  </span> - optioneel. Als u de optie <span class="codeph"> regexp </span> wilt gebruiken, wordt de gedefinieerde URL beschouwd als een reguliere expressie. </p> <p>Zie <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Reguliere expressies </a>. </p> <p>In de volgende definitie: </p> <p> <code> replace&nbsp;target&nbsp; <b>regexp&amp;nbsp;^.*/products/.*\.html$</b>&nbsp;Important&nbsp;information </code> </p> <p> "Belangrijke informatie" wordt in het veld "Doel" geïnjecteerd op alle pagina's die overeenkomen met de reguliere expressie <span class="codeph"> ^.*/products/.*\.html$ </span>. </p> <p>Daarom hebt u het volgende: </p> <p> <code> https://www.mydomain.com/products/page1.html 
      &nbsp;&nbsp;&nbsp;&nbsp;(Will&nbsp;receive&nbsp;"target"&nbsp;content) </code> </p> <p> <code> https://www.mydomain.com/product/oldstuff.html 
      &nbsp;&nbsp;&nbsp;&nbsp;(Will&nbsp;not&nbsp;receive&nbsp;"target"&nbsp;content) </code> </p> <p>In het volgende voorbeeld: </p> <p> <code> append&amp;nbsp;title&amp;nbsp;regexp&amp;nbsp;^.*\.pdf$&amp;nbsp;Millennium&amp;nbsp;Science </code> </p> <p>De injectie voegt "Millennium Science" toe aan de "title"-inhoud van alle pagina's die eindigen met de bestandsnaamextensie ".pdf". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> URL  </span> </p> </td> 
   <td colname="col2"> <p>Een URL is vereist en geeft aan welke documenten worden ingespoten. </p> <p>De URL is een van de volgende: </p> <p> 
     <ul id="ul_C5C74F6D5EA943B293742989EB822751"> 
      <li id="li_382392DB778D4E14BFFC96D35A861951"> Een volledig pad, zoals in https://www.mydomain.com/products.html </li> 
      <li id="li_EA2BD0FB66A44CD0844613316F6174D4"> Een gedeeltelijk pad, zoals in https://www.mydomain.com/products </li> 
      <li id="li_D5E0D6D897C8493ABBFC65517CD4A7DB"> Een URL die jokertekens gebruikt, zoals in https://www.mydomain.com/*.html </li> 
     </ul> </p> <p>De URL-waarde mag geen spatietekens bevatten. Als de optie <span class="codeph"> regexp </span> wordt gebruikt, wordt URL behandeld als een regelmatige uitdrukking. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value  </span> </p> </td> 
   <td colname="col2"> <p>Een waarde is vereist en wordt gebruikt om bestaande veldinhoud te vervangen of aan te vullen. U kunt meerdere waarden opgeven voor dezelfde veldnaam. Bijvoorbeeld: </p> <p>toevoegen <b>keys</b> https://www.mysite.com/travel/ <b>zomer</b>, <b>strand</b>, <b>zand</b> </p> <p>toevoegen <b>keys</b> https://www.mysite.com/travel/fare/*.html <b>goedkope tickets</b> </p> <p>In het bovenstaande voorbeeld worden de woorden "zomer, strand, zand" toegevoegd aan het veld "sleutels" op alle pagina's in de map "/reis/". De woorden "goedkope tickets" worden ook toegevoegd aan het veld "sleutels" op alle pagina's in de map "/reis/fare/". </p> </td> 
  </tr> 
 </tbody> 
</table>

Zie ook [Inhoudstypen selecteren om door te kruipen en index](../c-about-settings-menu/c-about-crawling-menu.md#task_CCAC5C67C8BF4AB7B79D34A1495D5EE8).

## Veld-injectiedefinities toevoegen {#task_E86566FA1FF74CF68115C0ADA05172AE}

Met [!DNL Injections] kunt u inhoud invoegen in uw webpagina&#39;s zonder dat u de pagina&#39;s zelf hoeft te bewerken.

U kunt optioneel **[!UICONTROL Test]** op de [!DNL Injections] pagina gebruiken. U voert een naam van een testveld in (bijvoorbeeld &quot;titel&quot; of &quot;tekst&quot;), de oorspronkelijke veldwaarde (bijvoorbeeld &quot;Startpagina&quot;) en een test-URL van uw website. De resulterende waarde wordt weergegeven ter referentie. De huidige waarden worden tijdens de test niet gewijzigd.

**Veldinjectiedefinities toevoegen**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Injections]**.
1. (Optioneel) Typ op de pagina [!DNL Injections] in het gebied [!DNL Test Field Injections] het testveld, de oorspronkelijke testwaarde en test-URL en klik vervolgens op **[!UICONTROL Test]**.
1. Voer in het veld [!DNL Field Injection Definitions] één injectiedefinitie per regel in.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Informatie over kenmerklader {#concept_9EF38E98811B42CDA41996432B9AD209}

Gebruik [!DNL Attribute Loader] om extra invoerbronnen te definiëren om gegevens die van een website zijn gekropen, te vergroten.

>[!NOTE]
>
>Als u Kenmerklader wilt gebruiken, moet deze mogelijk in uw account zijn ingeschakeld door uw accountvertegenwoordiger van de Adobe of door Adobe Support.

U kunt een invoerbron voor gegevensinvoer gebruiken om toegang te krijgen tot inhoud die is opgeslagen in een formulier dat afwijkt van wat normaal gesproken op een website wordt ontdekt. U doet dit gebruikend één van de beschikbare kruipmethodes. De gegevens uit deze bronnen kunnen dan in gegevens van gekropen inhoud worden geïnjecteerd.

Nadat u een definitie van de Lader van Attributen aan de [!DNL Staged Attribute Loader Definitions] pagina toevoegt, kunt u om het even welke configuratie het plaatsen behalve de waarden van de Naam en van het Type veranderen

Op de pagina [!DNL Attribute Loader] ziet u de volgende informatie:

* De naam van de gedefinieerde configuratie van kenmerklader die u hebt geconfigureerd en toegevoegd.
* Één van de volgende gegevensbrontypes voor elke schakelaar die u hebt toegevoegd:

   * **Tekst**  - Eenvoudige &quot;platte&quot; bestanden, komma&#39;s, tabs-afgebakende of andere consistent gescheiden indelingen.
   * **Feed**  - XML-feeds.

* Of de configuratie of niet voor volgende wordt toegelaten kruipt en het indexeren.
* Het adres van de gegevensbron.

Zie ook [Hoe het proces van de kenmerkinjectie voor Tekst en Diervoed werkt..](../c-about-settings-menu/c-about-metadata-menu.md#section_E059A33D61EE4DB0972A37B8A35E9E16)

Zie ook [Informatie over het configureren van meerdere kenmerklezers](../c-about-settings-menu/c-about-metadata-menu.md#section_4CC49C74EF294608A184E233F215ADFF)

Zie ook [Informatie over het gebruik van Voorvertoning wanneer u een kenmerk toevoegt...](../c-about-settings-menu/c-about-metadata-menu.md#section_E9CAB000A94C4D9189786C1EDB1CDB46)

## Hoe het proces van de attributeninjectie voor de configuraties van de Tekst en van het Diervoer in de Loader van Attributen {#section_E059A33D61EE4DB0972A37B8A35E9E16} werkt

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Stap </p> </th> 
   <th colname="col2" class="entry"> <p>Proces </p> </th> 
   <th colname="col3" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>1 </p> </td> 
   <td colname="col2"> <p>Download de gegevensbron. </p> </td> 
   <td colname="col3"> <p>Voor configuraties met tekst en feed is het een eenvoudige bestandsdownload. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>Verdeel de gedownloade gegevensbron in afzonderlijke pseudo-documenten. </p> </td> 
   <td colname="col3"> <p>Voor <span class="uicontrol"> Tekst </span>, beantwoordt elke nieuwe lijn-afgebakende lijn van tekst aan een individueel document, en wordt ontleed gebruikend het gespecificeerde afbakening, zoals een komma of een lusje. </p> <p>Voor <span class="uicontrol"> Feed </span> worden de gegevens van elk document geëxtraheerd met behulp van een reguliere-expressiepatroon in de volgende vorm: </p> <p> <code class="syntax js"> &lt;${Itemtag}&gt;(.*?)&lt;/${Itemtag}&gt; </code> </p> <p>Met <span class="uicontrol"> Map </span> op de pagina <span class="wintitle"> Kenmerklader toevoegen </span> maakt u een kopie van de gegevens die in de cache zijn opgeslagen en maakt u vervolgens een lijst met koppelingen voor de crawler. De gegevens worden opgeslagen in een lokaal geheime voorgeheugen en met de gevormde gebieden bevolkt. </p> <p>De geparseerde gegevens worden naar de lokale cache geschreven. </p> <p>Deze cache wordt later gelezen om de eenvoudige HTML-documenten te maken die de crawler nodig heeft. Bijvoorbeeld: </p> <p> <code class="syntax html"> &lt;html&gt;&lt;head&gt; 
      &lt;title&gt;{title}&lt;/title&gt; 
      &lt;meta&nbsp;name="{field}"&nbsp;content="{data}"&nbsp;/&gt; 
      ... 
      &lt;/head&gt;&lt;body&gt; 
      {body} 
      &lt;/body&gt;&lt;/html&gt; </code> </p> <p>Het <span class="codeph"> &lt;title&gt; </span> element wordt slechts geproduceerd wanneer een afbeelding aan het de meta-gegevensgebied van de Titel bestaat. Op dezelfde manier wordt het <span class="codeph"> &lt;body&gt; </span> element slechts geproduceerd wanneer een afbeelding aan het de meta-gegevensgebied van het Lichaam bestaat. </p> <p> <b>Belangrijk</b>: De toewijzing van waarden aan de vooraf gedefinieerde metatag voor URL wordt niet ondersteund. </p> <p>Voor alle andere toewijzingen worden <span class="codeph"> &lt;meta&gt; </span>-tags gegenereerd voor elk veld dat gegevens bevat die in het oorspronkelijke document zijn gevonden. </p> <p>De velden voor elk document worden toegevoegd aan de cache. Voor elk document dat naar het geheime voorgeheugen wordt geschreven, wordt een verbinding ook geproduceerd zoals in de volgende voorbeelden: </p> <p> <code class="syntax html"> &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      .... </code> </p> <p>Voor de toewijzing van de configuratie moet één veld zijn geïdentificeerd als primaire sleutel. Deze toewijzing vormt de sleutel die wordt gebruikt wanneer de gegevens van het geheime voorgeheugen worden gehaald. </p> <p>De schuifregelaar herkent de URL <span class="codeph">-index: </span> schemaprefix, die tot de plaatselijk caching gegevens kan dan toegang hebben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>1 </p> </td> 
   <td colname="col2"> <p>De documentset in de cache horizontaal schuiven. </p> </td> 
   <td colname="col3"> <p>De <span class="codeph">-index: </span> de verbindingen worden toegevoegd aan de kruipende lijst, en in de normale kruipende opeenvolging verwerkt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>Verwerk elk document. </p> </td> 
   <td colname="col3"> <p>De sleutelwaarde van elke verbinding beantwoordt aan een ingang in het geheime voorgeheugen, zo het kruipen van elke verbinding resulteert in de gegevens van dat document die van het geheime voorgeheugen worden gehaald. Vervolgens wordt de afbeelding 'geassembleerd' in een HTML-afbeelding die wordt verwerkt en aan de index wordt toegevoegd. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Informatie over het configureren van meerdere kenmerklezers {#section_4CC49C74EF294608A184E233F215ADFF}

U kunt meerdere configuraties van kenmerklader definiëren voor elke account.

Wanneer u een kenmerklader toevoegt, kunt u desgewenst de functie **[!UICONTROL Setup Maps]** gebruiken om een voorbeeld van uw gegevensbron te downloaden. De gegevens worden op geschiktheid onderzocht.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Type kenmerklader </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Tekst </p> </td> 
   <td colname="col2"> <p>Hiermee bepaalt u de waarde van het scheidingsteken door eerst tabs en vervolgens verticale balken ( <span class="codeph">) te proberen | </span>) en ten slotte komma's ( <span class="codeph"> , </span>). Als u reeds een afbakeningswaarde alvorens u <span class="uicontrol"> de Kaarten van de Opstelling </span> klikte, wordt die waarde gebruikt. </p> <p>Het best-geschikte schema resulteert in de gebieden van de Kaart die met gokken bij de aangewezen waarden van de Markering en van het Gebied worden ingevuld. Bovendien wordt een sampling van de geparseerde gegevens weergegeven. Selecteer <span class="uicontrol"> Koppen in eerste rij </span> als u weet dat het bestand een koptekstrij bevat. De opstellingsfunctie gebruikt deze informatie om de resulterende kaartingangen beter te identificeren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Feed </p> </td> 
   <td colname="col2"> <p>Downloadt de gegevensbron en voert het eenvoudige ontleden van XML uit. </p> <p>De resulterende XPath-id's worden weergegeven in de tagrijen van de tabel Kaart en vergelijkbare waarden in velden. Deze rijen identificeren slechts de beschikbare gegevens, en produceren niet de meer gecompliceerde definities van XPath. Het is echter nog steeds handig omdat het de XML-gegevens beschrijft en itemtag identificeert. </p> <p> <p>Opmerking:  De functie van Kaarten van de Opstelling downloadt de volledige bron van XML om zijn analyse uit te voeren. Als het bestand groot is, kan deze bewerking time-out veroorzaken. </p> </p> <p>Wanneer succesvol, identificeert deze functie alle mogelijke punten XPath, die vele niet wenselijk zijn te gebruiken. Zorg ervoor dat u de resulterende definities van de Kaart onderzoekt en degenen verwijdert die u niet nodig hebt of wilt. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>De functie Kaarten instellen werkt mogelijk niet voor grote XML-gegevenssets omdat de bestandsparser het gehele bestand in het geheugen probeert te lezen. Dit heeft tot gevolg dat u een toestand van onvoldoende geheugen kunt ervaren. Wanneer hetzelfde document echter wordt verwerkt op het moment van indexering, wordt het niet in het geheugen gelezen. In plaats daarvan worden grote documenten onderweg verwerkt en niet helemaal in het geheugen gelezen.

## Informatie over het gebruik van Voorvertoning wanneer u een kenmerklader {#section_E9CAB000A94C4D9189786C1EDB1CDB46} toevoegt

Kenmerklader-gegevens worden vóór een indexbewerking geladen.

Op het moment dat u een kenmerklader toevoegt, kunt u optioneel de functie **[!UICONTROL Preview]** gebruiken om de gegevens te valideren, alsof u deze opslaat. Het stelt een test tegen de configuratie in werking, maar zonder de configuratie aan de rekening op te slaan. De test heeft toegang tot de geconfigureerde gegevensbron. De downloadcache wordt echter naar een tijdelijke locatie geschreven. er is geen conflict met de hoofdcachemap die door de indexerende crawler wordt gebruikt.

De voorproef verwerkt slechts een gebrek van vijf documenten zoals die door **worden gecontroleerd Acct:IndexConnector-Voorproef-Max-Documents**. De voorvertoonde documenten worden getoond in bronvorm, aangezien zij aan de indexerende kruipper worden voorgesteld. De vertoning is gelijkaardig aan een &quot;Bron van de Mening&quot;eigenschap in browser van het Web. U kunt met standaardnavigatiekoppelingen door de documenten in de voorvertoningsset navigeren.

Voorvertoning ondersteunt geen XML-configuraties omdat dergelijke documenten rechtstreeks worden verwerkt en niet naar de cache worden gedownload.

## Definitie {#task_A735E5EF763343A9B675E1A3B09AFDBC} van kenmerklader toevoegen

Elke configuratie van de Lader van Attributen bepaalt een gegevensbron en afbeeldingen om de gegevenspunten te relateren die voor die bron aan meta-gegevensgebieden in de index worden bepaald.

>[!NOTE]
>
>Als u Kenmerklader wilt gebruiken, moet deze mogelijk in uw account zijn ingeschakeld door uw accountvertegenwoordiger van de Adobe of door Adobe Support.

Voordat de effecten van de nieuwe en ingeschakelde definitie zichtbaar zijn voor klanten, moet u de index van uw site opnieuw samenstellen.

**Een definitie van een kenmerklader toevoegen**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Klik op [!DNL Stage Attribute Loader Definitions] op de pagina.**[!UICONTROL Add New Attribute Loader]**
1. Stel op de pagina [!DNL Attribute Loader Add] de gewenste configuratieopties in. Welke opties beschikbaar zijn, is afhankelijk van de optie **[!UICONTROL Type]** die u hebt geselecteerd.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Naam </p> </td> 
      <td colname="col2"> <p>De unieke naam van de configuratie van kenmerklader. U kunt alfanumerieke tekens gebruiken. De tekens "_" en "-" zijn ook toegestaan. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Type </p> </td> 
      <td colname="col2"> <p>De bron van uw gegevens. Het gegevensbrontype dat u selecteert, heeft invloed op de resulterende opties die beschikbaar zijn op de pagina <span class="wintitle"> Kenmerklader toevoegen </span>. U kunt uit het volgende kiezen: </p> <p> 
      <ul id="ul_1ADC3DFBC929467385F7465BE8E13635"> 
      <li id="li_64FCD749F55442BAB316BD474128D4F9"> <span class="uicontrol"> Tekst  </span> <p>Eenvoudige, platte tekstbestanden, komma-afgebakende, tabgescheiden of andere consistent gescheiden indelingen. Elke nieuwe regel tekst die door een nieuwe regel wordt gescheiden, komt overeen met een afzonderlijk document en wordt met het opgegeven scheidingsteken geparseerd. </p> <p>U kunt elke waarde of kolom toewijzen aan een metagegevensveld waarnaar wordt verwezen door het kolomnummer, te beginnen bij 1 (één). </p> </li> 
      <li id="li_2A4F16CE6DCE4114B7F8E4FE156252BB"> <span class="uicontrol"> Feed  </span> <p>Downloadt een primair XML-document dat meerdere "rijen" met informatie bevat. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>Type gegevensbron: Tekst</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ingeschakeld </p> </td> 
      <td colname="col2"> <p>Zet de configuratie "aan"voor gebruik. U kunt de configuratie ook uitschakelen om te voorkomen dat deze wordt gebruikt. </p> <p> <b>Opmerking</b>: Uitgeschakelde configuraties van kenmerklader worden genegeerd. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Adres van gastheer </p> </td> 
      <td colname="col2"> <p>Hier geeft u het adres op van de serverhost waarop de gegevens zich bevinden. </p> <p>U kunt desgewenst een volledig URI-pad (Uniform Resource Identifier) opgeven naar het gegevensbrondocument, zoals in de volgende voorbeelden: </p> <p> <code otherprops="syntax html"> https://www.somewhere.com/some_path/some_file.tsv </code> </p> <p>of </p> <p> <code class="syntax html"> ftp://user:password@ftpserver.somewhere.com/some_path/some_file.csv </code> </p> <p>URI wordt verdeeld in de aangewezen ingangen voor de gebieden van het Adres van de Gastheer, van de Weg van het Dossier, van het Protocol, en, naar keuze, Gebruikersnaam, en van het Wachtwoord </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Bestandspad </p> </td> 
      <td colname="col2"> <p>Hiermee geeft u het pad op naar het eenvoudige, platte tekstbestand, een kommagescheiden bestand met tabs of een ander op consistente wijze gescheiden opmaakbestand. </p> <p>Het pad is relatief ten opzichte van de hoofdmap van het hostadres. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocol </p> </td> 
      <td colname="col2"> <p>Hiermee geeft u het protocol op dat wordt gebruikt voor toegang tot het bestand. U kunt uit het volgende kiezen: </p> <p> 
      <ul id="ul_F6BC10FD51CA4A1D855B2B3212838A9C"> 
      <li id="li_79FB7DC65E774ABBB23E57BF98AD9738"> HTTP <p>Indien nodig kunt u de juiste verificatiegegevens invoeren om toegang te krijgen tot de HTTP-server. </p> </li> 
      <li id="li_BAA9AD5E4B014E09B3A66C94022B7225"> HTTPS <p>Indien nodig kunt u de juiste verificatiegegevens invoeren om toegang te krijgen tot de HTTPS-server. </p> </li> 
      <li id="li_E716ABB169DD408BA91F1CA27F445A16"> FTP <p>U moet de juiste verificatiereferenties invoeren om toegang te krijgen tot de FTP-server. </p> </li> 
      <li id="li_FD7143019C5244C3B8A5B1B5AA84859A"> SFTP <p>U moet de juiste verificatiereferenties invoeren om toegang te krijgen tot de SFTP-server. </p> </li> 
      <li id="li_38E0036C1365419F9D00083CACA34AFB"> Bestand </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Time-out </p> </td> 
      <td colname="col2"> <p>Hiermee wordt de time-out in seconden opgegeven voor FTP-, SFTP-, HTTP- of HTTPS-verbindingen. Deze waarde moet liggen tussen 30 en 300. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Opnieuw </p> </td> 
      <td colname="col2"> <p>Hiermee wordt het maximale aantal pogingen opgegeven voor mislukte FTP-, SFTP-, HTTP- of HTTPS-verbindingen. Deze waarde moet tussen 0 en 10 liggen. </p> <p>De waarde nul (0) voorkomt pogingen opnieuw uit te voeren. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Codering </p> </td> 
      <td colname="col2"> <p>Geeft het tekencoderingssysteem aan dat wordt gebruikt in het opgegeven gegevensbronbestand. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Scheidingsteken </p> </td> 
      <td colname="col2"> <p>Hiermee geeft u het teken op dat u wilt gebruiken om elk veld in het opgegeven gegevensbronbestand af te bakenen. </p> <p>Het komma-teken ( <span class="codeph"> , </span>) is een voorbeeld van een scheidingsteken. De komma fungeert als een veldscheidingsteken waarmee gegevensvelden in het opgegeven gegevensbronbestand kunnen worden gescheiden. </p> <p><span class="uicontrol"> Tab selecteren? </span> Hiermee gebruikt u het teken voor de horizontale tab als scheidingsteken. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Kopteksten in eerste rij </p> </td> 
      <td colname="col2"> <p>Geeft aan dat de eerste rij in het gegevensbronbestand alleen koptekstinformatie bevat, niet gegevens. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Verhaaldagen </p> </td> 
      <td colname="col2"> <p>Hiermee stelt u het minimale interval in tussen downloads van kenmerkLoader-gegevens. Indexgetriggerde downloads die plaatsvinden binnen het gedownloade vernieuwingsfrequentie-interval worden genegeerd. Wanneer u deze waarde instelt op de standaardwaarde 1, worden de gegevens van de kenmerklader niet meer dan één keer gedownload binnen een periode van 24 uur. Alle indexen van het Onderzoek die binnen de download voorkomen verfrissen frequentieinterval gebruik de laatste gegevensreeks die werd gedownload. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Kaart </p> </td> 
      <td colname="col2"> <p>Hiermee geeft u kolomtoewijzingen aan metagegevens op met behulp van kolomnummers. </p> <p> 
      <ul id="ul_981AE2C6D30443BDBFC6575D413732A2"> 
      <li id="li_A42CB9DFFF8C45A7BAC2D471FE96CEBE"> <span class="uicontrol"> Kolom  </span> <p> Hiermee geeft u een kolomnummer op, waarbij de eerste kolom 1 (één) is. Als u nieuwe kaartrijen wilt toevoegen voor elke kolom, klikt u onder <span class="wintitle"> Handeling </span> op <span class="uicontrol"> + </span>. </p> <p>U hoeft niet naar elke kolom in de gegevensbron te verwijzen. In plaats daarvan kunt u ervoor kiezen waarden over te slaan. </p> </li> 
      <li id="li_26E8C9554A5D4BC5A5073D6385E3626F"> <span class="uicontrol"> Veld  </span> <p>Definieert de waarde van het naamkenmerk die wordt gebruikt voor elke gegenereerde &lt;meta&gt;-tag. </p> </li> 
      <li id="li_5DFA514B7F9549B98D6CBC095A66033C"> <span class="uicontrol"> Metagegevens?  </span> <p>Hiermee wordt <span class="uicontrol"> Veld </span> omgezet in een vervolgkeuzelijst waaruit u gedefinieerde metagegevensvelden voor de huidige account kunt selecteren. </p> <p>De waarde <span class="uicontrol"> Veld </span> kan desgewenst een ongedefinieerd metagegevensveld zijn. Een niet-gedefinieerd metagegevensveld is soms handig om inhoud te maken die wordt gebruikt door een <span class="wintitle">-script </span> filteren. </p> <p>Zie <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> Scripts filteren </a>. </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892C95"> <span class="uicontrol"> Primaire sleutel?  </span> <p>Er wordt slechts één veld geïdentificeerd als primaire sleutel. Dit veld wordt gebruikt als de "buitenlandse sleutel" die overeenkomt met de kenmerkladingsgegevens en het corresponderende document in de index. </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892D96"> <span class="uicontrol"> HTML verwijderen?  </span> <p>Als deze optie is ingeschakeld, worden alle HTML-tags in de gegevens van dit veld verwijderd. </p> </li> 
      <li id="li_359D2902859B4C5BADB0BA26F0BA4DC0"> <span class="uicontrol"> Handeling  </span> <p>Hiermee kunt u rijen toevoegen aan de kaart of rijen verwijderen van de kaart. De volgorde van de rijen is niet belangrijk. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>Type gegevensbron: Feed</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ingeschakeld </p> </td> 
      <td colname="col2"> <p>Zet de configuratie "aan"voor gebruik. U kunt de configuratie ook uitschakelen om te voorkomen dat deze wordt gebruikt. </p> <p> <b>Opmerking</b>: Uitgeschakelde configuraties van kenmerklader worden genegeerd. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Adres van gastheer </p> </td> 
      <td colname="col2"> <p>Hier geeft u het adres op van de serverhost waarop de gegevens zich bevinden. </p> <p>U kunt desgewenst een volledig URI-pad (Uniform Resource Identifier) opgeven naar het gegevensbrondocument, zoals in de volgende voorbeelden: </p> <p> <code class="syntax html"> https://www.somewhere.com/some_path/some_file.tsv </code> </p> <p>of </p> <p> <code class="syntax html"> ftp://user:password@ftpserver.somewhere.com/some_path/some_file.csv </code> </p> <p>URI wordt verdeeld in de aangewezen ingangen voor het Adres van de Gastheer, de Weg van het Dossier, het Protocol, en, naar keuze, de gebieden van de Gebruikersnaam, en van het Wachtwoord. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Bestandspad </p> </td> 
      <td colname="col2"> <p>Hiermee geeft u het pad op naar het primaire XML-document dat meerdere rijen met informatie bevat. </p> <p>Het pad is relatief ten opzichte van de hoofdmap van het hostadres. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocol </p> </td> 
      <td colname="col2"> <p>Hiermee geeft u het protocol op dat wordt gebruikt voor toegang tot het bestand. U kunt uit het volgende kiezen: </p> <p> 
      <ul id="ul_976A34FD14A841F2B610C1C0CCBB82B9"> 
      <li id="li_05BBA0F670F14431A89AE4178F1A6F94"> HTTP <p>Indien nodig kunt u de juiste verificatiegegevens invoeren om toegang te krijgen tot de HTTP-server. </p> </li> 
      <li id="li_100446691F304572B8FC3F083F86A2CB"> HTTPS <p>Indien nodig kunt u de juiste verificatiegegevens invoeren om toegang te krijgen tot de HTTPS-server. </p> </li> 
      <li id="li_027088A8E30444DAA8CCCC5B0BAA74C1"> FTP <p>U moet de juiste verificatiereferenties invoeren om toegang te krijgen tot de FTP-server. </p> </li> 
      <li id="li_DCEF9D5C99354990B03E29083C2ED8DC"> SFTP <p>U moet de juiste verificatiereferenties invoeren om toegang te krijgen tot de SFTP-server. </p> </li> 
      <li id="li_44E34FF2AB0D429EB3408106E6FCF780"> Bestand </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Itemtag </p> </td> 
      <td colname="col2"> <p>Identificeert het element van XML dat u kunt gebruiken om individuele lijnen van XML in het gegevensbrondossier te identificeren dat u specificeerde. </p> <p>In het volgende fragment Feed van een Adobe XML-document is de waarde ItemTag bijvoorbeeld <span class="codeph"> record </span>: </p> <p> <code class="syntax xml"> &lt;?xml&nbsp;version="1.0"&nbsp;encoding="utf-8"?&gt; 
        &lt;!DOCTYPE&nbsp;gsafeed&nbsp;PUBLIC&nbsp;"-//Google//DTD&nbsp;GSA&nbsp;Feeds//EN"&nbsp;""&gt; 
        &lt;gsafeed&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;header&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;datasource&gt;marketplace&lt;/datasource&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;feedtype&gt;incremental&lt;/feedtype&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/header&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;group&nbsp;action="add"&gt; 
        &lt;record&nbsp;url=https://www.adobe.com/cfusion/marketplace_gsa/ 
        index.cfm?event=marketplace.home&amp;amp;marketplaceid=1&nbsp;action="add"&nbsp;mimetype="text/html"displayurl="https://www.adobe.com/cfusion/marketplace/index.cfm?event=marketplace.home&amp;amp;marketplaceid=1"&gt; 
        &lt;metadata&gt; 
        &lt;meta&nbsp;name="mp_mkt"&nbsp;content="1"/&gt; 
        &lt;meta&nbsp;name="mp_logo"&nbsp;content="/images/marketplace/ 
        dbreferenced/marketplaceicons/icn_air.png"/&gt; 
        &lt;meta&nbsp;name="title"&nbsp;content="Adobe&nbsp;AIR&nbsp;Marketplace"/&gt; 
        &lt;meta&nbsp;name="description"&nbsp;content="Discover&nbsp;new&nbsp;applications&nbsp;..."/&gt; 
        &lt;/metadata&gt; 
        &lt;content&gt;&lt;![CDATA[&lt;html&gt;&lt;head&gt;&lt;title&gt;Adobe&nbsp;AIR&nbsp;Marketplace&lt;/title&gt;&lt;/head&gt;&lt;body&gt;Discover&nbsp;new&nbsp;applications&nbsp;...&lt;/body&gt;&lt;/html&gt;]]&gt;&lt;/cntent&gt; 
        &lt;/record&gt; 
        &lt;record&nbsp;url=https://www.adobe.com/cfusion/marketplace_gsa/ 
        index.cfm?event=marketplace.home&amp;amp;marketplaceid=2&nbsp;action="add"&nbsp;mimetype="text/html"&nbsp;displayurl="https://www.adobe.com/cfusion/ 
        marketplace/index.cfm?event=marketplace.home&amp;amp;marketplaceid=2"&gt; 
        &lt;metadata&gt; 
        &lt;meta&nbsp;name="mp_mkt"&nbsp;content="2"/&gt; 
        &lt;meta&nbsp;name="mp_logo"&nbsp;content="/images/marketplace/ 
        dbreferenced/marketplaceicons/icn_photoshop.png"/&gt; 
        &lt;meta&nbsp;name="title"&nbsp;content="Adobe&nbsp;Photoshop&nbsp;Marketplace"/&gt; 
        &lt;meta&nbsp;name="description"&nbsp;content="Extend&nbsp;your&nbsp;creative&nbsp;possibilities&nbsp;..."/&gt; 
        &lt;/metadata&gt; 
        &lt;content&gt;&lt;![CDATA[&lt;html&gt;&lt;head&gt;&lt;title&gt;Adobe&nbsp;Photoshop&nbsp;Marketplace&lt;/title&gt;&lt;/head&gt;&lt;body&gt;Extend&nbsp;your&nbsp;creative&nbsp;possibilities&nbsp;...&lt;/body&gt;&lt;/html&gt;]]&gt;/content&gt; 
        &lt;/record&gt; 
        ... 
        &lt;record&gt; 
        ... 
        &lt;/record&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/group&gt; 
        &lt;/gsafeed&gt; 
        </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Veldnaam kruisverwijzing </p> </td> 
      <td colname="col2"> <p>Hiermee wordt een metagegevensveld opgegeven waarvan de waarden worden gebruikt als 'opzoeksleutels' in de gegevens van de configuratie van kenmerklader. Als er geen waarde is geselecteerd (<b>—None—</b>), zijn de gegevens van deze configuratie niet beschikbaar voor gebruik in Beoordelingsberekeningen (<b>Regels</b> &gt; <b>Rangschikkingsregels</b> &gt; <b>Regels bewerken</b>). Als u een waarde selecteert, worden de waarden van dit veld gebruikt om te verwijzen naar de zoekfunctie van de site of om documenten te verhandelen met de gegevens van deze configuratie. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Verhaaldagen </p> </td> 
      <td colname="col2"> <p>Hiermee stelt u het minimale interval in tussen downloads van kenmerkLoader-gegevens. Indexgetriggerde downloads die plaatsvinden binnen het gedownloade vernieuwingsfrequentie-interval worden genegeerd. Wanneer u deze waarde instelt op de standaardwaarde 1, worden de gegevens van de kenmerklader niet meer dan één keer gedownload binnen een periode van 24 uur. Alle indexen van het Onderzoek die binnen de download voorkomen verfrissen frequentieinterval gebruik de laatste gegevensreeks die werd gedownload. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Kaart </p> </td> 
      <td colname="col2"> <p>Hiermee kunt u XML-element-aan-metagegevenstoewijzingen opgeven met XPath-expressies. </p> <p> 
      <ul id="ul_604108C0277C4892AE8A40CA39889ABD"> 
      <li id="li_0AF92270AE9F4BA8B2C7EE41FABC0F34"> <span class="uicontrol"> Tag  </span> <p>Hiermee wordt een XPath-representatie van de geparseerde XML-gegevens opgegeven. Met behulp van het voorbeeld Adobe XML-document hierboven, onder de optie Item-tag, kan deze worden toegewezen met behulp van de volgende syntaxis: </p> <p> <code class="syntax xml"> /record/@displayurl&nbsp;-&gt;&nbsp;page-url 
        /record/metadata/meta[@name='title']/@content&nbsp;-&gt;&nbsp;title 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;desc 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;body </code> </p> <p>De bovenstaande syntaxis wordt als volgt vertaald: </p> <p> 
        <ul id="ul_6400EBD08D424EADA1612FE4F7EFB640"> 
        <li id="li_9958F9B40D42434195597DBA9F2AF28F"> <code class="syntax xml"> /record/@displayurl&amp;nbsp;-&gt;&amp;nbsp;page-url </code> <p>Het <span class="codeph"> displayurl </span>-kenmerk van het <span class="codeph">-element record </span> verwijst naar het metagegevensveld <span class="codeph"> page-url </span>. </p> </li> 
        <li id="li_759013EA02CD48BE971A55B0A6A11424"> <code class="syntax xml"> /record/metadata/meta[@name='title']/@content&amp;nbsp;-&gt;&amp;nbsp;title </code> <p>Het <span class="codeph">-kenmerk content </span> van elk <span class="codeph">-meta </span>-element dat zich in een <span class="codeph">-metagegevenselement </span> bevindt, dat zich in een <span class="codeph">-record </span>-element bevindt, waarvan het naamkenmerk <span class="codeph">-titel </span> is, wordt toegewezen aan het metagegevensveld <span class="codeph">.</span> </p> </li> 
        <li id="li_E741CA59197D462EB2946EDE874AFDC8"> <code class="syntax xml"> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;desc </code> <p>Het <span class="codeph">-kenmerk content </span> van elk <span class="codeph">-meta </span>-element dat zich in een <span class="codeph">-metagegevenselement </span> bevindt, dat zich in het <span class="codeph">-element </span>-record bevindt, waarvan het naamkenmerk <span class="codeph">-beschrijving </span> is, wordt toegewezen aan het metagegevensveld <span class="codeph"> desc 1/&gt;.</span> </p> </li> 
        <li id="li_E35EAE3D284D46D485D9064D7BB6AB13"> <code class="syntax xml"> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;body </code> <p>Het <span class="codeph">-kenmerk content </span> van elk <span class="codeph">-meta </span>-element dat zich in een <span class="codeph">-metagegevenselement </span> bevindt, dat zich in het <span class="codeph">-element </span>-record bevindt, waarvan het naamkenmerk <span class="codeph">-beschrijving </span> is, wordt toegewezen aan het metagegevensveld <span class="codeph">.</span> </p> </li> 
        </ul> </p> <p>XPath is een relatief gecompliceerde notatie. Meer informatie is beschikbaar op de volgende locatie: </p> <p>Zie <a href="https://www.w3schools.com/xpath/" scope="external" format="html"> https://www.w3schools.com/xpath/ </a> </p> </li> 
      <li id="li_8147075D7ACD4811A7ED335F23FE62A6"> <span class="uicontrol"> Veld  </span> <p>Definieert de waarde van het naamkenmerk die wordt gebruikt voor elke gegenereerde <span class="codeph"> &lt;meta&gt; </span>-tag. </p> </li> 
      <li id="li_2380199D63BF425A919606D8232FA6E2"> <span class="uicontrol"> Metagegevens?  </span> <p>Hiermee wordt <span class="uicontrol"> Veld </span> omgezet in een vervolgkeuzelijst waaruit u gedefinieerde metagegevensvelden voor de huidige account kunt selecteren. </p> <p>De waarde <span class="uicontrol"> Veld </span> kan desgewenst een ongedefinieerd metagegevensveld zijn. Een niet-gedefinieerd metagegevensveld is soms handig om inhoud te maken die wordt gebruikt door <span class="wintitle"> Script filteren </span>. </p> <p>Zie <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> Scripts filteren </a>. </p> <p>Wanneer de Lader van Attributen de documenten van XML met veelvoudige klappen op om het even welk kaartgebied verwerkt, worden de veelvoudige waarden samengevoegd in één enkele waarde in het resulterende caching document. Deze waarden worden standaard gecombineerd met een komma-scheidingsteken. Stel echter dat de corresponderende <span class="wintitle">-veldwaarde </span> een gedefinieerd metagegevensveld is. Bovendien heeft dat gebied <span class="wintitle"> Lijsten van gewenste personen </span> plaatste attribuut. In dit geval wordt de waarde van Lijstscheidingstekens van het veld (het eerste gedefinieerde scheidingsteken) gebruikt bij de samenvoeging. </p> </li> 
      <li id="li_DEA24003E97E406DA2510C43CCFDC70E"> <span class="uicontrol"> Primaire sleutel?  </span> <p>Er wordt slechts één veld geïdentificeerd als primaire sleutel. Dit veld wordt gebruikt als de "buitenlandse sleutel" die overeenkomt met de kenmerkladingsgegevens en het corresponderende document in de index. </p> </li> 
      <li id="li_80D6AF130FCE40AC972FE4B605B86BF6"> <span class="uicontrol"> HTML verwijderen?  </span> <p>Als deze optie is ingeschakeld, worden alle HTML-tags in de gegevens van dit veld verwijderd. </p> </li> 
      <li id="li_D40E2F9AD8AD49FC9AC4B8C75BA31E28"> <span class="uicontrol"> Handeling  </span> <p>Hiermee kunt u rijen toevoegen aan de kaart of rijen verwijderen van de kaart. De volgorde van de rijen is niet belangrijk. </p> </li> 
      </ul> </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. (Optioneel) Klik op **[!UICONTROL Setup Maps]** om een voorbeeld van uw gegevensbron te downloaden. De gegevens worden op geschiktheid onderzocht.
1. Klik **[!UICONTROL Add]** om de configuratie aan [!DNL Attribute Loader Definitions] pagina toe te voegen.
1. Klik op [!DNL Attribute Loader Definitions] op de pagina.**[!UICONTROL rebuild your staged site index]**
1. (Optioneel) Voer op de pagina [!DNL Attribute Loader Definitions] een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Definitie {#task_AA2D1B2BCAFA44A6A0C59A0318274E80} van kenmerklader bewerken

U kunt een bestaande kenmerklader bewerken die u hebt gedefinieerd.

>[!NOTE]
>
>Als u Kenmerklader wilt gebruiken, moet deze mogelijk in uw account zijn ingeschakeld door uw accountvertegenwoordiger van de Adobe of door Adobe Support.

Niet alle opties voor kenmerklader zijn beschikbaar om te worden gewijzigd, zoals de naam of het type kenmerklader in de vervolgkeuzelijst [!DNL Type].

**De definitie van een kenmerklader bewerken**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Klik op de pagina [!DNL Attribute Loader] onder de kolomkop [!DNL Actions] op **[!UICONTROL Edit]** voor de definitienaam van een kenmerklader waarvan u de instellingen wilt wijzigen.
1. Stel op de pagina [!DNL Attribute Loader Edit] de gewenste opties in.

   Zie de optietabel onder [Definitie van kenmerklader toevoegen](../c-about-settings-menu/c-about-metadata-menu.md#task_A735E5EF763343A9B675E1A3B09AFDBC).
1. Klik op **[!UICONTROL Save Changes]**.
1. (Optioneel) Klik op [!DNL Attribute Loader Definitions] op de pagina.**[!UICONTROL rebuild your staged site index]**
1. (Optioneel) Voer op de pagina [!DNL Attribute Loader Definitions] een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## {#task_9B40D5ECFC81411E9480F62A0FD5F2E0} een kenmerklader kopiëren

U kunt een bestaande definitie van kenmerklader kopiëren en gebruiken als basis voor een nieuwe kenmerklader die u wilt maken.

>[!NOTE]
>
>Als u Kenmerklader wilt gebruiken, moet deze mogelijk in uw account zijn ingeschakeld door uw accountvertegenwoordiger van de Adobe of door Adobe Support.

Bij het kopiëren van een definitie van een kenmerklader wordt de gekopieerde definitie standaard uitgeschakeld. Als u de definitie wilt inschakelen of &quot;inschakelen&quot;, moet u deze bewerken op de pagina [!DNL Attribute Loader Edit] en **[!UICONTROL Enable]** selecteren.

Zie [Definitie van kenmerklader bewerken](../c-about-settings-menu/c-about-metadata-menu.md#task_AA2D1B2BCAFA44A6A0C59A0318274E80).

**Een kenmerklader-definitie kopiëren**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Klik op de pagina [!DNL Attribute Loader] onder de kolomkop [!DNL Actions] op **[!UICONTROL Copy]** voor de definitienaam van een kenmerklader waarvan u de instellingen wilt dupliceren.
1. Voer op de pagina [!DNL Attribute Loader Copy] de nieuwe naam van de definitie in.
1. Klik op **[!UICONTROL Copy]**.
1. (Optioneel) Voer op de pagina [!DNL Attribute Loader Definitions] een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## De naam wijzigen van een kenmerkLoader-definitie {#task_58D5DFD7EBC04111BCB91118E4440DB4}

U kunt de naam wijzigen van een bestaande definitie van kenmerklader.

>[!NOTE]
>
>Als u Kenmerklader wilt gebruiken, moet deze mogelijk in uw account zijn ingeschakeld door uw accountvertegenwoordiger van de Adobe of door Adobe Support.

**De naam van de definitie van een kenmerklader wijzigen**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Klik op de pagina [!DNL Attribute Loader] onder de kolomkop [!DNL Actions] op **[!UICONTROL Rename]** voor de definitienaam van kenmerklader die u wilt wijzigen.
1. Voer op de pagina [!DNL Attribute Loader Rename] de nieuwe naam van de definitie in het veld [!DNL Name] in.
1. Klik op **[!UICONTROL Rename]**.
1. (Optioneel) Voer op de pagina [!DNL Attribute Loader Definitions] een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Kenmerkladingsgegevens {#task_2F3C55189B0A4049AB2113F2291CC181} laden

U kunt de geconfigureerde gegevens van de kenmerklader downloaden naar het zoeken/verhandelen van sites.

De [!DNL Data Load] pagina toont de volgende informatie over de status van uw laatste verrichting van de Lading van de Gegevens van de Lader van Attributen:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Statusveld </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Status </p> </td> 
   <td colname="col2"> <p>Geeft aan of de laatste poging tot het laden van gegevens is gelukt of mislukt. Of de status van een gegevenslaadbewerking die al wordt uitgevoerd, wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Begintijd </p> </td> 
   <td colname="col2"> <p>Geeft de datum en tijd weer waarop de laatste bewerking voor het laden van gegevens is gestart. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Eindtijd </p> </td> 
   <td colname="col2"> <p>Geeft de voltooiingsdatum en -tijd weer van de laatste bewerking voor het laden van gegevens. Of het geeft aan dat de huidige bewerking voor het laden van gegevens nog wordt uitgevoerd. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Kenmerklader-gegevens laden**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Klik op [!DNL Attribute Loader Definitions] op de pagina.**[!UICONTROL Load Attribute Loader Data]**
1. Voer op de pagina **[!UICONTROL Attribute Loader Data Load]** een van de volgende handelingen uit:

   * Klik **[!UICONTROL Start Load]** om de laadbewerking te starten.

      Tijdens een verrichting van de gegevenslading, verstrekt **Progress** rij informatie over zijn vooruitgang.

   * Klik **[!UICONTROL Stop Load]** om de laadbewerking te stoppen.

1. Klik op **[!UICONTROL Close]** om terug te keren naar de pagina [!DNL Attribute Loader Definitions].

## Voorvertoning van kenmerkladingsgegevens {#task_735CDCC1D8174B7B9F5B8E0AFA5F0CA0}

U kunt Voorvertoning gebruiken om de laatst geladen gegevens van kenmerklader weer te geven.

In de kolom Rij in de tabel wordt het nummer voor elke gegevensrij weergegeven, waarmee de oorspronkelijke volgorde wordt aangegeven waarin de waarden voor kenmerklader zijn geladen.

In de overige kolommen worden de waarden weergegeven die aan elk item zijn gekoppeld.

Als de tabel leeg is, betekent dit dat u nog geen kenmerklader-gegevens hebt geladen. U kunt de pagina [!DNL Attribute Loader Data Preview] sluiten en vervolgens kenmerkladingsgegevens laden.

Zie [Kenmerkladingsgegevens laden](../c-about-settings-menu/c-about-metadata-menu.md#task_2F3C55189B0A4049AB2113F2291CC181).

**Voorvertoning van kenmerklader-gegevens weergeven**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Klik op de pagina [!DNL Attribute Loader Definitions] onder de kolom [!DNL Actions] op **[!UICONTROL Preview]** voor de configuratie waarvan u de gedownloade gegevens wilt weergeven.
1. Gebruik op de pagina [!DNL Attribute Loader Data Preview] de navigatie- en weergaveopties boven en onder aan de pagina om de gegevens weer te geven.

   Klik op een kolomkop in de tabel om de gegevens in oplopende of aflopende volgorde te sorteren.
1. Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL Download to Desktop]** om de lijst als .xlt dossier te downloaden en te bewaren.
   * Sluit de pagina wanneer u klaar bent met het voorvertonen van de kenmerklader-gegevens en ga terug naar de vorige weergegeven pagina.

## De instellingen van de definitie {#task_EA99A9694FE948ADA82C1DBA0667851B} van een kenmerklader weergeven

U kunt de configuratie-instellingen van een bestaande definitie van kenmerklader controleren.

Nadat een definitie van de Lader van Attributen aan [!DNL Attribute Loader Definitions] pagina wordt toegevoegd, kunt u niet zijn het Type plaatsen veranderen. In plaats daarvan moet u de definitie verwijderen en vervolgens een nieuwe definitie toevoegen.

>[!NOTE]
>
>Als u Kenmerklader wilt gebruiken, moet deze mogelijk in uw account zijn ingeschakeld door uw accountvertegenwoordiger van de Adobe of door Adobe Support.

**De instellingen van de definitie van een kenmerklader weergeven**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Klik op de pagina [!DNL Attribute Loader] onder de kolomkop [!DNL Actions] op **[!UICONTROL Edit]** voor de definitienaam van een kenmerklader waarvan u de instellingen wilt bekijken of bewerken.

## Logbestand weergeven van de meest recente gegevensbelasting van kenmerklader {#task_9C7D6E34BB6C4A40B7CA3EE36ACB0837}

U kunt [!DNL View Log] gebruiken om het dossier van het de gegevenslogboek van de Lader van Attributen van het meest recente downloadproces te onderzoeken. U kunt de logboekmening ook gebruiken om een lopende download te controleren.

Zie [Kenmerkladingsgegevens laden](../c-about-settings-menu/c-about-metadata-menu.md#task_2F3C55189B0A4049AB2113F2291CC181).

**Het logboek weergeven van de meest recente gegevens van Kenmerklader die zijn geladen**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Klik op [!DNL Attribute Loader Definitions] op de pagina. **[!UICONTROL View Log]** Logboekpagina,
1. Gebruik op de pagina [!DNL Attribute Loader Data Log] de navigatie- en weergaveopties boven en onder aan de pagina om de loggegevens weer te geven.
1. Als u klaar bent, sluit u de pagina om terug te keren naar de pagina [!DNL Attribute Loader Definitions].

## Definitie {#task_E8980F66888B476E98C228C1D307EDF8} van kenmerklader verwijderen

U kunt een bestaande definitie van kenmerklader verwijderen die u niet meer nodig hebt of gebruikt.

>[!NOTE]
>
>Als u Kenmerklader wilt gebruiken, moet deze mogelijk in uw account zijn ingeschakeld door uw accountvertegenwoordiger van de Adobe of door Adobe Support.

**Een definitie van een kenmerklader verwijderen**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Klik op de pagina [!DNL Attribute Loader Definitions] onder de kolomkop [!DNL Actions] op **[!UICONTROL Delete]** voor de definitienaam van kenmerklader die u wilt verwijderen.
1. Klik op [!DNL Attribute Loader Delete] op de pagina.**[!UICONTROL Delete]**
