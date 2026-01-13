---
title: Modelleinblicke
description: Erfahren Sie, wie Sie Details zu Ihrem Modell abrufen, z. B. einen Überblick über den Verlauf, Modelleinblicke und Modellqualität in Mix Modeler.
feature: Models
exl-id: d99852f9-ba0d-4a2e-b5f3-ca0efe6002fd
source-git-commit: 2775c5a3779f6731f7f3143f6ed21db2993c0955
workflow-type: tm+mt
source-wordcount: '2499'
ht-degree: 2%

---

# Modelleinblicke

Jede Visualisierung in Model Insights soll Ihnen bei Folgendem helfen:

* Visualisieren und Quantifizieren der Wirkung der Marketing-Aktivitäten Ihres Unternehmens.
* Ermitteln Sie, welche Kanäle leistungsstark sind.
* Ermitteln Sie, welche Kanäle möglicherweise optimiert werden müssen.

Diese Einblicke helfen Ihnen dann, die Priorisierung und Zuordnung von Ressourcen zu unterstützen.

Um Modelleinblicke anzuzeigen, gehen Sie in der ![&#x200B; &#x200B;](/help/assets/icons/FileData.svg)Modelle **[!UICONTROL Models]** in Mix Modeler folgendermaßen vor:

1. Wählen Sie in der **[!UICONTROL Models]**-Tabelle den Namen eines Modells aus, das die **[!UICONTROL Last run status]** &quot;![&quot; &#x200B;](/help/assets/icons/StatusGreen.svg) **[!UICONTROL Success]**.

1. Wählen Sie im Kontextmenü **[!UICONTROL Model Insights]** aus.



Die folgenden Registerkarten sind verfügbar:

* [Modelleinblicke](#model-insights)
* [Kanalsynergie](#channel-synergy)
* [Faktoren](#factors-beta) [!BADGE Beta]
* [Attribution](#attribution) (nur für MTA-aktivierte Modelle)
* [Diagnose](#diagnostics)
* [Historischer Überblick](#historical-overview).

Sie können den Zeitraum ändern, auf dem die Visualisierungen auf den einzelnen Registerkarten basieren. Geben Sie einen Datumsbereich ein oder wählen Sie ![Kalender](/help/assets/icons/Calendar.svg), um einen Datumsbereich auszuwählen.

## Modellabweichung

{{release-limited-testing-section}}

Wenn Modellabweichungen auf dem Modell erkannt werden, wird ein **[!UICONTROL Model drift detected]** Dialogfeld mit Optionen angezeigt, die später erinnert werden sollen oder das Modell sofort [**[!UICONTROL Retrain]**](overview.md#retrain). Wenn Sie **[!UICONTROL Remind me later]** auswählen, werden Sie am nächsten Tag oder bei der nächsten Anmeldung daran erinnert.

![Dialogfeld „Modelldrift erkannt“](/help/assets/model-drift-dialog.png)

## [!UICONTROL Model insights]

Die Registerkarte Modelleinblicke zeigt Visualisierungen für [Beitrag nach Datum und Basismedien](#contribution-by-date-and-base-media), [Beitrag nach Kanal](#contribution-by-channel), [Marketing-](#marketing-performance-summary) und [marginale Antwortkurven](#marginal-response-curves). Die Registerkarte enthält auch eine [Touchpoint-Aufschlüsselung](#touchppint-breakdown)-Tabelle.

![Modell - Modelleinblicke](/help/assets/model-insights-insights.png)

* Sie können den Mauszeiger über einzelne Diagrammelemente in jeder Visualisierung bewegen, um ein Pop-up mit weiteren Details anzuzeigen.

* Um eine CSV-Datei mit den Daten für die Visualisierung herunterzuladen, wählen Sie ![Herunterladen](/help/assets/icons/Download.svg) aus.

* Um Daten zu vollständigen Modelleinblicken im Microsoft® Excel-Format herunterzuladen, wählen Sie ![Herunterladen](/help/assets/icons/Download.svg) **[!UICONTROL Download data]** aus.


### Beitrag nach Datum und Basismedien

Diese gestapelte Diagrammvisualisierung ist wie folgt angeordnet:

* Die Basis wird unten angezeigt.
* Nicht ausgegebene Kanäle werden in der Mitte angezeigt.
* Die Ausgabenkanäle werden oben angezeigt.

Diese Visualisierung stellt den Beitragsanteil dar, der von der Basis, von Ausgabenkanälen und von nicht ausgegebenen Kanälen über einen Datumsbereich erreicht wird. Diese Visualisierung ist hilfreich, um die Inkrementalität zu präsentieren. Die Basis stellt dar, was ohne Marketing überhaupt passiert wäre, und die Nicht-Ausgabenkanäle plus Ausgabenkanäle (zusätzlich zur Basis) weisen auf die Wirkung Ihres Marketing hin. Kurz gesagt, die Nicht-Ausgaben plus Ausgaben entsprechen der inkrementellen Wirkung Ihrer Marketing-Maßnahmen, und die Visualisierung bietet eine einfache insight in den Wert, den das Marketing generiert.

### Beitrag nach Kanal

Eine Ringvisualisierung, die eine Verteilung des Beitrags nach verschiedenen Kanälen anzeigt. Diese Visualisierung zeigt die Inkrementalität durch die Linse der drei leistungsstärksten Kanäle (ohne Basis- und *Alle anderen* Kategorien). Die Visualisierung hilft bei der Priorisierung und Budgetzuweisung.

### Marketing-Leistungszusammenfassung

Eine horizontale Balkendiagrammvisualisierung, die den ROI oder die CPA-Leistung für jeden Kanal anzeigt. Diese Visualisierung zeigt den ROI/CPA Ihrer Marketing-Investitionen. Die Kanäle werden in absteigender Reihenfolge auf der Basis von ROI/CPA sortiert. Anhand der Visualisierung können Sie erkennen, welche Kanäle am effektivsten sind und möglicherweise optimiert werden müssen.

### Kurven der marginalen Reaktion

Das Liniendiagramm visualisiert und vergleicht die Grenzerträge, die durch die Investition in Ihre Marketing-Kanäle generiert werden.  und identifiziert den aktuellen Ausgabenpunkt und den marginalen Break-even-Punkt (bei dem Ihre inkrementelle Rendite geringer ist als Ihre inkrementellen Ausgaben). Auf diese Weise erfahren Sie, wann Ihre Marketing-Investition an Effektivität verliert.

Die Kurve, der aktuelle Ausgabepunkt, der marginale Break-even-Punkt und die entsprechenden Werte werden auf Grundlage des ausgewählten Datenbereichs und des von Ihnen ausgewählten Kanals berechnet.

So ändern Sie den Kanal:

* Wählen Sie einen Kanal aus dem Dropdown-Menü **[!UICONTROL Channel]** aus, um die Visualisierung für einen bestimmten Kanal zu aktualisieren.


### Touchpoint-Aufschlüsselung

Die Tabelle Touchpoint-Aufschlüsselung zeigt die wöchentlichen Touchpoint-Aufschlüsselungen für alle oder ausgewählte Kanäle auf wöchentlicher Basis und mit den jeweiligen Schlüsselmetriken an. Die Tabelle ermöglicht einen einfachen Vergleich, die Identifizierung von Trends und die Verfolgung der Leistung auf einer detaillierteren Kanalebene. Diese Tabelle ergänzt explizit die Visualisierung [Beitrag nach Datum und Basismedien](#contribution-by-date-and-base-media) und die Visualisierung [Beitrag nach Kanal](#contribution-by-channel).

![Touchpoint-Aufschlüsselung](../assets/touchpoint-breakdown.png)

Die folgenden Spalten sind verfügbar:

| Spalte | Beschreibung |
|---|---|
| **[!UICONTROL Date range]** | Die Woche, über die berichtet wird. |
| **[!UICONTROL Touchpoint]** | Der spezifische Touchpoint-Kanal. |
| **[!UICONTROL ROI]** | Der Prozentsatz von (**[!UICONTROL Revenue]** - **[!UICONTROL Spend]**) / **[!UICONTROL Spend]**. |
| **[!UICONTROL Revenue]** | Der Umsatz für den Datumsbereich. |
| **[!UICONTROL CPA]** | **[!UICONTROL Spend]**/**[!UICONTROL Conversions]**. |
| **[!UICONTROL Conversions]** | Die Konversionen für den Datumsbereich. |
| **[!UICONTROL Spend]** | Die Ausgaben für den Datenbereich. |

Um einen bestimmten Kanal oder alle Kanäle auszuwählen, wählen Sie aus dem Dropdown-Menü **[!UICONTROL View]** .

Um den Inhalt der Touchpoint-Aufschlüsselungstabelle herunterzuladen, wählen Sie ![Herunterladen](/help/assets/icons/Download.svg) **[!UICONTROL Download CSV]**.


## Kanalsynergie

Auf der Registerkarte **[!UICONTROL Channel synergy]** hilft Ihnen die **[!UICONTROL Channel synergies]** Visualisierung, zu erkennen, wie Marketing-Kanäle interagieren, um über ihre individuellen Beiträge hinaus multiplikative Effekte zu erzeugen.

Die Heatmap-Matrix bietet eine visuelle Darstellung der Synergiewerte zwischen Paaren von Ausgabenkanälen. Diese Matrix hilft Marketing-Fachleuten zu verstehen, wie Kanäle interagieren, um die Leistung zu steigern. Für jedes Modell werden die Synergiewerte von 0 auf 10 normiert. Diese Werte quantifizieren die *nächste Dollar-Synergie* die schätzt, wie effektiv zwei Kanäle zusammenarbeiten, wenn jeder von ihnen einen zusätzlichen Dollar an Ausgaben auf dem aktuellen Niveau erhält.

Dieser Next-Dollar-Rahmen bietet ein realistisches Maß für die relative Synergiestärke, da der Rahmen die tatsächlichen Ausgabenbedingungen in den Trainingsdaten berücksichtigt und so fundiertere Optimierungsentscheidungen ermöglicht.

![Planen von Kanalsynergien](/help/assets/model-channel-synergies.png)

Um eine CSV-Datei herunterzuladen, die die Matrix darstellt, wählen Sie ![Herunterladen](/help/assets/icons/Download.svg) **[!UICONTROL Download]**.

>[!NOTE]
>
>Wenn die Registerkarte **[!UICONTROL Channel synergy]** für ein vorhandenes Modell nicht sichtbar ist, müssen Sie das Modell neu trainieren, um die Funktionalität und Visualisierung zu aktivieren.



## **[!UICONTROL Factors]** [!BADGE Beta]

Die Registerkarte [!BADGE Beta] zeigt Einblicke zu externen Faktoren.

![Faktoren](/help/assets/factors.png)

Diese Visualisierung hilft Ihnen, den inkrementellen Effekt zu verstehen, den verschiedene interne und externe Faktoren auf die Baseline der Konversionen haben. Zum Beispiel wirtschaftliche Bedingungen oder Werbemaßnahmen.

Wählen Sie im Dropdown-Menü **[!UICONTROL Factors]** aus, welche Faktoren angezeigt werden sollen.

<!-- need to update the image when we do have a proper example -->

Um eine CSV-Datei mit den Daten für die Tabelle herunterzuladen, wählen Sie ![Herunterladen](/help/assets/icons/Download.svg) aus.

Wenn keine Daten verfügbar sind, wird die Meldung ![TableAndChart](/help/assets/icons/TableAndChart.svg) **[!UICONTROL No data is available, you may need to retrain your model, or change the date range to view insights]**.

## [!UICONTROL Attribution]

>[!NOTE]
>
>Die Registerkarte „Attribution“ ist nur für MTA-aktivierte Modelle verfügbar.


Auf der Registerkarte [!UICONTROL Attribution] können Sie die Effektivität von Touchpoints und Marketing-Kampagnen mit Daten auf Ereignisebene verstehen.  Siehe [Modell erstellen](build.md).

Die folgenden Attributionsmodelle werden unterstützt:

* Basierend auf dem ausgewählten Modell in Mix Modeler:
   * Algorithmisch - beeinflusst
   * Algorithmisch - inkrementell
* Regelbasiert:
   * Ausklangseinheiten
   * First Touch
   * Letztkontakt
   * Linear
   * U-Form

Eine Einführung in [&#x200B; Funktion der Multi-Touch](../get-started/about.md#multi-touch-attribution)Attribution in Mix Modeler finden Sie unter „Multi-Touch-Attribution“.

Wählen Sie ein oder mehrere Attributionsmodelle aus dem Dropdown-Menü **[!UICONTROL Attribution Model]** aus. Die ausgewählten Attributionsmodelle gelten für alle Visualisierungen auf der Registerkarte Attribution .

![Attribution](/help/assets/model-insights-attribution.png)

Die granularen Ereignis-Scores der Mix Modeler-Multi-Touch-Attribution entsprechen den Mix Modeler-Gesamtergebnissen und -ROIs. Diese Bewertungen werden auch als Datensätze in Experience Platform zur Verfügung gestellt.

Die Registerkarte Attribution besteht aus den folgenden Visualisierungen:

### [!UICONTROL Overview]

In der [!UICONTROL Overview] Visualisierung werden für die ausgewählten Attributionsmodelle die Konversionssummen und -prozentsätze angezeigt. Wenn Sie weitere Modelle auswählen, werden der Visualisierung zusätzliche Kreise hinzugefügt, von denen jede eine eigene Farbe hat, die der Legende entspricht.

Um ein Popup mit Details für ein Attributionsmodell anzuzeigen, bewegen Sie den Mauszeiger über einen beliebigen Kreis in der Visualisierung.

### [!UICONTROL Trends]

Die [!UICONTROL Daily trends]-, [!UICONTROL Weekly trends]- oder [!UICONTROL Monthly trends]-Visualisierung zeigt für die ausgewählten Attributionsmodelle die täglichen, wöchentlichen oder monatlichen Konversionstrends.

Um den Zeitraum auszuwählen, wählen Sie **[!UICONTROL Daily trends]**, **[!UICONTROL Weekly trends]** oder **[!UICONTROL Monthly trends]** aus ![Mehr](/help/assets/icons/More.svg).

Um Details anzuzeigen, bewegen Sie den Mauszeiger über die Datenzeile eines bestimmten Attributionsmodells, um ein Pop-up anzuzeigen, das die Gesamtzahl der Konversionen für diese Daten anzeigt.

### [!UICONTROL Breakdown]

Die [!UICONTROL Breakdown] Visualisierung ist eine Aufschlüsselung der Konversionen für jedes der ausgewählten Attributionsmodelle nach Kanal oder Touchpoint. Diese Visualisierung kann hilfreich sein, um Entscheidungen über die Effektivität der einzelnen Kanäle oder Touchpoints zu treffen.

Um den Aufschlüsselungstyp auszuwählen, wählen Sie **[!UICONTROL Breakdown by channel]** oder **[!UICONTROL Breakdown by touchpoint]** aus ![Mehr](/help/assets/icons/More.svg).

Um Details anzuzeigen, bewegen Sie den Mauszeiger über eines der Diagrammelemente.

### [!UICONTROL Top campaigns]

Die Visualisierung der Top-Kampagnen zeigt eine Tabelle der Top-Kampagnen mit Spalten für Kampagnenname, Kanal, Medientyp und inkrementelle Konversionen. Diese Visualisierung kann dabei helfen, Ihr Team über die Effektivität einer bestimmten Kampagne für einen bestimmten Kanal zu informieren und Einblicke darüber zu erhalten, in welche Kampagnen Sie weiter investieren sollten.

Um die Tabelle nach Kanal, Medientyp oder inkrementellen Konversionen in auf- ↑ absteigender Reihenfolge ↓ sortieren, wählen Sie die Spaltenüberschrift aus und schalten Sie die Sortierung um.

Um die Tabelle in einem separaten Dialogfeld zu erweitern, wählen Sie **[!UICONTROL Expand]** aus ![Mehr](/help/assets/icons/More.svg).

Das erweiterte Dialogfeld Top-Kampagnen zeigt dieselbe Tabelle mit zusätzlichen Spalten für

* Inkrementelle Konversionen
* Beeinflusste Konversionen
* First-Touch-Konversionen
* Last Touch-Konversionen

  Sie können jede der zusätzlichen Spaltenüberschriften auswählen, um die Tabelle in auf- oder absteigender Reihenfolge zu sortieren.

Um das erweiterte Dialogfeld Top-Kampagnen zu schließen, wählen Sie **[!UICONTROL Close]** aus.


### [!UICONTROL Breakdown by touchpoint position]

Die [!UICONTROL Breakdown by touchpoint position] Visualisierung ist eine Aufschlüsselung der zugewiesenen Konversionen nach Position des Touchpoints und Touchpoints auf allen Konversionspfaden. Dieses Diagramm hilft Ihnen zu vergleichen, ob ein Touchpoint an einer Position besser beiträgt als verbleibende Positionen und andere Touchpoints an einer beliebigen Position.

>[!NOTE]
>
>Die Summe des prozentualen Beitrags für ein Attributionsmodell über alle Touchpoints und Positionen hinweg sollte 100 betragen.


Die Positionen [!UICONTROL Starter], [!UICONTROL Player] und [!UICONTROL Closer] sind wie folgt definiert:

| Position | Beschreibung |
|---|---|
| [!UICONTROL Starter] | Diese Position gibt an, ob der Touchpoint der erste Touchpoint in einem Konversionspfad ist. |
| [!UICONTROL Player] | Diese Position gibt an, ob der Touchpoint nicht der erste oder der letzte Touch ist, der zur Konversion führt. |
| [!UICONTROL Closer] | Diese Position gibt an, ob der Touchpoint der letzte Berührungspunkt vor der Konversion ist. |


### [!UICONTROL Top conversion paths]

Die [!UICONTROL Top conversion paths] Visualisierung zeigt die fünf wichtigsten Konversionspfade basierend auf den ausgewählten Attributionsmodellen.

Für jeden Konvertierungspfad wird Folgendes angezeigt:

* die Anzahl der Kanäle, die eine Auswirkung haben,
* die insgesamt zugewiesenen Pfade,
* Der Prozentsatz der zugewiesenen Pfade für diesen Konversionspfad im Vergleich zur Gesamtzahl der zugewiesenen Pfade,
* für jeden Kanal den Prozentsatz des Beitrags zum Attributionsmodell und
* Die Summe dieser Prozentsätze des Kanalzuordnungsmodells.


## [!UICONTROL Diagnostics] {#diagnostics}


>[!CONTEXTUALHELP]
>id="models_diagnostics_modelassessment"
>title="Diagramme zur Modellbewertung"
>abstract="Visualisierungen der Modellbewertung schlüsseln tatsächliche und prognostizierte oder Restkonversionen auf."
>additional-url="https://experienceleague.adobe.com/de/docs/mix-modeler/using/overview" text="Überblick über Mix Modeler"
>additional-url="https://video.tv.adobe.com/v/3440803/?captions=ger&learn=on&enablevpops" text="Demo von Mix Modeler"


>[!CONTEXTUALHELP]
>id="models_diagnostics_pathstouched"
>title="Pfade mit Touchpoints"
>abstract="„Pfade mit Touchpoints“ ist der Prozentsatz der Pfade, die eine Konversion erzielen, und der Prozentsatz der Pfade, die keine Konversion erzielen, für jeden Touchpoint."


>[!CONTEXTUALHELP]
>id="models_diagnostics_modeldateinfo"
>title="Modelldatum „Ab“"
>abstract="Die Daten für diese Tabelle werden nur für bestimmte Zeiträume generiert.  Das **[!UICONTROL As of]** Datum gibt an, wann die Daten generiert wurden, und basiert auf Daten vom startDate bis endDate."


Auf der Registerkarte **[!UICONTROL Diagnostics]** werden Visualisierungen für Folgendes angezeigt:

* **[!UICONTROL Model Assessment]** Visualisierungen, die aus Folgendem bestehen:

  ![Modellbewertung](../assets/model-assessment.png)

   * Ein Diagramm, das Sie nach tatsächlichen Konversionen im Vergleich zu prognostizierten Konversionen oder Restkonversionen aufschlüsseln können.
Um die Visualisierung aufzuschlüsseln, wählen Sie eine der folgenden Optionen aus der **[!UICONTROL Breakdown]**.

      * **[!UICONTROL Actual vs Predicted]**: Diese Option vergleicht reale Werte mit Modellvorhersagen. Idealerweise sollten die prognostizierten Werte eng mit den tatsächlichen Werten übereinstimmen, obwohl eine gewisse Abweichung erwartet wird. Große oder systematische Abweichungen oder Muster können auf fehlende Beziehungen und Daten oder potenzielle Verzerrungen hinweisen.

      * **[!UICONTROL Residuals]**: Diese Option zeigt den Unterschied zwischen tatsächlichen und prognostizierten Werten an. Ein gut funktionierendes Modell hat zufällig verteilte Residuen ohne klare Muster oder zunehmende Ausbreitung. Strukturierte Trends oder sich ausweitende Residuen können auf fehlende Beziehungen und Daten oder Varianzprobleme hinweisen.

   * Eine Tabelle mit den folgenden Spalten für jede Konversionsmetrik:

      * **[!UICONTROL Actual Conversion]**
      * **[!UICONTROL Predicted Conversion]**
      * **[!UICONTROL Residual Conversion]**
      * **[!UICONTROL R<sup>2</sup>]**, ein Score, der angibt, wie gut die Daten zum Regressionsmodell passen (die Güte der Anpassung).
      * **[!UICONTROL MAPE]** (Mittelwert des absoluten Prozentfehlers), der einer der am häufigsten verwendeten KPIs zur Messung der Prognosegenauigkeit ist und den Prognosefehler als Prozentsatz des tatsächlichen Werts ausdrückt.
      * **[!UICONTROL RMSE]** (quadratischer Mittelwert des Fehlers): Gibt den durchschnittlichen Fehler an, gewichtet nach dem Quadrat des Fehlers.

  Um eine CSV-Datei mit den Daten für die Tabelle herunterzuladen, wählen Sie ![Herunterladen](/help/assets/icons/Download.svg) aus.

* **[!UICONTROL Model training fit metrics]** Tabelle, die für jede Konversionsmetrik angezeigt wird:

  ![Tabelle mit Modelltrainings-Fit-Metriken](../assets/model-training-fit-metrics.png)

   * **[!UICONTROL Training R<sup>2</sup>]**: Gibt den Anteil der Varianz in den tatsächlichen Werten an, der durch die Prognosen des Modells erklärt wird und von 0 bis 1 reicht.
   * **[!UICONTROL Training sMAPE]** (symmetrischer Mittelwert absoluter Prozentfehler): Misst den durchschnittlichen Prozentfehler bei Trainings-Daten. Niedrigere Werte bedeuten eine bessere Genauigkeit.
   * **[!UICONTROL Training RMSE]** (Root Mean Squared Error): Misst den durchschnittlichen prozentualen Fehler auf Trainings-Daten. Bestraft größere Fehler stärker als MAPE. Ein niedrigerer RMSE-Wert legt eine bessere Prognosegenauigkeit nahe, ist aber anfällig für Ausreißer.
   * **[!UICONTROL Out-of-sample sMAPE]**: Evaluiert den prozentualen Fehler bei nicht angezeigten Daten und gleicht Über- und Unterprognosen aus. Hilft bei der Bewertung der Generalisierung. Derzeit bewertet Mix Modeler den prozentualen Fehler anhand des letzten Quartals der Schulungsdaten als Holdout-Satz.
   * **[!UICONTROL Out-of-sample RMSE]**: Evaluiert den prozentualen Fehler bei nicht angezeigten Daten und gleicht Über- und Unterprognosen aus. Hilft bei der Bewertung der Generalisierung. Derzeit bewertet Mix Modeler den prozentualen Fehler anhand des letzten Quartals der Schulungsdaten als Holdout-Satz. RMSE bestraft größere Fehler stärker als MAPE.


* **[!UICONTROL Touchpoint effectiveness]** Tabelle, die das Ergebnis des algorithmischen Attributions-KI-Modells darstellt.

  ![Touchpoint-Effektivitätstabelle](../assets/touchpoint-effectiveness.png)

  Die Daten für diese Tabelle werden nur für bestimmte Zeiträume generiert. Wählen Sie **[!UICONTROL As of *xx/xx/xx, xx:xx TZ *]**![Info](/help/assets/icons/InfoOutline.svg) aus, um weitere Details anzuzeigen.

  Die Visualisierung zeigt für jeden Touchpoint in absteigender [!UICONTROL Efficiency measure] ![absteigender &#x200B;](/help/assets/icons/SortOrderDown.svg)):

   * **[!UICONTROL Paths touched]**: Visualisiert den Prozentsatz der Pfade mit Konversion und den Prozentsatz der Pfade ohne Konversion. Bei einem Touchpoint werden mehr zugewiesene Konversionen angezeigt, wenn das Attributionskonversionsverhältnis hoch ist. Dieses Verhältnis vergleicht den Prozentsatz der Pfade, die zu einer Konversion führen, mit dem Prozentsatz der Pfade, die *nicht* zu einer Konversion führen.
   * **[!UICONTROL Efficiency measure]**: Generiert vom algorithmischen Attributionsmodell, zeigt das Effizienzmaß die relative Bedeutung eines Touchpoints für die Konversion an, unabhängig vom Touchpoint-Volumen. Der Wirkungsgrad wird auf einer Skala von 1 bis 5 gemessen. Beachten Sie, dass ein höheres Touchpoint-Volumen keine höhere Effizienz garantiert.
   * **[!UICONTROL Total volume]**: Die Gesamtzahl der Berührungen eines Touchpoints durch eine Benutzerin oder einen Benutzer. Die Anzahl umfasst Touchpoints, die auf einem Pfad angezeigt werden, der eine Konversion erreicht, sowie Pfade, die *Konversion*.


### Modelldrifterkennung

>[!AVAILABILITY]
>
>Die in diesem Abschnitt beschriebene Funktion befindet sich in der eingeschränkten Testphase der Version und ist möglicherweise noch nicht in Ihrer Umgebung verfügbar. Dieser Hinweis wird entfernt, wenn die Funktion allgemein verfügbar ist. Informationen zum Mix Modeler-Veröffentlichungsprozess finden Sie unter [Mix Modeler-Funktionsversionen](/help/releases/latest.md).
>

Wenn eine Modellabweichung erkannt wird, wird oben eine **[!UICONTROL Model drift detected]**-Benachrichtigung angezeigt.

![Modell-Drift-Benachrichtigung](/help/assets/model-drift-notification.png)

Wählen Sie **[!UICONTROL Hide]** aus, um die Benachrichtigung auszublenden. Die Benachrichtigung wird am nächsten Tag oder bei der nächsten Anmeldung erneut angezeigt.


## [!UICONTROL Historical overview]

Die Registerkarte Historische Übersicht zeigt Visualisierungen für:

![Modell - Historischer Überblick](/help/assets/model-insights-historical-overview.png)


### Konversion und Ausgaben nach Geschäftsquartal und Produkt

Diese Visualisierung stellt die Konversions- und Ausgabenverteilung über verschiedene Quartale innerhalb des angegebenen Datumsbereichs dar. Die Visualisierung hilft bei der Identifizierung von Quartalen mit hoher Performance, in denen die Ausgaben die Konversionen fördern.


### Ausgaben nach Kanal

Diese Visualisierung stellt die Verteilung der Ausgaben über verschiedene Kanäle innerhalb des angegebenen Datumsbereichs dar. Die Visualisierung ermöglicht eine schnelle Identifizierung der Kanäle, die die meisten Ausgaben erhalten.


### Touchpoint-Ausgaben

Diese Visualisierung stellt die Verteilung der Ausgaben auf die bezahlten Touchpoints für jedes Quartal innerhalb des angegebenen Datumsbereichs dar. Die Visualisierung ermöglicht das Verständnis, welche Touchpoints innerhalb bestimmter Kanäle und Quartale priorisiert werden. Die Visualisierung hilft, Ausgabenmuster und -trends des Kanals zu identifizieren, insbesondere Kanäle mit niedrigen und unregelmäßigen Ausgaben im Laufe der Zeit.

So können Sie einen alternativen ausgabebasierten Kanal auswählen, der für diese Visualisierung angezeigt werden soll:

* Wählen Sie einen Kanal aus **[!UICONTROL Channels]**.


### Anzahl der Touchpoints

Diese Visualisierung stellt die Volumenverteilung auf alle Touchpoints für jedes Quartal innerhalb des angegebenen Datumsbereichs dar.

So können Sie einen alternativen volumenbasierten Kanal auswählen, der für diese Visualisierung angezeigt werden soll:

* Wählen Sie einen Kanal aus **[!UICONTROL Channels]**.


## **[!UICONTROL Edit]**

Sie können den Namen, die Beschreibung und den Zeitplan für das Training und die Bewertung des Modells bearbeiten.

1. Wählen Sie ![Bearbeiten](/help/assets/icons/Edit.svg) Bearbeiten aus

1. Im Dialogfeld **[!UICONTROL Edit model]** :

   * Geben Sie einen neuen **[!UICONTROL Name]** und eine neue **[!UICONTROL Description]** ein.

   * Um die Zeitplanung zu aktivieren, aktivieren Sie **[!UICONTROL Status]**. Sie können die Planung nur für Modelle aktivieren, die trainiert und bewertet wurden.

      1. **[!UICONTROL Scoring frequency]** auswählen:

         * **[!UICONTROL Daily]**: Geben Sie eine gültige Zeit ein (z. B. `05:22 pm`) oder verwenden Sie ![Uhr](/help/assets/icons/Clock.svg).
         * **[!UICONTROL Weekly]**: Wählen Sie einen Wochentag aus und geben Sie eine gültige Zeit ein (z. B. `05:22 pm`) oder verwenden Sie ![Uhr](/help/assets/icons/Clock.svg).
         * **[!UICONTROL Monthly]**: Wählen Sie einen Tag des Monats aus dem Dropdown-Menü Ausführen für jedes Dropdown-Menü aus und geben Sie eine gültige Zeit ein (z. B. `05:22 pm`) oder verwenden Sie ![Uhr](/help/assets/icons/Clock.svg).

      1. Wählen Sie eine **[!UICONTROL Training frequency]** aus dem Dropdown-Menü aus: **[!UICONTROL Monthly]**, **[!UICONTROL Quarterly]**, **[!UICONTROL Yearly]** oder **[!UICONTROL None]**.

     ![Modell bearbeiten](../assets/model-edit.png)

1. Wählen Sie **[!UICONTROL Save]** aus.
