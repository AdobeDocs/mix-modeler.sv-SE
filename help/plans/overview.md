---
title: Planer - översikt
description: Lär dig hur du visar, väljer ut och utför åtgärder på planer i Mix Modeler.
feature: Plans
exl-id: 45a8dc30-3259-493d-8ea5-1899903733a6
source-git-commit: 0d11168b71319e6c854482f89dbb1bb68962a880
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 0%

---

# Planer - översikt

Med planer i Mix Modeler kan ni fördela budgetar per affärsenhet och kanal. Planeringsfunktionen är integrerad med resultaten av de utbildade modellerna baserade på era harmoniserade data.

I en plan beskrivs de diskretionära investeringar (till exempel budgetar) som ett företag avser att spendera på marknadsrelaterade projekt under en viss tidsperiod. Dessa investeringar är till för gemensamma nyckeltal (t.ex. order, intäkter). Planer kan innehålla kostnader från kanaler som betald annonsering, sponsrat webbinnehåll och evenemang.

En plan kräver:

- en modell,
- ett dataområde,
- en budget.

En plan kan även innehålla:

- ett konfigurerat igenkänningsfönster,
- flera flygdatum där var och en har en målbudget,
- minsta och högsta budgetbegränsningar per kanal och flygdatum.

Om en modell som du har använt för din plan baseras på nya data måste du skapa en ny plan som tar hänsyn till ompoängterade data.


## Skapa planer

Om du vill skapa en plan använder du guiden Skapa Mix Modeler-plan. Mer information finns i [Skapa planer](build.md).


## Hantera planer

Om du vill visa en tabell över dina aktuella planer går du till Mix Modeler-gränssnittet:

1. Välj ![](/help/assets/icons2/FileChart.svg) **[!UICONTROL Plans]** i den vänstra listen.

1. Du ser en tabell över aktuella planer och deras status.

   Tabellkolumnerna anger information om planerna.

   | Kolumnnamn | Information |
   |---|---|
   | Namn | Namn på planen |
   | Modell | Modellen som används som bas för planen. |
   | Datumintervall | Det fullständiga datumintervallet för en plan. |
   | Budget | Den totala budgeten för en plan. |
   | Planmål | Målmåttet som har definierats för en målbaserad plan. |
   | Prognostiserad avkastning | Den [prognostiserade avkastningen](/help/main-guide/glossary.md) för en plan |
   | Prognostiserad avkastning | Den [prognostiserade avkastningen ](/help/main-guide/glossary.md) för en plan. |
   | Prognostiserad konvertering | Den [prognostiserade konverteringen](/help/main-guide/glossary.md) för en plan |
   | Prognostiserad CPA | [Prognostiserat CPA](/help/main-guide/glossary.md)för en plan |
   | Status | Status för en plan: <p><span style="color:red">●</span> misslyckades, <p><span style="color:blue">●</span> bearbetar, eller <p><span style="color:green">●</span> har slutförts. |

   {style="table-layout:auto"}

   Du kan använda ![ColumnSetting](/help/assets/icons/ColumnSetting.svg) för att markera ![Bock](/help/assets/icons/Checkmark.svg) de kolumner som ska visas i tabellen.

   Om du vill sortera tabellen i en kolumn i stigande ![ArrowMoveUp](/help/assets/icons2/ArrowMoveUp.svg)- eller fallande ![ArrowMoveDown](/help/assets/icons2/ArrowMoveDown.svg)ordning, markerar du kolumnens rubrik.

   Om du vill sortera eller ändra storlek på kolumnen **[!UICONTROL Name]**, **[!UICONTROL Model]** eller **[!UICONTROL Date range]** väljer du **[!UICONTROL Name]** ![ChevronDown](/help/assets/icons/ChevronDown.svg), **[!UICONTROL Model]** ![ChevronDown](/help/assets/icons/ChevronDown.svg) eller **[!UICONTROL Date range]** ![ChevronDown](/help/assets/icons/ChevronDown.svg). Välj **[!UICONTROL Sort ascending]**, **[!UICONTROL Sort descending]** eller **[!UICONTROL Resize column]** på snabbmenyn. Du kan också hålla markören över kolumnavgränsaren för dessa kolumner för att ändra storlek på en kolumn.

1. Använd ![Sök](/help/assets/icons/Search.svg) om du vill söka efter och filtrera tabellen efter en eller flera specifika planer.

### Planera insikter

Så här visar du insikterna för en plan och redigerar en plan:

1. Välj ![PLan](/help/assets/icons/FileChart.svg) **[!UICONTROL Plans]** i den vänstra listen.

1. Välj planens namn.

Du omdirigeras till [planinsikter](insights.md).


### Duplicera en plan

Så här duplicerar du en plan:

- Välj ![Mer](/help/assets/icons/More.svg) för en plan. Välj **[!UICONTROL Duplicate]** på snabbmenyn.
- Du kan också välja en plan i tabellen ![SelectBox](/help/assets/icons/SelectBox.svg) och välja ![Kopiera](/help/assets/icons/Copy.svg) **[!UICONTROL Duplicate]** i det blå åtgärdsfältet.

En ny plan, med ett namn som består av den ursprungliga planens namn som har lagts till med **[!UICONTROL (Copy)](_n_)**, skapas. Du omdirigeras automatiskt till [Planskapande](build.md) för att tillhandahålla uppdaterad information om den kopierade planen.

- Information (som Beskrivning, Budget med mera) från den ursprungliga planen kopieras över.
- Budgetbegränsningar från den ursprungliga planen kopieras till den nya planen.
- Du kan välja en annan modell som bas för den kopierade planen.
   - För kontaktytor eller kanaler som finns i den kopierade planen, men som inte finns i den nyligen valda modellen, tas alla begränsningar för dessa kontaktytor eller kanaler bort från planen.
   - För kontaktytor eller kanaler som inte finns i den kopierade planen, men som finns i den nyligen valda modellen, ställs begränsningarna in på:
      - ett minsta värde på `0`,
      - ett maximalt värde i linje med planens flygintervallbudget.



### Jämför planer

Så här jämför du planer:

1. Välj två planer i tabellen.
1. Välj ![Jämför](/help/assets/icons/Compare.svg) **[!UICONTROL Compare]** i det blå åtgärdsfältet. Du ser användargränssnittet för **[!UICONTROL Compare plans]**.


### Ta bort planer

Så här tar du bort en plan:

1. Välj ![Mer](/help/assets/icons/More.svg) för en plan. Välj **[!UICONTROL Delete]** på snabbmenyn. <br/>Du kan också välja en plan i tabellen ![SelectBox](/help/assets/icons/SelectBox.svg) och välja ![Delete](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** i det blå åtgärdsfältet.
1. Välj **[!UICONTROL Delete]** i bekräftelsedialogrutan **[!UICONTROL Delete plan]** om du vill ta bort planen. Välj **[!UICONTROL Cancel]** om du vill avbryta.

Så här tar du bort flera planer:

1. Välj flera planer.
1. Välj ![Ta bort](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** i det blå åtgärdsfältet för att ta bort planerna.
1. Välj **[!UICONTROL Delete]** i bekräftelsedialogrutan för **[!UICONTROL Delete *x *-planer]**om du vill ta bort planerna. Välj **[!UICONTROL Cancel]**om du vill avbryta.


