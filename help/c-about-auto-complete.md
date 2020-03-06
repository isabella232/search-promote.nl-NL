---
description: U kunt diverse gebieden van auto-Volledig vormen om de generatie van de auto-volledige toegelaten onderzoeksvorm te controleren, en het dossier autocomplete_data.js, die als deel van de auto-volledige toegelaten onderzoeksvorm inbegrepen is.
seo-description: U kunt diverse gebieden van auto-Volledig vormen om de generatie van de auto-volledige toegelaten onderzoeksvorm te controleren, en het dossier autocomplete_data.js, die als deel van de auto-volledige toegelaten onderzoeksvorm inbegrepen is.
seo-title: Over Auto-Voltooid
solution: Target
subtopic: Auto-Complete
title: Over Auto-Voltooid
topic: Design,Site search and merchandising
uuid: 3dfdd14d-2044-4f01-a5bc-fcb2eb0d5068
translation-type: tm+mt
source-git-commit: 439100ab96f4b597c55b1c1ae38a5778c208e896

---


# Over Auto-Voltooid{#about-auto-complete}

U kunt diverse gebieden van auto-Volledig vormen om de generatie van de auto-volledige toegelaten onderzoeksvorm te controleren, en het dossier autocomplete_data.js, die als deel van de auto-volledige toegelaten onderzoeksvorm inbegrepen is.

## Over Auto-Voltooid {#concept_093A9CD754864BA79B456FE4BEB64578}

Het dossier [!DNL autocomplete_data.js] wordt geregenereerd en gepubliceerd aan het netwerk van de onderzoeksinhoud telkens als er veranderingen zijn die de auto-Volledige pagina van de Opstelling heeft bewaard.

## Automatisch voltooien configureren {#task_F491F2BFC4D24A61BBDC48B9059C11BB}

U kunt de opties vormen en opstelling die de generatie van de auto-volledige toegelaten onderzoeksvorm, en het dossier controleren.

<!-- 

t_configuring_auto-complete.xml

 -->

Nadat u auto-volledig vormt, kunt u de resulterende bron van HTML voor overzicht bekijken. De bron van HTML is wat u kopieert en in de pagina&#39;s van uw website kleeft.

Zie het [onderzoeksformulier voorvertonen zoals het op uw...](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

Zie de [Auto-Volledige Lijst](c-about-auto-complete.md#task_1F8E0F346263443383F8CFD2C7AB35D4)van Word vormen.

Zie Automatische CSS [configureren](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96).

**Automatisch aanvullen configureren**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Auto-Complete Setup]**.
1. Voor de [!DNL Auto-Complete Setup] pagina, plaats de opties die u wilt.

   Zie ook het onderzoeksformulier [voorvertonen zoals het op uw...](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Optie </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Maximale suggesties </p> </td> 
      <td colname="col2"> <p>Specificeert het maximumaantal punten in de auto-volledige suggesties lijst te tonen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Minimale invoertekens </p> </td> 
      <td colname="col2"> <p>Specificeert het aantal karakters dat een klant in de auto-volledige onderzoeksvorm moet typen alvorens het suggesties toont. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Maximum aantal cache </p> </td> 
      <td colname="col2"> <p>Specificeert het maximumaantal eerder gevraagde auto-volledige suggesties om in browser van de klant in het voorgeheugen onder te brengen. Over het algemeen, zou u dit het plaatsen bij het gebrek van 1000 moeten verlaten. </p> <p>Terwijl u browser caching volledig kunt onbruikbaar maken door deze optie aan 0 te plaatsen, wordt het niet geadviseerd. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Formuliernaam </p> </td> 
      <td colname="col2"> <p>Specificeert de "naam"attributen van de auto-volledige toegelaten "vorm"markering van het onderzoeksformulier. Bijvoorbeeld: </p> <p> <span class="filepath"> &lt;form name="SiteSearch" method="get" action="https://sp1004337c.guided.t1.atomz.com" target="_blank"&gt; </span> </p> <p>waar <span class="filepath"> SiteSearch </span> de naamattributen van de vormmarkering is. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ID Div-tag </p> </td> 
      <td colname="col2"> <p>Specificeert de attributen van identiteitskaart van de auto-volledige toegelaten "afd."markering van de onderzoeksvorm. Bijvoorbeeld: </p> <p> <span class="filepath"> &lt;div id="autocomplete"&gt; </span> </p> <p>waarbij <span class="filepath"> autocompletering </span> het kenmerk van de afd.-tag is. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ID invoertag </p> </td> 
      <td colname="col2"> <p>Specificeert de attributen van identiteitskaart van de auto-volledige toegelaten "input"markering van de onderzoeksvorm. Bijvoorbeeld: </p> <p> <span class="filepath"> &lt;invoertype="text" id="q" name="q" /&gt; </span> </p> <p>waarbij <span class="filepath"> q het kenmerk id van de invoertag </span> is. </p> </td> 
      </tr> 
      <tr>
      <td colname="col1"> <p>Schermschaduw </p> </td>
      <td colname="col2"> <p>Voegt een cosmetische dalingsschaduw aan de auto-volledige suggesties lijst toe. </p> </td>
      </tr>
      <tr>
      <td colname="col1"> <p>Pas aan het begin van uitdrukking aan </p> </td>
      <td colname="col2"> <p>Stel slechts resultaten voor die aan het begin van de inputtekst aanpassen. </p> </td>
      </tr>
      <tr>
      <td colname="col1"> <p>Ondersteuning voor UTF-8-tekenset </p> </td>
      <td colname="col2"> <p>Handvat correct niet-ASCII karakters in termen. </p> </td>
      </tr>
    </tbody> 
   </table>

1. Klik op **[!UICONTROL Save Changes]**.
1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## De automatisch-volledige Word-lijst configureren {#task_1F8E0F346263443383F8CFD2C7AB35D4}

Vorm de lijst van woorden en uitdrukkingen die de auto-Volledige vertoningen aan een klant als suggesties.

<!-- 

t_configuring_auto-complete_word_list.xml

 -->

Zie Automatisch [configureren](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB).

Zie Automatische CSS [configureren](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96).

**Om de Auto-Volledige Lijst van Word te vormen**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Auto-Complete Word List]**.
1. Voor de [!DNL Auto-Complete Word List] pagina, plaats de opties die u wilt.

   Zie het [onderzoeksformulier voorvertonen zoals het op uw...](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Optie </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Periode van populaire zoekopdrachten </p> </td> 
      <td colname="col2"> <p> Controleert de tijdspanne voor de opneming van woorden en uitdrukkingen van de recente onderzoeken van een klant. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Maximum aantal zoekopdrachten </p> </td> 
      <td colname="col2"> <p>Controleert het maximumaantal gezochte woorden en uitdrukkingen om in de auto-volledige woordlijst te omvatten. De belangrijkste woorden en zinnen, die ook het meest populair zijn, zijn opgenomen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Veldnaam </p> </td> 
      <td colname="col2"> <p>Elke gebiedsnaam bepaalt de naam van één gebied waarvoor om geïndexeerde waarden te omvatten. Gebruik + en - om gebiedsnamen toe te voegen of te verwijderen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Maximum aantal waarden </p> </td> 
      <td colname="col2"> <p>Bepaalt de maximumtelling van gebiedswaarden die voor de geselecteerde gebiedsnaam worden toegestaan. De hoogste waarden, die ook het meest referenced zijn, zijn inbegrepen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Voeg deze woorden en zinnen toe </p> </td> 
      <td colname="col2"> <p> De auto-volledige woordlijst is bevolkt met de woorden en de uitdrukkingen die op dit gebied vermeld zijn. </p> <p> Klik <span class="uicontrol"> uitgeven </span> om de lijst te zien of woord en uitdrukkingen toe te voegen aan de lijst. Wanneer u wordt gebeëindigd, klik <span class="uicontrol"> sparen Veranderingen </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Verwijder deze woorden en zinnen </p> </td> 
      <td colname="col2"> <p> De ingangen op dit gebied worden niet getoond in de auto-volledige woordlijst. </p> <p> Klik <span class="uicontrol"> uitgeven </span> om de lijst te zien of woord en uitdrukkingen toe te voegen aan de lijst. Wanneer u wordt gebeëindigd, klik <span class="uicontrol"> sparen Veranderingen </span>. </p> <p> De regelmatige uitdrukkingen worden toegestaan in deze lijst. Om een regelmatige uitdrukking in deze lijst te specificeren, begin de lijn met 
        <userinput>
          regexp 
        </userinput> gevolgd door één enkele ruimte, gevolgd door de regelmatige uitdrukking. Om het even welke lijnen in de woordlijst die de regelmatige uitdrukking aanpassen worden verwijderd. </p> <p> <b>Belangrijk</b>: U zou regelmatige uitdrukkingen slechts moeten gebruiken als u eerder met hen in andere toepassingen hebt gewerkt. </p> <p>Zie <a href="c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Regelmatige expressies </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Kwestie negeren </p> </td> 
      <td colname="col2"> <p>De dubbele ingangen in de auto-volledige woordlijst die slechts door alfabetische in hoofdletters/kleine letters verschillen worden verwijderd; alle tekstlijstingangen worden gedwongen in kleine letters. </p> <p>Als u de Auto-Volledige suggesties "eerste gekapitaliseerde brief"of "alle kappen"wilt verschijnen, voeg toe 
        <userinput>
          teksttransformatie: kapitaliseren; 
        </userinput> of 
        <userinput>
          teksttransformatie: hoofddeksel; 
        </userinput> CSS teksteigenschappen aan de auto-Volledige CSS inhoud, onder "/* stijlen voor resultaatpunt */". </p> <p>Zie Automatisch-Volledige CSS <a href="c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96" type="task" format="dita" scope="local"> configureren </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Update op Re-Index </p> </td> 
      <td colname="col2"> <p>De auto-volledige woordlijst wordt automatisch geregenereerd nadat elke succesvolle rekening opnieuw indexeert. </p> </td> 
      </tr> 
    </tbody> 
   </table>

1. Klik op **[!UICONTROL Save Changes]**.
1. (Facultatief) doe om het even welke volgend:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.
   * Klik **[!UICONTROL Preview Word List]** om het even welke veranderingen te bewaren u hebt aangebracht, en dan open [!DNL Auto-Complete Word List Preview] pagina waar u de auto-volledige suggesties lijst kunt herzien. Gebruik de navigatieopties dichtbij de bovenkant van de pagina om de getoonde lijst te herzien en te raffineren. Wanneer u klaar bent, klik **[!UICONTROL Close]** om aan de [!DNL Auto-Complete Word List] pagina terug te keren.

      Zie De optie [Historie](t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Automatische CSS configureren {#task_EECE35DEB6C94F4A8A5B42B4DED76D96}

Gebruik Auto-Volledige CSS om het auto-volledige draperende stijlblad te vormen dat u wilt gebruiken.

<!-- 

t_configuring_auto-complete_css.xml

 -->

Auto-Volledige CSS controleert de inhoud van [!DNL autocomplete_styles.css], die als deel van de auto-volledige toegelaten onderzoeksvorm inbegrepen is. CSS u hier specificeert controleert de visuele presentatie van de auto-volledige voorstellijst. Bij een voorbeeld van de visuele presentatieideeën die mogelijk zijn, zie het volgende:

[https://developer.yahoo.com/yui/examples/autocomplete/ac_skinning.html](https://developer.yahoo.com/yui/examples/autocomplete/ac_skinning.html).

[Het vormen auto-Volledige Lijst](c-about-auto-complete.md#task_1F8E0F346263443383F8CFD2C7AB35D4)van Word.

[Automatisch voltooien](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB)configureren.

Wanneer u klaar bent met het vormen van auto-Volledige CSS, kunt u voorproef de onderzoeksvorm om te zien of is CSS die u specificeerde aanvaardbaar in verschijning en lay-out.

Zie het [onderzoeksformulier voorvertonen zoals het op uw...](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

**Belangrijk**: Om uw douane auto-volledige CSS toe te passen, moet u de commentaarmarkeringen uit de tweede lijn verwijderen die in de code van HTML verschijnt. Dan beweegt u de zelfde lijn aan binnen de hoofdsectie van de pagina die de onderzoeksvorm bevat.

Zie de HTML-code van het zoekformulier [kopiëren in...](c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

**Om auto-Volledige CSS te vormen**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Auto-Complete CSS]**.
1. Op het [!DNL Auto-Complete CSS] tekstgebied, kleef of typ de draperende informatie van het stijlblad die u met de auto-volledige voorstellijst wilt associëren.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Facultatief) doe om het even welke volgend:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Voorproef het onderzoeksformulier aangezien het op uw website zou verschijnen {#task_437B35EFA5424603A08AF8E79E6B4714}

Gebaseerd op uw configuratie van auto-Volledige en auto-Volledige CSS, kunt u voorproef hoe de onderzoeksvorm verschijnt als u de code van HTML aan uw website moest toevoegen.

<!-- 

t_previewing_the_search_form_as_it_would_appear_on_your_website.xml

 -->

Zie Automatisch [configureren](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB).

Zie Automatische CSS [configureren](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96).

Zie de HTML-code van het zoekformulier [kopiëren in...](c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

Zie [Inzamelingen gebruiken in zoekformulieren](c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3).

Zie frames [gebruiken met formulieren](c-appendices/c-searchforms.md#reference_82CDDDA1E37042E4849EBF7EA05407C5).

Zie [Voorbeeld van geavanceerd zoekformulier](c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A).

Zie [Geavanceerde HTML-code](c-appendices/c-searchforms.md#reference_9AAD4A46B68D4D48865508982CB86DB9)voor zoekformulier.

Zie [Geavanceerde sjablooncode](c-appendices/c-searchforms.md#reference_D762C22E754E462DBEECD88D2C3FA579)voor zoekformulieren.

**Aan voorproef het onderzoeksformulier zoals het op uw website zou verschijnen**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Search Form]**.
1. (Facultatief) klik **[!UICONTROL HTML code]** om HTML te zien dat u kopieert en in de pagina&#39;s van uw website kleeft.

## Het kopiëren van de code van HTML van het onderzoeksformulier in de pagina&#39;s van uw website {#task_A3A01EA800F24C0AA33902387E0362C7}

Gebaseerd op uw configuratie van auto-Volledige en auto-Volledige CSS, kunt u voorproef hoe de onderzoeksvorm verschijnt als u de code van HTML aan uw website moest toevoegen.

<!-- 

t_copying_the_html_code_of_the_search_form_into_the_pages_of_your_website.xml

 -->

Zie Automatisch [configureren](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB).

Zie Automatische CSS [configureren](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96).

Zie de HTML-code van het zoekformulier [kopiëren in...](c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

Zie [Inzamelingen gebruiken in zoekformulieren](c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3).

Zie frames [gebruiken met formulieren](c-appendices/c-searchforms.md#reference_82CDDDA1E37042E4849EBF7EA05407C5).

Zie [Voorbeeld van geavanceerd zoekformulier](c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A).

Zie [Geavanceerde HTML-code](c-appendices/c-searchforms.md#reference_9AAD4A46B68D4D48865508982CB86DB9)voor zoekformulier.

Zie [Geavanceerde sjablooncode](c-appendices/c-searchforms.md#reference_D762C22E754E462DBEECD88D2C3FA579)voor zoekformulieren.

**Om de code van HTML van het onderzoeksformulier in de pagina&#39;s van uw website te kopiëren**

1. Klik in het productmenu op **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Form Source]**.

   >[!NOTE]
   >
   >Verander niet de `form name=` waarde in de vormbron.

1. (Facultatief) doe om het even welke volgend:

   * Als u auto-volledige CSS vormde en de stijlen wilt die op de onderzoeksvorm worden toegepast, verwijder de commentaarmarkeringen uit de tweede lijn die in de code van HTML verschijnt. Daarna, beweeg de zelfde lijn aan binnen de hoofdsectie van de pagina die de onderzoeksvorm bevat.
   * Voor maximumprestaties, beweeg de markeringen die bij de bodem van de code van HTML vermeld zijn en plaats hen bij de bodem van de lichaamssectie van elke pagina die de onderzoeksvorm bevat.

1. Kopieer de code en plak het in de Web-pagina&#39;s van uw website waar u het onderzoeksformulier wilt verschijnen.
