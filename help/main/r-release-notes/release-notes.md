---
keywords: note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramento;miglioramenti;correzioni;correzioni di bug;aggiornamenti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
short-description: Learn about the new features, enhancements, and fixes included in the current release of [!DNL Adobe Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: db093dd3812e211a0e1437b522adcd5f87bc2e41
workflow-type: tm+mt
source-wordcount: '896'
ht-degree: 59%

---

# Note sulla versione (corrente) di [!DNL Target]

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di [!DNL Adobe Target Standard] e [!DNL Target Premium]. Sono inoltre incluse, ove applicabili, le note sulla versione di API di [!DNL Target], SDK, [!DNL Adobe Experience Platform Web SDK], at.js e altre modifiche alla piattaforma.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target] Standard/Premium 23.3.1 (28-30 marzo 2023)

Questa versione sarà disponibile in base al seguente programma scaglionato:

* **28 marzo**: area geografica Europa, Medio Oriente e Africa (EMEA)
* **29 marzo**: area geografica Asia Pacifico (APAC)
* **30 marzo**: area geografica delle Americhe

Questa versione include le nuove funzioni, i miglioramenti e le correzioni seguenti:

| Funzione | Dettagli |
|--- |--- |
| Metriche A4T ottimizzate per [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico]<p>(Data di rilascio: 30 marzo 2023) | [!DNL Target] consente di scegliere le metriche basate su eventi binomiali o le metriche basate su eventi continui quando si utilizza [!UICONTROL A4T] per attività di [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico].<P>In particolare, tieni conto delle seguenti modifiche nelle metriche supportate:<ul><li>[!DNL Target] ha mantenuto il comportamento precedente per le attività esistenti fino al 9 settembre 2023. Dopo tale data, le attività che utilizzando le metriche non supportate verranno interrotte e sarà necessario effettuarne la migrazione ai nuovi comportamenti.</li></ul>Per ulteriori informazioni, consulta &quot;Metriche di obiettivo supportate&quot; in [Supporto per A4T per [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico] attività](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md#supported).<br>In combinazione con questa funzione, sono state aggiornate le seguenti esercitazioni:<ul><li>[Configurazione dei rapporti A4T in  [!DNL Analysis Workspace]  per le attività di [!UICONTROL Allocazione automatica] ](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-allocate-activities.html?lang=it){target=_blank}</li><li>[Configurazione dei rapporti A4T in  [!DNL Analysis Workspace]  per le attività di [!UICONTROL Targeting automatico] ](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html?lang=it){target=_blank}</li></ul> |

* Miglioramento della sincronizzazione di pubblico e attività in modo che gli elementi creati in [!DNL Adobe Experience Platform] e [!DNL Adobe Audience Manager] sono disponibili in [!DNL Target] Interfaccia più rapida. (TGT-44568)
* È stata apportata una modifica per consentire agli utenti di rimuovere la [!UICONTROL URL predefinito] sotto [!UICONTROL Amministrazione] > [!UICONTROL Compositore esperienza visivo] > [!UICONTROL URL predefinito]. Questa modifica consente ai clienti di ripristinare l’URL predefinito a una stringa vuota, che in precedenza non era possibile dopo la configurazione iniziale. (TGT-44577)
* Sono state rimosse le restrizioni che impedivano ai clienti di modificare o eliminare i tipi di pubblico predefiniti (tipi di pubblico con nomi riservati). (TGT-44655)
* Disabilitato &quot;[!UICONTROL Fine]&quot; durante il caricamento degli spinaroli erano visibili nella [!DNL Target] Interfaccia utente durante la creazione [pubblico combinato](/help/main/c-target/combining-multiple-audiences.md). (TGT-44079)
* È stato corretto il [!UICONTROL Lingua] link nella parte inferiore del [!UICONTROL Tipi di pubblico] in modo che si colleghi correttamente a &quot;[!UICONTROL Preferenze di comunicazione dell&#39;account]&quot; pagina. (TGT-43562)
* È stato risolto un problema che a volte impediva ai clienti di creare [!UICONTROL Test A/B] dopo aver selezionato [!UICONTROL Adobe Analytics] opzione sotto [!UICONTROL Amministrazione] > [!UICONTROL Reporting] > [!UICONTROL Soluzione Experience Cloud di reporting]. (TGT-44844)
* È stato risolto un problema che impediva ai clienti di visualizzare l’ultima esperienza in un [!UICONTROL Test multivariato] attività con molte esperienze dall’interno di [!UICONTROL Compositore esperienza visivo] (Compositore esperienza visivo). La [Percorso DOM](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path) nella parte inferiore del Compositore esperienza visivo a volte impediva ai clienti di visualizzare l’ultima esperienza. (TGT-44578)
* È stato risolto un problema a causa del quale l’URL di navigazione nel Compositore esperienza visivo non rispecchiava la pagina corrente visibile in una normale sessione del browser se la pagina richiede l’autorizzazione o richiama reindirizzamenti. (TGT-44350)
* È stato risolto un problema che impediva ai clienti di modificare il [!UICONTROL Filtra criteri incompatibili] impostazione [!UICONTROL Recommendations] > [!UICONTROL Impostazioni]. (TGT-44398)
* È stato risolto un problema che causava la creazione di nuove richieste POST [!DNL Recommendations] feed con errore durante l’utilizzo di [!UICONTROL Classificazioni di Analytics] con suite di rapporti con punti nel loro nome. (TGT-44598)
* Collegamenti aggiornati nella [!DNL Target] Interfaccia utente per puntare al nuovo [Estensione Visual Editing Helper](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md). (TGT-44459)
* Protezione avanzata per impedire tentativi di falsificazione delle richieste lato server (SSRF) in [!DNL Recommendations] feed. (TGT-43769)
* È stato risolto un problema che impediva ai clienti di visualizzare in anteprima le immagini in [!DNL Recommendations] progetta se il nome dell&#39;immagine contiene [GB18030 caratteri](https://en.wikipedia.org/wiki/GB_18030){target=_blank}. (TGT-44614)
* È stato risolto un problema che causava [GB18030 caratteri](https://en.wikipedia.org/wiki/GB_18030){target=_blank} da evitare nel [!UICONTROL Modifiche] pannello durante la modifica [!UICONTROL Testo/HTML] di un’attività [!UICONTROL Esperienze] pagina. (TGT-44600)
* Sono state apportate diverse correzioni di localizzazione in tutta l’interfaccia utente di [!DNL Target].

## at.js versione 2.10.2 (7 marzo 2023)

* È stato risolto un problema che causava la restituzione di un errore della funzione `trackEvent`.

Per informazioni su tutte le versioni di at.js, consulta [Dettagli sulle versioni di at.js](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} in the [Adobe Target Developer Guide](https://developer.adobe.com/target/){target=_blank}.

## Note aggiuntive e dettagli sulla versione

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
