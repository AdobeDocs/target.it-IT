---
keywords: Note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di [!DNL Adobe Target], inclusi SDK, API e librerie JavaScript.
title: Quali nuove funzioni sono incluse nella versione corrente?
feature: Note sulla versione
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: bdf8fdc0c7d92cb59270518861693ec22eb596f2
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 76%

---

# Note sulla versione di Target (corrente)

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di [!DNL Adobe Target Standard] e [!DNL Target Premium]. Sono inoltre incluse, ove applicabili, le note sulla versione per API di Target, SDK, libreria JavaScript (at.js) e altre modifiche alla piattaforma.

>[!IMPORTANT]
>
>**Terminazione di mbox.js**: a partire dal 31 marzo 2021, [!DNL Adobe Target] non supporta più la libreria mbox.js. Dopo il 31 marzo 2021, tutte le chiamate effettuate da mbox.js avranno esito negativo e le pagine che hanno attività [!DNL Target] in esecuzione, si troveranno a utilizzare il contenuto predefinito.
>
>Per evitare potenziali problemi con i siti, passa alla versione più recente del nuovo [!DNL Adobe Experience Platform Web SDK] o della libreria JavaScript at.js. Per ulteriori informazioni, consulta [Panoramica: implementare Target per web lato client](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

(I codici tra parentesi sono per uso interno di [!DNL Adobe].)

## Python SDK 1.0.0 (16 giugno 2021)

È ora disponibile il nuovo [!DNL Adobe Target] SDK Python con funzionalità di decisione sul dispositivo. Questa nuova aggiunta rafforza la suite [!DNL Target] di SDK lato server. Questi SDK ti aiutano a integrare con [!DNL Target] e a velocizzare il tuo tempo di valutazione nella lingua scelta. Le integrazioni lato server stanno diventando una scelta popolare dato che il mercato si sta spostando verso un mondo senza cookie in cui i dati di prime parti sono preziosi. Gli SDK di Target sono disponibili nei linguaggi di programmazione più popolari del mercato (Python, Java, JavaScript, C# / .Net).

Per ulteriori informazioni, consulta la [documentazione Python SDK](https://adobetarget-sdks.gitbook.io/docs/sdk-reference-guides/python-sdk) nella [guida SDK Adobe Target](https://adobetarget-sdks.gitbook.io/docs/).

## Target Standard/Premium 21.5.1 (7 giugno 2021)

Questa versione include i seguenti miglioramenti:

| Funzione | Dettagli |
| --- | --- |
| ![Badge Premium](/help/assets/premium.png) API [!DNL Recommendations] per [!UICONTROL Ricerca catalogo] | Cerca nel catalogo di prodotti e contenuti [!DNL Recommendations] a livello di programmazione tramite API per identificare gli elementi che corrispondono a un criterio di ricerca e semplificare l’amministrazione del catalogo.<br>**Limitazioni e note**:<ul><li>La ricerca nel catalogo tramite API non è supportata per gli ambienti con più di 2.000.000 elementi.</li><li>I risultati della ricerca nel catalogo tramite API vengono aggiornati più rapidamente dei risultati della ricerca nel catalogo tramite l’interfaccia utente di [!DNL Target]. La ricerca nel catalogo nell’interfaccia utente di [!DNL Target] può richiedere tempo aggiuntivo per riflettere i risultati più recenti.</li></ul>Per ulteriori informazioni, consulta [Ricerca di entità](http://developers.adobetarget.com/api/recommendations/#tag/Searching-Entities) nella guida delle API di *[!DNL Adobe Target][!DNL Recommendations]*. |

Questa versione di manutenzione contiene le seguenti correzioni.

* È stato risolto un problema che causava la modifica dell&#39;area di lavoro predefinita in un&#39;altra area di lavoro durante l&#39;aggiornamento della pagina [!UICONTROL Audiences] . (TGT-38871)
* È stato risolto un problema in [!UICONTROL Amministrazione] > [!UICONTROL Implementazione] che a volte causava un messaggio di errore che diceva: &quot;La mbox globale potrebbe non essere sincronizzata. Prova a salvarlo di nuovo.&quot;

## ![Badge Adobe Experience Platform Web SDK](/help/assets/platform.png) [!DNL Adobe Experience Platform Web SDK] versione 2.5.0 (1° giugno 2021)

Questa versione di [!DNL Platform Web SDK] include il supporto per i seguenti elementi:

| Funzione | Dettagli |
| --- | --- |
| Supporto dei reindirizzamenti con [!UICONTROL Analytics for Target] (A4T) | Platform Web SDK ora supporta i [!DNL Target]reindirizzamenti quando si utilizza [A4T](/help/c-integrating-target-with-mac/a4t/a4t.md).<br>Per ulteriori informazioni, consulta [Analytics per l’implementazione di [!DNL Target] ](/help/c-integrating-target-with-mac/a4t/a4timplementation.md). |

## at.js versione 2.5.0 (13 maggio 2021)

Questa versione di at.js include i miglioramenti e le modifiche seguenti:

* Supporto di [Decisioning sul dispositivo](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/on-device-decisioning.md) per at.js.
* Supporto dei [collegamenti di anteprima](/help/c-activities/c-activity-qa/activity-qa.md) per le attività di Automated Personalization

Questa versione rimuove anche il supporto per Microsoft Internet Explorer 10, Internet Explorer 11 e tutte le versioni precedenti. Microsoft Edge continua a essere supportato in at.js 2.5.0 e versioni successive.

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
