---
title: Erstellen von Adobe Experience Platform-Tags
description: Erstellen von AJO-Zielgruppen anhand der Voreinstellungen für Benutzerinvestitionen (Aktien, Anleihen, CDs)
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-05T00:00:00Z
jira: KT-17923
exl-id: 6823ce13-bc77-4e2b-89e0-606e403c15f2
source-git-commit: 2ca9ffee1a2326b8ae55a8e8de496a632fea79c8
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# Adobe Experience Platform erstellen

Adobe Launch wird auf der Web-Seite so konfiguriert, dass die Adobe Experience Platform Web SDK geladen wird und der sendEvent-API-Aufruf für personalisierte Erlebnisse für Trigger aktiviert wird. Dadurch wird sichergestellt, dass die erforderlichen Client-seitigen Bibliotheken korrekt initialisiert werden, sodass für die Angebotsbereitstellung eine Echtzeit-Interaktion mit Adobe Journey Optimizer möglich ist.

* Bei Datenerfassung anmelden
* Klicken Sie auf Tags > Neue Eigenschaft .
* Erstellen Sie ein Adobe Experience Platform-Tag namens ECID-Service.

* Fügen Sie die folgenden Erweiterungen zum -Tag hinzu
  ![tags-extensions](assets/ecid-tag.png)

* Stellen Sie sicher, dass Sie Adobe Experience Platform Web SDK so konfigurieren, dass die richtige Umgebung und der im vorherigen Tutorial erstellte Datenstrom für Finanzberater verwendet werden
  ![web-sdk-configuration](assets/web-sdk-configuration.png)

* Für die Adobe Client-Datenschicht und die Haupterweiterungen ist keine zusätzliche Konfiguration erforderlich

## Datenelement erstellen

Das ECID-Datenelement in Adobe Launch wird ausschließlich zu Debugging- und Testzwecken erstellt. Damit können Entwicklerinnen und Entwickler die Experience Cloud-ID anzeigen, die der Browser-Sitzung einer Benutzerin oder eines Benutzers zugewiesen wurde. Dies kann dazu beitragen, die Identitätszuordnung zu überprüfen und sicherzustellen, dass die sendEvent-Aufrufe mit dem richtigen Profil verknüpft sind. Dieses Element ist nicht erforderlich, damit die Personalisierung funktioniert, ist aber bei der Implementierung und Qualitätssicherung nützlich

![ECID](assets/ecid-data-element.png)


## AEP-Tags in die HTML-Seite einschließen

Erstellen und Veröffentlichen der Adobe Experience Platform-Tags

Wenn eine AEP Tags-Eigenschaft veröffentlicht wird, stellt Adobe Ihnen ein Skript-Tag zur Verfügung, das Sie in Ihrem HTML-``` <head>``` oder am Ende der ``` <body>``` Tags platzieren müssen.

* Navigieren Sie zu Ihrer Eigenschaft „Tags (ECID-Service)“.

* Klicken Sie auf Umgebungen und dann auf das Symbol Installieren der gewünschten Umgebung (z. B. Entwicklung, Staging, Produktion).

* Notieren Sie sich den eingebetteten Code. Dieser Code muss unmittelbar vor dem schließenden ```</body>```-Tag auf der HTML-Seite platziert werden.
