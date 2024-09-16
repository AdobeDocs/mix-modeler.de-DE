---
title: Schemata
description: Erfahren Sie, wie Sie die Schemas verwalten, die zur Aufnahme von Daten in Mix Modeler erforderlich sind.
feature: Schemas
exl-id: 08289581-5af9-4422-b049-8c24105e2a8e
source-git-commit: 9a6c1f1c12ab29da80a1997cfd31ca07b38eaa22
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 5%

---

# Schemata

So verwalten Sie Schemata, indem Sie die Daten unterstützen, die Sie in Experience Platform erfassen und in Mix Modeler verwenden möchten:

1. Rufen Sie die Benutzeroberfläche des Mix Modelers auf.

1. Wählen Sie ![Schemas](/help/assets/icons/Schemas.svg) **[!UICONTROL Schemas]** unter **[!UICONTROL SETUP]** aus.

Weitere Informationen finden Sie in der [Übersicht über die Benutzeroberfläche von Schemas](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=de) .

## Aggregat- oder Zusammenfassungsdaten

Es wird dringend empfohlen, die Klasse &quot;XDM-Zusammenfassungsmetriken&quot;als Grundlage des Schemas zu verwenden, das allen Aggregat- oder Zusammenfassungsdaten zugrunde liegt, die Sie in Experience Platform erfassen und in Mix Modeler verwenden möchten.

Verwenden Sie die Klasse &quot;XDM-Zusammenfassungsmetriken&quot;für:

- Gartendaten, z. B. Daten aus Facebook oder YouTube, installiert.

- externe Faktoren, wie Daten aus SPX (S&amp;P 500 Börsenkursindizes), Wetterdaten,

- interne Faktoren, z. B. Preisänderungen, einen Weihnachtskalender.

>[!IMPORTANT]
>
>Die Schemadefinition muss mindestens ein numerisches Feld enthalten (unter Verwendung von Integer, Double, Boolean oder einem anderen numerischen Typ), um die erforderlichen Metriken für die erfassten Daten zu unterstützen.

Ein Schema, das die **[!DNL XDM Summary Metrics]** -Basisklasse verwendet, kann einfach sein, wie in **[!DNL ExternalFactorSummarySchema]** unten dargestellt.

![Schema externer Faktoren](/help/assets/external-factors-schema.png)

Dieses einfache Schema kann zum Erfassen von Datensätzen verwendet werden, die Daten enthalten, beispielsweise für:

- Konkurrierende Indexdaten

  | Zeitstempel | date_type | Faktor | value |
  |---|---|---|--:|
  | 2020-11-28T00:00:00.000Z | Woche | Konkurrentenindex | 289,8 |
  | 2020-12-05T00:00:00.000Z | Woche | Konkurrentenindex | 291,2 |
  | 2020-12-12T00:00:00.000Z | Woche | Konkurrentenindex | 280,07 |
  | ... | ... | ... | ... |

- Daten zu Feiertagszeiten

  | Zeitstempel | date_type | Faktor | value |
  |---|---|---|--:|
  | 2020-11-28T00:00:00.000Z | Woche | all_days_flag | 0,0 |
  | 2020-12-05T00:00:00.000Z | Woche | all_days_flag | 0,0 |
  | 2020-12-12T00:00:00.000Z | Woche | all_days_flag | 0,0 |
  | 2020-12-19T00:00:00.000Z | Woche | all_days_flag | 0,0 |
  | 2020-12-26T00:00:00.000Z | Woche | all_days_flag | 1,0 |
  | ... | ... | ... | ... |


Unten finden Sie ein umfassenderes Beispiel für eine **[!DNL LumaPaidMarketingSchema]**, die die **[!DNL XDM Summary Metrics]** als Basisklasse verwendet. Das Schema verwendet dedizierte Feldergruppen (mit Farben kommentiert) für Metriken (**[!DNL AMMMetrics]**), Dimensionen (**[!DNL AMMDimensions]**) und andere kundenspezifische Informationen (**[!DNL CustomerSpecific]**).

![Zusammenfassungsschema](/help/assets/summary-schema.png)

Angesichts der asynchronen Art der Profilerfassung wird bei der Erfassung von Aggregat- oder Zusammenfassungsdaten aus externen Quellen empfohlen, die Feldergruppe &quot;Prüfdetails für das externe Source-System&quot;als Teil eines Schemas zu verwenden. Diese Feldergruppe definiert einen Satz von Prüfeigenschaften für externe Quellen.


## Unterstützte Datentypen

Derzeit unterstützt Mix Modeler eine Untergruppe von Experience Platform-Datentypen. Die folgenden grundlegenden Datentypen (Felder), die in [Grundlagen der Schemakomposition](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#data-type) erwähnt werden, werden unterstützt:

- Zeichenfolge
- Ganzzahl
- Double
- Boolesch
- Lang
- Kurz
- Byte
- Datum
- Datum-Uhrzeit
