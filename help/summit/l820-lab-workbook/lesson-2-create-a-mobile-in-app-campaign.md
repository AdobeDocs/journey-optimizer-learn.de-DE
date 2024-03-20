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
source-git-commit: c509c768d07984d07ed2ec65634e000c54bb6ff1
workflow-type: tm+mt
source-wordcount: '1395'
ht-degree: 0%

---


# Lektion 2: Erstellen einer mobilen In-App-Kampagne

In dieser Lektion erstellen und Trigger für mobile In-App-Nachrichten.

## Lernziele

* Erfahren Sie, wie In-App-Nachrichten ausgelöst werden.
* Erfahren Sie, wie Sie eine mobile In-App-Kampagne erstellen.
* Trigger einer In-App-Nachricht.

## Übung 2.1 - Anmeldung bei Journey Optimizer

1. Öffnen [Adobe Journey Optimizer](https://experience.adobe.com/#/@techmarketingdemos/sname:summit-ajo-lab/journey-optimizer/home){target="_blank"}
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
   ![Personalisierungs-Popup](/help/summit/l820-lab-workbook/assets/2-1-4-ajo-personalization-pop-up.png)


>[!SUCCESS]
>
>Sie sollten bei Journey Optimizer und auf der Startseite angemeldet sein:
>
>![AJO-Homepage](/help/summit/l820-lab-workbook/assets/2-1-5-ajo-homepage.png)


## Übung 2.2 Eine mobile In-App-Kampagne erstellen

In dieser Übung erstellen Sie eine In-App-Nachrichtenkampagne, die ausgelöst wird, wenn Sie die App öffnen.

1. Wählen Sie in Journey Optimizer im linken Navigationsbereich die Option **[!UICONTROL Kampagnen]**.

1. Klicks **[!UICONTROL Kampagne erstellen]**.

   ![Kampagne erstellen](/help/summit/l820-lab-workbook/assets/2-3-1-1-create-campaign.png)

1. Im **[!UICONTROL Kampagne erstellen]** in der  **[!UICONTROL Aktion]** auswählen, wählen Sie die **[!UICONTROL In-App-Nachricht]** aktivieren.

1. Aus dem **[!UICONTROL Senden an]** Dropdown-Liste auswählen **[!DNL Mobile]**.

1. Aus dem **[!UICONTROL Anwendungsoberfläche]** Dropdown-Liste auswählen **[!DNL Frecopa Mobile App]**.

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

   ![Anwendungsoberfläche](/help/summit/l820-lab-workbook/assets/3-1-1-1-create.png)

>[!SUCCESS]
>
>Sie sollten nun die Campaign-Eigenschaften verwenden:
>
> ![Kampagneneigenschaften](/help/summit/l820-lab-workbook/assets/3-1-1-2-campaign-properties.png)

## Übung 2.3 Konfigurieren der Kampagne

### 2.3.1 [!UICONTROL Eigenschaftenabschnitt]

Geben Sie Ihrer Kampagne einen Namen. Beginnen Sie den Namen mit Ihrer Sitznummer, damit Sie Ihre Kampagne einfach wiederfinden können.

Wenn Ihre Sitznummer beispielsweise 99 ist:  `99 - Welcome Campaign`.

![Eigenschaftenabschnitt](/help/summit/l820-lab-workbook/assets/3-1-2-1-properties-section.png)

### 2.3.2 Benutzerdefinierte Trigger-Regel einrichten

1. Scrollen Sie nach unten zum **[!UICONTROL Trigger-Abschnitt]** Klicken Sie auf **[!UICONTROL Trigger bearbeiten]**.

   ![modifizieren](/help/summit/l820-lab-workbook/assets/3-2-1-2-edit-triggers.png)

1. Klicken Sie im Regel-Builder auf **[!UICONTROL Anwendungsstart]** und wählen Sie aus der Dropdown-Liste  *Daten an Platform gesendet*.
   ![An die Datenplattform gesendet](/help/summit/l820-lab-workbook/assets/trigger-drop-down-sent-to-platform.png)

1. Hinzufügen einer Bedingung durch Klicken auf **[!UICONTROL Bedingung hinzufügen]**.

   ![Schaltfläche &quot;Bedingung hinzufügen&quot;](/help/summit/l820-lab-workbook/assets/3-2-1-3-add-condition.png)

1. Aus dem **[!UICONTROL Eigenschaft auswählen]** Dropdown-Liste auswählen **[!UICONTROL XDM-Ereignistyp]**.

   ![XDM-Ereignistyp](/help/summit/l820-lab-workbook/assets/4-1-2-dropdown-xdm-event.png)

1. Fügen Sie im folgenden Textfeld eine *`<custom string value>`* dass du dich erinnern kannst.

1. Klicken Sie zum Speichern des Werts auf **[!UICONTROL Hinzufügen von**] `<custom string value>`.

   Dieser benutzerdefinierte Zeichenfolgenwert wird später verwendet, um Ihre Nachricht auszulösen.

   >[!TIP]
   > Wenn Sie Ihre Sitznummer zum benutzerdefinierten Zeichenfolgenwert hinzufügen, ist es für Sie einzigartig und einfacher, sich daran zu erinnern.
   > 
   > Beispiel: `99exerciseTrigger`

   ![benutzerdefinierten Trigger-Zeichenfolgenwert hinzufügen](/help/summit/l820-lab-workbook/assets/3-1-2-2-add-custom-trigger.png)

1. Klicks **[!UICONTROL Fertig]** oben rechts.

>[!SUCCESS]
>
>Sie haben Ihre In-App-Nachricht jetzt mit einem benutzerdefinierten Trigger-Ereignis definiert.
>
>![Kampagne mit definiertem Trigger](/help/summit/l820-lab-workbook/assets/3-1-2-2-campaign-with-custom-trigger.png)


### 2.3.3 Inhalt der In-App-Nachricht bearbeiten

Im **[!UICONTROL Aktion]** Abschnitt, klicken Sie auf **[!UICONTROL Inhalt bearbeiten]**.

![Schaltfläche &quot;Inhalt bearbeiten&quot;](/help/summit/l820-lab-workbook/assets/3-1-3-1-edit-content-button.png)

Die [!UICONTROL In-App-Nachricht] -Editor angezeigt, in dem Sie den Inhalt der In-App-Nachricht konfigurieren.

#### 2.3.3.1 Layout

Wählen Sie aus, welches Layout auf Ihre Nachricht angewendet werden soll.

Klicken Sie beispielsweise auf **[!UICONTROL Modal]** , um Ihre In-App-Nachricht in ein modales Layout umzuwandeln.

![Modal-Schaltfläche](/help/summit/l820-lab-workbook/assets/3-1-3-2-modal-button.png)

#### 2.3.3.2 Nachrichten verfassen und Kampagnen veröffentlichen

1. Fügen Sie im Medienabschnitt die folgende URL ein:  `https://t3.ftcdn.net/jpg/02/79/42/52/240_F_279425217_Hr9VBkknMr4fTpuZbxZXfcYdC7jSvGl2.jpg`
   <br>
Wenn Sie aus dem Wertefeld klicken, sollte Ihr Bild angezeigt werden.

   ![in der Vorschau angezeigte Medien](/help/summit/l820-lab-workbook/assets/3-1-3-2-media.png)

2. Im Folgenden **[!UICONTROL Inhalt]** hinzufügen, fügen Sie Ihren eigenen benutzerdefinierten Text hinzu, den Sie in Ihrer Nachricht für die **[!UICONTROL Kopfzeile]** und **[!UICONTROL body]**.

   ![Kopfzeile und Hauptteil](/help/summit/l820-lab-workbook/assets/3-1-3-2-content.png)

3. Zusätzliche Optionen:
   1. **Schaltflächen:**

      ![Schaltflächenabschnitt](/help/summit/l820-lab-workbook/assets/3-1-3-2-buttons.png)

      1. In diesem Abschnitt des Editors können Sie den Text für Ihre CTA-Schaltfläche anpassen, indem Sie das Feld Schaltflächentext bearbeiten.

      2. Die **[!UICONTROL Interaktionsereignis]** -Feld wird verwendet, um den Wert zu definieren, der an das SDK übergeben wird, wenn der CTA durch den Benutzer gedrückt wird.

      3. Die **[!UICONTROL Target]** -Feld wird verwendet, um zu definieren, wo der CTA den Benutzer aufnehmen soll. Dazu gehören URLs und Deeplinks. Sie können diesen Deeplink beispielsweise zu einer Produktseite hinzufügen, z. B. `dxdemo://exoticVibes`.

      4. Durch Drücken der **[!UICONTROL Schaltfläche + Hinzufügen]**.

      5. Wenn eine zweite Schaltfläche zu Ihrer Nachricht hinzugefügt wird, können Sie jetzt das Schaltflächenlayout mit der Dropdown-Liste ändern.


   2. **Erweiterte Formatierung**

      ![Erweiterter Formatierungsschalter](/help/summit/l820-lab-workbook/assets/3-1-3-2-advanced-formatting-toggle.png)

      Durch Aktivierung dieses Umschalters erhalten Sie im Editor zusätzliche Anpassungsoptionen.

      1. Mediengröße
      1. Schriftart
      1. Pt-Größe
      1. Schriftfarbe
      1. Ausrichtung

      ![Erweiterte Formatierungsoptionen](/help/summit/l820-lab-workbook/assets/3-1-3-2-advanced-formatting-options.png)

   3. **Registerkarte &quot;Einstellungen&quot;**

      Durch Umstellung auf diese Registerkarte und im **[!UICONTROL Vorschau]** können Sie die **App-Vorschau**.
      <br>\
      ![Registerkarte &quot;Einstellungen&quot;](/help/summit/l820-lab-workbook/assets/3-1-3-1-settings-tab.png)
      <br>

      1. Die **[!UICONTROL Layout]** gibt Ihnen die Möglichkeit, ein Bild als Hintergrund oder als Volltonfarbe zu verwenden.

      2. Die **[!UICONTROL Nachricht]** bietet benutzerdefinierte Interaktionen, die für Ihre Nachricht aktiviert werden können:
         1. Benutzerdefinierte Gesten
         2. Übernahme der Benutzeroberfläche
         3. Übernahme der benutzerdefinierten Benutzeroberfläche
         4. Benutzerdefinierte Größe
         5. Benutzerdefinierte Position
         6. Benutzerdefinierte Animation
         7. Meldungsrunde
   <br>
4. Wenn Sie die Bearbeitung Ihres Inhalts abgeschlossen haben und mit Ihrer Nachricht zufrieden sind, klicken Sie auf die Schaltfläche **[!UICONTROL Aktivieren] button**.

   >[!SUCCESS]
   >
   > Sie haben nun die Bearbeitung Ihrer mobilen In-App-Nachricht abgeschlossen. Sie sollten jetzt in der Kampagne sein. **[!UICONTROL Aktivieren]** Seite.
   >
   >![Überprüfen und Aktivieren](/help/summit/l820-lab-workbook/assets/3-1-4-1-review-and-activate.png)
   >
   > Hier können Sie eine vollständige Zusammenfassung Ihrer Nachricht sehen.
   >
   > *Beachten Sie den benutzerspezifischen Wert, den Sie als Trigger-Regel verwendet haben. Mit diesem Wert wird Ihre In-App-Nachricht ausgelöst. Der verwendete Wert befindet sich im markierten Bereich der Zusammenfassungsseite.*

   >[!NOTE]
   >Der aktuelle Trigger für die In-App-Nachricht ist der standardmäßige **Anwendungsstartereignis**, was bedeutet, dass die In-App-Nachricht beim Start der App ausgelöst wird. Sie können dies im **[!UICONTROL Planungsabschnitt]**.

5. Wenn Sie die Überprüfung Ihrer Kampagne abgeschlossen haben, klicken Sie auf die Schaltfläche Aktivieren , um die Kampagne zu veröffentlichen.
   <br>
   ![Aktivieren](/help/summit/l820-lab-workbook/assets/3-1-4-2-activate.png)


>[!SUCCESS]
>
> Jetzt sollte das Kampagnen-Dashboard angezeigt werden. Suchen Sie Ihre Kampagne durch Scrollen oder mithilfe der Suchfunktion. Wenn Ihre Kampagne den Status in **[!UICONTROL Live]** (~1min), Ihre Kampagne wurde veröffentlicht.
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


   ![modifizieren](/help/summit/l820-lab-workbook/assets/3-2-2-1-app-condition.PNG){width="250" align="center" zoomable="yes"}

>[!SUCCESS]
>
>Durch Klicken auf &quot;Senden&quot;haben Sie manuell einen Trigger ausgelöst und die von Ihnen erstellte In-App-Benachrichtigung wird angezeigt:
>
>![In-App-Nachricht](/help/summit/l820-lab-workbook/assets/3-1-3-3-in-app-message.png)
>
> *Wenn Probleme auftreten, die Ihre Nachricht auslösen, überprüfen Sie Folgendes:*
> 
> * *Vergewissern Sie sich, dass Sie in das Feld Ereignisname in Ihrer App den Regelwert Ihres Triggers genau so eingeben, wie er in der Kampagne vorhanden war.*
> * *Stellen Sie sicher, dass die Groß-/Kleinschreibung korrekt ist und dass Sie kein führendes oder End-Leerzeichen haben.*
> * *Sie können den Wert Ihrer Kampagnenregel nachschlagen, den Sie verwenden, wenn Sie zur Kampagnenübersichtsseite zurückkehren, indem Sie im Kampagnen-Dashboard erneut auf Ihre Trigger-Kampagne klicken.*

Sie haben gerade Ihre erste In-App-Nachricht für Journey Optimizer verfasst und veröffentlicht!


## Bonusübungen: Kampagnen duplizieren und Vorschau auf Gerät anzeigen

Die **Kampagne duplizieren** und **Vorschau auf Gerät** Funktionen sind vordefinierte Funktionen, mit denen Sie Ihre Kampagnen duplizieren und Ihre In-App-Nachrichten direkt auf Ihrem Gerät testen und überprüfen können, bevor Sie sie aktivieren. In dieser Übung erfahren Sie, wie Sie diese Funktion verwenden und eine Vorschau der in Übung 3.1 erstellten Nachricht anzeigen.

1. Öffnen Sie die soeben erstellte Kampagne, indem Sie auf der Dashboard-Seite Kampagnen auf den Namen der Kampagne klicken, um die Kampagne zu öffnen. Dadurch gelangen Sie zurück zum **[!UICONTROL Kampagne überprüfen]** Seite.
1. Drücken Sie die **[!UICONTROL Schaltfläche &quot;Duplizieren&quot;]**. Dadurch wird eine neue Eingabeaufforderung geöffnet, um Ihre neue Kampagne zu benennen, die dupliziert wird. Fügen Sie einen neuen Namen hinzu, an den Sie sich einfach erinnern können, oder verwenden Sie den Standardnamen , bei dem **[!DNL _copy]** wird standardmäßig hinzugefügt.

   ![Kampagne duplizieren](/help/summit/l820-lab-workbook/assets/3-2-duplicate-campaign.png)

1. Wenn Sie auf die Schaltfläche Duplizieren klicken, wird Ihre duplizierte Kampagne erstellt und Sie werden zum Dashboard der Kampagnen zurückgeleitet.
1. Sobald Ihre Kampagne dupliziert wurde, öffnen Sie die neue Kampagne.

1. Sie können auf die Funktion Vorschau auf Gerät im **[!UICONTROL Kampagnenübersicht]** oder auf der Seite **[!UICONTROL Kampagnenautor]** Schritt.

   ![Vorschau auf Schaltfläche des Geräts](/help/summit/l820-lab-workbook/assets/3-3-1-1-preview-on-device-button.png)
   <br>

1. Klicken Sie anschließend auf das **[!UICONTROL Schaltfläche starten]** über den Bildschirm Verbindung mit Gerät herstellen.

   ![Schaltfläche starten](/help/summit/l820-lab-workbook/assets/3-3-1-2-connect-to-device-start.png)
   <br>

1. Geben Sie die Basis-URL ein, die für den Start der Fréscopa-App konfiguriert wurde: `dxdemo://`

   ![Vorschau-URL](/help/summit/l820-lab-workbook/assets/3-3-1-3-preview-url.png)

   <br>

1. Befolgen Sie die Anweisungen auf dem Bildschirm:
   1. Scannen Sie den QR-Code mit Ihrem Mobilgerät, und die Fréscopa-App wird mit einem Bildschirm geöffnet, auf dem Sie einen angezeigten Pin eingeben können.
   2. Geben Sie den in AJO angezeigten Pin auf dem Bildschirm &quot;Assurance&quot;Ihres Geräts ein und klicken Sie auf die Schaltfläche Connect , die unten rechts angezeigt wird, sobald Sie den Pin eingegeben haben.


   ![Eingabefeld](/help/summit/l820-lab-workbook/assets/3-3-1-5-enter-pin.PNG){width="250" align="center" zoomable="yes"}
   <br>
1. Dieses Popup wird auf dem Bildschirm Ihres Computers angezeigt

   ![Popup](/help/summit/l820-lab-workbook/assets/3-3-pop-up.png)

1. Klicken Sie auf die Schaltfläche Fertig . Dadurch wird das Dialogfeld geschlossen und Ihr Telefon ist jetzt mit der Vorschau auf dem Gerät verbunden.


>[!SUCCESS]
>
> Ihre In-App-Nachricht wird auf Ihrem Gerät angezeigt.
>
> *Sobald die Verbindung hergestellt ist, sollte Ihre In-App-Nachricht jedes Mal angezeigt werden. Klicken Sie dann auf **[!UICONTROL Vorschau auf Gerät] button**.*