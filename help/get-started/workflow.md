---
title: Mix Modeler-Workflow
description: Den typischen Workflow für Mix Modeler verstehen.
feature: Ingest Data, Plans, Harmonized Data, Models
exl-id: 200ff846-5d78-4b25-a425-bfd558b88c88
TQID: https://experienceleague.adobe.com/PAKsHAqpIeBVCJGIPS2ZqWw-vVpS9LUpYdJRFKP0ynY
product_v2:
  - id: b88c80e3-31df-4609-989d-d4dac0e6d973
feature_v2:
  - id: e0abf868-dae2-4c1c-83e9-b21799232845
  - id: fbd94e4b-f9b8-42a4-8df5-3f917aabae24
  - id: a567f0f7-0057-4079-8ded-5b24cc25af15
  - id: f40f1683-8300-4054-aab8-77da06ad63ff
  - id: d822825b-9821-40d5-9b0d-42a9e3f317c5
subfeature_v2:
  - id: ad7101f7-ae92-401b-a25a-d3060d42989d
  - id: a4dc3e7d-bd07-4ac8-8e49-ff2e8fecf1e7
  - id: ee1bf083-e090-4def-936b-c111d29f42d0
  - id: d1167c89-f64a-42ca-ac95-1d91b7790df2
  - id: bc2f5225-03d4-4bc8-89ec-99d78c30e6dd
  - id: d4b8ba18-64c1-4413-be54-74405ec7f558
  - id: ba4fd72c-282e-4fb6-abc1-08e6fb87b2ad
  - id: b4655f7e-1a6e-4fa3-a7c5-3c34d4786e49
  - id: b2d4aeb9-eabe-49f6-8edb-bb2862d5980b
  - id: c89e26b6-808d-4500-8b01-450a63466999
  - id: a9505d76-24a1-4ffe-bd01-6ac32d5af453
  - id: cb40363e-1205-4921-971c-9ee6bdb18329
  - id: d7b067e6-4f39-41e9-a081-7650346a84cd
  - id: b2520ae7-8f6c-4952-935e-aacc2c10256f
  - id: e6c284e0-b6e6-4f82-bf96-e96bb5157b90
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
autotag-review: '2026-05-01T09:15:33.908Z'
source-git-commit: 5579087b9381c4d8e909ed5fe3099fd42d5c6799
workflow-type: tm+mt
source-wordcount: 238
ht-degree: 1%

---

# Mix Modeler-Workflow

In diesem Video erhalten Sie eine Einführung in den Benutzer-Workflow in Mix Modeler.

>[!VIDEO](https://video.tv.adobe.com/v/3440213/?captions=ger&learn=on)


Ein typischer Workflow in Mix Modeler besteht aus den folgenden Aktivitäten:

![ALT-Text](/help/assets/ApplicationWorkflow.svg)

|  | Aktivität | Beschreibung |
|---|---|---|
| ![Daten](/help/assets/icons/Data.svg){width="100"} | [**Daten aufnehmen**](../ingest-data/overview.md) | Ereignisdaten aus Experience Platform (z. B. Adobe Analytics, Web SDK, andere Quellen), aggregierte Daten aus Marketing-Kanälen (z. B. TV, ummauerte Gärten, E-Mail, eigene und betriebene Aktivitäten), Daten zu externen Faktoren von Kunden (z. B. Preisänderungen bei Abonnement-Services) und Daten zu internen Faktoren (z. B. Urlaubspläne) aufnehmen. |
| ![DataCheck](/help/assets/icons/DataCheck.svg){width="100"} | [**Daten harmonisieren**](../harmonize-data/overview.md) | Konfigurieren Sie Zuordnungsregeln und Konfliktlösungsregeln, um die verschiedenen Marketing-Datensätze zusammenzuführen, die zur Messung und Planung der Kampagnenleistung in Mix Modeler erforderlich sind. |
| ![FileConfig](/help/assets/icons/FileGear.svg){width="100"} | [**Erstellen von Modellen**](../models/overview.md) | Erstellen Sie Modellinstanzen mit Marketing-Touchpoints (z. B. Kanälen), Konversionsdefinitionen und internen und externen Faktoren. |
| ![FileData](/help/assets/icons/FileData.svg){width="100"} | [**Trainieren und Bewerten von Modellen**](../models/overview.md) | Erstellen Sie aggregierte Werte und Werte auf Ereignisebene mithilfe von Machine-Learning-Schulungen und -Bewertungen. |
| ![FileChart](/help/assets/icons/FileChart.svg){width="100"} | [**Pläne erstellen**](../plans/overview.md) | Erstellen und Erstellen von Plänen Ermitteln Sie mithilfe der Ergebnisse der Mix Modeler-Modelle die optimale Zuordnung von Marketing-Mitteln, um ein Geschäftsziel zu erreichen. |
| ![Dashboard](/help/assets/icons/Dashboard.svg){width="100"} | [**Übersichts-Dashboard**](../dashboard/overview.md) | Erhalten Sie mithilfe verschiedener konfigurierbarer Visualisierungen Einblicke in harmonisierte Daten, Modelle und Pläne. |

{style="table-layout:auto"}

Nachfolgend finden Sie einen Überblick darüber, wie Eingabedaten in Mix Modeler fließen können und wie Mix Modeler Ausgabedaten für die eigene Benutzeroberfläche, aber auch für andere Lösungen wie Customer Journey Analytics erzeugen kann.

![Datenfluss der Mix Modeler-Eingabe](../assets/mm-input-output.png)

<!--
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
