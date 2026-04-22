---
title: Web-Push in AJO
description: In diesem Tutorial wird gezeigt, wie Web-Push-Benachrichtigungen mithilfe von Adobe Journey Optimizer (AJO) implementiert werden. Sie erfahren, wie Sie das Benutzer-Opt-in mit der Web-SDK erfassen, Benachrichtigungen über geplante Kampagnen senden und Trigger-Echtzeit-Push-Nachrichten mithilfe eines benutzerdefinierten Price.drop-Ereignisses mit AEP-Tags senden.
feature: Push
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-04-21T00:00:00Z
jira: KT-20879
source-git-commit: 45f86aeb8fca071436785cc55225d853bb21998f
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---

# Web-Push in Adobe Journey Optimizer

Web-Push-Benachrichtigungen sind eine leistungsstarke Methode, um Benutzende in Echtzeit erneut einzubinden. Dieses Tutorial führt Sie durch die Implementierung mithilfe von Adobe Journey Optimizer (AJO). Zunächst verwenden Sie die Web-SDK, um die Opt-in-Voreinstellungen von Benutzenden für Push-Benachrichtigungen zu erfassen und so ein nahtloses und konformes Abonnementerlebnis sicherzustellen. Als Nächstes erstellen Sie eine Kampagne zum Senden von Push-Benachrichtigungen an Benutzer, die sich für die Kampagne entschieden haben, um eine zielgruppenbasierte Interaktion zu ermöglichen. Schließlich erfahren Sie, wie Sie AEP Tags nutzen können, um ein benutzerdefiniertes Preisabfallereignis zum Trigger zu bringen, das eine Journey in AJO initiiert und zeitnahe, personalisierte Push-Benachrichtigungen basierend auf dem Echtzeit-Benutzerverhalten bereitstellt.

Beispiel-Webseite, auf der Benutzer Benachrichtigungen auswählen können

![enable-notifications](assets/enable-notifications.png)

Beispiel einer Web-Seite für ein Preisabsenkungsereignis eines Triggers

![Preisverfall beim Trigger &#x200B;](assets/trigger-price-drop-event.png)

## Voraussetzungen

Dieses Tutorial ist praktisch und leicht zu befolgen. Es ist zwar kein fundiertes Fachwissen erforderlich, jedoch hilft eine grundlegende Vertrautheit mit den folgenden Konzepten:

- Adobe Journey Optimizer (Erstellen von Journey oder Kampagnen)
- Datenerfassung in AEP (Tags) und die Web-SDK
- Grundlegende Adobe Experience Platform-Konzepte wie Schemata und Ereignisse
- Einige JavaScript- und allgemeine Web-Entwicklungskonzepte
- Grundlegende Node.js-Kenntnisse (zum Generieren von VAPID-Schlüsseln und Bereitstellen eines einfachen Konfigurationsendpunkts)

Wenn Sie mit einem dieser Bereiche noch nicht vertraut sind, machen Sie sich keine Sorgen - das Tutorial führt Sie durch die wichtigsten Schritte auf dem Weg.
Dieses Tutorial konzentriert sich auf die Implementierung eines End-to-End-Anwendungsfalls für Web-Push-Benachrichtigungen. Daher hilft Ihnen ein praktisches Wissen über die oben genannten Tools und Konzepte dabei, effektiv vorzugehen.


## Browser-Benachrichtigungen 🔔 aktivieren

Wenn Benachrichtigungen blockiert sind oder nicht angezeigt werden, müssen Sie sie möglicherweise in Ihren Browser-Einstellungen aktivieren. Siehe die folgenden Handbücher:

- **Google Chrome (Windows/macOS)**\
  <https://support.google.com/chrome/answer/3220216>

- **Microsoft Edge (Windows)**\
  <https://support.microsoft.com/en-us/microsoft-edge/manage-website-notifications-in-microsoft-edge>

- **Safari (macOS)**\
  <https://support.apple.com/guide/safari/customize-website-notifications-sfri40734/mac>

- **Safari (iPhone/iPad)**\
  <https://support.apple.com/en-us/HT213893>


## Beispielanwendung


Damit Sie dem Beispiel folgen können, ist eine vollständige Beispielanwendung verfügbar.

- [Live-Demo - Opt-in:](https://ajo-web-push.onrender.com/)

- [Trigger-Preisabfallereignis:](https://ajo-web-push.onrender.com/price-drop-trigger.html)

- [Source-Code:](https://github.com/gbedekar489/ajo-web-push)

Sie können die Live-Demo erkunden, um den Fluss in Aktion zu sehen, oder das Repository klonen, um das Projekt lokal auszuführen.

