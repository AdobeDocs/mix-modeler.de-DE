---
title: Datensatzregeln
description: Erfahren Sie, wie Sie Datensatzregeln definieren, die im Rahmen der Harmonisierung Ihrer Daten in Mix Modeler verwendet werden.
feature: Harmonized Data, Dataset Rules
exl-id: 57d7940a-2900-4814-a30d-bb02bff7615d
source-git-commit: 86732fe30637aa72ced232d9f331a3cc64baa39b
workflow-type: tm+mt
source-wordcount: '980'
ht-degree: 1%

---

# Datensatzregeln

Datensatzregeln unterstützen Sie bei der Zuordnung Ihrer harmonisierten Felder zu Feldern aus den in Mix Modeler erfassten Daten.

* Für aggregierte Daten, die Sie in Adobe Experience Platform erfasst haben, ordnen Sie eines oder mehrere der verfügbaren Datensatzfelder den entsprechenden harmonisierten Feldern zu.
* Für Ereignisdaten können Sie ein oder mehrere harmonisierte Felder einzeln Feldern aus dem Datensatz zuordnen, entweder direkt oder unter Verwendung von Bedingungen.


## Verwalten von Datensatzregeln

So zeigen Sie eine Tabelle der verfügbaren Datensatzregeln in der Mix Modeler-Oberfläche an:

1. Auswählen ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** über die linke Leiste.

1. Auswählen **[!UICONTROL Dataset rules]** aus der oberen Leiste. Sie sehen eine Tabelle der Datensatzregeln.

Die Tabellenspalten geben Details zu den Datensatzregeln an:

| Spaltenname | Details |
| ---------------------- | ----------|
| Datensatz | Der Name des Datensatzes. |
| Quelle | Die Quelle des Datensatzes, zu der Adobe Analytics, Erlebnisereignisse, Zusammenfassungen (Aggregate) oder Kundenerlebnisereignisse gehören können. |
| Schema | Das Schema, dem der Datensatz entspricht. Sie können den Schemanamen schnell auswählen, um das Schema in einer neuen Registerkarte im Schema-Editor in Mix Modeler - Schemas zu öffnen. |
| Granularität | Die Granularität der Daten im Datensatz. Mögliche Werte sind Täglich, Wöchentlich, Monatlich oder Jährlich. |
| Beginn der Woche | Gibt an, welcher Wochentag als Beginn einer neuen Woche für den spezifischen Datensatz betrachtet wird. |
| Status | Der Status des Felds: <p><span style="color:gray">●</span> Entwurf oder <p><span style="color:green">●</span> Aktiv |
| Zuletzt geändert | Daten und Uhrzeit der letzten Änderung der Datensatzregel. |

{style="table-layout:auto"}

### Erstellen einer Datensatzregel

So erstellen Sie eine Datensatzregel in der ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** Benutzeroberfläche in Mix Modeler auswählen **[!UICONTROL Create Dataset rule]** im **[!UICONTROL Dataset rules configuration]** Assistent.

Im **[!UICONTROL Create]** Bildschirm,

1. In **[!UICONTROL Dataset details]**, wählen Sie einen Datensatz aus **[!UICONTROL Select dataset]** , um die Konfiguration zu starten. In der Liste werden Datensätze in **[!UICONTROL Consumer Experience Events]**, **[!UICONTROL Adobe Analytics]**, **[!UICONTROL Experience Event]** und **[!UICONTROL Summary]**.

1. Tag für die **[!UICONTROL Start of the week]**.

1. Auswählen **[!UICONTROL Daily]**, **[!UICONTROL Weekly]**, **[!UICONTROL Monthly]** oder **[!UICONTROL Yearly]** für **[!UICONTROL Granularity]**.

1. Wenn Sie einen Datensatz von **[!UICONTROL Summary]** category:

   1. Ordnen Sie jeden der **[!UICONTROL Available dataset fields]** entspricht **[!UICONTROL Standard harmonized fields]** in **[!UICONTROL Map to harmonized fields]**. Wenn Sie ein Datensatzfeld nicht einem harmonisierten Feld zuordnen möchten, wählen Sie **[!UICONTROL -- None --]**.

   1. Wenn Sie ein neues harmonisiertes Feld benötigen, das nicht in der Liste verfügbar ist, wählen Sie **[!UICONTROL Create New]** Schaffung eines neuen harmonisierten Bereichs. Sie sehen das Dialogfeld, wie unter [Neues harmonisiertes Feld hinzufügen](fields.md#add-a-harmonized-field) um Ihnen die Möglichkeit zu geben, schnell ein neues harmonisiertes Feld hinzuzufügen.

   1. Wenn die Zuordnung für alle Felder der Regel abgeschlossen ist, wählen Sie **[!UICONTROL Save as draft]** , um eine Entwurfsversion der Regel zu speichern, oder **[!UICONTROL Save]** , um die Regel zu speichern und zu aktivieren.  Auswählen **[!UICONTROL Cancel]** , um die Regelkonfiguration abzubrechen.

      ![Erstellen von Datensatzregeln](../assets/dataset-create-summary.png)

1. Wenn Sie einen Datensatz der Ereigniskategorie ausgewählt haben (**[!UICONTROL Experience Events]**, **[!UICONTROL Adobe Analytics]**, **[!UICONTROL Consumer Experience Events]**), in das Feld unter **[!UICONTROL Map to harmonized fields]**:

   1. Wählen Sie ein harmonisiertes Feld aus **[!UICONTROL Standard harmonized field]**.

   1. Wenn das ausgewählte harmonisierte Feld vom Typ Metrik ist:

      1. Auswählen **[!UICONTROL Count]** oder **[!UICONTROL Sum]** von **[!UICONTROL Mapping type]**.

      1. Wählen Sie eine **[!UICONTROL *AEP-Datensatzfeld *]**dass das harmonisierte Feld standardmäßig zugeordnet werden soll.

   1. Wenn das ausgewählte Feld eine Dimension vom Typ hat:

      1. Auswählen **[!UICONTROL Map Into]** oder **[!UICONTROL Case]** von **[!UICONTROL Mapping type]**.

      1. Wenn Sie **[!UICONTROL Map Into]** auswählen **[!UICONTROL Field]** und **[!UICONTROL *AEP-Datensatzfeld *]**oder **[!UICONTROL Value]**und einen Standardwert, um das harmonisierte Feld standardmäßig dem Datensatzfeld oder dem eingegebenen Wert zuzuordnen.

      1. Wenn Sie **[!UICONTROL Case]** auswählen **[!UICONTROL Field]** und **[!UICONTROL *AEP-Datensatzfeld *]**oder **[!UICONTROL Value]**und einen Standardwert, um das harmonisierte Feld standardmäßig dem Datensatzfeld oder dem eingegebenen Wert zuzuordnen.

         1. Außerdem definieren Sie einen oder mehrere Fälle, die aus einer oder mehreren Bedingungen bestehen, um explizit Werte festzulegen. Jede Bedingung kann nach einer bestimmten **[!UICONTROL *AEP-Datensatzfeld *]**ob **[!UICONTROL Exists]**oder **[!UICONTROL Not Exists]**oder ob **[!UICONTROL Contains]**,**[!UICONTROL Not Contains]**,**[!UICONTROL Equals]**,**[!UICONTROL Not Equals]**,**[!UICONTROL Starts With]**oder **[!UICONTROL Ends With]**einen Wert, der unter**[!UICONTROL * Eingabewert eingeben *]**.

         1. Um eine weitere Groß-/Kleinschreibung hinzuzufügen, wählen Sie ![Hinzufügen](../assets/icons/AddCircle.svg) **[!UICONTROL Add case]**, um eine weitere Bedingung hinzuzufügen, wählen Sie ![Hinzufügen](../assets/icons/AddCircle.svg) **[!UICONTROL Add condition]**.

         1. Um eine Groß-/Kleinschreibung oder Bedingung zu löschen, wählen Sie ![Schließen](../assets/icons/Close.svg) im entsprechenden Container.

         1. Um festzulegen, ob eine oder alle Bedingungen für einen Fall gelten sollen, wählen Sie **[!UICONTROL Any of]** oder **[!UICONTROL All of]**.

         1. Um den Ergebniswert für einen Fall festzulegen, geben Sie den Wert unter **[!UICONTROL Then]**.

      Das Beispiel unten

      * verwendet eine **[!UICONTROL Map Into]** **[!UICONTROL Mapping type]** zum Zuordnen des **[!UICONTROL Channel Type At Source]** harmonisiertes Feld an die **[!UICONTROL channel_type]** aus dem **[!DNL Luma Transactions]** Datensatz.

      * verwendet eine **[!UICONTROL Case]** **[!UICONTROL Mapping type]** , um den Wert der **[!UICONTROL marketing.campaignName]** im Feld **[!DNL Luma Transactions]** Datensatz in der **[!UICONTROL Campaign]** harmonisiertes Feld. Das harmonisierte Feld Kampagne ist auf Folgendes festgelegt:

         * `Black Friday` wenn die **[!UICONTROL marketing.campaignName]** is `_black_friday` oder `BlackFriday`.
         * auf den Wert der **[!UICONTROL marketing.campaignName]** in allen anderen Fällen.

        ![Ereignis der Datensatzregel](../assets/dataset-create-event.png)

1. Auswählen ![Hinzufügen](../assets/icons/AddCircle.svg) **[!UICONTROL Add field]** um zusätzliche Felder zu definieren.

Wählen Sie zum Abschluss **[!UICONTROL Save as draft]** , um eine Entwurfsversion der Regel zu speichern, oder **[!UICONTROL Save]** , um die Regel zu speichern und zu aktivieren.  Auswählen **[!UICONTROL Cancel]** , um die Regelkonfiguration abzubrechen.


### Eine Datensatzregel bearbeiten

So bearbeiten Sie eine Datensatzregel in der ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** -Schnittstelle in Mix Modeler:

1. Auswählen ![Mehr](../assets/icons/More.svg) im **[!UICONTROL Dataset]** -Spalte für die Datensatzregel, die Sie bearbeiten möchten.
1. Wählen Sie im Kontextmenü die Option ![Bearbeiten](../assets/icons/Edit.svg) **[!UICONTROL Edit]** , um mit der Bearbeitung der Datensatzregel zu beginnen. Siehe Abschnitt [Erstellen einer Datensatzregel](#create-a-dataset-rule) für weitere Details.


### Eine Datensatzregel löschen

So löschen Sie eine Datensatzregel in der ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** -Schnittstelle in Mix Modeler:

1. Auswählen ![Mehr](../assets/icons/More.svg) im **[!UICONTROL Dataset]** -Spalte für die Datensatzregel, die Sie löschen möchten.
1. Wählen Sie im Kontextmenü die Option ![Löschen](../assets/icons/Delete.svg) **[!UICONTROL Delete]** , um die Datensatzregel zu löschen. Sie werden zur Bestätigung aufgefordert. Auswählen **[!UICONTROL Delete]** , um die ausgewählte Datensatzregel dauerhaft zu löschen.


## Daten synchronisieren

So synchronisieren Sie Daten zwischen Ihren harmonisierten Daten und Zusammenfassungs- und / oder Ereignis-Datensätzen, indem Sie die gesamte Logik in Ihren Datensatzregeln befolgen:

1. Wählen Sie **[!UICONTROL Sync data]** aus.

1. Aus dem **[!UICONTROL Sync data for dataset rules]** auswählen Sie entweder **[!UICONTROL Refresh harmonized data for summary datasets]**, **[!UICONTROL Refresh harmonized data for event datasets]** oder **[!UICONTROL Refresh harmonized data for both summary + event datasets]**.

1. Auswählen **[!UICONTROL Sync]** , um die Synchronisierung auf der Grundlage der definierten Datensatzregeln zwischen harmonisierten Daten und Daten in Datensätzen zu starten. Um die Synchronisierung abzubrechen, wählen Sie **[!UICONTROL Cancel]**.

   ![Daten synchronisieren](../assets/sync-data.png)


## Voreinstellungen zur Datenzusammenführung

Sie können Voreinstellungen definieren, um Konflikte zu lösen, da Daten aus zusammengefassten und Ereignisquellen zusammengeführt werden. Gehen Sie dazu folgendermaßen vor:

1. Auswählen ![Voreinstellungen zur Datenzusammenführung](../assets/icons/Merge.svg) **Voreinstellungen zur Datenzusammenführung**.

1. Im **[!UICONTROL Data merge preferences]** dialog:

   ![Voreinstellungen zur Datenzusammenführung](../assets/data-merge-preferences.png)

   1. Wählen Sie die Standardmetrikeinstellung aus der **[!UICONTROL Default metric preference]** Liste. <p>Eine Standardeinstellung wird angewendet, wenn während der Harmonisierung mehrere Datenquellen versuchen, ein Metrikfeld für einen bestimmten Kanal zu aktualisieren. Diese Voreinstellung wird auf Sandbox-Ebene angewendet, es sei denn, sie wird für bestimmte Metrikvoreinstellungen überschrieben, die unter **[!UICONTROL Metric based preference]**.

   1. Verwendung ![Plus](../assets/icons/AddCircle.svg) **[!UICONTROL Add a metric]**, um eine oder mehrere Metriken darunter hinzuzufügen **[!UICONTROL Metric based preference]**.



      * Wählen Sie eine Metrik aus der **[!UICONTROL _Metrikauswahl_]** und
      * Wählen Sie **[!UICONTROL Summary]** oder **[!UICONTROL Event]** aus.

      Verwendung ![Löschen](../assets/icons/Close.svg) , um einen Eintrag aus der Liste zu löschen.

   1. Auswählen **[!UICONTROL Save]** , um die Voreinstellungen für die Datenzusammenführung zu speichern. Auswählen **[!UICONTROL Cancel]** abbrechen.
