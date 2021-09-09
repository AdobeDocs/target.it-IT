---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di Adobe Target.
title: Quali nuove funzioni saranno incluse nella prossima versione?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: afa370a38921ab76babf5e49edc1e4b23ee807b0
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 100%

---

# Note sulla versione di Target (prerelease)

Questo articolo contiene informazioni di pre-release. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso.

**Ultimo aggiornamento: 24 agosto 2021**

Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali, a seconda della tempistica delle versioni. I codici tra parentesi sono per uso interno di [!DNL Adobe].

>[!IMPORTANT]
>
>**Termine del ciclo di vita di mbox.js**: a partire dal 31 marzo 2021, [!DNL Adobe Target] non supporta più la libreria mbox.js. Dopo il 31 marzo 2021, tutte le chiamate effettuate da mbox.js avranno esito negativo e avranno un impatto sulle pagine che hanno attività [!DNL Target] in esecuzione, che presenteranno il contenuto predefinito.
>
>Per evitare potenziali problemi con i siti, effettua la migrazione alla versione più recente del nuovo [!DNL Adobe Experience Platform Web SDK] o della libreria JavaScript at.js. Per ulteriori informazioni, consulta [Panoramica: implementare Target per web lato client](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

## [!DNL Target Standard/Premium] 21.8.1 (10 agosto 2021)

Questa versione di manutenzione contiene molti miglioramenti al back-end, tra cui la seguente modifica visualizzata dal cliente:

* È stato risolto un problema a causa del quale i rapporti per le attività [!UICONTROL Auto Personalization] create nel [!UICONTROL Compositore esperienze basato su moduli] facevano riferimento alle offerte eliminate nei rapporti. Questo problema causava la visualizzazione di un messaggio di tipo: “Si sono verificati dei problemi nel recupero dei dati per questo rapporto. Se il problema persiste, contatta l’Assistenza clienti Adobe.” (TGT-41028)

## API di consegna di Target (3 agosto 2021)

Questo rilascio contiene i seguenti miglioramenti:

* Il limite per i parametri mbox è stato aumentato a 100 parametri. Il limite precedente era di 50 parametri. (TNT-41717)
* Il limite per `categoryId` è stato aumentato a 256 caratteri. Il limite precedente era di 128 caratteri.
* Sono stati aggiunti i seguenti dettagli di [!DNL Adobe Audience Manager] (AAM) all’API di consegna:

   * AAM UUID: ID interno di AAM utilizzato per identificare in modo univoco un utente.
   * dataPartnerId: ID per un partner dati.
   * dataPartnerUserId: ID utente fornito da un partner dati.

   In precedenza, l’API di consegna comprendeva solo `dcsLocationHint` e `blob`. (TNT-41644)

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
