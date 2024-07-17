---
title: 'Herausforderung: Produktauffüllung'
description: Wenden Sie Ihr erworbenes Wissen über das Erstellen von Segmenten an und testen Sie Ihre Fähigkeiten.
jira: KT-8417
feature: Segments
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 305aaf4c-7f5d-4f6f-abeb-466208f1fe48
source-git-commit: 5c763ec877c75c07132f4cc714d63695e12638dc
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 100%

---

# Herausforderung: Produktauffüllung

| Herausforderung | Produktauffüllung |
|---|---|
| Persona | Journey-Manager |
| Erforderliche Fähigkeiten | <ul><li>[Erstellen von Segmenten](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/profiles-segments-subscriptions/create-segments.html?lang=de)</li><li> [Importieren und Erstellen von HTML-E-Mail-Inhalten](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/email-channel/import-and-author-html-email-content.html?lang=de)</li><li>[Anwendungsfall: Segment lesen](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/use-case-read-segment.html?lang=de)</li> |
| Herunterzuladende Assets | [E-Mail-Datei zur Wiederverfügbarkeit von Produkten](/help/challenges/assets/email-assets/ProductRestockEmail.html.zip) |

## Die Story

Beim Surfen auf der Luma-Website können die Kundinnen und Kunden Produkte, die sie interessieren, einer Wunschliste hinzufügen, was es Luma ermöglicht, ihnen gezielte Marketing-Nachrichten und -Informationen über die Produkte zu senden.

## Ihre Herausforderung

Luma bittet Sie, eine Journey in Journey Optimizer zu implementieren. Diese benachrichtigt Kundinnen und Kunden, die einen vergriffenen Artikel auf ihrer Wunschliste haben, wenn dieser Artikel wieder vorrätig ist. Das Kreativ-Team stellt Ihnen die [E-Mail zur Wiederverfügbarkeit von Produkten](/help/challenges/assets/email-assets/ProductRestockEmail.html.zip) zur Verfügung.

>[!BEGINTABS]

>[!TAB Aufgabe]

## 1. Definieren Sie das Segment – Nicht vorrätige Artikel auf der Wunschliste

Um potenziell interessierte Kundinnen und Kunden anzusprechen, wenn Produkte wieder vorrätig sind, erstellen Sie eine Zielgruppe, die aus Kundinnen und Kunden besteht, die:

* mindestens einen Artikel zu ihrer Wunschliste hinzugefügt haben (Verwenden Sie den Ereignistyp: [!UICONTROL Commerce – für später speichern])
* Welche in den letzten Monaten nicht vorrätig waren (verwenden Sie Lagermenge = 0)
* Und den Artikel seitdem nicht gekauft haben.

>[!TIP]
>Schließen Sie alle „Einkäufe“-Ereignistypen aus, bei denen die SKU mit der SKU aus dem Ereignis *Für später speichern* übereinstimmt. Sie finden das Feld im Abschnitt *Variablen durchsuchen*.

Benennen Sie dieses Segment: `Out-of-stock-Wishlist`


### 2. Erstellen Sie die Journey – Benachrichtigung zur Wiederverfügbarkeit des Produkts

Wenn ein zuvor nicht vorrätiger Artikel wieder auf Lager ist, benachrichtigen Sie Kundinnen und Kunden, die einen nicht vorrätigen Artikel hinzugefügt hatten, mit einem Aufruf, jetzt einzukaufen, da der Artikel wieder auf Lager ist.

1. Rufen Sie die Journey auf: `Product Restock`
2. Die Journey sollte ausgelöst werden, wenn ein Produkt wieder auf Lager ist
3. Senden Sie die *E-Mail zur Wiederverfügbarkeit des Produkts* an
4. Benutzende, die diesen Artikel ihrer Wunschliste hinzugefügt haben, während er nicht vorrätig war.

>[!TAB Erfolgskriterien]

Testen Sie Ihre Journey:

1. Stellen Sie sicher, dass das Lesesegment-Ereignis den Namespace = `Luma CRM ID` hat.
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

Überprüfen Sie den Code in der rechten unteren Ecke des Bildschirms „Segment bearbeiten“ unter „Ereignisse“. Der Code sollte wie folgt aussehen:

Code:
```(Include have at least 1 Save For Laters event where ((Stock Quantity equals 0)) THENExclude all  Purchases events where ((SKU equals Save For Laters1 SKU)) ) and occurs in last 3 month(s)```

>[!ENDTABS]

### E-Mail erstellen – Wiederauffüllung von Luma-Produkten

Benachrichtigen Sie Kunden, die einen nicht vorrätigen Artikel hinzugefügt hatten, mit einem Aufruf, jetzt einzukaufen, da der Artikel wieder auf Lager ist.



>[!TIP]
>
> Nutzen Sie das vorliegende Geschäftsereignis. Sie müssen eine Bedingung hinzufügen, mit der überprüft wird, ob die SKU für die Wiederverfügbarkeit in einem (beliebigen) Ereignistyp enthalten ist, der für später gespeichert wird.
>




