---
title: Marknadsföringskontaktytor
description: Lär dig hur du skapar kontaktytor för marknadsföring som en del i arbetet med att harmonisera data i Mix Modeler.
feature: Harmonized Data, Marketing Touch Points
exl-id: 42851107-7568-4bc9-92ca-3cba713a522e
source-git-commit: 6751cea9155bab54c9c8405a57151323f570c477
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 0%

---

# Marknadsföringskontaktytor {#marketing-touchpoints}

>[!CONTEXTUALHELP]
>id="harmonizeddata_marketingtouchpoints_create"
>title="Marknadsföringskontaktytor"
>abstract="Marknadsföringskontaktytorna är marknadshändelser på mottagarnivå, individ- och cookienivå som används för att utvärdera effekten av marknadsinvesteringar på numeriska eller intäktsbaserade konverteringar.<br/><br/>Du kan inte konfigurera modellen med kontaktytor som har överlappande data och det måste finnas minst en kontaktyta med utgifter."


Marknadsföringskontaktytorna är marknadshändelser på mottagarnivå, individ- och cookienivå som används för att utvärdera effekten av marknadsinvesteringar på numeriska eller intäktsbaserade konverteringar.

Ni definierar kontaktytor för marknadsföring för att hjälpa er med attribueringsanalys.

## Hantera kontaktytor för marknadsföring

Om du vill se en tabell över tillgängliga kontaktytor för marknadsföring i Mix Modeler-gränssnittet:

1. Välj ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** i den vänstra listen.

1. Välj **[!UICONTROL Marketing touchpoint]** i det övre fältet. En tabell över kontaktytorna kring marknadsföring visas. Om fler sidor är tillgängliga använder du ![Vänsterpil](/help/assets/icons/ChevronLeft.svg) eller ![Högerpil](/help/assets/icons/ChevronRight.svg) vid **[!UICONTROL Page _x _av_x_]** för att flytta mellan sidor i tabellen.

Tabellkolumnerna anger information om kontaktytan för marknadsföring:

| Kolumnnamn | Information |
| --- | ---|
| Namn | Namnet på kontaktytan för marknadsföring. |
| Utgiftsmått | Det harmoniserade datamått som ska användas för att beräkna kontaktytskostnaden. |
| Volymmått | Det harmoniserade datamått som ska användas för att beräkna kontaktytans volym. |
| Regel | Den kontaktpunktsregel som ska användas. |
| Skapad | Datum och tid då kontaktytan för marknadsföring skapades. |
| Senast ändrad | Datum och tid för den senaste ändringen av kontaktytan för marknadsföring. |


## Lägg till en kontaktyta för marknadsföring

Om du vill lägga till en kontaktyta för marknadsföring går du till ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Marketing touchpoint]** i Mix Modeler:

1. Välj ![Lägg till](/help/assets/icons/AddCircle.svg) Lägg till kontaktyta för marknadsföring.

1. I dialogrutan **[!UICONTROL Marketing touchpoint]**.

   1. Ange ett namn för **[!UICONTROL Touchpoint Name]**, till exempel `Luma Touchpoint`.

   1. Definiera en **[!UICONTROL Touchpoint rule]**.

      1. Välj ett värde från **[!UICONTROL *Välj harmoniserat *]**, till exempel **[!UICONTROL Brand]**.

      1. Välj ett värde för operatorn ![Chevron](/help/assets/icons/ChevronDown.svg), till exempel **[!UICONTROL is]**.

      1. Välj ett värde från **[!UICONTROL *Välj värde *]**eller ange ett värde, till exempel **[!DNL Luma]**.

   1. Välj ett harmoniserat fält från **[!UICONTROL Touchpoint volume]**, till exempel **[!UICONTROL Impressions]**.

   1. Välj ett harmoniserat fält från **[!UICONTROL Touchpoint spend]**, till exempel **[!UICONTROL Cost]**.

      ![Marknadsföringskontaktyta](/help/assets/create-touchpoint.png)

   1. Välj **[!UICONTROL Create]** om du vill skapa kontaktytan för marknadsföring. Om du vill avbryta skapandet av en kontaktyta för marknadsföring väljer du **[!UICONTROL Cancel]** .

1. När kontaktytan skapas läggs den till i tabellen med kontaktytor för marknadsföring.


## Visa detaljer

Så här visar du information om en kontaktyta:

1. Välj ![Mer](/help/assets/icons/More.svg) när du hovrar över ett namn på en kontaktyta för marknadsföring i tabellen.

1. Välj ![Visa](/help/assets/icons/ViewDetail.svg) **Visa**. En dialogruta visar detaljer om kontaktytan för marknadsföring. Mer information finns i [Lägg till en kontaktyta för marknadsföring](#add-a-marketing-touchpoint). Välj **[!UICONTROL Cancel]** för att stänga dialogrutan.


## Visa rapport

Så här visar du en rapport om en kontaktyta:

1. Välj ![Mer](/help/assets/icons/More.svg) när du hovrar över ett namn på en kontaktyta för marknadsföring i tabellen.

1. Välj ![GraphTrend](/help/assets/icons/GraphTrend.svg) **Visa rapport**. En dialogruta visar en rapport om kontaktytan för marknadsföring.

   ![Vyrapport för marknadsföringskontaktyta](../assets/marketingtouchpoint-view-report.png)

   * Om du vill ändra granulariteten som ska rapporteras väljer du ett värde i listrutan **[!UICONTROL Weekly]**.
   * Om du vill ändra den period som ska rapporteras anger du ett start- och slutdatum eller använder ![Kalender](/help/assets/icons/Calendar.svg) för att definiera en period i kalenderpopup-fönstret.

1. Välj **[!UICONTROL Close]** för att stänga dialogrutan.

## Ta bort en kontaktyta för marknadsföring

Så här tar du bort en kontaktyta för marknadsföring:

1. Välj ![Ta bort](/help/assets/icons/Delete.svg) **Ta bort** när du hovrar över ett namn på en marknadsföringskontaktyta i tabellen.
1. I bekräftelsedialogrutan i dialogrutan **[!UICONTROL Delete touchpoint]** väljer du **[!UICONTROL Delete]** om du vill ta bort kontaktytan för marknadsföring permanent.

