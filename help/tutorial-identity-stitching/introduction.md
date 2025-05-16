---
title: Identitätszusammenfügung in AEP
description: Identitätszusammenfügung zwischen einem bekannten Benutzer (CRMID) und einem anonymen Web-Besucher (ECID), wodurch einheitliche Profile für die Echtzeit-Personalisierung und Angebotsentscheidung in Adobe Journey Optimizer (AJO) ermöglicht werden.
feature: Profiles
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-19T00:00:00Z
jira: KT-18089
source-git-commit: 502cdc41b666959141ff4dfc63608cc463009811
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 2%

---


# Beschreibung der Anwendungsfälle

In modernen Kundenerlebnissen ist es entscheidend, Benutzeridentitäten über Geräte und Kanäle hinweg zu vereinheitlichen. Dieser Anwendungsfall zeigt, wie die Identitätszuordnung in Adobe Experience Platform (AEP) implementiert wird, indem eine bekannte CRM-ID, die bei der Benutzeranmeldung erfasst wird, mit der anonymen Experience Cloud-ID (ECID) verknüpft wird, die von Adobe Web SDK generiert wird. Durch die Echtzeit-Zuordnung dieser Identitäten kann AEP ein vollständigeres Kundenprofil erstellen, das sowohl das anonyme Verhalten als auch authentifizierte Daten umfasst. Dies ermöglicht eine genauere Zielgruppensegmentierung, Personalisierung und Entscheidungsfindung in Tools wie Adobe Journey Optimizer (AJO).

