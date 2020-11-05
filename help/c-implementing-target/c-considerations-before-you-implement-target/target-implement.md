---
keywords: document.write;target;implement;implement target;dtm;dynamic tag management;at.js;mbox.js;target.js;mbox
description: Implementa Target facendo riferimento alle librerie (at.js o mbox.js) nelle tue pagine web.
title: Comprendere le librerie JavaScript di Target
feature: implementation general
topic: Target
uuid: c8a254c9-afc9-4a55-be01-788c11bef7cc
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '601'
ht-degree: 100%

---


# Comprendere le librerie JavaScript di [!DNL Target]{#understand-the-target-javascript-libraries}

Implementa [!DNL Target] facendo riferimento alle librerie di [!DNL Target] (at.js o mbox.js) nelle tue pagine web.

>[!NOTE]
>
>La libreria mbox.js non verrà più sviluppata. Tutti i clienti devono migrare da mbox.js a at.js. Per ulteriori informazioni, consulta [Migrazione a at.js da mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md#task_DE55DCE9AC2F49728395665DE1B1E6EA).

## Differenze tra le due librerie {#section_40117C78C2F84FECAC4F1BA40CC4F171}

Nella tabella seguente vengono illustrate le differenze tra le due librerie:

| Riferimento alla libreria | Descrizione |
|--- |--- |
| at.js | at.js sostituisce mbox.js per le implementazioni di [!DNL Target].<br>Tra gli altri vantaggi, at.js migliora i tempi di caricamento delle pagine per le implementazioni web, migliora la sicurezza, evita gli avvisi document.write in Google Chrome e fornisce migliori opzioni di implementazione per le applicazioni a pagina singola.<br>Per ulteriori informazioni, consulta [Implementazione di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md). |
| mbox.js | Prima di [!DNL Target] 16.3.1 (marzo 2016), [!DNL Target] richiedeva una chiamata a mbox.js per creare la mbox globale necessaria ad [!DNL Target] per fornire attività e tracciare i clic e la maggior parte delle metriche di successo. Questo file contiene le librerie necessarie per tutte le attività. Non è necessario mantenere diverse versioni del file specifiche per le singole attività.<br>Se sulla tua pagina sono già presenti wrapping mbox derivanti da un’implementazione precedente di [!DNL Target], puoi riutilizzarle nella nuova interfaccia. Il file mbox.js aggiornato rimane necessario, ma queste mbox possono essere selezionate per le attività e modificate utilizzando il Compositore esperienza visivo.<br>[!DNL Target] Standard e Premium aggiornano e integrano mbox.js con un riferimento a un file target.js. Il file target.js è in hosting presso Adobe. Il file Target.js consente di modificare il contenuto in qualsiasi pagina utilizzando il Compositore esperienza visivo, anche se la pagina non contiene mbox predefinite. Devi fare riferimento a questo file su ogni pagina del sito.<br>Per ulteriori informazioni, consulta [Implementazione di mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md).<br>**Importante**: la libreria mbox.js è ancora supportata, ma non ci saranno aggiornamenti di funzionalità. Tutti i clienti devono migrare a at.js. Per ulteriori informazioni, consulta [Migrazione a at.js da mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md)<br> |

## Impatto di at.js e mbox.js sul tempo di caricamento della pagina {#section_16630CD0FF0A498EB596A51381366A5A}

Molti clienti e consulenti vogliono conoscere l&#39;impatto di [!DNL at.js] e di [!DNL mbox.js] sul tempo di caricamento delle pagine, soprattutto nel contesto di nuovi utenti rispetto a utenti di ritorno. Purtroppo, è difficile misurare e offrire numeri concreti per quanto riguarda l&#39;influenza di [!DNL at.js] o [!DNL mbox.js] sul tempo di caricamento della pagina, a causa delle implementazioni del singolo cliente.

Tuttavia, se sulla pagina è presente l&#39;API dei visitatori, possiamo capire meglio in che modo [!DNL at.js] e [!DNL mbox.js] influenzano il tempo di caricamento delle pagine.

>[!NOTE]
>
>L’API dei visitatori e [!DNL at.js] o [!DNL mbox.js] hanno un impatto sul tempo di caricamento della pagina solo quando si utilizza la mbox globale (a causa della tecnica di celamento del corpo). Le mbox regionali non sono influenzate dall&#39;integrazione delle API dei visitatori.

Le sezioni seguenti illustrano la sequenza di azioni per i visitatori nuovi e per i visitatori di ritorno:

### Visitatori nuovi

1. L&#39;API dei visitatori viene caricata, analizzata ed eseguita.
1. at.js / mbox.js è caricato, analizzato ed eseguito.
1. Se la creazione automatica della mbox globale è abilitata, la libreria JavaScript di Target:

   * Crea un&#39;istanza dell&#39;oggetto Visitatore.
   * La libreria di Target cerca di recuperare i dati dell&#39;ID visitatore di Experience Cloud.
   * Poiché si tratta di un nuovo visitatore, l&#39;API dei visitatori genera una richiesta cross-domain a demdex.net.
   * Dopo il recupero dei dati dell&#39;ID visitatore di Experience Cloud, viene generata una richiesta a Target.

### Visitatori di ritorno

1. L&#39;API dei visitatori viene caricata, analizzata ed eseguita.
1. at.js / mbox.js è caricato, analizzato ed eseguito.
1. Se la creazione automatica della mbox globale è abilitata, la libreria JavaScript di Target:

   * Crea un&#39;istanza dell&#39;oggetto Visitatore.
   * La libreria di Target cerca di recuperare i dati dell&#39;ID visitatore di Experience Cloud.
   * L&#39;API dei visitatori recupera i dati dai cookie.
   * Dopo il recupero dei dati dell&#39;ID visitatore di Experience Cloud, viene generata una richiesta a Target.

>[!NOTE]
>
>Per i nuovi visitatori, quando è presente l&#39;API dei visitatori, Target deve connettersi più volte per assicurare che la richiesta includa i dati dell&#39;ID visitatore di Experience Cloud. Per i visitatori di ritorno, Target si connette solo per recuperare il contenuto personalizzato.
