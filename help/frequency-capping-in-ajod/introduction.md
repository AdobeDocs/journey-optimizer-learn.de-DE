---
title: Implementieren der Frequenzlimitierung für Adobe Journey Optimizer (AJO)-Angebote, die über AJO Decisioning bereitgestellt werden
description: In diesem Tutorial wird eine bestehende Implementierung von Adobe Journey Optimizer (AJO) erweitert, indem die Frequenzlimitierung für Angebote aktiviert wird, die mit AJO Decisioning bereitgestellt werden. Es wird beschrieben, wie Impression- und Interaktionsereignisse erfasst werden, die bei der Frequenzlimitierung verwendet werden.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-01-21T00:00:00Z
jira: KT-18526
exl-id: ae74485f-9ea1-428d-9c07-5db0c5cf93fb
source-git-commit: 441fdbc33486f027c22d1b94e03919c5666ca003
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%

---

# Implementieren der Frequenzlimitierung für Adobe Journey Optimizer (AJO)-Angebote, die über AJO Decisioning bereitgestellt werden

In diesem Tutorial erfahren Sie, wie Sie eine Frequenzlimitierung auf Angebote in Adobe Journey Optimizer anwenden, um zu steuern, wie oft Benutzer im Laufe der Zeit dasselbe Angebot sehen.

In diesem Tutorial wird davon ausgegangen, dass Sie bereits eine AJO-Kampagne eingerichtet haben, indem Sie dem [Tutorial zum Personalisieren von Angeboten auf der Grundlage von Wetterbedingungen“ folgen](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/personalizing-offers-with-real-time-weather-data/introduction)

Durch die Erfassung von decisioning.propositionDisplay- und decisioning.propositionInteract-Ereignissen über die Adobe Web SDK und deren Zuordnung zu XDM-Schemas in Adobe Experience Platform (AEP) kann Adobe Journey Optimizer Angebotsimpressionen und Interaktionen genau verfolgen und eine Frequenzlimitierung aktivieren, um zu begrenzen, wie oft ein Angebot einem Anwender angezeigt wird.

## Voraussetzungen für dieses Tutorial

Bevor Sie fortfahren, stellen Sie sicher, dass Sie über eine gültige Adobe Journey Optimizer-Kampagne mit Decisioning verfügen, das aktiv Angebote an eine Web-Oberfläche sendet.

In diesem Tutorial wird davon ausgegangen, dass die Angebotsbereitstellung bereits funktioniert, und es konzentriert sich ausschließlich auf die Konfiguration und Validierung des Frequenzlimitierungsverhaltens.




