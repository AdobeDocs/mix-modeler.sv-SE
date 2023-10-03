---
title: Mix Modeler arbetsflöde
description: Förstå det typiska arbetsflödet för Mix Modeler.
feature: Ingest Data, Plans, Harmonized Data, Models
exl-id: 200ff846-5d78-4b25-a425-bfd558b88c88
source-git-commit: 33883626d8e7aca2eecc3571593be53ef41ac458
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 0%

---

# Mix Modeler arbetsflöde

Ett typiskt arbetsflöde i Mix Modeler ser ut så här:

![Alt-text](../assets/ApplicationWorkflow.svg)

|  | Aktivitet | Beskrivning |
|---|---|---|
| ![Data](../assets/icons/Data.svg){width="100"} | [**Ingrediera data**](../ingest-data/overview.md) | Ingest event data from Experience Platform (t.ex. Adobe Analytics, Web SDK, andra källor), aggregerad data från marknadsföringskanaler (t.ex. TV, trädgårdar, e-post, ägda och drivna aktiviteter), externa faktordata från kunder (t.ex. prisförändringar i prenumerationstjänster) och interna faktordata (t.ex. semesterplaner). |
| ![DataCheck](../assets/icons/DataCheck.svg){width="100"} | [**Harmonisera data**](../harmonize-data/overview.md) | Konfigurera mappningsregler och konfliktlösningsregler för att sammanfoga de olika marknadsföringsdatauppsättningar som behövs för att mäta och planera kampanjprestanda i Mix Modeler. |
| ![FileConfig](../assets/icons/FileGear.svg){width="100"} | [**Konfigurera modeller**](../models/create.md) | Konfigurera modellinstanser med marknadsföringskontaktytor (till exempel kanaler) och konverteringsdefinitioner. |
| ![FileData](../assets/icons/FileData.svg){width="100"} | [**Tåg- och poängmodeller**](../models/overview.md) | Skapa bakgrundsmusik och poäng på händelsenivå med maskininlärning och poängsättning. |
| ![FileChart](../assets/icons/FileChart.svg){width="100"} | [**Skapa planer**](../plans/overview.md) | Bestäm den bästa fördelningen av marknadsföringsmedel för att uppnå ett affärsmål genom att använda produktionen från Mix Modeler-modeller. |
| ![Kontrollpanel](../assets/icons/Dashboard.svg){width="100"} | [**Översikt över instrumentpanel**](../dashboard/overview.md) | Få insikter om harmoniserade data, modeller och planer med olika konfigurerbara widgetar. |

{style="table-layout:auto"}
