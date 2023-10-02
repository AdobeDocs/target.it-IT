---
keywords: note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramento;miglioramenti;correzioni;correzioni di bug;aggiornamenti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
short-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 159cf7595878e0412f249a52dc979e0824c717eb
workflow-type: tm+mt
source-wordcount: '782'
ht-degree: 81%

---

# Note sulla versione (corrente) di [!DNL Target]

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di [!DNL Adobe Target Standard] e [!DNL Target Premium]. Sono inoltre incluse, ove applicabili, le note sulla versione di API di [!DNL Target], SDK, [!DNL Adobe Experience Platform Web SDK], at.js e altre modifiche alla piattaforma.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target] Standard/Premium 23.9.4 (data da definire)

Questa versione include i miglioramenti e le correzioni seguenti:

| Funzione | Dettagli |
| --- | --- |
| [!UICONTROL Attività] Aggiornamento interfaccia utente<P>e<P>[!UICONTROL Feed] Aggiornamento interfaccia utente | Nell&#39;ambito del [!DNL Adobe Target] impegno continuo del team per migliorare l’esperienza utente per [!DNL Target] utenti, questa versione aggiorna la [!UICONTROL Attività] e [!DNL Recommendations] [!UICONTROL Feed] pagine in [!DNL Target] UI. Questo aggiornamento unisce e standardizza i modelli di progettazione che in precedenza erano incoerenti, aggiungendo nuovi miglioramenti.<P>Per ulteriori informazioni, consulta [Attività](/help/main/c-activities/activities.md) e [Feed](/help/main/c-recommendations/c-products/feeds.md). |
| [!DNL Recommendations] modello di implementazione | Il *Modello di implementazione di Recommendations utilizzando at.js* articoli ti aiutano a comprendere e creare [!DNL Adobe Target Recommendations] implementazione quando si utilizza la libreria JavaScript at.js.<P>Per ulteriori informazioni, consulta [Panoramica sul modello di implementazione di Recommendations tramite at.js](https://experienceleague.adobe.com/docs/target-dev/developer/implementation-patterns/atjs/recs-implementation-pattern-atjs.html){target=_blank} nel *Guida per gli sviluppatori di Adobe Target*. |

* Aggiunto [!UICONTROL Compositore esperienza visivo] Miglioramenti al Compositore esperienza visivo per i framework dinamici. (TGT-44064)
* È stato risolto un problema che causava la selezione della data in `getViewInAnalyticsId` richiesta di non aggiornamento corretto. Questa correzione consente di ricalcolare [!DNL Analytics] collega nei rapporti quando vengono modificate le impostazioni dei rapporti relativi a metriche e intervalli di date. (TGT-46246)

## [!DNL Target] Standard/Premium 23.9.3 (18 settembre 2023)

Questa versione include i miglioramenti e le correzioni seguenti:

* È stato migliorato il [!UICONTROL Compositore esperienza visivo] (VEC) per supportare componenti Web Lightning (Light DOM). (TGT-45422)
* È stato risolto un problema che causava l’applicazione delle azioni VEC in un ordine errato. In alcuni casi, il VEC ha applicato alcune modifiche in modo asincrono e l’aggiunta di ulteriori modifiche a un elemento ha causato errori se tale elemento viene visualizzato dopo un’azione [!UICONTROL Inserisci]. Corregge anche l’URL del VEC, che ora si aggiorna quando si clicca sui collegamenti di ancoraggio. (TGT-45983)
* È stato risolto un problema relativo alla funzione [!UICONTROL Sovrapposizione] del VEC, che ora supporta gli elementi in shadow DOM. (TGT-45202 e TGT-45262)
* È stato risolto un problema che si verificava all’apertura della pagina di un’applicazione a pagina singola (SPA) nel VEC e di conseguenza il passaggio alla modalità [!UICONTROL Sfoglia] causava il malfunzionamento delle frecce Indietro e Avanti. (TGT-45956)
* È stato risolto un problema che impediva il caricamento di alcune pagine web nel VEC. (TGT-45983)

## [!DNL Target] Standard/Premium 23.9.2 (12-14 settembre 2023)

Questa versione sarà disponibile in base al seguente programma scaglionato:

* **12 settembre**: area geografica delle Americhe
* **13 settembre**: area geografica Asia-Pacifico (APAC)
* **14 settembre**: area geografica Europa, Medio Oriente e Africa (EMEA)

Questa versione include i miglioramenti e le correzioni seguenti:

* È stata modificata l’API di [!DNL Analytics] per la nuova versione 2.0 API di [!DNL Analytics]. (TGT-45345)
* Sono stati risolti i problemi che hanno interessato le attività [!UICONTROL Automated Personalization] (AP) per alcuni clienti, inclusa la sincronizzazione tempestiva dell’attività sul back-end di [!DNL Target] e la possibilità di fornire l’esperienza prevista nei collegamenti di anteprima. (TGT-46202)

## [!DNL Target] Standard/Premium 23.9.1 (6-11 settembre 2023)

Questa versione sarà disponibile in base al seguente programma scaglionato:

* **6 settembre**: area geografica delle Americhe
* **7 settembre**: area geografica Europa, Medio Oriente e Africa (EMEA)
* **11 settembre**: area geografica Asia-Pacifico (APAC)

Questa versione include i miglioramenti e le correzioni seguenti:

* È stato corretto un problema che causava incoerenza nei dati di reporting nell’interfaccia utente di [!DNL Target] e nell’interfaccia utente di [!DNL Adobe Analytics] per attività di [!UICONTROL allocazione automatica] che utilizzano [!UICONTROL Analytics for Target] (A4T) come origine di reporting. (TGT-46112)
* Il timeout per le chiamate PUT all’API di consegna di Target è stato aumentato a 15 secondi, per evitare errori di timeout. (TGT-46091)
* È stato corretto un problema che impediva l’aggiornamento costante dell’URL durante la navigazione nel sito web di un’applicazione a pagina singola (SPA). (TGT-45417)

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
