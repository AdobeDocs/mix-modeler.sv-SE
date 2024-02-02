---
title: Konverteringar
description: Lär dig hur du skapar konverteringar som du kan använda som en del av att harmonisera data i Mix Modeler.
feature: Harmonized Data, Conversions
exl-id: a8559426-452a-43e8-9a60-0c0bc97d863c
source-git-commit: 86732fe30637aa72ced232d9f331a3cc64baa39b
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

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
| Kategori | Konverteringskategorin för konverteringen. |
| Skapad | Datum och tid då konverteringen skapades. |
| Senast ändrad | Datum och tid för den senaste ändringen av konverteringen. |

{style="table-layout:auto"}

## Lägga till en konvertering

Så här lägger du till en konvertering i ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Conversion]** gränssnitt i Mix Modeler:

1. Välj ![Lägg till](../assets/icons/AddCircle.svg) **[!UICONTROL Add a conversion]**.

1. I **[!UICONTROL Create conversion]** dialog:

   1. Ange ett namn för **[!UICONTROL Conversion]**, till exempel `Store Conversions`.

   1. Definiera **[!UICONTROL Conversion category]**.

      1. Välj ett värde från **[!UICONTROL *Välj harmonisera...*]**, till exempel `Conversion types`.

      1. Välj ett värde för operatorn ![Chevron](../assets/icons/ChevronDown.svg), till exempel **[!UICONTROL is]**.

      1. Välj ett värde från **[!UICONTROL *Välj värde *]**eller ange ett värde, till exempel **[!UICONTROL Store]**.

   1. Välj ett harmoniserat fält från **[!UICONTROL Conversion metric for analysis]**, till exempel **[!UICONTROL Orders]**.

   1. Välj ett harmoniserat fält från **[!UICONTROL Revenue field]**, till exempel **[!UICONTROL Gross Demand]**.

   1. Om du vill skapa konverteringen väljer du **[!UICONTROL Create]**. Om du vill avbryta skapandet av en konvertering väljer du **[!UICONTROL Cancel]**.

      ![Alt-text](../assets/create-conversion.png)

1. När konverteringen skapas läggs den till i konverteringstabellen.


## Visa en konvertering

Visa en konvertering:

1. Välj ![Mer](../assets/icons/More.svg) när du hovrar över ett konverteringsnamn i tabellen.

1. Välj ![Visa](../assets/icons/ViewDetail.svg) **Visa**. En dialogruta med information om konverteringen. Se [Lägga till en konvertering](#add-a-conversion) för mer information. Välj **[!UICONTROL Cancel]** för att stänga dialogrutan.


## Ta bort en konvertering

Ta bort en konvertering:

1. Välj ![Ta bort](../assets/icons/Delete.svg) **Ta bort** när du hovrar över ett konverteringsnamn i tabellen.
1. I **[!UICONTROL Delete conversion]** dialogrutans bekräftelsedialogruta **[!UICONTROL Delete]** om du vill ta bort konverteringen permanent.
