---
title: Datenaufnahme - Übersicht
description: Erfahren Sie, wie Sie Daten in Mix Modeler aufnehmen.
feature: Datasets, Event Datasets, Summary Datasets, Aggregate Datasets
exl-id: dc16a601-bbd9-467b-8a7e-c32654d4069a
source-git-commit: 1a9df9f9819d9e0031e58443ec6a9e755a151ba0
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 10%

---

# Datenaufnahme - Übersicht

Mix Modeler arbeitet mit Daten auf Ereignisebene, aggregierten oder zusammenfassenden Daten zu Marketing-Bemühungen aus verschiedenen ummauerten Gärten. Und mit aggregierten oder zusammenfassenden Daten aus jeder anderen Quelle, wie Offline-Werbung, internen Faktoren oder externen Faktoren.

Kunden können alle Arten von Daten verwenden, die als Datensätze in Experience Platform aufgenommen werden und auf Schemata basieren, bei denen die XDM ExperienceEvent- oder XDM Summary-Metriken als Basisklasse verwendet werden.

Beispiel:

* Mit dem Adobe Analytics-Quell-Connector erfasste Daten. und in Datensätze umgewandelt, die der standardmäßigen oder einer benutzerdefinierten Version des Adobe Analytics-Schemas entsprechen.
* Daten, die mit der Experience Platform Web SDK, Mobile SDK oder der Edge Network Server-API erfasst werden, um Kundeninteraktionen im Web, auf Mobilgeräten oder auf anderen Gerätetypen zu erfassen.
* Aggregierte oder zusammengefasste Daten aus ummauerten Gärten (wie Facebook, YouTube), Traffic-Quellen oder Offline-Werbedaten.
* Nicht-Marketing-Aggregat- oder -Zusammenfassungsdaten mit internen oder externen Faktoren, die für die Modellerstellung nützlich sind.

Sie können jeden beliebigen von Experience Platform unterstützten Mechanismus verwenden, um Daten zu Erlebnisereignissen, aggregierten Marketing-Anstrengungen und Daten aus anderen Quellen aufzunehmen. Beispielsweise die Experience Platform-SDKs, APIs, Quell-Connectoren sowie Streaming- und Batch-Aufnahme. Weitere Informationen zur Aufnahme Ihrer Daten in Experience Platform zur Verwendung in Adobe Mix Modeler finden Sie unter [Datenaufnahme - Übersicht](https://experienceleague.adobe.com/de/docs/experience-platform/ingestion/home).

## Leitlinien

Um Daten zur Verwendung mit Mix Modeler in Experience Platform aufzunehmen, befolgen Sie die folgenden Richtlinien:

* Die inkrementellen Daten, die den Datensätzen hinzugefügt werden, sollten sich nicht überschneiden.
* Alle Daten aus einer einzigen Quelle sollten dieselbe Granularität aufweisen.
* Datum und Granularität sind obligatorische Felder im zugrunde liegenden Schema für alle aggregierten Daten, die als Datensätze aufgenommen werden
* Kanal ist ein Pflichtfeld im zugrunde liegenden Schema für alle Marketing-Aufwand-/Ausgabendaten, die als Datensätze aufgenommen werden.


## Beispiele

Nachfolgend finden Sie einige Beispiele für Daten, die normalerweise in Mix Modeler verwendet werden und über die standardmäßigen Erlebnisereignisdaten hinausgehen.

+++ Aggregierte Daten zum Marketing-Aufwand

| Geo | Datum | Datumstyp | Kanal | Campaign | Klicken | verdient | Interaktion | Impression | Öffnen | in Besitz | Gesendet | Ausgaben |
|---|:--|---|:---:|---|--:|---|--:|---|---|---|--:|--:|
| AMER | 31.10.2021 | day | E-MAIL | | 12752 | | | | | | 1132945 | |
| AMER | 31.10.2021 | day | FB | | 148844 | | | | | | | 42111 |
| AMER | 31.10.2021 | day | YT | | | | 2314452 | | | | | 10540 |
| JPN | 21.10.2021 | day | E-MAIL | | 21089 | | | | | | 3283626 | |
| JPN | 21.10.2021 | day | SOZIAL | | | | 621 | | | | | 74512 |

{style="table-layout:auto"}

+++

+++ Aggregierte Konversionsdaten

| Geo | Datum | Datumstyp | Produkt | Verkaufte Einheiten | Einnahmen |
|---|:---|:---:|---|--:|--:|
| EMEA | 13.09.2021 | day | Schöpferwirtschaft | 603 | 36537,68 |
| EMEA | 13.09.2021 | day | metavers | 55 | 21704,37 |
| JPN | 30.05.2022 | day | Pro Imaging | 487 | 64469,60 |
| JPN | 30.05.2022 | day | Document Cloud | 642 | 100509,07 |

{style="table-layout:auto"}

+++

+++ Daten zu externen Faktoren

| Daten | Datumstyp | Faktor | Wert |
|---|:---:|:---:|:---|
| 02.08.2020 | Woche | SPX | 3325,866 |
| 09.08.2020 | Woche | SPX | 3364,158 |
| 16.08.2020 | Woche | SPX | 3385,858 |
| 23.08.2020 | Woche | SPX | 3497,965 |

{style="table-layout:auto"}

+++

Um mit Daten in Mix Modeler arbeiten zu können, benötigen Sie Daten, die in Datensätzen erfasst und nach Schemata in Experience Platform modelliert wurden. Die Benutzeroberfläche von Mix Modeler bietet einfachen Zugriff auf die Benutzeroberfläche von Experience Platform-Schemata und Datensätzen.


## Überprüfen

Um zu überprüfen, ob Ihre Daten in Mix Modeler ordnungsgemäß verfügbar sind, können Sie Folgendes tun:

* Verwenden von Visualisierungen in der [Übersicht](/help/overview.md).
* Herunterladen und Überprüfen von Daten [Harmonisierte Daten](/help/harmonize-data/overview.md) in Harmonisierten Datensätzen.

Um zu überprüfen, ob Ihre Daten ordnungsgemäß in Experience Platform aufgenommen werden, können Sie [SQL-Abfragen mithilfe des Experience Platform Query Service schreiben und ausführen](https://experienceleague.adobe.com/en/docs/experience-platform/query/home).


>[!MORELIKETHIS]
>
>Weitere Informationen zum Verwalten von Schemata und Datensätzen finden Sie unter:
>
>* [Schemata](schemas.md)
>* [Datensätze](datasets.md)
