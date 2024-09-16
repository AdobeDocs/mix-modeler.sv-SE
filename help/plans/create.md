---
title: Skapa en plan
description: Lär dig hur du skapar en plan i Mix Modeler.
feature: Plans
exl-id: 6d61d0b2-5871-4d00-9a35-73fff0a1c3e5
source-git-commit: 9a6c1f1c12ab29da80a1997cfd31ca07b38eaa22
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 0%

---


# Skapa en plan

I Mix Modeler skapar du en plan med hjälp av planarbetsytan. På planarbetsytan kan du ange information och budgetar för din plan och den underliggande modellen som ska användas för din plan. När du har angett detaljer, budget och modell kan du gå vidare med en AI-rekommenderad plan eller redigera utgiften per kanal.

Om du vill skapa en plan väljer du **[!UICONTROL Open plan canvas]** i gränssnittet ![PLan](/help/assets/icons/FileChart.svg) **[!UICONTROL Plans]** i Mix Modeler.

1. Skärmen för att skapa plan:

   1. I avsnittet **[!UICONTROL Setup]**

      1. Ange en **[!UICONTROL Plan name]**, till exempel `Demo plan`. Ange en **[!UICONTROL Description]**, till exempel `Demo plan for Luma company`.
      1. Välj ett **[!UICONTROL Model]** från **[!UICONTROL _Välj ett alternativ._.]**.
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

   * Välj <img src="/help/assets/icons/NewPlan.svg" width="25" /> **[!UICONTROL Create plan now]** om du vill generera en AI-rekommenderad plan med prognostiserad avkastning på investerat kapital.

     Välj **[!UICONTROL OK]**. Din plan har skapats.


   * Välj ![TableEdit](/help/assets/icons/TableEdit.svg) **[!UICONTROL Edit channel budgets first]** om du vill redigera kanalbudgeten innan du skapar en plan med prognostiserad avkastning.

     Välj **[!UICONTROL OK]** så att du kan definiera din kanalutgift i **[!UICONTROL Spend selection]** i nästa steg.



1. I avsnittet **[!UICONTROL Spend selection]** använder du ![Chevron](/help/assets/icons/ChevronRight.svg) överst för att öppna kanaldistributionsvyn för det dataintervallet för varje datumintervall.

   1. Om du vill definiera budgetar för varje kanal anger du ett värde för **[!UICONTROL Min]** och **[!UICONTROL Max]** eller använder reglagen.

   1. Om du vill växla mellan valuta- eller procentindata väljer du **[!UICONTROL $]** eller **[!UICONTROL %]** för **[!UICONTROL View spend by]**.

      ![Utgiftsmarkering](/help/assets/plan-spend-selection.png)

   1. När du är klar väljer du **[!UICONTROL Create]**.

   1. I dialogrutan **[!UICONTROL Create plan]** väljer du **[!UICONTROL Create plan]** för att skapa din plan. Välj **[!UICONTROL Cancel]** om du vill avbryta skapandet av din plan. En **[!UICONTROL No work is saved]**-dialogruta visas för att bekräfta.
