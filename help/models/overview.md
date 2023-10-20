---
title: Modelle
description: Erfahren Sie, wie Sie Modelle in Mix Modeler konfigurieren und verwenden.
feature: Models
exl-id: c43d9bc9-4429-45c2-9247-bd24510a24be
source-git-commit: f445cb2b1ec04ffe9247e858c048587802bffe9c
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 2%

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

Verwenden Sie zum Erstellen eines Modells den Schritt-für-Schritt-Konfigurationsfluss des geführten Mix Modelers, der bei Auswahl von **[!UICONTROL Guide me]**. Siehe [Modell erstellen](create.md) für weitere Details.

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
