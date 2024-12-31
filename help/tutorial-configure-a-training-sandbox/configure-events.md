---
title: Konfigurieren von Ereignissen
description: Für die praktischen Journey Optimizer-Herausforderungen ist das Konfigurieren von drei Ereignissen erforderlich
feature: Sandboxes, Data Management, Application Settings
doc-type: tutorial
jira: KT-9382
role: Admin
level: Beginner
recommendations: noDisplay, noCatalog
exl-id: c7826818-c28a-493b-8aba-9d8a8102336d
source-git-commit: fd9d277be00449155c49b3809fe647d7342b6acd
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 100%

---

# Konfigurieren von Ereignissen

In diesem Abschnitt richten Sie die drei Ereignisse ein, die für die praktischen Übungen in den [Journey Optimizer-Herausforderungen](/help/challenges/introduction-and-prerequisites.md) erforderlich sind.

Im folgenden Video wird erläutert, wie Ereignisse erstellt werden:

>[!VIDEO](https://video.tv.adobe.com/v/336253?quality=12&learn=on){transcript=true}

## Erstellen des Online-Kaufereignisses von Luma

Bei Verwendung dieses Ereignisses erhält Journey Optimizer Informationen, wenn eine Person Luma-Produkte online kauft.

1. Erstellen Sie ein Ereignis mit den folgenden Parametern:

   | [!UICONTROL Parameter] | [!UICONTROL Wert] |
   |-------------|-----------|
   | [!UICONTROL NAME] | `LumaOnlinePurchase` |
   | [!UICONTROL TYP] | [!UICONTROL Unitär] |
   | [!UICONTROL Ereignis-ID-Typ] | [!UICONTROL Regelbasiert] |
   | [!UICONTROL Schema] | `Luma Web Events Schema` |
   | [!UICONTROL Felder] | `eventType` <br>`commerce.order.priceTotal`<br>`commerce.order.purchaseOrderNumber`<br>`commerce.shipping.adress.street1`<br>`commerce.shipping.adress.city`<br>`commerce.shipping.adress.postalCode`<br>`commerce.shipping.adress.state`<br>`productListItems.quantity`<br>`productListItems.Luma Product Catalog Schema._your Organization_ID.name`<br>`productListItems.Luma Product Catalog Schema._your Organization_IDprice`<br>`productListItems.Luma Product Catalog Schema._your Organization_ID.imageURL`<br>`productListItems.Luma Product Catalog Schema._your Organization_ID.url` |

1. Fügen Sie die [!UICONTROL Ereignis-ID-Bedingung] hinzu: `LumaOnlinePurchase.eventType is commerce.purchases`:

   1. Klicken Sie auf das Stiftsymbol, um das Feld zu bearbeiten.

   1. Ziehen Sie im Modal **[!UICONTROL Ereignis-ID-Bedingung hinzufügen]** den `eventType` per Drag-and-Drop auf die Arbeitsfläche.
   1. Wählen Sie `commerce.purchases` aus.
   1. Klicken Sie auf der Arbeitsfläche auf **[!UICONTROL OK]**.
   1. Klicken Sie im Modal auf **[!UICONTROL OK]**.

   ![Hinzufügen einer Ereignisbedingung](/help/tutorial-configure-a-training-sandbox/assets/Event-lumaOnlinePurchase-condition-1.png)

1. Wählen Sie [!UICONTROL NAMESPACE]: `Luma CRM ID (lumaCrmId)`

1. Wählen Sie **[!UICONTROL Speichern]** aus.

## Erstellen eines Ereignisses für *[!DNL Luma Product Restock]*

| [!UICONTROL Parameter] | [!UICONTROL Wert] |
|-------------|-----------|
| [!UICONTROL NAME] | `LumaProductRestock` |
| [!UICONTROL TYP] | [!UICONTROL Business] |
| [!UICONTROL Schema] | [!DNL Luma Product Inventory Event Schema] |
| [!UICONTROL Felder] | SKU <br> stockEventType<br><b>LumaProductCatalogSchema._yourOrganizationID.product :</b> <br>Name<br>Preis<br> ImageURL<br>Beschreibung |
| [!UICONTROL Bedingung] | LumaProductRestock._`your organization's ID`.inventoryEvent.stockEventType ist die Wiederverfügbarkeit |

Herzlichen Glückwunsch! Ihre Sandbox kann jetzt verwendet werden.
