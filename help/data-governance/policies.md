---
title: Richtlinien
description: Erfahren Sie, wie Sie von Mix Modeler aus auf Richtlinien zugreifen können.
feature: Administration
exl-id: 4dba7c30-ad1e-4213-a2b0-afc55f2448a3
TQID: https://experienceleague.adobe.com/fk6qAZS7Uymx2dzptcazBieXIJ3mGF2pjG-EDhm-Kh4
product_v2:
  - id: b88c80e3-31df-4609-989d-d4dac0e6d973
feature_v2:
  - id: f6633d1c-3d2d-4f48-95d4-4bbc9913db52
subfeature_v2:
  - id: fd80ec6b-9b9e-448a-a6d0-b0c9a15da6b8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
autotag-review: '2026-05-01T09:17:02.907Z'
source-git-commit: 5579087b9381c4d8e909ed5fe3099fd42d5c6799
workflow-type: tm+mt
source-wordcount: 507
ht-degree: 9%

---

# Richtlinien

Sobald Sie den Workflow zur Modellerstellung abgeschlossen haben und die Konfiguration des Modells übermitteln, wird [Richtliniendurchsetzung](https://experienceleague.adobe.com/de/docs/experience-platform/data-governance/enforcement/overview#automatic-enforcement) überprüft, ob Verstöße vorliegen. Wenn ein Richtlinienverstoß auftritt, wird ein Popup angezeigt, das angibt, dass eine oder mehrere Richtlinien verletzt wurden. Diese Prüfung dient dazu, sicherzustellen, dass Ihre Datenvorgänge und Marketing-Aktionen in Experience Platform mit Datennutzungsrichtlinien konform sind.

Standardmäßig sucht Mix Modeler nach Verstößen gegen von Adobe definierte Richtlinien, die mit den folgenden Kennzeichnungen und Marketing-Aktionen verbunden sind:

| Richtlinienname | Zugeordnete Kennzeichnung | Zugeordnete Marketing-Aktion |
|---|---|---|
| Nutzungsanalysen und benutzerbasierte Messung einschränken | C8 | Analytics |
| Datenwissenschaft einschränken | C9 | Data Science |
| Datenexport einschränken | C12 | Datenexport |

Verstöße werden auch für die Richtlinien überprüft, die Sie selbst definiert haben und die keine der in der obigen Tabelle aufgeführten Marketing-Aktionen enthalten.

Wenn Sie beim Erstellen einer Datensatzregel eine Richtlinie verletzen, wird ein Pop-up angezeigt, in dem Informationen über die Richtlinienverletzung angezeigt werden.

Beispiel:

- Sie haben die [!UICONTROL Restrict data science]-Richtlinie mit den zugehörigen [!UICONTROL C9] und den zugehörigen Marketing-[!UICONTROL Data Science] aktiviert.
- Sie die Bezeichnung [!UICONTROL C9] - [!UICONTROL No data science] auf das Feld `totalCost` in Ihrem Konversionsdatenschema angewendet haben,
- Sie sollten eine Datensatzregel einrichten, die unter anderem das `totalCost` Feld des Konversionsdatenschemas dem harmonisierten Feld mit dem Namen `spend` (und dem Anzeigenamen `Spend`) zuordnet.

Wenn Sie die Datensatzregel speichern möchten, wird ein **[!UICONTROL Data governance policy violation detected]**-Popup mit einer Liste der verletzten Richtlinien angezeigt. Wenn Sie den Richtliniennamen auswählen, wird im [!UICONTROL Violation summary] eine Liste der [!UICONTROL Active data governance labels] angezeigt, die [!UICONTROL Entity], [!UICONTROL Type], [!UICONTROL Field] und angewendete [!UICONTROL Government labels] enthält.

<!-- pending screenshot -->

Beim Anwenden einer Datennutzungskennzeichnung auf ein Schemafeld, das bereits in harmonisierten Daten verwendet wird, wird ein Pop-up angezeigt, in dem Informationen zur Richtlinienverletzung angezeigt werden.

Beispiel:

- Sie haben eine Datensatzregel eingerichtet, die unter anderem das `totalCost` Feld Ihres Konversionsdatenschemas dem harmonisierten Feld mit dem Namen `spend` (und dem Anzeigenamen `Spend`) zuordnet.
- Sie haben die harmonisierten Daten mindestens einmal erfolgreich synchronisiert (siehe [Datensatzregeln - Daten synchronisieren](/help/harmonize-data/dataset-rules.md#sync-data)).
- Sie aktivieren die [!UICONTROL Restrict data science] Richtlinie mit den zugehörigen [!UICONTROL C9] und den zugehörigen Marketing-[!UICONTROL Data Science],
- Sie möchten die Beschriftung [!UICONTROL C9] - [!UICONTROL No data science] auf das Feld `totalCost` in Ihrem Konversionsdatenschema anwenden.

Wenn Sie Ihre Schemaaktualisierung speichern möchten, wird ein **[!UICONTROL Data governance policy violation detected]**-Popup mit einer Liste der verletzten Richtlinien angezeigt. Wählen Sie den Richtliniennamen in der [!UICONTROL Violation summary] aus, um weitere Details in der [!UICONTROL Data Lineage] Liste zu finden.

<!-- pending screenshot -->

## Verstoß erkannt Pop-overs

Die Pop-overs „Verletzung der Data Governance-Richtlinie erkannt“ enthalten spezifische Informationen zur Verletzung. Sie können diese Verstöße durch Richtlinieneinstellungen und andere Maßnahmen beheben, die nicht direkt mit dem Konfigurations-Workflow zusammenhängen. Sie können beispielsweise die Kennzeichnungen so ändern, dass bestimmte Felder für datenwissenschaftliche Zwecke verwendet werden dürfen. Alternativ können Sie auch die Modellkonfiguration selbst ändern, sodass das Modell kein Objekt mit einer Datennutzungskennzeichnung verwendet.

Die ![Datenschutz](/help/assets/icons/Privacy.svg)-**[!UICONTROL Policies]** in der linken Leiste bietet Zugriff auf die [!UICONTROL Policies] von Experience Platform, sodass Sie Ihre Richtlinien, Kennzeichnungen und Marketing-Aktionen verwalten können.

<!--
Currently,  Mix Modeler does not support all of the data governance functionality offered by Experience Platform. Field level access control is supported. See [Field level access control](../harmonize-data/dataset-rules.md#field-level-access-control)
-->

>[!MORELIKETHIS]
>
>[Datennutzungsrichtlinien - Übersicht](https://experienceleague.adobe.com/de/docs/experience-platform/data-governance/policies/overview)
>
>

