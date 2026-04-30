---
keywords: note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti;aggiornamenti;aggiornamenti correnti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
short-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 7976d43e43baeabdb68509373f1b0b72bbe723b3
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 49%

---

# Note sulla versione (corrente) di [!DNL Target]

Esplora le funzioni, i miglioramenti e le correzioni più recenti in [!DNL Adobe Target]. Queste note sulla versione descrivono anche gli aggiornamenti alle API [!DNL Target], agli SDK, a [!DNL Adobe Experience Platform Web SDK], at.js e ad altri componenti della piattaforma, se applicabili.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## Aggiornamenti urgenti da conoscere {#time-sensitive}

[!BADGE Importante]{type=Informative}

Per gli aggiornamenti sensibili al tempo relativi a [!DNL Adobe Target] e alla tua implementazione, [!DNL Adobe] fornisce note dettagliate sulla versione e documentazione tramite [!UICONTROL Experience League]. Di seguito sono riportate alcune caratteristiche principali relative all’implementazione:

### La versione dell&#39;interfaccia utente [!DNL Target] è deprecata

Per ulteriori informazioni, vedere [[!DNL Target] Domande frequenti sull&#39;aggiornamento dell&#39;interfaccia utente](/help/main/c-intro/updated-ui-faq.md).

## [!DNL Target Standard/Premium] 26.4.4 (28 aprile 2026)

**Attività**

+++Vedi i dettagli

* **Errore con il filtro del pubblico nei report.** È stato risolto un problema che causava un errore nella sezione Reporting dell&#39;interfaccia utente [!DNL Target] in seguito alla modifica del filtro del pubblico in **[!UICONTROL Goals & Settings]**. (TGT-55006)

* **Ordina le attività per priorità.** È stato aggiunto l’ordinamento per priorità nell’elenco delle attività utilizzando l’intestazione di colonna **[!UICONTROL Priority]**, con ordine crescente e decrescente coerente con le altre colonne ordinabili. (TGT-54948)

* **Proprietà aggiuntive dell&#39;attività non mantenute dopo il salvataggio.** È stato risolto un problema che impediva la persistenza di alcune selezioni di **[!UICONTROL Properties]** dopo il salvataggio e la riapertura di un&#39;attività. (TGT-53889)

+++

**Localizzazione**

+++Vedi i dettagli

* **Etichette giapponesi per [!UICONTROL Page Delivery] operatori di regole.** Sono state corrette le stringhe illeggibili o danneggiate per le etichette degli operatori delle regole di consegna pagina nell’interfaccia utente giapponese. (TGT-53097)

+++

**API**

+++Vedi i dettagli

* **Reporting del supporto API [!DNL GraphQL] per `segmentId`.** Aggiunto `segmentId` all&#39;API [!DNL GraphQL] per la generazione di rapporti. (TGT-55021)

+++

**[!UICONTROL Visual Experience Composer](VEC)**

+++Vedi i dettagli

* **Modifiche visualizzate nell&#39;esperienza errata nell&#39;editor.** È stato risolto un problema che causava la visualizzazione di un&#39;eliminazione o altra modifica nell&#39;esperienza errata dopo il passaggio tra le esperienze in [!UICONTROL Visual Experience Composer]. (TGT-54955)

* **Modifiche rimosse durante l&#39;eliminazione di Inserisci HTML.** È stato risolto un problema a causa del quale l&#39;eliminazione del blocco **[!UICONTROL HTML]** aggiuntivo aggiunto con **[!UICONTROL Insert before]** o **[!UICONTROL Insert after]** rimuoveva anche una modifica collegata priva di selettore CSS. (TGT-54530)

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
