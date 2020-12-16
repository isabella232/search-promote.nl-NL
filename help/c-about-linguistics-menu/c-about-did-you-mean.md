---
description: U kunt vormen Bedoelde u zodat de klanten suggesties voor geldige onderzoekstermijnen krijgen wanneer zij onderzoeken hebben geprobeerd die ontbroken hebben. Suggesties worden gevormd door spelling te zoeken en correcties in de zoektermen te typen die resulteren in een geldige zoekopdracht.
seo-description: U kunt vormen Bedoelde u zodat de klanten suggesties voor geldige onderzoekstermijnen krijgen wanneer zij onderzoeken hebben geprobeerd die ontbroken hebben. Suggesties worden gevormd door spelling te zoeken en correcties in de zoektermen te typen die resulteren in een geldige zoekopdracht.
seo-title: Info Bedoelde je
solution: Target
title: Info Bedoelde je
topic: Linguistics,Site search and merchandising
uuid: c5973541-3d6b-4fc9-bad4-66d4d3559fe8
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e
workflow-type: tm+mt
source-wordcount: '776'
ht-degree: 0%

---


# Info Bedoelde u{#about-did-you-mean}

U kunt vormen Bedoelde u zodat de klanten suggesties voor geldige onderzoekstermijnen krijgen wanneer zij onderzoeken hebben geprobeerd die ontbroken hebben. Suggesties worden gevormd door spelling te zoeken en correcties in de zoektermen te typen die resulteren in een geldige zoekopdracht.

## Bezig met configureren: {#task_B539D6A0043547EFB1CA19B67E762371}

U kunt bepalen hoe [!DNL site search/merchandising] zoeksuggesties doet wanneer de vraag van een klant geen, of minimale, onderzoeksresultaten terugkeert.

<!-- 

t_configuring_did_you_mean.xml

 -->

**Om te vormen bedoelde u**

1. Klik in het productmenu op **[!UICONTROL Linguistics]** > **[!UICONTROL Did You Mean]**.
1. Voer op de pagina [!DNL Did You Mean] in het tekstveld **Deze woorden verwijderen uit Suggestions** spatie- of regelgescheiden woorden in om ongewenste suggesties te filteren.

   Dit zijn woorden in uw zoekindex die niet worden weergegeven als aanbevolen alternatieve zoektermen. U kunt elk woord dat overeenkomt met een patroon uitsluiten door middel van reguliere expressies. Anders wordt alleen het exacte woord verwijderd.

1. Stel de gewenste **Bedoelde opties** in.

   <!-- 
   
   r_did_you_mean_options.xml
   
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
      <td colname="col1"> <p>Suggestiealgoritme </p> </td> 
      <td colname="col2"> <p>Hiermee past u aan hoe ver de software gaat om suggesties te vinden. Als een gebruiker een fout maakt van één letter, komen alle algoritmen met dezelfde suggesties. De reden is dat er maar één bewerking nodig is om tot een werksuggestie te komen. Alle algoritmen vinden woorden die dicht bij het origineel liggen. Maar als de oorspronkelijke zoektermen niet overeenkomen met bestaande termen in de index, blijven de <b>Diep</b> en <b>Onjuiste spellers</b> Suggestie-algoritmen zoeken naar mogelijke suggesties. Dit scenario is nuttig als een klant een juiste naam probeert die moeilijk is te typen, en zij uit de namen klinken. Als u echter alleen vergelijkbare suggesties wilt weergeven, kunt u het algoritme <b>Quick</b> kiezen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Standaardaantal suggesties dat moet worden weergegeven </p> </td> 
      <td colname="col2"> <p>Hier geeft u het aantal suggesties voor termen (0-20) op dat u wilt weergeven wanneer de zoekopdracht van een klant geen resultaten oplevert. De standaardwaarde is 3. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Minimale woordlengte van suggestie </p> </td> 
      <td colname="col2"> <p>Bedoelde afbreekstreepjes door het minimale aantal letters voor een voorgesteld woord op te geven. </p> <p>Als u de waarde bijvoorbeeld instelt op 4, stelt de software geen woord voor dat 1, 2 of 3 tekens lang is. Als u de waarde 0 opgeeft, worden er geen korte woorden verwijderd uit de term suggesties. Als u een hoge waarde opgeeft, levert dit meestal geen suggesties voor termen op. De standaardwaarde is 3. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Minimale indexfrequentie </p> </td> 
      <td colname="col2"> <p> Hiermee geeft u op hoe vaak een woord minimaal in de index moet staan voordat het wordt opgenomen in het woordenboek Bedoelt u. </p> <p>U kunt geen negatief getal opgeven in het veld. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Zoeken naar een term die kan worden gebruikt als er geen resultaten zijn </p> </td> 
      <td colname="col2"> <p>Automatisch herzoekt u naar de eerste voorgestelde term wanneer de zoekopdracht van een klant geen resultaten oplevert en er ten minste één suggestie voor een term is gevonden. </p> <p>U kunt de volgende labels in uw presentatiesjabloon gebruiken om aan te geven dat bij het zoeken/verhandelen van sites automatisch naar een andere term wordt gezocht: </p> <p> <code>&nbsp;&lt;guided-if-suggestion-autosearch&gt;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Search&nbsp;for&nbsp;&lt;guided-param&nbsp;gsname="q"&nbsp;/&gt;&nbsp;instead&nbsp;of&nbsp;guided-suggestion-original-query&nbsp;/&gt;&nbsp;&lt;/guided-if-suggestion-autosearch&gt;</code> </p> <p>U kunt hier ook andere suggesties weergeven. </p> <p> <code>&nbsp;&lt;guided-if-suggestion-autosearch&gt;&nbsp;&nbsp;There&nbsp;was&nbsp;0&nbsp;matches&nbsp;for&nbsp;&lt;guided-suggestion-original-query&nbsp;/&gt;&nbsp;&nbsp;&nbsp;Did&nbsp;You&nbsp;Mean&nbsp;&lt;guided-param&nbsp;gsname="q"&gt;?&nbsp;Here&nbsp;are&nbsp;the&nbsp;results&nbsp;for&nbsp;that&nbsp;search.&nbsp;&nbsp;&nbsp;Or&nbsp;Did&nbsp;You&nbsp;Mean&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-suggestions&gt;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-suggestion-link&gt;&lt;guided-suggestion&nbsp;/&gt;&lt;/guided-suggestion-link&gt;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-suggestions&gt;&nbsp;&lt;/guided-if-suggestion-autosearch&gt;</code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Suggesties doen vanwege lage resultaten </p> </td> 
      <td colname="col2"> <p>Als een klant naar een term zoekt die minder dan tien resultaten oplevert, controleert het zoekprogramma of deze een suggestie heeft die meer dan 100 resultaten oplevert. Als dit het geval is, kunt u de volgende labels gebruiken om de gebruiker te laten weten dat hij of zij resultaten heeft geboekt, maar mogelijk naar iets anders heeft willen zoeken: </p> <p> <code>&nbsp;&lt;guided-if-suggestion-low-results&gt; &nbsp;&nbsp;You&nbsp;have&nbsp;a&nbsp;low&nbsp;result&nbsp;count&nbsp;for&nbsp;&lt;Search&nbsp;for&nbsp;guided-param&nbsp;gsname="q"&gt;.&nbsp;&nbsp;Did&nbsp;you&nbsp;mean:&nbsp;&lt;guided-suggestion&gt;&lt;guided-suggestion-link&gt;&lt;guided-suggestion&nbsp;/&gt;&lt;/guided-suggestion-link&gt;&lt;guided-if-not-last&gt;,&nbsp;&lt;/guided-if-not-last&gt;&lt;/guided-suggestions&gt;&nbsp;&lt;/guided-if-suggestion-low-results&gt;</code> </p> <p> In het bovenstaande scenario, wordt het aantal suggesties gecontroleerd door de waarde die in <span class="uicontrol"> Standaardtelling van te tonen suggesties </span> wordt gespecificeerd. De lage en hoge drempel zijn configureerbaar door de opties hieronder. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Suggesties doen als de oorspronkelijke resultaten minder zijn dan </p> </td> 
      <td colname="col2"> <p>Controleert het aantal resultaten wanneer het systeem begint om suggesties aan te bieden. </p> <p>Deze optie wordt alleen weergegeven wanneer u <span class="uicontrol"> Suggesties maken inschakelt vanwege een laag resultaat</span>. </p> <p>De standaardwaarde is 10. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Een suggestie moet minstens zoveel resultaten opleveren </p> </td> 
      <td colname="col2"> <p>Hiermee filtert u suggesties die worden gedaan als gevolg van lage resultaten in de primaire zoekopdracht op basis van het aantal resultaten. </p> <p>Deze optie wordt alleen weergegeven wanneer u <span class="uicontrol"> Suggesties maken inschakelt vanwege een laag resultaat</span>. </p> <p>De standaardwaarde is 100. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Klik **Wijzigingen opslaan**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

