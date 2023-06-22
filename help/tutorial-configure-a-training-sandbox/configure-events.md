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
source-git-commit: 81f5cc22d46f89ee1c7164a92988311ca6036b8b
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 100%

---

# Konfigurieren von Ereignissen

In diesem Abschnitt richten Sie die drei Ereignisse ein, die für die praktischen Übungen in den [Journey Optimizer-Herausforderungen](/help/challenges/introduction-and-prerequisites.md) erforderlich sind.

Im folgenden Video wird erläutert, wie Ereignisse erstellt werden:

>[!VIDEO](https://video.tv.adobe.com/v/336253?quality=12&learn=on)

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

## Erstellen eines Ereignisses für *[!DNL Luma Wishlist Add]*

| [!UICONTROL Parameter] | [!UICONTROL Wert] |
|-------------|-----------|
| [!UICONTROL NAME] | `LumaWishlistAdd` |
| [!UICONTROL TYP] | [!UICONTROL Unitär] |
| [!UICONTROL Ereignis-ID-Typ] | [!UICONTROL Regelbasiert] |
| [!UICONTROL Schema] | `Luma Product Interactions` |
| [!UICONTROL Felder] | EventType<br>productListItem.quantity<br><b>In Produktlistenelementen > Luma-Produkte > _*[!DNL yourOrganizationID]* > Produkt:</b> <br>Name<br>Preis<br> ProductImageURL<br>ProductURL |
| [!UICONTROL Bedingung] | [!DNL LumaWishlistAdd.eventType is commerce.saveForLaters] |
| [!UICONTROL Namespace] | Email(EMail) |

## Erstellen eines Ereignisses für *[!DNL Luma Product Restock]*

| [!UICONTROL Parameter] | [!UICONTROL Wert] |
|-------------|-----------|
| [!UICONTROL NAME] | `LumaProductRestock` |
| [!UICONTROL TYP] | [!UICONTROL Business] |
| [!UICONTROL Schema] | [!DNL Luma Product Inventory Events] |
| [!UICONTROL Felder] | SKU <br> stockEventType<br><b> yourOrganizationID > Produkt:</b> <br>Name<br>Preis<br> ImageURL<br>Beschreibung |
| [!UICONTROL Bedingung] | LumaProductRestock._`your organization's ID`.inventoryEvent.stockEventType ist die Wiederverfügbarkeit |

Herzlichen Glückwunsch! Ihre Sandbox kann jetzt verwendet werden.
