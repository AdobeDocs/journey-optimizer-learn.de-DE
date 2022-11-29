---
title: Bestellbestätigung erstellen
description: Testen Sie Ihr Wissen über das Erstellen und Personalisieren von Transaktionsnachrichten.
kt: 7531
feature: Journeys
role: User
level: Beginner
hide: true
exl-id: ec86e2ac-081d-47aa-a948-007107baa2b4
source-git-commit: 8a2062f0719e799dd2d039488e6bba943fb458c4
workflow-type: tm+mt
source-wordcount: '754'
ht-degree: 4%

---

# Transaktions-E-Mail zur Bestellbestätigung erstellen

![Bestellungsbestätigung](/help/challenges/assets/email-assets/luma-transactional-order-confirmation.png)

| Herausforderung | Transaktions-E-Mail zur Bestellbestätigung erstellen |
|---|---|
| Persona | Journey-Manager |
| Erforderliche Fähigkeiten | <ul><li>[Erstellen von E-Mail-Inhalten mit dem Nachrichten-Editor](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-messages/create-email-content-with-the-message-editor.html?lang=en)</li> <li>[Verwenden von kontextbezogenen Ereignisinformationen für die Personalisierung](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/personalize-content/use-contextual-event-information-for-personalization.html?lang=en)</li><li>[Verwenden von Helper-Funktionen für die Personalisierung](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/personalize-content/use-helper-functions-for-personalization.html?lang=en)</li></ul> |
| Herunterzuladende Assets | [Bestellbestätigungs-Assets](/help/challenges/assets/email-assets/order-confirmation-assets.zip) |

## Die Geschichte

Luma startet seinen Online-Shop und möchte ein gutes Kundenerlebnis sicherstellen, indem er eine Bestätigungs-E-Mail sendet, sobald ein Kunde eine Bestellung aufgegeben hat.

Erstellen und personalisieren Sie eine Bestätigungsnachricht für Transaktionsbestellungen.

## Hast du alles, was du brauchst?

## Ihre Herausforderung

Erstellen Sie eine E-Mail zur Bestellbestätigung, die ausgelöst wird, wenn ein Luma-Kunde eine Online-Bestellung abschließt.

### E-Mail zur Bestellbestätigung erstellen

Erstellen Sie eine neue E-Mail-Nachricht mit dem Titel &quot;(Ihr Name)_Luma - Auftragsbestätigung&quot;. Die Betreffzeile muss mit dem Vornamen des Empfängers personalisiert werden und die Phrase &quot;Vielen Dank für Ihren Kauf&quot; enthalten.

Gemäß der Markenrichtlinie von Luma sollte die E-Mail wie folgt strukturiert sein:

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
    <li>Größe 35%, zentrierter weißer Hintergrund </li>
    <li>Es sollte einen Link zur Luma-Website enthalten: https://publish1034.adobedemo.com/content/luma/us/en.html</li>
    <p>
    Tipp: Sie finden alle Bilder im Ordner "Assets"mit dem Namen "Nachrichtenbilder". <p>
    </td>
  </tr>
  <tr>
  <td>
  <div>
    <strong>Abschnitt zur Bestellbestätigung
    </strong>
  </td>
  <td>
    <strong>Bild</strong><p>
    <li>luma-transactional-order-confirmation-2.jpg </li>
    <li>Rand: Oben, unten (10)<div>
    <p>
    <strong>Text</strong><p>
    <em>Danke für den Kauf!</em><p>
    <li>Ausrichtung: left  </li>
   <li>Textfarbe: rgb(101, 106, 119); Schriftgröße:14 px</li>
    <li>Abstand: links (95), rechts (95)</li><div>
    <p>
     <em>Ihre Bestellung wurde aufgegeben.
    <p>Sobald Ihr Package versandt wurde, senden wir Ihnen eine E-Mail mit einer Trackingnummer, damit Sie Ihre Bestellung verfolgen können.</p></em>
    </strong><p>
    <li>Ausrichtung: left  </li>
    <li>Textfarbe: rgb(101, 106, 119); Schriftgröße:14 px </li>
    <li>Abstand: links (95), rechts (95)</li><div>
    </a>
    <p>
    <strong>Schaltfläche:</strong>
   <p><em>Bestellung anzeigen</em></p>
      <li>Hintergrundfarbe: rgb(25, 121, 195)</li>
      <li>Textfarbe: weiß</li>
      <li>Kein Rahmen</li>
      <li>Höhe: 40</li>
      <li>Einen Link zu einer Website Ihrer Wahl hinzufügen </li>
      <li>Linksbündig am Text oben ausrichten (Spitze: den Containerrand verwenden)</li>
  </td>
 <tr>
<td>
  <div>
     <strong>Bestelldetailabschnitt</strong>
      </div>
      <p>Tipps:
      <li>Dies sind kontextbezogene Ereignisinformationen. Sie können die Nachricht nur dann im Kontext hinzufügen, wenn Sie sie zu Ihrer Journey hinzufügen (siehe Schritt 2). Veröffentlichen Sie Ihre E-Mail nicht, bevor Sie sie der Journey hinzugefügt und mit den kontextuellen Ereignisinformationen modifiziert haben!</li>
      <li>Verwenden Sie die Hilfsfunktion: Jeder</li>
      <li>Verwenden Sie das HTML-Editor-Format für die Kontextdaten. Fügen Sie die Informationen mithilfe von DIV-Tags in Container ein.</li>
  </td>
  <td>
    <strong>Kopfzeile</strong>
    <p>
    <em>Bestellung {Bestellnummer}</em>
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

### Journey erstellen

1. Rufen Sie die Journey &quot;Ihr Name _Luma-Auftragsbestätigung&quot;auf.
1. Verwenden Sie das Ereignis: LumaOnlinePurchase
1. Aktion: Fügen Sie die in Schritt 1 erstellte Nachricht hinzu.
1. Kehren Sie zur Nachricht zurück und fügen Sie die Kontextattribute hinzu.
1. E-Mail veröffentlichen

>[!TIP]
>
>Damit Sie eine Fehlerbehebung bei Ihren Journey vornehmen können, empfiehlt es sich, im Fall von Zeitüberschreitung oder Fehlern einen alternativen Pfad zu allen Nachrichten-Aktionen hinzuzufügen.

+++Erfolgskriterien

Trigger der Journey, die Sie im Testmodus erstellt haben, und senden Sie die E-Mail an sich:

1. Zeigen Sie die ausgeblendeten Werte an, indem Sie auf das Augensymbol klicken:
   1. Klicken Sie in den E-Mail-Parametern auf das T-Symbol (aktivieren Sie die Parameterüberschreibungen
      ![E-Mail-Parameter überschreiben](/help/challenges/assets/c3-override-email-paramters.jpg)
   2. Klicken Sie in das Adressfeld
   3. Fügen Sie im nächsten Bildschirm Ihre E-Mail-Adresse in Klammern ein: *yourname@yourdomain* im Ausdruckseditor und klicken Sie auf &quot;OK&quot;.
2. Journey in den Testmodus versetzen
3. Trigger des Ereignisses mit den folgenden Parametern:
   * Legen Sie die Profilkennung auf Folgendes fest: Jenna_Palmer9530@emailsim.io
   * Ereignistyp: commerce.purchases
   * Name: Sprite Yoga Companion Kit
   * Menge: 1
   * Gesamtpreis: 61
   * Bestellnummer: 6253728
   * SKU: 24-WG080
   * productImageURL: <https://publish1034.adobedemo.com/content/dam/luma/en/products/gear/fitness-equipment/luma-yoga-kit-2.jpg>

Sie sollten die personalisierte Kaufbestätigungs-E-Mail mit dem angegebenen Produkt erhalten.

* Die Betreffzeile sollte mit dem Vornamen Ihres Testprofils beginnen: Jenna
* Der Abschnitt mit Bestelldetails sollte mit den Bestelldetails gefüllt werden, die Sie beim Testen eingegeben haben
* Die Kundeninformationen sollten die Stadt und Postleitzahl Ihres Testprofils enthalten:

   43913 Thierer Terrace, Washington DC 2009

+++

+ + + Prüfung der Arbeit

**Betreff:**

{{ profile.person.name.firstName }}, danke für Ihren Kauf!

**Kopfzeile und Bestätigungsabschnitt:**

![Header- und Bestellbestätigung](/help/challenges/assets/c2-header.png)

**Detailabschnitt Oder:**

![Bestelldetailabschnitt](/help/challenges/assets/c2-order-detail-section.png)

So sollte Ihr Code aussehen:

Header:

```javascript
Order: {{context.journey.events.1627840522.commerce.order.purchaseOrderNumber}}
```

Liste der Erzeugnisse:

Verwenden Sie die Hilfsfunktion &quot;each&quot;, um die Liste der Produkte zu erstellen. So sollte Ihr Code aussehen:

```javascript
{{#each context.journey.events.1911672547.productListItems as|product|}}
<div class="cart-item-chair" style="box-sizing:border-box;min-height:40px;padding-top:20px;padding-bottom:20px;padding-left:80px;border-radius:0px;background-image:url({{product._wwfovlab065.productImageURL}});background-position:0% 50%;background-size:60px;background-repeat:no-repeat;">
<h5 style="box-sizing:border-box;margin-bottom:5px;font-size:16px;line-height:20px;margin-top:0px;">${{product.priceTotal}}.00</h5>
<div class="text-small" style="box-sizing:border-box;padding-top:5px;color:rgb(101, 106, 119);font-size:14px;">{{product.name}}</div><div class="text-small" style="box-sizing:border-box;padding-top:5px;color:rgb(101, 106, 119);font-size:14px;">Quantity: {{product.quantity}}</div></div><div class="divider-small" style="box-sizing:border-box;height:1px;margin-top:10px;margin-bottom:10px;background-color:rgb(209, 213, 223);"> </div>
{{/each}}

Total: ${{context.journey.events.1627840522.commerce.order.priceTotal}} 
```

**Bereich &quot;Kundeninformationen&quot;**

![Kundenadresse](assets/c2-customer-information.png)

Die Personalisierung sollte wie folgt aussehen:

```javascript
{{profile.homeAddress.street1}}
{{profile.homeAddress.city}},{{profile.homeAddress.state}} {{profile.homeAddress.postalCode}}
```

**Fußzeile:**
![Fußzeile](/help/challenges/assets/c2-footer.png)

**Journey**

![Journey](/help/challenges/assets/c2-journey.png)

+++
