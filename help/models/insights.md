---
title: Modelleinblicke
description: Erfahren Sie, wie Sie Details zu Ihrem Modell erhalten, z. B. einen Überblick über den Verlauf, Modelleinblicke und Modellqualität im Mix Modeler.
feature: Models
exl-id: d99852f9-ba0d-4a2e-b5f3-ca0efe6002fd
source-git-commit: 25eb18443d0bdecdb02c026aec363271618441f5
workflow-type: tm+mt
source-wordcount: '1552'
ht-degree: 0%

---

# Modelleinblicke

Um Modelleinblicke anzuzeigen, gehen Sie in der Benutzeroberfläche ![Modelle](/help/assets/icons/FileData.svg) von **[!UICONTROL Models]** in Mix Modeler folgendermaßen vor:

1. Wählen Sie in der Tabelle **[!UICONTROL Models]** den Namen eines Modells mit der **[!UICONTROL Last run status]** <span style="color:green">● aus</span> **[!UICONTROL Success]**.

1. Wählen Sie im Kontextmenü **[!UICONTROL Model Insights]** aus.

![Registerkarte „Modelleinblicke“](/help/assets/model-insights-tabbar.png)

Sie sehen, wann das angegebene Modell zuletzt aktualisiert wurde, und Visualisierungen werden über vier Registerkarten angezeigt: [Modelleinblicke](#model-insights), [Attribution](#attribution), [Faktoren](#factors), [Diagnose](#diagnostics) und [Historischer Überblick](#historical-overview).

Sie können den Zeitraum ändern, auf dem die Visualisierungen auf den einzelnen Registerkarten basieren. Geben Sie einen Datumsbereich ein oder wählen Sie ![Kalender](/help/assets/icons/Calendar.svg), um einen Datumsbereich auszuwählen.

## [!UICONTROL Model insights]

Die Registerkarte Modelleinblicke zeigt Visualisierungen für [Beitrag nach Datum und Basismedien](#contribution-by-date-and-base-media), [Beitrag nach Kanal](#contribution-by-channel), [Marketing-](#marketing-performance-summary) und [marginale Antwortkurven](#marginal-response-curves). Die Registerkarte enthält auch eine [Touchpoint-Aufschlüsselung](#touchppint-breakdown)-Tabelle.

![Modell - Modelleinblicke](/help/assets/model-insights-insights.png)

* Sie können den Mauszeiger über einzelne Diagrammelemente in jeder Visualisierung bewegen, um ein Pop-up mit weiteren Details anzuzeigen.

* Um eine CSV-Datei mit den Daten für die Visualisierung herunterzuladen, wählen Sie ![Herunterladen](/help/assets/icons/Download.svg) aus.

* Um Daten zu vollständigen Modelleinblicken im Microsoft® Excel-Format herunterzuladen, wählen Sie ![Herunterladen](/help/assets/icons/Download.svg) **[!UICONTROL Download data]** aus.


### Beitrag nach Datum und Basismedien.

Das gestapelte Diagramm ist sortiert: unten als Basis, in der Mitte als Nicht-Ausgabekanäle und oben als Ausgabenkanäle.

### Beitrag nach Kanal

Die Ringdiagramm-Visualisierung zeigt eine Verteilung des Beitrags nach Kanal.

### Marketing-Leistungszusammenfassung.

Ein horizontales Balkendiagramm, das die ROI-Leistung nach Kanal anzeigt.

### Kurven der marginalen Reaktion.

Das Liniendiagramm visualisiert und vergleicht die Grenzerträge, die durch die Investition in Ihre Marketing-Kanäle generiert werden.  Und identifiziert den Break-even-Punkt, an dem Ihre inkrementelle Rendite geringer ist als Ihre inkrementellen Ausgaben. Auf diese Weise erfahren Sie, wann Ihre Marketing-Investition an Effektivität verliert.

Die Kurve, der Breakeven-Punkt und die entsprechenden Werte werden basierend auf dem ausgewählten Datenbereich und dem ausgewählten Kanal berechnet.

So ändern Sie den Kanal:

* Wählen Sie einen Kanal aus dem Dropdown-Menü **[!UICONTROL Channel]** aus, um die Visualisierung für einen bestimmten Kanal zu aktualisieren.


### Touchpoint-Aufschlüsselung

Die Tabelle Touchpoint-Aufschlüsselung zeigt die Touchpoint-Aufschlüsselungen für alle oder ausgewählte Kanäle auf wöchentlicher Basis an.

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


## [!UICONTROL Attribution]

>[!NOTE]
>
>Die Registerkarte „Attribution“ ist nur für MTA-aktivierte Modelle verfügbar.


Auf der Registerkarte [!UICONTROL Attribution] können Sie die Effektivität von Touchpoints und Marketing-Kampagnen mit Daten auf Ereignisebene verstehen.  Siehe [Modell erstellen](build.md).

Die folgenden Attributionsmodelle werden unterstützt:

* Basierend auf dem im Mix Modeler ausgewählten Modell:
   * Algorithmisch - beeinflusst
   * Algorithmisch - inkrementell
* Regelbasiert:
   * Ausklangseinheiten
   * First Touch
   * Letztkontakt
   * Linear
   * U-Form

Eine Einführung in [ Multi-Touch](../get-started/about.md#multi-touch-attribution)Attributionsfunktion in Mix Modeler finden Sie unter „Multi-Touch-Attribution“.

Wählen Sie ein oder mehrere Attributionsmodelle aus dem Dropdown-Menü **[!UICONTROL Attribution Model]** aus. Die ausgewählten Attributionsmodelle gelten für alle Visualisierungen auf der Registerkarte Attribution .

![Attribution](/help/assets/model-insights-attribution.png)

Die granularen Ereignis-Scores der Multi-Touch-Attribution für Mix Modeler entsprechen den allgemeinen Mix Modeler-Scores und ROIs. Diese Bewertungen werden auch als Datensätze im Experience Platform zur Verfügung gestellt.

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

## **[!UICONTROL Factors]** [!BADGE Beta]

Die Registerkarte [!BADGE Beta] zeigt Einblicke zu externen Faktoren.

![Faktoren](/help/assets/factors.png)

Diese Visualisierung hilft Ihnen, den inkrementellen Effekt zu verstehen, den verschiedene interne und externe Faktoren auf die Baseline der Konversionen haben. Zum Beispiel wirtschaftliche Bedingungen oder Werbemaßnahmen.

Wählen Sie im Dropdown-Menü **[!UICONTROL Factors]** aus, welche Faktoren angezeigt werden sollen.

<!-- need to update the image when we do have a proper example -->

Um eine CSV-Datei mit den Daten für die Tabelle herunterzuladen, wählen Sie ![Herunterladen](/help/assets/icons/Download.svg) aus.

Wenn keine Daten verfügbar sind, wird die Meldung ![TableAndChart](/help/assets/icons/TableAndChart.svg) **[!UICONTROL No data is available, you may need to retrain your model, or change the date range to view insights]**.

## [!UICONTROL Diagnostics]

Die Registerkarte Diagnose zeigt Visualisierungen für:

* [!UICONTROL Model Assessment] Visualisierung, die Sie nach tatsächlichen Konversionen im Vergleich zu prognostizierten Konversionen oder Restkonversionen aufschlüsseln können.

Um die Visualisierung aufzuschlüsseln, wählen Sie **[!UICONTROL Actual vs. Predicted]** oder **[!UICONTROL Residuals]** aus der **[!UICONTROL Breakdown]** aus.

* [!UICONTROL Model fitting metrics] Tabelle mit den folgenden Spalten für jede Konversionsmetrik:

   * Tatsächliche Konversion

   * Modellierte Konversion

   * Restkonvertierung (Unterschied zwischen tatsächlicher und modellierter Konversion)

   * Werte der Modellqualitätsbewertung:

      * R2 (R-Quadrat), das angibt, wie gut die Daten zum Regressionsmodell passen (die Anpassungsgüte).

      * MAPE (Mean Absolute Percentage Error, mittlerer absoluter Prozentfehler) ist einer der am häufigsten verwendeten KPIs zur Messung der Prognosegenauigkeit, der den Prognosefehler als Prozentsatz des tatsächlichen Werts ausdrückt.

      * RMSE (Root Mean Square Error, quadratischer Mittelwert der Fehlerquote): Gibt den durchschnittlichen Fehler an, gewichtet nach dem Quadrat des Fehlers.

Um eine CSV-Datei mit den Daten für die Tabelle herunterzuladen, wählen Sie ![Herunterladen](/help/assets/icons/Download.svg) aus.

* [!UICONTROL Touchpoint effectiveness] Tabelle, die das Ergebnis des algorithmischen Attribution AI-Modells darstellt. Die Daten für diese Tabelle werden nur für bestimmte Zeiträume generiert. Wählen Sie **[!UICONTROL As of *xx/xx/xx, xx:xx TZ *]**![Info](/help/assets/icons/InfoOutline.svg) aus, um weitere Details anzuzeigen.

Die Visualisierung zeigt für jeden Touchpoint in absteigender [!UICONTROL Efficiency measure] ![absteigender ](/help/assets/icons/SortOrderDown.svg)):

   * [!UICONTROL Paths touched]: Visualisiert den Prozentsatz der Pfade mit Konversion und den Prozentsatz der Pfade ohne Konversion. Bei einem Touchpoint werden mehr zugewiesene Konversionen angezeigt, wenn das Attributionskonversionsverhältnis hoch ist. Dieses Verhältnis vergleicht den Prozentsatz der Pfade, die zu einer Konversion führen, mit dem Prozentsatz der Pfade, die *nicht* zu einer Konversion führen.
   * [!UICONTROL Efficiency measure]: Generiert vom algorithmischen Attributionsmodell, zeigt das Effizienzmaß die relative Bedeutung eines Touchpoints für die Konversion an, unabhängig vom Touchpoint-Volumen. Der Wirkungsgrad wird auf einer Skala von 1 bis 5 gemessen. Beachten Sie, dass ein höheres Touchpoint-Volumen keine höhere Effizienz garantiert.
   * [!UICONTROL Total volume]: Die Gesamtzahl der Berührungen eines Touchpoints durch eine Benutzerin oder einen Benutzer. Die Anzahl umfasst Touchpoints, die auf einem Pfad angezeigt werden, der eine Konversion erreicht, sowie Pfade, die *Konversion*.

![Diagnose](/help/assets/model-insights-diagnostics.png)


## [!UICONTROL Historical overview]

Die Registerkarte Historische Übersicht zeigt Visualisierungen für:

* Konversion und Ausgaben nach Geschäftsquartal und Produkt.

* Ausgaben nach Kanal.

* Touchpoint-Ausgaben.

Sie können einen alternativen ausgabebasierten Kanal auswählen, der für diese Visualisierung angezeigt werden soll. Wählen Sie einen Kanal aus **[!UICONTROL Channels]**.

* Anzahl der Touchpoints.

Sie können einen alternativen volumenbasierten Kanal auswählen, der für diese Visualisierung angezeigt werden soll. Wählen Sie einen Kanal aus **[!UICONTROL Channels]**.

![Modell - Historischer Überblick](/help/assets/model-insights-historical-overview.png)

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
