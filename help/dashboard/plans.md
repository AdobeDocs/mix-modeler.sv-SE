---
title: Prestanda att planera
description: Lär dig hur du använder Performance för att planera i Mix Modeler.
feature: Dashboard, Plans, Models
exl-id: 930fc1d5-8e28-4610-af7b-c4ec91f86a8a
source-git-commit: 7834a0c4a5fd18902b73e7c307f61847bee05bc0
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 0%

---

# Prestanda att planera

>[!NOTE]
>
>Fliken **[!UICONTROL Performance to pan]** [!BADGE Beta]{type=Informative} i Mix Modeler ![Home](/help/assets/icons/Home.svg) **[!UICONTROL Overview]** är en betafunktion som kan komma att ändras. Funktionen är tillgänglig för ett begränsat antal kunder.

Fliken **[!UICONTROL Plans]** [!BADGE Beta]{type=Informative} i Mix Modeler ![Home](/help/assets/icons/Home.svg) **[!UICONTROL Overview]** innehåller en kontrollpanel för spårning som du kan använda för att övervaka hur väl marknadsföringen fungerar i förhållande till planen. Du kan spåra faktiska prestanda kontra planerade prestanda med statuskort och visualiseringar.

Kontrollpanelen hjälper dig att identifiera luckor, upptäcka risker eller möjligheter och göra vältajmade justeringar av dina planer och budgetar.

Så här väljer du vilka data som ska visas för KPI-statuskort och visualiseringar:

* Välj en plan i listrutan **[!UICONTROL Plan name]** med hjälp av alternativet **[!UICONTROL _Välj en plan.._]**.

* Ange en datumperiod. Om du vill ändra datumperioden anger du ett startdatum och ett slutdatum manuellt eller väljer en datumperiod med ![Kalender](/help/assets/icons/Calendar.svg).

På fliken **[!UICONTROL Plans]** [!BADGE Beta]{type=Informative} visas:

* [KPI-statuskort](#kpi-status-cards):

   * [Budget](#budget)
   * [Intäkter](#revenue)
   * [avkastning](#roi)
   * [KPI](#kpi)

* [Visualiseringar](#visualizations):
   * [*Mått*](#metric-actual-vs-planned)
   * [*Mått*](#metric-actual-vs-planned-by-granularity)
   * [Kanal ](#channel-metric-by-granularity)
   * [*Mått*](#metric-vs-metric-by-channel)
   * [*Mått*](#metric-by-granularity)
   * [*Mått*](#metric-by-channel)

## KPI-statuskort

![KPI-statuskort](../assets/performance-to-plan-kpi-cards.png)


### Budget

En cirkelformad förloppsvisualisering som visar hur era marknadsföringsutgifter står i jämförelse med budgeten för er plan för datumperioden.

### Intäkter

En cirkulär förloppsvisualisering som visar hur de faktiska intäkterna står i jämförelse med de planerade målintäkterna för datumperioden.


### avkastning

En radvisualisering som visar ROI för datumperioden.


### KPI

En radvisualisering som visar KPI för datumperioden.

Så här väljer du en annan KPI:

1. Välj ![Redigera](/help/assets/icons/Edit.svg).
1. Välj en KPI i listrutan **[!UICONTROL KPI status card]** i dialogrutan **[!UICONTROL KPI]**. Tillgängliga alternativ är: [!UICONTROL Conversions], [!UICONTROL CPA], [!UICONTROL Revenue], [!UICONTROL ROI] och [!UICONTROL Spend].


## Visualiseringar

Sex visualiseringar finns tillgängliga och du kan redigera var och en av de sex visualiseringarna.

Om du vill ändra storlek på en visualisering använder du handtaget ┛ längst ned till höger. Om du vill flytta en visualisering drar och släpper du bara visualiseringen till önskad plats.

Du kan hovra över valfri rad, stapel eller spridningselement i en visualisering för att visa ett popup-fönster med ytterligare information.

![Visualisering](../assets/performance-to-plan-visualizations.png)

### *Mått*: Faktiskt kontra planerat

En staplad fältvisualisering som jämför de valda mätvärdena för aktuella, planerade till-datum och summor.


### *Mått*: Faktiskt kontra planerat av *granularitet*

En radinvisualisering som visar faktiska och planerade värden för det valda mätvärdet och den valda granulariteten.


### Kanal *metrisk* av *granularitet*

En staplad stapelvisualisering som visar staplade staplar som visar kanaler för det valda mätvärdet och den valda granulariteten.


### *Mått* kontra *Mått* per kanal

En spridningsvisualisering som visar en spridningspunkt för kanaler över de valda mätvärdena.


### *Mått* av *granularitet*

En fältvisualisering som visar faktiska och planerade värden för det valda måttet.


### *Mått* efter kanal

En flerradsvisualisering som visar det valda måttet över den valda granulariteten.


### Redigera en visualisering

Så här redigerar du en visualisering:

1. Välj ![Redigera](/help/assets/icons/Edit.svg) för att öppna dialogrutan **[!UICONTROL Edit data]**.
1. Beroende på visualiseringen kan du ändra:

   * Ett eller två mått: Välj ett mått i listrutan **[!UICONTROL Select metric]**.

      * För avkastningsbaserade planer är alternativen: [!UICONTROL Conversions], [!UICONTROL CPA], [!UICONTROL Revenue], [!UICONTROL ROI], [!UICONTROL Spend] och [!UICONTROL Volume].
      * För CPA-baserade planer är alternativen: [!UICONTROL Conversions], [!UICONTROL CPA], [!UICONTROL Spend] och [!UICONTROL Volume].
   * **[!UICONTROL Granularity]**: Välj antingen **[!UICONTROL date ranges]** eller **[!UICONTROL week]** i listrutan **[!UICONTROL Granularity]**.

   I **[!UICONTROL Preview]** ser du hur ändringarna skiljer sig från visualiseringen i **[!UICONTROL Current]**.

1. Välj **[!UICONTROL Apply]** om du vill tillämpa ändringarna. Välj **[!UICONTROL Cancel]** om du vill avbryta eventuella ändringar i visualiseringen.
