---
title: Modelle
description: Erfahren Sie, wie Sie Modelle in Mix Modeler konfigurieren und verwenden.
feature: Models
exl-id: c43d9bc9-4429-45c2-9247-bd24510a24be
source-git-commit: 9a6c1f1c12ab29da80a1997cfd31ca07b38eaa22
workflow-type: tm+mt
source-wordcount: '805'
ht-degree: 1%

---

# Modelle

Mit der Modellfunktion in Mix Modeler können Sie Modelle konfigurieren, trainieren und bewerten, die für Ihre Geschäftsziele spezifisch sind. Das Training und Scoring unterstützt das KI-gestützte Transfer-Lernen zwischen der Multitouch-Attribution und der Marketing-Mix-Modellierung.

Die Modelle basieren auf den harmonisierten Daten, die Sie im Rahmen des Mix Modeler-Anwendungs-Workflows erstellen.

Ein Modell in Mix Modeler ist ein Modell für maschinelles Lernen, das verwendet wird, um ein bestimmtes Ergebnis basierend auf den Investitionen eines Marketingexperten zu messen und vorherzusagen. Marketing-Touchpoints und Daten der Zusammenfassungsebene können als Eingabe verwendet werden. Mit Mix Modeler können Sie Varianten von Modellen basierend auf verschiedenen Variablensätzen von Variablen, Dimensionen und Ergebnissen erstellen, z. B. Umsatz, verkaufte Einheiten und Leads.

Ein Modell erfordert:

* Eine Konversion.
* Ein oder mehrere Marketing-Touchpoints (Kanäle), die aus Zusammenfassungsdaten, Marketing-Touchpoint-Daten (Ereignisdaten) oder beidem bestehen.
* Ein konfigurierbares Lookback-Fenster.
* Ein konfigurierbares Schulungsfenster.

Ein Modell kann optional Folgendes enthalten:

* Externe Faktoren.
* Interne Faktoren.
* Frühere Kenntnisse von Marketing-Beiträgen aus anderen Quellen, z. B. Erfahrungen von Interessenträgern aus der Vergangenheit, schrittweise Tests und andere Modelle.
* Ausgabenfreigabe, die den relativen Ausgabenanteil als Proxy verwendet, wenn die Marketing-Daten gering sind.


## Modell erstellen

Verwenden Sie zum Erstellen eines Modells den schrittweisen Konfigurationsfluss des geführten Mix Modelers, der bei Auswahl von **[!UICONTROL Open model canvas]** verfügbar ist. Weitere Informationen finden Sie unter [Erstellen eines Modells](create.md) .

## Modelle verwalten

So zeigen Sie eine Tabelle Ihrer aktuellen Modelle in der Mix Modeler-Benutzeroberfläche an:

1. Wählen Sie in der linken Leiste ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** aus.

1. Sie sehen eine Tabelle der aktuellen Modelle.

   Die Tabellenspalten geben Details zum Modell an.

   | Spaltenname | Details |
   |---|---|
   | Name | Name des Modells |
   | Beschreibung | Beschreibung des Modells |
   | Konversionsereignis | Die für das Modell ausgewählte Konversion. |
   | Ausführungshäufigkeit | Die Ausführungsfrequenz des Trainings des Modells. |
   | Letzte Ausführung | Datum und Uhrzeit der letzten Schulung des Modells. |
   | Status | Der Status des letzten Trainings des Modells. <br/>![StatusGreen](/help/assets/icons/StatusGreen.svg) Erfolg<br/>![StatusOrange](/help/assets/icons/StatusOrange.svg) Schulungsproblem<br/> ![StatusOrange](/help/assets/icons/StatusOrange.svg) Warten auf Schulung <br/>![StatusRed](/help/assets/icons/StatusRed.svg) Fehlgeschlagen <br/>![StatusGreen](/help/assets/icons/StatusGray.svg) _ (wenn ein letzter Lauf ausgeführt wird) |

   {style="table-layout:auto"}

1. Um die für die Liste angezeigten Spalten zu ändern, wählen Sie ![Spalteneinstellungen](/help/assets/icons/ColumnSetting.svg) aus und schalten Sie die Spalten auf ![Aktivieren](/help/assets/icons/Checkmark.svg) oder aus.

Sie können die folgenden Aktionen für ein bestimmtes Modell ausführen.

### Details anzeigen

So zeigen Sie weitere Details eines Modells an:

1. Wählen Sie in der linken Leiste ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** aus.

1. Wählen Sie ![Info](/help/assets/icons/Info.svg) für ein Modell aus, um ein Popup mit Details anzuzeigen.



### Duplizieren

Sie können ein Modell schnell duplizieren.

1. Wählen Sie in der linken Leiste ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** aus.

1. Wählen Sie ![Mehr](/help/assets/icons/More.svg) für ein Modell und klicken Sie im Kontextmenü auf **[!UICONTROL Duplicate]**.


### Modelleinblicke

Die Modelleinblicke-Funktion ist nur für erfolgreich trainierte und bewertete Modelle verfügbar.

So zeigen Sie die Einblicke eines Modells an:

1. Wählen Sie in der linken Leiste ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** aus.

1. Wählen Sie den Modellnamen aus.

Sie werden zu [Model Insights](insights.md) umgeleitet.


### Umzug


Das erneute Trainieren eines Modells ist nur auf erfolgreich trainierten Modellen verfügbar.

Ziehen Sie in Erwägung, ein Modell neu zu trainieren, wenn Sie:

* Neue inkrementelle Marketing- und Faktordaten einschließen. Beispielsweise hat sich im letzten Quartal die Marktdynamik verändert oder Ihre Marketing-Datenverteilung hat sich erheblich geändert.

So trainieren Sie ein Modell neu:

1. Wählen Sie in der linken Leiste ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** aus.

1. Wählen Sie ![Mehr](/help/assets/icons/More.svg) für ein Modell und klicken Sie im Kontextmenü auf **[!UICONTROL Train]**. Wählen Sie alternativ ![DataRefresh](/help/assets/icons/DataRefresh.svg) **[!UICONTROL Train]** aus der blauen Aktionsleiste.

   Wählen Sie im Dialogfeld **[!UICONTROL Train model]** die Option aus, um:

   * **[!UICONTROL Train model with last 2 years of marketing data]** oder
   * **[!UICONTROL Train model using specific date range of data]**.
Geben Sie den Datumsbereich an. Sie können den ![Kalender](/help/assets/icons/Calendar.svg) verwenden, um einen Datumsbereich auszuwählen. Sie müssen einen Datenbereich mit mindestens einem Jahr auswählen.

   ![Modell erneut trainieren](../assets/re-train-model.png)

1. Wählen Sie **[!UICONTROL Train]** aus, um das Modell neu zu trainieren.


### Punktzahl oder Neubewertung


Sie können ein Modell inkrementell auf Grundlage neuer Marketing-Daten bewerten oder ein Modell für einen bestimmten Datumsbereich neu bewerten.

Sie sollten ein Modell erneut bewerten, wenn Sie:

* Korrektur falscher Marketing-Daten. Beispielsweise haben die jüngsten Paid-Search-Daten, die Sie in die Schulung und Auswertung des Modells einbezogen haben, eine Woche an Daten verpasst.
* Verwenden Sie neue inkrementelle Marketing-Daten, die durch Aktualisierungen der Datensätze verfügbar geworden sind, die Sie als Teil Ihrer harmonisierten Daten konfiguriert haben.

So bewerten oder bewerten Sie ein Modell neu:

1. Wählen Sie in der linken Leiste ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** aus.

1. Wählen Sie ![Mehr](/help/assets/icons/More.svg) für ein Modell und klicken Sie im Kontextmenü auf **[!UICONTROL Score]**. Wählen Sie alternativ ![DataRefresh](/help/assets/icons/DataRefresh.svg) **[!UICONTROL Score]** aus der blauen Aktionsleiste.

   Wählen Sie im Dialogfeld **[!UICONTROL Score marketing data]** die Option aus, um:

   * **[!UICONTROL Score new marketing data from *mm/dd/yyyy *]**, um Ihr Modell schrittweise anhand neuer Marketing-Daten zu bewerten, oder
   * **[!UICONTROL Score specific date range of marketing data]** , um für einen bestimmten Datumsbereich eine Neubewertung vorzunehmen.
Geben Sie den Datumsbereich an. Sie können den ![Kalender](/help/assets/icons/Calendar.svg) verwenden, um einen Datumsbereich auszuwählen.

   ![Modell erneut trainieren](../assets/re-score-model.png)

1. Wählen Sie **[!UICONTROL Score]** aus. Wenn Sie ein Modell mithilfe eines bestimmten Datenbereichs neu bewerten, wird ein Dialogfeld &quot;**[!UICONTROL Existing model is replaced]**&quot;angezeigt, in dem Sie aufgefordert werden, zu bestätigen, dass das Modell durch neue Werte für den ausgewählten Datumsbereich ersetzt werden soll. Wählen Sie **[!UICONTROL Replace model]** zur Bestätigung aus.


### Modell löschen

So löschen Sie ein Modell:

1. Wählen Sie in der linken Leiste ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** aus.

1. Wählen Sie ![Mehr](/help/assets/icons/More.svg) für ein Modell und klicken Sie im Kontextmenü auf **[!UICONTROL Delete]**. Wählen Sie alternativ ![Löschen](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** aus der blauen Aktionsleiste.

So löschen Sie mehrere Modelle:

1. Auswählen mehrerer Modelle.

1. Wählen Sie in der blauen Aktionsleiste ![Löschen](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** aus, um die Modelle zu löschen.

   >[!WARNING]
   >
   >Das Modell wird sofort gelöscht.


