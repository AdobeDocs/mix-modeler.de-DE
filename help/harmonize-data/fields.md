---
title: Harmonisierte Felder
description: Erfahren Sie, wie Sie Felder definieren, die im Rahmen der Harmonisierung Ihrer Daten im Mix Modeler verwendet werden sollen.
feature: Harmonized Data, Harmonized Fields
exl-id: f051279a-1ae9-49bd-a946-abfc34c90413
source-git-commit: 9a6c1f1c12ab29da80a1997cfd31ca07b38eaa22
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 10%

---

# Harmonisierte Felder

Harmonisierte Felder ermöglichen es Ihnen, Felder für konzeptionell dieselben Daten aus verschiedenen Quellen mit jeweils einer eigenen Definition dieser Daten zu definieren. Beispielsweise kann eine Klicks -Metrik je nach Datenquelle unterschiedlich definiert und benannt werden. Mit einem harmonisierten Feld Klicks können Sie eine gemeinsame Nomenklatur für eine Klicks-Metrik definieren, die auf diesen verschiedenen Quellen für Klickdaten basiert.

Mit harmonisierten Feldern können Sie die Felder definieren, die Sie im Rahmen des Workflows „Daten harmonisieren“ verwenden möchten. Die von Ihnen definierten Felder können zum Definieren von Datensatzregeln, Marketing-Touchpoints und Konversionen verwendet werden.

## Globale Harmonisierung

Die standardmäßig verfügbaren globalen Harmonisierungsfelder in der Mix Modeler sind:


| Feldname | Anzeigename | Kategorie | Datentyp | Kommentar |
| ---------------------- | ---------------------- | --------- | --------- | --------- |
| Marke | Marke | Dimension | String |           |
| Wahlkampf | Campaign | Dimension | String |           |
| Kanal | Kanal | Dimension | String |           |
| channel_id | Kanal-ID | Dimension | String |           |
| channel_type_at_source | Kanaltyp bei Source | Dimension | String |           |
| Kanal | Kanal | Dimension | String |           |
| Klicks | Klicks | Metrik | Zahl |           |
| conversionType | Konvertierungstyp | Dimension | String |           |
| Kosten | Kosten | Metrik | Währung |           |
| Datensatz | Datensatz | Dimension | String |           |
| date_type | Datumstyp | Dimension | String | Tag, Woche |
| E-Mails gesendet | E-Mails gesendet | Metrik | Zahl |           |
| event_date | Datum | Dimension | Datum/Uhrzeit |           |
| GROSS_DEMAND | Bruttomarge | Metrik | Währung |           |
| Impressionen | Impressionen | Metrik | Zahl |           |
| last_updated_date | Datum der letzten Aktualisierung | Dimension | Datum/Uhrzeit |           |
| linkVisits | Besuche verknüpfen | Metrik | Zahl |           |
| mediatype | Medientyp | Dimension | String |           |
| net_sales | Nettoumsatz | Metrik | Währung |           |
| Bestellungen | Bestellungen | Metrik | Zahl |           |
| sourceType | Source-Typ | Dimension | String |           |
| aufbrauchen | Ausgaben | Metrik | Währung |           |
| Verkehrsquelle | Traffic-Quelle | Dimension | String |           |

{style="table-layout:auto"}

Zusätzlich zu diesen global harmonisierten Feldern können Sie Ihre eigenen harmonisierten Felder hinzufügen, bearbeiten oder löschen.

## Verwalten harmonisierter Felder

So zeigen Sie eine Tabelle der verfügbaren harmonisierten Felder in der Benutzeroberfläche des Mix Modelers an:

1. Wählen Sie ![DataSearch](/help/assets/icons/DataCheck.svg)-**[!UICONTROL Harmonized data]** in der linken Leiste aus.

1. Wählen Sie **[!UICONTROL Fields]** in der oberen Leiste aus. Eine Tabelle der harmonisierten Felder wird angezeigt. Wenn mehr Seiten verfügbar sind, verwenden Sie ![Pfeil links](/help/assets/icons/ChevronLeft.svg) oder ![Pfeil rechts](/help/assets/icons/ChevronRight.svg) um **[!UICONTROL Page _x _von_x_]**, um zwischen Seiten der Tabelle zu wechseln.

   Die Tabellenspalten geben Details zu den harmonisierten Feldern an

   | Spaltenname | Details |
   | ---------------------- | ----------|
   | Feldname | Der Name des harmonisierten Felds. |
   | Anzeigename | Der Anzeigename des harmonisierten Felds. Dieser Anzeigename wird beim Definieren von Datensatzregeln, Marketing-Touchpoints und Konversionsdefinitionen verwendet. |
   | Kategorie | Gibt an, ob ein harmonisiertes Datenfeld ein [!UICONTROL Dimension], ein [!UICONTROL Metric] oder ein [!UICONTROL Derived] ist. Eine abgeleitete Kategorie ist ein harmonisiertes Feld, das eine metrikbasierte Formeldefinition verwendet. |
   | Datentyp | Gibt den Datentyp an ([!UICONTROL Number], [!UICONTROL String], [!UICONTROL Currency], [!UICONTROL Date time]). |
   | Erstellungsdatum | Datum und Uhrzeit der Erstellung des harmonisierten Felds. |
   | Besitzer | Gibt an, ob ein harmonisiertes Feld ein Standardfeld ist ([!UICONTROL Global]) oder von Ihnen definiert wird ([!UICONTROL Client]). |
   | Datum der letzten Änderung | Datum und Uhrzeit der letzten Änderung des harmonisierten Felds. |
   | Formel | Gibt die Formel für ein harmonisiertes Feld an, das auf einer abgeleiteten Kategorie basiert. |

   {style="table-layout:auto"}

1. Um nach einem bestimmten harmonisierten Feld zu suchen, verwenden Sie ![Suche](/help/assets/icons/Search.svg) **[!UICONTROL *Harmonisiertes Feld suchen *]**.


### Harmonisiertes Feld hinzufügen

Um ein harmonisiertes Feld hinzuzufügen, gehen Sie in der ![DataSearch](/help/assets/icons/DataCheck.svg)-**[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** im Mix Modeler folgendermaßen vor:

1. Wählen Sie ![Hinzufügen](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add field]** aus.

1. Im Dialogfeld **[!UICONTROL Create]** :

   1. Geben Sie einen **[!UICONTROL Field name]** ein, z. B. `region`.
   1. Geben Sie einen **[!UICONTROL Display name]** ein, z. B. `Region`.
   1. Wählen Sie eine **[!UICONTROL Category]** aus: **[!UICONTROL Dimension]**, **[!UICONTROL Metric]** oder **[!UICONTROL Derived]**.

      Wenn Sie **[!UICONTROL Derived]** auswählen, geben Sie eine **[!UICONTROL Formula]** an. Um einen gültigen arithmetischen Ausdruck zu erstellen, kombinieren Sie eine oder mehrere Metriken aus **[!UICONTROL Insert Metric]** mit einem oder mehreren Operatoren **[!UICONTROL + - * / ( )]** . Beispiel: `[orders]/[impressions]`

   1. **[!UICONTROL Data type]** auswählen.

      - **[!UICONTROL String]** oder **[!UICONTROL Date time]**, wenn die ausgewählte Kategorie &quot;Dimension&quot; ist.
      - **[!UICONTROL Number]** oder **[!UICONTROL Currency]**, wenn die ausgewählte Kategorie „Metrik“ oder „Abgeleitet“ ist.

   1. Wählen Sie **[!UICONTROL Submit]** aus, um das harmonisierte Feld hinzuzufügen. Wählen Sie **[!UICONTROL Close]** aus, um das Dialogfeld zu schließen, ohne das harmonisierte Feld hinzuzufügen.

      ![Feld erstellen](/help/assets/create-field.png)


### Harmonisiertes Feld bearbeiten

Sie können nur harmonisierte Felder bearbeiten, die Sie zuvor erstellt haben (Eigentümer ist Kunde). Globale harmonisierte Felder können nicht bearbeitet werden.

So bearbeiten Sie ein harmonisiertes Feld in der ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** im Mix Modeler:

1. Wählen Sie das harmonisierte Feld aus, das Sie bearbeiten möchten. Beispiel: **[!UICONTROL Region]**.

1. Ändern Sie im **[!UICONTROL Edit harmonization values]** die Werte für **[!UICONTROL Display name]**, **[!UICONTROL Category]** und **[!UICONTROL Data type]**. Weitere [ finden Sie unter &quot;](#add-a-harmonized-field) Feld hinzufügen“.

1. Wählen Sie **[!UICONTROL Submit]** aus, um die Änderungen auf das harmonisierte Feld anzuwenden.

   ![Bearbeiten eines Felds](/help/assets/edit-field.png)

### Löschen eines harmonisierten Felds

Sie können nur harmonisierte Felder löschen, die Sie zuvor erstellt haben (Eigentümer ist Kunde). Globales harmonisiertes Feld kann nicht gelöscht werden.

So löschen Sie ein harmonisiertes Feld in der ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** im Mix Modeler:

1. Wählen Sie das harmonisierte Feld aus, das Sie löschen möchten, z. B. **[!UICONTROL Region]**.

1. Wählen Sie ![ linken Bereich ](/help/assets/icons/Delete.svg)Löschen **[!UICONTROL Delete]** **[!UICONTROL Edit harmonization values]** aus.

   >[!WARNING]
   >
   >   Das Feld wird sofort gelöscht.

