---
title: Challenge zur Produktauffüllung
description: Wenden Sie Ihr erworbenes Wissen über das Erstellen von Segmenten an und testen Sie Ihre Fähigkeiten.
kt: 8417
feature: Segments
role: User
level: Beginner
hide: true
exl-id: 305aaf4c-7f5d-4f6f-abeb-466208f1fe48
source-git-commit: 7ecbed1b722d7f05ffd4a7c7071358d993cb1392
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 69%

---

# Challenge zur Produktauffüllung

| Challenge | Produktauffüllung |
|---|---|
| Persona | Journey-Manager |
| Erforderliche Fähigkeiten | <ul><li>[Erstellen von Segmenten](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/profiles-segments-subscriptions/create-segments.html?lang=de)</li><li> [Importieren und Erstellen von HTML-E-Mail-Inhalten](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/email-channel/import-and-author-html-email-content.html?lang=en)</li><li>[Anwendungsfall: Segment lesen](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/use-case-read-segment.html?lang=de)</li> |
| Herunterzuladende Assets | [E-Mail-Datei für Produktvorräte](/help/challenges/assets/email-assets/ProductRestockEmail.html.zip) |

## Die Story

Kunden können auf der Luma-Website Produkte hinzufügen, die sie interessieren, und so auf eine Wunschliste setzen, sodass Luma Kunden, die Marketingnachrichten und -informationen zu den Produkten auswählen, senden kann.

## Ihre Challenge

Luma bittet Sie, eine Journey in Journey Optimizer zu implementieren. Diese benachrichtigt Kundinnen und Kunden, die einen vergriffenen Artikel auf ihrer Wunschliste haben, wenn dieser Artikel wieder vorrätig ist. Das Kreativteam stellt Ihnen die [E-Mail-Datei für Produktvorräte](/help/challenges/assets/email-assets/ProductRestockEmail.html.zip).

>[!BEGINTABS]

>[!TAB Aufgabe]

## 1. Definieren Sie das Segment - Nicht vorrätige Wunschlisten-Elemente

Um potenzielle interessierte Kunden bei der erneuten Speicherung von Produkten anzusprechen, erstellen Sie ein Segment, das aus Kunden besteht:

* Wer mindestens ein Element zu seiner Wunschliste hinzugefügt hat (Ereignistyp verwenden: [!UICONTROL Commerce Save For Laters])
* Die in den letzten drei Monaten nicht vorrätig war (Lagermenge = 0)
* Und den Artikel seitdem nicht gekauft haben.

>[!TIP]
>Schließen Sie alle „Purchases“-Ereignistypen aus, bei denen die SKU mit der SKU aus dem Ereignis *Für später speichern* übereinstimmt. Sie finden das Feld im *Variablen durchsuchen* Abschnitt.

Benennen Sie dieses Segment: `Out-of-stock-Wishlist`


### 2. Erstellen Sie die Journey - Produktneuvorratsbenachrichtigung

Wenn ein zuvor nicht vorrätiger Artikel wieder auf Lager ist, benachrichtigen Sie Kunden, die einen nicht vorrätigen Artikel hinzugefügt hatten, mit einem Aufruf, jetzt einzukaufen, da der Artikel wieder auf Lager ist.

1. Rufen Sie die Journey auf: `Product Restock`
2. Die Journey sollte ausgelöst werden, wenn ein Produkt wieder auf Lager ist
3. Senden Sie die *Produkt-Repository-E* nach
4. Benutzende, die diesen Artikel ihrer Wunschliste hinzugefügt haben, während er nicht vorrätig war

>[!TAB Erfolgskriterien]

Testen Sie Ihre Journey:

1. Stellen Sie sicher, dass das Lesesegment-Ereignis den Namespace = hat. `Luma CRM ID`
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

>[!TAB Überprüfen Sie Ihre Arbeit]

So sollte Ihr Segment aussehen:

![Segment – Nicht vorrätige Artikel auf der Wunschliste](/help/challenges/assets/C1-S2.png)


So sollte Ihre Journey aussehen:

![Journey zur Produktauffüllung](/help/challenges/assets/c3-j3-journey.png)

Bedingung: auf Wunschliste

![Bedingung – auf Wunschliste](/help/challenges/assets/c3-j3-condition.png)

Bedingungs-Code:

```in(@{LumaProductRestock._wwfovlab065.sku},#{ExperiencePlatform.ExperienceEvents.experienceevent.all(currentDataPackField.eventType=="commerce.saveForLaters").productListItems.all().SKU})```


>[!TIP]
> * Wählen Sie die SKU unter „Für später speichern“ im Abschnitt *Variablen durchsuchen*
> * Verwenden Sie die Vergleichsoption, wenn Sie die SKU unter „Für später speichern“ in das Ereignisfeld ablegen


Überprüfen Sie den Code in der rechten unteren Ecke des Bildschirms Segment bearbeiten unter Ereignisse. Der Code sollte wie folgt aussehen:

Code:
```(Include have at least 1 Save For Laters event where ((Stock Quantity equals 0)) THENExclude all  Purchases events where ((SKU equals Save For Laters1 SKU)) ) and occurs in last 3 month(s)```

>[!ENDTABS]

### E-Mail erstellen – Wiederauffüllung von Luma-Produkten

Benachrichtigen Sie Kunden, die einen nicht vorrätigen Artikel hinzugefügt hatten, mit einem Aufruf, jetzt einzukaufen, da der Artikel wieder auf Lager ist.



>[!TIP]
>
> Nutzen Sie das vorliegende Geschäftsereignis. Fügen Sie eine Bedingung hinzu, mit der überprüft wird, ob die SKU erneut gespeichert im Ereignistyp (beliebig) enthalten ist, der für Später gespeichert werden soll.



