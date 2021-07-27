---
keywords: Note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
title: Quali nuove funzioni sono incluse nella versione corrente?
feature: Note sulla versione
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 21c7675085bf5dc06bf9b1b38a82b2be4d4b0f76
workflow-type: tm+mt
source-wordcount: '653'
ht-degree: 100%

---

# Note sulla versione di Target (corrente)

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di [!DNL Adobe Target Standard] e [!DNL Target Premium]. Sono inoltre incluse, ove applicabili, le note sulla versione per API di Target, SDK, libreria JavaScript (at.js) e altre modifiche alla piattaforma.

>[!IMPORTANT]
>
>**Terminazione di mbox.js**: a partire dal 31 marzo 2021, [!DNL Adobe Target] non supporta più la libreria mbox.js. Dopo il 31 marzo 2021, tutte le chiamate effettuate da mbox.js avranno esito negativo e le pagine che hanno attività [!DNL Target] in esecuzione, si troveranno a utilizzare il contenuto predefinito.
>
>Per evitare potenziali problemi con i siti, passa alla versione più recente del nuovo [!DNL Adobe Experience Platform Web SDK] o della libreria JavaScript at.js. Per ulteriori informazioni, consulta [Panoramica: implementare Target per web lato client](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

(I codici tra parentesi sono per uso interno di [!DNL Adobe].)

## at.js 2.6.0 (16 luglio 2021)

* Ai cookie è stato aggiunto un attributo sicuro ogni volta che le impostazioni at.js `secureOnly` sono impostate su `true`.
* Ora quando si utilizza `triggerView()` sono disponibili i token di risposta.
* È stato risolto un problema relativo all’evento `CONTENT_RENDERING_NO_OFFERS`. Ora questo evento viene attivato correttamente ogni volta che non viene restituito alcun contenuto da [!DNL Target].
* I dettagli delle metriche di clic di [!DNL Anlytics for Target] (A4T) vengono restituiti correttamente quando si utilizzano le richieste `prefetch`.
* La generazione di UUID non utilizza più `Math.random()`, ma si basa su `window.crypto`.
* La scadenza dei cookie `sessionId` viene estesa correttamente a ogni chiamata di rete.
* L’inizializzazione della cache di visualizzazione [!UICONTROL Applicazione a pagina singola] viene ora gestita correttamente e rispetta le impostazioni `viewsEnable`.

## [!DNL Target Standard/Premium] 21.6.1 (30 giugno 2021)

Questa versione contiene le nuove funzioni e i miglioramenti seguenti. I codici tra parentesi sono per uso interno di [!DNL Adobe].

| Funzione | Dettagli |
| --- | --- |
| [!UICONTROL Analytics for Target] (A4T) | Facendo clic sul collegamento “[!UICONTROL Visualizza in Analytics]” sulla pagina [!UICONTROL Rapporti] da un’attività che utilizza [!DNL Analytics] come origine per la generazione di rapporti (A4T), ora viene aperto [!DNL Analysis Workspace]. In precedenza, il collegamento apriva la funzione di generazione rapporti di [!DNL Analytics]. (TGT-36959) |

## Python SDK 1.0.0 (16 giugno 2021)

È ora disponibile il nuovo SDK Python [!DNL Adobe Target] con funzionalità di decisioning sul dispositivo. Questa nuova aggiunta rafforza la suite di SDK lato server per [!DNL Target]. Questi SDK facilitano l’integrazione con [!DNL Target] e velocizzano il time to value, nel linguaggio che preferisci. Le integrazioni lato server stanno diventando una scelta popolare dato che il mercato si sta spostando verso un mondo senza cookie in cui i dati di prime parti sono preziosi. Gli SDK di Target sono disponibili nei linguaggi di programmazione più diffusi sul mercato (Python, Java, JavaScript, C# / .Net).

Per ulteriori informazioni, consulta la [documentazione di Python SDK](https://adobetarget-sdks.gitbook.io/docs/sdk-reference-guides/python-sdk) nella [guida degli SDK di Adobe Target](https://adobetarget-sdks.gitbook.io/docs/).

## ![Badge Adobe Experience Platform Web SDK](/help/assets/platform.png) [!DNL Adobe Experience Platform Web SDK] versione 2.5.0 (1° giugno 2021)

Questa versione di [!DNL Platform Web SDK] include il supporto per i seguenti elementi:

| Funzione | Dettagli |
| --- | --- |
| Supporto dei reindirizzamenti con [!UICONTROL Analytics for Target] (A4T) | Platform Web SDK ora supporta i [!DNL Target]reindirizzamenti quando si utilizza [A4T](/help/c-integrating-target-with-mac/a4t/a4t.md).<br>Per ulteriori informazioni, consulta [Analytics per l’implementazione di  [!DNL Target] ](/help/c-integrating-target-with-mac/a4t/a4timplementation.md). |

## Note aggiuntive sulla versione e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Dettagli sulle versioni di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js [!DNL Adobe Target]. |

## Modifiche alla documentazione, precedenti note sulla versione e note sulla versione di Experience Cloud

Per informazioni aggiuntive, oltre alle note di ciascuna versione, consulta le seguenti risorse:

| Risorsa | Dettagli |
|--- |--- |
| Modifiche alla documentazione | Consulta le informazioni dettagliate sugli aggiornamenti di questa guida che non sono inclusi nelle presenti note sulla versione.<br>Per ulteriori informazioni, consulta [Modifiche alla documentazione](/help/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Note sulla versione per le versioni precedenti | Informazioni su nuove funzionalità e miglioramenti introdotti nelle versioni precedenti di Target Standard e Target Premium.<br>Per ulteriori informazioni, consulta [Note sulla versione per le versioni precedenti](/help/r-release-notes/release-notes-for-previous-releases.md). |
| Note sulla versione di Adobe Experience Cloud | Ultime note sulla versione per le soluzioni Adobe Experience Cloud.<br>Per ulteriori informazioni, consulta [Note sulla versione di Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=it). |

## Informazioni in anteprima {#section_5D588F0415A2435B851A4D0113ACA3A0}

Le risorse seguenti contengono informazioni sulle funzionalità in arrivo con la prossima versione di Target.

| Risorsa | Dettagli |
|--- |--- |
| Adobe Priority Product Update | Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) |
| Note sulle prossime versioni | Per informazioni sulle versioni di Target del mese corrente, incluse le informazioni prerelease, consulta la pagina [Note sulla versione di Target (prerelease)](/help/r-release-notes/target-release-notes.md). |
