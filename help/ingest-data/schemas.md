---
title: Scheman
description: Lär dig hur du hanterar de scheman som behövs för att importera data till Mix Modeler.
feature: Schemas
exl-id: 08289581-5af9-4422-b049-8c24105e2a8e
source-git-commit: b0306ad6fad8966822ed14c67f159a4aefb4e3f8
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 2%

---

# Scheman

Så här hanterar du scheman och stöder de data du vill importera i Experience Platform och använda i Mix Modeler:

1. Gå till Mix Modeler gränssnitt.

1. Välj ![Scheman](/help/assets/icons/Schemas.svg) **[!UICONTROL Schemas]**, under **[!UICONTROL SETUP]**.

Mer information finns i [Översikt över användargränssnittet för scheman](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=sv-SE).

## Sammanställd eller sammanfattad data

Vi rekommenderar starkt att du använder klassen XDM Summary Metrics som bas för schemat som underliggande för alla sammanställningsdata eller sammanfattningsdata som du vill importera i Experience Platform och använda i Mix Modeler.

Använd klassen XDM Summary Metrics för:

- trädgårdsdata, till exempel data från Facebook eller YouTube.

- data om externa faktorer, som data från SPX (s&amp;P 500 aktiekursindex), väderdata,

- interna faktordata, till exempel prisändringar, en ledighetskalender.

>[!IMPORTANT]
>
>Schemadefinitionen måste innehålla minst ett numeriskt fält (med heltal, dubbel, Boolean eller annan numerisk typ) för att stödja de värden som krävs för inkapslade data.

Ett schema som använder basklassen **[!DNL XDM Summary Metrics]** kan vara enkelt, vilket visas i **[!DNL ExternalFactorSummarySchema]** nedan.

![Schema för externa faktorer](/help/assets/external-factors-schema.png)

Det här enkla schemat kan användas för att importera datauppsättningar som innehåller data, till exempel:

- Konkurrentindexdata

  | tidsstämpel | date_type | faktor | value |
  |---|---|---|--:|
  | 2020-11-28T00:00:00.000Z | vecka | konkurrent_index | 289,8 |
  | 2020-12-05T00:00:00.000Z | vecka | konkurrent_index | 291,2 |
  | 2020-12-12T00:00:00.000Z | vecka | konkurrent_index | 280,07 |
  | ... | ... | ... | ... |

- Offentliga semesterdata

  | tidsstämpel | date_type | faktor | value |
  |---|---|---|--:|
  | 2020-11-28T00:00:00.000Z | vecka | all_holidays_flag | 0,0 |
  | 2020-12-05T00:00:00.000Z | vecka | all_holidays_flag | 0,0 |
  | 2020-12-12T00:00:00.000Z | vecka | all_holidays_flag | 0,0 |
  | 2020-12-19T00:00:00.000Z | vecka | all_holidays_flag | 0,0 |
  | 2020-12-26T00:00:00.000Z | vecka | all_holidays_flag | 1,0 |
  | ... | ... | ... | ... |


Nedan finns ett mer omfattande exempel på **[!DNL LumaPaidMarketingSchema]** som använder **[!DNL XDM Summary Metrics]** som basklass. Schemat använder dedikerade fältgrupper (kommenterade med färger) för mått (**[!DNL AMMMetrics]**), dimensioner (**[!DNL AMMDimensions]**) och annan kundspecifik information (**[!DNL CustomerSpecific]**).

![Sammanfattningsschema](/help/assets/summary-schema.png)

Med tanke på den asynkrona typen av profilinmatning uppmuntras det att använda fältgruppen Extern Source System Audit Details som en del av ett schema när aggregerade data eller sammanfattningsdata samlas in från externa källor. Den här fältgruppen definierar en uppsättning granskningsegenskaper för externa källor.


## Datatyper som stöds

För närvarande stöder Mix Modeler en delmängd av Experience Platform datatyper. Följande grundläggande datatyper (fält), som nämns i [Grundläggande om schemakomposition](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=sv-SE#data-type), stöds:

- Sträng
- Heltal
- Dubbel
- Boolean
- Lång
- Kort
- Byte
- Datum
- Datum-tid


>[!MORELIKETHIS]
>
>- [Scheman](schemas.md)
