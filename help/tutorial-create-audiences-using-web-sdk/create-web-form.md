---
title: Web-Formular erstellen
description: Erstellen Sie ein Formular auf Ihrer HTML-Seite, in dem Benutzer ihre Investitionsvoreinstellungen auswählen können
feature: Audiences
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-04-30T00:00:00.000Z
recommendations: noDisplay, noCatalog
jira: KT-17923
exl-id: 20de8dec-aac8-43ed-8305-e723f82a5dd9
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: d2971708-e780-44bb-9e2a-72f139796afd
    internal-label: Customer
subfeature_v2:
  - id: b32bb433-f8c6-4931-8e52-e657230a3bf2
    internal-label: Audiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: d4f3ee0d644b4f962763e6807f014efe132a9a05
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%
---
# Web-Formular erstellen

Das folgende HTML-Formular wurde erstellt, um die Benutzereinstellungen zu erfassen
![html-form](assets/web-form.png)

Wenn ein(e) Benutzende(r) auf die Schaltfläche auf der Web-Seite klickt, werden seine/ihre ausgewählten finanziellen Präferenzen (wie Aktien, Anleihen oder CDs) erfasst und in die Adobe-Datenschicht verschoben. Dieses Ereignis (assetClassSelection) speichert die Auswahl des Benutzers in Echtzeit. Adobe Launch überwacht dann dieses Ereignis, ruft die ausgewählte Anlageoption (PreferredFinancialInstrument) ab und kann Trigger-Aktionen ausführen, z. B. die Daten an Adobe Experience Platform (AEP) senden oder Personalisierungsregeln aktualisieren

Die folgende JavaScript wurde für die Verarbeitung der Formularübermittlung geschrieben

```javascript
function handleSubmission() {
  window.adobeDataLayer = window.adobeDataLayer || [];

  const selectedAssetClass = document.querySelector('input[name="assetclass"]:checked');
  const errorMessage = document.getElementById("error-message");
  const messageBox = document.getElementById("message");

  if (!selectedAssetClass) {
    errorMessage.textContent = "Please select a financial instrument.";
    messageBox.textContent = "";
    return;
  }

  errorMessage.textContent = "";

  const subscriptionEvent = {
    event: "assetClassSelection",
    xdm: {
      eventType: "assetClassSelection",
      eventID: "investment_preference_event",
      timestamp: new Date().toISOString(),
      FinancialInterest: {
        PreferredFinancialInstrument: selectedAssetClass.value
      }
    }
  };

  console.log("📩 Sending asset class data to AEP:", subscriptionEvent);
  window.adobeDataLayer.push(subscriptionEvent);

  // ✅ Show thank-you message
  messageBox.textContent = `Thank you for selecting "${selectedAssetClass.value}". We'll use this to personalize your experience.`;
}
```

[Das Beispiel-Formular für HTML wird im Rahmen dieses Tutorials bereitgestellt](assets/webform.zip)
