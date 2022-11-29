---
title: Manuelles Einrichten der Datenstruktur
description: Erstellen Sie die erforderlichen Identitäts-Namespaces und definieren Sie die Beispieldatenstruktur für Luma.
feature: Sandboxes, Data Management, Application Settings
doc-type: tutorial
kt: 9382
role: Admin
level: Beginner
recommendations: noDisplay, noCatalog
exl-id: de870229-d9a6-4051-9f76-13d402cce3b4
source-git-commit: 8a2062f0719e799dd2d039488e6bba943fb458c4
workflow-type: tm+mt
source-wordcount: '1076'
ht-degree: 8%

---

# Daten manuell einrichten

In diesem Abschnitt erstellen Sie die erforderlichen Identitäts-Namespaces und definieren die [!DNL Luma] Beispieldatenstruktur durch Erstellen der [[!UICONTROL Schemas]](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=de).

>[!TIP]
>Video-Tutorial ansehen [Zuordnungsidentitäten](/help/set-up-data/map-identities.md) bevor Sie beginnen.

## Schritt 1: Identitäts-Namespaces erstellen

In diesem Schritt erstellen Sie Identitäts-Namespaces für die [!DNL Luma] benutzerdefinierte Identitätsfelder mit `loyaltyId`, `crmId`und `lumaProduct`. Identitäts-Namespaces spielen eine entscheidende Rolle beim Erstellen von Echtzeit-Kundenprofilen, da zwei übereinstimmende Werte im selben Namespace es zwei Datenquellen ermöglichen, ein Identitätsdiagramm zu erstellen.

Erstellen Sie zunächst einen Namespace für die [!DNL Luma] Treueschema:

1. Navigieren Sie in der Benutzeroberfläche von Platform zu **[!UICONTROL Identitäten]** in der linken Navigation.

1. Auswählen **[!UICONTROL Identitäts-Namespace erstellen]**.

1. Geben Sie die folgenden Details an:

   | Anzeigename | Identitätssymbol | Typ |
   |---|---|---|
   | `Luma Loyalty ID` | `lumaLoyalty` | [!UICONTROL Geräteübergreifende ID] |

1. Wählen Sie **[!UICONTROL Erstellen]** aus.

   ![Erstellen von Namespaces](assets/createNamespace.png)

1. Erstellen Sie zwei weitere Namespaces, die die gleichen Schritte ausführen:

   | Anzeigename | Identitätssymbol | Typ |
   |---|---|---|
   | `Luma CRM ID` | `lumaCRM` | [!UICONTROL Geräteübergreifende ID] |
   | `Luma Product` | `lumaProduct` | [!UICONTROL Personenidentifizierung] |

## Schritt 2: Erstellen von Schemata

In diesem Schritt definieren Sie die Struktur der Beispieldaten, indem Sie sechs [[!UICONTROL Schemas]](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html):

* [[!DNL Luma Loyalty]](#create-luma-loyalty-schema)

* [[!DNL Luma Products]](#create-luma-products-schema)

* [[!DNL Luma Product Inventory Events]](#create-luma-product-inventory-event-schema)

* [[!DNL Luma CRM]](#create-luma-crm-and-luma-product-interactions-schemas)

* [[!DNL Luma Product Interactions]](#create-luma-crm-and-luma-product-interactions-schemas)

* [[!DNL Luma Test Profiles]](#create-luma-crm-and-luma-product-interactions-schemas)

>[!TIP]
>
>Video-Tutorial ansehen: [Schema erstellen](/help/set-up-data/create-schema.md) bevor Sie beginnen.

### Erstellen [!DNL Luma Loyalty] [!UICONTROL Schema] {#create-luma-loyalty-schema}

#### Schema erstellen

Erstellen Sie zunächst das [!DNL Luma Loyalty] schema:

1. Navigieren Sie zu **[!UICONTROL DATENVERWALTUNG]** > **[!UICONTROL Schemas]** in der linken Navigation.

1. Auswählen **[!UICONTROL Schema erstellen]** oben rechts.

1. Wählen Sie aus dem Dropdown-Menü **[!UICONTROL XDM Individual Profile]**, da Sie Attribute eines einzelnen Kunden modellieren (Punkte, Status usw.).

   ![Schema erstellen](assets/loyaltyCreateSchema.png)

#### Hinzufügen vorhandener Feldergruppen

Als Nächstes werden Sie aufgefordert, dem Schema Feldergruppen hinzuzufügen. Sie müssen alle Felder mithilfe von Gruppen zu Schemas hinzufügen. Sie fügen vorhandene Feldergruppen hinzu und müssen eine Feldergruppe erstellen.

>[!NOTE]
>
>Wenn die Variable [!UICONTROL Feldergruppen] modal wird nicht automatisch im [!UICONTROL Schemas] Seite, wählen Sie **[!UICONTROL Hinzufügen]** (wie in der folgenden Abbildung gezeigt).

![Feldergruppe hinzufügen](assets/add_field_group.png)

1. Im **[!UICONTROL Feldergruppen hinzufügen]** aktivieren Sie die folgenden Feldergruppen:

   * **[!UICONTROL Demografische Details]** für grundlegende Kundendaten wie Name und Geburtsdatum.

   * **[!UICONTROL Persönliche Kontaktangaben]** für grundlegende Kontaktdaten wie E-Mail-Adresse und Telefonnummer.

   * **[!UICONTROL Treuedetails]** für die Loyalitätsdetails wie Punkte, Zusammenführungsdatum oder Status. Die Gruppe &quot;Treuefeld&quot;befindet sich weit unten in der Liste, daher ist es am einfachsten, danach zu suchen.

1. Auswählen **[!UICONTROL Feldergruppe hinzufügen]** , um alle drei Feldergruppen zum Schema hinzuzufügen.

   ![Standardfeldgruppen auswählen](assets/addstandardFieldGroups.png)

1. Wählen Sie den obersten Knoten des Schemas aus.

1. Eingabe `Luma Loyalty` als [!UICONTROL Anzeigename].

#### Erstellen Sie eine [!UICONTROL Feldergruppe]

Um die Konsistenz der Schemas zu gewährleisten, empfiehlt Adobe, alle Systemkennungen in einer Gruppe zu verwalten:

1. Aus dem **[!UICONTROL Komposition]** Abschnitt unter [!UICONTROL Feldergruppen]auswählen **[!UICONTROL Hinzufügen]**.

1. Auswählen **[!UICONTROL Neue Feldergruppe erstellen]**.

1. Hinzufügen `Luma Identifiers` als **[!UICONTROL Anzeigename]**.

1. Hinzufügen `system identifiers for XDM Individual Profile class` als **[!UICONTROL Beschreibung]**.

1. Auswählen **[!UICONTROL Feldergruppen hinzufügen]**.

   ![Neue Feldergruppe erstellen](assets/addnewfieldgroup.png)

#### Felder zum neuen hinzufügen [!UICONTROL Feldergruppe]

Die neue leere Feldergruppe wird Ihrem Schema hinzugefügt. Mit den Schaltflächen + können Sie neue Felder an einer beliebigen Stelle in der Hierarchie hinzufügen. In diesem Fall müssen Sie Felder auf der Stammebene hinzufügen:

1. Auswählen **[!UICONTROL +]** neben dem Namen des Schemas.

   Dieser Schritt fügt ein Feld unter **Ihre Mandanten-ID** -Namespace, um Konflikte zwischen Ihren benutzerdefinierten Feldern und beliebigen Standardfeldern zu verwalten.

1. Im **[!UICONTROL Feldeigenschaften]** Fügen Sie in der Seitenleiste die Details des neuen Felds hinzu:

   * **Feldname:** `systemIdentifier`

   * **[!UICONTROL Anzeigename]:** `System Identifier`

   * **Typ:** Objekt

   * **[!UICONTROL Feldergruppe zuweisen]:** [!DNL Luma identifiers]

1. Auswählen **[!UICONTROL Anwenden]**.

   ![Systemkennung hinzufügen](assets/addsysteidentifier.png)

   Fügen Sie zwei Felder unter der `systemIdentifier` -Objekt:

   | [!UICONTROL fieldName] | [!UICONTROL Anzeigename] | [!UICONTROL Typ] |
   |-------------|-----------|----------|
   | `loyaltyId` | `Loyalty ID` | [!UICONTROL Zeichenfolge] |
   | `crmId` | `CRM Id` | [!UICONTROL Zeichenfolge] |

![fields](./assets/add_fields.png)

#### Festlegen von Identitäten

Sie verfügen nun über den Namespace und die [!DNL Luma] Treueschema konfiguriert. Bevor Sie Daten erfassen können, müssen Sie die Identitätsfelder beschriften. Jedes Schema, das mit [!UICONTROL Echtzeit-Kundenprofil] muss über eine primäre Identität verfügen und jeder aufgenommene Datensatz muss einen Wert für dieses Feld haben.

1. Legen Sie die **primary**:

   Aus dem `Luma Loyalty` schema:

   1. Wählen Sie die `Luma Identifiers` Feldergruppe.

   1. Wählen Sie die `loyaltyId` -Feld.

   1. Im **[!UICONTROL Feldeigenschaften]**, aktivieren Sie die **[!UICONTROL Identität]** ankreuzen.

   1. Aktivieren Sie die **[!UICONTROL Primäre Identität]** ankreuzen.

   1. Wählen Sie die `Luma Loyalty Id` Namespace aus **[!UICONTROL Identitäts-Namespaces]** Dropdown-Liste.

   1. Auswählen **[!UICONTROL Anwenden]**.

      ![primäre Identität](/help/tutorial-configure-a-training-sandbox/assets/primary_identity.png)

1. Legen Sie eine **sekundäre Identität**:

   Aus dem `Luma Loyalty` schema:

   1. Wählen Sie die `Luma Identifiers` Feldergruppe.

   2. Wählen Sie die `crmId` -Feld.

   3. Im **[!UICONTROL Feldeigenschaften]**, aktivieren Sie die **[!UICONTROL Identität]** ankreuzen.

   4. Wählen Sie die `Luma CRM Id` Namespace aus **[!UICONTROL Identitäts-Namespaces]** Dropdown-Liste.

   5. Auswählen **[!UICONTROL Anwenden]**.

#### Aktivieren für Profil und Speichern des Schemas

1. Wählen Sie den obersten Knoten des Schemas aus.

1. Im [!UICONTROL Feldeigenschaften] enable **[!UICONTROL Profil]**.

   Das Schema sollte wie folgt aussehen:

   ![Luma-Treueschema](assets/lumaloyaltyschema.png)

1. Wählen Sie **[!UICONTROL Speichern]** aus.

### Erstellen [!DNL Luma Products] [!UICONTROL Schema] {#create-luma-products-schema}

1. Navigieren Sie zu [!UICONTROL DATENVERWALTUNG] -> **[!UICONTROL Schemas]** in der linken Navigation.

1. Wählen Sie die **[!UICONTROL Schema erstellen]** rechts oben.

1. Wählen Sie aus dem Dropdown-Menü **[!UICONTROL Alle Schematypen durchsuchen]**, mit dem Sie eine Klasse erstellen können.

1. Wählen Sie **[!UICONTROL Neue Klasse erstellen].

1. Fügen Sie den Anzeigenamen hinzu: `Luma Products`.

1. Klasse zuweisen.

1. Erstellen Sie eine [!UICONTROL Feldergruppe]:

   * Anzeigename: `Luma Product Info`

1. Fügen Sie das folgende Feld zum [!DNL Luma] [!UICONTROL Produkt] Feldergruppe &quot;Info&quot;.

   * Feldname: `product`

   * Anzeigename: `Product`

   * Typ: [!UICONTROL Objekt]

   * Feldergruppe: [!DNL Luma Product info]

1. Auswählen **[!UICONTROL Anwenden]**.

1. Fügen Sie die folgenden Felder zum **[!DNL Product]** -Objekt:

   | [!UICONTROL fieldName] | [!UICONTROL Anzeigename] | [!UICONTROL Typ] |
   |-------------|-----------|----------|
   | `sku` | `SKU` | [!UICONTROL Zeichenfolge] |
   | `name` | `Name` | [!UICONTROL Zeichenfolge] |
   | `category` | `Category` | [!UICONTROL Zeichenfolge] |
   | `color` | `Color` | [!UICONTROL Zeichenfolge] |
   | `size` | `Size` | [!UICONTROL Zeichenfolge] |
   | `price` | `Price` | [!UICONTROL Double] |
   | `description` | `Description` | [!UICONTROL Zeichenfolge] |
   | `productImageURL` | `Product Image URL` | [!UICONTROL Zeichenfolge] |
   | `productURL` | `Product URL` | [!UICONTROL Zeichenfolge] |
   | `stockQuantity` | `Stock Quantity` | [!UICONTROL Zeichenfolge] |

1. Fügen Sie die **[!UICONTROL Anzeigename]** `Luma Products` zum Schema.

1. Wählen Sie **[!UICONTROL Speichern]** aus.

### Erstellen [!DNL Luma Product Inventory Event] [!UICONTROL Schema] {#create-luma-product-inventory-event-schema}

1. Navigieren Sie zu **[!UICONTROL DATENVERWALTUNG]** -> **[!UICONTROL Schemas]** in der linken Navigation.

1. Wählen Sie die **[!UICONTROL Schema erstellen]** rechts oben.

1. Wählen Sie aus dem Dropdown-Menü **[!UICONTROL Alle Schematypen durchsuchen]**.

1. Auswählen **[!UICONTROL Neue Klasse erstellen]**.

1. Fügen Sie den Anzeigenamen hinzu: `Business Event`.

1. Typ auswählen: *[!UICONTROL Zeitreihen]*.

1. Klasse zuweisen.

1. Erstellen Sie eine [!UICONTROL Feldergruppe]:

   * Anzeigename: `Product Inventory Event Details`

1. Fügen Sie die **[!UICONTROL Anzeigename]** `Luma Product Inventory Event Schema` zum Schema.

1. Fügen Sie der Feldergruppe &quot;Luma Product Info&quot;das folgende Feld hinzu:

   * Feldname: `inventoryEvent`

   * Anzeigename: `Inventory Event`

   * Typ: [!UICONTROL Objekt]

   * Feldergruppe: [!DNL Product Inventory Event Details]

1. Fügen Sie die folgenden Felder zum **[!DNL Product Inventory Event Details]** -Objekt:

   | [!UICONTROL fieldName] | [!UICONTROL Anzeigename] | [!UICONTROL Typ] |
   |-------------|-----------|----------|
   | `productId` | `Product ID` | [!UICONTROL Zeichenfolge] |
   | `sku` | `SKU` | [!UICONTROL Zeichenfolge] |
   | `stockEventType` | `Stock Event Type` | **[!UICONTROL Enum]** mit `restock` und `outOfStock` als Werte |

   1. , um `stockEventType` Wählen Sie für Enum den Typ aus: `string`.

   1. Scrollen Sie nach unten zum unteren Rand des **[!UICONTROL Feldeigenschaften]**.

   1. Aktivieren **[!UICONTROL Enum]**.

   1. Eingabe **[!UICONTROL values] ([!UICONTROL label)]**: `restock` (`restock`).

   1. Auswählen **[!UICONTROL Zeile hinzufügen]**.

   1. Eingabe **[!UICONTROL values] ([!UICONTROL label)]**: `outOfStock` (`out of stock`).

   1. Auswählen **[!UICONTROL Anwenden]**.

      ![enum](assets/enum.png)

1. Satz `productId` Feld als **[!UICONTROL primäre Identität]** using **[!DNL Luma Product namespace]**.

1. Wählen Sie die `sku` und definieren Sie eine Beziehung zum `product.sku` im Feld **[!DNL Luma Products]** Schema:

   1. Scrollen Sie nach unten zum unteren Rand des **[!UICONTROL Feldeigenschaften]**.

   1. Aktivieren **[!UICONTROL Beziehung]**.

      1. **[!UICONTROL Referenzschema]**: [!DNL Luma Products].

      1. **[!UICONTROL Referenz-Identitäts-Namespace]**: [!DNL Luma Product].
   1. Auswählen **[!UICONTROL Anwenden]**.

      Das Schema sollte wie folgt aussehen:

      ![SKU-Beziehung](assets/sku_relationship.png)


1. Aktivieren für **Profil**.

1. Auswählen [!UICONTROL Speichern] , um das Schema zu speichern.

### Erstellen Sie die [!DNL Luma CRM] und [!DNL Luma Product Interactions] Schemas {#create-luma-crm-and-luma-product-interactions-schemas}

Erstellen Sie die folgenden zusätzlichen [!UICONTROL Schemas]:

| [!UICONTROL Anzeigename] | [!DNL Luma CRM] | [!DNL Luma Product Interactions] | [!DNL Luma Test Profiles] |
|  ---| ------- | ---- |----|
| **[!UICONTROL Typ]** | [!UICONTROL XDM Individual Profile] | [!UICONTROL XDM-Erlebnisereignis] | [!UICONTROL XDM Individual Profile] |
| **[!UICONTROL Vorhandene Feldergruppe hinzufügen]** | Luma-Kennungen<br>Demografische Details<br>Persönliche Kontaktangaben | Identitätszuordnung<br>Commerce-Details | Luma-Kennungen<br>Demografische Details<br>Persönliche Kontaktangaben<br>Profiltestdetails |
| **[!UICONTROL Beziehung]** |  | *[!DNL productListItems.SKU]*:<br> Referenzschema *[!DNL Luma Products]* <br>[!DNL Reference identity namespace] *[!DNL Luma Product]* schema |
| **[!UICONTROL Primäre Identität] [!UICONTROL namespace])** | systemIdentifier.crmId<br>(Luma CRM ID) |  | personalEmail.address<br>(Email) |
| **[!UICONTROL Sekundäre Identität] [!UICONTROL namespace]** | personalEmail.address (Email)<br>mobilePhone.number (Phone) |  |
| **[!UICONTROL Profil aktivieren]** | ja | ja | ja |

## Nächste Schritte

Nachdem Sie die Datenstruktur erstellt haben, haben Sie [Erstellen von Datensätzen und Erfassen von Beispieldaten](/help/tutorial-configure-a-training-sandbox/manual-data-ingestion.md).
