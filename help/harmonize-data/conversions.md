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

1. Wählen Sie ![DataSearch](/help/assets//icons/DataCheck.svg) **[!UICONTROL Harmonized data]** in der linken Leiste aus.

1. Wählen Sie in der oberen Leiste **[!UICONTROL Conversions]** aus. Es wird eine Tabelle der Konversionen angezeigt.

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

Um eine Konversion hinzuzufügen, gehen Sie in der Oberfläche ![DataSearch](/help/assets//icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Conversion]** in den Mix Modeler:

1. Wählen Sie ![Hinzufügen](/help/assets//icons/AddCircle.svg) **[!UICONTROL Add a conversion]** aus.

1. Im Dialogfeld **[!UICONTROL Create conversion]** :

   1. Geben Sie einen Namen für **[!UICONTROL Conversion]** ein, beispielsweise `Store Conversions`.

   1. Definieren Sie die **[!UICONTROL Conversion category]**.

      1. Wählen Sie einen Wert aus **[!UICONTROL *Harmonize...*]**, z. B. `Conversion types`.

      1. Wählen Sie einen Wert für den Operator ![Chevron](/help/assets//icons/ChevronDown.svg) aus, z. B. **[!UICONTROL is]**.

      1. Wählen Sie einen Wert aus **[!UICONTROL *Wert auswählen *]**oder geben Sie einen Wert ein, z. B.**[!UICONTROL Store]**.

   1. Wählen Sie ein harmonisiertes Feld aus &quot;**[!UICONTROL Conversion metric for analysis]**&quot;, z. B. &quot;**[!UICONTROL Orders]**&quot;.

   1. Wählen Sie ein harmonisiertes Feld aus &quot;**[!UICONTROL Revenue field]**&quot;, z. B. &quot;**[!UICONTROL Gross Demand]**&quot;.

   1. Wählen Sie **[!UICONTROL Create]** aus, um die Konvertierung zu erstellen. Um die Erstellung einer Konvertierung abzubrechen, wählen Sie **[!UICONTROL Cancel]** aus.

      ![ALT-Text](/help/assets//create-conversion.png)

1. Nach der Erstellung wird die Konversion der Konversionstabelle hinzugefügt.


## Konvertierung anzeigen

So zeigen Sie eine Konversion an:

1. Wählen Sie ![Mehr](/help/assets//icons/More.svg) aus, wenn Sie den Mauszeiger über einen Konversionsnamen in der Tabelle bewegen.

1. Wählen Sie ![Ansicht](/help/assets//icons/ViewDetail.svg) **Ansicht** aus. In einem Dialogfeld werden Details zur Konvertierung angezeigt. Weitere Informationen finden Sie unter [Konvertierung hinzufügen](#add-a-conversion) . Wählen Sie **[!UICONTROL Cancel]** aus, um das Dialogfeld zu schließen.


## Löschen von Konversionen

So löschen Sie eine Konversion:

1. Wählen Sie ![Löschen](/help/assets//icons/Delete.svg) **Löschen** aus, wenn Sie den Mauszeiger über einen Konversionsnamen in der Tabelle bewegen.
1. Wählen Sie im Bestätigungsdialogfeld **[!UICONTROL Delete conversion]** die Option **[!UICONTROL Delete]** aus, um die Konvertierung dauerhaft zu löschen.
