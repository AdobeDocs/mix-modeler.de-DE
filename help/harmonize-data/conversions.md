---
title: Konversionen
description: Erfahren Sie, wie Sie Konversionen erstellen, die im Rahmen der Harmonisierung Ihrer Daten in Mix Modeler verwendet werden.
feature: Harmonized Data, Conversions
exl-id: a8559426-452a-43e8-9a60-0c0bc97d863c
source-git-commit: 9085363e951a4e306c64ad28f56e2c15b4a6029a
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 1%

---

# Konversionen

Konversionsereignisse sind Geschäftsziele, die die Auswirkungen von Marketingaktivitäten identifizieren. Beispiele: E-Commerce-Bestellungen, In-Store-Käufe, Website-Besuche usw.

Sie definieren Marketing-Konversionen für die Attributionsanalyse.

## Konversionen verwalten

Um eine Tabelle der verfügbaren Konvertierungen anzuzeigen, gehen Sie in die Mix Modeler-Oberfläche:

1. Auswählen ![DataSearch](/help/assets//icons/DataCheck.svg) **[!UICONTROL Harmonized data]** über die linke Leiste.

1. Auswählen **[!UICONTROL Conversions]** aus der oberen Leiste. Es wird eine Tabelle der Konversionen angezeigt.

Die Tabellenspalten geben Details zur Konvertierung an:

| Spaltenname | Details |
| --- | ---|
| Name | Der Name der Konvertierung. |
| Umsatz | Die harmonisierte Datenmetrik zur Berechnung des Umsatzes. |
| Konversionsmetrik | Die harmonisierte Datenmetrik, die als Konversionsmetrik für die Analyse verwendet werden soll. |
| Kategorie | Die Konversionskategorie der Konversion. |
| Erstellt | Datum und Uhrzeit der Erstellung der Konvertierung. |
| Zuletzt geändert | Datum und Uhrzeit der letzten Änderung der Konversion. |

{style="table-layout:auto"}

## Konvertierung hinzufügen

Um eine Konversion hinzuzufügen, müssen Sie im ![DataSearch](/help/assets//icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Conversion]** -Schnittstelle in Mix Modeler:

1. Auswählen ![Hinzufügen](/help/assets//icons/AddCircle.svg) **[!UICONTROL Add a conversion]**.

1. Im **[!UICONTROL Create conversion]** dialog:

   1. Geben Sie einen Namen für **[!UICONTROL Conversion]**, beispielsweise `Store Conversions`.

   1. Definieren Sie die **[!UICONTROL Conversion category]**.

      1. Wählen Sie einen Wert aus **[!UICONTROL *Harmonisieren...*]**, beispielsweise `Conversion types`.

      1. Wert für den Operator auswählen ![Chevron](/help/assets//icons/ChevronDown.svg), beispielsweise **[!UICONTROL is]**.

      1. Wählen Sie einen Wert aus **[!UICONTROL *Wert auswählen *]**oder geben Sie einen Wert ein, beispielsweise **[!UICONTROL Store]**.

   1. Wählen Sie ein harmonisiertes Feld aus **[!UICONTROL Conversion metric for analysis]**, beispielsweise **[!UICONTROL Orders]**.

   1. Wählen Sie ein harmonisiertes Feld aus **[!UICONTROL Revenue field]**, beispielsweise **[!UICONTROL Gross Demand]**.

   1. Um die Konvertierung zu erstellen, wählen Sie **[!UICONTROL Create]**. Um die Erstellung einer Konvertierung abzubrechen, wählen Sie **[!UICONTROL Cancel]**.

      ![Alternativtext](/help/assets//create-conversion.png)

1. Nach der Erstellung wird die Konversion der Konversionstabelle hinzugefügt.


## Konvertierung anzeigen

So zeigen Sie eine Konversion an:

1. Auswählen ![Mehr](/help/assets//icons/More.svg) wenn Sie den Mauszeiger über einen Konversionsnamen in der Tabelle bewegen.

1. Auswählen ![Ansicht](/help/assets//icons/ViewDetail.svg) **Ansicht**. In einem Dialogfeld werden Details zur Konvertierung angezeigt. Siehe [Konvertierung hinzufügen](#add-a-conversion) für weitere Informationen. Auswählen **[!UICONTROL Cancel]** , um das Dialogfeld zu schließen.


## Löschen von Konversionen

So löschen Sie eine Konversion:

1. Auswählen ![Löschen](/help/assets//icons/Delete.svg) **Löschen** wenn Sie den Mauszeiger über einen Konversionsnamen in der Tabelle bewegen.
1. Im **[!UICONTROL Delete conversion]** Dialogfeld zur Dialogbestätigung auswählen **[!UICONTROL Delete]** , um die Konvertierung dauerhaft zu löschen.
