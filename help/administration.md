---
title: Administrering
description: Lär dig hur du administrerar Adobe Mix Modeler.
source-git-commit: b5b277e3476bdf6c0c0da85425bba19bea00c594
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 7%

---


# Administrering

Använd [Adobe Admin Console](https://helpx.adobe.com/se/enterprise/using/admin-console.html) för att hantera Adobe Mix Modeler-produkter och -användare.

För att Adobe Mix Modeler ska fungera på rätt sätt måste du ange rätt behörigheter.

I Adobe Experience Cloud-gränssnittet

1. Välj **[!UICONTROL Permissions]** från den vänstra listen, under **[!UICONTROL ADMINISTRATION]**.

1. Välj ![Person](assets/icons/User.svg) **[!UICONTROL Roles]** från den vänstra panelen.

1. Välj en befintlig roll eller skapa en roll med **[!UICONTROL Create role]**. Om du väljer en befintlig roll väljer du ![Redigera](assets/icons/Edit.svg) **[!UICONTROL Edit]** om du vill redigera rollens behörigheter. Se [Hantera roller](https://helpx.adobe.com/se/enterprise/using/admin-console.html) för mer information.

1. Se till att du väljer följande behörigheter för rollen:

   * **[!UICONTROL Sandboxes]**: Välj minst en sandlåda.

   * **[!UICONTROL Data Management]**: se till att du väljer alternativ **[!UICONTROL View Datasets]** och **[!UICONTROL Manage Datasets]**.

   * **[!UICONTROL Data Modeling]**: se till att du väljer alternativ **[!UICONTROL Manage Schemas]** och **[!UICONTROL View Schemas]**.

   * **[!UICONTROL Destinations]**: se till att du väljer **[!UICONTROL Manage and Activate Dataset Destination]**, **[!UICONTROL Destination Authoring]**, **[!UICONTROL Activate Destinations]** och **[!UICONTROL View Destinations]**.

   * **[!UICONTROL Data Ingestion]**: se till att du väljer **[!UICONTROL View Sources]** och **[!UICONTROL Manage Sources]**.

   <!--
    * **[!UICONTROL Data Governance]**: ensure you select **[!UICONTROL View User Activity Log]** and **[!UICONTROL View Data Usage Policies]**.
    -->

   De behörigheter som har angetts för rollen ska se ut så här:

   ![Behörigheter](assets/permissions.png)

   <!--![Permissions](assets/permissions-including-privacy.png)-->

   Välj **[!UICONTROL Save]** för att spara behörigheterna.

1. I **[!UICONTROL Details]** inom **[!UICONTROL Role]**, lägg till lämpliga **[!UICONTROL Users]** och/eller **[!UICONTROL User groups]** för att ge användare tillgång till Adobe Mix Modeler.
