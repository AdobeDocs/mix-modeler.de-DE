---
title: Model Insights
description: Erfahren Sie, wie Sie Details zu Ihrem Modell erhalten, z. B. historische Übersicht, Modelleinblicke und Modellqualität in Mix Modeler.
feature: Models
exl-id: d99852f9-ba0d-4a2e-b5f3-ca0efe6002fd
source-git-commit: 4f4c7f05e90d73a0ab4865150b1ec4c2af88fc12
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 0%

---

# Model Insights

So zeigen Sie Modelleinblicke im ![Modelle](../assets/icons/FileData.svg) **[!UICONTROL Models]** -Schnittstelle in Mix Modeler:

1. Wählen Sie den Namen eines Modells mit einer **[!UICONTROL Last run status]** von <span style="color:green">●</span> **[!UICONTROL Success]** aus dem **[!UICONTROL Models]** Tabelle.

1. Wählen Sie im Kontextmenü die Option **[!UICONTROL Model Insights]**.

Sie sehen, wann das angegebene Modell zuletzt aktualisiert wurde und Widgets mit drei Registerkarten angezeigt werden: Historische Übersicht, Modelleinblicke und Modellqualität.

Sie können den Datumsbereich ändern, auf dem die Widgets auf den einzelnen Registerkarten basieren. Geben Sie einen Datumsbereich ein oder wählen Sie ![Kalender](../assets/icons/Calendar.svg) , um einen Datumsbereich auszuwählen.


## Historische Übersicht

Die Registerkarte Historische Übersicht zeigt Widgets für:

* Konversion und Ausgaben nach Fiscal Qtr und Produkt.

* Ausgaben nach Kanal

* Touchpoint-Ausgaben.

  Sie können einen alternativen ausgabenbasierten Kanal auswählen, der für dieses Widget angezeigt werden soll. Wählen Sie einen Kanal aus **[!UICONTROL Channels]**.

* Touchpoint-Lautstärke.

  Sie können einen alternativen volumenbasierten Kanal auswählen, der für dieses Widget angezeigt werden soll. Wählen Sie einen Kanal aus **[!UICONTROL Channels]**.

![Modell - Historische Übersicht](../assets/model-historical-overview.png)

## Modelleinblicke

Auf der Registerkarte Modelleinblicke werden Widgets für Folgendes angezeigt:

* Beitrag nach Datum und Basismedien Das gestapelte Diagramm ist geordnet: unten, in der Mitte die Kanäle ohne Ausgaben und oben die Kanäle für die Ausgabe.

* Beitrag nach Kanal

* Marketing-Leistungszusammenfassung.

* Kurven für die Randantwort.

![Modell - Modelleinblicke](../assets/model-model-insights.png)

Sie können den Mauszeiger über einzelne Diagrammelemente in jedem Widget bewegen, um ein Popover mit weiteren Details anzuzeigen.

Um eine CSV-Datei mit den Daten für das Widget herunterzuladen, wählen Sie ![Herunterladen](../assets/icons/Download.svg).

Um vollständige Modelleinblicke-Daten im Microsoft® Excel-Format herunterzuladen, wählen Sie ![Herunterladen](../assets/icons/Download.svg) **[!UICONTROL Download data]**.


## Modellqualität

![Modellqualitätsbeurteilung](/help/assets/model-quality-assessment.png)
Auf der Registerkarte Modellqualität wird eine

* [!UICONTROL Model Assessment] Visualisierung, die Sie auf tatsächliche oder prognostizierte oder Restkonversionen aufschlüsseln können.

  Um die Visualisierung aufzuschlüsseln, wählen Sie **[!UICONTROL Actual vs. Predicted]** oder **[!UICONTROL Residuals]** aus dem **[!UICONTROL Breakdown]** Liste.

* [!UICONTROL Model fitting metrics] -Tabelle mit den folgenden Spalten für jede Konversionsmetrik:

   * Tatsächliche Konversion

   * Modellierte Konversion

   * Restkonvertierung (Differenz zwischen tatsächlicher und modellierter Konversion)

   * Modellqualitätswerte:

      * R2 (R-squared), das angibt, wie gut die Daten zum Regressionsmodell passen (die Anpassungsgüte).

      * MAPE (Mean Absolute Percentage Error), einer der am häufigsten verwendeten KPIs zur Messung der Prognosegenauigkeit und zum Ausdruck des Prognosefehlers als Prozentsatz des tatsächlichen Werts.

      * RMSE (Root Mean Square Error): Zeigt den durchschnittlichen &quot;Fehler&quot;an, gewichtet nach dem Quadrat des Fehlers.

  Um eine CSV-Datei herunterzuladen, die die Daten für die Tabelle enthält, wählen Sie ![Herunterladen](../assets/icons/Download.svg).
