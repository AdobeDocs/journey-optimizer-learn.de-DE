---
title: Erstellen einer E-Mail zur Auftragsbestätigung
description: Testen Sie Ihr Wissen über das Erstellen und Personalisieren von Transaktionsnachrichten.
kt: 7531
feature: Journeys
role: User
level: Beginner
hide: true
exl-id: ec86e2ac-081d-47aa-a948-007107baa2b4
source-git-commit: 70815c3cd30de22aad7ec667b8baf9b4c8642491
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 82%

---


# Erstellen einer E-Mail zur Auftragsbestätigung

![Bestellungsbestätigung](/help/challenges/assets/email-assets/luma-transactional-order-confirmation.png)

| Challenge | Erstellen einer Transaktions-E-Mail zur Bestellbestätigung |
|---|---|
| Persona | Journey-Manager |
| Erforderliche Fähigkeiten | <ul><li>[Erstellen von E-Mail-Inhalten mit dem Nachrichten-Editor](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-messages/create-email-content-with-the-message-editor.html?lang=de)</li> <li>[Verwenden von kontextuellen Ereignisinformationen für die Personalisierung](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/personalize-content/use-contextual-event-information-for-personalization.html?lang=de)</li><li>[Verwenden von Helper-Funktionen für die Personalisierung](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/personalize-content/use-helper-functions-for-personalization.html?lang=de)</li></ul> |
| Herunterzuladende Assets | [Bestellbestätigungs-Assets](/help/challenges/assets/email-assets/order-confirmation-assets.zip) |

## Die Story

Luma startet seinen Online-Store und möchte ein gutes Kundenerlebnis sicherstellen, indem eine Bestätigungs-E-Mail für die Bestellung gesendet wird, sobald ein Kunde eine Bestellung aufgegeben hat.



## Ihre Challenge

Erstellen Sie eine Journey, die eine Bestätigungs-E-Mail sendet, wenn ein Luma-Kunde eine Online-Bestellung abschließt.

>[!BEGINTABS]

>[!TAB Aufgabe]

1. Erstellen Sie eine Journey namens `Luma - Order Confirmation`
2. Verwenden Sie das Ereignis: `LumaOnlinePurchase`
3. Erstellen Sie die Bestätigungs-E-Mail mit dem Namen `Luma - Order Confirmation`:

* Kategorie „Transaktion“ – Stellen Sie sicher, dass Sie die Transaktions-E-Mail-Oberfläche auswählen
* Die Betreffzeile muss mit dem Vornamen des Empfängers personalisiert werden und den Satz „Vielen Dank für Ihren Kauf“ enthalten
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
    <li>Sie sollte einen Link zur Luma-Website enthalten: https://publish1034.adobedemo.com/content/luma/us/en.html</li>
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
    <em>He {firstName}</em><p>
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
      <li> Entfernen Sie Rabatt, Gesamtsumme und Ankunft</p>
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
      <li>Die Strukturkomponente "1:2 Spalte links"für diesen Abschnitt verwenden
      <li>Dies sind kontextuelle Ereignisinformationen.
      <li>Verwenden Sie die [!UICONTROL helper function]: [!UICONTROL Each]
      <li>Wechseln Sie zum Format des Code-Editors, um die kontextuellen Daten hinzuzufügen.
  </td>
  <td>
    <strong>Kopfzeile</strong>
    <p>
    <em>Reihenfolge: `purchaseOrderNumber`</em>
    </p>
    <strong>Liste der bestellten Produkte:
 </strong>
  <p>Jedes Element sollte wie folgt formatiert sein:
 <img alt="Reihenfolge" src="./assets/c2-order.png"> 
</p>
</td>
  </tr>
</table>


>[!TIP]
>
>Damit Sie eine Fehlerbehebung bei Ihrer Journey vornehmen können, empfiehlt es sich, für alle Nachrichtenaktionen einen alternativen Pfad für den Fall einer Zeitüberschreitung oder eines Fehlers anzugeben.

>[!TAB Erfolgskriterien]

Triggern Sie die Journey, die Sie im Testmodus erstellt haben, und senden Sie die E-Mail an sich selbst:

1. Zeigen Sie die ausgeblendeten Werte an, indem Sie auf das Augensymbol klicken:
   1. Klicken Sie in den E-Mail-Parametern auf das T-Symbol (Parameterüberschreibungen aktivieren)
      ![E-Mail-Parameter überschreiben](/help/challenges/assets/c3-override-email-paramters.jpg)
   2. Klicken Sie in das Adressfeld
   3. Auf dem nächsten Bildschirm fügen Sie Ihre E-Mail-Adresse *yourname@yourdomain* in Klammern in den Ausdruckseditor ein und klicken Sie auf „OK“.
2. Setzen Sie die Journey in den Testmodus
3. Lösen Sie das Ereignis mit den folgenden Parametern aus:
   * Setzen Sie die Profilkennung auf: Identitätswert:`a8f14eab3b483c2b96171b575ecd90b1`
   * Ereignistyp: commerce.purchases
   * `Quantity`: 1
   * `Price Total:` 69
   * `Purchase Order Number:` 6253728
   * `SKU:` LLMH09
   * `City:` Washington
   * `Postal Code:` 20099
   * `State`: DC
   * `Street:` Thierer Terrace

Sie sollten die personalisierte Kaufbestätigungs-E-Mail mit angegebenem Produkt erhalten.

* Die Betreffzeile sollte den Vornamen des Testprofils enthalten: Leora
* Der Abschnitt „Bestelldetails“ sollte mit den Bestelldetails gefüllt sein, die Sie beim Testen eingegeben haben

>[!TAB Überprüfen Sie Ihre Arbeit]

**Journey**

![Journey](/help/challenges/assets/c2-journey.png)


**E-Mail**

**Betreffzeile:**

Vielen Dank für Ihren Einkauf. {{ profile.person.name.firstName }}!

So sollte Ihr E-Mail-Textkörper aussehen:

![E-Mail](//help/challenges/assets/c2-email.png)

**Abschnitt „Versand an“:**

So sollte Ihr Code aussehen:

```javascript
{{ profile.person.name.firstName }} {{ profile.person.name.lastName }}
{{context.journey.events.454181416.commerce.shipping.address.street1}}
{{context.journey.events.454181416.commerce.shipping.address.city}}, {{context.journey.events.454181416.commerce.shipping.address.state}} {{context.journey.events.454181416.commerce.shipping.address.postalCode}}
```

*event.45481416* wird für Sie eine andere Nummer sein.

TIPP: Personalisieren Sie jede Zeile separat

**Abschnitt „Bestelldetails“:**

So sollte Ihr Code aussehen:

Kopfzeile:

```javascript
Order #: {{context.journey.events.1627840522.commerce.order.purchaseOrderNumber}}
```

**Produktliste:**

Verwenden Sie zum Erstellen der Liste von Produkten die Helper-Funktion „each“. Zeigen Sie diese in einer Tabelle an. So sollte Ihr Code aussehen (mit Ihren spezifischen Variablen wie Ihrer Ereignis-ID - anstatt `454181416` und Ihrer Organisation anstelle von `techmarketingdemos` ):

```javascript
{{#each context.journey.events.454181416.productListItems as |product|}}<tr> <th class="colspan33"><div class="acr-fragment acr-component image-container" data-component-id="image" style="width:100%;text-align:center;" contenteditable="false"><!--[if mso]><table cellpadding="0" cellspacing="0" border="0" width="100%"><tr><td style="text-align: center;" ><![endif]--><img src="{{context.journey.events.454181416.productListItems.VYG__902489191a0a40e67f51f17f3ea9e2dfaf2dea3bd0bebe8b._techmarketingdemos.product.imageUrl}}" style="height:auto;width:100%;" height="233" width="233"><!--[if mso]></td></tr></table><![endif]--></div></th> <th class="colspan66"><div class="acr-fragment acr-component" data-component-id="text" contenteditable="false"><div class="text-container" contenteditable="true"><p><span style="font-weight:700;">{{context.journey.events.454181416.productListItems.VYG__902489191a0a40e67f51f17f3ea9e2dfaf2dea3bd0bebe8b._techmarketingdemos.product.name}}</span></p></div></div><div class="acr-fragment acr-component" data-component-id="text" contenteditable="false"><div class="text-container" contenteditable="true"><p>${{context.journey.events.454181416.productListItems.VYG__902489191a0a40e67f51f17f3ea9e2dfaf2dea3bd0bebe8b._techmarketingdemos.product.price}}.00</p><p>Quantity: {{context.journey.events.454181416.productListItems.quantity}}</p></div></div></th></tr> {{/each}}
```

**Gesamtpreis:**

Gesamt:`${{context.journey.events.1627840522.commerce.order.priceTotal}}.00`


>[!ENDTABS]