---
title: Zielgruppe erstellen
description: Definieren Sie ein Segment in Adobe Experience Platform, das sich an Benutzende richtet, die für den Empfang von Push-Benachrichtigungen berechtigt sind.
feature: Push
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-04-21T00:00:00.000Z
jira: KT-20879
exl-id: 427bb35a-d607-48be-845d-9587c4cad86b
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: 66e1fd99-672d-5d64-aa58-eca107f0fbae
    internal-label: Push
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: d4f3ee0d644b4f962763e6807f014efe132a9a05
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 3%
---
# Erstellen einer Zielgruppe

Um eine Audience für die Kampagne zu erstellen, definieren Sie in Adobe Experience Platform ein Segment, das Benutzende anspricht, die für den Empfang von Push-Benachrichtigungen berechtigt sind. In diesem Tutorial haben Benutzende mit einem aktiven Push-Abonnement (Push-Token vorhanden), die Benachrichtigungen nicht abgelehnt haben (Blockierungsliste-Flag ist „false„) und mit der angegebenen Anwendungskonfiguration verknüpft sind (Anwendungs-ID ist `my-first-push`). Diese Benutzenden sind vollständig berechtigt, Web-Push-Benachrichtigungen über Kampagnen oder Journey in Adobe Journey Optimizer zu erhalten. Nachdem Sie die Zielgruppe erstellt haben, stellen Sie sicher, dass sie ausgewertet wurde, damit die Profile ausgefüllt und für die Zielgruppenbestimmung bereit sind.
Diese Zielgruppe wird dann in der Kampagne verwendet, um geplante Web-Push-Nachrichten nur an abonnierte Benutzer zu senden.

![create-audience](assets/push-audience.png)
