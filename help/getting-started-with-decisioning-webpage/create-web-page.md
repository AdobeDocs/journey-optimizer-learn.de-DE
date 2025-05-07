---
title: Erstellen einer Web-Seite zum Testen der Lösung
description: Webseite zum Testen der personalisierten Angebote, die mithilfe von Decisioning bereitgestellt werden.
role: User
level: Beginner
doc-type: Tutorial
feature: Decisioning
last-substantial-update: 2025-05-05T00:00:00Z
jira: KT-17728
source-git-commit: 9695a4db0d0caa44a8c7d49e069320309ffc40a6
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---


# Erstellen einer Web-Seite zum Testen der Lösung

Diese Web-Seite wurde erstellt, um personalisierte Angebote zu testen, die über Adobe Journey Optimizer Decisioning bereitgestellt werden. Sie bietet eine kontrollierte Umgebung, in der der sendEvent-Aufruf ausgelöst und der zurückgegebene Angebotsinhalt gerendert werden kann, was bei der Validierung der End-to-End-Personalisierungseinrichtung hilft und sicherstellt, dass die Entscheidungsfindung wie erwartet funktioniert.

Das folgende Skript ist für das Abrufen und Anzeigen eines personalisierten Angebots auf einer Web-Seite mithilfe von Adobe Journey Optimizer verantwortlich.

1. HTML-Entitäten decodieren: Es gibt eine Hilfsfunktion, die alle Sonderzeichen im Angebotsinhalt sicher in lesbare HTML konvertiert.

2. Personalisierung ausführen:
Beim Aufruf wird eine Anfrage (sendEvent) an den Web-SDK von Adobe gesendet, um personalisierte Inhalte für einen bestimmten Bereich der Seite (das #ajo-offer) zu erhalten.
Wenn ein Angebot zurückgegeben wird, decodiert es die HTML und fügt es in die Seite ein.
Wenn nichts zurückgegeben wird, wird eine Warnung protokolliert.

3. Warten Sie auf die SDK:
Da Adobes SDK (Legierung) asynchron geladen wird, wartet das Skript, bis es vollständig geladen ist, bevor es die Anfrage stellt.
Es prüft alle 200 Millisekunden bis zu 20 Mal auf Legierung, um Fehler zu vermeiden.

4. Beim Laden der Seite: Nach Abschluss des Ladevorgangs startet das Skript den Prozess, indem es waitForAlloy() aufruft.



```javascript
< script >
    function decodeHtmlEntities(html) {
        const txt = document.createElement("textarea");
        txt.innerHTML = html;
        return txt.value;
    }


function runPersonalization() {
    console.log("🚀 Sending personalization request to AJO...");
    alloy("sendEvent", {
        renderDecisions: true,
        personalization: {
            surfaces: ["#ajo-offer"]
        }
    }).then(result => {
        console.log("🔍 Web SDK decision response:", result);

        const decision = result.propositions?.[0];
        const html = decision?.items?.[0]?.data?.content;

        const container = document.getElementById("ajo-offer");
        if (html && container) {
            const decodedHtml = decodeHtmlEntities(html);
            console.log("✅ Offer HTML content (decoded):", decodedHtml);
            container.innerHTML = decodedHtml;
        } else {
            console.warn("⚠️ No personalized offer returned.");
        }


    }).catch(error => {
        console.error("❌ sendEvent failed:", error);
    });
}

function waitForAlloy(callback, retries = 20) {
    if (typeof alloy === "function") {
        callback();
    } else if (retries > 0) {
        console.log("⌛ Waiting for Alloy...");
        setTimeout(() => waitForAlloy(callback, retries - 1), 200);
    } else {
        console.error("❌ alloy is not loaded after waiting.");
    }
}

// Trigger initial personalization on page load
document.addEventListener("DOMContentLoaded", function() {
    waitForAlloy(() => runPersonalization());
}); <
/script>
```

[Die Beispiel-HTML-Seite und zugehörige Assets können hier heruntergeladen werden](assets/web-page-assets.zip)