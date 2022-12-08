---
title: Ankündigung zur Sommerkollektion erstellen - Herausforderung
description: Senden Sie eine Mitteilung zur Sommerkollektion an ein Segment bestehender Kunden, um die neue Sommerkollektion von Luma zu bewerben.
kt: 8109
role: User
level: Beginner
last-substantial-update: 2022-11-16T00:00:00Z
hide: true
exl-id: ae457be7-2c67-4950-a072-1d7030b0e17b
source-git-commit: cfd438e198fdf62859569eed0c6ac22087ddbc75
workflow-type: tm+mt
source-wordcount: '1176'
ht-degree: 2%

---

# Ankündigung zur Sommerkollektion erstellen - Herausforderung

![Ankündigungsbanner für AJO-Sommerkollektionen](/help/challenges/assets/email-assets/luma-transactional-onboarding-3.png)

| Herausforderung | Ankündigung zur Sommerkollektion erstellen |
|---|---|
| Persona | Journey-Manager |
| Erforderliche Fähigkeiten | <ul><li>[Erstellen von Segmenten](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/profiles-segments-subscriptions/create-segments.html?lang=en)</li><li> [Importieren und Erstellen von HTML-E-Mail-Inhalten](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-messages/create-emails/import-and-author-html-email-content.html?lang=en)</li><li>[Anwendungsfall: Segment lesen](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/use-case-read-segment.html?lang=en)</li> |
| Herunterzuladende Assets | [Saisonale Sammlungs-E-Mail-Dateien](/help/challenges/assets/email-assets/emails-seasonal-collection-announcement.zip) |

## Die Geschichte

Luma, ein fiktionales Sportbekleidungsunternehmen, vermarktet die neueste Bekleidung und Zahnradsammlung und fördert den Umsatz für bestehende Kunden. Luma startet die neue Sommerkollektion und möchte speziell auf verschiedene Kundensegmente abzielen.

## Ihre Herausforderung

Das Marketing-Team von Luma bittet Sie, eine Marketing-Kampagne für Sommerkollektionen in Journey Optimizer zu implementieren. Ihre Herausforderung besteht darin,

* Erstellen Sie ein Segment, das definiert, welche Profile für den Erhalt der Promotion qualifiziert sind.
* Erstellen der Journey.

### Schritt 1: Definieren des Segments - Aktive Kunden

>[!BEGINTABS]

>[!TAB Aufgabe]

#### Erstellen Sie ein Segment in [!DNL Journey Optimizer]

* Erstellen Sie ein Segment in [!DNL Journey Optimizer] aufgerufen *Aktive Kunden*.
* Das Segment darf nur aktive Luma-Kunden umfassen.
* Aktive Kunden werden definiert als Kunden, die eine Ebene im Treueprogramm von Luma haben (Bronze, Silber, Gold oder Platin).


>[!TAB Erfolgskriterien]

Im Segment Builder können Sie die geschätzte Anzahl qualifizierter Profile anzeigen. Wenn Sie mit den Daten der Trainings-Sandbox arbeiten, verfügen Sie über rund 753 qualifizierte Profile von 1,29 K.

>[!NOTE]
>Es kann bis zu 24 Stunden dauern, bis die Segmentzugehörigkeit für vorhandene Profile angezeigt wird, da die vorhandenen Profile aufgestockt werden müssen.

**Dem Segment wurde ein qualifizierendes Profil hinzugefügt:**

Sie können die Qualifizierung der Profile überprüfen, die zum Segment hinzugefügt wurden, indem Sie in den in der Detailansicht Ihres Segments aufgelisteten Profilen zu navigieren.

Überprüfen Sie auf der Profilseite die [!UICONTROL Attribute] zur Bestätigung, dass sie sich qualifizieren: Die Ebene sollte Silber, Gold, Platin oder Diamant sein.

![Profilattribute](assets/C1-S1-profile-attributes.png)

Sie können auch die [!UICONTROL Segmentmitgliedschaft] tab: Ihr Segment sollte aufgelistet werden.

![Segmentzugehörigkeit](assets/C1-S1-profile-segment-membership.png)

>[!TAB Überprüfen Sie Ihre Arbeit]

Segmentfelder: [!UICONTROL Attribute] > [!UICONTROL XDM-individuelles Profil] > [!UICONTROL Treue] > [!UICONTROL Ebene]

So sollte Ihr Segment aussehen:

![Segment - Aktive Kunden](/help/challenges/assets/C1-S1.png)

Der Code sollte wie folgt aussehen:

```javascript
stringCompare("equals", loyalty.tier, ["diamond", "gold", "platinum", "silver"], false)
```

>[!ENDTABS]


### Schritt 2: Journey erstellen - Ankündigung zur Sommerkollektion

>[!BEGINTABS]

>[!TAB Aufgabe]

#### Mitteilung zur Sommerkollektion senden

Eine Agentur stellte Ihnen vier HTML-Dateien mit dem Design für E-Mails zur Verfügung:

* `SeasonalCollectionEmail.html`
* Luma Men&#39;s Collection E-Mail
* Luma Women&#39;s Collection E-Mail
* Luma - 20 % Rabatt auf E-Mail-Erfassung

1. [Herunterladen der E-Mail-Dateien der saisonalen Sammlung](/help/challenges/assets/email-assets/emails-seasonal-collection-announcement.zip).

2. Erstellen Sie eine Journey mit dem Namen *Luma - Ankündigung zur Sommerkollektion* auf der Grundlage der folgenden Leitlinien:

   1. Senden *Luma - Ankündigung der neuen Sommerkollektion* E-Mail an die *Aktive Kunden* Segment, das 10 % der Zielgruppe als Kontrollgruppe ausmacht
      * Nachrichtentitel *Luma - Ankündigung zur Sommerkollektion*
      * Betreff *(Vorname des Empfängers), die neue Luma Sommerkollektion ist hier!*
      * Verwenden Sie die bereitgestellte HTML-Datei `SeasonalCollectionEmail.html` für den E-Mail-Textkörper.
   2. Warten Sie zwei Tage und senden Sie dann eine Folgenachricht mit zielgerichteteren Inhalten:
      * Männliche Kunden sollten die **Luma Men&#39;s Collection** E-Mail.
         * Nachrichtentitel: *Luma Men&#39;s Collection*
         * Betreffzeile: *(Vorname des Empfängers), erforschen Sie Men&#39;s New Athletic Ausrüstung!*
         * E-Mail-Hauptteil: `MensCollectionEmail.html` für den E-Mail-Textkörper.
      * Weibliche Kunden sollten die **Luma Women&#39;s Collection** E-Mail.
         * Nachrichtentitel: *Luma Women&#39;s Collection*
         * Betreffzeile: *(Vorname des Empfängers), entdecken Sie Lumas Frauensammlung!*
         * E-Mail-Hauptteil: `WomensCollectionEmail.html`
      * Andere Kunden sollten **Luma - 20 % Ermäßigung der Sammlung** E-Mail.
         * Nachrichtentitel: *Luma - 20 % Ermäßigung der Sammlung*
         * Betreffzeile: *(Vorname des Empfängers), 20% Rabatt auf den Umsatz!*
         * E-Mail-Hauptteil: `20OOffCollectionEmail.html`
   3. Warten Sie nach dem Versand der oben genannten zielgerichteten E-Mails zwei Tage, bis die E-Mail geöffnet wird.
   4. Wenn die gewünschte E-Mail nicht innerhalb von 2 Tagen geöffnet wird, senden Sie die **Luma - 20 % der Sammlungs-E-Mail** als letzten Retargeting-Versuch


>[!TAB Erfolgskriterien]

#### Vorschau der E-Mails

**E-Mail-Nachricht Nr. 1: Luma - Mitteilung zur Sommerkollektion**

Vorschau der E-Mail:

1. Fügen Sie ein Testprofil hinzu: Louise Petti:
   1. Identitäts-Namespace: *Luma CRM ID*
   2. Identitätswert: *d1f132f9f9502bba047a6ec86c4b61f9*

Ergebnis:
* Die Betreffzeile sollte lauten: Louise, die neue Luma Kollektion ist da!
* Der Hauptteil der E-Mail sollte mit dem übereinstimmen, was Sie in der Vorschau gesehen haben: [Neue Mitteilung zur saisonalen Sammlung](/help/challenges/assets/email-assets/SeasonalCollectionEmail.html)


**E-Mail-Nachricht Nr. 2: Luma Men&#39;s Collection**

Senden Sie einen Testversand an sich:

1. Fügen Sie ein Testprofil hinzu: Stanleigh Stooke:
   1. Identitäts-Namespace: *Luma CRM ID*
   1. Identitätswert: `4f34057d9d9e792c28ba18ecae378e98`
1. Wählen Sie das Testprofil aus: Stanleigh Stooke.
1. Schicken Sie sich einen Testversand.

Ergebnis:\
Sie sollten eine E-Mail erhalten. Die Betreffzeile sollte lesen *Stanleigh, erforschen Sie die neue Sportausrüstung von Men&#39;s New!* und der E-Mail-Textkörper sollte mit dem übereinstimmen, was Sie in der Vorschau gesehen haben: [Luma Men&#39;s Collection](/help/challenges/assets/email-assets/MensCollectionEmail.html)

>[!NOTE]
>Es kann einige Minuten dauern, bis Sie den Testversand erhalten.

**E-Mail-Nachricht Nr. 3: Luma Women&#39;s Collection**

Vorschau der E-Mail mit dem Testprofil *Louise Petti.*

* Die Betreffzeile sollte lauten: *Louise, entdecken Sie Lumas Frauensammlung!*
* Der Hauptteil der E-Mail sollte mit dem übereinstimmen, was Sie in der Vorschau gesehen haben: [Luma Women&#39;s Collection](/help/challenges/assets/email-assets/WomensCollectionEmail.html)


**E-Mail-Nachricht Nr. 4: Luma - 20 % Rabatt**

Vorschau der E-Mail mit dem Testprofil *Louise Petti.*

* Die Betreffzeile sollte lauten: *Louise, genießen Sie 20% Rabatt!*
* Der Hauptteil der E-Mail sollte mit dem übereinstimmen, was Sie in der Vorschau gesehen haben: [Luma: 20 % Abholung](/help/challenges/assets/email-assets/20OOffCollectionEmail.html)


#### Testen einer Journey

>[!IMPORTANT]
>
>Bevor Sie die Journey in den Testmodus einstellen:
>
>1. Stellen Sie sicher, dass die Variable [!UICONTROL Segmentaktivität lesen] hat den Namespace auf **Luma CRM id(lumaCrmId)**
>1. Überschreiben Sie für jede E-Mail die Standard-E-Mail-Parameter für die E-Mails, damit sie an Ihre E-Mail-Adresse gesendet werden:
   >    * Zeigen Sie die verborgenen Werte an, indem Sie auf das Augensymbol klicken.
   >    * Klicken Sie in den E-Mail-Parametern auf das T-Symbol (Parameter überschreiben aktivieren).

      >
      >      ![E-Mail-Parameter überschreiben](/help/challenges/assets/c3-override-email-paramters.jpg)
   > 
   >    * Klicken Sie in die [!UICONTROL Adresse] field
   >    * Fügen Sie im nächsten Bildschirm Ihre E-Mail-Adresse in Klammern hinzu: `"yourname@yourdomain"` im Ausdruckseditor und klicken Sie auf &quot;OK&quot;.

>


Testen Sie die Journey und lassen Sie die E-Mails an Ihr eigenes Konto senden:

1. Setzen Sie die Journey in den Testmodus.
1. Wählen Sie jeweils ein Profil aus.
1. Wartezeit: Setzen Sie den Timer auf 120 Sekunden (geben Sie ihn in das Feld ein).
1. Trigger-Profileingang
1. Sie können jede Verzweigung mit einer der folgenden Methoden testen *Luma CRM-IDs* als Profilkennungen:
   * Weiblich: Leora Dietsche, Identitätswert:`a8f14eab3b483c2b96171b575ecd90b1`
   * Männlich: Stanleigh Stooke, Identitätswert: `4f34057d9d9e792c28ba18ecae378e98`
   * Geschlecht nicht angegeben: Louise Petti, Identitätswert: `d1f132f9f9502bba047a6ec86c4b61f9`

1. Nachdem Sie den Profileingang Trigger haben, sollten Sie die erste E-Mail erhalten. Die Kopfzeile sollte entsprechend dem ausgewählten Profil personalisiert werden.
1. Die Journey sollte in der entsprechenden Verzweigung fortgesetzt werden und Sie sollten die entsprechende E-Mail erhalten (z. B. wenn Sie *Jenna*, sollten Sie die *Luma Women&#39;s Collection* E-Mail).
1. Öffnen Sie die zweite E-Mail und die Journey sollte enden.
1. Sie können Schritt 4 wiederholen. - 7. für alle drei Profile, um zu überprüfen, ob Ihre Verzweigungen ordnungsgemäß funktionieren.
1. Um die Zeitüberschreitungen zu testen, setzen Sie die Wartezeit auf 30 Sekunden und Trigger Sie den Eintrag erneut.
1. Öffnen Sie nicht die E-Mails, die Sie erhalten (keine Vorschau der E-Mail anzeigen (!)) und die Wartezeit verlängern.

Sie sollten die folgenden E-Mails erhalten:

* Luma - Neue Ankündigung zur saisonalen Sammlung
* Je nachdem, welches Testprofil Sie verwendet haben, sollten Sie eine der folgenden E-Mails erhalten:
   * Leora: Luma Women&#39;s Collection
   * Stanleigh: Luma Men&#39;s Collection
   * Louise: Luma - 20 % Rabatt auf Sammlung
* Wenn Sie die zweite E-Mail nicht geöffnet haben: Die Luma - 20 % Rabatt

>[!TAB Überprüfen Sie Ihre Arbeit]

So sollte Ihre Journey aussehen:

![Journey](/help/challenges/assets/c3-j1-journey.png)

**Bedingung - Kontrollgruppe:**

![Kontrollgruppe](/help/challenges/assets/c3-j1-condition-control-group.png)

**Bedingung - Geschlecht:**\

![Bedingung - Geschlecht](/help/challenges/assets/c3-j1-condition-gender.png)
>[!ENDTABS]
