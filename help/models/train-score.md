---
title: Trainieren und Bewerten von Modellen
description: Erfahren Sie, wie Sie Modelle trainieren und bewerten.
feature: Models
source-git-commit: 6855d19347b7f6f1477a6265310df5950b8463c9
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 0%

---

# Trainieren und Bewerten von Modellen

Nachdem Sie ein Modell [erstellt](/help/models/build.md) erstellt haben, wird das Modell automatisch trainiert und bewertet. Sie können ein Modell manuell neu trainieren oder bewerten.

## trainieren

Erwägen Sie, ein Modell neu zu trainieren, wenn Sie neue inkrementelle Marketing- und Faktordaten einbeziehen möchten. Im letzten Quartal hat sich beispielsweise die Marktdynamik verändert oder Ihre Marketing-Datenverteilung hat sich erheblich verändert.

So trainieren Sie ein Modell neu:

1. Wählen Sie in der linken Leiste ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** aus.

1. Wählen Sie ![Mehr](/help/assets/icons/More.svg) für ein Modell aus und wählen Sie im Kontextmenü **[!UICONTROL Train]** aus. Wählen Sie alternativ ![DataRefresh](/help/assets/icons/DataRefresh.svg)-**[!UICONTROL Train]** in der blauen Aktionsleiste aus.

   Wählen Sie im Dialogfeld **[!UICONTROL Train model]** die Option aus, um:

   * **[!UICONTROL Train model with last 2 years of marketing data]** oder
   * **[!UICONTROL Train model using specific date range of data]**.
Geben Sie den Datumsbereich an. Sie können den ![Kalender“ verwenden](/help/assets/icons/Calendar.svg) um einen Datumsbereich auszuwählen. Es muss ein Datenbereich mit mindestens einem Jahr ausgewählt werden.

   ![Modell neu trainieren](../assets/retrain-model.png)

1. Wählen Sie **[!UICONTROL Train]** aus, um das Modell neu zu trainieren.


Ein Modell kann nur neu trainiert werden, wenn es erfolgreich trainiert wurde.


## Ergebnis


Sie können ein Modell inkrementell auf der Grundlage neuer Marketing-Daten bewerten oder ein Modell für einen bestimmten Datumsbereich neu bewerten.

Erwägen Sie, ein Modell neu zu bewerten, wenn Sie Folgendes tun möchten:

* Korrigieren Sie falsche Marketing-Daten. Beispielsweise fehlten für die Daten der letzten Paid Search, die Sie in das Training und die Bewertung des Modells eingeschlossen haben, eine Woche Daten.
* Verwenden Sie neue inkrementelle Marketing-Daten, die durch Aktualisierungen in den Datensätzen verfügbar geworden sind, die Sie als Teil Ihrer harmonisierten Daten konfiguriert haben.

So bewerten Sie ein Modell:

1. Wählen Sie in der linken Leiste ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** aus.

1. Wählen Sie ![Mehr](/help/assets/icons/More.svg) für ein Modell aus und wählen Sie im Kontextmenü **[!UICONTROL Score]** aus. Wählen Sie alternativ ![DataRefresh](/help/assets/icons/DataRefresh.svg)-**[!UICONTROL Score]** in der blauen Aktionsleiste aus.

   Wählen Sie im Dialogfeld **[!UICONTROL Score marketing data]** die Option aus, um:

   * **[!UICONTROL Score new marketing data from *MM/TT/JJJJ *]**, um Ihr Modell inkrementell mithilfe neuer Marketing-Daten zu bewerten, oder
   * **[!UICONTROL Score specific date range of marketing data]** für einen bestimmten Datumsbereich neu bewertet werden.
Geben Sie den Datumsbereich an. Sie können den ![Kalender“ verwenden](/help/assets/icons/Calendar.svg) um einen Datumsbereich auszuwählen.

   ![Erneutes Bewerten eines Modells](../assets/rescore-model.png)

1. Wählen Sie **[!UICONTROL Score]** aus. Wenn Sie ein Modell mit einem bestimmten Datenbereich neu bewerten, wird ein **[!UICONTROL Existing model is replaced]** Dialogfeld angezeigt, in dem Sie aufgefordert werden zu bestätigen, dass Sie das Modell durch neue Bewertungen für den ausgewählten Datumsbereich ersetzen möchten. Wählen Sie zur Bestätigung **[!UICONTROL Replace model]** aus.

>[!IMPORTANT]
>
>Das Neubewerten eines Modells ändert keine Pläne, die bereits auf der Grundlage des wiederhergestellten Modells erstellt wurden. Um das neue wiederhergestellte Modell in einem Plan zu verwenden, müssen Sie einen neuen Plan erstellen.

