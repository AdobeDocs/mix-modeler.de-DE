---
title: Datensätze harmonisieren - Übersicht
description: Erfahren Sie, wie Sie Daten in Mix Modeler harmonisieren.
feature: Harmonized Data
exl-id: 6cb70762-e3b2-46a0-b028-1d6daf3edae5
source-git-commit: 83ccceb5f8b73157048ed17b190194de4ed05c4f
workflow-type: tm+mt
source-wordcount: '1347'
ht-degree: 7%

---

# Datensätze harmonisieren - Übersicht

Die Daten in Mix Modeler sind je nach Datenquelle unterschiedlich. Die Daten können wie folgt sein:

* aggregierte oder zusammengefasste Daten, z. B. Daten aus Datenquellen von Walled Garden oder Offline-Werbedaten (wie Ausgaben), die bei der Ausführung einer Reklametafel, eines Ereignisses oder einer physischen Werbekampagne gesammelt wurden,
* Ereignisdaten, z. B. aus Erstanbieter-Datenquellen. Bei diesen Ereignisdaten kann es sich um Daten handeln, die über den Adobe Analytics-Quell-Connector von Adobe Analytics oder über die Experience Platform Web- oder Mobile-SDK- oder Edge Network-API erfasst werden, oder um Daten, die über Quell-Connectoren aufgenommen werden.

Der Harmonisierungsdienst von Mix Modeler nimmt die Aggregat- und Ereignisdaten in eine konsistente Datenansicht auf. Diese Datenansicht ist die Quelle für die Modelle in Mix Modeler. Der Service verwendet die höchste Granularität über die verschiedenen Datensätze hinweg. Wenn beispielsweise ein Datensatz eine Granularität von monatlichen Datensätzen hat und die übrigen Datensätze eine wöchentliche und tägliche Granularität haben, erstellt der Harmonisierungs-Service eine Datenansicht mit monatlicher Granularität.

## Faktoren

Faktoren sind für die Modellerstellung von entscheidender Bedeutung, und Sie möchten verstehen, welche Auswirkungen das Geschäft ganzheitlich hat. Faktoren stehen möglicherweise nicht in Zusammenhang mit Marketing-Daten.

* Interne Faktoren sind spezifisch für Ihr Unternehmen und können sich auf Ihre Konversionen auswirken. Beispielsweise Ihre Verkaufssaison, Werbeaktionen und mehr.

* Externe Faktoren sind Faktoren, die sich der Kontrolle Ihres Unternehmens entziehen, die sich jedoch weiterhin auf die von Ihnen erzielten Konversionen auswirken können. Beispiele sind CPI, S&amp;P 500 und mehr.

Die Factors-Funktion in Mix Modeler verwendet einen harmonisierten Faktoren-Workflow. Dieser Workflow vereinfacht die Verwaltung von Faktoren, sorgt für Konsistenz über Modelle hinweg und bietet ein intuitives Erlebnis.

Im Rahmen des Workflows Harmonisierte Faktoren gilt Folgendes:

1. Definieren harmonisierter Felder für Faktoren aus einem Faktordatensatz in [Datensatzregeln](/help/harmonize-data/dataset-rules.md#create-a-dataset-rule).
1. [Synchronisieren](/help/harmonize-data/dataset-rules.md#sync-data) Sie Ihre harmonisierten Daten.
1. [Verwenden Sie die Faktoren](/help/models/build.md#configure) in Ihrer Modellkonfiguration.

### Migration

Möglicherweise verfügen Sie über Modelle, die den Workflow für harmonisierte Faktoren noch nicht übernommen haben, und verwenden Sie den Workflow für Datensatzfaktoren von Experience Platform. Diese Modelle zeigen weiterhin ihre ursprünglichen, auf dem Datensatz basierenden Faktoren an, bis die Modelle mit neuen Faktoren aktualisiert werden, die auf dem harmonisierten Faktoren-Workflow basieren.

Wenn Sie ein Modell duplizieren, das den Workflow Datensatzbasierte Faktoren verwendet:

* Wenn das Modell nicht harmonisiert wurde, wird die alte Faktor-Konfiguration nicht in das duplizierte Modell übernommen. Sie müssen Faktoren mithilfe des neuen Workflows Harmonisierte Faktoren hinzufügen.
* Wurde das Modell harmonisiert, so werden Faktoren übernommen und beibehalten oder aktualisiert.

## Beispiel für harmonisierte Daten

Angenommen, Sie haben die folgenden Datensätze für Mix Modeler verfügbar.

**Datensatz 1**

Enthält den Marketing-Aufwandsdatensatz von YouTube mit einer Granularität des Aggregatdatensatzes von täglich.

| Datum | Datumstyp | Kanal | Campaign | Marke | Geo | Klicks | Ausgaben |
|---|:--:|---|---|---|---|---:|---:|
| 12-31-2021 | day | YouTube | y_fall_02 | BrandX | US | 10000 | 100 |
| 01-01-2022 | day | YouTube | y_fall_02 | BrandX | US | 1.000 | 10 |
| 01-03-2022 | day | YouTube | y_fall_01 | BrandY | CA | 10000 | 100 |
| 01-04-2022 | day | YouTube | Y_SUMMER_01 | Null | CA | 9000 | 80 |

{style="table-layout:auto"}


**Datensatz 2**

Enthält den Marketing-Aufwand-Datensatz von Facebook mit einer Granularität des aggregierten Datensatzes von „Wöchentlich“.

| Datum | Datumstyp | Kanal | Campaign | Geo | Klicks | Ausgaben |
|--- |:---:|--- |---|---|---:|---:|
| 01-01-2022 | Woche | Facebook | FB_FALL_01 | US | 8000 | 100 |
| 01-08-2022 | Woche | Facebook | FB_FALL_02 | US | 1.000 | 10 |
| 01-08-2022 | Woche | Facebook | FB_FALL_01 | US | 7000 | 100 |
| 01-16-2022 | Woche | Facebook | FB_Summer_01 | CA | 10000 | 80 |

{style="table-layout:auto"}


**Datensatz 3**

Ein Konversionsdatensatz mit einer Granularität des Aggregatdatensatzes von täglich.

| Datum | Datumstyp | Geo | Ziel | Einnahmen |
|--- |:---: |---|---|---:|
| 01-01-2022 | day | US | Mode | 200 |
| 01-08-2022 | day | US | Mode | 10 |
| 01-08-2022 | day | US | Schmuck | 1100 |
| 01-16-2022 | day | CA | Schmuck | 80 |

{style="table-layout:auto"}


**Datensatz 4**

Ein Beispiel für einen Erlebnisereignis-Datensatz (Web SDK Events) des Kunden.

| Zeitstempel | Identity-Namespace | Identitäts-ID | Kanal | Klicks |
|--- |--- |--- |--- |---:|
| 01-01-2022 00:01:01.000 | ECID | 64FD46FF-8C63-43B4-85A7-92B953113BA0 | CSE | 1 |
| 01-01-2022 00:01:01.000 | ECID | 64FD46FF-8C63-43B4-85A7-92B953113BA0 | CSE | 1 |
| 01-08-2022 00:01:01.000 | ECID | 2CA2A16E-CAF0-4FA9-9A8B-9774B39547C4 | CSE | 1 |
| 01-08-2022 00:01:01.000 | ECID | 5CE99BFB-E44A-40D9-B8CD-C5408BDA7CDC | CSE | 1 |

{style="table-layout:auto"}


Sie möchten einen harmonisierten Datensatz mit einer Granularität von auf wöchentlich erstellen. Die Ereignisdaten werden zur Granularität einer Woche aggregiert und zum harmonisierten Datensatz hinzugefügt. Das Ergebnis lautet:

**Harmonisierter Datensatz**

| Datum | Datumstyp | Kanal | Campaign | Marke | Geo | Ziel | Klicks | Ausgaben | Einnahmen |
|--- |:---:|--- |--- |--- |---|---|---:|---:|---:|
| 12-27-2021 | Woche | YouTube | y_fall_02 | BrandX | US | Null | 11000 | 110 | Null |
| 01-03-2022 | Woche | YouTube | y_fall_01 | BrandY | CA | Null | 10000 | 100 | Null |
| 01-03-2022 | Woche | YouTube | Y_SUMMER_01 | Null | CA | Null | 9000 | 80 | Null |
| 01-01-2022 | Woche | Facebook | FB_FALL_01 | Null | US | Null | 8000 | 100 | Null |
| 01-08-2022 | Woche | Facebook | FB_FALL_02 | Null | US | Null | 1.000 | 10 | Null |
| 01-08-2022 | Woche | Facebook | FB_FALL_01 | Null | US | Null | 7000 | 100 | Null |
| 01-16-2022 | Woche | Facebook | FB_Summer_01 | Null | CA | Null | 10000 | 80 | Null |
| 12-27-2021 | Woche | Null | Null | Null | US | Mode | Null | Null | 200 |
| 01-03-2022 | Woche | Null | Null | Null | US | Mode | Null | Null | 10 |
| 01-03-2022 | Woche | Null | Null | Null | US | Schmuck | Null | Null | 1100 |
| 01-10-2022 | Woche | Null | Null | Null | CA | Schmuck | Null | Null | 80 |
| 01-01-2022 | Woche | CSE | Null | Null | Null | Null | 2 | Null | Null |
| 01-08-2022 | Woche | CSE | Null | Null | Null | Null | 2 | Null | Null |

{style="table-layout:auto"}


## Harmonisierte Daten einrichten

Um einen harmonisierten Datensatz zu erstellen, wie im vereinfachten [Beispiel](#an-example-of-harmonized-data), müssen Sie die folgenden Schritte ausführen:

1. Definieren Sie zusätzliche [harmonisierte Felder](fields.md) die Sie über die bereits verfügbaren globalen harmonisierten Felder hinaus verwenden möchten.
1. Richten Sie [Datensatzregeln](dataset-rules.md) ein, um Felder aus Ihren Aggregat- oder Erlebnisereignis-Datensätzen harmonisierten Feldern zuzuordnen.
1. Definieren Sie [Marketing-Touchpoints](marketing-touchpoints.md) mithilfe der von Ihnen definierten standardmäßigen und zusätzlichen harmonisierten Felder.
1. Definieren Sie [Konversionen](conversions.md) mithilfe der von Ihnen definierten standardmäßigen und zusätzlichen harmonisierten Felder.


## Anzeigen harmonisierter Daten

So zeigen Sie Ihre harmonisierten Daten in der Benutzeroberfläche von Mix Modeler an:

1. Wählen Sie ![DataSearch](/help/assets/icons/DataCheck.svg)-**[!UICONTROL Harmonized datasets]** in der linken Leiste aus.

1. Wählen Sie **[!UICONTROL Harmonized data]** in der oberen Leiste aus. Anhand der Felder, Datensatzregeln, Marketing-Touchpoints und Konversionen, die Sie definiert haben, wird eine Zusammenfassung Ihrer harmonisierten Daten angezeigt.

   1. Um den Zeitraum neu zu definieren, auf dem die Zusammenfassung harmonisierter Daten basiert, geben Sie einen Datumsbereich für die **[!UICONTROL Date range]** ein oder verwenden Sie ![Kalender](/help/assets/icons/Calendar.svg), um einen Datenbereich auszuwählen.

   1. Um die harmonisierten Feldspalten zu ändern, die für die harmonisierte Datentabelle angezeigt werden, öffnen Sie ![ Dialogfeld &quot;](/help/assets/icons/Setting.svg)&quot; **[!UICONTROL Column settings]** Einstellungen“.

      1. Wählen Sie ![SelectBox](/help/assets/icons/SelectBox.svg) eine oder mehrere Spalten aus **[!UICONTROL AVAILABLE COLUMNS]** aus und verwenden Sie ![Pfeil nach rechts](/help/assets/icons/ChevronRight.svg), um diese Spalten **[!UICONTROL SELECTED COLUMNS]** hinzuzufügen.

      1. Wählen Sie ![SelectBox](/help/assets/icons/SelectBox.svg) eine oder mehrere Spalten aus **[!UICONTROL SELECTED COLUMNS]** aus und verwenden Sie ![Pfeil nach links](/help/assets/icons/ChevronLeft.svg), um die ausgewählten Spalten zu entfernen und an **[!UICONTROL AVAILABLE COLUMNS]** zurückzugeben.

      1. Wählen Sie eine Spalte aus der **[!UICONTROL DEFAULT SORT]** aus und wechseln Sie zwischen **[!UICONTROL Ascending]** oder **[!UICONTROL Descending]**.

      1. Um die Reihenfolge der angezeigten Spalten zu ändern, können Sie eine Spalte **[!UICONTROL SELECTED COLUMNS]** per Drag-and-Drop nach oben und unten verschieben .

   1. Wählen Sie **[!UICONTROL Submit]** aus, um Ihre Änderungen an den Spalteneinstellungen zu übermitteln. Wählen Sie **[!UICONTROL Close]** aus, um alle vorgenommenen Änderungen zu verwerfen.

1. Wenn mehr Seiten verfügbar sind, verwenden Sie ![Pfeil links](/help/assets/icons/ChevronLeft.svg) oder ![Pfeil rechts](/help/assets/icons/ChevronRight.svg) um **[!UICONTROL Page _x _von_x_]**, um zwischen Seiten zu wechseln.

1. Sie können optional die harmonisierten Daten herunterladen.

   1. Wählen Sie ![Download](/help/assets/icons/Download.svg) [!BADGE Beta] aus.
   1. Wählen Sie im Popup die Option ![Kreis hinzufügen](/help/assets/icons/AddCircle.svg) **[!UICONTROL Create]**.
   1. Geben Sie einen **[!UICONTROL Report name]** ein, z. B. `Test Report`.
   1. Wählen Sie ![FileCSV](/help/assets/icons/FileCSV.svg)-**[!UICONTROL Report]** aus.

   Ein CSV-Bericht mit einem Titel, der auf Ihrem angegebenen Berichtsnamen und dem aktuellen Datum und der aktuellen Uhrzeit (z. B. `Test Report_2025_04_23_9-5-18.csv`) basiert, wird in den standardmäßigen Download-Ordner heruntergeladen.


## Best Practices

Wenden Sie beim Erstellen Ihres harmonisierten Datensatzes die folgenden Best Practices an.

### Schema

* Vermeiden Sie Datentypkonflikte. Es treten Abweichungen auf, wenn der Datentyp eines Felds in den Datensätzen Ihrer aufgenommenen Datensätze nicht mit dem Datentyp übereinstimmt, den Sie für dieses Feld im zugrunde liegenden Schema konfiguriert haben.
* Vermeiden Sie falsche Schematypen. Beim Versuch, einen bestimmten Datentyp mit einem Datensatz aufzunehmen, der nicht mit dem Schema für diese Daten übereinstimmt, treten falsche Schematypen auf. Sie versuchen beispielsweise, Zusammenfassungsdaten mithilfe eines externen Faktordatensatzes aufzunehmen.

### Daten-Mapping

* Stellen Sie sicher, dass Sie die Identitäten für jeden Ereignisdatensatz ordnungsgemäß eingerichtet haben.

### Datenqualität

* Stellen Sie sicher, dass Sie das Datumsformat und das Zeitformat konsistent für alle Datensätze in Datensätzen verwenden, für die Daten mit Zeitstempel erforderlich sind.
* Stellen Sie sicher, dass Sie dieselbe Granularität (Tag oder Woche) für Datensätze in Aggregat- oder Zusammenfassungsdatensätzen verwenden.

### Datenberechnung

* Vermeiden Sie doppelte Zeilen in einem Datensatz.
* Stellen Sie sicher, dass jeder Datensatz, den Sie hochladen, spezifisch für einen eindeutigen Kanal und Konversionstyp ist. Duplizieren Sie Touchpoints oder Konversionen über mehrere Datensätze hinweg, um die Modellausgabe und -qualität zu beeinträchtigen.

