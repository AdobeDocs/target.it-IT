---
description: Note sulla versione relative all'SDK Node.js di Adobe Target
keywords: at.js;sdk;node.js;release;updates;sdks;server side;serverside;server-side;nodejs
seo-description: Note sulla versione relative alle API lato server di Adobe Target.
seo-title: Note sulla versione relative all'SDK Node.js di Adobe Target.
solution: Target
title: Note sulla versione - SDK Node.js di destinazione
topic: Standard
translation-type: tm+mt
source-git-commit: 9fa095b910b85f244b626c34cacdf9f4a13a6929

---


# Note sulla versione - SDK Node.js di destinazione

Note sulla versione relative all'SDK Node.js di Adobe Target.

## Versione 1.0.0 (9 ottobre 2019)

Le sezioni seguenti forniscono ulteriori informazioni sulla versione 1.0.0 dell’SDK di Target Node.js:

### Aggiunto

* Supporto API v1 per Target View Delivery, incluso il recupero preventivo Page Load e View.
* Supporto completo per la distribuzione di tutti i tipi di offerte create in Visual Experience Composer (VEC).
* Supporto per preacquisizione e notifiche per l'ottimizzazione delle prestazioni mediante la memorizzazione nella cache del contenuto prerecuperato.
* Supporto per l'ottimizzazione delle prestazioni nelle [!DNL Target] integrazioni ibride tramite `serverState` quando [!DNL Target] viene distribuito sia sul lato server che sul lato client.

   Stiamo introducendo un'impostazione denominata `serverState` che contiene le esperienze recuperate sul lato server, in modo che at.js v2.2+ non effettuerà una chiamata server aggiuntiva per recuperare le esperienze. Questo approccio ottimizza le prestazioni di caricamento delle pagine.

* Viene aperta in origine su GitHub come SDK [Node.js di](https://github.com/adobe/target-nodejs-sdk)Target.
* Nuovo metodo [API](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclientsendnotifications) sendNotifications() per l'invio di notifiche visualizzate/su cui è stato fatto clic [!DNL Target] per il contenuto preacquisito tramite [getOffers()](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclientgetoffers).
* Creazione semplificata di richieste API View Delivery con completamento automatico del campo interno con impostazioni predefinite (ad esempio, `request.id`, `request.context`ecc.).
* Convalida degli argomenti del metodo SDK API.
* Readme, campioni e unit test aggiornati.
* Nuova configurazione del flusso CI mediante le azioni GitHub.
* Aggiunta di CoC, linee guida sui contributi, PR e modelli per edizioni

### Modificato

* Progetto rinominato in `target-nodejs-sdk`.
* Refactoring principale, sostituendo l'API BatchMbox v2 di Target con l'API Target View Delivery v1.
* [gli argomenti del metodo](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclientcreate) create() API sono stati modificati, rimuovendo la nidificazione ridondante (vedete la dichiarazione del metodo precedente [qui](https://www.npmjs.com/package/@adobe/target-node-client#targetnodeclientcreate)).
* [gli argomenti del metodo](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclientgetoffers) API getOffers() sono stati modificati (vedete la dichiarazione del metodo precedente [qui](https://www.npmjs.com/package/@adobe/target-node-client#targetnodeclientgetoffers)).
* Il metodo `getTargetCookieName()` API è stato sostituito con `TargetCookieName` accessor. Consultate Accessori [dell'utility](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclient-utility-accessors)TargetClient.
* Il metodo `getTargetLocationHintCookieName()` API è stato sostituito con `TargetLocationHintCookieName` accessor.  Consultate Accessori [dell'utility](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclient-utility-accessors)TargetClient.

### Rimosso

* Supporto API BatchMbox v2 Target.
* Il metodo [API](https://www.npmjs.com/package/@adobe/target-node-client#targetnodeclientgetoffer) getOffer() è stato rimosso. Utilizzate invece il metodo [API](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclientgetoffers) getOffers().

