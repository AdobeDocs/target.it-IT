---
keywords: at.js;sdk;release;updates;sdks;server side;serverside;server-side;java;java sdk
description: Note sulla versione relative  Adobe Target Java SDK.
title: Note sulla versione relative  Adobe Target Java SDK.
feature: release notes
topic: Standard
translation-type: tm+mt
source-git-commit: e203dc94e9bb34c4090f5795cbf73869808ada88
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 2%

---


# Note sulla versione - SDK Java di Target

Note sulla versione relative all’SDK [Java di](https://github.com/adobe/target-java-sdk)Target.

L’SDK [!DNL Target] Java consente di implementare il lato [!DNL Target] server. Questo SDK Java consente di integrarsi facilmente [!DNL Target] con altre [!DNL Adobe Experience Cloud] soluzioni, come il [!DNL Adobe Experience Cloud Identity Service], [!DNL Adobe Analytics]e [!DNL Adobe Audience Manager].

Java SDK introduce procedure ottimali e rimuove le complessità durante l&#39;integrazione con [!DNL Target] tramite l&#39;API di distribuzione, in modo che i team di progettazione possano concentrarsi sulla logica aziendale.

Per saperne di più sull’SDK Java di Target, consulta  Adobe Tech Blog - Ottimizzazione lato [server con la nuova SDK](https://medium.com/adobetech/server-side-optimization-with-the-new-target-java-sdk-421dc418a3f2)Java di Target.

## Versione 1.1.0 (16 dicembre 2019)

La sezione seguente fornisce ulteriori informazioni sulla versione 1.1.0 dell’SDK Java di Target:

### Aggiunto

* È stato aggiunto il supporto per la configurazione proxy a causa di un contributo open source fornito da @hisham-hassan.

## Versione 1.0.1 (11 novembre 2019)

La sezione seguente fornisce ulteriori informazioni sulla versione 1.0.1 dell&#39;SDK Java di Target:

### Fisso

* Invia un ID dati supplementare in una richiesta Target anche quando non è presente alcun cookie API del visitatore.

## Versione 1.0.0 (31 ottobre 2019)

Le sezioni seguenti forniscono ulteriori informazioni sulla versione 1.0.0 dell&#39;SDK Java di Target:

### Aggiunto

* [Supporto API](https://developers.adobetarget.com/api/delivery-api/) Target View Delivery v1, incluso il recupero preventivo Page Load e View.
   * Supporto completo per la distribuzione di tutti i tipi di offerte create in Visual Experience Composer (VEC).
* Supporto per preacquisizione e notifiche che consentono di ottimizzare le prestazioni mediante la memorizzazione nella cache del contenuto preacquisito.
* Supporto per l&#39;ottimizzazione delle prestazioni nelle [!DNL Target] integrazioni ibride tramite `serverState`, quando [!DNL Target] viene distribuito sia sul lato server che sul lato client.
   * Stiamo introducendo un&#39;impostazione denominata `serverState` che contiene le esperienze recuperate sul lato server, in modo che at.js v2.2+ non effettuerà una chiamata server aggiuntiva per recuperare le esperienze. Questo approccio ottimizza le prestazioni di caricamento delle pagine.
* Viene aperta in origine su GitHub come SDK [Java](https://github.com/adobe/target-java-sdk)Target.
* Convalida degli argomenti del metodo SDK API.
* Sono stati aggiunti README, campioni e unit test.
* Sono stati aggiunti CoC, linee guida sui contributi, PR e modelli per edizioni.

