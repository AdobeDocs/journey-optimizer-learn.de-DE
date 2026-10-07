---
title: Implementieren der Frequenzlimitierung für Adobe Journey Optimizer (AJO)-Angebote, die über AJO Decisioning bereitgestellt werden
description: In diesem Tutorial wird eine bestehende Implementierung von Adobe Journey Optimizer (AJO) erweitert, indem die Frequenzlimitierung für Angebote aktiviert wird, die mit AJO Decisioning bereitgestellt werden. Es wird beschrieben, wie Impression- und Interaktionsereignisse erfasst werden, die bei der Frequenzlimitierung verwendet werden.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-01-21T00:00:00.000Z
jira: KT-18526
exl-id: ae74485f-9ea1-428d-9c07-5db0c5cf93fb
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
source-wordcount: '214'
ht-degree: 7%
---
# Implementieren der Frequenzlimitierung für Adobe Journey Optimizer (AJO)-Angebote, die über AJO Decisioning bereitgestellt werden

In diesem Tutorial erfahren Sie, wie Sie eine Frequenzlimitierung auf Angebote in Adobe Journey Optimizer anwenden, um zu steuern, wie oft Benutzer im Laufe der Zeit dasselbe Angebot sehen.

In diesem Tutorial wird davon ausgegangen, dass Sie bereits eine AJO-Kampagne eingerichtet haben, indem Sie dem [Tutorial zum Personalisieren von Angeboten auf der Grundlage von Wetterbedingungen“ folgen](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/personalizing-offers-with-real-time-weather-data/introduction)

Durch die Erfassung von decisioning.propositionDisplay- und decisioning.propositionInteract-Ereignissen über die Adobe Web SDK und deren Zuordnung zu XDM-Schemas in Adobe Experience Platform (AEP) kann Adobe Journey Optimizer Angebotsimpressionen und Interaktionen genau verfolgen und eine Frequenzlimitierung aktivieren, um zu begrenzen, wie oft ein Angebot einem Anwender angezeigt wird.

## Voraussetzungen für dieses Tutorial

Bevor Sie fortfahren, stellen Sie sicher, dass Sie über eine gültige Adobe Journey Optimizer-Kampagne mit Decisioning verfügen, das aktiv Angebote an eine Web-Oberfläche sendet.

In diesem Tutorial wird davon ausgegangen, dass die Angebotsbereitstellung bereits funktioniert, und es konzentriert sich ausschließlich auf die Konfiguration und Validierung des Frequenzlimitierungsverhaltens.




