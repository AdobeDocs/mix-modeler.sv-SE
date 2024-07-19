---
title: Harmoniserade områden
description: Lär dig hur du definierar fält som ska användas för att harmonisera data i Mix Modeler.
feature: Harmonized Data, Harmonized Fields
exl-id: f051279a-1ae9-49bd-a946-abfc34c90413
source-git-commit: 9085363e951a4e306c64ad28f56e2c15b4a6029a
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
| channel_type_at_source | Kanaltyp på Source | Dimension | Sträng |           |
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
| källtyp | Source Type | Dimension | Sträng |           |
| utgifter | Utgift | Mått | Valuta |           |
| trafikkälla | Traffic Source | Dimension | Sträng |           |

{style="table-layout:auto"}

Du kan lägga till, redigera eller ta bort egna harmoniserade fält ovanpå dessa globala harmoniserade fält.

## Hantera harmoniserade fält

En tabell över de tillgängliga harmoniserade fälten finns i Mix Modeler-gränssnittet:

1. Välj ![DataSearch](/help/assets//icons/DataCheck.svg) **[!UICONTROL Harmonized data]** i den vänstra listen.

1. Välj **[!UICONTROL Fields]** i det övre fältet. En tabell över de harmoniserade fälten visas. Om fler sidor är tillgängliga använder du ![Vänsterpil](/help/assets//icons/ChevronLeft.svg) eller ![Högerpil](/help/assets//icons/ChevronRight.svg) vid **[!UICONTROL Page _x _av_x_]** för att flytta mellan sidor i tabellen.

   Tabellkolumnerna anger information om de harmoniserade fälten

   | Kolumnnamn | Information |
   | ---------------------- | ----------|
   | Fältnamn | Namnet på det harmoniserade fältet. |
   | Visningsnamn | Det harmoniserade fältets visningsnamn. Det här visningsnamnet används när du definierar datauppsättningsregler, kontaktpunkter för marknadsföring och konverteringsdefinitioner. |
   | Kategori | Anger om ett harmoniserat datafält är ett [!UICONTROL Dimension], ett [!UICONTROL Metric] eller [!UICONTROL Derived]. En härledd kategori är ett harmoniserat fält som använder en metrisk formeldefinition. |
   | Datatyp | Anger datatypen ([!UICONTROL Number], [!UICONTROL String], [!UICONTROL Currency], [!UICONTROL Date time]). |
   | Skapad den | Datum och tid då det harmoniserade fältet skapades. |
   | Ägare | Anger om ett harmoniserat fält är standardfält ([!UICONTROL Global]) eller om det definieras av dig ([!UICONTROL Client]). |
   | Senast ändrat den | Uppgifter och tid för den senaste ändringen av det harmoniserade fältet. |
   | Formel | Anger formeln för ett harmoniserat fält baserat på en härledd kategori. |

   {style="table-layout:auto"}

1. Om du vill söka efter ett visst harmoniserat fält använder du ![Sök](/help/assets//icons/Search.svg) **[!UICONTROL *Sök i harmoniserat fält *]**.


### Lägg till ett harmoniserat fält

Om du vill lägga till ett harmoniserat fält går du till ![DataSearch](/help/assets//icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** i Mix Modeler:

1. Välj ![Lägg till](/help/assets//icons/AddCircle.svg) **[!UICONTROL Add field]**.

1. I dialogrutan **[!UICONTROL Create]**:

   1. Ange en **[!UICONTROL Field name]**, till exempel `region`.
   1. Ange en **[!UICONTROL Display name]**, till exempel `Region`.
   1. Välj en **[!UICONTROL Category]**: **[!UICONTROL Dimension]**, **[!UICONTROL Metric]** eller **[!UICONTROL Derived]**.

      Ange **[!UICONTROL Formula]** när du väljer **[!UICONTROL Derived]**. Om du vill skapa ett giltigt aritmetiskt uttryck kombinerar du en eller flera mätvärden från **[!UICONTROL Insert Metric]** med en eller flera operatorer **[!UICONTROL + - * / ( )]** . Exempel: `[orders]/[impressions]`

   1. Välj en **[!UICONTROL Data type]**.

      - **[!UICONTROL String]** eller **[!UICONTROL Date time]**, när den valda kategorin är Dimension.
      - **[!UICONTROL Number]** eller **[!UICONTROL Currency]** när den valda kategorin är Metrisk eller Härledd.

   1. Välj **[!UICONTROL Submit]** om du vill lägga till det harmoniserade fältet. Välj **[!UICONTROL Close]** om du vill stänga dialogrutan utan att lägga till det harmoniserade fältet.

      ![Skapa ett fält](/help/assets//create-field.png)


### Redigera ett harmoniserat fält

Du kan bara redigera harmoniserade fält som du skapat tidigare (ägaren är klienten). Du kan inte redigera ett globalt harmoniserat fält.

Om du vill redigera ett harmoniserat fält går du till ![DataSearch](/help/assets//icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** i Mix Modeler:

1. Markera det harmoniserade fält som du vill redigera. Exempel: **[!UICONTROL Region]**.

1. Ändra värden för **[!UICONTROL Display name]**, **[!UICONTROL Category]** och **[!UICONTROL Data type]** i rutan **[!UICONTROL Edit harmonization values]**. Mer information finns i [Lägg till ett harmoniserat fält](#add-a-harmonized-field).

1. Välj **[!UICONTROL Submit]** om du vill använda ändringarna i det harmoniserade fältet.

   ![Redigera ett fält](/help/assets//edit-field.png)

### Radera ett harmoniserat fält

Du kan bara ta bort harmoniserade fält som du skapat tidigare (ägaren är klienten). Du kan inte ta bort ett globalt harmoniserat fält.

Om du vill ta bort ett harmoniserat fält går du till ![DataSearch](/help/assets//icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** i Mix Modeler:

1. Markera det harmoniserade fält som du vill ta bort, till exempel **[!UICONTROL Region]**.

1. Välj ![Ta bort](/help/assets//icons/Delete.svg) **[!UICONTROL Delete]** i den vänstra rutan i **[!UICONTROL Edit harmonization values]**.

   >[!WARNING]
   >
   >   Fältet raderas omedelbart.

