---
title: Push-Kanal erstellen
description: Die Konfiguration des Push-Kanals definiert, wie Web-Push-Benachrichtigungen bereitgestellt werden, einschließlich der Anwendungseinstellungen und plattformspezifischer Details. Außerdem wird Ihre Push-Einrichtung mit den erforderlichen Anmeldeinformationen verknüpft, z. B. den GÜLTIGEN Schlüsseln, sodass AJO Benachrichtigungen an abonnierte Benutzende senden kann.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-01-21T00:00:00Z
jira: KT-20879
source-git-commit: 3d342c5c4de4dda221ce4427b1e4aef7ef8c22cc
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# Push-Kanal erstellen

Der erste Schritt besteht darin, in Adobe Journey Optimizer einen Push-Kanal zu erstellen. Im Rahmen dieser Einrichtung müssen Sie VAPID-Schlüssel generieren, die zur Authentifizierung und Aktivierung von Web-Push-Benachrichtigungen erforderlich sind. Diese Schlüssel werden dann in der Push-Kanal-Konfiguration verwendet, sodass AJO Benachrichtigungen sicher an abonnierte Benutzer senden kann.

## Generieren von VAPID-Schlüsseln

VAPID (Voluntary Application Server Identification) ist ein Web-Push-Standard, mit dem sich Ihr Server gegenüber Push-Services (wie Chrome, Edge usw.) identifizieren kann, die öffentliche/private Schlüsselpaare verwenden, sodass der Push-Anbieter weiß, wer die Benachrichtigung sendet.

Sie wird mithilfe eines Tools wie web-push-generate-valid-keys generiert, das einen öffentlichen Schlüssel (der mit dem Browser freigegeben wird) und einen privaten Schlüssel (auf dem Server gespeichert) erstellt, die zusammen zur Authentifizierung und zum sicheren Senden von Push-Nachrichten verwendet werden.

Für dieses Tutorial haben wir Node.js verwendet, um die gültigen Schlüssel zu generieren.

Stellen Sie sicher, dass Node.js installiert ist. Geben Sie dann den folgenden Befehl ein
```npm install web-push -g ```

![Web-Push](assets/install-web-push.png)

```web-push generate-vapid-keys```

![Vapid](assets/vapid-keys.png)

## Push-Anmeldedaten erstellen

* Bei Journey Optimizer anmelden

* Navigieren Sie zu Administration | Kanäle | Push-Einstellungen | Push-Anmeldeinformationen | Push-Anmeldeinformationen erstellen

* ![Push-Anmeldedaten](assets/push-credential.png)

## Kanalkonfiguration erstellen

* Bei Journey Optimizer anmelden

* Navigieren Sie zu Administration | Kanäle | Kanalkonfiguration erstellen
  ![channel-configuration](assets/push-channel.png)
