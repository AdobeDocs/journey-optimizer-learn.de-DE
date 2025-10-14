---
title: Erfassen von Angebotsinteraktionen mit Adobe Web SDK für KI-Modellschulungen
description: Dieser Artikel enthält Anleitungen zur Erfassung von Benutzerinteraktionsdaten - wie Angebotsimpressionen und Klicks - mithilfe der Adobe Experience Platform Web SDK (alloy.js). Diese Daten dienen als Grundlage für das Trainieren von KI-Modellen in Adobe Journey Optimizer (AJO), damit diese Angebote intelligent nach Benutzerverhalten und kontextuellen Signalen reihen.
feature: Decisioning
topic: Integrations
role: User
level: Beginner
doc-type: Article
last-substantial-update: 2025-07-08T00:00:00Z
jira: KT-18451
exl-id: 3cb280b3-71e5-4e91-9252-5679d794d4c4
source-git-commit: 6c4f33d1f55be298781cfb0958862f9710e3647a
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 4%

---

# Erfassen von Angebotsinteraktionen mit Adobe Web SDK für KI-Modellschulungen

>[!NOTE]
>
> Schließen Sie diesen Artikel nur ab, wenn Sie planen, KI-basierte Ranking-Methoden in Adobe Journey Optimizer zu verwenden, um zu personalisieren, welches Angebot basierend auf der prognostizierten Interaktion angezeigt wird.



Dieser Artikel zeigt, wie Sie Interaktionsereignisse von Angeboten (wie Impressions oder Klicks) mithilfe der Adobe Experience Platform Web SDK erfassen können, indem Sie alloy(„sendEvent“, …) direkt in Ihrem JavaScript-Code aufrufen. Die Daten werden in AEP aufgenommen und zum Trainieren von KI-Modellen in Adobe Journey Optimizer (AJO) verwendet, um das Angebotsranking auf der Grundlage des Echtzeitverhaltens zu verbessern.

Um in Adobe Journey Optimizer ein KI-Modell für das Angebotsranking zu erstellen, muss Ihr Datensatz auf einem Schema basieren, das die Feldergruppe „Vorschlagsinteraktionen“ enthält. Diese Feldergruppe unterstützt wichtige Entscheidungsereignisse wie decisioning.propositionDisplay und decisioning.propositionInteract sowie erforderliche Felder wie „relatedPropositions“, „display“ und „interact“.

Dazu gibt es zwei gültige Ansätze:

- Erstellen Sie ein neues Schema, einen neuen Datensatz und einen neuen Datenstrom, die bzw. der speziell für das Interaktions-Tracking konfiguriert wurde
- Aktualisieren eines vorhandenen Schemas - wie in diesem Tutorial beschrieben



## Vorhandenes Schema aktualisieren, um Interaktionsereignisse des Angebots zu erfassen

Anstatt ein neues Schema zu erstellen, wird das vorhandene Erlebnisereignisschema, das für wetterbezogene Angebote verwendet wird, aktualisiert, um das Interaktions-Tracking zu unterstützen.

In Adobe Experience Platform:

- Öffnen Sie das vorhandene _&#x200B;**Wetter-Schema**&#x200B;_ Erlebnisereignis-Schema, das Sie für wetterbasierte Angebote verwenden.

- Fügen Sie die Feldergruppe hinzu:
Erlebnisereignis - Interaktionen bei Vorschlägen

Sie müssen keinen neuen Datensatz oder Datenstrom erstellen - verwenden Sie weiterhin Ihr vorhandenes Setup für Wetterangebote. Die gesendeten Ereignisse entsprechen den Erwartungen von Adobe Journey Optimizer an das Trainieren von KI-Modellen und das Tracking der Angebotsleistung.


Aktuellen Datensatz weiter verwenden (kein neuer Datensatz erstellt werden muss)

Der vorhandene Datenstrom ist bereits konfiguriert und wird in der Adobe Experience Platform Tags -Eigenschaft verwendet. Dort sind keine Änderungen erforderlich.

Web SDK leitet neue Interaktionsereignisse automatisch an das richtige Ziel weiter.

Diese optimierte Einrichtung stellt sicher, dass alle Entscheidungs- und Wetterereignisse in einen einzigen, einheitlichen Datensatz aufgenommen werden. Dies ist ideal für das Trainieren von KI-Modellen in Adobe Journey Optimizer.


## Erfassen von Angebotsereignissen (Impressionen)

Die HTML-Struktur des Angebots wurde geändert, um interaktive Elemente einzuschließen - insbesondere `<a>`- und `<button>`-Tags -, sodass Benutzende mit dem Angebot interagieren können (z. B. Schaltflächen „Angebot anfordern“ oder „Mehr erfahren„).

Jede Schaltfläche enthält das Attribut data-offer-id , sodass die entsprechende Interaktion ordnungsgemäß verfolgt werden kann.



Um zu protokollieren, wann den Benutzern Angebote angezeigt werden, wurde die vorhandene JavaScript-Datei aktualisiert, die für das Rendern von Wetterangeboten verwendet wird, sodass sie die Anzeige von Ereignisverfolgung enthält.

Ein decisioning.propositionDisplay-Ereignis wird jetzt mit dem Adobe Web SDK (alloy.sendEvent) gesendet, wenn ein oder mehrere Angebote angezeigt werden. Dieses Ereignis enthält die erforderliche Anzeige: 1 Markierung und verweist auf die betreffenden Vorschläge.


```javascript
alloy("sendEvent", {
                    xdm: {
                      _id: generateUUID(),
                      timestamp: new Date().toISOString(),
                      eventType: "decisioning.propositionInteract",
                      identityMap: {
                        ECID: [{
                          id: ecidValue,
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
                  });
```

## Klickereignisse für Angebote (Interaktionen) erfassen

Um zu verfolgen, wann ein Benutzer auf ein Angebot klickt, haben wir die vorhandene JavaScript aktualisiert, um auf Klicks sowohl auf `<a>` als auch auf `<button>` zu warten, die im Angebotscontainer gerendert werden.

Wenn ein Klick erkannt wird, wird mithilfe der Adobe Web SDK ein decisioning.propositionInteract-Ereignis gesendet. Das Ereignis enthält die erforderliche Interact: 1-Markierung und verweist auf die spezifische Angebots-ID und den Entscheidungsumfang.

```javascript
// Attach click tracking to <a> and <button> elements
child.querySelectorAll("a, button").forEach(el => {
                el.addEventListener("click", () => {
                  const ecidValue = getECID();
                  if (!ecidValue || !offerId || !trackingToken) {
                    console.warn("Girish!!!!  Missing ECID, offerId, or trackingToken. Interaction event not sent.");
                    return;
                  }

                  alloy("sendEvent", {
                    xdm: {
                      _id: generateUUID(),
                      timestamp: new Date().toISOString(),
                      eventType: "decisioning.propositionInteract",
                      identityMap: {
                        ECID: [{
                          id: ecidValue,
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
                  });
                });
              });
```

## Erstellen eines KI-Modells für das Angebots-Ranking in Adobe Journey Optimizer Offer Decisioning

Da Angebotsimpressionen und -klicks jetzt über die Web-SDK erfasst und in Adobe Experience Platform gespeichert werden, können diese Daten zum Trainieren eines KI-Modells verwendet werden, das vorhersagt, welche Angebote die Interaktion am wahrscheinlichsten fördern.

Dieses KI-Modell wird in einer Rangfolgenformel oder Auswahlstrategie referenziert, um zu bestimmen, welche Angebote für jeden Benutzer priorisiert werden.
- Bei Journey Optimizer anmelden
- Gehen Sie zu Entscheidungsfindung > Strategie einrichten > KI-Modelle > KI-Modell erstellen .
- Stellen Sie sicher, dass Sie den richtigen Datensatz verwenden
  ![KI-Modell](assets/ai-model.png)
- Speichern und aktivieren Sie das KI-Modell.
- Aktualisieren Sie die im vorherigen Schritt erstellte Auswahlstrategie, um das KI-Modell für die Rangfolgenmethode zu verwenden.
  ![update-selection-strategy](assets/update-selection-strategy.png)

## Testen der Lösung

Fügen Sie die [aktualisierte JavaScript-Datei](assets/ai-model.js) in die [vorhandene Webseite“ &#x200B;](assets/weather-offers.html)
