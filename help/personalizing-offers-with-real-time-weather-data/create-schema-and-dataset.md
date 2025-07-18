---
title: Einrichten von XDM-Schema, Datensatz und Datenstrom in AEP
description: Erstellen von XDM-Schema, Datensatz und Datenstrom
feature: Audiences
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-06-10T00:00:00Z
recommendations: noDisplay, noCatalog
jira: KT-18258
exl-id: 1c7fe9e7-ab72-4d7b-960a-512d0e25808b
source-git-commit: 95a8abd08fbf57900870826112b01a8cd375fe96
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# Einrichten von XDM-Schema, Datensatz und Datenstrom in AEP

## XDM-Schema erstellen

Um Adobe Experience Platform Web SDK (Alloy.js) auf einer Web-Seite zu verwenden, müssen AEP-Tags mit einem Datenstrom verknüpft sein, der einem XDM-Ereignisschema zugeordnet ist. Web SDK (alloy.sendEvent) sendet Daten als Erlebnisereignisse an AEP, die einem XDM-Schema auf der Grundlage der XDM ExperienceEvent-Klasse entsprechen müssen.

So erstellen Sie ein XDM-Schema

- Bei Adobe Experience Platform anmelden
- Navigieren Sie zu _&#x200B;**Daten-Management > Schemata > Schema erstellen**&#x200B;_

- Erstellen Sie ein XDM-ereignisbasiertes Schema mit dem Namen **_Weather-Schema_**. Wenn Sie nicht mit dem Erstellen eines Schemas vertraut sind, befolgen Sie bitte diese [Dokumentation](https://experienceleague.adobe.com/de/docs/experience-platform/xdm/tutorials/create-schema-ui)


- Stellen Sie sicher, dass das Schema die folgenden Felder mit dem entsprechenden Datentyp enthält.

- ![weather-schema](assets/weather-schema.png)

- Fügen Sie die Feldergruppe _&#x200B;**Web-Details**&#x200B;_ zum Schema hinzu. Diese Feldergruppe ist für Berichtszwecke erforderlich.

## Erstellen eines Datensatzes basierend auf dem Schema

Ein **Datensatz in Adobe Experience Platform (AEP)** ist ein strukturierter Speicher-Container, mit dem Daten basierend auf einem definierten XDM-Schema aufgenommen, gespeichert und aktiviert werden.

- Navigieren Sie zu _&#x200B;**Daten-Management > Datensätze > Datensatz erstellen**&#x200B;_
- Erstellen Sie einen Datensatz mit dem Namen **_weather-schema-dataset_** basierend auf dem im vorherigen Schritt erstellten XDM _&#x200B;**Schema (**&#x200B;_ weather-schema).


## Erstellen eines Datenstroms

Ein Datenstrom in Adobe Experience Platform ist wie eine sichere Pipeline (oder Autobahn), die Ihre Website oder Ihr Programm mit Adobe-Services verbindet und es Ihnen ermöglicht, Daten einzufließen und personalisierte Inhalte zurückzufließen.

- Navigieren Sie zu _&#x200B;**Datenerfassung > Datenströme**&#x200B;_ und klicken Sie dann auf Neuer Datenstrom. Benennen des Datenstroms **wetterbezogener Datenstrom**


- Geben Sie die folgenden Details an, wie im folgenden Screenshot gezeigt
  ![Datenstrom](assets/datastream.png)
- Klicken Sie auf Speichern und dann auf Zuordnung hinzufügen und fügen Sie den Adobe Experience Platform-Service und den Ereignis-Datensatz mit aktivierten entsprechenden Kontrollkästchen hinzu
  ![datastream-mapping](assets/datastream-service.png)

- Speichern Sie den Datenstrom.
