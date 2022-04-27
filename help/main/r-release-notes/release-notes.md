---
keywords: Note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di [!DNL Adobe Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 25dac5f4712fec80323df9b0e00feb9750f5b155
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 56%

---

# Note sulla versione di Target (corrente)

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di [!DNL Adobe Target Standard] e [!DNL Target Premium]. Inoltre, le note sulla versione di [!DNL Target] API, SDK, [!DNL Adobe Experience Platform Web SDK], at.js e altre modifiche alla piattaforma sono inclusi, se applicabile.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target] versione di platform (27 aprile 2022)

Questa versione contiene le seguenti modifiche:

* Con questa versione puoi preacquisire il contenuto per [!UICONTROL Personalizzazione automatica] (AP) e [!UICONTROL Targeting automatico] (AT) attività (in precedenza non restituite da [!DNL Target]). Questo potrebbe modificare le esperienze visualizzate dagli utenti finali in caso di una chiamata di preacquisizione (nessuna modifica al flusso di esecuzione) se un’attività di AP/AT si trova nel percorso di consegna ed è più alta in priorità rispetto ad altre attività AB/XT che utilizzano la stessa posizione per la consegna dei contenuti.

## Versione di Target Platform (13 aprile 2022)

Questa versione contiene il seguente aggiornamento:

* È stato risolto un problema per garantire che l’ultimo ottetto degli indirizzi IP sia correttamente offuscato quando acquisito utilizzando gli script di profilo. (TNT-44076)

## [!DNL Target Standard/Premium] 22.3.1 (5 aprile 2022)

Questa versione contiene le seguenti modifiche e miglioramenti:

* È stato risolto un problema che causava il [!UICONTROL Includi] e [!UICONTROL Escludi] opzioni da disattivare per i tipi di pubblico combinati durante la modifica di un’attività. (TGT-43422)
* È stato risolto un problema che impediva ad alcuni clienti di visualizzare l’elenco dei tipi di pubblico disponibili durante la modifica di un’attività. (TGT-43404)
* È stato risolto un problema che impediva ad alcuni clienti di eliminare un indirizzo IP da &quot;[!UICONTROL IP da escludere [!DNL Target] dati di reporting]&quot; [!UICONTROL Amministrazione] > [!UICONTROL Reporting]. (TGT-43384)
* È stato risolto un problema che impediva l’uso di numeri negativi nel criterio del pubblico che verificava se una variabile fosse &quot;maggiore di&quot;, &quot;maggiore o uguale a&quot;, &quot;minore di&quot; o &quot;minore o uguale a&quot;. (TGT-43367)
* È stato risolto un problema che impediva ai clienti di visualizzare il [!UICONTROL Dettagli del pubblico] durante la creazione di tipi di pubblico combinati. (TGT-43303)

## Note aggiuntive sulla versione e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=it) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js [!DNL Adobe Target]. |

## Modifiche alla documentazione, precedenti note sulla versione e note sulla versione di Experience Cloud

Per informazioni aggiuntive, oltre alle note di ciascuna versione, consulta le seguenti risorse:

| Risorsa | Dettagli |
|--- |--- |
| Modifiche alla documentazione | Consulta le informazioni dettagliate sugli aggiornamenti di questa guida che non sono inclusi nelle presenti note sulla versione.<br>Per ulteriori informazioni, consulta [Modifiche alla documentazione](/help/main/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Note sulla versione per le versioni precedenti | Informazioni su nuove funzionalità e miglioramenti introdotti nelle versioni precedenti di Target Standard e Target Premium.<br>Per ulteriori informazioni, consulta [Note sulla versione per le versioni precedenti](/help/main/r-release-notes/release-notes-for-previous-releases.md). |
| Note sulla versione di Adobe Experience Cloud | Ultime note sulla versione per le soluzioni Adobe Experience Cloud.<br>Per ulteriori informazioni, consulta [Note sulla versione di Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=it). |

## Informazioni in anteprima {#section_5D588F0415A2435B851A4D0113ACA3A0}

Le risorse seguenti contengono informazioni sulle funzionalità in arrivo con la prossima versione di Target.

| Risorsa | Dettagli |
|--- |--- |
| Adobe Priority Product Update | Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) |
| Note sulle prossime versioni | Per informazioni sulle versioni di Target del mese corrente, incluse le informazioni prerelease, consulta la pagina [Note sulla versione di Target (prerelease)](/help/main/r-release-notes/target-release-notes.md). |
