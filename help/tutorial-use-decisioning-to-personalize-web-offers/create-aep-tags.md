---
title: Erstellen von Adobe Experience Platform-Tags
description: Erstellen von AJO-Zielgruppen anhand der Voreinstellungen für Benutzerinvestitionen (Aktien, Anleihen, CDs)
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-05T00:00:00.000Z
recommendations: noDisplay, noCatalog
jira: KT-17923
exl-id: 6823ce13-bc77-4e2b-89e0-606e403c15f2
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: a984631b-2bae-4860-9b15-69c41a799dcb
    internal-label: APIs and SDKs
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
    internal-label: Decisioning API
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: d4f3ee0d644b4f962763e6807f014efe132a9a05
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%
---
# Erstellen von Adobe Experience Platform-Tags

Experience Platform-Tags werden auf der Web-Seite so konfiguriert, dass sie die Adobe Experience Platform Web SDK laden, wodurch der sendEvent-API-Aufruf an den Trigger personalisierte Erlebnisse ermöglicht wird. Dadurch wird sichergestellt, dass die erforderlichen Client-seitigen Bibliotheken korrekt initialisiert werden, sodass für die Angebotsbereitstellung eine Echtzeit-Interaktion mit Adobe Journey Optimizer möglich ist.

1. Bei der Datenerfassung anmelden.
1. Klicken Sie auf **[!UICONTROL Tags]** > **[!UICONTROL Neue Eigenschaft]**.
1. Erstellen Sie ein Adobe Experience Platform-Tag namens ECID-Service.
1. Fügen Sie die folgenden Erweiterungen zum -Tag hinzu:

   ![tags-extensions](assets/ecid-tag.png)

1. Konfigurieren Sie Adobe Experience Platform Web SDK so, dass die richtige Umgebung und der im vorherigen Tutorial erstellte Datenstrom für Finanzberater verwendet werden.

   ![web-sdk-configuration](assets/web-sdk-configuration.png)

Für die Adobe Client-Datenschicht und die Haupterweiterungen ist keine zusätzliche Konfiguration erforderlich

## Datenelement erstellen

Das ECID-Datenelement in Experience Platform Tags wird ausschließlich zu Debugging- und Testzwecken erstellt. Mit dem Datenelement können Entwicklerinnen und Entwickler die Experience Cloud-ID anzeigen, die der Browser-Sitzung eines Benutzers zugewiesen wurde. Dies kann dazu beitragen, die Identitätszuordnung zu überprüfen und sicherzustellen, dass die `sendEvent`-Aufrufe mit dem richtigen Profil verknüpft sind. Dieses Element ist nicht erforderlich, damit die Personalisierung funktioniert, ist aber bei der Implementierung und Qualitätssicherung nützlich

![ECID](assets/ecid-data-element.png)


## AEP-Tags in die HTML-Seite einschließen

Erstellen und veröffentlichen Sie die Adobe Experience Platform-Tags.

Wenn eine AEP Tags-Eigenschaft veröffentlicht wird, stellt Adobe Ihnen ein Skript-Tag zur Verfügung, das Sie in Ihrem HTML-`<head>` oder am Ende der `<body>` Tags platzieren müssen.

1. Wechseln Sie zu Ihrer Eigenschaft „Tags (ECID-Service)“.

1. Klicken Sie auf Umgebungen und dann auf das Symbol Installieren der gewünschten Umgebung (z. B. Entwicklung, Staging, Produktion).

1. Beachten Sie den eingebetteten Code.

   Dieser Code muss unmittelbar vor dem schließenden -Tag `</body>` der HTML-Seite platziert werden.
