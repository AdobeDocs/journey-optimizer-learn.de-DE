---
title: Lokales Ausführen der Anwendung
description: Einrichten der Beispielanwendung lokal, um den Fluss der Web-Push-Benachrichtigungen mit AJO zu untersuchen.
feature: Push
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-04-21T00:00:00Z
jira: KT-20879
source-git-commit: 45f86aeb8fca071436785cc55225d853bb21998f
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---

# Lokales Ausführen der Anwendung

Auf dieser Seite werden Sie durch das lokale Einrichten der Beispielanwendung geführt, damit Sie den Web-Push-Benachrichtigungsfluss mit Adobe Journey Optimizer testen und untersuchen können. Sie klonen das Repository, konfigurieren Umgebungsvariablen und führen die Anwendung auf Ihrem lokalen System aus.


Führen Sie diese Schritte aus, um die Beispielanwendung auf Ihrem lokalen System auszuführen.

## &#x200B;1. Installieren von Node.js

Stellen Sie sicher, **Node.js (Version 16 oder höher)** auf Ihrem System installiert ist.

Sie können [hier herunterladen:](https://nodejs.org/)

Überprüfen der Installation

```node -v```

```npm -v```


## &#x200B;2. Klonen des Repositorys

```git clone https://github.com/gbedekar489/ajo-web-push.git```

```cd ajo-web-push```

## &#x200B;3. Installieren von Abhängigkeiten

```npm install```

## &#x200B;4. Konfigurieren von Umgebungsvariablen

Erstellen Sie eine .env-Datei im Stammverzeichnis und fügen Sie Folgendes hinzu:

```
DATASTREAM_ID=your_datastream_id
ORG_ID=your_org_id
VAPID_PUBLIC_KEY=your_vapid_public_key
APP_ID=your_app_id
DATASET_ID=your_profile_dataset_id
PORT=3000
```

Bei der lokalen Ausführung werden diese Werte aus der .env-Datei gelesen. In der Produktion (z. B. Render) werden sie als Umgebungsvariablen konfiguriert.