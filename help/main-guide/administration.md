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

Verwenden Sie die [Adobe Admin ConsoleMix Modeler ](https://helpx.adobe.com/de/enterprise/using/admin-console.html), um Benutzerprodukte und -benutzer zu verwalten.

Damit Mix Modeler ordnungsgemäß funktioniert, müssen Sie die richtigen Berechtigungen festlegen.

In der Adobe Experience Cloud-Benutzeroberfläche:

1. Wählen Sie **[!UICONTROL Permissions]** in der linken Leiste unter **[!UICONTROL ADMINISTRATION]** aus.

1. Wählen Sie ![ linken Bedienfeld ](/help/assets/icons/User.svg)Benutzer **[!UICONTROL Roles]** aus.

1. Wählen Sie eine vorhandene Rolle aus oder erstellen Sie eine Rolle mithilfe von **[!UICONTROL Create role]** (z. B. **Mix Modeler**) Wenn Sie eine vorhandene Rolle auswählen, klicken Sie auf ![Bearbeiten](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]**, um die Berechtigungen für die Rolle zu bearbeiten. Weitere Informationen finden [ unter ](https://helpx.adobe.com/de/enterprise/using/admin-console.html) von Rollen .

1. Stellen Sie sicher, dass Sie eine oder mehrere Sandboxes für die Rolle ausgewählt haben.

1. Fügen Sie die Ressource **0&rbrace;Adobe Mix Modeler&quot; zur Liste der Ressourcen für die Rolle hinzu.**

1. Stellen Sie sicher, dass Sie die richtigen **[!UICONTROL Adobe Mix Modeler]** für die Rolle auswählen, die Sie konfigurieren. Sie können eine oder mehrere der folgenden Rollen auswählen:

   - **[!UICONTROL View Adobe Mix Modeler Harmonized Data]**
   - **[!UICONTROL Manage Adobe Mix Modeler Harmonized Data]**
   - **[!UICONTROL View Adobe Mix Modeler Models Configuration]**
   - **[!UICONTROL Manage Adobe Mix Modeler Models Configuration]**
   - **[!UICONTROL View Adobe Mix Modeler Plans Configuration]**
   - **[!UICONTROL Manage Adobe Mix Modeler Plans Configuration]**

     ![Mix Modeler-RBAC](/help/assets/mix-modeler-rbac.png)


1. Stellen Sie sicher, dass Sie zusätzliche Berechtigungen für die Rolle auswählen. Um beispielsweise Datensätze und Schemata anzuzeigen oder zu verwalten, wählen Sie:

   - **[!UICONTROL Data Management]**: Wählen Sie die entsprechenden Optionen aus: **[!UICONTROL View Datasets]** oder **[!UICONTROL Manage Datasets]**.

   - **[!UICONTROL Data Modeling]**: Wählen Sie die entsprechenden Optionen aus: **[!UICONTROL Manage Schemas]** oder **[!UICONTROL View Schemas]**.

   <!--
    * **[!UICONTROL Data Governance]**: ensure you select **[!UICONTROL View User Activity Log]** and **[!UICONTROL View Data Usage Policies]**.
    -->

   <!--![Permissions](assets/permissions-including-privacy.png)-->

   Wählen Sie **[!UICONTROL Save]** aus, um die Berechtigungen zu speichern.

1. Fügen Sie in **[!UICONTROL Details]** in **[!UICONTROL Role]** die entsprechenden **[!UICONTROL Users]** oder **[!UICONTROL User groups]** hinzu, um Benutzenden Zugriff auf Mix Modeler zu gewähren.
