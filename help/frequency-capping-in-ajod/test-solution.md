---
title: Testen der Lösung
description: Erstellen Sie eine einfache Web-Seite, um Impressions- und Klick-Ereignisse auf die Angebote zu erfassen.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-07-18T00:00:00.000Z
recommendations: noDisplay, noCatalog
jira: KT-18526
exl-id: 6b6c66d3-218d-4f5b-adb0-a2eca05989ab
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: a984631b-2bae-4860-9b15-69c41a799dcb
    internal-label: APIs and SDKs
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
    internal-label: Decisioning API
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: d4f3ee0d644b4f962763e6807f014efe132a9a05
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 2%
---
# Testen der Lösung

## Bereitstellen der Beispiel-Assets

Wenn Node.js nicht installiert ist, laden Sie es herunter und [ Sie es von hier](https://nodejs.org/)

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
