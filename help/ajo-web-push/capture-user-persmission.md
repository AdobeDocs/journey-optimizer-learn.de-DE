---
title: Benutzerberechtigung erfassen
description: Erstellen Sie eine Web-Seite, um das Einverständnis des Benutzers zum Empfang von Push-Benachrichtigungen zu erfassen.
feature: Push
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-04-21T00:00:00Z
jira: KT-20879
source-git-commit: 45f86aeb8fca071436785cc55225d853bb21998f
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---

# Benutzerberechtigung erfassen

Auf dieser Web-Seite wird das Einverständnis des Benutzers zum Empfang von Push-Benachrichtigungen erfasst. Der Benutzer wird aufgefordert, Benachrichtigungen über die Benachrichtigungs-API des Browsers zu aktivieren und das Push-Abonnement bei Adobe Experience Platform unter Verwendung der Web-SDK zu registrieren. Dadurch wird sichergestellt, dass nur angemeldete Benutzende über Kampagnen und Journey in Adobe Journey Optimizer Push-Benachrichtigungen erhalten können.

Um Web-Push-Benachrichtigungen zu aktivieren, lädt die Seite zunächst eine Konfigurationsdatei, indem fetch(“/config„) innerhalb einer Initialisierungsfunktion aufgerufen wird. Diese Konfiguration wird von einer Node.js-Anwendung bereitgestellt und enthält Schlüsselwerte wie die Datenstrom-ID, die Organisations-ID, den gültigen öffentlichen Schlüssel, die App-ID und die Tracking-Datensatz-ID. Sobald die Konfiguration geladen ist, wird die Adobe Web SDK initialisiert und der Service Worker wird registriert, um Push-Messaging zu unterstützen. Wenn ein(e) Benutzende(r) auf Benachrichtigungen aktivieren klickt, werden sie im Browser mithilfe der Web-Benachrichtigungs-API zur Eingabe einer Berechtigung aufgefordert. Wenn die Berechtigung erteilt wurde, sendet die Web-SDK das Push-Abonnement an Adobe Experience Platform, und der/die Benutzende wird 24 Stunden lang als angemeldet markiert, um wiederholte Eingabeaufforderungen zu vermeiden. Sie können diesen Fluss auf der lokalen Web-Seite „shop-smart.html“ versuchen, die in der [Beispielanwendung](http://localhost:3000/) enthalten ist, nachdem Sie den Server gestartet haben.

![request-permissions](assets/request-notifications.png)

