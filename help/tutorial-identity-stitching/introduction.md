---
title: Identitätszusammenfügung in AEP
description: Richten Sie die Identitätszuordnung zwischen einer bekannten Benutzerin oder einem bekannten Benutzer (CRMID) und einer anonymen Web-Besucherin oder einem anonymen Web-Besucher (ECID) ein, wodurch einheitlichen Profile die Echtzeit-Personalisierung und Angebotsentscheidung in Adobe Journey Optimizer (AJO) ermöglicht wird.
feature: Profiles
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-19T00:00:00.000Z
jira: KT-18089
exl-id: d6a1201a-3779-4718-8ea8-b88f925f53b6
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: d2971708-e780-44bb-9e2a-72f139796afd
    internal-label: Customer
subfeature_v2:
  - id: ef9a83ca-eefa-47cf-aa34-f1a34715583a
    internal-label: Profiles
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: d4f3ee0d644b4f962763e6807f014efe132a9a05
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 11%
---
# Identitätszusammenfügung in AEP

In modernen Kundenerlebnissen ist es entscheidend, Benutzeridentitäten über Geräte und Kanäle hinweg zu vereinheitlichen. Dieser Anwendungsfall zeigt, wie die Identitätszuordnung in Adobe Experience Platform (AEP) implementiert wird, indem eine bekannte CRM-ID, die bei der Benutzeranmeldung erfasst wird, mit der anonymen Experience Cloud-ID (ECID) verknüpft wird, die von der Adobe Web SDK generiert wird. Durch die Echtzeit-Zuordnung dieser Identitäten kann AEP ein vollständigeres Kundenprofil erstellen, das sowohl das anonyme Verhalten als auch authentifizierte Daten umfasst. Dies ermöglicht eine genauere Zielgruppensegmentierung, Personalisierung und Entscheidungsfindung in Tools wie Adobe Journey Optimizer (AJO).

## Für das Tutorial zum Identitätszuordnung erforderliche Fähigkeiten

Um dieses Tutorial optimal nutzen zu können, wird eine Vertrautheit mit folgenden Themen empfohlen:

- Grundlegende Konzepte von **Adobe Experience Platform (AEP)**\
  Informationen zu Schemata, Datensätzen, Identitäten, Zusammenführungsrichtlinien und Echtzeitprofilen.

- **Schema- und Identitätsmodellierung**\
  Möglichkeit zum Konfigurieren von Identitätsfeldern in profil- und ereignisbasierten Schemata.

- **Adobe Launch (Tags) und Web SDK (Alloy.js)**\
  Erfahrung mit dem Einrichten von Datenelementen und Regeln zum Senden von Daten an AEP mithilfe der Web-SDK.

- **Grundlagen zu JavaScript**\
  Komfortables Arbeiten mit -Funktionen zur Erfassung von Benutzereingaben, Benutzerereignissen und Debugging-API-Aufrufen.

- **Debugging-Tools für AEP**\
  Möglichkeit, den AEP-Debugger und den Identitätsdiagramm-Viewer zu verwenden, um die Identitätszuordnung zu überprüfen.

- **Datenaufnahme in AEP**\
  Vertrautheit mit dem Hochladen von Beispieldaten in Datensätze und Sicherstellung der Datenqualität.


