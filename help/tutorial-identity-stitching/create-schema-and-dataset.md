---
title: Einrichten von XDM-Schema, Datensatz und Datenstrom in AEP
description: Erstellen von XDM-Schema, Datensatz und Datenstrom
feature: Audiences
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-04-30T00:00:00.000Z
recommendations: noDisplay, noCatalog
jira: KT-18089
exl-id: 8bb85ba7-3c50-4596-88f8-e112c48a8253
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: d2971708-e780-44bb-9e2a-72f139796afd
    internal-label: Customer
subfeature_v2:
  - id: b32bb433-f8c6-4931-8e52-e657230a3bf2
    internal-label: Audiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: d4f3ee0d644b4f962763e6807f014efe132a9a05
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 0%
---
# Einrichten von XDM-Schema, Datensatz und Datenstrom in AEP

## XDM-Schema erstellen

Um Adobe Experience Platform Web SDK (Alloy.js) auf einer Web-Seite zu verwenden, müssen AEP-Tags mit einem Datenstrom verknüpft sein, der einem XDM-Ereignisschema zugeordnet ist. Web SDK (alloy.sendEvent) sendet Daten als Erlebnisereignisse an AEP, die einem XDM-Schema auf der Grundlage der XDM ExperienceEvent-Klasse entsprechen müssen.

So erstellen Sie ein XDM-Schema

* Bei Adobe Experience Platform anmelden
* Daten-Management -> Schemata -> Schema erstellen

* Erstellen Sie ein XDM-ereignisbasiertes Schema namens **_Financial Advisors_**. Wenn Sie nicht mit dem Erstellen eines Schemas vertraut sind, befolgen Sie bitte diese [Dokumentation](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/tutorials/create-schema-ui)


* Stellen Sie sicher, dass das Schema für das Profil aktiviert ist.

## Erstellen eines Datensatzes basierend auf dem Schema

Ein **Datensatz in Adobe Experience Platform (AEP)** ist ein strukturierter Speicher-Container, mit dem Daten basierend auf einem definierten XDM-Schema aufgenommen, gespeichert und aktiviert werden.


* Daten-Management -> Datensätze -> Datensatz erstellen
* Erstellen Sie einen Datensatz mit **_Namen „Finanzberater_** Datensatz“ basierend auf dem im vorherigen Schritt erstellten XDM-Schema (Finanzberater).

* Stellen Sie sicher, dass der Datensatz für das Profil aktiviert ist

## Erstellen eines Datenstroms

Ein Datenstrom in Adobe Experience Platform ist wie eine sichere Pipeline (oder Autobahn), die Ihre Website oder Ihr Programm mit Adobe-Services verbindet und es Ihnen ermöglicht, Daten einzufließen und personalisierte Inhalte zurückzufließen.

* Navigieren Sie zu Datenerfassung > Datenströme und klicken Sie dann auf Neuer Datenstrom. Benennen des Datenstroms **_Financial Advisors DataStream_**

* Geben Sie die folgenden Details an, wie im folgenden Screenshot gezeigt
  ![Datenstrom](assets/datastream.png)
* Klicken Sie auf Speichern und dann auf Zuordnung hinzufügen und fügen Sie den Adobe Experience Platform-Service und den Ereignis-Datensatz wie abgebildet hinzu
  ![datastream-mapping](assets/datastream-service.png)

* Wählen Sie den entsprechenden (zuvor erstellten) Ereignis-Datensatz aus.

* Speichern Sie den Datenstrom.
