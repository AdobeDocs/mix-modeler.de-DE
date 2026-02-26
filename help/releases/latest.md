---
title: Aktuelle Versionshinweise zu Mix Modeler anzeigen
description: Versionshinweise zum neuesten Mix Modeler
feature-set: Experience Cloud
feature: Release Notes
exl-id: 38a47672-2af2-437c-b769-4d5febb941f5
source-git-commit: 95b38fd12554e7ad223434c056d870a561fd9c68
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 3%

---

# Aktuelle Versionshinweise zu Mix Modeler

**Letzte Aktualisierung**: 26. Februar 2026.

Diese Versionshinweise beziehen sich auf die neueste Version von Mix Modeler. Mix Modeler-Versionen basieren auf einem kontinuierlichen Bereitstellungsmodell, das einen ungefähren monatlichen Veröffentlichungsintervall ermöglicht. Dementsprechend werden diese Versionshinweise aktualisiert, also überprüfen Sie sie regelmäßig.

## Februar 2026

| Funktion | Beschreibung | [Rollout-Start](#release-strategy) | [Allgemeine Verfügbarkeit](#release-strategy) |
|---|---|---|---|
| **Arbeitsablauf für harmonisierte Faktoren** | Faktoren werden jetzt im Rahmen eines Workflows [Harmonisierte Faktoren“ ](/help/harmonize-data/overview.md#factors). Dies vereinfacht die [ (Definition von Faktordaten](/help/ingest-data/schemas.md#factor-standard-fields-field-group) die [ (Verwaltung interner und externer Faktoren als Teil Ihrer Datensatzregeln](/help/harmonize-data/dataset-rules.md#factor-datasets) und die Verwendung von Faktordaten in [Modellen](/help/models/build.md#configure). | &#x200B;25. Februar 2026 | &#x200B;25. Februar 2026 |
| **[!UICONTROL Granular incrementality reporting]** | Definieren Sie harmonisierte Felder, damit Sie die Berichterstellung für Ihr Modell mit [granularen Insights-Reporting-Feldern](/help/models/build.md#granular-insights-reporting-fields) aufschlüsseln können, anstatt separate Modelle erstellen zu müssen. | &#x200B;18. Februar 2026 | &#x200B;18. Februar 2026 |

## Januar 2026

| Funktion | Beschreibung | [Rollout-Start](#release-strategy) | [Allgemeine Verfügbarkeit](#release-strategy) |
|---|---|---|---|
| **[!UICONTROL Dataset rules]** | [Tabelle mit Datensatzregeln wurde ](/help/harmonize-data/dataset-rules.md). Sie können nach einer oder mehreren Datensatzregeln suchen und eine Datensatzregel direkt in der Tabelle anzeigen, bearbeiten oder löschen. | &#x200B;13. Januar 2026 | &#x200B;13. Januar 2026 |
| **[!UICONTROL Current spend]** | Fügen Sie einen aktuellen Ausgabenpunkt in der [Visualisierung der marginalen Antwortkurve](/help/models/insights.md#marginal-response-curves) in Modelleinblicke hinzu. | &#x200B;13. Januar 2026 | &#x200B;13. Januar 2026 |
| **[!UICONTROL Sort and resize columns]** | Sortieren und Ändern der Größe von Spalten in der Tabelle [Modelle](/help/models/overview.md) und [Pläne](/help/plans/overview.md) hinzugefügt. | &#x200B;13. Januar 2026 | &#x200B;13. Januar 2026 |
| **Fehlerbehebungen** | Fehlerbehebungen für folgende Tickets: <ul><li>AMM-3328: Feldeingabe für neue Operatoren für Faktoren deaktiviert</li><li>AMM-3359: Datumsauswahl und Kombinationsfeld-Sperre.</li><li>AMM-3441: Beim Duplizieren eines Plans werden Datumsbereich und Budget nicht automatisch ausgefüllt.</li></ul> | &#x200B;13. Januar 2026 | &#x200B;13. Januar 2026 |


## Versionsstrategie

[!UICONTROL Mix Modeler] verwendet Feature Flags (auch als „Umschalter“ bezeichnet), um die Sichtbarkeit neuer Funktionen zu steuern, sodass Tests im kontrollierten Maßstab vor der vollständigen Veröffentlichung möglich sind. Diese Versionsstrategie umfasst die folgenden Phasen:

* **Eingeschränktes Testen**: Eine schrittweise Veröffentlichung beginnt mit Tests durch Adobe-interne Benutzende. Sie wird dann einer kleinen Gruppe von Kundenkonten zur Verfügung gestellt, um sicherzustellen, dass die Funktion den Anforderungen und Erwartungen der Kunden entspricht.

* **Start des Rollouts**: Der Rollout einer stufenweisen Veröffentlichung beginnt mit der eingeschränkten Testphase. Die Verfügbarkeit der Version für Kunden wird dann im Laufe einiger Monate von 0 % auf 100 % skaliert. Der schrittweise Rollout erfolgt auf der Ebene der Experience Cloud-Organisation, sodass alle berechtigten Benutzenden in einer Organisation dasselbe Erlebnis erhalten.
