---
description: Informazioni sulle API di distribuzione sul lato server di Target, sulle API di consigli e su SDK di NodeJS.
keywords: lato server;api;sdk;nodejs;node js;api Recommendations
seo-description: Informazioni sulle API di consegna lato server di Adobe Target, sulle API di Recommendations e sull'SDK nodejs.
seo-title: Implementazione lato server di Adobe Target
solution: Target
title: 'Lato server: implementare Target'
topic: 'Consigli '
uuid: 21d321c7-3da4-44a2-a04f-1807cc2a893b
translation-type: tm+mt
source-git-commit: 385864d9daae19468c4557e51043d5b788924658

---


# Lato server: implementare Target{#server-side-implement-target}

Informazioni sulle [!DNL Adobe Target] API di consegna lato server, API lato server server, API nodejs SDK, [!DNL Target Recommendations] API e [!DNL Target Classic] API (disabilitata).

Il processo seguente si verifica in un&#39;implementazione lato server di [!DNL Target]:

1. Un dispositivo client richiede una richiesta di un&#39;esperienza attraverso il server.
1. Il server invia la richiesta a [!DNL Target].
1. [!DNL Target] reindirizza la risposta al server.
1. Il server decide quale esperienza distribuire al dispositivo client per il rendering.

L&#39;esperienza non deve essere visualizzata in un browser; può essere visualizzato in un&#39;e-mail o in un messaggio, tramite un assistente vocale o tramite altre esperienze non visive o non basate su browser. Poiché il server si unisce al client, [!DNL Target]questo tipo di implementazione è ideale anche se avete bisogno di maggiore controllo e sicurezza o di disporre di processi di back-end complessi che desiderate eseguire sul vostro server.

La sezione seguente elenca le varie API e l’SDK di NodeJS e fornisce ulteriori informazioni:

## API di distribuzione lato server

Collegamento: [API lato server API](https://developers.adobetarget.com/api/#server-side-delivery)

`/rest/v1/mbox`

[!DNL Target] consente all&#39;applicazione di effettuare chiamate mbox da qualsiasi browser, dispositivo mobile o persino un altro server. L&#39;API di consegna lato server è progettata specificatamente per l&#39;integrazione [!DNL Target] con qualsiasi piattaforma lato server che effettua chiamate HTTP/HTTPS.

Puoi utilizzare l&#39;API per integrare l&#39;applicazione personalizzata con [!DNL Target]. Ciò è particolarmente importante per le organizzazioni che desiderano distribuire targeting a un dispositivo IoT non basato su browser, ad esempio una TV collegata, un kiosk o uno schermo digitale specializzato.

Questo parametro può restituire offerte solo per mbox normali. Puoi anche recuperare il contenuto per un solo mbox.

Questa API implementa le funzioni mbox esistenti in un sistema REST.

Questa API non elabora i cookie o le chiamate di reindirizzamento.

## API di distribuzione lato server

Collegamento: [API Consegna batch lato server](https://developers.adobetarget.com/api/#server-side-batch-delivery)

`/rest/v2/batchmbox`

L&#39;API di distribuzione in batch consente all&#39;applicazione di richiedere il contenuto di più mbox in una singola chiamata. Dispone anche di una modalità di preacquisizione che consente a client come app mobili, server e così via di recuperare il contenuto per più mbox in una richiesta, nella cache locale e in un secondo momento notifica [!DNL Target] quando l&#39;utente accede a tali mbox.

Questo parametro può restituire offerte solo per mbox normali. Poiché è possibile recuperare contenuto per più mbox, per la prestazione, l&#39;API di mbox consente di utilizzare il linguaggio mbox. Consente di evitare l&#39;esecuzione di più richieste HTTP, che possono essere dispendiose.

## SDK di NodeJS

Collegamento: [Nodejs SDK](https://www.npmjs.com/package/@adobe/target-node-client)

In termini di SDK, attualmente abbiamo un solo SDK, l&#39;SDK di NodeJS.

L&#39;SDK di NodeJS è un sottile involucro del modulo HTTP/HTTPS principale di NodeJS. In realtà, le API di NodeJS SDK utilizzano le stesse API di distribuzione lato server.

Di seguito è riportata la mappatura:

* `MarketingCloudClient.getOffer() \*- invokes \*/res/v1/mbox endpoint`
* `MarketingCloudClient.getOffers() \*- invokes \*/res/v2/batchmbox endpoint`

## [!DNL Target Recommendations] API

Collegamento: [API di Target Recommendations](https://developers.adobetarget.com/api/recommendations)

Le API di consigli consentono di interagire a livello di codice con i server di consigli di Target. Queste API possono essere integrate con una serie di applicazioni per eseguire funzioni che vengono normalmente eseguite mediante l&#39;interfaccia utente.

## [!DNL Target Classic] API

[!DNL Target Classic] L&#39;interfaccia utente e le API sono state disattivate. Per informazioni sul passaggio alle API moderne di Target, consulta [Passaggio dalle API Target obsolete ad Adobe I/O](../../c-implementing-target/c-api-and-sdk-overview/target-api-documentation.md#concept_3A31E26C8FAF49598152ACFE088BD4D2).

>[!NOTE]
>Le API di authoring (in cui si creano attività, offerte, tipi di pubblico e così via) non supportano la condivisione delle risorse tra diverse origini (Cross Origin Resource Sharing, CORS).

## Differenze tra le API di distribuzione lato server e SDK di NodeJS {#section_10336B7934F54CE98E35907A4748A4A4}

Molti clienti hanno dei dubbi a proposito delle differenze tra le API di distribuzione lato server e l&#39;SDK di NodeJS. Ciò è particolarmente vero quando si tratta di prestazioni.

Le domande frequenti seguenti dovrebbero aiutarti a decidere quale utilizzare:

**Quando si utilizzano le API Server “pure” rispetto all&#39;SDK di NodeJS?**

Se si utilizza NodeJS come tecnologia backend, SDK di NodeJS SDK è una scelta naturale. L&#39;SDK gestisce molti dettagli, quali cookie, intestazioni, payload e così via. Ciò consente di concentrarsi sul nucleo dell&#39;applicazione.

**Sono stati apportati miglioramenti a livello di prestazioni utilizzando l&#39;SDK di NodeJS?**

Purtroppo non sono presenti numeri di prestazioni. Tuttavia, in generale, l&#39;SDK di NodeJS dovrebbe offrire prestazioni migliori grazie all&#39;architettura basata su eventi NodeJS. Tenete presente che la maggior parte del tempo viene passato sul [!DNL Target] backend. L&#39;SDK di NodeJS è molto ridotto. L&#39;SDK è sostanzialmente responsabile del package di una [!DNL Target] richiesta e dell&#39;analisi di una [!DNL Target] risposta.
