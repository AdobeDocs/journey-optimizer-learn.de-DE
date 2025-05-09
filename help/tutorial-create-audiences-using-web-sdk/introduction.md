---
title: Erstellen von Audiences mit Web SDK
description: In diesem Tutorial erfahren Sie, wie Sie Benutzereinstellungen über ein Web-Formular erfassen, diese Daten in Echtzeit an Adobe Experience Platform (AEP) senden und Benutzer basierend auf ihrer Auswahl dynamisch für Audiences qualifizieren. Durch die Kombination von Adobe Tags (Launch), AEP Web SDK (Alloy.js) und Edge-Segmentierung ermöglichen Sie sofortige Personalisierungsmöglichkeiten für Kunden, die an Aktien, Anleihen oder Einlagenzertifikaten (CDs) interessiert sind.
feature: Audiences
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-04-30T00:00:00Z
jira: KT-17923
exl-id: ebaa3aa5-0a08-43fd-8d06-8e4b5d8dee05
source-git-commit: 163edfb3367d03729d68c9339ee2af4a0fe3a1b3
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---

# Erstellen von Audiences mit Web SDK

In diesem Tutorial erfahren Sie, wie Sie Benutzereinstellungen über ein Web-Formular erfassen, diese Daten in Echtzeit an Adobe Experience Platform (AEP) senden und Benutzer basierend auf ihrer Auswahl dynamisch für Audiences qualifizieren. Durch die Kombination von Adobe Tags (Launch), AEP Web SDK (Alloy.js) und Edge-Segmentierung ermöglichen Sie sofortige Personalisierungsmöglichkeiten für Kunden, die an Aktien, Anleihen oder Einlagenzertifikaten (CDs) interessiert sind.

## Voraussetzungen für dieses Tutorial

* Zugriff auf Adobe Experience Platform

* Grundlegendes zu Adobe Experience Platform-Konzepten (Profile, Audiences, Datensätze)

* Vertrautheit mit Adobe Tags (Launch) - Einrichten von Datenelementen und Regeln

* Grundlegende JavaScript-Kenntnisse (Lesen und Schreiben einfacher Funktionen)

* Möglichkeit zur Verwendung von Browser-DevTools (Konsolen- und Netzwerk-Registerkarten)


## ZIEL

Ziel dieses Tutorials ist es, drei verschiedene Zielgruppen in Adobe Experience Platform (AEP) zu erstellen und zu qualifizieren:

* An Aktien interessierte Kunden

* An Anleihen interessierte Kunden

* Kunden, die an CDs interessiert sind

Benutzer senden ihre Voreinstellungen über ein Web-Formular, und diese Voreinstellungen werden über die AEP Web SDK mit Adobe Launch aufgenommen, was die Echtzeit-Zielgruppen-Qualifizierung ermöglicht.

## Verwendete Tools

* Adobe Experience Platform (AEP)

* Adobe Experience Platform Tags

* AEP Web SDK (Alloy.js)

* Segmentierung in AEP Edge

* Eine Webseite mit einem Präferenzformular
