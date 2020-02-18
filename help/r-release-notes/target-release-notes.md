---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes
description: Note sulla versione che forniscono informazioni su funzioni, miglioramenti e correzioni per le versioni DNL Adobe Target più recenti o imminenti.
title: Note sulla versione prerelease di Adobe Target
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: 48b0141e7234ad3bbff9a6805cdf5ccb4c1aa0b9

---


# Note sulla versione di Target (prerelease){#target-release-notes-prerelease}

Queste note sulla versione contengono informazioni su funzioni, miglioramenti e correzioni per le versioni più recenti o in arrivo di [!DNL Adobe Target].

**Ultimo aggiornamento: 18 febbraio 2020**

>[!NOTE]
>
>* Questo articolo contiene informazioni prerelease. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso. Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali o possono essere diverse, a seconda della tempistica delle release.
   >
   >
* I codici tra parentesi sono per uso interno di [!DNL Adobe].
   >
   >
* A partire dal 1 marzo 2020, Target disabiliterà il supporto per la crittografia TLS 1.1 e TLS 1.0. Transport Layer Security (TLS) è tra i protocolli di sicurezza distribuiti più ampiamente ed è oggi utilizzato per i browser web e per altre applicazioni dove i dati devono essere scambiati in modo sicuro all’interno di una rete. Questa modifica è necessaria per soddisfare lo standard di conformità alla sicurezza generalmente accettato di TLS 1.2 o versione successiva. Verificare la versione TLS in uso. Se la versione in uso è inferiore alla 1.2, implementate le modifiche necessarie prima del 1 marzo 2020 per continuare a utilizzare Target come previsto.
   >
   >   
   Per informazioni dettagliate sul possibile impatto e sui passi che potrebbero essere necessari per aggiornare l&#39;implementazione, vedete Modifiche [alla crittografia](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md)TLS (Transport Layer Security).


## Target Standard/Premium 20.2.1 (19 febbraio 2020)

>[!IMPORTANT]
>
>Il 30 agosto 2020, Adobe Target non supporterà più la libreria mbox.js. Dopo il 30 agosto 2020, tutte le chiamate effettuate da mbox.js avranno esito negativo e avranno un impatto sulle pagine in cui sono in esecuzione attività Target. È consigliabile che tutti i clienti effettuino la migrazione alla versione più recente della libreria at.js prima di tale data, in modo da evitare potenziali problemi con i siti. For more information, see [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md).
>
>Sebbene mbox.js sia attualmente supportato, a partire da luglio 2017 non sono stati forniti aggiornamenti di funzionalità per questa libreria. Il più recente at.js offre molti vantaggi rispetto a mbox.js. Tra gli altri vantaggi, at.js migliora i tempi di caricamento delle pagine per le implementazioni Web, migliora la sicurezza e offre migliori opzioni di implementazione per le applicazioni a pagina singola.
>
>Spostando tutti i clienti a at.js, i nostri tecnici e il nostro staff di supporto saranno in grado di fornirvi nuove funzionalità e di offrire il supporto che vi aspettate da Adobe.

Questa versione contiene i seguenti miglioramenti e correzioni:

* È stato risolto un problema che impediva ai clienti di selezionare una raccolta durante la ricerca di un catalogo. (TGT-36230)
* È stato corretto un problema in seguito al quale un criterio creato tramite API, ma a cui non si fa riferimento da un&#39;attività creata nell&#39;interfaccia utente di Target, poteva essere eliminato erroneamente dall&#39;interfaccia utente. (TGT-35917)
* Miglioramenti della sicurezza implementati nell&#39;informativa sulla sicurezza dei contenuti (CSP). (TGT-36190)
* È stato risolto un problema che causava la visualizzazione di &quot;NaN%&quot; durante lo scorrimento della barra della percentuale di ponderazione attributo verso l&#39;estrema sinistra. (TGT-36211)
* È stato risolto un problema che impediva ai clienti di modificare l&#39;algoritmo in un&#39;attività di Automated Personalization (AP) da Foresta casuale a Varianza residua. (TGT-36321)
* Sono stati risolti i problemi di localizzazione per consentire la corretta visualizzazione del testo dell&#39;interfaccia in diverse lingue.

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
