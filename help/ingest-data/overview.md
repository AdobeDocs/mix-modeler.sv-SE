---
title: Översikt över infogningsdata
description: Lär dig hur du importerar data till Mix Modeler.
feature: Datasets, Event Datasets, Summary Datasets, Aggregate Datasets
exl-id: dc16a601-bbd9-467b-8a7e-c32654d4069a
source-git-commit: 1a9df9f9819d9e0031e58443ec6a9e755a151ba0
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 5%

---

# Översikt över infogningsdata

Mix Modeler arbetar med data på händelsenivå, sammanställda eller sammanfattande data om marknadsföringsinsatser från olika trädgårdar. Och med sammanställda eller sammanfattande data från andra källor, som offlinereklam, interna faktorer eller externa faktorer.

Kunderna kan använda alla typer av data som är inkapslade i Experience Platform som datauppsättningar och som är baserade på scheman med hjälp av XDM ExperienceEvent eller XDM Summary Metrics som basklass.

Exempel:

* Data samlas in med Adobe Analytics källanslutning. Och omvandlades till datauppsättningar som överensstämmer med standardversionen eller en anpassad version av Adobe Analytics-schemat.
* Data som samlats in med Experience Platform Web SDK, Mobile SDK eller Edge Network Server API för att samla in kundinteraktioner på webben, mobiler eller andra typer av enheter.
* Samla in eller sammanfatta data från uttjänta trädgårdar (som Facebook, YouTube), trafikkällor eller offlinereklam.
* Sammanlagda eller sammanfattande data som inte är marknadsförda och som innehåller interna eller externa faktorer som är användbara för modelluppbyggnad.

Ni kan använda vilken mekanism som helst, som stöds av Experience Platform, för att hämta data på upplevelsehändelsenivå, aggregerade marknadsföringssatsdata och data från andra källor. som Experience Platform SDK:er, API:er, källanslutningar samt strömning och batchförbrukning. Om du vill veta mer om hur du samlar in data i Experience Platform för användning i Adobe Mix Modeler kan du läsa [översikten över datainmatning](https://experienceleague.adobe.com/sv/docs/experience-platform/ingestion/home).

## Riktlinjer

Följ dessa riktlinjer när du vill importera data till Experience Platform för användning med Mix Modeler:

* De inkrementella data som läggs till i datauppsättningarna får inte överlappa varandra.
* Alla data från en enda källa ska vara av samma granularitet.
* Datum och granularitet är obligatoriska fält i det underliggande schemat för alla sammanställda data som hämtas som datamängder
* Kanalen är ett obligatoriskt fält i det underliggande schemat för alla marknadsföringsinsatser/utgiftsdata som matats in som datauppsättningar.


## Exempel

Nedan finns några exempel på data som vanligtvis används i Mix Modeler utöver de mer vanliga händelsedatan för upplevelser.

+++ Sammanställd information om marknadsföringsinsats

| Geo | Datum | Datumtyp | Kanal | Campaign | Klicka på | Intjänad | Engagemang | Impression | Öppna | Ägt | Skickat | Utgift |
|---|:--|---|:---:|---|--:|---|--:|---|---|---|--:|--:|
| AMER | 2021-10-31 | dag | E-POST | | 12752 | | | | | | 1132945 | |
| AMER | 2021-10-31 | dag | FB | | 148844 | | | | | | | 42111 |
| AMER | 2021-10-31 | dag | JT | | | | 2314452 | | | | | 10540 |
| JPN | 2021-10-21 | dag | E-POST | | 21089 | | | | | | 3283626 | |
| JPN | 2021-10-21 | dag | SOCIALA | | | | 621 | | | | | 74512 |

{style="table-layout:auto"}

+++

+++ Sammanställa konverteringsdata

| Geo | Datum | Datumtyp | Produkt | Sålda enheter | Intäkter |
|---|:---|:---:|---|--:|--:|
| EMEA | 2021-09-13 | dag | Skapare av ekonomi | 603 | 36537,68 |
| EMEA | 2021-09-13 | dag | Metaverse | 55 | 21704,37 |
| JPN | 2022-05-30 | dag | Pro Imaging | 487 | 64469,60 |
| JPN | 2022-05-30 | dag | Document Cloud | 642 | 100509,07 |

{style="table-layout:auto"}

+++

+++ Externa faktordata

| Data | Datumtyp | Faktor | Värde |
|---|:---:|:---:|:---|
| 2020-08-02 | vecka | SPX | 3325,866 |
| 2020-08-09 | vecka | SPX | 3364,158 |
| 2020-08-16 | vecka | SPX | 3385,858 |
| 2020-08-23 | vecka | SPX | 3497,965 |

{style="table-layout:auto"}

+++

För att kunna arbeta med data i Mix Modeler behöver du data som samlats in i datauppsättningar och modellerats efter scheman i Experience Platform. Mix Modeler-gränssnittet ger enkel åtkomst till både Experience Platform Scheman och datauppsättningsgränssnittet.


## Validera

Så här validerar du om dina data är tillgängliga i Mix Modeler:

* Använd visualiseringar i [översikten](/help/overview.md).
* Hämta och inspektera data från [harmoniserade data](/help/harmonize-data/overview.md) i harmoniserade datauppsättningar.

Om du vill verifiera om dina data har importerats korrekt i Experience Platform kan du [skriva och köra SQL-frågor med Experience Platform Query Service](https://experienceleague.adobe.com/sv/docs/experience-platform/query/home).


>[!MORELIKETHIS]
>
>Mer information om hur du hanterar scheman och datauppsättningar finns i:
>
>* [Scheman](schemas.md)
>* [Datauppsättningar](datasets.md)
