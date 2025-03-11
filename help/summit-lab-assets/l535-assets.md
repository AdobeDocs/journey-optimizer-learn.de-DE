---
title: L535 Cheat Sheet
description: Diese Seite enthält Text und Links, die im Summit Lab L535 verwendet werden.
feature: In App, SMS, Push, Email
doc-type: article
role: User
level: Beginner
recommendations: noDisplay, noCatalog
hide: true
hidefromtoc: true
exl-id: 1c3f4341-1293-463d-bee0-57440fcff23a
source-git-commit: fd21222a7f2560c08140585477199687cd205b73
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 22%

---

# Summit Lab L535 - Cheat Sheet

Diese Seite enthält Text und Links, die im Summit Lab L535 verwendet werden. Dadurch lässt sich der Inhalt kopieren und in die Journey Optimizer-Nachrichten einfügen.

## Links

* [SecurFinancial-Website](https://dsn.adobe.com/web/hausmann-FTTN?token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6ImFub255bW91cyIsImVtYWlsIjoiYW5vbnltb3VzQGFkb2JlLmNvbSIsIm5hbWUiOiJBbm9ueW1vdXMiLCJpc1N1cGVyVXNlciI6ZmFsc2UsImlzc3VlciI6ImhhdXNtYW5uIiwicHJvamVjdHMiOnsiaGF1c21hbm4tRlRUTiI6InZpZXcifSwiaWF0IjoxNzQwNzU2NTYxLCJleHAiOjE3NDMzNDg1NjF9.ryOTsqDH9B33436RlIo4AHFxx8aGjNEMqv9FAxLZb9U){target="_blank"}
* [Adobe Journey Optimizer](https://experience.adobe.com/#/@techmarketingdemos/sname:ajo-summit-lab/journey-optimizer/journeys){target="_blank"}
* [L535-Arbeitsmappe](/help/summit-lab-assets/assets/summit_lab_manual_l535-final-v3.pdf){target="_blank"}
* [App herunterladen](https://demo-system-next.s3.amazonaws.com/dxdemo/summit/index.html){target="_blank"}

## Kopieren und Einfügen für Übungen

### Übung 2.1 - Bei Journey Optimizer anmelden

Melden Sie sich mit den folgenden Details an:

E-Mail:    L535+*Ihre Sitznummer*@adobeeventlab.com

Kennwort:       Adobe4Summit!


### Übung 2.3 - E-Mail-Nachricht erstellen

#### Prompt

```
Generate a welcome email for new SecurFinancial customers who just opened a new checking account. 
Add a call to action to install the SecurFinancial mobile app.
```

### Übung 3.1 - Anwenden dynamischer Inhalte auf die SMS-Nachricht

#### Code

```
{%#if select _Push_details1 from profile.pushNotificationDetails where
_Push_details1.token.isNotNull()%}
Welcome to your new SecurFinancial checking account! Discover the
SecurFinancial mobile app, designed for effortless banking. Manage accounts,
transfer funds, and monitor transactions securely, anytime, anywhere. Open the
app
{%else%}
Welcome to your new SecurFinancial checking account! Discover the
SecurFinancial mobile app, designed for effortless banking. Manage accounts,
transfer funds, and monitor transactions securely, anytime, anywhere. Click here
to install the app: https://demo-systemnext.
s3.amazonaws.com/dxdemo/summit/index.html
{%/if%} 
```

### Übung 4.2 - Abwandlungen konfigurieren

#### Titel

```
Welcome to SecurFinancial
```

#### Textkörper

```
Did you know you can find an ATM near in the SecurFinancial app? Try it now!
```

#### URL

```
dxdemo://atm
```

### Übung 6 - Inhaltskarten

#### Titel

```
Welcome to SecurFinancial!
```

#### Textkörper

```
Thank you for downloading the app. You can find ATMs, track your spending and more. All within the app.
```

#### Medien-URL

```
https://demo-system-next.s3.amazonaws.com/assets/securfinancial/home-loan.jpg
```

#### Schaltflächentitel

```
Find ATMs
```

#### Ziel-URL

```
dxdemo://atm
```

## Bilder

![SecureFinancial-Logo](/help/summit-lab-assets/assets/SecureFinancial-logo.png)


![Mobiltelefon](/help/summit-lab-assets/assets/online-banking-app-01.png)


