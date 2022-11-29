---
title: Konfigurieren einer Trainings-Sandbox - Einführung
description: Erfahren Sie, wie Sie eine Sandbox für Schulungszwecke konfigurieren. Führen Sie die erforderlichen Schritte aus, um die Schemas zu konfigurieren, Beispieldaten zu erfassen und Ereignisse zu erstellen.
feature: Sandboxes, Data Management, Application Settings
doc-type: tutorial
kt: 9382
role: Admin
level: Beginner
exl-id: 8fa673de-9be9-4ab2-94cf-cfa8ac518223
source-git-commit: 8a2062f0719e799dd2d039488e6bba943fb458c4
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 6%

---

# Konfigurieren einer Trainings-Sandbox - Einführung und Voraussetzungen

![Banner-Tutorial - Konfigurieren einer Trainings-Sandbox](./assets/ajo-banner-configure-training-sandbox.png)

Dieses Tutorial richtet sich an Administratoren und Dateningenieure, die mit der Bereitstellung einer Adobe Journey Optimizer-Schulungsumgebung beauftragt sind. Erfahren Sie, wie Sie die Schemas konfigurieren, Beispieldaten erfassen und Ereignisse erstellen können. Außerdem werden drei Testprofile erstellt, mit denen die Lernenden ihre Arbeit überprüfen können.

Die bereitgestellten Beispieldaten basieren auf einer fiktiven Sportbekleidung namens _[!DNL Luma]_. [!DNL Luma] verfügt über Geschäfte in mehreren Ländern, eine Online-Präsenz mit einer Website und mobile Apps. [!DNL Luma] verwendet Adobe Journey Optimizer, um ihren Kunden verknüpfte, kontextbezogene und personalisierte Erlebnisse bereitzustellen.

Am Ende dieses Tutorials verfügen Sie über eine Sandbox, die die [!DNL Luma] Anwendungsfälle, die in den praktischen Übungen im [Journey Optimizer-Herausforderungen](/help/challenges/introduction-and-prerequisites.md) Abschnitt.

## Voraussetzungen

Bevor Sie mit der Einrichtung Ihrer Trainings-Sandbox beginnen können, stellen Sie Folgendes sicher:

1. Eine dedizierte Entwicklung [Sandbox](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/access-control/create-and-manage-sandboxes.html?lang=en).
1. [E-Mail-Nachrichtenvorgaben](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/channel-configuration/set-up-email-channel.html?lang=en) für Marketing- und Transaktionsnachrichten konfiguriert wurden.
1. **[!UICONTROL Journey-Administrator]** und **[!UICONTROL Data Manager]** Berechtigungen für die Trainings-Sandbox.
1. Ihre [Organisations-ID](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=de).

1. Die JSON-Dateien mit den Beispieldaten, die für Ihre Journey Optimizer-Instanz konfiguriert sind:

   1. Laden Sie die `luma-data.zip` file [here](/help/tutorial-configure-a-training-sandbox/assets/luma-data.zip), die alle für dieses Tutorial erforderlichen JSON-Dateien enthält.

   1. Verschieben Sie aus dem Ordner Downloads den `luma-data.zip` an den gewünschten Speicherort auf Ihrem Computer zu kopieren und zu dekomprimieren.

      Es sollten drei JSON-Dateien vorhanden sein: `luma-crm.json`, `luma-loyalty.json`, `luma-products.json`.

      Diese Dateien enthalten die Beispieldaten, die Sie in Ihre Sandbox aufnehmen.

   1. Öffnen Sie jede Datei und suchen Sie **`yourOrganizationID`** und ersetzen Sie sie durch Ihre [Organisations-ID](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=en).

   1. Speichern Sie die Dateien.

## Los geht‘s

Beginnen Sie mit der [Manuelle Datenerfassung](/help/tutorial-configure-a-training-sandbox/manual-data-set-up.md). In diesem Schritt definieren Sie die erforderliche Datenstruktur. Nachdem Sie den Datensatz eingerichtet haben, können Sie Daten in Ihre Sandbox aufnehmen und dann Ereignisse einrichten.
