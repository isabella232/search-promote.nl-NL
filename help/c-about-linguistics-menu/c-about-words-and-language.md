---
description: U kunt Woorden & Taal gebruiken om te bepalen hoe de onderzoekstermijnen aan de inhoud van uw Web-pagina's worden aangepast.
seo-description: U kunt Woorden & Taal gebruiken om te bepalen hoe de onderzoekstermijnen aan de inhoud van uw Web-pagina's worden aangepast.
seo-title: Over woorden en taal
solution: Target
title: Over woorden en taal
topic: Linguistics,Site search and merchandising
uuid: 793d7a40-4609-44b8-a170-536eb1434537
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# Over woorden en taal{#about-words-language}

U kunt gebruiken [!DNL Words & Language] om te bepalen hoe de onderzoekstermijnen aan de inhoud van uw Web-pagina&#39;s worden aangepast.

## Woorden en taal gebruiken {#concept_CEB4B9576F3C4E2EB87B352EEC738D79}

Alvorens de gevolgen van [!DNL Words & Language] montages aan plaatsbezoekers beschikbaar zijn, met inbegrip van om het even welke veranderingen u aan die montages aanbrengt, moet u uw plaatsindex regenereren. Het terugwinnen, in tegenstelling tot het indexeren, impliceert niet kruipend uw Web-pagina&#39;s en vergt slechts een paar seconden.

## Het vormen hoe de onderzoekstermijnen aan uw Webinhoud worden aangepast {#task_351A9144A51F4B41923BDBACDEF3B616}

U kunt Woorden &amp; Taal gebruiken om te bepalen hoe het plaatsonderzoek/de merchandising onderzoekstermijnen aan de inhoud van uw Web-pagina&#39;s aanpast.

<!-- 

t_configuring_how_search_terms_matched_to_your_web_content.xml

 -->

**Om te vormen hoe de onderzoekstermijnen aan uw Webinhoud worden aangepast**

1. Klik in het productmenu op **[!UICONTROL Linguistics]** > **[!UICONTROL Words & Language]**.
1. Voor de [!DNL Words & Languages] pagina, plaats de opties die u wilt.

   <!-- 
   
   r_words_and_languages_options.xml
   
   -->

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Optie </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Gevallengevoeligheid </p> </td> 
      <td colname="col2"> <p>Standaard niet geselecteerd. </p> <p>Bepaalt of hoofdletters van kleine letters worden onderscheiden. Bijvoorbeeld, wanneer geselecteerd, "wordt succesvol"onderscheiden van "slagen", en de onderzoeksresultaten kunnen tussen twee variëren. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Diacritische gevoeligheid </p> </td> 
      <td colname="col2"> <p>Standaard geselecteerd. </p> <p> Bepaalt of de woorden die diacritische karakters bevatten van woorden worden onderscheiden die niet. Als u bijvoorbeeld "parameter" selecteert, wordt deze onderscheiden van "página". Schrap deze optie als u een website hebt die niet-Engelse talen gebruikt. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Aantal </p> </td> 
      <td colname="col2"> <p>Standaard geselecteerd. </p> <p>Bepaalt of de woorden die cijfers bevatten worden geïndexeerd. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Apostrophes negeren </p> </td> 
      <td colname="col2"> <p>Standaard niet geselecteerd. </p> <p>Apostrophes worden verwijderd uit vragen. Een zoekopdracht naar 'Bomen' zou bijvoorbeeld dezelfde resultaten opleveren als een zoekopdracht naar 'Bomen'. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ignore Hyphens </p> </td> 
      <td colname="col2"> <p>Standaard niet geselecteerd. </p> <p>Hyphens worden verwijderd uit vragen. Een zoekopdracht naar "blue-bell" zou bijvoorbeeld dezelfde resultaten opleveren als een zoekopdracht naar "bluebell". </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Partiële alfanumerieke matching </p> </td> 
      <td colname="col2"> <p>Standaard niet geselecteerd. </p> <p>Wanneer geselecteerd, laat deze optie u tekenen op alfabetische-numerieke overgangen verdelen om vrije-tekstgelijken op deel of producttekenen toe te staan. </p> <p>Bijvoorbeeld, veronderstel dat u een productherkenningsteken van <span class="codeph"> 910XT </span> in de lichaamsinhoud van één of meerdere pagina's op een website hebt. Wanneer deze optie <i>niet</i> wordt geselecteerd, <span class="keyword"> vindt het Onderzoek&amp;Promote van Adobe gelijken voor dit productherkenningsteken wanneer het zoeken naar </span> 910XT <span class="codeph"> </span>. En, met <span class="uicontrol"> Onderzoek contact-Div-laat </span> aangezet toe, <span class="keyword"> zou het Onderzoek&amp;Promote van Adobe </span> ook <span class="codeph"> 910 XT vinden </span>. Nochtans, zou het geen gevallen van <span class="codeph"> 910 </span> of <span class="codeph"> XT </span> uitsluitend vinden. </p> <p>Wanneer u <span class="uicontrol"> Gedeeltelijke Alfanumerieke Aanpassing selecteert </span>, breekt de indexeerder deze gemengde alfanumerieke tekenen in veelvoudige tekenen. Bijvoorbeeld, wordt een productherkenningsteken zoals <span class="codeph"> XYZ123 </span> geïndexeerd in drie tekenen: <span class="codeph"> XYZ123 </span>, <span class="codeph"> XYZ </span>, en <span class="codeph"> 123 </span>. Dergelijke functionaliteit staat voor onderzoek-tijd vrije-tekst aanpassing op om het even welk van deze varianten toe. </p> <p>In een ander voorbeeld, veronderstel dat u het productherkenningsteken <span class="codeph"> AB910XT hebt </span>. Als u <span class="uicontrol"> Gedeeltelijke Alfanumerieke Aanpassing selecteert </span> en <i></i> Onderzoek contact-Div-toelaat <span class="uicontrol"> aangezet hebt, </span> Adobe Search&amp;Promote <span class="keyword"> indexen het als </span> <span class="codeph"> </span><span class="codeph"> </span><span class="codeph"> </span><span class="codeph"> </span>AB910XT,  AB, 910, enXT. Dan, wanneer een gebruiker naar <span class="codeph"> 910XT </span>, bijvoorbeeld zoekt, breidt het onderzoek zich uit om instanties van <span class="codeph"> 910XT </span>, <span class="codeph"> 910 </span>, of <span class="codeph"> XT ook te vinden </span>. </p> <p> <p>Opmerking:  <span class="uicontrol"> Onderzoek contact-Div-laat toe </span> wordt niet toegelaten door gebrek. Neem contact op met Technische ondersteuning om de functie voor uw gebruik te activeren. </p> </p> <p> <p>Opmerking:  <span class="uicontrol"> Gedeeltelijke alfanumerieke matchen </span> wordt globaal toegepast op alle geïndexeerde velden. Nochtans, beïnvloedt het slechts de aanpassing van de vrije-tekst; het heeft geen invloed op de exacte matching of de waaier aanpassing. </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Sound-Alike Matching </p> </td> 
      <td colname="col2"> <p>Standaard geselecteerd. </p> <p>Woorden die op elkaar lijken, zoals "gezondheid" en "gezondheid". Met deze functie kan uw klant eenvoudig zoeken, ondanks een verkeerde spelling van een woord. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Alternatieve Word-formulieren </p> </td> 
      <td colname="col2"> <p>Het gebrek is de <b>Standaard Afwisselende Vormen</b>van Word. </p> <p>U kunt uit de volgende opties in de Afwisselende drop-down lijst van de Vormen van Word selecteren: 
      <ul id="ul_CAC73FB4D1384312BB5DD327D3D66948"> 
      <li id="li_F4E76CD27EA34AC5BC81E648BC6CBA4C"><b>Geen</b> <p>Bij indexering worden geen stamformulieren of alternatieve woordformulieren gebruikt. </p> </li> 
      <li id="li_3186FD1F3BC94A5CB66FFF8EA6726D81"><b>Standaard Alternatieve Word-formulieren</b> <p>Het afremmen wordt automatisch gedaan tijdens het indexeren. </p> </li> 
      <li id="li_5815DE0795E0423C9C84C62B96A3F841"><b>Domeinwoordenlijst</b> <p>Om het even welk domeinwoordenboek dat u als stamwoordenboek plaatst wordt gebruikt een bron van afwisselende woordvormen. </p> <p>Zie <a href="../c-about-linguistics-menu/c-about-dictionaries.md#concept_B8028B71EC8144669614C64578EDB034" type="concept" format="dita" scope="local"> over woordenboeken </a>. </p> <p>Zie Een woordenboek <a href="../c-about-linguistics-menu/c-about-dictionaries.md#task_541E8453A12F4A8E89CF6F595469F074" type="task" format="dita" scope="local"> configureren als een stamwoordenlijst </a>. </p> </li> 
      </ul> </p> <p>Als het uitdrukking stampen in <span class="keyword"> </span>Adobe Onderzoek&amp;Promote wordt toegelaten, me ervan bewust ben dat de afwisselende woordvormen ook binnen uitdrukkingen voorkomen. </p> <p>Zie <a href="../c-searchpromote-release-notes/c-rn-06-19-14-version-815.md#concept_E8CEBC65A28A4E61BDE69B4B4DA55E73" format="dita" scope="local"> Zoeken en Promote 8.15.0 Release Notes (6/19/2014) </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Taal </p> </td> 
      <td colname="col2"> <p>Het gebrek is <b>Engels (Verenigde Staten)</b>. </p> <p>De geselecteerde taal zorgt ervoor dat de datum en de numerieke waarden volgens de overeenkomsten worden ontleed die in het geselecteerde deel van de wereld worden gebruikt. </p> <p>Wanneer de <span class="uicontrol"> Afwisselende Vormen van Word aan de Vormen van </span> Standaard Afwisselend Word <span class="uicontrol"> of aan het Woordenboek van het </span> Domein <span class="uicontrol"> </span>worden geplaatst, veranderen de woordvormen en de woordeinden volgens de taalregels voor de geselecteerde taal. </p> <p>Door gebrek, wordt het plaatsen van de Taal niet gebruikt om de taal van pagina's te bepalen die van uw website worden gelezen. De taal voor een gelezen pagina wordt bepaald van zijn HTTP- kopballen of van metatags binnen de pagina zelf. Uw website kan pagina's in vele verschillende talen bevatten. Elke pagina wordt correct gelezen en geïndexeerd, ongeacht de taal die hier wordt geselecteerd. </p> <p>Als u een karakter gebruikt van Unicode - reeks het coderen zoals UTF-8 voor sommige pagina's op uw website, zorg ervoor dat de taal voor elk van die pagina's correct wordt gespecificeerd. Als de aangewezen HTTP- kopballen of metatags niet voor uw documenten van Unicode bestaan, kunt u <span class="uicontrol"> Montages </span> &gt; <span class="uicontrol"> Meta-gegevens </span> &gt; <span class="uicontrol"> Injecties gebruiken </span> om de aangewezen taal te specificeren. </p> <p>Controle <span class="uicontrol"> Toepassen op documenten zonder gespecificeerde taal? </span> om de Taal te gebruiken die voor pagina's plaatst die van uw website worden gelezen die geen uitdrukkelijk het plaatsen hebben. Gebruik dit het plaatsen wanneer slechts <i>sommige</i> van uw documenten taalmontages niet hebben. De Montages van het gebruik <span class="uicontrol"> &gt; </span> Meta-gegevens <span class="uicontrol"> &gt; </span> Injecties <span class="uicontrol"> als of </span> geen <i></i> van uw documenten taalmontages hebben, of de reeks van beïnvloede documenten is een bekende en handelbaar kleine lijst. </p> <p>Zie <a href="../c-about-settings-menu/c-about-metadata-menu.md#concept_DA091920671948A0A893A26B3A2FAAE5" type="concept" format="dita" scope="local"> over injecties </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Decompounder gebruiken? </p> </td> 
      <td colname="col2"> <p> <p>Opmerking:  Dit kenmerk wordt alleen gebruikt voor Deens en Duits. Ook, wordt deze eigenschap niet toegelaten door gebrek. Neem contact op met Technische ondersteuning om de functie voor uw gebruik te activeren. Nadat het wordt toegelaten, de <b>Decompounder van het Gebruik?</b> optie verschijnt slechts in de gebruikersinterface als u <span class="uicontrol"> Deens </span> of <span class="uicontrol"> Duits </span> van de <span class="uicontrol"> </span> drop-down lijst selecteert van de Taal die eerder in deze lijst wordt beschreven. </p> </p> <p>Wanneer u Decompounder van het <span class="uicontrol"> Gebruik selecteert? </span>De dienst breidt Deense of Duitse samengestelde woorden uit, die de indexering van samenstellende woorden samen met de oorspronkelijke samengestelde woorden mogelijk maken. </p> <p>Om te zien hoe deze eigenschap werkt, ga woorden in het tekstgebied in, en klik dan <span class="uicontrol"> Test </span>. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Klik op **[!UICONTROL Save Settings]**.
1. Aan voorproef de resultaten van uw veranderingen, klik **[!UICONTROL regenerate your staged site index]** om uw gefaseerde websiteindex te herbouwen.
1. (Facultatief) doe één van het volgende:

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

