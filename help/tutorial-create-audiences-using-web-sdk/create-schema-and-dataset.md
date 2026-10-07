---
title: Einrichten von XDM-Schema, Datensatz und Datenstrom in AEP
description: Erstellen von XDM-Schema, Datensatz und Datenstrom
feature: Audiences
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-04-30T00:00:00.000Z
jira: KT-17923
exl-id: 0efa418a-5b4f-4012-a6fc-afaa34a59285
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
source-wordcount: '284'
ht-degree: 0%
---
# Einrichten von XDM-Schema, Datensatz und Datenstrom in AEP

## XDM-Schema erstellen

* Bei Adobe Experience Platform anmelden
* Daten-Management -> Schemata -> Schema erstellen

* Erstellen Sie ein XDM-ereignisbasiertes Schema namens _Financial Advisors_. Wenn Sie nicht mit dem Erstellen eines Schemas vertraut sind, befolgen Sie bitte diese [Dokumentation](https://experienceleague.adobe.com/de/docs/experience-platform/xdm/tutorials/create-schema-ui)

* Fügen Sie Ihrem Schema die folgende Struktur hinzu. Das PreferredFinancialInstrument-Element speichert die Voreinstellungen des Benutzers für Aktien, Anleihen, CD. Die **__techmarketingdemos_**&#x200B;ist die Mandanten-ID und unterscheidet sich in Ihrer Umgebung.
  ![xdm-schema](assets/xdm-schema.png)

* Für das PreferredFinancialInstrument-Element sind Aufzählungswerte wie unten dargestellt definiert
  ![enum-values](assets/enum-values.png)

* Stellen Sie sicher, dass das Schema für das Profil aktiviert ist.

## Erstellen eines Datensatzes basierend auf dem Schema

Ein **Datensatz in Adobe Experience Platform (AEP)** ist ein strukturierter Speicher-Container, mit dem Daten basierend auf einem definierten XDM-Schema aufgenommen, gespeichert und aktiviert werden.


* Daten-Management -> Datensätze -> Datensatz erstellen
* Erstellen Sie einen Datensatz mit _Namen „Finanzberater_ Datensatz“ basierend auf dem im vorherigen Schritt erstellten XDM-Schema (Finanzberater).

* Stellen Sie sicher, dass der Datensatz für das Profil aktiviert ist

## Erstellen eines Datenstroms

Ein Datenstrom in Adobe Experience Platform ist wie eine sichere Pipeline (oder Autobahn), die Ihre Website oder Ihr Programm mit Adobe-Services verbindet und es Ihnen ermöglicht, Daten einzufließen und personalisierte Inhalte zurückzufließen.

* Datenerfassung > Datenströme und klicken Sie dann auf Neuer Datenstrom. Benennen des Datenstroms _Financial Advisors DataStream_

* Geben Sie die folgenden Details an, wie im folgenden Screenshot gezeigt
  ![Datenstrom](assets/datastream.png)
* Klicken Sie auf Speichern und dann auf Zuordnung hinzufügen und fügen Sie den Adobe Experience Platform-Service und den Ereignis-Datensatz wie abgebildet hinzu
  ![datastream-mapping](assets/datastream-service.png)

* Wählen Sie den entsprechenden (zuvor erstellten) Ereignis-Datensatz aus.

* Speichern des Datenstroms

