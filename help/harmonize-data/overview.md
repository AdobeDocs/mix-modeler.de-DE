---
title: Daten harmonisieren
description: Erfahren Sie, wie Sie Daten im Adobe Mix Model harmonisieren.
feature: Harmonized Data
source-git-commit: ac17f5a9fcf036c8e689879578e4b745b789cea3
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 18%

---


# Daten harmonisieren

Die Daten im Adobe Mix Modeler unterscheiden sich je nach Datenquelle. Die Daten können wie folgt lauten:

* aggregierte Daten, z. B. aus Datenquellen mit eingebautem Garten erfasst,
* Ereignisdaten, z. B. aus Erstanbieter-Datenquellen. Diese Ereignisdaten können Daten sein, die über den Adobe Analytics-Quell-Connector von Adobe Analytics oder über das Adobe Experience Platform Web oder Mobile SDK oder die Edge Network API erfasst werden, oder Daten, die über Quell-Connectoren erfasst werden.

Der Harmonisierungsdienst von Adobe Mix Modeler gleicht die Aggregat- und Ereignisdaten in einer einheitlichen Datenansicht an. Diese Datenansicht ist die Quelle für die Pläne und Modelle in Adobe Mix Modeler.

## Beispiel für harmonisierte Daten

Angenommen, Sie verfügen über die folgenden Datensätze für Adobe Mix Modeler.

**Datensatz 1**

Enthält Marketingaufwand-Datensatz aus YouTube, wobei die Granularität der aggregierten Daten auf täglich eingestellt ist.

| Datum | Datum Typ | Kanal | Campaign | Marke | Geo | Klicks | Ausgeben |
|---|:--:|---|---|---|---|---:|---:|
| 12-31-2021 | day | YouTube | Y_Fall_02 | BrandX | USA | 10000 | 100 |
| 01-01-2022 | day | YouTube | Y_Fall_02 | BrandX | USA | 1000 | 10 |
| 01-03-2022 | day | YouTube | Y_Fall_01 | BrandY | CA | 10000 | 100 |
| 01-04-2022 | day | YouTube | Y_Summer_01 | Null | CA | 9000 | 80 |

{style="table-layout:auto"}


**Datensatz 2**

Enthält Marketing-Aufwandsdatensatz aus Facebook, wobei die Granularität der aggregierten Daten auf Wöchentlich eingestellt ist.

| Datum | Datum Typ | Kanal | Campaign | Geo | Klicks | Ausgeben |
|--- |:---:|--- |---|---|---:|---:|
| 01-01-2022 | Woche | Facebook | FB_Fall_01 | USA | 8000 | 100 |
| 01-08-2022 | Woche | Facebook | FB_Fall_02 | USA | 1000 | 10 |
| 01-08-2022 | Woche | Facebook | FB_Fall_01 | USA | 7000 | 100 |
| 01-16-2022 | Woche | Facebook | FB_Summer_01 | CA | 10000 | 80 |

{style="table-layout:auto"}


**Datensatz 3**

Ein Konversionsdatensatz mit einer Granularität der aggregierten Daten, die auf täglich eingestellt sind.

| Datum | Datum Typ | Geo | Ziel | Umsatz |
|--- |:---: |---|---|---:|
| 01-01-2022 | day | USA | Mode | 200 |
| 01-08-2022 | day | USA | Mode | 10 |
| 01-08-2022 | day | USA | Schmuck | 1100 |
| 01-16-2022 | day | CA | Schmuck | 80 |

{style="table-layout:auto"}


**Datensatz 4**

Ein Beispiel für einen Erlebnisereignis-Datensatz (Web SDK-Ereignisse) vom Kunden.

| Zeitstempel | Identity-Namespace | ID | Kanal | Klicks |
|--- |--- |--- |--- |---:|
| 01-01-2022 00:01:01.000 | ECID | 64fd46ff-8c63-43b4-85a7-92b953113ba0 | CSE | 1 |
| 01-01-2022 00:01:01.000 | ECID | 64fd46ff-8c63-43b4-85a7-92b953113ba0 | CSE | 1 |
| 01-08-2022 00:01:01.000 | ECID | 2ca2a16e-caf0-4fa9-9a8b-9774b39547c4 | CSE | 1 |
| 01-08-2022 00:01:01.000 | ECID | 5ce99bfb-e44a-40d9-b8cd-c5408bda7cdc | CSE | 1 |

{style="table-layout:auto"}


Sie möchten einen harmonisierten Datensatz erstellen, dessen Granularität auf &quot;Wöchentlich&quot;festgelegt ist. Die Ereignisdaten werden in die Granularität &quot;Woche&quot;aggregiert und zum harmonisierten Datensatz hinzugefügt. Das Ergebnis lautet:

**Harmonisierter Datensatz**

| Datum | Datum Typ | Kanal | Campaign | Marke | Geo | Ziel | Klicks | Ausgeben | Umsatz |
|--- |:---:|--- |--- |--- |---|---|---:|---:|---:|
| 12-27-2021 | Woche | YouTube | Y_Fall_02 | BrandX | USA | Null | 11000 | 110 | Null |
| 01-03-2022 | Woche | YouTube | Y_Fall_01 | BrandY | CA | Null | 10000 | 100 | Null |
| 01-03-2022 | Woche | YouTube | Y_Summer_01 | Null | CA | Null | 9000 | 80 | Null |
| 01-01-2022 | Woche | Facebook | FB_Fall_01 | Null | USA | Null | 8000 | 100 | Null |
| 01-08-2022 | Woche | Facebook | FB_Fall_02 | Null | USA | Null | 1000 | 10 | Null |
| 01-08-2022 | Woche | Facebook | FB_Fall_01 | Null | USA | Null | 7000 | 100 | Null |
| 01-16-2022 | Woche | Facebook | FB_Summer_01 | Null | CA | Null | 10000 | 80 | Null |
| 12-27-2021 | Woche | Null | Null | Null | USA | Mode | Null | Null | 200 |
| 01-03-2022 | Woche | Null | Null | Null | USA | Mode | Null | Null | 10 |
| 01-03-2022 | Woche | Null | Null | Null | USA | Schmuck | Null | Null | 1100 |
| 01-10-2022 | Woche | Null | Null | Null | CA | Schmuck | Null | Null | 80 |
| 01-01-2022 | Woche | CSE | Null | Null | Null | Null | 2 | Null | Null |
| 01-08-2022 | Woche | CSE | Null | Null | Null | Null | 2 | Null | Null |

{style="table-layout:auto"}


## Harmonisierte Daten einrichten

So erstellen Sie einen harmonisierten Datensatz, wie in der vereinfachten [example](#an-example-of-harmonized-data)müssen Sie die folgenden Schritte ausführen:

1. Zusätzliche Definition [harmonisierte Felder](fields.md) die Sie über die bereits verfügbaren harmonisierten globalen Felder hinaus verwenden möchten.
1. Einrichten [Datensatzregeln](dataset-rules.md) , um Felder aus Ihrem Aggregat- oder Erlebnisereignis-Datensatz harmonisierten Feldern zuzuordnen.
1. Definieren [Marketing-Touchpoints](marketing-touchpoints.md) unter Verwendung der von Ihnen definierten standardmäßigen und zusätzlichen harmonisierten Felder.
1. Definieren [Konversionen](conversions.md) unter Verwendung der von Ihnen definierten standardmäßigen und zusätzlichen harmonisierten Felder.


## Harmonisierte Daten anzeigen

So zeigen Sie Ihre harmonisierten Daten in der Adobe Mix Modeller-Benutzeroberfläche an:

1. Auswählen ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized datasets]** über die linke Leiste.

1. Auswählen **[!UICONTROL Harmonized Data]** aus der oberen Leiste. Es wird eine Zusammenstellung Ihrer harmonisierten Daten basierend auf den von Ihnen definierten Feldern, Datensatzregeln, Marketing-Touchpoints und Konversionen angezeigt.

   1. Um den Zeitraum, auf dem die Zusammenstellung harmonisierter Daten basiert, neu zu definieren, geben Sie einen Datumsbereich für **[!UICONTROL Date range]** oder Verwendung ![Kalender](../assets/icons/Calendar.svg) , um einen Datenbereich auszuwählen.

   1. Um die für die harmonisierte Datentabelle angezeigten Spalten zu ändern, verwenden Sie ![Einstellungen](../assets/icons/Setting.svg) , um die **[!UICONTROL Column settings]** angezeigt.

      1. Auswählen ![SelectBox](../assets/icons/SelectBox.svg) eine oder mehrere Spalten aus **[!UICONTROL AVAILABLE COLUMNS]** und Verwendung ![Chevron rechts](../assets/icons/ChevronRight.svg) , um diese Spalten hinzuzufügen **[!UICONTROL SELECTED COLUMNS]**.

      1. Auswählen ![SelectBox](../assets/icons/SelectBox.svg) eine oder mehrere Spalten aus **[!UICONTROL SELECTED COLUMNS]** und Verwendung ![Chevron links](../assets/icons/ChevronLeft.svg) , um die ausgewählten Spalten zu entfernen und diese Spalten zurück an **[!UICONTROL AVAILABLE COLUMNS]**.

      1. Wählen Sie eine Spalte aus **[!UICONTROL DEFAULT SORT]** und umschalten zwischen **[!UICONTROL Ascending]** oder **[!UICONTROL Descending]**.

      1. Um die Reihenfolge der angezeigten Spalten zu ändern, können Sie eine Spalte verschieben in **[!UICONTROL SELECTED COLUMNS]** per Drag &amp; Drop nach oben und unten

   1. Auswählen **[!UICONTROL Submit]** , um die Änderungen an den Spalteneinstellungen einzureichen. Auswählen **[!UICONTROL Close]** , um alle von Ihnen vorgenommenen Änderungen abzubrechen.


