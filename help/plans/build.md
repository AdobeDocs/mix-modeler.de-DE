---
title: Pläne erstellen
description: Erfahren Sie, wie Sie in Mix Modeler Pläne erstellen.
feature: Plans
exl-id: 6d61d0b2-5871-4d00-9a35-73fff0a1c3e5
source-git-commit: 1d017960409e5433ac6b4950a5cf7a5b3174840a
workflow-type: tm+mt
source-wordcount: '708'
ht-degree: 1%

---


# Pläne erstellen

In Mix Modeler erstellen Sie einen Plan mithilfe der Arbeitsfläche „Plan“. Auf der Arbeitsfläche des Plans können Sie die Details und Budgets Ihres Plans sowie das zugrunde liegende Modell einrichten, das für Ihren Plan verwendet werden soll. Nachdem Sie Details, Budget und Modell angegeben haben, können Sie mit einem von KI empfohlenen Plan fortfahren oder die Ausgaben nach Kanal bearbeiten.

Um einen Plan zu erstellen, wählen Sie in der ![PLan](/help/assets/icons/FileChart.svg)-**[!UICONTROL Plans]** in Mix Modeler **[!UICONTROL Create plan]** aus.


1. Im **[!UICONTROL Plan creation]**:

   1. Im **[!UICONTROL Setup]** Abschnitt:

      1. Geben Sie einen **[!UICONTROL Plan name]** ein, z. B. `Demo plan`. Geben Sie einen **[!UICONTROL Description]** ein, z. B. `Demo plan for Luma company`.
      1. Wählen Sie eine **[!UICONTROL Model]** aus **[!UICONTROL _Option auswählen…_,]**
      1. Sie können **[!UICONTROL Create model]** ![LinkOut](/help/assets/icons/LinkOut.svg) auswählen, um ein Modell direkt aus der Planerstellung heraus zu erstellen. Dadurch wird eine neue Registerkarte in Ihrem Browser geöffnet und die Benutzeroberfläche [Modelle](../models/overview.md) angezeigt.

         ![Planeinrichtung](/help/assets/plan-setup.png)

   1. Im **[!UICONTROL Budget]** Abschnitt:

      1. Geben Sie einen Datumsbereich an, indem Sie entweder Daten eingeben oder einen Datumsbereich mithilfe von ![Kalender](/help/assets/icons/Calendar.svg) auswählen.
      1. Geben Sie ein Budget ein.

      Um zusätzliche Datumsbereiche mit jeweils ihrem Budget hinzuzufügen, wählen Sie ![CalendarAdd](/help/assets/icons/CalendarAdd.svg) **[!UICONTROL Add row]**.

      Um einen Datumsbereich und das zugehörige Budget zu löschen, wählen Sie ![Schließen](/help/assets/icons/Close.svg).

      So definieren Sie ein spezifiziertes Maximalbudget:

      1. Schalten Sie **[!UICONTROL Maximize budget]** ein.
      1. Geben Sie den Betrag des maximalen Budgets an. Der Betrag sollte gleich oder höher als der Gesamtbetrag der für die Datumsbereiche angegebenen Budgets sein.

         ![Budget planen](/help/assets/plan-budget.png)

   1. Wählen Sie **[!UICONTROL Next]** aus.

1. Im Dialogfeld **[!UICONTROL Done with all required fields]** :

   ![Plan abgeschlossen](/help/assets/plan-done-required-fields.png)

   * Wählen Sie ![Neuer Plan](/help/assets/icons/NewPlan.svg) **[!UICONTROL Create plan now]** aus, wenn Sie einen von KI empfohlenen Plan mit prognostiziertem ROI generieren möchten.


     Wählen Sie **[!UICONTROL OK]** aus. Ihr Plan wird erstellt.


   * Wählen Sie ![TableEdit](/help/assets/icons/TableEdit.svg) aus **[!UICONTROL Edit channel budgets first]** wenn Sie das Kanalbudget bearbeiten und erweiterte Konfigurationen definieren möchten, bevor ein Plan mit prognostiziertem ROI erstellt wird.

     Wählen Sie **[!UICONTROL OK]** aus, damit Sie im nächsten Schritt Ihre Kanalausgaben in **[!UICONTROL Spend selection]** definieren können.



1. Verwenden Sie im **[!UICONTROL Spend selection]** Abschnitt für jeden Budgetdatumsbereich den ![Chevron](/help/assets/icons/ChevronRight.svg), um die Kanalverteilungsansicht für diesen Datenbereich zu öffnen.

   Sie können historische Referenzdaten verwenden, wenn Sie vergangene Marketing-Ausgabendaten und -Erkenntnisse verwenden möchten. Sie sollten historische Referenzdaten berücksichtigen für:

   * Verbessern Sie die Budgetzuweisung durch Hervorhebung leistungsstarker Kanäle und leistungsschwacher Kanäle.
   * Unterstützung der Trendanalyse.
   * Identifizieren Sie effektive Strategien und vermeiden Sie Fehler bei der Konfiguration von Plänen.

   Wenn Sie einen historischen Referenzzeitraum auswählen, richten Sie sich nach den Voreinstellungen für frühere Ausgabenmuster aus, und die Planungsfunktion von Mix Modeler kann Pläne generieren, die Ihren Erwartungen entsprechen. Diese Pläne sollten letztendlich das Vertrauen der Stakeholder stärken, sicherstellen, dass Marketing-Pläne strategisch und effizient sind und dass diese Pläne auf bewährten Leistungsdaten und Geschäftsanforderungen basieren.

   ![Auswahl der Ausgaben](/help/assets/plan-spend-selection.png)

   1. Wählen Sie die **[!UICONTROL Spend pattern]**.

      * Standardmäßig ist dies **[!UICONTROL Automatic]**.
      * Wählen Sie **[!UICONTROL Historical reference]** aus und geben Sie einen **[!UICONTROL Start date]** ein, um auf frühere, Mix Modeler bereits verfügbare Marketing-Ausgabendaten zu verweisen. Die **[!UICONTROL End date]** wird automatisch anhand des Datenbereichs bestimmt, für den Sie das Ausgabenmuster definieren. Das vorgeschlagene Startdatum ist das erste verfügbare Datum für frühere Marketing-Ausgaben. Um anzuzeigen, dass Sie einen nicht vorhandenen oder ungültigen historischen Referenzzeitraum ausgewählt haben, wird ein ![AlertRed](/help/assets/icons/AlertRed.svg) angezeigt.

   1. Um Budgets für jeden Kanal zu definieren, geben Sie einen Wert für **[!UICONTROL Min]** und **[!UICONTROL Max]** ein oder verwenden Sie die Schieberegler.

   1. Um zwischen Eingabe von Währung oder Prozentsatz umzuschalten, wählen Sie **[!UICONTROL $]** oder **[!UICONTROL %]** für **[!UICONTROL View spend by]** aus.

   1. Wenn Sie fertig sind, wählen Sie **[!UICONTROL Create]** aus.
      ![Auswahl der Ausgaben](/help/assets/plan-spend-selection.png)

   1. Wählen Sie **[!UICONTROL Next]** aus.


1. Im Abschnitt **[!UICONTROL Advanced configurations]** können Sie optionale erweiterte Konfigurationen eingeben.

   ![Zusammenfassung des Plans](../assets/plan-advanced-configurations.png)

   * Ihr Planname , Modell, Datumsbereich und Gesamtbudget sind zusammengefasst.

   * Standardmäßig berechnet Mix Modeler den durchschnittlichen Umsatz pro Konversion automatisch anhand der neuesten saisonalen Verlaufsdaten. In **[!UICONTROL Average Revenue per conversion]** können Sie den spezifischen durchschnittlichen Umsatz pro Konversion definieren.

      1. Für jeden Datumsbereich in Ihrem Budget:

         1. Wählen Sie im Dropdown-Menü **[!UICONTROL Date range]** einen Datumsbereich aus.
         1. Geben Sie einen **[!UICONTROL Average revenue]** Wert ein.

      1. Wählen Sie ![AddCircle](/help/assets/icons/AddCircle.svg) Benutzerdefinierten durchschnittlichen Umsatz pro Konversionseinheit hinzufügen , um einen Datumsbereich hinzuzufügen.
      1. Wählen Sie ![RemoveCircle](/help/assets/icons/RemoveCircle.svg) aus, um einen Datumsbereich zu entfernen.

     >[!NOTE]
     >
     >Wenn Ihr Modell keine historischen Umsatzdaten enthält, müssen Sie für jeden Datumsbereich, den Sie für Ihr Budget angegeben haben, einen durchschnittlichen Umsatz pro Konversion definieren.
     >

   * Standardmäßig berechnet Mix Modeler die Kanalkosten automatisch anhand der neuesten saisonalen Verlaufsdaten. In **[!UICONTROL Channel costs]** können Sie benutzerdefinierte Kanalkosten definieren.

      1. Definieren Sie für jeden Kanal in Ihrem Modell benutzerdefinierte Kanalkosten.

         1. Wählen Sie einen Kanal aus dem Dropdown-Menü **[!UICONTROL Channel]** aus.
         1. Für jeden Datumsbereich in Ihrem Budget:
            1. Wählen Sie im Dropdown-Menü **[!UICONTROL Date range]** einen Datumsbereich aus.
            1. Geben Sie einen **[!UICONTROL Average revenue]** Wert ein.
         1. Wählen Sie ![AddCircle](/help/assets/icons/AddCircle.svg)-**[!UICONTROL Add custom average revenue per conversion unit]** aus, um einen Datumsbereich hinzuzufügen.
         1. Wählen Sie ![RemoveCircle](/help/assets/icons/RemoveCircle.svg) aus, um einen Datumsbereich zu entfernen.

      1. Wählen Sie ![AddCircle](/help/assets/icons/AddCircle.svg)-**[!UICONTROL Add custom channel cost]** aus, um einen Kanal hinzuzufügen.
      1. Wählen Sie ![CrossSize400](/help/assets/icons/CrossSize400.svg) aus, um einen benutzerdefinierten Kanal zu entfernen.


   1. Wenn Sie fertig sind, wählen Sie **[!UICONTROL Create]** aus.

   1. Wählen Sie im Dialogfeld **[!UICONTROL Create plan]** die Option **[!UICONTROL Create plan]** aus, um Ihren Plan zu erstellen. Wählen Sie **[!UICONTROL Cancel]** aus, um die Erstellung Ihres Plans abzubrechen. Zur Bestätigung wird ein **[!UICONTROL No work is saved]** Dialogfeld angezeigt.

