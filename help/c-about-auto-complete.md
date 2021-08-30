---
description: U kunt diverse gebieden van auto-aanvullen vormen om de generatie van het auto-aanvullen toegelaten onderzoeksformulier te controleren, en het dossier autocomplete_data.js, dat als deel van de auto-aanvullen toegelaten onderzoeksvorm inbegrepen is.
solution: Target
subtopic: Auto-Complete
title: Info Automatisch aanvullen
topic-legacy: Design,Site search and merchandising
uuid: 3dfdd14d-2044-4f01-a5bc-fcb2eb0d5068
exl-id: a1d08c0a-6c68-4da2-88d2-fe953d333536
source-git-commit: 95bf92df17d7832df72e8d883a22f9063e53a18d
workflow-type: tm+mt
source-wordcount: '1486'
ht-degree: 1%

---

# Info Automatisch aanvullen{#about-auto-complete}

U kunt diverse gebieden van auto-aanvullen vormen om de generatie van het auto-aanvullen toegelaten onderzoeksformulier te controleren, en het dossier autocomplete_data.js, dat als deel van de auto-aanvullen toegelaten onderzoeksvorm inbegrepen is.

## Info Automatisch aanvullen {#concept_093A9CD754864BA79B456FE4BEB64578}

Het bestand [!DNL autocomplete_data.js] wordt opnieuw gegenereerd en naar het netwerk met zoekinhoud gepubliceerd telkens wanneer er wijzigingen worden aangebracht die de pagina Setup automatisch aanvullen heeft opgeslagen.

## Automatisch aanvullen configureren {#task_F491F2BFC4D24A61BBDC48B9059C11BB}

U kunt de opties configureren en instellen die het genereren van het automatisch ingevulde zoekformulier en het bestand bepalen.

<!-- 

t_configuring_auto-complete.xml

 -->

Nadat u automatisch aanvullen hebt geconfigureerd, kunt u de resulterende HTML-bron bekijken voor revisie. De HTML-bron is wat u kopieert en plakt op de pagina&#39;s van uw website.

Zie [Voorvertoning van het zoekformulier weergeven zoals dit op uw scherm wordt weergegeven...](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

Zie [De Auto-Volledige Lijst van Word van het Vormen](c-about-auto-complete.md#task_1F8E0F346263443383F8CFD2C7AB35D4).

Zie [Automatisch aanvullen van CSS](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96) configureren.

**Automatisch aanvullen configureren**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Auto-Complete Setup]**.
1. Stel op de pagina [!DNL Auto-Complete Setup] de gewenste opties in.

   Zie ook [Voorvertoning van het zoekformulier weergeven zoals dit op uw scherm wordt weergegeven...](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Maximumaantal suggesties </p> </td> 
      <td colname="col2"> <p>Hiermee geeft u het maximum aantal items op dat in de lijst met automatisch aangevulde suggesties moet worden weergegeven. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Minimale invoertekens </p> </td> 
      <td colname="col2"> <p>Hiermee geeft u het aantal tekens op dat een klant in het automatisch ingevulde zoekformulier moet typen voordat suggesties worden weergegeven. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Maximum aantal cacheitems </p> </td> 
      <td colname="col2"> <p>Geeft het maximumaantal eerder opgevraagde automatisch aangevulde suggesties aan om in de browser van de klant in cache te plaatsen. In het algemeen, zou u dit het plaatsen bij het gebrek van 1000 moeten verlaten. </p> <p>U kunt het in cache plaatsen van browsers volledig uitschakelen door deze optie in te stellen op 0, maar dit wordt niet aanbevolen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Formuliernaam </p> </td> 
      <td colname="col2"> <p>Hiermee geeft u het kenmerk "name" op van de tag "form" van het ingeschakelde zoekformulier dat automatisch wordt ingevuld. Bijvoorbeeld: </p> <p> <span class="filepath"> &lt;form name="SiteSearch" method="get" action="https://sp1004337c.guided.t1.atomz.com" target="_blank"&gt; </span> </p> <p>waarbij <span class="filepath"> SiteSearch </span> het naamkenmerk van de formuliertag is. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Div-tag-id </p> </td> 
      <td colname="col2"> <p>Hiermee geeft u het Id-kenmerk op van de 'div'-tag van het ingeschakelde zoekformulier dat automatisch wordt ingevuld. Bijvoorbeeld: </p> <p> <span class="filepath"> &lt;div id="autocomplete"&gt; </span> </p> <p>waarbij <span class="filepath"> automatisch aanvullen </span> het kenmerk van de div-tag is. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Invoer-id </p> </td> 
      <td colname="col2"> <p>Hiermee geeft u het Id-kenmerk op van de 'input'-tag van het ingeschakelde zoekformulier dat automatisch wordt ingevuld. Bijvoorbeeld: </p> <p> <span class="filepath"> &lt;input type="text" id="q" name="q" /&gt; </span> </p> <p>waarbij <span class="filepath"> q </span> het id-kenmerk van de invoertag is. </p> </td> 
      </tr> 
      <tr>
      <td colname="col1"> <p>Schaduw weergeven </p> </td>
      <td colname="col2"> <p>Hiermee voegt u een cosmetische slagschaduw toe aan de lijst met automatisch aangevulde suggesties. </p> </td>
      </tr>
      <tr>
      <td colname="col1"> <p>Alleen afstemmen aan begin van woordgroep </p> </td>
      <td colname="col2"> <p>Stel alleen resultaten voor die overeenkomen met het begin van de invoertekst. </p> </td>
      </tr>
      <tr>
      <td colname="col1"> <p>Ondersteuning voor UTF-8-tekenset </p> </td>
      <td colname="col2"> <p>U kunt niet-ASCII-tekens op de juiste wijze afhandelen. </p> </td>
      </tr>
    </tbody> 
   </table>

1. Klik op **[!UICONTROL Save Changes]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** als u om het even welke veranderingen wilt terugkeren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Woordenlijst automatisch aanvullen configureren {#task_1F8E0F346263443383F8CFD2C7AB35D4}

Configureer de lijst met woorden en woordgroepen die automatisch aanvullen als suggesties aan de klant weergeeft.

<!-- 

t_configuring_auto-complete_word_list.xml

 -->

Zie [Automatisch aanvullen configureren](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB).

Zie [Automatisch aanvullen van CSS](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96) configureren.

**Automatisch aanvullen van woordenlijst configureren**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Auto-Complete Word List]**.
1. Stel op de pagina [!DNL Auto-Complete Word List] de gewenste opties in.

   Zie [Voorvertoning van het zoekformulier weergeven zoals dit op uw scherm wordt weergegeven...](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Periode voor populaire zoekopdrachten </p> </td> 
      <td colname="col2"> <p> Bepaalt de tijdsperiode voor het opnemen van woorden en woordgroepen uit recente zoekopdrachten van een klant. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Maximum aantal zoekopdrachten </p> </td> 
      <td colname="col2"> <p>Hiermee bepaalt u het maximum aantal gezochte woorden en woordgroepen dat in de lijst met automatisch aanvullen wordt opgenomen. De belangrijkste woorden en zinnen, die ook het populairst zijn, worden opgenomen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Veldnaam </p> </td> 
      <td colname="col2"> <p>Elke veldnaam definieert de naam van één veld waarin geïndexeerde waarden moeten worden opgenomen. Gebruik + en - om veldnamen toe te voegen of te verwijderen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Maximum aantal waarden </p> </td> 
      <td colname="col2"> <p>Hiermee definieert u het maximale aantal veldwaarden dat is toegestaan voor de geselecteerde veldnaam. De hoogste waarden, die ook het meest van verwijzingen zijn, zijn inbegrepen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Voeg deze woorden en uitdrukkingen toe </p> </td> 
      <td colname="col2"> <p> De lijst met automatisch aangevulde woorden wordt gevuld met de woorden en uitdrukkingen die in dit gebied worden vermeld. </p> <p> Klik op <span class="uicontrol"> Bewerken </span> om de lijst weer te geven of om woorden en woordgroepen aan de lijst toe te voegen. Als u klaar bent, klikt u op <span class="uicontrol"> Wijzigingen opslaan </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Deze woorden en woordgroepen verwijderen </p> </td> 
      <td colname="col2"> <p> Items in dit gebied worden niet weergegeven in de woordenlijst die automatisch wordt ingevuld. </p> <p> Klik op <span class="uicontrol"> Bewerken </span> om de lijst weer te geven of om woorden en woordgroepen aan de lijst toe te voegen. Als u klaar bent, klikt u op <span class="uicontrol"> Wijzigingen opslaan </span>. </p> <p> Reguliere expressies zijn toegestaan in deze lijst. Als u een reguliere expressie in deze lijst wilt opgeven, begint u met <code>regexp</code> gevolgd door één spatie, gevolgd door de reguliere expressie. Alle regels in de woordenlijst die overeenkomen met de reguliere expressie worden verwijderd. </p> <p> <b>Belangrijk</b>: U moet reguliere expressies alleen gebruiken als u er in andere toepassingen eerder mee hebt gewerkt. </p> <p>Zie <a href="c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Reguliere expressies </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Hoofdlettergebruik negeren </p> </td> 
      <td colname="col2"> <p>Dubbele items in de woordenlijst voor automatisch aanvullen die alleen verschillen in alfabetische hoofdletters/kleine letters, worden verwijderd. alle vermeldingen in de woordenlijst moeten in kleine letters worden geschreven. </p> <p>Als u de suggesties voor automatisch aanvullen wilt weergeven met de hoofdletter "first letter" of "all caps", voegt u de 
        <code>
          text-transform : capitalize; 
        </code> of 
        <code>
          text-transform : uppercase; 
        </code> CSS-teksteigenschappen aan de CSS-inhoud automatisch aanvullen onder "/* stijlen voor resultaatitem */". </p> <p>Zie <a href="c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96" type="task" format="dita" scope="local"> CSS automatisch aanvullen </a> configureren. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Bijwerken op nieuwe index </p> </td> 
      <td colname="col2"> <p>Automatisch aanvullen van woordenlijst wordt automatisch opnieuw gegenereerd nadat elke account opnieuw is gecompileerd. </p> </td> 
      </tr> 
    </tbody> 
   </table>

1. Klik op **[!UICONTROL Save Changes]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** als u om het even welke veranderingen wilt terugkeren die u hebt aangebracht.
   * Klik op **[!UICONTROL Preview Word List]** om de aangebrachte wijzigingen op te slaan en open vervolgens de pagina [!DNL Auto-Complete Word List Preview] waar u de lijst met automatisch aangevulde suggesties kunt bekijken. Gebruik de navigatieopties boven aan de pagina om de weergegeven lijst te bekijken en te verfijnen. Als u klaar bent, klikt u op **[!UICONTROL Close]** om terug te keren naar de pagina [!DNL Auto-Complete Word List].

      Zie [De optie Historie gebruiken](t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## CSS automatisch aanvullen configureren {#task_EECE35DEB6C94F4A8A5B42B4DED76D96}

Gebruik CSS automatisch aanvullen om de automatisch aangevulde CSS-stijlpagina te configureren die u wilt gebruiken.

<!-- 

t_configuring_auto-complete_css.xml

 -->

CSS automatisch aanvullen bestuurt de inhoud van [!DNL autocomplete_styles.css], die als deel van de auto-aanvullen toegelaten onderzoeksvorm inbegrepen is. Met de CSS die u hier opgeeft, wordt de visuele presentatie van de lijst met automatisch aangevulde suggesties bepaald. Raadpleeg de volgende secties voor een voorbeeld van de mogelijke visuele presentatieideeën:

<!-- 404 DEAD LINK [https://developer.yahoo.com/yui/examples/autocomplete/ac_skinning.html](https://developer.yahoo.com/yui/examples/autocomplete/ac_skinning.html). -->

[Word-lijst](c-about-auto-complete.md#task_1F8E0F346263443383F8CFD2C7AB35D4) automatisch aanvullen configureren.

[Automatisch aanvullen](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB) configureren.

Als u de CSS automatisch aanvullen hebt geconfigureerd, kunt u het zoekformulier bekijken om te zien of de door u opgegeven CSS acceptabel is in weergave en lay-out.

Zie [Voorvertoning van het zoekformulier weergeven zoals dit op uw scherm wordt weergegeven...](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

**Belangrijk**: Als u de aangepaste automatisch aangevulde CSS wilt toepassen, moet u de commentaartags verwijderen uit de tweede regel die in de HTML-code wordt weergegeven. Vervolgens verplaatst u dezelfde regel naar de kopsectie van de pagina die het zoekformulier bevat.

Zie [De HTML-code van het zoekformulier kopiëren naar..](c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

**Automatisch aanvullen van CSS configureren**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Auto-Complete CSS]**.
1. Plak of typ in het tekstveld [!DNL Auto-Complete CSS] de trapsgewijze stijlbladgegevens die u wilt koppelen aan de lijst met automatisch aangevulde suggesties.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een voorbeeld bekijken van het zoekformulier zoals het op uw website wordt weergegeven {#task_437B35EFA5424603A08AF8E79E6B4714}

Op basis van uw configuratie van CSS automatisch aanvullen en automatisch aanvullen kunt u een voorbeeld bekijken van het zoekformulier als u de HTML-code aan uw website wilt toevoegen.

<!-- 

t_previewing_the_search_form_as_it_would_appear_on_your_website.xml

 -->

Zie [Automatisch aanvullen configureren](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB).

Zie [Automatisch aanvullen van CSS](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96) configureren.

Zie [De HTML-code van het zoekformulier kopiëren naar..](c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

Zie [Verzamelingen gebruiken in zoekformulieren](c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3).

Zie [Frames gebruiken met formulieren](c-appendices/c-searchforms.md#reference_82CDDDA1E37042E4849EBF7EA05407C5).

Zie [Voorbeeld van een geavanceerd zoekformulier](c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A).

Zie [Geavanceerde HTML-code voor zoekformulieren](c-appendices/c-searchforms.md#reference_9AAD4A46B68D4D48865508982CB86DB9).

Zie [Geavanceerde sjablooncode voor zoekformulieren](c-appendices/c-searchforms.md#reference_D762C22E754E462DBEECD88D2C3FA579).

**Een voorbeeld van het zoekformulier bekijken zoals het op uw website wordt weergegeven**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Search Form]**.
1. (Optioneel) Klik op **[!UICONTROL HTML code]** om de HTML weer te geven die u kopieert en plakt op de pagina&#39;s van uw website.

## De HTML-code van het zoekformulier naar de pagina&#39;s van uw website kopiëren {#task_A3A01EA800F24C0AA33902387E0362C7}

Op basis van uw configuratie van CSS automatisch aanvullen en automatisch aanvullen kunt u een voorbeeld bekijken van het zoekformulier als u de HTML-code aan uw website wilt toevoegen.

<!-- 

t_copying_the_html_code_of_the_search_form_into_the_pages_of_your_website.xml

 -->

Zie [Automatisch aanvullen configureren](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB).

Zie [Automatisch aanvullen van CSS](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96) configureren.

Zie [De HTML-code van het zoekformulier kopiëren naar..](c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

Zie [Verzamelingen gebruiken in zoekformulieren](c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3).

Zie [Frames gebruiken met formulieren](c-appendices/c-searchforms.md#reference_82CDDDA1E37042E4849EBF7EA05407C5).

Zie [Voorbeeld van een geavanceerd zoekformulier](c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A).

Zie [Geavanceerde HTML-code voor zoekformulieren](c-appendices/c-searchforms.md#reference_9AAD4A46B68D4D48865508982CB86DB9).

Zie [Geavanceerde sjablooncode voor zoekformulieren](c-appendices/c-searchforms.md#reference_D762C22E754E462DBEECD88D2C3FA579).

**De HTML-code van het zoekformulier kopiëren naar de pagina&#39;s van uw website**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Form Source]**.

   >[!NOTE]
   >
   >Wijzig de waarde `form name=` in de formulierbron niet.

1. (Optioneel) Voer een van de volgende handelingen uit:

   * Als u de automatisch aangevulde CSS hebt geconfigureerd en de stijlen op het zoekformulier wilt toepassen, verwijdert u de commentaartags van de tweede regel die in de HTML-code wordt weergegeven. Vervolgens verplaatst u dezelfde regel naar de kopsectie van de pagina die het zoekformulier bevat.
   * Voor maximale prestaties verplaatst u de tags die onder aan de HTML-code staan, en plaatst u deze onder aan de hoofdsectie van elke pagina die het zoekformulier bevat.

1. Kopieer de code en plak deze op de webpagina&#39;s van uw website waar u het zoekformulier wilt weergeven.
