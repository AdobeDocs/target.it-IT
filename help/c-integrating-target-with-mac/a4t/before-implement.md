---
description: Diverse modifiche si verificano nel processo di raccolta dei dati quando si abilita Analytics come origine della generazione di rapporti per Target (A4T).
keywords: Consigli
seo-description: Diverse modifiche si verificano nel processo di raccolta dei dati quando si abilita Analytics come origine della generazione di rapporti per Target (A4T).
seo-title: Prima dell’implementazione di Adobe Analytics come origine per la generazione di rapporti per Adobe Target (A4T)
solution: Target
title: Prima dell’implementazione
topic: Premium
uuid: fe603a4b-bd61-49f4-b1b7-a0329aa905f5
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Prima dell’implementazione{#before-you-implement}

Diverse modifiche si verificano nel processo di raccolta dei dati quando si abilita Analytics come origine della generazione di rapporti per Target (A4T).

Prima di decidere di utilizzare questa integrazione, consulta le sezioni seguenti e considera l'impatto sui processi di reporting:

## Requisiti di implementazione {#section_A0D2EF18033D4C3997B08A6EBB34C17A}

>[!IMPORTANT]
>
>Prima di iniziare a utilizzare A4T, è necessario richiedere che il tuo account sia predisposto per l’integrazione. Utilizza [questo modulo](https://www.adobe.com/go/audiences) per richiedere il provisioning.

Questa integrazione A4T richiede l’implementazione delle seguenti versioni della libreria (o più recenti), a seconda che si desideri utilizzare o meno le offerte di reindirizzamento con A4T:

### Requisiti necessari se *non* si utilizzano offerte di reindirizzamento con A4T

Questa integrazione richiede l'implementazione delle seguenti versioni della libreria (o successive) se non si prevede di utilizzare le offerte di reindirizzamento con A4T. L’ordine nell’elenco corrisponde all’ordine delle operazioni.

* Servizio ID visitatore di Experience Cloud: visitorAPI.js versione 1.8.0
* Adobe Target (a seconda dell'implementazione): at.js versione 0.9.1 o mbox.js versione 61
* Adobe Analytics: appMeasurement.js versione 1.7.0

### Requisiti necessari se si utilizzano offerte di reindirizzamento con A4T

Per utilizzare le offerte di reindirizzamento con A4T, devi implementare le seguenti versioni della libreria (o successive). L’ordine nell’elenco corrisponde all’ordine delle operazioni.

* Servizio ID visitatore di Experience Cloud: visitorAPI.js versione 2.3.0
* Adobe Target: at.js versione 1.6.2

   **Nota:** la libreria mbox.js non supporta le offerte di reindirizzamento con A4T. L’implementazione deve utilizzare at.js.

* Adobe Analytics: appMeasurement.js versione 2.1

Le istruzioni per il download e la distribuzione sono elencate in [Adobe per l'implementazione di Target](https://marketing.adobe.com/resources/help/en_US/target/a4t/c_a4timplementation.html).

## Aspetti da considerare prima dell’implementazione {#section_50D49CC52E11414089C89FB67F9B88F5}

* Questa integrazione è abilitata sulle nuove attività quando selezioni l'utilizzo di Analytics come origine di reporting. Dopo avere apportato le modifiche all'implementazione descritte in questo documento, le attività esistenti non vengono influenzate.
* Il processo di configurazione di Analytics come origine di rapporti per Target comprende diverse fasi di implementazione, seguite da una fase di previsionamento. È opportuno rivedere l'intero processo come descritto di seguito prima di procedere all'implementazione. Dopo aver completato questi passaggi, sarà possibile utilizzare Analytics, non appena attivato, come origine per i rapporti. Il processo di previsionamento può richiedere fino a cinque giorni lavorativi.
* Il servizio ID visitatore crea un ID visitatore condiviso attraverso Experience Cloud. Anche se non sostituisce l'ID mboxPC di Target o UUID di Audience Manager, sostituisce il modo in cui Analytics identifica i nuovi visitatori. Se impostato correttamente, i visitatori di ritorno di Analytics dovrebbero anche essere identificati tramite il loro vecchio ID Analytics per evitare il calo dei visitatori. Allo stesso modo, poiché il mboxPCid di Target rimane intatto, non viene perso nessun dato di profili visitatore di Target quando si aggiorna al servizio ID visitatore.
* Il servizio ID visitatore deve essere eseguito prima del codice di pagina di Analytics e Target. Assicurati che appaia `VisitorAPI.js` sopra i tag per tutti gli altri prodotti Experience Cloud.

## Latenza {#section_9489BE6FD21641A4844E591711E3F813}

Dopo l'abilitazione di questa integrazione, è possibile che si verifichi una latenza aggiuntiva di 5-10 minuti in Adobe Analytics. Questo aumento della latenza consente la memorizzazione dei dati da Analytics e Target nello stesso hit, con conseguente possibilità di suddividere i test per pagina e sezione del sito.

Questo aumento si riflette in tutti i servizi e gli strumenti di Adobe Analytics, compresi lo streaming live e il reporting in tempo reale e si applica nei seguenti scenari:

* Per lo streaming live, i rapporti in tempo reale e le richieste API e per i dati correnti per le variabili di traffico, vengono ritardati solo gli insiemi con ID di dati supplementari.
* Per i dati correnti sulle metriche di conversione, i dati finalizzati e i feed di dati, tutti gli hit sono ritardati di altri 5-7 minuti.

Tieni presente che l'aumento della latenza inizia dopo aver implementato il servizio ID visitatore di Experience Cloud, anche se questa integrazione non è stata completamente implementata.

## ID supplementare {#section_2C1F745A2B7D41FE9E30915539226E3A}

Tutte le chiamate di Target utilizzate da un'attività A4T per consegnare il contenuto o registrare la metrica di obiettivo devono avere un hit Analytics corrispondente che condivide lo stesso ID supplementare per A4T per funzionare correttamente.

Hit che contengono dati di Analytics e Target includono un ID di dati supplementare. Tale ID è visibile in [Adobe Debugger](https://marketing.adobe.com/resources/help/en_US/sc/implement/?f=debugger) come parametro `sdid`. Ad esempio: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`. Questo ID viene generato in qualsiasi momento siano presenti i seguenti criteri:

* È implementato il servizio ID visitatore
* È implementata una versione di [!DNL mbox.js] che supporta questa integrazione.

Durante la risoluzione dei problemi, assicurati di confermare che l'ID supplementare sia presente negli hit di Analytics.

## Client-side Analytics logging {#client-side}

By default, when at.js, the [!DNL Experience Cloud Visitor ID Service], and appMeasurement.js are on the page, [!DNL Adobe Analytics] and [!DNL Target] correctly stitch events for reporting and analytics purposes in the backend as long as the correct supplemental ID is included from the page, as mentioned above. Non sarà necessario gestire ed eseguire altre operazioni per A 4 T in modo corretto.

However, there are cases when you might want to have more control on when and how to send analytics data related to [!DNL Target] to [!DNL Analytics] for reporting purposes. You might have an in-house analytics tool that you leverage for internal purposes but also want to send the analytics data to [!DNL Analytics] via your in-house analytics product so that other members of your organization can continue to utilize [!DNL Analytics] as a visual reporting source. See [Step 7: Reference at.js or mbox.js on all site pages](/help/c-integrating-target-with-mac/a4t/a4timplementation.md#step7) in *Analytics for Target Implementation* for more information.
