---
description: U kunt de uitbreiding van onderzoeksvraagresultaten met voeten treden.
seo-description: U kunt de uitbreiding van onderzoeksvraagresultaten met voeten treden.
seo-title: Info over Overschrijvingen voor Query-uitbreiding
solution: Target
title: Info over Overschrijvingen voor Query-uitbreiding
topic: Linguistics,Site search and merchandising
uuid: dfe18004-b8fd-4889-b01c-72a3b0c82b9c
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e
workflow-type: tm+mt
source-wordcount: '665'
ht-degree: 0%

---


# Info over Overschrijvingen van de Uitbreiding van de Vraag{#about-query-expansion-overrides}

U kunt de uitbreiding van onderzoeksvraagresultaten met voeten treden.

## Het gebruiken van de Uitbreiding van de Vraag treedt {#concept_6895B469B0E044299E93361BFA06B554} met voeten

Wanneer u een opheffing van de vraaguitbreiding vormt, creeert u een reeks &quot;regels&quot;. Elke regel zegt in feite: &quot;Vouw `<this>` niet uit in `<that>` op het moment van zoeken&quot;, waarbij `<this>` een eenvoudig tekstwoord of eenvoudige woordgroep is en `<that>` een tekstwoord of woordgroep of een classificatie.

>[!NOTE]
>
>Deze functie is standaard niet ingeschakeld in Search&amp;Promote. Neem contact op met Technische ondersteuning om de functie voor uw gebruik te activeren. Nadat de functie Overschrijvingen van de Uitbreiding van de Vraag wordt toegelaten, moet u het &quot;aanzetten&quot;in het gebruikersinterface.

**Hoe een Uitbreiding van de Vraag met voeten treedt werkt**

Wanneer een Tekst en Term waarde in de Uitbreiding van de Vraag met voeten treedt toevoegen pagina wordt gespecificeerd, handelt de code op de specifieke bedrading. Wanneer een classificatietype wordt opgegeven als een term, zoals Woordenboeken of Alternatieve Word Forms, wordt de waarde Niet uitbreiden niet geconverteerd naar een formulier dat wordt gemaakt door de opgegeven classificatie.

Stel dat u de volgende definitie hebt:

`Do Not Expand = "dog"`

`Type = Text`

`Term = "dogs"`

Een zoekopdracht naar &quot;hond&quot;, die via Alternate Word Forms &quot;honden&quot; en &quot;honden&quot; omvat, zou geen &quot;honden&quot; omvatten.

Als de definitie echter als volgt luidt:

`Do Not Expand = "dog"`

`Type = Alternate Word Forms`

De query omvat niet &quot;honden&quot; of &quot;honden&quot; (het beschikbare Alternatieve Word Forms voor &quot;honden&quot;.)

U kunt meerdere termen, meerdere classificaties of beide opgeven. Nochtans, als u allen als Type selecteert, wordt om het even welke meervoudige lijst doen ineenstorten aan enkel één enkel &quot;Alle&quot;ingang.

Als tekst- en classificatiegegevens in een regel worden gemengd, worden ze opnieuw ingedeeld in de gebruikersinterface en worden eerst tekstwaarden weergegeven. Dit houdt echter niet in dat de volgorde van de evaluatie op het moment van de zoekactie wordt gewijzigd of gewijzigd.

Teksttermen worden gevalideerd om betekenisloze verwijzingen te verwijderen. Dit betekent dat de term wordt vergeleken met de waarde Niet uitbreiden en dat de term wordt verwijderd als er een overeenkomst is. Daarnaast worden dubbele Term-waarden (tekst of classificatie) verwijderd.

Als u een nieuwe regel toevoegt met de waarde Niet uitbreiden die een eerdere definitie dupliceert, worden de voorwaarden van de nieuwe definitie toegevoegd aan het origineel.

## Het vormen de Uitbreiding van de Vraag treedt met voeten {#task_A087354A509D4997BA275186C224160E}

Het bepalen van en het toevoegen van een opheffing van de Uitbreiding van de Vraag in Search&amp;Promote.

<!-- 

t_configuring_query_expansion_overrides.xml

 -->

>[!NOTE]
Deze functie is standaard niet ingeschakeld in Search&amp;Promote. Neem contact op met Technische ondersteuning om de functie voor uw gebruik te activeren. Nadat de functie Overschrijvingen van de Uitbreiding van de Vraag wordt toegelaten, moet u het &quot;aanzetten&quot;in het gebruikersinterface. De eerste paar stappen hieronder schetsen hoe te om dat te doen.

**Overschrijvingen van de Uitbreiding van de Vraag vormen**

1. Klik in Search&amp;Promote op **Instellingen** > **Gebruiker** > **Rollen weergeven**.
1. Voor de pagina van de Rollen van de Mening, in de kolom van Acties van de lijst, klik **geef** rechts van de rol uit die u toegang tot de Overschrijvingen van de Uitbreiding van de Vraag op het menu van de Taalkunde wilt verlenen.
1. Vouw op de pagina Rol bewerken de taalstructuur uit.
1. Controleer **Overschrijvingen van de Uitbreiding van de vraag**, en klik dan **sparen Veranderingen**.
1. Klik **Taalkundige** > **Overschrijvingen van de Uitbreiding van de vraag**.
1. Klik **Overschrijvingen van de Uitbreiding van de Vraag toevoegen**.
1. Stel de gewenste opties in op de pagina Opheffen voor query-uitbreiding.

   <!-- 
   
   r_query_expansion_override_definitions.xml
   
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
      <td colname="col1"> <p>Niet uitbreiden </p> </td> 
      <td colname="col2"> <p>Hiermee geeft u het woord of de woordgroep op die u niet wilt uitbreiden. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Type </p> </td> 
      <td colname="col2"> <p>Selecteer <b>Tekst</b> om een specifiek woord of een woordkoppeling te specificeren. U kunt ook een classificatie selecteren om op te geven dat het woord of de woordgroep Niet uitbreiden niet wordt omgezet via de geselecteerde classificatie. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Term </p> </td> 
      <td colname="col2"> <p>Alleen beschikbaar als u <b>Tekst</b> als het Type hebt geselecteerd. Hiermee geeft u het woord of de woordgroep op die u wilt uitsluiten van de zoekuitbreiding. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Handeling </p> </td> 
      <td colname="col2"> <p> Klik <b>+</b> of <b>-</b> om Termijnen, respectievelijk, aan de definitie toe te voegen of te schrappen. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Wanneer u wordt gebeëindigd, klik **toevoegen**.

   Van de pagina van de Definities van de Uitbreiding van de Vraag treedt met voeten, kunt u de definities uitgeven of schrappen u hebt toegevoegd.
1. Als u een voorvertoning van de resultaten van uw toevoegingen wilt weergeven, klikt u op **De gefaseerde site-index opnieuw genereren** in het blauwe vak om uw gefaseerde website-index snel opnieuw samen te stellen.
1. (Optioneel) Voer een van de volgende handelingen uit:

   * Klik **Live**.

      Zie [Live-instellingen weergeven](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)

   * Klik **Push Live**.

      Zie [Werkgebiedinstellingen live spoelen](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)

