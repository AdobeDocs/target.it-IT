---
keywords: content security policy;csp;at.js;whitelist;elenco consentiti;sfarfallio;pre-hiding;prehiding
description: Scopri le direttive Content Security Policy (CSP) da aggiungere quando utilizzi Adobe Target.
title: In che modo  [!DNL Target]  gestisce le direttive Content Security Policy (CSP)?
feature: Privacy & Security
role: Developer
exl-id: 31457b16-ed21-4540-8d0c-abfb49d1fbe9
source-git-commit: 719eb95049dad3bee5925dff794871cd65969f79
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 90%

---

# Direttive Content Security Policy (CSP)

Se utilizzi [Informativa sulla sicurezza dei contenuti](https://en.wikipedia.org/wiki/Content_Security_Policy) (CSP) per [!DNL Adobe Target] Implementazione, aggiungi le seguenti direttive CSP quando utilizzi [at.js 2.1 o successivo](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank}:

* `connect-src` con `*.tt.omtrdc.net` inserito nell’elenco Consentiti. Necessario per consentire la richiesta di rete all’edge [!DNL Target].
* `style-src unsafe-inline`. Necessario per il controllo di pre-hiding e sfarfallio.
* `script-src unsafe-inline`. Necessario per consentire l’esecuzione di JavaScript che potrebbe far parte di un’offerta HTML.

## Domande frequenti

Domande frequenti sui criteri di sicurezza:

### I criteri di condivisione delle risorse tra diverse origini (Cross Origin Resource Sharing, CORS) e i criteri Flash tra più domini presentano problemi di sicurezza?

L’implementazione consigliata del criterio CORS consiste nel consentire l’accesso solo alle origini affidabili che lo richiedono, inserendo i domini affidabili in un elenco Consentiti. Lo stesso vale per il criterio Flash tra domini diversi. Alcuni clienti di [!DNL Adobe Target] hanno dubbi in merito all’uso di caratteri jolly nei domini in [!DNL Target]. Temono che, se un utente ha effettuato l’accesso a un’applicazione e visita un dominio consentito dal criterio, eventuali contenuti dannosi in esecuzione su tale dominio possa potenzialmente recuperare contenuti sensibili dall’applicazione ed eseguire azioni entro il contesto di sicurezza dell’utente che ha eseguito l’accesso. Questa situazione viene comunemente definita CSRF (Cross-Site Request Forgery).

Tuttavia, in un’implementazione di [!DNL Adobe Target], tali criteri non dovrebbe rappresentare problemi di sicurezza.

“adobe.tt.omtrdc.net” è un dominio di proprietà di Adobe. [!DNL Adobe Target] è uno strumento di test e personalizzazione. In quanto tale, è previsto che [!DNL Target] possa ricevere ed elaborare richieste provenienti da ovunque senza richiedere alcuna autenticazione. Tali richieste contengono coppie di chiave/valore utilizzate per test A/B, consigli o personalizzazione dei contenuti.

[!DNL Adobe] non memorizza dati personali (PII, Personally Identifiable Information) né altri dati sensibili sui server Edge di [!DNL Adobe Target] a cui fa riferimento “adobe.tt.omtrdc.net”.

È previsto che [!DNL Target] possa essere accessibile da qualsiasi dominio tramite chiamate JavaScript. L’unico modo per consentire tale accesso consiste nello sfruttare “Access-Control-Allow-Origin” con un carattere jolly.
