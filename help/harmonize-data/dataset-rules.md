---
title: Datensatzregeln
description: Erfahren Sie, wie Sie Datensatzregeln definieren, die im Rahmen der Harmonisierung Ihrer Daten in Mix Modeler verwendet werden sollen.
feature: Harmonized Data, Dataset Rules
exl-id: 57d7940a-2900-4814-a30d-bb02bff7615d
source-git-commit: d22bb8c9526821c28c9a59967e1be399957d3051
workflow-type: tm+mt
source-wordcount: '1628'
ht-degree: 1%

---

# Datensatzregeln

Datensatzregeln unterstützen Sie bei der Zuordnung Ihrer harmonisierten Felder zu Feldern aus den Daten, die Sie in Mix Modeler aufgenommen haben.

* Für aggregierte Daten, die Sie in Adobe Experience Platform aufgenommen haben, ordnen Sie eines oder mehrere der verfügbaren Datensatzfelder den entsprechenden harmonisierten Feldern zu.
* Für Ereignisdaten können Sie direkt oder unter Verwendung von Bedingungen ein oder mehrere harmonisierte Felder einzeln Feldern aus dem Datensatz zuordnen.


## Verwalten von Datensatzregeln

Eine Tabelle der verfügbaren Datensatzregeln finden Sie in der Benutzeroberfläche von Mix Modeler:

1. Wählen Sie ![DataSearch](/help/assets/icons/DataCheck.svg)-**[!UICONTROL Harmonized data]** in der linken Leiste aus.

1. Wählen Sie **[!UICONTROL Dataset rules]** in der oberen Leiste aus. Es wird eine Tabelle mit den Datensatzregeln angezeigt.

Die Tabellenspalten geben Details zu den Datensatzregeln an:

| Spaltenname | Details |
| ---------------------- | ----------|
| Datensatz | Der Name des Datensatzes. |
| Quelle | Die Quelle des Datensatzes: Adobe Analytics, Erlebnisereignisse, Zusammenfassung (Aggregat) oder Kundenerlebnisereignisse. |
| Schema | Das Schema, dem der Datensatz entspricht. Sie können den Schemanamen schnell auswählen, um das Schema in einer neuen Registerkarte im Schema-Editor unter ![Schema](/help/assets/icons/Schemas.svg) [Schemas](../ingest-data/schemas.md) zu öffnen. |
| Granularität | Die Granularität von Daten im Datensatz. Mögliche Werte sind Täglich, Wöchentlich, Monatlich oder Jährlich. |
| Wochenbeginn | Gibt an, welcher Wochentag als Beginn einer neuen Woche für den spezifischen Datensatz betrachtet wird. |
| Status | Der Status des Felds: <p>Entwurf <span style="color:gray">●</span> oder <p><span style="color:green">●</span> aktiv |
| Zuletzt geändert | Datum und Uhrzeit der letzten Änderung der Datensatzregel. |

{style="table-layout:auto"}

### Erstellen einer Datensatzregel

Um eine Datensatzregel zu erstellen, wählen Sie in der ![DataSearch](/help/assets/icons/DataCheck.svg)-**[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** in Mix Modeler im **[!UICONTROL Create a dataset rule]**-Assistenten **[!UICONTROL Dataset rules configuration]** aus.

Auf dem Bildschirm **[!UICONTROL Create]**

1. Wählen Sie **[!UICONTROL Dataset details]** einen Datensatz aus **[!UICONTROL Select dataset]** aus, um mit der Konfiguration zu beginnen. In der Liste werden Datensätze in **[!UICONTROL Consumer Experience Events]**, **[!UICONTROL Adobe Analytics]**, **[!UICONTROL Experience Event]** und **[!UICONTROL Summary]** kategorisiert.

1. Wählen Sie einen Tag für die **[!UICONTROL Start of the week]** aus.

1. Wählen Sie **[!UICONTROL Daily]**, **[!UICONTROL Weekly]**, **[!UICONTROL Monthly]** oder **[!UICONTROL Yearly]** für **[!UICONTROL Granularity]** aus.

1. Wenn Sie einen Datensatz der Kategorie **[!UICONTROL Summary]** ausgewählt haben, wählen Sie **[!UICONTROL Aggregation]** oder **[!UICONTROL Replacement]** für die **[!UICONTROL Data restatement is by]** aus.

   Die Berichterstattung über Daten von Publishern ist für Marketing-Analysten sehr wichtig, da die Arbeit mit Publishern oft erhebliche Ausgaben mit sich bringt und Änderungen an den Berichtsdaten zu sehr unterschiedlichen Einblicken und Investitionsplänen führen können. Darüber hinaus benötigen Marketing-Analysten genaue Daten, um die richtigen Erkenntnisse zu gewinnen und überzeugende Vorschläge zu unterbreiten, um das Vertrauen der Stakeholder zu gewinnen. Diese Herausgeber wie Google und Facebook passen jedoch ihre Berichtsdaten häufig an bzw. löschen sie, während sie ihre Daten miteinander abstimmen. Der Zeitrahmen für die meisten Änderungen liegt innerhalb von 7 Tagen nach der gemeldeten Medienleistung. Weitere Änderungen der Daten sind innerhalb von 30 Tagen möglich. Im Allgemeinen gelten Bücher nach 30 Tagen als geschlossen und die Daten vollständig.

   Mix Modeler unterstützt die Datenanpassung. Um sicherzustellen, dass die Daten, die für das Reporting, die Modellierung und die Planung verwendet werden, korrekt sind. Und dass die Daten in der Lage sind, die Erwartungen und Bedürfnisse der Marken- und Marketing-Analysten zu unterstützen.

   Sie können neu angepasste Zeilen von Zusammenfassungsdaten als inkrementelle Zeilen in einem Experience Platform-Datensatz senden, und der Harmonisierungs-Service aktualisiert den harmonisierten Datensatz mit diesen neu angepassten Daten. Auf ähnliche Weise können Sie auch Zeilen mit Zusammenfassungsdaten entfernen, die im Harmonisierungsdienst widergespiegelt werden müssen.

1. Im **[!UICONTROL Map to harmonized fields]** Abschnitt:

   1. Wählen Sie ein harmonisiertes Feld aus **[!UICONTROL Standard harmonized field]** aus.

   1. Wenn das ausgewählte harmonisierte Feld vom Typ „Metrik“ ist:

      1. Wählen Sie **[!UICONTROL Count]** oder **[!UICONTROL Sum]** aus **[!UICONTROL Mapping type]** aus.

      1. Wählen Sie ein **[!UICONTROL *AEP *]**Datensatzfeld aus, dem das harmonisierte Feld standardmäßig zugeordnet werden soll.

   1. Wenn das ausgewählte Feld vom Typ Dimension ist:

      1. Wählen Sie **[!UICONTROL Map Into]** oder **[!UICONTROL Case]** aus **[!UICONTROL Mapping type]** aus.

      1. Wenn Sie **[!UICONTROL Map Into]** ausgewählt haben, wählen Sie **[!UICONTROL Field]** und **[!UICONTROL *AEP-Datensatzfeld *]**oder **[!UICONTROL Value]**und einen Standardwert aus, um das harmonisierte Feld standardmäßig dem Datensatzfeld oder dem eingegebenen Wert zuzuordnen.

      1. Wenn Sie **[!UICONTROL Case]** auswählen, wählen Sie **[!UICONTROL Field]** und **[!UICONTROL *AEP-Datensatzfeld *]**oder **[!UICONTROL Value]**und einen Standardwert aus, um das harmonisierte Feld standardmäßig dem Datensatzfeld oder dem eingegebenen Wert zuzuordnen.

         1. Um Werte explizit festzulegen, definieren Sie einen oder mehrere Fälle, die aus einer oder mehreren Bedingungen bestehen. Jede Bedingung kann auf ein bestimmtes **[!UICONTROL *AEP-Datensatzfeld prüfen *]**ob es **[!UICONTROL Exists]**oder **[!UICONTROL Not Exists]**oder ob es **[!UICONTROL Contains]**,**[!UICONTROL Not Contains]**,**[!UICONTROL Equals]**,**[!UICONTROL Not Equals]**,**[!UICONTROL Starts With]**oder **[!UICONTROL Ends With]**einen unter**[!UICONTROL * Eingabewert eingeben *]**.

         1. Um einen weiteren Fall hinzuzufügen, wählen Sie ![Hinzufügen](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add case]**. Um eine weitere Bedingung hinzuzufügen, wählen Sie ![Hinzufügen](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add condition]**.

         1. Um einen Fall oder eine Bedingung zu löschen, wählen ![ im ](/help/assets/icons/Close.svg) Container die Option „Schließen“ aus.

         1. Um festzulegen, ob eine oder alle Bedingungen für einen Fall gelten sollen, wählen Sie **[!UICONTROL Any of]** oder **[!UICONTROL All of]** aus.

         1. Um den Ergebniswert für einen Fall festzulegen, geben Sie den Wert unter **[!UICONTROL Then]** ein.

      Beispiel unten

      * verwendet eine **[!UICONTROL Map Into]** **[!UICONTROL Mapping type]**, um das **[!UICONTROL Channel Type At Source]** harmonisierte Feld dem **[!UICONTROL channel_type]** Feld aus dem **[!DNL Luma Transactions]** zuzuordnen.

      * verwendet eine **[!UICONTROL Case]** **[!UICONTROL Mapping type]**, um den Wert des **[!UICONTROL marketing.campaignName]** Felds im **[!DNL Luma Transactions]** Datensatz dem **[!UICONTROL Campaign]** harmonisierten Feld zuzuordnen. Das Feld Harmonisierte Kampagne ist auf Folgendes festgelegt:

         * `Black Friday`, wann die **[!UICONTROL marketing.campaignName]** `_black_friday` oder `BlackFriday` ist.
         * auf den Wert des **[!UICONTROL marketing.campaignName]** in allen anderen Fällen.

        ![Datensatz-Regelereignis](/help/assets/dataset-create-event.png)

      Wenn Sie ein standardmäßiges harmonisiertes Feld aus einem Zusammenfassungsdatensatz zuordnen, versucht Mix Modeler, das entsprechende Experience Platform-Datensatzfeld abzuleiten. Bei Erfolg:

      * Wenn das Feld vom Typ „Dimension“ ist, wird **[!UICONTROL Map into]** als **[!UICONTROL Mapping type]** ausgewählt.
      * Wenn das Feld vom Typ „Metrik“ ist, wird **[!UICONTROL Sum]** als **[!UICONTROL Mapping type]** ausgewählt.
      * **[!UICONTROL Field]** ist als **[!UICONTROL Default]** Zuordnungstyp ausgewählt.
      * Das entsprechende Experience Platform-Datensatzfeld wird automatisch für das *AEP-Datensatzfeld eingefügt*.

      Sie können jeden der vorgeschlagenen Werte ändern, wenn diese falsch sind oder Ihren spezifischen Anwendungsfall nicht unterstützen.

1. Wählen Sie ![Hinzufügen](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add field]** aus, um zusätzliche Felder zu definieren.

Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save as draft]** , um eine Entwurfsversion der Regel zu speichern, oder auf **[!UICONTROL Save]** , um die Regel zu speichern und zu aktivieren. Wählen Sie **[!UICONTROL Cancel]** aus, um die Regelkonfiguration abzubrechen.

>[!NOTE]
>
>Das dedizierte **[!UICONTROL Map to harmonized fields]**-Erlebnis für Regeln für Zusammenfassungsdatensätze wird nicht mehr unterstützt. Alle Datensatzregeln verwenden jetzt unabhängig vom Datensatztyp ein ähnliches **[!UICONTROL Map to harmonized fields]**. Für zusammenfassende Datensätze, für die Sie Regeln mit dem veralteten **[!UICONTROL Map to harmonized fields]**-Erlebnis definiert haben, sollten Sie diese Regeln mit dem generischen **[!UICONTROL Map to harmonized field]**-Erlebnis vergleichen.
>



### Bearbeiten einer Datensatzregel

Um eine Datensatzregel zu bearbeiten, gehen Sie in der Benutzeroberfläche ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** in Mix Modeler folgendermaßen vor:

1. Wählen Sie ![Mehr](/help/assets/icons/More.svg) in der Spalte **[!UICONTROL Dataset]** für die Datensatzregel aus, die Sie bearbeiten möchten.
1. Wählen Sie im Kontextmenü die Option ![Bearbeiten](/help/assets/icons/Edit.svg) aus **[!UICONTROL Edit]** um mit der Bearbeitung der Datensatzregel zu beginnen. Weitere Informationen finden [ unter „Erstellen ](#create-a-dataset-rule) Datensatzregel“.


### Löschen einer Datensatzregel

Um eine Datensatzregel zu löschen, gehen Sie in der Benutzeroberfläche ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** in Mix Modeler folgendermaßen vor:

1. Wählen Sie ![Mehr](/help/assets/icons/More.svg) in der Spalte **[!UICONTROL Dataset]** für die Datensatzregel aus, die Sie löschen möchten.
1. Wählen Sie im Kontextmenü die Option ![Löschen](/help/assets/icons/Delete.svg) aus, **[!UICONTROL Delete]** die Datensatzregel zu löschen. Sie werden zur Bestätigung aufgefordert. Wählen Sie **[!UICONTROL Delete]** aus, um die ausgewählte Datensatzregel dauerhaft zu löschen.



## Daten synchronisieren

So synchronisieren Sie Daten zwischen Ihren harmonisierten Daten und Zusammenfassungs- und/oder Ereignis-Datensätzen, während Sie die Logik in Ihren Datensatzregeln anwenden:

1. Wählen Sie **[!UICONTROL Sync data]** aus.

1. Wählen Sie im **[!UICONTROL Sync data for dataset rules]**-Dialogfeld entweder
   * **[!UICONTROL Refresh harmonized data for summary datasets]**,
   * **[!UICONTROL Refresh harmonized data for event datasets]** oder
   * **[!UICONTROL Refresh harmonized data for both summary + event datasets]**.

1. Um die Synchronisierung auf der Grundlage der definierten Datensatzregeln zwischen harmonisierten Daten und Daten in Datensätzen zu starten, wählen Sie **[!UICONTROL Sync]** aus. Um die Synchronisierung abzubrechen, wählen Sie **[!UICONTROL Cancel]** aus.

   ![Daten synchronisieren](/help/assets/sync-data.png)


## Voreinstellungen für die Datenzusammenführung

>[!NOTE]
>
>[!BADGE Beta]{type=Informative} Die Voreinstellungen für die Datenzusammenführung sind eine Beta-Funktion und ihre Funktionalität kann sich ändern.

Um genaue Modellvorhersagen zu gewährleisten, können Sie Voreinstellungen für die Datenzusammenführung definieren. Diese Funktion ermöglicht es Benutzenden, Konflikte nach dem Zusammenführen von Daten auf Zusammenfassungsebene und Ereignisebene zu beheben.

Sie können eine Standardeinstellung für Metriken konfigurieren, die bei widersprüchlichen Aktualisierungen angewendet wird. Diese Standardmetrik kann eine von drei Optionen sein:

* **[!UICONTROL Summary data]**
* **[!UICONTROL Sum of summary and event data]**
* **[!UICONTROL Event data]**

Wenn während der Harmonisierung mehrere Datenquellen versuchen, ein Metrikfeld für einen bestimmten Kanal zu aktualisieren, wird die vom Benutzer konfigurierte Standardvoreinstellung angewendet. Diese Voreinstellung wird auf Sandbox-Ebene angewendet, es sei denn, sie wird für bestimmte metrikbasierte Voreinstellungen überschrieben, die zusätzlich konfiguriert wurden.

Unter **[!UICONTROL Metric based preferences]** kann der Benutzer die spezifische Quelle (**[!UICONTROL Summary]** oder **[!UICONTROL Event]**) für eine bestimmte Metrik und den entsprechenden Konversionstyp für diese Metrik konfigurieren.

Typische Anwendungsfälle sind:

* dieselbe Werbemetrik in mehreren Datensätzen gemessen und gemeldet wird oder
* Messmetriken können in einigen Datensätzen unvollständig sein, während ein anderer Datensatz eine Obermenge einer bestimmten Metrik sein kann, was zu einer doppelten Zählung führt.

### Konfigurieren

So konfigurieren Sie die Voreinstellungen für die Datenzusammenführung:


1. Wählen Sie ![Voreinstellungen für die Datenzusammenführung](/help/assets/icons/Merge.svg) [!BADGE Beta] aus.

1. Im **[!UICONTROL Data merge preferences]**-Dialogfeld [!BADGE Betaversion]{type=Informative}:

   ![Voreinstellungen für die Datenzusammenführung](/help/assets/data-merge-preferences.png)

   * **[!UICONTROL Default metric preference]** auswählen. Die ausgewählte Standard-Metrikvoreinstellung wird angewendet, wenn während der Harmonisierung mehrere Datenquellen ein Metrikfeld für einen bestimmten Kanal aktualisieren. Die Voreinstellung wird auf Sandbox-Ebene angewendet, es sei denn, sie wird für bestimmte metrikbasierte Voreinstellungen überschrieben. Sie können zwischen **[!UICONTROL Summary data]**, **[!UICONTROL Event data]** und **[!UICONTROL Sum of summary and event data]** wählen.

   * So fügen Sie metrikbasierte Voreinstellungen hinzu:

      1. Wählen Sie ![Plus](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add a metric]** aus.
         1. Wählen Sie eine Metrik aus der Liste **[!UICONTROL *Metrikauswahl *]**aus.
         1. Wählen Sie **[!UICONTROL CHANNELS]** oder **[!UICONTROL CONVERSION TYPES]** aus. Wählen Sie aus der Liste **[!UICONTROL All]** oder einen bestimmten Kanal- oder Konvertierungstyp aus.
         1. Wählen Sie **[!UICONTROL Summary]** oder **[!UICONTROL Event]** aus, um anzugeben, ob beim Zusammenführen von Daten Zusammenfassungsdaten oder Ereignisdaten für die Metrik (und alle oder ausgewählte Kanäle) bevorzugt werden.

         So fügen Sie einen oder mehrere zusätzliche Kanal- oder Konvertierungstypen hinzu:

         1. Wählen Sie ![Plus](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add a channel]** oder ![Plus](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add a conversion type]**.
         1. Wählen Sie **[!UICONTROL Summary]** oder **[!UICONTROL Event]** aus.

         Um einen Kanal oder Konversionstyp zu löschen, wählen Sie ![Cross](/help/assets/icons/Close.svg) aus.

      1. Um spezifischere metrikbasierte Voreinstellungen hinzuzufügen, wiederholen Sie den vorherigen Schritt.

   * Um eine vorhandene spezifische metrikbasierte Voreinstellung zu löschen, wählen Sie ![Löschen](/help/assets/icons/Delete.svg).

1. Wählen Sie **[!UICONTROL Save]** aus, um die Voreinstellungen für die Datenzusammenführung zu speichern. Eine erneute Synchronisierung der Daten wird eingeleitet. <br/>Wählen Sie zum Abbrechen **[!UICONTROL Cancel]** aus.

## Löschen eines Quelldatensatzes

Wenn Sie einen Quelldatensatz löschen, der in Ihren harmonisierten Daten verwendet wird, werden die zugrunde liegenden Einträge in diesem Quelldatensatz aus dem [[!UICONTROL Harmonized data]](/help/harmonize-data/overview.md) entfernt. Die Datensatzregel mit dem gelöschten Quelldatensatz verbleibt jedoch in der Konfigurationsliste der Datensatzregel mit einem Symbol ![DataRemove](/help/assets/icons/DataRemove.svg), das angibt, dass der Quelldatensatz gelöscht wurde. Weitere Informationen finden Sie unter:

* Wählen Sie ![Mehr](/help/assets/icons/More.svg) und ![Vorschau](/help/assets/icons/Preview.svg) **[!UICONTROL View]** aus dem Kontextmenü aus.
Das Dialogfeld **[!UICONTROL Dataset rule mapping - Fields]** zeigt Informationen über den gelöschten Quelldatensatz und die in der Datensatzregelkonfiguration verwendeten Felder an.

Wenn Sie zu Ihrer **[!UICONTROL Dataset rules]**-Konfiguration zurückkehren, wird ein Dialogfeld angezeigt, in dem erklärt wird, dass mindestens ein Quelldatensatz gelöscht wurde. Die harmonisierten Daten sind bei einer nächsten Ad-hoc- oder geplanten Synchronisierung betroffen. Überprüfen Sie die Konfiguration Ihrer Datensatzregel.

Die harmonisierten Daten werden bei der nächsten Ad-hoc-Synchronisation oder geplanten Synchronisation ohne die gelöschten Quelldaten aktualisiert. Sie sehen jedoch weiterhin Warndialogfelder, in denen Sie aufgefordert werden, die Datensatzregel basierend auf dem gelöschten Quelldatensatz zu löschen. Dieser Warnhinweis ermöglicht es Benutzenden, die betroffenen Felder im gelöschten Datensatz anzuzeigen und auszuwerten. Und um die Auswirkungen auf Marketing-Touchpoints oder Konversionen zu ermitteln, die in beliebigen Modellen verwendet werden können. Nachdem Sie diese Auswirkungen überprüft und abgemildert haben, sollten Sie die Datensatzregel aus der Konfigurationsliste für die Datensatzregel löschen.
