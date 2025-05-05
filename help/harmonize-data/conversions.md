---
title: Konverteringar
description: Lär dig hur du skapar konverteringar som du kan använda som en del av att harmonisera data i Mix Modeler.
feature: Harmonized Data, Conversions
exl-id: a8559426-452a-43e8-9a60-0c0bc97d863c
source-git-commit: 935b179e31d1b677a8c83b1566c02b7aaa617e8d
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# Konverteringar

Konverteringshändelser är affärsmål som identifierar effekten av marknadsföringsaktiviteter. Exempel: e-handelsorder, butiksköp, webbplatsbesök och så vidare.

Ni definierar marknadsföringskonverteringar för attribueringsanalys.

## Hantera konverteringar

Om du vill se en tabell över tillgängliga konverteringar i gränssnittet Mix Modeler:

1. Välj ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** i den vänstra listen.

1. Välj **[!UICONTROL Conversions]** i det övre fältet. En tabell över konverteringarna visas.

Tabellkolumnerna anger information om konverteringen:

| Kolumnnamn | Information |
| --- | ---|
| Namn | Namnet på konverteringen. |
| Intäkter | Det harmoniserade datamått som ska användas för att beräkna intäkter från en konvertering. |
| Konverteringsmått | Det harmoniserade datamått som ska användas som konverteringsmått för analys. |
| Kategori | Konverteringskategorin för konverteringen. |
| Skapad | Datum och tid då konverteringen skapades. |
| Senast ändrad | Datum och tid för den senaste ändringen av konverteringen. |


## Lägga till en konvertering

Om du vill lägga till en konvertering går du till ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Conversion]** i Mix Modeler:

1. Välj ![Lägg till](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add a conversion]**.

1. I dialogrutan **[!UICONTROL Create conversion]**:

   1. Ange ett namn för **[!UICONTROL Conversion]**, till exempel `Store Conversions`.

   1. Definiera **[!UICONTROL Conversion category]**.

      1. Välj ett värde från **[!UICONTROL *Välj harmonisera..*]**, till exempel `Conversion types`.

      1. Välj ett värde för operatorn ![Chevron](/help/assets/icons/ChevronDown.svg), till exempel **[!UICONTROL is]**.

      1. Välj ett värde från **[!UICONTROL *Välj värde *]**&#x200B;eller ange ett värde, till exempel **[!UICONTROL Store]**.

   1. Välj ett harmoniserat fält från **[!UICONTROL Conversion metric for analysis]**, till exempel **[!UICONTROL Orders]**.

   1. Välj ett harmoniserat fält från **[!UICONTROL Revenue field]**, till exempel **[!UICONTROL Gross Demand]**.

   1. Välj **[!UICONTROL Create]** om du vill skapa konverteringen. Om du vill avbryta skapandet av en konvertering väljer du **[!UICONTROL Cancel]**.

      ![Alt-text](/help/assets/create-conversion.png)

1. När konverteringen skapas läggs den till i konverteringstabellen.


## Visa detaljer

Så här visar du information om en konvertering:

1. Välj ![Mer](/help/assets/icons/More.svg) när du hovrar över ett konverteringsnamn i tabellen.

1. Välj ![Visa](/help/assets/icons/ViewDetail.svg) **Visa information**. En dialogruta med information om konverteringen. Mer information finns i [Lägg till en konvertering](#add-a-conversion). Välj **[!UICONTROL Cancel]** för att stänga dialogrutan.

## Visa rapport

Så här visar du en rapport om en konvertering:

1. Välj ![Mer](/help/assets/icons/More.svg) när du hovrar över ett konverteringsnamn i tabellen.

1. Välj ![GraphTrend](/help/assets/icons/GraphTrend.svg) **Visa rapport**. En dialogruta visar en rapport om konverteringen.

   ![Konverteringsrapport](../assets/conversion-view-report.png)

   * Om du vill ändra granulariteten som ska rapporteras väljer du ett värde i listrutan **[!UICONTROL Weekly]**.
   * Om du vill ändra den period som ska rapporteras anger du ett start- och slutdatum eller använder ![Kalender](/help/assets/icons/Calendar.svg) för att definiera en period i kalenderpopup-fönstret.

1. Välj **[!UICONTROL Close]** för att stänga dialogrutan.

## Ta bort en konvertering

Ta bort en konvertering:

1. Välj ![Ta bort](/help/assets/icons/Delete.svg) **Ta bort** när du hovrar över ett konverteringsnamn i tabellen.
1. I bekräftelsedialogrutan i dialogrutan **[!UICONTROL Delete conversion]** väljer du **[!UICONTROL Delete]** om du vill ta bort konverteringen permanent.
