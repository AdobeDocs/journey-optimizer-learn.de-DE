---
title: L731 Hitzbogen
description: Diese Seite enthält Text und Links, die im Summit-Lab L731 verwendet werden.
feature: In App, SMS, Push, Email
doc-type: article
role: User
level: Beginner
recommendations: noDisplay, noCatalog
hide: true
hidefromtoc: true
exl-id: ffc5e8c8-8729-4e7e-aa51-d74f91b0cf29
source-git-commit: 28da398f6813b1926c79b5cd45f415e2cfa9f40f
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 69%

---

# Summit-Lab L731 - Heizblatt

Diese Seite enthält Text und Links, die im Summit-Lab L731 verwendet werden. Dadurch lässt sich der Inhalt kopieren und in die Journey Optimizer-Nachrichten einfügen.

## Übung 1.1 - Herunterladen und Installieren der App

### iOS

![QR-Code für iOS](/help/assets/lab731-ios-qr-code.png)


## Übung 1.3: Bei Adobe Journey Optimizer anmelden

[Klicken Sie hier , um sich bei Journey Optimizer anzumelden.](https://experience.adobe.com/#/@techmarketingdemos/sname:summit-2023-ajo-lab/journey-optimizer/home)

**Anmeldedetails:**

* Benutzername: `L731+<your seat number>@summitlab.us` (Beispiel: L731+001@summitlab.us)
* Kennwort: Adobe 2023!


## Übung 2.1 – Erstellen einer In-App-Kampagne



| Feld | Text | Links |
|----|----|----|
| Kampagnenname | `<your seat number> March Vegas Campaign` |  |
| Matcher | booknow |  |
| Medien-URL-Option |  | https://mcfadyen.com/wp-content/uploads/2023/01/Adobe-Summit-2023-Banner.png |
| Titel | Es passiert live! |  |
| Textkörper | Adobe Summit kehrt vom 21.–23. März 2023 nach Las Vegas zurück. Es warten inspirierende Rednerinnen und Redner, Sessions zur Vertiefung von Kenntnissen und neue Vernetzungen. |  |
| Schaltfläche | Jetzt Hotel buchen und 10 % sparen | lab://booking?suite=presidential&amp;discount=10 |
| Schaltfläche: Interaktives Ereignis | In-App-CTA |  |
| Basis-URL |  | lab:// |



## Lektion 3 – Erstellen einer Omni-Channel-Journey

| Nachricht | Titel/Betreffzeile | Text | Link |
|----|----|----|----|----|
| Push-Benachrichtigung | Willkommen bei Vegas Stay! | Mit dem Check-in per App umgehen Sie Warteschlangen. | lab://checkin |  |
| SMS |  | Willkommen bei Vegas Stay. Mit dem Check-in per App umgehen Sie Warteschlangen: lab://checkin |  |
| email | {{profile.person.name.firstName}}, Sie sind eingecheckt, sehen Sie sich jetzt unsere Angebote für Ihren Aufenthalt an! |  |  |


Dies ist das Bild, das wir für die SMS- und die Push-Benachrichtigung verwenden:

![Online-Check-in](/help/assets/vegas_online_check_in.jpg)
