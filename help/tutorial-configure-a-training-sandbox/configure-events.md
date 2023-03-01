---
title: Ereignisse konfigurieren
description: Konfigurieren von drei Ereignissen, die für die praktischen Journey Optimizer-Herausforderungen erforderlich sind
feature: Sandboxes, Data Management, Application Settings
doc-type: tutorial
kt: 9382
role: Admin
level: Beginner
recommendations: noDisplay, noCatalog
hide: true
exl-id: c7826818-c28a-493b-8aba-9d8a8102336d
source-git-commit: 4df1bdca81a585f728aa68519aa7ec7cd0c2f014
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 10%

---

# Ereignisse konfigurieren

In diesem Abschnitt richten Sie die drei Ereignisse ein, die für die praktischen Übungen im [Journey Optimizer-Herausforderungen](/help/challenges/introduction-and-prerequisites.md).

Im folgenden Video wird erläutert, wie Ereignisse erstellt werden:

>[!VIDEO](https://video.tv.adobe.com/v/336253?quality=12)

## Online-Kaufereignis von Luma erstellen

Bei Verwendung dieses Ereignisses erhält Journey Optimizer Informationen, wenn ein Benutzer Luma-Produkte online kauft.

1. Erstellen Sie ein Ereignis mit den folgenden Parametern:

   | [!UICONTROL Parameter] | [!UICONTROL Wert] |
   |-------------|-----------|
   | [!UICONTROL NAME] | `LumaOnlinePurchase` |
   | [!UICONTROL TYP] | [!UICONTROL Einzelfall] |
   | [!UICONTROL Ereignis-ID-Typ] | [!UICONTROL Regelbasiert] |
   | [!UICONTROL Schema] | `Luma Web Events Schema` |
   | [!UICONTROL Felder] | `eventType` <br>`commerce.order.priceTotal`<br>`commerce.order.purchaseOrderNumber`<br>`commerce.shipping.adress.street1`<br>`commerce.shipping.adress.city`<br>`commerce.shipping.adress.postalCode`<br>`commerce.shipping.adress.state`<br>`productListItems.quantity`<br>`productListItems.Luma Product Catalog Schema._your Organization_ID.name`<br>`productListItems.Luma Product Catalog Schema._your Organization_IDprice`<br>`productListItems.Luma Product Catalog Schema._your Organization_ID.imageURL`<br>`productListItems.Luma Product Catalog Schema._your Organization_ID.url` |

1. Fügen Sie die [!UICONTROL Ereignis-ID-Bedingung]: `LumaOnlinePurchase.eventType is commerce.purchases`:

   1. Wählen Sie das Stiftsymbol aus, um das Feld zu bearbeiten.

   1. Im **[!UICONTROL Ereignis-ID-Bedingung hinzufügen]** modal, ziehen Sie die `eventType` auf die Arbeitsfläche.
   1. Wählen Sie `commerce.purchases` aus.
   1. Auswählen **[!UICONTROL Ok]** auf der Arbeitsfläche.
   1. Auswählen **[!UICONTROL Ok]** auf dem Modal.

   ![Ereignisbedingung hinzufügen](/help/tutorial-configure-a-training-sandbox/assets/Event-lumaOnlinePurchase-condition-1.png)

1. Auswählen [!UICONTROL NAMESPACE]: `Luma CRM ID (lumaCrmId)`

1. Wählen Sie **[!UICONTROL Speichern]** aus.

## Erstellen *[!DNL Luma Wishlist Add]* event

| [!UICONTROL Parameter] | [!UICONTROL Wert] |
|-------------|-----------|
| [!UICONTROL NAME] | `LumaWishlistAdd` |
| [!UICONTROL TYP] | [!UICONTROL Einzelfall] |
| [!UICONTROL Ereignis-ID-Typ] | [!UICONTROL Regelbasiert] |
| [!UICONTROL Schema] | `Luma Product Interactions` |
| [!UICONTROL Felder] | EventType<br>productListItem.quantity<br><b>In Produktlistenelementen > Luma-Produkte > _*[!DNL yourOrganizationID]* > Produkt:</b> <br>Name<br>Preis<br> ProductImageURL<br>ProductURL |
| [!UICONTROL Bedingung] | [!DNL LumaWishlistAdd.eventType is commerce.saveForLaters] |
| [!UICONTROL Namespace] | Email(EMail) |

## Erstellen *[!DNL Luma Product Restock]* event

| [!UICONTROL Parameter] | [!UICONTROL Wert] |
|-------------|-----------|
| [!UICONTROL NAME] | `LumaProductRestock` |
| [!UICONTROL TYP] | [!UICONTROL Business] |
| [!UICONTROL Schema] | [!DNL Luma Product Inventory Events] |
| [!UICONTROL Felder] | SKU <br> stockEventType<br><b> yourOrganizationID > product:</b> <br>name<br>price<br> ImageURL<br>description |
| [!UICONTROL Bedingung] | LumaProductRestock._`your organization's ID`.inventoryEvent.stockEventType is restock |

Herzlichen Glückwunsch! Ihre Sandbox kann jetzt verwendet werden.
