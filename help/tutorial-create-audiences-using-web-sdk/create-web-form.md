---
title: Web-Formular erstellen
description: Erstellen Sie ein Formular auf Ihrer HTML-Seite, in dem Benutzer ihre Investitionsvoreinstellungen auswählen können
feature: Audiences
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-04-30T00:00:00Z
recommendations: noDisplay, noCatalog
jira: KT-17923
exl-id: 20de8dec-aac8-43ed-8305-e723f82a5dd9
source-git-commit: 163edfb3367d03729d68c9339ee2af4a0fe3a1b3
workflow-type: tm+mt
source-wordcount: '123'
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
