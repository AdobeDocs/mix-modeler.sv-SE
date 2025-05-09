---
title: Planera insikter
description: Lär dig hur du ser insikter om din plan och redigerar en plan i Mix Modeler.
feature: Plans
exl-id: 91385595-284f-4fcb-b54b-9539905e552b
source-git-commit: fbed53a1c394d6d110db6a8a181ca815056377de
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 0%

---

# Planera insikter


I [!UICONTROL Plan insights] skapas dina planinsikter och visar [!UICONTROL Model], [!UICONTROL Data range] och [!UICONTROL Total budget] som planen baseras på.

När hämtningen är klar visas en översikt över din plan, som består av:

- [!UICONTROL Forecasted paid channel ROI]-visualisering
- [!UICONTROL Forecasted revenue]-visualisering
- [!UICONTROL Forecasted conversion]-visualisering
- [!UICONTROL Marginal channel return]-visualisering
- tabellen [!UICONTROL Data range breakdown] i planen, med kolumner för

   - Kanal
   - avkastning
   - CPA
   - Intäkter
   - Konverteringsmål
   - Utgift

Om du vill stänga gränssnittet väljer du **[!UICONTROL Close]**.

Om du vill ändra hur du visar avkastningen på din plan väljer du **[!UICONTROL X]** eller **[!UICONTROL &#x200B; %]** **[!UICONTROL View ROI]**.

## Prognostiserade utgifter för betalda kanaler och avkastning på investerat kapital

Den här visualiseringen visar en utspridd yta för de förutsagda utgifterna och avkastningen på investeringar i dina betalda kanaler, baserat på modell, datumintervall och budget.

![Prognostiserad visualisering av utgifter för betalda kanaler och avkastning ](../assets/overview-plan-forecasted-paid-channel-send-roi.png)


## Prognostiserade intäkter

I den här stapeldiagramvisningen visas de beräknade intäkterna för kanalerna baserat på modell, datumintervall och budget.

![Prognostiserad intäktsvisualisering](../assets/overview-plan-forecasted-revenue.png)


## Prognostiserade konverteringar

I den här stapeldiagramvisningen visas de prognostiserade konverteringarna för kanalerna baserat på modell, datumintervall och budget.

![Prognostiserad konverteringsvisualisering](../assets/overview-plan-forecasted-conversions.png)


## Marginalkanalsretur

Den här linjediagramvisningen visar en marginell returkurva för den valda kanalen med indikatorer för **[!UICONTROL Marginal break-even]** och **[!UICONTROL Return point]**. Den här visualiseringen hjälper er att förstå hur en kanals utgifter sträcker sig från att nå en marginell nollpunkt och om ni har utrymme att öka utgifterna i en kanal eller borde spendera mindre på en kanal för att förbättra kanalens utläggseffektivitet.

![Återkommande visualisering av marginella kanaler](../assets/overview-plan-marginal-channel-return.png)

Om du vill välja en viss kanal för visualiseringen väljer du en kanal i listrutan **[!UICONTROL View]**.


## Uppdelning av datumintervall

Tabellen [!UICONTROL Date range breakdown] visar detaljerade, detaljerade data per kanal för [!UICONTROL ROI], [!UICONTROL Revenue], [!UICONTROL CPA], [!UICONTROL Conversions] och [!UICONTROL Spend].

![Indelningstabell för datumintervall](../assets/overview-plan-date-range-breakdown.png)

1. Välj ![Hämta](/help/assets/icons/Download.svg) **[!UICONTROL Download CSV]** om du vill hämta en CSV-fil som innehåller data för datumintervallet. På snabbmenyn:

   - Välj ![Hämta](/help/assets/icons/Download.svg) **[!UICONTROL Detailed CSV]** om du vill ha detaljerade data i CSV-format.
   - Välj ![Hämta](/help/assets/icons/Download.svg) **[!UICONTROL Summary CSV]** om du vill visa sammanfattningsdata i CSV-format.

   Detaljerade data är data insamlade per vecka. Sammanfattningsdata är data som lagras i det modellgivna datumintervallet.

1. Välj **[!UICONTROL All channels]**, **[!UICONTROL Paid channels]** eller **[!UICONTROL Non-paid channels]** från markeringen **[!UICONTROL View]** om du vill visa datumintervallfördelningen per kanalkategori.


## Redigera plan

1. Om du vill redigera din plan väljer du ![Redigera](/help/assets/icons/Edit.svg) **[!UICONTROL Edit plan]**:

   1. I avsnittet **[!UICONTROL Spend selection]** använder du ![Chevron](/help/assets/icons/ChevronRight.svg) för att öppna kanaldistributionsvyn för det dataintervallet för varje datumintervall.

   1. Om du vill ändra budgeten för varje kanal ändrar du värdena för **[!UICONTROL Min]** och **[!UICONTROL Max]** eller använder reglagen.

   1. Om du vill växla mellan valuta- eller procentindata väljer du **[!UICONTROL $]** eller **[!UICONTROL %]** för **[!UICONTROL View spend by]**.

      ![Utgiftsmarkering](/help/assets/spend-selection.png)

   1. Om du vill redigera information om din plan väljer du **[!UICONTROL Edit details]**:

      1. I avsnittet **[!UICONTROL Setup]** ändrar du **[!UICONTROL Plan name]** och **[!UICONTROL Description]**, om tillämpligt.

      1. I avsnittet **[!UICONTROL Budget]**:

         1. Ändra **[!UICONTROL Date range]** för ett eller flera av din plans datumintervall, antingen genom att ange datum eller välja ett datumintervall med ![Kalender](/help/assets/icons/Calendar.svg).

         1. Ändra **[!UICONTROL Budget]** för ett eller flera av din plans datumintervall.

         Om du vill lägga till ytterligare datumintervall, var och en med sin budget, väljer du ![CalendarAdd](/help/assets/icons/CalendarAdd.svg) **[!UICONTROL Add row]**.

         Om du vill ta bort ett datumintervall och en associerad budget väljer du ![Stäng](/help/assets/icons/Close.svg).

         Så här definierar du en maximal budget:

         1. Aktivera **[!UICONTROL Maximize budget]**.
         1. Ange det maximala budgetbeloppet. Beloppet ska vara lika med eller högre än det totala budgetbeloppet som angetts för datumintervallen.

      1. Välj **[!UICONTROL Next]** om du vill återgå till avsnittet **[!UICONTROL Spend]**. Välj **[!UICONTROL Cancel]** om du vill återgå till din planöversikt.

         ![Avtalsinformation](/help/assets/plan-details.png)


1. När du är klar med redigeringen av din plan väljer du **[!UICONTROL Edit]**.

   I dialogrutan **[!UICONTROL All changes are final]** väljer du **[!UICONTROL OK]** för att uppdatera planens aktuella utgiftsallokering och prognoser för avkastning och intäkter. Välj **[!UICONTROL Cancel]** om du vill avbryta uppdateringen av din plan.

1. Om du vill avbryta dina avtalsuppdateringar väljer du **[!UICONTROL Cancel]**.

   I dialogrutan **[!UICONTROL No work will be saved]** väljer du **[!UICONTROL Cancel]** för att fortsätta arbeta med din plan eller **[!UICONTROL OK]** för att återgå till gränssnittet för planer.
