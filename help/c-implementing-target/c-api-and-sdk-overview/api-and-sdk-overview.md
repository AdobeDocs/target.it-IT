---
description: Informazioni sulle API di distribuzione sul lato server di Target, sulle API di consigli e su SDK di NodeJS.
keywords: lato server;api;sdk;nodejs;node js;api Recommendations
seo-description: Informazioni sulle API di consegna lato server di Adobe Target, sulle API di Recommendations e sull'SDK nodejs.
seo-title: Implementazione lato server di Adobe Target
solution: Target
title: 'Lato server: implementare Target'
topic: Consigli
uuid: 21d321c7-3da4-44a2-a04f-1807cc2a893b
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Lato server: implementare Target{#server-side-implement-target}

Information about [!DNL Adobe Target] Server Side delivery APIs, Server Side Batch Delivery APIs, NodeJS SDK, [!DNL Target Recommendations] APIs, and [!DNL Target Classic] APIs (decommissioned).

The following process occurs in a server-side implementation of [!DNL Target]:

1. Un dispositivo client richiede una richiesta di un'esperienza attraverso il server.
1. Your server sends that request to [!DNL Target].
1. [!DNL Target] reindirizza la risposta al server.
1. Il server decide quale esperienza distribuire al dispositivo client per il rendering.

L'esperienza non deve essere visualizzata in un browser; può essere visualizzato in un'e-mail o in un messaggio, tramite un assistente vocale o tramite altre esperienze non visive o non basate su browser. Because your server sits between the client and [!DNL Target], this type of implementation is also ideal if you need greater control and security or have complex backend processes that you want to run on your server.

La sezione seguente elenca le varie API e l’SDK di NodeJS e fornisce ulteriori informazioni:

## API di distribuzione lato server

Link: [Server Side Delivery APIs](https://developers.adobetarget.com/api/#server-side-delivery)

`/rest/v1/mbox`

[!DNL Target] consente all'applicazione di effettuare chiamate mbox da qualsiasi browser, dispositivo mobile o persino un altro server. The Server Side delivery API is specifically designed to integrate [!DNL Target] with any server-side platform that makes HTTP/HTTPS calls.

Puoi utilizzare l'API per integrare l'applicazione personalizzata con [!DNL Target]. Ciò è particolarmente importante per le organizzazioni che desiderano distribuire targeting a un dispositivo IoT non basato su browser, ad esempio una TV collegata, un kiosk o uno schermo digitale specializzato.

Questo parametro può restituire offerte solo per mbox normali. Puoi anche recuperare il contenuto per un solo mbox.

Questa API implementa le funzioni mbox esistenti in un sistema REST.

Questa API non elabora i cookie o le chiamate di reindirizzamento.

## API di distribuzione lato server

Link: [Server Side Batch Delivery APIs](https://developers.adobetarget.com/api/#server-side-batch-delivery)

`/rest/v2/batchmbox`

L'API di distribuzione in batch consente all'applicazione di richiedere il contenuto di più mbox in una singola chiamata. It also has a prefetch mode that enables clients like mobile apps, servers, and so forth to fetch content for multiple mboxes in one request, cache it locally, and later notify [!DNL Target] when the user visits those mboxes.

Questo parametro può restituire offerte solo per mbox normali. Poiché è possibile recuperare contenuto per più mbox, per la prestazione, l'API di mbox consente di utilizzare il linguaggio mbox. Consente di evitare l'esecuzione di più richieste HTTP, che possono essere dispendiose.

## SDK di NodeJS

Link: [NodeJS SDK](https://www.npmjs.com/package/@adobe/target-node-client)

In termini di SDK, attualmente abbiamo un solo SDK, l'SDK di NodeJS.

L'SDK di NodeJS è un sottile involucro del modulo HTTP/HTTPS principale di NodeJS. In realtà, le API di NodeJS SDK utilizzano le stesse API di distribuzione lato server.

Di seguito è riportata la mappatura:

* `MarketingCloudClient.getOffer() \*- invokes \*/res/v1/mbox endpoint`
* `MarketingCloudClient.getOffers() \*- invokes \*/res/v2/batchmbox endpoint`

## [!DNL Target Recommendations] API

Link: [Target Recommendations APIs](https://developers.adobetarget.com/api/recommendations)

Le API di consigli consentono di interagire a livello di codice con i server di consigli di Target. Queste API possono essere integrate con una serie di applicazioni per eseguire funzioni che vengono normalmente eseguite mediante l'interfaccia utente.

## [!DNL Target Classic] API

[!DNL Target Classic] L'interfaccia utente e le API sono state disattivate. Per informazioni sul passaggio alle API moderne di Target, consulta [Passaggio dalle API Target obsolete ad Adobe I/O](../../c-implementing-target/c-api-and-sdk-overview/target-api-documentation.md#concept_3A31E26C8FAF49598152ACFE088BD4D2).

>[!NOTE]
>Le API di authoring (in cui si creano attività, offerte, tipi di pubblico e così via) non supportano la condivisione delle risorse tra diverse origini (Cross Origin Resource Sharing, CORS).

## Differenze tra le API di distribuzione lato server e SDK di NodeJS {#section_10336B7934F54CE98E35907A4748A4A4}

Molti clienti hanno dei dubbi a proposito delle differenze tra le API di distribuzione lato server e l'SDK di NodeJS. Ciò è particolarmente vero quando si tratta di prestazioni.

Le domande frequenti seguenti dovrebbero aiutarti a decidere quale utilizzare:

**Quando si utilizzano le API Server “pure” rispetto all'SDK di NodeJS?**

Se si utilizza NodeJS come tecnologia backend, SDK di NodeJS SDK è una scelta naturale. L'SDK gestisce molti dettagli, quali cookie, intestazioni, payload e così via. Ciò consente di concentrarsi sul nucleo dell'applicazione.

**Sono stati apportati miglioramenti a livello di prestazioni utilizzando l'SDK di NodeJS?**

Purtroppo non sono presenti numeri di prestazioni. Tuttavia, in generale, l'SDK di NodeJS dovrebbe offrire prestazioni migliori grazie all'architettura basata su eventi NodeJS. Be aware that most of the time is spent on the [!DNL Target] backend. L'SDK di NodeJS è molto ridotto. The SDK is basically responsible for packaging a [!DNL Target] request and parsing a [!DNL Target] response.
