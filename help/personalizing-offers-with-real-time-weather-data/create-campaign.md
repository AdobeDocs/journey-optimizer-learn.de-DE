---
title: Erstellen einer Kampagne
description: Erfahren Sie, wie eine AJO-Kampagne Audiences, Entscheidungsrichtlinien und Kanäle verbindet, um personalisierte Angebote zum richtigen Zeitpunkt über Kunden-Touchpoints bereitzustellen.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-30T00:00:00Z
recommendations: noDisplay, noCatalog
jira: KT-18258
exl-id: c3e4f760-9b10-4a99-bc53-9245e76c1bab
source-git-commit: 51707a64a5d05227b663fed5e0413b4d2ffee0a9
workflow-type: tm+mt
source-wordcount: '642'
ht-degree: 1%

---

# Erstellen einer Kampagne

Um den Nutzern auf der Web-Seite personalisierte Angebote zu unterbreiten, wurde in Adobe Journey Optimizer eine Kampagne erstellt und mit dem richtigen Kanal, dem Code-basierten Erlebniskanal, konfiguriert. Diese Konfiguration stellt sicher, dass die Angebote über Echtzeit-Entscheidungsfindung an Benutzer übermittelt werden, die mit der Website interagieren.

In dieser Kampagne wurde eine Entscheidungsrichtlinie definiert, um zu steuern, wie Angebote ausgewählt werden. Die Entscheidungspolitik umfasst eine Auswahlstrategie, die Folgendes umfasst:

- Eine Sammlung von Angebotselementen (z. B. basierend auf wetterbezogenen Tags),
- Eignungsregeln, die bestimmen, welche Angebote für einen Benutzer gelten, und
- Eine Rangfolgenformel, die geeigneten Angeboten Bewertungen zuweist, um die relevantesten Angebote zu priorisieren.

Wenn ein Benutzer die Website besucht, erkennt das System den Standort und ruft mithilfe einer Wetter-API die aktuelle Temperatur ab. Diese Temperaturdaten werden dann über die Web SDK (Alloy) an Adobe Experience Platform gesendet. Basierend auf diesen kontextuellen Echtzeitdaten wertet Adobe Journey Optimizer vordefinierte Angebote aus, die mit Tags für bestimmte Wetterbedingungen versehen sind, z. B. heiß, mild oder kalt. Das relevanteste Angebot unter Verwendung der Auswahlstrategie und der Rangfolgenformel wird automatisch auf der Web-Seite mithilfe der Adobe Decisioning-Engine gerendert, um sicherzustellen, dass die Benutzenden personalisierte Inhalte erhalten, die an das aktuelle Wetter in ihrer Region angepasst sind.


## Allgemeine Schritte zum Erstellen einer Kampagne in AJO

- Erstellen einer Kanalkonfiguration
   - Definieren, wo und wie die Angebote angezeigt werden (z. B. eine Web-Seite mit Code-basiertem Erlebnis).
   - Beim Journey Optimizer anmelden
   - Navigieren Sie zu _**Administration -> Kanäle -> Kanalkonfiguration erstellen**_
   - **Name**: `offers-by-weather`\
     Identifiziert diese Konfiguration für die Bereitstellung personalisierter Web-Angebote.
- **channel**:
  `Code-based experience`\
  Angebote werden nicht direkt in das DOM eingefügt. Stattdessen gibt AJO unformatierten HTML zurück, der mithilfe von benutzerdefiniertem JavaScript geparst wird.
- **Platform**: `Web`\
  Speziell für Webbrowser. Es sind keine mobilen Kanäle aktiviert.

- **Seiten-URL**: `https://gbedekar489.github.io/weather/weather-offers.html`\
  Der Kanal ist für eine bestimmte Testseite konfiguriert, die während der Entwicklung verwendet wird.
- **Standort auf Seite**: `offerContainer`\
  Die zurückgegebenen Angebote werden dynamisch analysiert und mithilfe der Frontend-Logik in diesen Container gerendert.

- **Inhaltsformat**: `HTML`\
  Die Angebote werden als unformatierte HTML-Fragmente bereitgestellt, sodass Sie vollständig steuern können, wie sie gestaltet, gefiltert und angezeigt werden.


- **Neue Kampagne starten**
   - Navigieren Sie zum Abschnitt Kampagnen und erstellen Sie eine neue geplante Marketing-Kampagne. Benennen Sie die Kampagne entsprechend.
   - **Aktion hinzufügen**
      - Fügen Sie die Code-basierte Erlebnisaktion hinzu und verknüpfen Sie die Aktion mit einer zuvor erstellten Kanalkonfiguration.



   - **Zielgruppe**
      - Alle Besucher (Standard).
      - Identitätstyp: ECID (Experience Cloud ID)
Diese Einstellung verwendet die ECID als primäre Identität zum Erkennen von Benutzern.


- **Entscheidungsrichtlinie erstellen**
   - Die Aktion ist mit einer **Entscheidungsrichtlinie“ verknüpft** die definiert, wie Angebote ausgewählt und wie viele Angebote zur Anzeige zurückgegeben werden. Diese Richtlinie verwendet eine **Auswahlstrategie** die zuvor im Tutorial erstellt wurde.
   - Um die Entscheidungsrichtlinie einzufügen, klicken Sie in den _**Aktionen auf**_ Inhalt bearbeiten und anschließend auf **_Code bearbeiten_**, um den Personalisierungseditor zu öffnen.
   - Wählen Sie _**Symbol**_ Entscheidungsrichtlinie“ auf der linken Seite aus und klicken Sie auf die Schaltfläche **Entscheidungsrichtlinie hinzufügen**, um den Bildschirm **Entscheidungsrichtlinie erstellen** zu öffnen. Geben Sie der Entscheidungsrichtlinie einen aussagekräftigen Namen und wählen Sie die Anzahl der Elemente aus, die die Entscheidungsrichtlinie zurückgeben soll. Der Standardwert ist 1.
   - Klicken Sie **_Weiter_**, fügen Sie die im vorherigen Schritt erstellte Auswahlstrategie zur Entscheidungsrichtlinie hinzu und klicken Sie auf **Weiter**, um den Prozess der Erstellung der Entscheidungsrichtlinie abzuschließen. Es wurden keine Fallback-Angebote mit der Entscheidungsrichtlinie verknüpft.



- **Entscheidungsrichtlinie einfügen**
  ![personalization-editor](assets/personalization-editor.png)

  Fügen Sie die neu erstellte Entscheidungsrichtlinie ein, indem Sie auf die Schaltfläche _**Richtlinie einfügen**_ klicken. Dadurch wird eine for-Schleife im Personalisierungseditor auf der rechten Seite eingefügt.
Platzieren Sie den Cursor zwischen den einzelnen Schleifen in Zeile zwei und fügen Sie den offerText ein, indem Sie durch Drilldown des `tenant name` zum Angebot navigieren

  Der Handlebars-Code durchläuft die Angebote, die von einer bestimmten Entscheidungsrichtlinie in Adobe Journey Optimizer zurückgegeben werden.
  ![Lenker](assets/handlebar-code.png)

- **Veröffentlichen Sie die Kampagne**\
  Aktivieren Sie die Kampagne, um personalisierte Angebote in Echtzeit bereitzustellen.
