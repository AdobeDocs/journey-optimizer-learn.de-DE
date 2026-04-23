---
title: Kampagne erstellen
description: Erstellen Sie eine Kampagne, um Benutzende anzusprechen, die sich für den Empfang von Push-Benachrichtigungen entschieden haben, und versenden Sie die Nachricht zum geplanten Zeitpunkt.
feature: Push
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-04-21T00:00:00Z
jira: KT-20879
exl-id: 94fda23f-e26a-494b-8e5c-6c442bae61c4
source-git-commit: c339fe796af1e691cd3b1c98cd6ba8a8772551e4
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 1%

---

# Kampagne erstellen

In diesem Schritt erstellen Sie eine Kampagne in Adobe Journey Optimizer, um geplante Web-Push-Benachrichtigungen an Benutzer zu senden, die sich angemeldet haben. Die Kampagne richtet sich an eine geeignete Audience und sendet Nachrichten zu einem vordefinierten Zeitpunkt, was eine geplante und zielgruppenbasierte Interaktion ermöglicht.

* Bei Journey Optimizer anmelden
* Navigieren Sie zur Journey-Verwaltung | Kampagnen | Kampagnen erstellen

## Angeben der Kampagneneinstellungen


Geben Sie den Kampagnennamen an

![campaign-name](assets/campign-push-notification.png)

## Aktion mit der Kampagne verknüpfen

Verknüpfen Sie die zuvor in diesem Tutorial erstellte Konfiguration des Push-Kanals

![campaign-action](assets/campign-push-notification-action.png)

## Zielgruppe mit der Kampagne verknüpfen

Audience-`AudienceForPush` mit der Kampagne verknüpfen

![campaign-audience](assets/campign-push-notification-audience.png)

## Inhalt für die Push-Benachrichtigung erstellen

Erstellen Sie grundlegende Push-Inhalte zum Testen der Push-Benachrichtigung. Geben Sie Titel und Text der Nachricht an, wie unten dargestellt

![content-for-push-notification](assets/campign-push-notification-content.png)

## Planen der Kampagne

Planung der Kampagne gemäß Ihren Anforderungen

![schedule-campaign](assets/campign-push-notification-schedule.png)

Stellen Sie abschließend sicher, dass Sie die Kampagne aktivieren.

## Testen der Kampagne

Um die Kampagne zu testen, aktivieren Sie zunächst Benachrichtigungen auf der [Webseite, indem Sie sich anmelden](http://localhost:3000) wenn Sie dazu aufgefordert werden. Warten Sie nach dem Opt-in, bis die Kampagne zum geplanten Zeitpunkt ausgeführt wird. Wenn die Kampagne ausgeführt wird, sollten Sie die Push-Benachrichtigung in Ihrem Browser erhalten.
