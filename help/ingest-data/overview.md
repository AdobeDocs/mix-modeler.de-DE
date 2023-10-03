---
title: Daten erfassen
description: Erfahren Sie, wie Sie Daten in Mix Modeler erfassen.
feature: Datasets, Event Datasets, Summary Datasets, Aggregate Datasets
exl-id: dc16a601-bbd9-467b-8a7e-c32654d4069a
source-git-commit: 33883626d8e7aca2eecc3571593be53ef41ac458
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 15%

---

# Daten erfassen

Mix Modeler arbeitet mit Daten auf Ereignisebene, aggregierten Daten zu Marketing-Maßnahmen aus verschiedenen installierten Gärten sowie Aggregat- oder Zusammenfassungsdaten aus anderen Quellen wie Offline-Werbung, internen Faktoren oder externen Faktoren.

Kunden können beliebige Daten verwenden, die als Datensätze in Experience Platform aufgenommen werden und auf Schemas basieren, indem sie XDM ExperienceEvent oder XDM Summary Metrics als Basisklasse verwenden.

Beispiel:

* Daten, die mit dem Adobe Analytics-Quell-Connector erfasst und in Datensätze umgewandelt wurden, die der Standardversion oder einer benutzerdefinierten Version des Adobe Analytics-Schemas entsprechen, oder alternativ
* Daten, die mit dem Experience Platform Web SDK, Mobile SDK oder Edge Network Server API zur Erfassung von Kundeninteraktionen im Web, auf Mobilgeräten oder auf anderen Geräten erfasst werden,
* Aggregat von Daten aus eingeschlossenen Gärten (wie Facebook, YouTube), Traffic-Quellen oder Offline-Werbedaten,
* Nicht-Marketing-Aggregat- oder Zusammenfassungsdaten mit internen oder externen Faktoren, die für die Modellerstellung nützlich sind.

Sie können jede Art von Mechanismus verwenden, der von Experience Platform unterstützt wird, um Ihre Erlebnisereignisebene zu erfassen, Daten zu Marketing-Maßnahmen zu aggregieren und Daten aus anderen Quellen zu erfassen. Experience Platform-SDK, APIs, Quell-Connectoren sowie Streaming- und Batch-Erfassung.


## Leitlinien

Gehen Sie wie folgt vor, um Daten in Experience Platform zur Verwendung mit Mix Modeler aufzunehmen:

* Die inkrementellen Daten, die zu den Datensätzen hinzugefügt werden, sollten sich nicht überschneiden.
* Alle Daten aus einer einzigen Quelle sollten dieselbe Granularität aufweisen.
* Datum und Granularität sind Pflichtfelder im zugrunde liegenden Schema für alle aggregierten Daten, die als Datensätze erfasst werden
* Der Kanal ist ein Pflichtfeld im zugrunde liegenden Schema für alle Marketing-Aufwands-/Ausgabedaten, die als Datensätze erfasst werden.


## Beispiele

Nachstehend finden Sie einige Beispiele für Daten, die üblicherweise in Mix Modeler verwendet werden, die über die standardmäßigen Erlebnisereignisdaten hinausgehen.

+++ Aggregieren von Daten zu Marketing-Maßnahmen

| Geo | Datum | Datum Typ | Kanal | Campaign | Klicken | Earned | Interaktion | Impression | Öffnen | Eigene | Gesendet |
|---|:--|---|:---:|---|--:|---|--:|---|---|---|--:|
| AMER | 2021-10-31 | day | E-MAIL | | 12752 | | | | | | 1132945 |
| AMER | 2021-10-31 | day | FB | | 148844 | | | | | | |
| AMER | 2021-10-31 | day | YT | | | | 2314452 | | | | |
| JPN | 2021-10-21 | day | E-MAIL | | 21089 | | | | | | 3283626 |
| JPN | 2021-10-21 | day | SOCIAL | | | | 621 | | | | |

{style="table-layout:auto"}

+++

+++ Aggregieren von Konversionsdaten

| Geo | Datum | Datum Typ | Produkt | Verkaufte Einheiten | Umsatz |
|---|:---|:---:|---|--:|--:|
| EMEA | 2021-09-13 | day | Kreativwirtschaft | 603 | 36537.68 |
| EMEA | 2021-09-13 | day | Metaverse | 55 | 21704.37 |
| JPN | 2022-05-30 | day | Pro Imaging | 487 | 64469.60 |
| JPN | 2022-05-30 | day | Document Cloud | 642 | 100509.07 |

{style="table-layout:auto"}

+++

+++ Daten zu externen Faktoren

| Daten | Datum Typ | Faktor | Wert |
|---|:---:|:---:|:---|
| 2020-08-02 | Woche | SPX | 3325.866 |
| 2020-08-09 | Woche | SPX | 3364.158 |
| 2020-08-16 | Woche | SPX | 3385.858 |
| 2020-08-23 | Woche | SPX | 3497.965 |

{style="table-layout:auto"}

+++

Um mit Daten in Mix Modeler zu arbeiten, benötigen Sie Daten, die in Datensätzen erfasst und nach Schemas im Experience Platform modelliert wurden. Die Mix Modeler-Oberfläche bietet einfachen Zugriff auf die Benutzeroberfläche von Schemas und Datensätzen.


>[!MORELIKETHIS]
>
>Weitere Informationen zum Verwalten von Schemas und Datensätzen finden Sie unter:
>
>* [Schemata](schemas.md)
>* [Datensätze](datasets.md)
