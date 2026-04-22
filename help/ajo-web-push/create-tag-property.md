---
title: Tag-Eigenschaft erstellen
description: Die Tag-Eigenschaft sendet die Daten vom Browser über Web SDK an AEP.
feature: Push
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-01-21T00:00:00Z
jira: KT-20879
source-git-commit: 3d342c5c4de4dda221ce4427b1e4aef7ef8c22cc
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%

---

# Tag-Eigenschaft erstellen

Im zweiten Teil dieses Tutorials erfahren Sie, wie Sie Push-Benachrichtigungen in Echtzeit durch das manuelle Senden eines benutzerdefinierten price.drop-Ereignisses in Trigger setzen können. Bei diesem Ansatz wird die AEP-Datenerfassung (Tags) verwendet, um das Ereignis von der Web-Seite zu erfassen und an Adobe Experience Platform zu senden. Sobald das Ereignis aufgenommen wurde, wird eine Journey in Adobe Journey Optimizer Trigger, sodass Sie bei Bedarf Push-Benachrichtigungen auf der Grundlage von Benutzeraktionen oder Geschäftsereignissen senden können.

Diese Eigenschaft wird mit dem AEP Web SDK konfiguriert, der mit dem zuvor im Tutorial erstellten `WebPushDataStream` verbunden ist. Die Tag-Eigenschaft überwacht das `price.drop`-Ereignis in der Adobe-Datenschicht und ordnet die relevanten Produktdetails zu, indem sie das ProductListItems-Datenelement aktualisiert. Nach der Vorbereitung der Daten wird eine Regel in der Tag-Eigenschaft ausgelöst und das price.drop-Ereignis über die Web-SDK an AEP gesendet. Dieses Ereignis dient dann als Einstiegspunkt für eine Journey in Adobe Journey Optimizer und ermöglicht den sofortigen Versand von Push-Benachrichtigungen basierend auf dem Preisverfall.

## Tag-Elemente

ProductListItems zum Speichern von Produktdetails

![tag-elements](assets/product-list-items-element.png)

XDM-Variablenzuordnung zur `schemaForPushNotification`

![xdm-variable](assets/xdmvariable-data-element.png)

## Regel erstellen

Überwachen des price.drop-Ereignisses
![data-push-event](assets/tag-rule-event.png)

Aktualisieren Sie productListItems mithilfe der Variablen update .
![update-variable](assets/update-variable.png)
Senden Sie abschließend das price.drop-Ereignis mit der aktualisierten xdm-Variablen an AEP
![send-event](assets/send-event.png)

Der folgende JavaScript-Code sendet das price.drop-Ereignis von der Webseite an AEP Tags

```javascript
 <script>
      window.adobeDataLayer.push({
        event: "price.drop",
        productListItems: productListItems
      });
  </script>
```



