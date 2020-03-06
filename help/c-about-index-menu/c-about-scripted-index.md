---
description: Met Scripted Index kunt u, stijgende indexerende opties schrijven bijwerken en handhaven zonder de behoefte aan login. De onderzoeksrobot leest instructies van een tekstdossier dat op uw server wordt ontvangen.
seo-description: Met Scripted Index kunt u, stijgende indexerende opties schrijven bijwerken en handhaven zonder de behoefte aan login. De onderzoeksrobot leest instructies van een tekstdossier dat op uw server wordt ontvangen.
seo-title: Over Scripted Index
solution: Target
subtopic: Scripted Index
title: Over Scripted Index
topic: Index,Site search and merchandising
uuid: 51e726ad-414b-4cbd-8a68-fefc3cf9b565
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a

---


# Over Scripted Index{#about-scripted-index}

Met Scripted Index kunt u, stijgende indexerende opties schrijven bijwerken en handhaven zonder de behoefte aan login. De onderzoeksrobot leest instructies van een tekstdossier dat op uw server wordt ontvangen.

## Scripted Index gebruiken {#concept_34F58D551BC04BFB8ADC294B9DA9199D}

## Ongeveer vormend scripted stijgende indexering {#section_161D254065E143F3A39F3FC09C400090}

Om Scripted Index te gebruiken, gebruikt u de pagina van de Configuratie van de Index van Scripted Incremental om URL aan een manuscriptdossier (een duidelijk tekstdossier) te specificeren dat op uw server wordt gevestigd. Bijvoorbeeld, `https://www.mysite.com/indexlist.txt`. Aangezien uw plaats verandert, kunt u bevelblokken aan het tekstdossier of manueel of automatisch toevoegen (met een manuscript dat door de aankomst van informatie van een nieuwsvoer, voorraadticker, of ander veranderd dossier wordt teweeggebracht).

Wanneer de scripted stijgende index begint, leest de onderzoeksrobot het tekstdossier en stelt de nieuwe bevelen in werking die in dat dossier worden gevonden. Door gebrek, verwerkt de onderzoeksrobot slechts de nieuwe bevelen, die door de dossierdatum worden bepaald. Tenzij u **[!UICONTROL Clear Date]** tegelijkertijd controleert u Scripted Index vormt, herinnert de onderzoeksrobot &quot;de datum-specifier&quot;van het onlangs verwerkte blok.

## Ongeveer het manuscriptdossier {#section_B312E40539F44C6583B4F9637D428E19}

Het manuscriptdossier dat u in URL specificeert is een duidelijk tekstdossier dat op uw server wordt gevestigd. U kunt vervoerwinst, lijnvoer, of allebei voor de eind-van-lijn opeenvolging gebruiken. Een lege lijn bevat nul of meer witte ruimtekarakters die door een eind-van-lijn opeenvolging worden gevolgd. Alle bevelen zijn case-insensitive.

Het tekstdossier wordt georganiseerd in blokken die de informatie beschrijven die de onderzoeksrobot gebruikt wanneer het een scripted stijgende index uitvoert.

De blokken worden bevolen door datum, met de oudste blokken bij de bovenkant van het tekstdossier, en de meest recente blokken bij de bodem. Elk blok begint met één enkele lijn datum-bevel en een datum-specifier bevel, en beëindigt met een spatie-lijn separator zoals in het volgende blokvoorbeeld (binnen tussen zijn verscheidene bevelen):

Een belangrijke nul wordt vereist voor alle rangschikkende data lager dan 10th wanneer het gebruiken van de stijl van HTTP 1.1. Bijvoorbeeld, 6 November is 06 Nov, niet 6 nov.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Opdracht </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>date-command </p> </td> 
   <td colname="col2"> <p>De eerste lijn van elk blok begint met één van twee datumbevelen: </p> <p> 
     <ul id="ul_9C1B229B7F1846C490B853FC34989E77"> 
      <li id="li_31FEF1A7163842BDBB0ABE779D07045A"> <span class="codeph"> datum </span> <p>Gebruik het "datum"bevel om erop te wijzen dat date-specifier uit een dag, een datum, een tijd, en een tijdzone zal bestaan. </p> </li> 
      <li id="li_0918D5B090014C1A852CB80BB7C2867C"> <span class="codeph"> seconden </span> <p>De <span class="codeph"> seconden van het gebruik </span> om erop te wijzen dat date-specifier uit een tijd in epoch seconden (bijvoorbeeld, 784111777) zal bestaan. Wanneer het gebruiken van <span class="codeph"> seconden </span>, zorg ervoor dat het aantal seconden tussen blokken stijgt. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>date-specifier </p> </td> 
   <td colname="col2"> <p>Het <span class="codeph"> date-specifier </span> bevel registreert typisch of de rangschikkende datum en de tijd (datumbevel) of de tijd in epoch seconden (secondenbevel) dat de blokinformatie aan het dossier werd toegevoegd. Bijvoorbeeld: </p> <p> <code> date&nbsp;Sun,&nbsp;06&nbsp;Nov&nbsp;1994&nbsp;08:49:37&nbsp;GMT&nbsp;(HTTP&nbsp;1.1&nbsp;style) 
      date&nbsp;Sunday,&nbsp;06-Nov-94&nbsp;08:49:37&nbsp;GMT&nbsp;(HTTP&nbsp;1.0&nbsp;style) 
      date&nbsp;Sun&nbsp;Nov&nbsp;6&nbsp;08:49:37&nbsp;1994&nbsp;(Unix&nbsp;asctime()&nbsp;date&nbsp;style) 
      seconds&nbsp;784111777&nbsp;(Unix&nbsp;epoch-seconds&nbsp;style) </code> </p> <p>Een belangrijke nul wordt vereist voor alle rangschikkende data lager dan 10th wanneer het gebruiken van de stijl van HTTP 1.1. Bijvoorbeeld, 6 November is 06 Nov, niet 6 nov. </p> <p>De onderzoeksrobot "herinnert"date-specifier van het onlangs verwerkte blok en slechts indexeert informatie die het "nieuwer"beschouwt. (Real-time doet er niet toe voor de zoekrobot. In plaats daarvan, is de tijd met betrekking tot andere eerder verwerkte tijden wat van belang is.) </p> <p>Nadat de onderzoeksrobot een blok met een date-specifier van 10:00 p.m. leest, bijvoorbeeld, het geen blokken die tijden vóór 10:00 p.m. registreren, ongeacht wanneer de indexverrichting loopt. In een worst-case scenario, zou u verkeerd het jaar "2040"in plaats van "2004"in uw date-specifier kunnen ingaan. In zo'n geval, indexeert de onderzoeksrobot het blok van 2040 tijdens de volgende het indexeren verrichting en weigert dan om het even welke andere blokken van informatie te lezen (tenzij één post-data 2040). Als dit zou moeten gebeuren, verwijder alle eerder verwerkte blokken uit het tekstdossier, klik <span class="uicontrol"> Duidelijke Datum </span>, en duw dan het levend. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>commentaarlijn </p> </td> 
   <td colname="col2"> <p>Beginnen met commentaarlijnen met het karakter "#". </p> <p>Elke commentaarlijn moet een lijn van zijn zijn zijn; u kunt geen eind-van-lijn commentaren typen. </p> <p>Een commentaarlijn wordt niet beschouwd als een lege lijn. Het kan overal in een blok, zelfs vóór een datum of een secondenbevel zoals in het volgende voorbeeld ook verschijnen: </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;#Added&nbsp;by&nbsp;Cathy&nbsp;Read&nbsp;after&nbsp;the&nbsp;Y2K&nbsp;seminar 
      &nbsp;&nbsp;&nbsp;&nbsp;date&nbsp;Mon,&nbsp;29&nbsp;Dec&nbsp;1999&nbsp;09:32:20&nbsp;GMT&nbsp; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>actie-opdracht </p> </td> 
   <td colname="col2"> <p>Elk tekstblok kan zo vele actiebevelen bevatten aangezien u wilt. De volgende actie-bevel opties beantwoorden aan die voor standaard het stijgende indexeren: </p> <p> 
     <ul id="ul_8E1435350A0F416BB8F7826CD3886E74"> 
      <li id="li_22181666628C48A28A6A0BA1F7CA8E77"> 
       <userinput>
         toevoegen 
       </userinput> <p>Gebruik met URL. De onderzoeksrobot indexeert slechts gespecificeerde URLs die sinds uw laatste het indexeren verrichting zijn veranderd. Bovendien, volgt de onderzoeksrobot verbindingen die binnen gespecificeerde documenten en indexen slechts die documenten bevat zijn die zijn veranderd. </p> <p>U kunt URL met volgen 
        <userinput>
          onopvolgzaam 
        </userinput> of 
        <userinput>
          noindex 
        </userinput> sleutelwoorden zoals in het volgende voorbeeld: </p> <p> <code> add&amp;nbsp;https://www.mydomain.com/&amp;nbsp;noindex </code> </p> </li> 
      <li id="li_8E47BF07DB24417083883F5BF40D6B9E"> 
       <userinput>
         bijwerken 
       </userinput> <p>Gebruik met masker URL. De onderzoeksrobot vindt en werkt alle documenten bij die het gespecificeerde masker URL aanpassen. </p> <p>U kunt URL met volgen 
        <userinput>
          onopvolgzaam 
        </userinput> of 
        <userinput>
          noindex 
        </userinput> sleutelwoorden zoals in het volgende voorbeeld: </p> <p> <code> update&amp;nbsp;https://www.mydomain.com/products/ </code> </p> </li> 
      <li id="li_B3EC8B1670D54F66A1D8411A694EF7E4"> 
       <userinput>
         omvatten 
       </userinput> of 
       <userinput>
         uitsluiten 
       </userinput> <p>Gebruik met masker URL. De onderzoeksrobot vindt en indexen ("omvat") of negeert ("sluit") documenten uit die op het gespecificeerde type van masker worden gebaseerd. </p> <p>Bijvoorbeeld: </p> <p> <code> include&amp;nbsp;https://www.mydomain.com/products/household/lightbulbs*.html </code> </p> <p>of </p> <p> <code> exclude&amp;nbsp;https://www.mydomain.com/archive/ </code> </p> </li> 
      <li id="li_050B54B735F0475E93806455FA6DC6A5"> 
       <userinput>
         incassodatum 
       </userinput> of 
       <userinput>
         uitsluitingsdatum 
       </userinput> <p>Gebruik met masker URL. De onderzoeksrobot vindt en indexen ("omvat") of negeert ("sluit") documenten uit die op zowel URL als de datum van documenten worden gebaseerd. De volgende soorten maskers zijn beschikbaar: </p> <p> 
        <ul id="ul_23A15CB492214B86BE84D8E6EA1820AE"> 
         <li id="li_0C7051AC3B5A4C57A3E477F7B6246611"> 
          <userinput>
            aantal dagen NNN 
          </userinput> <p>De onderzoeksrobot indexeert alle documenten die het gespecificeerde masker URL aanpassen en NNN dagen of meer oud zijn. </p> <p>U kunt het masker URL met de sleutelwoorden volgen 
           <userinput>
             onopvolgzaam 
           </userinput>, 
           <userinput>
             noindex 
           </userinput>en/of 
           <userinput>
             serverdatum 
           </userinput>. </p> </li> 
         <li id="li_983A10E2ED5D434EA9031F32143F4EF4"> 
          <userinput>
            inclusiedatum JJJJ-MM-DD 
          </userinput> <p> De onderzoeksrobot indexeert alle documenten die het gespecificeerde Url- masker aanpassen en zijn zo oud of ouder dan de datum JJJJ-MM-DD, waar "JJJJ"het 4 cijferjaar is, "MM"is de één of twee-cijfermaand (1-12), en "DD"is de één of twee-cijferige dag (1-31). </p> <p>U kunt het masker URL met de sleutelwoorden volgen 
           <userinput>
             onopvolgzaam 
           </userinput>, 
           <userinput>
             noindex 
           </userinput>en/of 
           <userinput>
             serverdatum 
           </userinput>. </p> </li> 
         <li id="li_733CE1B748024CECA7FBE00D7BC7B88A"> 
          <userinput>
            uitsluitingsdagen NNN 
          </userinput> <p> Maakt het indexeren van alle documenten onbruikbaar die het gespecificeerde masker URL aanpassen en NNN dagen of meer oud zijn. </p> <p>U kunt het masker URL met het sleutelwoord volgen 
           <userinput>
             serverdatum 
           </userinput>. </p> </li> 
         <li id="li_90056A0B96CC4DA3854711860A15CE89"> 
          <userinput>
            exclusief datum JJJJ-MM-DD 
          </userinput> <p>Maakt het indexeren van alle documenten onbruikbaar die het gespecificeerde masker URL aanpassen en zijn zo oud of ouder dan de datum JJJJ-MM-DD. </p> <p>U kunt het masker URL met het sleutelwoord volgen 
           <userinput>
             serverdatum 
           </userinput>. </p> </li> 
        </ul> </p> </li> 
      <li id="li_AA78F22B60FE4535BE73BA87A8992C08"> 
       <userinput>
         verwijderen 
       </userinput> <p>URL's opgeven. De onderzoeksrobot verwijdert documenten uit de index die door URL worden geïdentificeerd. </p> </li> 
      <li id="li_9C63061568AA4D57A4FEBCF6DB9194EC"> 
       <userinput>
         deletemask 
       </userinput> <p>De onderzoeksrobot verwijdert documenten uit de index die het gespecificeerde masker URL aanpast. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

Zie ook [over Maskers](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164)URL.

## Script-bestandsvoorbeeld {#section_9F580F20E7214751B157A28B392BD64E}

In het volgende voorbeeld van het manuscriptdossier, verwerkt de onderzoeksrobot de blokken op voorwaarde dat date-specifiers post-date date datum-specifier van het onlangs verwerkte blok. Als dat het geval is, dan komen de volgende het indexeren verrichtingen voor:

* Schrapt `y2k-problems.html` van de index.
* Voegt `no-y2k-problems.html` aan de onderzoeksindex toe en volgt geen van de verbindingen voor `no-y2k-problems.html`.

* Terwijl het kruipen, sluit URLs uit die `housewares.htm` en `lightfixtures.htm`l van de onderzoeksindex aanpassen.

* Neem alle andere directory&#39;s en documenten onder op `www.mydomain.com`.
* Werk alle documenten binnen de `products` en `information` folders bij, kruipend en indexerend alle dochterverbindingen die sinds de laatste het indexeren verrichting zijn veranderd.

* Terwijl het kruipen, sluit URLs in de `archive` sectie van de website uit als zij op of vóór 1 Januari, 1999 gedateerd zijn.
* Sluit URLs uit die `housewares.html` en van de onderzoeksindex aanpassen `lightfixtures.html` .

* De dossiers van de index in de `help` folder, maar kruipen of indexeren geen verbindingen van die dossiers.
* Kruip en indexeer om het even welke andere dossiers die voor worden ontmoet `www.mydomain.com`.

```
# Start of file. 
# Added by John Smith 
date Sat, 01 Jan 2004 16:05:53 PST 
exclude https://www.mydomain.com/housewares.html 
exclude https://www.mydomain.com/lightfixtures.html 
include https://www.mydomain.com/ 
delete https://www.mydomain.com/y2k-problems.html 
add https://www.mydomain.com/no-y2k-problems.html nofollow 
 
date Sun, 02 Jan 2004 20:19:08 PST 
# Added by the wire service updater 
exclude-date 1999-01-01 https://www.mydomain.com/archive server-date 
exclude https://www.mydomain.com/housewares.html 
exclude https://www.mydomain.com/lightfixtures.html 
include https://www.mydomain.com/help/ nofollow 
include https://www.mydomain.com/ 
# no add files, just update existing files 
# update all files in the "products" directory 
update https://www.mydomain.com/products/ 
# update all files in the "information" directory 
update regexp ^https://www\.mydomain\.com/information/.*$ 
# End of file.
```

## Het vormen van een scripted stijgende index {#task_05AE040FE75E40FFAA5E10B6B6D4D255}

U kunt een manuscript specificeren dat u hebt gecreeerd dat schrijft, bijwerkt, en handhaaft een stijgende index, zonder de behoefte aan login. De onderzoeksrobot leest instructies van het tekstdossier dat op uw server wordt ontvangen om de stijgende index uit te voeren.

**Om een scripted stijgende index te vormen**

1. Klik in het productmenu op **[!UICONTROL Index]** > **[!UICONTROL Scripted Index]** > **[!UICONTROL Configuration]**.
1. Voor de **[!UICONTROL Scripted Incremental Index Configuration]** pagina, in **[!UICONTROL Script File URL]**, ga URL aan het manuscript van het tekstdossier in dat op uw server wordt gevestigd.

   Zie [over Scripted Index](../c-about-index-menu/c-about-scripted-index.md#concept_34F58D551BC04BFB8ADC294B9DA9199D).
1. (Facultatief) controleer **[!UICONTROL Clear Date]** als u niet de onderzoeksrobot de datum-specifier van het onlangs verwerkte blok wilt &quot;herinneren&quot;.

   Door gebrek, verwerkt de onderzoeksrobot slechts nieuwe blokken van bevelen die in het tekstdossier worden gevonden, dat door de datum van het dossier wordt bepaald. Als u niet het gebrek wilt, controleer **[!UICONTROL Clear Date]**.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Het plaatsen van het scripted stijgende indexprogramma voor een levende website {#task_B3A87AC4AC784507859C23B9062BA11C}

U kunt scripted stijgende indexering plannen om met regelmatige intervallen door de dag voor te komen.

De basistijd die u selecteert is lokaal volgens de tijdzone die in de Montages van de Rekening wordt gevormd.

Zie [Je accountinstellingen](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)configureren.

De servers van het Web zijn vaak gepland om voor onderhoud in het midden van de nacht neer te gaan. Als uw server tijdens een geplande indextijd neer is, zal het het indexeren proces ontbreken. Zeker ben dat u een tijd van dag selecteert wanneer uw Webserver beschikbaar is.

Het indexprogramma is slechts op uw levende index van toepassing; u kunt gefaseerde stijgende indexen niet plannen.

**Om het scripted stijgende indexprogramma voor een levende website te plaatsen**

1. Klik in het productmenu op **[!UICONTROL Index]** > **[!UICONTROL Scripted Index]** > **[!UICONTROL Live Schedule]**.
1. Voor de **[!UICONTROL Scripted Incremental Index Schedule]** pagina, in de **[!UICONTROL Read the Scripted Incrementally Indexing File]** drop-down lijst, selecteer de frequentie dat u het scripted stijgende dossier van de indextekst, in uren of notulen wilt lopen.
1. In de **[!UICONTROL Base Time]** drop-down lijst, selecteer de beginnende tijd wanneer u een nieuwe scripted stijgende index wilt regenereren.
1. Klik op **[!UICONTROL Save Changes]**.

## Het runnen van een scripted stijgende index van een levende of gefaseerde website {#task_6E6FC76EE1E84A5FADB3B67AD7B1DACB}

U kunt de Stijgende Index van Scripted gebruiken om &quot;stukken&quot;van uw levende of gefaseerde website, zoals een inzameling van vaak veranderde pagina&#39;s te indexeren, allen zonder de behoefte aan login.

Om deze eigenschap te gebruiken, ben zeker dat u een scripted stijgende dossier van de indextekst hebt gevormd.

Zie het [Vormen van een scripted stijgende index](../c-about-index-menu/c-about-scripted-index.md#task_05AE040FE75E40FFAA5E10B6B6D4D255).

**Om een scripted stijgende index van een levende of gefaseerde website in werking te stellen**

1. Voor het productmenu, doe één van het volgende:

   * Klik op **[!UICONTROL Index]** > **[!UICONTROL Scripted Index]** > **[!UICONTROL Live Index]**.
   * Klik op **[!UICONTROL Index]** > **[!UICONTROL Scripted Index]** > **[!UICONTROL Staged Index]**.

1. Klik op **[!UICONTROL Scripted Index Now]**.
1. (Facultatief) als het indexeren fouten voorkwamen, klik **[!UICONTROL View Errors]** om het bijbehorende logboek te bekijken.

## Het bekijken van het scripted stijgende indexlogboek van een levende of gefaseerde website {#task_CBFCE9B9A87B4DF7A2A35A6E83DE93D7}

Wanneer een levende volledige scripted index of een gefaseerde volledige scripted index volledig is, kunt u zijn bijbehorend logboek bekijken om het even welke fouten problemen op te lossen die voorkwamen.

U kunt geen logboeken uitvoeren, noch hen bewaren. Nochtans, blijft het logboek beschikbaar voor het bekijken tot de nieuwe index voorkomt.

**Om het stijgende indexlogboek van een levende of gefaseerde website te bekijken**

1. Voor het productmenu, doe één van het volgende:

   * Klik op **[!UICONTROL Index]** > **[!UICONTROL Scripted Index]** > **[!UICONTROL Live Log]**.

   * Klik op **[!UICONTROL Index]** > **[!UICONTROL Scripted Index]** > **[!UICONTROL Staged Log]**.

1. Voor de logboekpagina, bij de bovenkant of de bodem, doe om het even welke volgend:

   * Gebruik de navigatieopties **[!UICONTROL First]**, **[!UICONTROL Prev]**, **[!UICONTROL Next]**, **[!UICONTROL Last]**, of **[!UICONTROL Go to line]** om zich door het logboek te bewegen.

   * Gebruik de vertoningsopties **[!UICONTROL Errors only]**, **[!UICONTROL Wrap line]**, of **[!UICONTROL Show]** om te raffineren wat u ziet.

