---
title: Datenaufnahme - Übersicht
description: Erfahren Sie, wie Sie Daten in Mix Modeler aufnehmen.
feature: Datasets, Event Datasets, Summary Datasets, Aggregate Datasets
exl-id: dc16a601-bbd9-467b-8a7e-c32654d4069a
TQID: https://experienceleague.adobe.com/XPr8Av7skzHBYoU6WtNw8PtHFrPH-MokICrLwoB2-J0
product_v2: id: b88c80e3-31df-4609-989d-d4dac0e6d973
feature_v2: id: e0abf868-dae2-4c1c-83e9-b21799232845id: fbd94e4b-f9b8-42a4-8df5-3f917aabae24
subfeature_v2: id: ad7101f7-ae92-401b-a25a-d3060d42989did: d1167c89-f64a-42ca-ac95-1d91b7790df2id: ee1bf083-e090-4def-936b-c111d29f42d0id: a4dc3e7d-bd07-4ac8-8e49-ff2e8fecf1e7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
autotag-review: '2026-05-01T09:11:34.506Z'
source-git-commit: 5579087b9381c4d8e909ed5fe3099fd42d5c6799
workflow-type: tm+mt
source-wordcount: 584
ht-degree: 17%

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

| Geo | Datum | Datumstyp | Kanal | Campaign | Click | verdient | Interaktion | Impression | Öffnen Sie | in Besitz | Gesendet | Ausgaben |
|---|:--|---|:---:|---|--:|---|--:|---|---|---|--:|--:|
| AMER | 2021-10-31 | Tag | E-MAIL | | 12752 | | | | | | 1132945 | |
| AMER | 2021-10-31 | Tag | FB | | 148844 | | | | | | | 42111 |
| AMER | 2021-10-31 | Tag | YT | | | | 2314452 | | | | | 10540 |
| JPN | 2021-10-21 | Tag | E-MAIL | | 21089 | | | | | | 3283626 | |
| JPN | 2021-10-21 | Tag | SOZIAL | | | | 621 | | | | | 74512 |

{style="table-layout:auto"}

+++

+++ Aggregierte Konversionsdaten

| Geo | Datum | Datumstyp | Produkt | Verkaufte Einheiten | Umsatz |
|---|:---|:---:|---|--:|--:|
| EMEA | 2021-09-13 | Tag | Schöpferwirtschaft | 603 | 36537.68 |
| EMEA | 2021-09-13 | Tag | metavers | 55 | 21704.37 |
| JPN | 2022-05-30 | Tag | Pro Imaging | 487 | 64469.60 |
| JPN | 2022-05-30 | Tag | Document Cloud | 642 | 100509.07 |

{style="table-layout:auto"}

+++

+++ Daten zu externen Faktoren

| Daten | Datumstyp | Faktor | Wert |
|---|:---:|:---:|:---|
| 2020-08-02 | Woche | SPX | 3325.866 |
| 2020-08-09 | Woche | SPX | 3364.158 |
| 2020-08-16 | Woche | SPX | 3385.858 |
| 2020-08-23 | Woche | SPX | 3497.965 |

{style="table-layout:auto"}

+++

Um mit Daten in Mix Modeler arbeiten zu können, benötigen Sie Daten, die in Datensätzen erfasst und nach Schemata in Experience Platform modelliert wurden. Die Benutzeroberfläche von Mix Modeler bietet einfachen Zugriff auf die Benutzeroberfläche von Experience Platform-Schemata und Datensätzen.


## Überprüfen

Um zu überprüfen, ob Ihre Daten in Mix Modeler ordnungsgemäß verfügbar sind, können Sie Folgendes tun:

* Verwenden von Visualisierungen in der [Übersicht](/help/overview.md).
* Herunterladen und Überprüfen von Daten [Harmonisierte Daten](/help/harmonize-data/overview.md) in Harmonisierten Datensätzen.

Um zu überprüfen, ob Ihre Daten ordnungsgemäß in Experience Platform aufgenommen werden, können Sie [SQL-Abfragen mithilfe des Experience Platform Query Service schreiben und ausführen](https://experienceleague.adobe.com/de/docs/experience-platform/query/home).


>[!MORELIKETHIS]
>
>Weitere Informationen zum Verwalten von Schemata und Datensätzen finden Sie unter:
>
>* [Schemata](schemas.md)
>* [Datensätze](datasets.md)
