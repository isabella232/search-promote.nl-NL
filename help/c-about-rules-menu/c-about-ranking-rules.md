---
description: U kunt het Rangschikken Regels gebruiken om het relatieve plaatsen of het rangschikken van de onderzoeksresultaten te controleren van een klant die op de bevat inhoud van de meta-markering en de verwante metriek van de Analyse van Adobe wordt gebaseerd.
seo-description: U kunt het Rangschikken Regels gebruiken om het relatieve plaatsen of het rangschikken van de onderzoeksresultaten te controleren van een klant die op de bevat inhoud van de meta-markering en de verwante metriek van de Analyse van Adobe wordt gebaseerd.
seo-title: Over rangschikkingsregels
solution: Target
subtopic: Ranking Rules
title: Over rangschikkingsregels
topic: Rules,Site search and merchandising
uuid: 21962f9a-1d9c-442f-a6c4-5f452436c640
translation-type: tm+mt
source-git-commit: f4f69e6bdb37fb39045f8f25cffa4bf616834e54

---


# Over rangschikkingsregels{#about-ranking-rules}

U kunt het Rangschikken Regels gebruiken om het relatieve plaatsen of het rangschikken van de onderzoeksresultaten te controleren van een klant die op de bevat inhoud van de meta-markering en de verwante metriek van de Analyse van Adobe wordt gebaseerd.

## Rangschikkende regels gebruiken {#concept_F555C076759B4E81B925441CFE707397}

U bepaalt het rangschikken regels om de relatieve plaatsing van de documenten binnen uw onderzoeksresultaten te beïnvloeden, die op de inhoud van elk document wordt gebaseerd. U kunt het rangschikken regels of op meta markeringsinhoud, de metriek van de Analyse van Adobe (als uw rekening om met de Analyse van Adobe) wordt gevormd te werken, of de metriek van HBX van de Analyse van Adobe baseren (als uw rekening wordt gevormd om met de Analyse van Adobe te werken HBX).

U kunt Web-pagina&#39;s plaatsen die meta-markeringen met gewenste kenmerken, zoals een bepaalde merknaam of een prijs, of Web-pagina&#39;s bevatten die de wenselijke zeer belangrijke prestatiesindicatoren van de Analyse van Adobe, zoals unieke kijkers, hebben om een hogere rangschikking te ontvangen dan Web-pagina&#39;s die niet hebben. De &quot;wenselijke&quot;kenmerken worden gemakkelijk bijgewerkt door het toevoegen van of het uitgeven van Rangschikkende Regels en dan het re-indexeren van uw website.

Als u meer dan één meta-markering van type &quot;bepaalde rang&quot;hebt, kunt u afzonderlijke inzamelingen van regels tot stand brengen om in het berekenen van de diverse rangschikkingsgebieden te gebruiken. U kunt een rangschikkende regelgroep toevoegen, die u aan één van uw bepaalde gebieden van de Rank kunt dan toewijzen. De groepen van de regel bevatten normaal één of meerdere regeldefinities, maar kunnen ook naar andere groepen van de Regel verwijzen, zodat kunt u één of meerdere groepen algemeen gebruikte regels tot stand brengen die tijdens de berekening van uw veelvoudige ranken worden gedeeld.

Zie [Een rangschikkende regelgroep](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)toevoegen.

Een positieve rangorde bevordert onderzoeksresultaten naar de bovenkant; een negatieve rank waarde wijst onderzoeksresultaten naar de bodem van de onderzoeksresultaten aan. De normale waaier voor het rangschikken van waarden is 1.0 die de maximumbevordering binnen de onderzoeksresultaten is, terwijl -1.0 de maximumdegradatie is. Terwijl u deze waaier kunt aanpassen door het gebied van de Rank in meta-gegevensdefinities uit te geven, is dit type van aanpassing gewoonlijk onnodig.

Zie [over definities](../c-about-settings-menu/c-about-metadata-menu.md#concept_AE48035C210145169BE067D396975620).

Als u meer dan één rangschikkingsgebied onder Montages > Meta-gegevens > Definities hebt bepaald, hebt u de optie om extra reeksen rangschikkende regels, voor elk rangschikkingsgebied tot stand te brengen. U kunt extra reeksen rangschikkende regels bepalen zonder direct met een rangschikkingsgebied worden geassocieerd. Deze flexibiliteit laat u reeksen gemeenschappelijke Regels tot stand brengen die in de berekening van één of meerdere rangswaarde kunnen worden gedeeld.

**Belangrijk**: Alvorens u het Rangschikken Regels kunt gebruiken, zijn er verscheidene stappen van de rekeningsconfiguratie die u moet voltooien.

Zie rangschikken [configureren](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5)

## Rangschikking configureren {#task_4CEBC13925B047FC95BDC217B48089C5}

Alvorens u het rangschikken regels kunt gebruiken, zijn er verscheidene stappen van de rekeningsconfiguratie die u moet voltooien.

**Om rangschikking te vormen**

1. Kies uit het volgende:

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Taak </p> </th> 
      <th colname="col2" class="entry"> <p>Configuratie </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Om rangschikkende regels tot stand te brengen die op meta-markeringen gebaseerd zijn </p> </td> 
      <td colname="col2"> <p> 
      <ol id="ol_28ABB980143948DFA79AC4360AAB7556"> 
      <li id="li_544075CFA0964C6F8FAF7941AAA9ECCC"> Voor het productmenu, klik <span class="uicontrol"> Montages </span> &gt; <span class="uicontrol"> Meta-gegevens </span> &gt; <span class="uicontrol"> Definities </span>. </li> 
      <li id="li_F237F13B89E8425080C15D3BD697652C"> Voor de pagina van Definities, voegt de klik <span class="uicontrol"> Nieuw Gebied toe </span>. </li> 
      <li id="li_2A839874D71D45FEA661B3D3B8BE2A86"> Op de Add pagina van het Gebied, op het de tekstgebied van de Naam van het <span class="uicontrol"> </span> Gebied, type 
      <userinput>
        rangschikken 
      </userinput>; in het tekstveld Naam <span class="uicontrol"> meta-tag </span> , typt u 
      <userinput>
        rangschikken 
      </userinput>; in de <span class="uicontrol"> drop-down lijst van het Type van Gegevens, uitgezochte </span> Rang <span class="uicontrol"> </span>. Verlaat alle andere gebiedsopties zoals-is. <p>Zie de vraagparameter <span class="codeph"> sp_sr </span> in de parameters van het het onderzoekCGI van de <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> Achterkant </a>. </p> </li> 
      <li id="li_8E91AF4BE51A4A41ABBF9680DDE0B7CE">Klik <span class="uicontrol"> toevoegen </span>. </li> 
      </ol> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Om rangschikkende regels tot stand te brengen die op de metriek van de Analyse van Adobe gebaseerd zijn </p> </td> 
      <td colname="col2"> <p> 
      <ol id="ol_BE57CBC303D941778B10D855ADC93C68"> 
      <li id="li_8DF5D8F924B24ECBBD2D93C76C69D00C"> Zorg ervoor u de authentificatie van de Analyse van opstellingsAdobe van binnen plaatsonderzoek/merchandising hebt. <p>Zie de metrieke authentificatie van de Analyses van <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_8AA93F6273B747F9B4DE9E8DFBCBDC42" type="task" format="dita" scope="local"> de Opstelling van Adobe </a>. </p> </li> 
      <li id="li_CF7DD073FC5A432DADBD282AA8BB9920"> Selecteer en voeg een beschikbare rapportreeks toe. <p>Zie Een Adobe Analytics Report Suite <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_6DE17305EA7146DA8C30FF8FDF68A3C0" type="task" format="dita" scope="local"> toevoegen </a>. </p> </li> 
      <li id="li_9A63448577D04E028DF211D8715F943A"> Vorm de lijst van de metriek van de Analyse van Adobe die u voor de verwezenlijking van nieuwe het Rangeren Regels beschikbaar wilt zijn. <p>Zie het <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664" type="task" format="dita" scope="local"> Uitgeven van de metriek van de Analyse van Adobe van een Reeks van het Rapport </a>. </p> </li> 
      <li id="li_1ACA3611D9B44AC394604CD89209C966"> Laad de aanvankelijke metriek van de Analyse van Adobe voor uw websitepagina's. <p>Zie de gegevens van de Analyse van Adobe van de <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_2F3C55189B0A4049AB2113F2291CC181" type="task" format="dita" scope="local"> Lading </a>. </p> </li> 
      </ol> </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Voeg één of meerdere Rangschikkende Regels toe.

   Zie [Een rangschikkingsregel](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A)toevoegen.

1. Klik **[!UICONTROL regenerate your staged site index]** om een volledige-herindex van uw website (van **[!UICONTROL Index]** > uit te voeren **[!UICONTROL Full Index]**).

   Zie Een volledige index van een live of gefaseerde website [uitvoeren...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Zie [het Vormen van een stijgende index van een gefaseerde website](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. Controleer de waarden in de kolom van de Rank in **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]** om te verifiëren dat uw het Rangschikken Regels correct werden toegepast.

## Informatie over het rangschikken van documenten naar leeftijd {#topic_770815CF1B2A491F83FF765871B6F1B8}

U kunt een HTML- document op zijn leeftijd rangschikken met een exponentiële vervalfunctie. De snelheid van verval wordt gespecificeerd met een gekozen halfwaardetijd constante, de hoeveelheid tijd die moet overgaan alvorens de waarde aan de helft van zijn aanvankelijke waarde daalt.

De rangschikking van de leeftijd is gebaseerd op de volgende twee vergelijkingen:

`K = -ln(2) / H`

`RANK = e^(K * T)`

Variabelen `H` en `T` zijn input voor deze functie: de gewenste halfwaardetijd `H` is en `T` de leeftijd van het document, uitgedrukt in seconden. `K` de berekende halfwaardetijd is en het exponentiële verval van de gespecificeerde leeftijdswaarde `RANK` is. De resulterende waarde is van 0 door 1. Een recentere document heeft een rangschikkingswaarde dichter aan 1 vergeleken bij een ouder document. In theorie, zouden de documenten nooit de waarde van 0 moeten bereiken, maar het afronden van fouten kan een resultaat veroorzaken om 0 te worden.

## Voorschriften voor het gebruik van leeftijdsrangschikking {#section_D716507D589442C6B7848892BD28F966}

* Uw rekening zou reeds correct voor rangschikking moeten worden gevormd. Als het niet wordt gevormd, zie het [Vormen rangschikken](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5).
* Het HTML-document moet een HTML-meta-tagveld hebben dat de geboortedatum weergeeft, of het begin als tijdstempel, of een andere belangrijke datumwaarde.
* De speciale ingebouwde functie, `search_get_age_rank()`, zoals die in Add wordt gespecificeerd of geef de Rangschikkende pagina&#39;s van de Regel uit, wordt gebruikt om de leeftijdsrang van een document te berekenen. De volgende secties beschrijven in detail het algemene gebruik van de leeftijdsrangschikkende functie. Een voorbeeld wordt ook voorgesteld dat de leeftijd-rangschikkende eigenschap aantoont.

## Het gebruiken van search_get_age_rank () op de Add Rangschikkende pagina van de Regel of de Edit Rangschikkende pagina van de Regel {#section_34BC5276F2AB4419AD92872A397CA0AF}

Specificeer `search_get_age_rank()` als volgt:

`search_get_age_rank(Birthdate#Half_Life#Default_Rank)`

* Geboortedatum - de geboortedatum of aanloopdatum van het dossier moet een datum geformatteerd koord volgens de de datumformaten van het gebied zijn. Deze datum formatteerde koord moet een gebiedsverwijzing zijn, zoals in `{field_name}`.
* Half_Life - de halfwaardetijd is de hoeveelheid tijd die moet overgaan alvorens de waarde aan de helft van zijn aanvankelijke waarde daalt. Deze waarde wordt uitgedrukt in het aantal dagen en het is een geheel of een drijvend puntaantal.
* Default_Rank - De standaardrang wordt gebruikt als veiligheidsnet voor het geval de geboortedatum ongeldig is of de datum in de toekomst is. U kunt deze standaardwaarde niet gebruiken als zijn bijbehorend meta-gegevensgebied een geldige standaardwaarde ook heeft. De waarde hier is een drijvend puntaantal of een geheel. Zie hieronder voor suggesties als u in problemen loopt waarmee de standaardwaarde wordt gebruikt.

Zie [Een rangschikkingsregel](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A)toevoegen.

Zie [Een rangschikkende regel](../c-about-rules-menu/c-about-ranking-rules.md#task_5EBF55A43D6545FEA46BAE5E586FA275)bewerken.

**Voorbeeld**

In het volgende voorbeeld:

`search_get_age_rank({birthdate}#28#0.20)`

de datum in het `birthdate` gebied van het document wordt overgegaan binnen als tijdstempel. De halfwaardetijd is 28 dagen. De standaard rangschikkende waarde is 0.20 als de datum ongeldig is.

Zie de optieslijst in het [Toevoegen van een rangschikkende regel](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A).

In de sectie van Waarden/van Ranks van de Add Rangschikkende pagina van de Regel of de Edit Rangende pagina van de Regel, kunt u slechts `search_get_age_rank` met douane-gemaakte regels gebruiken. Daarom zeker ben dat u **Douane** van de drop-down lijst van Waarden/van Ranks kiest. Wanneer de regel de leeftijd-rangschikkende functie gebruikt, worden geen ruimten toegestaan in het waardesegment van de regel. Zeker ben dat er geen ruimten in de functieargumenten of tussen hen zijn. En er zijn geen ruimten tussen wiskundige of voorwaardelijke operatoren.

Het volgende is een voorbeeld van een waarden/ranks regel-een regel verbonden aan een tekstgebied:

`regexp .* search_get_age_rank({other_field}#365#0.20)`

Dit voorbeeld veronderstelt dat een datumwaarde `other_field` bevat. Als dit gebied zelf geen datum-type gebied is, wordt deze waarde geïnterpreteerd gebruikend de datumformaten verbonden aan het vooraf bepaalde gebied van de Datum. Anders, worden de de datumformaten van dit gebied gebruikt. Deze waarde/ranks ingang wordt gebruikt wanneer het gebied van het document, dat de Gegevensbron van de Regel identificeert, niet-leeg is, en de de terugkeerwaarde van de functie (van 0 door 1) is de toegewezen rang.

Voor een Regel verbonden aan een numeriek gebied, specifiek een gebied van de Datum:

`9999999999 search_get_age_rank({other_field}#365#0.20)`

Aangezien elk document wordt verwerkt, `other_field` wordt de waarde in omgezet in de Unix &quot;epoch&quot;vorm, gebruikend de definities van het de datumformaat van het gebied. Deze waarde wordt gebruikt in de `search_get_age_rank()` vraag. Aangezien elke &quot;epoch&quot;waarde minder dan 99999999999 (voor nu minstens) is, levert de Regel eenvoudig de terugkeerwaarde van de functie (van 0 door 1) als rang.

In beide voorafgaande voorbeelden, is het typisch dat de Gegevensbron van de Regel het zelfde gebied is dat in de `search_get_age_rank()` functie - in dit geval wordt gebruikt - `other_field` .

## Een voorbeeld van het integreren van leeftijdsrangschikking in rangschikkingsregels {#section_A86D909687CC45E19D4EA7A4A9283F28}

Het volgende is een voorbeeld van hoe u leeftijd kunt integreren rangschikkend in rangschikkende regels. Het voorbeeld toont u ook de ruwe resultaten van de leeftijd-rangschikkende functie en de resultaten van de rangschikkende regels. Het voorbeeld veronderstelt het volgende:

* De Web-pagina&#39;s die zijn gekropen hebben de meta-markering van HTML genoemd &quot;geboortedatum&quot;. De inhoud van deze markering is een tijdzegel met betrekking tot het document.
* De meta-gegevensdefinities hebben een bepaald metatag gebied voor de markering van de verjaardagsdatum. Dit gebied wordt geplaatst aan type &quot;datum.&quot;

**Rangorde**

Zie [Een nieuw meta-tagveld](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)toevoegen.

Nu voegt u een nieuwe rangschikkingsregel toe. De regel wordt bepaald om het gebied van de &quot;geboortedatum&quot;op het document te gebruiken. Een nieuwe rangschikkende regel wordt toegevoegd met de volgende geplaatste eigenschappen:

* Type gegevensbron: Meta-tag
* Naam gegevensbron: geboortedatum
* Gewicht/omstandigheden: 10 - Maximale betekenis
* Waarden/waarden: 9999999999 search_get_age_rank ({geboortedatum} #14#0.10)
* Standaardscore: -1

De regel doet verschillende dingen. Het gewicht van de regel is vastgesteld op 10. De rangeerwaarde is simpelweg het resultaat van de leeftijdsrangorde functie, een waarde van 0 door 1. Je kunt geen spaties gebruiken met `search_get_age_rank()`. Ook, merk op dat het gebied &quot;geboortedatum&quot;in steunen wordt ingesloten. Tot slot wanneer u sparen deze regel, de komma&#39;s in de definitie van Waarden/van Ranks wordt vervangen door `#` karakters; dit gedrag is normaal .

**De resultaten bekijken**

Gebruik de eigenschap van de Mening van Gegevens om de resultaten van de leeftijd-rang functie snel te zien. Voeg de aangewezen gebieden van Meta-gegevens toe. In het voorbeeld, `age_val` en `myrank` zijn de twee gebieden van Meta-gegevens die aan de Mening van Gegevens zouden moeten worden toegevoegd. Het `myrank` gebied toont hoe de leeftijd rangschikt de rangschikkende waarden beïnvloedt. Het `age_val` gebied toont de ruwe output van de exponentieel-vervalfunctie voor dat document.

## Standaardwaarden {#section_CB109EF78F914E92955D512ACFC3310E}

Het volgende is drie standaardwaarden betrokken bij de functie `search_get_age_rank()`:

* De standaardwaarde die u in de `search_get_age_rank()` functie zelf kunt ingaan.
* De standaardwaarde van de rangorde van de het Rangschikken regel.
* De standaardwaarde van de definitie van Meta-gegevens.

Afhankelijk van waar de mislukking voorkomt, kunt u verschillende standaardwaarden krijgen.

Bijvoorbeeld, zou de standaardwaarde van de definitie van Meta-gegevens nooit moeten gebeuren als het Rangschikken en het Filtreren behoorlijk worden uitgevoerd. Deze standaardwaarde is de laatste redactiewaarde wanneer geen geldige of bekende inhoud voor dat gebied van Meta-gegevens bestaat. De standaardwaarde van de rangschikkende regels kan verschijnen wanneer van verwijzingen voorzien zijn eigen bijbehorende markering en de markering mist in het document. `search_get_age_rank()` In dit geval, gaat deze regel recht naar de standaardwaarde van de regel. Als de leeftijd-rangschikkende functieverwijzingen de markering van een andere rangschikkende regel, is het mogelijk dat de standaardwaarde die in die leeftijd-rangschikkende functie wordt overgegaan wordt gebruikt als de referenced markering mist of ongeldig is.

## Een rangschikkingsregel toevoegen {#task_A132789FD4E5423DAD090DCDA7311E8A}

U kunt toevoegen [!DNL Ranking Rules] om de relatieve plaatsing van de Web-pagina&#39;s binnen uw resultaten van het Onderzoek te beïnvloeden, die op de inhoud van elke Web-pagina wordt gebaseerd.

Zie rangschikken [configureren](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5).

**Om een rangschikkende regel toe te voegen**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. (Facultatief) als u een regelingengroep hebt gecreeerd en regels aan de groep, op de [!DNL Define Ranking Rules] pagina, in de **[!UICONTROL Select Rule Group]** drop-down lijst toegevoegd, selecteer een regelgroep die de regels bevat u wilt uitgeven.

   Zie [Een rangschikkende regelgroep](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)toevoegen.
1. Voor de [!DNL Define Ranking Rules] pagina, klik **[!UICONTROL Add Rule]** om een nieuwe het Rangschikken Regel toe te voegen, of een verwijzing naar een reeks van de Regel toe te voegen.
1. Voor de [!DNL Add Ranking Rule] pagina, plaats de opties u wilt. De gebieden die met een asterisk (*) worden gemerkt worden vereist.

   Het type van Gegevensbron dat u selecteert beïnvloedt de keuzen die op de [!DNL Data Source Name] drop-down lijst beschikbaar zijn. Bijvoorbeeld, als u **[!UICONTROL Meta Tag]** als Type van Gegevensbron selecteerde, verwijst de Naam van de Gegevensbron naar de naam van een meta- markering op uw websitepagina&#39;s. Als u selecteerde, verwijst de Naam van de Gegevensbron naar één van de metrische namen van de Analyse van Adobe die u in een Reeks van het Rapport zoals die op de **[!UICONTROL Adobe Analytics Metric (Number)]****[!UICONTROL Edit Adobe Analytics Metrics]** pagina in plaatsonderzoek/merchandising wordt gevonden selecteerde.

   Zie het [Uitgeven van de metriek van de Analyse van Adobe van een Reeks](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664)van het Rapport.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Optie </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Type gegevensbron </p> </td> 
      <td colname="col2"> <p>Bepaalt de kenmerken van de gegevensbron die als input aan deze het rangschikken regel wordt gebruikt. </p> <p>De gegevensbrontypes die u kunt selecteren omvatten het volgende: 
      <ul id="ul_B0A97BF0E314495985F44A642C86918D"> 
      <li id="li_4D8BDE32853540809AE78FF5FF5677A1"> <span class="uicontrol"> Meta-tag </span> <p> Baseert deze regel op numerieke gegevens of tekstuele gegevens die binnen een genoemde meta markering op uw websitepagina's worden opgeslagen. </p> </li> 
      <li id="li_4976C31D67254C7F81D554EC49DDBB40"> <span class="uicontrol"> Metrisch van de Analyse van Adobe (Aantal) </span> <p>Baseert deze regel op numerieke metrische Analytics van Adobe die met uw plaatspagina's wordt geassocieerd. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Naam gegevensbron </p> </td> 
      <td colname="col2"> <p>Als u de Markering van <span class="uicontrol"> Meta </span> als Type van Gegevensbron koos, is dit de naam van een meta markering die binnen de pagina's van uw website wordt gevonden. De namen in het drop-down menu komen uit de lijst van bepaalde meta-gegevenswaarden die in Montages &gt; Meta-gegevens &gt; Definities werden gevormd. </p> <p>Zie <a scope="local" href="../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5" type="task" format="dita"> Een nieuw meta-tagveld toevoegen </a>. </p> <p>Als u Metrisch van de Analyse van Adobe (Aantal) als Type van Gegevensbron koos, is dit de naam van metrisch de Analyse van Adobe. De namen in het drop-down menu, komen uit de lijst bepaalde beschikbare metriek van de Analyse van Adobe die in Montages &gt; de Analyse van Adobe &gt; Metriek &gt; werden gevormd uitgeven. </p> <p>Zie het <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664" type="task" format="dita" scope="local"> Uitgeven van de metriek van de Analyse van Adobe van een Reeks van het Rapport </a>. </p> <p>Als de metrische naam van de Analyse van Adobe die u selecteerde niet reeds in <span class="uicontrol"> Montages </span> &gt; <span class="uicontrol"> Meta-gegevens </span> &gt; <span class="uicontrol"> Definities wordt bepaald </span>, worden een tekstgebied en een Add knoop getoond. Ga de naam van het Gebied van Meta-gegevens in (de naam van het meta-gegevensgebied kan niet 20 karakters overschrijden), en klik dan <span class="uicontrol"> toevoegen </span>. </p> <p>Wanneer de pagina's met de veelvoudige sleutels van de Analyse van Adobe, zoals met een productpagina worden ontmoet die veelvoudige producten toont, specificeert de Samengestelde Regeling hoe te om de veelvoudige metrische waarden van de Analyse van Adobe te behandelen verbonden aan die pagina. Selecteer één van het volgende: </p> <p> 
      <ul id="ul_D6E51748BB3949048A37C1895F2C0A58"> 
      <li id="li_04F00F382A264C96A519B0D975E25E94"> <span class="uicontrol"> Som </span> <p>Keert de som metrische waarden terug. </p> </li> 
      <li id="li_FA44219B663F4CC197BD3A094EB84396"> <span class="uicontrol"> Gemiddeld </span> <p>Keert het gemiddelde van de waarden (de som terug die door het aantal waarden wordt verdeeld). </p> </li> 
      <li id="li_F0EAAE1EA1754FFEB30F611E5550097B"> <span class="uicontrol"> Maximaal </span> <p>Keert het grootste van de waarden terug. </p> </li> 
      <li id="li_38E3E3F3D9AF4C57803B84B60223FB9D"> <span class="uicontrol"> Eerste </span> <p>Keert de waarde terug die aan de eerste sleutel beantwoordt. </p> </li> 
      <li id="li_4AEE470CE6BB4D899E975915EC226624"> <span class="uicontrol"> Laatste </span> <p>Keer de waarde terug die aan de laatste sleutel beantwoordt. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Gewicht/voorwaarden </p> </td> 
      <td colname="col2"> <p>Bevat of een eenvoudig, enig aantal van het regelgewicht, of een in paren gerangschikte lijst van de aantallen van het regelgewicht en testvoorwaarden. </p> <p>Een aantal van het regelgewicht is een waarde van 1-10 die erop wijst hoe belangrijk deze rangschikkende regel met betrekking tot de andere rangschikkende regels in het bepalen van de algemene rang van een document is. Een hoger regelgewicht wijst op hoger belang. Een gewicht van nul (0) negeert de regel. </p> <p>Verkies <span class="uicontrol"> Douane </span> van de drop-down lijst om het regelgewicht voor diverse pagina's aan te passen door een lijst van regelgewicht/testtoestenparen te bepalen. De voorwaarden van de test zijn fragmenten van Perl die worden gebruikt om de Waarden van de Gegevensbron, of globale variabelen te testen die binnen uw manuscript van de douanefilter (bijvoorbeeld, prijs, merk, seizoen, of paginameningen zoals in het volgende voorbeeld) worden bepaald. Als een testvoorwaarde aan "waar evalueert,"wordt de bijbehorende waarde van het regelgewicht toegepast. Als een testvoorwaarde aan "vals evalueert,"wordt de volgende voorwaarde in de lijst geëvalueerd. <code> 0&nbsp;({price}&nbsp;&gt;&nbsp;50.00)&nbsp;&amp;&amp;&nbsp;({brand}=~/Kuhl/)5&nbsp;{season}&nbsp;=~&nbsp;/Fall/10&nbsp;{pageviews}&nbsp;&gt;&nbsp;1000005 </code>In het douane gecreeerde gewicht/voorwaardenvoorbeeld hierboven, wordt het regelgewicht 0 toegepast als de eerste testvoorwaarde aan "waar evalueert." De prijs bevat dus een waarde van meer dan 50 en het merk bevat "Kuhl"). Als de eerste testvoorwaarde aan "vals evalueert,"wordt de volgende voorwaarde geëvalueerd. Als aan geen van de voorgaande voorwaarden is voldaan, wordt het regelgewicht 5 toegekend. </p> <p>U zou een regelgewicht zonder voorwaarde aan het eind van de lijst altijd moeten verstrekken. Als u dit niet doet, krijgt de regel een gewicht van 0 in het geval dat geen van de voorwaardentests aan "waar"evalueert. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Waarden/Ranks </p> </td> 
      <td colname="col2"> <p>Bestaat uit of één van de ingebouwde het rangschikken functies, of mogelijke inhoud van de Gegevensbron samen met gewenste ranks. </p> <p>Als u Metrisch van de Analyse van <span class="uicontrol"> Adobe (Aantal) </span> als Type van Gegevensbron koos, wordt u voorgesteld met een drop-down lijst met de volgende opties: 
      <ul id="ul_104906B6AA8547BAB6979AA37C4FAB90"> 
      <li id="li_7656A2855A054DB8B64E90FE501517AA"> <span class="uicontrol"> Auto-Rank door Orde (gebrek) </span> <p>Berekent een rang die op de relatieve positie van het document, volgens zijn Metrische Analyse van Adobe gebaseerd is. Bijvoorbeeld, dichter de positie van het document aan het top-ranked document, hoger zijn rang. </p> </li> 
      <li id="li_1A7D60EA6965434AA6D39B215C158306"> <span class="uicontrol"> Auto-Rank door Waarde </span> <p>Berekent een rang die op de relatieve waarde van het document, volgens zijn Metrische Analyse van Adobe wordt gebaseerd. Bijvoorbeeld, dichter de waarde van het document aan de hoogste rangschikte waarde van het document, hoger zijn rang. </p> </li> 
      <li id="li_457DE44D6ADA40619DC77220BF12318E"> <span class="uicontrol"> Aangepast </span> <p>Specificeert douanemontages. Bijvoorbeeld, zou een Gegevensbron met de naam van "merk"de merknaam voor een bepaald product kunnen bevatten. Je kunt het relatieve belang van elk merk opgeven door het aan te bieden samen met de rang ervan. </p> </li> 
      </ul> </p> <p>De rangeerwaarden die van de auto-Rank berekeningen zijn teruggekeerd zijn in waaier 0.0 (het laagst) aan 1.0 (het hoogste). Zij worden niet aangepast volgens de waaiers die voor het gebied van de Rank onder Montages &gt; Meta-gegevens &gt; Definities worden bepaald. </p> <p>In het volgende voorbeeld, als de merkgegevensbron voor een bepaald onderzoeksresultaat precies "DKNY aanpast,"is de toegepaste rang voor dat resultaat 0.5. Anders, als het merk "Levis is,"is de toegepaste rang 0.1. De inhoud van de Gegevensbron moet de vastgestelde waarde aanpassen. Met andere woorden, als de inhoud van de Gegevensbron "Levis Corp."is, zal het niet de waarde "Levis"aanpassen. De kwestie wordt genegeerd, zodat "DKNY"gelijken "dkny"en "Dkny". <code> DKNY&nbsp;0.5 Levis&nbsp;0.1 Lee&nbsp;0.2 </code> </p> <p>Als geavanceerder optie, kunt u waarden als regelmatige uitdrukkingen specificeren. Bijvoorbeeld, veronderstel sommige van uw plaatspagina's een merkwaarde van "Levis"bevatten en andere plaatspagina's een merkwaarde van "de jeans van Levis." bevatten U kunt een regelmatige uitdrukking gebruiken die met het sleutelwoord wordt gespecificeerd 
      <userinput>
        regexp 
      </userinput>. </p> <p>Zie <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Regelmatige expressies </a>. </p> <p>In het volgende voorbeeld, wordt een document van het onderzoeksresultaat dat merkinhoud "de jeans van Levis"bevat toegewezen een rang van 0.1. Zoals met standaardvergelijking, wordt het geval genegeerd voor regelmatige uitdrukkingen. <code> DKNY&nbsp;0.5 regexp&nbsp;Levis.*&nbsp;0.1 Lee&nbsp;0.2 </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Standaardscore </p> </td> 
      <td colname="col2"> <p> Specificeert de rang om voor de documenten van het onderzoeksresultaat toe te passen die om het even welke gespecificeerde waarden niet aanpassen. In het bovenstaande voorbeeld wordt aan een document met zoekresultaten met een "merk" Gegevensbron met "het hiaat" de standaardwaarde toegewezen omdat "het hiaat" niet overeenkomt met een van de gedefinieerde waarden. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Opmerkingen </p> </td> 
      <td colname="col2"> <p>Voeg informatie toe die tot de rangschikkende regeldefinitie of de definitie van de regelgroep behoort die u creeerde. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   De waaier van geldige rank waarden is normaal -1.0 tot 1.0 zoals in het volgende:

   * `-1.0` is &quot;MinimumRank (vertoning lager in de onderzoeksresultaten).&quot;
   * `0.0` is &quot;Neutrale rang (verander niet de orde van onderzoeksresultaten).&quot;
   * `1.0` is &quot;Maximum rang (vertoning hoger in de onderzoeksresultaten.&quot;
   De bepaalde ranken zouden binnen de zelfde waaier voor elke regel moeten zijn. De rangschikkingswaaiers moeten ook de waaiers aanpassen die voor het gebied van de Rank onder **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > worden bepaald **[!UICONTROL Definitions]**.

   Zie [Een nieuw meta-tagveld](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)toevoegen.

   Zie ook een rangschikkende regel [](../c-about-rules-menu/c-about-ranking-rules.md#task_5EBF55A43D6545FEA46BAE5E586FA275)bewerken.
1. Klik op **[!UICONTROL Add]**.
1. Aan voorproef de resultaten van de regeltoevoeging, klik **[!UICONTROL regenerate your staged site index]** om uw gefaseerde websiteindex te herbouwen.

   Zie Een volledige index van een live of gefaseerde website [uitvoeren...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Zie Een incrementele index van een live of gefaseerde website [uitvoeren...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een rangschikkingsregel bewerken {#task_5EBF55A43D6545FEA46BAE5E586FA275}

U kunt een bestaande rangschikkende regel uitgeven die u reeds hebt toegevoegd.

Zie rangschikken [configureren](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5).

**Om een rangschikkende regel uit te geven**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. (Facultatief) als u een regelingengroep hebt gecreeerd en om het even welke regels aan de groep toegevoegd, op de **[!UICONTROL Define Ranking Rules]** pagina, in de **[!UICONTROL Select Rule Group]** drop-down lijst, selecteer een regelgroep die de regels bevat u wilt uitgeven.

   Zie [Een rangschikkende regelgroep](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)toevoegen.
1. In de lijst, onder de **[!UICONTROL Actions]** kolomkopbal, klik **[!UICONTROL Edit]** voor de gegevensbronnaam u wilt veranderen.
1. Voor de [!DNL Edit Ranking Rule] pagina, plaats de opties die u wilt. De gebieden die met een asterisk (*) worden gemerkt worden vereist.

   Zie de lijst van opties onder het [Toevoegen van een rangschikkende regel](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A).
1. Klik op **[!UICONTROL Save Changes]**.
1. Herbouw uw gefaseerde websiteindex aan voorproef de resultaten van de regel uitgeven.

   Zie Een volledige index van een live of gefaseerde website [uitvoeren...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Zie Een incrementele index van een live of gefaseerde website [uitvoeren...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een rangschikkingsregel verwijderen {#task_742A3BCC2A6E4164BE84CC7408807EBB}

U kunt het rangschikken regels schrappen die u niet meer te gebruiken.

Zie rangschikken [configureren](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5).

Zie [Een rangschikkende regelgroep](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)toevoegen.

**Om een rangschikkende regel te schrappen**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. (Facultatief) als u een regelingengroep hebt gecreeerd en om het even welke regels aan de groep toegevoegd, op de [!DNL Define Ranking Rules] pagina, in de **[!UICONTROL Select Rule Group]** drop-down lijst, selecteer een regelgroep die regels bevat die u wilt schrappen.
1. In de lijst, onder de **[!UICONTROL Actions]** kolomkopbal, klik **[!UICONTROL Delete]** voor de gegevensbronnaam u wilt veranderen.
1. Voor de [!DNL Delete Ranking Rule] pagina, klik **[!UICONTROL Delete]**.

   Je wordt teruggestuurd naar de [!DNL Define Ranking Rules] pagina.
1. Herbouw uw gefaseerde websiteindex aan voorproef de resultaten van de regelschrapping.

   Zie Een volledige index van een live of gefaseerde website [uitvoeren...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Zie Een incrementele index van een live of gefaseerde website [uitvoeren...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een rangschikkende regelgroep toevoegen {#task_B65081B3CC9E4330A7FEE77B7BCD36C8}

Als u meer dan één meta-markering van type &quot;rang&quot;hebt bepaald, kunt u afzonderlijke inzamelingen van regels tot stand brengen om in het berekenen van de diverse rangschikkingsgebieden te gebruiken. U kunt een rangschikkende regelgroep toevoegen, die u aan één van uw bepaalde gebieden van de Rank kunt dan toewijzen.

De groepen van de regel bevatten gewoonlijk één of meerdere regels die u hebt toegevoegd. Nochtans, kunnen de groepen van de Regel ook naar andere groepen van de Regel verwijzen. Bijvoorbeeld, kunt u één of meerdere regelingengroepen tot stand brengen en dan algemeen gebruikte regels toevoegen aan elke. Die regels worden dan gedeeld tijdens de berekening van uw veelvoudige ranken.

Zie [Een rangschikkende regelgroep](../c-about-rules-menu/c-about-ranking-rules.md#task_D3EC0437E47144BC9E754FEF99C725E5)bewerken.

Zie een rangschikkende regelgroep [](../c-about-rules-menu/c-about-ranking-rules.md#task_BE5BE01F377843BEA9846E094A07F2EA)verwijderen.

Zie Rangordegroepen [herzien](../c-about-rules-menu/c-about-ranking-rules.md#task_5694459D050C4254A25186038CD66B6E).

**Om een rangschikkende regelgroep toe te voegen**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. Klik op de [!DNL Define Ranking Rules] pagina rechts van de **[!UICONTROL Select Rule Group]** vervolgkeuzelijst op **[!UICONTROL Add]**.
1. Op de [!DNL Add Ranking Rule Group] pagina, op het **[!UICONTROL Rule Group Name]** gebied, typ een unieke naam voor de nieuwe regelgroep.
1. In de **[!UICONTROL Rank Field Name]** drop-down lijst, selecteer een het gebiedsnaam van de rangmeta-gegevens die u met de nieuwe regelgroep wilt associëren. Selecteer **[!UICONTROL None]** als u geen rang wilt toewijzen.

   De lijst van de namen van het rank gebied komt uit meta-gegevensdefinities die in **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]** werden toegevoegd.

   Zie de lijst van opties in het [Toevoegen van een nieuw gebied](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)van de meta- markering.
1. Klik op **[!UICONTROL Add]**.
1. Herbouw uw gefaseerde websiteindex aan voorproef de resultaten van de regeltoevoeging.

   Zie Een volledige index van een live of gefaseerde website [uitvoeren...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Zie Een incrementele index van een live of gefaseerde website [uitvoeren...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een rangschikkende regelgroep bewerken {#task_D3EC0437E47144BC9E754FEF99C725E5}

U kunt de montages van een bestaande rangschikkende regelgroep uitgeven.

Zie [Een rangschikkende regelgroep](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)toevoegen.

**Om een rangschikkende regelgroep uit te geven**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. Klik op de [!DNL Define Ranking Rules] pagina rechts van de **[!UICONTROL Select Rule Group]** vervolgkeuzelijst op **[!UICONTROL Edit]**.
1. Op de [!DNL Edit Ranking Rule Group] pagina, op het **[!UICONTROL Rule Group Name]** gebied, typ een unieke naam voor de regelgroep.
1. In de **[!UICONTROL Rank Field Name]** drop-down lijst, selecteer een het gebiedsnaam van de rangmeta-gegevens die u met de regelgroep wilt associëren. Selecteer **[!UICONTROL None]** als u geen rang wilt toewijzen.

   De lijst van de namen van het rank gebied komt uit meta-gegevensdefinities die in **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]** werden toegevoegd.

   Zie de lijst van opties in het [Toevoegen van een nieuw gebied](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)van de meta- markering.
1. Klik op **[!UICONTROL Save Changes]**.
1. Herbouw uw gefaseerde websiteindex aan voorproef de resultaten van de regeltoevoeging.

   Zie Een volledige index van een live of gefaseerde website [uitvoeren...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Zie Een incrementele index van een live of gefaseerde website [uitvoeren...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Het schrappen van een het rangschikken regelgroep {#task_BE5BE01F377843BEA9846E094A07F2EA}

U kunt een het Rangen Groep van de Regel schrappen die u niet meer nodig hebt of gebruikt. Wanneer u een groep schrapt, worden om het even welke Regels die aan de groep werden toegevoegd, ook geschrapt. U kunt niet de standaard &quot;rangschikkende Regels&quot;groep schrappen.

De inhoud van om het even welke Groepen van de Regel die in de schrappingsgroep bevat worden niet geschrapt; alleen de verwijzingen naar deze groepen worden verwijderd .

Zorg ervoor dat u uw website opnieuw instelt, zodat de wijziging correct wordt weergegeven in de zoekresultaten.

Zie [Een rangschikkende regelgroep](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)toevoegen.

**Om een rangschikkende regelgroep te schrappen**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. Voor de [!DNL Define Ranking Rules] pagina, in de **[!UICONTROL Select Rule Group]** drop-down lijst, selecteer een groep die u wilt schrappen.
1. To the right of the **[!UICONTROL Select Rule Group]** drop-down list, click **[!UICONTROL Delete]**.
1. Voor de [!DNL Delete Ranking Rule Group] pagina, klik **[!UICONTROL Delete]**.
1. Herbouw uw gefaseerde websiteindex aan voorproef de resultaten van de regeltoevoeging.

   Zie Een volledige index van een live of gefaseerde website [uitvoeren...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Zie Een incrementele index van een live of gefaseerde website [uitvoeren...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Beoordelen van rangordegroepen {#task_5694459D050C4254A25186038CD66B6E}

U kunt het Rangschikken Overzicht van de Groepen van de Regel gebruiken om elke naam van het Gebied van de Rank, en bijbehorende gegevensbron en weging te zien.

Zie [Een rangschikkende regelgroep](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)toevoegen.

**Om rangschikkende regelgroepen te herzien**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. Klik op de [!DNL Define Ranking Rules] pagina rechts van de **[!UICONTROL Select Rule Group]** vervolgkeuzelijst op **[!UICONTROL Overview]**.
1. Voor de [!DNL Ranking Rule Groups Overview] pagina, klik **[!UICONTROL Close]** om aan de [!DNL Define Ranking Rules] pagina terug te keren.
1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Rangschikkingsregels voor tests {#task_56F64EE7ED5B42E481F0990A9DD98ADB}

U kunt een geschikte test URL de het Rangschikken definities verstrekken van de Regel die u opstelling hebt. De metriek die in de berekeningen wordt gebruikt worden getoond, samen met de berekende waarde van de Rank.

Zie [over rangschikkingsregels](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397).

**Om rangschikkingsregels te testen**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. Op de [!DNL Define Ranking Rules] pagina, in het **[!UICONTROL Test URL]** gebied, typ URL aan een Web-pagina die op uw website is.
1. Klik op **[!UICONTROL Test]**.
1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Aanpassen van het gewicht in verband met de rangschikkingsregels {#task_3CB6FC92A66F4D99874A42D55825DB64}

U kunt de relatieve bijdragen van uw individuele Rangschikkende Regels, en de bijdrage van het Rangschikken aan de definitieve onderzoeksresultaten veranderen.

Wanneer het Rangschikken niet wordt bepaald, zijn de onderzoeksresultaten 100% op de **[!UICONTROL Natural Relevance]** kant van de de schuifbar van Regels &amp; van de Relevantie op de **[!UICONTROL Adjust Ranking Weights]** pagina. Dit evenwicht betekent eenvoudig dat de onderzoeksresultaten worden bevolen gebaseerd slechts op onderzoekstermijnen.

Wanneer het Rangeren wordt bepaald, wordt het bijbehorende de meta-gegevensgebied van de Rank toegewezen een waarde van de Relevantie, die zich van 1-10 uitstrekt. Een waarde van 1 betekent dat de berekende Rank 10% van het onderzoeksresultaat dat tot opdracht geeft, en Natural Relevance de resterende 90% uitmaakt.

Als u meer dan één Regel hebt die in een groep van de Regel wordt bepaald, bepaalt de waarde van het Gewicht van elke Regel hoeveel het resultaat van die Regel tot de totale berekende Rank bijdraagt. Bijvoorbeeld, veronderstel u een Natuurlijk Relevantie van 80% hebt, betekenend dat de bijbehorende relevantie van het gebied van de Rank 2 is. U hebt ook twee regels vastgesteld: één met een gewicht van 3, en de tweede met een gewicht van 7. In dat geval bedraagt de bijdrage van de eerste regel aan het eindresultaat 6% ((3 / (3 + 7)) * 20%). De bijdrage van de tweede regel aan het eindresultaat is 14% ((7 / (3+7)) * 20%).

**Om het gewicht aan te passen verbonden aan rangschikkingsregels**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Adjust Weights]**.
1. Voor de [!DNL Adjust Ranking Weights] pagina, in de **[!UICONTROL Select Rule Group]** drop-down lijst, selecteer een groep de waarvan rangschikkende gewichten u wilt aanpassen.
1. Sleep de schuiven om de overeenkomstige bijdragewaarden te veranderen.

   Het cirkeldiagram wijst op uw veranderingen grafisch.
1. Klik op **[!UICONTROL Save Changes]**.
1. Herbouw uw gefaseerde websiteindex aan voorproef de resultaten van de regeltoevoeging.

   Zie Een volledige index van een live of gefaseerde website [uitvoeren...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Zie Een incrementele index van een live of gefaseerde website [uitvoeren...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Facultatief) doe één van het volgende:

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).
