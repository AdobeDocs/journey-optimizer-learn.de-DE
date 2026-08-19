---
title: Erste Schritte mit der Journey Optimizer-Treue
description: Erfahren Sie, wie Sie sich an der Adobe Journey Optimizer-Treue beteiligen, eine Herausforderung konfigurieren, sie anwenden und anzeigen und ihre Leistung analysieren können.
topic: Get Started
role: User
level: Beginner
doc-type: Tutorial
jira: KT-21773
last-substantial-update: 2026-07-28T00:00:00Z
source-git-commit: e1b213bdc6e44fd7943d6e345c136697c8f1ee3c
workflow-type: tm+mt
source-wordcount: '1171'
ht-degree: 43%

---


# Erste Schritte mit der Journey Optimizer-Treue

Mit Treue-Challenges können Sie ansprechende, spielerisch gestaltete Treueprogramme entwickeln, die das Kundenverhalten positiv beeinflussen und die Markenbindung stärken. Stellen Sie Herausforderungen auf, die Kunden für bestimmte Aktionen belohnen, von Käufen und dem Schreiben von Rezensionen bis hin zur Interaktion mit Social Media und Verweisen auf Freunde.

## Einführung in die Treue

In diesem Abschnitt wird Journey Optimizer Loyalty vorgestellt: Was es ist, wo es sich unter Adobe Journey Optimizer befindet und der Challenge-Lebenszyklus von der Einrichtung bis zur Analyse.

<!--
CARDS

* https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/loyalty/discover-journey-optimizer-loyalty
  {description = Understand what Journey Optimizer Loyalty is, where it sits under AJO, and the challenge lifecycle.}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Discover Journey Optimizer Loyalty">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/loyalty/discover-journey-optimizer-loyalty" title="Journey Optimizer-Treue entdecken" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3496441/?format=jpeg&nocache=1787096895391" alt="Journey Optimizer-Treue entdecken"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/loyalty/discover-journey-optimizer-loyalty" target="_blank" rel="referrer" title="Journey Optimizer-Treue entdecken">Entdecken Sie Journey Optimizer-Treue</a>
                    </p>
                    <p class="is-size-6">Erfahren Sie, was Journey Optimizer Loyalty ist, wo sie unter AJO steht und wie der Challenge-Lebenszyklus aussieht.</p>
                </div>
                <a href="https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/loyalty/discover-journey-optimizer-loyalty" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Ansehen</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

## Einrichten von Treue

Dieser Abschnitt behandelt die anfängliche einmalige Einrichtung, die erforderlich ist, bevor Sie mit der Erstellung einer Herausforderung beginnen können.


<!--
CARDS

* ./set-up-loyalty/set-up-a-loyalty-reward-provider.md
  {description = Learn how to set up a reward provider, create reward definitions, and configure reward payloads so Adobe Journey Optimizer can issue loyalty rewards through your external rewards system.}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Set up a loyalty reward provider">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="./set-up-loyalty/set-up-a-loyalty-reward-provider.md" title="Einrichten eines Anbieters für Treueprämien" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3497346/?format=jpeg&nocache=1787096895737" alt="Einrichten eines Anbieters für Treueprämien"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="./set-up-loyalty/set-up-a-loyalty-reward-provider.md" target="_blank" rel="referrer" title="Einrichten eines Anbieters für Treueprämien">Richten Sie einen Anbieter für Treueprämien ein</a>
                    </p>
                    <p class="is-size-6">Erfahren Sie, wie Sie einen Belohnungsanbieter einrichten, Belohnungsdefinitionen erstellen und Belohnungs-Payloads konfigurieren, damit Adobe Journey Optimizer Treueprämien über Ihr externes Belohnungssystem ausstellen kann.</p>
                </div>
                <a href="./set-up-loyalty/set-up-a-loyalty-reward-provider.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Ansehen</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

## Herausforderung konfigurieren

Dieser Abschnitt führt Sie schrittweise durch die Erstellung und Konfiguration einer Herausforderung zum Treueprogramm: Typ, Struktur und Zeitplan, Aufgaben und Belohnungen.


<!--
CARDS

* ./configure-your-challenge/set-up-a-loyalty-challenge.md
  {description = Learn how to set up a loyalty challenge by selecting the right challenge type, configuring audiences and schedules, defining participation rules, and controlling how progress is tracked and rewarded.}
* ./configure-your-challenge/create-tasks.md
  {description = Learn how to set up tasks: purchase & spend, quantities, eligible items & exclusions, and reuse.}
* ./configure-your-challenge/configure-rewards.md
  {description = Learn how to configure rewards: provider, milestone vs. completion delivery, reward types & coupons.}
* ./configure-your-challenge/create-a-challenge-and-get-insights-with-cx-enterprise-coworker.md
  {description = Learn how to use CX Enterprise Coworker to create, configure, and launch loyalty challenges using natural language, including audiences, rewards, schedules, and automated journey setup.}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Set up a loyalty challenge">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="./configure-your-challenge/set-up-a-loyalty-challenge.md" title="Herausforderung „Treue“ einrichten" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3496471/?format=jpeg&nocache=1787096896047" alt="Herausforderung „Treue“ einrichten"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="./configure-your-challenge/set-up-a-loyalty-challenge.md" target="_blank" rel="referrer" title="Herausforderung „Treue“ einrichten">Richten Sie eine Herausforderung bezüglich der Treue ein</a>
                    </p>
                    <p class="is-size-6">Erfahren Sie, wie Sie eine Herausforderung für das Treueprogramm einrichten, indem Sie den richtigen Herausforderungstyp auswählen, Audiences und Zeitpläne konfigurieren, Teilnahmeregeln definieren und steuern, wie der Fortschritt verfolgt und belohnt wird.</p>
                </div>
                <a href="./configure-your-challenge/set-up-a-loyalty-challenge.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Ansehen</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Create tasks for your loyalty challenge">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="./configure-your-challenge/create-tasks.md" title="Aufgaben für die Herausforderung „Treue“ erstellen" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3496442/?format=jpeg&nocache=1787096896055" alt="Aufgaben für die Herausforderung „Treue“ erstellen"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="./configure-your-challenge/create-tasks.md" target="_blank" rel="referrer" title="Aufgaben für die Herausforderung „Treue“ erstellen">Erstellen Sie Aufgaben für Ihre Herausforderung zur Treue</a>
                    </p>
                    <p class="is-size-6">Erfahren Sie, wie Sie Aufgaben einrichten: Einkauf und Ausgaben, Mengen, geeignete Artikel und Ausschlüsse sowie Wiederverwendung.</p>
                </div>
                <a href="./configure-your-challenge/create-tasks.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Ansehen</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Configure rewards">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="./configure-your-challenge/configure-rewards.md" title="Konfigurieren von Prämien" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3496481/?format=jpeg&nocache=1787096896071" alt="Konfigurieren von Prämien"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="./configure-your-challenge/configure-rewards.md" target="_blank" rel="referrer" title="Konfigurieren von Prämien">Konfigurieren von Belohnungen</a>
                    </p>
                    <p class="is-size-6">Erfahren Sie, wie Sie Belohnungen konfigurieren: Anbieter, Meilenstein vs. Abschluss des Versands, Belohnungstypen und Gutscheine.</p>
                </div>
                <a href="./configure-your-challenge/configure-rewards.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Ansehen</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Create a loyalty challenge and surface insights with CX Enterprise Coworker">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="./configure-your-challenge/create-a-challenge-and-get-insights-with-cx-enterprise-coworker.md" title="Erstellen Sie mit CX Enterprise Coworker eine Herausforderung bezüglich der Kundentreue und gewinnen Sie Erkenntnisse." target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3496528/?format=jpeg&nocache=1787096896064" alt="Erstellen Sie mit CX Enterprise Coworker eine Herausforderung bezüglich der Kundentreue und gewinnen Sie Erkenntnisse."
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="./configure-your-challenge/create-a-challenge-and-get-insights-with-cx-enterprise-coworker.md" target="_blank" rel="referrer" title="Erstellen Sie mit CX Enterprise Coworker eine Herausforderung bezüglich der Kundentreue und gewinnen Sie Erkenntnisse.">Mit CX Enterprise Coworker eine Herausforderung für die Kundentreue schaffen und Erkenntnisse gewinnen</a>
                    </p>
                    <p class="is-size-6">Erfahren Sie, wie Sie mit CX Enterprise Coworker Treueprobleme mithilfe natürlicher Sprache erstellen, konfigurieren und starten können, einschließlich Zielgruppen, Belohnungen, Zeitplänen und automatisierter Journey-Einrichtung.</p>
                </div>
                <a href="./configure-your-challenge/create-a-challenge-and-get-insights-with-cx-enterprise-coworker.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Ansehen</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

## Herausforderung anwenden und anzeigen

In diesem Abschnitt erfahren Sie, wie Sie Ihren Kunden durch Inhaltskarten und Code-basierte Erlebnisse eine Herausforderung bieten können.

<!--
CARDS

* ./apply-and-display-your-challenge/build-a-challenge-content-card.md
  {description = Learn how to build a challenge content card / code-based experience, covering opt-in and dynamic progress across the opt-in, progress, and completed stages, plus rewards and channel configuration.}
* ./apply-and-display-your-challenge/display-challenge-content-using-code-based-experience-channel.md
  {dewcription = Learn how to use code-based experiences to promote loyalty challenges, display challenge progress, and deliver personalized content within your app using HTML or JSON.}
* ./apply-and-display-your-challenge/set-up-lifecycle-messaging-for-your-challenge.md
  {description = Learn how to configure multi-channel messaging for every stage of a loyalty challenge, from invitations and engagement messages to completion and reward notifications.}
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Build a challenge content card">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="./apply-and-display-your-challenge/build-a-challenge-content-card.md" title="Erstellen einer Challenge-Inhaltskarte" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3496529/?format=jpeg&nocache=1787096896398" alt="Erstellen einer Challenge-Inhaltskarte"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="./apply-and-display-your-challenge/build-a-challenge-content-card.md" target="_blank" rel="referrer" title="Erstellen einer Challenge-Inhaltskarte">Erstellen einer Challenge-Inhaltskarte</a>
                    </p>
                    <p class="is-size-6">Erfahren Sie, wie Sie eine Challenge-Inhaltskarte / ein Code-basiertes Erlebnis erstellen, in dem Opt-in und dynamischer Fortschritt für das Opt-in, der Fortschritt und die abgeschlossenen Phasen sowie Belohnungen und die Kanalkonfiguration behandelt werden.</p>
                </div>
                <a href="./apply-and-display-your-challenge/build-a-challenge-content-card.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Ansehen</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Display challenge content using the code-based experience channel">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="./apply-and-display-your-challenge/display-challenge-content-using-code-based-experience-channel.md" title="Anzeigen von Challenge-Inhalten mit dem Code-basierten Erlebniskanal" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3497465/?format=jpeg&nocache=1787096896404" alt="Anzeigen von Challenge-Inhalten mit dem Code-basierten Erlebniskanal"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="./apply-and-display-your-challenge/display-challenge-content-using-code-based-experience-channel.md" target="_blank" rel="referrer" title="Anzeigen von Challenge-Inhalten mit dem Code-basierten Erlebniskanal">Anzeigen von Challenge-Inhalten mit dem Code-basierten Erlebniskanal</a>
                    </p>
                    <p class="is-size-6">Erfahren Sie, wie Sie mit Code-basierten Erlebnissen Herausforderungen im Zusammenhang mit der Treue fördern, den Fortschritt bei Herausforderungen anzeigen und personalisierte Inhalte in Ihrer App mit HTML oder JSON bereitstellen können.</p>
                </div>
                <a href="./apply-and-display-your-challenge/display-challenge-content-using-code-based-experience-channel.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Ansehen</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Set up lifecycle messaging for your challenge">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="./apply-and-display-your-challenge/set-up-lifecycle-messaging-for-your-challenge.md" title="Einrichten von Lifecycle-Messaging für Ihre Herausforderung" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3497455/?format=jpeg&nocache=1787096896388" alt="Einrichten von Lifecycle-Messaging für Ihre Herausforderung"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="./apply-and-display-your-challenge/set-up-lifecycle-messaging-for-your-challenge.md" target="_blank" rel="referrer" title="Einrichten von Lifecycle-Messaging für Ihre Herausforderung">Richten Sie Lifecycle-Messaging für Ihre Herausforderung ein</a>
                    </p>
                    <p class="is-size-6">Erfahren Sie, wie Sie Multi-Channel-Messaging für jede Phase einer Herausforderung im Zusammenhang mit dem Treueprogramm konfigurieren können, von Einladungen und Interaktionsnachrichten bis hin zu Benachrichtigungen über den Abschluss und die Belohnung.</p>
                </div>
                <a href="./apply-and-display-your-challenge/set-up-lifecycle-messaging-for-your-challenge.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Ansehen</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

## Analyse und Bericht

In diesem Abschnitt wird beschrieben, wie Sie die Leistung Ihrer Herausforderungen im Rahmen des Treueprogramms messen, sobald sie live sind.

<!--
CARDS

* ./analyze-and-report/measure-performance-with-challenge-reports.md
  {description = Learn how to use challenge reports and performance dashboards to measure participation, completion rates, revenue attribution, and overall loyalty program performance.}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Measure challenge performance with challenge reports">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="./analyze-and-report/measure-performance-with-challenge-reports.md" title="Challenge-Performance mit Challenge-Berichten messen" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3497534/?format=jpeg&nocache=1787096896562" alt="Challenge-Performance mit Challenge-Berichten messen"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="./analyze-and-report/measure-performance-with-challenge-reports.md" target="_blank" rel="referrer" title="Challenge-Performance mit Challenge-Berichten messen">Challenge-Performance mit Challenge-Berichten messen</a>
                    </p>
                    <p class="is-size-6">Erfahren Sie, wie Sie Challenge-Berichte und Performance-Dashboards verwenden, um die Teilnahme, Abschlussraten, Umsatzzuordnung und die Gesamtleistung des Treueprogramms zu messen.</p>
                </div>
                <a href="./analyze-and-report/measure-performance-with-challenge-reports.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Ansehen</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->
