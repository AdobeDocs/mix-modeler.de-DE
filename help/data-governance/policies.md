---
title: Richtlinien
description: Erfahren Sie, wie Sie über Mix Modeler auf Richtlinien zugreifen können.
feature: Administration
exl-id: 4dba7c30-ad1e-4213-a2b0-afc55f2448a3
source-git-commit: 132dc18b84723358a7d65e2aaadd49cf1deb2dd8
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 11%

---

# Richtlinien

Sobald Sie den Workflow zum Erstellen eines Modells und Senden der Modellkonfiguration durchlaufen haben, überprüft [Richtliniendurchsetzung](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/enforcement/overview#automatic-enforcement), ob Verstöße vorliegen. Wenn ein Richtlinienverstoß auftritt, wird ein Popup angezeigt, das angibt, dass eine oder mehrere Richtlinien verletzt wurden. Mit dieser Prüfung soll sichergestellt werden, dass Ihre Datenvorgänge und Marketingaktionen innerhalb von Experience Platform mit Datennutzungsrichtlinien konform sind.

Standardmäßig prüft der Mix Modeler, ob Verstöße gegen von Adobe definierte Richtlinien im Zusammenhang mit den folgenden Bezeichnungen und Marketing-Aktionen vorliegen:

| Richtlinienname | Zugehörige Bezeichnung | Zugehörige Marketing-Aktion |
|---|---|---|
| Nutzungsanalyse und benutzerbasierte Messung beschränken | C8 | Analytics |
| Datenwissenschaft beschränken | C9 | Data Science |
| Datenexport beschränken | C12 | Datenexport |

Verstöße werden auch auf die Richtlinien überprüft, die Sie selbst definiert haben und die alle in der obigen Tabelle aufgelisteten Marketing-Aktionen enthalten.

Wenn Sie beim Erstellen einer Datensatzregel gegen eine Richtlinie verstoßen, wird ein Popup angezeigt, in dem Informationen zur Richtlinienverletzung angezeigt werden.

Beispiel:

- Sie die [!UICONTROL Restrict data science]-Richtlinie mit der zugehörigen Beschriftung [!UICONTROL C9] und der zugehörigen Marketing-Aktion [!UICONTROL Data Science] aktiviert haben,
- Sie haben die Beschriftung [!UICONTROL C9] - [!UICONTROL No data science] auf das Feld `totalCost` in Ihrem Konversionsdatenschema angewendet,
- Sie möchten eine Datensatzregel einrichten, die unter anderem das Feld `totalCost` des Konversionsdatenschemas dem harmonisierten Feld mit dem Namen `spend` (und dem Anzeigenamen `Spend`) zuordnet.

Wenn Sie die Datensatzregel speichern möchten, wird ein Popup mit dem Namen &quot;**[!UICONTROL Data governance policy violation detected]**&quot;angezeigt, in dem eine Liste der verletzten Richtlinien angezeigt wird. Wenn Sie den Richtliniennamen auswählen, sehen Sie in den [!UICONTROL Violation summary] eine Liste der [!UICONTROL Active data governance labels], die die angewendeten [!UICONTROL Entity], [!UICONTROL Type], [!UICONTROL Field] und [!UICONTROL Government labels] enthält.

<!-- pending screenshot -->

Wenn Sie eine Datennutzungsbezeichnung auf ein Schemafeld anwenden, das bereits in harmonisierten Daten verwendet wird, wird ein Popup angezeigt, in dem Informationen zur Richtlinienverletzung angezeigt werden.

Beispiel:

- Sie haben eine Datensatzregel eingerichtet, die unter anderem das Feld `totalCost` Ihres Konversionsdatenschemas dem harmonisierten Feld mit dem Namen `spend` (und dem Anzeigenamen `Spend`) zuordnet.
- Sie haben die harmonisierten Daten mindestens einmal erfolgreich synchronisiert (siehe [Datensatzregeln - Daten synchronisieren](/help/harmonize-data/dataset-rules.md#sync-data)).
- Sie aktivieren die [!UICONTROL Restrict data science]-Richtlinie mit der zugehörigen Beschriftung [!UICONTROL C9] und der zugehörigen Marketing-Aktion [!UICONTROL Data Science],
- Sie möchten die Beschriftung [!UICONTROL C9] - [!UICONTROL No data science] auf das Feld `totalCost` im Umrechnungsdatenschema anwenden.

Wenn Sie Ihre Schemaaktualisierung speichern möchten, wird ein &quot;**[!UICONTROL Data governance policy violation detected]**&quot;-Popup angezeigt, in dem eine Liste der verletzten Richtlinien angezeigt wird. Wählen Sie den Richtliniennamen im [!UICONTROL Violation summary] aus, um weitere Details in der Liste [!UICONTROL Data Lineage] zu finden.

<!-- pending screenshot -->

## Durch Verletzung erkannte Popovers

Die festgestellten Verstöße gegen Data Governance-Richtlinien enthalten spezifische Informationen über den Verstoß. Sie können diese Verstöße durch Richtlinieneinstellungen und andere Maßnahmen beheben, die nicht direkt mit dem Konfigurations-Workflow zusammenhängen. Sie können beispielsweise die Beschriftungen so ändern, dass bestimmte Felder für Datenwissenschaften verwendet werden dürfen. Alternativ können Sie auch die Modellkonfiguration selbst ändern, sodass das Modell kein Objekt mit einer Datennutzungsbezeichnung verwendet.

Die Auswahl ![Datenschutz](/help/assets/icons/Privacy.svg) **[!UICONTROL Policies]** in der linken Leiste bietet Zugriff auf die Oberfläche [!UICONTROL Policies] von Experience Platform, sodass Sie Ihre Richtlinien, Bezeichnungen und Marketing-Aktionen verwalten können.

<!--
Currently,  Mix Modeler does not support all of the data governance functionality offered by Experience Platform. Field level access control is supported. See [Field level access control](../harmonize-data/dataset-rules.md#field-level-access-control)
-->

>[!MORELIKETHIS]
>
>[Datennutzungsrichtlinien – Übersicht](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/policies/overview)
>
>

