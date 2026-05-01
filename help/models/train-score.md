---
title: Trainieren und Bewerten von Modellen
description: Erfahren Sie, wie Sie Modelle trainieren und bewerten.
feature: Models
exl-id: c4fbe13e-4548-421b-ba90-274fc42f4be2
TQID: https://experienceleague.adobe.com/yHi6d-zZeT5fpedJeqNAj-Q01NlEK-y3MybA5p54DhE
autotag-review: '2026-05-01T09:03:34.273Z'
product_v2: id: b88c80e3-31df-4609-989d-d4dac0e6d973
feature_v2: id: f40f1683-8300-4054-aab8-77da06ad63ff
subfeature_v2: id: cb40363e-1205-4921-971c-9ee6bdb18329
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: 5579087b9381c4d8e909ed5fe3099fd42d5c6799
workflow-type: tm+mt
source-wordcount: 374
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

1. Wählen Sie **[!UICONTROL Score]** aus. Beim Erstellen eines Modells mit einem bestimmten Datenbereich wird ein **[!UICONTROL Existing model is replaced]** angezeigt, in dem Sie aufgefordert werden, zu bestätigen, dass das Modell durch neue Bewertungen für den ausgewählten Datumsbereich ersetzt werden soll. Wählen Sie zur Bestätigung **[!UICONTROL Replace model]** aus.

>[!IMPORTANT]
>
>Das Neubewerten eines Modells ändert keine Pläne, die bereits auf der Grundlage des wiederhergestellten Modells erstellt wurden. Um das neue wiederhergestellte Modell in einem Plan zu verwenden, müssen Sie einen neuen Plan erstellen.
