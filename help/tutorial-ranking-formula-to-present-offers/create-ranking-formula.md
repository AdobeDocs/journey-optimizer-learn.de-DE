---
title: Rangfolgeformel erstellen
description: Eine Rangfolgenformel in Adobe Journey Optimizer wird bei der Angebotsentscheidung verwendet, insbesondere innerhalb einer Auswahlstrategie, um die Prioritätsreihenfolge der geeigneten Angebote zu bestimmen.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-30T00:00:00.000Z
recommendations: noDisplay, noCatalog
jira: KT-18188
exl-id: eee1b86e-b33f-408e-9faf-90317bc5e861
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
source-wordcount: '346'
ht-degree: 19%
---
# Rangfolgeformel erstellen

Eine Rangfolgenformel in Adobe Journey Optimizer wird bei der Angebotsentscheidung verwendet, insbesondere innerhalb einer Auswahlstrategie, um die Prioritätsreihenfolge der geeigneten Angebote zu bestimmen. Die Rangfolgenformel kommt nach der Eignungsfilterung ins Spiel, wenn mehrere Angebote für ein bestimmtes Profil qualifiziert sind, aber nur das oberste (oder einige wenige) basierend auf Geschäftslogik oder Profilkontext angezeigt werden sollten.

* Bei Journey Optimizer anmelden

* Entscheidungsfindung -> Strategie einrichten -> Rangfolgenformeln -> Formel erstellen

Rangfolgeformel
![name_description](assets/formuala-ranking.png)

Ein Kriterium in einer Rangfolgenformel bezieht sich auf eine bedingte Regel, die verwendet wird, um einem Angebot eine Bewertung zuzuweisen. Diese Kriterien vergleichen Attribute aus dem Angebot mit dem Profil oder Kontext, um zu bestimmen, wie relevant ein Angebot für eine bestimmte Person ist.



Kriterium 1

Diese Bedingung filtert Entscheidungselemente (Angebote), **nur die Angebote** enthalten, die mit „IncomeLevel“ getaggt sind.
Diese gefilterten Angebote werden dann mit dem nächsten Schritt fortgefahren - z. B. mit der Rangfolge oder dem Versand -, basierend auf der von Ihnen definierten zusätzlichen Logik.
![criteria_one](assets/income-related-formula.png)


Der folgende Ausdruck wird verwendet, um die Rangfolgenbewertung zu erstellen

```pql
if(   offer._techmarketingdemos.offerDetails.zipCode = _techmarketingdemos.zipCode,   _techmarketingdemos.annualIncome / 1000 + 10000,   if(     not offer._techmarketingdemos.offerDetails.zipCode,     _techmarketingdemos.annualIncome / 1000,     -9999   ) )
```

Funktionsweise der Formel

* Wenn das Angebot dieselbe Postleitzahl wie die Benutzerin bzw. der Benutzer hat, weisen Sie ihm eine sehr hohe Punktzahl zu, damit es zuerst ausgewählt wird.

* Wenn das Angebot überhaupt keine Postleitzahl hat (es handelt sich um ein allgemeines Angebot), geben Sie ihm eine normale Punktzahl, die auf dem Einkommen der Benutzerin bzw. des Benutzers basiert.

* Wenn das Angebot eine andere Postleitzahl hat als die Benutzerin bzw. der Benutzer, geben Sie ihm eine sehr niedrige Punktzahl, damit es nicht ausgewählt wird.

Auf diese Weise wird das System:

* versucht immer zuerst, ein Angebot anzuzeigen, das einer Postleitzahl entspricht,

* Fällt auf ein allgemeines Angebot zurück, wenn keine Übereinstimmung gefunden wird, und vermeidet die Anzeige von Angeboten, die für andere Postleitzahlen vorgesehen sind.


Wenn ein Angebotselement keines der Filterkriterien erfüllt (z. B. wenn es nicht das Tag „IncomeLevel“ hat), erhält das Angebot standardmäßig einen Ranking-Wert von 10.




