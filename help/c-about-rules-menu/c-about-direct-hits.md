---
description: Met directe treffers kunt u een klant omleiden naar een opgegeven URL wanneer de klant naar een overeenkomstige term zoekt. Met dit soort functionaliteit kunt u de navigatie van de zoekopdracht op uw website verbeteren.
solution: Target
title: Info over Direct Hits
topic-legacy: Rules,Site search and merchandising
uuid: 374d63c8-2b82-4165-b543-05b587757baa
exl-id: 251dfa47-f55a-469c-8fca-e187877b7759
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 1%

---

# Info over Directe uren{#about-direct-hits}

Met directe treffers kunt u een klant omleiden naar een opgegeven URL wanneer de klant naar een overeenkomstige term zoekt. Met dit soort functionaliteit kunt u de navigatie van de zoekopdracht op uw website verbeteren.

## Directe uren gebruiken {#concept_C5EE074A19FD4D5B8DD21DB575E35565}

Direct treffers bestaan uit twee hoofdelementen: de URL van uw website en een of meer door komma&#39;s gescheiden zoektermen. Directe treffers worden als volgt gespecificeerd:

```
    website_URL: term
    website_URL: term, term, term
```

Stel dat u een bedrijfswebsite hebt met een pagina die al uw voorwaarden en bepalingen bevat. Wanneer een klant naar uw voorwaarden zoekt in plaats van de resultaten weer te geven, kunt u de klant doorverwijzen naar de pagina met voorwaarden en bepalingen.

```
    https://www.mycompany.com/policies.asp?article=terms: terms and conditions, terms, conditions, security
    https://www.mycompany.com/press/news.asp: press releases, press
```

Als de zoekterm niet overeenkomt met een direct resultaat, worden de zoekresultaten op de gebruikelijke manier geretourneerd.

## Direct treffers configureren {#task_64DFB8C554874C699FCC0C2F26C3669F}

U kunt zoektermen opgeven die een webbrowser omleiden naar een URI in plaats van zoekresultaten te retourneren.

<!-- 

t_configuring_direct_hits.xml

 -->

Lege regels en commentaarregels die beginnen met een &#39;#&#39; (hash) teken zijn toegestaan.

**Directe treffers configureren**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Direct Hits]**.
1. Voer in het veld [!DNL Direct Hits] de URL van uw website en een of meer door komma&#39;s gescheiden zoektermen in.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Directe treffers testen {#task_1E2EA833BF90423AA0DD8C5BBFE77445}

Voordat u live gaat met regels voor directe treffers, kunt u direct raken testen door een term in te voeren.

<!-- 

t_testing_direct_hits.xml

 -->

Als u een termijn test die niet door een directe klapregel wordt behandeld, wordt een bericht getoond latend u kent. In een dergelijk scenario, als de directe raakregel op uw website live was, zouden de onderzoeksresultaten zoals gebruikelijk zijn teruggekeerd. Als u een termijn test die door een directe klapregel wordt behandeld, wordt een bericht getoond latend u dat een omleiding aan gespecificeerde URL is voorgekomen.

**Direct treffers testen**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Direct Hits]**.
1. Voer in het veld [!DNL Test Direct Hits] een zoekterm in en klik op **[!UICONTROL Test]**.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie [De optie Historie gebruiken](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Klik op **[!UICONTROL Live]**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Werkgebiedinstellingen leegmaken live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).
