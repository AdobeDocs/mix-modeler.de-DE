---
title: Schemata
description: Erfahren Sie, wie Sie die Schemas verwalten, die zur Aufnahme von Daten in Adobe Mix Model erforderlich sind.
feature: Schemas
source-git-commit: 4a6cbda1ff0a779ebf8a38a4de3f797ed9e54b00
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 6%

---


# Schemata

So verwalten Sie Schemata, indem Sie die Daten unterstützen, die Sie in Adobe Experience Platform erfassen und im Adobe Mix-Modeler verwenden möchten:

1. Wechseln Sie zur Adobe Mix Modeler-Oberfläche.

1. Auswählen ![Schemas](../assets/icons/Schemas.svg) **[!UICONTROL Schemas]**, darunter **[!UICONTROL DATA MANAGEMENT]**.

Siehe [Übersicht über die Benutzeroberfläche von Schemas](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=de) für weitere Informationen.

## Aggregat- oder Zusammenfassungsdaten

Es wird dringend empfohlen, die Klasse &quot;XDM-Zusammenfassungsmetriken&quot;als Grundlage des Schemas zu verwenden, das allen Aggregat- oder Zusammenfassungsdaten zugrunde liegt, die Sie in Experience Platform erfassen und in Adobe Mix Modeler verwenden möchten.

Ein Beispiel für eine **[!DNL LumaPaidMarketingSchema]** Verwendung der XDM-Zusammenfassungsmetriken als Basisklasse und dedizierter Feldergruppen (mit Farben kommentiert) für die Metrik (**[!DNL AMMMetrics]**), Dimensionen (**[!DNL AMMDimensions]**) und anderen kundenspezifischen Informationen (**[!DNL CustomerSpecific]**).

![Zusammenfassungsschema](../assets/summary-schema.png)

Um einen Satz von Prüfeigenschaften zu definieren, wird dringend empfohlen, die Feldgruppe &quot;Prüfdetails des externen Quellsystems&quot;als Teil eines Schemas zu verwenden, das zur Erfassung von Aggregat- oder Zusammenfassungsdaten aus externen Quellen verwendet wird.
