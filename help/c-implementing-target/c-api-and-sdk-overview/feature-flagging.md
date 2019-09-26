---
description: I team di prodotti tecnologici contemporanei stanno adottando principi di consegna continua per il lancio di prodotti. Target consente agli sviluppatori e ai team di prodotto di distribuire nuove funzionalità di prodotto in modo rapido ed efficiente.
keywords: rollout;rollout;consegna continua;avvio prodotto;rollout graduale
seo-description: I team di prodotti tecnologici contemporanei stanno adottando principi di consegna continua per il lancio di prodotti. Adobe Target consente agli sviluppatori e ai team di prodotto di distribuire nuove funzionalità di prodotto in modo rapido ed efficiente in un'implementazione graduale.
seo-title: I team di prodotti tecnologici contemporanei stanno adottando principi di consegna continua per il lancio di prodotti. Adobe Target consente a sviluppatori e team di prodotti di distribuire nuove funzionalità di prodotto in modo rapido ed efficiente.
solution: Target
title: Flagging delle funzioni
topic: Standard
translation-type: tm+mt
source-git-commit: 08debab3ec3d2f6e6bfd3c42476dc1a021185ab7

---


# Flagging delle funzioni

I team di prodotti tecnologici contemporanei stanno adottando principi di consegna continua per il lancio di prodotti. Adobe Target consente agli sviluppatori e ai team di prodotto di distribuire nuove funzionalità di prodotto in modo rapido ed efficiente in un'implementazione graduale.

I seguenti collegamenti forniscono informazioni sui concetti chiave da comprendere per abilitare la distribuzione continua:

* [Attività di test A/B](/help/c-activities/t-test-ab/test-ab.md)
* [Offerte JSON](/help/c-experiences/c-manage-content/create-json-offer.md)
* [Miglioramenti del pubblico](/help/c-target/c-audiences/creating-a-profile-attribute-comparison-audience.md)

## Consegna continua

1. Per impostazione predefinita, quando viene rilasciata, la funzione è disattivata.

   Utilizzate una variabile lato server o in-app per controllarla.

1. Create un'offerta JSON Target che imposti questa variabile su "on".

1. Create un'attività di test A/B in [](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md) Visual Experience Composer (VEC) con due esperienze e utilizzate l'offerta JSON creata nel passaggio precedente in un'esperienza.

   Oppure

   Create un'attività di test A/B in [Form-Based Experience Composer](/help/c-experiences/form-experience-composer.md) con una singola esperienza e utilizzate l'offerta JSON creata nel passaggio precedente.

   >[!NOTE]
   >
   >Experience Composer basato su modulo consente di creare un'attività di test A/B con una singola esperienza. Non potete creare l'attività con una singola esperienza utilizzando il VEC.

1. Specificate l'allocazione di traffico desiderata per l'attività.

   Se desiderate iniziare a distribuire questa funzione al 5% dei visitatori, specificate 5 nel passaggio Targeting del flusso di lavoro guidato in tre parti e inviate il 100% dei visitatori idonei all'esperienza con l'offerta JSON (Esperienza A).

   L'illustrazione seguente mostra il VEC con due esperienze.

   ![Traffic allocation for feature flagging in the VEC](/help/c-implementing-target/c-api-and-sdk-overview/assets/feature-flagging.png)

   L'illustrazione seguente mostra Experience Composer basato su modulo con una singola esperienza.

   ![Traffic allocation for feature flagging in the Form-based Experience Composer](/help/c-implementing-target/c-api-and-sdk-overview/assets/feature-flagging-form.png)

1. You can increase the traffic allocation to this activity by gradually increasing the 5% either through the Target UI or using the API until you reach 100% traffic allocation.

   >[!NOTE]
   >
   >An A/B Test activity is sticky for a visitor through the session. If you decrease the traffic allocation, visitors who started seeing this feature continue to view it until their sessions are reset.

## Funzioni di test A/B

Se utilizzi A/B/..N Funzioni di test, utilizzate l'approccio sopra descritto con i seguenti miglioramenti:

* Each feature variant should be represented using an appropriate JSON offer that makes a Target experience.
* È possibile gestire l'allocazione del traffico per questo test come descritto in precedenza.

## Parametrized rollouts

Il metodo descritto sopra consente di gestire un rollout controllato.

You can roll out a feature for your beta participants only and then later roll out the feature to all other customers. This can be easily achieved by leveraging Target Location (mbox) parameters or profile parameters. [](/help/c-target/c-audiences/c-target-rules/custom-parameters.md)[](/help/c-target/c-audiences/c-target-rules/visitor-profile.md) These parameters can be used in conjunction with phased traffic allocation.

## Server-side vs. client-side

Feature rollouts and testing can be delivered via Target APIs (and server-side SDKs) as well as the client side SDKs (JS, Mobile SDK). [](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md) Depending on how your website, mobile app, or kiosk is architected, you can leverage Target's different integration options.
