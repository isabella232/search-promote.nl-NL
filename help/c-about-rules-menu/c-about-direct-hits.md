---
description: De directe hits laten u een klant aan een gespecificeerde URL opnieuw richten wanneer de klantenonderzoeken naar een passende termijn. Dit soort functionaliteit laat u de navigatie van het onderzoek van uw website verbeteren.
seo-description: De directe hits laten u een klant aan een gespecificeerde URL opnieuw richten wanneer de klantenonderzoeken naar een passende termijn. Dit soort functionaliteit laat u de navigatie van het onderzoek van uw website verbeteren.
seo-title: Ongeveer Directe Hits
solution: Target
title: Ongeveer Directe Hits
topic: Rules,Site search and merchandising
uuid: 374d63c8-2b82-4165-b543-05b587757baa
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# Ongeveer Directe Hits{#about-direct-hits}

De directe hits laten u een klant aan een gespecificeerde URL opnieuw richten wanneer de klantenonderzoeken naar een passende termijn. Dit soort functionaliteit laat u de navigatie van het onderzoek van uw website verbeteren.

## Directe uren gebruiken {#concept_C5EE074A19FD4D5B8DD21DB575E35565}

Directe hits bestaan uit twee hoofdelementen: de URL van uw website en een of meer komma-begrensde zoektermen. Directe hits worden als volgt gespecificeerd:

```
    website_URL: term
    website_URL: term, term, term
```

Bijvoorbeeld, veronderstel dat u een collectieve website met een pagina hebt die elk van uw termijnen en voorwaarden specificeert. Wanneer een klant naar uw voorwaarden en bepalingen zoekt, in plaats van de resultaten weer te geven, kunt u de klant doorverwijzen naar de pagina met voorwaarden en bepalingen.

```
    https://www.mycompany.com/policies.asp?article=terms: terms and conditions, terms, conditions, security
    https://www.mycompany.com/press/news.asp: press releases, press
```

Als de vraagtermijn geen directe klappen aanpast, zijn de onderzoeksresultaten teruggekeerd op de gebruikelijke manier.

## Directe hits configureren {#task_64DFB8C554874C699FCC0C2F26C3669F}

U kunt onderzoekstermijnen specificeren die Webbrowser aan URI in plaats van het terugkeren van onderzoeksresultaten opnieuw richten.

<!-- 

t_configuring_direct_hits.xml

 -->

De lege lijnen en de commentaarlijnen die met een karakter &quot;#&quot;beginnen (knoeiboel) worden toegelaten.

**Om directe klappen te vormen**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Direct Hits]**.
1. Op het [!DNL Direct Hits] gebied, ga URL van uw website, en één of meerdere komma-afgebakende onderzoekstermijnen in.
1. Klik op **[!UICONTROL Save Changes]**.
1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Testresultaten {#task_1E2EA833BF90423AA0DD8C5BBFE77445}

Alvorens u directe klapregels levend duwt, kunt u directe klappen testen door een termijn in te gaan.

<!-- 

t_testing_direct_hits.xml

 -->

Als u een termijn test die niet door een directe klapregel wordt behandeld, wordt een bericht getoond latend u het weten. In een dergelijk scenario, als de directe klapregel op uw website levend was, zouden de onderzoeksresultaten zoals gebruikelijk zijn teruggekeerd. Als u een termijn test die door een directe klapregel wordt behandeld, wordt een bericht getoond latend u weet dat opnieuw richt aan gespecificeerde URL is voorgekomen.

**Om directe hits te testen**

1. Klik in het productmenu op **[!UICONTROL Rules]** > **[!UICONTROL Direct Hits]**.
1. Op het [!DNL Test Direct Hits] gebied, ga een onderzoekstermijn in, en klik dan **[!UICONTROL Test]**.
1. (Facultatief) doe één van het volgende:

   * Klik **[!UICONTROL History]** om het even welke veranderingen terug te keren die u hebt aangebracht.

      Zie De optie [Historie](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)gebruiken.

   * Klik op **[!UICONTROL Live]**.

      Zie live-instellingen [bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Klik op **[!UICONTROL Push Live]**.

      Zie [Stadsmontages van het Pushing leven](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

