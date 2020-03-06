---
description: U kunt de uitbreiding van de resultaten van de onderzoeksvraag met voeten treden.
seo-description: U kunt de uitbreiding van de resultaten van de onderzoeksvraag met voeten treden.
seo-title: Ongeveer de Uitbreiding van de Vraag treedt met voeten
solution: Target
title: Ongeveer de Uitbreiding van de Vraag treedt met voeten
topic: Linguistics,Site search and merchandising
uuid: dfe18004-b8fd-4889-b01c-72a3b0c82b9c
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# Ongeveer de Uitbreiding van de Vraag treedt met voeten{#about-query-expansion-overrides}

U kunt de uitbreiding van de resultaten van de onderzoeksvraag met voeten treden.

## Het gebruiken van de Uitbreiding van de Vraag treedt met voeten {#concept_6895B469B0E044299E93361BFA06B554}

Wanneer u een opheffing van de vraaguitbreiding vormt, creeert u een reeks &quot;regels&quot;. Elke regel zegt, hoofdzakelijk, &quot;breid niet `<this>` in `<that>` op het tijdstip van onderzoek&quot;uit waar een eenvoudig tekstwoord of een uitdrukking, en `<this>` `<that>` is tekstwoord of een uitdrukking, of een classificatie is.

>[!NOTE]
>
>Deze eigenschap wordt niet toegelaten in Onderzoek&amp;Promote, door gebrek. Neem contact op met Technische ondersteuning om de functie voor uw gebruik te activeren. Nadat de Uitbreiding van de Vraag eigenschap met voeten treedt wordt toegelaten, moet u &quot;het&quot;in het gebruikersinterface aanzetten.

**Hoe een Opheffing van de Uitbreiding van de Vraag werkt**

Wanneer een waarde van de Tekst en van de Term in de Uitbreiding van de Vraag wordt gespecificeerd met voeten treedt voeg pagina toe, de codehandelingen op de specifieke bedrading. Wanneer een classificatietype als Termijn, zoals Woordenboeken of de Afwisselende Vormen van Word wordt gespecificeerd, breid geen waarde uit wordt omgezet in om het even welke vorm die door de vermelde classificatie wordt gecreeerd uit.

Bijvoorbeeld, veronderstel dat u de volgende definitie hebt:

`Do Not Expand = "dog"`

`Type = Text`

`Term = "dogs"`

Een zoekopdracht naar &quot;hond&quot;, die zich uitbreidt tot &quot;honden&quot; en &quot;honden&quot; in de vorm van Alternate Word Forms, zou geen &quot;honden&quot; omvatten.

Indien de definitie echter als volgt luidt:

`Do Not Expand = "dog"`

`Type = Alternate Word Forms`

De vraag omvat niet &quot;honden&quot;of &quot;honden&quot; (de beschikbare Afwisselende Vormen van Word voor &quot;hond&quot;.)

U kunt veelvoudige termijnen, veelvoudige classificaties, of allebei specificeren. Nochtans, als u allen als Type selecteert, wordt om het even welke lijst van de veelvoudige termijn doen ineenstorten aan enkel één enkele &quot;allen&quot;ingang.

Als de tekst en de classificatieingangen in om het even welke regel worden gemengd, worden zij gereorganiseerd in het gebruikersinterface om tekstwaarden eerst te tonen. Dit impliceert echter niet of beïnvloedt de orde van evaluatie op het tijdstip van onderzoek niet.

De termijnen van de tekst worden bevestigd om betekenisloze verwijzingen te verwijderen. Namelijk vergelijkt het de termijn met niet uitbreiden waarde en verwijdert de termijn als er een gelijke is. Bovendien, worden de dubbele waarden van de Term, of tekst of classificatie, verwijderd.

Als u een nieuwe regel met toevoegt breid geen waarde uit herhalend een vroegere definitie, worden de Termijnen van de nieuwe definitie toegevoegd aan origineel.

## Het vormen de Uitbreiding van de Vraag treedt met voeten {#task_A087354A509D4997BA275186C224160E}

Het bepalen van en het toevoegen van een opheffing van de Uitbreiding van de Vraag in Onderzoek&amp;Promote.

<!-- 

t_configuring_query_expansion_overrides.xml

 -->

>[!NOTE]
Deze eigenschap wordt niet toegelaten in Onderzoek&amp;Promote, door gebrek. Neem contact op met Technische ondersteuning om de functie voor uw gebruik te activeren. Nadat de Uitbreiding van de Vraag eigenschap met voeten treedt wordt toegelaten, moet u &quot;het&quot;in het gebruikersinterface aanzetten. De eerste stappen hieronder schetsen hoe dat moet.

**Om de Uitbreiding van de Vraag te vormen treedt met voeten**

1. Klik in Zoeken en promoten op **Instellingen** > **Gebruiker** > **Rollen** bekijken.
1. Voor de pagina van de Rollen van de Mening, in de kolom van Acties van de lijst, geeft de klik aan het recht van de rol **** uit die u toegang tot de Uitbreiding van de Vraag wilt verlenen met voeten treedt op het menu van de Taalkunde.
1. Voor de Edit pagina van de Rol, breid de boom van de Taalkunde uit.
1. De uitbreiding van de **Vraag van de controle treedt** met voeten, en klikt dan **sparen Veranderingen**.
1. Klik **Taalkunde** > de Uitbreiding van de **Vraag treedt met voeten**.
1. Klik **toevoegen de Uitbreiding van de Vraag met voeten treedt**.
1. In de Uitbreiding van de Vraag treedt met voeten toevoegt pagina, plaats de opties u wilt.

   <!-- 
   
   r_query_expansion_override_definitions.xml
   
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
      <td colname="col1"> <p>Niet uitbreiden </p> </td> 
      <td colname="col2"> <p>Specificeert het woord of de uitdrukking dat u niet wilt uitbreiden. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Type </p> </td> 
      <td colname="col2"> <p>Selecteer <b>Tekst</b> om een specifiek woord of een uitdrukking te specificeren die rangschikken. Of, selecteer een classificatie om te specificeren dat niet het woord of de uitdrukking uitbreiden niet door de geselecteerde classificatie wordt omgezet. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Termijn </p> </td> 
      <td colname="col2"> <p>Slechts beschikbaar als u <b>Tekst</b> als Type selecteerde. Specificeert het woord of de uitdrukking van de onderzoeksuitbreiding uit te sluiten. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Actie </p> </td> 
      <td colname="col2"> <p> Klik <b>+</b> of <b>-</b> om Termen, respectievelijk, aan de definitie toe te voegen of te schrappen. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Wanneer u wordt gebeëindigd, voegt de klik **toe**.

   Van de Uitbreiding van de Vraag treedt de pagina van Definities met voeten, kunt u de definities uitgeven of schrappen u hebt toegevoegd.
1. Aan voorproef **regenereren de resultaten van uw toevoegingen, regenereert de klik uw gefaseerde plaatsindex** in de blauwe doos om uw gefaseerde websiteindex snel te herbouwen.
1. (Facultatief) doe één van het volgende:

   * Klik op **Live**.

      Zie live- [instellingen bekijken](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)

   * Klik **op Live** drukken.

      Zie [Stadsinstellingen pushing live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)

