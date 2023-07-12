---
title: Erstellen einer Ankündigung zur Sommerkollektion – Herausforderung
description: Senden Sie eine Ankündigung zur Sommerkollektion an ein Segment bestehender Kundinnen und Kunden, um die neue Sommerkollektion von Luma zu bewerben.
jira: KT-8109
feature: Segments, Journeys, Email
role: User
level: Beginner
last-substantial-update: 2023-02-01T00:00:00Z
exl-id: ae457be7-2c67-4950-a072-1d7030b0e17b
source-git-commit: 035d568fc25119142b92e0caa8adfb0ae5e21be8
workflow-type: tm+mt
source-wordcount: '1126'
ht-degree: 100%

---

# Erstellen einer Ankündigung zur Sommerkollektion – Herausforderung

![Banner für die Ankündigung zur AJO-Sommerkollektion](/help/challenges/assets/email-assets/luma-transactional-onboarding-3.png)

| Herausforderung | Erstellen einer Ankündigung zur Sommerkollektion |
|---|---|
| Persona | Journey-Manager |
| Erforderliche Fähigkeiten | <ul><li>[Erstellen von Segmenten](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/profiles-segments-subscriptions/create-segments.html?lang=de)</li><li> [Importieren und Erstellen von HTML-E-Mail-Inhalten](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-messages/create-emails/import-and-author-html-email-content.html?lang=de)</li><li>[Anwendungsfall: Segment lesen](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/use-case-read-segment.html?lang=de)</li> |
| Herunterzuladende Assets | [E-Mail-Dateien zur saisonalen Kollektion](/help/challenges/assets/email-assets/emails-seasonal-collection-announcement.zip) |

{style="table-layout:auto"}

## Die Story

Luma, ein fiktionales Sportbekleidungsunternehmen, vermarktet die neueste Bekleidungs- und Zubehörkollektion, um den Umsatz durch bestehende Kundinnen und Kunden zu steigern. Luma startet die neue Sommerkollektion und möchte verschiedene Kundensegmente speziell ansprechen.

## Ihre Herausforderung

Das Marketing-Team von Luma bittet Sie, eine Marketing-Kampagne für Sommerkollektionen in Journey Optimizer zu implementieren. Ihre Herausforderung besteht in Folgendem:

* Erstellen Sie ein Segment, das definiert, welche Profile für den Erhalt der Promotion qualifiziert sind.
* Erstellen Sie die Journey.

### Schritt 1: Definieren des Segments – Aktive Kundinnen und Kunden

>[!BEGINTABS]

>[!TAB Aufgabe]

#### Erstellen Sie ein Segment in [!DNL Journey Optimizer]

* Erstellen Sie ein Segment in [!DNL Journey Optimizer] namens *Aktive Kundinnen und Kunden*.
* Das Segment darf nur aktive Kundinnen und Kunden von Luma umfassen.
* Aktive Kundinnen und Kunden werden definiert als Personen, die eine Stufe im Treueprogramm von Luma erreicht haben (Bronze, Silber, Gold oder Platin).


>[!TAB Erfolgskriterien]

Im Segment Builder können Sie die geschätzte Anzahl qualifizierter Profile anzeigen. Wenn Sie mit den Daten der Trainings-Sandbox arbeiten, verfügen Sie über rund 753 qualifizierte Profile von insgesamt 1290.

>[!NOTE]
>Es kann bis zu 24 Stunden dauern, bis die Segmentzugehörigkeit für vorhandene Profile angezeigt wird, da die vorhandenen Profile aufgestockt werden müssen.

**Dem Segment wurde ein passendes Profil hinzugefügt:**

Sie können die zum Segment hinzugefügten Profile überprüfen, indem Sie zu einem der Profile navigieren, die in der Detailansicht Ihres Segments aufgelistet sind.

Überprüfen Sie auf der Profilseite die Registerkarte [!UICONTROL Attribute], dass sie qualifiziert sind: die Stufe sollte Silber, Gold, Platin oder Diamant sein.

![Profilattribute](assets/C1-S1-profile-attributes.png)

Sie können auch zur Registerkarte [!UICONTROL Segmentzugehörigkeit] gehen. Ihr Segment sollte dort aufgelistet werden.

![Segmentzugehörigkeit](assets/C1-S1-profile-segment-membership.png)

>[!TAB Überprüfen Sie Ihre Arbeit]

Segmentfelder: **[!UICONTROL Attribute]** > **[!UICONTROL individuelles XDM-Profil]** > **[!UICONTROL Treue]** > **[!UICONTROL Ebene]**

So sollte Ihr Segment aussehen:

![Segment – Aktive Kundinnen und Kunden](/help/challenges/assets/C1-S1.png)

Der Code sollte wie folgt aussehen:

```javascript
stringCompare("equals", loyalty.tier, ["diamond", "gold", "platinum", "silver"], false)
```

>[!ENDTABS]


### Schritt 2: Erstellen der Journey – Ankündigung der Sommerkollektion

>[!BEGINTABS]

>[!TAB Aufgabe]

#### Ankündigung zur Sommerkollektion senden

Eine Agentur hat Ihnen vier HTML-Dateien mit dem Design für die E-Mails zur Verfügung gestellt:

* `SeasonalCollectionEmail.html`
* E-Mail zur Herrenkollektion von Luma
* E-Mail zur Damenkollektion von Luma
* E-Mail Luma – 20 % Rabatt auf die Kollektion

1. [Herunterladen der E-Mail-Dateien zur saisonalen Kollektion](/help/challenges/assets/email-assets/emails-seasonal-collection-announcement.zip).

1. Erstellen Sie eine Journey mit dem Namen *Luma – Ankündigung zur Sommerkollektion* basierend auf den folgenden Leitlinien:

   1. Senden Sie die E-Mail *Luma – Ankündigung der neuen Sommerkollektion* an das Segment *Aktive Kunden*, wobei 10 % der Audience als Kontrollgruppe dient
      * Titel der Nachricht: *Luma – Ankündigung zur Sommerkollektion*
      * Betreff: *(Vorname des Empfängers), die neue Sommerkollektion von Luma ist hier!*
      * Verwenden Sie die bereitgestellte HTML-Datei `SeasonalCollectionEmail.html` für den Textkörper der E-Mail.
   1. Warten Sie zwei Tage und senden Sie dann eine Folgenachricht mit zielgerichteteren Inhalten:
      * Männliche Kunden sollten die E-Mail zur **Herrenkollektion von Luma** erhalten.
         * Titel der Nachricht: *Herrenkollektion von Luma*
         * Betreffzeile: *(Vorname des Empfängers), erkunden Sie die neue Sportbekleidung für Herren!*
         * Textkörper der E-Mail: `MensCollectionEmail.html` für den E-Mail-Textkörper.
      * Kundinnen sollten die E-Mail zur **Damenkollektion von Luma** erhalten.
         * Titel der Nachricht: *Damenkollektion von Luma*
         * Betreffzeile: *(Vorname der Empfängerin), erkunden Sie die Damenkollektion von Luma!*
         * Textkörper der E-Mail: `WomensCollectionEmail.html`
      * Andere Kundinnen und Kunden sollten die E-Mail **Luma – 20 % Rabatt auf die Kollektion** erhalten.
      * Titel der Nachricht: *Luma – 20 % Rabatt auf die Kollektion*
      * Betreffzeile: *(Vorname des Empfängers/der Empfängerin), erhalten Sie 20 % Rabatt auf Ihre Käufe!*
      * Textkörper der E-Mail: `20OOffCollectionEmail.html`
   1. Warten Sie nach dem Versand der oben genannten zielgerichteten E-Mails zwei Tage, bis die E-Mail geöffnet wird.
   1. Wenn die zielgerichtete E-Mail nicht innerhalb von 2 Tagen geöffnet wird, senden Sie die E-Mail **Luma – 20 % Rabatt auf die Kollektion** als letzten Retargeting-Versuch


>[!TAB Erfolgskriterien]

#### Vorschau der E-Mails

**E-Mail-Nachricht Nr. 1: Luma – Ankündigung der Sommerkollektion**

Vorschau der E-Mail:

1. Fügen Sie ein Testprofil hinzu: Louise Petti:
   * Identity-Namespace: *Luma CRM ID*
   * Identitätswert: *d1f132f9f9502bba047a6ec86c4b61f9*

Ergebnis:

* Die Betreffzeile sollte lauten: Louise, die neue Kollektion von Luma ist hier!

**E-Mail-Nachricht Nr. 2: Herrenkollektion von Luma**

Senden Sie sich selbst eine Test-E-Mail:

1. Fügen Sie ein Testprofil hinzu: Stanleigh Stooke:
   * Identity-Namespace: *Luma CRM ID*
   * Identitätswert: `4f34057d9d9e792c28ba18ecae378e98`
2. Wählen Sie das Testprofil aus: Stanleigh Stooke.
3. Führen Sie einen Testversand an Sie selbst durch.

Ergebnis:\
Sie sollten eine E-Mail erhalten. Die Betreffzeile sollte lauten: *Stanleigh, erkunden Sie die neue Sportbekleidung für Herren!* und der Textkörper der E-Mail sollten mit dem übereinstimmen, was Sie in der Vorschau gesehen haben.

>[!NOTE]
>Es kann einige Minuten dauern, bis Sie die Test-E-Mail erhalten.

**E-Mail-Nachricht Nr. 3: Damenkollektion von Luma**

Zeigen Sie eine Vorschau der E-Mail mit dem Testprofil *Louise Petti* an.

* Die Betreffzeile sollte lauten: *Louise, erkunden Sie die Damenkollektion von Luma!*

**E-Mail-Nachricht Nr. 4: Luma – 20 % Rabatt auf die Kollektion**

Zeigen Sie eine Vorschau der E-Mail mit dem Testprofil *Louise Petti* an.

* Die Betreffzeile sollte lauten: *Louise, erhalten Sie 20% Rabatt auf Ihre Käufe!*

#### Testen der Journey

>[!IMPORTANT]
>
>Bevor Sie die Journey in den Testmodus setzen:
>
>1. Stellen Sie sicher, dass der Namespace für die Aktivität [!UICONTROL Segment lesen] auf **Luma CRM id(lumaCrmId)** eingestellt ist
>1. Überschreiben Sie für jede E-Mail die standardmäßigen E-Mail-Parameter, damit sie an Ihre E-Mail-Adresse gesendet werden:
>    * Zeigen Sie die ausgeblendeten Werte an, indem Sie auf das Augensymbol klicken.
>    * Klicken Sie in den E-Mail-Parametern auf das T-Symbol (Parameterüberschreibungen aktivieren).
>
>      ![E-Mail-Parameter überschreiben](/help/challenges/assets/c3-override-email-paramters.jpg)
> 
>    * Klicken Sie in das Feld [!UICONTROL Adresse]
>    * Fügen Sie im nächsten Bildschirm Ihre E-Mail-Adresse in Klammern hinzu: `"yourname@yourdomain"` im Ausdruckseditor, dann auf „OK“ klicken.
>

Testen Sie die Journey und lassen Sie die E-Mails an Ihr eigenes Konto senden:

1. Setzen Sie die Journey in den Testmodus.
1. Wählen Sie **[!UICONTROL Jeweils ein Einzelprofil]**.
1. Wartezeit: Setzen Sie den Timer auf 120 Sekunden (geben Sie dies in das Feld ein).
1. Auslösen des Profileintritts
1. Sie können jede Verzweigung mit einer der folgenden *Luma CRM-IDs* als Profilkennungen testen:
   * Weiblich: Leora Dietsche, Identitätswert: `a8f14eab3b483c2b96171b575ecd90b1`
   * Männlich: Stanleigh Stooke, Identitätswert: `4f34057d9d9e792c28ba18ecae378e98`
   * Geschlecht nicht angegeben: Louise Petti, Identitätswert: `d1f132f9f9502bba047a6ec86c4b61f9`

1. Nachdem Sie den Profileintritt ausgelöst haben, sollten Sie die erste E-Mail erhalten. Die Kopfzeile sollte entsprechend dem ausgewählten Profil personalisiert sein.
1. Die Journey sollte in der entsprechenden Verzweigung fortgesetzt werden, und Sie sollten die entsprechende E-Mail erhalten (wenn Sie beispielsweise *Jenna* auswählen, sollten Sie die E-Mail *Damenkollektion von Luma* erhalten).
1. Öffnen Sie die zweite E-Mail, und die Journey sollte enden.
1. Sie können Schritt 4 wiederholen. - 7. für alle drei Profile, um zu überprüfen, ob Ihre Verzweigungen ordnungsgemäß funktionieren.
1. Um die Zeitüberschreitungen zu testen, setzen Sie die Wartezeit auf 30 Sekunden und lösen Sie den Eintritt erneut aus.
1. Öffnen Sie die erhaltenen E-Mails nicht (keine Vorschau der E-Mail anzeigen (!)) und lassen Sie die Wartezeit verstreichen.

Sie sollten die folgenden E-Mails erhalten:

* Luma – Ankündigung zur neuen saisonalen Kollektion
* Je nachdem, welches Testprofil Sie verwendet haben, sollten Sie eine der folgenden E-Mails erhalten:
   * Leora: Damenkollektion von Luma
   * Stanleigh: Herrenkollektion von Luma
   * Louise: Luma – 20 % Rabatt auf die Kollektion
* Wenn Sie die zweite E-Mail nicht geöffnet haben: 20 % Rabatt auf die Kollektion von Luma

>[!TAB Überprüfen Sie Ihre Arbeit]

So sollte Ihre Journey aussehen:

![Journey](/help/challenges/assets/c3-j1-journey.png)

**Bedingung – Kontrollgruppe:**

![Kontrollgruppe](/help/challenges/assets/c3-j1-condition-control-group.png)

**Bedingung – Geschlecht:**\

![Bedingung – Geschlecht](/help/challenges/assets/c3-j1-condition-gender.png)
>[!ENDTABS]
