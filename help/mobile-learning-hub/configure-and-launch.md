---
title: Konfigurieren und starten
description: Konfigurieren Sie die mobilen Kanäle in Adobe Journey Optimizer (AJO) und Adobe Experience Platform (AEP), integrieren Sie sie mit mobilen Apps und stellen Sie sicher, dass sie für die Ausführung von Marketing-Kampagnen bereit sind.
feature: Overview
role: Developer, Admin
level: Beginner, Intermediate
hide: true
index: false
last-substantial-update: 2025-08-22T00:00:00Z
exl-id: d8ffe406-b54b-455f-bd41-7d1fef0a4714
source-git-commit: 6faf1e92516a54afa9c987b693a27d2284726fff
workflow-type: tm+mt
source-wordcount: '2549'
ht-degree: 15%

---


# Konfigurieren und starten

Für **Administratoren** und **Entwickler mobiler Apps** wird in diesem Abschnitt gezeigt, wie Sie mobile und Web-Kanäle in Adobe Journey Optimizer konfigurieren und starten. Es behandelt Voraussetzungen, Berechtigungen und Platform-Unterstützung und führt Sie dann durch die Erstellung App-spezifischer Konfigurationen.

>[!IMPORTANT]
>
> Wenn Sie neu bei Journey Optimizer und Experience Platform sind, machen Sie sich mit den grundlegenden Konzepten des Daten-Managements in Journey Optimizer vertraut, indem Sie diesen Kurs absolvieren:
>
> [Engineeringdaten für die intelligente Journey-Aktivierung in Adobe Journey Optimizer](https://experienceleague.adobe.com/de/courses/ajo-engineer-data-for-intelligent-journey-activation){target="_blank"}
>
>*Erfahren Sie, wie Sie Echtzeit-Kundenprofildaten für Journey Optimizer mithilfe von Experience Platform einrichten und verwalten. Machen Sie sich mit Datenmodellierung, Identitätszuordnung und Datenaufnahme vertraut, um einheitliche Journey für personalisierte Kundenprofile zu erstellen.*


## Mobile-Funktionen in Adobe Journey Optimizer

Erfahren Sie, welche mobilen Funktionen Adobe Journey Optimizer für Entwickler, Marketing-Experten und Produkt-Teams bietet, einschließlich Push-Messaging, In-App-Messaging und Personalisierung von Inhalten.

>[!VIDEO](https://video.tv.adobe.com/v/3409520?captions=ger&quality=12&learn=on){transcript=true}


## Mobile SDK- und App-Konfiguration

Mobile-Implementierungen in Journey Optimizer beginnen mit der **Adobe Experience Platform Mobile SDK**-Integration in Ihrer App. SDKs sind für die Datenerfassung und die Interaktion mit Adobe Experience Platform (AEP) und seinen Anwendungen wie Adobe Journey Optimizer (AJO) von entscheidender Bedeutung.

>[!PREREQUISITES]
>
>Vergewissern Sie sich, dass Sie Folgendes haben:
>
> - Adobe Journey Optimizer (AJO) für Ihre Organisation bereitgestellt.
> - Zugriff auf Adobe Experience Platform mit Datenerfassungs- und Journey Optimizer-Berechtigungen.
> - Administratorrechte in AJO für Kanal- und Konfigurationseinstellungen.
> - Zugriff auf den Quellcode Ihrer Mobile App (iOS, Android oder plattformübergreifendes Framework).
> - Für Ihre App sind die erforderlichen Funktionen auf Betriebssystemebene aktiviert (z. B. Push-Berechtigungen, Erweiterungen des Benachrichtigungs-Service, Hintergrundmodi).

Die mobile SDK:

- Sammelt App-Ereignisse (Bildschirmansichten, Tippen, Käufe, Lebenszyklus-Ereignisse usw.) und sendet sie an die **Adobe Experience Platform Edge Network**.
- Verwaltet **Identität** und **Einverständnis**, sodass Journey Optimizer Kundenprofile sicher erstellen und verwenden kann.
- Registriert und aktualisiert **Push-Token** und sendet **Push- und In-App-Tracking-Ereignisse** zurück an Adobe Experience Platform.
- lässt sich mit der **[Journey Optimizer Mobile](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer)** Erweiterung integrieren, damit Nachrichten durchgängig gesendet, gerendert und gemessen werden können.

Ohne die in Ihrer App integrierte Mobile SDK kann Journey Optimizer nicht zuverlässig:

- Versand und Tracking von Mobile-Push- und In-App-Nachrichten.
- Rendern und Verfolgen von Inhaltskarten.
- Verwenden Sie das In-App-Verhalten in Echtzeit, um Journey in Triggern zu erstellen und Erlebnisse zu personalisieren.

**[-> Hier klicken für die aktuellen SDK-Versionen](https://developer.adobe.com/client-sdks/home/current-sdk-versions/){target="_blank"}**

### Erforderliche Mobile SDK-Komponenten für Journey Optimizer

Um Journey Optimizer Mobile-Kanäle (Push, In-App, Inhaltskarten, Code-basierte Erlebnisse) zu verwenden, müssen Sie eine Reihe von **Core** und **Channel-spezifischen** in Ihrer Mobile App installieren und konfigurieren:

>[!BEGINTABS]

>[!TAB Core]

#### Haupterweiterungen (für alle Anwendungsfälle für Mobilgeräte erforderlich)

| Zweck | Beispiele für Erweiterungen (iOS/Android) | Anmerkungen |
|----------------------|-----------------------------------------------|-------|
| Event-Hub und -Services | Mobile Core/AEP Core, AEP Services | Foundation für alle anderen Erweiterungen. Bietet Ereignis-Hub, Netzwerk, Speicher und freigegebenen Status. |
| Edge Network | Adobe Experience Platform Edge Network | Sendet App-Ereignisse an Adobe Experience Platform Edge Network. |
| Identität | Identität für Edge Network | Verwaltet ECID und andere Identitäten, die für Profil und Segmentierung verwendet werden. |
| Einverständnis | Einverständnis für Edge Network | Sammelt Voreinstellungen für das Benutzereinverständnis und erzwingt diese. |
| Assurance | Adobe Experience Platform Assurance | Wird verwendet, um die SDK- und Kanalkonfiguration End-to-End zu validieren und zu debuggen. |

>[!TAB kanalspezifisch]

#### Kanalspezifische Erweiterungen für Journey Optimizer

| Kanal/Funktion | Zusätzliche wichtige Erweiterungen (zusätzlich zum Core) | Was sie ermöglichen |
|------------------------|---------------------------------------------------------------------|------------------|
| Push-Benachrichtigungen  | Journey Optimizer Mobile-Erweiterung (Push) | Push-Token registrieren und aktualisieren, Push-Tracking-Ereignisse senden, eine Verbindung zur AJO-Push-Konfiguration herstellen. |
| In-App-Messaging | Journey Optimizer Mobile-Erweiterung (In-App), Messaging-UI-Komponenten | Rufen Sie In-App-Nachrichten im Kontext ab und zeigen Sie sie an, senden Sie Impressionen und Interaktionsereignisse. |
| Inhaltskarten | Messaging SDK mit Unterstützung für Inhaltskarten | Abrufen, Rendern und Verfolgen von Inhaltskarten für präzise Journey Optimizer-Berichte. |
| Code-basierte Erlebnisse | Journey Optimizer/Decisioning-Erweiterungen oder Edge-Server-API | Entscheidungen für bestimmte „Oberflächen“ in Ihrer App abrufen; Ihre App steuert, wie Inhalte gerendert werden. |

>[!ENDTABS]

### Einrichten einer mobilen Tag-Eigenschaft

Erweiterungen werden in einer **mobilen Tag-Eigenschaft** in **Datenerfassung** konfiguriert.

Die Eigenschaft steuert:

- Welche Mobile SDK-Erweiterungen installiert sind.
- Welche Ereignisse in Ihrem App-Trigger die Edge Network aufrufen.
- Wie Daten in XDM zugeordnet und an Adobe-Lösungen (Journey Optimizer, Analytics usw.) weitergeleitet werden

Eine Eigenschaft ist ein Container, den Sie mit Erweiterungen, Regeln, Datenelementen und Bibliotheken füllen. Um diese Ressourcen zu verwenden, müssen Sie eine mobile Eigenschaft in der Datenerfassungs-Benutzeroberfläche erstellen und konfigurieren. Normalerweise wird für jede Mobile App, die verwaltet werden soll, eine Mobile-Eigenschaft erstellt.


Sie können [diese Mobile-Eigenschaft manuell erstellen und konfigurieren](https://experienceleague.adobe.com/de/docs/platform-learn/data-collection/tags/create-a-property){target="_blank"} oder für Mobile In-App und Push die [Geführte Kanaleinrichtung](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/web-and-mobile-channels/guided-channel-setup){target="_blank"} verwenden, um die erforderliche Tag-Eigenschaft, den Datenstrom und die Kanalkonfiguration für iOS und Android automatisch zu erstellen.

>[!TIP]
>  
> Für neue mobile In-App- und Push-Implementierungen **[Geführte Kanaleinrichtung](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/web-and-mobile-channels/guided-channel-setup){target="_blank"}** der empfohlene Ausgangspunkt. Dies reduziert das Risiko falsch konfigurierter Datenströme oder fehlender Erweiterungen und führt Sie durch die SDK-Validierung mit Assurance.


<!-- CARDS
* https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/web-and-mobile-channels/guided-channel-setup
 {description = Learn how to quickly set up and validate web and mobile channels across Experience Platform, Journey Optimizer, and Data Collection, and configure a push notification for a sample iOS marketing app.}
 * https://developer.adobe.com/client-sdks/home/getting-started/get-the-sdk
 * https://developer.adobe.com/client-sdks/home/base/assurance
 * https://experienceleague.adobe.com/de/docs/platform-learn/implement-mobile-sdk/overview 
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Guided channel setup">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/web-and-mobile-channels/guided-channel-setup" title="Geführte Kanaleinrichtung" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3449631/?captions=ger&format=jpeg&nocache=1764708699246" alt="Geführte Kanaleinrichtung"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/web-and-mobile-channels/guided-channel-setup" target="_blank" rel="referrer" title="Geführte Kanaleinrichtung">Anleitung zur Kanaleinrichtung</a>
                    </p>
                    <p class="is-size-6">Erfahren Sie, wie Sie schnell Web- und Mobile-Kanäle für Experience Platform, Journey Optimizer und die Datenerfassung einrichten und validieren und eine Push-Benachrichtigung für eine Beispiel-Marketing-App für iOS konfigurieren.</p>
                </div>
                <a href="https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/web-and-mobile-channels/guided-channel-setup" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Ansehen</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Get the Adobe Experience Platform Mobile SDK">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://developer.adobe.com/client-sdks/home/getting-started/get-the-sdk" title="Abrufen der Adobe Experience Platform Mobile SDK" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://developer.adobe.com/shared/images/adobe-social-share.png" alt="Abrufen der Adobe Experience Platform Mobile SDK"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://developer.adobe.com/client-sdks/home/getting-started/get-the-sdk" target="_blank" rel="referrer" title="Abrufen der Adobe Experience Platform Mobile SDK">Adobe Experience Platform Mobile SDK abrufen</a>
                    </p>
                    <p class="is-size-6">Ein Handbuch, in dem erläutert wird, wie Sie Adobe Experience Platform Mobile SDK in Ihrer Anwendung installieren.</p>
                </div>
                <a href="https://developer.adobe.com/client-sdks/home/getting-started/get-the-sdk" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Weitere Informationen</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Adobe Experience Platform Assurance overview">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://developer.adobe.com/client-sdks/home/base/assurance" title="Übersicht über Adobe Experience Platform Assurance" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://developer.adobe.com/shared/images/adobe-social-share.png" alt="Übersicht über Adobe Experience Platform Assurance"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://developer.adobe.com/client-sdks/home/base/assurance" target="_blank" rel="referrer" title="Übersicht über Adobe Experience Platform Assurance">Übersicht über Adobe Experience Platform Assurance</a>
                    </p>
                    <p class="is-size-6">Eine Übersicht über die Adobe Experience Platform Assurance Mobile-Erweiterung.</p>
                </div>
                <a href="https://developer.adobe.com/client-sdks/home/base/assurance" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Weitere Informationen</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Implement Adobe Experience Cloud in mobile apps tutorial">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/de/docs/platform-learn/implement-mobile-sdk/overview" title="Tutorial zur Implementierung von Adobe Experience Cloud in Mobile Apps" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://experienceleague.adobe.com/de/docs/platform-learn/implement-mobile-sdk/overview./media_1c75750ec1be623e56a379ca69ef6c495799e52a5.png?width=400&format=png&optimize=medium" alt="Tutorial zur Implementierung von Adobe Experience Cloud in Mobile Apps"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/de/docs/platform-learn/implement-mobile-sdk/overview" target="_blank" rel="referrer" title="Tutorial zur Implementierung von Adobe Experience Cloud in Mobile Apps">Tutorial zur Implementierung von Adobe Experience Cloud in Mobile Apps</a>
                    </p>
                    <p class="is-size-6">Erfahren Sie, wie Sie die Mobile Apps von Adobe Experience Cloud implementieren. Dieses Tutorial führt Sie durch eine Implementierung von Experience Cloud-Programmen in einer Swift- oder Android-Beispielanwendung.</p>
                </div>
                <a href="https://experienceleague.adobe.com/de/docs/platform-learn/implement-mobile-sdk/overview" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Weitere Informationen</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

>[!SUCCESS]
>
>**Checkliste für die Eignung für Mobile SDK**
>
> [ Installierte ] Core SDK (Core, Edge, Identity, Consent, Assurance).
> [ ] Erweiterung [Journey Optimizer Mobile](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/) für die Kanäle hinzugefügt, die Sie verwenden werden (Push, In-App, Inhaltskarten, codebasiert).
> [ ] Datenstrom wurde korrekt für Ereignis- und Profildatensätze konfiguriert.
> [ ] mit Assurance implementierte und validierte Identität und Einverständnis
> [ Registrierung und Tracking von Push-Token ] End-to-End validiert.
> [ ] In-App- und/oder Inhaltskarten werden auf einem Gerät validiert angezeigt.
> [ ] Geführte Kanal-Setup , das für neue Implementierungen verwendet wird, oder Konfiguration, die manuell auf die dokumentierten Schritte ausgerichtet ist.


## Adobe Journey Optimizer-Kanalkonfiguration

Durch die Konfiguration mobiler Kanäle in Adobe Journey Optimizer wird sichergestellt, dass Push-Benachrichtigungen und In-App-Nachrichten Ihre App-Benutzer sicher und zuverlässig erreichen. Als Administrator legen Sie die technischen Grundlagen wie App-Anmeldeinformationen, SDK-Integration und Authentifizierungsschlüssel fest, die personalisierte, konforme und optimierte mobile Interaktion ermöglichen. Die ordnungsgemäße Einrichtung ist für die Bereitstellung nahtloser Erlebnisse auf mobilen Touchpoints entscheidend.

>[!PREREQUISITES]
>
> - App-Registrierung in Adobe Experience Platform für mobile Kanäle abgeschlossen.
> - Adobe Experience Platform Mobile SDK in Ihre App integriert.
> - Für iOS (APNs) und Android (FCM) konfigurierte Push-Anmeldedaten.
> - SMS-/MMS-/RCS-Provider-Konten einrichten und Anmeldedaten verfügbar.
> - Die Zugangsdaten für die WhatsApp Business-API wurden konfiguriert und überprüft.
> - Authentifizierungsschlüssel, Zertifikate und API-Token für alle Kanäle.
> - Für jeden Kanal (Push, SMS, WhatsApp) definierte Einverständnis- und Opt-in-Richtlinien.
> - Testumgebungen, die für die Validierung von Konfigurationen vor dem Launch vorbereitet wurden.

### WhatsApp

Erfahren Sie, wie Sie den **WhatsApp-Kanal“ konfigurieren**:

<!-- CARDS

* https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/whatsapp-channel/set-up-whatsapp-channel
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Set up the WhatsApp channel">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/whatsapp-channel/set-up-whatsapp-channel" title="Einrichten des WhatsApp-Kanals" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3470277/?captions=ger&format=jpeg&nocache=1764708699649" alt="Einrichten des WhatsApp-Kanals"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/whatsapp-channel/set-up-whatsapp-channel" target="_blank" rel="referrer" title="Einrichten des WhatsApp-Kanals">Einrichten des WhatsApp-Kanals</a>
                    </p>
                    <p class="is-size-6">Dieses Tutorial führt Sie durch die Einrichtung des WhatsApp-Kanals in Adobe Journey Optimizer, um Echtzeit-Messaging für geschäftliche Zwecke zu ermöglichen.</p>
                </div>
                <a href="https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/whatsapp-channel/set-up-whatsapp-channel" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Ansehen</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

### SMS/MMS/RCS

Konfigurieren Sie **SMS-/MMS-/**-Kanäle) mit den Standardanbietern (Twilio, Synch oder Infobip) oder verwenden Sie einen benutzerdefinierten SMS-Anbieter:

<!-- CARDS
* https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/set-up-sms-channel
* https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/configure-custom-sms-provider
{description = Learn how to configure custom SMS providers in Journey Optimizer, set up API credentials and webhooks, manage opt-in/opt-out keywords, and launch personalized campaigns.}
* https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/configure-mms-api-credentials-and-channel-surfaces
* https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/set-up-rcs
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Configure SMS API credentials and channel surfaces">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/set-up-sms-channel" title="Konfigurieren von SMS-API-Anmeldedaten und Kanaloberflächen" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3413355?format=jpeg&nocache=1764708699948" alt="Konfigurieren von SMS-API-Anmeldedaten und Kanaloberflächen"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/set-up-sms-channel" target="_blank" rel="referrer" title="Konfigurieren von SMS-API-Anmeldedaten und Kanaloberflächen">Konfigurieren von SMS-API-Anmeldeinformationen und Kanaloberflächen</a>
                    </p>
                    <p class="is-size-6">Erfahren Sie, wie Sie Journey Optimizer mit einem SMS-Dienstleister verbinden und wie Sie eine SMS-Kanaloberfläche erstellen.</p>
                </div>
                <a href="https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/set-up-sms-channel" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Ansehen</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Configure a custom SMS provider">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/configure-custom-sms-provider" title="Konfigurieren eines benutzerdefinierten SMS-Anbieters" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3431625/?format=jpeg&nocache=1764708699956" alt="Konfigurieren eines benutzerdefinierten SMS-Anbieters"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/configure-custom-sms-provider" target="_blank" rel="referrer" title="Konfigurieren eines benutzerdefinierten SMS-Anbieters">Konfigurieren eines benutzerdefinierten SMS-Anbieters</a>
                    </p>
                    <p class="is-size-6">Erfahren Sie, wie Sie benutzerdefinierte SMS-Anbieter in Journey Optimizer konfigurieren, API-Anmeldeinformationen und Webhooks einrichten, Opt-in-/Opt-out-Schlüsselwörter verwalten und personalisierte Kampagnen starten.</p>
                </div>
                <a href="https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/configure-custom-sms-provider" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Ansehen</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Configure MMS API credentials and channel surfaces">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/configure-mms-api-credentials-and-channel-surfaces" title="Konfigurieren von MMS-API-Anmeldeinformationen und Kanaloberflächen" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3438055/?captions=ger&format=jpeg&nocache=1764708699939" alt="Konfigurieren von MMS-API-Anmeldeinformationen und Kanaloberflächen"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/configure-mms-api-credentials-and-channel-surfaces" target="_blank" rel="referrer" title="Konfigurieren von MMS-API-Anmeldeinformationen und Kanaloberflächen">Konfigurieren von SMS-API-Anmeldeinformationen und Kanaloberflächen</a>
                    </p>
                    <p class="is-size-6">Erfahren Sie, wie Sie Journey Optimizer mit einem MMS-Dienstanbieter verbinden und wie Sie eine MMS-Kanaloberfläche erstellen.</p>
                </div>
                <a href="https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/configure-mms-api-credentials-and-channel-surfaces" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Ansehen</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Set up RCS in Journey Optimizer">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/set-up-rcs" title="Einrichten von RCS in Journey Optimizer" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3464764/?captions=ger&format=jpeg&nocache=1764708699952" alt="Einrichten von RCS in Journey Optimizer"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/set-up-rcs" target="_blank" rel="referrer" title="Einrichten von RCS in Journey Optimizer">Einrichten von RCS in Journey Optimizer</a>
                    </p>
                    <p class="is-size-6">Erfahren Sie, wie Sie an Ihre Marke angepasste, interaktive RCS-Nachrichten in Adobe Journey Optimizer mithilfe eines benutzerdefinierten SMS-Anbieters konfigurieren und senden. Dieses Tutorial führt Sie durch die Einrichtung von API-Anmeldedaten, Webhooks und Kanalkonfigurationen sowie anschließend durch die Erstellung einer Journey für umfassende, personalisierte Messaging-Erlebnisse – und all dies innerhalb der nativen Messaging-App.</p>
                </div>
                <a href="https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/set-up-rcs" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Ansehen</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

## Einhaltung von Datenschutzgesetzen und Platform-Richtlinien.

<!-- CARDS
* https://experienceleague.adobe.com/de/docs/journey-optimizer/using/privacy/privacy-landing-page{image=../mobile-learning-hub/assets/privacy.webp}{title = Privacy Features in Adobe Journey Optimizer}{description = Learn how to process privacy requests, audit user actions, manage consent, apply governance rules, and leverage advanced security options like Customer Managed Keys.}
* https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/data-governance-framework
* https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/classify-data-using-lables{cta = Watch}
* https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/create-data-usage-policies
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Privacy Features in Adobe Journey Optimizer">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/de/docs/journey-optimizer/using/privacy/privacy-landing-page" title="Datenschutzfunktionen in Adobe Journey Optimizer" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../mobile-learning-hub/assets/privacy.webp" alt="Datenschutzfunktionen in Adobe Journey Optimizer"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/de/docs/journey-optimizer/using/privacy/privacy-landing-page" target="_blank" rel="referrer" title="Datenschutzfunktionen in Adobe Journey Optimizer">Datenschutzfunktionen in Adobe Journey Optimizer</a>
                    </p>
                    <p class="is-size-6">Erfahren Sie, wie Sie Datenschutzanfragen verarbeiten, Benutzeraktionen prüfen, Einverständnis verwalten, Governance-Regeln anwenden und erweiterte Sicherheitsoptionen wie kundenseitig verwaltete Schlüssel nutzen können.</p>
                </div>
                <a href="https://experienceleague.adobe.com/de/docs/journey-optimizer/using/privacy/privacy-landing-page" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Weitere Informationen</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Data Governance Framework Overview">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/data-governance-framework" title="Übersicht über das Data-Governance-Framework" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/33153/?captions=ger&format=jpeg&nocache=1764708700348" alt="Übersicht über das Data-Governance-Framework"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/data-governance-framework" target="_blank" rel="referrer" title="Übersicht über das Data-Governance-Framework">Übersicht über das Data Governance-Framework</a>
                    </p>
                    <p class="is-size-6">Machen Sie sich mit den Governance-Funktionen in Adobe Experience Platform vertraut.</p>
                </div>
                <a href="https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/data-governance-framework" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Ansehen</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Classify data using labels">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/classify-data-using-lables" title="Klassifizieren von Daten mithilfe von Labels" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3422789?captions=ger&format=jpeg&nocache=1764708700350" alt="Klassifizieren von Daten mithilfe von Labels"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/classify-data-using-lables" target="_blank" rel="referrer" title="Klassifizieren von Daten mithilfe von Labels">Klassifizieren von Daten mithilfe von Labels</a>
                    </p>
                    <p class="is-size-6">Informationen darüber, wie Schemata und Datensätze mit Labels versehen können.</p>
                </div>
                <a href="https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/classify-data-using-lables" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Ansehen</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Create Data Usage Policies">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/create-data-usage-policies" title="Erstellen von Richtlinien zur Datennutzung" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/37126/?captions=ger&format=jpeg&nocache=1764708700349" alt="Erstellen von Richtlinien zur Datennutzung"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/create-data-usage-policies" target="_blank" rel="referrer" title="Erstellen von Richtlinien zur Datennutzung">Erstellen von Richtlinien zur Datennutzung</a>
                    </p>
                    <p class="is-size-6">Informationen darüber, wie sich Richtlinien zur Datennutzung erstellen und verwalten lassen.</p>
                </div>
                <a href="https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/create-data-usage-policies" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Ansehen</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

## Häufige Implementierungsfehler und wie diese vermieden werden

Die meisten Probleme mit Mobilgeräten haben ihren Ursprung in der **SDK- oder Datenerfassungskonfiguration** und nicht in den Journey Optimizer-Journey oder -Kampagnen selbst. Verwenden Sie die nachstehende Tabelle, um die Fehlerursache zu ermitteln, und erweitern Sie dann den entsprechenden Abschnitt, um weitere Details anzuzeigen.

### Fallstricke auf einen Blick

| # | Problem/Symptom | Häufig auftretende Fehler | Fehlerbehebung auf einen Blick |
|---|----------------------------------------------|-----------------------------------------------------|------------------------------------------|
| 1 | Einrichtung des geführten Kanals schlägt fehl; kein oder geringer Traffic | [SDK-Versionen oder -Erweiterungen nicht abgestimmt](#1-sdk-versions-and-extensions-not-aligned-with-channel-requirements) | Aktualisieren von SDK-/Erweiterungsversionen; in Assurance validieren |
| 2 | Tracking von Batches schlägt fehl; Fehler in AEP | [Datenströme oder Datensätze falsch konfiguriert](#2-misconfigured-datastreams-or-datasets) | Zuordnen von Ereignissen zu Ereignis-Datensätzen und Profilen zu Profil-Datensätzen |
| 3 | Journey feuern nicht; seltsame Personalisierung | [Identität oder Einverständnis fehlt/inkonsistent](#3-missing-or-inconsistent-identity-and-consent) | Implementieren von Edge Identity &amp; Consent; Überprüfen in Assurance |
| 4 | Kein Push-Versand oder Öffnungen in Berichten | [Push-Token-Registrierung oder -Tracking beschädigt](#4-push-token-registration-and-tracking-not-wired-correctly) | Fehlerbehebung bei Token-Registrierung und Interaktions-Tracking über SDK |
| 5 | Keine In-App-Impressions trotz aktiver Kampagnen | [In-App-Nachrichten oder -Inhaltskarten werden nicht angezeigt](#5-in-app-messages-or-content-cards-not-displaying) | Überprüfen von Messaging-Erweiterungen, Triggern und Assurance-Entscheidungsantworten |

### Detaillierte Anleitungen pro Fallstrick

Öffnen Sie die Fallgrube, die Ihren Symptomen entspricht, um zu sehen, was überprüft werden muss und wie es behoben werden kann.

+++1 SDK-Versionen und -Erweiterungen, die nicht den Kanalanforderungen entsprechen
**Was Sie bemerken werden**

- Push- oder In-App-Aktivitäten erreichen das Gerät nicht.
- Einrichtung des geführten Kanals oder Kanalvalidierung schlägt fehl.
- In Assurance fehlen Erweiterungen für Journey Optimizer, Edge oder Identity.

**Was zu überprüfen**

- Verwenden Sie die für die Einrichtung **geführten Kanals erforderlichen Erweiterungsversionen Mobile Core** und &lbrace;2 **Journey Optimizer)?**
- In **Assurance** unter „Erweiterungen und Ereignisse“:
   - Werden die erwarteten Erweiterungen geladen?
   - Werden Ereignisse an die Edge Network gesendet und quittiert?

**Fehlerbehebung**

- Führen Sie ein Upgrade auf die unterstützten Erweiterungsversionen für Mobile SDK und Journey Optimizer durch.
- Erstellen Sie die App neu, stellen Sie erneut eine Verbindung mit Assurance her und führen Sie die Einrichtung des geführten Kanals erneut aus.

Siehe: [Einrichten von Mobilgeräten und Web](https://experienceleague.adobe.com/de/docs/journey-optimizer/using/configuration/guided-setup/set-mobile-config){target="_blank"}

+++

+++2 falsch konfigurierte Datenströme oder Datensätze
**Was Sie bemerken werden**

- Ereignisse oder Push-Tracking-Batches schlagen in Platform-Datensätzen fehl.
- Fehler bei der Datenaufnahme (z. B. „Aktualisierungen werden für Ereignisse nicht unterstützt„).
- Push- oder In-App-Berichte zeigen wenig oder kein Tracking.

**Was zu überprüfen**

- Hat jemand **Systemschemata oder Datensätze) geändert,** für das Journey Optimizer-Tracking erstellt wurden?
- In Ihrem **Datenstrom**:
   - Sind Erlebnisereignisse einem (Ereignis **Datensatz zugeordnet**?
   - Sind Profilattribute einem **Profildatensatz“**?

**Fehlerbehebung**

- Bearbeiten Sie keine von AJO erstellten Systemdatensätze/-schemata.
- Korrigieren Sie die Datenstromzuordnung (Ereignisse → Ereignisdatensatz, Profile → Profildatensatz).
- Bevorzugt die Einrichtung geführter Kanäle oder die dokumentierten Schritte des Datenstroms anstelle von Ad-hoc-Änderungen.

Siehe: [Fluss von Push-Benachrichtigungen in Adobe Journey Optimizer](https://experienceleague.adobe.com/de/docs/journey-optimizer/using/channels/push/push-config/push-gs){target="_blank"}

+++

+++3 Fehlende oder inkonsistente Identität und Einverständnis
**Was Sie bemerken werden**

- Journey nehmen für App-Benutzer nicht den erwarteten Trigger vor.
- Personalization stimmt nicht mit dem Verhalten der Benutzenden in anderen Kanälen überein.
- Ereignisse werden in Experience Platform angezeigt, Profile sehen jedoch fragmentiert aus.

**Was zu überprüfen**

- Wird **Identity for Edge Network** implementiert und eine stabile primäre ID (z. B. Anmelde-ID) gesendet?
- Wird **Einverständnis für Edge Network** implementiert und aktualisiert, wenn sich die Voreinstellungen ändern?
- In **Assurance**:
   - Enthalten ausgehende Ereignisse Einverständniswerte?
   - Enthalten diese IDs konsistent ECID und Ihre primären IDs?

**Fehlerbehebung**

- Implementieren oder korrigieren Sie **Identity for Edge Network** in der App.
- Implementieren Sie **Einverständnis für Edge Network** und verbinden Sie es mit der Einverständnis-Benutzeroberfläche Ihrer App.
- Testen Sie in Assurance erneut, bis Identität und Einverständnis bei allen relevanten Ereignissen angezeigt werden.

Siehe: [Implementieren des Einverständnisses für Implementierungen von Platform Mobile SDK](https://experienceleague.adobe.com/de/docs/platform-learn/implement-mobile-sdk/app-implementation/consent){target="_blank"}

+++

+++4 Push-Token-Registrierung und -Tracking sind nicht korrekt verkabelt.
**Was Sie bemerken werden**

- Benutzende erhalten nie Push-Benachrichtigungen, obwohl Kampagnen oder Journey ausgeführt werden.
- Push-Berichte zeigen keine Öffnungen, Abbrüche oder Interaktionen.

**Was zu überprüfen**

- Registriert die App das Push-Token bei der Journey Optimizer-Erweiterung:
   - Bei der ersten Installation?
   - Nach jedem App-Update?
   - Wann immer das Betriebssystem das Token aktualisiert?
- Wird beim Öffnen oder Schließen einer Benachrichtigung in Assurance das Tracking von Ereignissen angezeigt?

**Fehlerbehebung**

- Fügen Sie den Code hinzu, der:
   - Registriert das Token über die Journey Optimizer Mobile-Erweiterung, sobald es erstellt oder aktualisiert wird.
   - Sendet Push-Interaktionsereignisse (Öffnen, Schließen, benutzerdefinierte Aktionen) über die Mobile SDK.
- Verwenden Sie Assurance, um zu bestätigen, dass Registrierungs- und Tracking-Ereignisse erwartungsgemäß ausgelöst werden.

Siehe: [Fluss von Push-Benachrichtigungen in Adobe Journey Optimizer](https://experienceleague.adobe.com/de/docs/journey-optimizer/using/channels/push/push-config/push-gs){target="_blank"}

+++

+++5 In-App-Nachrichten oder Inhaltskarten werden nicht angezeigt
**Was Sie bemerken werden**

- In-App-Nachrichten oder -Inhaltskarten werden trotz aktiver Kampagnen oder Journey nie angezeigt.
- Berichte zeigen 0 Impressionen an.

**Was zu überprüfen**

- Sind **Journey Optimizer Mobile Messaging/In-App-Erweiterung** und **Messaging SDK** in der App installiert und registriert?
- In Ihrer **Tags**-Konfiguration:
   - Gibt es Regeln, die Trigger für die richtigen Ereignisse (z. B. Bildschirmansichten oder benutzerspezifische Ereignisse) anfordern?
- In **Assurance**:
   - Wenn diese Ereignisse ausgelöst werden, sehen Sie, wie In-App- oder Inhaltskarten-Entscheidungsanfragen ausgelöst werden?
   - Sehen Sie Antworten, die von der Edge Network zurückgegeben werden?

**Fehlerbehebung**

- Installieren und registrieren Sie die erforderlichen Messaging-Erweiterungen.
- Regeln hinzufügen oder korrigieren, die Entscheidungen von Triggern zu Ihren Zielereignissen (Bildschirme, benutzerdefinierte Ereignisse) ermöglichen.
- Stellen Sie bei Inhaltskarten Folgendes sicher:
   - Abrufen von Karten über die Messaging-SDK-APIs.
   - Rendern Sie sie in Ihrer Benutzeroberfläche.
   - Rückverfolgung von Interaktionen über die SDK.

Siehe:
- [Erstellen und Senden von In-App-Nachrichten](https://experienceleague.adobe.com/de/docs/platform-learn/implement-mobile-sdk/experience-cloud/journey-optimizer/journey-optimizer-inapp){target="_blank"}
- [Konfigurieren der Unterstützung für Inhaltskarten in Mobile SDK](https://experienceleague.adobe.com/de/docs/journey-optimizer/using/channels/content-card/configure/content-card-lp){target="_blank"}

+++


>[!SUCCESS]
>
> **Bereitschafts-Checkliste**
>
> Bevor Sie die App an Marketing-Fachleute übergeben, bestätigen Sie in **[Assurance](https://developer.adobe.com/client-sdks/home/base/assurance/){target="_blank"}** dass:
> 
> [ ] Core SDK + Journey Optimizer-Erweiterungen geladen werden,\
> [ ] Ereignisse fließen im richtigen Datenstrom und in den richtigen Datensätzen ab,\
> [ ]Identität und Einverständnis sind bei allen wichtigen Ereignissen vorhanden,\
> [ ] Push-Token und -Interaktionen werden verfolgt und\
> [ ] Mindestens eine Test-In-App-Nachricht oder -Inhaltskarte wurde angezeigt und als Impression aufgezeichnet.

## Blog-Beiträge

- [Verwenden von CDN-basierter Client-seitiger Personalisierung (ODD) auf Mobilgeräten für schnellere Personalisierungen.](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/using-cdn-based-client-side-personalization-odd-on-mobile-for/ba-p/761626?profile.language=de){target="_blank"}
- [Mobile Activation für Adobe Experience Cloud](https://experienceleaguecommunities.adobe.com/t5/adobe-target-blogs/mobile-activation-for-adobe-experience-cloud/ba-p/541595?profile.language=de){target="_blank"}
