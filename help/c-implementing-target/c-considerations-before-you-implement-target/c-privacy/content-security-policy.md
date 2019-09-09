---
description: Informazioni sulle direttive CSP (Content Security Policy) da aggiungere quando si utilizza Adobe Target in. js 2.1 o versione successiva.
keywords: criteri di sicurezza dei contenuti; csp; at. js; whitelist; sfarfallio; pre-hide; pre-nascondere; prehiding
seo-description: Informazioni sulle direttive CSP (Content Security Policy) da aggiungere quando si utilizza Adobe Target in. js 2.1 o versione successiva.
seo-title: Criteri di sicurezza dei contenuti (CSP)
solution: Target
subtopic: Introduzione
title: Direttive sulla sicurezza dei contenuti (CSP)
topic: Standard
translation-type: tm+mt
source-git-commit: df40d69676cea586451e3b64b56ef602da91173f

---


# Direttive sulla sicurezza dei contenuti (CSP)

Se utilizzi [la](https://en.wikipedia.org/wiki/Content_Security_Policy) CSP (Content Security Policy) per l'implementazione di Target, aggiungi le seguenti direttive CSP quando utilizzi [at. js 2.1 o versione successiva](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md):

* `connect-src` con `*.tt.omtrdc.net` la lista bianca. Necessario per consentire la richiesta di rete al [!DNL Target] margine.
* `style-src unsafe-inline`. Obbligatorio per il controllo preliminare e sfarfallio.
* `script-src unsafe-inline`.  Richiesto per consentire l'esecuzione javascript che potrebbe far parte di un'offerta HTML.
