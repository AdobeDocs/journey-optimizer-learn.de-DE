---
title: Journey erstellen
description: Journey erstellen, die beim price.drop-Ereignis ausgelöst wird
feature: Push
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-04-21T00:00:00.000Z
jira: KT-20879
exl-id: 14342b47-5485-4f7f-9312-cff1ee0f8972
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: 66e1fd99-672d-5d64-aa58-eca107f0fbae
    internal-label: Push
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: d4f3ee0d644b4f962763e6807f014efe132a9a05
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 0%
---
# Journey erstellen

In diesem Schritt erstellen Sie eine Journey in Adobe Journey Optimizer, die durch das benutzerdefinierte price.drop-Ereignis ausgelöst wird. Wenn dieses Ereignis eingeht, startet die Journey in Echtzeit und sendet eine Push-Benachrichtigung an Benutzer, die sich für das Ereignis angemeldet haben, wodurch eine ereignisgesteuerte Interaktion ermöglicht wird.

Um eine Journey zu erstellen, die beim price.drop-Ereignis ausgelöst wird, führen Sie die folgenden Schritte aus

* Bei Journey Optimizer anmelden
* Navigieren Sie zur Journey-Verwaltung | Journey | Journey erstellen

![create-Journey](assets/create-journey.png)

## PriceDropEvent hinzufügen

Ziehen Sie die `PriceDropEvent` aus dem Abschnitt Ereignisse auf die Arbeitsfläche.
![price-drop-event](assets/add-price-drop-event.png)

## Push-Aktion hinzufügen

Erweitern Sie den Abschnitt Aktionen . Ziehen Sie die Aktivität `Action` auf die Arbeitsfläche und wählen Sie als Aktionstyp Push aus
![Push-Aktion](assets/add-push-action.png)

## Konfigurieren der Push-Aktion

Wählen Sie die Aktivität Push-Benachrichtigung aus und klicken Sie auf Aktion konfigurieren .

![configure-push-action](assets/configure-push-action.png)

## Konfiguration des Push-Benachrichtigungskanals

Verknüpfen Sie `MyFirstWebPushChannel` zuvor im Tutorial erstellte Konfiguration mit dieser Push-Benachrichtigung

![channel-configuration](assets/journey-actions.png)

## Push-Benachrichtigung erstellen

Fügen Sie der Push-Benachrichtigung mithilfe des Personalisierungseditors eine Kombination aus statischem und dynamischem Inhalt hinzu, um die Nachricht ansprechender und relevanter zu gestalten.

Um mit dem Verfassen der Nachricht zu beginnen, klicken Sie auf `Content` , um die Registerkarte Inhalt zu öffnen, auf der Sie sowohl den festen Text als auch die dynamischen Felder definieren können, die aus den Ereignisdaten abgeleitet werden.
![content-push](assets/compose-message.png)

Geben Sie den Titel der Push-Nachricht an und öffnen Sie dann den Personalisierungseditor, um den Nachrichtentext zu erstellen. Der Inhalt enthält dynamisch die Namen der Produkte, deren Preise gefallen sind. Verwenden Sie dazu die Funktion each [helper .](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/personalization/functions/helpers#each)
Gehen Sie wie folgt vor, um die Liste der Produkte zu durchlaufen und ihre Namen in der Nachricht zu rendern.

## Nachrichtentext erstellen

Wählen Sie die Funktion `Each` aus dem Menü Hilfsfunktionen aus und fügen Sie sie ein.
![helper-function](assets/journey-content-helper-function.png)

Wählen Sie die kontextuellen Attribute | Journey Orchestration | Ereignisse | PriceDropEvent | productListItems | Name

Klicken Sie auf das Symbol &quot;+&quot;, um das Array in jede Schleife im Personalisierungseditor einzufügen. Aktualisieren Sie dann den Nachrichteninhalt so, dass er dem Format entspricht, das im Referenz-Screenshot angezeigt wird. Beachten Sie, dass die in Ihrer Umgebung angezeigte Ereignis-ID von der angezeigten abweichen kann.

![context-attributes](assets/journey-content-context-attributes.png)

Speichern Sie abschließend alle Ihre Änderungen und veröffentlichen Sie die Journey. Nach der Veröffentlichung wird die Journey aktiv und überwacht eingehende price.drop-Ereignisse. Wenn ein solches Ereignis eingeht, wird der Journey in Echtzeit ausgelöst und eine Push-Benachrichtigung wird an Benutzerinnen und Benutzer gesendet, die sich für den Empfang von Benachrichtigungen entschieden haben, wodurch eine rechtzeitige und relevante Interaktion sichergestellt wird.

## Testen der Lösung

Um den Trigger des price.drop-Ereignisses auszuführen, öffnen Sie die [price drop Trigger&quot;, wählen ](http://localhost:3000/price-drop-trigger.html) ein oder mehrere Produkte aus und klicken Sie auf Trigger Price Drop. Dadurch wird das Ereignis über die Adobe-Datenschicht mithilfe von AEP-Tags gesendet, die dann die Journey initiieren und die Push-Benachrichtigung in Echtzeit bereitstellen.
