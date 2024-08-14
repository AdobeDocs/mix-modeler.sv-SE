---
title: Åtkomstkontroller
description: Lär dig hur du konfigurerar åtkomstkontroller i Mix Modeler.
feature: Administration
source-git-commit: 6776a91563f120db1341adef923aab4b0f582c9d
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

---

# Åtkomstkontroller

Åtkomstkontroll för Mix Modeler tillhandahålls via Experience Platform i [Adobe Admin Console](https://adminconsole.adobe.com/) och via [Permissions](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home#platform-permissions) i Experience Platform. Den här funktionen utnyttjar produktprofiler i Admin Console, som länkar användare med behörigheter och sandlådor.

Mer information om åtkomstkontroll finns i [Översikt över åtkomstkontroll](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home).

## Rollbaserad åtkomstkontroll

Se [Administration](../main-guide/administration.md) om hur du konfigurerar rollbaserade åtkomstbehörigheter för Mix Modeler-användare och användargrupper i Experience Platform.

## Attributbaserad åtkomstkontroll

[Attributbaserad åtkomstkontroll](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/overview) är en funktion hos Experience Platform som gör att administratörer kan styra åtkomsten till specifika objekt och/eller funktioner baserat på attribut. Attribut kan läggas till i ett objekt, t.ex. en etikett som lagts till i ett schemafält eller segment. En administratör definierar åtkomstprinciper som innehåller attribut för att hantera behörigheter för användaråtkomst.

Med den här funktionen kan du etikettera XDM-schemafält (Experience Data Model) med etiketter som definierar användningsområde för organisationen eller data. Samtidigt kan administratörer använda användar- och rolladministrationsgränssnittet för att definiera åtkomstprinciper i XDM-schemafält. Och hantera åtkomsten som ges till användare eller grupper av användare bättre (interna, externa eller externa användare). Dessutom gör attributbaserad åtkomstkontroll det möjligt för administratörer att hantera åtkomsten till specifika segment.

Genom attributbaserad åtkomstkontroll kan administratörer styra användarnas tillgång till både känsliga personuppgifter (SPD) och personligt identifierbar information (PII) i alla plattformsarbetsflöden och -resurser. Administratörer kan definiera användarroller som bara har åtkomst till specifika fält och data som motsvarar dessa fält.

När datauppsättningsregler konfigureras för harmoniserade datauppsättningar, tillämpas Experience Platform [attributbaserad åtkomstkontroll](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/overview) på fältnivå. Ett fält är begränsat när en etikett är kopplad till ett schemafält. Och en aktiv princip som nekar dig åtkomst till det fältet aktiveras. Resultatet blir:

* du inte ser de schemafält som är begränsade för dig när du skapar en datauppsättningsregel,
* du inte kan visa eller redigera mappningen av ett eller flera schemafält som är begränsade för dig. När du redigerar eller visar en datauppsättningsregel som innehåller sådana begränsade fält visas följande skärm.
  ![Åtgärden tillåts inte](/help/assets//action-not-permitted.png)

