---
title: Harmonisierte Felder
description: Erfahren Sie, wie Sie Felder definieren, die zur Harmonisierung Ihrer Daten in Mix Modeler verwendet werden sollen.
feature: Harmonized Data, Harmonized Fields
exl-id: f051279a-1ae9-49bd-a946-abfc34c90413
source-git-commit: 9085363e951a4e306c64ad28f56e2c15b4a6029a
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 10%

---

# Harmonisierte Felder

Harmonisierte Felder ermöglichen es Ihnen, Felder für konzeptionell dieselben Daten zu definieren, die aus verschiedenen Quellen stammen und jeweils eine eigene Definition dieser Daten enthalten. Beispielsweise kann eine Klickmetrik je nach Datenquelle anders definiert und benannt werden. Ein harmonisiertes Feld für Klicks ermöglicht es Ihnen, basierend auf diesen verschiedenen Klickdatenquellen eine gemeinsame Nomenklatur für eine Klickmetrik zu definieren.

Mithilfe von harmonisierten Feldern können Sie die Felder definieren, die Sie im Rahmen des Daten-Workflows harmonisieren möchten. Die von Ihnen definierten Felder können zum Definieren von Datensatzregeln, Marketing-Touchpoints und Konversionen verwendet werden.

## Globale Harmonisierungsbereiche

Die standardmäßig verfügbaren globalen Harmonisierungsfelder in Mix Modeler sind:


| Feldname | Anzeigename | Kategorie | Datentyp | Kommentar |
| ---------------------- | ---------------------- | --------- | --------- | --------- |
| Marke | Marke | Dimension | Zeichenfolge |           |
| Kampagne | Kampagne | Dimension | Zeichenfolge |           |
| channel | Kanal | Dimension | Zeichenfolge |           |
| channel_id | Kanal-ID | Dimension | Zeichenfolge |           |
| channel_type_at_source | Kanaltyp bei Source | Dimension | Zeichenfolge |           |
| channel | Kanal | Dimension | Zeichenfolge |           |
| Klicks | Klicks | Metrik | Zahl |           |
| conversiontype | Konversionstyp | Dimension | Zeichenfolge |           |
| Kosten | Kosten | Metrik | Währung |           |
| Datensatz | Datensatz | Dimension | Zeichenfolge |           |
| date_type | Datum Typ | Dimension | Zeichenfolge | Tag, Woche |
| email | Gesendete E-Mails | Metrik | Zahl |           |
| event_date | Datum | Dimension | Datum/Uhrzeit |           |
| brutto_demand | Bruttonachfrage | Metrik | Währung |           |
| Impressionen | Implikationen | Metrik | Zahl |           |
| last_updated_date | Letztes Aktualisierungsdatum | Dimension | Datum/Uhrzeit |           |
| linkvisitors | Besuche verknüpfen | Metrik | Zahl |           |
| mediatype | Medientyp | Dimension | Zeichenfolge |           |
| net_sales | Nettoverkäufe | Metrik | Währung |           |
| Bestellungen | Bestellungen | Metrik | Zahl |           |
| sourcetype | Source-Typ | Dimension | Zeichenfolge |           |
| ausgaben | Ausgeben | Metrik | Währung |           |
| trafficSource | Traffic-Quelle | Dimension | Zeichenfolge |           |

{style="table-layout:auto"}

Sie können zusätzlich zu diesen global harmonisierten Feldern Ihre eigenen harmonisierten Felder hinzufügen, bearbeiten oder löschen.

## Harmonisierte Felder verwalten

Eine Tabelle der verfügbaren harmonisierten Felder finden Sie in der Mix Modeler-Benutzeroberfläche:

1. Wählen Sie ![DataSearch](/help/assets//icons/DataCheck.svg) **[!UICONTROL Harmonized data]** in der linken Leiste aus.

1. Wählen Sie in der oberen Leiste **[!UICONTROL Fields]** aus. Sie sehen eine Tabelle der harmonisierten Felder. Wenn weitere Seiten verfügbar sind, verwenden Sie ![Pfeil nach links](/help/assets//icons/ChevronLeft.svg) oder ![Pfeil nach rechts](/help/assets//icons/ChevronRight.svg) bei **[!UICONTROL Page _x _von_x_]** , um zwischen den Seiten der Tabelle zu wechseln.

   Die Tabellenspalten geben Details zu den harmonisierten Feldern an

   | Spaltenname | Details |
   | ---------------------- | ----------|
   | Feldname | Der Name des harmonisierten Felds. |
   | Anzeigename | Der Anzeigename des harmonisierten Felds. Dieser Anzeigename wird beim Definieren von Datensatzregeln, Marketing-Touchpoints und Konversionsdefinitionen verwendet. |
   | Kategorie | Gibt an, ob ein harmonisiertes Datenfeld ein [!UICONTROL Dimension], ein [!UICONTROL Metric] oder ein [!UICONTROL Derived] ist. Eine abgeleitete Kategorie ist ein harmonisiertes Feld, das eine metrikbasierte Formeldefinition verwendet. |
   | Datentyp | Gibt den Datentyp an ([!UICONTROL Number], [!UICONTROL String], [!UICONTROL Currency], [!UICONTROL Date time]). |
   | Erstellungsdatum | Datum und Uhrzeit der Erstellung des harmonisierten Felds. |
   | Inhaber | Gibt an, ob ein harmonisiertes Feld ein Standardfeld ([!UICONTROL Global]) oder von Ihnen definiert ([!UICONTROL Client]) ist. |
   | Datum der letzten Änderung | Daten und Zeitpunkt der letzten Änderung des harmonisierten Felds. |
   | Formel | Gibt die Formel für ein harmonisiertes Feld basierend auf einer abgeleiteten Kategorie an. |

   {style="table-layout:auto"}

1. Um nach einem bestimmten harmonisierten Feld zu suchen, verwenden Sie ![Suche](/help/assets//icons/Search.svg) **[!UICONTROL *Harmonisiertes Suchfeld *]**.


### Harmonisiertes Feld hinzufügen

Um ein harmonisiertes Feld hinzuzufügen, gehen Sie in die Benutzeroberfläche ![DataSearch](/help/assets//icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** des Mix Modelers:

1. Wählen Sie ![Hinzufügen](/help/assets//icons/AddCircle.svg) **[!UICONTROL Add field]** aus.

1. Im Dialogfeld **[!UICONTROL Create]** :

   1. Geben Sie einen **[!UICONTROL Field name]** ein, z. B. `region`.
   1. Geben Sie einen **[!UICONTROL Display name]** ein, z. B. `Region`.
   1. Wählen Sie eine **[!UICONTROL Category]**: **[!UICONTROL Dimension]**, **[!UICONTROL Metric]** oder **[!UICONTROL Derived]**.

      Wenn Sie &quot;**[!UICONTROL Derived]**&quot;auswählen, geben Sie einen &quot;**[!UICONTROL Formula]**&quot;an. Um einen gültigen arithmetischen Ausdruck zu erstellen, kombinieren Sie eine oder mehrere Metriken aus **[!UICONTROL Insert Metric]** mit einem oder mehreren Operatoren **[!UICONTROL + - * / ( )]** . Beispiel: `[orders]/[impressions]`

   1. Wählen Sie einen **[!UICONTROL Data type]** aus.

      - **[!UICONTROL String]** oder **[!UICONTROL Date time]**, wenn die ausgewählte Kategorie Dimension ist.
      - **[!UICONTROL Number]** oder **[!UICONTROL Currency]** , wenn die ausgewählte Kategorie Metrik oder Abgeleitet ist.

   1. Wählen Sie **[!UICONTROL Submit]** aus, um das harmonisierte Feld hinzuzufügen. Wählen Sie **[!UICONTROL Close]** aus, um das Dialogfeld zu schließen, ohne das harmonisierte Feld hinzuzufügen.

      ![Erstellen eines Felds](/help/assets//create-field.png)


### Harmonisiertes Feld bearbeiten

Sie können nur harmonisierte Felder bearbeiten, die Sie zuvor erstellt haben (Eigentümer ist Client). Ein global harmonisiertes Feld kann nicht bearbeitet werden.

So bearbeiten Sie ein harmonisiertes Feld in der Benutzeroberfläche ![DataSearch](/help/assets//icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** im Mix Modeler:

1. Wählen Sie das harmonisierte Feld aus, das Sie bearbeiten möchten. Beispiel: **[!UICONTROL Region]**.

1. Ändern Sie im Bereich **[!UICONTROL Edit harmonization values]** die Werte für **[!UICONTROL Display name]**, **[!UICONTROL Category]** und **[!UICONTROL Data type]**. Weitere Informationen finden Sie unter [Hinzufügen eines harmonisierten Felds](#add-a-harmonized-field) .

1. Wählen Sie **[!UICONTROL Submit]** aus, um die Änderungen auf das harmonisierte Feld anzuwenden.

   ![Bearbeiten eines Felds](/help/assets//edit-field.png)

### Harmonisiertes Feld löschen

Sie können nur harmonisierte Felder löschen, die Sie zuvor erstellt haben (Eigentümer ist Kunde). Ein globales harmonisiertes Feld kann nicht gelöscht werden.

So löschen Sie ein harmonisiertes Feld in der Benutzeroberfläche ![DataSearch](/help/assets//icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** im Mix Modeler:

1. Wählen Sie das harmonisierte Feld aus, das Sie löschen möchten, z. B. **[!UICONTROL Region]**.

1. Wählen Sie ![Löschen](/help/assets//icons/Delete.svg) **[!UICONTROL Delete]** aus dem linken Bereich **[!UICONTROL Edit harmonization values]**.

   >[!WARNING]
   >
   >   Das Feld wird sofort gelöscht.

