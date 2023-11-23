---
title: Poängdata
description: Lär dig hur en modells poängdata i Mix Modeler bevaras.
feature: Models
source-git-commit: 3596b83937b3f61ac453940f3a666d8aaf713679
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 3%

---


# Poängdata

Som en del av poängsättningen för en modell lagras bedömningsdata i en datauppsättning i Experience Platform. Den här datauppsättningen följer ett schema som skapats för varje modell i din Mix Modeler-instans.

Schemat för bedömning av data har namn som `AMM AI Schema - <name of model> <id>`. Exempel: `AMM AI Schema - Model for Online Conversion 10120`.

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
| **intäkt** | Dubbel | Intäkter som härrör från denna konvertering för den angivna kontaktytan. |
| **scoreCreatedTime** | DateTime | Tid när den här poängposten skapas. |
| **touchpointEndDate** | Datum | Slutdatum för pekpunktsfönstret. |
| **touchpointName** | Sträng | Namnet på den kontaktyta som skapades under konfigurationssteget för pekpunktsdefinitionen. Kontaktpunkten är för närvarande definierad i mediekanalen. |
| **touchpointStartDate** | Datum | Startdatum för pekpunktsfönstret. |

