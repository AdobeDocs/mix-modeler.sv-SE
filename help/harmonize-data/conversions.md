---
title: Konverteringar
description: Lär dig hur du skapar konverteringar som du kan använda som en del av att harmonisera data i Mix Modeler.
feature: Harmonized Data, Conversions
source-git-commit: 08cfd4239f6bcaf885565f3ae04cbd51869e8c00
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 1%

---


# Konverteringar

Konverteringshändelser är affärsmål som identifierar effekten av marknadsföringsaktiviteter. Exempel: e-handelsorder, butiksköp, webbplatsbesök och så vidare.

Ni definierar marknadsföringskonverteringar för attribueringsanalys.

## Hantera konverteringar

Om du vill se en tabell över tillgängliga konverteringar i gränssnittet Mix Modeler:

1. Välj ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** från den vänstra listen.

1. Välj **[!UICONTROL Conversions]** i det övre fältet. En tabell över konverteringarna visas.

Tabellkolumnerna anger information om konverteringen:

| Kolumnnamn | Information |
| --- | ---|
| Namn | Namnet på konverteringen. |
| Intäkter | Det harmoniserade datamått som ska användas för att beräkna intäkter från en konvertering. |
| Konverteringsmått | Det harmoniserade datamått som ska användas som konverteringsmått för analys. |
| Skapad | Datum och tid då konverteringen skapades. |
| Senast ändrad | Datum och tid för den senaste ändringen av konverteringen. |

{style="table-layout:auto"}

## Lägga till en konvertering

Så här lägger du till en konvertering i ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Conversion]** gränssnitt i Mix Modeler:

1. Välj ![Lägg till](../assets/icons/AddCircle.svg) **[!UICONTROL Add a conversion]**.

1. I **[!UICONTROL Create Conversion]** dialog:

   1. Ange ett namn för **[!UICONTROL Conversion]**, till exempel `Store Conversions`.

   1. Definiera **[!UICONTROL Conversion category]**.

      1. Välj ett värde från **[!UICONTROL *Välj harmonisera...*]**, till exempel `Conversion Type`.

      1. Välj ett värde för operatorn ![Chevron](../assets/icons/ChevronDown.svg), till exempel **[!UICONTROL is]**.

      1. Välj ett värde från **[!UICONTROL *Välj värde *]**eller ange ett värde, till exempel **[!UICONTROL Store]**.

   1. Välj ett harmoniserat fält från **[!UICONTROL Conversion metric for analysis]**, till exempel **[!UICONTROL Orders]**.

   1. Välj ett harmoniserat fält från **[!UICONTROL Revenue field]**, till exempel **[!UICONTROL Gross Demand]**.

   1. Skapa konverteringen genom att välja **[!UICONTROL Create]**. Om du vill avbryta skapandet av en konvertering väljer du **[!UICONTROL Cancel]**.

      ![Alt-text](../assets/create-conversion.png)

1. När konverteringen skapas läggs den till i konverteringstabellen.
