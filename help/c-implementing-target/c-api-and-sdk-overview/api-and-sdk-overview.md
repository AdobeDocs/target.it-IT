---
description: Informazioni sulle API di distribuzione sul lato server di Target, sulle API di consigli e su SDK di NodeJS.
keywords: lato server;api;sdk;nodejs;node js;api Recommendations
seo-description: Informazioni sulle API di distribuzione lato server di Adobe Target, sulle API di Recommendations e sull’SDK di NodeJS.
seo-title: Implementazione lato server di Adobe Target
solution: Target
title: Implementazione lato server di Target
topic: Consigli
uuid: 21d321c7-3da4-44a2-a04f-1807cc2a893b
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Lato server: implementare Target{#server-side-implement-target}

Informazioni su API di distribuzione lato server di [!DNL Adobe Target], API di distribuzione in batch lato server, SDK di NodeJS, API di [!DNL Target Recommendations] e API di [!DNL Target Classic] (dismesse).

Il processo seguente si verifica in un’implementazione lato server di [!DNL Target]:

1. Un dispositivo client richiede un’esperienza attraverso il server.
1. Il server invia la richiesta a [!DNL Target].
1. [!DNL Target] restituisce la risposta al server.
1. Il server decide quale esperienza distribuire al dispositivo client che la riprodurrà.

L’esperienza non deve necessariamente essere visualizzata in un browser; può essere visualizzata in un’e-mail o un chiosco, tramite un assistente vocale oppure tramite altre esperienze non visive o su un dispositivo non basato su browser. Poiché il server risiede tra il client e [!DNL Target], questo tipo di implementazione è ideale anche se hai bisogno di maggiore controllo e sicurezza oppure in presenza di processi di backend complessi che devono essere eseguiti sul server.

La sezione seguente elenca le varie API e l’SDK di NodeJS e fornisce ulteriori informazioni:

## API di distribuzione lato server

Link: [Server Side Delivery APIs](https://developers.adobetarget.com/api/#server-side-delivery)

`/rest/v1/mbox`

[!DNL Target] consente all’applicazione di effettuare chiamate mbox da qualsiasi browser, dispositivo mobile o persino un altro server. L’API di distribuzione lato server è progettata appositamente per integrare [!DNL Target] con qualsiasi piattaforma lato server che effettua chiamate HTTP/HTTPS.

Puoi utilizzare l’API per integrare l’applicazione personalizzata con [!DNL Target]. Ciò è particolarmente importante per le organizzazioni che desiderano distribuire targeting a un dispositivo IoT non basato su browser, ad esempio una TV collegata, un kiosk o uno schermo digitale specializzato.

Questo parametro può restituire offerte solo per mbox normali. Puoi anche recuperare il contenuto per un solo mbox.

Questa API implementa le funzioni mbox esistenti in un sistema REST.

Questa API non elabora i cookie o le chiamate di reindirizzamento.

## API di distribuzione lato server

Link: [Server Side Batch Delivery APIs](https://developers.adobetarget.com/api/#server-side-batch-delivery)

`/rest/v2/batchmbox`

L'API di distribuzione in batch consente all'applicazione di richiedere il contenuto di più mbox in una singola chiamata. Inoltre, dispone di una modalità di precarica che consente ai client come applicazioni per dispositivi mobili, server e così via di recuperare contenuti per più mbox in una richiesta, memorizzarli nella cache locale e successivamente inviare una notifica a [!DNL Target] quando l’utente visita queste mbox.

Questo parametro può restituire offerte solo per mbox normali. Poiché è possibile recuperare contenuto per più mbox, per la prestazione, l'API di mbox consente di utilizzare il linguaggio mbox. Consente di evitare l'esecuzione di più richieste HTTP, che possono essere dispendiose.

## SDK di NodeJS

Collegamento: SDK [NodeJS](https://www.npmjs.com/package/@adobe/target-node-client)

In termini di SDK, attualmente abbiamo un solo SDK, l'SDK di NodeJS.

L'SDK di NodeJS è un sottile involucro del modulo HTTP/HTTPS principale di NodeJS. In realtà, le API di NodeJS SDK utilizzano le stesse API di distribuzione lato server.

Di seguito è riportata la mappatura:

* `MarketingCloudClient.getOffer() \*- invokes \*/res/v1/mbox endpoint`
* `MarketingCloudClient.getOffers() \*- invokes \*/res/v2/batchmbox endpoint`

## API di [!DNL Target Recommendations]

Link: [Target Recommendations APIs](https://developers.adobetarget.com/api/recommendations)

Le API di consigli consentono di interagire a livello di codice con i server di consigli di Target. Queste API possono essere integrate con una serie di applicazioni per eseguire funzioni che vengono normalmente eseguite mediante l'interfaccia utente.

## API di [!DNL Target Classic]

L’interfaccia utente e le API di [!DNL Target Classic] sono state dismesse. Per informazioni sul passaggio alle API moderne di Target, consulta [Passaggio dalle API Target obsolete ad Adobe I/O](../../c-implementing-target/c-api-and-sdk-overview/target-api-documentation.md#concept_3A31E26C8FAF49598152ACFE088BD4D2).

>[!NOTE]
>Le API di authoring (in cui si creano attività, offerte, tipi di pubblico e così via) non supportano la condivisione delle risorse tra diverse origini (Cross Origin Resource Sharing, CORS).

## Differenze tra le API di distribuzione lato server e SDK di NodeJS {#section_10336B7934F54CE98E35907A4748A4A4}

Molti clienti hanno dei dubbi a proposito delle differenze tra le API di distribuzione lato server e l'SDK di NodeJS. Ciò è particolarmente vero quando si tratta di prestazioni.

Le domande frequenti seguenti dovrebbero aiutarti a decidere quale utilizzare:

**Quando si utilizzano le API Server “pure” rispetto all'SDK di NodeJS?**

Se si utilizza NodeJS come tecnologia backend, SDK di NodeJS SDK è una scelta naturale. L'SDK gestisce molti dettagli, quali cookie, intestazioni, payload e così via. Ciò consente di concentrarsi sul nucleo dell'applicazione.

**Sono stati apportati miglioramenti a livello di prestazioni utilizzando l'SDK di NodeJS?**

Purtroppo non sono presenti numeri di prestazioni. Tuttavia, in generale, l'SDK di NodeJS dovrebbe offrire prestazioni migliori grazie all'architettura basata su eventi NodeJS. Tieni presente che la maggior parte del tempo è dedicata al backend di [!DNL Target]. L’elaborazione eseguita dall’SDK di NodeJS è molto ridotta. L’SDK è praticamente responsabile della creazione di pacchetti di una richiesta di [!DNL Target] e dell’analisi di una risposta di [!DNL Target].
