---
title: Erfassen von Impressions- und Interaktionsereignissen
description: Erfassen von Impression- und Interaktionsereignissen und Vorbereiten der Daten für das Reporting in Journey Optimizer.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
recommendations: noDisplay, noCatalog
last-substantial-update: 2025-07-18T00:00:00Z
jira: KT-18526
exl-id: 7e6014b5-c5a6-467b-8e31-58c5d966464c
source-git-commit: bef6d831c639d40514552dae3ff20132626a4a09
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 0%

---

# Erfassen von Impressions- und Interaktionsereignissen

Um das Reporting zu Angebotsimpressionen und Klicks aus AJO Decisioning zu aktivieren, müssen die folgenden Komponenten konfiguriert werden:
>[!NOTE]
>
> Diese Voraussetzungen wurden bereits im Abschnitt Erstellen eines Schemas und Datensatzes des (vorherigen [) &#x200B;](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/personalizing-offers-with-real-time-weather-data/create-schema-and-dataset)

## &#x200B;1. Datensatz in Adobe Experience Platform (AEP)

- Ein Datensatz, der auf einem **XDM ExperienceEvent**-Schema basiert.

Das Schema muss `Web Details` Feldergruppe enthalten, die die Seiten-URL, den Referrer usw. erfasst.

## &#x200B;2. Konfiguration des Datenstroms

- Adobe Experience Platform In **muss** Datenstrom erstellt werden.
- Dieser Datenstrom muss mit dem oben konfigurierten Datensatz verknüpft sein, um sicherzustellen, dass alle Web SDK-Ereignisse ordnungsgemäß in das richtige Ziel aufgenommen werden.

## &#x200B;3. Adobe Experience Platform Tags-Eigenschaft

- AEP Web SDK-Erweiterung, die für die Verwendung des im vorherigen Schritt erstellten Datenstroms konfiguriert ist.
- Experience Cloud ID-Dienst konfiguriert
- Ein Datenelement mit dem Namen ECID wird der Eigenschaft hinzugefügt
- Auf der Site implementiert, auf der Angebote gerendert werden.


Um das Reporting über die Angebotsleistung zu aktivieren, besteht der erste Schritt darin, zu erfassen, wann Angebote angezeigt werden (Impressionen) und wann sie angeklickt werden (Interaktionen). Diese Ereignisse bilden die Grundlage für die Messung der Interaktion, die Berechnung von Klickraten und die Analyse der Angebotseffektivität in Adobe Experience Platform.

Die Funktion alloy(„sendEvent„) wird verwendet, um Benutzerinteraktionen mit von Adobe Journey Optimizer (AJO) zurückgegebenen Angeboten zu protokollieren.

Die SendEvent-Payload erfasst Angebotsinteraktionen, indem sie den Ereignistyp (decisioning.propositionDisplay für Impressionen oder decisioning.propositionInteract für Klicks), eine eindeutige Ereignis-ID, einen eindeutigen Zeitstempel und eine eindeutige Benutzeridentität (identityMap) umfasst. Sie enthält auch die Liste der angezeigten oder angeklickten Angebote (Vorschläge) zusammen mit Tracking-Token, um eine genaue Zuordnung sicherzustellen. Diese Struktur ermöglicht die Berichterstellung und Optimierung der Leistung personalisierter Angebote in Adobe Journey Optimizer.

Es werden zwei Arten von Interaktionsereignissen erfasst:

## Impression-Ereignis

Eine Impression tritt auf, wenn ein Angebot auf der Seite gerendert wird und für den Benutzer sichtbar wird. Das Ereignis wird mit dem Ereignistyp decisioning.propositionDisplay verfolgt.


```javascript
 alloy("sendEvent", {
            xdm: {
              _id: generateUUID(),
              timestamp: new Date().toISOString(),
              eventType: "decisioning.propositionDisplay",
              identityMap: {
                    ECID: [{
                      id: _satellite.getVar("ECID"),
                      authenticatedState: "authenticated",
                      primary: true
                    }]
                  },
              _experience: {
                decisioning: {
                  propositionEventType: {
                    display: 1
                  },
                    propositionAction: {
                            id: offerId,
                            tokens: [trackingToken]
                  },
                  
                   propositions: window.latestPropositions
                  
                }
              }
            }
          });
        }
```

## Angebotsinteraktion

Eine Interaktion wird aufgezeichnet, wenn ein Benutzer innerhalb des gerenderten Angebots auf eine call-to-action (CTA) klickt. Das Ereignis wird mit dem Ereignistyp decisioning.propositionInteract verfolgt.

```javascript
alloy("sendEvent", {
                xdm: {
                  _id: generateUUID(),
                  timestamp: new Date().toISOString(),
                  eventType: "decisioning.propositionInteract",
                  identityMap: {
                    ECID: [{
                      id: _satellite.getVar("ECID"),
                      authenticatedState: "ambiguous",
                      primary: true
                    }]
                  },
                  _experience: {
                    decisioning: {
                      propositionEventType: {
                        interact: 1
                      },
                      propositionAction: {
                        id: offerId,
                        tokens: [trackingToken]
                      },
                       propositions: window.latestPropositions
                    }
                  }
                }
              })
```

Die Einbindung von Vorschlägen in Klick- und Impressionsereignisse ist für ein präzises Angebotsreporting in Adobe Journey Optimizer unerlässlich. Diese Vorschläge stellen die exakten Angebote dar, die den Benutzenden unterbreitet wurden, sodass Adobe Benutzerinteraktionen (z. B. Impressionen oder Klicks) wieder den spezifischen Entscheidungen des Systems zuordnen kann.

Jedes Angebot in einem Vorschlag enthält ein Tracking-Token, bei dem es sich um eine eindeutige Kennung handelt, die von Adobe generiert wird. Dieses Token muss genau so übergeben werden, wie es im entsprechenden Klick- oder Impressionsereignis empfangen wurde - ohne Änderung. Durch übereinstimmende Tracking-Token wird sichergestellt, dass Adobe die Benutzeraktion präzise mit der richtigen Angebotsentscheidung verknüpfen kann, was nachgelagertes Reporting und KI-basierte Optimierung ermöglicht.
