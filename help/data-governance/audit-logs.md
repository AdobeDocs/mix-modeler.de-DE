---
title: Audit-Protokolle
description: Erfahren Sie, wie Sie von Mix Modeler aus auf Prüfprotokolle zugreifen können.
feature: Administration
exl-id: aa65aac5-bea4-43ff-b0d0-9e8a6a97d3ca
source-git-commit: 77a338ae568c854b99069b849a18661d413c501c
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 12%

---

# Audit-Protokolle

Um die Transparenz und Sichtbarkeit der im System durchgeführten Aktivitäten zu erhöhen, wird die Benutzeraktivität innerhalb des Mix Modeler-Workflows in den Experience Platform-Auditprotokollen erfasst, um benutzergesteuerte Änderungen an den Mix Modeler-Kategorien zu verstehen. Diese Protokolle bilden ein Audit-Protokoll, das Ihnen bei der Fehlerbehebung helfen kann und Ihrem Unternehmen helfen kann, die Richtlinien zur Unternehmensdatenverwaltung und die gesetzlichen Anforderungen effektiv zu erfüllen.

<!-- DO WE HAVE TO ADD THIS
If you are subject to the Health Insurance Portability and Accountability Act (HIPAA) and create, receive, maintain, or transmit permitted sensitive personal data through Mix Modeler, you are responsible for executing a BAA with Adobe and licensing Healthcare Shield.
-->

Ein Prüfprotokoll informiert darüber, wer welche Aktion ausgeführt hat und wann. Jede in einem Protokoll aufgezeichnete Aktion enthält Metadaten, die den Aktionstyp, das Datum und die Uhrzeit, die E-Mail-ID der oder des Benutzenden, die oder der die Aktion durchgeführt hat, und weitere für den Aktionstyp relevante Attribute angeben. Sie verfolgt die Aktionen zum Erstellen, Aktualisieren und Löschen, die von Benutzern in Mix Modeler ausgeführt werden.

So überprüfen Sie das Auditprotokoll in der Mix Modeler-Benutzeroberfläche:

1. Wählen Sie ![Aufgabenliste](/help/assets/icons/TaskList.svg) **[!UICONTROL Audits]** aus **[!UICONTROL PRIVACY]** aus.

1. In **[!UICONTROL Audits]** können Sie den **[!UICONTROL Activity log]** finden. Das Aktivitätsprotokoll enthält Einträge für die folgenden Mix Modeler-Kategorien, -Aktionen und -Status.

   | Kategorie | Aktion | Status |
   |---|---|---|
   | Mix Modeler-Datensatzregel | Erstellen | Zulassen oder Ablehnen |
   | Mix Modeler-Datensatzregel | Update | Zulassen oder Ablehnen |
   | Mix Modeler-Datensatzregel | Löschen | Zulassen oder Ablehnen |
   | Mix Modeler | Erstellen | Zulassen oder Ablehnen |
   | Mix Modeler | Update | Zulassen oder Ablehnen |
   | Mix Modeler | Löschen | Zulassen oder Ablehnen |
   | Mix Modeler-Marketing-Touchpoint | Erstellen | Zulassen oder Ablehnen |
   | Mix Modeler-Marketing-Touchpoint | Update | Zulassen oder Ablehnen |
   | Mix Modeler-Marketing-Touchpoint | Löschen | Zulassen oder Ablehnen |
   | Mix Modeler-Konversion | Erstellen | Zulassen oder Ablehnen |
   | Mix Modeler-Konversion | Update | Zulassen oder Ablehnen |
   | Mix Modeler-Konversion | Löschen | Zulassen oder Ablehnen |
   | Mix Modeler-Modell | Erstellen | Zulassen oder Ablehnen |
   | Mix Modeler-Modell | Update | Zulassen oder Ablehnen |
   | Mix Modeler-Modell | Löschen | Zulassen oder Ablehnen |
   | Mix Modeler-Modell | Neubewertung | Zulassen oder Ablehnen |
   | Mix Modeler-Modell | Klonen | Zulassen oder Ablehnen |
   | Mix Modeler-Modell | Zug/Zug | Zulassen oder Ablehnen |
   | Mix Modeler-Modell | Herunterladen/Speichern von Metadaten | Zulassen oder Ablehnen |
   | Mix Modeler-Abo | Erstellen | Zulassen oder Ablehnen |
   | Mix Modeler-Abo | Update | Zulassen oder Ablehnen |
   | Mix Modeler-Abo | Verknüpftes Modell ändern | Zulassen oder Ablehnen |
   | Harmonisierung der Daten des Mix Modelers | Trigger synchronisieren | Zulassen oder Ablehnen |


1. Wählen Sie einen Eintrag im Aktivitätsprotokoll aus, um einen Bereich für weitere Details zu öffnen.

   ![Mix Modeler-Audit](/help/assets/mix-modeler-audit.png)

1. Um nach dem Bereich **[!UICONTROL Category]**, **[!UICONTROL Action]**, **[!UICONTROL Request ID]**, **[!UICONTROL User]**, **[!UICONTROL Status]** oder **[!UICONTROL Date]** zu filtern, wählen Sie ![Filter](/help/assets/icons/Filter.svg) aus.

1. Um die im Aktivitätsprotokoll angezeigten Spalten zu ändern, wählen Sie ![Spalten](/help/assets/icons/ColumnSetting.svg) aus und wählen Sie im Dialogfeld **[!UICONTROL Customize table]** die anzuzeigenden Spalten aus. Wählen Sie &quot;**[!UICONTROL Apply]**&quot;, um die Auswahl anzuwenden, &quot;**[!UICONTROL Cancel]**&quot;, um die Auswahl abzubrechen.

1. Um das Prüfprotokoll herunterzuladen, wählen Sie ![Download](/help/assets/icons/Download.svg) **[!UICONTROL Download log]** aus. Wählen Sie im Dialogfeld **[!UICONTROL Download log]** entweder **[!UICONTROL CSV]** oder **[!UICONTROL JSON]** als Format und dann **[!UICONTROL Download]** aus.

## Zugriff auf Prüfprotokolle

Wenn die Funktion für Ihr Unternehmen aktiviert ist, werden bei auftretenden Aktivitäten automatisch Prüfprotokolle erfasst. Sie müssen die Erfassung von Auditprotokollen nicht manuell aktivieren.

Zum Anzeigen und Exportieren von Auditprotokollen müssen Sie über die Zugriffssteuerungsberechtigung Auditprotokolle erhalten haben. Informationen zum Verwalten individueller Berechtigungen für Mix Modeler-Funktionen finden Sie in der Dokumentation zur [Zugriffskontrolle](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home) .
