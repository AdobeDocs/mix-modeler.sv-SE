---
title: Skapa planer
description: Lär dig hur du bygger planer i Mix Modeler.
feature: Plans
exl-id: 6d61d0b2-5871-4d00-9a35-73fff0a1c3e5
source-git-commit: 498f50e4d1568e58d0ac2833022822340a5f6337
workflow-type: tm+mt
source-wordcount: '948'
ht-degree: 0%

---


# Skapa planer

I Mix Modeler skapar du en plan med hjälp av planguiden. I planguiden kan du ställa in detaljer, budgetar eller målvärden för din plan och den underliggande modellen som ska användas för din plan. När du har angett detaljer, budget, målvärden och modell kan du gå vidare med en AI-rekommenderad plan eller redigera utgiften per kanal. Du kan definiera avancerade konfigurationer för genomsnittliga intäkter per konvertering och kanalkostnader.

Du måste definiera det mål som du vill maximera din plan mot. Detta mål kan antingen vara en budget som du kan spendera eller ett mål som du vill uppnå. Om målet är ett mål måste du dessutom ange värden för målmåttet som ska användas: konvertering, intäkter, CPA eller avkastning.

Om du vill skapa en plan väljer du **[!UICONTROL Create plan]** i ![PLan](/help/assets/icons/FileChart.svg) **[!UICONTROL Plans]** -gränssnittet i Mix Modeler.


1. På skärmen **[!UICONTROL Plan creation]**:

   1. I avsnittet **[!UICONTROL Setup]**:

      1. Ange en **[!UICONTROL Plan name]**, till exempel `Goal based plan`. Ange en **[!UICONTROL Description]**, till exempel `A goal based plan`.
      1. Välj ett **[!UICONTROL Model]** från **[!UICONTROL _Välj ett alternativ._.]**

         ![Planinställningar](/help/assets/plan-setup.png)

   1. I avsnittet **[!UICONTROL Goal]** väljer du det mål som du vill optimera din plan mot. Du kan välja mellan

      * **[!UICONTROL I have a budget to spend]**

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


      * **[!UICONTROL I have a target to achieve]** [!BADGE Beta]

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


   1. Välj **[!UICONTROL Next]**.

1. I dialogrutan **[!UICONTROL Done with all required fields]**:

   ![Planen är klar](/help/assets/plan-done-required-fields.png)

   * Välj ![NewPlan](/help/assets/icons/NewPlan.svg) **[!UICONTROL Create plan now]** om du vill generera en AI-rekommenderad plan med prognostiserad avkastning. Välj **[!UICONTROL OK]**. Din plan har skapats.





   * Välj ![TableEdit](/help/assets/icons/TableEdit.svg) **[!UICONTROL Edit channel budgets first]** om du vill redigera kanalbudgeten och definiera avancerade konfigurationer innan en plan med prognostiserad avkastning skapas.  Välj **[!UICONTROL OK]** så att du kan definiera din kanalutgift i **[!UICONTROL Spend selection]** i nästa steg.


     >[!IMPORTANT]
     >
     >Informationen nedan är bara relevant om du har valt ![TableEdit](/help/assets/icons/TableEdit.svg) **[!UICONTROL Edit channel budgets first]**


1. I avsnittet **[!UICONTROL Spend selection]** använder du ![Chevron](/help/assets/icons/ChevronRight.svg) för att öppna kanaldistributionsvyn för det dataintervallet för varje datumintervall.

   Ni kan använda historiska referensdata om ni vill använda tidigare marknadsföringsutgiftsdata och insikter. Ta hänsyn till historiska referensdata för:

   * Förbättra budgettilldelningen genom att markera högpresterande kanaler och dåligt fungerande kanaler.
   * stödja trendanalys.
   * Identifiera effektiva strategier och undvik misstag när du konfigurerar planer.

   Om du väljer en historisk referensperiod kan du anpassa dig till tidigare inställningar för utgiftsmönster och Mix Modeler planeringsfunktion generera planer som ligger inom dina förväntningar. Dessa planer bör i slutändan öka intressenternas förtroende, säkerställa att marknadsföringsplanerna är strategiska, effektiva och att dessa planer bygger på beprövade resultatdata och affärsbehov.

   ![Utgiftsmarkering](/help/assets/plan-spend-selection.png)

   1. Välj **[!UICONTROL Spend pattern]**.

      * Standardalternativet är **[!UICONTROL Automatic]**.
      * Välj **[!UICONTROL Historical reference]** och ange en **[!UICONTROL Start date]** för att referera till tidigare marknadsföringsutgiftsdata som redan är tillgängliga för Mix Modeler. **[!UICONTROL End date]** bestäms automatiskt utifrån det datumintervall för vilket du definierar utgiftsmönstret. Det föreslagna startdatumet är det första tillgängliga datumet för tidigare marknadsföringsutgifter som finns. Om du vill ange att du har valt en icke-befintlig eller ogiltig historik referensperiod visas en ![AlertRed](/help/assets/icons/AlertRed.svg).

   1. Om du vill definiera budgetar för varje kanal anger du ett värde för **[!UICONTROL Min]** och **[!UICONTROL Max]** eller använder reglagen.

   1. Om du vill växla mellan valuta- eller procentindata väljer du **[!UICONTROL $]** eller **[!UICONTROL %]** för **[!UICONTROL View spend by]**. Den här växlingen är inaktiverad om du har valt målmått som inte är valutabaserade.

   1. När du är klar väljer du **[!UICONTROL Create]**.
      ![Utgiftsmarkering](/help/assets/plan-spend-selection.png)

   1. Välj **[!UICONTROL Next]**.



1. I avsnittet **[!UICONTROL Advanced configurations]** kan du ange valfria avancerade konfigurationer.

   ![Sammanfattning av plan](../assets/plan-advanced-configurations.png)

   * Ditt plannamn, din modell, datumintervall och din totala budget sammanfattas.

   * Som standard beräknar Mix Modeler automatiskt den genomsnittliga intäkten per konvertering med hjälp av de senaste historiska säsongsuppgifterna. I **[!UICONTROL Average Revenue per conversion]** kan du definiera en specifik genomsnittlig intäkt per konvertering.

      1. För varje datumintervall i din budget:

         1. Välj ett datumintervall i listrutan **[!UICONTROL Date range]**.
         1. Ange ett **[!UICONTROL Average revenue]**-värde.

      1. Välj ![AddCircle](/help/assets/icons/AddCircle.svg) Lägg till en anpassad genomsnittlig intäkt per konverteringsenhet för att lägga till ett datumintervall.
      1. Välj ![RemoveCircle](/help/assets/icons/RemoveCircle.svg) om du vill ta bort ett datumintervall.

     >[!NOTE]
     >
     >Om modellen inte innehåller historiska intäktsdata måste du definiera en genomsnittlig intäkt per konvertering för varje datumintervall som du anger för din budget.
     >

   * Som standard beräknar Mix Modeler automatiskt kanalkostnaderna med hjälp av de senaste säsongsuppgifterna. I **[!UICONTROL Channel costs]** kan du definiera anpassade kanalkostnader.

      1. Definiera en anpassad kanalkostnad för varje kanal i modellen.

         1. Välj en kanal i listrutan **[!UICONTROL Channel]**.
         1. För varje datumintervall i din budget:
            1. Välj ett datumintervall i listrutan **[!UICONTROL Date range]**.
            1. Ange ett **[!UICONTROL Average revenue]**-värde.
         1. Välj ![AddCircle](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add custom average revenue per conversion unit]** om du vill lägga till ett datumintervall.
         1. Välj ![RemoveCircle](/help/assets/icons/RemoveCircle.svg) om du vill ta bort ett datumintervall.

      1. Välj ![AddCircle](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add custom channel cost]** om du vill lägga till en kanal.
      1. Välj ![CrossSize400](/help/assets/icons/CrossSize400.svg) om du vill ta bort en anpassad kanal.


1. När du är klar väljer du **[!UICONTROL Create]**.

1. I dialogrutan **[!UICONTROL Create plan]** väljer du **[!UICONTROL Create plan]** för att skapa din plan. Välj **[!UICONTROL Cancel]** om du vill avbryta skapandet av din plan. En **[!UICONTROL No work is saved]**-dialogruta visas för att bekräfta.

