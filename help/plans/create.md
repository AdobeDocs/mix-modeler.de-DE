---
title: Plan erstellen
description: Erfahren Sie, wie Sie in Mix Modeler einen Plan erstellen.
feature: Plans
exl-id: 6d61d0b2-5871-4d00-9a35-73fff0a1c3e5
source-git-commit: 9085363e951a4e306c64ad28f56e2c15b4a6029a
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 1%

---


# Plan erstellen

Im Mix Modeler erstellen Sie einen Plan mithilfe der Planarbeitsfläche. Auf der Planarbeitsfläche können Sie die Details und Budgets Ihres Plans und das für Ihren Plan zu verwendende Modell einrichten. Nachdem Sie Details, Budget und Modell festgelegt haben, können Sie einen von AI empfohlenen Plan erstellen oder die Ausgaben nach Kanal bearbeiten.

Um einen Plan zu erstellen, klicken Sie im ![PLan](/help/assets//icons/FileChart.svg) **[!UICONTROL Plans]** Benutzeroberfläche in Mix Modeler auswählen **[!UICONTROL Open plan canvas]**.

1. Im Bildschirm Planerstellung :

   1. Im **[!UICONTROL Setup]** Abschnitt

      1. Geben Sie einen **[!UICONTROL Plan name]**, beispielsweise `Demo plan`. Geben Sie einen **[!UICONTROL Description]**, beispielsweise `Demo plan for Luma company`.
      1. Wählen Sie eine **[!UICONTROL Model]** von **[!UICONTROL _Wählen Sie eine Option aus._.]**.
      1. Sie können ![LinkOut](/help/assets//icons/LinkOut.svg) **[!UICONTROL Create model]** , um ein Modell direkt in der Planerstellung zu erstellen. Dadurch wird eine neue Registerkarte in Ihrem Browser geöffnet und die [Modelle](../models/overview.md) -Schnittstelle.

         ![Einrichtung planen](/help/assets//plan-setup.png)

   1. Im **[!UICONTROL Budget]** Abschnitt:

      1. Geben Sie einen Datumsbereich an, indem Sie entweder ein Datum eingeben oder einen Datumsbereich mit ![Kalender](/help/assets//icons/Calendar.svg).
      1. Geben Sie ein Budget ein.

      Um zusätzliche Datumsbereiche hinzuzufügen, wählen Sie jeden mit dem Budget aus. ![CalendarAdd](/help/assets//icons/CalendarAdd.svg) **[!UICONTROL Add row]**.

      Um einen Datumsbereich und das zugehörige Budget zu löschen, wählen Sie ![Schließen](/help/assets//icons/Close.svg).

      So definieren Sie ein bestimmtes Höchstbudget:

      1. Switch **[!UICONTROL Maximize budget]** auf.
      1. Geben Sie den Höchstbetrag an. Der Betrag sollte dem Gesamtbudget entsprechen oder darüber liegen, der für die Datumsbereiche angegeben wurde.

         ![Budget planen](/help/assets//plan-budget.png)

   1. Wählen Sie **[!UICONTROL Next]** aus.

1. Im **[!UICONTROL Done with all required fields]** dialog:

   ![Plan abgeschlossen](/help/assets//plan-done-required-fields.png)

   * Auswählen <img src="/help/assets//icons/NewPlan.svg" width="25" /> **[!UICONTROL Create plan now]** wenn Sie einen von AI empfohlenen Plan mit prognostiziertem ROI generieren möchten.

     Auswählen **[!UICONTROL OK]**. Ihr Plan wird erstellt.


   * Auswählen ![TableEdit](/help/assets//icons/TableEdit.svg) **[!UICONTROL Edit channel budgets first]** wenn Sie das Kanalbudget bearbeiten möchten, bevor Sie einen Plan mit prognostiziertem ROI erstellen.

     Auswählen **[!UICONTROL OK]**, damit Sie Ihre Kanalausgaben in festlegen können **[!UICONTROL Spend selection]** im nächsten Schritt.



1. Im **[!UICONTROL Spend selection]** verwenden, verwenden Sie für jeden Budgetdatumsbereich die ![Chevron](/help/assets//icons/ChevronRight.svg) Öffnen Sie oben die Kanalverteilungsansicht für diesen Datenbereich.

   1. Um Budgets für jeden Kanal zu definieren, geben Sie einen Wert für **[!UICONTROL Min]** und **[!UICONTROL Max]** oder benutzen Sie die Regler.

   1. Um zwischen Währungs- oder Prozenteingabe umzuschalten, wählen Sie **[!UICONTROL $]** oder **[!UICONTROL %]** für **[!UICONTROL View spend by]**.

      ![Ausgabenauswahl](/help/assets//plan-spend-selection.png)

   1. Wenn Sie fertig sind, wählen Sie **[!UICONTROL Create]** aus.

   1. Im **[!UICONTROL Create plan]** Dialogfeld auswählen **[!UICONTROL Create plan]** um Ihren Plan zu erstellen. Auswählen **[!UICONTROL Cancel]** , um die Erstellung Ihres Plans abzubrechen. A **[!UICONTROL No work is saved]** angezeigt, um zu bestätigen.
