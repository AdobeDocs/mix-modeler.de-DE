---
title: Konversionen
description: Erfahren Sie, wie Sie Konversionen erstellen, die im Rahmen der Harmonisierung Ihrer Daten in Mix Modeler verwendet werden können.
feature: Harmonized Data, Conversions
exl-id: a8559426-452a-43e8-9a60-0c0bc97d863c
source-git-commit: 9a6c1f1c12ab29da80a1997cfd31ca07b38eaa22
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 1%

---

# Konversionen

Konversionsereignisse sind Geschäftsziele, die die Auswirkungen von Marketing-Aktivitäten identifizieren. Beispiele: E-Commerce-Bestellungen, In-Store-Käufe, Website-Besuche usw.

Marketing-Konversionen werden für die Attributionsanalyse definiert.

## Konversionen verwalten

Um eine Tabelle der verfügbaren Konvertierungen anzuzeigen, gehen Sie in der Benutzeroberfläche des Mix Modelers folgendermaßen vor:

1. Wählen Sie ![DataSearch](/help/assets/icons/DataCheck.svg)-**[!UICONTROL Harmonized data]** in der linken Leiste aus.

1. Wählen Sie **[!UICONTROL Conversions]** in der oberen Leiste aus. Eine Tabelle mit den Konversionen wird angezeigt.

Die Tabellenspalten geben Details zur Konversion an:

| Spaltenname | Details |
| --- | ---|
| Name | Der Name der Konversion. |
| Einnahmen | Die harmonisierte Datenmetrik, die zur Berechnung des Umsatzes aus einer Konversion verwendet wird. |
| Konversionsmetrik | Die harmonisierte Datenmetrik, die als Konversionsmetrik für die Analyse verwendet werden soll. |
| Kategorie | Die Konvertierungskategorie der Konversion. |
| Erstellt | Datum und Uhrzeit der Erstellung der Konversion. |
| Zuletzt geändert | Datum und Uhrzeit der letzten Änderung der Konvertierung. |

{style="table-layout:auto"}

## Konversion hinzufügen

Um eine Konversion hinzuzufügen, gehen Sie in der ![DataSearch](/help/assets/icons/DataCheck.svg)-**[!UICONTROL Harmonized data]** > **[!UICONTROL Conversion]** in den Mix Modeler:

1. Wählen Sie ![Hinzufügen](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add a conversion]** aus.

1. Im Dialogfeld **[!UICONTROL Create conversion]** :

   1. Geben Sie einen Namen für **[!UICONTROL Conversion]** ein, z. B. `Store Conversions`.

   1. Definieren Sie die **[!UICONTROL Conversion category]**.

      1. Wählen Sie einen Wert unter **[!UICONTROL *Wählen Sie Harmonisieren…*]**aus, z. B. `Conversion types`.

      1. Wählen Sie einen Wert für den Operator ![Chevron](/help/assets/icons/ChevronDown.svg), z. B. **[!UICONTROL is]**.

      1. Wählen Sie einen Wert unter **[!UICONTROL *Wert auswählen *]**aus oder geben Sie einen Wert ein, z. B.**[!UICONTROL Store]**.

   1. Wählen Sie ein harmonisiertes Feld aus **[!UICONTROL Conversion metric for analysis]** aus, z. B. **[!UICONTROL Orders]**.

   1. Wählen Sie ein harmonisiertes Feld aus **[!UICONTROL Revenue field]** aus, z. B. **[!UICONTROL Gross Demand]**.

   1. Um die Konversion zu erstellen, wählen Sie **[!UICONTROL Create]** aus. Um die Erstellung einer Konvertierung abzubrechen, wählen Sie **[!UICONTROL Cancel]** aus.

      ![ALT-Text](/help/assets/create-conversion.png)

1. Nach ihrer Erstellung wird die Konversion zur Konversionstabelle hinzugefügt.


## Konvertierung anzeigen

So zeigen Sie eine Konversion an:

1. Wählen Sie ![Mehr](/help/assets/icons/More.svg) aus, wenn Sie den Mauszeiger über einen Konversionsnamen in der Tabelle bewegen.

1. Wählen Sie ![Ansicht](/help/assets/icons/ViewDetail.svg) **Ansicht** aus. Ein Dialogfeld zeigt Details zur Konvertierung an. Weitere Informationen [ Sie unter ](#add-a-conversion) hinzufügen . Wählen Sie **[!UICONTROL Cancel]** aus, um das Dialogfeld zu schließen.


## Löschen einer Konversion

So löschen Sie eine Konversion:

1. Wählen Sie ![Löschen](/help/assets/icons/Delete.svg) **Löschen** aus, wenn Sie den Mauszeiger über einen Konversionsnamen in der Tabelle bewegen.
1. Wählen Sie im Bestätigungsdialogfeld **[!UICONTROL Delete conversion]** die Option **[!UICONTROL Delete]** aus, um die Konvertierung dauerhaft zu löschen.
