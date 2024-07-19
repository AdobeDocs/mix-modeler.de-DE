---
title: Modelle
description: Erfahren Sie, wie Sie Modelle in Mix Modeler konfigurieren und verwenden.
feature: Models
exl-id: c43d9bc9-4429-45c2-9247-bd24510a24be
source-git-commit: 9085363e951a4e306c64ad28f56e2c15b4a6029a
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 1%

---

# Modelle

Mit der Modellfunktion in Mix Modeler können Sie KI/ML-Modelle konfigurieren, trainieren und bewerten, die speziell auf Ihre Geschäftsziele abgestimmt sind und durch KI-gestütztes Transferlernen zwischen der Multitouch-Attribution und der Marketing-Mix-Modellierung unterstützt werden.

Die Modelle basieren auf den harmonisierten Daten, die Sie im Rahmen des Mix Modeler-Anwendungs-Workflows erstellen.

Ein Modell in Mix Modeler ist ein Modell für maschinelles Lernen, das verwendet wird, um ein bestimmtes Ergebnis basierend auf den Investitionen eines Marketingexperten zu messen und/oder vorherzusagen. Marketing-Touchpoints und Daten der Zusammenfassungsebene können als Eingabe verwendet werden. Mit Mix Modeler können Sie Varianten von Modellen basierend auf verschiedenen Variablensätzen von Variablen, Dimensionen und Ergebnissen erstellen, z. B. Umsatz, verkaufte Einheiten und Leads.

Ein Modell erfordert:

* eine Konversion,
* einen oder mehrere Marketing-Touchpoints (Kanäle), die aus Zusammenfassungsdaten, Marketing-Touchpoint-Daten (Ereignisdaten) oder beidem bestehen,
* ein konfigurierbares Lookback-Fenster für
* ein konfigurierbares Schulungsfenster.

Ein Modell kann optional Folgendes enthalten:

* externe Faktoren,
* interne Faktoren,
* so genannte &quot;Priors&quot;(Wahrscheinlichkeitsverteilung, die Wissen oder Unsicherheit über Daten vor oder vor der Beobachtung dieser Daten darstellt), die frühere Konversionen nach Kanälen indiziert,
* Ausgabeanteil, der den relativen Ausgabenanteil als Proxy verwendet, wenn die Marketingdaten gering sind.


## Modell erstellen

Verwenden Sie zum Erstellen eines Modells den schrittweisen Konfigurationsfluss des geführten Mix Modelers, der bei Auswahl von **[!UICONTROL Open model canvas]** verfügbar ist. Weitere Informationen finden Sie unter [Erstellen eines Modells](create.md) .

## Modelle verwalten

So zeigen Sie eine Tabelle Ihrer aktuellen Modelle in der Mix Modeler-Benutzeroberfläche an:

1. Wählen Sie in der linken Leiste ![](/help/assets//icons/FileData.svg) **[!UICONTROL Models]** aus.

1. Sie sehen eine Tabelle der aktuellen Modelle.

   Die Tabellenspalten geben Details zum Modell an.

   | Spaltenname | Details |
   |---|---|
   | Name | Name des Modells |
   | Beschreibung | Beschreibung des Modells |
   | Konversionsereignis | Die für das Modell ausgewählte Konversion. |
   | Ausführungshäufigkeit | Die Ausführungsfrequenz des Trainings des Modells. |
   | Letzte Ausführung | Datum und Uhrzeit der letzten Schulung des Modells. |
   | Status | Der Status des letzten Trainings des Modells. <br/><span style="color:green"></span> Erfolg<br/><span style="color:orange"> </span> Schulungsproblem<br/> <span style="color:orange"></span> Warten auf Training <br/><span style="color:red"></span> Fehlgeschlagen <br/><span style="color:gray"></span> _ (wenn ein letzter Lauf in Verarbeitung ist) |

   {style="table-layout:auto"}

1. Um die für die Liste angezeigten Spalten zu ändern, wählen Sie ![Spalteneinstellungen](/help/assets//icons/ColumnSetting.svg) aus und schalten Sie die Spalten auf ![Aktivieren](/help/assets//icons/Checkmark.svg) oder aus.


### Details eines Modells anzeigen

So zeigen Sie weitere Details eines Modells an:

1. Wählen Sie ![Info](/help/assets//icons/Info.svg) für ein Modell aus, um ein Popup mit Details anzuzeigen.



### Modelleinblicke

So zeigen Sie Einblicke in ein Modell in der Mix Modeler-Oberfläche an:

1. Wählen Sie in der linken Leiste ![](/help/assets//icons/FileData.svg) **[!UICONTROL Models]** aus.

1. Wählen Sie den Namen eines Modells mit dem Wert **[!UICONTROL Last run status]** von <span style="color:green"></span> aus. **[!UICONTROL Success]** aus der Tabelle **[!UICONTROL Models]**. Modelleinblicke sind nur für erfolgreich trainierte Modelle verfügbar.

1. Wählen Sie im Kontextmenü **[!UICONTROL Model Insights]** aus. Sie werden zu [Model Insights](insights.md) umgeleitet.


### Neubewertung


So bewerten Sie ein Modell in der Mix Modeler-Oberfläche neu:

1. Wählen Sie in der linken Leiste ![](/help/assets//icons/FileData.svg) **[!UICONTROL Models]** aus.

1. Wählen Sie den Namen eines Modells mit dem Wert **[!UICONTROL Last run status]** von <span style="color:green"></span> aus. **[!UICONTROL Success]** aus der Tabelle **[!UICONTROL Models]**. Die Neubewertung ist nur für erfolgreich trainierte Modelle verfügbar.

1. Wählen Sie im Kontextmenü **[!UICONTROL Re-score]** aus. Es kann einige Minuten dauern, bis ein aktualisierter Status für das Modell angezeigt wird.


### Modell löschen

So löschen Sie ein Modell:

1. Wählen Sie den Namen des Modells aus, das Sie löschen möchten.

1. Wählen Sie im Kontextmenü **[!UICONTROL Delete]** aus, um das Modell zu löschen.

   >[!WARNING]
   >
   >Das Modell wird sofort gelöscht.


