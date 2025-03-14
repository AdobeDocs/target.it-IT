---
keywords: note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti,aggiornamenti correnti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
short-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: cd335504f5354aa9052ae7e958cf803cd90a9ae9
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 39%

---

# Note sulla versione (corrente) di [!DNL Target]

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di [!DNL Adobe Target Standard] e [!DNL Target Premium]. Sono inoltre incluse, ove applicabili, le note sulla versione di API di [!DNL Target], SDK, [!DNL Adobe Experience Platform Web SDK], at.js e altre modifiche alla piattaforma.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target Standard/Premium] 25.3.6 (14 marzo 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto l&#39;errore &quot;Input utente non valido&quot; nelle attività [!UICONTROL Visual Experience Composer] (VEC) con [!UICONTROL Click Tracking] abilitato quando lo stesso selettore [!UICONTROL ClickTrack] viene utilizzato più volte. (TGT-51921)
* È stato corretto l’errore &quot;Input utente non valido&quot; nelle attività del Compositore esperienza visivo con posizioni condivise (ad esempio, selettore HEAD) e offerte identiche. (TGT-51879)
* È stato risolto un problema che causava la condivisione delle modifiche dell’esperienza tra i vari tipi di pubblico. (TGT-51815)
* Sono stati risolti degli errori di convalida durante la creazione di attività a causa di conflitti di ID segmento. Gli errori si sono verificati quando [!DNL Target] ha rilevato attività esistenti utilizzando segmenti anonimi. (TGT-51784)
* È stato risolto un problema che impediva a [!DNL Target] di salvare attività con regole di esclusione in un pubblico. (TGT-51581)
* È stato risolto un problema che impediva ai clienti di creare, eliminare o spostare cartelle senza accedere all’area di lavoro predefinita. (TGT-51499)
* È stato risolto un problema che causava un errore nelle richieste di GET durante il recupero dell&#39;elenco delle metriche [!DNL Analytics]. (TGT-51106)

## [!DNL Target Standard/Premium] 25.3.5 (11 marzo 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema che impediva agli utenti di modificare le offerte nel pannello [!UICONTROL Modifications]. (TGT-51800)
* È stato risolto un problema che impediva la corretta visualizzazione delle azioni nel pannello sinistro per esperienze e tipi di pubblico, incluso in modalità [!UICONTROL ClickTrack]. (TGT-51895)
* È stato risolto un problema a causa del quale i selettori [!UICONTROL ClickTrack] non venivano applicati alla pagina corretta del pubblico. (TGT-51871)

## [!DNL Target Standard/Premium] 25.3.4 (7 marzo 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema che impediva la modifica o il riutilizzo dei tipi di pubblico per sola attività nel pannello [!UICONTROL Audiences]. (TGT-51860)
* È stato risolto un problema che impediva ai clienti [!DNL Target Standard] di creare attività utilizzando reporting di [!UICONTROL Analytics for Target] (A4T). (TGT-51854)
* È stato risolto un problema che escludeva i contatori degli ID locali dal payload durante le operazioni di creazione e modifica in batch. (TGT-51867)

## [!DNL Target Standard/Premium] 25.3.2 (6 marzo 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema che impediva la creazione di una nuova attività in seguito alla copia di un’attività con un pubblico per sola attività, utilizzando erroneamente il pubblico dell’attività originale. (TGT-51855)
* È stato risolto un problema che impediva la modifica delle attività [!UICONTROL Experience Targeting] (XT) con tipi di pubblico per sola attività. (TGT-51846)
* È stato risolto un problema che impediva al Compositore esperienza visivo di applicare correttamente le modifiche a un&#39;esperienza alla prima modifica. [!UICONTROL Visual Experience Composer] (TGT-51843)
* È stato risolto un problema che attivava un errore &quot;ID&quot; quando si faceva clic su alcuni elementi all’interno del Compositore esperienza visivo. (TGT-51814)
* È stata aggiornata la gestione degli errori nel Compositore esperienza visivo durante la creazione dell’attività. (TGT-51759)
* È stato risolto un problema che causava un errore di &quot;input utente non valido&quot; durante il salvataggio dell&#39;attività a causa di una visualizzazione mancante nel pannello [!UICONTROL Modifications]. (TGT-51827)
* È stato risolto un problema che impediva la creazione di criteri per i consigli. (TGT-51834)
* È stato aggiunto un messaggio di conferma prima del reindirizzamento a un URL diverso. (TGT-51703)
* Sono stati risolti dei problemi relativi ai test di integrazione di GraphQL in offerte e cartelle. (TGT-51839)

## [!DNL Target Standard/Premium] 25.3.1 (3 marzo 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* Un pubblico combinato può includere sottogruppi, ciascuno contenente più tipi di pubblico. Questa versione ha risolto un problema che impediva la visualizzazione dei tipi di pubblico dei sottogruppi nella finestra di dialogo [!UICONTROL Rules]. (TGT-51813)
* È stato risolto un problema che causava la sostituzione di alcuni tipi di pubblico di esperienza con [!UICONTROL All Visitors] durante l&#39;apertura di attività precedenti. (TGT-51812)
* È stato risolto un problema che impediva la modifica di attività con tipi di pubblico per sola attività. (TGT-51807)
* È stato risolto un problema che impediva la modifica delle modifiche dell&#39;intestazione della pagina nell&#39;interfaccia utente [!DNL Target] aggiornata. (TGT-51797)
* È stato risolto un errore Null che si verificava durante la duplicazione di un’esperienza, l’eliminazione di un’altra esperienza e il tentativo di salvare l’attività. (TGT-51796)
* È stato risolto un problema che impediva la visualizzazione delle regole di esclusione del pubblico nel pannello informazioni del pubblico durante il passaggio [!UICONTROL Targeting] della creazione delle attività. (TGT-51579)
* Aggiornati messaggi di errore localizzati in coreano. (TGT-51701 e TGT-51699)

## Note aggiuntive e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=it) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js [!DNL Adobe Target]. |

## Modifiche alla documentazione, precedenti note sulla versione e note sulla versione di Experience Cloud

Per informazioni aggiuntive, oltre alle note di ciascuna versione, consulta le seguenti risorse:

| Risorsa | Dettagli |
|--- |--- |
| [Modifiche alla documentazione](/help/main/r-release-notes/doc-change.md) | Consulta le informazioni dettagliate sugli aggiornamenti di questa guida che non sono inclusi nelle presenti note sulla versione. |
| [Note sulla versione per le versioni precedenti](/help/main/r-release-notes/release-notes-for-previous-releases.md). | Informazioni su nuove funzionalità e miglioramenti introdotti nelle versioni precedenti di Target Standard e Target Premium. |
| [Note sulla versione di Adobe Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=it){target=_blank} | Ultime note sulla versione per le soluzioni Adobe Experience Cloud. |

## Informazioni in anteprima {#section_5D588F0415A2435B851A4D0113ACA3A0}

Le risorse seguenti contengono informazioni sulle funzionalità in arrivo con la prossima versione di Target.

| Risorsa | Dettagli |
|--- |--- |
| [Adobe Priority Product Update](https://www.adobe.com/subscription/priority-product-update.html){target=_blank} | Notifiche anticipate sui miglioramenti dei prodotti in arrivo per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud]. |
| [Note sulla versione di Target: prerelease](/help/main/r-release-notes/target-release-notes.md){target=_blank} | Informazioni sulle versioni di Target del mese corrente, incluse le informazioni prerelease. |
