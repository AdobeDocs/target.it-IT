---
keywords: note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramento;miglioramenti;correzioni;correzioni di bug;aggiornamenti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
short-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: e130c68c838e799228956c598c583038a2f68ecf
workflow-type: ht
source-wordcount: '494'
ht-degree: 100%

---

# Note sulla versione (corrente) di [!DNL Target]

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di [!DNL Adobe Target Standard] e [!DNL Target Premium]. Sono inoltre incluse, ove applicabili, le note sulla versione di API di [!DNL Target], SDK, [!DNL Adobe Experience Platform Web SDK], at.js e altre modifiche alla piattaforma.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## Aggiornamento pianificato dell’infrastruttura Edge di [!DNL Adobe Target]  {#edge}

A causa dell’aggiornamento pianificato dell’infrastruttura Edge, è necessario inserire nell’elenco Consentiti indirizzi IP o domini aggiuntivi. Consulta i domini NAT e IP per le distribuzioni Edge 41-48 e inseriscili nell’elenco Consentiti. Gli aggiornamenti dell’infrastruttura iniziano il 9 agosto 2023.

Per ulteriori informazioni, consulta [Inserire nell’elenco Consentiti nodi Edge di Target](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/privacy/allowlist-edges.html?lang=it){target=_blank} nella *Guida per gli sviluppatori di Adobe Target*.

## [!DNL Target] Standard/Premium 23.8.1 (9 agosto 2023)

Questa versione include i miglioramenti e le correzioni seguenti:

* È stato risolto un problema che a volte impediva la corretta sincronizzazione delle attività, come mostrato nella colonna “[!UICONTROL Stato]” sulla pagina dell’elenco [!UICONTROL Attività]. (TGT-46010 e TGT-44831)
* È stato risolto un problema che a volte impediva la visualizzazione del collegamento a “[!UICONTROL Visualizza in Analytics]” sulla pagina di attività [!UICONTROL Rapporti] che utilizza [!UICONTROL Analytics for Target] (A4T) come origine di reporting. (TGT-45808)
* È stata corretta la presentazione di valori in tabelle, in modo da visualizzarli come percentuali anziché come numeri con decimali. Ad esempio, 8% invece di 0,08. (TGT-45548)
* È stato risolto un problema che impediva alla clientela di utilizzare l’attivazione della tastiera per passare all’elemento successivo nella pagina [!UICONTROL Obiettivi e impostazioni] per le attività di [!UICONTROL Targeting dell’esperienza] (XT). (TGT-44526)
* È stato risolto un problema che causava la perdita dell’attivazione della tastiera dopo l’apertura della finestra di dialogo “[!UICONTROL Aggiungi tipi di pubblico]” durante la creazione di un’attività. (TGT-44525)

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
