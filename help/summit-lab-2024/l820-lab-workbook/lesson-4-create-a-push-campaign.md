---
title: 'Lektion 4: Erstellen einer Push-Kampagne'
description: Überprüfen Sie Profildaten und erfahren Sie, wie Sie Zielgruppen in Journey Optimizer erstellen und eine Push-Benachrichtigung senden.
feature: Push
role: User
level: Intermediate
doc-type: Tutorial
duration: 0
recommendations: noDisplay, noCatalog
jira: KT-14980
exl-id: 0f82d6a5-18c0-45f2-968e-a678fc2d5768
source-git-commit: 55ba1a46c1473d94847e7fccc69ed2a33badb54c
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 2%

---

# Lektion 4: Erstellen einer Push-Kampagne

In der vorherigen Übung waren Sie ein Kaffee-Enthusiast, ein Fréscopa-Kunde. Sie haben über ihre Website und die Fréscopa-App mit der Marke interagiert und viele Transaktionsnachrichten erhalten. Diese Nachrichten werden durch die Interaktion des Benutzers mit der Website oder der Anwendung ausgelöst.

In dieser Übung setzen Sie Ihren Marketer-Hut auf und implementieren eine Marketing-Kampagne für Frésopa, die den Push-Kanal nutzt, um die Benutzenden der Fréscopa-App anzusprechen. Push-Benachrichtigungen werden verwendet, um App-Benutzer zu informieren, auch wenn sie die App nicht verwenden, aber auch, um sie erneut mit der App zu interagieren. Ziel ist es, den Kunden durch einen Rabatt von 10 % zum Kauf der Hausmischung zu motivieren.

## Lernziele

* Wissen, wie man eine Push-Kampagne erstellt.
* Verstehen, wie man eine Push-Nachricht entwirft.

<br>

## Übung 4.1 - Erstellen einer Push-Kampagne

In dieser Übung erstellen Sie die Push-Kampagne, entwerfen und passen die Push-Benachrichtigung an und senden die Push-Benachrichtigung an Ihr eigenes Gerät.

1. Wählen Sie in Journey Optimizer im linken Navigationsbereich im Abschnitt **[!UICONTROL JOURNEY-MANAGEMENT]** die Option **Kampagnen**.

1. Klicken Sie **[!UICONTROL Kampagne erstellen]**.

   ![Kampagne erstellen](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-1-1-create-campaign.png)

1. Aktivieren Sie auf **[!UICONTROL Seite]** Kampagne erstellen“ im Abschnitt **[!UICONTROL Aktion]** das Kontrollkästchen **[!UICONTROL Push]**.

1. Wählen Sie im Dropdown **[!UICONTROL Menü]** Programmoberfläche“ die Option *[!DNL Frecopa-Push]* aus.

1. Klicken Sie **[!UICONTROL Erstellen]**, um eine Push-Kampagne zu erstellen.

   ![Programmoberfläche](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-1-2-app-surface.png)

>[!SUCCESS]
>
>Sie sollten sich jetzt auf der Seite Kampagneneigenschaften befinden:
> ![Kampagneneigenschaften](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-1-2-campaign-properties.png)

## Übung 4.2 - Kampagne konfigurieren

Auf dieser Seite konfigurieren Sie die Eigenschaften, die Audience, die Aktionen und den Zeitplan Ihrer Kampagne.

### 4.2.1 [!UICONTROL Abschnitt „Eigenschaften“]

Geben Sie Ihrer Kampagne einen Namen. Achten Sie darauf, den Namen mit Ihrer Sitznummer zu beginnen, damit Sie Ihre Kampagne bei der Suche leicht finden können.

Wenn Ihre Sitznummer beispielsweise 99: `99 - 10% Discount Campaign` lautet.

### 4.2.2 **[!UICONTROL Zielgruppenbereich]**

1. Klicken Sie im Abschnitt Audience auf **[!UICONTROL Audience auswählen]**.

   ![Audience-Abschnitt](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-2-5-audience-section.png)

1. Suchen Sie auf dem **[!UICONTROL Zielgruppe auswählen]** nach der Zielgruppe:

   **Lab -`your seat number`**

1. Wählen Sie die Audience aus und klicken Sie dann auf **[!UICONTROL Speichern]**.

   ![Zielgruppenauswahl](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-2-7-select-audience.png)

### 4.2.3 Bearbeiten des Inhalts der Push-Benachrichtigung

In dieser Übung entwerfen und passen Sie die Push-Benachrichtigung an.

1. Klicken Sie **[!UICONTROL Abschnitt]** Aktion“ auf die Schaltfläche **[!UICONTROL Inhalt ]bearbeiten**.

   ![Schaltfläche „Inhalt bearbeiten“](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-action-edit-content-button.png)

1. Wählen Sie im nächsten Bildschirm je nach vorhandenem Mobilgerät entweder die Registerkarte [!DNL iOS™] oder [!DNL Android™] aus, um Ihre Inhalte zu konfigurieren.

>[!BEGINTABS]

>[!TAB iOS]

Registerkarte ![iOS](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-ios-tab.png)

>[!TAB Android]

Registerkarte ![Android](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-android-tab.png)

>[!ENDTABS]

#### 4.2.3.1 [!UICONTROL Nachricht erstellen] Abschnitt

1. **Nachricht verfassen:** können gerne Text hinzufügen. Im Folgenden finden Sie Beispiele, die Sie verwenden können:

   * Titel: `Get 10% off today!`
   * Textkörper: `Today only! Get 10% off on your House Blend coffee purchase!`

     ![Nachricht erstellen](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-compose-message.png)

#### 4.2.3.2 Ändern Sie das Klickverhalten der Nachricht, um **eine Produktseite zu öffnen**

1. Wählen Sie im Abschnitt **[!UICONTROL Klickverhalten]** die Option **[!UICONTROL Deeplink]** aus der Dropdown-Liste **[!UICONTROL Klickverhalten des Textkörpers]**.

1. Kopieren Sie die folgende URL und fügen Sie sie im Feld **URL** ein:

   `dxdemo://exoticVibes`

   ![Deep-Link](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-deeplink.png)

#### 4.2.3.3 Hinzufügen eines Bildes zur Nachricht

1. Klicken Sie **[!UICONTROL Abschnitt &quot;]** hinzufügen“ auf **[!UICONTROL Medien hinzufügen]**.

   ![Medien-Schaltflächen hinzufügen](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-3-3-add-media-buttons.png)

1. Öffnen Sie im Bildschirm **[!UICONTROL Assets auswählen]** im linken Navigationsbereich den **Fréscopa-Ordner** und wählen Sie ein Bild aus diesem Ordner aus.

   Beispiel: `HouseBlend.png`

1. Klicken Sie auf das Bild und dann auf **[!UICONTROL Auswählen],** das Bild zu Ihrer Push-Benachrichtigung hinzuzufügen.

   ![Bild auswählen](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-3-3-select-image.png)

   >[!SUCCESS]
   >
   > 1. Klicken Sie im Bildschirm Vorschau auf **[!UICONTROL Ansicht erweitern]**.
   > 1. Vorschau der Nachricht
   > <br>
   >
   > ![Ansicht erweitern](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-3-expand-view.png)

### Bonusübung

Wenn Sie diesen Teil der Übung abgeschlossen haben und noch etwas Zeit haben, versuchen Sie die Bonusübung:

+++ Bonusübung

#### Personalisieren Sie die Nachricht, die Sie senden, indem Sie den Vornamen des Empfängers hinzufügen.

1. Klicken Sie **Personalisierungsdialog** neben dem Feld **[!UICONTROL Hauptteil]**.

   ![Personalisierungsschaltfläche](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-personalization-button.png)

1. Platzieren Sie **Bildschirm „Personalisierungsdialog** den Cursor an die Stelle, an der Sie den Vornamen zum Text hinzufügen möchten.

1. Stellen Sie sicher **dass im linken Navigationsbereich** Profilattribute“ ausgewählt sind.

   ![Profilattribut](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-personalize-body-profile-attributes.png)

1. Suchen Sie **Feld &quot;**&quot; nach: `first name`.

1. Klicken Sie auf **+** neben **Vorname (Profilattribute>Person>Vollständiger Name)**, um das Personalisierungsfeld zu Ihrem Text hinzuzufügen.

   ![Nach Vornamen suchen](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-personalize-search-first-name.png)

   >[!SUCCESS]
   >
   > So sollte Ihr Text aussehen:
   > 
   >![Personalization-Token](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-personalization-token.png)

1. Klicken Sie **[!UICONTROL Speichern]**, um die Personalisierung zu speichern.


   >[!SUCCESS]
   >
   > 1. Klicken Sie im Bildschirm Vorschau auf **[!UICONTROL Ansicht erweitern]**.
   > 1. Vorschau der Nachricht
   > 
   > ![Ansicht erweitern](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-3-expand-view.png)

+++

### 4.2.4. Überprüfung und Aktivierung

Wenn Sie mit dem Inhalt Ihrer Nachricht zufrieden sind, können Sie die Nachricht aktivieren:

1. Klicken Sie auf **[!UICONTROL Zum Aktivieren überprüfen]**.

   ![Schaltfläche „Überprüfen und aktivieren](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-4-review-and-activate-button.png)

1. Klicken Sie auf dem **[!UICONTROL Zu aktivierende Überprüfung]** auf **[!UICONTROL Aktivieren]**.

   ![Zum Aktivieren überprüfen](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-4-review-to-activate.png)

>[!SUCCESS]
> Suchen Sie auf der **Übersichtsseite Kampagnen** nach Ihrer Kampagne und überprüfen Sie den Status.
>
> ![Kampagnenstatus](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-push-completed.png)
> 
> Der Status ändert sich von Verarbeitung zu Live und zu Abgeschlossen . Dies kann einige Minuten dauern.
> Sobald der Status auf „Abgeschlossen“ geändert wurde:
>
> ![Push-Ergebnisse](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-push-notification-result.png)

## Weitere Ressourcen

**Anleitungsvideos:**

* [Konfigurieren und Senden von Push-Kampagnen](/help/channels/create-a-push-campaign.md)

**Produktdokumentation:**

* [Erste Schritte mit Push-Benachrichtigungen](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/push/get-started-push)
* [Erstellen einer Push-Benachrichtigung](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/push/create-push)
* [Gestalten einer Push-Benachrichtigung](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/push/design-push)
* [Push-Benachrichtigung überprüfen und senden](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/push/send-push)
