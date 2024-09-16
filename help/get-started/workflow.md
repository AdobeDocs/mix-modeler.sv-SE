---
title: Mix Modeler arbetsflöde
description: Förstå det typiska arbetsflödet för Mix Modeler.
feature: Ingest Data, Plans, Harmonized Data, Models
exl-id: 200ff846-5d78-4b25-a425-bfd558b88c88
source-git-commit: 9a6c1f1c12ab29da80a1997cfd31ca07b38eaa22
workflow-type: tm+mt
source-wordcount: '302'
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
| ![FileConfig](/help/assets/icons/FileGear.svg){width="100"} | [**Konfigurera modeller**](../models/create.md) | Konfigurera modellinstanser med marknadsföringskontaktytor (t.ex. kanaler), konverteringsdefinitioner samt interna och externa faktorer. |
| ![FileData](/help/assets/icons/FileData.svg){width="100"} | [**Modeller för utbildning och bakgrundsmusik**](../models/overview.md) | Skapa bakgrundsmusik och poäng på händelsenivå med maskininlärning och poängsättning. |
| ![FileChart](/help/assets/icons/FileChart.svg){width="100"} | [**Skapa planer**](../plans/overview.md) | Bestäm den bästa fördelningen av marknadsföringsmedel för att uppnå ett affärsmål genom att använda produktionen från Mix Modeler-modeller. |
| ![Instrumentpanel](/help/assets/icons/Dashboard.svg){width="100"} | [**Översikt över instrumentpanel**](../dashboard/overview.md) | Få insikter om harmoniserade data, modeller och planer med olika konfigurerbara visualiseringar. |

{style="table-layout:auto"}

Det detaljerade dataorienterade flödesschemat nedan visar hur:

* harmoniserade uppgifter bygger på

   * upplevelsehändelsedata (som kommer från Analytics-källkopplingen, samlas in via Experience Platform SDK:er och API:er, hämtas via källanslutningar eller med direktuppspelningsinmatning),
   * sammanställda eller sammanfattande data från trädgårdar (som Facebook, YouTube), trafikkällor eller offlinereklam, och
   * definitioner av harmoniserade fält och datauppsättningsregler.

* en modell baseras på:

   * de konverterings- och marknadsdefinitioner som följer av harmoniserade data och
   * sammanställda eller sammanfattande data som inte är marknadsför och som innehåller interna eller externa faktorer.

* poäng för attribueringshändelser med flera beröringspunkter kan eventuellt matas tillbaka till Experience Platform datasjön för användning i efterföljande modellkonfiguration, utbildning och poängsättning.

![Omfattande arbetsflöde](/help/assets/comprehensive-workflow.svg)
