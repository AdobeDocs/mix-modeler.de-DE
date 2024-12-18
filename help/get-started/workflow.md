---
title: Mix Modeler-Workflow
description: Den typischen Workflow für Mix Modeler verstehen.
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


Ein typischer Workflow in Mix Modeler besteht aus den folgenden Aktivitäten:

![ALT-Text](/help/assets/ApplicationWorkflow.svg)

|  | Aktivität | Beschreibung |
|---|---|---|
| ![Daten](/help/assets/icons/Data.svg){width="100"} | [**Daten aufnehmen**](../ingest-data/overview.md) | Nehmen Sie Ereignisdaten vom Experience Platform auf (z. B. Adobe Analytics, Web SDK, andere Quellen), aggregierte Daten von Marketing-Kanälen (z. B. TV, ummauerte Gärten, E-Mail, eigene und betriebene Aktivitäten), Daten zu externen Faktoren von Kunden (z. B. Preisänderungen im Abonnement-Service) und Daten zu internen Faktoren (z. B. Urlaubspläne). |
| ![DataCheck](/help/assets/icons/DataCheck.svg){width="100"} | [**Daten harmonisieren**](../harmonize-data/overview.md) | Konfigurieren Sie Zuordnungsregeln und Konfliktlösungsregeln, um die verschiedenen Marketing-Datensätze zusammenzuführen, die zur Messung und Planung der Kampagnenleistung im Mix Modeler erforderlich sind. |
| ![FileConfig](/help/assets/icons/FileGear.svg){width="100"} | [**Modelle konfigurieren**](../models/create.md) | Konfigurieren Sie Modellinstanzen mit Marketing-Touchpoints (z. B. Kanälen), Konversionsdefinitionen und internen und externen Faktoren. |
| ![FileData](/help/assets/icons/FileData.svg){width="100"} | [**Trainieren und Bewerten von Modellen**](../models/overview.md) | Erstellen Sie aggregierte Werte und Werte auf Ereignisebene mithilfe von Machine-Learning-Schulungen und -Bewertungen. |
| ![FileChart](/help/assets/icons/FileChart.svg){width="100"} | [**Pläne erstellen**](../plans/overview.md) | Ermitteln Sie anhand der Ergebnisse der Modelle von Mix Modeler die beste Aufteilung der Marketing-Mittel, um ein Geschäftsziel zu erreichen. |
| ![Dashboard](/help/assets/icons/Dashboard.svg){width="100"} | [**Übersichts-Dashboard**](../dashboard/overview.md) | Erhalten Sie mithilfe verschiedener konfigurierbarer Visualisierungen Einblicke in harmonisierte Daten, Modelle und Pläne. |

{style="table-layout:auto"}

Das detaillierte datenorientierte Flussdiagramm unten zeigt, wie:

* Harmonisierte Daten basieren auf:

   * Erlebnisereignisdaten (aus dem Analytics-Quell-Connector, erfasst über Experience Platform-SDKs und APIs, aufgenommen über Quell-Connectoren oder mithilfe der Streaming-Aufnahme),
   * aggregierte oder zusammengefasste Daten aus ummauerten Gärten (wie Facebook, YouTube), Traffic-Quellen oder Offline-Werbedaten und
   * Definitionen harmonisierter Felder und Datensatzregeln.

* Ein Modell basiert auf:

   * die Konversions- und Marketing-Touchpoint-Definitionen, die sich aus den harmonisierten Daten und
   * Nicht-Marketing-Aggregat- oder -Zusammenfassungsdaten, die interne oder externe Faktoren enthalten.

* Multi-Touch-Attributionsereignis-Scores können möglicherweise in den Experience Platform Data Lake zurückgeleitet werden, um sie in nachfolgenden Modellkonfigurationen, Schulungen und Bewertungen zu verwenden.

![Umfassender Workflow](/help/assets/comprehensive-workflow.svg)
