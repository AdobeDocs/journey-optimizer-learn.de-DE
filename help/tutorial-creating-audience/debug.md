---
title: Testen der Lösung
description: Methoden zum Debuggen der Projektmappe
feature: Audiences
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-04-30T00:00:00Z
jira: KT-17923
source-git-commit: f970a1780b1bdf717675cd79c98a38ac422a679f
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# Testen der Lösung

Um Ihre Implementierung zu validieren, öffnen Sie zunächst die Web-Seite, die Ihr Präferenzformular enthält. Verwenden Sie die DevTools des Browsers (Registerkarten „Konsole“ und „Netzwerk„), um den Prozess der Formularübermittlung zu überwachen. Nachdem Sie eine Voreinstellung übermittelt haben (z. B. „Lager“ auswählen), bestätigen Sie, dass der AEP Web SDK (alloy.sendEvent) erfolgreich Trigger aufweist und dass die richtigen Daten an Adobe Experience Platform gesendet werden. Navigieren Sie in AEP zum Abschnitt Zielgruppen und stellen Sie mithilfe der Edge-Segmentierung innerhalb weniger Augenblicke sicher, dass Ihr Profil für die erwartete Zielgruppe qualifiziert ist (z. B. „Interesse an Aktien„). Sie können auch die eingehenden Ereignisdaten im zugehörigen Datensatz überprüfen, um sicherzustellen, dass er den richtigen Präferenzwert enthält. Wiederholung dieses Prozesses für jede Anlageklasse (Aktien, Anleihen, CDs), um sicherzustellen, dass der gesamte Workflow ordnungsgemäß funktioniert.

## Tipps zur Fehlerbehebung

Wenn Sie nicht sehen, dass sich das Profil sofort für die vorgesehene Zielgruppe qualifiziert, überprüfen Sie Folgendes:


### Validieren der Adobe-Datenschicht-Push

* Öffnen Sie die Entwickler-Tools-→ des Browsers
* Type console.log(window.adobeDataLayer);
* Vergewissern Sie sich, dass nach der Formularübermittlung ein Ereignis mit dem Ereignis „assetClassSelection“ und dem richtigen PreferredFinancialInstrument-Wert angezeigt wird

### Ausführung der Launch-Regel bestätigen

* Öffnen der Adobe Experience Platform Debugger (Chrome-Erweiterung)
* Beim Debugger anmelden
* Formular senden
* Überprüfen, ob das DataPush-Ereignis für AssetClassSelection erfasst wird

Der folgende Debugger-Screenshot sollte Ihnen helfen
![aep-debugger](assets/aep-debugger.png)

### Abrufen der ECID

Die ECID (Experience Cloud ID) ist die eindeutige, beständige Kennung von Adobe, mit der Benutzende über Experience Cloud-Lösungen und -Sitzungen hinweg erkannt und vereinheitlicht werden.

* Registerkarte „Netzwerk“ → Chrome Developer Tools

* Filtern nach „interagieren“ oder „sammeln“

* Formular senden
* Klicken Sie auf die Registerkarte Antwort und notieren Sie sich die ECID

![get-ecid](assets/get-ecid.png)

### Echtzeit-Profil und Zielgruppen-Qualifizierung überprüfen

* Bei Journey Optimizer anmelden
* Gehen Sie zu Kunden->Profile->Durchsuchen
* Suchen Sie nach ECID, die Sie aus dem vorherigen Schritt erhalten haben, wie im Screenshot gezeigt
  ![ecid-profile](assets/ecid-profile.png)
* Klicken Sie auf das Profil und wählen Sie die Registerkarte Ereignisse aus, um zu überprüfen, ob investment_preferences_event aufgeführt ist.
  ![events-tab](assets/profile-events.png)
* Öffnen Sie die mit dem Ereignis verknüpfte JSON und überprüfen Sie, ob sie die richtigen Ereignisdaten enthält.

### Zusätzliche Tipps zur Fehlerbehebung

* Stellen Sie sicher, dass das Schema und das Datensatzprofil aktiviert sind.
* Stellen Sie sicher, dass die Edge-Segmentierung für die Zielgruppe aktiviert ist, sodass die Qualifizierung nahezu in Echtzeit erfolgt.
* Ein paar Minuten warten und die Ansicht Zielgruppen aktualisieren kann ebenfalls hilfreich sein, insbesondere wenn Tests direkt nach der Veröffentlichung von Änderungen durchgeführt werden.
* Stellen Sie sicher, dass Zielgruppenregeln korrekt definiert sind und auf die genauen Feldnamen und Werte verweisen, die bei der Formularübermittlung erfasst werden.



