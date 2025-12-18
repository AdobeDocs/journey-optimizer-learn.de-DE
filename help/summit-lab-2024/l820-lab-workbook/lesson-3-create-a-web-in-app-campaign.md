---
title: 'Lektion 3: Erstellen einer Web-In-App-Kampagne'
description: Erstellen und Trigger einer Web-In-App-Kampagne.
feature: In App
role: User
level: Intermediate
doc-type: Article
duration: 0
recommendations: noDisplay, noCatalog
jira: KT-13983
thumbnail: KT-13983.jpeg
exl-id: 0f84adfb-edb1-47fa-b696-58eec2b33bb1
source-git-commit: 7b3d668e8400d9f86c764f5dc4c4455b50cd0cdc
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 2%

---

# Lektion 3: Erstellen einer Web-In-App-Kampagne

Nachdem Sie nun mobile Erlebnisse für die App erstellt haben, erstellen Sie in dieser Lektion eines der Erlebnisse, die Sie auf der Fréscopa-Website gesehen haben. Sie erstellen eine Web-In-App-Kampagne. Sie entwerfen und passen eine Nachricht an und definieren einen Trigger, der die Nachricht auslöst.

## Lernziele

* Wissen, wie Sie eine Web-In-App-Kampagne erstellen.
* Trigger einer In-App-Nachricht.

## Übung 3.1 Erstellen einer Web-In-App-Kampagne

In dieser Übung erstellen Sie die Kampagne und definieren, auf welcher Web-Seite die In-App-Nachricht angezeigt wird.

1. Wählen Sie in Journey Optimizer im linken Navigationsbereich unter **JOURNEY-VERWALTUNG** die Option **Kampagnen** aus.

1. Klicken Sie **Kampagne erstellen**.

   ![CreateCampaign](/help/summit-lab-2024/l820-lab-workbook/assets/4-1-create-campaign.png)

1. Aktivieren Sie auf **Seite** Kampagne erstellen“ im Abschnitt **Aktion** das Kontrollkästchen **In-App-**.

1. Wählen Sie im **Senden an** die Option **Web.**

1. Geben Sie die folgende URL ein: **https://dsn.adobe.com/web/adobe-summit-2024/exercise** - *Dies ist die Webseite, auf der Ihre Nachricht angezeigt wird.*

   ![In-App-URL](/help/summit-lab-2024/l820-lab-workbook/assets/4-1-1-in-app-url.png)

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

## Übung 3.2 Kampagne konfigurieren

Trigger Auf dieser Seite definieren Sie die Eigenschaften der Kampagne und das Ereignis, durch das die In-App-Nachricht auf der Web-Seite angezeigt werden soll. Belassen Sie alle anderen Einstellungen auf der Standardeinstellung. Für diese Übung müssen Sie keine bestimmte Zielgruppe definieren.

### 3.2.1 [!UICONTROL Abschnitt „Eigenschaften“]

1. Geben Sie **Abschnitt** Ihrer Kampagne einen eindeutigen **Namen**:

   >[!NOTE]
   > Achten Sie darauf, den Namen mit Ihrer Sitznummer zu beginnen, damit Sie leicht
   > Finden Sie Ihre Kampagne später.
   > 
   > Wenn Ihre Sitznummer beispielsweise 99 lautet: 
   >
   > ![Eigenschaftsname](/help/summit-lab-2024/l820-lab-workbook/assets/4-1-2-properties-name.png)


### 3.2.2 Benutzerdefinierte Trigger-Regel einrichten

In diesem Abschnitt legen Sie fest, welche Trigger die Nachricht auf der Website anzeigen sollen. Sie definieren einen eindeutigen Trigger, mit dem Sie die Nachricht nur an sich selbst senden können.

1. Scrollen Sie nach unten zum Abschnitt **[!UICONTROL Trigger]** klicken Sie dann auf **[!UICONTROL Trigger bearbeiten]**.

   ![Ändern](/help/summit-lab-2024/l820-lab-workbook/assets/3-2-1-2-edit-triggers.png)

1. Klicken Sie im Regel-Builder auf **[!UICONTROL Anwendungsstart]** und wählen Sie aus der Dropdown-Liste *Daten an Platform gesendet*.
   ![Dropdown für Trigger-Ereignis](/help/summit-lab-2024/l820-lab-workbook/assets/trigger-drop-down-sent-to-platform.png)

1. Fügen Sie eine Bedingung hinzu, indem Sie auf **[!UICONTROL + Bedingung hinzufügen]**.

   ![Schaltfläche „Bedingung hinzufügen“](/help/summit-lab-2024/l820-lab-workbook/assets/3-2-1-3-add-condition.png)

1. Wählen Sie in der **[!UICONTROL Eigenschaft auswählen]** die Option **[!UICONTROL XDM-Ereignistyp]** aus.

   ![XDM-Ereignistyp](/help/summit-lab-2024/l820-lab-workbook/assets/4-1-2-dropdown-xdm-event.png)


1. Fügen Sie im folgenden Textfeld einen *`<custom string value>`* hinzu, an den Sie sich erinnern können, und drücken Sie **[!UICONTROL Hinzufügen]** `<custom string value>`, um den Wert zu speichern.

   Dieser benutzerdefinierte Zeichenfolgenwert wird später zum Auslösen Ihrer Nachricht verwendet.

   >[!TIP]
   > Wenn Sie Ihre Sitznummer zum benutzerdefinierten Zeichenfolgenwert hinzufügen, wird es eindeutig und für Sie leichter, sich an sie zu erinnern.
   > 
   > Beispiel: `99web`
   > 

   ![Benutzerdefinierten Trigger-Zeichenfolgenwert hinzufügen](/help/summit-lab-2024/l820-lab-workbook/assets/4-1-2-add-custom-trigger-dropdown.png)

1. Klicken Sie **[!UICONTROL oben rechts]** die Schaltfläche „Fertig“.

>[!SUCCESS]
>
>Sie haben jetzt Ihre Web-In-App-Nachricht mit einem benutzerdefinierten Trigger-Ereignis definiert.
>
>![Web-Kampagne mit benutzerdefiniertem Trigger definiert](/help/summit-lab-2024/l820-lab-workbook/assets/4-1-2-2-web-campaign-with-custom-trigger.png)


### 3.2.3 Bearbeiten des Inhalts der In-App-Nachricht

In diesem Abschnitt definieren Sie Inhalt, Design und Layout Ihrer Nachricht.

1. Klicken Sie auf **Schaltfläche** Inhalt bearbeiten“ im Abschnitt **Aktion**, um auf das Authoring-Konstrukt zuzugreifen.

   ![Schaltfläche „Inhalt bearbeiten“](/help/summit-lab-2024/l820-lab-workbook/assets/3-1-3-1-edit-content-button.png)

1. Der Authoring-Prozess ist derselbe Prozess, den Sie in den obigen Mobile-In-App-Übungen abgeschlossen haben. Nehmen Sie sich Zeit, um Ihre Nachricht mit Ihrem eigenen Titel, Textkörper und Medieninhalt frei zu bearbeiten.

   Wenn Sie das modale oder Vollbild-Layout verwenden, können Sie eine Schaltfläche hinzufügen. Mit dieser URL können Sie die Produktseite öffnen: **https://dsn.adobe.com/web/adobe-summit-2024/P2WsaDPf_**

1. Wenn Sie die Bearbeitung Ihrer Nachricht abgeschlossen haben, klicken Sie auf **[!UICONTROL Zum Aktivieren überprüfen]**.

1. Wenn auf dem Überprüfungsbildschirm alles gut aussieht, klicken Sie auf **[!UICONTROL Aktivieren]**, um Ihre Web-In-App-Nachricht zu veröffentlichen.

1. Sie kehren zum Kampagnen-Dashboard zurück.

   Warten Sie, während sich der Kampagnenstatus in &quot;**&quot; ändert** bevor Sie zu 4.1.4 wechseln.

## Übung 3.3 Trigger der Web-In-App-Nachricht

1. Rufen Sie die Fréscopa-Website auf und navigieren Sie in Ihrem Browser zur **Übung**-Seite.

   ![Link für Webübungen](/help/summit-lab-2024/l820-lab-workbook/assets/4-2-frescopa-web-exercise-link.png)

1. Stellen Sie sicher, dass Sie die Web-Seite aktualisieren.

1. Geben Sie den eindeutigen Zeichenfolgenwert ein, den Sie in Ihrer Kampagne definiert haben.

   ![Übungsseite](/help/summit-lab-2024/l820-lab-workbook/assets/4-2-exercise-page.png)

1. Klicken Sie auf **[!UICONTROL Senden]**.

>[!SUCCESS]
>
>Wenn Sie mit Ihrem eindeutigen Wert auf die Schaltfläche Senden klicken, wird Ihre Web-In-App-Nachricht in Trigger gesetzt. Und Sie sollten sehen, dass Ihre Web-In-App-Nachricht auf Ihrem Bildschirm erscheint.
>
>In dieser Übung wurde ein benutzerdefiniertes XDM-Sendeereignis simuliert, das Sie durch Ihr Fréscopa-Kundenerlebnis gesehen haben.


## Weitere Ressourcen

**Anleitungsvideos:**

* [Erstellen einer In-App-Kampagne](/help/channels/create-an-in-app-campaign.md)
* [Verfassen einer In-App-Nachricht ](/help/channels/author-in-app-messages.md)

**Produktdokumentation:**

* [Erste Schritte mit dem In-App-Kanal](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/in-app/get-started-in-app)
* [Erstellen einer Web-In-App-Nachricht](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/in-app/create-in-app-web)
* [Gestalten Ihrer In-App-Inhalte](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/in-app/design-in-app)
* [Überprüfen und Senden Ihrer In-App-Benachrichtigung](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/in-app/send-in-app)
