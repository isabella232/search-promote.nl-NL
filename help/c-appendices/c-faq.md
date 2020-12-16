---
description: 'null'
seo-description: 'null'
seo-title: Veelgestelde vragen
solution: Target
title: Veelgestelde vragen
topic: Appendices,Site search and merchandising
uuid: 4ce454a4-e770-4587-91a0-a25491818ac6
translation-type: tm+mt
source-git-commit: 4270ea66ba645ad0f71c9c8b5c2a1fcc6eb02ad2
workflow-type: tm+mt
source-wordcount: '8639'
ht-degree: 0%

---


# Veelgestelde vragen{#frequently-asked-questions}

## Adobe Flash {#reference_4A25BBDE32214AF5A1A454F38FD51243}

Een pagina met veelgestelde vragen waarin de ondersteuning van het indexeren en zoeken van SWF-bestanden op een website wordt besproken.

Hier volgt een overzicht van veelvoorkomende vragen met betrekking tot SWF-bestanden:

* [Wanneer wordt een SWF-bestand gekropen en geïndexeerd?](#section_01BB5259140D4D5FB04CCB7A1A63DE99)
* [Wat moet ik doen om een SWF-bestand te indexeren?..](#section_0A6A52CC70D4495BBE14D91906318F95)
* [Hoe worden SWF-bestanden herkend?](#section_B36C0536AB544F509601DC6A11A8E656)
* [Hoe worden SWF-bestanden geïndexeerd?](#section_36856058A4B54FA5ABF921344F50410C)
* [Telt een SWF-bestand als een pagina?](#section_0158D6DE70BC40D78E2374787B9F58AB)
* [Hoe voorkom ik dat afzonderlijke SWF-bestanden worden geïndexeerd...](#section_E38AD37989EF410B97AF5125057BFD22)
* [Hoe voorkom ik dat SWF-bestanden worden geïndexeerd...](#section_DF2606A50E9A44859CFA0D44D7C5F2E4)
* [Hoe komt het dat ik de Chinese, Japanse of Koreaanse SWF-bestanden niet kan doorzoeken op mijn website?](#section_EE1A3A705AE74148BD195A0CE513A5C4)

## Wanneer wordt een SWF-bestand gekropen en geïndexeerd? {#section_01BB5259140D4D5FB04CCB7A1A63DE99}

Een SWF-bestand wordt gekropen en geïndexeerd als het zich in een insluiting- of objecttag op een HTML-pagina bevindt, zoals in het volgende voorbeeld:

```
<embed src="Flash-file-URL">  
 
<object>  
<param name=movie value="Flash-file-URL">  
</object> 
```

Een SWF-bestand wordt ook herkend als u de URL van het bestand als ingangspunt opgeeft.

Zie [Meerdere URL-ingangspunten toevoegen die u wilt indexeren](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45).

## Wat moet ik doen om een SWF-bestand te indexeren? {#section_0A6A52CC70D4495BBE14D91906318F95}

Als u SWF-bestanden wilt verslepen en indexeren, selecteert u het inhoudstype **[!UICONTROL Adobe Flash Movies]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**).

Zolang er vanuit een `<embed>`-tag of een `<object>`-tag in een HTML-document naar het Flash-bestand wordt verwezen, wordt de tekst geïndexeerd en wordt naar alle URL&#39;s in het bestand gesprongen.

Als er niet naar uw bestand wordt verwezen vanuit een `<embed>`-tag of een `<object>`-tag, kunt u het SWF-bestand in een `<a href=...>`-tag opnemen in een HTML-document of als een URL-ingangspunt.

Zie [Meerdere URL-ingangspunten toevoegen die u wilt indexeren](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45).

## Hoe worden SWF-bestanden herkend? {#section_B36C0536AB544F509601DC6A11A8E656}

SWF-bestanden worden aangeduid met het volgende MIME-type:

`application/x-shockwave-flash`

SWF-bestanden worden ook herkend met de MIME-typen `application/octet-stream` of `text/plain`, op voorwaarde dat de bestandsextensie .swf is.

Een onjuist geconfigureerde server kan een ander MIME-type gebruiken voor SWF-bestanden. Controleer de serverconfiguratie als u problemen ondervindt met het horizontaal schuiven en indexeren van SWF-bestanden.

## Hoe worden SWF-bestanden geïndexeerd? {#section_36856058A4B54FA5ABF921344F50410C}

Tekst in een SWF-bestand wordt geïndexeerd alsof het `<body>`-tekst in de insluitende HTML-pagina betreft. Als een zoekresultaat tekst vindt die in een ingesloten SWF-bestand staat, wordt het resultaat gekoppeld aan de insluitende HTML-pagina en niet aan het SWF-bestand. Op deze manier wordt het SWF-bestand in de juiste context weergegeven.

Als een SWF-bestand een URL bevat als een handeling &#39;Film laden&#39;, wordt de tekst in het SWF-bestand waarnaar wordt verwezen, geïndexeerd als onderdeel van de insluitende HTML-pagina.

Als een SWF-bestand een URL bevat als een actie &#39;URL ophalen&#39;, wordt de URL later gekropen en geïndexeerd, net zoals een HTML `<a href=...>`-verwijzing later wordt gekropen en geïndexeerd.

Wanneer een SWF-bestand wordt weergegeven als een URL-invoerpunt, wordt de tekst van het SWF-bestand geïndexeerd als één pagina. Een zoekresultaat dat tekst zoekt vanuit een invoerpunt-SWF-koppelingen rechtstreeks naar de film, niet naar een ingesloten HTML-pagina.

Zie [Meerdere URL-ingangspunten toevoegen die u wilt indexeren](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45).

## Telt een SWF-bestand als een pagina? {#section_0158D6DE70BC40D78E2374787B9F58AB}

Nee. Een SWF-bestand wordt beschouwd als onderdeel van de bijbehorende HTML-pagina. Alle URL&#39;s van het type Film laden die zich in SWF-bestanden bevinden, worden ook beschouwd als onderdeel van de insluitende HTML-pagina. SWF-bestanden waarnaar wordt verwezen vanuit een HTML-pagina, tellen daarom niet als een &quot;pagina&quot; voor het totale aantal pagina&#39;s van de account.

Als een SWF-bestand wordt vermeld als een URL-ingangspunt, worden dat SWF-bestand en alle URL&#39;s voor Film laden die in dat SWF-bestand worden vermeld, geteld als één &quot;pagina&quot; voor het totale aantal pagina&#39;s van de account.

## Hoe voorkom ik dat afzonderlijke SWF-bestanden worden geïndexeerd? {#section_E38AD37989EF410B97AF5125057BFD22}

Als u wilt voorkomen dat een SWF-bestand wordt geïndexeerd, kunt u een metatag voor robots ( `<meta name="ROBOTS" content="NOINDEX">`) of een tag `<noindex>` toevoegen aan het insluitende HTML-document. Dit is het document dat de tag `<embed>` of `<object>` bevat.

U kunt ook de meta-tag robots ( `<meta name="ROBOTS" content="NOFOLLOW">`) gebruiken om volgende URL&#39;s in het SWF-bestand te voorkomen. Als het insluitende HTML-document is uitgeschakeld, worden de URL&#39;s die in het SWF-bestand worden vermeld als &#39;URL ophalen&#39;, niet gevolgd.

## Hoe voorkom ik dat SWF-bestanden op mijn website worden geïndexeerd? {#section_DF2606A50E9A44859CFA0D44D7C5F2E4}

Als u SWF-indexering wilt uitschakelen, deselecteert u het inhoudstype **[!UICONTROL Adobe Flash Movies]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**).

U kunt er ook voor kiezen [!DNL URL Masks] te gebruiken om de indexering van SWF-bestanden uit te schakelen.

Zie [URL-maskers toevoegen om delen van te indexeren of niet te indexeren..](../c-about-settings-menu/c-about-crawling-menu.md#task_E1AFC17C746048B8843013D979E082C1).

Voer een van de volgende URL-maskers in om SWF-indexering uit te schakelen:

* `exclude *.swf` (als u geen reguliere expressies gebruikt)
* `exclude regexp ^.*\.swf$` (als u reguliere expressies gebruikt)

Zie [Gewone uitdrukkingen](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

## Hoe komt het dat ik de Chinese, Japanse of Koreaanse SWF-bestanden niet kan doorzoeken op mijn website? {#section_EE1A3A705AE74148BD195A0CE513A5C4}

Bij zoeken/verhandelen van sites wordt UTF-8 verkregen van SWF-bestanden die zijn gemaakt met Adobe Flash. De UTF-8 bevat geen taalaanduiding. Als u het inhoudstype **[!UICONTROL Adobe Flash Movies]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**) selecteerde, moet u meta-gegevensinjecties gebruiken om de taal te specificeren die door het Swf- dossier wordt gebruikt.

Zie [Veldinjectiedefinities toevoegen](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE).

Oudere SWF-bestanden geven ook geen tekenset op. Als u het SWF-inhoudstype **[!UICONTROL Adobe Flash Movies]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**) hebt geselecteerd, moet u metagegevensinjecties gebruiken om de tekenset op te geven die in het SWF-bestand wordt gebruikt.

## Algemene zoekopdracht {#reference_E2C675162789452A9B99C6633B12CBEF}

Een pagina met veelgestelde vragen waarin wordt besproken hoe klanten die uw website bezoeken, met zoeken en verhandelen naar websites kunnen zoeken.

Hier volgt een aantal algemene vragen over algemene zoekopdrachten:

* [Moet ik software installeren om de site te kunnen gebruiken...](#section_02AB2AFF71984F9DAA3AF2B7C0847A22)
* [Wat gebeurt er als mijn site de paginalimiet overschrijdt?](#section_ECA5FA01032D4322BABA4E2C7FE498C1)
* [Hoe wijzig ik het e-mailadres waar de week...](#section_AE27F63DD13F425B940C8E7D9ED5C614)
* [Hoe veilig is mijn klanteninformatie op plaatsonderzoek/handel?](#section_5484CB954167412BB7F0480CB0C504B8)
* [Hoe zit het met de privacy van mijn klantgegevens?](#section_8FB493F15E51454BA92A0C83E14C0CC7)
* [Kan ik mijn eigen banneradvertenties laten zien op de zoekactie...](#section_611EB8B32C16418386CB7DC7FB6954B8)

Hier volgen enkele veelgestelde vragen over zoekfuncties:

* [Kan ik de zoekresultaten voor mijn site aanpassen?](#section_A64B3A621B794DF78D35ED06D9C43D0B)
* [Kan ik zien waarnaar klanten op mijn zoeken...](#section_73709E1B0E82478DA7B4D15B6C845F33)
* [Hoe kan ik bepalen welke inhoudstypen (PDF, tekst, Flash, MP3 en Microsoft Office) worden geïndexeerd en doorzocht?](#section_0AB8CB4B6BFA4286AA082055FEBFBE1C)
* [Worden dynamisch gegenereerde webpagina&#39;s door middel van ASP-, JSP-, PHP-, CFM- of Perl-gebaseerde inhoud ondersteund?](#section_E279F004F1C542A2B9773B832E7B013F)
* [Hoe kan ik synoniemen gebruiken om de zoekresultaten te verbeteren...](#section_E6E36E12514F4D7BAB01F8D1AB61D57B)
* [Heb ik controle over de volgorde van zoekresultaten...](#section_C6361048502745779D9749A842C4C370)
* [Kan ik de taal van de pagina met zoekresultaten wijzigen...](#section_6EE41DA8241247D48BBEB061A50599C5)
* [Mag ik meer dan één plaats op mijn Adobe hebben...](#section_AFA8825182094660A71EEC84B8329D6D)
* [Kan ik meer dan één domein zoeken?](#section_BFBB0E9861D942F095B56CF0A8F16596)
* [Kan ik mijn site onderverdelen in afzonderlijke secties zodat...](#section_52153A9DE9F9493B967A70583848B2A4)
* [Hoe kan ik delen van mijn website uitsluiten van...](#section_D452EDE153654EF398F4A87780C6D43B)
* [Welke tekensets worden ondersteund?](#section_A62A6F8F15804F968C77F2DEBDE8F8FD)
* [Wat gebeurt er als ik mijn website verander of bijwerk?](#section_489050E0EBC14D0594DBBAA0CCF4F6BA)
* [Kan mijn site automatisch worden geïndexeerd?](#section_9C7D41636238488691ECDFEE4D4E5103)
* [Ik gebruik wachtwoorden op mijn website. Kan ik nog steeds zoeken/verkopen op de site gebruiken?](#section_4618EB5B66704640B5502D1B5CB4B32E)
* [Steunt u het kruipen en het indexeren van https of...](#section_D5BB8B8FBEA4405583E86B4AEC37151B)
* [Wordt bij het zoeken/verhandelen van sites het bestand robots.txt op mijn website gerespecteerd?](#section_73BBF6FE93C64C109F45CBC2FA394DB2)
* [Bepaalde delen van mijn website moeten regelmatig worden bijgewerkt...](#section_6D2FB1DE1B8A49729F9CCAE2A2770AB3)
* [Kan ik scripts of programma&#39;s gebruiken om incrementele stappen te starten...](#section_0B6BB039557A42AA876D35D748E17DD0)

## Moet ik om het even welke software installeren om plaats te gebruiken onderzoek/koopwaar? {#section_02AB2AFF71984F9DAA3AF2B7C0847A22}

Nee. Dit is het belangrijkste voordeel van het zoeken/verhandelen van sites. De engine is een professionele toepassing die volledig op onze krachtige servers wordt gehost en onderhouden. Hierdoor is de software gebruiksvriendelijker dan andere zoekoplossingen. U hoeft alleen maar een kleine hoeveelheid HTML-code aan uw pagina&#39;s toe te voegen, zodat klanten van uw website zoekopdrachten kunnen invoeren. Bij het zoeken en verhandelen van sites wordt voor alle andere zaken gezorgd.

## Wat gebeurt er als mijn site de paginalimiet overschrijdt? {#section_ECA5FA01032D4322BABA4E2C7FE498C1}

We blijven uw zoekopdrachten uitvoeren, zodat uw bezoekers uw website zonder onderbreking kunnen doorzoeken. Als u wilt controleren of uw website de paginalimiet overschrijdt, controleert u de status Volledige index of Live log.

Zie [Volledige index](../c-about-index-menu/c-about-full-index.md#concept_C69BD21863FD4856B49326F35DB570D3).

Zie [Het volledige indexlogboek van een live of gefaseerd weergeven...](../c-about-index-menu/c-about-full-index.md#task_02E5E944C56B4EB19CC1FF321F3221B8).

## Hoe wijzig ik het e-mailadres waar de wekelijkse rapporten worden verzonden? {#section_AE27F63DD13F425B940C8E7D9ED5C614}

Wekelijkse rapporten worden naar de eigenaar van elke actieve account verzonden. U kunt het e-mailadres wijzigen door op **[!UICONTROL Settings]** > **[!UICONTROL My Profile]** > **[!UICONTROL Personal Information]** te klikken. Als u meer dan één actief onderzoeksrekening hebt, dan worden alle nieuwsbrieven verzonden naar het nieuwe adres.

Zie [Uw persoonlijke gebruikersinformatie configureren](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6).

## Hoe veilig is mijn klanteninformatie op plaatsonderzoek/handel? {#section_5484CB954167412BB7F0480CB0C504B8}

Zoeken/verhandelen van sites is veilig, snel, stabiel en gebruiksvriendelijk. U wordt niet gedwongen om cookies te gebruiken (hoewel u wilt) om onze producten te gebruiken, en gevoelige informatie, zoals wachtwoorden, wordt nooit geplaatst op enige verbinding URL die later van uw browser kan worden teruggewonnen.

## Hoe zit het met de privacy van mijn klantgegevens? {#section_8FB493F15E51454BA92A0C83E14C0CC7}

Adobe zet zich in voor het respecteren van de privacy van hun klanten en bezoekers. Zie de Adobe [Privacy Center](https://www.adobe.com/privacy.html).

## Kan ik mijn eigen banneradvertenties tonen op de pagina&#39;s met zoekresultaten? {#section_611EB8B32C16418386CB7DC7FB6954B8}

Ja. U bepaalt de vormgeving en de inhoud van de zoekresultaten. Binnen het malplaatje van onderzoeksresultaten voor uw website, kunt u verbindingen aan uw eigen banneruitwisselingsnetwerk zoals LinkExchange of SmartClicks tot stand brengen. Alle treffers die door uw bezoekers worden gemaakt, worden correct gecrediteerd op uw banneruitwisselingsaccount.

## Kan ik de zoekresultaten voor mijn site aanpassen? {#section_A64B3A621B794DF78D35ED06D9C43D0B}

Ja. Dit is een exclusieve functie voor zoeken/verhandelen van sites. Met onze geavanceerde sjabloontechnologie en een beetje kennis van HTML, kunt u precies bepalen hoe de zoekresultaten worden weergegeven.

Zie [Sjabloontags zoeken](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4).

De overgang tussen uw eigen servers en zoek-/verkoopservers van de site is volledig naadloos en onzichtbaar voor uw klanten. Als u geen HTML kent of u geen tijd hebt om een douanemalplaatje tot stand te brengen, kunt u van een assortiment aantrekkelijke, klaar-aan-gebruiksmalplaatjes kiezen die in huisteam van professionele Webontwikkelaars creëren.

## Kan ik zien naar welke klanten op mijn site zoeken? {#section_73709E1B0E82478DA7B4D15B6C845F33}

Ja. We houden zoekstatistieken bij voor zoekopdrachten die bezoekers de afgelopen twee maanden op uw website hebben uitgevoerd. U kunt deze statistieken op elk ogenblik onder Rapporten over het productmenu herzien. Met zoekrapporten krijgt u essentiële informatie over wat bezoekers precies zoeken op uw website. U kunt deze informatie gebruiken om het ontwerp te verbeteren of de zoekfunctie/merchandising-engine voor de site af te stemmen, zodat bezoekers er beter van kunnen profiteren.

## Hoe kan ik bepalen welke inhoudstypen (PDF, tekst, Flash, MP3 en Microsoft Office) worden geïndexeerd en doorzocht? {#section_0AB8CB4B6BFA4286AA082055FEBFBE1C}

U kunt accounts eenvoudig configureren om het indexeren en zoeken van tekst in PDF-documenten, documenten zonder tekst, Flash-films, MP3-bestanden of Microsoft Office-documenten in of uit te schakelen.

Deze instellingen worden beheerd op de pagina [!DNL Staged Content Types].

Zie [Informatie over inhoudssoorten](../c-about-settings-menu/c-about-crawling-menu.md#concept_6FEA1355C0374500B4C53090C34A8A07).

## Worden dynamisch gegenereerde webpagina&#39;s door middel van ASP-, JSP-, PHP-, CFM- of Perl-gebaseerde inhoud ondersteund? {#section_E279F004F1C542A2B9773B832E7B013F}

Statische of dynamisch gegenereerde HTML-webpagina&#39;s worden geïndexeerd, inclusief pagina&#39;s die zijn gemaakt op basis van databases of een ander back-end proces. Omdat de HTML-code die een browser ziet, geïndexeerd is, kunt u zoeken en verhandelen op websites gebruiken zolang deze back-end architecturen maar HTML-pagina&#39;s opleveren.

De zoekrobot crawt uw website door te beginnen met de eerste pagina op het websiteadres dat is opgegeven in [!DNL Account Settings] en koppelingen te volgen van pagina naar pagina.

Zie [Uw accountinstellingen configureren](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9).

Wanneer de zoekrobot naar alle pagina&#39;s van uw website knippert en deze indexeert, kunt u met de zoekfunctie naar uw site zoeken. Met andere woorden, als dynamisch gegenereerde documenten naar uw website worden geweven met koppelingen van andere pagina&#39;s, kan de zoekrobot nog steeds doorkruisen en de dynamische inhoud indexeren.

Nadat de inhoud van uw website is gekropen en geïndexeerd, kunnen klanten naar uw website zoeken naar informatie binnen de geïndexeerde inhoud.

## Hoe kan ik synoniemen gebruiken om de zoekresultaten voor mijn site te verbeteren? {#section_E6E36E12514F4D7BAB01F8D1AB61D57B}

U kunt synoniemen gebruiken wanneer u bezoekers pagina&#39;s wilt zoeken die verwant zijn aan hun zoekopdracht.

Stel dat u een pagina hebt met een prijslijst van producten die op uw site te koop zijn. Maar na het bekijken van de zoekrapporten die worden geleverd door het zoeken naar en verkopen van sites, zien klanten in hun zoekopdrachten naar het woord &#39;kosten&#39;, &#39;kosten&#39;, &#39;kosten&#39; of &#39;kosten&#39;. Met deze woorden wordt de pagina met de prijslijst niet weergegeven in de zoekresultaten. Met de functie [!DNL Add Synonyms] in [!DNL Dictionaries] kunt u opgeven dat deze woorden synoniemen zijn en dat uw klant uw prijslijst kan vinden, ongeacht welke zoekterm zij gebruiken.

Zie [Informatie over woordenboeken](../c-about-linguistics-menu/c-about-dictionaries.md#concept_B8028B71EC8144669614C64578EDB034).

## Heb ik controle over de volgorde van zoekresultaten? {#section_C6361048502745779D9749A842C4C370}

Ja. Gebruikend de geavanceerde relevantieinterface, kunt u controleren welke pagina&#39;s voor een specifieke onderzoeksvraag zijn teruggekeerd. Deze functie is handig als u er zeker van wilt zijn dat klanten een specifieke pagina zien wanneer ze vragen naar bepaalde woorden.

Zie [Een nieuw metatag toevoegen gebied](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).

## Kan ik de taal van de pagina met zoekresultaten wijzigen? {#section_6EE41DA8241247D48BBEB061A50599C5}

Ja. De sjabloon voor zoeken/verhandelen van sites is flexibel wanneer u een resultatenpagina wilt samenstellen die de taal van uw keuze gebruikt en overeenkomt met de weergave van uw website.

De sjabloon bestaat uit een combinatie van tekst, standaard HTML-tags en speciale tags die zijn gedefinieerd om de zoekresultaten weer te geven. Wanneer een klant een zoekopdracht uitvoert, leest de zoekrobot de sjabloon, wordt de tekst uitgevoerd met standaard-HTML-tags en worden de resultatenkoppelingen ingevoegd op basis van de speciale sjabloontags.

Zie [Sjabloontags zoeken](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4).

Als u de resultatentaal wilt wijzigen, kunt u de Engelse tekst bewerken die in de sjabloon wordt weergegeven.

Zie [Een presentatie of een transportsjabloon bewerken](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3).

## Kan ik meer dan één plaats op mijn Adobe Klantenlogin hebben? {#section_AFA8825182094660A71EEC84B8329D6D}

Ja. Met één Adobe-aanmelding voor klanten kunt u een andere zoekfunctie voor vele verschillende websites beheren. Selecteer en beheer accounts onder Accounts.

Zie [Een andere account selecteren om te gebruiken](../c-about-accounts-menu.md#task_03C0FE918E2D44529CDC3B8DB75D1B26).

## Kan ik meer dan één domein zoeken? {#section_BFBB0E9861D942F095B56CF0A8F16596}

Ja. U kunt toegang tot meer dan één domein vormen door [!DNL URL Entrypoints] te gebruiken. Geef URL-invoerpunten op voor andere domeinen die u bezit. Onthoud dat u toestemming moet hebben om domeinen te indexeren die u niet hebt.

Zie [Informatie over URL-invoerpunten](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573).

## Kan ik mijn site onderverdelen in afzonderlijke secties zodat klanten elk van deze gebieden afzonderlijk of op de hele site kunnen doorzoeken? {#section_52153A9DE9F9493B967A70583848B2A4}

Ja. Er is een functie &quot;Verzamelingen&quot; opgenomen waarmee klanten specifieke gebieden van uw website kunnen doorzoeken en snel kunnen terugvinden naar wat ze zoeken.

Zie [Informatie over verzamelingen](../c-about-settings-menu/c-about-searching-menu.md#concept_62E42ACE53D54EEE9273433B86259127).

Klanten kunnen bijvoorbeeld een verzameling URL&#39;s doorzoeken die betrekking hebben op productverkoopinformatie of een verzameling URL&#39;s die betrekking hebben op ondersteuningsservices. U kunt inzamelingen plaatsen zodat uw klanten een drop-down lijst van inzamelingen of een groep controledozen zien.

## Hoe kan ik voorkomen dat delen van mijn website worden doorzocht? {#section_D452EDE153654EF398F4A87780C6D43B}

Ja. Geef URL-maskers op om te bepalen welke websitepagina&#39;s u wilt opnemen in indexering of wilt uitsluiten. URL-maskers bepalen of websitepagina&#39;s in uw zoekresultaten worden weergegeven.

Zie [Informatie over URL-maskers](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164).

Zie [Informatie over script voor URL-maskers](../c-about-settings-menu/c-about-filtering-menu.md#concept_384F32EA18F84853A7BA99A04009330B).

Als u wilt voorkomen dat delen van afzonderlijke webpagina&#39;s worden doorzocht, kunt u delen van een pagina uitsluiten van indexering. Omring de tekst met `<noindex>`- en `</noindex>`-tags. Deze methode is handig als u navigatietekst wilt uitsluiten van zoekopdrachten.

## Welke tekensets worden ondersteund? {#section_A62A6F8F15804F968C77F2DEBDE8F8FD}

Webpagina&#39;s geven doorgaans de tekenset aan met een metatag die lijkt op het volgende:

`<META HTTP-EQUIV="Content-Type" CONTENT="text/html; charset=iso-8859-1">`

Met de functie voor zoeken en verhandelen van sites worden webpagina&#39;s op de juiste wijze geïndexeerd met alle gangbare tekensets die momenteel op internet worden gebruikt. Enkele ondersteunde tekensets zijn onder andere:

<table> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Arabisch (ISO-8859-6) </p> </td> 
   <td colname="col2"> <p>Chinees (traditioneel); Big5) </p> </td> 
   <td colname="col3"> <p>Japans (Shift_JIS) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Arabisch (Windows-1256) </p> </td> 
   <td colname="col2"> <p>Chinees (traditioneel); EUC-TW) </p> </td> 
   <td colname="col3"> <p>Russisch (KOI8-R) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Baltisch (ISO-8859-4) </p> </td> 
   <td colname="col2"> <p>Cyrillisch (ISO-8859-5) </p> </td> 
   <td colname="col3"> <p>Zuid-Europees (ISO-8859-3) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Baltisch (Windows-1257) </p> </td> 
   <td colname="col2"> <p>Cyrillisch (Windows-1251) </p> </td> 
   <td colname="col3"> <p>Turks (ISO-8859-9) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Midden-Europees (ISO-8859-2) </p> </td> 
   <td colname="col2"> <p>Grieks (ISO-8859-7) </p> </td> 
   <td colname="col3"> <p>Turks (Windows-1254) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Midden-Europees (Windows-1250) </p> </td> 
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
   <td colname="col3"> <p>West-Europees (ISO-8859-1) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chinees (vereenvoudigd); EUC-CN) </p> </td> 
   <td colname="col2"> <p>Japans (EUC-JP) </p> </td> 
   <td colname="col3"> <p>West-Europees (ISO-8859-15) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chinees (vereenvoudigd); (GB2312) </p> </td> 
   <td colname="col2"> <p>Japans (ISO-2022-JP) </p> </td> 
   <td colname="col3"> <p>West-Europees (Windows-1252) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chinees (vereenvoudigd); GBK) </p> </td> 
   <td colname="col2"> <p>Japans (ISO-2022-JP-1) </p> </td> 
   <td colname="col3"> <p>West-Europees (x-mac-roman) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chinees (vereenvoudigd); HZ-GB-2312) </p> </td> 
   <td colname="col2"> <p>Japans (ISO-2022-JP-2) </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

Neem contact op met Technische ondersteuning voor informatie over tekensets die hierboven niet worden vermeld.

## Wat gebeurt er als ik mijn website verander of bijwerk? {#section_489050E0EBC14D0594DBBAA0CCF4F6BA}

Nadat u de inhoud van uw website hebt gewijzigd, kunt u een volledige index of een incrementele index uitvoeren. Bij zoeken/verhandelen van sites worden alle gewijzigde website-inhoud gedownload en geïndexeerd. Nadat de indexering is voltooid, kunnen uw klanten de nieuwe inhoud zoeken. U kunt ook een automatische indexering van uw site op een bepaald tijdstip en op een bepaalde dag plannen.

Zie [Een volledige index van een actieve of gefaseerde website uitvoeren...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

Zie [Een incrementele index van een actieve of gefaseerde website uitvoeren...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

Zie [Het volledige indexschema instellen voor een live website](../c-about-index-menu/c-about-full-index.md#task_6760F3256D004A228B38968DF15421F0).

Zie [Het incrementele indexschema instellen voor een live website](../c-about-index-menu/c-about-incremental-index.md#task_2A46BA189ECC4317A9D5C6E99A336F33).

## Kan mijn site automatisch worden geïndexeerd? {#section_9C7D41636238488691ECDFEE4D4E5103}

Ja. U kunt elke dag een automatische index van uw site plannen.

Naast het dagelijks automatisch indexeren kunt u ervoor kiezen om delen van de site regelmatig incrementeel te wijzigen. Op dagen dat u een automatische index hebt gepland, kunt u de tijd van dag controleren de index plaatsvindt. U kunt ook altijd handmatig een site-index starten wanneer u dat wilt.

Zie [Het volledige indexschema instellen voor een live website](../c-about-index-menu/c-about-full-index.md#task_6760F3256D004A228B38968DF15421F0).

Zie [Het incrementele indexschema instellen voor een live website](../c-about-index-menu/c-about-incremental-index.md#task_2A46BA189ECC4317A9D5C6E99A336F33).

## Ik gebruik wachtwoorden op mijn website. Kan ik nog steeds zoeken/verkopen op de site gebruiken? {#section_4618EB5B66704640B5502D1B5CB4B32E}

Als u HTTP Basic-verificatie gebruikt om bepaalde delen van uw website met een wachtwoord te beveiligen, kunt u voorwaarden en wachtwoorden opgeven die met zoeken en verkopen van sites kunnen worden gebruikt om uw site te indexeren.

Zie [Wachtwoorden toevoegen voor toegang tot gebieden van uw website die...](../c-about-settings-menu/c-about-crawling-menu.md#task_DED19D476FF04B48BB6456D5ECB8628A).

## Steunt u het kruipen en het indexeren van https of veilige serverinhoud? {#section_D5BB8B8FBEA4405583E86B4AEC37151B}

Ja. U kunt de inhoud op beveiligde servers (https) horizontaal schuiven en indexeren.

## Wordt bij het zoeken/verhandelen van sites het bestand robots.txt op mijn website gerespecteerd? {#section_73BBF6FE93C64C109F45CBC2FA394DB2}

Ja. Het Protocol van de Uitsluiting van Robots is volgzaam. De zoekrobot controleert het bestand robots.txt als dit bestand aanwezig is op uw website. Als het bestand robots.txt alle robots van uw site uitsluit, wordt de robot voor het zoeken en verhandelen van sites ook uitgesloten. Als u wilt dat alleen de robot voor het zoeken/verhandelen van sites door uw site kan kruipen, stelt u de inhoud van het bestand robots.txt als volgt in:

```
User-agent: Atomz/1.0 
Disallow:
```

```
User-agent: * 
Disallow: /
```

U kunt meer over Web robots en het Protocol van de Uitsluiting Robots bij het volgende leren:

[https://www.robotstxt.org/orig.html](https://www.robotstxt.org/orig.html)

## Bepaalde delen van mijn website moeten regelmatig worden bijgewerkt, zodat mijn klanten de meest nauwkeurige zoekresultaten krijgen. Helpt incrementele indexering bij dit probleem? {#section_6D2FB1DE1B8A49729F9CCAE2A2770AB3}

Ja. Dit scenario is wat de stijgende indexerende eigenschap werd gebouwd om plaatsonderzoek/handel te vergemakkelijken. Het primaire voordeel van incrementele indexering is dat bedrijven hiermee vaak dynamisch veranderende gedeelten van hun website kunnen indexeren. Deze functionaliteit zorgt ervoor dat u zoekresultaten weergeeft met &quot;tot de minuut&quot; nauwkeurigheid.

Zie [Een incrementele index van een actieve of gefaseerde website uitvoeren...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

Zie [Het incrementele indexschema instellen voor een live website](../c-about-index-menu/c-about-incremental-index.md#task_2A46BA189ECC4317A9D5C6E99A336F33).

## Worden dynamisch gegenereerde webpagina&#39;s ondersteund door een back-enddatabase, zoals productcatalogi of voorraadbeheersystemen? {#section_26896C556483457E879785E751583B16}

Statische of dynamisch gegenereerde HTML-webpagina&#39;s, inclusief pagina&#39;s die zijn gemaakt op basis van databases, of andere back-endprocessen, worden geïndexeerd. Omdat de HTML-code, die door een browser wordt weergegeven, is geïndexeerd, kunt u zoeken en verhandelen op websites gebruiken zolang de achterste databasegegevens HTML-pagina&#39;s opleveren.

De zoekrobot crawt uw website door te beginnen met de eerste pagina op het websiteadres dat is opgegeven in [!DNL Account Settings] en koppelingen te volgen van pagina naar pagina.

Zie [Uw accountinstellingen configureren](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9).

Wanneer de zoekrobot naar alle pagina&#39;s van uw website knippert en deze indexeert, kunt u met de zoekfunctie naar uw site zoeken. Met andere woorden, als dynamisch gegenereerde documenten naar uw website worden geweven met koppelingen van andere pagina&#39;s, kan de zoekrobot nog steeds doorlopen en de dynamische database-inhoud indexeren.

Nadat de inhoud van uw website is gekropen en geïndexeerd, kunnen klanten naar uw website zoeken naar informatie binnen de geïndexeerde inhoud.

U kunt het zoeken van volledige inhoud of een nauwer op onderwerp-gebaseerd onderzoek gemakkelijk toelaten beperkt tot informatie in de titel, of meta-beschrijving, of meta-sleutelwoorden documentmarkeringen, of alle drie. Met behulp van metagegevensdefinities kunt u ook aangepaste weergavevelden maken, zoals een productafbeelding, in de werkelijke zoekresultaten.

Zie [Een nieuw metatag toevoegen gebied](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).

## Kan ik scripts of programma&#39;s gebruiken om een incrementele index van mijn site te starten? {#section_0B6BB039557A42AA876D35D748E17DD0}

Ja. U kunt scripts of programma&#39;s gebruiken om een incrementele index van uw website te starten en de servers pingelen om de site te indexeren wanneer de inhoud wordt gewijzigd of bijgewerkt.

Zie [Informatie over index met scripts](../c-about-index-menu/c-about-scripted-index.md#concept_34F58D551BC04BFB8ADC294B9DA9199D).

## Implementatie van functies {#reference_2D0C4A80B8D64051BA9694D562DCE663}

Een pagina met vaak gestelde vragen waarin verschillende functies-implementaties in [!DNL Search&Promote] worden besproken.

Hieronder volgen algemene vragen over functies-implementaties in [!DNL Search&Promote] op een website:

* [Waarom lopen mijn bedrijfsregels niet?](#section_7FEB60383D8A4B11A60DFF9067274699)
* [Waarom heb ik problemen die indexeren plannen, fouten beginnen indexerend, en kwesties beginnen gefaseerd indexeren?](#section_E05758193DF5436784B0145839989F75)
* [Mijn maximale indexgrootte overschrijdt mijn toegestane grens. Waarom gebeurt dit en hoe los ik het op?](#section_12E7DA979C4C4B1D8A3A6415FC3DDA70)

## Waarom lopen mijn bedrijfsregels niet? {#section_7FEB60383D8A4B11A60DFF9067274699}

Vorm bedrijfsregels wanneer de banners verschijnen, of helpen beslissen welke resultaten verschijnen en in welke orde. U kunt de positie van een punt in uw facet ook vormen, en welke malplaatje voor een bepaalde onderzoek wordt gebruikt.
Herplaats bedrijfsregels om de orde te veranderen waarin zij op presentatiesjablonen lopen. De bedrijfsregels worden uitgevoerd in de volgorde waarin ze zijn gedefinieerd; namelijk hoger het de ordeaantal van een regel, later het in het proces in werking stelt, die vroegere regels trompelt. U wijzigt de volgorde van de regels door een nieuw nummer in te voeren in de kolom Volgorde van de tabel op de pagina Bedrijfsregels.

Zie [Informatie over bedrijfsregels](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

## Waarom heb ik problemen die indexeren plannen, fouten beginnen indexerend, en kwesties beginnen gefaseerd indexeren? {#section_E05758193DF5436784B0145839989F75}

Wanneer u een index produceert, of het volledig of stijgend is, kruipt de statusinformatie van de index in real time wordt getoond. U kunt bijvoorbeeld de begintijd, de verstreken tijd en eventuele fouten weergeven die tijdens het indexeringsproces zijn opgetreden. Er wordt ook informatie weergegeven over de status van de laatste index. Gebruik deze informatie om het even welke indexerende fouten problemen op te lossen u ontmoet.

Zie [Het volledige indexschema voor een live website instellen](../c-about-index-menu/c-about-full-index.md#task_6760F3256D004A228B38968DF15421F0) en [Het incrementele indexschema voor een live website instellen](../c-about-index-menu/c-about-incremental-index.md#task_2A46BA189ECC4317A9D5C6E99A336F33) voor het plannen van een index.

Zie [Een volledige index van een actieve of gefaseerde website uitvoeren voor het starten van een gefaseerde index..](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D) of [Een incrementele index van een actieve of gefaseerde website uitvoeren...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

## Mijn maximale indexgrootte overschrijdt mijn toegestane grens. Waarom gebeurt dit en hoe los ik het op? {#section_12E7DA979C4C4B1D8A3A6415FC3DDA70}

Een website kan over het algemeen groeien en in de loop der tijd &quot;ontdekt&quot;meer documenten en Web-pagina&#39;s die werden toegevoegd. Uiteindelijk kan uw account de limiet voor de indexgrootte overschrijden. In dergelijke gevallen kunt u overwegen **[!UICONTROL URL Mask]** te gebruiken. Met deze functie verbergt u documenten en webpagina&#39;s van indexcrawling die u niet wilt of niet nodig hebt om te indexeren, waardoor de indexgrootte afneemt. Een andere mogelijkheid is contact op te nemen met Technische ondersteuning om de limiet voor indexgrootte in uw account te verhogen.

Zie [Informatie over URL-maskers](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164).

Als u niet zeker weet wat u moet doen, neemt u contact op met Technische ondersteuning. Er kunnen vele andere variabelen zijn die uw indexgrootte beïnvloeden die, indien aangepast, ook de facturering van uw rekening kunnen beïnvloeden.

## Internationaal {#reference_F017C2968BFB446499EF1D3CE2CAC0FE}

Een pagina met veelgestelde vragen bevat ondersteuning voor het indexeren en zoeken van meer dan 19 talen, waaronder Aziatische multibyte-talen zoals Chinees (vereenvoudigd en traditioneel), Japans en Koreaans.

Hieronder volgen algemene vragen over talen en tekensets:

* [Wat controleert het karakter - vastgestelde codering van de onderzoeksvraag...](#section_DF2E8570AFC2480FA199FD26C941A22F)
* [Alleen doorzochte pagina&#39;s waarvan de codering overeenkomt met de codering van..](#section_9E544F3DB7DE41618DC1BC8224B32C5A)
* [Welke codering wordt gebruikt voor de pagina met zoekresultaten?](#section_DA68670F35D54EAABF7DBB010F4409BF)
* [Kan ik zoeken en verhandelen van sites gebruiken op Unicode-, UTF-8- en gecodeerde pagina&#39;s?](#section_130997CB08934A13A5261D85CF88040C)
* [Hoe komt het dat ik de Chinese, Japanse of Koreaanse PDF-bestanden niet kan doorzoeken op mijn website?](#section_539AFF482F814D28B5929F683D2F2175)
* [Hoe komt het dat ik de Chinese, Japanse of Koreaanse SWF-bestanden niet kan doorzoeken op mijn website?](#section_9C0849528AFF4C10AA97A2C912992638)
* [Hoe komt het dat ik de Chinese, Japanse of Koreaanse Microsoft Office-bestanden niet kan doorzoeken op mijn website?](#section_6764BA6863AF492EBA9BE5CCC12CDD1F)
* [Hoe komt het dat ik de Chinese, Japanse of Koreaanse MP3-bestanden niet kan doorzoeken op mijn website?](#section_DB6D60CF46F94125BF4E54AF3036DBFC)
* [Moet ik iets speciaals doen om de ...](#section_A8BA6DDD3A6048319D3530BCFD6DA1A5)
* [Hoe komen Chinese, Japanse of Koreaanse lettertypen voor in zoekresultaten onder Netscape 4.7 en eerder?](#section_DF42567063304F918D406AC76529DFB7)

## Wat controleert het karakter - vastgestelde codering van de onderzoeksvraag? {#section_DF2E8570AFC2480FA199FD26C941A22F}

Het gedeelte &#39;Webformulieren&#39; van uw zoekaccount bevat voorbeeldzoekformulieren waarmee u zoekfuncties aan uw website kunt toevoegen. Als u deze code voor zoekformulieren bekijkt, ziet u een regel die lijkt op het volgende:

`<input type=hidden name="sp_f" value="iso-8859-1">`

Deze coderegel vertelt het zoekprogramma dat de binnenkomende query is gecodeerd in iso-8859-1, een algemene codering voor West-Europese talen. U kunt deze instelling wijzigen door naar het productmenu te gaan en op **[!UICONTROL Settings]** > **[!UICONTROL My Profile]** > **[!UICONTROL Personal Information]** te klikken. Selecteer op de pagina [!DNL Personal Information] in de vervolgkeuzelijst **[!UICONTROL Character Encoding]** een nieuwe codering.

Zie [Uw persoonlijke gebruikersinformatie configureren](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6).

U kunt de coderingswaarde op uw webpagina&#39;s ook handmatig wijzigen door de regel `sp_f` van het zoekformulier te bewerken. De waarde `sp_f` van het zoekformulier moet overeenkomen met de codering van de tekenset van de pagina waarin het formulier wordt weergegeven.

## Worden alleen pagina&#39;s doorzocht waarvan de codering overeenkomt met de codering van de zoekopdracht? {#section_9E544F3DB7DE41618DC1BC8224B32C5A}

Standaard, nee. Zolang de codering van de tekenset op de websitepagina&#39;s juist wordt aangegeven, worden de vereiste conversies uitgevoerd tussen de codering van de zoekquery en die van de pagina&#39;s, zelfs wanneer pagina&#39;s meerdere coderingen gebruiken.

## Welke codering wordt gebruikt voor de pagina met zoekresultaten? {#section_DA68670F35D54EAABF7DBB010F4409BF}

De tekensetcodering van uw account bepaalt de standaardcodering voor uw resultatensjabloon.

Zie [Uw persoonlijke gebruikersinformatie configureren](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6).

Meer informatie over het opgeven van een tekenset in een HTML-sjabloon.

Zie [Sjabloontags zoeken](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4).

## Kan ik zoeken en verhandelen van sites gebruiken op Unicode-, UTF-8- en gecodeerde pagina&#39;s? {#section_130997CB08934A13A5261D85CF88040C}

Ja. Unicode-tekensets, zoals UTF-8, bieden echter onvoldoende informatie om de taal te bepalen waarin de pagina&#39;s worden geschreven. Om deze pagina&#39;s correct te zoeken, is het noodzakelijk om de taal te specificeren. Om de documenttaal te bepalen, wordt de informatie verwerkt in de volgende orde:

* HTTP-header van de taal die door de server voor het document wordt geleverd.
* META-elementen (bijvoorbeeld `META HTTP-EQUIV="Content-Language" Content="ja_JP"`) in de sectie `<HEAD>` van het document.

* LANG-kenmerk van de tag `<HTML>` (bijvoorbeeld `<HTML LANG="ja_JP">`).

Als uw server niet wordt gevormd om de inhoud-Taal HTTP- kopbal te leveren, en uw documenten noch het taalelement META, noch de taalattributen voor de `<HTML>` markering bevatten, kunt u meta-gegevensinjecties gebruiken om de aangewezen taal te specificeren.

Zie [Veldinjectiedefinities toevoegen](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE).

## Hoe komt het dat ik de Chinese, Japanse of Koreaanse PDF-bestanden niet kan doorzoeken op mijn website? {#section_539AFF482F814D28B5929F683D2F2175}

Bij zoeken/verhandelen van sites wordt UTF-8 uit Adobe PDF-bestanden opgehaald, zonder taalaanduiding. Als u **[!UICONTROL PDF Documents]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**) hebt geselecteerd, moet u meta-gegevensinjecties gebruiken om de taal te specificeren die in het Pdf- dossier wordt gebruikt.

Zie [Veldinjectiedefinities toevoegen](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE).

## Hoe komt het dat ik de Chinese, Japanse of Koreaanse SWF-bestanden niet kan doorzoeken op mijn website? {#section_9C0849528AFF4C10AA97A2C912992638}

Bij het zoeken/verhandelen van sites wordt UTF-8 verkregen uit Adobe Flash-filmbestanden die zijn gemaakt met Adobe Flash zonder taalaanduiding. Als u het inhoudstype **[!UICONTROL Adobe Flash Movies]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**) selecteerde, moet u meta-gegevensinjecties gebruiken om de taal te specificeren die in het Swf- dossier wordt gebruikt.

Voor Flash versie 4 of oudere versies van SWF-bestanden wordt de tekenset van de tekens in het bestand niet opgegeven. Als u het inhoudstype **[!UICONTROL Adobe Flash Movies]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**) selecteerde, moet u meta-gegevensinjecties gebruiken om de karakterreeks te specificeren die in het Swf- dossier wordt gebruikt.

Zie [Veldinjectiedefinities toevoegen](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE).

## Hoe komt het dat ik de Chinese, Japanse of Koreaanse Microsoft Office-bestanden niet kan doorzoeken op mijn website? {#section_6764BA6863AF492EBA9BE5CCC12CDD1F}

Bij het zoeken/verhandelen van sites wordt UTF-8 uit Microsoft Office-bestanden (Microsoft Word, Microsoft Excel en Microsoft PowerPoint) opgehaald zonder dat er een taal wordt aangeduid. Als u het inhoudstype **[!UICONTROL Microsoft Office Files]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**) selecteerde, moet u meta-gegevensinjecties gebruiken om de taal te specificeren die in de dossiers van Microsoft Office wordt gebruikt.

Zie [Veldinjectiedefinities toevoegen](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE).

## Hoe komt het dat ik de Chinese, Japanse of Koreaanse MP3-bestanden niet kan doorzoeken op mijn website? {#section_DB6D60CF46F94125BF4E54AF3036DBFC}

Als u het inhoudstype **[!UICONTROL Text in MP3 Music Files]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**) selecteert, moet u meta-gegevensinjecties gebruiken om de karakterreeks te specificeren die wordt gebruikt om de MP3 dossiers te coderen.

Zie [Veldinjectiedefinities toevoegen](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE).

## Moet ik iets speciaals doen om de .txt dossiers op mijn website te krijgen om correct te indexeren? {#section_A8BA6DDD3A6048319D3530BCFD6DA1A5}

Als u het inhoudstype **[!UICONTROL Text Documents]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**) selecteerde, moet u meta-gegevensinjecties gebruiken om de karakterreeks te specificeren die wordt gebruikt om de .txt dossiers te coderen.

Zie [Veldinjectiedefinities toevoegen](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE).

## Hoe komen Chinese, Japanse of Koreaanse lettertypen voor in zoekresultaten onder Netscape 4.7 en eerder? {#section_DF42567063304F918D406AC76529DFB7}

Als in uw account de standaardsjabloon, een van de gebruiksklare sjablonen of een sjabloon op basis van een van deze sjablonen wordt gebruikt, kan het lettertypetags bevatten die Arial of Helvetica als lettertypevlakken opgeven. Bijvoorbeeld, `<font face="arial, helvetica" size="+1">`. In Netscape 4.7 en lager worden geen Chinese, Japanse of Koreaanse tekens weergegeven wanneer het lettertype Arial of Helvetica wordt gebruikt. Verwijder het `face`-kenmerk of vervang het lettertype door een lettertype dat geschikter is voor Chinees, Japans of Koreaans.

## Lage aantal pagina&#39;s {#reference_4344E3E3CB2948939860F8C078BD7773}

Een pagina met veelgestelde vragen waarin algemene problemen worden besproken die te maken hebben met een laag aantal indexpagina&#39;s.

Hier volgen veel vragen over het lage aantal indexpagina&#39;s:

* [Hebt u uw indexlogboek onderzocht?](#section_D6626536DC3D40DDA4A1224F1CB276BF)
* [Hebt u typfouten in uw URL?](#section_BD2CEABC5D0F4A0DA38F3AD72ABBA676)
* [Heeft de entrypunt-webpagina koppelingen naar andere pagina&#39;s...](#section_1C2D6ED54E7249268B555D9DC33352B3)
* [Zijn koppelingen naar andere pagina&#39;s op uw website ingesloten in...](#section_EE34A67D60A844EBB0921C03544FF63E)
* [Zijn de HTML-tags op uw webpagina in een...](#section_F31A2F5D2C284AC084158A5BD763DC5D)
* [Hebt u onjuist gevormde HTML-commentaartags in uw...](#section_D1C39D79341845CB9C38579AABDF3A24)
* [Bevat uw webpagina koppelingen naar pagina&#39;s op een andere pagina...](#section_F8082759184049AAA8FA6342C1F84389)
* [Gebruikt u een virtuele domeinservice voor uw URL...](#section_2861F09EA21A45E6B7E15F032739CDF3)
* [Gebruikt uw webpagina een meta-vernieuwingstag?](#section_5A2F544C237C49B8B1A7FE0C45371C0D)
* [Gebruikt uw webpagina een meta-robots-tag?](#section_36275A33DDFE4620BABA948F8A63DBD2)
* [Gebruikt uw website een uitsluitingsbestand voor robots?](#section_BF7B663347814F58AD736066C86B7D25)

## Hebt u uw indexlogboek onderzocht? {#section_D6626536DC3D40DDA4A1224F1CB276BF}

Het indexlogboek bevat gedetailleerde informatie die door de robot voor zoeken en verkopen van sites wordt verzameld terwijl deze uw website indexeert. Het logbestand bevat een lijst met koppelingen en aangetroffen fouten. Het onderzoeken van het indexlogboek is de beste plaats om te beginnen te bepalen waarom niet alle pagina&#39;s op uw website worden geïndexeerd.

Zie [Het volledige indexlogboek van een live of gefaseerd weergeven...](../c-about-index-menu/c-about-full-index.md#task_02E5E944C56B4EB19CC1FF321F3221B8).

Zie [Het incrementele indexlogboek van een live of gefaseerd weergeven...](../c-about-index-menu/c-about-incremental-index.md#task_E668E1F1240C476DAA1CA783DC728232).

## Hebt u typfouten in uw URL? {#section_BD2CEABC5D0F4A0DA38F3AD72ABBA676}

Wanneer u lange URL&#39;s in HTML-formulieren typt, kunnen er een of meer typografische fouten optreden. Onthoud dat URL&#39;s geen spaties mogen bevatten. Houd er rekening mee dat bepaalde webservers URL&#39;s in hoofdletters en kleine letters verwerken.

Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**. Controleer het volgende op de pagina [!DNL Staged URL Entrypoints]:

* U hebt geen typografische fouten in uw URL&#39;s.
* De tekens in de URL&#39;s gebruiken allemaal de juiste behuizing.
* De URL&#39;s bevatten geen spatietekens.

Als u de URL-ingangen wilt testen, kopieert en plakt u een URL in een webbrowser om te zien of uw website wordt weergegeven. Als dit niet het geval is, controleert u opnieuw of u geen fouten hebt gemaakt in het URL-pad.

Zie [Informatie over URL-invoerpunten](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573).

## Heeft de ingangspunt-webpagina koppelingen naar andere pagina&#39;s op uw website? {#section_1C2D6ED54E7249268B555D9DC33352B3}

De robot voor het zoeken/verhandelen van sites crawt net als uw klant door uw website. door koppelingen van pagina naar pagina te volgen. Er moeten koppelingen aanwezig zijn op de entrypuntwebpagina voordat de zoekrobot andere pagina&#39;s op uw site kan zoeken en indexeren.

Zie [Meerdere URL-ingangspunten toevoegen die u wilt indexeren](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45).

## Zijn koppelingen naar andere pagina&#39;s op uw website ingesloten in JavaScript? {#section_EE34A67D60A844EBB0921C03544FF63E}

U kunt geavanceerde navigatietechnieken op uw website gebruiken, zoals roll-over-acties en menu&#39;s, die JavaScript gebruiken om aan andere pagina&#39;s te verbinden. De robot voor het zoeken en verhandelen van sites kan echter geen koppelingen volgen die zijn ingesloten in JavaScript.

U kunt dit probleem oplossen door verborgen koppelingen naar andere pagina&#39;s in de HTML met de JavaScript-code te plaatsen. Hoewel klanten van uw website deze verbindingen niet zien, vindt en kruipt de onderzoeksrobot hen nog. U kunt verborgen labels onder aan de pagina plaatsen vlak voor de tag `</body>`. Ze kunnen er als volgt uitzien:

```
<a href="/mydir/mypag1.html"></a> 
<a href="/mydir/mypag2.html"></a>
```

Een andere oplossing is om de URL&#39;s van de extra pagina&#39;s op uw website weer te geven als ingangspunten die u wilt doorzoeken en indexeren. Begin URLs met `https://` zoals aangetoond in het volgende:

```
https://www.mydomain.com/mydir/mypag1.html 
https://www.mydomain.com/mydir/mypag2.html
```

Zie [Meerdere URL-ingangspunten toevoegen die u wilt indexeren](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45).

## Zijn de HTML-tags op uw webpagina in een ongeldige volgorde? {#section_F31A2F5D2C284AC084158A5BD763DC5D}

De HTML-specificatie vereist dat de `<html>`-, `<head>`- en `<body>`-tags een specifieke reeks in een HTML-document volgen. Tags in al uw webpagina&#39;s moeten de volgende volgorde hebben:

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

Als de HTML-tags niet in de juiste volgorde staan, kan de robot voor het zoeken/verkopen van sites de webpagina niet correct parseren en indexeren. Hieronder ziet u een voorbeeld van tags die zich niet in de juiste volgorde bevinden:

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

Plaats in dat geval de `<html>`-, `<head>`- en `<body>`-tags in de juiste volgorde op uw webpagina.

## Hebt u onjuist gevormde HTML-commentaartags in uw webpagina? {#section_D1C39D79341845CB9C38579AABDF3A24}

Zorg ervoor dat u eventuele ongeldige HTML-opmerkingen in uw webpagina&#39;s zorgvuldig controleert en corrigeert.

De HTML-specificatie vereist dat een HTML-opmerking begint met de tekens `<!--` en eindigt met de tekens `-->`. Het is gemakkelijk om verkeerd geformatteerde commentaren over het hoofd te zien die de plaats onderzoek/handelaarrobot veroorzaken om de markeringen op uw Web-pagina verkeerd te ontleden. Een onjuist gevormde opmerking kan ertoe leiden dat de robot die de site zoekt/verkoopt andere belangrijke tags mist die moeten worden geparseerd. Houd rekening met opmerkingen vlak voor de tag `<body>` in uw webpagina.

Hieronder ziet u een voorbeeld van een correct geformuleerde opmerking:

`<!-- This HTML comment is OK. -->`

Hieronder ziet u een voorbeeld van een onjuist geformuleerd commentaar:

```
<!- This HTML comment is improperly formed. -> 
<! This HTML comment is also improperly formed. >
```

## Bevat uw webpagina koppelingen naar pagina&#39;s in een ander domein? {#section_F8082759184049AAA8FA6342C1F84389}

Een website kan vaak bestaan uit pagina&#39;s die eigenlijk op een Webserver met een verschillend domeinadres bestaan. Stel bijvoorbeeld dat uw hoofdwebsiteadres het volgende is:

`https://www.mydomain.com/`

Uw website kan ook pagina&#39;s in een ander domein hebben, zoals:

`https://www.otherdomain.com/`

Standaard volgt de robot voor het zoeken/verhandelen van sites geen koppelingen op een ander domein dan het hoofddomein. Door echter extra ingangspunten voor uw zoekaccount in te stellen, kunt u eenvoudig meerdere domeinen indexeren.

Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**. Voeg de URL van het ingangspunt voor de hoofdwebsite van uw site toe. Voeg vervolgens extra URL-ingangen toe aan andere domeinen die sitepagina&#39;s bevatten. Stel bijvoorbeeld uw hoofd-URL-ingangspunt in op:

`https://www.mydomain.com/`

en voeg het volgende extra site-URL-ingangspunt toe:

`https://www.otherdomain.com/`

## Gebruikt u een virtuele domeinservice voor uw URL? {#section_2861F09EA21A45E6B7E15F032739CDF3}

Mogelijk gebruikt u een virtuele domeinservice (ook wel een &quot;domeinomleidingsservice&quot; genoemd) om klanten een betere URL te bieden om naar uw website te gaan. Stel dat het werkelijke adres van uw website het volgende is:

`https://www.myispdomain.com/~myname/mywebpages/`

U gebruikt echter een virtuele domeinservice, zodat klanten naar uw site kunnen gaan op de volgende adressen:

`https://myname.adomain.com/`

of

`https://adomain.com/myname/`

Standaard volgt de robot voor het zoeken/verhandelen van sites geen koppelingen op een ander domein dan het hoofddomein. Door echter extra ingangspunten voor uw zoekaccount in te stellen, kunt u eenvoudig meerdere domeinen indexeren.

Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**. Voeg het ingangspunt URL van de hoofdwebsite toe aan de virtuele domeinnaam van uw site. Voeg vervolgens extra ingangspunten toe aan het domein waar uw website feitelijk woont.

U kunt bijvoorbeeld het volgende hoofdtoegangspunt voor de URL instellen:

`https://myname.adomain.com/`

Voeg het volgende URL-ingangspunt voor de website toe:

`https://www.myispdomain.com/~myname/mywebpages/`

## Gebruikt uw webpagina een meta-vernieuwingstag? {#section_5A2F544C237C49B8B1A7FE0C45371C0D}

Veel websites hebben een voorpagina met een meta-vernieuwingstag tussen de `<head>...</head>`-tags, vergelijkbaar met het volgende:

`<meta http-equiv="Refresh" content="0;URL=https://www.adomain.com/apath/afile.html">`

In bepaalde omstandigheden kan de robot voor het zoeken/verhandelen van sites de URL voor het vernieuwen van meta niet volgen om de inhoud van uw website te indexeren. Dit probleem kunt u eenvoudig oplossen door extra toegangspunten in te stellen.

Klik in het productmenu op **[!UICONTROL Settings]** > Crawling > **[!UICONTROL URL Entrypoints]**. Voeg een ander ingangspunt aan URL van meta toe verfrist markering.

## Gebruikt uw webpagina een meta-robots-tag? {#section_36275A33DDFE4620BABA948F8A63DBD2}

Soms gebruiken webpagina&#39;s meta-robots-tags om webrobots te beheren die periodiek proberen door een website te kruipen. Metarobots-tags worden weergegeven tussen de `<head>...</head>`-tags van een webpagina en zien er ongeveer als volgt uit:

`<meta name="robots" content="noindex, nofollow">`

Omdat de robot voor het zoeken en verhandelen van sites zelf een webrobot is, volgt deze de richting van de meta-robots-tag. Door andere robots op deze manier uit te sluiten sluit u ook de robot voor zoeken/verkopen van sites uit.

U kunt meer over Web robots en het Protocol van de Uitsluiting Robots bij het volgende leren:

[https://www.robotstxt.org/orig.html](https://www.robotstxt.org/orig.html)

Verwijder of wijzig de meta-robots-tag op de webpagina&#39;s die u wilt indexeren op uw website.

## Gebruikt uw website een uitsluitingsbestand voor robots? {#section_BF7B663347814F58AD736066C86B7D25}

Soms heeft een website een pagina met de naam robots.txt die alle of bepaalde robots ervan weerhoudt te crawling. Als u wilt controleren of uw website een bestand robots.txt heeft, zoekt u het naar het bestand vlak onder het domein op hoofdniveau, zoals hieronder wordt weergegeven:

`https://www.yourdomain.com/robots.txt`

De inhoud van het bestand robots.txt ziet er ongeveer als volgt uit:

```
User-agent: * 
Disallow: /
```

Omdat de robot voor het zoeken en verhandelen van sites zelf een webrobot is, volgt deze de aanwijzingen in het bestand robots.txt. De robot voor het zoeken en verhandelen van sites wordt hier niet in opgenomen. Als u dit probleem wilt verhelpen, bewerkt u het uitsluitingsbestand voor robots (robots.txt) zodat de robot voor het zoeken/verhandelen van sites kan doorkruipen en uw website als volgt kan indexeren:

```
User-agent: Atomz/1.0 
Disallow: 
 
User-agent: * 
Disallow: /
```

## Microsoft Office {#reference_A85FCC8A96514A7584F4D2A8AC8111D1}

Een pagina met veelgestelde vragen waarin de ondersteuning van het indexeren en zoeken van Microsoft® Office-bestanden op een website wordt besproken.

Hieronder volgen algemene vragen over Microsoft Office-bestanden:

* [Wat wordt geïndexeerd in een dossier van Microsoft Office?](#section_8681DADFCFE24B7787B1FC08D431EE28)
* [Wat niet in een dossier van Microsoft Office wordt geïndexeerd...](#section_BD53BDABFDD94D7EB0E1F55EC18017BB)
* [Hoe worden Microsoft Office-bestanden anders geïndexeerd dan HTML-pagina&#39;s...](#section_C104B44684F340549A6B9EB8F39EDDBB)
* [Hoe voorkom ik dat Microsoft Office-bestanden worden geïndexeerd...](#section_FEBA71274CD14CB99731ADF982087F4C)

## Wat wordt geïndexeerd in een dossier van Microsoft Office? {#section_8681DADFCFE24B7787B1FC08D431EE28}

De volledige inhoud van Microsoft Word-bestanden, Microsoft Excel-bestanden en Microsoft PowerPoint-bestanden wordt geïndexeerd.

De volgende onderdelen van een Microsoft Word-bestand worden geïndexeerd:

* Titel
* Trefwoorden
* Onderwerp (beschrijving)
* Op tekst gebaseerde inhoud
* Hyperlinks naar andere documenten

De volgende onderdelen van een Microsoft Excel-bestand worden geïndexeerd:

* Titel
* Trefwoorden
* Onderwerp (beschrijving)
* Tekst in cellen
* Waarden van numerieke formules in cellen

De volgende onderdelen van een Microsoft PowerPoint-bestand worden geïndexeerd:

* Titel
* Trefwoorden
* Onderwerp (beschrijving)
* Tekst op elke dia

## Wat wordt niet geïndexeerd in een dossier van Microsoft Office? {#section_BD53BDABFDD94D7EB0E1F55EC18017BB}

Afbeeldingen die zich in Microsoft Office-bestanden bevinden, of tekst die deel uitmaakt van een ingesloten afbeelding, worden niet geïndexeerd. Definities van aangepaste eigenschappen worden niet als metagegevens geïndexeerd. Sommige tekst in speciale velden, zoals kop- en voetteksten in een PowerPoint-bestand, wordt ook niet geïndexeerd.

## Hoe worden Microsoft Office-bestanden anders geïndexeerd dan HTML-pagina&#39;s? {#section_C104B44684F340549A6B9EB8F39EDDBB}

Het verschil tussen de indexering van Microsoft Office-bestanden en HTML-bestanden door de zoekrobot is dat elk HTML-bestand een afzonderlijke pagina is en dat één Microsoft Office-bestand honderden pagina&#39;s kan vertegenwoordigen. Daarom wordt elke pagina binnen een Microsoft Office-bestand geteld als een afzonderlijke pagina onder uw zoekaccount.

## Hoe voorkom ik dat Microsoft Office-bestanden op mijn website worden geïndexeerd? {#section_FEBA71274CD14CB99731ADF982087F4C}

Als u niet wilt dat de zoekrobot doorloopt en Microsoft Office-bestanden indexeert, deselecteert u het inhoudstype **[!UICONTROL Microsoft Office Files]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**).

U kunt [!DNL URL Masks] ook gebruiken om het indexeren van de dossiers van Microsoft Office onbruikbaar te maken.

Voer de volgende URL-maskers in:

<table> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Als u geen reguliere expressies gebruikt </p> </td> 
   <td colname="col2"> 
    <ul id="ul_DFEC911DA11C484C8E4671A0F00E1F88"> 
     <li id="li_2E50374E3869426B97353A5A8CBE09EC">exclude *.doc </li> 
     <li id="li_9089D11161524D90849CA88F703772B6">*.xls uitsluiten </li> 
     <li id="li_7F6CFC6212E64C04AAF38E21A667C763">*.ppt uitsluiten </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Als u reguliere expressies gebruikt </p> </td> 
   <td colname="col2"> 
    <ul id="ul_012A45C3EC04460EA09C0ECFB49A8FA9"> 
     <li id="li_0C239F0A536D465F85A98EBF7B6ADF27">regexp ^ uitsluiten.*\.doc$ </li> 
     <li id="li_9F91DA35A2A646ACAFF2BA37F9136E2A">regexp ^ uitsluiten.*\.xls$ </li> 
     <li id="li_9D768D9EA2DB44FBB00A1979E21672E2">regexp ^ uitsluiten.*\.ppt$ </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

Zie [URL-maskers toevoegen om delen van te indexeren of niet te indexeren..](../c-about-settings-menu/c-about-crawling-menu.md#task_E1AFC17C746048B8843013D979E082C1).

Zie [Gewone uitdrukkingen](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

## MP3 {#reference_7614250EE81C4EEFA43E57A6A74E83D7}

Een pagina met veelgestelde vragen bevat ondersteuning voor het indexeren en zoeken van MP3-muziekbestanden op een website.

Hieronder volgen algemene vragen over MP3-bestanden.

* [Wanneer is een MP3-bestand gekropen en geïndexeerd?](#section_538EA1682C9C47E3A62640BB25D84C36)
* [Wat moet ik doen om te kruipen en te indexeren...](#section_3CD794446E3545379C14E9F222118665)
* [Hoe wordt een MP3-bestand herkend?](#section_230E7336965A424F96C5CCF1D3C2D103)
* [Wat wordt er geïndexeerd in een MP3-bestand?](#section_E99D252B27CA4946AED3FCD3ABD8779D)
* [Telt een MP3-bestand als een pagina?](#section_9910BEB6617D4D2090558CDF6C65D16B)
* [Hoe voorkom ik dat afzonderlijke MP3-bestanden worden geïndexeerd...](#section_C989DC1D3D3841B38F683A462195DC05)
* [Hoe voorkom ik dat MP3-bestanden worden geïndexeerd?](#section_305D2B28D1124776B6DC0C62A17827C6)
* [Waarom kan ik de Chinese, Japanse of Koreaanse MP3-bestanden niet doorzoeken op mijn site?](#section_06A48DA3F9E742CC93CC8B5CCD7382FA)

## Wanneer is een MP3-bestand gekropen en geïndexeerd? {#section_538EA1682C9C47E3A62640BB25D84C36}

MP3-bestanden lopen vast en indexeren op een van de volgende twee manieren. De meest gebruikelijke manier is van een href-ankertag in een HTML-bestand:

`<a href="MP3-file-URL"></a>`

Een tweede manier is door de URL van het MP3-bestand in te voeren als een URL-ingangspunt.

Zie [Informatie over URL-invoerpunten](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573).

## Wat moet ik doen om te kruipen en de MP3 dossiers op mijn plaats te indexeren? {#section_3CD794446E3545379C14E9F222118665}

Als u MP3-crawling en -indexering voor uw account wilt activeren, klikt u in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**. Selecteer **[!UICONTROL Text in MP3 Music Files]** op de pagina [!DNL Staged Content Types].

Zie [Informatie over inhoudssoorten](../c-about-settings-menu/c-about-crawling-menu.md#concept_6FEA1355C0374500B4C53090C34A8A07).

## Hoe wordt een MP3-bestand herkend? {#section_230E7336965A424F96C5CCF1D3C2D103}

Een MP3-bestand wordt herkend door het MIME-type, namelijk &quot;audio/mpeg&quot;.

## Wat wordt er geïndexeerd in een MP3-bestand? {#section_E99D252B27CA4946AED3FCD3ABD8779D}

In MP3-bestanden wordt optioneel een kleine hoeveelheid tekstuele informatie opgeslagen. Deze informatie kan bestaan uit de albumnaam, de naam van de artiest, de titel van het nummer, het genre van het nummer, het jaar van de release en een opmerking. Deze informatie wordt opgeslagen helemaal aan het eind van het dossier in wat wordt genoemd TAG. MP3-bestanden die TAG-informatie bevatten, worden als volgt geïndexeerd:

* De titel van het nummer wordt behandeld als de titel van een HTML-pagina.
* De opmerking wordt behandeld als een beschrijving die is gedefinieerd voor een HTML-pagina.
* Het genre wordt behandeld als een trefwoord dat is gedefinieerd voor een HTML-pagina.
* De naam van de artiest, de albumnaam en het jaar van uitgave worden beschouwd als de hoofdtekst van een HTML-document.

## Telt een MP3-bestand als een pagina? {#section_9910BEB6617D4D2090558CDF6C65D16B}

Ja, elk MP3-bestand dat op uw website is gekropen en geïndexeerd, wordt als één pagina geteld.

## Hoe voorkom ik dat afzonderlijke MP3-bestanden worden geïndexeerd? {#section_C989DC1D3D3841B38F683A462195DC05}

omring de ankerlabels die aan de MP3-bestanden zijn gekoppeld met de tags `<nofollow>` en `</nofollow>`. De zoekrobot volgt de koppelingen tussen deze tags niet.

Een andere methode is het toevoegen van de URL&#39;s van de MP3-bestanden als uitsluitingsmaskers.

Zie [Informatie over URL-maskers](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164).

Zie [Informatie over script voor URL-maskers](../c-about-settings-menu/c-about-filtering-menu.md#concept_384F32EA18F84853A7BA99A04009330B).

## Hoe voorkom ik dat MP3-bestanden worden geïndexeerd? {#section_305D2B28D1124776B6DC0C62A17827C6}

De eenvoudigste manier om MP3-indexering voor uw account te beheren, is door **[!UICONTROL Text in MP3 Music Files]** op de pagina [!DNL Staged Content Types] uit te schakelen.

Zie [Inhoudstypen selecteren om door te kruipen en te indexeren](../c-about-settings-menu/c-about-crawling-menu.md#task_CCAC5C67C8BF4AB7B79D34A1495D5EE8).

U kunt ook de functie URL-maskers gebruiken om MP3-indexering via bestandsextensie uit te schakelen. Om dit te doen, op het productmenu, klik **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Masks]**. Voer een van de volgende maskers in:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Als uw account... </p> </th> 
   <th colname="col2" class="entry"> <p>Het volgende URL-masker invoeren </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Gebruikt geen reguliere expressies </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> *.mp3 uitsluiten  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gebruikt reguliere expressies </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> regexp ^ uitsluiten.*\.mp3$ </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Zie [Gewone uitdrukkingen](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

## Waarom kan ik de Chinese, Japanse of Koreaanse MP3-bestanden niet doorzoeken op mijn site? {#section_06A48DA3F9E742CC93CC8B5CCD7382FA}

Als u in Chinese, Japanse of Koreaanse MP3-bestanden wilt zoeken, klikt u in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]** > **[!UICONTROL Text in MP3 Music Files]**. Klik vervolgens op **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Injections]** en geef de tekenset op die wordt gebruikt om de MP3-bestanden te coderen.

Zie [Inhoudstypen selecteren om door te kruipen en te indexeren](../c-about-settings-menu/c-about-crawling-menu.md#task_CCAC5C67C8BF4AB7B79D34A1495D5EE8).

Zie [Informatie over injecties](../c-about-settings-menu/c-about-metadata-menu.md#concept_DA091920671948A0A893A26B3A2FAAE5).

## PDF {#reference_F127C4915A0D436DA34E5D75ABFBB21B}

In een pagina met veelgestelde vragen wordt de ondersteuning van het indexeren en zoeken van PDF-bestanden op een website besproken.

Hieronder volgen algemene vragen over PDF-bestanden:

* [Wat wordt er geïndexeerd in een PDF-bestand?](#section_62BFCD7158B44F2BB3B1864224B50174)
* [Wat wordt niet geïndexeerd in een PDF-bestand?](#section_A14B353AE503408896BACBBF3F748FA0)
* [Hoe worden geïndexeerde PDF-bestanden geteld?](#section_C35DE36A65D649BD8FF314E9EFD990A6)
* [Kan in de zoekresultaten een PDF-pictogram worden weergegeven?](#section_829CE82CC3544502A13D27C4DB820189)
* [Kan de zoekresultaten koppelen naar een bepaalde pagina in...](#section_A06E7F7017E6441E98209D288EE57BF6)
* [Hoe voorkom ik dat PDF-bestanden worden geïndexeerd...](#section_96671419A822486AAC654D8DAD819940)
* [Hoe komt het dat ik de Chinese, Japanse of Koreaanse PDF-bestanden niet kan doorzoeken op mijn website?](#section_D41CA8EFCA0242EA8CF5F8F1924E4CD8)

## Wat wordt er geïndexeerd in een PDF-bestand? {#section_62BFCD7158B44F2BB3B1864224B50174}

De volledige inhoud van PDF-bestanden wordt geïndexeerd. De volgende delen van een PDF-bestand worden geïndexeerd:

* Titel
* Trefwoorden
* Onderwerp (beschrijving)
* Op tekst gebaseerde inhoud

## Wat wordt niet geïndexeerd in een PDF-bestand? {#section_A14B353AE503408896BACBBF3F748FA0}

De PDF-inhoudsopgave, afbeeldingen in het bestand of tekst die deel uitmaakt van een ingesloten afbeelding, worden niet geïndexeerd.

## Hoe worden geïndexeerde PDF-bestanden geteld? {#section_C35DE36A65D649BD8FF314E9EFD990A6}

Elk PDF-bestand wordt als één document geteld, inclusief PDF&#39;s die meerdere pagina&#39;s bevatten.

## Kan in de zoekresultaten een PDF-pictogram worden weergegeven? {#section_829CE82CC3544502A13D27C4DB820189}

Ja. Met de tag `<search-if-link-extension>` in de sjabloon kunt u een PDF-pictogram of andere afbeeldingen of tekst in de zoekresultaten opnemen:

```
<search-results> 
  ... 
  <search-if-link-extension value=".pdf"> 
    <img src="/search/i/pdficon.gif"> 
  </search-if-link-extension> 
  ... 
</search-results>
```

Met PDF-pictogrammen kunnen uw klanten weten dat een zoekresultaat is gekoppeld aan een PDF-bestand dat erg groot kan zijn. De bestandsgrootte kan van belang zijn voor klanten die uw website openen via een modem of een mobiel apparaat.

## Kunnen de zoekresultaten een koppeling maken naar een bepaalde pagina in een PDF-bestand? {#section_A06E7F7017E6441E98209D288EE57BF6}

Ja. Met de sjabloontag voor slimme koppelingen ( `<search-smart-link>...</search-smart-link>`) kunnen klanten klikken om de eerste PDF-pagina met het zoekresultaat te openen.

Als u slimme koppelingen wilt gebruiken, vervangt u de `<search-link>...</search-link>`-tags in de sectie met zoekresultaten van de sjabloon door `<search-smart-link>...</search-smart-link>`-tags. Wanneer een klant op een koppeling klikt die door de tags voor slimme koppelingen wordt gegenereerd, gaat de klant naar de eerste PDF-pagina die relevant is voor de zoekopdracht.

>[!NOTE]
>
>Als u deze functie wilt gebruiken, moet de klant een recente versie van de Adobe Acrobat of Adobe Acrobat-Reader gebruiken, die de markeringsplug-in en de External Window Handler (EWH)-plug-in moet bevatten. Bovendien moet hun webbrowser de Adobe Acrobat-insteekmodule voor Netscape Navigator gebruiken (u kunt elke browser gebruiken die deze insteekmodule voor Netscape Navigator accepteert) of het Acrobat ActiveX-besturingselement voor Internet Explorer 4.0 en hoger.

Zie [Sjabloontags zoeken](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4).

## Hoe voorkom ik dat PDF-bestanden op mijn website worden geïndexeerd? {#section_96671419A822486AAC654D8DAD819940}

Als u niet wilt dat de zoekrobot doorloopt en PDF-bestanden indexeert, deselecteert u het inhoudstype **[!UICONTROL PDF Documents]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**).

U kunt er ook voor kiezen [!DNL URL Masks] te gebruiken om PDF-indexering uit te schakelen.

Zie [URL-maskers toevoegen om delen van te indexeren of niet te indexeren..](../c-about-settings-menu/c-about-crawling-menu.md#task_E1AFC17C746048B8843013D979E082C1).

Voer een van de volgende URL-maskers in om PDF-indexering uit te schakelen:

* `exclude *.pdf` (als u geen reguliere expressies gebruikt)
* `exclude regexp ^.*\.pdf$` (als u reguliere expressies gebruikt)

Zie [Gewone uitdrukkingen](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

## Hoe komt het dat ik de Chinese, Japanse of Koreaanse PDF-bestanden niet kan doorzoeken op mijn website? {#section_D41CA8EFCA0242EA8CF5F8F1924E4CD8}

Bij zoeken/verhandelen van sites wordt UTF-8 van PDF-bestanden zonder taalaanduiding verkregen. Als u het inhoudstype **[!UICONTROL PDF Documents]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**) hebt geselecteerd, moet u meta-gegevensinjecties gebruiken om de taal te specificeren die in het Pdf- dossier wordt gebruikt.

Zie [Veldinjectiedefinities toevoegen](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE).

## Te veel pagina&#39;s {#reference_48A748BC1ED14844ACAC2735C8388E8A}

Een pagina met veelgestelde vragen waarin een aantal redenen wordt uitgelegd waarom de indexator meer pagina&#39;s heeft geteld dan u eigenlijk hebt, en hoe de oplossing in elk geval is.

Als u zeker weet dat uw website onder uw paginalimiet ligt, maar de indexeerfunctie geeft aan dat de limiet is bereikt, kunt u deze veelvoorkomende vragen en antwoorden voor mogelijke oplossingen beter controleren.

* [Hebt u uw diverse indexlogboeken onderzocht?](#section_C929BF9FDA6B4C9A9078C45AFE80EFE8)
* [Worden CGI-programma&#39;s geïndexeerd op uw website?](#section_86ED8A641B3841EC80153B4F107548FD)
* [Heeft uw server ingeschakeld bladeren door mappen?](#section_073C88EEE74F4CA0AD2C7145D4810B22)
* [Zijn er forums of nieuwsgroepen op uw website?](#section_8DCB94F0850A41B9B2EA885F779E2F84)
* [Zijn er PDF- of Microsoft Office-bestanden op uw website...](#section_455FC5438DF74E68AB9A31D359EAD4D9)
* [Hebt u meerdere URL-ingangen?](#section_8C54AFD7DF56472A9364D516482B534C)
* [Hebt u de interne bytes of tijdslimieten van overschreden...](#section_AE1BE61A58864FFE81F0BCEED2EBB15D)

## Hebt u uw diverse indexlogboeken onderzocht? {#section_C929BF9FDA6B4C9A9078C45AFE80EFE8}

Het indexlogboek bevat gedetailleerde informatie die is verzameld door de robot voor zoeken en verkopen van sites tijdens het indexeren van uw website. Het logboek bevat een lijst met alle gekropen koppelingen en aangetroffen fouten. Het onderzoeken van het indexlogboek is de beste plaats om te beginnen wanneer u probeert om te bepalen welke pagina&#39;s worden geïndexeerd.

Zie [Het volledige indexlogboek van een live of gefaseerd weergeven...](../c-about-index-menu/c-about-full-index.md#task_02E5E944C56B4EB19CC1FF321F3221B8).

Zie [Het incrementele indexlogboek van een live of gefaseerd weergeven...](../c-about-index-menu/c-about-incremental-index.md#task_E668E1F1240C476DAA1CA783DC728232).

Zie [Het gescripte incrementele-indexlogboek van een live of... weergeven.](../c-about-index-menu/c-about-scripted-index.md#task_CBFCE9B9A87B4DF7A2A35A6E83DE93D7).

Zie [Het opnieuw gegenereerde indexlogboek van een live of gefaseerd weergeven...](../c-about-index-menu/c-about-regenerate-index.md#task_61CE8F9E7BF84BA89A8D482B2106BB15).

Zie [Het opnieuw gerangschikte indexlogboek van een live of gefaseerde website weergeven](../c-about-index-menu/c-about-re-rank-index.md#task_3C76107DFAC1495FACD3ABB0A688208D).

## Worden CGI-programma&#39;s geïndexeerd op uw website? {#section_86ED8A641B3841EC80153B4F107548FD}

CGI-programma&#39;s gebruiken URL-parameters die er soms toe leiden dat de indexeerfunctie meerdere &#39;nepURL&#39;s&#39; doorloopt. Als de plaatsonderzoek/de handel drijft uw programma&#39;s van CGI en het volgen URLs met parameters CGI in hen leest, zijn er waarschijnlijk verscheidene veelvouden van pagina&#39;s die worden gekropen en worden geïndexeerd die niet nuttig voor uw onderzoeksindex zijn. De typische parameters van CGI verschijnen in URLs met `?` of `&` karakters.

U kunt de CGI-programma&#39;s maskeren zodat ze niet worden geïndexeerd met de functie URL-maskers. U kunt een URL-voorvoegsel maskeren of reguliere expressies gebruiken om uw CGI-scripts te maskeren.

Zie [Informatie over URL-maskers](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164).

Zie [Informatie over script voor URL-maskers](../c-about-settings-menu/c-about-filtering-menu.md#concept_384F32EA18F84853A7BA99A04009330B).

Zie [Gewone uitdrukkingen](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

## Heeft uw server ingeschakeld bladeren door mappen? {#section_073C88EEE74F4CA0AD2C7145D4810B22}

Wanneer voor een webserver bladeren met mappen is ingeschakeld en een bepaalde map geen bestand index.html bevat, kan bij een bezoek aan die map een lijst met bestanden in die map worden weergegeven. Doorgaans staan er koppelingen boven aan de pagina, zodat u de lijst op verschillende manieren kunt sorteren, bijvoorbeeld door te klikken op **[!UICONTROL Name]**, **[!UICONTROL Last modified]**, **[!UICONTROL Size]** enzovoort. Doorgaans worden deze als URL&#39;s in het indexlogboek voor zoeken/wijzigen van sites weergegeven met tekens zoals `?M=A` aan het einde. De site zoekt/verkoopt de index aan en volgt deze als koppelingen. Dit kan ertoe leiden dat meerdere &#39;onechte&#39; URL&#39;s worden geïndexeerd.

Een goed ontworpen website heeft meestal indexbestanden in elke map of het bladeren door mappen uitgeschakeld voor mappen zonder indexbestanden. Gelukkig is er een gemakkelijke manier om deze &quot;valse&quot; URL&#39;s te maskeren als u uw pagina&#39;s niet kunt wijzigen of directorylijsten op de server niet kunt uitschakelen.

Klik **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Masks]** om deze taak uit te voeren. Voeg een masker toe om het even welke URL te maskeren die het karakter `?` bevat. U kunt deze taak uitvoeren door het volgende reguliere-expressiemasker in te voeren:

`exclude regexp ^.*\?.*$`

Nadat u het masker hebt gemaakt, moet u de website opnieuw indexeren.

Zie [Een volledige index van een actieve of gefaseerde website uitvoeren...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

Zie [Een incrementele index van een actieve of gefaseerde website uitvoeren...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

## Zijn er forums of nieuwsgroepen op uw website? {#section_8DCB94F0850A41B9B2EA885F779E2F84}

Als forums of nieuwsgroepen op uw website worden gekropen, volgt deze mogelijk URL&#39;s voor verschillende weergaveopties of sorteeropties. Dit betekent dat dezelfde pagina meerdere malen wordt geïndexeerd.

Meestal worden forums of nieuwsgroepen geleverd met hun eigen zoekmachines. In dat geval kunt u [!DNL URL Masks] gebruiken om de forums te maskeren van het zoeken naar of het verhandelen van sites.

Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Masks]**. Op de pagina [!DNL Staged URL Masks] maskeert u uw forums door hun URL&#39;s in te voeren als uitsluitings-URL-maskers.

Zie [URL-maskers toevoegen om delen van te indexeren of niet te indexeren..](../c-about-settings-menu/c-about-crawling-menu.md#task_E1AFC17C746048B8843013D979E082C1).

Nadat u de maskers hebt gemaakt, moet u uw website opnieuw indexeren.

Zie [Een volledige index van een actieve of gefaseerde website uitvoeren...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

Zie [Een incrementele index van een actieve of gefaseerde website uitvoeren...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

## Zijn er PDF- of Microsoft Office-bestanden op uw website? {#section_455FC5438DF74E68AB9A31D359EAD4D9}

Als u PDF-bestanden of [!DNL Microsoft Office]-bestanden op uw website hebt, telt de indexgrootte van slechts een paar bestanden wellicht veel pagina&#39;s. Er worden meer pagina&#39;s geïndexeerd dan documenten die u hebt, omdat elke pagina in een PDF- of Microsoft Office-bestand als een aparte pagina wordt geteld.

Klik in het productmenu op **[!UICONTROL Index]** > **[!UICONTROL Full Index]** > **[!UICONTROL Live Index]**. Selecteer [!DNL Full Index] op de pagina en klik vervolgens **[!UICONTROL Full Index Now]** om een totaal aantal pagina&#39;s weer te geven. **[!UICONTROL Count All Pages]** Als u geen PDF-bestanden of Microsoft Office-bestanden wilt indexeren, kunt u dit inhoudstype uitschakelen onder **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**.

Zie [Een volledige index van een actieve of gefaseerde website uitvoeren...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

Zie [Informatie over inhoudssoorten](../c-about-settings-menu/c-about-crawling-menu.md#concept_6FEA1355C0374500B4C53090C34A8A07).

## Hebt u meerdere URL-ingangen? {#section_8C54AFD7DF56472A9364D516482B534C}

De robot voor zoeken/verhandelen van sites begint te crawling bij opgegeven URL-ingangen en volgt alle gevonden koppelingen naar alle inhoud in dat specifieke domein. Als u vele ingangspunten URL hebt gespecificeerd, kan een significant aantal pagina&#39;s worden gekropen.

Gebruik als volgt de `nofollow`-tag van het uitsluitingsprotocol voor robots in de koppen van de invoerpuntdocumenten op de extra domeinen:

```
<html> 
<head> 
<meta name="robots" content="nofollow"> 
</head>
```

De bovenstaande code vertelt de robot die de site zoekt/verkoopt de inhoud van de pagina te indexeren, maar niet de koppelingen naar extra pagina&#39;s te volgen.

U kunt meer over Web robots en het Protocol van de Uitsluiting Robots bij het volgende leren:

[https://www.robotstxt.org/orig.html](https://www.robotstxt.org/orig.html)

Als u geen toegang hebt tot de bron van de pagina&#39;s in andere domeinen, kunt u de meerdere URL-ingangen verwijderen. Dit helpt u indexerende activiteit slechts tot die domeinen beperken waarvan inhoud u klanten wilt kunnen zoeken.

Zie [Informatie over URL-invoerpunten](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573).

## Hebt u de interne bytes of tijdslimieten van het zoeken/verhandelen van sites overschreden? {#section_AE1BE61A58864FFE81F0BCEED2EBB15D}

Controleer of uw account de limiet op het scherm &quot;Volledige indexstatus&quot; heeft bereikt. Als de status meldt dat uw index langer is dan toegestaan of dat het langer duurt dan toegestaan, wordt uw website niet volledig geïndexeerd. U kunt deze fout corrigeren, zodat u de juiste dekking krijgt en een juiste telling van de websitepagina&#39;s.

Om plaatsonderzoek/handelingsservers te beschermen, zijn er interne grenzen op bytes en tijd. Alleen als bestanden met bladeren erg groot zijn of als de zoekfunctie/merchandising van de site traag verloopt op de server, worden deze limieten bereikt.

Als u een tijdslimiet hebt bereikt, controleert u of de server online is en probeert u de index later opnieuw. Als u een bytelimiet hebt bereikt, controleert u de gekropen bestanden door het indexlogboek te bekijken. Zijn ze ongewoon groot? Neem contact op met Technische ondersteuning als u een van deze berichten ziet.
