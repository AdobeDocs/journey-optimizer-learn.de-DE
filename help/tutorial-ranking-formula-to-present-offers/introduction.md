---
title: Angebote mit Rangfolgeformeln basierend auf Postleitzahl und Einkommen des Benutzers personalisieren
description: Verwenden Sie die Rangfolgeformeln von Adobe Journey Optimizer, um dynamisch die relevantesten Finanzangebote bereitzustellen, die auf die Postleitzahl und die Einkommensstufe jedes Benutzers zugeschnitten sind, um eine höhere Interaktion und eine intelligentere Personalisierung zu ermöglichen.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-27T00:00:00Z
jira: KT-18188
source-git-commit: 58d2964644bc199b9db212040676d87d54f767b9
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# Angebote mit Rangfolgeformeln basierend auf Postleitzahl und Einkommen des Benutzers personalisieren

In diesem Anwendungsbeispiel wird gezeigt, wie mithilfe von Benutzerattributen wie Postleitzahl und Jahreseinkommen in Adobe Journey Optimizer personalisierte Finanzangebote bereitgestellt werden können. Durch die Verwendung von Rangfolgeformeln werden Angebote auf intelligente Weise bewertet und basierend auf standortspezifischen Promotions und einkommensbasierter Eignung priorisiert. So können beispielsweise ertragsstarke CDs an Nutzer in wohlhabenden Postleitzahlen verkauft werden, während sich aufstrebenden Anlegern vielfältige Anlageoptionen präsentieren. Ranking-Formeln stellen sicher, dass jeder Benutzer Angebote erhält, die sowohl relevant als auch finanziell angemessen sind. Rangfolgekriterien werden mithilfe von Profilattributen, Kontextsignalen und optionalen KI-Modellen definiert, um die Entscheidungsgenauigkeit weiter zu verbessern. Angebote werden in Echtzeit über Web- oder E-Mail-Kanäle bereitgestellt, was zu höherer Interaktion und Konversion führt. Dieser Ansatz kombiniert Geschäftslogik mit datengesteuerter Personalisierung, um das Benutzererlebnis und die Marketing-Wirkung zu steigern.

## Voraussetzungen

Dieses Tutorial baut auf den wichtigsten Konzepten von Adobe Journey Optimizer und Adobe Experience Platform auf. Bevor Sie fortfahren, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

* [Das Tutorial zum Identitätszuordnen](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorial-on-identity-stitching-in-aep/introduction) wurde abgeschlossen. CRM-IDs wurden erfolgreich mit ECIDs in Adobe Experience Platform verknüpft.

* vertraut mit dem Erstellen von Angebotselementen in AJO, einschließlich Inhaltsdefinition, Metadateneinrichtung und Eignungsregeln.

* vertraut mit der Konfiguration von Kanälen (wie Web oder E-Mail) für die Angebotsbereitstellung.

* vertraut mit dem Erstellen und Aktivieren von Kampagnen in AJO.

* vertraut mit der Verwendung von Adobe Launch (Tags) zum Bereitstellen der Web-SDK und Senden von Ereignissen mit Identitäts- und Profildaten.

Dieses Tutorial behandelt die nächsten Schritte in Offer Decisioning:

* Erstellen einer Rangfolgenmethode mit Profilattributen wie Postleitzahl und Jahreseinkommen.

* Definieren einer Auswahlstrategie zum Gruppieren und Priorisieren von Angeboten

* Erstellen einer Entscheidungsrichtlinie , um jedem Kontakt das relevanteste Angebot zu unterbreiten.


