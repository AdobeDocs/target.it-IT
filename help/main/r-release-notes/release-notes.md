---
keywords: note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti;aggiornamenti;aggiornamenti correnti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
short-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 186bfa96c0849d9cd838b3d493c10cccfd4ff068
workflow-type: tm+mt
source-wordcount: '4104'
ht-degree: 8%

---

# Note sulla versione (corrente) di [!DNL Target]

Esplora le funzioni, i miglioramenti e le correzioni più recenti in [!DNL Adobe Target]. Queste note sulla versione descrivono anche gli aggiornamenti alle API [!DNL Target], agli SDK, a [!DNL Adobe Experience Platform Web SDK], at.js e ad altri componenti della piattaforma, se applicabili.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## Aggiornamenti urgenti da conoscere {#time-sensitive}

[!BADGE Importante]{type=Informative}

Per aggiornamenti sensibili al tempo relativi a [!DNL Adobe Target] e alla tua implementazione, [!DNL Adobe]fornisce note dettagliate sulla versione e documentazione tramite [!UICONTROL Experience League]. Di seguito sono riportate alcune caratteristiche principali relative all’implementazione:

### La versione dell&#39;interfaccia utente [!DNL Target] è deprecata

+++Vedi i dettagli
Il team [!DNL Target] offre una funzionalità temporanea che consente di passare dall&#39;interfaccia utente [!DNL Target] aggiornata alla versione precedente utilizzando un pulsante di attivazione/disattivazione. Questa opzione è disponibile solo durante la fase finale del rollout dell’interfaccia utente.

![Attivazione/disattivazione versione interfaccia utente di Target](/help/main/r-release-notes/assets/toggle.png)

Una volta completato il rollout, l’interruttore viene rimosso e tutti gli utenti passano definitivamente all’interfaccia utente aggiornata. [!DNL Adobe] consiglia di pianificare in anticipo, in quanto questa funzione verrà gradualmente eliminata a breve.

#### Timeline obsoleto

A causa dei problemi recenti identificati, principalmente correlati a complesse personalizzazioni dei clienti, il team [!DNL Target] ha regolato la timeline di obsolescenza:

* **17 giugno 2025**: tutte le organizzazioni IMS sono state abilitate per l&#39;interfaccia utente [!DNL Target] aggiornata, per utenti specifici o a livello di organizzazione, per iniziare a testare la nuova esperienza.

* **30 giugno 2025**: l&#39;esperienza [aggiornata [!DNL Target] interfaccia utente](/help/main/c-intro/understand-the-target-ui.md) è diventata predefinita per tutte le organizzazioni IMS che hanno attivato l&#39;interruttore della versione dell&#39;interfaccia utente.

   * Per impostazione predefinita, i clienti che attualmente vedono l’interfaccia utente legacy visualizzano ora l’interfaccia utente aggiornata al momento dell’accesso.
   * L’interruttore della versione dell’interfaccia utente rimane disponibile fino alla fine di luglio e consente agli utenti di tornare indietro se necessario.

  >[!IMPORTANT]
  >
  > [!DNL Adobe] consiglia vivamente di utilizzare l&#39;interfaccia utente [!DNL Target] aggiornata. Torna all&#39;interfaccia utente legacy solo se si verifica un problema di blocco, a causa di [limitazioni del comportamento di attivazione/disattivazione](#limitations).

* **dal 15 luglio al 30 luglio 2025**: l&#39;attivazione/disattivazione della versione dell&#39;interfaccia utente verrà disabilitata in modo permanente in più fasi. Le organizzazioni IMS interessate non sono più in grado di ripristinare l’interfaccia utente legacy.

   * Le eccezioni vengono esaminate caso per caso.
   * I ritardi nell’attivazione/disattivazione dell’impostazione obsoleta vengono concessi solo brevemente (alcuni giorni), mentre i problemi di blocco vengono risolti.

Contatta l&#39;[Assistenza clienti Adobe](/help/main/cmp-resources-and-contact-information.md#/help/main/cmp-resources-and-contact-information.md) per qualsiasi problema o se prevedi problemi durante questa transizione.

#### Limitazioni del comportamento di attivazione/disattivazione dell’interfaccia utente {#limitations}

Le informazioni seguenti descrivono i limiti di cui tenere conto quando si sceglie di utilizzare l’interruttore di versione:

* **Visibilità delle nuove attività**: le attività create nell&#39;interfaccia utente aggiornata non saranno visibili se si torna all&#39;interfaccia precedente.
* **Modifica di attività esistenti**: le modifiche apportate alle attività esistenti (originariamente create nell&#39;interfaccia utente legacy) durante l&#39;utilizzo dell&#39;interfaccia utente aggiornata vengono pubblicate nel sito Web. Tuttavia, se passi all’interfaccia precedente, questi aggiornamenti non sono visibili; in questa finestra vengono visualizzati solo gli ultimi aggiornamenti apportati dall’interfaccia precedente.
* **Coerenza dei dettagli dell&#39;attività**: le modifiche più recenti, indipendentemente dall&#39;interfaccia utente utilizzata, si riflettono sul sito Web attivo. Tuttavia, nell’interfaccia utente legacy vengono visualizzate solo le modifiche più recenti apportate all’interno di tale versione. Questa situazione potrebbe causare confusione se le attività modificate nell’interfaccia utente aggiornata hanno un aspetto diverso da quello visualizzato nell’interfaccia utente precedente.

#### Altre risorse sull’interfaccia utente aggiornata

* [[!DNL Target] Domande frequenti sull&#39;aggiornamento dell&#39;interfaccia utente](/help/main/c-intro/updated-ui-faq.md): queste domande frequenti riguardano le domande comuni sulla nuova interfaccia utente [!DNL Target] e sul nuovo Compositore esperienza visivo [!UICONTROL Visual Experience Composer], incluse le modifiche alla navigazione, le posizioni delle funzioni e la rimozione dell&#39;opzione di versione temporanea dell&#39;interfaccia utente. Che tu sia un addetto marketing, uno sviluppatore o un amministratore, queste domande frequenti consentono una transizione fluida e di sfruttare al massimo l’interfaccia utente aggiornata.
* [[!DNL Target Standard/Premium] 25.2.1 (17 febbraio 2025) - Note sulla versione](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-2): fornisce un riepilogo delle modifiche principali apportate all&#39;interfaccia utente in [!DNL Target] per [!UICONTROL Activities], [!UICONTROL Recommendations] e [!UICONTROL Visual Experience Composer] (Compositore esperienza visivo).
* [[!DNL Target Standard/Premium] 25.1.1 (9 gennaio 2025) - Note sulla versione](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-1): fornisce un riepilogo delle modifiche principali apportate all&#39;interfaccia utente in [!DNL Target] per [!UICONTROL Offers Library].
* [Comprendere l&#39;interfaccia utente [!DNL Target] UI](/help/main/c-intro/understand-the-target-ui.md): fornisce una breve panoramica per acquisire familiarità con [!DNL Target] e fornisce collegamenti per informazioni più approfondite e istruzioni dettagliate.
* [[!UICONTROL Visual Experience Composer] modifiche](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md): la versione di [!DNL Adobe Target Standard/Premium] 25.2.1 (17 febbraio 2015) introduce una versione aggiornata di [!UICONTROL Visual Experience Composer] (VEC). Questo articolo spiega le differenze tra le versioni legacy e aggiornata del Compositore esperienza visivo.
* [[!UICONTROL Visual Experience Composer] opzioni](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md): questo articolo illustra l&#39;interfaccia utente del Compositore esperienza visivo aggiornata e le relative opzioni.

+++

## [!DNL Target Standard/Premium] 25.9.2 (22 settembre 2025)

Questa versione include le seguenti correzioni e miglioramenti:

**[!UICONTROL Audiences]**

+++Vedi i dettagli
* **È stato risolto un problema che impediva la copia delle attività a causa di ID di pubblico non validi.** I clienti che tentavano di copiare le attività nel processo di creazione attività aggiornato hanno riscontrato un errore causato da ID di pubblico non validi (ad esempio, -1752722444307). Questo problema di convalida del back-end impediva la duplicazione delle attività all’interno della stessa area di lavoro. Questo problema è stato risolto e le attività possono essere copiate correttamente senza errori relativi al pubblico. (TGT-53717)
* **È stato risolto un problema che causava la visualizzazione di errori di input utente non validi per i tipi di pubblico per sola attività nelle attività [!UICONTROL Automated Personalization] e nel modale [!UICONTROL Manage Content].** Clienti hanno riscontrato errori di input utente non validi durante la configurazione dei tipi di pubblico per sola attività nella finestra modale [!UICONTROL  Manage Content] per le attività di Personalizzazione automatizzata. Questo problema si verificava nonostante il pubblico fosse stato precedentemente utilizzato correttamente. Le configurazioni del pubblico combinato ora vengono salvate correttamente senza attivare errori di convalida. (TGT-53749)

+++

**Documentazione**

+++Vedi i dettagli
* **Le pagine della documentazione di Web SDK specifiche di Target sono state spostate nell&#39;archivio Adobe Target.** Nell&#39;ambito della ristrutturazione della documentazione di Web SDK, il contenuto specifico di [!DNL Target] è stato migrato dai documenti generali di Web SDK alla [!DNL Adobe Target] [Guida per gli sviluppatori](https://experienceleague.adobe.com/en/docs/target-dev/developer/a4t/overview-a4t?lang=en){target=_blank}. Questa modifica migliora la reperibilità dei contenuti e garantisce che il team di prodotto appropriato mantenga le indicazioni specifiche per la soluzione. (TGT-53374)

+++

**[!UICONTROL Offer Decisions]**

+++Vedi i dettagli
* **L&#39;opzione Decisione offerta è ora visibile in modo coerente durante la creazione dell&#39;attività iniziale.** È stato risolto un problema nell&#39;interfaccia utente aggiornata a causa del quale l&#39;opzione [!UICONTROL Offer Decision] non veniva visualizzata durante il primo flusso di creazione per le attività A/B, in particolare quando si accedeva in modalità in incognito ai tenant con Decisioni di offerta abilitati. L&#39;opzione è stata visualizzata solo dopo essere passati al passaggio [!UICONTROL Targeting] e essere tornati a [!UICONTROL Experiences]. Questa correzione assicura che l&#39;opzione [!UICONTROL Offer Decision] sia immediatamente disponibile durante la configurazione iniziale, migliorando l&#39;usabilità e riducendo la confusione. (TGT-51888)

+++

**[!UICONTROL Offers]**

+++Vedi i dettagli
* **È stato risolto un problema a causa del quale le offerte di reindirizzamento non includevano `redirectOptions` nel payload quando `includeContent=true`.** Clienti che recuperavano offerte di reindirizzamento con `includeContent=true ` non avevano il campo `redirectOptions` nel payload di risposta. Questa incoerenza ha interessato i flussi di lavoro, ad esempio la copia delle offerte e la creazione di attività. Le offerte di reindirizzamento ora includono correttamente `redirectOptions` quando il contenuto viene richiesto. (TGT-53737)

+++

**[!DNL Recommendations]**

+++Vedi i dettagli
* **Tracciamento dei clic ripristinato per [!UICONTROL Recommendations] attività create nell&#39;interfaccia utente aggiornata.** È stato risolto un problema di tabulazione a causa del quale [!UICONTROL Recommendations] attività create nell&#39;interfaccia utente aggiornata non registravano il tracciamento dei clic, causando nessuna conversione segnalata. Le attività create nell’interfaccia utente legacy hanno tracciato correttamente i clic e segnalato le conversioni come previsto. Questa correzione assicura che le attività Consigli create nell’interfaccia utente aggiornata includano ora gli attributi di tracciamento corretti, il ripristino dei rapporti di conversione e l’allineamento con le metriche A4T. (TGT-53287)
* **Tracciamento dei clic ripristinato per le attività Consigli.** È stato risolto un problema che impediva alle attività [!UICONTROL Recommendations] create nell&#39;interfaccia utente aggiornata di registrare il tracciamento dei clic, causando la mancata segnalazione di conversioni. L&#39;interfaccia utente legacy ha applicato correttamente un ID di tracciamento (`at-track-click`) al contenuto [!UICONTROL Recommendations], mentre l&#39;interfaccia utente aggiornata ha inserito erroneamente un segnaposto (`__recsClickTrackIdPlaceholder__`), impedendo il tracciamento del back-end. Questa correzione assicura che il contenuto di [!DNL Recommendations] includa ora l&#39;ID di tracciamento corretto, ripristinando i rapporti di conversione e l&#39;allineamento con le metriche A4T. (TGT-53496)
* **Arresto anomalo dell&#39;editor della raccolta risolto nell&#39;interfaccia utente aggiornata.** È stato risolto un problema nell&#39;interfaccia utente [!UICONTROL Visual Experience Composer] (VEC) aggiornata a causa del quale l&#39;apertura di una raccolta dal pannello Editor causava l&#39;arresto anomalo della pagina con un errore di tipo: impossibile leggere le proprietà di non definito (lettura di &#39;customLocale&#39;). Questo errore si è verificato in più tipi di attività, inclusi [!UICONTROL Recommendations] e test A/B. (TGT-53703)
* **Opzione per rimuovere la raccolta selezionata ripristinata nel Compositore esperienza visivo.** È stato risolto un problema nel Compositore esperienza visivo a causa del quale gli utenti potevano sostituire solo una raccolta selezionata in un&#39;attività [!UICONTROL Recommendations], ma non potevano rimuoverla completamente. Questa limitazione bloccava i casi d’uso che richiedevano una rimozione pulita della raccolta senza sostituzione. Questa correzione introduce una chiara opzione per rimuovere la raccolta selezionata, consentendo una maggiore flessibilità nella configurazione delle attività e nell’allineamento con il comportamento precedente dell’interfaccia utente. (TGT-53652)
* **Le raccolte di criteri personalizzati ora vengono visualizzate correttamente nell&#39;interfaccia utente [!UICONTROL Recommendations].** È stato risolto un problema nell&#39;interfaccia Recommendations (Consigli) a causa del quale le raccolte create utilizzando criteri personalizzati non riuscivano a visualizzare i risultati del prodotto. Mentre le raccolte standard basate su attributi funzionavano come previsto, quelle che utilizzavano filtri personalizzati restituivano &quot;Nessun risultato trovato&quot; nonostante corrispondenze di catalogo valide. Questa correzione assicura che le raccolte che utilizzano attributi personalizzati ora vengano compilate correttamente nella scheda [!UICONTROL Product], ripristinando la funzionalità completa per i flussi di lavoro di consigli personalizzati. (TGT-53653)
* **È stato risolto un problema che impediva la visualizzazione dei prodotti nelle raccolte alla prima apertura della pagina [!UICONTROL Products].** I clienti che accedono alle raccolte nella sezione [!UICONTROL Recommendations] hanno riscontrato risultati di prodotto vuoti alla prima apertura della pagina [!UICONTROL Products]. Questo problema è stato causato da un errore di back-end nella query GraphQL, che non è riuscito a caricare i dati di prodotto per le raccolte con criteri personalizzati. Il problema è stato risolto e i prodotti ora vengono visualizzati correttamente senza la necessità di cambiare ambiente. (TGT-53694)
* **È stato risolto un problema che impediva la rimozione delle raccolte nelle attività [!UICONTROL Recommendations] basate su moduli.** I clienti che hanno creato [!UICONTROL Recommendations] attività utilizzando [!UICONTROL Form-Based Experience Composer] non hanno potuto deselezionare una raccolta scelta in precedenza. L’interfaccia utente richiedeva la selezione di una raccolta prima del salvataggio, impedendo agli utenti di ripristinare &quot;Tutte le raccolte&quot;. Questo comportamento è stato aggiornato per corrispondere alla funzionalità del Compositore esperienza visivo, consentendo ai clienti di salvare senza una raccolta selezionata e di impostare come predefinito &quot;Tutte le raccolte&quot;, come previsto. (TGT-53708)
* **È stato risolto un problema che impediva l&#39;impostazione delle promozioni per attributo a causa di valori mancanti per la raccolta o le regole di filtro.** I clienti che configurano promozioni per attributo nel processo di creazione attività hanno riscontrato un errore che indica che in una promozione manca un ID raccolta o valori di regole di filtro. Questo problema di convalida bloccava la progressione anche quando la configurazione sembrava completa. Le promozioni possono ora essere salvate correttamente se configurate per attributo. (TGT-53750)
* **È stato risolto un problema che impediva il salvataggio delle attività a causa di nomi di esperienza duplicati.** I clienti hanno riscontrato un errore di input utente non valido durante il salvataggio di attività che includevano combinazioni specifiche di criteri e progettazioni. L’errore è stato attivato da nomi di esperienza duplicati, anche quando la configurazione sembrava valida. È ora possibile salvare le attività con configurazioni distinte senza conflitti di denominazione. (TGT-53805)
* **È stato risolto un problema a causa del quale la convalida rimaneva non valida per le promozioni configurate dall&#39;attributo.** I clienti hanno riscontrato errori di convalida persistenti durante la configurazione delle promozioni per attributo nel processo di creazione attività, anche quando tutti i campi obbligatori erano compilati correttamente. Il problema è stato causato da una logica di convalida non corretta nel flusso di lavoro [!UICONTROL Recommendations]. Le promozioni basate su attributi ora vengono convalidate e salvate come previsto. (TGT-53811)
* **È stato risolto un problema a causa del quale l&#39;applicazione di una promozione a un&#39;attività live [!UICONTROL Recommendations] generava un errore.** I clienti hanno riscontrato l&#39;errore &quot;A Promotion is missing an Collection ID or filtering rule values&quot; durante il tentativo di applicare una promozione iniziale a un&#39;attività [!UICONTROL Recommendations] attiva, anche dopo aver fornito dettagli di configurazione validi. È ora possibile applicare le promozioni alle attività live senza attivare gli errori di convalida, garantendo un’esperienza più fluida nell’interfaccia utente aggiornata per la creazione delle attività. (TGT-53738)
* **È stato risolto un problema che impediva la visualizzazione dei prodotti nelle raccolte nell&#39;interfaccia utente di [!UICONTROL Recommendations].** clienti di un singolo tenant hanno segnalato che non è stato possibile caricare gli elenchi di prodotti durante la visualizzazione di alcune raccolte nella sezione [!UICONTROL Recommendations] della nuova interfaccia utente. Il problema è stato temporaneamente risolto cambiando gli ambienti, ma questa soluzione alternativa ha portato a una scarsa esperienza utente. Le entità prodotto ora vengono caricate in modo coerente senza richiedere l’attivazione dell’ambiente. (TGT-53783)
* **È stato risolto un problema a causa del quale i criteri e le progettazioni non venivano visualizzati su una riga nell&#39;interfaccia utente per la creazione di attività.** In precedenza, i criteri e le progettazioni nel processo di creazione attività venivano visualizzati in formato compresso, rendendo difficile per i clienti visualizzare e gestire singoli elementi. Ogni criterio e progettazione viene ora visualizzato sulla propria riga, migliorando la leggibilità e l’usabilità nell’interfaccia utente aggiornata. (TGT-53818)

+++

**Rapporti**

+++Vedi i dettagli
* La metrica **[!UICONTROL Total Revenue]è ora inclusa nelle esportazioni CSV dai rapporti attività.** È stato risolto un problema nell&#39;interfaccia utente aggiornata di [!UICONTROL Overview] a causa del quale i ricavi totali venivano visualizzati correttamente nella visualizzazione dei rapporti attività, ma non nell&#39;esportazione CSV, visualizzati come $0. Questa discrepanza ha impedito agli utenti di fare affidamento sui dati esportati per l’analisi e il reporting offline. (TGT-53325)
* La metrica **[!UICONTROL Total Sales]è ora inclusa nelle esportazioni CSV dai rapporti attività.** È stato risolto un problema nell&#39;interfaccia utente aggiornata a causa del quale la metrica [!UICONTROL Total Sales] veniva visualizzata correttamente nella vista dei rapporti attività ma non nell&#39;esportazione CSV. Questa discrepanza impediva agli utenti di accedere a dati completi sulle prestazioni nei rapporti scaricati. Questa correzione assicura che i valori [!UICONTROL Total Sales] vengano ora inclusi con precisione nelle esportazioni CSV, ripristinando la coerenza tra reporting in-app e analisi offline. (TGT-53330)
* **Messaggi di errore migliorati per [!UICONTROL Graph View] quando le metriche non sono abilitate.** È stato risolto un problema nel Compositore esperienza visivo a causa del quale [!UICONTROL Graph View] visualizzava un messaggio generico di tipo &quot;Si è verificato un errore&quot; quando una metrica richiesta non era abilitata nella suite di rapporti [!DNL Analytics] associata. Questo problema è stato attivato da un errore `not_enabled_metric` nella risposta GraphQL back-end. Questa correzione sostituisce il vago errore con un messaggio più informativo che aiuta gli utenti a identificare i problemi di configurazione in [!DNL Analytics], riducendo confusione e inutili escalation di supporto. (TGT-53577)
* **È stato risolto un problema a causa del quale la durata del report superava il limite supportato di 90 giorni.** I clienti che utilizzano il filtro &quot;[!UICONTROL Last X Days]&quot; nella sezione [!UICONTROL Reports] hanno potuto selezionare durate superiori a 90 giorni, il che potrebbe causare problemi di prestazioni e dati incompleti. Il filtro è stato aggiornato per applicare un intervallo massimo di 90 giorni, garantendo una generazione di rapporti coerente e affidabile. (TGT-53795)
* **È stato risolto un problema per cui i rapporti CSV delle prestazioni venivano generati utilizzando l&#39;ambiente predefinito invece di quello selezionato.** In precedenza, quando i clienti modificavano l&#39;ambiente nelle impostazioni dei rapporti e generavano un rapporto sulle prestazioni, il CSV risultante conteneva dati provenienti dall&#39;ambiente predefinito anziché da quello selezionato.  L&#39;interfaccia utente ora passa correttamente il parametro `environmentId`, assicurandosi che il rapporto rifletta l&#39;ambiente scelto. Inoltre, è stata migliorata la gestione degli errori. Se si verificano errori GraphQL durante la generazione del file CSV, l’interfaccia utente visualizza ora un messaggio di errore chiaro invece di produrre un file CSV vuoto. (TGT-53064)
* **È stato risolto un problema che impediva la visualizzazione dei dati in [!UICONTROL Graph View] da parte del reporting di Analytics for Target (A4T).I clienti** che utilizzano [!DNL Target] con integrazione A4T hanno riscontrato un errore di tipo &quot;Si è verificato un errore&quot; quando sono passati alla visualizzazione grafico nella scheda Reporting delle attività di test A/B. Anche se [!UICONTROL Table View] è stato caricato correttamente, [!UICONTROL Graph View] non è riuscito a eseguire il rendering delle tendenze della metrica nell&#39;intervallo di tempo selezionato. [!UICONTROL Graph View] visualizza ora i dati sulle prestazioni come previsto per tutte le metriche supportate, migliorando la visibilità e la precisione di reporting nell&#39;interfaccia utente aggiornata. (TGT-53573)

+++

**Compositore esperienza visivo**

+++Vedi i dettagli
* **I metadati degli elementi sono ora visibili al passaggio del mouse nel menu delle breadcrumb.** È stato migliorato il menu delle breadcrumb nel Compositore esperienza visivo per visualizzare ulteriori dettagli dell&#39;elemento come ID, classe e nome quando si passa il puntatore su un elemento. Questo miglioramento consente agli utenti di identificare e differenziare gli elementi più facilmente durante la configurazione dell’attività. (TGT-53409)
* **Il passaggio del cursore Breadcrumb evidenzia l&#39;elemento corrispondente nel Compositore esperienza visivo.** È stato migliorato [!UICONTROL Visual Experience Composer] per evidenziare l&#39;elemento corrispondente nell&#39;editor quando si passa il puntatore del mouse sugli elementi nel menu delle breadcrumb. Viene visualizzato anche il tipo di elemento, ad esempio contenitore, testo in grassetto o pulsante. Questo comportamento si applica agli elementi di pari livello ed esclude i tipi non supportati come SVG, in base all’elenco di convalida. (TGT-53411)
* **È stato ripristinato l&#39;avviso di modifiche non salvate nei flussi di lavoro di modifica del Compositore esperienza visivo.** È stato risolto un problema nel Compositore esperienza visivo a causa del quale gli utenti non venivano più informati delle modifiche non salvate apportate alle modifiche al codice personalizzato. A differenza dell’interfaccia utente legacy, nella nuova esperienza non sono presenti prompt quando si esce o si chiude l’editor di personalizzazione, con conseguente perdita accidentale di avanzamento. Con questa correzione vengono ripristinati gli avvisi per tutti i tipi di modifica, incluso il codice personalizzato, e viene garantito che gli utenti vengano avvisati prima di uscire senza salvare. (TGT-53435).
* **Le modifiche al codice personalizzato ora persistono durante l&#39;aggiornamento della pagina nel Compositore esperienza visivo.** È stato risolto un problema nel Compositore esperienza visivo a causa del quale le modifiche al codice personalizzato andavano perse durante gli aggiornamenti del sito Web. Questo problema si verificava su pagine con più ricaricamenti, causando la reimpostazione e il ripristino delle modifiche non salvate da parte dell’editor. La correzione assicura che le modifiche del codice personalizzato rimangano intatte anche se la pagina viene ricaricata durante la modifica, evitando la perdita accidentale di avanzamento. (TTGT-53501)
* **Problema di accesso risolto per l&#39;accesso al sito nel Compositore esperienza visivo.** È stato risolto un problema che impediva agli utenti di accedere al loro sito durante l&#39;accesso tramite il Compositore esperienza visivo. Il flusso di accesso reindirizzava ripetutamente gli utenti alla pagina di accesso, impedendo la configurazione e l’anteprima dell’attività. Questa correzione assicura che il Compositore esperienza visivo non interferisca più con il comportamento di accesso, ripristinando l’accesso previsto per gli utenti autenticati. (TGT-53524)
* **Problema di duplicazione dei cookie risolto nell&#39;estensione VEC Helper.** È stato risolto un problema a causa del quale l&#39;estensione [!UICONTROL Adobe Experience Cloud Visual Editing Helper] duplicava il cookie `at_qa_mode` durante il controllo qualità tramite collegamenti di anteprima. Quando si cambiavano manualmente gli indici di anteprima, venivano creati più cookie con valori in conflitto tra i domini, impedendo ai tester di cambiare in modo affidabile le varianti. Questo comportamento è stato osservato anche al di fuori dell’interfaccia utente di Target e ha interessato sia gli account interni che quelli client. Questa correzione assicura una gestione coerente dei cookie impedendo le voci duplicate e allineando l’ambito del dominio, consentendo un passaggio continuo delle varianti senza richiedere la pulizia manuale dei cookie. (TGT-53579)
* **È stato risolto un problema che causava perdite di memoria quando si facevano clic su elementi in una determinata pagina home.** I clienti che creano attività in questa home page hanno riscontrato perdite di memoria durante l&#39;interazione con gli elementi della pagina. Il problema era legato a un numero eccessivo di avvisi nella console e a un utilizzo crescente della memoria nei sottoframe, in particolare a causa di attributi di srcset non corretti. L’utilizzo della memoria rimane ora stabile durante l’interazione. (TGT-53761)
* **È stato risolto un problema che causava l&#39;arresto anomalo del Compositore esperienza visivo e la visualizzazione di una schermata vuota durante il caricamento di alcune attività.** clienti da un tenant specifico hanno segnalato che l&#39;editor non è riuscito a caricare attività specifiche. Il Compositore esperienza visivo rimaneva bloccato su &quot;Applicazione delle modifiche iniziali&quot; prima dell’arresto anomalo e della visualizzazione di una schermata vuota. Il Compositore esperienza visivo ora carica le attività interessate senza errori nel processo aggiornato di creazione delle attività. (TGT-52932)
* **È stato risolto un problema che causava la visualizzazione di etichette di posizione incoerenti nella barra [!UICONTROL Manage Content] delle attività [!UICONTROL Automated Personalization].** Clienti hanno segnalato che la barra [!UICONTROL Manage Content] mostrava numeri di posizione non corrispondenti nelle schede [!UICONTROL Experiences] e [!UICONTROL Offers]. (ad esempio, Posizione 2 e Posizione 4 in Esperienze e Posizione 1 e Posizione 2 in Offerta) anche quando erano configurate solo due posizioni. Le etichette di posizione ora sono coerenti e mappate con precisione alle modifiche, migliorando la chiarezza e l’usabilità nel processo di creazione delle attività. (TGT-52934)
* **È stato risolto un problema che causava la perdita di modifiche nel Compositore esperienza visivo dopo il salvataggio.** Clienti hanno segnalato che dopo il salvataggio di una modifica nel Compositore esperienza visivo, la pagina veniva aggiornata e ripristinata la versione precedente della modifica. Questo problema causava la perdita degli aggiornamenti più recenti a meno che l’intera attività non venisse salvata immediatamente. Le modifiche ora persistono correttamente dopo il salvataggio e l’editor non ripristina più le modifiche in modo imprevisto, garantendo un’esperienza affidabile nel flusso di lavoro per la creazione di attività. (TGT-53500)
* **È stata migliorata la selezione degli elementi nel Compositore esperienza visivo tramite la visualizzazione del tipo di elemento al passaggio del mouse e nella selezione.** Per migliorare l&#39;usabilità durante la creazione di attività, il Compositore esperienza visivo ora decora gli elementi HTML con il loro tipo quando passa il puntatore del mouse sopra di essi o quando questi sono selezionati. Questo miglioramento consente ai clienti di identificare e selezionare più facilmente gli elementi corretti. Gli elementi selezionati vengono evidenziati con un colore distinto e gli elementi al passaggio del mouse sono evidenziati in blu. Viene visualizzato anche il tipo di elemento, che fornisce un contesto più chiaro durante la modifica. (TGT-53502)

+++

## Aggiornamenti Datastream (19 settembre 2025)

La combinazione di ID e sandbox dello stream di dati deve essere univoca per [!DNL Adobe Target] connessioni di destinazione.

È stata aggiornata la logica di convalida per le connessioni di destinazione [!DNL Target] per fare in modo che la combinazione di ID dello stream di dati e nome della sandbox sia univoca all’interno di un’organizzazione IMS. Ciò significa che:

* Impossibile riutilizzare la stessa coppia ID dello stream di dati + nome sandbox in più connessioni di destinazione [!DNL Target].
* Lo stesso ID dello stream di dati può essere utilizzato per connessioni diverse solo se sono configurate in sandbox diverse.
* Questa regola si applica a tutte le selezioni dello stream di dati, anche quando si seleziona &quot;Nessuno&quot;.

Questo aggiornamento garantisce una configurazione coerente e impedisce conflitti tra ambienti con più sandbox. Per ulteriori informazioni, vedere [Connessione Adobe Target](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/personalization/adobe-target-connection){target=_blank} nella *Guida delle destinazioni Experience Platform*.

## [!DNL Target Standard/Premium] 25.9.1 (5 settembre 2025)

Questa versione include i seguenti aggiornamenti e correzioni:

**[!UICONTROL Experience Fragments]**

+++Vedi i dettagli
* **Attribuzione utente migliorata per le offerte [!UICONTROL AEM Experience Fragment].** È stato risolto un problema nel Compositore esperienza visivo in cui il campo &quot;[!UICONTROL Last updated]&quot; per le offerte [!UICONTROL AEM Experience Fragment] (XF) mostrava in modo errato un ID di codice invece del nome utente. Questa discrepanza si è verificata durante la selezione delle offerte nell’interfaccia utente aggiornata, creando un’incoerenza con l’interfaccia utente legacy e le offerte HTML, in cui veniva visualizzato correttamente il nome dell’ultimo editor. Questa correzione garantisce un’attribuzione utente coerente tra i tipi di offerta, migliorando la trasparenza e l’allineamento al comportamento previsto. (TGT-52880 e TGT-52898)

+++

**Offer Decisioning**

+++Vedi i dettagli
* **L&#39;errore di decisione dell&#39;offerta è stato risolto per le offerte ODE.** È stato risolto un problema a causa del quale le offerte ODE (Offer Decision Engine) inserite tramite [!DNL Target] restituivano un errore 400 a causa di metadati di formato mancanti. Il messaggio di errore indicava che il tipo MIME era nullo, impedendo l’elaborazione corretta delle decisioni sulle offerte. Questa correzione assicura la corretta gestione dei metadati dell’offerta, ripristinando la funzionalità per la distribuzione personalizzata dei contenuti e consentendo l’esecuzione ininterrotta delle campagne di marketing. (TGT-53635)
* **Problema di rendering dell&#39;offerta ODS risolto.** È stato risolto un problema che impediva il rendering delle offerte [!DNL Offer Decision Service] (ODS) create tramite [!DNL Adobe Journey Optimizer] (AJO) durante la generazione delle attività tramite il Compositore esperienza visivo nell&#39;interfaccia utente aggiornata. La stessa configurazione funzionava correttamente nell’interfaccia utente legacy, creando confusione e bloccando l’esecuzione della campagna. Questa correzione assicura la distribuzione coerente delle offerte in entrambe le versioni dell’interfaccia utente, ripristinando il comportamento previsto per la personalizzazione basata su AJO.

+++

**Rapporti**

+++Vedi i dettagli
* **Opzione Download ripristinata nella sezione dei report dell&#39;interfaccia utente aggiornata per la panoramica dei report.** È stato risolto un problema nella nuova interfaccia utente della panoramica a causa del quale il pulsante [!UICONTROL Download] non era presente nella sezione Rapporti, impedendo agli utenti di esportare i punteggi di importanza degli attributi. Questo aggiornamento ripristina la funzionalità di esportazione completa, consentendo un accesso semplificato ai dati scaricabili a scopo di analisi e reporting. (TGT-53222)
* Pulsante **[!UICONTROL Download full CSV report]ripristinato nella visualizzazione [!UICONTROL Important attributes].** È stato risolto un problema nell&#39;interfaccia utente aggiornata per la creazione di attività in cui il pulsante [!UICONTROL Download full CSV report] non era presente nella sezione [!UICONTROL Important Attributes] della visualizzazione Report. Questa correzione consente di ripristinare l’accesso alle informazioni scaricabili, garantendo funzionalità coerenti sia nell’interfaccia utente aggiornata che in quella legacy. (TGT-53238)
* **Sono stati risolti dei problemi relativi alla generazione di rapporti per [!UICONTROL Auto Target] nell&#39;interfaccia utente aggiornata della panoramica.** Sono stati risolti diversi problemi relativi all&#39;interfaccia utente nell&#39;interfaccia di panoramica aggiornata che interessavano il reporting delle attività di [!UICONTROL Auto Target]. Queste correzioni includono:

   * Metriche di incremento e affidabilità mancanti nei rapporti di riepilogo
   * Indicatore di colore errato per la casella di controllo &quot;Modelli generati&quot;
   * Rapporto grafico non funzionale nonostante la varianza dei dati in [!DNL Analytics]
   * Collegamento di download mancante per i report [!UICONTROL Automated Segments] e [!UICONTROL Important Attributes]
   * Visualizzazione report [!UICONTROL Automated Segments] interrotto

  Queste correzioni ripristinano il comportamento di reporting previsto e migliorano la visibilità delle prestazioni di [!UICONTROL Auto Target] nell&#39;interfaccia utente aggiornata. (TGT-53484)

+++

**[!UICONTROL Visual Experience Composer]**

+++Vedi i dettagli
* **La convalida del modulo è stata corretta per le condizioni di presenza dei parametri nell&#39;interfaccia utente aggiornata.** È stato risolto un problema nell&#39;interfaccia utente aggiornata in cui la selezione di &quot;[!UICONTROL Custom mbox parameter value is present]&quot; o &quot;[!UICONTROL Parameter is present]&quot; richiedeva erroneamente ai clienti di immettere un valore. Questo comportamento è in conflitto con la logica prevista, che si limita a verificare l’esistenza di un parametro indipendentemente dal suo valore. La correzione allinea la convalida del modulo al comportamento previsto, consentendo una configurazione dell’attività più fluida e supportando l’adozione completa dell’interfaccia utente aggiornata. (TGT-53638)
* **Logica del modulo corretta per le regole di presenza dei parametri nella consegna delle pagine.&quot;** È stato risolto un problema nell&#39;interfaccia utente aggiornata a causa del quale la selezione delle regole di consegna pagine come &quot;[!UICONTROL Parameter is present],&quot; &quot;[!UICONTROL Parameter is not present],&quot;[!UICONTROL Parameter value is present]&quot; o &quot;[!UICONTROL Parameter value is not present]&quot; richiedeva erroneamente agli utenti di immettere un valore di parametro aggiuntivo. Questo comportamento non era coerente con l’interfaccia utente legacy e contraddiceva la logica prevista di rilevamento della presenza di parametri senza specificare un valore. Questa correzione ripristina il comportamento di configurazione previsto delle regole, semplificando la configurazione delle attività e migliorando l’usabilità. (TGT-53640)
* **Logica di convalida migliorata per il generatore di regole con più pagine nell&#39;interfaccia utente aggiornata.** Sono stati risolti diversi problemi di convalida nel generatore di regole con più pagine nell&#39;interfaccia utente aggiornata. Queste correzioni includono:

   * Impedire la creazione di regole quando il parametro mbox è vuoto
   * Visualizzazione dei messaggi di errore appropriati per gli stati di regola non validi
   * Correzione della logica di convalida per gli operatori unari e basati su parametri che non richiedono valori di operando
   * Abilitazione delle regole dei frammenti hash con operatori unari ripristinando la funzionalità di salvataggio

  Questi aggiornamenti garantiscono una configurazione precisa delle regole e migliorano l’usabilità in scenari di consegna pagine complessi. (TGT-53722)
* **Problema di ridenominazione percorso risolto nelle attività A/B e MVT.** È stato corretto un bug nell&#39;interfaccia utente aggiornata a causa del quale la ridenominazione di un percorso in un&#39;attività [!UICONTROL A/B Test] o [!UICONTROL Multivariate Test] (MVT) non persisteva dopo la navigazione tra l&#39;elenco dei percorsi, il targeting e il back. Questo aggiornamento garantisce che le modifiche al nome della posizione vengano salvate e applicate in modo coerente in tutto il flusso di lavoro dell’attività. (TGT-52367)
* **È stata corretta la persistenza del nome della posizione per le attività MVT e AP nell&#39;interfaccia utente aggiornata.** È stato risolto un problema nell&#39;interfaccia utente aggiornata a causa del quale i nomi di percorso modificati nelle attività [!UICONTROL Multivariate Test] (MVT) e [!UICONTROL Automated Personalization] (AP) non venivano salvati correttamente. Dopo aver rinominato una posizione, lo spostamento tra le schede, ad esempio [!UICONTROL Targeting] e [!UICONTROL Experiences], ha ripristinato lo stato precedente dei nomi. Questa correzione assicura una denominazione della posizione coerente tra le schede e migliora l’affidabilità durante la configurazione dell’attività. (TGT-52927)
* **L&#39;etichettatura della posizione è stata corretta nel pannello Gestione esperienze per le attività MVT.** È stato risolto un problema nell&#39;interfaccia utente aggiornata a causa del quale il pannello [!UICONTROL Manage Experiences] nelle attività [!UICONTROL Multivariate Test] (MVT) mostrava una numerazione dei percorsi incoerente. Questa correzione assicura che le etichette di posizione siano sequenziali e correttamente allineate con le modifiche definite dall’utente, migliorando la chiarezza e l’usabilità durante la configurazione dell’esperienza. (TGT-52929)

+++

## Note aggiuntive e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=it) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js [!DNL Adobe Target]. |

## Modifiche alla documentazione, precedenti note sulla versione e note sulla versione di Experience Cloud

Per informazioni aggiuntive, oltre alle note di ciascuna versione, consulta le seguenti risorse:

| Risorsa | Dettagli |
|--- |--- |
| [Modifiche alla documentazione](/help/main/r-release-notes/doc-change.md) | Consulta le informazioni dettagliate sugli aggiornamenti di questa guida che non sono inclusi nelle presenti note sulla versione. |
| [Note sulla versione per le versioni precedenti](/help/main/r-release-notes/release-notes-for-previous-releases.md). | Informazioni su nuove funzionalità e miglioramenti introdotti nelle versioni precedenti di Target Standard e Target Premium. |
| [Note sulla versione di Adobe Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=it){target=_blank} | Ultime note sulla versione per le soluzioni Adobe Experience Cloud. |

## Informazioni in anteprima {#section_5D588F0415A2435B851A4D0113ACA3A0}

Le risorse seguenti contengono informazioni sulle funzionalità in arrivo con la prossima versione di Target.

| Risorsa | Dettagli |
|--- |--- |
| [Adobe Priority Product Update](https://www.adobe.com/subscription/priority-product-update.html){target=_blank} | Notifiche anticipate sui miglioramenti dei prodotti in arrivo per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud]. |
| [Note sulla versione di Target: prerelease](/help/main/r-release-notes/target-release-notes.md){target=_blank} | Informazioni sulle versioni di Target del mese corrente, incluse le informazioni prerelease. |
