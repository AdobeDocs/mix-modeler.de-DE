---
title: Data Governance
description: Erfahren Sie, wie Sie die Dienste und Tools von Experience Platform verwenden, mit denen Sie Ihre erfassten Erlebnisdaten steuern können. So halten Sie Ihre Geschäftspraktiken, gesetzlichen Verpflichtungen und Entwicklungsprozesse ein.
feature: Administration
source-git-commit: 6776a91563f120db1341adef923aab4b0f582c9d
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 11%

---

# Data Governance

Die Integration zwischen Mix Modeler und Experience Platform bietet Mix Modelern die Möglichkeit, die intrinsischen Data Governance-Funktionen von Experience Platform zu nutzen. In diesem Abschnitt der Dokumentation werden die Besonderheiten der Data Governance-Funktionen beschrieben, die in Mix Modeler verfügbar sind.

Experience Platform Data Governance bietet Ihnen die Möglichkeit, Ihre Daten über die gesamte Journey zu steuern und zu verstehen, die Daten über Experience Platform erfassen. Diese Journey umfasst die Pflege der Datenqualität, Datenherkunft, Datenkatalogisierung und vieles mehr.

Datennutzungsbezeichnungen und Richtlinien, die für Datensätze erstellt werden, die von der Experience Platform-Oberfläche im Mix Modeler verwendet werden, sofern angemessen. Beispielsweise werden Benutzer durch diese Beschriftungen beim Löschen von Datensätzen, die Teil einer Datensatzregel in den harmonisierten Daten sind, angehalten oder gewarnt. Alternativ können Sie Schemafelder ausblenden, die für Benutzer beim Erstellen einer Datensatzregel eingeschränkt sind.

Die Data Governance-Integration ermöglicht Ihnen eine effizientere Verwaltung der Compliance. Datenverantwortliche in Ihrem Unternehmen können Richtlinien festlegen, um die Nutzung zu beschränken. So können Sie Daten verwenden, die den von Datenverantwortlichen definierten Richtlinien entsprechen. Weitere Informationen finden Sie in der Dokumentation zu [Kennzeichnungen und Richtlinien](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/data-governance).

Die folgenden Data Governance-Funktionen sind verfügbar:

| Funktion | Details |
|---|---|
| Zugriffssteuerungen | Rollenbasierte Zugriffskontrolle und attributbasierte Zugriffskontrolle (auf Feldebene) werden unterstützt. Weitere Informationen finden Sie unter [Zugriffssteuerungen](access-controls.md) . |
| Audit-Protokolle | Wenn Mix Modeler bestimmte Kategorien erstellen, aktualisieren oder löschen, zeichnet die Experience Platform Audit-Funktion die Aktivität in den Auditprotokollen auf. Weitere Informationen finden Sie unter [Prüfprotokolle](audit-logs.md) . |
| Richtlinien | Im Rahmen des harmonisierten Daten-Workflows werden Experience Platform-definierte Richtlinien durchgesetzt. Jeder Verstoß gegen Datennutzungsbezeichnungen wird gemeldet und dem Benutzer angezeigt. Weitere Informationen finden Sie unter [Richtlinien](policies.md) . |
| Verschlüsselung | Alle Datensätze, die für die Eingabe und Ausgabe von Modellen verwendet werden, folgen den Experience Platform-Richtlinien. Die Experience Platform-Datenverschlüsselung gilt für Daten während der Ruhezeit und während der Übertragung. |
| Datenhygiene | Alle Datensätze, die für Eingabe- und Nicht-Experience Platform-Modelle verwendet werden, folgen den-Richtlinien. Experience Platform bietet eine Reihe von Tools zur Verwaltung des Lebenszyklus von Kundendaten, einschließlich der Unterstützung verschiedener Arten von Datenabläufen. Wenn Sie einen Quelldatensatz aus Experience Platform löschen, der als Teil Ihrer harmonisierten Daten verwendet wird, werden Sie benachrichtigt. Weitere Informationen finden Sie unter [Datensatzregeln](/help/harmonize-data/dataset-rules.md) . |
| Kundenseitig verwaltete Schlüssel | Wenn Sie Mix Modeler mit dem Privacy Security Shield- oder Healthcare Shield-Add-on lizenziert haben, können Sie die Funktion &quot;Kundenverwaltete Schlüssel&quot;verwenden, um Azure Key Vault zu nutzen und Ihre eigenen Schlüssel über APIs zu importieren. Sie verfügen über eine vollständige Verwaltung der Daten, die in Modellen in Mix Modeler verarbeitet werden. |
