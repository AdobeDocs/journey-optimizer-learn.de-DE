---
title: Lab-Arbeitsmappe - L820 - Erstellen personalisierter Mobile Momente mit Adobe Journey Optimizer
description: Erfahren Sie mehr über verschiedene Szenarien für Mobilgeräte und erfahren Sie, wie Sie mit Journey Optimizer personalisierte Erlebnisse für Web und Mobilgeräte implementieren.
feature: Overview
role: User
level: Intermediate
doc-type: Tutorial
duration: 0
jira: KT-14977
thumbnail: KT-14977.jpeg
last-substantial-update: 2024-03-26T00:00:00Z
exl-id: e6d029f9-c936-427b-9d6e-4e296fd3c3ce
source-git-commit: b4eb509d50afeea02eac937be85643aa22370249
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---

# LAB-ARBEITSMAPPE

![Adobe Summit - alt text](/help/summit/l820-lab-workbook/assets/adobe-summit.png "Adobe Summit")

## L820 - Erstellen personalisierter Mobile Momente mit Adobe Journey Optimizer

In diesem praxisorientierten Labor werden verschiedene Szenarien für Mobilgeräte untersucht und erfahren, wie Sie mit Journey Optimizer personalisierte Erlebnisse für Web und Mobilgeräte implementieren.


>[!IMPORTANT]
>
>Vermeiden Sie es, Fotos oder Screenshots aus der Sitzung in Social Media zu veröffentlichen.
><br>
>**Adobe Confidential**
>Die Informationen und Produktangaben, die heute in diesem Labor veröffentlicht werden, sind Adobe Vertraulichkeitsinformationen.
>Die Teilnehmer dürfen vertrauliche Informationen weder reproduzieren, verwenden, verbreiten noch an andere Personen oder Einrichtungen weitergeben.
>Produktangaben dienen nur zu Informationszwecken, sind keine Garantie für zukünftige Funktionen und können jederzeit geändert werden. Daher sind solche Produktmerkmale oder -funktionalitäten in keiner Weise Bestandteil Ihrer Vereinbarung mit Adobe oder anderweitig an Sie gebunden.
><br>
>**Haftungsausschluss**
>Adobe bietet Ihnen frühzeitigen Zugriff auf die Funktionen, die generative KI-Technologie nutzen. Bitte beachten Sie, dass diese Funktionen noch in der Entwicklung sind und Antworten hervorrufen können, die unerwartet oder ungenau sind. Wir freuen uns über Ihr Feedback, da wir diese Funktion auf den Markt bringen.


### Wichtige Schritte

* Machen Sie sich mit der Vielfalt der unterstützten mobilen Erlebnisse vertraut.
* Push-Kampagnen konfigurieren
* Erfahren Sie, wie Sie mobile In-App-Kampagnen konfigurieren.
* Richten Sie Web-In-App-Nachrichten ein.
* Testen Sie Ihre eigenen personalisierten Szenarien.

### Voraussetzungen

* Ihre Sitznummer kennen: Sie finden Ihre Sitznummer auf der Tischplatte der Labormaschine:

![Sitznummer](/help/summit/l820-lab-workbook/assets/locate-seat-number.png)
Sie benötigen Zugriff auf:

* [Adobe Journey Optimizer](https://experience.adobe.com/#/@techmarketingdemos/sname:summit-ajo-lab/journey-optimizer/home){target="_blank"} - Anmeldedetails werden während der Übungen bereitgestellt.
* [Fréscopa-Website](https://dsn.adobe.com/p/adobe-summit-2024?token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6ImFub255bW91cyIsImVtYWlsIjoiYW5vbnltb3VzQGFkb2JlLmNvbSIsImlzc3VlciI6InNoYXJlZC1saW5rIiwiYXJnb24iOnsiYWNjZXNzIjoicmVhZC1wcm9qZWN0IiwicHJvamVjdElkIjoiYWRvYmUtc3VtbWl0LTIwMjQifSwiaWF0IjoxNzEwNTI0MTIwLCJleHAiOjE3MTIzMzg1MjB9.q2uGVst6HjJw8SCWl-3pViNzepkdGnNCvGqZnbbkTsY){target="_blank"}


### Anwendungsfall verstehen

Fréscopa, ein dynamisches und innovatives Unternehmen, hat sich auf die Revolutionierung des Kaffeeerlebnisses spezialisiert, indem es eine einzigartige Mischung aus Kaffee-Abonnement-Dienstleistungen und einer vielfältigen Auswahl an Kaffee-bezogenen Produkten auf seiner Website und in seiner mobilen Anwendung bereitstellt. Fréscopa ist ein Unternehmen, das sich für hervorragende Qualität und Geschmack einsetzt und sich für Kaffeefans einsetzt, die auf der Suche nach Komfort und erstklassigen Optionen sind.

Das Kerngeschäft von Fréscopa liegt in der Bereitstellung von Kaffee-Abonnements, die den Kunden eine kuratierte Auswahl an hochwertigen Bohnen bieten, die direkt vor der Haustür geliefert werden. Dieser personalisierte Ansatz sorgt dafür, dass Kaffeeliebhaber ein frisches und angenehmes Erlebnis genießen können, das auf ihre Wünsche zugeschnitten ist.

Ergänzend zu seinen Abonnementdiensten bieten die Website und die mobile App von Fréscopa eine umfassende Palette von Kaffee-bezogenen Produkten, die es Kunden ermöglichen, ihre Kaffeerituale zu erkunden und zu verbessern. Vom Braugerät bis zum handwerklichen Zubehör bietet Fréscopa eine zentrale Anlaufstelle für Kaffeeempfänger, die nach Qualität und Komfort suchen.

Fréscopas Engagement für Exzellenz geht über seine Produkte hinaus, da das Unternehmen sich der Schaffung einer nahtlosen und genussvollen Journey widmet. Durch die Kombination innovativer Technologien und einen kundenorientierten Ansatz steht Fréscopa an der Spitze der sich entwickelnden Kaffeebranche. Im Wesentlichen verkörpert Fréscopa die Fusion von Leidenschaft und Technologie, indem es die Art und Weise neu definiert, wie Einzelpersonen ihren Kaffee genießen und erleben. Fréscopa lädt Kaffeefreunde mit einem Schwerpunkt auf Qualität, Komfort und personalisierten Angeboten zu einem Journey des Geschmacks ein, das direkt vor der Haustür geliefert wird.
