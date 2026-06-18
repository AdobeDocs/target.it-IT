---
keywords: note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti;aggiornamenti;aggiornamenti correnti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
short-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
TQID: https://experienceleague.adobe.com/-Unx6cVsw3wch2LJgPtvBYPe-10rdpiJ4v9F7tMSP08
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
subfeature_v2:
  - id: fd0ff162-b6d3-4a11-8aeb-e165a01c0f0a
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 3fc6930bcff97685e6f3f6dab1a32db05fbfed8a
workflow-type: tm+mt
source-wordcount: 612
ht-degree: 44%

---

# Note sulla versione (corrente) di [!DNL Target]

Esplora le funzioni, i miglioramenti e le correzioni più recenti in [!DNL Adobe Target]. Queste note sulla versione descrivono anche gli aggiornamenti alle API [!DNL Target], agli SDK, a [!DNL Adobe Experience Platform Web SDK], at.js e ad altri componenti della piattaforma, se applicabili.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target Standard/Premium] 26.6.5 (17 giugno 2026)

**Attività**

+++Vedi i dettagli

* **Errore durante l&#39;utilizzo da parte di un&#39;attività di tipi di pubblico eliminati all&#39;origine.** È stato risolto un problema che causava la visualizzazione di un errore a indicare che un’attività utilizzava uno o più tipi di pubblico eliminati alla sorgente. (TGT-55272)

+++

**[!UICONTROL Analytics per Target] (A4T)**

+++Vedi i dettagli

* **Rapporti A4T non visibili.** È stato risolto un problema che impediva la visualizzazione dei report [!UICONTROL Analytics for Target] (A4T). (TGT-55432)

+++

## [!DNL Target Standard/Premium] 26.6.4 (16 giugno 2026)

**Attività**

+++Vedi i dettagli

* **[!UICONTROL Salva e chiudi] nell&#39;interfaccia utente [!DNL Target] aggiornata.** È stata ripristinata l&#39;opzione **[!UICONTROL Salva e chiudi]** nell&#39;interfaccia utente [!DNL Target] aggiornata. (TGT-55152)

* **URL di controllo qualità nell&#39;interfaccia utente [!DNL Target] aggiornata.** È stato risolto un problema che impediva il corretto funzionamento degli URL di controllo qualità nell&#39;interfaccia utente [!DNL Target] aggiornata. ([TGT-55110](https://jira.corp.adobe.com/browse/TGT-55110))

+++

**Localizzazione**

+++Vedi i dettagli

* **Formato percentuale non localizzato nei report grafico panoramica attività.** È stato risolto un problema che impediva la localizzazione del formato percentuale nel grafico in **[!UICONTROL Vista grafico]** nella scheda **[!UICONTROL Rapporti]** della pagina **[!UICONTROL Panoramica attività]**. (TGT-50100)

* **Caratteri giapponesi nell&#39;URL attività.** È stato risolto un problema che causava il danneggiamento dei caratteri giapponesi nell&#39;URL attività nella pagina **[!UICONTROL Panoramica attività]** e nell&#39;elenco attività dopo il salvataggio di un&#39;attività. (TGT-53459)

* **Timestamp non localizzato nel nome attività predefinito.** È stato risolto un problema a causa del quale la marca temporale non veniva localizzata nel titolo dell’attività quando veniva mantenuto il nome attività predefinito durante la creazione dell’attività. (TGT-53273)

+++

**[!UICONTROL Funzione Consigli]**

+++Vedi i dettagli

* **Caratteri multibyte nell&#39;URL dopo la creazione dei feed.** È stato risolto un problema che causava il danneggiamento dei caratteri multibyte nell’URL dopo la creazione dei feed. (TGT-54793)

+++

<!--
* **Blank page or CORS errors with Enhanced Experience Composer.** Fixed an issue where the [!UICONTROL Visual Experience Composer] could fail to load when Enhanced Experience Composer (EEC) was enabled. (TGT-54576)

**[!UICONTROL Visual Experience Composer] (VEC)**

+++See details

* **Click tracking for Experience B.** Fixed an issue where click tracking was not saved for **[!UICONTROL Experience B]** in the [!UICONTROL Visual Experience Composer]. (TGT-54843)

+++
-->

## Aggiornamenti urgenti da conoscere {#time-sensitive}

[!BADGE Importante]{type=Informative}

Per gli aggiornamenti sensibili al tempo relativi a [!DNL Adobe Target] e alla tua implementazione, [!DNL Adobe] fornisce note dettagliate sulla versione e documentazione tramite [!UICONTROL Experience League]. Di seguito sono riportate alcune caratteristiche principali relative all’implementazione:

### La versione dell&#39;interfaccia utente [!DNL Target] è deprecata

Per ulteriori informazioni, vedere [[!DNL Target] Domande frequenti sull&#39;aggiornamento dell&#39;interfaccia utente](/help/main/c-intro/updated-ui-faq.md).

## Note aggiuntive e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=it) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js di [!DNL Adobe Target]. |

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
