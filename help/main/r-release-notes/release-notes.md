---
keywords: note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti;aggiornamenti;aggiornamenti correnti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
short-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
hold: true
source-git-commit: 44d9cd4de7ff2064e6005a4d7ece7f37194fbf2f
workflow-type: tm+mt
source-wordcount: '590'
ht-degree: 41%

---

# Note sulla versione (corrente) di [!DNL Target]

Esplora le funzioni, i miglioramenti e le correzioni più recenti in [!DNL Adobe Target]. Queste note sulla versione descrivono anche gli aggiornamenti alle API [!DNL Target], agli SDK, a [!DNL Adobe Experience Platform Web SDK], at.js e ad altri componenti della piattaforma, se applicabili.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## Aggiornamenti urgenti da conoscere {#time-sensitive}

[!BADGE Importante]{type=Informative}

Per gli aggiornamenti sensibili al tempo relativi a [!DNL Adobe Target] e alla tua implementazione, [!DNL Adobe] fornisce note dettagliate sulla versione e documentazione tramite [!UICONTROL Experience League]. Di seguito sono riportate alcune caratteristiche principali relative all’implementazione:

### La versione dell&#39;interfaccia utente [!DNL Target] è deprecata

Per ulteriori informazioni, vedere [[!DNL Target] Domande frequenti sull&#39;aggiornamento dell&#39;interfaccia utente](/help/main/c-intro/updated-ui-faq.md).

## [!DNL Target Standard/Premium] 26.3.2 (10 marzo 2026)

**Attività**

+++Vedi i dettagli

* **Le modifiche dirette delle offerte nell&#39;esperienza non vengono salvate.** Questa correzione risolve un problema per cui le modifiche apportate alle offerte dirette all&#39;interno di un&#39;esperienza di attività non venivano salvate. In precedenza, quando gli utenti aprivano un’offerta diretta, apportavano modifiche e la salvavano, le modifiche apparivano inizialmente riflesse ma andavano perse quando riaprivano l’offerta. La correzione assicura che le modifiche apportate alle offerte dirette vengano salvate correttamente e persistano alla riapertura dell’offerta. (TGT-54653)

+++

**Implementazione**

+++Vedi i dettagli

* **Aggiungi gestione visualizzazione momentanea di altri contenuti nella schermata Implementazione.** È stato aggiunto un nuovo interruttore alla schermata [!UICONTROL Implementation] per controllare l&#39;abilitazione dell&#39;impostazione di gestione della visualizzazione momentanea di altri contenuti. Questa opzione consente agli amministratori di configurare la gestione della visualizzazione momentanea di altri contenuti direttamente dalla schermata Implementazione. (TGT-52247)

+++

**Panoramica**

+++Vedi i dettagli

* **Mostra il nome completo del pubblico e dell&#39;esperienza nella pagina Panoramica.** Questo miglioramento aggiorna la pagina [!UICONTROL Overview] per visualizzare il nome completo dei tipi di pubblico e delle esperienze. In precedenza, i nomi lunghi venivano troncati e non erano completamente visibili; per visualizzarli, era necessario fare clic tre volte per selezionare tutto il testo. L’aggiornamento garantisce che siano visibili i nomi completi di pubblico ed esperienza, facilitando l’identificazione e la revisione delle configurazioni delle attività da parte degli utenti. (TGT-53323)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++Vedi i dettagli

* **Le modifiche del Compositore esperienza visivo non vengono applicate ai siti che utilizzano Shadow DOM (Salesforce Lightning Web Components).** Questa correzione risolve un problema in cui le modifiche apportate in Adobe Target (come le modifiche del colore di CTA) non venivano salvate o riportate sul sito attivo per i siti basati su Salesforce che utilizzano Lightning Web Components (LWC). CMS non accettava aggiornamenti dalle attività di Target e questo problema si verificava in modo coerente tra i test A/B e altri tipi di attività. (TGT-54059)

+++

## Note aggiuntive e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=it) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js [!DNL Adobe Target]. |

## Modifiche alla documentazione, precedenti note sulla versione e note sulla versione di Experience Cloud

Per informazioni aggiuntive, oltre alle note di ciascuna versione, consulta le seguenti risorse:

| Risorsa | Dettagli |
|--- |--- |
| [Modifiche alla documentazione](/help/main/r-release-notes/doc-change.md) | Consulta le informazioni dettagliate sugli aggiornamenti di questa guida che non sono inclusi nelle presenti note sulla versione. |
| [Note sulla versione per le versioni precedenti](/help/main/r-release-notes/release-notes-for-previous-releases.md). | Informazioni su nuove funzionalità e miglioramenti introdotti nelle versioni precedenti di Target Standard e Target Premium. |
| [Note sulla versione di Adobe Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=it){target=_blank} | Ultime note sulla versione per le soluzioni Adobe Experience Cloud. |

## Informazioni pre-release {#section_5D588F0415A2435B851A4D0113ACA3A0}

Le risorse seguenti contengono informazioni sulle funzionalità in arrivo con la prossima versione di Target.

| Risorsa | Dettagli |
|--- |--- |
| [Adobe Priority Product Update](https://www.adobe.com/subscription/priority-product-update.html){target=_blank} | Notifiche anticipate sui miglioramenti dei prodotti in arrivo per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud]. |
| [Note sulla versione di Target: pre-release](/help/main/r-release-notes/target-release-notes.md){target=_blank} | Informazioni sulle versioni di Target del mese corrente, incluse le informazioni pre-release. |
