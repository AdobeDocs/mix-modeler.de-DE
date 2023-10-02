---
title: Modelle
description: Erfahren Sie, wie Sie Modelle in Mix Modeler konfigurieren und verwenden.
feature: Models
source-git-commit: 08cfd4239f6bcaf885565f3ae04cbd51869e8c00
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 3%

---


# Modelle

Mit der Modellfunktion in Mix Modeler können Sie KI/ML-Modelle konfigurieren, trainieren und bewerten, die speziell auf Ihre Geschäftsziele abgestimmt sind und durch KI-gestütztes Transferlernen zwischen der Multitouch-Attribution und der Marketing-Mix-Modellierung unterstützt werden.

Die Modelle basieren auf den harmonisierten Daten, die Sie im Rahmen des Mix Modeler-Anwendungs-Workflows erstellen.

Um ein Modell zu erstellen, verwenden Sie den schrittweisen Konfigurationsfluss des Modells Mix Model , der bei Auswahl von verfügbar ist. **[!UICONTROL Guide me]**. Siehe [Modell erstellen](create.md) für weitere Details.

## Modelle verwalten

So zeigen Sie eine Tabelle Ihrer aktuellen Modelle in der Mix Modeler-Benutzeroberfläche an:

1. Auswählen ![](../assets/icons/FileData.svg) **[!UICONTROL Models]** über die linke Leiste.

1. Sie sehen eine Tabelle der aktuellen Modelle.

   Die Tabellenspalten geben Details zum Modell an.

   | Spaltenname | Details |
   |---|---|
   | Name | Name des Modells |
   | Beschreibung | Beschreibung des Modells |
   | Konversionsereignisse | Die für das Modell ausgewählte Konversion. |
   | Datensatz | Der Datensatz, den das Modell zum Trainieren und Bewerten verwendet. Dies ist standardmäßig der harmonisierte Datensatz. |
   | Ausführungshäufigkeit | Die Ausführungsfrequenz des Trainings des Modells. |
   | Letzte Ausführung | Datum und Uhrzeit der letzten Schulung des Modells. |
   | Status der letzten Ausführung | Der Status des letzten Trainings des Modells. <br/><span style="color:green">●</span> Erfolg<br/><span style="color:orange">●</span> Schulungsfehler<br/> <span style="color:orange">●</span> Vorbereitung der Schulung <br/><span style="color:red">●</span> Fehlgeschlagen |

   {style="table-layout:auto"}

1. Um die für die Liste angezeigten Spalten zu ändern, wählen Sie ![Spalteneinstellungen](../assets/icons/ColumnSetting.svg) und Spalten ein-/ausschalten ![Überprüfen](../assets/icons/Checkmark.svg) oder aus.

### Modell löschen

So löschen Sie ein Modell:

1. Wählen Sie den Namen des Modells aus, das Sie löschen möchten.

1. Wählen Sie im Kontextmenü die Option **[!UICONTROL Delete]** , um das Modell zu löschen.

### Details eines Modells anzeigen

So zeigen Sie weitere Details eines Modells an:

1. Wählen Sie den Namen des Modells aus, für das Sie weitere Details anzeigen möchten.

1. Wählen Sie im Kontextmenü die Option **[!UICONTROL More]**. Details zum ausgewählten Modell finden Sie im rechten Bereich.



### Modelleinblicke

>[!NOTE]
>
>Diese Auswahl ist nur für erfolgreich trainierte Modelle verfügbar.
>

So zeigen Sie Einblicke in ein Modell in der Mix Modeler-Oberfläche an:

1. Auswählen ![](../assets/icons/FileData.svg) **[!UICONTROL Models]** über die linke Leiste.

1. Wählen Sie den Namen eines Modells mit einer **[!UICONTROL Last run status]** von <span style="color:green">●</span> **[!UICONTROL Success]** aus dem **[!UICONTROL Models]** Tabelle.

1. Wählen Sie im Kontextmenü die Option **[!UICONTROL Model Insights]**. Sie werden zu [Model Insights](insights.md).


