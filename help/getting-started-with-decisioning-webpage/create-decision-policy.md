---
title: Entscheidungsrichtlinie erstellen
description: Eine Entscheidungsrichtlinie definiert die Logik, mit der bestimmt wird, welche Angebote einem Benutzer während der Personalisierung bereitgestellt werden.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-05T00:00:00Z
jira: KT-17728
source-git-commit: a675979bc590190e0481e63efbc2cfd30752b7c0
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 13%

---


# Entscheidungsrichtlinie erstellen

Entscheidungsrichtlinien sind Container für Angebote, die die Entscheidungs-Engine nutzen, um je nach Zielgruppe die besten bereitzustellenden Inhalte auszuwählen.

Klicken Sie im Personalisierungseditor im linken Navigationsbereich auf das Element Entscheidungsrichtlinie und dann auf Entscheidungsrichtlinie hinzufügen .

![create-decision-policy](assets/decision-policy.png)

Klicken Sie auf Hinzufügen , um die Auswahlstrategie auszuwählen
Klicken Sie auf Fallback auswählen , um das Fallback-Angebot auszuwählen.
Klicken Sie auf Weiter , um die Entscheidungsrichtlinie zu überprüfen, und klicken Sie auf Erstellen , um den Prozess der Erstellung der Entscheidungsrichtlinie abzuschließen.


![Entscheidungspolitik](assets/decision-policy2.png)


## Verwenden der Entscheidungsrichtlinie im Code-Editor

Klicken Sie im Personalisierungseditor auf Richtlinie einfügen. Der Code, der der Entscheidungsrichtlinie entspricht, wird hinzugefügt.

Zu diesem Zeitpunkt können Sie alle erforderlichen Entscheidungsattribute direkt in den Code aufnehmen. Diese Attribute werden in dem vom Angebotskatalog verwendeten Schema definiert. Standardattribute sind unter dem Namespace __Erlebnis“ organisiert, während alle benutzerdefinierten Attribute, die für Ihre Organisation spezifisch sind, unter dem Namespace `_<imsOrg>` gespeichert werden.

![using_decision_policy](assets/Insert-policy.png)

Dieser Code durchläuft eine Liste personalisierter Angebote, die für den Benutzer ausgewählt wurden, und zeigt den Text für jedes Angebot auf der Webseite an. Sie zeigt die Nachricht (offerText genannt) jedes Angebots innerhalb eines Absatzes an, damit die Benutzer ihren maßgeschneiderten Inhalt klar sehen können.
Wenn kein personalisiertes Angebot verfügbar ist, wird ein Fallback-Angebot angezeigt, um sicherzustellen, dass die Platzierung nicht leer bleibt.

Klicken Sie auf Speichern und dann auf Kampagne aktivieren .