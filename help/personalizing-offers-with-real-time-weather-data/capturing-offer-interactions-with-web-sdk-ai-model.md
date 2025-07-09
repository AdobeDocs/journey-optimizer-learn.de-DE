---
title: Erfassen von Angebotsinteraktionen mit Adobe Web SDK für KI-Modellschulungen
description: Dieser Artikel enthält Anleitungen zur Erfassung von Benutzerinteraktionsdaten - wie Angebotsimpressionen und Klicks - mithilfe der Adobe Experience Platform Web SDK (alloy.js). Diese Daten dienen als Grundlage für das Trainieren von KI-Modellen in Adobe Journey Optimizer (AJO), um Angebote intelligent nach Benutzerverhalten und kontextuellen Signalen zu ordnen.
feature: Decisioning
topic: Integrations
role: User
level: Beginner
doc-type: Article
last-substantial-update: 2025-07-08T00:00:00Z
jira: KT-18451
source-git-commit: 41f0d44fb39c9d187ee8c97d54202387fa9eda56
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 0%

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
if (offerIds.length > 0) {
  alloy("sendEvent", {
    xdm: {
      _id: generateUUID(),
      timestamp: new Date().toISOString(),
      eventType: "decisioning.propositionDisplay",
      _experience: {
        decisioning: {
          propositionEvent: {
            display: 1
          },
          involvedPropositions: offerIds.map(id => ({
            id,
            scope: "web://gbedekar489.github.io/weather/weather-offers.html#offerContainer"
          }))
        }
      }
    }
  });
}
```

## Klickereignisse für Angebote (Interaktionen) erfassen

Um zu verfolgen, wann ein Benutzer auf ein Angebot klickt, haben wir die vorhandene JavaScript aktualisiert, um auf Klicks sowohl auf `<a>` als auch auf `<button>` zu warten, die im Angebotscontainer gerendert werden.

Wenn ein Klick erkannt wird, wird mithilfe der Adobe Web SDK ein decisioning.propositionInteract-Ereignis gesendet. Das Ereignis enthält die erforderliche Interact: 1-Markierung und verweist auf die spezifische Angebots-ID und den Entscheidungsumfang.

```javascript
// Attach click tracking to <a> and <button> elements
wrapper.querySelectorAll("a, button").forEach(el => {
  el.addEventListener("click", () => {
    const offerId = el.getAttribute("data-offer-id") || item.id;
    console.log("Clicked element offerId:", offerId);

    alloy("sendEvent", {
      xdm: {
        _id: generateUUID(),
        timestamp: new Date().toISOString(),
        eventType: "decisioning.propositionInteract",
        _experience: {
          decisioning: {
            propositionEvent: {
              interact: 1
            },
            involvedPropositions: [{
              id: offerId,
              scope: "web://gbedekar489.github.io/weather/weather-offers.html#offerContainer"
            }]
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

Fügen Sie die [aktualisierte JavaScript-Datei](assets/ai-model.js) in die [vorhandene Webseite“ ](assets/weather-offers.html)