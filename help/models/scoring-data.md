---
title: Poängdata
description: Lär dig hur en modells poängdata i Mix Modeler bevaras.
feature: Models
exl-id: 2f2c3d20-7b14-41cc-a11a-03e8ad9e5d7a
source-git-commit: 86732fe30637aa72ced232d9f331a3cc64baa39b
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 0%

---

# Poängdata

Som en del av poängsättningen för en modell lagras bedömningsdata i en datauppsättning i Experience Platform. Den här datauppsättningen följer ett schema som skapats för varje modell i din Mix Modeler-instans.

Schemat för betygsdata har namnet `AMM AI Schema - <name of model> <id>`. Till exempel: `AMM AI Schema - Model for Online Conversion 10120`.

Datauppsättningen, som bevarar poängdata för en modell, namnges som `AMM AI Aggregrate Scores - <id>`, till exempel `AMM AI Aggregrate Scores - 10120`.


## Schema

Schemat innehåller en fältgrupp med ett objekt som innehåller information om poängen. Objektet består av följande fält.

| Fältnamn | Typ | Definition |
|---|---|---|
| **campaignGroup** | Sträng | Namnet på kampanjgruppen. |
| **campaignName** | Sträng | Namnet på kampanjen. |
| **bidrag** | Dubbel | Bidrag som härrör från denna konvertering för den angivna kontaktytan. |
| **conversionEndDate** | Datum | Slutdatum för konverteringsfönstret. |
| **conversionName** | Sträng | Namnet på den konvertering som skapades under konfigurationssteget för konverteringen. |
| **conversionStartDate** | Datum | Startdatum för konverteringsfönstret. |
| **geo** | Sträng | Den geografiska plats där konverteringen har skett. |
| **mediaChannel** | Sträng | Namnet på den kanal som användes under konfigurationssteget för kontaktytan. |
| **mediaSubChannel** | Sträng | Underkanalens namn. |
| **intäkter** | Dubbel | Intäkter som härrör från denna konvertering för den angivna kontaktytan. |
| **scoreCreatedTime** | DateTime | Tid när den här poängposten skapas. |
| **touchPointEndDate** | Datum | Slutdatum för pekpunktsfönstret. |
| **touchpointName** | Sträng | Namnet på den kontaktyta som skapades under konfigurationssteget för pekpunktsdefinitionen. Kontaktpunkten är för närvarande definierad i mediekanalen. |
| **kontaktytaStartdatum** | Datum | Startdatum för pekpunktsfönstret. |

Mer information finns i [Scheman](../ingest-data/schemas.md).
