---
title: Visa den aktuella versionsinformationen för Mix Modeler
description: Senaste versionsinformation för Mix Modeler
feature-set: Experience Cloud
feature: Release Notes
exl-id: 38a47672-2af2-437c-b769-4d5febb941f5
source-git-commit: 7581053507bd1a6a07b2f3853f454631ecee8cec
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# Aktuella versionsinformation för Mix Modeler

**Senast uppdaterad**: 26 februari 2026.

Versionsinformationen innehåller den senaste utgåvan av Mix Modeler. Mix Modeler-releaser fungerar enligt en kontinuerlig leveransmodell, vilket möjliggör en ungefärlig månadsvis publiceringsgräns. Versionsinformationen uppdateras därför, så kontrollera dem regelbundet.

## Februari 2026

| Funktion | Beskrivning | [Startar](#release-strategy) | [Allmän tillgänglighet](#release-strategy) |
|---|---|---|---|
| **Arbetsflöde för harmoniserade faktorer** | Faktorer hanteras nu som en del av ett [harmoniserat faktorarbetsflöde](/help/harmonize-data/overview.md#factors). Detta förenklar hur du [definierar faktordata](/help/ingest-data/schemas.md#factor-standard-fields-field-group), [hanterar interna och externa faktorer som en del av datauppsättningsreglerna](/help/harmonize-data/dataset-rules.md#factor-datasets) och hur du använder faktordata i [modeller](/help/models/build.md#configure). | 25 februari 2026 | 25 februari 2026 |
| **[!UICONTROL Granular incrementality reporting]** | Definiera harmoniserade fält så att du kan fördjupa dig i modellrapporteringen med [detaljerade insikter, rapportfält](/help/models/build.md#granular-insights-reporting-fields), i stället för att behöva skapa separata modeller. | 18 februari 2026 | 18 februari 2026 |

## Januari 2026

| Funktion | Beskrivning | [Startar](#release-strategy) | [Allmän tillgänglighet](#release-strategy) |
|---|---|---|---|
| **[!UICONTROL Dataset rules]** | [Uppdaterad regeltabell för datauppsättning](/help/harmonize-data/dataset-rules.md). Du kan söka efter en eller flera datauppsättningsregler och visa, redigera eller ta bort en datauppsättningsregel direkt från tabellen. | 13 januari 2026 | 13 januari 2026 |
| **[!UICONTROL Current spend]** | Lägg till en aktuell utgiftspunkt i visualiseringen av den [marginella kurvan](/help/models/insights.md#marginal-response-curves) i modellinsikter. | 13 januari 2026 | 13 januari 2026 |
| **[!UICONTROL Sort and resize columns]** | Sortering och storleksändring av kolumner i tabellen [Models](/help/models/overview.md) och [Planer](/help/plans/overview.md) har lagts till. | 13 januari 2026 | 13 januari 2026 |
| **Korrigeringar** | Fixar följande biljetter: <ul><li>AMM-3328: Fältindata inaktiverat för nya operatorer för faktorer</li><li>AMM-3359: Datumväljaren och kombinationslåset.</li><li>AMM-3441: Om du duplicerar en plan fylls inte datumintervallet och budgeten automatiskt i.</li></ul> | 13 januari 2026 | 13 januari 2026 |


## Frisläppningsstrategi

[!UICONTROL Mix Modeler] använder funktionsflaggor (kallas även&quot;växlar&quot;) för att styra synligheten för nya funktioner, vilket möjliggör kontrollerad skaltestning före den fullständiga versionen. Den här versionsstrategin innehåller följande faser:

* **Begränsad testning**: En fasversion börjar med att testas av interna Adobe-användare. Den görs sedan tillgänglig för en liten grupp kundkonton för att säkerställa att funktionen uppfyller kundernas behov och förväntningar.

* **Början av utrullning**: utrullningen av en fasversion börjar med den begränsade testfasen. Versionen skalas sedan från 0 % till 100 % för kunder under ett par månader. Utfasad utrullning sker på Experience Cloud-organisationsnivå, så att alla berättigade användare i en organisation får samma upplevelse.

