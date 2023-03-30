---
title: Konfigurieren einer Trainings-Sandbox – Einführung
description: Erfahren Sie, wie Sie eine Sandbox für Trainingszwecke konfigurieren. Führen Sie die erforderlichen Schritte aus, um die Schemata zu konfigurieren, Beispieldaten aufzunehmen und Ereignisse zu erstellen.
feature: Sandboxes, Data Management, Application Settings
doc-type: tutorial
kt: 9382
role: Admin
level: Beginner
last-substantial-update: 2023-02-01T00:00:00Z
exl-id: 8fa673de-9be9-4ab2-94cf-cfa8ac518223
source-git-commit: f7bfe367411f2bae23631ac4ecb34ad1d250381c
workflow-type: tm+mt
source-wordcount: '338'
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
