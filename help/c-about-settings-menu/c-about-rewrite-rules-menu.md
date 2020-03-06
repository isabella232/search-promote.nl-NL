---
description: Gebruik het Rewrite menu van Regels om te plaatsen kruipt en onderzoek URL en titelregels.
seo-description: Gebruik het Rewrite menu van Regels om te plaatsen kruipt en onderzoek URL en titelregels.
seo-title: Informatie over het menu Regels herschrijven
solution: Target
subtopic: Rewrite Rules
title: Informatie over het menu Regels herschrijven
topic: Settings,Site search and merchandising
uuid: 77ee84dd-fdba-4d34-ae8e-2fe786599800
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a

---


# Informatie over het menu Regels herschrijven {#about-the-rewrite-rules-menu}

Gebruik het Rewrite menu van Regels om te plaatsen kruipt en onderzoek URL en titelregels.

## URL-regels voor winkelobjecten overschrijven {#concept_B71CF4C8030A4A74A22C3BFE4DE3B865}

kruipt URL-regels specificeren hoe de URL&#39;s die het tegenkomt binnen de webinhoud worden herschreven. U kunt een onbeperkt aantal regels en voorwaarden specificeren, en u kunt om het even welk gedeelte van ontmoet URLs manipuleren.

<!-- 

c_about_crawl_list_store_url_rules.xml

 -->

De kruipende regels zijn het nuttigst om dynamische delen van een URL, zoals een zittingsherkenningsteken te herschrijven dat voor elke klant uniek is die uw website bezoekt. U kunt ook gebruiken herschrijft regels om gedeelten van een URL, zoals vraagparameters, van de onderzoeksrobot te verbergen. Door gebrek, worden geen regels gespecificeerd en geen URL wordt het herschrijven uitgevoerd.

Aangezien een website wordt gekropen, wordt ingebedde inhoud URLs opgeslagen in een tijdelijke lijst van extra Web-pagina&#39;s om te kruipen. Voordat een URL aan deze lijst wordt toegevoegd, worden de regels voor het herschrijven van winkels op deze lijst toegepast. Typisch, herschrijft de Opslag regels worden gebruikt om een zittingsidentiteitskaart uit een URL te verwijderen of een specifieke zittingsidentiteitskaart af te dwingen voor kruipend. Wanneer de onderzoeksrobot een URL van de lijst terugwint, herschrijf de Retrieve regels worden gebruikt om gedeelten van die URL opnieuw te manipuleren. Typisch, wint regels terug wordt gebruikt voor het opnemen van tijd-gevoelige gegevens terug in URL terug. Het is deze definitieve URL die wordt gebruikt om de pagina van uw website eigenlijk terug te winnen.

Zie [over kruipende Lijst terugwinnen URL Regels](../c-about-settings-menu/c-about-rewrite-rules-menu.md#concept_EC8E2E48B99A458D8567B526C9827CBA).

Meestal gebruik je alleen URL-regels voor winkel. Win Regels terug URL is slechts noodzakelijk als URLs dynamische gegevens, zoals een zittingsidentiteitskaart bevat, en als die dynamische gegevens in tijd veranderen om geldig te blijven. In dit geval, gebruik u de Regels van de Opslag URL om de meest recente staat van de gegevens van ontmoet URLs te krijgen. Dan gebruik u terugwinnen URL Regels om die gegevens aan elke URL toe te voegen wanneer de onderzoeksrobot probeert om de pagina terug te winnen.

Elke regel wordt gespecificeerd met een herschrijf regel (RewriteRule) richtlijn en één of meerdere facultatieve herschrijf voorwaarden (RewriteCond). De volgorde van de regels is belangrijk. De regelreeks wordt van een lus voorzien door regel door. Wanneer een regel aanpast, het lijnen door om het even welke overeenkomstige herschrijft voorwaarden. Een kruipende regel URL wordt gespecificeerd op de volgende manier:

```
RewriteCond TestString CondPattern [Flags] 
RewriteRule Pattern Substitution [Flags]
```

Wanneer een ingebedde URL wordt ontmoet, probeert de onderzoeksrobot om URL aan het Patroon van elke kruipende regel aan te passen. Als de patroongelijken, herschrijft de motor overeenkomstige richtlijnen RewriteCond zoekt. Als geen voorwaarden aanwezig zijn, wordt URL gesubstitueerd met een nieuwe waarde die van het koord van de Vervanging wordt geconstrueerd en met de volgende regel in de regelreeks verdergaat. Indien de voorwaarden bestaan, worden zij verwerkt in de volgorde waarin zij worden vermeld. De herschrijf motor probeert om een voorwaardenpatroon (CondPattern) tegen een testkoord (TestString) aan te passen. Als de twee gelijke, dan wordt de volgende voorwaarde verwerkt tot geen meer voorwaarden beschikbaar zijn. Als alle voorwaarden aanpassen, wordt URL vervangen met de Vervanging die in de regel wordt gespecificeerd. Als niet aan de voorwaarde wordt voldaan, ontbreekt de volledige reeks voorwaarden en de overeenkomstige regel.

## Informatie over richtlijnen herschrijven {#section_162122340BB34F12BB9A36DC9349092B}

Een richtlijn RewriteRule heeft de volgende vorm:

```
           
<i>RewriteRule Pattern Substitution [Flags]</i> 
        
```

`Pattern` kan een POSIX regelmatige uitdrukking zijn, die wordt toegepast op huidige URL. De &quot;huidige URL&quot;kan van originele gevraagde URL verschillen, omdat de vroegere regels reeds URL kunnen hebben aangepast en veranderd.

Zie [Regelmatige expressies](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

U kunt niet het &quot;niet&quot;karakter (&quot;!&quot;) gebruiken om het patroon voor te bereiden. Het &quot;niet&quot;karakter laat u een patroon negeren, namelijk om waar te zijn slechts als huidige URL NIET dit patroon aanpast. Het &quot;niet&quot;karakter kan worden gebruikt wanneer het beter is om een negatief patroon aan te passen, of als definitieve standaardregel.

>[!NOTE]
>
>U kunt niet zowel het &quot;niet&quot;karakter als gegroepeerde vervangingen in een patroon gebruiken. Bovendien kunt u geen verwaarloosd patroon gebruiken wanneer het substitutiekoord $N bevat.

U kunt haakjes gebruiken om een backreference in het patroon tot stand te brengen, dat door de Substitutie en CondPattern kan worden van verwijzingen voorzien.

**Vervanging** URL wordt vervangen door het substitutiekoord, dat het volgende bevat:

Gewone tekst: Tekst die door onveranderd wordt overgegaan.

De verwijzingen van de achtergrond verlenen toegang tot de gegroepeerde delen (binnenhaakje) van het Patroon of CondPattern. Het volgende is de twee types van backreferences:

* **Achterverwijzingen** van RewriteRule Deze gelijke backreferences in het overeenkomstige Patroon RewriteRule en nemen de vorm $N (0 &lt;= N &lt;= 9). Bijvoorbeeld: `RewriteRule ^https:// ([^/]*) (.*)$ https://${tolower: $1} $2.`

* **HerwriteCond Backreferences** Deze gelijke backreferences in het laatst overeenkomende RewriteCond CondPattern en nemen de vorm %N (0 &lt;= N &lt;= 9).

Variabelen: Dit zijn variabelen van de vorm % {NAME_OF_VARIABLE} waar NAME_OF_VARIABLE een koord voor de naam van een bepaalde variabele is. Zie de `*[E]*` vlag voor meer informatie bij het plaatsen van milieuvariabelen.

Functies: Dit zijn functies van de vorm $ {NAME_OF_FUNCTION:key} waar NAME_OF_FUNCTION het volgende is:

* de aanjager maakt alle karakters in *zeer belangrijke* kleine letters.
* toupper maakt alle karakters in *zeer belangrijke* hoofdletters.
* vlucht URL-codeert alle karakters in *sleutel*.
* De tekens &#39;a&#39;...z&#39;, &#39;A&#39;...Z&#39;, &#39;0&#39;...9&#39;, &#39;*&#39;, &#39;-&#39;, &#39;.&#39;, &#39;/&#39;, &#39;@&#39; en &#39;_&#39; ongewijzigd blijven; de ruimten worden vertaald in &quot;+&quot;, en alle andere karakters worden omgezet in hun %xx URL-Gecodeerde equivalent.
* unescape zet &#39;+&#39; terug naar spatie en alle %xx URL-gecodeerde tekens terug naar enkele tekens.

>[!NOTE]
>
>Er is een speciale substitutiekoord: `'-'` dat betekent &quot;GEEN vervanging&quot;. Het `'-'` koord wordt vaak gebruikt met C (ketting) vlag, latend u een URL aan verscheidene patronen aanpassen alvorens een substitutie voorkomt.

**Vlaggen**

(facultatief) sluit vlaggen in steunen in `[]`. De veelvoudige vlaggen zijn komma-gescheiden.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> "last|L" </p> </td> 
   <td colname="col2"> <p>Laatste regel. </p> <p>Houdt het herschrijvingsproces tegen en past geen extra herschrijvingsregels toe. Gebruik deze vlag om het even welke verdere verwerking aan huidige URL te verhinderen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'Volgende|N' </p> </td> 
   <td colname="col2"> <p>Volgende ronde. </p> <p> Reruns het het herschrijven proces (opnieuw beginnend met de eerste het herschrijven regel) gebruikend URL van de laatste het herschrijven regel (niet originele URL). Wees voorzichtig om geen dooflus te creëren! </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> "ketting|C" </p> </td> 
   <td colname="col2"> <p>Beeten met de volgende regel. </p> <p>Ketst de huidige regel aan de volgende regel (die ook aan zijn volgende regel kan worden geketend, etc.). Als een regel aanpast, dan gaat het substitutieproces zoals gebruikelijk verder. Als de regel niet aanpast, dan worden alle verdere geketende regels overgeslagen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> "no case|NC" </p> </td> 
   <td colname="col2"> <p>Geen zaak. </p> <p> Maakt het Patroon niet gevoelig geval (namelijk is er geen verschil tussen "A-Z"en "a-z") wanneer het patroon tegen huidige URL wordt aangepast. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> "skip|S=num" </p> </td> 
   <td colname="col2"> <p>Sla de volgende regel of regels over. </p> <p> Als de huidige regel aanpast, dwingt deze vlag de herschrijfmotor om de volgende numregels in de regelreeks over te slaan. Gebruik deze vlag om pseudo te maken als-dan-else concepten. De laatste regel van de toen-clausule wordt een skip=N waar N het aantal regels in de anders-clausule is. </p> <p> <p>Opmerking:  Deze vlag is niet hetzelfde als de 'chain|C' vlag!) </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> "env|E=VAR:VAL" </p> </td> 
   <td colname="col2"> <p>Plaatst de milieuvariabele. </p> <p>Creeert een milieuvariabele "VAR"die aan de waarde VAL wordt geplaatst, waar VAL regelmatige uitdrukkingsbackreferences, $N en %N kan bevatten, die worden uitgebreid. U kunt deze vlag meer dan eens gebruiken om veelvoudige variabelen te plaatsen. De variabelen kunnen later worden van verwijzingen voorzien in een volgend patroon RewriteCond via % {VAR}. </p> <p>Gebruik deze vlag om informatie van URLs te ontdoen en te herinneren. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>De opslag herschrijft Regels en Win herschrijft Regels herschrijft delen veranderlijke waarden. Wegens dit gedrag, kunt u een variabele aan een time-sensitive zittingswaarde plaatsen wanneer ingebedde URL wordt ontmoet en opgeslagen. Wanneer volgende URL van de tijdelijke opslaglijst wordt teruggewonnen, kan de recentste sessionid waarde aan het worden toegevoegd alvorens die pagina wordt teruggewonnen.

**Voorbeeld van een RewriteRule met een functie**

Veronderstel dat u een case-sensitive server hebt, die de koorden `"www.mydomain.com"` en `"www.MyDomain.com"` verschillend behandelt. Opdat uw server correct werkt, zorg ervoor dat het domein altijd is `"www.mydomain.com"` alhoewel sommige documenten verbindingen bevatten die van verwijzingen voorzien `"www.MyDomain.com."` om dit te doen, kon u de volgende regel gebruiken:

```
RewriteRule  ^https:// 
<b>([^/]*)</b> 
<i>(.*)</i>$  https://${tolower:$1}$2
```

Deze herschrijf regel gebruikt de functie `tolower` om het domeingedeelte van een URL te herschrijven om ervoor te zorgen dat het altijd in kleine letters zoals in het volgende is:

1. Het patroon `(^https://([^/]*)(.*)$)` bevat een backreference `([^/]*)` die alle karakters tussen `https://` en eerste `/` in URL aanpast. Het patroon bevat ook een tweede backreference `(.*)` die alle resterende karakters in URL aanpast.

1. De vervanging `(https://${tolower:$1}$2)` vertelt de onderzoeksmotor om URL te herschrijven door de `tolower` functie op de eerste backreference te gebruiken `(https:// ${tolower:$1}$2)` verlatend de rest van URL onaangetast `(https://${tolower:$1} $2)`.

Aldus, `https://www.MyDomain.com/INTRO/index.Html` wordt een URL van de vorm herschreven zoals `https://www.mydomain.com/INTRO/index.Html`.

## Informatie over richtlijnen herschrijvenCond {#section_CD5A19B2D3204F73B645411931FC34A1}

De richtlijn RewriteCond bepaalt een regelvoorwaarde. Wanneer een RewriteCond een RewriteRule voorafgaat, wordt de regel slechts gebruikt als zijn patroon de huidige titel aanpast en de extra voorwaarden van toepassing zijn. De herschrijvingsvoorwaarden nemen de volgende vorm aan:

```
           
<i>RewriteCond TestString CondPattern [Flags]</i> 
        
```

`TestString` is een koord dat de volgende concepten kan bevatten:

Gewone tekst: Tekst die door onveranderd wordt overgegaan.

De verwijzingen van de achtergrond verlenen toegang tot de gegroepeerde delen (binnenhaakje) van het Patroon of CondPattern. Het volgende is de twee types van backreferences:

* **Achterverwijzingen** van RewriteRule Deze gelijke backreferences in het overeenkomstige Patroon RewriteRule en nemen de vorm $N (0 &lt;= N &lt;= 9). Bijvoorbeeld, `RewriteRule ^https:// ([^/]*) (.*)$ https://${tolower: $1} $2`.

* **HerwriteCond Backreferences** Deze gelijke backreferences in het laatst overeenkomende RewriteCond CondPattern en nemen de vorm %N (0&lt;= N &lt;= 9).

Variabelen: Dit zijn variabelen van de vorm % {NAME_OF_VARIABLE} waar NAME_OF_VARIABLE een koord voor de naam van een bepaalde variabele kan zijn. Zie de RewriteRule vlag voor meer informatie bij het plaatsen van variabelen *`[E]`* .

Functies: Dit zijn functies van de vorm $ {NAME_OF_FUNCTION:key} waar NAME_OF_FUNCTION het volgende is:

* de aanjager maakt alle karakters in *zeer belangrijke* kleine letters.
* toupper maakt alle karakters in *zeer belangrijke* hoofdletters.
* vlucht URL-codeert alle karakters in sleutel. De tekens &#39;a&#39;...z&#39;, &#39;A&#39;...Z&#39;, &#39;0&#39;...9&#39;, &#39;*&#39;, &#39;-&#39;, &#39;.&#39;, &#39;/&#39;, &#39;@&#39;, en &#39;_&#39; worden ongewijzigd gelaten, worden de ruimten vertaald in &#39;+&#39;, en alle andere karakters worden omgezet in hun `%xx` URL-Gecodeerde equivalent.
* unescape zet &#39;+&#39; terug naar spatie om en alle `%xx` URL codeert karakters terug naar enkele karakters.

**CondPattern** is een standaard Uitgebreide Regelmatige Uitdrukking met sommige toevoegingen. Het patroonkoord kan met een `!` karakter (uitroepteken) worden vooraf bepaald om een niet-aanpassingspatroon te specificeren. In plaats van echte regelmatige uitdrukkingskoorden, kunt u één van de volgende speciale varianten gebruiken:

>[!NOTE]
>
>U kunt al deze tests met een uitroepteken (&#39;!&#39;) ook voorschrijven om hun betekenis te negeren.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CondPattern-tekenreeks </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> '&lt;CondPattern' </p> </td> 
   <td colname="col2"> <p>Lexisch minder. </p> <p> Behandelt CondPattern als duidelijk koord en vergelijkt het lexically bij TestString. Waar als TestString lexisch minder dan CondPattern is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '&gt;CondPattern' </p> </td> 
   <td colname="col2"> <p>Lexisch groter. </p> <p> Behandelt CondPattern als duidelijk koord en vergelijkt het lexically bij TestString. Waar als TestString lexisch groter is dan CondPattern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '=CondPattern' </p> </td> 
   <td colname="col2"> <p>Lexisch gelijk. </p> <p> Behandelt CondPattern als duidelijk koord en vergelijkt het lexically bij TestString. Waar als TestString lexisch gelijk aan CondPattern is, d.w.z., zijn de twee koorden precies gelijk (karakter door karakter). Als CondPattern enkel ""(twee aanhalingstekens) is, vergelijkt dit TestString met het lege koord. </p> </td> 
  </tr> 
 </tbody> 
</table>

**De vlaggen**(facultatief) sluiten vlaggen in steunen in `[]`. De veelvoudige vlaggen zijn komma-gescheiden.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> "no case|NC" </p> </td> 
   <td colname="col2"> <p> Geen zaak. </p> <p>Deze vlag maakt de test niet gevoelig geval, d.w.z., is er geen verschil tussen "A-Z"en "a-z"zowel in uitgebreide TestString als in CondPattern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> "ornext|OR" </p> </td> 
   <td colname="col2"> <p>Of de volgende voorwaarde. </p> <p>Gebruik deze vlag om regelvoorwaarden met lokaal OF in plaats van impliciet te combineren EN. Zonder deze vlag, zou u de voorwaarde/de regel veelvoudige tijden moeten schrijven. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Voorbeeld**

Sommige Web-pagina&#39;s wijzen een &quot;sessionid&quot;variabele van CGI toe de eerste keer een bezoeker bij een plaats aankomt. Deze variabele wordt gebruikt om de bezoeker te identificeren en, aangezien de bezoeker door de plaats doorbladert, wordt de variabele overgegaan langs. Omdat de zoekrobot lijkt op een bezoeker van je site, krijgt hij een sessionid-nummer toegewezen. De onderzoeksrobot handhaaft deze enige &quot;sessionid&quot;waarde, zelfs als een tweede plaatspagina probeert om een nieuwe waarde toe te wijzen. Om dit te verzekeren, hebt u twee herschrijvingsregels nodig.

De eerste regel wordt gebruikt om de sessionid variabele te identificeren en op te slaan:

```
RewriteCond  %{sessionid}  !.+ 
RewriteRule  ^.+sessionid= 
<b>([^&#]+)</b>.*$  -   
<i>[E=sessionid:$1]</i>
```

RewriteRule gebruikt een e-vlag `([E=sessionid:$1])` om de huidige waarde van de sessionid parameter van CGI aan de variabele toe te wijzen `sessionid`. De `$1` verwijzing verwijst naar de eerste backreference, die tussen de eerste reeks haakjes in het Patroon van RewriteRule bevat is `([^&#]+)`.

De regelmatige uitdrukking `^&#]+` past het gedeelte van een URL tussen het woord `sessionid` en het volgende `**&**or**#**` karakter aan. Aangezien dit RewriteRule slechts wordt gebruikt om de aanvankelijke waarde voor de sessionid variabele tot stand te brengen, herschrijft het niet. Merk op dat het gebied van de Substitutie van de regel aan `-` om wordt geplaatst te wijzen op dat geen het herschrijven wordt vereist.

RewriteCond onderzoekt de variabele `sessionid` ( `%{sessionid}`). Als het zelfs geen enkel karakter heeft (!..+), dan de gelijken RewriteRule.

Gebruikend deze regel, wordt URL gelezen als `https://www.domain.com/home/?sessionid=1234&function=start` en wijs de waarde `1234` aan de variabele toe `sessionid`.

De tweede regel wordt gebruikt om al URLs te herschrijven die het volgende Patroon RewriteRule aanpassen:

```
RewriteRule   
<b>^(.+)</b>sessionid=[^&#]+ 
<i>(.*)$</i>  $1sessionid=%{sessionid}$2
```

Het patroon RewriteRule bevat twee backreferences: `(.+)` en `(.*)`. De eerste backreference past alle karakters vóór aan `sessionid`. De tweede backreference past alle karakters na het eindigen aan `&` of `#`.

Het patroon van de Vervanging herschrijft URL gebruikend de eerste backreference, die door het koord &quot;sessionid=&quot;wordt gevolgd, die door de waarde van de variabele van zittingsidentiteitskaart door de eerste regel wordt bepaald, die door de tweede backreference wordt gevolgd `%{sessionid}`die. `($1sessionid=%{sessionid} $2)`

Bericht dat dit RewriteRule geen RewriteCond bevat. Als dusdanig, veroorzaakt het herschrijven voor al URLs die het *Patroon* RewriteRule aanpassen. Aldus, als de waarde van de sessionid variabele ( `%{sessionid}`) is `1234`, `https://www.domain.com/products/?sessionid=5678&function=buy` wordt een URL van de vorm herschreven zoals `https://www.domain.com/products/?sessionid=1234&function=buy`

## Erkenning {#section_B17088EF38244496BC1DDD4ECF75EB5B}

De software van de herschrijfmachine werd oorspronkelijk ontwikkeld door de Groep van Apache voor gebruik in het de serverproject van HTTP van Apache (https://www.apache.org/).

## Het toevoegen van een kruipende regel van de lijstopslag URL {#task_22DD40DF95584B12BE8E6ECFBF579BCD}

U kunt toevoegen kruipt de regels van de lijstopslag URL om te specificeren hoe URLs die binnen Webinhoud wordt ontmoet wordt herschreven. U kunt een onbeperkt aantal regels en voorwaarden specificeren, en u kunt om het even welk gedeelte van ontmoet URLs manipuleren.

<!-- 

t_adding_a_crawl_list_store_url_rule.xml

 -->

**Om toe te voegen kruip de regels van de lijstopslag URL**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Rewrite Rules]** > **[!UICONTROL Crawl List Store URL Rules]**.
1. Op het [!DNL Crawl List Store URL Rules] gebied, ga de regels in die u wilt.

   De lege lijnen en de commentaarlijnen die met een karakter &quot;#&quot;beginnen (knoeiboel) worden toegelaten.
1. (Facultatief) op de [!DNL Crawl List Store URL Rules] pagina, op het [!DNL Test Crawl List Store URL Rules] gebied, ga een test URL in waarvan kruipt regels u, dan **Test** testen en wilt klikken.
1. Klik **sparen Veranderingen**.
1. (Facultatief) herbouw uw gefaseerde plaatsindex als u aan voorproef de resultaten wilt.

   Zie [het Vormen van een stijgende index van een gefaseerde website](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Facultatief) op de [!DNL Crawl List Store URL Rules] pagina, doe om het even welke volgend:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Ongeveer kruipt de Lijst URL Regels terugwint {#concept_EC8E2E48B99A458D8567B526C9827CBA}

kruipt URL-regels specificeren hoe de URL&#39;s die worden aangetroffen in webinhoud worden herschreven. U kunt een onbeperkt aantal regels en voorwaarden specificeren, en u kunt om het even welk gedeelte van ontmoet URLs manipuleren.

<!-- 

c_about_crawl_list_retrieve_url_rules.xml

 -->

Alvorens de gevolgen van de regels aan klanten zichtbaar zijn, ben zeker u herbouwt uw plaatsindex.

De kruipende regels zijn het nuttigst om dynamische delen van een URL, zoals een zittingsherkenningsteken te herschrijven dat voor elke klant uniek is die uw website bezoekt. U kunt ook gebruiken herschrijft regels om gedeelten van een URL, zoals vraagparameters, van de onderzoeksrobot te verbergen. Door gebrek, worden geen regels gespecificeerd en geen URL wordt het herschrijven uitgevoerd.

Aangezien een website wordt gekropen, wordt ingebedde inhoud URLs opgeslagen in een tijdelijke lijst van extra Web-pagina&#39;s om te kruipen. Wanneer de onderzoeksrobot een URL van de lijst terugwint, wordt Win herschrijf Regels gebruikt om gedeelten van die URL te manipuleren. Typisch, wint regels terug worden gebruikt voor het opnemen van tijd-gevoelige gegevens in een URL. Het is deze definitieve URL die wordt gebruikt om de pagina van uw website eigenlijk terug te winnen.

Win herschrijf Regels terug zijn slechts noodzakelijk als URLs dynamische gegevens, zoals een zittingsidentiteitskaart bevat, en als die dynamische gegevens in tijd veranderen om geldig te blijven. In dit geval, gebruik u de Regels van de Rewrite van de Opslag om de meest recente staat van de gegevens van ontmoet URLs te krijgen. Dan, gebruikt u Win herschrijf Regels om die gegevens aan elke URL toe te voegen wanneer de onderzoeksrobots de pagina terugwint.

Elke regel wordt gespecificeerd met een herschrijf regel (RewriteRule) richtlijn en één of meerdere facultatieve herschrijf voorwaarden (RewriteCond). De volgorde van de regels is belangrijk. De regelreeks wordt van een lus voorzien door regel door. Wanneer een regel aanpast, het lijnen door om het even welke overeenkomstige herschrijft voorwaarden. Een kruipende regel URL wordt gespecificeerd op de volgende manier:

```
RewriteCond TestString CondPattern [Flags] 
RewriteRule Pattern Substitution [Flags]
```

Wanneer een ingebedde URL wordt ontmoet, probeert de onderzoeksrobot om URL aan het Patroon van elke kruipende regel aan te passen. Als de patroongelijken, herschrijft de motor overeenkomstige richtlijnen RewriteCond zoekt. Als geen voorwaarden aanwezig zijn, wordt URL gesubstitueerd met een nieuwe waarde die van het koord van de Vervanging wordt geconstrueerd en met de volgende regel in de regelreeks verdergaat. Indien de voorwaarden bestaan, worden zij verwerkt in de volgorde waarin zij worden vermeld. De herschrijf motor probeert om een voorwaardenpatroon (CondPattern) tegen een testkoord (TestString) aan te passen. Als de twee gelijke, dan wordt de volgende voorwaarde verwerkt tot geen meer voorwaarden beschikbaar zijn. Als alle voorwaarden aanpassen, wordt URL vervangen met de Vervanging die in de regel wordt gespecificeerd. Als niet aan de voorwaarde wordt voldaan, ontbreekt de volledige reeks voorwaarden en de overeenkomstige regel.

## Informatie over richtlijnen herschrijven {#section_32B24B29627946398AFBC5F869A610CB}

Een richtlijn RewriteRule heeft de volgende vorm:

```
           
<i>RewriteRule Pattern Substitution [Flags]</i> 
        
```

`Pattern` kan een POSIX regelmatige uitdrukking zijn, die wordt toegepast op huidige URL. De &quot;huidige URL&quot;kan van originele gevraagde URL verschillen, omdat de vroegere regels reeds URL kunnen hebben aangepast en veranderd.

Zie [Regelmatige expressies](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

U kunt niet het &quot;niet&quot;karakter (&quot;!&quot;) gebruiken om het patroon voor te bereiden. Het &quot;niet&quot;karakter laat u een patroon negeren, namelijk om waar te zijn slechts als huidige URL NIET dit patroon aanpast. Het &quot;niet&quot;karakter kan worden gebruikt wanneer het beter is om een negatief patroon aan te passen, of als definitieve standaardregel.

>[!NOTE]
>
>U kunt niet zowel het &quot;niet&quot;karakter als gegroepeerde vervangingen in een patroon gebruiken. Bovendien kunt u geen verwaarloosd patroon gebruiken wanneer het substitutiekoord $N bevat.

U kunt haakjes gebruiken om een backreference in het patroon tot stand te brengen, dat door de Substitutie en CondPattern kan worden van verwijzingen voorzien.

**Vervanging** URL wordt vervangen door het substitutiekoord, dat het volgende bevat:

Gewone tekst: Tekst die door onveranderd wordt overgegaan.

De verwijzingen van de achtergrond verlenen toegang tot de gegroepeerde delen (binnenhaakje) van het Patroon of CondPattern. Het volgende is de twee types van backreferences:

* **Achterverwijzingen** van RewriteRule Deze gelijke backreferences in het overeenkomstige Patroon RewriteRule en nemen de vorm $N (0 &lt;= N &lt;= 9). Bijvoorbeeld: `RewriteRule ^https:// ([^/]*) (.*)$ https://${tolower: $1} $2.`

* ** RewriteCond Backreferences** Deze gelijke backreferences in het laatst overeenkomende RewriteCond CondPattern en nemen de vorm %N (0 &lt;= N &lt;= 9).

Variabelen: Dit zijn variabelen van de vorm % {NAME_OF_VARIABLE} waar NAME_OF_VARIABLE een koord voor de naam van een bepaalde variabele is. Zie de vlag *[E]* voor meer informatie bij het plaatsen van milieuvariabelen.

Functies: Dit zijn functies van de vorm $ {NAME_OF_FUNCTION:key} waar NAME_OF_FUNCTION het volgende is:

* de aanjager maakt alle karakters in *zeer belangrijke* kleine letters.
* toupper maakt alle karakters in *zeer belangrijke* hoofdletters.
* vlucht URL-codeert alle karakters in *sleutel*.
* De tekens &#39;a&#39;...z&#39;, &#39;A&#39;...Z&#39;, &#39;0&#39;...9&#39;, &#39;*&#39;, &#39;-&#39;, &#39;.&#39;, &#39;/&#39;, &#39;@&#39; en &#39;_&#39; ongewijzigd blijven; de ruimten worden vertaald in &quot;+&quot;, en alle andere karakters worden omgezet in hun %xx URL-Gecodeerde equivalent.
* unescape zet &#39;+&#39; terug naar spatie en alle %xx URL-gecodeerde tekens terug naar enkele tekens.

>[!NOTE]
>
>Er is een speciale substitutiekoord: &quot;-&quot; dat betekent &quot;GEEN vervanging&quot;. Het &quot;-&quot;koord wordt vaak gebruikt met de vlag van C (ketting), latend u een URL aan verscheidene patronen aanpassen alvorens een substitutie voorkomt.

**Vlaggen**

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> "last|L" </p> </td> 
   <td colname="col2"> <p>Laatste regel. </p> <p>Houdt het herschrijvingsproces tegen en past geen extra herschrijvingsregels toe. Gebruik deze vlag om het even welke verdere verwerking aan huidige URL te verhinderen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'Volgende|N' </p> </td> 
   <td colname="col2"> <p>Volgende ronde. </p> <p> Reruns het het herschrijven proces (opnieuw beginnend met de eerste het herschrijven regel) gebruikend URL van de laatste het herschrijven regel (niet originele URL). Wees voorzichtig om geen dodlus te creëren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> "ketting|C" </p> </td> 
   <td colname="col2"> <p>Beeten met de volgende regel. </p> <p>Ketst de huidige regel aan de volgende regel (die ook aan zijn volgende regel kan worden geketend, etc.). Als een regel aanpast, dan gaat het substitutieproces zoals gebruikelijk verder. Als de regel niet aanpast, dan worden alle verdere geketende regels overgeslagen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> "no case|NC" </p> </td> 
   <td colname="col2"> <p>Geen zaak. </p> <p> Maakt het Patroon niet gevoelig geval (namelijk is er geen verschil tussen "A-Z"en "a-z") wanneer het patroon tegen huidige URL wordt aangepast. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> "skip|S=num" </p> </td> 
   <td colname="col2"> <p>Sla de volgende regel of regels over. </p> <p> Als de huidige regel aanpast, dwingt deze vlag de herschrijfmotor om de volgende numregels in de regelreeks over te slaan. Gebruik deze vlag om pseudo te maken als-dan-else concepten. De laatste regel van de toen-clausule wordt een skip=N waar N het aantal regels in de anders-clausule is. </p> <p> <p>Opmerking:  Deze vlag is niet hetzelfde als de 'chain|C' vlag!) </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> "env|E=VAR:VAL" </p> </td> 
   <td colname="col2"> <p>Plaatst de milieuvariabele. </p> <p>Creeert een milieuvariabele "VAR"die aan de waarde VAL wordt geplaatst, waar VAL regelmatige uitdrukkingsbackreferences, $N en %N kan bevatten, die worden uitgebreid. U kunt deze vlag meer dan eens gebruiken om veelvoudige variabelen te plaatsen. De variabelen kunnen later worden van verwijzingen voorzien in een volgend patroon RewriteCond via % {VAR}. </p> <p>Gebruik deze vlag om informatie van URLs te ontdoen en te herinneren. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>De opslag herschrijft Regels en Win herschrijft Regels herschrijft delen veranderlijke waarden. Wegens dit gedrag, kunt u een variabele aan een time-sensitive zittingswaarde plaatsen wanneer ingebedde URL wordt ontmoet en opgeslagen. Wanneer volgende URL van de tijdelijke opslaglijst wordt teruggewonnen, kan de recentste sessionid waarde aan het worden toegevoegd alvorens die pagina wordt teruggewonnen.

**Voorbeeld van een RewriteRule met een functie**

Veronderstel dat u een case-sensitive server hebt, die de koorden &quot;www.mydomain.com&quot;en &quot;www.MyDomain.com&quot;verschillend behandelt. Opdat uw server correct werkt, zorg ervoor dat het domein altijd &quot;www.mydomain.com&quot;is alhoewel sommige documenten verbindingen bevatten die &quot;www.MyDomain.com van verwijzingen voorzien.&quot; Om dit te doen, kon u de volgende regel gebruiken:

```
RewriteRule  ^https:// 
<b>([^/]*)</b> 
<i>(.*)</i>$  https://${tolower:$1}$2
```

Deze herschrijf regel gebruikt de functie `tolower` om het domeingedeelte van een URL te herschrijven om ervoor te zorgen dat het altijd in kleine letters zoals in het volgende is:

1. Het patroon `(^https://([^/]*)(.*)$)` bevat een backreference ** `([^/]*)`** die alle karakters tussen `https://` en de eerste `/` in URL aanpast. Het patroon bevat ook een tweede backreference `(.*)` die alle resterende karakters in URL aanpast.
1. De vervanging `(https://${tolower:$1}$2)` vertelt de onderzoeksmotor om URL te herschrijven door de `tolower` functie op de eerste backreference te gebruiken `(https:// ${tolower:$1}$2)` verlatend de rest van URL onaangetast `(https://${tolower:$1} $2)`.

Aldus, `https://www.MyDomain.com/INTRO/index.Html` wordt een URL van de vorm herschreven zoals `https://www.mydomain.com/INTRO/index.Html`.

## Informatie over richtlijnen herschrijvenCond {#section_ADD642A24B68452CB98294A0BD687EC3}

De richtlijn RewriteCond bepaalt een regelvoorwaarde. Wanneer een RewriteCond een RewriteRule voorafgaat, wordt de regel slechts gebruikt als zijn patroon de huidige titel aanpast en de extra voorwaarden van toepassing zijn. De herschrijvingsvoorwaarden nemen de volgende vorm aan:

```
           
<i>RewriteCond TestString CondPattern [Flags]</i> 
        
```

`TestString` is een koord dat de volgende concepten kan bevatten:

Gewone tekst: Tekst die door onveranderd wordt overgegaan.

De verwijzingen van de achtergrond verlenen toegang tot de gegroepeerde delen (binnenhaakje) van het Patroon of CondPattern. Het volgende is de twee types van backreferences:

* **Achterverwijzingen** van RewriteRule Deze gelijke backreferences in het overeenkomstige Patroon RewriteRule en nemen de vorm $N (0 &lt;= N &lt;= 9). Bijvoorbeeld, `RewriteRule ^https:// ([^/]*) (.*)$ https://${tolower: $1} $2`.

* **HerwriteCond Backreferences** Deze gelijke backreferences in het laatst overeenkomende RewriteCond CondPattern en nemen de vorm %N (0&lt;= N &lt;= 9).

Variabelen: Dit zijn variabelen van de vorm % {NAME_OF_VARIABLE} waar NAME_OF_VARIABLE een koord voor de naam van een bepaalde variabele kan zijn. Zie de RewriteRule vlag voor meer informatie bij het plaatsen van variabelen *`[E]`* .

Functies: Dit zijn functies van de vorm $ {NAME_OF_FUNCTION:key} waar NAME_OF_FUNCTION het volgende is:

* de aanjager maakt alle karakters in *zeer belangrijke* kleine letters.
* toupper maakt alle karakters in *zeer belangrijke* hoofdletters.
* vlucht URL-codeert alle karakters in sleutel. De tekens &#39;a&#39;...z&#39;, &#39;A&#39;...Z&#39;, &#39;0&#39;...9&#39;, &#39;*&#39;, &#39;-&#39;, &#39;.&#39;, &#39;/&#39;, &#39;@&#39;, en &#39;_&#39; worden ongewijzigd gelaten, worden de ruimten vertaald in &#39;+&#39;, en alle andere karakters worden omgezet in hun %xx URL-Gecodeerde equivalent.
* unescape zet &#39;+&#39; terug naar spatie om en alle %xx URL codekarakters terug naar enkele karakters.

**CondPattern** is een standaard Uitgebreide Regelmatige Uitdrukking met sommige toevoegingen. Het patroonkoord kan met een &quot;!&quot; vooraf worden bevestigd karakter (uitroepteken) om een niet-aanpassingspatroon te specificeren. In plaats van echte regelmatige uitdrukkingskoorden, kunt u één van de volgende speciale varianten gebruiken:

>[!NOTE]
>
>U kunt al deze tests met een uitroepteken (&#39;!&#39;) ook voorschrijven om hun betekenis te negeren.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CondPattern-tekenreeks </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> '&lt;CondPattern' </p> </td> 
   <td colname="col2"> <p>Lexisch minder. </p> <p> Behandelt CondPattern als duidelijk koord en vergelijkt het lexically bij TestString. Waar als TestString lexisch minder dan CondPattern is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '&gt;CondPattern' </p> </td> 
   <td colname="col2"> <p>Lexisch groter. </p> <p> Behandelt CondPattern als duidelijk koord en vergelijkt het lexically bij TestString. Waar als TestString lexisch groter is dan CondPattern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '=CondPattern' </p> </td> 
   <td colname="col2"> <p>Lexisch gelijk. </p> <p> Behandelt CondPattern als duidelijk koord en vergelijkt het lexically bij TestString. Waar als TestString lexisch gelijk aan CondPattern is, d.w.z., zijn de twee koorden precies gelijk (karakter door karakter). Als CondPattern enkel ""(twee aanhalingstekens) is, vergelijkt dit TestString met het lege koord. </p> </td> 
  </tr> 
 </tbody> 
</table>

**De vlaggen**(facultatief) sluiten vlaggen in steunen in `[]`. De veelvoudige vlaggen zijn komma-gescheiden.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> "no case|NC" </p> </td> 
   <td colname="col2"> <p> Geen zaak. </p> <p>Deze vlag maakt de test niet gevoelig geval, d.w.z., is er geen verschil tussen "A-Z"en "a-z"zowel in uitgebreide TestString als in CondPattern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> "ornext|OR" </p> </td> 
   <td colname="col2"> <p>Of de volgende voorwaarde. </p> <p>Gebruik deze vlag om regelvoorwaarden met lokaal OF in plaats van impliciet te combineren EN. Zonder deze vlag, zou u de voorwaarde/de regel veelvoudige tijden moeten schrijven. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Voorbeeld**

Sommige Web-pagina&#39;s wijzen een &quot;sessionid&quot;variabele van CGI toe de eerste keer een bezoeker bij een plaats aankomt. Deze variabele wordt gebruikt om de bezoeker te identificeren en, aangezien de bezoeker door de plaats doorbladert, wordt de variabele overgegaan langs. Omdat de zoekrobot lijkt op een bezoeker van je site, krijgt hij een sessionid-nummer toegewezen. De onderzoeksrobot handhaaft deze enige &quot;sessionid&quot;waarde, zelfs als een tweede plaatspagina probeert om een nieuwe waarde toe te wijzen. Om dit te verzekeren, hebt u twee herschrijvingsregels nodig.

De eerste regel wordt gebruikt om de sessionid variabele te identificeren en op te slaan:

```
RewriteCond  %{sessionid}  !.+ 
RewriteRule  ^.+sessionid= 
<b>([^&#]+)</b>.*$  -   
<i>[E=sessionid:$1]</i>
```

RewriteRule gebruikt een e-vlag `([E=sessionid:$1])` om de huidige waarde van de sessionid parameter van CGI aan de variabele toe te wijzen `sessionid`. De `$1` verwijzing verwijst naar de eerste backreference, die tussen de eerste reeks haakjes in het Patroon van RewriteRule bevat is `([^&#]+)`.

De regelmatige uitdrukking `^&#]+` past het gedeelte van een URL tussen het woord `sessionid` en volgende**&amp;**of**#**karakter aan. Aangezien dit RewriteRule slechts wordt gebruikt om de aanvankelijke waarde voor de sessionid variabele tot stand te brengen, herschrijft het niet. Merk op dat het gebied van de Substitutie van de regel aan `-` om wordt geplaatst te wijzen op dat geen het herschrijven wordt vereist.

RewriteCond onderzoekt de variabele `sessionid` ( `%{sessionid}`). Als het zelfs geen enkel karakter heeft (!..+), dan de gelijken RewriteRule.

Gebruikend deze regel, wordt URL gelezen als `https://www.domain.com/home/?sessionid=1234&function=start` en wijs de waarde `1234` aan de variabele toe `sessionid`.

De tweede regel wordt gebruikt om al URLs te herschrijven die het volgende Patroon RewriteRule aanpassen:

```
RewriteRule   
<b>^(.+)</b>sessionid=[^&#]+ 
<i>(.*)$</i>  $1sessionid=%{sessionid}$2
```

Het patroon RewriteRule bevat twee backreferences: `(.+)` en `(.*)`. De eerste backreference past alle karakters vóór aan `sessionid`. De tweede backreference past alle karakters na het eindigen aan `&` of `#`.

Het patroon van de Vervanging herschrijft URL gebruikend de eerste backreference, die door het koord &quot;sessionid=&quot;wordt gevolgd, die door de waarde van de variabele van zittingsidentiteitskaart door de eerste regel wordt bepaald, die door de tweede backreference wordt gevolgd `%{sessionid}`die. `($1sessionid=%{sessionid} $2)`

Bericht dat dit RewriteRule geen RewriteCond bevat. Als dusdanig, veroorzaakt het herschrijven voor al URLs die het *Patroon* RewriteRule aanpassen. Aldus, als de waarde van de sessionid variabele ( `%{sessionid}`) is `1234`, `https://www.domain.com/products/?sessionid=5678&function=buy` wordt een URL van de vorm herschreven zoals `https://www.domain.com/products/?sessionid=1234&function=buy`

## Erkenning {#section_EC3A1DAEB5A54C93A265CB119DF91E9F}

De software van de herschrijfmachine werd oorspronkelijk ontwikkeld door de Groep van Apache voor gebruik in het de serverproject van HTTP van Apache (https://www.apache.org/).

## Het toevoegen kruipt lijst wint URL regels terug {#task_94A28ED7DC404BFF9767DBB5ADEE6B7A}

U kunt toevoegen kruipt lijst terugwint regels URL om te specificeren hoe ontmoet URLs binnen Webinhoud wordt herschreven. Win herschrijf Regels terug zijn slechts noodzakelijk als URLs dynamische gegevens, zoals een zittingsidentiteitskaart bevat, en als die dynamische gegevens in tijd veranderen om geldig te blijven.

<!-- 

t_adding_crawl_list_retrieve_url_rules.xml

 -->

**Om toe te voegen kruipt de lijst URL regels terug wint**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Rewrite Rules]** > **[!UICONTROL Crawl List Retrieve URL Rules]**.
1. Op het [!DNL Crawl List Retrieve URL Rules] gebied, ga de regels in die u wilt.

   De lege lijnen en de commentaarlijnen die met een karakter &quot;#&quot;beginnen (knoeiboel) worden toegelaten.
1. (Facultatief) op de [!DNL Crawl List Retrieve URL Rules] pagina, op het [!DNL Test Crawl List Retrieve URL Rules] gebied, ga een test URL in waarvan kruipt regels u, dan **Test** testen en wilt klikken.
1. Klik **sparen Veranderingen**.
1. (Facultatief) herbouw uw gefaseerde plaatsindex als u aan voorproef de resultaten wilt.

   Zie [het Vormen van een stijgende index van een gefaseerde website](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Facultatief) op de [!DNL Crawl List Retrieve URL Rules] pagina, doe om het even welke volgend:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Informatie over regels voor overschrijdingen {#concept_BD3A576987DA4D93A998B0B9CDDC3C79}

Kruip de Regels van de Titel specificeren hoe de ontmoet titels binnen de inhoud van het Web worden herschreven alvorens zij in de onderzoeksindex worden opgeslagen.

<!-- 

c_about_crawl_title_rules.xml

 -->

Bijvoorbeeld, kunt u gebruiken herschrijft regel om een gedeelte van een titel zoals een organisatienaam te verwijderen. Aangezien een website wordt gekropen, worden de ontmoet titels opgeslagen in een tijdelijke buffer. Nochtans, alvorens een titel aan deze buffer wordt toegevoegd, worden de titelregels toegepast op het. Door gebrek, heeft het plaatsonderzoek/de merchandising geen kruipende titelregels en maakt geen titelwijzigingen.

Alvorens de gevolgen van de regels aan klanten zichtbaar zijn, herbouw uw plaatsindex.

U kunt om het even welke veranderingen snel terugkeren u aanbrengt om de Regels van de Titel te kruipen door de eigenschap van de Geschiedenis te gebruiken.

De regels kunnen uit twee hoofdelementen bestaan: HerwriteRule en facultatieve RewriteCond. U kunt een onbeperkt aantal regels en voorwaarden specificeren. De orde van deze regels is belangrijk omdat de geplaatste regel door regel door van een lus wordt voorzien. Wanneer een regel aanpast, het lijnen door om het even welke (facultatieve) overeenkomstige herschrijft voorwaarden. Kruip de regels URL worden gespecificeerd op de volgende manier:

```
RewriteCond  
<i>TestString CondPattern [Flags]</i> 
RewriteRule  
<i>Pattern Substitution [Flags]</i> 
 
RewriteCond  
<i>TestString CondPattern [Flags]</i> 
RewriteRule  
<i>Pattern Substitution [Flags]</i>
```

Wanneer een titel wordt ontmoet, probeert de onderzoeksrobot om de titel aan het Patroon van elke kruipende regel aan te passen. Als de patroongelijken, herschrijft de motor overeenkomstige richtlijnen RewriteCond zoekt. Als geen voorwaarden aanwezig zijn, wordt URL gesubstitueerd met een nieuwe waarde die van het koord van de Vervanging wordt geconstrueerd en met de volgende regel in de regelreeks verdergaat. Indien de voorwaarden bestaan, worden zij verwerkt in de volgorde waarin zij worden vermeld. De herschrijf motor probeert om een voorwaardenpatroon (CondPattern) tegen een testkoord (TestString) aan te passen. Als de twee gelijke, dan wordt de volgende voorwaarde verwerkt tot geen meer voorwaarden beschikbaar zijn. Als alle voorwaarden aanpassen, wordt URL vervangen met de Vervanging die in de regel wordt gespecificeerd. Als niet aan de voorwaarde wordt voldaan, ontbreekt de volledige reeks voorwaarden en de overeenkomstige regel.

Ga de Crawl URL Regels in het tekstvakje in, en klik dan sparen Veranderingen. De lege lijnen en de commentaarlijnen die met een karakter &quot;#&quot;beginnen (knoeiboel) worden toegelaten. Om de onderzoeksregels te testen, kunt u een test URL in het de tekstvakje van de &quot;Test ingaan herschrijft Regels&quot;, en klikt dan Test.

## HerschrijvenRegel richtlijn {#section_669445C505754E838E14029D6583D9B6}

Elke richtlijn RewriteRule bepaalt één het herschrijven regel. De regels worden toegepast in de volgorde waarin zij worden vermeld. Een herschrijfregel neemt de volgende vorm aan:

```
RewriteRule Pattern Substitution [Flags]
```

**Het patroon** kan een regelmatige uitdrukking van POSIX zijn, die op de huidige titel wordt toegepast. De &quot;huidige titel&quot; verschilt van de oorspronkelijke titel, omdat eerdere regels al aangepast en gewijzigd zijn.

Zie [Regelmatige expressies](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

U kunt het &quot;niet&quot;karakter (&quot;!&quot;) gebruiken om het patroon voor te bereiden. Het &quot;niet&quot;karakter staat u toe om een patroon te negeren, namelijk om waar te zijn slechts als de huidige titel NIET het patroon aanpast. Het &quot;niet&quot;karakter kan worden gebruikt wanneer het beter is om een negatief patroon aan te passen, of als definitieve standaardregel. Opmerking: U kunt niet zowel het &quot;niet&quot;karakter als gegroepeerde vervangingen in een patroon gebruiken. Bovendien kunt u geen verwaarloosd patroon gebruiken wanneer het substitutiekoord $N bevat.

U kunt haakjes gebruiken om een backreference tot stand te brengen, die door de Vervanging en CondPattern kan worden van verwijzingen voorzien.

**Substitutie** De titel wordt vervangen door de substitutiereeks. Het koord kan het volgende bevatten:

Gewone tekst - Tekst die door onveranderd wordt overgegaan.

De verwijzingen van de achtergrond verlenen toegang tot de gegroepeerde delen (binnenhaakje) van het Patroon of CondPattern. Het volgende is twee types van backreferences:

* Achterreferenties herschrijvenRegel

   Deze gelijke backreferences in het overeenkomstige Patroon RewriteRule en nemen de vorm $N (0 &lt;= N &lt;= 9). Bijvoorbeeld: `RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`
* Achterreferenties herschrijvenCond

   Deze gelijke backreferences in laatste overeenkomende RewriteCond CondPattern en nemen de vorm %N (0 &lt;= N &lt;= 9).

Variabelen Dit zijn variabelen van de vorm % {NAME_OF_VARIABLE} waar NAME_OF_VARIABLE een koord voor de naam van een bepaalde variabele kan zijn. Zie de `[E]` vlag voor meer informatie bij het plaatsen van milieuvariabelen.

Functies Dit zijn functies van de vorm $ {NAME_OF_FUNCTION: key} waar NAME_OF_FUNCTION is:

* de aanjager maakt alle karakters in *zeer belangrijke* kleine letters.
* toupper maakt alle karakters in *zeer belangrijke* hoofdletters.

>[!NOTE]
>
>Er is een speciale substitutiekoord: &quot;-&quot; dat betekent &quot;GEEN vervanging&quot;. Het &quot;-&quot;koord is vaak nuttig met de vlag van C (ketting), toestaand u om een titel aan verscheidene patronen aan te passen alvorens een substitutie voorkomt.

**Vlaggen** (facultatief)

De vlaggen zijn ingesloten tussen haakjes `[]`en de veelvoudige vlaggen zijn komma-gescheiden:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> "last|L" </p> </td> 
   <td colname="col2"> <p>Laatste regel. </p> <p> Houdt het herschrijfproces tegen en past geen extra herschrijvingsregels toe. Gebruik deze vlag om het even welke verdere verwerking aan de huidige titel te verhinderen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'Volgende|N' </p> </td> 
   <td colname="col2"> <p>Volgende ronde. </p> <p> Reruns het herschrijvingsproces (opnieuw beginnend met de eerste het herschrijven regel) gebruikend de titel van de laatste het herschrijven regel, niet de originele titel. Wees voorzichtig om geen dode lus te creëren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> "ketting|C" </p> </td> 
   <td colname="col2"> <p>Beeten met de volgende regel. </p> <p>Ketst de huidige regel aan de volgende regel (die ook aan zijn volgende regel kan worden geketend, etc.). Als een regel aanpast, dan gaat het substitutieproces zoals gebruikelijk verder. Als de regel niet aanpast, dan worden alle verdere geketende regels overgeslagen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> "no case|NC" </p> </td> 
   <td colname="col2"> <p>Geen zaak. </p> <p>Maakt het Patroon niet gevoelig geval (namelijk is er geen verschil tussen "A-Z"en "a-z") wanneer het patroon tegen de huidige titel wordt aangepast. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> "skip|S=num" </p> </td> 
   <td colname="col2"> <p>Sla volgende regel of regels over. </p> <p> Als de huidige regel aanpast, dwingt deze vlag de herschrijfmotor om de volgende numregels in de regelreeks over te slaan. Gebruik dit om pseudo als-dan-anders concepten te maken. De laatste regel van de toen-clausule wordt een skip=N waar N het aantal regels in de anders-clausule is. (Opmerking: Dit is niet het zelfde als de "ketting|C"vlag!) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> "env|E=VAR:VAL" </p> </td> 
   <td colname="col2"> <p>Stel de omgevingsvariabele in. </p> <p> Creeert een milieuvariabele "VAR"die aan de waarde VAL wordt geplaatst, waar VAL regelmatige uitdrukkingsbackreferences, $N en %N kan bevatten, die wordt uitgebreid. U kunt deze vlag meer dan eens gebruiken om veelvoudige variabelen te plaatsen. De variabelen kunnen later in een volgend patroon RewriteCond via % {VAR} worden van verwijzingen voorzien. Gebruik deze vlag om informatie van titels te ontdoen en te herinneren. </p> </td> 
  </tr> 
 </tbody> 
</table>

## HerschrijvenCond-richtlijn (optioneel) {#section_D664B71DE3884E0790531804C49A3222}

De richtlijn RewriteCond bepaalt een regelvoorwaarde. Wanneer een RewriteCond een RewriteRule voorafgaat, wordt de regel slechts gebruikt als zijn patroon de huidige titel aanpast en de extra voorwaarden van toepassing zijn.

De richtlijnen van de herschrijvingsvoorwaarde nemen de volgende vorm aan:

```
RewriteCond TestString CondPattern [Flags] 
```

**TestString** is een koord dat de volgende concepten kan bevatten:

Gewone tekst - Tekst die door onveranderd wordt overgegaan.

De verwijzingen van de achtergrond verlenen toegang tot de gegroepeerde delen (binnenhaakje) van het Patroon of CondPattern. Er zijn twee types van backreferences:

* RewriteRule Backreferences Deze gelijke backreferences in het overeenkomstige Patroon RewriteRule en nemen de vorm $N (0 &lt;= N &lt;= 9). Bijvoorbeeld: `RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`
* Achterverwijzingen herschrijvenCond Deze gelijke backreferences in laatste overeenkomende RewriteCond CondPattern en nemen de vorm %N (0 &lt;= N &lt;= 9).

Variabelen Dit zijn variabelen van de vorm % {NAME_OF_VARIABLE} waar NAME_OF_VARIABLE een koord voor de naam van een bepaalde variabele kan zijn. Zie de `[E]` vlag voor meer informatie bij het plaatsen van milieuvariabelen.

Functies Dit zijn functies van de vorm $ {NAME_OF_FUNCTION:key} waar NAME_OF_FUNCTION is:

* de aanjager maakt alle karakters in *zeer belangrijke* kleine letters.
* toupper maakt alle karakters in *zeer belangrijke* hoofdletters.
* vlucht URL-codeert alle karakters in sleutel.
* De tekens &#39;a&#39;...z&#39;, &#39;A&#39;...Z&#39;, &#39;0&#39;...9&#39;, &#39;*&#39;, &#39;-&#39;, &#39;.&#39;, &#39;/&#39;, &#39;@&#39;, en &#39;_&#39; worden ongewijzigd gelaten, worden de ruimten vertaald in &#39;+&#39;, en alle andere karakters worden omgezet in hun %xx URL-Gecodeerde equivalent.
* unescape zet &#39;+&#39; terug naar spatie en alle %xx URL-gecodeerde tekens terug naar enkele tekens.

**CondPattern** is een standaard Uitgebreide Regelmatige Uitdrukking met sommige toevoegingen. Het patroonkoord kan met een &quot;!&quot; vooraf worden bevestigd karakter (uitroepteken) om een niet-aanpassingspatroon te specificeren. In plaats van echte regelmatige uitdrukkingskoorden, kunt u één van de volgende speciale varianten gebruiken.

>[!NOTE]
>
>U kunt al deze tests met een uitroepteken (&#39;!&#39;) voorschrijven om hun betekenis te negeren.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CondPattern-tekenreeks </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> '&lt;CondPattern' </p> </td> 
   <td colname="col2"> <p>Is lexicaal minder. </p> <p>Behandelt <i>CondPattern</i> als duidelijk koord en vergelijkt het lexically met <i>TestString</i>. Waar als <i>TestString</i> lexically minder dan <i>CondPattern</i>is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '&gt;CondPattern' </p> </td> 
   <td colname="col2"> <p>Is lexicaal groter. </p> <p>Behandelt <i>CondPattern</i> als duidelijk koord en vergelijkt het lexically met <i>TestString</i>. Waar als <i>TestString</i> lexically groter is dan <i>CondPattern</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '=CondPattern' </p> </td> 
   <td colname="col2"> <p> Is lexicaal gelijk. </p> <p>Behandelt <i>CondPattern</i> als duidelijk koord en vergelijkt het lexically met <i>TestString</i>. Waar als <i>TestString</i> lexisch gelijk aan <i>CondPattern</i>is, d.w.z., zijn de twee koorden precies gelijk (karakter door karakter). Als <i>CondPattern</i> enkel ""(twee aanhalingstekens) is, vergelijkt dit <i>TestString</i> bij het lege koord. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Vlaggen** (facultatief)

De vlaggen zijn ingesloten tussen haakjes `[]`en de veelvoudige vlaggen zijn komma-gescheiden:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> "no case|NC" </p> </td> 
   <td colname="col2"> <p>Geen zaak. </p> <p> Maakt de test niet gevoelig. Namelijk is er geen verschil tussen "A-Z"en "a-z"zowel in uitgebreide <i>TestString</i> als in <i>CondPattern.</i> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> "ornext|OR" </p> </td> 
   <td colname="col2"> <p> Of de volgende voorwaarde. </p> <p>Gebruik deze vlag om regelvoorwaarden met lokaal OF in plaats van impliciet te combineren EN. Zonder deze vlag, zou u de voorwaarde/de regel veelvoudige tijden moeten schrijven. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Voorbeeld**

Veronderstel dat u een collectieve Website met een standaardtitelformaat hebt: &quot;Mijn Bedrijf&quot;gevolgd door een koppelteken en toen een pagina-specifieke beschrijving (&quot;Mijn Bedrijf - Onthaal&quot;of &quot;Mijn Bedrijf - Nieuws&quot;, bijvoorbeeld). U wilt &quot;Mijn Bedrijf -&quot;van de titel ontdoen en de volledige titel in hoofdletters omzetten wanneer het de plaats indexeert.

De volgende herschrijf regel gebruikt de functietrapper om slechts het beschrijvende gedeelte van een titel in hoofdletters te herschrijven:

```
RewriteRule  ^My[[:blank:]]Company[[:blank:]]-[[:blank:]] 
<b>(.*)</b>$  ${toupper: 
<b>$1</b>}
```

Het patroon van de regel `(^My[[:blank:]]Company[[:blank:]]-[[:blank:]] (.*))` bevat een backreference `(.*)` die de titelinhoud aanpast die &quot;Mijn Bedrijf-&quot;volgt. Herinner dat het omringen van een gedeelte van een patroon met haakje () tot een backreference leidt die door de Substitutie kan worden van verwijzingen voorzien. In dit voorbeeld, herschrijft de Vervanging ($ {toupper:**$1**}) die backreference (**$1**) gebruikend de toupperfunctie.

Aldus, wordt een titel van het formulier &quot;Mijn Bedrijf - Onthaal&quot;herschreven als &quot;WELKOM&quot;.

**Erkenning**

De software van de herschrijfmachine werd oorspronkelijk ontwikkeld door de Groep van Apache voor gebruik in het de serverproject van HTTP van Apache (https://www.apache.org/).

## Het toevoegen kruipt titelregels kruipt {#task_272BB4C603BA4C9ABDBEEB398798B101}

U kunt toevoegen kruipt titelregels om te specificeren hoe de ontmoete titels binnen de Webinhoud worden herschreven alvorens zij in de onderzoeksindex worden opgeslagen.

<!-- 

t_adding_crawl_title_rules.xml

 -->

**Om toe te voegen kruipt titelregels**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Rewrite Rules]** > **[!UICONTROL Crawl Title Rules]**.
1. Op het [!DNL Crawl Title Rules] gebied, ga de regels in die u wilt.

   De lege lijnen en de commentaarlijnen die met een karakter &quot;#&quot;beginnen (knoeiboel) worden toegelaten.
1. (Facultatief) op de [!DNL Crawl Title Rules] pagina, op het [!DNL Test Crawl Title Rules] gebied, ga een test URL in waarvan onderzoeksregels u, dan **Test** testen en wilt klikken.
1. Klik **sparen Veranderingen**.
1. (Facultatief) herbouw uw gefaseerde plaatsindex als u aan voorproef de resultaten wilt.

   Zie [het Vormen van een stijgende index van een gefaseerde website](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Facultatief) op de [!DNL Crawl Title Rules] pagina, doe om het even welke volgend:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Informatie over URL-regels zoeken {#concept_017EC95E68844B6C8CC9F874F0EC8D3C}

De Regels van het onderzoek URL specificeren hoe URLs in uw Website onderzoeksresultaten zou moeten tonen. De regels werken op volledige URLs. Om het even welk gedeelte van URL kan worden gemanipuleerd, met inbegrip van vraagargumenten waar de informatie van zittingsidentiteitskaart vaak wordt gehouden.

<!-- 

c_about_search_url_rules.xml

 -->

Typisch, onderzoek worden de regels URL gebruikt om een zittingsidentiteitskaart in een URL op te nemen. Nochtans, kunt u onderzoekURL regels ook gebruiken om de domeinnaam te veranderen die met uw resultaten wordt getoond. Door gebrek, worden geen regels gespecificeerd en geen wijziging URL wordt uitgevoerd.

De regels van het onderzoek URL kunnen uit twee belangrijke elementen bestaan: HerwriteRule en facultatieve RewriteCond. Wanneer een URL als deel van een onderzoeksresultaat inbegrepen is, worden de regels gebruikt om het te manipuleren. U kunt een onbeperkt aantal van onderzoekURL regels en voorwaarden specificeren. De orde van deze regels is belangrijk omdat de geplaatste regel door regel-door-regel van een lus wordt voorzien. Wanneer een regel aanpast, de softwarelijnen door om het even welke (facultatieve) overeenkomstige herschrijf voorwaarden. Kruip de regels URL worden gespecificeerd op de volgende manier:

```
RewriteCond  
<i>TestString CondPattern [Flags]</i> 
RewriteRule  
<i>Pattern Substitution [Flags]</i> 
 
RewriteCond  
<i>TestString CondPattern [Flags]</i> 
RewriteRule  
<i>Pattern Substitution [Flags]</i>
```

Wanneer het verwerken van een URL, probeert het plaatsonderzoek/de merchandising om het aan het Patroon van elke onderzoeksregel aan te passen. Als de gelijke ontbreekt, herschrijf de motor onmiddellijk ophoudt verwerkend de regel en gaat met de volgende regel in de reeks verder. Als de patroon aanpast, zoekt de herschrijfmotor overeenkomstige RewriteCond instructies. Als geen voorwaarden bestaan, wordt URL gesubstitueerd met een nieuwe waarde. Deze waarde wordt geconstrueerd van het koord van de Substitutie en gaat met de volgende regel in de regelreeks verder. Als de voorwaarden bestaan, is de orde dat zij vermeld zijn hoe zij worden verwerkt. De herschrijf motor probeert om een voorwaardenpatroon (CondPattern) tegen een testkoord (TestString) aan te passen. Als de twee gelijke, dan wordt de volgende voorwaarde verwerkt tot geen meer voorwaarden beschikbaar zijn. Als alle voorwaarden aanpassen, wordt URL vervangen met de Vervanging die in de regel wordt gespecificeerd. Als niet aan de voorwaarde wordt voldaan, ontbreekt de volledige reeks voorwaarden en de overeenkomstige regel.

## Informatie over RewriteRule-richtlijn {#section_A3473B5B90B74DA1970213113A90591E}

Een herschrijfregel neemt de volgende vorm aan:

```
RewriteRule  
<i>Pattern Substitution [Flags]</i>
```

**Het patroon** kan een regelmatige uitdrukking van POSIX zijn, die wordt toegepast op huidige URL. De &quot;huidige URL&quot;kan van originele URL verschillen, omdat de vroegere regels het kunnen reeds aangepast en veranderd hebben.

Zie [Regelmatige expressies](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

U kunt het &quot;niet&quot;karakter (&quot;!&quot;) gebruiken om het patroon voor te bereiden. Het &quot;niet&quot;karakter laat u een patroon negeren. Met andere woorden, is het waar slechts als huidige URL NIET het patroon aanpast. U kunt het &quot;niet&quot;karakter gebruiken wanneer het beter is om een negatief patroon aan te passen, of als definitieve standaardregel. Merk op dat u niet zowel het &quot;niet&quot;karakter als gegroepeerde vervangingen in een patroon kunt gebruiken. Bovendien kunt u geen verwaarloosd patroon gebruiken wanneer het substitutiekoord $N bevat.

U kunt haakjes gebruiken om een backreference tot stand te brengen, die door de Vervanging en CondPattern kan worden van verwijzingen voorzien.

**Vervanging** URL wordt volledig vervangen door het substitutiekoord, dat het volgende kan bevatten:

Gewone Tekst - Tekst die door onveranderd wordt overgegaan.

De verwijzingen van de achtergrond verlenen toegang tot de gegroepeerde delen (binnenhaakje) van het Patroon of CondPattern. Er zijn twee types van backreferences:

RewriteRule Backreferences Deze gelijke backreferences in het overeenkomstige Patroon RewriteRule en nemen de vorm $N (0 &lt;= N &lt;= 9). Bijvoorbeeld: `RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`

Achterverwijzingen herschrijvenCond - Deze gelijke backreferences in het laatst overeenkomende RewriteCond CondPattern en nemen de vorm %N (0 &lt;= N &lt;= 9).

Functies: Dit zijn functies van de vorm $ {NAME_OF_FUNCTION:key} waar NAME_OF_FUNCTION is:

* de aanjager maakt alle karakters in *zeer belangrijke* kleine letters.
* toupper maakt alle karakters in *zeer belangrijke* hoofdletters.
* vlucht URL-codeert alle karakters in *sleutel*.
* De tekens &#39;a&#39;...z&#39;, &#39;A&#39;...Z&#39;, &#39;0&#39;...9&#39;, &#39;*&#39;, &#39;-&#39;, &#39;.&#39;, &#39;/&#39;, &#39;@&#39; en &#39;_&#39; ongewijzigd blijven; de ruimten worden vertaald in &quot;+&quot;; alle andere karakters worden omgezet in hun %xx URL-Gecodeerde equivalent.
* unescape zet &#39;+&#39; terug naar spatie en alle %xx URL-gecodeerde tekens terug naar enkele tekens.

>[!NOTE]
>
>Er is een speciale substitutiekoord: &quot;-&quot; dat betekent &quot;GEEN vervanging&quot;. De &quot;-&quot;koord is vaak nuttig samen met de vlag van C (ketting). Het laat u een URL aan verscheidene patronen aanpassen alvorens een substitutie voorkomt.

**Vlaggen** (facultatief)

De vlaggen zijn ingesloten tussen haakjes `[]`en de veelvoudige vlaggen zijn komma-gescheiden:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> "last|L" </p> </td> 
   <td colname="col2"> <p>Laatste regel. </p> <p> Stop het herschrijvingsproces en pas geen extra herschrijvingsregels toe. Gebruik deze vlag om het even welke verdere verwerking aan huidige URL te verhinderen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'Volgende|N' </p> </td> 
   <td colname="col2"> <p> Volgende ronde. </p> <p>Voer het herschrijfproces (opnieuw beginnen met de eerste herschrijfregel) opnieuw uit met de URL van de laatste herschrijfregel (niet de originele URL). Wees voorzichtig om geen dode lus te creëren! </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> "ketting|C" </p> </td> 
   <td colname="col2"> <p> Beeten met de volgende regel. </p> <p>Deze vlag ketent de huidige regel aan de volgende regel, die ook aan zijn volgende regel kan worden geketend, enzovoort. Als een regel aanpast, dan gaat het substitutieproces zoals gebruikelijk verder. Als de regel niet aanpast, dan worden alle verdere geketende regels overgeslagen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> "no case|NC" </p> </td> 
   <td colname="col2"> <p>Geen zaak. </p> <p>Deze vlag maakt het Patroon case-insensitive. Met andere woorden, er is geen verschil tussen "A-Z"en "a-z"wanneer het patroon tegen huidige URL wordt aangepast. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> "skip|S=num" </p> </td> 
   <td colname="col2"> <p>Sla volgende regel of regels over. </p> <p> Als de huidige regel aanpast, dwingt deze vlag de herschrijfmotor om de volgende numregels in de regelreeks over te slaan. Gebruik dit om pseudo als-dan-anders concepten te maken. De laatste regel van de toen-clausule wordt een skip=N waar N het aantal regels in de anders-clausule is. (Opmerking: Dit is niet het zelfde als de "ketting|C"vlag!) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> "env|E=VAR:VAL" </p> </td> 
   <td colname="col2"> <p>Omgevingsvariabele instellen. </p> <p> Deze vlag leidt tot een milieuvariabele "VAR"die aan de waarde VAL wordt geplaatst. De VAL kan regelmatige uitdrukkingsbackreferences, $N en %N bevatten, die worden uitgebreid. U kunt deze vlag meer dan eens gebruiken om veelvoudige variabelen te plaatsen. De variabelen kunnen later worden van verwijzingen voorzien in een volgend patroon RewriteCond via % {VAR}. Gebruik deze vlag om informatie van URLs te ontdoen en te herinneren. </p> </td> 
  </tr> 
 </tbody> 
</table>

Merk op dat de Opslag Regels herschrijft en Win herschrijft Regels delen veranderlijke waarden herschrijft. Wegens dit, kunt u een variabele aan een time-sensitive zittingswaarde plaatsen wanneer ingebedde URL wordt ontmoet en opgeslagen. Wanneer volgende URL van de tijdelijke opslaglijst wordt teruggewonnen, kan de recentste sessionid waarde aan het worden toegevoegd alvorens die pagina wordt teruggewonnen.

**Voorbeeld**

Veronderstel dat u een case-sensitive server hebt. Het behandelt de koorden &quot;www.mydomain.com&quot;en &quot;www.MyDomain.com&quot;verschillend. Om uw serverwerk correct te hebben, moet u ervoor zorgen dat het domein altijd &quot;www.mydomain.com&quot;is alhoewel sommige documenten verbindingen bevatten die &quot;www.MyDomain.com&quot;van verwijzingen voorzien. Om dit te doen, kon u de volgende regel gebruiken:

```
RewriteRule  ^https:// 
<b>([^/]*)</b> 
<i>(.*)</i>$  https://${tolower:$1}$2 
```

Deze herschrijf regel gebruikt de functie &quot;tolower&quot;om het domeingedeelte van een URL te herschrijven om ervoor te zorgen dat het altijd in kleine letters is:

1. Het patroon `(^https://([^/]*)(.*)$)` bevat een backreference **`([^/]*)`** die alle karakters tussen &quot;https://&quot;en eerste &quot;/&quot;in URL aanpast. Het patroon bevat ook een tweede backreference **(.*)** dat alle resterende karakters in URL aanpast.

1. De substitutie `(https://${tolower:$1}$2)` vertelt de onderzoeksmotor om URL te herschrijven door de **tolower** functie op de eerste backreference te gebruiken `(https://**${tolower:$1**}$2)` verlatend de rest van URL onaangeroerd `(https://${tolower:$1}*$2*)`.

Daarom `https://www.MyDomain.com/INTRO/index.Html` wordt een URL van het formulier herschreven zoals `https://www.mydomain.com/INTRO/index.Html`

**HerschrijvenCond-richtlijn** (optioneel)

De richtlijn RewriteCond bepaalt een regelvoorwaarde. Wanneer een RewriteCond een RewriteRule voorafgaat, wordt de regel slechts gebruikt als zijn patroon de huidige titel aanpast en de extra voorwaarden van toepassing zijn.

De richtlijnen van de herschrijvingsvoorwaarde nemen de volgende vorm aan:

```
RewriteCond  
<i>TestString CondPattern [Flags]</i>
```

*TestString* is een koord dat de volgende concepten kan bevatten:

Gewone tekst: Tekst die door onveranderd wordt overgegaan.

De verwijzingen van de achtergrond verlenen toegang tot de gegroepeerde delen (binnenhaakje) van het Patroon of CondPattern. Er zijn twee types van backreferences:

* ** RewriteRule Backreferences** Deze gelijke backreferences in het overeenkomstige Patroon RewriteRule en nemen de vorm $N (0 &lt;= N &lt;= 9). Bijvoorbeeld: `RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`

* **HerwriteCond Backreferences** Deze gelijke backreferences in het laatst overeenkomende RewriteCond CondPattern en nemen de vorm %N (0 &lt;= N &lt;= 9).

Variabelen Dit zijn variabelen van de vorm % {NAME_OF_VARIABLE} waar NAME_OF_VARIABLE een koord voor de naam van een bepaalde variabele kan zijn. Zie de RewriteRule vlag voor meer informatie bij het plaatsen van variabelen *`[E]`* .

>[!NOTE]
>
>Herschrijf regels maken over het algemeen gebruik van variabelen. Alle parameters van CGI van huidige URL worden automatisch gemaakt in variabelen. Bijvoorbeeld, `"https://search.atomz.com/search/?sp_a=sp00000000&sp_q="Product"&session=1234&id=5678"` zal het onderzoek URL automatisch vier variabelen verstrekken, die in de herschrijfregels kunnen worden van verwijzingen voorzien. In dit voorbeeld, wordt één variabele genoemd &quot;zitting&quot;en zijn waarde is &quot;1234&quot;terwijl een andere variabele &quot;identiteitskaart&quot;wordt genoemd, en zijn waarde is &quot;5678.&quot; (De andere twee variabelen zijn `sp_a` en `sp_q`.) U zou alle noodzakelijke variabelen als verborgen gebieden van de onderzoeksvorm op uw Web-pagina moeten overgaan. In dit voorbeeld, zou u de &quot;zitting&quot;en &quot;identiteitskaart&quot;waarden moeten overgaan, die de gebruiker identificeren die van de Website het onderzoek uitvoert. Om een verborgen gebied op de onderzoeksvorm over te gaan, gebruik een markering als `<input type=hidden name="session" value="1234">`.

Functies Dit zijn functies van de vorm $ {NAME_OF_FUNCTION:key} waar NAME_OF_FUNCTION is:

* de aanjager maakt alle karakters in *zeer belangrijke* kleine letters.
* toupper maakt alle karakters in *zeer belangrijke* hoofdletters.
* vlucht URL-codeert alle karakters in *sleutel*. De tekens &#39;a&#39;...z&#39;, &#39;A&#39;...Z&#39;, &#39;0&#39;...9&#39;, &#39;*&#39;, &#39;-&#39;, &#39;.&#39;, &#39;/&#39;, &#39;@&#39;, en &#39;_&#39; worden ongewijzigd gelaten, worden de ruimten vertaald in &#39;+&#39;, en alle andere karakters worden omgezet in hun %xx URL-Gecodeerde equivalent.
* unescape zet &#39;+&#39; terug naar spatie om en alle %xx URL codekarakters terug naar enkele karakters.

**CondPattern** is een standaard Uitgebreide Regelmatige Uitdrukking met sommige toevoegingen. Het patroonkoord kan met een &quot;!&quot; vooraf worden bevestigd karakter (uitroepteken) om een niet-aanpassingspatroon te specificeren. In plaats van echte regelmatige uitdrukkingskoorden, kunt u één van de volgende speciale varianten gebruiken.

U kunt elk van deze tests door een uitroepteken (&#39;!&#39;) te gebruiken voorschrijven om hun betekenis te negeren.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CondPattern-tekenreeks </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> '&lt;CondPattern' </p> </td> 
   <td colname="col2"> <p>Is lexicaal minder. </p> <p> Behandelt <i>CondPattern</i> als duidelijk koord en vergelijkt het lexically met <i>TestString</i>. Waar als <i>TestString</i> lexically minder dan <i>CondPattern</i>is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '&gt;CondPattern' </p> </td> 
   <td colname="col2"> <p>Is lexicaal groter. </p> <p> Behandelt <i>CondPattern</i> als duidelijk koord en vergelijkt het lexically met <i>TestString</i>. Waar als <i>TestString</i> lexically groter is dan <i>CondPattern</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '=CondPattern' </p> </td> 
   <td colname="col2"> <p>Is lexicaal gelijk. </p> <p> Behandelt <i>CondPattern</i> als duidelijk koord en vergelijkt het lexically met <i>TestString</i>. Waar als <i>TestString</i> lexisch gelijk aan <i>CondPattern</i>is. Namelijk zijn de twee koorden precies gelijk (karakter door karakter). Als <i>CondPattern</i> enkel ""(twee aanhalingstekens) is, vergelijkt dit <i>TestString</i> bij het lege koord. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Vlaggen** (facultatief)

De vlaggen zijn ingesloten tussen haakjes `[]`en de veelvoudige vlaggen zijn komma-gescheiden:

&quot;geen geval|NC&quot; (geen geval): Dit maakt de testcase-insensitive. Met andere woorden, is er geen verschil tussen &quot;A-Z&quot;en &quot;a-z&quot;zowel in uitgebreide *TestString* als in *CondPattern*.

&#39;of volgende|OR&#39; (of volgende voorwaarde): Gebruik dit om regelvoorwaarden met lokaal OF in plaats van impliciet te combineren EN. Zonder deze vlag zou u de voorwaarde/de regel veelvoudige tijden moeten schrijven.

**Voorbeeld**

Sommige Web-pagina&#39;s wijzen een &quot;sessionid&quot;variabele van CGI toe de eerste keer een klant bij een plaats aankomt. Deze variabele wordt gebruikt om de klant te identificeren en, aangezien de klant door de plaats doorbladert, wordt de variabele overgegaan langs. Omdat de zoekrobot eruit ziet als een klant van je site, krijgt hij een sessionid-nummer toegewezen. De onderzoeksrobot handhaaft deze enige &quot;sessionid&quot;waarde, zelfs als een tweede plaatspagina probeert om een nieuwe waarde toe te wijzen. Om dit te verzekeren, hebt u de volgende herschrijfregel nodig:

```
RewriteCond  %{sessionid}  .+ 
RewriteRule  ^ 
<b>(.+)</b>sessionid=[^&#]+ 
<i>(.*)</i>$   
<b>$1</b>sessionid=%{sessionid} 
<i>$2</i>
```

Het patroon RewriteRule bevat twee backreferences: (...)+) en (..*). De eerste backreference past alle karakters vóór &quot;sessionid=&quot; aan. De tweede backreference past alle karakters na het eindigen &#39;&amp;&#39; of &#39;#&#39; van de sessionid aan.

Het patroon van de Vervanging herschrijft URL gebruikend de eerste backreference, die door het koord &quot;sessionid=&quot;wordt gevolgd, die door de waarde van de variabele van zittingsidentiteitskaart wordt gevolgd, die als parameter van CGI in URL werd overgegaan, die door de tweede backreference wordt gevolgd. `($1sessionid=%{sessionid}$2)`.

**RewriteCond** onderzoekt veranderlijke sessionid `(%{sessionid})`. Als het ten minste één teken bevat (...+), dan de gelijken RewriteRule.

Aldus, als de onderzoeksvraag is `"https://search.atomz.com/search/?sp_a=sp99999999&sp_q=word&sessionid=5678"`, dan zal al onderzoeksresultaat URLs worden herschreven zodat de &quot;sessionid&quot;waarde &quot;5678&quot;in plaats van de &quot;sessionid&quot;waarde is die de onderzoeksrobot ontmoette toen het uw plaats kruipde en de verbindingen bewaarde.

**Erkenning**

De software van de herschrijfmachine werd oorspronkelijk ontwikkeld door de Groep van Apache voor gebruik in het de serverproject van HTTP van Apache (https://www.apache.org/).

## URL-regels toevoegen voor zoeken {#task_50C77D1B53804AEEB20896F74265BD6F}

U kunt onderzoek URL regels toevoegen om te specificeren hoe URLs in uw resultaten van het websiteonderzoek wordt getoond. De regels werken op volledige URLs. U kunt om het even welk gedeelte van URL, met inbegrip van vraagargumenten manipuleren waar de informatie van zittingsidentiteitskaart vaak wordt gehouden.

<!-- 

t_adding_search_url_rules.xml

 -->

**ZoekURL-regels toevoegen**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Rewrite Rules]** > **[!UICONTROL Search URL Rules]**.
1. Op het [!DNL Search URL Rules] gebied, ga de regels in die u wilt.

   De lege lijnen en de commentaarlijnen die met een karakter &quot;#&quot;beginnen (knoeiboel) worden toegelaten.
1. (Facultatief) op de [!DNL Search URL Rules] pagina, op het [!DNL Test Search URL Rules] gebied, ga een test URL in waarvan kruipt regels u, dan **Test** testen en wilt klikken.
1. Klik **sparen Veranderingen**.
1. (Facultatief) herbouw uw gefaseerde plaatsindex als u aan voorproef de resultaten wilt.

   Zie [het Vormen van een stijgende index van een gefaseerde website](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Facultatief) op de [!DNL Search URL Rules] pagina, doe om het even welke volgend:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Over de regels voor zoektitels {#concept_C72D20F8DFF64EDE809AF4B72797E858}

De Regels van de Titel van het onderzoek specificeren hoe de titels in uw resultaten van het websiteonderzoek worden getoond. Om het even welk gedeelte van de titel kan worden gemanipuleerd.

<!-- 

c_about_search_title_rules.xml

 -->

Een herschrijf regel zou kunnen worden gebruikt om een gedeelte van een titel, zoals een organisatienaam te verwijderen, bijvoorbeeld. Door gebrek, heeft het plaatsonderzoek/de merchandising geen titelregels en maakt geen titelwijzigingen.

De regels van de titel kunnen uit twee hoofdelementen bestaan: HerwriteRule en facultatieve RewriteCond. Er kan een onbeperkt aantal regels en voorwaarden worden vastgesteld. De orde van deze regels is belangrijk, omdat de regelreeks door regel door van een lus wordt voorzien. Wanneer een regel aanpast, de softwarelijnen door om het even welke (facultatieve) overeenkomstige herschrijf voorwaarden. De regels van de Titel van het onderzoek worden gespecificeerd op de volgende manier:

```
RewriteCond  
<i>TestString CondPattern [Flags]</i> 
RewriteRule  
<i>Pattern Substitution [Flags]</i> 
 
RewriteCond  
<i>TestString CondPattern [Flags]</i> 
RewriteRule  
<i>Pattern Substitution [Flags]</i>
```

Wanneer een titel wordt ontmoet, probeert het plaatsonderzoek/het merchandising om het aan het Patroon van elk aan te passen kruipt regel. Als de patroongelijken, herschrijft de motor overeenkomstige richtlijnen RewriteCond zoekt. Als geen voorwaarden aanwezig zijn, wordt de titel vervangen door een nieuwe waarde die van het koord van de Vervanging wordt geconstrueerd en met de volgende regel in de regelreeks verdergaat. Indien de voorwaarden bestaan, worden zij verwerkt in de volgorde waarin zij worden vermeld. De herschrijf motor probeert om een voorwaardenpatroon (CondPattern) tegen een testkoord (TestString) aan te passen. Als de twee gelijke, dan wordt de volgende voorwaarde verwerkt tot geen meer voorwaarden beschikbaar zijn. Als alle voorwaarden aanpassen, wordt URL vervangen met de Vervanging die in de regel wordt gespecificeerd. Als niet aan de voorwaarde wordt voldaan, ontbreekt de volledige reeks voorwaarden en de overeenkomstige regel.

## HerschrijvenRegel richtlijn {#section_3BF2B0FF89F74A26AE79D68FA3184B9B}

Elke richtlijn RewriteRule bepaalt één het herschrijven regel. De regels worden toegepast in de volgorde waarin zij worden vermeld. Een herschrijfregel neemt de volgende vorm aan:

```
RewriteRule Pattern Substitution [Flags]
```

**Patroon** een regelmatige POSIX uitdrukking, die wordt toegepast op de huidige titel. De &quot;huidige titel&quot; kan afwijken van de oorspronkelijke titel, omdat eerdere regels mogelijk al aangepast en gewijzigd zijn.

Zie [Regelmatige expressies](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

U kunt het &quot;niet&quot;karakter (&quot;!&quot;) gebruiken om het patroon voor te bereiden. Het &quot;niet&quot;karakter laat u een patroon negeren. Dat wil zeggen, om waar te zijn slechts als de huidige titel NIET het patroon aanpast. Het &quot;niet&quot;karakter kan worden gebruikt wanneer het beter is om een negatief patroon aan te passen, of als definitieve standaardregel. Opmerking: U kunt niet zowel het &quot;niet&quot;karakter als gegroepeerde vervangingen in een patroon gebruiken. Bovendien kunt u geen verwaarloosd patroon gebruiken wanneer het substitutiekoord $N bevat.

U kunt haakjes gebruiken om een backreference tot stand te brengen, die door de Substitutie en CondPattern kan worden van verwijzingen voorzien.

**Substitutie** De titel wordt volledig vervangen door het substitutiekoord, dat het volgende kan bevatten:

Gewone tekst - Tekst die door onveranderd wordt overgegaan.

**De verwijzingen** verlenen toegang tot de gegroepeerde delen (binnenhaakje) van het Patroon of CondPattern. Het volgende is twee types van backreferences:

* **Achterverwijzingen** van RewriteRule Deze gelijke backreferences in het overeenkomstige Patroon RewriteRule en nemen de vorm $N (0 &lt;= N &lt;= 9). Bijvoorbeeld: `RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`

* ** RewriteCond Backreferences** Deze gelijke backreferences in het laatst overeenkomende RewriteCond CondPattern en nemen de vorm %N (0 &lt;= N &lt;= 9).

**Variabelen** dit zijn variabelen van de vorm % {NAME_OF_VARIABLE} waar NAME_OF_VARIABLE een koord voor de naam van een bepaalde variabele kan zijn. Zie de vlag [E] voor meer informatie bij het plaatsen van milieuvariabelen. De variabelen kunnen ook in de onderzoeksvorm worden bepaald die de onderzoeksresultaten produceerde.

**Functies** Dit zijn functies van de vorm $ {NAME_OF_FUNCTION: key} waar NAME_OF_FUNCTION is:

* de aanjager maakt alle karakters in *zeer belangrijke* kleine letters.
* toupper maakt alle karakters in *zeer belangrijke* hoofdletters.

Er is een speciale substitutiekoord: &quot;-&quot; dat betekent &quot;GEEN vervanging&quot;. Het &quot;-&quot;koord is vaak nuttig samen met de vlag van C (ketting), toestaand u om een titel aan verscheidene patronen aan te passen alvorens een substitutie voorkomt.

**Vlaggen** (facultatief)

De vlaggen zijn ingesloten tussen haakjes `[]`, en de veelvoudige vlaggen zijn komma-gescheiden:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> "last|L" </p> </td> 
   <td colname="col2"> <p> Laatste regel. </p> <p> Stop het herschrijvingsproces en pas geen extra herschrijvingsregels toe. Gebruik deze vlag om het even welke verdere verwerking aan de huidige titel te verhinderen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'Volgende|N' </p> </td> 
   <td colname="col2"> <p>Volgende ronde. </p> <p> Voer het herschrijfproces (opnieuw beginnen met de eerste herschrijvingsregel) opnieuw uit met de titel van de laatste herschrijfregel (niet de oorspronkelijke titel!). Wees voorzichtig om geen dode lus te creëren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> "ketting|C" </p> </td> 
   <td colname="col2"> <p>Beeten met de volgende regel. </p> <p> Deze vlag ketent de huidige regel aan de volgende regel (die ook aan zijn volgende regel kan worden geketend, etc.). Als een regel aanpast, dan gaat het substitutieproces zoals gebruikelijk verder. Als de regel niet aanpast, dan worden alle verdere geketende regels overgeslagen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> "no case|NC" </p> </td> 
   <td colname="col2"> <p> Geen zaak. </p> <p> Deze vlag maakt het Patroon case-insensitive. Dat wil zeggen dat er geen verschil is tussen "A-Z" en "a-z" wanneer het patroon wordt vergeleken met de huidige titel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> "skip|S=num" </p> </td> 
   <td colname="col2"> <p> Sla volgende regel of regels over. </p> <p> Als de huidige regel aanpast, dwingt deze vlag de herschrijfmotor om de volgende numregels in de regelreeks over te slaan. Gebruik dit om pseudo als-dan-anders concepten te maken. De laatste regel van de toen-clausule wordt een skip=N waar N het aantal regels in de anders-clausule is. (Dit is niet het zelfde als de "ketting|C"vlag!) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> "env|E=VAR:VAL" </p> </td> 
   <td colname="col2"> <p>Stel de omgevingsvariabele in. </p> <p> Deze vlag leidt tot een milieuvariabele "VAR"die aan de waarde VAL wordt geplaatst, waar VAL regelmatige uitdrukkingsbackreferences, $N en %N kan bevatten, die zullen worden uitgebreid. U kunt deze vlag meer dan eens gebruiken om veelvoudige variabelen te plaatsen. De variabelen kunnen later in een volgend patroon RewriteCond via % {VAR} worden van verwijzingen voorzien. Gebruik deze vlag om informatie van titels te ontdoen en te herinneren. </p> </td> 
  </tr> 
 </tbody> 
</table>

## HerschrijvenCond-richtlijn (optioneel) {#section_9D72B2AB454849A7B681BC39C506AAA3}

De richtlijn RewriteCond bepaalt een regelvoorwaarde. Wanneer een RewriteCond een RewriteRule voorafgaat, wordt de regel slechts gebruikt als zijn patroon de huidige titel aanpast en de extra voorwaarden van toepassing zijn.

De richtlijnen van de herschrijvingsvoorwaarde nemen de volgende vorm aan:

```
RewriteCond TestString CondPattern [Flags]
```

**TestString** is een koord dat de volgende concepten kan bevatten:

Gewone tekst - Tekst die door onveranderd wordt overgegaan.

De verwijzingen van de achtergrond verlenen toegang tot de gegroepeerde delen (binnenhaakje) van het Patroon of CondPattern. Er zijn twee types van backreferences:

* **Achterverwijzingen** van RewriteRule Deze gelijke backreferences in het overeenkomstige Patroon RewriteRule en nemen de vorm $N (0 &lt;= N &lt;= 9). Bijvoorbeeld: `RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`

* **HerwriteCond Backreferences** Deze gelijke backreferences in het laatst overeenkomende RewriteCond CondPattern en nemen de vorm %N (0 &lt;= N &lt;= 9).

**Variabelen** dit zijn variabelen van de vorm % {NAME_OF_VARIABLE} waar NAME_OF_VARIABLE een koord voor de naam van een bepaalde variabele kan zijn. Zie de `[E]` vlag voor meer informatie bij het plaatsen van milieuvariabelen. De variabelen kunnen ook in de onderzoeksvorm worden bepaald die de onderzoeksresultaten produceerde.

**Functies** Dit zijn functies van de vorm $ {NAME_OF_FUNCTION:key} waar NAME_OF_FUNCTION is:

* de aanjager maakt alle karakters in *zeer belangrijke* kleine letters.
* toupper maakt alle karakters in *zeer belangrijke* hoofdletters.
* vlucht URL-codeert alle karakters in *sleutel*.
* De tekens &#39;a&#39;...z&#39;, &#39;A&#39;...Z&#39;, &#39;0&#39;...9&#39;, &#39;*&#39;, &#39;-&#39;, &#39;.&#39;, &#39;/&#39;, &#39;@&#39;, en &#39;_&#39; worden ongewijzigd gelaten, worden de ruimten vertaald in &#39;+&#39;, en alle andere karakters worden omgezet in hun %xx URL-Gecodeerde equivalent.
* unescape zet &#39;+&#39; terug naar spatie en alle %xx URL-gecodeerde tekens terug naar enkele tekens.

Er is een speciale substitutiekoord: &quot;-&quot; dat betekent &quot;GEEN vervanging&quot;. Het &quot;-&quot;koord is vaak nuttig samen met de vlag van C (ketting), toestaand u om een URL aan verscheidene patronen aan te passen alvorens een substitutie voorkomt.

**CondPattern** een standaard Uitgebreide Regelmatige Uitdrukking met sommige toevoegingen. Het patroonkoord kan met een &quot;!&quot; vooraf worden bevestigd karakter (uitroepteken) om een niet-aanpassingspatroon te specificeren. In plaats van echte regelmatige uitdrukkingskoorden, kunt u één van de volgende speciale varianten gebruiken.

Al deze tests kunnen ook worden voorafgegaan door een uitroepteken (&#39;!&#39;) om hun betekenis te negeren.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CondPattern-tekenreeks </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> '&lt;CondPattern' </p> </td> 
   <td colname="col2"> <p>Is lexicaal minder. </p> <p> Behandelt <i>CondPattern</i> als duidelijk koord en vergelijkt het lexically met <i>TestString</i>. Waar als <i>TestString</i> lexically minder dan <i>CondPattern</i>is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '&gt;CondPattern' </p> </td> 
   <td colname="col2"> <p> Is lexicaal groter. </p> <p> Behandelt <i>CondPattern</i> als duidelijk koord en vergelijkt het lexically met <i>TestString</i>. Waar als <i>TestString</i> lexically groter is dan <i>CondPattern</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '=CondPattern' </p> </td> 
   <td colname="col2"> <p>Is lexicaal gelijk. </p> <p> Behandelt <i>CondPattern</i> als duidelijk koord en vergelijkt het lexically met <i>TestString</i>. Waar als <i>TestString</i> lexisch gelijk aan <i>CondPattern</i>is. Namelijk zijn de twee koorden precies gelijk (karakter door karakter). Als <i>CondPattern</i> enkel ""(twee aanhalingstekens) is, vergelijkt dit <i>TestString</i> bij het lege koord. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Vlaggen** (facultatief)

De vlaggen zijn ingesloten tussen haakjes`[]`, en de veelvoudige vlaggen zijn komma-gescheiden:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> "geen geval|NC" (geen geval) </p> </td> 
   <td colname="col2"> <p>Maakt de test niet gevoelig. Namelijk is er geen verschil tussen "A-Z"en "a-z"zowel in uitgebreide <i>TestString</i> als in <i>CondPattern</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'of volgende|OR' (of volgende voorwaarde) </p> </td> 
   <td colname="col2"> <p> Gebruik dit om regelvoorwaarden met lokaal OF in plaats van impliciet te combineren EN. Zonder deze vlag zou u de voorwaarde/de regel veelvoudige tijden moeten schrijven. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Voorbeeld {#section_E7454FFE169E459AABD9D033651939CB}

Veronderstel dat u een collectieve Website met een standaardtitelformaat hebt: &quot;Mijn Bedrijf&quot;gevolgd door een koppelteken en toen een pagina-specifieke beschrijving (&quot;Mijn Bedrijf - Onthaal&quot;of &quot;Mijn Bedrijf - Nieuws&quot;, bijvoorbeeld). U wilt &quot;Mijn Bedrijf -&quot;van de titel ontdoen en de volledige titel in hoofdletters omzetten wanneer het de plaats indexeert.

De volgende herschrijf regel gebruikt de functietrapper om slechts het beschrijvende gedeelte van een titel in hoofdletters te herschrijven:

```
RewriteRule  ^My[[:blank:]]Company[[:blank:]]-[[:blank:]] 
<b>(.*)</b>$  ${toupper: 
<b>$1</b>} 
```

Het patroon van de regel `(^My[[:blank:]]Company[[:blank:]]-[[:blank:]] (.*))` bevat een backreference **`(.*)`** die de titelinhoud aanpast die &quot;Mijn Bedrijf-&quot;volgt. Herinner dat het omringen van een gedeelte van een patroon met haakje () tot een backreference leidt die door de Substitutie kan worden van verwijzingen voorzien. In dit voorbeeld, herschrijft de Vervanging ($ {toupper:**$1**}) die backreference (**$1**) gebruikend de toupperfunctie.

Aldus, wordt een titel van het formulier &quot;Mijn Bedrijf - Onthaal&quot;herschreven als &quot;WELKOM&quot;.

**Erkenning**

De software van de herschrijfmachine werd oorspronkelijk ontwikkeld door de Groep van Apache voor gebruik in het de serverproject van HTTP van Apache (https://www.apache.org/).

## Regels voor zoektitels toevoegen {#task_155CECB74BE3444384EDBBD04F41515E}

U kunt de regels van de onderzoekstitel toevoegen om te specificeren hoe de titels in uw resultaten van het websiteonderzoek worden getoond. U kunt om het even welk gedeelte van de titel manipuleren.

<!-- 

t_adding_search_title_rules.xml

 -->

**Om de regels van de zoektitel toe te voegen**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Rewrite Rules]** > **[!UICONTROL Search Title Rules]**.
1. Op het [!DNL Search Title Rules] gebied, ga de regels in die u wilt.

   De lege lijnen en de commentaarlijnen die met een karakter &quot;#&quot;beginnen (knoeiboel) worden toegelaten.
1. (Facultatief) op de [!DNL Search Title Rules] pagina, op het [!DNL Test Search Title Rules] gebied, ga een testtitel in, en klik dan **Test**.
1. Klik **sparen Veranderingen**.
1. (Facultatief) herbouw uw gefaseerde plaatsindex als u aan voorproef de resultaten wilt.

   Zie [het Vormen van een stijgende index van een gefaseerde website](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Facultatief) op de [!DNL Search Title Rules] pagina, doe om het even welke volgend:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

