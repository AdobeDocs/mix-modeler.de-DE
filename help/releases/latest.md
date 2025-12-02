---
title: Aktuelle Versionshinweise zu Mix Modeler anzeigen
description: Versionshinweise zum neuesten Mix Modeler
feature-set: Experience Cloud
feature: Release Notes
exl-id: 38a47672-2af2-437c-b769-4d5febb941f5
source-git-commit: cfdab6820423f1c5a01ecac52796414cde9a9935
workflow-type: tm+mt
source-wordcount: '874'
ht-degree: 4%

---

# Aktuelle Versionshinweise zu Mix Modeler

**Letzte Aktualisierung**: 12. November 2025.

Diese Versionshinweise beziehen sich auf die neueste Version von Mix Modeler. Mix Modeler-Versionen basieren auf einem kontinuierlichen Bereitstellungsmodell, das einen ungefähren monatlichen Veröffentlichungsintervall ermöglicht. Dementsprechend werden diese Versionshinweise aktualisiert, also überprüfen Sie sie regelmäßig.



## November 2025

| Funktion | Beschreibung | [Rollout-Start](#release-strategy) | [Allgemeine Verfügbarkeit](#release-strategy) |
|---|---|---|---|
| **[!UICONTROL Plans tracking]** | Benutzern ermöglichen, zu verstehen, wie die Ausführung von Marketing-Plänen verfolgt, was geplant ist. So können Sie sicher sein, wie Marketing funktioniert. Oder identifizieren Sie Chancen und Risiken früher, um Kurse zu korrigieren und Geschäftsziele zu erreichen. Die [Visualisierungen zur Leistungsplanung](/help/dashboard/plans.md#performance-to-plan) werden aktualisiert und ermöglichen die Konfiguration von Metriken und Granularität. | &#x200B;12. November 2025 | &#x200B;12. November 2025 |
| **[!UICONTROL Channel synergy insights]** | Verraten Sie, wie Marketing-Kanäle zusammenarbeiten, um eine größere Wirkung zu erzielen. Mit diesen Einblicken können Sie die bisherige Marketing-Leistung zuversichtlich erklären und die Marketing-Ausgaben entsprechend anpassen, um die Gesamtrendite Ihres Marketing-Portfolios zu maximieren. Eine Kanal-Synergie-Matrix ist in [Modelleinblicke](/help/models/insights.md#channel-synergy) und [Planeinblicke](/help/plans/insights.md#channel-synergies) verfügbar. | &#x200B;12. November 2025 | &#x200B;12. November 2025 |
| **Fehlerbehebungen** | Fehlerbehebungen für folgende Tickets: <ul><li>AMM-2920: Planerstellung und Migration.</li><li>AMM-3282: Wissenschaftliche Notation für kleine Zahlen in großen Rastern.</li></ul> | &#x200B;12. November 2025 | &#x200B;12. November 2025 |


## September 2025

| Funktion | Beschreibung | [Rollout-Start](#release-strategy) | [Allgemeine Verfügbarkeit](#release-strategy) |
|---|---|---|---|
| **[!UICONTROL Dataset mapping validations]** | Es wurden Validierungen zu Experience Platform-Datensatzzuordnungen für harmonisierte Felder hinzugefügt. | Mittwoch, 9. September 2025 | Mittwoch, 9. September 2025 |
| **[!UICONTROL Context menu on links to model and plans]** | Browser-Kontextmenü für Links zu Modellen und Plänen aktiviert. Sie können jetzt dieses Browser-Kontextmenü verwenden, um einen bestimmten Plan oder ein Modell in einer neuen Registerkarte oder einem neuen Fenster zu öffnen. | Mittwoch, 9. September 2025 | Mittwoch, 9. September 2025 |
| **Fehlerbehebungen** | Fehlerbehebungen für folgende Tickets: <ul><li>AMM-3101: Fehlerkorrektur - Es wurde eine falsche Zuordnungserstellung für Regeln behoben: `event_date` wurde als Feldname anstelle von `timestamp` übergeben.</li><li>AMM-3092: Es wurde ein Problem behoben, bei dem der Wert der maximalen Kanalbeschränkung in einem duplizierten budgetbasierten Plan nicht geändert werden konnte.</li><li>AM3130: Fehlerhafte **[!UICONTROL Run frequency]** in einem Detailpopup-Fenster eines Modells behoben.</li><li>AMM3158: Aktualisierte Beschriftungen für die **[!UICONTROL Select target metric]** Optionen als Teil des **[!UICONTROL Optimize]** Bereichs in der Benutzeroberfläche [Pläne erstellen](/help/plans/build.md).</li><li>AMM 3176: Es wurde ein Problem behoben, [&#x200B; die Visualisierung „Aufschlüsselung nach Kanal](/help/models/insights.md#breakdown) auf **[!UICONTROL Attribution]** Registerkarte in **[!UICONTROL Model Insights]** nicht angezeigt werden konnte.</li></ul> | Mittwoch, 9. September 2025 | Mittwoch, 9. September 2025 |
| **Fehlerbehebungen** | Fehlerbehebungen für folgende Tickets: <ul><li>AMM-3174: Verbesserte Erfahrung, wenn keine vorhandenen Pläne verfügbar sind.</li><li>AMM-3216: Verbesserte Validierung für benutzerdefinierte Datumsbereiche.</li><li>AMM-3240: Feste Ausführungsmodellfrequenz.</ul> | &#x200B;23. September 2025 | &#x200B;23. September 2025 |

## Juli–August 2025

| Funktion | Beschreibung | [Rollout-Start](#release-strategy) | [Allgemeine Verfügbarkeit](#release-strategy) |
|---|---|---|---|
| **[!UICONTROL Compare plans update]** | Die Benutzeroberfläche [Pläne vergleichen](/help/plans/compare.md) zeigt jetzt zusätzliche Details zu Paid Marketing an: ROI oder CPA und Umsatz. | &#x200B;20. August 2025 | &#x200B;20. August 2025 |
| **Harmonisierungsaktualisierungen** | Alle Datensatzregeln verwenden jetzt unabhängig vom Datensatztyp eine ähnliche [generische Zuordnung zu harmonisierten &#x200B;](/help/harmonize-data/dataset-rules.md)). Wenn Sie ein standardmäßiges harmonisiertes Feld aus einem Zusammenfassungsdatensatz zuordnen, versucht Mix Modeler, das entsprechende Experience Platform-Datensatzfeld automatisch abzuleiten. | Mittwoch, 29. Juli 2025 | Mittwoch, 29. Juli 2025 |
| **Verbesserter Plan - marginale ROI-/CPA-Optimierung** | Dadurch können Sie die Verteilung der Marketing-Budgets im Zeitverlauf verbessern. Anstatt den marginalen ROI/CPA über den gesamten Planungszeitraum hinweg zu konvergieren, können Sie [über Monate hinweg optimieren](/help/plans/build.md) während Sie die monatlichen Ausgabenmuster beibehalten. | Mittwoch, 8. Juli 2025 | Mittwoch, 8. Juli 2025 |


## Mai - Juni 2025

| Funktion | Beschreibung | [Rollout-Start](#release-strategy) | [Allgemeine Verfügbarkeit](#release-strategy) |
|---|---|---|---|
| **Zielbasierte Pläne** | Neben Budgets können Sie ein Ziel (Ziel) definieren, wenn Sie [&#x200B; Plan erstellen &#x200B;](/help/plans/build.md) [&#x200B; bearbeiten &#x200B;](/help/plans/insights.md#edit-plan). Beispiele für Zielmetriken sind Umsatz, Konversion, CPA oder ROI. | &#x200B;18. Juni 2025 | Mittwoch, 8. Juli 2025 |
| **Konfiguration des Ausgabenmusters** | Wenn Sie einen Plan erstellen, haben Sie jetzt die Möglichkeit, bei der Definition des Ausgabenmusters für jeden Budgetdatumsbereich [historische Referenz](/help/plans/build.md)-Daten (wie Daten zu früheren Marketing-Ausgaben und Einblicke) zu verwenden. | &#x200B;14. Mai 2025 | &#x200B;14. Mai 2025 |
| **Erweiterte Plankonfigurationen** | Sie können [erweiterte Konfigurationen](/help/plans/build.md) für Ihren Plan definieren, z. B. durchschnittliche Einnahmen pro Konvertierung und Kanalkosten. | &#x200B;14. Mai 2025 | &#x200B;14. Mai 2025 |

## März bis April 2025

| Funktion | Beschreibung | [Rollout-Start](#release-strategy) | [Allgemeine Verfügbarkeit](#release-strategy) |
|---|---|---|---|
| **Modelldrifterkennung** | Wenn Sie ein Modell öffnen, werden Sie [aufgefordert, das Modell neu zu trainieren, wenn eine Modelldrift erkannt wird](/help/models/insights.md#model-drift). | &#x200B;3. April 2025 | 7. Mai 2025 |
| **Marginaler Kanalgewinn in Planerkenntnissen** | Zu Plan Insights [&#x200B; eine Visualisierung &#x200B;](/help/plans/insights.md#marginal-channel-return)marginaler Kanalgewinn“ hinzugefügt, die den marginalen Breakeven und den Plangewinn für alle oder ausgewählte Kanäle anzeigt. | &#x200B;3. April 2025 | &#x200B;24. April 2025 |


## Januar bis Februar 2025

| Funktion | Beschreibung | [Rollout-Start](#release-strategy) | [Allgemeine Verfügbarkeit](#release-strategy) |
|---|---|---|---|
| **Verschachtelte Bedingungen** | Sie können verschachtelte Bedingungen mithilfe von UND und ODER erstellen, wenn Sie eine geeignete Datenpopulation als Teil der [Konfiguration eines Modells](/help/models/build.md#configure) definieren. | &#x200B;15. Januar 2025 | &#x200B;18. Februar 2025 |
| **Anzeigen von Berichten** | Sie können einen Bericht zu einem [Konversions](/help/harmonize-data/conversions.md#view-report) oder einem [Marketing-Touchpoint](/help/harmonize-data/marketing-touchpoints.md#view-report) anzeigen, den Sie im Rahmen der Datenharmonisierung definiert haben. | &#x200B;15. Januar 2025 | &#x200B;18. Februar 2025 |
| **Löschbestätigungen** | Sie werden aufgefordert, das Löschen eines [Plans](/help/plans/overview.md#delete-plans) oder eines [Modells](/help/models/overview.md#delete-models) zu bestätigen. | &#x200B;15. Januar 2025 | &#x200B;18. Februar 2025 |
| **Verbesserungen an der Benutzeroberfläche** | Sie können auswählen[&#x200B; welche &#x200B;](/help/models/insights.md#factors-beta) in Modelleinblicke angezeigt werden sollen. | &#x200B;15. Januar 2025 | &#x200B;18. Februar 2025 |
| **Fehlerbehandlung** | Benutzerfreundliche Fehlermeldungen und ein verbessertes Anwendererlebnis für Fehlerszenarien bei der Datenharmonisierung und bei Plänen. | &#x200B;18. Februar 2025 | &#x200B;18. Februar 2025 |
| **Modellstatus** | Neudefinition von [Modellstatus](/help/models/overview.md#manage-models) über den Modelllebenszyklus hinweg. | &#x200B;18. Februar 2025 | &#x200B;18. Februar 2025 |


## Versionsstrategie

[!UICONTROL Mix Modeler] verwendet Feature Flags (auch als „Umschalter“ bezeichnet), um die Sichtbarkeit neuer Funktionen zu steuern, sodass Tests im kontrollierten Maßstab vor der vollständigen Veröffentlichung möglich sind. Diese Versionsstrategie umfasst die folgenden Phasen:

* **Eingeschränktes Testen**: Eine schrittweise Veröffentlichung beginnt mit Tests durch Adobe-interne Benutzende. Sie wird dann einer kleinen Gruppe von Kundenkonten zur Verfügung gestellt, um sicherzustellen, dass die Funktion den Anforderungen und Erwartungen der Kunden entspricht.

* **Start des Rollouts**: Der Rollout einer stufenweisen Veröffentlichung beginnt mit der eingeschränkten Testphase. Die Verfügbarkeit der Version für Kunden wird dann im Laufe einiger Monate von 0 % auf 100 % skaliert. Der schrittweise Rollout erfolgt auf der Ebene der Experience Cloud-Organisation, sodass alle berechtigten Benutzenden in einer Organisation dasselbe Erlebnis erhalten.
