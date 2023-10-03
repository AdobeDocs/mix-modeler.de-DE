---
title: Schemata
description: Erfahren Sie, wie Sie die Schemas verwalten, die zur Aufnahme von Daten in Mix Modeler erforderlich sind.
feature: Schemas
exl-id: 08289581-5af9-4422-b049-8c24105e2a8e
source-git-commit: 33883626d8e7aca2eecc3571593be53ef41ac458
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 8%

---

# Schemata

So verwalten Sie Schemata, indem Sie die Daten unterstützen, die Sie in Experience Platform erfassen und in Mix Modeler verwenden möchten:

1. Rufen Sie die Benutzeroberfläche des Mix Modelers auf.

1. Auswählen ![Schemas](../assets/icons/Schemas.svg) **[!UICONTROL Schemas]**, darunter **[!UICONTROL DATA MANAGEMENT]**.

Siehe [Übersicht über die Benutzeroberfläche von Schemas](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=de) für weitere Informationen.

## Aggregat- oder Zusammenfassungsdaten

Es wird dringend empfohlen, die Klasse &quot;XDM-Zusammenfassungsmetriken&quot;als Grundlage des Schemas zu verwenden, das allen Aggregat- oder Zusammenfassungsdaten zugrunde liegt, die Sie in Experience Platform erfassen und in Mix Modeler verwenden möchten.

Verwenden Sie die Klasse &quot;XDM-Zusammenfassungsmetriken&quot;für:

- Gartendaten, z. B. Daten aus Facebook oder YouTube, installiert.

- externe Faktoren, wie Daten aus SPX (S&amp;P 500 Börsenkursindizes), Wetterdaten,

- interne Faktoren, z. B. Preisänderungen, einen Weihnachtskalender.

>[!IMPORTANT]
>
>Die Schemadefinition muss mindestens ein numerisches Feld enthalten (unter Verwendung von Integer, Double, Boolean oder einem anderen numerischen Typ), um die erforderlichen Metriken für die erfassten Daten zu unterstützen.

Ein Schema, das **[!DNL XDM Summary Metrics]** Die Basisklasse kann einfach sein, wie in der **[!DNL ExternalFactorSummarySchema]** unten.

![Externes Factoryschema](../assets/external-factors-schema.png)

Dieses einfache Schema kann zum Erfassen von Datensätzen verwendet werden, die Daten enthalten, beispielsweise für:

- Konkurrierende Indexdaten

  | Zeitstempel | date_type | Faktor | value |
  |---|---|---|--:|
  | 28.11.2020:00:00.000Z | Woche | Konkurrentenindex | 289.8 |
  | 2020-12-05T00:00:00.000Z | Woche | Konkurrentenindex | 291.2 |
  | 12.12.2020 T00:00:00.000Z | Woche | Konkurrentenindex | 280.07 |
  | ... | ... | ... | ... |

- Daten zu Feiertagszeiten

  | Zeitstempel | date_type | Faktor | value |
  |---|---|---|--:|
  | 28.11.2020:00:00.000Z | Woche | all_days_flag | 0.0 |
  | 2020-12-05T00:00:00.000Z | Woche | all_days_flag | 0.0 |
  | 12.12.2020 T00:00:00.000Z | Woche | all_days_flag | 0.0 |
  | 2020-12-19T00:00:00.000Z | Woche | all_days_flag | 0.0 |
  | 26.12.2020:00:00.000Z | Woche | all_days_flag | 1,0 |
  | ... | ... | ... | ... |


Ein umfassenderes Beispiel für eine **[!DNL LumaPaidMarketingSchema]** mithilfe der **[!DNL XDM Summary Metrics]** als Basisklasse. Das Schema verwendet dedizierte Feldergruppen (mit Farben kommentiert) für Metriken (**[!DNL AMMMetrics]**), Dimensionen (**[!DNL AMMDimensions]**) und anderen kundenspezifischen Informationen (**[!DNL CustomerSpecific]**).

![Zusammenfassungsschema](../assets/summary-schema.png)

Angesichts der asynchronen Art der Profilerfassung wird bei der Erfassung von Aggregat- oder Zusammenfassungsdaten aus externen Quellen empfohlen, die Feldergruppe &quot;Prüfdetails des externen Quellsystems&quot;als Teil eines Schemas zu verwenden. Diese Feldergruppe definiert einen Satz von Prüfeigenschaften für externe Quellen.
