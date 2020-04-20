---
keywords: Release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates
description: Queste note sulla versione forniscono informazioni su funzioni, miglioramenti, correzioni e problemi noti per ciascuna versione di Adobe Target Standard e Target Premium.
title: 'Note sulla versione di Adobe Target (corrente) '
topic: Recommendations
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: 1befd131034805ba81e4d68e7e976fd290041d52

---


# Note sulla versione di Target (corrente){#target-release-notes-current}

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di Target Standard e Target Premium. Inoltre, se applicabile, sono incluse anche le note sulla versione per le API Target, gli SDK, la libreria JavaScript (at.js) e altre modifiche alla piattaforma.

>[!NOTE]
>
>* **mbox.js obsoleto**: Il 30 agosto 2020, Adobe Target non supporterà più la libreria mbox.js. Dopo il 30 agosto 2020, tutte le chiamate effettuate da mbox.js avranno esito negativo e avranno un impatto sulle pagine in cui sono in esecuzione attività Target. È consigliabile che tutti i clienti effettuino la migrazione alla versione più recente della libreria at.js prima di tale data, in modo da evitare potenziali problemi con i siti. For more information, see [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md). Consultate *Adobe Target Experience Builder (Generatore di competenze Adobe Target): Chat sviluppatore, migrate il file mbox.js di Adobe Target in at.js* di seguito per informazioni sulla registrazione per una prossima chat sviluppatore su questo argomento.
   >
   >   
   Sebbene mbox.js sia attualmente supportato, a partire da luglio 2017 non sono stati forniti aggiornamenti di funzionalità per questa libreria. Il più recente at.js offre molti vantaggi rispetto a mbox.js. Tra gli altri vantaggi, at.js migliora i tempi di caricamento delle pagine per le implementazioni Web, migliora la sicurezza e offre migliori opzioni di implementazione per le applicazioni a pagina singola.
   >
   >   
   Spostando tutti i clienti a at.js, i nostri tecnici e il nostro staff di supporto saranno in grado di fornirvi nuove funzionalità e di offrire il supporto che vi aspettate da Adobe.


I codici tra parentesi sono per uso interno di [!DNL Adobe].

## Adobe Target Experience Builder: Chat sviluppatore, trasferire mbox.js di Adobe Target in at.js {#skill-builder}

Join David Son, Adobe Target Product Manager, illustra i vantaggi della migrazione di mbox.js a at.js. Ascoltate gli ultimi aggiornamenti at.js, scoprite le sue funzionalità migliorate e come si allineano con le tendenze più ampie nel panorama tecnologico, nonché alcuni suggerimenti pratici per garantire che la migrazione da mbox.js a at.js estenda lo stesso valore da Target. Gli sviluppatori di Adobe Target non vogliono perdere questa opportunità!

Martedì 5 maggio, 8:00 - 9:00 AM (PDT)

[Registrati qui!](https://atskillbuilder-devchat.experienceleague.adobeevents.com/)

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
