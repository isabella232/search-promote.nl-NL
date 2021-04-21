---
description: Met Scripted Index kunt u stijgende indexeringsopties schrijven, bijwerken en handhaven zonder de behoefte aan login. De zoekrobot leest instructies uit een tekstbestand dat op uw server wordt gehost.
solution: Target
subtopic: Scripted Index
title: Over Scriptindex
topic-legacy: Index,Site search and merchandising
uuid: 51e726ad-414b-4cbd-8a68-fefc3cf9b565
exl-id: e1d14cd5-4885-4e3a-bc5f-fe0b6a4df15e
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '1725'
ht-degree: 0%

---

# Info over Scriptindex{#about-scripted-index}

Met Scripted Index kunt u stijgende indexeringsopties schrijven, bijwerken en handhaven zonder de behoefte aan login. De zoekrobot leest instructies uit een tekstbestand dat op uw server wordt gehost.

## Scriptindex {#concept_34F58D551BC04BFB8ADC294B9DA9199D} gebruiken

## Informatie over het configureren van incrementele indexering met scripts {#section_161D254065E143F3A39F3FC09C400090}

Als u Scripted Index wilt gebruiken, gebruikt u de pagina Configuratie van incrementele index met scripts om de URL op te geven naar een scriptbestand (een tekstbestand zonder opmaak) dat zich op uw server bevindt. Bijvoorbeeld, `https://www.mysite.com/indexlist.txt`. Als uw site verandert, kunt u handmatig of automatisch opdrachtblokken aan het tekstbestand toevoegen (met een script dat wordt geactiveerd door de aankomst van informatie uit een nieuwsfeed, voorraadkiezer of ander gewijzigd bestand).

Wanneer de gescripte incrementele index begint, leest de zoekrobot het tekstbestand en voert de nieuwe opdrachten uit die in dat bestand staan. Standaard verwerkt de zoekrobot alleen de nieuwe opdrachten, die worden bepaald door de bestandsdatum. Tenzij u **[!UICONTROL Clear Date]** op het tijdstip controleert u Scripted Index vormt, &quot;herinnert de onderzoeksrobot&quot;datum-specifier van het onlangs verwerkte blok.

## Informatie over het scriptbestand {#section_B312E40539F44C6583B4F9637D428E19}

Het scriptbestand dat u in de URL opgeeft, is een tekstbestand zonder opmaak dat zich op uw server bevindt. U kunt looppasterugkeer, lijnvoer, of allebei voor de eind-van-lijn opeenvolging gebruiken. Een lege regel bevat nul of meer spatietekens gevolgd door een regeleinde. Alle opdrachten zijn hoofdlettergevoelig.

Het tekstbestand is ingedeeld in blokken die de informatie beschrijven die de zoekrobot gebruikt wanneer deze een gescripte incrementele index uitvoert.

Blokken worden op datum geordend, met de oudste blokken boven aan het tekstbestand en de meest recente blokken onder aan. Elk blok begint met één enkele lijn datum-bevel en een datum-specifier bevel, en eindigt met een leeg-lijn separator zoals in het volgende blokvoorbeeld (binnen zijn verscheidene bevelen):

Een voorloopnul is vereist voor alle rangsdatums lager dan de tiende bij gebruik van de HTTP 1.1-stijl. 6 november is bijvoorbeeld 06 nov, niet 6 nov.

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
   <td colname="col2"> <p>De eerste regel van elk blok begint met een van twee datumopdrachten: </p> <p> 
     <ul id="ul_9C1B229B7F1846C490B853FC34989E77"> 
      <li id="li_31FEF1A7163842BDBB0ABE779D07045A"> <span class="codeph"> date  </span> <p>Gebruik het "datum"bevel om erop te wijzen dat date-specifier uit een dag, een datum, een tijd, en een tijdzone zal bestaan. </p> </li> 
      <li id="li_0918D5B090014C1A852CB80BB7C2867C"> <span class="codeph"> seconden  </span> <p>Gebruik <span class="codeph"> seconden </span> om aan te geven dat date-specifier uit een tijd in epoch seconden zal bestaan (bijvoorbeeld, 784111777). Wanneer het gebruiken <span class="codeph"> seconden </span>, zorg ervoor dat het aantal seconden tussen blokken stijgt. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>date-specifier </p> </td> 
   <td colname="col2"> <p>De <span class="codeph"> datum-specifier </span> bevel registreert typisch of de normale datum en de tijd (datumbevel) of de tijd in epoch seconden (secondenbevel) dat de blokinformatie aan het dossier werd toegevoegd. Bijvoorbeeld: </p> <p> <code> date&nbsp;Sun,&nbsp;06&nbsp;Nov&nbsp;1994&nbsp;08:49:37&nbsp;GMT&nbsp;(HTTP&nbsp;1.1&nbsp;style) 
      date&nbsp;Sunday,&nbsp;06-Nov-94&nbsp;08:49:37&nbsp;GMT&nbsp;(HTTP&nbsp;1.0&nbsp;style) 
      date&nbsp;Sun&nbsp;Nov&nbsp;6&nbsp;08:49:37&nbsp;1994&nbsp;(Unix&nbsp;asctime()&nbsp;date&nbsp;style) 
      seconds&nbsp;784111777&nbsp;(Unix&nbsp;epoch-seconds&nbsp;style) </code> </p> <p>Een voorloopnul is vereist voor alle rangsdatums lager dan de tiende bij gebruik van de HTTP 1.1-stijl. 6 november is bijvoorbeeld 06 nov, niet 6 nov. </p> <p>De zoekrobot "onthoudt" de date-specifier van het laatst verwerkte blok en indexeert alleen de informatie die het als "nieuwer" beschouwt. (Real-time is niet van belang voor de zoekrobot. In plaats daarvan is de tijd in vergelijking met andere eerder verwerkte tijden van belang.) </p> <p>Nadat de zoekrobot een blok met een date-specifier van 10:00 p.m. leest het bijvoorbeeld geen blokken die tijden vóór 10:00 p.m. registreren, ongeacht wanneer de indexverrichting loopt. In een worst-case scenario, zou u het jaar "2040"in plaats van "2004"in uw date-specifier verkeerd kunnen ingaan. In zo'n geval, indexeert de onderzoeksrobot het 2040 blok tijdens de volgende het indexeren verrichting en dan weigert om het even welke andere blokken van informatie te lezen (tenzij één post-data 2040). Als dit zou moeten gebeuren, verwijder alle eerder verwerkte blokken uit het tekstdossier, klik <span class="uicontrol"> Duidelijke Datum </span>, en duw dan het levend. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>opmerkingsregel </p> </td> 
   <td colname="col2"> <p>Begin commentaarregels met het teken "#". </p> <p>Elke commentaarregel moet een eigen regel zijn; u kunt geen opmerkingen aan het einde van de regel typen. </p> <p>Een commentaarregel wordt niet als een lege regel beschouwd. Het kan ook overal in een blok, zelfs vóór een datum of secondenbevel zoals in het volgende voorbeeld verschijnen: </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;#Added&nbsp;by&nbsp;Cathy&nbsp;Read&nbsp;after&nbsp;the&nbsp;Y2K&nbsp;seminar 
      &nbsp;&nbsp;&nbsp;&nbsp;date&nbsp;Mon,&nbsp;29&nbsp;Dec&nbsp;1999&nbsp;09:32:20&nbsp;GMT&nbsp; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>action-command </p> </td> 
   <td colname="col2"> <p>Elk tekstblok kan zoveel handelingsopdrachten bevatten als u wilt. De volgende actie-bevel opties beantwoorden aan die voor standaard stijgende indexering: </p> <p> 
     <ul id="ul_8E1435350A0F416BB8F7826CD3886E74"> 
      <li id="li_22181666628C48A28A6A0BA1F7CA8E77"> 
       <code>
         add 
       </code> <p>Gebruik met URL. De zoekrobot indexeert alleen de opgegeven URL's die zijn gewijzigd sinds de laatste indexeringsbewerking. Bovendien volgt de zoekrobot koppelingen binnen opgegeven documenten en indexeert alleen de documenten die zijn gewijzigd. </p> <p>U kunt de URL volgen met 
        <code>
          nofollow 
        </code> of 
        <code>
          noindex 
        </code> trefwoorden zoals in het volgende voorbeeld: </p> <p> <code> add&amp;nbsp;https://www.mydomain.com/&amp;nbsp;noindex </code> </p> </li> 
      <li id="li_8E47BF07DB24417083883F5BF40D6B9E"> 
       <code>
         update 
       </code> <p>Gebruiken met URL-masker. De zoekrobot zoekt en werkt alle documenten bij die overeenkomen met het opgegeven URL-masker. </p> <p>U kunt de URL volgen met 
        <code>
          nofollow 
        </code> of 
        <code>
          noindex 
        </code> trefwoorden zoals in het volgende voorbeeld: </p> <p> <code> update&amp;nbsp;https://www.mydomain.com/products/ </code> </p> </li> 
      <li id="li_B3EC8B1670D54F66A1D8411A694EF7E4"> 
       <code>
         include 
       </code> of  
       <code>
         exclude 
       </code> <p>Gebruiken met URL-masker. De zoekrobot zoekt en indexeert ("include") of negeert ("exclude") documenten op basis van het opgegeven type masker. </p> <p>Bijvoorbeeld: </p> <p> <code> include&amp;nbsp;https://www.mydomain.com/products/household/lightbulbs*.html </code> </p> <p>of </p> <p> <code> exclude&amp;nbsp;https://www.mydomain.com/archive/ </code> </p> </li> 
      <li id="li_050B54B735F0475E93806455FA6DC6A5"> 
       <code>
         include-date 
       </code> of  
       <code>
         exclude-date 
       </code> <p>Gebruiken met URL-masker. De zoekrobot zoekt en indexeert ("include") of negeert ("exclude") documenten op basis van zowel de URL als de datum van documenten. De volgende typen maskers zijn beschikbaar: </p> <p> 
        <ul id="ul_23A15CB492214B86BE84D8E6EA1820AE"> 
         <li id="li_0C7051AC3B5A4C57A3E477F7B6246611"> 
          <code>
            include-days NNN 
          </code> <p>De zoekrobot indexeert alle documenten die overeenkomen met het opgegeven URL-masker en die NNN days of ouder zijn. </p> <p>U kunt het URL-masker volgen met de trefwoorden 
           <code>
             nofollow 
           </code>, 
           <code>
             noindex 
           </code>, en/of 
           <code>
             server-date 
           </code>. </p> </li> 
         <li id="li_983A10E2ED5D434EA9031F32143F4EF4"> 
          <code>
            include-date YYYY-MM-DD 
          </code> <p> De zoekrobot indexeert alle documenten die overeenkomen met het opgegeven URL-masker en die even oud of ouder zijn dan de datum YYYY-MM-DD, waarbij "YYYY" het jaartal in 4 cijfers is, "MM" de maand met 1 of 2 cijfers (1-12) en "DD" de dag met 1 of 2 cijfers (1-31). </p> <p>U kunt het URL-masker volgen met de trefwoorden 
           <code>
             nofollow 
           </code>, 
           <code>
             noindex 
           </code>, en/of 
           <code>
             server-date 
           </code>. </p> </li> 
         <li id="li_733CE1B748024CECA7FBE00D7BC7B88A"> 
          <code>
            exclude-days NNN 
          </code> <p> Hiermee schakelt u het indexeren uit van alle documenten die overeenkomen met het opgegeven URL-masker en die NNN days of ouder zijn. </p> <p>U kunt het URL-masker volgen met het trefwoord 
           <code>
             server-date 
           </code>. </p> </li> 
         <li id="li_90056A0B96CC4DA3854711860A15CE89"> 
          <code>
            exclude-date YYYY-MM-DD 
          </code> <p>Hiermee schakelt u het indexeren uit van alle documenten die overeenkomen met het opgegeven URL-masker en die even oud of ouder zijn dan de datum YYYY-MM-DD. </p> <p>U kunt het URL-masker volgen met het trefwoord 
           <code>
             server-date 
           </code>. </p> </li> 
        </ul> </p> </li> 
      <li id="li_AA78F22B60FE4535BE73BA87A8992C08"> 
       <code>
         delete 
       </code> <p>Geef URL's op. De zoekrobot verwijdert documenten uit de index die door de URL worden geïdentificeerd. </p> </li> 
      <li id="li_9C63061568AA4D57A4FEBCF6DB9194EC"> 
       <code>
         deletemask 
       </code> <p>De zoekrobot verwijdert documenten uit de index die overeenkomen met het opgegeven URL-masker. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

Zie ook [Informatie over URL-maskers](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164).

## Voorbeeld van scriptbestand {#section_9F580F20E7214751B157A28B392BD64E}

In het volgende scriptbestandvoorbeeld verwerkt de zoekrobot de blokken op voorwaarde dat de date-specifiers de date-specifier van het laatst verwerkte blok zijn. Als dat het geval is, vinden de volgende indexeringsverrichtingen plaats:

* Verwijdert `y2k-problems.html` uit de index.
* Voegt `no-y2k-problems.html` aan de onderzoeksindex toe en volgt geen van de verbindingen voor `no-y2k-problems.html`.

* Sluit tijdens het horizontaal schuiven URL&#39;s die overeenkomen met `housewares.htm` en `lightfixtures.htm`l uit van de zoekindex.

* Alle andere mappen en documenten opnemen onder `www.mydomain.com`.
* Werk alle documenten binnen `products` en `information` folders bij, die en alle secundaire verbindingen kruipen indexeren die sinds de laatste het indexeren verrichting zijn veranderd.

* Sluit tijdens het horizontaal schuiven URL&#39;s uit in het gedeelte `archive` van de website als deze gedateerd zijn op of vóór 1 januari 1999.
* Sluit URL&#39;s die overeenkomen met `housewares.html` en `lightfixtures.html` uit van de zoekindex.

* Indexeer bestanden in de map `help`, maar kruip of indexeer geen koppelingen uit die bestanden.
* kruipt en indexeert andere dossiers die voor `www.mydomain.com` worden ontmoet.

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

## Een gescripte incrementele index {#task_05AE040FE75E40FFAA5E10B6B6D4D255} configureren

U kunt een script opgeven dat u hebt gemaakt en dat een incrementele index schrijft, bijwerkt en onderhoudt, zonder dat u zich hoeft aan te melden. De zoekrobot leest instructies uit het tekstbestand dat op uw server wordt gehost om de incrementele index uit te voeren.

**Een gescripte incrementele index configureren**

1. Klik in het productmenu op **[!UICONTROL Index]** > **[!UICONTROL Scripted Index]** > **[!UICONTROL Configuration]**.
1. Op **[!UICONTROL Scripted Incremental Index Configuration]** pagina, in **[!UICONTROL Script File URL]**, ga URL aan het manuscript van het tekstdossier in dat op uw server wordt gevestigd.

   Zie [Informatie over index met scripts](../c-about-index-menu/c-about-scripted-index.md#concept_34F58D551BC04BFB8ADC294B9DA9199D).
1. (Optioneel) Schakel **[!UICONTROL Clear Date]** in als u niet wilt dat de zoekrobot de datum-aanduiding van het laatst verwerkte blok &quot;onthoudt&quot;.

   Standaard verwerkt de zoekrobot alleen nieuwe opdrachtblokken die in het tekstbestand worden gevonden. Dit wordt bepaald door de datum van het bestand. Als u niet het gebrek wilt, controleer **[!UICONTROL Clear Date]**.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Het gescripte incrementele-indexschema voor een live website instellen {#task_B3A87AC4AC784507859C23B9062BA11C}

U kunt de gescripte stijgende indexering plannen om met regelmatige intervallen door de dag voor te komen.

De basistijd die u selecteert is lokaal volgens de tijdzone die in de Montages van de Rekening wordt gevormd.

Zie [Uw accountinstellingen configureren](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9).

Webservers zullen vaak halverwege de nacht naar beneden gaan voor onderhoud. Als uw server tijdens een geplande indextijd neer is, zal het indexeren proces ontbreken. Zorg ervoor dat u een tijdstip van de dag selecteert waarop uw webserver beschikbaar is.

Het indexschema is alleen van toepassing op uw live index. u kunt gefaseerde incrementele indexen niet plannen.

**Het gescripte incrementele-indexschema voor een live website instellen**

1. Klik in het productmenu op **[!UICONTROL Index]** > **[!UICONTROL Scripted Index]** > **[!UICONTROL Live Schedule]**.
1. Selecteer op de pagina **[!UICONTROL Scripted Incremental Index Schedule]** in de vervolgkeuzelijst **[!UICONTROL Read the Scripted Incrementally Indexing File]** de frequentie waarmee u het gescripte incrementele-indextekstbestand wilt uitvoeren, in uren of minuten.
1. Selecteer in de vervolgkeuzelijst **[!UICONTROL Base Time]** de begintijd wanneer u een nieuwe gescripte incrementele index opnieuw wilt genereren.
1. Klik op **[!UICONTROL Save Changes]**.

## Een gescripte incrementele index van een actieve of gefaseerde website uitvoeren {#task_6E6FC76EE1E84A5FADB3B67AD7B1DACB}

U kunt Scripted Incremental Index gebruiken om &quot;stukken&quot;van uw levende of gefaseerde website, zoals een inzameling van vaak veranderde pagina&#39;s te indexeren, allen zonder de behoefte om binnen te registreren.

Als u deze functie wilt gebruiken, moet u een gescript incrementeel indextekstbestand configureren.

Zie [Een gescripte incrementele index configureren](../c-about-index-menu/c-about-scripted-index.md#task_05AE040FE75E40FFAA5E10B6B6D4D255).

**Een gescripte incrementele index van een actieve of gefaseerde website uitvoeren**

1. Voer een van de volgende handelingen uit in het menu Product:

   * Klik op **[!UICONTROL Index]** > **[!UICONTROL Scripted Index]** > **[!UICONTROL Live Index]**.
   * Klik op **[!UICONTROL Index]** > **[!UICONTROL Scripted Index]** > **[!UICONTROL Staged Index]**.

1. Klik op **[!UICONTROL Scripted Index Now]**.
1. (Optioneel) Als er indexatiefouten zijn opgetreden, klikt u op **[!UICONTROL View Errors]** om het gekoppelde logboek weer te geven.

## Het gescripte incrementele-indexlogboek van een actieve of gefaseerde website weergeven {#task_CBFCE9B9A87B4DF7A2A35A6E83DE93D7}

Wanneer een live volledige scriptindex of een gefaseerde volledige scriptindex is voltooid, kunt u het bijbehorende logboek weergeven om eventuele fouten op te lossen.

U kunt logboeken niet exporteren of opslaan. Het logboek blijft echter beschikbaar voor weergave totdat de nieuwe index wordt weergegeven.

**Het incrementele indexlogboek van een live of gefaseerde website weergeven**

1. Voer een van de volgende handelingen uit in het menu Product:

   * Klik op **[!UICONTROL Index]** > **[!UICONTROL Scripted Index]** > **[!UICONTROL Live Log]**.

   * Klik op **[!UICONTROL Index]** > **[!UICONTROL Scripted Index]** > **[!UICONTROL Staged Log]**.

1. Voer een of meerdere van de volgende handelingen uit op de logpagina, boven of onder:

   * Gebruik de navigatieopties **[!UICONTROL First]**, **[!UICONTROL Prev]**, **[!UICONTROL Next]**, **[!UICONTROL Last]**, of **[!UICONTROL Go to line]** om door het logboek te bewegen.

   * Gebruik de weergaveopties **[!UICONTROL Errors only]**, **[!UICONTROL Wrap line]** of **[!UICONTROL Show]** om te verfijnen wat u ziet.
