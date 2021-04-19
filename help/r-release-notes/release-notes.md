---
keywords: Note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di Adobe Target, inclusi SDK, API e librerie JavaScript.
title: Quali nuove funzioni sono incluse nella versione corrente?
feature: Note sulla versione
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
translation-type: tm+mt
source-git-commit: dba3044c94502ea9e25b21a3034dc581de10f431
workflow-type: tm+mt
source-wordcount: '632'
ht-degree: 35%

---

# Note sulla versione di Target (corrente)

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione [!DNL Adobe Target Standard] e [!DNL Target Premium]. Sono inoltre incluse, se applicabile, le note sulla versione per API di Target, SDK, libreria JavaScript (at.js) e altre modifiche alla piattaforma.

>[!IMPORTANT]
>
>**Terminazione di mbox.js**: A partire dal 31 marzo 2021,  [!DNL Adobe Target] non supporta più la libreria mbox.js . Dopo il 31 marzo 2021, tutte le chiamate effettuate da mbox.js avranno esito negativo e avranno un impatto positivo sulle pagine che hanno [!DNL Target] attività in esecuzione servendo il contenuto predefinito.
>
>Esegui la migrazione alla versione più recente della nuova [!DNL Adobe Experience Platform Web SDK] o della libreria JavaScript at.js prima di questa data per evitare potenziali problemi con i tuoi siti. Per ulteriori informazioni, consulta [Panoramica: implementare Target per web lato client](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

(I codici tra parentesi sono per uso interno di [!DNL Adobe].)

## Target Standard/Premium 21.4.1 (19 aprile 2021)

Questa versione contiene le nuove funzioni e i miglioramenti seguenti. I codici tra parentesi sono per uso interno di [!DNL Adobe].

| Funzione | Dettagli |
| --- | --- |
| Supporto delle decisioni sul dispositivo per at.js<br>(data da annunciare) | Le decisioni sul dispositivo consentono agli addetti al marketing e agli sviluppatori di distribuire esperimenti e personalizzazioni sul browser di un utente con latenza vicina allo zero.<br>Per ulteriori informazioni, consulta Decisioni  [sul dispositivo per at.js.](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/on-device-decisioning.md) |
| ![Operatori basati su ](/help/assets/premium.png) PremiumList per le regole di filtro entità | [!DNL Target Recommendations] supporta nuovi operatori basati su elenco per le regole di filtro entità. (TGT-39234)<br>Gli operatori appena aggiunti includono:<br><ul><li>È Contenuto Nell’Elenco</li><li>Non è contenuto nell’elenco</li><li>Elenco Contiene Un Elemento In</li><li>L&#39;Elenco Non Contiene Un Elemento In</li><li>Elenco Contiene Tutti Gli Elementi In</li><li>Elenco Non Contiene Tutti Gli Elementi</li></ul>Per ulteriori informazioni, consulta &quot;Operatori disponibili&quot; in [Utilizzare regole di inclusione dinamiche e statiche](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#operators). |

Questa versione contiene le seguenti correzioni.

* È stato risolto un problema che impediva la sincronizzazione di un&#39;attività dopo la modifica del pubblico in [!UICONTROL Tutti i visitatori]. (TGT-40259)
* È stato risolto un problema che impediva la duplicazione delle offerte quando vengono utilizzate in posizioni diverse nelle attività [!UICONTROL Automated Personalization] anche se l&#39;opzione [!UICONTROL Non consentire duplicati] è abilitata. (TGT-39567)
* È stato risolto un problema che impediva il caricamento corretto della pagina [!UICONTROL Amministrazione] > [!UICONTROL Configurazione Scene7] . (TGT-39918)
* È stato risolto un problema che causava il mapping delle proprietà all&#39;area di lavoro errata. (TGT-39869)
* È stato risolto un problema che causava un caricamento infinito se la richiesta non riusciva dopo la modifica dell’ambiente durante la creazione di un’esclusione consigli. (TGT-39948)

## at.js versione 2.5.0 (data da annunciare)

Questa versione di at.js include i miglioramenti e le modifiche seguenti:

* [Supporto ](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/on-device-decisioning.md) decisionale su dispositivo per at.js.
* [Supporto dei ](/help/c-activities/c-activity-qa/activity-qa.md) collegamenti di anteprima per le attività di Automated Personalization.

Questa versione rimuove anche il supporto per Microsoft Internet Explorer 10 e versioni successive.

## Note aggiuntive sulla versione e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Dettagli sulle versioni di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js [!DNL Adobe Target]. |

## Modifiche alla documentazione, precedenti note sulla versione e note sulla versione di Experience Cloud

Per informazioni aggiuntive, oltre alle note di ciascuna versione, consulta le seguenti risorse:

| Risorsa | Dettagli |
|--- |--- |
| Modifiche alla documentazione | Visualizza informazioni dettagliate sugli aggiornamenti apportati a questa guida che non sono inclusi in queste note sulla versione.<br>Per ulteriori informazioni, consulta [Modifiche alla documentazione](/help/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Note sulla versione per le versioni precedenti | Informazioni su nuove funzionalità e miglioramenti introdotti nelle versioni precedenti di Target Standard e Target Premium.<br>Per ulteriori informazioni, consulta [Note sulla versione per le versioni precedenti](/help/r-release-notes/release-notes-for-previous-releases.md). |
| Note sulla versione di Adobe Experience Cloud | Ultime note sulla versione per le soluzioni Adobe Experience Cloud.<br>Per ulteriori informazioni, consulta  [Experience Cloud Note sulla versione](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html). |

## Informazioni in anteprima {#section_5D588F0415A2435B851A4D0113ACA3A0}

Le risorse seguenti contengono informazioni sulle funzionalità in arrivo con la prossima versione di Target.

| Risorsa | Dettagli |
|--- |--- |
| Adobe di aggiornamento prioritario del prodotto | Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:<br>[](https://www.adobe.com/subscription/priority-product-update.html)https://www.adobe.com/subscription/priority-product-update.html |
| Note sulle prossime versioni | Per informazioni sulle versioni di Target del mese corrente, incluse le informazioni prerelease, consulta la pagina [Note sulla versione di Target (prerelease)](/help/r-release-notes/target-release-notes.md). |
