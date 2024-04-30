---
title: Administrering
description: Lär dig hur du administrerar Mix Modeler.
feature: Administration
exl-id: 76d6d15d-a838-4ee2-9929-e55ea8946b80
source-git-commit: 51a4bc6557422a281fa03d49877cb378d14314e2
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 2%

---

# Administrering

Använd [Adobe Admin Console](https://helpx.adobe.com/se/enterprise/using/admin-console.html) för att hantera Mix Modeler-produkter och -användare.

För att Mix Modeler ska fungera på rätt sätt måste du ange rätt behörigheter.

I Adobe Experience Cloud-gränssnittet:

1. Välj **[!UICONTROL Permissions]** från den vänstra listen, under **[!UICONTROL ADMINISTRATION]**.

1. Välj ![Person](assets/icons/User.svg) **[!UICONTROL Roles]** från den vänstra panelen.

1. Välj en befintlig roll eller skapa en roll med **[!UICONTROL Create role]** (till exempel **Mix Modeler**). Om du väljer en befintlig roll väljer du ![Redigera](assets/icons/Edit.svg) **[!UICONTROL Edit]** om du vill redigera rollens behörigheter. Se [Hantera roller](https://helpx.adobe.com/se/enterprise/using/admin-console.html) för mer information.

1. Kontrollera att du har valt en eller flera sandlådor för rollen.

1. Lägg till **Adobe Mix Modeler** resurs i listan över resurser för rollen.

1. Se till att du väljer rätt **[!UICONTROL Adobe Mix Modeler]** behörigheter för rollen som du konfigurerar. Du kan välja en eller flera av följande roller:

   - **[!UICONTROL View Adobe Mix Modeler Harmonized Data]**
   - **[!UICONTROL Manage Adobe Mix Modeler Harmonized Data]**
   - **[!UICONTROL View Adobe Mix Modeler Models Configuration]**
   - **[!UICONTROL Manage Adobe Mix Modeler Models Configuration]**
   - **[!UICONTROL View Adobe Mix Modeler Plans Configuration]**
   - **[!UICONTROL Manage Adobe Mix Modeler Plans Configuration]**

     ![Mix Modeler RBAC](assets/mix-modeler-rbac.png)


1. Se till att du väljer ytterligare behörigheter för rollen. Om du till exempel vill visa eller hantera datauppsättningar och scheman väljer du:

   - **[!UICONTROL Data Management]**: välj de relevanta alternativen: **[!UICONTROL View Datasets]** eller **[!UICONTROL Manage Datasets]**.

   - **[!UICONTROL Data Modeling]**: välj de relevanta alternativen: **[!UICONTROL Manage Schemas]** eller **[!UICONTROL View Schemas]**.

   <!--
    * **[!UICONTROL Data Governance]**: ensure you select **[!UICONTROL View User Activity Log]** and **[!UICONTROL View Data Usage Policies]**.
    -->

   <!--![Permissions](assets/permissions-including-privacy.png)-->

   Välj **[!UICONTROL Save]** för att spara behörigheterna.

1. I **[!UICONTROL Details]** inom **[!UICONTROL Role]**, lägg till lämpliga **[!UICONTROL Users]** eller **[!UICONTROL User groups]** för att ge användare tillgång till Mix Modeler.
