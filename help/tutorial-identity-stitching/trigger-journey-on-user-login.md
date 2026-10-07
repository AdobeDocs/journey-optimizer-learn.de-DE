---
title: Trigger Adobe Journey Optimizer Journey mit Adobe Web SDK
description: Erfahren Sie, wie Sie eine Adobe Journey Optimizer-Journey aus Site-Ereignissen wie Benutzeranmeldungen starten, indem Sie das über Adobe Experience Platform Tags konfigurierte AEP Web SDK nutzen.
feature: Profiles
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-09-24T00:00:00.000Z
recommendations: noDisplay, noCatalog
jira: KT-19287
exl-id: c6d4f720-3780-4012-a2bd-8eae23599144
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: d2971708-e780-44bb-9e2a-72f139796afd
    internal-label: Customer
subfeature_v2:
  - id: ef9a83ca-eefa-47cf-aa34-f1a34715583a
    internal-label: Profiles
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: d4f3ee0d644b4f962763e6807f014efe132a9a05
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 10%
---
# Trigger Adobe Journey Optimizer Journey mit Adobe Web SDK

In dieser Erweiterung des Tutorials zum Identitätszuordnen wird die Adobe Journey Optimizer-Journey ausgelöst, die den angemeldeten Benutzer mithilfe seines zugeordneten Profils per E-Mail benachrichtigt. **In diesem Artikel wird davon ausgegangen, dass Sie mit dem E-Mail-Kanal und der Erstellung von Inhalten für den E-Mail-Kanal vertraut sind.**

## E-Mail-Kanal-Konfiguration erstellen

* Bei _&#x200B;**Journey Optimizer anmelden**&#x200B;_
* Navigieren Sie zu _&#x200B;**Administration -> Kanäle -> Kanalkonfiguration erstellen**&#x200B;_
* Wählen Sie **E** Mail) in der Kanalliste aus. Geben Sie einen aussagekräftigen Namen und eine Beschreibung an.
* Füllen Sie die E-Mail-Einstellungen aus.
* Geben Sie Ausführungsdetails an, wie unten dargestellt. Die E-Mail wird an die im Feld gespeicherte E-Mail-Adresse des Profils gesendet
* ![email-channel](assets/email-channel-execution.png)
* Aktivieren der E-Mail-Kanalkonfiguration

## Ereignis erstellen

* Bei _&#x200B;**Journey Optimizer anmelden**&#x200B;_
* Navigieren Sie zu _&#x200B;**Administration -> Konfigurationen**&#x200B;_
* Klicken Sie auf die Schaltfläche Verwalten auf der Karte Ereignisse und klicken Sie auf Ereignis erstellen . Geben Sie die Werte wie unten gezeigt an
* ![Journey-Ereignis](assets/journey-event1.png)

* Überprüfen, ob eventType des Ereignisses LoginEvent entspricht. Der `LoginEvent` wird im Adobe Experience Platform-Tag festgelegt.
* Ereignis speichern

## Journey erstellen

* Bei _&#x200B;**Journey Optimizer anmelden**&#x200B;_
* Navigieren Sie zu _&#x200B;**Journey-Verwaltung > Journey > Journey erstellen**&#x200B;_
* Ziehen Sie das _&#x200B;**UserLoggedIn**&#x200B;_-Ereignis auf die Arbeitsfläche
* E-Mail aus dem Aktionsmenü ziehen und ablegen. Konfigurieren Sie die E-Mail-Aktion so, dass sie die zuvor erstellte E-Mail-Kanalkonfiguration verwendet.
* Veröffentlichen Sie die Journey.

## So wird die Journey ausgelöst

Die Journey wird ausgelöst, wenn die über die Web-SDK gesendete Ereignis-Payload mit der in der Journey konfigurierten übereinstimmt. In diesem Beispiel ist das Ereignis `UserLoggedIn` Ereignistyp `LoginEvent`.

* Überprüfen Sie dies, indem Sie den Journey-Bericht anzeigen.
* ![Journey-Bericht](assets/journey-triggered-report.png)
