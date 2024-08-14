---
title: Scoring-Daten
description: Erfahren Sie, wie die Scoring-Daten eines Modells in Mix Modeler beibehalten werden.
feature: Models
exl-id: 2f2c3d20-7b14-41cc-a11a-03e8ad9e5d7a
source-git-commit: b6045176e82b97f848113f4e0ffbbb995c48b3d4
workflow-type: tm+mt
source-wordcount: '675'
ht-degree: 10%

---

# Scoring-Daten

Beim Scoring eines Modells werden die Scoring-Daten in einem Datensatz unter Experience Platform persistiert. Wenn Sie während der Modellerstellung die Multi-Touch-Attribution aktiviert haben, werden zusätzliche Ereigniswertdaten in einem Datensatz in Experience Platform persistiert.

Jeder dieser Datensätze entspricht einem Schema. Dieser Artikel dokumentiert diese Schemas.


## Aggregieren des Datenschemas für Scoring

Das Schema für Scoring-Daten hat den Namen `AMM AI Schema - <name of model> <id>`. Beispiel: `AMM AI Schema - Model for Online Conversion 10120`.

Der Datensatz, der die Scoring-Daten für ein Modell beibehält, erhält den Namen `AMM AI Aggregrate Scores - <id>`, z. B. `AMM AI Aggregrate Scores - 10120`.

Das Schema enthält eine Feldergruppe mit einem Objekt, das Details zu den Werten enthält. Das Objekt besteht aus den folgenden Feldern.

| Feldname | Typ | Definition |
|---|---|---|
| `campaignGroup` | Zeichenfolge | Name der Kampagnengruppe. |
| `campaignName` | String | Name der Kampagne. |
| `contribution` | Double | Beitrag, der dieser Konversion für den jeweiligen Touchpoint zugeordnet wurde. |
| `conversionEndDate` | Datum | Enddatum des Konvertierungsfensters. |
| `conversionName` | String | Name der Konvertierung, die während des Einrichtungsschritts für die Konversionsdefinition erstellt wurde. |
| `conversionStartDate` | Datum | Startdatum des Konvertierungsfensters. |
| `geo` | String | Der geografische Ort, an dem die Konversion erfolgte. |
| `mediaChannel` | String | Name des Kanals, der beim Setup-Schritt des Touchpoints verwendet wurde. |
| `mediaSubChannel` | String | Name des Unterkanals. |
| `revenue` | Double | Umsatz, der dieser Konversion für den jeweiligen Touchpoint zugeordnet wurde. |
| `scoreCreatedTime` | DateTime | Zeitstempel, wenn dieser Ergebnisdatensatz erstellt wird. |
| `touchpointEndDate` | Datum | Enddatum des Touchpoint-Fensters. |
| `touchpointName` | String | Name des Touchpoints, der beim Setup-Schritt der Touchpoint-Definition erstellt wurde. Derzeit ist der Touchpoint im Medienkanal definiert. |
| `touchpointStartDate` | Datum | Startdatum des Touchpoint-Fensters. |


## Schema für Ereignisbewertungs-Daten

Das Schema für Scoring-Daten hat den Namen `Attribution AI Scores - <name of model> <id> - Schema`. Beispiel: `Attribution AI Scores - Model for Online Conversion 10120 - Schema`.

Der Datensatz, der die Scoring-Daten für ein Modell beibehält, erhält den Namen `Attribution AI Scores - <name of model> <id>`, z. B. `Attribution AI Scores - Model for Online Conversion 10120 `.

Das Schema enthält eine Feldergruppe mit einem Objekt, das Details zu den Kernen enthält. Das Objekt hat den Namen &quot;`attibution_AI_scores__<name of model> id`&quot;.

Die Feldergruppe enthält die folgenden Felder.

| Feldname | Typ | Beschreibung |
|---|---|---|
| `conversion` | Objekt | Konversionsmetadaten-Spalten. |
|     `passThrough` | Objekt |  |
|         `eventType` | String | |
|         `channel_typeAtSource` | String | |
|      `dataSource` | String | Globale eindeutige Identifizierung einer Datenquelle. <br> **Beispiel:** `Adobe Analytics` |
|      `eventSource` | String | Die Quelle, an der das tatsächliche Ereignis aufgetreten ist. <br> **Beispiel:** `Adobe.com` |
|      `eventType` | String | Der primäre Ereignistyp für diesen Zeitreihensatz. <br> **Beispiel:** `Order` |
|      `geo` | String | Der geografische Ort, an dem die Konversion bereitgestellt wurde `placeContext.geo.countryCode` <br>. **Beispiel:** `US` |
|      `path` | String | |
|      `priceTotal` | Double | Durch die Konversion erzielter Umsatz <br> **Beispiel:** `99.9` |
|      `product` | String | Die XDM-Kennung des Produkts selbst. <br> **Beispiel:** `RX 1080 ti` |
|      `productType` | String | Der Anzeigename für das Produkt, wie er dem Benutzer für diese Produktansicht angezeigt wird. <br> **Beispiel:** `Gpus` |
|      `quantity` | Ganzzahl | Während der Konvertierung gekaufte Menge. <br> **Beispiel:** `1` |
|      `receivedTimeStamp` | DateTime | Zeitstempel der Konvertierung erhalten. <br> **Beispiel:** `2020-06-09T00:01:51.000Z` |
|      `skuId` | String | Bestandseinheit (Stock Keeping Unit, SKU), die eindeutige Kennung eines vom Anbieter definierten Produkts. <br> **Beispiel:** `MJ-03-XS-Black` |
|      `timestamp` | DateTime | Zeitstempel der Konvertierung. <br> **Beispiel:** `2020-06-09T00:01:51.000Z` |
|      `totalDaysToConversion` | Ganzzahl |  |
|      `totalTouchpointCount` | Ganzzahl | |
| `customerProfile` | Objekt | Identitätsdetails des Benutzers, der zum Erstellen des Modells verwendet wird. |
|      `identity` | Objekt | |
|           `id` | String | |
|           `namespace` | String | Enthält die Details des Benutzers, der zum Erstellen des Modells verwendet wird, z. B. `id` und `namespace`. |
| `touchpointsDetail` | Objekt[] | Die Liste der Touchpoint-Details, die zur Konversion führen, geordnet nach Touchpoint-Vorkommen oder Zeitstempel. |
|      `scores` | Objekt | Touchpoint-Beitrag zu dieser Konversion als Ergebnis. |
|           `algorithmicInfluenced` | Double | Beeinflusstes Ergebnis ist der Anteil der Konversion, für den jeder Marketing-Touchpoint verantwortlich ist. |
|           `algorithmicSourced` | Double | Das inkrementelle Ergebnis ist der Betrag der direkt durch einen Marketing-Touchpoint verursachten marginalen Auswirkungen. |
|           `decayUnits` | Double | Regelbasierte Attributionsbewertung, bei der Touchpoints, die näher an der Konversion liegen, mehr Gewichtung erhalten als Touchpoints, die zeitlich weit von der Konversion entfernt sind. |
|           `firstTouch` | Double | Regelbasierte Attributionsbewertung, die alle Gutschriften dem ursprünglichen Touchpoint auf einem Konversionspfad zuweist. |
|           `lastTouch` | Double | Regelbasierte Attributionsbewertung, die die gesamte Gutschrift dem Touchpoint zuweist, der der Konversion am nächsten ist. |
|           `linear` | Double | Regelbasierte Attributionsbewertung, die jedem Touchpoint auf einem Konversionspfad die gleiche Gewichtung zuweist. |
|           `uShape` | Double | Regelbasierte Attributionsbewertung, die 40 % des Guthabens dem ersten Touchpoint und 40 % des Guthabens dem letzten Touchpoint zuweist. Die anderen Touchpoints teilen die verbleibenden 20 % gleichmäßig auf. |
|      `touchPoint` | Objekt | Touchpoint-Metadaten. |
|           `passThrough` | Objekt | |
|                `eventType` | String | |
|           `campaignGroup` | String |  |
|           `campaignName` | String | |
|           `campaignTag` | String | |
|           `eventId` | String | |
|           `geo` | String | |
|           `mediaAction` | String | |
|           `mediaChannel` | String | |
|           `receivedTimeStamp` | DateTime | |
|           `timestamp` | DateTime | |
|      `isFirstInThePosition` | Ganzzahl | |
|      `lag` | Ganzzahl | |
|      `position` | String | |
|      `touchpointCountToConversion` | Ganzzahl | |
|      `touchpointName` | String | Name des Touchpoints, der beim Einrichten konfiguriert wurde. <br> **Beispiel:** `PAID_SEARCH_CLICK` |
| `conversionName` | String | Name der Konversion, die während der Einrichtung konfiguriert wurde. <br> **Beispiel:** `Order`, `Lead`, `Visit` |
| `scoreCreatedTime` | DateTime | |
| `segmentation` | String | Konversionssegment, z. B. Geo-Segmentierung, auf dem das Modell basiert. Wenn Segmente fehlen, ist `segmentation` gleich `conversionName`. <br> **Beispiel:** `ORDER_US` |





Weitere Informationen finden Sie unter [Schemas](../ingest-data/schemas.md) .
