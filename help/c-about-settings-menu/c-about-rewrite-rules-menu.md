---
description: Met het menu Regels herschrijven kunt u de regels voor het doorzoeken en doorzoeken van URL's en titels instellen.
solution: Target
subtopic: Rewrite Rules
title: Het menu Regels herschrijven
topic-legacy: Settings,Site search and merchandising
uuid: 77ee84dd-fdba-4d34-ae8e-2fe786599800
exl-id: cff17ead-6997-4ff6-a995-7ca020b06d50
translation-type: tm+mt
source-git-commit: aa095add9eb656913792b3f14001dda66cdd7d67
workflow-type: tm+mt
source-wordcount: '10178'
ht-degree: 0%

---

# Informatie over het menu Regels herschrijven {#about-the-rewrite-rules-menu}

Met het menu Regels herschrijven kunt u de regels voor het doorzoeken en doorzoeken van URL&#39;s en titels instellen.

## Info over URL-regels voor een webwinkel horizontaal schuiven {#concept_B71CF4C8030A4A74A22C3BFE4DE3B865}

Met URL-regels horizontaal schuiven geeft u op hoe de URL&#39;s die worden aangetroffen in webinhoud, worden herschreven. U kunt een onbeperkt aantal regels en voorwaarden opgeven en u kunt elk gedeelte van de aangetroffen URL&#39;s manipuleren.

<!-- 

c_about_crawl_list_store_url_rules.xml

 -->

De regels voor horizontaal schuiven zijn vooral handig voor het herschrijven van dynamische delen van een URL, zoals een sessie-id die uniek is voor elke klant die uw website bezoekt. U kunt ook herschrijfregels gebruiken om delen van een URL, zoals queryparameters, te verbergen voor de zoekrobot. Standaard worden geen regels opgegeven en wordt het herschrijven van de URL niet uitgevoerd.

Wanneer een website wordt gekropen, worden ingesloten inhoud-URL&#39;s opgeslagen in een tijdelijke lijst met extra webpagina&#39;s die moeten worden vergroot. Voordat een URL aan deze lijst wordt toegevoegd, worden de regels voor het herschrijven van winkels op deze URL toegepast. Doorgaans worden de regels voor het herschrijven van winkels gebruikt om een sessie-id te verwijderen uit een URL of om een specifieke sessie-id voor horizontaal schuiven af te dwingen. Wanneer de zoekrobot een URL uit de lijst ophaalt, worden de regels voor het opvragen van herschrijven gebruikt om gedeelten van die URL opnieuw te manipuleren. Doorgaans worden de regels voor het ophalen gebruikt voor het invoegen van tijdgevoelige gegevens in de URL. Deze laatste URL wordt gebruikt om de pagina daadwerkelijk van uw website op te halen.

Zie [Info kruipt Lijst terugwinnen URL-regels](../c-about-settings-menu/c-about-rewrite-rules-menu.md#concept_EC8E2E48B99A458D8567B526C9827CBA).

Doorgaans gebruik je alleen URL-regels voor winkel. Retrieve URL-regels zijn alleen nodig als URL&#39;s dynamische gegevens bevatten, zoals een sessie-id, en als die dynamische gegevens na verloop van tijd veranderen om geldig te blijven. In dit geval gebruikt u Winkel-URL-regels om de meest recente status van de gegevens van de aangetroffen URL&#39;s op te halen. Vervolgens gebruikt u de URL-regels ophalen om die gegevens aan elke URL toe te voegen wanneer de zoekrobot de pagina probeert op te halen.

Elke regel wordt gespecificeerd met een herschrijven regel (RewriteRule) richtlijn en één of meerdere facultatieve herschrijft voorwaarden (RewriteCond). De volgorde van de regels is belangrijk. De regelreeks wordt door regel van een lus voorzien. Wanneer een regel aanpast, het door om het even welke overeenkomstige herschrijft voorwaarden van een lus voorziet. Een kruipende URL regel wordt gespecificeerd op de volgende manier:

```
RewriteCond TestString CondPattern [Flags] 
RewriteRule Pattern Substitution [Flags]
```

Wanneer een ingesloten URL wordt aangetroffen, probeert de zoekrobot de URL overeen te laten komen met het patroon van elke horizontale lijn. Als het patroon overeenkomt, zoekt de engine voor herschrijven naar de overeenkomende richtlijnen voor herschrijvenCond. Als er geen voorwaarden aanwezig zijn, wordt de URL vervangen door een nieuwe waarde die wordt samengesteld uit de vervangende tekenreeks en gaat deze verder met de volgende regel in de regelset. Indien er voorwaarden bestaan, worden ze verwerkt in de volgorde waarin ze worden vermeld. De engine voor herschrijven probeert een voorwaardepatroon (CondPattern) af te stemmen op een testtekenreeks (TestString). Als de twee gelijke, dan wordt de volgende voorwaarde verwerkt tot geen meer voorwaarden beschikbaar zijn. Als alle voorwaarden overeenkomen, wordt de URL vervangen door de Substitutie die in de regel is opgegeven. Als niet aan de voorwaarde wordt voldaan, ontbreekt de volledige reeks voorwaarden en de overeenkomstige regel.

## Info over RewriteRule-instructies {#section_162122340BB34F12BB9A36DC9349092B}

Een instructie RewriteRule heeft de volgende vorm:

```
           
<i>RewriteRule Pattern Substitution [Flags]</i> 
        
```

`Pattern` Dit kan een reguliere POSIX-expressie zijn, die wordt toegepast op de huidige URL. De &quot;huidige URL&quot; kan afwijken van de oorspronkelijke aangevraagde URL, omdat eerdere regels mogelijk al overeenkomen met de URL en deze hebben gewijzigd.

Zie [Gewone uitdrukkingen](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

U kunt het teken &#39;not&#39; (&#39;!&#39;) niet gebruiken als u een voorvoegsel voor het patroon wilt toevoegen. Met het teken &#39;not&#39; kunt u een patroon negeren. Dit betekent dat u alleen waar hoeft te zijn als de huidige URL NIET overeenkomt met dit patroon. Het teken &#39;not&#39; kan worden gebruikt wanneer een negatief patroon beter kan worden weergegeven of als een laatste standaardregel.

>[!NOTE]
>
>U kunt niet zowel het teken &quot;niet&quot; als de gegroepeerde jokertekens in een patroon gebruiken. Daarnaast kunt u geen negatiefpatroon gebruiken wanneer de vervangende tekenreeks $N bevat.

U kunt ronde haakjes gebruiken om een achterverwijzing in het patroon te maken, waarnaar kan worden verwezen door Substitution en CondPattern.

**** VervangingDe URL wordt vervangen door de vervangingstekenreeks die het volgende bevat:

Onbewerkte tekst: Tekst die ongewijzigd wordt doorgegeven.

Backreferences bieden toegang tot de gegroepeerde delen (tussen haakjes) van het Patroon of het CondPattern. Hier volgen de twee typen terugverwijzingen:

* **RewriteRule** BackreferencesDeze gelijke backreferences in het overeenkomstige RewriteRule Pattern en nemen de vorm $N (0  &lt;> Bijvoorbeeld: `RewriteRule ^https:// ([^/]*) (.*)$ https://${tolower: $1} $2.`

* **RewriteCond** BackreferencesDeze overeenkomsten backreferences in the last match RewriteCond Cond Cond Pattern en hebben de vorm %N (0  &lt;>

Variabelen: Dit zijn variabelen van de vorm %{NAME_OF_VARIABLE} waar NAME_OF_VARIABLE een koord voor de naam van een bepaalde variabele is. Zie de markering `*[E]*` voor meer informatie over het instellen van omgevingsvariabelen.

Functies: Dit zijn functies van de vorm ${NAME_OF_FUNCTION:key} waar NAME_OF_FUNCTION het volgende is:

* met tolower worden alle tekens in *key* kleine letters gemaakt.
* toupper maakt alle tekens in *key* hoofdletters.
* escape URL-codeert alle tekens in *key*.
* De tekens &#39;a&#39;..z&#39;, &#39;A&#39;..&#39;Z&#39;, &#39;0&#39;..&#39;9&#39;, &#39;*&#39;, &#39;-&#39;, &#39;.&#39;, &#39;/&#39;, &#39;@&#39; en &#39;_&#39; worden niet gewijzigd; spaties worden omgezet in &#39;+&#39; en alle andere tekens worden getransformeerd naar hun %xx URL-gecodeerde equivalent.
* unescape transformeert &#39;+&#39; terug naar spatie en alle %xx URL-gecodeerde tekens terug naar één teken.

>[!NOTE]
>
>Er is een speciale vervangende tekenreeks: `'-'` dat betekent &quot;GEEN vervanging&quot;. De tekenreeks `'-'` wordt vaak gebruikt met de markering C (chain), zodat u een URL kunt koppelen aan verschillende patronen voordat een vervanging plaatsvindt.

**Vlaggen**

(optioneel) Afsluitmarkeringen tussen haakjes `[]`. Meerdere markeringen worden gescheiden door komma&#39;s.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'last|L' </p> </td> 
   <td colname="col2"> <p>Laatste regel. </p> <p>Stopt het herschrijfproces en past geen aanvullende herschrijfregels toe. Gebruik deze markering om verdere verwerking naar de huidige URL te voorkomen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'next|N' </p> </td> 
   <td colname="col2"> <p>Volgende ronde. </p> <p> Herstelt het herschrijfproces (opnieuw beginnend met de eerste het herschrijven regel) gebruikend URL van de laatste het herschrijven regel (niet originele URL). Wees voorzichtig en maak geen dode lus! </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'chain|C' </p> </td> 
   <td colname="col2"> <p>Bewerkt met volgende regel. </p> <p>Hiermee wordt de huidige regel geketend op de volgende regel (die ook aan de volgende regel kan worden gekoppeld, enzovoort). Als een regel overeenkomt, gaat het vervangingsproces zoals gewoonlijk verder. Als de regel niet overeenkomt, worden alle volgende regels in een keten overgeslagen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' </p> </td> 
   <td colname="col2"> <p>Geen geval. </p> <p> Maakt het patroon niet hoofdlettergevoelig (er is dus geen verschil tussen 'A-Z' en 'a-z') wanneer het patroon overeenkomt met de huidige URL. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'skip|S=num' </p> </td> 
   <td colname="col2"> <p>Sla de volgende regel of regels over. </p> <p> Als de huidige regel aanpast, dwingt deze vlag de herschrijfmotor om de volgende numregels in de regelreeks over te slaan. Gebruik deze markering om pseudo-if-then-else-constructs te maken. De laatste regel van toen-clausule wordt een skip=N waar N het aantal regels in de else-clausule is. </p> <p> <p>Opmerking:  Deze markering is niet hetzelfde als de markering 'chain|C'!) </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'env|E=VAR:VAL' </p> </td> 
   <td colname="col2"> <p>Hiermee wordt de omgevingsvariabele ingesteld. </p> <p>Maakt een omgevingsvariabele "VAR" die is ingesteld op de waarde VAL, waarbij VAL reguliere expressies backreferences, $N en %N kan bevatten, die worden uitgebreid. U kunt deze markering meerdere keren gebruiken om meerdere variabelen in te stellen. De variabelen kunnen later worden geschrapt-van verwijzingen voorzien in een volgend patroon RewriteCond via %{VAR}. </p> <p>Gebruik deze markering om informatie van URL's te verwijderen en te onthouden. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>De Opslag herschrijft Regels en terugwinnen herschrijft Regels delen veranderlijke waarden. Vanwege dit gedrag kunt u een variabele instellen op een tijdgevoelige sessionid-waarde wanneer een ingesloten URL wordt aangetroffen en opgeslagen. Wanneer de volgende URL wordt opgehaald uit de lijst met tijdelijke opslag, kan de laatste sessionid-waarde eraan worden toegevoegd voordat die pagina wordt opgehaald.

**Voorbeeld van een RewriteRule met een functie**

Veronderstel dat u een case-sensitive server hebt, die de koorden `"www.mydomain.com"` en `"www.MyDomain.com"` verschillend behandelt. Uw server werkt alleen correct als het domein altijd `"www.mydomain.com"` is, ook al bevatten sommige documenten koppelingen die `"www.MyDomain.com."` Hiervoor verwijzen, u kunt de volgende regel gebruiken:

```
RewriteRule  ^https:// 
<b>([^/]*)</b> 
<i>(.*)</i>$  https://${tolower:$1}$2
```

Deze herschrijfregel gebruikt de functie `tolower` om het domeingedeelte van een URL te herschrijven om ervoor te zorgen dat het altijd in kleine letters zoals in het volgende is:

1. Het patroon `(^https://([^/]*)(.*)$)` bevat een backreference `([^/]*)` die alle karakters tussen `https://` en eerste `/` in URL aanpast. Het patroon bevat ook een tweede achterverwijzing `(.*)` die overeenkomt met alle resterende tekens in de URL.

1. De vervanging `(https://${tolower:$1}$2)` vertelt het onderzoeksmotor om URL te herschrijven door de `tolower` functie op de eerste backreference `(https:// ${tolower:$1}$2)` te gebruiken die de rest van URL onveranderd `(https://${tolower:$1} $2)` laat.

Zo wordt een URL van het formulier `https://www.MyDomain.com/INTRO/index.Html` herschreven als `https://www.mydomain.com/INTRO/index.Html`.

## Info over RewriteCond-instructies {#section_CD5A19B2D3204F73B645411931FC34A1}

De instructie RewriteCond definieert een regelvoorwaarde. Wanneer RewriteCond een RewriteRule voorafgaat, wordt de regel slechts gebruikt als zijn patroon de huidige titel aanpast en de extra voorwaarden van toepassing zijn. Herschrijfvoorwaarden hebben de volgende vorm:

```
           
<i>RewriteCond TestString CondPattern [Flags]</i> 
        
```

`TestString` is een tekenreeks die de volgende elementen kan bevatten:

Onbewerkte tekst: Tekst die ongewijzigd wordt doorgegeven.

Backreferences bieden toegang tot de gegroepeerde delen (tussen haakjes) van het Patroon of het CondPattern. Hier volgen de twee typen terugverwijzingen:

* **RewriteRule** BackreferencesDeze gelijke backreferences in het overeenkomstige RewriteRule Pattern en nemen de vorm $N (0  &lt;> Bijvoorbeeld, `RewriteRule ^https:// ([^/]*) (.*)$ https://${tolower: $1} $2`.

* **RewriteCond** BackreferencesDeze overeenkomsten backreferences in the last match RewriteCond Cond Cond Pattern en hebben de vorm %N (0&lt;>

Variabelen: Dit zijn variabelen van de vorm %{NAME_OF_VARIABLE} waar NAME_OF_VARIABLE een koord voor de naam van een bepaalde variabele kan zijn. Zie de markering RewriteRule *`[E]`* voor meer informatie over het plaatsen van variabelen.

Functies: Dit zijn functies van de vorm ${NAME_OF_FUNCTION:key} waar NAME_OF_FUNCTION het volgende is:

* met tolower worden alle tekens in *key* kleine letters gemaakt.
* toupper maakt alle tekens in *key* hoofdletters.
* escape URL-codeert alle tekens in sleutel. De tekens &#39;a&#39;..z&#39;, &#39;A&#39;..&#39;Z&#39;, &#39;0&#39;..&#39;9&#39;, &#39;*&#39;, &#39;-&#39;, &#39;.&#39;, &#39;/&#39;, &#39;@&#39; en &#39;_&#39; worden niet gewijzigd, spaties worden omgezet in &#39;+&#39; en alle andere tekens worden omgezet in hun `%xx` URL-gecodeerde equivalent.
* unescape transformeert &#39;+&#39; terug naar spatie en alle `%xx` URL-coderingstekens terug naar enkele tekens.

**** CondPatternis een standaard Extended Regular Expression met enkele toevoegingen. De patroontekenreeks kan worden voorafgegaan door een `!`-teken (uitroepteken) om een niet-overeenkomend patroon op te geven. In plaats van echte reguliere-expressietekenreeksen kunt u een van de volgende speciale varianten gebruiken:

>[!NOTE]
>
>U kunt al deze tests met een uitroepteken (&#39;!&#39;) ook vooraf instellen hun betekenis te negeren.

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
   <td colname="col2"> <p>Lexisch minder. </p> <p> Behandelt CondPattern als een onbewerkte tekenreeks en vergelijkt het lexicaal met TestString. True if TestString is lexically less than CondPattern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '&gt;CondPattern' </p> </td> 
   <td colname="col2"> <p>Lexisch groter. </p> <p> Behandelt CondPattern als een onbewerkte tekenreeks en vergelijkt het lexicaal met TestString. True als TestString lexically groter is dan CondPattern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '=CondPattern' </p> </td> 
   <td colname="col2"> <p>Lexisch gelijk. </p> <p> Behandelt CondPattern als een onbewerkte tekenreeks en vergelijkt het lexicaal met TestString. True if TestString is lexously gelijk aan CondPattern, dat wil zeggen, de twee tekenreeksen zijn exact gelijk (karakter door karakter). Als CondPattern enkel "" (twee aanhalingstekens) is, vergelijkt dit TestString met het lege koord. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Markeringen**
 (optioneel) Afsluiten markeringen tussen haakjes  `[]`. Meerdere markeringen worden gescheiden door komma&#39;s.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' </p> </td> 
   <td colname="col2"> <p> Geen geval. </p> <p>Deze vlag maakt de test niet hoofdlettergevoelig, namelijk is er geen verschil tussen "A-Z"en "a-z"zowel in uitgebreide TestString als in CondPattern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'ornext|OR' </p> </td> 
   <td colname="col2"> <p>Of volgende voorwaarde. </p> <p>Gebruik deze vlag om regelvoorwaarden met lokale OF in plaats van impliciete AND te combineren. Zonder deze vlag, zou u de cond/de regel veelvoudige tijden moeten schrijven. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Voorbeeld**

Sommige webpagina&#39;s wijzen de eerste keer dat een bezoeker bij een site aankomt, een CGI-variabele toe. Deze variabele wordt gebruikt om de bezoeker te identificeren en, aangezien de bezoeker door de plaats bladert, wordt de variabele overgegaan. Omdat de zoekrobot eruit ziet als een bezoeker van uw site, krijgt deze een sessionid-nummer toegewezen. De zoekrobot handhaaft deze enkele waarde voor sessionid, zelfs als een tweede sitepagina een nieuwe waarde probeert toe te wijzen. Om dit te verzekeren, hebt u twee herschrijven regels nodig.

De eerste regel wordt gebruikt om de sessionid-variabele te identificeren en op te slaan:

```
RewriteCond  %{sessionid}  !.+ 
RewriteRule  ^.+sessionid= 
<b>([^&#]+)</b>.*$  -   
<i>[E=sessionid:$1]</i>
```

RewriteRule gebruikt een E-vlag `([E=sessionid:$1])` om de huidige waarde van de zittende parameter CGI aan de variabele `sessionid` toe te wijzen. `$1` verwijst naar de eerste backreference, die tussen de eerste reeks haakjes in het Patroon van RewriteRule `([^&#]+)` bevat.

De reguliere expressie `^&#]+` komt overeen met het deel van een URL tussen het woord `sessionid` en het volgende `**&**or**#**` teken. Aangezien deze RewriteRule slechts wordt gebruikt om de aanvankelijke waarde voor de sessionid variabele tot stand te brengen, herschrijft het niet. Merk op dat het gebied van de Vervanging van de regel aan `-` wordt geplaatst om erop te wijzen dat het herschrijven niet wordt vereist.

RewriteCond onderzoekt de variabele `sessionid` ( `%{sessionid}`). Als het zelfs geen enkel teken heeft (!.+), dan de overeenkomsten RewriteRule.

Met deze regel wordt de URL gelezen als `https://www.domain.com/home/?sessionid=1234&function=start` en wijst u de waarde `1234` toe aan de variabele `sessionid`.

De tweede regel wordt gebruikt om alle URL&#39;s te herschrijven die overeenkomen met het volgende RewriteRule-patroon:

```
RewriteRule   
<b>^(.+)</b>sessionid=[^&#]+ 
<i>(.*)$</i>  $1sessionid=%{sessionid}$2
```

Het patroon RewriteRule bevat twee terugverwijzingen: `(.+)` en `(.*)`. De eerste backreference komt overeen met alle tekens vóór `sessionid`. De tweede backreference komt overeen met alle tekens na het einde van `&` of `#`.

Het patroon van de Vervanging herschrijft URL gebruikend de eerste backreference, die door het koord &quot;sessionid=&quot;wordt gevolgd, door de waarde van de zittingidentiteitskaart variabele die door de eerste regel `%{sessionid}` wordt bepaald, door de tweede backreference wordt gevolgd. `($1sessionid=%{sessionid} $2)`

Bericht dat this RewriteRule geen RewriteCond bevat. Als dusdanig, veroorzaakt het herschrijven voor alle URLs die RewriteRule *Pattern* aanpassen. Als de waarde van de sessionid-variabele ( `%{sessionid}`) `1234` is, wordt een URL van het formulier `https://www.domain.com/products/?sessionid=5678&function=buy` herschreven als `https://www.domain.com/products/?sessionid=1234&function=buy`

## Toespraak {#section_B17088EF38244496BC1DDD4ECF75EB5B}

De software voor het herschrijven van engines is oorspronkelijk ontwikkeld door de Apache Group voor gebruik in het Apache HTTP-serverproject (https://www.apache.org/).

## Een regel {#task_22DD40DF95584B12BE8E6ECFBF579BCD} toevoegen voor een verkennende lijstopslag

U kunt URL-regels voor het verkennende lijstarchief toevoegen om op te geven hoe de URL&#39;s die worden aangetroffen in webinhoud, worden herschreven. U kunt een onbeperkt aantal regels en voorwaarden opgeven en u kunt elk gedeelte van de aangetroffen URL&#39;s manipuleren.

<!-- 

t_adding_a_crawl_list_store_url_rule.xml

 -->

**U voegt als volgt de URL-regels van de vervagingsopslag toe:**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Rewrite Rules]** > **[!UICONTROL Crawl List Store URL Rules]**.
1. Voer in het veld [!DNL Crawl List Store URL Rules] de gewenste regels in.

   Lege regels en commentaarregels die beginnen met een &#39;#&#39; (hash) teken zijn toegestaan.
1. (Optioneel) Voer in het veld [!DNL Test Crawl List Store URL Rules] op de pagina [!DNL Crawl List Store URL Rules] een test-URL in waarvan u de horizontaal schuivende regels wilt testen en klik op **[!UICONTROL Test]**.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Optioneel) Maak de gefaseerde site-index opnieuw als u een voorvertoning van de resultaten wilt zien.

   Zie [Een incrementele index van een gefaseerde website configureren](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Optioneel) Voer op de pagina [!DNL Crawl List Store URL Rules] een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Info URL-regels ophalen lijst horizontaal schuiven {#concept_EC8E2E48B99A458D8567B526C9827CBA}

Met URL-regels horizontaal schuiven bepaalt u hoe de URL&#39;s die worden aangetroffen in webinhoud, worden herschreven. U kunt een onbeperkt aantal regels en voorwaarden opgeven en u kunt elk gedeelte van de aangetroffen URL&#39;s manipuleren.

<!-- 

c_about_crawl_list_retrieve_url_rules.xml

 -->

Voordat de effecten van de regels zichtbaar zijn voor klanten, moet u de site-index opnieuw samenstellen.

De regels voor horizontaal schuiven zijn vooral handig voor het herschrijven van dynamische delen van een URL, zoals een sessie-id die uniek is voor elke klant die uw website bezoekt. U kunt ook herschrijfregels gebruiken om delen van een URL, zoals queryparameters, te verbergen voor de zoekrobot. Standaard worden geen regels opgegeven en wordt het herschrijven van de URL niet uitgevoerd.

Wanneer een website wordt gekropen, worden ingesloten inhoud-URL&#39;s opgeslagen in een tijdelijke lijst met extra webpagina&#39;s die moeten worden vergroot. Wanneer de zoekrobot een URL uit de lijst ophaalt, worden de regels voor herschrijven ophalen gebruikt om gedeelten van die URL te manipuleren. Doorgaans worden de regels voor het ophalen gebruikt voor het invoegen van tijdgevoelige gegevens in een URL. Deze laatste URL wordt gebruikt om de pagina daadwerkelijk van uw website op te halen.

Terugschrijfregels ophalen is alleen nodig als URL&#39;s dynamische gegevens bevatten, zoals een sessie-id, en als die dynamische gegevens in de loop der tijd veranderen om geldig te blijven. In dit geval gebruikt u Regels voor herschrijven van opslaan om de meest recente status van de gegevens van de aangetroffen URL&#39;s op te halen. Vervolgens gebruikt u de optie Herschrijfregels ophalen om die gegevens aan elke URL toe te voegen wanneer de zoekrobots de pagina ophalen.

Elke regel wordt gespecificeerd met een herschrijven regel (RewriteRule) richtlijn en één of meerdere facultatieve herschrijft voorwaarden (RewriteCond). De volgorde van de regels is belangrijk. De regelreeks wordt door regel van een lus voorzien. Wanneer een regel aanpast, het door om het even welke overeenkomstige herschrijft voorwaarden van een lus voorziet. Een kruipende URL regel wordt gespecificeerd op de volgende manier:

```
RewriteCond TestString CondPattern [Flags] 
RewriteRule Pattern Substitution [Flags]
```

Wanneer een ingesloten URL wordt aangetroffen, probeert de zoekrobot de URL overeen te laten komen met het patroon van elke horizontale lijn. Als het patroon overeenkomt, zoekt de engine voor herschrijven naar de overeenkomende richtlijnen voor herschrijvenCond. Als er geen voorwaarden aanwezig zijn, wordt de URL vervangen door een nieuwe waarde die wordt samengesteld uit de vervangende tekenreeks en gaat deze verder met de volgende regel in de regelset. Indien er voorwaarden bestaan, worden ze verwerkt in de volgorde waarin ze worden vermeld. De engine voor herschrijven probeert een voorwaardepatroon (CondPattern) af te stemmen op een testtekenreeks (TestString). Als de twee gelijke, dan wordt de volgende voorwaarde verwerkt tot geen meer voorwaarden beschikbaar zijn. Als alle voorwaarden overeenkomen, wordt de URL vervangen door de Substitutie die in de regel is opgegeven. Als niet aan de voorwaarde wordt voldaan, ontbreekt de volledige reeks voorwaarden en de overeenkomstige regel.

## Info over RewriteRule-instructies {#section_32B24B29627946398AFBC5F869A610CB}

Een instructie RewriteRule heeft de volgende vorm:

```
           
<i>RewriteRule Pattern Substitution [Flags]</i> 
        
```

`Pattern` Dit kan een reguliere POSIX-expressie zijn, die wordt toegepast op de huidige URL. De &quot;huidige URL&quot; kan afwijken van de oorspronkelijke aangevraagde URL, omdat eerdere regels mogelijk al overeenkomen met de URL en deze hebben gewijzigd.

Zie [Gewone uitdrukkingen](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

U kunt het teken &#39;not&#39; (&#39;!&#39;) niet gebruiken als u een voorvoegsel voor het patroon wilt toevoegen. Met het teken &#39;not&#39; kunt u een patroon negeren. Dit betekent dat u alleen waar hoeft te zijn als de huidige URL NIET overeenkomt met dit patroon. Het teken &#39;not&#39; kan worden gebruikt wanneer een negatief patroon beter kan worden weergegeven of als een laatste standaardregel.

>[!NOTE]
>
>U kunt niet zowel het teken &quot;niet&quot; als de gegroepeerde jokertekens in een patroon gebruiken. Daarnaast kunt u geen negatiefpatroon gebruiken wanneer de vervangende tekenreeks $N bevat.

U kunt ronde haakjes gebruiken om een achterverwijzing in het patroon te maken, waarnaar kan worden verwezen door Substitution en CondPattern.

**** VervangingDe URL wordt vervangen door de vervangingstekenreeks die het volgende bevat:

Onbewerkte tekst: Tekst die ongewijzigd wordt doorgegeven.

Backreferences bieden toegang tot de gegroepeerde delen (tussen haakjes) van het Patroon of het CondPattern. Hier volgen de twee typen terugverwijzingen:

* **RewriteRule** BackreferencesDeze gelijke backreferences in het overeenkomstige RewriteRule Pattern en nemen de vorm $N (0  &lt;> Bijvoorbeeld: `RewriteRule ^https:// ([^/]*) (.*)$ https://${tolower: $1} $2.`

* ** HerwriteCond Backreferences** Deze gelijke backreferences in the last match RewriteCond CondPattern en hebben de vorm %N (0 &lt;= N &lt;= 9).

Variabelen: Dit zijn variabelen van de vorm %{NAME_OF_VARIABLE} waar NAME_OF_VARIABLE een koord voor de naam van een bepaalde variabele is. Zie de markering *[E]* voor meer informatie over het instellen van omgevingsvariabelen.

Functies: Dit zijn functies van de vorm ${NAME_OF_FUNCTION:key} waar NAME_OF_FUNCTION het volgende is:

* met tolower worden alle tekens in *key* kleine letters gemaakt.
* toupper maakt alle tekens in *key* hoofdletters.
* escape URL-codeert alle tekens in *key*.
* De tekens &#39;a&#39;..z&#39;, &#39;A&#39;..&#39;Z&#39;, &#39;0&#39;..&#39;9&#39;, &#39;*&#39;, &#39;-&#39;, &#39;.&#39;, &#39;/&#39;, &#39;@&#39; en &#39;_&#39; worden niet gewijzigd; spaties worden omgezet in &#39;+&#39; en alle andere tekens worden getransformeerd naar hun %xx URL-gecodeerde equivalent.
* unescape transformeert &#39;+&#39; terug naar spatie en alle %xx URL-gecodeerde tekens terug naar één teken.

>[!NOTE]
>
>Er is een speciale vervangende tekenreeks: &quot;-&quot; betekent &quot;GEEN vervanging&quot;. De tekenreeks &#39;-&#39; wordt vaak gebruikt met de markering C (chain), zodat u een URL kunt koppelen aan verschillende patronen voordat een vervanging plaatsvindt.

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
   <td colname="col1"> <p> 'last|L' </p> </td> 
   <td colname="col2"> <p>Laatste regel. </p> <p>Stopt het herschrijfproces en past geen aanvullende herschrijfregels toe. Gebruik deze markering om verdere verwerking naar de huidige URL te voorkomen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'next|N' </p> </td> 
   <td colname="col2"> <p>Volgende ronde. </p> <p> Herstelt het herschrijfproces (opnieuw beginnend met de eerste het herschrijven regel) gebruikend URL van de laatste het herschrijven regel (niet originele URL). Zorg ervoor dat u geen impasse-lus maakt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'chain|C' </p> </td> 
   <td colname="col2"> <p>Bewerkt met volgende regel. </p> <p>Hiermee wordt de huidige regel geketend op de volgende regel (die ook aan de volgende regel kan worden gekoppeld, enzovoort). Als een regel overeenkomt, gaat het vervangingsproces zoals gewoonlijk verder. Als de regel niet overeenkomt, worden alle volgende regels in een keten overgeslagen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' </p> </td> 
   <td colname="col2"> <p>Geen geval. </p> <p> Maakt het patroon niet hoofdlettergevoelig (er is dus geen verschil tussen 'A-Z' en 'a-z') wanneer het patroon overeenkomt met de huidige URL. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'skip|S=num' </p> </td> 
   <td colname="col2"> <p>Sla de volgende regel of regels over. </p> <p> Als de huidige regel aanpast, dwingt deze vlag de herschrijfmotor om de volgende numregels in de regelreeks over te slaan. Gebruik deze markering om pseudo-if-then-else-constructs te maken. De laatste regel van toen-clausule wordt een skip=N waar N het aantal regels in de else-clausule is. </p> <p> <p>Opmerking:  Deze markering is niet hetzelfde als de markering 'chain|C'!) </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'env|E=VAR:VAL' </p> </td> 
   <td colname="col2"> <p>Hiermee wordt de omgevingsvariabele ingesteld. </p> <p>Maakt een omgevingsvariabele "VAR" die is ingesteld op de waarde VAL, waarbij VAL reguliere expressies backreferences, $N en %N kan bevatten, die worden uitgebreid. U kunt deze markering meerdere keren gebruiken om meerdere variabelen in te stellen. De variabelen kunnen later worden geschrapt-van verwijzingen voorzien in een volgend patroon RewriteCond via %{VAR}. </p> <p>Gebruik deze markering om informatie van URL's te verwijderen en te onthouden. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>De Opslag herschrijft Regels en terugwinnen herschrijft Regels delen veranderlijke waarden. Vanwege dit gedrag kunt u een variabele instellen op een tijdgevoelige sessionid-waarde wanneer een ingesloten URL wordt aangetroffen en opgeslagen. Wanneer de volgende URL wordt opgehaald uit de lijst met tijdelijke opslag, kan de laatste sessionid-waarde eraan worden toegevoegd voordat die pagina wordt opgehaald.

**Voorbeeld van een RewriteRule met een functie**

Veronderstel dat u een case-sensitive server hebt, die de koorden &quot;www.mydomain.com&quot;en &quot;www.MyDomain.com&quot;verschillend behandelt. Uw server werkt alleen correct als het domein altijd &quot;www.mydomain.com&quot; is, ook al bevatten sommige documenten koppelingen naar &quot;www.MyDomain.com&quot;. Hiervoor kunt u de volgende regel gebruiken:

```
RewriteRule  ^https:// 
<b>([^/]*)</b> 
<i>(.*)</i>$  https://${tolower:$1}$2
```

Deze herschrijfregel gebruikt de functie `tolower` om het domeingedeelte van een URL te herschrijven om ervoor te zorgen dat het altijd in kleine letters zoals in het volgende is:

1. Het patroon `(^https://([^/]*)(.*)$)` bevat een backreference ** `([^/]*)`** die alle karakters tussen `https://` en eerste `/` in URL aanpast. Het patroon bevat ook een tweede achterverwijzing `(.*)` die overeenkomt met alle resterende tekens in de URL.
1. De vervanging `(https://${tolower:$1}$2)` vertelt het onderzoeksmotor om URL te herschrijven door de `tolower` functie op de eerste backreference `(https:// ${tolower:$1}$2)` te gebruiken die de rest van URL onveranderd `(https://${tolower:$1} $2)` laat.

Zo wordt een URL van het formulier `https://www.MyDomain.com/INTRO/index.Html` herschreven als `https://www.mydomain.com/INTRO/index.Html`.

## Info over RewriteCond-instructies {#section_ADD642A24B68452CB98294A0BD687EC3}

De instructie RewriteCond definieert een regelvoorwaarde. Wanneer RewriteCond een RewriteRule voorafgaat, wordt de regel slechts gebruikt als zijn patroon de huidige titel aanpast en de extra voorwaarden van toepassing zijn. Herschrijfvoorwaarden hebben de volgende vorm:

```
           
<i>RewriteCond TestString CondPattern [Flags]</i> 
        
```

`TestString` is een tekenreeks die de volgende elementen kan bevatten:

Onbewerkte tekst: Tekst die ongewijzigd wordt doorgegeven.

Backreferences bieden toegang tot de gegroepeerde delen (tussen haakjes) van het Patroon of het CondPattern. Hier volgen de twee typen terugverwijzingen:

* **RewriteRule** BackreferencesDeze gelijke backreferences in het overeenkomstige RewriteRule Pattern en nemen de vorm $N (0  &lt;> Bijvoorbeeld, `RewriteRule ^https:// ([^/]*) (.*)$ https://${tolower: $1} $2`.

* **RewriteCond** BackreferencesDeze overeenkomsten backreferences in the last match RewriteCond Cond Cond Pattern en hebben de vorm %N (0&lt;>

Variabelen: Dit zijn variabelen van de vorm %{NAME_OF_VARIABLE} waar NAME_OF_VARIABLE een koord voor de naam van een bepaalde variabele kan zijn. Zie de markering RewriteRule *`[E]`* voor meer informatie over het plaatsen van variabelen.

Functies: Dit zijn functies van de vorm ${NAME_OF_FUNCTION:key} waar NAME_OF_FUNCTION het volgende is:

* met tolower worden alle tekens in *key* kleine letters gemaakt.
* toupper maakt alle tekens in *key* hoofdletters.
* escape URL-codeert alle tekens in sleutel. De tekens &#39;a&#39;..z&#39;, &#39;A&#39;..&#39;Z&#39;, &#39;0&#39;..&#39;9&#39;, &#39;*&#39;, &#39;-&#39;, &#39;.&#39;, &#39;/&#39;, &#39;@&#39; en &#39;_&#39; worden niet gewijzigd, spaties worden omgezet in &#39;+&#39; en alle andere tekens worden omgezet in hun equivalent voor %xx URL-codering.
* unescape transformeert &#39;+&#39; terug naar spatie en alle %xx URL-coderingstekens terug naar enkele tekens.

**** CondPatternis een standaard Extended Regular Expression met enkele toevoegingen. De patroontekenreeks kan worden voorafgegaan door een &#39;!&#39; teken (uitroepteken) om een patroon op te geven dat niet overeenkomt. In plaats van echte reguliere-expressietekenreeksen kunt u een van de volgende speciale varianten gebruiken:

>[!NOTE]
>
>U kunt al deze tests met een uitroepteken (&#39;!&#39;) ook vooraf instellen hun betekenis te negeren.

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
   <td colname="col2"> <p>Lexisch minder. </p> <p> Behandelt CondPattern als een onbewerkte tekenreeks en vergelijkt het lexicaal met TestString. True if TestString is lexically less than CondPattern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '&gt;CondPattern' </p> </td> 
   <td colname="col2"> <p>Lexisch groter. </p> <p> Behandelt CondPattern als een onbewerkte tekenreeks en vergelijkt het lexicaal met TestString. True als TestString lexically groter is dan CondPattern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '=CondPattern' </p> </td> 
   <td colname="col2"> <p>Lexisch gelijk. </p> <p> Behandelt CondPattern als een onbewerkte tekenreeks en vergelijkt het lexicaal met TestString. True if TestString is lexously gelijk aan CondPattern, dat wil zeggen, de twee tekenreeksen zijn exact gelijk (karakter door karakter). Als CondPattern enkel "" (twee aanhalingstekens) is, vergelijkt dit TestString met het lege koord. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Markeringen**
 (optioneel) Afsluiten markeringen tussen haakjes  `[]`. Meerdere markeringen worden gescheiden door komma&#39;s.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' </p> </td> 
   <td colname="col2"> <p> Geen geval. </p> <p>Deze vlag maakt de test niet hoofdlettergevoelig, namelijk is er geen verschil tussen "A-Z"en "a-z"zowel in uitgebreide TestString als in CondPattern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'ornext|OR' </p> </td> 
   <td colname="col2"> <p>Of volgende voorwaarde. </p> <p>Gebruik deze vlag om regelvoorwaarden met lokale OF in plaats van impliciete AND te combineren. Zonder deze vlag, zou u de cond/de regel veelvoudige tijden moeten schrijven. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Voorbeeld**

Sommige webpagina&#39;s wijzen de eerste keer dat een bezoeker bij een site aankomt, een CGI-variabele toe. Deze variabele wordt gebruikt om de bezoeker te identificeren en, aangezien de bezoeker door de plaats bladert, wordt de variabele overgegaan. Omdat de zoekrobot eruit ziet als een bezoeker van uw site, krijgt deze een sessionid-nummer toegewezen. De zoekrobot handhaaft deze enkele waarde voor sessionid, zelfs als een tweede sitepagina een nieuwe waarde probeert toe te wijzen. Om dit te verzekeren, hebt u twee herschrijven regels nodig.

De eerste regel wordt gebruikt om de sessionid-variabele te identificeren en op te slaan:

```
RewriteCond  %{sessionid}  !.+ 
RewriteRule  ^.+sessionid= 
<b>([^&#]+)</b>.*$  -   
<i>[E=sessionid:$1]</i>
```

RewriteRule gebruikt een E-vlag `([E=sessionid:$1])` om de huidige waarde van de zittende parameter CGI aan de variabele `sessionid` toe te wijzen. `$1` verwijst naar de eerste backreference, die tussen de eerste reeks haakjes in het Patroon van RewriteRule `([^&#]+)` bevat.

De reguliere expressie `^&#]+` komt overeen met het deel van een URL tussen het woord `sessionid` en het volgende **&amp;**of**#**teken. Aangezien deze RewriteRule slechts wordt gebruikt om de aanvankelijke waarde voor de sessionid variabele tot stand te brengen, herschrijft het niet. Merk op dat het gebied van de Vervanging van de regel aan `-` wordt geplaatst om erop te wijzen dat het herschrijven niet wordt vereist.

RewriteCond onderzoekt de variabele `sessionid` ( `%{sessionid}`). Als het zelfs geen enkel teken heeft (!.+), dan de overeenkomsten RewriteRule.

Met deze regel wordt de URL gelezen als `https://www.domain.com/home/?sessionid=1234&function=start` en wijst u de waarde `1234` toe aan de variabele `sessionid`.

De tweede regel wordt gebruikt om alle URL&#39;s te herschrijven die overeenkomen met het volgende RewriteRule-patroon:

```
RewriteRule   
<b>^(.+)</b>sessionid=[^&#]+ 
<i>(.*)$</i>  $1sessionid=%{sessionid}$2
```

Het patroon RewriteRule bevat twee terugverwijzingen: `(.+)` en `(.*)`. De eerste backreference komt overeen met alle tekens vóór `sessionid`. De tweede backreference komt overeen met alle tekens na het einde van `&` of `#`.

Het patroon van de Vervanging herschrijft URL gebruikend de eerste backreference, die door het koord &quot;sessionid=&quot;wordt gevolgd, door de waarde van de zittingidentiteitskaart variabele die door de eerste regel `%{sessionid}` wordt bepaald, door de tweede backreference wordt gevolgd. `($1sessionid=%{sessionid} $2)`

Bericht dat this RewriteRule geen RewriteCond bevat. Als dusdanig, veroorzaakt het herschrijven voor alle URLs die RewriteRule *Pattern* aanpassen. Als de waarde van de sessionid-variabele ( `%{sessionid}`) `1234` is, wordt een URL van het formulier `https://www.domain.com/products/?sessionid=5678&function=buy` herschreven als `https://www.domain.com/products/?sessionid=1234&function=buy`

## Toespraak {#section_EC3A1DAEB5A54C93A265CB119DF91E9F}

De software voor het herschrijven van engines is oorspronkelijk ontwikkeld door de Apache Group voor gebruik in het Apache HTTP-serverproject (https://www.apache.org/).

## Door de lijst voor horizontaal schuiven toe te voegen, worden URL-regels {#task_94A28ED7DC404BFF9767DBB5ADEE6B7A} opgehaald

U kunt toevoegen kruipt lijst wint URL regels terug om te specificeren hoe ontmoet URLs binnen Web inhoud wordt herschreven. Terugschrijfregels ophalen is alleen nodig als URL&#39;s dynamische gegevens bevatten, zoals een sessie-id, en als die dynamische gegevens in de loop der tijd veranderen om geldig te blijven.

<!-- 

t_adding_crawl_list_retrieve_url_rules.xml

 -->

**Om toe te voegen kruipt lijst wint URL-regels terug:**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Rewrite Rules]** > **[!UICONTROL Crawl List Retrieve URL Rules]**.
1. Voer in het veld [!DNL Crawl List Retrieve URL Rules] de gewenste regels in.

   Lege regels en commentaarregels die beginnen met een &#39;#&#39; (hash) teken zijn toegestaan.
1. (Optioneel) Voer in het veld [!DNL Test Crawl List Retrieve URL Rules] op de pagina [!DNL Crawl List Retrieve URL Rules] een test-URL in waarvan u de horizontaal schuivende regels wilt testen en klik op **[!UICONTROL Test]**.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Optioneel) Maak de gefaseerde site-index opnieuw als u een voorvertoning van de resultaten wilt zien.

   Zie [Een incrementele index van een gefaseerde website configureren](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Optioneel) Voer op de pagina [!DNL Crawl List Retrieve URL Rules] een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Informatie over de regels voor horizontaal schuiven {#concept_BD3A576987DA4D93A998B0B9CDDC3C79}

Met Titelregels horizontaal schuiven geeft u op hoe titels in webinhoud worden herschreven voordat ze in de zoekindex worden opgeslagen.

<!-- 

c_about_crawl_title_rules.xml

 -->

U kunt bijvoorbeeld een herschrijfregel gebruiken om een gedeelte van een titel, zoals een organisatienaam, te verwijderen. Wanneer een website wordt gekropen, worden aangetroffen titels opgeslagen in een tijdelijke buffer. Voordat echter een titel aan deze buffer wordt toegevoegd, worden de titelregels erop toegepast. Standaard heeft het zoeken/verhandelen van sites geen horizontaal schuivende titelregels en worden er geen titelwijzigingen aangebracht.

Voordat de effecten van de regels zichtbaar zijn voor klanten, moet u de index van uw site opnieuw samenstellen.

U kunt om het even welke veranderingen snel terugkeren u aanbrengt om de Regels van de Titel te kruipen door de eigenschap van de Geschiedenis te gebruiken.

De regels kunnen uit twee hoofdelementen bestaan: de RewriteRule en facultatieve RewriteCond. U kunt een onbeperkt aantal regels en voorwaarden opgeven. De orde van deze regels is belangrijk omdat de regel door regel wordt geplaatst. Wanneer een regel aanpast, het door om het even welke (facultatieve) overeenkomstige herschrijft voorwaarden van een lus voorziet. URL-regels voor horizontaal schuiven worden als volgt opgegeven:

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

Wanneer een titel wordt ontmoet, probeert de onderzoeksrobot om de titel aan het Patroon van elke kruiper regel aan te passen. Als het patroon overeenkomt, zoekt de engine voor herschrijven naar de overeenkomende richtlijnen voor herschrijvenCond. Als er geen voorwaarden aanwezig zijn, wordt de URL vervangen door een nieuwe waarde die wordt samengesteld uit de vervangende tekenreeks en gaat deze verder met de volgende regel in de regelset. Indien er voorwaarden bestaan, worden ze verwerkt in de volgorde waarin ze worden vermeld. De engine voor herschrijven probeert een voorwaardepatroon (CondPattern) af te stemmen op een testtekenreeks (TestString). Als de twee gelijke, dan wordt de volgende voorwaarde verwerkt tot geen meer voorwaarden beschikbaar zijn. Als alle voorwaarden overeenkomen, wordt de URL vervangen door de Substitutie die in de regel is opgegeven. Als niet aan de voorwaarde wordt voldaan, ontbreekt de volledige reeks voorwaarden en de overeenkomstige regel.

Voer de URL-regels voor horizontaal schuiven in het tekstvak in en klik op Wijzigingen opslaan. Lege regels en commentaarregels die beginnen met een &#39;#&#39; (hash) teken zijn toegestaan. Om de onderzoeksregels te testen, kunt u een test URL in het &quot;Test ingaan herschrijft Regels&quot;tekstvakje, en dan Test klikken.

## RewriteRule, instructie {#section_669445C505754E838E14029D6583D9B6}

Elke instructie RewriteRule definieert één herschrijfregel. Regels worden toegepast in de volgorde waarin ze worden weergegeven. Een herschrijfregel heeft de volgende vorm:

```
RewriteRule Pattern Substitution [Flags]
```

**Patroon** kan een reguliere POSIX-expressie zijn, die wordt toegepast op de huidige titel. De &quot;huidige titel&quot; verschilt van de oorspronkelijke titel, omdat eerdere regels er al op zijn afgestemd en gewijzigd.

Zie [Gewone uitdrukkingen](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

U kunt het teken &#39;not&#39; (&#39;!&#39;) gebruiken als u een voorvoegsel voor het patroon wilt toevoegen. Met het teken &#39;not&#39; kunt u een patroon negeren. Dit betekent dat u alleen waar hoeft te zijn als de huidige titel NIET overeenkomt met het patroon. Het teken &#39;not&#39; kan worden gebruikt wanneer een negatief patroon beter kan worden weergegeven of als een laatste standaardregel. Opmerking: U kunt niet zowel het teken &quot;niet&quot; als de gegroepeerde jokertekens in een patroon gebruiken. Bovendien kunt u geen ontkend patroon gebruiken wanneer het vervangingskoord `$N` bevat.

U kunt ronde haakjes gebruiken om een achterverwijzing te maken, waarnaar kan worden verwezen door de Vervangend en CondPattern.

Vervanging - De titel wordt vervangen door de vervangende tekenreeks. De tekenreeks kan het volgende bevatten:

Onbewerkte tekst - Tekst die ongewijzigd wordt doorgegeven.

Backreferences bieden toegang tot de gegroepeerde delen (tussen haakjes) van het Patroon of het CondPattern. Hieronder vindt u twee typen terugverwijzingen:

* RewriteRule Backreferences - Deze gelijke backreferences in het overeenkomstige Patroon RewriteRule en nemen de vorm $N (0 &lt;= N &lt;= 9).

   Bijvoorbeeld: `RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`

* RewriteCond Backreferences - Deze overeenkomsten backreferences in the last match RewriteCond Cond CondPattern en hebben de vorm %N (0 &lt;= N &lt;= 9).

Variabelen Dit zijn variabelen van de vorm %{NAME_OF_VARIABLE} waar NAME_OF_VARIABLE een tekenreeks voor de naam van een gedefinieerde variabele kan zijn. Zie de markering `[E]` voor meer informatie over het instellen van omgevingsvariabelen.

Functies Dit zijn functies van de vorm ${NAME_OF_FUNCTION: key} waarbij NAME_OF_FUNCTION is:

* met tolower worden alle tekens in *key* kleine letters gemaakt.
* toupper maakt alle tekens in *key* hoofdletters.

>[!NOTE]
>
>Er is een speciale vervangende tekenreeks: &quot;-&quot; betekent &quot;GEEN vervanging&quot;. De tekenreeks &#39;-&#39; is vaak handig met de markering C (chain), zodat u een titel kunt koppelen aan verschillende patronen voordat een vervanging plaatsvindt.

**Vlaggen**  (optioneel)

Vlaggen staan tussen haakjes `[]`en meerdere markeringen worden door komma&#39;s gescheiden:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'last|L' </p> </td> 
   <td colname="col2"> <p>Laatste regel. </p> <p> Stopt het herschrijfproces en past geen extra herschrijfregels toe. Gebruik deze markering om verdere verwerking tot de huidige titel te voorkomen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'next|N' </p> </td> 
   <td colname="col2"> <p>Volgende ronde. </p> <p> Herstelt het herschrijven proces (opnieuw beginnend met de eerste het herschrijven regel) gebruikend de titel van de laatste het herschrijven regel, niet de originele titel. Wees voorzichtig en maak geen dode lus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'chain|C' </p> </td> 
   <td colname="col2"> <p>Bewerkt met volgende regel. </p> <p>Hiermee wordt de huidige regel geketend op de volgende regel (die ook aan de volgende regel kan worden gekoppeld, enzovoort). Als een regel overeenkomt, gaat het vervangingsproces zoals gewoonlijk verder. Als de regel niet overeenkomt, worden alle volgende regels in een keten overgeslagen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' </p> </td> 
   <td colname="col2"> <p>Geen geval. </p> <p>Maakt het patroon niet hoofdlettergevoelig (er is dus geen verschil tussen 'A-Z' en 'a-z') wanneer het patroon overeenkomt met de huidige titel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'skip|S=num' </p> </td> 
   <td colname="col2"> <p>Volgende regel of regels overslaan. </p> <p> Als de huidige regel aanpast, dwingt deze vlag de herschrijfmotor om de volgende numregels in de regelreeks over te slaan. Gebruik dit om pseudo-if-then-else constructs te maken. De laatste regel van toen-clausule wordt een skip=N waar N het aantal regels in de else-clausule is. (Opmerking: Dit is niet hetzelfde als de markering 'chain|C'!) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'env|E=VAR:VAL' </p> </td> 
   <td colname="col2"> <p>Omgevingsvariabele instellen. </p> <p> Maakt een omgevingsvariabele "VAR" die is ingesteld op de waarde VAL, waarbij VAL reguliere expressies backreferences, $N en %N kan bevatten, die wordt uitgebreid. U kunt deze markering meerdere keren gebruiken om meerdere variabelen in te stellen. Er kan later naar de variabelen worden verwezen in het volgende RewriteCond-patroon via %{VAR}. Met deze markering kunt u gegevens uit titels verwijderen en onthouden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Richting herschrijvenCond (optioneel) {#section_D664B71DE3884E0790531804C49A3222}

De instructie RewriteCond definieert een regelvoorwaarde. Wanneer RewriteCond een RewriteRule voorafgaat, wordt de regel slechts gebruikt als zijn patroon de huidige titel aanpast en de extra voorwaarden van toepassing zijn.

Richtlijnen voor herschrijven van voorwaarden hebben de volgende vorm:

```
RewriteCond TestString CondPattern [Flags] 
```

**** TestString is een tekenreeks die de volgende constructies kan bevatten:

Onbewerkte tekst - Tekst die ongewijzigd wordt doorgegeven.

Backreferences bieden toegang tot de gegroepeerde delen (tussen haakjes) van het Patroon of het CondPattern. Er zijn twee typen terugverwijzingen:

* RewriteRule Backreferences - Deze gelijke backreferences in het overeenkomstige Patroon RewriteRule en nemen de vorm $N (0 &lt;= N &lt;= 9).

   Bijvoorbeeld: `RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`

* RewriteCond Backreferences - Deze overeenkomsten backreferences in the last match RewriteCond Cond CondPattern en hebben de vorm %N (0 &lt;= N &lt;= 9).

Variabelen Dit zijn variabelen van de vorm %{NAME_OF_VARIABLE} waar NAME_OF_VARIABLE een tekenreeks voor de naam van een gedefinieerde variabele kan zijn. Zie de markering `[E]` voor meer informatie over het instellen van omgevingsvariabelen.

Functies Dit zijn functies van de vorm ${NAME_OF_FUNCTION:key} waar NAME_OF_FUNCTION is:

* met tolower worden alle tekens in *key* kleine letters gemaakt.
* toupper maakt alle tekens in *key* hoofdletters.
* escape URL-codeert alle tekens in sleutel.
* De tekens &#39;a&#39;..z&#39;, &#39;A&#39;..&#39;Z&#39;, &#39;0&#39;..&#39;9&#39;, &#39;*&#39;, &#39;-&#39;, &#39;.&#39;, &#39;/&#39;, &#39;@&#39; en &#39;_&#39; worden niet gewijzigd, spaties worden omgezet in &#39;+&#39; en alle andere tekens worden omgezet in hun equivalent voor %xx URL-codering.
* unescape transformeert &#39;+&#39; terug naar spatie en alle %xx URL-gecodeerde tekens terug naar één teken.

**** CondPatternis een standaard Extended Regular Expression met enkele toevoegingen. De patroontekenreeks kan worden voorafgegaan door een &#39;!&#39; teken (uitroepteken) om een patroon op te geven dat niet overeenkomt. In plaats van echte reguliere-expressietekenreeksen kunt u een van de volgende speciale varianten gebruiken.

>[!NOTE]
>
>U kunt al deze tests met een uitroepteken (&#39;!&#39;) voorvoegsel geven hun betekenis te negeren.

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
   <td colname="col2"> <p>Is lexicaal minder. </p> <p>Behandelt <i>CondPattern</i> als een gewone tekenreeks en vergelijkt het lexicaal met <i>TestString</i>. True if <i>TestString</i> is lexically less than <i>CondPattern</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '&gt;CondPattern' </p> </td> 
   <td colname="col2"> <p>Is lexicaal groter. </p> <p>Behandelt <i>CondPattern</i> als een gewone tekenreeks en vergelijkt het lexicaal met <i>TestString</i>. True if <i>TestString</i> is lexically greater than <i>CondPattern</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '=CondPattern' </p> </td> 
   <td colname="col2"> <p> Is lexicaal gelijk. </p> <p>Behandelt <i>CondPattern</i> als een gewone tekenreeks en vergelijkt het lexicaal met <i>TestString</i>. True if <i>TestString</i> is lexically equal to <i>CondPattern</i>, that, the two strings are exact equal (character by character). Als <i>CondPattern</i> enkel "" (twee aanhalingstekens) is, vergelijkt dit <i>TestString</i> met het lege koord. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Vlaggen**  (optioneel)

Vlaggen staan tussen haakjes `[]`en meerdere markeringen worden door komma&#39;s gescheiden:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' </p> </td> 
   <td colname="col2"> <p>Geen geval. </p> <p> Maakt de test niet gevoelig. Er is dus geen verschil tussen 'A-Z' en 'a-z' in het uitgevouwen <i>TestString</i> en in het <i>CondPattern.</i> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'ornext|OR' </p> </td> 
   <td colname="col2"> <p> Of volgende voorwaarde. </p> <p>Gebruik deze vlag om regelvoorwaarden met lokale OF in plaats van impliciete AND te combineren. Zonder deze vlag, zou u de cond/de regel veelvoudige tijden moeten schrijven. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Voorbeeld**

Veronderstel dat u een collectieve Website met een standaardtitelformaat hebt: &quot;Mijn Bedrijf&quot;die door een koppelteken en dan een pagina-specifieke beschrijving wordt gevolgd (&quot;Mijn Bedrijf - Onthaal&quot;of &quot;Mijn Bedrijf - Nieuws&quot;, bijvoorbeeld). U wilt &quot;Mijn Bedrijf -&quot;van de titel schrappen en de volledige titel in hoofdletters omzetten wanneer het de plaats indexeert.

De volgende herschrijfregel gebruikt de functie toupper om alleen het beschrijvende gedeelte van een titel in hoofdletters te herschrijven:

```
RewriteRule  ^My[[:blank:]]Company[[:blank:]]-[[:blank:]] 
<b>(.*)</b>$  ${toupper: 
<b>$1</b>}
```

Het patroon van de regel

`(^My[[:blank:]]Company[[:blank:]]-[[:blank:]] (.*))`

bevat een backreference `(.*)` die de titelinhoud aanpast die &quot;Mijn Bedrijf-&quot;volgt. Houd er rekening mee dat de omringing van een gedeelte van een patroon met haakje ( ) een achterverwijzing maakt waarnaar door de Substitutie kan worden verwezen. In dit voorbeeld wordt de optie Vervangen

`(${toupper:**$1**})`

herschrijft die backreference (`**$1**`) gebruikend de toupperfunctie.

Zo wordt een titel van het formulier &quot;Mijn bedrijf - Welkom&quot; herschreven als &quot;WELCOME&quot;.

**Erkenning**

De software voor het herschrijven van engines is oorspronkelijk ontwikkeld door de Apache Group voor gebruik in het Apache HTTP-serverproject (https://www.apache.org/).

## De regels voor horizontaal schuivende titels toevoegen {#task_272BB4C603BA4C9ABDBEEB398798B101}

U kunt horizontaal schuivende titelregels toevoegen om op te geven hoe de aangetroffen titels in de webinhoud worden herschreven voordat ze in de zoekindex worden opgeslagen.

<!-- 

t_adding_crawl_title_rules.xml

 -->

**U voegt als volgt de regels voor horizontaal schuivende titels toe:**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Rewrite Rules]** > **[!UICONTROL Crawl Title Rules]**.
1. Voer in het veld [!DNL Crawl Title Rules] de gewenste regels in.

   Lege regels en commentaarregels die beginnen met een &#39;#&#39; (hash) teken zijn toegestaan.
1. (Optioneel) Voer in het veld [!DNL Test Crawl Title Rules] op de pagina [!DNL Crawl Title Rules] een test-URL in waarvan u de zoekregels wilt testen en klik vervolgens op **[!UICONTROL Test]**.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Optioneel) Maak de gefaseerde site-index opnieuw als u een voorvertoning van de resultaten wilt zien.

   Zie [Een incrementele index van een gefaseerde website configureren](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Optioneel) Voer op de pagina [!DNL Crawl Title Rules] een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Informatie over URL-regels zoeken {#concept_017EC95E68844B6C8CC9F874F0EC8D3C}

Zoeken in URL-regels geven aan hoe de URL&#39;s in de zoekresultaten van uw website moeten worden weergegeven. De regels werken op volledige URL&#39;s. Om het even welk gedeelte van URL kan worden gemanipuleerd, met inbegrip van vraagargumenten waar de informatie van zittingidentiteitskaart vaak wordt gehouden.

<!-- 

c_about_search_url_rules.xml

 -->

Doorgaans worden URL-regels voor zoeken gebruikt om een sessie-id in te voegen in een URL. U kunt URL-regels voor zoeken echter ook gebruiken om de domeinnaam te wijzigen die bij de resultaten wordt weergegeven. Standaard worden geen regels opgegeven en wordt geen URL-wijziging uitgevoerd.

URL-regels voor zoeken kunnen uit twee hoofdelementen bestaan: de RewriteRule en facultatieve RewriteCond. Wanneer een URL is opgenomen als onderdeel van een zoekresultaat, worden de regels gebruikt om deze te manipuleren. U kunt een onbeperkt aantal regels en voorwaarden voor de zoek-URL opgeven. De orde van deze regels is belangrijk omdat de regel wordt geplaatst door regel-voor-regel. Wanneer een regel aanpast, de softwarelijnen door om het even welke (facultatieve) overeenkomstige herschrijfvoorwaarden. URL-regels voor horizontaal schuiven worden als volgt opgegeven:

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

Bij het verwerken van een URL probeert het zoeken/verhandelen van de site deze aan te passen aan het patroon van elke zoekregel. Als de gelijke ontbreekt, houdt de herschrijfmotor onmiddellijk op verwerkend de regel en gaat met de volgende regel in de reeks verder. Als het patroon overeenkomt, zoekt de engine voor herschrijven naar de overeenkomstige instructies voor herschrijvenCond. Als er geen voorwaarden bestaan, wordt de URL vervangen door een nieuwe waarde. Deze waarde wordt geconstrueerd van het koord van de Vervanging en gaat met de volgende regel in de regelreeks verder. Als er voorwaarden bestaan, is de volgorde waarin ze worden vermeld de manier waarop ze worden verwerkt. De engine voor herschrijven probeert een voorwaardepatroon (CondPattern) af te stemmen op een testtekenreeks (TestString). Als de twee gelijke, dan wordt de volgende voorwaarde verwerkt tot geen meer voorwaarden beschikbaar zijn. Als alle voorwaarden overeenkomen, wordt de URL vervangen door de Substitutie die in de regel is opgegeven. Als niet aan de voorwaarde wordt voldaan, ontbreekt de volledige reeks voorwaarden en de overeenkomstige regel.

## Info over de instructie RewriteRule {#section_A3473B5B90B74DA1970213113A90591E}

Een herschrijfregel heeft de volgende vorm:

```
RewriteRule  
<i>Pattern Substitution [Flags]</i>
```

**Patroon** kan een reguliere POSIX-expressie zijn, die wordt toegepast op de huidige URL. De &quot;huidige URL&quot; kan afwijken van de oorspronkelijke URL, omdat eerdere regels mogelijk al overeenkomen en deze hebben gewijzigd.

Zie [Gewone uitdrukkingen](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

U kunt het teken &#39;not&#39; (&#39;!&#39;) gebruiken als u een voorvoegsel voor het patroon wilt toevoegen. Met het teken &#39;not&#39; kunt u een patroon negeren. Met andere woorden, het is alleen waar als de huidige URL NIET overeenkomt met het patroon. U kunt het teken &#39;not&#39; gebruiken wanneer het beter is om een negatief patroon aan te passen, of als laatste standaardregel. U kunt niet zowel het teken &quot;niet&quot; als de gegroepeerde jokertekens in een patroon gebruiken. Daarnaast kunt u geen negatiefpatroon gebruiken wanneer de vervangende tekenreeks $N bevat.

U kunt ronde haakjes gebruiken om een achterverwijzing te maken, waarnaar kan worden verwezen door de Vervangend en CondPattern.

**** VervangingDe URL wordt volledig vervangen door de vervangende tekenreeks, die het volgende kan bevatten:

Onbewerkte tekst - Tekst die ongewijzigd wordt doorgegeven.

Backreferences biedt toegang tot de gegroepeerde onderdelen (tussen haakjes) van het patroon of het patroon. Er zijn twee typen terugverwijzingen:

RewriteRule Backreferences Deze gelijke backreferences in het overeenkomstige Patroon RewriteRule en nemen de vorm $N (0 &lt;= N &lt;= 9). Bijvoorbeeld: `RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`

RewriteCond Backreferences - Deze overeenkomsten backreferences in the last match RewriteCond Cond CondPattern en hebben de vorm %N (0 &lt;= N &lt;= 9).

Functies: Dit zijn functies van de vorm ${NAME_OF_FUNCTION:key} waar NAME_OF_FUNCTION is:

* met tolower worden alle tekens in *key* kleine letters gemaakt.
* toupper maakt alle tekens in *key* hoofdletters.
* escape URL-codeert alle tekens in *key*.
* De tekens &#39;a&#39;..z&#39;, &#39;A&#39;..&#39;Z&#39;, &#39;0&#39;..&#39;9&#39;, &#39;*&#39;, &#39;-&#39;, &#39;.&#39;, &#39;/&#39;, &#39;@&#39; en &#39;_&#39; worden niet gewijzigd; spaties worden vertaald naar &#39;+&#39;; alle andere tekens worden getransformeerd naar hun equivalent voor %xx URL-codering.
* unescape transformeert &#39;+&#39; terug naar spatie en alle %xx URL-gecodeerde tekens terug naar één teken.

>[!NOTE]
>
>Er is een speciale vervangende tekenreeks: &quot;-&quot; betekent &quot;GEEN vervanging&quot;. De tekenreeks &#39;-&#39; is vaak nuttig in combinatie met de markering C (chain). Hiermee kunt u een URL afstemmen op verschillende patronen voordat een vervanging plaatsvindt.

**Vlaggen**  (optioneel)

Vlaggen staan tussen haakjes `[]`en meerdere markeringen worden door komma&#39;s gescheiden:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'last|L' </p> </td> 
   <td colname="col2"> <p>Laatste regel. </p> <p> Stop het herschrijven proces en pas geen extra het herschrijven regels toe. Gebruik deze markering om verdere verwerking naar de huidige URL te voorkomen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'next|N' </p> </td> 
   <td colname="col2"> <p> Volgende ronde. </p> <p>Voer het herschrijfproces opnieuw uit (opnieuw te beginnen met de eerste herschrijfregel) met de URL van de laatste herschrijfregel (niet de oorspronkelijke URL). Wees voorzichtig en maak geen dode lus! </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'chain|C' </p> </td> 
   <td colname="col2"> <p> Bewerkt met volgende regel. </p> <p>Deze vlag ketent de huidige regel aan de volgende regel, die ook aan zijn volgende regel kan worden geketend, etc. Als een regel overeenkomt, gaat het vervangingsproces zoals gewoonlijk verder. Als de regel niet overeenkomt, worden alle volgende regels in een keten overgeslagen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' </p> </td> 
   <td colname="col2"> <p>Geen geval. </p> <p>Met deze markering is het patroon niet hoofdlettergevoelig. Met andere woorden, er is geen verschil tussen 'A-Z' en 'a-z' wanneer het patroon overeenkomt met de huidige URL. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'skip|S=num' </p> </td> 
   <td colname="col2"> <p>Volgende regel of regels overslaan. </p> <p> Als de huidige regel aanpast, dwingt deze vlag de herschrijfmotor om de volgende numregels in de regelreeks over te slaan. Gebruik dit om pseudo-if-then-else constructs te maken. De laatste regel van toen-clausule wordt een skip=N waar N het aantal regels in de else-clausule is. (Opmerking: Dit is niet hetzelfde als de markering 'chain|C'!) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'env|E=VAR:VAL' </p> </td> 
   <td colname="col2"> <p>Omgevingsvariabele instellen. </p> <p> Deze markering maakt een omgevingsvariabele "VAR" die op de waarde VAL wordt ingesteld. VAL kan reguliere expressies backreferences, $N en %N bevatten, die worden uitgebreid. U kunt deze markering meerdere keren gebruiken om meerdere variabelen in te stellen. De variabelen kunnen later worden geschrapt-van verwijzingen voorzien in een volgend patroon RewriteCond via %{VAR}. Gebruik deze markering om informatie van URL's te verwijderen en te onthouden. </p> </td> 
  </tr> 
 </tbody> 
</table>

Merk op dat de Opslag herschrijft Regels en terugwinnen herschrijft Regels veranderlijke waarden delen. Hierdoor kunt u een variabele instellen op een tijdgevoelige sessionid-waarde wanneer een ingesloten URL wordt aangetroffen en opgeslagen. Wanneer de volgende URL wordt opgehaald uit de lijst met tijdelijke opslag, kan de laatste sessionid-waarde eraan worden toegevoegd voordat die pagina wordt opgehaald.

**Voorbeeld**

Stel dat u een hoofdlettergevoelige server hebt. De tekenreeksen &quot;www.mydomain.com&quot; en &quot;www.MyDomain.com&quot; worden anders verwerkt. Om uw server correct te laten werken, moet u ervoor zorgen dat het domein altijd &quot;www.mydomain.com&quot;is alhoewel sommige documenten verbindingen bevatten die &quot;www.MyDomain.com&quot;van verwijzingen voorzien. Hiervoor kunt u de volgende regel gebruiken:

```
RewriteRule  ^https:// 
<b>([^/]*)</b> 
<i>(.*)</i>$  https://${tolower:$1}$2 
```

Deze herschrijfregel gebruikt de functie &quot;tolower&quot; om het domeingedeelte van een URL te herschrijven zodat deze altijd in kleine letters is:

1. Het patroon `(^https://([^/]*)(.*)$)` bevat een backreference **`([^/]*)`** die alle karakters tussen &quot;https://&quot;en eerste &quot;/&quot;in URL aanpast. Het patroon bevat ook een tweede backreference **(.*)** die alle resterende karakters in URL aanpast.

1. De vervanging `(https://${tolower:$1}$2)` vertelt het onderzoeksmotor om URL te herschrijven door de **tolower** functie op de eerste backreference `(https://**${tolower:$1**}$2)` te gebruiken die de rest van URL onveranderd `(https://${tolower:$1}*$2*)` laat.

Daarom wordt een URL van het formulier `https://www.MyDomain.com/INTRO/index.Html` herschreven als `https://www.mydomain.com/INTRO/index.Html`

**Cond Directive**  herschrijven (optioneel)

De instructie RewriteCond definieert een regelvoorwaarde. Wanneer RewriteCond een RewriteRule voorafgaat, wordt de regel slechts gebruikt als zijn patroon de huidige titel aanpast en de extra voorwaarden van toepassing zijn.

Richtlijnen voor herschrijven van voorwaarden hebben de volgende vorm:

```
RewriteCond  
<i>TestString CondPattern [Flags]</i>
```

** TestString is een tekenreeks die de volgende constructies kan bevatten:

Onbewerkte tekst: Tekst die ongewijzigd wordt doorgegeven.

Backreferences bieden toegang tot de gegroepeerde delen (tussen haakjes) van het Patroon of het CondPattern. Er zijn twee typen terugverwijzingen:

* RewriteRule Backreferences - Deze gelijke backreferences in het overeenkomstige Patroon RewriteRule en nemen de vorm $N (0 &lt;= N &lt;= 9).

   Bijvoorbeeld: `RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`

* RewriteCond Backreferences - Deze overeenkomsten backreferences in the last match RewriteCond Cond CondPattern en hebben de vorm %N (0 &lt;= N &lt;= 9).

Variabelen Dit zijn variabelen van de vorm %{NAME_OF_VARIABLE} waar NAME_OF_VARIABLE een tekenreeks voor de naam van een gedefinieerde variabele kan zijn. Zie de markering RewriteRule *`[E]`* voor meer informatie over het plaatsen van variabelen.

>[!NOTE]
>
>Regels voor herschrijven maken over het algemeen gebruik van variabelen. Alle CGI-parameters van de huidige URL worden automatisch omgezet in variabelen. Bijvoorbeeld, verstrekt het onderzoek URL `"https://search.atomz.com/search/?sp_a=sp00000000&sp_q="Product"&session=1234&id=5678"` automatisch vier variabelen, die in herschrijven regels kunnen worden van verwijzingen voorzien. In dit voorbeeld wordt één variabele &quot;session&quot; genoemd en de waarde ervan is &quot;1234&quot;, terwijl een andere variabele &quot;id&quot; wordt genoemd en de waarde &quot;5678&quot; is. (De andere twee variabelen zijn `sp_a` en `sp_q`.) U moet alle benodigde variabelen als verborgen velden doorgeven vanuit het zoekformulier op uw webpagina. In dit voorbeeld, zou u de &quot;zitting&quot;en &quot;identiteitskaart&quot;waarden moeten overgaan, die de gebruiker identificeren van de Website die het onderzoek uitvoert. Als u een verborgen veld wilt doorgeven op het zoekformulier, gebruikt u een tag zoals `<input type=hidden name="session" value="1234">`.

Functies Dit zijn functies van de vorm ${NAME_OF_FUNCTION:key} waar NAME_OF_FUNCTION is:

* met tolower worden alle tekens in *key* kleine letters gemaakt.
* toupper maakt alle tekens in *key* hoofdletters.
* escape URL-codeert alle tekens in *key*. De tekens &#39;a&#39;..z&#39;, &#39;A&#39;..&#39;Z&#39;, &#39;0&#39;..&#39;9&#39;, &#39;*&#39;, &#39;-&#39;, &#39;.&#39;, &#39;/&#39;, &#39;@&#39; en &#39;_&#39; worden niet gewijzigd, spaties worden omgezet in &#39;+&#39; en alle andere tekens worden omgezet in hun equivalent voor %xx URL-codering.
* unescape transformeert &#39;+&#39; terug naar spatie en alle %xx URL-coderingstekens terug naar enkele tekens.

**** CondPatternis een standaard Extended Regular Expression met enkele toevoegingen. De patroontekenreeks kan worden voorafgegaan door een &#39;!&#39; teken (uitroepteken) om een patroon op te geven dat niet overeenkomt. In plaats van echte reguliere-expressietekenreeksen kunt u een van de volgende speciale varianten gebruiken.

U kunt al deze tests door een uitroepteken (&#39;!&#39;) vóór te gaan gebruiken hun betekenis te negeren.

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
   <td colname="col2"> <p>Is lexicaal minder. </p> <p> Behandelt <i>CondPattern</i> als een gewone tekenreeks en vergelijkt het lexicaal met <i>TestString</i>. True if <i>TestString</i> is lexically less than <i>CondPattern</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '&gt;CondPattern' </p> </td> 
   <td colname="col2"> <p>Is lexicaal groter. </p> <p> Behandelt <i>CondPattern</i> als een gewone tekenreeks en vergelijkt het lexicaal met <i>TestString</i>. True if <i>TestString</i> is lexically greater than <i>CondPattern</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '=CondPattern' </p> </td> 
   <td colname="col2"> <p>Is lexicaal gelijk. </p> <p> Behandelt <i>CondPattern</i> als een gewone tekenreeks en vergelijkt het lexicaal met <i>TestString</i>. True if <i>TestString</i> is lexically equal to <i>CondPattern</i>. De twee tekenreeksen zijn dus exact gelijk (teken voor teken). Als <i>CondPattern</i> enkel "" (twee aanhalingstekens) is, vergelijkt dit <i>TestString</i> met het lege koord. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Vlaggen**  (optioneel)

Vlaggen staan tussen haakjes `[]`en meerdere markeringen worden door komma&#39;s gescheiden:

&#39;nocase|NC&#39; (geen geval): Hierdoor is de test niet hoofdlettergevoelig. Met andere woorden, er is geen verschil tussen &#39;A-Z&#39; en &#39;a-z&#39; zowel in de uitgevouwen *TestString* als in de *CondPattern*.

&#39;or next|OR&#39; (of volgende voorwaarde): Gebruik dit om regelvoorwaarden met lokale OF in plaats van impliciete AND te combineren. Zonder deze vlag zou u de voorwaarde/de regel veelvoudige tijden moeten schrijven.

**Voorbeeld**

Sommige Web-pagina&#39;s wijzen een &quot;sessionid&quot;CGI variabele toe de eerste keer een klant bij een plaats aankomt. Deze variabele wordt gebruikt om de klant te identificeren en, aangezien de klant door de plaats doorbladert, wordt de variabele overgegaan. Omdat de zoekrobot eruit ziet als een klant voor uw site, krijgt deze een sessionid-nummer toegewezen. De zoekrobot handhaaft deze enkele waarde voor sessionid, zelfs als een tweede sitepagina een nieuwe waarde probeert toe te wijzen. Om dit te verzekeren, hebt u de volgende herschrijfregel nodig:

```
RewriteCond  %{sessionid}  .+ 
RewriteRule  ^ 
<b>(.+)</b>sessionid=[^&#]+ 
<i>(.*)</i>$   
<b>$1</b>sessionid=%{sessionid} 
<i>$2</i>
```

Het patroon RewriteRule bevat twee terugverwijzingen: (.+) en (.*). De eerste backreference komt overeen met alle tekens vóór &quot;sessionid=&quot;. De tweede backreference komt overeen met alle tekens nadat de sessionid &#39;&amp;&#39; of &#39;#&#39; heeft beëindigd.

Het patroon van de Vervanging herschrijft URL gebruikend de eerste backreference, die door het koord &quot;sessionid=&quot;wordt gevolgd, door de waarde van de zittingidentiteitskaart variabele, die als parameter CGI in URL werd overgegaan, die door de tweede backreference wordt gevolgd. `($1sessionid=%{sessionid}$2)`.

**RewriteCond** onderzoekt veranderlijke sessionid `(%{sessionid})`. Als het ten minste één teken bevat (.+), dan de overeenkomsten RewriteRule.

Als de zoekquery dus `"https://search.atomz.com/search/?sp_a=sp99999999&sp_q=word&sessionid=5678"` is, worden alle URL&#39;s van zoekresultaten herschreven zodat de waarde &quot;sessionid&quot; 5678 is in plaats van de waarde &quot;sessionid&quot; die de zoekrobot tegenkwam toen deze door uw site kruipde en de koppelingen opsloeg.

**Erkenning**

De software voor het herschrijven van engines is oorspronkelijk ontwikkeld door de Apache Group voor gebruik in het Apache HTTP-serverproject (https://www.apache.org/).

## URL-regels voor zoeken toevoegen {#task_50C77D1B53804AEEB20896F74265BD6F}

U kunt URL-regels voor zoeken toevoegen om op te geven hoe de URL&#39;s in de zoekresultaten van uw website worden weergegeven. De regels werken op volledige URL&#39;s. U kunt om het even welk gedeelte van URL manipuleren, met inbegrip van vraagargumenten waar de informatie van zittingidentiteitskaart vaak wordt gehouden.

<!-- 

t_adding_search_url_rules.xml

 -->

**URL-regels voor zoeken toevoegen:**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Rewrite Rules]** > **[!UICONTROL Search URL Rules]**.
1. Voer in het veld [!DNL Search URL Rules] de gewenste regels in.

   Lege regels en commentaarregels die beginnen met een &#39;#&#39; (hash) teken zijn toegestaan.

1. (Optioneel) Voer in het veld [!DNL Test Search URL Rules] op de pagina [!DNL Search URL Rules] een test-URL in waarvan u de horizontaal schuivende regels wilt testen en klik op **[!UICONTROL Test]**.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Optioneel) Maak de gefaseerde site-index opnieuw als u een voorvertoning van de resultaten wilt zien.

   Zie [Een incrementele index van een gefaseerde website configureren](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Optioneel) Voer op de pagina [!DNL Search URL Rules] een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Info over Regels voor zoektitels {#concept_C72D20F8DFF64EDE809AF4B72797E858}

De Regels van de Titel van het onderzoek specificeren hoe de titels in uw Website onderzoeksresultaten worden getoond. Elk gedeelte van de titel kan worden gemanipuleerd.

<!-- 

c_about_search_title_rules.xml

 -->

Een herschrijfregel kan worden gebruikt om een gedeelte van een titel te verwijderen, zoals bijvoorbeeld een organisatienaam. Standaard gelden voor zoeken/verhandelen van sites geen titelregels en worden er geen titelwijzigingen aangebracht.

De titelregels kunnen uit twee hoofdelementen bestaan: de RewriteRule en facultatieve RewriteCond. Een onbeperkt aantal regels en voorwaarden kan worden gespecificeerd. De volgorde van deze regels is belangrijk, omdat de regel via regel wordt doorlopen. Wanneer een regel aanpast, de softwarelijnen door om het even welke (facultatieve) overeenkomstige herschrijfvoorwaarden. De regels voor zoektitels zijn als volgt opgegeven:

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

Wanneer een titel wordt ontmoet, probeert het plaatsonderzoek/het koopproces om het aan het Patroon van elke kruiperregel aan te passen. Als het patroon overeenkomt, zoekt de engine voor herschrijven naar de overeenkomende richtlijnen voor herschrijvenCond. Als er geen voorwaarden aanwezig zijn, wordt de titel vervangen door een nieuwe waarde die wordt samengesteld uit de vervangende tekenreeks en gaat deze verder met de volgende regel in de regelset. Indien er voorwaarden bestaan, worden ze verwerkt in de volgorde waarin ze worden vermeld. De engine voor herschrijven probeert een voorwaardepatroon (CondPattern) af te stemmen op een testtekenreeks (TestString). Als de twee gelijke, dan wordt de volgende voorwaarde verwerkt tot geen meer voorwaarden beschikbaar zijn. Als alle voorwaarden overeenkomen, wordt de URL vervangen door de Substitutie die in de regel is opgegeven. Als niet aan de voorwaarde wordt voldaan, ontbreekt de volledige reeks voorwaarden en de overeenkomstige regel.

## Directive {#section_3BF2B0FF89F74A26AE79D68FA3184B9B} herschrijven

Elke instructie RewriteRule definieert één herschrijfregel. Regels worden toegepast in de volgorde waarin ze worden weergegeven. Een herschrijfregel heeft de volgende vorm:

```
RewriteRule Pattern Substitution [Flags]
```

**De reguliere expressie** PatternA POSIX, die wordt toegepast op de huidige titel. De &quot;huidige titel&quot; kan afwijken van de oorspronkelijke titel, omdat eerdere regels mogelijk al zijn aangepast en gewijzigd.

Zie [Gewone uitdrukkingen](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

U kunt het teken &#39;&#39;not&#39;&#39; gebruiken. als u een voorvoegsel voor het patroon wilt toevoegen. Met het teken &#39;not&#39; kunt u een patroon negeren. Dat wil zeggen dat de huidige titel NIET overeenkomt met het patroon. Het teken &#39;not&#39; kan worden gebruikt wanneer een negatief patroon beter kan worden weergegeven of als een laatste standaardregel. Opmerking: U kunt niet zowel het teken &quot;niet&quot; als de gegroepeerde jokertekens in een patroon gebruiken. Daarnaast kunt u geen negatiefpatroon gebruiken wanneer de vervangende tekenreeks $N bevat.

U kunt ronde haakjes gebruiken om een achterverwijzing te maken, waarnaar kan worden verwezen door de Vervangend en CondPattern.

**** SubstitutionDe titel wordt volledig vervangen door de substitutiereeks, die het volgende kan bevatten:

Onbewerkte tekst - Tekst die ongewijzigd wordt doorgegeven.

* Backreferences - Biedt toegang tot de gegroepeerde onderdelen (tussen haakjes) van het Patroon of CondPattern. Hieronder vindt u twee typen terugverwijzingen:

* RewriteRule Backreferences - Deze gelijke backreferences in het overeenkomstige Patroon RewriteRule en nemen de vorm $N (0 &lt;= N &lt;= 9).

   Bijvoorbeeld: `RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`

* ** HerwriteCond Backreferences** Deze gelijke backreferences in the last match RewriteCond CondPattern en hebben de vorm %N (0 &lt;= N &lt;= 9).

**** VariabelenDit zijn variabelen van de vorm %{NAME_OF_VARIABLE} waar NAME_OF_VARIABLE een koord voor de naam van een bepaalde variabele kan zijn. Zie de markering [E] voor meer informatie over het instellen van omgevingsvariabelen. Variabelen kunnen ook worden gedefinieerd in het zoekformulier dat de zoekresultaten heeft gegenereerd.

**** FunctionsThis zijn functies van de vorm ${NAME_OF_FUNCTION: key} waarbij NAME_OF_FUNCTION is:

* met tolower worden alle tekens in *key* kleine letters gemaakt.
* toupper maakt alle tekens in *key* hoofdletters.

Er is een speciale vervangende tekenreeks: &quot;-&quot; betekent &quot;GEEN vervanging&quot;. De tekenreeks &#39;-&#39; is vaak handig in combinatie met de markering C (chain), zodat u een titel kunt koppelen aan verschillende patronen voordat een vervanging plaatsvindt.

**Vlaggen**  (optioneel)

Vlaggen staan tussen haakjes `[]` en meerdere markeringen worden door komma&#39;s gescheiden:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'last|L' </p> </td> 
   <td colname="col2"> <p> Laatste regel. </p> <p> Stop het herschrijven proces en pas geen extra het herschrijven regels toe. Gebruik deze markering om verdere verwerking tot de huidige titel te voorkomen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'next|N' </p> </td> 
   <td colname="col2"> <p>Volgende ronde. </p> <p> Voer het herschrijfproces opnieuw uit (opnieuw te beginnen met de eerste herschrijfregel) met gebruik van de titel van de laatste herschrijfregel (niet de oorspronkelijke titel!). Wees voorzichtig en maak geen dode lus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'chain|C' </p> </td> 
   <td colname="col2"> <p>Bewerkt met volgende regel. </p> <p> Deze vlag ketent de huidige regel aan de volgende regel (die ook aan zijn volgende regel kan worden geketend, etc.). Als een regel overeenkomt, gaat het vervangingsproces zoals gewoonlijk verder. Als de regel niet overeenkomt, worden alle volgende regels in een keten overgeslagen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' </p> </td> 
   <td colname="col2"> <p> Geen geval. </p> <p> Met deze markering is het patroon niet hoofdlettergevoelig. Er is dus geen verschil tussen 'A-Z' en 'a-z' wanneer het patroon overeenkomt met de huidige titel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'skip|S=num' </p> </td> 
   <td colname="col2"> <p> Volgende regel of regels overslaan. </p> <p> Als de huidige regel aanpast, dwingt deze vlag de herschrijfmotor om de volgende numregels in de regelreeks over te slaan. Gebruik dit om pseudo-if-then-else constructs te maken. De laatste regel van toen-clausule wordt een skip=N waar N het aantal regels in de else-clausule is. (Dit is niet hetzelfde als de markering 'chain|C'!) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'env|E=VAR:VAL' </p> </td> 
   <td colname="col2"> <p>Omgevingsvariabele instellen. </p> <p> Deze markering leidt tot een omgevingsvariabele "VAR"die aan de waarde VAL wordt geplaatst, waar VAL regelmatige uitdrukkingen backreferences, $N en %N kan bevatten, die zullen worden uitgebreid. U kunt deze markering meerdere keren gebruiken om meerdere variabelen in te stellen. Er kan later naar de variabelen worden verwezen in het volgende RewriteCond-patroon via %{VAR}. Met deze markering kunt u gegevens uit titels verwijderen en onthouden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Richting herschrijvenCond (optioneel) {#section_9D72B2AB454849A7B681BC39C506AAA3}

De instructie RewriteCond definieert een regelvoorwaarde. Wanneer RewriteCond een RewriteRule voorafgaat, wordt de regel slechts gebruikt als zijn patroon de huidige titel aanpast en de extra voorwaarden van toepassing zijn.

Richtlijnen voor herschrijven van voorwaarden hebben de volgende vorm:

```
RewriteCond TestString CondPattern [Flags]
```

**** TestString is een tekenreeks die de volgende constructies kan bevatten:

Onbewerkte tekst - Tekst die ongewijzigd wordt doorgegeven.

Backreferences bieden toegang tot de gegroepeerde delen (tussen haakjes) van het Patroon of het CondPattern. Er zijn twee typen terugverwijzingen:

* RewriteRule Backreferences - Deze gelijke backreferences in het overeenkomstige Patroon RewriteRule en nemen de vorm $N (0 &lt;= N &lt;= 9).

   Bijvoorbeeld: `RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`

* RewriteCond Backreferences - Deze overeenkomsten backreferences in the last match RewriteCond Cond CondPattern en hebben de vorm %N (0 &lt;= N &lt;= 9).

**** VariabelenDit zijn variabelen van de vorm %{NAME_OF_VARIABLE} waar NAME_OF_VARIABLE een koord voor de naam van een bepaalde variabele kan zijn. Zie de markering `[E]` voor meer informatie over het instellen van omgevingsvariabelen. Variabelen kunnen ook worden gedefinieerd in het zoekformulier dat de zoekresultaten heeft gegenereerd.

**** FunctiesDit zijn functies van de vorm ${NAME_OF_FUNCTION:key} waar NAME_OF_FUNCTION is:

* met tolower worden alle tekens in *key* kleine letters gemaakt.
* toupper maakt alle tekens in *key* hoofdletters.
* escape URL-codeert alle tekens in *key*.
* De tekens &#39;a&#39;..z&#39;, &#39;A&#39;..&#39;Z&#39;, &#39;0&#39;..&#39;9&#39;, &#39;*&#39;, &#39;-&#39;, &#39;.&#39;, &#39;/&#39;, &#39;@&#39; en &#39;_&#39; worden niet gewijzigd, spaties worden omgezet in &#39;+&#39; en alle andere tekens worden omgezet in hun equivalent voor %xx URL-codering.
* unescape transformeert &#39;+&#39; terug naar spatie en alle %xx URL-gecodeerde tekens terug naar één teken.

Er is een speciale vervangende tekenreeks: &quot;-&quot; betekent &quot;GEEN vervanging&quot;. De tekenreeks &#39;-&#39; is vaak handig in combinatie met de markering C (chain), zodat u een URL kunt koppelen aan verschillende patronen voordat een vervanging plaatsvindt.

**** CondPatternA standaard Extended Regular Expression with some additions. De patroontekenreeks kan worden voorafgegaan door een &#39;!&#39; teken (uitroepteken) om een patroon op te geven dat niet overeenkomt. In plaats van echte reguliere-expressietekenreeksen kunt u een van de volgende speciale varianten gebruiken.

Al deze tests kunnen ook worden voorafgegaan door een uitroepteken (&#39;!&#39;) hun betekenis te negeren.

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
   <td colname="col2"> <p>Is lexicaal minder. </p> <p> Behandelt <i>CondPattern</i> als een gewone tekenreeks en vergelijkt het lexicaal met <i>TestString</i>. True if <i>TestString</i> is lexically less than <i>CondPattern</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '&gt;CondPattern' </p> </td> 
   <td colname="col2"> <p> Is lexicaal groter. </p> <p> Behandelt <i>CondPattern</i> als een gewone tekenreeks en vergelijkt het lexicaal met <i>TestString</i>. True if <i>TestString</i> is lexically greater than <i>CondPattern</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '=CondPattern' </p> </td> 
   <td colname="col2"> <p>Is lexicaal gelijk. </p> <p> Behandelt <i>CondPattern</i> als een gewone tekenreeks en vergelijkt het lexicaal met <i>TestString</i>. True if <i>TestString</i> is lexically equal to <i>CondPattern</i>. De twee tekenreeksen zijn dus exact gelijk (teken voor teken). Als <i>CondPattern</i> enkel "" (twee aanhalingstekens) is, vergelijkt dit <i>TestString</i> met het lege koord. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Vlaggen**  (optioneel)

Vlaggen staan tussen haakjes`[]` en meerdere markeringen worden gescheiden door komma&#39;s:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Markering </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' (geen geval) </p> </td> 
   <td colname="col2"> <p>Maakt de test niet gevoelig. Er is dus geen verschil tussen 'A-Z' en 'a-z' in de uitgevouwen <i>TestString</i> en in de <i>CondPattern</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'or next|OR' (of volgende voorwaarde) </p> </td> 
   <td colname="col2"> <p> Gebruik dit om regelvoorwaarden met lokale OF in plaats van impliciete AND te combineren. Zonder deze vlag zou u de voorwaarde/de regel veelvoudige tijden moeten schrijven. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Voorbeeld {#section_E7454FFE169E459AABD9D033651939CB}

Veronderstel dat u een collectieve Website met een standaardtitelformaat hebt: &quot;Mijn Bedrijf&quot;die door een koppelteken en dan een pagina-specifieke beschrijving wordt gevolgd (&quot;Mijn Bedrijf - Onthaal&quot;of &quot;Mijn Bedrijf - Nieuws&quot;, bijvoorbeeld). U wilt &quot;Mijn Bedrijf -&quot;van de titel schrappen en de volledige titel in hoofdletters omzetten wanneer het de plaats indexeert.

De volgende herschrijfregel gebruikt de functie toupper om alleen het beschrijvende gedeelte van een titel in hoofdletters te herschrijven:

```
RewriteRule  ^My[[:blank:]]Company[[:blank:]]-[[:blank:]] 
<b>(.*)</b>$  ${toupper: 
<b>$1</b>} 
```

Het patroon van de regel `(^My[[:blank:]]Company[[:blank:]]-[[:blank:]] (.*))` bevat een backreference **`(.*)`** die de titelinhoud aanpast die &quot;Mijn Bedrijf-&quot;volgt. Houd er rekening mee dat de omringing van een gedeelte van een patroon met haakje ( ) een achterverwijzing maakt waarnaar door de Substitutie kan worden verwezen. In dit voorbeeld wordt de optie Vervangen

`(${toupper:**$1**})`

herschrijft die backreference (**$1**) gebruikend de toupperfunctie.

Zo wordt een titel van het formulier &quot;Mijn bedrijf - Welkom&quot; herschreven als &quot;WELCOME&quot;.

**Erkenning**

De software voor het herschrijven van engines is oorspronkelijk ontwikkeld door de Apache Group voor gebruik in het Apache HTTP-serverproject (https://www.apache.org/).

## Regels voor zoektitels toevoegen {#task_155CECB74BE3444384EDBBD04F41515E}

U kunt regels voor zoektitels toevoegen om op te geven hoe titels in de zoekresultaten van uw website worden weergegeven. U kunt elk gedeelte van de titel manipuleren.

<!-- 

t_adding_search_title_rules.xml

 -->

**Ga als volgt te werk om regels voor zoektitels toe te voegen:**

1. Klik in het productmenu op **[!UICONTROL Settings]** > **[!UICONTROL Rewrite Rules]** > **[!UICONTROL Search Title Rules]**.
1. Voer in het veld [!DNL Search Title Rules] de gewenste regels in.

   Lege regels en commentaarregels die beginnen met een &#39;#&#39; (hash) teken zijn toegestaan.
1. (Optioneel) Voer in het veld [!DNL Test Search Title Rules] op de pagina [!DNL Search Title Rules] een testtitel in en klik vervolgens op **[!UICONTROL Test]**.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Optioneel) Maak de gefaseerde site-index opnieuw als u een voorvertoning van de resultaten wilt zien.

   Zie [Een incrementele index van een gefaseerde website configureren](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Optioneel) Voer op de pagina [!DNL Search Title Rules] een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).
