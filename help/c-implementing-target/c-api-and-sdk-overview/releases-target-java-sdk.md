---
description: Note sulla versione relative all'SDK Java di Adobe Target
keywords: at.js;sdk;release;updates;sdk;lato server;server;lato server;java;java sdk
seo-description: Note sulla versione relative all'SDK Java di Adobe Target.
seo-title: Note sulla versione relative all'SDK Java di Adobe Target.
solution: Target
title: Note sulla versione - Java SDK di destinazione
topic: Standard
translation-type: tm+mt
source-git-commit: 540367e4c49c712df98dc132bccf4f29b4d6f095

---


# Note sulla versione - Java SDK di destinazione

Note sulla versione relative all’SDK [Java di](https://github.com/adobe/target-java-sdk)Target.

L’SDK [!DNL Target] Java consente di implementare il lato [!DNL Target] server. Questo SDK Java consente di integrarsi facilmente [!DNL Target] con altre [!DNL Adobe Experience Cloud] soluzioni, come il [!DNL Adobe Experience Cloud Identity Service], [!DNL Adobe Analytics]e [!DNL Adobe Audience Manager].

Java SDK introduce procedure ottimali e rimuove le complessità durante l'integrazione con [!DNL Target] tramite l'API di distribuzione, in modo che i team di progettazione possano concentrarsi sulla logica aziendale.

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

