---
title: Erstellen von Modellen
description: Erfahren Sie, wie Sie in Mix Modeler Modelle erstellen.
feature: Models
exl-id: e1093c09-1e23-460b-92de-cfb0061112fd
source-git-commit: 3b6b127bfaf79cee99a869b21ff0c1a911b3ad6c
workflow-type: tm+mt
source-wordcount: '910'
ht-degree: 0%

---

# Erstellen von Modellen

Um Ihre benutzerdefinierten KI-gestützten Modelle zu erstellen, bietet die Benutzeroberfläche einen Schritt-für-Schritt-Konfigurationsablauf für Modelle.

Wählen Sie in ![ Models](/help/assets/icons/FileData.svg)-**[!UICONTROL Models]** in Mix Modeler **[!UICONTROL Open model canvas]** aus.

## Einrichten

Name und Beschreibung werden im **[!UICONTROL Setup]** Schritt definiert:

1. Geben Sie Ihre **[!UICONTROL Name]** ein, z. B. `Demo model`. Geben Sie einen **[!UICONTROL Description]** ein, z. B. `Demo model to explore AI featues of Mix Modeler`.

   ![Modellname und -beschreibung](/help/assets/model-name-description.png)

1. Wählen Sie **[!UICONTROL Next]** aus, um mit dem nächsten Schritt fortzufahren. Wählen Sie **[!UICONTROL Cancel]** aus, um die Modellkonfiguration abzubrechen.

## Konfigurieren

Das Modell wird im **[!UICONTROL Configure]** konfiguriert. Die Konfiguration umfasst die Definition von Konversionszielen, Marketing-Touchpoints, die geeignete Datenpopulation, externe und interne Faktoren und mehr.

1. Im **[!UICONTROL Conversion goal]** Abschnitt:

   ![Modell - Konvertierungsschritt](/help/assets/model-conversion-step.png)

   1. Wählen Sie im Dropdown-Menü **[!UICONTROL Conversion]** eine Konvertierung aus. Die verfügbaren Konversionen sind die Konversionen, die Sie als Teil von &quot;[&quot; ](../harmonize-data/conversions.md) [!UICONTROL Harmonized datasets] definiert haben. Beispiel: **[!UICONTROL Online Conversion]**.

   1. Sie können **[!UICONTROL Create a conversion]** ![LinkOutLight](/help/assets/icons/LinkOutLight.svg) auswählen, um eine Konvertierung direkt aus der Modellkonfiguration heraus zu erstellen.



1. Im Abschnitt **[!UICONTROL Marketing touchpoints]** können Sie einen oder mehrere Marketing-Touchpoints auswählen, die den Marketing-Touchpoints entsprechen, die Sie als Teil von [Marketing-Touchpoints](../harmonize-data/marketing-touchpoints.md) in [!UICONTROL Harmonized datasets] definiert haben.


   ![Modell - Marketing-Touchpoint-Schritt](/help/assets/model-marketing-touchpoint-step.png)

   1. Wählen Sie einen oder mehrere Marketing-Touchpoints aus dem Dropdown-Menü **[!UICONTROL Touchpoint include]** aus.

      * Sie können ![CrossSize75](/help/assets/icons/CrossSize75.svg) verwenden, um einen Touchpoint zu entfernen.
      * Sie können **[!UICONTROL Clear all]** verwenden, um alle Touchpoints zu entfernen.

   1. Sie können **[!UICONTROL Create a touchpoint]** ![LinkOutLight](/help/assets/icons/LinkOutLight.svg) auswählen, um einen Marketing-Touchpoint direkt in der Modellkonfiguration zu erstellen.

   >[!NOTE]
   >
   >Sie können das Modell nicht mit Touchpoints einrichten, die sich überschneidende Daten haben, und es muss mindestens einen Touchpoint mit Ausgaben geben.

1. Standardmäßig wird eine Punktzahl für alle Daten in Ihrer harmonisierten Ansicht generiert. Um nur eine Teilmenge der Population zu bewerten, definieren Sie einen oder mehrere Filter mithilfe von Containern im Abschnitt **[!UICONTROL Eligible data population]** .

   ![Modell - Mögliche Datenpopulation](/help/assets/model-eligible-data-population-step.png)

   * Definieren Sie für jeden Container ein oder mehrere Ereignisse.

      1. Für jedes Ereignis:

         1. Wählen Sie eine Metrik oder Dimension aus **[!UICONTROL _Harmonisiertes Feld auswählen_]**.

         1. Wählen Sie den entsprechenden Operator aus: **[!UICONTROL equals]**, **[!UICONTROL not equals]**, **[!UICONTROL less than]**, **[!UICONTROL greater than]**, **[!UICONTROL starts with]**, **[!UICONTROL doesn't start with]**, **[!UICONTROL ends with]**, **[!UICONTROL doesn't end with]**, **[!UICONTROL contains]**, **[!UICONTROL doesn't contain]**, **[!UICONTROL is in]** oder **[!UICONTROL is not in]**.

         1. Einen Wert eingeben oder auswählen unter **[!UICONTROL _Wert eingeben oder_]**.

      1. Um ein zusätzliches Ereignis zum Container hinzuzufügen, wählen Sie ![Hinzufügen](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add event]**.

      1. Um ein Ereignis aus dem Container zu entfernen, klicken Sie auf ![Schließen](/help/assets/icons/CrossSize75.svg).

      1. Um nach allen oder mehreren im Container definierten Ereignissen zu filtern, wählen Sie **[!UICONTROL Any of]** oder **[!UICONTROL All of]** aus. Entsprechend ändert sich die Bezeichnung von **[!UICONTROL Include ... Or ...]** zu **[!UICONTROL Include ... And ...]**.

   * Um einen geeigneten Datenpopulations-Container hinzuzufügen, wählen Sie ![Hinzufügen](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add eligible population]** aus.

   * Um einen geeigneten Datenpopulations-Container zu entfernen, wählen Sie innerhalb des Containers ![Mehr](/help/assets/icons/More.svg) und wählen Sie **[!UICONTROL Remove marketing touchpoint]** aus dem Kontextmenü aus.

   * Wählen Sie **Und** und **Oder** zwischen Containern aus, um komplexere Definitionen für Ihre auswählbare Datenpopulation zu erstellen.


1. Um Datensätze mit externen Faktoren zu Ihrem Modell hinzuzufügen, verwenden Sie einen oder mehrere Container im **[!UICONTROL External factors dataset]**. Ein Beispiel für externe Faktoren sind S&amp;P-Indizes.

   ![Modell - Datensatz für externe Faktoren](/help/assets/model-external-factors-dataset-step.png)

   * Für jeden Container:

      1. Geben Sie einen **[!UICONTROL External factor name]** ein, z. B. `External Factors`.

      1. Wählen Sie einen Datensatz aus dem Dropdown-Menü **[!UICONTROL Dataset]** aus. Sie können ![Daten](/help/assets/icons/Data.svg) auswählen, um Datensätze zu verwalten. Weitere Informationen finden [ unter ](../ingest-data/datasets.md)Datensätze“.

      1. Wählen Sie eine Option aus dem Dropdown-Menü **[!UICONTROL Impact on conversion]** aus: **[!UICONTROL Auto select]**, **[!UICONTROL Positive]** oder **[!UICONTROL Negative]**. Die Standardoption ist **[!UICONTROL Auto select]**, mit der das Modell die Auswirkungen bestimmen kann. Sie können den Standardwert überschreiben.

   * Um einen zusätzlichen Datensatz-Container für externe Faktoren hinzuzufügen, wählen Sie ![Hinzufügen](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add external factor]**.

   * Um einen Datensatz-Container für externe Faktoren zu entfernen, wählen Sie ![RemoveCircle](/help/assets/icons/RemoveCircle.svg) aus.




1. Um Datensätze mit internen Faktoren zu Ihrem Modell hinzuzufügen, verwenden Sie einen oder mehrere Container im **[!UICONTROL Internal factors dataset]**. Ein Beispiel für interne Faktoren sind E-Mail-Marketing-Daten.

   ![Modell - Datensatz für interne Faktoren](/help/assets/model-internal-factors-dataset-step.png)

   * Für jeden Container:

      1. Geben Sie einen **[!UICONTROL Internal factor name]** ein, z. B. `Email Marketing Data`.

      1. Wählen Sie einen Datensatz aus **[!UICONTROL _Datensatz auswählen_]**. Sie können ![Daten](/help/assets/icons/Data.svg) auswählen, um Datensätze zu verwalten. Weitere Informationen finden [ unter ](../ingest-data/datasets.md)Datensätze“.

      1. Wählen Sie eine Option aus dem Dropdown-Menü **[!UICONTROL Impact on conversion]** aus: **[!UICONTROL Auto select]**, **[!UICONTROL Positive]** oder **[!UICONTROL Negative]**.

   * Um einen zusätzlichen Datensatz-Container für interne Faktoren hinzuzufügen, wählen Sie ![Hinzufügen](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add internal factor]**.

   * Um einen Datensatz-Container für interne Faktoren zu entfernen, wählen Sie ![RemoveCircle](/help/assets/icons/RemoveCircle.svg) aus.



1. Um das Lookback-Fenster für das Modell zu definieren, geben Sie einen Wert zwischen `1` und `52` in **[!UICONTROL Give contribution credit to touchpoints occurring within]** **[!UICONTROL weeks prior to the conversion]** … ein.

1. Wählen Sie **[!UICONTROL Next]** aus, um mit dem nächsten Schritt fortzufahren. Wenn eine weitere Konfiguration erforderlich ist, wird in einem roten Umriss und Text erläutert, welche zusätzlichen Konfigurationen erforderlich sind. <br/>Wählen Sie **[!UICONTROL Back]** aus, um zum vorherigen Schritt zurückzukehren. <br/>Wählen Sie **[!UICONTROL Cancel]** aus, um die Modellkonfiguration abzubrechen.


## Erweitert

Im **[!UICONTROL Advanced]** Schritt können Sie erweiterte Einstellungen festlegen. In diesem Schritt können Sie Ihr Modell für die Multi-Touch-Attribution (MTA) aktivieren.

1. Im **[!UICONTROL Spend share]** Abschnitt:

   * Um historische Marketing-Investitionsquoten zu verwenden und das Modell bei geringen Marketing-Daten zu informieren, aktivieren Sie **[!UICONTROL Allow spend share]**.

1. Im **[!UICONTROL MTA enabled]** Abschnitt:

   * Um MTA-Funktionen für das Modell zu aktivieren, aktivieren Sie **[!UICONTROL MTA enabled]**. Wenn Sie MTA aktiviert haben, sind Multi-Touch-Attributionseinblicke verfügbar, nachdem Sie Ihr Modell trainiert und bewertet haben. Weitere Informationen finden Sie [ Registerkarte ](insights.md#attribution)Attribution“ in [Modell-Insights](insights.md).

1. Im **[!UICONTROL Prior knowledge]** Abschnitt:

   ![Modell - Vorkenntnisse](/help/assets/model-prior-knowledge-step.png)

   1. Wählen Sie die **[!UICONTROL Rule type]** aus, die standardmäßig **[!UICONTROL Absolute values]** ist.

   1. Geben Sie mithilfe der Spalte **[!UICONTROL Contribution proportion]** die Beitragsprozentsätze für jeden der unter **[!UICONTROL Name]** aufgelisteten Kanäle an.

   1. Bei Bedarf können Sie für jeden Kanal einen **[!UICONTROL Level of confidence]** Prozentsatz hinzufügen.

   1. Verwenden Sie bei Bedarf **[!UICONTROL Clear all]** , um alle Eingabewerte für die Spalten **[!UICONTROL Contribution proportion]** und **[!UICONTROL Level of confidence]** zu löschen.


## Zeitplan

Im **[!UICONTROL Schedule]** Schritt können Sie das Training und die Bewertung für Ihr Modell planen.

1. Im **[!UICONTROL Schedule]** Abschnitt können Sie das Modell-Training und die Bewertung planen.

   ![Modell planen](../assets/model-schedule.png)

   Zur geplanten Modellbewertung und zum Training:

   1. Schalte **[!UICONTROL Enable scheduled model scoring and training]** ein.
   1. **[!UICONTROL Scoring frequency]** auswählen:

      * **[!UICONTROL Daily]**: Geben Sie eine gültige Zeit ein (z. B. `05:22 pm`) oder verwenden Sie ![Uhr](/help/assets/icons/Clock.svg).
      * **[!UICONTROL Weekly]**: Wählen Sie einen Wochentag aus und geben Sie eine gültige Zeit ein (z. B. `05:22 pm`) oder verwenden Sie ![Uhr](/help/assets/icons/Clock.svg).
      * **[!UICONTROL Monthly]**: Wählen Sie einen Tag des Monats aus dem Dropdown-Menü Ausführen für jedes Dropdown-Menü aus und geben Sie eine gültige Zeit ein (z. B. `05:22 pm`) oder verwenden Sie ![Uhr](/help/assets/icons/Clock.svg).

   1. Wählen Sie eine **[!UICONTROL Training frequency]** aus dem Dropdown-Menü aus: **[!UICONTROL Monthly]**, **[!UICONTROL Quarterly]**, **[!UICONTROL Yearly]** oder **[!UICONTROL None]**.

1. Wählen Sie im Abschnitt **[!UICONTROL Define training window]** zwischen:

   ![Modell - Trainings-Fenster definieren](/help/assets/model-define-training-window.png)

   * **[!UICONTROL Have Mix Modeler select a helpful training window]** und

   * **[!UICONTROL Manually input a training window]**. Wenn ausgewählt, definieren Sie die Anzahl der Jahre in **[!UICONTROL Include events the following years prior to a conversion]**.


1. Wählen Sie **[!UICONTROL Finish]** aus, um Ihre Modellkonfiguration abzuschließen.

   * Wählen Sie im Dialogfeld **[!UICONTROL Create instance?]** die Option **[!UICONTROL Ok]** aus, um den ersten Satz von Trainings- und Scoring-Durchgängen sofort mit dem Trigger zu versehen. Ihr Modell wird mit dem Status ![StatusOrange](/help/assets/icons/StatusOrange.svg) **[!UICONTROL Awaiting training]** aufgelistet.

     Wählen Sie zum Abbrechen **[!UICONTROL Cancel]** aus.

   * Wenn eine weitere Konfiguration erforderlich ist, wird in einem roten Umriss und Text erläutert, welche zusätzlichen Konfigurationen erforderlich sind.

   Wählen Sie **[!UICONTROL Back]** aus, um zum vorherigen Schritt zurückzukehren.

   Wählen Sie **[!UICONTROL Cancel]** aus, um die Modellkonfiguration abzubrechen.
