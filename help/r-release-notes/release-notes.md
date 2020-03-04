---
keywords: Release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes
description: Queste note sulla versione forniscono informazioni su funzioni, miglioramenti, correzioni e problemi noti per ciascuna versione di Adobe Target Standard e Target Premium.
title: 'Note sulla versione di Adobe Target (corrente) '
topic: Recommendations
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: 669160af359972cace9c298aa061fcfa2af69072

---


# Note sulla versione di Target (corrente){#target-release-notes-current}

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di Target Standard e Target Premium. Inoltre, se applicabile, sono incluse anche le note sulla versione per le API Target, gli SDK, la libreria JavaScript (at.js) e altre modifiche alla piattaforma.

>[!NOTE]
>
>* **Modifiche** del supporto TLS: A partire dal 1 marzo 2020, Target disabiliterà il supporto per la crittografia TLS 1.1 e TLS 1.0. Transport Layer Security (TLS) è tra i protocolli di sicurezza distribuiti più ampiamente ed è oggi utilizzato per i browser web e per altre applicazioni dove i dati devono essere scambiati in modo sicuro all’interno di una rete. Questa modifica è necessaria per soddisfare lo standard di conformità alla sicurezza generalmente accettato di TLS 1.2 o versione successiva. Verificare la versione TLS in uso. Se la versione in uso è inferiore alla 1.2, implementate le modifiche necessarie prima del 1 marzo 2020 per continuare a utilizzare Target come previsto.
   >
   >   
   Per informazioni dettagliate sul possibile impatto e sui passi che potrebbero essere necessari per aggiornare l&#39;implementazione, vedete Modifiche [alla crittografia](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md)TLS (Transport Layer Security).
   >
   >
* **mbox.js obsoleto**: Il 30 agosto 2020, Adobe Target non supporterà più la libreria mbox.js. Dopo il 30 agosto 2020, tutte le chiamate effettuate da mbox.js avranno esito negativo e avranno un impatto sulle pagine in cui sono in esecuzione attività Target. È consigliabile che tutti i clienti effettuino la migrazione alla versione più recente della libreria at.js prima di tale data, in modo da evitare potenziali problemi con i siti. For more information, see [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md).
   >
   >   
   Sebbene mbox.js sia attualmente supportato, a partire da luglio 2017 non sono stati forniti aggiornamenti di funzionalità per questa libreria. Il più recente at.js offre molti vantaggi rispetto a mbox.js. Tra gli altri vantaggi, at.js migliora i tempi di caricamento delle pagine per le implementazioni Web, migliora la sicurezza e offre migliori opzioni di implementazione per le applicazioni a pagina singola.
   >
   >   
   Spostando tutti i clienti a at.js, i nostri tecnici e il nostro staff di supporto saranno in grado di fornirvi nuove funzionalità e di offrire il supporto che vi aspettate da Adobe.
   >
   >
* I codici tra parentesi sono per uso interno di [!DNL Adobe].


## Target Standard/Premium 20.2.1 (3 marzo 2020)

>[!IMPORTANT]
>
>Consultate le informazioni riportate sopra sulla rimozione di mbox.js.

Questa versione contiene i seguenti miglioramenti, correzioni e modifiche:

* È stato risolto un problema che impediva ai clienti di selezionare una raccolta durante la ricerca di un catalogo. (TGT-36230)
* È stato corretto un problema in seguito al quale un criterio creato tramite API, ma a cui non si fa riferimento da un&#39;attività creata nell&#39;interfaccia utente di Target, poteva essere eliminato erroneamente dall&#39;interfaccia utente. (TGT-35917)
* Miglioramenti della sicurezza implementati nell&#39;informativa sulla sicurezza dei contenuti (CSP). (TGT-36190)
* È stato risolto un problema che causava la visualizzazione di &quot;NaN%&quot; durante lo scorrimento della barra della percentuale di ponderazione attributo verso l&#39;estrema sinistra. (TGT-36211)
* Sono stati risolti i problemi di localizzazione per consentire la corretta visualizzazione del testo dell&#39;interfaccia in diverse lingue.
* Le seguenti metriche di Adobe Analytics non sono più supportate per Analytics for Target (A4T) a partire dalla release di marzo 2020 di Target:
   * averfacilitisitprofondità
   * bots
* Le metriche seguenti non sono più supportate e vengono automaticamente convertite in nuove versioni della stessa metrica la prima volta che un utente modifica un&#39;attività contenente la metrica:

   | Metrica obsoleta | Nuova metrica |
   |--- |--- |
   | `averagetimespentonpage` | `averagetimespentonsite` (nota: misurati in minuti anziché in secondi) |
   | `instances` | `occurrences` |
   | `singleaccess` | `singlepagevisits` |
   | `uniquevisitors` | `visitors` |
   | `visitorsdaily`, `visitorshourly`, `visitorsmonthly`, `visitorsquarterly`, `visitorsweekly`, `visitorsyearly` | `visitors` |

## Navigazione in Adobe Experience Cloud (22 febbraio 2019)

* Quando effettuate l’accesso al [!DNL Adobe Experience Cloud]pannello, viene visualizzata la nuova navigazione dell’intestazione. È molto simile alla navigazione precedente con la barra nera nella parte superiore, ma offre i seguenti miglioramenti:

   * Passaggio più semplice tra organizzazioni [!DNL Identity Management System] (IMS) o a una soluzione diversa.
   * Aiuto utente migliorato: I risultati della ricerca includono i risultati della documentazione del [!DNL Target] prodotto, forum della community e altri contenuti video, che consentono di accedere più facilmente a più contenuti per trarre il massimo vantaggio [!DNL Target]. È stato inoltre aggiunto un meccanismo di feedback nel menu [!UICONTROL Aiuto] , che semplifica la segnalazione dei problemi o la condivisione delle idee.

   * Miglioramento della funzionalità NPS (Net Promoter Score) per il feedback, in modo che il modale del sondaggio non disturbi il flusso di lavoro.
   * Flusso di accesso migliorato. Precedentemente, tutti [!DNL Target] i clienti accedevano alla pagina di destinazione di Target dopo aver fatto clic sull’ [!DNL Target] icona nell’intestazione. Questa pagina ha quindi permesso ai clienti di procedere con [!DNL Target Standard/Premium], [!DNL Search&Promote], o [!DNL Recommendations Classic], come mostrato di seguito:

      ![Pagina di destinazione](/help/r-release-notes/assets/landing.png)

      Abbiamo eliminato questa pagina di destinazione per tutti i nostri clienti. Ora è sempre possibile accedere direttamente alla pagina Elenco  attività facendo clic sull’ [!DNL Target] icona nella nuova barra di navigazione dell’intestazione.

      Se utilizzate [!DNL Recommendations Classic], potete passare direttamente alla soluzione oppure dal collegamento breve creato nella scheda [!UICONTROL Recommendations] , come illustrato di seguito:

      ![Collegamento profondo Recs Classic](/help/r-release-notes/assets/recs-classic.png)

      Se utilizzate [!DNL Search&Promote], dovete accedere direttamente all’URL [](https://center.atomz.com/center/?ims=1) Search&amp;Promote (https://center.atomz.com/center/?ims=1). Il percorso per raggiungere [!DNL Search&Promote] dall&#39;interno di [!DNL Adobe Target] è stato rimosso completamente.

   * Le notifiche per non [!DNL Target] sono attualmente disponibili nel menu a discesa [!UICONTROL Notifiche] dell&#39;intestazione.
   >[!NOTE]
   >
   >Durante il rollout della nuova barra di navigazione, noterete anche alcune modifiche agli URL. Tutti i precedenti collegamenti con segnalibro continuano a funzionare, ma vi invitiamo a contrassegnare nuovi collegamenti per un&#39;apertura più rapida.

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
