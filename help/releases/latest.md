---
title: Aktuelle Versionshinweise zu Mix Modeler anzeigen
description: Versionshinweise zum neuesten Mix Modeler
feature-set: Experience Cloud
feature: Release Notes
exl-id: 38a47672-2af2-437c-b769-4d5febb941f5
source-git-commit: 58f8745a224407cfb8ce3912bde9f0f85b5d8b46
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 2%

---

# Aktuelle Versionshinweise zu Mix Modeler

**Letzte Aktualisierung**: 14. Mai 2025.

Diese Versionshinweise beziehen sich auf die neueste Version von Mix Modeler. Mix Modeler-Versionen basieren auf einem kontinuierlichen Bereitstellungsmodell, das einen ungefähren monatlichen Veröffentlichungsintervall ermöglicht. Dementsprechend werden diese Versionshinweise aktualisiert, also überprüfen Sie sie regelmäßig.


## Mai - Juni 2025

| Funktion | Beschreibung | [Rollout-Start](#release-strategy) | [Allgemeine Verfügbarkeit](#release-strategy) |
|---|---|---|---|
| **Konfiguration des Ausgabenmusters** | Wenn Sie einen Plan erstellen, haben Sie jetzt die Möglichkeit, bei der Definition des Ausgabenmusters für jeden Budgetdatumsbereich [historische Referenz](/help/plans/build.md)-Daten (wie Daten zu früheren Marketing-Ausgaben und Einblicke) zu verwenden. | 14. Mai 2025 | 14. Mai 2025 |
| **Erweiterte Plankonfigurationen** | Sie können [erweiterte Konfigurationen](/help/plans/build.md) für Ihren Plan definieren, z. B. durchschnittliche Einnahmen pro Konvertierung und Kanalkosten. | 14. Mai 2025 | 14. Mai 2025 |

## März bis April 2025

| Funktion | Beschreibung | [Rollout-Start](#release-strategy) | [Allgemeine Verfügbarkeit](#release-strategy) |
|---|---|---|---|
| **Modelldrifterkennung** | Wenn Sie ein Modell öffnen, werden Sie [aufgefordert, das Modell neu zu trainieren, wenn eine Modelldrift erkannt wird](/help/models/insights.md#model-drift). | 3. April 2025 | 7. Mai 2025 |
| **Marginaler Kanalgewinn in Planerkenntnissen** | Zu Plan Insights [ eine Visualisierung ](/help/plans/insights.md#marginal-channel-return)marginaler Kanalgewinn“ hinzugefügt, die den marginalen Breakeven und den Plangewinn für alle oder ausgewählte Kanäle anzeigt. | 3. April 2025 | 24. April 2025 |


## Januar bis Februar 2025

| Funktion | Beschreibung | [Rollout-Start](#release-strategy) | [Allgemeine Verfügbarkeit](#release-strategy) |
|---|---|---|---|
| **Verschachtelte Bedingungen** | Sie können verschachtelte Bedingungen mithilfe von UND und ODER erstellen, wenn Sie eine geeignete Datenpopulation als Teil der [Konfiguration eines Modells](/help/models/build.md#configure) definieren. | 15. Januar 2025 | 18. Februar 2025 |
| **Anzeigen von Berichten** | Sie können einen Bericht zu einem [Konversions](/help/harmonize-data/conversions.md#view-report) oder einem [Marketing-Touchpoint](/help/harmonize-data/marketing-touchpoints.md#view-report) anzeigen, den Sie im Rahmen der Datenharmonisierung definiert haben. | 15. Januar 2025 | 18. Februar 2025 |
| **Löschbestätigungen** | Sie werden aufgefordert, das Löschen eines [Plans](/help/plans/overview.md#delete-plans) oder eines [Modells](/help/models/overview.md#delete-models) zu bestätigen. | 15. Januar 2025 | 18. Februar 2025 |
| **Verbesserungen an der Benutzeroberfläche** | Sie können auswählen[ welche ](/help/models/insights.md#factors-beta) in Modelleinblicke angezeigt werden sollen. | 15. Januar 2025 | 18. Februar 2025 |
| **Fehlerbehandlung** | Benutzerfreundliche Fehlermeldungen und ein verbessertes Anwendererlebnis für Fehlerszenarien bei der Datenharmonisierung und bei Plänen. | 18. Februar 2025 | 18. Februar 2025 |
| **Modellstatus** | Neudefinition von [Modellstatus](/help/models/overview.md#manage-models) über den Modelllebenszyklus hinweg. | 18. Februar 2025 | 18. Februar 2025 |


## Versionsstrategie

[!UICONTROL Mixx Modeler] verwendet Feature Flags (auch als „Umschalter“ bezeichnet), um die Sichtbarkeit neuer Funktionen zu steuern, sodass Tests im kontrollierten Maßstab vor der vollständigen Veröffentlichung möglich sind. Diese Versionsstrategie umfasst die folgenden Phasen:

* **Eingeschränktes Testen**: Eine schrittweise Veröffentlichung beginnt mit Tests durch Adobe-interne Benutzende. Sie wird dann einer kleinen Gruppe von Kundenkonten zur Verfügung gestellt, um sicherzustellen, dass die Funktion den Anforderungen und Erwartungen der Kunden entspricht.

* **Start des Rollouts**: Der Rollout einer stufenweisen Veröffentlichung beginnt mit der eingeschränkten Testphase. Die Verfügbarkeit der Version für Kunden wird dann im Laufe einiger Monate von 0 % auf 100 % skaliert. Der schrittweise Rollout erfolgt auf der Ebene der Experience Cloud-Organisation, sodass alle berechtigten Benutzenden in einer Organisation dasselbe Erlebnis erhalten.
