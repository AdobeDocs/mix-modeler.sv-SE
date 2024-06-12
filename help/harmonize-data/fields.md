---
title: Harmoniserade områden
description: Lär dig hur du definierar fält som ska användas för att harmonisera data i Mix Modeler.
feature: Harmonized Data, Harmonized Fields
exl-id: f051279a-1ae9-49bd-a946-abfc34c90413
source-git-commit: fecb122f6e2e8ae532babd0e2964ad200174a032
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 0%

---

# Harmoniserade områden

Med harmoniserade fält kan du definiera fält för i princip samma data, som kommer från olika källor, där vart och ett har en egen definition av dessa data. En klickmätare kan till exempel definieras och namnges på olika sätt beroende på datakällan. Med ett klickharmoniserat fält kan du definiera en gemensam nomenklatur för ett klickmått baserat på de olika källorna med klickdata.

Med harmoniserade fält kan du definiera de fält som du vill använda som en del av arbetsflödet för att harmonisera data. De fält du definierar kan användas för att definiera datauppsättningsregler, marknadsföringskontaktytor och konverteringar.

## Globala harmoniseringsområden

De standardiserade fälten för global harmonisering i Mix Modeler är följande:


| Fältnamn | Visningsnamn | Kategori | Datatyp | Kommentar |
| ---------------------- | ---------------------- | --------- | --------- | --------- |
| varumärke | Varumärke | Dimension | Sträng |           |
| kampanj | Campaign | Dimension | Sträng |           |
| kanal | Kanal | Dimension | Sträng |           |
| channel_id | Kanal-ID | Dimension | Sträng |           |
| channel_type_at_source | Kanaltyp vid källa | Dimension | Sträng |           |
| kanal | Kanal | Dimension | Sträng |           |
| klickningar | Klickningar | Mått | Nummer |           |
| konversionstyp | Konverteringstyp | Dimension | Sträng |           |
| kostnad | Kostnad | Mått | Valuta |           |
| datauppsättning | Datauppsättning | Dimension | Sträng |           |
| date_type | Datumtyp | Dimension | Sträng | dag, vecka |
| e-postmeddelande | Skickade e-postmeddelanden | Mått | Nummer |           |
| event_date | Datum | Dimension | Datum och tid |           |
| bruttoefterfrågan | Bruttoefterfrågan | Mått | Valuta |           |
| visningar | Besvingar | Mått | Nummer |           |
| last_updated_date | Senast uppdaterat | Dimension | Datum och tid |           |
| länkbesök | Länka besök | Mått | Nummer |           |
| mediatyp | Medietyp | Dimension | Sträng |           |
| net_sales | Nettoförsäljning | Mått | Valuta |           |
| order | Beställningar | Mått | Nummer |           |
| källtyp | Källtyp | Dimension | Sträng |           |
| utgifter | Utgift | Mått | Valuta |           |
| trafikkälla | Trafikkälla | Dimension | Sträng |           |

{style="table-layout:auto"}

Du kan lägga till, redigera eller ta bort egna harmoniserade fält ovanpå dessa globala harmoniserade fält.

## Hantera harmoniserade fält

En tabell över de tillgängliga harmoniserade fälten finns i Mix Modeler-gränssnittet:

1. Välj ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** från den vänstra listen.

1. Välj **[!UICONTROL Fields]** i det övre fältet. En tabell över de harmoniserade fälten visas. Om det finns fler tillgängliga sidor använder du ![Pil vänster](../assets/icons/ChevronLeft.svg) eller ![Högerpil](../assets/icons/ChevronRight.svg) på **[!UICONTROL Page _x _av_x_]** för att flytta mellan sidor i tabellen.

   Tabellkolumnerna anger information om de harmoniserade fälten

   | Kolumnnamn | Information |
   | ---------------------- | ----------|
   | Fältnamn | Namnet på det harmoniserade fältet. |
   | Visningsnamn | Det harmoniserade fältets visningsnamn. Det här visningsnamnet används när du definierar datauppsättningsregler, kontaktpunkter för marknadsföring och konverteringsdefinitioner. |
   | Kategori | Anger om ett harmoniserat datafält är ett [!UICONTROL Dimension], a [!UICONTROL Metric] eller [!UICONTROL Derived]. En härledd kategori är ett harmoniserat fält som använder en metrisk formeldefinition. |
   | Datatyp | Anger datatypen ([!UICONTROL Number], [!UICONTROL String], [!UICONTROL Currency], [!UICONTROL Date time]). |
   | Skapad den | Datum och tid då det harmoniserade fältet skapades. |
   | Ägare | Anger om ett harmoniserat fält är standardfält ([!UICONTROL Global]) eller definieras av dig ([!UICONTROL Client]). |
   | Senast ändrat den | Uppgifter och tid för den senaste ändringen av det harmoniserade fältet. |
   | Formel | Anger formeln för ett harmoniserat fält baserat på en härledd kategori. |

   {style="table-layout:auto"}

1. Om du vill söka efter ett visst harmoniserat fält använder du ![Sök](../assets/icons/Search.svg) **[!UICONTROL *Sök i harmoniserat fält *]**.


### Lägg till ett harmoniserat fält

Lägga till ett harmoniserat fält i ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** i Mix Modeler:

1. Välj ![Lägg till](../assets/icons/AddCircle.svg) **[!UICONTROL Add field]**.

1. I **[!UICONTROL Create]** dialog:

   1. Ange en **[!UICONTROL Field name]**, till exempel `region`.
   1. Ange en **[!UICONTROL Display name]**, till exempel `Region`.
   1. Välj en **[!UICONTROL Category]**: **[!UICONTROL Dimension]**, **[!UICONTROL Metric]** eller **[!UICONTROL Derived]**.

      När du väljer **[!UICONTROL Derived]**, ange en **[!UICONTROL Formula]**. Om du vill skapa ett giltigt aritmetiskt uttryck kombinerar du en eller flera mätvärden från **[!UICONTROL Insert Metric]** med en eller flera operatorer **[!UICONTROL + - * / ( )]** . Exempel: `[orders]/[impressions]`

   1. Välj en **[!UICONTROL Data type]**.

      - **[!UICONTROL String]** eller **[!UICONTROL Date time]**, när markerad kategori är Dimension.
      - **[!UICONTROL Number]** eller **[!UICONTROL Currency]** när den valda kategorin är Metrisk eller Härledd.

   1. Välj **[!UICONTROL Submit]** att lägga till det harmoniserade fältet. Välj **[!UICONTROL Close]** att stänga dialogen utan att lägga till det harmoniserade fältet.

      ![Skapa ett fält](../assets/create-field.png)


### Redigera ett harmoniserat fält

Du kan bara redigera harmoniserade fält som du skapat tidigare (ägaren är klienten). Du kan inte redigera ett globalt harmoniserat fält.

Redigera ett harmoniserat fält i dialogrutan ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** i Mix Modeler:

1. Markera det harmoniserade fält som du vill redigera. Till exempel: **[!UICONTROL Region]**.

1. I **[!UICONTROL Edit harmonization values]** ruta, ändra värden för **[!UICONTROL Display name]**, **[!UICONTROL Category]** och **[!UICONTROL Data type]**. Se [Lägg till ett harmoniserat fält](#add-a-harmonized-field) för mer information.

1. Välj **[!UICONTROL Submit]** tillämpa ändringarna på det harmoniserade fältet.

   ![Redigera ett fält](../assets/edit-field.png)

### Radera ett harmoniserat fält

Du kan bara ta bort harmoniserade fält som du skapat tidigare (ägaren är klienten). Du kan inte ta bort ett globalt harmoniserat fält.

Radera ett harmoniserat fält i dialogrutan ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** i Mix Modeler:

1. Markera det harmoniserade fält som du vill ta bort, till exempel **[!UICONTROL Region]**.

1. Välj ![Ta bort](../assets/icons/Delete.svg) **[!UICONTROL Delete]** från **[!UICONTROL Edit harmonization values]** vänster ruta.

   >[!WARNING]
   >
   >   Fältet raderas omedelbart.

