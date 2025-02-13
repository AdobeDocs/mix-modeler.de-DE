---
title: Data Governance - Übersicht
description: Erfahren Sie, wie Sie die Services und Tools von Experience Platform verwenden, mit denen Sie Ihre erfassten Erlebnisdaten steuern können. So halten Sie Ihre Geschäftspraktiken, rechtlichen Verpflichtungen und Ihren Entwicklungsprozess ein.
feature: Administration
exl-id: 87407c29-e158-48bf-bde9-b3c16a16107e
source-git-commit: 0ee212a626986e4c721d0e58f2528d0ca1a9fdbf
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 10%

---

# Data Governance - Übersicht

Die Integration zwischen Mix Modeler und Experience Platform bietet Mix Modeler die Möglichkeit, die internen Data Governance-Funktionen von Experience Platform zu nutzen. In diesem Abschnitt der Dokumentation werden die Besonderheiten der in Mix Modeler verfügbaren Data Governance-Funktionen beschrieben.

Experience Platform Data Governance bietet Ihnen die Möglichkeit, Ihre Daten über den gesamten Journey, den Daten über Experience Platform durchlaufen, zu kontrollieren und zu erfassen. Diese Journey umfasst die Aufrechterhaltung der Datenqualität, der Datenherkunft, der Datenkatalogisierung und vieles mehr.

Datennutzungsbeschriftungen und -richtlinien, die für Datensätze erstellt werden, die von der Experience Platform-Oberfläche in der Mix Modeler genutzt werden, sofern zutreffend. Beispielsweise stoppen oder warnen diese Kennzeichnungen Benutzende, wenn sie Datensätze löschen, die Teil einer Datensatzregel in den harmonisierten Daten sind. Oder blenden Sie Schemafelder aus, die beim Erstellen einer Datensatzregel für Benutzer eingeschränkt sind.

Die Data Governance-Integration ermöglicht ein effizienteres Compliance-Management. Datenverantwortliche in Ihrem Unternehmen können Richtlinien festlegen, um die Nutzung zu beschränken. So können Sie Daten verwenden, die den von Datenverantwortlichen definierten Richtlinien entsprechen. Weitere Informationen finden Sie in der Dokumentation zu [Kennzeichnungen und Richtlinien](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/data-governance).

Die folgenden Data Governance-Funktionen sind verfügbar:

| Funktion | Details |
|---|---|
| Zugriffssteuerungen | Es werden die rollenbasierte Zugriffssteuerung und die attributbasierte Zugriffssteuerung (auf Feldebene) unterstützt. Weitere Informationen finden [ unter ](access-controls.md). |
| Audit-Protokolle | Wenn Benutzende bestimmte Mix Modeler-Kategorien erstellen, aktualisieren oder löschen, zeichnet die Experience Platform-Überwachungsfunktion die Aktivität in den Administratorprotokollen auf. Weitere [ finden Sie ](audit-logs.md) Auditprotokolle . |
| Richtlinien | Im Rahmen des harmonisierten Daten-Workflows werden von Experience Platform definierte Richtlinien durchgesetzt. Jeder Verstoß gegen Datennutzungskennzeichnungen wird gemeldet und dem Benutzer angezeigt. Weitere Informationen finden [ unter ](policies.md). |
| Verschlüsselung | Alle Datensätze, die für die Eingabe und Ausgabe von Modellen verwendet werden, entsprechen den Experience Platform-Richtlinien. Die Experience Platform-Datenverschlüsselung gilt für Daten im Ruhezustand und während der Übertragung. |
| Datenhygiene | Alle Datensätze, die für Eingabe- und Nicht-Modelle verwendet werden, entsprechen den Experience Platform-Richtlinien. Experience Platform bietet eine Reihe von Tools zur Verwaltung des Lebenszyklus von Kundendaten, einschließlich der Unterstützung verschiedener Arten von Datenablauf. Wenn Sie einen Quelldatensatz aus Experience Platform löschen, der als Teil Ihrer harmonisierten Daten verwendet wird, werden Sie benachrichtigt. Weitere Informationen [ Sie unter ](/help/harmonize-data/dataset-rules.md)Datensatzregeln“. |
| Kundenseitig verwaltete Schlüssel | Wenn Sie Mix Modeler mit dem Add-on Privacy Security Shield oder Healthcare Shield lizenziert haben, können Sie die Funktion Customer Managed Keys verwenden, um Azure Key Vault zu nutzen und Ihre eigenen Schlüssel über APIs zu übertragen. Sie verfügen über eine vollständige Verwaltung von Daten, die innerhalb von Modellen in Mix Modeler verarbeitet werden. |
