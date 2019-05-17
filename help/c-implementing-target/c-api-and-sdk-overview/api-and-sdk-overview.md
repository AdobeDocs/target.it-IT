---
description: Informazioni sulle API di distribuzione sul lato server di Target, sulle API di consigli e su SDK di NodeJS.
keywords: lato server;api;sdk;nodejs;node js;api Recommendations
seo-description: Informazioni sulle API di distribuzione sul lato server di Target, sulle API di consigli e su SDK di NodeJS.
seo-title: 'Lato server: implementare Target'
solution: Target
title: 'Lato server: implementare Target'
topic: 'Consigli '
uuid: 21d321c7-3da4-44a2-a04f-1807cc2a893b
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Lato server: implementare Target{#server-side-implement-target}

Informazioni su API di distribuzione Target lato server, API distribuzione in batch lato server, SDK di NodeJS, API di Target Recommendations e API di Target Classic (disattivata).

La sezione seguente elenca le varie API e l’SDK di NodeJS e fornisce ulteriori informazioni:

## API di distribuzione lato server

Collegamento: [API lato server API](https://developers.adobetarget.com/api/#server-side-delivery)

`/rest/v1/mbox`

Adobe Target consente all&#39;applicazione di effettuare chiamate mbox da qualsiasi browser, dispositivo mobile o persino un altro server. L&#39;API di distribuzione lato server è progettata appositamente per integrare Adobe Target con qualsiasi piattaforma lato server che effettua chiamate HTTP/HTTPS.

Puoi utilizzare l&#39;API per integrare l&#39;applicazione personalizzata con Target. Ciò è particolarmente importante per le organizzazioni che desiderano distribuire targeting a un dispositivo IoT non basato su browser, ad esempio una TV collegata, un kiosk o uno schermo digitale specializzato.

Questo parametro può restituire offerte solo per mbox normali. Puoi anche recuperare il contenuto per un solo mbox.

Questa API implementa le funzioni mbox esistenti in un sistema REST.

Questa API non elabora i cookie o le chiamate di reindirizzamento.

## API di distribuzione lato server

Collegamento: [API Consegna batch lato server](https://developers.adobetarget.com/api/#server-side-batch-delivery)

`/rest/v2/batchmbox`

L&#39;API di distribuzione in batch consente all&#39;applicazione di richiedere il contenuto di più mbox in una singola chiamata. Inoltre, dispone di una modalità di precarica che consente ai client come applicazioni per dispositivi mobili, server e così via di recuperare contenuti per più mbox in una richiesta, memorizzarli nella cache localmente e successivamente inviare una notifica a Target quando l&#39;utente visita questi mbox.

Questo parametro può restituire offerte solo per mbox normali. Poiché è possibile recuperare contenuto per più mbox, per la prestazione, l&#39;API di mbox consente di utilizzare il linguaggio mbox. Consente di evitare l&#39;esecuzione di più richieste HTTP, che possono essere dispendiose.

## SDK di NodeJS

Collegamento: [Nodejs SDK](https://www.npmjs.com/package/@adobe/target-node-client)

In termini di SDK, attualmente abbiamo un solo SDK, l&#39;SDK di NodeJS.

L&#39;SDK di NodeJS è un sottile involucro del modulo HTTP/HTTPS principale di NodeJS. In realtà, le API di NodeJS SDK utilizzano le stesse API di distribuzione lato server.

Di seguito è riportata la mappatura:

* `MarketingCloudClient.getOffer() \*- invokes \*/res/v1/mbox endpoint`
* `MarketingCloudClient.getOffers() \*- invokes \*/res/v2/batchmbox endpoint`

## API di consigli di Target

Collegamento: [API di Target Recommendations](https://developers.adobetarget.com/api/recommendations)

Le API di consigli consentono di interagire a livello di codice con i server di consigli di Target. Queste API possono essere integrate con una serie di applicazioni per eseguire funzioni che vengono normalmente eseguite mediante l&#39;interfaccia utente.

## API di Target Classic

L&#39;interfaccia utente di Target Classic e le API sono state disattivate. Per informazioni sul passaggio alle API moderne di Target, consulta [Passaggio dalle API Target obsolete ad Adobe I/O](../../c-implementing-target/c-api-and-sdk-overview/target-api-documentation.md#concept_3A31E26C8FAF49598152ACFE088BD4D2).

>[!NOTE]
>Le API di authoring (in cui si creano attività, offerte, tipi di pubblico e così via) non supportano la condivisione delle risorse tra diverse origini (Cross Origin Resource Sharing, CORS).

## Differenze tra le API di distribuzione lato server e SDK di NodeJS {#section_10336B7934F54CE98E35907A4748A4A4}

Molti clienti hanno dei dubbi a proposito delle differenze tra le API di distribuzione lato server e l&#39;SDK di NodeJS. Ciò è particolarmente vero quando si tratta di prestazioni.

Le domande frequenti seguenti dovrebbero aiutarti a decidere quale utilizzare:

**Quando si utilizzano le API Server “pure” rispetto all&#39;SDK di NodeJS?**

Se si utilizza NodeJS come tecnologia backend, SDK di NodeJS SDK è una scelta naturale. L&#39;SDK gestisce molti dettagli, quali cookie, intestazioni, payload e così via. Ciò consente di concentrarsi sul nucleo dell&#39;applicazione.

**Sono stati apportati miglioramenti a livello di prestazioni utilizzando l&#39;SDK di NodeJS?**

Purtroppo non sono presenti numeri di prestazioni. Tuttavia, in generale, l&#39;SDK di NodeJS dovrebbe offrire prestazioni migliori grazie all&#39;architettura basata su eventi NodeJS. Tieni presente che la maggior parte del tempo è dedicata al backend di Target. L&#39;SDK di NodeJS è molto ridotto. L&#39;SDK è praticamente responsabile della creazione di pacchetti di una richiesta Target e dell&#39;analisi di una risposta Target.
