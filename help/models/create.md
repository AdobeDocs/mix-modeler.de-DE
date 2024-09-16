---
title: Modell erstellen
description: Erfahren Sie, wie Sie in Mix Modeler ein Modell erstellen.
feature: Models
exl-id: e1093c09-1e23-460b-92de-cfb0061112fd
source-git-commit: 9a6c1f1c12ab29da80a1997cfd31ca07b38eaa22
workflow-type: tm+mt
source-wordcount: '691'
ht-degree: 0%

---

# Modell erstellen

Um ein Modell zu erstellen, wählen Sie in der Benutzeroberfläche ![Modelle](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** im Mix Modeler **[!UICONTROL Open model canvas]** aus.

Um Ihre benutzerdefinierten KI-gestützten Modelle zu erstellen, bietet die Benutzeroberfläche einen schrittweisen Konfigurationsfluss für Modelle.

1. Im Schritt **[!UICONTROL Setup]** :

   1. Geben Sie Ihr Modell **[!UICONTROL Name]** ein, z. B. `Demo model`. Geben Sie einen **[!UICONTROL Description]** ein, z. B. `Demo model to explore AI featues of Mix Modeler`.

      ![Modellname und Beschreibung](/help/assets/model-name-description.png)

   1. Wählen Sie **[!UICONTROL Next]** aus, um mit dem nächsten Schritt fortzufahren. Wählen Sie **[!UICONTROL Cancel]** aus, um die Modellkonfiguration abzubrechen.

1. Im Schritt **[!UICONTROL Configure]** :

   1. Im Abschnitt **[!UICONTROL Conversion goal]** innerhalb des Containers:

      1. Geben Sie einen **[!UICONTROL Conversion name]** für die Konvertierung ein, z. B. `Conversion`

      1. Wählen Sie eine Konvertierung aus **[!UICONTROL *Harmonisiertes Feld auswählen *]**, das die verfügbaren Konversionen enthält, die Sie als Teil von [Konversionen](../harmonize-data/conversions.md) in [!UICONTROL Harmonized datasets] definiert haben. Beispiel:**[!UICONTROL Online Conversion]**.

      1. Sie können ![Antwort](/help/assets/icons/Reply.svg) **[!UICONTROL Create new conversion]** auswählen, um eine Konversion direkt aus der Modellkonfiguration zu erstellen.

         ![Modell - Konvertierungsschritt](/help/assets/model-conversion-step.png)

   1. Im Abschnitt **[!UICONTROL Marketing touchpoints]** sehen Sie eine Reihe von Marketing-Touchpoint-Containern, die den Marketing-Touchpoints entsprechen, die Sie in [!UICONTROL Harmonized datasets] als Teil von [Marketing-Touchpoints](../harmonize-data/marketing-touchpoints.md) definiert haben.

      * Für jeden Behälter:

         1. Sie können die **[!UICONTROL Marketing touchpoint name]** ändern.

         1. Wählen Sie einen Marketing-Touchpoint aus **[!UICONTROL _Marketing-Touchpoint auswählen_]**.

         1. Sie können ![Antwort](/help/assets/icons/Reply.svg) **[!UICONTROL Create new marketing touchpoint]** auswählen, um einen Marketing-Touchpoint direkt in der Modellkonfiguration zu erstellen.

      * Um einen Marketing-Touchpoint-Container hinzuzufügen, wählen Sie ![Hinzufügen](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add marketing touchpoint]** aus.

      * Um einen Marketing-Touchpoint-Container zu entfernen, wählen Sie im Container ![Mehr](/help/assets/icons/More.svg) und dann im Kontextmenü die Option **[!UICONTROL Remove container]** aus.

        ![Modell - Marketing-Touchpoints-step](/help/assets/model-marketing-touchpoint-step.png)

   1. Standardmäßig wird ein Ergebnis für alle Daten in Ihrer harmonisierten Ansicht generiert. Um nur eine Teilmenge der Population zu bewerten, definieren Sie einen oder mehrere Filter mithilfe von Containern im Abschnitt **[!UICONTROL Eligible data population]** .

      * Definieren Sie für jeden Container ein oder mehrere Ereignisse.

         1. Für jedes Ereignis:

            1. Wählen Sie eine Metrik oder Dimension aus **[!UICONTROL _Harmonisiertes Feld auswählen_]** aus.

            1. Wählen Sie den entsprechenden Operator aus: **[!UICONTROL equals]**, **[!UICONTROL not equals]**, **[!UICONTROL less than]**, **[!UICONTROL greater than]**, **[!UICONTROL starts with]**, **[!UICONTROL doesn't start with]**, **[!UICONTROL ends with]**, **[!UICONTROL doesn't end with]**, **[!UICONTROL contains]**, **[!UICONTROL doesn't contain]**, **[!UICONTROL is in]** oder **[!UICONTROL is not in]**.

            1. Geben Sie unter **[!UICONTROL _Wert eingeben oder auswählen_]** einen Wert ein.

         1. Um dem Container ein zusätzliches Ereignis hinzuzufügen, wählen Sie ![Hinzufügen](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add event]** aus.

         1. Um ein Ereignis aus dem Container zu entfernen, wählen Sie ![Schließen](/help/assets/icons/Close.svg) aus.

         1. Um nach allen oder mehreren im Container definierten Ereignissen zu filtern, wählen Sie **[!UICONTROL Any of]** oder **[!UICONTROL All of]** aus. Die Bezeichnung ändert sich entsprechend von **[!UICONTROL Include ... Or ...]** in **[!UICONTROL Include ... And ...]**.

      * Um einen geeigneten Datenpopulationsbehälter hinzuzufügen, wählen Sie ![Hinzufügen](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add eligible population]** aus.

      * Um einen geeigneten Datenpopulations-Container zu entfernen, wählen Sie im Container ![Mehr](/help/assets/icons/More.svg) und dann im Kontextmenü die Option **[!UICONTROL Remove marketing touchpoint]** aus.

        ![Modell - Berechtigte Datenpopulation](/help/assets/model-eligible-data-population-step.png)

   1. Um Ihrem Modell Datensätze mit externen Faktoren hinzuzufügen, verwenden Sie einen oder mehrere Behälter im Abschnitt **[!UICONTROL External factors dataset]** .

      * Für jeden Behälter:

         1. Geben Sie einen **[!UICONTROL Factor name]** bei **[!UICONTROL _Faktor eingeben_]** ein.

         1. Wählen Sie einen Datensatz aus **[!UICONTROL _Datensatz auswählen_]**. Sie können ![Daten](/help/assets/icons/Data.svg) auswählen, um Datensätze zu verwalten. Weitere Informationen finden Sie unter [Datensätze](../ingest-data/datasets.md) .

      * Um einen weiteren Datensatz-Container mit externen Faktoren hinzuzufügen, wählen Sie ![Hinzufügen](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add external factor]** aus.

      * Um einen externen Faktoren-Datensatz-Container zu entfernen, wählen Sie im Container ![Mehr](/help/assets/icons/More.svg) und dann im Kontextmenü die Option **[!UICONTROL Remove external factor]** aus.

        ![Modell - Datensatz mit externen Faktoren](/help/assets/model-external-factors-dataset-step.png)


   1. Um Ihrem Modell Datensätze mit internen Faktoren hinzuzufügen, verwenden Sie einen oder mehrere Behälter im Abschnitt **[!UICONTROL Internal factors dataset]** .

      * Für jeden Behälter:

         1. Geben Sie einen **[!UICONTROL Factor name]** bei **[!UICONTROL _Faktor eingeben_]** ein.

         1. Wählen Sie einen Datensatz aus **[!UICONTROL _Datensatz auswählen_]**. Sie können ![Daten](/help/assets/icons/Data.svg) auswählen, um Datensätze zu verwalten. Weitere Informationen finden Sie unter [Datensätze](../ingest-data/datasets.md) .

      * Um einen weiteren internen Faktoren-Datensatz-Container hinzuzufügen, wählen Sie ![Hinzufügen](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add internal factor]** aus.

      * Um einen zusätzlichen internen Faktoren-Datensatz-Container zu entfernen, wählen Sie im Container ![Mehr](/help/assets/icons/More.svg) und **[!UICONTROL Remove internal factor]** aus dem Kontextmenü aus.

        ![Modell - Interner Faktor-Datensatz](/help/assets/model-internal-factors-dataset-step.png)

   1. Um das Lookback-Fenster für das Modell zu definieren, geben Sie einen Wert zwischen `1` und `52` in **[!UICONTROL Give contribution credit to touchpoints occurring within]** ... **[!UICONTROL weeks prior to the conversion]** ein.

   1. Wählen Sie **[!UICONTROL Next]** aus, um mit dem nächsten Schritt fortzufahren. Wenn mehr Konfiguration erforderlich ist, wird in einem roten Entwurf und Text beschrieben, welche zusätzliche Konfiguration erforderlich ist. <br/>Wählen Sie **[!UICONTROL Back]** aus, um zum vorherigen Schritt zurückzukehren. <br/>Wählen Sie **[!UICONTROL Cancel]** aus, um die Modellkonfiguration abzubrechen.

1. Im Schritt **[!UICONTROL Advanced]** :

   1. Wählen Sie im Abschnitt **[!UICONTROL Define training window]** zwischen

      * **[!UICONTROL Have Mix Modeler select a helpful training window]** und

      * **[!UICONTROL Manually input a training window]**. Wenn diese Option aktiviert ist, definieren Sie die Anzahl der Jahre in **[!UICONTROL Include events the following years prior to a conversion]**.

        ![Modell - Trainings-Fenster definieren](/help/assets/model-define-training-window.png)

   1. Im Abschnitt **[!UICONTROL Spend share]** :

      * Wenn Sie historische Marketing-Investment-Verhältnisse verwenden möchten, um das Modell zu informieren, wenn die Marketing-Daten gering sind, aktivieren Sie **[!UICONTROL Allow spend share]**.

   1. Im Abschnitt **[!UICONTROL Prior knowledge]** :

      1. Wählen Sie die **[!UICONTROL Rule type]**.

      1. Geben Sie mithilfe der Spalte **[!UICONTROL Contribution proportion]** Beitragsprozentsätze für jeden der unter **[!UICONTROL Name]** aufgelisteten Kanäle an.

      1. Gegebenenfalls können Sie für jeden Kanal einen **[!UICONTROL Level of confidence]** Prozentsatz hinzufügen.

      1. Verwenden Sie bei Bedarf **[!UICONTROL Clear all]** , um alle Eingabewerte für die Spalten **[!UICONTROL Contribution proportion]** und **[!UICONTROL Level of confidence]** zu löschen.

         ![Modell - Vorkenntnisse](/help/assets/model-prior-knowledge-step.png)

1. Wählen Sie **[!UICONTROL Finish]** aus, um die Modellkonfiguration abzuschließen.

   * Wählen Sie im Dialogfeld **[!UICONTROL Create instance?]** die Option **[!UICONTROL Ok]** aus, um den ersten Satz von Trainings- und Scoring-Läufen sofort Trigger. Ihr Modell wird mit dem Status <span style="color:orange"></span> aufgeführt **[!UICONTROL Awaiting training]**.

     Wählen Sie **[!UICONTROL Cancel]** aus, um abzubrechen.

   * Wenn mehr Konfiguration erforderlich ist, wird in einem roten Entwurf und Text beschrieben, welche zusätzliche Konfiguration erforderlich ist.

   Wählen Sie **[!UICONTROL Back]** aus, um zum vorherigen Schritt zurückzukehren.

   Wählen Sie **[!UICONTROL Cancel]** aus, um die Modellkonfiguration abzubrechen.
