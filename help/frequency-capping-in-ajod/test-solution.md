---
title: Testen der Lösung
description: Erstellen Sie eine einfache Web-Seite, um Impressions- und Klick-Ereignisse auf die Angebote zu erfassen.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-07-18T00:00:00Z
recommendations: noDisplay, noCatalog
jira: KT-18526
exl-id: 6b6c66d3-218d-4f5b-adb0-a2eca05989ab
source-git-commit: bef6d831c639d40514552dae3ff20132626a4a09
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 1%

---

# Testen der Lösung

## Bereitstellen der Beispiel-Assets

Wenn Node.js nicht installiert ist, laden Sie es herunter und [&#x200B; Sie es von hier](https://nodejs.org/)

Überprüfen Sie die Installation, indem Sie Folgendes ausführen:

`node -v`

`npm -v`

## Einrichten des Projektordners

Erstellen Sie mithilfe der folgenden Befehle ein neues Verzeichnis für die Beispielanwendung:

`mkdir frequency-capping `

`cd frequency-capping `

## Initialisieren des Projekts

`npm init -y`

## Installieren der erforderlichen Frameworks

`npm install express`

## Asset-Dateien kopieren

* Entpacken Sie den Inhalt von [server.zip](assets/server.zip) und legen Sie ihn im Ordner `frequency-capping` ab.
* Extrahieren Sie den Inhalt von [public.zip](assets/public.zip) in den Ordner „frequency-capping“

## Aktualisieren der Oberflächen-URL in der JavaScript-Datei

Öffnen Sie die `frequency-capping.js` im `public\scripts` und aktualisieren Sie die Eigenschaft „Oberflächen“ so, dass sie mit der in der Kampagne verwendeten Kanalkonfiguration übereinstimmt

## JS-Server des Startknotens

Navigieren Sie zum Ordner `c:\frequency-capping` . Führen Sie den `node server.js` Befehl aus, um den Node-JS-Server auf Port 3000 zu starten.


## Aktualisieren der Adobe Experience Platform Tags-Eigenschaft

Öffnen Sie die `frequency-capping.html` im Ordner `public` im Texteditor und ersetzen Sie das Skript-Tag durch das Skript-Tag Ihrer Adobe Experience Platform-Tag-Eigenschaft, das Sie im vorherigen Schritt dieses Tutorials erstellt haben. Speichern Sie die Datei

```
<script src="https://assets.adobedtm.com/AEM_TAGS/launch-ENabcd1234.min.js" async></script>
```

## Interagieren mit Angeboten

* Öffnen Sie die [Webseite](http://localhost:3000) in Ihrem bevorzugten Browser.
* Interagieren mit dem Angebot
* Die Seite aktualisieren
* Abhängig von den Regeln zur Frequenzlimitierung sollte Ihnen ein neues Angebot angezeigt werden

## Anzeigen des Berichts

* Bei Journey Optimizer anmelden
* Navigieren Sie zu Journey-Verwaltung > Kampagnen
* Klicken Sie auf die Kampagne und wählen Sie dann den entsprechenden Bericht aus dem Menü Bericht .
