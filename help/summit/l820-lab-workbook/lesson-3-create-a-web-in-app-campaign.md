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
source-git-commit: c509c768d07984d07ed2ec65634e000c54bb6ff1
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 0%

---



# Lektion 3: Erstellen einer Web-In-App-Kampagne

Nachdem Sie nun mobile Erlebnisse für die App erstellt haben, erstellen Sie in dieser Lektion eines der Erlebnisse, die Sie auf der Fréscopa-Website gesehen haben. Sie erstellen eine Web-In-App-Kampagne. Sie entwerfen und passen eine Nachricht an und definieren einen Trigger, der die Nachricht auslöst.

## Lernziele

* Erfahren Sie, wie Sie eine Web-In-App-Kampagne erstellen.
* Trigger einer In-App-Nachricht.

## Übung 3.1 Erstellen einer Web-In-App-Kampagne

In dieser Übung erstellen Sie die Kampagne und definieren, auf welcher Webseite die In-App-Nachricht angezeigt wird.

1. In Journey Optimizer im linken Navigationsbereich unter **JOURNEY MANAGEMENT** select **Kampagnen**.

1. Klicks **Kampagne erstellen**.

   ![CreateCampaign](/help/summit/l820-lab-workbook/assets/4-1-create-campaign.png)

1. Im **Kampagne erstellen** in der **Aktion** auswählen, wählen Sie die **In-App-Nachricht** aktivieren.

1. Aus dem **Senden an** Dropdown-Liste auswählen **Web.**

1. Geben Sie die folgende URL ein: **https://dsn.adobe.com/web/adobe-summit-2024/exercise** - *Dies ist die Webseite, auf der Ihre Nachricht erscheinen wird.*

   ![In-App-URL](/help/summit/l820-lab-workbook/assets/4-1-1-in-app-url.png)

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

## Übung 3.2 Konfigurieren Ihrer Kampagne

Auf dieser Seite definieren Sie die Eigenschaften der Kampagne und das Ereignis, mit dem die In-App-Nachricht auf der Webseite angezeigt werden soll. Behalten Sie alle anderen Einstellungen standardmäßig bei. Für diese Übung müssen Sie keine bestimmte Zielgruppe definieren.

### 3.2.1 [!UICONTROL Eigenschaftenabschnitt]

1. Im **Eigenschaften** -Abschnitt, um Ihrer Kampagne eine eindeutige **Name**:

   >[!NOTE]
   > Beginnen Sie den Namen mit Ihrer Sitznummer, damit Sie
   > Sie finden Ihre Kampagne später.
   > 
   > Wenn Ihre Sitznummer beispielsweise 99 ist: 
   >
   > ![Eigenschaftsname](/help/summit/l820-lab-workbook/assets/4-1-2-properties-name.png)


### 3.2.2 Benutzerdefinierte Trigger-Regel einrichten

In diesem Abschnitt legen Sie fest, welche Trigger die Nachricht auf der Website anzeigen soll. Sie definieren einen eindeutigen Trigger, mit dem Sie die Nachricht nur an sich selbst senden können.

1. Scrollen Sie nach unten zum **[!UICONTROL Trigger-Abschnitt]** Klicken Sie auf **[!UICONTROL Trigger bearbeiten]**.

   ![modifizieren](/help/summit/l820-lab-workbook/assets/3-2-1-2-edit-triggers.png)

1. Klicken Sie im Regel-Builder auf **[!UICONTROL Anwendungsstart]** und wählen Sie aus der Dropdown-Liste  *Daten an Platform gesendet*.
   ![Dropdown-Liste für Trigger-Ereignisse](/help/summit/l820-lab-workbook/assets/trigger-drop-down-sent-to-platform.png)

1. Hinzufügen einer Bedingung durch Klicken auf **[!UICONTROL + Bedingung hinzufügen]**.

   ![Schaltfläche &quot;Bedingung hinzufügen&quot;](/help/summit/l820-lab-workbook/assets/3-2-1-3-add-condition.png)

1. Aus dem **[!UICONTROL Eigenschaft auswählen]** Dropdown-Liste auswählen **[!UICONTROL XDM-Ereignistyp]**.

   ![XDM-Ereignistyp](/help/summit/l820-lab-workbook/assets/4-1-2-dropdown-xdm-event.png)


1. Fügen Sie im folgenden Textfeld eine *`<custom string value>`* dass Sie sich daran erinnern können, und drücken Sie **[!UICONTROL Hinzufügen]** `<custom string value>` , um den Wert zu speichern.

   Dieser benutzerdefinierte Zeichenfolgenwert wird später verwendet, um Ihre Nachricht auszulösen.

   >[!TIP]
   > Wenn Sie Ihre Sitznummer zum benutzerdefinierten Zeichenfolgenwert hinzufügen, wird es für Sie einzigartig und einfacher, sich daran zu erinnern.
   > 
   > Beispiel: `99web`
   > 

   ![benutzerdefinierten Trigger-Zeichenfolgenwert hinzufügen](/help/summit/l820-lab-workbook/assets/4-1-2-add-custom-trigger-dropdown.png)

1. Drücken Sie die **[!UICONTROL Fertig]** Schaltfläche oben rechts.

>[!SUCCESS]
>
>Sie haben Ihre Web-In-App-Nachricht jetzt mit einem benutzerspezifischen Trigger-Ereignis definiert.
>
>![Webkampagne mit definiertem Trigger](/help/summit/l820-lab-workbook/assets/4-1-2-2-web-campaign-with-custom-trigger.png)


### 3.2.3 Inhalt der In-App-Nachricht bearbeiten

In diesem Abschnitt definieren Sie den Inhalt, das Design und das Layout Ihrer Nachricht.

1. Klicken Sie auf **Inhalt bearbeiten** im **Aktion** -Abschnitt, um auf das Authoring-Konstrukt zuzugreifen.

   ![Schaltfläche &quot;Inhalt bearbeiten&quot;](/help/summit/l820-lab-workbook/assets/3-1-3-1-edit-content-button.png)

1. Der Authoring-Prozess ist derselbe Prozess, den Sie in den oben genannten Mobile In-App-Übungen abgeschlossen haben. Nehmen Sie sich Zeit, um Ihre Nachricht mit Ihrem eigenen Titel, Körper und Medieninhalt frei zu bearbeiten.

   Wenn Sie das modale Layout oder das Vollbildlayout verwenden, können Sie eine Schaltfläche hinzufügen. Sie können diese URL verwenden, um die Produktseite zu öffnen: **https://dsn.adobe.com/web/adobe-summit-2024/P2WsaDPf_**

1. Wenn Sie mit der Bearbeitung der Nachricht fertig sind, klicken Sie auf **[!UICONTROL Aktivieren]**.

1. Wenn alles auf dem Prüfungsbildschirm gut aussieht, klicken Sie auf **[!UICONTROL Aktivieren]** , um Ihre Web-In-App-Nachricht zu veröffentlichen.

1. Sie werden zum Kampagnen-Dashboard zurückgeleitet.

   Warten Sie, bis sich der Kampagnenstatus ändert **Live** vor der Umstellung auf Version 4.1.4.

## Üben Sie 3.3 Trigger der Web-In-App-Nachricht

1. Navigieren Sie zur Website &quot;Fréscopa&quot;und navigieren Sie zur **Übung** in Ihrem Browser.

   ![Link zu Webübungen](/help/summit/l820-lab-workbook/assets/4-2-frescopa-web-exercise-link.png)

1. Aktualisieren Sie die Webseite unbedingt.

1. Geben Sie den eindeutigen Zeichenfolgenwert ein, den Sie in Ihrer Kampagne definiert haben.

   ![Übungsseite](/help/summit/l820-lab-workbook/assets/4-2-exercise-page.png)

1. Klicken Sie auf **[!UICONTROL Senden]**.

>[!SUCCESS]
>
>Wenn Sie auf die Schaltfläche Senden mit Ihrem eindeutigen Wert klicken, wird Ihre Web-In-App-Nachricht ausgelöst. Außerdem sollte Ihre Web-In-App-Nachricht auf dem Bildschirm angezeigt werden.
>
>Diese Übung simulierte ein benutzerspezifisches XDM-Versandereignis, das Sie durch Ihr Fréscopa-Kundenerlebnis gesehen haben.
