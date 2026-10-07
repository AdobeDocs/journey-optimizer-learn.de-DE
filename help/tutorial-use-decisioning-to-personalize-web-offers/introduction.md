---
title: Verwenden von Decisioning zur Personalisierung von Web-Angeboten
description: Erfahren Sie, wie Sie mit Journey Optimizer (AJO) Decisioning personalisierte Angebote auf einer Web-Seite unterbreiten können, indem Sie die in Experience Platform (AEP) integrierte Zielgruppensegmentierung nutzen.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-05T00:00:00.000Z
jira: KT-17728
exl-id: 382ee746-e8cd-4843-bfe9-913df8914136
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: a984631b-2bae-4860-9b15-69c41a799dcb
    internal-label: APIs and SDKs
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
    internal-label: Decisioning API
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: d4f3ee0d644b4f962763e6807f014efe132a9a05
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 7%
---
# Verwenden von Decisioning zur Personalisierung von Web-Angeboten

Dieses Tutorial baut auf einer zuvor erstellten Zielgruppensegmentierung auf, die mithilfe der Adobe Experience Platform (AEP) Web SDK eingerichtet wurde. Im [vorherigen Tutorial](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/create-audiences-using-web-sdk/introduction) wurden Benutzerpräferenzen wie Interesse an Aktien, Anleihen oder Einlagenzertifikaten (CDs) erfasst und verwendet, um Personen in Experience Platform in Audiences zu unterteilen, die sie ansprechen möchten. Dieses Tutorial baut auf dieser Grundlage auf, indem mit Adobe Journey Optimizer (AJO) Decisioning in Echtzeit personalisierte Finanzangebote für diese Zielgruppen bereitgestellt werden, wodurch sowohl Interaktions- als auch Konversionsergebnisse verbessert werden.


## Voraussetzungen für dieses Tutorial

* Zugriff auf Experience Platform

* Grundlegendes zu Experience Platform-Konzepten (Profile, Audiences, Datensätze)

* Vertrautheit mit Journey Optimizer

* Grundlegende JavaScript-Kenntnisse (Lesen und Schreiben einfacher Funktionen)

* Möglichkeit zur Verwendung von Browser-DevTools (Konsolen- und Netzwerk-Registerkarten)


## Ziel

Dieses Tutorial führt Sie durch die Bereitstellung personalisierter Anlageangebote wie Aktien, Anleihen oder CDs auf einer Website mit Journey Optimizer. Durch die Nutzung von Zielgruppensegmentierungs- und Entscheidungsstrategien erfahren Sie, wie Sie sicherstellen können, dass jeder Besucher das relevanteste Angebot basierend auf seinen Präferenzen sieht.

## Verwendete Tools

* Adobe Experience Platform (AEP)
* Adobe Journey Optimizer (AJO)
* Adobe Experience Platform Tags
* AEP Web SDK (`Alloy.js`)
* Segmentierung in AEP Edge
* Eine Webseite zur Anzeige der Angebote
