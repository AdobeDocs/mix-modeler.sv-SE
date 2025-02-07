---
title: Värderingsdata för amerikansk e
description: Lär dig hur en modells poängdata i Mix Modeler bevaras.
feature: Models
exl-id: 2f2c3d20-7b14-41cc-a11a-03e8ad9e5d7a
source-git-commit: f073e8f44fc2aa731a69725ebdb99700d1f91a91
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 0%

---

# Använd poängdata

Som en del av poängsättningen för en modell lagras bedömningsdata i en datauppsättning i Experience Platform. När du har aktiverat multitouch-attribuering när du skapar en modell sparas ytterligare data om händelsepoäng i en datauppsättning i Experience Platform.

Alla dessa datauppsättningar följer ett schema. I den här artikeln beskrivs dessa scheman.


## Schema för sammanställd poängsättningsdata

Schemat för betygsdata har namnet `AMM AI Schema - <name of model> <id>`. Till exempel: `AMM AI Schema - Model for Online Conversion 10120`.

Datauppsättningen, som bevarar poängdata för en modell, namnges som `AMM AI Aggregrate Scores - <id>`, till exempel `AMM AI Aggregrate Scores - 10120`.

Schemat innehåller en fältgrupp med ett objekt som innehåller information om poängen. Objektet består av följande fält.

| Fältnamn | Typ | Definition |
|---|---|---|
| `campaignGroup` | Sträng | Namnet på kampanjgruppen. |
| `campaignName` | Sträng | Namnet på kampanjen. |
| `contribution` | Dubbel | Bidrag som härrör från denna konvertering för den angivna kontaktytan. |
| `conversionEndDate` | Datum | Slutdatum för konverteringsfönstret. |
| `conversionName` | Sträng | Namnet på den konvertering som skapades under konfigurationssteget för konverteringen. |
| `conversionStartDate` | Datum | Startdatum för konverteringsfönstret. |
| `geo` | Sträng | Den geografiska plats där konverteringen har skett. |
| `mediaChannel` | Sträng | Namnet på den kanal som användes under konfigurationssteget för kontaktytan. |
| `mediaSubChannel` | Sträng | Underkanalens namn. |
| `revenue` | Dubbel | Intäkter som härrör från denna konvertering för den angivna kontaktytan. |
| `scoreCreatedTime` | DateTime | Tidsstämpel när den här poängposten skapas. |
| `touchpointEndDate` | Datum | Slutdatum för pekpunktsfönstret. |
| `touchpointName` | Sträng | Namnet på den kontaktyta som skapades under konfigurationssteget för pekpunktsdefinitionen. Kontaktpunkten är för närvarande definierad i mediekanalen. |
| `touchpointStartDate` | Datum | Startdatum för pekpunktsfönstret. |


## Datamodell för händelsebedömning

Schemat för betygsdata har namnet `Attribution AI Scores - <name of model> <id> - Schema`. Till exempel: `Attribution AI Scores - Model for Online Conversion 10120 - Schema`.

Datauppsättningen, som bevarar poängdata för en modell, namnges som `Attribution AI Scores - <name of model> <id>`, till exempel `Attribution AI Scores - Model for Online Conversion 10120 `.

Schemat innehåller en fältgrupp som innehåller ett objekt med information om kärnorna. Objektet har namnet `attibution_AI_scores__<name of model> id`.

Fältgruppen innehåller följande fält.

| Fältnamn | Typ | Beskrivning |
|---|---|---|
| `conversion` | Objekt | Konvertera metadatakolumner. |
|     `passThrough` | Objekt |  |
|         `eventType` | Sträng | |
|         `channel_typeAtSource` | Sträng | |
|      `dataSource` | Sträng | Global unik identifiering av en datakälla. <br> **Exempel:** `Adobe Analytics` |
|      `eventSource` | Sträng | Källan när den faktiska händelsen inträffade. <br> **Exempel:** `Adobe.com` |
|      `eventType` | Sträng | Den primära händelsetypen för den här tidsserieposten. <br> **Exempel:** `Order` |
|      `geo` | Sträng | Den geografiska plats där konverteringen levererades `placeContext.geo.countryCode`. <br> **Exempel:** `US` |
|      `path` | Sträng | |
|      `priceTotal` | Dubbel | Intäkter som erhållits genom konverteringen <br> **Exempel:** `99.9` |
|      `product` | Sträng | XDM-identifieraren för själva produkten. <br> **Exempel:** `RX 1080 ti` |
|      `productType` | Sträng | Visningsnamnet för produkten som det visas för användaren för den här produktvyn. <br> **Exempel:** `Gpus` |
|      `quantity` | Heltal | Kvantitet som köpts under konverteringen. <br> **Exempel:** `1` |
|      `receivedTimeStamp` | DateTime | Tidsstämpel för konverteringen togs emot. <br> **Exempel:** `2020-06-09T00:01:51.000Z` |
|      `skuId` | Sträng | Lagerhållningsenhet (SKU), den unika identifieraren för en produkt som definieras av leverantören. <br> **Exempel:** `MJ-03-XS-Black` |
|      `timestamp` | DateTime | Tidsstämpel för konverteringen. <br> **Exempel:** `2020-06-09T00:01:51.000Z` |
|      `totalDaysToConversion` | Heltal |  |
|      `totalTouchpointCount` | Heltal | |
| `customerProfile` | Objekt | Identitetsinformation om användaren som användes för att skapa modellen. |
|      `identity` | Objekt | |
|           `id` | Sträng | |
|           `namespace` | Sträng | Innehåller information om användaren som används för att skapa modellen, till exempel `id` och `namespace`. |
| `touchpointsDetail` | Objekt [] | Listan med kontaktpunktsdetaljer som leder till konverteringen, ordnade efter kontaktytpunktsförekomst eller tidsstämpel. |
|      `scores` | Objekt | Pekpunktsbidrag till den här konverteringen som poäng. |
|           `algorithmicInfluenced` | Dubbel | Påverkade poäng är den del av konverteringen som varje kontaktyta för marknadsföring ansvarar för. |
|           `algorithmicSourced` | Dubbel | Inkrementell poäng är mängden marginell påverkan som direkt orsakas av en kontaktyta för marknadsföring. |
|           `decayUnits` | Dubbel | Regelbaserat attribueringspoäng där kontaktytor som ligger närmare konverteringen får mer kredit än kontaktytor som ligger längre bort från konverteringen. |
|           `firstTouch` | Dubbel | Regelbaserat attribueringspoäng som tilldelar alla krediter till den första kontaktytan på en konverteringsbana. |
|           `lastTouch` | Dubbel | Regelbaserat attribueringspoäng som tilldelar all kredit till den kontaktyta som ligger närmast konverteringen. |
|           `linear` | Dubbel | Regelbaserat attribueringspoäng som tilldelar varje kontaktyta samma poäng på en konverteringsbana. |
|           `uShape` | Dubbel | Regelbaserat attribueringspoäng som tilldelar 40 % av krediten till den första kontaktytan och 40 % av krediten till den sista kontaktytan. De andra kontaktytorna delar de återstående 20 % jämnt. |
|      `touchPoint` | Objekt | Kontaktpunktsmetadata. |
|           `passThrough` | Objekt | |
|                `eventType` | Sträng | |
|           `campaignGroup` | Sträng |  |
|           `campaignName` | Sträng | |
|           `campaignTag` | Sträng | |
|           `eventId` | Sträng | |
|           `geo` | Sträng | |
|           `mediaAction` | Sträng | |
|           `mediaChannel` | Sträng | |
|           `receivedTimeStamp` | DateTime | |
|           `timestamp` | DateTime | |
|      `isFirstInThePosition` | Heltal | |
|      `lag` | Heltal | |
|      `position` | Sträng | |
|      `touchpointCountToConversion` | Heltal | |
|      `touchpointName` | Sträng | Namnet på den kontaktyta som konfigurerades under installationen. <br> **Exempel:** `PAID_SEARCH_CLICK` |
| `conversionName` | Sträng | Namnet på konverteringen som konfigurerades under installationen. <br> **Exempel:** `Order`, `Lead`, `Visit` |
| `scoreCreatedTime` | DateTime | |
| `segmentation` | Sträng | Konverteringssegment som geosegmentering, som modellen är byggd mot. När segment saknas är `segmentation` samma som `conversionName`. <br> **Exempel:** `ORDER_US` |





Mer information finns i [Scheman](../ingest-data/schemas.md).
