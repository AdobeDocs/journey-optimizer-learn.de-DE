---
title: Erstellen einer E-Mail zur Auftragsbestätigung
description: Testen Sie Ihr Wissen über das Erstellen und Personalisieren von Transaktionsnachrichten.
kt: 7531
feature: Journeys
role: User
level: Beginner
hide: true
exl-id: ec86e2ac-081d-47aa-a948-007107baa2b4
source-git-commit: e377ddb8b84dccd503274caf9ffa3d4c73eedc28
workflow-type: tm+mt
source-wordcount: '653'
ht-degree: 50%

---


# Erstellen einer E-Mail zur Auftragsbestätigung

![Bestellungsbestätigung](/help/challenges/assets/email-assets/luma-transactional-order-confirmation.png)

| Challenge | Erstellen einer Transaktions-E-Mail zur Bestellbestätigung |
|---|---|
| Persona | Journey-Manager |
| Erforderliche Fähigkeiten | <ul><li>[Erstellen von E-Mail-Inhalten mit dem Nachrichten-Editor](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/email-channel/create-content-with-the-email-designer.html?lang=en)</li> <li>[Verwenden von kontextuellen Ereignisinformationen für die Personalisierung](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/personalize-content/use-contextual-event-information-for-personalization.html?lang=de)</li><li>[Verwenden von Helper-Funktionen für die Personalisierung](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/personalize-content/use-helper-functions-for-personalization.html?lang=de)</li></ul> |
| Herunterzuladende Assets | [Bestellbestätigungs-Assets](/help/challenges/assets/email-assets/order-confirmation-assets.zip) |

## Die Story

Luma startet seinen Online-Store und möchte ein gutes Kundenerlebnis sicherstellen, indem eine Bestätigungs-E-Mail für die Bestellung gesendet wird, sobald ein Kunde eine Bestellung aufgegeben hat.



## Ihre Challenge

Erstellen Sie eine Journey, die eine Bestätigungs-E-Mail sendet, wenn ein Luma-Kunde eine Online-Bestellung abschließt.

>[!BEGINTABS]

>[!TAB Aufgabe]

1. Erstellen Sie eine Journey namens `Luma - Order Confirmation`
2. Verwenden Sie das Ereignis: `LumaOnlinePurchase`
3. Erstellen Sie eine **transactional**  E-Mail namens `Luma - Order Confirmation`
* Betreffzeile &quot;Vielen Dank für Ihren Kauf, `FirstName`&quot;
* Verwenden Sie die Vorlage `Luma - Order summary` und ändern Sie sie:
   * Entfernen Sie die `You may also like` Abschnitte
   * Fügen Sie den Abmelde-Link am Ende der E-Mail hinzu.

Die E-Mail sollte wie folgt strukturiert sein:
<table>
<tr>
<td>
  <div>
     <strong> Kopfzeilenabschnitt</strong>
      </div>
  </td>
  <td>
      <p>
     <li>luma_logo.png</li>
    <li>Es sollte einen Link zur Luma-Website enthalten: https://luma.enablementadobe.com/content/luma/us/en.html</li>
    <p>
    </td>
  </tr>
  <tr>
  <td>
  <div>
    <strong>Abschnitt zur Bestellbestätigung
 </strong>
  </td>
  <td>
    <p>
    <strong>Text</strong><p>
    <em>He {firstName},</em><p>
   <div>
    <p>
     <em>Ihre Bestellung wurde aufgegeben.
    <p>Sobald Ihr Paket ausgeliefert wird, senden wir Ihnen eine E-Mail mit einer Tracking-Nummer, damit Sie Ihre Bestellung verfolgen können.</p></em>
    </strong>
    </tr>
  </td>
 <td>
  <div>
     <strong> Abschnitt „Versand an“</strong>
      </div>
      <p>
      <li>Vorname und Nachname stammen aus dem Profil
      <li>Ersetzen Sie die hartcodierte Adresse in der Vorlage durch die <b>Lieferadresse</b>
      <li>Die Adressdetails sind kontextbezogene Attribute der Veranstaltung (Straße 1, Stadt, Postleitzahl, Bundesland)
      <li> Entfernen <i>Rabatt, gesamt, Ankunft</i></p>
  </td>
  <td>
  <p> Versand an:</p>
      <em>{firstName} {lastName}<br>
     {Street 1}<br>
     {City}, {State} {postalCode}<br></em></p>
  </td>
 <tr>
<td>
  <div>
     <strong>Bestelldetailabschnitt</strong>
      </div>
       <p><li>Fügen Sie diesen Abschnitt unterhalb der <b>Versand an</b> Abschnitt.
      </p><br>
      <p><b>Tipps:</b>
      <li>Strukturkomponente verwenden <b>1:2 Spalte links</b> für diesen Abschnitt
      <li>Dies sind kontextuelle Ereignisinformationen.
      <li>Verwenden Sie die [!UICONTROL helper function]: [!UICONTROL Each]
      <li>Wechseln Sie zum Format des Code-Editors, um die kontextuellen Daten hinzuzufügen.
  </td>
  <td>
    <strong>Kopfzeile</strong>
    <p>
  Reihenfolge: <em>{purchaseOrderNumber}</em>
    </p>
    <strong>Liste der bestellten Produkte:
 </strong>
  <p>Führen Sie jedes Produkt in der Bestellung mit einem Bild, dem Preis und dem Namen auf.
  <p>Das Layout der einzelnen Elemente sollte wie folgt aussehen:
   <img alt="Reihenfolge" src="./assets/c2-order.png"> 
<p><b>Link zum Warenkorb hinzufügen</b>
<p>Ersetzen Sie die Bestell-ID in der URL durch die Bestellnummer:
   <i>https://luma.enablementadobe.com/content/luma/us/en/user/account/order-history/order-details.html?orderId=90845952-c2ea-4872-8466-5289183e4607</i>
</td>
  </tr>
</table>


>[!TIP]
>
>Damit Sie eine Fehlerbehebung bei Ihren Journey vornehmen können, sollten Sie allen Nachrichtenaktionen einen alternativen Pfad hinzufügen, wenn eine Zeitüberschreitung oder ein Fehler auftritt.

>[!TAB Erfolgskriterien]

Trigger der Journey, die Sie im Testmodus erstellt haben, und senden Sie die E-Mail an sich:

1. Bevor Sie in den Testmodus wechseln, überschreiben Sie die E-Mail-Parameter, die an die Test-E-Mail-Adresse gesendet werden sollen:
   1. Öffnen Sie die E-Mail-Detailansicht.
   2. Klicken Sie im Abschnitt E-Mail-Parameter auf das T-Symbol (Parameter überschreiben aktivieren).
   3. Klicken Sie in das Adressfeld
   4. Fügen Sie im nächsten Bildschirm Ihre E-Mail-Adresse in Klammern ein: *&quot;yourname@yourdomain&quot;* im Ausdruckseditor und klicken Sie auf &quot;OK&quot;.
2. Setzen Sie die Journey in den Testmodus
3. Lösen Sie das Ereignis mit den folgenden Parametern aus:
   * Setzen Sie die Profilkennung auf: Identitätswert:`a8f14eab3b483c2b96171b575ecd90b1`
   * Ereignistyp: commerce.purchases
   * `Quantity`: 1
   * `Price Total:` 69
   * `Purchase Order Number:` 90845952-c2ea-4872-8466-5289183e4607
   * `SKU:` LLMH09
   * `City:`San Jose
   * `Postal Code:` 95119
   * `State`: CA
   * `Street:` 245 Park Avenue

Sie sollten die personalisierte Kaufbestätigungs-E-Mail erhalten.

* Die Betreffzeile sollte den Vornamen des Testprofils enthalten: Leora

* So sollte Ihr E-Mail-Textkörper aussehen:

![E-Mail](/help/challenges/assets/c2-email.png)

>[!TAB Überprüfen Sie Ihre Arbeit]

**Journey**

![Journey](/help/challenges/assets/c2-journey.png)


**E-Mail**

**Betreffzeile:**

Vielen Dank für Ihren Einkauf. {{ profile.person.name.firstName }}!

**Abschnitt „Versand an“:**

So sollte Ihr Code aussehen:

```javascript
{{ profile.person.name.firstName }} {{ profile.person.name.lastName }}
{{context.journey.events.454181416.commerce.shipping.address.street1}}
{{context.journey.events.454181416.commerce.shipping.address.city}}, {{context.journey.events.454181416.commerce.shipping.address.state}} {{context.journey.events.454181416.commerce.shipping.address.postalCode}}
```

*event.45481416* ist eine andere Nummer für Sie.

TIPP: Personalisieren Sie jede Zeile separat

**Bestelldetailabschnitt:**

So sollte Ihr Code aussehen:

Kopfzeile:

```javascript
Order #: {{context.journey.events.1627840522.commerce.order.purchaseOrderNumber}}
```

**Produktliste:**

Verwenden Sie zum Erstellen der Liste von Produkten die Helper-Funktion „each“. Zeigen Sie diese in einer Tabelle an. So sollte Ihr Code aussehen (mit Ihren spezifischen Variablen wie Ihrer Ereignis-ID - anstatt `454181416` und Ihre -Organisation anstelle von `techmarketingdemos` ):

```javascript
{{#each context.journey.events.454181416.productListItems as |product|}}<tr> <th class="colspan33"><div class="acr-fragment acr-component image-container" data-component-id="image" style="width:100%;text-align:center;" contenteditable="false"><!--[if mso]><table cellpadding="0" cellspacing="0" border="0" width="100%"><tr><td style="text-align: center;" ><![endif]--><img src="{{context.journey.events.454181416.productListItems.VYG__902489191a0a40e67f51f17f3ea9e2dfaf2dea3bd0bebe8b._techmarketingdemos.product.imageUrl}}" style="height:auto;width:100%;" height="233" width="233"><!--[if mso]></td></tr></table><![endif]--></div></th> <th class="colspan66"><div class="acr-fragment acr-component" data-component-id="text" contenteditable="false"><div class="text-container" contenteditable="true"><p><span style="font-weight:700;">{{context.journey.events.454181416.productListItems.VYG__902489191a0a40e67f51f17f3ea9e2dfaf2dea3bd0bebe8b._techmarketingdemos.product.name}}</span></p></div></div><div class="acr-fragment acr-component" data-component-id="text" contenteditable="false"><div class="text-container" contenteditable="true"><p>${{context.journey.events.454181416.productListItems.VYG__902489191a0a40e67f51f17f3ea9e2dfaf2dea3bd0bebe8b._techmarketingdemos.product.price}}.00</p></div></div></th></tr> {{/each}}
```

**Schaltfläche &quot;Bestellung anzeigen&quot;:**

`https://luma.enablementadobe.com/content/luma/us/en/user/account/order-history/order-details.html?orderId={{context.journey.events.454181416.commerce.order.purchaseOrderNumber}}`

**Gesamtpreis:**

Gesamt:`${{context.journey.events.1627840522.commerce.order.priceTotal}}.00`


>[!ENDTABS]