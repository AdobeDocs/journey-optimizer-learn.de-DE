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
source-git-commit: 55ba1a46c1473d94847e7fccc69ed2a33badb54c
workflow-type: tm+mt
source-wordcount: '1432'
ht-degree: 1%

---

# Lektion 2: Erstellen einer mobilen In-App-Kampagne

In dieser Lektion erstellen und Trigger von In-App-Nachrichten für Mobilgeräte.

## Lernziele

* Verstehen, wie In-App-Nachrichten ausgelöst werden.
* Wissen, wie Sie eine mobile In-App-Kampagne erstellen.
* Trigger einer In-App-Nachricht.

## Übung 2.1 - Bei Journey Optimizer anmelden

1. [Adobe Journey Optimizer öffnen](https://experience.adobe.com/#/@techmarketingdemos/sname:summit-ajo-lab/journey-optimizer/home){target="_blank"}
2. Melden Sie sich mit den folgenden Details an:
   <br>
   **Benutzername:** L820+**`<your seat number>`**@adobeeventlab.com
   **Kennwort:**   Adobe2024!
   <br>
Die Details für Ihre Anmeldung finden Sie auf Ihrem Lab-Computer-Desktop. Verwenden Sie die Adobe ID und das Kennwort.
   ![Desktop](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/desk-top.png)

   ![Anmeldebildschirm](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-1-1-ajo-sign-in.png)
   <br>
3. Sie können die nächsten beiden Bildschirme überspringen:
   <br>
   ![Telefonnummer](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-1-3-ajo-add-phone.png)
   <br>
   ![Personalization-Popup](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-1-4-ajo-personalization-pop-up.png)


>[!SUCCESS]
>
>Sie sollten bei Journey Optimizer und auf der Homepage angemeldet sein:
>
>![AJO-Homepage](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-1-5-ajo-homepage.png)


## Übung 2.2 Erstellen einer mobilen In-App-Kampagne

In dieser Übung erstellen Sie eine In-App-Nachrichtenkampagne, die ausgelöst wird, wenn Sie die App öffnen.

1. Wählen Sie in Journey Optimizer im linken Navigationsbereich die Option **[!UICONTROL Kampagnen]**.

1. Klicken Sie **[!UICONTROL Kampagne erstellen]**.

   ![Kampagne erstellen](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-1-1-create-campaign.png)

1. Aktivieren Sie auf **[!UICONTROL Seite]** Kampagne erstellen“ im Abschnitt **[!UICONTROL Aktion]** das Kontrollkästchen **[!UICONTROL In-App-]**.

1. Wählen Sie im **[!UICONTROL Senden an]** die Option **[!DNL Mobile]** aus.

1. Wählen Sie im Dropdown **[!UICONTROL Menü]** Programmoberfläche“ die Option **[!DNL Frecopa Mobile App]** aus.

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

   ![Programmoberfläche](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-1-1-1-create.png)

>[!SUCCESS]
>
>Sie sollten sich jetzt in den Kampagneneigenschaften befinden:
>
> ![Kampagneneigenschaften](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-1-1-2-campaign-properties.png)

## Übung 2.3 Kampagne konfigurieren

### 2.3.1 [!UICONTROL Abschnitt Eigenschaften]

Geben Sie Ihrer Kampagne einen Namen. Achten Sie darauf, den Namen mit Ihrer Sitznummer zu beginnen, damit Sie Ihre Kampagne einfach wieder finden können.

Wenn Ihre Sitznummer beispielsweise 99: `99 - Welcome Campaign` lautet.

![Eigenschaftenabschnitt](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-1-2-1-properties-section.png)

### 2.3.2 Benutzerdefinierte Trigger-Regel einrichten

1. Scrollen Sie nach unten zum Abschnitt **[!UICONTROL Trigger]** klicken Sie dann auf **[!UICONTROL Trigger bearbeiten]**.

   ![Ändern](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-2-1-2-edit-triggers.png)

1. Klicken Sie im Regel-Builder auf **[!UICONTROL Anwendungsstart]** und wählen Sie aus der Dropdown-Liste *Daten an Platform gesendet*.
   ![An Datenplattform gesendet](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/trigger-drop-down-sent-to-platform.png)

1. Fügen Sie eine Bedingung hinzu, indem Sie **[!UICONTROL Bedingung hinzufügen]** klicken.

   ![Schaltfläche „Bedingung hinzufügen“](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-2-1-3-add-condition.png)

1. Wählen Sie in der **[!UICONTROL Eigenschaft auswählen]** die Option **[!UICONTROL XDM-Ereignistyp]** aus.

   ![XDM-Ereignistyp](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/4-1-2-dropdown-xdm-event.png)

1. Fügen Sie im folgenden Textfeld einen *`<custom string value>`* hinzu, an den Sie sich erinnern können.

1. Um den Wert zu speichern, klicken Sie auf **[!UICONTROL Hinzufügen**] `<custom string value>`.

   Dieser benutzerdefinierte Zeichenfolgenwert wird später zum Auslösen Ihrer Nachricht verwendet.

   >[!TIP]
   > Wenn Sie Ihre Lizenznummer zum benutzerdefinierten Zeichenfolgenwert hinzufügen, ist dies eindeutig und fällt Ihnen leichter.
   > 
   > Beispiel: `99exerciseTrigger`

   ![Benutzerdefinierten Trigger-Zeichenfolgenwert hinzufügen](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-1-2-2-add-custom-trigger.png)

1. Klicken **[!UICONTROL oben]** auf „Fertig“.

>[!SUCCESS]
>
>Sie haben nun Ihre In-App-Nachricht mit einem benutzerdefinierten Trigger-Ereignis definiert.
>
>![Kampagne mit benutzerdefiniertem Trigger definiert](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-1-2-2-campaign-with-custom-trigger.png)


### 2.3.3 Bearbeiten des Inhalts der In-App-Nachricht

Klicken Sie **[!UICONTROL Abschnitt]** Aktion“ auf **[!UICONTROL Inhalt bearbeiten]**.

![Schaltfläche „Inhalt bearbeiten“](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-1-3-1-edit-content-button.png)

Der [!UICONTROL In-App]Nachrichteneditor wird angezeigt, in dem Sie den Inhalt der In-App-Nachricht konfigurieren.

#### 2.3.3.1

Auswählen, welches Layout auf Ihre Nachricht angewendet werden soll.

Klicken Sie beispielsweise auf **[!UICONTROL Modal]**, damit Ihre In-App-Nachricht ein modales Layout erhält.

![modale Schaltfläche](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-1-3-2-modal-button.png)

#### 2.3.3.2 Verfassen Ihrer Nachricht und Veröffentlichen Ihrer Kampagne

1. Fügen Sie im Abschnitt „Medien“ die folgende URL ein: `https://t3.ftcdn.net/jpg/02/79/42/52/240_F_279425217_Hr9VBkknMr4fTpuZbxZXfcYdC7jSvGl2.jpg`
   <br>
Wenn Sie aus dem Wertefeld klicken, sollte Ihr Bild angezeigt werden.

   ![In der Vorschau angezeigte Medien](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-1-3-2-media.png)

2. Fügen Sie im folgenden **[!UICONTROL Inhalt]**-Abschnitt Ihren eigenen benutzerdefinierten Text hinzu, den Sie in Ihrer Nachricht für die **[!UICONTROL Kopfzeile]** und (**[!UICONTROL )]** möchten.

   ![Kopfzeile und Hauptteil](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-1-3-2-content.png)

3. Zusätzliche Optionen:
   1. **Schaltflächen:**

      ![Abschnitt Schaltflächen](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-1-3-2-buttons.png)

      1. In diesem Abschnitt des Editors können Sie den Text für Ihre CTA-Schaltfläche anpassen, indem Sie das Textfeld Schaltfläche bearbeiten.

      2. Das Feld **[!UICONTROL Interaktionsereignis]** wird verwendet, um den Wert zu definieren, der an den SDK übergeben wird, wenn der Benutzer auf die CTA klickt.

      3. Im Feld **[!UICONTROL Target]** wird definiert, wohin die Benutzerin bzw. der Benutzer von CTA gebracht werden soll. Dazu gehören URLs und Deeplinks. Sie können beispielsweise diesen Deeplink zu einer Produktseite wie `dxdemo://exoticVibes` hinzufügen.

      4. Sie können zusätzliche Schaltflächen hinzufügen, indem Sie auf die Schaltfläche **[!UICONTROL + Hinzufügen]**.

      5. Wenn Sie Ihrer Nachricht eine zweite Schaltfläche hinzufügen, können Sie jetzt das Schaltflächen-Layout mit der Dropdown-Liste ändern.


   2. **Erweiterte Formatierung**

      ![Umschalter für erweiterte Formatierung](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-1-3-2-advanced-formatting-toggle.png)

      Durch Aktivieren dieses Umschalters erhalten Sie zusätzliche Anpassungsoptionen im Editor.

      1. Mediengröße
      1. Schriftart
      1. Punkt-Größe
      1. Schriftfarbe
      1. Ausrichtung

      ![Erweiterte Formatierungsoptionen](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-1-3-2-advanced-formatting-options.png)

   3. **Registerkarte „Einstellungen**

      Durch Wechsel zu dieser Registerkarte und im Abschnitt **[!UICONTROL Vorschau]** können Sie die &quot;**-Vorschau“**.
      <br>\
      ![Registerkarte „Einstellungen](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-1-3-1-settings-tab.png)
      <br>

      1. Im **[!UICONTROL Layout]** haben Sie die Möglichkeit, ein Bild als Hintergrund oder eine Volltonfarbe zu verwenden.

      2. Der Abschnitt **[!UICONTROL Nachricht]** enthält benutzerdefinierte Interaktionen, die für Ihre Nachricht aktiviert werden können:
         1. Benutzerdefinierte Gesten
         2. UI-Übernahme
         3. Benutzerdefinierte UI-Übernahme
         4. Benutzerdefinierte Größe
         5. Benutzerdefinierte Position
         6. Benutzerdefinierte Animation
         7. Nachricht mit abgerundeter Ecke
   <br>
4. Wenn Sie mit dem Verfassen Ihres Inhalts fertig sind und mit Ihrer Nachricht zufrieden sind, klicken Sie auf die Schaltfläche **[!UICONTROL Zum Aktivieren überprüfen]**.

   >[!SUCCESS]
   >
   > Sie haben jetzt das Verfassen Ihrer In-App-Nachricht für Mobilgeräte abgeschlossen. Sie sollten sich jetzt auf der Seite **[!UICONTROL Zur Aktivierung überprüfen]** befinden.
   >
   >![Überprüfen und aktivieren](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-1-4-1-review-and-activate.png)
   >
   > Hier können Sie eine vollständige Zusammenfassung Ihrer Nachricht sehen.
   >
   > *Beachten Sie den benutzerdefinierten Wert, den Sie als Trigger-Regel verwendet haben. Dieser Wert wird zum Auslösen Ihrer In-App-Nachricht verwendet. Der verwendete Wert ist unter im Hervorhebungsbereich der Zusammenfassungsseite zu finden.*

   >[!NOTE]
   >Der aktuelle Trigger für die In-App-Nachricht ist der Standardwert **Anwendungsstartereignis tritt auf** was bedeutet, dass die In-App-Nachricht beim Start der App ausgelöst wird. Sie können dies im Abschnitt &quot;**[!UICONTROL &quot;]**.

5. Wenn Sie mit der Überprüfung Ihrer Kampagne fertig sind, klicken Sie auf die Schaltfläche Aktivieren , um die Kampagne zu veröffentlichen.
   <br>
   ![aktivieren](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-1-4-2-activate.png)


>[!SUCCESS]
>
> Jetzt sollte das Kampagnen-Dashboard angezeigt werden. Suchen Sie Ihre Kampagne, indem Sie scrollen oder die Suchfunktion verwenden. Wenn Ihre Kampagne den Status in **[!UICONTROL Live]** (~1 Min.) ändert, ist Ihre Kampagne jetzt veröffentlicht.
>
> ![Veröffentlichte Kampagne](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-1-3-2-published-campaign.png)
>


## Übung 2.4 - Trigger der mobilen In-App-Nachricht

So aktualisieren Sie die Payload und laden Ihre neu veröffentlichte Kampagne herunter:

1. Schließen Sie die Fréscopa-App auf Ihrem Mobilgerät vollständig.
2. Öffnen Sie die Fréscopa-App erneut.
3. Navigieren Sie nun in der App zur Registerkarte Übungen .

   ![Übungsknopf](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-2-3-app-exercise-button.png)

4. Geben Sie in das Textfeld den Wert für den benutzerdefinierten Trigger ein, den Sie in Campaign definiert haben. Klicken Sie dann auf Senden.


   ![Ändern](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-2-2-1-app-condition.PNG){width="250" align="center" zoomable="yes"}

>[!SUCCESS]
>
>Wenn Sie auf „Senden“ klicken, haben Sie manuell einen Trigger ausgelöst und die von Ihnen erstellte In-App-Benachrichtigung erscheint:
>
>![In-App-Nachricht](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-1-3-3-in-app-message.png)
>
> *Wenn beim Auslösen Ihrer Nachricht Probleme auftreten, überprüfen Sie Folgendes:*
> 
> * *Stellen Sie im Feld Ereignisname in Ihrer Mobile App sicher, dass Sie den Wert Ihrer Kampagnenregel genau so eingegeben haben, wie Sie ihn in der Trigger-App hatten.*
> * *Achten Sie darauf, dass die Groß- und Kleinschreibung korrekt ist und dass Sie keine Leerzeichen am Anfang oder Ende haben.*
> * *Sie können den Wert Ihrer Kampagnenregel nachschlagen, den Sie verwendet haben, wenn Sie zur Kampagnenüberprüfungsseite zurückkehren, indem Sie im Kampagnen-Dashboard auf „Zurück“ in Ihre Trigger-Regel klicken.*

Sie haben soeben Ihre erste In-App-Nachricht für Journey Optimizer verfasst und veröffentlicht!


## Bonusübung: Kampagne und Vorschau auf Gerät duplizieren

Die Funktionen **Kampagne duplizieren** und **Vorschau auf Gerät** sind vorkonfigurierte Funktionen, mit denen Sie Ihre Kampagnen duplizieren und Ihre In-App-Nachrichten direkt auf Ihrem Gerät testen und überprüfen können, bevor Sie sie aktivieren. In dieser Übung erfahren Sie, wie Sie diese Funktion verwenden und eine Vorschau der in Übung 3.1 erstellten Nachricht anzeigen.

1. Öffnen Sie die soeben erstellte Kampagne, indem Sie auf den Namen der Kampagne auf der Seite Kampagnen-Dashboard klicken, um die Kampagne zu öffnen. Dadurch gelangen Sie zurück zur Seite **[!UICONTROL Kampagne überprüfen]**.
1. Drücken Sie die **[!UICONTROL Duplizieren]**. Dadurch wird eine neue Eingabeaufforderung mit dem Namen der neuen Kampagne geöffnet, die dupliziert wird. Fügen Sie einen neuen Namen hinzu, den Sie sich leicht merken können, oder verwenden Sie den Standardnamen, bei dem **[!DNL _copy]** standardmäßig hinzugefügt wird.

   ![Kampagne duplizieren](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-2-duplicate-campaign.png)

1. Sobald Sie auf die Schaltfläche Duplizieren klicken, wird Ihre doppelte Kampagne erstellt und Sie gelangen zurück zum Kampagnen-Dashboard.
1. Nachdem Ihre Kampagne dupliziert wurde, öffnen Sie Ihre neue Kampagne.

1. Sie können auf die Funktion Vorschau auf Gerät auf der Seite **[!UICONTROL Kampagnenüberprüfung]** oder im Schritt **[!UICONTROL Kampagnenautor]** zugreifen.

   ![Schaltfläche „Vorschau auf Gerät“](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-3-1-1-preview-on-device-button.png)
   <br>

1. Klicken Sie als Nächstes auf **[!UICONTROL Start]** im Bildschirm Mit Gerät verbinden .

   ![Start-Schaltfläche](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-3-1-2-connect-to-device-start.png)
   <br>

1. Geben Sie die Basis-URL ein, die für den Start der Fréscopa-App konfiguriert wurde: `dxdemo://`

   ![Vorschau-URL](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-3-1-3-preview-url.png)

   <br>

1. Befolgen Sie die Anweisungen auf dem Bildschirm:
   1. Scannen Sie den QR-Code mit Ihrem Mobilgerät, und die Fréscopa-App wird mit einem Bildschirm geöffnet, auf dem Sie eine angezeigte PIN eingeben können.
   2. Geben Sie auf Ihrem Gerät die in AJO auf dem Assurance-Bildschirm angezeigte Pin ein und klicken Sie auf die Schaltfläche Verbinden, die unten rechts angezeigt wird, nachdem Sie die Pin eingegeben haben.


   ![PIN eingeben](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-3-1-5-enter-pin.PNG){width="250" align="center" zoomable="yes"}
   <br>
1. Dieses Popup erscheint auf Ihrem Computerbildschirm

   ![Popup](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-3-pop-up.png)

1. Klicken Sie auf die Schaltfläche Fertig . Dadurch wird das Dialogfeld geschlossen und Ihr Telefon ist jetzt mit der Vorschau auf dem Gerät verbunden.


>[!SUCCESS]
>
> Ihre In-App-Nachricht wird auf Ihrem Gerät angezeigt.
>
> *Nach der Verbindung sollte Ihre In-App-Nachricht jedes Mal angezeigt werden, wenn Sie auf die Schaltfläche **[!UICONTROL Vorschau auf Gerät] klicken**.

## Weitere Ressourcen

**Anleitungsvideos:**

* [Erstellen einer In-App-Kampagne](/help/channels/create-an-in-app-campaign.md)
* [Verfassen einer In-App-Nachricht &#x200B;](/help/channels/author-in-app-messages.md)

**Produktdokumentation:**

* [Erste Schritte mit dem In-App-Kanal](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/in-app/get-started-in-app)
* [Erstellen einer mobilen In-App-Nachricht](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/in-app/create-in-app)
* [Gestalten Ihrer In-App-Inhalte](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/in-app/design-in-app)
* [Überprüfen und Senden Ihrer In-App-Benachrichtigung](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/in-app/send-in-app)
