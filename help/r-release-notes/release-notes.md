---
keywords: Release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates
description: Queste note sulla versione forniscono informazioni su funzioni, miglioramenti, correzioni e problemi noti per ciascuna versione di Adobe Target Standard e Target Premium.
title: 'Note sulla versione di Adobe Target (corrente) '
topic: Recommendations
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: 9a74178fa337d0890ae3c4813e01ba0a12a44902
workflow-type: tm+mt
source-wordcount: '817'
ht-degree: 33%

---


# Note sulla versione di Target (corrente){#target-release-notes-current}

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di Target Standard e Target Premium. Inoltre, se applicabile, sono incluse anche le note sulla versione per le API Target, gli SDK, la libreria JavaScript (at.js) e altre modifiche alla piattaforma.

>[!NOTE]
>
>* **mbox.js obsoleto**: Il 30 agosto 2020, Adobe Target non supporterà più la libreria mbox.js. Dopo il 30 agosto 2020, tutte le chiamate effettuate da mbox.js avranno esito negativo e avranno un impatto sulle pagine in cui sono in esecuzione attività Target. È consigliabile che tutti i clienti effettuino la migrazione alla versione più recente della libreria at.js prima di tale data, in modo da evitare potenziali problemi con i siti. For more information, see [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md). Consultate *Adobe Target Experience Builder (Generatore di competenze Adobe Target): Chat sviluppatore, effettua la migrazione di mbox.js di Adobe Target in at.js* di seguito per ulteriori informazioni.
   >
   >   
   Sebbene mbox.js sia attualmente supportato, a partire da luglio 2017 non sono stati forniti aggiornamenti di funzionalità per questa libreria. Il più recente at.js offre molti vantaggi rispetto a mbox.js. Tra gli altri vantaggi, at.js migliora i tempi di caricamento delle pagine per le implementazioni Web, migliora la sicurezza e offre migliori opzioni di implementazione per le applicazioni a pagina singola.
   >
   >   
   Spostando tutti i clienti a at.js, i nostri tecnici e il nostro staff di supporto saranno in grado di fornirvi nuove funzionalità e di offrire il supporto che vi aspettate da Adobe.
   >
   >
* **Annunci** Target: Consultate la pagina degli annunci di Target per informazioni sugli eventi in programma, comprese le sessioni di Target Experience Builder, le chat per sviluppatori, i webinar e le sessioni Target Coffee Break. Per ulteriori informazioni, vedi Annunci [Target](/help/r-release-notes/target-announcements.md).


I codici tra parentesi sono per uso interno di [!DNL Adobe].

## Modifiche all&#39;API v2 di stato batch profilo (14 maggio 2020)

Con la release del 20 maggio, lo stato del batch di profili restituirà solo i dati di errore a livello di riga in corso (i dati di successo non verranno restituiti). Gli ID profilo non riusciti verranno restituiti dall&#39;API in futuro.

Le risposte API precedenti e nuove sono le seguenti:

`ProfileBatchStatus Api
http://<<edge>>/m2/<<client>>/profile/batchStatus?batchId=<batchid>`

**Attualmente la risposta è la seguente:**

```
<response>
 
    <batchId>samplebatch-1585929692655-59449976</batchId>
 
    <status>complete</status>
 
    <batchSize>164</batchSize>
 
    <profile>
 
        <id>1514187733806-729395</id>
 
        <status>success</status>
 
    </profile>
 
    <profile>
 
        <id>1573612762055-214017</id>
 
        <status>success</status>
 
    </profile>
 
    <profile>
 
        <id>some profile id</id>
 
        <status>failed</status>
 
    </profile>
 
</response>
```

**Dopo il 4 maggio, la risposta sarà:**

```
<response>
 
    <batchId>samplebatch-1585929692655-59449976</batchId>
 
    <status>complete</status>
 
    <batchSize>164</batchSize>
 
    <profile>
 
        <id>some profile id</id>
 
        <status>failed</status>
 
    </profile>
 
</response>
```

## Target Standard/Premium 20.4.1 (6 maggio 2020)

Questa versione contiene i seguenti miglioramenti, correzioni e modifiche:

* È stato risolto un problema che classificava erroneamente un tipo di dispositivo e browser per un&#39;audience. (TGT-36266)
* È stato risolto un problema che impediva la visualizzazione dei dati del rapporto quando visualizzati su schermi con una larghezza inferiore a 963 pixel. (TGT-36549)
* È stato risolto un problema che impediva il corretto rendering dei rapporti Personalizzazione automatica. (TGT-36619)
* È stato risolto un problema che consentiva la selezione di metriche incompatibili nelle attività di allocazione automatica e di destinazione automatica che utilizzano Analytics per Target (A4t). (TGT-36646)
* È stato risolto un problema che impediva la corretta visualizzazione di alcune opzioni in Visual Experience Composer (VEC). (TGT-36571)
* È stato risolto un problema nell&#39;interfaccia di Target a causa del quale altre anteprime delle offerte di Recommendations visualizzavano il contenuto modificato dopo che un utente aveva sostituito il contenuto in un&#39;unica esperienza. (TGT-36053 e TGT-36894)
* È stato risolto un problema che impediva ad alcuni utenti di eliminare elementi da un catalogo di Recommendations. (TGT-36455)
* È stato risolto un problema che impediva agli utenti di salvare i criteri di Recommendations in un&#39;attività con più pagine. (TGT-36249)
* È stato risolto un problema che causava la scomparsa dei pulsanti di scelta dell&#39;origine dati comportamentale durante la modifica dei criteri per una seconda volta consecutiva. (TGT-36796)
* È stato risolto un problema di visualizzazione a causa del quale un algoritmo di Recommendations visualizzava &quot;Recupero dei risultati&quot; per un periodo prolungato. (TGT-36550 e TGT-36551)
* Sono state aggiornate molte stringhe di interfaccia utente localizzate in diverse lingue.

## Note aggiuntive sulla versione e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione - API lato server di Target](/help/c-implementing-target/c-api-and-sdk-overview/releases-server-side.md) | Note sulla versione relative alle API lato server di Adobe Target. |
| [Note sulla versione - SDK Node.js di destinazione](/help/c-implementing-target/c-api-and-sdk-overview/releases-nodejs.md) | Note sulla versione relative all&#39;SDK Node.js di Adobe Target. |
| [Note sulla versione - Java SDK di destinazione](/help/c-implementing-target/c-api-and-sdk-overview/releases-target-java-sdk.md) | Note sulla versione relative all&#39;SDK Java di Adobe Target. |
| [Dettagli sulle versioni di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Informazioni dettagliate sulle modifiche in ciascuna versione della libreria JavaScript di Adobe Target in.js. |
| [Dettagli sulle versioni di mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mboxjs-change-log.md) | In questa pagina sono elencate le modifiche per ogni versione di mbox.js.<br>Tenete presente che la libreria mbox.js non è più in fase di sviluppo. Tutti i clienti devono migrare da mbox.js a at.js. |

## Modifiche alla documentazione, precedenti note sulla versione e note sulla versione di Experience Cloud {#section_1BC5F5208DA548E9B4344A0836E4B943}

Per informazioni aggiuntive, oltre alle note di ciascuna versione, consulta le seguenti risorse:

| Risorsa | Dettagli |
|--- |--- |
| Modifiche alla documentazione | Informazioni dettagliate sugli aggiornamenti apportati a questa guida che potrebbero non essere incluse nelle note sulla versione.<br>Per ulteriori informazioni, consulta [Modifiche alla documentazione](../r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Note sulla versione per le versioni precedenti | Informazioni su nuove funzionalità e miglioramenti introdotti nelle versioni precedenti di Target Standard e Target Premium.<br>Per ulteriori informazioni, consulta [Note sulla versione per le versioni precedenti](../r-release-notes/release-notes-for-previous-releases.md). |
| Note sulla versione di Adobe Experience Cloud | Ultime note sulla versione per le soluzioni Adobe Experience Cloud.<br>Per ulteriori informazioni, consulta [Note](https://docs.adobe.com/content/help/en/release-notes/experience-cloud/current.html)sulla versione di Experience Cloud. |

## Informazioni in anteprima {#section_5D588F0415A2435B851A4D0113ACA3A0}

Le risorse seguenti contengono informazioni sulle funzionalità in arrivo con la prossima versione di Target.

| Risorsa | Dettagli |
|--- |--- |
| Adobe Priority Product Update | Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:<br>[](https://www.adobe.com/subscription/priority-product-update.html)https://www.adobe.com/subscription/priority-product-update.html |
| Note sulle prossime versioni | Per informazioni sulle versioni di Target del mese corrente, incluse le informazioni prerelease, consulta la pagina [Note sulla versione di Target (prerelease)](/help/r-release-notes/target-release-notes.md). |
