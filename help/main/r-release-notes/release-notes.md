---
keywords: note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramento;miglioramenti;correzioni;correzioni di bug;aggiornamenti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
short-description: Learn about the new features, enhancements, and fixes included in the current release of [!DNL Adobe Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 207095a1db483abcc59f7806a67e559ee8694397
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 64%

---

# Note sulla versione (corrente) di [!DNL Target]

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di [!DNL Adobe Target Standard] e [!DNL Target Premium]. Sono inoltre incluse, ove applicabili, le note sulla versione di API di [!DNL Target], SDK, [!DNL Adobe Experience Platform Web SDK], at.js e altre modifiche alla piattaforma.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target] Standard/Premium 22.15.1 (8 e 9 marzo 2023)

Questa versione sarà disponibile in base al seguente programma scaglionato:

* **8 marzo**: Regione delle Americhe
* **9 marzo**: Area Europa, Medio Oriente e Africa (EMEA)
* **9 marzo**: regione Asia-Pacifico (APAC)

>[!NOTE]
>
>A causa di problemi che sono stati risolti nel frattempo, le metriche A4T ottimizzate per [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico]&quot; la funzionalità rilasciata l&#39;8 e il 9 marzo è stata temporaneamente rimossa. Dopo ulteriori test interni, la funzione verrà rilasciata di nuovo nelle prossime settimane.

Questa versione include le seguenti correzioni:

* Aggiornamenti per la creazione di componenti web personalizzati con la [!UICONTROL Compositore esperienza visivo] (Compositore esperienza visivo):

   * È stata corretta la selezione degli elementi DOM ombra nel Compositore esperienza visivo, ottimizzando il processo di authoring in modo che non vi sia alcuna dipendenza dal [!DNL Target] tipo di implementazione durante la creazione della radice shadow. Ora, la selezione degli elementi DOM ombra nel Compositore esperienza visivo dovrebbe funzionare per qualsiasi sito web.
   * È stato risolto un problema che impediva il caricamento di elementi HTML utilizzando #Shadow DOM nel Compositore esperienza visivo. (TGT-35801)
   * Sono stati risolti i problemi del Compositore esperienza visivo con SPA siti web che utilizzano ShadowDOM. (TGT-43169)
   * È stato risolto un problema relativo all’obiettivo di ottimizzazione: &quot;clic su un elemento&quot; che non identificava correttamente il selettore CSS in ShadowDOM.

>[!NOTE]
>
>Per garantire la consegna delle modifiche create nel Compositore esperienza visivo, assicurati di utilizzare un [!DNL Target] SDK ([at.js](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} or [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html){target=_blank} (alloy.js)) con una versione maggiore di 2.8.

**Problema noto**: Tracciamento dei clic su un elemento radice ombra quando si utilizza [!DNL Adobe Experience Platform Web SDK] non funziona correttamente. (TNT-47012)

## at.js versione 2.10.2 (7 marzo 2023)

* È stato risolto un problema che causava il `trackEvent` per restituire sempre un errore.

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
