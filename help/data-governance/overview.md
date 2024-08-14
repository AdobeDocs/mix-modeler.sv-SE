---
title: Datastyrning
description: Lär dig hur du använder de tjänster och verktyg från Experience Platform som gör att du kan kontrollera dina insamlade upplevelsedata. Så att ni följer era rutiner, juridiska skyldigheter och utvecklingsprocesser.
feature: Administration
source-git-commit: 6776a91563f120db1341adef923aab4b0f582c9d
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 0%

---

# Datastyrning

Integrationen mellan Mix Modeler och Experience Platform ger Mix Modeler möjlighet att utnyttja de inneboende funktionerna för datastyrning i Experience Platform. I det här avsnittet av dokumentationen beskrivs detaljerna för de funktioner för datastyrning som finns i Mix Modeler.

Med Experience Platform Data Governance kan ni styra och förstå data under hela den resa som data tar genom Experience Platform. Den här resan innebär att upprätthålla datakvalitet, datalinje, datakatalogisering och mycket annat.

Etiketter och profiler för dataanvändning som skapas på datauppsättningar som förbrukas av Experience Platform i Mix Modeler, där så är lämpligt. Dessa etiketter stoppar eller varnar till exempel användare när de tar bort datauppsättningar som ingår i en datauppsättningsregel i harmoniserade data. Eller dölj schemafält som är begränsade för användare när en datauppsättningsregel skapas.

Tack vare integreringen av datastyrning kan ni hantera regelefterlevnaden effektivare. Datahanteringen i organisationen kan ange regler som begränsar användningen. Det innebär att du kan använda data som överensstämmer med policyer som definieras av data stewards. Läs dokumentationen om [Etiketter och profiler](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/data-governance) om du vill veta mer.

Följande funktioner för datastyrning är tillgängliga:

| Funktion | Information |
|---|---|
| Åtkomstkontroller | Rollbaserad åtkomstkontroll och attributbaserad (fältnivåbaserad) åtkomstkontroll stöds. Mer information finns i [Åtkomstkontroller](access-controls.md). |
| Granskningsloggar | När användare skapar, uppdaterar eller tar bort specifika Mix Modeler-kategorier registrerar funktionen Experience Platform Audit aktiviteten i granskningsloggarna. Mer information finns i [Granskningsloggar](audit-logs.md). |
| Policyer | Som en del av det harmoniserade arbetsflödet för data tillämpas policyer som definieras av Experience Platform. Överträdelser av dataanvändningsetiketter rapporteras och visas för användaren. Mer information finns i [Profiler](policies.md). |
| Kryptering | Alla datauppsättningar som används för indata och utdata för modeller följer riktlinjerna för Experience Platform. Experience Platform datakryptering gäller för data i vila och under överföring. |
| Datahygien | Alla datauppsättningar som används för indata och ut-modeller följer riktlinjerna för Experience Platform. Experience Platform tillhandahåller en uppsättning verktyg för att hantera kundens datalängd, inklusive stöd för olika typer av utgångsdatum. När du tar bort en källdatauppsättning från Experience Platform, som används som en del av dina harmoniserade data, meddelas du. Mer information finns i [Datauppsättningsregler](/help/harmonize-data/dataset-rules.md). |
| Kundhanterade nycklar | När du har licensierat Mix Modeler med tillägget Privacy Security Shield eller Healthcare Shield kan du använda funktionen Customer Managed Keys för att utnyttja Azure Key Vault för att ta med dina egna nycklar via API:er. Ni har fullständig hantering av data som bearbetas i modeller i Mix Modeler. |
