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
source-git-commit: 69bc8aace3cc502a18e691584824176833413c7e
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---

# Testen der Lösung

Um die Lösung durchgängig zu testen, müssen die Dateien [weather-offers.html](assets/weather-offers.html) und [collection-impressions-click-events.js](assets/capture-impressions-click-events.js) auf einem Webserver oder einem öffentlichen Hosting-Service wie Github Pages gehostet werden. Dies ist erforderlich, da die Geolocation-API des Browsers nur über HTTPS oder localhost funktioniert

## Herunterladen der bereitgestellten Dateien

[HTML-Datei](assets/weather-offers.html)

[JavaScript-Datei](assets/capture-impressions-click-events.js)

## Aktualisieren der Oberflächen-URL in der JavaScript-Datei

Öffnen Sie die `capture-impressions-click-events.js` und aktualisieren Sie die ` "web://yourdomain.com/weather/weather-offers.html#offerContainer"`, indem Sie `yourdomain.com` durch die tatsächliche Domain ersetzen, in der die HTML-Datei gehostet wird.


## Aktualisieren der Adobe Experience Platform Tags-Eigenschaft

Öffnen Sie die Datei „weather-offers.html“ im Texteditor und ersetzen Sie das Skript-Tag durch das Skript-Tag Ihrer Adobe Experience Platform-Tag-Eigenschaft, das im vorherigen Schritt dieses Tutorials erstellt wurde. Speichern Sie die Datei

```
<script src="https://assets.adobedtm.com/AEM_TAGS/launch-ENabcd1234.min.js" async></script>
```

## Interagieren mit Angeboten

- Öffnen Sie die Webseite in Ihrem bevorzugten Browser.

- _&#x200B;**Standortverfolgung**&#x200B;_ zulassen. Dies ist erforderlich, um die Wetterdetails basierend auf Ihrem Standort zu erhalten.

- Klicken Sie auf die Schaltfläche im Ereignis Interaktionsangebote an Trigger .

## Anzeigen des Berichts

- Bei Journey Optimizer anmelden

- Navigieren Sie zu Journey-Verwaltung > Kampagnen

- Klicken Sie auf die Kampagne und wählen Sie dann den entsprechenden Bericht aus dem Menü Bericht .
