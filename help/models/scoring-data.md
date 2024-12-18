---
title: Bewertungsdaten
description: Erfahren Sie, wie die Bewertungsdaten eines Modells im Mix Modeler beibehalten werden.
feature: Models
exl-id: 2f2c3d20-7b14-41cc-a11a-03e8ad9e5d7a
source-git-commit: b6045176e82b97f848113f4e0ffbbb995c48b3d4
workflow-type: tm+mt
source-wordcount: '675'
ht-degree: 10%

---

# Bewertungsdaten

Im Rahmen der Bewertung eines Modells werden Bewertungsdaten in einem Datensatz in Experience Platform beibehalten. Wenn Sie die Multi-Touch-Attribution während der Modellerstellung aktiviert haben, werden zusätzliche Ereignisbewertungsdaten in einem Datensatz im Experience Platform beibehalten.

Jeder dieser Datensätze entspricht einem Schema. In diesem Artikel werden diese Schemata dokumentiert.


## Schema für aggregierte Bewertungsdaten

Das Schema für die Bewertung von Daten heißt `AMM AI Schema - <name of model> <id>`. Beispiel: `AMM AI Schema - Model for Online Conversion 10120`.

Der Datensatz, der die Bewertungsdaten für ein Modell beibehält, wird wie `AMM AI Aggregrate Scores - <id>` benannt, z. B. `AMM AI Aggregrate Scores - 10120`.

Das Schema enthält eine Feldergruppe mit einem -Objekt, das Details zu den Scores enthält. Das -Objekt besteht aus den folgenden Feldern.

| Feldname | Typ | Definition |
|---|---|---|
| `campaignGroup` | Zeichenfolge | Name der Kampagnengruppe. |
| `campaignName` | String | Name der Kampagne. |
| `contribution` | Double | Dieser Konversion zugewiesener Beitrag für den jeweiligen Touchpoint. |
| `conversionEndDate` | Datum | Enddatum des Konvertierungsfensters. |
| `conversionName` | String | Name der Konvertierung, die beim Setup-Schritt der Konversionsdefinition erstellt wurde. |
| `conversionStartDate` | Datum | Startdatum des Konvertierungsfensters. |
| `geo` | String | Der geografische Ort, an dem die Konversion stattgefunden hat. |
| `mediaChannel` | String | Name des Kanals, der während des Touchpoint-Einrichtungsschritts verwendet wurde. |
| `mediaSubChannel` | String | Name des Unterkanals. |
| `revenue` | Double | Dieser Konversion zugewiesener Umsatz für den jeweiligen Touchpoint. |
| `scoreCreatedTime` | DateTime | Zeitstempel, wann dieser Score-Datensatz erstellt wird. |
| `touchpointEndDate` | Datum | Enddatum des Touchpoint-Fensters |
| `touchpointName` | String | Name des Touchpoints, der beim Setup-Schritt der Touchpoint-Definition erstellt wurde. Derzeit ist der Touchpoint im Medienkanal definiert. |
| `touchpointStartDate` | Datum | Startdatum des Touchpoint-Fensters. |


## Schema für Ereignisbewertungsdaten

Das Schema für die Bewertung von Daten heißt `Attribution AI Scores - <name of model> <id> - Schema`. Beispiel: `Attribution AI Scores - Model for Online Conversion 10120 - Schema`.

Der Datensatz, der die Bewertungsdaten für ein Modell beibehält, wird wie `Attribution AI Scores - <name of model> <id>` benannt, z. B. `Attribution AI Scores - Model for Online Conversion 10120 `.

Das Schema enthält eine Feldergruppe mit einem Objekt, das Details zu den Kernen enthält. Das Objekt trägt den Namen `attibution_AI_scores__<name of model> id`.

Die Feldergruppe enthält die folgenden Felder.

| Feldname | Typ | Beschreibung |
|---|---|---|
| `conversion` | Objekt | Konversionsmetadaten-Spalten. |
|     `passThrough` | Objekt |  |
|         `eventType` | String | |
|         `channel_typeAtSource` | String | |
|      `dataSource` | String | Globale eindeutige Identifizierung einer Datenquelle. <br> **Beispiel:** `Adobe Analytics` |
|      `eventSource` | String | Die Quelle, an der das tatsächliche Ereignis aufgetreten ist. <br> **Beispiel:** `Adobe.com` |
|      `eventType` | String | Der primäre Ereignistyp für diesen Zeitreiheneintrag. <br> **Beispiel:** `Order` |
|      `geo` | String | Der geografische Ort, an dem die Konversion bereitgestellt wurde, `placeContext.geo.countryCode`. <br> **Beispiel:** `US` |
|      `path` | String | |
|      `priceTotal` | Double | Durch die <br> erzielter Umsatz **Beispiel:** `99.9` |
|      `product` | String | Die XDM-Kennung des Produkts selbst. <br> **Beispiel:** `RX 1080 ti` |
|      `productType` | String | Der Anzeigename für das Produkt, wie er dem Benutzer für diese Produktansicht präsentiert wird. <br> **Beispiel:** `Gpus` |
|      `quantity` | Ganzzahl | Bei der Konversion gekaufte Menge <br> **Beispiel:** `1` |
|      `receivedTimeStamp` | DateTime | Zeitstempel der Konversion empfangen. <br> **Beispiel:** `2020-06-09T00:01:51.000Z` |
|      `skuId` | String | Lagerhaltungseinheit (SKU), die eindeutige Kennung für ein vom Anbieter definiertes Produkt. <br> **Beispiel:** `MJ-03-XS-Black` |
|      `timestamp` | DateTime | Zeitstempel der Konversion. <br> **Beispiel:** `2020-06-09T00:01:51.000Z` |
|      `totalDaysToConversion` | Ganzzahl |  |
|      `totalTouchpointCount` | Ganzzahl | |
| `customerProfile` | Objekt | Identitätsdetails des Benutzers, der zum Erstellen des Modells verwendet wurde. |
|      `identity` | Objekt | |
|           `id` | String | |
|           `namespace` | String | Enthält die Details des Benutzers, der zum Erstellen des Modells verwendet wird, z. B. `id` und `namespace`. |
| `touchpointsDetail` | Objekt[] | Die Liste der Touchpoint-Details, die zur Konversion führen, sortiert nach Touchpoint-Vorkommen oder Zeitstempel. |
|      `scores` | Objekt | Touchpoint-Beitrag zu dieser Konversion als Score. |
|           `algorithmicInfluenced` | Double | Der beeinflusste Score ist der Anteil der Konversion, für den jeder Marketing-Touchpoint verantwortlich ist. |
|           `algorithmicSourced` | Double | Der inkrementelle Score ist der Betrag der marginalen Auswirkungen, die direkt durch einen Marketing-Touchpoint verursacht werden. |
|           `decayUnits` | Double | Regelbasierter Attributionswert, bei dem Touchpoints, die näher an der Konversion liegen, mehr Credits erhalten als Touchpoints, die zeitlich weiter von der Konversion entfernt liegen. |
|           `firstTouch` | Double | Regelbasierter Attributionswert, der alle Credits dem ersten Touchpoint auf einem Konversionspfad zuweist. |
|           `lastTouch` | Double | Regelbasierte Attributionsbewertung, die den gesamten Wert dem Touchpoint zuweist, der der Konversion am nächsten ist. |
|           `linear` | Double | Regelbasierter Attributionswert, der jedem Touchpoint auf einem Konversionspfad den gleichen Wert zuweist. |
|           `uShape` | Double | Regelbasierter Attributionswert, der 40 % des Werts dem ersten Touchpoint und 40 % dem letzten Touchpoint zuweist. Die anderen Touchpoints teilen die restlichen 20 % gleichmäßig auf. |
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
|      `touchpointName` | String | Name des Touchpoints, der bei der Einrichtung konfiguriert wurde. <br> **Beispiel:** `PAID_SEARCH_CLICK` |
| `conversionName` | String | Name der Konvertierung, die beim Setup konfiguriert wurde. <br> **Beispiel:** `Order`, `Lead`, `Visit` |
| `scoreCreatedTime` | DateTime | |
| `segmentation` | String | Konversionssegmente wie die Geosegmentierung, anhand derer das Modell erstellt wird. Wenn Segmente fehlen, ist `segmentation` identisch mit `conversionName`. <br> **Beispiel:** `ORDER_US` |





Weitere Informationen finden [ unter ](../ingest-data/schemas.md).
