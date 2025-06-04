---
title: Erstellen einer Web-Seite zum Testen der Projektmappe
description: Webseite zum Testen der personalisierten Angebote, die mithilfe von Decisioning bereitgestellt werden.
role: User
level: Beginner
doc-type: Tutorial
feature: Decisioning
last-substantial-update: 2025-05-31T00:00:00Z
jira: KT-18188
recommendations: noDisplay, noCatalog
exl-id: 6b1eec78-153c-4ea5-acfe-2dcc6f1e6078
source-git-commit: 82d82b3aac2bf91e259b01fd8c6b4d6065f9640a
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---

# Erstellen einer Web-Seite zum Testen der Projektmappe

Diese Beispielanwendung simuliert einen realen Anmeldefluss, bei dem die Benutzeranmeldeinformationen Server-seitig validiert werden, bevor die CRM-ID an Adobe Experience Platform (AEP) gesendet wird. Ein lokaler Node.js-Server wird verwendet, um die Web-Seiten sicher bereitzustellen, grundlegende Authentifizierungslogik zu verarbeiten und Browser-Einschränkungen zu vermeiden (z. B. blockierter lokaler Dateizugriff oder fehlende CORS-Header), die die Funktionalität von Adobe Launch oder Web SDK beeinträchtigen könnten. Dadurch wird sichergestellt, dass das Erlebnis näher an einer echten Produktionsumgebung liegt.

Personalisierte Angebote werden erst angezeigt, nachdem sich der Benutzer angemeldet hat. Ab diesem Zeitpunkt ist die Identitätszuordnung zwischen der CRM-ID des Benutzers und der ECID (Experience Cloud-ID) abgeschlossen. Diese Identitätszuordnung stellt sicher, dass Adobe Journey Optimizer (AJO) das Profil genau erkennen und zielgerichtete Angebote zurückgeben kann.

Nach erfolgreicher Anmeldung wird eine Personalisierungsanfrage an AJO gesendet, um verfügbare Angebote für den Benutzer abzurufen. Diese Angebote werden als HTML-Fragmente zurückgegeben, die jeweils mit einem Attribut für Daten-Tags eingebettet sind - z. B. data-tags=„ajo offer-vacation-based cd zip-92128 come-high“ - und den Angebotsnamen sowie Segmentierungsdetails wie Postleitzahl und Einkommensstufe enthalten.

JavaScript analysiert diese HTML-Blöcke und legt sie jeweils in einen Karussellelement-Container ein. Die Elemente werden horizontal innerhalb einer Karussellspur angeordnet, was eine wischbare Navigation ermöglicht. Mit den Schaltflächen Zurück und Weiter (◀ und ▶) können Benutzer die personalisierten Angebote einzeln durchblättern.

Diese Einrichtung bietet ein responsives und maßgeschneidertes Erlebnis, sodass jeder Benutzer Angebote sieht, die für sein Finanzprofil relevant sind - erst nachdem seine Identität plattformübergreifend sicher zugeordnet wurde.

## Diese Lösung testen

* Erstellen Sie einen Ordner mit dem Namen „ranking-Formula“ innerhalb Ihres vorhandenen Node.js-Projekts.

* Entpacken Sie die [bereitgestellten Dateien in diesen Ordner mit Rangfolgeformeln.](assets/ranking-formula.zip)

* Führen Sie die App aus, indem Sie zum Ordner navigieren und den Server starten:
   * `cd ranking-formula`

   * `node server.js`


* Öffnen Sie Ihren Browser und navigieren Sie zu http://localhost:3000/formula.html.

* Anmelden mit alice/pass123

Da sich Alice in der 92128 Postleitzahl befindet, werden auf diesen Ort zugeschnittene Angebote angezeigt.
