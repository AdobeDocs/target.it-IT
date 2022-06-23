---
keywords: Note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: a0a20b99a76ba0346f00e3841a345e916ffde8ea
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 92%

---

# Note sulla versione di Target (corrente)

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di [!DNL Adobe Target Standard] e [!DNL Target Premium]. Sono inoltre incluse, ove applicabili, le note sulla versione di API di [!DNL Target], SDK, [!DNL Adobe Experience Platform Web SDK], at.js e altre modifiche alla piattaforma.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target Standard/Premium] 22.6.1 (versione scaglionata: (7-9 giugno 2022)

Questa versione sarà disponibile in base al seguente programma scaglionato:

* **7 giugno**: area geografica Asia Pacifico (APAC)
* **8 giugno**: area geografica delle Americhe
* **9 giugno**: area geografica Europa, Medio Oriente e Africa (EMEA)

Questa versione include i miglioramenti e le correzioni seguenti:

* È stato introdotto un miglioramento per la nuova pagina [!UICONTROL Tipi di pubblico] per evitare uno stato di mancata coerenza tra il vecchio database, in cui erano precedentemente archiviati i tipi di pubblico, e la nuova architettura, che recupera le informazioni direttamente dal back-end. (TGT-43552)
* È stato risolto un problema che impediva ad alcuni clienti di salvare i tipi di pubblico combinati a causa dell’interfaccia di Target che creava contenitori “vuoti”. (TGT-43588)

## Versione della piattaforma di destinazione (25 maggio 2022)

Questa versione include i miglioramenti e le correzioni seguenti:

* Aggiunto [Suggerimenti client agente utente](https://developer.adobe.com/target/implement/client-side/atjs/user-agent-and-client-hints/)Supporto di {target=_blank}.
* È stato risolto un problema che causava timeout in modo intermittente durante il rendering [!UICONTROL Decisioni di offerta] nelle attività di [!UICONTROL Experience Targeting] (XT). (TNT-44611)

## at.js versione 2.9.0 (27 maggio 2022)

* Aggiunto [Suggerimenti client agente utente](https://developer.adobe.com/target/implement/client-side/atjs/user-agent-and-client-hints/)Supporto di {target=_blank}.
* È stato corretto un errore per cui più richieste di mbox sulla stessa pagina avevano ID di impression diversi.

## Note aggiuntive sulla versione e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=it) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/) | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js [!DNL Adobe Target]. |

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
