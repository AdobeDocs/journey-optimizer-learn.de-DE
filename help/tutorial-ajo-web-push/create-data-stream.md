---
title: Erstellen eines Datenstroms
description: Diese Seite führt Sie durch die Erstellung eines Datenstroms in Adobe Experience Platform, der erforderlich ist, um Daten aus der Web-SDK zu erfassen und an AEP und Adobe Journey Optimizer weiterzuleiten. Der Datenstrom fungiert als Verbindung zwischen Ihrer Web-Anwendung und Adobe-Services und ermöglicht die Verarbeitung von Push-Abonnement- und Ereignisdaten.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-04-21T00:00:00Z
jira: KT-20879
exl-id: d419f6a4-67d5-46b5-9ae7-5a317300d1ad
source-git-commit: 676c21ca09e0df8d404b05081d71b147755d65d5
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# Erstellen eines Datenstroms

Ein Datenstrom in Adobe Experience Platform (AEP) fungiert als Endpunkt, der Daten empfängt, die von der Web-SDK gesendet werden. Diese Daten werden an konfigurierte Services wie AEP, Adobe Analytics oder Adobe Journey Optimizer weitergeleitet. In diesem Tutorial wird der Datenstrom verwendet, um Web-Push-Abonnementdaten und „price.drop“-Ereignisse zur Aktivierung an AEP zu senden.

## Erstellen eines Ereignisschemas zum Tracking von Push-Benachrichtigungen

Erstellen Sie ein neues XDM ExperienceEvent-Schema mit dem Namen `SchemaForPushNotification`. Fügen Sie die `Push Notification Tracking` und `Commerce Details` Feldergruppen zu diesem Schema hinzu. Die Felder aus der Feldergruppe &quot;Commerce-Details“ werden verwendet, um Produktinformationen zu erfassen und das benutzerdefinierte price.drop-Ereignis Trigger.

![event-schema](assets/event-schema.png)

## Profilschema erstellen, um das Einverständnis des Benutzers zu speichern

In diesem Tutorial verwenden wir die vordefinierte `AJO Push Profile Schema`. Dieses Schema speichert die Details des Push-Abonnements des Benutzers, einschließlich des Push-Tokens, das zum Versand von Web-Push-Benachrichtigungen erforderlich ist.

![profile_schema](assets/profile-schema.png)

## Erstellen von Datensätzen für das Schema

Erstellen Sie einen Datensatz mit dem Namen `DataSetForPushNotification` unter Verwendung des zuvor erstellten Ereignisschemas. Verwenden Sie für Profildaten die vordefinierte `AJO Push Profile Dataset`, die mit dem Push-Profilschema verknüpft ist. Notieren Sie sich die `DataSetForPushNotification`-ID, da sie später im Tutorial bei der Konfiguration der Anwendung über die .env-Datei erforderlich sein wird.

## Erstellen eines Datenstroms mit dem Ereignis- und Profildatensatz

Erstellen Sie einen neuen Datenstrom mit dem Namen WebPushDataStream unter Verwendung der im vorherigen Schritt erstellten Ereignis- und Profildatensätze. Notieren Sie sich die Datenstrom-ID, da sie später im Tutorial bei der Konfiguration der Anwendung über die .env-Datei erforderlich sein wird.

![Datenstrom](assets/datastream.png)
