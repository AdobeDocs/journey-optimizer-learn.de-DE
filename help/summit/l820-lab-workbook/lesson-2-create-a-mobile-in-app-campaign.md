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

In dieser Lektion erstellen und Trigger für mobile In-App-Nachrichten.

## Lernziele

* Erfahren Sie, wie In-App-Nachrichten ausgelöst werden.
* Erfahren Sie, wie Sie eine mobile In-App-Kampagne erstellen.
* Trigger einer In-App-Nachricht.

## Übung 2.1 - Anmeldung bei Journey Optimizer

1. Öffnen Sie [Adobe Journey Optimizer](https://experience.adobe.com/#/@techmarketingdemos/sname:summit-ajo-lab/journey-optimizer/home){target="_blank"}
2. Melden Sie sich mit den folgenden Details an:
   <br>
   **Benutzername:** L820+**`<your seat number>`**@adobeeventlab.com
   **Kennwort:**   Adobe2024!
   <br>
Die Details für Ihre Anmeldung finden Sie auf Ihrem Desktop. Verwenden Sie die Adobe ID und das Kennwort.
   ![Desktop](/help/summit/l820-lab-workbook/assets/desk-top.png)

   ![Anmeldebildschirm](/help/summit/l820-lab-workbook/assets/2-1-1-ajo-sign-in.png)
   <br>
3. Sie können die nächsten beiden Bildschirme überspringen:
   <br>
   ![Telefonnummer](/help/summit/l820-lab-workbook/assets/2-1-3-ajo-add-phone.png)
   <br>
   ![Personalization pop-up](/help/summit/l820-lab-workbook/assets/2-1-4-ajo-personalization-pop-up.png)


>[!SUCCESS]
>
>Sie sollten bei Journey Optimizer und auf der Startseite angemeldet sein:
>
>![AJO-Homepage](/help/summit/l820-lab-workbook/assets/2-1-5-ajo-homepage.png)


## Übung 2.2 Eine mobile In-App-Kampagne erstellen

In dieser Übung erstellen Sie eine In-App-Nachrichtenkampagne, die ausgelöst wird, wenn Sie die App öffnen.

1. Wählen Sie in Journey Optimizer im linken Navigationsbereich **[!UICONTROL Kampagnen]** aus.

1. Klicken Sie auf **[!UICONTROL Kampagne erstellen]**.

   ![Kampagne erstellen](/help/summit/l820-lab-workbook/assets/2-3-1-1-create-campaign.png)

1. Aktivieren Sie auf der Seite **[!UICONTROL Kampagne erstellen]** im Abschnitt **[!UICONTROL Aktion]** das Kontrollkästchen **[!UICONTROL In-App-Nachricht]** .

1. Wählen Sie aus dem Dropdown-Menü **[!UICONTROL An]** senden die Option **[!DNL Mobile]** aus.

1. Wählen Sie aus dem Dropdown-Menü **[!UICONTROL App-Oberfläche]** die Option **[!DNL Frecopa Mobile App]** aus.

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

   ![App-Oberfläche](/help/summit/l820-lab-workbook/assets/3-1-1-1-create.png)

>[!SUCCESS]
>
>Sie sollten nun die Campaign-Eigenschaften verwenden:
>
> ![Kampagneneigenschaften](/help/summit/l820-lab-workbook/assets/3-1-1-2-campaign-properties.png)

## Übung 2.3 Konfigurieren der Kampagne

### 2.3.1 [!UICONTROL Eigenschaftenabschnitt]

Geben Sie Ihrer Kampagne einen Namen. Beginnen Sie den Namen mit Ihrer Sitznummer, damit Sie Ihre Kampagne einfach wiederfinden können.

Beispiel: Ihre Sitznummer ist 99: `99 - Welcome Campaign`.

![Eigenschaftenabschnitt](/help/summit/l820-lab-workbook/assets/3-1-2-1-properties-section.png)

### 2.3.2 Benutzerdefinierte Trigger-Regel einrichten

1. Scrollen Sie nach unten zum Abschnitt **[!UICONTROL Trigger]** und klicken Sie dann auf **[!UICONTROL Trigger bearbeiten]**.

   ![modify](/help/summit/l820-lab-workbook/assets/3-2-1-2-edit-triggers.png)

1. Klicken Sie im Regel-Builder auf **[!UICONTROL Application Launch]** und wählen Sie aus dem Dropdown-Menü *Daten an Platform senden* aus.
   ![An Datenplattform gesendet](/help/summit/l820-lab-workbook/assets/trigger-drop-down-sent-to-platform.png)

1. Fügen Sie eine Bedingung hinzu, indem Sie auf **[!UICONTROL Bedingung hinzufügen]** klicken.

   ![Schaltfläche &quot;Bedingung hinzufügen&quot;](/help/summit/l820-lab-workbook/assets/3-2-1-3-add-condition.png)

1. Wählen Sie aus der Dropdownliste **[!UICONTROL Eigenschaft auswählen]** die Option **[!UICONTROL XDM-Ereignistyp]** aus.

   ![XDM-Ereignistyp](/help/summit/l820-lab-workbook/assets/4-1-2-dropdown-xdm-event.png)

1. Fügen Sie im folgenden Textfeld eine *`<custom string value>`* hinzu, die Sie sich merken können.

1. Um den Wert zu speichern, klicken Sie auf **[!UICONTROL Hinzufügen**] `<custom string value>`.

   Dieser benutzerdefinierte Zeichenfolgenwert wird später verwendet, um Ihre Nachricht auszulösen.

   >[!TIP]
   > Wenn Sie Ihre Sitznummer zum benutzerdefinierten Zeichenfolgenwert hinzufügen, ist es für Sie einzigartig und einfacher, sich daran zu erinnern.
   > 
   > Beispiel: `99exerciseTrigger`

   ![benutzerdefinierten Trigger-Zeichenfolgenwert hinzufügen](/help/summit/l820-lab-workbook/assets/3-1-2-2-add-custom-trigger.png)

1. Klicken Sie oben rechts auf **[!UICONTROL Fertig]** .

>[!SUCCESS]
>
>Sie haben Ihre In-App-Nachricht jetzt mit einem benutzerdefinierten Trigger-Ereignis definiert.
>
>![Kampagne mit definiertem Trigger](/help/summit/l820-lab-workbook/assets/3-1-2-2-campaign-with-custom-trigger.png)


### 2.3.3 Inhalt der In-App-Nachricht bearbeiten

Klicken Sie im Abschnitt **[!UICONTROL Aktion]** auf **[!UICONTROL Inhalt bearbeiten]**.

![Schaltfläche &quot;Inhalt bearbeiten&quot;](/help/summit/l820-lab-workbook/assets/3-1-3-1-edit-content-button.png)

Der Editor [!UICONTROL In-App-Nachricht] wird angezeigt, in dem Sie den Inhalt der In-App-Nachricht konfigurieren.

#### 2.3.3.1 Layout

Wählen Sie aus, welches Layout auf Ihre Nachricht angewendet werden soll.

Klicken Sie beispielsweise auf **[!UICONTROL Modal]** , um Ihre In-App-Nachricht in ein modales Layout umzuwandeln.

![modale Schaltfläche](/help/summit/l820-lab-workbook/assets/3-1-3-2-modal-button.png)

#### 2.3.3.2 Nachrichten verfassen und Kampagnen veröffentlichen

1. Fügen Sie im Medienabschnitt die folgende URL ein: `https://t3.ftcdn.net/jpg/02/79/42/52/240_F_279425217_Hr9VBkknMr4fTpuZbxZXfcYdC7jSvGl2.jpg`
   <br>
Wenn Sie aus dem Wertefeld klicken, sollte Ihr Bild angezeigt werden.

   ![in der Vorschau angezeigte Medien](/help/summit/l820-lab-workbook/assets/3-1-3-2-media.png)

2. Fügen Sie im folgenden Abschnitt **[!UICONTROL Inhalt]** Ihren eigenen benutzerdefinierten Text hinzu, den Sie in Ihrer Nachricht für den **[!UICONTROL Header]** und den **[!UICONTROL Hauptteil]** anzeigen möchten.

   ![Kopfzeile und Textkörper](/help/summit/l820-lab-workbook/assets/3-1-3-2-content.png)

3. Zusätzliche Optionen:
   1. **Schaltflächen:**

      ![Schaltflächenabschnitt](/help/summit/l820-lab-workbook/assets/3-1-3-2-buttons.png)

      1. In diesem Abschnitt des Editors können Sie den Text für Ihre CTA-Schaltfläche anpassen, indem Sie das Feld Schaltflächentext bearbeiten.

      2. Das Feld **[!UICONTROL Interact event]** wird verwendet, um den Wert zu definieren, der an das SDK übergeben wird, wenn der CTA vom Benutzer gedrückt wird.

      3. Das Feld **[!UICONTROL Ziel]** wird verwendet, um zu definieren, wohin der CTA den Benutzer führen soll. Dazu gehören URLs und Deeplinks. Sie können diesen Deeplink beispielsweise zu einer Produktseite wie `dxdemo://exoticVibes` hinzufügen.

      4. Sie können zusätzliche Schaltflächen hinzufügen, indem Sie auf **[!UICONTROL + Schaltfläche &quot;Hinzufügen&quot;]** drücken.

      5. Wenn eine zweite Schaltfläche zu Ihrer Nachricht hinzugefügt wird, können Sie jetzt das Schaltflächenlayout mit der Dropdown-Liste ändern.


   2. **Erweiterte Formatierung**

      ![Umschalter für erweiterte Formatierung](/help/summit/l820-lab-workbook/assets/3-1-3-2-advanced-formatting-toggle.png)

      Durch Aktivierung dieses Umschalters erhalten Sie im Editor zusätzliche Anpassungsoptionen.

      1. Mediengröße
      1. Schriftart
      1. Punktgröße
      1. Schriftfarbe
      1. Ausrichtung

      ![Erweiterte Formatierungsoptionen](/help/summit/l820-lab-workbook/assets/3-1-3-2-advanced-formatting-options.png)

   3. **Registerkarte &quot;Einstellungen&quot;**

      Durch Wechsel zu dieser Registerkarte und im Abschnitt **[!UICONTROL Vorschau]** können Sie die **App-Vorschau** ändern.
      <br>\
      ![Registerkarte &quot;Einstellungen&quot;](/help/summit/l820-lab-workbook/assets/3-1-3-1-settings-tab.png)
      <br>

      1. Im Abschnitt **[!UICONTROL Layout]** haben Sie die Möglichkeit, ein Bild als Hintergrund oder als Volltonfarbe zu verwenden.

      2. Der Abschnitt **[!UICONTROL Nachricht]** enthält benutzerdefinierte Interaktionen, die für Ihre Nachricht aktiviert werden können:
         1. Benutzerdefinierte Gesten
         2. Übernahme der Benutzeroberfläche
         3. Übernahme der benutzerdefinierten Benutzeroberfläche
         4. Benutzerdefinierte Größe
         5. Benutzerdefinierte Position
         6. Benutzerdefinierte Animation
         7. Nachricht mit abgerundeter Ecke
   <br>
4. Wenn Sie die Inhaltserstellung abgeschlossen haben und mit Ihrer Nachricht zufrieden sind, klicken Sie auf die Schaltfläche **[!UICONTROL Überprüfen, um ] zu aktivieren** .

   >[!SUCCESS]
   >
   > Sie haben nun die Bearbeitung Ihrer mobilen In-App-Nachricht abgeschlossen. Sie sollten sich jetzt auf der Seite Campaign **[!UICONTROL Überprüfen, um]** zu aktivieren befinden.
   >
   >![Überprüfen und Aktivieren](/help/summit/l820-lab-workbook/assets/3-1-4-1-review-and-activate.png)
   >
   > Hier können Sie eine vollständige Zusammenfassung Ihrer Nachricht sehen.
   >
   > *Beachten Sie den benutzerdefinierten Wert, den Sie als Trigger-Regel verwendet haben. Mit diesem Wert wird Ihre In-App-Nachricht ausgelöst. Der verwendete Wert befindet sich im markierten Bereich der Zusammenfassungsseite.*

   >[!NOTE]
   >Der aktuelle Trigger für die In-App-Nachricht ist das standardmäßige **Anwendungsstartereignis passiert**, d. h. die In-App-Nachricht wird beim Start der App ausgelöst. Sie können dies im Abschnitt **[!UICONTROL Zeitplan]** sehen.

5. Wenn Sie die Überprüfung Ihrer Kampagne abgeschlossen haben, klicken Sie auf die Schaltfläche Aktivieren , um die Kampagne zu veröffentlichen.
   <br>
   ![activate](/help/summit/l820-lab-workbook/assets/3-1-4-2-activate.png)


>[!SUCCESS]
>
> Jetzt sollte das Kampagnen-Dashboard angezeigt werden. Suchen Sie Ihre Kampagne durch Scrollen oder mithilfe der Suchfunktion. Wenn Ihre Kampagne den Status in **[!UICONTROL Live]** (~1min) ändert, wurde Ihre Kampagne jetzt veröffentlicht.
>
> ![Veröffentlichte Kampagne](/help/summit/l820-lab-workbook/assets/3-1-3-2-published-campaign.png)
>


## Üben 2.4 Trigger der mobilen In-App-Nachricht

So aktualisieren Sie die Payload und laden Ihre neu veröffentlichte Kampagne herunter:

1. Schließen Sie auf Ihrem Mobilgerät die Fréscopa-App vollständig.
2. Öffnen Sie die Fréscopa-App erneut.
3. Navigieren Sie nun zur Registerkarte Übung der App.

   ![Schaltfläche &quot;Übung&quot;](/help/summit/l820-lab-workbook/assets/3-2-3-app-exercise-button.png)

4. Geben Sie im Textfeld Ihren benutzerdefinierten Trigger-Wert ein, den Sie in Campaign definiert haben. Klicken Sie dann auf Senden.


   ![modify](/help/summit/l820-lab-workbook/assets/3-2-2-1-app-condition.PNG){width="250" align="center" zoomable="yes"}

>[!SUCCESS]
>
>Durch Klicken auf &quot;Senden&quot;haben Sie manuell einen Trigger ausgelöst und die von Ihnen erstellte In-App-Benachrichtigung wird angezeigt:
>
>![In-App-Nachricht](/help/summit/l820-lab-workbook/assets/3-1-3-3-in-app-message.png)
>
> *Wenn Probleme auftreten, die Ihre Nachricht auslösen, überprüfen Sie Folgendes:*
> 
> * *Vergewissern Sie sich, dass Sie in das Feld Ereignisname in Ihrer App den Wert Ihrer Trigger-Regel genau so eingeben, wie er in der Kampagne vorhanden war.*
> * *Stellen Sie sicher, dass die Groß-/Kleinschreibung korrekt ist und dass Sie kein führendes oder End-Leerzeichen haben.*
> * *Sie können den Wert Ihrer Kampagnenregel nachschlagen, den Sie verwendet haben, wenn Sie zu Ihrer Kampagnenübersichtsseite zurückkehren, indem Sie im Kampagnen-Dashboard auf Ihre Trigger-Kampagne klicken.*

Sie haben gerade Ihre erste In-App-Nachricht für Journey Optimizer verfasst und veröffentlicht!


## Bonusübungen: Kampagnen duplizieren und Vorschau auf Gerät anzeigen

Die Funktionen **Kampagne duplizieren** und **Vorschau auf Gerät** sind vordefinierte Funktionen, mit denen Sie Ihre Kampagnen duplizieren und Ihre In-App-Nachrichten direkt auf Ihrem Gerät testen und überprüfen können, bevor Sie sie aktivieren. In dieser Übung erfahren Sie, wie Sie diese Funktion verwenden und eine Vorschau der in Übung 3.1 erstellten Nachricht anzeigen.

1. Öffnen Sie die soeben erstellte Kampagne, indem Sie auf der Dashboard-Seite Kampagnen auf den Namen der Kampagne klicken, um die Kampagne zu öffnen. Dadurch gelangen Sie zurück zur Seite **[!UICONTROL Kampagne überprüfen]** .
1. Drücken Sie die Taste **[!UICONTROL Duplizieren]**. Dadurch wird eine neue Eingabeaufforderung geöffnet, um Ihre neue Kampagne zu benennen, die dupliziert wird. Fügen Sie einen neuen Namen hinzu, an den Sie sich einfach erinnern können, oder verwenden Sie den Standardnamen, bei dem standardmäßig **[!DNL _copy]** hinzugefügt wird.

   ![doppelte Kampagne](/help/summit/l820-lab-workbook/assets/3-2-duplicate-campaign.png)

1. Wenn Sie auf die Schaltfläche Duplizieren klicken, wird Ihre duplizierte Kampagne erstellt und Sie werden zum Dashboard der Kampagnen zurückgeleitet.
1. Sobald Ihre Kampagne dupliziert wurde, öffnen Sie die neue Kampagne.

1. Sie können auf die Funktion Vorschau auf Gerät auf der Seite **[!UICONTROL Kampagnenübersicht]** oder im Schritt **[!UICONTROL Kampagnenautor]** zugreifen.

   ![Vorschau auf Geräteschaltfläche](/help/summit/l820-lab-workbook/assets/3-3-1-1-preview-on-device-button.png)
   <br>

1. Klicken Sie anschließend im Bildschirm &quot;Verbindung mit Gerät&quot;auf die Schaltfläche **[!UICONTROL Start]** .

   ![Schaltfläche &quot;Start&quot;](/help/summit/l820-lab-workbook/assets/3-3-1-2-connect-to-device-start.png)
   <br>

1. Geben Sie die Basis-URL ein, die für den Start der Fréscopa-App konfiguriert wurde: `dxdemo://`

   ![Vorschau-URL](/help/summit/l820-lab-workbook/assets/3-3-1-3-preview-url.png)

   <br>

1. Befolgen Sie die Anweisungen auf dem Bildschirm:
   1. Scannen Sie den QR-Code mit Ihrem Mobilgerät, und die Fréscopa-App wird mit einem Bildschirm geöffnet, auf dem Sie einen angezeigten Pin eingeben können.
   2. Geben Sie den in AJO angezeigten Pin auf dem Gerätebildschirm ein und klicken Sie auf die Schaltfläche Verbinden , die nach Eingabe des Pins unten rechts angezeigt wird.


   ![enter pin](/help/summit/l820-lab-workbook/assets/3-3-1-5-enter-pin.PNG){width="250" align="center" zoomable="yes"}
   <br>
1. Dieses Popup wird auf dem Bildschirm Ihres Computers angezeigt

   ![pop-up](/help/summit/l820-lab-workbook/assets/3-3-pop-up.png)

1. Klicken Sie auf die Schaltfläche Fertig . Dadurch wird das Dialogfeld geschlossen und Ihr Telefon ist jetzt mit der Vorschau auf dem Gerät verbunden.


>[!SUCCESS]
>
> Ihre In-App-Nachricht wird auf Ihrem Gerät angezeigt.
>
> *Nach der Verbindung sollte Ihre In-App-Nachricht jedes Mal angezeigt werden. Klicken Sie dazu auf die Schaltfläche **[!UICONTROL Vorschau auf Gerät]** .

## Zusätzliche Ressourcen

**Videos:**

* [Erstellen einer In-App-Kampagne](/help/channels/create-an-in-app-campaign.md)
* [Verfassen einer In-App-Nachricht ](/help/channels/author-in-app-messages.md)

**Produktdokumentation:**

* [Erste Schritte mit dem In-App-Kanal](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/in-app/get-started-in-app)
* [ Mobile In-App-Nachricht erstellen](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/in-app/create-in-app)
* [Gestalten Ihrer In-App-Inhalte](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/in-app/design-in-app)
* [Überprüfen und Senden Ihrer In-App-Benachrichtigung](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/in-app/send-in-app)
