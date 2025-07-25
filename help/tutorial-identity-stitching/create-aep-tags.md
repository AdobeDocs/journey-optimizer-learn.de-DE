---
title: Senden von CRMID an Adobe Experience Platform
description: Erstellen Sie Adobe Experience Platform-Tags, um die vom Browser empfangene CRMID an Adobe Experience Platform zu senden.
feature: Profiles
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-19T00:00:00Z
recommendations: noDisplay, noCatalog
jira: KT-18089
exl-id: 894ad6b7-c4b4-465e-8535-3fdcd77e00eb
source-git-commit: 40690024e5348dd3ac05f350e49a67a99d5e455e
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 10%

---

# Senden von CRMID an Adobe Experience Platform

Adobe Experience Platform Tags wird verwendet, um die CRMID an Adobe Experience Platform (AEP) zu senden, da sie einen flexiblen, ereignisgesteuerten Mechanismus zur Übertragung von Identitätsdaten direkt aus dem Browser bietet. Durch das Senden der CRMID nach der Benutzeranmeldung kann AEP die anonyme ECID mit dem bekannten CRM-Profil verknüpfen, was eine genaue Identitätszuordnung ermöglicht. Diese Verknüpfung bildet die Grundlage für die Erstellung einheitlicher Kundenprofile, die Qualifizierung von Zielgruppen und die Bereitstellung personalisierter Erlebnisse in Echtzeit in Adobe Journey Optimizer (AJO).

Eine Experience Platform Tags-Eigenschaft _**FinWise**_ wird erstellt. Die folgenden Erweiterungen wurden der Tags-Eigenschaft hinzugefügt

![tags-extensions](assets/tags-extensions.png)

Konfigurieren Sie die AEP Web SDK-Erweiterung mit dem im vorherigen Schritt erstellten DataStream von Financial Advisors .
Der Experience Cloud ID-Dienst ist eine optionale Erweiterung, die der Tag-Eigenschaft zu Debugging-Zwecken hinzugefügt wird.

## Tag-Datenelemente

Erstellen Sie die folgenden Datenelemente

| Datenelement | Erweiterung | Datenelementtyp | Benutzerdefinierte Einstellungen |
|--------------|-----------------------------------|---------------------------|----------------------------------------|
| crmid | Adobe Client-Datenschicht | Berechneter Status der Datenschicht | user.crmid |
| ECID | Experience Cloud ID Service | ECID |                                        |
| identität | Adobe Experience Platform Web SDK | Identitätszuordnung | ![Bild](assets/identity-settings.png) |
| XDMVariable | Adobe Experience Platform Web SDK | Variable | ![Bild](assets/xdmvariable.png) |

## Regel erstellen

Erstellen Sie eine Regel mit dem Namen userLoggedIn mit dem folgenden Ereignis und den folgenden Aktionen

Ereignis
![event](assets/data-pushed-event.png)

Aktion „Variable aktualisieren“
![update-variable](assets/update-variable.png)
Ereignisaktion senden
![send-event](assets/send-event.png)

## Speichern und erstellen

Speichern Sie Ihre Änderungen, erstellen Sie die Bibliothek und erstellen Sie sie.
