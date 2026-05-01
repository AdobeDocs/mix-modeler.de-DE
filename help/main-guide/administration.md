---
title: Administration
description: Erfahren Sie, wie Sie Mix Modeler verwalten.
feature: Administration
exl-id: 76d6d15d-a838-4ee2-9929-e55ea8946b80
TQID: https://experienceleague.adobe.com/0MxMv6Due-i9-8JxKTb3vk2NDZ5mc6Pj4yEe-liCszg
autotag-review: '2026-05-01T09:07:55.299Z'
product_v2: id: b88c80e3-31df-4609-989d-d4dac0e6d973
feature_v2: id: fe2edbb1-46f9-4347-a27c-577cab3640cb
subfeature_v2: id: abe9e290-7d2f-4131-b71e-ef9900865044id: a6da0571-746e-4d59-89a4-7b691b1c3b9a
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b23e006f-0a29-4f1d-8fd0-77aa56f3d12bid: ebde5b41-29c9-4f5e-9ef6-1197e85409e3id: eddd9b14-83bd-4ff4-9072-54a4a484abb7id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 5579087b9381c4d8e909ed5fe3099fd42d5c6799
workflow-type: tm+mt
source-wordcount: 194
ht-degree: 7%

---

# Administration

Verwenden Sie die [Adobe Admin Console](https://helpx.adobe.com/de/enterprise/using/admin-console.html), um Mix Modeler-Produkte und -Benutzer zu verwalten.

Damit Mix Modeler ordnungsgemäß funktioniert, müssen Sie die richtigen Berechtigungen festlegen.

In der Adobe Experience Cloud-Benutzeroberfläche:

1. Wählen Sie **[!UICONTROL Permissions]** in der linken Leiste unter **[!UICONTROL ADMINISTRATION]** aus.

1. Wählen Sie ![ linken Bedienfeld ](/help/assets/icons/User.svg)Benutzer **[!UICONTROL Roles]** aus.

1. Wählen Sie eine vorhandene Rolle aus oder erstellen Sie eine Rolle mithilfe von **[!UICONTROL Create role]** (z. B. **Mix Modeler**) Wenn Sie eine vorhandene Rolle auswählen, klicken Sie auf ![Bearbeiten](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]**, um die Berechtigungen für die Rolle zu bearbeiten. Weitere Informationen finden [ unter ](https://helpx.adobe.com/de/enterprise/using/admin-console.html) von Rollen .

1. Stellen Sie sicher, dass Sie eine oder mehrere Sandboxes für die Rolle ausgewählt haben.

1. Fügen Sie die **Adobe Mix Modeler**-Ressource zur Liste der Ressourcen für die Rolle hinzu.

1. Stellen Sie sicher, dass Sie die richtigen **[!UICONTROL Adobe Mix Modeler]** für die Rolle auswählen, die Sie konfigurieren. Sie können eine oder mehrere der folgenden Rollen auswählen:

   - **[!UICONTROL View Adobe Mix Modeler Harmonized Data]**
   - **[!UICONTROL Manage Adobe Mix Modeler Harmonized Data]**
   - **[!UICONTROL View Adobe Mix Modeler Models Configuration]**
   - **[!UICONTROL Manage Adobe Mix Modeler Models Configuration]**
   - **[!UICONTROL View Adobe Mix Modeler Plans Configuration]**
   - **[!UICONTROL Manage Adobe Mix Modeler Plans Configuration]**

     ![Mix Modeler RBAC](/help/assets/mix-modeler-rbac.png)


1. Stellen Sie sicher, dass Sie zusätzliche Berechtigungen für die Rolle auswählen. Um beispielsweise Datensätze und Schemata anzuzeigen oder zu verwalten, wählen Sie:

   - **[!UICONTROL Data Management]**: Wählen Sie die entsprechenden Optionen aus: **[!UICONTROL View Datasets]** oder **[!UICONTROL Manage Datasets]**.

   - **[!UICONTROL Data Modeling]**: Wählen Sie die entsprechenden Optionen aus: **[!UICONTROL Manage Schemas]** oder **[!UICONTROL View Schemas]**.

   <!--
    * **[!UICONTROL Data Governance]**: ensure you select **[!UICONTROL View User Activity Log]** and **[!UICONTROL View Data Usage Policies]**.
    -->

   <!--![Permissions](assets/permissions-including-privacy.png)-->

   Wählen Sie **[!UICONTROL Save]** aus, um die Berechtigungen zu speichern.

1. Fügen Sie in **[!UICONTROL Details]** in **[!UICONTROL Role]** die entsprechenden **[!UICONTROL Users]** oder **[!UICONTROL User groups]** hinzu, um Benutzenden Zugriff auf Mix Modeler zu gewähren.
