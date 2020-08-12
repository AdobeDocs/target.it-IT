---
keywords: at.js;sdk;node.js;release;updates;sdks;server side;serverside;server-side;nodejs
description: Note sulla versione relative  API lato server Adobe Target.
title: Note sulla versione relative  SDK Node.js di Adobe Target.
feature: null
topic: Standard
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 1%

---


# Note sulla versione - SDK Node.js di Target

Note sulla versione relative a [SDK](https://github.com/adobe/target-nodejs-sdk)Node.js di Adobe Target.

L’SDK Node.js di Target consente di distribuire lato [!DNL Target] server.

Questo SDK Node.js consente di integrarsi facilmente [!DNL Target] con altre [!DNL Adobe Experience Cloud] soluzioni, come il [!DNL Adobe Experience Cloud Identity Service], [!DNL Adobe Analytics]e [!DNL Adobe Audience Manager].

L’SDK Node.js introduce procedure ottimali e rimuove le complessità durante l’integrazione con [!DNL Target] tramite la nostra API di distribuzione, in modo che i team tecnici possano concentrarsi sulla logica aziendale.

Per ulteriori informazioni sull’SDK di Target Node.js, consulta  Adobe Tech Blog - [Open Sourcing, the New  Adobe Target Node.js SDK](https://medium.com/adobetech/open-sourcing-the-new-adobe-target-node-js-sdk-b6feafd828bc).

## Versione 1.0.0 (9 ottobre 2019)

Le sezioni seguenti forniscono ulteriori informazioni sulla versione 1.0.0 dell’SDK di Target Node.js:

### Aggiunto

* Supporto API v1 per Target View Delivery, incluso il recupero preventivo Page Load e View.
* Supporto completo per la distribuzione di tutti i tipi di offerte create in Visual Experience Composer (VEC).
* Supporto per la preacquisizione e le notifiche per l&#39;ottimizzazione delle prestazioni mediante la memorizzazione nella cache del contenuto prerecuperato.
* Supporto per l&#39;ottimizzazione delle prestazioni nelle [!DNL Target] integrazioni ibride tramite `serverState` quando [!DNL Target] viene distribuito sia sul lato server che sul lato client.

   Stiamo introducendo un&#39;impostazione denominata `serverState` che contiene le esperienze recuperate sul lato server, in modo che at.js v2.2+ non effettuerà una chiamata server aggiuntiva per recuperare le esperienze. Questo approccio ottimizza le prestazioni di caricamento delle pagine.

* Viene aperta in origine su GitHub come SDK [Node.js di](https://github.com/adobe/target-nodejs-sdk)Target.
* Nuovo metodo [API](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclientsendnotifications) sendNotifications() per l&#39;invio di notifiche visualizzate/su cui è stato fatto clic [!DNL Target] per il contenuto preacquisito tramite [getOffers()](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclientgetoffers).
* Creazione semplificata di richieste API View Delivery con completamento automatico del campo interno con impostazioni predefinite (ad esempio, `request.id`, `request.context`ecc.).
* Convalida degli argomenti del metodo SDK API.
* Readme, campioni e unit test aggiornati.
* Nuova configurazione del flusso CI mediante le azioni GitHub.
* Aggiunta di CoC, linee guida sui contributi, PR e modelli per edizioni

### Modificato

* Progetto rinominato in `target-nodejs-sdk`.
* Refactoring principale, sostituendo l&#39;API BatchMbox v2 di Target con l&#39;API Target View Delivery v1.
* [gli argomenti del metodo](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclientcreate) create() API sono stati modificati, rimuovendo la nidificazione ridondante (vedete la dichiarazione del metodo precedente [qui](https://www.npmjs.com/package/@adobe/target-node-client#targetnodeclientcreate)).
* [gli argomenti del metodo](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclientgetoffers) API getOffers() sono stati modificati (vedete la dichiarazione del metodo precedente [qui](https://www.npmjs.com/package/@adobe/target-node-client#targetnodeclientgetoffers)).
* Il metodo `getTargetCookieName()` API è stato sostituito con `TargetCookieName` accessor. Consultate Accessori [dell&#39;utility](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclient-utility-accessors)TargetClient.
* Il metodo `getTargetLocationHintCookieName()` API è stato sostituito con `TargetLocationHintCookieName` accessor.  Consultate Accessori [dell&#39;utility](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclient-utility-accessors)TargetClient.

### Rimosso

* Supporto API BatchMbox v2 Target.
* Il metodo [API](https://www.npmjs.com/package/@adobe/target-node-client#targetnodeclientgetoffer) getOffer() è stato rimosso. Utilizzate invece il metodo [API](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclientgetoffers) getOffers().

