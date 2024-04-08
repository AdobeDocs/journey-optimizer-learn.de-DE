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
source-git-commit: befde57252ebc12c5d6df31fde8078e4535d1261
workflow-type: tm+mt
source-wordcount: '781'
ht-degree: 2%

---

# Lektion 4: Erstellen einer Push-Kampagne

In der vorherigen Übung waren Sie ein Kaffee-Enthusiast, ein Fréscopa-Kunde. Sie haben über ihre Website und die Fréscopa-App mit der Marke interagiert und viele Transaktionsnachrichten erhalten. Diese Nachrichten werden durch die Interaktion des Benutzers mit der Website oder der Anwendung ausgelöst.

In dieser Übung setzen Sie Ihren Marketing-Hut auf und implementieren eine Marketing-Kampagne für Fréscopa, die den Push-Kanal nutzen wird, um die Benutzer der Fréscopa-App anzusprechen. Push-Benachrichtigungen werden verwendet, um App-Benutzer zu informieren, auch wenn sie die App nicht verwenden, aber auch, um sie erneut mit der App zu interagieren. Ziel ist es, den Kunden durch einen Rabatt von 10 % zum Kauf der Hausmischung zu motivieren.

## Lernziele

* Wissen, wie man eine Push-Kampagne erstellt.
* Erfahren Sie, wie Sie eine Push-Benachrichtigung entwerfen.

<br>

## Übung 4.1 - Erstellen einer Push-Kampagne

In dieser Übung erstellen Sie die Push-Kampagne, entwerfen und passen die Push-Benachrichtigung an und senden die Push-Benachrichtigung an Ihr eigenes Gerät.

1. In Journey Optimizer, im linken Navigationsbereich, im **[!UICONTROL JOURNEY-VERWALTUNG]** auswählen **Kampagnen**.

1. Klick **[!UICONTROL Kampagne erstellen]**.

   ![Kampagne erstellen](/help/summit/l820-lab-workbook/assets/2-3-1-1-create-campaign.png)

1. Auf der **[!UICONTROL Kampagne erstellen]** Seite, in der  **[!UICONTROL Aktion]** auswählen **[!UICONTROL Push-Benachrichtigung]** Kontrollkästchen.

1. Aus dem **[!UICONTROL Programmoberfläche]** Dropdown, auswählen *[!DNL Frecopa-Push]*.

1. Klick **[!UICONTROL Erstellen]** um eine Push-Kampagne zu erstellen.

   ![Programmoberfläche](/help/summit/l820-lab-workbook/assets/2-3-1-2-app-surface.png)

>[!SUCCESS]
>
>Sie sollten sich jetzt auf der Seite Kampagneneigenschaften befinden:
> ![Kampagneneigenschaften](/help/summit/l820-lab-workbook/assets/2-3-1-2-campaign-properties.png)

## Übung 4.2 - Konfigurieren der Kampagne

Auf dieser Seite konfigurieren Sie die Eigenschaften, die Audience, die Aktionen und den Zeitplan Ihrer Kampagne.

### 4.2.1 [!UICONTROL Abschnitt Eigenschaften]

Geben Sie Ihrer Kampagne einen Namen. Achten Sie darauf, den Namen mit Ihrer Sitznummer zu beginnen, damit Sie Ihre Kampagne bei der Suche leicht finden können.

Wenn Ihre Sitznummer beispielsweise 99 lautet: `99 - 10% Discount Campaign`.

### 4.2.2 **[!UICONTROL Zielgruppen-Abschnitt]**

1. Klicken Sie im Abschnitt Zielgruppe auf **[!UICONTROL Zielgruppe auswählen]**.

   ![Zielgruppen-Abschnitt](/help/summit/l820-lab-workbook/assets/2-3-2-5-audience-section.png)

1. Auf der **[!UICONTROL Zielgruppe auswählen]** auf dem Bildschirm nach der Audience suchen:

   **Labor - Sitz`your seat number`**

1. Wählen Sie die Audience aus und klicken Sie dann auf **[!UICONTROL Speichern]**.

   ![Zielgruppenauswahl](/help/summit/l820-lab-workbook/assets/2-3-2-7-select-audience.png)

### 4.2.3 Bearbeiten des Inhalts der Push-Benachrichtigung

In dieser Übung entwerfen und passen Sie die Push-Benachrichtigung an.

1. In der **[!UICONTROL Aktion]** klicken Sie auf das Symbol **[!UICONTROL Inhalt bearbeiten] Schaltfläche**.

   ![Schaltfläche Inhalt bearbeiten](/help/summit/l820-lab-workbook/assets/2-3-action-edit-content-button.png)

1. Wählen Sie im nächsten Bildschirm je nach vorhandenem Mobilgerät entweder die [!DNL iOS™] oder [!DNL Android™] Registerkarte zum Konfigurieren Ihres Inhalts.

>[!BEGINTABS]

>[!TAB iOS]

![Registerkarte iOS](/help/summit/l820-lab-workbook/assets/2-3-ios-tab.png)

>[!TAB Android]

![Registerkarte Android](/help/summit/l820-lab-workbook/assets/2-3-android-tab.png)

>[!ENDTABS]

#### 4.2.3.1 [!UICONTROL Nachricht erstellen] Sektion

1. **Verfassen Sie Ihre Nachricht:** Sie können gerne einen beliebigen Text hinzufügen. Im Folgenden finden Sie Beispiele, die Sie verwenden können:

   * Titel: `Get 10% off today!`
   * Textkörper: `Today only! Get 10% off on your House Blend coffee purchase!`

     ![Nachricht erstellen](/help/summit/l820-lab-workbook/assets/2-3-compose-message.png)

#### 4.2.3.2 Ändern Sie das Klickverhalten der Nachricht in **Öffnen einer Produktseite**

1. In der **[!UICONTROL Klickverhalten]** auswählen **[!UICONTROL Deeplink]** vom **[!UICONTROL Textkörper-Klickverhalten]** Dropdown.

1. Kopieren Sie die folgende URL und fügen Sie sie in den **URL-Feld**:

   `dxdemo://exoticVibes`

   ![Deep-Link](/help/summit/l820-lab-workbook/assets/2-3-deeplink.png)

#### 4.2.3.3 Hinzufügen eines Bildes zur Nachricht

1. In der **[!UICONTROL Medien hinzufügen]** klicken Sie auf **[!UICONTROL Medien hinzufügen]**.

   ![Medien-Schaltflächen hinzufügen](/help/summit/l820-lab-workbook/assets/2-3-3-3-add-media-buttons.png)

1. Auf der **[!UICONTROL Assets auswählen]** im linken Navigationsbereich öffnen Sie die Datei **Fréscopa-Ordner** und ein Bild aus diesem Ordner auswählen.

   Beispiel: `HouseBlend.png`

1. Klicken Sie auf das Bild und dann auf **[!UICONTROL Auswählen] Schaltfläche** , um das Bild zu Ihrer Push-Benachrichtigung hinzuzufügen.

   ![Bild auswählen](/help/summit/l820-lab-workbook/assets/2-3-3-3-select-image.png)

   >[!SUCCESS]
   >
   > 1. Klicken Sie im Bildschirm Vorschau auf **[!UICONTROL Ansicht erweitern]**.
   > 1. Vorschau der Nachricht
   > <br>
   >
   > ![Ansicht erweitern](/help/summit/l820-lab-workbook/assets/2-3-3-expand-view.png)

### Bonusübung

Wenn Sie diesen Teil der Übung abgeschlossen haben und noch etwas Zeit haben, versuchen Sie es mit der Bonusübung:

+++ Bonusübung

#### Personalisieren Sie die zu sendende Nachricht, indem Sie den Vornamen der Empfängerin bzw. des Empfängers hinzufügen.

1. Klick **Personalisierungsdialog** neben dem **[!UICONTROL Textkörper]** Feld.

   ![Schaltfläche „Personalisierung“](/help/summit/l820-lab-workbook/assets/2-3-personalization-button.png)

1. Auf der **Personalisierungsdialog** den Cursor an die Stelle setzen, an der der Vorname im Text eingefügt werden soll.

1. Stellen Sie sicher, dass die **Profilattribute** werden im linken Navigationsbereich ausgewählt.

   ![Profilattribut](/help/summit/l820-lab-workbook/assets/2-3-personalize-body-profile-attributes.png)

1. In der **Suchfeld**, suchen Sie nach: `first name`.

1. Klick **+** neben dem **Vorname (Profilattribute>Person>Vollständiger Name)** , um das Personalisierungsfeld zu Ihrem Text hinzuzufügen.

   ![Nach Vornamen suchen](/help/summit/l820-lab-workbook/assets/2-3-personalize-search-first-name.png)

   >[!SUCCESS]
   >
   > So sollte Ihr Text aussehen:
   > 
   >![Personalisierungs-Token](/help/summit/l820-lab-workbook/assets/2-3-personalization-token.png)

1. Klick **[!UICONTROL Speichern]** , um die Personalisierung zu speichern.


   >[!SUCCESS]
   >
   > 1. Klicken Sie im Bildschirm Vorschau auf **[!UICONTROL Ansicht erweitern]**.
   > 1. Vorschau der Nachricht
   > 
   > ![Ansicht erweitern](/help/summit/l820-lab-workbook/assets/2-3-3-expand-view.png)

+++

### 4.2.4. Überprüfung und Aktivierung

Wenn Sie mit dem Inhalt Ihrer Nachricht zufrieden sind, können Sie die Nachricht aktivieren:

1. Klick **[!UICONTROL Zum Aktivieren überprüfen]**.

   ![Schaltfläche „Überprüfen und aktivieren“](/help/summit/l820-lab-workbook/assets/2-3-4-review-and-activate-button.png)

1. Auf der **[!UICONTROL Zum Aktivieren überprüfen]** Bildschirm, klicken Sie auf **[!UICONTROL aktivieren]**.

   ![Zum Aktivieren überprüfen](/help/summit/l820-lab-workbook/assets/2-3-4-review-to-activate.png)

>[!SUCCESS]
> Auf der **Übersichtsseite zu Kampagnen**, suchen Sie Ihre Kampagne und überprüfen Sie den Status.
>
> ![Kampagnenstatus](/help/summit/l820-lab-workbook/assets/2-3-push-completed.png)
> 
> Der Status ändert sich von Verarbeitung in Live und dann in Abgeschlossen . Dies kann einige Minuten dauern.
> Sobald der Status in „Abgeschlossen“ geändert wurde:
>
> ![Push-Ergebnisse](/help/summit/l820-lab-workbook/assets/2-3-push-notification-result.png)

## Zusätzliche Ressourcen

**Anleitungsvideos:**

* [Konfigurieren und Senden von Push-Kampagnen](/help/channels/create-a-push-campaign.md)

**Produktdokumentation:**

* [Erste Schritte mit Push-Benachrichtigungen](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/push/get-started-push)
* [Erstellen einer Push-Benachrichtigung](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/push/create-push)
* [Gestalten einer Push-Benachrichtigung](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/push/design-push)
* [Push-Benachrichtigung überprüfen und senden](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/push/send-push)
