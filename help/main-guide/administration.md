---
title: Administration
description: Erfahren Sie, wie Sie Mix Modeler verwalten.
feature: Administration
exl-id: 76d6d15d-a838-4ee2-9929-e55ea8946b80
source-git-commit: 995f15b6d2dd99d5304a4cda7b1fa5f8a1d00023
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---

# Administration

Verwenden Sie die [Adobe Admin Console](https://helpx.adobe.com/de/enterprise/using/admin-console.html) um Mix Modeler-Produkte und -Benutzer zu verwalten.

Damit Mix Modeler ordnungsgemäß funktioniert, müssen Sie die richtigen Berechtigungen festlegen.

In der Adobe Experience Cloud-Benutzeroberfläche:

1. Auswählen **[!UICONTROL Permissions]** von der linken Leiste unter **[!UICONTROL ADMINISTRATION]**.

1. Auswählen {{user}} **[!UICONTROL Roles]** aus dem linken Bereich.

1. Wählen Sie eine vorhandene Rolle aus oder erstellen Sie eine Rolle mithilfe von **[!UICONTROL Create role]** (zum Beispiel: **Mix Modeler**). Wenn Sie eine vorhandene Rolle auswählen, wählen Sie {{edit}} **[!UICONTROL Edit]** um die Berechtigungen für die Rolle zu bearbeiten. Siehe [Rollen verwalten](https://helpx.adobe.com/de/enterprise/using/admin-console.html) für weitere Informationen.

1. Stellen Sie sicher, dass Sie eine oder mehrere Sandboxes für die Rolle ausgewählt haben.

1. Fügen Sie die **Adobe Mix Modeler** Ressource in die Liste der Ressourcen für die Rolle.

1. Stellen Sie sicher, dass Sie die richtige **[!UICONTROL Adobe Mix Modeler]** -Berechtigungen für die Rolle, die Sie konfigurieren. Sie können eine oder mehrere der folgenden Rollen auswählen:

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

   Auswählen **[!UICONTROL Save]** , um die Berechtigungen zu speichern.

1. In **[!UICONTROL Details]** Innerhalb **[!UICONTROL Role]**, fügen Sie die entsprechenden hinzu **[!UICONTROL Users]** oder **[!UICONTROL User groups]** , um Benutzern Zugriff auf Mix Modeler zu gewähren.
