---
keywords: note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti;aggiornamenti;aggiornamenti correnti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
short-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 860dd22fc4ec261a62869cb656d72bd49f2bd91c
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 51%

---

# Note sulla versione (corrente) di [!DNL Target]

Esplora le funzioni, i miglioramenti e le correzioni più recenti in [!DNL Adobe Target]. Queste note sulla versione descrivono anche gli aggiornamenti alle API [!DNL Target], agli SDK, a [!DNL Adobe Experience Platform Web SDK], at.js e ad altri componenti della piattaforma, se applicabili.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## Aggiornamenti urgenti da conoscere {#time-sensitive}

[!BADGE Importante]{type=Informative}

Per gli aggiornamenti sensibili al tempo relativi a [!DNL Adobe Target] e alla tua implementazione, [!DNL Adobe] fornisce note dettagliate sulla versione e documentazione tramite [!UICONTROL Experience League]. Di seguito sono riportate alcune caratteristiche principali relative all’implementazione:

### La versione dell&#39;interfaccia utente [!DNL Target] è deprecata

Per ulteriori informazioni, vedere [[!DNL Target] Domande frequenti sull&#39;aggiornamento dell&#39;interfaccia utente](/help/main/c-intro/updated-ui-faq.md).

## [!DNL Target Standard/Premium] 26.5.1 (7 maggio 2026)

**Integrazioni**

+++Vedi i dettagli

* Gestione di **[!DNL Adobe Target]in Experimentation Accelerator.** È stato aggiunto il supporto per l&#39;assegnazione di [!DNL Target] aree di lavoro alle sandbox di Experimentation Accelerator in modo che i team possano visualizzare gli esperimenti di [!DNL Adobe Target] in Experimentation Accelerator in un&#39;unica posizione. [Ulteriori informazioni](../c-integrating-target-with-mac/experimentation-accelerator.md)

+++

**Attività**

+++Vedi i dettagli

* **[!UICONTROL Graph View]non sincronizzati con la tabella e il download.** È stato risolto un problema che causava la visualizzazione di metriche mancanti o pari a zero in **[!UICONTROL Graph View]** per alcuni intervalli di date anche se **[!UICONTROL Table View]** e il report scaricato mostravano ancora i valori corretti. (TGT-54998)

+++

**[!UICONTROL Audiences]**

+++Vedi i dettagli

* **Elenco di utilizzo del pubblico non completamente sottoposto a rendering.** È stato risolto un problema a causa del quale la sezione **[!UICONTROL Usage]** nei dettagli del pubblico poteva visualizzare solo un sottoinsieme di attività mappate anche quando a quel pubblico erano associate attività aggiuntive. (TGT-55094)

+++

**[!UICONTROL Administration]**

+++Vedi i dettagli

* **Conferma più chiara per l&#39;offuscamento dell&#39;IP dell&#39;ultimo ottetto.** Quando modifichi **[!UICONTROL Obfuscate Visitor IP addresses]** in **[!UICONTROL Last octet]** il **[!UICONTROL Administration]** > **[!UICONTROL Implementation]**, nella finestra di dialogo di conferma viene ora spiegato che [!DNL Target] nasconde l&#39;ultimo ottetto dell&#39;indirizzo IP del visitatore. (TGT-44821)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++Vedi i dettagli

* **Pagina vuota o incompleta con Compositore esperienza avanzato.** È stato risolto un problema che impediva a [!UICONTROL Visual Experience Composer] di caricare il sito nell&#39;editor quando **[!UICONTROL Enhanced Experience Composer]** era abilitato. (TGT-54576)

+++


<!--
* **Blank page or CORS errors with Enhanced Experience Composer.** Fixed an issue where the [!UICONTROL Visual Experience Composer] could fail to load when Enhanced Experience Composer (EEC) was enabled. (TGT-54576)




**[!UICONTROL Visual Experience Composer] (VEC)**

+++See details

* **Click tracking for Experience B.** Fixed an issue where click tracking was not saved for **[!UICONTROL Experience B]** in the [!UICONTROL Visual Experience Composer]. (TGT-54843)

+++
-->

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
