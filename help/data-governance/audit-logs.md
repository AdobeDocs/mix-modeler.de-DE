---
title: Audit-Protokolle
description: Erfahren Sie, wie Sie von Mix Modeler aus auf Auditprotokolle zugreifen können.
feature: Administration
exl-id: aa65aac5-bea4-43ff-b0d0-9e8a6a97d3ca
source-git-commit: 1a9df9f9819d9e0031e58443ec6a9e755a151ba0
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 12%

---

# Audit-Protokolle

Um die Transparenz und Sichtbarkeit der im System durchgeführten Aktivitäten zu erhöhen, werden Benutzeraktivitäten innerhalb des Mix Modeler-Workflows in Experience Platform-Auditprotokollen erfasst, um benutzergesteuerte Änderungen an Mix Modeler-Kategorien zu verstehen. Diese Protokolle bilden einen Audit-Trail, der Ihnen bei der Fehlerbehebung und Ihrem Unternehmen helfen kann, die Richtlinien zur Unternehmensdatenverwaltung und die gesetzlichen Anforderungen effektiv zu erfüllen.

<!-- DO WE HAVE TO ADD THIS
If you are subject to the Health Insurance Portability and Accountability Act (HIPAA) and create, receive, maintain, or transmit permitted sensitive personal data through Mix Modeler, you are responsible for executing a BAA with Adobe and licensing Healthcare Shield.
-->

Ein Auditprotokoll informiert darüber, wer welche Aktion wann ausgeführt hat. Jede in einem Protokoll aufgezeichnete Aktion enthält Metadaten, die den Aktionstyp, das Datum und die Uhrzeit, die E-Mail-ID der oder des Benutzenden, die oder der die Aktion durchgeführt hat, und weitere für den Aktionstyp relevante Attribute angeben. Es verfolgt die von Benutzenden in Mix Modeler durchgeführten Aktionen zum Erstellen, Aktualisieren und Löschen.

So überprüfen Sie das Administratorprotokoll in der Benutzeroberfläche von Mix Modeler:

1. Wählen Sie ![Aufgabenliste](/help/assets/icons/TaskList.svg) **[!UICONTROL Audits]** aus **[!UICONTROL PRIVACY]** aus.

1. In **[!UICONTROL Audits]** finden Sie die **[!UICONTROL Activity log]**. Das Aktivitätsprotokoll zeigt Einträge für die folgenden Mix Modeler-Kategorien, -Aktionen und -Status an.

   | Kategorie | Aktion | Status |
   |---|---|---|
   | Mix Modeler-Datensatzregel | Erstellen | Zulassen oder Ablehnen |
   | Mix Modeler-Datensatzregel | Update | Zulassen oder Ablehnen |
   | Mix Modeler-Datensatzregel | Löschen | Zulassen oder Ablehnen |
   | Mix Modeler-Feld | Erstellen | Zulassen oder Ablehnen |
   | Mix Modeler-Feld | Update | Zulassen oder Ablehnen |
   | Mix Modeler-Feld | Löschen | Zulassen oder Ablehnen |
   | Mix Modeler Marketing Touchpoint | Erstellen | Zulassen oder Ablehnen |
   | Mix Modeler Marketing Touchpoint | Update | Zulassen oder Ablehnen |
   | Mix Modeler Marketing Touchpoint | Löschen | Zulassen oder Ablehnen |
   | Mix Modeler-Konversion | Erstellen | Zulassen oder Ablehnen |
   | Mix Modeler-Konversion | Update | Zulassen oder Ablehnen |
   | Mix Modeler-Konversion | Löschen | Zulassen oder Ablehnen |
   | Mix Modeler-Modell | Erstellen | Zulassen oder Ablehnen |
   | Mix Modeler-Modell | Update | Zulassen oder Ablehnen |
   | Mix Modeler-Modell | Löschen | Zulassen oder Ablehnen |
   | Mix Modeler-Modell | neu bewerten | Zulassen oder Ablehnen |
   | Mix Modeler-Modell | Klonen | Zulassen oder Ablehnen |
   | Mix Modeler-Modell | Trainieren/Umschulen | Zulassen oder Ablehnen |
   | Mix Modeler-Modell | Herunterladen/Speichern von Metadaten | Zulassen oder Ablehnen |
   | Mix Modeler-Plan | Erstellen | Zulassen oder Ablehnen |
   | Mix Modeler-Plan | Update | Zulassen oder Ablehnen |
   | Mix Modeler-Plan | Zugehöriges Modell ändern | Zulassen oder Ablehnen |
   | Mix Modeler-Datenharmonisierung | Trigger Sync | Zulassen oder Ablehnen |


1. Wählen Sie einen Eintrag im Aktivitätsprotokoll aus, um ein Bedienfeld mit weiteren Details zu öffnen.

   ![Mix Modeler-Audit](/help/assets/mix-modeler-audit.png)

1. Um nach **[!UICONTROL Category]**, **[!UICONTROL Action]**, **[!UICONTROL Request ID]**, **[!UICONTROL User]**, **[!UICONTROL Status]** oder **[!UICONTROL Date]** Bereich zu filtern, wählen Sie ![Filter](/help/assets/icons/Filter.svg).

1. Um die im Aktivitätsprotokoll angezeigten Spalten zu ändern, wählen Sie ![Spalten](/help/assets/icons/ColumnSetting.svg) und im Dialogfeld &quot;**[!UICONTROL Customize table]**&quot; die anzuzeigenden Spalten aus. Wählen Sie **[!UICONTROL Apply]** aus, um die Auswahl anzuwenden, **[!UICONTROL Cancel]** um sie aufzuheben.

1. Um das Administratorprotokoll herunterzuladen, wählen Sie ![Herunterladen](/help/assets/icons/Download.svg) **[!UICONTROL Download log]**. Wählen Sie im Dialogfeld **[!UICONTROL Download log]** entweder **[!UICONTROL CSV]** oder **[!UICONTROL JSON]** als Format aus und klicken Sie auf **[!UICONTROL Download]**.

## Zugriff auf Auditprotokolle

Wenn die Funktion für Ihr Unternehmen aktiviert ist, werden bei Aktivitäten automatisch Auditprotokolle erfasst. Die Auditprotokollerfassung muss nicht manuell aktiviert werden.

Um Auditprotokolle anzeigen und exportieren zu können, benötigen Sie die Zugriffsberechtigung Zugriff auf Auditprotokolle . Informationen zum Verwalten individueller Berechtigungen für Mix Modeler-Funktionen finden Sie in der [Dokumentation zur Zugriffssteuerung](https://experienceleague.adobe.com/de/docs/experience-platform/access-control/home).
