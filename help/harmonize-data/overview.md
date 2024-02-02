---
title: Harmonisera data
description: Lär dig att harmonisera data i Mix Modeler.
feature: Harmonized Data
exl-id: 6cb70762-e3b2-46a0-b028-1d6daf3edae5
source-git-commit: 86732fe30637aa72ced232d9f331a3cc64baa39b
workflow-type: tm+mt
source-wordcount: '854'
ht-degree: 5%

---

# Harmonisera data

Data i Mix Modeler är av olika karaktär beroende på datakällan. Data kan vara:

* Sammanlagda eller sammanfattande data, t.ex. insamlade från datakällor i trädgården eller offlinereklam som samlats in (t.ex. utgifter) från en reklamkampanj, ett evenemang eller en fysisk annonskampanj.
* händelsedata, till exempel från datakällor från första part. Dessa händelsedata kan samlas in via Adobe Analytics källanslutning från Adobe Analytics, via Experience Platform Web eller Mobile SDK eller Edge Network API, eller data som hämtas via källanslutningar.

Harmoniseringstjänsten i Mix Modeler likställer aggregat och händelsedata i en enhetlig datavy. Den här datavyn, tillsammans med interna och externa faktordata, är källan för modellerna i Mix Modeler.

## Ett exempel på harmoniserade data

Tänk dig att du har följande datauppsättningar tillgängliga för Mix Modeler.

**Datauppsättning 1**

Innehåller datauppsättning för marknadsföringsinsats från YouTube, med en kornighet av aggregerade data inställda på dagligen.

| Datum | Datumtyp | Kanal | Campaign | Varumärke | Geo | Klickningar | Utgift |
|---|:--:|---|---|---|---|---:|---:|
| 12-31-2021 | dag | YouTube | Y_Höst_02 | BrandX | USA | 10000 | 100 |
| 01-01-2022 | dag | YouTube | Y_Höst_02 | BrandX | USA | 1000 | 10 |
| 01-03-2022 | dag | YouTube | Y_Höst_01 | BrandY | CA | 10000 | 100 |
| 01-04-2022 | dag | YouTube | Y_Sommar_01 | Null | CA | 9000 | 80 |

{style="table-layout:auto"}


**Datauppsättning 2**

Innehåller datauppsättning för marknadsföringsinsats från Facebook, med en kornighet av aggregerade data inställda på veckovis.

| Datum | Datumtyp | Kanal | Campaign | Geo | Klickningar | Utgift |
|--- |:---:|--- |---|---|---:|---:|
| 01-01-2022 | vecka | Facebook | FB_Höst_01 | USA | 8000 | 100 |
| 01-08-2022 | vecka | Facebook | FB_Höst_02 | USA | 1000 | 10 |
| 01-08-2022 | vecka | Facebook | FB_Höst_01 | USA | 7000 | 100 |
| 01-16-2022 | vecka | Facebook | FB_Sommar_01 | CA | 10000 | 80 |

{style="table-layout:auto"}


**Datauppsättning 3**

En konverteringsdatamängd med en kornighet av aggregerade data inställda på daglig.

| Datum | Datumtyp | Geo | Mål | Intäkter |
|--- |:---: |---|---|---:|
| 01-01-2022 | dag | USA | Fashion | 200 |
| 01-08-2022 | dag | USA | Fashion | 10 |
| 01-08-2022 | dag | USA | Juveler | 1100 |
| 01-16-2022 | dag | CA | Juveler | 80 |

{style="table-layout:auto"}


**Datauppsättning 4**

Ett exempel på en upplevelsehändelsedatamängd (Web SDK-händelser) från kunden.

| Tidsstämpel | Identitetsnamnutrymme | Identitets-ID | Kanal | Klickningar |
|--- |--- |--- |--- |---:|
| 01-01-2022 00:01:01,000 | ECID | 64fd46ff-8c63-43b4-85a7-92b953113ba0 | ÄRENDE | 1 |
| 01-01-2022 00:01:01,000 | ECID | 64fd46ff-8c63-43b4-85a7-92b953113ba0 | ÄRENDE | 1 |
| 01-08-2022 00:01:01,000 | ECID | 2ca2a16e-caf0-4fa9-9a8b-9774b39547c4 | ÄRENDE | 1 |
| 01-08-2022 00:01:01,000 | ECID | 5ce99bfb-e44a-40d9-b8cd-c5408bda7cdc | ÄRENDE | 1 |

{style="table-layout:auto"}


Du vill skapa en harmoniserad datauppsättning med en granularitet som är inställd på veckovis. Händelsedata aggregeras till veckans granularitet och läggs till i den harmoniserade datamängden. Resultatet är:

**Harmoniserad datauppsättning**

| Datum | Datumtyp | Kanal | Campaign | Varumärke | Geo | Mål | Klickningar | Utgift | Intäkter |
|--- |:---:|--- |--- |--- |---|---|---:|---:|---:|
| 12-27-2021 | vecka | YouTube | Y_Höst_02 | BrandX | USA | Null | 11000 | 110 | Null |
| 01-03-2022 | vecka | YouTube | Y_Höst_01 | BrandY | CA | Null | 10000 | 100 | Null |
| 01-03-2022 | vecka | YouTube | Y_Sommar_01 | Null | CA | Null | 9000 | 80 | Null |
| 01-01-2022 | vecka | Facebook | FB_Höst_01 | Null | USA | Null | 8000 | 100 | Null |
| 01-08-2022 | vecka | Facebook | FB_Höst_02 | Null | USA | Null | 1000 | 10 | Null |
| 01-08-2022 | vecka | Facebook | FB_Höst_01 | Null | USA | Null | 7000 | 100 | Null |
| 01-16-2022 | vecka | Facebook | FB_Sommar_01 | Null | CA | Null | 10000 | 80 | Null |
| 12-27-2021 | vecka | Null | Null | Null | USA | Fashion | Null | Null | 200 |
| 01-03-2022 | vecka | Null | Null | Null | USA | Fashion | Null | Null | 10 |
| 01-03-2022 | vecka | Null | Null | Null | USA | Juveler | Null | Null | 1100 |
| 01-10-2022 | vecka | Null | Null | Null | CA | Juveler | Null | Null | 80 |
| 01-01-2022 | vecka | ÄRENDE | Null | Null | Null | Null | 2 | Null | Null |
| 01-08-2022 | vecka | ÄRENDE | Null | Null | Null | Null | 2 | Null | Null |

{style="table-layout:auto"}


## Konfigurera harmoniserade data

Att bygga en harmoniserad datauppsättning, som i den förenklade [exempel](#an-example-of-harmonized-data)måste du följa dessa steg:

1. Definiera ytterligare [harmoniserade fält](fields.md) som du vill använda utanför de globalt harmoniserade fält som redan är tillgängliga.
1. Konfigurera [datauppsättningsregler](dataset-rules.md) för att mappa fält från dina aggregerade data eller upplevelsedatamängder till harmoniserade fält.
1. Definiera [kontaktytor](marketing-touchpoints.md) med hjälp av de standardiserade och ytterligare harmoniserade fält som du har definierat.
1. Definiera [konverteringar](conversions.md) med hjälp av de standardiserade och ytterligare harmoniserade fält som du har definierat.


## Visa harmoniserade data

För att se harmoniserade data i Mix Modeler-gränssnittet:

1. Välj ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized datasets]** från den vänstra listen.

1. Välj **[!UICONTROL Harmonized Data]** i det övre fältet. Ni ser en sammanfattning av era harmoniserade data baserat på de fält, datamängdsregler, kontaktytor och konverteringar ni har definierat.

   1. För att omdefiniera den period på vilken sammanfattningen av harmoniserade uppgifter baseras, ange ett datumintervall för **[!UICONTROL Date range]** eller använda ![Kalender](../assets/icons/Calendar.svg) för att markera ett dataområde.

   1. Om du vill ändra de harmoniserade fältkolumnerna som visas för den harmoniserade datatabellen använder du ![Inställningar](../assets/icons/Setting.svg) för att öppna **[!UICONTROL Column settings]** -dialogrutan.

      1. Välj ![SelectBox](../assets/icons/SelectBox.svg) en eller flera kolumner från **[!UICONTROL AVAILABLE COLUMNS]** och använda ![Sparr höger](../assets/icons/ChevronRight.svg) för att lägga till de här kolumnerna i **[!UICONTROL SELECTED COLUMNS]**.

      1. Välj ![SelectBox](../assets/icons/SelectBox.svg) en eller flera kolumner från **[!UICONTROL SELECTED COLUMNS]** och använda ![Chevron vänster](../assets/icons/ChevronLeft.svg) för att ta bort de markerade kolumnerna och returnera dessa kolumner till **[!UICONTROL AVAILABLE COLUMNS]**.

      1. Välj en kolumn från **[!UICONTROL DEFAULT SORT]** och växla **[!UICONTROL Ascending]** eller **[!UICONTROL Descending]**.

      1. Om du vill ändra visningsordningen för kolumner kan du flytta en kolumn i **[!UICONTROL SELECTED COLUMNS]** upp och ned genom att dra och släppa.

   1. Välj **[!UICONTROL Submit]** om du vill skicka in ändringar av kolumninställningen. Välj **[!UICONTROL Close]** om du vill avbryta alla ändringar du har gjort.

1. Om det finns fler tillgängliga sidor använder du ![Pil vänster](../assets/icons/ChevronLeft.svg) eller ![Högerpil](../assets/icons/ChevronRight.svg) på **[!UICONTROL Page _x _av_x_]** för att flytta mellan sidor.
