---
title: Skapa planer
description: Lär dig hur du bygger planer i Mix Modeler.
feature: Plans
exl-id: 6d61d0b2-5871-4d00-9a35-73fff0a1c3e5
source-git-commit: 1d017960409e5433ac6b4950a5cf7a5b3174840a
workflow-type: tm+mt
source-wordcount: '708'
ht-degree: 0%

---


# Skapa planer

I Mix Modeler skapar du en plan med hjälp av planarbetsytan. På planarbetsytan kan du ange information och budgetar för din plan och den underliggande modellen som ska användas för din plan. När du har angett detaljer, budget och modell kan du gå vidare med en AI-rekommenderad plan eller redigera utgiften per kanal.

Om du vill skapa en plan väljer du **[!UICONTROL Create plan]** i ![PLan](/help/assets/icons/FileChart.svg) **[!UICONTROL Plans]** -gränssnittet i Mix Modeler.


1. På skärmen **[!UICONTROL Plan creation]**:

   1. I avsnittet **[!UICONTROL Setup]**:

      1. Ange en **[!UICONTROL Plan name]**, till exempel `Demo plan`. Ange en **[!UICONTROL Description]**, till exempel `Demo plan for Luma company`.
      1. Välj ett **[!UICONTROL Model]** från **[!UICONTROL _Välj ett alternativ._.]**
      1. Du kan välja ![LinkOut](/help/assets/icons/LinkOut.svg) **[!UICONTROL Create model]** om du vill skapa en modell direkt från planskapandet. Då öppnas en ny flik i webbläsaren och gränssnittet [Models](../models/overview.md) visas.

         ![Planinställningar](/help/assets/plan-setup.png)

   1. I avsnittet **[!UICONTROL Budget]**:

      1. Ange ett datumintervall, antingen genom att skriva datum eller genom att välja ett datumintervall med ![Kalender](/help/assets/icons/Calendar.svg).
      1. Ange en budget.

      Om du vill lägga till ytterligare datumintervall, var och en med sin budget, väljer du ![CalendarAdd](/help/assets/icons/CalendarAdd.svg) **[!UICONTROL Add row]**.

      Om du vill ta bort ett datumintervall och en associerad budget väljer du ![Stäng](/help/assets/icons/Close.svg).

      Så här definierar du en angiven maxbudget:

      1. Aktivera **[!UICONTROL Maximize budget]**.
      1. Ange det maximala budgetbeloppet. Beloppet ska vara lika med eller högre än det totala budgetbeloppet som angetts för datumintervallen.

         ![Planera budget](/help/assets/plan-budget.png)

   1. Välj **[!UICONTROL Next]**.

1. I dialogrutan **[!UICONTROL Done with all required fields]**:

   ![Planen är klar](/help/assets/plan-done-required-fields.png)

   * Välj ![NewPlan](/help/assets/icons/NewPlan.svg) **[!UICONTROL Create plan now]** om du vill generera en AI-rekommenderad plan med prognostiserad avkastning.


     Välj **[!UICONTROL OK]**. Din plan har skapats.


   * Välj ![TableEdit](/help/assets/icons/TableEdit.svg) **[!UICONTROL Edit channel budgets first]** om du vill redigera kanalbudgeten och definiera avancerade konfigurationer innan en plan med prognostiserad avkastning skapas.

     Välj **[!UICONTROL OK]** så att du kan definiera din kanalutgift i **[!UICONTROL Spend selection]** i nästa steg.



1. I avsnittet **[!UICONTROL Spend selection]** använder du ![Chevron](/help/assets/icons/ChevronRight.svg) för att öppna kanaldistributionsvyn för det dataintervallet för varje datumintervall.

   Ni kan använda historiska referensdata om ni vill använda tidigare marknadsföringsutgiftsdata och insikter. Du bör överväga historiska referensdata för att:

   * Förbättra budgettilldelningen genom att markera högpresterande kanaler och dåligt fungerande kanaler.
   * stödja trendanalys.
   * Identifiera effektiva strategier och undvik misstag när du konfigurerar planer.

   Om du väljer en historisk referensperiod kan du anpassa dig till tidigare inställningar för utgiftsmönster och Mix Modeler planeringsfunktion generera planer som ligger inom dina förväntningar. Dessa planer bör i slutändan öka intressenternas förtroende, säkerställa att marknadsföringsplanerna är strategiska, effektiva och att dessa planer bygger på beprövade resultatdata och affärsbehov.

   ![Utgiftsmarkering](/help/assets/plan-spend-selection.png)

   1. Välj **[!UICONTROL Spend pattern]**.

      * Som standard är detta **[!UICONTROL Automatic]**.
      * Välj **[!UICONTROL Historical reference]** och ange en **[!UICONTROL Start date]** för att referera till tidigare marknadsföringsutgiftsdata som redan är tillgängliga för Mix Modeler. **[!UICONTROL End date]** bestäms automatiskt utifrån det dataområde som du definierar utgiftsmönstret för. Det föreslagna startdatumet är den första tillgängliga informationen om tidigare marknadsföringsutgifter som finns tillgänglig. Om du vill ange att du har valt en icke-befintlig eller ogiltig historik referensperiod visas en ![AlertRed](/help/assets/icons/AlertRed.svg).

   1. Om du vill definiera budgetar för varje kanal anger du ett värde för **[!UICONTROL Min]** och **[!UICONTROL Max]** eller använder reglagen.

   1. Om du vill växla mellan valuta- eller procentindata väljer du **[!UICONTROL $]** eller **[!UICONTROL %]** för **[!UICONTROL View spend by]**.

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

      1. Definiera anpassade kanalkostnader för varje kanal i modellen.

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

