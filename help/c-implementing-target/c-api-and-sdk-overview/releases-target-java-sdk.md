---
keywords: at.js;sdk;release;updates;sdk;lato server;server;lato server;java;java sdk
description: Note sulla versione relative all'SDK Java di Adobe Target.
title: Note sulla versione relative all'SDK Java di Adobe Target.
topic: Standard
translation-type: tm+mt
source-git-commit: af0434a14bf9a816366941b9e2108fb8ba7c9d24

---


# Note sulla versione - Java SDK di destinazione

Note sulla versione relative all’SDK [Java di](https://github.com/adobe/target-java-sdk)Target.

L’SDK [!DNL Target] Java consente di implementare il lato [!DNL Target] server. Questo SDK Java consente di integrarsi facilmente [!DNL Target] con altre [!DNL Adobe Experience Cloud] soluzioni, come il [!DNL Adobe Experience Cloud Identity Service], [!DNL Adobe Analytics]e [!DNL Adobe Audience Manager].

Java SDK introduce procedure ottimali e rimuove le complessità durante l'integrazione con [!DNL Target] tramite l'API di distribuzione, in modo che i team di progettazione possano concentrarsi sulla logica aziendale.

Per ulteriori informazioni su Target Java SDK, consulta Adobe Tech Blog - Ottimizzazione lato [server con la nuova SDK](https://medium.com/adobetech/server-side-optimization-with-the-new-target-java-sdk-421dc418a3f2)Java di Target.

## Versione 1.0.1 (11 novembre 2019)

La sezione seguente fornisce ulteriori informazioni sulla versione 1.0.1 dell'SDK Java di Target:

### Fisso

* Invia un ID dati supplementare in una richiesta Target anche quando non è presente alcun cookie API del visitatore.

## Versione 1.0.0 (31 ottobre 2019)

Le sezioni seguenti forniscono ulteriori informazioni sulla versione 1.0.0 dell'SDK Java di Target:

### Aggiunto

* [Supporto API](https://developers.adobetarget.com/api/delivery-api/) Target View Delivery v1, incluso il recupero preventivo Page Load e View.
   * Supporto completo per la distribuzione di tutti i tipi di offerte create in Visual Experience Composer (VEC).
* Supporto per preacquisizione e notifiche che consentono di ottimizzare le prestazioni mediante la memorizzazione nella cache del contenuto preacquisito.
* Supporto per l'ottimizzazione delle prestazioni nelle [!DNL Target] integrazioni ibride tramite `serverState`, quando [!DNL Target] viene distribuito sia sul lato server che sul lato client.
   * Stiamo introducendo un'impostazione denominata `serverState` che contiene le esperienze recuperate sul lato server, in modo che at.js v2.2+ non effettuerà una chiamata server aggiuntiva per recuperare le esperienze. Questo approccio ottimizza le prestazioni di caricamento delle pagine.
* Viene aperta in origine su GitHub come SDK [Java](https://github.com/adobe/target-java-sdk)Target.
* Convalida degli argomenti del metodo SDK API.
* Sono stati aggiunti README, campioni e unit test.
* Sono stati aggiunti CoC, linee guida sui contributi, PR e modelli per edizioni.

