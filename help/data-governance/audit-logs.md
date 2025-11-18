---
title: Granskningsloggar
description: Lär dig hur du får åtkomst till granskningsloggar från Mix Modeler.
feature: Administration
exl-id: aa65aac5-bea4-43ff-b0d0-9e8a6a97d3ca
source-git-commit: 1a9df9f9819d9e0031e58443ec6a9e755a151ba0
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 1%

---

# Granskningsloggar

För att öka insynen i och synligheten för aktiviteter som utförs i systemet, hämtas användaraktiviteter i Mix Modeler-arbetsflödet in i Experience Platform granskningsloggar för att förstå användardrivna ändringar i Mix Modeler-kategorier. Loggarna utgör en verifieringskedja som kan hjälpa dig med felsökningsproblem och som kan hjälpa ditt företag att effektivt följa företagets policyer för datahantering och lagstadgade krav.

<!-- DO WE HAVE TO ADD THIS
If you are subject to the Health Insurance Portability and Accountability Act (HIPAA) and create, receive, maintain, or transmit permitted sensitive personal data through Mix Modeler, you are responsible for executing a BAA with Adobe and licensing Healthcare Shield.
-->

En granskningslogg informerar vem som utförde vilken åtgärd och när. Varje åtgärd som registreras i en logg innehåller metadata som anger åtgärdstyp, datum och tid, e-post-ID för användaren som utförde åtgärden samt ytterligare attribut som är relevanta för åtgärdstypen. Den spårar de åtgärder som användare i Mix Modeler utför för att skapa, uppdatera och ta bort.

Så här inspekterar du granskningsloggen i Mix Modeler-gränssnittet:

1. Välj ![Uppgiftslista](/help/assets/icons/TaskList.svg) **[!UICONTROL Audits]** från **[!UICONTROL PRIVACY]**.

1. I **[!UICONTROL Audits]** hittar du **[!UICONTROL Activity log]**. I aktivitetsloggen visas poster för följande Mix Modeler-kategorier, åtgärder och status.

   | Kategori | Åtgärd | Status |
   |---|---|---|
   | Mix Modeler-datauppsättningsregel | Skapa | Tillåt eller Neka |
   | Mix Modeler-datauppsättningsregel | Uppdatering | Tillåt eller Neka |
   | Mix Modeler-datauppsättningsregel | Ta bort | Tillåt eller Neka |
   | Mix Modeler Field | Skapa | Tillåt eller Neka |
   | Mix Modeler Field | Uppdatering | Tillåt eller Neka |
   | Mix Modeler Field | Ta bort | Tillåt eller Neka |
   | Mix Modeler Marketing Touchpoint | Skapa | Tillåt eller Neka |
   | Mix Modeler Marketing Touchpoint | Uppdatering | Tillåt eller Neka |
   | Mix Modeler Marketing Touchpoint | Ta bort | Tillåt eller Neka |
   | Mix Modeler Conversion | Skapa | Tillåt eller Neka |
   | Mix Modeler Conversion | Uppdatering | Tillåt eller Neka |
   | Mix Modeler Conversion | Ta bort | Tillåt eller Neka |
   | Mix Modeler Model | Skapa | Tillåt eller Neka |
   | Mix Modeler Model | Uppdatering | Tillåt eller Neka |
   | Mix Modeler Model | Ta bort | Tillåt eller Neka |
   | Mix Modeler Model | Rescore | Tillåt eller Neka |
   | Mix Modeler Model | Klona | Tillåt eller Neka |
   | Mix Modeler Model | Tåg/regn | Tillåt eller Neka |
   | Mix Modeler Model | Hämta/spara metadata | Tillåt eller Neka |
   | Mix Modeler Plan | Skapa | Tillåt eller Neka |
   | Mix Modeler Plan | Uppdatering | Tillåt eller Neka |
   | Mix Modeler Plan | Ändra associerad modell | Tillåt eller Neka |
   | Mix Modeler Data Harmonization | Utlösarsynkronisering | Tillåt eller Neka |


1. Välj en post i aktivitetsloggen om du vill öppna en panel med mer information.

   ![Mix Modeler Audit](/help/assets/mix-modeler-audit.png)

1. Om du vill filtrera på intervallet **[!UICONTROL Category]**, **[!UICONTROL Action]**, **[!UICONTROL Request ID]**, **[!UICONTROL User]**, **[!UICONTROL Status]** eller **[!UICONTROL Date]** väljer du ![Filter](/help/assets/icons/Filter.svg).

1. Om du vill ändra kolumnerna som visas i aktivitetsloggen väljer du ![Kolumner](/help/assets/icons/ColumnSetting.svg) och markerar de kolumner som ska visas i dialogrutan **[!UICONTROL Customize table]**. Välj **[!UICONTROL Apply]** om du vill använda markeringen, **[!UICONTROL Cancel]** om du vill avbryta markeringen.

1. Om du vill hämta granskningsloggen väljer du ![Hämta](/help/assets/icons/Download.svg) **[!UICONTROL Download log]**. I dialogrutan **[!UICONTROL Download log]** väljer du antingen **[!UICONTROL CSV]** eller **[!UICONTROL JSON]** som format och väljer **[!UICONTROL Download]**.

## Åtkomst till granskningsloggar

När funktionen är aktiverad för din organisation samlas granskningsloggarna automatiskt in när aktiviteten inträffar. Du behöver inte aktivera granskningsloggen manuellt.

Om du vill visa och exportera granskningsloggar måste du ha beviljats åtkomstkontrollbehörighet för granskningsloggar. Mer information om hur du hanterar enskilda behörigheter för Mix Modeler-funktioner finns i [åtkomstkontrollsdokumentationen](https://experienceleague.adobe.com/sv/docs/experience-platform/access-control/home).
