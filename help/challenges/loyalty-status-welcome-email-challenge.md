---
title: Erstellen einer Willkommens-E-Mail zum Treuestatus - Herausforderung
description: Machen Sie sich mit den Grundlagen zum Erstellen einer Journey in der Journey-Arbeitsfläche vertraut.
kt: 8109
feature: Journeys
role: User
level: Beginner
hide: true
source-git-commit: 957515149af1281d29a45b24ca499ef097656eb8
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 8%

---


# Erstellen einer Willkommens-E-Mail zum Treuestatus - Herausforderung

![Willkommens-E-Mail zum Treuestatus von AJO - Challenge Banner](/help/challenges/assets/email-assets/luma-transactional-onboarding-1.png)

| Herausforderung | Willkommens-E-Mail zum Treuestatus erstellen |
|---|---|
| Persona | Journey-Manager |
| Erforderliche Fähigkeiten | <ul><li>[Erstellen von E-Mail-Inhalten mit dem Nachrichten-Editor](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-messages/create-email-content-with-the-message-editor.html?lang=en)</li> <li>[Verwenden von kontextbezogenen Ereignisinformationen für die Personalisierung](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/personalize-content/use-contextual-event-information-for-personalization.html?lang=en)</li><li>[Verwenden von Helper-Funktionen für die Personalisierung](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/personalize-content/use-helper-functions-for-personalization.html?lang=en)</li></ul> |
| Herunterzuladende Assets | [Bestellbestätigungs-Assets](/help/challenges/assets/email-assets/order-confirmation-assets.zip) |

## Die Geschichte

Luma bietet ein Treueprogramm an, um Kunden zu gewinnen und zu binden. Das Programm umfasst vier Stufen: Silber, Gold, Platin und Diamant.

Jede Loyalitätsstufe erhält unterschiedliche Stufen oder Belohnungen, Rabatte und andere spezielle Anreize als Belohnung für ihr Wiederholungsgeschäft.

So unterstreichen Sie den speziellen Diamantenstatus. Luma möchte den Kunden eine Willkommens-E-Mail senden, wenn sie die Diamantenebene erreichen.

## Ihre Herausforderung

Sie wurden aufgefordert, eine Journey einzurichten, die automatisch eine Begrüßungs-E-Mail an Kunden sendet, wenn diese die Diamanten-Treuestufe erreichen.

>[!NOTE]
> Wenn Sie in einer freigegebenen Trainings-Sandbox arbeiten, empfiehlt es sich, Ihren Namen oder Ihre Initialen als Präfix zum Namen eines von Ihnen erstellten Elements hinzuzufügen.

### Erstellen Sie ein Segment mit dem Luma-Diamantstatus .

Erstellen Sie ein Segment in Journey Optimizer mit dem Namen **Ihr Name - Luma - Diamantenstatus**.

### Erstellen der Luma - Neuer Status - Raute - Transaktions-E-Mail-Nachricht

Erstellen einer Begrüßungs-E-Mail

1. Erstellen Sie eine Transaktions-E-Mail mit dem Titel `(your name)_Luma – New Status – Diamond – Transactional email message`.
2. E-Mail mit Betreffzeile versehen `Welcome to Diamond Status, (recipient's first name)!`.
3. Verwenden Sie die bereitgestellte HTML-Datei **[DiamondStatusEmail.html](/help/challenges/assets/email-assets/DiamondStatusEmail.html)** für den E-Mail-Textkörper.


### **Journey #3 - Diamond status upgrade Begrüßungs-E-Mail**

Senden Sie eine E-Mail, wenn ein Treuekunden zu einer neuen Ebene wechselt, um ihm zu gratulieren und ihn über seine neuen Vorteile zu informieren.

1. Erstellen Sie eine Journey, die ausgelöst wird, wenn ein Kunde in die neue Treuestufe Diamond wechselt (insbesondere wenn der Kunde in das für ein neues Mitglied der Diamantstufe definierte Segment eintritt), um die E-Mail &quot;Luma - Neuer Status - Karo - Transaktionen&quot;zu senden.
2. Schließen Sie die Journey in den Testmodus ein und Trigger die Journey, die Sie sich selbst senden können.  

ERFOLGSKRITERIEN

Sie sollten die personalisierte E-Mail &quot;Luma - New Status - Diamond-Transactional&quot; erhalten.
