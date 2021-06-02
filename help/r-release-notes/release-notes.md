---
keywords: Note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di Adobe Target, inclusi SDK, API e librerie JavaScript.
title: Quali nuove funzioni sono incluse nella versione corrente?
feature: Note sulla versione
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: ea5a451e71f390ddacc6ccea583112dd831184dc
workflow-type: tm+mt
source-wordcount: '701'
ht-degree: 84%

---

# Note sulla versione di Target (corrente)

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di [!DNL Adobe Target Standard] e [!DNL Target Premium]. Sono inoltre incluse, ove applicabili, le note sulla versione per API di Target, SDK, libreria JavaScript (at.js) e altre modifiche alla piattaforma. 

>[!IMPORTANT]
>
>**Terminazione di mbox.js**: a partire dal 31 marzo 2021, [!DNL Adobe Target] non supporta più la libreria mbox.js. Dopo il 31 marzo 2021, tutte le chiamate effettuate da mbox.js avranno esito negativo e le pagine che hanno attività [!DNL Target] in esecuzione, si troveranno a utilizzare il contenuto predefinito.
>
>Esegui la migrazione alla versione più recente della nuova [!DNL Adobe Experience Platform Web SDK] o della libreria JavaScript at.js per evitare potenziali problemi con i tuoi siti. Per ulteriori informazioni, consulta [Panoramica: implementare Target per web lato client](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

(I codici tra parentesi sono per uso interno di [!DNL Adobe].)

## ![Badgeversion 2.6.0 di Adobe Experience Platform Web SDK (1° giugno 2021) ](/help/assets/platform.png) [!DNL Adobe Experience Platform Web SDK] 

Questa versione di [!DNL Platform Web SDK] include il supporto per i seguenti elementi:

| Funzione | Dettagli |
| --- | --- |
| Supporto dei reindirizzamenti con [!UICONTROL Analytics for Target] (A4T) | L’SDK per web di Platform ora supporta i reindirizzamenti [!DNL Target] quando si utilizza [A4T](/help/c-integrating-target-with-mac/a4t/a4t.md).<br>Per ulteriori informazioni, consulta  [Analytics  [!DNL Target] for implementation](/help/c-integrating-target-with-mac/a4t/a4timplementation.md). |
| Token di risposta | L’SDK per web di Platform ora supporta i token di risposta [!DNL Target] .<br>Per ulteriori informazioni, consulta Token di  [risposta](/help/administrating-target/response-tokens.md). |

## at.js versione 2.5.0 (13 maggio 2021)

Questa versione di at.js include i miglioramenti e le modifiche seguenti:

* Supporto di [Decisioning sul dispositivo](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/on-device-decisioning.md) per at.js.
* Supporto dei [collegamenti di anteprima](/help/c-activities/c-activity-qa/activity-qa.md) per le attività di Automated Personalization

Questa versione rimuove anche il supporto per Microsoft Internet Explorer 10, Internet Explorer 11 e tutte le versioni precedenti. Microsoft Edge continua a essere supportato in at.js 2.5.0 e versioni successive.

## Target Standard/Premium 21.4.1 (19 aprile 2021)

Questa versione contiene le nuove funzioni e i miglioramenti seguenti. I codici tra parentesi sono per uso interno di [!DNL Adobe].

| Funzione | Dettagli |
| --- | --- |
| Supporto del decisioning sul dispositivo per at.js<br>(Data non ancora annunciata) | Il decisioning sul dispositivo consente agli addetti al marketing e agli sviluppatori di rilasciare esperienze sperimentali e personalizzazioni sul browser di un utente con latenza pressoché pari a zero.<br>Per ulteriori informazioni, consulta [Decisioning sul dispositivo per at.js.](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/on-device-decisioning.md) |
| ![Premium](/help/assets/premium.png) Operatori basati su elenco per regole di filtro delle entità | [!DNL Target Recommendations] supporta nuovi operatori basati su elenco per le regole di filtro delle entità. (TGT-39234)<br>I nuovi operatori includono:<br><ul><li>È contenuto nell’elenco</li><li>Non è contenuto nell’elenco</li><li>L’elenco contiene un elemento in</li><li>L’elenco non contiene un elemento in</li><li>L’elenco contiene tutti gli elementi in</li><li>L’elenco non contiene tutti gli elementi in</li></ul>Per ulteriori informazioni, consulta “Operatori disponibili” in [Utilizzare regole di inclusione dinamiche e statiche](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#operators). |

Questa versione include le seguenti correzioni.

* È stato risolto un problema che impediva la sincronizzazione di un’attività dopo la modifica del pubblico in [!UICONTROL Tutti i visitatori]. (TGT-40259)
* È stato risolto un problema che impediva la duplicazione delle offerte quando vengono utilizzate in posizioni diverse nelle attività [!UICONTROL Automated Personalization] anche se l’opzione [!UICONTROL Non consentire duplicati] è abilitata. (TGT-39567)
* È stato risolto un problema che impediva il caricamento corretto della pagina [!UICONTROL Amministrazione] > [!UICONTROL Configurazione Scene7]. (TGT-39918)
* È stato risolto un problema che causava il mapping delle proprietà sull’area di lavoro errata. (TGT-39869)
* È stato risolto un problema che causava un caricamento infinito se la richiesta non riusciva dopo la modifica dell’ambiente durante la creazione di un’esclusione di consigli. (TGT-39948)

## Note aggiuntive sulla versione e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Dettagli sulle versioni di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js [!DNL Adobe Target]. |

## Modifiche alla documentazione, precedenti note sulla versione e note sulla versione di Experience Cloud

Per informazioni aggiuntive, oltre alle note di ciascuna versione, consulta le seguenti risorse:

| Risorsa | Dettagli |
|--- |--- |
| Modifiche alla documentazione | Consulta le informazioni dettagliate sugli aggiornamenti di questa guida che non sono inclusi nelle presenti note sulla versione.<br>Per ulteriori informazioni, consulta [Modifiche alla documentazione](/help/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Note sulla versione per le versioni precedenti | Informazioni su nuove funzionalità e miglioramenti introdotti nelle versioni precedenti di Target Standard e Target Premium.<br>Per ulteriori informazioni, consulta [Note sulla versione per le versioni precedenti](/help/r-release-notes/release-notes-for-previous-releases.md). |
| Note sulla versione di Adobe Experience Cloud | Ultime note sulla versione per le soluzioni Adobe Experience Cloud.<br>Per ulteriori informazioni, consulta [Note sulla versione di Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=it). |

## Informazioni in anteprima {#section_5D588F0415A2435B851A4D0113ACA3A0}

Le risorse seguenti contengono informazioni sulle funzionalità in arrivo con la prossima versione di Target.

| Risorsa | Dettagli |
|--- |--- |
| Adobe Priority Product Update | Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) |
| Note sulle prossime versioni | Per informazioni sulle versioni di Target del mese corrente, incluse le informazioni prerelease, consulta la pagina [Note sulla versione di Target (prerelease)](/help/r-release-notes/target-release-notes.md). |
