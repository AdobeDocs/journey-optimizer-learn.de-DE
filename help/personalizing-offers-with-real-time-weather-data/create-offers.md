---
title: Erstellen Sie Angebote, um dynamische Entscheidungen und Rangfolgen zu testen.
description: Ein Angebotselement in Decisioning stellt ein einzelnes Element personalisierter Inhalte dar, z. B. eine Nachricht, ein Bild, eine Promotion oder eine Empfehlung, die einem Benutzer auf der Grundlage definierter Regeln und Bedingungen bereitgestellt werden können.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-06-10T00:00:00Z
recommendations: noDisplay, noCatalog
jira: KT-18258
exl-id: ee940654-6c6c-42d2-8c33-e0b1dfa5c3ed
source-git-commit: 95a8abd08fbf57900870826112b01a8cd375fe96
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---

# Erstellen von Angeboten zum Testen von dynamischer Entscheidungsfindung und Rangfolge

Diese Angebote dienen dazu, dynamische Entscheidungen und Rangfolgen auf der Grundlage von kontextuellen Echtzeiteingaben (wie Temperatur) zu testen, die über die Adobe Web SDK (alloy(„sendEvent„)) weitergeleitet werden.

Vor der Erstellung der Angebote wurde das Schema der Angebotselemente um ein neues Feld erweitert: offerText

![offer-schema](assets/offer-schema.png).

Erstellen der folgenden drei Angebote


## Hot Weather Angebot (Tag:hot)

Der Angebotstext für Heißwetterangebote

```html
<div data-tags="weather hot skincare sunscreen" style="border: 1px solid #e0e0e0; padding: 1.5rem; border-radius: 10px; background-color: #fff3e0;">   <h2 style="color: #e65100;">Protect Your Skin This Summer</h2>   <p>High temperatures mean high UV risk. Get <strong>20% off</strong> our dermatologist-recommended sunscreens and skin protection kits.</p>   <p>Offer valid this week only for areas with temperatures over 90°F.</p> <button  class="ajo-cta"> Shop Sunscreen</button>   </div>
```


## Angebot für mildes Wetter (Tag:spring)

Der Angebotstext für mildes Wetter

```html
<div class="offer-content" style="text-align: center; padding: 1rem;">   <img     src="https://raw.githubusercontent.com/gbedekar489/gbedekar489.github.io/c857d12d92603daa50e9f707db0ba6ee87372eec/weather/spring.jpeg"     alt="Spring gardening scene"     style="width: 100%; max-width: 450px; border-radius: 12px; margin-bottom: 1rem;"   >   <h2>Grow More Than Just Flowers 🌿</h2>   <p>     Spring is here, and it's the perfect time to cultivate your garden — and your savings!     Enjoy <strong>$50 off</strong> when you spend $250 or more on gardening tools, seeds, and accessories.   </p>   <p><strong>Promo Code:</strong> <code>GROWSPRING</code></p>   <p><em>Offer valid through May 31. Let your garden — and your wallet — thrive.</em></p> <button  class="ajo-cta"> YES,I want this offer</button> </div>
```

## Angebot für kaltes Wetter (Tag:cold)

Der Angebotstext für das Angebot bei kaltem Wetter

```html
<div class="offer-content" style="text-align: center; padding: 1rem;">   <img src="https://raw.githubusercontent.com/gbedekar489/gbedekar489.github.io/main/weather/pexels-romanp-16170.jpg"         alt="Winter clothing"         style="width: 100%; max-width: 400px; border-radius: 12px; margin-bottom: 1rem;">   <h2>Cold Weather, Hot Deals 🧤</h2>   <p>Stay warm in style with our exclusive <strong>25% off</strong> winter outerwear. From puffer jackets to wool scarves, find the perfect layers to beat the chill.</p>   <p><strong>Use code:</strong> <code>WINTER25</code> at checkout</p>   <p><em>Limited time offer. While supplies last.</em></p><button  class="ajo-cta"> Shop Sunscreen</button> </div>
```

### Sammlung erstellen

Navigieren Sie zu **_Decisioning -> Kataloge -> Sammlung -> Sammlung erstellen_**
Benennen Sie **Sammlung „Wetterbezogene Angebote**

Gruppieren Sie diese Angebote in dieser Sammlung mithilfe des Regel-Builders.

