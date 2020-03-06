---
description: De Schoonmaakregels van de Vraag van het gebruik om de inkomende vraag te analyseren en te wijzigen.
seo-description: De Schoonmaakregels van de Vraag van het gebruik om de inkomende vraag te analyseren en te wijzigen.
seo-title: Informatie over regels voor het opschonen van query
solution: Target
title: Informatie over regels voor het opschonen van query
topic: Rules,Site search and merchandising
uuid: 683af81f-f7c0-45f8-9212-e5e7cb82ccca
translation-type: tm+mt
source-git-commit: d07cdc2c88f93eed4cecb0ee8818f7fdea06ee9d

---


# Informatie over regels voor het opschonen van query{#about-query-cleaning-rules}

De Schoonmaakregels van de Vraag van het gebruik om de inkomende vraag te analyseren en te wijzigen.

## Het gebruiken van de Regels van de Schoonmaakbeurt van de Vraag {#concept_17F3CDDC3C8A4128AF092A82B777B86C}

Deze eigenschap wordt vaak gebruikt wanneer u plaatsonderzoek/koopwaar wilt wijzigen gedrag. Bijvoorbeeld, kon u een leeg onderzoek in een populair sleutelwoord in plaats van een &quot;*&quot;onderzoek veranderen, waarbij een populair product wordt bevorderd. U kunt vraag het schoonmaken regels ook gebruiken om een directe klap uit te voeren, waar u aan een URL opnieuw richt. Dit kan bijzonder nuttig zijn wanneer u ontdekt dat iemand naar een product SKU zoekt en u het onderzoek wilt overslaan en aan de pagina van dat product opnieuw richten. Het Schoonmaken van de vraag kan de vraag en de vastgestelde douanevariabelen ook ontmijnen die in recentere stappen van de verwerkingsstroom kunnen worden gebruikt. De het reinigen van de vraag regels worden uitgevoerd opeenvolging voor elke vraag. Om de orde van uw regels te veranderen kunt u belemmering-en-daling gebruiken. De daadwerkelijke orde wordt niet veranderd tot u sparen het.

De vraag schoonmaakregels in een vraag schoonmaakmodule worden onderzocht om te bepalen als om het even welke vraagparameters moeten worden gewijzigd of als om het even welke douanevariabelen moeten worden geplaatst. Elke regel van de vraagschoonmaak bestaat uit twee belangrijke elementen: het optreden van de regel en de facultatieve voorwaarden. Een onbeperkt aantal regels en voorwaarden kan worden gespecificeerd. De orde van deze regels is belangrijk, aangezien het plaatsonderzoek/de merchandising lijnen door de regel vastgestelde regel door regel. Wanneer de voorwaarden van een regel aanpassen, worden alle bijbehorende acties uitgevoerd.

Nadat de vraagreiniging wordt voltooid, worden de resulterende parameters van CGI gebruikt verdergaand. Om het even welke douanevariabelen die werden geplaatst zijn beschikbaar voor gebruik door recentere stadia in de verwerkingsstroom. Door gebrek, verwijdert het systeem automatisch het leiden en het slepen witte ruimte uit de vraagtermijn.

## Informatie over de reinigingsvoorwaarden voor query {#section_BF6F25F94FED4DDEA8600D921EA43A66}

De voorwaarden zijn facultatief. Als u besluit dat de acties voor elke vraag worden gespecificeerd, worden de acties altijd genomen. De voorwaarden kunnen op om het even welke CGI vraagparameter, bestaand koekje, of douanevariabele worden gebaseerd die een vorige regel heeft geplaatst. Het wordt beschouwd als &quot;beste praktijken&quot;voor de eerste vraag schoonmaakregel om voor elke vraag te lopen, waar het bepaalt en alle douanevariabelen initialiseert u van plan bent te gebruiken.

## Informatie over het Schonen van de Vraag Acties {#section_78F74A9B48DE484191CDA95F5B4E7154}

Alle acties binnen een vraag schoonmaakregel die passende voorwaarden heeft worden uitgeoefend. De acties bestaan typisch uit een verrichting, de gegevens waarop om de verrichting uit te voeren, en de waarde aan gebruik.

Zie de lijst van opties in het [Toevoegen van een vraag schoonmaakregel](../c-about-rules-menu/c-about-query-cleaning-rules.md#task_47F43988D3D9485F8AE1DFDA7E00BF54).

## Over omleiden {#section_597481E6194440C0A7B9E6FC901A81C0}

De interface van de direct-Hits laat u een reeks opnieuw richten bepalen die op de inkomende vraagtermijn wordt gebaseerd. Richt binnen het Schonen van de Vraag opnieuw uit breidt dit idee. Nochtans, geeft opnieuw richt u fijnere granularity op wanneer opnieuw richt via het specificeren van voorwaarden plaatsvindt en laat u aan een dynamische URL eerder dan een statische URL opnieuw richten. Wanneer u de omleidingsactie selecteert, wordt de rij bijgewerkt om een tekstvakje te hebben waar u URL specificeert u aan zou willen opnieuw richten. In URL, kunt u variabelen of parameters specificeren die u zou willen substitueren via het insluiten van hen in dubbele krullende steunen. De variabelen van de douane zijn van hogere belangrijkheid dan de parameters van CGI in de vervanging.

## Voorbeelden {#section_DB5047CC38FB4A57B15CAAF9848073E3}

Veronderstel u een kledingdetailhandel met een website hebt. Als de gebruiker Onderzoek zonder enige onderzoekstermijnen klikt, wilt u een onderzoek tegen jeans terugkeren, omdat dat is wat u internationaal gekend voor bent. U wilt ook de vraagtermijn voor een geslacht ontleden zodat u een pre-onderzoeksregel kunt tot stand brengen later, die op de douanevariabele wordt gebaseerd die een verschillend presentatiemalplaatje voor elk geslacht gebruikt.

```
On condition: 
  query q equal 
Perform the following actions: 
  Set query parameter q to value jeans 
 
On condition: 
  Query q matches regular expression wom[e|a]n[s]|girl[s] 
Perform the following actions: 
  Add custom variable gender 
  Set custom variable gender to value female 
 
On condition: 
  Query q matches regular expression men[s]|boy[s] 
Perform the following actions: 
  Add custom variable gender 
  Set custom variable gender to value male
```

MegaElectronic is een grote elektronicawinkel. Door hun zoekgegevens te analyseren, heeft MegaElectronic opgemerkt dat veel van hun barbaarse klanten vaak zoeken naar een product met behulp van de SKU van het product, in plaats van een zoekresultaat voor het enige product te retourneren, zou MegaElectronic graag willen doorverwijzen naar de webpagina die aan die SKU is gekoppeld.

```
On condition: 
  query q matches regular expression ^\D\D\D-\d\d\d\d$ 
Perform the following actions: 
  redirect to https://www.megaelectronic.com/?sku={{q}}
```

## Het toevoegen van een vraag schoonmaakregel {#task_47F43988D3D9485F8AE1DFDA7E00BF54}

U kunt regels bepalen die schoonmaken of de inkomende onderzoeksvraag van een klant uitgeven.

U kunt slechts malplaatjes selecteren die momenteel bestaan. Als u geen malplaatjes hebt, moet u hen eerst bepalen.

Zie [over sjablonen](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5).

**Om een vraag schoonmaakregel toe te voegen**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Query Cleaning]**.
1. Voor de [!DNL Query Cleaning Rules] pagina, klik **[!UICONTROL Add New Rule]**.
1. Op het [!DNL Name] gebied, typ de naam van de nieuwe vraag schoonmaakregel.
1. Voor de [!DNL Add Query Cleaning Rule] pagina, gebruik de drop-down lijsten en tekstgebieden om uw vraag uit te bouwen.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Optie </p> </th> 
      <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Cookie </p> </td> 
      <td colname="col2"> <p>Een HTTP koekje. U kunt voorwaarden bepalen die op koekjes worden gebaseerd die met uw domein worden geassocieerd. Of, u kunt een koekje plaatsen dat met uitgaande onderzoeksresultaten wordt geschreven. De naam en de waarden van koekjes moeten het Uniforme Herkenningsteken van het Middel zijn gecodeerd. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Aangepaste variabele </p> </td> 
      <td colname="col2"> <p>Een user-defined variabele. Voeg, schrap, of plaats een onbeperkte hoeveelheid user-defined variabelen toe. U kunt om het even welke user-defined variabelen hier binnen de Regels van het pre-Onderzoek en de Regels van het post-Onderzoek van verwijzingen voorzien. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Systeemvariabele </p> </td> 
      <td colname="col2"> <p>Alleen-lezen variabelen die zijn ingesteld op het interne systeem dat u kunt controleren. De volgende systeemvariabelen worden ondersteund: </p> <p> 
        <ul id="ul_BC17F1637F27424CA4E8F530C28A3245"> 
          <li id="li_C7DF96EFD7AA4A449D00F7EACCAA0EB1"> <span class="uicontrol"> hostnaam </span> <p>De naam van de servergastheer. </p> </li> 
          <li id="li_F85AB1D2B9374A859657D12B8ED6674B"> <span class="uicontrol"> buik </span> <p>De gevraagde uri zonder het vraagkoord. </p> </li> 
          <li id="li_440149C9EC6E4805B77BBC97BE41542A"> <span class="uicontrol"> arcering </span> <p>Het volledige vraagkoord. </p> </li> 
          <li id="li_F583FC4B0E404858BB3522B33A6F7A0A"> <span class="uicontrol"> milieu </span> <p>"Stadium"of "leef"afhankelijk van of de inkomende vraag naar uw gefaseerde of levende milieu werd verzonden. </p> </li> 
          <li id="li_15902AA49B144D42A5E95D7E8B0FB1E1"> <span class="uicontrol"> verwijzende </span> <p>URL die de klant kwam van. </p> </li> 
          <li id="li_6FEE352DB7A842FCB2EBE1398AD03666"> <span class="uicontrol"> gebruikersagent </span> <p>De "gebruiker-agent"koord van browser van de klant. </p> </li> 
        </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Query-parameter </p> </td> 
      <td colname="col2"> <p>De parameters van CGI gingen tot de vraag over. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Backend Parameter </p> </td> 
      <td colname="col2"> <p>De inkomende vraagparameters worden uiteindelijk vertaald in achterste deelparameters die worden gebruikt om het onderzoek uit te voeren. </p> <p>Zie <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> Achterste onderzoekCGI parameters </a>. </p> <p>De parameters van de steun verschijnen niet op navigatie elementen. Dientengevolge, kunt u om het even welke extra parameters verbergen die u op een onderzoek van uw klanten wilt toepassen. De acties op achterste deelparameters zijn laat-bindend; dat wil zeggen, ze worden toegepast vlak voordat de zoekopdracht wordt verzonden. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Gezicht </p> </td> 
      <td colname="col2"> <p>Speciale parameters van de CGI verbonden aan een bepaald facet. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Rank </p> </td> 
      <td colname="col2"> <p>Laat u specificeren welke rangschikkende regel in het onderzoek te gebruiken. Deze optie verschijnt slechts wanneer u sommige het rangschikken gebieden en het rangschikken bepaalde regels hebt. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Winkel </p> </td> 
      <td colname="col2"> <p>De onderzoeksmotor ontdekt automatisch welke opslag de gebruiker binnen gebaseerd op de gastheernaam of de <span class="codeph"> gs_store </span> vraagparameter is, met de laatstgenoemde die belangrijkheid hebben is. U kunt voorwaarden van de opslag tot stand brengen. In vraag het reinigen slechts, kunt u een actie ook gebruiken om de huidige opslag over-ride te nemen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Laatste regel </p> </td> 
      <td colname="col2"> <p>Wanneer de voorwaarden voor een regel worden voldaan die laatste regelreeks heeft, voert de vraag zuiverende verwerkingsmodule geen extra regels na de actie van de passende regel uit. Dit is nuttig wanneer u acties hebt geplaatst die een recentere regel zullen veroorzaken om aan te passen maar u wilt niet de recentere regel in brand steken. Merk op dat, als de actie van een regel moet uitvoeren opnieuw richt, direct plaatsvindt opnieuw richt, zodat doet het hoofdzakelijk alsof de laatste regel werd geplaatst. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Opschorten </p> </td> 
      <td colname="col2"> <p>Zet het lopen van de regel uit maar schrapt niet de regel. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Klik op **[!UICONTROL Add]**.
1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Een regel voor het reinigen van vragen bewerken {#task_FA2FF1A7E2634350AD703485CBC27CB3}

U kunt bestaande vraag het schoonmaken regels uitgeven die u aan de pagina van de Regels van de Schoonmaak van de Vraag hebt toegevoegd.

**Om een vraag schoonmaakregel uit te geven**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Query Cleaning]**.
1. Voor de [!DNL Query Cleaning Rules] pagina, onder de **[!UICONTROL Actions]** kolom van de lijst, klik **[!UICONTROL Edit]** voor de bijbehorende regel die u wilt uitgeven.
1. Voor de [!DNL Edit Query Cleaning Rule] pagina, gebruik de drop-down lijsten en tekstgebieden om uw vraag uit te bouwen.

   Zie de lijst van opties onder het [Toevoegen van een vraag schoonmaakregel](../c-about-rules-menu/c-about-query-cleaning-rules.md#task_47F43988D3D9485F8AE1DFDA7E00BF54).
1. Klik op **[!UICONTROL Save Changes]**.
1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Het schrappen van een vraag schoonmaakregel {#task_C52D17226B824590B087CAB6970CBB01}

U kunt vraag het reinigen regels schrappen die u niet meer nodig hebt of gebruikt.

Wanneer u een regel schrapt, wordt de orde dat de resterende regels in werking worden gesteld automatisch aangepast om van de schrapping rekenschap te geven.

**Om een vraag schoonmaakregel te schrappen**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Query Cleaning]**.
1. Voor de [!DNL Query Cleaning Rules] pagina, onder de **[!UICONTROL Actions]** kolom van de lijst, klik **[!UICONTROL Delete]** voor de bijbehorende regel die u wilt schrappen.
1. Klik in het [!DNL Confirmation] dialoogvenster op **[!UICONTROL OK]**.
1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Het veranderen van de orde dat de vraag zuiveringsregels in werking stellen {#task_C24012C45A4445468A7FD998017388CA}

U kunt vraag schoonmaakregels opnieuw in orde brengen om de orde te veranderen waarin zij op presentatiemalplaatjes lopen.

De schoonmaakregels van de vraag lopen in de orde dat zij werden bepaald. Hoger het de ordeaantal van een regel, later loopt het in het proces, die vroegere regels trompelen. U bestelt regels opnieuw door een nieuw aantal in de kolom van de Orde van de lijst op de [!DNL Query Cleaning Rules] pagina in te gaan. U kunt belemmering-en-daling op regels ook gebruiken om hun looppasorde te veranderen.

**Om de orde te veranderen dat de vraag zuiveringsregels in werking stellen**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Query Cleaning]**.
1. Op de [!DNL Query Cleaning Rules] pagina, doe één van het volgende:

   * Klik de [!DNL Order] kolomkopbal om de regels in stijgende of dalende orde te sorteren.
   * In de [!DNL Order] kolom, op het tekstgebied links van een naam van de vraagschoonmaakregel, typ het ordeaantal dat u de regel wilt lopen.
   * Sleep een lijstrij aan de positie die u de regel wilt in werking stellen. Alle ordeaantallen worden bijgewerkt om op de nieuwe orde te wijzen waarin de regels lopen.

1. Klik op **[!UICONTROL Save Changes]**.
1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

