---
title: Aktivieren der Frequenzlimitierung für eine AJO-Kampagne
description: Die Frequenzlimitierung in Adobe Journey Optimizer wird auf der Ebene der einzelnen Angebote angewendet und beruht auf der Erfassung sowohl von Impressions- als auch von Klickereignissen für Angebote. Dies erfordert das Tracking der Ereignisse decisioning.propositionDisplay und decisioning.propositionInteract unter Verwendung der Adobe Web SDK und deren Zuordnung zu einem aktualisierten XDM-Erlebnisereignisschema in Adobe Experience Platform.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-01-21T00:00:00Z
jira: KT-18526
source-git-commit: bef6d831c639d40514552dae3ff20132626a4a09
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---

# Aktivieren der Frequenzlimitierung für eine AJO-Kampagne

Um eine Frequenzlimitierung auf Angebote anzuwenden, führen Sie die folgenden Schritte aus:

## Ereignisschema aktualisieren

* Aktualisieren Sie das vorhandene Ereignisschema, indem Sie die Feldergruppe wie dargestellt hinzufügen
* ![event-schema](assets/schema.png)

## Aktualisieren der Frequenzlimitierung für das Angebot


* ![Angebot](assets/offer-capping.png)

## Tracking-Token zum Angebot hinzufügen

Bearbeiten Sie die in der Kampagne verwendete Entscheidungsrichtlinie, indem Sie ein Fallback-Angebot hinzufügen
![Fallback](assets/fallback.png)

Sie können trackingToken und ItemID hinzufügen, indem Sie im linken Navigationsbereich auf das Entscheidungsrichtliniensymbol klicken und in der Entscheidungsstruktur einen Drilldown durchführen, um die itemID und trackingToken auszuwählen.

Fügen Sie die Element-ID und das Tracking-Token dem div hinzu, das das Angebot enthält, wie unten gezeigt
![id-and-tracking-token](assets/id-and-tracking-token.png)

Dadurch wird sichergestellt, dass jedes gerenderte Angebot ein Daten-Tracking-Token enthält, das für eine genaue Impression- und Klick-Ereignis-Verfolgung unerlässlich ist.


Aktiviert die geänderte Kampagne.


## Senden von Impression- und Tracking-Ereignissen

Ändern Sie den vorhandenen JavaScript-Code, um Angebotsimpressions- und Interaktionsereignisse mithilfe der Adobe Web SDK zu erfassen und an Adobe Experience Platform zu senden. Siehe den [hier bereitgestellten Beispielcode.](capture-impression-click-events.md)


