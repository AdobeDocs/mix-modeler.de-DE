---
title: Mix Modeler-Workflow
description: Den typischen Workflow für Mix Modeler verstehen.
feature: Ingest Data, Plans, Harmonized Data, Models
exl-id: 200ff846-5d78-4b25-a425-bfd558b88c88
source-git-commit: f12eea7454d1c81b347dc4960f5c491d81725f7d
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 1%

---

# Mix Modeler-Workflow

In diesem Video erhalten Sie eine Einführung in den Benutzer-Workflow in Mix Modeler.

>[!VIDEO](https://video.tv.adobe.com/v/3440213/?learn=on&captions=ger)


Ein typischer Workflow in Mix Modeler besteht aus den folgenden Aktivitäten:

![ALT-Text](/help/assets/ApplicationWorkflow.svg)

|  | Aktivität | Beschreibung |
|---|---|---|
| ![Daten](/help/assets/icons/Data.svg){width="100"} | [**Daten aufnehmen**](../ingest-data/overview.md) | Nehmen Sie Ereignisdaten vom Experience Platform auf (z. B. Adobe Analytics, Web SDK, andere Quellen), aggregierte Daten von Marketing-Kanälen (z. B. TV, ummauerte Gärten, E-Mail, eigene und betriebene Aktivitäten), Daten zu externen Faktoren von Kunden (z. B. Preisänderungen im Abonnement-Service) und Daten zu internen Faktoren (z. B. Urlaubspläne). |
| ![DataCheck](/help/assets/icons/DataCheck.svg){width="100"} | [**Daten harmonisieren**](../harmonize-data/overview.md) | Konfigurieren Sie Zuordnungsregeln und Konfliktlösungsregeln, um die verschiedenen Marketing-Datensätze zusammenzuführen, die zur Messung und Planung der Kampagnenleistung im Mix Modeler erforderlich sind. |
| ![FileConfig](/help/assets/icons/FileGear.svg){width="100"} | [**Erstellen von Modellen**](../models/overview.md) | Erstellen Sie Modellinstanzen mit Marketing-Touchpoints (z. B. Kanälen), Konversionsdefinitionen und internen und externen Faktoren. |
| ![FileData](/help/assets/icons/FileData.svg){width="100"} | [**Trainieren und Bewerten von Modellen**](../models/overview.md) | Erstellen Sie aggregierte Werte und Werte auf Ereignisebene mithilfe von Machine-Learning-Schulungen und -Bewertungen. |
| ![FileChart](/help/assets/icons/FileChart.svg){width="100"} | [**Pläne erstellen**](../plans/overview.md) | Erstellen und Erstellen von Plänen Ermitteln Sie anhand der Ergebnisse der Modelle von Mix Modeler die beste Aufteilung der Marketing-Mittel, um ein Geschäftsziel zu erreichen. |
| ![Dashboard](/help/assets/icons/Dashboard.svg){width="100"} | [**Übersichts-Dashboard**](../dashboard/overview.md) | Erhalten Sie mithilfe verschiedener konfigurierbarer Visualisierungen Einblicke in harmonisierte Daten, Modelle und Pläne. |

{style="table-layout:auto"}

<!---
The detailed data-oriented flowchart below illustrates how:

* harmonized data is based on:

  * experience event data (originating from Analytics source connector, collected through Experience Platform SDKs and APIs, ingested through source connectors, or using streaming ingestion),
  * aggregate or summary data from walled gardens (like Facebook, YouTube), traffic sources, or offline advertising data, and 
  * definitions of harmonized fields and dataset rules.

* a model is based on:

  * the conversion and marketing touchpoint definitions resulting from the harmonized data and 
  * non-marketing aggregate or summary data containing internal or external factors.

* mult-touch attribution event scores can potentially be fed back into Experience Platform data lake for use in subsequent model configuration, training and scoring.

![Comprehensive workflow](/help/assets/comprehensive-workflow.svg)

-->
