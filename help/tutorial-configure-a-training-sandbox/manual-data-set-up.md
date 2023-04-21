---
title: Manuelles Einrichten der Datenstruktur
description: Erstellen Sie die erforderlichen Identity-Namespaces und definieren Sie die Beispieldatenstruktur für Luma.
feature: Sandboxes, Data Management, Application Settings
doc-type: tutorial
kt: 9382
role: Admin
level: Beginner
recommendations: noDisplay, noCatalog
exl-id: de870229-d9a6-4051-9f76-13d402cce3b4
source-git-commit: b91d6ccdb54213873b91b7ffa9d95d7cb5261ee8
workflow-type: ht
source-wordcount: '1021'
ht-degree: 100%

---

# Manuelles Einrichten der Daten

In diesem Abschnitt erstellen Sie die erforderlichen Identity-Namespaces und definieren die [!DNL Luma]-Beispieldatenstruktur durch Erstellen der [[!UICONTROL Schemata]](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=de).

>[!TIP]
>Sehen Sie sich das Video-Tutorial [Zuordnen von Identitäten](/help/set-up-data/map-identities.md) an, bevor Sie beginnen.

## Schritt 1: Identity-Namespaces erstellen

In diesem Schritt erstellen Sie Identity-Namespaces für die benutzerdefinierten Identitätsfelder von [!DNL Luma] mit Namen `lumaLoyaltyId`, `lumaCrmId` und `lumaProductSKU`. Identity-Namespaces spielen eine entscheidende Rolle beim Erstellen von Echtzeit-Kundenprofilen, da zwei übereinstimmende Werte im selben Namespace es zwei Datenquellen ermöglichen, ein Identitätsdiagramm zu erstellen.

Erstellen Sie zunächst einen [!UICONTROL Namespace] für das [!DNL Luma Loyalty ID]-Schema:

1. Navigieren Sie dazu in der Journey Optimizer-Benutzeroberfläche zu **[!UICONTROL Kunde]** > **[!UICONTROL Identitäten]** im linken Navigationsbereich.

1. Wählen Sie **[!UICONTROL Identity-Namespace erstellen]** aus.

1. Geben Sie die folgenden Details an:

   | Anzeigename | Identitätssymbol | Typ |
   |---|---|---|
   | `Luma Loyalty ID` | `lumaLoyaltyId` | [!UICONTROL Geräteübergreifende ID] |

1. Wählen Sie **[!UICONTROL Erstellen]** aus.

   ![Erstellen von Namespaces](assets/createNamespace.png)

1. Erstellen Sie mit den gleichen Schritten zwei weitere Namespaces:

   | Anzeigename | Identitätssymbol | Typ |
   |---|---|---|
   | `Luma CRM ID` | `lumaCrmId` | [!UICONTROL Geräteübergreifende ID] |
   | `Luma Product SKU` | `lumaProductSKU` | [!UICONTROL Nichtpersonenkennung] |

## Schritt 2: Schemata erstellen

In diesem Schritt definieren Sie die Struktur der Beispieldaten, indem Sie sechs [[!UICONTROL Schemata]](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=de) erstellen:

* [[!DNL Luma Loyalty Schema]](#create-luma-loyalty-schema)

* [[!DNL Luma Product Catalog Schema]](#create-luma-product-catalog-schema)

* [[!DNL Luma Product Inventory Events]-Schema](#create-luma-product-inventory-event-schema)

* [[!DNL Luma CRM Schema]](#create-luma-crm-and-luma-product-interactions-schemas)

* [[!DNL Luma Web Events Schema]](#create-luma-crm-and-luma-product-interactions-schemas)

* [[!DNL Luma Offline Purchase Events Schema]](#create-additional-schemas)

* [[!DNL Luma Test Profiles Schema]](#create-additional-schemas)

>[!TIP]
>
>Sehen Sie sich das Video-Tutorial [Erstellen eines Schemas](/help/set-up-data/create-schema.md) an, bevor Sie beginnen.

### Erstellen von [!DNL Luma Loyalty Schema] {#create-luma-loyalty-schema}

In diesem Abschnitt wird beschrieben, wie Sie das [!DNL Luma Loyalty]-Schema erstellen und die Feldergruppen konfigurieren.

#### Erstellen des Schemas

1. Gehen Sie zu **[!UICONTROL DATEN-MANAGEMENT]** > **[!UICONTROL Schemata]** im linken Navigationsbereich.

1. Klicken Sie auf **[!UICONTROL Schema erstellen]** oben rechts.

1. Wählen Sie aus dem Dropdown-Menü **[!UICONTROL Individuelles XDM-Profil]** aus.

   Sie wählen diese Option aus, da Sie Attribute eines einzelnen Kunden modellieren (Punkte, Status usw.).

#### Hinzufügen weiterer Feldergruppen

Als Nächstes werden Sie aufgefordert, dem Schema mithilfe von Gruppen Feldergruppen hinzuzufügen. Sie müssen vorhandene Feldergruppen hinzufügen und eine Feldergruppe erstellen.

1. Wähen Sie auf der Seite [!UICONTROL Schema], wenn das Modal „Feldergruppen“ nicht automatisch geöffnet wurde, **[!UICONTROL Hinzufügen]** aus.

   ![Hinzufügen einer Feldergruppe](assets/add_field_group.png)

1. Aktivieren Sie auf der Seite **[!UICONTROL Feldergruppen hinzufügen]** die folgenden Feldergruppen:

   * **[!UICONTROL Demografische Details]** für grundlegende Kundendaten wie Name und Geburtsdatum.

   * **[!UICONTROL Persönliche Kontaktangaben]** für grundlegende Kontaktdaten wie E-Mail-Adresse und Telefonnummer.

   * **[!UICONTROL Treuedetails]** für die Treuedetails wie Punkte, Beitrittsdatum oder Status. Die Feldergruppe für die Treuedetails befindet sich weit unten in der Liste, daher ist es am einfachsten, danach zu suchen.

1. Wählen Sie **[!UICONTROL Feldergruppe hinzufügen]** aus, um alle drei Feldergruppen zum Schema hinzuzufügen.

   ![Auswahl der Standardfeldergruppen](assets/addstandardFieldGroups.png)

1. Wählen Sie den obersten Knoten des Schemas aus.

1. Geben Sie `Luma Loyalty Schema` als den **[!UICONTROL Anzeigenamen]** ein.

#### Erstellen einer [!UICONTROL Feldergruppe] {#create-field-group}

Um dafür zu sorgen, dass das Schemata durchgehend einheitlich ist, empfiehlt Adobe, alle Systemkennungen in einer einzigen Gruppe zu verwalten:

1. Wählen Sie im Abschnitt **[!UICONTROL Komposition]** unter [!UICONTROL Feldergruppen] die Option **[!UICONTROL Hinzufügen]** aus.

1. Wählen Sie **[!UICONTROL Neue Feldergruppe erstellen]** aus.

1. Fügen Sie `Luma Identity Profile Field Group` als den **[!UICONTROL Anzeigenamen]** hinzu.

1. Fügen Sie `system identifiers for XDM Individual Profile class` als die **[!UICONTROL Beschreibung]** hinzu.

1. Wählen Sie **[!UICONTROL Feldergruppen hinzufügen]** aus.

   ![Erstellen einer neuen Feldergruppe](assets/addnewfieldgroup.png)

#### Hinzufügen von Feldern zur neuen [!UICONTROL Feldergruppe]

Die neue, leere Feldergruppe wird Ihrem Schema hinzugefügt. Mit den Schaltflächen „+“ können Sie neue Felder an einer beliebigen Stelle in der Hierarchie hinzufügen. In diesem Fall müssen Sie Felder auf der Stammebene hinzufügen:

1. Klicken Sie auf **[!UICONTROL +]** neben dem Namen des Schemas.

   Dieser Schritt fügt ein Feld unter dem Namespace **Ihre Mandanten-ID** hinzu, um Konflikte zwischen Ihren benutzerdefinierten Feldern und Standardfeldern zu handhaben.

1. Fügen Sie in der Seitenleiste **[!UICONTROL Feldeigenschaften]** die Details des neuen Felds hinzu:

   * **Feldname:** `systemIdentifier`

   * **[!UICONTROL Anzeigename]:** `System Identifier`

   * **Typ:** Objekt

   * **[!UICONTROL Feldergruppe zuweisen]:** [!DNL Luma identifiers]

1. Wählen Sie **[!UICONTROL Anwenden]** aus.

   ![Hinzufügen einer Systemkennung](assets/addsysteidentifier.png)

   Fügen Sie zwei Felder unter dem `systemIdentifier`-Objekt hinzu:

   | [!UICONTROL Feldname] | [!UICONTROL Anzeigename] | [!UICONTROL Typ] |
   |-------------|-----------|----------|
   | `loyaltyId` | `Loyalty Id` | [!UICONTROL String] |
   | `crmId` | `CRM Id` | [!UICONTROL String] |

![Felder](./assets/add_fields.png)

#### Festlegen von Identitäten

Sie haben jetzt den [!UICONTROL Namespace] und das [!DNL Luma Loyalty schema] konfiguriert. Bevor Sie Daten aufnehmen können, müssen Sie die Identitätsfelder beschriften. Jedes Schema, das mit [!UICONTROL Echtzeit-Kundenprofil] verwendet wird, muss über eine primäre Identität verfügen und jeder aufgenommene Datensatz muss einen Wert für dieses Feld haben.

1. Legen Sie die **primäre Identität** fest:

   Aus dem **[!DNL Luma Loyalty Schema]**:

   1. Wählen Sie die **[!DNL Luma Identity Profile Field Group]**.

   2. Wählen Sie das Feld **[!DNL loyaltyId]** aus.

   3. Aktivieren Sie in den **[!UICONTROL Feldeigenschaften]** das Kästchen **[!UICONTROL Identität]**.

   4. Aktivieren Sie das Kästchen **[!UICONTROL Primäre Identität]**.

   5. Wählen Sie aus dem Dropdown-Menü **[!UICONTROL Identity-Namespaces]** den `Luma Loyalty Id`-Namespace aus.

   6. Wählen Sie **[!UICONTROL Anwenden]** aus.

      ![Primäre Identität](/help/tutorial-configure-a-training-sandbox/assets/primary_identity.png)

2. Legen Sie eine **sekundäre Identität** fest:

   Aus dem **[!DNL Luma Loyalty Schema]**:

   1. Wählen Sie die **[!DNL Luma Identity Profile Field Group]**.

   2. Wählen Sie das Feld `crmId` aus.

   3. Aktivieren Sie in den **[!UICONTROL Feldeigenschaften]** das Kästchen **[!UICONTROL Identität]**.

   4. Wählen Sie den `Luma CRM Id`-Namespace aus der Dropdown-Liste **[!UICONTROL Identity-Namespaces]** aus.

   5. Wählen Sie **[!UICONTROL Anwenden]** aus.

#### Aktivieren für das Profil und Speichern des Schemas

1. Wählen Sie den obersten Knoten des Schemas aus.

1. Aktivieren Sie in den [!UICONTROL Feldeigenschaften] die Option **[!UICONTROL Profil]**.

   Das Schema sollte wie folgt aussehen:

   ![Luma-Treueschema](assets/lumaloyaltyschema.png)

1. Wählen Sie **[!UICONTROL Speichern]** aus.

### Erstellen von [!DNL Luma Product Catalog Schema] {#create-luma-product-catalog-schema}

1. Gehen Sie zu **[!UICONTROL DATEN-MANAGEMENT]** > **[!UICONTROL Schemata]** im linken Navigationsbereich.

1. Wählen Sie **[!UICONTROL Schema erstellen]** aus (oben rechts).

1. Um eine Klasse zu erstellen, wählen Sie **[!UICONTROL Alle Schematypen durchsuchen]** aus dem Dropdown-Menü aus.

1. Wählen Sie **[!UICONTROL Neue Klasse erstellen]** aus.

1. Fügen Sie den Anzeigenamen hinzu: `Luma Product Catalog Class`.

1. Weisen Sie die Klasse zu.

1. Erstellen Sie eine [!UICONTROL Feldergruppe]:

   * Anzeigename: `Luma Product Catalog Field Group`

1. Fügen Sie das folgende Feld zur **[!DNL Luma Product Catalog Field Group]** hinzu.

   * Feldname: `product`

   * Anzeigename: `Product`

   * Typ: [!UICONTROL Objekt]

   * Feldergruppe: [!DNL Luma Product Catalog Field Group]

1. Wählen Sie **[!UICONTROL Anwenden]** aus.

1. Fügen Sie die folgenden Felder zum **[!DNL Product]**-Objekt hinzu:

   | [!UICONTROL Feldname] | [!UICONTROL Anzeigename] | [!UICONTROL Typ] |
   |-------------|-----------|----------|
   | `sku` | `Product SKU` | [!UICONTROL String] |
   | `name` | `Product Name` | [!UICONTROL String] |
   | `category` | `Product Category` | [!UICONTROL String] |
   | `color` | `Product Color` | [!UICONTROL String] |
   | `size` | `Product Size` | [!UICONTROL String] |
   | `price` | `Product Price` | [!UICONTROL Double] |
   | `description` | `Product Description` | [!UICONTROL String] |
   | `imageUrl` | `Product Image URL` | [!UICONTROL String] |
   | `stockQuantity` | `Product Stock Quantity` | [!UICONTROL String] |
   | `url` | `Product URL` | [!UICONTROL String] |

1. Legen Sie die **[!DNL SKU]** als primäre Identität fest.
1. Fügen Sie den **[!UICONTROL Anzeigenamen]** `Luma Product Catalog Field Group` zur [!UICONTROL Feldergruppe] hinzu.

1. Wählen Sie **[!UICONTROL Speichern]** aus.

### Erstellen von [!DNL Luma Product Inventory Event Schema] {#create-luma-product-inventory-event-schema}

1. Gehen Sie zu **[!UICONTROL DATEN-MANAGEMENT]** > **[!UICONTROL Schemata]** im linken Navigationsbereich.

1. Klicken Sie auf **[!UICONTROL Schema erstellen]** oben rechts.

1. Wählen Sie aus dem Dropdown-Menü **[!UICONTROL Alle Schematypen durchsuchen]** aus.

1. Wählen Sie **[!UICONTROL Neue Klasse erstellen]** aus.

1. Fügen Sie den Anzeigenamen hinzu: `Luma Business Event Class`.

1. Wählen Sie den Typ aus: *[!UICONTROL Zeitreihe]*.

1. Weisen Sie die Klasse zu.

1. Erstellen Sie eine [!UICONTROL Feldergruppe]:

   * Anzeigename: `Luma Product Inventory Event Details Field Group`

1. Fügen Sie den **[!UICONTROL Anzeigenamen]** `Luma Product Inventory Event Schema` zum Schema hinzu.

1. Fügen Sie das folgende Feld zur **[!DNL Luma Product Inventory Event Details Field Group]** hinzu: 

   * Feldname: `inventoryEvent`

   * Anzeigename: `Inventory Event`

   * Typ: [!UICONTROL Objekt]

   * Feldergruppe: `Luma Product Inventory Event Details Field Group`

1. Fügen Sie die folgenden Felder zum `Product Inventory Event Details`-Objekt hinzu:

   | [!UICONTROL Feldname] | [!UICONTROL Anzeigename] | [!UICONTROL Typ] |
   |-------------|-----------|----------|
   | `sku` | `SKU` | [!UICONTROL String] |
   | `stockEventType` | `Stock Event Type` | [!UICONTROL String] |

   1. Um den `stockEventType` auf „Aufzählung“ festzulegen, wählen Sie den Typ `string` aus.

   2. Scrollen Sie nach unten zum unteren Rand der **[!UICONTROL Feldeigenschaften]**.

   3. Aktivieren Sie **[!UICONTROL Aufzählung]**.

   4. Geben Sie **[!UICONTROL Werte] ([!UICONTROL Beschriftung)]** ein: `restock` (`Restock`).

   5. Klicken Sie auf **[!UICONTROL Zeile hinzufügen]**.

   6. Geben Sie **[!UICONTROL Werte] ([!UICONTROL Beschriftung)]** ein: `outOfStock` (`Out of Stock`).

   7. Wählen Sie **[!UICONTROL Anwenden]** aus.

      ![Aufzählung](assets/enum.png)

1. Legen Sie das Feld `inventory.Event.sku` mithilfe des **[!DNL LumaProductSKU namespace]** als **[!UICONTROL primäre Identität]** fest.

1. Wählen Sie das Feld `sku` aus und definieren Sie eine Beziehung zum Feld `product.sku` im Schema **[!DNL Luma Product catalog Schema]**:

   1. Scrollen Sie nach unten zum unteren Rand der **[!UICONTROL Feldeigenschaften]**.

   2. Aktivieren Sie **[!UICONTROL Beziehung]**.

      1. **[!UICONTROL Referenzschema]**: [!DNL Luma Product Catalog Schema].

      2. **[!UICONTROL Referenz-Identity-Namespace]**: [!DNL LumaProductSKU].
   3. Wählen Sie **[!UICONTROL Anwenden]** aus.

      Das Schema sollte wie folgt aussehen:

      ![SKU-Beziehung](assets/sku_relationship.png)


1. Aktivieren Sie es für das **Profil**.

1. Klicken Sie auf [!UICONTROL Speichern], um das Schema zu speichern.

### Erstellen zusätzlicher Schemata {#create-additional-schemas}

Erstellen Sie die folgenden zusätzlichen [!UICONTROL Schemata]:

| [!UICONTROL Anzeigename] | [!DNL Luma CRM Schema] | [!DNL Luma Web Events Schema] | [!DNL Luma Test Profiles schema] | [!DNL Luma Offline Purchase Events Schema] |
|  ---| ------- | ---- |----|----|
| **[!UICONTROL Klasse]** | [!UICONTROL Individuelles XDM-Profil] | [!UICONTROL XDM-Erlebnisereignis] | [!UICONTROL Individuelles XDM-Profil] | [IUICONTROL XDM ExperienceEvent] |
| **[!UICONTROL Hinzufügen einer bestehenden Feldergruppe]** | `Luma Identity Profile Field Group`<br>`Demographic Details`<br>`Personal Contact Details` | `Orchestration eventID`<br>`Consumer Experience Event`<br>`AEP Web SDK ExperienceEvent` | `Luma Identity Profile Field Group`<br>`Demographic Details`<br>`Personal Contact Details`<br>`Profile test details` | `Luma Identity Profile Field Group` <br>`Commerce Details` |
| **[!UICONTROL Beziehung]** |  | `productListItems.SKU`:<br> Referenzschema `Luma Product Catalog Schema` <br>[!DNL Reference identity namespace] `lumaProductSKU` |  | `productListItems.SKU`:<br> Referenzschema `Luma Product Catalog Schema` <br>[!DNL Reference identity namespace] `lumaProductSKU` |
| **[!UICONTROL Primäre Identität] [!UICONTROL Namespace])** | `systemIdentifier.crmId` |  | `systemIdentifier.crmId` | `systemIdentifier.LoyaltyId` |
| **[!UICONTROL Für Profil aktivieren]** | ja | ja | ja | ja |

## Nächste Schritte

Jetzt, da Sie die Datenstruktur erstellt haben, können Sie [Datensätze erstellen und Beispieldaten aufnehmen](/help/tutorial-configure-a-training-sandbox/manual-data-ingestion.md).
