---
keywords: Note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: dea956fe5d28200515a9638306a7d879585cb794
workflow-type: tm+mt
source-wordcount: '841'
ht-degree: 43%

---

# Note sulla versione di Target (corrente)

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di [!DNL Adobe Target Standard] e [!DNL Target Premium]. Sono inoltre incluse, ove applicabili, le note sulla versione di API di [!DNL Target], SDK, [!DNL Adobe Experience Platform Web SDK], at.js e altre modifiche alla piattaforma.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target] Standard/Premium 22.10.1 (versione scaglionata dal 5 al 7 ottobre 2022)

Questa versione sarà disponibile in base al seguente programma scaglionato:

* **5 ottobre**: regione Asia-Pacifico (APAC)
* **6 ottobre**: Regione delle Americhe
* **7 ottobre**: Area Europa, Medio Oriente e Africa (EMEA)

Questa versione contiene le seguenti nuove funzioni, miglioramenti e correzioni:

| Funzione | Dettagli |
| --- | --- |
| [!DNL Adobe Experience Manager] (AEM) frammenti di esperienza | Gli aggiornamenti alla funzionalità frammenti di esperienza AEM includono:<ul><li>È stata aggiunta la possibilità di filtrare AEM frammenti di esperienza per tipo (HTML o JSON) in [!UICONTROL Offerte] elenco. (TGT-43121)</li><li>È stato risolto un problema che consentiva ai clienti di inserire JSON [!UICONTROL Frammento esperienza] offerte quando si utilizza il Compositore esperienza visivo, che non è supportato. Le offerte JSON possono essere inserite solo quando si utilizza il [!UICONTROL Esperienza basata su moduli] compositore. (TGT-43846)</li></ul>Per ulteriori informazioni, consulta AEM [frammenti esperienza](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md). |
| Nuovo [!UICONTROL Compositore esperienza visivo] estensione per Google Chrome | Nuovo [!DNL Adobe Target] [!UICONTROL Compositore esperienza visivo] L’estensione (VEC) per Chrome è disponibile in Chrome Web Store.<br>A partire da gennaio 2023, la [!DNL Target] L’estensione VEC Helper smetterà di funzionare in Google Chrome perché Google non consente le estensioni che utilizzano Manifest V2. Scarica la nuova estensione per continuare a creare visivamente i tuoi siti web in [!DNL Target] a partire dal nuovo anno.<br>I seguenti collegamenti mostrano le due estensioni in Chrome Web Store:<ul><li>[Nuova estensione](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target=_blank}</li><li>[Vecchia estensione](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak){target=_blank}</li></ul>Per ulteriori informazioni, consulta [Estensione Visual Editing Helper](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md). |
| Metriche A4T ottimizzate per [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico]<br>(Data esatta di rilascio da determinare.) | Tieni presente le seguenti modifiche:<ul><li>È stato aggiunto il supporto per le metriche binarie e di ottimizzazione in [!UICONTROL Analytics for Target] Generazione di rapporti per A4T per [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico] attività</li><li>Comportamento mantenuto per le attività esistenti fino al 20 febbraio 2023. Dopo questa data, le attività verranno interrotte per forzare la migrazione delle attività esistenti a nuovi comportamenti</li><li>A partire dal 20 febbraio 2023, supporto per `averagetimespentonsite`, `bouncerate`e `entries` metriche in [!DNL Target] le attività diventeranno obsolete.</li></ul> |
| Aggiornamenti alla documentazione | Gli aggiornamenti principali della documentazione includono:<ul><li>Novità e aggiornamento [Documentazione dell’API per l’amministrazione di Adobe Target e la creazione di rapporti](https://developer.adobe.com/target/administer/admin-api/){target=_blank} include una copertura completa degli endpoint API di amministrazione e reporting, tra cui proprietà, offerte, host, ambienti, client, pubblico, attività e altro ancora.<br>Vedi questo e altri contenuti per sviluppatori nella sezione [[!DNL Adobe Target] [!UICONTROL Guida per gli sviluppatori]](https://developer.adobe.com/target/){target=_blank}.</li><li>[Calcoli statistici nei test A/Bn](/help/main/c-reports/statistical-methodology/statistical-calculations.md)<br>Questo articolo documenta i calcoli statistici dettagliati utilizzati nei test A/Bn manuali in [!DNL Adobe Target].<br>Le informazioni contenute in questo articolo sostituiscono le *Calcoli di Adobe Target per test A/B* file pdf precedentemente disponibile per il download su questo sito.</li></ul> |

* È stato risolto un problema che impediva la corretta visualizzazione delle informazioni sulla regola del pubblico in [!UICONTROL Perfezionamenti dei tipi di pubblico] finestra delle informazioni. (TGT-43917)
* Miglioramento delle prestazioni della [!DNL Target] Interfaccia utente per il caricamento di tipi di pubblico che si avvicinano alla [limite consigliato per le regole di targeting](/help/main/r-troubleshooting-target/target-limits.md#targeting-rules). (TGT-43675)
* È stato risolto un problema che impediva la corretta visualizzazione di alcuni componenti nel [!UICONTROL Modifiche] sul pannello [!UICONTROL Esperienze] quando crei o modifichi attività nel Compositore esperienza visivo dopo il passaggio da [!UICONTROL Componi] a [!UICONTROL Sfoglia] modalità. (TGT-43300)
* È stato risolto un problema che impediva ad alcuni clienti di archiviare [!UICONTROL Test A/B] attività che utilizzano [!UICONTROL Targeting automatico]. (TGT-40978)
* Aggiunta la possibilità di utilizzare automaticamente una singola offerta in più posizioni all&#39;interno di un singolo gruppo di reporting. (TGT-40689)

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
