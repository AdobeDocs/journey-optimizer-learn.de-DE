---
source-git-commit: 084d4d9457db32e30855cd6466439b1de96f2b68
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 3%
---
# Live-Aktivitäten

## Was ist es?

Mit **Live-** können Sie beständige Aktualisierungen in Echtzeit bereitstellen, die Kunden über den Fortschritt einer Aktivität informieren, z. B. eine sich in Vorbereitung befindende Bestellung, ein Versand während der Fahrt oder eine Fahrt auf dem Weg. Anstatt für jede Aktualisierung eine neue Benachrichtigung zu senden, wird eine einzelne Live-Aktivität erstellt, dann aktualisiert und beendet, wenn sich die Aktivität entwickelt, wobei der Sperrbildschirm oder die Benachrichtigungsschattierung des Kunden mit dem synchronisiert wird, was passiert.

Adobe Journey Optimizer unterstützt Live-Aktivitäten auf beiden wichtigen Mobilplattformen:

* **[iOS Live-Aktivitäten](/help/channels/ios-live-activities.md)** - Umfangreiche Echtzeit-Updates auf dem iPhone-Sperrbildschirm und auf Dynamic Island.
* **[Live-](/help/channels/android-live-updates.md)** zu Android- Persistente Echtzeit-Updates im Android-Benachrichtigungsschatten.

Informationen zum Konfigurieren der Mobile SDK und zum Verwenden der APIs zum Starten, Aktualisieren und Beenden von Live-Erlebnissen in allen Kunden-Journey finden Sie unter [Konfigurieren von Live-Aktivitäten](https://experienceleague.adobe.com/de/docs/journey-optimizer/using/channels/live-activity/configure-live-activity/mobile-live-configuration-sdk){target="_blank"}.

## Anwendungsszenarien

Wählen Sie Live-Aktivitäten als bevorzugten Kanal aus, wenn Sie Folgendes benötigen:

| # | Vorteil | Warum | Beispielhafte Anwendungsfälle |
|---|---------|-----|-------------------|
| 1 | Laufende Fortschritte auf einen Blick | Aktualisierungen werden direkt auf dem Sperrbildschirm oder dem dynamischen Insel-/Benachrichtigungsschatten angezeigt, ohne dass der Benutzer die App öffnet | <ul><li>Tracking der Lebensmittelzustellung</li><li>Mitfahrstatus</li><li>Live-Sportergebnisse</li></ul> |
| 2 | Verringern der Benachrichtigungsmüdigkeit | Eine einzelne Aktivität wird aktualisiert, anstatt wiederholte Push-Benachrichtigungen auszulösen | <ul><li>Auftragsvorbereitung und Lieferetappen</li><li>Flugbrett und Gate-Updates</li></ul> |
| 3 | Zeitkritischer, kurzlebiger Kontext | Ideal für Aktivitäten mit klarem Start und Ende | <ul><li>Countdowns der Bordsteinabfrage</li><li>Workout- oder Timer-Sitzungen</li></ul> |
| 4 | Native, überschaubare Benutzeroberfläche | Verwendet betriebssystemnative Oberflächen (Dynamic Island, Sperrbildschirm, Benachrichtigungsschattierung) für ein gut sichtbares, reibungsarmes Erlebnis | <ul><li>Package-Tracking</li><li>Warteschlangen- oder Wartezeit-Updates</li></ul> |

## Wenn *Live* Aktivitäten verwenden möchten

* Bei lang laufenden oder offenen Status ohne klares Ende: Beenden Sie die Aktivität, sobald der zugrunde liegende Prozess abgeschlossen ist.
* Für Werbe- oder Marketing-Inhalte - verwenden Sie stattdessen Push-Benachrichtigungen, In-App-Nachrichten oder Inhaltskarten.
* Wenn die Aktualisierungskadenz sehr hoch ist - häufige Aktualisierungen können vom Betriebssystem gedrosselt werden oder für den Benutzer laut sein.
* Wenn Ihre App die für iOS Live-Aktivitäten oder Android Live-Updates erforderlichen Betriebssystemversionen nicht unterstützt.
