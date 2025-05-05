---
title: Policyer
description: Lär dig hur du får åtkomst till profiler från Mix Modeler.
feature: Administration
exl-id: 4dba7c30-ad1e-4213-a2b0-afc55f2448a3
source-git-commit: 132dc18b84723358a7d65e2aaadd49cf1deb2dd8
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 1%

---

# Policyer

När du har gått igenom arbetsflödet för att skapa en modell och skicka in modellens konfiguration, kontrollerar [policytillämpning](https://experienceleague.adobe.com/sv/docs/experience-platform/data-governance/enforcement/overview#automatic-enforcement) om det finns några överträdelser. Om en principöverträdelse inträffar visas en portfölj som anger att en eller flera profiler har överträtts. Den här kontrollen är till för att säkerställa att datahanteringen och marknadsföringsåtgärderna i Experience Platform är kompatibla med dataanvändningspolicyer.

Som standard söker Mix Modeler efter överträdelser av Adobe-definierade policyer som är kopplade till följande etiketter och marknadsföringsåtgärder:

| Principnamn | Associerad etikett | Associerad marknadsföringsåtgärd |
|---|---|---|
| Begränsa användningsanalys och användarbaserad mätning | C8 | Analytics  |
| Begränsa datavetenskap | C9 | Datavetenskap |
| Begränsa dataexport | C12 | Dataexport |

Överträdelser kontrolleras också för de policyer som du har definierat själv och som innehåller alla marknadsföringsåtgärder som listas i tabellen ovan.

När du bryter mot en princip när du skapar en datauppsättningsregel visas en portfölj som visar information om policyöverträdelsen.

Exempel:

- du har aktiverat principen [!UICONTROL Restrict data science] med den associerade etiketten [!UICONTROL C9] och den associerade marknadsföringsåtgärden [!UICONTROL Data Science],
- du har använt etiketten [!UICONTROL C9] - [!UICONTROL No data science] på fältet `totalCost` i konverteringsdataramodemet,
- du vill konfigurera en datauppsättningsregel som bland annat mappar fältet `totalCost` i konverteringsdatarammet till det harmoniserade fältet med namnet `spend` (och visningsnamnet `Spend`).

När du vill spara datauppsättningsregeln visas ett **[!UICONTROL Data governance policy violation detected]**-popup-fönster med en lista över profiler som har överträtts. När du väljer principnamn i [!UICONTROL Violation summary] visas en lista över [!UICONTROL Active data governance labels] som innehåller [!UICONTROL Entity], [!UICONTROL Type], [!UICONTROL Field] och [!UICONTROL Government labels] som används.

<!-- pending screenshot -->

När du använder en dataanvändningsetikett på ett schemafält som redan används i harmoniserade data, visas en portfölj som visar information om policyöverträdelsen.

Exempel:

- du har konfigurerat datauppsättningsregel som bland annat mappar fältet `totalCost` i konverteringsdatarammet till det harmoniserade fältet med namnet `spend` (och visningsnamnet `Spend`).
- du har synkroniserat harmoniserade data minst en gång (se [Datauppsättningsregler - Synkronisera data](/help/harmonize-data/dataset-rules.md#sync-data)).
- du aktiverar principen [!UICONTROL Restrict data science] med den associerade etiketten [!UICONTROL C9] och den associerade marknadsföringsåtgärden [!UICONTROL Data Science],
- du vill använda etiketten [!UICONTROL C9] - [!UICONTROL No data science] i fältet `totalCost` i konverteringsdataramodet.

När du vill spara schemauppdateringen visas ett **[!UICONTROL Data governance policy violation detected]**-popup-fönster med en lista över profiler som har överträtts. Välj principnamnet i [!UICONTROL Violation summary] om du vill ha mer information i listan [!UICONTROL Data Lineage].

<!-- pending screenshot -->

## Brott mot påvisade poseringar

De upptäckta pobjekten för brott mot datahanteringsprincipen ger specifik information om överträdelsen. Du kan lösa dessa överträdelser med hjälp av principinställningar och andra åtgärder som inte är direkt relaterade till konfigurationsarbetsflödet. Du kan till exempel ändra etiketterna så att vissa fält kan användas i datavetenskapliga syften. Du kan också ändra själva modellkonfigurationen så att modellen inte använder ett objekt med en dataanvändningsetikett.

Markeringen ![Sekretess](/help/assets/icons/Privacy.svg) **[!UICONTROL Policies]** i den vänstra listen ger åtkomst till gränssnittet [!UICONTROL Policies] i Experience Platform, vilket gör att du kan hantera principer, etiketter och marknadsföringsåtgärder.

<!--
Currently,  Mix Modeler does not support all of the data governance functionality offered by Experience Platform. Field level access control is supported. See [Field level access control](../harmonize-data/dataset-rules.md#field-level-access-control)
-->

>[!MORELIKETHIS]
>
>[Översikt över dataanvändningsprinciper](https://experienceleague.adobe.com/sv/docs/experience-platform/data-governance/policies/overview)
>
>

