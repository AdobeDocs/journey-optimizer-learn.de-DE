---
title: E-Mail zur Bestellbestätigung erstellen
description: Testen Sie Ihr Wissen über das Erstellen und Personalisieren von Transaktionsnachrichten.
kt: 7531
feature: Journeys
role: User
level: Beginner
hide: true
exl-id: ec86e2ac-081d-47aa-a948-007107baa2b4
source-git-commit: 4268144ade6588e48fc38cae7e542c227af96827
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 5%

---


# E-Mail zur Bestellbestätigung erstellen

![Bestellungsbestätigung](/help/challenges/assets/email-assets/luma-transactional-order-confirmation.png)

| Herausforderung | Transaktions-E-Mail zur Bestellbestätigung erstellen |
|---|---|
| Persona | Journey-Manager |
| Erforderliche Fähigkeiten | <ul><li>[Erstellen von E-Mail-Inhalten mit dem Nachrichten-Editor](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-messages/create-email-content-with-the-message-editor.html?lang=en)</li> <li>[Verwenden von kontextbezogenen Ereignisinformationen für die Personalisierung](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/personalize-content/use-contextual-event-information-for-personalization.html?lang=en)</li><li>[Verwenden von Helper-Funktionen für die Personalisierung](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/personalize-content/use-helper-functions-for-personalization.html?lang=en)</li></ul> |
| Herunterzuladende Assets | [Bestellbestätigungs-Assets](/help/challenges/assets/email-assets/order-confirmation-assets.zip) |

## Die Geschichte

Luma startet seinen Online-Store und möchte ein gutes Kundenerlebnis sicherstellen, indem eine Bestätigungs-E-Mail für die Bestellung bereitgestellt wird, sobald ein Kunde eine Bestellung aufgegeben hat.



## Ihre Herausforderung

Erstellen Sie eine Journey, die eine Bestätigungs-E-Mail sendet, wenn ein Luma-Kunde eine Online-Bestellung abschließt. Die Luma

>[!BEGINTABS]

>[!TAB Aufgabe]

1. Erstellen Sie eine Journey mit dem Namen `Luma - Order Confirmation`
2. Verwenden Sie das Ereignis: `LumaOnlinePurchase` als Trigger
3. Erstellen Sie die Bestätigungs-E-Mail mit dem Namen `Luma - Order Confirmation`:

* Kategorietransaktion - Stellen Sie sicher, dass Sie die Transaktions-E-Mail-Oberfläche auswählen.
* Die Betreffzeile muss mit dem Vornamen des Empfängers personalisiert werden und die Phrase &quot;Vielen Dank für Ihren Kauf&quot; enthalten.
* Verwenden Sie die `Luma - Order summary` und ändern Sie sie:

Die E-Mail sollte wie folgt strukturiert sein:
<table>
<tr>
<td>
  <div>
     <strong> Kopfzeilenabschnitt</strong>
      </div>
  </td>
  <td>
    <strong>Luma-Logo</strong>
      <p>
     <li>luma_logo.png</li>
    <li>Es sollte einen Link zur Luma-Website enthalten: https://publish1034.adobedemo.com/content/luma/us/en.html</li>
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
    <em>He {first name}</em><p>
    <li>Ausrichtung: left  </li>
   <li>Textfarbe: rgb(69, 97, 162) #4461a2; 
   <li>Schriftgröße: 20 px</li>
   <div>
    <p>
     <em>Ihre Bestellung wurde aufgegeben.
    <p>Sobald Ihr Package versandt wurde, senden wir Ihnen eine E-Mail mit einer Trackingnummer, damit Sie Ihre Bestellung verfolgen können.</p></em>
    </strong>
    </tr>
  </td>
 <td>
  <div>
     <strong> Zu Abschnitt schicken</strong>
      </div>
      <p><li>Ersetzen Sie die hartcodierte Adresse in der Vorlage durch die Lieferadresse. 
      <li>Die Adressdetails sind kontextbezogene Attribute der Veranstaltung (Straße, Stadt, Postleitzahl, Bundesland)
      <li>Vorname und Nachname stammen aus dem Profil
      <li> Rabatt, Gesamtsumme, Ankunft entfernen</p>
  </td>
  <td>
  <p> Versand an:</p>
      <em>Vorname Nachname<br>
     Adresse</em></p>
  </td>
 <tr>
<td>
  <div>
     <strong>Bestelldetailabschnitt</strong>
      </div>
       <p><li>Fügen Sie diesen Abschnitt nach dem <b>Versand an</b> und <b>Bestellung anzeigen</b> Schaltfläche.
      </p><br>
      <p><b>Tipps:</b>
      <li>Dies sind kontextbezogene Ereignisinformationen.
      <li>Verwenden Sie die [!UICONTROL Helper-Funktion]: [!UICONTROL each]
      <li>Wechseln Sie zum Format des Code-Editors , um die Kontextdaten hinzuzufügen.
      <li>Fügen Sie die Informationen mithilfe von DIV-Tags in Container ein.
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
<strong>Produktbild:</strong>
<li>-Klasse: Warenkorb-Artikelstuhl
<li>style: border-box: min-height:40px</li>
<li>Auffüllung oben und unten:20px</li>
<li>padding-left:80px</li>
<li>border-radius:0px</li>
<li>Als Hintergrundbild für den Container verwenden</li>
<li>background-position: 0 % 50 %</li>
<li>background-size: 60 px</li>
<li>background-repeat: no-repeat</li>
<p>
<strong>Preis:</strong>
<li>Format = H5</li>
<li>style = box-size:border-box</li>
<li>margin-bottom:5px</li>
<li>margin-top:0px;</li>
<p>
<strong>Name und Menge:</strong>
<li>class=text-small</li>
<li>style=box-size: border-box</li>
<li>padding-top: 5px</li>
<li>color: rgb(101, 106, 119)</li>
<li>Schriftgröße:14 px</li>
<p>
</td>
  </tr>
</table>


>[!TIP]
>
>Damit Sie eine Fehlerbehebung bei Ihren Journey vornehmen können, empfiehlt es sich, im Fall von Zeitüberschreitung oder Fehlern einen alternativen Pfad zu allen Nachrichten-Aktionen hinzuzufügen.

>[!TAB Erfolgskriterien]

Trigger der Journey, die Sie im Testmodus erstellt haben, und senden Sie die E-Mail an sich:

1. Zeigen Sie die ausgeblendeten Werte an, indem Sie auf das Augensymbol klicken:
   1. Klicken Sie in den E-Mail-Parametern auf das T-Symbol (aktivieren Sie die Parameterüberschreibungen
      ![E-Mail-Parameter überschreiben](/help/challenges/assets/c3-override-email-paramters.jpg)
   2. Klicken Sie in das Adressfeld
   3. Fügen Sie im nächsten Bildschirm Ihre E-Mail-Adresse in Klammern ein: *yourname@yourdomain* im Ausdruckseditor und klicken Sie auf &quot;OK&quot;.
2. Journey in den Testmodus versetzen
3. Trigger des Ereignisses mit den folgenden Parametern:
   * Legen Sie die Profilkennung auf Folgendes fest: Identitätswert:`a8f14eab3b483c2b96171b575ecd90b1`
   * Ereignistyp: commerce.purchases
   * Name: Sprite Yoga Companion Kit
   * Menge: 1
   * `Price Total:` 61
   * `Purchase Order Number:` 6253728
   * `SKU:` 24-WG080
   * `productImageURL:` <https://publish1034.adobedemo.com/content/dam/luma/en/products/gear/fitness-equipment/luma-yoga-kit-2.jpg>
   * `City:` San Jose
   * `Postal Code:` 95110
   * `State`: CA
   * `Street:` 345 Park Ave

Sie sollten die personalisierte Kaufbestätigungs-E-Mail mit dem angegebenen Produkt erhalten.

* Die Betreffzeile sollte den Vornamen des Testprofils enthalten: Leora
* Der Abschnitt mit Bestelldetails sollte mit den Bestelldetails gefüllt werden, die Sie beim Testen eingegeben haben

>[!TAB Überprüfen Sie Ihre Arbeit]

**Journey**

![Journey](/help/challenges/assets/c2-journey.png)


**E-Mail**

**Betreff:**

{{ profile.person.name.firstName }}, danke für Ihren Kauf!

**Zu Abschnitt schicken:**

So sollte Ihr Code aussehen:

```javascript
{{ profile.person.name.firstName }} {{ profile.person.name.lastName }}
{{context.journey.events.454181416.commerce.shipping.address.street1}}
{{context.journey.events.454181416.commerce.shipping.address.city}}, {{context.journey.events.454181416.commerce.shipping.address.state}} {{context.journey.events.454181416.commerce.shipping.address.postalCode}}
```

*event.45481416* wird eine andere Nummer für Sie sein.

TIPP: Jede Zeile separat personalisieren

**Detailabschnitt Oder:**

![Bestelldetailabschnitt](/help/challenges/assets/c2-order-detail-section.png)

So sollte Ihr Code aussehen:

Header:

```javascript
Order: {{context.journey.events.1627840522.commerce.order.purchaseOrderNumber}}
```

**Liste der Erzeugnisse:**

Verwenden Sie die Hilfsfunktion &quot;each&quot;, um die Liste der Produkte zu erstellen. Zeigen Sie sie in einer Tabelle an. So sollte Ihr Code aussehen:

```javascript
<div class="text-container" contenteditable="true">
  <p><span class="acr-expression-field" contenteditable="false">{{#each context.journey.events.454181416.productListItems as |product|}}
    </span></p>
  <div class="cart-item-chair" style="box-sizing:border-box;min-height:40px;padding-top:20px;padding-bottom:20px;padding-left:80px;border-radius:0px;background-image:url({{product.VYG__902489191a0a40e67f51f17f3ea9e2dfaf2dea3bd0bebe8b._techmarketingdemos.product.imageUrl}});background-position:0% 50%;background-size:60px;background-repeat:no-repeat;">
    <h5 style="box-sizing:border-box;margin-bottom:5px;font-size:16px;line-height:20px;margin-top:0px;">${{product.VYG__902489191a0a40e67f51f17f3ea9e2dfaf2dea3bd0bebe8b._techmarketingdemos.product.price}}.00</h5>
    <div class="text-small" style="box-sizing:border-box;padding-top:5px;color:rgb(101, 106, 119);font-size:14px;">{{product.VYG__902489191a0a40e67f51f17f3ea9e2dfaf2dea3bd0bebe8b._techmarketingdemos.product.name}}</div>
    <div class="text-small" style="box-sizing:border-box;padding-top:5px;color:rgb(101, 106, 119);font-size:14px;">Quantity: {{product.quantity}}</div>
  </div>
  <div class="divider-small" style="box-sizing:border-box;height:1px;margin-top:10px;margin-bottom:10px;background-color:rgb(209, 213, 223);"> </div>
  {{/each}}<p></p>
  <p></p>
</div>
```

**Preissumme:**

Gesamt:`${{context.journey.events.1627840522.commerce.order.priceTotal}}`

**Bereich &quot;Kundeninformationen&quot;**

![Kundenadresse](assets/c2-customer-information.png)

Die Personalisierung sollte wie folgt aussehen:

```javascript
{{profile.homeAddress.street1}}
{{profile.homeAddress.city}},{{profile.homeAddress.state}} {{profile.homeAddress.postalCode}}
```

>[!ENDTABS]