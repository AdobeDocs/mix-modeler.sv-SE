---
title: Scheman
description: Lär dig hur du hanterar de scheman som behövs för att importera data till Adobe Mix-modelleraren.
feature: Datasets
source-git-commit: abbfc78e9fa774a240d000131f35d3dc257c15ea
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 1%

---


# Scheman

Så här hanterar du scheman och stöder de data du vill importera i Adobe Experience Platform och använda i Adobe Mix-modelleraren:

1. Gå till gränssnittet Adobe Mix Modeler.

1. Välj ![Scheman](../assets/icons/Schemas.svg) **[!UICONTROL Schemas]**, under **[!UICONTROL DATA MANAGEMENT]**.

Se [Översikt över schemaanvändargränssnittet](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=en) för mer information.

## Sammanställd eller sammanfattad data

Vi rekommenderar starkt att du använder klassen XDM Summary Metrics som bas för schemat som underliggande aggregerade data eller sammanfattningsdata som du vill importera i Experience Platform och använda i Adobe Mix Modeler.

Nedan finns ett exempel på en **[!DNL LumaPaidMarketingSchema]** med XDM Summary Metrics som basklass och dedikerade fältgrupper (kommenterade med färger) för mätvärden (**[!DNL AMMMetrics]**), dimensioner (**[!DNL AMMDimensions]**) och annan kundspecifik information (**[!DNL CustomerSpecific]**).

![Sammanfattningsschema](../assets/summary-schema.png)

Om du vill definiera en uppsättning granskningsegenskaper bör du använda fältgruppen Granskningsdetaljer för externt källsystem, som en del av ett schema som används för att samla in sammanställningsdata eller sammanfattningsdata från externa källor.
