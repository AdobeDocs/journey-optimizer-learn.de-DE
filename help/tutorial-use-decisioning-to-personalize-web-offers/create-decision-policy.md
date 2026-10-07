---
title: Erstellen einer Entscheidungsrichtlinie
description: Verwenden Sie eine Entscheidungsrichtlinie, um die Logik zu definieren, um zu bestimmen, welche Angebote einem Benutzer während der Personalisierung bereitgestellt werden.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-05T00:00:00.000Z
recommendations: noDisplay, noCatalog
jira: KT-17728
exl-id: 186e4a7d-6077-401f-9958-2f955214bc35
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
source-wordcount: '246'
ht-degree: 8%
---
# Erstellen einer Entscheidungsrichtlinie

Entscheidungsrichtlinien sind Container für Ihre Angebote, die die [!UICONTROL Decisioning]-Engine nutzen, um je nach Zielgruppe die besten bereitzustellenden Inhalte auszuwählen.

1. Klicken Sie im Personalisierungseditor im linken Navigationsbereich auf **[!UICONTROL Entscheidungsrichtlinie]** und anschließend auf **[!UICONTROL Entscheidungsrichtlinie hinzufügen]**.

   ![create-decision-policy](assets/decision-policy.png)

1. Klicken Sie **[!UICONTROL Hinzufügen]**, um die Auswahlstrategie auszuwählen.

   ![Entscheidungspolitik](assets/decision-policy2.png)

1. Klicken Sie **[!UICONTROL Fallback auswählen]**, um das Fallback-Angebot auszuwählen.
1. Klicken Sie **[!UICONTROL Weiter]**, um die Entscheidungsrichtlinie zu überprüfen.
1. Klicken Sie **[!UICONTROL Erstellen]**, um die Erstellung der Entscheidungsrichtlinie abzuschließen.

## Verwenden der Entscheidungsrichtlinie im Code-Editor

1. Klicken Sie im Personalisierungseditor auf **[!UICONTROL Richtlinie einfügen]**.

   Der Code, der der Entscheidungsrichtlinie entspricht, wird hinzugefügt.

   Zu diesem Zeitpunkt können Sie alle erforderlichen Entscheidungsattribute direkt in den Code aufnehmen. Diese Attribute werden in dem vom Angebotskatalog verwendeten Schema definiert. Standardattribute sind unter dem Namespace `__experience` organisiert, während alle benutzerdefinierten Attribute, die für Ihre Organisation spezifisch sind, unter dem Namespace `_<imsOrg>` gespeichert werden.

   ![using_decision_policy](assets/Insert-policy.png)

   Dieser Code durchläuft eine Liste personalisierter Angebote, die für den Benutzer ausgewählt wurden, und zeigt den Text für jedes Angebot auf der Webseite an. Es zeigt die Nachricht (`offerText` genannt) von jedem Angebot innerhalb eines Absatzes an, sodass Benutzende ihren maßgeschneiderten Inhalt klar sehen können.

   Wenn kein personalisiertes Angebot verfügbar ist, wird ein Fallback-Angebot angezeigt, um sicherzustellen, dass die Platzierung nicht leer bleibt.

1. Klicken Sie **[!UICONTROL Speichern]** und aktivieren Sie die Kampagne.
