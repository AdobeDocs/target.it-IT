---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates
description: Note sulla versione che forniscono informazioni su funzioni, miglioramenti e correzioni per le versioni DNL Adobe Target più recenti o imminenti.
title: Note sulla versione prerelease di Adobe Target
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: e9a6545ab65cf1214977f8fa472904527c18a04d

---


# Note sulla versione di Target (prerelease){#target-release-notes-prerelease}

Questo articolo contiene informazioni prerelease. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso.

**Ultimo aggiornamento: 24 aprile 2020**

Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni presenti in queste pagine potrebbero essere le stesse, a seconda della data di rilascio. I codici tra parentesi sono per uso interno di [!DNL Adobe].

>[!NOTE]
>
>* **mbox.js obsoleto**: Il 30 agosto 2020, Adobe Target non supporterà più la libreria mbox.js. Dopo il 30 agosto 2020, tutte le chiamate effettuate da mbox.js avranno esito negativo e avranno un impatto sulle pagine in cui sono in esecuzione attività Target. È consigliabile che tutti i clienti effettuino la migrazione alla versione più recente della libreria at.js prima di tale data, in modo da evitare potenziali problemi con i siti. For more information, see [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md). Consultate *Adobe Target Experience Builder (Generatore di competenze Adobe Target): Chat sviluppatore, migrate il file mbox.js di Adobe Target in at.js* di seguito per informazioni sulla registrazione per una prossima chat sviluppatore su questo argomento.
   >
   >   
   Sebbene mbox.js sia attualmente supportato, a partire da luglio 2017 non sono stati forniti aggiornamenti di funzionalità per questa libreria. Il più recente at.js offre molti vantaggi rispetto a mbox.js. Tra gli altri vantaggi, at.js migliora i tempi di caricamento delle pagine per le implementazioni Web, migliora la sicurezza e offre migliori opzioni di implementazione per le applicazioni a pagina singola.
   >
   >   
   Spostando tutti i clienti a at.js, i nostri tecnici e il nostro staff di supporto saranno in grado di fornirvi nuove funzionalità e di offrire il supporto che vi aspettate da Adobe.


## Adobe Target Experience Builder: Chat sviluppatore, trasferire mbox.js di Adobe Target in at.js {#skill-builder}

Join David Son, Adobe Target Product Manager, illustra i vantaggi della migrazione di mbox.js a at.js. Ascoltate gli ultimi aggiornamenti at.js, scoprite le sue funzionalità migliorate e come si allineano con le tendenze più ampie nel panorama tecnologico, nonché alcuni suggerimenti pratici per garantire che la migrazione da mbox.js a at.js estenda lo stesso valore da Target. Gli sviluppatori di Adobe Target non vogliono perdere questa opportunità!

Martedì 5 maggio, 8:00 - 9:00 AM (PDT)

[Registrati qui!](https://atskillbuilder-devchat.experienceleague.adobeevents.com/)

## Target Standard/Premium 20.4.1 (27 aprile 2020)

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

## Modifiche all&#39;API v2 per lo stato del batch profilo (4 maggio 2020)

Con la release del 4 maggio, lo stato del batch di profili restituirà solo i dati di errore a livello di riga in corso (i dati di successo non verranno restituiti). Gli ID profilo non riusciti verranno restituiti dall&#39;API in futuro.

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

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
