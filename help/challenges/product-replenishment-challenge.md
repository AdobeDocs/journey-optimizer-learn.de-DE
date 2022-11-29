---
title: Herausforderung bei der Produktwiedergabe
description: Wenden Sie das, was Sie über das Erstellen von Segmenten gelernt haben, an und testen Sie Ihre Fähigkeiten.
kt: 8417
feature: Segments
role: User
level: Beginner
hide: true
exl-id: 305aaf4c-7f5d-4f6f-abeb-466208f1fe48
source-git-commit: 8a2062f0719e799dd2d039488e6bba943fb458c4
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 3%

---

# Herausforderung bei der Produktwiedergabe

| Herausforderung | Produktnachfüllung |
|---|---|
| Persona | Journey-Manager |
| Erforderliche Fähigkeiten | <ul><li>[Erstellen von Segmenten](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-segments.html?lang=en)</li><li> [Importieren und Erstellen von HTML-E-Mail-Inhalten](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-messages/import-and-author-html-email-content.html?lang=en)</li><li>[Anwendungsfall: Segment lesen](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/use-case-read-segment.html?lang=en)</li> |
| Herunterzuladende Assets | [Saisonale Sammlungs-E-Mail-Dateien](/help/challenges/assets/email-assets/emails-seasonal-collection-announcement.zip) |

## Die Geschichte

Wenn Kunden auf der Website von Luma Produkte hinzufügen, die sie interessieren, können sie auf eine Wunschliste setzen. Dadurch kann Luma Kunden senden, die Marketingnachrichten und -informationen zu den Produkten erhalten möchten.

## Ihre Herausforderung

Luma fordert Sie auf, eine Journey in Journey Optimizer zu implementieren, die Kunden, die einen Artikel auf ihrer Wunschliste haben, der zuvor nicht vorrätig war, darüber informiert, wenn dieser Artikel wieder auf Lager ist.

## Definieren des Segments - Nicht vorrätige Wunschlisten-Elemente

Um potenzielle interessierte Kunden bei der erneuten Speicherung von Produkten anzusprechen, erstellen Sie ein Segment, das aus Kunden besteht

* Wer mindestens ein Element zu seiner Wunschliste hinzugefügt hat (Ereignistyp verwenden: [!UICONTROL Commerce Save For Laters])
* Welche **nicht vorrätig** in den letzten 3 Monaten (Verwendung der Lagermenge = 0)
* Und haben seitdem nicht den Artikel gekauft.

Benennen Sie dieses Segment: *Ihr Name - Out-of-stock-Wishlist*

+++**ÜBERPRÜFEN IHRER ARBEIT**

So sollte Ihr Segment aussehen:

![Segment - Nicht vorrätige Wunschlisten-Elemente](/help/challenges/assets/C1-S2.png)

Kunden, die in den letzten drei Monaten einen Artikel auf ihre Wunschliste gesetzt haben, der nicht auf Lager war:

* Ereignis: Für Später speichern
   * Mindestens 1 einschließen
   * Wenn die Lagermenge 0 beträgt

und haben seitdem nicht den Artikel gekauft:

* Schließen Sie alle Kauf -Ereignistypen aus, bei denen die SKU mit der SKU aus der **Für späteres Ereignis speichern**.

>[!TIP]
> * Wählen Sie die SKU unter &quot;Für Later speichern&quot;im *Variablen durchsuchen* Abschnitt
> * Verwenden Sie die Vergleichsoption, wenn Sie die SKU unter Speichern für später in das Ereignisfeld ablegen


Überprüfen Sie den Code in der rechten unteren Ecke des Bildschirms Segment bearbeiten unter Ereignisse . Der Code sollte wie folgt aussehen:

Code:
```(Include have at least 1 Save For Laters event where ((Stock Quantity equals 0)) THENExclude all  Purchases events where ((SKU equals Save For Laters1 SKU)) ) and occurs in last 3 month(s)```

+++

### E-Mail erstellen - Luma-Produkt-Wiederauffüllung

Benachrichtigen Sie Kunden, die einen nicht vorrätigen Artikel mit einem Aufruf zum Einkaufen hinzugefügt haben, jetzt darüber, dass der Artikel wieder auf Lager ist.

### Journey erstellen - Benachrichtigung zur Produktüberarbeitung

Wenn ein zuvor nicht vorrätiger Artikel wieder auf Lager ist, benachrichtigen Sie Kunden, die einen nicht vorrätigen Artikel hinzugefügt haben, mit einem Aufruf zum Einkaufen, jetzt, dass der Artikel wieder auf Lager ist.

1. Erstellen Sie eine Journey mit dem Namen &quot;Ihr Name_Luma - Produktneuerung&quot;.
1. Die Journey sollte ausgelöst werden, wenn ein Produkt wieder auf Lager ist
1. Senden Sie die *Nachfüllen von Luma-Produkten* E-Mail an
1. Benutzer, die diesen Artikel ihrer Wunschliste hinzugefügt haben, während er nicht vorrätig war

>[!TIP]
>
> Verwenden Sie das vorhandene Geschäftsereignis. Sie müssen eine Bedingung hinzufügen, mit der überprüft wird, ob die SKU erneut vorrätig ist, wenn der Ereignistyp (Beliebig) für spätere Ereignisse enthalten ist.

+++**ERFOLGSKRITERIEN**

Testen Sie Ihre Journey:

1. Stellen Sie sicher, dass das Segmentqualifikationsereignis den Namespace = E-Mail aufweist.
1. Überschreiben Sie die Standard-E-Mail-Parameter und legen Sie sie auf Ihre eigene E-Mail-Adresse fest (Anweisungen finden Sie in E-Mail 1 ).
1. Journey auf Testmodus setzen
1. Trigger und Ereignis - Geben Sie die folgenden Daten ein:

   * Beschreibung: Vergessen Sie die fantasievollen Maschinen und teuren Mitgliedschaften - das Harmony Lumaflex Strength Band Kit ist alles, was Sie für ein erstaunliches Training benötigen. Das Kit hat alles, was Sie für eine Reihe von Stärkung und Ton Übungen benötigen.
   * Name: Harmony Lumaflex Strength Band Kit
   * Preis: 22
   * Produkt-ID: 24-UG03
   * Produktbild-URL: https://publish1034.adobedemo.com/content/dam/luma/en/products/gear/fitness-equipment/ug03-bk-0.jpSKU: 24-UG03
   * Lagerereignistyp: restock
   * Profilkennung: Jenna_Palmer9530@emailsim.io

Sie sollten die E-Mail &quot;Luma Email Product Replenfy&quot; mit den Produktdetails und der Personalisierung für Jenna erhalten.

+++

+++**ÜBERPRÜFEN IHRER ARBEIT**

So sollte Ihre Journey aussehen:

![Journey zur Produkterneuerung](/help/challenges/assets/c3-j3-journey.png)

Bedingung: In Wunschliste

![Bedingung - in der Wunschliste](/help/challenges/assets/c3-j3-condition.png)

Bedingungscode:

```in(@{LumaProductRestock._wwfovlab065.sku},#{ExperiencePlatform.ExperienceEvents.experienceevent.all(currentDataPackField.eventType=="commerce.saveForLaters").productListItems.all().SKU})```

+++
