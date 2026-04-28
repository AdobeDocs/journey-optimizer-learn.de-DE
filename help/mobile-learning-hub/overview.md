---
title: Mobiler Lern-Hub
description: The mobile learning hub equips developers, administrators, marketers, and analysts with everything needed to configure inbound and outbound mobile channels and integrate them seamlessly into powerful cross-channel campaigns and journeys in Journey Optimizer.
feature: Overview
role: User, Admin, Developer
hide: false
index: true
jira: KT-19860
last-substantial-update: 2025-12-18T00:00:00Z
exl-id: f0612a1d-f919-4b67-9e33-a9fb623062dc
source-git-commit: 3917e11cdf8c0450c19ce653a0964f6dc9da6a3c
workflow-type: tm+mt
source-wordcount: '944'
ht-degree: 7%

---

# Journey Optimizer - Mobile Learning Hub

Bauen Sie auf Adobe Journey Optimizer, um Ihre mobile Interaktionsstrategie sofort umzusetzen oder aufzuwerten. Der mobile Lern-Hub bietet Entwickelnden, Admins, Marketing-Fachleuten sowie Analystinnen und Analysten alles, was sie für die Konfiguration eingehender und ausgehender mobiler Kanäle benötigen, und integriert diese Kanäle nahtlos in leistungsstarke Cross-Channel-Kampagnen und -Journeys.

Explore best practices, learn how to drive adoption, and setup centralized reporting workflows — all in one place — to deliver impactful, data-driven mobile experiences that reach customers anytime, anywhere.

>[!VIDEO](https://video.tv.adobe.com/v/3477007?captions=ger&quality=12&learn=on){transcript=true}


## Mobile channel overview

Journey Optimizer supports both inbound and outbound mobile channels:

### Outbound-Kanäle

Outbound channels let you proactively deliver messages to customers without requiring a prior interaction. These interactions are ideal for campaigns, promotions, or transactional events.

All outbound channels in Adobe Journey Optimizer enforce Custom Consent Policies at message send time. If consent is not granted for a specific marketing action, the message is automatically suppressed to ensure compliant delivery.

| ![Push Notifications](/help/mobile-learning-hub/assets/mobile-phone.webp){width=&quot;250&quot;, height=&quot;250&quot;}<br> **[Push Notifications](/help/mobile-learning-hub/channels/push-notifications-overview.md)** | ![SMS/MMS/RCS](/help/mobile-learning-hub/assets/SMS.png){width=&quot;250&quot;, height=&quot;250&quot;}<br> **[SMS / MMS / RCS](/help/mobile-learning-hub/channels/sms-mms-rcs-overview.md)** | ![WhatsApp](/help/mobile-learning-hub/assets/whatsapp.webp){width=&quot;250&quot;, height=&quot;250&quot;}<br> **[WhatsApp](/help/mobile-learning-hub/channels/whatsapp-overview.md)** |
|-------------------------------------|------------------------------------|-------------------------------|
| Sent outside the app, push messages grab attention immediately. They&#39;re ideal for time-sensitive updates and encouraging users to return to your app. | Direct messages sent to users&#39; mobile phones without needing the app. Great for urgent alerts, reminders, and rich media content like images or videos. | Conversational channel through a widely used messaging app, allowing personalized, two-way communication and interactive campaigns. |

### Eingehende Kanäle

Inbound channels support customer-initiated interactions, allowing you to deliver personalized experiences the moment users engage with your brand. They enable real-time personalization and data capture—such as landing page forms or on-site behaviors—that feed directly into Adobe Experience Platform (AEP) for segmentation, targeting, and activation across journeys.


| ![In-App Messages](/help/mobile-learning-hub/assets/frescopa-in-app.png){width=&quot;250&quot;,height=&quot;50%&quot;}<br> **[In-App Messages](/help/mobile-learning-hub/channels/in-app-messages-overview.md)** | ![Content Cards](/help/mobile-learning-hub/assets/content-card.jpeg){width=&quot;250&quot;, height=&quot;250&quot;}<br> **[Content Cards](/help/mobile-learning-hub/channels/content-cards-overview.md)** | ![Code-basiertes Erlebnis](/help/mobile-learning-hub/assets/code-based.png){width=„250“, height=„250“}<br> **[Code-basiertes Erlebnis](/help/mobile-learning-hub/channels/code-based-experience-overview.md)** |
|-------------------------------------|------------------------------------|-------------------------------|
| Diese Nachrichten werden bereitgestellt, während Benutzende Ihre App aktiv verwenden, und sind in Echtzeit und interaktiv. Sie eignen sich perfekt, um Kunden im Moment anzusprechen. | Benutzerinnen und Benutzer können jederzeit innerhalb der App auf nicht aufdringliche, persistente Nachrichten zugreifen. Inhaltskarten eignen sich gut für die Freigabe fortlaufender Angebote oder hilfreicher Informationen. | Benutzerdefinierte Nachrichten ermöglichen hochgradig personalisierte und dynamische Kampagnen, die Echtzeitdaten und komplexe Journey von Kunden integrieren. |


### Wie können mobile Kanäle zusammenarbeiten?

Durch die Kombination dieser Kanäle können Sie ein nahtloses und effektives Kundenerlebnis schaffen:

1. Verwenden Sie [Push-Benachrichtigungen](/help/mobile-learning-hub/channels/push-notifications-overview.md), um schnell Aufmerksamkeit zu erregen und Benutzer zurück zu Ihrer App zu bringen (z. B. „Der Verkauf beginnt jetzt!„).

2. Senden Sie [In-App-Nachrichten](/help/mobile-learning-hub/channels/in-app-messages-overview.md) mit personalisierten Werbeaktionen (z. B. „Hier ist Ihr Rabatt von 15 % für den heutigen Verkauf„).

3. Bieten Sie [Inhaltskarten](/help/mobile-learning-hub/channels/content-cards-overview.md) damit Benutzer die Promotion jederzeit vor Ablauf erneut aufrufen können (z. B. „Ihr Rabatt von 15 % endet am Freitag„).

4. Verwenden Sie [SMS/MMS/](/help/mobile-learning-hub/channels/sms-mms-rcs-overview.md)), um rechtzeitig Erinnerungen oder Rich-Media-Angebote direkt an Benutzer zu senden, die sich nicht in der App befinden.

5. Engagieren Sie Kunden in aussagekräftige Gespräche über [WhatsApp](/help/mobile-learning-hub/channels/whatsapp-overview.md), ideal für Kunden-Support oder interaktive Kampagnen.

6. Nutzen Sie [Code-basierte Erlebnisse](/help/mobile-learning-hub/channels/code-based-experience-overview.md) um jede Nachricht auf der Grundlage des Benutzerverhaltens und der Voreinstellungen anzupassen und so eine wirklich personalisierte Journey kanalübergreifend zu erstellen.

## Fundament aufbauen

Lernen Sie die Konzepte und Gewusst wie

<table style="table-layout:fixed">
  <tr style="border: 0;">
    <td>
    <a href="configure-and-launch.md"><img src="./assets/configure-message.jpg"></a>
    <div><strong>Konfigurieren und starten</strong><br/> Konfigurieren der mobilen Kanäle und Integration mit mobilen Apps.</div>
    </td>
    <td>
    <a href="design-and-deliver.md"><img src="./assets/create-message.webp"></a>
    <div><strong>Entwerfen und bereitstellen</strong><br/>Verwenden Sie mobile Kanäle, um personalisierte Journey und Kampagnen zu erstellen, die Kundinnen und Kunden in Echtzeit ansprechen.</div>
    </td>
    <td>
    <a href="measure-and-optimize.md"><img src="./assets/reports.webp"></a>
    <div><strong>Messen und Optimieren</strong><br/> Zugreifen auf Berichte, Analysieren der Leistung und Verfeinern von Strategien für bessere Ergebnisse.
    </div>
    </td>
  </tr>
</table>

## Gängige Anwendungsfälle für mobile Unternehmen

| Anwendungsfall | Beschreibung | Mobile Kanalnutzung |
|---------|-------------|----------------------|
| **App-Onboarding und -Übernahme** | Führt neue Benutzer durch die ersten Schritte der App-Interaktion: Installation der App, Abschluss der Einrichtung und Erkennung wichtiger Funktionen. Ziel ist es, die Kundenbindung und langfristige Nutzung zu maximieren. | - Push-Benachrichtigungen und SMS heißen Benutzer willkommen und sorgen für eine sofortige Profilfertigstellung.<br>- In-App-Nachrichten heben Funktionen hervor und ermutigen zu ersten Aktionen.<br>- Deep-Links in E-Mails oder Anzeigen leiten Benutzer zu bestimmten App-Bildschirmen, um ein nahtloses Onboarding zu ermöglichen. |
| **standortbasierte Interaktion** | Stellt personalisierte, zeitnahe Nachrichten für Benutzer bereit, die auf deren physischer Nähe zu Geschäften, Ereignissen oder anderen relevanten Orten basieren. | - Geofencing- und Beacon-Tech-Trigger-Push-Benachrichtigungen, wenn Benutzende in Zielzonen eintreten.<br>- SMS/MMS stellen lokalisierte Angebote und Updates bereit.<br>- In-App-Banner und -Karten passen Inhalte basierend auf dem Echtzeit-Standort an. |
| **Rückgewinnung bei Abbruch** | Targeting von Benutzenden, die Warenkorb-, Formular- oder Browsersitzungen verlassen, um sie zurückzuholen und die beabsichtigte Aktion abzuschließen. | - Push-Benachrichtigungen erinnern Benutzer an abgebrochene Warenkörbe oder unvollständige Aktionen.<br>- SMS-Folgenachrichten enthalten Anreize oder direkte Links zur Wiederaufnahme.<br>- Bei der Rückkehr von Benutzern werden In-App-Aufforderungen angezeigt, die personalisierte Empfehlungen bieten. |
| **Upsell- und Crosssell-Kampagnen** | Werbt für zusätzliche Produkte oder Upgrades bei Bestandskunden auf der Grundlage ihres Verhaltens, ihrer Voreinstellungen oder ihres Kaufverlaufs. | - Push-Benachrichtigungen heben relevante Upsell-Möglichkeiten hervor.<br>- In-App-Nachrichten und -Inhaltskarten präsentieren komplementäre Elemente.<br>- SMS-Kampagnen zielen mit exklusiven Angeboten auf segmentierte Zielgruppen ab. |
| **Abwanderungsprävention** | Identifiziert Benutzende, die das Risiko haben, das System zu verlassen, und setzt personalisierte Aufbewahrungsstrategien ein, um ihre Loyalität zu wahren. | - Mobile Kontaktaufnahme mit Predictive Analytics-Triggern zu gefährdeten Benutzern.<br>- Push-Benachrichtigungen und SMS bieten Treueprämien oder personalisierte Inhalte.<br>- In-App-Umfragen sammeln Feedback zur Verbesserung der Aufbewahrungsstrategien. |
| **Multi-Channel-Messaging** | Orchestriert konsistentes Messaging über mehrere mobile Kanäle, um sicherzustellen, dass Benutzer zeitnahe und relevante Nachrichten erhalten. | - Push-, In-App-, SMS- und E-Mail-Nachrichten werden für Unified Messaging koordiniert.<br>- SDKs ermöglichen die kanalübergreifende Echtzeit-Personalisierung.<br>- Inhaltskarten bleiben sitzungsübergreifend bestehen, um wichtige Botschaften zu untermauern. |

## Kunden-Anwendungsfälle

* [Personalisierung im Flug: Wie Fluggesellschaften Angebote mit Adobe Journey Optimizer erhöhen können (Blog)](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/take-flight-with-personalization-how-airlines-can-elevate-offers/ba-p/767513?profile.language=de)
