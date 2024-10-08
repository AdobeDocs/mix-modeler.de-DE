---
title: Mix Modeler-Workflow
description: Machen Sie sich mit dem typischen Workflow für Mix Modeler vertraut.
feature: Ingest Data, Plans, Harmonized Data, Models
exl-id: 200ff846-5d78-4b25-a425-bfd558b88c88
source-git-commit: 9a6c1f1c12ab29da80a1997cfd31ca07b38eaa22
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# Mix Modeler-Workflow

In diesem Video erhalten Sie eine Einführung in den Benutzer-Workflow in Mix Modeler.

>[!VIDEO](https://video.tv.adobe.com/v/3424854/?learn=on)


Ein typischer Workflow in Mix Modeler besteht aus folgenden Aktivitäten:

![ALT-Text](/help/assets/ApplicationWorkflow.svg)

|  | Aktivität | Beschreibung |
|---|---|---|
| ![Daten](/help/assets/icons/Data.svg){width="100"} | [**Aufnehmen von Daten**](../ingest-data/overview.md) | Erfassen Sie Ereignisdaten von der Experience Platform (z. B. Adobe Analytics, Web SDK, andere Quellen), aggregierte Daten von Marketingkanälen (z. B. Fernsehen, umschlossene Gärten, E-Mail, eigene und betriebene Aktivitäten), Daten externer Faktoren von Kunden (z. B. Preisänderungen im Abonnementdienst) und interne Faktoren (z. B. Urlaubspläne). |
| ![DataCheck](/help/assets/icons/DataCheck.svg){width="100"} | [**Daten harmonisieren**](../harmonize-data/overview.md) | Konfigurieren Sie Zuordnungsregeln und Konfliktlösungsregeln, um die verschiedenen Marketing-Datensätze zusammenzuführen, die zum Messen und Planen der Kampagnenleistung in Mix Modeler erforderlich sind. |
| ![FileConfig](/help/assets/icons/FileGear.svg){width="100"} | [**Modelle konfigurieren**](../models/create.md) | Konfigurieren Sie Modellinstanzen mit Marketing-Touchpoints (z. B. Kanälen), Konversionsdefinitionen und internen und externen Faktoren. |
| ![FileData](/help/assets/icons/FileData.svg){width="100"} | [**Trainings- und Bewertungsmodelle**](../models/overview.md) | Erstellen Sie aggregierte Werte und Werte auf Ereignisebene mithilfe von maschinellem Lernen, Training und Scoring. |
| ![FileChart](/help/assets/icons/FileChart.svg){width="100"} | [**Pläne erstellen**](../plans/overview.md) | Bestimmen Sie anhand der Ergebnisse der Modelle des Mix Modelers die bestmögliche Zuordnung von Marketing-Fonds, um ein Geschäftsziel zu erreichen. |
| ![Dashboard](/help/assets/icons/Dashboard.svg){width="100"} | [**Dashboard &quot;Überblick&quot;**](../dashboard/overview.md) | Erhalten Sie mithilfe verschiedener konfigurierbarer Visualisierungen Einblicke in harmonisierte Daten, Modelle und Pläne. |

{style="table-layout:auto"}

Das unten stehende detaillierte datenorientierte Flussdiagramm zeigt, wie:

* Die harmonisierten Daten stützen sich auf:

   * Erlebnisereignisdaten (aus dem Analytics-Quell-Connector, der über Experience Platform-SDKs und APIs erfasst wird, über Quell-Connectoren erfasst wird oder die Streaming-Erfassung verwendet wird),
   * aggregierte oder zusammenfassende Daten aus den so genannten &quot;Walls Gardens&quot;(wie Facebook, YouTube), Traffic-Quellen oder Offline-Werbedaten und
   * Definitionen harmonisierter Felder und Datensatzregeln.

* Ein Modell basiert auf:

   * die aus den harmonisierten Daten resultierenden Konversions- und Marketing-Touchpoint-Definitionen und
   * Daten, die keine Marketing-Aggregate oder Zusammenfassungen enthalten und interne oder externe Faktoren enthalten.

* Mult-Touch-Attributionsereignis-Bewertungen können potenziell in den Experience Platform Data Lake zurückgespeist werden, um sie bei der nachfolgenden Modellkonfiguration, Schulung und Auswertung zu verwenden.

![Umfassender Workflow](/help/assets/comprehensive-workflow.svg)
