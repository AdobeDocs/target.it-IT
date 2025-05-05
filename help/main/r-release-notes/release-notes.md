---
keywords: note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti,aggiornamenti correnti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
short-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 0f96fb2a74a0716542308037d183847c91b1dc04
workflow-type: tm+mt
source-wordcount: '557'
ht-degree: 52%

---

# Note sulla versione (corrente) di [!DNL Target]

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di [!DNL Adobe Target Standard] e [!DNL Target Premium]. Sono inoltre incluse, ove applicabili, le note sulla versione di API di [!DNL Target], SDK, [!DNL Adobe Experience Platform Web SDK], at.js e altre modifiche alla piattaforma.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target Standard/Premium] 25.5.1 (5 maggio 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema che impediva la visualizzazione di perfezionamenti del pubblico per alcune attività nell’interfaccia utente aggiornata. (TGT-52057)
* È stato risolto un problema che impediva l’utilizzo di tipi di pubblico combinati nelle attività di. (TGT-52346)
* È stato risolto un problema che impediva la creazione di una nuova attività in un’area di lavoro non predefinita utilizzando un pubblico per sola attività dalla stessa area di lavoro. (TGE-52349)
* È stato risolto un problema che causava la scomparsa dei tipi di pubblico per sola attività dall’interfaccia utente aggiornata dopo la creazione e la selezione di un nuovo pubblico. (TGT=52091)
* È stato risolto un problema che impediva l’utilizzo di tipi di pubblico duplicati nelle attività di. (TGT-51200 e TGT-52057)
* È stato risolto un problema che causava l’inversione dei perfezionamenti del pubblico e dei tipi di pubblico dell’attività nell’interfaccia utente aggiornata. (TGT-52158)
* È stato risolto un problema che impediva la creazione di una nuova attività a causa dell’errore di inserimento dell’utente: &quot;area di lavoro non predefinita non consentita per questo utente&quot;. (TGT-52267)
* È stato risolto un problema che impediva la visualizzazione delle offerte nell’interfaccia utente aggiornata per le aree di lavoro predefinite e non predefinite. [!DNL Target] ora visualizza le offerte da entrambe le aree di lavoro. (TGT-52339)
* È stato risolto un problema a causa del quale [!DNL Target] non avvisava i clienti quando modificava un&#39;attività e modificava un elemento del sito Web modificato. (TGT-52100)
* È stato risolto un problema a causa del quale la modifica di un’offerta con offerte ad hoc creava una nuova offerta invece di aggiornare quella esistente. (TGT-52135)
* È stato risolto un problema che causava un errore di payload non valido durante lo spostamento delle offerte nelle cartelle. (TGT-52325)
* È stato risolto un problema che causava un errore di inserimento dell’utente durante lo spostamento delle offerte nelle cartelle. (TGT-52296)
* È stato aggiunto un campo `audienceMetadata` per ogni attività, per assicurarti che venga letto e aggiornato durante la modifica dell&#39;attività. (TGT-51004)

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
