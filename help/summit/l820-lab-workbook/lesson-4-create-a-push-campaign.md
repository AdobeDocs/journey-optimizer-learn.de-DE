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
source-git-commit: c590b47ad3dfc54badbac0d8fcaff6b9dd053cc1
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 0%

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

1. In Journey Optimizer im linken Navigationsbereich im **[!UICONTROL JOURNEY MANAGEMENT]** Bereich, wählen Sie **Kampagnen**.

1. Klicks **[!UICONTROL Kampagne erstellen]**.

   ![Kampagne erstellen](/help/summit/l820-lab-workbook/assets/2-3-1-1-create-campaign.png)

1. Im **[!UICONTROL Kampagne erstellen]** in der  **[!UICONTROL Aktion]** auswählen, wählen Sie die **[!UICONTROL Push-Benachrichtigung]** aktivieren.

1. Aus dem **[!UICONTROL Anwendungsoberfläche]** Dropdown-Liste auswählen *[!DNL Frecopa-Push]*.

1. Klicks **[!UICONTROL Erstellen]** , um eine Push-Kampagne zu erstellen.

   ![Anwendungsoberfläche](/help/summit/l820-lab-workbook/assets/2-3-1-2-app-surface.png)

>[!SUCCESS]
>
>Sie sollten sich jetzt auf der Seite mit den Kampagneneigenschaften befinden:
> ![Kampagneneigenschaften](/help/summit/l820-lab-workbook/assets/2-3-1-2-campaign-properties.png)

## Übung 4.2 - Konfigurieren der Kampagne

Auf dieser Seite konfigurieren Sie die Eigenschaften, die Zielgruppe, die Aktionen und den Zeitplan Ihrer Kampagne.

### 4.2.1 [!UICONTROL Eigenschaftenabschnitt]

Geben Sie Ihrer Kampagne einen Namen. Beginnen Sie den Namen mit Ihrer Sitznummer, damit Sie Ihre Kampagne bei der Suche einfach finden können.

Wenn Ihre Sitznummer beispielsweise 99 ist: `99 - 10% Discount Campaign`.

### 4.2.2 **[!UICONTROL Zielgruppenbereich]**

1. Klicken Sie im Audience-Bereich auf **[!UICONTROL Zielgruppe auswählen]**.

   ![Audience-Bereich](/help/summit/l820-lab-workbook/assets/2-3-2-5-audience-section.png)

1. Im **[!UICONTROL Zielgruppe auswählen]** -Bildschirm, suchen Sie nach der Zielgruppe:

   **Lab - Sitz`your seat number`**

1. Wählen Sie die Zielgruppe aus und klicken Sie auf **[!UICONTROL Speichern]**.

   ![Zielgruppenauswahl](/help/summit/l820-lab-workbook/assets/2-3-2-7-select-audience.png)

### 4.2.3 Inhalt der Push-Benachrichtigung bearbeiten

In dieser Übung entwerfen und passen Sie die Push-Benachrichtigung an.

1. Im **[!UICONTROL Aktion]** klicken Sie auf die **[!UICONTROL Inhalt bearbeiten] button**.

   ![Schaltfläche &quot;Inhalt bearbeiten&quot;](/help/summit/l820-lab-workbook/assets/2-3-action-edit-content-button.png)

1. Wählen Sie auf dem nächsten Bildschirm je nach Mobilgerät entweder [!DNL iOS™] oder [!DNL Android™] um den Inhalt zu konfigurieren.

>[!BEGINTABS]

>[!TAB iOS]

![iOS-Registerkarte](/help/summit/l820-lab-workbook/assets/2-3-ios-tab.png)

>[!TAB Android]

![Android-Registerkarte](/help/summit/l820-lab-workbook/assets/2-3-android-tab.png)

>[!ENDTABS]

#### 4.2.3.1 [!UICONTROL Nachricht erstellen] Abschnitt

1. **Erstellen Sie Ihre Nachricht:** Sie können beliebig beliebigen Text hinzufügen. Im Folgenden finden Sie Beispiele für die Verwendung von:

   * Titel: `Get 10% off today!`
   * Textkörper: `Today only! Get 10% off on your House Blend coffee purchase!`

     ![Nachricht erstellen](/help/summit/l820-lab-workbook/assets/2-3-compose-message.png)

#### 4.2.3.2 Ändern Sie das Klick-Verhalten der Nachricht in **Produktseite öffnen**

1. Im **[!UICONTROL Klickverhalten]** Bereich, wählen Sie **[!UICONTROL Deeplink]** aus dem **[!UICONTROL Klick-Verhalten des Textkörpers]** Dropdown.

1. Kopieren Sie die folgende URL und fügen Sie sie in die **URL-Feld**:

   `dxdemo://exoticVibes`

   ![Deep-Link](/help/summit/l820-lab-workbook/assets/2-3-deeplink.png)

#### 4.2.3.3 Bild zur Nachricht hinzufügen

1. Im **[!UICONTROL Medien hinzufügen]** Abschnitt, klicken Sie auf **[!UICONTROL Medien hinzufügen]**.

   ![Medien-Schaltflächen hinzufügen](/help/summit/l820-lab-workbook/assets/2-3-3-3-add-media-buttons.png)

1. Im **[!UICONTROL Auswählen von Assets]** in der linken Navigation öffnen Sie die **Ordner &quot;Fréscopa&quot;** und wählen Sie ein Bild aus diesem Ordner aus.

   Beispiel: `HouseBlend.png`

1. Klicken Sie auf das Bild und klicken Sie auf das **[!UICONTROL Auswählen] button** , um das Bild zu Ihrer Push-Benachrichtigung hinzuzufügen.

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

1. Klicks **Personalisierungsdialogfeld** neben dem **[!UICONTROL body]** -Feld.

   ![Personalisierungsschaltfläche](/help/summit/l820-lab-workbook/assets/2-3-personalization-button.png)

1. Im **Personalisierungsdialogfeld** platzieren Sie den Cursor an die Stelle, an der Sie den Vornamen im Text hinzufügen möchten.

1. Stellen Sie sicher, dass **Profilattribute** werden im linken Navigationsbereich ausgewählt.

   ![Profilattribut](/help/summit/l820-lab-workbook/assets/2-3-personalize-body-profile-attributes.png)

1. Im **Suchfeld**, suchen Sie nach: `first name`.

1. Klicks **+** neben dem **Vorname (Profilattribute > Person > Vollständiger Name)** , um das Personalisierungsfeld zu Ihrem Text hinzuzufügen.

   ![Suchen nach Vornamen](/help/summit/l820-lab-workbook/assets/2-3-personalize-search-first-name.png)

   >[!SUCCESS]
   >
   > So sollte Ihr Text aussehen:
   > 
   >![Personalisierungstoken](/help/summit/l820-lab-workbook/assets/2-3-personalization-token.png)

1. Klicks **[!UICONTROL Speichern]** , um die Personalisierung zu speichern.


   >[!SUCCESS]
   >
   > 1. Klicken Sie im Vorschaubildschirm auf **[!UICONTROL Ansicht erweitern]**.
   > 1. Vorschau der Nachricht erzeugen
   > 
   > ![Ansicht erweitern](/help/summit/l820-lab-workbook/assets/2-3-3-expand-view.png)

+++

### 4.2.4. Überprüfen und aktivieren

Wenn Sie mit dem Inhalt Ihrer Nachricht zufrieden sind, können Sie die Nachricht aktivieren:

1. Klicks **[!UICONTROL Aktivieren]**.

   ![Schaltfläche zum Überprüfen und Aktivieren](/help/summit/l820-lab-workbook/assets/2-3-4-review-and-activate-button.png)

1. Im **[!UICONTROL Aktivieren]** Bildschirm, klicken Sie **[!UICONTROL Aktivieren]**.

   ![Überprüfen, um den Bildschirm zu aktivieren](/help/summit/l820-lab-workbook/assets/2-3-4-review-to-activate.png)

>[!SUCCESS]
> Im **Übersichtsseite der Kampagnen**, suchen Sie Ihre Kampagne und überprüfen Sie den Status.
>
> ![Kampagnenstatus](/help/summit/l820-lab-workbook/assets/2-3-push-completed.png)
> 
> Der Status wechselt von der Verarbeitung zur Live-Schaltung zu &quot;Abgeschlossen&quot;. Dies kann einige Minuten dauern.
> Sobald der Status abgeschlossen ist:
>
> ![Push-Ergebnisse](/help/summit/l820-lab-workbook/assets/2-3-push-notification-result.png)


**Danke!**

Danke für Ihre Teilnahme. Bitte teilen Sie uns mit, wie und ob das Labor Ihre Erwartungen erfüllt hat, indem Sie die Lab 820 Session Umfrage in der Summit App abschließen.

