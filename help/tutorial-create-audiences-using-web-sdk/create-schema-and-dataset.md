---
title: Einrichten von XDM-Schema, Datensatz und Datenstrom in AEP
description: Erstellen von XDM-Schema, Datensatz und Datenstrom
feature: Audiences
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-04-30T00:00:00Z
jira: KT-17923
exl-id: 0efa418a-5b4f-4012-a6fc-afaa34a59285
source-git-commit: 15b2379c251ed0d7583a01fb6af67815322456cf
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# Einrichten von XDM-Schema, Datensatz und Datenstrom in AEP

## XDM-Schema erstellen

* Bei Adobe Experience Platform anmelden
* Daten-Management -> Schemata -> Schema erstellen

* Erstellen Sie ein XDM-ereignisbasiertes Schema namens _Financial Advisors_. Wenn Sie nicht mit dem Erstellen eines Schemas vertraut sind, befolgen Sie bitte diese [Dokumentation](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/tutorials/create-schema-ui)

* Fügen Sie Ihrem Schema die folgende Struktur hinzu. Das PreferredFinancialInstrument-Element speichert die Voreinstellungen des Benutzers für Aktien, Anleihen, CD. Die **__techmarketingdemos_**ist die Mandanten-ID und unterscheidet sich in Ihrer Umgebung.
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

