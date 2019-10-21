---
description: Queste note sulla versione forniscono informazioni su funzionalità, miglioramenti, correzioni e problemi noti per ogni versione di Target Standard e Target Premium.
keywords: Note sulla versione;nuove funzioni;rilasci;aggiornamenti;aggiornamento;rilascio;miglioramenti;correzioni;correzioni di bug
seo-description: Queste note sulla versione forniscono informazioni su funzioni, miglioramenti, correzioni e problemi noti per ciascuna versione di Adobe Target Standard e Target Premium.
seo-title: 'Note sulla versione di Adobe Target (corrente) '
solution: Target
title: Note sulla versione di Target (corrente)
topic: Consigli
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: 956a6b88fac9a13b98ede655e930aa016fe82533

---


# Note sulla versione di Target (corrente){#target-release-notes-current}

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di Target Standard e Target Premium. Inoltre, se applicabile, sono incluse anche le note sulla versione per le API Target, gli SDK, la libreria JavaScript (at.js) e altre modifiche alla piattaforma.

I codici tra parentesi sono per uso interno di [!DNL Adobe].

## Target Standard/Premium 19.10.1 (22 ottobre 2019)

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| ![Premium badge](/help/assets/premium.png) - Raccomandazioni<br>basate sull'utente (24 ottobre 2019) | Raccomanda gli elementi in base alla cronologia di navigazione, visualizzazione e acquisto di ogni visitatore. Tali elementi sono generalmente denominati "Consigliati per l'utente."<br>Questo criterio consente di fornire contenuti ed esperienze personalizzati sia ai visitatori nuovi che di ritorno. L'elenco delle raccomandazioni è ponderato per l'attività più recente del visitatore, viene aggiornato in sessione e diventa più personalizzato man mano che il visitatore naviga nel sito.<br>Per ulteriori informazioni, vedere "Raccomandazioni basate sull'utente" in [Criteri/algoritmi](/help/c-recommendations/c-algorithms/algorithms.md#criteria-algorithms). |

### Miglioramenti, correzioni e modifiche

* Quando effettuate l’accesso al [!DNL Adobe Experience Cloud]pannello, viene visualizzata la nuova navigazione dell’intestazione. La navigazione precedente è molto simile a quella con la barra nera nella parte superiore, ma offre i seguenti miglioramenti:

   * Passaggio più semplice tra organizzazioni [!DNL Identity Management System] (IMS) o a una soluzione diversa.
   * Aiuto utente migliorato: I risultati della ricerca includono i risultati della documentazione del [!DNL Target] prodotto, forum della community e altri contenuti video, che consentono di accedere più facilmente a più contenuti per trarre il massimo vantaggio [!DNL Target]. È stato inoltre aggiunto un meccanismo di feedback nel menu [!UICONTROL Aiuto] , che semplifica la segnalazione dei problemi o la condivisione delle idee.

   * Miglioramento della funzionalità NPS (Net Promoter Score) per il feedback, in modo che il modale del sondaggio non disturbi il flusso di lavoro.
   * Flusso di accesso migliorato. Precedentemente, tutti [!DNL Target] i clienti accedevano alla pagina di destinazione di Target dopo aver fatto clic sull’ [!DNL Target] icona nell’intestazione. Questa pagina ha quindi consentito ai clienti di continuare con [!DNL Target Standard/Premium], [!DNL Search&Promote]o [!DNl Recommendations Classic], come mostrato di seguito:

      ![Pagina di destinazione](/help/r-release-notes/assets/landing.png)

      Abbiamo eliminato questa pagina di destinazione per tutti i nostri clienti. Ora è sempre possibile accedere direttamente alla pagina Elenco  attività facendo clic sull’ [!DNL Target] icona nella nuova barra di navigazione dell’intestazione.

      Se utilizzate [!DNL Recommendations Classic], potete passare direttamente alla soluzione oppure dal collegamento breve creato nella scheda [!UICONTROL Recommendations] , come illustrato di seguito:

      ![Collegamento profondo Recs Classic](/help/r-release-notes/assets/recs-classic.png)

      Se usi [!DNL Search&Promote], devi andare direttamente al collegamento. Il percorso per raggiungere [!DNL Search&Promote] dall'interno di [!DNL Adobe Target] è stato rimosso completamente.

   * Le notifiche per non [!DNL Target] sono attualmente disponibili nel menu a discesa [!UICONTROL Notifiche] dell'intestazione.
   >[!NOTE]
   >
   >Queste funzioni non verranno implementate simultaneamente, né verranno distribuite insieme a tutti i clienti. Nel corso dei prossimi giorni verranno introdotte queste funzionalità a partire dalla release [!DNL Target Standard/Premium] 19.10.1 (22 ottobre 2019).
   >
   >Durante il rollout della nuova barra di navigazione, noterete anche alcune modifiche agli URL. Tutti i precedenti collegamenti con segnalibro continuano a funzionare, ma vi invitiamo a contrassegnare nuovi collegamenti per un'apertura più rapida.

## at.js versioni 2.2 e 1.8 (10 ottobre 2019)

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| at.js versione 2.2<br><br>andat.js versione 1.8 | Queste versioni di at.js forniscono:<ul><li>Sono state migliorate le prestazioni quando si utilizzano sia il servizio Experience Cloud ID (ECID) v4.4 che at.js 2.2 o at.js 1.8 sulle pagine Web.</li><li>In precedenza, l'ECID effettuava due chiamate di blocco prima che at.js potesse recuperare le esperienze. È stato ridotto a una singola chiamata, il che migliora notevolmente le prestazioni.</li></ul> Per trarre vantaggio da questi miglioramenti in termini di prestazioni, l'aggiornamento a at.js 2.2 o at.js 1.8 insieme alla libreria ECID v4.4.<br>at.js 2.2 fornisce:<ul><li>**serverState**: Un'impostazione disponibile in at.js v2.2+ che può essere utilizzata per ottimizzare le prestazioni della pagina quando viene implementata un'integrazione ibrida di Target. L'integrazione ibrida significa che stai utilizzando sia at.js v2.2+ sul lato client che l'API di consegna o un SDK Target sul lato server per distribuire esperienze. `serverState` consente a at.js v2.2+ di applicare esperienze direttamente dal contenuto recuperato sul lato server e restituito al client come parte della pagina che viene servita.<br>Per ulteriori informazioni, vedi "serverState" in [targetGlobalSettings](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#server-state).</li></ul> |

## Piattaforma Target (9 ottobre 2019)

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| Node.js SDK versione 1.0 | L’SDK Node.js di Target consente di distribuire Target lato server.<br>Questo SDK Node.js consente di integrare facilmente Target con altre soluzioni Experience Cloud, come Adobe Experience Cloud Identity Service, Adobe Analytics e Adobe Audience Manager.<br>L’SDK Node.js introduce procedure ottimali e rimuove le complessità durante l’integrazione con Adobe Target tramite la nostra API di distribuzione, in modo che i team tecnici possano concentrarsi sulla logica aziendale. Di seguito sono riportate alcune importanti funzioni introdotte nell’ultima versione:<ul><li>Supporto per preacquisizione e notifiche che consentono di ottimizzare le prestazioni tramite caching.</li><li>Supporto per l'ottimizzazione delle prestazioni in caso di integrazione ibrida di Target sia sulle pagine Web che sul lato server. Stiamo introducendo un'impostazione denominata `serverState` che verrà compilata dalle esperienze recuperate tramite il lato server, in modo che at.js 2.2 non effettuerà più una chiamata server aggiuntiva per recuperare le esperienze. Questo approccio ottimizza le prestazioni di caricamento delle pagine.</li><li> Supporto per il recupero di attività create VEC tramite Node.js SDK, reso possibile dalla nuova API di consegna.</li><li>Apri in origine in modo che i tuoi sviluppatori possano contribuire all’SDK Node.js.</li></ul><br>Per ulteriori informazioni, vedi Note sulla [versione - SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-nodejs.md)Target Node.js. |
| API di consegna | In produzione è disponibile un endpoint API di distribuzione completamente nuovo (/v1/delivery). Le funzioni principali sono:<ul><li>Un endpoint per recuperare le esperienze per una o più mbox.</li><li>Recuperate le attività create VEC tramite l'API.</li><li>Supporto per un oggetto completamente nuovo, denominato Views (Visualizzazioni), utilizzato per le applicazioni SPA (Single Page Applications) e per le applicazioni mobili.</li></ul><br>Per ulteriori informazioni, consultate Note sulla [versione - API](/help/c-implementing-target/c-api-and-sdk-overview/releases-server-side.md)lato server di Target. |

## Note aggiuntive sulla versione e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione - API lato server di Target](/help/c-implementing-target/c-api-and-sdk-overview/releases-server-side.md) | Note sulla versione relative alle API lato server di Adobe Target. |
| [Note sulla versione - SDK Node.js di destinazione](/help/c-implementing-target/c-api-and-sdk-overview/releases-nodejs.md) | Note sulla versione relative all'SDK Node.js di Adobe Target. |
| [Dettagli sulle versioni di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Informazioni dettagliate sulle modifiche in ciascuna versione della libreria JavaScript di Adobe Target in.js. |
| [Dettagli sulle versioni di mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mboxjs-change-log.md) | In questa pagina sono elencate le modifiche per ogni versione di mbox.js.<br>La libreria mbox.js non è più in fase di sviluppo. Tutti i clienti devono migrare da mbox.js a at.js. |

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
