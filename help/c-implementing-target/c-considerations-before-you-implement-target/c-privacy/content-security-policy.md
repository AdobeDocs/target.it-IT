---
keywords: content security policy;csp;at.js;whitelist;allowlist;flicker;pre-hide;pre-hiding;prehiding
description: Informazioni sulle direttive Content Security Policy (CSP) da aggiungere quando si utilizza  Adobe Target at.js 2.1 o versione successiva.
title: Informativa sulla sicurezza dei contenuti (CSP)
feature: null
subtopic: Getting Started
topic: Standard
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 5%

---


# Direttive Content Security Policy (CSP)

Se utilizzi [Content Security Policy](https://en.wikipedia.org/wiki/Content_Security_Policy) (CSP) per l&#39;implementazione di Target, quando utilizzi [at.js 2.1 o versione successiva](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)devi aggiungere le seguenti direttive CSP:

* `connect-src` con `*.tt.omtrdc.net` inserito nell&#39;elenco Consentiti. Necessario per consentire la richiesta di rete al [!DNL Target] margine.
* `style-src unsafe-inline`. Necessario per il controllo pre-occultamento e sfarfallio.
* `script-src unsafe-inline`.  Obbligatorio per consentire l&#39;esecuzione JavaScript che potrebbe far parte di un&#39;offerta HTML.
