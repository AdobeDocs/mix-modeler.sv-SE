---
title: Marknadsföringskontaktytor
description: Lär dig hur du skapar kontaktytor för marknadsföring som kan användas för att harmonisera data i Adobe Mix-modelleraren.
feature: Harmonized Data, Marketing Touch Points
source-git-commit: ac17f5a9fcf036c8e689879578e4b745b789cea3
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---


# Marknadsföringskontaktytor

Marknadsföringskontaktytorna är marknadshändelser på mottagarnivå, individ- och cookienivå som används för att utvärdera effekten av marknadsinvesteringar på numeriska eller intäktsbaserade konverteringar.

Ni definierar kontaktytor för marknadsföring för att hjälpa er med attribueringsanalys.

## Hantera kontaktytor för marknadsföring

Om du vill se en tabell över tillgängliga kontaktytor för marknadsföring i modellgränssnittet för Adobe Mix:

1. Välj ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** från den vänstra listen.

1. Välj **[!UICONTROL Marketing touchpoint]** i det övre fältet. En tabell över kontaktytorna kring marknadsföring visas.

Tabellkolumnerna anger information om kontaktytan för marknadsföring:

| Kolumnnamn | Information |
| --- | ---|
| Namn | Namnet på kontaktytan för marknadsföring. |
| Utgiftsmått | Det harmoniserade datamått som ska användas för att beräkna kontaktytskostnaden. |
| Volymmått | Det harmoniserade datamått som ska användas för att beräkna kontaktytans volym. |
| Skapad | Datum och tid då kontaktytan för marknadsföring skapades. |
| Senast ändrad | Datum och tid för den senaste ändringen av kontaktytan för marknadsföring. |

{style="table-layout:auto"}

## Lägg till en kontaktyta för marknadsföring

Om du vill lägga till en kontaktyta för marknadsföring går du till ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Marketing touchpoint]** gränssnitt i Adobe Mix-modelleraren:

1. Välj ![Lägg till](../assets/icons/AddCircle.svg) Lägg till kontaktyta för marknadsföring.

1. I **[!UICONTROL Marketing touchpoint]** -dialogrutan.

   1. Ange ett namn för **[!UICONTROL Touchpoint Name]**, till exempel `Luma Touchpoint`.

   1. Definiera en **[!UICONTROL Touchpoint rule]**.

      1. Välj ett värde från **[!UICONTROL *Välj harmonisera...*]**, till exempel **[!UICONTROL Brand]**.

      1. Välj ett värde för operatorn ![Chevron](../assets/icons/ChevronDown.svg), till exempel **[!UICONTROL is]**.

      1. Välj ett värde från **[!UICONTROL *Välj värde *]**eller ange ett värde, till exempel **[!DNL Luma]**.

   1. Välj ett harmoniserat fält från **[!UICONTROL Touchpoint volume]**, till exempel **[!UICONTROL Impressions]**.

   1. Välj ett harmoniserat fält från **[!UICONTROL Touchpoint spend]**, till exempel **[!UICONTROL Cost]**.

      ![Marknadsföringskontaktyta](../assets/create-touchpoint.png)

   1. Om du vill skapa en kontaktyta för marknadsföring väljer du **[!UICONTROL Create]**. Om du vill avbryta skapandet av en kontaktyta väljer du **[!UICONTROL Cancel]** .

1. När kontaktytan skapas läggs den till i tabellen med kontaktytor för marknadsföring.

