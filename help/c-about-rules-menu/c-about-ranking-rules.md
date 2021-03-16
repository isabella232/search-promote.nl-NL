---
description: U kunt Rangschikkingsregels gebruiken om de relatieve positie of rangschikking van de zoekresultaten van een klant te bepalen op basis van de inhoud van de metatag en de gerelateerde Adobe Analytics-meetgegevens.
solution: Target
subtopic: Ranking Rules
title: Info over Rangschikkingsregels
topic: Regels, zoeken en verhandelen van sites
uuid: 21962f9a-1d9c-442f-a6c4-5f452436c640
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '4621'
ht-degree: 0%

---


# Info over Rangschikkingsregels{#about-ranking-rules}

U kunt Rangschikkingsregels gebruiken om de relatieve positie of rangschikking van de zoekresultaten van een klant te bepalen op basis van de inhoud van de metatag en de gerelateerde Adobe Analytics-meetgegevens.

## Willekeurige regels gebruiken {#concept_F555C076759B4E81B925441CFE707397}

U definieert waarderingsregels om de relatieve plaatsing van de documenten in de zoekresultaten te beïnvloeden op basis van de inhoud van elk document. U kunt waarderingsregels baseren op metatag-inhoud, Adobe Analytics-meetgegevens (als uw account is geconfigureerd voor Adobe Analytics) of Adobe Analytics-HBX (als uw account is geconfigureerd voor Adobe Analytics-HBX).

U kunt webpagina&#39;s instellen die metatags met de gewenste kenmerken bevatten, zoals een bepaalde merknaam of prijs, of webpagina&#39;s die wenselijke prestatie-indicatoren van Adobe Analytics hebben, zoals unieke viewers, om een hogere positie te krijgen dan webpagina&#39;s die dat niet doen. De &quot;wenselijke&quot;kenmerken worden gemakkelijk bijgewerkt door het toevoegen of het uitgeven van het Rangschikken Regels en dan uw website opnieuw te indexeren.

Als u meerdere metatags van het type &quot;rank&quot; hebt gedefinieerd, kunt u aparte verzamelingen regels maken die u kunt gebruiken voor het berekenen van de verschillende velden in de rang. U kunt een groep met rangtelregels toevoegen die u vervolgens kunt toewijzen aan een van de gedefinieerde Rank-velden. De groepen van de regel bevatten normaal één of meerdere regeldefinities, maar kunnen ook naar andere groepen van de Regel verwijzen, zodat kunt u één of meerdere groepen algemeen gebruikte regels tot stand brengen die tijdens de berekening van uw veelvoudige ranken worden gedeeld.

Zie [Een rangschikkingsregelgroep toevoegen](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8).

Een positieve rangorde bevordert onderzoeksresultaten naar de bovenkant; met een negatieve rangorde worden de zoekresultaten onderaan in de zoekresultaten aangegeven. De normale waaier voor rangschikkingswaarden is 1.0 die de maximumbevordering binnen de onderzoeksresultaten is, terwijl -1.0 de maximumdemotie is. Hoewel u dit bereik kunt aanpassen door het veld Rank te bewerken in metagegevensdefinities, is dit type aanpassing meestal niet nodig.

Zie [Informatie over definities](../c-about-settings-menu/c-about-metadata-menu.md#concept_AE48035C210145169BE067D396975620).

Als u meer dan één rangtelveld hebt gedefinieerd onder Instellingen > Metagegevens > Definities, kunt u extra sets met rangtelregels maken, één voor elk rankingveld. U kunt extra reeksen rangschikkingsregels bepalen zonder direct met een rangschikkingsgebied worden geassocieerd. Met deze flexibiliteit kunt u sets algemene regels maken die kunnen worden gedeeld bij de berekening van een of meer randewaarden.

**Belangrijk**: Alvorens u het Rangschikken Regels kunt gebruiken, zijn er verscheidene stappen van de rekeningsconfiguratie die u moet voltooien.

Zie [Rangschikking configureren](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5)

## Classificatie {#task_4CEBC13925B047FC95BDC217B48089C5} configureren

Voordat u rangschikkingsregels kunt gebruiken, zijn er verschillende stappen in de accountconfiguratie die u moet voltooien.

**Classificatie configureren**

1. Kies een van de volgende opties:

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Taak </p> </th> 
      <th colname="col2" class="entry"> <p>Configuratie </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Classificatieregels maken die zijn gebaseerd op metatags </p> </td> 
      <td colname="col2"> <p> 
      <ol id="ol_28ABB980143948DFA79AC4360AAB7556"> 
      <li id="li_544075CFA0964C6F8FAF7941AAA9ECCC"> Klik in het productmenu op <span class="uicontrol"> Instellingen </span> &gt; <span class="uicontrol"> Metagegevens </span> &gt; <span class="uicontrol"> Definities </span>. </li> 
      <li id="li_F237F13B89E8425080C15D3BD697652C"> Klik op <span class="uicontrol"> Nieuw veld toevoegen </span> op de pagina Definities. </li> 
      <li id="li_2A839874D71D45FEA661B3D3B8BE2A86"> Typ op de pagina Veld toevoegen in het tekstveld <span class="uicontrol"> Veldnaam </span> 
      <code>
        rank 
      </code>; Typ in het tekstveld <span class="uicontrol"> Naam metatag </span> 
      <code>
        rank 
      </code>; Selecteer <span class="uicontrol"> Rang </span> in de vervolgkeuzelijst <span class="uicontrol"> Gegevenstype </span>. Laat alle andere veldopties ongewijzigd. <p>Zie de vraagparameter <span class="codeph"> sp_sr </span> in <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> Achterste onderzoek CGI parameters </a>. </p> </li> 
      <li id="li_8E91AF4BE51A4A41ABBF9680DDE0B7CE">Klik <span class="uicontrol"> toevoegen </span>. </li> 
      </ol> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Om rangschikkingsregels tot stand te brengen die op de metriek van Adobe Analytics worden gebaseerd </p> </td> 
      <td colname="col2"> <p> 
      <ol id="ol_BE57CBC303D941778B10D855ADC93C68"> 
      <li id="li_8DF5D8F924B24ECBBD2D93C76C69D00C"> Zorg ervoor dat u Adobe Analytics-verificatie hebt ingesteld vanuit de zoekfunctie/merchandising op de site. <p>Zie <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_8AA93F6273B747F9B4DE9E8DFBCBDC42" type="task" format="dita" scope="local"> Metrische verificatie van Adobe Analytics instellen </a>. </p> </li> 
      <li id="li_CF7DD073FC5A432DADBD282AA8BB9920"> Selecteer en voeg een beschikbare rapportreeks toe. <p>Zie <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_6DE17305EA7146DA8C30FF8FDF68A3C0" type="task" format="dita" scope="local"> Een Adobe Analytics-rapportsuite toevoegen </a>. </p> </li> 
      <li id="li_9A63448577D04E028DF211D8715F943A"> Vorm de lijst van metriek van Adobe Analytics die u voor de verwezenlijking van nieuwe het Rangschikken Regels beschikbaar wilt zijn. <p>Zie <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664" type="task" format="dita" scope="local"> De Adobe Analytics-meetgegevens van een rapportsuite </a> bewerken. </p> </li> 
      <li id="li_1ACA3611D9B44AC394604CD89209C966"> Laad de oorspronkelijke Adobe Analytics-gegevens voor uw websitepagina's. <p>Zie <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_2F3C55189B0A4049AB2113F2291CC181" type="task" format="dita" scope="local"> Adobe Analytics-gegevens laden </a>. </p> </li> 
      </ol> </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Voeg een of meer rangtelregels toe.

   Zie [Een rangschikkingsregel toevoegen](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A).

1. Klik **[!UICONTROL regenerate your staged site index]** om een volledige herindex van uw website uit te voeren (van **[!UICONTROL Index]** > **[!UICONTROL Full Index]**).

   Zie [Een volledige index van een actieve of gefaseerde website uitvoeren...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Zie [Een incrementele index van een gefaseerde website configureren](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. Controleer de waarden in de kolom Rang in **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]** om te verifiëren dat uw het Rangschikken Regels correct werden toegepast.

## Documenten rangschikken op leeftijd {#topic_770815CF1B2A491F83FF765871B6F1B8}

U kunt een HTML-document op zijn leeftijd rangschikken met een exponentiële verval functie. De snelheid van verval wordt bepaald met een gekozen halfwaardetijd constante, de hoeveelheid tijd die moet overgaan alvorens de waarde aan de helft van zijn aanvankelijke waarde daalt.

De leeftijdsclassificatie is gebaseerd op de volgende twee vergelijkingen:

`K = -ln(2) / H`

`RANK = e^(K * T)`

De variabelen `H` en `T` zijn input aan deze functie: `H` is de gewenste halfwaardetijd en `T` is de leeftijd van het document, uitgedrukt in seconden. `K` de berekende halfwaardetijd en  `RANK` de exponentiële afname van de opgegeven leeftijdswaarde. De resulterende waarde ligt tussen 0 en 1. Een recentere document heeft een rangorde dichter aan 1 dan een ouder document. In theorie mogen documenten nooit de waarde 0 bereiken, maar afrondingsfouten kunnen ertoe leiden dat het resultaat 0 wordt.

## Voorschriften voor het gebruik van de leeftijdsklasse {#section_D716507D589442C6B7848892BD28F966}

* Uw account moet al correct zijn geconfigureerd voor classificatie. Als het niet wordt gevormd, zie [Het vormen rangschikking](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5).
* Het HTML-document moet een HTML-metatag hebben waarin de geboortedatum, het begin als tijdstempel of een andere relevante datumwaarde wordt weergegeven.
* De speciale ingebouwde functie, `search_get_age_rank()`, zoals die in Add wordt gespecificeerd of de pagina&#39;s van de Regel van het Rangschikken uitgeeft, wordt gebruikt om de de leeftijdsrang van een document te berekenen. In de volgende secties wordt het algemene gebruik van de leeftijdsklasseringsfunctie uitvoerig beschreven. Er wordt ook een voorbeeld weergegeven waarin de functie voor leeftijdsbepaling wordt getoond.

## Het gebruiken van search_get_age_rank () op de Add Willekeurige pagina van de Regel of de Edit Willekeurige pagina van de Regel {#section_34BC5276F2AB4419AD92872A397CA0AF}

Geef `search_get_age_rank()` als volgt op:

`search_get_age_rank(Birthdate#Half_Life#Default_Rank)`

* Geboortedatum - De geboortedatum of aanmaakdatum van het bestand moet een tekenreeks met de datumnotatie zijn in overeenstemming met de datumnotatie van het veld. Deze datumopgemaakte tekenreeks moet een veldverwijzing zijn, zoals in `{field_name}`.
* Half_Life - De halfwaardetijd is de hoeveelheid tijd die moet overgaan alvorens de waarde aan de helft van zijn aanvankelijke waarde daalt. Deze waarde wordt uitgedrukt in het aantal dagen en is een geheel getal of een drijvende-kommagetal.
* Default_Rank - De standaardrang wordt gebruikt als veiligheidsnet voor het geval dat de geboortedatum ongeldig is of de datum in de toekomst is. U kunt deze standaardwaarde niet gebruiken als het bijbehorende metagegevensveld ook een geldige standaardwaarde heeft. De waarde hier is een drijvende-kommagetal of een geheel getal. Zie hieronder voor suggesties als u problemen ondervindt waarmee de standaardwaarde wordt gebruikt.

Zie [Een rangschikkingsregel toevoegen](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A).

Zie [Een rangschikkingsregel bewerken](../c-about-rules-menu/c-about-ranking-rules.md#task_5EBF55A43D6545FEA46BAE5E586FA275).

**Voorbeeld**

In het volgende voorbeeld:

`search_get_age_rank({birthdate}#28#0.20)`

de datum in het `birthdate` gebied van het document wordt overgegaan in als tijd-stempel. De halfwaardetijd is 28 dagen. De standaardwaarde voor rangschikking is 0,20 als de datum ongeldig is.

Zie de optietabel in [Een rangschikkingsregel toevoegen](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A).

In de sectie Waarden/spaties van de Add het Rangschikken pagina van de Regel of de Edit het Rangschikken pagina van de Regel, kunt u `search_get_age_rank` met douane-gemaakte regels slechts gebruiken. Zorg er daarom voor dat u **Aangepast** kiest in de vervolgkeuzelijst Waarden/spaties. Wanneer de regel de ouderrangschikkende functie gebruikt, worden geen ruimten toegestaan in het waardegedeelte van de regel. Zorg ervoor dat er geen spaties voorkomen in de functieargumenten of daartussen. En er zijn geen spaties tussen wiskundige of voorwaardelijke operatoren.

Hieronder ziet u een voorbeeld van een regel voor waarden/ranks, een regel die is gekoppeld aan een tekstveld:

`regexp .* search_get_age_rank({other_field}#365#0.20)`

In dit voorbeeld wordt ervan uitgegaan dat `other_field` een datumwaarde bevat. Als dit veld zelf geen datumveld is, wordt deze waarde geïnterpreteerd met de datumnotaties die zijn gekoppeld aan het vooraf gedefinieerde datumveld. Anders worden de datumnotaties van dit veld gebruikt. Deze waarden/ranks-vermelding wordt gebruikt wanneer het veld van het document, dat de gegevensbron van de regel identificeert, niet leeg is en de geretourneerde waarde van de functie (van 0 tot en met 1) de toegewezen rang is.

Voor een Regel die aan een Numeriek gebied wordt geassocieerd, specifiek een gebied van de Datum:

`9999999999 search_get_age_rank({other_field}#365#0.20)`

Tijdens het verwerken van elk document wordt de waarde in `other_field` geconverteerd naar het Unix-formulier &quot;epoch&quot;, waarbij de datumnotatiedefinities van het veld worden gebruikt. Deze waarde wordt gebruikt in de `search_get_age_rank()` vraag. Aangezien elke &quot;epoch&quot;waarde minder dan 999999999999 (voor nu minstens) is, levert de Regel eenvoudig de terugkeerwaarde van de functie (van 0 door 1) als rang.

In beide voorgaande voorbeelden is het typisch dat de gegevensbron van de regel hetzelfde veld is als in de functie `search_get_age_rank()` - `other_field` in dit geval.

## Een voorbeeld van het integreren van leeftijdsrangschikking in rangorderegels {#section_A86D909687CC45E19D4EA7A4A9283F28}

Hieronder ziet u hoe u de rangschikking van de leeftijd kunt integreren in de rangschikkingsregels. In het voorbeeld ziet u ook de onbewerkte resultaten van de functie voor leeftijdsbepaling en de resultaten van de rangschikkingsregels. In het voorbeeld wordt uitgegaan van het volgende:

* De webpagina&#39;s die horizontaal schuiven, hebben een HTML-metatag met de naam &#39;verjaardatum&#39;. De inhoud van deze tag is een tijdstempel die betrekking heeft op het document.
* De metagegevensdefinities hebben een gedefinieerd metatag veld voor de verjaardagstag. Dit veld is ingesteld op het type &quot;date&quot;.

**Regels voor rangschikking**

Zie [Een nieuw metatag toevoegen gebied](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).

Nu voegt u een nieuwe rangschikkingsregel toe. De regel wordt gedefinieerd om het veld &#39;verjaardatum&#39; in het document te gebruiken. Er wordt een nieuwe rangschikkingsregel toegevoegd met de volgende eigenschappen ingesteld:

* Type gegevensbron: Meta-tag
* Naam gegevensbron: geboortedatum
* Gewichten/omstandigheden: 10 - Maximaal belang
* Waarden/spaties: 9999999999 search_get_age_rank({verjaardatum}#14#0.10)
* Standaardwaarde: -1

De regel doet verschillende dingen. Het gewicht van de regel is ingesteld op 10. De randewaarde is gewoon het resultaat van de leeftijdsklasse functie, een waarde van 0 tot en met 1. U kunt geen spaties gebruiken met `search_get_age_rank()`. U ziet ook dat het veld &quot;verjaardatum&quot; tussen haakjes staat. Wanneer u deze regel opslaat, worden de komma&#39;s in de definitie Values/Ranks vervangen door `#` tekens. dit gedrag is normaal .

**De resultaten weergeven**

Met de functie Gegevens weergeven kunt u snel de resultaten van de functie voor de leeftijd zien. Voeg de desbetreffende metagegevensvelden toe. In het voorbeeld zijn `age_val` en `myrank` de twee gebieden van Meta-gegevens die aan de Mening van Gegevens zouden moeten worden toegevoegd. In het veld `myrank` ziet u hoe de rangschikking van de leeftijd van invloed is op de rangschikkingswaarden. In het veld `age_val` wordt de onbewerkte uitvoer van de functie exponentieel verval voor dat document weergegeven.

## Standaardwaarden {#section_CB109EF78F914E92955D512ACFC3310E}

Hieronder vindt u drie standaardwaarden die bij de functie `search_get_age_rank()` horen:

* De standaardwaarde die u in de `search_get_age_rank()` functie kunt ingaan zelf.
* De standaardwaarde voor de rang van de regel.
* De standaardwaarde in de metagegevensdefinitie.

Afhankelijk van de plaats waar de fout optreedt, kunnen verschillende standaardwaarden worden opgehaald.

De standaardwaarde van de metagegevensdefinitie zou bijvoorbeeld nooit mogen voorkomen als Rangschikken en Filteren correct is geïmplementeerd. Deze standaardwaarde is de laatste redactiewaarde wanneer er geen geldige of bekende inhoud voor dat metagegevensveld bestaat. De standaardwaarde in de rangschikkingsregels kan verschijnen wanneer `search_get_age_rank()` naar zijn eigen bijbehorende markering verwijst en de markering in het document mist. In dit geval gaat deze regel recht naar de standaardwaarde van de regel. Als de functie voor leeftijdsbepaling verwijst naar een tag van een andere rangschikkingsregel, is het mogelijk dat de standaardwaarde die in die functie voor leeftijdsklassering wordt doorgegeven, wordt gebruikt als de tag waarnaar wordt verwezen ontbreekt of ongeldig is.

## Een waarderingsregel {#task_A132789FD4E5423DAD090DCDA7311E8A} toevoegen

U kunt [!DNL Ranking Rules] toevoegen om de relatieve plaatsing van de Web-pagina&#39;s binnen uw resultaten van het Onderzoek te beïnvloeden, die op de inhoud van elke Web-pagina wordt gebaseerd.

Zie [Rangschikking configureren](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5).

**Een waarderingsregel toevoegen**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. (Optioneel) Als u een regelgroep hebt gemaakt en regels aan de groep hebt toegevoegd, selecteert u op de pagina [!DNL Define Ranking Rules] in de vervolgkeuzelijst **[!UICONTROL Select Rule Group]** een regelgroep met de regels die u wilt bewerken.

   Zie [Een rangschikkingsregelgroep toevoegen](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8).
1. Voor [!DNL Define Ranking Rules] pagina, klik **[!UICONTROL Add Rule]** om een nieuwe het Rangschikken Regel toe te voegen, of een verwijzing aan een reeks van de Regel toe te voegen.
1. Stel op de pagina [!DNL Add Ranking Rule] de gewenste opties in. Velden met een sterretje (*) zijn verplicht.

   Het type gegevensbron dat u selecteert, beïnvloedt de keuzen die op [!DNL Data Source Name] drop-down lijst beschikbaar zijn. Als u bijvoorbeeld **[!UICONTROL Meta Tag]** hebt geselecteerd als gegevenstype voor gegevensbron, verwijst de naam van een metatag op de websitepagina&#39;s. Als u **[!UICONTROL Adobe Analytics Metric (Number)]** selecteerde, verwijst de Naam van de Gegevensbron naar één van de metrische namen van Adobe Analytics die u in een Reeks van het Rapport zoals gevonden op de **[!UICONTROL Edit Adobe Analytics Metrics]** pagina in plaatsonderzoek/handel.

   Zie [De Adobe Analytics-meetgegevens van een rapportsuite](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664) bewerken.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Type gegevensbron </p> </td> 
      <td colname="col2"> <p>Bepaalt de kenmerken van de gegevensbron die als input aan deze rangschikkingsregel wordt gebruikt. </p> <p>De volgende gegevensbrontypen kunt u selecteren: 
      <ul id="ul_B0A97BF0E314495985F44A642C86918D"> 
      <li id="li_4D8BDE32853540809AE78FF5FF5677A1"> <span class="uicontrol"> Meta-tag  </span> <p> Deze regel is gebaseerd op numerieke gegevens of tekstuele gegevens die zijn opgeslagen in een benoemde metatag op uw websitepagina's. </p> </li> 
      <li id="li_4976C31D67254C7F81D554EC49DDBB40"> <span class="uicontrol"> Adobe Analytics Metric (Number)  </span> <p>Deze regel is gebaseerd op een numerieke Adobe Analytics-maateenheid die aan uw sitepagina's is gekoppeld. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Naam gegevensbron </p> </td> 
      <td colname="col2"> <p>Als u <span class="uicontrol"> Meta-tag </span> als gegevenstype gegevensbron hebt gekozen, is dit de naam van een meta-tag die op de pagina's van uw website staat. De namen in het vervolgkeuzemenu zijn afkomstig uit de lijst met gedefinieerde metagegevenswaarden die zijn geconfigureerd in Instellingen &gt; Metagegevens &gt; Definities. </p> <p>Zie <a scope="local" href="../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5" type="task" format="dita"> Een nieuw metatag toevoegen veld </a>. </p> <p>Als u Metrisch van Adobe Analytics (Aantal) als Type van Gegevensbron kiest, is dit de naam van metrische Adobe Analytics. De namen in het vervolgkeuzemenu zijn afkomstig uit de lijst met beschikbare Adobe Analytics-meetgegevens die zijn geconfigureerd in Instellingen &gt; Adobe Analytics &gt; Metriek &gt; Bewerken. </p> <p>Zie <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664" type="task" format="dita" scope="local"> De Adobe Analytics-meetgegevens van een rapportsuite </a> bewerken. </p> <p>Als de door u geselecteerde metrische Adobe Analytics-naam nog niet is gedefinieerd in <span class="uicontrol"> Instellingen </span> &gt; <span class="uicontrol"> Metagegevens </span> &gt; <span class="uicontrol"> Definities </span>, worden een tekstveld en een knop Toevoegen weergegeven. Voer de naam in van het veld Metagegevens (de naam van het metagegevensveld mag niet langer zijn dan 20 tekens) en klik op <span class="uicontrol"> Toevoegen </span>. </p> <p>Wanneer pagina's worden aangetroffen met meerdere Adobe Analytics-toetsen, zoals op een productpagina met meerdere producten, geeft Composite Scheme aan hoe de meervoudige Adobe Analytics-metrische waarden die aan die pagina zijn gekoppeld, moeten worden verwerkt. Selecteer een van de volgende opties: </p> <p> 
      <ul id="ul_D6E51748BB3949048A37C1895F2C0A58"> 
      <li id="li_04F00F382A264C96A519B0D975E25E94"> <span class="uicontrol"> Som  </span> <p>Retourneert de som van de metrische waarden. </p> </li> 
      <li id="li_FA44219B663F4CC197BD3A094EB84396"> <span class="uicontrol"> Gemiddeld  </span> <p>Retourneert het gemiddelde van de waarden (de som gedeeld door het aantal waarden). </p> </li> 
      <li id="li_F0EAAE1EA1754FFEB30F611E5550097B"> <span class="uicontrol"> Maximum  </span> <p>Retourneert de grootste van de waarden. </p> </li> 
      <li id="li_38E3E3F3D9AF4C57803B84B60223FB9D"> <span class="uicontrol"> Eerste  </span> <p>Retourneert de waarde die overeenkomt met de eerste toets. </p> </li> 
      <li id="li_4AEE470CE6BB4D899E975915EC226624"> <span class="uicontrol"> Laatste  </span> <p>Retourneer de waarde die overeenkomt met de laatste toets. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Gewichten/omstandigheden </p> </td> 
      <td colname="col2"> <p>Bevat een eenvoudig getal met één regeldikte of een gepaarde lijst met regelgewichtnummers en testvoorwaarden. </p> <p>Een regelgewichtaantal is een waarde van 1-10 die erop wijst hoe belangrijk deze rangschikkingsregel met betrekking tot de andere rangschikkingsregels in het bepalen van de algemene rang van een document is. Een hogere regeldikte geeft een groter belang aan. Bij een gewicht van nul (0) wordt de lijn genegeerd. </p> <p>Kies <span class="uicontrol"> Aangepast </span> in de vervolgkeuzelijst om de regeldikte voor verschillende pagina's aan te passen door een lijst met paren regeldikte/testvoorwaarden te definiëren. De voorwaarden van de test zijn fragmenten van Perl die worden gebruikt om de Waarden van de Gegevensbron, of globale variabelen te testen die binnen uw manuscript van de douanefilter (bijvoorbeeld, prijs, merk, seizoen, of paginameningen zoals in het volgende voorbeeld) worden bepaald. Als een testvoorwaarde "waar"evalueert,"wordt de bijbehorende waarde van de regeldikte toegepast. Als een testvoorwaarde false oplevert, wordt de volgende voorwaarde in de lijst geëvalueerd. <code> 0&nbsp;({price}&nbsp;&gt;&nbsp;50.00)&nbsp;&amp;&amp;&nbsp;({brand}=~/Kuhl/)5&nbsp;{season}&nbsp;=~&nbsp;/Fall/10&nbsp;{pageviews}&nbsp;&gt;&nbsp;1000005 </code>In het aangepaste gewicht/voorwaardenvoorbeeld hierboven wordt regelgewicht 0 toegepast als de eerste testvoorwaarde 'true' oplevert. De prijs bevat dus een waarde groter dan 50 en het merk bevat "Kuhl"). Als de eerste testvoorwaarde false oplevert, wordt de volgende voorwaarde geëvalueerd. Als aan geen van de vorige voorwaarden wordt voldaan, wordt regelgewicht 5 toegewezen. </p> <p>U zou altijd een regelgewicht zonder voorwaarde aan het eind van de lijst moeten verstrekken. Als u dit niet doet, krijgt de regel een gewicht van 0 in het geval waar geen van de voorwaardentests aan "waar"evalueert. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Waarden/spaties </p> </td> 
      <td colname="col2"> <p>Bestaat uit één van beide ingebouwde rangschikkingsfuncties, of mogelijke inhoud van de Gegevensbron samen met gewenste ranks. </p> <p>Als u <span class="uicontrol"> Metrisch van Adobe Analytics (Aantal) </span> als Type van Gegevensbron kiest, wordt u voorgesteld met een drop-down lijst met de volgende opties: 
      <ul id="ul_104906B6AA8547BAB6979AA37C4FAB90"> 
      <li id="li_7656A2855A054DB8B64E90FE501517AA"> <span class="uicontrol"> Auto-Rank op Volgorde (gebrek)  </span> <p>Hiermee wordt een positie berekend die is gebaseerd op de relatieve positie van het document volgens de Adobe Analytics Metric. Hoe dichter de positie van het document bij het document met de hoogste positie ligt, hoe hoger de positie. </p> </li> 
      <li id="li_1A7D60EA6965434AA6D39B215C158306"> <span class="uicontrol"> Automatisch terugdraaien op waarde  </span> <p>Hiermee wordt een rangorde berekend op basis van de relatieve waarde van het document volgens de Adobe Analytics Metric. Hoe dichter de waarde van het document bijvoorbeeld bij de waarde van het document met de hoogste positie komt, hoe hoger de positie. </p> </li> 
      <li id="li_457DE44D6ADA40619DC77220BF12318E"> <span class="uicontrol"> Aangepast  </span> <p>Hier geeft u aangepaste instellingen op. Een gegevensbron met de naam "merk" kan bijvoorbeeld de merknaam voor een bepaald product bevatten. Je kunt het relatieve belang van elk merk opgeven door het aan te bieden met de rangorde. </p> </li> 
      </ul> </p> <p>De randewaarden die door de berekeningen Auto-Rank worden geretourneerd, liggen tussen 0,0 (laagste) en 1,0 (hoogste). Ze worden niet aangepast volgens de bereiken die zijn gedefinieerd voor het veld Rang onder Instellingen &gt; Metagegevens &gt; Definities. </p> <p>In het volgende voorbeeld, als de merkgegevensbron voor een bepaald onderzoeksresultaat precies "DKNY aanpast,"is de toegepaste rangorde voor dat resultaat 0.5. Als het merk "Levis" is, is de toegepaste rangorde 0,1. De gegevensbroninhoud moet overeenkomen met de ingestelde waarde. Met andere woorden: als de gegevensbroninhoud "Levis Corp." is, komt deze niet overeen met de waarde "Levis". Case wordt genegeerd, dus 'DKNY' komt overeen met 'dkny' en 'Dkny'. <code> DKNY&nbsp;0.5 Levis&nbsp;0.1 Lee&nbsp;0.2 </code> </p> <p>Als geavanceerdere optie kunt u waarden opgeven als reguliere expressies. Stel dat sommige van uw sitepagina's de merkwaarde Levis bevatten en andere sitepagina's de merkwaarde Levis jeans bevatten. U kunt een reguliere expressie gebruiken die is opgegeven met het trefwoord 
      <code>
        regexp 
      </code>. </p> <p>Zie <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Reguliere expressies </a>. </p> <p>In het volgende voorbeeld krijgt een zoekresultaatdocument met de merkinhoud "Levis jeans" een rang van 0,1. Net als bij standaardvergelijking wordt case genegeerd voor reguliere expressies. <code> DKNY&nbsp;0.5 regexp&nbsp;Levis.*&nbsp;0.1 Lee&nbsp;0.2 </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Standaardwaarde </p> </td> 
      <td colname="col2"> <p> Geeft de rang aan die moet worden toegepast voor documenten met zoekresultaten die niet overeenkomen met een van de opgegeven waarden. In het bovenstaande voorbeeld wordt aan een zoekresultatendocument met een "merk"-gegevensbron met "de tussenruimte" de standaardwaarde voor de rangorde toegewezen, omdat "de tussenruimte" niet overeenkomt met een van de gedefinieerde waarden. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Notities </p> </td> 
      <td colname="col2"> <p>Voeg informatie toe die tot de het rangschikken regeldefinitie of de definitie van de regelgroep behoort die u creeerde. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   Het bereik van geldige rangtelwaarden ligt normaal gesproken tussen -1,0 en 1,0, zoals in het volgende voorbeeld:

   * `-1.0` is &quot;Minimum Rank (vertoning lager in de onderzoeksresultaten).&quot;
   * `0.0` is &quot;Neutrale rangorde (de volgorde van zoekresultaten niet wijzigen).&quot;
   * `1.0` is &quot;Maximumrang (weergave hoger in de zoekresultaten.&quot;

   De bepaalde ranks zouden binnen de zelfde waaier voor elke regel moeten zijn. De rank bereiken moeten ook de waaiers aanpassen die voor het gebied van de Rang onder **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]** worden bepaald.

   Zie [Een nieuw metatag toevoegen gebied](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).

   Zie ook [Een rangschikkingsregel bewerken](../c-about-rules-menu/c-about-ranking-rules.md#task_5EBF55A43D6545FEA46BAE5E586FA275).
1. Klik op **[!UICONTROL Add]**.
1. Klik op **[!UICONTROL regenerate your staged site index]** om een voorvertoning van de resultaten van de regeltoevoeging weer te geven en de gefaseerde website-index opnieuw samen te stellen.

   Zie [Een volledige index van een actieve of gefaseerde website uitvoeren...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Zie [Een incrementele index van een actieve of gefaseerde website uitvoeren...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een waarderingsregel {#task_5EBF55A43D6545FEA46BAE5E586FA275} bewerken

U kunt een bestaande waarderingsregel bewerken die u al hebt toegevoegd.

Zie [Rangschikking configureren](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5).

**Een waarderingsregel bewerken**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. (Optioneel) Als u een regelgroep hebt gemaakt en regels aan de groep hebt toegevoegd, selecteert u op de pagina **[!UICONTROL Define Ranking Rules]** in de vervolgkeuzelijst **[!UICONTROL Select Rule Group]** een regelgroep met de regels die u wilt bewerken.

   Zie [Een rangschikkingsregelgroep toevoegen](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8).
1. Klik in de tabel onder de kolomkop **[!UICONTROL Actions]** op **[!UICONTROL Edit]** voor de naam van de gegevensbron die u wilt wijzigen.
1. Stel op de pagina [!DNL Edit Ranking Rule] de gewenste opties in. Velden met een sterretje (*) zijn verplicht.

   Zie de optietabel onder [Een rangschikkingsregel toevoegen](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A).
1. Klik op **[!UICONTROL Save Changes]**.
1. Maak de gefaseerde website-index opnieuw om een voorvertoning van de resultaten van de regelbewerking weer te geven.

   Zie [Een volledige index van een actieve of gefaseerde website uitvoeren...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Zie [Een incrementele index van een actieve of gefaseerde website uitvoeren...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een waarderingsregel {#task_742A3BCC2A6E4164BE84CC7408807EBB} verwijderen

U kunt waarderingsregels verwijderen die u niet meer hoeft te gebruiken.

Zie [Rangschikking configureren](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5).

Zie [Een rangschikkingsregelgroep toevoegen](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8).

**Een waarderingsregel verwijderen**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. (Optioneel) Als u een regelgroep hebt gemaakt en regels aan de groep hebt toegevoegd, selecteert u op de pagina [!DNL Define Ranking Rules] in de vervolgkeuzelijst **[!UICONTROL Select Rule Group]** een regelgroep die regels bevat die u wilt verwijderen.
1. Klik in de tabel onder de kolomkop **[!UICONTROL Actions]** op **[!UICONTROL Delete]** voor de naam van de gegevensbron die u wilt wijzigen.
1. Klik op [!DNL Delete Ranking Rule] op de pagina.**[!UICONTROL Delete]**

   U bent teruggekeerd aan de [!DNL Define Ranking Rules] pagina.
1. Maak de gefaseerde website-index opnieuw om een voorvertoning weer te geven van de resultaten van de regelverwijdering.

   Zie [Een volledige index van een actieve of gefaseerde website uitvoeren...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Zie [Een incrementele index van een actieve of gefaseerde website uitvoeren...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een rangschikkingsregelgroep {#task_B65081B3CC9E4330A7FEE77B7BCD36C8} toevoegen

Als u meerdere metatags van het type &quot;rank&quot; hebt gedefinieerd, kunt u aparte verzamelingen regels maken die u kunt gebruiken voor het berekenen van de verschillende velden in de rang. U kunt een groep met rangtelregels toevoegen die u vervolgens kunt toewijzen aan een van de gedefinieerde Rank-velden.

Regelgroepen bevatten gewoonlijk een of meer regels die u hebt toegevoegd. Nochtans, kunnen de groepen van de Regel ook naar andere groepen van de Regel verwijzen. U kunt bijvoorbeeld een of meer regelgroepen maken en vervolgens veelgebruikte regels aan elke groep toevoegen. Deze regels worden vervolgens gedeeld tijdens de berekening van uw meerdere ranks.

Zie [Een rangschikkingsregelgroep bewerken](../c-about-rules-menu/c-about-ranking-rules.md#task_D3EC0437E47144BC9E754FEF99C725E5).

Zie [Een classificatieregel verwijderen](../c-about-rules-menu/c-about-ranking-rules.md#task_BE5BE01F377843BEA9846E094A07F2EA).

Zie [Rangschikkingsgroepen controleren](../c-about-rules-menu/c-about-ranking-rules.md#task_5694459D050C4254A25186038CD66B6E).

**Een groep met rangtelregels toevoegen**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. Klik op [!DNL Define Ranking Rules] rechts van de vervolgkeuzelijst **[!UICONTROL Select Rule Group]** op **[!UICONTROL Add]**.
1. Typ op de pagina [!DNL Add Ranking Rule Group] in het veld **[!UICONTROL Rule Group Name]** een unieke naam voor de nieuwe regelgroep.
1. Selecteer in de vervolgkeuzelijst **[!UICONTROL Rank Field Name]** een veldnaam voor de rangtelmetagegevens die u aan de nieuwe regelgroep wilt koppelen. Selecteer **[!UICONTROL None]** als u geen rang wilt toewijzen.

   De lijst met namen van rangvelden is afkomstig van metagegevensdefinities die zijn toegevoegd in **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**.

   Zie de optietabel in [Een nieuw metatag toevoegen gebied](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).
1. Klik op **[!UICONTROL Add]**.
1. Maak de gefaseerde website-index opnieuw om een voorvertoning weer te geven van de resultaten van de regeltoevoeging.

   Zie [Een volledige index van een actieve of gefaseerde website uitvoeren...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Zie [Een incrementele index van een actieve of gefaseerde website uitvoeren...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een rangschikkingsregelgroep {#task_D3EC0437E47144BC9E754FEF99C725E5} bewerken

U kunt de instellingen van een bestaande groep met rangtelregels bewerken.

Zie [Een rangschikkingsregelgroep toevoegen](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8).

**Een groep met rangtelregels bewerken**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. Klik op [!DNL Define Ranking Rules] rechts van de vervolgkeuzelijst **[!UICONTROL Select Rule Group]** op **[!UICONTROL Edit]**.
1. Typ op de pagina [!DNL Edit Ranking Rule Group] in het veld **[!UICONTROL Rule Group Name]** een unieke naam voor de regelgroep.
1. Selecteer in de vervolgkeuzelijst **[!UICONTROL Rank Field Name]** een veldnaam voor de rangtelmetagegevens die u aan de regelgroep wilt koppelen. Selecteer **[!UICONTROL None]** als u geen rang wilt toewijzen.

   De lijst met namen van rangvelden is afkomstig van metagegevensdefinities die zijn toegevoegd in **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**.

   Zie de optietabel in [Een nieuw metatag toevoegen gebied](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).
1. Klik op **[!UICONTROL Save Changes]**.
1. Maak de gefaseerde website-index opnieuw om een voorvertoning weer te geven van de resultaten van de regeltoevoeging.

   Zie [Een volledige index van een actieve of gefaseerde website uitvoeren...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Zie [Een incrementele index van een actieve of gefaseerde website uitvoeren...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een rangschikkingsregelgroep {#task_BE5BE01F377843BEA9846E094A07F2EA} verwijderen

U kunt een het Rangschikken Groep van de Regel schrappen die u niet meer nodig hebt of gebruikt. Wanneer u een groep verwijdert, worden Regels die aan de groep zijn toegevoegd, ook verwijderd. U kunt de standaardgroep &#39;Regels rangschikken&#39; niet verwijderen.

De inhoud van om het even welke Groepen van de Regel die in de schrappingsgroep bevat wordt niet geschrapt; alleen de verwijzingen naar deze groepen worden verwijderd.

Zorg ervoor dat u uw website opnieuw indexeert, zodat de wijziging op de juiste wijze wordt doorgevoerd in de zoekresultaten.

Zie [Een rangschikkingsregelgroep toevoegen](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8).

**Een groep met rangtelregels verwijderen**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. Selecteer op de pagina [!DNL Define Ranking Rules] in de vervolgkeuzelijst **[!UICONTROL Select Rule Group]** een groep die u wilt verwijderen.
1. Rechts van de vervolgkeuzelijst **[!UICONTROL Select Rule Group]** klikt u op **[!UICONTROL Delete]**.
1. Klik op [!DNL Delete Ranking Rule Group] op de pagina.**[!UICONTROL Delete]**
1. Maak de gefaseerde website-index opnieuw om een voorvertoning weer te geven van de resultaten van de regeltoevoeging.

   Zie [Een volledige index van een actieve of gefaseerde website uitvoeren...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Zie [Een incrementele index van een actieve of gefaseerde website uitvoeren...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Rangschikkingsgroepen bekijken {#task_5694459D050C4254A25186038CD66B6E}

U kunt het Rangschikken Overzicht van de Groepen van de Regel gebruiken om elke groepen Rank het Naam van het Gebied, en bijbehorende gegevensbron en weging te zien.

Zie [Een rangschikkingsregelgroep toevoegen](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8).

**Classificatie van regelgroepen controleren**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. Klik op [!DNL Define Ranking Rules] rechts van de vervolgkeuzelijst **[!UICONTROL Select Rule Group]** op **[!UICONTROL Overview]**.
1. Klik op [!DNL Ranking Rule Groups Overview] op de pagina **[!UICONTROL Close]** om terug te keren naar de pagina [!DNL Define Ranking Rules].
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Regels {#task_56F64EE7ED5B42E481F0990A9DD98ADB} voor testclassificatie

U kunt een geschikte URL-test opgeven voor de definities van Rangschikking die u hebt ingesteld. De metriek die in de berekeningen wordt gebruikt wordt getoond, samen met de berekende waarde van de Rank.

Zie [Informatie over rangschikkingsregels](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397).

**Classificatieregels testen**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. Typ op de pagina [!DNL Define Ranking Rules] in het gebied **[!UICONTROL Test URL]** de URL naar een webpagina op uw website.
1. Klik op **[!UICONTROL Test]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Het gewicht van waarderingsregels aanpassen {#task_3CB6FC92A66F4D99874A42D55825DB64}

U kunt de relatieve bijdragen van uw individuele Rangschikkingsregels, en de bijdrage van Rangschikking aan de definitieve onderzoeksresultaten veranderen.

Wanneer Rangschikking niet wordt bepaald, zijn de onderzoeksresultaten 100% op **[!UICONTROL Natural Relevance]** kant van de Regels &amp; de schuif van de Relevantie op **[!UICONTROL Adjust Ranking Weights]** pagina. Dit evenwicht houdt eenvoudigweg in dat de zoekresultaten alleen op zoektermen worden geordend.

Wanneer het Rangschikken wordt bepaald, wordt het bijbehorende Rank meta-gegevensgebied toegewezen een waarde van de Relevantie, die zich van 1-10 uitstrekken. De waarde 1 betekent dat de berekende Rank 10% van de zoekresultaatvolgorde vertegenwoordigt en de resterende 90% van de zoekresultaten.

Als u meer dan één Regel hebt die in een groep van de Regel wordt bepaald, bepaalt de waarde van het Gewicht van elke Regel hoeveel het resultaat van die Regel aan de totale berekende Rang bijdraagt. Stel dat u bijvoorbeeld een natuurlijk belang van 80% hebt, wat betekent dat de relevantie van het bijbehorende veld Rank 2 is. U hebt ook twee regels gedefinieerd: één met een gewicht van 3, en de tweede met een gewicht van 7. In dat geval bedraagt de bijdrage van de eerste regel aan het eindresultaat 6% ((3 / (3+7)) * 20%). De bijdrage van de tweede regel aan het eindresultaat is 14% ((7 / (3+7)) * 20%).

**Het gewicht van de rangorderegels aanpassen**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Adjust Weights]**.
1. Selecteer op de pagina [!DNL Adjust Ranking Weights] in de vervolgkeuzelijst **[!UICONTROL Select Rule Group]** een groep waarvan u de rangschikkingsdikten wilt aanpassen.
1. Sleep de schuifregelaars om de bijbehorende bijdragewaarden te wijzigen.

   Het cirkeldiagram geeft uw wijzigingen grafisch weer.
1. Klik op **[!UICONTROL Save Changes]**.
1. Maak de gefaseerde website-index opnieuw om een voorvertoning weer te geven van de resultaten van de regeltoevoeging.

   Zie [Een volledige index van een actieve of gefaseerde website uitvoeren...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Zie [Een incrementele index van een actieve of gefaseerde website uitvoeren...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).
