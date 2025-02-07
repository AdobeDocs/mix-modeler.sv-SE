---
title: Mix Modeler arbetsflöde
description: Förstå det typiska arbetsflödet för Mix Modeler.
feature: Ingest Data, Plans, Harmonized Data, Models
exl-id: 200ff846-5d78-4b25-a425-bfd558b88c88
source-git-commit: f12eea7454d1c81b347dc4960f5c491d81725f7d
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---

# Mix Modeler arbetsflöde

I den här videon visas en introduktion till användararbetsflödet i Mix Modeler.

>[!VIDEO](https://video.tv.adobe.com/v/3424854/?learn=on)


Ett typiskt arbetsflöde i Mix Modeler består av följande aktiviteter:

![Alt-text](/help/assets/ApplicationWorkflow.svg)

|  | Aktivitet | Beskrivning |
|---|---|---|
| ![Data](/help/assets/icons/Data.svg){width="100"} | [**Ingest data**](../ingest-data/overview.md) | Ingest event data from Experience Platform (t.ex. Adobe Analytics, Web SDK, andra källor), aggregerad data från marknadsföringskanaler (t.ex. TV, trädgårdar, e-post, ägda och drivna aktiviteter), externa faktordata från kunder (t.ex. prisförändringar i prenumerationstjänster) och interna faktordata (t.ex. semesterplaner). |
| ![DataCheck](/help/assets/icons/DataCheck.svg){width="100"} | [**Harmonisera data**](../harmonize-data/overview.md) | Konfigurera mappningsregler och konfliktlösningsregler för att sammanfoga de olika marknadsföringsdatauppsättningar som behövs för att mäta och planera kampanjprestanda i Mix Modeler. |
| ![FileConfig](/help/assets/icons/FileGear.svg){width="100"} | [**Skapa modeller**](../models/overview.md) | Bygg modellinstanser med kontaktytor för marknadsföring (t.ex. kanaler), konverteringsdefinitioner samt interna och externa faktorer. |
| ![FileData](/help/assets/icons/FileData.svg){width="100"} | [**Modeller för utbildning och bakgrundsmusik**](../models/overview.md) | Skapa bakgrundsmusik och poäng på händelsenivå med maskininlärning och poängsättning. |
| ![FileChart](/help/assets/icons/FileChart.svg){width="100"} | [**Skapa planer**](../plans/overview.md) | Skapa och bygga planer. Bestäm den bästa fördelningen av marknadsföringsmedel för att uppnå ett affärsmål genom att använda produktionen från Mix Modeler-modeller. |
| ![Instrumentpanel](/help/assets/icons/Dashboard.svg){width="100"} | [**Översikt över instrumentpanel**](../dashboard/overview.md) | Få insikter om harmoniserade data, modeller och planer med olika konfigurerbara visualiseringar. |

{style="table-layout:auto"}

<!---
The detailed data-oriented flowchart below illustrates how:

* harmonized data is based on:

  * experience event data (originating from Analytics source connector, collected through Experience Platform SDKs and APIs, ingested through source connectors, or using streaming ingestion),
  * aggregate or summary data from walled gardens (like Facebook, YouTube), traffic sources, or offline advertising data, and 
  * definitions of harmonized fields and dataset rules.

* a model is based on:

  * the conversion and marketing touchpoint definitions resulting from the harmonized data and 
  * non-marketing aggregate or summary data containing internal or external factors.

* mult-touch attribution event scores can potentially be fed back into Experience Platform data lake for use in subsequent model configuration, training and scoring.

![Comprehensive workflow](/help/assets/comprehensive-workflow.svg)

-->
