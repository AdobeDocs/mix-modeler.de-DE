---
title: Schemata
description: Erfahren Sie, wie Sie die Schemata verwalten, die zur Aufnahme von Daten in Mix Modeler erforderlich sind.
feature: Schemas
exl-id: 08289581-5af9-4422-b049-8c24105e2a8e
source-git-commit: b0306ad6fad8966822ed14c67f159a4aefb4e3f8
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 6%

---

# Schemata

So verwalten Sie Schemata, indem Sie die Daten unterstützen, die Sie in Experience Platform aufnehmen und in Mix Modeler verwenden möchten:

1. Wechseln Sie zur Mix Modeler-Benutzeroberfläche.

1. Wählen Sie ![Schemata](/help/assets/icons/Schemas.svg) **[!UICONTROL Schemas]** unter **[!UICONTROL SETUP]** aus.

Weitere Informationen dazu finden [&#x200B; in der Übersicht &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=de) Schemas-Benutzeroberfläche .

## Aggregierte oder zusammenfassende Daten

Es wird dringend empfohlen, die Klasse XDM Summary Metrics als Grundlage für das Schema zu verwenden, das allen Aggregat- oder Zusammenfassungsdaten zugrunde liegt, die Sie in Experience Platform aufnehmen und in Mix Modeler verwenden möchten.

Verwenden Sie die Klasse XDM Summary Metrics für:

- Ummauerte Gartendaten, z. B. Daten von Facebook oder YouTube.

- Daten externer Faktoren, wie Daten von SPX (S&amp;P 500 Aktienpreisindizes), Wetterdaten,

- Daten zu internen Faktoren, z. B. Preisänderungen, Feiertagskalender.

>[!IMPORTANT]
>
>Die Schemadefinition muss mindestens ein numerisches Feld enthalten (mit Ganzzahl, Doppelt, Boolesch oder einem anderen numerischen Typ), um die erforderlichen Metriken für die aufgenommenen Daten zu unterstützen.

Ein Schema, das die **[!DNL XDM Summary Metrics]** Basisklasse verwendet, kann einfach sein, wie in der folgenden **[!DNL ExternalFactorSummarySchema]** dargestellt.

![Schema „Externe Faktoren](/help/assets/external-factors-schema.png)

Dieses einfache Schema kann verwendet werden, um Datensätze aufzunehmen, die Daten enthalten für z. B.:

- Wettbewerbsindexdaten

  | Zeitstempel | date_type | Faktor | Wert |
  |---|---|---|--:|
  | 28.11.2020 T00:00:00.000Z | Woche | Competitor_index | 289,8 |
  | 2020-12-05T00:00:00.000Z | Woche | Competitor_index | 291,2 |
  | 2020-12-12T00:00:00.000Z | Woche | Competitor_index | 280,07 |
  | … | ... | ... | ... |

- Daten zu Feiertagen

  | Zeitstempel | date_type | Faktor | Wert |
  |---|---|---|--:|
  | 28.11.2020 T00:00:00.000Z | Woche | all_hosts_flag | 0,0 |
  | 2020-12-05T00:00:00.000Z | Woche | all_hosts_flag | 0,0 |
  | 2020-12-12T00:00:00.000Z | Woche | all_hosts_flag | 0,0 |
  | 2020-12-19T00:00:00.000Z | Woche | all_hosts_flag | 0,0 |
  | 26.12.2020:00:00.000Z | Woche | all_hosts_flag | 1,0 |
  | ... | ... | ... | ... |


Unten finden Sie ein umfassendes Beispiel für eine **[!DNL LumaPaidMarketingSchema]**, bei der die **[!DNL XDM Summary Metrics]** als Basisklasse verwendet wird. Das Schema verwendet dedizierte Feldergruppen (mit Farben kommentiert) für Metriken (**[!DNL AMMMetrics]**), Dimensionen (**[!DNL AMMDimensions]**) und andere kundenspezifische Informationen (**[!DNL CustomerSpecific]**).

![Zusammenfassungsschema](/help/assets/summary-schema.png)

Da die Profilaufnahme asynchron erfolgt, wird empfohlen, bei der Erfassung von Aggregat- oder Zusammenfassungsdaten aus externen Quellen die Feldergruppe Audit-Details des externen Source-Systems als Teil eines Schemas zu verwenden. Diese Feldergruppe definiert einen Satz von Audit-Eigenschaften für externe Quellen.


## Unterstützte Datentypen

Derzeit unterstützt Mix Modeler eine Untergruppe von Experience Platform-Datentypen nicht. Die folgenden grundlegenden Datentypen (Felder), die unter [Grundlagen der Schemakomposition](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=de#data-type) erwähnt werden, werden unterstützt:

- Zeichenfolge
- Ganzzahl
- Double
- Boolesch
- Lang
- Kurz
- Byte
- Datum
- Datum-Uhrzeit


>[!MORELIKETHIS]
>
>- [Schemata](schemas.md)
