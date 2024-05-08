---
keywords: note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramento;miglioramenti;correzioni;correzioni di bug;aggiornamenti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
short-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 44445f269a69a3ac3e3bc88bab8abf9fc4d51663
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 58%

---

# Note sulla versione (corrente) di [!DNL Target]

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di [!DNL Adobe Target Standard] e [!DNL Target Premium]. Sono inoltre incluse, ove applicabili, le note sulla versione di API di [!DNL Target], SDK, [!DNL Adobe Experience Platform Web SDK], at.js e altre modifiche alla piattaforma.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target] creazione di rapporti in [!DNL Adobe Customer Journey Analytics] (8 maggio 2024)

L’integrazione tra [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/customer-journey-analytics){target=_blank} e [!DNL Target] fornisce potenti strumenti di analisi per il programma di ottimizzazione, che consentono di risparmiare tempo prezioso.

I vantaggi principali dell’utilizzo di [!DNL Customer Journey Analytics] come origine di reporting per [!DNL Target] sono:

* Gli addetti al marketing possono applicare dinamicamente le metriche di successo di [!DNL Customer Journey Analytics] ai rapporti delle attività di [!DNL Target] in qualsiasi momento. Non è necessario specificare tutte le impostazioni prima di eseguire l’attività.
* Gli addetti al marketing possono trarre vantaggio da [!DNL Customer Journey Analytics] funzioni, ad esempio [Pannello Sperimentazione](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/panels/experimentation){target=_blank}, per analizzare ulteriormente la personalizzazione del sito web.
* Gli addetti al marketing possono disporre di un’unica fonte di reporting per [[!DNL Adobe Journey Optimizer]](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/reporting/cja-ajo){target=_blank} e [!DNL Target]. Entrambi i prodotti di personalizzazione possono essere collegati a [!DNL Customer Journey Analytics] per una visione più olistica della personalizzazione web.

Per ulteriori informazioni, consulta [Generazione di rapporti di Target in Adobe Customer Journey Analytics](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md).

## [!UICONTROL Visual Experience Composer] estensione helper (23 aprile 2024)

La versione precedente [!DNL Target] L’estensione helper per Compositore esperienza visivo è stata creata con Manifest V2. [!DNL Google] ha annunciato che non consentirà più le estensioni create utilizzando Manifest V2 a partire da giugno 2024. Per ulteriori informazioni, consulta [[!UICONTROL Visual Experience Composer] estensione helper](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md).

[!DNL Adobe] consiglia ai clienti di passare a quello più recente [Estensione Helper per editing video](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) non appena possibile.

## Aggiornamenti per `Browser:iPad` e `Browser:iPhone` in [!UICONTROL Browser] attributi del pubblico (30 aprile 2024)

| Aggiornamenti | Dettagli |
|--- |--- |
| [!UICONTROL Browser:iPad] e [!UICONTROL Browser:iPhone] aggiornato in [Attributi del browser](/help/main/c-target/c-audiences/c-target-rules/browser.md) utilizzato durante la creazione di tipi di pubblico. | [!DNL Adobe Target] consente di: [esegui il targeting su uno qualsiasi dei vari attributi di categoria](/help/main/c-target/c-audiences/c-target-rules/target-rules.md), inclusi i visitatori che utilizzano un [opzioni browser o browser](/help/main/c-target/c-audiences/c-target-rules/browser.md) quando visitano la tua pagina.<P>A partire da [!DNL Target] Standard/Premium 24.3.1 (4-6 marzo 2024), tipi di pubblico incorporati creati utilizzando l’interfaccia utente di Target, ad esempio `Browser:iPad` e `Browser:iPhone` verrà aggiornato per eseguire il targeting corretto per [!DNL iPad] e [!DNL iPhone] utilizzo `profile.mobile.deviceVendor`, `profile.mobile.isMobilePhone` e `profile.mobile.isTablet`.<P>Questo aggiornamento non richiede alcuna azione da parte dei clienti.<p><B>Importante</b>: per consentire ai clienti di eseguire il targeting corretto per [!DNL iPad] e [!DNL iPhone] negli script di profilo (e nei segmenti JavaScript), il cliente deve apportare modifiche manuali tramite **30 aprile 2024**. Per esempi di impostazioni alternative che devono essere modificate manualmente, vedere [Aggiornamenti per [!DNL iPad] e [!DNL iPhone] in [!UICONTROL Browser] attributi del pubblico](/help/main/c-target/c-audiences/c-target-rules/browser.md#updates). |

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

## Informazioni in anteprima {#section_5D588F0415A2435B851A4D0113ACA3A0}

Le risorse seguenti contengono informazioni sulle funzionalità in arrivo con la prossima versione di Target.

| Risorsa | Dettagli |
|--- |--- |
| [Adobe Priority Product Update](https://www.adobe.com/subscription/priority-product-update.html){target=_blank} | Notifiche anticipate sui miglioramenti dei prodotti in arrivo per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud]. |
| [Note sulla versione di Target: prerelease](/help/main/r-release-notes/target-release-notes.md){target=_blank} | Informazioni sulle versioni di Target del mese corrente, incluse le informazioni prerelease. |
