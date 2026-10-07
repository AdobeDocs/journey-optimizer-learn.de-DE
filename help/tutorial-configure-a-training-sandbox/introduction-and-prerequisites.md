---
title: Konfigurieren einer Trainings-Sandbox – Einführung
description: Erfahren Sie, wie Sie eine Sandbox für Trainings-Zwecke konfigurieren. Führen Sie die erforderlichen Schritte aus, um die Schemata zu konfigurieren, Beispieldaten aufzunehmen und Ereignisse zu erstellen.
feature: Sandboxes, Data Management, Application Settings
doc-type: tutorial
jira: KT-9382
role: Admin
level: Beginner
last-substantial-update: 2023-02-01T00:00:00.000Z
exl-id: 8fa673de-9be9-4ab2-94cf-cfa8ac518223
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: aeebb91a-f216-4d5f-8da1-3a7e6f696ed0
    internal-label: Data management activity
  - id: d556b755-390a-43f0-be32-a08cf6236126
    internal-label: Configuration
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
    internal-label: Administration
subfeature_v2:
  - id: d2e8a157-b3b0-4143-9ff3-809bf400be56
    internal-label: Sandboxes
  - id: efb19423-4da4-4fd1-88d8-5ee8c71ae766
    internal-label: Application settings
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: d4f3ee0d644b4f962763e6807f014efe132a9a05
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 100%
---
# Konfigurieren einer Trainings-Sandbox – Einführung und Voraussetzungen

![Banner-Tutorial – Konfigurieren einer Trainings-Sandbox](./assets/ajo-banner-configure-training-sandbox.png)

Dieses Tutorial richtet sich an Administrierende und Dateningenieurinnen bzw. -ingenieure, die mit der Bereitstellung einer Trainings-Umgebung in Adobe [!DNL Journey Optimizer] betraut sind. Erfahren Sie, wie Sie die Schemata konfigurieren, Beispieldaten aufnehmen und Ereignisse erstellen können. Außerdem werden drei Testprofile erstellt, mit denen die Lernenden ihre Arbeit überprüfen können.

Die bereitgestellten Beispieldaten basieren auf einem fiktiven Unternehmen für Sportbekleidung namens _[!DNL Luma]_. [!DNL Luma] verfügt über Geschäfte in mehreren Ländern, eine Online-Präsenz mit einer Website und Mobile Apps. [!DNL Luma] verwendet Adobe Journey Optimizer, um seinen Kundinnen und Kunden vernetzte, kontextuelle und personalisierte Erlebnisse zu bieten.

Am Ende dieses Tutorials verfügen Sie über eine Sandbox, die die [!DNL Luma]-Anwendungsfälle unterstützt, welche in den praktischen Übungen im Abschnitt [Journey Optimizer-Herausforderungen](/help/challenges/introduction-and-prerequisites.md) behandelt werden.

## Voraussetzungen

Bevor Sie mit der Einrichtung Ihrer Trainings-Sandbox beginnen können, stellen Sie sicher, dass Sie Folgendes haben:

1. eine dedizierte Entwicklungs-[Sandbox](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/access-control/create-and-manage-sandboxes.html?lang=de)

1. [E-Mail-Nachrichten-Voreinstellungen](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/set-up-email-channel.html?lang=de), die für Marketing- und Transaktionsnachrichten konfiguriert sind

1. Rechte als **[!UICONTROL Journey-Admin]** und **[!UICONTROL Daten-Manager]** für die Trainings-Sandbox

1. Ihre [Organisations-ID](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=de)

1. die JSON-Dateien mit den Beispieldaten, die für Ihre Journey Optimizer-Instanz konfiguriert sind:

   1. Laden Sie [hier](/help/tutorial-configure-a-training-sandbox/assets/luma-data/luma-sample-data.zip) die Datei `luma-sample-data.zip` herunter, die alle für dieses Tutorial erforderlichen JSON-Dateien enthält.

   1. Verschieben Sie die Datei `luma-data.zip` aus dem Downloads-Ordner an den gewünschten Speicherort auf Ihrem Computer und entpacken Sie sie.

      Diese Dateien enthalten die Beispieldaten für Ihre Trainings-Sandbox.

   1. Öffnen Sie jede Datei, suchen Sie nach **`yourOrganizationID`** und ersetzen Sie sie durch Ihre [Organisations-ID](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=de).

   1. Speichern Sie die Dateien.

## Los geht‘s

Beginnen Sie mit der [manuellen Dateneinrichtung](/help/tutorial-configure-a-training-sandbox/manual-data-set-up.md).

In diesem Schritt definieren Sie die erforderliche Datenstruktur. Nachdem Sie den Datensatz eingerichtet haben, können Sie Daten in Ihre Sandbox aufnehmen und dann Ereignisse einrichten.
