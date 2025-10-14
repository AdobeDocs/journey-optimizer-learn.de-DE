---
title: Beispielanwendung zur Nachahmung der Anmeldeaktivität erstellen
description: Erstellen einer Node.js-Beispielanwendung zur Simulation eines Anmeldeflusses
feature: Profiles
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-19T00:00:00Z
recommendations: noDisplay, noCatalog
jira: KT-18089
exl-id: e080149c-0ac0-4559-b99d-ebad9f03b98b
source-git-commit: 667f146639635515a5572e9ace41d83ab4452bb8
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# Beispielanwendung zur Nachahmung der Anmeldeaktivität erstellen

Diese Beispielanwendung, die auf einem Node.js-Server erstellt und bereitgestellt wird, zeigt, wie eine CRM-ID an Adobe Experience Platform (AEP) gesendet wird, wenn sich ein Benutzer anmeldet. Das Programm simuliert einen Anmeldefluss, bei dem die Benutzeranmeldeinformationen Server-seitig validiert werden. Nach erfolgreicher Anmeldung wird die CRM-ID des Benutzers abgerufen und an die adobeDataLayer gepusht. Dadurch wird eine entsprechende Regel in Adobe Experience Platform Tags (ehemals Adobe Launch) ausgelöst.

Mit der Funktion attachloginHandler wird ein Ereignis-Listener für das Senden an ein Anmeldeformular angefügt. Bei der Übermittlung des Formulars verhindert sie die Standardaktion, validiert die Anmeldeinformationen anhand des -Objekts eines vordefinierten Benutzers und ruft die CRM-ID ab, sofern gültig. Die Funktion übergibt ein userLoggedIn-Ereignis mit der CRM-ID und dem Authentifizierungsstatus an die adobeDataLayer und Adobe Experience Platform Tags nimmt es auf, um die Daten an Adobe Experience Platform (AEP) zu senden.


```javascript
function attachLoginHandler() {
    const form = document.getElementById("loginForm");
    if (!form) return;

    form.addEventListener("submit", function(e) {
        e.preventDefault();
        const username = document.getElementById("username").value;
        const password = document.getElementById("password").value;

        if (users[username] && users[username].password === password) {
            const crmid = users[username].crmid;
            window.adobeDataLayer = window.adobeDataLayer || [];
            debugger;
            window.adobeDataLayer.push({
                event: "UserLoggedIn",
                user: {
                    crmid: crmid,
                    authenticatedState: "authenticated"
                }
            });
        }
    });
}
```

Das Adobe Experience Platform-Tags-Skript wird mithilfe eines `<head>`-Tags in den `<script>` der HTML-Seite eingefügt:

`<script src="https://assets.adobedtm.com/b5eu4857867/4e4d84957/launch-b69e276bb9b5-development.min.js" async crossorigin="anonymous"></script>`

Das AEP Tags-Skript wurde abgerufen, indem eine im vorherigen Schritt erstellte Web-SDK-fähige Eigenschaft veröffentlicht und der Einbettungs-Code aus der Registerkarte Umgebungen kopiert wurde.
