---
keywords: Release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates
description: Queste note sulla versione forniscono informazioni su funzioni, miglioramenti, correzioni e problemi noti per ciascuna versione di Adobe Target Standard e Target Premium.
title: 'Note sulla versione di Adobe Target (corrente) '
topic: Recommendations
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: 8bd08463509e06673bedd0fedf9ee15e46472826
workflow-type: tm+mt
source-wordcount: '957'
ht-degree: 31%

---


# Note sulla versione di Target (corrente){#target-release-notes-current}

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di Target Standard e Target Premium. Inoltre, se applicabile, sono incluse anche le note sulla versione per le API Target, gli SDK, la libreria JavaScript (at.js) e altre modifiche alla piattaforma.

>[!NOTE]
>
>* **mbox.js obsoleto**: Il 30 agosto 2020  Adobe Target non supporterà più la libreria mbox.js. Dopo il 30 agosto 2020, tutte le chiamate effettuate da mbox.js avranno esito negativo e avranno un impatto sulle pagine che hanno attività Target in esecuzione. È consigliabile che tutti i clienti effettuino la migrazione alla versione più recente della libreria at.js prima di tale data, in modo da evitare potenziali problemi con i siti. Per ulteriori informazioni, consulta [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) and [Adobe Target Experience Builder (Funzionamento di At.js e Generatore di competenze di ): Chat sviluppatore, migrate  Adobe Target  mbox.js in at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
   >
   >   
   Sebbene mbox.js sia attualmente supportato, a partire da luglio 2017 non sono stati forniti aggiornamenti di funzionalità per questa libreria. Il più recente at.js offre molti vantaggi rispetto a mbox.js. Tra gli altri vantaggi, at.js migliora i tempi di caricamento delle pagine per le implementazioni Web, migliora la sicurezza e offre migliori opzioni di implementazione per le applicazioni a pagina singola.
   >
   >   
   Spostando tutti i clienti a at.js, i nostri tecnici e il nostro staff di supporto saranno in grado di fornirvi nuove funzionalità e di offrire il supporto che vi aspettate da Adobe.
   >
   >
* **Annunci** Target: Consultate la pagina degli annunci Target per informazioni sugli eventi in programma, comprese le sessioni di Target Experience Builder, le chat per sviluppatori, i webinar e le sessioni di Target Coffee Break. Per ulteriori informazioni, consultate Annunci [Target](/help/r-release-notes/target-announcements.md).


I codici tra parentesi sono per uso interno di [!DNL Adobe].

## versioni at.js 1.8.2 e at.js 2.3.1 (15 giugno 2020)

Nelle librerie [!DNL Target] at.js sono stati apportati i seguenti miglioramenti e correzioni:

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| Payload JSON di at.js 1.8.2 | Questa versione di at.js è una versione di manutenzione e include le seguenti correzioni:<ul><li>È stato risolto un problema che si verificava quando si utilizzavano CNAME e edge override, in at.js 1.*x* potrebbe creare in modo non corretto il dominio del server, causando il fallimento della [!DNL Target] richiesta. (TNT-35064)</li></ul>For more information, see [at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md). |
| Payload JSON di at.js 2.3.1 | Questa release di at.js è una versione di manutenzione e include i miglioramenti e le correzioni seguenti:<ul><li>L’impostazione `deviceIdLifetime` è stata sostituita tramite [targetGlobalSettings](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md). (TNT-36349)</li><li>È stato risolto un problema che si verificava quando si utilizzavano CNAME e edge override, in at.js 2.*x* potrebbe creare in modo non corretto il dominio del server, causando il fallimento della [!DNL Target] richiesta. (TNT-35065)</li><li>È stato risolto un problema che si verificava durante l’utilizzo dell’ [!DNL Target] estensione v2 e dell’ [!DNL Launch][!DNL Adobe Analytics] estensione, [!DNL Launch] causava il ritardo della [!DNL Target] chiamata [!DNL Analytics] `sendBeacon` . (TNT-36407, TNT-35990, TNT-36000)</li></ul>For more information, see [at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md). |

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
* È stato risolto un problema che consentiva di selezionare metriche incompatibili nelle attività di allocazione automatica e Target automatica che utilizzano  Analytics per Target (A4t). (TGT-36646)
* È stato risolto un problema che impediva la corretta visualizzazione di alcune opzioni in Visual Experience Composer (VEC). (TGT-36571)
* È stato risolto un problema nell&#39;interfaccia utente di Target che causava la visualizzazione in anteprima del contenuto modificato da parte di altri utenti dopo la sostituzione del contenuto in un&#39;unica esperienza. (TGT-36053 e TGT-36894)
* È stato risolto un problema che impediva ad alcuni utenti di eliminare elementi da un catalogo di Recommendations. (TGT-36455)
* È stato risolto un problema che impediva agli utenti di salvare i criteri di Recommendations in un&#39;attività con più pagine. (TGT-36249)
* È stato risolto un problema che causava la scomparsa dei pulsanti di scelta dell&#39;origine dati comportamentale durante la modifica dei criteri per una seconda volta consecutiva. (TGT-36796)
* È stato risolto un problema di visualizzazione a causa del quale un algoritmo di Recommendations visualizzava &quot;Recupero dei risultati&quot; per un periodo prolungato. (TGT-36550 e TGT-36551)
* Sono state aggiornate molte stringhe di interfaccia utente localizzate in diverse lingue.

## Note aggiuntive sulla versione e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione - API lato server di Target](/help/c-implementing-target/c-api-and-sdk-overview/releases-server-side.md) | Note sulla versione relative  Adobe Target  API lato server. |
| [Note sulla versione - SDK Node.js di Target](/help/c-implementing-target/c-api-and-sdk-overview/releases-nodejs.md) | Note sulla versione relative a  SDK Node.js  Adobe Target. |
| [Note sulla versione - Target Java SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-target-java-sdk.md) | Note sulla versione relative  SDK Java  Adobe Target. |
| [Dettagli sulle versioni di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Informazioni dettagliate sulle modifiche in ciascuna versione dell&#39;Adobe Target  in JavaScript library.js. |
| [Dettagli sulle versioni di mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mboxjs-change-log.md) | In questa pagina sono elencate le modifiche per ogni versione di mbox.js.<br>Tenete presente che la libreria mbox.js non è più in fase di sviluppo. Tutti i clienti devono migrare da mbox.js a at.js. |

## Modifiche alla documentazione, precedenti note sulla versione e note sulla versione di Experience Cloud {#section_1BC5F5208DA548E9B4344A0836E4B943}

Per informazioni aggiuntive, oltre alle note di ciascuna versione, consulta le seguenti risorse:

| Risorsa | Dettagli |
|--- |--- |
| Modifiche alla documentazione | Informazioni dettagliate sugli aggiornamenti apportati a questa guida che potrebbero non essere incluse nelle note sulla versione.<br>Per ulteriori informazioni, consulta [Modifiche alla documentazione](../r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Note sulla versione per le versioni precedenti | Informazioni su nuove funzionalità e miglioramenti introdotti nelle versioni precedenti di Target Standard e Target Premium.<br>Per ulteriori informazioni, consulta [Note sulla versione per le versioni precedenti](../r-release-notes/release-notes-for-previous-releases.md). |
| Note sulla versione di Adobe Experience Cloud | Ultime note sulla versione per le soluzioni Adobe Experience Cloud.<br>Per ulteriori informazioni, consultate [Note](https://docs.adobe.com/content/help/en/release-notes/experience-cloud/current.html)sulla versione di Experience Cloud. |

## Informazioni in anteprima {#section_5D588F0415A2435B851A4D0113ACA3A0}

Le risorse seguenti contengono informazioni sulle funzionalità in arrivo con la prossima versione di Target.

| Risorsa | Dettagli |
|--- |--- |
| Adobe Priority Product Update | Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:<br>[](https://www.adobe.com/subscription/priority-product-update.html)https://www.adobe.com/subscription/priority-product-update.html |
| Note sulle prossime versioni | Per informazioni sulle versioni di Target del mese corrente, incluse le informazioni prerelease, consulta la pagina [Note sulla versione di Target (prerelease)](/help/r-release-notes/target-release-notes.md). |
