---
source-git-commit: 0ce6d5013bbcf55e49ae920670919f6929a142ec
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 1%

---
# In-App-Nachrichten

## Was sind In-App-Nachrichten?

In-App-Nachrichten sind Nachrichten, die innerhalb einer App angezeigt werden, während der Benutzer sie aktiv verwendet. Es handelt sich um Nachrichten vom Typ Überlagerung , die sich über Ihrer App befinden. Sie werden nicht auf dem Sperrbildschirm oder außerhalb der App angezeigt. Stattdessen werden sie als Banner, Pop-ups oder kleine Karten angezeigt, während der Benutzer die App erkundet.

In-App-Nachrichten werden durch bestimmte Benutzeraktionen oder -bedingungen ausgelöst, z. B. das Anzeigen einer bestimmten Seite, das Abschließen eines Kaufs oder die Zugehörigkeit zu einem Zielgruppensegment.


Beispiel:

* Ein Spiel könnte ein Pop-up zeigen, in dem eine neue Funktion erklärt wird, sobald der Benutzer sie freischaltet.
* Eine Shopping-App zeigt beim Durchsuchen von Elementen möglicherweise ein Banner mit einem Couponcode an.
* Eine Social-Media-App könnte eine Nachricht anzeigen, die den Benutzer auffordert, neuen Konten zu folgen.

## Anwendungsfälle

| **Vorteile** | **Warum** | **Anwendungsbeispiele** |
|----------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| Hohe Benutzerinteraktion | Erfasst Benutzer, während sie in der App aktiv sind, um eine höhere Sichtbarkeit und Aktion sicherzustellen | <ul><li>Onboarding-exemplarische Vorgehensweisen</li><li>Ankündigungen zu Funktionen</li><li>Popups für Echtzeit-Support</li></ul> |
| Kontextuell relevant | Ermöglicht das Auslösen von Nachrichten durch das Benutzerverhalten, wodurch sie zeitnah und personalisiert sind | <ul><li> Upsell nach Verwendung der Funktion</li><li> Inaktivitätsstöße</li><li> Fehler- oder Erfolgsmeldungen</li></ul> |
| Versand in Echtzeit | Ermöglicht die sofortige Kommunikation für zeitkritische oder kritische Updates | <ul><li> Systemausfälle</li><li>Transaktionsbestätigungen</li><li>Zahlungsausfälle</li></ul> |
| Keine Abhängigkeit von externen Kanälen | Behält das Benutzererlebnis in Ihrem Produkt bei, ohne auf E-Mail/SMS angewiesen zu sein | <ul><li> Erinnerungen zum Abschluss des Tutorials</li><li>Warnhinweise zum Ablauf von Testversionen</li></ul> |
| Besseres Konversionspotenzial | Kontextbezogene Nachrichten konvertieren besser als plattformexterne Nachrichten | <ul><li> Upgrade-Eingabeaufforderungen nach Erreichen der Plandolimits</li><li>In-App-Umfragen</li></ul> |
| Anpassung und Segmentierung | Kann basierend auf Benutzerdaten oder App-Ereignissen personalisiert werden | <ul><li> Auf Benutzerebene oder Aktivitätsebene zugeschnittene Nachrichten</li><li> Rollenspezifische Warnhinweise </li></ul> |
| Nicht aufdringlich (wenn gut konzipiert) | Ermöglicht subtile, aber effektive Kommunikation, ohne den Benutzerfluss zu unterbrechen | <ul><li> QuickInfos</li><li>Slide-ins mit Updates</li><li>Chat-Widget-Stupser</li></ul> |


## Wenn *nicht* In-App-Kommunikation verwenden

* **Der Benutzer verwendet die App nicht aktiv**\
  In-App-Nachrichten werden nicht angezeigt, wenn der Benutzer derzeit nicht angemeldet ist oder mit Ihrem Produkt interagiert. Verwenden Sie stattdessen E-Mail oder Push.
* **Kritische oder zeitkritische Probleme, die sofortiges Eingreifen erfordern**\
  Verwenden Sie für dringende Nachrichten (z. B. Sicherheitswarnungen, Zahlungsausfälle) Kanäle, die den Benutzer außerhalb der App erreichen können, z. B. SMS oder E-Mail.
* **Regulatorische oder rechtliche Kommunikation**\
  Compliance-bezogene Nachrichten (z. B. Terminologieaktualisierungen, Richtlinienänderungen) erfordern möglicherweise eine Versand- und Lesebestätigung, die besser für E-Mails geeignet ist.
* **Account-Reaktivierung oder Win-Back-Kampagnen**\
  Wenn der/die Benutzende inaktiv ist oder abgewandert ist, werden keine In-App-Nachrichten angezeigt. Verwenden Sie Rückgewinnungskampagnen per E-Mail oder Push-Benachrichtigungen.
* **Transaktionsaktualisierungen mit hohem Volumen**\
  Benachrichtigungen wie Versandaktualisierungen oder Quittungen werden oft besser per E-Mail gesendet, um sie zu archivieren und zu vereinfachen.
* **Überbeanspruchung führt zu Bannerblindheit oder Ärger**\
  Zu viele In-App-Nachrichten auf Benutzer zu stoßen, kann den UX schaden und zu Frustration oder ignorierten Nachrichten führen.
* **Keine Konnektivität/Offline-Szenarien**\
  In-App ist davon abhängig, dass der Benutzer online und in der Sitzung ist - in Offline-First-Umgebungen ist dies nicht hilfreich.

