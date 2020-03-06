---
description: U kunt vormen betekende u zodat de klanten suggesties voor geldige onderzoekstermijnen worden gegeven wanneer zij onderzoeken hebben geprobeerd die hebben ontbroken. De suggesties worden gevormd door spelling te zoeken en correcties in de onderzoekstermijnen te typen die in een geldig onderzoek resulteren.
seo-description: U kunt vormen betekende u zodat de klanten suggesties voor geldige onderzoekstermijnen worden gegeven wanneer zij onderzoeken hebben geprobeerd die hebben ontbroken. De suggesties worden gevormd door spelling te zoeken en correcties in de onderzoekstermijnen te typen die in een geldig onderzoek resulteren.
seo-title: Over Bedoelde je
solution: Target
title: Over Bedoelde je
topic: Linguistics,Site search and merchandising
uuid: c5973541-3d6b-4fc9-bad4-66d4d3559fe8
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# Over Bedoelde je{#about-did-you-mean}

U kunt vormen betekende u zodat de klanten suggesties voor geldige onderzoekstermijnen worden gegeven wanneer zij onderzoeken hebben geprobeerd die hebben ontbroken. De suggesties worden gevormd door spelling te zoeken en correcties in de onderzoekstermijnen te typen die in een geldig onderzoek resulteren.

## Het vormen betekende u {#task_B539D6A0043547EFB1CA19B67E762371}

U kunt maken hoe onderzoekssuggesties [!DNL site search/merchandising] maakt wanneer de vraag van een klant geen, of minimale, onderzoeksresultaten terugkeert.

<!-- 

t_configuring_did_you_mean.xml

 -->

**Om te vormen bedoelde u**

1. Klik in het productmenu op **[!UICONTROL Linguistics]** > **[!UICONTROL Did You Mean]**.
1. Voor de [!DNL Did You Mean] pagina, in **Remove gaan deze Woorden uit de tekstgebied van Suggesties** , ruimte of lijn gescheiden woorden in om ongewenste suggesties te filtreren.

   Dit zijn woorden in uw onderzoeksindex die niet verschijnen zoals geadviseerde alternatieve onderzoekstermijnen. U kunt om het even welk woord uitsluiten dat een patroon door het gebruik van regelmatige uitdrukkingen aanpast. Anders, enkel wordt het nauwkeurige woord verwijderd.

1. Plaats **Deed u opties bedoelt** die u wilt.

   <!-- 
   
   r_did_you_mean_options.xml
   
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
      <td colname="col1"> <p>Suggestiealgoritme </p> </td> 
      <td colname="col2"> <p>Past aan hoe ver de software gaat om suggesties te vinden. Als een gebruiker een fout van één letter maakt, komen alle algoritmen met de zelfde suggesties. De reden is omdat het slechts één vergt uitgeven om tot een werkende suggestie te komen, en alle algoritmen vinden woorden die dicht bij origineel zijn. Maar wanneer de originele onderzoekstermijnen niet gelijkaardig aan bestaande termijnen in de index zijn, blijven de <b>Diepe</b> en de <b>Dubbele Algoritmen van de Suggestie van Spellers</b> naar mogelijke suggesties zoeken. Dit scenario is nuttig als een klant een juiste naam probeert die moeilijk is te typen, en zij klinken uit de namen. Nochtans, als u slechts gelijkaardige suggesties wilt verschijnen, kunt u het <b>Snelle</b> algoritme kiezen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Standaardtelling van te tonen suggesties </p> </td> 
      <td colname="col2"> <p>Specificeert het aantal van Bedoelde u term suggesties (0-20) die u wilt tonen wanneer het onderzoek van een klant geen resultaten terugkeert. Het gebrek is 3. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Minimale woordlengte suggestie </p> </td> 
      <td colname="col2"> <p>De prunes betekenden u termijnen door het minimale aantal brieven voor een voorgesteld woord te specificeren. </p> <p>Bijvoorbeeld, als u de waarde aan 4 plaatst, stelt de software geen woord voor dat 1, 2, of 3 lange karakters is. Als u een waarde van 0 specificeert, worden geen korte woorden verwijderd uit de term suggesties. Als u een hoge waarde specificeert, resulteert het gewoonlijk in geen termijnsuggesties. De standaardwaarde is 3. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Minimale indexfrequentie </p> </td> 
      <td colname="col2"> <p> Specificeert het minimumaantal tijden een woord in de index moet verschijnen alvorens het in Deed u woordenboek omvat is. </p> <p>U kunt geen negatief aantal op het gebied specificeren. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Zoek naar voorgestelde termijn als geen resultaten </p> </td> 
      <td colname="col2"> <p>Automatisch opnieuw zoeken naar de eerste voorgestelde term wanneer de zoekopdracht van een klant geen resultaten oplevert en er ten minste één is... Bedoelde u een term suggestie. </p> <p>U kunt de volgende markeringen in uw presentatiemalplaatje gebruiken om erop te wijzen dat het plaatsonderzoek/de handel drijven automatisch naar een verschillende termijn zoekt: </p> <p> <code>&nbsp;&lt;guided-if-suggestion-autosearch&gt;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Search&nbsp;for&nbsp;&lt;guided-param&nbsp;gsname="q"&nbsp;/&gt;&nbsp;instead&nbsp;of&nbsp;guided-suggestion-original-query&nbsp;/&gt;&nbsp;&lt;/guided-if-suggestion-autosearch&gt;</code> </p> <p>U kunt hier ook andere suggesties tonen. </p> <p> <code>&nbsp;&lt;guided-if-suggestion-autosearch&gt;&nbsp;&nbsp;There&nbsp;was&nbsp;0&nbsp;matches&nbsp;for&nbsp;&lt;guided-suggestion-original-query&nbsp;/&gt;&nbsp;&nbsp;&nbsp;Did&nbsp;You&nbsp;Mean&nbsp;&lt;guided-param&nbsp;gsname="q"&gt;?&nbsp;Here&nbsp;are&nbsp;the&nbsp;results&nbsp;for&nbsp;that&nbsp;search.&nbsp;&nbsp;&nbsp;Or&nbsp;Did&nbsp;You&nbsp;Mean&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-suggestions&gt;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-suggestion-link&gt;&lt;guided-suggestion&nbsp;/&gt;&lt;/guided-suggestion-link&gt;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-suggestions&gt;&nbsp;&lt;/guided-if-suggestion-autosearch&gt;</code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Suggesties doen vanwege lage resultaten </p> </td> 
      <td colname="col2"> <p>Als een klant naar een termijn zoekt die minder dan tien resultaten oplevert, controleert de onderzoeksmotor om te zien of heeft het een suggestie die meer dan 100 resultaten kan opleveren. Als het, kunt u de volgende markeringen gebruiken om aan de gebruiker erop te wijzen dat terwijl zij resultaten hebben, zij naar iets anders kunnen willen zoeken: </p> <p> <code>&nbsp;&lt;guided-if-suggestion-low-results&gt; &nbsp;&nbsp;You&nbsp;have&nbsp;a&nbsp;low&nbsp;result&nbsp;count&nbsp;for&nbsp;&lt;Search&nbsp;for&nbsp;guided-param&nbsp;gsname="q"&gt;.&nbsp;&nbsp;Did&nbsp;you&nbsp;mean:&nbsp;&lt;guided-suggestion&gt;&lt;guided-suggestion-link&gt;&lt;guided-suggestion&nbsp;/&gt;&lt;/guided-suggestion-link&gt;&lt;guided-if-not-last&gt;,&nbsp;&lt;/guided-if-not-last&gt;&lt;/guided-suggestions&gt;&nbsp;&lt;/guided-if-suggestion-low-results&gt;</code> </p> <p> In het bovengenoemde scenario, wordt het aantal suggesties gecontroleerd door de waarde die in <span class="uicontrol"> Standaard telling van te tonen</span>suggesties wordt gespecificeerd. De lage en hoge drempel zijn configureerbaar door de opties hieronder. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Doe suggesties wanneer de eerste resultaten minder dan </p> </td> 
      <td colname="col2"> <p>Controleert het aantal resultaten wanneer het systeem begint om suggesties aan te bieden. </p> <p>Deze optie verschijnt slechts wanneer u controleert <span class="uicontrol"> doe suggesties toe te schrijven aan lage resultaten</span>. </p> <p>Het gebrek is 10. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Een suggestie moet minstens zoveel resultaten opleveren </p> </td> 
      <td colname="col2"> <p>De suggesties van filters die wegens lage resultaten in primair onderzoek door hun resultaattelling worden gemaakt. </p> <p>Deze optie verschijnt slechts wanneer u controleert <span class="uicontrol"> doe suggesties toe te schrijven aan lage resultaten</span>. </p> <p>Het gebrek is 100. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Klik **sparen Veranderingen**.
1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

