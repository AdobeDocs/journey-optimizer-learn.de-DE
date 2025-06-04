---
title: Erstellen von Adobe Experience Platform-Tags
description: Erstellen von AJO-Zielgruppen anhand der Voreinstellungen für Benutzerinvestitionen (Aktien, Anleihen, CDs)
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-05T00:00:00Z
recommendations: noDisplay, noCatalog
jira: KT-17923
exl-id: 6823ce13-bc77-4e2b-89e0-606e403c15f2
source-git-commit: 82d82b3aac2bf91e259b01fd8c6b4d6065f9640a
workflow-type: tm+mt
source-wordcount: '286'
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

Das ECID-Datenelement in Experience Platform Tags wird ausschließlich zu Debugging- und Testzwecken erstellt. Mit dem Datenelement können Entwicklerinnen und Entwickler die Experience Cloud-ID anzeigen, die der Browser-Sitzung einer Benutzerin oder eines Benutzers zugewiesen wurde. Dies kann dazu beitragen, die Identitätszuordnung zu überprüfen und sicherzustellen, dass die `sendEvent`-Aufrufe mit dem richtigen Profil verknüpft sind. Dieses Element ist nicht erforderlich, damit die Personalisierung funktioniert, ist aber bei der Implementierung und Qualitätssicherung nützlich

![ECID](assets/ecid-data-element.png)


## AEP-Tags in die HTML-Seite einschließen

Erstellen und veröffentlichen Sie die Adobe Experience Platform-Tags.

Wenn eine AEP Tags-Eigenschaft veröffentlicht wird, stellt Adobe Ihnen ein Skript-Tag zur Verfügung, das Sie in Ihrem HTML-``` <head>``` oder am Ende der ``` <body>``` Tags platzieren müssen.

1. Wechseln Sie zu Ihrer Eigenschaft „Tags (ECID-Service)“.

1. Klicken Sie auf Umgebungen und dann auf das Symbol Installieren der gewünschten Umgebung (z. B. Entwicklung, Staging, Produktion).

1. Beachten Sie den eingebetteten Code.

   Dieser Code muss unmittelbar vor dem schließenden ```</body>```-Tag auf der HTML-Seite platziert werden.
