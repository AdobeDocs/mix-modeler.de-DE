---
title: Modelle - Übersicht
description: Erfahren Sie, wie Sie in Mix Modeler Modelle erstellen und verwenden.
feature: Models
exl-id: c43d9bc9-4429-45c2-9247-bd24510a24be
source-git-commit: 85f9b42a775006cd3566447b2bb9d0a806fa3e73
workflow-type: tm+mt
source-wordcount: '1174'
ht-degree: 1%

---

# Modelle - Übersicht

Mit der Modellfunktion in Mix Modeler können Sie Modelle konfigurieren, trainieren und bewerten, die speziell auf Ihre Geschäftsziele zugeschnitten sind. Das Training und Scoring unterstützt KI-gestütztes Transferlernen zwischen Multitouch-Attribution und Marketing-Mix-Modellierung.

Die Modelle basieren auf den harmonisierten Daten, die Sie im Rahmen des Workflows der Mix Modeler-Anwendung erstellen.

Ein Modell in Mix Modeler ist ein maschinelles Lernmodell, mit dem ein bestimmtes Ergebnis anhand der Investitionen eines Marketing-Experten gemessen und vorhergesagt werden kann. Marketing-Touchpoints und Daten auf Zusammenfassungsebene können als Eingabe verwendet werden. Mit Mix Modeler können Sie Varianten von Modellen erstellen, die auf verschiedenen Variablensätzen, Dimensionen und Ergebnissen basieren, z. B. Umsatz, verkaufte Einheiten, Leads.

Ein Modell erfordert:

* Eine Konversion.
* Ein oder mehrere Marketing-Touchpoints (Kanäle), die aus Daten auf Zusammenfassungsebene, Marketing-Touchpoint-Daten (Ereignisdaten) oder beidem bestehen.
* Ein konfigurierbares Lookback-Fenster.
* Ein konfigurierbares Trainings-Fenster.

Ein Modell kann optional Folgendes enthalten:

* Externe Faktoren.
* Interne Faktoren.
* Vorkenntnisse von Marketing-Beiträgen aus anderen Quellen wie Erfahrungen mit früheren Stakeholdern, inkrementelle Tests und andere Modelle.
* Ausgabenanteil, der den relativen Ausgabenanteil als Proxy verwendet, wenn die Marketing-Daten spärlich sind.

Wenn ein Modell zum ersten Mal erstellt wird, startet die Erstellung sofort den Trainings- und Bewertungsprozess. Nach Abschluss des anfänglichen Trainings- und Scoring-Durchgangs stehen Modelleinblicke zur Überprüfung zur Verfügung. Ein Modell kann anschließend neu trainiert werden. Außerdem können Daten zum Modell hinzugefügt werden, sodass Sie das Modell manuell neu bewerten müssen. Umschulung und Neubewertung sind ein iterativer Prozess, da neue Erkenntnisse und Informationen auftauchen und Anpassungen erforderlich sind, um eine Modellanpassung zu erhalten, die für Ihre Geschäftsziele am besten geeignet ist.


## Erstellen von Modellen

Verwenden Sie zum Erstellen eines Modells den Schritt-für-Schritt-Konfigurationsablauf für Mix Modeler-Modelle, der bei der Auswahl von **[!UICONTROL Open model canvas]** verfügbar ist. Weitere [ finden Sie unter ](build.md) von Modellen .

## Modelle verwalten

So zeigen Sie eine Tabelle Ihrer aktuellen Modelle in der Benutzeroberfläche von Mix Modeler an:

1. Wählen Sie in der linken Leiste ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** aus.

1. Eine Tabelle der aktuellen Modelle wird angezeigt.

   Die Tabellenspalten geben Details zum Modell an.

   | Spaltenname | Details |
   |---|---|
   | Name | Modellname |
   | Beschreibung | Beschreibung des Modells |
   | Konversionsereignis | Die für das Modell ausgewählte Konvertierung. |
   | Ausführungshäufigkeit | Die Lauffrequenz des Trainings des Modells. |
   | Letzte Ausführung | Datum und Uhrzeit des letzten Trainings des Modells. |
   | Status | Der Status des Modells. |

   {style="table-layout:auto"}

   Der gemeldete Status des Modells hängt davon ab, wo sich ein Modell innerhalb seines Lebenszyklus befindet. Ob beispielsweise ein Modell erstellt, erfolgreich (neu) trainiert wurde oder nicht oder ob die Bewertung erfolgreich (neu) erstellt wurde oder nicht.

   In der folgenden Tabelle:

   * ![Häkchen](/help/assets/icons/Checkmark.svg) - zeigt eine erfolgreiche Ausführung eines Schritts im Modelllebenszyklus an.
   * ![Uhr](/help/assets/icons/Clock.svg) - zeigt die aktuelle Ausführung eines Schritts im Modelllebenszyklus an.
   * ![Schließen](/help/assets/icons/Close.svg) - zeigt eine fehlgeschlagene Ausführung eines Schritts im Modelllebenszyklus an.

   | Status | Erstellen | trainieren | Ergebnis | umschulen | neu bewerten |
   |---|:---:|:---:|:---:|:---:|:---:|
   | In Bearbeitung | ![Häkchen](/help/assets/icons/Checkmark.svg) | | | | |
   | In Bearbeitung | ![Häkchen](/help/assets/icons/Checkmark.svg) | ![Uhr](/help/assets/icons/Clock.svg) | | | |
   | In Bearbeitung | ![Häkchen](/help/assets/icons/Checkmark.svg) | ![Häkchen](/help/assets/icons/Checkmark.svg) | ![Uhr](/help/assets/icons/Clock.svg) | | |
   | In Bearbeitung | ![Häkchen](/help/assets/icons/Checkmark.svg) | ![Häkchen](/help/assets/icons/Checkmark.svg) | ![Häkchen](/help/assets/icons/Checkmark.svg) | ![Uhr](/help/assets/icons/Clock.svg) | |
   | In Bearbeitung | ![Häkchen](/help/assets/icons/Checkmark.svg) | ![Häkchen](/help/assets/icons/Checkmark.svg) | ![Häkchen](/help/assets/icons/Checkmark.svg) | ![Häkchen](/help/assets/icons/Checkmark.svg) | ![Uhr](/help/assets/icons/Clock.svg) |
   | Training failed | ![Häkchen](/help/assets/icons/Checkmark.svg) | ![Schließen](/help/assets/icons/Close.svg) | | | |
   | Training failed | ![Häkchen](/help/assets/icons/Checkmark.svg) | ![Häkchen](/help/assets/icons/Checkmark.svg) | ![Häkchen](/help/assets/icons/Checkmark.svg) | ![Schließen](/help/assets/icons/Close.svg) | |
   | Training successful | ![Häkchen](/help/assets/icons/Checkmark.svg) | ![Häkchen](/help/assets/icons/Checkmark.svg) | | | |
   | Training successful | ![Häkchen](/help/assets/icons/Checkmark.svg) | ![Häkchen](/help/assets/icons/Checkmark.svg) | ![Häkchen](/help/assets/icons/Checkmark.svg) | ![Häkchen](/help/assets/icons/Checkmark.svg) | |
   | Bewertung fehlgeschlagen | ![Häkchen](/help/assets/icons/Checkmark.svg) | ![Häkchen](/help/assets/icons/Checkmark.svg) | ![Schließen](/help/assets/icons/Close.svg) | | |
   | Bewertung fehlgeschlagen | ![Häkchen](/help/assets/icons/Checkmark.svg) | ![Häkchen](/help/assets/icons/Checkmark.svg) | ![Häkchen](/help/assets/icons/Checkmark.svg) | ![Häkchen](/help/assets/icons/Checkmark.svg) | ![Schließen](/help/assets/icons/Close.svg) |
   | Bewertung erfolgreich | ![Häkchen](/help/assets/icons/Checkmark.svg) | ![Häkchen](/help/assets/icons/Checkmark.svg) | ![Häkchen](/help/assets/icons/Checkmark.svg) | | |
   | Bewertung erfolgreich | ![Häkchen](/help/assets/icons/Checkmark.svg) | ![Häkchen](/help/assets/icons/Checkmark.svg) | ![Häkchen](/help/assets/icons/Checkmark.svg) | ![Häkchen](/help/assets/icons/Checkmark.svg) | ![Häkchen](/help/assets/icons/Checkmark.svg) |

   {style="table-layout:fixed"}

1. Um die für die Liste angezeigten Spalten zu ändern, wählen Sie ![Spalteneinstellungen](/help/assets/icons/ColumnSetting.svg) aus und schalten Sie die Spalten ein ![Aktivieren](/help/assets/icons/Checkmark.svg) oder aus.

Sie können die folgenden Aktionen für ein bestimmtes Modell ausführen.

### Modelleinblicke

Die Funktion Modelleinblicke ist nur für erfolgreich trainierte und bewertete Modelle verfügbar.

So zeigen Sie die Insights eines Modells an:

1. Wählen Sie in der linken Leiste ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** aus.

1. Wählen Sie den Modellnamen.

Sie werden zu &quot;[ Insights“ ](insights.md).


### Details anzeigen

So zeigen Sie weitere Details zu einem Modell an:

1. Wählen Sie in der linken Leiste ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** aus.

1. Wählen Sie ![Info](/help/assets/icons/Info.svg) für ein Modell aus, um ein Popup mit Details anzuzeigen.


### Duplizieren

Sie können ein Modell schnell duplizieren.

1. Wählen Sie in der linken Leiste ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** aus.

1. Wählen Sie ![Mehr](/help/assets/icons/More.svg) für ein Modell aus und wählen Sie im Kontextmenü **[!UICONTROL Duplicate]** aus.

Sie werden zu den Schritten zum Erstellen eines neuen Modells weitergeleitet, wobei ein vorgeschlagener Name aus dem Namen des ursprünglichen Modells mit **[!UICONTROL (Copy)](_)_ wird**.

### Bearbeiten

Sie können den Namen, die Beschreibung und den Zeitplan für das Training und die Bewertung eines Modells bearbeiten.

1. Wählen Sie in der linken Leiste ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** aus.

1. Wählen Sie ![Mehr](/help/assets/icons/More.svg) für ein Modell aus und wählen Sie im Kontextmenü **[!UICONTROL Edit]** aus.

   Im Dialogfeld **[!UICONTROL Edit model]** :

   * Geben Sie einen neuen **[!UICONTROL Name]** und eine neue **[!UICONTROL Description]** ein.

   * Um die Zeitplanung zu aktivieren, aktivieren Sie **[!UICONTROL Status]**. Sie können die Planung nur für Modelle aktivieren, die trainiert und bewertet wurden.

      1. **[!UICONTROL Scoring frequency]** auswählen:

         * **[!UICONTROL Daily]**: Geben Sie eine gültige Zeit ein (z. B. `05:22 pm`) oder verwenden Sie ![Uhr](/help/assets/icons/Clock.svg).
         * **[!UICONTROL Weekly]**: Wählen Sie einen Wochentag aus und geben Sie eine gültige Zeit ein (z. B. `05:22 pm`) oder verwenden Sie ![Uhr](/help/assets/icons/Clock.svg).
         * **[!UICONTROL Monthly]**: Wählen Sie einen Tag des Monats aus dem Dropdown-Menü Ausführen für jedes Dropdown-Menü aus und geben Sie eine gültige Zeit ein (z. B. `05:22 pm`) oder verwenden Sie ![Uhr](/help/assets/icons/Clock.svg).

      1. Wählen Sie eine **[!UICONTROL Training frequency]** aus dem Dropdown-Menü aus: **[!UICONTROL Monthly]**, **[!UICONTROL Quarterly]**, **[!UICONTROL Yearly]** oder **[!UICONTROL None]**.

     ![Modell bearbeiten](../assets/model-edit.png)

1. Wählen Sie **[!UICONTROL Save]** aus.



### umschulen

Ein Modell neu trainieren ist nur für erfolgreich trainierte Modelle verfügbar.

Ziehen Sie in Erwägung, ein Modell neu zu trainieren, wenn Sie Folgendes tun möchten:

* Neue inkrementelle Marketing- und Faktordaten einschließen. Im letzten Quartal hat sich beispielsweise die Marktdynamik verändert oder Ihre Marketing-Datenverteilung hat sich erheblich verändert.

So trainieren Sie ein Modell neu:

1. Wählen Sie in der linken Leiste ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** aus.

1. Wählen Sie ![Mehr](/help/assets/icons/More.svg) für ein Modell aus und wählen Sie im Kontextmenü **[!UICONTROL Train]** aus. Wählen Sie alternativ ![DataRefresh](/help/assets/icons/DataRefresh.svg)-**[!UICONTROL Train]** in der blauen Aktionsleiste aus.

   Wählen Sie im Dialogfeld **[!UICONTROL Train model]** die Option aus, um:

   * **[!UICONTROL Train model with last 2 years of marketing data]** oder
   * **[!UICONTROL Train model using specific date range of data]**.
Geben Sie den Datumsbereich an. Sie können den ![Kalender“ verwenden](/help/assets/icons/Calendar.svg) um einen Datumsbereich auszuwählen. Es muss ein Datenbereich mit mindestens einem Jahr ausgewählt werden.

   ![Modell neu trainieren](../assets/retrain-model.png)

1. Wählen Sie **[!UICONTROL Train]** aus, um das Modell neu zu trainieren.


### Punktzahl oder Punktzahl


Sie können ein Modell inkrementell auf der Grundlage neuer Marketing-Daten bewerten oder ein Modell für einen bestimmten Datumsbereich neu bewerten.

Erwägen Sie, ein Modell neu zu bewerten, wenn Sie Folgendes tun möchten:

* Korrigieren Sie falsche Marketing-Daten. Beispielsweise fehlten für die Daten der letzten Paid Search, die Sie in das Training und die Bewertung des Modells eingeschlossen haben, eine Woche Daten.
* Verwenden Sie neue inkrementelle Marketing-Daten, die durch Aktualisierungen in den Datensätzen verfügbar geworden sind, die Sie als Teil Ihrer harmonisierten Daten konfiguriert haben.

So bewerten Sie ein Modell:

1. Wählen Sie in der linken Leiste ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** aus.

1. Wählen Sie ![Mehr](/help/assets/icons/More.svg) für ein Modell aus und wählen Sie im Kontextmenü **[!UICONTROL Score]** aus. Wählen Sie alternativ ![DataRefresh](/help/assets/icons/DataRefresh.svg)-**[!UICONTROL Score]** in der blauen Aktionsleiste aus.

   Wählen Sie im Dialogfeld **[!UICONTROL Score marketing data]** die Option aus, um:

   * **[!UICONTROL Score new marketing data from *MM/TT/JJJJ *]**, um Ihr Modell inkrementell mithilfe neuer Marketing-Daten zu bewerten, oder
   * **[!UICONTROL Score specific date range of marketing data]** für einen bestimmten Datumsbereich neu bewertet werden.
Geben Sie den Datumsbereich an. Sie können den ![Kalender“ verwenden](/help/assets/icons/Calendar.svg) um einen Datumsbereich auszuwählen.

   ![Erneutes Bewerten eines Modells](../assets/rescore-model.png)

1. Wählen Sie **[!UICONTROL Score]** aus. Wenn Sie ein Modell mit einem bestimmten Datenbereich neu bewerten, wird ein **[!UICONTROL Existing model is replaced]** Dialogfeld angezeigt, in dem Sie aufgefordert werden zu bestätigen, dass Sie das Modell durch neue Bewertungen für den ausgewählten Datumsbereich ersetzen möchten. Wählen Sie zur Bestätigung **[!UICONTROL Replace model]** aus.


### Modelle löschen

Löschen eines Modells:

1. Wählen Sie in der linken Leiste ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** aus.
1. Wählen Sie ![Mehr](/help/assets/icons/More.svg) für ein Modell aus und wählen Sie im Kontextmenü **[!UICONTROL Delete]** aus. Wählen Sie alternativ ![ blaue Aktionsleiste ](/help/assets/icons/Delete.svg)Löschen“ **[!UICONTROL Delete]**.
1. Wählen Sie **[!UICONTROL Delete]** im Bestätigungsdialogfeld **[!UICONTROL Delete model]** aus, um das Modell zu löschen. Wählen Sie zum Abbrechen **[!UICONTROL Cancel]** aus.

So löschen Sie mehrere Modelle:

1. Mehrere Modelle auswählen.
1. Wählen Sie in der blauen Aktionsleiste die Option ![Löschen](/help/assets/icons/Delete.svg) aus, **[!UICONTROL Delete]** die Modelle zu löschen.
1. Wählen Sie **[!UICONTROL Delete]** im Bestätigungsdialogfeld **[!UICONTROL Delete *x *-Modelle]**, um die Modelle zu löschen. Wählen Sie zum Abbrechen **[!UICONTROL Cancel]**aus.

