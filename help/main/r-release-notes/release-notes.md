---
keywords: Note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 5566393192b131b837fece1bb2a6781e2f953190
workflow-type: tm+mt
source-wordcount: '1055'
ht-degree: 100%

---

# Note sulla versione (corrente) di [!DNL Target]

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di [!DNL Adobe Target Standard] e [!DNL Target Premium]. Sono inoltre incluse, ove applicabili, le note sulla versione di API di [!DNL Target], SDK, [!DNL Adobe Experience Platform Web SDK], at.js e altre modifiche alla piattaforma.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## Rilascio di Models API (23 novembre 2022)

Le nuove Models API di [!DNL Adobe Target], dette anche “API per modelli” o “API per elenco Bloccati”, consentono agli utenti di visualizzare e gestire l’elenco dielle funzioni utilizzate nei modelli di apprendimento automatico per le attività di [!UICONTROL Automated Personalization] (AP) e [!UICONTROL Targeting automatico] (TA).

Per ulteriori informazioni, consulta [Panoramica di Models API](https://developer.adobe.com/target/before-administer/models-api/){target=_blank} nella *Guida per gli sviluppatori di Adobe Target*.

## [!DNL Target] Standard/Premium 22.10.3 (rilascio scaglionato dal 25 al 27 ottobre 2022)

Questa versione sarà disponibile in base al seguente programma scaglionato:

* **25 ottobre**: area geografica Europa, Medio Oriente e Africa (EMEA)
* **26 ottobre**: area geografica Asia-Pacifico (APAC)
* **27 ottobre**: area geografica delle Americhe

Questa versione include le nuove funzioni, i miglioramenti e le correzioni seguenti:

| Funzione | Dettagli |
| --- | --- |
| Metriche A4T ottimizzate per [!UICONTROL Allocazione automatica] e [!UICONTROL targeting automatico]<br> (disponibile per il testing per alcuni clienti selezionati. Sarà disponibile per tutti i clienti in una versione futura). | In particolare, tieni conto dei seguenti cambiamenti:<ul><li>È stato aggiunto il supporto per metriche non binarie e di ottimizzazione nel reporting di [!UICONTROL Analytics for Target] (A4T) per le attività di [!UICONTROL Allocazione automatica] e [!UICONTROL targeting automatico]</li><li>Il comportamento delle attività esistenti verrà mantenuto fino al febbraio 2023. Dopo tale data, le attività verranno interrotte e sarà necessario effettuarne la migrazione ai nuovi comportamenti.</li><li>A partire dal 20 febbraio 2023, il supporto per le metriche `averagetimespentonsite`, `bouncerate` e `entries` nelle attività [!DNL Target] sarà ritirato.</li></ul> |

* Sono state aggiunte descrizioni comando nell’interfaccia utente di [!DNL Target] per consentire ai clienti di navigare nel generatore di pubblico in modo più efficiente e per scoprire come utilizzare funzioni che potrebbero non essere familiari. (TGT-44139)
* È stata aggiunta una funzionalità per impedire ai clienti di modificare un’attività disabilitata da [!DNL Target] perché utilizza metriche non supportate. Un messaggio nell’interfaccia utente indica ai clienti di duplicare l’attività e quindi aggiornare la metrica di conversione.

   Con questa versione le metriche `averagetimespentonsite`, `bouncerate` e `entries` nelle attività di [!DNL Target] diventeranno obsolete per le nuove attività. Le attività esistenti possono continuare a utilizzare tali metriche fino a maggio 2023.

* È stata aggiunta una descrizione comando nell’interfaccia utente di [!DNL Target] per consentire ai clienti di selezionare un criterio di ottimizzazione durante la creazione o la modifica di un’attività di [!UICONTROL targeting automatico] che utilizza A4T.

## [!DNL Target] Standard/Premium 22.10.1 (rilascio scaglionato dal 10 al 13 ottobre 2022)

Questa versione sarà disponibile in base al seguente programma scaglionato:

* **10 ottobre**: area geografica Asia-Pacifico (APAC)
* **12 ottobre**: area geografica delle Americhe
* **13 ottobre**: area geografica Europa, Medio Oriente e Africa (EMEA)

Questa versione include le nuove funzioni, i miglioramenti e le correzioni seguenti:

| Funzione | Dettagli |
| --- | --- |
| [!DNL Adobe Experience Manager] Frammenti esperienza (AEM) | Gli aggiornamenti relativi alla funzionalità dei frammenti di esperienza AEM includono:<ul><li>È stata aggiunta la possibilità di filtrare i Frammenti di esperienza di (AEM) per tipo (HTML o JSON) nell’elenco delle [!UICONTROL Offerte]. (TGT-43121)</li><li>È stato risolto un problema che consentiva ai clienti di inserire offerte di [!UICONTROL Frammenti di esperienza] JSON utilizzando il Compositore esperienza visivo (VEC), azione che non è supportata. Le offerte JSON possono essere inserite esclusivamente utilizzando il [!UICONTROL Compositore esperienza basato su moduli]. (TGT-43846)</li></ul>Per ulteriori informazioni, consulta i [Frammenti esperienza AEM](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md). |
| Nuova estensione [!UICONTROL Compositore esperienza visivo] per Google Chrome | Nel Chrome Web Store, è disponibile una nuova estensione per il [!UICONTROL Compositore esperienza visivo] (VEC) di [!DNL Adobe Target] per Chrome.<br>A partire dal mese di gennaio 2023, l’attuale estensione [!DNL Target] VEC Helper cesserà di funzionare in Google Chrome perché Google non consentirà l’utilizzo di estensioni basate su Manifest V2. Scarica la nuova estensione per continuare a creare visivamente i tuoi siti web in [!DNL Target] a partire dal nuovo anno.<br>I seguenti collegamenti mostrano le due estensioni nel Chrome Web Store:<ul><li>[Nuova estensione](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target=_blank}</li><li>[Estensione precedente](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak){target=_blank}</li></ul>Per ulteriori informazioni, consulta [Estensione Helper per editing video](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md). |
| Aggiornamenti della documentazione | Gli aggiornamenti principali della documentazione includono:<ul><li>La [Documentazione delle API per l’amministrazione e il reporting di Adobe Target](https://developer.adobe.com/target/administer/admin-api/){target=_blank} nuova e aggiornata include una copertura completa degli endpoint API di amministrazione e reporting, tra cui proprietà, offerte, host, ambienti, client, tipi di pubblico, attività e molto altro ancora.<br>Consulta la documentazione e altri contenuti per sviluppatori nella sezione [[!DNL Adobe Target] [!UICONTROL Guida per gli sviluppatori]](https://developer.adobe.com/target/){target=_blank}.</li><li>[Calcoli statistici nei test A/Bn](/help/main/c-reports/statistical-methodology/statistical-calculations.md)<br>Questo articolo documenta i calcoli statistici dettagliati utilizzati nei test A/Bn manuali in [!DNL Adobe Target].<br>Le informazioni contenute in questo articolo sostituiscono il file pdf dei *Calcoli di Adobe Target per test A/B* precedentemente disponibile per il download su questo sito.</li></ul> |

* È stato risolto un problema che impediva la corretta visualizzazione delle informazioni sulle regole del pubblico nella finestra [!UICONTROL Perfezionamenti dei tipi di pubblico]. (TGT-43917)
* Sono state migliorate le prestazioni dell’interfaccia utente di [!DNL Target] durante il caricamento dei tipi di pubblico che si avvicinano al [limite consigliato per le regole di targeting](/help/main/r-troubleshooting-target/target-limits.md#targeting-rules). (TGT-43675)
* È stato risolto un problema che impediva la corretta visualizzazione di alcuni componenti sul pannello [!UICONTROL Modifiche] nella pagina [!UICONTROL Esperienze] durante la creazione o la modifica delle attività nel Compositore esperienza visivo dopo il passaggio dalla modalità [!UICONTROL Componi] alla modalità [!UICONTROL Sfoglia]. (TGT-43300)
* È stato risolto un problema che impediva ad alcuni clienti di archiviare le attività di [!UICONTROL Test A/B] che utilizzano il [!UICONTROL Targeting automatico]. (TGT-40978)
* È stata aggiunta la possibilità di utilizzare automaticamente un’unica offerta in più posizioni all’interno di un singolo gruppo di reporting. (TGT-40689)

## Note aggiuntive sulla versione e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=it) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js di [!DNL Adobe Target]. |

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
