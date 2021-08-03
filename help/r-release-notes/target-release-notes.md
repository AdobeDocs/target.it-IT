---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di Adobe Target.
title: Quali nuove funzioni saranno incluse nella prossima versione?
feature: Note sulla versione
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 131a938470a45144ad3ab487b6bccfa306abcaf1
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 74%

---

# Note sulla versione di Target (prerelease)

Questo articolo contiene informazioni di pre-release. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso.

**Ultimo aggiornamento: 3 agosto 2021**

Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali, a seconda della tempistica delle versioni. I codici tra parentesi sono per uso interno di [!DNL Adobe].

>[!IMPORTANT]
>
>**Termine del ciclo di vita di mbox.js**: a partire dal 31 marzo 2021, [!DNL Adobe Target] non supporta più la libreria mbox.js. Dopo il 31 marzo 2021, tutte le chiamate effettuate da mbox.js avranno esito negativo e avranno un impatto sulle pagine che hanno attività [!DNL Target] in esecuzione, che presenteranno il contenuto predefinito.
>
>Per evitare potenziali problemi con i siti, effettua la migrazione alla versione più recente del nuovo [!DNL Adobe Experience Platform Web SDK] o della libreria JavaScript at.js. Per ulteriori informazioni, consulta [Panoramica: implementare Target per web lato client](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

## API di consegna Target (data da determinare)

Questa versione contiene i seguenti miglioramenti:

* Il limite per i parametri mbox è stato aumentato a 100 parametri. Il limite precedente era di 50 parametri. (TNT-41717)
* Il limite per `categoryId` è stato aumentato a 256 caratteri. Il limite precedente era di 128 caratteri.
* I seguenti dettagli [!DNL Adobe Audience Manager] (AAM) sono stati aggiunti all’API di consegna:

   * UUID AAM (ID utente univoco Adobe Audience Manager)
   * dataPartnerId
   * dataPartnerUserId

   In precedenza, l’API di consegna comprendeva solo `dcsLocationHint` e `blob`. (TNT-41644)

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
