---
title: Skapa en plan
description: Lär dig hur du skapar en plan i Mix Modeler.
feature: Plans
exl-id: 6d61d0b2-5871-4d00-9a35-73fff0a1c3e5
source-git-commit: 86732fe30637aa72ced232d9f331a3cc64baa39b
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 0%

---


# Skapa en plan

I Mix Modeler skapar du en plan med hjälp av planarbetsytan. På planarbetsytan kan du ange information och budgetar för din plan och den underliggande modellen som ska användas för din plan. När du har angett detaljer, budget och modell kan du gå vidare med en AI-rekommenderad plan eller redigera utgiften per kanal.

Skapa en plan i ![PLan](../assets/icons/FileChart.svg) **[!UICONTROL Plans]** i Mix Modeler väljer **[!UICONTROL Open plan canvas]**.

1. Skärmen för att skapa plan:

   1. I **[!UICONTROL Setup]** section

      1. Ange en **[!UICONTROL Plan name]**, till exempel `Demo plan`. Ange en **[!UICONTROL Description]**, till exempel `Demo plan for Luma company`.
      1. Välj en **[!UICONTROL Model]** från **[!UICONTROL _Välj ett alternativ.._.]**.
      1. Du kan välja ![LinkOut](../assets/icons/LinkOut.svg) **[!UICONTROL Create model]** för att skapa en modell direkt från när du skapar en plan. Då öppnas en ny flik i webbläsaren och [Models](../models/overview.md) gränssnitt.

         ![Planinställningar](../assets/plan-setup.png)

   1. I **[!UICONTROL Budget]** avsnitt:

      1. Ange ett datumintervall, antingen genom att skriva datum eller genom att välja ett datumintervall med ![Kalender](../assets/icons/Calendar.svg).
      1. Ange en budget.

      Om du vill lägga till ytterligare datumintervall väljer du ![KalenderLägg till](../assets/icons/CalendarAdd.svg) **[!UICONTROL Add row]**.

      Om du vill ta bort ett datumintervall och en associerad budget väljer du ![Stäng](../assets/icons/Close.svg).

      Så här definierar du en angiven maxbudget:

      1. Byt **[!UICONTROL Maximize budget]** på.
      1. Ange det maximala budgetbeloppet. Beloppet ska vara lika med eller högre än det totala budgetbeloppet som angetts för datumintervallen.

         ![Planbudget](../assets/plan-budget.png)

   1. Välj **[!UICONTROL Next]**.

1. I **[!UICONTROL Done with all required fields]** dialog:

   ![Planen är klar](../assets/plan-done-required-fields.png)

   * Välj <img src="../assets/icons/NewPlan.svg" width="25" /> **[!UICONTROL Create plan now]** om du vill generera en AI-rekommenderad plan med prognostiserad avkastning på investerat kapital.

     Välj **[!UICONTROL OK]**. Din plan har skapats.


   * Välj ![TabellRedigera](../assets/icons/TableEdit.svg) **[!UICONTROL Edit channel budgets first]** om du vill redigera kanalbudgeten innan du skapar en plan med prognostiserad avkastning på investeringen.

     Välj **[!UICONTROL OK]** så att ni kan definiera era kanalutgifter i **[!UICONTROL Spend selection]** i nästa steg.



1. I **[!UICONTROL Spend selection]** för varje datumintervall i budgeten använder du ![Chevron](../assets/icons/ChevronRight.svg) I det övre fönstret öppnas kanaldistributionsvyn för det dataintervallet.

   1. Ange ett värde för **[!UICONTROL Min]** och **[!UICONTROL Max]** eller använda skjutreglagen.

   1. Om du vill växla mellan valuta- eller procentindata väljer du **[!UICONTROL $]** eller **[!UICONTROL %]** for **[!UICONTROL View spend by]**.

      ![Utgiftsval](../assets/plan-spend-selection.png)

   1. När du är klar väljer du **[!UICONTROL Create]**.

   1. I **[!UICONTROL Create plan]** dialogruta, välja **[!UICONTROL Create plan]** för att skapa en plan. Välj **[!UICONTROL Cancel]** för att avbryta skapandet av din plan. A **[!UICONTROL No work is saved]** visas för att bekräfta.
