---
keywords: note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramento;miglioramenti;correzioni;correzioni di bug;aggiornamenti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
short-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: d2aac088d5f1ae60a4b0e7ac1fff9960e2959130
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 82%

---

# Note sulla versione (corrente) di [!DNL Target]

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di [!DNL Adobe Target Standard] e [!DNL Target Premium]. Sono inoltre incluse, ove applicabili, le note sulla versione di API di [!DNL Target], SDK, [!DNL Adobe Experience Platform Web SDK], at.js e altre modifiche alla piattaforma.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target]Standard/Premium 23.11.1 (13 e 14 novembre 2023)

Questa versione è pianificata per i seguenti giorni:

* **13 novembre**: area geografica Asia-Pacifico (APAC)
* **14 novembre**: area geografica delle Americhe
* **14 novembre**: area geografica Europa, Medio Oriente e Africa (EMEA)

Questa versione include i miglioramenti e le correzioni seguenti:

* È stata migliorata la [Controllo di qualità delle attività](/help/main/c-activities/c-activity-qa/activity-qa.md) funzionalità da supportare [disabilitazione delle offerte duplicate](/help/main/c-activities/t-automated-personalization/managing-exclusions.md) per esperienze in [!UICONTROL Automated Personalization] attività. (TGT-46627)
* È stata aggiunta una descrizione nell’interfaccia utente di [!DNL Target] per aiutare la clientela a comprendere il motivo per cui potrebbero non essere disponibili dati nei rapporti sulle attività, se non viene allocato traffico all’esperienza di controllo. Nella descrizione è incluso un collegamento a ulteriori informazioni: [Perché non sono disponibili dati per il rapporto della mia attività?](/help/main/c-reports/reporting-frequently-asked-questions.md#section_E4722F6445884130951DF79981C8289B). (TGT-46610)
* È stato risolto un problema che impediva a una parte della clientela la corretta visualizzazione delle attività nella pagina [!UICONTROL Attività]. (TGT-46830)
* Sono stati risolti i seguenti problemi che interessavano le attività che utilizzavano [[!UICONTROL Analytics for Target]](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) come origine per la generazione di rapporti:
   * È stato risolto un problema che impediva ad alcuni clienti di visualizzare i dati di reporting. (TGT-46557)
   * È stato risolto un problema che a volte causava la [!UICONTROL Visualizza in Analytics] sulle pagine di reporting delle attività per non funzionare correttamente. (TGT-46731)
   * È stato risolto un problema che impediva l’utilizzo di dati per [!UICONTROL Incremento] e [!UICONTROL Affidabilità] per visualizzare correttamente in [!DNL Target] UI. (TGT-46592, TGT-46554, TGT-46586)

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
