---
title: Verwenden von Decisioning zur Personalisierung von Web-Angeboten
description: Erfahren Sie, wie Sie mit Journey Optimizer (AJO) Decisioning personalisierte Angebote auf einer Web-Seite unterbreiten können, indem Sie die in Experience Platform (AEP) integrierte Zielgruppensegmentierung nutzen.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-05T00:00:00Z
jira: KT-17728
exl-id: 382ee746-e8cd-4843-bfe9-913df8914136
source-git-commit: 7d812f589172c5052a1e9bfcf6a99d0769a6c2c7
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 2%

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
