---
title: Testen der Lösung
description: Erstellen einer Journey zum Senden einer E-Mail bei Formularübermittlung
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-12-25T00:00:00Z
jira: KT-20014
source-git-commit: 043f41acd8f7f7165d9ec416d8f789f78d407ca1
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---

# Testen der Lösung


Testen der Lösung
>[!VIDEO](https://video.tv.adobe.com/v/3478546)

## Bereitstellen der Beispiel-Assets

Wenn Node.js nicht installiert ist, laden Sie es herunter und [ Sie es von hier](https://nodejs.org/)

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

* Erstellen Sie im Ordner `public` den Ordner `trigger-journey` .
* Entpacken Sie den Inhalt von [index.zip] in den öffentlichen Ordner
* Aktualisieren Sie die `.env` Datei mit den entsprechenden Werten. Diese Werte sind über den cURL-Befehl verfügbar, der beim Erstellen der HTTP-Source-Verbindung heruntergeladen wurde

## Server ausführen

Stellen Sie sicher, dass Sie sich im `trigger-journey` befinden.
Ausführen des `node server.js`
Lassen Sie Ihren Browser auf [Web-Seite](http://localhost:3000/) verweisen
Füllen Sie das Formular aus und senden Sie es ab. Die Journey wird ausgelöst und eine E-Mail wird an die im Formular eingegebene E-Mail-ID gesendet.


