---
title: 'Lektion 4: Erstellen einer Push-Kampagne'
description: Überprüfen Sie Profildaten und erfahren Sie, wie Sie in Journey Optimizer Zielgruppen erstellen und eine Push-Benachrichtigung senden.
feature: Push
role: User
level: Intermediate
doc-type: Tutorial
duration: 0
recommendations: noDisplay, noCatalog
jira: KT-14980
exl-id: 0f82d6a5-18c0-45f2-968e-a678fc2d5768
source-git-commit: befde57252ebc12c5d6df31fde8078e4535d1261
workflow-type: tm+mt
source-wordcount: '781'
ht-degree: 2%

---

# Lektion 4: Erstellen einer Push-Kampagne

In der vorherigen Übung waren Sie ein Kaffeefanatiker, ein Fréscopa-Kunde. Sie haben über ihre Website und die Fréscopa-App mit der Marke interagiert und viele Transaktionsnachrichten erhalten. Diese Nachrichten werden durch die Interaktion des Benutzers mit der Website oder der Anwendung ausgelöst.

In dieser Übung implementieren Sie Ihren Marketingspezialisten, der eine Marketing-Kampagne für Frésopa durchführt, die den Push-Kanal nutzt, um die Benutzer der Fréscopa-App anzusprechen. Push-Benachrichtigungen werden verwendet, um App-Benutzer auf dem Laufenden zu halten, selbst wenn sie die App nicht verwenden, aber auch, um sie erneut mit der App zu verbinden. Ziel ist es, den Kunden durch ein Angebot von 10 % Rabatt zu ermutigen, die Hausmischung zu kaufen.

## Lernziele

* Erfahren Sie, wie Sie eine Push-Kampagne erstellen.
* Hier erfahren Sie, wie Sie eine Push-Nachricht erstellen.

<br>

## Übung 4.1 - Erstellen einer Push-Kampagne

In dieser Übung erstellen Sie die Push-Kampagne, entwerfen und passen die Push-Benachrichtigung an und senden die Push-Benachrichtigung an Ihr eigenes Gerät.

1. Wählen Sie in Journey Optimizer im linken Navigationsbereich im Bereich **[!UICONTROL JOURNEY-MANAGEMENT]** die Option **Kampagnen**.

1. Klicken Sie auf **[!UICONTROL Kampagne erstellen]**.

   ![Kampagne erstellen](/help/summit/l820-lab-workbook/assets/2-3-1-1-create-campaign.png)

1. Aktivieren Sie auf der Seite **[!UICONTROL Kampagne erstellen]** im Abschnitt **[!UICONTROL Aktion]** das Kontrollkästchen **[!UICONTROL Push-Benachrichtigung]** .

1. Wählen Sie aus dem Dropdown-Menü **[!UICONTROL App-Oberfläche]** die Option *[!DNL Frecopa-Push]* aus.

1. Klicken Sie auf **[!UICONTROL Erstellen]** , um eine Push-Kampagne zu erstellen.

   ![App-Oberfläche](/help/summit/l820-lab-workbook/assets/2-3-1-2-app-surface.png)

>[!SUCCESS]
>
>Sie sollten sich jetzt auf der Seite mit den Kampagneneigenschaften befinden:
> ![Kampagneneigenschaften](/help/summit/l820-lab-workbook/assets/2-3-1-2-campaign-properties.png)

## Übung 4.2 - Konfigurieren der Kampagne

Auf dieser Seite konfigurieren Sie die Eigenschaften, die Zielgruppe, die Aktionen und den Zeitplan Ihrer Kampagne.

### 4.2.1 [!UICONTROL Eigenschaftenabschnitt]

Geben Sie Ihrer Kampagne einen Namen. Beginnen Sie den Namen mit Ihrer Sitznummer, damit Sie Ihre Kampagne bei der Suche einfach finden können.

Wenn Ihre Sitznummer beispielsweise 99 ist: `99 - 10% Discount Campaign`.

### 4.2.2 **[!UICONTROL Zielgruppenabschnitt]**

1. Klicken Sie im Audience-Bereich auf **[!UICONTROL Select audience]**.

   ![Audience-Abschnitt](/help/summit/l820-lab-workbook/assets/2-3-2-5-audience-section.png)

1. Suchen Sie im Bildschirm **[!UICONTROL Zielgruppe auswählen]** nach der Zielgruppe:

   **Lab - Sitz`your seat number`**

1. Wählen Sie die Zielgruppe aus und klicken Sie dann auf **[!UICONTROL Speichern]**.

   ![Zielgruppenauswahl](/help/summit/l820-lab-workbook/assets/2-3-2-7-select-audience.png)

### 4.2.3 Inhalt der Push-Benachrichtigung bearbeiten

In dieser Übung entwerfen und passen Sie die Push-Benachrichtigung an.

1. Klicken Sie im Abschnitt **[!UICONTROL Aktion]** auf die Schaltfläche **[!UICONTROL Inhalt bearbeiten]**.

   ![Schaltfläche &quot;Inhalt bearbeiten&quot;](/help/summit/l820-lab-workbook/assets/2-3-action-edit-content-button.png)

1. Wählen Sie auf dem nächsten Bildschirm je nach Mobilgerät entweder die Registerkarte [!DNL iOS™] oder [!DNL Android™] aus, um den Inhalt zu konfigurieren.

>[!BEGINTABS]

>[!TAB iOS]

![Registerkarte &quot;iOS&quot;](/help/summit/l820-lab-workbook/assets/2-3-ios-tab.png)

>[!TAB Android]

![Registerkarte &quot;Android&quot;](/help/summit/l820-lab-workbook/assets/2-3-android-tab.png)

>[!ENDTABS]

#### 4.2.3.1 [!UICONTROL Nachricht erstellen] -Abschnitt

1. **Erstellen Sie Ihre Nachricht:** Fühlen Sie sich frei, beliebigen Text hinzuzufügen. Im Folgenden finden Sie Beispiele für die Verwendung von:

   * Titel: `Get 10% off today!`
   * Textkörper: `Today only! Get 10% off on your House Blend coffee purchase!`

     ![Nachricht erstellen](/help/summit/l820-lab-workbook/assets/2-3-compose-message.png)

#### 4.2.3.2 Ändern Sie das Klick-Verhalten der Nachricht in **Öffnen einer Produktseite**

1. Wählen Sie im Abschnitt **[!UICONTROL Beim Klick-Verhalten]** die Option **[!UICONTROL Deeplink]** aus dem Dropdown-Menü **[!UICONTROL Klick-Verhalten des Textkörpers]**.

1. Kopieren Sie die folgende URL und fügen Sie sie in das Feld **URL** ein:

   `dxdemo://exoticVibes`

   ![Deep-Link](/help/summit/l820-lab-workbook/assets/2-3-deeplink.png)

#### 4.2.3.3 Bild zur Nachricht hinzufügen

1. Klicken Sie im Abschnitt **[!UICONTROL Medien hinzufügen]** auf **[!UICONTROL Medien hinzufügen]**.

   ![Medien-Schaltflächen hinzufügen](/help/summit/l820-lab-workbook/assets/2-3-3-3-add-media-buttons.png)

1. Öffnen Sie im Bildschirm &quot;**[!UICONTROL Assets auswählen]**&quot;im linken Navigationsbereich den Ordner &quot;**Fréscopa&quot;** und wählen Sie ein Bild aus diesem Ordner aus.

   Beispiel: `HouseBlend.png`

1. Klicken Sie auf das Bild und dann auf die Schaltfläche **[!UICONTROL Auswählen]** , um das Bild Ihrer Push-Benachrichtigung hinzuzufügen.

   ![Bild auswählen](/help/summit/l820-lab-workbook/assets/2-3-3-3-select-image.png)

   >[!SUCCESS]
   >
   > 1. Klicken Sie im Vorschaubildschirm auf **[!UICONTROL Ansicht erweitern]**.
   > 1. Vorschau der Nachricht erzeugen
   > <br>
   >
   > ![Ansicht erweitern](/help/summit/l820-lab-workbook/assets/2-3-3-expand-view.png)

### Bonusübungen

Wenn Sie diesen Teil der Übung absolviert haben und dennoch etwas Zeit haben, versuchen Sie die Bonusübung:

+++ Bonusübung

#### Nachricht durch Hinzufügung des Vornamens des Empfängers personalisieren

1. Klicken Sie neben dem Feld **[!UICONTROL Hauptteil]** auf **Personalisierungsdialog**.

   ![Personalisierungsschaltfläche](/help/summit/l820-lab-workbook/assets/2-3-personalization-button.png)

1. Platzieren Sie im Bildschirm **Personalisierungsdialogfeld** den Cursor an die Stelle, an der Sie den Vornamen zum Text hinzufügen möchten.

1. Stellen Sie sicher, dass die **Profilattribute** im linken Navigationsbereich ausgewählt sind.

   ![Profilattribut](/help/summit/l820-lab-workbook/assets/2-3-personalize-body-profile-attributes.png)

1. Suchen Sie im **Suchfeld** nach: `first name`.

1. Klicken Sie auf **+** neben dem Vornamen (Profilattribute > Person > Vollständiger Name)**, um das Personalisierungsfeld zu Ihrem Text hinzuzufügen.**

   ![Suche nach Vorname](/help/summit/l820-lab-workbook/assets/2-3-personalize-search-first-name.png)

   >[!SUCCESS]
   >
   > So sollte Ihr Text aussehen:
   > 
   >![Personalization-Token](/help/summit/l820-lab-workbook/assets/2-3-personalization-token.png)

1. Klicken Sie auf **[!UICONTROL Speichern]** , um die Personalisierung zu speichern.


   >[!SUCCESS]
   >
   > 1. Klicken Sie im Vorschaubildschirm auf **[!UICONTROL Ansicht erweitern]**.
   > 1. Vorschau der Nachricht erzeugen
   > 
   > ![Ansicht erweitern](/help/summit/l820-lab-workbook/assets/2-3-3-expand-view.png)

+++

### 4.2.4. Überprüfen und aktivieren

Wenn Sie mit dem Inhalt Ihrer Nachricht zufrieden sind, können Sie die Nachricht aktivieren:

1. Klicken Sie auf **[!UICONTROL Überprüfen, um zu aktivieren]**.

   ![Schaltfläche &quot;Überprüfen und aktivieren&quot;](/help/summit/l820-lab-workbook/assets/2-3-4-review-and-activate-button.png)

1. Klicken Sie im Bildschirm **[!UICONTROL Überprüfen, um]** zu aktivieren, auf **[!UICONTROL Aktivieren]**.

   ![Überprüfen, um Bildschirm zu aktivieren](/help/summit/l820-lab-workbook/assets/2-3-4-review-to-activate.png)

>[!SUCCESS]
> Suchen Sie auf der Übersichtsseite **Kampagnen** Ihre Kampagne und überprüfen Sie den Status.
>
> ![Kampagnenstatus](/help/summit/l820-lab-workbook/assets/2-3-push-completed.png)
> 
> Der Status wechselt von der Verarbeitung zur Live-Schaltung zu &quot;Abgeschlossen&quot;. Dies kann einige Minuten dauern.
> Sobald der Status abgeschlossen ist:
>
> ![Push-Ergebnisse](/help/summit/l820-lab-workbook/assets/2-3-push-notification-result.png)

## Zusätzliche Ressourcen

**Videos:**

* [Konfigurieren und Senden von Push-Kampagnen](/help/channels/create-a-push-campaign.md)

**Produktdokumentation:**

* [Erste Schritte mit der Push-Benachrichtigung](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/push/get-started-push)
* [Erstellen einer Push-Benachrichtigung](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/push/create-push)
* [Gestalten einer Push-Benachrichtigung](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/push/design-push)
* [Überprüfen und Senden Ihrer Push-Benachrichtigung](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/push/send-push)
