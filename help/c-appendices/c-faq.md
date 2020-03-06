---
description: ongeldig
seo-description: ongeldig
seo-title: Vaak gestelde vragen
solution: Target
title: Vaak gestelde vragen
topic: Appendices,Site search and merchandising
uuid: 4ce454a4-e770-4587-91a0-a25491818ac6
translation-type: tm+mt
source-git-commit: 4270ea66ba645ad0f71c9c8b5c2a1fcc6eb02ad2

---


# Vaak gestelde vragen{#frequently-asked-questions}

## Adobe Flash {#reference_4A25BBDE32214AF5A1A454F38FD51243}

Een vaak gestelde vragenpagina die steun van het indexeren en het zoeken van Swf- dossiers op een website bespreekt.

Het volgende is gemeenschappelijke vragen betreffende Swf- dossiers:

* [Wanneer is een Swf- dossier gekropen en geïndexeerd?](#section_01BB5259140D4D5FB04CCB7A1A63DE99)
* [Wat moet ik doen om een SWF te indexeren...](#section_0A6A52CC70D4495BBE14D91906318F95)
* [Hoe worden SWF-bestanden herkend?](#section_B36C0536AB544F509601DC6A11A8E656)
* [Hoe worden SWF-bestanden geïndexeerd?](#section_36856058A4B54FA5ABF921344F50410C)
* [Wordt een SWF-bestand als pagina geteld?](#section_0158D6DE70BC40D78E2374787B9F58AB)
* [Hoe ik het indexeren van individuele Swf- dossiers verhinderd...](#section_E38AD37989EF410B97AF5125057BFD22)
* [Hoe verhinder ik Swf- dossiers worden geïndexeerd op...](#section_DF2606A50E9A44859CFA0D44D7C5F2E4)
* [Hoe komt het dat ik de Chinese, Japanse, of Koreaanse Swf- dossiers niet op mijn website kan zoeken?](#section_EE1A3A705AE74148BD195A0CE513A5C4)

## Wanneer is een Swf- dossier gekropen en geïndexeerd? {#section_01BB5259140D4D5FB04CCB7A1A63DE99}

Een Swf- dossier is gekropen en geïndexeerd als het in een bed of objecten markering op een HTML- pagina, zoals in het volgende voorbeeld bevat is:

```
<embed src="Flash-file-URL">  
 
<object>  
<param name=movie value="Flash-file-URL">  
</object> 
```

Een Swf- dossier wordt ook erkend als u van het dossier URL als ingangspunt een lijst maakt.

Zie [het Toevoegen van veelvoudige URL ingangspunten die u geïndexeerd](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45)wilt.

## Wat moet ik doen om een Swf- dossier te indexeren? {#section_0A6A52CC70D4495BBE14D91906318F95}

Om te kruipen en de dossiers van de indexSWF, selecteer het inhoudstype **[!UICONTROL Adobe Flash Movies]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**).

Zolang uw dossier van de Flits van een `<embed>` markering of een `<object>` markering in een HTML- document van verwijzingen wordt voorzien, wordt de tekst geïndexeerd en alle URLs die in het dossier worden vermeld zijn gekropen.

Als uw dossier niet van of een `<embed>` markering of een `<object>` markering van verwijzingen wordt voorzien, kunt u van het Swf- dossier in een `<a href=...>` markering in een HTML- document of als ingangspunt een lijst maken URL.

Zie [het Toevoegen van veelvoudige URL ingangspunten die u geïndexeerd](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45)wilt.

## Hoe worden SWF-bestanden herkend? {#section_B36C0536AB544F509601DC6A11A8E656}

De swf- dossiers worden geïdentificeerd door het volgende MIME type:

`application/x-shockwave-flash`

De Swf- dossiers worden ook erkend met `application/octet-stream`&quot;of `text/plain` MIME types, op voorwaarde dat de dossieruitbreiding .swf is.

Een misconfigured server zou een verschillend type MIME voor Swf- dossiers kunnen gebruiken. Zeker ben dat u uw serverconfiguratie controleert als u problemen kruipend en indexerend Swf- dossiers hebt.

## Hoe worden SWF-bestanden geïndexeerd? {#section_36856058A4B54FA5ABF921344F50410C}

De tekst in een Swf- dossier wordt geïndexeerd alsof het `<body>` tekst in de insluitende HTML- pagina was. Als een onderzoeksresultaat tekst in een ingebed Swf- dossier vindt, verbindt het resultaat eigenlijk met de insluitende HTML- pagina en niet het Swf- dossier. Deze manier, wordt het Swf- dossier getoond in de correcte context.

Als een Swf- dossier een URL als actie van de &quot;Film van de Lading&quot;bevat, wordt de tekst in het referenced Swf- dossier geïndexeerd als deel van de insluitende HTML- pagina.

Als een Swf- dossier een URL als &quot;krijg URL&quot;actie bevat, wordt URL gekropen en later geïndexeerd, enkel aangezien een `<a href=...>` verwijzing van HTML later gekropen en geïndexeerd is.

Als een Swf- dossier als ingang URL vermeld is, wordt de Swf- dossiertekst geïndexeerd als één enkele pagina. Een onderzoeksresultaat dat tekst van een ingangSWF verbindingen direct aan de film, niet aan een insluitende HTML- pagina vindt.

Zie [het Toevoegen van veelvoudige URL ingangspunten die u geïndexeerd](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45)wilt.

## Wordt een SWF-bestand als pagina geteld? {#section_0158D6DE70BC40D78E2374787B9F58AB}

Nee. Een Swf- dossier wordt beschouwd als om een deel van zijn insluitende HTML- pagina te zijn. Al &quot;de Film van de Lading&quot;URLs in Swf- dossiers wordt bevat ook beschouwd als deel van de insluitende HTML- pagina. Daarom tellen de Swf- dossiers die van een HTML- pagina van verwijzingen worden voorzien niet als &quot;pagina&quot;voor het de paginalrootte van de rekening.

Als een Swf- dossier als ingangspunt URL vermeld is, dan worden dat Swf- dossier en al &quot;de Film van de Lading&quot;URLs die in dat Swf- dossier worden vermeld geteld als één &quot;pagina&quot;voor het de paginaaantal van de rekening.

## Hoe verhinder ik het indexeren van individuele Swf- dossiers? {#section_E38AD37989EF410B97AF5125057BFD22}

Om het indexeren van een Swf- dossier te verhinderen, kunt u of een robots meta- markering ( `<meta name="ROBOTS" content="NOINDEX">`) of een `<noindex>` markering aan het insluitende HTML- document toevoegen. Namelijk het document dat de `<embed>` of `<object>` markering bevat.

U kunt de meta-markering van robots ( `<meta name="ROBOTS" content="NOFOLLOW">`) ook gebruiken om volgende URLs te verhinderen die in het Swf- dossier bevat zijn. Als het insluitende HTML- document na gehandicapten heeft, worden URLs die als &quot;krijgen URL&quot;acties in het Swf- dossier worden vermeld niet gevolgd.

## Hoe verhinder ik Swf- dossiers op mijn website worden geïndexeerd? {#section_DF2606A50E9A44859CFA0D44D7C5F2E4}

Om SWF onbruikbaar te maken schrap het indexeren het inhoudstype **[!UICONTROL Adobe Flash Movies]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**).

U kunt ook verkiezen te gebruiken [!DNL URL Masks] om het indexeren van Swf- dossiers onbruikbaar te maken.

Zie [Toevoegend Maskers URL aan index of niet indexdelen van...](../c-about-settings-menu/c-about-crawling-menu.md#task_E1AFC17C746048B8843013D979E082C1).

Om het indexeren onbruikbaar te maken SWF, ga één van de volgende maskers URL in:

* `exclude *.swf` (als u geen reguliere expressies gebruikt)
* `exclude regexp ^.*\.swf$` (als u reguliere expressies gebruikt)

Zie [Regelmatige expressies](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

## Hoe komt het dat ik de Chinese, Japanse, of Koreaanse Swf- dossiers niet op mijn website kan zoeken? {#section_EE1A3A705AE74148BD195A0CE513A5C4}

Het onderzoek/de merchandising van de plaats verkrijgt UTF-8 van Swf- dossiers die met de Flits van Adobe worden gecreeerd. UTF-8 bevat geen taalaanduiding. Als u het inhoudstype **[!UICONTROL Adobe Flash Movies]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**) selecteerde, moet u meta-gegevensinjecties gebruiken om de taal te specificeren die door het Swf- dossier wordt gebruikt.

Zie [Veldinjectiedefinities](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)toevoegen.

Oudere SWF-bestanden geven ook geen tekenset op. Als u het inhoudstype SWF **[!UICONTROL Adobe Flash Movies]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**) selecteerde, moet u meta-gegevensinjecties gebruiken om het karakter te specificeren dat in het Swf- dossier wordt gebruikt.

## Algemene zoekopdracht {#reference_E2C675162789452A9B99C6633B12CBEF}

Een vaak gestelde vragenpagina die bespreekt hoe de plaatsonderzoek/de handel in goederen klanten die uw website bezoeken helpt vinden wat zij zoeken.

Het volgende is gemeenschappelijke vragen betreffende algemeen zoeken:

* [Moet ik om het even welke software installeren om plaats te gebruiken...](#section_02AB2AFF71984F9DAA3AF2B7C0847A22)
* [Wat gebeurt er als mijn site de paginagrens overschrijdt?](#section_ECA5FA01032D4322BABA4E2C7FE498C1)
* [Hoe verander ik het e-mailadres waar het weekblad...](#section_AE27F63DD13F425B940C8E7D9ED5C614)
* [Hoe veilig is mijn klanteninformatie over plaatsonderzoek/merchandising?](#section_5484CB954167412BB7F0480CB0C504B8)
* [Hoe zit het met de privacy van mijn klantgegevens?](#section_8FB493F15E51454BA92A0C83E14C0CC7)
* [Mag ik mijn eigen banneradvertenties laten zien op de zoektocht...](#section_611EB8B32C16418386CB7DC7FB6954B8)

Het volgende is gemeenschappelijke vragen betreffende onderzoekseigenschappen:

* [Kan ik de zoekresultaten voor mijn site aanpassen?](#section_A64B3A621B794DF78D35ED06D9C43D0B)
* [Kan ik zien wat klanten zoeken op mijn...](#section_73709E1B0E82478DA7B4D15B6C845F33)
* [Hoe kan ik controleren welke inhoudstypes (PDF, tekst, Flits, MP3 en Microsoft Office) worden geïndexeerd en worden gezocht?](#section_0AB8CB4B6BFA4286AA082055FEBFBE1C)
* [Worden dynamisch geproduceerde Web-pagina&#39;s door als ASPIS, JSP, PHP, CFM, of Perl-based inhoud gesteund?](#section_E279F004F1C542A2B9773B832E7B013F)
* [Hoe kan ik synoniemen gebruiken om de onderzoeksresultaten te verbeteren...](#section_E6E36E12514F4D7BAB01F8D1AB61D57B)
* [Heb ik controle over het opdracht geven tot van onderzoeksresultaten...](#section_C6361048502745779D9749A842C4C370)
* [Kan ik de taal van de pagina van onderzoeksresultaten veranderen...](#section_6EE41DA8241247D48BBEB061A50599C5)
* [Kan ik meer dan één plaats op mijn Adobe hebben...](#section_AFA8825182094660A71EEC84B8329D6D)
* [Kan ik meer dan één domein zoeken?](#section_BFBB0E9861D942F095B56CF0A8F16596)
* [Kan ik mijn site onderverdelen in afzonderlijke secties zodat...](#section_52153A9DE9F9493B967A70583848B2A4)
* [Hoe kan ik delen van mijn website uitsluiten van...](#section_D452EDE153654EF398F4A87780C6D43B)
* [Welke tekensets worden ondersteund?](#section_A62A6F8F15804F968C77F2DEBDE8F8FD)
* [Wat als ik mijn website verander of bijwerken?](#section_489050E0EBC14D0594DBBAA0CCF4F6BA)
* [Kan mijn site automatisch worden geïndexeerd?](#section_9C7D41636238488691ECDFEE4D4E5103)
* [Ik gebruik wachtwoorden op mijn website. Kan ik nog steeds zoeken of verhandelen op de site?](#section_4618EB5B66704640B5502D1B5CB4B32E)
* [Steunt u het kruipen en het indexeren van https of...](#section_D5BB8B8FBEA4405583E86B4AEC37151B)
* [Is het zoeken/verkopen van de plaats eer het robots.txt- dossier op mijn website?](#section_73BBF6FE93C64C109F45CBC2FA394DB2)
* [Bepaalde gedeelten van mijn website moeten regelmatig worden bijgewerkt, zodat...](#section_6D2FB1DE1B8A49729F9CCAE2A2770AB3)
* [Kan ik manuscripten of programma&#39;s gebruiken om een stijgende... in werking te stellen.](#section_0B6BB039557A42AA876D35D748E17DD0)

## Moet ik om het even welke software installeren om plaatsonderzoek/merchandising te gebruiken? {#section_02AB2AFF71984F9DAA3AF2B7C0847A22}

Nee. Dit is het primaire voordeel van plaatsonderzoek/merchandising. De engine is een professionele toepassing die volledig op onze krachtige servers wordt gehost en onderhouden. Dit maakt de software gemakkelijker te gebruiken dan andere onderzoeksoplossingen. Het enige ding u moet doen is een kleine hoeveelheid code van HTML aan uw pagina&#39;s toevoegen zodat de klanten aan uw website onderzoeken kunnen ingaan. Het zoeken/de handel van de plaats zorgt voor alle rest.

## Wat gebeurt er als mijn site de paginagrens overschrijdt? {#section_ECA5FA01032D4322BABA4E2C7FE498C1}

We blijven je zoekopdrachten bedienen zodat je bezoekers je website zonder onderbreking kunnen doorzoeken. Om te zien of overschrijdt uw website de paginagrens, herzie uw Volledige status van de Index of Levend Logboek.

Zie [over Volledige Index](../c-about-index-menu/c-about-full-index.md#concept_C69BD21863FD4856B49326F35DB570D3).

Zie het [Bekijken van het volledige indexlogboek van levend of getrapte...](../c-about-index-menu/c-about-full-index.md#task_02E5E944C56B4EB19CC1FF321F3221B8).

## Hoe verander ik het e-mailadres waar de wekelijkse rapporten worden verzonden? {#section_AE27F63DD13F425B940C8E7D9ED5C614}

Wekelijks worden de rapporten verzonden naar de eigenaar van elke actieve rekening. Je kunt het e-mailadres wijzigen door op **[!UICONTROL Settings]** > **[!UICONTROL My Profile]** > **[!UICONTROL Personal Information]** te klikken. Als u meer dan één actieve onderzoeksrekening hebt, dan worden alle bulletins verzonden naar het nieuwe adres.

Zie Je persoonlijke gebruikersgegevens [configureren](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6).

## Hoe veilig is mijn klanteninformatie over plaatsonderzoek/merchandising? {#section_5484CB954167412BB7F0480CB0C504B8}

Het onderzoek/de merchandising van de plaats is veilig, snel, stabiel, en gemakkelijk te gebruiken. U wordt niet gedwongen om koekjes te gebruiken (hoewel u kunt als u wilt) om onze producten te gebruiken, en de gevoelige informatie, zoals wachtwoorden, wordt nooit gezet op om het even welke verbinding URL die later van uw browser kan worden teruggewonnen.

## Hoe zit het met de privacy van mijn klantgegevens? {#section_8FB493F15E51454BA92A0C83E14C0CC7}

Adobe is geëngageerd aan het naleven van de privacy van hun klanten en bezoekers. Zie het Centrum van de [Privacy van Adobe](https://www.adobe.com/privacy.html).

## Kan ik mijn eigen banneradvertenties op de pagina&#39;s van onderzoeksresultaten tonen? {#section_611EB8B32C16418386CB7DC7FB6954B8}

Ja. U controleert de verschijning en de inhoud van de onderzoeksresultaten. Binnen het malplaatje van onderzoeksresultaten voor uw website, kunt u verbindingen aan uw eigen netwerk van de banneruitwisseling zoals LinkExchange of SmartClicks tot stand brengen. Alle hits van bezoekers worden correct gecrediteerd op je ruilrekening voor banners.

## Kan ik de zoekresultaten voor mijn site aanpassen? {#section_A64B3A621B794DF78D35ED06D9C43D0B}

Ja. Dit is een exclusieve eigenschap van plaatsonderzoek/merchandising. Met onze geavanceerde sjabloontechnologie en een beetje kennis van HTML, kunt u precies bepalen hoe de zoekresultaten worden weergegeven.

Zie [Zoeksjabloontags](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4).

De overgang tussen uw eigen servers en zoek-/merchandising-servers op de locatie is volledig naadloos en onzichtbaar voor uw klanten. Als u geen HTML kent of u hebt geen tijd om een douanemalplaatje tot stand te brengen, kunt u van een assortiment aantrekkelijke, gebruiksklare malplaatjes kiezen die het team van de professionele Webontwikkelaars van Adobe in huis tot stand brengt.

## Kan ik zien naar welke klanten op mijn site zoeken? {#section_73709E1B0E82478DA7B4D15B6C845F33}

Ja. We houden zoekstatistieken bij voor zoekopdrachten die bezoekers de afgelopen twee maanden op je website hebben gemaakt. U kunt deze statistieken op elk ogenblik herzien onder Rapporten over het productmenu. De rapporten van het onderzoek geven u essentiële informatie betreffende precies wat de bezoekers op uw website zoeken. U kunt deze informatie gebruiken om het ontwerp te verbeteren of de plaats te stemmen onderzoek/de koopwaar-motor om uw bezoekers beter te dienen.

## Hoe kan ik controleren welke inhoudstypes (PDF, tekst, Flits, MP3 en Microsoft Office) worden geïndexeerd en worden gezocht? {#section_0AB8CB4B6BFA4286AA082055FEBFBE1C}

U kunt rekeningen gemakkelijk vormen om het indexeren en het zoeken van tekst toe te laten of onbruikbaar te maken die binnen Pdf- documenten, gewone tekstdocumenten, de films van de Flits, MP3 dossiers, of de documenten van Microsoft Office wordt gevonden.

Deze montages worden gecontroleerd op de [!DNL Staged Content Types] pagina.

Zie [over inhoudstypen](../c-about-settings-menu/c-about-crawling-menu.md#concept_6FEA1355C0374500B4C53090C34A8A07).

## Worden dynamisch geproduceerde Web-pagina&#39;s door als ASPIS, JSP, PHP, CFM, of Perl-based inhoud gesteund? {#section_E279F004F1C542A2B9773B832E7B013F}

De statische of dynamisch geproduceerde Web-pagina&#39;s van HTML worden geïndexeerd, met inbegrip van pagina&#39;s die van gegevensbestanden, of een ander achterste-eindproces worden gebouwd. Omdat de code van HTML die browser ziet wordt geïndexeerd, kunt u plaatsonderzoek/merchandising op websites gebruiken zolang deze achterste-eindarchitectuur in HTML- pagina&#39;s resulteert.

De onderzoeksrobot kruipt uw website door met de eerste pagina bij het websiteadres te beginnen dat in wordt gespecificeerd, [!DNL Account Settings]en volgt verbindingen van pagina aan pagina volgt.

Zie [Je accountinstellingen](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)configureren.

Wanneer de zoekrobot alle pagina&#39;s van je website kruipt en indexeert, kan je de zoekmachine gebruiken om je site te doorzoeken. Met andere woorden, als dynamisch geproduceerde documenten in uw website met verbindingen van andere pagina&#39;s worden geweven, kan de onderzoeksrobot nog kruipen en de dynamische inhoud indexeren.

Nadat uw websiteinhoud is gekropen en geïndexeerd, kunnen de klanten aan uw website naar informatie binnen de geïndexeerde inhoud zoeken.

## Hoe kan ik synoniemen gebruiken om de onderzoeksresultaten voor mijn plaats te verbeteren? {#section_E6E36E12514F4D7BAB01F8D1AB61D57B}

U kunt synoniemen gebruiken wanneer u bezoekers pagina&#39;s wilt vinden die met hun onderzoeksvraag verwant zijn.

Stel bijvoorbeeld dat je een pagina hebt met een prijslijst van producten die op je site te koop zijn. Nochtans, na het onderzoeken van de onderzoeksrapporten die door plaatsonderzoek/merchandising worden verstrekt, vindt u dat de klanten het woord &quot;kosten,&quot;uitgave,&quot;last,&quot;of &quot;kosten&quot;in hun onderzoeken zoeken zoeken. Deze woorden geven de pagina met je prijslijst niet weer in de zoekresultaten. Met de [!DNL Add Synonyms] eigenschap in [!DNL Dictionaries], kunt u specificeren dat deze woorden alle synoniemen zijn, en uw klant kan uw prijslijst vinden, ongeacht welke onderzoekstermijn zij gebruiken.

Zie [over woordenboeken](../c-about-linguistics-menu/c-about-dictionaries.md#concept_B8028B71EC8144669614C64578EDB034).

## Heb ik controle over het opdracht geven tot van onderzoeksresultaten? {#section_C6361048502745779D9749A842C4C370}

Ja. Gebruikend de geavanceerde relevantieinterface, kunt u controleren welke pagina&#39;s voor een specifieke onderzoeksvraag zijn teruggekeerd. Deze eigenschap is nuttig als u zeker wilt zijn dat de klanten een specifieke pagina zien wanneer zij voor bepaalde woorden vragen.

Zie [Een nieuw meta-tagveld](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)toevoegen.

## Kan ik de taal van de pagina met zoekresultaten wijzigen? {#section_6EE41DA8241247D48BBEB061A50599C5}

Ja. Het malplaatje van het plaatsonderzoek/van de merchandising is flexibel wanneer het over het laten van u een resultatenpagina construeren die de taal van uw keus gebruikt en de verschijning van uw website aanpast.

Het malplaatje bestaat uit een combinatie tekst, de standaard markeringen van HTML, en de speciale markeringen die worden bepaald om de onderzoeksresultaten te tonen. Wanneer een klant een onderzoek uitvoert, leest de onderzoeksrobot het malplaatje, output de tekst gebruikend de standaardmarkeringen van HTML, en neemt de resultatenverbindingen op die op de speciale malplaatjemarkeringen worden gebaseerd.

Zie [Zoeksjabloontags](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4).

Als u de resultatentaal wilt veranderen, kunt u de Engelse tekst uitgeven die op het malplaatje verschijnt.

Zie Een presentatie [bewerken of een transportsjabloon](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3).

## Kan ik meer dan één plaats op mijn Login van de Klant van Adobe hebben? {#section_AFA8825182094660A71EEC84B8329D6D}

Ja. Met één enkele Login van de Klant van Adobe, kunt u een verschillende onderzoeksmotor voor vele verschillende websites beheren. Selecteer en beheer rekeningen onder &quot;Rekeningen.&quot;

Zie Een andere account [selecteren voor gebruik](../c-about-accounts-menu.md#task_03C0FE918E2D44529CDC3B8DB75D1B26).

## Kan ik meer dan één domein zoeken? {#section_BFBB0E9861D942F095B56CF0A8F16596}

Ja. U kunt toegang vormen meer dan één domein door te gebruiken [!DNL URL Entrypoints]. Verstrek entrypoints URL voor extra domeinen die u bezit. Herinner dat u toestemming moet hebben om domeinen te indexeren die u niet bezit.

Zie [over URL Inschrijvingen](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573).

## Kan ik mijn plaats in afzonderlijke secties onderverdelen zodat de klanten om het even welk van deze gebieden individueel of de volledige plaats kunnen zoeken? {#section_52153A9DE9F9493B967A70583848B2A4}

Ja. Een &quot;Inzamelingen&quot;eigenschap is inbegrepen die klanten specifieke gebieden van uw website laat zoeken om snel te vinden wat zij zoeken.

Zie [over Verzamelingen](../c-about-settings-menu/c-about-searching-menu.md#concept_62E42ACE53D54EEE9273433B86259127).

Bijvoorbeeld, kunnen de klanten een inzameling van URLs zoeken met betrekking tot de informatie van de productverkoop of een inzameling van URLs met betrekking tot de steundiensten. U kunt opstellingsinzamelingen zodat uw klanten een drop-down lijst van inzamelingen of een groep controledozen zien.

## Hoe sluit ik delen van mijn website uit om te worden doorzocht? {#section_D452EDE153654EF398F4A87780C6D43B}

Ja. Specificeer maskers URL om te bepalen welke websitepagina&#39;s u van het indexeren wilt omvatten of uitsluiten. De maskers URL bepalen of de websitepagina&#39;s in uw onderzoeksresultaten verschijnen.

Zie [over Maskers](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164)URL.

Zie [Ongeveer het manuscript](../c-about-settings-menu/c-about-filtering-menu.md#concept_384F32EA18F84853A7BA99A04009330B)van Maskers URL.

Om delen van individuele Web-pagina&#39;s te verhinderen worden gezocht, kunt u gedeelten van een pagina uitsluiten van het indexeren. Omring de tekst met `<noindex>` en `</noindex>` markeringen. Deze methode is nuttig als u navigatietekst van onderzoeken wilt uitsluiten.

## Welke tekensets worden ondersteund? {#section_A62A6F8F15804F968C77F2DEBDE8F8FD}

De pagina&#39;s van het Web specificeren typisch het karakter dat met een meta markering gelijkend op het volgende wordt geplaatst:

`<META HTTP-EQUIV="Content-Type" CONTENT="text/html; charset=iso-8859-1">`

Het plaatsonderzoek/de merchandising motor indexeert behoorlijk Web-pagina&#39;s gebruikend alle gemeenschappelijke karakterreeksen in gebruik vandaag op Internet. Enkele gesteunde karakterreeksen omvatten het volgende:

<table> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Arabisch (ISO-8859-6) </p> </td> 
   <td colname="col2"> <p>Chinees (traditioneel; Groot5) </p> </td> 
   <td colname="col3"> <p>Japans (Shift_JIS) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Arabisch (Windows-1256) </p> </td> 
   <td colname="col2"> <p>Chinees (traditioneel; EUC-TW) </p> </td> 
   <td colname="col3"> <p>Russisch (KOI8-R) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Oostzee (ISO-8859-4) </p> </td> 
   <td colname="col2"> <p>Cyrillisch (ISO-8859-5) </p> </td> 
   <td colname="col3"> <p>Zuid-Europees (ISO-8859-3) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Oostzee (Windows-1257) </p> </td> 
   <td colname="col2"> <p>Cyrillisch (Windows-1251) </p> </td> 
   <td colname="col3"> <p>Turks (ISO-8859-9) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Midden-Europa (ISO-8859-2) </p> </td> 
   <td colname="col2"> <p>Grieks (ISO-8859-7) </p> </td> 
   <td colname="col3"> <p>Turks (Windows-1254) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Midden-Europa (Windows-1250) </p> </td> 
   <td colname="col2"> <p>Grieks (Windows-1253) </p> </td> 
   <td colname="col3"> <p>Unicode (UTF-8) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chinees (ISO-2022-CN) </p> </td> 
   <td colname="col2"> <p>Hebreeuws (ISO-8859-8) </p> </td> 
   <td colname="col3"> <p>US-ASCII (us-ascii) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chinees (ISO-2022-CN-EXT) </p> </td> 
   <td colname="col2"> <p>Hebreeuws (Windows-1255) </p> </td> 
   <td colname="col3"> <p>West-Europa (ISO-8859-1) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chinees (vereenvoudigd); EUC-CN) </p> </td> 
   <td colname="col2"> <p>Japans (EUC-JP) </p> </td> 
   <td colname="col3"> <p>West-Europa (ISO-8859-15) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chinees (vereenvoudigd); GB2312) </p> </td> 
   <td colname="col2"> <p>Japans (ISO-2022-JP) </p> </td> 
   <td colname="col3"> <p>West-Europa (Windows-1252) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chinees (vereenvoudigd); GBK) </p> </td> 
   <td colname="col2"> <p>Japans (ISO-2022-JP-1) </p> </td> 
   <td colname="col3"> <p>West-Europa (x-mac-roman) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chinees (vereenvoudigd); HZ-GB-2312) </p> </td> 
   <td colname="col2"> <p>Japans (ISO-2022-JP-2) </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

Neem contact op met Technische ondersteuning om te vragen naar tekensets die hierboven niet worden vermeld.

## Wat als ik mijn website verander of bijwerken? {#section_489050E0EBC14D0594DBBAA0CCF4F6BA}

Nadat u de inhoud van uw website hebt veranderd, kunt u of een volledige index of een stijgende index uitvoeren. Het onderzoek/de handel van de plaats downloadt en indexeert om het even welke veranderde websiteinhoud. Nadat het indexeren volledig is, kunnen uw klanten de nieuwe inhoud zoeken. U kunt een automatische indexering van uw plaats op een bepaald ogenblik en op een specifieke dag ook plannen.

Zie Een volledige index van een live of gefaseerde website [uitvoeren...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

Zie Een incrementele index van een live of gefaseerde website [uitvoeren...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

Zie het [Plaatsen van het volledige indexprogramma voor een levende website](../c-about-index-menu/c-about-full-index.md#task_6760F3256D004A228B38968DF15421F0).

Zie het [Plaatsen van het stijgende indexprogramma voor een levende website](../c-about-index-menu/c-about-incremental-index.md#task_2A46BA189ECC4317A9D5C6E99A336F33).

## Kan mijn site automatisch worden geïndexeerd? {#section_9C7D41636238488691ECDFEE4D4E5103}

Ja. U kunt een automatische index van uw plaats elke dag plannen.

Naast het dagelijkse automatische indexeren, kunt u verkiezen om vaak delen van hun plaats te hebben veranderd oplopend geïndexeerd. Op dagen dat u een automatische geplande index hebt, kunt u de tijd van dag controleren de index plaatsvindt. Ook, kunt u een plaatsindex altijd manueel in werking stellen wanneer u wilt.

Zie het [Plaatsen van het volledige indexprogramma voor een levende website](../c-about-index-menu/c-about-full-index.md#task_6760F3256D004A228B38968DF15421F0).

Zie het [Plaatsen van het stijgende indexprogramma voor een levende website](../c-about-index-menu/c-about-incremental-index.md#task_2A46BA189ECC4317A9D5C6E99A336F33).

## Ik gebruik wachtwoorden op mijn website. Kan ik nog steeds zoeken of verhandelen op de site? {#section_4618EB5B66704640B5502D1B5CB4B32E}

Als u de BasisAuthentificatie van HTTP gebruikt om bepaalde gedeelten van uw website te wachtwoord-beschermen, kunt u gebieden en wachtwoorden specificeren die het plaatsonderzoek/de handel kan gebruiken om uw plaats te indexeren.

Zie Wachtwoorden [toevoegen voor het openen van gebieden van uw website die... vereisen.](../c-about-settings-menu/c-about-crawling-menu.md#task_DED19D476FF04B48BB6456D5ECB8628A).

## Steunt u kruipend en het indexeren van https of veilige serverinhoud? {#section_D5BB8B8FBEA4405583E86B4AEC37151B}

Ja. U kunt kruipen en inhoud op veilige servers (https) indexeren.

## Is het zoeken/verkopen van de plaats eer het robots.txt- dossier op mijn website? {#section_73BBF6FE93C64C109F45CBC2FA394DB2}

Ja. Het Protocol van de Uitsluiting van Robots is volgzaam. De onderzoeksrobot onderzoekt het robots.txt- dossier als het op uw website aanwezig is. Als uw robots.txt- dossier alle robots van het kruipen van uw plaats uitsluit, is het plaatsonderzoek/de koopwaar robot ook uitgesloten. Om slechts de plaats onderzoek/de koopwaar robot toe te staan om uw plaats te kruipen, plaats de inhoud van uw robots.txt- dossier aan het volgende:

```
User-agent: Atomz/1.0 
Disallow:
```

```
User-agent: * 
Disallow: /
```

U kunt meer over Webrobots en het Protocol van de Uitsluiting van Robots bij het volgende leren:

[https://www.robotstxt.org/orig.html](https://www.robotstxt.org/orig.html)

## Bepaalde gedeelten van mijn website moeten regelmatig worden bijgewerkt, zodat mijn klanten de meest nauwkeurige zoekresultaten krijgen. Helpt het stijgende indexeren met deze kwestie? {#section_6D2FB1DE1B8A49729F9CCAE2A2770AB3}

Ja. Dit scenario is wat de stijgende het indexeren eigenschap werd gebouwd om plaatsonderzoek/merchandising te vergemakkelijken. Het stijgende het indexeren is het primaire voordeel dat het bedrijven toestaat om dynamisch veranderende gedeelten van hun website vaak te indexeren. Dergelijke functionaliteit zorgt ervoor dat u onderzoeksresultaten met &quot;tot de minieme&quot;nauwkeurigheid toont.

Zie Een incrementele index van een live of gefaseerde website [uitvoeren...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

Zie het [Plaatsen van het stijgende indexprogramma voor een levende website](../c-about-index-menu/c-about-incremental-index.md#task_2A46BA189ECC4317A9D5C6E99A336F33).

## Worden dynamisch geproduceerde Web-pagina&#39;s gesteund van een achterste deelgegevensbestand, zoals productcatalogi of inventarisbeheersystemen? {#section_26896C556483457E879785E751583B16}

De statische of dynamisch geproduceerde Web-pagina&#39;s van HTML, met inbegrip van pagina&#39;s die van gegevensbestanden worden gebouwd, of een ander achterste-eindproces worden geïndexeerd. Omdat de code van HTML, zoals die door browser wordt bekeken, wordt geïndexeerd, kunt u plaatsonderzoek/merchandising op websites gebruiken zolang de achterste deelgegevensbestandinformatie in HTML- pagina&#39;s resulteert.

De onderzoeksrobot kruipt uw website door met de eerste pagina bij het websiteadres te beginnen dat in wordt gespecificeerd, [!DNL Account Settings]en volgt verbindingen van pagina aan pagina volgt.

Zie [Je accountinstellingen](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)configureren.

Wanneer de zoekrobot alle pagina&#39;s van je website kruipt en indexeert, kan je de zoekmachine gebruiken om je site te doorzoeken. Met andere woorden, als de dynamisch geproduceerde documenten in uw website met verbindingen van andere pagina&#39;s worden geweven, kan de onderzoeksrobot nog kruipen en de dynamische gegevensbestandinhoud indexeren.

Nadat uw websiteinhoud is gekropen en geïndexeerd, kunnen de klanten aan uw website naar informatie binnen de geïndexeerde inhoud zoeken.

U kunt het volledig-inhoud gemakkelijk toelaten zoekend of een meer smal op onderwerp-gebaseerd onderzoek dat tot informatie in de titel, of meta-beschrijving, of de meta-sleutelwoorden documentmarkeringen, of alle drie wordt beperkt. Gebruikend meta-gegevensdefinities, kunt u de gebieden van de douanevertoning, zoals een productbeeld, in de daadwerkelijke onderzoeksresultaten ook tot stand brengen.

Zie [Een nieuw meta-tagveld](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)toevoegen.

## Kan ik manuscripten of programma&#39;s gebruiken om een stijgende index van mijn plaats in werking te stellen? {#section_0B6BB039557A42AA876D35D748E17DD0}

Ja. U kunt manuscripten of programma&#39;s gebruiken om een stijgende index van uw website in werking te stellen, evenals de servers te pingelen om de plaats te indexeren wanneer de inhoud wordt veranderd of bijgewerkt.

Zie [over Scripted Index](../c-about-index-menu/c-about-scripted-index.md#concept_34F58D551BC04BFB8ADC294B9DA9199D).

## Implementaties van functies {#reference_2D0C4A80B8D64051BA9694D562DCE663}

Een vaak gestelde vragen pagina die diverse eigenschapimplementaties binnen bespreekt [!DNL Search&Promote].

Het volgende is gemeenschappelijke vragen betreffende eigenschapimplementaties in [!DNL Search&Promote] op een website:

* [Waarom lopen mijn bedrijfsregels niet?](#section_7FEB60383D8A4B11A60DFF9067274699)
* [Waarom heb ik problemen die indexering plannen, fouten die beginnen indexerend, en kwesties beginnen gefaseerd indexeren?](#section_E05758193DF5436784B0145839989F75)
* [Mijn grens van de indexgrootte overschrijdt mijn toegestane grens. Waarom gebeurt dit en hoe los ik het op?](#section_12E7DA979C4C4B1D8A3A6415FC3DDA70)

## Waarom lopen mijn bedrijfsregels niet? {#section_7FEB60383D8A4B11A60DFF9067274699}

Vorm bedrijfsregels wanneer de banners verschijnen, of helpen beslissen welke resultaten verschijnen en in welke orde. U kunt de positie van een punt in uw facet ook vormen, en welk malplaatje wordt gebruikt voor een bepaald onderzoek.
Geef bedrijfsregels opnieuw in orde om de orde te veranderen waarin zij op presentatiemalplaatjes lopen. De bedrijfsregels lopen in de orde dat zij werden bepaald; namelijk hoger het de ordeaantal van een regel, later loopt het in het proces, die vroegere regels trompelen. U bestelt regels door een nieuw aantal in de kolom van de Orde van de lijst op de pagina Bedrijfs van Regels opnieuw in te gaan.

Zie [over de bedrijfsregels](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

## Waarom heb ik problemen die indexering plannen, fouten die beginnen indexerend, en kwesties beginnen gefaseerd indexeren? {#section_E05758193DF5436784B0145839989F75}

Wanneer u een index produceert, of het volledig of stijgend is, kruipt de index statusinformatie in real time wordt getoond. Bijvoorbeeld, kunt u de begintijd, verstreken tijd, en om het even welke fouten bekijken die tijdens het het indexeren proces zijn voorgekomen. De informatie over het statuut van uw laatste index wordt ook getoond. Gebruik deze informatie om het even welke het indexeren fouten problemen op te lossen u ontmoet.

Voor het plannen van een index, zie het [Plaatsen van het volledige indexprogramma voor een levende website](../c-about-index-menu/c-about-full-index.md#task_6760F3256D004A228B38968DF15421F0) en het [Plaatsen van het stijgende indexprogramma voor een levende website](../c-about-index-menu/c-about-incremental-index.md#task_2A46BA189ECC4317A9D5C6E99A336F33).

Voor het beginnen van een gefaseerde index, zie het [Lopen van een volledige index van een levende of gefaseerde website...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D) of een incrementele index van een live of gefaseerde website [uitvoeren...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

## Mijn grens van de indexgrootte overschrijdt mijn toegestane grens. Waarom gebeurt dit en hoe los ik het op? {#section_12E7DA979C4C4B1D8A3A6415FC3DDA70}

Een website kan de neiging hebben om te groeien en in tijdOnderzoek &amp; promote &quot;ontdekt&quot;meer documenten en Web-pagina&#39;s die werden toegevoegd. Uiteindelijk, kan uw rekening uw het indexeren groottegrens overschrijden, in dergelijke gevallen, kunt u overwegen te gebruiken **[!UICONTROL URL Mask]**. Deze eigenschap verbergt docs en Web-pagina&#39;s van index die kruipt dat u niet wilt of niet te hoeven om geïndexeerd te hebben, daardoor verminderend uw indexgrootte. Een andere optie kan zijn contact op te nemen met de technische support om uw limiet voor de indexgrootte groter in uw account te laten instellen.

Zie [over Maskers](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164)URL.

Als u niet zeker weet wat u moet doen, neemt u contact op met Technische ondersteuning. Er kunnen vele andere variabelen zijn die uw indexgrootte beïnvloeden die, indien aangepast, ook de facturering van uw rekening kunnen beïnvloeden.

## Internationaal {#reference_F017C2968BFB446499EF1D3CE2CAC0FE}

Een vaak gestelde vragenpagina die steun van het indexeren en het zoeken van meer dan 19 talen bespreekt, met inbegrip van multi-byte Aziatische talen zoals Chinees (Vereenvoudigd en Traditioneel), Japanner, en Koreaans.

Het volgende is gemeenschappelijke vragen betreffende talen en karakterreeksen:

* [Wat controleert het karakter - vastgestelde coderen van de onderzoeksvraag...](#section_DF2E8570AFC2480FA199FD26C941A22F)
* [Zijn slechts doorzocht pagina&#39;s de waarvan het coderen het coderen van.. aanpast.](#section_9E544F3DB7DE41618DC1BC8224B32C5A)
* [Welke codering wordt gebruikt voor de pagina van onderzoeksresultaten?](#section_DA68670F35D54EAABF7DBB010F4409BF)
* [Kan ik plaatsonderzoek/merchandising op Unicode, UTF-8, gecodeerde pagina&#39;s gebruiken?](#section_130997CB08934A13A5261D85CF88040C)
* [Hoe komt het dat ik de Chinese, Japanse, of Koreaanse Pdf- dossiers niet op mijn website kan zoeken?](#section_539AFF482F814D28B5929F683D2F2175)
* [Hoe komt het dat ik de Chinese, Japanse, of Koreaanse Swf- dossiers niet op mijn website kan zoeken?](#section_9C0849528AFF4C10AA97A2C912992638)
* [Hoe komt het dat ik niet de Chinese, Japanse, of Koreaanse dossiers van Microsoft Office op mijn website kan zoeken?](#section_6764BA6863AF492EBA9BE5CCC12CDD1F)
* [Hoe komt het dat ik de Chinese, Japanse, of Koreaanse MP3 dossiers niet op mijn website kan zoeken?](#section_DB6D60CF46F94125BF4E54AF3036DBFC)
* [Moet ik iets speciaals doen om de...](#section_A8BA6DDD3A6048319D3530BCFD6DA1A5)
* [Hoe komen de Chinese, Japanse, of Koreaanse doopvonten in onderzoeksresultaten onder Netscape 4.7 en vroeger verschijnen?](#section_DF42567063304F918D406AC76529DFB7)

## Welke controles het karakter - vastgestelde coderen van de onderzoeksvraag? {#section_DF2E8570AFC2480FA199FD26C941A22F}

De sectie van de &quot;Vormen van het Web&quot;van uw rekening van het Onderzoek bevat de vormen van het steekproefonderzoek die u gebruikt om onderzoeksfunctionaliteit aan uw website toe te voegen. Als u deze code van onderzoeksvormen kijkt, kunt u een lijn gelijkend op het volgende vinden:

`<input type=hidden name="sp_f" value="iso-8859-1">`

Deze lijn van code vertelt de onderzoeksmotor dat de inkomende vraag in iso-8859-1 wordt gecodeerd, een gemeenschappelijke codering voor de talen van West-Europa. U kunt dit het plaatsen veranderen door naar het productmenu te gaan en te klikken **[!UICONTROL Settings]** > **[!UICONTROL My Profile]** > **[!UICONTROL Personal Information]**. Voor de [!DNL Personal Information] pagina, in de **[!UICONTROL Character Encoding]** drop-list, selecteer een nieuwe het coderen.

Zie Je persoonlijke gebruikersgegevens [configureren](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6).

U kunt de het coderen waarde op uw Web-pagina&#39;s ook manueel veranderen door de `sp_f` lijn van de onderzoeksvorm uit te geven. Herinner dat de `sp_f` waarde van de onderzoeksvorm het karakter moet aanpassen - vastgestelde codering van de pagina waarin het verschijnt.

## Worden slechts de pagina&#39;s gezocht de waarvan het coderen het coderen van de onderzoeksvraag aanpast? {#section_9E544F3DB7DE41618DC1BC8224B32C5A}

Standaard, nee. Zolang uw websitepagina&#39;s correct hun karakter identificeren - vastgestelde het coderen, worden de noodzakelijke omzettingen gemaakt tussen het coderen van de onderzoeksvraag en dat van de pagina&#39;s, zelfs wanneer de pagina&#39;s veelvoudige het coderen gebruiken.

## Welke codering wordt gebruikt voor de pagina van onderzoeksresultaten? {#section_DA68670F35D54EAABF7DBB010F4409BF}

Het karakter - de vastgestelde codering van uw rekening bepaalt het gebrek coderend voor uw resultatenmalplaatje.

Zie Je persoonlijke gebruikersgegevens [configureren](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6).

U kunt meer leren over het specificeren van een karakter - reeks in een malplaatje van HTML.

Zie [Zoeksjabloontags](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4).

## Kan ik plaatsonderzoek/merchandising op Unicode, UTF-8, gecodeerde pagina&#39;s gebruiken? {#section_130997CB08934A13A5261D85CF88040C}

Ja. Nochtans, verstrekken de het karakterreeksen van Unicode, zoals UTF-8, niet genoeg informatie om de taal te bepalen dat de pagina&#39;s binnen worden geschreven. Om deze pagina&#39;s correct te zoeken, is het noodzakelijk om de taal te specificeren. Om de documenttaal te bepalen, wordt de informatie verwerkt in de volgende orde:

* HTTP- kopbal van de inhoud-Taal die voor het document door uw server wordt geleverd.
* META-elementen (bijvoorbeeld `META HTTP-EQUIV="Content-Language" Content="ja_JP"`) in de `<HEAD>` sectie van het document.

* Het attribuut van de LANG van de `<HTML>` markering (bijvoorbeeld, `<HTML LANG="ja_JP">`).

Als uw server niet wordt gevormd om de inhoud-Taal HTTP- kopbal te leveren, en uw documenten noch het taalelement META, noch de taalattributen voor de `<HTML>` markering bevatten, kunt u meta-gegevensinjecties gebruiken om de aangewezen taal te specificeren.

Zie [Veldinjectiedefinities](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)toevoegen.

## Hoe komt het dat ik de Chinese, Japanse, of Koreaanse Pdf- dossiers niet op mijn website kan zoeken? {#section_539AFF482F814D28B5929F683D2F2175}

Het onderzoek/de handel van de plaats verkrijgt UTF-8 van de dossiers van Adobe PDF zonder aanwijzing van taal. Als u selecteerde **[!UICONTROL PDF Documents]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**), moet u meta-gegevensinjecties gebruiken om de taal te specificeren die in het Pdf- dossier wordt gebruikt.

Zie [Veldinjectiedefinities](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)toevoegen.

## Hoe komt het dat ik de Chinese, Japanse, of Koreaanse Swf- dossiers niet op mijn website kan zoeken? {#section_9C0849528AFF4C10AA97A2C912992638}

Het onderzoek/de merchandising van de plaats verkrijgt UTF-8 van de filmdossiers van de Flits van Adobe die met de Flits van Adobe zonder aanwijzing van taal werden gecreeerd. Als u het inhoudstype **[!UICONTROL Adobe Flash Movies]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**) selecteerde, moet u meta-gegevensinjecties gebruiken om de taal te specificeren die in het Swf- dossier wordt gebruikt.

Voor versie 4 van de Flits of oudere versies van Swf- dossiers, wordt de karakterreeks van de karakters in het dossier niet gespecificeerd. Als u het inhoudstype **[!UICONTROL Adobe Flash Movies]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**) selecteerde, moet u meta-gegevensinjecties gebruiken om het karakter te specificeren dat in het Swf- dossier wordt gebruikt.

Zie [Veldinjectiedefinities](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)toevoegen.

## Hoe komt het dat ik niet de Chinese, Japanse, of Koreaanse dossiers van Microsoft Office op mijn website kan zoeken? {#section_6764BA6863AF492EBA9BE5CCC12CDD1F}

Het onderzoek/de handel van de plaats verkrijgt UTF-8 van de dossiers van Microsoft Office (Microsoft Word, Microsoft Excel, en Microsoft PowerPoint) zonder aanwijzing van taal. Als u het inhoudstype **[!UICONTROL Microsoft Office Files]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**) selecteerde, moet u meta-gegevensinjecties gebruiken om de taal te specificeren die in de dossiers van Microsoft Office wordt gebruikt.

Zie [Veldinjectiedefinities](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)toevoegen.

## Hoe komt het dat ik de Chinese, Japanse, of Koreaanse MP3 dossiers niet op mijn website kan zoeken? {#section_DB6D60CF46F94125BF4E54AF3036DBFC}

Als u het inhoudstype **[!UICONTROL Text in MP3 Music Files]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**) selecteert, moet u meta-gegevensinjecties gebruiken om het karakter te specificeren dat wordt gebruikt om de MP3 dossiers te coderen.

Zie [Veldinjectiedefinities](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)toevoegen.

## Moet ik iets speciaals doen om de .txt dossiers op mijn website correct te krijgen om te indexeren? {#section_A8BA6DDD3A6048319D3530BCFD6DA1A5}

Als u het inhoudstype **[!UICONTROL Text Documents]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**) selecteerde, moet u meta-gegevensinjecties gebruiken om de karakterreeks te specificeren die wordt gebruikt om de .txt dossiers te coderen.

Zie [Veldinjectiedefinities](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)toevoegen.

## Hoe komen de Chinese, Japanse, of Koreaanse doopvonten in onderzoeksresultaten onder Netscape 4.7 en vroeger verschijnen? {#section_DF42567063304F918D406AC76529DFB7}

Als uw rekening het standaardmalplaatje, één van de gebruiksklare malplaatjes, of een malplaatje gebruikt dat op om het even welk van die malplaatjes wordt gebaseerd, kan het doopvontmarkeringen bevatten die Arial of Helvetica als doopvontgezichten specificeren. Bijvoorbeeld, `<font face="arial, helvetica" size="+1">`. Netscape 4.7 en vroeger toont geen Chinese, Japanse, of Koreaanse karakters wanneer het Arial of Helvetica doopvontgezicht wordt gebruikt. Verwijder de `face` attributen of vervang het doopvontgezicht met één die geschikter voor Chinees, Japanner, of Koreaan is.

## Lage paginanummer {#reference_4344E3E3CB2948939860F8C078BD7773}

Een vaak gestelde vragenpagina die gemeenschappelijke problemen verbonden aan een lage indexerende paginanummer bespreekt.

Het volgende is gemeenschappelijke vragen betreffende de lage indexerende paginantellingen:

* [Hebt u uw indexlogboek onderzocht?](#section_D6626536DC3D40DDA4A1224F1CB276BF)
* [Heb je typefouten in je URL?](#section_BD2CEABC5D0F4A0DA38F3AD72ABBA676)
* [Heeft de entrypunt Web-pagina verbindingen aan andere pagina&#39;s...](#section_1C2D6ED54E7249268B555D9DC33352B3)
* [Zijn de verbindingen aan andere pagina&#39;s op uw website ingebed in...](#section_EE34A67D60A844EBB0921C03544FF63E)
* [Zijn de markeringen van HTML op uw Web-pagina in...](#section_F31A2F5D2C284AC084158A5BD763DC5D)
* [Hebt u verkeerd gevormde de de commentaarmarkeringen van HTML in uw...](#section_D1C39D79341845CB9C38579AABDF3A24)
* [Bevat uw Web-pagina verbindingen aan pagina&#39;s op een andere...](#section_F8082759184049AAA8FA6342C1F84389)
* [Gebruikt u een virtuele domeindienst voor uw URL...](#section_2861F09EA21A45E6B7E15F032739CDF3)
* [Gebruikt uw Web-pagina een meta verfrist markering?](#section_5A2F544C237C49B8B1A7FE0C45371C0D)
* [Gebruikt uw Web-pagina een markering van meta robots?](#section_36275A33DDFE4620BABA948F8A63DBD2)
* [Gebruikt uw website een dossier van de robots uitsluiting?](#section_BF7B663347814F58AD736066C86B7D25)

## Hebt u uw indexlogboek onderzocht? {#section_D6626536DC3D40DDA4A1224F1CB276BF}

Het indexlogboek bevat gedetailleerde informatie dat de plaats onderzoek/de koopwaar robot verzamelt aangezien het uw website indexeert. Het logboek omvat een lijst van verbindingen gekropen en ondervonden fouten. Het onderzoeken van het indexlogboek is de beste plaats beginnen te bepalen waarom alle pagina&#39;s op uw website niet worden geïndexeerd.

Zie het [Bekijken van het volledige indexlogboek van levend of getrapte...](../c-about-index-menu/c-about-full-index.md#task_02E5E944C56B4EB19CC1FF321F3221B8).

Zie het [Bekijken van het stijgende indexlogboek van levend of getrapte...](../c-about-index-menu/c-about-incremental-index.md#task_E668E1F1240C476DAA1CA783DC728232).

## Heb je typefouten in je URL? {#section_BD2CEABC5D0F4A0DA38F3AD72ABBA676}

Wanneer u lange URLs in de vormen van HTML typt, kan het één of meerdere typografische fouten introduceren. Herinner dat URLs geen ruimten zou moeten bevatten. Ook, ben me ervan bewust dat sommige Webservers URLs op een case-sensitive manier behandelen.

Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**. On the [!DNL Staged URL Entrypoints] page, verify the following:

* U hebt geen typografische fouten in uw URLs.
* De karakters in URLs gebruiken allen de correcte omhulling.
* Er zijn geen ruimtekarakters in URLs.

Om uw ingangen te testen URL, kopieer en kleef een URL in Webbrowser om te zien of verschijnt uw website. Als het niet verschijnt, controleer opnieuw om ervoor te zorgen dat u geen fouten in uw weg URL hebt gemaakt.

Zie [over URL Inschrijvingen](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573).

## Heeft de entrypunt Web-pagina verbindingen aan andere pagina&#39;s op uw website? {#section_1C2D6ED54E7249268B555D9DC33352B3}

De robot voor zoeken/verkopen van sites kruipt uw website net als uw klant. door links te volgen van pagina naar pagina. De verbindingen moeten in de ingangWeb-pagina aanwezig zijn alvorens de onderzoeksrobot andere pagina&#39;s op uw plaats kan vinden en indexeren.

Zie [het Toevoegen van veelvoudige URL ingangspunten die u geïndexeerd](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45)wilt.

## Zijn de verbindingen aan andere pagina&#39;s op uw website ingebed in JavaScript? {#section_EE34A67D60A844EBB0921C03544FF63E}

U kunt verfijnde navigatietechnieken op uw website, zoals roll-over acties en menu&#39;s gebruiken, die JavaScript gebruiken om met andere pagina&#39;s te verbinden. Nochtans, kan de plaats onderzoek/de koopwaar robot geen verbindingen volgen ingebed in JavaScript.

Één oplossing u kunt gebruiken om deze kwestie te overwinnen is verborgen verbindingen aan andere pagina&#39;s in HTML te plaatsen die JavaScript bevat. Hoewel de klanten aan uw website deze verbindingen niet zien, vindt en kruipt de onderzoeksrobot hen nog steeds. U kunt verborgen markeringen bij de bodem van de pagina vlak vóór de `</body>` markering plaatsen. Zij zouden als het volgende kunnen kijken:

```
<a href="/mydir/mypag1.html"></a> 
<a href="/mydir/mypag2.html"></a>
```

Een andere oplossing moet van URLs van de extra pagina&#39;s op uw website als ingangspunten een lijst maken om te kruipen en index. Begin met URLs met `https://` zoals aangetoond in het volgende:

```
https://www.mydomain.com/mydir/mypag1.html 
https://www.mydomain.com/mydir/mypag2.html
```

Zie [het Toevoegen van veelvoudige URL ingangspunten die u geïndexeerd](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45)wilt.

## Zijn de markeringen van HTML op uw Web-pagina in een ongeldige opeenvolging? {#section_F31A2F5D2C284AC084158A5BD763DC5D}

De specificatie van HTML vereist dat de `<html>`, `<head>`, en de `<body>` markeringen een specifieke opeenvolging in een HTML- document volgen. De markeringen in al uw Web-pagina&#39;s moeten de volgende opeenvolging hebben:

```
<html> 
<head> 
...  
<i>head tags go here</i> ... 
</head> 
<body> 
...  
<i>body tags go here</i> ... 
</body> 
</html>
```

Als de HTML-tags niet in de juiste volgorde staan, kan de zoekrobot/handelswaar op de site uw webpagina niet goed ontleden en indexeren. Het volgende is een voorbeeld van markeringen die niet in de juiste opeenvolging zijn:

```
<body> 
<head> 
...  
<i>head tags are here</i> ... 
</head> 
...  
<i>body tags are here</i> ... 
</body>
```

In zulk geval, plaats de `<html>`, `<head>`, en `<body>` markeringen in de juiste opeenvolging op uw Web-pagina.

## Hebt u verkeerd de commentaarmarkeringen van HTML in uw Web-pagina gevormd? {#section_D1C39D79341845CB9C38579AABDF3A24}

Zeker ben dat u zorgvuldig om het even welke ongeldige commentaren van HTML in uw Web-pagina&#39;s herziet en verbetert.

De specificatie van HTML vereist dat een HTML- commentaar met de karakters begint `<!--` en met de karakters eindigt `-->`. Het is gemakkelijk om verkeerd geformatteerde commentaren over het hoofd te zien die de de plaatsonderzoek/koopwaar robot veroorzaken om de markeringen op uw Web-pagina verkeerd te ontleden. Een verkeerd gevormde commentaar kan de plaats onderzoek/koopwaar robot veroorzaken om andere belangrijke markeringen te missen die moeten worden ontleed. Denk aan commentaren vlak vóór de `<body>` markering in uw Web-pagina.

Het volgende is een voorbeeld van een behoorlijk gevormde commentaar:

`<!-- This HTML comment is OK. -->`

Het volgende is een voorbeeld van een verkeerd gevormde commentaren:

```
<!- This HTML comment is improperly formed. -> 
<! This HTML comment is also improperly formed. >
```

## Bevat uw Web-pagina verbindingen aan pagina&#39;s op een ander domein? {#section_F8082759184049AAA8FA6342C1F84389}

Vaak kan een website uit pagina&#39;s bestaan die eigenlijk op een Webserver met een verschillend domeinadres bestaan. Bijvoorbeeld, als uw belangrijkste websiteadres het volgende is:

`https://www.mydomain.com/`

Uw website kan pagina&#39;s op een ander domein zoals het volgende ook hebben:

`https://www.otherdomain.com/`

Door gebrek, volgt de plaatsonderzoek/de koopwaar robot geen verbindingen op een domein buiten het belangrijkste. Nochtans, door extra ingangen voor uw onderzoeksrekening te plaatsen, kunt u veelvoudige domeinen gemakkelijk indexeren.

Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**. Voeg de URL van het hoofdartikel van de website van uw site toe. Dan, voeg extra entrypoints URL aan een andere domeinen toe die plaatspagina&#39;s bevatten. Bijvoorbeeld, zou u uw belangrijkste ingang URL aan plaatsen:

`https://www.mydomain.com/`

en voeg het volgende extra plaats URL entrypoint toe:

`https://www.otherdomain.com/`

## Gebruikt u een virtuele domeindienst voor uw URL? {#section_2861F09EA21A45E6B7E15F032739CDF3}

U zou een virtuele domeindienst (soms genoemd de &quot;dienst van de domeinomleiding&quot;kunnen gebruiken) om een betere URL voor klanten te verstrekken om aan uw website te krijgen. Bijvoorbeeld, veronderstel het echte adres van uw website het volgende is:

`https://www.myispdomain.com/~myname/mywebpages/`

Nochtans, gebruikt u een virtuele domeindienst zodat kunnen de klanten aan uw plaats bij de volgende adressen krijgen:

`https://myname.adomain.com/`

of

`https://adomain.com/myname/`

Door gebrek, volgt de plaatsonderzoek/de koopwaar robot geen verbindingen op een domein buiten het belangrijkste. Nochtans, door extra ingangen voor uw onderzoeksrekening te plaatsen, kunt u veelvoudige domeinen gemakkelijk indexeren.

Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**. Voeg het &quot;belangrijkste websiteURL ingangspunt&quot;aan de virtuele domeinnaam van uw plaats toe. Dan, voeg extra ingangen aan het domein toe waar uw website eigenlijk leeft.

Bijvoorbeeld, zou u uw belangrijkste ingang URL aan het volgende plaatsen:

`https://myname.adomain.com/`

En voeg de volgende extra website URL ingang toe:

`https://www.myispdomain.com/~myname/mywebpages/`

## Gebruikt uw Web-pagina een meta verfrist markering? {#section_5A2F544C237C49B8B1A7FE0C45371C0D}

Vele websites hebben een voorpagina die meta omvat verfrist markering tussen de `<head>...</head>` markeringen gelijkend op het volgende:

`<meta http-equiv="Refresh" content="0;URL=https://www.adomain.com/apath/afile.html">`

Onder bepaalde omstandigheden, kan de plaatsonderzoek/de koopwaar robot niet de meta volgen verfrist URL om de inhoud van uw website te indexeren. Deze kwestie is gemakkelijk om rond te werken door extra ingangen te plaatsen.

Klik in het productmenu op **[!UICONTROL Settings]** > Crawling > **[!UICONTROL URL Entrypoints]**. Voeg een ander ingangspunt aan URL van meta toe verfrist markering.

## Gebruikt uw Web-pagina een markering van meta robots? {#section_36275A33DDFE4620BABA948F8A63DBD2}

Soms gebruiken de Web-pagina&#39;s meta robots markeringen om Webrobots te controleren die periodiek proberen om een website te kruipen. Meta-robots-tags worden weergegeven tussen de `<head>...</head>` tags van een webpagina en lijken op de volgende tag:

`<meta name="robots" content="noindex, nofollow">`

Omdat de robot op de site op zoek is naar/zich verkoopt als een webrobot, volgt hij de richting van de meta-robots-tag. Door andere robots op deze manier uit te sluiten, sluit u ook de robot voor zoeken/verkopen van sites uit.

U kunt meer over Webrobots en het Protocol van de Uitsluiting van Robots bij het volgende leren:

[https://www.robotstxt.org/orig.html](https://www.robotstxt.org/orig.html)

Verwijder of wijzig de markering van meta robots op de Web-pagina&#39;s die u op uw website wordt geïndexeerd wilt.

## Gebruikt uw website een dossier van de robots uitsluiting? {#section_BF7B663347814F58AD736066C86B7D25}

Soms heeft een website een pagina genaamd robots.txt die alle of bepaalde robots uitsluit van het kruipen ervan. Om te zien of heeft uw website een robots.txt dossier, zoek het enkel onder het top-level domein zoals aangetoond in het volgende:

`https://www.yourdomain.com/robots.txt`

De inhoud van het robots.txt- dossier kijkt gelijkaardig aan de volgende tekst:

```
User-agent: * 
Disallow: /
```

Omdat de site zoek/merchandising-robot zelf een webrobot is, volgt hij de richtingen in het robots.txt-bestand - het sluit het zoeken/verkopen van sites robot uit. Om rond deze kwestie te werken, geef het dossier van de uitsluiting van robots (robots.txt) uit om de plaats onderzoek/koopwaar robot toe te laten om te kruipen en uw website als volgt te indexeren:

```
User-agent: Atomz/1.0 
Disallow: 
 
User-agent: * 
Disallow: /
```

## Microsoft Office {#reference_A85FCC8A96514A7584F4D2A8AC8111D1}

Een vaak gestelde vragenpagina die steun van het indexeren en het zoeken van de dossiers van Microsoft® Office op een website bespreekt.

Het volgende is gemeenschappelijke vragen betreffende de dossiers van Microsoft Office:

* [Wat wordt geïndexeerd in een dossier van Microsoft Office?](#section_8681DADFCFE24B7787B1FC08D431EE28)
* [Wat niet wordt geïndexeerd in een dossier van Microsoft Office...](#section_BD53BDABFDD94D7EB0E1F55EC18017BB)
* [Hoe worden de dossiers van Microsoft Office verschillend van HTML- pagina&#39;s geïndexeerd..](#section_C104B44684F340549A6B9EB8F39EDDBB)
* [Hoe verhinder ik de dossiers van Microsoft Office worden geïndexeerd...](#section_FEBA71274CD14CB99731ADF982087F4C)

## Wat wordt geïndexeerd in een dossier van Microsoft Office? {#section_8681DADFCFE24B7787B1FC08D431EE28}

De volledige inhoud van de dossiers van Microsoft Word, de dossiers van Microsoft Excel, en de dossiers van Microsoft PowerPoint worden geïndexeerd.

De volgende delen van een dossier van Microsoft Word worden geïndexeerd:

* Titel
* Trefwoorden
* Onderwerp (beschrijving)
* Inhoud op basis van tekst
* Hyperlinks naar andere documenten

De volgende delen van een dossier van Microsoft Excel worden geïndexeerd:

* Titel
* Trefwoorden
* Onderwerp (beschrijving)
* Tekst in cellen
* Waarden van numerieke formules in cellen

De volgende delen van een dossier van Microsoft PowerPoint worden geïndexeerd:

* Titel
* Trefwoorden
* Onderwerp (beschrijving)
* Tekst op elke dia

## Wat wordt niet geïndexeerd in een dossier van Microsoft Office? {#section_BD53BDABFDD94D7EB0E1F55EC18017BB}

De grafiek die in de dossiers van Microsoft Office bevat zijn, of om het even welke tekst die deel van bevat grafisch uitmaakt wordt niet geïndexeerd. De het bezitsdefinities van de douane worden niet geïndexeerd als meta-gegevens. Sommige tekst op speciale gebieden, zoals kopballen en footers in een dossier van PowerPoint, wordt ook niet geïndexeerd.

## Hoe worden de dossiers van Microsoft Office verschillend van HTML- pagina&#39;s geïndexeerd? {#section_C104B44684F340549A6B9EB8F39EDDBB}

Het verschil tussen hoe de onderzoeksrobot de dossiers van Microsoft Office en HTML- dossiers indexeert is dat elk HTML- dossier een individuele pagina is en één enkel dossier van Microsoft Office kan honderden pagina&#39;s vertegenwoordigen. Om deze reden, wordt elke pagina geteld binnen een dossier van Microsoft Office als afzonderlijke pagina onder uw onderzoeksrekening.

## Hoe verhinder ik de dossiers van Microsoft Office op mijn website worden geïndexeerd? {#section_FEBA71274CD14CB99731ADF982087F4C}

Als u niet de onderzoeksrobot wilt kruipen en de dossiers van Microsoft Office indexeren, schrap het inhoudstype **[!UICONTROL Microsoft Office Files]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**).

U kunt ook gebruiken [!DNL URL Masks] om het indexeren van de dossiers van Microsoft Office onbruikbaar te maken.

Voer de volgende URL-maskers in:

<table> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Als u geen reguliere expressies gebruikt </p> </td> 
   <td colname="col2"> 
    <ul id="ul_DFEC911DA11C484C8E4671A0F00E1F88"> 
     <li id="li_2E50374E3869426B97353A5A8CBE09EC">uitsluiten *.doc </li> 
     <li id="li_9089D11161524D90849CA88F703772B6">uitsluiten *.xls </li> 
     <li id="li_7F6CFC6212E64C04AAF38E21A667C763">uitsluiten *.ppt </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Als u reguliere expressies gebruikt </p> </td> 
   <td colname="col2"> 
    <ul id="ul_012A45C3EC04460EA09C0ECFB49A8FA9"> 
     <li id="li_0C239F0A536D465F85A98EBF7B6ADF27">exclusief regexp ^ .*\.doc$ </li> 
     <li id="li_9F91DA35A2A646ACAFF2BA37F9136E2A">exclusief regexp ^ .*\.xls$ </li> 
     <li id="li_9D768D9EA2DB44FBB00A1979E21672E2">exclusief regexp ^ .*\.ppt$ </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

Zie [Toevoegend Maskers URL aan index of niet indexdelen van...](../c-about-settings-menu/c-about-crawling-menu.md#task_E1AFC17C746048B8843013D979E082C1).

Zie [Regelmatige expressies](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

## MP3 {#reference_7614250EE81C4EEFA43E57A6A74E83D7}

Een vaak gestelde vragenpagina die steun van het indexeren en het zoeken van MP3 muziekdossiers op een website bespreekt.

Het volgende is gemeenschappelijke vragen betreffende MP3 dossiers.

* [Wanneer is een MP3 dossier gekropen en geïndexeerd?](#section_538EA1682C9C47E3A62640BB25D84C36)
* [Wat moet ik doen om te kruipen en te indexeren...](#section_3CD794446E3545379C14E9F222118665)
* [Hoe wordt een MP3 dossier erkend?](#section_230E7336965A424F96C5CCF1D3C2D103)
* [Wat wordt geïndexeerd in een MP3 dossier?](#section_E99D252B27CA4946AED3FCD3ABD8779D)
* [Telt een MP3- dossier als pagina?](#section_9910BEB6617D4D2090558CDF6C65D16B)
* [Hoe verhindert ik het indexeren van individuele MP3 dossiers...](#section_C989DC1D3D3841B38F683A462195DC05)
* [Hoe verhinder ik MP3 dossiers worden geïndexeerd?](#section_305D2B28D1124776B6DC0C62A17827C6)
* [Waarom kan ik niet de Chinese, Japanse, of Koreaanse MP3 dossiers op mijn plaats zoeken?](#section_06A48DA3F9E742CC93CC8B5CCD7382FA)

## Wanneer is een MP3 dossier gekropen en geïndexeerd? {#section_538EA1682C9C47E3A62640BB25D84C36}

MP3 de dossiers zijn gekropen en index op één van twee manieren. De gemeenschappelijkste manier is van een href van het anker markering in een HTML- dossier:

`<a href="MP3-file-URL"></a>`

Een tweede manier is URL van het MP3 dossier als ingang in te gaan URL.

Zie [over URL Inschrijvingen](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573).

## Wat moet ik doen kruipen en de MP3 dossiers op mijn plaats indexeren? {#section_3CD794446E3545379C14E9F222118665}

Om MP3 te activeren kruipend en indexerend voor uw rekening, op het productmenu, klik **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**. Selecteer op de [!DNL Staged Content Types] pagina **[!UICONTROL Text in MP3 Music Files]**.

Zie [over inhoudstypen](../c-about-settings-menu/c-about-crawling-menu.md#concept_6FEA1355C0374500B4C53090C34A8A07).

## Hoe wordt een MP3 dossier erkend? {#section_230E7336965A424F96C5CCF1D3C2D103}

Een MP3 dossier wordt erkend door zijn MIME type dat &quot;audio/mpeg&quot;is.

## Wat wordt geïndexeerd in een MP3 dossier? {#section_E99D252B27CA4946AED3FCD3ABD8779D}

MP3 de dossiers slaan naar keuze een kleine hoeveelheid tekstuele informatie op. Die informatie kan de albumnaam, kunstenaarsnaam, liedtitel, liedgenre, jaar van versie, en een commentaar omvatten. Deze informatie wordt opgeslagen op het allerlaatste eind van het dossier in wat wordt genoemd TAG. MP3 de dossiers die de informatie bevatten van de TAG worden geïndexeerd door op de volgende manier:

* De titel van het lied wordt behandeld als de titel van een HTML- pagina.
* De opmerking wordt behandeld als een beschrijving die is gedefinieerd voor een HTML-pagina.
* Het genre wordt behandeld als een sleutelwoord dat voor een HTML- pagina wordt bepaald.
* De kunstenaarsnaam, de albumnaam, en het jaar van versie worden behandeld als het lichaam van een HTML- document.

## Telt een MP3- dossier als pagina? {#section_9910BEB6617D4D2090558CDF6C65D16B}

Ja, elk MP3-bestand dat gekropen en geïndexeerd is op uw website, wordt als één pagina geteld.

## Hoe verhinder ik het indexeren van individuele MP3 dossiers? {#section_C989DC1D3D3841B38F683A462195DC05}

Omring de ankermarkeringen die met de MP3 dossiers met `<nofollow>` en `</nofollow>` markeringen verbinden. De zoekrobot volgt geen links tussen die tags.

Een andere methode is URLs van de MP3 dossiers toe te voegen aangezien maskers uitsluiten.

Zie [over Maskers](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164)URL.

Zie [Ongeveer het manuscript](../c-about-settings-menu/c-about-filtering-menu.md#concept_384F32EA18F84853A7BA99A04009330B)van Maskers URL.

## Hoe verhinder ik MP3 dossiers worden geïndexeerd? {#section_305D2B28D1124776B6DC0C62A17827C6}

De gemakkelijkste manier om MP3 het indexeren voor uw rekening te controleren is door **[!UICONTROL Text in MP3 Music Files]** op de [!DNL Staged Content Types] pagina te schrappen.

Zie [het Selecteren van inhoudstypes om te kruipen en index](../c-about-settings-menu/c-about-crawling-menu.md#task_CCAC5C67C8BF4AB7B79D34A1495D5EE8).

U kunt de eigenschap van Maskers ook gebruiken URL om MP3 indexerend door dossieruitbreiding onbruikbaar te maken. Om dit te doen, op het productmenu, klik **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Masks]**. Voer een van de volgende maskers in:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Als je account... </p> </th> 
   <th colname="col2" class="entry"> <p>Voer het volgende URL-masker in </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Maakt geen gebruik van reguliere expressies </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> uitsluiten *.mp3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gebruikt regelmatige uitdrukkingen </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> exclusief regexp ^ .*\.mp3$ </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Zie [Regelmatige expressies](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

## Waarom kan ik niet de Chinese, Japanse, of Koreaanse MP3 dossiers op mijn plaats zoeken? {#section_06A48DA3F9E742CC93CC8B5CCD7382FA}

Om Chinese, Japanse, of Koreaanse MP3 dossiers, op het productmenu te zoeken, klik **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]** > **[!UICONTROL Text in MP3 Music Files]**. Dan, klik **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Injections]**, en specificeer de karakterreeks die wordt gebruikt om de MP3 dossiers te coderen.

Zie [het Selecteren van inhoudstypes om te kruipen en index](../c-about-settings-menu/c-about-crawling-menu.md#task_CCAC5C67C8BF4AB7B79D34A1495D5EE8).

Zie [over injecties](../c-about-settings-menu/c-about-metadata-menu.md#concept_DA091920671948A0A893A26B3A2FAAE5).

## PDF {#reference_F127C4915A0D436DA34E5D75ABFBB21B}

Een vaak gestelde vragen pagina bespreekt steun van het indexeren en het zoeken van Pdf- dossiers op een website.

Het volgende is gemeenschappelijke vragen betreffende Pdf- dossiers:

* [Wat wordt geïndexeerd in een Pdf- dossier?](#section_62BFCD7158B44F2BB3B1864224B50174)
* [Wat wordt niet geïndexeerd in een Pdf- dossier?](#section_A14B353AE503408896BACBBF3F748FA0)
* [Hoe worden de geïndexeerde Pdf- dossiers geteld?](#section_C35DE36A65D649BD8FF314E9EFD990A6)
* [Kunnen de onderzoeksresultaten een pictogram PDF tonen?](#section_829CE82CC3544502A13D27C4DB820189)
* [Kan de onderzoeksresultaten met een bepaalde pagina verbinden binnen...](#section_A06E7F7017E6441E98209D288EE57BF6)
* [Hoe kan ik voorkomen dat PDF-bestanden geïndexeerd worden op...](#section_96671419A822486AAC654D8DAD819940)
* [Hoe komt het dat ik de Chinese, Japanse, of Koreaanse Pdf- dossiers niet op mijn website kan zoeken?](#section_D41CA8EFCA0242EA8CF5F8F1924E4CD8)

## Wat wordt geïndexeerd in een Pdf- dossier? {#section_62BFCD7158B44F2BB3B1864224B50174}

De volledige inhoud van Pdf- dossiers wordt geïndexeerd. De volgende delen van een Pdf- dossier worden geïndexeerd:

* Titel
* Trefwoorden
* Onderwerp (beschrijving)
* Inhoud op basis van tekst

## Wat wordt niet geïndexeerd in een Pdf- dossier? {#section_A14B353AE503408896BACBBF3F748FA0}

De Pdf- inhoudstafel, om het even welke grafiek binnen het dossier, of om het even welke tekst die deel van bevat grafisch uitmaakt worden niet geïndexeerd.

## Hoe worden de geïndexeerde Pdf- dossiers geteld? {#section_C35DE36A65D649BD8FF314E9EFD990A6}

Elk Pdf- dossier wordt geteld, met inbegrip van PDFs die veelvoudige pagina&#39;s bevatten, als één enkel document.

## Kunnen de onderzoeksresultaten een pictogram PDF tonen? {#section_829CE82CC3544502A13D27C4DB820189}

Ja. Gebruik de `<search-if-link-extension>` markering binnen uw malplaatje om een pictogram PDF, of andere grafiek of tekst, in de onderzoeksresultaten te omvatten:

```
<search-results> 
  ... 
  <search-if-link-extension value=".pdf"> 
    <img src="/search/i/pdficon.gif"> 
  </search-if-link-extension> 
  ... 
</search-results>
```

De pictogrammen PDF helpen uw klanten weten dat een onderzoeksresultaat met een Pdf- dossier verbindt dat zeer groot zou kunnen zijn. De grootte van het dossier kan aan klanten van belang zijn die tot uw website over een modem of op een mobiel apparaat toegang hebben.

## Kunnen de onderzoeksresultaten met een bepaalde pagina in een Pdf- dossier verbinden? {#section_A06E7F7017E6441E98209D288EE57BF6}

Ja. Met behulp van de tag slim linksjabloon ( `<search-smart-link>...</search-smart-link>`) kunnen klanten klikken om de eerste PDF-pagina met het zoekresultaat te openen.

Om slimme verbindingen te gebruiken, vervang de `<search-link>...</search-link>` markeringen in de sectie van onderzoeksresultaten van uw malplaatje met `<search-smart-link>...</search-smart-link>` markeringen. Wanneer een klant een verbinding klikt die de slim-verbindingsmarkeringen produceren, gaan zij naar de eerste Pdf- pagina relevant voor hun onderzoeksvraag.

>[!NOTE]
>
>Om deze eigenschap te gebruiken, moet de klant een recente versie van de Acrobaat van Adobe, of de Lezer van de Acrobaat van Adobe gebruiken, die de hoogtepuntelektrische toestel en het Externe elektrische toestel van de Manager van het Venster (EWH) moet omvatten. Bovendien moet hun Webbrowser het elektrische toestel van de Acrobaat van Adobe voor de Navigator van Netscape gebruiken (u kunt om het even welke browser gebruiken die dit elektrische toestel van de Navigator van Netscape) of de controle van ActiveX van de Acrobaat voor Internet Explorer 4.0 goedkeurt en later.

Zie [Zoeksjabloontags](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4).

## Hoe kan ik voorkomen dat PDF-bestanden op mijn website worden geïndexeerd? {#section_96671419A822486AAC654D8DAD819940}

Als u niet de onderzoeksrobot wilt kruipen en PDF dossiers indexeren, schrap het inhoudstype **[!UICONTROL PDF Documents]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**).

U kunt ook verkiezen om het indexeren PDF [!DNL URL Masks] onbruikbaar te maken.

Zie [Toevoegend Maskers URL aan index of niet indexdelen van...](../c-about-settings-menu/c-about-crawling-menu.md#task_E1AFC17C746048B8843013D979E082C1).

Als u PDF-indexering wilt uitschakelen, voert u een van de volgende URL-maskers in:

* `exclude *.pdf` (als u geen reguliere expressies gebruikt)
* `exclude regexp ^.*\.pdf$` (als u reguliere expressies gebruikt)

Zie [Regelmatige expressies](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

## Hoe komt het dat ik de Chinese, Japanse, of Koreaanse Pdf- dossiers niet op mijn website kan zoeken? {#section_D41CA8EFCA0242EA8CF5F8F1924E4CD8}

Het onderzoek/de handel van de plaats verkrijgt UTF-8 van Pdf- dossiers zonder aanwijzing van taal. Als u het inhoudstype **[!UICONTROL PDF Documents]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**) selecteerde, moet u meta-gegevensinjecties gebruiken om de taal te specificeren die in het Pdf- dossier wordt gebruikt.

Zie [Veldinjectiedefinities](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)toevoegen.

## Te veel pagina&#39;s {#reference_48A748BC1ED14844ACAC2735C8388E8A}

Een vaak gestelde vraagpagina die sommige redenen verklaart waarom de indexeerder meer pagina&#39;s heeft geteld dan u eigenlijk hebt, en wat de oplossing in elk geval is.

Als u zeker bent dat uw website onder uw paginagrens ligt, maar de indexeerder vertelt u dat de limiet is bereikt, zou u deze algemene vragen en antwoorden voor mogelijke oplossingen moeten herzien.

* [Hebt u uw diverse indexlogboeken onderzocht?](#section_C929BF9FDA6B4C9A9078C45AFE80EFE8)
* [Worden CGI-programma&#39;s geïndexeerd op uw website?](#section_86ED8A641B3841EC80153B4F107548FD)
* [Heeft uw server toegelaten folder het doorbladeren?](#section_073C88EEE74F4CA0AD2C7145D4810B22)
* [Zijn er fora of nieuwsgroepen op uw website?](#section_8DCB94F0850A41B9B2EA885F779E2F84)
* [Zijn er PDF of de dossiers van Microsoft Office op uw website...](#section_455FC5438DF74E68AB9A31D359EAD4D9)
* [Heb je meerdere URL-ingangen?](#section_8C54AFD7DF56472A9364D516482B534C)
* [Heb je de interne bytes of tijdslimieten van overschreden...](#section_AE1BE61A58864FFE81F0BCEED2EBB15D)

## Hebt u uw diverse indexlogboeken onderzocht? {#section_C929BF9FDA6B4C9A9078C45AFE80EFE8}

Het indexlogboek bevat gedetailleerde informatie die door de plaats onderzoek/koopwaar robot wordt verzameld aangezien het uw website indexeert. Het logboek omvat een lijst van alle gekropen verbindingen en ontmoete fouten. Het onderzoeken van het indexlogboek is de beste te beginnen plaats wanneer u probeert om te bepalen welke pagina&#39;s geïndexeerd worden.

Zie het [Bekijken van het volledige indexlogboek van levend of getrapte...](../c-about-index-menu/c-about-full-index.md#task_02E5E944C56B4EB19CC1FF321F3221B8).

Zie het [Bekijken van het stijgende indexlogboek van levend of getrapte...](../c-about-index-menu/c-about-incremental-index.md#task_E668E1F1240C476DAA1CA783DC728232).

Zie het [Bekijken van het scripted stijgende indexlogboek van levend of...](../c-about-index-menu/c-about-scripted-index.md#task_CBFCE9B9A87B4DF7A2A35A6E83DE93D7).

Zie het [bekijken van het geregenereerde indexlogboek van een levende of getrapte...](../c-about-index-menu/c-about-regenerate-index.md#task_61CE8F9E7BF84BA89A8D482B2106BB15).

Zie het [bekijken van het opnieuw rangschikte indexlogboek van een levende of gefaseerde website](../c-about-index-menu/c-about-re-rank-index.md#task_3C76107DFAC1495FACD3ABB0A688208D).

## Worden CGI-programma&#39;s geïndexeerd op uw website? {#section_86ED8A641B3841EC80153B4F107548FD}

De programma&#39;s van CGI gebruiken parameters URL die soms de indexeerder veroorzaken om veelvoudige &quot;valse&quot;URLs te kruipen. Als het plaatsonderzoek/de merchandising uw programma&#39;s van CGI en het volgen van URLs met de parameters van CGI in hen lezen, zijn er waarschijnlijk verscheidene veelvouden van pagina&#39;s die worden gekropen en geïndexeerd die niet nuttig voor uw onderzoeksindex zijn. De typische parameters van CGI verschijnen in URLs met `?` of `&` karakters.

U kunt de programma&#39;s van CGI maskeren worden geïndexeerd gebruikend de eigenschap van Maskers URL. U kunt een prefix maskeren URL of regelmatige uitdrukkingen gebruiken om uw manuscripten van CGI te maskeren.

Zie [over Maskers](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164)URL.

Zie [Ongeveer het manuscript](../c-about-settings-menu/c-about-filtering-menu.md#concept_384F32EA18F84853A7BA99A04009330B)van Maskers URL.

Zie [Regelmatige expressies](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

## Heeft uw server toegelaten folder het doorbladeren? {#section_073C88EEE74F4CA0AD2C7145D4810B22}

Wanneer een Webserver folder toegelaten heeft doorbladeren en er geen index.html- dossier aanwezig in een bepaalde folder is, kan een bezoek aan die folder de lijst van dossiers in die folder tonen. Gewoonlijk, zijn er verbindingen bij de bovenkant van de pagina om u te laten de lijst op verschillende manieren sorteren enkel door te klikken **[!UICONTROL Name]**, **[!UICONTROL Last modified]**, **[!UICONTROL Size]** etc. Typisch, verschijnen deze in het van de plaatsonderzoek/handel drijvende indexlogboek als URLs met karakters zoals `?M=A` aan het eind. De plaats onderzoek/de handel drijvende indexeerder volgt deze als verbindingen, en dit kan tot het indexeren van veelvoudige &quot;valse&quot;URLs leiden.

Typisch, heeft een goed-ontworpen website of indexdossiers die in elke folder worden gevestigd, of het heeft folder het doorbladeren gehandicapt voor die folders zonder indexdossiers. Gelukkig, is er een gemakkelijke manier om deze &quot;valse&quot;URLs te maskeren als u niet uw pagina&#39;s kunt veranderen of folderlijsten op de serverkant onbruikbaar maken.

Om deze taak te verwezenlijken, klik **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Masks]**. Voeg een masker toe om het even welke URL te maskeren die het karakter bevat `?`. U kunt deze taak doen door het volgende regelmatige uitdrukkingsmasker in te gaan:

`exclude regexp ^.*\?.*$`

Nadat u het masker hebt gecreeerd, ben zeker dat u uw website herstelt.

Zie Een volledige index van een live of gefaseerde website [uitvoeren...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

Zie Een incrementele index van een live of gefaseerde website [uitvoeren...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

## Zijn er fora of nieuwsgroepen op uw website? {#section_8DCB94F0850A41B9B2EA885F779E2F84}

Als de forums of nieuwsgroepen op uw website worden gekropen, zou het URLs voor verschillende vertoningsopties of soortopties kunnen volgen. Dit gedrag betekent dat de zelfde pagina veelvoudige tijden wordt geïndexeerd.

Typisch, komen de forums of de nieuwsgroepen met hun eigen onderzoeksmotoren. In zulk geval, kunt u gebruiken [!DNL URL Masks] om de forums van plaatsonderzoek/merchandising te maskeren.

Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Masks]**. Op de [!DNL Staged URL Masks] pagina, maskeer uw forums door hun URLs in te gaan als sluit maskers URL uit.

Zie [Toevoegend Maskers URL aan index of niet indexdelen van...](../c-about-settings-menu/c-about-crawling-menu.md#task_E1AFC17C746048B8843013D979E082C1).

Nadat u de maskers hebt gecreeerd, ben zeker dat u uw website opnieuw indexeert.

Zie Een volledige index van een live of gefaseerde website [uitvoeren...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

Zie Een incrementele index van een live of gefaseerde website [uitvoeren...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

## Zijn er PDF of Microsoft Office dossiers op uw website? {#section_455FC5438DF74E68AB9A31D359EAD4D9}

Als u Pdf- dossiers of [!DNL Microsoft Office] - dossiers op uw website hebt, zou u kunnen opmerken dat de indexgrootte van slechts een paar dossiers vele pagina&#39;s telt. De reden dat er meer pagina&#39;s worden geïndexeerd dan documenten u hebt is omdat elke pagina in een dossier van PDF of van Microsoft Office als afzonderlijke pagina wordt geteld.

Klik in het productmenu op **[!UICONTROL Index]** > **[!UICONTROL Full Index]** > **[!UICONTROL Live Index]**. Voor de [!DNL Full Index] pagina, selecteer **[!UICONTROL Count All Pages]**, en klik dan **[!UICONTROL Full Index Now]** om een totale paginanetelling te zien. Als u geen PDF- dossiers of de geïndexeerde dossiers van Microsoft Office wilt, kunt u dit inhoudstype onder **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]** onbruikbaar maken.

Zie Een volledige index van een live of gefaseerde website [uitvoeren...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

Zie [over inhoudstypen](../c-about-settings-menu/c-about-crawling-menu.md#concept_6FEA1355C0374500B4C53090C34A8A07).

## Heb je meerdere URL-ingangen? {#section_8C54AFD7DF56472A9364D516482B534C}

De plaats onderzoek/koopwaar robot begint kruipend bij gespecificeerde ingang URL en volgt alle gevonden verbindingen aan al inhoud in dat bepaalde domein. Als u vele ingangen URL hebt gespecificeerd, kan een significant aantal pagina&#39;s worden gekropen.

Gebruik de `nofollow` markering van het Protocol van de Uitsluiting van Robots in de kopballen van de documenten van het entrypoint op de extra domeinen als volgt:

```
<html> 
<head> 
<meta name="robots" content="nofollow"> 
</head>
```

De code hierboven vertelt de plaats onderzoek/koopwaar robot om de inhoud van de pagina te indexeren, maar niet om de verbindingen aan extra pagina&#39;s te volgen.

U kunt meer over Webrobots en het Protocol van de Uitsluiting van Robots bij het volgende leren:

[https://www.robotstxt.org/orig.html](https://www.robotstxt.org/orig.html)

Als u geen toegang tot de bron van de pagina&#39;s op extra domeinen hebt, kunt u de veelvoudige ingangen verwijderen URL. Het doen van dit helpt u om indexerende activiteit slechts tot die domeinen te beperken de waarvan inhoud u klanten wilt kunnen zoeken.

Zie [over URL Inschrijvingen](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573).

## Hebt u de interne bytes of tijdslimieten van plaatsonderzoek/merchandising overschreden? {#section_AE1BE61A58864FFE81F0BCEED2EBB15D}

Controleer of uw account de limiet van het scherm &quot;Volledige indexstatus&quot; heeft bereikt. Als de status meldt dat uw index groter is dan toegestaan of dat het meer tijd heeft geduurd dan toegestaan, is uw website niet volledig geïndexeerd. U kunt deze fout verbeteren zodat u juiste dekking en telling van websitepagina&#39;s krijgt.

Om plaatsonderzoek/merchandising servers te beschermen, zijn er interne grenzen op bytes en tijd. Slechts wanneer de gekropen dossiers zeer groot zijn, of wanneer de server die het plaatsonderzoek/de handel probeert te bereiken langzaam is zijn deze grenzen bereikt.

Als u een tijdslimiet raakt, zorg ervoor dat uw server online is, en probeer opnieuw de index in een recentere tijd. Als u een bytes grens raakt, controleer de gekropen dossiers door uw indexlogboek te bekijken. Zijn ze ongewoon groot? Neem contact op met Technische ondersteuning als u een van deze berichten ziet.
