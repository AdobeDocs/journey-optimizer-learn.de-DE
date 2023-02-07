---
title: Erstellen einer Willkommens-E-Mail zum Treuestatus – Challenge
description: Machen Sie sich mit den Grundlagen zum Erstellen einer Journey in der Journey-Arbeitsfläche vertraut.
kt: 8109
feature: Journeys
role: User
level: Beginner
hide: true
exl-id: 6fd58b8e-7178-495d-a85d-eb67fc4f3acf
source-git-commit: a4f2d3e7f5cd4255d029315ffb21dd44609ebf38
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 85%

---

# Erstellen einer Willkommens-E-Mail zum Treuestatus – Challenge

![Willkommens-E-Mail zum Treuestatus – Challenge-Banner](/help/challenges/assets/email-assets/luma-transactional-onboarding-1.png)

| Challenge | Erstellen einer Willkommens-E-Mail zum Treuestatus |
|---|---|
| Persona | Journey-Manager |
| Erforderliche Fähigkeiten | <ul><li>[Erstellen von Segmenten](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/profiles-segments-subscriptions/create-segments.html?lang=de)</li> <li>[Segmentqualifizierung](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/use-case-read-segment-qualification.html?lang=de)</li><li>[HTML-Inhalt importieren](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/email-channel/import-and-author-html-email-content.html)</li></ul> |
| Herunterzuladende Assets | [StatusUpgradeEmail.zip](/help/challenges/assets/email-assets/StatusUpgradeEmail.zip) |

## Die Story

Luma bietet ein Treueprogramm an, um Kundinnen und Kunden zu gewinnen und zu binden. Das Programm umfasst vier Stufen: Bronze, Silber, Gold und Platin. Jede Loyalitätsstufe erhält unterschiedliche Prämien, Rabatte und andere spezielle Anreize als Belohnung für ihr Wiederholungsgeschäft.

Zur Hervorhebung des besonderen Platinstatus. Luma möchte Kunden eine Willkommens-E-Mail senden, wenn sie die Platin-Ebene erreichen.

## Ihre Challenge

Sie wurden gebeten, eine Journey einzurichten, die automatisch eine Willkommens-E-Mail an Kundinnen und Kunden sendet, wenn diese die Platin-Treuestufe erreichen.

>[!BEGINTABS]

>[!TAB Aufgabe]

Wenn sich ein Treuekunden für die Platin-Stufe qualifiziert, sollte er eine E-Mail erhalten, um ihm zu gratulieren und ihn über seine neuen Vorteile zu informieren. Das Kreativ-Team hat eine HTML-Datei **[Luma – Status-Upgrade – Willkommens-E-Mail](/help/challenges/assets/email-assets/StatusUpgradeEmail.zip)** mit dem E-Mail-Textkörper bereitgestellt.

1. Erstellen Sie ein [!UICONTROL Segment] namens `Luma – platinum status` in Journey Optimizer.
2. Erstellen Sie eine Journey namens `Luma – New Status – platinum`.
   1. Ein Kunde tritt in die Journey ein, wenn er sich für die Platin-Loyalitätsstufe qualifiziert.
   2. Der Kunde sollte eine E-Mail-Nachricht mit der Bezeichnung `Luma – Platinum Status - Welcome` und der Betreffzeile `Welcome to Platinum Status, {firstName}!` erhalten, deren Textkörper vom Kreativ-Team bereitgestellt wird. Dies ist eine [!UICONTROL Transaktions]-E-Mail.
   3. Beim Hochladen der HTML-Datei stellen Sie fest, dass in der E-Mail vom Status „Diamant“ die Rede ist und nicht von „Platin“. Aktualisieren Sie die E-Mail im [!UICONTROL Email Designer].

>[!TAB Erfolgskriterien]

Testen Sie Ihre Journey:

1. Stellen Sie sicher, dass für die [!UICONTROL Aktivität „Segment lesen“] der [!UICONTROL Namespace] auf **[!DNL Luma CRM id(lumaCrmId)]** gesetzt ist.
2. Überschreiben Sie die standardmäßigen [!UICONTROL E-Mail-Parameter] und setzen Sie sie auf Ihre eigene E-Mail-Adresse
   * Klicken Sie in den [!UICONTROL E-Mail-Parametern] auf das T-Symbol (Parameterüberschreibungen aktivieren)
   * Klicken Sie in das [!UICONTROL Adressfeld]
   * Fügen Sie im nächsten Bildschirm Ihre E-Mail-Adresse in Klammern hinzu: `"yourname@yourdomain"` im Ausdruckseditor, dann auf „OK“ klicken.
3. Setzen Sie die Journey in den Testmodus
4. Auswählen **Trigger eines Ereignisses**
5. Fügen Sie in das Feld [!UICONTROL Profilkennung] die folgende [!DNL CRM ID] für `Stanleigh Stooke` ein: `4f34057d9d9e792c28ba18ecae378e98`

**Ergebnis**: Sie sollten eine personalisierte E-Mail *Luma – Platin-Status – Willkommen* erhalten.

So sollte die E-Mail aussehen:

![Luma – Status-Upgrade – Willkommens-E-Mail](/help/challenges/assets/status-upgrade-welcome-email.png)

>[!TAB Überprüfen Sie Ihre Arbeit]

So sollte das Segment aussehen:

![Luma - Platinstatus-Segment](/help/challenges/assets/segment-luma-platinum-status.png)

So sollte Ihre Journey aussehen:

![platinum-status-upgrade-journey](/help/challenges/assets/journey-luma-status-upgrade.png)

>[!ENDTABS]
