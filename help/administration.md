---
title: Pläne vergleichen
description: Erfahren Sie, wie Sie Pläne im Adobe Mix Model vergleichen.
source-git-commit: 1eaebc6f6178270a9e8aebb6b250e0b0a6289f52
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 7%

---


# Administration

Verwenden Sie die [Adobe Admin Console](https://helpx.adobe.com/de/enterprise/using/admin-console.html) um Adobe Mix Modeler-Produkte und -Benutzer zu verwalten.

Damit Adobe Mix Modeler ordnungsgemäß funktioniert, müssen Sie die richtigen Berechtigungen festlegen.

In der Adobe Experience Cloud-Benutzeroberfläche

1. Auswählen **[!UICONTROL Permissions]** von der linken Leiste unter **[!UICONTROL ADMINISTRATION]**.

1. Auswählen ![Person](assets/icons/User.svg) **[!UICONTROL Roles]** aus dem linken Bereich.

1. Wählen Sie eine vorhandene Rolle aus oder erstellen Sie eine Rolle mithilfe von **[!UICONTROL Create role]**. Wenn Sie eine vorhandene Rolle ausgewählt haben, wählen Sie ![Bearbeiten](assets/icons/Edit.svg) **[!UICONTROL Edit]** um die Berechtigungen für die Rolle zu bearbeiten. Siehe [Rollen verwalten](https://helpx.adobe.com/de/enterprise/using/admin-console.html) für weitere Informationen.

1. Stellen Sie sicher, dass Sie die folgenden Berechtigungen für die Rolle auswählen:

   * **[!UICONTROL Sandboxes]**: Wählen Sie mindestens eine Sandbox aus.

   * **[!UICONTROL Data Management]**: Stellen Sie sicher, dass Sie die Optionen auswählen **[!UICONTROL View Datasets]** und **[!UICONTROL Manage Datasets]**.

   * **[!UICONTROL Data Modeling]**: Stellen Sie sicher, dass Sie die Optionen auswählen **[!UICONTROL Manage Schemas]** und **[!UICONTROL View Schemas]**.

   * **[!UICONTROL Destinations]**: Wählen Sie **[!UICONTROL Manage and Activate Dataset Destination]**, **[!UICONTROL Destination Authoring]**, **[!UICONTROL Activate Destinations]** und **[!UICONTROL View Destinations]**.

   * **[!UICONTROL Data Ingestion]**: Wählen Sie **[!UICONTROL View Sources]** und **[!UICONTROL Manage Sources]**.

   Die für die Rolle eingerichteten Berechtigungen sollten wie folgt aussehen:

   ![Berechtigungen](assets/permissions.png)

   Auswählen **[!UICONTROL Save]** , um die Berechtigungen zu speichern.

1. In **[!UICONTROL Details]** Innerhalb **[!UICONTROL Role]**, fügen Sie die entsprechenden hinzu **[!UICONTROL Users]** und/oder **[!UICONTROL User groups]** , um Benutzern Zugriff auf Adobe Mix Modeler zu gewähren.
