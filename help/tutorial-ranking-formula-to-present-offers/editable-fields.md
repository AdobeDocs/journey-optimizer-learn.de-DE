---
title: Verwenden von bearbeitbaren Formularfeldern in AJO-Code-basierten Erlebnissen
description: Erfahren Sie, wie Sie in den Code-basierten Erlebnisvorlagen von Adobe Journey Optimizer bearbeitbare Inhaltsbausteine mithilfe von Inline-Formularfeldern erstellen, um Marketingexperten dynamische, wiederverwendbare Kampagneninhalte zu ermöglichen.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-06-22T00:00:00Z
recommendations: noDisplay, noCatalog
jira: KT-18416
exl-id: 0ba695d6-becb-440d-b0d0-de5b51b42562
source-git-commit: 65d91d4fb0e978e62e5d95bf40355dcb8d27efb9
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 1%

---

# Verwenden von bearbeitbaren Formularfeldern in AJO-Code-basierten Erlebnissen

In vielen Marketing-Journey, insbesondere in regulierten Branchen, ist es wichtig, einen Haftungsausschluss einzufügen, der je nach Kampagne, Geografie oder Produkt variieren kann. Durch die Verwendung eines [bearbeitbaren Felds](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/channels/code-based-experience-channel/form-fields-in-code-based-experiences) direkt im AJO Personalization-Editor können Marketing-Fachleute und Rechtsabteilungen die volle Kontrolle über den Haftungsausschlusstext behalten, ohne Entwickler einzubeziehen oder die Entscheidungslogik zu ändern.

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
