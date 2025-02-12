---
title: Datastyrningsöversikt
description: Lär dig hur du använder de tjänster och verktyg från Experience Platform som gör att du kan kontrollera dina insamlade upplevelsedata. Så att ni följer era rutiner, juridiska skyldigheter och utvecklingsprocesser.
feature: Administration
exl-id: 87407c29-e158-48bf-bde9-b3c16a16107e
source-git-commit: 0ee212a626986e4c721d0e58f2528d0ca1a9fdbf
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 0%

---

# Datastyrningsöversikt

Integrationen mellan Mix Modeler och Experience Platform ger Mix Modeler möjlighet att utnyttja Experience Platform inneboende funktioner för datastyrning. I det här avsnittet av dokumentationen beskrivs detaljerna för de funktioner för datastyrning som finns i Mix Modeler.

Experience Platform datastyrning ger er möjlighet att kontrollera och förstå era data under hela den resa som data tar genom Experience Platform. Den här resan innebär att upprätthålla datakvalitet, datalinje, datakatalogisering och mycket annat.

Etiketter och profiler för dataanvändning som skapas på datauppsättningar som används av Experience Platform i Mix Modeler, där så är lämpligt. Dessa etiketter stoppar eller varnar till exempel användare när de tar bort datauppsättningar som ingår i en datauppsättningsregel i harmoniserade data. Eller dölj schemafält som är begränsade för användare när en datauppsättningsregel skapas.

Tack vare integreringen av datastyrning kan ni hantera regelefterlevnaden effektivare. Datahanteringen i organisationen kan ange regler som begränsar användningen. Det innebär att du kan använda data som överensstämmer med policyer som definieras av data stewards. Läs dokumentationen om [Etiketter och profiler](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/data-governance) om du vill veta mer.

Följande funktioner för datastyrning är tillgängliga:

| Funktion | Information |
|---|---|
| Åtkomstkontroller | Rollbaserad åtkomstkontroll och attributbaserad (fältnivåbaserad) åtkomstkontroll stöds. Mer information finns i [Åtkomstkontroller](access-controls.md). |
| Granskningsloggar | När användare skapar, uppdaterar eller tar bort specifika Mix Modeler-kategorier registrerar Experience Platform Audit-funktionen aktiviteten i granskningsloggarna. Mer information finns i [Granskningsloggar](audit-logs.md). |
| Policyer | Som en del av det harmoniserade arbetsflödet för data tillämpas Experience Platform-definierade regler. Överträdelser av dataanvändningsetiketter rapporteras och visas för användaren. Mer information finns i [Profiler](policies.md). |
| Kryptering | Alla datauppsättningar som används för indata och utdata av modeller följer Experience Platform riktlinjer. Experience Platform datakryptering gäller för data i vila och under överföring. |
| Datahygien | Alla datauppsättningar som används för indata och ut-modeller följer Experience Platform riktlinjer. Experience Platform tillhandahåller en uppsättning verktyg för att hantera kundens datalängd, inklusive stöd för olika typer av utgångsdatum. När du tar bort en källdatauppsättning från Experience Platform, som används som en del av dina harmoniserade data, meddelas du. Mer information finns i [Datauppsättningsregler](/help/harmonize-data/dataset-rules.md). |
| Kundhanterade nycklar | När du har licensierat Mix Modeler med tillägget Privacy Security Shield eller Healthcare Shield kan du använda funktionen Customer Managed Keys för att utnyttja Azure Key Vault för att få egna nycklar via API:er. Ni har fullständig hantering av data som bearbetas i Mix Modeler. |
