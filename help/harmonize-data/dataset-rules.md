---
title: Datensatzregeln
description: Erfahren Sie, wie Sie Datensatzregeln definieren, die im Rahmen der Harmonisierung Ihrer Daten in Mix Modeler verwendet werden.
feature: Harmonized Data, Dataset Rules
exl-id: 57d7940a-2900-4814-a30d-bb02bff7615d
source-git-commit: 9a6c1f1c12ab29da80a1997cfd31ca07b38eaa22
workflow-type: tm+mt
source-wordcount: '1313'
ht-degree: 1%

---

# Datensatzregeln

Datensatzregeln unterstützen Sie bei der Zuordnung Ihrer harmonisierten Felder zu Feldern aus den in Mix Modeler erfassten Daten.

* Für aggregierte Daten, die Sie in Adobe Experience Platform erfasst haben, ordnen Sie eines oder mehrere der verfügbaren Datensatzfelder den entsprechenden harmonisierten Feldern zu.
* Für Ereignisdaten können Sie ein oder mehrere harmonisierte Felder einzeln Feldern aus dem Datensatz zuordnen, entweder direkt oder unter Verwendung von Bedingungen.


## Verwalten von Datensatzregeln

So zeigen Sie eine Tabelle der verfügbaren Datensatzregeln in der Mix Modeler-Oberfläche an:

1. Wählen Sie ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** in der linken Leiste aus.

1. Wählen Sie in der oberen Leiste **[!UICONTROL Dataset rules]** aus. Sie sehen eine Tabelle der Datensatzregeln.

Die Tabellenspalten geben Details zu den Datensatzregeln an:

| Spaltenname | Details |
| ---------------------- | ----------|
| Datensatz | Der Name des Datensatzes. |
| Quelle | Die Quelle des Datensatzes: Adobe Analytics, Erlebnisereignisse, Zusammenfassung (Aggregat) oder Consumer Experience Events. |
| Schema | Das Schema, dem der Datensatz entspricht. Sie können den Schemanamen schnell auswählen, um das Schema in einer neuen Registerkarte im Schema-Editor in ![Schema](/help/assets/icons/Schemas.svg) [Schemas](../ingest-data/schemas.md) zu öffnen. |
| Granularität | Die Granularität der Daten im Datensatz. Mögliche Werte sind Täglich, Wöchentlich, Monatlich oder Jährlich. |
| Beginn der Woche | Gibt an, welcher Wochentag als Beginn einer neuen Woche für den spezifischen Datensatz betrachtet wird. |
| Status | Der Status des Felds: <p><span style="color:gray"></span> Entwurf oder <p><span style="color:green"></span> Aktiv |
| Zuletzt geändert | Daten und Uhrzeit der letzten Änderung der Datensatzregel. |

{style="table-layout:auto"}

### Erstellen einer Datensatzregel

Um eine Datensatzregel zu erstellen, wählen Sie in der Benutzeroberfläche ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** des Mix Modelers im Assistenten **[!UICONTROL Dataset rules configuration]** die Option **[!UICONTROL Create a dataset rule]** aus.

Im Bildschirm **[!UICONTROL Create]**:

1. Wählen Sie in **[!UICONTROL Dataset details]** einen Datensatz aus **[!UICONTROL Select dataset]** aus, um die Konfiguration zu starten. In der Liste werden Datensätze in **[!UICONTROL Consumer Experience Events]**, **[!UICONTROL Adobe Analytics]**, **[!UICONTROL Experience Event]** und **[!UICONTROL Summary]** kategorisiert.

1. Wählen Sie einen Tag für die **[!UICONTROL Start of the week]** aus.

1. Wählen Sie **[!UICONTROL Daily]**, **[!UICONTROL Weekly]**, **[!UICONTROL Monthly]** oder **[!UICONTROL Yearly]** für **[!UICONTROL Granularity]** aus.

1. Wenn Sie einen Datensatz der Kategorie **[!UICONTROL Summary]** ausgewählt haben:

   1. Um festzulegen, ob Daten für den Datensatz vorhandene Daten aggregieren oder ersetzen, wählen Sie **[!UICONTROL Aggregation]** oder **[!UICONTROL Replacement]** für **[!UICONTROL Data restatement is by]** aus.

   1. Ordnen Sie jeden der **[!UICONTROL Available dataset fields]** den entsprechenden **[!UICONTROL Standard harmonized fields]** in **[!UICONTROL Map to harmonized fields]** zu. Wenn Sie ein Datensatzfeld nicht einem harmonisierten Feld zuordnen möchten, wählen Sie explizit **[!UICONTROL -- None --]** aus.

   1. Wenn Sie ein neues harmonisiertes Feld benötigen, das nicht in der Liste verfügbar ist, wählen Sie **[!UICONTROL Create New]** aus, um ein neues harmonisiertes Feld zu erstellen. Das Dialogfeld wird wie unter [Neues harmonisiertes Feld hinzufügen](fields.md#add-a-harmonized-field) beschrieben angezeigt.

   1. Wenn die Zuordnung für alle Felder der Regel abgeschlossen ist, wählen Sie **[!UICONTROL Save as draft]** , um eine Entwurfsversion der Regel zu speichern, oder **[!UICONTROL Save]**, um die Regel zu speichern und zu aktivieren. Wählen Sie **[!UICONTROL Cancel]** aus, um die Regelkonfiguration abzubrechen.

      ![Erstellen von Datensatzregeln](/help/assets/dataset-create-summary.png)

1. Wenn Sie einen Datensatz der Ereigniskategorie (**[!UICONTROL Experience Events]**, **[!UICONTROL Adobe Analytics]**, **[!UICONTROL Consumer Experience Events]**) im Feld unter **[!UICONTROL Map to harmonized fields]** ausgewählt haben:

   1. Wählen Sie ein harmonisiertes Feld aus **[!UICONTROL Standard harmonized field]** aus.

   1. Wenn das ausgewählte harmonisierte Feld vom Typ Metrik ist:

      1. Wählen Sie **[!UICONTROL Count]** oder **[!UICONTROL Sum]** aus **[!UICONTROL Mapping type]** aus.

      1. Wählen Sie ein **[!UICONTROL *AEP-Datensatzfeld *]**aus, dem das harmonisierte Feld standardmäßig zugeordnet werden soll.

   1. Wenn das ausgewählte Feld eine Dimension vom Typ hat:

      1. Wählen Sie **[!UICONTROL Map Into]** oder **[!UICONTROL Case]** aus **[!UICONTROL Mapping type]** aus.

      1. Wenn Sie &quot;**[!UICONTROL Map Into]**&quot;ausgewählt haben, wählen Sie &quot;**[!UICONTROL Field]**&quot;und &quot;**[!UICONTROL *AEP-Datensatzfeld *]**&quot;oder &quot;**[!UICONTROL Value]**&quot;und einen Standardwert, um das harmonisierte Feld standardmäßig dem Datensatzfeld oder dem eingegebenen Wert zuzuordnen.

      1. Wenn Sie &quot;**[!UICONTROL Case]**&quot;auswählen, wählen Sie &quot;**[!UICONTROL Field]**&quot;und &quot;**[!UICONTROL *AEP-Datensatzfeld *]**&quot;oder &quot;**[!UICONTROL Value]**&quot;und einen Standardwert, um das harmonisierte Feld standardmäßig dem Datensatzfeld oder dem eingegebenen Wert zuzuordnen.

         1. Um explizit Werte festzulegen, definieren Sie einen oder mehrere Fälle, die aus einer oder mehreren Bedingungen bestehen. Jede Bedingung kann prüfen, ob es **[!UICONTROL Exists]** oder **[!UICONTROL Not Exists]** oder **[!UICONTROL Contains]**, **[!UICONTROL Not Contains]**, **[!UICONTROL Equals]**, **[!UICONTROL Not Equals]**, **[!UICONTROL Starts With]** oder **[!UICONTROL Ends With]** um ein bestimmtes Feld für den AEP-Datensatz **[!UICONTROL *Eingabefeld *]**geht.**[!UICONTROL **]**

         1. Um eine weitere Groß-/Kleinschreibung hinzuzufügen, wählen Sie ![Hinzufügen](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add case]** und klicken Sie auf ![Hinzufügen](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add condition]**, um eine weitere Bedingung hinzuzufügen.

         1. Um eine Groß-/Kleinschreibung oder Bedingung zu löschen, wählen Sie im entsprechenden Container ![Schließen](/help/assets/icons/Close.svg) aus.

         1. Um auszuwählen, ob eine oder alle Bedingungen für einen Fall gelten sollen, wählen Sie **[!UICONTROL Any of]** oder **[!UICONTROL All of]**.

         1. Um den Ergebniswert für einen Fall festzulegen, geben Sie den Wert bei **[!UICONTROL Then]** ein.

      Das Beispiel unten

      * verwendet eine **[!UICONTROL Map Into]** **[!UICONTROL Mapping type]**, um das harmonisierte Feld **[!UICONTROL Channel Type At Source]** dem Feld **[!UICONTROL channel_type]** aus dem Datensatz **[!DNL Luma Transactions]** zuzuordnen.

      * verwendet eine **[!UICONTROL Case]** **[!UICONTROL Mapping type]** , um den Wert des Felds **[!UICONTROL marketing.campaignName]** im Datensatz **[!DNL Luma Transactions]** bedingt dem harmonisierten Feld **[!UICONTROL Campaign]** zuzuordnen. Das harmonisierte Feld Kampagne ist auf Folgendes festgelegt:

         * `Black Friday` , wenn der **[!UICONTROL marketing.campaignName]** `_black_friday` oder `BlackFriday` ist.
         * in allen anderen Fällen auf den Wert von **[!UICONTROL marketing.campaignName]** gesetzt.

        ![Ereignis für Datensatzregel](/help/assets/dataset-create-event.png)

1. Wählen Sie ![Hinzufügen](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add field]** aus, um zusätzliche Felder zu definieren.

Wenn Sie fertig sind, wählen Sie **[!UICONTROL Save as draft]** , um eine Entwurfsversion der Regel zu speichern, oder **[!UICONTROL Save]**, um die Regel zu speichern und zu aktivieren. Wählen Sie **[!UICONTROL Cancel]** aus, um die Regelkonfiguration abzubrechen.


### Eine Datensatzregel bearbeiten

Um eine Datensatzregel zu bearbeiten, gehen Sie in der Oberfläche ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** in Mix Modeler wie folgt vor:

1. Wählen Sie ![Mehr](/help/assets/icons/More.svg) in der Spalte **[!UICONTROL Dataset]** für die Datensatzregel aus, die Sie bearbeiten möchten.
1. Wählen Sie im Kontextmenü ![Bearbeiten](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]** aus, um mit der Bearbeitung der Datensatzregel zu beginnen. Weitere Informationen finden Sie unter [Erstellen einer Datensatzregel](#create-a-dataset-rule) .


### Eine Datensatzregel löschen

Um eine Datensatzregel zu löschen, gehen Sie in der Oberfläche ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** in Mix Modeler wie folgt vor:

1. Wählen Sie ![Mehr](/help/assets/icons/More.svg) in der Spalte **[!UICONTROL Dataset]** für die Datensatzregel aus, die Sie löschen möchten.
1. Wählen Sie im Kontextmenü ![Löschen](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** aus, um die Datensatzregel zu löschen. Sie werden zur Bestätigung aufgefordert. Wählen Sie **[!UICONTROL Delete]** aus, um die ausgewählte Datensatzregel dauerhaft zu löschen.


## Daten synchronisieren

So synchronisieren Sie Daten zwischen Ihren harmonisierten Daten und Zusammenfassungs- und / oder Ereignis-Datensätzen, während Sie die Logik in Ihren Datensatzregeln anwenden:

1. Wählen Sie **[!UICONTROL Sync data]** aus.

1. Wählen Sie im Dialogfeld **[!UICONTROL Sync data for dataset rules]** entweder
   * **[!UICONTROL Refresh harmonized data for summary datasets]**,
   * **[!UICONTROL Refresh harmonized data for event datasets]** oder
   * **[!UICONTROL Refresh harmonized data for both summary + event datasets]**.

1. Um die Synchronisierung auf Grundlage der definierten Datensatzregeln zwischen harmonisierten Daten und Daten in Datensätzen zu starten, wählen Sie **[!UICONTROL Sync]** aus. Um die Synchronisierung abzubrechen, wählen Sie **[!UICONTROL Cancel]** aus.

   ![Daten synchronisieren](/help/assets/sync-data.png)


## Voreinstellungen zur Datenzusammenführung

>[!NOTE]
>
>[!BADGE beta]{type=Informative}

Die Voreinstellungen für die Datenzusammenführung helfen bei der Lösung von Konflikten, wenn Daten aus zusammengefassten und Ereignisdatenquellen zusammengeführt werden. Anwendungsbeispiele sind:

* dieselbe Werbemetrik in mehreren Datensätzen gemessen und gemeldet wird oder
* Die Metrikmessung kann in einigen Datensätzen unvollständig sein, während ein anderer Datensatz eine Obermenge einer bestimmten Metrik sein kann, was zu einer doppelten Zählung führt.

Um präzise Modellprognosen zu gewährleisten, können Sie Voreinstellungen für die Datenzusammenführung definieren:

1. Wählen Sie ![Voreinstellungen für die Datenzusammenführung](/help/assets/icons/Merge.svg) [!BADGE Beta] aus.

1. In der **[!UICONTROL Data merge preferences]** [!BADGE beta]{type=Informative}

   ![Voreinstellungen für die Datenzusammenführung](/help/assets/data-merge-preferences.png)

   * Wählen Sie einen **[!UICONTROL Default metric preference]** aus. Die ausgewählte Standardmetrik-Voreinstellung wird angewendet, wenn während der Harmonisierung mehrere Datenquellen ein Metrikfeld für einen bestimmten Kanal aktualisieren. Die Voreinstellung wird auf Sandbox-Ebene angewendet, es sei denn, sie wird für bestimmte metrikbasierte Voreinstellungen überschrieben. Sie können zwischen **[!UICONTROL Summary data]**, **[!UICONTROL Event data]** und **[!UICONTROL Sum of summary and event data]** wählen.

   * So fügen Sie bestimmte metrikbasierte Voreinstellungen hinzu:

      1. Wählen Sie ![Plus](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add a metric]** aus.
         1. Wählen Sie eine Metrik aus der Liste **[!UICONTROL *Metrikauswahl *]**aus.
         1. Wählen Sie **[!UICONTROL CHANNELS]** oder **[!UICONTROL CONVERSION TYPES]** aus. Wählen Sie in der Liste **[!UICONTROL All]** oder einen bestimmten Kanal oder Konversionstyp aus.
         1. Wählen Sie **[!UICONTROL Summary]** oder **[!UICONTROL Event]** aus, um festzulegen, ob Zusammenfassungsdaten oder Ereignisdaten für die Metrik (und den gesamten oder ausgewählten Kanal) beim Zusammenführen von Daten bevorzugt werden.

         So fügen Sie einen oder mehrere zusätzliche Kanal- oder Konversionstypen hinzu:

         1. Wählen Sie ![Plus](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add a channel]** oder ![Plus](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add a conversion type]** aus.
         1. Wählen Sie **[!UICONTROL Summary]** oder **[!UICONTROL Event]** aus.

         Um einen Kanal oder Konvertierungstyp zu löschen, wählen Sie ![Cross](/help/assets/icons/Close.svg) aus.

      1. Um spezifischere metrikbasierte Voreinstellungen hinzuzufügen, wiederholen Sie den vorherigen Schritt.

   * Um eine vorhandene spezifische metrikbasierte Voreinstellung zu löschen, wählen Sie ![Löschen](/help/assets/icons/Delete.svg) aus.

1. Wählen Sie **[!UICONTROL Save]** aus, um die Voreinstellungen für die Datenzusammenführung zu speichern. Eine erneute Synchronisierung der Daten wird initiiert. <br/>Wählen Sie **[!UICONTROL Cancel]** aus, um abzubrechen.

## Quelldatensatz löschen

Wenn Sie einen Quelldatensatz löschen, der in Ihren harmonisierten Daten verwendet wird, werden die zugrunde liegenden Einträge in diesem Quelldatensatz aus dem [[!UICONTROL Harmonized data]](/help/harmonize-data/overview.md) entfernt. Die Datensatzregel mit dem gelöschten Quelldatensatz verbleibt jedoch in der Konfigurationsliste der Datensatzregel mit dem Symbol ![DataRemove](/help/assets/icons/DataRemove.svg) , das angibt, dass der Quelldatensatz gelöscht wurde. Weitere Informationen erhalten Sie:

* Wählen Sie ![Mehr](/help/assets/icons/More.svg) und ![Vorschau](/help/assets/icons/Preview.svg) **[!UICONTROL View]** aus dem Kontextmenü aus.
Das Dialogfeld &quot;**[!UICONTROL Dataset rule mapping - Fields]**&quot;zeigt Informationen zum gelöschten Quelldatensatz und zu den Feldern an, die in der Konfiguration der Datensatzregel verwendet werden.

Wenn Sie zur **[!UICONTROL Dataset rules]** -Konfiguration zurückkehren, wird ein Dialogfeld angezeigt, in dem erklärt wird, dass mindestens ein Quelldatensatz gelöscht wurde. Die harmonisierten Daten wirken sich auf die nächste Ad-hoc- oder geplante Synchronisation aus. Überprüfen Sie die Konfiguration Ihrer Datensatzregel.

Die harmonisierten Daten werden bei der nächsten Ad-hoc-Synchronisierung oder geplanten Synchronisation ohne die gelöschten Quelldaten aktualisiert. Sie werden jedoch weiterhin in Warndialogfeldern aufgefordert, die Datensatzregel basierend auf dem gelöschten Quelldatensatz zu löschen. Mit diesem Warnhinweis können Benutzer die betroffenen Felder im gelöschten Datensatz anzeigen und auswerten. Und um die Auswirkungen auf Marketing-Touchpoints oder Konversionen zu ermitteln, die in beliebigen Modellen verwendet werden können. Nachdem Sie diese Auswirkungen überprüft und abgemildert haben, sollten Sie die Datensatzregel aus der Konfigurationsliste der Datensatzregel löschen.
