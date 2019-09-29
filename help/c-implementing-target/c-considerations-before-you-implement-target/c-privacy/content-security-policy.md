---
description: Informazioni sulle direttive Content Security Policy (CSP) da aggiungere quando si utilizza Adobe Target at.js 2.1 o versione successiva.
keywords: criteri di protezione del contenuto;csp;at.js;whitelist;flicker;pre-hide;pre-hide;prehide
seo-description: Informazioni sulle direttive Content Security Policy (CSP) da aggiungere quando si utilizza Adobe Target at.js 2.1 o versione successiva.
seo-title: Informativa sulla sicurezza dei contenuti (CSP)
solution: Target
subtopic: Introduzione
title: Direttive sulla sicurezza dei contenuti
topic: Standard
translation-type: tm+mt
source-git-commit: df40d69676cea586451e3b64b56ef602da91173f

---


# Direttive sulla sicurezza dei contenuti

Se utilizzi [Content Security Policy](https://en.wikipedia.org/wiki/Content_Security_Policy) (CSP) per l'implementazione di Target, quando utilizzi [at.js 2.1 o versione successiva](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)devi aggiungere le seguenti direttive CSP:

* `connect-src` con `*.tt.omtrdc.net` lista bianca. Necessario per consentire la richiesta di rete al [!DNL Target] margine.
* `style-src unsafe-inline`. Necessario per il controllo pre-occultamento e sfarfallio.
* `script-src unsafe-inline`.  Obbligatorio per consentire l'esecuzione JavaScript che potrebbe far parte di un'offerta HTML.
