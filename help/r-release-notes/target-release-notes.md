---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates
description: Note sulla versione che forniscono informazioni su funzioni, miglioramenti e correzioni per le versioni DNL Adobe Target più recenti o imminenti.
title: Note sulla versione prerelease di Adobe Target
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: 1d34000b446c0fd37c6894bf5066f3cd16fc92a7

---


# Note sulla versione di Target (prerelease){#target-release-notes-prerelease}

Questo articolo contiene informazioni prerelease. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso.

**Ultimo aggiornamento: 25 marzo 2020**

Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni presenti in queste pagine potrebbero essere le stesse, a seconda della data di rilascio. I codici tra parentesi sono per uso interno di [!DNL Adobe].

>[!NOTE]
>
>* **mbox.js obsoleto**: Il 30 agosto 2020, Adobe Target non supporterà più la libreria mbox.js. Dopo il 30 agosto 2020, tutte le chiamate effettuate da mbox.js avranno esito negativo e avranno un impatto sulle pagine in cui sono in esecuzione attività Target. È consigliabile che tutti i clienti effettuino la migrazione alla versione più recente della libreria at.js prima di tale data, in modo da evitare potenziali problemi con i siti. For more information, see [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md).
   >
   >   
   Sebbene mbox.js sia attualmente supportato, a partire da luglio 2017 non sono stati forniti aggiornamenti di funzionalità per questa libreria. Il più recente at.js offre molti vantaggi rispetto a mbox.js. Tra gli altri vantaggi, at.js migliora i tempi di caricamento delle pagine per le implementazioni Web, migliora la sicurezza e offre migliori opzioni di implementazione per le applicazioni a pagina singola.
   >
   >   
   Spostando tutti i clienti a at.js, i nostri tecnici e il nostro staff di supporto saranno in grado di fornirvi nuove funzionalità e di offrire il supporto che vi aspettate da Adobe.


## Target at.js (25 marzo 2020)

Sono disponibili le seguenti nuove versioni delle librerie JavaScript di Target at.js:

* at.js versione 2.3.0
* at.js versione 1.8.1

For more information, see [at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).

## Target Standard/Premium 20.2.1 (23 marzo 2020)

>[!IMPORTANT]
>
>Consultate le informazioni riportate sopra sulla rimozione di mbox.js.

Questa versione contiene i seguenti miglioramenti, correzioni e modifiche:

* È stato risolto un problema che impediva ai clienti di selezionare una raccolta durante la ricerca di un catalogo. (TGT-36230)
* È stato corretto un problema in seguito al quale un criterio creato tramite API, ma a cui non si fa riferimento da un&#39;attività creata nell&#39;interfaccia utente di Target, poteva essere eliminato erroneamente dall&#39;interfaccia utente. (TGT-35917)
* Miglioramenti della sicurezza implementati nell&#39;informativa sulla sicurezza dei contenuti (CSP). (TGT-36190)
* È stato risolto un problema che causava la visualizzazione di &quot;NaN%&quot; durante lo scorrimento della barra della percentuale di ponderazione attributo verso l&#39;estrema sinistra. (TGT-36211)
* Sono stati risolti i problemi di localizzazione per consentire la corretta visualizzazione del testo dell&#39;interfaccia in diverse lingue.
* Abbiamo standardizzato l&#39;elenco delle metriche disponibili dalle attività di Adobe Analytics per Target (A4T) eliminando le metriche di Adobe Analytics non supportate nella versione corrente delle API di Adobe Analytics. Questo ci consentirà di estendere il supporto A4T nelle prossime release di Adobe Target.

   Sono state apportate le seguenti modifiche:

   * &quot;Tempo medio trascorso sulla pagina&quot; è stato sostituito da &quot;Tempo medio trascorso sul sito&quot;. Tutte le attività che utilizzano questa metrica nella metrica Obiettivo principale avranno &quot;Tempo medio trascorso sul sito&quot; (nota: misurati in minuti anziché in secondi) selezionati come Metrica obiettivo principale al successivo modifica dell&#39;attività.
   * &quot;Visitatori&quot; è stato sostituito da &quot;Visitatori unici&quot;. Per tutte le attività che utilizzano questa metrica come Metrica obiettivo principale, alla successiva modifica dell&#39;attività verrà selezionato &quot;Visitatori unici&quot; come Metrica obiettivo principale.

* Le metriche seguenti sono state eliminate e non possono più essere selezionate come Metrica obiettivo principale quando si crea una nuova attività A4T.

   | Metriche obsolete | Metriche di sostituzione suggerite |
   |--- |--- |
   | Visitatori giornalieri, Visitatori orari, Visitatori mensili, Visitatori trimestrali, Visitatori settimanali, Visitatori annuali | Visitatori univoci |
   | Profondità media delle visite | n/d Non suggerito come metrica di obiettivo principale |
   | Bot | n/d Non suggerito come metrica di obiettivo principale |
   | Frequenza arresti anomali per dispositivi mobili, Durata media sessione per dispositivi mobili, Classifica media app store, Frequenza arresti anomali delle prestazioni delle app mobili, Valutazione media app store per dispositivi mobili | n/d Non suggerito come metrica di obiettivo principale |

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
