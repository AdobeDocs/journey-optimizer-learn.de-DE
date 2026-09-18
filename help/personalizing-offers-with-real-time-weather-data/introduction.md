---
title: Personalisieren von Angeboten mit Echtzeit-Wetterdaten in Adobe Journey Optimizer mithilfe eines Web SDK
description: In diesem Tutorial erfahren Sie, wie Sie mithilfe von kontextuellen Echtzeitdaten und der Personalisierungs-API des Adobe Web SDK dynamische, wetterabhängige Angebote in Adobe Journey Optimizer bereitstellen können. Sie erfahren, wie Sie Wetterattribute (wie Temperatur und Bedingungen) von Ihrer Website an Adobe Experience Platform übergeben, sie Ihrem Ereignisschema zuordnen und in Entscheidungsregeln und Rangfolgenformeln verwenden, um Angebote zum Zeitpunkt des Seitenladevorgangs zu personalisieren. Ideal für Marketing-Fachleute und Entwickelnde, die digitale Erlebnisse mit Echtzeit-Umgebungskontext verbessern möchten.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-06-10
jira: KT-18258
exl-id: f40dd541-470c-4f42-8181-eb1c277ebaa3
source-git-commit: b4cf9b677c6bc142e1013649db16b3a70b405052
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
