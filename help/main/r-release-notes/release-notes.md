---
keywords: note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramento;miglioramenti;correzioni;correzioni di bug;aggiornamenti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
short-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 8da8daf7da0cfe3e4936cb48b4c594c464708775
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 66%

---

# Note sulla versione (corrente) di [!DNL Target]

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di [!DNL Adobe Target Standard] e [!DNL Target Premium]. Sono inoltre incluse, ove applicabili, le note sulla versione di API di [!DNL Target], SDK, [!DNL Adobe Experience Platform Web SDK], at.js e altre modifiche alla piattaforma.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target] Standard/Premium 23.9.1 (6-11 settembre 2023)

Questa versione sarà disponibile in base al seguente programma scaglionato:

* **6 settembre**: area geografica delle Americhe
* **7 settembre**: area geografica Europa, Medio Oriente e Africa (EMEA)
* **11 settembre**: area geografica Asia-Pacifico (APAC)

Questa versione include i miglioramenti e le correzioni seguenti:

* È stato risolto un problema che causava incoerenza nei dati di reporting in. [!DNL Target] Interfaccia e [!DNL Adobe Analytics] Interfaccia utente per [!UICONTROL Allocazione automatica] attività che utilizzano [!UICONTROL Analytics for Target] (A4T) come origine per la generazione di rapporti. (TGT-46112)
* Il timeout per le chiamate PUT all’API di consegna di Target è stato aumentato a 15 secondi per evitare errori di timeout. (TGT-46091)
* È stato risolto un problema che causava la visualizzazione di un nome di report errato quando si passava da un [!UICONTROL Vista tabella] e [!UICONTROL Segmenti automatizzati] e [!UICONTROL Attributi importanti] rapporti. (TGT-46040)
* È stata migliorata la [!UICONTROL Compositore esperienza visivo] (Compositore esperienza visivo) per supportare Lightning DOM (Web Components). (TGT-45422)
* È stato risolto un problema che causava l’applicazione delle azioni del Compositore esperienza visivo in un ordine errato. In alcuni casi, il Compositore esperienza visivo ha applicato alcune modifiche in modo asincrono e l’aggiunta di modifiche aggiuntive a un elemento ha causato errori se tale elemento viene visualizzato dopo un’ [!UICONTROL Inserisci] azione. (TGT-45983)
* È stato risolto un problema che si verificava all’apertura di una pagina di un’applicazione a pagina singola (SPA) nel Compositore esperienza visivo, quando si passava alla modalità Sfoglia, causava il malfunzionamento delle frecce Indietro e Avanti. (TGT-45956)
* È stato risolto un problema che impediva l’aggiornamento coerente dell’URL durante la navigazione in un sito web di un’applicazione a pagina singola (SPA). (TGT-45417)

## Note aggiuntive e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=it) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js [!DNL Adobe Target]. |

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
