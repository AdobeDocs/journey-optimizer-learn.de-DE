---
title: Nachverfolgung und Meldung von über AJO Offer Decisioning bereitgestellten Adobe Journey Optimizer (AJO)-Angeboten
description: Dieses Tutorial erweitert eine bestehende Implementierung von Adobe Journey Optimizer (AJO), die personalisierte Angebote auf der Grundlage von Kontextdaten wie Temperatur bereitstellt. Es wird beschrieben, wie Impression- und Interaktionsereignisse erfasst und die Daten für das Reporting in Journey Optimizer vorbereitet werden.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-07-18T00:00:00Z
jira: KT-18526
exl-id: ae74485f-9ea1-428d-9c07-5db0c5cf93fb
source-git-commit: 551d0d365bcb42e63910af1fae626d1bbc1fabfa
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---

# Nachverfolgung und Meldung von über AJO Offer Decisioning bereitgestellten Adobe Journey Optimizer (AJO)-Angeboten

Dieser Anwendungsfall konzentriert sich auf die Aktivierung von Reporting und Leistungsanalysen für Angebote, die über Adobe Journey Optimizer (AJO) bereitgestellt werden. Wenn Angebote anhand kontextueller Signale (z. B. Wetter oder Standort) personalisiert und bereitgestellt werden, müssen sowohl Impressionen als auch Benutzerinteraktionen verfolgt werden, um ihre Effektivität zu bewerten.

Durch die Erfassung von decisioning.propositionDisplay- und decisioning.propositionInteract-Ereignissen über die Adobe Web SDK und deren Zuordnung zu strukturierten XDM-Schemata in Adobe Experience Platform (AEP) werden Interaktionsdaten auf Angebotsebene zur Analyse verfügbar. Diese Daten können dann in Customer Journey Analytics (CJA) verwendet werden, um Dashboards zu erstellen, Schlüsselmetriken wie Clickthrough-Rate (CTR) zu messen und die Angebotsleistung in verschiedenen Zielgruppensegmenten und kontextuellen Bedingungen zu vergleichen.

Ziel ist es, klare, datengestützte Einblicke in die Leistung personalisierter Angebote zu erhalten und somit Informationen für künftige Entscheidungsstrategien zu liefern.



![reporting-dashboard](assets/dashboard-reporting.png)


## Voraussetzungen für dieses Tutorial

Bevor Sie beginnen, absolvieren Sie [ Tutorial zum Personalisieren von Angeboten mit Echtzeit-Wetterdaten .](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/personalizing-offers-with-real-time-weather-data/introduction) Es werden alle grundlegenden Komponenten festgelegt, einschließlich:

- Web SDK-Integration
- Angebotseinrichtung in Adobe Journey Optimizer (AJO)
- Entscheidungen mithilfe von kontextuellen Attributen wie Wetter und Temperatur
- Echtzeit-Angebotsrendering auf einer Web-Seite

Dieses Tutorial baut direkt auf dieser Implementierung auf und konzentriert sich speziell auf die Erfassung von Angebots-Impressions und Interaktionen für die Berichterstellung und Analyse in Journey Optimizer.
