---
title: Erstellen einer Willkommens-E-Mail zum Treuestatus - Herausforderung
description: Machen Sie sich mit den Grundlagen zum Erstellen einer Journey in der Journey-Arbeitsfläche vertraut.
kt: 8109
feature: Journeys
role: User
level: Beginner
hide: true
exl-id: 6fd58b8e-7178-495d-a85d-eb67fc4f3acf
source-git-commit: e148101f8404c8e2019ee17823bcf1d7a9668bc5
workflow-type: tm+mt
source-wordcount: '454'
ht-degree: 4%

---

# Erstellen einer Willkommens-E-Mail zum Treuestatus - Herausforderung

![Willkommens-E-Mail zum Treuestatus von AJO - Challenge Banner](/help/challenges/assets/email-assets/luma-transactional-onboarding-1.png)

| Herausforderung | Willkommens-E-Mail zum Treuestatus erstellen |
|---|---|
| Persona | Journey-Manager |
| Erforderliche Fähigkeiten | <ul><li>[Erstellen von Segmenten](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/profiles-segments-subscriptions/create-segments.html)</li> <li>[Segmentqualifizierung](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/use-case-read-segment-qualification.html)</li><li>[HTML-Inhalt importieren](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-messages/create-emails/import-and-author-html-email-content.html)</li></ul> |
| Herunterzuladende Assets | [platinumStatusEmail.zip](/help/challenges/assets/email-assets/platinumStatusEmail.zip) |

## Die Geschichte

Luma bietet ein Treueprogramm an, um Kunden zu gewinnen und zu binden. Das Programm umfasst vier Stufen: Bronze, Silber, Gold und Platin. Jede Loyalitätsstufe erhält unterschiedliche Stufen oder Belohnungen, Rabatte und andere spezielle Anreize als Belohnung für ihr Wiederholungsgeschäft.

Zur Hervorhebung des speziellen Platinstatus. Luma möchte Kunden eine Willkommens-E-Mail senden, wenn sie die Platin-Ebene erreichen.

## Ihre Herausforderung

Sie wurden aufgefordert, eine Journey einzurichten, die automatisch eine Willkommens-E-Mail an Kunden sendet, wenn diese die Platin-Treuestufe erreichen.

>[!BEGINTABS]

>[!TAB Aufgabe]

Wenn sich ein Treuekunden für die Platin-Stufe qualifiziert, sollte er eine E-Mail erhalten, um ihm zu gratulieren und ihn über seine neuen Vorteile zu informieren. Das Kreativteam hat eine HTML-Datei bereitgestellt **[Luma - Status-Upgrade - Willkommens-E-Mail](/help/challenges/assets/email-assets/StatusUpgradeEmail.zip)** durch den E-Mail-Textkörper.

1. Erstellen Sie ein Segment in Journey Optimizer mit dem Namen `Luma – status upgrade`.
2. Erstellen Sie eine Journey namens &quot;Luma - New Status - Platin&quot;.
   1. Ein Kunde tritt in die Journey ein, wenn er sich für die Platin-Treuestufe qualifiziert.
   2. Der Kunde sollte eine E-Mail mit der Bezeichnung erhalten `Luma – Platinum Status - Welcome`durch die Betreffzeile `Welcome to Platinum Status, (recipient's first name)!` mit dem vom Kreativteam zur Verfügung gestellten Text.
   3. Beim Hochladen der HTML-Datei wird in der E-Mail der Status &quot;diamond&quot; und nicht &quot;platinum&quot; angegeben. Anstatt eine neue Datei vom Kreativteam anzufordern, aktualisieren Sie die E-Mail im E-Mail-Designer.

>[TIPP!]
> Stellen Sie sicher, dass die Luma - Platinum Status - Welcome eMail transaktional ist.


>[!TAB Erfolgskriterien]

Testen Sie Ihre Journey:

1. Stellen Sie sicher, dass für die Aktivität &quot;Segment lesen&quot;der Namespace auf **Luma CRM id(lumaCrmId)**
2. Standard-E-Mail-Parameter überschreiben und auf Ihre eigene E-Mail-Adresse festlegen

+++ Klicken Sie hier , um weitere Informationen zum Überschreiben zu erhalten.
   * Zeigen Sie die verborgenen Werte an, indem Sie auf das Augensymbol klicken.
   * Klicken Sie in den E-Mail-Parametern auf das T-Symbol (Parameter überschreiben aktivieren).

   ![E-Mail-Parameter überschreiben](/help/challenges/assets/c3-override-email-paramters.jpg)

   * Klicken Sie in das Adressfeld
   * Fügen Sie im nächsten Bildschirm Ihre E-Mail-Adresse in Klammern ein: `"yourname@yourdomain"` im Ausdruckseditor und klicken Sie auf &quot;OK&quot;.
+++


3. Journey auf Testmodus setzen
4. Trigger eines Ereignisses
5. Fügen Sie im Feld Profilkennung die folgende CRM-ID für Standard-Stooke hinzu: `4f34057d9d9e792c28ba18ecae378e98`

Sie sollten personalisierte *Luma - Platin-Status - Willkommen* E-Mail.

>[!TAB Überprüfen Sie Ihre Arbeit]

So sollte Ihre Journey aussehen:

![platinum-status-upgrade-Journey](/help/challenges/assets/journey-luma-status-upgrade.png)


So sollte die E-Mail aussehen:

![Luma - Status-Upgrade - Willkommens-E-Mail](/help/challenges/assets/status-upgrade-welcome-email.png)

>[!ENDTABS]
