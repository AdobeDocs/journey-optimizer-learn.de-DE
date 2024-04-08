---
title: 'Lektion 2: Erstellen einer mobilen In-App-Kampagne'
description: Erstellen und Trigger einer mobilen In-App-Kampagne.
feature: In App
role: User
level: Intermediate
doc-type: Article
duration: 0
recommendations: noDisplay, noCatalog
jira: KT-14983
thumbnail: KT-14983.jpeg
exl-id: fe18eca7-229c-4867-ab34-1862bad63124
source-git-commit: 4f5c92f79eba3651b3633b7850e993160cb1f72c
workflow-type: tm+mt
source-wordcount: '1434'
ht-degree: 1%

---

# Lektion 2: Erstellen einer mobilen In-App-Kampagne

In dieser Lektion erstellen und Trigger von In-App-Nachrichten für Mobilgeräte.

## Lernziele

* Verstehen, wie In-App-Nachrichten ausgelöst werden.
* Wissen, wie man eine mobile In-App-Kampagne erstellt.
* Trigger einer In-App-Nachricht.

## Übung 2.1 - Bei Journey Optimizer anmelden

1. Öffnen Sie [Adobe Journey Optimizer](https://experience.adobe.com/#/@techmarketingdemos/sname:summit-ajo-lab/journey-optimizer/home){target="_blank"}
2. Melden Sie sich mit den folgenden Details an:
   <br>
   **Benutzername:** L820+**`<your seat number>`**@adobeeventlab.com
   **Kennwort:**   Adobe2024!
   <br>
Die Details für Ihre Anmeldung finden Sie auf Ihrem Lab-Computer-Desktop. Verwenden Sie die Adobe ID und das Kennwort.
   ![Arbeitsfläche](/help/summit/l820-lab-workbook/assets/desk-top.png)

   ![Anmeldebildschirm](/help/summit/l820-lab-workbook/assets/2-1-1-ajo-sign-in.png)
   <br>
3. Sie können die nächsten beiden Bildschirme überspringen:
   <br>
   ![Telefonnummer](/help/summit/l820-lab-workbook/assets/2-1-3-ajo-add-phone.png)
   <br>
   ![Popup für Personalisierung](/help/summit/l820-lab-workbook/assets/2-1-4-ajo-personalization-pop-up.png)


>[!SUCCESS]
>
>Sie sollten bei Journey Optimizer und auf der Homepage angemeldet sein:
>
>![AJO-Homepage](/help/summit/l820-lab-workbook/assets/2-1-5-ajo-homepage.png)


## Übung 2.2 Erstellen einer mobilen In-App-Kampagne

In dieser Übung erstellen Sie eine In-App-Nachrichtenkampagne, die ausgelöst wird, wenn Sie die App öffnen.

1. Wählen Sie in Journey Optimizer im linken Navigationsbereich Folgendes aus **[!UICONTROL Kampagnen]**.

1. Klick **[!UICONTROL Kampagne erstellen]**.

   ![Kampagne erstellen](/help/summit/l820-lab-workbook/assets/2-3-1-1-create-campaign.png)

1. Auf der **[!UICONTROL Kampagne erstellen]** Seite, in der  **[!UICONTROL Aktion]** auswählen **[!UICONTROL In-App-Nachricht]** Kontrollkästchen.

1. Aus dem **[!UICONTROL Senden an]** Dropdown, auswählen **[!DNL Mobile]**.

1. Aus dem **[!UICONTROL Programmoberfläche]** Dropdown, auswählen **[!DNL Frecopa Mobile App]**.

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

   ![Programmoberfläche](/help/summit/l820-lab-workbook/assets/3-1-1-1-create.png)

>[!SUCCESS]
>
>Sie sollten sich jetzt in den Kampagneneigenschaften befinden:
>
> ![Kampagneneigenschaften](/help/summit/l820-lab-workbook/assets/3-1-1-2-campaign-properties.png)

## Übung 2.3 Konfigurieren der Kampagne

### 2,3,1 [!UICONTROL Abschnitt Eigenschaften]

Geben Sie Ihrer Kampagne einen Namen. Achten Sie darauf, den Namen mit Ihrer Sitznummer zu beginnen, damit Sie Ihre Kampagne leicht wiederfinden können.

Wenn Ihre Sitznummer beispielsweise 99 lautet:  `99 - Welcome Campaign`.

![Abschnitt „Eigenschaften“](/help/summit/l820-lab-workbook/assets/3-1-2-1-properties-section.png)

### 2.3.2 Benutzerdefinierte Trigger-Regel einrichten

1. Scrollen Sie nach unten zum **[!UICONTROL Abschnitt &quot;Trigger&quot;]** und klicken Sie dann auf **[!UICONTROL Trigger bearbeiten]**.

   ![modifizieren](/help/summit/l820-lab-workbook/assets/3-2-1-2-edit-triggers.png)

1. Klicken Sie im Regel-Builder auf **[!UICONTROL Anwendungsstart]** und wählen Sie aus dem Dropdown-Menü aus  *Daten an Platform gesendet*.
   ![An Datenplattform senden](/help/summit/l820-lab-workbook/assets/trigger-drop-down-sent-to-platform.png)

1. Hinzufügen einer Bedingung durch Klicken auf **[!UICONTROL Bedingung hinzufügen]**.

   ![Schaltfläche „Bedingung hinzufügen“](/help/summit/l820-lab-workbook/assets/3-2-1-3-add-condition.png)

1. Aus dem **[!UICONTROL Eigenschaft auswählen]** Dropdown, auswählen **[!UICONTROL XDM-Ereignistyp]**.

   ![XDM-Ereignistyp](/help/summit/l820-lab-workbook/assets/4-1-2-dropdown-xdm-event.png)

1. Fügen Sie im folgenden Textfeld eine *`<custom string value>`* an die du dich erinnern kannst.

1. Um den Wert zu speichern, klicken Sie auf **[!UICONTROL Hinzufügen**] `<custom string value>`.

   Dieser benutzerdefinierte Zeichenfolgenwert wird später zum Auslösen Ihrer Nachricht verwendet.

   >[!TIP]
   > Wenn Sie Ihre Lizenznummer zum benutzerdefinierten Zeichenfolgenwert hinzufügen, ist dies eindeutig und fällt Ihnen leichter.
   > 
   > Beispiel: `99exerciseTrigger`

   ![Zeichenfolgenwert des benutzerdefinierten Triggers hinzufügen](/help/summit/l820-lab-workbook/assets/3-1-2-2-add-custom-trigger.png)

1. Klick **[!UICONTROL Fertig]** Oben rechts.

>[!SUCCESS]
>
>Sie haben nun Ihre In-App-Nachricht mit einem benutzerdefinierten Trigger-Ereignis definiert.
>
>![Kampagne mit benutzerdefiniertem Trigger](/help/summit/l820-lab-workbook/assets/3-1-2-2-campaign-with-custom-trigger.png)


### 2.3.3 Bearbeiten des Inhalts der In-App-Nachricht

In der **[!UICONTROL Aktion]** klicken Sie auf **[!UICONTROL Inhalt bearbeiten]**.

![Schaltfläche Inhalt bearbeiten](/help/summit/l820-lab-workbook/assets/3-1-3-1-edit-content-button.png)

Die [!UICONTROL In-App-Nachricht] Der Editor wird angezeigt, in dem Sie den Inhalt der In-App-Nachricht konfigurieren.

#### 2.3.3.1 Layout

Wählen Sie aus, welches Layout auf Ihre Nachricht angewendet werden soll.

Klicken Sie beispielsweise auf **[!UICONTROL Modal]** , um Ihre In-App-Nachricht in ein modales Layout umzuwandeln.

![Modal-Taste](/help/summit/l820-lab-workbook/assets/3-1-3-2-modal-button.png)

#### 2.3.3.2 Verfassen Ihrer Nachricht und Veröffentlichen Ihrer Kampagne

1. Fügen Sie im Abschnitt „Medien“ die folgende URL ein:  `https://t3.ftcdn.net/jpg/02/79/42/52/240_F_279425217_Hr9VBkknMr4fTpuZbxZXfcYdC7jSvGl2.jpg`
   <br>
Wenn Sie aus dem Wertefeld klicken, sollte Ihr Bild angezeigt werden.

   ![In der Vorschau angezeigte Medien](/help/summit/l820-lab-workbook/assets/3-1-3-2-media.png)

2. Im Folgenden **[!UICONTROL Inhalt]** Fügen Sie in Ihrem eigenen benutzerdefinierten Text hinzu, der in Ihrer Nachricht für den **[!UICONTROL Kopfzeile]** und **[!UICONTROL Textkörper]**.

   ![Kopfzeile und Hauptteil](/help/summit/l820-lab-workbook/assets/3-1-3-2-content.png)

3. Zusätzliche Optionen:
   1. **Schaltflächen:**

      ![Abschnitt „Schaltflächen“](/help/summit/l820-lab-workbook/assets/3-1-3-2-buttons.png)

      1. In diesem Abschnitt des Editors können Sie den Text für Ihre CTA-Schaltfläche anpassen, indem Sie das Textfeld Schaltfläche bearbeiten.

      2. Die **[!UICONTROL Interaktionsereignis]** wird verwendet, um den Wert zu definieren, der an das SDK übergeben wird, wenn der CTA vom Benutzer gedrückt wird.

      3. Die **[!UICONTROL Zielgruppe]** wird verwendet, um festzulegen, wohin der CTA den Benutzer bringen soll. Dazu gehören URLs und Deeplinks. Sie können beispielsweise diesen Deeplink zu einer Produktseite hinzufügen, z. B. `dxdemo://exoticVibes`.

      4. Sie können zusätzliche Schaltflächen hinzufügen, indem Sie drücken. **[!UICONTROL + Schaltfläche hinzufügen]**.

      5. Wenn Sie Ihrer Nachricht eine zweite Schaltfläche hinzufügen, haben Sie jetzt die Möglichkeit, das Schaltflächen-Layout mit dem Dropdown-Feld zu ändern.


   2. **Erweiterte Formatierung**

      ![Umschalter für erweiterte Formatierung](/help/summit/l820-lab-workbook/assets/3-1-3-2-advanced-formatting-toggle.png)

      Durch Aktivieren dieses Umschalters erhalten Sie zusätzliche Anpassungsoptionen im Editor.

      1. Mediengröße
      1. Schriftart
      1. Punkt-Größe
      1. Schriftfarbe
      1. Ausrichtung

      ![Erweiterte Formatierungsoptionen](/help/summit/l820-lab-workbook/assets/3-1-3-2-advanced-formatting-options.png)

   3. **Registerkarte „Einstellungen“**

      Durch Wechsel zu dieser Registerkarte und in der **[!UICONTROL Vorschau]** können Sie den **App-Vorschau**.
      <br>\
      ![Registerkarte „Einstellungen“](/help/summit/l820-lab-workbook/assets/3-1-3-1-settings-tab.png)
      <br>

      1. Die **[!UICONTROL Layout]** In diesem Abschnitt haben Sie die Möglichkeit, ein Bild als Hintergrund oder eine Volltonfarbe zu verwenden.

      2. Die **[!UICONTROL Nachricht]** bietet benutzerdefinierte Interaktionen, die für Ihre Nachricht aktiviert werden können:
         1. Benutzerdefinierte Gesten
         2. UI-Übernahme
         3. Übernahme durch die benutzerdefinierte Benutzeroberfläche
         4. Benutzerdefinierte Größe
         5. Benutzerdefinierte Position
         6. Benutzerdefinierte Animation
         7. Nachricht mit abgerundeter Ecke
   <br>
4. Wenn Sie mit dem Verfassen Ihres Inhalts fertig sind und mit Ihrer Nachricht zufrieden sind, klicken Sie auf das Symbol **[!UICONTROL Zum Aktivieren überprüfen] Schaltfläche**.

   >[!SUCCESS]
   >
   > Sie haben jetzt das Verfassen Ihrer In-App-Nachricht für Mobilgeräte abgeschlossen. Sie sollten sich jetzt in der Kampagne befinden **[!UICONTROL Zum Aktivieren überprüfen]** Seite.
   >
   >![Überprüfen und aktivieren](/help/summit/l820-lab-workbook/assets/3-1-4-1-review-and-activate.png)
   >
   > Hier können Sie eine vollständige Zusammenfassung Ihrer Nachricht sehen.
   >
   > *Beachten Sie den benutzerdefinierten Wert, den Sie als Trigger-Regel verwendet haben. Dieser Wert wird zum Auslösen Ihrer In-App-Nachricht verwendet. Der verwendete Wert finden Sie unter im Hervorhebungsbereich der Zusammenfassungsseite.*

   >[!NOTE]
   >Der aktuelle Trigger für die In-App-Nachricht ist der Standard **Anwendungsstartereignis**, was bedeutet, dass die In-App-Nachricht beim Start der App ausgelöst wird. Sie können dies in der **[!UICONTROL Zeitplanabschnitt]**.

5. Wenn Sie mit der Überprüfung Ihrer Kampagne fertig sind, klicken Sie auf die Schaltfläche Aktivieren , um die Kampagne zu veröffentlichen.
   <br>
   ![aktivieren](/help/summit/l820-lab-workbook/assets/3-1-4-2-activate.png)


>[!SUCCESS]
>
> Jetzt sollte das Kampagnen-Dashboard angezeigt werden. Suchen Sie Ihre Kampagne, indem Sie scrollen oder die Suchfunktion verwenden. Wenn sich der Status Ihrer Kampagne in ändert **[!UICONTROL LIVE]** (~1min), Ihre Kampagne wurde jetzt veröffentlicht.
>
> ![Veröffentlichte Kampagne](/help/summit/l820-lab-workbook/assets/3-1-3-2-published-campaign.png)
>


## Übung 2.4 Trigger der In-App-Nachricht für Mobilgeräte

So aktualisieren Sie die Payload und laden Sie Ihre neu veröffentlichte Kampagne herunter:

1. Schließen Sie die Fréscopa-App auf Ihrem Mobilgerät vollständig.
2. Öffnen Sie die Fréscopa-App erneut.
3. Navigieren Sie nun in der App zur Registerkarte Übungen .

   ![Übungsknopf](/help/summit/l820-lab-workbook/assets/3-2-3-app-exercise-button.png)

4. Geben Sie in das Textfeld den Wert für den benutzerdefinierten Trigger ein, den Sie in Campaign definiert haben. Klicken Sie dann auf Senden.


   ![modifizieren](/help/summit/l820-lab-workbook/assets/3-2-2-1-app-condition.PNG){width="250" align="center" zoomable="yes"}

>[!SUCCESS]
>
>Wenn Sie auf „Senden“ klicken, haben Sie manuell einen Trigger ausgelöst und die von Ihnen erstellte In-App-Benachrichtigung erscheint:
>
>![In-App-Nachricht](/help/summit/l820-lab-workbook/assets/3-1-3-3-in-app-message.png)
>
> *Wenn Sie Probleme haben, Ihre Nachricht auszulösen, überprüfen Sie Folgendes:*
> 
> * *Stellen Sie sicher, dass Sie im Feld Ereignisname in Ihrer Mobile App den Wert Ihrer Kampagnenregel genau so eingeben, wie Sie ihn in der Trigger-Regel hatten.*
> * *Achten Sie darauf, dass die Groß- und Kleinschreibung korrekt ist und dass Sie keine Leerzeichen am Anfang oder Ende haben.*
> * *Trigger Sie können den Wert Ihrer Kampagnenregel nachschlagen, den Sie verwendet haben, wenn Sie zur Kampagnenüberprüfungsseite zurückkehren. Klicken Sie dazu im Kampagnen-Dashboard auf „Zurück„.*

Sie haben soeben Ihre erste Journey Optimizer In-App-Nachricht verfasst und veröffentlicht!


## Bonusübung: Duplizieren Sie die Kampagne und die Vorschau auf dem Gerät

Die **Kampagne duplizieren** und **Vorschau auf Gerät** -Funktionen sind vorkonfigurierte Funktionen, mit denen Sie Ihre Kampagnen duplizieren und Ihre In-App-Nachrichten direkt auf Ihrem Gerät testen und überprüfen können, bevor Sie sie aktivieren. In dieser Übung erfahren Sie, wie Sie diese Funktion verwenden und eine Vorschau der in Übung 3.1 erstellten Nachricht anzeigen.

1. Öffnen Sie die soeben erstellte Kampagne, indem Sie auf den Namen der Kampagne auf der Seite des Kampagnen-Dashboards klicken, um die Kampagne zu öffnen. Dadurch gelangen Sie zurück zum **[!UICONTROL Kampagne überprüfen]** Seite.
1. Drücken Sie die **[!UICONTROL Schaltfläche duplizieren]**. Dadurch wird eine neue Eingabeaufforderung mit dem Namen der neuen Kampagne geöffnet, die dupliziert wird. Fügen Sie einen neuen Namen hinzu, den Sie sich leicht merken können, oder verwenden Sie den Standardnamen, wobei **[!DNL _copy]** wird standardmäßig hinzugefügt.

   ![Kampagne duplizieren](/help/summit/l820-lab-workbook/assets/3-2-duplicate-campaign.png)

1. Sobald Sie auf die Schaltfläche Duplizieren klicken, wird Ihre doppelte Kampagne erstellt und Sie gelangen zurück zum Kampagnen-Dashboard.
1. Nachdem Ihre Kampagne dupliziert wurde, öffnen Sie Ihre neue Kampagne.

1. Sie können auf die Funktion Vorschau auf Gerät in der **[!UICONTROL Kampagnenüberprüfung]** oder auf der Seite **[!UICONTROL Kampagnenautor]** Schritt.

   ![Schaltfläche „Vorschau auf Gerät“](/help/summit/l820-lab-workbook/assets/3-3-1-1-preview-on-device-button.png)
   <br>

1. Klicken Sie anschließend auf die Schaltfläche **[!UICONTROL Schaltfläche „Start“]** Vom Bildschirm Mit Gerät verbinden .

   ![Schaltfläche „Start“](/help/summit/l820-lab-workbook/assets/3-3-1-2-connect-to-device-start.png)
   <br>

1. Geben Sie die Basis-URL ein, die für den Start der Fréscopa-App konfiguriert wurde: `dxdemo://`

   ![Vorschau-URL](/help/summit/l820-lab-workbook/assets/3-3-1-3-preview-url.png)

   <br>

1. Befolgen Sie die Anweisungen auf dem Bildschirm:
   1. Scannen Sie den QR-Code mit Ihrem Mobilgerät, und die Fréscopa-App öffnet sich mit einem Bildschirm, auf dem Sie eine angezeigte PIN eingeben können.
   2. Geben Sie auf Ihrem Gerät die in AJO auf dem Bildschirm Assurance angezeigte Pin ein und klicken Sie auf die Schaltfläche Verbinden, die unten rechts angezeigt wird, sobald Sie die Pin eingegeben haben.


   ![Pin eingeben](/help/summit/l820-lab-workbook/assets/3-3-1-5-enter-pin.PNG){width="250" align="center" zoomable="yes"}
   <br>
1. Dieses Popup erscheint auf dem Bildschirm Ihres Computers

   ![Popup](/help/summit/l820-lab-workbook/assets/3-3-pop-up.png)

1. Klicken Sie auf die Schaltfläche Fertig . Dadurch wird das Dialogfeld geschlossen und Ihr Telefon ist jetzt mit der Vorschau auf dem Gerät verbunden.


>[!SUCCESS]
>
> Ihre In-App-Nachricht wird auf Ihrem Gerät angezeigt.
>
> *Sobald die Verbindung hergestellt ist, sollte Ihre In-App-Nachricht jedes Mal angezeigt werden, wenn Sie auf die Schaltfläche **[!UICONTROL Vorschau auf Gerät] Schaltfläche**.

## Zusätzliche Ressourcen

**Anleitungsvideos:**

* [Erstellen einer In-App-Kampagne](/help/channels/create-an-in-app-campaign.md)
* [Verfassen einer In-App-Nachricht ](/help/channels/author-in-app-messages.md)

**Produktdokumentation:**

* [Erste Schritte mit dem In-App-Kanal](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/in-app/get-started-in-app)
* [Erstellen einer In-App-Nachricht für Mobilgeräte](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/in-app/create-in-app)
* [Gestalten Ihrer In-App-Inhalte](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/in-app/design-in-app)
* [Überprüfen und Senden Ihrer In-App-Benachrichtigung](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/in-app/send-in-app)
