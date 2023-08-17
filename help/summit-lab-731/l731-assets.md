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
source-git-commit: 01869838bb08e0d7848934f345afdd54824aaa75
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 100%

---

# Summit-Lab L731 – Cheat Sheet

Diese Seite enthält Text und Links, die im Summit-Lab L731 verwendet werden. Dadurch lässt sich der Inhalt kopieren und in die Journey Optimizer-Nachrichten einfügen.

## Lektion 1.1 – Herunterladen und Installieren der App

Scannen Sie den QR-Code, um die App herunterzuladen.

>[!BEGINTABS]

>[!TAB iOS]

![QR-Code für iOS](/help/assets/lab731-ios-qr-code.png)

>[!IMPORTANT]
>
>Wenn Sie nach dem Einlöse-Code gefragt werden, schließen Sie bitte die TestFlight-App und scannen Sie den QR-Code erneut.
>
>Bitte erlauben Sie Benachrichtigungen.
>

Sie werden aufgefordert, Testflight zu installieren, Schritte 1 bis 4. Nachdem Sie Testflight installiert haben, führen Sie die Schritte 5 bis 8 aus, um die Vegas Stay App zu installieren:

<table>
<tr>
</tr>
<tr>
<td>
 <div>
      <p>
      <b>Schritt 1 </b>
      <p>
      <a>
        <img alt="Testflight 1" src="../assets/l731-ios-install/ios-install-1.png"/>
      </a>
      </div>
  </td>
  <td>
 <div>
      <p>
      <b>Schritt 2 </b>
      <p>
      <a>
        <img alt="Testflight 1" src="../assets/l731-ios-install/ios-install-2.PNG"/>
      </a>
      </div>
  </td>
  <td>
 <div>
      <p>
      <b>Schritt 3 </b>
      <p>
      <a>
        <img alt="Testflight 1" src="../assets/l731-ios-install/ios-install-3.PNG"/>
      </a>
      </div>
  </td>
  <td>
 <div>
      <p>
      <b>Schritt 4 </b>
      <p>
      <a>
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
      <a>
        <img alt="Testflight 1" src="../assets/l731-ios-install/ios-install-5.PNG"/>
      </a>
      </div>
  </td>
  <td>
 <div>
      <p>
      <a>
      <b>Schritt 6 </b>
      <p>
        <img alt="Testflight 1" src="../assets/l731-ios-install/ios-install-6.PNG"/>
      </a>
      </div>
  </td>
  <td>
 <div>
      <p>
      <a>
      <b>Schritt 7 </b>
      <p>
        <img alt="Testflight 1" src="../assets/l731-ios-install/ios-install-7.PNG"/>
      </a>
      </div>
  </td>
  <td>
 <div>
      <p>
      <a>
      <b>Schritt 8 </b>
      <p>
        <img alt="Testflight 1" src="../assets/l731-ios-install/ios-install-8.PNG"/>
      </a>
      </div>
  </td>
  </tr>
</table>

>[!TAB Android]

![QR-Code für Android](/help/assets/lab731-android-qr-code.png)

Da die App nicht im Google Play Store registriert ist, erhalten Sie eine Warnmeldung:

![Android-Warnbildschirm](/help/assets/lab731-install-android.png)

Klicken Sie auf **Trotzdem installieren**

>[!ENDTABS]

## Übung 1: Bei Adobe Journey Optimizer anmelden

[Klicken Sie hier, um sich bei Journey Optimizer anzumelden](https://experience.adobe.com/#/@techmarketingdemos/sname:summit-2023-ajo-lab/journey-optimizer/home){target="_blank"}

**Anmeldedetails**

* **Benutzername:** `L731+<your seat number>@summitlab.us` (Beispiel: L731+001@summitlab.us)
* **Kennwort:** Adobe2023!


## Übung 2 – Erstellen einer In-App-Kampagne

| Abschnitt | Feld | Text | Links |
|----|----|----|----|
| **Eigenschaften** | Kampagnenname | `<your seat number> Vegas Stay Campaign` |  |
| **Triggers** | Land | jetzt buchen |  |
| **Inhalt bearbeiten:** Medien | Medien-URL-Option |  | https://i.ibb.co/NstLhjW/Firefly-Poster-with-heading-Adobe-Max-84773.jpg |
| **Inhalt bearbeiten:** Inhalt | Titel | Holen Sie sich Ihren Frühbucherrabatt! |  |
| **Inhalt bearbeiten:** Inhalt | Textkörper | Adobe MAX kehrt nach Las Vegas zurück. Freuen Sie sich auf inspirierende Rednerinnen und Redner sowie auf Sessions, die Ihre Fähigkeiten erweitern, und auf neue Kontakte. Buchen Sie jetzt Ihre Suite und erhalten Sie 10 % Rabatt. |  |
| **Inhalt bearbeiten:** Schaltflächen | Schaltfläche | Erhalten Sie 10 % Rabatt! | lab://booking?suite=presidential&amp;discount=10 |
| **Inhalt bearbeiten:** Schaltflächen | Interaktionsereignis | In-App-CTA |  |
| **Vorschau auf Gerät** | Basis-URL für die Vorschau auf dem Gerät |  | **iOS:** lab:// <br>**Android**: https://lab |

## Lektion 3: Erstellen einer Push-Benachrichtigung

| Feld | Text | Links |
|----|----|----|
| Kampagnenname | `<your seat number> Max Push Campaign` |  |
| Titel | Hallo! |  |
| Textkörper | Wussten Sie schon, dass Adobe MAX nach Las Vegas zurückkommt? Buchen Sie jetzt Ihr Zimmer und erhalten Sie 10 % Rabatt. |  |
| Medien-URL-Option |  | https://i.ibb.co/1M0BnZn/Firefly-Big-conference-big-stage-with-ADBE-text-on-screen-40178.jpg |
