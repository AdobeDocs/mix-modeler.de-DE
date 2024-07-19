---
title: Scoring-Daten
description: Erfahren Sie, wie die Scoring-Daten eines Modells in Mix Modeler beibehalten werden.
feature: Models
exl-id: 2f2c3d20-7b14-41cc-a11a-03e8ad9e5d7a
source-git-commit: 86732fe30637aa72ced232d9f331a3cc64baa39b
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 8%

---

# Scoring-Daten

Beim Scoring eines Modells werden die Scoring-Daten in einem Datensatz unter Experience Platform persistiert. Dieser Datensatz entspricht einem Schema, das für jedes Modell in Ihrer Mix Modeler-Instanz erstellt wurde.

Das Schema für Scoring-Daten hat den Namen `AMM AI Schema - <name of model> <id>`. Beispiel: `AMM AI Schema - Model for Online Conversion 10120`.

Der Datensatz, der die Scoring-Daten für ein Modell beibehält, erhält den Namen `AMM AI Aggregrate Scores - <id>`, z. B. `AMM AI Aggregrate Scores - 10120`.


## Schema

Das Schema enthält eine Feldergruppe mit einem Objekt, das Details zu den Werten enthält. Das Objekt besteht aus den folgenden Feldern.

| Feldname | Typ | Definition |
|---|---|---|
| **campaignGroup** | Zeichenfolge | Name der Kampagnengruppe. |
| **campaignName** | Zeichenfolge | Name der Kampagne. |
| **beitrag** | Double | Beitrag, der dieser Konversion für den jeweiligen Touchpoint zugeordnet wurde. |
| **conversionEndDate** | Datum | Enddatum des Konvertierungsfensters. |
| **conversionName** | Zeichenfolge | Name der Konvertierung, die während des Einrichtungsschritts für die Konversionsdefinition erstellt wurde. |
| **conversionStartDate** | Datum | Startdatum des Konvertierungsfensters. |
| **geo** | Zeichenfolge | Der geografische Ort, an dem die Konversion erfolgte. |
| **mediaChannel** | Zeichenfolge | Name des Kanals, der beim Setup-Schritt des Touchpoints verwendet wurde. |
| **mediaSubChannel** | Zeichenfolge | Name des Unterkanals. |
| **Umsatz** | Double | Umsatz, der dieser Konversion für den jeweiligen Touchpoint zugeordnet wurde. |
| **scoreCreatedTime** | DateTime | Zeitpunkt, zu dem dieser Ergebnisdatensatz erstellt wird. |
| **touchpointEndDate** | Datum | Enddatum des Touchpoint-Fensters. |
| **touchpointName** | Zeichenfolge | Name des Touchpoints, der beim Setup-Schritt der Touchpoint-Definition erstellt wurde. Derzeit ist der Touchpoint im Medienkanal definiert. |
| **touchpointStartDate** | Datum | Startdatum des Touchpoint-Fensters. |

Weitere Informationen finden Sie unter [Schemas](../ingest-data/schemas.md) .
