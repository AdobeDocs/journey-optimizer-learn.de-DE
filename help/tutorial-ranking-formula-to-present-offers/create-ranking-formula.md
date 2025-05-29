---
title: Rangfolgeformel erstellen
description: Eine Rangfolgenformel in Adobe Journey Optimizer wird bei der Angebotsentscheidung verwendet, insbesondere innerhalb einer Auswahlstrategie, um die Prioritätsreihenfolge der geeigneten Angebote zu bestimmen.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-30T00:00:00Z
jira: KT-18188
source-git-commit: 58d2964644bc199b9db212040676d87d54f767b9
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 0%

---


# Rangfolgeformel erstellen

Eine Rangfolgenformel in Adobe Journey Optimizer wird bei der Angebotsentscheidung verwendet, insbesondere innerhalb einer Auswahlstrategie, um die Prioritätsreihenfolge der geeigneten Angebote zu bestimmen. Die Rangfolgenformel kommt nach der Eignungsfilterung ins Spiel, wenn mehrere Angebote für ein bestimmtes Profil qualifiziert sind, aber nur das oberste (oder einige wenige) basierend auf Geschäftslogik oder Profilkontext angezeigt werden sollten.

* Bei Journey Optimizer anmelden

* Entscheidungsfindung -> Strategie einrichten -> Rangfolgenformeln -> Formel erstellen

Rangfolgeformel
![name_description](assets/formuala-ranking.png)

Ein Kriterium in einer Rangfolgenformel bezieht sich auf eine bedingte Regel, die verwendet wird, um einem Angebot eine Bewertung zuzuweisen. Diese Kriterien vergleichen Attribute aus dem Angebot mit dem Profil oder Kontext, um zu bestimmen, wie relevant ein Angebot für eine bestimmte Person ist.



Kriterium 1
![criteria_one](assets/criteria1.png)

Kriterium 1 umfasst drei Kriterien:

* Angebot._techmarketingdemos.offerDetails.zipCode == „92128“ - prüft die mit dem Angebot verknüpfte Postleitzahl.

* _techmarketingdemos.zipCode == „92128“ - Prüft die Postleitzahl im Profil des Benutzers.

* _techmarketingdemos.annualIncome > 100000 - prüft das Einkommensniveau aus dem Benutzerprofil.

Wenn alle diese Kriterien erfüllt sind, erhält das Angebot die Bewertung 40.






Kriterium 2
![criteria_two](assets/criteria2.png)

Kriterium 2 umfasst drei Kriterien:

* Angebot._techmarketingdemos.offerDetails.zipCode == „92126“ - prüft die mit dem Angebot verknüpfte Postleitzahl.

* _techmarketingdemos.zipCode == „92126“ - Prüft die Postleitzahl im Profil des Benutzers.

* _techmarketingdemos.annualIncome &lt; 100000 - Prüft das Einkommensniveau des Benutzerprofils.

Wenn alle diese Kriterien erfüllt sind, erhält das Angebot eine Bewertung von 30.




