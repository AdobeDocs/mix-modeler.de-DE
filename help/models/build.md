---
title: Erstellen von Modellen in Mix Modeler
description: Erfahren Sie, wie Sie in Mix Modeler Modelle erstellen, einschließlich der Einrichtung, Konfiguration und Angabe erweiterter Optionen für das Modell.
feature: Models
solution: Mix Modeler
exl-id: e1093c09-1e23-460b-92de-cfb0061112fd
source-git-commit: 011b9b83569925ca9ff4f1ee472288473fbe8502
workflow-type: tm+mt
source-wordcount: '1276'
ht-degree: 2%

---

# Erstellen von Modellen

Um Ihre benutzerdefinierten KI-gestützten Modelle zu erstellen, bietet die Benutzeroberfläche einen Schritt-für-Schritt-Konfigurationsablauf für Modelle.

Wählen Sie in ![&#x200B; Models](/help/assets/icons/FileData.svg)-**[!UICONTROL Models]** in Mix Modeler **[!UICONTROL Open model canvas]** aus.

## Einrichten

Im **[!UICONTROL Setup]** Schritt definieren Sie einen Namen und eine Beschreibung:

1. Geben Sie Ihre **[!UICONTROL Name]** ein, z. B. `Demo model`. Geben Sie einen **[!UICONTROL Description]** ein, z. B. `Demo model to explore AI features of Mix Modeler`.

   ![Modellname und -beschreibung](/help/assets/model-name-description.png)

1. Wählen Sie **[!UICONTROL Next]** aus, um mit dem nächsten Schritt fortzufahren. Wählen Sie **[!UICONTROL Cancel]** aus, um die Modellkonfiguration abzubrechen.

## Konfigurieren{#configure}

>[!CONTEXTUALHELP]
>id="model_marketingtouchpoints_select"
>title="Marketing-Touchpoints"
>abstract="Marketing-Touchpoints sind Marketing-Ereignisse auf Empfangs-, Personen- und/oder Cookie-Ebene, mit denen die Auswirkungen von Marketing-Investitionen auf numerische oder umsatzbasierte Konversionen bewertet werden.<br/><br/>Sie können das Modell nicht mit Touchpoints einrichten, die überlappende Daten aufweisen, und es muss mindestens einen Touchpoint mit Ausgaben geben."

Das Modell wird im **[!UICONTROL Configure]** konfiguriert. Die Konfiguration umfasst die Definition von Konversionszielen, Marketing-Touchpoints, die geeignete Datenpopulation, externe und interne Faktoren und mehr.

1. Im **[!UICONTROL Conversion goal]** Abschnitt:

   ![Modell - Konvertierungsschritt](/help/assets/model-conversion-step.png)

   1. Wählen Sie im Dropdown-Menü **[!UICONTROL Conversion]** eine Konvertierung aus. Die verfügbaren Konversionen sind die Konversionen, die Sie als Teil von &quot;[&quot; &#x200B;](../harmonize-data/conversions.md) [!UICONTROL Harmonized datasets] definiert haben. Beispiel: **[!UICONTROL Online Conversion]**.

   1. Sie können ![&#x200B; &#x200B;](/help/assets/icons/LinkOutLight.svg)LinkOutLight **[!UICONTROL Create a conversion]** auswählen, um eine Konvertierung direkt aus der Modellkonfiguration heraus zu erstellen.



1. Im Abschnitt **[!UICONTROL Marketing touchpoints]** können Sie einen oder mehrere Marketing-Touchpoints auswählen, die den Marketing-Touchpoints entsprechen, die Sie als Teil von [Marketing-Touchpoints](../harmonize-data/marketing-touchpoints.md) in [!UICONTROL Harmonized datasets] definiert haben.


   ![Modell - Marketing-Touchpoint-Schritt](/help/assets/model-marketing-touchpoint-step.png)

   1. Wählen Sie einen oder mehrere Marketing-Touchpoints aus dem Dropdown-Menü **[!UICONTROL Touchpoint include]** aus.

      * Sie können ![CrossSize75](/help/assets/icons/CrossSize75.svg) verwenden, um einen Touchpoint zu entfernen.
      * Sie können **[!UICONTROL Clear all]** verwenden, um alle Touchpoints zu entfernen.

   1. Sie können ![&#x200B; &#x200B;](/help/assets/icons/LinkOutLight.svg)LinkOutLight **[!UICONTROL Create a touchpoint]** auswählen, um einen Marketing-Touchpoint direkt in der Modellkonfiguration zu erstellen.

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

   * Um einen geeigneten Datenpopulations-Container zu entfernen, wählen Sie innerhalb des Containers ![Mehr](/help/assets/icons/More.svg) und wählen Sie **[!UICONTROL Remove container]** aus dem Kontextmenü aus.

   * Wählen Sie **Und** und **Oder** zwischen Containern aus, um komplexere Definitionen für Ihre auswählbare Datenpopulation zu erstellen.


1. Um Datensätze mit externen Faktoren zu Ihrem Modell hinzuzufügen, verwenden Sie einen oder mehrere Container im **[!UICONTROL External factors dataset]**. Ein Beispiel für externe Faktoren sind S&amp;P-Indizes.

   ![Modell - Datensatz für externe Faktoren](/help/assets/model-external-factors-dataset-step.png)

   * Für jeden Container:

      1. Geben Sie einen **[!UICONTROL External factor name]** ein, z. B. `External Factors`.

      1. Wählen Sie einen Datensatz aus dem Dropdown-Menü **[!UICONTROL Dataset]** aus. Sie können ![Daten](/help/assets/icons/Data.svg) auswählen, um Datensätze zu verwalten. Weitere Informationen finden [&#x200B; unter &#x200B;](../ingest-data/datasets.md)Datensätze“.

      1. Wählen Sie eine Option aus dem Dropdown-Menü **[!UICONTROL Impact on conversion]** aus: **[!UICONTROL Auto select]**, **[!UICONTROL Positive]** oder **[!UICONTROL Negative]**. Die Standardoption ist **[!UICONTROL Auto select]**, mit der das Modell die Auswirkungen bestimmen kann. Sie können den Standardwert überschreiben.

   * Um einen zusätzlichen Datensatz-Container für externe Faktoren hinzuzufügen, wählen Sie ![Hinzufügen](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add external factor]**.

   * Um einen Datensatz-Container für externe Faktoren zu entfernen, wählen Sie ![RemoveCircle](/help/assets/icons/RemoveCircle.svg) aus.




1. Um Datensätze mit internen Faktoren zu Ihrem Modell hinzuzufügen, verwenden Sie einen oder mehrere Container im **[!UICONTROL Internal factors dataset]**. Ein Beispiel für interne Faktoren sind E-Mail-Marketing-Daten.

   ![Modell - Datensatz für interne Faktoren](/help/assets/model-internal-factors-dataset-step.png)

   * Für jeden Container:

      1. Geben Sie einen **[!UICONTROL Internal factor name]** ein, z. B. `Email Marketing Data`.

      1. Wählen Sie einen Datensatz aus **[!UICONTROL _Datensatz auswählen_]**. Sie können ![Daten](/help/assets/icons/Data.svg) auswählen, um Datensätze zu verwalten. Weitere Informationen finden [&#x200B; unter &#x200B;](../ingest-data/datasets.md)Datensätze“.

      1. Wählen Sie eine Option aus dem Dropdown-Menü **[!UICONTROL Impact on conversion]** aus: **[!UICONTROL Auto select]**, **[!UICONTROL Positive]** oder **[!UICONTROL Negative]**.

   * Um einen zusätzlichen Datensatz-Container für interne Faktoren hinzuzufügen, wählen Sie ![Hinzufügen](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add internal factor]**.

   * Um einen Datensatz-Container für interne Faktoren zu entfernen, wählen Sie ![RemoveCircle](/help/assets/icons/RemoveCircle.svg) aus.



1. Um das Lookback-Fenster für das Modell zu definieren, geben Sie einen Wert zwischen `1` und `52` in **[!UICONTROL Give contribution credit to touchpoints occurring within]** **[!UICONTROL weeks prior to the conversion]** … ein.

1. Wählen Sie **[!UICONTROL Next]** aus, um mit dem nächsten Schritt fortzufahren. Wenn eine weitere Konfiguration erforderlich ist, wird in einem roten Umriss und Text erläutert, welche zusätzlichen Konfigurationen erforderlich sind. <br/>Wählen Sie **[!UICONTROL Back]** aus, um zum vorherigen Schritt zurückzukehren. <br/>Wählen Sie **[!UICONTROL Cancel]** aus, um die Modellkonfiguration abzubrechen.


## Erweitert

Im **[!UICONTROL Advanced]** Schritt können Sie erweiterte Einstellungen festlegen. In diesem Schritt können Sie Ihr Modell für die Multi-Touch-Attribution (MTA) aktivieren.

1. Im **[!UICONTROL Spend share]** Abschnitt:

   * Um historische Marketing-Investitionsquoten zu verwenden und das Modell bei geringen Marketing-Daten zu informieren, aktivieren Sie **[!UICONTROL Allow spend share]**. Diese Einstellung wird insbesondere in den folgenden Szenarien empfohlen:
      * Ein Kanal verfügt nicht über genügend Beobachtungen (z. B. niedrige Ausgabenfrequenz, Impressionen oder Klicks).
      * Sie modellieren stark frequente, aber regelmäßige und potenziell teure Medien (wie das Fernsehen für einige Marken), bei denen die Daten spärlich sein können.

     >[!NOTE]
     >
     >Bei einmaligen Investitionen (z. B. einer Super Bowl-Anzeige) sollten Sie diese Daten als Faktor einbeziehen, anstatt sich auf den Ausgabenanteil zu verlassen.
     >


1. Im **[!UICONTROL MTA enabled]** Abschnitt:

   * Um MTA-Funktionen für das Modell zu aktivieren, aktivieren Sie **[!UICONTROL MTA enabled]**. Wenn Sie MTA aktiviert haben, sind Multi-Touch-Attributionseinblicke verfügbar, nachdem Sie Ihr Modell trainiert und bewertet haben. Weitere Informationen finden Sie [&#x200B; Registerkarte &#x200B;](insights.md#attribution)Attribution“ in [Modell-Insights](insights.md).

1. Im **[!UICONTROL Prior knowledge]** Abschnitt:

   ![Modell - Vorkenntnisse](/help/assets/model-prior-knowledge-step.png)

   1. Wählen Sie die **[!UICONTROL Rule type]** aus, die standardmäßig **[!UICONTROL Absolute values]** ist.

   1. Geben Sie mithilfe der Spalte **[!UICONTROL Name]** die Beitragsprozentsätze für jeden der unter **[!UICONTROL Contribution proportion]** aufgelisteten Kanäle an.

   1. Bei Bedarf können Sie für jeden Kanal einen **[!UICONTROL Level of confidence]** Prozentsatz hinzufügen.

   1. Verwenden Sie bei Bedarf **[!UICONTROL Clear all]** , um alle Eingabewerte für die Spalten **[!UICONTROL Contribution proportion]** und **[!UICONTROL Level of confidence]** zu löschen.


## Optionen festlegen

Sie können [Schulung und Bewertung &#x200B;](#schedule), [Trainings-Fenster definieren](#training-window) und [granulare Insights-Reporting-Felder](#granular-insights-reporting-fields) für Ihr Modell im **[!UICONTROL Set options]** Schritt angeben.


### Zeitplan

Im Abschnitt **[!UICONTROL Schedule]** können Sie das Modell-Training und die Bewertung planen.

![Modell planen](../assets/model-schedule.png)

Zur geplanten Modellbewertung und zum Training:

1. Schalte **[!UICONTROL Enable scheduled model scoring and training]** ein.
1. **[!UICONTROL Scoring frequency]** auswählen:

   * **[!UICONTROL Daily]**: Geben Sie eine gültige Zeit ein (z. B. `05:22 pm`) oder verwenden Sie ![Uhr](/help/assets/icons/Clock.svg).
   * **[!UICONTROL Weekly]**: Wählen Sie einen Wochentag aus und geben Sie eine gültige Zeit ein (z. B. `05:22 pm`) oder verwenden Sie ![Uhr](/help/assets/icons/Clock.svg).
   * **[!UICONTROL Monthly]**: Wählen Sie einen Tag des Monats aus dem Dropdown-Menü Ausführen für jedes Dropdown-Menü aus und geben Sie eine gültige Zeit ein (z. B. `05:22 pm`) oder verwenden Sie ![Uhr](/help/assets/icons/Clock.svg).

1. Wählen Sie eine **[!UICONTROL Training frequency]** aus dem Dropdown-Menü aus: **[!UICONTROL Monthly]**, **[!UICONTROL Quarterly]**, **[!UICONTROL Yearly]** oder **[!UICONTROL None]**.


### Trainings-Fenster

Wählen Sie im Abschnitt **[!UICONTROL Define training window]** zwischen:

![Modell - Trainings-Fenster definieren](/help/assets/model-define-training-window.png)

* **[!UICONTROL Have Mix Modeler select a helpful training window]** und

* **[!UICONTROL Manually input a training window]**. Wenn ausgewählt, definieren Sie die Anzahl der Jahre in **[!UICONTROL Include events the following years prior to a conversion]**.


### Berichtsfelder für granulare Insights

Der **[!UICONTROL Granular insights reporting fields]** Abschnitt verwendet die granulare Inkrementalitäts-Reporting-Funktion. Mit dieser Funktion können Sie harmonisierte Felder auswählen, um Konversions- und Touchpoint-Inkrementalitätswerte aufzuschlüsseln.

![Definieren von granularen Insights-Reporting-Feldern](/help/assets/granular-insights-reporting-fields.png)

Sie definieren diese harmonisierten Felder, damit Sie die Berichterstellung Ihres Modells mithilfe von granularen Berichtsspalten aufschlüsseln können, anstatt separate Modelle erstellen zu müssen.

Sie erstellen beispielsweise ein Modell, das auf Umsatz ausgerichtet ist, aber auch an Kampagnen, Medientypen, Regionen und der Leistung von Traffic-Quellen interessiert ist. Ohne die granulare Inkrementalitäts-Reporting-Funktion müssten Sie vier separate Modelle erstellen. Mit der Reporting-Funktion für granulare Inkrementalität können Sie Ihr Umsatzmodell auf Kampagnen, Medientypen, Regionen und Traffic-Quellen aufschlüsseln.

1. Wählen Sie ein oder mehrere harmonisierte Felder aus dem **[!UICONTROL _Harmonisierte Felder auswählen_]** unter **[!UICONTROL Includes]** aus. Die ausgewählten harmonisierten Felder werden dem Bedienfeld hinzugefügt.
1. Wählen Sie **[!UICONTROL *Harmonisiertes Feld *]**![CrossSize100](/help/assets/icons/CrossSize100.svg) aus, um ein harmonisiertes Feld aus dem Container mit den ausgewählten harmonisierten Feldern zu entfernen.
1. Wählen Sie **[!UICONTROL Clear all]** aus, um alle ausgewählten harmonisierten Felder zu entfernen.

Die ausgewählten harmonisierten Felder für die granulare Inkrementalitätsberichterstattung sind als Teil der aus der Bewertung des Modells resultierenden Experience Platform [Schema](/help/ingest-data/schemas.md) und [Datensatz](/help/ingest-data/datasets.md) verfügbar. Die granularen Insights-Berichtsfelder befinden sich in den **[!UICONTROL conversionPassthrough]**- und **[!UICONTROL touchpointPassthrough]**.

![Screenshot der Objekte conversionPassthrough und touchpointPassthrough in einem Schema für ein Modell, das für granulare Inkrementalitätsberichte aktiviert ist](/help/assets/schema-granular-insights-reporting.png)


## beenden

* Wählen Sie **[!UICONTROL Finish]** aus, um Ihre Modellkonfiguration abzuschließen.

   * Wählen Sie im Dialogfeld **[!UICONTROL Create instance?]** die Option **[!UICONTROL Ok]** aus, um den ersten Satz von Trainings- und Scoring-Durchgängen sofort mit dem Trigger zu versehen. Ihr Modell wird mit dem Status ![StatusOrange](/help/assets/icons/StatusOrange.svg) **[!UICONTROL Awaiting training]** aufgelistet.

     Wählen Sie zum Abbrechen **[!UICONTROL Cancel]** aus.

   * Wenn eine weitere Konfiguration erforderlich ist, wird in einem roten Umriss und Text erläutert, welche zusätzlichen Konfigurationen erforderlich sind.

* Wählen Sie **[!UICONTROL Back]** aus, um zum vorherigen Schritt zurückzukehren.

* Wählen Sie **[!UICONTROL Cancel]** aus, um die Modellkonfiguration abzubrechen.

