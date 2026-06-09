---
title: Detaillierte Einblicke in Mix Modeler
description: Erkunden Sie die technische Methodik hinter Adobe Mix Modeler, einschließlich Multi-Touch-Attribution, Marketing-Mix-Modellierung, Transfer Learning und Budgetoptimierung.
feature: Administration
hide: true
feature_v2:
  - id: a234aebd-3855-4376-a64d-29b38411e0c5
  - id: fe1c9ae8-a908-4ae1-a0b6-fcf35177b134
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
source-git-commit: 4f4fe68694c81ddb258656eb05d62ef057f200cb
workflow-type: tm+mt
source-wordcount: 2747
ht-degree: 0%

---


# Tiefere Einblicke


Adobe Mix Modeler ist eine einheitliche, KI/ML-gestützte Messplattform, die Multi-Touch-Attribution (MTA) und Marketing-Mix-Modellierung (MMM) kombiniert, um genaue, skalierbare und zukunftssichere Marketing-Erkenntnisse zu liefern. In diesem Artikel werden die Methoden, Designoptionen und technischen Innovationen hinter Mix Modeler detailliert beschrieben. und basiert auf [dieser Summit 2025-Sitzung](https://business.adobe.com/de/summit/2025/sessions/marketing-mix-modeling-at-adobe-learn-to-predict-s602.html){target="_blank"} die eine detaillierte Aufschlüsselung der Methodik, Designentscheidungen und technischen Innovationen hinter Mix Modeler enthält.

Mit zunehmender Komplexität des Marketings bleiben herkömmliche Messansätze hinter den Erfordernissen zurück. Fragmentierte Daten, sich verändernde Datenschutzbeschränkungen und die Notwendigkeit, sowohl Geschwindigkeit als auch Strenge zu gewährleisten, machen es erforderlich, die Bewertung der Marketing-Leistung zu überdenken. Adobes Antwort ist Mix Modeler: ein integriertes System, das maschinelles Lernen nutzt, um mehrere Datenquellen zusammenzufügen und Paradigmen zu einer kohärenten Strategie zu modellieren.


>[!TIP]
>
>Einer der Hauptvorteile von Mix Modeler ist die Barrierefreiheit der Lösung für Marketing-Fachleute. Die Anwendung vereinfacht komplexe Datenwissenschaften durch eine benutzerfreundliche Oberfläche, die keinen datenwissenschaftlichen Hintergrund erfordert. Wenn Sie an einem tiefen Einblick interessiert sind, werden in diesem Artikel die technischen Entscheidungen bei der Entwicklung von Mix Modeler untersucht. Der Artikel setzt eine gewisse Vertrautheit mit (fortgeschrittenen) datenwissenschaftlichen Konzepten voraus.

In diesem Artikel werden die grundlegenden Komponenten detaillierter erläutert. Diese grundlegenden Komponenten sind:

* [Multi-Touch-Attribution](#multi-touch-attribution-mta)
* [Marketing-Mix-Modellierung](#marketing-mix-modeling-mmm)
* [Transfer Learning](#transfer-learning) (der intelligente Austausch von Ergebnissen zwischen Multi-Touch-Attribution und Marketing-Mix-Modellierung)



## Multi-Touch-Attribution (MTA)


### Überblick

Das Multi-Touch-Attributionsmodell (MTA), auf dem Mix Modeler basiert, basiert auf einem auf Daten auf Ereignisebene trainierten Modell für das zeitdiskrete Überleben. Zu den Daten gehören Suchvorgänge, Klicks, Produktansichten, Hinzufügen zu Warenkörben und Checkouts. Mithilfe des überwachten Lernens schätzt das Modell die bedingte Konversionswahrscheinlichkeit bei jedem Schritt im Kunden-Journey. Das Modell berücksichtigt sowohl Konversions- als auch Nicht-Konversions-Kunden-Journey-Pfade, um zu messen, wie verschiedene Marketing-Touchpoints das Kundenverhalten im Laufe der Zeit beeinflussen. Der Nicht-Konversionspfad ist genauso wichtig wie der Konversionspfad. Der Kontrast zwischen den beiden Pfaden hilft zu verstehen, ob ein bestimmter Typ von Marketing-Touchpoint die Konversion effektiv steigert. Wenn beispielsweise ein Touchpoint-Typ auf einem Nicht-Konversionspfad genauso wahrscheinlich erscheint wie auf einem Konversionspfad, hat dieser Touchpoint keine Auswirkungen auf die Konversion. Dieses Verhalten steht im Gegensatz zu einem Touchpoint, der häufig auf einem Konversionspfad und nicht auf einem Nicht-Konversionspfad erscheint.

![Daten auf Ereignisebene](/help/assets/event-level-data.png)

### Schlüsselkonzepte

Die wichtigsten Konzepte der Multi-Touch-Attribution sind:

* **Zinsmodellierung** Kundenkonversion wird als eine Akkumulation von Zinsen im Zeitverlauf modelliert.

  ![Risikoposition erhöht Zinsen](/help/assets/exposure-increases-interest.jpg)

  Bei diesem Ansatz treiben eine Reihe von Interessensignalen die Konversionswahrscheinlichkeit, jeweils beeinflusst durch

   * frühere Medienexpositionen,
   * Media Adstock Impact (ein Modell, wie Reaktionen auf Werbung und Verfall auf Verbrauchermärkten reagieren) und
   * Andere Baseline-Faktoren.



  Diese Signale werden als *ϴ<sub>BL</sub>* + *ϴE,<sub>-t1</sub>* + *ϴ<sub>E,tc-t2</sub>* und *ϴ<sub>S, tc-t3</sub>* dargestellt, wobei:

   * *ϴ*: veranschaulicht die Modellparameter (was wird aus dem Modell gelernt).
   * *TC*: Der Zeitpunkt der Konversion.
   * *TC-TX: Die Zeit zwischen der Belichtung und der Konversion, die für das Modell relevant ist.
   * *BL*: Grundlinie.
   * *E*: E-Mail
   * *S*: Suche.

  Im Modellierungs-Framework besteht das Ziel darin, explizit die Zeit zwischen jeder Medienexposition und dem Zeitpunkt der Konversion zu berücksichtigen (*tc-tx*), wobei zu berücksichtigen ist, dass neuere Interaktionen mehr Gewicht haben als ältere.

* **Wahrscheinlichkeitszuordnung**: Die Konversionswahrscheinlichkeit wird aus dem Interessenlevel mithilfe einer S-förmigen logistischen Funktion abgeleitet.

  ![Konversionswahrscheinlichkeit](/help/assets/probability-of-conversion.jpg)

  Durch das überwachte maschinelle Lernen, das ein Modell für das zeitdiskrete Überleben verwendet, visualisiert die obige Abbildung den Journey von Kunde A zur Konversion. Das Zinsniveau wird auf der X-Achse und die Konversionswahrscheinlichkeit auf der Y-Achse angezeigt. Diese Zuordnung zeigt, dass die zweite E-Mail-Exposition (*ϴE, tc-t2*) die größte Auswirkung auf die Konversion hat. Wie sich aus einem signifikanten Anstieg der Konversionswahrscheinlichkeit zum Zeitpunkt dieses Schritts ergibt.

* **Abnehmende Renditen**: Zusätzliche Touchpoints haben weniger inkrementelle Auswirkungen, wenn das Interesse wächst.

  Die S-förmige Kurve aus der obigen Abbildung zeigt auch, dass die Exposition des Kunden gegenüber zusätzlichen Touchpoints mit zunehmendem Zinsniveau weniger inkrementelle Auswirkungen hat.

* **Modell des zeitdiskreten Überlebens**: Die Verwendung eines Modells des zeitdiskreten Überlebens führt zu mehr Flexibilität im Modell, wodurch das Modell zeitliche Nuancen im Kundenverhalten erfassen kann. Das Diskrete-Zeit-Überlebensmodell lockert auch einige der restriktiveren Annahmen, die für kontinuierliche-Zeit-Überlebensmodelle erforderlich sind.

  ![Modell für das zeitdiskrete Überleben](/help/assets/discrete-time-survival-model.jpg)

  Eine Funktion mit kontinuierlicher Zeit modelliert die Auswirkung von E-Mail-Werbemitteln auf das Zinsniveau zu einem beliebigen Zeitpunkt seit dem Zeitpunkt der Exposition: *ϴ<sub>E</sub>(;⋋)*
Eine Diskrete-Zeit-Funktion modelliert die Auswirkungen von E-Mail-Werbemitteln auf das Interessensniveau als diskrete Zeitfenster unter Verwendung von skalaren Parametern: *ϴ<sub>E,i</sub> ≥ 0<sub>E,i+1</sub>*


### Vorteile

Der für Mix Modeler gewählte Multi-Touch-Attributionsansatz hat mehrere Hauptvorteile.

* Berücksichtigen Sie sowohl Konversions- als auch Nicht-Konversionspfade und stellen Sie so eine genauere Schätzung der tatsächlichen Medienwirkung sicher.
* Integrieren Sie Anzeigen und abnehmende Renditen, die das tatsächliche Kundenverhalten modellieren, und vermeiden Sie übermäßig vereinfachte Annahmen, die häufig in regelbasierten Modellen zu finden sind.
* Effiziente Skalierung auf große Datensätze durch Optimierung für verteiltes Computing und parallele Verarbeitung.
* Unterstützen Sie eine intuitive Touchpoint-Attribution, die eine klare Interpretation im Gegensatz zu anderen Methoden wie Hidden-Markov-Modellen ermöglicht.
* Bietet eine starke Leistung und hohe Prädiktionsgenauigkeit im Vergleich zu anderen Klassifizierungsalgorithmen.

Mix Modeler bietet eine [marketerfreundliche Oberfläche](/help/models/insights.md#attribution) um die Einblicke zu erfassen, die aus der Multi-Touch-Attribution resultieren.

![Modellattribution Insights](/help/assets/model-insights-attribution.png)


Obwohl die Multi-Touch-Attribution alle diese Vorteile bietet, ist Mix Modeler nicht in vollem Umfang auf Konversionserkenntnisse aus Daten auf Ereignisebene angewiesen. Die Modellierung des Marketing-Mix ist eine weitere grundlegende Komponente, um Daten auf aggregierter Ebene zu berücksichtigen.

## Marketing-Mix-Modellierung (MMM)

Die Marketing-Mix-Modellierung (MMM) basiert auf Daten auf aggregierter Ebene und verwendet eine multiplikative Modellstruktur anstelle einer additiven, um reale Marketing-Interaktionen widerzuspiegeln.

![Daten auf Aggregatebene](/help/assets/mmm-aggregate-data.jpg)

Die Abbildung zeigt Daten auf Aggregatebene im Tabellenformat an. Jede Zeile entspricht einem Zeitraum (normalerweise eine Woche, manchmal einen Tag), und jede Spalte stellt eine Variable dar. Die Tabelle enthält:

* die Spalte „Konversion“ (die Ergebnisvariable des Modells),
* Medienspalten (z. B.: Suchen, Anzeigen) und
* Faktorspalten (z. B. Saisonabhängigkeit, Werbeaktionen), um interne oder externe Einflüsse außerhalb der Medienausgaben zu erfassen, die sich noch auf die Medienleistung auswirken.

Das Modell prognostiziert Konversionen der Woche 4 anhand der hellgrün hervorgehobenen Daten, einschließlich der Faktoren dieser Woche und der historischen Eingaben aus den Medienkanälen.

### Schlüsselkonzepte

Die wichtigsten Konzepte der Marketing-Mix-Modellierung sind:

* **Multiplikatives Modell**: Umsätze oder Konversionen sind das Produkt einer Grundlinie und von Medienmultiplikatoren.

  Anstelle eines additiven Modells:
  *Wöchentliche Konversionen = Grundlegender Bedarf **+**&#x200B;Multiplikator für **+**&#x200B;Multiplikator für Anzeige **+**…*
Verwenden eines multiplikativen Modells:
  *Wöchentliche Konversionen = Grundlegender Bedarf **x**&#x200B;Multiplikator der Suche **x**&#x200B;Multiplikator der Anzeige **x**….*

  Oder in einer Formel: ** Y = ⨍<sub>BL</sub>(X<sub>faktoren</sub>;</sub><sub>faktoren</sub>) x ⨍<sub>S</sub>(X<sub>S</sub>;<sub>S</sub>) ⨍<sub>D(X<sub>D</sub>;<sub></sub>)*

  Beispiel:

   * Woche der tatsächlichen Konversionen: 1730.
   * Woche prognostizierte Konversionen: 1787,5 = 1100 x 1,25 x 1,3, wobei:
      * 1100: In Woche 4 wurde die Baseline-Nachfrage vorhergesagt, eine Funktion für die Daten zu Faktor 1 und 2 in Woche 4.
      * 1.25: Prognostizierter Suchmultiplikator für Woche 4, eine Funktion aus den Suchdaten von Woche 1 bis Woche 4.
      * 1.3: Prognostizierter Anzeigemultiplikator für Woche 4, eine Funktion zur Anzeige von Daten von Woche 1 bis Woche 4.

  Der erwartete Unterschied zwischen den Prognosen des Modells (1787.5) und den tatsächlichen Konversionen (1730) ist der Rest, der oft klein und kein Grund zur Sorge ist.


* **Adstock und abnehmender Ertrag erfassen**: Adstock wird mithilfe von exponentiellem Zerfall und Leistungsfunktionen erfasst.

  ![Abnehmende Renditen bei der Erfassung von Werbebeständen](/help/assets/capturing-adstock-diminishing-return.jpg)


  Der exponentielle Verfall von Adstock kann entweder einseitig oder zweiseitig sein, je nachdem, wo die größte Auswirkung nach der Medieninvestition auftritt.

  Um abnehmende Rücksendungen zu vermeiden, wird die Leistungsfunktion angewendet: *x<sup></sup>* für *∈ (0,1*). Diese Leistungsfunktion führt zu einem konkaven Diagramm, um den abnehmenden Ertrag zu erfassen. Der abnehmende Ertrag wird dann in der Multiplikatorfunktion innerhalb des MMM-Modells erfasst.


### Vorteile

Die Vorteile des Marketing-Mix-Modellierungsansatzes basieren auf der Tatsache, dass das multiplikative Modell das erwartete reale Marketing-Verhalten besser unterstützt. Beispiel:

* Mediensynergie, bei der Medienkanäle häufig besser zusammenarbeiten als isoliert.
* Zeitlich unterschiedliche Auswirkungen, bei denen die gleiche Marketinginvestition aufgrund externer Faktoren zu unterschiedlichen Zeitpunkten zu unterschiedlichen Renditen führen kann.
* Budgetempfehlungen im Zeitverlauf, wenn die erwarteten Marktbedingungen oder Basisschwankungen im Zeitverlauf bei der Budgetzuweisung hilfreich sind.

Mix Modeler bietet eine [marketerfreundliche Oberfläche](/help/models/insights.md#attribution) um die verschiedenen Erkenntnisse aus der Marketing-Mix-Modellierung zu erfassen. Beispielsweise eine Aufschlüsselung des Faktorbeitrags, um den Anteil der Basisumrechnungen anzuzeigen, der verschiedenen im Modell enthaltenen Faktoren zugeordnet werden kann.


![Verteilung der Faktorbeiträge](/help/assets/factors-example.png)


#### Beispiel

Dieses vereinfachte Beispiel zeigt, wie ein Ansatz zur multiplikativen Modellierung für einen fiktiven Sneaker-Online-Store eine bessere Budgetzuweisung ermöglicht als das additive Modell.

![Multiplikativer Modellansatz](/help/assets/benefits-mmm.jpg)

##### Annahmen

* Die Sneaker-Nachfrage ist im Sommer höher und im Winter niedriger, wie die Gesamtgrundbeiträge zeigen.

* Die Standardstrategie für die Marketing-Planung besteht darin, einen festen Betrag an Marketing-Budget (840 $) über das gesamte Jahr auszugeben, wobei jeder Monat dasselbe Budget erhält.

* Adstock wird ignoriert und bezahlte Medien werden als Einheit behandelt. Diese Annahmen sind unabhängig vom gewählten Modell und beeinflussen den Vergleich nicht.

* Ein konstantes Budget im Additivmodell bedeutet einen konstanten Beitrag über jeden Monat, der für das Additivmodell auf dem oberen Diagramm in der mittleren Spalte angezeigt wird.

* Im multiplikativen Modell bedeutet ein konstantes Budget konstante Multiplikatoren pro Monat. Um einen zeitvariablen Effekt für dieselben monatlichen Ausgaben zu erzielen, arbeitet der Multiplikator mit dem Basisbedarf. Dieser Multiplikatoreffekt ist im unteren Diagramm in der mittleren Spalte dargestellt.

##### Budgets verschieben

Besteht die Möglichkeit, von einem festen Budget wegzukommen und das Budget zu verschieben, aber das Gesamtbudget auf 840 Dollar zu belassen?

* Im additiven Modell besteht aus Modellierungsperspektive kein Anreiz für eine Änderung, da keine Interaktion mit der Grundlinie besteht. Eine Pauschale ist optimal. Wenn Sie $1 von November auf Mai verschieben, ist der Gewinn im Mai aufgrund sinkender Renditen geringer als der Rückgang im November.
* In einem multiplikativen Modell gibt es Raum für Veränderungen. Basierend auf der Basislinie können Sie Budgets von Wintermonaten in Sommermonate verschieben. Der Zuwachs im Sommermonat ist aufgrund des Multiplikationseffekts größer als der Verlust im Wintermonat. Das Ausmaß der Verschiebung und der Wechsel zu wird in den [Budgetoptimierungsalgorithmen) behandelt, &#x200B;](#budget-optimization) in der Marketing-Mix-Modellierung verwendet werden.



## Lerntransfer

Neben der Multi-Touch-Attribution und der Marketing-Mix-Modellierung ist das Experimentieren eine weitere wichtige Säule bei der Lösung von Marketing-Messproblemen. Obwohl das Experimentieren nicht im Rahmen von Mix Modeler implementiert wird, können Sie mithilfe von Experimenten, wie z. B. das Deaktivieren von Marketing in bestimmten Märkten, die kausalen Auswirkungen von Marketing auf den Umsatz verstehen.

Adobe empfiehlt und nutzt Transfer-Learning, um Einblicke aus der Multi-Touch-Attribution, Marketing-Mix-Modellierung, Experimenten und anderen früheren Wissensquellen zu kombinieren.  Diese Mischung kann als mehrschichtiger Ansatz beschrieben werden. Jede Schicht weist Lücken auf, um die Einschränkungen bei der Herstellung eines zusammenhängenden Modells zu veranschaulichen. Wenn Sie die Ebenen jedoch auf die richtige Art und Weise stapeln, können Sie die Lücken im kombinierten Modell ausgleichen.
Wenden Sie diese Analogie an, wenn Sie die Kombination aus Multi-Touch-Attribution, Marketing-Mix-Modellierung, Experimentieren und früheren Wissensquellen verwenden. Vermischen Sie diese Komponenten so, dass die Kombination am wenigsten an Fehlern in jeder der Komponenten leidet.

Im Wesentlichen ist Transferlernen numerische Optimierungsalgorithmen bei der Arbeit. Im Rahmen des Modelltrainings wird eine Verlustfunktion eingerichtet (um den Unterschied zwischen der prognostizierten Leistung eines Modells und dem tatsächlichen Wert (der Ground Truth) zu quantifizieren). Und es wird eine Metrik für die Anpassungsgüte (um zu bewerten, wie gut die Prognosen eines Modells mit den beobachteten Daten übereinstimmen) bestimmt. Das Transferlernen löst dann die numerische Optimierung, um die Tags (Modellparameter) zu erhalten. Wenn es eine oder mehrere Informationsquellen gibt, wird diese ursprüngliche Zieloptimierungsfunktion um einen anderen Begriff erweitert. Dieser Begriff misst den Abstand zwischen dem, was Sie als Vorkenntnisse bereitgestellt haben, und dem, was das Modell erzeugt, um es miteinander zu vergleichen.


### Bidirektionales Transferlernen

Wenn Sie sowohl Daten auf Ereignisebene als auch Daten auf Aggregatebene haben, umfasst das bidirektionale Transferlernen den folgenden Workflow.

![Bidirektionales Transferlernen](/help/assets/bi-directional-transfer-learning.jpg)

| Schritt | Beschreibung |
|:---:|---|
| 1a | Das standardmäßige MTA-Modell wird auf Daten trainiert. Normalerweise wird ein MTA-Modell in einem kürzeren Zeitfenster trainiert als das MMM-Modell. Die Daten umfassen Ereignisdaten aus Online-Kanälen. |
| 1b | Das MTA-Modell wird trainiert. Normalerweise wird ein MMM-Modell auf einem Zeitfenster von mindestens zwei Jahren trainiert. Die Daten umfassen Faktoren, Online- und Offline-Kanäle. |
| 2 | Das MTA-Modell wird bewertet. |
| 3 | Die Ergebnisse des bewerteten MTA-Modells werden als Transfer Learning in MMM eingespeist. |
| 4 | Das MMM-Modell wird mit der Übertragung der Lerndaten aktualisiert. Diese Aktualisierung bedeutet, dass ein neuer Satz von Parameterschätzungen für zusätzliche Einblicke und die Budgetoptimierung verwendet wird. Die Kanäle und die Zeitabdeckung ändern sich nicht. |
| 5 | Das MMM-Modell wird anhand der wöchentlichen Aggregatdaten für die Kanäle bewertet. |
| 6 | Das Ergebnis des bewerteten MMM-Modells wird als Transfer Learning in den MTA eingespeist. |
| 7 | Die MTA-Bewertungen für Daten auf Ereignisebene werden mithilfe der Übertragung von Lernergebnissen aktualisiert und für zusätzliche Einblicke verwendet. |

Beachten Sie Folgendes:

* MTA ist in Bezug auf die Kanalabdeckung begrenzt (z. B. nur Daten auf Ereignisebene aus Web- und Mobildaten), ist jedoch aufgrund der großen Datenmenge von Vorteil. Der Hauptaspekt von MTA ist die relative Leistung.
* MMM versteht das ganzheitlichere Bild mit Faktoren, Online- und Offline-Kanälen.
* Die Übertragung von Lerninhalten vom MTA auf MMM aktualisiert das MMM-Modell. Die Lernergebnisse beeinflussen die Parameter, die das multiplikative *Modell)*. Die Übertragung von Lerninhalten von MMM auf MTA aktualisiert den MTA *Bewertungen*. Es besteht keine Notwendigkeit, das MTA-Modell zu beeinflussen, da die anfänglichen Scores bereits statistisch ausreichend sind.

## Vorkenntnisse

Neben MTA, MMM und Experimentieren gibt es also viele weitere Quellen für Vorkenntnisse, die Sie optional für die Marketing-Messplanung nutzen können. Verschiedene Unternehmen verfügen über unterschiedliche Quellen für Vorkenntnisse. Beispiele sind Ausgabenanteile, frühere interne Modelle oder Branchenerfahrung.

![Vorkenntnisse](/help/assets/prior-knowledge.jpg)

Der Modellerstellungsprozess kann alle diese Informationsquellen durch denselben Transfer-Lernprozess nutzen. Diese Quellen für Vorkenntnisse sind optional. Sie müssen keine vorherigen Wissensquellen haben, damit die Marketing-Mix-Modellierung funktioniert. Wenn Sie nicht über Vorkenntnisse verfügen, wird das Standardmodell verwendet, um Score-Einblicke und dann Budgetoptimierung zu generieren. Wenn Sie bereits über Vorkenntnisse verfügen, können Sie das MMM-Modell mithilfe von Lerntransfer aktualisieren.


## Budgetoptimierung

Die Budgetoptimierung basiert auf dem zuvor erläuterten multiplikativen MMM-Modell.

In einem einfachen Beispiel gibt es zwei Kanäle: Suche und Anzeige. Und Sie haben ein Gesamtbudget. Ziel ist es, das Budget auf die beiden Kanäle aufzuteilen, um die Konversionsrate zu maximieren. Die numerische Optimierung wird verwendet, um den optimalen Budgetmix zu finden, der die Konversion unter der Gesamtbudgetbeschränkung maximiert. Nehmen wir an, Ihre Gesamtbudgetbeschränkung beträgt 130.000 $.

Die Budgetoptimierungsformel lautet: *Max ⨍(X<sub>S</sub>, X<sub>D</sub>) = ⨍<sub>BL</sub>(X<sub>faktoren</sub>) x ⨍<sub>S</sub>(X<sub>S</sub>) x ⨍<sub>(X<sub>DD</sub>)*, wobei *X<sub></sub>* *<sub></sub>* *<sub></sub>* SsSsundXxDdParameter prognostiziert werden undXxX</sub>DFaktorenprognostiziert wird.

![Budgetbeschränkungen](/help/assets/budget-constraints.png)


### Einschränkungen auf Kanalebene

Angenommen, es gibt zusätzliche Einschränkungen auf Kanalebene:

* $10K - $80K für die Suche.
* $5K - $70K für die Anzeige.
* Insgesamt 130.000 $.

Daher führt der anrechenbare Budgetmix zu einer Einschränkung der Optimierungsoberfläche. Der numerische Optimierungsalgorithmus hilft dann bei der Bestimmung der optimalen Budgetzuweisung.

### Über mehrere Konversionen hinweg

Planen Sie zusätzlich zu den Einschränkungen auf Kanalebene eine optimale Budgetzuweisung für mehrere Konversionen.

![Budgetoptimierung über Konversionen hinweg](/help/assets/planning-across-multiple-conversions.jpg)

Um eine optimale Budgetzuweisung über Konversionen hinweg zu ermöglichen, wird für jede der Konversionen ein gewichteter Durchschnitt der oben genannten Funktion verwendet. Die Formel wird *⨍<sub>neu</sub>(X) = w<sub>1</sub>f<sub>1</sub>(X) + w<sub>2</sub>f<sub>2</sub>(X)*

Beispiele für die Budgetoptimierung über mehrere Konversionen hinweg sind:

* Sie möchten den Gesamtumsatz aus Online-Verkäufen und In-Store-Konversionen maximieren.
* Sie möchten mithilfe von Markenbewusstseins-KPIs und Konversionen im Vertrieb eine Optimierung für den langfristigen Erfolg durchführen.

Im zweiten Beispiel sind die Einheiten der beiden Konversionen nicht ähnlich (Markenbewusstsein-KPI versus Konversionen), aber das spielt keine Rolle. Konversionen oder Modelle müssen nicht auf dieselben Kanäle verweisen und können sich auch überschneiden. Die numerische Optimierung findet innerhalb der gegebenen Einschränkungen die beste Lösung für das Problem.


## Zusammenfassung

Adobe Mix Modeler ist mehr als nur ein Messwerkzeug. Mix Modeler ist eine Entscheidungs-Support-Engine und bietet folgende Stärken:

* Die Fähigkeit, reale Komplexität mit statistischer Genauigkeit zu modellieren
* Eine einheitliche Integration verschiedener Daten- und Modellierungsparadigmen
* Eine zukunftssichere Architektur, die sich an Trends zur Datenverwerfung anpasst

Die Kombination aus Interpretierbarkeit und Leistung hat Mix Modeler in den Mittelpunkt der datengesteuerten Marketing-Transformation von Adobe gerückt. Mix Modeler ermöglicht es Marketing-Teams, schnellere, intelligentere und besser abgestimmte Investitionsentscheidungen zu treffen.
