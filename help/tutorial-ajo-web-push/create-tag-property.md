---
title: Tag-Eigenschaft erstellen
description: Die Tag-Eigenschaft sendet die Daten vom Browser über Web SDK an AEP.
feature: Push
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-01-21T00:00:00.000Z
jira: KT-20879
exl-id: 108de002-f033-4b88-bee5-2b50463c345c
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
source-wordcount: '250'
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
