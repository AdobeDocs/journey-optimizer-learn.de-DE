---
title: Identitätszusammenfügung in AEP
description: Identitätszusammenfügung zwischen einem bekannten Benutzer (CRMID) und einem anonymen Web-Besucher (ECID), wodurch einheitliche Profile für die Echtzeit-Personalisierung und Angebotsentscheidung in Adobe Journey Optimizer (AJO) ermöglicht werden.
feature: Profiles
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-19T00:00:00Z
jira: KT-18089
exl-id: d6a1201a-3779-4718-8ea8-b88f925f53b6
source-git-commit: 96d9d525a3d9be399f7fa229b67166acf8130721
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 1%

---

# Beschreibung der Anwendungsfälle

In modernen Kundenerlebnissen ist es entscheidend, Benutzeridentitäten über Geräte und Kanäle hinweg zu vereinheitlichen. Dieser Anwendungsfall zeigt, wie die Identitätszuordnung in Adobe Experience Platform (AEP) implementiert wird, indem eine bekannte CRM-ID, die bei der Benutzeranmeldung erfasst wird, mit der anonymen Experience Cloud-ID (ECID) verknüpft wird, die von Adobe Web SDK generiert wird. Durch die Echtzeit-Zuordnung dieser Identitäten kann AEP ein vollständigeres Kundenprofil erstellen, das sowohl das anonyme Verhalten als auch authentifizierte Daten umfasst. Dies ermöglicht eine genauere Zielgruppensegmentierung, Personalisierung und Entscheidungsfindung in Tools wie Adobe Journey Optimizer (AJO).

## 🧠 für das Tutorial zum Identitätszuordnung erforderlich

Um dieses Tutorial optimal nutzen zu können, wird eine Vertrautheit mit folgenden Themen empfohlen:

- Grundlegende Konzepte von **Adobe Experience Platform (AEP)**\
  Informationen zu Schemata, Datensätzen, Identitäten, Zusammenführungsrichtlinien und Echtzeitprofilen.

- **Schema- und Identitätsmodellierung**\
  Möglichkeit zum Konfigurieren von Identitätsfeldern in profil- und ereignisbasierten Schemata.

- **Adobe Launch (Tags) und Web SDK (Alloy.js)**\
  Erfahrung mit dem Einrichten von Datenelementen und Regeln zum Senden von Daten an AEP mithilfe der Web-SDK.

- **Grundlagen zu JavaScript**\
  Trigger Komfortables Arbeiten mit -Funktionen zur Erfassung von Benutzereingaben, Benutzerereignissen und Debugging-API-Aufrufen.

- **Debugging-Tools für AEP**\
  Möglichkeit, den AEP-Debugger und den Identitätsdiagramm-Viewer zu verwenden, um die Identitätszuordnung zu überprüfen.

- **Datenaufnahme in AEP**\
  Vertrautheit mit dem Hochladen von Beispieldaten in Datensätze und Sicherstellung der Datenqualität.


