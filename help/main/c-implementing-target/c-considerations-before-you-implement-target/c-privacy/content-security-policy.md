---
keywords: content security policy;csp;at.js;whitelist;elenco consentiti;sfarfallio;pre-hiding;prehiding
description: Scopri le direttive Content Security Policy (CSP) da aggiungere quando utilizzi Adobe Target.
title: In che modo  [!DNL Target]  gestisce le direttive Content Security Policy (CSP)?
feature: Privacy & Security
role: Developer
exl-id: 31457b16-ed21-4540-8d0c-abfb49d1fbe9
source-git-commit: db632225d21c2e061e82269bec168341b410575a
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 29%

---

# Direttive Content Security Policy (CSP)

Se utilizzi le direttive [Content Security Policy](https://en.wikipedia.org/wiki/Content_Security_Policy) (CSP) per l’mplementazione di [!DNL Adobe Target], aggiungi le seguenti direttive CSP quando utilizzi [at.js 2.1 o versione successiva](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md):

* `connect-src` con `*.tt.omtrdc.net` inserito nell’elenco Consentiti. Necessario per consentire la richiesta di rete all’edge [!DNL Target].
* `style-src unsafe-inline`. Necessario per il controllo di pre-hiding e sfarfallio.
* `script-src unsafe-inline`. Necessario per consentire l’esecuzione di JavaScript che potrebbe far parte di un’offerta HTML.

## Domande frequenti

Consulta le seguenti domande frequenti sui criteri di sicurezza:

### I criteri di condivisione delle risorse tra diverse origini (Cross Origin Resource Sharing, CORS) e i criteri di Flash tra più domini presentano problemi di sicurezza?

Il modo consigliato per implementare il criterio CORS è quello di consentire l’accesso solo alle origini attendibili che lo richiedono tramite un inserì nell&#39;elenco Consentiti di domini affidabili. Lo stesso si può dire per la politica Flash tra domini diversi. Alcuni [!DNL Adobe Target] i clienti sono preoccupati per l&#39;uso di caratteri jolly per i domini in [!DNL Target]. Il problema è che se un utente ha effettuato l&#39;accesso a un&#39;applicazione e visita un dominio consentito dal criterio, qualsiasi contenuto dannoso in esecuzione su quel dominio può potenzialmente recuperare contenuto sensibile dall&#39;applicazione ed eseguire azioni nel contesto di sicurezza dell&#39;utente connesso. Questo viene comunemente definito CSRF (Cross-Site Request Forgery).

In un [!DNL Adobe Target] Tuttavia, l&#39;attuazione di tali politiche non dovrebbe rappresentare una questione di sicurezza.

&quot;adobe.tt.omtrdc.net&quot; è un dominio di proprietà di Adobe. [!DNL Adobe Target] è uno strumento di test e personalizzazione e si prevede che: [!DNL Target] può ricevere ed elaborare le richieste da qualsiasi luogo senza richiedere alcuna autenticazione. Queste richieste contengono coppie chiave/valore utilizzate per test A/B, consigli o personalizzazione dei contenuti.

[!DNL Adobe] non memorizza informazioni personali (PII, Personally Identifiable Information) o altre informazioni sensibili su [!DNL Adobe Target] server edge, a cui fa riferimento &quot;adobe.tt.omtrdc.net&quot;.

Ci si aspetta che [!DNL Target] è accessibile da qualsiasi dominio tramite chiamate JavaScript. L&#39;unico modo per consentire questo accesso è quello di sfruttare &quot;Access-Control-Allow-Origin&quot; con un carattere jolly.
