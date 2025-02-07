---
title: Översikt över harmoniserade datauppsättningar
description: Lär dig att harmonisera data i Mix Modeler.
feature: Harmonized Data
exl-id: 6cb70762-e3b2-46a0-b028-1d6daf3edae5
source-git-commit: f073e8f44fc2aa731a69725ebdb99700d1f91a91
workflow-type: tm+mt
source-wordcount: '895'
ht-degree: 5%

---

# Översikt över harmoniserade datauppsättningar

Data i Mix Modeler är av olika karaktär beroende på datakällan. Data kan vara:

* Sammanlagda eller sammanfattande data, t.ex. insamlade från datakällor i trädgården eller offlinereklam som samlats in (t.ex. utgifter) från en reklamkampanj, ett evenemang eller en fysisk annonskampanj.
* händelsedata, till exempel från datakällor från första part. Dessa händelsedata kan samlas in via Adobe Analytics-källanslutningen från Adobe Analytics, via Experience Platform Web eller Mobile SDK eller Edge Network, eller via data som hämtas via källanslutningar.

Harmoniseringstjänsten i Mix Modeler likställer aggregat och händelsedata i en enhetlig datavy. Den här datavyn, tillsammans med interna och externa faktordata, är källan för modellerna i Mix Modeler. Tjänsten använder den högsta granulariteten för de olika datauppsättningarna. Om en datauppsättning till exempel har en kornighet på månatliga och återstående datauppsättningar som har en kornighet varje vecka och dag, skapar harmoniseringstjänsten en datavy med hjälp av månatlig granularitet.

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
| 01-01-2022 00:01:01.000 | ECID | 64fd46ff-8c63-43b4-85a7-92b953113ba0 | ÄRENDE | 1 |
| 01-01-2022 00:01:01.000 | ECID | 64fd46ff-8c63-43b4-85a7-92b953113ba0 | ÄRENDE | 1 |
| 01-08-2022 00:01:01.000 | ECID | 2ca2a16e-caf0-4fa9-9a8b-9774b39547c4 | ÄRENDE | 1 |
| 01-08-2022 00:01:01.000 | ECID | 5ce99bfb-e44a-40d9-b8cd-c5408bda7cdc | ÄRENDE | 1 |

{style="table-layout:auto"}


Du vill skapa en harmoniserad datauppsättning med en granularitet som är inställd på veckovis. Händelsedata aggregeras till veckans granularitet och läggs till i den harmoniserade datamängden. Resultatet är:

**Harmoniserad datamängd**

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

Om du vill skapa en harmoniserad datauppsättning, som i det förenklade [exemplet](#an-example-of-harmonized-data), måste du följa dessa steg:

1. Definiera ytterligare [harmoniserade fält](fields.md) som du vill använda utöver de globala harmoniserade fält som redan är tillgängliga.
1. Konfigurera [datauppsättningsregler](dataset-rules.md) för att mappa fält från dina aggregerade data eller upplevelsehändelsedatamängder till harmoniserade fält.
1. Definiera [kontaktytor för marknadsföring](marketing-touchpoints.md) med hjälp av standardfälten och de ytterligare harmoniserade fälten som du har definierat.
1. Definiera [konverteringar](conversions.md) med hjälp av standardfälten och de ytterligare harmoniserade fälten som du har definierat.


## Visa harmoniserade data

För att se harmoniserade data i Mix Modeler-gränssnittet:

1. Välj ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized datasets]** i den vänstra listen.

1. Välj **[!UICONTROL Harmonized Data]** i det övre fältet. En sammanfattning av dina harmoniserade data visas baserat på de fält, datamängdsregler, kontaktytor för marknadsföring och konverteringar du har definierat.

   1. Om du vill definiera om den period som sammanfattningen av harmoniserade data baseras på anger du ett datumintervall för **[!UICONTROL Date range]** eller använder ![Kalender](/help/assets/icons/Calendar.svg) för att välja ett dataområde.

   1. Om du vill ändra de harmoniserade fältkolumnerna som visas för den harmoniserade datatabellen använder du ![Inställningar](/help/assets/icons/Setting.svg) för att öppna dialogrutan **[!UICONTROL Column settings]**.

      1. Välj ![SelectBox](/help/assets/icons/SelectBox.svg) en eller flera kolumner från **[!UICONTROL AVAILABLE COLUMNS]** och använd ![Sparron till höger](/help/assets/icons/ChevronRight.svg) för att lägga till de här kolumnerna i **[!UICONTROL SELECTED COLUMNS]**.

      1. Välj ![SelectBox](/help/assets/icons/SelectBox.svg) en eller flera kolumner från **[!UICONTROL SELECTED COLUMNS]** och använd ![Sparron till vänster](/help/assets/icons/ChevronLeft.svg) för att ta bort de markerade kolumnerna och returnera kolumnerna till **[!UICONTROL AVAILABLE COLUMNS]**.

      1. Välj en kolumn från **[!UICONTROL DEFAULT SORT]** och växla mellan **[!UICONTROL Ascending]** eller **[!UICONTROL Descending]**.

      1. Om du vill ändra visningsordningen för kolumner kan du flytta en kolumn i **[!UICONTROL SELECTED COLUMNS]** uppåt och nedåt genom att dra och släppa .

   1. Välj **[!UICONTROL Submit]** om du vill skicka in ändringar av kolumninställningen. Välj **[!UICONTROL Close]** om du vill avbryta alla ändringar du har gjort.

1. Om det finns fler sidor kan du använda ![Vänsterpil](/help/assets/icons/ChevronLeft.svg) eller ![Högerpil](/help/assets/icons/ChevronRight.svg) vid **[!UICONTROL Page _x _av_x_]** för att flytta mellan sidorna.
