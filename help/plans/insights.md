---
title: Planera insikter
description: Lär dig hur du ser insikter om din plan och redigerar en plan i Mix Modeler.
feature: Plans
exl-id: 91385595-284f-4fcb-b54b-9539905e552b
source-git-commit: f0871834ec665c907caf0af3edeeed4fb2549a58
workflow-type: tm+mt
source-wordcount: '1134'
ht-degree: 0%

---

# Planera insikter


I [!UICONTROL Plan insights] skapas dina planinsikter och visar [!UICONTROL Model], [!UICONTROL Data range] och [!UICONTROL Plan target] som planen baseras på.


När insikterna skapas visas en översikt över din plan, som består av:

- En rubrik som visar [!UICONTROL Model], [!UICONTROL Data range] och [!UICONTROL Plan target] som planen baseras på.
   - Om du har definierat en målbaserad plan visas ett märke som anger statusen för ditt mål Möjliga alternativ är:

      - [!BADGE Mål som kan uppnås]{type=Positive}
      - [!BADGE Målet kan inte nås]{type=Negative}

   - Välj ![SparronDown](/help/assets/icons/ChevronDown.svg) **[!UICONTROL Show more]** om du vill visa mer information.

- [[!UICONTROL Forecasted paid channel ROI]-visualisering](#forecasted-paid-channel-spend-and-roi)
- [[!UICONTROL Forecasted revenue]-visualisering](#forecasted-revenue)
- [[!UICONTROL Forecasted conversion]-visualisering](#forecasted-conversions)
- [[!UICONTROL Marginal channel return]-visualisering](#marginal-channel-return)
- tabellen [[!UICONTROL Data range breakdown] i planen ](#date-range-breakdown), med kolumner för

   - Kanal
   - avkastning
   - CPA
   - Intäkter
   - Konverteringsmål
   - Utgift

Om du vill stänga gränssnittet väljer du **[!UICONTROL Close]**.

Om du vill ändra hur du visar avkastningen på din plan väljer du **[!UICONTROL X]** eller **[!UICONTROL &#x200B; %]** **[!UICONTROL View ROI]**.

## Prognostiserade utgifter för betalda kanaler och avkastning på investerat kapital

Den här visualiseringen visar en utspridd yta för de prognostiserade investeringarna och avkastningen på investeringar i dina betalda kanaler, baserat på modell, datumintervall och budget.

![Prognostiserad visualisering av utgifter för betalda kanaler och avkastning ](../assets/overview-plan-forecasted-paid-channel-send-roi.png)


## Prognostiserade intäkter

I den här stapeldiagramvisningen visas de beräknade intäkterna för kanalerna baserat på modell, datumintervall och budget.

![Prognostiserad intäktsvisualisering](../assets/overview-plan-forecasted-revenue.png)


## Prognostiserade konverteringar

I den här stapeldiagramvisningen visas de prognostiserade konverteringarna för kanalerna baserat på modell, datumintervall och budget.

![Prognostiserad konverteringsvisualisering](../assets/overview-plan-forecasted-conversions.png)


## Marginalkanalsretur

Den här linjediagramvisningen visar en marginell returkurva för den valda kanalen med indikatorer för **[!UICONTROL Marginal break-even]** och **[!UICONTROL Return point]**. Den här visualiseringen hjälper er att förstå hur en kanals utgifter går från att nå en marginell nollpunkt. Och oavsett om ni har utrymme att öka utgifterna i en kanal eller ska lägga mindre på en kanal för att förbättra effektiviteten i kanalinvesteringen.

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

Om du vill redigera din plan väljer du ![Redigera](/help/assets/icons/Edit.svg) **[!UICONTROL Edit plan]**.

1. I avsnittet **[!UICONTROL Spend selection]** använder du ![Chevron](/help/assets/icons/ChevronRight.svg) för att öppna kanaldistributionsvyn för det dataintervallet för varje datumintervall.

   Ni kan använda historiska referensdata om ni vill använda tidigare marknadsföringsutgiftsdata och insikter. Ta hänsyn till historiska referensdata för:

   - Förbättra budgettilldelningen genom att markera högpresterande kanaler och dåligt fungerande kanaler.
   - stödja trendanalys.
   - Identifiera effektiva strategier och undvik misstag när du konfigurerar planer.

   Om du väljer en historisk referensperiod kan du anpassa dig till tidigare inställningar för utgiftsmönster och Mix Modeler planeringsfunktion generera planer som ligger inom dina förväntningar. Dessa planer bör i slutändan öka intressenternas förtroende, säkerställa att marknadsföringsplanerna är strategiska, effektiva och att dessa planer bygger på beprövade resultatdata och affärsbehov.

   ![Utgiftsmarkering](/help/assets/plan-spend-selection.png)

   1. Välj **[!UICONTROL Spend pattern]**.

      - Standardalternativet är **[!UICONTROL Automatic]**.
      - Välj **[!UICONTROL Historical reference]** och ange en **[!UICONTROL Start date]** för att referera till tidigare marknadsföringsutgiftsdata som redan är tillgängliga för Mix Modeler. **[!UICONTROL End date]** bestäms automatiskt utifrån det valda dataområdet. Det föreslagna startdatumet är den första tillgängliga informationen om tidigare marknadsföringsutgifter som finns tillgänglig. Om du vill ange att du har valt en historik som inte finns visas en ![AlertRed](/help/assets/icons/AlertRed.svg).


   1. Om du vill ändra budgeten för varje kanal ändrar du värdena för **[!UICONTROL Min]** och **[!UICONTROL Max]** eller använder reglagen.

   1. Om du vill växla mellan valuta- eller procentindata väljer du **[!UICONTROL $]** eller **[!UICONTROL %]** för **[!UICONTROL View spend by]**.

   1. Om du vill redigera information om din plan väljer du **[!UICONTROL Edit details]**:

      1. I avsnittet **[!UICONTROL Setup]**:

         1. Ange en **[!UICONTROL Plan name]**, till exempel `Demo plan`. Ange en **[!UICONTROL Description]**, till exempel `Demo plan for Luma company`.
         1. Välj ett **[!UICONTROL Model]** från **[!UICONTROL _Välj ett alternativ._.]**

            ![Planinställningar](/help/assets/plan-setup.png)

      1. I avsnittet **[!UICONTROL Goal]** väljer du det mål som du vill optimera din plan mot. Du kan välja mellan
         - **[!UICONTROL I have a budget to spend]**

           ![Planera budget](../assets/plan-budget.png)

           Med det här alternativet kan du ange budgetar för ett eller flera datumintervall.

            1. I behållaren **[!UICONTROL Optimize]**:
               1. Välj en konvertering i listrutan **[!UICONTROL Select conversion]**.
               1. Välj en modell i listrutan **[!UICONTROL Select model]**.
            1. Ange en **[!UICONTROL Date range]**, antingen genom att skriva datum eller välja ett datumintervall med ![Kalender](/help/assets/icons/Calendar.svg).
            1. Ange **[!UICONTROL Budget]**.
Om du vill lägga till ytterligare datumintervall, var och en med sin budget, väljer du ![CalendarAdd](/help/assets/icons/CalendarAdd.svg) **[!UICONTROL Add row]**.
Om du vill ta bort ett datumintervall och en associerad budget väljer du ![Stäng](/help/assets/icons/Close.svg).
            1. Så här definierar du en valfri maxbudget som du vill begränsa planen inom:
               1. Aktivera **[!UICONTROL Maximize budget]**.
               1. Ange beloppet för den maximala budgeten. Beloppet ska vara lika med eller högre än det totala beloppet för budgetarna som anges för datumintervallen.


         - **[!UICONTROL I have a target to achieve]** [!BADGE Beta]

           ![Planera mål](../assets/plan-target.png)

            1. I behållaren **[!UICONTROL Optimize]**
               1. Välj en konvertering i listrutan **[!UICONTROL Select conversion]**.
               1. Välj ett målmått i listrutan **[!UICONTROL Select target metric]**. Du kan välja mellan **[!UICONTROL Conversion]**, **[!UICONTROL CPA]**, **[!UICONTROL Revenue]** eller **[!UICONTROL ROI]**.
               1. Välj en modell i listrutan **[!UICONTROL Select model]**.
            1. Ange ett datumintervall, antingen genom att skriva datum eller genom att välja ett datumintervall med ![Kalender](/help/assets/icons/Calendar.svg).
            1. Ange ett värde för det valda målmåttet. Ett tal för **[!UICONTROL Conversion]**, ett procenttal för **[!UICONTROL ROI]** eller valutavärden för **[!UICONTROL CPA]** och **[!UICONTROL Revenue]**.
Om du vill lägga till ytterligare datumintervall väljer du ![CalendarAdd](/help/assets/icons/CalendarAdd.svg) **[!UICONTROL Add row]** för var och en med sina målmått.
Om du vill ta bort ett datumintervall och tillhörande målmått väljer du ![Stäng](/help/assets/icons/Close.svg).
            1. Så här definierar du en valfri maxbudget som du vill begränsa planen inom:
               1. Aktivera **[!UICONTROL Maximize budget]**.
               1. Ange beloppet för den maximala budgeten.

         1. Välj **[!UICONTROL Next]** om du vill återgå till avsnittet **[!UICONTROL Spend selection]**.

1. I avsnittet **[!UICONTROL Advanced configuration]**:

   ![Redigera avancerad konfiguration](../assets/edit-plan-advanced-configuration.png)

   - Ditt plannamn, din modell, datumintervall och din totala budget sammanfattas.

   - Som standard beräknar Mix Modeler automatiskt den genomsnittliga intäkten per konvertering med hjälp av de senaste historiska säsongsuppgifterna. I **[!UICONTROL Average Revenue per conversion]** kan du definiera en specifik genomsnittlig intäkt per konvertering.

   1. För varje datumintervall i din budget:
      1. Välj ett datumintervall i listrutan **[!UICONTROL Date range]**.
      1. Ange ett **[!UICONTROL Average revenue]**-värde.
   1. Välj ![AddCircle](/help/assets/icons/AddCircle.svg) Lägg till en anpassad genomsnittlig intäkt per konverteringsenhet för att lägga till ett datumintervall.
   1. Välj ![RemoveCircle](/help/assets/icons/RemoveCircle.svg) om du vill ta bort ett datumintervall.

   >[!NOTE]
   >
   >Om modellen inte innehåller historiska intäktsdata måste du definiera en genomsnittlig intäkt per konvertering för varje datumintervall som du anger för din budget.
   >

   - Som standard beräknar Mix Modeler automatiskt kanalkostnaderna med hjälp av de senaste säsongsuppgifterna. I **[!UICONTROL Channel costs]** kan du definiera anpassade kanalkostnader.

   1. Definiera anpassade kanalkostnader för varje kanal i modellen.
      1. Välj en kanal i listrutan **[!UICONTROL Channel]**.
      1. För varje datumintervall i din budget:
         1. Välj ett datumintervall i listrutan **[!UICONTROL Date range]**.
         1. Ange ett **[!UICONTROL Average revenue]**-värde.
      1. Välj ![AddCircle](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add custom average revenue per conversion unit]** om du vill lägga till ett datumintervall.
      1. Välj ![RemoveCircle](/help/assets/icons/RemoveCircle.svg) om du vill ta bort ett datumintervall.

   1. Välj ![AddCircle](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add custom channel cost]** om du vill lägga till en kanal.
   1. Välj ![CrossSize400](/help/assets/icons/CrossSize400.svg) om du vill ta bort en anpassad kanal.


1. När du är klar med redigeringen av din plan väljer du **[!UICONTROL Edit]**.

   I dialogrutan **[!UICONTROL All changes are final]** väljer du **[!UICONTROL OK]** för att uppdatera planens aktuella utgiftsallokering och prognoser för avkastning och intäkter. Välj **[!UICONTROL Cancel]** om du vill avbryta uppdateringen av din plan.


- Om du vill avbryta dina avtalsuppdateringar väljer du **[!UICONTROL Cancel]**. I dialogrutan **[!UICONTROL No work will be saved]** väljer du **[!UICONTROL Cancel]** för att fortsätta arbeta med din plan eller **[!UICONTROL OK]** för att återgå till gränssnittet för planer.
- Om du vill gå tillbaka i guiden väljer du **[!UICONTROL Back]**.
