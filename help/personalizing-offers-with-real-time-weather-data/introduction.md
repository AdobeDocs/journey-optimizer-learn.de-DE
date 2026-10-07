---
title: Personalisieren von Angeboten mit Echtzeit-Wetterdaten in Adobe Journey Optimizer mithilfe eines Web SDK
description: In diesem Tutorial erfahren Sie, wie Sie mithilfe von kontextuellen Echtzeitdaten und der Personalisierungs-API des Adobe Web SDK dynamische, wetterabhängige Angebote in Adobe Journey Optimizer bereitstellen können. Sie erfahren, wie Sie Wetterattribute (wie Temperatur und Bedingungen) von Ihrer Website an Adobe Experience Platform übergeben, sie Ihrem Ereignisschema zuordnen und in Entscheidungsregeln und Rangfolgenformeln verwenden, um Angebote zum Zeitpunkt des Seitenladevorgangs zu personalisieren. Ideal für Marketing-Fachleute und Entwickelnde, die digitale Erlebnisse mit Echtzeit-Umgebungskontext verbessern möchten.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-06-10T00:00:00.000Z
jira: KT-18258
exl-id: f40dd541-470c-4f42-8181-eb1c277ebaa3
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
source-wordcount: '230'
ht-degree: 43%
---
# Beschreibung der Anwendungsfälle

Die Verwendung wetterbezogener Daten in Adobe Journey Optimizer (AJO) zur Bereitstellung von Angeboten ermöglicht es Unternehmen, Kundenerlebnisse auf der Grundlage realer, in Echtzeit vorhandener Umgebungsbedingungen zu personalisieren. Das Wetter ist ein starkes, kontextuelles Signal. Bedürfnisse und Verhalten der Menschen ändern sich je nach Wetter. Durch Verwendung von Wetterdaten:

Bereitstellen relevanter Angebote, die der Stimmung und Umgebung der Kunden entsprechen

Zeigen Sie an einem heißen Tag ein Angebot für kalte Getränke oder AC-Einheiten an. Werben Sie an einem regnerischen Tag für Jacken oder Regenschirme

Beispiel für ein wetterbasiertes Angebot


![weather-offers](assets/offers-use-case.png)



## Voraussetzungen für dieses Tutorial

* Zugriff auf Experience Platform.

* Grundlegende Informationen zu Adobe Experience Platform Tags.

* Grundlegende Kenntnisse zu Experience Platform-Konzepten (Profile, Zielgruppen, Datensätze).

* Vertrautheit mit Journey Optimizer

* Grundlegende JavaScript-Kenntnisse (Lesen und Schreiben einfacher Funktionen).

* Möglichkeit zur Verwendung von Browser-DevTools (Konsolen- und Netzwerk-Registerkarten).
