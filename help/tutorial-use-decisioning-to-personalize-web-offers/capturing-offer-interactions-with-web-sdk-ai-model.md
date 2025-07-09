---
title: Erfassen von Angebotsinteraktionen mit Adobe Web SDK für KI-Modellschulungen
description: Dieser Artikel konzentriert sich auf die Erfassung von Benutzerinteraktionsdaten - wie Angebotsimpressionen und Klicks - mithilfe der Adobe Experience Platform Web SDK (alloy.js). Diese Daten dienen als Grundlage für das Trainieren von KI-Modellen in Adobe Journey Optimizer (AJO), um Angebote intelligent nach Benutzerverhalten und kontextuellen Signalen zu ordnen.
feature: Decisioning
topic: Integrations
role: User
level: Beginner
doc-type: Article
last-substantial-update: 2025-07-08T00:00:00Z
jira: KT-18451
source-git-commit: dfb280df3453e7811dffd95b9af664b873a9af31
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 7%

---


# Erfassen von Angebotsinteraktionen mit Adobe Web SDK für KI-Modellschulungen

Dieser Artikel zeigt, wie Sie Interaktionsereignisse von Angeboten (wie Impressions oder Klicks) mithilfe der Adobe Experience Platform Web SDK erfassen können, indem Sie alloy(„sendEvent“, …) direkt in Ihrem JavaScript-Code aufrufen. Die Daten werden in AEP aufgenommen und zum Trainieren von KI-Modellen in Adobe Journey Optimizer (AJO) verwendet, um das Angebotsranking auf der Grundlage des Echtzeitverhaltens zu verbessern.

## Voraussetzungen

Bevor Sie beginnen, stellen Sie sicher, dass Folgendes vorhanden ist:

- Eine funktionierende Adobe Launch-Eigenschaft mit installierter Adobe Experience Platform Web SDK-Erweiterung.

- Ein [Datenstrom](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/decisioning/experience-decisioning/collect-event-data/create-dataset) konfiguriert und Ihrer AEP-Sandbox zugeordnet.

- Eine Website, auf der Launch bereitgestellt wird.


## Erstellen eines Schemas und Datensatzes für Interaktionsereignisse von Angeboten

Um Erlebnisereignisse zu erfassen, müssen Sie zunächst einen Datensatz erstellen, in dem diese Ereignisse gesendet werden.

Führen Sie die in diesem Artikel [ Schritte aus, um das erforderliche Schema und den erforderlichen Datensatz zu erstellen](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/decisioning/experience-decisioning/collect-event-data/create-dataset)

## Erstellen eines Datenstroms in AEP

![data-stream](assets/ai-model-data-stream.png)
Hinzufügen des Adobe Experience Platform-Service zum Datenstrom
![data-stream-service](assets/data-stream-service.png)

## Konfigurieren von Adobe Experience Platform-Tags mit dem Web-SDK

In den Erweiterungseinstellungen:

Konfigurieren der Adobe Experience Platform Web SDK-Erweiterung für die Verwendung des erstellten Datenstroms
