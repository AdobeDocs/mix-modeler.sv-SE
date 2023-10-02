---
title: Scheman
description: Lär dig hur du hanterar scheman som krävs för att importera data till Mix Modeler.
feature: Schemas
source-git-commit: c145754ecd6a6d8f5aab333ced739c4053aeaae5
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 2%

---


# Scheman

Så här hanterar du scheman och stöder de data du vill importera i Adobe Experience Platform och använda i Mix Modeler:

1. Gå till gränssnittet Mix Modeler.

1. Välj ![Scheman](../assets/icons/Schemas.svg) **[!UICONTROL Schemas]**, under **[!UICONTROL DATA MANAGEMENT]**.

Se [Översikt över schemaanvändargränssnittet](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=en) för mer information.

## Sammanställd eller sammanfattad data

Vi rekommenderar starkt att du använder klassen XDM Summary Metrics som bas för schemat som underliggande för alla sammanställningsdata eller sammanfattningsdata som du vill importera i Experience Platform och använda i Mix Modeler.

Använd klassen XDM Summary Metrics för:

- trädgårdsdata, till exempel data från Facebook eller YouTube.

- data om externa faktorer, som data från SPX (s&amp;P 500 aktiekursindex), väderdata,

- interna faktordata, till exempel prisändringar, en ledighetskalender.

>[!IMPORTANT]
>
>Schemadefinitionen måste innehålla minst ett numeriskt fält (med heltal, dubbel, Boolean eller annan numerisk typ) för att stödja de värden som krävs för inkapslade data.

Ett schema som använder **[!DNL XDM Summary Metrics]** basklassen kan vara enkel, vilket visas i **[!DNL ExternalFactorSummarySchema]** nedan.

![Schema för externa faktorer](../assets/external-factors-schema.png)

Det här enkla schemat kan användas för att importera datauppsättningar som innehåller data för:

- Konkurrentindexdata

  | tidsstämpel | date_type | faktor | value |
  |---|---|---|--:|
  | 2020-11-28T00:00:00,000Z | vecka | konkurrent_index | 289.8 |
  | 2020-12-05T00:00:00,000Z | vecka | konkurrent_index | 291.2 |
  | 2020-12-12T00:00:00,000Z | vecka | konkurrent_index | 280.07 |
  | ... | ... | ... | ... |

- Offentliga semesterdata

  | tidsstämpel | date_type | faktor | value |
  |---|---|---|--:|
  | 2020-11-28T00:00:00,000Z | vecka | all_holidays_flag | 0.0 |
  | 2020-12-05T00:00:00,000Z | vecka | all_holidays_flag | 0.0 |
  | 2020-12-12T00:00:00,000Z | vecka | all_holidays_flag | 0.0 |
  | 2020-12-19T00:00:00,000Z | vecka | all_holidays_flag | 0.0 |
  | 2020-12-26T00:00:00,000Z | vecka | all_holidays_flag | 1.0 |
  | ... | ... | ... | ... |


Nedan finns ett mer omfattande exempel på **[!DNL LumaPaidMarketingSchema]** med **[!DNL XDM Summary Metrics]** som basklass. Schemat använder dedikerade fältgrupper (kommenterade med färger) för mått (**[!DNL AMMMetrics]**), dimensioner (**[!DNL AMMDimensions]**) och annan kundspecifik information (**[!DNL CustomerSpecific]**).

![Sammanfattningsschema](../assets/summary-schema.png)

Med tanke på den asynkrona typen av profilinmatning bör du använda fältgruppen Granskningsdetaljer för externt källsystem som en del av ett schema när du samlar in sammanställda eller sammanfattningsdata från externa källor. Den här fältgruppen definierar en uppsättning granskningsegenskaper för externa källor.
