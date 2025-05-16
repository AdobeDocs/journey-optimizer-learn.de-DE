---
title: Importieren von CRM-Beispieldaten in den AEP-Profildatensatz
description: Importieren Sie Beispieldatensätze (z. B. mit CRMID, E-Mail, Einkommen, Postleitzahl), um zu überprüfen, ob AEP diese Profile anhand freigegebener Kennungen wie ECID korrekt mit anonymen Web-Besuchern verknüpfen kann.
feature: Profiles
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-19T00:00:00Z
jira: KT-18089
source-git-commit: 502cdc41b666959141ff4dfc63608cc463009811
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 6%

---

# Importieren von CRM-Beispieldaten in den AEP-Profildatensatz

Um mit der Identitätszuordnung zu beginnen, importieren Sie CRM-Beispielprofildaten in einen Datensatz, der mit einem profilaktivierten Schema in Adobe Experience Platform verknüpft ist

## Benutzerdefinierten Namespace erstellen

* Navigieren Sie zu Kunde > Identitäten > Identity-Namespace erstellen .
* Wählen Sie Individuelle geräteübergreifende ID und geben Sie den Anzeigenamen und das Identitätssymbol an, wie im folgenden Screenshot gezeigt.
  ![custom-namespace](assets/custom-namespace.png)

## Erstellen eines profilaktivierten Schemas

Erstellen Sie ein individuelles Profilschema mit dem Namen **_FinWiseProfileSchema_**. Schließen Sie Felder wie „AnnualIncome“, „Email“, „firstName“, „lastName“ und „LoyaltyStatus“ ein.
Fügen Sie ein Identitätsfeld **_crmid_** unter dem SystemIdentifier-Objekt hinzu. Das Feld „crmid“ als Identität und primär markieren


![profile-schema](assets/finwise-profile-schema.png)

## Vorbereiten von Beispieldaten

| crmId | firstName | lastName | E-Mail | Loyalitätsstatus | Jahreseinkommen |
|--------|-----------|----------|---------------------------|---------------|--------------|
| FIN001 | Alice | Falsch | alice.wong@example.com | Gold | 336104 |
| FIN002 | Brian | Smith | brian.smith@example.com | Silber | 191065 |
| FIN003 | Cathy | Johnson | cathy.johnson@example.com | Bronze | 117015 |
| FIN004 | David | Lee | david.lee@example.com | Bronze | 61869 |
| FIN005 | EVA | Martinez | eva.martinez@example.com | Silber | 191371 |
| FIN006 | freimütig | Braun | frank.brown@example.com | Silber | 196132 |
| FIN007 | Anmut | Kim | grace.kim@example.com | Gold | 309851 |
| FIN008 | Henry | Davis | henry.davis@example.com | Gold | 318378 |
| FIN009 | Isla | Clark | isla.clark@example.com | Silber | 181776 |
| FIN010 | Wagenheber | Lopez | jack.lopez@example.com | Silber | 186643 |

## Aufnehmen der CSV-Datei

* Erstellen Sie einen Datensatz mit dem **_FinWiseCustomerDataSetWithAnnualIncome_**, basierend auf dem **_FinWiseProfileSchema_**, der im vorherigen Schritt erstellt wurde

* Navigieren Sie zu Verbindungen > Quellen > Lokales System
* Wählen Sie **_Daten hinzufügen_** unter Lokaler Datei-Upload aus. Wählen Sie unbedingt _**FinWiseCustomerDataSetWithAnnualIncome**_ als Zieldatensatz aus.
  ![ingest-csv](assets/ingest-csv-into-dataset.png)
* Navigieren Sie zum nächsten Bildschirm. Laden Sie die [CSV-Datei](assets/sample_crm_data.csv) hoch und überprüfen Sie die Zuordnungen
  ![Zuordnungen](assets/mappings.png)

* Klicken Sie auf Beenden , um die Datenaufnahme zu starten

## Profil überprüfen

* Navigieren Sie zu Kunde > Profile und suchen Sie nach der FinWise CRM ID gleich FIN001 oder einem anderen gültigen Wert
  ![verify-profile](assets/verify-profiles.png)
