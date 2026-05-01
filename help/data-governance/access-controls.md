---
title: Zugriffssteuerungen
description: Erfahren Sie, wie Sie Zugriffssteuerungen in Mix Modeler konfigurieren.
feature: Administration
exl-id: c9ec97d9-b9a2-41f5-8626-1cf967d5d7fe
TQID: https://experienceleague.adobe.com/EoiF5ui2Bqq0Oxuv-s5E5pQclj9gnjoKgZ1bOzRK-vY
product_v2:
  - id: b88c80e3-31df-4609-989d-d4dac0e6d973
feature_v2:
  - id: fe2edbb1-46f9-4347-a27c-577cab3640cb
subfeature_v2:
  - id: abe9e290-7d2f-4131-b71e-ef9900865044
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
autotag-review: '2026-05-01T09:20:37.287Z'
source-git-commit: 5579087b9381c4d8e909ed5fe3099fd42d5c6799
workflow-type: tm+mt
source-wordcount: 412
ht-degree: 25%

---

# Zugriffssteuerungen

Die Zugriffssteuerung für Mix Modeler wird über Experience Platform in der [Adobe Admin Console](https://adminconsole.adobe.com/) und über [Permissions](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home#platform-permissions) in Experience Platform bereitgestellt. Diese Funktion nutzt Produktprofile in der Admin Console, um Benutzende mit Berechtigungen und Sandboxes zu verknüpfen.

Weitere Informationen zur Zugriffssteuerung finden Sie unter [Zugriffssteuerung - Übersicht](https://experienceleague.adobe.com/de/docs/experience-platform/access-control/home).

## Rollenbasierte Zugriffssteuerung

Siehe [Administration](../main-guide/administration.md) über die Konfiguration rollenbasierter Zugriffsberechtigungen für Mix Modeler-Benutzende und -Benutzergruppen in Experience Platform.

## Attributbasierte Zugriffssteuerung

[Attributbasierte Zugriffssteuerung](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/overview) ist eine Funktion von Experience Platform, mit der Admins den Zugriff auf bestimmte Objekte und/oder Funktionen anhand von Attributen steuern können. Attribute können Metadaten sein, die einem Objekt hinzugefügt werden, z. B. ein Label, das einem Schemafeld oder Segment hinzugefügt wird. Administrierende definieren Zugriffsrichtlinien, die Attribute zur Verwaltung von Benutzerzugriffsberechtigungen enthalten.

Mit der attributbasierten Zugriffssteuerung können Sie Schemafelder des Experience-Datenmodells (XDM) mit Labels versehen, die Organisations- oder Datennutzungsbereiche definieren. Parallel dazu können Admins die Benutzeroberfläche zur Verwaltung von Benutzenden und Rollen verwenden, um Zugriffsrichtlinien für XDM-Schemafelder zu definieren. und den Zugriff für Benutzende oder Benutzergruppen (interne, externe oder Drittanbieter-Benutzende) besser verwalten. Darüber hinaus ermöglicht die attributbasierte Zugriffskontrolle Admins die Verwaltung des Zugriffs auf bestimmte Segmente.

Durch attributbasierte Zugriffssteuerung können Admins den Zugriff der Benutzenden sowohl auf sensible persönliche Daten (Sensitive Personal Data, SPD) als auch auf personenbezogene Daten (PII) für alle Platform-Workflows und -Ressourcen steuern. Administrierende können Benutzerrollen definieren, die nur Zugriff auf bestimmte Felder und Daten haben, die diesen Feldern entsprechen.

Beim Konfigurieren von Datensatzregeln für harmonisierte Datensätze wird die [attributbasierte Zugriffssteuerung](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/overview) von Experience Platform auf Feldebene erzwungen. Ein Feld ist eingeschränkt, wenn eine Bezeichnung an ein Schemafeld angehängt wird. Außerdem ist eine aktive Richtlinie aktiviert, die den Zugriff auf dieses Feld verweigert. Das Ergebnis:

* Die Schemafelder, die für Sie eingeschränkt sind, werden beim Erstellen einer Datensatzregel nicht angezeigt.
* Sie können die Zuordnung eines oder mehrerer Schemafelder, die für Sie eingeschränkt sind, nicht anzeigen oder bearbeiten. Wenn Sie eine Datensatzregel bearbeiten oder anzeigen, die solche eingeschränkten Felder enthält, wird der folgende Bildschirm angezeigt.
  ![Aktion nicht zulässig](/help/assets/action-not-permitted.png)
