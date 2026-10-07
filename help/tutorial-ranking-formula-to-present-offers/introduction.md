---
title: Personalisieren von auf Postleitzahl und Einkommen basierenden Angeboten mit Rangfolgenformeln
description: Verwenden Sie Rangfolgenformeln von Adobe Journey Optimizer, um dynamisch die relevantesten Finanzangebote bereitzustellen, die auf die Postleitzahl und das Einkommensniveau jeder Benutzerin bzw. jedes Benutzers zugeschnitten sind. So ermöglichen Sie eine höhere Interaktion und intelligentere Personalisierung.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-27T00:00:00.000Z
jira: KT-18188
exl-id: 11685f7c-8048-4318-9c28-71bd7da8f7ff
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
source-wordcount: '338'
ht-degree: 21%
---
# Personalisieren von Angeboten mit Rangfolgeformeln basierend auf der Postleitzahl und dem Einkommen des Benutzers

In diesem Anwendungsbeispiel wird gezeigt, wie mithilfe von Benutzerattributen wie Postleitzahl und Jahreseinkommen in Adobe Journey Optimizer personalisierte Finanzangebote bereitgestellt werden können. Durch die Verwendung von Rangfolgeformeln werden Angebote auf intelligente Weise bewertet und basierend auf standortspezifischen Angeboten und einkommensbasierter Eignung priorisiert. So können beispielsweise ertragsstarke CDs an Nutzer in wohlhabenden Postleitzahlen verkauft werden, während sich aufstrebenden Anlegern vielfältige Anlageoptionen präsentieren. Ranking-Formeln stellen sicher, dass jeder Benutzer Angebote erhält, die sowohl relevant als auch finanziell angemessen sind. Rangfolgekriterien werden mithilfe von Profilattributen, Kontextsignalen und optionalen KI-Modellen definiert, um die Entscheidungsgenauigkeit weiter zu verbessern. Angebote werden in Echtzeit über Web- oder E-Mail-Kanäle bereitgestellt, was zu höherer Interaktion und Konversion führt. Dieser Ansatz kombiniert Geschäftslogik mit datengesteuerter Personalisierung, um das Benutzererlebnis und die Marketing-Wirkung zu steigern.

## Voraussetzungen

Dieses Tutorial baut auf den wichtigsten Konzepten von Adobe Journey Optimizer und Adobe Experience Platform auf. Bevor Sie fortfahren, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

* [Das Tutorial zum Identitätszuordnen](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorial-on-identity-stitching-in-aep/introduction) wurde abgeschlossen. CRM-IDs wurden erfolgreich mit ECIDs in Adobe Experience Platform verknüpft.

* vertraut mit dem Erstellen von Angebotselementen in AJO, einschließlich Inhaltsdefinition, Metadateneinrichtung und Eignungsregeln.

* vertraut mit der Konfiguration von Kanälen (wie Web oder E-Mail) für die Angebotsbereitstellung.

* vertraut mit dem Erstellen und Aktivieren von Kampagnen in AJO.

* vertraut mit der Verwendung von Adobe Launch (Tags) zum Bereitstellen der Web-SDK und Senden von Ereignissen mit Identitäts- und Profildaten.

Dieses Tutorial behandelt die nächsten Schritte in Offer Decisioning:

* Erstellen einer Rangfolgenmethode mit Profilattributen wie Postleitzahl und Jahreseinkommen.

* Definieren einer Auswahlstrategie zum Gruppieren und Priorisieren von Angeboten

* Erstellen einer Entscheidungsrichtlinie , um jedem Kontakt das relevanteste Angebot zu unterbreiten.
