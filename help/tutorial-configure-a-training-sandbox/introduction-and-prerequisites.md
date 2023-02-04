---
title: Konfigurieren einer Trainings-Sandbox - Einführung
description: Erfahren Sie, wie Sie eine Sandbox für Schulungszwecke konfigurieren. Führen Sie die erforderlichen Schritte aus, um die Schemas zu konfigurieren, Beispieldaten zu erfassen und Ereignisse zu erstellen.
feature: Sandboxes, Data Management, Application Settings
doc-type: tutorial
kt: 9382
role: Admin
level: Beginner
hide: true
exl-id: 8fa673de-9be9-4ab2-94cf-cfa8ac518223
source-git-commit: e377ddb8b84dccd503274caf9ffa3d4c73eedc28
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 10%

---

# Konfigurieren einer Trainings-Sandbox - Einführung und Voraussetzungen

![Banner-Tutorial - Konfigurieren einer Trainings-Sandbox](./assets/ajo-banner-configure-training-sandbox.png)

Dieses Tutorial richtet sich an Administratoren und Dateningenieure, die mit der Bereitstellung einer Adobe Journey Optimizer-Schulungsumgebung beauftragt sind. Erfahren Sie, wie Sie die Schemas konfigurieren, Beispieldaten erfassen und Ereignisse erstellen können. Außerdem werden drei Testprofile erstellt, mit denen die Lernenden ihre Arbeit überprüfen können.

Die bereitgestellten Beispieldaten basieren auf einer fiktiven Sportbekleidung namens _[!DNL Luma]_. [!DNL Luma] verfügt über Geschäfte in mehreren Ländern, eine Online-Präsenz mit einer Website und mobile Apps. [!DNL Luma] verwendet Adobe Journey Optimizer, um seinen Kundinnen und Kunden vernetzte, kontextuelle und personalisierte Erlebnisse zu bieten.

Am Ende dieses Tutorials verfügen Sie über eine Sandbox, die die [!DNL Luma] Anwendungsfälle, die in den praktischen Übungen im [Journey Optimizer-Herausforderungen](/help/challenges/introduction-and-prerequisites.md) Abschnitt.

## Voraussetzungen

Bevor Sie mit der Einrichtung Ihrer Trainings-Sandbox beginnen können, stellen Sie Folgendes sicher:

1. Eine dedizierte Entwicklung [Sandbox](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/access-control/create-and-manage-sandboxes.html?lang=en).
1. [E-Mail-Nachrichtenvorgaben](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/channel-configuration/set-up-email-channel.html?lang=en) für Marketing- und Transaktionsnachrichten konfiguriert wurden.
1. **[!UICONTROL Journey-Administrator]** und **[!UICONTROL Data Manager]** Berechtigungen für die Trainings-Sandbox.
1. Ihre [Organisations-ID](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=de).
1. Die JSON-Dateien mit den Beispieldaten, die für Ihre Journey Optimizer-Instanz konfiguriert sind:
   1. Laden Sie die `luma-sample-data.zip` file [here](/help/tutorial-configure-a-training-sandbox/assets/luma-data/luma-sample-data.zip), die alle für dieses Tutorial erforderlichen JSON-Dateien enthält.
   1. Verschieben Sie aus dem Ordner Downloads den `luma-data.zip` Datei an den gewünschten Speicherort auf Ihrem Computer und entpacken Sie sie. Diese Dateien enthalten die Beispieldaten für Ihre Trainings-Sandbox.
   1. Öffnen Sie jede Datei und suchen Sie **`yourOrganizationID`** und ersetzen Sie sie durch Ihre [Organisations-ID](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=de).
   1. Speichern Sie die Dateien.

## Los geht‘s

Beginnen Sie mit der [Manuelle Datenerfassung](/help/tutorial-configure-a-training-sandbox/manual-data-set-up.md). In diesem Schritt definieren Sie die erforderliche Datenstruktur. Nachdem Sie den Datensatz eingerichtet haben, können Sie Daten in Ihre Sandbox aufnehmen und dann Ereignisse einrichten.
