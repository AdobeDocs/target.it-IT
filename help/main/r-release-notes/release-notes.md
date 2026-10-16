---
keywords: note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti;aggiornamenti;aggiornamenti correnti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di [!DNL Adobe Target].
short-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di [!DNL Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
TQID: 'https://experienceleague.adobe.com/-Unx6cVsw3wch2LJgPtvBYPe-10rdpiJ4v9F7tMSP08'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: dfc8a233-f2b5-4811-bf63-b4262aebc5a5
    internal-label: Administration and configuration
subfeature_v2:
  - id: fd0ff162-b6d3-4a11-8aeb-e165a01c0f0a
    internal-label: at.js
  - id: c5abb976-5170-45d6-bcac-66d15d10a4d4
    internal-label: Release notes
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: ece061af0f50ec45e07b9710d355a9c91731578e
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 42%
---
# Note sulla versione (corrente) di [!DNL Target]

Esplora le funzioni, i miglioramenti e le correzioni più recenti in [!DNL Adobe Target]. Queste note sulla versione descrivono anche gli aggiornamenti alle API [!DNL Target], agli SDK, a [!DNL Adobe Experience Platform Web SDK], at.js e ad altri componenti della piattaforma, se applicabili.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target Standard/Premium] 26.10.2 (15 ottobre 2026)

**[!UICONTROL Attività]**

+++Vedi i dettagli

* **Impostazioni obiettivo errate visualizzate nella panoramica attività**. È stato risolto un problema a causa del quale le impostazioni dell&#39;obiettivo visualizzate nella pagina **[!UICONTROL Panoramica]** di un&#39;attività non erano corrette. Ad esempio, `https://` è stato aggiunto all&#39;URL della pagina e la condizione **[!UICONTROL URL contiene]** non è stata visualizzata, anche se la configurazione effettiva dell&#39;obiettivo era corretta. (TGT-56326)

+++

**[!UICONTROL Funzione Consigli]**

+++Vedi i dettagli

* **Consigli di backup visualizzati dopo l&#39;aggiornamento di una promozione in un&#39;attività live**. È stato risolto un problema a causa del quale la modifica di una promozione in un&#39;attività di [!DNL Recommendations] in tempo reale causava la creazione di nuove promozioni e unità di consigli da parte di [!DNL Target], anche se la definizione non era modificata. (TGT-56369)

+++

**[!UICONTROL Rapporti]**

+++Vedi i dettagli

* **Predefiniti per rapporti eliminati dopo due settimane**. È stato risolto un problema a causa del quale i predefiniti per la generazione di rapporti salvati dagli utenti per un’attività venivano eliminati automaticamente dopo circa due settimane. (TGT-56374)

+++

**[!UICONTROL Compositore esperienza visivo] (VEC)**

+++Vedi i dettagli

* Supporto di **Safari aggiunto a[!DNL Adobe Target]**. [!DNL Target] è ora supportato nel browser [!DNL Safari]. Compositore esperienza visivo e [!DNL Enhanced Experience Composer] non sono supportati in [!DNL Safari]. Di conseguenza, in [!DNL VEC] viene ora visualizzata una sovrapposizione per avvisare gli utenti che devono passare a [!DNL Chrome] per utilizzare l&#39;editor. (TGT-55853)
  [Ulteriori informazioni](../c-experiences/c-visual-experience-composer/visual-experience-composer.md#browser-requirements)
+++


## [!DNL Target Standard/Premium] 26.10.1 (13 ottobre 2026)

**[!UICONTROL Analytics per Target]**

+++Vedi i dettagli

* **La generazione di rapporti A4T non riesce e viene visualizzato l&#39;errore &quot;Si è verificato un errore&quot;**. È stato risolto un problema a causa del quale le attività [!DNL A4T] che utilizzano una suite di rapporti appena aggiunta visualizzavano un errore &quot;Si è verificato un errore&quot; nel rapporto [!DNL Target] anziché nei risultati. Facendo clic su **[!UICONTROL Visualizza in Analytics]** viene visualizzato anche il messaggio &quot;Suite di rapporti non compatibile&quot; con informazioni di classificazione [!DNL Analytics for Target] mancanti. (TGT-56389)

+++

**[!UICONTROL Compositore esperienza visivo] (VEC)**

+++Vedi i dettagli

* **È stato visualizzato un HTML non elaborato invece del nome dell&#39;offerta per [!DNL Experience Fragments] distribuito tramite una mbox**. È stato risolto un problema che causava la visualizzazione di codice/HTML non elaborato nel pannello **[!UICONTROL Modifiche]** al posto del nome dell&#39;offerta quando un [!DNL Experience Fragment] veniva distribuito tramite una mbox. (TGT-56241)

+++

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
