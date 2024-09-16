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

Die Zugriffskontrolle für den Mix Modeler wird über Experience Platform in der [Adobe Admin Console](https://adminconsole.adobe.com/) und über [Berechtigungen](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home#platform-permissions) in der Experience Platform bereitgestellt. Diese Funktion nutzt Produktprofile in der Admin Console, die Benutzer mit Berechtigungen und Sandboxes verknüpfen.

Weitere Informationen zur Zugriffskontrolle finden Sie unter [Zugriffskontrolle - Übersicht](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home).

## Rollenbasierte Zugriffssteuerung

Informationen zum Konfigurieren rollenbasierter Zugriffsberechtigungen für Mix Modeler- und Benutzergruppen in Experience Platform finden Sie unter [Administration](../main-guide/administration.md) .

## Attributbasierte Zugriffssteuerung

[Attributbasierte Zugriffssteuerung](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/overview) ist eine Funktion von Experience Platform, mit der Administratoren den Zugriff auf bestimmte Objekte und/oder Funktionen anhand von Attributen steuern können. Attribute können Metadaten sein, die einem Objekt hinzugefügt werden, z. B. eine Bezeichnung, die einem Schemafeld oder Segment hinzugefügt wird. Administrierende definieren Zugriffsrichtlinien, die Attribute zur Verwaltung von Benutzerzugriffsberechtigungen enthalten.

Mit der attributbasierten Zugriffssteuerung können Sie Schemafelder des Experience-Datenmodells (XDM) mit Bezeichnungen versehen, die Organisations- oder Datennutzungsbereiche definieren. Parallel dazu können Administratoren die Benutzeroberfläche zur Verwaltung von Benutzern und Rollen verwenden, um Zugriffsrichtlinien für XDM-Schemafelder zu definieren. Außerdem können Sie den Benutzern oder Benutzergruppen (interne, externe oder Drittanbieter-Benutzer) gewährten Zugriff besser verwalten. Darüber hinaus ermöglicht die attributbasierte Zugriffskontrolle Admins die Verwaltung des Zugriffs auf bestimmte Segmente.

Mithilfe der attributbasierten Zugriffssteuerung können Administrierende den Zugriff der Benutzenden sowohl auf sensible persönliche Daten (Sensitive Personal Data, SPD) als auch auf personenbezogene Daten (Personally Identifiable Information, PII) für alle Platform-Workflows und -Ressourcen steuern. Administrierende können Benutzerrollen definieren, die nur Zugriff auf bestimmte Felder und Daten haben, die diesen Feldern entsprechen.

Beim Konfigurieren von Datensatzregeln für harmonisierte Datensätze wird die Experience Platform [attributbasierte Zugriffssteuerung](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/overview) auf Feldebene durchgesetzt. Ein Feld ist eingeschränkt, wenn eine Beschriftung an ein Schemafeld angehängt wird. Eine aktive Richtlinie wird aktiviert, die Ihnen den Zugriff auf dieses Feld verweigert. Das Ergebnis:

* Sie sehen die Schemafelder nicht, die Ihnen beim Erstellen einer Datensatzregel vorbehalten sind.
* Sie können die Zuordnung eines oder mehrerer für Sie eingeschränkter Schemafelder nicht anzeigen oder bearbeiten. Wenn Sie eine Datensatzregel mit solchen eingeschränkten Feldern bearbeiten oder anzeigen, wird der folgende Bildschirm angezeigt.
  ![Aktion nicht erlaubt](/help/assets/action-not-permitted.png)
