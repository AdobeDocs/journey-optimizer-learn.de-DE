---
title: Erstellen von Adobe Experience Platform-Tags
description: Erstellen von AJO-Zielgruppen anhand der Voreinstellungen für Benutzerinvestitionen (Aktien, Anleihen, CDs)
feature: Audiences
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-04-30T00:00:00.000Z
recommendations: noDisplay, noCatalog
jira: KT-18258
exl-id: 04fad076-e897-4831-9147-768721858a80
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
source-wordcount: '286'
ht-degree: 0%
---
# Erstellen von Adobe Experience Platform-Tags

Adobe Experience Platform-Tags (ehemals Adobe Launch) helfen bei der Verwaltung und Bereitstellung von Marketing- und Analysetechnologien* auf Ihrer Website, ohne den Code der Website ändern zu müssen.

In [ Video wird der Prozess der Erstellung von Adobe Experience Tags beschrieben](https://experienceleague.adobe.com/en/playlists/experience-platform-get-started-with-tags)

* Bei Datenerfassung anmelden
* Klicken Sie auf _**Tags -> Neue Eigenschaft**
* Erstellen Sie ein Adobe Experience Platform-Tag _**Personalisierung bei Wetter**_.
* Fügen Sie die folgenden Erweiterungen zum -Tag hinzu

![tags-extensions](assets/tags-extensions1.png)

* Fügen Sie ein Datenelement mit dem Namen „ECID“ hinzu, wie unten dargestellt. Dieses Datenelement wird später im Reporting verwendet

![ecid-data-element](assets/ecid-data-element.png)

* Stellen Sie sicher, dass Sie Adobe Experience Platform Web SDK so konfigurieren, dass die richtige Umgebung und der **wetterbezogene Datenstrom** verwendet werden, die im vorherigen Schritt erstellt wurden.

![web-sdk-configuration](assets/tags-extensions.png)



## Erstellen und Bereitstellen der AEP-Tags


Erstellen Sie eine neue Bibliothek und fügen Sie ihr alle geänderten Ressourcen hinzu, wie in den folgenden Screenshots dargestellt.

**Bibliothek hinzufügen**

![new-library](assets/tag-add-library.png)

**Bibliothek erstellen**

Geben Sie im Bildschirm Bibliothek erstellen den Bibliotheksnamen und die Umgebung an.

Alle geänderten Ressourcen zu dieser Bibliothek hinzufügen
![tag-library](assets/tag-build-library.png)

Klicken Sie dann auf die Schaltfläche Speichern und in Entwicklung erstellen , um die Bibliothek zu erstellen

## AEP-Tags in die HTML-Seite einschließen

Wenn Sie eine AEP Tags-Eigenschaft veröffentlichen, erhalten Sie von Adobe ein Skript-Tag, das Sie in Ihrem HTML-` <head>` oder am Ende der ` <body>` Tags platzieren müssen.

1. Navigieren Sie zur Eigenschaft Tags (Personalisierung bei Wetter) .
2. Klicken Sie auf Umgebungen und dann auf das Symbol Installieren der gewünschten Umgebung (z. B. Entwicklung, Staging, Produktion).
3. Notieren Sie sich den eingebetteten Code. Dies ist in einer späteren Phase dieses Tutorials erforderlich.
