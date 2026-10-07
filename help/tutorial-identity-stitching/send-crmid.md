---
title: Beispielanwendung zur Nachahmung der Anmeldeaktivität erstellen
description: Erstellen einer Node.js-Beispielanwendung zur Simulation eines Anmeldeflusses
feature: Profiles
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-19T00:00:00.000Z
recommendations: noDisplay, noCatalog
jira: KT-18089
exl-id: e080149c-0ac0-4559-b99d-ebad9f03b98b
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: d2971708-e780-44bb-9e2a-72f139796afd
    internal-label: Customer
subfeature_v2:
  - id: ef9a83ca-eefa-47cf-aa34-f1a34715583a
    internal-label: Profiles
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: d4f3ee0d644b4f962763e6807f014efe132a9a05
workflow-type: tm+mt
source-wordcount: '208'
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

Das Adobe Experience Platform-Tags-Skript wird mithilfe eines `<script>`-Tags in den `<head>` der HTML-Seite eingefügt:

`<script src="https://assets.adobedtm.com/b5eu4857867/4e4d84957/launch-b69e276bb9b5-development.min.js" async crossorigin="anonymous"></script>`

Das AEP Tags-Skript wurde abgerufen, indem eine im vorherigen Schritt erstellte Web-SDK-fähige Eigenschaft veröffentlicht und der Einbettungs-Code aus der Registerkarte Umgebungen kopiert wurde.
