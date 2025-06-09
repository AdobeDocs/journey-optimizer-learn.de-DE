---
title: Testen der Lösung
description: Erstellen Sie eine einfache Web-Seite, um die kontextbezogene Personalisierung von Angeboten mithilfe von Echtzeit-Temperaturdaten zu testen.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-06-10T00:00:00Z
recommendations: noDisplay, noCatalog
jira: KT-18258
source-git-commit: a9fc14da78e1c67b01aef5dcdd417ce02d36d50a
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 1%

---

# Testen der Lösung

Eine Web-Seite wird erstellt, um die kontextuelle Personalisierung von Angeboten mithilfe von Echtzeit-Temperaturdaten zu testen. Wenn eine Benutzerin oder ein Benutzer die Seite besucht, fordert der Browser zur Eingabe des Zugriffs auf die Geolokalisierung auf. Nach der Genehmigung ruft die Seite die aktuellen Wetterdetails - wie Temperatur, Bedingung und Ort - über die OpenWeatherMap-API ab. Diese kontextuellen Daten werden Benutzenden angezeigt und mithilfe der Adobe Web SDK (Alloy) an Adobe Experience Platform gesendet.

Der sendEvent-Aufruf wird mit renderDecisions: false konfiguriert, d. h. die von Adobe Journey Optimizer zurückgegebenen Angebote werden manuell verarbeitet. Das Skript verarbeitet die Entscheidungsantwort, decodiert den Inhalt und fügt das relevanteste Angebot dynamisch in einen bezeichneten Container (#offerContainer) ein.

## Funktionsweise von JavaScript

Die JavaScript ruft Wetterinformationen basierend auf dem Standort der Benutzerin bzw. des Benutzers dynamisch ab und verwendet Adobe Experience Platform (AEP), um personalisierte Angebote bereitzustellen. Im Folgenden finden Sie eine Aufschlüsselung der Schritte:

1. **Wartet, bis Legierung geladen wird**

   Das -Skript stellt sicher, dass die Adobe Web SDK (Alloy) vollständig geladen ist, bevor Personalisierungsanfragen gestellt werden.

2. **Ruft den Standort des Benutzers ab**

   Sie verwendet die Geolocation-API des Browsers, um den aktuellen Breiten- und Längengrad des Benutzers abzurufen.

3. **Ruft Wetterdaten ab**

   Sie ruft die OpenWeatherMap-API auf, um aktuelle Wetterdetails zu erhalten:

   Temperatur (in °F)

   Wetterbedingungen (z. B. „Regen“, „Klar„)

   Name der Stadt

   Feuchtigkeit

4. **Anzeigen von Wetterinformationen auf der Webseite**

   Aktualisiert das DOM mit einer Meldung wie:

   „Die aktuelle Temperatur in San Diego liegt bei 72°F mit klarem Himmel.“

5. **Sendet Wetterkontext an AEP**

   Verwendet alloy(„sendEvent„), um kontextuelle Wetterdaten an AEP zu senden

   ```javascript
   xdm: {
   eventType: "decisioning.request",
   _techmarketingdemos: {
   temperature: temp,
   weatherConditions: condition,
   cityName: city
     }
   }
   ```

6. **Angebote abrufen und rendern**

   Empfängt von AJO zurückgegebene Angebote.

   Decodiert den HTML-Inhalt.

   fügt die Angebote dynamisch in die <div id="offerContainer"> Element.

7. **Beispiel für Assets**

   Die zum Testen der Lösung verwendete Webseite kann heruntergeladen werden

[Web-Seite](assets/weather-offers.html)

[JavaScript-Code](assets/weather-related-offers-script.js)

