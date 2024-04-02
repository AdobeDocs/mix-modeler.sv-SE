---
title: Modellinsikter
description: Lär dig hur du får information om din modell, som historisk översikt, modellinsikter och modellkvalitet i Mix Modeler.
feature: Models
exl-id: d99852f9-ba0d-4a2e-b5f3-ca0efe6002fd
source-git-commit: 4f4c7f05e90d73a0ab4865150b1ec4c2af88fc12
workflow-type: tm+mt
source-wordcount: '388'
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

* Bidrag per datum och basmedia. Det staplade diagrammet ordnas: Bas längst ned, Ej använda kanaler i mitten och Utläggskanaler överst.

* Bidrag per kanal.

* Sammanfattning av marknadsföringsprestanda.

* Marginalkurvor.

![Modell - modellinsikter](../assets/model-model-insights.png)

Du kan hovra över enskilda diagramelement i varje widget för att visa en pover med mer information.

Om du vill hämta en CSV-fil som innehåller data för widgeten väljer du ![Ladda ned](../assets/icons/Download.svg).

Om du vill hämta fullständiga data om modellinsikter i Microsoft® Excel-format väljer du ![Ladda ned](../assets/icons/Download.svg) **[!UICONTROL Download data]**.


## Modellkvalitet

![Modellkvalitetsbedömning](/help/assets/model-quality-assessment.png)
På fliken för modellkvalitet visas en

* [!UICONTROL Model Assessment] visualisering, som du kan bryta ned på faktiska kontra förväntade eller kvarstående konverteringar.

  Om du vill bryta ned visualiseringen väljer du **[!UICONTROL Actual vs. Predicted]** eller **[!UICONTROL Residuals]** från **[!UICONTROL Breakdown]** lista.

* [!UICONTROL Model fitting metrics] tabell, med följande kolumner för varje konverteringsmått:

   * Faktisk konvertering

   * Modellerad konvertering

   * Restkonvertering (skillnad mellan faktisk konvertering och modellkonvertering)

   * Värden för modellkvalitetsskala:

      * R2 (R-fyrkantig), som anger hur väl data passar in i regressionsmodellen (godheten i passform).

      * MAPE (medelvärde för absolut procentfel), som är en av de mest använda KPI:erna för att mäta prognosens exakthet och uttrycker prognosfelet som en procentandel av det faktiska värdet.

      * RMSE (Rot Mean Square Error): som visar det genomsnittliga felet, viktat enligt kvadraten på felet.

  Om du vill hämta en CSV-fil som innehåller data för tabellen väljer du ![Ladda ned](../assets/icons/Download.svg).
