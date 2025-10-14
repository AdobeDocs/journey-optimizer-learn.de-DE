---
title: Trigger Adobe Journey Optimizer Journey mit Adobe Web SDK
description: Erfahren Sie, wie Sie eine Adobe Journey Optimizer-Journey aus Site-Ereignissen wie Benutzeranmeldungen starten, indem Sie die über Adobe Experience Platform Tags konfigurierte AEP Web SDK nutzen
feature: Profiles
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-09-24T00:00:00Z
recommendations: noDisplay, noCatalog
jira: KT-19287
source-git-commit: 6927cade07790603e711f4e6e4c3f6982a56e6f5
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---

# Trigger Adobe Journey Optimizer Journey mit Adobe Web SDK

In dieser Erweiterung des Tutorials zum Identitätszuordnen wird die Adobe Journey Optimizer-Journey ausgelöst, die den angemeldeten Benutzer mithilfe seines zugeordneten Profils per E-Mail benachrichtigt. **In diesem Artikel wird davon ausgegangen, dass Sie mit dem E-Mail-Kanal und der Erstellung von Inhalten für den E-Mail-Kanal vertraut sind.**

## E-Mail-Kanal-Konfiguration erstellen

* Bei _**Journey Optimizer anmelden**_
* Navigieren Sie zu _**Administration -> Kanäle -> Kanalkonfiguration erstellen**_
* Wählen Sie **E** Mail) in der Kanalliste aus. Geben Sie einen aussagekräftigen Namen und eine Beschreibung an.
* Füllen Sie die E-Mail-Einstellungen aus.
* Geben Sie Ausführungsdetails an, wie unten dargestellt. Die E-Mail wird an die im Feld gespeicherte E-Mail-Adresse des Profils gesendet
* ![email-channel](assets/email-channel-execution.png)
* Aktivieren der E-Mail-Kanalkonfiguration

## Ereignis erstellen

* Bei _**Journey Optimizer anmelden**_
* Navigieren Sie zu _**Administration -> Konfigurationen**_
* Klicken Sie auf die Schaltfläche Verwalten auf der Karte Ereignisse und klicken Sie auf Ereignis erstellen . Geben Sie die Werte wie unten gezeigt an
* ![Journey-Ereignis](assets/journey-event1.png)

* Überprüfen, ob eventType des Ereignisses LoginEvent entspricht. Der `LoginEvent` wird im Adobe Experience Platform-Tag festgelegt.
* Ereignis speichern

## Journey erstellen

* Bei _**Journey Optimizer anmelden**_
* Navigieren Sie zu _**Journey-Verwaltung > Journey > Journey erstellen**_
* Ziehen Sie das _**UserLoggedIn**_-Ereignis auf die Arbeitsfläche
* E-Mail aus dem Aktionsmenü ziehen und ablegen. Konfigurieren Sie die E-Mail-Aktion so, dass sie die zuvor erstellte E-Mail-Kanalkonfiguration verwendet.
* Veröffentlichen Sie die Journey.

## So wird die Journey ausgelöst

Die Journey wird ausgelöst, wenn die über die Web-SDK gesendete Ereignis-Payload mit der in der Journey konfigurierten übereinstimmt. In diesem Beispiel ist das Ereignis `UserLoggedIn` Ereignistyp `LoginEvent`.

* Überprüfen Sie dies, indem Sie den Journey-Bericht anzeigen.
* ![Journey-Bericht](assets/journey-triggered-report.png)




