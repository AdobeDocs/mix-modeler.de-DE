---
title: Pläne - Übersicht
description: Erfahren Sie, wie Sie Pläne in Mix Modeler anzeigen, auswählen und Aktionen für sie durchführen können.
feature: Plans
exl-id: 45a8dc30-3259-493d-8ea5-1899903733a6
source-git-commit: 09b0868cc6f631188b2609b1da81d1a6b6f0aa9f
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 0%

---

# Pläne - Übersicht

Mit Plänen in Mix Modeler können Sie Budgets nach Geschäftseinheit und Kanal zuweisen. Die Planungsfunktionalität ist auf Basis der harmonisierten Daten in die Ergebnisse der trainierten Modelle integriert.

Ein Plan beschreibt die diskretionären Investitionen (z. B. Budgets), die ein Unternehmen im Laufe eines bestimmten Zeitraums für Marketing-bezogene Projekte ausgeben möchte. Diese Investitionen dienen allgemeinen KPIs (z. B. Bestellungen, Umsatz). Die Pläne können Ausgaben aus Kanälen wie bezahlter Werbung, gesponserten Web-Inhalten und Veranstaltungen umfassen.

Ein Plan erfordert:

- ein Modell,
- einen Datenbereich,
- Ein Budget.

Ein Plan kann optional Folgendes enthalten:

- ein konfiguriertes Erkennungsfenster,
- mehrere Flugtermine, von denen jedes ein Zielbudget hat,
- Mindest- und Höchstbudgetbeschränkungen nach Kanal und Flugdatum.

Wenn ein Modell, das Sie für Ihren Plan verwendet haben, mit neuen Daten bewertet wird, müssen Sie einen neuen Plan erstellen, um die neu bewerteten Daten zu berücksichtigen.


## Pläne erstellen

Verwenden Sie zum Erstellen eines Plans den Assistenten zur Erstellung eines Mix Modeler-Plans. Weitere [ finden Sie ](build.md)Erstellen von Plänen“.


## Pläne verwalten

So zeigen Sie eine Tabelle Ihrer aktuellen Pläne in der Benutzeroberfläche von Mix Modeler an:

1. Wählen Sie in der linken Leiste ![](/help/assets/icons/FileChart.svg) **[!UICONTROL Plans]** aus.

1. Sie sehen eine Tabelle der aktuellen Pläne und ihres Status.

   Die Tabellenspalten geben Details zu den Plänen an.

   | Spaltenname | Details |
   |---|---|
   | Name | Name des Plans |
   | Modell | Das als Grundlage für den Plan verwendete Modell. |
   | Datumsbereich | Der vollständige Datumsbereich für einen Plan. |
   | Budget | Das Gesamtbudget für einen Plan. |
   | Prognostizierte Rendite | Die [prognostizierte ](/help/main-guide/glossary.md)) für einen Plan |
   | Prognostizierter ROI | Der [prognostizierte ROI](/help/main-guide/glossary.md) für einen Plan. |
   | Prognostizierte Konversion | Die [prognostizierte Konversion](/help/main-guide/glossary.md) für einen Plan |
   | Prognostizierter CPA | Die [prognostizierte CPA](/help/main-guide/glossary.md) für einen Plan |
   | Status | Der Status eines Plans: <p><span style="color:red">●</span> fehlgeschlagen, <p><span style="color:blue">●</span> Verarbeitung läuft oder <p><span style="color:green">●</span> abgeschlossen. |

   {style="table-layout:auto"}

   Sie können ![ColumnSetting](/help/assets/icons/ColumnSetting.svg) verwenden, um die ![ Spalten (](/help/assets/icons/Checkmark.svg)) auszuwählen, die in der Tabelle angezeigt werden sollen.

1. Verwenden Sie ![Suche](/help/assets/icons/Search.svg), um die Tabelle nach einem oder mehreren bestimmten Plänen zu durchsuchen und zu filtern.

### Planerkenntnisse

So zeigen Sie die Einblicke eines Plans an und bearbeiten ihn:

1. Wählen Sie ![PLan](/help/assets/icons/FileChart.svg) in der linken Leiste **[!UICONTROL Plans]** aus.

1. Wählen Sie den Plannamen.

Sie werden zu &quot;[-Einblicke“ ](insights.md).


### Duplizieren eines Plans

Duplizieren eines Plans:

- Wählen Sie ![Mehr](/help/assets/icons/More.svg) für einen Plan aus. Wählen Sie im Kontextmenü **[!UICONTROL Duplicate]** aus.
- Wählen Sie alternativ einen Plan in der Tabelle ![SelectBox](/help/assets/icons/SelectBox.svg) aus und wählen Sie ![Kopieren](/help/assets/icons/Copy.svg) aus der blauen Aktionsleiste **[!UICONTROL Duplicate]**.

Es wird ein neuer Plan mit einem Namen erstellt, der sich aus dem Namen des ursprünglichen Plans zusammensetzt und an den **[!UICONTROL (Copy)](_n_)** angehängt ist. Sie werden automatisch zu [Planerstellung](build.md) umgeleitet, um aktualisierte Details für den kopierten Plan anzugeben.

- Details (wie Beschreibung, Budget und mehr) aus dem ursprünglichen Plan werden kopiert.
- Budgetbeschränkungen aus dem ursprünglichen Plan werden in den neu erstellten Plan kopiert.
- Sie haben die Möglichkeit, ein anderes Modell als Basis für den kopierten Plan auszuwählen.
   - Für Touchpoints oder Kanäle, die im kopierten Plan vorhanden sind, aber im neu ausgewählten Modell nicht vorhanden sind, werden alle Einschränkungen für diese Touchpoints oder Kanäle aus dem Plan entfernt.
   - Für Touchpoints oder Kanäle, die nicht im kopierten Plan, aber im neu ausgewählten Modell vorhanden sind, werden die Begrenzungen auf Folgendes festgelegt:
      - einen Mindestwert von `0`,
      - einen Höchstwert in Übereinstimmung mit dem Budget für den Flugbereich.



### Pläne vergleichen

Pläne vergleichen:

1. Wählen Sie zwei Pläne aus der Tabelle aus.
1. Wählen ![ in ](/help/assets/icons/Compare.svg) blauen Aktionsleiste **[!UICONTROL Compare]** Vergleichen“ aus. Sie sehen die **[!UICONTROL Compare plans]** Benutzeroberfläche.


### Pläne löschen

Löschen eines Plans:

1. Wählen Sie ![Mehr](/help/assets/icons/More.svg) für einen Plan aus. Wählen Sie im Kontextmenü **[!UICONTROL Delete]** aus. <br/>Wählen Sie alternativ einen Plan in der Tabelle ![SelectBox](/help/assets/icons/SelectBox.svg) aus und wählen Sie ![Löschen](/help/assets/icons/Delete.svg) aus **[!UICONTROL Delete]** blauen Aktionsleiste.
1. Wählen Sie **[!UICONTROL Delete]** im Bestätigungsdialogfeld **[!UICONTROL Delete plan]** aus, um den Plan zu löschen. Wählen Sie zum Abbrechen **[!UICONTROL Cancel]** aus.

So löschen Sie mehrere Pläne:

1. Mehrere Pläne auswählen.
1. Wählen Sie in der blauen Aktionsleiste die Option ![Löschen](/help/assets/icons/Delete.svg) aus, **[!UICONTROL Delete]** die Pläne zu löschen.
1. Wählen Sie **[!UICONTROL Delete]** im Bestätigungsdialogfeld **[!UICONTROL Delete *x *Pläne]**aus, um die Pläne zu löschen. Wählen Sie zum Abbrechen **[!UICONTROL Cancel]**aus.


