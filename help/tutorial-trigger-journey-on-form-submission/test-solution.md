---
title: Testen der Lösung
description: Erstellen einer Journey zum Senden einer E-Mail bei Formularübermittlung
feature: Journeys
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-12-25T00:00:00.000Z
jira: KT-20014
exl-id: 9b4a3e0c-d153-4a6b-a7de-b926bd669f6a
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
    internal-label: Journeys
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: d4f3ee0d644b4f962763e6807f014efe132a9a05
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 1%
---
# Testen der Lösung


Testen der Lösung
>[!VIDEO](https://video.tv.adobe.com/v/3478546)

## Bereitstellen der Beispiel-Assets

Wenn Node.js nicht installiert ist, laden Sie es herunter und [&#x200B; Sie es von hier](https://nodejs.org/)

Überprüfen Sie die Installation, indem Sie Folgendes ausführen:

`node -v`

`npm -v`

## Einrichten des Projektordners

Erstellen Sie mithilfe der folgenden Befehle ein neues Verzeichnis für die Beispielanwendung:

`mkdir trigger-journey `

`cd trigger-journey`

## Initialisieren des Projekts

`npm init -y`

## Installieren der erforderlichen Frameworks

`npm install express dotenv axios cors`

## Asset-Dateien kopieren

* Entpacken Sie den Inhalt von [project-root.zip](assets/project-root.zip) und legen Sie ihn im `trigger-journey` ab.

* Erstellen Sie im Ordner `trigger-journey` den Ordner `public` .
* Aktualisieren Sie die `.env` Datei mit den entsprechenden Werten. Diese Werte sind über den cURL-Befehl verfügbar, der beim Erstellen der HTTP-Source-Verbindung heruntergeladen wurde.
* Entpacken Sie den Inhalt von [index.zip](assets/index.zip) in den `public` Ordner

## Server ausführen

Stellen Sie sicher, dass Sie sich im `trigger-journey` befinden.
Befehl ausführen `node server.js`
Verweisen Sie Ihren Browser auf [Web-Seite](http://localhost:3000/)
Füllen Sie das Formular aus und senden Sie es ab. Die Journey wird ausgelöst und eine E-Mail wird an die im Formular eingegebene E-Mail-ID gesendet.
