---
title: Erstellen einer Willkommens-E-Mail zum Treuestatus – Challenge
description: Erstellen Sie eine Journey, die automatisch eine Begrüßungs-E-Mail an Kunden sendet, wenn diese die Treuestufe erreichen.
kt: 8109
feature: Journeys
role: User
level: Beginner
last-substantial-update: 2023-02-01T00:00:00Z
exl-id: 6fd58b8e-7178-495d-a85d-eb67fc4f3acf
source-git-commit: aaf273b8b6fe0a5f33c132cc0113ec2460152349
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 60%

---

# Erstellen einer Willkommens-E-Mail zum Treuestatus – Challenge

![Willkommens-E-Mail zum Treuestatus – Challenge-Banner](/help/challenges/assets/email-assets/luma-transactional-onboarding-1.png)

| Challenge | Erstellen einer Willkommens-E-Mail zum Treuestatus |
|---|---|
| Persona | Journey-Manager |
| Erforderliche Fähigkeiten | <ul><li>[Erstellen von Segmenten](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/profiles-segments-subscriptions/create-segments.html?lang=de)</li> <li>[Segmentqualifizierung](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/use-case-read-segment-qualification.html?lang=de)</li><li>[HTML-Inhalt importieren](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/email-channel/import-and-author-html-email-content.html?lang=de)</li></ul> |
| Herunterzuladende Assets | [StatusUpgradeEmail.zip](/help/challenges/assets/email-assets/StatusUpgradeEmail.zip) |

{style=&quot;table-layout:auto&quot;}

## Die Story

Luma bietet ein Treueprogramm an, um Kundinnen und Kunden zu gewinnen und zu binden. Das Programm umfasst vier Stufen: Bronze, Silber, Gold und Platin. Jede Loyalitätsstufe erhält unterschiedliche Prämien, Rabatte und andere spezielle Anreize als Belohnung für ihr Wiederholungsgeschäft.

Um den speziellen Platin-Status zu unterstreichen, möchte Luma eine Willkommens-E-Mail an Kunden senden, wenn sie die Platin-Ebene erreichen.

## Ihre Challenge

Sie wurden gebeten, eine Journey einzurichten, die automatisch eine Willkommens-E-Mail an Kundinnen und Kunden sendet, wenn diese die Platin-Treuestufe erreichen.

>[!BEGINTABS]

>[!TAB Aufgabe]

Wenn sich ein Treuekunden für die Platin-Stufe qualifiziert, sollte er eine E-Mail erhalten, um ihm zu gratulieren und ihn über seine neuen Vorteile zu informieren. Das Kreativteam hat eine HTML-Datei bereitgestellt **[Luma - Status-Upgrade - Willkommens-E-Mail](/help/challenges/assets/email-assets/StatusUpgradeEmail.zip)** durch den E-Mail-Textkörper.

1. Erstellen Sie ein [!UICONTROL Segment] namens `Luma - platinum status` in Journey Optimizer.

1. Erstellen Sie eine Journey namens `Luma - New Status - platinum`.

   1. Ein Kunde wechselt in die Journey, wenn er sich für die Treuestufe auf Platin qualifiziert.

   1. Der Kunde sollte eine E-Mail-Nachricht mit der Bezeichnung `Luma - Platinum Status - Welcome` und der Betreffzeile `Welcome to Platinum Status, {firstName}!` erhalten, deren Textkörper vom Kreativ-Team bereitgestellt wird. Dies ist ein [!UICONTROL transactional] E-Mail.

   1. Beim Hochladen der HTML-Datei stellen Sie fest, dass in der E-Mail vom Status „Diamant“ die Rede ist und nicht von „Platin“. Aktualisieren Sie die E-Mail im [!UICONTROL E-Mail-Designer], anstatt eine neue Datei vom Kreativ-Team anzufordern.

>[!TAB Erfolgskriterien]

Testen Sie Ihre Journey:

1. Stellen Sie sicher, dass [!UICONTROL Segmentaktivität lesen] hat die [!UICONTROL namespace] auf **[!DNL Luma CRM id(lumaCrmId)]**.

1. Überschreiben Sie die standardmäßigen [!UICONTROL E-Mail-Parameter] und setzen Sie sie auf Ihre eigene E-Mail-Adresse:
   * Im **[!UICONTROL E-Mail-Parameter]** klicken Sie auf das T-Symbol (Parameter-Überschreibung aktivieren).

   * Klicken Sie auf **[!UICONTROL Adresse]** -Feld.

   * Fügen Sie im nächsten Bildschirm Ihre E-Mail-Adresse in Klammern hinzu: `"yourname@yourdomain"` Klicken Sie im Ausdruckseditor auf **[!UICONTROL OK]**.

1. Setzen Sie die Journey in den Testmodus.

1. Auswählen **[!UICONTROL Trigger eines Ereignisses]**.

1. Fügen Sie Folgendes hinzu: `CRM ID` für `Stanleigh Stooke` im **[!UICONTROL Profilkennung]** -Feld: `4f34057d9d9e792c28ba18ecae378e98`

**Ergebnis:** Sie sollten personalisierte *Luma - Platin-Status - Willkommen* E-Mail.

So sollte die E-Mail aussehen:

![Luma - Status-Upgrade - Willkommens-E-Mail](/help/challenges/assets/status-upgrade-welcome-email.png)

>[!TAB Überprüfen Sie Ihre Arbeit]

So sollte das Segment aussehen:

![Luma – Platinstatus-Segment](/help/challenges/assets/segment-luma-platinum-status.png)

So sollte Ihre Journey aussehen:

![platinum-status-upgrade-journey](/help/challenges/assets/journey-luma-status-upgrade.png)

>[!ENDTABS]
