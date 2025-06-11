---
title: Personalisieren von Angeboten mit Echtzeit-Wetterdaten in Adobe Journey Optimizer mithilfe von Web SDK
description: In diesem Tutorial erfahren Sie, wie Sie mithilfe von kontextuellen Echtzeitdaten und der Adobe Web SDK Personalization-API dynamische, wetterabhängige Angebote in Adobe Journey Optimizer bereitstellen können. Sie erfahren, wie Sie Wetterattribute (wie Temperatur und Bedingungen) von Ihrer Website an Adobe Experience Platform übergeben, sie Ihrem Ereignisschema zuordnen und in Entscheidungsregeln und Rangfolgeformeln verwenden können, um Angebote zum Zeitpunkt des Seitenladevorgangs zu personalisieren. Ideal für Marketing-Experten und Entwickler, die digitale Erlebnisse mit Echtzeit-Umgebungskontext verbessern möchten.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-06-10T00:00:00Z
jira: KT-18258
source-git-commit: 13c891c02a9a2da3ff742afaab7ceb449a417b5e
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 1%

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
