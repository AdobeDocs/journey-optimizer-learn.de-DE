---
title: Personalisieren von Web-Seitenangeboten mit AJO Decisioning auf der Grundlage von Zielgruppen
description: Erfahren Sie, wie Sie mit Adobe Journey Optimizer (AJO) Decisioning personalisierte Angebote auf einer Web-Seite unterbreiten können, indem Sie die in Adobe Experience Platform (AEP) integrierte Zielgruppensegmentierung nutzen.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-05T00:00:00Z
jira: KT-17728
source-git-commit: 9695a4db0d0caa44a8c7d49e069320309ffc40a6
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 1%

---


# Erstellen von AJO-Zielgruppen anhand der Voreinstellungen für Benutzerinvestitionen (Aktien, Anleihen, CDs)

Dieses Tutorial baut auf einer zuvor erstellten Zielgruppensegmentierung auf, die mithilfe der Adobe Experience Platform (AEP) Web SDK eingerichtet wurde. Im vorherigen Tutorial wurden Benutzerpräferenzen wie Interesse an Aktien, Anleihen oder Einlagenzertifikaten (Certificate of Deposit, CDs) erfasst und verwendet, um Personen in zielgerichtete Zielgruppen innerhalb von Adobe Experience Platform (AEP) zu unterteilen. Dieses Tutorial baut auf dieser Grundlage auf, indem mit Adobe Journey Optimizer (AJO) Decisioning in Echtzeit personalisierte Finanzangebote für diese Zielgruppen bereitgestellt werden, wodurch sowohl Interaktions- als auch Konversionsergebnisse verbessert werden.

Sie können die personalisierten AJO-Angebote live über den unten stehenden Link testen.
[Klicken Sie hier, um die Live-Demo anzuzeigen](https://gbedekar489.github.io/finwise/welcome.html) - die Seite zeigt Echtzeitangebote basierend auf Ihren Investitionsvoreinstellungen an.

## Voraussetzungen für dieses Tutorial

* Zugriff auf Adobe Experience Platform

* Grundlegendes zu Adobe Experience Platform-Konzepten (Profile, Audiences, Datensätze)

* Vertrautheit mit Adobe Journey Optimizer

* Grundlegende JavaScript-Kenntnisse (Lesen und Schreiben einfacher Funktionen)

* Möglichkeit zur Verwendung von Browser-DevTools (Konsolen- und Netzwerk-Registerkarten)


## ZIEL

Dieses Tutorial führt Sie durch die Bereitstellung personalisierter Anlageangebote wie Aktien, Anleihen oder CDs auf einer Website mit Adobe Journey Optimizer (AJO). Durch die Nutzung von Zielgruppensegmentierungs- und Entscheidungsstrategien erfahren Sie, wie Sie sicherstellen können, dass jeder Besucher das relevanteste Angebot basierend auf seinen Präferenzen sieht.

## Verwendete Tools

* Adobe Experience Platform (AEP)
* Adobe Journey Optimizer (AJO)
* Adobe Experience Platform Tags
* AEP Web SDK (Alloy.js)
* Segmentierung in AEP Edge
* Eine Webseite zur Anzeige der Angebote





