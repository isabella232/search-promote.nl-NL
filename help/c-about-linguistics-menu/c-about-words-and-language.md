---
description: Met Woorden en taal kunt u bepalen hoe de zoektermen overeenkomen met de inhoud van uw webpagina's.
solution: Target
title: Woorden en taal
topic: Taalkunde, zoeken en verhandelen van sites
uuid: 793d7a40-4609-44b8-a170-536eb1434537
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '1026'
ht-degree: 0%

---


# Info Woorden en taal{#about-words-language}

U kunt [!DNL Words & Language] gebruiken om te bepalen hoe de onderzoekstermijnen aan de inhoud van uw Web-pagina&#39;s worden aangepast.

## Woorden en taal {#concept_CEB4B9576F3C4E2EB87B352EEC738D79} gebruiken

Voordat de effecten van de [!DNL Words & Language]-instellingen beschikbaar zijn voor sitebezoekers, inclusief eventuele wijzigingen die u aanbrengt in deze instellingen, moet u de index van de site opnieuw genereren. In tegenstelling tot indexering betekent het opnieuw genereren niet dat u door uw webpagina&#39;s wilt bladeren en het duurt slechts een paar seconden.

## Bepalen hoe zoektermen overeenkomen met uw webinhoud {#task_351A9144A51F4B41923BDBACDEF3B616}

Met Woorden en taal kunt u bepalen hoe zoektermen en winkels op de site overeenkomen met de inhoud van uw webpagina&#39;s.

<!-- 

t_configuring_how_search_terms_matched_to_your_web_content.xml

 -->

**Bepalen hoe zoektermen overeenkomen met uw webinhoud**

1. Klik in het productmenu op **[!UICONTROL Linguistics]** > **[!UICONTROL Words & Language]**.
1. Stel op de pagina [!DNL Words & Languages] de gewenste opties in.

   <!-- 
   
   r_words_and_languages_options.xml
   
   -->

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Hoofdlettergevoeligheid </p> </td> 
      <td colname="col2"> <p>Standaard niet geselecteerd. </p> <p>Hiermee wordt bepaald of hoofdletters worden onderscheiden van kleine letters. Als u bijvoorbeeld selecteert, wordt ''Voltooid'' onderscheiden van ''Voltooid'' en kunnen de zoekresultaten per item verschillen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Diakritische gevoeligheid </p> </td> 
      <td colname="col2"> <p>Standaard geselecteerd. </p> <p> Hiermee wordt bepaald of woorden die diakritische tekens bevatten, worden onderscheiden van woorden die dat niet doen. Als deze optie is geselecteerd, wordt 'gedrag' onderscheiden van 'página'. Schakel deze optie uit als u een website hebt die niet-Engelse talen gebruikt. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Getallen </p> </td> 
      <td colname="col2"> <p>Standaard geselecteerd. </p> <p>Hiermee wordt bepaald of woorden met cijfers worden geïndexeerd. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Apostroffen negeren </p> </td> 
      <td colname="col2"> <p>Standaard niet geselecteerd. </p> <p>Apostroffen worden verwijderd uit query's. Als u bijvoorbeeld zoekt naar 'Boomstructuur', worden dezelfde resultaten geretourneerd als wanneer u naar 'Boomstam' zoekt. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Afbreekstreepjes negeren </p> </td> 
      <td colname="col2"> <p>Standaard niet geselecteerd. </p> <p>Afbreekstreepjes worden uit query's verwijderd. Als u bijvoorbeeld zoekt naar "blue-bell", worden dezelfde resultaten geretourneerd als wanneer u zoekt naar "bluebell". </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Partiële alfanumerieke overeenkomsten </p> </td> 
      <td colname="col2"> <p>Standaard niet geselecteerd. </p> <p>Als deze optie is ingeschakeld, kunt u tokens splitsen op alfabetische numerieke overgangen om overeenkomsten met vrije tekst op onderdelen of producttokens toe te staan. </p> <p>Stel dat u een product-id van <span class="codeph"> 910XT </span> hebt in de hoofdinhoud van een of meer pagina's op een website. Wanneer deze optie <i>niet</i> geselecteerd is, <span class="keyword"> Adobe Search&amp;Promote </span> vindt gelijken voor deze product herkenningsteken wanneer het zoeken naar <span class="codeph"> 910XT </span>. En als <span class="uicontrol"> Search Concat-Div-Enable </span> ingeschakeld was, zou <span class="keyword"> Adobe Search&amp;Promote </span> ook <span class="codeph"> 910 XT </span> vinden. Het zou echter geen exemplaren van <span class="codeph"> 910 </span> of <span class="codeph"> XT </span> vinden uitsluitend. </p> <p>Wanneer u <span class="uicontrol"> Onvolledige alfanumerieke gelijke </span> selecteert, breekt de indexeerder deze gemengde alfanumerieke tokens in veelvoudige tokens. Een product-id zoals <span class="codeph"> XYZ123 </span> wordt bijvoorbeeld in drie tokens geïndexeerd: <span class="codeph"> XYZ123 </span>, <span class="codeph"> XYZ </span> en <span class="codeph"> 123 </span>. Met deze functionaliteit kunnen deze varianten op elkaar worden afgestemd en dus tijdens de zoektijd. </p> <p>In een ander voorbeeld, veronderstel dat u het product herkenningsteken <span class="codeph"> AB910XT </span> hebt. Als u <span class="uicontrol"> Gedeeltelijke alfanumerieke aanpassing </span> <i>en</i> Zoekopdracht-Div-inschakelen </span> hebt ingeschakeld, wordt deze <span class="keyword"> Adobe Search&amp;Promote </span> geïndexeerd als <span class="codeph"> AB910XT </span>, <span class="codeph"> AB a11/&gt;, <span class="codeph"> 910 </span> en <span class="codeph"> XT </span>. <span class="uicontrol"></span> Wanneer een gebruiker vervolgens zoekt naar <span class="codeph"> 910XT </span>, bijvoorbeeld, wordt de zoekopdracht uitgebreid om ook instanties van <span class="codeph"> 910XT </span>, <span class="codeph"> 910 </span> of <span class="codeph"> XT </span> te zoeken. </span></p> <p> <p>Opmerking:  <span class="uicontrol"> Zoeken in concat-Div-Enable </span> is niet standaard ingeschakeld. Neem contact op met Technische ondersteuning om de functie voor uw gebruik te activeren. </p> </p> <p> <p>Opmerking:  <span class="uicontrol"> Onvolledige alfanumerieke matchingopties </span> wordt globaal toegepast op alle geïndexeerde velden. Het heeft echter alleen invloed op overeenkomsten met vrije tekst; het heeft geen invloed op de exacte overeenkomst of op de overeenkomsten tussen bereiken en bereiken. </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Sound-Alike Matching </p> </td> 
      <td colname="col2"> <p>Standaard geselecteerd. </p> <p>Woorden die op dezelfde manier klinken, zoals "gezondheid" en "gezondheid". Met deze functie kan uw klant gemakkelijk zoeken ondanks een spelfout. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Alternatief Word Forms </p> </td> 
      <td colname="col2"> <p>Standaard is <b>Standaard alternatief Word Forms</b>. </p> <p>U kunt uit de volgende opties in de Alternate Word Forms drop-down lijst selecteren: 
      <ul id="ul_CAC73FB4D1384312BB5DD327D3D66948"> 
      <li id="li_F4E76CD27EA34AC5BC81E648BC6CBA4C"><b>Geen</b> <p>Tijdens indexering worden geen stampingen of alternatieve woordformulieren toegepast. </p> </li> 
      <li id="li_3186FD1F3BC94A5CB66FFF8EA6726D81"><b>Standaard alternatief Word Forms</b> <p>Het stammen wordt automatisch gedaan tijdens het indexeren. </p> </li> 
      <li id="li_5815DE0795E0423C9C84C62B96A3F841"><b>Domeinwoordenboek</b> <p>Elk domeinwoordenboek dat u instelt als stamwoordenboek, wordt gebruikt als bron van alternatieve woordformulieren. </p> <p>Zie <a href="../c-about-linguistics-menu/c-about-dictionaries.md#concept_B8028B71EC8144669614C64578EDB034" type="concept" format="dita" scope="local"> Informatie over woordenboeken </a>. </p> <p>Zie <a href="../c-about-linguistics-menu/c-about-dictionaries.md#task_541E8453A12F4A8E89CF6F595469F074" type="task" format="dita" scope="local"> Een woordenboek configureren als een stamwoordenboek </a>. </p> </li> 
      </ul> </p> <p>Als woordstamming is ingeschakeld in <span class="keyword"> Adobe Search&amp;Promote </span>, moet u er rekening mee houden dat alternatieve woordvormen ook voorkomen binnen woordgroepen. </p> <p>Zie <a href="../c-searchpromote-release-notes/c-rn-06-19-14-version-815.md#concept_E8CEBC65A28A4E61BDE69B4B4DA55E73" format="dita" scope="local"> Opmerkingen bij de release van Search&amp;Promote 8.15.0 (19-6-2014) </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Taal </p> </td> 
      <td colname="col2"> <p>De standaardwaarde is <b>Engels (Verenigde Staten)</b>. </p> <p>De geselecteerde taal zorgt ervoor dat datum en numerieke waarden worden geparseerd volgens de conventies die in het geselecteerde deel van de wereld worden gebruikt. </p> <p>Als <span class="uicontrol"> Alternate Word Forms </span> is ingesteld op <span class="uicontrol"> Default Alternate Word Forms </span> of op <span class="uicontrol"> Domain Dictionary </span>, veranderen Word forms en word endings volgens de linguïstische regels voor de geselecteerde taal. </p> <p>Standaard wordt de taalinstelling niet gebruikt om de taal te bepalen van pagina's die van uw website worden gelezen. De taal voor een leespagina wordt bepaald aan de hand van de HTTP-headers of de metatags op de pagina zelf. Uw website kan pagina's in vele verschillende talen bevatten. Elke pagina wordt correct gelezen en geïndexeerd, ongeacht de taal die hier wordt geselecteerd. </p> <p>Als u voor bepaalde pagina's op uw website een codering van een Unicode-tekenset zoals UTF-8 gebruikt, moet u controleren of de taal voor elk van deze pagina's correct is opgegeven. Als de aangewezen HTTP- kopballen of metatags niet voor uw documenten van Unicode bestaan, kunt u <span class="uicontrol"> Montages </span> &gt; <span class="uicontrol"> Meta-gegevens </span> &gt; <span class="uicontrol"> Injecties </span> gebruiken om de aangewezen taal te specificeren. </p> <p><span class="uicontrol"> Toepassen op documenten zonder opgegeven taal? </span> om de taalinstelling te gebruiken voor pagina's die worden gelezen van uw website zonder expliciete instelling. Gebruik deze instelling wanneer slechts <i>sommige</i> van uw documenten taalinstellingen hebben. Gebruik <span class="uicontrol"> Instellingen </span> &gt; <span class="uicontrol"> Metagegevens </span> &gt; <span class="uicontrol"> Injecties </span> als <i>none</i> van uw documenten taalinstellingen hebben of als de set met betrokken documenten een bekende en beheerbaar kleine lijst is. </p> <p>Zie <a href="../c-about-settings-menu/c-about-metadata-menu.md#concept_DA091920671948A0A893A26B3A2FAAE5" type="concept" format="dita" scope="local"> Informatie over injecties </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Decompounder gebruiken? </p> </td> 
      <td colname="col2"> <p> <p>Opmerking:  Deze functie wordt alleen gebruikt voor Deens en Duits. Deze functie is ook niet standaard ingeschakeld. Neem contact op met Technische ondersteuning om de functie voor uw gebruik te activeren. Nadat het wordt toegelaten, <b>Gebruik Decompounder?</b> Deze optie wordt alleen weergegeven in de gebruikersinterface als u  <span class="uicontrol"> Deens  </span> of  <span class="uicontrol"> Duits selecteert in de  </span> vervolgkeuzelijst  <span class="uicontrol">   </span> Taal die eerder in deze tabel is beschreven. </p> </p> <p>Wanneer u <span class="uicontrol"> Decompounder gebruiken selecteert? </span>De dienst breidt Deense of Duitse samengestelde woorden uit, die het indexeren van componentwoorden samen met de originele samengestelde woorden mogelijk maken. </p> <p>Als u wilt zien hoe deze functie werkt, voert u woorden in het tekstveld in en klikt u op <span class="uicontrol"> Testen </span>. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Klik op **[!UICONTROL Save Settings]**.
1. Als u de resultaten van uw wijzigingen wilt bekijken, klikt u op **[!UICONTROL regenerate your staged site index]** om de gefaseerde website-index opnieuw samen te stellen.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

