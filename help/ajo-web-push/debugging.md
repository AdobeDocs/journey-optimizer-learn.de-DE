---
title: Debugging von Web Push in AJO
description: Auf dieser Seite finden Sie hilfreiche Tipps zum Debugging des Flusses von Web-Push-Benachrichtigungen, einschließlich der Überprüfung von Web SDK-Anfragen,
feature: Push
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-04-21T00:00:00Z
jira: KT-20879
source-git-commit: 45f86aeb8fca071436785cc55225d853bb21998f
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# Debugging von Web Push in AJO

Auf dieser Seite finden Sie hilfreiche Tipps zum Debugging des Flusses von Web-Push-Benachrichtigungen, einschließlich der Überprüfung von Web-SDK-Anfragen, der Überprüfung der ECID und des Benutzerprofils in AEP und der Sicherstellung, dass Ereignisse wie price.drop korrekt gesendet und empfangen werden.

- **Verwenden der Adobe Experience Platform Debugger (Chrome-Erweiterung)**\
  Installieren Sie die [AEP Debugger-Erweiterung für Chrome](https://chrome.google.com/webstore/detail/adobe-experience-platform/bfnnokhpnncpkdmbokanobigaccjkpob), um die Web-SDK-Aktivität leichter zu überprüfen:

Mit diesem Tool können Sie:
- Web SDK-Anfragen und -Antworten anzeigen\
- ECID (Experience Cloud ID) überprüfen\
- Validieren der Datenstromkonfiguration und Payloads

- **Überprüfen, ob der Benutzer identifiziert ist (ECID)**\
  Verwenden Sie den AEP-Debugger oder die Browser-Konsole, um zu bestätigen, dass eine ECID generiert wird. Diese ID wird verwendet, um Benutzende in AEP und AJO zu verfolgen.

- **Verwenden Sie die Registerkarte „Netzwerk“, um Anfragen zu überprüfen**\
  Öffnen Sie **Registerkarte Netzwerk** in den Entwickler-Tools Ihres Browsers und filtern Sie nach Anfragen, die von der Web-SDK gesendet werden (suchen Sie nach `/collect` oder `interact`).
   - Bestätigungsanfragen werden gesendet, wenn die Seite geladen wird und Aktionen ausgelöst werden
   - Überprüfen, ob das `price.drop` Ereignis in der Payload enthalten ist

- **Suchen des Benutzerprofils in AEP**\
  Verwenden Sie die ECID, um in Adobe Experience Platform nach dem Benutzerprofil zu suchen. Auf diese Weise können Sie überprüfen, ob der Benutzer erkannt wird und ob seine Daten (z. B. Push-Abonnements) korrekt gespeichert werden.

- **Überprüfen Sie, ob das `price.drop` empfangen wird**\
  Nachdem Sie das Ereignis von der Web-Seite ausgelöst haben, überprüfen Sie in AEP, ob das Ereignis aufgenommen und mit derselben ECID verknüpft wurde.
Überprüfen Sie die JSON-Datei des message.feedback-Ereignisses auf `feedback.status`. Der Statuswert sollte `sent` sein
  ![Preisverfall](assets/price-drop-profile-event.png)

- **Bestätigen, dass Push-Benachrichtigungen aktiviert sind**\
  Stellen Sie sicher, dass:
   - Der Benutzer hat die Browser-Benachrichtigungsaufforderung akzeptiert
   - Im Profil des Benutzers ist ein Push-Token vorhanden

- **Überprüfen Sie das Journey-Setup**\
  Stellen Sie sicher, dass die Journey veröffentlicht und so konfiguriert ist, dass sie auf das `price.drop` wartet.

