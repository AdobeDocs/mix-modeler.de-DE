---
title: Administration
description: Erfahren Sie, wie Sie Mix Modeler verwalten.
feature: Administration
exl-id: 76d6d15d-a838-4ee2-9929-e55ea8946b80
source-git-commit: 4d84c93121fc476cc6610ad572bab161bbacfc23
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 2%

---

# Administration

Verwenden Sie den [Adobe Admin Console](https://helpx.adobe.com/de/enterprise/using/admin-console.html), um Mix Modeler und Benutzer zu verwalten.

Damit Mix Modeler ordnungsgemäß funktioniert, müssen Sie die richtigen Berechtigungen festlegen.

In der Adobe Experience Cloud-Benutzeroberfläche:

1. Wählen Sie in der linken Leiste unter **[!UICONTROL ADMINISTRATION]** die Option &quot;**[!UICONTROL Permissions]**&quot;.

1. Wählen Sie im linken Bereich ![Benutzer](/help/assets/icons/User.svg) **[!UICONTROL Roles]** aus.

1. Wählen Sie eine vorhandene Rolle aus oder erstellen Sie eine Rolle mit **[!UICONTROL Create role]** (z. B. **Mix Modeler**). Wenn Sie eine vorhandene Rolle auswählen, wählen Sie ![Bearbeiten](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]** aus, um die Berechtigungen für die Rolle zu bearbeiten. Weitere Informationen finden Sie unter [Rollen verwalten](https://helpx.adobe.com/de/enterprise/using/admin-console.html) .

1. Stellen Sie sicher, dass Sie eine oder mehrere Sandboxes für die Rolle ausgewählt haben.

1. Fügen Sie die Ressource **Adobe Mix Modeler** zur Liste der Ressourcen für die Rolle hinzu.

1. Stellen Sie sicher, dass Sie die richtigen **[!UICONTROL Adobe Mix Modeler]** -Berechtigungen für die Rolle auswählen, die Sie konfigurieren. Sie können eine oder mehrere der folgenden Rollen auswählen:

   - **[!UICONTROL View Adobe Mix Modeler Harmonized Data]**
   - **[!UICONTROL Manage Adobe Mix Modeler Harmonized Data]**
   - **[!UICONTROL View Adobe Mix Modeler Models Configuration]**
   - **[!UICONTROL Manage Adobe Mix Modeler Models Configuration]**
   - **[!UICONTROL View Adobe Mix Modeler Plans Configuration]**
   - **[!UICONTROL Manage Adobe Mix Modeler Plans Configuration]**

     ![Mix Modeler RBAC](/help/assets/mix-modeler-rbac.png)


1. Stellen Sie sicher, dass Sie zusätzliche Berechtigungen für die Rolle auswählen. Um beispielsweise Datensätze und Schemas anzuzeigen oder zu verwalten, wählen Sie Folgendes aus:

   - **[!UICONTROL Data Management]**: Wählen Sie die entsprechenden Optionen aus: **[!UICONTROL View Datasets]** oder **[!UICONTROL Manage Datasets]**.

   - **[!UICONTROL Data Modeling]**: Wählen Sie die entsprechenden Optionen aus: **[!UICONTROL Manage Schemas]** oder **[!UICONTROL View Schemas]**.

   <!--
    * **[!UICONTROL Data Governance]**: ensure you select **[!UICONTROL View User Activity Log]** and **[!UICONTROL View Data Usage Policies]**.
    -->

   <!--![Permissions](assets/permissions-including-privacy.png)-->

   Wählen Sie **[!UICONTROL Save]** aus, um die Berechtigungen zu speichern.

1. Fügen Sie in **[!UICONTROL Details]** innerhalb von **[!UICONTROL Role]** die entsprechenden **[!UICONTROL Users]** oder **[!UICONTROL User groups]** hinzu, um Benutzern Zugriff auf Mix Modeler zu gewähren.
