---
title: Zielgruppe erstellen
description: Definieren Sie ein Segment in Adobe Experience Platform, das sich an Benutzende richtet, die für den Empfang von Push-Benachrichtigungen berechtigt sind.
feature: Push
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-04-21T00:00:00Z
jira: KT-20879
exl-id: 427bb35a-d607-48be-845d-9587c4cad86b
source-git-commit: 676c21ca09e0df8d404b05081d71b147755d65d5
workflow-type: tm+mt
source-wordcount: '43'
ht-degree: 9%

---

# Erstellen einer Zielgruppe

Um eine Audience für die Kampagne zu erstellen, definieren Sie in Adobe Experience Platform ein Segment, das Benutzende anspricht, die für den Empfang von Push-Benachrichtigungen berechtigt sind. In diesem Tutorial haben Benutzende mit einem aktiven Push-Abonnement (Push-Token vorhanden), die Benachrichtigungen nicht abgelehnt haben (Blockierungsliste-Flag ist „false„) und mit der angegebenen Anwendungskonfiguration verknüpft sind (Anwendungs-ID ist `my-first-push`). Diese Benutzenden sind vollständig berechtigt, Web-Push-Benachrichtigungen über Kampagnen oder Journey in Adobe Journey Optimizer zu erhalten. Nachdem Sie die Zielgruppe erstellt haben, stellen Sie sicher, dass sie ausgewertet wurde, damit die Profile ausgefüllt und für die Zielgruppenbestimmung bereit sind.
Diese Zielgruppe wird dann in der Kampagne verwendet, um geplante Web-Push-Nachrichten nur an abonnierte Benutzer zu senden.

![create-audience](assets/push-audience.png)
