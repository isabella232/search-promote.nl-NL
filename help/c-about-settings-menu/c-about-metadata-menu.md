---
description: Gebruik het menu van Meta-gegevens om de definities van het Onderzoek en indexinjecties aan te passen.
seo-description: Gebruik het menu van Meta-gegevens om de definities van het Onderzoek en indexinjecties aan te passen.
seo-title: Ongeveer het menu van Meta-gegevens
solution: Target
subtopic: Metadata
title: Ongeveer het menu van Meta-gegevens
topic: Settings,Site search and merchandising
uuid: f12fc863-a140-45e8-b219-3dbfdef099cd
translation-type: tm+mt
source-git-commit: cf2707d124bd3f3a864610bcf41dda5e5670fc90

---


# Ongeveer het menu van Meta-gegevens{#about-the-metadata-menu}

Gebruik het menu van Meta-gegevens om de definities van het Onderzoek en indexinjecties aan te passen.

## Informatie over definities {#concept_AE48035C210145169BE067D396975620}

U kunt gebruiken [!DNL Definitions] om de inhoud en de relevantie van de HTML en meta-gegevensgebieden aan te passen die worden overwogen wanneer een klant een onderzoeksvraag voorlegt.

U kunt de gebieden uitgeven die reeds vooraf bepaald zijn. Of, u kunt nieuwe user-defined gebieden ook tot stand brengen die op de inhoud van de meta-gegevensmarkering worden gebaseerd. Elke definitie wordt getoond op één enkele lijn op de [!DNL Staged Definitions] pagina.

Zie ook [over de Meningen](../c-about-reports-menu/c-about-data-views.md#concept_DCA897D074464BC1861AA47B40CC86C3)van Gegevens.

## Het toevoegen van een nieuw meta markeringsgebied {#task_6DF188C0FC7F4831A4444CA9AFA615E5}

U kunt uw eigen gebieden van de meta-gegevensmarkering bepalen en toevoegen.

Alvorens de gevolgen van de nieuwe definitie van de meta- markering aan klanten zichtbaar zijn, moet u uw plaatsindex herbouwen.

**Om een nieuw meta markeringsgebied toe te voegen**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**.
1. Voor de [!DNL Definitions] pagina, klik **[!UICONTROL Add New Field]**.
1. Voor de [!DNL Add Field] pagina, plaats de opties die u wilt.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Optie </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Veldnaam </p> </td> 
      <td colname="col2"> <p>Specificeert een naam die wordt gebruikt om het gebied van verwijzingen te voorzien. </p> <p>De veldnaam moet aan de volgende regels voldoen: </p> <p> 
      <ul id="ul_D39D09CD7E7D41A59ECB6C5A6F4F263D"> 
      <li id="li_11CE852BE3C64CEF90FEC7A6E1079E13"> De naam mag alleen alfanumerieke tekens bevatten. </li> 
      <li id="li_7FC340E7C58545C88CE9AF4AF09AD7AD"> De streepjes worden toegestaan in de naam, maar geen ruimten. </li> 
      <li id="li_996FF38457AB4C6DB22B15850A0830CC"> Je kunt een naam invoeren van maximaal 20 tekens. </li> 
      <li id="li_C1019E587995444D9587D5EA495D719E"> De naam is niet case-sensitive, maar wordt getoond en precies opgeslagen aangezien u het typt. </li> 
      <li id="li_E55404D6CE354EC89CFFEB1048A11F44"> U kunt niet de namen gebruiken die op de vooraf bepaalde gebieden bestaan zoals die in de lijst op de <span class="wintitle"> Gelaagde </span> pagina van Definities worden gezien. </li> 
      <li id="li_7CE328AE3B5F45A8A09E2DA7ECB62551"> U kunt niet het woord "om het even welk"als waarde van een user-defined gebiedsnaam gebruiken. </li> 
      <li id="li_9B8287EED1784E79BFCBBBA956705CD2"> U kunt niet de namen van vooraf bepaalde gebieden uitgeven. </li> 
      </ul> </p> <p> Voorbeelden van veldnamen: </p> <p> 
      <ul id="ul_5881669913D04E35A6D4A6D31BEE7DF3"> 
        <li id="li_0AFFB8B516FE40F8A615C2F578F2CEA3"> auteur </li> 
        <li id="li_7F0ADFBFB21E4B84ACA8A1CEBFE344D1"> Publicatiedatum </li> 
        <li id="li_6D1BEB3D19AC499E9227EC115AEB6296"> iets wild </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Naam/namen meta-tag </p> </td> 
      <td colname="col2"> <p>Bepaalt de inhoud die met het bepaalde gebied wordt geassocieerd. </p> <p>De lijst van namen kan tot 255 lange karakters zijn. En, kan de naam om het even welke karakters bevatten die in de naamattributen van een meta markering van HTML worden toegestaan. </p> <p>U kunt veelvoudige metamarkeringen in één enkele gebiedsdefinitie specificeren. </p> <p>De veelvoudige waarden moeten komma-gescheiden zijn, en de uiterst linkse meta markeringsnaam die op om het even welke bepaalde Web-pagina wordt gevonden neemt belangrijkheid. </p> <p>Bijvoorbeeld, veronderstel dat u een gebied genoemd "auth"hebt bepaald. De veldnaam heeft de bijbehorende meta-tags "auteur, dc.auteur". In dit geval, wordt de inhoud van de "auteur"meta-markering geïndexeerd en over dat van "dc.auteur"gezocht als beide meta- markeringen op een Web-pagina verschijnen. </p> <p>De user-defined gebieden moeten minstens één naam van de meta- markering in hun definitie hebben. De vooraf bepaalde gebieden te hoeven om geen bijbehorende meta- markering te hebben. Nochtans, als één of meerdere metamarkeringen worden gespecificeerd, treedt de inhoud van de meta- markeringen de huidige gegevensbron voor elke markering met voeten. </p> <p>Bijvoorbeeld, als de meta markering "dc.title"met het vooraf bepaalde gebied van de "titel"wordt geassocieerd, wordt de inhoud van de meta-markering "dc.title"geïndexeerd over dat van 
      <userinput>
        &lt;titel&gt; 
      </userinput> tag voor een bepaald document. </p> <p>Voorbeelden hiervan zijn: </p> <p> 
      <ul id="ul_0132E15FC19E4C0CA13CD5A12EA3BBEC"> 
      <li id="li_ECD3B194FECB4C2090CAEC8449320D3F"> dc. datum </li> 
      <li id="li_09C76BC7AC7348859D01989697212E31"> beschrijving </li> 
      <li id="li_9230C0450F9D424087D1F127048DA311"> merknaam </li> 
      </ul> </p> </td> 
    </tr> 
      <tr> 
      <td colname="col1"> <p>Gegevenstype </p> </td> 
      <td colname="col2"> <p>Elk gebied heeft een bijbehorend gegevenstype zoals tekst, aantal, datum, versie, rang, of plaats. Dit gegevenstype bepaalt hoe de inhoud van het gebied wordt geïndexeerd, gezocht en naar keuze, gesorteerd. </p> <p>U kunt niet het gegevenstype veranderen nadat u de gebiedsdefinitie creeert. </p> <p>Gebruik de volgende informatie om u te helpen het gegevenstype selecteren dat voor de informatie relevant is die het gebied bevat. </p> <p> 
      <ul id="ul_A3AD5A0CF354410F836311F39151B8A6"> 
      <li id="li_9F412DA7D9EF497BA6E65F9CE10F3046"> <span class="uicontrol"> De het type van </span> gegevens van de tekst gebieden worden behandeld als karakterkoorden. </li> 
      <li id="li_AD78B75644AE40208F0239311015611F"> <span class="uicontrol"> De het gegevenstype van het aantal gebieden worden behandeld als geheel of floating-point numerieke waarden. </span> </li> 
      <li id="li_0B46975C589148E9A7C32A8D250487B7"> <span class="uicontrol"> Datumgegevenstype velden worden behandeld als datum-/tijdspecificaties. </span> U kunt de toegestane datum/tijdformaten aanpassen wanneer u toevoegt of het nieuwe gebied uitgeeft. </li> 
      <li id="li_BB68CB1DBE0543AC9000B3DEDFB28E7E"> <span class="uicontrol"> De het gegevenstype van de versie </span> gebieden worden behandeld als vrij-vorm numerieke gegevens. Bijvoorbeeld, 1.2.3 soorten vóór 1.2.2. </li> 
      <li id="li_0BA895B4DADA46528A7A4161EEB1521E"> <span class="uicontrol"> Gegevenstype van </span> banken wordt behandeld het zelfde als "Aantal"typevelden, behalve dat zij extra de rangschikking/relevantie berekeningen in de onderzoeksresultaten beïnvloeden. <p>Zie <a href="../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397" type="concept" format="dita" scope="local"> over rangschikkingsregels </a>. </p> </li> 
      <li id="li_459405DA437049AD88AA1FAC28F04720"> <span class="uicontrol"> De het gegevenstype van de plaats </span> - gebieden worden behandeld als fysieke plaats overal in de wereld. De toegestane plaatsformaten omvatten het volgende: <p> 
      <ul id="ul_D2CEBFA1A5504AA996BA2F7641AFB7F3"> 
      <li id="li_5283A2F2D5D84840B3D920C08D43654C"> De codes van 5 of 9 cijferZIP in de vorm van DDD of DDD-DDDD, waar elke "D"een 0-9 cijfer is. </li> 
      <li id="li_A5CD4DFC90164BC68183DB7D10603B7C"> Driecijferige gebiedscodes in de vorm van DDD. </li> 
      <li id="li_9DAEAE64BC7F4902B25043D998C8F56D"> De paren van de breedte/van de lengte in de vorm ±DD.DDDD±DDD.DDDD, waar het eerste aantal de breedtegraad specificeert en het tweede aantal de lengtegraad specificeert. </li> 
      </ul> </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Lijsten toestaan </p> </td> 
      <td colname="col2"> <p>Beschikbaar slechts als het gegevenstype <span class="uicontrol"> Tekst </span>, of <span class="uicontrol"> Aantal </span> wordt geselecteerd. </p> <p>De afzonderlijke index bepaalde waarden in de meta-gegevensinhoud van dit gebied. </p> <p>Bijvoorbeeld, wordt de inhoud "Rood, Geel, Groen, Blauw"behandeld als vier afzonderlijke waarden in plaats van wanneer "de Lijsten van de Toestaan"wordt geselecteerd. Deze behandeling is het nuttigst met waaier het zoeken (gebruiken 
      <userinput>
        sp_q_min 
      </userinput>, 
      <userinput>
        sp_q_max 
      </userinput>of 
      <userinput>
        sp_q_exact 
      </userinput>) en met de 
      <userinput>
        &lt;zoek-gebied-waarde-lijst&gt; 
      </userinput>, 
      <userinput>
        &lt;zoek-gebied-waarden&gt; 
      </userinput>, en 
      <userinput>
        &lt;zoek-vertoning-gebied-waarden&gt; 
      </userinput>. </p> <p>Niet beschikbaar als het gegevenstype van de Versie wordt geselecteerd. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Dynamisch gezichtspunt </p> </td> 
      <td colname="col2"> <p> 
        <!--NEW 2/2/2014--> <p>Opmerking:  Deze eigenschap wordt niet toegelaten door gebrek. Neem contact op met Technische ondersteuning om deze voor uw gebruik te activeren. Nadat het wordt geactiveerd, verschijnt het in het gebruikersinterface. </p> </p> <p>Plaatst de geïdentificeerde facet om dynamisch te zijn. </p> <p>De gebieden worden gebouwd bovenop de gebieden van de meta- markering. Een meta markeringsgebied is een laag-niveau, de laag van het kernonderzoek van Adobe Onderzoek&amp;Promote. De facetten, anderzijds maken deel uit van GS (Geleid Onderzoek) - de high-level, presentatielaag van het Onderzoek&amp;Promote van Adobe. Facets eigen meta markeringsgebieden, echter, weten de meta markeringsgebieden niets over facetten. </p> <p>Zie <a href="../c-about-design-menu/c-about-dynamic-facets.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> over Dynamische Facets </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Dedupup toestaan </p> </td> 
      <td colname="col2"> <p>Controleer deze optie om deduplicatie voor dit gebied toe te laten. Dat wil zeggen, laat dit gebied toe om bij onderzoek-tijd als 
        <userinput>
          sp_dedupe_field 
        </userinput> CGI-parameter zoeken. </p> <p>Zie <a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> de parameters van CGI van het Onderzoek </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Naam tabel </p> </td> 
      <td colname="col2"> <p>Hiermee wordt het gegeven veld permanent gekoppeld aan de gegeven tabelnaam. </p> <p>Om het even welke tijd zulk een gebied binnen een parameter van het kernonderzoek CGI of een malplaatjemarkering wordt vermeld, wordt de lijstnaam automatisch verstrekt. Deze eigenschap staat de selectie van dynamische facetten door lijstgelijken toe, maar u kunt het voor niet-dynamische facetgebieden ook gebruiken, indien gewenst. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Lijstscheidingen </p> </td> 
      <td colname="col2"> <p>Beschikbaar slechts als <span class="uicontrol"> toestaat de Lijsten </span> wordt geselecteerd. </p> <p>Specificeert welke karakters afzonderlijke lijstwaarden. U kunt veelvoudige karakters specificeren, elk waarvan als waardeseparator wordt behandeld. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Zoeken op standaard </p> </td> 
      <td colname="col2"> <p>Wanneer geselecteerd, wordt de gebiedsinhoud gezocht zelfs wanneer het gebied niet uitdrukkelijk in een bepaalde onderzoeksvraag wordt gespecificeerd. Als u deze optie schrapt, wordt het gebied slechts gezocht wanneer gevraagd. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Verticaal updateveld </p> </td> 
      <td colname="col2"> <p> <p>Opmerking:  Deze eigenschap wordt niet toegelaten door gebrek. Neem contact op met Technische ondersteuning om deze voor uw gebruik te activeren. Nadat het wordt geactiveerd, verschijnt het in het gebruikersinterface. </p> </p> <p>Plaatst het geïdentificeerde gebied om een Verticaal gebied van de Update te zijn. </p> <p>Verticale updatevelden zijn kandidaten die moeten worden bijgewerkt in de vorm van het Verticale updateproces ( <span class="uicontrol"> Index </span> &gt; <span class="uicontrol"> Verticale update </span>.) Vanwege de manier waarop Verticale updates worden gemaakt, kan inhoud uit deze velden niet worden doorzocht in zoeken in de vrije tekst. Het controleren van deze optie resulteert in de inhoud van dit gebied die niet aan de "woord"index tijdens om het even welk soort indexverrichting wordt toegevoegd. Het laat ook de update van dit gebied tijdens een Verticale verrichting van de Update toe. </p> <p>Meer over Verticale Updates leren, zie <a href="../c-about-index-menu/c-about-vertical-updates.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> over Verticale Update </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Relevantie </p> </td> 
      <td colname="col2"> <p>U kunt de relevantie van vooraf bepaalde en user-defined gebieden uitgeven. </p> <p>Relevantie wordt gespecificeerd op schaal 1-10. Een instelling van 1 betekent dat het de minst relevante is en 10 het meest relevant zijn. Deze waarden worden in aanmerking genomen wanneer de software de vraaggelijken op elk gebied overweegt. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Sorteren </p> </td> 
      <td colname="col2"> <p>Specificeert wanneer de resultaten door het genoemde gebied, als 
        <userinput>
          sp_s 
        </userinput> CGI-parameter zoeken. </p> <p>Zie <a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> de parameters van CGI van het Onderzoek </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Taal </p> </td> 
      <td colname="col2"> <p>Beschikbaar slechts als het gegevenstype <span class="uicontrol"> Rank </span>, <span class="uicontrol"> Aantal </span>, of <span class="uicontrol"> Datum </span> wordt geselecteerd. </p> <p>Controleert de taal en de scèneovereenkomsten die wanneer het indexeren van de datum, het aantal, en rangschikkingswaarden voor dit gebied worden toegepast. </p> <p>U kunt verkiezen om de rekeningstaal (Talen &gt; Woorden &amp; Talen) toe te passen. Of, u kunt de taal toepassen die met het document wordt geassocieerd dat elke aantal of datumwaarde, of een specifieke taal bevat. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Datumformaat(s) </p> </td> 
      <td colname="col2"> <p>Beschikbaar slechts als de gegevenstype <span class="uicontrol"> Datum </span> wordt geselecteerd. </p> <p>Controleert de datumformaten die wanneer het indexeren van datumwaarden voor dit gebied worden erkend. </p> <p>Een standaardlijst van de koorden van het datumformaat wordt verstrekt voor elk datumgebied. U kunt aan de lijst toevoegen of de lijst uitgeven om de behoeften van uw eigen plaats te passen. </p> <p>Zie <a href="../c-appendices/r-date-formats.md#reference_4D1FC1F6B9F44857967188496D8D335B" type="reference" format="dita" scope="local"> Datumformaten </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Formaten voor de testdatum </p> </td> 
      <td colname="col2"> <p>Beschikbaar slechts als de gegevenstype <span class="uicontrol"> Datum als Type van Gegevens </span> wordt geselecteerd. </p> <p>Laat u voorproef de datumformaten die u hebt gespecificeerd om ervoor te zorgen dat zij correct geformatteerd zijn. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Tijdzone </p> </td> 
      <td colname="col2"> <p>Beschikbaar slechts als de gegevenstype <span class="uicontrol"> Datum als Type van Gegevens </span> wordt geselecteerd. </p> <p>Controleert de veronderstelde tijdzone die wordt toegepast wanneer het indexeren van datumwaarden voor dit gebied dat geen tijdzone specificeert. </p> <p>Bijvoorbeeld, als uw streek van de rekeningstijd aan "Amerika/Los Angeles"wordt geplaatst en u de Tijdzone van de Rekening van het <span class="uicontrol"> </span>Gebruik selecteert, wordt de volgende waarde van de meta-datum, die geen gespecificeerde tijdzone heeft, behandeld alsof het de Tijd van de Stille Oceaan was, rekenend voor daglichtbesparingen rekenschap gevend: </p> <p>&lt;meta name="dc.date" content="Mon, 05 sep. 2012:12:00"&gt; </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Minste belangrijke waarde van de Rank </p> </td> 
      <td colname="col2"> <p>Beschikbaar slechts als de gegevenstype <span class="uicontrol"> Rank </span> als Type van Gegevens wordt geselecteerd. </p> <p>Controleert de rank waarde die de minimumrang van om het even welk document vertegenwoordigt. </p> <p>Als uw document rangschikken zich van 0 voor de laagste rang aan 10 voor de hoogste rang uitstrekken, dan plaatst u deze waarde aan 0. </p> <p>Als uw document rangschikken zich van 1 voor de hoogste rang aan 10 voor de laagste rang uitstrekken, dan plaatst u deze waarde aan 10. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Standaardwaarde van de Rank </p> </td> 
      <td colname="col2"> <p>Beschikbaar slechts als de gegevenstype <span class="uicontrol"> Rank </span> als Type van Gegevens wordt geselecteerd. </p> <p>Controleert de rank waarde die wordt gebruikt als een document om het even welke meta- markeringen niet bevat die voor dit rangschikkingsgebied worden bepaald. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Belangrijkste waarde van de Rank </p> </td> 
      <td colname="col2"> <p>Beschikbaar slechts als de gegevenstype <span class="uicontrol"> Rank </span> als Type van Gegevens wordt geselecteerd. </p> <p>Controleert de rank waarde die de maximumrang van om het even welk document vertegenwoordigt. </p> <p>Als uw document rangschikken zich van 0 voor de laagste rang aan 10 voor de hoogste rang uitstrekken, dan plaatst u deze waarde aan 10. </p> <p>Als uw document rangschikken zich van 1 voor de hoogste rang aan 10 voor de laagste rang uitstrekken, dan plaatst u deze waarde aan 1. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Standaardeenheden </p> </td> 
      <td colname="col2"> <p>Beschikbaar slechts als het gegevenstype <span class="uicontrol"> Plaats als Type van Gegevens </span> wordt geselecteerd. </p> <p>Controleert de behandeling van afstandswaarden voor nabijheidsonderzoeken. </p> <p>Als u de standaardeenheden op <span class="uicontrol"> Miles plaatst </span>, dan om het even welke nabijheidsonderzoekscriteria minimum/maximumafstand die op dit gebied (als 
      <userinput>
        sp_q_min[_#] 
      </userinput> of de 
      <userinput>
        sp_q_max[_#] 
      </userinput> De parameters van CGI van het onderzoek) worden behandeld als mijlen, anders als kilometers. </p> <p>Deze optie controleert ook de standaardoppervlakken die op de output van worden toegepast 
      <userinput>
        &lt;Search-Display-Veld&gt; 
      </userinput> de het malplaatjelag van onderzoeksresultaten wanneer toegepast op een gebied van de nabijheidsonderzoeksoutput. </p> <p>Zie <a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> Over nabijheidsonderzoek </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Beschrijving bereik maken? </p> </td> 
      <td colname="col2"> <p>Beschikbaar slechts als het <span class="uicontrol"> Aantal als Type van Gegevens </span> wordt geselecteerd. </p> <p>Controleert de automatische verwezenlijking van de beschrijvingen van de Waaier van het Gebied, voor gebruik met <span class="uicontrol"> Ontwerp </span> &gt; <span class="uicontrol"> Navigatie </span> &gt; <span class="uicontrol"> Facets </span>. </p> <p>Zie <a href="../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5" format="dita" scope="local"> Over Facets </a>. </p> <p> <p>Opmerking:  Als dit gebied het Verticale Gebied van de Update heeft <span class="uicontrol"> </span> gecontroleerd, wordt het geproduceerde de beschrijvingsgebied van de Waaier van het Gebied bijgewerkt tijdens een Verticale Update. Nochtans, wordt het geadviseerd dat het gebied dat op het Gebied van de Waaier wordt geïdentificeerd <span class="uicontrol"> ook het Verticale Gebied van de Update heeft </span> <span class="uicontrol"> </span> gecontroleerd. </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Bereik </p> </td> 
      <td colname="col2"> <p>Beschikbaar slechts als <span class="uicontrol"> creeer de Beschrijving van de Waaier </span> wordt gecontroleerd. </p> <p>Het <span class="uicontrol"> </span> gebied van de Tekst dat met waaierbeschrijvingen voor het huidige gebied moet worden bijgewerkt. Deze lijst bevat alle <span class="uicontrol"> gebieden van de Tekst </span> die niet reeds met andere gebieden voor de generatie van de Waaier van het Gebied worden gebruikt. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Waarden bereik </p> </td> 
      <td colname="col2"> <p>Beschikbaar slechts als <span class="uicontrol"> creeer de Beschrijving van de Waaier </span> wordt gecontroleerd en een punt van het Gebied van de <span class="uicontrol"> Waaier wordt </span> geselecteerd. </p> <p>Een leeg-afgebakende lijst van gegevenspunten aan gebruik wanneer het creëren van de beschrijvingen van de Waaier van het Gebied. Bijvoorbeeld: </p> <code> 10&amp;nbsp;20&amp;nbsp;50&amp;nbsp;100&amp;nbsp;1000 </code> <p>U kunt deze waarden in om het even welke orde ingaan. De waarden worden gesorteerd en de duplicaten worden verwijderd alvorens het wordt bewaard. U kunt negatieve en niet geheelwaarden ook specificeren. </p> <p>Voor elk van de waarden van dit gebied: 
      <ul id="ul_C4B41AF5AADF4B84B9C489CE82FF7075"> 
      <li id="li_90736394A5AE4F5CA6B47687BCB627AA">als de waarde minder dan (&lt;) de kleinste waarde in de Waarden van de <span class="uicontrol"> Waaier is </span>, wordt het <span class="uicontrol"> "minder dan"Formaat </span> gebruikt </li> 
      <li id="li_A5C272B2D26A468CA07EB2046B2EA8A7">als de waarde groter is dan of gelijk aan (&gt;=) de grootste waarde in de Waarden van de <span class="uicontrol"> Waaier </span>, wordt het <span class="uicontrol"> "Grotere dan"Formaat </span> gebruikt. </li> 
      <li id="li_9DDFB70E1E824CF4819C57450C1A6DD2">anders, wordt een "waaier"gevonden wanneer de gebiedswaarde tussen twee opeenvolgende Waarden van de <span class="uicontrol"> Waaier </span> (groter dan (&gt;) de kleinere waarde en minder dan of gelijk aan (&lt;=) de grotere waarde) valt, en het <span class="uicontrol"> Tussenliggende Formaat </span> wordt gebruikt. </li> 
    </ul> </p> <p>Bijvoorbeeld, zal de bovengenoemde voorbeeldreeks waarden een reeks beschrijvingen voor waarden bepalen: 
    <ul id="ul_03ED30D5A19346AB8E6809BDD186A9A9"> 
      <li id="li_F97A6B3763954EFE9B6751F472AF7D20">minder dan 10 </li> 
      <li id="li_12B6F636A6444B8292E0BFE4F55032DF">groter dan of gelijk aan 10 en kleiner dan 20 </li> 
      <li id="li_545A2EAF5BD046B5AD59B77DB43DCD14">groter dan of gelijk aan 20 en kleiner dan 50 </li> 
      <li id="li_26A8CD2422524D2CBD36794C6908572A">groter dan of gelijk aan 50 en kleiner dan 100 </li> 
      <li id="li_05EBEEE68DC348E0821F1CC16D04D69C">100 of meer en minder dan 10000 </li> 
      <li id="li_9513A6B519394780A6A41B80762A0370">groter dan of gelijk aan 10000 </li> 
      </ul> </p> <p>Zie <span class="uicontrol"> Test met Greater dan? </span> om te veranderen hoe deze tests worden uitgevoerd. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>"Minder dan"-indeling </p> </td> 
      <td colname="col2"> <p>Beschikbaar slechts als <span class="uicontrol"> creeer de Beschrijving van de Waaier </span> wordt gecontroleerd en een punt van het Gebied van de <span class="uicontrol"> Waaier wordt </span> geselecteerd. </p> <p>Dit is het malplaatje wordt gebruikt om de waaierbeschrijving voor waarden te specificeren minder dan de kleinste waarde die in de Waarden van de <span class="uicontrol"> Waaier wordt gevonden </span>. De kleinste waarde zal worden vertegenwoordigd gebruikend het numerieke placeholder teken <span class="uicontrol"> ~N~ </span>. Bijvoorbeeld: </p> <code> Less&amp;nbsp;than&amp;nbsp;~N~ </code> <p>of: </p> <code> ~N~&amp;nbsp;and&amp;nbsp;below </code> <p>Normaal, zal de waarde "as-is"geformatteerd zijn - d.w.z. voor een <span class="uicontrol"> </span> definitie van de Waarden van de Waaier van "5 10 20"en een geleverde waarde van 1, zou de geproduceerde waaierbeschrijving eenvoudig iets als "minder dan 5"zijn. Als u in plaats daarvan het "4.99 en hieronder"zou willen hebben, plaats <span class="uicontrol"> Precision </span> aan <span class="uicontrol"> 2 </span> en gebruik dit formaat: </p> <code> ~n~&amp;nbsp;and&amp;nbsp;below </code> <p>In <span class="uicontrol"> "Minder dan"Formaat </span>, zal het kleine <span class="uicontrol"> ~n~ </span> veroorzaken dat de waarde om <i>onderaan</i> volgens het <span class="uicontrol"> precisie </span> plaatsen wordt rond gemaakt. </p> <p>Opmerking: om om het even welke numerieke placeholder in de waaierbeschrijving te omvatten, zoals is, specificeer met een backslash (\) prefix - b.v. <span class="uicontrol"> \~N~ </span> of <span class="uicontrol"> \~n~ </span>. Om een backslash karakter te omvatten, specificeer het met een andere backslash - b.v. <span class="uicontrol"> \\ </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Intermediair formaat </p> </td> 
      <td colname="col2"> <p>Beschikbaar slechts als <span class="uicontrol"> creeer de Beschrijving van de Waaier </span> wordt gecontroleerd en een punt van het Gebied van de <span class="uicontrol"> Waaier wordt </span> geselecteerd. </p> <p>Dit is het malplaatje wordt gebruikt om de waaierbeschrijving voor waarden te specificeren die ergens tussen de kleinste en grootste waarden vallen die in de Waarden van de <span class="uicontrol"> Waaier worden gevonden </span>. Voor de bepaalde waaier, zal de lagere waaierwaarde worden vertegenwoordigd gebruikend het numerieke placeholder teken <span class="uicontrol"> ~L~ </span>, en de hogere waaierwaarde zal worden vertegenwoordigd gebruikend het teken <span class="uicontrol"> ~H~ </span>. Bijvoorbeeld: </p> <code> ~L~&amp;nbsp;to&amp;nbsp;~H~ </code> <p>of: </p> <code> Between&amp;nbsp;~L~&amp;nbsp;and&amp;nbsp;~H~ </code> <p>of: </p> <code> Less&amp;nbsp;than&amp;nbsp;~H~&amp;nbsp;and&amp;nbsp;greater&amp;nbsp;than&amp;nbsp;~L~ </code> <p>Normaal, zullen de waarden "zoals-is"geformatteerd zijn - d.w.z. voor een <span class="uicontrol"> </span> definitie van de Waarden van de Waaier van "5 10 20"en een geleverde waarde van 8, zou de geproduceerde waaierbeschrijving eenvoudig iets als "tussen 5 en 10"zijn. Als u in plaats daarvan het "tussen 5 en 9.99"zou willen hebben, met de hogere waarde <i>neerwaarts</i>wordt aangepast, plaats <span class="uicontrol"> Precision </span> aan <span class="uicontrol"> 2 </span> en gebruik dit formaat: </p> <code> Between&amp;nbsp;~L~&amp;nbsp;and&amp;nbsp;~h~ </code> <p>Op dezelfde manier kan <span class="uicontrol"> ~L~ </span> worden vervangen door <span class="uicontrol"> ~l~ </span> om de lagere waarde <i>naar boven</i>te laten bijstellen, ook volgens de <span class="uicontrol"> Precision </span> instelling. Dit betekent dat een definitie als: </p> <code> Between&amp;nbsp;~l~&amp;nbsp;and&amp;nbsp;~H~ </code> <p>met een <span class="uicontrol"> Precision- </span> waarde van <span class="uicontrol"> 2 </span> zou "tussen 5.01 en 10"creëren. </p> <p>De kleine letters <span class="uicontrol"> ~l~ </span> zullen ervoor zorgen dat de lagere waarde <i>naar boven</i> wordt afgerond volgens de <span class="uicontrol"> Precision </span> instelling, en de lagere waarde ~h~ <span class="uicontrol"> zal ervoor zorgen dat de hogere waarde </span> naar beneden <i></i>wordt afgerond. </p> <p>Opmerking: om om het even welke numerieke placeholder in de waaierbeschrijving te omvatten, zoals is, specificeer met een backslash (\) prefix - b.v. <span class="uicontrol"> \~L~ </span> of <span class="uicontrol"> \~h~ </span>. Om een backslash karakter te omvatten, specificeer het met een andere backslash - b.v. <span class="uicontrol"> \\ </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>"Groter dan"-indeling </p> </td> 
      <td colname="col2"> <p>Beschikbaar slechts als <span class="uicontrol"> creeer de Beschrijving van de Waaier </span> wordt gecontroleerd en een punt van het Gebied van de <span class="uicontrol"> Waaier wordt </span> geselecteerd. </p> <p>Dit is het malplaatje dat wordt gebruikt om de waaierbeschrijving voor waarden te specificeren groter dan de grootste waarde die in de Waarden van de <span class="uicontrol"> Waaier wordt gevonden </span>. De grootste waarde zal worden vertegenwoordigd gebruikend het numerieke placeholder teken <span class="uicontrol"> ~N~ </span>. Bijvoorbeeld: </p> <code> Greater&amp;nbsp;than&amp;nbsp;~N~ </code> <p>of: </p> <code> ~N~&amp;nbsp;and&amp;nbsp;above </code> <p>Normaal, zal de waarde "as-is"geformatteerd zijn - d.w.z. voor een <span class="uicontrol"> </span> definitie van de Waarden van de Waaier van "5 10 20"en een geleverde waarde van 30, zou de geproduceerde waaierbeschrijving eenvoudig iets als "groter zijn dan 20". Als u in plaats daarvan het "20.01 en hierboven"zou willen hebben, plaats <span class="uicontrol"> Precision </span> aan <span class="uicontrol"> 2 </span> en gebruik dit formaat: </p> <code> ~n~&amp;nbsp;and&amp;nbsp;above </code> <p>In <span class="uicontrol"> "Groter dan"Formaat </span>, zal het kleine <span class="uicontrol"> ~n~ </span> veroorzaken dat de waarde <i>naar boven</i> volgens het <span class="uicontrol"> precisie </span> plaatsen wordt afgerond. </p> <p>Opmerking: om om het even welke numerieke placeholder in de waaierbeschrijving te omvatten, zoals is, specificeer met een backslash (\) prefix - b.v. <span class="uicontrol"> \~N~ </span> of <span class="uicontrol"> \~n~ </span>. Om een backslash karakter te omvatten, specificeer het met een andere backslash - b.v. <span class="uicontrol"> \\ </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nauwkeurigheid </p> </td> 
      <td colname="col2"> <p>Beschikbaar slechts als <span class="uicontrol"> creeer de Beschrijving van de Waaier </span> wordt gecontroleerd en een punt van het Gebied van de <span class="uicontrol"> Waaier wordt </span> geselecteerd. </p> <p>Een geheelwaarde die het aantal cijfers rechts van een decimaal punt specificeert. Dit controleert ook afrondingsverrichtingen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Strip op nullen? </p> </td> 
      <td colname="col2"> <p>Beschikbaar slechts als <span class="uicontrol"> creeer de Beschrijving van de Waaier </span> wordt gecontroleerd, wordt een <span class="uicontrol"> punt van het Gebied van de Waaier geselecteerd en een niet-nul </span> waarde van de Precision <span class="uicontrol"> </span> is geplaatst. </p> <p>Moeten we "0,50" weergeven als ".50"? </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Strip op nullen? </p> </td> 
      <td colname="col2"> <p>Beschikbaar slechts als <span class="uicontrol"> creeer de Beschrijving van de Waaier </span> wordt gecontroleerd, wordt een <span class="uicontrol"> punt van het Gebied van de Waaier geselecteerd en een niet-nul </span> waarde van de Precision <span class="uicontrol"> </span> is geplaatst. </p> <p>Moeten we "10.00" als "10" weergeven? </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Duizenden separators weergeven? </p> </td> 
      <td colname="col2"> <p>Beschikbaar slechts als <span class="uicontrol"> creeer de Beschrijving van de Waaier </span> wordt gecontroleerd en een punt van het Gebied van de <span class="uicontrol"> Waaier wordt </span> geselecteerd. </p> <p>Moeten we "10000" tonen als "10.000"? De locale-specifieke waarden zullen worden gebruikt. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Pas nul waarden aan? </p> </td> 
      <td colname="col2"> <p>Beschikbaar slechts als <span class="uicontrol"> creeer de Beschrijving van de Waaier </span> wordt gecontroleerd en een punt van het Gebied van de <span class="uicontrol"> Waaier wordt </span> geselecteerd. </p> <p>Als afgeronde nulwaarden worden weergegeven, moeten ze dan naar boven of naar beneden worden afgerond volgens de <span class="uicontrol"> Precision- </span> instelling? d.w.z. "0,01" weergeven? </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Test met Greater Than? </p> </td> 
      <td colname="col2"> <p>Beschikbaar slechts als <span class="uicontrol"> creeer de Beschrijving van de Waaier </span> wordt gecontroleerd en een punt van het Gebied van de <span class="uicontrol"> Waaier wordt </span> geselecteerd. </p> <p>Aangezien elke waarde tegen de waarden in de Waarden van de <span class="uicontrol"> Waaier wordt vergeleken </span>, die in <i><b>dalende</b></i> orde wordt verwerkt, wordt het vergeleken, door gebrek, gebruikend de exploitant Groter dan of Gelijk (&gt;=), die ophoudt zodra deze test slaagt. Dit betekent dat met een reeks Waarden van de <span class="uicontrol"> Waaier </span> zoals "10 20 50 100 1000"zal de waarde 100 in de waaier 100 tot 1000 vallen, aangezien 100 inderdaad &gt;= 100 is. Als u liever zou hebben het in waaier 50 tot 100 vallen, controleer deze optie, die de vergelijkingen zal veroorzaken om de exploitant te gebruiken Groter dan (&gt;), in plaats daarvan. </p> <p>Bijvoorbeeld, voor elk van de waarden van dit gebied, wanneer deze optie wordt gecontroleerd: 
      <ul id="ul_969621B1BD914FA5BD73ED21F8841010"> 
      <li id="li_157BEFDA7D0E44C481F4E4BC9046EF24">als de waarde minder dan of gelijk aan (&lt;=) de kleinste waarde in de Waarden van de <span class="uicontrol"> Waaier is </span>, zal het <span class="uicontrol"> "minder dan"Formaat </span> worden gebruikt </li> 
      <li id="li_737EE666CA6243A8864E17A311CF3ACC">als de waarde groter is dan (&gt;) de grootste waarde in de Waarden van de <span class="uicontrol"> Waaier </span>, zal het <span class="uicontrol"> "Grotere dan"Formaat </span> worden gebruikt </li> 
      <li id="li_353A9820F7F74CCCBB3281EC4CB48734">anders, zal een waaier worden gevonden waar de gebiedswaarde tussen twee opeenvolgende Waarden van de <span class="uicontrol"> Waaier </span> (groter dan of gelijk aan (&gt;=) de kleinere waarde en minder dan (&lt;) de grotere waarde) valt, en het <span class="uicontrol"> Tussenliggende Formaat </span> zal worden gebruikt </li> 
    </ul> </p> <p>en, bij ongecontroleerd: 
    <ul id="ul_945844C33C2E4D95A598C4876E15F211"> 
      <li id="li_653B6E2934574DA3B4BCEF07D0A84527">als de waarde minder dan (&lt;) de kleinste waarde in de Waarden van de <span class="uicontrol"> Waaier is </span>, zal het <span class="uicontrol"> "minder dan"Formaat </span> worden gebruikt </li> 
      <li id="li_AECA6880002F40FAB1820B37237550A7">als de waarde groter is dan of gelijk aan (&gt;=) de grootste waarde in de Waarden van de <span class="uicontrol"> Waaier </span>, zal het <span class="uicontrol"> "Grotere dan"Formaat </span> worden gebruikt </li> 
      <li id="li_ECB2DF7CA592497298E9ADC708220366">anders, zal een waaier worden gevonden waar de gebiedswaarde tussen twee opeenvolgende Waarden van de <span class="uicontrol"> Waaier </span> (groter dan (&gt;) de kleinere waarde en minder dan of gelijk aan (&lt;=) de grotere waarde) valt, en het <span class="uicontrol"> Tussenliggende Formaat </span> zal worden gebruikt </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Test </p> </td> 
      <td colname="col2"> <p>Beschikbaar slechts als <span class="uicontrol"> creeer de Beschrijving van de Waaier </span> wordt gecontroleerd en een punt van het Gebied van de <span class="uicontrol"> Waaier wordt </span> geselecteerd. </p> <p>Levert een steekproef numerieke waarde en druk de <span class="uicontrol"> knoop van de Test </span> om te zien hoe het Gebied van de Waaier wordt gecreeerd. De geproduceerde beschrijving van de Waaier zal in het venster worden getoond. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   Zie ook [Toevoegen van een nieuw meta-tagveld](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).
1. Klik op **[!UICONTROL Add]**.
1. (Facultatief) herbouw uw gefaseerde plaatsindex als u aan voorproef de resultaten wilt.

   Zie [het Vormen van een stijgende index van een gefaseerde website](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Facultatief) op de [!DNL Definitions] pagina, doe om het even welke volgend:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Vooraf gedefinieerde of door de gebruiker gedefinieerde meta-tagvelden bewerken {#task_0A7657B63596421BB6DB3ED44F827AB3}

U kunt slechts bepaalde gebieden in vooraf bepaalde meta- markeringen uitgeven, of alle gebieden in meta- markeringen uitgeven die user-defined zijn.

Alvorens de gevolgen van uw veranderingen van de meta- markering aan klanten zichtbaar zijn, moet u uw plaatsindex herbouwen.

**Om vooraf bepaalde of user-defined meta-markeringsgebieden uit te geven**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**.
1. Voor de [!DNL Definitions] pagina, in de [!DNL Actions] kolom van de lijst, klik **[!UICONTROL Edit]** in de rij van de naam van het meta- markeringsgebied die u wilt veranderen.
1. Voor de [!DNL Pinned Keyword Results Manager] pagina, in de lijst, klik **[!UICONTROL Edit]** in de rij van het sleutelwoord dat u wilt veranderen.
1. Voor de [!DNL Edit Field] pagina, plaats de opties die u wilt.

   Als u verkoos om veranderingen in een vooraf bepaald gebied van de meta- markering aan te brengen, me ervan bewust ben dat niet alle gebieden editable zijn.

   Zie de lijst van opties onder het [Toevoegen van een nieuw gebied](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)van de meta- markering.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Facultatief) herbouw uw gefaseerde plaatsindex als u aan voorproef de resultaten wilt.

   Zie [het Vormen van een stijgende index van een gefaseerde website](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Facultatief) op de [!DNL Definitions] pagina, doe om het even welke volgend:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Het schrappen van een user-defined gebied van de meta- markering {#task_9361EF38B5E743038B6672FA6CF70FD3}

U kunt een user-defined gebied van de meta- markering schrappen dat u niet meer nodig hebt of gebruikt.

U kunt vooraf bepaalde meta-tagvelden niet verwijderen. Nochtans, kunt u bepaalde gebieden uitgeven.

Zie Vooraf gedefinieerde of door de gebruiker gedefinieerde meta-tagvelden [bewerken](../c-about-settings-menu/c-about-metadata-menu.md#task_0A7657B63596421BB6DB3ED44F827AB3).

Alvorens de gevolgen van uw schrappings meta-markering aan klanten zichtbaar zijn, moet u uw plaatsindex herbouwen.

**Om een user-defined meta-markeringsgebied te schrappen**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**.
1. Voor de [!DNL Definitions] pagina, in de [!DNL User-defined fields] sectie van lijst, klik **[!UICONTROL Delete]** in de rij van de naam van het meta- markeringsgebied die u wilt verwijderen.
1. Klik in het dialoogvenster Bevestiging op **[!UICONTROL OK]**.
1. (Facultatief) herbouw uw gefaseerde plaatsindex als u aan voorproef de resultaten wilt.

   Zie [het Vormen van een stijgende index van een gefaseerde website](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Facultatief) op de [!DNL Definitions] pagina, doe om het even welke volgend:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Over injecties {#concept_DA091920671948A0A893A26B3A2FAAE5}

U kunt gebruiken [!DNL Injections] om inhoud in uw Web-pagina&#39;s zonder de behoefte op te nemen om de pagina&#39;s zelf uit te geven.

U kunt inhoud aan specifieke geïndexeerde gebieden zoals &quot;doel&quot;of &quot;lichaam&quot;toevoegen, of vervang geïndexeerde inhoud met nieuwe waarden. Bijvoorbeeld, als u nieuwe inhoud in het &quot;doel&quot;meta markeringsgebied opnam, wordt Deze informatie behandeld enkel aangezien het hard-gecodeerde paginacontent zou zijn. U kunt de inhoud van om het even welk vooraf bepaald gebied van de meta- markering uitgeven ongeacht of uw plaatspagina&#39;s overeenkomstige inhoud hebben. Bijvoorbeeld, kunt u de inhoud van de volgende vooraf bepaalde namen van het meta- markeringsgebied uitgeven:

* vlek
* lichaam
* charset
* datum
* desc
* sleutels
* taal
* doelwit
* titel
* url

## Werken met proefveldinjecties {#section_74939EA9E6EA4D2A92E8066B3B11CF92}

U kunt **[!UICONTROL Test]** op de [!DNL Staged Injections] pagina naar keuze gebruiken. U gaat een naam van het testgebied (bijvoorbeeld, &quot;titel&quot;of &quot;lichaam&quot;in), de originele gebiedswaarde (bijvoorbeeld, &quot;Homepage&quot;), en een test URL van uw website. De resulterende waarde wordt getoond voor uw verwijzing. De huidige waarden worden niet tijdens de test gewijzigd.

## Werken met veldinjectiedefinities {#section_C1BBF19DE8EF4A6F8CC3ED691F3953A9}

De definities van injecties hebben de volgende vorm:

```
append|replace field [regexp] URL value
```

De `append|replace`, `field`, `URL`.. en `value` objecten zijn verplicht. U voert per lijn één injectiedefinitie in. Het volgende voorbeeld bevat zes verschillende injectiedefinities.

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
   <th colname="col1" class="entry"> <p>Inspuitdefinitie </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> toevoegen|vervangen </span> </p> </td> 
   <td colname="col2"> <p>Verkies "toevoegen"om de waarde van de injectiedefinitie ("Adobe toe te voegen: Neem contact met ons op of "Nu in de uitverkoop!" in de bovenstaande voorbeelden) op de inhoud van bestaande velden. Verkies "vervangen"om bestaande gebiedsinhoud met de bepaalde waarde te beschrijven. Als een veld momenteel geen inhoud heeft, wordt de gedefinieerde waarde automatisch toegevoegd, ongeacht welke optie (toevoegen of vervangen) wordt gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> veld </span> </p> </td> 
   <td colname="col2"> <p>Een gebiedsnaam wordt vereist. Het volgende is tien vooraf bepaalde gebiedsnamen die u kunt gebruiken: </p> <p> 
     <ul id="ul_B9336FA53023474EAEE399116E7FC972"> 
      <li id="li_C621203DCD2B4875A54A1DD19F0B5B90"> <span class="codeph"> vlek </span> </li> 
      <li id="li_9217E6A037254BEDBB8D006B70D7670D"> <span class="codeph"> lichaam </span> </li> 
      <li id="li_DCDC50F93F224F02897419B745E09399"> <span class="codeph"> charset </span> </li> 
      <li id="li_D95668236B6547B99966668C82B302AB"> <span class="codeph"> datum </span> </li> 
      <li id="li_D2071681274345C3B97E9ADA6D223271"> <span class="codeph"> desc </span> </li> 
      <li id="li_26683A9209454A438D811187FB929482"> <span class="codeph"> sleutels </span> </li> 
      <li id="li_A5E19F81B872402CA62B5AB9497E030D"> <span class="codeph"> taal </span> </li> 
      <li id="li_FD0B1CD9E6304B18B9D7F57E61015107"> <span class="codeph"> doelwit </span> </li> 
      <li id="li_400D7E3F3E9B47EFB2FF5C0D278DB573"> <span class="codeph"> titel </span> </li> 
      <li id="li_449BCBEE4F64424BB69F780C10F5956C"> <span class="codeph"> url </span> </li> 
     </ul> </p> <p>Elke gebiedsnaam beantwoordt aan elementen op uw plaatspagina's. Als u bijvoorbeeld de naam van het veld <span class="codeph"> </span> desc opgeeft, kunt u de waarde van de injectiedefinitie toevoegen aan het veld dat overeenkomt met de beschrijving Meta-tags op uw site-pagina's. </p> <p>Als geen beschrijving van de markering van Meta op uw pagina's bestaat, leidt de bepaalde inhoud tot de markering voor u. De inhoud die in een <span class="codeph"> desc- </span> injectievertoningen op uw resultatenpagina wordt gespecificeerd enkel zoals hard-gecodeerde inhoud Meta-Beschrijving zou. </p> <p>U kunt veelvoudige definities met de zelfde gebiedsnaam ook tot stand brengen. Bijvoorbeeld, verondersteld u de volgende injecties hebt: </p> <p> <code> replace&nbsp; <b>title</b>&nbsp;https://www.mysite.com/&nbsp;Welcome&nbsp;to&nbsp;My&nbsp;Site </code> </p> <p> <code> replace&nbsp; <b>title</b>&nbsp;https://www.mysite.com/company/*.html&nbsp;My&nbsp;Site:&nbsp;Contact </code> </p> <p>Alle pagina's op de site in het bovenstaande voorbeeld krijgen een geïnjecteerde titel "Welkom bij mijn site". Pagina's in de map "/company/" worden geïnjecteerd met een nieuwe titel "My Site: Contact met ons opnemen", dat de vorige vervangt. </p> <p>Merk op dat injecties worden toegepast in de volgorde waarin ze worden weergegeven in het tekstvak <span class="wintitle"> Veldinjectiedefinities </span> . Als het zelfde gebied ("titel"in dit voorbeeld) meer dan eens voor pagina's bij de zelfde plaats wordt bepaald, neemt de recentere definitie belangrijkheid. </p> <p> <span class="codeph"> [regexp] </span> - optioneel. Als u verkiest om de <span class="codeph"> regexp </span> optie te gebruiken, wordt bepaalde URL behandeld als regelmatige uitdrukking. </p> <p>Zie <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Regelmatige expressies </a>. </p> <p>In de volgende definitie: </p> <p> <code> replace&nbsp;target&nbsp; <b>regexp&amp;nbsp;^.*/products/.*\.html$</b>&nbsp;Important&nbsp;information </code> </p> <p> "Belangrijke informatie" wordt in het veld "doel" geïnjecteerd op alle pagina's die overeenkomen met de reguliere expressie <span class="codeph"> ^.*/producten/.*\.html$ </span>. </p> <p>Daarom hebt u het volgende: </p> <p> <code> https://www.mydomain.com/products/page1.html 
      &nbsp;&nbsp;&nbsp;&nbsp;(Will&nbsp;receive&nbsp;"target"&nbsp;content) </code> </p> <p> <code> https://www.mydomain.com/product/oldstuff.html 
      &nbsp;&nbsp;&nbsp;&nbsp;(Will&nbsp;not&nbsp;receive&nbsp;"target"&nbsp;content) </code> </p> <p>In het volgende voorbeeld: </p> <p> <code> append&amp;nbsp;title&amp;nbsp;regexp&amp;nbsp;^.*\.pdf$&amp;nbsp;Millennium&amp;nbsp;Science </code> </p> <p>De injectie voegt "Millennium Science" toe aan de "title"-inhoud van alle pagina's die eindigen met een filename extensie ".pdf". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> URL </span> </p> </td> 
   <td colname="col2"> <p>Een URL wordt vereist en specificeert welke documenten worden ingespoten. </p> <p>URL is om het even welke volgend: </p> <p> 
     <ul id="ul_C5C74F6D5EA943B293742989EB822751"> 
      <li id="li_382392DB778D4E14BFFC96D35A861951"> Een volledige weg, zoals in https://www.mydomain.com/products.html </li> 
      <li id="li_EA2BD0FB66A44CD0844613316F6174D4"> Een gedeeltelijke weg, zoals in https://www.mydomain.com/products </li> 
      <li id="li_D5E0D6D897C8493ABBFC65517CD4A7DB"> Een URL die wilde kaarten gebruikt, zoals in https://www.mydomain.com/*.html </li> 
     </ul> </p> <p>De waarde URL moet geen ruimtekarakters in het hebben. Als de <span class="codeph"> regexp </span> optie wordt gebruikt, wordt URL behandeld als een regelmatige uitdrukking. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> waarde </span> </p> </td> 
   <td colname="col2"> <p>Een waarde wordt vereist en wordt gebruikt om of aan bestaande gebiedsinhoud te vervangen of toe te voegen. U kunt veelvoudige waarden voor de zelfde gebiedsnaam specificeren. Bijvoorbeeld: </p> <p>voeg <b>sleutels</b> toe https://www.mysite.com/travel/ <b>zomer</b>, <b>strand</b>, <b>zand</b> </p> <p>voeg <b>sleutels</b> toe https://www.mysite.com/travel/fare/*.html <b>goedkope tickets</b> </p> <p>In het bovenstaande voorbeeld worden de woorden "zomer, strand, zand" toegevoegd aan het veld "keys" op alle pagina's in de directory "/travel/". De woorden "goedkope tickets" worden ook toegevoegd aan het veld "sleutels" op alle pagina's in de directory "/reis/fare/". </p> </td> 
  </tr> 
 </tbody> 
</table>

Zie ook het [Selecteren van inhoudstypes om te kruipen en index](../c-about-settings-menu/c-about-crawling-menu.md#task_CCAC5C67C8BF4AB7B79D34A1495D5EE8).

## Toevoeging van definities van veldinspuiting {#task_E86566FA1FF74CF68115C0ADA05172AE}

U kunt gebruiken [!DNL Injections] om inhoud in uw Web-pagina&#39;s zonder de behoefte op te nemen om de pagina&#39;s zelf uit te geven.

U kunt **[!UICONTROL Test]** op de [!DNL Injections] pagina naar keuze gebruiken. U gaat een naam van het testgebied (bijvoorbeeld, &quot;titel&quot;of &quot;lichaam&quot;in), de originele gebiedswaarde (bijvoorbeeld, &quot;Homepage&quot;), en een test URL van uw website. De resulterende waarde wordt getoond voor uw verwijzing. De huidige waarden worden niet tijdens de test gewijzigd.

**Om gebiedsinjectiedefinities toe te voegen**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Injections]**.
1. (Facultatief) op de [!DNL Injections] pagina, op het [!DNL Test Field Injections] gebied, ga het testgebied, de test originele waarde, en test URL in, en klik dan **[!UICONTROL Test]**.
1. Voer in het [!DNL Field Injection Definitions] veld één injectiedefinitie per lijn in.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Facultatief) doe om het even welke volgend:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Over Attribuutlader {#concept_9EF38E98811B42CDA41996432B9AD209}

Gebruik [!DNL Attribute Loader] om extra inputbronnen te bepalen om gegevens te vergroten die van een website worden gekropen.

>[!NOTE]
>
>Om de Lader van Attributen te gebruiken, kunt u het moeten hebben toegelaten in uw rekening door uw de rekeningsvertegenwoordiger van Adobe of door de Steun van Adobe.

U kunt een inputbron van de gegevensvoer gebruiken om tot inhoud toegang te hebben die in een vorm wordt opgeslagen die van verschillend is wat typisch op een website wordt ontdekt. U doet dit gebruikend één van beschikbaar kruipt methodes. De gegevens uit deze bronnen kunnen dan in gegevens van gekropen inhoud worden geïnjecteerd.

Nadat u een definitie van de Lader van Attributen aan de [!DNL Staged Attribute Loader Definitions] pagina toevoegt, kunt u om het even welke configuratie veranderen plaatsend behalve de waarden van de Naam en de waarden van het Type

De [!DNL Attribute Loader] pagina toont u de volgende informatie:

* De naam van de bepaalde configuratie van de Lader van Attributen die u hebt gevormd en toegevoegd.
* Één van de volgende gegevensbrontypes voor elke schakelaar die u hebt toegevoegd:

   * **Tekst** - Eenvoudige &quot;vlakke&quot;dossiers, komma-afgebakend, lusje-afgebakend, of andere constant afgebakende formaten.
   * **Voeder** - XML-feeds.

* Of de configuratie of niet voor volgende wordt toegelaten kruip en het indexeren.
* Het adres van de gegevensbron.

Zie ook [Hoe het proces van de attributeninjectie voor Tekst en Diervoeders.. werkt..](../c-about-settings-menu/c-about-metadata-menu.md#section_E059A33D61EE4DB0972A37B8A35E9E16)

Zie ook [over het vormen van de veelvoudige Lagers van Attributen](../c-about-settings-menu/c-about-metadata-menu.md#section_4CC49C74EF294608A184E233F215ADFF)

Zie ook [over het gebruik van Voorproef wanneer u een Attribuut... toevoegt.](../c-about-settings-menu/c-about-metadata-menu.md#section_E9CAB000A94C4D9189786C1EDB1CDB46)

## Hoe het proces van de attributeninjectie voor de configuraties van de Tekst en van het Diervoer in de Lader van Attributen werkt {#section_E059A33D61EE4DB0972A37B8A35E9E16}

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
   <td colname="col3"> <p>Voor de configuraties van de Tekst en van het Diervoer, is het een eenvoudige dossierdownload. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>Onderdeel de gedownloade gegevensbron in individuele pseudo-documenten. </p> </td> 
   <td colname="col3"> <p>Voor <span class="uicontrol"> Tekst </span>, beantwoordt elke newline-afgebakende lijn van tekst aan een individueel document, en ontleed gebruikend de gespecificeerde afbakening, zoals een komma of een tabel. </p> <p>Voor <span class="uicontrol"> diervoeders </span>, worden de gegevens van elk document gehaald gebruikend een regelmatig uitdrukkingspatroon in de volgende vorm: </p> <p> <code class="syntax js"> &lt;${Itemtag}&gt;(.*?)&lt;/${Itemtag}&gt; </code> </p> <p>Gebruikend <span class="uicontrol"> Kaart </span> op de <span class="wintitle"> Lader van Attributen voeg </span> pagina toe, creeer een caching exemplaar van de gegevens en creeer dan een lijst van verbindingen voor crawler. Het gegeven wordt opgeslagen in een lokaal geheime voorgeheugen en bevolkt met de gevormde gebieden. </p> <p>Het ontlede gegeven wordt geschreven aan het lokale geheime voorgeheugen. </p> <p>Dit geheime voorgeheugen wordt gelezen later om de eenvoudige documenten van HTML tot stand te brengen nodig door kruipper. Bijvoorbeeld: </p> <p> <code class="syntax html"> &lt;html&gt;&lt;head&gt; 
      &lt;title&gt;{title}&lt;/title&gt; 
      &lt;meta&nbsp;name="{field}"&nbsp;content="{data}"&nbsp;/&gt; 
      ... 
      &lt;/head&gt;&lt;body&gt; 
      {body} 
      &lt;/body&gt;&lt;/html&gt; </code> </p> <p>Het <span class="codeph"> &lt;title&gt; </span> element wordt slechts geproduceerd wanneer een afbeelding aan het de meta-gegevensgebied van de Titel bestaat. Op dezelfde manier wordt het <span class="codeph"> &lt;body&gt; </span> element slechts geproduceerd wanneer een afbeelding aan het de meta-gegevensgebied van het Lichaam bestaat. </p> <p> <b>Belangrijk</b>: De toewijzing van waarden aan de vooraf bepaalde meta-markering URL wordt niet gesteund. </p> <p>Voor alle andere afbeeldingen, worden <span class="codeph"> &lt;meta&gt; </span> markeringen geproduceerd voor elk gebied dat gegevens heeft die in het oorspronkelijke document worden gevonden. </p> <p>De gebieden voor elk document worden toegevoegd aan het geheime voorgeheugen. Voor elk document dat aan het geheime voorgeheugen wordt geschreven, wordt een verbinding ook geproduceerd zoals in de volgende voorbeelden: </p> <p> <code class="syntax html"> &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      .... </code> </p> <p>De afbeelding van de configuratie moet één gebied hebben dat als Primaire Sleutel wordt geïdentificeerd. Deze afbeelding vormt de sleutel die wordt gebruikt wanneer het gegeven van het geheime voorgeheugen wordt gehaald. </p> <p>crawler herkent de URL- <span class="codeph"> index: </span> de regelprefix, die tot de plaatselijk caching gegevens kan dan toegang hebben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>kruip de caching documentreeks. </p> </td> 
   <td colname="col3"> <p>De <span class="codeph"> index: de </span> verbindingen worden toegevoegd aan de hangende lijst van de kruippakje, en in de normale kruipende opeenvolging verwerkt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>Elk document verwerken. </p> </td> 
   <td colname="col3"> <p>De belangrijkste waarde van elke verbinding beantwoordt aan een ingang in het geheime voorgeheugen, zo kruipend resulteert elke verbinding in de gegevens die van dat document van het geheime voorgeheugen worden gehaald. Het wordt dan "geassembleerd"in een beeld van HTML dat wordt verwerkt en aan de index toegevoegd. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Over het vormen van veelvoudige Lagers van Attributen {#section_4CC49C74EF294608A184E233F215ADFF}

U kunt de veelvoudige configuraties van de Lader van Attributen voor om het even welke rekening bepalen.

Wanneer u een Lader van Attributen toevoegt, kunt u de eigenschap naar keuze gebruiken **[!UICONTROL Setup Maps]** om een steekproef van uw gegevensbron te downloaden. De gegevens worden op geschiktheid onderzocht.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Type Attribuutlader </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Tekst </p> </td> 
   <td colname="col2"> <p>Bepaalt de afbakeningswaarde door lusjes eerst te proberen, dan verticaal-bars ( <span class="codeph"> | </span>) en ten slotte komma's ( <span class="codeph"> , </span>). Als u reeds een afbakeningswaarde alvorens u <span class="uicontrol"> de Kaarten van de Opstelling klikte </span>, wordt die waarde gebruikt in plaats daarvan. </p> <p>De best-geschikte regeling resulteert in de gebieden van de Kaart die met gokken bij de aangewezen waarden van de Markering en van het Gebied worden ingevuld. Bovendien, wordt een steekproef van de ontlede gegevens getoond. Ben zeker om <span class="uicontrol"> Kopballen in Eerste Rij te selecteren </span> als u weet dat het dossier een kopbalrij omvat. De opstellingsfunctie gebruikt deze informatie om de resulterende kaartingangen beter te identificeren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Diervoeders </p> </td> 
   <td colname="col2"> <p>Downloadt de gegevensbron en voert het eenvoudige ontleden van XML uit. </p> <p>De resulterende herkenningstekens van XPath worden getoond in de rijen van de Markering van de lijst van de Kaart, en gelijkaardige waarden in Gebieden. Deze rijen identificeren slechts de beschikbare gegevens, en produceren niet de ingewikkeldere definities van XPath. Nochtans, is het nog nuttig omdat het de gegevens van XML beschrijft en ItemTag identificeert. </p> <p> <p>Opmerking:  De functie van de Kaarten van de Opstelling downloadt de volledige bron van XML om zijn analyse uit te voeren. Als het dossier groot is, kon deze verrichting uit tijd worden. </p> </p> <p>Wanneer succesvol, identificeert deze functie alle mogelijke punten van XPath, veel waarvan niet wenselijk zijn te gebruiken. Zeker ben dat u de resulterende definities van de Kaart onderzoekt en degenen verwijdert die u niet nodig hebt of wilt. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>De eigenschap van de Kaarten van de Opstelling kan niet voor grote de gegevensreeksen van XML werken omdat zijn dossiersyntactische parser probeert om het volledige dossier in geheugen te lezen. Als gevolg hiervan kon je een &#39;out-of-memory&#39; aandoening ervaren. Nochtans, wanneer het zelfde document op het tijdstip van het indexeren wordt verwerkt, wordt het niet gelezen in geheugen. In plaats daarvan, worden de grote documenten &quot;onderweg,&quot;verwerkt en niet volledig in geheugen eerst gelezen.

## Ongeveer het gebruik van Voorproef wanneer u een Lader van Attributen toevoegt {#section_E9CAB000A94C4D9189786C1EDB1CDB46}

De gegevens van de Lader van attributen worden geladen voorafgaand aan een verrichting van de Index.

Op het ogenblik dat u een Lader van Attributen toevoegt, kunt u de eigenschap naar keuze gebruiken **[!UICONTROL Preview]** om de gegevens te bevestigen, alsof u het opsloeg. Het stelt een test tegen de configuratie in werking, maar zonder de configuratie aan de rekening te bewaren. De test heeft toegang tot de gevormde gegevensbron. Nochtans, schrijft het het downloadgeheime voorgeheugen aan een tijdelijke plaats; het botst niet met de belangrijkste geheim voorgeheugenomslag die het indexeren kruipt gebruikt.

De voorproef verwerkt slechts een gebrek van vijf documenten zoals die door **Acct worden gecontroleerd:IndexConnector-Voorproef-Maximum-Documenten**. De previewed documenten worden getoond in bronvorm, aangezien zij aan het indexeren kruipper worden voorgesteld. De vertoning is gelijkaardig aan een &quot;Bron van de Mening&quot;eigenschap in browser van het Web. U kunt de documenten in de voorproefreeks navigeren gebruikend standaardnavigatiekoppelingen.

De voorproef steunt de geen configuraties van XML omdat dergelijke documenten direct worden verwerkt en niet aan het geheime voorgeheugen worden gedownload.

## Het toevoegen van een definitie van de Lader van Attributen {#task_A735E5EF763343A9B675E1A3B09AFDBC}

Elke configuratie van de Lader van Attributen bepaalt een gegevensbron en afbeeldingen om de gegevenspunten te relateren die voor die bron aan meta-gegevensgebieden in de index worden bepaald.

>[!NOTE]
>
>Om de Lader van Attributen te gebruiken, kunt u het moeten hebben toegelaten in uw rekening door uw de rekeningsvertegenwoordiger van Adobe of door de Steun van Adobe.

Alvorens de gevolgen van de nieuwe en toegelaten definitie aan klanten zichtbaar zijn, herbouw uw plaatsindex.

**Om een definitie van de Lader van Attributen toe te voegen**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Voor de [!DNL Stage Attribute Loader Definitions] pagina, klik **[!UICONTROL Add New Attribute Loader]**.
1. Voor de [!DNL Attribute Loader Add] pagina, plaats de configuratieopties die u wilt. De opties die beschikbaar zijn hangen van af **[!UICONTROL Type]** die u selecteerde.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Optie </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Naam </p> </td> 
      <td colname="col2"> <p>De unieke naam van de configuratie van de Lader van Attributen. U kunt alfanumerieke karakters gebruiken. De tekens "_" en "-" zijn ook toegestaan. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Type </p> </td> 
      <td colname="col2"> <p>De bron van uw gegevens. Het gegevenstype dat u selecteert beïnvloedt de resulterende opties die op de <span class="wintitle"> Lader van Attributen beschikbaar zijn voegt </span> pagina toe. U kunt van het volgende kiezen: </p> <p> 
      <ul id="ul_1ADC3DFBC929467385F7465BE8E13635"> 
      <li id="li_64FCD749F55442BAB316BD474128D4F9"> <span class="uicontrol"> Tekst </span> <p>Eenvoudige vlakke tekstdossiers, komma-afgebakend, lusje-afgebakend, of andere constant afgebakende formaten. Elke newline-afgebakende lijn van tekst beantwoordt aan een individueel document, en ontleed gebruikend de gespecificeerde afbakening. </p> <p>U kunt elke waarde, of kolom, aan een meta-gegevensgebied in kaart brengen, dat door het kolomaantal van verwijzingen wordt voorzien, dat bij 1 (begint). </p> </li> 
      <li id="li_2A4F16CE6DCE4114B7F8E4FE156252BB"> <span class="uicontrol"> Diervoeders </span> <p>Downloadt een hoofddocument van XML dat veelvoudige "rijen"van informatie bevat. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>Type gegevensbron: Tekst</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ingeschakeld </p> </td> 
      <td colname="col2"> <p>Zet de configuratie "aan"voor gebruik. Of, u kunt "van"de configuratie uitzetten om te verhinderen als wordt gebruikt. </p> <p> <b>Opmerking</b>: De gehandicapte configuraties van de Lader van Attributen worden genegeerd. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Hostadres </p> </td> 
      <td colname="col2"> <p>Specificeert het adres van de servergastheer waar uw gegevens worden gevestigd. </p> <p>Indien gewenst, kunt u een volledige weg van URI (het Eenvormige Herkenningsteken van het Middel) aan het gegevensbrondocument specificeren zoals in de volgende voorbeelden: </p> <p> <code otherprops="syntax html"> https://www.somewhere.com/some_path/some_file.tsv </code> </p> <p>of </p> <p> <code class="syntax html"> ftp://user:password@ftpserver.somewhere.com/some_path/some_file.csv </code> </p> <p>URI wordt verdeeld in de aangewezen ingangen voor het Adres van de Gastheer, de Weg van het Dossier, het Protocol, en, naar keuze, Gebruikersbenaming, en de gebieden van het Wachtwoord </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Bestandspad </p> </td> 
      <td colname="col2"> <p>Specificeert de weg aan het eenvoudige vlakke tekstdossier, komma-afgebakend, lusje-afgebakend, of ander constant afgebakend formaatdossier. </p> <p>De weg is met betrekking tot de wortel van het gastheeradres. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocol </p> </td> 
      <td colname="col2"> <p>Specificeert het protocol dat wordt gebruikt om tot het dossier toegang te hebben. U kunt van het volgende kiezen: </p> <p> 
      <ul id="ul_F6BC10FD51CA4A1D855B2B3212838A9C"> 
      <li id="li_79FB7DC65E774ABBB23E57BF98AD9738"> HTTP <p>Indien nodig, kunt u juiste authentificatiegeloofsbrieven ingaan om tot de server van HTTP toegang te hebben. </p> </li> 
      <li id="li_BAA9AD5E4B014E09B3A66C94022B7225"> HTTPS <p>Indien nodig, kunt u juiste authentificatiegeloofsbrieven ingaan om tot de server toegang te hebben HTTPS. </p> </li> 
      <li id="li_E716ABB169DD408BA91F1CA27F445A16"> FTP <p>U moet juiste authentificatiegeloofsbrieven ingaan om tot de server van FTP toegang te hebben. </p> </li> 
      <li id="li_FD7143019C5244C3B8A5B1B5AA84859A"> SFTP <p>U moet juiste authentificatiegeloofsbrieven ingaan om tot de server toegang te hebben SFTP. </p> </li> 
      <li id="li_38E0036C1365419F9D00083CACA34AFB"> Bestand </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Onderbreking </p> </td> 
      <td colname="col2"> <p>Specificeert de onderbreking, in seconden, voor FTP, SFTP, HTTP of verbindingen HTTPS. Deze waarde moet tussen 30 en 300 zijn. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Retries </p> </td> 
      <td colname="col2"> <p>Specificeert het maximumaantal pogingen voor ontbroken verbindingen FTP, SFTP, HTTP of HTTPS opnieuw. Deze waarde moet tussen 0 en 10 zijn. </p> <p>Een waarde van nul (0) zal herhalingspogingen verhinderen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Codering </p> </td> 
      <td colname="col2"> <p>Specificeert het karakter het coderen systeem dat in het gespecificeerde gegevensbrondossier wordt gebruikt. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Afbakening </p> </td> 
      <td colname="col2"> <p>Specificeert het karakter dat u wilt gebruiken om elk gebied in het gespecificeerde gegevensbrondossier te afbakenen. </p> <p>Het komma karakter ( <span class="codeph"> , </span>) is een voorbeeld van een afbakening. De komma doet dienst als gebiedsafbakening die helpt om gegevensgebieden in uw gespecificeerd gegevensbrondossier te scheiden. </p> <p>Selecteer <span class="uicontrol"> Tab? </span> om het horizontale lusjekarakter als afbakening te gebruiken. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Koppen in de Eerste rij </p> </td> 
      <td colname="col2"> <p>Wijst erop dat de eerste rij in het gegevensbrondossier kopbalinformatie slechts, niet gegevens bevat. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Stale dagen </p> </td> 
      <td colname="col2"> <p>Plaatst het minimuminterval tussen downloads van de gegevens van de Lader van Attributen. De index-teweeggebrachte downloads die binnen de download voorkomen verfrissen frequentieinterval worden genegeerd. Wanneer u deze waarde aan het gebrek van 1 plaatst, downloadt de gegevens van de Lader van Attributen niet meer dan eens binnen een periode van 24 uur. Alle indexen van het Onderzoek die binnen de download voorkomen verfrissen frequentieinterval gebruik de laatste gegevensreeks die werd gedownload. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Kaart </p> </td> 
      <td colname="col2"> <p>Specificeert kolom-aan-meta-gegevensafbeeldingen, gebruikend kolomaantallen. </p> <p> 
      <ul id="ul_981AE2C6D30443BDBFC6575D413732A2"> 
      <li id="li_A42CB9DFFF8C45A7BAC2D471FE96CEBE"> <span class="uicontrol"> Kolom </span> <p> Specificeert een kolomaantal, met de eerste kolom die 1 (één) zijn. Om nieuwe kaartrijen voor elke kolom, onder <span class="wintitle"> Actie toe te voegen </span>, klik <span class="uicontrol"> + </span>. </p> <p>U te hoeven niet om elke kolom in de gegevensbron van verwijzingen te voorzien. In plaats daarvan, kunt u verkiezen om waarden over te slaan. </p> </li> 
      <li id="li_26E8C9554A5D4BC5A5073D6385E3626F"> <span class="uicontrol"> Veld </span> <p>Bepaalt de waarde van de naamattributen die voor elke geproduceerde &lt;meta&gt; markering wordt gebruikt. </p> </li> 
      <li id="li_5DFA514B7F9549B98D6CBC095A66033C"> <span class="uicontrol"> Metagegevens? </span> <p>Veroorzaakt <span class="uicontrol"> Gebied </span> om een drop-down lijst te worden waarvan u bepaalde meta-gegevensgebieden voor de huidige rekening kunt selecteren. </p> <p>De <span class="uicontrol"> waarde van het Gebied </span> kan een niet gedefiniëerd meta-gegevensgebied zijn, indien gewenst. Een niet gedefiniëerd meta-gegevensgebied is soms nuttig om inhoud tot stand te brengen die door een <span class="wintitle"> Filtrerend Manuscript wordt gebruikt </span>. </p> <p>Zie <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> over Filtrerend Manuscript </a>. </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892C95"> <span class="uicontrol"> Primaire sleutel? </span> <p>Slechts één gebied wordt geïdentificeerd als primaire sleutel. Dit gebied zal als "buitenlandse sleutel"worden gebruikt om de gegevens van de Lader van Attributen met het overeenkomstige document in de index aan te passen. </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892D96"> <span class="uicontrol"> HTML strippen? </span> <p>Wanneer deze optie wordt gecontroleerd, worden om het even welke markeringen van HTML die in de gegevens van dit gebied worden gevonden verwijderd. </p> </li> 
      <li id="li_359D2902859B4C5BADB0BA26F0BA4DC0"> <span class="uicontrol"> Actie </span> <p>Laat u rijen aan de kaart toevoegen of rijen verwijderen uit de kaart. De orde van de rijen is niet belangrijk. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>Type gegevensbron: Diervoeders</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ingeschakeld </p> </td> 
      <td colname="col2"> <p>Zet de configuratie "aan"voor gebruik. Of, u kunt "van"de configuratie uitzetten om te verhinderen als wordt gebruikt. </p> <p> <b>Opmerking</b>: De gehandicapte configuraties van de Lader van Attributen worden genegeerd. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Hostadres </p> </td> 
      <td colname="col2"> <p>Specificeert het adres van de servergastheer waar uw gegevens worden gevestigd. </p> <p>Indien gewenst, kunt u een volledige weg van URI (het Eenvormige Herkenningsteken van het Middel) aan het gegevensbrondocument specificeren zoals in de volgende voorbeelden: </p> <p> <code class="syntax html"> https://www.somewhere.com/some_path/some_file.tsv </code> </p> <p>of </p> <p> <code class="syntax html"> ftp://user:password@ftpserver.somewhere.com/some_path/some_file.csv </code> </p> <p>URI wordt verdeeld in de aangewezen ingangen voor het Adres van de Gastheer, de Weg van het Dossier, het Protocol, en, naar keuze, Gebruikersbenaming, en de gebieden van het Wachtwoord. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Bestandspad </p> </td> 
      <td colname="col2"> <p>Specificeert de weg aan het hoofddocument van XML dat veelvoudige "rijen"van informatie bevat. </p> <p>De weg is met betrekking tot de wortel van het gastheeradres. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocol </p> </td> 
      <td colname="col2"> <p>Specificeert het protocol dat wordt gebruikt om tot het dossier toegang te hebben. U kunt van het volgende kiezen: </p> <p> 
      <ul id="ul_976A34FD14A841F2B610C1C0CCBB82B9"> 
      <li id="li_05BBA0F670F14431A89AE4178F1A6F94"> HTTP <p>Indien nodig, kunt u juiste authentificatiegeloofsbrieven ingaan om tot de server van HTTP toegang te hebben. </p> </li> 
      <li id="li_100446691F304572B8FC3F083F86A2CB"> HTTPS <p>Indien nodig, kunt u juiste authentificatiegeloofsbrieven ingaan om tot de server toegang te hebben HTTPS. </p> </li> 
      <li id="li_027088A8E30444DAA8CCCC5B0BAA74C1"> FTP <p>U moet juiste authentificatiegeloofsbrieven ingaan om tot de server van FTP toegang te hebben. </p> </li> 
      <li id="li_DCEF9D5C99354990B03E29083C2ED8DC"> SFTP <p>U moet juiste authentificatiegeloofsbrieven ingaan om tot de server toegang te hebben SFTP. </p> </li> 
      <li id="li_44E34FF2AB0D429EB3408106E6FCF780"> Bestand </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Item </p> </td> 
      <td colname="col2"> <p>Identificeert het element van XML dat u kunt gebruiken om de individuele lijnen van XML in het gegevensbrondossier te identificeren dat u specificeerde. </p> <p>Bijvoorbeeld, in het volgende fragment van het Diervoer van een document van Adobe XML, is de waarde van het Punt <span class="codeph"> verslag </span>: </p> <p> <code class="syntax xml"> &lt;?xml&nbsp;version="1.0"&nbsp;encoding="utf-8"?&gt; 
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
      <td colname="col2"> <p>Specificeert een meta-gegevensgebied de waarvan waarden als raadpleging "sleutels"in de gegevens van de configuratie van de Lader van Attributen worden gebruikt. Als geen waarde wordt geselecteerd (<b>-niets-</b>), is het gegeven van deze configuratie niet beschikbaar voor gebruik in het Rangschikken van berekeningen (<b>Regels</b> &gt; <b>Rangschikkende Regels</b> &gt; <b>geef Regels</b>uit). Wanneer u een waarde selecteert, worden de waarden van dit gebied gebruikt om plaatsonderzoek/merchandising documenten met de gegevens van deze configuratie te vergelijken. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Stale dagen </p> </td> 
      <td colname="col2"> <p>Plaatst het minimuminterval tussen downloads van de gegevens van de Lader van Attributen. De index-teweeggebrachte downloads die binnen de download voorkomen verfrissen frequentieinterval worden genegeerd. Wanneer u deze waarde aan het gebrek van 1 plaatst, downloadt de gegevens van de Lader van Attributen niet meer dan eens binnen een periode van 24 uur. Alle indexen van het Onderzoek die binnen de download voorkomen verfrissen frequentieinterval gebruik de laatste gegevensreeks die werd gedownload. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Kaart </p> </td> 
      <td colname="col2"> <p>Laat u XML-element-aan-meta-gegevensafbeeldingen specificeren, gebruikend de uitdrukkingen van XPath. </p> <p> 
      <ul id="ul_604108C0277C4892AE8A40CA39889ABD"> 
      <li id="li_0AF92270AE9F4BA8B2C7EE41FABC0F34"> <span class="uicontrol"> Markering </span> <p>Specificeert een vertegenwoordiging van XPath van de ontlede gegevens van XML. Gebruikend het document van voorbeeldAdobe XML hierboven, onder de optieItem, kon het worden in kaart gebracht gebruikend de volgende syntaxis: </p> <p> <code class="syntax xml"> /record/@displayurl&nbsp;-&gt;&nbsp;page-url 
        /record/metadata/meta[@name='title']/@content&nbsp;-&gt;&nbsp;title 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;desc 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;body </code> </p> <p>De bovengenoemde syntaxis vertaalt als het volgende: </p> <p> 
        <ul id="ul_6400EBD08D424EADA1612FE4F7EFB640"> 
        <li id="li_9958F9B40D42434195597DBA9F2AF28F"> <code class="syntax xml"> /record/@displayurl&amp;nbsp;-&gt;&amp;nbsp;page-url </code> <p>Het <span class="codeph"> vertoningsattribuut </span> van het <span class="codeph"> verslag </span> elementenkaarten aan het meta-gegevensgebied pagina-url <span class="codeph"> </span>. </p> </li> 
        <li id="li_759013EA02CD48BE971A55B0A6A11424"> <code class="syntax xml"> /record/metadata/meta[@name='title']/@content&amp;nbsp;-&gt;&amp;nbsp;title </code> <p>Het <span class="codeph"> inhoudsattribuut </span> van om het even welk <span class="codeph"> meta- </span> element dat binnen een <span class="codeph"> meta-gegevenselement bevat is, dat binnen een </span> verslag- <span class="codeph"> element bevat is, de waarvan naamattribuut </span> titel is, kaarten aan de  titel van het meta-gegevensgebied in kaart brengen <span class="codeph"> </span><span class="codeph"> </span>. </p> </li> 
        <li id="li_E741CA59197D462EB2946EDE874AFDC8"> <code class="syntax xml"> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;desc </code> <p>Het <span class="codeph"> inhoudsattribuut </span> van om het even welk <span class="codeph"> meta- </span> element dat binnen een <span class="codeph"> meta-gegevenselement bevat is, dat binnen het </span> verslag- <span class="codeph"> element bevat is, de waarvan naamattribuut </span> <span class="codeph"> </span><span class="codeph"> </span>beschrijving is, kaarten aan het meta-gegevensgebied desc. </p> </li> 
        <li id="li_E35EAE3D284D46D485D9064D7BB6AB13"> <code class="syntax xml"> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;body </code> <p>Het <span class="codeph"> inhoudsattribuut </span> van om het even welk <span class="codeph"> meta- </span> element dat binnen een <span class="codeph"> meta-gegevenselement bevat is, dat binnen het </span> verslag- <span class="codeph"> element bevat is, de waarvan naam het attribuut </span> beschrijving is, kaarten aan het  lichaam van het meta-gegevensgebied in kaart brengt <span class="codeph"> </span><span class="codeph"> </span>. </p> </li> 
        </ul> </p> <p>XPath is een vrij ingewikkelde aantekening. Meer informatie is beschikbaar op de volgende plaats: </p> <p>Zie <a href="https://www.w3schools.com/xpath/" scope="external" format="html"> https://www.w3schools.com/xpath/ </a> </p> </li> 
      <li id="li_8147075D7ACD4811A7ED335F23FE62A6"> <span class="uicontrol"> Veld </span> <p>Bepaalt de waarde van de naamattributen die voor elke geproduceerde <span class="codeph"> &lt;meta&gt; </span> markering wordt gebruikt. </p> </li> 
      <li id="li_2380199D63BF425A919606D8232FA6E2"> <span class="uicontrol"> Metagegevens? </span> <p>Veroorzaakt <span class="uicontrol"> Gebied </span> om een drop-down lijst te worden waarvan u bepaalde meta-gegevensgebieden voor de huidige rekening kunt selecteren. </p> <p>De <span class="uicontrol"> waarde van het Gebied </span> kan een niet gedefiniëerd meta-gegevensgebied zijn, indien gewenst. Een niet gedefiniëerd meta-gegevensgebied is soms nuttig om inhoud tot stand te brengen die door Manuscript wordt gebruikt te <span class="wintitle"> filtreren </span>. </p> <p>Zie <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> over Filtrerend Manuscript </a>. </p> <p>Wanneer de Lader van Attributen de documenten van XML met veelvoudige klappen op om het even welk kaartgebied verwerkt, worden de veelvoudige waarden aaneengeschakeld in één enkele waarde in het resulterende caching document. Door gebrek, worden deze waarden gecombineerd gebruikend een komma afbakening. Nochtans, veronderstel dat de overeenkomstige <span class="wintitle"> </span> waarde van het Gebied een bepaald meta-gegevensgebied is. Bovendien heeft dat gebied de <span class="wintitle"> Allow reeks van de </span> attributen van Lijsten. In dit geval, wordt de waarde van de Delimiters van de Lijst van het gebied, die de eerste bepaalde afbakening is, gebruikt in de aaneenschakeling. </p> </li> 
      <li id="li_DEA24003E97E406DA2510C43CCFDC70E"> <span class="uicontrol"> Primaire sleutel? </span> <p>Slechts één gebied wordt geïdentificeerd als primaire sleutel. Dit gebied zal als "buitenlandse sleutel"worden gebruikt om de gegevens van de Lader van Attributen met het overeenkomstige document in de index aan te passen. </p> </li> 
      <li id="li_80D6AF130FCE40AC972FE4B605B86BF6"> <span class="uicontrol"> HTML strippen? </span> <p>Wanneer deze optie wordt gecontroleerd, worden om het even welke markeringen van HTML die in de gegevens van dit gebied worden gevonden verwijderd. </p> </li> 
      <li id="li_D40E2F9AD8AD49FC9AC4B8C75BA31E28"> <span class="uicontrol"> Actie </span> <p>Laat u rijen aan de kaart toevoegen of rijen verwijderen uit de kaart. De orde van de rijen is niet belangrijk. </p> </li> 
      </ul> </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. (Facultatief) klik **[!UICONTROL Setup Maps]** om een steekproef van uw gegevensbron te downloaden. De gegevens worden op geschiktheid onderzocht.
1. Klik **[!UICONTROL Add]** om de configuratie aan de [!DNL Attribute Loader Definitions] pagina toe te voegen.
1. Voor de [!DNL Attribute Loader Definitions] pagina, klik **[!UICONTROL rebuild your staged site index]**.
1. (Facultatief) op de [!DNL Attribute Loader Definitions] pagina, doe om het even welke volgend:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Het uitgeven van een definitie van de Lader van Attributen {#task_AA2D1B2BCAFA44A6A0C59A0318274E80}

U kunt een bestaande Lader van Attributen uitgeven die u hebt bepaald.

>[!NOTE]
>
>Om de Lader van Attributen te gebruiken, kunt u het moeten hebben toegelaten in uw rekening door uw de rekeningsvertegenwoordiger van Adobe of door de Steun van Adobe.

Niet zijn alle opties van de Lader van Attributen beschikbaar voor u aan verandering, zoals de Naam van de Lader van Attributen of het Type van het Type van [!DNL Type] drop-down lijst.

**Om een definitie van de Lader van Attributen uit te geven**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Voor de [!DNL Attribute Loader] pagina, onder de [!DNL Actions] kolomrubriek, klik **[!UICONTROL Edit]** voor een de definitienaam van de Lader van Attributen de waarvan montages u wilt veranderen.
1. Voor de [!DNL Attribute Loader Edit] pagina, plaats de opties u wilt.

   Zie de lijst van opties onder het [Toevoegen van een definitie](../c-about-settings-menu/c-about-metadata-menu.md#task_A735E5EF763343A9B675E1A3B09AFDBC)van de Lader van Attributen.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Facultatief) op de [!DNL Attribute Loader Definitions] pagina, klik **[!UICONTROL rebuild your staged site index]**.
1. (Facultatief) op de [!DNL Attribute Loader Definitions] pagina, doe om het even welke volgend:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Het kopiëren van een definitie van de Lader van Attributen {#task_9B40D5ECFC81411E9480F62A0FD5F2E0}

U kunt een bestaande definitie van de Lader van Attributen kopiëren om als basis voor een nieuwe Lader van Attributen te gebruiken die u wilt tot stand brengen.

>[!NOTE]
>
>Om de Lader van Attributen te gebruiken, kunt u het moeten hebben toegelaten in uw rekening door uw de rekeningsvertegenwoordiger van Adobe of door de Steun van Adobe.

Wanneer het kopiëren van een definitie van de Lader van Attributen, wordt de gekopieerde definitie onbruikbaar gemaakt door gebrek. Om de definitie in te schakelen of &quot;aan te zetten&quot;, moet u deze bewerken vanaf de [!DNL Attribute Loader Edit] pagina en selecteren **[!UICONTROL Enable]**.

Zie een definitie [van de Lader van Attributen](../c-about-settings-menu/c-about-metadata-menu.md#task_AA2D1B2BCAFA44A6A0C59A0318274E80)uitgeven.

**Om een definitie van de Lader van Attributen te kopiëren**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Voor de [!DNL Attribute Loader] pagina, onder de [!DNL Actions] kolomrubriek, klik **[!UICONTROL Copy]** voor een de definitienaam van de Lader van Attributen de waarvan montages u wilt dupliceren.
1. Voor de [!DNL Attribute Loader Copy] pagina, ga de nieuwe naam van de definitie in.
1. Klik op **[!UICONTROL Copy]**.
1. (Facultatief) op de [!DNL Attribute Loader Definitions] pagina, doe om het even welke volgend:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## De naam van een definitie van de Lader van Attributen wijzigen {#task_58D5DFD7EBC04111BCB91118E4440DB4}

U kunt de naam van een bestaande definitie van de Lader van Attributen veranderen.

>[!NOTE]
>
>Om de Lader van Attributen te gebruiken, kunt u het moeten hebben toegelaten in uw rekening door uw de rekeningsvertegenwoordiger van Adobe of door de Steun van Adobe.

**Om een definitie van de Lader van Attributen anders te noemen**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Voor de [!DNL Attribute Loader] pagina, onder de [!DNL Actions] kolomrubriek, klik **[!UICONTROL Rename]** voor de definitienaam van de Lader van Attributen die u wilt veranderen.
1. Voor de [!DNL Attribute Loader Rename] pagina, ga de nieuwe naam van de definitie op het [!DNL Name] gebied in.
1. Klik op **[!UICONTROL Rename]**.
1. (Facultatief) op de [!DNL Attribute Loader Definitions] pagina, doe om het even welke volgend:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Gegevens over de ladingswaarde van Attributen laden {#task_2F3C55189B0A4049AB2113F2291CC181}

U kunt de gevormde gegevens van de Lader van Attributen in plaatsonderzoek downloaden/merchandising.

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
   <td colname="col2"> <p>Wijst op het succes of de mislukking van de laatste poging van de gegevenslading. Of, toont het de status van een verrichting van de gegevenslading die reeds lopend is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Begintijd </p> </td> 
   <td colname="col2"> <p>Toont de datum en de tijd dat de laatste verrichting van de gegevenslading begon. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tijd stoppen </p> </td> 
   <td colname="col2"> <p>Toont de voltooiingsdatum en de tijd van de laatste verrichting van de gegevenslading. Of, wijst het erop de huidige verrichting van de gegevenslading nog lopend is. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Om de gegevens van de Lader van Attributen te laden**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Voor de [!DNL Attribute Loader Definitions] pagina, klik **[!UICONTROL Load Attribute Loader Data]**.
1. Op de **[!UICONTROL Attribute Loader Data Load]** pagina, doe één van het volgende:

   * Klik **[!UICONTROL Start Load]** om de ladingsverrichting te beginnen.

      Tijdens een gegevensladingsverrichting, verstrekt **de rij van de Voortgang** informatie over zijn vooruitgang.

   * Klik **[!UICONTROL Stop Load]** om de ladingsverrichting tegen te houden.

1. Klik **[!UICONTROL Close]** om op de [!DNL Attribute Loader Definitions] pagina terug te komen.

## Previewing de gegevens van de Lader van Attributen {#task_735CDCC1D8174B7B9F5B8E0AFA5F0CA0}

U kunt Voorproef gebruiken om uw onlangs geladen gegevens van de Lader van Attributen te bekijken.

De kolom van de Rij in de lijst toont het aantal voor elke rij van gegevens, die op de originele orde wijzen dat de waarden van de Lader van Attributen werden geladen.

De resterende kolommen tonen de waarden die met elke ingang worden geassocieerd.

Als de lijst leeg is, betekent het dat u nog geen gegevens van de Lader van Attributen hebt geladen. U kunt de [!DNL Attribute Loader Data Preview] pagina sluiten, en dan de gegevens van de Lader van Attributen laden.

Zie de gegevens van de Lader van de [Attributen van de Lading](../c-about-settings-menu/c-about-metadata-menu.md#task_2F3C55189B0A4049AB2113F2291CC181).

**Aan voorproef de gegevens van de Lader van Attributen**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Voor de [!DNL Attribute Loader Definitions] pagina, onder de [!DNL Actions] kolom, klik **[!UICONTROL Preview]** voor de configuratie waarvan gedownloade gegevens u wilt bekijken.
1. Voor de [!DNL Attribute Loader Data Preview] pagina, gebruik de navigatie en het bekijken opties bij de bovenkant en de bodem van de pagina om de gegevens te bekijken.

   Klik om het even welke kolomrubriek in de lijst om de gegevens in stijgende of dalende orde te sorteren.
1. Doe om het even welke volgend:

   * Klik **[!UICONTROL Download to Desktop]** om de lijst als .xlt dossier te downloaden en op te slaan.
   * Sluit de pagina wanneer u klaar bent met het voorvertonen van de gegevens van de Lader van Attributen en ga aan de eerder bekeken pagina terug.

## Het bekijken van de montages van een definitie van de Lader van Attributen {#task_EA99A9694FE948ADA82C1DBA0667851B}

U kunt de configuratiemontages van een bestaande definitie van de Lader van Attributen herzien.

Nadat een definitie van de Lader van Attributen aan de [!DNL Attribute Loader Definitions] pagina wordt toegevoegd, kunt u niet zijn het plaatsen van het Type veranderen. In plaats daarvan, moet u de definitie schrappen en dan nieuwe toevoegen.

>[!NOTE]
>
>Om de Lader van Attributen te gebruiken, kunt u het moeten hebben toegelaten in uw rekening door uw de rekeningsvertegenwoordiger van Adobe of door de Steun van Adobe.

**Om de montages van een definitie van de Lader van Attributen te bekijken**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Voor de [!DNL Attribute Loader] pagina, onder de [!DNL Actions] kolomrubriek, klik **[!UICONTROL Edit]** voor een de definitienaam van de Lader van Attributen de waarvan montages u wilt herzien of uitgeven.

## Het bekijken van het logboek van de meest recente de gegevenslading van de Lader van Attributen {#task_9C7D6E34BB6C4A40B7CA3EE36ACB0837}

U kunt gebruiken [!DNL View Log] om het de gegevenslogboekdossier van de Lader van Attributen van het meest recente downloadproces te onderzoeken. U kunt de logboekmening ook gebruiken om een lopende download te controleren.

Zie de gegevens van de Lader van de [Attributen van de Lading](../c-about-settings-menu/c-about-metadata-menu.md#task_2F3C55189B0A4049AB2113F2291CC181).

**Om het logboek van de meest recente de gegevenslading van de Lader van Attributen te bekijken**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Voor de [!DNL Attribute Loader Definitions] pagina, klik **[!UICONTROL View Log]**. Logpagina,
1. Voor de [!DNL Attribute Loader Data Log] pagina, gebruik de navigatie en het bekijken opties bij de bovenkant en de bodem van de pagina om de logboekinformatie te bekijken.
1. Wanneer u wordt gebeëindigd, sluit de pagina om aan de [!DNL Attribute Loader Definitions] pagina terug te keren.

## Het schrappen van een definitie van de Lader van Attributen {#task_E8980F66888B476E98C228C1D307EDF8}

U kunt een bestaande definitie van de Lader van Attributen schrappen die u niet meer nodig hebt of gebruikt.

>[!NOTE]
>
>Om de Lader van Attributen te gebruiken, kunt u het moeten hebben toegelaten in uw rekening door uw de rekeningsvertegenwoordiger van Adobe of door de Steun van Adobe.

**Om een definitie van de Lader van Attributen te schrappen**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Voor de [!DNL Attribute Loader Definitions] pagina, onder de [!DNL Actions] kolomrubriek, klik **[!UICONTROL Delete]** voor de de definitienaam van de Lader van Attributen u wilt verwijderen.
1. Voor de [!DNL Attribute Loader Delete] pagina, klik **[!UICONTROL Delete]**.
