---
title: Erstellen einer Willkommens-E-Mail zum Treuestatus - Herausforderung
description: Machen Sie sich mit den Grundlagen zum Erstellen einer Journey in der Journey-Arbeitsfläche vertraut.
kt: 8109
feature: Journeys
role: User
level: Beginner
hide: true
exl-id: 6fd58b8e-7178-495d-a85d-eb67fc4f3acf
source-git-commit: cc9d123e4b8efd82eea348c31f5b993556438074
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 5%

---

# Erstellen einer Willkommens-E-Mail zum Treuestatus - Herausforderung

![Willkommens-E-Mail zum Treuestatus - Challenge Banner](/help/challenges/assets/email-assets/luma-transactional-onboarding-1.png)

| Herausforderung | Willkommens-E-Mail zum Treuestatus erstellen |
|---|---|
| Persona | Journey-Manager |
| Erforderliche Fähigkeiten | <ul><li>[Erstellen von Segmenten](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/profiles-segments-subscriptions/create-segments.html)</li> <li>[Segmentqualifizierung](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/use-case-read-segment-qualification.html)</li><li>[HTML-Inhalt importieren](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-messages/create-emails/import-and-author-html-email-content.html)</li></ul> |
| Herunterzuladende Assets | [StatusUpgradeEmail.zip](/help/challenges/assets/email-assets/StatusUpgradeEmail.zip) |

## Die Geschichte

Luma bietet ein Treueprogramm an, um Kunden zu gewinnen und zu binden. Das Programm umfasst vier Stufen: Bronze, Silber, Gold und Platin. Jede Loyalitätsstufe erhält unterschiedliche Prämien, Rabatte und andere spezielle Anreize als Belohnung für ihr Wiederholungsgeschäft.

Zur Hervorhebung des speziellen Platinstatus. Luma möchte Kunden eine Willkommens-E-Mail senden, wenn sie die Platin-Ebene erreichen.

## Ihre Herausforderung

Sie wurden aufgefordert, eine Journey einzurichten, die automatisch eine Willkommens-E-Mail an Kunden sendet, wenn diese die Platin-Treuestufe erreichen.

>[!BEGINTABS]

>[!TAB Aufgabe]

Wenn sich ein Treuekunden für die Platin-Stufe qualifiziert, sollte er eine E-Mail erhalten, um ihm zu gratulieren und ihn über seine neuen Vorteile zu informieren. Das Kreativteam hat eine HTML-Datei bereitgestellt **[Luma - Status-Upgrade - Willkommens-E-Mail](/help/challenges/assets/email-assets/StatusUpgradeEmail.zip)** durch den E-Mail-Textkörper.

1. Erstellen Sie eine [!UICONTROL Segment] in Journey Optimizer `Luma – status upgrade`.
2. Erstellen Sie eine Journey mit dem Namen `Luma – New Status – platinum`.
   1. Ein Kunde tritt in die Journey ein, wenn er sich für die Platinloyalitätsstufe qualifiziert.
   2. Der Kunde sollte eine E-Mail mit der Bezeichnung erhalten `Luma – Platinum Status - Welcome`durch die Betreffzeile `Welcome to Platinum Status, (recipient's first name)!` mit dem E-Mail-Textkörper, der vom Kreativteam bereitgestellt wird. Dies ist ein [!UICONTROL transactional] E-Mail.
   3. Beim Hochladen der HTML-Datei wird in der E-Mail der Status &quot;diamond&quot; und nicht &quot;platinum&quot; angegeben. Aktualisieren Sie die E-Mail in Email Designer, anstatt eine neue Datei vom Kreativteam anzufordern.

>[!TAB Erfolgskriterien]

Testen Sie Ihre Journey:

1. Stellen Sie sicher, dass die Variable [!UICONTROL Segmentaktivität lesen] hat die [!UICONTROL namespace] auf **[!DNL Luma CRM id(lumaCrmId)]**
2. Standardeinstellung überschreiben [!UICONTROL E-Mail-Parameter] und legen Sie sie auf Ihre eigene E-Mail-Adresse fest
   * Zeigen Sie die verborgenen Werte an, indem Sie auf das Augensymbol klicken.
   * Im [!UICONTROL E-Mail-Parameter]klicken Sie auf das T-Symbol (Parameter überschreiben aktivieren)

       ![E-Mail-Parameter überschreiben](/help/challenges/assets/c3-override-email-paramters.jpg)
   
   * Klicken Sie in die [!UICONTROL Adressfeld]
   * Fügen Sie im nächsten Bildschirm Ihre E-Mail-Adresse in Klammern ein: `"yourname@yourdomain"` im Ausdruckseditor und klicken Sie auf &quot;OK&quot;.


3. Journey auf Testmodus setzen
4. Trigger eines Ereignisses
5. Fügen Sie Folgendes hinzu: [!DNL CRM ID] für [!DNL Stanleigh Stooke] in [!UICONTROL Profilkennung] -Feld: `4f34057d9d9e792c28ba18ecae378e98`

**Ergebnis:** Sie sollten personalisierte *Luma - Platin-Status - Willkommen* E-Mail.

>[!TAB Überprüfen Sie Ihre Arbeit]

So sollte Ihre Journey aussehen:

![platinum-status-upgrade-Journey](/help/challenges/assets/journey-luma-status-upgrade.png)


So sollte die E-Mail aussehen:

![Luma - Status-Upgrade - Willkommens-E-Mail](/help/challenges/assets/status-upgrade-welcome-email.png)

>[!ENDTABS]
