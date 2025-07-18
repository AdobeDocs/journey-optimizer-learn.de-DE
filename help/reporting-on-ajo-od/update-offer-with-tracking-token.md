---
title: Tracking und Reporting von über AJO Offer Decisioning bereitgestellten Adobe Journey Optimizer (AJO)-Angeboten
description: Dieses Tutorial erweitert eine bestehende Implementierung von Adobe Journey Optimizer (AJO), die personalisierte Angebote auf der Grundlage von Kontextdaten wie Temperatur bereitstellt. Es wird beschrieben, wie Impression- und Interaktionsereignisse erfasst und die Daten für das Reporting in Journey Optimizer vorbereitet werden.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-06-10T00:00:00Z
jira: KT-18526
source-git-commit: fa4795d92cf290b867df23277a297c99d6222224
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 0%

---

# Hinzufügen von Tracking-Token zu Angebotselementen

Gehen Sie wie folgt vor, um den Code im Personalisierungseditor zu ändern:

Navigieren Sie zur _&#x200B;**Journey-Verwaltung > Kampagnen**&#x200B;_

Öffnen Sie die entsprechende Kampagne und klicken Sie auf die Schaltfläche _&#x200B;**Kampagne stoppen**&#x200B;_, um die Kampagne zu stoppen.

Öffnen Sie die gestoppte Kampagne und klicken Sie auf _&#x200B;**Schaltfläche Kampagne ändern**&#x200B;_.

Klicken Sie auf _&#x200B;**Inhalt**&#x200B;_ und dann auf die Schaltfläche _&#x200B;**Code bearbeiten**&#x200B;_, um den Personalisierungseditor zu öffnen.

Fügen Sie dem div zwei neue Datenattribute hinzu, wie im Screenshot gezeigt
![tracking-token](assets/offer-item-with-tracking-code.png)

Sie können trackingToken und ItemID hinzufügen, indem Sie im linken Navigationsbereich auf das Entscheidungsrichtliniensymbol klicken und in der Entscheidungsstruktur einen Drilldown durchführen, um die itemID und trackingToken auszuwählen.
![tracking-token](assets/insert-tracking-token.png)

Dadurch wird sichergestellt, dass jedes gerenderte Angebot ein Daten-Tracking-Token enthält, das für eine genaue Impression- und Klick-Ereignis-Verfolgung unerlässlich ist.

Speichern Sie die Änderungen und aktivieren Sie die Kampagne.
