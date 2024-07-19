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

Um einen Plan zu erstellen, wählen Sie in der Benutzeroberfläche ![PLan](/help/assets//icons/FileChart.svg) **[!UICONTROL Plans]** im Mix Modeler **[!UICONTROL Open plan canvas]** aus.

1. Im Bildschirm Planerstellung :

   1. Im Abschnitt **[!UICONTROL Setup]**

      1. Geben Sie einen **[!UICONTROL Plan name]** ein, z. B. `Demo plan`. Geben Sie einen **[!UICONTROL Description]** ein, z. B. `Demo plan for Luma company`.
      1. Wählen Sie eine **[!UICONTROL Model]** aus **[!UICONTROL _Wählen Sie eine Option aus._.]**.
      1. Sie können ![LinkOut](/help/assets//icons/LinkOut.svg) **[!UICONTROL Create model]** auswählen, um ein Modell direkt innerhalb der Planerstellung zu erstellen. Dadurch wird eine neue Registerkarte in Ihrem Browser geöffnet und die Benutzeroberfläche [Modelle](../models/overview.md) angezeigt.

         ![Einrichtung planen](/help/assets//plan-setup.png)

   1. Im Abschnitt **[!UICONTROL Budget]** :

      1. Geben Sie einen Datumsbereich an, indem Sie entweder Datumsangaben eingeben oder einen Datumsbereich mit ![Kalender](/help/assets//icons/Calendar.svg) auswählen.
      1. Geben Sie ein Budget ein.

      Um weitere Datumsbereiche hinzuzufügen, wählen Sie mit jedem Budget ![CalendarAdd](/help/assets//icons/CalendarAdd.svg) **[!UICONTROL Add row]** aus.

      Um einen Datumsbereich und das zugehörige Budget zu löschen, wählen Sie ![Schließen](/help/assets//icons/Close.svg) aus.

      So definieren Sie ein bestimmtes Höchstbudget:

      1. Schalten Sie **[!UICONTROL Maximize budget]** ein.
      1. Geben Sie den Höchstbetrag an. Der Betrag sollte dem Gesamtbudget entsprechen oder darüber liegen, der für die Datumsbereiche angegeben wurde.

         ![Budget planen](/help/assets//plan-budget.png)

   1. Wählen Sie **[!UICONTROL Next]** aus.

1. Im Dialogfeld **[!UICONTROL Done with all required fields]** :

   ![Plan abgeschlossen](/help/assets//plan-done-required-fields.png)

   * Auswählen <img src="/help/assets//icons/NewPlan.svg" width="25" /> **[!UICONTROL Create plan now]** , wenn Sie einen von AI empfohlenen Plan mit prognostiziertem ROI generieren möchten.

     Wählen Sie **[!UICONTROL OK]** aus. Ihr Plan wird erstellt.


   * Wählen Sie ![TableEdit](/help/assets//icons/TableEdit.svg) **[!UICONTROL Edit channel budgets first]** aus, wenn Sie das Kanalbudget bearbeiten möchten, bevor Sie einen Plan mit prognostiziertem ROI erstellen.

     Wählen Sie **[!UICONTROL OK]** aus, damit Sie Ihre Kanalausgaben in **[!UICONTROL Spend selection]** im nächsten Schritt definieren können.



1. Verwenden Sie im Abschnitt **[!UICONTROL Spend selection]** für jeden Budgetdatumsbereich die obere Ecke, um die Kanalverteilungsansicht für diesen Datenbereich zu öffnen.![](/help/assets//icons/ChevronRight.svg)

   1. Geben Sie zum Definieren von Budgets für jeden Kanal einen Wert für **[!UICONTROL Min]** und **[!UICONTROL Max]** ein oder verwenden Sie die Regler.

   1. Um zwischen Währungs- oder Prozenteingabe umzuschalten, wählen Sie **[!UICONTROL $]** oder **[!UICONTROL %]** für **[!UICONTROL View spend by]** aus.

      ![Ausgabenauswahl](/help/assets//plan-spend-selection.png)

   1. Wenn Sie fertig sind, wählen Sie **[!UICONTROL Create]** aus.

   1. Wählen Sie im Dialogfeld **[!UICONTROL Create plan]** die Option **[!UICONTROL Create plan]** aus, um Ihren Plan zu erstellen. Wählen Sie **[!UICONTROL Cancel]** aus, um die Erstellung Ihres Plans abzubrechen. Ein **[!UICONTROL No work is saved]** -Dialogfeld wird angezeigt, um zu bestätigen.
