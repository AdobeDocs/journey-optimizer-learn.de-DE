---
title: Lab-Arbeitsmappe - L820 - Erstellen personalisierter Mobile-Momente mit Adobe Journey Optimizer
description: Erkunden Sie verschiedene Szenarien für Mobilgeräte und erfahren Sie, wie Sie mit Journey Optimizer personalisierte Erlebnisse für Web- und Mobilgeräte implementieren.
feature: Overview
role: User
level: Intermediate
doc-type: Tutorial
duration: 0
jira: KT-14977
thumbnail: KT-14977.jpeg
last-substantial-update: 2024-03-26T00:00:00Z
exl-id: e6d029f9-c936-427b-9d6e-4e296fd3c3ce
source-git-commit: fd50ce73503ca6b42e0171d8476ea08928ebd165
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---

# LABORARBEITSMAPPE

![Adobe Summit - ALT-Text](/help/summit-lab-2024/l820-lab-workbook/assets/adobe-summit.png "Adobe Summit")

## L820 - Erstellen personalisierter Mobile-Momente mit Adobe Journey Optimizer

In diesem praxisorientierten Labor erkunden Sie verschiedene Szenarien für Mobilgeräte und erfahren, wie Sie mit Journey Optimizer personalisierte Erlebnisse für Web- und Mobilgeräte implementieren.


>[!IMPORTANT]
>
>Bitte verzichten Sie darauf, Fotos oder Screenshots aus der Sitzung in den sozialen Medien zu posten.
><br>
>**Vertraulichkeit von Adobe**
>Die Informationen und Produktinformationen, die heute in diesem Labor veröffentlicht werden, sind vertrauliche Informationen von Adobe.
>Die Teilnehmer dürfen vertrauliche Informationen weder reproduzieren noch verwenden, verbreiten oder weitergeben.
>Produktangaben dienen nur zu Informationszwecken, stellen keine Garantie für zukünftige Funktionen dar und können jederzeit geändert werden. Daher sind solche Produktfunktionen in keiner Weise Teil Ihrer Vereinbarung mit Adobe oder anderweitig an Sie gebunden.
><br>
>**Haftungsausschluss**
>Adobe bietet Ihnen frühzeitigen Zugriff auf die Funktionen, die generative KI-Technologie nutzen. Beachten Sie, dass diese Funktionen noch in der Entwicklung sind und zu unerwarteten oder ungenauen Antworten führen können. Wir freuen uns über Ihr Feedback, da wir diese Funktion auf den Markt bringen.


### Wichtige Erkenntnisse

* Machen Sie sich mit der Vielfalt der unterstützten mobilen Erlebnisse vertraut.
* Konfigurieren Sie eine Push-Kampagne.
* Erfahren Sie, wie Sie mobile In-App-Kampagnen konfigurieren.
* Einrichten von Web-In-App-Nachrichten.
* Testen Sie Ihre eigenen personalisierten Szenarien.

### Voraussetzungen

* Ermitteln Sie Ihre Sitznummer: Sie finden Ihre Sitznummer auf dem Schreibtisch des Laborgeräts:

![Sitznummer](/help/summit-lab-2024/l820-lab-workbook/assets/locate-seat-number.png)
Sie benötigen Zugriff auf:

* [Adobe Journey Optimizer](https://experience.adobe.com/#/@techmarketingdemos/sname:summit-ajo-lab/journey-optimizer/home){target="_blank"} - Anmeldedaten werden bei den Übungen bereitgestellt.
* [Fréscopa-Website](https://dsn.adobe.com/p/adobe-summit-2024?token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6ImFub255bW91cyIsImVtYWlsIjoiYW5vbnltb3VzQGFkb2JlLmNvbSIsImlzc3VlciI6InNoYXJlZC1saW5rIiwiYXJnb24iOnsiYWNjZXNzIjoicmVhZC1wcm9qZWN0IiwicHJvamVjdElkIjoiYWRvYmUtc3VtbWl0LTIwMjQifSwiaWF0IjoxNzEwNTI0MTIwLCJleHAiOjE3MTIzMzg1MjB9.q2uGVst6HjJw8SCWl-3pViNzepkdGnNCvGqZnbbkTsY){target="_blank"}


### Anwendungsfall verstehen

Fréscopa, ein dynamisches und innovatives Unternehmen, ist darauf spezialisiert, das Kaffeeerlebnis durch seine einzigartige Mischung aus Kaffee-Abonnement-Services und einer Vielzahl von Kaffee-bezogenen Produkten, die auf seiner Website und in seiner mobilen App verfügbar sind, zu revolutionieren. Mit dem Engagement, außergewöhnliche Qualität und Geschmack zu liefern, bietet Fréscopa für Kaffeebegeisterte, die Komfort und Premium-Optionen suchen.

Der Kern des Geschäfts von Fréscopa liegt in den Kaffeeabonnements, die den Kunden eine kuratierte Auswahl an hochwertigen Bohnen direkt vor der Haustür liefern. Dieser personalisierte Ansatz stellt sicher, dass Kaffeeliebhaber ein frisches und angenehmes Erlebnis genießen können, das auf ihre Vorlieben zugeschnitten ist.

Ergänzend zu den Abonnementdiensten bieten die Website und die mobile App von Fréscopa eine umfassende Palette an Kaffeeprodukten, mit denen Kunden ihre Kaffeerituale erkunden und verbessern können. Von Braugeräten bis hin zu handwerklichen Accessoires bietet Fréscopa einen One-Stopp-Shop für Kaffeefans, die Qualität und Komfort suchen.

Fréscopas Engagement für Exzellenz geht über die Produkte hinaus, denn das Unternehmen ist bestrebt, eine nahtlose und angenehme Kunden-Journey zu schaffen. Die Kombination aus innovativen Technologien und einem kundenorientierten Ansatz positioniert Fréscopa an der Spitze der sich entwickelnden Kaffeeindustrie. Im Wesentlichen verkörpert Fréscopa die Verschmelzung von Leidenschaft und Technologie und definiert die Art und Weise, wie Menschen ihren Kaffee erleben und genießen. Mit dem Fokus auf Qualität, Bequemlichkeit und personalisierte Angebote lädt Fréscopa Kaffeebegeisterte zu einer Journey des Geschmacks ein, die direkt vor der Haustür geliefert wird.
