---
title: Challenge zur Produktauffüllung
description: Wenden Sie Ihr erworbenes Wissen über das Erstellen von Segmenten an und testen Sie Ihre Fähigkeiten.
kt: 8417
feature: Segments
role: User
level: Beginner
hide: true
exl-id: 305aaf4c-7f5d-4f6f-abeb-466208f1fe48
source-git-commit: 0e83d8fbad6bd87ed25980251970898cb5b94bc0
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 100%

---

# Challenge zur Produktauffüllung

| Challenge | Produktauffüllung |
|---|---|
| Persona | Journey-Manager |
| Erforderliche Fähigkeiten | <ul><li>[Erstellen von Segmenten](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-segments.html?lang=de)</li><li> [Importieren und Erstellen von HTML-E-Mail-Inhalten](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-messages/import-and-author-html-email-content.html?lang=de)</li><li>[Anwendungsfall: Segment lesen](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/use-case-read-segment.html?lang=de)</li> |
| Herunterzuladende Assets | [E-Mail-Dateien zur saisonalen Kollektion](/help/challenges/assets/email-assets/emails-seasonal-collection-announcement.zip) |

## Die Story

Wenn Kundinnen und Kunden auf der Website navigieren, können sie Produkte, die sie interessieren, auf eine Wunschliste setzen. So kann Luma den Kundinnen und Kunden gezielte Marketing-Nachrichten und Informationen zu den Produkten senden.

## Ihre Challenge

Luma bittet Sie, eine Journey in Journey Optimizer zu implementieren. Diese benachrichtigt Kundinnen und Kunden, die einen vergriffenen Artikel auf ihrer Wunschliste haben, wenn dieser Artikel wieder vorrätig ist.

## Definieren des Segments – Nicht vorrätige Artikel auf der Wunschliste

Um potenzielle interessierte Kundinnen und Kunden im Fall der erneuten Verfügbarkeit von Produkten anzusprechen, erstellen Sie ein Segment, das aus Personen besteht,

* die mindestens einen Artikel zu ihrer Wunschliste hinzugefügt haben (Verwenden des Ereignistyps: [!UICONTROL Commerce – für später speichern])
* Welche in den letzten 3 Monaten **nicht vorrätig** waren (Verwenden der Lagermenge = 0)
* Und den Artikel seitdem nicht gekauft haben.

Benennen Sie dieses Segment: *Ihr Name – Wunschliste für nicht vorrätige Artikel*

+++**ÜBERPRÜFEN SIE IHRE ARBEIT**

So sollte Ihr Segment aussehen:

![Segment – Nicht vorrätige Artikel auf der Wunschliste](/help/challenges/assets/C1-S2.png)

Kundinnen und Kunden, die in den letzten drei Monaten einen Artikel auf ihre Wunschliste gesetzt haben, der nicht vorrätig war:

* Ereignis: Für später speichern
   * Mindestens 1 einschließen
   * Wenn die Lagermenge 0 beträgt

und seitdem den Artikel nicht gekauft haben:

* Schließen Sie alle „Purchases“-Ereignistypen aus, bei denen die SKU mit der SKU aus dem Ereignis **Für später speichern** übereinstimmt.

>[!TIP]
> * Wählen Sie die SKU unter „Für später speichern“ im Abschnitt *Variablen durchsuchen*
> * Verwenden Sie die Vergleichsoption, wenn Sie die SKU unter „Für später speichern“ in das Ereignisfeld ablegen


Überprüfen Sie den Code in der rechten unteren Ecke des Bildschirms „Segment bearbeiten“ unter „Ereignisse“. Der Code sollte wie folgt aussehen:

Code:
```(Include have at least 1 Save For Laters event where ((Stock Quantity equals 0)) THENExclude all  Purchases events where ((SKU equals Save For Laters1 SKU)) ) and occurs in last 3 month(s)```

+++

### E-Mail erstellen – Wiederauffüllung von Luma-Produkten

Benachrichtigen Sie Kunden, die einen nicht vorrätigen Artikel hinzugefügt hatten, mit einem Aufruf, jetzt einzukaufen, da der Artikel wieder auf Lager ist.

### Erstellen der Journey – Benachrichtigung zur Wiederverfügbarkeit des Produkts

Wenn ein zuvor nicht vorrätiger Artikel wieder auf Lager ist, benachrichtigen Sie Kunden, die einen nicht vorrätigen Artikel hinzugefügt hatten, mit einem Aufruf, jetzt einzukaufen, da der Artikel wieder auf Lager ist.

1. Erstellen Sie eine Journey mit dem Namen „Ihr Name_Luma – Produkt-Wiederverfügbarkeit“
1. Die Journey sollte ausgelöst werden, wenn ein Produkt wieder auf Lager ist
1. Senden Sie die E-Mail *Luma-Produktauffüllung* an
1. Benutzende, die diesen Artikel ihrer Wunschliste hinzugefügt haben, während er nicht vorrätig war

>[!TIP]
>
> Nutzen Sie das vorliegende Geschäftsereignis. Sie müssen eine Bedingung hinzufügen, mit der überprüft wird, ob die SKU für die Auffüllung der Lagerbestände in (irgend)einem Ereignistyp enthalten ist, für später.

+++**ERFOLGSKRITERIEN**

Testen Sie Ihre Journey:

1. Stellen Sie sicher, dass das Segmentqualifikationsereignis den Namespace = E-Mail aufweist.
1. Überschreiben Sie die Standard-E-Mail-Parameter, indem Sie sie entsprechend Ihrer eigenen E-Mail-Adresse festlegen (Anweisungen dafür finden Sie in E-Mail 1).
1. Setzen Sie die Journey in den Testmodus
1. Auslösen des Ereignisses – Geben Sie die folgenden Daten ein:

   * Beschreibung: Vergessen Sie originelle Geräte und teure Mitgliedschaften – das Harmony Lumaflex Strength Band-Set ist alles, was Sie für ein tolles Training brauchen. Das Set enthält alles, was Sie für vielfältige Kräftigungs- und Muskelaufbauübungen benötigen.
   * Name: Harmony Lumaflex Strength Band-Set
   * Preis: 22
   * Produkt-ID: 24-UG03
   * Produktbild-URL: https://publish1034.adobedemo.com/content/dam/luma/en/products/gear/fitness-equipment/ug03-bk-0.jpSKU: 24-UG03
   * Lagerereignistyp: restock
   * Profilkennung: Jenna_Palmer9530@emailsim.io

Sie sollten die E-Mail „Luma E-Mail Produktnachschubdisposition“ mit den Produktdetails und der Personalisierung für Jenna erhalten.

+++

+++**ÜBERPRÜFEN SIE IHRE ARBEIT**

So sollte Ihre Journey aussehen:

![Journey zur Produktauffüllung](/help/challenges/assets/c3-j3-journey.png)

Bedingung: auf Wunschliste

![Bedingung – auf Wunschliste](/help/challenges/assets/c3-j3-condition.png)

Bedingungs-Code:

```in(@{LumaProductRestock._wwfovlab065.sku},#{ExperiencePlatform.ExperienceEvents.experienceevent.all(currentDataPackField.eventType=="commerce.saveForLaters").productListItems.all().SKU})```

+++
