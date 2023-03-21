---
title: L731 Cheat Sheet
description: Diese Seite enthält Text und Links, die im Summit-Lab L731 verwendet werden.
feature: In App, SMS, Push, Email
doc-type: article
role: User
level: Beginner
recommendations: noDisplay, noCatalog
hide: true
hidefromtoc: true
exl-id: ffc5e8c8-8729-4e7e-aa51-d74f91b0cf29
source-git-commit: 3d39dc6e04992175331a3bf2855370359a8d4527
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 53%

---

# Summit-Lab L731 – Cheat Sheet

Diese Seite enthält Text und Links, die im Summit-Lab L731 verwendet werden. Dadurch lässt sich der Inhalt kopieren und in die Journey Optimizer-Nachrichten einfügen.

## Lektion 1.1 – Herunterladen und Installieren der App

Überprüfen Sie den QR-Code, um die App herunterzuladen.

>[!BEGINTABS]

>[!TAB iOS]

![QR-Code für iOS](/help/assets/lab731-ios-qr-code.png)

Sie werden aufgefordert, Testflight zu installieren (Schritte 1 bis 4). Nachdem Sie Testflight installiert haben, führen Sie die Schritte 5 bis 8 aus, um die Vegas Stay App zu installieren:

<table>
<tr>
</tr>
<tr>
<td>
 <div>
      <p>
      <b>Schritt 1 </b>
      <p>
      <a href="Step 1:">
        <img alt="Testflight 1" src="../assets/l731-ios-install/ios-install-1.png"/>
      </a>
      </div>
  </td>
  <td>
 <div>
      <p>
      <b>Schritt 2 </b>
      <p>
      <a href="Step 1:">
        <img alt="Testflight 1" src="../assets/l731-ios-install/ios-install-2.PNG"/>
      </a>
      </div>
  </td>
  <td>
 <div>
      <p>
      <b>Schritt 3 </b>
      <p>
      <a href="Step 1:">
        <img alt="Testflight 1" src="../assets/l731-ios-install/ios-install-3.PNG"/>
      </a>
      </div>
  </td>
  <td>
 <div>
      <p>
      <b>Schritt 4 </b>
      <p>
      <a href="Step 4">
        <img alt="Testflight 1" src="../assets/l731-ios-install/ios-install-4.PNG"/>
      </a>
      </div>
  </td>
  </tr>
  <tr>
<td>
 <div>
      <p>
      <b>Schritt 5 </b>
      <p>
      <a href="Step 1:">
        <img alt="Testflight 1" src="../assets/l731-ios-install/ios-install-5.PNG"/>
      </a>
      </div>
  </td>
  <td>
 <div>
      <p>
      <b>Schritt 6 </b>
      <p>
      <a href="Step 1:">
        <img alt="Testflight 1" src="../assets/l731-ios-install/ios-install-6.PNG"/>
      </a>
      </div>
  </td>
  <td>
 <div>
      <p>
      <b>Schritt 7 </b>
      <p>
      <a href="Step 1:">
        <img alt="Testflight 1" src="../assets/l731-ios-install/ios-install-7.PNG"/>
      </a>
      </div>
  </td>
  <td>
 <div>
      <p>
      <b>Schritt 8 </b>
      <p>
      <a href="Step 4">
        <img alt="Testflight 1" src="../assets/l731-ios-install/ios-install-8.PNG"/>
      </a>
      </div>
  </td>
  </tr>
</table>

>[!TAB Android]

![QR-Code für Android](/help/assets/lab731-android-qr-code.png)

Wenn Sie den Android-Simulator verwenden, verwenden Sie diesen Link: [https://ajolab.s3.amazonaws.com/ajolabapp-release.apk](https://ajolab.s3.amazonaws.com/ajolabapp-release.apk)

Da die App nicht beim Google Play Store registriert ist, erhalten Sie eine Warnmeldung:

![Android-Warnbildschirm](/help/assets/lab731-install-android.png)

Klicken **Installieren**

>[!ENDTABS]

## Übung 1.3: Bei Adobe Journey Optimizer anmelden

[Klicken Sie hier, um sich bei Journey Optimizer anzumelden](https://experience.adobe.com/#/@techmarketingdemos/sname:summit-2023-ajo-lab/journey-optimizer/home)

**Anmeldedetails:**

* **Benutzername:** `L731+<your seat number>@summitlab.us` (Beispiel: L731+001@summitlab.us)
* **Kennwort:** Adobe 2023!


## Übung 2.1 – Erstellen einer In-App-Kampagne

| Feld | Text | Links |
|----|----|----|
| Kampagnenname | `<your seat number> March Vegas Campaign` |  |
| Matcher | jetzt buchen |  |
| Medien-URL-Option |  | https://mcfadyen.com/wp-content/uploads/2023/01/Adobe-Summit-2023-Banner.png |
| Titel | Es ist Happening &amp; es ist Live! |  |
| Textkörper | Adobe Summit kehrt vom 21.–23. März 2023 nach Las Vegas zurück. Es warten inspirierende Rednerinnen und Redner, Sessions zur Vertiefung von Kenntnissen und neue Vernetzungen. |  |
| Schaltfläche | Jetzt Hotel buchen und 10 % sparen | lab://booking?suite=presidential&amp;discount=10 |
| Schaltfläche: Interaktives Ereignis | In-App-CTA |  |
| Basis-URL |  | iOS: lab:// <br>Android&amp;: https://lab |


## Lektion 3 – Erstellen einer Omni-Channel-Journey

**Journey Label:**
`<your seat number>` - Willkommens-Journey

>[!BEGINTABS]

>[!TAB Push-Nachricht]

**Titel:**
Willkommensnachricht

**Titel:**\
Willkommen bei Vegas Stay!

**Textkörper:**\
Mit dem Check-in per App umgehen Sie Warteschlangen.

**Deeplink:** lab://checkin

**Medien:**

https://experienceleague.adobe.com/docs/journey-optimizer-learn/assets/vegas_online_check_in.jpg?lang=en


Dies ist das Bild, das wir für die Push-Benachrichtigung verwenden:

![Online-Check-in](/help/assets/vegas_online_check_in.jpg)

>[!TAB SMS-Nachricht]

**Titel:**
Willkommensnachricht

**Nachricht:**
Willkommen bei Vegas Stay. Mit dem Check-in per App umgehen Sie Warteschlangen: lab://checkin

>[!TAB E-Mail-Nachricht]

**Titel:**
Bestätigungsnachricht

**Betreffzeile:**
{{profile.person.name.firstName}}, Sie sind eingecheckt, sehen Sie sich jetzt unsere Angebote für Ihren Aufenthalt an!

>[!ENDTABS]
