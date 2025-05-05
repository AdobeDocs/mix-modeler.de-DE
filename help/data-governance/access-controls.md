---
title: Zugriffssteuerungen
description: Erfahren Sie, wie Sie Zugriffssteuerungen in Mix Modeler konfigurieren.
feature: Administration
exl-id: c9ec97d9-b9a2-41f5-8626-1cf967d5d7fe
source-git-commit: 9a6c1f1c12ab29da80a1997cfd31ca07b38eaa22
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 32%

---

# Zugriffssteuerungen

Die Zugriffssteuerung für den Mix Modeler wird durch Experience Platform in der [Adobe Admin Console](https://adminconsole.adobe.com/) und durch [Permissions](https://experienceleague.adobe.com/de/docs/experience-platform/access-control/home#platform-permissions) in Experience Platform bereitgestellt. Diese Funktion nutzt Produktprofile in der Admin Console, um Benutzende mit Berechtigungen und Sandboxes zu verknüpfen.

Weitere Informationen zur Zugriffssteuerung finden Sie unter [Zugriffssteuerung - Übersicht](https://experienceleague.adobe.com/de/docs/experience-platform/access-control/home).

## Rollenbasierte Zugriffssteuerung

Siehe [Administration](../main-guide/administration.md) über die Konfiguration rollenbasierter Zugriffsberechtigungen für Mix Modeler und Benutzergruppen auf Experience Platform.

## Attributbasierte Zugriffssteuerung

[Attributbasierte Zugriffssteuerung](https://experienceleague.adobe.com/de/docs/experience-platform/access-control/abac/overview) ist eine Funktion von Experience Platform, mit der Admins den Zugriff auf bestimmte Objekte und/oder Funktionen anhand von Attributen steuern können. Attribute können Metadaten sein, die einem Objekt hinzugefügt werden, z. B. eine Bezeichnung, die einem Schemafeld oder Segment hinzugefügt wird. Administrierende definieren Zugriffsrichtlinien, die Attribute zur Verwaltung von Benutzerzugriffsberechtigungen enthalten.

Mit der attributbasierten Zugriffssteuerung können Sie Schemafelder des Experience-Datenmodells (XDM) mit Bezeichnungen versehen, die Organisations- oder Datennutzungsbereiche definieren. Parallel dazu können Admins die Benutzeroberfläche zur Verwaltung von Benutzenden und Rollen verwenden, um Zugriffsrichtlinien für XDM-Schemafelder zu definieren. und den Zugriff für Benutzende oder Benutzergruppen (interne, externe oder Drittanbieter-Benutzende) besser verwalten. Darüber hinaus ermöglicht die attributbasierte Zugriffskontrolle Admins die Verwaltung des Zugriffs auf bestimmte Segmente.

Mithilfe der attributbasierten Zugriffssteuerung können Administrierende den Zugriff der Benutzenden sowohl auf sensible persönliche Daten (Sensitive Personal Data, SPD) als auch auf personenbezogene Daten (Personally Identifiable Information, PII) für alle Platform-Workflows und -Ressourcen steuern. Administrierende können Benutzerrollen definieren, die nur Zugriff auf bestimmte Felder und Daten haben, die diesen Feldern entsprechen.

Beim Konfigurieren von Datensatzregeln für harmonisierte Datensätze wird [ Experience Platform (attributbasierte ](https://experienceleague.adobe.com/de/docs/experience-platform/access-control/abac/overview)) auf Feldebene erzwungen. Ein Feld ist eingeschränkt, wenn eine Bezeichnung an ein Schemafeld angehängt wird. Außerdem ist eine aktive Richtlinie aktiviert, die den Zugriff auf dieses Feld verweigert. Das Ergebnis:

* Die Schemafelder, die für Sie eingeschränkt sind, werden beim Erstellen einer Datensatzregel nicht angezeigt.
* Sie können die Zuordnung eines oder mehrerer Schemafelder, die für Sie eingeschränkt sind, nicht anzeigen oder bearbeiten. Wenn Sie eine Datensatzregel bearbeiten oder anzeigen, die solche eingeschränkten Felder enthält, wird der folgende Bildschirm angezeigt.
  ![Aktion nicht zulässig](/help/assets/action-not-permitted.png)
