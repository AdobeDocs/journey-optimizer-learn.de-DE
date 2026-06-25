---
title: Benutzerberechtigung erfassen
description: Erstellen Sie eine Web-Seite, um das Einverständnis des Benutzers zum Empfang von Push-Benachrichtigungen zu erfassen.
feature: Push
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-04-21T00:00:00.000Z
jira: KT-20879
exl-id: 5897420a-7488-4d48-b56c-86a53d1d2395
TQID: 'https://experienceleague.adobe.com/O5xiLJ7UOQNYSkfpCa2umhCkxt1cKILsO4fOKxtVifM'
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
source-git-commit: 676c21ca09e0df8d404b05081d71b147755d65d5
workflow-type: tm+mt
source-wordcount: 219
ht-degree: 0%

---

# Benutzerberechtigung erfassen

Auf dieser Web-Seite wird das Einverständnis des Benutzers zum Empfang von Push-Benachrichtigungen erfasst. Der Benutzer wird aufgefordert, Benachrichtigungen über die Benachrichtigungs-API des Browsers zu aktivieren und das Push-Abonnement bei Adobe Experience Platform unter Verwendung der Web-SDK zu registrieren. Dadurch wird sichergestellt, dass nur angemeldete Benutzende über Kampagnen und Journey in Adobe Journey Optimizer Push-Benachrichtigungen erhalten können.

Um Web-Push-Benachrichtigungen zu aktivieren, lädt die Seite zunächst eine Konfigurationsdatei, indem fetch(“/config„) innerhalb einer Initialisierungsfunktion aufgerufen wird. Diese Konfiguration wird von einer Node.js-Anwendung bereitgestellt und enthält Schlüsselwerte wie die Datenstrom-ID, die Organisations-ID, den gültigen öffentlichen Schlüssel, die App-ID und die Tracking-Datensatz-ID. Sobald die Konfiguration geladen ist, wird die Adobe Web SDK initialisiert und der Service Worker wird registriert, um Push-Messaging zu unterstützen. Wenn ein(e) Benutzende(r) auf Benachrichtigungen aktivieren klickt, werden sie im Browser mithilfe der Web-Benachrichtigungs-API zur Eingabe einer Berechtigung aufgefordert. Wenn die Berechtigung erteilt wurde, sendet die Web-SDK das Push-Abonnement an Adobe Experience Platform, und der/die Benutzende wird 24 Stunden lang als angemeldet markiert, um wiederholte Eingabeaufforderungen zu vermeiden. Sie können diesen Fluss auf der lokalen Web-Seite „shop-smart.html“ versuchen, die in der [Beispielanwendung](http://localhost:3000/) enthalten ist, nachdem Sie den Server gestartet haben.

![request-permissions](assets/request-notifications.png)
