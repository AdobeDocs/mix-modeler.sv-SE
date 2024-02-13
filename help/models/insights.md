---
title: Modellinsikter
description: Lär dig hur du får information om din modell, som historisk översikt, modellinsikter och modellkvalitet i Mix Modeler.
feature: Models
exl-id: d99852f9-ba0d-4a2e-b5f3-ca0efe6002fd
source-git-commit: 17d4609f251808f68372185ac90530e164024b5f
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 0%

---

# Modellinsikter

Visa modellinsikter i ![Models](../assets/icons/FileData.svg) **[!UICONTROL Models]** gränssnitt i Mix Modeler:

1. Markera namnet på en modell med en **[!UICONTROL Last run status]** av <span style="color:green">●</span> **[!UICONTROL Success]** från **[!UICONTROL Models]** tabell.

1. Välj **[!UICONTROL Model Insights]**.

Du ser när den angivna modellen senast har uppdaterats och widgetar visas på tre flikar: Historisk översikt, Modellinsikter och Modellkvalitet.

Du kan ändra den datumperiod som widgetarna på varje flik baseras på. Ange en datumperiod eller välj ![Kalender](../assets/icons/Calendar.svg) för att välja en datumperiod.


## Historisk översikt

På fliken Historik visas widgetar för:

* Konvertering och utgifter per kv och produkt.

* Utgift per kanal.

* Utlägg för kontaktpunkt.

  Du kan välja en alternativ utgiftsbaserad kanal att visa för den här widgeten. Välj en kanal från **[!UICONTROL Channels]**.

* Pekpunktsvolym.

  Du kan välja en alternativ volymbaserad kanal att visa för den här widgeten. Välj en kanal från **[!UICONTROL Channels]**.

![Modell - historisk översikt](../assets/model-historical-overview.png)

## Modellinsikter

På fliken Modellinsikter visas widgetar för:

* Bidrag per datum och basmedia. Det staplade diagrammet ordnas: Bas längst ned, Kanaler utan utgifter i mitten och Utläggskanaler överst.

* Bidrag per kanal.

* Sammanfattning av marknadsföringsprestanda.

* Marginalkurvor.

![Modell - modellinsikter](../assets/model-model-insights.png)

Du kan hovra över enskilda diagramelement i varje widget för att visa en pover med mer information.

Om du vill hämta en CSV-fil som innehåller data för widgeten väljer du ![Ladda ned](../assets/icons/Download.svg).

Om du vill hämta fullständiga data om modellinsikter i Microsoft® Excel-format väljer du ![Ladda ned](../assets/icons/Download.svg) **[!UICONTROL Download data]**.




## Modellkvalitet

På fliken Modellkvalitet visas widgetar för mätning:

* R2 (R-fyrkantig), som anger hur väl data passar in i regressionsmodellen (godheten i passform).

* MAPE (medelvärde för absolut procentfel), som är en av de mest använda KPI:erna för att mäta prognosens exakthet och uttrycker prognosfelet som en procentandel av det faktiska värdet.

* RMSE (Rot Mean Square Error): som visar det genomsnittliga felet, viktat enligt kvadraten på felet.

![Modellkvalitet](../assets/model-quality.png)

Om du vill hämta en CSV-fil som innehåller data för widgeten väljer du ![Mer](../assets/icons/More.svg) i widgeten och på snabbmenyn väljer ![Ladda ned](../assets/icons/Download.svg) **[!UICONTROL Download as CSV]**.
