---
title: Erstellen von Zielgruppen in Adobe Journey Optimizer
description: Erfahren Sie, wie Sie in AJO Audiences definieren und erstellen, um personalisierte Kunden-Journey und Echtzeit-Entscheidungen zu ermöglichen
feature: Audiences
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-04-30T00:00:00Z
jira: KT-17923
source-git-commit: ba83be3caf214d2daaa8c99556d246686ff3f0cb
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# Erstellen von Zielgruppen in Adobe Journey Optimizer


Zielgruppen in Adobe Experience Platform sind Benutzergruppen, die basierend auf ihren Aktionen, Voreinstellungen oder Profilinformationen erstellt werden, um personalisierte Erlebnisse bereitzustellen.

* Bei Journey Optimizer anmelden
* Gehen Sie zu Kunde > Zielgruppen > Zielgruppe erstellen .
* Erstellen von Zielgruppen mit der Methode „Regel erstellen“

  ![Audience](assets/rule-based-audience.png)

* Erstellen der folgenden drei Zielgruppen

   * Kunden, die an Aktien interessiert sind

   * Kunden, die an Anleihen interessiert sind

   * Kunden, die an CD interessiert sind


* Stellen Sie sicher, dass die Auswertungsmethode für jede Zielgruppe auf _**Edge**_ für die Echtzeit-Qualifizierung festgelegt ist.
  ![edge-audience](assets/audience-edge.png)

* Verwenden Sie das Feld PreferredFinancialInstrument , um Benutzer basierend auf ihren ausgewählten Anlagebetrieben wie Aktien, Anleihen oder CDs zu segmentieren

![event](assets/event-attribute.png)

![PreferredFinancialInstrument](assets/stock-customers.png)




>[!NOTE]
>
>>Wenn das Feld PreferredFinancialInstrument nicht auf der Registerkarte Ereignisse angezeigt wird, klicken Sie auf das Einstellungssymbol und schalten Sie die Option Vollständiges XDM-Schema anzeigen um.



![toggle-full-xdm-schema](assets/show-custom-fields.png)


