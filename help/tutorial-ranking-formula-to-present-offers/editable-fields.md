---
title: Verwenden von bearbeitbaren Formularfeldern in AJO-Code-basierten Erlebnissen
description: Erfahren Sie, wie Sie in den Vorlagen für Code-basierte Erlebnisse von Adobe Journey Optimizer bearbeitbare Inhaltsbausteine mithilfe von Inline-Formularfeldern erstellen, um Marketing-Fachleute mit dynamischen, wiederverwendbaren Kampagneninhalten zu unterstützen.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-06-22T00:00:00.000Z
recommendations: noDisplay, noCatalog
jira: KT-18416
exl-id: 0ba695d6-becb-440d-b0d0-de5b51b42562
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
source-wordcount: '221'
ht-degree: 22%
---
# Verwenden von bearbeitbaren Formularfeldern in AJO-Code-basierten Erlebnissen

In vielen Marketing-Journey, insbesondere in regulierten Branchen, ist es wichtig, einen Haftungsausschluss einzufügen, der je nach Kampagne, Geografie oder Produkt variieren kann. Durch die Verwendung eines [bearbeitbaren Felds](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/channels/code-based-experience-channel/form-fields-in-code-based-experiences) direkt im AJO Personalization-Editor können Marketing-Fachleute und Rechtsabteilungen die volle Kontrolle über den Haftungsausschlusstext behalten, ohne Entwickler einzubeziehen oder die Entscheidungslogik zu ändern.

Dies ermöglicht schnelle Aktualisierungen und stellt die Einhaltung von Vorschriften über Kampagnen hinweg sicher, während entschieden ausgewählte Inhalte wie Angebote genutzt werden.

## Einfügen eines bearbeitbaren Felds im Personalisierungseditor

- Öffnen Sie die im vorherigen Schritt erstellte Kampagne.
- Klicken Sie _&#x200B;**Kampagne ändern**&#x200B;_
- Navigieren Sie zur Registerkarte _&#x200B;**Inhalt**&#x200B;_ .
- Klicken Sie auf _&#x200B;**Code bearbeiten**&#x200B;_ und fügen Sie ein bearbeitbares Feld namens legalDisclaimer mit einem Standardwert mit der folgenden Syntax im Personalisierungseditor ein

- `{{#inline "legalDisclaimer" name="Legal Disclaimer"}} Legal Disclaimer will go here {{/inline}}`

- Verwenden Sie die Variable `{{{legalDisclaimer}}}` in der Vorlage, wie unten gezeigt

- ![editable-fields](assets/editable-fields.png)

- Marketing-Experten können das Feld „Haftungsausschluss“ einfach bearbeiten, ohne den Personalisierungseditor öffnen zu müssen.
- ![editable-field-marketer](assets/editable-field-marketer-view.png)



## Veröffentlichen der Kampagne

Aktivieren Sie die Kampagne, um personalisierte Angebote in Echtzeit bereitzustellen.
