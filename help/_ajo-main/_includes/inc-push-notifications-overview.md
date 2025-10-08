---
source-git-commit: 201470e35095b38617d1a1bb5d7b16c1e60f431e
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 2%

---

# Übersicht über Push-Benachrichtigungen

## Was sind Push-Benachrichtigungen?

**Push-Benachrichtigungen** sind Kurznachrichten, die auf einem Smartphone, Tablet oder Computer eingeblendet werden - auch wenn der Benutzer die App, die ihn gesendet hat, nicht verwendet. Apps können damit „auf die Schulter tippen“ und so Aufmerksamkeit erregen.

Beispiel:

* Eine Shopping-App könnte Sie auf einen großen Verkauf hinweisen.
* Eine Versand-App informiert Sie möglicherweise darüber, dass Ihre Bestellung in Bearbeitung ist.
* Eine Airline-App könnte Ihnen mitteilen, dass Ihr Flug bereit zum Einchecken ist.

**Wichtig:** Der Benutzer muss der App zunächst die Berechtigung (Opt-in) erteilen, bevor er Ihnen Push-Benachrichtigungen senden kann. Dies geschieht normalerweise, wenn die App nach dem Herunterladen zum ersten Mal geöffnet wird, oder später, wenn die App während der Verwendung erneut gefragt wird. Ohne die Erlaubnis des Benutzers kann die App keine Push-Benachrichtigungen an ihr Gerät senden.

## Anwendungsfälle

Wählen Sie Push-Benachrichtigungen als bevorzugten Messaging-Kanal, wenn Sie Folgendes benötigen:

| # | Vorteil | Warum | Anwendungsbeispiele |
|---|---------|-----|-------------------|
| 1 | Zeitkritische Updates | Push-Benachrichtigungen können auf dem Sperrbildschirm oder als Banner angezeigt werden, ohne dass der Benutzer die App öffnen muss. | <ul><li> Dringende Warnmeldungen (Service-Ausfälle, Sicherheitswarnungen)</li><li>Zeitkritische Angebote (Flash-Verkäufe)</li><li> Echtzeit-Updates (Sportergebnisse, Bestellübermittlung)</ul> |
| 2 | Rückgewinnung | Push-Benachrichtigungen können inaktive Benutzende zurück in die App bringen, indem sie personalisierte und relevante Eingabeaufforderungen bereitstellen. | <ul><li> Warenkorbabbruch oder Erinnerungen zum Durchsuchen — z. B. „Sie haben Artikel in Ihrem Warenkorb gelassen — jetzt für 10 % Rabatt zur Kasse gehen.“</li></ul> |
| 3 | Verringern der Abhängigkeit von kostspieligeren Kanälen | Push-Benachrichtigungen können in der Regel kostenlos gesendet werden, sobald Sie die Infrastruktur erstellt haben, im Gegensatz zu SMS oder E-Mail, bei denen pro Nachricht Kosten entstehen. | <ul><li> Verwenden Sie für häufige Aktualisierungen Push-Benachrichtigungen anstelle von gebührenpflichtigen SMS.</li></ul> |
| 4 | Bereitstellen vielfältiger, interaktiver Inhalte | Moderne Push-APIs ermöglichen Bilder, Videos, Schnellaktionen (z. B. „Akzeptieren“ / „Ablehnen„) oder Deep-Links zu bestimmten Mobile-App-Bildschirmen. | <ul><li>Marketing-Kampagnen mit visueller Attraktivität</li><li>Schnelle Benutzeraktionen, ohne die App vollständig zu öffnen.</li></ul> |
| 5 | Nutzen von gerätenativen Funktionen | Push-Benachrichtigungen können mit iOS/Android-Betriebssystemfunktionen wie Vibrationen, Sounds, Abzeichen und Geofencing-Triggern integriert werden. | <ul><li> Standortbasierte Angebote in der Nähe eines Geschäfts</li><li> Erinnerungen werden zu bestimmten Zeiten ausgelöst.</li></ul> |
| 6 | Wann ein Opt-in wahrscheinlich ist | Push funktioniert nur für Benutzer, die sich explizit angemeldet haben. Wenn die App einen hohen Wert bietet oder die Marke bereits über Vertrauen verfügt, können die Opt-in-Raten hoch sein. | <ul><li> Apps mit loyalen Benutzerbasen</li><li> Onboarding-Abläufe, die den Wert von Benachrichtigungen erklären.</li></ul> |

## Wenn *nicht* Push als primären Kanal verwenden soll

* Niedrige Opt-in-Raten oder Benutzerwiderstand bei Benachrichtigungen.
* Bedarf an langfristigen Inhalten (E-Mail ist möglicherweise besser).
* Sensible oder sehr private Informationen (Push-Benachrichtigungen können auf Sperrbildschirmen angezeigt werden).
* Benutzende befinden sich meist auf dem Desktop und nicht in der Mobile App.
