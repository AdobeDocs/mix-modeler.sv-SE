---
title: Granskning
description: Lär dig hur du granskar Mix Modeler.
feature: Administration
exl-id: 76d6d15d-a838-4ee2-9929-e55ea8946b80
source-git-commit: b8435c46276be9d0755049a502ba029b0983cb72
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 0%

---

# Granskning

>[!AVAILABILITY]
>
>Funktionerna som beskrivs i den här artikeln är i den begränsade testfasen av releasen och är kanske inte tillgängliga än i din miljö. Den här anteckningen tas bort när funktionen är allmänt tillgänglig. Mer information om de senaste Mix Modeler-versionerna finns i [Mix Modeler](/help/releases/latest.md).

Du kan granska vad användare gör i Mix Modeler med granskningsgränssnittet i Experience Platform och inbäddat i användargränssnittet i Mix Modeler.

Så här inspekterar du granskningsloggen i Mix Modeler-gränssnittet:

1. Välj ![Uppgiftslista](../assets/icons/TaskList.svg) **[!UICONTROL Audits]** från **[!UICONTROL PRIVACY]**.

1. I **[!UICONTROL Audits]** du hittar **[!UICONTROL Activity log]**. I aktivitetsloggen visas poster för följande Mix Modeler-kategorier, åtgärder och status.

   | Kategori | Åtgärd | Status |
   |---|---|---|
   | Mix Modeler datauppsättningsregel | Skapa | Tillåt eller neka |
   | Mix Modeler datauppsättningsregel | Uppdatera | Tillåt eller neka |
   | Mix Modeler datauppsättningsregel | Ta bort | Tillåt eller neka |
   | Mix Modeler | Skapa | Tillåt eller neka |
   | Mix Modeler | Uppdatera | Tillåt eller neka |
   | Mix Modeler | Ta bort | Tillåt eller neka |
   | Mix Modeler Marketing Touch Point | Skapa | Tillåt eller neka |
   | Mix Modeler Marketing Touch Point | Uppdatera | Tillåt eller neka |
   | Mix Modeler Marketing Touch Point | Ta bort | Tillåt eller neka |
   | Konvertering av Mix Modeler | Skapa | Tillåt eller neka |
   | Konvertering av Mix Modeler | Uppdatera | Tillåt eller neka |
   | Konvertering av Mix Modeler | Ta bort | Tillåt eller neka |
   | Mix Modeler Model | Skapa | Tillåt eller neka |
   | Mix Modeler Model | Uppdatera | Tillåt eller neka |
   | Mix Modeler Model | Ta bort | Tillåt eller neka |

1. Välj en post i aktivitetsloggen om du vill öppna en panel med mer information.

   ![Mix Modeler granskning](../assets/mix-modeler-audit.png)

1. Filtrera på **[!UICONTROL Category]**, **[!UICONTROL Action]**, **[!UICONTROL Request ID]**, **[!UICONTROL User]**, **[!UICONTROL Status]** eller **[!UICONTROL Date]** område, markera ![Filter](../assets/icons/Filter.svg).

1. Om du vill ändra kolumnerna som visas i aktivitetsloggen väljer du ![Kolumner](../assets/icons/ColumnSetting.svg) och i **[!UICONTROL Customize table]** markerar de kolumner som ska visas. Välj **[!UICONTROL Apply]** för att använda markeringen, **[!UICONTROL Cancel]** om du vill avbryta markeringen.

1. Om du vill hämta granskningsloggen väljer du ![Ladda ned](../assets/icons/Download.svg) **[!UICONTROL Download log]**. I **[!UICONTROL Download log]** välj antingen **[!UICONTROL CSV]** eller **[!UICONTROL JSON]** som format och välj **[!UICONTROL Download]**.
