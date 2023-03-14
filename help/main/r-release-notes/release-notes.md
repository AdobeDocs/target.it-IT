---
keywords: note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramento;miglioramenti;correzioni;correzioni di bug;aggiornamenti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 8cdf362d9e45153b26bca5a45ed59ef557adc016
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 56%

---

# Note sulla versione (corrente) di [!DNL Target]

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di [!DNL Adobe Target Standard] e [!DNL Target Premium]. Sono inoltre incluse, ove applicabili, le note sulla versione di API di [!DNL Target], SDK, [!DNL Adobe Experience Platform Web SDK], at.js e altre modifiche alla piattaforma.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target] Standard/Premium 22.15.1 (8 e 9 marzo 2023)

Questa versione sarà disponibile in base al seguente programma scaglionato:

* **8 marzo**: area geografica delle Americhe
* **9 marzo**: area geografica Europa, Medio Oriente e Africa (EMEA)
* **9 marzo**: area geografica Asia-Pacifico (APAC)

Questa versione contiene le nuove funzioni e i miglioramenti seguenti:

| Funzione | Dettagli |
| --- | --- |
| Metriche A4T ottimizzate per [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico] | [!DNL Target] consente di scegliere metriche basate su eventi binomiali o metriche basate su eventi continui quando si utilizza [!UICONTROL A4T] per [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico] attività.<P>Tieni presente le seguenti modifiche sensibili al tempo nelle metriche supportate:<ul><li>[!DNL Target] ha mantenuto il comportamento precedente per le attività esistenti fino al 9 settembre 2023. Dopo questa data, le attività che utilizzano metriche non supportate verranno interrotte per forzare la migrazione delle attività esistenti al nuovo comportamento.</li></ul>Per ulteriori informazioni, consulta [Metriche obiettivo supportate](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md#supported) in *Supporto A4T per attività di allocazione automatica e targeting automatico*. |
| [!UICONTROL Allocazione automatica] utilizzo [!UICONTROL Analytics for Target] (A4T) | Nuovo tutorial:<ul><li>[Configurazione dei rapporti A4T in [!DNL Analysis Workspace] per [!UICONTROL Allocazione automatica] attività](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-allocate-activities.html){target=_blank}</li></ul> |
| [!UICONTROL Targeting automatico] utilizzo [!UICONTROL Analytics for Target] (A4T) | Nuovo tutorial:<ul><li>[Configurazione dei rapporti A4T in [!DNL Analysis Workspace] per [!UICONTROL Targeting automatico] attività](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html){target=_blank}</li></ul> |

Questa versione include le seguenti correzioni:

* Aggiornamenti per la creazione di componenti web personalizzati con [!UICONTROL Compositore esperienza visivo] (VEC):

   * È stata corretta la selezione degli elementi DOM dell’ombreggiatura nel Compositore esperienza visivo, migliorando il processo di authoring in modo che non vi sia alcuna dipendenza da [!DNL Target] tipo di implementazione durante la creazione della directory principale shadow. Ora, la selezione degli elementi DOM ombra nel Compositore esperienza visivo dovrebbe funzionare per qualsiasi sito web.
   * È stato risolto un problema che impediva il caricamento di elementi HTML utilizzando #Shadow DOM nel Compositore esperienza visivo. (TGT-35801)
   * Sono stati risolti i problemi relativi al Compositore esperienza visivo con i siti web SPA che utilizzavano ShadowDOM. (TGT-43169)
   * È stato risolto un problema relativo all’obiettivo di ottimizzazione: &quot;clic su un elemento&quot; che non identificava correttamente il selettore CSS in ShadowDOM.

>[!NOTE]
>
>Per garantire la trasmissione delle modifiche create nel Compositore esperienza visivo, assicurati di utilizzare una [!DNL Target] SDK ([at.js](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} or [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html){target=_blank} (alloy.js)) con una versione superiore a 2.8.

**Problema noto**: tracciamento dei clic su un elemento principale ombra quando si utilizza [!DNL Adobe Experience Platform Web SDK] non funziona correttamente. (TNT-47012)

## at.js versione 2.10.2 (7 marzo 2023)

* È stato risolto un problema che causava la `trackEvent` per restituire sempre un errore.

Per informazioni su tutte le versioni di at.js, vedi [Dettagli sulle versioni di at.js](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} in the [Adobe Target Developer Guide](https://developer.adobe.com/target/){target=_blank}.

## Note aggiuntive sulla versione e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=it) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js [!DNL Adobe Target]. |

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
