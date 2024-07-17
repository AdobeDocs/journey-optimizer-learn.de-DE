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
source-git-commit: 4f5c92f79eba3651b3633b7850e993160cb1f72c
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 2%

---

# Lektion 3: Erstellen einer Web-In-App-Kampagne

Nachdem Sie nun mobile Erlebnisse für die App erstellt haben, erstellen Sie in dieser Lektion eines der Erlebnisse, die Sie auf der Fréscopa-Website gesehen haben. Sie erstellen eine Web-In-App-Kampagne. Sie entwerfen und passen eine Nachricht an und definieren einen Trigger, der die Nachricht auslöst.

## Lernziele

* Erfahren Sie, wie Sie eine Web-In-App-Kampagne erstellen.
* Trigger einer In-App-Nachricht.

## Übung 3.1 Erstellen einer Web-In-App-Kampagne

In dieser Übung erstellen Sie die Kampagne und definieren, auf welcher Webseite die In-App-Nachricht angezeigt wird.

1. Wählen Sie in Journey Optimizer im linken Navigationsbereich unter **JOURNEY-MANAGEMENT** die Option **Kampagnen**.

1. Klicken Sie auf **Kampagne erstellen**.

   ![CreateCampaign](/help/summit/l820-lab-workbook/assets/4-1-create-campaign.png)

1. Aktivieren Sie auf der Seite **Kampagne erstellen** im Abschnitt **Aktion** das Kontrollkästchen **In-App-Nachricht** .

1. Wählen Sie im Dropdown-Menü **An** senden die Option **Web** aus.

1. Geben Sie die folgende URL ein: **https://dsn.adobe.com/web/adobe-summit-2024/exercise** - *Dies ist die Webseite, auf der Ihre Nachricht angezeigt wird.*

   ![In-App-URL](/help/summit/l820-lab-workbook/assets/4-1-1-in-app-url.png)

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

## Übung 3.2 Konfigurieren Ihrer Kampagne

Auf dieser Seite definieren Sie die Eigenschaften der Kampagne und das Ereignis, mit dem die In-App-Nachricht auf der Webseite angezeigt werden soll. Behalten Sie alle anderen Einstellungen standardmäßig bei. Für diese Übung müssen Sie keine bestimmte Zielgruppe definieren.

### 3.2.1 [!UICONTROL Eigenschaftenabschnitt]

1. Geben Sie im Abschnitt **Eigenschaften** Ihrer Kampagne einen eindeutigen **Namen**:

   >[!NOTE]
   > Beginnen Sie den Namen mit Ihrer Sitznummer, damit Sie
   > Sie finden Ihre Kampagne später.
   > 
   > Wenn Ihre Sitznummer beispielsweise 99 ist: 
   >
   > ![Eigenschaftsname](/help/summit/l820-lab-workbook/assets/4-1-2-properties-name.png)


### 3.2.2 Benutzerdefinierte Trigger-Regel einrichten

In diesem Abschnitt legen Sie fest, welche Trigger die Nachricht auf der Website anzeigen soll. Sie definieren einen eindeutigen Trigger, mit dem Sie die Nachricht nur an sich selbst senden können.

1. Scrollen Sie nach unten zum Abschnitt **[!UICONTROL Trigger]** und klicken Sie dann auf **[!UICONTROL Trigger bearbeiten]**.

   ![modify](/help/summit/l820-lab-workbook/assets/3-2-1-2-edit-triggers.png)

1. Klicken Sie im Regel-Builder auf **[!UICONTROL Application Launch]** und wählen Sie aus dem Dropdown-Menü *Daten an Platform senden* aus.
   ![Dropdown-Liste für Trigger-Ereignisse](/help/summit/l820-lab-workbook/assets/trigger-drop-down-sent-to-platform.png)

1. Fügen Sie eine Bedingung hinzu, indem Sie auf **[!UICONTROL + Bedingung hinzufügen]** klicken.

   ![Schaltfläche &quot;Bedingung hinzufügen&quot;](/help/summit/l820-lab-workbook/assets/3-2-1-3-add-condition.png)

1. Wählen Sie aus der Dropdownliste **[!UICONTROL Eigenschaft auswählen]** die Option **[!UICONTROL XDM-Ereignistyp]** aus.

   ![XDM-Ereignistyp](/help/summit/l820-lab-workbook/assets/4-1-2-dropdown-xdm-event.png)


1. Fügen Sie im folgenden Textfeld einen *`<custom string value>`* hinzu, den Sie sich merken können, und drücken Sie die Taste **[!UICONTROL Hinzufügen]** `<custom string value>`, um den Wert zu speichern.

   Dieser benutzerdefinierte Zeichenfolgenwert wird später verwendet, um Ihre Nachricht auszulösen.

   >[!TIP]
   > Wenn Sie Ihre Sitznummer zum benutzerdefinierten Zeichenfolgenwert hinzufügen, wird es für Sie einzigartig und einfacher, sich daran zu erinnern.
   > 
   > Beispiel: `99web`
   > 

   ![benutzerdefinierten Trigger-Zeichenfolgenwert hinzufügen](/help/summit/l820-lab-workbook/assets/4-1-2-add-custom-trigger-dropdown.png)

1. Drücken Sie die Schaltfläche **[!UICONTROL Fertig]** oben rechts.

>[!SUCCESS]
>
>Sie haben Ihre Web-In-App-Nachricht jetzt mit einem benutzerspezifischen Trigger-Ereignis definiert.
>
>![Webkampagne mit definiertem Trigger](/help/summit/l820-lab-workbook/assets/4-1-2-2-web-campaign-with-custom-trigger.png)


### 3.2.3 Inhalt der In-App-Nachricht bearbeiten

In diesem Abschnitt definieren Sie den Inhalt, das Design und das Layout Ihrer Nachricht.

1. Klicken Sie im Abschnitt **Aktion** auf die Schaltfläche **Inhalt bearbeiten** , um auf das Authoring-Konstrukt zuzugreifen.

   ![Schaltfläche &quot;Inhalt bearbeiten&quot;](/help/summit/l820-lab-workbook/assets/3-1-3-1-edit-content-button.png)

1. Der Authoring-Prozess ist derselbe Prozess, den Sie in den oben genannten Mobile In-App-Übungen abgeschlossen haben. Nehmen Sie sich Zeit, um Ihre Nachricht mit Ihrem eigenen Titel, Körper und Medieninhalt frei zu bearbeiten.

   Wenn Sie das modale Layout oder das Vollbildlayout verwenden, können Sie eine Schaltfläche hinzufügen. Sie können diese URL zum Öffnen der Produktseite verwenden: **https://dsn.adobe.com/web/adobe-summit-2024/P2WsaDPf_**

1. Wenn Sie mit der Bearbeitung der Nachricht fertig sind, klicken Sie auf **[!UICONTROL Überprüfen, um]** zu aktivieren.

1. Wenn auf dem Prüfungsbildschirm alles gut aussieht, klicken Sie auf **[!UICONTROL Aktivieren]** , um Ihre Web-In-App-Nachricht zu veröffentlichen.

1. Sie werden zum Kampagnen-Dashboard zurückgeleitet.

   Warten Sie, bis der Kampagnenstatus in **Live** geändert wird, bevor Sie auf 4.1.4 umsteigen.

## Üben Sie 3.3 Trigger der Web-In-App-Nachricht

1. Gehen Sie zur Website &quot;Fréscopa&quot;und navigieren Sie zur Seite **Übung** in Ihrem Browser.

   ![Link &quot;Webübungen&quot;](/help/summit/l820-lab-workbook/assets/4-2-frescopa-web-exercise-link.png)

1. Aktualisieren Sie die Webseite unbedingt.

1. Geben Sie den eindeutigen Zeichenfolgenwert ein, den Sie in Ihrer Kampagne definiert haben.

   ![Übungsseite](/help/summit/l820-lab-workbook/assets/4-2-exercise-page.png)

1. Klicken Sie auf **[!UICONTROL Senden]**.

>[!SUCCESS]
>
>Wenn Sie auf die Schaltfläche Senden mit Ihrem eindeutigen Wert klicken, wird Ihre Web-In-App-Nachricht ausgelöst. Außerdem sollte Ihre Web-In-App-Nachricht auf dem Bildschirm angezeigt werden.
>
>Diese Übung simulierte ein benutzerspezifisches XDM-Versandereignis, das Sie durch Ihr Fréscopa-Kundenerlebnis gesehen haben.


## Zusätzliche Ressourcen

**Videos:**

* [Erstellen einer In-App-Kampagne](/help/channels/create-an-in-app-campaign.md)
* [Verfassen einer In-App-Nachricht ](/help/channels/author-in-app-messages.md)

**Produktdokumentation:**

* [Erste Schritte mit dem In-App-Kanal](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/in-app/get-started-in-app)
* [Erstellen einer Web-In-App-Nachricht](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/in-app/create-in-app-web)
* [Gestalten Ihrer In-App-Inhalte](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/in-app/design-in-app)
* [Überprüfen und Senden Ihrer In-App-Benachrichtigung](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/in-app/send-in-app)
