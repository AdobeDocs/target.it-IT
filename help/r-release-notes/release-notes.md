---
keywords: Note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di [!DNL Adobe Target].
title: Quali nuove funzioni sono incluse nella versione corrente?
feature: Note sulla versione
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 95fdb1dcee873f7a414a3aecdc363fca2b621c01
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 61%

---

# Note sulla versione di Target (corrente)

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di [!DNL Adobe Target Standard] e [!DNL Target Premium]. Inoltre, se applicabile, sono incluse anche le note sulla versione per API, SDK di Target, [!DNL Adobe Experience Platform Web SDK], at.js e altre modifiche alla piattaforma.

>[!IMPORTANT]
>
>**Terminazione di mbox.js**: a partire dal 31 marzo 2021, [!DNL Adobe Target] non supporta più la libreria mbox.js. Dopo il 31 marzo 2021, tutte le chiamate effettuate da mbox.js avranno esito negativo e le pagine che hanno attività [!DNL Target] in esecuzione, si troveranno a utilizzare il contenuto predefinito.
>
>Per evitare potenziali problemi con i siti, passa alla versione più recente del nuovo [!DNL Adobe Experience Platform Web SDK] o della libreria JavaScript at.js. Per ulteriori informazioni, consulta [Panoramica: implementare Target per web lato client](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

(I codici tra parentesi sono per uso interno di [!DNL Adobe].)

## at.js 2.6.1 (16 agosto 2021)

* Correzione di bug per &quot;Nessun artefatto memorizzato nella cache disponibile per la modalità ibrida&quot; quando si utilizzano le decisioni sul dispositivo.

## [!DNL Target] node.js SDK 2.2.0 (11 agosto 2021)

* Aggiunta raccolta dati di telemetria SDK
* Codice openapi del client API di consegna automatica

Per ulteriori informazioni su questa versione e sulle versioni precedenti, consulta il [Change log](https://github.com/adobe/target-nodejs-sdk/blob/main/CHANGELOG.md) nella [documentazione SDK di Target node.js](https://github.com/adobe/target-nodejs-sdk) su Github.

## [!DNL Target Standard/Premium] 21.8.1 (10 agosto 2021)

Questa versione di manutenzione contiene molti miglioramenti back-end, tra cui la seguente modifica rivolta al cliente:

* È stato risolto un problema a causa del quale i rapporti per le attività [!UICONTROL Personalizzazione automatica] create nel [!UICONTROL Compositore esperienza basato su moduli] facevano riferimento alle offerte eliminate nei rapporti. Questo problema causava la visualizzazione del seguente messaggio di errore: &quot;Si sono verificati problemi durante il recupero dei dati per questo report. Contatta l’Assistenza clienti Adobe se il problema persiste.&quot; (TGT-41028)

## [!DNL Target Delivery API] (3 agosto 2021)

Questa versione contiene i seguenti miglioramenti:

* Il limite per i parametri mbox è stato aumentato a 100 parametri. Il limite precedente era di 50 parametri. (TNT-41717)
* Il limite per `categoryId` è stato aumentato a 256 caratteri. Il limite precedente era di 128 caratteri.
* I seguenti dettagli [!DNL Adobe Audience Manager] (AAM) sono stati aggiunti all’API di consegna:

   * UUID AAM: ID AAM interno utilizzato per identificare in modo univoco un utente.
   * dataPartnerId: ID per un partner dati.
   * dataPartnerUserId: ID utente fornito da un partner dati.

   In precedenza, l’API di consegna comprendeva solo `dcsLocationHint` e `blob`. (TNT-41644)

## at.js 2.6.0 (27 luglio 2021)

* Ai cookie è stato aggiunto un attributo sicuro ogni volta che le impostazioni at.js `secureOnly` sono impostate su `true`.
* Ora quando si utilizza `triggerView()` sono disponibili i token di risposta.
* È stato risolto un problema relativo all’evento `CONTENT_RENDERING_NO_OFFERS`. Ora questo evento viene attivato correttamente ogni volta che non viene restituito alcun contenuto da [!DNL Target].
* I dettagli delle metriche di clic di [!DNL Analytics for Target] (A4T) vengono restituiti correttamente quando si utilizzano le richieste `prefetch`.
* La generazione di UUID non utilizza più `Math.random()`, ma si basa su `window.crypto`.
* La scadenza dei cookie `sessionId` viene estesa correttamente a ogni chiamata di rete.
* L’inizializzazione della cache di visualizzazione [!UICONTROL Applicazione a pagina singola] viene ora gestita correttamente e rispetta le impostazioni `viewsEnable`.

## Note aggiuntive sulla versione e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en) | Dettagli sulle modifiche apportate a ogni versione dell’SDK per web di Platform. |
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
