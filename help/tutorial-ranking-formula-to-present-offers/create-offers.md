---
title: Erstellen von standortbasierten Angeboten mit Postleitzahl-Targeting
description: Ein Angebotselement in Decisioning stellt ein einzelnes Element personalisierter Inhalte dar, z. B. eine Nachricht, ein Bild, eine Promotion oder eine Empfehlung, die einem Benutzer auf der Grundlage definierter Regeln und Bedingungen bereitgestellt werden können.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-30T00:00:00Z
jira: KT-18188
exl-id: 7dd49746-bea6-4679-9d88-d8f9d2aa5b52
source-git-commit: fb0ef6d502c6e3ba37ef528683a8888ed83f2990
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%

---

# Erstellen von standortbasierten Angeboten mit Postleitzahl-Targeting

Vor der Erstellung der Angebote wurde das Schema der Angebotsposition um ein neues Feld erweitert: Postleitzahl. Dieses benutzerdefinierte Feld ermöglicht es, jedes Angebot explizit mit seiner Ziel-Postleitzahl zu versehen, was eine standortbasierte Filterung und Rangfolge während der Entscheidungsfindung ermöglicht.

Mit der Aktualisierung des Schemas wurden zwei personalisierte Angebote erstellt:

* Angebot 1: „Flexible Investitionspläne für Mira Mesa (92126)“
Dieses Angebot ist auf junge Fachkräfte und technologieorientierte Anwohner in 92126 zugeschnitten und fördert flexible Anlageoptionen wie ETFs und Fonds auf Gegenseitigkeit, die auf langfristiges Wachstum abzielen. Das Feld Postleitzahl ist auf 92126 festgelegt.

* Angebot 2: „High-Yield-CDs für Rancho Bernardo (92128)“
Dieses Angebot richtet sich an finanziell stabile und zur Rente bereite Personen in 92128. Es bietet erstklassige Einlagenzertifikate (CDs) mit garantierten Renditen. Das Feld Postleitzahl ist auf 92128 festgelegt.

Diese Angebote sind jetzt mit Standort-Metadaten angereichert, sodass sie für die dynamische Auswahl und das Ranking auf der Grundlage der Postleitzahlen der Benutzerprofile in späteren Schritten in Frage kommen.

Der folgende Screenshot zeigt die benutzerdefinierten Attribute, die zum Angebotselementschema hinzugefügt wurden.

![offers-meta-data](assets/offers-meta-data.png)


## Angebot für 92126

Der Angebotstext für Angebote in 92126 Postleitzahl

```html
<div style="max-width: 600px; margin: 2rem auto; padding: 1.5rem; border: 1px solid #ddd; border-radius: 12px; font-family: Arial, sans-serif; background-color: #f9f9f9; box-shadow: 0 4px 12px rgba(0,0,0,0.05);">   <h2 style="color: #1a237e; font-size: 1.5rem; margin-bottom: 0.5rem;">     Boost Your Financial Game with Smart Investment Options   </h2>   <p style="color: #333; font-size: 1rem; line-height: 1.6;">     In Mira Mesa (92126), ambition meets opportunity. Whether you're building wealth or just getting started, our     <strong>diversified investment plans</strong> — including <strong>tech-focused ETFs</strong> and     <strong>flexible mutual funds</strong> — are designed to grow with your goals.   </p>   <p style="color: #333; font-size: 1rem; line-height: 1.6;">     Enjoy expert guidance, low fees, and strategies built for busy professionals who want more from their money — without the hassle.   </p>   <a href="#start-investing" style="display: inline-block; margin-top: 1rem; background-color: #1a73e8; color: white; padding: 0.75rem 1.25rem; border-radius: 8px; text-decoration: none; font-weight: bold;">     Start Investing Smarter   </a> </div>
```


## Angebot für 92128

Der Angebotstext für Angebote in 92128 Postleitzahl

```html
<div style="max-width: 600px; margin: 2rem auto; padding: 1.5rem; border: 1px solid #ddd; border-radius: 12px; font-family: Arial, sans-serif; background-color: #fdfdfd; box-shadow: 0 4px 12px rgba(0,0,0,0.05);">   <h2 style="color: #1a237e; font-size: 1.5rem; margin-bottom: 0.5rem;">     Grow Your Savings with Confidence – Exclusive CD Rates for 92128   </h2>   <p style="color: #333; font-size: 1rem; line-height: 1.6;">     Live in Rancho Bernardo? Take advantage of your financial momentum with our <strong>high-yield Certificates of Deposit</strong>, offering up to <strong>5.25% APY</strong>.     Designed for peace of mind and smart growth, our flexible CD options let you lock in guaranteed returns while enjoying the stability you deserve.   </p>   <p style="color: #333; font-size: 1rem; line-height: 1.6;">     Whether you're planning retirement or simply securing your future, this offer is tailored for residents like you.   </p>   <a href="#explore-cd-options" style="display: inline-block; margin-top: 1rem; background-color: #1a73e8; color: white; padding: 0.75rem 1.25rem; border-radius: 8px; text-decoration: none; font-weight: bold;">     Explore CD Options   </a> </div>
```

## Generisches Angebot (Fallback-Angebot)

Der Angebotstext für das generische Angebot ohne mit dem Angebot verknüpfte Postleitzahl

```html
<div style="max-width: 600px; margin: 2rem auto; padding: 1.5rem; border: 1px solid #ddd; border-radius: 12px; font-family: Arial, sans-serif; background-color: #ffffff; box-shadow: 0 4px 12px rgba(0,0,0,0.05);">
  <h2 style="color: #1a237e; font-size: 1.5rem; margin-bottom: 0.5rem;">
    Invest Smarter: Build Wealth with Flexible Financial Plans
  </h2>
  <p style="color: #333; font-size: 1rem; line-height: 1.6;">
    Looking to take control of your financial future? Our flexible investment solutions are designed to meet a wide range of goals — from growing savings to planning for retirement.
    Choose from diversified mutual funds, ETFs, and professionally managed portfolios, all with expert guidance and minimal hassle.
  </p>
  <p style="color: #333; font-size: 1rem; line-height: 1.6;">
    Whether just starting out or optimizing an existing strategy, this offer provides the tools to invest with confidence — no matter where you live.
  </p>
  <a href="#explore-investment-plans" style="display: inline-block; margin-top: 1rem; background-color: #1a73e8; color: white; padding: 0.75rem 1.25rem; border-radius: 8px; text-decoration: none; font-weight: bold;">
    Explore Investment Plans
  </a>
</div>
```

Gruppieren Sie diese Angebote in einer Sammlung **einkommensbezogene Angebote**

Die Angebote stehen allen Besuchern zur Verfügung, d. h. es gibt keine strengen Eignungsbegrenzungen. Anschließend wird die Rangfolgenformel wichtig, um anhand des Profilkontexts zu bestimmen, welches Angebot angezeigt werden soll.
Da die Eignungsregeln die Angebote nicht filtern, werden alle drei als Kandidaten behandelt.
Die Auswahlstrategie ruft alle drei ab.
Die Rangfolgeformel bewertet sie anhand von Profilattributen (wie Postleitzahl und Jahreseinkommen), um das beste auszuwählen.
