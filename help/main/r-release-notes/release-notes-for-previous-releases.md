---
keywords: Note sulla versione;note sulla versione prerelease;miglioramenti futuri;correzioni future;funzioni future;prossima versione
description: Visualizza un elenco di funzioni, miglioramenti e correzioni inclusi nelle versioni precedenti di Adobe Target.
title: Quali funzioni sono incluse nelle versioni precedenti?
feature: Release Notes
exl-id: e4d261a1-d3aa-46ea-b1ce-efa76a90dc71
source-git-commit: 00c52d362f3d3a4f3bf9c90475dc8ad4c1f88311
workflow-type: tm+mt
source-wordcount: '48946'
ht-degree: 67%

---

# Note sulla versione per le versioni precedenti

Note sulle versioni precedenti di [!DNL Adobe Target], incluse le note di rilascio per [!DNL Target Standard/Premium], la piattaforma [!DNL Target] e le librerie JavaScript (at.js) di [!DNL Target].

Le note sulla versione vengono ordinate in ordine decrescente per mese e anno di rilascio.

>[!NOTE]
>
>Consulta [Note sulla versione di Target (corrente)](/help/main/r-release-notes/release-notes.md#reference_8FE40B43A5A34DDF8F26A53D55EE036A) per informazioni sulle versioni di Target del mese corrente (piattaforma e Target Standard/Premium).

## Note sulla versione - 2025

### [!DNL Target Standard/Premium] 25.7.4 (1 agosto 2025)

Questa versione risolve i problemi recenti, causati principalmente da complesse personalizzazioni dei clienti, e include le correzioni e i miglioramenti seguenti:

**Attività**

+++Vedi i dettagli
* È stato risolto un problema a causa del quale un cliente riscontrava un errore di tipo &quot;Input utente non valido&quot; durante il tentativo di salvare un’attività live, anche senza apportare modifiche. La risposta di GraphQL indica un problema LocalId duplicato. (TGT-53329, TGT-53373 e TGT-53195)
* È stato risolto un problema che impediva la creazione di un’esperienza di reindirizzamento nel Compositore esperienza visivo aggiornato. L’URL di reindirizzamento è stato ignorato ed è stata visualizzata la pagina originale. (TGT-53306)

+++

**Localizzazione**

+++Vedi i dettagli
* È stato risolto un problema di localizzazione nel modale [!UICONTROL Create Criteria] a causa del quale, quando si selezionava l&#39;opzione &quot;tra i seguenti valori&quot; nell&#39;elenco a discesa [!UICONTROL Choose Price Rule], la stringa &quot;to&quot; veniva slocalizzata nella sezione [!UICONTROL Inclusion Rules]. (TGT-49754)
* È stato risolto un problema di localizzazione con la stringa &quot;[!UICONTROL All host groups]&quot; nell&#39;elenco a discesa [!UICONTROL Environment] della procedura guidata di creazione dei feed non localizzata correttamente. (TGT-46737)

+++

**QA**

+++Vedi i dettagli
* È stato risolto un problema che impediva all’ambiente di controllo qualità di caricare i dati in più schede, rendendo l’interfaccia inutilizzabile. (TGT-53377)
* È stato risolto un problema che impediva la creazione di un’attività nell’ambiente di controllo qualità. Il processo è stato reindirizzato alla pagina [!UICONTROL Activities] invece di essere completato correttamente. (TGT-53328)

+++

**Raccomandazioni**

+++Vedi i dettagli
* È stato risolto un problema che causava l&#39;arresto anomalo della pagina quando si passava il mouse sull&#39;operando di &quot;apprendimento profondo&quot; durante la creazione di una raccolta in [!DNL Recommendations]. (TGT-53305)
* È stato risolto un problema a causa del quale i suggerimenti del filtro in [!UICONTROL Catalog Search] nell&#39;interfaccia utente aggiornata non erano accurati. (TGT-52007)
* È stato risolto un problema nell&#39;interfaccia utente [!DNL Recommendations] a causa del quale veniva visualizzato il filtro Operandi quando si utilizzavano gli operatori &quot;value is present&quot; (valore presente) o &quot;value is not present&quot; (valore non presente), anche se doveva essere nascosto. (TGT-53012)

+++

**Compositore esperienza visivo**

+++Vedi i dettagli
* È stato risolto un problema che si verificava quando un utente faceva clic su [!UICONTROL Manage Content] e poi su [!UICONTROL Done] durante la modifica di un&#39;attività di Automated Personalization (AP). La pagina restava vuota e non rispondeva. (TGT-53047 e TGT-52993)
* È stato risolto un problema che causava l&#39;arresto anomalo della pagina a causa della selezione della metrica di conversione [!UICONTROL Viewed an mbox] in [!UICONTROL Goals & Settings]. (TGT-53346, TGT-53343, TGT-53348)
* È stato risolto un problema che impediva alla funzionalità [!UICONTROL Redirect to URL] di funzionare come previsto, in quanto non si verificava alcun reindirizzamento anche con URL validi. (TGT-53307)

+++

**Aree di lavoro**

+++Vedi i dettagli
* È stato risolto un problema che si verificava durante la copia di attività tra aree di lavoro causava la duplicazione di voci &quot;Copia pubblico&quot; e conflitti di ID. I tipi di pubblico vengono ora copiati con ID univoci, contesto dell’area di lavoro e gestione ricorsiva per i tipi di pubblico combinati (fino a 5 livelli). (TGT-53081)
* È stato risolto un problema che si verificava se l&#39;area di lavoro era impostata su &quot;[!UICONTROL All Workspaces]&quot;. La copia di un&#39;attività già esistente nell&#39;area di lavoro predefinita generava un errore errato:

  &quot;È necessario includere almeno una proprietà per le aree di lavoro non predefinite.&quot;

  Poiché la copia si trova nell’area di lavoro predefinita, non è richiesta alcuna proprietà. Se si tenta di aggiungere una proprietà e salvare, viene generato un secondo errore:

  &quot;Input utente non valido&quot;

+++

### [!DNL Target Standard/Premium] 25.7.3 (venerdì 24 luglio 2025)

A causa dei problemi recenti identificati, principalmente correlati a complesse personalizzazioni dei clienti, questa versione include le correzioni e gli aggiornamenti seguenti:

**Attività**

+++Vedi i dettagli
* È stato risolto un problema a causa del quale il metodo `buildViews` nella classe del generatore impostava erroneamente `viewMaxLocalId` sul numero totale di visualizzazioni, anziché sul numero massimo di `viewLocalId` assegnate. (TGT-53207)
* È stato risolto un problema nell&#39;interfaccia utente [!DNL Target] aggiornata a causa del quale le offerte eliminate nelle attività [!UICONTROL Automated Personalization] (AP) venivano visualizzate come `Deleted option with ID: X` invece dei nomi originali (ad esempio, `Offer Name [Deleted]` come mostrato nell&#39;interfaccia utente legacy). Questa correzione ripristina un’etichettatura significativa per le offerte eliminate, migliorando la chiarezza e rendendo il reporting più preciso e intuitivo. (TGT-52921)
* È stato risolto un problema a causa del quale alcune attività migrate dal front-end [!DNL Target] a [!DNL Target] Central presentavano configurazioni di metriche incoerenti a causa di un bug di sincronizzazione precedentemente corretto. In particolare, le attività che originariamente utilizzavano una metrica di conversione e successivamente venivano aggiornate a una metrica basata su Analytics mantenevano valori obsoleti nei campi `primaryMetricType` e `successCriteria`. (TGT-52643)
* È stato risolto un problema che rendeva modificabile l&#39;intero contenuto di una pagina di anteprima Controllo di qualità a causa dell&#39;inclusione involontaria dell&#39;attributo `contentEditable` nelle modifiche di HTML. Questo consentiva agli utenti di fare clic e modificare qualsiasi testo nella pagina, causando potenzialmente problemi di layout e confusione durante il controllo qualità. (TGT-53247)
* È stato risolto un problema che causava la duplicazione della modifica spostando una modifica da [!DNL Page Load] a [!UICONTROL View], rimanendo in [!UICONTROL Page Load] e visualizzando anche in [!UICONTROL View]. Inoltre, la rimozione della modifica da [!UICONTROL View] la rimuoverebbe erroneamente anche da [!UICONTROL Page Load]. (TGT-53270)

+++

**API**

+++Vedi i dettagli
* È stato risolto un problema nel livello di persistenza back-end a causa del quale le opzioni eliminate venivano memorizzate correttamente ma non erano accessibili tramite gli endpoint API esistenti. Di conseguenza, le applicazioni front-end non sono state in grado di recuperare nomi significativi per le opzioni eliminate, influendo sulle visualizzazioni di reporting storiche. Questa correzione assicura che i dati delle opzioni eliminati conservati possano ora essere visualizzati correttamente nell’interfaccia utente. (TGT-52973)
* È stato implementato un nuovo endpoint di migrazione per supportare il trasferimento delle opzioni di attività eliminate dalle attività basate su JCR a [!DNL Target] Central. Questa funzionalità consente di eseguire il tracciamento e il reporting in modo coerente tra i sistemi. Questa funzione garantisce che le opzioni eliminate vengano mantenute e sincronizzate nel front-end e nel back-end di [!DNL Target], migliorando l&#39;integrità dei dati e dei report cronologici. (TGT-53217)
* È stato introdotto un nuovo endpoint API che consente agli utenti di ripristinare da un database secondario le opzioni delle attività precedentemente eliminate. Questa funzionalità sfrutta l&#39;infrastruttura esistente fornita dalle classi `RemovedCampaignElements` e `RemovedOptionInfo`, garantendo la perfetta reintegrazione delle opzioni eliminate nelle attività attive. (TGT-52903)
* È stato risolto un problema che impediva l&#39;apertura o la modifica di [!DNL Recommendations] attività contenenti nomi di metriche con più di 25 caratteri a causa di limitazioni API. Questa correzione assicura la compatibilità con i nomi delle metriche che superano il limite di caratteri, ripristinando l’accesso completo alle attività interessate. (TGT-52839)

+++

**Compositore esperienza basato su moduli**

+++Vedi i dettagli
* È stato risolto un problema in [!UICONTROL Form-Based Experience Composer] che causava l&#39;arresto anomalo dell&#39;editor dopo aver fatto clic sull&#39;icona **[!UICONTROL Manage Content]** ( ![icona Gestisci contenuto](/help/main/assets/icons/Experience.svg) ) durante la creazione o la modifica di un&#39;attività [!UICONTROL Automated Personalization] (AP). (TGT-53047)

+++

**Raccomandazioni**

+++Vedi i dettagli
* È stato risolto un problema che impediva a [!UICONTROL Catalog Search] di caricare risultati aggiuntivi durante lo scorrimento alla fine dell&#39;elenco, ripristinando un comportamento coerente con l&#39;interfaccia utente legacy. (TGT-53088)
* È stato risolto un problema che impediva l&#39;eliminazione di elementi dalla finestra di dialogo [!UICONTROL Criteria Details]. (TGT-53245)
* È stato risolto un problema che impediva l’apertura o l’interazione con prodotti senza nome. Questo problema si verificava durante la selezione di ambienti che restituivano risultati senza nome, impedendo l’accesso ai dettagli del prodotto. (TGT-53007)
* È stato risolto un problema che causava l&#39;arresto anomalo della pagina [!UICONTROL Catalog Search] e la visualizzazione di una schermata vuota durante la selezione di alcuni prodotti. (TGT-53087)
* È stato risolto un problema che impediva agli utenti di modificare l&#39;attività site_cart_z1 [!DNL Recommendation] nell&#39;interfaccia utente [!DNL Target]. Il tentativo di aprire l&#39;attività ha generato un errore nella pagina [!UICONTROL Overview], bloccando l&#39;accesso all&#39;editor. (TGT-53221)

+++

**Generazione di rapporti**

+++Vedi i dettagli
* È stato risolto un problema che impediva la cancellazione del campo sandbox nel database delle attività quando si cambiava l&#39;origine per la generazione di rapporti da [!DNL Customer Journey Analytics] o [!DNL Analytics] a [!DNL Target]. In precedenza, l’interfaccia utente inviava correttamente sandbox: null, ma il backend ignorava questo valore, lasciando sul posto i dati sandbox obsoleti. Il backend ora cancella correttamente il campo sandbox quando viene ricevuto null. (TGT-52798)
* È stato reimplementato il livello di persistenza delle opzioni eliminate nel backend di Target per supportare rapporti cronologici accurati nelle attività [!UICONTROL Automated Personalization] (AP). In precedenza, quando un’opzione veniva eliminata, il suo nome andava perso, rendendo difficile l’interpretazione dei dati sulle prestazioni passati.

  **Miglioramenti chiave**:

   * Le opzioni eliminate vengono ora tracciate utilizzando l&#39;infrastruttura esistente `RemovedCampaignElements` e `RemovedOptionInfo`.
   * Quando un’opzione viene rimossa da un’attività di Personalizzazione automatizzata, i relativi metadati (ad esempio, ID e nome) vengono mantenuti.
   * L&#39;interfaccia utente di reporting può ora visualizzare il nome dell&#39;opzione originale (ad esempio, `Option Name [Deleted]`) insieme alle metriche cronologiche, migliorando la chiarezza e l&#39;usabilità.

  Questo aggiornamento assicura rapporti coerenti e significativi, anche dopo la rimozione di opzioni da un’attività. (TGT-52986)

+++

**Compositore esperienza visivo**

+++Vedi i dettagli
* È stato risolto un problema nel Compositore esperienza visivo a causa del quale l’applicazione di una modifica a una visualizzazione causava la duplicazione e attivava un errore di tipo &quot;Input utente non valido&quot;. (TGT-52886)
* È stato risolto un problema con la funzionalità [!UICONTROL Undo] per le opzioni [!UICONTROL Insert Before] e [!UICONTROL Insert After] durante la configurazione delle offerte di immagini nel Compositore esperienza visivo.

  In precedenza, l&#39;annullamento di un&#39;azione [!UICONTROL Insert Before] o [!UICONTROL Insert After] sulle offerte di immagini causava un comportamento incoerente o il mancato ripristino corretto della modifica, in particolare nelle attività create nell&#39;interfaccia utente legacy di [!DNL Target]. Questo problema è stato risolto per garantire che le azioni di annullamento ora funzionino in modo affidabile per queste modifiche. (TGT-52809)

* È stato risolto un problema che causava l&#39;impostazione involontaria dell&#39;attributo `contentEditable` su true e persisteva nel contenuto HTML salvato. Questo aggiornamento garantisce un output HTML più pulito e atteso senza un comportamento di modifica non intenzionale. (TGT-52319)
* Per evitare la perdita permanente delle opzioni eliminate e garantire un comportamento coerente tra i servizi, è stata implementata la funzionalità di eliminazione temporanea per le opzioni nell’interfaccia utente e nei microservizi correlati.

  **Modifiche chiave**:

   * Le opzioni non vengono più eliminate definitivamente. Vengono invece contrassegnati con un nuovo flag eliminato: true nell&#39;oggetto XML dei parametri.
   * Questo flag viene utilizzato solo dall&#39;interfaccia utente [!DNL Target] aggiornata per escludere dal rendering le opzioni eliminate e per impedire che vengano inviate ai servizi Edge.
   * Le opzioni eliminate rimangono parte del payload dell’attività durante le modifiche, garantendo la tracciabilità ed evitando la consegna ai clienti di opzioni inesistenti.

  Questo aggiornamento migliora l’integrità dei dati e si allinea alle best practice per la gestione delle eliminazioni nei sistemi distribuiti. (TGT-52726)

+++

**Aree di lavoro**

+++Vedi i dettagli
* È stato risolto un problema che si verificava durante la copia di un’attività da un’area di lavoro non predefinita a quella predefinita o tra aree di lavoro non predefinite. Le offerte ora sono duplicate con funzioni avanzate di tracciamento e denominazione per evitare conflitti.

  **Miglioramenti chiave**:
   * Le offerte vengono ricreate nell’area di lavoro di destinazione con ID e metadati aggiornati.
   * Le offerte copiate vengono rinominate utilizzando il formato: &quot;Copia nome offerta&quot; più un numero casuale o una marca temporale per garantire l’univocità.
   * Il sistema aggiorna gli stati dell’offerta e dell’attività in modo da riflettere i nuovi ID.
   * Questa funzionalità evita gli errori causati da più nomi identici di &quot;Copia offerta&quot; durante le azioni di copia ripetute.
   * Le offerte potrebbero non essere visualizzate immediatamente nell’elenco delle offerte dell’area di lavoro di destinazione, ma vengono elaborate e visualizzate in modo appropriato.

  Questo aggiornamento migliora l’affidabilità e la tracciabilità durante la gestione delle offerte in più aree di lavoro. (TGT-53080)

+++

### [!DNL Target Standard/Premium] 25.7.2 (sabato 18 luglio 2025)

A causa dei problemi recenti identificati, principalmente correlati a complesse personalizzazioni dei clienti, questa versione include le correzioni e gli aggiornamenti seguenti:

**Attività**

+++Vedi i dettagli
* È stato aggiunto un ulteriore avviso di conferma durante l’annullamento delle modifiche dell’attività con modifiche non salvate: &quot;Desideri salvare questa attività? Se non esegui il salvataggio, tutte le modifiche andranno perse.&quot; Questo messaggio consente di evitare la perdita accidentale di dati. (TGT-52865)
* È stata ripristinata la funzionalità legacy nel cursore [!UICONTROL Priority] in [!UICONTROL Goals & Settings], consentendo ai clienti di immettere direttamente un valore numerico, come supportato nell&#39;interfaccia utente legacy. (TGT-53185 e TGT-53219)

+++

**Tipi di pubblico**

+++Vedi i dettagli
* È stato risolto un problema che impediva il salvataggio o la modifica di attività contenenti tipi di pubblico personalizzati. I clienti hanno riscontrato un messaggio di errore di tipo &quot;Impossibile completare la richiesta. Se il problema persiste, contattare [!DNL Adobe Client Care].&quot; quando si tenta di salvare le modifiche apportate a determinate attività, o anche se non le si salva. (TGT-53189)

+++

**[!UICONTROL Analytics for Target] (A4T)**

+++Vedi i dettagli
* È stato risolto un problema che si verificava quando i clienti visualizzavano i rapporti per attività specifiche sulla pagina [!UICONTROL Goals & Settings]. Il collegamento [!UICONTROL View in Analytics] puntava erroneamente all&#39;ambiente di controllo qualità invece che all&#39;ambiente di produzione. (TGT-53163)

+++

**[!UICONTROL Experiences]e[!UICONTROL Offers]**

+++Vedi i dettagli
* È stato risolto un problema che causava un ciclo infinito quando si richiamava `triggerView` tramite codice personalizzato. (TGT-52885)
* È stato risolto un problema che causava incongruenze tra `LocalIds` definiti per le attività e `LocalIds` utilizzati nelle definizioni delle esperienze. (TGT-52669)
* È stato risolto un problema a causa del quale nella pagina dell&#39;attività [!UICONTROL Overview] mancavano i nomi delle metriche, visualizzando solo &quot;Offerta&quot; invece del nome della metrica corretto. (TGT-53054)

+++

**Compositore esperienza basato su moduli**

+++Vedi i dettagli
* È stato risolto un problema in [!UICONTROL Form-Based Experience Composer] che impediva il salvataggio dell&#39;attività e attivava il messaggio di errore: &quot;Impossibile leggere le proprietà di non definito (lettura di &#39;map&#39;)&quot;. (TGT-53145)

+++

**Raccomandazioni**

+++Vedi i dettagli
* È stato risolto un problema che causava la visualizzazione dell&#39;errore &#39;Impossibile recuperare i dettagli del prodotto&#39; in seguito a un clic su un prodotto da [!UICONTROL Catalog Search], con l&#39;apertura di un modale senza un&#39;opzione di chiusura. (TGT-53082)
* È stato risolto un problema che impediva l&#39;aggiornamento corretto di [consigli come offerte](/help/main/c-recommendations/recommendations-as-an-offer.md) nelle attività [!UICONTROL A/B Test] durante la modifica di raccolte o promozioni. (TGT-52884)
* È stato risolto un problema nell’ambiente di produzione a causa del quale, facendo clic su un’entità nell’interfaccia utente aggiornata, veniva visualizzato l’errore: &quot;Impossibile recuperare i dettagli del prodotto. Se il problema persiste, contattare [!DNL Adobe Client Care].&quot; (TGT-53071)

+++

**Rapporti**

+++Vedi i dettagli
* È stato risolto un problema a causa del quale il salvataggio dei dettagli dell’ordine in un file CSV generava un file vuoto. (TGT-52225)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++Vedi i dettagli
* È stato risolto un problema sulla pagina [!UICONTROL Goals & Settings] a causa del quale i selettori utilizzati in più esperienze non venivano evidenziati in modo coerente come selezionati. (TGT-53062)
* È stato risolto un problema che impediva la modifica dell’attività e attivava il messaggio di errore: &quot;Impossibile leggere le proprietà di non definito (lettura di &quot;map&quot;)&quot;. (TGT-53161)

+++

**Aree di lavoro**

+++Vedi i dettagli
* È stata migliorata la gestione delle offerte ad hoc quando si passa da un’area di lavoro a un’altra.
   * Quando si passa dall’area di lavoro predefinita a un’area di lavoro non predefinita (o tra aree di lavoro non predefinite), le offerte ad hoc vengono ora copiate correttamente. Durante l’inizializzazione, il contesto dell’area di lavoro viene aggiornato e all’offerta viene assegnato un nuovo ID per garantirne l’univocità.
   * Non si verificano modifiche quando si rimane all’interno della stessa area di lavoro. (TGT-53079)
* È stato risolto un problema che impediva ai clienti di [copiare attività tra aree di lavoro diverse](/help/main/c-activities/edit-activity.md#section_45A92E1DD3934523B07E71EF90C4F8B6). (TGT-52753 e TGT-47094)
* È stato risolto un problema che si verificava durante la modifica delle proprietà tra le aree di lavoro.
   * Quando si passa dall&#39;area di lavoro predefinita a un&#39;area di lavoro non predefinita, se la proprietà corrente esiste nell&#39;area di lavoro di destinazione, la proprietà viene mantenuta.
   * Se nell&#39;elenco [!UICONTROL Properties] viene visualizzato un avviso (è probabile che alcune proprietà non siano compatibili) e il cliente fa clic su [!UICONTROL Add] o [!UICONTROL Remove] e quindi fa clic su [!UICONTROL Save], tutte le proprietà non presenti nell&#39;area di lavoro di destinazione verranno rimosse. Se il cliente fa clic su [!UICONTROL Cancel], tutte le proprietà rimangono, anche se non esistono nell&#39;area di lavoro di destinazione. (TGT-47094)
   * Se rimani nella stessa area di lavoro o passi da un’area di lavoro non predefinita a quella predefinita o a un’altra, tutto rimane invariato. (TGT-53078)
* È stata aggiornata la logica di convalida dell’entità in modo da rispettare il contesto dell’area di lavoro originale dell’attività. Entità come [!UICONTROL Experience Fragments] (XFs) ora vengono convalidate in base all&#39;area di lavoro in cui è stata originariamente creata l&#39;attività. Ad esempio, se nel workspace di default esiste un file XF e l&#39;attività viene copiata dal workspace X al workspace Y, la convalida viene comunque eseguita finché il file XF è valido nel workspace originale (predefinito). (TGT-53196)
* Supporto migliorato per la copia di tipi di pubblico ad hoc durante la duplicazione delle attività.
   * I tipi di pubblico ad hoc, tra cui metriche, rapporti, pagine e tipi di sola attività, vengono ora copiati automaticamente nei seguenti scenari:
      * Quando si copia un’attività dall’area di lavoro predefinita a un’area di lavoro non predefinita.
      * Quando copi un’attività all’interno della stessa area di lavoro. (TGT-53197)

+++

### [!DNL Target Standard/Premium] 25.7.1 (sabato 11 luglio 2025)

A causa dei problemi recenti identificati, principalmente correlati a complesse personalizzazioni dei clienti, questa versione include le correzioni e gli aggiornamenti seguenti:

**Attività**

+++Vedi i dettagli
* È stato risolto un problema a causa del quale l&#39;URL [!UICONTROL Activity QA] includeva un parametro di query non necessario: `at_preview_evaluate_as_true_audience_ids`. (TGT-52907)
* È stato risolto un problema a causa del quale gli URL di anteprima includevano erroneamente tipi di pubblico aggiuntivi oltre a quello esplicitamente digitato dall’utente. Questo comportamento è stato corretto per garantire che solo il pubblico specificato venga applicato durante la generazione di un collegamento di controllo qualità o di anteprima. (TGT-52912)
* È stato risolto un problema che impediva agli utenti di creare attività [!UICONTROL Auto-Target] (AT) se [!UICONTROL Auto-Allocate] (AA) era selezionato per primo durante la configurazione dell&#39;allocazione del traffico. Questo problema causava un errore di convalida del back-end e impediva il salvataggio dell’attività. (TGT-53096)

+++

**Tipi di pubblico**

+++Vedi i dettagli
* È stato risolto un problema che impediva agli utenti con il ruolo [!UICONTROL Approver] di aggiungere o salvare perfezionamenti del pubblico per sola attività. Il tentativo di eseguire questa operazione ha generato un errore 403 Forbidden, che indica che il privilegio &quot;[editor]&quot; è obbligatorio, anche se l&#39;utente dispone di autorizzazioni sufficienti per approvare e gestire le attività. (TGT-52984)
* È stato risolto un problema che si verificava quando un pubblico specifico per l&#39;attività veniva rimosso utilizzando l&#39;opzione [!UICONTROL Remove Audience Refinement] e il pubblico non veniva più visualizzato nell&#39;elenco dei tipi di pubblico per essere riselezionato all&#39;interno della stessa attività. Questo comportamento impediva agli utenti di aggiungere nuovamente lo stesso pubblico, a meno che non venga ricreato da zero. (TGT-52979)
* È stato risolto un problema a causa del quale i perfezionamenti del pubblico per sola attività scomparivano dall’interfaccia utente subito dopo essere stati rimossi da una posizione, anche prima del salvataggio dell’attività. Questo comportamento contraddiceva le funzionalità previste e le linee guida con la descrizione comando, che recita: &quot;Tutti i tipi di pubblico non utilizzati da questa libreria verranno eliminati una volta salvata l’attività&quot;. (TGT-52982)
* È stato risolto un problema che si verificava durante il tentativo di assegnare un pubblico diverso da [!UICONTROL All Visitors] a un&#39;attività. Al momento del salvataggio, veniva visualizzato il seguente messaggio di errore: &quot;Impossibile completare la richiesta. Se il problema persiste, contatta [!UICONTROL Adobe Client Care].&quot; (TGT-53008)
* È stato risolto un problema che impediva il salvataggio di un’attività dopo la creazione e l’assegnazione di un nuovo pubblico all’interno dell’editor attività. Il messaggio di errore visualizzato era: &quot;Impossibile completare la richiesta. Se il problema persiste, contattare [!UICONTROL Adobe Client Care].&quot; (TGT-52977)

+++

**[!UICONTROL Analytics for Target] (A4T)**

+++Vedi i dettagli
* È stato risolto un problema che causava un errore &quot;Input utente non valido&quot; durante la copia di un&#39;attività esistente e la modifica dell&#39;origine per la generazione di rapporti in [!DNL Adobe Analytics] (A4T). L&#39;errore è stato attivato quando alcune azioni di metrica incompatibili con il reporting di [!DNL Analytics], come `restart_same_experience`, `restart_random_experience` e `restart_new_experience`, sono state mantenute dall&#39;attività originale. (TGT-52900)
* È stato risolto un problema che impediva ai clienti di creare o salvare un&#39;attività selezionando [!DNL Adobe Analytics] (A4T) come origine per la generazione di rapporti nel passaggio [!UICONTROL Goals & Settings]. Il problema si è verificato in modo specifico quando si selezionava una metrica [!UICONTROL Custom Event] (ad esempio, &quot;Evento personalizzato 16&quot;), causando il seguente errore: &quot;Input utente non valido&quot;. (TGT-52910)
* È stato risolto un problema a causa del quale facendo clic sul collegamento &quot;[!UICONTROL View in Analytics]&quot; gli utenti venivano reindirizzati alla home page invece del dashboard [!DNL Analytics] desiderato. (TGT-53092 e TGT-53093)
  <!-- * Fixed an issue when cloning an existing activity and changing the reporting source from [!DNL Target] to [!DNL Adobe Analytics], users encounter a "400 - Invalid User Input" error, preventing the activity from being saved. (TGT-52875)-->
* È stato risolto un problema che si verificava durante la visualizzazione di un&#39;attività [!DNL Recommendations] nell&#39;interfaccia utente [!UICONTROL Overview] aggiornata. Impossibile caricare la sezione [!UICONTROL Goals & Settings] se [!DNL Adobe Analytics] (A4T) è selezionato come origine per la generazione di rapporti. Veniva visualizzato il seguente messaggio di errore: &quot;Si è verificato un errore. Impossibile completare la richiesta. Se il problema persiste, contatta l’Assistenza clienti Adobe.” (TGT-52999)

+++

**[!UICONTROL Experiences]e[!UICONTROL Offers]**

+++Vedi i dettagli
<!-- * Fixed an issue where using the [!UICONTROL Manage Content] feature in [!UICONTROL Automated Personalization] (AP) activities caused the page to crash and remain blank. This issue occurred after clicking [!UICONTROL Done] in the content manager, particularly in activities created or edited in the updated UI. (TGT-53047)-->
* È stato risolto un problema che impediva alla funzionalità [!UICONTROL Manage Content] di convalidare correttamente lo stato di una posizione dopo la rimozione di tutte le opzioni di contenuto. Questo problema poteva causare un comportamento incoerente o errori durante il tentativo di salvare o procedere con la configurazione dell’attività. (TGT-52801)
* È stato risolto un problema che causava la visualizzazione di un errore di tipo &quot;Input non valido&quot; durante l’aggiunta di una nuova pagina e l’eliminazione di elementi specifici in diverse esperienze. L&#39;errore viene attivato dalla generazione del duplicato `LocalIds` durante la manipolazione dell&#39;elemento, in particolare quando si passa da un&#39;esperienza all&#39;altra e si modificano le strutture di pagina condivise. (TGT-52720)
* È stato risolto un problema che causava la visualizzazione di posizioni non definite nel pannello [!UICONTROL Generate Adhoc Offer] da parte dell&#39;utilizzo della funzione [!UICONTROL Manage Content]. (TGT-53076 e TGT-53070)
* È stato chiarito il comportamento del cliente in cui le modifiche apportate utilizzando un&#39;offerta HTML potrebbero sembrare mancanti quando si torna dal passaggio [!UICONTROL Targeting] a [!UICONTROL Experiences]. Per questo cliente, il sito web interessato ha generato in modo dinamico più selettori DOM modificati a ogni caricamento di pagina. Di conseguenza, il selettore originariamente utilizzato per la modifica non viene trovato quando l’editor viene riaperto, causando la visualizzazione della modifica come mancante o non valida. Questo scenario funziona come previsto. Per garantire che le modifiche persistano visivamente nell’editor, si consiglia ai client di utilizzare selettori stabili e coerenti che non cambiano tra i ricaricamenti delle pagine. (TGT-52874)
* È stato risolto un problema a causa del quale il tentativo di eliminare o disattivare un’offerta che faceva parte di un’esperienza esclusa generava un errore di tipo &quot;Input utente non valido&quot;. Questo problema si verificava anche se l’offerta non veniva utilizzata attivamente nelle esperienze incluse. (TGT-52917)

+++

**Compositore esperienza basato su moduli**

+++Vedi i dettagli
* È stato risolto un problema nelle attività basate su moduli a causa del quale la duplicazione di un’esperienza e la modifica del codice personalizzato in una delle esperienze duplicate applicavano involontariamente tali modifiche a tutte le esperienze duplicate. Dopo la duplicazione, ora ogni esperienza conserva il proprio codice personalizzato in modo indipendente. (TGT-51600)

+++

**Localizzazione**

+++Vedi i dettagli
* Sono state aggiornate le stringhe di localizzazione nella nuova interfaccia utente per francese (fr_FR), tedesco (de_DE), italiano (it_IT), coreano (ko_KO) e cinese semplificato (zh_CN).

+++

**[!DNL Recommendations]**

+++Vedi i dettagli
* È stato aggiunto un nuovo feed [!DNL Recommendations] [status](/help/main/c-recommendations/c-products/feeds.md#status): [!UICONTROL Partial Import Failed]. (KB-2215)
* È stato risolto un problema che interessava il flusso di lavoro di creazione attività durante l&#39;aggiunta di [!DNL Recommendations] con [!UICONTROL promotions]. Quando gli utenti hanno selezionato &quot;[!UICONTROL Promote by Attribute]&quot; e aggiunto una regola di filtro (ad esempio, [!UICONTROL Parameter Matching]), il tipo di regola e i valori dell&#39;operando selezionati non sono stati mantenuti dopo il salvataggio e la modifica dell&#39;attività. Alla riapertura, il tipo di regola di filtro cambiava in modo imprevisto e mancavano i valori dell’operando. (TGT-53059)
* È stato risolto un problema nell&#39;interfaccia utente [!DNL Recommendations] a causa del quale qualsiasi promozione creata con una singola regola veniva erroneamente interpretata e visualizzata come un tipo di promozione &quot;Elenco di elementi&quot;, indipendentemente dalla logica della regola. (TGT-53063)
* È stato risolto un problema che si verificava durante l&#39;utilizzo dell&#39;interfaccia utente [!UICONTROL Overview] aggiornata. Il pulsante &quot;[!UICONTROL Download Recommendations Data]&quot; era mancante per le attività [!UICONTROL Experience Targeting] (XT) che includono [!DNL Recommendations]. (TGT-52730 e TGT-52756)
* In precedenza, nell’interfaccia utente Consigli veniva visualizzato solo il numero di entità importate correttamente da un feed. Tuttavia, il formato del messaggio di back-end include sia il numero di entità importate che il numero totale di entità nel formato: `# of entities imported / # of total entities`. A causa di questa discrepanza, gli utenti visualizzavano solo il primo valore (conteggio importato) nell’interfaccia utente, creando confusione. Ora l’interfaccia utente visualizza entrambi i numeri. (TGT-53073)
* È stato risolto un problema che impediva ai clienti di salvare una regola di filtro durante la configurazione di una promozione &quot;[!UICONTROL Promote by attribute]&quot; in un&#39;attività A/B basata su modulo con consigli. Dopo il salvataggio e la riapertura dell’attività, la regola di filtro risultava mancante e l’attività non poteva essere salvata correttamente. (TGT-53057)

+++

**Rapporti**

+++Vedi i dettagli
* È stato risolto un problema che causava il download di un file vuoto durante la selezione di &quot;[!UICONTROL Export order details to CSV]&quot; dalla pagina [!UICONTROL Reports]. Questo problema si verificava anche quando nell’attività erano presenti dati di ordine validi. (TGT-52225)
* È stato risolto un problema che si verificava durante il tentativo di salvare un’attività dopo la creazione e l’assegnazione di un nuovo pubblico di reportistica. Il messaggio di errore restituito era: &quot;Accesso negato. Per eseguire questa operazione, sono necessari tutti i privilegi seguenti: [editor].&quot; Questo problema si verificava nonostante l’utente avesse accesso a livello di approvatore. (TGT-53103)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++Vedi i dettagli
* È stato risolto un problema a causa del quale l’applicazione di una modifica a una vista determinava la duplicazione della vista e l’attività restituiva un errore di tipo &quot;Input utente non valido&quot;. Questa correzione assicura che le modifiche della visualizzazione vengano applicate correttamente senza causare errori di duplicazione o convalida. (TGT-52886)
* È stato risolto un problema che impediva la corretta visualizzazione delle modifiche al codice personalizzato in caso di esperienza errata. In particolare, le modifiche progettate per un’esperienza sono state mostrate in un’esperienza diversa, generando confusione e potenziale configurazione errata delle attività live. (TGT-52776)
* È stato risolto un problema che impediva la modifica o il salvataggio delle modifiche del codice personalizzato nella nuova interfaccia utente del Compositore esperienza visivo. In particolare:

   * Dopo aver modificato un blocco di codice personalizzato e aver salvato, le modifiche non venivano riportate nell’interfaccia utente o nell’anteprima Controllo qualità.
   * In alcuni casi, non è stato possibile eliminare le modifiche a meno che l’attività non sia stata chiusa e riaperta.
   * Come soluzione alternativa, gli utenti dovevano copiare il codice, eliminare la modifica e ricrearla manualmente con il contenuto aggiornato. (TGT-53072)

* È stato risolto un problema che causava la mancata risposta del pannello [!UICONTROL Modifications] a causa della modifica e del salvataggio del codice personalizzato. (TGT-53075)
* È stato risolto un problema a causa del quale le modifiche apportate al codice personalizzato nelle esperienze di varianti venivano applicate involontariamente all&#39;esperienza [!UICONTROL Control]. Questo causava modifiche non intenzionali nel comportamento di consegna. L&#39;esperienza [!UICONTROL Control] ora rimane isolata dalle modifiche al codice personalizzato apportate ad altre esperienze. (TGT-52413)
* È stato risolto un problema a causa del quale le modifiche apportate a un’esperienza (ad esempio, Esperienza B) venivano duplicate involontariamente a un’altra esperienza (Esperienza A) se l’utente faceva clic sulla seconda esperienza prima del caricamento completo dell’editor. Questo comportamento potrebbe anche causare la perdita di modifiche se l’esperienza selezionata inizialmente non avesse subito modifiche. (TGT-52597)
* È stato risolto un problema per cui le modifiche apportate nel passaggio [!UICONTROL Modifications] della creazione dell&#39;attività non venivano salvate in modo coerente. In alcuni casi, dopo aver completato tutti i passaggi e aver fatto clic su [!UICONTROL Save], lo script personalizzato aggiunto nella sezione [!UICONTROL Modifications] non si rifletterebbe sul sito live, nonostante nessun errore visibile durante il processo di salvataggio. (TGT-52661)
* È stato risolto un problema a causa del quale le modifiche al codice personalizzato non venivano salvate correttamente e venivano involontariamente applicate a più esperienze all’interno della stessa attività. Inoltre, si sono verificati problemi di accesso all’apertura o all’aggiornamento di alcune attività, con la conseguente visualizzazione di schermate vuote. Questi problemi sono stati risolti per garantire una modifica stabile delle attività e un isolamento accurato delle esperienze. (TGT-52594)
* È stato risolto un problema che impediva agli utenti di passare a un URL diverso in [!UICONTROL Browse Mode]. Ciò impediva ai tester e agli editor di convalidare o visualizzare in anteprima pagine alternative all’interno della stessa sessione di attività. (TGT-53052)
* È stato risolto un problema che causava l&#39;apertura simultanea di più istanze di [!UICONTROL Visual Experience Composer] (VEC) durante la creazione dell&#39;attività. Questo problema si verificava quando gli utenti disabilitavano [!UICONTROL Enhanced Experience Composer] (EEC) e rimuovevano la barra finale dall&#39;URL del sito Web nel passaggio [!UICONTROL Page Delivery]. (TGT-52782)
* È stato risolto un problema a causa del quale il menu a discesa della metrica [!UICONTROL Revenue] nel passaggio [!UICONTROL Goals & Settings] impostava erroneamente il valore predefinito [!UICONTROL Revenue per Visit] (RPVISIT), anche dopo che l&#39;utente aveva selezionato una metrica diversa.  Il problema si verificava durante la compressione e la nuova espansione del pannello di configurazione della metrica, causando il ripristino del valore selezionato in precedenza. (TGT-52811 e TGT-52878)
* Sono stati risolti diversi problemi nel flusso di lavoro di creazione attività relativi alla denominazione delle offerte e alla traduzione dei contenuti in [!UICONTROL Automated Personalization] (AP) e [!UICONTROL Multivariate Testing] (MVT) attività:

  Problemi chiave risolti:

   * La creazione di più offerte HTML con lo stesso nome (ad esempio, &quot;Esperienza&quot;) ha attivato l’errore &quot;I nomi di offerta duplicati non sono consentiti&quot;, ma l’interfaccia utente non indicava chiaramente quali offerte causavano il conflitto.
   * La ridenominazione delle offerte tramite il pannello di destra ha aggiornato il nome nell&#39;interfaccia utente, ma la modifica non è stata riportata nella scheda [!UICONTROL Manage Content] o nella scheda [!UICONTROL Offers], causando errori di convalida persistenti.
   * Nelle attività MVT, anche se l’errore di nome duplicato non persisteva dopo la ridenominazione, l’interfaccia utente non riusciva ancora a riflettere i nomi delle offerte aggiornati in modo coerente tra le schede. (TGT-52933)

+++

### [!DNL Target Standard/Premium] 25.6.4 (sabato 27 giugno 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* Opzione [!UICONTROL Rearrange] aggiunta all&#39;interfaccia utente [!UICONTROL Visual Experience Composer] (VEC) aggiornata per allinearla alle funzionalità disponibili nel Compositore esperienza visivo legacy. (TGT-46957 e TGT-52876)
* È stato risolto un problema che impediva il mantenimento delle modifiche apportate alle esperienze di varianti (ad esempio, Esperienza B) in un&#39;attività [!UICONTROL A/B Test]. Dopo il passaggio da un’esperienza all’altra, le modifiche apportate alla variante scompaiono. Questo problema non ha influito sull’esperienza di controllo. (TGT-52664)
* È stato risolto un problema che impediva ad alcuni clienti di creare o salvare attività, mentre altri potevano eseguire le stesse azioni senza alcun problema. Il problema era incoerente tra gli account.(TGT-52842)
* È stato risolto un problema che impediva agli utenti del Compositore esperienza visivo aggiornato di spostare le modifiche a [!UICONTROL Page Load event], una funzionalità già presente nell&#39;interfaccia utente legacy. (TGT-52617)
* È stato risolto un problema nell&#39;interfaccia utente aggiornata a causa del quale gli eventi [!UICONTROL page load] non erano visibili in [!DNL Target] durante la creazione delle modifiche; gli aggiornamenti sono stati applicati solo alle visualizzazioni. (TGT-52604)
* È stato risolto un problema che impediva la corretta visualizzazione di alcune modifiche dell’attività nel Compositore esperienza visivo aggiornato. (TGT-52818)
* È stata corretta un&#39;eccezione Null Pointer che si verificava durante il recupero dei dati di reporting per le attività di [!UICONTROL Automated Personalization] (AP). (TGT-52362)
* È stato risolto un problema che impediva la visualizzazione dei dettagli a livello di offerta nel file .CSV per le attività [!UICONTROL Automated Personalization] (AP). (TGT-52675)
* È stato risolto un problema che si verificava durante l’applicazione di modifiche nel Compositore esperienza visivo aggiornato, a causa del quale le modifiche inizialmente venivano visualizzate correttamente, incluso il [!UICONTROL Experience Fragment] previsto. Tuttavia, quando si passa da un’esperienza all’altra o si apportano ulteriori modifiche, alcune modifiche non vengono applicate a causa di problemi del selettore. (TGT-52679)
* È stato risolto un problema a causa del quale, quando veniva creata una nuova attività clonandone una esistente, i collegamenti di controllo qualità nell’attività clonata mantenevano erroneamente gli URL della pagina dall’attività originale. (TGT-52775)
* È stato risolto un problema che impediva involontariamente a [!UICONTROL On-device Decisioning] di essere disponibile nel Compositore esperienza visivo aggiornato. (TGT-52371)
* È stato risolto un problema che impediva la modifica di un&#39;attività di prodotto [!DNL Recommendations]. Quando si tenta di accedere al Compositore esperienza visivo tramite l’interfaccia utente di Target, nella pagina [!UICONTROL Overview] viene visualizzato un errore che impedisce eventuali modifiche. (TGT-52823)
* È stato risolto un problema che impediva il salvataggio di un&#39;attività [!DNL Recommendations] quando i nomi delle esperienze superavano i 50 caratteri. (TGT-52619)
* È stato risolto un problema che impediva ai clienti di salvare un’attività Consigli dopo la modifica dei criteri nella nuova interfaccia utente. Il problema sembra essere relativo alle autorizzazioni e non influisce su tutti gli utenti con ruoli simili. (TGT-52816)
* È stato risolto un problema che impediva agli utenti con la mansione [!UICONTROL Editor] di modificare un&#39;attività [!DNL Recommendations]. Il tentativo di modificare la progettazione e salvare l&#39;attività ha restituito un errore 403 Forbidden, che indica che il privilegio &quot;[editor]&quot; era obbligatorio, anche se l&#39;utente aveva già quel ruolo nell&#39;area di lavoro pertinente. (TGT-52836)

### [!DNL Target Standard/Premium] 25.6.3 (sabato 20 giugno 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema a causa del quale la copia di un’attività da un’area di lavoro a un’altra causava errori quali &quot;non deve essere null&quot; o &quot;Si è verificato un errore&quot;. (TGT-52474)
* È stato risolto un problema che impediva la generazione di rapporti [!UICONTROL Automated Segments] e [!UICONTROL Important Attributes] per alcune attività. (TGT-52904)
* È stato risolto un problema nel Compositore esperienza visivo aggiornato a causa del quale la gestione del contenuto predefinito nelle attività di [!UICONTROL Automated Personalization] (AP) non corrispondeva all&#39;interfaccia utente legacy. Il sistema ora aggiunge automaticamente un `optionGroup` predefinito denominato &quot;Contenuto predefinito&quot; con `optionGroupLocalId = 0` quando nessun gruppo viene aggiunto in modo esplicito. Questo gruppo include l&#39;opzione predefinita, ad esempio `optionLocalId: 0`. Se il contenuto predefinito viene rimosso, viene rimosso anche il gruppo di opzioni corrispondente. (TGT-52651)
* È stato risolto un problema nelle attività [!UICONTROL Multivariate Test] (MVT) a causa del quale il riutilizzo di un `experienceLocalId` da esperienze precedentemente rimosse non era consentito correttamente. (TGT-52672)
* È stato risolto un problema che impediva la copia o la modifica delle attività contenenti un frammento di esperienza. Questo ha attivato l&#39;errore: `Enum "AemOfferType" cannot represent value: "html"`. (TGT-52635)
* È stato risolto un problema che impediva agli URL nei percorsi di attività di visualizzare i parametri di query a causa di caratteri non validi, ad esempio barre (/). (TNT52845)
* È stato migliorato il messaggio di errore di convalida per gli aggiornamenti dell&#39;attività [!DNL A/B Test] tramite l&#39;API di back-end. Quando sono presenti nomi di posizione duplicati, il messaggio ora indica chiaramente: &quot;I nomi duplicati non sono consentiti&quot; per `locations.selectors`. (TGT-52589)
* È stato corretto un errore che si verificava durante l&#39;aggiornamento di un&#39;attività live [!UICONTROL Recommendations] a causa di una proprietà non riconosciuta nel payload della richiesta. Il sistema ora gestisce correttamente il codice JSON &quot;Non valido&quot;. Errore &quot;Nome proprietà non riconosciuto&quot;. (TGT-52723)
* È stato risolto un problema che impediva la creazione di una progettazione [!DNL Recommendations]. Facendo clic su [!UICONTROL Create] è stato attivato il messaggio: &quot;Deve essere utilizzata almeno 1 variabile di entità nello script&quot;. (TGT-52395 e TGT-52899)
* È stato risolto un problema che impediva il salvataggio di una progettazione [!DNL Recommendations] senza modifiche. (TGT-52879)
* È stato corretto un errore di convalida del back-end che causava un errore &quot;400 Bad Request&quot; durante il salvataggio di un&#39;attività [!UICONTROL Recommendations]. (TGT-52716)
* È stato risolto un problema in [!UICONTROL Form-Based Experience Composer] a causa del quale il passaggio del mouse su una mbox con caratteri speciali nel menu a discesa [!UICONTROL Location] causava la visualizzazione di un valore vuoto dell&#39;editor e causava l&#39;attivazione di un messaggio di tipo &quot;Impossibile eseguire &#39;querySelector&#39; su &#39;Element&#39;.&quot; errore. (TGT-52717)
* È stata migliorata la precisione dello stato di avanzamento con un nuovo indicatore &quot;PARTIALLY_IMPORTED&quot;. In precedenza, i feed venivano contrassegnati come &quot;riusciti&quot; anche quando non venivano importate tutte le righe di un file, il che era fuorviante. (TGT-52892)
* È stato corretto un errore a causa del quale, dopo la migrazione ad AP V2, alcune chiamate API a `/admin/rest/ui/v1/campaigns` restituivano errori lato client (HTTP 4xx). (TGT-52721)

### [!DNL Target Standard/Premium] 25.6.2 (venerdì 12 giugno 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato aggiunto un [nuovo articolo di domande frequenti](/help/main/c-intro/updated-ui-faq.md) per risolvere le domande comuni sull&#39;interfaccia utente [!DNL Target] e sul Compositore esperienza visivo aggiornati di [!UICONTROL Visual Experience Composer].
* È stato risolto un problema che impediva il funzionamento della regola &quot;[!UICONTROL URL - does not contain]&quot; in [!UICONTROL Page Delivery], consentendo la visualizzazione del contenuto anche quando avrebbe dovuto essere bloccato. (TGT-52754)
* È stato risolto un problema che impediva a [!UICONTROL Page Delivery] di visualizzare correttamente il messaggio di errore: &quot;Non sono consentiti URL di pagina duplicati. (TGT-52765)
* È stato risolto un problema a causa del quale i tipi di pubblico per [!UICONTROL Page Delivery] URL contenenti frammenti di esperienza venivano creati con # erroneamente aggiunto. (TGT-52786)
* È stato risolto un problema che causava la mancata risposta dell&#39;interfaccia utente di [!UICONTROL Goals and Settings] a causa della copia di un&#39;attività e della modifica delle impostazioni nella pagina [!DNL Target]. (TGT-52797)
* È stato risolto un problema nel Compositore esperienza visivo [!UICONTROL Visual Experience Composer] aggiornato che consentiva erroneamente il reindirizzamento di una pagina aggiuntiva in un&#39;attività [!UICONTROL A/B Test] allo stesso URL. (TGT-51838)
* È stato risolto un problema che impediva il salvataggio delle modifiche alle metriche nella pagina [!UICONTROL Goals and Settings] durante la modifica di un&#39;attività. (TGT-52799)
* È stato risolto un problema a causa del quale l’aggiunta di una nuova esperienza durante il caricamento dell’editor web causava la duplicazione del contenuto dell’esperienza precedente. (TGT-51397)
* È stata ripristinata la possibilità di utilizzare codice personalizzato all&#39;esterno del tag `<head>`, una funzione precedentemente disponibile nell&#39;interfaccia utente di Target precedente. (TGT-52304 e TGT-52300)
* È stata rimossa la convalida non necessaria durante la selezione dell’area di lavoro predefinita durante la creazione dell’attività. La convalida obbligatoria delle proprietà non si applica più all’area di lavoro predefinita, ma rimane attiva per le aree di lavoro non predefinite. (TGT-52449)
* È stato risolto un problema nel Compositore esperienza visivo [!UICONTROL Visual Experience Composer] aggiornato a causa del quale non venivano rilevate `triggerView()` chiamate. (TGT-52575)
* È stato risolto un problema nel Compositore esperienza visivo [!UICONTROL Visual Experience Composer] aggiornato che impediva agli utenti di aggiungere modifiche alle visualizzazioni di [!UICONTROL Single Page Application] (SPA). (TGT-52556)
* È stato risolto un problema nell&#39;interfaccia utente [!DNL Target] aggiornata che impediva ai clienti di visualizzare i dettagli delle offerte. (TGT-52607)
* È stato risolto un problema che impediva agli aggiornamenti apportati alle offerte in [!UICONTROL Offers Library] di trovarsi nel [!UICONTROL Visual Experience Composer] (Compositore esperienza visivo) aggiornato. (TGT-52637)
* È stato risolto un problema che impediva la corretta visualizzazione della sezione Offerte durante la creazione di un’attività. (TGT-52773)
* È stata aggiunta la convalida per garantire che tutti i `optionLocalIds` a cui si fa riferimento in `optionGroups` siano presenti nell&#39;array delle opzioni. I riferimenti non validi vengono rimossi automaticamente durante la creazione dell’attività. (TGT-52687)
* È stato risolto un problema a causa del quale i gruppi di reporting e le esclusioni non venivano mantenuti dopo l’aggiunta di una nuova offerta. (TGT-52728)
* È stato risolto un problema che causava la visualizzazione di un selettore di opzioni vuoto nelle attività senza un pulsante [!UICONTROL Activity QA]. (TGT-52733)
* È stato risolto un problema che impediva il corretto rendering del contenuto dei collegamenti di controllo qualità. (TGT-52718)
* È stato risolto un problema a causa del quale la sostituzione di un elemento con un frammento di esperienza non rifletteva correttamente le modifiche nell’ambiente di controllo qualità. (TGT-52762)
* È stato risolto un problema nel Compositore esperienza visivo [!UICONTROL Visual Experience Composer] aggiornato che causava un errore di tipo &quot;Input non valido&quot; quando gli utenti tentavano di aggiungere frammenti di esperienza. (TGT-52701)
* È stato risolto un problema che causava la visualizzazione del modale &quot;Modifica pubblico&quot; vuoto durante la modifica del targeting del pubblico nel [!UICONTROL Visual Experience Composer] (VEC) aggiornato. (TGT-52749)
* È stato aggiunto un messaggio per informare gli utenti quando un’entità non è accessibile nell’area di lavoro selezionata. (TGT-52767)
* È stato risolto un problema che impediva all’interfaccia utente di consentire l’assegnazione manuale di un ID ambiente a un criterio. Viene invece utilizzato l&#39;ID predefinito per il gruppo host [!UICONTROL Product Catalog Search]. Questa correzione assicura che le modifiche ai criteri vengano ora applicate in tutti gli ambienti, non solo a quello predefinito. (TGT-52817)
* È stato risolto un problema che causava l&#39;assenza dell&#39;opzione &quot;[!UICONTROL Download Recommendations data]&quot; per le attività [!UICONTROL Experience Targeting] (XT) con consigli. (TGT-52730 e TGT-52756)

### [!DNL Target Standard/Premium] 25.6.1 (sabato 6 giugno 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema a causa del quale i collegamenti di controllo qualità non fornivano l’esperienza corretta per l’attività associata. (TGT-52163 e TGT-52790)
* È stato risolto un problema che causava la mancanza dell’ID del pubblico associato nei collegamenti di controllo qualità. (TGT-52722)
* È stato risolto un problema per garantire che le esperienze vengano consegnate solo quando le condizioni URL di consegna pagina configurate vengono soddisfatte con precisione. (TGT-52696)
* È stato risolto un problema che impediva ai clienti di creare un modello struttura [!DNL Recommendations]. Il tentativo di creare un modello ha attivato l’errore: &quot;Deve essere utilizzata almeno 1 variabile di entità nello script&quot;. (TGT-52395)
* È stato risolto un problema che impediva il salvataggio delle progettazioni di [!DNL Recommendations] tramite gli array Velocity. Il messaggio di errore &quot;Deve essere utilizzata almeno 1 variabile di entità nello script&quot; è stato attivato in modo errato. (TGT-52734)
* È stato risolto un problema che impediva l&#39;accesso alle modifiche nel [!UICONTROL Visual Experience Composer] (VEC) quando non era possibile caricare la pagina per le pagine Web interne. (TGT-52488 &amp;TGT-52470)
* È stato risolto un problema che impediva la visualizzazione del pannello [!UICONTROL Modifications] nel Compositore esperienza visivo con schermi di dimensioni inferiori. (TGT-52470)
* È stato risolto un problema nel Compositore esperienza visivo aggiornato a causa del quale il passaggio dalla modalità [!UICONTROL Browse] alla modalità [!UICONTROL Design] causava un errore della console e impediva ulteriori interazioni. (TGT-52532)
* È stato risolto un problema nel Compositore esperienza visivo a causa del quale, facendo clic su alcuni elementi, le dimensioni venivano involontariamente estese. (TGT-52497)
* È stato risolto un problema che impediva il caricamento o il riconoscimento di alcuni elementi di pagina nel Compositore esperienza visivo, impedendo interazioni quali la selezione di pulsanti o banner e l’interruzione del tracciamento accurato degli eventi nelle attività. (TGT-52663)
* È stato risolto un problema che impediva ai clienti di eliminare o rimuovere le offerte nelle attività [!UICONTROL Automated Personalization] (AP). (TGT-52690)
* È stato risolto un problema che causava un comportamento incoerente di qualificazione delle attività nelle attività multipagina. (TGT-52694)
* È stato risolto un problema che causava la visualizzazione di un URL non valido per la pagina [!UICONTROL Overview] dell&#39;attività. [!UICONTROL Activity Location] (TGT-52695)
* È stato risolto un problema nell&#39;interfaccia utente [!DNL Target] aggiornata che causava la visualizzazione di voci duplicate per i percorsi attività. (TGT-52693)
* È stato risolto un problema che attivava un errore `getAudiencesV3`, impedendo ai clienti di modificare o copiare le attività. (TGT-52709)
* È stato risolto un problema che causava un errore di payload non valido durante l&#39;aggiunta di [!UICONTROL Experience Fragments] o offerte HTML a un&#39;attività. (TGT-52779 e TGT-52773)
* È stato risolto un problema nell&#39;interfaccia utente [!DNL Target] aggiornata a causa del quale E[!UICONTROL xperience Fragments] non veniva visualizzato correttamente a causa di un errore di input non valido. (TGT-52701)
* È stato risolto un problema che impediva ai clienti di modificare le attività in [!UICONTROL Form-based Experience Composer] a causa di un errore utente non valido. (TGT-52470)
* È stato risolto un problema di localizzazione nella lingua coreana a causa del quale le traduzioni precedenti utilizzavano caratteri al di fuori del piano multilingue di base. La traduzione aggiornata utilizza caratteri appropriati che trasmettono con precisione il significato previsto. (TGT-52508 e TGT-52509)
* È stato risolto un problema di localizzazione nella lingua coreana a causa del quale la traduzione di &quot;date&quot; risultava incoerente quando si selezionavano le date di inizio e di fine per un’attività. (TGT-52510)

### [!DNL Target Standard/Premium] 25.5.4 (29 maggio 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema che impediva l’aggiunta o la modifica di URL in modalità di controllo qualità. (TGT-51941)
* È stata aggiunta un&#39;impostazione di traffico in modalità Controllo di qualità in [!UICONTROL Reports] > [!UICONTROL Report Settings] ( ![icona Impostazioni report](/help/main/assets/icons/Setting.svg) ) per allinearla alle funzionalità dell&#39;interfaccia utente legacy di [!DNL Target]. (TGT-52228 e TGT-52329)
* È stato risolto un problema che causava la generazione di collegamenti di controllo qualità errati da parte dell’attività basata su moduli. L’URL/posizione dell’attività includeva un &quot;1&quot; non voluto alla fine, che ora è stato rimosso per garantire un collegamento accurato. (TGT-52355 e TGT-52358)
* È stato risolto un problema che causava la generazione di collegamenti di controllo qualità errati da parte dell’attività basata su moduli. L&#39;URL attività includeva un `http://pid-ppc` non previsto all&#39;inizio dell&#39;URL, che ora è stato rimosso per garantire un collegamento accurato. (TGT-52557)
* È stato risolto un problema a causa del quale [!DNL Target] generava collegamenti di controllo qualità non validi per le attività basate su moduli. (TGT-52528 e TGT-52603)
* È stato risolto un problema che causava l&#39;elaborazione del salvataggio di un&#39;attività modificata, ma mai completata, e nessun messaggio di errore veniva visualizzato in [!DNL Target]. (TGT-52461)
* È stato risolto un problema che impediva al [!UICONTROL Visual Experience Composer] (VEC) aggiornato di rilevare automaticamente il valore `at_property`. (TGT-52347)
* È stato risolto un problema che causava la registrazione di due modifiche quando ne era prevista solo una dopo il passaggio tra le modalità [!UICONTROL Browse] e [!UICONTROL Design] nel Compositore esperienza visivo durante l&#39;interazione con un elemento modulo. (TGT-52455)
* È stato risolto un problema che impediva la selezione dell’impostazione [!UICONTROL Clicked an Element] nel Compositore esperienza visivo aggiornato a causa di un errore che indicava che il selettore non era valido, era già utilizzato o non era visibile. (TGT-52467)
* È stato risolto un problema che causava la visualizzazione di caselle duplicate (ghost) a causa dell’aggiunta di una casella [!UICONTROL Recommendation Offer] nel Compositore esperienza visivo aggiornato. Il passaggio tra l’Esperienza A e B ha aggiunto ripetutamente più caselle fantasma. (TGT-52505 e TGT-52519)
* È stato risolto un problema nell&#39;interfaccia utente [!DNL Target] aggiornata a causa del quale le modifiche apportate a un&#39;offerta HTML tramite il menu [!UICONTROL Offer] non venivano riportate nell&#39;attività associata e viceversa. Questo comportamento ora corrisponde all&#39;interfaccia utente legacy, in cui gli aggiornamenti vengono sincronizzati correttamente tra il menu [!UICONTROL Offer] e l&#39;attività. (TGT-52540 e TGT-52541)
* È stato risolto un problema a causa del quale gli aggiornamenti recenti di [!UICONTROL Experience Fragments] in [!UICONTROL Offers Library] non venivano rispecchiati durante il tentativo di utilizzarli all&#39;interno di un&#39;attività. (TGT-52659)
* È stato risolto un problema di localizzazione nella traduzione in cinese semplificato di un messaggio di conferma. Nella versione precedente mancavano le virgolette intorno al nome della posizione e utilizzava un linguaggio informale, contrariamente a quanto previsto dalla guida di stile del cliente. La traduzione aggiornata ora utilizza la punteggiatura corretta e un tono formale. (TGT-52364)

### [!DNL Target Standard/Premium] 25.5.3 (22 maggio 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema che impediva il corretto funzionamento della funzione di ricerca per nome nell&#39;elenco [!UICONTROL Activities] con query con più parole. (TGT-52529)
* È stato risolto un problema che impediva l&#39;esclusione delle esperienze dalle attività [!UICONTROL Automated Personalization] (AP). (TGT-52383)
* È stato risolto un problema che causava l&#39;assenza dell&#39;opzione &quot;[!UICONTROL Contains]&quot; da [!UICONTROL Filter Rules] durante la gestione del contenuto nelle attività di Personalizzazione automatizzata. (TGT-52384)
* È stata risolta un&#39;incoerenza di reporting nelle attività di [!UICONTROL Automated Personalization] (AP), in particolare per quanto riguarda il modo in cui le offerte predefinite vengono tracciate e segnalate utilizzando i valori `optionLocalId` del sistema interno di [!DNL Target].
* È stato risolto un problema che impediva ai collegamenti di controllo qualità di fornire l’esperienza di attività desiderata. (TGT-52163)
* È stato risolto un problema che impediva agli utenti con autorizzazioni [!UICONTROL Approver] di modificare le attività live in modo errato, ricevendo un messaggio di errore &quot;Accesso negato&quot;. (TGT-52416)
* È stato risolto un problema che impediva la visualizzazione dei perfezionamenti del pubblico per alcune attività nell&#39;interfaccia utente [!DNL Target] aggiornata. (TGT-52057)
* È stato risolto un problema che causava l’inversione dei perfezionamenti del pubblico e dei tipi di pubblico dell’attività nell’interfaccia utente aggiornata. (TGT-52158)
* È stato risolto un problema a causa del quale la generazione di offerte ad hoc generava offerte duplicate. (TGT-51938)
* È stato risolto un problema che bloccava gli aggiornamenti delle offerte e causava la visualizzazione errata di un errore &quot;Utente non valido&quot;. (TGT-52361)
* È stato risolto un problema che impediva il salvataggio delle attività esistenti, causando un errore di tipo &quot;Input utente non valido&quot;. (TGT-52422)
* È stato risolto un problema che impediva la modifica delle offerte HTML esistenti, causando un errore di tipo &quot;Input utente non valido&quot; al momento del salvataggio, anche quando non venivano apportate modifiche al codice. (TGT-52351)
* È stato risolto un problema che impediva a [!DNL Target] di riconoscere il carattere &quot;#&quot; nell&#39;URL di un sito Web. (TGT-52093)
* È stato risolto un problema che impediva la modifica delle attività [!DNL Recommendations] per aggiungere o aggiornare promozioni, causando errori di salvataggio e promozioni duplicate. (TGT-52343)
* È stato risolto un problema che impediva la modifica di criteri o progettazioni nelle attività [!DNL Recommendations], causando un errore &quot;JSON non valido: nome proprietà non riconosciuto&quot;. (TGT-52375)
* È stato risolto un problema che impediva la corretta visualizzazione dei criteri di sequenza nel Compositore esperienza visivo [!UICONTROL Visual Experience Composer] per le attività [!DNL Recommendations]. (TGT-52435)
* È stato risolto un problema che impediva la corretta identificazione delle visualizzazioni nelle pagine di applicazioni a pagina singola quando si utilizzava [!DNL Adobe Experience Platform Web SDK]. (TGT-52106)
* È stato risolto un problema a causa del quale i dettagli di On-Device Decisioning (ODS) non venivano salvati correttamente, nonostante fossero inclusi nel payload dell’operazione batch. (TGT-52406)
* Alle attività è stato aggiunto un campo `audienceMetadata` che consente di leggerlo e aggiornarlo durante la modifica. (TGT-51004)
* È stato aggiunto un messaggio di errore per avvisare gli utenti quando un arco temporale del pubblico non è valido. (TGT52522)
* È stata aggiornata la struttura delle attività per supportare tipi di pubblico duplicati di diversi tipi. (TGT-51200)

### Versione di [!DNL Adobe Target] [!DNL AI Assistant] (16 maggio 2025)

Siamo entusiasti di annunciare il lancio di [!DNL AI Assistant] in [!DNL Adobe Target]. Questa potente funzionalità dell&#39;interfaccia utente è stata progettata per facilitare la navigazione e la comprensione dei concetti di [!DNL Target]. Disponibile in più prodotti in [!DNL Adobe Experience Cloud], tra cui [!DNL Target], [!DNL AI Assistant] è qui per rivoluzionare la tua esperienza.

[!DNL AI Assistant] in [!UICONTROL Target] è uno strumento di conversazione che puoi utilizzare per accelerare i flussi di lavoro con le applicazioni e i servizi [!DNL Experience Platform]. Utilizza [!DNL AI Assistant] per migliorare la tua produttività complessiva e approfondire la tua conoscenza dei prodotti

In [!DNL Target], la prima fase di [!DNL AI Assistant] fornisce informazioni preziose sui prodotti basate sulla documentazione di [!DNL Experience League]. Sono state trattate sia la configurazione di uno script di profilo, la risoluzione di problemi o l&#39;aggiornamento a AEP Web SDK, [!DNL AI Assistant].

Per ulteriori informazioni, vedere [Panoramica dell&#39;Assistente di Adobe Experience Platform AI](/help/main/c-intro/ai-assistant.md).

### [!DNL Target Standard/Premium] 25.5.2 (8 maggio 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* [!DNL Target] utenti con diritti [!UICONTROL Product Administrator] e [!UICONTROL System Administrator] possono ora modificare tutte le impostazioni nelle pagine [!UICONTROL Administration], indipendentemente dal loro ruolo in [!DNL Target]. Gli utenti senza queste autorizzazioni dispongono di accesso in sola lettura a queste impostazioni. Questo aggiornamento garantisce un controllo dell&#39;accesso più rigoroso sulle [impostazioni di amministrazione](/help/main/administrating-target/administrating-target.md). (TGT-48179)
* È stato risolto un problema di caching che impediva il salvataggio dell&#39;attività [Preferenze sito](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#settings). (TGT-52213)
* È stato risolto un problema che impediva ai clienti di abilitare la selezione per ID e classe nella sezione [!UICONTROL Site Preferences] dopo il caricamento del sito nel Compositore esperienza visivo. L&#39;impostazione [!UICONTROL Site Preferences] è stata automaticamente disabilitata anche dopo l&#39;abilitazione. (TGT-52207)
* È stato risolto un problema che impediva a [!UICONTROL Visual Experience Composer] (VEC) di visualizzare la pagina corretta quando [gli URL di consegna della pagina](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#settings) terminavano con una barra (/). (TGT-52237)
* È stato risolto un problema che impediva la rimozione delle modifiche al codice personalizzato durante la modifica delle esperienze. (TGT-52240)
* È stato risolto un problema a causa del quale le modifiche HTML nel Compositore esperienza visivo sovrapponevano gli elementi di pagina esistenti. (TGT-52265)
* È stato risolto un problema che impediva la modifica del codice personalizzato nel Compositore esperienza visivo aggiornato a causa del fatto che il codice personalizzato esistente non era visibile nell’editor. (TGT-52272)
* È stato risolto un problema che causava il messaggio di errore &quot;I nomi duplicati non sono consentiti&quot; durante il salvataggio di un’attività Consigli. (TGT-52318)
* È stato risolto un problema nel Compositore esperienza visivo aggiornato che impediva ai clienti di modificare elementi di testo o rimuovere oggetti contenitore. (TGT-52348)
* È stato risolto un problema che impediva la corretta visualizzazione di [!DNL Customer Journey Analytics] in una pagina attività [!UICONTROL Overview]. (TGT-52359)
* È stato risolto un problema che impediva ai gruppi di reporting di persistere nelle attività [!UICONTROL Automated Personalization] (AP). (TGT-52368)
* È stato risolto un problema che impediva il salvataggio di attività che includevano offer decisioning. (TGT-52390)
* È stato risolto un problema che causava la selezione dell&#39;offerta predefinita ma la visualizzazione di altri contenuti dell&#39;offerta nelle attività [!UICONTROL Automated Personalization] (AP) e [!UICONTROL Multivariate Test] (MVT). (TGT-52372)
* È stata corretta la logica delle autorizzazioni di GET per verificare con OR tra accesso completo all’organizzazione e accesso specifico per organizzazione + utente. (TGT-52374)
* È stato risolto un problema che impediva la visualizzazione dei nomi del pubblico dopo la selezione di un pubblico per [!UICONTROL Managed Content] e [!UICONTROL Reporting Audiences], anche se [!UICONTROL Show Only Selected] era abilitato. (TGT-52393)

### [!DNL Target Standard/Premium] 25.5.1 (5 maggio 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema che impediva la visualizzazione di perfezionamenti del pubblico per alcune attività nell’interfaccia utente aggiornata. (TGT-52057)
* È stato risolto un problema che impediva l’utilizzo di tipi di pubblico combinati nelle attività di. (TGT-52346)
* È stato risolto un problema che impediva la creazione di una nuova attività in un’area di lavoro non predefinita utilizzando un pubblico per sola attività dalla stessa area di lavoro. (TGE-52349)
* È stato risolto un problema che causava la scomparsa dei tipi di pubblico per sola attività dall’interfaccia utente aggiornata dopo la creazione e la selezione di un nuovo pubblico. (TGT=52091)
* È stato risolto un problema che impediva l’utilizzo di tipi di pubblico duplicati nelle attività di. (TGT-51200 e TGT-52057)
* È stato risolto un problema che causava l’inversione dei perfezionamenti del pubblico e dei tipi di pubblico dell’attività nell’interfaccia utente aggiornata. (TGT-52158)
* È stato risolto un problema che impediva la creazione di una nuova attività a causa dell’errore di inserimento dell’utente: &quot;area di lavoro non predefinita non consentita per questo utente&quot;. (TGT-52267)
* È stato risolto un problema che impediva la visualizzazione delle offerte nell’interfaccia utente aggiornata per le aree di lavoro predefinite e non predefinite. [!DNL Target] ora visualizza le offerte da entrambe le aree di lavoro. (TGT-52339)
* È stato risolto un problema a causa del quale [!DNL Target] non avvisava i clienti quando modificava un&#39;attività e modificava un elemento del sito Web modificato. (TGT-52100)
* È stato risolto un problema a causa del quale la modifica di un’offerta con offerte ad hoc creava una nuova offerta invece di aggiornare quella esistente. (TGT-52135)
* È stato risolto un problema che causava un errore di payload non valido durante lo spostamento delle offerte nelle cartelle. (TGT-52325)
* È stato risolto un problema che causava un errore di inserimento dell’utente durante lo spostamento delle offerte nelle cartelle. (TGT-52296)
* È stato aggiunto un campo `audienceMetadata` per ogni attività, per assicurarti che venga letto e aggiornato durante la modifica dell&#39;attività. (TGT-51004)

### [!DNL Target Standard/Premium] 25.4.5 (25 aprile 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema che causava discrepanze nelle inserzioni del pubblico tra la pagina delle impostazioni [!UICONTROL Activity] e la pagina della panoramica [!UICONTROL Reporting]. (TGT-52203)
* È stato risolto un problema che impediva l’aggiunta di una nuova pagina a un’attività a causa di un errore di input dell’utente non valido. (TGT-52263)
* È stato risolto un problema che causava l&#39;incremento errato di `OptionLocalIDs` quando l&#39;opzione rimaneva invariata. (TGT-52187)
* È stato risolto un problema che causava l&#39;incremento errato di `location` e `OptionLocalIDs` quando l&#39;opzione rimaneva invariata. (TGT-52188)
* È stato risolto un problema che causava un errore nella posizione della pagina [!UICONTROL Overview] dell&#39;attività. (TGT-52182)
* È stato risolto un problema che impediva la visualizzazione di un avviso di selezione non valido per una posizione non valida. (TGT-52110)
* È stato risolto un problema a causa del quale i file di reporting scaricati mostravano correttamente i dati presenti nell’interfaccia utente di reporting. (TGT-52068)
* È stato risolto un problema che impediva il corretto funzionamento delle operazioni batch dopo l’aggiunta delle regole di consegna della pagina. (TGT-52097)
* È stato risolto un problema a causa del quale [!DNL Target] eliminava tutti i parametri di query dall&#39;URL del sito Web. (TGT-52100)
* È stato risolto un errore della console che impediva ai clienti di creare attività nell&#39;interfaccia utente [!DNL Target] legacy e aggiornata. (TGT-52181)
* È stato risolto un problema che impediva ai clienti di aggiungere nuove pagine, causando un errore di input dell’utente non valido. (TGT-52258)
* È stato risolto un problema che causava la scomparsa delle modifiche dopo l&#39;aggiunta di ulteriori pagine e il ritorno alla scheda [!UICONTROL Experiences]. (TGT-52264)
* È stato risolto un problema che impediva ai clienti di modificare il pubblico in un&#39;attività [!UICONTROL Experience Targeting] (XT). (TGT-52191)
* È stato corretto un errore che impediva la modifica di un’attività XT a causa di una regola dell’interfaccia utente non supportata. (TGT-52273)
* È stato risolto un problema nel [!UICONTROL Visual Experience Composer] (VEC) aggiornato a causa del quale le breadcrumb non venivano sempre visualizzate nella parte inferiore dell’editor, causando difficoltà nella selezione precisa degli elementi. (TGT-52169)
* È stato risolto un problema che impediva all&#39;elenco a discesa [!UICONTROL Audience] di visualizzare tutti i tipi di pubblico a causa dell&#39;impaginazione. (TGT-52204)
* È stato risolto un problema che causava un messaggio di input utente non valido durante l&#39;aggiunta di nuove offerte nelle attività [!UICONTROL Automated Personalization] (AP). (TGT-52210)
* È stato risolto un problema a causa del quale [!UICONTROL Analytics for Target] (A4T) veniva erroneamente selezionato come origine per la generazione di rapporti, anche se il cliente non aveva accesso ad A4T. (TGT-52226)
* È stato risolto un problema che impediva il salvataggio di un&#39;attività con la metrica URL [!UICONTROL View a Page]. (TGT-52260)
* È stato risolto un problema che impediva ai clienti di selezionare aree di lavoro durante la creazione di offerte all’interno di un’attività. (TGT-52289)
* È stato risolto un problema che impediva ai clienti di creare attività in tutte le aree di lavoro. (Tgt-52218)
* È stato risolto un problema che causava la visualizzazione errata delle modifiche da un’esperienza quando si passava a un’altra. (TGT-52184)
* È stato risolto un problema che impediva la corretta visualizzazione dell&#39;offerta predefinita nell&#39;interfaccia utente [!DNL Target] all&#39;apertura dell&#39;attività. (TGT-52198)

### Aggiornamento delle autorizzazioni di Target (22 aprile 2025)

Questo aggiornamento futuro migliora il controllo dell&#39;organizzazione sulle configurazioni delle istanze [!DNL Target], impedendo aggiornamenti accidentali che potrebbero influire sulla distribuzione delle attività tra i vari team di test e personalizzazione.

A decorrere dal 22 aprile 2025, solo gli amministratori [!UICONTROL Product] e [!UICONTROL Solutions] potranno aggiornare le impostazioni nelle sezioni [!UICONTROL Administration], indipendentemente dai loro ruoli nelle aree di lavoro [!DNL Target]. Gli utenti senza questa autorizzazione avranno accesso in sola lettura alle sezioni [!UICONTROL Administration].

Per ulteriori informazioni, vedere [Amministrare Target](/help/main/administrating-target/start-target.md).

### [!DNL Target Standard/Premium] 25.4.4 (17 aprile 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato aggiunto un messaggio di errore per guidare gli utenti nella risoluzione delle opzioni duplicate in un’attività. (TGT-51927)
* È stato risolto un problema che impediva la rimozione di `ClickTrack` selettori durante l&#39;eliminazione di pagine o esperienze con offerte di reindirizzamento. (TGT-51952)
* È stato risolto un problema che causava l&#39;autorizzazione di selettori `ClickTrack` vuoti. [!DNL Target] ora richiede che il campo del selettore non sia vuoto. (TGT-52107)
* È stato risolto un problema che consentiva erroneamente le metriche con nomi duplicati. Le metriche ora richiedono nomi univoci. (TGT-52201)
* È stato risolto un problema a causa del quale le definizioni dei tipi di pubblico non erano visibili durante la modifica del targeting a livello di offerta nelle attività [!UICONTROL Automated Personalization] (AP). (TGT-52148)
* È stato risolto un problema che impediva ai clienti con diritti [!UICONTROL Editor] di salvare le attività. (TGT-52227)
* `OptionLocalIDs` non incrementa più in modo errato quando l&#39;opzione rimane invariata. (TGT-52139)
* È stato risolto un problema che causava un messaggio &quot;Non valido `optionLocalIds`&quot; durante il tentativo di creare un&#39;attività. (TGT-52154)
* Sono state corrette le discrepanze tra `OptionLocalIDs` definiti per un&#39;attività e quelli utilizzati per definire le esperienze. (TGT-52215)
* È stato risolto un problema che causava un errore di convalida durante il tentativo di creazione di un’attività A/B. (TGT-51923)

### [!DNL Target Standard/Premium] 25.4.3 (11 aprile 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato corretto un errore che impediva ai clienti di aprire il pop-up di informazioni sul pubblico per alcune attività [!UICONTROL Experience Targeting] (XT). (TGT-52049)
* È stato risolto un problema che causava il ripristino dell&#39;impostazione del pubblico su &quot;[!UICONTROL All Visitors]&quot; a seguito delle modifiche apportate in [!UICONTROL Visual Experience Composer] (VEC). (TGT-52132)
* È stato risolto un problema che impediva la visualizzazione di perfezionamenti del pubblico per attività specifiche (TGT-52057)
* È stato risolto un problema che impediva ai clienti di inserire un [!UICONTROL Experience Fragment] nell&#39;area di lavoro predefinita. (TGT-52073)
* È stato risolto un problema che causava la visualizzazione di un&#39;offerta come &quot;Contenuto non trovato&quot; e non sulla pagina [!UICONTROL Offers] per un&#39;attività [!UICONTROL Automated Personalization] (AP). (TGT-52150)
* È stata aggiunta la possibilità di consentire la duplicazione dei tipi di pubblico all’interno di un’attività. (TGT-51200)
* È stato risolto un problema che causava la visualizzazione del nome mbox errato nella pagina [!UICONTROL Goals & Settings] per un&#39;attività XT dopo la modifica. (TGT-52026)
* È stato risolto un problema che causava la visualizzazione di `defaultContent` nelle opzioni nonostante non fosse in `experiences/optionLocations`. (TGT-52036)
* È stato risolto un problema per garantire che le stringhe vuote non vengano convertite in valori Null. (TGT-52037)
* È stato risolto un problema che richiedeva ai clienti di riconfigurare [!UICONTROL Optimization Goal] in [!UICONTROL Reporting Settings] nella pagina [!UICONTROL Goals & Settings] dopo le modifiche. (TGT-52071)
* È stato risolto un problema a causa del quale un&#39;attività senza regole di consegna pagina visualizzava più regole sulla pagina [!UICONTROL Overview]. (TGT-52084)
* È stato aggiunto un messaggio di errore per gli utenti che tentano di salvare un’offerta con caratteri al di fuori del piano multilingue di base, ad esempio emoji. (TGT-52105)
* È stato risolto un problema a causa del quale l’apertura di un’attività attivava il messaggio di errore: &quot;Questa attività utilizza uno o più tipi di pubblico eliminati alla sorgente&quot;. (TGT-52120)
* È stato risolto un problema che impediva la visualizzazione delle metriche ClickTrack nel Compositore esperienza visivo [!UICONTROL Visual Experience Composer] aggiornato durante la modifica. (TGT-52152)
* È stato risolto un problema a causa del quale un URL con un parametro di query come posizione dell&#39;attività non visualizzava il parametro di query nella pagina [!UICONTROL Overview] dell&#39;attività. (TGT-51635)
* È stato risolto un problema che impediva la visualizzazione dell&#39;intero URL dell&#39;esperienza in [!UICONTROL Browse mode] all&#39;interno del [!UICONTROL Visual Experience Composer] (VEC). (TGT-52101)
* È stato risolto un problema a causa del quale la modifica di un’attività causava l’aggiunta di &quot;/&quot; alla fine dell’URL da parte della consegna della pagina, che ne causava l’invalidità. (TGT-52114)
* È stato risolto un problema che causava il reindirizzamento errato del collegamento [!UICONTROL Activity QA] nella home page di [!UICONTROL Form-Based Experience Composer] alla home page di [!DNL Adobe Experience Cloud]. (TGT-52055)
* È stato risolto un problema che impediva il mantenimento delle pagine aggiuntive aggiunte all&#39;attività [!UICONTROL A/B Test] dopo il salvataggio e la riapertura. (TGT-51994)
* È stato risolto un problema che impediva ai clienti di eliminare gli stili nella sezione stile in linea. (TGT-52070)
* È stato ripristinato l&#39;accesso alle [schede di definizione del pubblico](/help/main/c-target/c-audiences/audiences.md#section_11B9C4A777E14D36BA1E925021945780) nella finestra di dialogo [!UICONTROL Activity QA], in modo simile all&#39;interfaccia utente legacy. (TGT-52056)
* L’interfaccia utente aggiornata non salvava pagine o tipi di pubblico senza modifiche. Se i clienti hanno aggiunto nuove pagine o tipi di pubblico a un&#39;attività ma non vi apportano modifiche, [!DNL Target] ha eliminato i tipi di pubblico non modificati al momento del salvataggio. Le notifiche sono state aggiunte in posizioni rilevanti per informare gli utenti di questo comportamento. (TGT-52104)

### [!DNL Target Standard/Premium] 25.4.1 (2 aprile 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema che causava la scomparsa dei tipi di pubblico dell’esperienza dalle attività di. (TGT-52003)
* È stato risolto un problema che causava elementi imprevisti durante la consegna. (TGT-52011)
* È stato risolto un problema che impediva ai clienti di visualizzare il pubblico nel grafico di targeting nella pagina Ove[!UICONTROL r]view e durante la modifica dell&#39;attività. (TGT-52050)
* È stato risolto un problema che impediva ai clienti di riordinare le esperienze in ordine di priorità nelle attività [!UICONTROL Experience Targeting] (XT). (TGT-52054)
* È stato risolto un problema che causava un rendering errato quando si annullavano le modifiche allo stile del testo. (TGT-51876)
* È stato risolto un problema a causa del quale durante la modifica di un&#39;offerta di reindirizzamento, [!DNL Target] rimuove anche i selettori [!UICONTROL ClickTrack] associati a tale offerta. (TGT-51936)
* È stato risolto un problema che causava il salvataggio errato del selettore da parte di [!DNL Target] durante l&#39;annullamento di [!UICONTROL ClickTrack]. (TGT-51937)
* È stato risolto un problema che causava un errore di nome non valido dopo l&#39;apertura e la chiusura del selettore mbox sulla pagina [!UICONTROL Goals & Settings] senza apportare modifiche. (TGT-51983)
* È stato risolto un problema che impediva la modifica delle offerte ad hoc create nell&#39;interfaccia utente legacy di [!DNL Target]. (TGT-51984)
* È stato risolto un problema che bloccava le attività di modifica con offerte ad hoc contenenti codice personalizzato. (TGT-51995)
* È stato risolto un problema che causava la visualizzazione delle regole di esclusione come regole di inclusione durante la modifica delle definizioni di pubblico combinato. (TGT-51999)
* È stato risolto un problema che impediva la corretta visualizzazione del codice personalizzato durante la modifica dell’esperienza. (TGT-52005)
* È stato risolto un problema che rendeva l&#39;opzione [!UICONTROL Insert Before] non disponibile per l&#39;inserimento di contenuto prima della barra di navigazione. (TGT-52031)
* È stato risolto un problema che impediva la corretta evidenziazione dell’esperienza predefinita nel reporting. (TGT-51716)
* È stato risolto un problema che attivava un messaggio `default message [Invalid optionLocalIds: xx]]` durante la creazione di un&#39;attività. (TGT-52038)

### at.js versione 2.11.8 (31 marzo 2025)

* È stata risolta una vulnerabilità identificata da CodeQL nella convalida del suffisso di stringa per evitare casi edge durante le operazioni di ridimensionamento e spostamento. (TNT-51516)

### [!DNL Target Standard/Premium] 25.3.8 (28 marzo 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema che causava il caricamento lento della pagina [!UICONTROL Activities]. (TGT-51151)

### [!DNL Target Standard/Premium] 25.3.7 (26 marzo 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema che impediva il salvataggio di attività multipagina se una pagina veniva eliminata dopo le modifiche. (TGT-51988)
* È stato risolto un errore che si verificava durante la modifica di un&#39;attività: `default message [Invalid optionLocalIds: xx]]`. (TGT-51985)
* È stato risolto un problema a causa del quale l’aggiunta di nuove modifiche a un’attività rimuoveva le modifiche esistenti. (TGT-51981)
* È stato risolto un problema a causa del quale la sostituzione di un pubblico con &quot;[!UICONTROL All visitors]&quot; durante la creazione o la modifica dell&#39;attività causava un errore &quot;I tipi di pubblico duplicati non sono consentiti&quot;. (TGT-51978)
* È stato risolto un problema che causava un errore &quot;Input utente non valido&quot; durante il salvataggio di un&#39;attività [!UICONTROL A/B Test]. (TGT-51976)
* È stato risolto un problema che impediva la corretta visualizzazione delle metriche calcolate sulla pagina [!UICONTROL Goals & Settings]. (TGT-51975)
* È stato risolto un problema che impediva la corrispondenza tra `companyName` e `reportSuite` nella configurazione [!DNL Analytics] per la metrica `pageviews`. (TGT-51965)
* È stato risolto un problema che causava la rimozione delle modifiche dal passaggio a un’esperienza in un’attività. (TGT-51945)
* È stato risolto un problema a causa del quale la rimozione di un pubblico di pagina causava la rimozione anche di [!UICONTROL ClickTrack] selettori. (TGT-51935)
* È stato risolto un problema che impediva la modifica di un&#39;attività dopo l&#39;apertura della relativa pagina [!UICONTROL Overview]. (TGT-51931)
* È stato risolto un problema che causava un errore `[Unused optionLocalIds: 0]]` durante la creazione dell&#39;attività. (TGT-51920)
* È stato risolto un problema a causa del quale alcune modifiche non venivano tradotte correttamente dopo la rimozione delle modifiche allo stile del testo. (TGT-51876)
* È stato risolto un problema che impediva il corretto aggiornamento dei tipi di pubblico di destinazione in [!UICONTROL Form-Based Experience Composer]. (TGT-51845)
* È stato risolto un problema che impediva l&#39;aggiornamento corretto dell&#39;URL in [!UICONTROL Visual Experience Composer] durante la navigazione dell&#39;attività. (TGT-51832)
* È stato risolto un problema che impediva la visualizzazione delle offerte nell&#39;interfaccia utente [!UICONTROL Offers], nonostante la corretta visualizzazione durante la creazione di un&#39;attività e l&#39;aggiunta di offerte. (TGT-51805)
* È stato risolto un problema a causa del quale alcune attività non disponevano di una schermata di fallback per visualizzare il contenuto predefinito quando non era possibile distribuire contenuto personalizzato o mirato. (TGT-51638)
* È stato risolto un problema che impediva la corretta visualizzazione delle offerte live e di alcune cartelle nell&#39;interfaccia utente [!UICONTROL Offers]. (TGT-51628)
* È stato risolto un problema che impediva la corretta localizzazione di alcune stringhe URL e goURL. (TGT-35741)
* È stato risolto un problema che impediva la corretta localizzazione dei ruoli ([!UICONTROL Approver], [!UICONTROL Editor] e [!UICONTROL Observer]) nell&#39;interfaccia utente [!DNL Target]. (TGT-29925)

### [!DNL Target Standard/Premium] 25.3.6 (14 marzo 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto l&#39;errore &quot;Input utente non valido&quot; nelle attività [!UICONTROL Visual Experience Composer] (VEC) con [!UICONTROL Click Tracking] abilitato quando lo stesso selettore [!UICONTROL ClickTrack] viene utilizzato più volte. (TGT-51921)
* È stato corretto l’errore &quot;Input utente non valido&quot; nelle attività del Compositore esperienza visivo con posizioni condivise (ad esempio, selettore HEAD) e offerte identiche. (TGT-51879)
* È stato risolto un problema che causava la condivisione delle modifiche dell’esperienza tra i vari tipi di pubblico. (TGT-51815)
* Sono stati risolti degli errori di convalida durante la creazione di attività a causa di conflitti di ID segmento. Gli errori si sono verificati quando [!DNL Target] ha rilevato attività esistenti utilizzando segmenti anonimi. (TGT-51784)
* È stato risolto un problema che impediva a [!DNL Target] di salvare attività con regole di esclusione in un pubblico. (TGT-51581)
* È stato risolto un problema che impediva ai clienti di creare, eliminare o spostare cartelle senza accedere all’area di lavoro predefinita. (TGT-51499)
* È stato risolto un problema che causava un errore nelle richieste di GET durante il recupero dell&#39;elenco delle metriche [!DNL Analytics]. (TGT-51106)

### [!DNL Target Standard/Premium] 25.3.5 (11 marzo 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema che impediva agli utenti di modificare le offerte nel pannello [!UICONTROL Modifications]. (TGT-51800)
* È stato risolto un problema che impediva la corretta visualizzazione delle azioni nel pannello sinistro per esperienze e tipi di pubblico, incluso in modalità [!UICONTROL ClickTrack]. (TGT-51895)
* È stato risolto un problema a causa del quale i selettori [!UICONTROL ClickTrack] non venivano applicati alla pagina corretta del pubblico. (TGT-51871)

### [!DNL Target Standard/Premium] 25.3.4 (7 marzo 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema che impediva la modifica o il riutilizzo dei tipi di pubblico per sola attività nel pannello [!UICONTROL Audiences]. (TGT-51860)
* È stato risolto un problema che impediva ai clienti [!DNL Target Standard] di creare attività utilizzando reporting di [!UICONTROL Analytics for Target] (A4T). (TGT-51854)
* È stato risolto un problema che escludeva i contatori degli ID locali dal payload durante le operazioni di creazione e modifica in batch. (TGT-51867)

### [!DNL Target Standard/Premium] 25.3.2 (6 marzo 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema che impediva la creazione di una nuova attività in seguito alla copia di un’attività con un pubblico per sola attività, utilizzando erroneamente il pubblico dell’attività originale. (TGT-51855)
* È stato risolto un problema che impediva la modifica delle attività [!UICONTROL Experience Targeting] (XT) con tipi di pubblico per sola attività. (TGT-51846)
* È stato risolto un problema che impediva al Compositore esperienza visivo di applicare correttamente le modifiche a un&#39;esperienza alla prima modifica. [!UICONTROL Visual Experience Composer] (TGT-51843)
* È stato risolto un problema che attivava un errore &quot;ID&quot; quando si faceva clic su alcuni elementi all’interno del Compositore esperienza visivo. (TGT-51814)
* È stata aggiornata la gestione degli errori nel Compositore esperienza visivo durante la creazione dell’attività. (TGT-51759)
* È stato risolto un problema che causava un errore di &quot;input utente non valido&quot; durante il salvataggio dell&#39;attività a causa di una visualizzazione mancante nel pannello [!UICONTROL Modifications]. (TGT-51827)
* È stato risolto un problema che impediva la creazione di criteri per i consigli. (TGT-51834)
* È stato aggiunto un messaggio di conferma prima del reindirizzamento a un URL diverso. (TGT-51703)
* Sono stati risolti dei problemi relativi ai test di integrazione di GraphQL in offerte e cartelle. (TGT-51839)

### [!DNL Target Standard/Premium] 25.3.1 (3 marzo 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* Un pubblico combinato può includere sottogruppi, ciascuno contenente più tipi di pubblico. Questa versione ha risolto un problema che impediva la visualizzazione dei tipi di pubblico dei sottogruppi nella finestra di dialogo [!UICONTROL Rules]. (TGT-51813)
* È stato risolto un problema che causava la sostituzione di alcuni tipi di pubblico di esperienza con [!UICONTROL All Visitors] durante l&#39;apertura di attività precedenti. (TGT-51812)
* È stato risolto un problema che impediva la modifica di attività con tipi di pubblico per sola attività. (TGT-51807)
* È stato risolto un problema che impediva la modifica delle modifiche dell&#39;intestazione della pagina nell&#39;interfaccia utente [!DNL Target] aggiornata. (TGT-51797)
* È stato risolto un errore Null che si verificava durante la duplicazione di un’esperienza, l’eliminazione di un’altra esperienza e il tentativo di salvare l’attività. (TGT-51796)
* È stato risolto un problema che impediva la visualizzazione delle regole di esclusione del pubblico nel pannello informazioni del pubblico durante il passaggio [!UICONTROL Targeting] della creazione delle attività. (TGT-51579)
* Aggiornati messaggi di errore localizzati in coreano. (TGT-51701 e TGT-51699)

### [!DNL Target Standard/Premium] 25.2.3 (26 febbraio 2025)

Questa versione include i seguenti aggiornamenti:

* È stato risolto un problema che impediva aggiornamenti delle attività dopo la versione 25.2.1 di [!DNL Target] per alcune attività. (TGT-51781)
* È stato risolto un problema che causava la rimozione di tutte le modifiche apportate al pubblico nello stato in seguito all&#39;annullamento del processo di creazione attività (selezione di [!UICONTROL Cancel] invece di [!UICONTROL Add Audience]). (TGT-51769 e TGT-51770)
* È stato risolto un problema che impediva il caricamento di [!UICONTROL Visual Experience Composer] (VEC) per alcune attività, in particolare quando veniva utilizzato un codice personalizzato.  Il problema ha portato il Compositore esperienza visivo a visualizzare una schermata vuota o a ripristinare la versione precedente dell&#39;interfaccia utente [!DNL Target]. (TGT-51758)
* È stato risolto un problema a causa del quale le modifiche venivano eliminate dopo la modifica della distribuzione delle pagine per i tipi di pubblico. (TGT-51756)
* È stato risolto un problema che causava la rimozione dalle attività di tutti i tipi di pubblico non metrici (pubblico di pagina e pubblico di esperienza) in seguito alla modifica di un tipo di metrica nella pagina [!UICONTROL Goals & Settings]. (TGT-51753)
* È stato risolto un problema per cui facendo clic su [!UICONTROL Cancel] durante la modifica di un&#39;attività, l&#39;interfaccia utente di Target passava a [!UICONTROL Activities List] invece che alla pagina [!UICONTROL Activity Details]. (TGT-51731)
* È stato risolto un problema che impediva ai clienti di scaricare i report tramite l&#39;opzione [!UICONTROL Export Reports to CSV]. (TGT-51708)
* È stato risolto un problema nel Compositore esperienza basato su moduli a causa del quale [!DNL Target Standard] clienti venivano erroneamente visualizzati per l&#39;utilizzo di [!UICONTROL Properties], una funzionalità [!DNL Target Premium]. (TGT-51678)
* È stato risolto un problema che impediva la visualizzazione degli attributi [!DNL Adobe Experience Platform] durante la creazione di nuove offerte. (TGT-51665)
* Tutti i filtri attivi per l&#39;inventario [!DNL Recommendations] sono stati spostati nella ricerca rapida, allineando l&#39;interfaccia utente con [!UICONTROL Catalog Search] invece della barra [!UICONTROL Filter]. (TGT-50723)

### at.js versione 2.11.7 (26 febbraio 2025)

Questa versione include i seguenti aggiornamenti:

* È stata corretta la registrazione di telemetria quando `localStorage` non è disponibile. La telemetria causava problemi ad alcuni clienti che avevano disabilitato `localStorage` nei loro browser.

Per informazioni su questa versione e sulle versioni precedenti di at.js, consulta [Dettagli sulla versione di at.js](https://experienceleague.adobe.com/it/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions){target=_blank}.

### Target Standard/Premium 25.2.1 (martedì 17 febbraio 2025) {#ui-update-2}

Questa versione include i seguenti aggiornamenti:

* Aggiornamento dell&#39;interfaccia utente di [!UICONTROL Activities]
* Aggiornamento dell&#39;interfaccia utente di [!DNL Recommendations]

#### Aggiornamento dell&#39;interfaccia utente di [!UICONTROL Activities]

Mentre il tentativo di modernizzazione dell&#39;interfaccia utente [!DNL Adobe Target] continua, è possibile annunciare la disponibilità generale dell&#39;interfaccia utente [!UICONTROL Activities] aggiornata.

>[!NOTE]
>
>A partire dal 17 febbraio, i clienti avranno gradualmente accesso alla nuova interfaccia utente [!UICONTROL Activities]. Per garantire un rollout senza soluzione di continuità per tutti i clienti, questa versione verrà implementata in fasi controllate. La prima fase aggiornerà il gruppo iniziale di [!DNL Target] clienti alla nuova interfaccia utente [!UICONTROL Activities]. Le fasi successive aggiorneranno i clienti rimanenti.

>[!IMPORTANT]
>
>Per informazioni importanti sul piano di fine del ciclo di vita per l&#39;attivazione/disattivazione della versione dell&#39;interfaccia utente [!DNL Target], vedere [[!DNL Target] Impostazione/disattivazione della versione dell&#39;interfaccia utente](/help/main/r-release-notes/release-notes.md#toggle).

In base al sistema di progettazione [!DNL Adobe Spectrum] più recente, l&#39;aggiornamento standardizza i modelli di progettazione precedentemente incoerenti, aggiungendo nuovi miglioramenti, ad esempio:

* [Generazione rapporti riprogettata](/help/main/administrating-target/reporting.md) per ottenere informazioni più approfondite sui risultati delle attività.
* [[!UICONTROL Updated Change Log]](/help/main/c-activities/change-log.md) pagina, sta ottenendo le informazioni da [[!DNL Audit Query API]](https://experienceleague.adobe.com/it/docs/experience-platform/landing/governance-privacy-security/audit-logs/audit-api/overview){target=_blank} per approfondimenti in tempo reale.
* [Viste elenco personalizzabili](/help/main/c-activities/activities.md) per una maggiore flessibilità tra le diverse esigenze del team.
* [Sono state migliorate le schermate di informazioni rapide e dettagli](/help/main/c-activities/activities.md) per un accesso più semplice alle informazioni.
* [Opzioni di ricerca e filtro persistenti alla sessione](/help/main/c-activities/activities.md).
* Completamente [ ha ricostruito [!UICONTROL Visual Editing Composer]](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) con il supporto per gli ultimi aggiornamenti di sicurezza dai provider del browser e una moderna interfaccia utente.

  Per informazioni sulle differenze tra il Compositore esperienza visivo aggiornato e la versione precedente, vedi:

   * [Modifiche al Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md)
   * [Opzioni del Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md)

* [Aggiornamento [!DNL Chrome] dell&#39;estensione](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) che supporta Manifest V3 per una maggiore sicurezza e un migliore supporto per i cookie di prime parti.

![Aggiornamento attività](/help/main/r-release-notes/assets/activities-refresh.png)

#### Aggiornamento dell&#39;interfaccia utente di [!DNL Recommendations]

Mentre il tentativo di modernizzazione dell&#39;interfaccia utente [!DNL Adobe Target] continua, è possibile annunciare la disponibilità generale dell&#39;interfaccia utente [!DNL Recommendations] aggiornata.

>[!NOTE]
>
>A partire dal 17 febbraio, i clienti avranno gradualmente accesso alla nuova interfaccia utente [!UICONTROL Recommendations]. Per garantire un rollout senza soluzione di continuità per tutti i clienti, questa versione verrà implementata in fasi controllate. La prima fase aggiornerà il gruppo iniziale di [!DNL Target] clienti alla nuova interfaccia utente [!UICONTROL Activities]. Le fasi successive aggiorneranno i clienti rimanenti.

In base al sistema di progettazione [!DNL Adobe Spectrum] più recente, l&#39;aggiornamento standardizza i modelli di progettazione precedentemente incoerenti, aggiungendo nuovi miglioramenti, ad esempio:

* La [ricerca nel catalogo prodotti](/help/main/c-recommendations/c-products/catalog-search.md) ora include un database aggiornato che consente la sincronizzazione in tempo reale dei prodotti.
* [!UICONTROL Recommendations] oggetti ([!UICONTROL Criteria], [!UICONTROL Designs], [!UICONTROL Collections] e [!UICONTROL Exclusions]) [creati tramite API sono ora disponibili nell&#39;interfaccia utente](/help/main/c-recommendations/c-recommendations-faq/recommendations-faq.md).
* [Le impostazioni dei consigli](/help/main/administrating-target/recommendations-settings.md) sono state consolidate nella sezione [!UICONTROL Administration].
* Visualizzazioni elenco personalizzabili per una maggiore flessibilità tra le diverse esigenze del team.
* Aggiornati editor di codice HTML e JSON con [evidenziazione della sintassi e numerazione delle righe](/help/main/c-experiences/c-manage-content/create-json-offer.md).
* Sono state migliorate le schermate di informazioni rapide e dettagli per un accesso più semplice alle informazioni.
* Opzioni di ricerca e filtro persistenti nella sessione.

![Aggiornamento dell&#39;interfaccia utente Recommendations](/help/main/r-release-notes/assets/recs-ui-refresh.png)

### Target Standard/Premium 25.1.1 (venerdì 9 gennaio 2025) {#ui-update-1}

Questa versione include i seguenti aggiornamenti:

#### Aggiornamento dell&#39;interfaccia utente di [!UICONTROL Offers Library]

Per migliorare l&#39;esperienza utente per [!DNL Adobe Target] utenti, questa versione aggiorna l&#39;interfaccia utente di [!UICONTROL Offers Library].

>[!NOTE]
>
>Per garantire un rollout senza soluzione di continuità per tutti i clienti, questa versione verrà implementata in fasi controllate. La prima fase ha aggiornato il gruppo iniziale di clienti Target alla nuova interfaccia utente Offerte. Le fasi successive aggiorneranno i clienti rimanenti.

>[!IMPORTANT]
>
>Per informazioni importanti sul piano di fine del ciclo di vita per l&#39;attivazione/disattivazione della versione dell&#39;interfaccia utente [!DNL Target], vedere [[!DNL Target] Impostazione/disattivazione della versione dell&#39;interfaccia utente](/help/main/r-release-notes/release-notes.md#toggle).

Utilizzando il più recente sistema di progettazione [!DNL Adobe Spectrum], questo aggiornamento standardizza i modelli di progettazione incoerenti e introduce nuovi miglioramenti, tra cui i seguenti:

* **Gestione delle offerte in blocco**: seleziona ed elimina o sposta più offerte contemporaneamente.

* **[!UICONTROL Code Editor]aggiornamenti**: gli editor HTML e JSON sono stati aggiornati con l&#39;evidenziazione della sintassi e la numerazione delle righe.

* **Schede offerte migliorate**: informazioni rapide e schede dettagli migliorate per un accesso più semplice alle informazioni.

* **Ricerca e filtri persistenti**: aggiunge opzioni di ricerca e filtro persistenti nella sessione.

Per ulteriori informazioni, vedere [Offerte](/help/main/c-experiences/c-manage-content/manage-content.md) e i sottoarticoli in questa sezione. Tutti gli articoli sulle offerte in questa sezione sono stati aggiornati per riflettere queste modifiche dell’interfaccia utente.

Di seguito un breve video che evidenzia le modifiche apportate a questa versione:

![Video di aggiornamento dell&#39;interfaccia utente delle offerte](/help/main/r-release-notes/assets/offers-video-v2.gif)

## Note sulla versione - 2024

### Ottimizzazione dell&#39;ambito [!DNL Adobe Experience Platform Web SDK] `__view__` (22 ottobre 2024)

Tra il 22 luglio 2024 e il 15 agosto 2024, il team [!DNL Target] ha ottimizzato l&#39;ambito `__view__`, migliorando la precisione dei rapporti sulle impression delle attività, sulle visite e sui visitatori. Questa ottimizzazione mira a acquisire automaticamente i dati di reporting per le proposte con rendering automatico e dovrebbe essere trasparente per la maggior parte degli account.

Questa ottimizzazione verrà abilitata per tutti i nuovi clienti di [!DNL Adobe Experience Platform Web SDK]. Tuttavia, l’ottimizzazione è disabilitata per i clienti che hanno eseguito la migrazione da at.js e non hanno seguito i passaggi di implementazione indicati di seguito. Esortiamo questi clienti a rivedere le loro implementazioni entro il 3 febbraio 2025. Dopo questa data, abiliteremo l’ottimizzazione per tutti i clienti. Il mancato riesame e adeguamento delle implementazioni entro tale data potrebbe influire sui rapporti, come indicato di seguito. Contatta [!DNL Adobe Customer Care] se devi confermare se l&#39;implementazione è interessata o se hai bisogno di più tempo per regolarla.

>[!IMPORTANT]
>
>Se non riesci a completare la revisione dell’implementazione e risolvere eventuali problemi entro il 3 febbraio 2025, puoi richiedere una proroga una tantum di sei mesi. Assicurati di inviare la richiesta entro il 31 gennaio 2025. Adobe rivedrà e deciderà sulla tua richiesta.

Per beneficiare di questa ottimizzazione in caso di rendering manuale della proposta, controlla [[!DNL Platform Web SDK implementation]](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/aep-web-sdk){target=_blank} per assicurarti di inviare le notifiche dopo il rendering manuale delle esperienze o quando utilizzi il metodo `applyPropositions` (o l&#39;azione [!DNL Launch] corrispondente come helper) per eseguire il rendering delle esperienze.

Gli scenari più comuni in cui viene eseguito manualmente il rendering delle esperienze includono:

* Utilizzo delle offerte JSON
* Utilizzo di un ambito di decisione personalizzato in un&#39;attività creata in [[!UICONTROL Form-Based Experience Composer]](/help/main/c-experiences/form-experience-composer.md)
* Non utilizzare `renderDecisions: true` durante il recupero di un&#39;attività creata utilizzando [!UICONTROL Form-Based Experience Composer] che utilizza l&#39;ambito `__view__` globale

Se le notifiche non sono implementate come documentato in [Rendering del contenuto personalizzato](https://experienceleague.adobe.com/it/docs/experience-platform/web-sdk/personalization/rendering-personalization-content){target=_blank} nella guida *Raccolta dati*, i dati di reporting potrebbero essere mancanti in [!DNL Target] e in [Analytics for Target reporting](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T). In alcuni scenari, potresti notare una suddivisione del traffico errata perché i dati di reporting non vengono acquisiti. Oppure, in altri scenari, riportare ripetutamente lo stesso evento.

A seconda dell&#39;implementazione, verifica la presenza di [!DNL Analytics] e l&#39;impatto dei rapporti A4T.

[!DNL Platform Web SDK] supporta due tipi di implementazione per il rendering di esperienze e personalizzazioni:

* **Chiamata singola per la personalizzazione e la misurazione.**

  Inizialmente consigliato, l&#39;approccio a chiamata singola per [!DNL Platform Web SDK] verrà dichiarato obsoleto a favore dell&#39;approccio a chiamata divisa. Adobe consiglia a tutte le nuove implementazioni di utilizzare il nuovo approccio di split-call e consiglia ai clienti esistenti di passare anche loro al metodo di split-call.

  Se si continua a utilizzare l&#39;approccio a chiamata singola, è possibile che nei report [!DNL Analytics] vengano rilevate le seguenti modifiche impreviste:

   * Un tuffo nei mancati recapiti.
   * Gli hit A4T e [!UICONTROL Page View] non sono uniti tra loro, rendendo difficile eseguire determinati raggruppamenti e correlazioni dei rapporti A4T utilizzando [!DNL Analytics] eVar ed eventi.

* **Chiamate divise (note anche come eventi di inizio e fine pagina).**

  Questo tipo di implementazione è il nuovo [approccio di implementazione con chiamata divisa](https://experienceleague.adobe.com/it/docs/experience-platform/web-sdk/use-cases/top-bottom-page-events){target=_blank} consigliato da [!DNL Adobe]. Con questo approccio, la nuova ottimizzazione non influisce sui rapporti [!DNL Analytics] o A4T.

In caso di domande, contatta l&#39;[Assistenza clienti Adobe](/help/main/cmp-resources-and-contact-information.md##reference_ACA3391A00EF467B87930A450050077C). (KB-2179)

### at.js versione 2.11.6 (29 settembre 2024)

* È stato risolto un problema che impediva a [!DNL Target] di funzionare correttamente con le offerte di reindirizzamento all&#39;interno di [!UICONTROL Visual Experience Composer] (VEC) o [!UICONTROL Form-Based Experience Composer].

Per ulteriori informazioni sulle versioni di at.js, consulta [Dettagli sulla versione di at.js](https://experienceleague.adobe.com/it/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions){target=_blank} nella *Guida per gli sviluppatori di Adobe Target*.

### Generazione rapporti [!DNL Target] in [!DNL Adobe Customer Journey Analytics] (8 maggio 2024)

L&#39;integrazione tra [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/it/docs/customer-journey-analytics){target=_blank} e [!DNL Target] offre potenti strumenti di analisi che consentono di risparmiare tempo per il programma di ottimizzazione.

I vantaggi principali dell’utilizzo di [!DNL Customer Journey Analytics] come origine di reporting per [!DNL Target] sono:

* Gli addetti al marketing possono applicare dinamicamente le metriche di successo di [!DNL Customer Journey Analytics] ai rapporti delle attività di [!DNL Target] in qualsiasi momento. Non è necessario specificare tutte le impostazioni prima di eseguire l’attività.
* Gli addetti al marketing possono sfruttare le funzionalità di [!DNL Customer Journey Analytics], ad esempio il [pannello Sperimentazione](https://experienceleague.adobe.com/it/docs/analytics-platform/using/cja-workspace/panels/experimentation){target=_blank}, per analizzare ulteriormente la personalizzazione del sito Web.

Per ulteriori informazioni, consulta [Generazione rapporti di Target in Adobe Customer Journey Analytics](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md).

### Estensione helper [!UICONTROL Visual Experience Composer] (23 aprile 2024)

L&#39;estensione legacy [!DNL Target] Helper per il Compositore esperienza visivo è stata creata con Manifest V2. [!DNL Google] ha annunciato che non consentirà più le estensioni create utilizzando Manifest V2 a partire da giugno 2024. Per ulteriori informazioni, vedere [[!UICONTROL Visual Experience Composer] estensione helper](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md).

[!DNL Adobe] consiglia ai clienti di passare al più recente [estensione Helper per editing video](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) non appena possibile.

### Aggiornamenti per `Browser:iPad` e `Browser:iPhone` negli attributi del pubblico [!UICONTROL Browser] (30 aprile 2024)

| Aggiornamenti | Dettagli |
|--- |--- |
| [!UICONTROL Browser:iPad] e [!UICONTROL Browser:iPhone] aggiornati in [Attributi browser](/help/main/c-target/c-audiences/c-target-rules/browser.md) utilizzati durante la creazione di tipi di pubblico. | [!DNL Adobe Target] consente di [eseguire il targeting per uno qualsiasi degli attributi di categoria](/help/main/c-target/c-audiences/c-target-rules/target-rules.md), inclusi i visitatori che visitano la pagina utilizzando [opzioni browser o browser](/help/main/c-target/c-audiences/c-target-rules/browser.md) specifiche.<P>A partire da [!DNL Target] Standard/Premium 24.3.1 (4-6 marzo 2024), i tipi di pubblico incorporati creati utilizzando l&#39;interfaccia utente di Target, come `Browser:iPad` e `Browser:iPhone`, verranno aggiornati per eseguire il targeting corretto per [!DNL iPad] e [!DNL iPhone] utilizzando `profile.mobile.deviceVendor`, `profile.mobile.isMobilePhone` e `profile.mobile.isTablet`.<P>Questo aggiornamento non richiede alcuna azione da parte dei clienti.<p><B>Importante</b>: per consentire ai clienti di eseguire il targeting corretto per [!DNL iPad] e [!DNL iPhone] negli script di profilo (e nei segmenti JavaScript), il cliente deve apportare modifiche manuali entro il **30 aprile 2024**. Per esempi di impostazioni alternative che devono essere modificate manualmente, vedere [Aggiornamenti per [!DNL iPad] e [!DNL iPhone] in [!UICONTROL Browser] attributi pubblico](/help/main/c-target/c-audiences/c-target-rules/browser.md#updates). |

### Estensione [!UICONTROL Visual Editing Helper] (14 marzo 2024)

Questa versione contiene i miglioramenti e le correzioni seguenti per l&#39;estensione [[!DNL Adobe Experience Cloud Editing Helper]](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) per [!DNL Google Chrome]:

* È stato migliorato il meccanismo di caricamento dell’iFrame durante l’authoring nei siti web dei clienti.
* È stato risolto un problema che causava la duplicazione dei cookie da parte dell&#39;estensione durante l&#39;esecuzione dell&#39;authoring nel Compositore esperienza visivo [!UICONTROL Visual Experience Composer].

### [!DNL Target] Standard/Premium 24.3.1 (4-6 marzo 2024)

Questa versione include i miglioramenti e le correzioni seguenti:

* È stata corretta la logica che calcola il numero di selettori univoci in un’attività. (TGT-47878)
* È stato risolto un problema che impediva la corretta visualizzazione delle attività [!UICONTROL Multivariate] (MVT) configurate con il reporting [!UICONTROL Analytics for Target] (A4T). (TGT-47490)
* È stato migliorato il messaggio di avviso visualizzato nel reporting quando un’esperienza senza traffico viene utilizzata come esperienza di controllo. (TGT-47537)
* Sono state aggiunte numerose correzioni di back-end e localizzazione.

### [!DNL Target] Standard/Premium 24.1.1 (22, 23 e 25 gennaio 2024)

Questa versione include i miglioramenti e le correzioni seguenti:

* Nelle attività [!UICONTROL Analytics for Target] (A4T) con metriche dell&#39;obiettivo di ricavo non veniva visualizzato &quot;Ricavi&quot; come nome della colonna e la metrica Ricavi non veniva visualizzata nel formato ($) nei rapporti. Si trattava di un problema estetico che è stato risolto. (TGT-46995)
* È stato risolto un problema che impediva il corretto funzionamento della reportistica degli intervalli di date. (TGT-47396)
* È stato risolto un problema che causava la visualizzazione dello stato errato sulla pagina [!UICONTROL All Activities] dopo che i clienti avevano attivato o disattivato un&#39;attività utilizzando l&#39;icona [!UICONTROL More Actions]. (TGT-47367)
* È stato risolto un problema che impediva la visualizzazione del report [!UICONTROL Important Attributes] per un singolo cliente. (TGT-47272)
* È stato risolto un problema che causava la visualizzazione di un messaggio di “payload non valido” quando un singolo cliente tentava di abilitare “Richiedi autenticazione”. (TGT-47195)
* Sono state aggiornate diverse stringhe localizzate nell’interfaccia utente di [!DNL Target].

## Note sulla versione - 2023

### [!DNL Target] Standard/Premium 23.11.1 (13 e 14 novembre 2023)

Questa versione è pianificata per i seguenti giorni:

* **13 novembre**: area geografica Asia-Pacifico (APAC)
* **14 novembre**: area geografica delle Americhe
* **14 novembre**: area geografica Europa, Medio Oriente e Africa (EMEA)

Questa versione include i miglioramenti e le correzioni seguenti:

* Miglioramento della funzionalità di controllo qualità [Attività](/help/main/c-activities/c-activity-qa/activity-qa.md) per supportare [offerte duplicate](/help/main/c-activities/t-automated-personalization/managing-exclusions.md) per esperienze in [!UICONTROL Automated Personalization] attività. (TGT-46627)
* È stata aggiunta una descrizione nell’interfaccia utente di [!DNL Target] per aiutare la clientela a comprendere il motivo per cui potrebbero non essere disponibili dati nei rapporti sulle attività, se non viene allocato traffico all’esperienza di controllo. Nella descrizione è incluso un collegamento a ulteriori informazioni: [Perché non sono disponibili dati per il rapporto della mia attività?](/help/main/c-reports/reporting-frequently-asked-questions.md#section_E4722F6445884130951DF79981C8289B). (TGT-46610)
* È stato risolto un problema che impediva la corretta visualizzazione delle attività nella pagina [!UICONTROL Activities] per alcuni clienti. (TGT-46830)
* Sono stati risolti i seguenti problemi che interessavano le attività che utilizzano [[!UICONTROL Analytics for Target]](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) come origine per la generazione di rapporti:
   * È stato risolto un problema che impediva ad alcuni clienti di visualizzare i dati di reporting. (TGT-46557)
   * È stato risolto un problema che a volte impediva il corretto funzionamento del collegamento [!UICONTROL View in Analytics] nelle pagine di reporting delle attività. (TGT-46731)
   * È stato risolto un problema che impediva la corretta visualizzazione dei dati per [!UICONTROL Lift] e [!UICONTROL Confidence] nell&#39;interfaccia utente di [!DNL Target]. (TGT-46592, TGT-46554, TGT-46586)

### Aggiornamento dell&#39;interfaccia utente della pagina [!UICONTROL Activities] (25 ottobre 2023)

Come parte degli sforzi continui del team [!DNL Adobe Target] per migliorare l&#39;esperienza utente per [!DNL Target] utenti, questa versione aggiorna la pagina [!UICONTROL Activities] nell&#39;interfaccia utente [!DNL Target]. Questo aggiornamento unisce e standardizza i modelli di progettazione precedentemente incoerenti, aggiungendo allo stesso tempo nuovi miglioramenti.

A partire da mercoledì 25 ottobre, una percentuale di clienti avrà accesso alla nuova interfaccia utente e altri clienti potranno accedervi nei giorni successivi.

Per ulteriori informazioni, consulta [Attività](/help/main/c-activities/activities.md).

### [!DNL Target] Standard/Premium 23.10.2 (24 ottobre 2023)

Questa versione include i miglioramenti e le correzioni seguenti:

* È stata migliorata la nuova interfaccia utente [!UICONTROL Activities] in modo che [!UICONTROL Visual Experience Composer] (VEC) si apra con le impostazioni predefinite per `selectorCriteria` durante la creazione di una nuova attività. (TGT-46586)
* È stato risolto un problema che impediva ad alcuni clienti di modificare elementi in modalità [!UICONTROL Composer] durante l&#39;utilizzo del Compositore esperienza visivo. (TGT-46470)
* È stata aggiunta la possibilità di specificare un selettore preferito generico quando si utilizzano attributi personalizzati. (TGT-46545)
* È stato risolto un problema che a volte impediva la visualizzazione di un report [!UICONTROL Auto-Target] che utilizza [!UICONTROL Analytics for Target] (A4T) nell&#39;interfaccia utente [!DNL Target], anche se il report veniva visualizzato correttamente in [!DNL Adobe Analysis Workspace]. (TGT-46494)
* Sono state aggiornate diverse stringhe localizzate nell’interfaccia utente di Target. (TGT-18899)

### [!DNL Target] Standard/Premium 23.9.4 (4-6 ottobre 2023)

Questa versione include i miglioramenti e le correzioni seguenti:

| Funzione | Dettagli |
| --- | --- |
| Pattern di implementazione di [!DNL Recommendations] | Gli articoli *Pattern di implementazione di Recommendations tramite at.js* contribuiscono a comprendere e creare l’implementazione di [!DNL Adobe Target Recommendations] quando si utilizza la libreria JavaScript at.js.<P>Per ulteriori informazioni, consulta [Schema di implementazione di Recommendations utilizzando la panoramica di at.js](https://experienceleague.adobe.com/docs/target-dev/developer/implementation-patterns/atjs/recs-implementation-pattern-atjs.html?lang=it){target=_blank} nella *Guida per gli sviluppatori di Adobe Target*. |

* Sono stati aggiunti [!UICONTROL Visual Experience Composer] miglioramenti (VEC) per i framework dinamici. (TGT-44064)
* È stato risolto un problema che causava un aggiornamento non corretto alla data selezionata nella richiesta `getViewInAnalyticsId`. Questa correzione consente di ricalcolare il collegamento di [!DNL Analytics] nel reporting quando vengono modificate le impostazioni dei rapporti relativi alle metriche e agli intervalli di date. (TGT-46246)

### [!DNL Target] Standard/Premium 23.9.3 (18 settembre 2023)

Questa versione include i miglioramenti e le correzioni seguenti:

* Miglioramento di [!UICONTROL Visual Experience Composer] (VEC) per il supporto di Lightning Web Components (Light DOM). (TGT-45422)
* È stato risolto un problema che causava l’applicazione delle azioni VEC in un ordine errato. In alcuni casi, il Compositore esperienza visivo ha applicato alcune modifiche in modo asincrono e l’aggiunta di modifiche aggiuntive a un elemento ha causato errori se tale elemento viene visualizzato dopo un’azione [!UICONTROL Insert]. Corregge anche l’URL del VEC, che ora si aggiorna quando si clicca sui collegamenti di ancoraggio. (TGT-45983)
* È stato risolto un problema relativo alla funzione VEC [!UICONTROL Overlay], che ora supporta gli elementi nei DOM shadow. (TGT-45202 e TGT-45262)
* È stato risolto un problema che si verificava all’apertura di una pagina Applicazione a pagina singola nel Compositore esperienza visivo, quando si passava alla modalità [!UICONTROL Browse], causava il malfunzionamento delle frecce Indietro e Avanti. (TGT-45956)
* È stato risolto un problema che impediva il caricamento di alcune pagine web nel VEC. (TGT-45983)

### [!DNL Target] Standard/Premium 23.9.2 (12-14 settembre 2023)

Questa versione include i miglioramenti e le correzioni seguenti:

* È stata modificata l’API di [!DNL Analytics] per la nuova versione 2.0 API di [!DNL Analytics]. (TGT-45345)
* Sono stati risolti i problemi che hanno interessato le attività di [!UICONTROL Automated Personalization] (AP) per alcuni clienti, inclusa la sincronizzazione tempestiva dell&#39;attività nel backend di [!DNL Target] e la distribuzione dell&#39;esperienza prevista nei collegamenti di anteprima. (TGT-46202)

### [!DNL Target] Standard/Premium 23.9.1 (6-11 settembre 2023)

Questa versione include i miglioramenti e le correzioni seguenti:

* È stato risolto un problema che causava dati di reporting incoerenti nell&#39;interfaccia utente [!DNL Target] e nell&#39;interfaccia utente [!DNL Adobe Analytics] per le attività [!UICONTROL Auto-Allocate] che utilizzano [!UICONTROL Analytics for Target] (A4T) come origine per la generazione di rapporti. (TGT-46112)
* Il timeout per le chiamate PUT all’API di consegna di Target è stato aumentato a 15 secondi, per evitare errori di timeout. (TGT-46091)
* È stato corretto un problema che impediva l’aggiornamento costante dell’URL durante la navigazione nel sito web di un’applicazione a pagina singola (SPA). (TGT-45417)

### Aggiornamento pianificato dell’infrastruttura Edge di [!DNL Adobe Target]  {#edge}

A causa dell’aggiornamento pianificato dell’infrastruttura Edge, è necessario inserire nell’elenco Consentiti indirizzi IP o domini aggiuntivi. Consulta i domini NAT e IP per le distribuzioni Edge 41-48 e inseriscili nell’elenco Consentiti. Gli aggiornamenti dell’infrastruttura iniziano il 9 agosto 2023.

Per ulteriori informazioni, vedere [Inserire nell&#39;elenco Consentiti i nodi edge di Target](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/privacy/allowlist-edges.html?lang=it){target=_blank} nella *Guida per gli sviluppatori di Adobe Target*.

### [!DNL Target] Standard/Premium 23.8.1 (9 agosto 2023)

Questa versione include i miglioramenti e le correzioni seguenti:

* È stato risolto un problema che a volte impediva la corretta sincronizzazione delle attività, come mostrato nella colonna &quot;[!UICONTROL Status]&quot; nella pagina dell&#39;elenco [!UICONTROL Activity]. (TGT-46010 e TGT-44831)
* È stato risolto un problema che a volte impediva la visualizzazione del collegamento &quot;[!UICONTROL View in Analytics]&quot; nella pagina [!UICONTROL Reports] delle attività che utilizzano [!UICONTROL Analytics for Target] (A4T) come origine per la generazione di rapporti. (TGT-45808)
* È stata corretta la presentazione di valori in tabelle, in modo da visualizzarli come percentuali anziché come numeri con decimali. Ad esempio, 8% invece di 0,08. (TGT-45548)
* È stato risolto un problema che impediva ai clienti di utilizzare lo stato attivo sulla tastiera per passare all&#39;elemento successivo nella pagina [!UICONTROL Goals & Settings] per le attività [!UICONTROL Experience Targeting] (XT). (TGT-44526)
* È stato risolto un problema che causava la perdita dello stato attivo della tastiera dopo l&#39;apertura della finestra di dialogo &quot;[!UICONTROL Add audiences]&quot; durante la creazione di un&#39;attività. (TGT-44525)

### [!DNL Target] Standard/Premium 23.7.1 (24-26 luglio)

Questa versione include i miglioramenti e le correzioni seguenti:

* È stata migliorata la ricerca durante l&#39;esplorazione di [elementi utilizzando il percorso DOM](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path) nel [!UICONTROL Visual Experience Composer] (Compositore esperienza visivo) per includere elementi DOM shadow. (TGT-45262)
* È stato risolto un problema che impediva il corretto funzionamento delle impostazioni [Cambia sovrapposizione](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md). (TGT-45202)
* È stato risolto un problema a causa del quale alcuni clienti ricevevano il messaggio di errore “L’utente non è autorizzato ad accedere al rapporto” e non potevano scaricare i rapporti delle attività. (TGT-45724 e TGT-45747)

### [!DNL Target] Standard/Premium 23.6.1 (27-29 giugno)

Questo rilascio contiene i seguenti miglioramenti:

| Funzione | Dettagli |
|--- |--- |
| [!UICONTROL QA mode] per [!UICONTROL Automated Personalization] attività | [!DNL Adobe Target] [!UICONTROL QA mode] è ora disponibile per le attività [!UICONTROL Automated Personalization], sostituendo la funzionalità [!UICONTROL Preview links].<P>Per ulteriori informazioni, consulta [Controllo qualità delle attività](/help/main/c-activities/c-activity-qa/activity-qa.md). |

* Miglioramenti delle prestazioni per non consentire la funzionalità di duplicazione (inclusa la riduzione del tempo di caricamento) durante la [gestione delle esclusioni](/help/main/c-activities/t-automated-personalization/managing-exclusions.md#concept_4EF78013F80E48EFA024AE0274C9F037) in [!UICONTROL Automated Personalization] attività.

### [!DNL Target] Standard/Premium 23.5.2 (31 maggio 2023)

Questa versione include i miglioramenti e le correzioni seguenti:

* È stato risolto un problema che causava la visualizzazione di una pagina vuota durante la generazione di un token di autorizzazione di un profilo API. (TGT-45387 e TGT-45423)
* È stato risolto un problema che impediva la visualizzazione di un&#39;immagine nel pannello [!UICONTROL Create Design] se il nome dell&#39;immagine conteneva GB 18030 caratteri. (TGT-44614)
* È stato risolto un problema a causa del quale in alcuni caratteri dei simboli GB 18030 veniva erroneamente applicato l’escape nel testo/HTML nelle esperienze. (TGT-44600)
* È stato risolto un problema che causava il blocco dei report per [!UICONTROL Auto Personalization] attività durante l&#39;analisi. (TGT-44820)
* È stato risolto un problema che impediva la ricerca di un&#39;attività nella pagina [!UICONTROL Activity] se il nome dell&#39;attività conteneva una parentesi quadra ( [or] ). (TGT-44777)
* È stato risolto un problema che impediva la sincronizzazione di un’attività se il relativo obiettivo conteneva caratteri speciali. (TGT-44982)
* È stato risolto un problema che impediva ad alcuni clienti la visualizzazione delle attività nell’interfaccia utente di [!DNL Target] per l’area di lavoro predefinita. (TGT-45286)
* È stato aggiornato il comportamento del flag “Disabilita duplicati”. I flag di esclusione offerte ripetute sono stati aggiornati per consentire tali offerte in caso di offerta di contenuto predefinita (per API v3 e v4) e per consentire le opzioni duplicate se tali opzioni fanno riferimento all’offerta di contenuto predefinita e non hanno modelli definiti. (TNT-46617)
* È stato risolto un problema a causa del quale un parametro di query veniva aggiunto a un URL e non consentiva il caricamento della pagina nel Compositore esperienza visivo [!UICONTROL Visual Experience Composer]. (TGT-44873)
* Sono state apportate diverse correzioni di localizzazione in tutta l’interfaccia utente di [!DNL Target].

### Attributi del profilo di Real-Time CDP condivisi con [!DNL Target] [!UICONTROL Real-Time CDP Profile Attributes] (13 giugno 2023)

Questa versione contiene i seguenti miglioramenti:

| Funzione | Dettagli |
|--- |--- |
| Attributi di profilo Real-Time CDP condivisi con [!DNL Target] | [!UICONTROL Real-Time CDP Profile Attributes] può essere condiviso con [!DNL Target] per l&#39;utilizzo in offerte HTML e JSON.<P>Per ulteriori informazioni, consulta [Condividere gli attributi di profilo Real-Time CDP con [!DNL Target]](/help/main/c-integrating-target-with-mac/integrating-with-rtcdp.md#rtcdp-profile-attributes). |

### [!DNL Target] Standard/Premium 23.5.1 (23-25 maggio 2023)

Questa versione include i nuovi miglioramenti e le correzioni seguenti:

* È stato risolto un problema che impediva ad alcuni clienti di creare tipi di pubblico con profili di visitatori utilizzando gli operatori “maggiore di” o “minore di”. (TGT-45271)
* Sono state apportate diverse correzioni di localizzazione in tutta l’interfaccia utente di [!DNL Target].
* L’interfaccia utente di Target è stata aggiornata in diverse posizioni in vista di un prossimo aggiornamento (le modifiche sono dietro un flag di funzione fino al rilascio degli aggiornamenti).

### [!DNL Target] Standard/Premium 23.4.1 (25-27 aprile 2023)

Questa versione contiene aggiornamenti di sicurezza e le seguenti nuove funzioni:

| Funzione | Dettagli |
|--- |--- |
| AEM [!UICONTROL Content Fragments] per personalizzazione e sperimentazione headless | Utilizza [!DNL Adobe Experience Manager] (AEM) [!UICONTROL Content Fragments] in [!DNL Target] attività. Combina la facilità d’uso e la potenza di AEM con le potenti capacità dell’intelligenza artificiale (IA) e dell’apprendimento automatico (ML) in [!DNL Target] per facilitare la personalizzazione e la sperimentazione headless.<P>Per ulteriori informazioni, vedere [AEM [!UICONTROL Content Fragments]](/help/main/c-integrating-target-with-mac/aem/content-fragments-aem.md). |
| [*Guida per gli sviluppatori di Adobe Target*](https://experienceleague.adobe.com/docs/target-dev/developer/overview.html?lang=it){target=_blank} | La *Guida per gli sviluppatori di Adobe Target* è stata trasferita in *[!UICONTROL Adobe Experience League]*. Il passaggio a *[!UICONTROL Experience League]* facilita la localizzazione del testo in altre lingue, unifica la ricerca in *Experience League* per estendere e offrire i risultati di ricerca sia da *[!UICONTROL Adobe Target Business Practitioner Guide]* che da *[!UICONTROL Adobe Target Developer Guide]* e offre ulteriori vantaggi.<P>Verrai reindirizzato automaticamente dal percorso precedente a *[!UICONTROL Experience League]*. Aggiorna i segnalibri secondo necessità. |

### [!DNL Target] Standard/Premium 23.3.1 (28-30 marzo 2023)

Questa versione include le nuove funzioni, i miglioramenti e le correzioni seguenti:

| Funzione | Dettagli |
|--- |--- |
| Metriche A4T ottimizzate per [!UICONTROL Auto-Allocate] e [!UICONTROL Auto-Target]<p>(Data di rilascio: 30 marzo 2023) | [!DNL Target] consente di scegliere metriche basate su eventi binomiali o metriche basate su eventi continui quando si utilizza [!UICONTROL A4T] per le attività [!UICONTROL Auto-Allocate] e [!UICONTROL Auto-Target].<P>In particolare, tieni conto delle seguenti modifiche nelle metriche supportate:<ul><li>[!DNL Target] ha mantenuto il comportamento precedente per le attività esistenti fino al 9 settembre 2023. Dopo tale data, le attività che utilizzando le metriche non supportate verranno interrotte e sarà necessario effettuarne la migrazione ai nuovi comportamenti.</li></ul>Per ulteriori informazioni, vedere &quot;Metriche obiettivo supportate&quot; in [Supporto A4T per [!UICONTROL Auto-Allocate] e [!UICONTROL Auto-Target] attività](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md#supported).<br>Con questa funzione sono stati aggiornati i seguenti tutorial:<ul><li>[Configurazione dei rapporti A4T in [!DNL Analysis Workspace] per [!UICONTROL Auto-Allocate] attività](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-allocate-activities.html?lang=it){target=_blank}</li><li>[Configurazione dei rapporti A4T in [!DNL Analysis Workspace] per [!UICONTROL Auto-Target] attività](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html?lang=it){target=_blank}</li></ul> |

* Miglioramento della sincronizzazione del pubblico e delle attività in modo che gli elementi creati in [!DNL Adobe Experience Platform] e [!DNL Adobe Audience Manager] siano disponibili più rapidamente nell’interfaccia di [!DNL Target]. (TGT-44568)
* Interfaccia utente migliorata per consentire agli utenti di rimuovere [!UICONTROL Default URL] in [!UICONTROL Administration] > [!UICONTROL Visual Experience Composer] > [!UICONTROL Default URL]. Questa modifica consente ai clienti di impostare di nuovo l’URL predefinito su una stringa vuota, cosa che in precedenza non era possibile dopo la configurazione iniziale. (TGT-44577)
* Sono state rimosse le restrizioni che impedivano di modificare o eliminare i tipi di pubblico predefiniti (tipi di pubblico con nomi riservati). (TGT-44655)
* Disabilitata l&#39;opzione &quot;[!UICONTROL Done]&quot; durante il caricamento degli spinner, era visibile nell&#39;interfaccia utente [!DNL Target] durante la creazione di [tipi di pubblico combinati](/help/main/c-target/combining-multiple-audiences.md). (TGT-44079)
* È stato corretto il collegamento [!UICONTROL Language] nella parte inferiore della pagina [!UICONTROL Audiences] in modo che si colleghi correttamente alla pagina &quot;[!UICONTROL Account communication preferences]&quot;. (TGT-43562)
* È stato risolto un problema che a volte impediva ai clienti di creare [!UICONTROL A/B Test] attività dopo aver selezionato l&#39;opzione [!UICONTROL Adobe Analytics] in [!UICONTROL Administration] > [!UICONTROL Reporting] > [!UICONTROL Reporting Experience Cloud Solution]. (TGT-44844)
* È stato risolto un problema che impediva ai clienti di visualizzare l&#39;ultima esperienza in un&#39;attività [!UICONTROL Multivariate Test] con molte esperienze all&#39;interno del [!UICONTROL Visual Experience Composer] (VEC). Il [percorso DOM](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path) nella parte inferiore del Compositore esperienza visivo a volte impediva ai clienti di visualizzare l’ultima esperienza. (TGT-44578)
* È stato risolto un problema a causa del quale l’URL di navigazione nel Compositore esperienza visivo non rifletteva la pagina corrente visibile in una normale sessione del browser se la pagina richiedeva un’autorizzazione o richiamava reindirizzamenti. (TGT-44350)
* È stato risolto un problema che impediva ai clienti di modificare l&#39;impostazione [!UICONTROL Filter Incompatible Criteria] in [!UICONTROL Recommendations] > [!UICONTROL Settings]. (TGT-44398)
* È stato risolto un problema che impediva la creazione di feed [!DNL Recommendations] da parte di richieste POST durante l&#39;utilizzo di [!UICONTROL Analytics Classifications] con suite di rapporti il cui nome conteneva punti. (TGT-44598)
* I collegamenti nell’interfaccia di [!DNL Target] sono stati aggiornati per puntare alla nuova [estensione Visual Editing Helper](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md). (TGT-44459)
* Protezione avanzata per impedire tentativi di falsificazione di richieste lato server (SSRF) nei feed di [!DNL Recommendations]. (TGT-43769)
* Sono state apportate diverse correzioni di localizzazione in tutta l’interfaccia utente di [!DNL Target].

### at.js versione 2.10.2 (7 marzo 2023)

* È stato risolto un problema che causava la restituzione di un errore della funzione `trackEvent`.

Per informazioni su tutte le versioni di at.js, consulta [Dettagli sulla versione di at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank} nella [Guida per gli sviluppatori di Adobe Target](https://experienceleague.adobe.com/docs/target-dev/developer/overview.html?lang=it){target=_blank}.

### [!DNL Target] Standard/Premium 22.15.1 (8-9 marzo 2023)

Questa versione sarà disponibile in base al seguente programma scaglionato:

* **8 marzo**: area geografica delle Americhe
* **9 marzo**: area geografica Europa, Medio Oriente e Africa (EMEA)
* **9 marzo**: area geografica Asia Pacifico (APAC)

Questa versione include le seguenti correzioni:

* Aggiornamenti per la creazione di componenti Web personalizzati con [!UICONTROL Visual Experience Composer] (VEC):

   * È stata corretta la selezione di elementi shadow DOM nel Compositore esperienza visivo, ottimizzando il processo di authoring in modo che non vi sia alcuna dipendenza dal tipo di implementazione di [!DNL Target] durante la creazione della radice shadow. Ora, la selezione di elementi shadow DOM nel Compositore esperienza visivo dovrebbe funzionare per qualsiasi sito web.
   * È stato risolto un problema che impediva il caricamento di elementi HTML utilizzando #Shadow DOM nel Compositore esperienza visivo. (TGT-35801)
   * Sono stati risolti alcuni problemi del Compositore esperienza visivo che si verificavano con siti web SPA che utilizzano ShadowDOM. (TGT-43169)
   * È stato risolto un problema relativo all’obiettivo di ottimizzazione “clic su un elemento” che non identificava correttamente il selettore CSS in ShadowDOM.

>[!NOTE]
>
>Per garantire il recapito delle modifiche create nel Compositore esperienza visivo, assicurati di utilizzare un SDK [!DNL Target] ([at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank} o [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=it){target=_blank} (alloy.js)) con una versione successiva alla 2.8.

**Problema noto**: il tracciamento dei clic su un elemento radice shadow durante l’utilizzo di [!DNL Adobe Experience Platform Web SDK] non funziona correttamente. (TNT-47012)

### at.js versione 2.10.2 (7 marzo 2023)

* È stato risolto un problema che causava la restituzione di un errore della funzione `trackEvent`.

Per informazioni su tutte le versioni di at.js, consulta [Dettagli sulla versione di at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank} nella [Guida per gli sviluppatori di Adobe Target](https://experienceleague.adobe.com/docs/target-dev/developer/overview.html?lang=it){target=_blank}.

### [!DNL Target] Standard/Premium 22.14.5 (13-15 febbraio 2023)

Questa versione sarà disponibile in base al seguente programma scaglionato:

* **13 febbraio**: area geografica delle Americhe
* **15 febbraio**: area geografica Europa, Medio Oriente e Africa (EMEA)
* **15 febbraio**: area geografica Asia-Pacifico (APAC)

Questa versione include le seguenti correzioni:

* È stato risolto un problema che causava il seguente messaggio di errore, anche se una proprietà era specificata nelle attività di Automated Personalization (AP): “Errori: almeno una proprietà deve appartenere a un’area di lavoro non predefinita” (TGT-44607)
* È stato risolto un potenziale problema di sicurezza che influiva sui feed di Recommendations lato server. (TGT-43769)

### at.js versione 2.10.1 (2 febbraio 2023)

* È stato corretto un bug a causa del quale le attività che coinvolgono regole di pubblico contenenti parametri nel cui nome è presente il carattere punto non restituivano l’esperienza prevista per le decisioni sul dispositivo.
* È stato corretto un bug introdotto in at.js 2.6.0 a causa del quale at.js attivava una chiamata di consegna, anche quando `mboxDisable` era abilitato.

Per informazioni su tutte le versioni di at.js, consulta [Dettagli sulla versione di at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank} nella [Guida per gli sviluppatori di Adobe Target](https://experienceleague.adobe.com/docs/target-dev/developer/overview.html?lang=it){target=_blank}.

### [!DNL Target] Standard/Premium 22.13.3 (25-26 gennaio 2023)

Questa versione sarà disponibile in base al seguente programma scaglionato:

* **25 gennaio**: area geografica Europa, Medio Oriente e Africa (EMEA)
* **25 gennaio**: area geografica Asia-Pacifico (APAC)
* **26 gennaio**: area geografica delle Americhe

Questa versione include le nuove funzioni, i miglioramenti e le correzioni seguenti:

| Funzione | Dettagli |
| --- | --- |
| [Offerta JSON](/help/main/c-experiences/c-manage-content/create-json-offer.md) per il supporto in Automated Personalization (AP) | È stato aggiunto il supporto per le offerte JSON nelle attività [!UICONTROL Automated Personalization] (AP) tramite il Compositore esperienza basato su moduli. (TGT-41460) |
| [Frammenti di esperienza AEM](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md) | È stata aggiunta la possibilità di distinguere tra tipi di frammento di [!DNL Adobe Experience Manager] (AEM XF) esportati in [!DNL Target]. Invece dell’opzione “Frammento esperienza”, [!DNL Target] ora consente di filtrare e cercare i dati utilizzando “HTML XF” e “JSON XF”. (TGT-44132) |

* È stato risolto un problema che causava un &quot;errore 500&quot; nelle attività [!UICONTROL A/B Test] e [!UICONTROL Experience Targeting] (XT) che contenevano consigli. Questo problema si verificava quando [!DNL Target] non riusciva a eliminare correttamente gli oggetti di criteri dall’interfaccia utente di [!DNL Target] e dal back-end di [!DNL Recommendations] non più in uso. (TGT-44383)
* Rimozione della posizione dal nome dell&#39;offerta visualizzato nel report [!UICONTROL Offer Level] per le attività [!UICONTROL Automated Personalization]. Questa modifica rende il rapporto più leggibile. (TGT-44294)
* Sono state rimosse le opzioni del calendario di 45 giorni e 90 giorni da AP e dai report [!UICONTROL Auto-Target] [!UICONTROL Personalization Insights] e [!UICONTROL Important Attributes] nell&#39;interfaccia utente [!DNL Target]. A causa dei pattern di utilizzo e nel tentativo di migliorare le prestazioni, questi intervalli di date sono stati dichiarati obsoleti. L’interfaccia utente è stata aggiornata per riflettere gli intervalli attualmente consentiti: 15, 30 e 60 giorni. (TGT-39357)
* Impossibile modificare l&#39;impostazione [!UICONTROL Same as Optimization Goal] nella pagina [!UICONTROL Goals & Settings] dopo che l&#39;attività è in esecuzione. (TGT-43923)
* È stato risolto un problema che causava errori con l’ambiente di lavoro predefinito nel back-end di [!DNL Target] in caso di aggiornamento da [!DNL Target Standard] a [!DNL Target Premium]. (TGT-44081 e TGT-44306)
* È stata apportata una modifica per consentire le suite di rapporti di [!DNL Analytics] che contengono il carattere punto “.” nei nomi da utilizzare nell’interfaccia utente di [!DNL Target] per creare feed di classificazione in [!DNL Analytics].
* È stato modificato il collegamento nella pagina [!UICONTROL Implementation] ([!UICONTROL Administration] > [!UICONTROL Implementation]) per &quot;Metodi di implementazione con decisioning sul dispositivo&quot; in modo che faccia riferimento alla pagina che spiega come utilizzare il decisioning sul dispositivo per tutti gli SDK supportati: Node.js, Java, .NET e Python. Per ulteriori informazioni, consulta [Guida introduttiva agli SDK di Target](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/getting-started.html?lang=it){target=_blank} nella [Guida per gli sviluppatori di Adobe Target](https://experienceleague.adobe.com/docs/target-dev/developer/overview.html?lang=it){target=_blank}.
* È stato risolto un problema che causava errori durante il caricamento dei file utilizzando [!DNL Scene7] e [!DNL Target].
* È stata migliorata l’accessibilità dell’interfaccia utente di [!DNL Target] per le persone con disabilità utilizzando i risultati di una verifica interna in termini di usabilità. I miglioramenti dell’accessibilità includono l’accesso a funzioni che in precedenza non erano raggiungibili tramite la tastiera, miglioramenti al testo alternativo, la possibilità di eseguire lo zoom di parti dell’interfaccia utente per renderle più utilizzabili, l’attivazione della tastiera migliorata e molto altro ancora.   (TGT-42759)
* Sono state apportate diverse correzioni di localizzazione in tutta l’interfaccia utente di [!DNL Target].

## Note sulla versione - 2022

### Rilascio di Models API (23 novembre 2022)

Le nuove Models API di [!DNL Adobe Target], dette anche API di Inserisce nell&#39;elenco Bloccati di di, consentono agli utenti di visualizzare e gestire l&#39;elenco delle funzionalità utilizzate nei modelli di apprendimento automatico per le attività [!UICONTROL Automated Personalization] (AP) e [!UICONTROL Auto-Target] (AT).

Per ulteriori informazioni, vedere [Panoramica di Models API](https://experienceleague.adobe.com/docs/target-dev/developer/api/models-api/models-api.html?lang=it){target=_blank} nella *Guida per gli sviluppatori di Adobe Target*.

### [!DNL Target] Standard/Premium 22.10.3 (rilascio scaglionato dal 25 al 27 ottobre 2022)

Questa versione include le seguenti correzioni:

* Sono state aggiunte descrizioni comando nell’interfaccia utente di [!DNL Target] per consentire ai clienti di navigare nel generatore di pubblico in modo più efficiente e per scoprire come utilizzare funzioni che potrebbero non essere familiari. (TGT-44139)
* È stata aggiunta una funzionalità per impedire ai clienti di modificare un’attività disabilitata da [!DNL Target] perché utilizza metriche non supportate. Un messaggio nell’interfaccia utente indica ai clienti di duplicare l’attività e quindi aggiornare la metrica di conversione.

  Con questa versione le metriche `averagetimespentonsite`, `bouncerate` e `entries` nelle attività di [!DNL Target] diventeranno obsolete per le nuove attività. Le attività esistenti possono continuare a utilizzare tali metriche fino a maggio 2023.

* È stata aggiunta una descrizione comando nell&#39;interfaccia utente [!DNL Target] per consentire ai clienti di selezionare un criterio di ottimizzazione durante la creazione o la modifica di un&#39;attività [!UICONTROL Auto-Target] che utilizza A4T.

### [!DNL Target] Standard/Premium 22.10.1 (rilascio scaglionato dal 10 al 13 ottobre 2022)

Questa versione include le nuove funzioni, i miglioramenti e le correzioni seguenti:

| Funzione | Dettagli |
| --- | --- |
| [!DNL Adobe Experience Manager] Frammenti esperienza (AEM) | Gli aggiornamenti relativi alla funzionalità dei frammenti di esperienza AEM includono:<ul><li>È stata aggiunta la possibilità di filtrare i Frammenti di esperienza di AEM per tipo (HTML o JSON) nell&#39;elenco [!UICONTROL Offers]. (TGT-43121)</li><li>È stato risolto un problema che consentiva ai clienti di inserire offerte JSON [!UICONTROL Experience Fragment] utilizzando il Compositore esperienza visivo (VEC), azione che non è supportata. Le offerte JSON possono essere inserite solo utilizzando il compositore [!UICONTROL Form-Based Experience]. (TGT-43846)</li></ul>Per ulteriori informazioni, consulta i [Frammenti esperienza AEM](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md). |
| Nuova estensione [!UICONTROL Visual Experience Composer] per Google Chrome | Una nuova estensione [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) per Chrome è disponibile in Chrome Web Store.<br>A partire dal mese di gennaio 2023, l’attuale estensione [!DNL Target] VEC Helper cesserà di funzionare in Google Chrome perché Google non consentirà l’utilizzo di estensioni basate su Manifest V2. Scarica la nuova estensione per continuare a creare visivamente i tuoi siti web in [!DNL Target] a partire dal nuovo anno.<br>I seguenti collegamenti mostrano le due estensioni nel Chrome Web Store:<ul><li>[Nuova estensione](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target=_blank}</li><li>[Estensione precedente](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak){target=_blank}</li></ul>Per ulteriori informazioni, consulta [Estensione Helper per editing video](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md). |

* È stato risolto un problema che impediva la corretta visualizzazione delle informazioni sulle regole del pubblico nella finestra delle informazioni di [!UICONTROL Audiences Refinements]. (TGT-43917)
* Sono state migliorate le prestazioni dell’interfaccia utente di [!DNL Target] durante il caricamento dei tipi di pubblico che si avvicinano al [limite consigliato per le regole di targeting](/help/main/r-troubleshooting-target/target-limits.md#targeting-rules). (TGT-43675)
* È stato risolto un problema che impediva la corretta visualizzazione di alcuni componenti nel pannello [!UICONTROL Modifications] della pagina [!UICONTROL Experiences] durante la creazione o la modifica di attività nel Compositore esperienza visivo dopo il passaggio dalla modalità [!UICONTROL Compose] alla modalità [!UICONTROL Browse]. (TGT-43300)
* È stato risolto un problema che impediva ad alcuni clienti di archiviare [!UICONTROL A/B Test] attività che utilizzano [!UICONTROL Auto-Target]. (TGT-40978)
* È stata aggiunta la possibilità di utilizzare automaticamente un’unica offerta in più posizioni all’interno di un singolo gruppo di reporting. (TGT-40689)

### [!DNL Target] Standard/Premium 22.9.1 (rilascio scaglionato dal 13 all’15 settembre 2022)

Questa versione sarà disponibile in base al seguente programma scaglionato:

* **13 settembre**: area geografica Europa, Medio Oriente e Africa (EMEA)
* **14 settembre**: area geografica delle Americhe
* **15 settembre**: area geografica Asia-Pacifico (APAC)

Questa versione include i miglioramenti e le correzioni seguenti:

* È stata aggiunta l’opzione [!UICONTROL Cross-Domain] per il download di at.js 2.10.0 (e versioni successive) per consentire o disabilitare l’impostazione di cookie di terze parti. (TGT-43674)
* Sono state aggiornate le notifiche nell’interfaccia utente di [!DNL Target] per informare i clienti nel caso in cui l’importazione di feed [!DNL Recommendations] non riesca. (TGT-35811)
* È stato risolto un problema che impediva il corretto funzionamento di [!UICONTROL Decision Offers] all&#39;interno di [!UICONTROL Visual Experience Composer] (VEC). (TGT-43866)
* È stato risolto un problema che causava la visualizzazione di un messaggio di errore durante la selezione dell&#39;obiettivo di conversione [!UICONTROL Clicked an Element] durante la creazione di un&#39;attività [!UICONTROL Multivariate Testing] (MVT). (TGT-43842)
* È stato risolto un problema che impediva la visualizzazione della colonna [!UICONTROL Impressions] nel file di rapporto CSV scaricato per le attività [!UICONTROL Automated Personalization] (AP). (TGT-43780)
* È stato risolto un problema che impediva ai clienti di modificare le offerte HTML/JSON dopo la duplicazione delle esperienze durante l&#39;utilizzo di [!UICONTROL Form-Based Experience Composer]. (TGT-43633)
* È stato risolto un problema che impediva ai clienti di copiare un&#39;attività [!UICONTROL A/B Test] da un&#39;area di lavoro non predefinita a un&#39;altra area di lavoro non predefinita. (TGT-41910)
* È stato risolto un problema che impediva ai clienti di visualizzare correttamente gli utilizzi di [!DNL Recommendations] oggetti (progettazioni, criteri, raccolte e così via) nelle attività [!UICONTROL A/B Test] e [!UICONTROL Experience Targeting] (XT) che contengono consigli, nonché di eliminare gli oggetti criteri non più in uso dall&#39;interfaccia utente [!DNL Target] e dal back-end [!DNL Recommendations]. (TGT-42331)
* È stato risolto un problema che causava la visualizzazione di un avviso di timeout di rete nell’[!DNL Target] Interfaccia utente per il recupero dei parametri. (TGT-43737)
* Sono stati apportati aggiornamenti all’interfaccia utente per garantire che alcune azioni di trascinamento della selezione siano accessibili da tastiera. (TGT-42969)
* Sono stati apportati aggiornamenti all’interfaccia utente per garantire che le stringhe di testo siano localizzate correttamente.

### at.js versione 2.10.0 (13 settembre 2022)

* È stata aggiunta l’opzione [!UICONTROL Cross-Domain] per il download di at.js 2.10.0 (e versioni successive) per consentire o disabilitare l’impostazione di cookie di terze parti. (TGT-43674)

### [!DNL Target Standard/Premium] 22.8.1 (rilascio graduale 17-18 agosto 2022)

Questa versione di manutenzione include correzioni di back-end e localizzazione.

### Versione della piattaforma [!DNL Target] (20 luglio 2022)

Questa versione include i miglioramenti e le correzioni seguenti:

| Funzione | Descrizione |
| --- | --- |
| Miglioramento della precisione di valutazione del pubblico e riduzione della latenza per l’utente finale tramite il supporto IPv6 (TNT-43364, TNT-44692) | Le geolocalizzazioni dei visitatori ora sono determinate dagli indirizzi IPv6, se disponibili, anziché solo dagli indirizzi IPv4. Le API di consegna supportano anche i parametri di input IPv6. I filtri e l’elenco Consentiti supportano sia gli indirizzi IPv4 che IPv6. Grazie al supporto di IPv6 in questa versione, i visitatori verranno inclusi in modo più preciso nei tipi di pubblico (verranno qualificati per le attività o inclusi nei criteri di filtro in modo più accurato). Anche la latenza dei dati risulterà migliorata, in quanto i client IPv6 verranno instradati direttamente, evitando il sovraccarico del gateway IPv6-IPv4. |
| È stato risolto un problema di gestione del payload lato client di A4T (TNT-44926) | Con l’integrazione lato server di A4T, se Adobe Target identifica una richiesta come proveniente da un bot, il payload non viene inoltrato ad Analytics e nei registri di [!DNL Target] non viene registrato alcun evento mod_stats. Con questa versione, la registrazione lato client di A4T è stata migliorata in modo che il comportamento relativo al payload A4T corrisponda a quello lato server di A4T: i visitatori identificati come bot vengono esclusi dal conteggio e dal reporting di [!DNL Target]. (Il problema in questione era limitato alle implementazioni che utilizzavano la gestione del payload lato client; il lato server non ne era interessato. Con questa versione, il comportamento è ora coerente sia per la gestione del payload lato server che per quello lato client.) |

### [!DNL Target Standard/Premium] 22.6.2 (30 giugno 2022)

Questa versione include i miglioramenti e le correzioni seguenti:

| Funzione | Descrizione |
| --- | ---  |
| Notifiche interne al prodotto | Ottieni le seguenti notifiche interne al prodotto:<ul><li>**Attività**: notifiche per tutti i tipi di attività quando un&#39;attività viene approvata o disattivata, manualmente o alla sua data di inizio o di fine. La notifica include il nome dell’attività e un collegamento alla pagina di panoramica dell’attività.</li><li>**Script di profilo**: notifiche quando uno script di profilo viene attivato o disattivato, manualmente o da Target.</li><li>**Feed di Recommendations**: notifiche quando un feed di Recommendations viene attivato o disattivato, manualmente o da Target. Le notifiche vengono inviate anche quando un feed di Recommendations non riesce.</li></ul> Per impostazione predefinita, le notifiche vengono ricevute dagli amministratori di prodotto, e dagli utenti che pubblicano e che approvano. Le notifiche possono essere configurate nelle preferenze di Experience Cloud.<br>Per ulteriori informazioni consulta [Notifiche e annunci](/help/main/c-intro/understand-the-target-ui.md#notifications-announcements). |
| *Guida per gli sviluppatori di Adobe Target* | La *Guida per gli sviluppatori di Adobe Target* consolida tutti i contenuti per sviluppatori di [!DNL Target] in un’unica pratica guida. La guida include informazioni sull’implementazione di [!DNL Target] e [!DNL Recommendations], sugli SDK di [!DNL Target] e sulle API di [!DNL Target].<br>Per ulteriori informazioni, vedere [Guida per gli sviluppatori di Adobe Target](https://experienceleague.adobe.com/docs/target-dev/developer/overview.html?lang=it){target=_blank}. |

* Gli utenti con il ruolo [!UICONTROL Editor] non possono più modificare i tipi di pubblico nelle attività live. (TGT-43582)
* Se un cliente tenta di salvare un pubblico con un punto esclamativo ( ! ) come primo carattere del nome del pubblico (ad esempio !Londra). (TGT-43643)
* È stato risolto un problema a causa del quale alcune schede dei dettagli di definizione del pubblico per alcuni clienti indicavano che un’attività terminata è ancora in esecuzione. (TGT-43527)

### [!DNL Target Standard/Premium] 22.6.1 (rilascio graduale: 7-9 giugno 2022)

Questa versione sarà disponibile in base al seguente programma scaglionato:

* **7 giugno**: area geografica Asia Pacifico (APAC)
* **8 giugno**: area geografica delle Americhe
* **9 giugno**: area geografica Europa, Medio Oriente e Africa (EMEA)

Questa versione include i miglioramenti e le correzioni seguenti:

* È stato introdotto un miglioramento per la nuova pagina [!UICONTROL Audiences] per evitare uno stato incoerente tra il vecchio database, in cui erano precedentemente archiviati i tipi di pubblico, e la nuova architettura, che recupera le informazioni direttamente dal back-end. (TGT-43552)
* È stato risolto un problema che impediva ad alcuni clienti di salvare i tipi di pubblico combinati a causa dell’interfaccia di Target che creava contenitori “vuoti”. (TGT-43588)

### Versione della piattaforma Target (25 maggio 2022)

Questa versione include i miglioramenti e le correzioni seguenti:

* È stato aggiunto il supporto [per i User Agent Client Hints](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/user-agent-and-client-hints.html?lang=it){target=_blank}.
* È stato risolto un problema che causava timeout in modo intermittente durante il rendering di [!UICONTROL Offer Decisions] nelle attività [!UICONTROL Experience Targeting] (XT). (TNT-44611)

### at.js versione 2.9.0 (27 maggio 2022)

* È stato aggiunto il supporto [per i User Agent Client Hints](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/user-agent-and-client-hints.html?lang=it){target=_blank}.
* È stato corretto un errore per cui più richieste di mbox sulla stessa pagina avevano ID di impression diversi.

### [!DNL Target Standard/Premium] 22.5.1 (rilascio scaglionato; 11-13 maggio 2022)

Questa versione sarà disponibile in base al seguente programma scaglionato:

* **11 maggio**: area geografica Asia-Pacifico (APAC)
* **12 maggio**: area geografica delle Americhe
* **13 maggio**: area geografica Europa, Medio Oriente e Africa (EMEA)

Questa versione include i miglioramenti e le correzioni seguenti:

* È stato risolto un problema che causava un errore di JavaScript e impediva ad alcuni clienti di accedere ai dettagli di alcune attività di [!UICONTROL Automated Personalization] (AP). (TGT-43526)
* È stato risolto un problema che impediva ad alcuni clienti di aggiungere (o modificare) un’offerta specifica a un’attività AP. (TGT-43503)
* È stato risolto un problema nell’interfaccia utente di [!DNL Target] a causa del quale veniva visualizzato il seguente messaggio di errore: “La mbox globale potrebbe non essere sincronizzata. Prova a salvarla di nuovo.” Questo problema era relativo alla sola interfaccia utente e non aveva alcun impatto sulle implementazioni dei clienti. (TGT-43475)
* È stato risolto un problema che impediva a un cliente di modificare perfezionamenti e tipi di pubblico a livello di esperienza per un&#39;attività, se questi erano stati creati prima dell&#39;implementazione della nuova interfaccia utente [!UICONTROL Audiences]. (TGT-43433)
* È stato risolto un problema a causa del quale i clienti potevano selezionare tipi di pubblico [!DNL Adobe Audience Manager] (AAM) duplicati durante la modifica dei tipi di pubblico di reporting per un’attività. (TGT-43430)
* È stato risolto un problema che impediva ai clienti di creare tipi di pubblico duplicati, ma in aree di lavoro diverse. (TGT-43423)
* È stato risolto un problema che impediva ai clienti di eliminare le posizioni con offerte ad hoc nelle attività create in [!UICONTROL Form-Based Experience Composer]. (TGT-43315)
* È stato risolto un problema che impediva ai clienti di accedere alle offerte con codice dopo aver fatto clic su offerte con immagini e aver quindi aggiornato l’interfaccia utente. (TGT-43566)
* È stato risolto un problema che causava il ripristino dello script originale non modificato dopo che uno script di profilo veniva modificato, attivato e quindi disattivato. Ora vengono mantenute le modifiche applicate allo script di profilo. (TGT-43249)
* È stato risolto un problema che generava il seguente errore se si tentava di spostare un pubblico in un’altra area di lavoro: “Impossibile completare la richiesta. Se il problema persiste, contatta l’Assistenza clienti di Adobe.” (TGT-43212)
* È stato corretto un errore che si verificava se si clonavano modifiche al codice personalizzato per le pagine di app a pagina singola (SPA). (TGT-43137)
* È stato risolto un problema che interessava la modifica della promozione originale dopo la duplicazione di un’esperienza e la successiva modifica della promozione. (TGT-41775)

### [!DNL Target Standard/Premium] 22.4.1 (28 aprile 2022)

Questa versione include la seguente correzione:

* È stato risolto un problema a causa del quale tre algoritmi basati su carrello utilizzavano la stessa condizione Acquisto/Acquisto sul backend di [!DNL Target]. (TGT-43456)
* È stato abilitato l&#39;aggiornamento del token dell&#39;interfaccia utente [!DNL Target] per le organizzazioni abilitate con [account Business ID](https://helpx.adobe.com/it/enterprise/using/identity.html){target=_blank} e autenticazione basata su criteri (PBA). (TGT-42590)

### Versione della piattaforma [!DNL Target] (giovedì 27 aprile 2022)

Questa versione contiene la seguente modifica:

* Con questa versione è possibile preacquisire il contenuto per le attività [!UICONTROL Auto Personalization] (AP) e [!UICONTROL Auto-Target] (AT) (in precedenza non restituite da [!DNL Target]). Ciò potrebbe modificare le esperienze visualizzate dagli utenti finali in caso di chiamata di preacquisizione (nessuna modifica al flusso &quot;execute&quot;) se un’attività AP/AT si trova nel percorso di consegna ed è di priorità più elevata rispetto ad altre attività AB/XT che utilizzano la stessa posizione per la distribuzione di contenuti.

### Versione piattaforma [!DNL Target] (30 marzo)

Questa versione contiene i seguenti miglioramenti:

* Le metriche di tracciamento dei clic includeranno il payload di Analytics nelle richieste API di consegna per le attività che utilizzano Analytics come origine per la generazione di rapporti (A4T) ed elaborano gli eventi sul lato client. (TNT-43073)

### [!DNL Target Standard] tipi di pubblico aggiornati (28 marzo)

Questa versione contiene i seguenti aggiornamenti:

* La nuova interfaccia utente [!UICONTROL Audiences] verrà abilitata per tutti i clienti [!DNL Target Standard].

### Correzioni tecniche per clienti Target Standard/Premium (22 marzo 2022)

Questa versione di manutenzione include i seguenti miglioramenti:

* È stata aggiunta la funzionalità per restituire dati di payload [!DNL Analytics] per visualizzazioni `prefetch` e metriche di clic `pageLoad` quando si utilizza [!UICONTROL Delivery API] con attività che utilizzano [!UICONTROL Analytics as the reporting source] (A4T). (TNT-43198)
* L’elenco degli agenti utente che filtrano i bot è stato aggiornato per consentire l’utilizzo di un tipo di browser comunemente utilizzato in Giappone. (TNT-43867)

### Target Standard/Premium 22.2.1 (1° febbraio 2022)

Questa versione di manutenzione contiene le correzioni e i miglioramenti seguenti relativi alla nuova interfaccia utente [!UICONTROL Audiences], annunciata in Target Standard/Premium versione 22.1.2, che nelle prossime sei settimane verrà gradualmente implementata per i clienti in tutte le aree geografiche. Le correzioni apportate allineano le funzionalità dei tipi di pubblico creati in [!DNL Adobe Target Standard/Premium].

* È stato risolto un problema che impediva ai tipi di pubblico importati da [!DNL Adobe Experience Platform], [!DNL Adobe Experience Cloud] e [!DNL Adobe Target Classic] di essere assegnati come tipi di pubblico nella generazione dei rapporti. (TGT-43140)
* È stata aggiunta l&#39;opzione [!UICONTROL Delete] nell&#39;elenco [!UICONTROL Audiences] per i tipi di pubblico importati da [!DNL Adobe Experience Platform], [!DNL Adobe Experience Cloud] e [!DNL Adobe Target Classic]. È stata aggiunta anche la funzionalità di eliminazione in blocco. (TGT-42914)

### at.js versione 2.8.1 (28 gennaio 2022)

* È stato corretto un problema che impediva la mappatura di `pageLoad` su target-global-mbox nella modalità di esecuzione ibrida [!UICONTROL On Device Decisioning] (ODD).
* È stato risolto un problema relativo ai dettagli di analisi per richieste mbox.
* Sono state aggiornate le dipendenze di sviluppo per correggere alcune vulnerabilità di sicurezza.

### [!DNL Target Standard/Premium] 22.1.2 (26 gennaio 2022)

| Funzione | Dettagli |
| --- | --- |
| Tipi di pubblico [!DNL Adobe Experience Platform] in [!DNL Target] | Ora puoi sfruttare e utilizzare i tipi di pubblico [!DNL Adobe Experience Platform] in [!DNL Target]. Il team [!DNL Target], il team [!DNL Experience Platform] [!DNL Destinations] e il team [!DNL Unified Profile Service] sono lieti di annunciare la disponibilità generale dei casi d&#39;uso &quot;Same Page/Next Page Personalization&quot;.<br>L’utilizzo dei tipi di pubblico creati in [!DNL Adobe Experience Platform] fornisce dati più completi sui clienti, per una personalizzazione più incisiva. [Real-time Customer Data Platform](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=it){target=_blank} (RTCP), basato su [!DNL Adobe Experience Platform], consente alle aziende di unire dati noti e anonimi provenienti da più origini aziendali per creare profili cliente da utilizzare per fornire ai clienti esperienze personalizzate in tempo reale su tutti i canali e dispositivi.<br>Per ulteriori informazioni, consulta [Utilizzare i tipi di pubblico da Adobe Experience Platform](/help/main/c-target/c-audiences/audiences.md#aep) in *Creare tipi di pubblico*.<br>Leggi il blog di Adobe e guarda il video: [[!DNL Adobe] annuncia Same Page Enhanced Personalization with [!DNL Adobe Target] and [!DNL Real-time Customer Data Platform]](https://blog.adobe.com/en/publish/2021/10/05/adobe-announces-same-page-enhanced-personalization-with-adobe-target-real-time-customer-data-platform){target=_blank}. |
| Aggiornamento dell&#39;interfaccia utente [!UICONTROL Audiences] | Come parte degli sforzi continui del team [!DNL Adobe Target] per migliorare l&#39;esperienza utente per [!DNL Target] utenti, questa versione aggiorna le pagine [!UICONTROL Audiences] e [!UICONTROL Profile Scripts] nell&#39;interfaccia utente [!DNL Target]. Questo aggiornamento unisce e standardizza i disegni di progettazione precedentemente incoerenti, aggiungendo nuovi miglioramenti, ad esempio:<ul><li>Possibilità di selezionare ed eliminare più tipi di pubblico contemporaneamente</li><li>Una [progettazione di audience builder](/help/main/c-target/c-audiences/create-audience.md) rinnovata</li><li>Supporto della regola di esclusione nel generatore di regole di libreria [!UICONTROL Audience]</li><li>Un nuovo filtro &quot;Audience Source&quot; per consentire un rilevamento più rapido del pubblico</li><li>Opzioni di ricerca e filtro persistenti nella sessione</li><li>Possibilità di spostare i tipi di pubblico tra aree di lavoro diverse per i clienti [!DNL Target Premium].</li></ul>Per ulteriori informazioni, consulta [Tipi di pubblico](/help/main/c-target/target.md).<br>**NOTA**: questa funzione verrà implementata gradualmente nelle prossime otto settimane per i clienti in diverse aree geografiche. |
| Aggiornamento dell&#39;interfaccia utente [!UICONTROL Profile Scripts] | Anche la libreria [!UICONTROL Profile Scripts] è stata aggiornata e include un&#39;interfaccia aggiornata insieme a diversi aggiornamenti di produttività:<ul><li>Possibilità di selezionare ed eliminare contemporaneamente più script di profilo</li><li>Un nuovo editor di codice per gli script di profilo</li><li>Evidenziazione della sintassi e controllo degli errori all’interno dell’editor di codice</li><li>Parametri dei token (mbox o profilo) che si completano automaticamente tramite scelte rapide da tastiera</li></ul>Per ulteriori informazioni, consulta [Profili dei visitatori](/help/main/c-target/c-visitor-profile/visitor-profile.md).<br>**NOTA**: questa funzione verrà implementata gradualmente nelle prossime otto settimane per i clienti in diverse aree geografiche. |

### [!DNL Target Standard/Premium] 22.1.1 (12 gennaio 2022)

Questa versione include correzioni di bug e funzionalità preliminari necessarie per integrazioni future.

### Versione della piattaforma Target (13 aprile 2022)

Questa versione contiene i seguenti aggiornamenti:

* È stato risolto un problema per garantire che l’ultimo ottetto di indirizzi IP sia offuscato correttamente quando viene acquisito utilizzando gli script di profilo. (TNT-44076)

### [!DNL Target Standard/Premium] 22.3.1 (5 aprile 2022)

Questa versione contiene le modifiche e i miglioramenti seguenti:

* È stato risolto un problema che causava la disabilitazione delle opzioni [!UICONTROL Include] e [!UICONTROL Exclude] per i tipi di pubblico combinati durante la modifica di un&#39;attività. (TGT-43422)
* È stato risolto un problema che impediva ad alcuni clienti di visualizzare l’elenco dei tipi di pubblico disponibili durante la modifica di un’attività. (TGT-43404)
* È stato risolto un problema che impediva ad alcuni clienti di eliminare un indirizzo IP dall&#39;elenco &quot;[!UICONTROL IPs to exclude from [!DNL Target] reporting data]&quot; in [!UICONTROL Administration] > [!UICONTROL Reporting]. (TGT-43384)
* È stato risolto un problema che impediva l’uso di numeri negativi nel criterio di pubblico che verifica se una variabile è “maggiore di”, “maggiore o uguale a”, “minore di”; o “minore o uguale a”. (TGT-43367)
* È stato risolto un problema che impediva ai clienti di visualizzare la scheda [!UICONTROL Audience Details] durante la creazione di tipi di pubblico combinati. (TGT-43303)

### at.js versione 2.8.0 (7 gennaio 2022)

La [!DNL Target] libreria JavaScript at.js ora raccoglie dati di telemetria relativi all’utilizzo delle funzioni e alle prestazioni. I dati personali non vengono raccolti. La rinuncia a questa funzione è disponibile impostando `telemetryEnabled` false in `targetGlobalSettings`. Per ulteriori informazioni, consulta [telemetryEnabled in targetGlobalSettings](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html?lang=it){target=_blank}.

## Note sulla versione - 2021

### at.js versione 2.7.0 (28 ottobre 2021)

Questa versione contiene i seguenti miglioramenti:

* È stato aggiunto il supporto per [Componenti web](https://developer.mozilla.org/en-US/docs/Web/Web_Components). Questa versione di at.js è necessaria per creare e testare esperienze e offerte personalizzate su elementi personalizzati e su elementi al loro interno. Questa funzionalità è inclusa in [!DNL Target Standard/Premium] versione 21.10.5.

### [!DNL Target Standard/Premium] 21.10.5 (28 ottobre 2021)

Questa versione di manutenzione include i seguenti miglioramenti:

| Funzione | Dettagli |
| --- | --- |
| [!UICONTROL Visual Experience Composer] (VEC) | È stato aggiunto il supporto per [Componenti web](https://developer.mozilla.org/en-US/docs/Web/Web_Components). È possibile creare e testare esperienze e offerte personalizzate su elementi personalizzati e su elementi al loro interno.<br>Per ulteriori informazioni, consulta la sezione sulle [opzioni del Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#custom). |

### [!DNL Target Standard/Premium] 21.10.4 (21 ottobre 2021)

Questa versione di manutenzione include i seguenti miglioramenti:

| Funzione | Dettagli |
| --- | --- |
| Consigli in base al carrello | È stata aggiunta una nuova famiglia di algoritmi per distribuire consigli in base al contenuto del carrello del visitatore.<br>Per ulteriori informazioni, consulta la sezione &quot;In base al carrello&quot; in [Creare criteri](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md), le sezioni &quot;Aggiunte al carrello, visualizzazioni carrello e pagine dipagamento&quot; ed &quot;Escludi elementi già presenti nel carrello del visitatore&quot; in [Pianificare e implementare le attività Consigli](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html?lang=it){target=_blank} e la sezione &quot;In base al carrello&quot; in [Basare i consigli su una chiave di consigli](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md). |

### [!DNL Target Standard/Premium] 21.10.3 (19 ottobre 2021)

Questa versione di manutenzione include i seguenti miglioramenti, correzioni e modifiche:

* Sono stati risolti i problemi che impedivano ai clienti di aprire il pannello [!UICONTROL A4T] in [!DNL Analysis Workspace] facendo clic sul pulsante [!UICONTROL View in Analytics] nel reporting attività di [!DNL Target]. (TGT-42099, TGT-42100)
* È stato risolto un problema che impediva la visualizzazione del pulsante [!UICONTROL Edit Design] durante la modifica delle attività [!UICONTROL A/B Test] e [!UICONTROL Experience Targeting] (XT) utilizzando [!UICONTROL Form-Based Experience Composer]. (TGT-41980)
* È stato risolto un problema che impediva la visualizzazione della casella di controllo [!UICONTROL Compatible] nella selezione dei criteri durante la creazione di una nuova attività [!UICONTROL Recommendations]. (TGT-42053)
* È stato corretto un messaggio di errore errato visualizzato quando non era possibile selezionare [!DNL Analytics] come origine per la generazione di rapporti (A4T) per mancanza di autorizzazioni [!DNL Analytics]. (TGT-41954)
* Sono state implementate più correzioni di accessibilità per migliorare la navigazione da tastiera in tutte le aree dell’interfaccia utente di [!DNL Target].

### [!DNL Target Standard/Premium] 21.10.2 (13 ottobre 2021)

Sono stati aggiunti i seguenti miglioramenti quando si utilizza [!DNL Target] [!UICONTROL Audiences] con [!DNL Adobe Experience Platform Web SDK]:

* Sono state aggiunte icone di avviso, finestre a comparsa e messaggi in diverse aree dell’interfaccia utente [!DNL Target] per indicare che il pubblico è stato eliminato alla sorgente e non è più disponibile per l’utilizzo in attività [!DNL Target].

  Le illustrazioni seguenti mostrano alcuni punti in cui vengono visualizzate le icone, le finestre a comparsa e i messaggi:

   * Pagina elenco [!UICONTROL Activity]

     ![Messaggio di pubblico eliminato alla sorgente nella pagina dell’elenco Attività](assets/deleted-at-source-audiences-list.png)

   * Attività [!UICONTROL Overview] pagine:

     ![Messaggio di pubblico eliminato alla sorgente nella pagina della panoramica](assets/deleted-at-source-overview.png)

   * Passaggio [!UICONTROL Experiences] del flusso di lavoro per la creazione di attività:

     ![Messaggio di pubblico eliminato alla sorgente nella pagina [!UICONTROL Experiences]](assets/deleted-at-source-experiences.png)

   * Passaggio [!UICONTROL Targeting] del flusso di lavoro per la creazione di attività:

     ![Messaggio di pubblico eliminato alla sorgente nella pagina [!UICONTROL Targeting]](assets/deleted-at-source-targeting.png)

   * Passaggio [!UICONTROL Goals & Settings] del flusso di lavoro per la creazione di attività:

     ![Messaggio di pubblico eliminato alla sorgente nella pagina [!UICONTROL Goals & Settings]](assets/deleted-at-source-goals-settings.png)

   * Ottimizzazioni del pubblico ([!UICONTROL Replace Audience] nel passaggio [!UICONTROL Targeting] del flusso di lavoro per la creazione di attività):

* Se tenti di utilizzare la funzione Combina pubblico e uno dei tipi di pubblico è stato eliminato alla sorgente, [!UICONTROL Save] è disabilitato.

### [!DNL Target Standard/Premium] 21.10.1 (6 ottobre 2021)

Questa versione include le seguenti nuove funzionalità:

| Funzione | Dettagli |
| --- | --- |
| Aggiornamento dell&#39;interfaccia utente [!UICONTROL Audiences] | Come parte degli sforzi continui del team [!DNL Adobe Target] per migliorare l&#39;esperienza utente per [!DNL Target] utenti, questa versione aggiorna le pagine [!UICONTROL Audiences] e [!UICONTROL Profile Scripts] nell&#39;interfaccia utente [!DNL Target]. Questo aggiornamento unisce e standardizza i disegni di progettazione precedentemente incoerenti, aggiungendo nuovi miglioramenti, ad esempio:<ul><li>Possibilità di selezionare ed eliminare più tipi di pubblico contemporaneamente</li><li>Una [progettazione di audience builder](/help/main/c-target/c-audiences/create-audience.md) rinnovata</li><li>Supporto della regola di esclusione nel generatore di regole di libreria [!UICONTROL Audience]</li><li>Un nuovo filtro &quot;Audience Source&quot; per consentire un rilevamento più rapido del pubblico</li><li>Opzioni di ricerca e filtro persistenti nella sessione</li></ul>Per ulteriori informazioni, consulta [Tipi di pubblico](/help/main/c-target/target.md). |
| Aggiornamento dell&#39;interfaccia utente [!UICONTROL Profile Scripts] | Anche la libreria [!UICONTROL Profile Scripts] è stata aggiornata e include un&#39;interfaccia aggiornata insieme a diversi aggiornamenti di produttività:<ul><li>Possibilità di selezionare ed eliminare contemporaneamente più script di profilo</li><li>Un nuovo editor di codice per gli script di profilo</li><li>Evidenziazione della sintassi e controllo degli errori all’interno dell’editor di codice</li><li>Parametri dei token (mbox o profilo) che si completano automaticamente tramite scelte rapide da tastiera</li></ul>Per ulteriori informazioni, consulta [Profili dei visitatori](/help/main/c-target/c-visitor-profile/visitor-profile.md). |
| Creazione e modifica dei criteri per i consigli [!BADGE Premium]{type=Positive url="/help/main/c-intro/intro.md#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."} | Il flusso di lavoro di creazione e modifica di [!UICONTROL Recommendations Criteria] è stato razionalizzato per semplificare la scelta dell&#39;algoritmo e delle impostazioni consigliate per raggiungere gli obiettivi.<br>Per ulteriori informazioni, consulta [Creare i criteri](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md). |
| ![Badge Premium](/help/main/assets/premium.png) Miglioramenti della frequenza di aggiornamento dell’intervallo di lookback e dell’algoritmo di Recommendations | È ora possibile eseguire gli algoritmi “Più visualizzati” e “Più venduti” con un intervallo di lookback di sei ore per acquisire il contenuto con tendenze più recenti. Quando l’intervallo di lookback di sei ore è selezionato, i risultati delle raccomandazioni vengono aggiornati ogni 3-6 ore nel corso della giornata.<br>Per ulteriori informazioni, consulta [Origine dati](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#data-source) in *Creare i criteri*. |

### [!DNL Target Standard/Premium] 21.9.1 (14 settembre 2021)

Questa versione di manutenzione include i seguenti miglioramenti, correzioni e modifiche.

* Sono stati risolti dei problemi che impedivano ai clienti di accedere al [!UICONTROL Visual Experience Composer] (VEC) a causa di nuovi criteri di sicurezza per i cookie di terze parti in alcuni browser Web. Questo problema è stato discusso in “Pagine non caricate nel Compositore esperienza visivo o Compositore esperienza avanzato quando si utilizza Google Chrome versione 80+” in [Risoluzione dei problemi relativi al Compositore esperienza visivo e al Compositore esperienza avanzato](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md).
* È stato risolto un problema a causa del quale i nomi delle offerte nel Compositore esperienza visivo mostravano il percorso dell’offerta invece del nome descrittivo. (TGT-41300)
* I nomi delle esperienze ora si riflettono in [!DNL Analysis Workspace] per le attività A4T. (TGT-38674)
* È stato risolto un problema in [!DNL Recommendations] a causa del quale le modifiche di ID entità in una promozione in un’attività duplicata venivano erroneamente applicate all’attività originale. (TGT-41482)
* È stato risolto un problema che impediva la corretta visualizzazione del pulsante &quot;Modifica criteri&quot; nella pagina [!UICONTROL Experiences] per le attività [!DNL Recommendations] nel Compositore esperienza visivo. (TGT-39512)
* È stato risolto un problema che impediva la sincronizzazione delle attività quando venivano duplicate e copiate in un’area di lavoro di test. (TGT-40686)
* È stato risolto un problema che impediva la modifica di un selettore con [frammenti di esperienza](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md) durante l&#39;utilizzo di &quot;[!UICONTROL Insert After]&quot; nel Compositore esperienza visivo. (TGT-41802)
* È stato risolto un problema che impediva l’invio al backend di contenuto JSON vuoto in un’offerta. [!DNL Target] ora invia l’oggetto JSON anche se è vuoto. (TGT-41555)
* È stato risolto un problema che causava l&#39;apertura del report legacy [!DNL Analytics] invece di [!DNL Analysis Workspace] quando i clienti facevano clic su &quot;[!UICONTROL View in Analytics]&quot; durante la visualizzazione di un report. (TGT-41867)
* Sono stati aggiunti ulteriori chiarimenti al messaggio visualizzato nell&#39;interfaccia utente quando un cliente tenta di selezionare [!DNL Analytics] come origine per la generazione di rapporti (A4T) per un&#39;attività [!UICONTROL Automated Personalization]. Il messaggio indica che &quot;[!DNL Target] è l&#39;unica origine supportata per le attività [!UICONTROL Automated Personalization].&quot; (TGT-41954)
* È stato aggiunto un ulteriore chiarimento al messaggio di errore visualizzato quando i clienti tentano di separare gli host con “nuova riga” invece delle virgole. (TGT-40671)
* È stato risolto un problema che causava discrepanze nelle date di alcune attività &quot;[!UICONTROL Last Updated]&quot; rispetto all&#39;interfaccia utente inglese per i clienti spagnoli e giapponesi (quando si visualizzava l&#39;interfaccia utente in spagnolo e giapponese). (TGT-38980)

### at.js 2.6.1 (16 agosto 2021)

* Correzione di un bug relativo all’errore “Nessun artefatto nella cache disponibile per la modalità ibrida” quando si utilizzano le decisioni sul dispositivo.

### [!DNL Target] node.js SDK 2.2.0 (11 agosto 2021)

* Aggiunta raccolta dati di telemetria SDK
* Codegen openapi del client API di consegna automatica

Per ulteriori informazioni su questa versione e sulle versioni precedenti, consulta il [Change log](https://github.com/adobe/target-nodejs-sdk/blob/main/CHANGELOG.md) nella [documentazione dell’SDK node.js di Target](https://github.com/adobe/target-nodejs-sdk) su Github.

### [!DNL Target Standard/Premium] 21.8.1 (10 agosto 2021)

Questa versione di manutenzione contiene molti miglioramenti al back-end, tra cui la seguente modifica visualizzata dal cliente:

* È stato risolto un problema a causa del quale i rapporti per le attività [!UICONTROL Auto Personalization] create in [!UICONTROL Form-Based Experience Composer] facevano riferimento a offerte eliminate nei rapporti. Questo problema causava la visualizzazione di un messaggio di errore di tipo: “Si sono verificati dei problemi nel recupero dei dati per questo rapporto. Se il problema persiste, contatta l’Assistenza clienti Adobe.” (TGT-41028)

### API di consegna di Target (3 agosto 2021)

Questo rilascio contiene i seguenti miglioramenti:

* Il limite per i parametri mbox è stato aumentato a 100 parametri. Il limite precedente era di 50 parametri. (TNT-41717)
* Il limite per `categoryId` è stato aumentato a 256 caratteri. Il limite precedente era di 128 caratteri.
* Sono stati aggiunti i seguenti dettagli di [!DNL Adobe Audience Manager] (AAM) all’API di consegna:

   * AAM UUID: ID interno di AAM utilizzato per identificare in modo univoco un utente.
   * dataPartnerId: ID per un partner dati.
   * dataPartnerUserId: ID utente fornito da un partner dati.

  In precedenza, l’API di consegna comprendeva solo `dcsLocationHint` e `blob`. (TNT-41644)

### [!DNL Target Standard/Premium] 21.6.1 (30 giugno 2021)

Questa versione contiene le nuove funzioni e i miglioramenti seguenti. I codici tra parentesi sono per uso interno di [!DNL Adobe].

| Funzione | Dettagli |
| --- | --- |
| [!UICONTROL Analytics for Target] (A4T) | Facendo clic sul collegamento &quot;[!UICONTROL View in Analytics]&quot; sulla pagina [!UICONTROL Reports] da un&#39;attività che utilizza [!DNL Analytics] come origine per la generazione di rapporti (A4T), ora viene aperto [!DNL Analysis Workspace]. In precedenza, il collegamento apriva la funzione di generazione rapporti di [!DNL Analytics]. (TGT-36959) |

### Python SDK 1.0.0 (16 giugno 2021)

È ora disponibile il nuovo SDK Python [!DNL Adobe Target] con funzionalità di decisioning sul dispositivo. Questa nuova aggiunta rafforza la suite di SDK lato server per [!DNL Target]. Questi SDK facilitano l’integrazione con [!DNL Target] e velocizzano il time to value, nel linguaggio che preferisci. Le integrazioni lato server stanno diventando una scelta popolare dato che il mercato si sta spostando verso un mondo senza cookie in cui i dati di prime parti sono preziosi. Gli SDK di Target sono disponibili nei linguaggi di programmazione più diffusi sul mercato (Python, Java, JavaScript, C# / .Net).

Per ulteriori informazioni, consulta la [documentazione di Python SDK](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/python/overview.html?lang=it){target=_blank} nella [Guida per gli sviluppatori di Adobe Target](https://experienceleague.adobe.com/docs/target-dev/developer/overview.html?lang=it){target=_blank}.

### Target Standard/Premium 21.5.1 (7 giugno 2021)

Questa versione include i seguenti miglioramenti:

| Funzione | Dettagli |
| --- | --- |
| ![Badge Premium](/help/main/assets/premium.png) [!DNL Recommendations] [!UICONTROL Catalog Search] API | Cerca nel catalogo di prodotti e contenuti [!DNL Recommendations] a livello di programmazione tramite API per identificare gli elementi che corrispondono a un criterio di ricerca e semplificare l’amministrazione del catalogo.<br>**Limitazioni e note**:<ul><li>La ricerca nel catalogo tramite API non è supportata per gli ambienti con più di 2.000.000 elementi.</li><li>I risultati della ricerca nel catalogo tramite API vengono aggiornati più rapidamente dei risultati della ricerca nel catalogo tramite l’interfaccia utente di [!DNL Target]. La ricerca nel catalogo nell’interfaccia utente di [!DNL Target] può richiedere tempo aggiuntivo per riflettere i risultati più recenti.</li></ul>Per ulteriori informazioni, consulta [Ricerca di entità](https://developers.adobetarget.com/api/recommendations/#tag/Searching-Entities) nella guida delle API di *[!DNL Adobe Target][!DNL Recommendations]*. |

Questa versione di manutenzione include le seguenti correzioni.

* È stato risolto un problema che causava la modifica dell&#39;area di lavoro predefinita in un&#39;altra area di lavoro durante l&#39;aggiornamento della pagina [!UICONTROL Audiences]. (TGT-38871)
* È stato risolto un problema in [!UICONTROL Administration] > [!UICONTROL Implementation] che a volte causava un messaggio di errore di tipo: &quot;La mbox globale potrebbe non essere sincronizzata. Prova a salvarla di nuovo.”

### ![Badge Adobe Experience Platform Web SDK](/help/main/assets/platform.png) [!DNL Adobe Experience Platform Web SDK] versione 2.5.0 (1° giugno 2021)

Questa versione di [!DNL Platform Web SDK] include il supporto per i seguenti elementi:

| Funzione | Dettagli |
| --- | --- |
| Supporto dei reindirizzamenti con [!UICONTROL Analytics for Target] (A4T) | Platform Web SDK ora supporta i [!DNL Target]reindirizzamenti quando si utilizza [A4T](/help/main/c-integrating-target-with-mac/a4t/a4t.md).<br>Per ulteriori informazioni, consulta [Implementazione di Analytics per  [!DNL Target] ](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md). |

### at.js versione 2.5.0 (13 maggio 2021)

Questa versione di at.js include i miglioramenti e le modifiche seguenti:

* Supporto di [Decisioning sul dispositivo](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/on-device-decisioning/overview.html?lang=it){target=_blank} per at.js.
* Supporto dei [collegamenti di anteprima](/help/main/c-activities/c-activity-qa/activity-qa.md) per le attività di Automated Personalization

Questa versione rimuove anche il supporto per Microsoft Internet Explorer 10, Internet Explorer 11 e tutte le versioni precedenti. Microsoft Edge continua a essere supportato in at.js 2.5.0 e versioni successive.

### Target Standard/Premium 21.4.1 (19 aprile 2021)

Questa versione contiene le nuove funzioni e i miglioramenti seguenti. I codici tra parentesi sono per uso interno di [!DNL Adobe].

| Funzione | Dettagli |
| --- | --- |
| Supporto del decisioning sul dispositivo per at.js<br>(Data non ancora annunciata) | Il decisioning sul dispositivo consente agli addetti al marketing e agli sviluppatori di rilasciare esperienze sperimentali e personalizzazioni sul browser di un utente con latenza pressoché pari a zero.<br>Per ulteriori informazioni, consulta [Decisioning sul dispositivo per at.js](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/on-device-decisioning/overview.html?lang=it){target=_blank}. |
| ![Premium](/help/main/assets/premium.png) Operatori basati su elenco per regole di filtro delle entità | [!DNL Target Recommendations] supporta nuovi operatori basati su elenco per le regole di filtro delle entità. (TGT-39234)<br>I nuovi operatori includono:<br><ul><li>È contenuto nell’elenco</li><li>Non è contenuto nell’elenco</li><li>L’elenco contiene un elemento in</li><li>L’elenco non contiene un elemento in</li><li>L’elenco contiene tutti gli elementi in</li><li>L’elenco non contiene tutti gli elementi in</li></ul>Per ulteriori informazioni, consulta “Operatori disponibili” in [Utilizzare regole di inclusione dinamiche e statiche](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#operators). |

Questa versione include le seguenti correzioni.

* È stato risolto un problema che impediva la sincronizzazione di un&#39;attività dopo la modifica del pubblico in [!UICONTROL All Visitors]. (TGT-40259)
* È stato risolto un problema che impediva la duplicazione delle offerte quando vengono utilizzate in posizioni diverse nelle attività [!UICONTROL Automated Personalization] anche se l&#39;opzione [!UICONTROL Disallow Duplicates] è abilitata. (TGT-39567)
* È stato risolto un problema che impediva il caricamento corretto della pagina [!UICONTROL Administration] > [!UICONTROL Scene7 configuration]. (TGT-39918)
* È stato risolto un problema che causava il mapping delle proprietà sull’area di lavoro errata. (TGT-39869)
* È stato risolto un problema che causava un caricamento infinito se la richiesta non riusciva dopo la modifica dell’ambiente durante la creazione di un’esclusione di consigli. (TGT-39948)

### at.js 2.4.1 (23 marzo 2021)

Questa release di at.js è una versione di manutenzione e include i miglioramenti e le correzioni seguenti:

* È stato risolto un problema a causa del quale `targetPageParams` veniva incluso nelle richieste mbox. `targetPageParams` deve essere incluso solo nelle richieste `pageLoad`. (TNT-40247)
* È stato risolto un problema relativo agli oggetti globali del documento e della finestra nell’estensione [!DNL Adobe Experience Platform Launch], sostituendo con riferimenti diretti le dipendenze degli oggetti globali Platform Launch. (TNT-37124)

### Modifiche all’indirizzo IP per i server di elaborazione dei feed Recommendations (16 marzo 2021)

Gli indirizzi IP del server di elaborazione dei feed di [!DNL Target Recommendations] sono stati aggiornati il 16 marzo 2021. Per ulteriori informazioni, consulta [Indirizzi IP utilizzati dai server di elaborazione dei feed Consigli](/help/main/c-recommendations/c-recommendations-faq/ip-addresses-marketing-cloud.md).

### Target Standard/Premium 21.2.1 (9 marzo 2021)

Questa versione di manutenzione include i seguenti miglioramenti, correzioni e modifiche.

I codici tra parentesi sono per uso interno di [!DNL Adobe].

* È stata aumentata la dimensione dell’offerta consentita (TGT-38304):

  | Tipo | Limite precedente | Nuovo limite |
  | --- | --- | --- |
  | HTML | 256 KB | 1024 KB |
  | Offerte visive dall’interfaccia utente di Target | 64 KB | 1024 KB per ogni esperienza |
  | Tramite API | 512 KB | 1024 KB |

* I report [!UICONTROL Personalization Insights] per le attività [!UICONTROL Auto-Target] (AT) e [!UICONTROL Automated Personalization] (AP) ora vengono prodotti ogni giorno. È possibile scegliere un report che fornisce [!UICONTROL Automated Segments] o [!UICONTROL Important Attributes] per gli ultimi 15, 30 e 60 giorni. Le opzioni di 45 giorni e 90 giorni sono state rimosse per consentire l’esecuzione giornaliera delle altre impostazioni dell’intervallo di lookback. (TGT-39472)
* È stato risolto un problema che impediva la visualizzazione della dipendenza corrente quando i clienti facevano clic su [!UICONTROL Edit Dependency] nella pagina [!UICONTROL Goals & Settings] di un&#39;attività. (TGT-39340)
* È stato risolto un problema che si verificava durante l&#39;aggiornamento di [!UICONTROL Audience Library] di un&#39;area di lavoro. Prima dell’aggiornamento, vengono visualizzati i tipi di pubblico per l’area di lavoro attualmente selezionata. Dopo l&#39;aggiornamento, [!UICONTROL Default Workspace] e i relativi tipi di pubblico vengono visualizzati. L’area di lavoro corrente e i relativi tipi di pubblico ora persistono dopo l’aggiornamento. (TGT-38871)
* È stato risolto un problema che si verificava durante la copia di un&#39;attività [!UICONTROL Recommendations] e in seguito modificando l&#39;attività originale con la variazione della sequenza di criteri. La modifica nella sequenza di criteri nell’attività originale veniva erroneamente applicata anche all’attività copiata. (TGT-39155)
* È stato risolto un problema che causava la visualizzazione di un numero errato di prodotti per [!UICONTROL Recommendations] esclusioni. (TGT-39599)

### Target Standard/Premium 21.1.1 (19 gennaio 2021)

Questa versione di manutenzione include i seguenti miglioramenti, correzioni e modifiche.

I codici tra parentesi sono per uso interno di [!DNL Adobe].

* È stato aggiunto un avviso durante la selezione di una metrica [!DNL Adobe Analytics] quando si utilizza [!UICONTROL Analytics as the reporting source] (A4T) in un&#39;attività [!UICONTROL Auto-Target]. I modelli [!UICONTROL Auto-Target] sono ottimizzati per funzionare con metriche binarie (basate sulla conversione). La selezione di una metrica continua, ad esempio i ricavi, potrebbe avere risultati non ottimali e i report [!UICONTROL Personalization Insights] potrebbero non essere accurati. (TGT-38926)
* È stata aggiunta un&#39;icona di stato nel rapporto [!UICONTROL Auto-Target Summary] per le attività [!UICONTROL Auto-Target] che utilizzano A4T. L&#39;icona di controllo verde accanto a ogni esperienza nel rapporto indica che per quell&#39;esperienza è stato generato un modello di apprendimento automatico personalizzato. L&#39;icona dell&#39;orologio indica che non è stato fornito abbastanza traffico per generare il modello. (TGT-38925)
* I rapporti [!UICONTROL Automated Segments] e [!UICONTROL Important Attributes] per le attività [!UICONTROL Auto-Target] che utilizzano metriche di conversione A4T e [!DNL Analytics] vengono generati e hanno lo stesso aspetto di quando si utilizza [!DNL Target] come origine per la generazione di rapporti. (TGT-38931)
* Opzione di filtro dell&#39;ambiente aggiunta all&#39;elenco [!UICONTROL Recommendations] [!UICONTROL Collections]. (TGT-38353)
* È stato risolto un problema che causava la visualizzazione del conteggio dei prodotti errato nelle raccolte [!UICONTROL Recommendations]. (TGT-39162)
* È stato aggiunto un filtro [!UICONTROL Last Updated] a [!UICONTROL Recommendations] [!UICONTROL Catalog Search]. (TGT-38340)
* È stato risolto un problema in [!UICONTROL Recommendations] che causava il blocco della pagina [!UICONTROL Create Sequence] dopo la modifica del settore verticale. (TGT-38160)
* È stato risolto un problema che impediva agli utenti di rimuovere un pubblico da un&#39;offerta in un&#39;attività [!UICONTROL Automated Personalization] (AP). (TGT-39058)
* È stato risolto un problema che causava la visualizzazione errata dell&#39;intervallo di tempo (date di inizio e di fine) nelle schede [!UICONTROL Audience Info] per alcuni clienti. (TGT-39150)
* È stato risolto un problema che impediva ad alcuni clienti di visualizzare l&#39;elenco delle attività in [!UICONTROL Default Workspace]. (TGT-38526)

### at.js 2.4.0 (14 gennaio 2021)

Questa versione di at.js è una versione di manutenzione che include i miglioramenti e le correzioni seguenti:

* È stato aggiunto il supporto per l’ID di piattaforma/profilo unificato agli ID cliente dell’API Delivery.
* È stata corretta l’iniezione di tag di stile non valida.

## Note sulla versione - 2020

### Target Standard/Premium 20.10.1 (27 ottobre 2020)

Questa versione include le seguenti nuove funzionalità:

| Funzione | Dettagli |
| --- | --- |
| Decisioning sul dispositivo | Le attività di decisioning sul dispositivo consentono sia agli addetti al marketing che agli sviluppatori di prodotti di distribuire personalizzazioni basate sulla sperimentazione e sull’apprendimento automatico dall’interno del dispositivo di un utente, su canali diversi, con latenza pressoché pari a zero.<br>Velocità e prestazioni sono importanti, in termini di approfondimenti sul cliente e soddisfazione degli utenti.<br>Le attività di decisioning sul dispositivo consentono di compilare istruzioni chiave di personalizzazione e sperimentazione nei tipi di attività Test A/B e Targeting esperienza (XT), sotto forma di “artefatti di ottimizzazione”, ossia oggetti JSON caricati sul dispositivo del cliente tramite la rete CDN. Inoltre, poiché il decisioning sul dispositivo si collega in modo nativo con i prodotti [!DNL Adobe Experience Cloud], gli utenti di [!DNL Target] ricevono analisi rapide e iterazioni di esperienze più veloci.<br>Per ulteriori informazioni, consulta *[Decisioning sul dispositivo per at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/on-device-decisioning/on-device-decisioning.html?lang=it){target=_blank} e [Introduzione alle decisioni sul dispositivo](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/on-device-decisioning/overview.html?lang=it){target=_blank} per il lato server. |

Questa versione include i miglioramenti, le correzioni e le modifiche seguenti:

* È stato risolto un problema che impediva la visualizzazione di [!UICONTROL Average Lift Confidence Interval] e [!UICONTROL Confidence] nel reporting [!DNL Auto-Target] per la riga [!UICONTROL Total]. Le misurazioni vengono visualizzate correttamente per tutte le singole esperienze. (TGT-37301)
* È stato risolto un problema che ha interessato la generazione di rapporti [!DNL Adobe Target Premium] per [!UICONTROL Auto-Target] utenti dal 15 settembre alle 2:30 (PDT) al 6 ottobre alle 9:25 (PDT). Quando si visualizzano i rapporti per le metriche di conversione interessate (configurate utilizzando l&#39;opzione &quot;[!UICONTROL Viewed a page]&quot; o &quot;[!UICONTROL Clicked on mbox]&quot;), i tassi di conversione non vengono riportati correttamente. Al momento non è presente alcun problema di consegna noto.
* È stata aggiunta una colonna [!UICONTROL Last Updated At] selezionabile nella tabella [!UICONTROL Catalog Search] e un filtro [!UICONTROL Last Updated At]. Questo miglioramento consente di risparmiare tempo e lavoro: non è più necessario aprire ogni singolo elemento per vedere quando è stato aggiornato per l’ultima volta, ed è possibile filtrare in base alla data dell’ultimo aggiornamento degli elementi.

  ![Illustrazione della colonna e del filtro Ultimo aggiornamento](/help/main/r-release-notes/assets/column-and-filter.png)

* Sono stati effettuati aggiornamenti per rendere l’interfaccia utente di Target compatibile con le [linee guida per l’accessibilità dei contenuti web](https://www.w3.org/WAI/standards-guidelines/wcag/) 2.0, criteri di successo di livello A e AA (WCAG 2.0 AA). (TGT-34384 e TGT-24679)
* Miglioramenti all’informativa sulla sicurezza dei contenuti (Content Security Policy, CSP). (TGT-37035)
* È stato introdotto un modo per specificare il codice cliente come parametro per i clienti che utilizzano CNAME. (TNT-38571)
* È in corso il trasferimento della documentazione di [!DNL Adobe Experience Cloud] a [!DNL Experience League]. Nel mese di ottobre, tutte le note sulla versione, gli articoli, i video e i tutorial verranno trasferiti dalla posizione corrente in `docs.adobe.com` a [!DNL Experience League]. In questo modo tutti i contenuti di apprendimento, supporto autonomo, abilitazione e community saranno accessibili da un’unica posizione. Questa modifica non richiede alcun intervento da parte tua: tutti i collegamenti esistenti verranno reindirizzati a [!DNL Experience League]. All’inizio di questo passaggio, le note sulla versione verranno aggiornate di conseguenza.

### Target Standard/Premium 20.9.1 (30 settembre 2020)

Questa versione di manutenzione include i seguenti miglioramenti, correzioni e modifiche:

* Sono state migliorate la navigazione e la funzionalità per gli utenti che utilizzano solo la tastiera. (TGT-34487, TGT-34516, TGT-34517, TGT-34514)
* Sono state aggiunte etichette nell’interfaccia utente per aiutare gli utenti che utilizzano tecnologie per l’accessibilità. (TGT-34500, TGT-34501, TGT-34502, TGT-24504)
* È stato migliorato il contrasto di testo e colori per immagini e testo nell’interfaccia utente. (TGT-34513)

### Target Standard/Premium 20.8.3 (15 settembre 2020)

| Funzione | Dettagli |
| --- | --- |
| ![Icona Premium](/help/main/assets/premium.png) Supporto di Analytics for Target (A4T) per le attività di Targeting automatico | [!UICONTROL Auto-Target] attività ora supportano [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md).<br>Questa integrazione consente di utilizzare l&#39;algoritmo di machine learning [!UICONTROL Auto-Target] per scegliere l&#39;esperienza migliore per ogni visitatore in base al profilo, al comportamento e al contesto.<br>Se hai già implementato [A4T](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md) per l&#39;utilizzo con attività di Test A/B ed Experience Targeting, è tutto pronto.<br>Per ulteriori informazioni, consulta [Supporto A4T per attività di allocazione automatica e targeting automatico](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md). |

### Target Standard/Premium 20.8.2 (10 settembre 2020)

| Funzione | Dettagli |
| --- | --- |
| ![Icona Premium](/help/main/assets/premium.png) Controllo degli slot di consigli entro sequenze di criteri | Le sequenze di criteri ora consentono di controllare il numero di slot raggruppati per ogni criterio di consigli, consentendo di combinare e abbinare diversi tipi di elementi o diverse logiche degli algoritmi.<br>Per ulteriori informazioni, consulta [Creare sequenze di criteri](/help/main/c-recommendations/c-algorithms/create-criteria-sequence.md#sequence). |

### Target Standard/Premium 20.8.1 (2 settembre 2020)

Questa versione include i miglioramenti, le correzioni e le modifiche seguenti:

* È stato risolto un problema che causava la visualizzazione di errori durante il caricamento delle nuove pagine [!UICONTROL Administration] dopo il cambio di organizzazione. (TGT-37730)
* È stato risolto un problema che causava la visualizzazione del codice client errato nella pagina [!UICONTROL Administration > Implementation]. (TGT-37849)
* È stato risolto un problema che a volte impediva agli utenti di utilizzare le funzioni di modifica nel Compositore esperienza visivo [!UICONTROL Visual Experience Composer] dopo il suo corretto caricamento. (TGT-37162)
* È stato risolto un problema che impediva il caricamento delle pagine in Compositore esperienza visivo e Compositore esperienza avanzato anche se l’estensione VEC Helper era installata. Questo era dovuto a cambiamenti in Google Chrome 80+. Scarica l’[estensione VEC Helper aggiornata](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md). (TGT-37893)
* È stato risolto un problema che a volte impediva agli utenti di scaricare at.js dalla pagina [!UICONTROL Administration > Implementation] dopo il cambio di organizzazione. (TGT-37668)
* Il pulsante di download di at.js ora è disattivato durante il caricamento per impedire a [!DNL Target] di inviare più richieste se gli utenti fanno clic più volte. (TGT-37633)
* È stato risolto un problema nelle attività [!UICONTROL Experience Targeting] (XT) a causa del quale le esperienze visualizzavano il messaggio &quot;recupero risultati&quot; per un periodo di tempo prolungato. (TGT-37684)
* Sono state migliorate la navigazione e la funzionalità per gli utenti che utilizzano solo la tastiera. (TGT-34479 e TGT-34473)
* Sono state aggiunte etichette nell’interfaccia utente per aiutare gli utenti che utilizzano tecnologie per l’accessibilità. (TGT-34480)
* È stato migliorato il messaggio di errore visualizzato quando si elimina un riquadro di visualizzazione mobile attualmente utilizzato in un’attività. Il messaggio di errore ora recita: “Questo riquadro di visualizzazione è attualmente associato a una o più attività. Per eliminarlo, rimuovilo da tali attività.” (TGT-37030)
* Nel Compositore esperienza visivo è stato aggiunto il supporto necessario per consentire il tracciamento dei clic su un selettore css che corrisponde a più di un elemento nella pagina. (TGT-37323)
* È stato risolto un problema che impediva ad alcuni utenti di visualizzare l&#39;elenco [!UICONTROL Activity]. Veniva visualizzato il seguente messaggio di errore: “Impossibile recuperare i suggerimenti URL.” L’errore si verificava per gli utenti che utilizzano un ritorno a capo in FirstName (FirstName/r/n) nel sistema di back-end Adobe. (TGT-37330)
* È stato risolto un problema che impediva agli utenti di visualizzare la pagina [!UICONTROL Activity] se il nome dell&#39;area di lavoro (specificato in [!UICONTROL Adobe Admin Console for Enterprise]) contiene un apostrofo. (TGT-37709)
* È stato risolto un problema nelle attività [!UICONTROL Auto-Allocate] durante la selezione delle metriche di ottimizzazione e conversione, a causa del quale un messaggio di errore chiedeva agli utenti di selezionare una suite di rapporti, anche se ne era già stata specificata una. (TGT-37689)
* È stato risolto un problema che a volte causava la visualizzazione di metriche vuote sulla pagina [!UICONTROL Goals and Settings] dopo l&#39;accesso alla pagina [!UICONTROL Targeting] e il suo ritorno. (TGT-37691)
* È stato risolto un problema che causava un valore errato dell’ultima modifica per i criteri [!DNL Recommendations]. (TGT-37666)
* È stato risolto un problema che causava la visualizzazione degli ID mbox nell’elenco a discesa mbox, invece dei nomi mbox. (TGT-37739)

### at.js 2.3.2 (24 luglio 2020)

Questa versione di at.js è una versione di manutenzione e include la correzione seguente:

* È stato corretto un bug a causa del quale uno script o un codice aggiungeva proprietà predefinite alla finestra o al documento.

### Target Standard/Premium 20.7.1 (27 luglio 2020)

Questa versione include le seguenti modifiche:

#### Aggiornamento dell&#39;interfaccia utente della sezione [!UICONTROL Administration]

Stiamo gradualmente riscrivendo l’intera interfaccia utente di [!DNL Target] utilizzando un nuovo stack tecnologico per poter offrire prestazioni migliori, ridurre il tempo di manutenzione necessario per il rilascio di nuove funzioni e migliorare l’esperienza di utilizzo in tutto il prodotto. La prima sezione aggiornata è la sezione [!UICONTROL Setup], rinominata [!UICONTROL Administration].

Come parte di questo aggiornamento, potrai eseguire facilmente molte azioni utilizzando le pagine della sezione [!UICONTROL Administration], ad esempio:

* Scarica l&#39;ultimo file at.js dalla scheda [!UICONTROL Implementation] (**[!UICONTROL Administration]** > **[!UICONTROL Implementation]**).
* Personalizza le impostazioni at.js e verifica facilmente le modifiche (**[!UICONTROL Administration]** > **[!UICONTROL Implementation]**).
* Modifica le impostazioni di reporting avanzate, ad esempio la valuta e il fuso orario predefiniti, gli indirizzi IP da escludere dai rapporti, ecc. (**[!UICONTROL Administration]** > **[!UICONTROL Reporting]**)
* Offusca gli indirizzi IP dei visitatori per motivi di privacy (**[!UICONTROL Administration]** > **[!UICONTROL Implementation]**)
* Visualizza l&#39;elenco esistente di utenti per area di lavoro e i relativi ruoli, prima di gestirli in Adobe Admin Console (**[!UICONTROL Administration]** > **[!UICONTROL Users]**).
* Cerca e filtra tutte le tabelle nella sezione [!UICONTROL Administration].

Per ulteriori informazioni, consulta [Panoramica sull’amministrazione di Target](/help/main/administrating-target/administrating-target.md).

#### Miglioramenti, correzioni e modifiche

Questa versione include i miglioramenti, le correzioni e le modifiche seguenti:

* È stato risolto un problema a causa del quale le preferenze del sito non venivano mantenute dopo l’aggiornamento. (TGT-37239)
* È stato risolto un problema che impediva il corretto funzionamento di [!UICONTROL Insert After] > [!UICONTROL Image] con immagini SVG (Scalable Vector Graphics). (TGT-37242)
* È stato risolto un problema per gli utenti con il ruolo [!UICONTROL Publisher] che impediva l&#39;eliminazione delle bozze di attività. (TGT-37358)
* È stato risolto un problema che impediva agli utenti di modificare un&#39;attività quando è selezionato [!UICONTROL All My Workspaces]. (TGT-37276)

### Target Standard/Premium 20.5.1 (17 giugno 2020)

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| Supporto di Analytics for Target (A4T) per le attività [!UICONTROL Auto-Allocate] | [!UICONTROL Auto-Allocate] attività ora supportano [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md).<br>Questa integrazione ti consente di utilizzare la funzionalità multi-armed bandit di [!UICONTROL Auto-Allocate] per indirizzare il traffico verso esperienze vincenti, utilizzando al tempo stesso una metrica di obiettivo di [!UICONTROL Adobe Analytics] e/o funzionalità di reporting e analisi di [!UICONTROL Adobe Analytics].<br>Se hai già implementato [A4T](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md) per l&#39;utilizzo con attività di Test A/B ed Experience Targeting, è tutto pronto.<br>Per ulteriori informazioni, consulta [Supporto di A4T per attività di allocazione automatica e targeting automatico](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md). |
| Token di risposta per il metodo di allocazione del traffico per le attività di Targeting automatico e Automated Personalization | Sono stati aggiunti due [token di risposta](/help/main/administrating-target/response-tokens.md) alle attività [!UICONTROL Auto-Target] e [!UICONTROL Automated Personalization] per consentire di determinare se un visitatore ha ricevuto una particolare esperienza a seguito dell&#39;assegnazione al traffico &quot;di controllo&quot; o &quot;mirato&quot;.<ul><li>`experience.trafficAllocationId` restituirà 0 se un visitatore ha ricevuto un&#39;esperienza dal traffico &quot;di controllo&quot; e 1 se un visitatore ha ricevuto un&#39;esperienza dalla distribuzione del traffico &quot;mirata&quot;.</li><li>`experience.trafficAllocationType` restituirà &quot;controllo&quot; o &quot;destinazione&quot;.</li></ul>Per ulteriori informazioni sul controllo rispetto al traffico di destinazione, consulta [Selezionare il controllo per un’attività Automated Personalization o Targeting automatico](/help/main/c-activities/t-automated-personalization/experience-as-control.md). |
| Ruolo [!UICONTROL Publisher] | Questo nuovo ruolo è simile al ruolo [!UICONTROL Observer] corrente (può visualizzare le attività, ma non può crearle o modificarle). Tuttavia, il ruolo [!UICONTROL Publisher] dispone dell&#39;autorizzazione aggiuntiva per attivare le attività.<br>Per ulteriori informazioni, vedi: <ul><li>**Utenti di Target Standard**: [Specificare ruoli e autorizzazioni](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#roles-permissions) in *Utenti*.</li><li>**Utenti di Target Premium**: [Passaggio 6: Specificare ruoli e autorizzazioni](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md#section_8C425E43E5DD4111BBFC734A2B7ABC80) in *Configurare le autorizzazioni Enterprise*.</li></ul> |
| Supporto di A4T in [!DNL Analysis Workspace]<br>25 giugno 2020 | [!UICONTROL Anaytics for Target] (A4T) è ora supportato in [!DNL Analysis Workspace]. [!UICONTROL Analytics for Target (A4T) panel] consente di analizzare le attività e le esperienze [!DNL Adobe Target] in [!DNL Analysis Workspace].<br>Per ulteriori informazioni, consulta [Rapporti in Analytics](/help/main/c-integrating-target-with-mac/a4t/reporting.md) in *Generazione di rapporti per A4T* e [Pannello Analytics for Target (A4T)](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/a4t-panel.html?lang=it) nella *Guida agli strumenti di Analytics*. |

**Miglioramenti, correzioni e modifiche**

* È stato risolto un problema a causa del quale, nella definizione dell’attività, veniva memorizzata la metrica “visitors” invece di “UniqueVisitors”. (TGT-37098)
* È stato risolto un problema nell&#39;interfaccia utente di [!DNL Target] che causava il malfunzionamento della barra di scorrimento verticale nella pagina [!UICONTROL Audiences]. (TGT-36968)

### Versioni di at.js 1.8.2 e at.js 2.3.1 (15 giugno 2020)

Nelle librerie at.js [!DNL Target] sono stati apportati i miglioramenti e le correzioni seguenti:

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| at.js 1.8.2 | Questa versione di at.js è una versione di manutenzione e include la correzione seguente:<ul><li>È stato risolto un problema che si verificava con l’utilizzo di CNAME e Edge override, at.js 1.*x* poteva creare il dominio del server in modo errato, causando un errore nella richiesta di [!DNL Target]. (TNT-35064)</li></ul>Per ulteriori informazioni, consulta [Dettagli della versione at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank}. |
| at.js 2.3.1 | Questa release di at.js è una versione di manutenzione e include i miglioramenti e le correzioni seguenti:<ul><li>L’impostazione `deviceIdLifetime` ora può essere sostituita tramite [targetGlobalSettings](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html?lang=it){target=_blank}. (TNT-36349)</li><li>È stato risolto un problema che si verificava con l’utilizzo di CNAME e Edge override, at.js 2.*x* poteva creare il dominio del server in modo errato, causando un errore nella richiesta di [!DNL Target]. (TNT-35065)</li><li>È stato risolto un problema che si verificava durante l’utilizzo delle estensioni [!DNL Target] [!DNL Launch] v2 e [!DNL Adobe Analytics] [!DNL Launch], a causa del quale [!DNL Target] ritardava la chiamata di [!DNL Analytics] `sendBeacon`. (TNT-36407, TNT-35990, TNT-36000)</li></ul>Per ulteriori informazioni, consulta [Dettagli della versione at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank}. |

### Modifiche in API v2 per lo stato di Batch profili (14 maggio 2020)

A partire dalla versione del 20 maggio, lo stato di Batch profili restituirà solo i dati di errore a livello di riga (i dati di successo non verranno restituiti). Inoltre, gli ID profilo con errore verranno restituiti dall’API.

Risposte API precedenti e nuove:

`ProfileBatchStatus Api`
`http://<<edge>>/m2/<<client>>/profile/batchStatus?batchId=<batchid>`

**Attualmente la risposta si presenta così:**

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

### Target Standard/Premium 20.4.1 (6 maggio 2020)

Questa versione include i miglioramenti, le correzioni e le modifiche seguenti:

* È stato risolto un problema che qualificava in modo errato un tipo di dispositivo e browser per un pubblico. (TGT-36266)
* È stato risolto un problema che impediva la visualizzazione dei dati del rapporto su schermi con una larghezza inferiore a 963 pixel. (TGT-36549)
* È stato risolto un problema che impediva il corretto rendering dei rapporti di Personalizzazione automatica. (TGT-36619)
* È stato risolto un problema che consentiva la selezione di metriche non compatibili nelle attività di Allocazione automatica e Targeting automatico che utilizzano Analytics for Target (A4T). (TGT-36646)
* È stato risolto un problema che impediva la corretta visualizzazione di alcune opzioni nel Compositore esperienza visivo. (TGT-36571)
* È stato risolto un problema nell’interfaccia utente di Target a causa del quale altre anteprime di offerte Consigli visualizzavano il contenuto modificato dopo che un utente aveva sostituito il contenuto in una singola esperienza. (TGT-36053 e TGT-36894)
* È stato risolto un problema che impediva ad alcuni utenti di eliminare elementi da un catalogo Consigli. (TGT-36455)
* È stato risolto un problema che impediva agli utenti di salvare criteri Consigli in un’attività multipagina. (TGT-36249)
* È stato risolto un problema che causava la scomparsa dei pulsanti di scelta dell’origine dati comportamentale quando si modificavano i criteri per una seconda volta consecutiva. (TGT-36796)
* È stato risolto un problema a causa un algoritmo Consigli visualizzava il messaggio “recupero dei risultati” per un periodo prolungato. (TGT-36550 e TGT-36551)
* Sono state aggiornate numerose stringhe dell’interfaccia utente per diverse lingue.

### Target at.js (25 marzo 2020)

Sono disponibili le seguenti nuove versioni delle librerie JavaScript at.js di Target:

* versione at.js 2.3.0
* versione at.js 1.8.1

Per ulteriori informazioni, consulta [Dettagli della versione at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank}.

### Target Standard/Premium 20.2.1 (23 marzo 2020)

Questa versione include i miglioramenti, le correzioni e le modifiche seguenti:

* È stato risolto un problema che impediva ai clienti di selezionare una raccolta durante la ricerca in un catalogo. (TGT-36230)
* È stato risolto un problema in cui un criterio creato tramite API ma a cui non si fa riferimento da alcuna attività creata nell’interfaccia utente di Target poteva essere eliminato erroneamente dall’interfaccia utente. (TGT-35917)
* Sono stati implementati miglioramenti relativi alla sicurezza Content Security Policy (CSP). (TGT-36190)
* È stato risolto un problema che causava la visualizzazione di “NaN%” se si scorreva la barra della percentuale di ponderazione degli attributi fino all’estremità destra. (TGT-36211)
* Sono stati risolti alcuni problemi di localizzazione, per la corretta visualizzazione del testo dell’interfaccia utente in varie lingue.
* Abbiamo standardizzato l’elenco delle metriche disponibili dalle attività di Adobe Analytics for Target (A4T) dichiarando obsolete le metriche di Adobe Analytics non supportate nella versione corrente delle API di Adobe Analytics. Questo ci consentirà di estendere il supporto A4T nelle future versioni di Adobe Target.

  Sono state apportate le seguenti modifiche:

   * “Tempo medio trascorso su pagina” è stato sostituito da “Tempo medio trascorso nel sito”. Per tutte le attività che utilizzano questa metrica per l’obiettivo principale, alla successiva modifica dell’attività, verrà selezionato “Tempo medio trascorso nel sito” (nota: misurato in minuti anziché in secondi) come metrica dell’obiettivo principale.
   * “Visitatori” è stato sostituito da “Visitatori univoci”. Per tutte le attività che utilizzano questa metrica per l’obiettivo principale, alla successiva modifica dell’attività verrà selezionato “Visitatori univoci” come metrica dell’obiettivo principale.

* Le metriche seguenti sono state dichiarate obsolete e non possono più essere selezionate come metrica dell’obiettivo principale durante la creazione di una nuova attività A4T.

  | Metriche obsolete | Metriche di sostituzione consigliate |
  |--- |--- |
  | Visitatori giornalieri, Visitatori orari, Visitatori mensili, Visitatori trimestrali, Visitatori settimanali, Visitatori annuali | Visitatori univoci |
  | Profondità media della visita | n/d. Non suggerito come metrica di obiettivo principale |
  | Bot | n/d. Non suggerito come metrica di obiettivo principale |
  | Frequenza arresti anomali mobile, Lunghezza media sessione precedente mobile, Classifica media app store mobile, Frequenza arresti anomali prestazioni app mobile, Valutazione media app store mobile | n/d. Non suggerito come metrica di obiettivo principale |

### Navigazione in Adobe Experience Cloud (22 febbraio 2019)

* Quando accedi ad [!DNL Adobe Experience Cloud], trovi la nuova navigazione dell’intestazione. Assomiglia molto alla navigazione precedente, con la barra nera nella parte superiore, ma offre i seguenti miglioramenti:

   * Passaggio più semplice tra le diverse organizzazioni [!DNL Identity Management System] (IMS) o verso una soluzione diversa.
   * Guida utente migliorata: i risultati della ricerca includono i risultati provenienti dalla documentazione di [!DNL Target], dai forum della community e nuovi contenuti video, che consentono di accedere più facilmente a più risorse per ottenere il massimo da [!DNL Target]. Abbiamo inoltre aggiunto un meccanismo di feedback direttamente nel menu [!UICONTROL Help] per facilitare la segnalazione dei problemi o la condivisione delle tue idee.

   * È stata migliorata la funzionalità di feedback NPS (Net Promoter Score), in modo che la modalità di sondaggio non disturbi il flusso di lavoro.

   * Le notifiche per [!DNL Target] non sono attualmente disponibili nel menu a discesa [!UICONTROL Notifications] nell&#39;intestazione.

  >[!NOTE]
  >
  >Con l’introduzione della nuova barra di navigazione, noterai anche alcune modifiche URL. Tutti i precedenti collegamenti impostati come segnalibro o preferiti continuano a funzionare, ma ti invitiamo a salvare come segnalibro i nuovi collegamenti, per accedervi più rapidamente.

### Target Standard/Premium 20.1.1 (4 febbraio 2020)

Target Standard/Premium 20.1.1 è una versione di manutenzione e include miglioramenti generali e di back-end. Sono inoltre incluse le seguenti correzioni:

* È stato risolto un problema a causa del quale il campo del server di tracciamento di Adobe Analytics risultava vuoto nella pagina Obiettivi e impostazioni per le attività esistenti di Adobe for Target (A4T). (TGT-35960)
* È stato risolto un problema nell’interfaccia utente che impediva la visualizzazione della selezione nel secondo elenco a discesa durante la creazione di un pubblico per l’affinità tra categorie. (TGT-36098)

## Note sulla versione - 2019 {#releases-2019}

### SDK Java di Target versione 1.1.0 (16 dicembre 2019)

* È stato aggiunto il supporto per la configurazione proxy in seguito al contributo open source di @hisham-hassan.

### SDK Java di Target versione 1.0.1 (11 novembre 2019)

Il seguente problema è stato risolto nella versione 1.0.1:

* Invio di ID di dati supplementari in una richiesta Target anche quando non è presente alcun cookie API visitatore.

### Piattaforma Target (31 ottobre 2019)

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| SDK Java | L’SDK Java di [!DNL Target] consente di implementare [!DNL Target] lato server. Questo SDK Java consente di integrare facilmente [!DNL Target] con altre soluzioni [!DNL Adobe Experience Cloud] come [!DNL Adobe Experience Cloud Identity Service], [!DNL Adobe Analytics] e [!DNL Adobe Audience Manager].<br>L’SDK Java introduce alcune best practice e semplifica l’integrazione con [!DNL Target] tramite l’API di consegna, in modo che i team di progettazione possano concentrarsi sulla logica di business. Di seguito sono riportate le funzioni principali introdotte nell’ultima versione:<ul><li>Supporto per preacquisizione e notifiche che consentono di ottimizzare le prestazioni tramite la memorizzazione in cache.</li><li>Supporto per l’ottimizzazione delle prestazioni quando si dispone di un’integrazione ibrida di [!DNL Target] sia sulle pagine web che sul lato server. Stiamo introducendo un’impostazione denominata `serverState` che viene compilata da esperienze recuperate tramite il lato server, in modo che at.js 2.2 non effettuerà più una chiamata aggiuntiva al server per recuperare le esperienze. Questo approccio ottimizza le prestazioni di caricamento delle pagine.</li><li>Supporto per il recupero di attività create dal Compositore esperienza visivo tramite l’SDK Java, reso possibile dalla nuova API di consegna.</li><li>Open source, in modo che gli sviluppatori possano contribuire all’[SDK Java di Target](https://github.com/adobe/target-java-sdk).</li></ul>Per ulteriori informazioni sull’SDK Java di Target, consulta l’articolo [Server-Side Optimization with the new Target Java SDK](https://medium.com/adobetech/server-side-optimization-with-the-new-target-java-sdk-421dc418a3f2), nell’Adobe Tech Blog. |

### Target Standard/Premium 19.10.2 (31 ottobre 2019)

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| ![Icona Premium](/help/main/assets/premium.png) Attributi con più valori | A volte è necessario utilizzare un campo con più valori. Prendi in considerazione gli esempi seguenti:<ul><li>Offri dei film agli utenti. Un dato film ha più attori.</li><li>Vendi biglietti per concerti. Un dato utente ha più band preferite.</li><li>Vendi vestiti. Una camicia è disponibile in più taglie.</li></ul>Per gestire i consigli in questi scenari, puoi trasmettere dati con più valori alla funzione Consigli di Target e utilizzare operatori speciali con più valori.<br>Per ulteriori informazioni, consulta [Utilizzare attributi con più valori](/help/main/c-recommendations/c-algorithms/work-with-multi-value-attributes.md). |

### Target Standard/Premium 19.10.1 (22 ottobre 2019)

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| ![Icona Premium](/help/main/assets/premium.png) Consigli basati sugli utenti<br> (24 ottobre 2019) | Consiglia gli articoli in base alla cronologia di navigazione, visualizzazione e acquisto di ogni visitatore. Questi articoli sono generalmente presentati al visitatore come “Consigliati per te”.<br>Questi criteri ti consentono di fornire contenuti ed esperienze personalizzati sia ai visitatori nuovi che a quelli di ritorno. L’elenco dei consigli è ponderato rispetto all’attività più recente del visitatore, viene aggiornato durante la sessione e diventa sempre più personalizzato man mano che il visitatore naviga sul sito.<br>Per ulteriori informazioni, consulta “Consigli basati sugli utenti” in [Criteri/Algoritmi](/help/main/c-recommendations/c-algorithms/algorithms.md#criteria-algorithms). |

**Navigazione in Adobe Experience Cloud**

* Quando accedi a [!DNL Adobe Experience Cloud], trovi la nuova navigazione dell’intestazione. Assomiglia molto alla navigazione precedente, con la barra nera nella parte superiore, ma offre i seguenti miglioramenti:

   * Passaggio più semplice tra le diverse organizzazioni [!DNL Identity Management System] (IMS) o verso una soluzione diversa.
   * Guida utente migliorata: i risultati della ricerca includono i risultati provenienti dalla documentazione di [!DNL Target], dai forum della community e nuovi contenuti video, che consentono di accedere più facilmente a più risorse per ottenere il massimo da [!DNL Target]. Abbiamo inoltre aggiunto un meccanismo di feedback direttamente nel menu [!UICONTROL Help] per facilitare la segnalazione dei problemi o la condivisione delle tue idee.

   * È stata migliorata la funzionalità di feedback NPS (Net Promoter Score), in modo che la modalità di sondaggio non disturbi il flusso di lavoro.

   * Le notifiche per [!DNL Target] non sono attualmente disponibili nel menu a discesa [!UICONTROL Notifications] nell&#39;intestazione.

  >[!NOTE]
  >
  >Queste funzioni verranno implementate gradualmente, e non saranno subito disponibili per tutti i clienti. Nel corso delle prossime settimane, presenteremo queste funzioni a partire dal rilascio di [!DNL Target Standard/Premium] 19.10.1 (22 ottobre 2019).
  >
  >Con l’introduzione della nuova barra di navigazione, noterai anche alcune modifiche URL. Tutti i precedenti collegamenti impostati come segnalibro o preferiti continuano a funzionare, ma ti invitiamo a salvare come segnalibro i nuovi collegamenti, per accedervi più rapidamente.

### at.js versioni 2.2 e 1.8 (10 ottobre 2019)

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| at.js versione 2.2<br>e<br>at.js versione 1.8 | Novità di queste versioni di at.js:<ul><li>Prestazioni migliorate quando si utilizzano sia Experience Cloud ID Service (ECID) v4.4 che at.js 2.2 o at.js 1.8 sulle pagine web.</li><li>In precedenza, l’ECID effettuava due chiamate di blocco prima che at.js potesse recuperare le esperienze. Questa funzione è stata ridotta a una singola chiamata, il che migliora notevolmente le prestazioni.</li></ul> Per usufruire di questi miglioramenti delle prestazioni, effettua l’aggiornamento a at.js 2.2 o at.js 1.8 insieme alla libreria ECID v4.4.<br>at.js 2.2 fornisce:<ul><li>**serverState**: impostazione disponibile in at.js v2.2+ che può essere utilizzata per ottimizzare le prestazioni della pagina quando viene implementata un’integrazione ibrida di Target. Per integrazione ibrida si intende l’utilizzo sia di at.js v2.2+ sul lato client che dell’API di consegna o di un SDK Target sul lato server per distribuire le esperienze. `serverState` consente a at.js v2.2+ di applicare le esperienze direttamente dal contenuto recuperato sul lato server e restituito al client come parte della pagina trasmessa.<br>Per ulteriori informazioni, consulta “serverState” in [targetGlobalSettings](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html?lang=it){target=_blank}.</li></ul> |

### Piattaforma Target (9 ottobre 2019)

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| SDK di Node.js versione 1.0 | SDK di Node.js di Target consente di implementare Target lato server.<br>L’SDK di Node.js consente di integrare facilmente Target con altre soluzioni Experience Cloud, come il servizio Adobe Experience Cloud Identity, Adobe Analytics e Adobe Audience Manager.<br>L’SDK di Node.js introduce alcune best practice e semplifica l’integrazione con Adobe Target tramite la nostra API di consegna, in modo che i team di progettazione possano concentrarsi sulla logica di business. Di seguito sono riportate le funzioni principali introdotte nell’ultima versione:<ul><li>Supporto per preacquisizione e notifiche che consentono di ottimizzare le prestazioni tramite la memorizzazione in cache.</li><li>Supporto per l’ottimizzazione delle prestazioni in caso di integrazione ibrida di Target sia sulle pagine web che sul lato server. Stiamo introducendo l’impostazione `serverState` che verrà compilata da esperienze recuperate tramite il lato server, in modo che at.js 2.2 non effettuerà più una chiamata aggiuntiva al server per recuperare le esperienze. Questo approccio ottimizza le prestazioni di caricamento delle pagine.</li><li> Supporto per il recupero di attività create dal Compositore esperienza visivo tramite SDK di Node.js, reso possibile dalla nuova API di consegna.</li><li>Open source, in modo che i tuoi sviluppatori possano contribuire all’SDK di Node.js.</li></ul> |
| API di consegna | È disponibile in produzione un endpoint API di consegna completamente nuovo (/v1/delivery). Le funzioni principali sono:<ul><li>Un endpoint per il recupero di esperienze per una o più mbox</li><li>Recupero delle attività create dal Compositore esperienza visivo tramite l’API</li><li>Supporto per il nuovo oggetto Viste, utilizzato per applicazioni a pagina singola e applicazioni mobili</li></ul> |

### Target Standard/Premium 19.9.2 (30 settembre 2019)

Questa versione di manutenzione include i seguenti miglioramenti:

* Diverse correzioni di sicurezza, compreso l’aggiornamento di sicurezza dell’editor Rich Text (RTE) nel Compositore esperienza visivo. (TGT-35383)
* È ora possibile aggiungere offerte Consigli a elementi diversi da DIV (ad esempio P, UL, H1), oltre a DIV, nelle attività di test A/B e di Targeting esperienza. (TGT-34333)
* Le notifiche degli eventi (icona a forma di campanello nell’interfaccia utente di Target) non sono più disponibili. Presto sarà disponibile un nuovo look per le notifiche.

### Target Standard/Premium 19.9.1 (10 settembre 2019)

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| ![Icona Premium](/help/main/assets/premium.png) Autorizzazioni Enterprise | Con la versione di Target di settembre 2019, le Autorizzazioni Enterprise forniranno ai clienti i seguenti controlli di accesso:<UL><li>Possibilità di scegliere le aree di lavoro a cui applicare l’integrazione.</li><li>Possibilità di applicare un ruolo all’integrazione Adobe I/O: Approvatore, Editor o Osservatore.</li></ul>Per istruzioni dettagliate e ulteriori informazioni, consulta [Consentire alle integrazioni Adobe I/O di accedere alle aree di lavoro e assegnare ruoli](/help/main/administrating-target/c-user-management/property-channel/configure-adobe-io-integration.md). |

### Target Standard/Premium 19.7.1 (24 luglio 2019) {#tgt-19-7-1}

Questa versione include le seguenti nuove funzionalità e miglioramenti:

(I codici tra parentesi sono per uso interno di Adobe.)

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| ![Badge Premium ](/help/main/assets/premium.png)<br>Consigli in attività di Test A/B e Targeting esperienza | Lo stato di un’offerta (algoritmo) di tipo Consigli viene visualizzato nella pagina Panoramica per le attività Test A/B e Targeting esperienza che contengono offerte di tipo Consigli. Gli stati includono: Risultati pronti, Risultati non pronti ed Errore di feed. (TGT-33649)<br>Visualizza [Consigli come offerta](/help/main/c-recommendations/recommendations-as-an-offer.md#status). |
| Supporto per il tracciamento tra domini diversi per at.js 2.0+ tramite la libreria Experience Cloud ID (ECID) | In precedenza, il tracciamento tra domini diversi non era supportato in at.js 2.*x*. Con questa versione, i clienti che usano at.js 2.0 o versioni successive possono utilizzare il tracciamento tra domini diversi tramite la libreria ECID. Per il corretto funzionamento del tracciamento tra domini diversi, la libreria ECID deve essere installata sulla pagina insieme at.js 2.0 o versione successiva. È necessario utilizzare la [libreria Experience Cloud ID 4.3.0+](https://experienceleague.adobe.com/docs/id-service/using/release-notes/release-notes.html?lang=it).<br>Consulta [Supporto del tracciamento tra più domini in at.js 2.x](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank}. |
| Supporto di Target per Apple ITP 2.1 e ITP 2.2 tramite la libreria Experience Cloud ID (ECID) 4.3 | Oggi, i clienti di Target possono mitigare Apple ITP 2.1 e ITP 2.2 sfruttando il programma di certificazione CNAME di Adobe.<br>Con questa versione, Target introduce un&#39;integrazione diretta con la libreria ECID 4.3, che sfrutta un cookie lato server per mitigare ITP 2.1 e ITP 2.2. Si consiglia vivamente ai clienti di Target di implementare la [libreria ECID 4.3+](https://experienceleague.adobe.com/docs/id-service/using/release-notes/release-notes.html?lang=it) insieme alla libreria JavaScript di Target per mitigare eventuali versioni future di ITP. La libreria ECID continuerà a essere migliorata per offrire una soluzione solida per i criteri dei cookie in continua evoluzione introdotti dai browser.<br>Consulta [Apple Intelligent Tracking Prevention (ITP) 2.x](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/privacy/apple-itp-2x.html?lang=it){target=_blank}. |

**Miglioramenti, correzioni e modifiche**

* È stato risolto un problema che impediva la cancellazione dei valori di esclusione nelle attività Consigli durante l’aggiunta di valori duplicati. (TGT-34996)
* Ora puoi rimuovere una progettazione in un’attività Consigli dalla pagina Targeting (passaggio 2 del flusso di lavoro guidato in tre parti). Per poter rimuovere una progettazione, devono essere selezionate più di una progettazione. (TGT-35118)
* È stato risolto un problema a causa del quale, per alcuni clienti, le schede dei criteri personalizzate non venivano caricate correttamente nell’interfaccia utente di Target o non potevano essere modificate. (TGT-35170)

### at.js versione 2.1.1 (24 luglio 2019)

Questa release di at.js è una versione di manutenzione e include i miglioramenti e le correzioni seguenti:

(I codici tra parentesi sono per uso interno di Adobe.)

* È stato risolto un problema a causa del quale venivano attivati più beacon quando si utilizzava la metrica Tracciamento dei clic nella pagina Obiettivi e impostazioni nel Compositore esperienza visivo. (TNT-32812)
* È stato corretto un problema a causa del quale `triggerView()` non poteva eseguire il rendering delle offerte più di una volta. (TNT-32780)
* È stato corretto un problema relativo a `triggerView()` per fare sì che la richiesta contenga informazioni Experience Cloud ID (ECID). (TNT-32776)
* È stato risolto un problema a causa del quale la notifica `triggerView()` non veniva attivata nonostante l’assenza di visualizzazioni salvate. (TNT-32614)
* È stato risolto un problema che provocava un errore a causa dell’utilizzo di decodeURIcomponent e si verificavano problemi se l’URL conteneva un parametro di stringa query non valido. (TNT-32710)
* Il flag beacon ora è impostato su “true” nel contesto di richieste di consegna inviate tramite l’API `Navigator.sendBeacon()`. (TNT-32683)
* È stato risolto un problema che, per alcuni clienti, impediva la visualizzazione delle offerte Consigli sui siti web. I clienti potevano vedere i contenuti delle offerte nella chiamata API per la consegna, ma l’offerta non veniva applicata al sito web. (TNT-32680)
* È stato risolto un problema di funzionamento imprevisto del tracciamento dei clic tra più esperienze. (TNT-32644)
* È stato risolto un problema che impediva ad at.js di applicare la seconda metrica dopo un errore nel rendering della prima metrica. (TNT-32628)
* È stato risolto un problema nel passare `mboxThirdPartyId` utilizzando la funzione `targetPageParams`, a causa del quale il payload della richiesta non veniva incluso nei parametri della query o nel payload della richiesta. (TNT-32613)
* È stato risolto un problema a causa del quale, nei browser basati su Chromium (incluso Google Chrome), venivano bloccate le risposte alle notifiche di visualizzazione o clic. (TNT-32290)

Per informazioni su questa versione e sulle versioni precedenti di at.js, consulta [Dettagli della versione di at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank}.

### Target Standard/Premium 19.6.1 (26 giugno 2019) {#tgt-19-6-1-historical}

Questa versione include le seguenti nuove funzionalità e miglioramenti:

(I codici tra parentesi sono per uso interno di Adobe.)

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| Compositore esperienza visivo | **Nuove opzioni del menu del compositore esperienza visivo**: quando fai clic su un elemento di pagina nel Compositore esperienza visivo, un menu mostra le opzioni disponibili per tale tipo di elemento.<ul><li>È ora possibile utilizzare l&#39;opzione [!UICONTROL Styles > Background] per modificare l&#39;immagine e il colore di sfondo per l&#39;elemento selezionato. (TGT-15001)</li></ul>Consulta *Stili* in [Opzioni del Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#styles).<br>**Miglioramenti apportati al tracciamento dei clic**: è stata migliorata la procedura per configurare il tracciamento nel Compositore esperienza visivo e Compositore esperienza visivo per applicazione a pagina singola.<ul><li>Quando selezioni gli elementi da usare nel tracciamento dei clic, i nomi di tutti gli elementi disponibili vengono visualizzati nel pannello Modifiche a destra, rendendo più facile e veloce la selezione degli elementi desiderati.</li><li>Nella pagina [!UICONTROL Goals & Settings] del flusso di lavoro guidato in tre parti per le attività viene visualizzato il numero di elementi selezionati per il tracciamento dei clic. Se passi il puntatore su questo numero vengono visualizzati i nomi di tutti gli elementi selezionati. (TGT-33878)</li></ul>Consulta [Tracciamento dei clic](/help/main/c-activities/r-success-metrics/click-tracking.md). |
| Compositore di esperienze visive su una singola pagina (SPA VEC) | **Flusso di lavoro guidato**: un nuovo flusso di lavoro guidato consente di comprendere in che modo configurare le impostazioni delle regole di consegna pagina per eseguire correttamente un’attività per l’app a pagina singola. (TGT-33718)<br> Consulta [Compositore esperienza visivo per app a pagina singola](/help/main/c-experiences/spa-visual-experience-composer.md#page-delivery-settings).<br>**Modifiche apportate alla funzione Clona**: ora puoi definire una modifica utilizzando il Compositore esperienza visivo per app a pagina singola e quindi clonarla per utilizzarla in altre viste nell’app a pagina singola. (TGT-33882)<br>Consulta [Compositore esperienza visivo per app a pagina singola](/help/main/c-experiences/spa-visual-experience-composer.md). |
| ![Badge Premium](/help/main/assets/premium.png) Automated Personalization e Targeting automatico | **Specificare come controllo un’esperienza specifica**: è possibile selezionare un’esperienza da utilizzare come controllo durante la creazione di un’attività AP e Targeting automatico. Questa funzione ti permette di indirizzare tutto il traffico di controllo a una specifica esperienza, in base alla percentuale di allocazione del traffico configurata nell’attività. Puoi quindi valutare i rapporti sulle prestazioni del traffico personalizzato rispetto al traffico verso l’esperienza di controllo. L’opzione di controllo corrente (esperienza distribuita in modo casuale) continuerà a essere disponibile. (TGT-32801, TGT-26572 e TGT-26571)<br>Consulta [Selezionare il controllo per un&#39;attività Automated Personalization o Targeting automatico](/help/main/c-activities/t-automated-personalization/experience-as-control.md).<br>**Rapporti Approfondimenti personalizzazione**: la denominazione intuitiva degli attributi quando un visitatore visualizza contenuti specifici in una posizione specifica fornisce informazioni più significative. (TGT-33421 e TGT-34957)<br>Consulta [Raccolta di dati per gli algoritmi di personalizzazione Target](/help/main/c-activities/t-automated-personalization/ap-data.md). |
| ![Badge Premium](/help/main/assets/premium.png) Consigli | È possibile utilizzare il pulsante di attivazione Consiglia articoli acquistati in precedenza durante la creazione della logica Articoli visualizzati di recente. (TGT-34030)<br>Per ulteriori informazioni, consulta [Articoli visualizzati di recente](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#previously-purchased) in “Creare criteri”. |
| Criteri per cookie SameSite di Google Chrome | Google ha recentemente annunciato che, a partire da Chrome 76, il cui rilascio è previsto per il 30 luglio 2019, gli sviluppatori devono specificare esplicitamente quali cookie possono funzionare tra siti web diversi e quali cookie possono tracciare gli utenti.<br>Nel settore si fanno grandi progressi nella creazione di un web più sicuro per i consumatori, e Target conferma il suo impegno costante nel distribuire esperienze personalizzate rispettando e superando le aspettative dei visitatori sulla privacy.<br>Consulta [Criteri per cookie SameSite di Google Chrome](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/privacy/google-chrome-samesite-cookie-policies.html?lang=it){target=_blank}. |

### at.js versione 2.1.0 (3 giugno 2019) {#atjs-210}

Siamo felici di annunciare le seguenti funzionalità in at.js 2.1.0:

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| Supporto di Adobe Opt-in | Adobe Opt-in è un metodo per semplificare le integrazioni delle soluzioni Adobe con le piattaforme di gestione del consenso.<br>Per ulteriori informazioni su Adobe Opt-in, consulta [Privacy e Regolamento generale sulla protezione dei dati (GDPR)](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/privacy/cmp-privacy-and-general-data-protection-regulation.html?lang=it){target=_blank}. |
| Conformità allo standard di settore CSP | at.js non utilizza più eval() per eseguire JavaScript. |
| Registrazione Analytics lato client | Fornisce ai clienti pieno controllo su come desiderano inviare dati analitici ad Adobe Analytics, lato client o lato server.<br>Per ulteriori informazioni, consulta [Registrazione Analytics lato client](/help/main/c-integrating-target-with-mac/a4t/before-implement.md#client-side) in *Prima dell’implementazione*. |
| Invio di notifiche | Consenti agli sviluppatori di inviare notifiche quando un’esperienza viene riprodotto dal codice anziché utilizzando `applyOffer()` o `applyOffers()`.<br>Per ulteriori informazioni, consulta [adobe.target.sendNotifications(options)](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/adobe-target-sendnotifications-atjs-21.html?lang=it){target=_blank}. |
| Dimensioni file ridotte | Dimensione di at.js è stata ridotta di circa il 24%. Le dimensioni ridotte del file migliorano le prestazioni di caricamento delle pagine e riducono il tempo necessario al download di at.js sulla pagina. |
| Aggiornamenti della documentazione di at.js | Per un elenco completo degli articoli aggiornati in seguito al rilascio di at.js 2.1.0, consulta le voci del 3 giugno 2019 in modifiche [Modifiche alla documentazione](/help/main/r-release-notes/doc-change.md). |

### [!DNL Target] Standard/Premium 19.5.1 (21 maggio 2019) {#tgt-19-5-1-historical}

(I codici tra parentesi sono per uso interno di [!DNL Adobe].)

#### Aggiornamenti delle funzioni

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| Compositore di esperienze visive su una singola pagina (SPA VEC) | Il Compositore di esperienze visive SPA include i seguenti miglioramenti per permetterti di lavorare in modo più rapido ed efficiente:<ul><li>Facendo clic su un’azione nell’app a pagina singola, viene evidenziato l’elemento del sito dove l’azione verrà applicata. Ogni azione del Compositore esperienza visivo creata in una visualizzazione presenta quattro icone corrispondenti: Informazioni, Modifica, Sposta ed Elimina. La nuova funzionalità Sposta di questa versione consente di spostare l’azione in un evento di caricamento pagina o in qualsiasi altra visualizzazione già esistente nel pannello delle modifiche. (TGT-33746)</li><li>Potrai eseguire molte azioni prima che la pagina si carichi nel Compositore esperienza visivo, anche qualora non possa essere caricata completamente (ad esempio, se il codice personalizzato non è più operativo). Nell’interfaccia utente di Target, le azioni che possono essere modificate solo dopo il caricamento del sito risultano disabilitate. (TGT-33851 e TGT-34149)</li></ul>Per ulteriori informazioni, consulta [Compositore esperienza visivo per app a pagina singola](/help/main/c-experiences/spa-visual-experience-composer.md). |

#### Miglioramenti, correzioni e modifiche

* Le icone della barra degli strumenti vengono visualizzate correttamente dopo aver annullato il caricamento di una pagina nel Compositore esperienza visivo. Se non è possibile eseguire azioni specifiche finché non è stato completato il caricamento della pagina, le icone della barra degli strumenti associate sono disattivate. (TGT-33811)

### [!DNL Target] Standard/Premium 19.4.2 (30 aprile 2019) {#release-19-4-2}

Questa versione include i miglioramenti, le modifiche e le funzioni seguenti:

(I codici tra parentesi sono per uso interno di [!DNL Adobe].)

#### Aggiornamenti delle funzioni

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| [!UICONTROL Visual Experience Composer] | I seguenti miglioramenti introdotti nel Compositore esperienza visivo di [!UICONTROL Visual Experience Composer] permettono di lavorare in modo più rapido ed efficiente:<ul><li>La funzione percorso DOM è ora disponibile quando si imposta il tracciamento dei clic.<br>Per ulteriori informazioni, consulta [Tracciamento dei clic](/help/main/c-activities/r-success-metrics/click-tracking.md#considerations).</li><li>Il pannello Stili consente di visualizzare o modificare il valore degli stili esistenti per l’elemento selezionato. Inoltre, è possibile aggiungere ulteriore formattazione.<br>Per accedere al pannello Stili, fai clic su un elemento di pagina nel Compositore esperienza visivo, quindi su [!UICONTROL Edit] > [!UICONTROL Styles].<br>Il pannello Stili viene visualizzato sul lato destro del Compositore esperienza visivo. Il pannello contiene un elenco di stili che consente di modificare o aggiungere formattazione all’elemento selezionato. Se hai familiarità con l’utilizzo di Cascading Style Sheet (CSS) o se ricevi del codice dallo sviluppatore, un editor CSS in tempo reale consente di visualizzare le modifiche e aggiungere stili.<br>Per ulteriori informazioni, vedi [Stili](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#styles) in *Opzioni del Compositore esperienza visivo*.</li><li>L’editor Rich Text supporta ora elementi HTML5 nidificati.<br>Le specifiche HTML5 consentono nuove combinazioni di tag per la nidificazione. La versione precedente dell’editor Rich Text non supportava la nuova nidificazione di tag consentita dalle specifiche HTML5. Di conseguenza, tutti gli elementi nidificati selezionati nel Compositore esperienza visivo non venivano gestiti correttamente, generando modifiche HTML indesiderate. (TGT-33618)<br>Per ulteriori informazioni, consulta [Modifica testo/HTML](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#edit-text-html) nelle *opzioni del Compositore esperienza visivo*.</li> |

#### Miglioramenti, correzioni e modifiche

* È stato migliorato il flusso di lavoro quando si eliminano le risorse nel Compositore esperienza visivo. Le risorse eliminate vengono rimosse da [!UICONTROL Offers library] e da [!DNL Scene7] (se applicabile). Le risorse eliminate non vengono più visualizzate nei risultati di ricerca. (TGT-31981)
* Adesso puoi eliminare le cartelle delle risorse anche se contengono immagini (cartelle non vuote). (TGT-33265)

  In precedenza, non era possibile eliminare una cartella non vuota dalla libreria delle offerte immagini di Target ([!UICONTROL Offers] > [!UICONTROL Image Offers]). Riceverai una &quot;Cartella non è vuota!&quot; se avessi tentato di eliminare la cartella dall’interfaccia utente. Con questa funzione, stiamo aggiungendo la funzionalità di eliminazione della cartella per rimuovere un’intera cartella contenente un numero qualsiasi di risorse e sottocartelle. Questa funzione è disponibile anche nell’interfaccia di Target e di Adobe Experience Cloud Assets.

   * Le cartelle non vuote nella libreria Offerta immagini possono essere eliminate. Se le immagini contenute nella cartella non sono indicate in nessuna attività, l’intera cartella e il relativo contenuto vengono eliminati. Se in un’attività vi sono riferimenti ad alcune immagini, vengono eliminate tutte le immagini senza riferimenti, mentre vengono mantenute quelle con riferimenti e le cartelle che le contengono.
   * Il rendering delle offerte immagini nel selettore delle risorse immagine risulta più rapido ed efficiente.

  Per ulteriori informazioni, consulta [Operazioni con il contenuto della libreria](/help/main/c-experiences/c-manage-content/assets-working.md). (TGT-32897)

* Abbiamo migliorato il rendering delle offerte immagini nel selettore di Assets. La visualizzazione e la selezione delle offerte immagini sono ora più veloci ed efficienti. (TGT-32897)
* Abbiamo migliorato la gestione dei reindirizzamenti agli URL quando si annulla il caricamento di una pagina nel Compositore esperienza visivo. (TGT-33815)
* Dopo aver selezionato una raccolta [!UICONTROL Recommendations] dal selettore delle raccolte, è necessario fare clic sul pulsante [!UICONTROL Save]. Questo flusso di lavoro è in linea con gli altri flussi di lavoro all’interno di [!DNL Target]. (TGT-33205)
* È stato risolto un problema a causa del quale una piccola serie di rapporti Approfondimenti restituiva tassi di conversione dello 0% invece dei tassi di conversione effettivi. (TNT-32125)

### [!DNL Target] Standard/Premium 19.4.1 (15 aprile 2019) {#release-19-4-1}

Questa è una versione di manutenzione e include la seguente modifica:

(I codici tra parentesi sono per uso interno di [!DNL Adobe].)

* L’interfaccia utente di [!DNL Adobe Experience Cloud] è stata aggiornata per riflettere le modifiche a livello di branding e prodotto. (TGT-33546, TGT-33272 e TGT-33331)

#### [!DNL Target] Standard/Premium 19.3.1 (29 marzo 2019) {#release-19-3-1}

Questa versione include i miglioramenti, le modifiche e le funzioni seguenti:

(I codici tra parentesi sono per uso interno di [!DNL Adobe].)

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| Compositore esperienza visivo | I seguenti miglioramenti introdotti nel Compositore esperienza visivo permettono di lavorare in modo più rapido ed efficiente:<ul><li>Ora è possibile annullare il caricamento di un sito Web nel Compositore esperienza visivo per sbloccare la modifica di un’attività. Questo miglioramento è utile, ad esempio, se desideri apportare una piccola modifica a un’attività, rivederne le impostazioni o aggiungere del codice personalizzato, senza attendere che il sito venga caricato. (TGT-31288)<br>Consulta [Annullare il caricamento di una pagina all’interno del Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md#cancel-loading).</li><li>Potrai eseguire molte azioni prima che la pagina si carichi nel Compositore esperienza visivo, anche qualora non possa essere caricata completamente (ad esempio, se il codice personalizzato non è più operativo). Nell’interfaccia utente di Target, le azioni che possono essere modificate solo dopo il caricamento del sito risultano disabilitate. (TGT-31288, TGT-31611 e TGT-32602)<br>Consulta [Modificare una pagina durante il suo caricamento o dopo il suo mancato caricamento](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md#loading).</li><li>Ora nel Compositore esperienza visivo viene visualizzato il percorso DOM, per consentirti di selezionare facilmente l’elemento appropriato durante la creazione o la modifica delle esperienze. (TGT-13422)<br>Consulta [Navigare tra gli elementi utilizzando il percorso DOM](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path).</li></ul> |

### at.js versione 2.0.1 (19 marzo 2019) {#atjs201}

Questa è una versione di manutenzione e include i miglioramenti e le correzioni seguenti:

(I codici tra parentesi sono per uso interno di [!DNL Adobe].)

* È stata risolta una situazione di tipo “race condition” nel codice di polling DOM che causava eccezioni JavaScript per alcuni clienti. (TNT-31869)
* Le notifiche di rendering delle visualizzazioni sono state disaccoppiate dai gestori di eventi di tracciamento dei clic. Inizialmente, Target non inviava notifiche se non era possibile allegare gestori di eventi di tracciamento dei clic a una visualizzazione riprodotta. Target invia ora una notifica della visualizzazione anche quando non vengono trovati elementi di clic. (TNT-31969)
* È stato risolto un problema per cui il flag di reindirizzamento dell’evento della richiesta riuscita era sempre impostato su true. (TNT-31907)
* È stato risolto un problema che causava la registrazione con successo dell’azione di riorganizzazione del Compositore esperienza visivo, anche quando mancavano elementi. (TNT-31924)
* È stato risolto un problema che causava la mancata inclusione del token di proprietà delle Autorizzazioni Enterprise per alcuni clienti. (TNT-31999)

>[!NOTE]
>
>[!DNL Adobe]Se hai bisogno del supporto per le funzioni di Opt-In per i requisiti del Regolamento generale sulla protezione dei dati (GDPR), devi attualmente utilizzare at.js 1.7.1. Il supporto Opt-in non è al momento disponibile in at.js 2.*x*.

### at.js versione 1.7.1 (19 marzo 2019) {#atjs171}

Questa è una versione di manutenzione e include la seguente correzione:

(I codici tra parentesi sono per uso interno di [!DNL Adobe].)

* È stata risolta una situazione di tipo “race condition” nel codice di polling DOM che causava eccezioni JavaScript per alcuni clienti. (TNT-31869)

### Modifiche alla piattaforma (19 febbraio 2019) {#atjs2}

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| at.js versione 2.0.0<br>19 febbraio 2019 | at.js 2.x è ora disponibile.<br>La versione più recente di at.js offre set di funzioni avanzati che consentono all’azienda di eseguire personalizzazioni su tecnologie lato client di nuova generazione. Questa nuova versione si concentra sull&#39;aggiornamento di at.js per garantire interazioni in sintonia con le applicazioni a pagina singola.<br>Di seguito sono riportati alcuni vantaggi dell’utilizzo di at.js 2.x che non sono disponibili nelle versioni precedenti:<ul><li>La capacità di memorizzare nella cache tutte le offerte al caricamento di pagina per ridurre più chiamate al server a una singola chiamata al server.</li><li>Migliora enormemente le esperienze degli utenti finali sul sito, in quanto le offerte appaiono immediatamente tramite la cache senza l’implementazione di chiamate al server tradizionali.</li><li>Una semplice riga di codice e una configurazione per sviluppatori una tantum per consentire agli esperti di marketing di creare ed eseguire attività A/B e di esperienza (XT) tramite il Compositore esperienza visivo sulle applicazioni a pagina singola.</li></ul>at.js 2.x introduce le seguenti nuove funzioni:<ul><li>getOffers()</li><li>applyOffers()</li><li>triggerView()</li></ul>Le seguenti funzioni sono state rese obsolete con l’introduzione di at.js 2.x:<ul><li>mboxCreate()</li><li>mboxDefine</li><li>registerExtension()</li></ul>Per ulteriori informazioni, consulta [Aggiornamento da at.js 1.x a at.js 2.x](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank} e [Funzioni di at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank}.<br>**Nota**: se hai bisogno del supporto di Adobe Opt-In per il [Regolamento generale sulla protezione dei dati](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/privacy/cmp-privacy-and-general-data-protection-regulation.html?lang=it){target=_blank} (RGPD){target=_blank}, al momento devi utilizzare at.js 1.7.0. Il supporto per Opt-in non è disponibile in at.js 2.x. |
| at.js versione 1.7.0<br>14 febbraio 2019 | È disponibile at.js 1.7.0.<br>Questa versione include il supporto di Adobe Opt-in. Adobe Opt-in è un metodo per semplificare le integrazioni delle soluzioni Adobe con le piattaforme di gestione del consenso.<br>Per ulteriori informazioni su Adobe Opt-in, consulta [Privacy e Regolamento generale sulla protezione dei dati](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/privacy/cmp-privacy-and-general-data-protection-regulation.html?lang=it){target=_blank} (RGPD){target=_blank}.<br>Questa versione risolve anche un problema in cui Target potrebbe sostituire i parametri degli URL reindirizzati con parametri provenienti dall’URL di reindirizzamento.<br>**Nota**: se hai bisogno del supporto di Adobe Opt-in per i requisiti GDPR, al momento devi utilizzare at.js 1.7.0. Il supporto di Opt-in non è disponibile in at.js 2.x.<br>Per un elenco di tutte le versioni, consulta [Dettagli sulle versioni di at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank}. |

### [!DNL Target] Standard/Premium 19.2.1 (19 febbraio 2019) {#target-19-2-1}

Questa versione include i miglioramenti, le modifiche e le funzioni seguenti:

(I codici tra parentesi sono per uso interno di [!DNL Adobe].)

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| Compositore esperienza visivo per app a pagina singola | Il compositore esperienza visivo (VEC) per app a pagina singola (SPA) consente agli addetti al marketing di creare test e di personalizzare contenuti nelle SPA in modalità fai-da-te senza dover dipendere sempre dagli sviluppatori. Il Compositore esperienza visivo può essere utilizzato per creare attività nei framework più popolari, come ad esempio React e Angular. (TGT-27916)<br>Per ulteriori informazioni, consulta [Compositore esperienza visivo per app a pagina singola](/help/main/c-experiences/spa-visual-experience-composer.md) e [Integrazione delle applicazioni a pagina singola](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/deploy-at-js/target-atjs-single-page-application.html?lang=it){target=_blank}.<br>Oltre all’articolo precedente, sono presenti molti argomenti relativi ad applicazioni a pagina singola e at.js che trattano di questa funzione e come implementarla. Per ulteriori informazioni, consulta [Modifiche alla documentazione](/help/main/r-release-notes/doc-change.md). |
| Compositore esperienza visivo | I seguenti miglioramenti introdotti nel Compositore esperienza visivo permettono di lavorare in modo più rapido ed efficiente:<ul><li>Sono ora disponibili le opzioni Inserisci prima e Inserisci dopo nel Compositore esperienza visivo durante l’inserimento dei [frammenti esperienza AEM](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md). Consulta [Opzioni del Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md). (TGT-32385)</li><li>L’estensione [!DNL Adobe Target] VEC Helper per il browser Google Chrome consente di caricare i siti web in modo affidabile nel Compositore esperienza visivo (VEC), per creare e verificare rapidamente le esperienze web. Consulta [Estensione VEC  Helper](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md). (TGT-32746)</li></ul> |
| ![Badge Premium](/help/main/assets/premium.png)<br>Consigli in [!UICONTROL A/B Test] e [!UICONTROL Experience Targeting] attività | È ora possibile includere i consigli nelle attività [!UICONTROL A/B Test] (inclusi [!UICONTROL Auto-Allocate] e [!UICONTROL Auto-Target]) e [!UICONTROL Experience Targeting] (XT). Questo apre a funzionalità tutte nuove, ad esempio:<ul><li>Contenuto relativo e non relativo a consigli di test e targeting all’interno della stessa attività.</li><li>Facile sperimentazione con il posizionamento di consigli sulla pagina, tra cui l’ordine di più consigli.</li><li>Invio automatico di traffico all&#39;esperienza di consigli con le prestazioni migliori tramite [!UICONTROL Auto-Allocate].</li><li>Assegnazione dinamica di visitatori a esperienze di consigli su misura in base ai singoli profili tramite [!UICONTROL Auto-Target].</li></ul>Per iniziare, crea un&#39;attività [!UICONTROL A/B Test] o [!UICONTROL Experience Targeting] tramite il Compositore esperienza visivo e utilizza l&#39;azione [!UICONTROL Insert Before], [!UICONTROL Insert After] o [!UICONTROL Replace With] per aggiungere consigli a un&#39;esperienza. (RECS-6166)<br>Per ulteriori informazioni, consulta [Consigli come offerta](/help/main/c-recommendations/recommendations-as-an-offer.md). |
| ![Badge Premium ](/help/main/assets/premium.png)<br> Supporto di autorizzazioni Enterprise nelle API di Target | [Le API dell’amministratore Adobe Target](https://developers.adobetarget.com/api/#admin-apis) ora sfrutteranno appieno le stesse funzionalità di autorizzazioni Enterprise disponibili nell’interfaccia utente di Target. Dal **21 febbraio 2019**, gli amministratori di sistema possono accedere ai dati dei rapporti in modo programmatico, nonché creare e gestire attività, offerte e pubblico in qualsiasi area di lavoro. In precedenza, queste azioni erano disponibili solo nell’area di lavoro predefinita. Il supporto per le attività di Personalizzazione automatizzata (AP) sarà disponibile in una versione futura. |

**Miglioramenti, correzioni e modifiche**

* Per migliorare la sicurezza, [!DNL Target] ora evita di accedere endpoint di metadati Amazon Web Services (AWS) durante il caricamento del Compositore esperienza visivo. (TGT-33129)

### Modifiche alla piattaforma (gennaio 2019) {#platform-19-1-previous}

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| Targeting<br>25 gennaio 2019 | Apportate modifiche al modo in cui il targeting abbina la funzione confronti “equals” con valori non decimali e decimali restituiti da script di profilo o da qualsiasi altra origine di input, come parametri mbox, parametri di profilo, ecc.<br>Per ulteriori informazioni, consulta [Domande frequenti su Target e tipi di pubblico](/help/main/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md). |
| Script di profilo<br>17 gennaio 2019 | Per motivi di prestazioni, si consiglia di restituire un valore restituito non superiore ai 256 caratteri.<br>Per un valore di ritorno Stringa, se la dimensione del valore restituito supera i 2048 caratteri, il sistema disabilita lo script.<br>Per un valore di ritorno Array, se la dimensione dei valori concatenati dell’array supera i 2048 caratteri, il sistema disabilita lo script.<br>Per ulteriori informazioni sui limiti dei caratteri e altri limiti (dimensioni dell&#39;offerta, pubblico, profili, valori, parametri, ecc.) che influiscono sulle attività e su altri elementi in Target, vedi [Limiti](/help/main/r-troubleshooting-target/target-limits.md). |
| at.js<br>16 gennaio 2019 | at.js 1.6.4 è una versione di manutenzione e risolve i seguenti problemi:<ul><li>È stata corretta una situazione di tipo “race condition” critica in Microsoft Internet Explorer 11 che causava l’applicazione di offerte duplicate. (TNT-31374)</li><li>Risolto un problema che comprometteva il tracciamento dei clic in caso di offerta predefinita con un click-token e offerte HTML. (TNT-31493)</li><li>Esteso il cookie mboxEdgeCluster con ogni richiesta di Target. Questa opzione si utilizza solo quando mboxEdgeOverride è attivo. (TNT-31485)</li></ul> |

### [!DNL Target] Standard/Premium 19.1.1 (22 gennaio 2019) {#release-19-1-1-previous}

Questa versione include i miglioramenti, le modifiche e le funzioni seguenti:

(I codici tra parentesi sono per uso interno di Adobe.)

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| Supporto del ![badge Target Premium](/help/main/assets/premium.png)<br/>[!UICONTROL Enterprise Permissions] in [!DNL Target] API | [Le API dell’amministratore Adobe Target](https://developers.adobetarget.com/api/#admin-apis) ora sfrutteranno appieno le stesse funzionalità di autorizzazioni Enterprise disponibili nell’interfaccia utente di Target. A partire **dal 21 febbraio 2019**, gli amministratori di sistema potranno accedere ai dati dei rapporti in modo programmatico, nonché creare e gestire attività, offerte e pubblico in qualsiasi area di lavoro. In precedenza, queste azioni erano disponibili solo nell’area di lavoro predefinita. Il supporto per le attività di Automated Personalization (AP) sarà disponibile in una versione futura. |
| ![Badge Target Premium](/help/main/assets/premium.png)<br/>[!UICONTROL Recommendations]: filtrare raccolte ed esclusioni per ambiente (gruppo di host) | È ora possibile visualizzare in anteprima il contenuto di [!UICONTROL Recommendations] raccolte ed esclusioni per un ambiente selezionato (gruppo di host).<br/>In precedenza, quando si visualizzava una raccolta o un&#39;esclusione, gli elementi visualizzati erano risultati per il gruppo di host predefinito (specificato in [!UICONTROL Recommendations > Settings > Default Host Group]).<br/>Ora, quando crei o aggiorni una raccolta o un&#39;esclusione, puoi utilizzare il selettore [!UICONTROL Environment] per scegliere l&#39;ambiente di cui visualizzare i risultati in anteprima. Il nuovo filtro [!UICONTROL Environment] ti consente di risparmiare tempo e fatica, perché non dovrai più passare alla pagina [!UICONTROL Settings] per selezionare il gruppo di host predefinito appropriato prima di creare o modificare raccolte ed esclusioni.<br/>**Nota:** dopo aver modificato l&#39;ambiente selezionato, è necessario fare clic su [!UICONTROL Search] per aggiornare i risultati restituiti.<br/>Il nuovo filtro [!UICONTROL Environment] è disponibile nelle seguenti posizioni nell&#39;interfaccia utente [!DNL Target]:<ul><li>[!UICONTROL Catalog Search] ([!UICONTROL Recommendations > Catalog Search])</li><li>Finestra di dialogo [!UICONTROL Create Collection] ([!UICONTROL Recommendations > Collections > Create New])</li><li>Finestra di dialogo [!UICONTROL Update Collection] ([!UICONTROL Recommendations > Collections > Edit])</li><li>Finestra di dialogo [!UICONTROL Create Exclusion] ([!UICONTROL Recommendations > Exclusions > Create New])</li><li>Finestra di dialogo [!UICONTROL Update Exclusion] ([!UICONTROL Recommendations > Exclusions > Edit])</li></ul><br>Per maggiori informazioni, vedi i seguenti argomenti:<uL><li>[Raccolte](/help/main/c-recommendations/c-products/collections.md)</li><li>[Esclusioni](/help/main/c-recommendations/c-products/exclusions.md)</li><li>[Ricerca nel catalogo](/help/main/c-recommendations/c-products/catalog-search.md)</li><li>[Impostazioni](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html?lang=it){target=_blank}</li><li>[Consigli: filtrare raccolte ed esclusioni per ambiente (gruppo di host)](/help/main/administrating-target/hosts.md)</li></ul>(TGT-20622)</ul> |

**Miglioramenti, correzioni e modifiche**

* Risolto un problema che causava la disattivazione del pulsante Salva quando l’utente accedeva tramite la finestra di dialogo di accesso alla scadenza della sessione durante la modifica di un pubblico. (TGT-32722)

## Note sulla versione - 2018 {#reference_36ACC83E135A41F28104C44755C26D5B}

### Piattaforma (15 novembre 2018) {#section_484A56774E004282B98FFFF851E4E670}

<table id="table_7320E43397D2471FA313A9D6FC21E55F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzionalità/Miglioramento </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>at.js 1.6.3 </p> </td> 
   <td colname="col2"> <p>È ora disponibile la versione 1.6.3 di at.js. </p> <p> 
     <ul id="ul_2C7CB74B1AAF4B52B6EB382977F7DC28"> 
      <li id="li_07CF8EDB25E24A7AB9B7A0F3402BAEB1"> <p>I selettori sono ora in sequenza CSS se contengono ID o classi CSS che iniziano con una cifra, due trattini o un trattino seguito da una cifra (ad esempio #-123). (TNT-31061) </p> </li> 
      <li id="li_6504E90D7C534A1BB9A2DE8510CE3B90"> <p>Risolto un problema introdotto con at.js 1.6.2 per cui le offerte del Compositore esperienza visivo di diverse attività che si applicavano allo stesso selettore CSS non rispettavano la priorità delle attività. (TNT-31052) </p> </li> 
      <li id="li_D347CA513F1240E4BF79D757287AB30C"> <p>Corretto un problema con il timeout di una promessa in ambienti in cui non era presente alcun supporto nativo per le promesse. (TNT-30974) </p> </li> 
      <li id="li_17F41A84CCFF41D7993E35DE10F87066"> <p>L’acquisizione e la segnalazione dei problemi ora avviene correttamente tramite l’evento di rendering del contenuto non riuscito. In precedenza, il sistema poteva segnalare la corretta esecuzione di JavaScript anche in caso contrario. (TNT-30599) </p> </li> 
     </ul> </p> <p>Per ulteriori informazioni, consulta <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it" format="dita" scope="local">Dettagli della versione di at.js</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 18.11.1 (12 novembre 2018) {#section_6BBA8B1EE9D241C28E12856A375E97F6}

La versione di [!DNL Target] Standard/Premium del 12 novembre include miglioramenti di back-end, correzioni e modifiche. I report [!UICONTROL Personalization Insights] saranno disponibili il 14 novembre.

<table id="table_EF529199D1C741F7BDBC9C41A37B7D26"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzionalità/Miglioramento </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" class="premium"> <p>Rapporti Approfondimenti personalizzazione </p> <p> <p>Nota: disponibile il 14 novembre 2018. </p> </p> </td> 
   <td colname="col2"> <p>Sono disponibili due rapporti specializzati per gli utenti di attività di <span class="wintitle">Automated Personalization (AP)</span> e <span class="wintitle">Targeting automatico (AT)</span>: </p> <p> 
     <ul id="ul_C338AC34C57C49E1A8DFA471167EC40A"> 
      <li id="li_2329BFC8CC524EBBA99C2F8EDC745B90"> <p><b><span class="wintitle"> Segmenti automatizzati</span>:</b> i vari visitatori rispondono in modo diverso alle offerte/esperienze nell'attività di AP/AT. Questo rapporto mostra come i diversi segmenti automatizzati definiti dai modelli di personalizzazione di Target rispondono alle offerte/esperienze dell'attività. </p> </li> 
      <li id="li_48556C9BAD48476DA00DD666F5265E2B"> <p><b><span class="wintitle"> Attributi importanti</span>:</b> nelle varie attività, i vari attributi possono essere più o meno importanti per il modo in cui il modello decide di effettuare la personalizzazione. Questo rapporto mostra gli attributi principali che hanno influenzato il modello e la loro importanza relativa. </p> </li> 
     </ul> </p> <p>Consulta <a href="/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767" format="dita" scope="local"> rapporti Approfondimenti Personalization</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 18.10.1 (24 ottobre 2018) {#section_FA37BF4E840B424E8BC4791D7234FE2A}

Questa versione include i miglioramenti e le funzioni seguenti:

(I codici tra parentesi sono per uso interno di Adobe.)

<table id="table_B1911F55CCE1428881D258380A8254A9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzionalità/Miglioramento </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Esperienze </p> </td> 
   <td colname="col2"> <p>È ora possibile copiare un'esperienza in un'attività di Targeting esperienza (XT) così da poter apportare modifiche minori senza dover ricreare l'esperienza da zero. Questa funzionalità era già disponibile per i test A/B. (TGT-31504) </p> <p>Consulta <a href="https://experienceleague.adobe.com/docs/target/using/activities/experience-targeting/create-targeting/xt-add-experience.html?lang=it" format="html" scope="external">Creare esperienze.</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Offerte nelle attività di Automated Personalization (AP) </p> </td> 
   <td colname="col2"> <p>Nella versione di settembre 2018 è stato aggiunto un miglioramento che consente di filtrare le offerte in base ai gruppi di rapporti. È ora possibile filtrare le Offerte non assegnate così da poter assegnare un gruppo di rapporti a un'offerta attualmente non assegnata ad alcun gruppo di rapporti. (TGT-31882) </p> <p>Consulta <a href="https://experienceleague.adobe.com/docs/target/using/activities/automated-personalization/create-ap-activity.html?lang=it" format="html" scope="external">Creare un'attività di Automated Personalization.</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Origine per la generazione di rapporti per le attività </p> </td> 
   <td colname="col2"> <p>In <span class="wintitle">Amministrazione</span> &gt; <span class="wintitle">Compositore esperienza visivo</span>, è possibile selezionare l’origine per la generazione di rapporti sulle attività, in <span class="keyword"> Target </span> o <span class="keyword"> Adobe Analytics </span>. È inoltre possibile selezionare l'origine per la generazione di rapporti per ogni attività. </p> <p>A partire da questa versione, è necessario tenere presenti alcune importanti considerazioni sul flusso di lavoro quando si sceglie l'origine per la generazione di rapporti in <span class="wintitle">Preferenze</span> o per attività.</p></td> 
  </tr> 
 </tbody> 
</table>

**Miglioramenti, correzioni e modifiche**

Questa versione di [!DNL Target] include i seguenti miglioramenti, correzioni e modifiche:

* Migliorata la gestione dei tipi di pubblico eliminati in Adobe Audience Manager (AAM) a cui si fa riferimento nelle attività di Target. (TGT-23338)

   * Se un pubblico è stato eliminato in AAM, viene visualizzata un&#39;icona di avviso sia nell&#39;elenco [!UICONTROL Audience] che nel selettore del pubblico. Un suggerimento nell&#39;interfaccia utente indica inoltre che il pubblico è stato eliminato in AAM.
   * Se si tenta di combinare più tipi di pubblico con un pubblico eliminato o se si tenta di salvare un&#39;attività che fa riferimento a un pubblico eliminato, viene visualizzato un messaggio di avviso.

  Consulta [Informazioni sui tipi di pubblico](https://experienceleague.adobe.com/docs/target/using/audiences/create-audiences/audiences.html?lang=it).

* È stato risolto un problema che impediva agli utenti in determinate situazioni di creare un&#39;attività quando Adobe Analytics era selezionato come origine per la generazione di rapporti nella pagina [!UICONTROL Administration]. Gli utenti visualizzavano il messaggio “Seleziona una suite di rapporti” anche se non veniva data la possibilità di selezionarla. (TGT-31968)

### Piattaforma (19 ottobre 2018)

<table id="table_7320E43397D2471FA313A9D6FC21E55F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzionalità/Miglioramento </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>at.js 1.6.2 </p> </td> 
   <td colname="col2"> <p>Questa è una versione di manutenzione e risolve il seguente problema: </p> <p> 
     <ul id="ul_2C7CB74B1AAF4B52B6EB382977F7DC28"> 
      <li id="li_07CF8EDB25E24A7AB9B7A0F3402BAEB1"> <p>Risolto un problema che portava a un ciclo “async” infinito in alcuni siti clienti. </p> </li> 
     </ul> </p> <p> <p>Importante: in aggiunta, la versione 1.6.2 di at.js contiene tutti i miglioramenti e le correzioni inclusi nelle versioni 1.6.1 e 1.6.0 di at.js. Queste versioni non sono più disponibili per il download. Si consiglia di eseguire l'aggiornamento alla versione 1.6.2 se si utilizza la versione 1.6.1 o 1.6.0. </p> </p> <p>Per ulteriori informazioni, consulta <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it" format="html" scope="external">Dettagli della versione di at.js</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 18.9.1 (26 settembre 2018) {#section_95CF405C95E44DBEA3CB308FDD5071CD}

<!-- 

target/r_release-notes-2018.xml

 -->

Questa versione include i miglioramenti e le funzioni seguenti:

>[!NOTE]
>
>I codici tra parentesi sono per uso interno di Adobe.

<table id="table_7ABC8E7477194D4C8C9E82ECE60E3498"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzionalità/Miglioramento </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" class="premium"> <p>Offerte nelle attività di Automated Personalization (AP) </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_9C39ACD865CE4167BDBAA093EDFD3B68"> 
      <li id="li_19710BA5965E4F858B128E1E9FF89471"> <p>È ora possibile utilizzare più offerte dalla stessa posizione in un gruppo di esclusione. Per un numero elevato di esclusioni (nell’ordine delle migliaia), si noterà inoltre il caricamento più rapido della finestra di dialogo Gestione contenuto e della pagina di anteprima durante la creazione di un'attività di Automated Personalization (AP). (TGT-31329) Consulta <a href="/help/main/c-activities/t-automated-personalization/managing-exclusions.md#topic_30B4E4F89C914EB2B20B038C0299ED2E" format="dita" scope="local"> Gestire le esclusioni </a>. </p> </li> 
      <li id="li_542C66E2998541BC87D0A96F4672C665"> <p>È ora possibile filtrare le offerte in base ai gruppi di rapporti. (TGT-31643) Vedere <a href="/help/main/c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Creazione di un'attività Automated Personalization </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Compositore esperienza visivo </p> </td> 
   <td colname="col2"> <p>È stata aggiunta un'azione <span class="wintitle">Inserisci prima</span> al (VEC). Essa è simile all'opzione esistente <span class="wintitle">Inserisci dopo</span>. Quando si seleziona un elemento nella pagina, è possibile fare clic su <span class="wintitle">Inserisci prima</span> e scegliere se si desidera inserire un'immagine, un HTML o un testo. L’elemento inserito viene visualizzato prima dell’elemento selezionato. (TGT-30473) Consulta <a href="/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local">Opzioni del Compositore esperienza visivo.</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Miglioramenti, correzioni e modifiche**

Questa versione di [!DNL Target] include i seguenti miglioramenti, correzioni e modifiche:

* L’aspetto delle schede Criteri è stato aggiornato per essere più intuitivo e facile da usare. (TGT-30469)
* Miglioramenti delle prestazioni nell&#39;interfaccia utente per un caricamento più rapido delle pagine.

### Target Standard/Premium 18.8.1 (21 agosto 2018) {#section_66A0030993D54565BE30E56AC9CAC1DA}

Questa versione include i miglioramenti e le funzioni seguenti:

>[!NOTE]
>
>I codici tra parentesi sono per uso interno di Adobe.

<table id="table_4785030753B24AA1A973E1DF790B83DD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzionalità/Miglioramento </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" class="premium"> <p>Rapporti Approfondimenti personalizzazione </p> </td> 
   <td colname="col2"> <p>Accedi a rapporti specializzati per le attività di Automated Personalization e Targeting automatico: </p> <p> 
     <ul id="ul_54652C5AE0984657BB9A0E46673CB2F1"> 
      <li id="li_0807959BA7D94114BE47A43D3454CAB4"> <p><b>Segmenti automatizzati:</b> scopri come diversi segmenti automatizzati definiti dai modelli di personalizzazione di Target rispondono alle offerte o esperienze della tua attività. </p> </li> 
      <li id="li_48210B1E4EB24288B96CDECAF1CEE34A"> <p><b>Classifica attributi modello:</b> scopri i principali attributi che hanno influenzato i modelli di personalizzazione di Target e l’importanza relativa di ciascun attributo. </p> </li> 
     </ul> </p> <p> <p>Nota: questa funzione sarà presto disponibile. Resta in attesa per un annuncio della data esatta in cui questa funzione sarà pronta per l'uso. </p> </p> <p>Consulta <a href="/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767" format="dita" scope="local"> rapporti Approfondimenti Personalization </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Compositore esperienza visivo </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_406B95728467496CA6CC5892F88B69FE"> 
      <li id="li_6D717868FB204A3A95832E709773B424"> <p>Puoi ancorare il pannello Modifiche in verticale lungo il lato dell’interfaccia di Target oppure in orizzontale lungo il bordo inferiore. </p> <p>Consulta <a href="/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md#concept_B3A6E9EE3A60406DB640E205EA1745B5" format="dita" scope="local">Modifiche.</a> </p> </li> 
      <li id="li_27750AFBCB3E4CB8B0B53592B2447E59"> <p>Le varie azioni del Compositore esperienza visivo sono state raggruppate per offrire maggiore rapidità ed efficienza. (TGT-30472) </p> <p>Consulta <a href="/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local">Opzioni del Compositore esperienza visivo.</a> </p> </li> 
      <li id="li_27FEBEE245E64ADF9ADF561C6CBBDE8F"> <p>Grazie alla finestra di modifica più grande puoi modificare le offerte in modo più efficiente. (TGT-31052) </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Suggerimenti </p> </td> 
   <td colname="col2"> <p>Per sfruttare al massimo Adobe Target, scopri di più sulle sue funzioni e come sfruttarle. La funzionalità Suggerimenti viene visualizzata nella pagina Elenco attività e fornisce collegamenti a video, casi d'uso, blog, documentazione e molto altro ancora. Diventa un utente esperto di Target! </p> <p>Consulta <a href="/help/main/c-activities/activities.md#section_F77F30A246A14B538D9363B7F3639F97" format="dita" scope="local">Suggerimenti.</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Serie di webinar sui fondamenti di Target </p> </td> 
   <td colname="col2"> <p>Partecipa alla nuova serie di webinar sui fondamenti di Target, una serie Customer Success offerta dalla community. </p> <p> Il prossimo webinar, Best Practices in Reporting &amp; Value Socialization, è in programma per il 22 agosto 2018 dalle 8 alle 9 (PDT). </p> <p>Guarda la <a href="/help/main/cmp-resources-and-contact-information.md#concept_11902FAC95C64479AABE020557A7EEE4" format="dita" scope="local">serie di webinar sui concetti di base di Target.</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Miglioramenti, correzioni e modifiche**

Questa versione di [!DNL Target] include i seguenti miglioramenti, correzioni e modifiche:

* Abbiamo aggiunto diversi miglioramenti per rendere Target ancora più sicuro. (TGT-31090, TGT-31089, TGT-31143)

### Target Standard/Premium 18.7.1 (25 luglio 2018) {#section_A4A9C20EB677455F84FF0BA389F645E5}

Questa versione include i miglioramenti e le funzioni seguenti:

>[!NOTE]
>
>I codici tra parentesi sono per uso interno di Adobe.

<table id="table_7E3513EABA4948DC92EADCCE0234A9FF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzionalità/Miglioramento </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Attività A/B e di targeting esperienza (XT) </p> </td> 
   <td colname="col2"> <p>Modifica ed elimina le esperienze direttamente dal diagramma di attività. Ora puoi passare al Compositore esperienza visivo (VEC) per un'esperienza specifica o eliminare un'esperienza direttamente dal diagramma. </p> <p> <img src="assets/experience_edit.png" id="image_FA6E5F07B04A4B4BA02EA71EDB6908A7" /> </p> <p>Consulta: </p> <p> 
     <ul id="ul_CB0C1146716F4C09BF924CF3DFA7DC1A"> 
      <li id="li_3767DD36F597481FB312CC577CD668F0"> <p>Attività A/B: <a href="/help/main/c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00" format="dita" scope="local"> Aggiungi esperienza </a> </p> </li> 
      <li id="li_E2990CA178C6446BA7206643A3164FEF"> <p>Attività Targeting esperienza: <a href="/help/main/c-activities/t-experience-target/t-xt-create/xt-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00" format="dita" scope="local">Creare esperienze </a> </p> </li> 
     </ul> </p> <p>(TGT-30229) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tipi di pubblico </p> </td> 
   <td colname="col2"> <p>Confronta un attributo di profilo con un altro attributo di profilo anziché con un numero statico. </p> <p>Vedere <a href="/help/main/c-target/c-audiences/creating-a-profile-attribute-comparison-audience.md#concept_4C2124B79A5B4556A6C1D10C0F5E40A0" format="dita" scope="local"> Creazione di un pubblico di confronto di attributi di profilo </a>. </p> <p> (TGT-28406) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Codice personalizzato </p> </td> 
   <td colname="col2"> <p>Il “codice personalizzato” è ora disponibile nel pannello “Aggiungi modifiche” anziché nella scheda. Puoi anche aggiungere ulteriori codici personalizzati e assegnare facoltativamente un nome a ciascuno di essi. (TGT-28504) </p> <p>Consulta <a href="/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md#concept_B3A6E9EE3A60406DB640E205EA1745B5" format="dita" scope="local">Modifiche.</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Consigli </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_371C18DFC6D24E94B3D4FFFD83FC8D3A"> 
      <li id="li_9D11939014E7479AB7FD8910852A5386"> <p>Visualizza un elenco di attività che fanno riferimento a criteri selezionati sulla relativa scheda Criteri. La scheda elenca le attività attive e inattive. (TGT-27672) </p> </li> 
      <li id="li_B97BF9305EB04F6D8B1F6178B2E0CB34"> <p>Dal diagramma attività, le schede Criteri ora mostrano quando i risultati sono pronti per essere visualizzati. (TGT-27673) </p> <p>Consulta <a href="/help/main/c-recommendations/c-algorithms/algorithms.md" format="dita" scope="local">Criteri.</a> </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Modelli di esperienza </p> </td> 
   <td colname="col2"> <p>I modelli Adobe Target Experience sono esempi di offerte precodificate con ingressi configurabili utilizzabili in Target per eseguire alcuni casi comuni di utilizzo del percorso di classe. Questi modelli di esperienza sono disponibili gratuitamente per gli sviluppatori e i rivenditori come punto di partenza per eseguire alcuni casi comuni di utilizzo esterno in Adobe Target (tramite il Compositore esperienza visivo o il Compositore esperienza basato su modulo). La personalizzazione potrebbe essere necessaria per l'integrazione con l'architettura della pagina web o della piattaforma. </p> <p>Vedere <a href="/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/experience-templates.md#concept_109BBD7EABC04DD39E6B7B1687786652" format="dita" scope="local"> modelli di esperienza </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Serie di webinar sui fondamenti di Target </p> </td> 
   <td colname="col2"> <p>Partecipa alla nuova serie di webinar sui fondamenti di Target <a href="/help/main/cmp-resources-and-contact-information.md#concept_11902FAC95C64479AABE020557A7EEE4" format="dita" scope="local"> di </a>, una serie Customer Success offerta dalla community. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Miglioramenti, correzioni e modifiche**

Questa versione di [!DNL Target] include i seguenti miglioramenti, correzioni e modifiche:

* Per migliorare l&#39;utilizzo, sono state aumentate le dimensioni di Editor RTF. (TGT-24775)
* I diagrammi nel passaggio di Target (passaggio 2 del workflow guidato in tre fasi) per le attività di Automated Personalization (AP) e test multivariato (MVT) sono stati riprogettati secondo i progetti utilizzati per le attività A/B, Targeting esperienza (XT) e Consigli. (TGT-30712)
* Il valore della metrica per il rapporto di generazione del percorso di test multivariato (MVT) è ora più uniforme ai valori di altre metriche, che vengono arrotondati a due posizioni decimali. (TGT-30921)

### Version 1.5.0 di at.js (22 giugno 2018) {#section_53C622F4978F4BC9ACD932D4B7194C12}

<table id="table_B332A93D4A6E4568BA3F7FA8EC0787F4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzionalità/Miglioramento </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>at.js </p> </td> 
   <td colname="col2"> <p>È ora disponibile la versione 1.5.0 di at.js. </p> <p> <p>Nota: i codici tra parentesi sono per uso interno di Adobe. </p> </p> <p> 
     <ul id="ul_41FE0EED2D8B4ADE84FC4CA0FA0CE8A0"> 
      <li id="li_2DC17381CB7949AFA35B054B9CA723FA"> <p>I dettagli dell'evento <span class="codeph">a richiesta riuscita</span> contengono il flag di reindirizzamento. Questo flag può essere utilizzato per determinare se la pagina verrà reindirizzata a un URL diverso. Se desideri conoscere l'URL, abbonati a <span class="codeph">at-content-rendering-redirect</span>. (TNT-29834) </p> </li> 
      <li id="li_2852878862724BB2BD475C8FC7BF20DA"> <p>È stato risolto un problema che ha causato il mancato funzionamento di <span class="codeph">window.targetGlobalSettings.enabled</span> con un'eccezione di esecuzione se è stato impostato su falso. (TNT-29829) </p> </li> 
      <li id="li_96E5E409B36444F1B0E3E2606DC03996"> <p>È stato risolto un problema che ha causato un errore durante il caricamento nel Compositore esperienza visivo se si utilizza il codice personalizzato per una richiesta mbox globale di abilitazione e si nasconde il corpo. (TNT-29795) </p> </li> 
      <li id="li_818AA4EDDAC04D8B9BB4BA708D6BEF99"> <p>È stato aggiunto il supporto per <span class="codeph">screenOrientation</span>, <span class="codeph">devicePixelRatio</span> e <span class="codeph">webGLRenderer</span>. Questi nuovi parametri di richiesta di Target vengono utilizzati per iPhone X e altri sistemi di rilevamento dispositivi moderni. Per ulteriori informazioni, consulta <a href="/help/main/c-target/c-audiences/c-target-rules/mobile.md#concept_2A794199DC1A4D349FFFBC7DCF1FEB89" format="dita" scope="local">Mobile</a>. (TNT-29781) </p> </li> 
      <li id="li_87E3FB8B423C472AB1EE0DF2D7C64885"> <p>È stato risolto un problema per cui il suggerimento di posizione di Adobe Audience Manager (AAM) non veniva sempre inviato. (TNT-29695) </p> </li> 
      <li id="li_E9E5A5035AC24F54ADEF5447E3F15D3B"> <p>Per i browser che lo supportano, at.js 1.5.0 passa a MutationObserver per la votazione del selettore. Le versioni precedenti a at.js 1.0.0 utilizzavano un polyfill MutationObserver, che si è dimostrato problematico. Per evitare problemi di polyfill, la versione 1.5.0 utilizza il seguente pseudo codice per decidere quale meccanismo di programmazione utilizzare: </p> <p> 
        <code>
          if MutationObserver is supported scheduler = MutationObserver else if document is visible scheduler = requestAnimationFrame else scheduler = setTimeout 
        </code> </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 18.6.1 (20 giugno 2018) {#section_B63C660815B245DA9922BE33E03734A1}

Questa versione include i miglioramenti e le funzioni seguenti:

>[!NOTE]
>
>I codici tra parentesi sono per uso interno di Adobe.

<table id="table_5A60FFE5E86148F4BDC6A7031D03D6BA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzionalità/Miglioramento </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Compositore esperienza visivo </p> </td> 
   <td colname="col2"> <p>Quando fai clic su un azione nel Pannello delle modifiche, il Compositore esperienza visivo automaticamente scorre la pagina web ed evidenzia l'elemento corrispondente. Non è più necessario scorrere manualmente la pagina per trovare l'elemento HTML interessato dalla modifica. </p> <p> <img src="assets/modifications_panel.png" id="image_6E01280636E34ADDA9527AD18A34310B" /> </p> <p>(TGT-30441) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Browser supportati </p> </td> 
   <td colname="col2"> <p>È stato aggiunto Microsoft Edge come browser supportato per l'interfaccia utente di Target e per la distribuzione dei contenuti. </p> <p>Per ulteriori informazioni, vedi. <a href="https://experienceleague.adobe.com/docs/target-dev/developer/implementation/supported-browsers.html?lang=it" format="dita" scope="local">Browser supportati</a> (TGT-14102) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Consigli </p> </td> 
   <td colname="col2"> <p>Il criterio Articoli visualizzati di recente ora restituisce risultati specifici per un dato <a href="/help/main/administrating-target/hosts.md#concept_516BB01EBFBD4449AB03940D31AEB66E" format="dita" scope="local">ambiente </a>. Se due siti appartengono ad ambienti diversi e un visitatore passa da un sito all’altro, ciascun sito mostra solo gli articoli visualizzati di recente per il sito appropriato. Se due siti si trovano nello stesso ambiente e un visitatore passa tra di essi, il visitatore vedrà gli stessi elementi visualizzati di recente per entrambi i siti. </p></td> 
  </tr> 
 </tbody> 
</table>

**Miglioramenti, correzioni e modifiche**

Questa versione di [!DNL Target] include i seguenti miglioramenti, correzioni e modifiche:

* La riga Backup del file CSV scaricabile dei Consigli ora ha un &quot;&#42;&quot; iniziale (virgolette doppie che racchiudono un asterisco) invece di &#42; (un singolo asterisco).
* La riga dei Più venduti/Più visualizzati nel file CSV scaricabile dei Consigli non ha più una virgola davanti.

### Modifiche alla piattaforma di Target (19 giugno 2018) {#section_0638BD69F3C640479A2A258AD78C0884}

Questa versione include i seguenti miglioramenti:

>[!NOTE]
>
>I codici tra parentesi sono per uso interno di Adobe.

* La lista dei dispositivi è stata aggiornata per includere i più recenti modelli di cellulare. È stata aggiunta la capacità di distribuire contenuto con targeting a specifici modelli di iPhone usando il Device Marketing Name o Device Model.

  I clienti che usano SDK mobile non hanno necessità di utilizzare questa funzione. I clienti che utilizzano at.js devono fare l&#39;upgrade alla versione 1.5.0 di at.js.

  Per ulteriori informazioni, consulta [Mobile](/help/main/c-target/c-audiences/c-target-rules/mobile.md#concept_2A794199DC1A4D349FFFBC7DCF1FEB89). (TNT-26714, TNT-28288)

### API per il download di Target (5 giugno 2018) {#section_B8729DA10F18433C8D8E01B04F308ED2}

Puoi usare l&#39;API per il download dei consigli per scaricare i consigli in un file CSV che può essere visualizzato in un editor di fogli di calcolo o di testo. Per migliorare la sicurezza, a partire dal **5 giugno 2018**, Target bloccherà le richieste HTTP e autorizzerà solo quelle HTTPS.

### Target Standard/Premium 18.5.1 (22 maggio 2018) {#section_7C1427793C2A48DBAC39F8290717DC5B}

Questa versione include i miglioramenti e le funzioni seguenti:

>[!NOTE]
>
>I codici tra parentesi sono per uso interno di Adobe.

<table id="table_1C51F61184684072BC69AD15BA68BEBB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Rapporti </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_8D08FE4AC7D748EFB2BBFF87DBDC5CE5"> 
      <li id="li_B8929C19276D42168A28A3775CDEDFB3"> <p>Puoi salvare fino a dieci diversi predefiniti del rapporto di una singola attività dopo averla configurata come desiderato (metriche, pubblico, impostazioni avanzate e così via). Tutti gli utenti di Target possono visualizzare, modificare ed eliminare i vari predefiniti, a prescindere da chi li ha creati. (TGT-21268) </p> </li> 
      <li id="li_7ADA62F2ACA049C9B4A8986B09A9F4AA"> <p>Puoi configurare un rapporto di attività individuale come desideri e poi salvare tale configurazione come predefinita/impostazione preferita. Questa è la vista che compare quando vedi che il rapporto dell'attività sta avanzando. (TGT-10082) </p> </li> 
      <li id="li_DC63C04F3A884BDDA55B5515E4643B7B"> <p>Segnalazioni e messaggi all'interno dei rapporti ti premettono di sapere se uno o più tipi di pubblico, metriche, gruppi ospite o esperienze sono state cancellate dal rapporto precedentemente configurato. La segnalazione o il messaggio ti indica di scegliere un altro pubblico, metrica, gruppo ospite o esperienza da preimpostare nuovamente. (TGT-29424) </p> </li> 
     </ul> </p> <p>Per ulteriori informazioni, vedere la sezione Predefinito target in <a href="/help/main/c-reports/c-report-settings/report-settings.md#concept_3A80D5A394EC4B639DC715E06085BDB0" format="dita" scope="local"> Impostazioni report </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Script di profilo </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_F382C8E7708846A08676E1534BC92878"> 
      <li id="li_70E89504525C4119B588C230DCE772E8"> <p>Puoi visualizzare schede a comparsa di script di profilo simili come schede informative. Queste schede informative sullo script di profilo ti permettono di visualizzare l’elenco delle attività che si riferiscono allo script di profilo selezionato, insieme ad altri metadati utili. (TGT-28253) </p> <p>Per ulteriori informazioni, vedere la sezione Visualizzazione delle schede di informazioni sugli script di profilo in <a href="/help/main/c-target/c-visitor-profile/profile-parameters.md#concept_8C07AEAB0A144FECA8B4FEB091AED4D2" format="dita" scope="local"> Attributi degli script di profilo </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tipi di pubblico </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_DFEB778393024E3EBBC482F31A5B39BC"> 
      <li id="li_4049E334A38F4F94842FF1E35F177FE9"> <p>La creazione di tipi di pubblico personalizzati ora permette di usare il parametro mbox direttamente senza dover per forza specificare il nome mbox. Il nome dell’elemento mbox è ora facoltativo. Questa modifica consente di utilizzare parametri da più elementi mbox o di fare riferimento a un parametro che non è ancora stato registrato nella rete Edge. In alternativa, puoi applicare un filtro o sul parametro mbox con il nome mbox. </p> <p>Questo miglioramento è stato esteso anche ai criteri dei consigli, promozioni dei consigli e regole del test di esempio. </p> </li> 
     </ul> </p> <p>Per ulteriori informazioni, vedere <a href="/help/main/c-target/c-audiences/c-target-rules/custom-parameters.md#concept_C4C6E00D7C5A4BE9B72D471DB2E3027B" format="dita" scope="local"> Parametri personalizzati </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Consigli </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_7765B69E679D4C94B1E863E340DFDE15"> 
      <li id="li_F2AF7E1AFBD6461990EF1D83D1989582"> <p>Durante la selezione dei criteri di consigli nel compositore esperienza basato su moduli, è ora disponibile un collegamento diretto alla scheda dei criteri selezionati per poter modificare in modo semplice e veloce i criteri. (TGT-28483) </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local">Compositore esperienza basato su moduli</a>. </p> </li> 
      <li id="li_517F0A174587416B8621D6F710C1AC48"> <p>Ora per creare i criteri e le promozioni della funzione Consigli e le regole per il test dei modelli è possibile utilizzare il parametro mbox direttamente senza che sia necessario specificare il nome mbox. Il nome dell’elemento mbox è ora facoltativo. Questa modifica consente di utilizzare parametri da più elementi mbox o di fare riferimento a un parametro che non è ancora stato registrato nella rete Edge. In alternativa, puoi applicare un filtro o sul parametro mbox con il nome mbox. </p> <p>Questo miglioramento è stato esteso anche alla creazione di tipi di pubblico personalizzati. </p> <p>Per ulteriori informazioni, vedere <a href="/help/main/c-recommendations/c-recommendations-faq/recommendations-faq.md#concept_EF272DE4AC6C47B19026BFBE816F5DB8" format="dita" scope="local"> Domande frequenti sui consigli </a>. </p> </li> 
      <li id="li_AAB242830D1E47B78E58A980B717C736"> <p>L'interfaccia utente delle schede di progettazione dei consigli è stata aggiornata. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Miglioramenti, correzioni e modifiche**

Questa versione di [!DNL Target] include i seguenti miglioramenti, correzioni e modifiche:

* È stata aggiornata l’interfaccia utente per il passaggio 2 del flusso di lavoro guidato in tre fasi, per creare o modificare un test A/B oppure un’attività Targeting esperienza (XT) o Consigli. (TGT-18911)

### Target Standard/Premium 18.4.1 (25 aprile 2018) {#section_445DBC5402BA456BAF2D24AEA33A91C9}

Questa versione include i miglioramenti e le funzioni seguenti:

>[!NOTE]
>
>I codici tra parentesi sono per uso interno di Adobe.

<table id="table_6D99C48B72D24728BF623608053931D3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Frammenti di esperienza di Adobe Experience Manager (AEM) </p> </td> 
   <td colname="col2"> <p>I frammenti di esperienza creati in AEM possono essere utilizzati nelle attività di Target per combinare la facilità d'uso e la potenza di AEM con le potenti capacità di intelligenza automatizzata (AI) ed apprendimento automatico (ML) di Target per testare e personalizzare le esperienze su grande scala.  </p> <p>AEM riunisce tutti i contenuti e le risorse in una posizione centrale per alimentare la tua strategia di personalizzazione. AEM consente di creare facilmente contenuti per desktop, tablet e dispositivi mobili in un'unica posizione senza scrivere codice. Non è necessario creare pagine per ogni dispositivo: AEM regola automaticamente ogni esperienza utilizzando i contenuti. </p> <p> Target consente di fornire esperienze personalizzate in scala su una combinazione di approcci di apprendimento automatico basati sulle regole e guidati da intelligenze automatizzate che incorporano variabili comportamentali, contestuali e offline.Con Target puoi facilmente impostare ed eseguire attività di test A/B e multivariati per determinare le offerte, i contenuti e le esperienze migliori. </p> <p>La funzione Frammenti esperienza rappresenta un enorme passo avanti per la collaborazione tra i creatori e i manager di contenuti ed esperienze, e i professionisti di personalizzazione e ottimizzazione che usano Target per conseguire risultati di business. </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-experiences/c-manage-content/aem-experience-fragments.md#topic_1E1E4EA01F074349B2CF8785387B5FE8" format="dita" scope="local">Frammenti esperienza AEM</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rapporti </p> </td> 
   <td colname="col2"> 
    <ul id="ul_EAB90C510EA04D6A8AEFF23A77DB2337"> 
     <li id="li_47DA6EB92CC84FFDBFDC9CC9386AF654"> <p>Puoi ora ricaricare un rapporto per aggiornarne la visualizzazione di tabelle e grafici senza ricaricare l’intera pagina, la configurazione o l’intervallo di date. (TGT-28125) </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-reports/c-report-settings/report-settings.md#concept_3A80D5A394EC4B639DC715E06085BDB0" format="dita" scope="local">Impostazioni dei rapporti</a>. </p> </li> 
     <li id="li_AB2DE7A45D914FD7AEB0832187AF3844"> <p>Il calendario nei rapporti contiene ora degli intervalli di date predefiniti, come ad esempio Ultimi 7 giorni, Ultimi 15 giorni e così via. (TGT-29171) </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-reports/c-report-settings/report-settings.md#concept_3A80D5A394EC4B639DC715E06085BDB0" format="dita" scope="local">Impostazioni dei rapporti</a>. </p> </li> 
     <li id="li_46DF9037E0ED4935B3BCDB35E8BED065"> <p>La larghezza della colonna della vista tabella è stata modificata per ridurre lo scorrimento orizzontale quando vengono applicate più metriche. (TGT-26575) </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Localizzazione dell’interfaccia utente </p> </td> 
   <td colname="col2"> <p>L’interfaccia utente di Target è ora disponibile nelle seguenti lingue: </p> <p> 
     <ul id="ul_DB6C771FCFDF43F498F8754920A70BCD"> 
      <li id="li_A65D07DF66844AC8BEEC1D413F214191"> <p>Cinese semplificato </p> </li> 
      <li id="li_5986DD06AF5B4F76B3A02CFBF2DC3644"> <p>Cinese tradizionale </p> </li> 
      <li id="li_341FDC1CEC2B4C4BBD45CB2A0A54F2A3"> <p>Coreano </p> </li> 
      <li id="li_A4C31539B98E42348D5F1A18C63EAB6C"> <p>Italiano </p> </li> 
      <li id="li_97E3E0A916B64601BBF601AAED581174"> <p>Portoghese </p> </li> 
     </ul> </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tipi di pubblico </p> </td> 
   <td colname="col2"> <p>Durante la creazione di un pubblico personalizzato basato su un parametro mbox, <span class="codeph">mboxParameter</span> non richiede più di specificare <span class="codeph">mboxName </span>. Il nome dell’elemento mbox è ora facoltativo. Questa modifica consente di utilizzare parametri da più elementi mbox o di fare riferimento a un parametro che non è ancora stato registrato nella rete Edge. (TGT-25807) </p> <p> <p>Nota: questa funzionalità è visibile nell’interfaccia utente di Target ma è attualmente disabilitata. Questa funzionalità verrà presto abilitata (data da comunicarsi). </p> </p> 
  </td> 
  </tr> 
 </tbody> 
</table>

**Miglioramenti, correzioni e modifiche**

Questa versione di [!DNL Target] include i seguenti miglioramenti, correzioni e modifiche:

* Transport Layer Security (TLS) è tra i protocolli di sicurezza distribuiti più ampiamente ed è oggi utilizzato per i browser web e per altre applicazioni dove i dati devono essere scambiati in modo sicuro all’interno di una rete. Adobe possiede degli standard di sicurezza e conformità che richiedono la chiusura dei protocolli più vecchi e l’utilizzo di TLS 1.2 per poter avere la versione in uso più aggiornata e più sicura. A partire dalla versione 18.4.1 di Target (25 aprile 2018), Adobe Target farà dei passi avanti per avvicinarsi alla crittografia TLS 1.2 ed eliminare completamente il supporto per la crittografia TLS 1.0 entro il 12 settembre 2018. È importante che esamini a fondo le specifiche e pianifichi le modifiche per una transizione senza problemi. Per ulteriori informazioni, consulta [Modifiche alla crittografia TLS](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/tls-transport-layer-security-encryption.html?lang=it){target=_blank}.
* È stata migliorata l’interfaccia utente delle schede Criteri dei consigli, per migliorarne la fruibilità. (TGT-27829)

### at.js (3 aprile 2018) {#section_932DF1004F4648668FE4984BFAF2EC49}

Questa versione include i miglioramenti e le funzioni seguenti:

<table id="table_76576D9D931B4DA99900F2C03175938E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>at.js </p> </td> 
   <td colname="col2"> <p>È ora disponibile la versione 1.3.0 di at.js. Per ulteriori informazioni, consulta <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/deploy-at-js/implement-target-without-a-tag-manager.html?lang=it" format="dita" scope="local">Scarica at.js</a> e <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it" format="dita" scope="local">Dettagli della versione di at.js</a>. </p> <p> 
     <ul id="ul_349BEB37B6C94FF0801F121042037803"> 
      <li id="li_4C2F82F4DD394ED5A0BFF978B15FEDDF"> <p>I seguenti nuovi eventi sono disponibili per facilitare il tracciamento, il debug e la personalizzazione dell’interazione con at.js: </p> <p> 
        <ul id="ul_EFF7E2FCEA0D42298779DDE13B54503F"> 
         <li id="li_6A2B06A522004EDE96D9A552571A7C30"> <p>LIBRARY_LOADED </p> </li> 
         <li id="li_61AA203A21DF4B7EAE075374A09C8FF0"> <p>REQUEST_START </p> </li> 
         <li id="li_DAF9CC1E86834C62B93419429B43A2CB"> <p>CONTENT_RENDERING_START </p> </li> 
         <li id="li_A52DC337115248A1BE5AF5B358BE5A9A"> <p>CONTENT_RENDERING_NO_OFFERS </p> </li> 
         <li id="li_7D71E48016B1446995493EBBF7D32447"> <p>CONTENT_RENDERING_REDIRECT </p> </li> 
        </ul> </p> <p>Per ulteriori informazioni, consulta <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/atjs-functions.html?lang=it" format="dita" scope="local"> eventi personalizzati at.js </a>. </p> </li> 
      <li id="li_E2704294F8BA47FFAABE7572F67FB5C0"> <p>È possibile integrare una richiesta at.js con parametri aggiuntivi provenienti da provider di dati. Aggiungi i provider di dati a <span class="codeph">window.targetGlobalSettings</span> nella <span class="codeph">chiave dataProviders </span>. </p> <p>Per ulteriori informazioni, consulta “Fornitori dati” in <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/atjs-functions.html?lang=it" format="dita" scope="local">targetGlobalSettings()</a>. </p> </li> 
      <li id="li_02EAFE6DA0D44CF88980184FD14226A5"> <p>Le richieste at.js ora utilizzano GET, ma passeranno a POST quando la dimensione dell’URL supererà i 2048 caratteri. La nuova proprietà <span class="codeph">urlSizeLimit</span> consente di aumentare questo limite, se necessario. Questa modifica consente di allineare Target at.js ad AppMeasurement, che utilizza la stessa tecnica. </p> </li> 
      <li id="li_43363A4F3A764394AA88D2595F93D8C0"> <p>Target ora impone che venga utilizzata la chiave <span class="codeph">mbox</span> nella funzione <span class="codeph">adobe.target.applyOffer(options)</span>. Questa chiave era già richiesta in passato, ma Target ora ne impone l’utilizzo per garantire la corretta convalida di Target e il corretto utilizzo di questa funzione da parte dei clienti. </p> <p>Per ulteriori informazioni, consulta <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/atjs-functions.html?lang=it" format="dita" scope="local">adobe.target.applyOffer(options)</a>. </p> </li> 
      <li id="li_7336D8D48A894291A378E0BB212B7F9B"> <p>at.js offre una funzionalità migliorata per il tracciamento di eventi e clic. at.js utilizza <span class="codeph">navigator.sendBeacon()</span> per inviare i dati di tracciamento degli eventi; se <span class="codeph">navigator.sendBeacon()</span> non è supportato, si basa su richieste XHR sincrone. Questa alternativa riguarda principalmente Internet Explorer 10 e 11 e alcune versioni di Safari. Con iOS 11.3, in Safari verrà aggiunto il supporto di <span class="codeph">navigator.sendBeacon()</span>. </p> </li> 
      <li id="li_28D7324137B14C75BF6F1EA0B2487C9B"> <p>at.js ora può renderizzare le offerte anche quando una pagina viene aperta nelle schede in background. Alcuni utenti di Target hanno riscontrato problemi quando <span class="codeph">requestAnimationFrame()</span> è stato disattivato a causa del comportamento di limitazione del browser per le schede in background. </p> </li> 
      <li id="li_3278979E1C6C41DEA7E8025AEB337985"> <p>In questa versione sono stati aggiunti svariati miglioramenti a livello di prestazioni, tra cui call stack più brevi durante l’ispezione di un profilo CPU in Chrome. </p> </li> 
      <li id="li_AAA9C0DCC3354DFA8907968C8E6427F6"> <p>at.js 1.3.0 non supporta più la consegna di contenuti in Microsoft Internet Explorer 9. Per un elenco dei browser supportati, vedere <a href="https://experienceleague.adobe.com/docs/target-dev/developer/implementation/supported-browsers.html?lang=it" format="dita" scope="local"> browser supportati </a>. Da adesso in poi, tutte le richieste vengono eseguite tramite <span class="codeph">XMLHttpRequest</span> con supporto CORS, senza richieste JSONP. Questa modifica migliora notevolmente la sicurezza. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 18.3.1 (20 marzo 2018) {#section_880706BE15544A03A2C951F267F4AEC5}

Questa versione include i miglioramenti e le funzioni seguenti:

>[!NOTE]
>
>I codici tra parentesi sono per uso interno di Adobe.

<table id="table_AE38682151A948AEA21E35A353F18D76"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" class="premium"> <p>Attributo di popolarità “Entità” </p> </td> 
   <td colname="col2"> <p><b>Novità: 22 marzo 2018</b> </p> <p>Ora puoi impostare la popolarità in base all’attributo Entità nel flusso esistente quando un attributo personalizzato è selezionato come chiave. </p> <p>Dopo aver selezionato la chiave desiderata (in questo caso, un attributo di profilo personalizzato), per “Logica consigli”, puoi scegliere due nuove opzioni: </p> <p> 
     <ul id="ul_7A6F2398ADE846EF8A7A3110C2736BF7"> 
      <li id="li_66BFF016564749B298B88F6B9638B64E"> <p>Articoli più visualizzati </p> </li> 
      <li id="li_937FE5C40ED8471391B282D1ACE8C133"> <p>Articoli più venduti </p> </li> 
     </ul> </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tipi di pubblico </p> </td> 
   <td colname="col2"> <p>Quando visualizzi la scheda a comparsa delle definizioni dei tipi di pubblico (ad esempio, dalla Libreria tipi di pubblico), puoi vedere altre attività che fanno riferimento a quel pubblico, se applicabile. In questo modo puoi evitare di intervenire accidentalmente sulle attività mentre modifichi i tipi di pubblico. </p> <p>In precedenza, quando tentavi di eliminare un pubblico a cui facevano riferimento alcune attività, un messaggio di avvertenza ti informava che non era possibile eliminare un pubblico a cui fanno riferimento un massimo di 10 attività. </p> <p>Per ulteriori informazioni, vedere <a href="/help/main/c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271" format="dita" scope="local"> Informazioni sui tipi di pubblico </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rapporti </p> </td> 
   <td colname="col2"> <p>Le informazioni su incremento e limiti nei rapporti sono più complete e utili, con una descrizione che specifica come avviene il calcolo dei limiti. (TGT-28729) </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-reports/statistical-methodology/statistical-calculations.md" format="dita" scope="local">Incremento medio, limiti di incremento e intervallo di confidenza</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Attività di Automated Personalization (AP) e Targeting automatico </p> </td> 
   <td colname="col2"> <p>Puoi trovare ulteriori indicazioni nell’interfaccia utente e nell’Aiuto per allocare in modo più efficace le percentuali di traffico nelle attività di Automated Personalization (AP) e Targeting automatico. </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-activities/auto-target/auto-target-to-optimize.md" format="dita" scope="local">Determinazione dell’allocazione del traffico</a> e <a href="/help/main/c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local">Creazione di un’attività di Automated Personalization</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Consigli: regole di inclusione, raccolte ed esclusioni per Criteri personalizzati </p> </td> 
   <td colname="col2"> <p>Adesso puoi aggiungere filtri in tempo reale all’output dei criteri personalizzati. Ad esempio, puoi limitare gli articoli consigliati a quelli della categoria o del marchio preferito dal visitatore. Così puoi combinare calcoli offline e filtri in tempo reale. </p> <p>Con l’aggiunta delle regole di inclusione ai Criteri personalizzati, i consigli non sono più statici ma diventano dinamici, in base agli interessi del visitatore. </p> <p> 
     <ul id="ul_BDD55AB34F4A43C691D2399C16AA3D6C"> 
      <li id="li_133C33E0D02E4861A4C855BD8A492E69"> <p>Adesso puoi configurare i Criteri personalizzati, come altri criteri nei consigli. </p> </li> 
      <li id="li_AC201F0917BF465C985E8947635F762E"> <p>Puoi utilizzare raccolte, esclusioni e inclusioni (incluse le regole speciali per Prezzo e Inventario) proprio come per tutti gli altri criteri. Le raccolte e le esclusioni erano già supportate. Con questa versione sono state aggiunte le inclusioni. </p> </li> 
     </ul> </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-recommendations/c-algorithms/algorithms.md" format="dita" scope="local">Criteri</a>. </p> <p>(TGT-28488) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Consigli: regole di inclusione, raccolte ed esclusioni per i criteri “Visualizzati di recente” </p> </td> 
   <td colname="col2"> <p>Puoi filtrare gli articoli visualizzati di recente in modo che vengano visualizzati solo gli articoli con uno specifico attributo. Ad esempio, nel caso di una multinazionale con più linee di business, un visitatore potrebbe visualizzare gli articoli in più siti della stessa società. In questo caso, puoi limitare gli articoli visualizzati di recente al solo sito su cui sono stati visualizzati. In tal modo gli articoli visualizzati di recente non saranno visualizzati sugli altri siti della stessa società. </p> <p> 
     <ul id="ul_A2D260F01CA047EEA72EF56BD0EE88FA"> 
      <li id="li_DB107DD357B741CCB2B7A4FDAD16F9D6"> <p>Adesso puoi configurare i criteri per la funzione Visualizzato di recente, come gli altri criteri nei consigli. </p> </li> 
      <li id="li_85452C03F0924D4C8D854509F1293021"> <p>Puoi utilizzare raccolte, esclusioni e inclusioni (incluse le regole speciali per Prezzo e Inventario) proprio come per tutti gli altri criteri. Le raccolte e le esclusioni erano già supportate. Con questa versione sono state aggiunte le inclusioni. </p> </li> 
     </ul> </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-recommendations/c-algorithms/algorithms.md" format="dita" scope="local">Criteri</a>. </p> <p>(TGT-22843) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Estensione Target per Adobe Launch </p> </td> 
   <td colname="col2"> <p>Launch è la soluzione Adobe di nuova generazione per la gestione dei tag. Launch offre ai clienti un modo semplice di implementare e gestire tutti i tag di analisi, marketing e annunci pubblicitari necessari per fornire ai clienti esperienze personalizzate. </p> <p>Grazie all’estensione di Target puoi implementare rapidamente e facilmente Target nel tuo ambiente. </p> <p>Per ulteriori informazioni, vedere <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/deploy-at-js/implement-target-using-adobe-launch.html?lang=it" format="dita" scope="local"> Implementazione di Target con Adobe Launch </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Miglioramenti, correzioni e modifiche**

Questa versione di [!DNL Target] include i seguenti miglioramenti, correzioni e modifiche:

* Quando crei o modifichi attività A/B e Targeting esperienze (XT), Target conserva le informazioni sull’ultima esperienza, pagina o versione di esperienza aperta (tramite la funzionalità per più tipi di pubblico) e, alla successiva apertura dell’interfaccia utente di Target, seleziona la pagina appropriata. (TGT-28225)
* Sono state apportate delle correzioni di sicurezza per motivi di conformità.

### Target Standard/Premium 18.2.1 (15 febbraio 2018) {#section_837CBBB7A89D45D99855A8C5F5E7BFFB}

Questa versione include i miglioramenti e le funzioni seguenti:

<table id="table_1C7A462AE8D4492FA5555F060031F665"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Adobe Marketing Cloud è stato rinominato e si chiama ora Adobe Experience Cloud. </p> </td> 
   <td colname="col2"> <p>Experience Cloud è un insieme integrato di soluzioni e servizi di marketing digitali realizzati da Adobe. È anche un'interfaccia intuitiva che ti consente di accedere rapidamente a soluzioni e servizi di base cloud. </p> <p>Il cambio di nome e le modifiche all'interfaccia utente: Adobe Marketing Cloud è stato rinominato e ora si chiama Adobe Experience Cloud. In aggiunta, noterai delle modifiche dell’interfaccia utente di Target e nel modulo per cambiare soluzione. </p></td> 
  </tr> 
 </tbody> 
</table>

**Miglioramenti, correzioni e modifiche**

Questa versione di [!DNL Target] include alcuni miglioramenti, correzioni e modifiche di back-end.

### Piattaforma di Target (18 gennaio 2018) {#section_F6A0DC31636D403F92BDB9DCE7A3F6ED}

Questa versione include i miglioramenti e le funzioni seguenti:

<table id="table_0F5BF9370E214302BDFE0AC2D66EC773"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>at.js </p> </td> 
   <td colname="col2"> <p>In at.js 1.2.3 è stato aggiunto il supporto per le offerte JSON. Le offerte JSON sono supportate solo nelle attività create utilizzando il Compositore esperienza basato su moduli. Attualmente le offerte JSON possono essere utilizzate solo tramite chiamate API dirette. Consulta <a href="/help/main/c-experiences/c-manage-content/create-json-offer.md#concept_63C7BEE1F0DB4A7596D997219B7C136D" format="dita" scope="local">Creare un’offerta JSON</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Altre modifiche </p> </td> 
   <td colname="col2"> <p>Adesso le regole di esclusione, i cataloghi, le regole di inclusione degli algoritmi e i filtri in fase di esecuzione non sono sensibili alla distinzione maiuscole/minuscole. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 18.1.1 (23 gennaio 2018) {#section_3A2216543B064D6F82EC03E1F8AEC74D}

Questa versione include i miglioramenti e le funzioni seguenti:

>[!NOTE]
>
>I codici tra parentesi sono per uso interno di Adobe.

<table id="table_872FE2BE61CC4A5CA369D9A6C730686E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Tipi di pubblico </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_42D7C86043C94A7BBA5ED405B2902E3A"> 
      <li id="li_50F2A7D05AB244E18D263A476BD906B3"> <p>Ora puoi creare un pubblico con Arco temporale senza date di inizio o di fine. In questo modo puoi utilizzare lo stesso pubblico in più attività (senza creare una copia del pubblico) controllando le date di inizio e di fine a livello di attività. Vedere <a href="/help/main/c-target/c-audiences/c-target-rules/time-frame.md#concept_0FE1E8DACD104F8B870B0BADE3197F0A" format="dita" scope="local"> Intervallo di tempo </a>. (TGT-25975) </p> </li> 
      <li id="li_6F08D63BC4F040859D51C47C3521C5E1"> <p>La funzionalità Copia e modifica è disponibile per il pubblico solo attività: fai clic su Seleziona pubblico &gt; Solo attività, e passa il puntatore su un pubblico. In precedenza, questa funzionalità esisteva solo per il pubblico di Librerie. Vedere <a href="/help/main/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483" format="dita" scope="local"> Creazione di un pubblico per sola attività </a>. (TGT-27410) </p> </li> 
      <li id="li_A8CF45E6DC37401AA273F7D6CF617524"> <p>Il pubblico solo attività può avere lo stesso nome in attività diverse. In precedenza, i nomi duplicati generavano l’aggiunta di marche temporali; un pubblico duplicato denominato "Target nel giorno feriale" veniva salvato come "Target nel giorno feriale-1456732099201". </p> <p>I tipi di pubblico della Libreria continua a richiedere nomi univoci. (TGT-17967) </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rapporti </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_C595EEF916494342AD99FF0FDF999927"> 
      <li id="li_8C74478D3480406591DC876F69C19329"> <p>Ora puoi visualizzare gli intervalli di affidabilità per le variabili continue. (TGT-22085) </p> </li> 
      <li id="li_21B31F91685C46CAA47688FDE5735312"> <p>Target ora visualizza i limiti di incremento quando statisticamente significativi nei rapporti.(TGT-27301, TGT-27794 e TGT-26387) </p> </li> 
     </ul> </p> <p>Consulta <a href="/help/main/c-reports/c-report-settings/report-settings.md#concept_4BB6A7FDAB6F4806A632F9CD989B8BFA" format="dita" scope="local">Impostazioni rapporti.</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Offerte </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_BD0C5B260E7E4F139FBC1FBA286C0B81"> 
      <li id="li_FCDBABE6C5034A3596F5BBF024245FB9"> <p>Target supporta ora la creazione di offerte JSON nella libreria offerte per l’utilizzo in Compositore di esperienza basata su modulo. Consulta <a href="/help/main/c-experiences/c-manage-content/create-json-offer.md#concept_63C7BEE1F0DB4A7596D997219B7C136D" format="dita" scope="local">Creare un’offerta JSON</a>. (TGT-27064) </p> </li> 
      <li id="li_5500AE7DCF4146E88E4619382CE8E836"> <p>Ora puoi visualizzare le attività che fanno riferimento a un'offerta di codice nella scheda pop-up della definizione di ogni offerta. Questa funzionalità non è applicabile alle offerte di immagine. Vedi <a href="/help/main/c-experiences/c-manage-content/manage-content.md#concept_17874A6FCBB743AA84C5988E8571CCF3" format="dita" scope="local"> Offerte </a>. (TGT-26277) </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Consigli </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_63613AD2D744442AA12CD23F4DAC75B4"> 
      <li id="li_4DD5CF06D93A4083BCB34A4FFA293C89"> <p>L’interfaccia utente visualizza lo stato di caricamento dei dati dell'algoritmo personalizzato per i consigli. Consulta <a href="/help/main/c-recommendations/c-algorithms/recommendations-csv.md#task_1BBA49883E794670A09F0ABE1B3F4288" format="dita" scope="local">Caricamento di criteri personalizzati </a>. (TGT-23891) </p> </li> 
      <li id="li_14FCFDD0A0E84B47AF1488DB4DDF197B">Gli operatori Valore presente e Valore mancante sono disponibili durante la creazione di regole di inclusione dell'algoritmo. Vedere <a href="/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F" format="dita" scope="local"> Utilizzare regole di inclusione dinamiche e statiche </a>. (TGT-24110) </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Newsletter di Adobe Target Insider </p> </td> 
   <td colname="col2"> <p>Adobe Target Insider è una newsletter mensile per i membri della community di Adobe Target. Scopri aggiornamenti del prodotto e progetti futuri, suggerimenti e trucchi per la personalizzazione e l’ottimizzazione, storie di successo dai nostri clienti, i prossimi eventi, white paper ricchi di informazioni, articoli di blog e altro ancora. Per saperne di più, leggi la <a href="https://theblog.adobe.com/stay-optimized-adobe-target-insider-newsletter/" format="https" scope="external">lettera di annuncio</a>. </p> <p> <a href="https://www.adobe.com/subscription/adobe_target_newsletter.html" format="html" scope="external"> Iscriviti alla newsletter</a>: ti aiuterà a fornire ai clienti le esperienze eccezionali che sono alla base del successo aziendale. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Miglioramenti, correzioni e modifiche**

Questa versione di [!DNL Target] include i miglioramenti, le correzioni e le modifiche seguenti per i clienti:

* Ora puoi scorrere la pagina durante la riorganizzazione delle esperienze al Passaggio 2 del flusso di lavoro guidato in tre passaggi durante la creazione di attività. (TGT-27652)
* Puoi fare clic con il pulsante destro del mouse su un&#39;attività dall&#39;Elenco attività per aprirla in una nuova scheda. Ad esempio, in Firefox, fai clic con il pulsante destro del mouse sull&#39;attività desiderata e poi scegli Apri il link in una nuova scheda. (TGT-27409)
* Miglioramenti delle prestazioni apportate alla Pagina progettazione (Consigli > progettazioni). La velocità per visualizzare e cercare le progettazioni è stata migliorata. (TGT-21792)
* Adesso at.js è l&#39;opzione di implementazione predefinita per il download. (TGT-24676)
* La convalida degli URL consente l&#39;utilizzo di doppi trattini. In precedenza, un URL con trattini doppi non poteva essere caricato nel Compositore esperienza visivo. (TGT-28176)
* Correzioni multiple di localizzazione dell&#39;interfaccia utente per i linguaggi supportati.

## Versione 2017 {#reference_59C7622A111C4147804A8AAC6D27BB8D}

### Piattaforma Target (8 novembre 2017) {#section_536B3C0F32ED441C8D82704B94F6AF7E}

Questa versione include i miglioramenti e le funzioni seguenti:

<table id="table_793CDDF1BD9E48BDBABBF6CD979BE186"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>at.js </p> </td> 
   <td colname="col2"> <p>È ora disponibile la versione 1.2.2 di at.js. Per ulteriori informazioni, consulta <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/deploy-at-js/implement-target-without-a-tag-manager.html?lang=it" format="dita" scope="local">Scarica at.js</a>. </p> <p> 
     <ul id="ul_3C4C9385A0F3489AA2137A2C88AE93CF"> 
      <li id="li_E658799D930547E6901ACFBF7C541F1F"> <p>È stato risolto un problema a causa del quale veniva restituito un errore di JavaScript se la libreria di Target era caricata in una pagina che utilizzava la modalità non standard. (TNT-28312) </p> </li> 
      <li id="li_050620115ED84CBDA736D94E9AAC6550"> <p>È stato risolto un problema a causa del quale il tracciamento dei clic di Target impediva il corretto funzionamento delle chiamate di raccolta dati di Analytics. (TNT-28261) </p> </li> 
      <li id="li_97BC1B7295364ACDAD3FB07005ED592F"> <p>È stato corretto un problema che impediva il corretto funzionamento di <span class="codeph">getOffer() params</span> se <span class="codeph">targetPageParams()</span> restituiva una stringa vuota. (TNT-28359) </p> </li> 
      <li id="li_B542D4A4E37141BA8BE79D416E1B58DB"> <p>È stato risolto un problema nella generazione dell’ID di sessione quando si utilizza solo x. (TNT-28361) </p> </li> 
     </ul> </p> <p>Il timeout predefinito per at.js è stato modificato da 15 secondi a 5 secondi. </p> <p>Se al momento il timeout è impostato a 15 secondi, verrà aggiornato al nuovo valore predefinito di 5 secondi. Se in precedenza era stato impostato un valore diverso, invece, la modifica non verrà applicata. </p> </td> 
  </tr>  
 </tbody> 
</table>

### Target Standard/Premium 17.11.1 (8 novembre 2017) {#section_324A9B1DA0B14F5999FEE41F15B13A44}

Questa versione include i miglioramenti e le funzioni seguenti (i codici tra parentesi sono per uso interno di Adobe):

<table id="table_6ADDF3552AD04666B76F2D3F457BB042"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Offerte </p> </td> 
   <td colname="col2"> <p> Un utente che dispone dell'autorizzazione “Editor” non può modificare un'offerta riferita a un'attività in tempo reale o pianificata. </p> <p> <p>Nota: se un cliente Target Premium utilizza le <a href="https://experienceleague.adobe.com/docs/target/using/administer/manage-users/enterprise/property-channel.html?lang=it" format="html" scope="external">autorizzazioni utente Enterprise</a> e seleziona l’opzione Tutte le aree di lavoro, Target applica l’autorizzazione più elevata dell’utente in tutte le aree di lavoro. Se l'autorizzazione più elevata è “Editor”, Target limita la modifica come indicato sopra. </p>  </p> <p>Queste restrizioni si applicano a tutte le offerte, non solo a quelle create in Target. (TGT-27276) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Token di risposta </p> </td> 
   <td colname="col2"> <p>Aggiunti i seguenti parametri incorporati: </p> <p> 
     <ul id="ul_17AD5B9788514E9DB14ED435A4224BFE"> 
      <li id="li_334F10A5B7934215B4D37278901BAF96"> <p>profile.tntId </p> </li> 
      <li id="li_AA9B4611035344549CC933FFC499289F"> <p>profile.marketingCloudVisitorId </p> </li> 
      <li id="li_DD751027371D4293BF9DB872278BD1B3"> <p>profile.thirdPartyId </p> </li> 
      <li id="li_B6D983A1B68D49AAA40CB401437676F1"> <p>profile.categoryAffinity </p> </li> 
      <li id="li_F5E86BFD14CA4C198F36F3F9987750F9"> <p>profile.categoryAffinities </p> </li> 
     </ul> </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/administrating-target/response-tokens.md#concept_2B21B222F6A344D68CA5929817E836C4" format="dita" scope="local">Token di risposta</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 17.10.1 (25 ottobre 2017) {#section_EF74751744024C209A02F45322642D37}

Questa versione include i miglioramenti e le funzioni seguenti (i codici tra parentesi sono per uso interno di Adobe):

<table id="table_307DF0CD143048BC9E419444C556B8FB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Tipi di pubblico </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_6E91AEC68A6E45D8B2907C77E752FEC6"> 
      <li id="li_A5778B528358433DB31D700D8F9BCB79"> <p>Durante la creazione di un'attività, è possibile creare un pubblico solo attività all'interno del flusso di lavoro guidato in tre passaggi. Questo tipo di pubblico può essere utilizzato in altre posizioni all'interno della stessa attività, ma non viene memorizzato nella Libreria di pubblico per essere usato in altre attività. (TGT-25474) </p> <p> <img src="assets/adhoc_audience.png" id="image_32C7C8B72F51425595A2E266AEFA17E9" /> </p> <p>Per ulteriori informazioni, vedere <a href="/help/main/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483" format="dita" scope="local"> Creazione di un pubblico per sola attività </a>. </p> </li> 
      <li id="li_691812682A5B42C0941324F2BC7D5740"> <p>Per tutte le attività, puoi scegliere una metrica di successo che qualifica l’utente per un determinato tipo di pubblico. In passato, Target identificava gli utenti come idonei per un determinato tipo di pubblico al momento dell’accesso a un’attività. Ora invece puoi scegliere quando valutare il pubblico scegliendo una metrica di successo. (TGT-15805) </p> <p> <img src="assets/success_metric.png" id="image_0CEC6015A2C4429790A063FE54CC1A35" /> </p> </li> 
     </ul> </p> <p>Per ulteriori informazioni, vedere <a href="/help/main/c-target/apply-reporting-audience-success-metric.md#concept_5F11149ACCA84FE79C7B9F766B6B0595" format="dita" scope="local"> Applicare un pubblico di reportistica a una metrica di successo </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Targeting automatico </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_6F89BD36373E47C4B3A6F8584D431D82"> 
      <li id="li_5F7B590AF8F24066ADD270E9F75CB12F"> <p>Le attività di Targeting automatico supportano ora la generazione rapporti a livello di segmento. (TGT-22777) </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-activities/auto-target/auto-target-to-optimize.md" format="dita" scope="local">Targeting automatico per esperienze personalizzate</a>. </p> </li> 
      <li id="li_35042E7D6BB04265B42F08A23A774E92"> <p>Puoi modificare la percentuale di Controllo per le attività Targeting automatico. (TGT-26467) </p> <p> <img src="assets/auto-target-control-small.png" id="image_81F6F61DB61240C289FB71362851AA53" /> </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-activities/auto-target/auto-target-to-optimize.md" format="dita" scope="local">Targeting automatico per esperienze personalizzate</a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Offerte </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_667DDEDDC5284C8393F8BCA5CD9EF12A"> 
      <li id="li_E00DB93297EC4100B46E42D867757DAA"> <p>Ora puoi visualizzare i dettagli di definizione di un'offerta, senza doverla aprire, tramite una scheda popup direttamente dalla Libreria offerte. (TGT-26377) </p> <p> <img src="assets/offer-card.png" id="image_1980AE8E9BED424085CC482C773C20EC" /> </p> <p>Per ulteriori informazioni, vedere <a href="/help/main/c-experiences/c-manage-content/manage-content.md#concept_17874A6FCBB743AA84C5988E8571CCF3" format="dita" scope="local"> offerte </a>. </p> </li> 
      <li id="li_F71AC4FDAC0E4BEE81D39490E82686C0"> <p>Puoi copiare e modificare offerte e cartelle nel Selettore di offerta durante la creazione di un'attività. (TGT-26936) </p> <p> <img src="assets/offer-picker.png" id="image_1077A6C7A8DD40FB9370CB55BD7260E5" /> </p> <p>Per ulteriori informazioni, vedere <a href="/help/main/c-experiences/c-manage-content/manage-content.md#concept_17874A6FCBB743AA84C5988E8571CCF3" format="dita" scope="local"> offerte </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Compositore esperienza basato su moduli </p> </td> 
   <td colname="col2"> <p>Nel Compositore esperienza basato su moduli, i Perfezionamenti sono stati sostituiti da funzionalità di pubblico complete. I perfezionamenti per le attività esistenti vengono trasferiti ai tipi di pubblico per sola attività. (TGT-13646) </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local">Compositore esperienza basato su moduli</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Token di risposta </p> </td> 
   <td colname="col2"> <p>È ora possibile creare token di risposta direttamente da Target senza attendere che vengano creati o importati. In precedenza, era possibile visualizzare solo i token creati tramite API all'interno dell'Interfaccia utente del token di risposta. Le modifiche apportate alla funzione consentono inoltre di evitare duplicati dei token di risposta. (TGT-26534) </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/administrating-target/response-tokens.md#concept_2B21B222F6A344D68CA5929817E836C4" format="dita" scope="local">Token di risposta</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Miglioramenti, correzioni e modifiche**

Questa versione di [!DNL Target] include i miglioramenti, le correzioni e le modifiche seguenti per i clienti:

* Puoi eliminare i tipi di pubblico importati (Target Classic, Experience Cloud, ecc.) dalla Libreria tipi di pubblico. Target avverte se si tenta di eliminare il pubblico di un&#39;attività attiva. (TGT-25171)
* I tipi di pubblico importati da Target Classic sono ora etichettati come Adobe Target Classic nella libreria Pubblico. In passato, nell’interfaccia utente non vi era distinzione tra Target Standard/Premium e Target Classic. (TGT-27093)
* Le Raccolte si applicano ora a tutti i criteri (inclusi gli elementi visualizzati di recente). (TGT-26646)
* Nella libreria Pubblico e nella Libreria delle offerte è possibile filtrare in base all’Area di lavoro (funzione disponibile per gli utenti Target Premium con autorizzazioni per gli utenti Enterprise). (TGT-26813)
* Sono stati apportati miglioramenti nell&#39;interfaccia utente dei Rapporti per ottimizzare lo scorrimento degli elenchi a discesa dei filtri all&#39;interno delle tabelle e dei posizionamenti. (TGT-23713 e TGT-26819)

### Modifiche alla piattaforma Target (13 ottobre 2017) {#section_6C298C5C3D01415CB4B658EB2166096C}

<table id="table_8457FAE3508F454F9DFDEF093FBD7E40"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Modifica </th> 
   <th colname="col2" class="entry"> Dettagli </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> at.js </span> </p> </td> 
   <td colname="col2"> <p><b>13 ottobre 2017</b> </p> <p> È ora disponibile la versione 1.2.1 di <span class="filepath">at.js</span>. Per ulteriori informazioni, consulta <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it" format="dita" scope="local">Dettagli della versione di at.js</a>. </p> <p> 
     <ul id="ul_14D6BB3B51974789BBFC036A45B7A56B"> 
      <li id="li_AE9826C8FC4A4DF4BE61BB72C2946C93"> <p>È stato risolto un problema che impediva a Target di aprire il collegamento in una nuova scheda durante il tracciamento dei clic su un collegamento con target="_blank". </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 17.9.1 (25 settembre 2017 e 12 ottobre 2017) {#section_ECC5DD8B6ED443788B46F53E25FC896E}

Questa versione include i miglioramenti e le funzioni seguenti (i codici tra parentesi sono per uso interno di Adobe):

<table id="table_0A8817F64F434875A485FD671C6988AB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> Anteprima dell'esperienza mobile </p> </td> 
   <td colname="col2"> <p><b>Aggiornamento: 12 ottobre 2017</b> </p> <p> È ora possibile selezionare più attività di app mobile dall'interfaccia utente e visualizzarle in anteprima sul dispositivo. Questa funzione ti permette di sperimentare diverse modalità di anteprima e controllo qualità senza doverti affidare a particolari generatori di test e simulatori. </p> <p>Per eseguirla, è necessario scaricare e installare la versione 4.14 (o successiva) appropriata di Adobe Mobile SDK. </p> <p>Per ulteriori informazioni, vedere <a href="https://experienceleague.adobe.com/docs/target-dev/developer/mobile-apps/target-mobile-preview.html?lang=it" format="dita" scope="local"> Anteprima mobile di Target </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Consegna a dispositivi mobili con funzioni batch e preacquisizione </p> </td> 
   <td colname="col2"> <p><b>Aggiornamento: 12 ottobre 2017</b> </p> <p> Il contenuto di più mbox può essere pre-acquisito in una singola chiamata e memorizzato nella cache locale del dispositivo senza preoccuparsi di come, quando e se l'utente finale vedrà il contenuto. </p> <p>Per eseguirla, è necessario scaricare e installare la versione 4.14 (o successiva) appropriata di Adobe Mobile SDK. </p> <p>Per ulteriori informazioni, vedere <a href="https://experienceleague.adobe.com/docs/target-dev/developer/mobile-apps/version-4/prefetch-offer-content.html?lang=it" format="dita" scope="local"> Preacquisizione del contenuto dell'offerta </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Attività </p> </td> 
   <td colname="col2"> <p>Nel flusso di lavoro di creazione delle attività sono stati apportati i seguenti miglioramenti: </p> <p> 
     <ul id="ul_2D251AC11FC54E86AE84DEFFB6FDF43C"> 
      <li id="li_AB8F12B3CF654120BD16EAE570517741"> <p>Durante la modifica di un'attività, è possibile apportare le variazioni desiderate nel passaggio che stai visualizzando: fai clic sul menu a discesa dal pulsante di menu combinato, quindi seleziona <span class="wintitle">Avanti</span> per passare alla fase successiva; fai clic su <span class="wintitle">Salva e Chiudi</span> per salvare le modifiche e visualizzare la pagina <span class="wintitle">Panoramica</span> dell'attività oppure clicca su <span class="wintitle">Salva</span> per salvare le modifiche e rimanere in tale fase. </p> <p> <img src="assets/edit_split_button_2.png" id="image_ABC7EE42F5D341EC88AACC54CA98DA2F" /> </p> <p>Per ulteriori informazioni, vedere <a href="/help/main/c-activities/edit-activity.md#concept_BB064C0D4A194BD1A1AE7CCA1E6BB8F0" format="dita" scope="local"> Modificare un'attività</a>. </p> </li> 
      <li id="li_4C71E2570ECF4BBAB08443D89230CE82"> <p>Durante la modifica di un'attività, puoi aprire il passaggio desiderato del flusso di lavoro, apportare le modifiche (ad esempio le percentuali di esperienza, il pubblico e così via), quindi salvare o chiudere l'attività senza dover seguire i tre passaggi del flusso di lavoro guidato. </p> <p> <img src="assets/edit_activity.png" id="image_0B9A2EF729C34A1D9FA84B8B7B17A3C1" /> </p> <p>Per ulteriori informazioni, vedere <a href="/help/main/c-activities/edit-activity.md#concept_BB064C0D4A194BD1A1AE7CCA1E6BB8F0" format="dita" scope="local"> Modificare un'attività</a>. </p> </li> 
      <li id="li_36EF9AD13B2D40ADB99343C9F758D5FD"> <p>Durante la scelta del destinatario nella fase 2 del flusso di lavoro guidato in tre passaggi, è ora possibile modificare o copiare un pubblico passando il puntatore sul pubblico desiderato nella finestra di dialogo <span class="wintitle">Scegli pubblico</span>. </p> <p> <img src="assets/audience_picker_hover.png" id="image_6DC33A0856A346948E517F0BA4C9039F" /> </p> </li> 
     </ul> </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md#concept_A268236C1224451DB7844BF67F41A087" format="dita" scope="local">Selezionare pubblico</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Generazione di rapporti </p> </td> 
   <td colname="col2"> <p>Per la generazione rapporti sono disponibili le nuove funzioni e i miglioramenti seguenti: </p> <p> 
     <ul id="ul_2D1AF91D1B4E478FBFFA0B83EE30075E"> 
      <li id="li_98E67A4DA8BF4CFF90C279FAC12F4C54"> <p>È possibile scegliere la metodologia di conteggio per i grafici del rapporto. Nota che questo non è supportato nelle attività Targeting automatico e Automated Personalization (AP). </p> <p>Per ulteriori informazioni, consulta la riga “Metodologia di conteggio” in <a href="/help/main/c-reports/c-report-settings/report-settings.md#concept_4BB6A7FDAB6F4806A632F9CD989B8BFA" format="dita" scope="local">Impostazioni rapporti</a>. </p> </li> 
      <li id="li_5803CE90DB764C9E983702CB6C1AFEE3"> <p>Puoi visualizzare più metriche in un singolo rapporto per le attività A/B con Targeting automatico. (TGT-23464) </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-reports/c-report-settings/view-multiple-metrics.md#concept_9E3C3F6F3EC1412FAF252975AC0720B7" format="dita" scope="local">Visualizzare più metriche in un rapporto</a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tipi di pubblico </p> </td> 
   <td colname="col2"> <p>È ora possibile visualizzare le definizioni dei tipi di pubblico importati da Target Classic o creati tramite API. (TGT-22630) </p> <p> <img src="assets/imported_mobile_audience_rn.png" id="image_6ED9EA63FD7D440286DBAFDBD696BA64" /> </p> <p>Per ulteriori informazioni, vedere "Visualizzazione delle definizioni del pubblico" in <a href="/help/main/c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271" format="dita" scope="local"> Informazioni sui tipi di pubblico </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Editor di codice </p> </td> 
   <td colname="col2"> <p>Il Compositore esperienza basato su moduli e l'editor offerte HTML ora utilizzano lo stesso editor di codice utilizzato dal Compositore esperienza visivo nel codice personalizzato. (TGT-25808) </p> <p>Questo miglioramento aggiunge le seguenti nuove funzioni quando si utilizza l'editor di codice nel Compositore esperienza basato su moduli e quando si creano offerte HTML: </p> <p> 
     <ul id="ul_CBB17806FBF34774A8160A61204ED014"> 
      <li id="li_22665F583F1742E280D5BC7EC4203007"> <p>I numeri di riga sono ora visibili per una migliore fruibilità. </p> </li> 
      <li id="li_B0D863CDAD2E46A4B133BB86886EB527"> <p>L’evidenziazione della sintassi ti aiuta a evitare errori di sintassi per le offerte HTML. </p> </li> 
     </ul> </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md#concept_B3A6E9EE3A60406DB640E205EA1745B5" format="dita" scope="local">Editor di codice</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Geotargeting </p> </td> 
   <td colname="col2"> <p>È ora possibile utilizzare la latitudine e la longitudine nel geotargeting. (TGT-12129) </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-target/c-audiences/c-target-rules/geo.md#concept_5B4D99DE685348FB877929EE0F942670" format="dita" scope="local">Geo</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SDK di node.js </p> </td> 
   <td colname="col2"> <p>È possibile installare gli SDK di node.js da <a href="https://www.npmjs.com/package/@adobe/target-node-client" format="https" scope="external">npm @adobe/target-node-client</a> per implementare ed eseguire facilmente i test lato server sulle applicazioni node.js. Negli SDK di node, il servizio ID visitatore è abilitato per connettere tutti i dati Adobe ed è possibile utilizzare Adobe Analytics come origine per la generazione rapporti (A4T). </p> </td> 
  </tr> 
 </tbody> 
</table>

**Miglioramenti, correzioni e modifiche**

Questa versione di [!DNL Target] include i miglioramenti, le correzioni e le modifiche seguenti per i clienti (i codici tra parentesi sono per uso interno di Adobe):

* Gli utenti con autorizzazioni di Approvatore possono ora generare e attivare token di autenticazione API di profilo. (TGT-24074)

  Per ulteriori informazioni, consulta [Impostazioni API di profilo](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/profile-api-settings.html?lang=it){target=_blank}.

* Quando, durante la creazione di un’attività in Compositore esperienza visivo, l’utente ricarica la pagina, l’URL dell’attività e le proprietà associate vengono mantenuti nell’interfaccia utente. La necessità di ricaricare può verificarsi nel caso in cui l&#39;attività utilizzi un contenuto misto (contenuto protetto e non protetto) o nel caso siano presenti problemi di autorizzazione. (TGT-28230)
* È stata migliorata la messaggistica quando un&#39;attività utilizza contenuto misto (contenuto protetto e non protetto). Il messaggio fornisce informazioni per consentire agli utenti di eseguire i passaggi necessari per aprire un sito HTTP o un sito con chiamate miste (HTTPS e HTTP). (TGT-26271)

Per ulteriori informazioni, consulta [Abilitazione di contenuto misto nel browser](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/mixed-content.md#concept_46D022D50280468C9EF6D5DF6EFC911C).

* È stato migliorato il flusso di lavoro quando la sessione Target di un utente scade durante la configurazione delle opzioni nelle pagine Amministrazione, Tipi di pubblico e Consigli. Quando l&#39;utente fa clic su Salva viene visualizzato il messaggio di sessione scaduta; effettuando di nuovo il log in, una finestra di dialogo informa l&#39;utente che l&#39;accesso è andato a buon fine e l&#39;interfaccia utente rimane nella stessa pagina di Target senza perdita di dati. (TGT-25557)

### Modifiche alla piattaforma Target (27 settembre 2017) {#section_AC32516DFBA64AD2AC9A74171D452778}

<table id="table_701D8D53D1DF4F28ADAC6EC221B0208A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Modifica </th> 
   <th colname="col2" class="entry"> Dettagli </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> at.js </span> </p> </td> 
   <td colname="col2"> <p><b>27 settembre 2017</b> </p> <p> La versione 1.2.0 di <span class="filepath">at.js</span> è ora disponibile in una versione di manutenzione che contiene per lo più correzioni di bug. Per ulteriori informazioni, consulta <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it" format="dita" scope="local">Dettagli della versione di at.js</a>. </p> <p> 
     <ul id="ul_D11024549C3643C7A756988087498D24"> 
      <li id="li_E1B3994125B64F6AB20B29FE8BCD8459"> <p>È stato risolto un problema che impediva azioni predefinite per i casi speciali di tracciamento dei clic. (TNT-28089) </p> </li> 
      <li id="li_53806C902AA04B31B59AA87A1E707348"> <p>È stato risolto un problema che impediva a Target di aprire il collegamento in una nuova scheda durante il tracciamento dei clic con un collegamento contenente <span class="codeph">target="_blank"</span>. (TNT-28072) </p> </li> 
      <li id="li_94F5794330D14C71BA07B3F17D0705FD"> <p> Gli indirizzi IP possono essere utilizzati come dominio dei cookie. (TNT-28002) </p> </li> 
      <li id="li_7D2A11B17672419583F9632CDA00D28F"> <p>È stato risolto un problema che causava la visualizzazione momentanea di altro contenuto nelle offerte di reindirizzamento aventi una mbox globale o altre mbox regionali. (TNT-27978) </p> </li> 
      <li id="li_BA27A749A7A242478080F3D8E04148FC"> <p> È stato risolto un problema che causava un errore nell’impostazione di attività Targeting esperienza nel Compositore esperienza visivo durante il passaggio da Sfoglia a Componi e viceversa. (TNT-27942) </p> </li> 
      <li id="li_FA11ABA5B9CD435080426805C5359A51"> <p> È stata risolta la gestione errata delle classi di stile che causava la visualizzazione momentanea di altro contenuto sugli elementi contrassegnati per il monitoraggio dei clic. (TNT-27896) </p> </li> 
      <li id="li_E2DFBAE52FCA4996BA083868CBFCCD10"> <p>È stato corretto un problema a causa del quale i parametri mbox globali si mescolavano con gli altri parametri mbox. (TNT-27846) </p> </li> 
      <li id="li_B3153BBD66AA4D51AE81EF6C903CF78D"> <p>Sono state apportate modifiche per garantire che Handlebar, Mustache e altre librerie di modelli lato client siano gestite correttamente da <span class="filepath">at.js</span>. (TNT-27831) </p> </li> 
      <li id="li_B859939C1B5A4DF78CF8ADF236B88306"> <p>Sono state apportate modifiche per garantire che <span class="codeph">sdidParamExpiry</span> sia inizializzato correttamente e passato all’API visitatore. Questa è una regressione che è stata aggiunta a <span class="codeph">at.js 1.1.0</span>. Non influisce sulle versioni precedenti di <span class="filepath">at.js</span>. Questa modifica riguarda soltanto i clienti che usano offerte di reindirizzamento e A4T. (TNT-27791) </p> </li> 
      <li id="li_24A748DFB7824AE6AC7331B7EA940BFF"> <p>Sono state apportate modifiche per garantire che <span class="codeph">SCRIPT</span> venga eseguito indipendentemente dal tipo di attributo utilizzato. (TNT-27865) </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Targeting esperienza (XT) </p> </td> 
   <td colname="col2"> <p><b>21 settembre 2017</b> </p> <p>Con la versione del 21 settembre, in Target cambierà il modo in cui gli utenti vengono inseriti nelle esperienze di attività di targeting delle esperienze (XT) (campagne Pagina di destinazione in Target Classic). Per tutte le attività nuove ed esistenti sia in Target Standard/Premium che in Target Classic, gli utenti devono soddisfare le regole del targeting delle esperienze su ogni impression per poter continuare a vedere il contenuto dell’esperienza ed essere conteggiati nei rapporti. In precedenza, se l’utente non era più qualificato per alcuna esperienza, avrebbe continuato a vedere il contenuto dell’ultima esperienza per la quale si era qualificato, e ad essere conteggiato nei rapporti per tale esperienza. </p> <p>Con questa versione tale modifica avverrà automaticamente per tutte le attività esistenti e per ogni nuova attività creata dopo il rilascio. Se desideri continuare con il metodo precedente (prima del 21 settembre), puoi creare il pubblico utilizzando script di profilo in modo che un utente debba soddisfare una condizione solo una volta per continuare a rientrare in tale pubblico in futuro. Quindi, utilizza questo pubblico per ogni esperienza nell’attività. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 17.8.1 (22 agosto 2017) {#section_71A554D072F04B18B359C1626529E5D8}

<table id="table_AAC16F89060D4CC09762A370B86C0885"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" class="premium"> <p>Autorizzazioni utente Enterprise per Target Premium </p> </td> 
   <td colname="col2"> <p>Crea aree di lavoro separate in Target e quindi assegna agli utenti ruoli e autorizzazioni diversi per le singole proprietà digitali. </p> <p>Per ulteriori informazioni, vedere <a href="/help/main/administrating-target/c-user-management/property-channel/property-channel.md#concept_E396B16FA2024ADBA27BC056138F9838" format="dita" scope="local"> autorizzazioni per gli utenti Enterprise </a>. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Modalità controllo qualità </p> </td> 
   <td colname="col2"> <p>Verifica in modo facile e completo la qualità delle attività tramite collegamenti di anteprima che restano invariati, l’eventuale definizione di un pubblico di destinazione e rapporti di controllo qualità mantenuti separati dai dati delle attività live. </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-activities/c-activity-qa/activity-qa.md" format="dita" scope="local">Controllo qualità delle attività</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Miglioramenti, correzioni e modifiche**

Questa versione di [!DNL Target] include i miglioramenti, le correzioni e le modifiche seguenti per i clienti (i codici tra parentesi sono per uso interno di Adobe):

* Ora è possibile visualizzare i dettagli della definizione del pubblico in una scheda a comparsa in diverse aree nell’interfaccia utente di Target, senza aprire il pubblico. Questa funzionalità si applica solo ai tipi di pubblico creati in [!DNL Target Standard/Premium. (TGT-25772)].
* È ora possibile visualizzare le definizioni dei tipi di pubblico adhoc all&#39;interno della sezione creazione/panoramica dell&#39;attività. (TGT-25570)
* Le seguenti variabili sono ora disponibili come array [Velocity](/help/main/c-recommendations/c-design-overview/customizing-a-template.md#concept_94F1554C3F2E4CDB9A2C3D78F10EDA59): `entiites` e `entityN.categoriesList`.

### Modifiche alla piattaforma Target (3 agosto 2017) {#section_FA5BF6808EA74F3A9E8E941530879208}

<table id="table_1B43199F1AE64E69AE65313B23741444"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Modifica </th> 
   <th colname="col2" class="entry"> Dettagli </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> at.js </span> </p> </td> 
   <td colname="col2"> <p><b>3 agosto 2017</b> </p> <p> È ora disponibile la versione 1.1 di <span class="filepath">at.js</span>. Per ulteriori informazioni, consulta <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/deploy-at-js/implement-target-without-a-tag-manager.html?lang=it" format="dita" scope="local">Scarica at.js</a>. </p> <p>I miglioramenti e le correzioni seguenti sono inclusi nella versione 1.1 di <span class="filepath">at.js</span>: </p> <p> 
     <ul id="ul_B7408267413347888938E2E7D48ABDBD"> 
      <li id="li_4DDF6DCFE6014C6795B6A9C9DFB54C21"> <p>È stata aggiunta la gestione dei token di risposta. Per ulteriori informazioni, consulta <a href="/help/main/administrating-target/response-tokens.md#concept_2B21B222F6A344D68CA5929817E836C4" format="dita" scope="local">Token di risposta</a>. </p> </li> 
      <li id="li_741CD22B7D074FBA90180B2E36FACE0D"> <p>È stato risolto un problema in modo che <span class="codeph">document.currentScript polyfill</span> non interferisca con Angular 1.X. </p> </li> 
      <li id="li_EF1B3D3DCC7F4D2490D2BFE660EC661C"> <p>Sono state apportate modifiche per garantire che il tracciamento dei clic non interferisca con la proprietà di visibilità. Gli elementi di tracciamento dei clic sono contrassegnati con la classe CSS <span class="codeph">at-element-click-tracking</span> anziché <span class="codeph">at-element-marker </span>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 17.7.3 (3 agosto 2017) {#section_D90CB766679442C7A0642E5D79657674}

<table id="table_C81EA97B251547169BC9681E5DDB4B8F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Token di risposta </p> </td> 
   <td colname="col2"> <p>I token di risposta consentono di generare automaticamente le variabili ammissibili (ad esempio, gli attributi del profilo) nelle risposte di Target che assegnano attività (ad esempio, visualizza mbox). I token di risposta possono essere utilizzati a scopo di debug o per l'integrazione con provider di terze parti (ad esempio Clicktale). </p> <p>I token di risposta sono simili ai plug-in del server di <span class="keyword">Adobe Target Classic</span> e forniscono equivalenza di funzione tra le due soluzioni. </p> <p> <p>Nota: i token di risposta sono disponibili con <span class="filepath">at.js</span> 1.1 e versioni successive</span>. </p> </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/administrating-target/response-tokens.md#concept_2B21B222F6A344D68CA5929817E836C4" format="dita" scope="local">Token di risposta</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 17.7.2 (27 luglio 2017) {#section_6980EC04D3CF4A00919953B9B10BC472}

<table id="table_DB51BD66756F4EBD875ED008B2C7C5D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" class="premium"> <p>Targeting automatico </p> </td> 
   <td colname="col2"> <p>La funzionalità Targeting automatico è ora disponibile per tutti i clienti Target Premium. </p> <p>La funzione Targeting automatico utilizza l’apprendimento automatico avanzato per individuare più esperienze ad alte prestazioni definite dall’addetto al marketing. Inoltre, indica l’esperienza più adatta per ogni visitatore in base al suo profilo cliente individuale e al comportamento dei visitatori precedenti con profili simili, al fine di personalizzare contenuti e favorire le conversioni. </p> <p>Durante la creazione di un'attività A/B tramite il flusso di lavoro guidato in tre passaggi, è possibile scegliere di allocare il traffico utilizzando l'opzione <span class="wintitle">Targeting automatico per Esperienze personalizzate</span>: </p> <p> <img src="assets/auto-target-ui-small.png" id="image_DB7899CAD51D411EAB858CE132BECAA5" /> </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-activities/auto-target/auto-target-to-optimize.md" format="dita" scope="local">Targeting automatico per esperienze personalizzate</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 17.7.1 (20 luglio 2017) {#section_BB75DE30174F4ADD963451909FB81D74}

<table id="table_BCE36E0D56804E7B8861858DCF2F380E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Tipi di pubblico </p> </td> 
   <td colname="col2"> <p>Ora puoi visualizzare i dettagli della definizione di pubblico in vari luoghi dell'interfaccia utente di Target grazie a una scheda popup, senza dover aprire la sezione Pubblico. Questa funzionalità si applica solo ai tipi di pubblico creati in <span class="keyword">Target Standard/Premium</span>. </p> <p> <img src="assets/audience_details.png" id="image_AD0F411715DA43ACB4A913B1E54C13DC" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Metriche di successo </p> </td> 
   <td colname="col2"> <p>Precedentemente, Target consentiva la dipendenza da una singola metrica e quella metrica doveva essere raggiunta prima che il suo conteggio incrementasse. È ora possibile fornire dipendenza da più metriche, insieme alla flessibilità necessaria per decidere se la metrica deve essere raggiunta o non raggiunta per incrementare il conteggio. </p> <p>La funzionalità di dipendenza a metriche multiple non è supportata nei seguenti casi: </p> <p> 
     <ul id="ul_EC856F910B704D648065EA7DA13EE5B0"> 
      <li id="li_1A82414FE50B414CAA1A0A88E80BCC1B"> <p>Attività di Consigli. Questa funzionalità è supportata da tutti gli altri tipi di attività. </p> </li> 
      <li id="li_2D6CF42264D445FCB6C400ED321DE952"> <p>Se si utilizza Analytics come fonte di Reporting (A4T). </p> </li> 
      <li id="li_E3A983A70BB04AE8B25A7CEC1F5FE1D9"> <p>Il tipo di metrica "Visualizzazione di una pagina". </p> </li> 
      <li id="li_9AAF6BB275F7489BA691676E308172D5"> <p>Il tipo di metrica "Clic su un elemento" per le attività del Compositore esperienza visivo. </p> </li> 
     </ul> </p> <p>Per maggiori informazioni, vedi i seguenti argomenti: </p> <p> 
     <ul id="ul_4B0EFFDD257C42579E19569DCBE15BE3"> 
      <li id="li_2402575F27F547968BD536C460BF81B5"> <p>A/B: <a href="/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC" format="dita" scope="local">Obiettivi e impostazioni </a> </p> </li> 
      <li id="li_FB5E7CBC0154406C989F5A5C6CAA0C8F"> <p>Automated Personalization (AP): <a href="/help/main/c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local">Creazione di un’attività di personalizzazione automatica </a> </p> </li> 
      <li id="li_57C36A7945A24A52BCBD62CA0F15B668"> <p>Targeting esperienza (XT): <a href="/help/main/c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC" format="dita" scope="local">Obiettivi e impostazioni </a> </p> </li> 
      <li id="li_06674A3152A547268A1AE5EE818EF1A5"> <p>Multivariate (MVT): <a href="/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC" format="dita" scope="local">Obiettivi e impostazioni </a> </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Generazione rapporti (allocazione automatica di test A/B) </p> </td> 
   <td colname="col2"> <p>È ora disponibile la possibilità di visualizzare più metriche per l'allocazione automatica di attività A/B. </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-reports/c-report-settings/view-multiple-metrics.md#concept_9E3C3F6F3EC1412FAF252975AC0720B7" format="dita" scope="local">Visualizzare più metriche in un rapporto</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tipi di pubblico </p> </td> 
   <td colname="col2"> <p>I tipi di pagina del sito e gli operatori di confronto del pubblico ora corrispondono ai tipi e agli operatori di confronto di Target Classic. </p> <p>Puoi creare un pubblico delle pagine del sito utilizzando “parametro di query definito dall'utente” o “intestazione definita dall'utente”. </p> <p>Per ulteriori informazioni, vedere <a href="/help/main/c-target/c-audiences/c-target-rules/site-pages.md#concept_6425D5304568490899E8340CC94798A9" format="dita" scope="local"> pagine del sito </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Attività </p> </td> 
   <td colname="col2"> <p>L'elenco Attività consente ora di filtrare i tipi di attività di Allocazione automatizzata e di Targeting automatico. </p> <p>Per ulteriori informazioni, vedere <a href="/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> attività </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Criteri e promozioni dei consigli </p> </td> 
   <td colname="col2"> <p>È ora possibile gestire i valori vuoti durante l'applicazione di filtri per Corrispondenza attributo entità, Corrispondenza attributo profilo e Corrispondenza parametri. </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F" format="dita" scope="local">Utilizzare regole di inclusione dinamiche e statiche</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Questa versione di [!DNL Target] include i seguenti miglioramenti e correzioni di problemi rivolti al cliente: (i codici tra parentesi sono per uso interno di Adobe):

* È stato migliorato il flusso di lavoro nel caso in cui, durante la creazione o la modifica di un&#39;attività o di un&#39;offerta da parte dell&#39;utente, la sessione di [!DNL Target] risulti scaduta. Quando l&#39;utente fa clic su [!UICONTROL Save], viene visualizzato il messaggio di sessione scaduta, ma dopo aver effettuato di nuovo il log in, una finestra di dialogo informa l&#39;utente che l&#39;accesso è andato a buon fine e l&#39;interfaccia utente rimane nella stessa pagina in [!DNL Target] senza perdita di dati.

  Se durante l&#39;esecuzione di un&#39;azione intermittente in una pagina di [!DNL Target] si verifica un arresto di sessione, l&#39;utente è invitato a eseguire nuovamente l&#39;accesso e viene quindi indirizzato all&#39;ultima pagina da lui modificata nell&#39;interfaccia utente di [!DNL Target].

* È stato risolto un problema che causava la perdita delle modifiche al codice personalizzato se l’utente si allontanava (cambiava le esperienze, cambiava pagina, cambiava pubblico, faceva clic su Avanti, ecc.) e dimenticava di salvare le modifiche. All&#39;utente viene ora richiesto di salvare le modifiche. (TGT-23766)
* Quando un&#39;attività viene archiviata, viene visualizzato il messaggio “archiviazione dell&#39;attività” anziché “aggiornamento dell&#39;attività”. (KB-1517)
* Il selettore a discesa nelle seguenti posizioni all&#39;interno dell&#39;interfaccia utente di Target è stato sostituito con funzionalità di completamento automatico per migliorarne la velocità e le prestazioni: (TGT-22939)

   * Pagina attività > *attività* > Passaggio 3 > Selettore suite di rapporti
   * Tipi di pubblico > Crea pubblico > Profilo visitatore
   * Consigli > Creazione feed > se tipo di origine > Analytics > Selettore suite di rapporti

* È stata migliorata la messaggistica di errore quando un sito dispone di “opzioni X-frame” impostate su SAMEORIGIN e il sito non può essere caricato nel Compositore esperienza visivo. All’utente viene presentato un messaggio in cui si chiede di passare al Compositore esperienza avanzato in Amministrazione > Compositore esperienza visivo. (TGT-17356)
* In Target Standard/Premium, i rapporti vengono ora visualizzati nel fuso orario del tuo account anziché nel fuso orario del server di Target (US EST). (TGT-24868)
* Se le attività create in [!DNL Target] vengono aggiornate all&#39;esterno di [!DNL Target] (ad esempio, tramite Adobe I/O), i seguenti attributi di attività vengono importati di nuovo in [!DNL Target]:

  `thirdpartyId`

  `startDate`

  `endDate`

  `status`

  `priority`

  `marketingCloudMetadata(remoteModifiedBy)`

  Questo processo di importazione verrà eseguito quando verrà aperta la pagina attività, con un ritardo massimo di dieci minuti. (KB-1526)

### Target Standard/Premium 17.6.2 (22 giugno 2017) {#section_F0372B07B56E454CB048CE79FF56E9CD}

<table id="table_8C4DB1B83B874E4C85CE9FF352E7B857"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" class="premium"> <p>Attività di Automated Personalization (AP) </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_F5BB1074DD4140C798CB55D68DEEF824"> 
      <li id="li_9596AABA14C64DEEB2E70E8ADED8AA74">È possibile creare attività di Automated Personalization utilizzando il Compositore basato su moduli. </li> 
      <li id="li_315F5FF590404670A677FEA6E4E0DF5D">Nuovi valori di affidabilità per la Automated Personalization </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Consigli: criteri e promozioni </p> </td> 
   <td colname="col2"> <p> È ora possibile creare criteri dinamici e promozioni in base alla corrispondenza degli attributi del profilo e alla corrispondenza di parametri. </p> <p> <img src="assets/inclusion_rules.png" id="image_D136F75A5C2B428390FE231559AEC2D3" /> </p> <p> <p>Nota: se hai dimestichezza con la configurazione delle regole di inclusione prima della versione di Target 17.6.1 (giugno 2017), noterai che alcune delle opzioni e degli operatori sono cambiati. Vengono visualizzati solo gli operatori applicabili all’opzione selezionata; alcuni altri operatori sono stati rinominati (“corrisponde a” è ora “è uguale a”), per maggiore coerenza e intuitività. Tutte le regole di esclusione esistenti create prima di questa versione sono state automaticamente convertite nella nuova struttura. Non è necessaria alcuna modifica da parte dell’utente. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Miglioramenti dell'Editor di codice del Compositore esperienza visivo </p> </td> 
   <td colname="col2"> <p> Se il formato della pagina cambia e alcune azioni non possono essere eseguite, ora viene visualizzato un avviso di errore accanto a ogni azione che non può essere elaborata. In precedenza, un errore generale notificava all'utente che la struttura della pagina era cambiata. Ora, invece, l'editor di codice evidenzia ogni azione non riuscita. </p> </td> 
  </tr> 
 </tbody> 
</table>

Questa versione di [!DNL Target] include i miglioramenti e le correzioni seguenti per il cliente:

* Prestazioni ottimizzate sui gruppi host e sulle pagine di ricerca di entità consigli.
* In tutte le sezioni di Target, i messaggi di errore sono più descrittivi, specialmente se correlati agli errori di sincronizzazione.
* È stato corretto un problema che a volte causava un errore di conteggio sul diagramma di attività nell&#39;interfaccia utente, quando veniva applicata l&#39;eliminazione automatica dei duplicati dopo la creazione di gruppi di esclusione.
* È stato risolto un problema a causa del quale le inclusioni manuali potevano non venire riportate correttamente nell&#39;interfaccia utente quando veniva modificata un&#39;attività esistente tramite il Gruppo di esclusione.

### Target Standard/Premium 17.6.1 (8 giugno 2017) {#section_1D05FE23CE3744DDB5D28E933341F575}

<table id="table_47117524922A472AA977C652B581B356"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Attività di Targeting di esperienza (XT) </p> </td> 
   <td colname="col2"> <p>La funzionalità drag-and-drop consente di organizzare il pubblico e le esperienze nell'ordine desiderato durante la creazione o la modifica di attività di Targeting di esperienza (XT). I visitatori saranno valutati per le esperienze, nell'ordine dall'alto verso il basso. </p> <p> <img src="assets/move_exp.jpg" id="image_0AA2EE2B5B00462C8E125A30F145E654" /> </p> <p>Per ulteriori informazioni, vedere <a href="/help/main/c-activities/t-experience-target/t-xt-create/xt-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00" format="dita" scope="local"> Creare l'esperienza </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Generazione rapporti: A/B, Targeting esperienza e Consigli </p> </td> 
   <td colname="col2"> <p>Rapporti per le attività A/B, Targeting esperienza e Consigli includono rappresentazioni visive che consentono di visualizzare visivamente l'intervallo di affidabilità e di incrementarlo in modo da poter determinare più accuratamente un vincitore. Passando il mouse sopra le rappresentazioni, puoi vedere i numeri reali. Questa funzionalità non è disponibile per le attività che utilizzano Analytics come origine per la generazione di rapporti (A4T). </p> <p> <img src="assets/whisker.JPG" id="image_DFD8EED61D52497280066D55AD473479" /> </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-reports/c-report-settings/report-settings.md#concept_4BB6A7FDAB6F4806A632F9CD989B8BFA" format="dita" scope="local">Impostazioni dei rapporti</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Attività di Automated Personalization (AP) </p> </td> 
   <td colname="col2"> <p>È possibile creare Gruppi di esclusione nelle attività AP per escludere automaticamente le esperienze con le offerte designate. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Consigli: criteri e promozioni </p> </td> 
   <td colname="col2"> <p><b>(Programmata per essere rilasciata il 22 giugno 2017)</b> È ora possibile creare criteri dinamici e promozioni in base alla corrispondenza degli attributi del profilo e alla corrispondenza dei parametri. </p> <p> <img src="assets/inclusion_rules.png" id="image_694305D969AF43F7822012F69614250C" /> </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F" format="dita" scope="local">Utilizzare regole di inclusione dinamiche e statiche</a>. </p> <p> <p>Nota: se hai dimestichezza con la configurazione delle regole di inclusione prima della versione di Target 17.6.1 (giugno 2017), noterai che alcune delle opzioni e degli operatori sono cambiati. Vengono visualizzati solo gli operatori applicabili all’opzione selezionata; alcuni altri operatori sono stati rinominati (“corrisponde a” è ora “è uguale a”), per maggiore coerenza e intuitività. Tutte le regole di esclusione esistenti create prima di questa versione sono state automaticamente convertite nella nuova struttura. Non è necessaria alcuna modifica da parte dell’utente. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Denominazione delle attività </p> </td> 
   <td colname="col2"> <p>Prima del salvataggio, viene ora richiesto di assegnare un nome all'attività. Non è possibile salvare un'attività senza un nome. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Nuova posizione del Forum di Target </p> </td> 
   <td colname="col2"> <p> Il Forum di Target è stato spostato nella nuova <a href="https://experienceleaguecommunities.adobe.com/t5/adobe-target/ct-p/adobe-target-community" format="https" scope="external">Piattaforma di Adobe Community</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 17.4.1 (27 aprile 2017) {#section_24E6889AF1E0405497F6F77A407A9A46}

Questa versione include i miglioramenti e le funzioni seguenti:

<table id="table_9554D0094421417C88548BDC97B710F5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Dettagli </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Generazione di rapporti </td> 
   <td colname="col2"> <p><b>Visualizzazione di più obiettivi/metriche:</b> È ora possibile visualizzare più metriche nelle attività A/B e Targeting esperienza (XT), ad eccezione delle attività A/B di <a href="/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4" format="dita" scope="local"> Allocazione automatica </a> e <a href="/help/main/c-activities/auto-target/auto-target-to-optimize.md" format="dita" scope="local"> Targeting automatico di </a>. </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-reports/c-report-settings/view-multiple-metrics.md#concept_9E3C3F6F3EC1412FAF252975AC0720B7" format="dita" scope="local">Visualizzare più metriche in un rapporto</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Questa versione di [!DNL Target] si concentra su correzioni back end e include i seguenti miglioramenti e correzioni di problemi rivolti al cliente: (i codici tra parentesi sono per uso interno di Adobe):

* È stato corretto un problema che causava il malfunzionamento dell&#39;impostazione “Incrementa il conteggio, rilascia l&#39;utente e consenti il reinserimento”, nelle impostazioni avanzate delle attività. (TNT-26556)
* È stato risolto un problema che impediva la rimozione da Target dei dati degli Attributi dei clienti dopo che questi erano stati aggiornati con NULL nell&#39;interfaccia utente di Experience Cloud. (TNT-26462)

### Modifiche alla Piattaforma Target (13 aprile 2017) {#section_B59C26405EB7482AA80820D6D39B9C44}

<table id="table_6167ECB7B44F40DCADF299F46F1F795C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Modifica </th> 
   <th colname="col2" class="entry"> Dettagli </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> at.js </span> </p> </td> 
   <td colname="col2"> <p> È ora disponibile la versione 0.9.6 di <span class="filepath">at.js</span>. Per ulteriori informazioni, consulta <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/deploy-at-js/implement-target-without-a-tag-manager.html?lang=it" format="dita" scope="local">Scarica at.js</a>. </p> <p>I miglioramenti e le correzioni seguenti sono inclusi nella versione 0.9.6 di <span class="filepath">at.js</span>: </p> <p> 
     <ul id="ul_108DF85393614C69988E299485D338FD"> 
      <li id="li_4117C900982240B5AFFCFE1B2716A443"> <p>Supporto per le offerte di reindirizzamento per A4T. Dopo aver scaricato e installato la versione 0.9.6 di <span class="filepath">at.js</span>, è possibile utilizzare le offerte di reindirizzamento in attività che utilizzano <span class="keyword">Adobe Analytics</span> come origine per la generazione di rapporti per <span class="keyword">Target</span> (A4T). Oltre alla versione 0.9.6 di <span class="filepath">at.js</span>, l’implementazione deve soddisfare altri requisiti minimi al fine di usare le offerte di reindirizzamento e A4T. Per ulteriori informazioni e importanti informazioni aggiuntive che dovresti conoscere, consulta <a href="/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#concept_21BF213F10E1414A9DCD4A98AF207905" format="dita" scope="local">Offerte di reindirizzamento: domande frequenti su A4T.</a> </p> </li> 
      <li id="li_DA5321D72E81496DB7C49D589E1A59C4"> <p>Prima della versione 0.9.6 di <span class="filepath">at.js</span>, se l’API visitatore era presente nella pagina e l’impostazione <span class="codeph">visitorApiTimeout</span> era troppo aggressiva, poteva capitare che i dati ECID non venissero inviati nella richiesta di <span class="keyword">Target</span>. Questo poteva portare a problemi come la presenza di dati parziali in <span class="keyword">Analytics</span> durante l’utilizzo di A4T. </p> <p>Questo comportamento è stato modificato nella versione 0.9.6 di <span class="filepath">at.js</span>: anche se l’impostazione <span class="codeph">visitorApiTimeout</span> è impostata su 1 ms, ad esempio, Target tenterà di raccogliere SDID, server di tracciamento e dati degli ID cliente, per inviarli nella richiesta di Target. </p> </li> 
      <li id="li_B11CE11D9A594CB1ABB85BD0D93C4A15"> <p>È stata aggiunta l’impostazione <span class="codeph">selectorsPollingTimeout</span>. Per ulteriori informazioni, consulta <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/atjs-functions.html?lang=it" format="dita" scope="local">targetGlobalSettings()</a>. </p> </li> 
      <li id="li_D6F862099A374FE394F4DA3520A1BBF0"> <p>Il formato della risposta da <span class="codeph">getOffer()</span> è stato modificato. Per ulteriori informazioni, consulta <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/atjs-functions.html?lang=it" format="dita" scope="local">adobe.target.getOffer(options)</a>. </p> </li> 
      <li id="li_80166567ED8945ECB37FEEE2C5F06ACE"> <p>La funzione di log della console è stata aggiunta per le dichiarazioni <span class="codeph">&lt;!DOCTYPE&gt;</span> non supportate. </p> </li> 
      <li id="li_02904EBAE8D3400092B762F0B28B0C86"> <p>È stato risolto un problema a causa del quale i plug-in <span class="keyword"> di Target Classic </span> non venivano applicati correttamente quando venivano distribuite offerte multiple predefinite a un singolo mbox. (TGT-22664)</p> </li> 
      <li id="li_7016022D9DDE4529B77984F195825AB7"> <p>È stata migliorata la configurazione dei cookie per i domini di primo livello a due lettere (TLD) per garantire che il cookie mbox venga configurato correttamente per questi domini (ad esempio, <span class="filepath">test.no</span>, <span class="filepath">autodrives.ca</span> e così via). </p> </li> 
      <li id="li_3B1F618DEC744056B5BB172C4DBB359A"> <p>L’algoritmo per l’estrazione del dominio di primo livello che deve essere utilizzato quando si salvano i cookie è stato modificato nella versione 0.9.6. di <span class="codeph">at.js</span>. A causa di questa modifica, i cookie non possono essere salvati in indirizzi IP. Il più delle volte, gli indirizzi IP vengono utilizzati per scopi di test, ma come soluzioni alternative è possibile utilizzare le voci DNS, regolare il file host in una casella locale. </p> </li> 
      <li id="li_A52181499E63402DB4E16E33E36A9400"> <p>Risolta la gestione delle azioni Sposta e Ridisponi nel caso in cui le proprietà siano valori stringa anziché numeri interi. </p> </li> 
     </ul> </p> <p>Per informazioni su questa versione e sulle versioni precedenti di <span class="filepath">at.js</span>, consulta <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it" format="dita" scope="local">Dettagli della versione di at.js.</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 17.3.1 (30 marzo 2017 - aggiornato il 13 aprile 2017) {#section_5C13660A8AA34F35A9CBEFEEC88738D0}

Questa versione include i miglioramenti e le funzioni seguenti:

<table id="table_4BA8DA701BC64427957355E144570EFE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Analytics for Target (A4T) </p> <p>Offerte di reindirizzamento </p> </td> 
   <td colname="col2"> <p><b>Aggiornato il 13 aprile 2017.</b> </p> <p>È ora possibile utilizzare le offerte di reindirizzamento nelle attività che utilizzano <span class="keyword">Analytics</span> come origine per la generazione rapporti. </p> <p>Queste librerie devono essere incluse sia nella pagina con l'offerta di reindirizzamento sia nella pagina a cui il visitatore viene reindirizzato. Come parte di questa modifica, i nuovi parametri URL verranno aggiunti automaticamente agli URL di reindirizzamento se il servizio ID visitatore è implementato nel sito, indipendentemente dal fatto che si stia utilizzando Analytics come origine per la generazione rapporti per quell'attività. </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#concept_21BF213F10E1414A9DCD4A98AF207905" format="dita" scope="local"> offerte di reindirizzamento - Domande frequenti su A4T </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tipi di pubblico </p> </td> 
   <td colname="col2"> <p>I seguenti miglioramenti sono stati apportati al targeting di pubblico: </p> <p> 
     <ul id="ul_C920198404654C97A33190A29ACA6990"> 
      <li id="li_DB52EF909C9640649981940460CDF2B5"> <p><b>Ripartizione tra settimana e giorno:</b> è possibile impostare le opzioni di <span class="wintitle">ripartizione settimana/giorno</span> per creare modelli ricorrenti per il targeting di pubblico. </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-target/c-audiences/c-target-rules/time-frame.md#concept_0FE1E8DACD104F8B870B0BADE3197F0A" format="dita" scope="local"> Arco temporale </a>. </p> </li> 
      <li id="li_2541A6EF2D604CE098012A16909C237E"> <p><b> Esclusioni nel pubblico combinato:</b> è ora possibile aggiungere regole di esclusione per escludere il pubblico quando si combinano più tipi di pubblico. </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5" format="dita" scope="local">Combinazione di più tipi di pubblico</a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Consigli </p> </td> 
   <td colname="col2"> <p><b>Promozioni dinamiche:</b> ora i consigli di Target supportano le corrispondenze dinamiche per le promozioni. </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F" format="dita" scope="local">Utilizzare regole di inclusione dinamiche e statiche</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>La possibilità di visualizzare più metriche in un rapporto, inclusa nella versione 17.3.1 di Target (30 marzo 2017), è stata rimossa a causa di un comportamento imprevisto. Questa funzione sarà nuovamente disponibile in una versione successiva.

Questa versione di [!DNL Target] include i seguenti miglioramenti e correzioni rivolti al cliente:

* L&#39;interfaccia utente di [!DNL Target] è stata aggiornata per supportare le offerte di reindirizzamento in attività che utilizzano [!UICONTROL Analytics for Target] (A4T) come origine per la generazione di rapporti. Questa funzionalità richiederà la versione 0.9.6 di [!DNL at.js], che sarà disponibile a breve.
* L&#39;interfaccia utente di [!DNL Target] è stata aggiornata in alcuni punti:

   * Nei report e nelle attività, è ora possibile accedere ad alcune opzioni ( [!UICONTROL Edit], [!UICONTROL Share to Feed], [!UICONTROL View Experience URLs], ecc.) facendo clic sull&#39;icona [!UICONTROL More Options] ( ![icon_more_options image](assets/icon_more_options.png)

      
   * Nella libreria [!UICONTROL Offers], le offerte ora vengono visualizzate in un elenco anziché come schede. Altre modifiche minori dell&#39;interfaccia utente sono state apportate in tutta l&#39;interfaccia utente della libreria [!UICONTROL Offers].

* Prestazioni significativamente migliorate negli elenchi [!UICONTROL Activity] e [!UICONTROL Audience]. Inoltre, i tempi di caricamento dei risultati di ricerca saranno di nuovo molto più veloci.
* &quot;Visualizzazioni&quot; è ora &quot;Visite&quot; in [!UICONTROL Offer Level Report] per [!UICONTROL Automated Personalization] rapporti.
* [!DNL Target] ora supporta il passaggio da un ambiente a un altro (gruppi host) per le attività [!UICONTROL Automated Personalization].
* [!UICONTROL Automated Personalization] attività ora supportano i gruppi host.

### Target Standard/Premium 17.2.1 (21 febbraio 2017) {#section_FC6412353DE64E848FFD5E8EFF72C7C7}

>[!NOTE]
>
>[!DNL Adobe Experience Manager] 6.2 con FP-11577 (o versioni successive) ora supporta [!DNL at.js] implementazioni con la relativa integrazione [!UICONTROL Adobe Target Cloud Services]. Per ulteriori informazioni, consulta [Pacchetti di funzionalità](https://experienceleague.adobe.com/docs/?lang=it) e [Integrazione con Adobe Target](https://experienceleague.adobe.com/docs/?lang=it) nella documentazione di *Adobe Experience Manager 6.2*.

Questa versione di [!DNL Target] è incentrata sulla fruibilità e sui miglioramenti delle prestazioni, e include i seguenti miglioramenti e correzioni (i codici tra parentesi sono per uso interno di Adobe):

* Sono stati aggiunti ulteriori elementi al menu della guida, a cui è possibile accedere dall&#39;angolo superiore destro dell&#39;interfaccia utente di [!DNL Target]. Le nuove opzioni includono: “Blog” e “Video”. L&#39;opzione “Adobe Experience Cloud Status” è ora “Adobe Target Standard/Premium Status”. (TGT-22629)
* Quando si elimina un pubblico,[!DNL Target] visualizza un elenco di attività che fanno riferimento a quel pubblico. Gli utenti possono fare clic su ogni attività nell&#39;elenco per visualizzare la relativa pagina [!UICONTROL Overview]. (TGT-17997)
* È stata migliorata la funzione `user.activeCampaigns`, che restituisce l&#39;ID della campagna per tutte le campagne/attività a cui l&#39;utente è iscritto, anche se non ha interagito con la campagna/attività nella sessione corrente. (TNT-26237)
* Il pulsante [!UICONTROL Create Activity] nella pagina [!UICONTROL Activities] è ora attivo prima che tutti i nomi di attività vengano caricati nell&#39;elenco. Questo miglioramento consente agli utenti di creare nuove attività più velocemente, soprattutto quando l&#39;account ha molte attività configurate. (TGT-21470)
* È stato implementato il Compositore esperienza avanzato per migliorare il tempo di caricamento dei siti Web che eseguono HTTPS con accesso tramite proxy. Target non recupera più risorse statiche tramite proxy. (TGT-21793)
* Sono stati apportati miglioramenti alle prestazioni sulla pagina [!UICONTROL Goals & Settings], in particolare al tempo di caricamento quando sono definite molte metriche per un&#39;attività. (TGT-21654)
* Aggiunta una descrizione comandi nella pagina [!UICONTROL Goals & Settings] di tutte le attività che utilizzano [!UICONTROL Analytics for Target] (A4T), per informare gli utenti che non è necessario un server di tracciamento se nelle pagine dell&#39;attività è caricato at.js (versione 0.9.1 o successiva). (TGT-22607)
* I nomi delle metriche ora vengono visualizzati nella pagina [!UICONTROL Goals & Settings] senza che sia necessario espandere ogni metrica per visualizzare l&#39;intero nome della metrica. Questo miglioramento consente agli utenti di modificare le metriche più rapidamente e in modo più efficiente. (TGT-21276)
* È ora possibile applicare le regole di inclusione di [!DNL Recommendations] ai criteri personalizzati (aggiornamento tramite CSV), come per qualsiasi altro criterio. (TGT-21896)
* È stata migliorata l&#39;interfaccia utente e la facilità d&#39;uso della pagina [!UICONTROL Offers], in particolare durante la creazione o la gestione di cartelle e la creazione di offerte. (TGT-22509 e TGT-22187)
* È stata migliorata l&#39;esperienza utente nel Compositore esperienza visivo di [!UICONTROL Visual Experience Composer] quando si selezionano gli elementi da nascondere.
(TGT-22224)
* È stata migliorata l&#39;esperienza utente durante la creazione di attività utilizzando [!UICONTROL Form-Based Experience Composer]. Quando si sceglie un percorso mbox, il bordo di convalida rimane evidenziato dopo aver fatto clic su [!UICONTROL Next]. (TGT-22221)
* Sono stati ottimizzati i rapporti scaricati per distinguere tra le offerte attive ed eliminate. (TGT-22449)
* È stato risolto un problema che impediva la visualizzazione di risorse obsolete nell&#39;elenco a scorrimento infinito all&#39;interno dell&#39;interfaccia utente del servizio principale delle Risorse di Experience Cloud. (TGT-19733)
* È stato risolto un problema a causa del quale nei rapporti CSV scaricati non veniva rispettata l&#39;impostazione dell&#39;ordine estremo. (TGT-21871)
* È stato risolto un problema a causa del quale gli ordini estremi non venivano contrassegnati correttamente nel rapporto CSV [!UICONTROL Order Details] scaricato. (TGT-22500)
* È stato risolto un problema che causava la visualizzazione dell&#39;ora dell&#39;ordine errata nel rapporto CSV scaricato di [!UICONTROL Campaign Audit], anche se nel rapporto veniva visualizzata la data dell&#39;ordine corretta. (TNT-26469)
* È stato risolto un problema che impediva il corretto funzionamento dell&#39;opzione [!UICONTROL Disable JavaScript] nelle attività multipagina. (TGT-15130)
* Se utilizzi il Compositore esperienza basato su moduli con una mbox diversa da quella globale creata automaticamente (`target-global-mbox`) e selezioni una metrica di coinvolgimento come metrica di successo, potrai visualizzare gli incrementi di metrica solo sulle pagine che hanno la mbox utilizzata nell&#39;attività. Ad esempio, se la mbox è `homepage_mbox`, la metrica [!UICONTROL Pages Per Visit] è il numero di hit per `homepage_mbox` durante quella visita.

  È comunque possibile aggiungere un’altra posizione all’attività e assegnare la mbox globale a tale posizione, con il contenuto predefinito. Così facendo l’oggetto mbox globale viene collegato all’attività e Target può contare la metrica per la generazione di rapporti.

### Modifiche alla piattaforma Target (18 gennaio 2017) {#section_EA41802B2B24426FBA88D25E17DBE360}

<table id="table_3A2CD47252894F119B0E60BF6A9285B0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Modifica </th> 
   <th colname="col2" class="entry"> Dettagli </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> at.js</span> versione 0.9.4 </p> </td> 
   <td colname="col2"> <p>18 gennaio 2017 </p> <p> La versione 0.9.4 di <span class="codeph">at.js</span> contiene le seguenti modifiche: </p> <p> 
     <ul id="ul_8F149C28E2D946B9888B4D2F45167C3C"> 
      <li id="li_93E866BBFE374E93BCDB65BCFAC33B62"> <p> I nomi mbox possono ora contenere caratteri speciali, tra cui il simbolo e commerciale (&amp;). (TNT-26144) </p> <p>Per ulteriori informazioni, consulta <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/deploy-at-js/implement-target-without-a-tag-manager.html?lang=it" format="dita" scope="local">Configurazioni at.js</a>. </p> </li> 
      <li id="li_99309046030B4D93B59113C01A8789DA"> <p>È stata aggiunta l’impostazione <span class="codeph">secureOnly</span> che indica se <span class="codeph">at.js</span> deve utilizzare solo HTTPS o può passare da HTTP a HTTPS in base al protocollo della pagina. Si tratta di un’impostazione avanzata con impostazione predefinita False e può essere bypassata tramite <span class="codeph">targetGlobalSettings </span>. (TNT-26183) </p> <p>Per ulteriori informazioni, consulta <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/atjs-functions.html?lang=it" format="dita" scope="local">targetGlobalSettings()</a>. </p> </li> 
      <li id="li_D84D578C43A24D4896795999F841CEB8"> <p>L'opzione <span class="wintitle">Supporto di browser legacy</span> è disponibile nelle versioni 0.9.3 e precedenti di <span class="codeph">at.js</span>. Questa opzione è stata rimossa nella versione 0.9.4 di <span class="codeph">at.js</span>. </p> <p>Per ulteriori informazioni, consulta <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/deploy-at-js/implement-target-without-a-tag-manager.html?lang=it" format="dita" scope="local">Configurazioni at.js</a>. </p> </li> 
     </ul> </p> <p>Per informazioni dettagliate sulle modifiche apportate a ogni versione di <span class="codeph">at.js</span>, vedi <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it" format="html" scope="external">Dettagli sulla versione di at.js.</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 17.1.1 (19 gennaio 2017) {#section_88AFA2F54CF24DF7822CFEBB07DFABE2}

Questa versione include i miglioramenti e le funzioni seguenti:

<table id="table_4F7D4A71F5DF4E8782C7DBEEEF24AD04"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Contenuto/offerte </p> </td> 
   <td colname="col2"> <p>Per le offerte, sono ora disponibili i seguenti miglioramenti: </p> <p> 
     <ul id="ul_7D8E81443E0F48B6A0C1D1DF6F27D292"> 
      <li id="li_EA529EF4EBC2416E9D3B9E7251E7AAAB"> <p>La pagina Contenuti è stata rinominata Offerte. Inoltre, ci sono ora due schede lungo il lato destro per separare le offerte di codice dalle offerte di immagine. </p> <p>Se prima di questa versione usavi codici e immagini nella stessa cartella, Target li divide in due cartelle duplicate. </p> </li> 
      <li id="li_9574FA6BDCFB4BAB938273BF7F4B21C8"> <p>Le offerte create tramite Target Classic, Adobe Experience Manager (AEM), Adobe Mobile Services (AMS) e API sono ora visibili nell'interfaccia utente di Target Standard/Premium. Le offerte create in Target Classic sono modificabili in Target Standard/Premium. (TGT-15738) </p> <p> Le offerte che sono state aggiornate negli ultimi due anni utilizzando questi metodi saranno visibili in Target Standard/Premium (da gennaio 2015 e oltre). </p> </li> 
      <li id="li_CAD67C9EBB564525ABD2269D918275F8"> <p>È ora possibile filtrare le offerte per origine e tipo. </p> </li> 
     </ul> </p> <p>Per ulteriori informazioni, vedere <a href="/help/main/c-experiences/c-manage-content/manage-content.md#concept_17874A6FCBB743AA84C5988E8571CCF3" format="dita" scope="local"> offerte </a>. </p> <p>È stato apportato il seguente miglioramento al targeting di geolocalizzazione: </p> <p> 
     <ul id="ul_DD8B50F980B8447A8C37EA96530D8949"> 
      <li id="li_348E04AB29B14E6F83E3A7E7BF7D75B8"> <p>È ora possibile utilizzare i valori <span class="codeph">profile.geolocation</span> direttamente come token in offerte, plug-in e così via. (TNT-25967) </p> </li> 
     </ul> </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-target/c-audiences/c-target-rules/geo.md#concept_5B4D99DE685348FB877929EE0F942670" format="dita" scope="local">Geo</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Generazione di rapporti </p> <p> <p>Nota: questi miglioramenti non si applicano ai rapporti di Analytics for Target (A4T). </p> </p> </td> 
   <td colname="col2"> <p>I seguenti miglioramenti di generazione rapporti sono ora disponibili per i rapporti di Target. </p> <p> 
     <ul id="ul_ACFCA821B120419EA252EF5031309D52"> 
      <li id="li_0B634602BB044AEDB26DAF78189AB833"> <p>L'interfaccia utente per i rapporti è stata riprogettata. </p> </li> 
      <li id="li_309435D10AE84E8795C4CCC1F36747F7"> <p>I rapporti di Target ora hanno un'opzione che permette di reimpostare i dati di generazione rapporti per rimuovere i dati obsoleti. (TGT-5933) </p> </li> 
      <li id="li_9D30BFCC4CD6461B9DDCD5797A5E2B3A"> <p>Le opzioni di metodologia di conteggio per la generazione rapporti includono Visitatori (impostazione predefinita), Visite e Impression di attività. (TGT-10002) </p> </li> 
     </ul> </p> <p>Per ulteriori informazioni, vedere <a href="/help/main/c-reports/statistical-methodology/statistical-calculations.md" format="dita" scope="local"> Impostazioni report </a> e Metodologia di conteggio <a href="/help/main/c-reports/statistical-methodology/statistical-calculations.md" format="dita" scope="local"> </a>. </p> <p>I seguenti miglioramenti di generazione rapporti sono ora disponibili per i rapporti CSV scaricabili: </p> <p> 
     <ul id="ul_18B0636A41B94F9F903ABFE3E13285DA"> 
      <li id="li_2422075AA0A34F868809C5D580FC5D4B"> <p>Il rapporto CSV a livello di offerta dispone ora di ulteriori dettagli riguardanti ogni offerta. (TGT-18995) </p> </li> 
      <li id="li_659D126E846348D4BE4544962F41539F"> <p>Ora i file CSV scaricati a livello di offerta includono sempre i dati dei segmenti di controllo e di destinazione per i rapporti di <span class="wintitle">Automated Personalization</span>. (TGT-22000) </p> </li> 
     </ul> </p> <p>Sono ora disponibili i seguenti miglioramenti riguardanti la generazione rapporti per la sezione Automated Personalization (AP). </p> <p> 
     <ul id="ul_5743684487CD4905BA998C298FD423D7"> 
      <li id="li_EB48BA21E00C4878B4408D24DD23BA9C"> <p>È stato migliorato il tempo di caricamento della generazione rapporti per le attività di Automated Personalization. </p> </li> 
      <li id="li_B8ECCE250A674B83A66705AD5C45B9C3"> <p>L'intervallo di affidabilità per le variabili continue (metrica di Ricavi e di Coinvolgimento) viene ora visualizzato nei rapporti di riepilogo di Automated Personalization (AP). </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Attività </p> </td> 
   <td colname="col2"> <p>I miglioramenti seguenti sono ora disponibili per le attività di Target: </p> <p> 
     <ul id="ul_436556860E6C4AEEB35411A02E78A199"> 
      <li id="li_5CC3B995D0AF4B658B3D6C3F6895AA41"> <p>Le attività create in <span class="keyword">Adobe Mobile Services</span> vengono ora visualizzate all'interno dell'interfaccia utente di <span class="keyword">Target Standard/Premium</span>. (TGT-10806) </p> <p>Per ulteriori informazioni, vedere <a href="/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> attività </a>. </p> </li> 
      <li id="li_684F9FC5CF414F4A892E6495352B5939"> <p>Quando si creano test multivariati, è ora possibile escludere più del 10% di esperienze dal test; in questo caso, per effettuare l’analisi è necessario utilizzare la generazione rapporti non in linea. (TGT-21719) </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/preview-experiences.md#task_21A700587E88453A9FC2210C0DE53A28" format="dita" scope="local">Esperienze di anteprima per un test multivariato</a>. </p> </li> 
      <li id="li_B2FC7414C76848B39AD6EA20EE483F06"> <p>L'ID della campagna è ora visibile nella pagina Panoramica di ogni attività. Questa funzione è utile per le operazioni API e di risoluzione dei problemi. (TGT-20928) </p> </li> 
      <li id="li_5A9880AFE5FB46168D92255AA088B854"> <p>La progettazione delle pagine Conflitti e Registro modifiche è stata migliorata. </p> </li> 
      <li id="li_1489EA6C30C94B2AB394189E5FAFF6F6"> <p>La lunghezza massima consentita per i nomi di offerta anonimi nelle attività di Automated Personalization (AP) è stata aumentata da 30 a 250 caratteri. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tipi di pubblico </p> </td> 
   <td colname="col2"> <p>I seguenti miglioramenti sono ora disponibili per il pubblico: </p> <p> 
     <ul id="ul_F1D1F97266134D4ABE627CF2DCE2C6D4"> 
      <li id="li_99A611FCC1254D229D79B8FD075B952A"> <p> Durante la creazione di destinatari di dispositivi mobili, nell’elenco a discesa ora è disponibile l'opzione incorporata <span class="wintitle">Nome dispositivo di marketing</span>. </p> <p>Questa modifica consente di scegliere facilmente un nome di modello di dispositivo anziché cercare il numero del modello di dispositivo appropriato. Ad esempio, il nome di marketing del dispositivo Galaxy S7 è “Samsung Galaxy S7 Edge”, mentre il modello del dispositivo è “SM-G9350”. (TGT-18393) </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-target/c-audiences/c-target-rules/mobile.md#concept_2A794199DC1A4D349FFFBC7DCF1FEB89" format="dita" scope="local">Mobile</a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Consigli </p> </td> 
   <td colname="col2"> <p>I seguenti miglioramenti sono stati apportati alla funzione Recommendations: </p> <p> 
     <ul id="ul_9D3644890C0C472D8B485DE9A52898B3"> 
      <li id="li_1E5662348F6E4ABDB2B74FE3326F2FD3"> <p>La linea di risultati dell'Algoritmo di backup è ora inclusa nei file CSV scaricabili Più visualizzati e Più acquistati. Il consiglio di backup inizia con “*,” </p> </li> 
      <li id="li_91DFD809378D4C20918F8F875747CE07"> <p>Gli stati aggiuntivi ti permettono di conoscere il progresso del feed dei consigli. </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-recommendations/c-products/feeds.md#concept_1228B31E3D0B483B9DD42C5E2AE436E3" format="dita" scope="local">Feed</a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Compositore esperienza visivo avanzato </p> </td> 
   <td colname="col2"> <p>Aggiornamento degli indirizzi IP per il Compositore esperienza visivo avanzato. </p> <p>Se inserisci nell’elenco Consentiti gli indirizzi IP utilizzati per il Compositore esperienza visivo, aggiungi i nuovi indirizzi IP. </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md#reference_77743144F10143A3A89D56E116D296E4" format="dita" scope="local">Risoluzione dei problemi relativi a Compositore esperienza visivo.</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Versione 2016 {#reference_607661929B504CCFAB3791B13C0DCDBE}

### Target Standard/Premium 16.10.2 (8 novembre 2016) {#section_2FDEFB3D56CC4BD7BC04DBEECFF6E942}

**Problemi risolti**

Questa versione include le seguenti correzioni:

* Risolto un problema in [!DNL Recommendations] che rendeva impossibile la creazione di feed per ambienti non predefiniti (gruppi di host).
* Sono state apportate diverse migliorie per ridurre gli errori di sincronizzazione delle attività.
* Non è più possibile creare offerte di reindirizzamento per attività che utilizzano [!DNL Analytics for Target] (A4T).

### Target Standard/Premium 16.10.1 (25 ottobre 2016) {#section_F76F7329FCAC452FB88F8BE0BA727044}

Questa versione include i miglioramenti e le funzioni seguenti:

<table id="table_F8C01B2A9F07443490DB3025AC3AAC2A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Allocazione automatica: contrassegno per l'esperienza migliore </td> 
   <td colname="col2"> <p>Ora è più facile individuare l'esperienza migliore in un'attività di allocazione automatica A/B. </p> <p>Molti addetti al marketing commettono l’errore di dichiarare un’esperienza vincente prima che i risultati indichino chiaramente quale sia l’esperienza migliore. </p> <p>Quando si utilizza la funzionalità <span class="wintitle">Allocazione automatica del traffico</span>, nella parte superiore della pagina di <span class="keyword">Target</span> dedicata alle attività appare un contrassegno che indica “Ancora nessun vincitore” finché l'attività non raggiunge il numero minimo di conversioni con sufficiente sicurezza. Quando viene dichiarata l'esperienza migliore, in <span class="keyword">Target</span> appare la scritta “Vincitore: esperienza X”. </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4" format="dita" scope="local">Allocazione traffico automatica</a> e <a href="/help/main/c-activities/automated-traffic-allocation/determine-winner.md#concept_5741A89ED7224E1285A3BC34B2CCD0F9" format="dita" scope="local">Determinare un vincitore</a>. </p> <p> <p>Nota: da oggi, le attività di allocazione automatica A/B non sono più supportate in Analytics for Target (A4T). A partire da questa versione, tutte le attività di allocazione automatica A/B con A4T abilitato saranno commutate in modalità <span class="wintitle">Manuale</span> (allocazione del traffico in parti uguali). </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Individuare dispositivi mobili tramite gestore di telefonia </td> 
   <td colname="col2"> <p>Crea un pubblico per i dispositivi mobili sulla base del gestore di telefonia (Verizon, Sprint, AT&amp;T, T-Mobile ecc.). L'opzione <span class="wintitle">Gestore</span> è tra le impostazioni <span class="wintitle">Geo</span>. </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-target/c-audiences/c-target-rules/geo.md#concept_5B4D99DE685348FB877929EE0F942670" format="dita" scope="local">Geo</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Generare token di autenticazione mboxTrace dall'interfaccia utente di Target </td> 
   <td colname="col2"> <p>Abilita gli strumenti avanzati di debug di <span class="keyword">Target</span> creando un token di autenticazione temporaneo. </p> <p>Fai clic su <span class="uicontrol">Genera token di autenticazione</span> nella pagina <span class="wintitle">Dettagli implementazione</span> (<span class="uicontrol">Amministrazione</span> &gt; <span class="uicontrol">Implementazione</span>). Potrai aggiungere il parametro risultante agli URL della pagina web per scopi di risoluzione dei problemi. </p> <p>Per ulteriori informazioni, vedere "Recuperare il token di autorizzazione da utilizzare con gli strumenti di debug" in <a href="/help/main/c-activities/c-troubleshooting-activities/content-trouble.md#concept_D2548B486C984B1E97ED7A72075B8EEA" format="dita" scope="local"> Risoluzione dei problemi relativi alla distribuzione dei contenuti </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Consigli: sequenziazione di un insieme di criteri </td> 
   <td colname="col2"> <p>Utilizza set composti da un numero massimo di cinque criteri creati in precedenza in una singola esperienza per un maggiore controllo sui consigli presentati ai visitatori. </p> <p>Per ulteriori informazioni, vedere <a href="/help/main/c-recommendations/c-algorithms/create-criteria-sequence.md"> Creare sequenze di criteri </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Consigli: inserimento di promozioni esterne </td> 
   <td colname="col2"> <p>Aggiungi articoli in promozione e controllane il posizionamento nelle progettazioni dei consigli. </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md#task_CC5BD28C364742218C1ACAF0D45E0E14" format="dita" scope="local">Aggiunta di promozioni</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="firstlook"> <p><b>First Look</b> </p> Targeting automatico nelle attività A/B </td> 
   <td colname="col2"> <p> <p>Nota: l'offerta “First Look” è abilitata soltanto per alcuni clienti di questa versione per effettuare test e fornire riscontri. </p> </p> <p>Indirizza automaticamente le esperienze negli A/B test per fornire ad ogni visitatore l'esperienza più adatta. </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-activities/auto-target/auto-target-to-optimize.md" format="dita" scope="local">Targeting automatico per esperienze personalizzate</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Modifiche alla piattaforma Target (10 ottobre 2016) {#section_0761AED70C3E44EA9D8546107B162CC1}

<table id="table_E3E52A4362724D05A8472DB5F51A2429"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Modifica </th> 
   <th colname="col2" class="entry"> Dettagli </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> at.js</span> versione 0.9.3 </p> </td> 
   <td colname="col2"> <p>10 ottobre 2016 </p> <p> È ora disponibile la versione 0.9.3 di <span class="codeph">at.js</span>. </p> <p> 
     <ul id="ul_E4D300700390433E9EF8D5C9D3AA7669"> 
      <li id="li_E916EB3A77ED4CFF90CF6B4D30F188B1"> <p>Le chiamate mbox si attivano in Microsoft Internet Explorer 11 quando i browser legacy sono disabilitati nelle impostazioni <span class="codeph">at.js</span>. </p> </li> 
      <li id="li_1130509832CE429DB6DE636404CC54E1"> <p>Il contenuto predefinito viene renderizzato in caso di mancata riuscita di un’offerta remota dinamica (ad esempio, se l’URL non è corretto e genera un errore 404). </p> </li> 
      <li id="li_21B5225D894B43CB863A775C937F66F4"> <p>Garantisce che gli elementi vengano rivelati rapidamente quando è impossibile trovare i selettori di tracciamento clic del Compositore esperienza visivo nel DOM. </p> </li> 
     </ul> </p> <p>Per ulteriori informazioni, consulta <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it" format="dita" scope="local">Dettagli della versione di at.js</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 16.9.1 (22 settembre 2016) {#section_3CD20678B6254DE1A9BD41FDD2255DDD}

Questa versione include i miglioramenti e le funzioni seguenti:

<table id="table_FED049F97C054CA895E0AEA3F2B180BF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Combinare più tipi di pubblico </td> 
   <td colname="col2"> <p>Combina al volo più tipi di pubblico (tra cui quelli di <span class="keyword">Adobe Experience Cloud</span> e di <span class="keyword">Target</span>) durante il flusso di lavoro per la creazione di attività. </p> <p>Ad esempio, puoi indirizzare tutti i clienti fidelizzati includendo un segmento di <span class="keyword">Audience Manager</span> specifico per lo status di fidelizzazione e combinarlo con un segmento di <span class="keyword">Target</span> composto da persone iscritte al tuo programma fedeltà nella sessione corrente, invece di creare un terzo pubblico permanente. </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5" format="dita" scope="local">Combinazione di più tipi di pubblico</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Targeting dei visitatori durante un periodo di tempo specifico </td> 
   <td colname="col2"> <p>Aggiungi la data di inizio e fine del periodo per indirizzare un pubblico. </p> <p>Per esempio, utilizzando i nuovi tipi di pubblico combinati ad hoc di cui sopra, è possibile indirizzare gli utenti che spendono meno su contenuti specifici nei tre giorni prima del Black Friday e su altri contenuti dopo il Black Friday. </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-target/c-audiences/c-target-rules/time-frame.md#concept_0FE1E8DACD104F8B870B0BADE3197F0A" format="dita" scope="local"> Arco temporale </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Salvare raccolte avanzate </td> 
   <td colname="col2"> <p>La funzionalità di ricerca nella pagina <span class="wintitle">Contenuto</span> comprende ora cartelle salvate, denominate raccolte avanzate, per risparmiare tempo quando si eseguono ricerche simili. </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-experiences/c-manage-content/filter-and-search-content.md#concept_3B59B8F025BF4CEA82ECC5199D365276" format="dita" scope="local">Ricerca contenuti e crea raccolte avanzate</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Compositore esperienza basato su moduli </td> 
   <td colname="col2"> <p>Aggiungi un collegamento a un'immagine. Il collegamento può essere di tipo click-through, di destinazione o di arrivo. </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local">Compositore esperienza basato su moduli</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Miglioramenti**

Questa versione include i seguenti miglioramenti:

| Miglioramento | Descrizione |
|---|---|
| Compositore esperienza visivo | È stata migliorata la messaggistica di errore. |

**Problemi noti**

* L&#39;opzione [!UICONTROL Render Using JavaScript] non è attualmente supportata se viene utilizzata insieme al codice personalizzato nel Compositore esperienza visivo.

### Modifiche alla piattaforma Target (settembre 2016) {#section_1955146045A247D393DB824669A2A916}

<table id="table_8FDAEED5D84C4C718AB863BD6C383F20"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Modifica </th> 
   <th colname="col2" class="entry"> Dettagli </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> at.js</span> versione 0.9.2 </p> </td> 
   <td colname="col2"> <p>21 settembre 2016 </p> <p> È ora disponibile la versione 0.9.2 di <span class="codeph">at.js</span>. </p> <p> 
     <ul id="ul_0778A9049C9D48A7B6CB4B79A95F0F4C"> 
      <li id="li_689FF306179F4EC3B391DEE3C53F4B1D"> <p>È stata aggiunta un’impostazione <span class="codeph">optoutEnabled</span> per abilitare o disabilitare la rinuncia a Device Graph. Se questa impostazione è impostata su <span class="codeph">Vero</span> e il visitatore ha scelto di non aderire al tracciamento, il browser del visitatore non farà nessuna chiamata mbox. Device Graph è attualmente in versione beta. Questa impostazione è inizialmente impostata su <span class="codeph">Falso</span>, ma deve essere impostata su <span class="codeph">Vero</span> se si utilizza Device Graph.</p> </li> 
      <li id="li_663462C0680049F89CA8FE1853F31807"> <p>È stato aggiunto il supporto di <span class="codeph">CustomEvent</span> per il meccanismo di notifica. In precedenza, il meccanismo di notifica degli eventi <span class="codeph">at.js</span> non poteva essere utilizzato tramite API DOM standard, come ad esempio <span class="codeph">document.addEventListener()</span>. Ora è possibile utilizzare <span class="codeph">document.addEventListener()</span> per sottoscrivere a eventi <span class="codeph">at.js</span>, come ad esempio eventi di richiesta e di rendering del contenuto. </p> </li> 
      <li id="li_3FB2914F8D2F4AFFAA9B4622E8CA1EFF"> <p>È stato risolto un problema relativo alle offerte create nel Compositore esperienza visivo. Prima di questa versione, Target nascondeva i selettori e li mostrava solo in caso di corrispondenza di tutti i selettori. In <span class="codeph">at.js</span> 0.9.2 Target mostra i selettori non appena corrispondono. </p> </li> 
     </ul> </p> <p>Per ulteriori informazioni, consulta <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it" format="dita" scope="local">Dettagli della versione di at.js</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 16.9.1 (22 settembre 2016) {#section_60ADF842E4A0424E8D2A81FB8B813A7A}

Questa versione include i miglioramenti e le funzioni seguenti:

<table id="table_896218AECE4C4EC691B76E79CC7DC356"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Combinare più tipi di pubblico </td> 
   <td colname="col2"> <p>Combina al volo più tipi di pubblico (tra cui quelli di <span class="keyword">Adobe Experience Cloud</span> e di <span class="keyword">Target</span>) durante il flusso di lavoro per la creazione di attività. </p> <p>Ad esempio, puoi indirizzare tutti i clienti fidelizzati includendo un segmento di <span class="keyword">Audience Manager</span> specifico per lo status di fidelizzazione e combinarlo con un segmento di <span class="keyword">Target</span> composto da persone iscritte al tuo programma fedeltà nella sessione corrente, invece di creare un terzo pubblico permanente. </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5" format="dita" scope="local">Combinazione di più tipi di pubblico</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Targeting dei visitatori durante un periodo di tempo specifico </td> 
   <td colname="col2"> <p>Aggiungi la data di inizio e fine del periodo per indirizzare un pubblico. </p> <p>Per esempio, utilizzando i nuovi tipi di pubblico combinati ad hoc di cui sopra, è possibile indirizzare gli utenti che spendono meno su contenuti specifici nei tre giorni prima del Black Friday e su altri contenuti dopo il Black Friday. </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-target/c-audiences/c-target-rules/time-frame.md#concept_0FE1E8DACD104F8B870B0BADE3197F0A" format="dita" scope="local"> Arco temporale </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Salvare raccolte avanzate </td> 
   <td colname="col2"> <p>La funzionalità di ricerca nella pagina <span class="wintitle">Contenuto</span> comprende ora cartelle salvate, denominate raccolte avanzate, per risparmiare tempo quando si eseguono ricerche simili. </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-experiences/c-manage-content/filter-and-search-content.md#concept_3B59B8F025BF4CEA82ECC5199D365276" format="dita" scope="local">Ricerca contenuti e crea raccolte avanzate</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Compositore esperienza basato su moduli </td> 
   <td colname="col2"> <p>Aggiungi un collegamento a un'immagine. Il collegamento può essere di tipo click-through, di destinazione o di arrivo. </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local">Compositore esperienza basato su moduli</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Miglioramenti**

Questa versione include i seguenti miglioramenti:

| Miglioramento | Descrizione |
|---|---|
| Compositore esperienza visivo | È stata migliorata la messaggistica di errore. |

**Problemi noti**

* L&#39;opzione [!UICONTROL Render Using JavaScript] non è attualmente supportata se viene utilizzata insieme al codice personalizzato nel Compositore esperienza visivo.

### Adobe [!DNL Target] Standard/Premium 16.8.1 (23 agosto 2016) {#section_A8854D4EDF014AEBB81F49EB104D4A20}

La versione 16.8.1 di Adobe Target Standard/Premium (23 agosto 2016) prevede le seguenti funzionalità e migliorie:

<table id="table_AE048CB9EA1C4C7BBC2E9D90D26F7395"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Gestione di host e ambiente (gruppo host) </p> </td> 
   <td colname="col2"> <p>Organizza siti e ambienti di preproduzione per gestirli facilmente e per generare rapporti separati. </p> <p>Per facilitare la gestione, gli host sono raccolti in ambienti. Gli ambienti preimpostati includono Produzione, Staging e Sviluppo. È inoltre possibile aggiungere nuovi ambienti. </p> <p>Questa funzionalità è pari a quella di <span class="keyword">Target Classic</span>. </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/administrating-target/hosts.md#concept_516BB01EBFBD4449AB03940D31AEB66E" format="dita" scope="local">Host</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Affinità tra categorie </p> </td> 
   <td colname="col2"> <p>La funzione di affinità tra categorie acquisisce automaticamente le categorie visitate da un utente e calcola l'affinità dell'utente con la categoria in modo che possa essere indirizzata e segmentata. Questo è utile per assicurare che il targeting del contenuto sia rivolto ai visitatori per i quali la probabilità di azione su tali informazioni è più elevata. </p> <p>Questa funzionalità è pari a quella di <span class="keyword">Target Classic</span>. </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-target/c-visitor-profile/category-affinity.md#concept_75EC1E1123014448B8B92AD16B2D72CC" format="dita" scope="local">Affinità tra categorie</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Attivare/disattivare il Compositore esperienza avanzato a livello di attività </p> </td> 
   <td colname="col2"> <p>Attiva/disattiva il <span class="wintitle">Compositore esperienza avanzato</span> a livello di account (si applica a tutte le attività create nell'account) o a livello di singola attività. </p> <p>Prima, era possibile abilitare/disabilitare il Compositore esperienza avanzato solo a livello di account. </p> <p>Per ulteriori informazioni, vedere <a href="/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D" format="dita" scope="local"> esperienze </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="premium">Automated Personalization: rapporti sulle prestazioni dell’offerta </p> </td> 
   <td colname="col2"> <p>Scarica un rapporto sulle prestazioni dell’offerta con tutte le metriche di successo dell’attività di Automated Personalization. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Miglioramenti**

Questa versione include i seguenti miglioramenti:

<table id="table_E2E4BE72BD79413A821C6A6D1A3AB0F8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Miglioramento </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Rinnovamento dell'interfaccia utente dell'editor di codice </p> </td> 
   <td colname="col2"> <p>L'interfaccia utente dell'editor di codice è stata resa più intuitiva e più facile da utilizzare. </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md#concept_B3A6E9EE3A60406DB640E205EA1745B5" format="dita" scope="local">Editor di codice</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Sono stati segnalati i seguenti problemi:

* Parte del testo dell&#39;interfaccia utente per la funzionalità [!UICONTROL Category Affinity] viene visualizzato solo in inglese. Il testo in altre lingue sarà disponibile nella versione di [!DNL Target] di settembre.

### Modifiche alla piattaforma Target (luglio 2016) {#section_09C18773707B4059852A41C764F817E4}

<table id="table_33B60910EAE24BAFA778F280F72FB683"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Modifica </th> 
   <th colname="col2" class="entry"> Dettagli </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> at.js</span> versione 0.9.1 </p> </td> 
   <td colname="col2"> <p>14 luglio 2016 </p> <p> È ora disponibile la versione 0.9.1 di <span class="filepath">at.js</span>. </p> <p>Per ulteriori informazioni, consulta <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it" format="dita" scope="local">Dettagli della versione di at.js</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Adobe [!DNL Target] Standard/Premium 16.7.1 (21 luglio 2016) {#section_DB583EF9A30247A488EE319583911F22}

La versione 16.7.1 di Adobe Target Standard/Premium (21 luglio 2016) prevede le seguenti funzionalità e migliorie:

<table id="table_EBA34BD2F5C745DD9EC5231AD79F6C00"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Impostazioni prioritarie per le attività </td> 
   <td colname="col2"> <p>È ora possibile impostare livelli di priorità da 0 a 999 per le attività. Questo permette un controllo più preciso sull'attività da visualizzare quando vengono assegnate più attività allo stesso percorso con lo stesso pubblico. </p> <p>Questa opzione deve essere attivata in <span class="wintitle">Amministrazione</span> &gt; <span class="wintitle">Generazione rapporti</span>. </p> <p>L'opzione Priorità a grana fine si applica alle attività di Test A/B, Automated Personalization, Targeting esperienza e Test multivariati. </p> <p>Per maggiori informazioni, vedi i seguenti argomenti: </p> <p> 
     <ul id="ul_FD92CD06CF25480887AC171274262E18"> 
      <li id="li_D321FAED82944D2685DA69EB310D80BE"><b>Test A/B: </b> <a href="/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC" format="dita" scope="local">obiettivi e impostazioni</a> </li> 
      <li id="li_12ECDFD71DB94E22A85AB13B487E8503"><b>Automated Personalization: </b> <a href="/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local">Automated Personalization</a> </li> 
      <li id="li_84B893C214994246AB36E28E84C51460"><b>Targeting esperienza: </b> <a href="/help/main/c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC" format="dita" scope="local">Obiettivi e impostazioni</a> </li> 
      <li id="li_26533B659C0E49D6A6D3B3FEBE9CA930"><b>Test multivariato: </b> <a href="/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC" format="dita" scope="local">Obiettivi e impostazioni</a> </li> 
      <li id="li_FBACF2B73B2E491BBB85618153AC4568"><b>Attività: </b> <a href="/help/main/c-activities/activity-settings.md#task_C6B2FF8374724933BE79A83549B9CD02" format="dita" scope="local">Impostazioni attività</a> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Attributi per Consigli con più valori </td> 
   <td colname="col2"> <p>Da oggi, tutti gli attributi personalizzati della funzione <span class="keyword">Consigli</span> possono contenere più valori entità. </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-recommendations/c-products/custom-entity-attributes.md#concept_E5CF39BCAC8140309A73828706288322" format="dita" scope="local">Attributi di entità personalizzati</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Supporto di offerte dinamiche/remote </td> 
   <td colname="col2"> <p>In <span class="keyword">Target Standard/Premium</span>, il contenuto dinamico può far parte di qualsiasi attività basata su moduli. Il contenuto dinamico viene archiviato all'esterno di <span class="keyword">Target </span>. </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-experiences/c-manage-content/about-remote-offers.md#concept_657016A0E6174C22B89036E9C8A0170F" format="dita" scope="local">Creare offerte remote</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Copiare tipi di pubblico e script di profilo </td> 
   <td colname="col2"> <p>Da oggi, si può copiare un pubblico esistente e modificarlo per crearne uno simile. </p> <p>Per ulteriori informazioni, vedere <a href="/help/main/c-target/c-audiences/create-audience.md#task_E18BD77A9A8F4ED0AC50569F94556558" format="dita" scope="local"> Creazione di un pubblico </a>. </p> <p>È inoltre possibile copiare gli script dei profili esistenti. </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-target/c-visitor-profile/profile-parameters.md#concept_8C07AEAB0A144FECA8B4FEB091AED4D2" format="dita" scope="local">Attributi del profilo</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Utilizza le classi per determinare i selettori di elementi </td> 
   <td colname="col2"> <p>Da oggi, i selettori di elementi si possono basare su classi o ID nelle attività di Automated Personalization e Test multivariato. Nelle versioni precedenti, questa opzione era disponibile solo per le attività di Prova A/B. </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-experiences/c-visual-experience-composer/vec-selectors.md#concept_4EB7663E255F439B8D24079D23479337" format="dita" scope="local">Selettori di elementi utilizzati nel Compositore esperienza visivo.</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Consigli: Somiglianza del contenuto </td> 
   <td colname="col2"> <p> Utilizza le regole di somiglianza del contenuto per formulare consigli basati su attributi di elemento o file multimediale. </p> </td> 
  </tr> 
 </tbody> 
</table>

<table id="table_699755B33F8F48ECABB6FC7E78289A79"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Miglioramento </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Miglioramenti della reportistica </p> </td> 
   <td colname="col2"> <p>Da oggi, sui rapporti della metrica di successo che vengono scaricati, compaiono i nomi dei segmenti e delle metriche anziché i loro ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Valutare la condizione di entrata mbox su ogni richiesta nelle attività di Automated Personalization </td> 
   <td colname="col2"> <p>Nelle attività di Automated Personalization, i criteri di immissione (targeting URL, regole di modello, targeting pubblico) vengono valutati per ogni richiesta per una distribuzione più accurata dell’offerta. </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local">Automated Personalization</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Adobe [!DNL Target] Standard/Premium 16.6.1 (16 giugno 2016) {#section_C1E9F43111BF4160AF31482CD53E00BD}

Non sono previste versioni rivolte ai clienti per giugno.

**Problemi risolti**

Questa versione include le seguenti correzioni:

* È stato risolto un problema a causa del quale ad alcuni clienti appariva una schermata bianca quando tentavano di modificare la loro pagina all&#39;interno del Compositore esperienza visivo.

**Problemi noti**

Sono stati segnalati i seguenti problemi:

* Quando si seleziona “Disabilita JavaScript” per la pagina A in un&#39;attività multipagina, JavaScript viene disabilitato ovunque, anche se “Disabilita JavaScript” non viene selezionato in altre pagine.
* Problema con gli URL di anteprima delle esperienze con reindirizzamento. Come soluzione alternativa, nel Compositore esperienza, fai clic su **[!UICONTROL Configure]**, scegli **[!UICONTROL Multiple Audiences]** e aggiungi **[!UICONTROL All visitors]** come unico pubblico. Continua a salvare l&#39;attività. Questo non cambia la distribuzione dell&#39;attività, ma consente il funzionamento dell&#39;anteprima. Questo problema verrà risolto nella versione di luglio di Adobe Target.

* Nella documentazione viene illustrato il comportamento previsto per la casella di controllo Reindirizza URL. Tuttavia, a causa di un bug, la casella di controllo non appare selezionata come impostazione predefinita. Questo difetto verrà corretto al più presto.

  Per verificare questa opzione in un&#39;attività esistente con un&#39;offerta di reindirizzamento, adotta la seguente soluzione:

   1. Apri il popup per il reindirizzamento a un URL.
   1. Modifica l&#39;URL sostituendolo con uno fittizio e salva.
   1. Modifica nuovamente l&#39;URL fittizio sostituendolo con l&#39;URL di reindirizzamento previsto dalla tua campagna.
   1. Seleziona l&#39;opzione “Includi parametri di query correnti” e salva.

  Se si seleziona l&#39;opzione durante la creazione di una nuova offerta di reindirizzamento, i parametri di query verranno probabilmente inclusi nel reindirizzamento.

  Per le attività create in precedenza, se questa opzione è selezionata nel compositore esperienza dell&#39;attività, il reindirizzamento includerà i parametri della query. Se non è selezionata, i parametri di query correnti non verranno inclusi nel reindirizzamento.

### Adobe [!DNL Target] Standard/Premium 16.5.1 (19 maggio 2016) {#section_406CE09317994F55A26C2FDB77C77FEA}

La versione 16.5.1 di Adobe Target Standard/Premium (19 maggio 2016) prevede le seguenti funzionalità e migliorie:

<table id="table_DDC5356FD6B8443EAA6EB81C03ADF73A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Versioni di esperienza </td> 
   <td colname="col2"> <p>Le versioni destinate a diversi gruppi possono ora essere configurate all'interno di esperienze nelle attività A/B. </p> <p>Vedi <a href="/help/main/c-activities/t-test-ab/t-test-create-ab/target-experience-to-multiple-audiences.md#task_0138112E283A4A5B9F8AB9AAF2FBC2FF" format="dita" scope="local"> Eseguire il targeting di un'esperienza per più tipi di pubblico </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Algoritmi personalizzati per i consigli </td> 
   <td colname="col2"> <p>Le mappature degli algoritmi personalizzati possono essere caricati in un file CSV. Non è più necessario utilizzare l'API basata su XML. </p> <p>Consulta <a href="/help/main/c-recommendations/c-algorithms/recommendations-csv.md#task_1BBA49883E794670A09F0ABE1B3F4288" format="dita" scope="local">Caricamento di criteri personalizzati.</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Analytics for Target: server di tracciamento Analytics </td> 
   <td colname="col2"> <p>Per garantire un corretto monitoraggio della reportistica, è necessario specificare un server di tracciamento quando si creano o modificano attività che utilizzano Analytics for Target (A4T). L'esecuzione delle attività esistenti continuerà secondo le impostazioni attuali. </p> <p>Consulta <a href="/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823" format="dita" scope="local">Utilizzo di un server di tracciamento di Analytics.</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Nuovi video didattici </td> 
   <td colname="col2"> <p>Per aiutarti, sono stati aggiunti i seguenti video didattici: </p> <p> 
     <ul id="ul_47BAE946E764404497B7D81EE4C5D076"> 
      <li id="li_E16E50F94D3748E2985FB78F75140626">Utilizzo di DTM per passare i parametri alla mbox globale </li> 
      <li id="li_A8CCDE3EFF25430580E6C372000CF964">Utilizzo di DTM per distribuire Target </li> 
      <li id="li_8897F7B5930B448D87274CEDFCC75AE4">Configurazione di un test multivariato </li> 
      <li id="li_2573DF52CE974ED0AF9EA433C97BC4C0">Creazione di un'attività A/B </li> 
      <li id="li_52F28040D54D43E787B763E6AA998614">Informazioni sui tipi di attività </li> 
      <li id="li_577C8DDEB4CE429CA3C14BE5655F6E11">Configurazione delle impostazioni di attività </li> 
      <li id="li_2F7FCA657FD04E02ADD6E6964A8EA1F0">Targeting di un'attività </li> 
      <li id="li_A08B8AFF48764D1B9EA706977F72AA66">Creazione di un pubblico </li> 
      <li id="li_493CDC3BEA5F4EA0821B971579177E03">Utilizzo del pubblico </li> 
      <li id="li_19045C86E1524649B56F82416934EF13">Utilizzo della Libreria di contenuti </li> 
      <li id="li_8E89F3691A6F4400A2DFDFE5186DFA83">Utilizzo degli script di profilo </li> 
      <li id="li_2EBB2B61BFA24F5FB858C0551AB20F70">Impostazione delle preferenze dell'account </li> 
      <li id="li_E1886818C7BF4F36B07EC293F1A45911">Informazioni sulle modalità del Compositore esperienza visivo </li>  
      <li id="li_A87B876298344B2987BDC5FFD5580EC0">Creazione e gestione degli utenti di Target </li> 
      <li id="li_F90E1083444E4DBAA8C406AC293C0FD6">Impostazione delle metriche di successo </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Miglioramenti dell'interfaccia utente </td> 
   <td colname="col2"> <p>È stata migliorata l’interfaccia utente per la ricerca nei consigli e il Compositore esperienza visivo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> File CSV scaricabile di Consigli </td> 
   <td colname="col2"> <p>I file CSV scaricabili dispongono ora di una riga per tutti gli ambienti, inclusi quelli che non hanno consigli sulle entità (ad esempio: 
     <code>
       &#x200B;# environment: 1724 
     </code>). </p> </td> 
  </tr> 
 </tbody> 
</table>

**Miglioramenti**

Miglioramento al processo di provisioning di A4T.

**Problemi noti**

Sono stati segnalati i seguenti problemi:

* Quando si seleziona “Disabilita JavaScript” per la pagina A in un&#39;attività multipagina, JavaScript viene disabilitato ovunque, anche se “Disabilita JavaScript” non viene selezionato in altre pagine.
* Problema con gli URL di anteprima delle esperienze con reindirizzamento. Come soluzione alternativa, nel Compositore esperienza, fai clic su **[!UICONTROL Configure]**, scegli **[!UICONTROL Multiple Audiences]** e aggiungi **[!UICONTROL All visitors]** come unico pubblico. Continua a salvare l&#39;attività. Questo non cambia la distribuzione dell&#39;attività, ma consente il funzionamento dell&#39;anteprima. Questo problema verrà risolto nella versione di luglio di Adobe Target.

### Nuova libreria di implementazione di [!DNL Target], at.js 0.8.0 (5 maggio 2016) {#section_6A44C277E82D409AB6DCD0901F43794A}

at.js è una nuova libreria di implementazione per Target, progettata sia per le tipiche implementazioni web sia per le applicazioni a pagina singola.

Ad esempio, at.js migliora i tempi di caricamento delle pagine per le implementazioni web, migliora la sicurezza e fornisce migliori opzioni di implementazione per le applicazioni a pagina singola.

La libreria at.js include anche i componenti inclusi in target.js, quindi cessano le chiamate a target.js.

Quando implementi at.js, tieni presente quanto segue:

* I reindirizzamenti del Compositore esperienza visivo non funzionano.
* Le versioni di Internet Explorer precedenti a 8 non sono supportate.
* L’implementazione asincrona potrebbe impedire il funzionamento delle integrazioni legacy come il plug-in Test&amp;Target a SiteCatalyst.
* Tutte le chiamate a Target vengono effettuate tramite XMLHTTPRequest e il contenuto viene restituito tramite JSON.

### Adobe [!DNL Target] Standard/Premium 16.4.1 Fix (5 maggio 2016) {#section_70552F61E83140C7B4D2A245198B630E}

* Da oggi, è possibile scaricare la versione 0.8.0 di at.js dall&#39;interfaccia di Target.
* Le API di Target sono state modificate. `applyOffer` ora richiede `mbox param [0]`.

  ```
  adobe.target.applyOffer({ 
      "mbox": "target-global-mbox", 
   "params": {"test": "true"}, 
      "selector": ".banner-text", 
      "offer": offer 
  });
  ```

### Adobe [!DNL Target] Standard/Premium 16.4.1 (21 aprile 2016) {#section_C968860FAB81485BA12BD588F4ECA401}

Questa versione include i miglioramenti e le funzioni seguenti:

<table id="table_162CC5A0DB324B38A8A4252A18976686"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Miglioramenti dell'interfaccia utente </td> 
   <td colname="col2"> <p>L'interfaccia utente è cambiata notevolmente in questa versione. Alcuni dei cambiamenti più evidenti: </p> <p> 
     <ul id="ul_28F382C60ADE43F5A3A4BD0CD5A5CE52"> 
      <li id="li_C47240826E5844D6843314F453F042FC">La navigazione, precedentemente a sinistra, è stata spostata in alto </li> 
      <li id="li_3BB03504E98C40CC85583DCD9A4CEA06">Finestre di dialogo migliorate </li> 
      <li id="li_AE71506DF1E748A788C40E1F09951732">Flusso di creazione delle attività migliorato </li> 
     </ul> </p> <p>Inoltre, è stata modificata la modalità di selezione delle soluzioni Adobe Experience Cloud, tra cui quella di Target. Per accedere alle soluzioni e ai servizi Experience Cloud, fai clic sull’icona del menu: </p> <p> <img src="assets/menu-shell-400.png" id="image_6E9323E0EBEA41B1A7319D6BCC43E769" width="400" height="140" /> </p> <p>Per ulteriori informazioni sull'accesso a Target e sull'impostazione di Target come pagina predefinita dopo l'accesso a Experience Cloud, vedere <a href="/help/main/c-intro/target-access-from-mac.md#task_5467C72DAFCB4BB583762CAAFC00A5CF" format="dita" scope="local"> Accedere a Target da Adobe Experience Cloud </a>. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Le regole di inclusione possono essere disabilitate per i suggerimenti di backup </td> 
   <td colname="col2"> <p>Quando i suggerimenti di backup sono abilitati, si può scegliere di non applicare le regole di inclusione ai suggerimenti di backup. </p>  </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Consigli: nuove funzionalità di debug nell’area di testo tramite <span class="codeph">mboxTrace </span> </td> 
   <td colname="col2"> <p>L'aggiunta di <span class="codeph">&amp;mboxTrace</span> a un URL sostituisce, in tale pagina, i consigli con i dettagli di debug, che comprendono informazioni sui consigli presentati, criteri, progettazione, esclusioni, inclusioni, consigli di backup presentati e altro ancora. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> API per la funzione Consigli: caricare un CSV per i criteri personalizzati </td> 
   <td colname="col2"> <p>È possibile caricare un CSV per i criteri personalizzati tramite API. </p> <p>Questa funzionalità verrà inserita nell'interfaccia utente di Target Premium in una prossima versione. </p>  </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> API per la funzione Consigli: nuove API di progettazione </td> 
   <td colname="col2"> <p>Le nuove API di progettazione permettono di gestire i progetti delle attività Consigli tramite API. </p>  </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> AP: metriche di successo dipendenti </td> 
   <td colname="col2"> La funzionalità Automated Personalization supporta ora la capacità di limitare una metrica di successo in modo da conteggiare solamente se una precedente metrica di successo è stata soddisfatta. <p>Per ulteriori informazioni, vedi <a href="/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924" format="dita" scope="local">Metriche di successo.</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> AP: download della visualizzazione riepilogo dei rapporti </td> 
   <td colname="col2"> Da oggi, gli utenti possono scaricare la visualizzazione riepilogo (cioè il confronto tra Controllo e Traffico automatizzato) suddivisa in tutte le metriche di successo disponibili. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gli attributi del cliente possono essere utilizzati come token nelle offerte </td> 
   <td colname="col2"> <p>In precedenza, si poteva fare riferimento agli attributi dei clienti negli script di profilo, formattati come <span class="codeph"> crs.get(’&lt; <span class="varname">Nome origine dati </span>&gt;.&lt; <span class="varname"> Nome attributo </span>&gt;’) </span>. </p> <p>Da oggi, gli attributi sono disponibili come token negli script di profilo e direttamente nelle offerte senza prima richiedere uno script di profilo. Il token deve essere nel formato: <span class="codeph">$crs. <span class="varname"> datasourceName </span>. <span class="varname"> attributeName </span> </span>. </p> <p>Consulta <a href="/help/main/c-target/c-visitor-profile/variables-profiles-parameters-methods.md#section_62B4821EB6564FF4A14159A837AD4EDB" format="dita" scope="local">Token CRS</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Miglioramento del codice personalizzato </td> 
   <td colname="col2"> Il codice personalizzato può ora eseguire il codice JavaScript nel tag <span class="codeph">&lt;head&gt;</span>. L'esecuzione del codice non attende più che il tag <span class="codeph">&lt;body&gt;</span> sia presente nel DOM. In precedenza, il selettore era soltanto il primo elemento del tag <span class="codeph">&lt;body&gt;</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Nuovi video didattici </td> 
   <td colname="col2"> Per aiutarti, sono stati aggiunti alcuni video didattici. Attualmente è possibile visualizzare video sul Compositore esperienza visivo <a href="/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D" format="dita" scope="local"> e sul Compositore esperienza basato su moduli </a>. Saranno aggiunti altri video nelle prossime settimane. </td> 
  </tr> 
 </tbody> 
</table>

**Problemi risolti**

Questa versione include le seguenti correzioni:

* Il problema sulla versione 48 di Chrome che causava un malfunzionamento del Compositore esperienza visivo è stato risolto. Per beneficiare di questa correzione, aggiorna Chrome alla versione 50.

**Problemi noti**

Sono stati segnalati i seguenti problemi:

* Quando si seleziona “Disabilita JavaScript” per la pagina A in un&#39;attività multipagina, JavaScript viene disabilitato ovunque, anche se “Disabilita JavaScript” non viene selezionato in altre pagine.

### Adobe [!DNL Target] Standard/Premium 16.3.1 (15 marzo 2016) {#section_A5A9B03A5CCD4213AD656BE722B5FF67}

Questa versione include i miglioramenti e le funzioni seguenti:

<table id="table_F2A89DF1EAB443B4B4C7E0BC6118384B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>First Look: </p> <p>Nuova libreria di implementazione di Target, at.js </p> </td> 
   <td colname="col2"> <p> <p>Nota: questa offerta “First Look” è disponibile tramite download API. Sarà disponibile tramite l'interfaccia di Target in una prossima versione. Nel frattempo, è possibile scaricare la libreria at.js, testarla nel proprio ambiente e distribuirla nell'implementazione della produzione di Target. </p> </p> <p> at.js è una nuova libreria di implementazione per Target, progettata sia per le tipiche implementazioni web sia per le applicazioni a pagina singola. </p></p> <p>Ad esempio, at.js migliora i tempi di caricamento delle pagine per le implementazioni web, migliora la sicurezza e fornisce migliori opzioni di implementazione per le applicazioni a pagina singola. </p> <p>La libreria at.js include anche i componenti inclusi in target.js, quindi cessano le chiamate a target.js. </p> <p>Quando implementi at.js, tieni presente quanto segue: </p> <p> 
     <ul id="ul_8C50C669AA7B4464A5FDECFCFD8662ED"> 
      <li id="li_6065B208480D46178055B40A2654E0C6">I reindirizzamenti del Compositore esperienza visivo non funzionano. </li> 
      <li id="li_A2FABD3C21994511A45DED84283E526E">Le versioni di Internet Explorer precedenti a 8 non sono supportate. </li> 
      <li id="li_04499B391F784B89B09A1D6329B1C790">L’implementazione asincrona potrebbe impedire il funzionamento delle integrazioni legacy come il plug-in Test&amp;Target a SiteCatalyst. </li>  
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Metriche di successo dipendenti </td> 
   <td colname="col2"> <p>Questa funzionalità offre la possibilità di considerare valido il raggiungimento di una metrica di successo da parte di un utente soltanto se questo ha già raggiunto l'idoneità in una metrica di successo diversa. </p> <p> Per esempio, un test potrebbe cambiare l'immagine hero nella pagina home. L'addetto al marketing potrebbe voler contare soltanto le conversioni delle persone che hanno fatto clic sull'immagine hero. In questo modo, può fissare una metrica di successo per “clic su immagine protagonista nella homepage” e poi un'altra metrica per l'acquisto. Successivamente, l'addetto al marketing potrà aggiungere una regola sulla metrica “acquisto” per assicurarsi che i visitatori abbiano prima raggiunto la metrica di successo “clic su immagine protagonista su homepage”. </p> <p> <p>Nota: se il targeting di un pubblico è già impostato su una posizione in una metrica di successo, questa funzione non è supportata per tale metrica. </p> </p> <p> Le Metriche di successo dipendenti sono supportate soltanto nelle attività AB, XT e MVT. Per le attività Automated Personalization e Consigli, la funzione sarà disponibile in seguito. </p> <p>Per ulteriori informazioni, vedi <a href="/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924" format="dita" scope="local">Metriche di successo.</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Miglioramenti alla fruibilità dell'allocazione automatica </td> 
   <td colname="col2"> <p>Quando il modello per un'attività di allocazione automatica è pronto, dall'interfaccia utente non sono consentite le seguenti operazioni: </p> <p> 
     <ul id="ul_52B790B2B0D746769A3471E09CE1A122"> 
      <li id="li_B9F0FFF019CE4CB697F5D0B60061DC27">Impostazione della modalità di Allocazione traffico su Manuale </li> 
      <li id="li_C271B0BE4C5C4B06BB21703239E7B061">Modifica dell'origine dei rapporti da “Adobe Target” a “Analytics” e viceversa </li> 
      <li id="li_E023DDA7ED9142B58D54F42904ADC994">Modifica del tipo di metrica obiettivo </li> 
      <li id="li_619F4765CEEC48E0A45E1821C282A082">Modifica delle opzioni nel pannello “Impostazioni avanzate” </li> 
     </ul> </p> <p>Per la documentazione sull’allocazione automatica, consulta <a href="/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4" format="dita" scope="local">Allocazione automatica del traffico</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Problemi noti**

Sono stati segnalati i seguenti problemi:

* Quando si seleziona “Disabilita JavaScript” per la pagina A in un&#39;attività multipagina, JavaScript viene disabilitato ovunque, anche se “Disabilita JavaScript” non viene selezionato in altre pagine.
* Su Internet Explorer 10 potrebbero verificarsi alcuni problemi di interfaccia, tra cui visualizzazione momentanea di altri contenuti e possibile lentezza.
* L&#39;aggiornamento della versione 48 di Chrome ha generato un problema di malfunzionamento del Compositore esperienza visivo su Chrome. Google sta lavorando alla soluzione. Per informazioni, fai riferimento a [https://code.google.com/p/chromium/issues/detail?id=582603](https://code.google.com/p/chromium/issues/detail?id=582603). Per aggirare questo problema:

   * Utilizza Firefox o Internet Explorer.
   * Abilita il Compositore esperienza avanzato, che può essere configurato dalla scheda **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]**.

### Adobe [!DNL Target] Standard/Premium 16.2.1 (18 febbraio 2016) {#section_47E5CEE2EED24CB3B71D7457673F3200}

Questa versione include i miglioramenti e le funzioni seguenti:

| Funzione | Descrizione |
|---|---|
| Targeting dell&#39;inclusione nelle attività per percentuale. | Ora puoi limitare le voci nelle attività [A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) e [multivariate](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md#task_BF870FA60A8245AB8F0B775BE32EA710) a una percentuale di visitatori o membri del pubblico. Ad esempio, puoi limitare l’accesso al 50% di tutti i visitatori o 45% del pubblico “Californians”. |
| Supporto di Ricavi, Ordini e Coinvolgimento in Allocazione automatica | Da oggi è possibile scegliere metriche su Ricavi (RPV), Ordini e Coinvolgimento come obiettivi per le attività A/B con l&#39;allocazione automatica selezionata. In precedenza, erano supportate solo le metriche di conversione. Consulta [Allocazione traffico automatizzata](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4). |
| Filtra in base all&#39;origine | Da oggi è possibile filtrare l&#39;elenco delle attività in base all&#39;origine in cui sono state create. Le opzioni sono Adobe Target e Adobe Experience Manager. Vedi [Attività](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03). |
| Miglioramenti delle prestazioni di Automated Personalization | Automated Personalization è stato riprogettato per funzionare meglio con un gran numero di combinazioni offerta/posizione. |

**Problemi noti**

Sono stati segnalati i seguenti problemi:

* Quando si seleziona “Disabilita JavaScript” per la pagina A in un&#39;attività multipagina, JavaScript viene disabilitato ovunque, anche se “Disabilita JavaScript” non viene selezionato in altre pagine.
* Su Internet Explorer 10 potrebbero verificarsi alcuni problemi di interfaccia, tra cui visualizzazione momentanea di altri contenuti e possibile lentezza.
* L&#39;aggiornamento della versione 48 di Chrome ha generato un problema di malfunzionamento del Compositore esperienza visivo su Chrome. Google sta lavorando alla soluzione. Per informazioni, fai riferimento a [https://code.google.com/p/chromium/issues/detail?id=582603](https://code.google.com/p/chromium/issues/detail?id=582603). Per aggirare questo problema:

   * Utilizza Firefox o Internet Explorer.
   * Abilita il Compositore esperienza avanzato, che può essere configurato dalla scheda **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]**.

### Adobe [!DNL Target] Standard/Premium 16.1.1 (28 gennaio 2016) {#section_8BF7705B452C449F961AEFC568A0778C}

Questa versione include i miglioramenti e le funzioni seguenti:

<table id="table_8525ECC9B6D0435ABEF8C27F747B7A0C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Miglioramenti dell'interfaccia utente. </td> 
   <td colname="col2"> <p>L'aspetto degli elenchi Attività e Tipi di pubblico è stato migliorato, così come la funzionalità di ricerca/ordinamento. Ulteriori modifiche dell'interfaccia utente verranno incluse nelle prossime versioni. </p> <p>Vedi <a href="/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> attività </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Tipi di pubblico “Super” </td> 
   <td colname="col2"> <p>Utilizza la logica nidificata AND/OR (E/O) nella configurazione dei tipi di pubblico. </p> <p>Vedere <a href="/help/main/c-target/c-audiences/create-audience.md#task_E18BD77A9A8F4ED0AC50569F94556558" format="dita" scope="local"> Creazione di un pubblico </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Seleziona gruppi host nei rapporti </td> 
   <td colname="col2"> <p>I gruppi host sono disponibili nei rapporti. </p> <p> <p>Nota: questa opzione non è disponibile per la Automated Personalization. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Supporto di Internet Explorer 11 </td> 
   <td colname="col2"> <p>Da oggi, Internet Explorer 11 è supportato dall'interfaccia di Target. </p> <p>Vedi <a href="https://experienceleague.adobe.com/docs/target-dev/developer/implementation/supported-browsers.html?lang=it" format="dita" scope="local"> browser supportati </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Visualizzare l'intervallo di affidabilità nei rapporti di Target per variabili continue </td> 
   <td colname="col2"> <p>Visualizza l'intervallo di affidabilità per le metriche di tipo ricavo (RPV, AOV, Vendite, Ordini) e per le metriche di coinvolgimento. </p> <p>Ad esempio, se RPV = 200,00 e l'intervallo di affidabilità = 50,00, per RPV si dovrebbe ottenere 200,00 +/- 50,00 </p> <p>Questa modifica è applicabile ai test A/B, Targeting esperienza e multivariati. </p> <p>Consulta <a href="/help/main/c-reports/statistical-methodology/statistical-calculations.md" format="dita" scope="local">Livello di affidabilità e intervallo di affidabilità.</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Miglioramento delle regole dell'URL del Compositore esperienza visivo </td> 
   <td colname="col2"> <p>In precedenza, le regole dell'URL del modello del Compositore esperienza visivo si ponevano in una condizione OR rispetto all'URL della pagina. Ora si può scegliere AND o OR (E/O) quando si specificano più URL. OR (O) è l'impostazione predefinita. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="premium">Recommendations: </p> <p>Cambiamento nella codifica della distribuzione globale mbox </p> </td> 
   <td colname="col2"> <p>Da oggi, nella creazione di un progetto, il progetto HTML viene racchiuso in un elemento <span class="codeph">&lt;div&gt;</span> per impostazione predefinita. </p> <p>Per informazioni sulla creazione di una progettazione, consulta <a href="/help/main/c-recommendations/c-design-overview/create-design.md#task_CC5BD28C364742218C1ACAF0D45E0E14" format="dita" scope="local">Creare una progettazione.</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tecnica di rinforzo dell'apprendimento automatico del Valore ciclo vita (LTV) </p> </td> 
   <td colname="col2"> <p>Questo nuovo algoritmo si concentra sulla conversione a lungo termine nell'arco di molte sessioni invece che sul miglioramento della conversione nella singola sessione. Questa tecnica è adatta ai siti con molti visitatori di ritorno perché ottimizza il ricavo complessivo dell'intero scambio interattivo con il visitatore. </p> <p>Consulta <a href="/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local">Automated Personalization</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Miglioramento: consentito il targeting sui frammenti hash (#) </p> </td> 
   <td colname="col2"> <p>Da oggi è possibile indirizzare la parte di un URL che segue un hash (#). </p> <p>Vedere <a href="/help/main/c-experiences/c-visual-experience-composer/temtest.md#task_2539D51A18044F82B0D9895636546781" format="dita" scope="local"> Includere la stessa esperienza su pagine simili </a> e altri argomenti correlati. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Scaricare i rapporti sulle metriche di successo </p> </td> 
   <td colname="col2"> <p> Scarica un singolo file CSV con tutte le metriche di successo elencate anziché un rapporto del solo obiettivo finale dell'attività. </p> <p>Vedere <a href="/help/main/c-reports/reports.md" format="dita" scope="local"> report </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Problemi risolti**

Questa versione include le seguenti correzioni:

* Risolto un problema per cui tutte le attività basate su AEM venivano considerate attività di Targeting esperienza (XT). Ora, AEM utilizza i tipi di attività corretti per le attività A/B e XT.
* Rimossa un&#39;opzione per l&#39;utilizzo di metriche non di conversione come obiettivo nelle nuove attività con allocazione automatica. Questa opzione sarà nuovamente disponibile in una versione successiva.
* Risolto un problema che impediva l&#39;eliminazione di uno script di profilo creato in Target Classic da Target Standard.
* Risolto un problema che racchiudeva un modello non HTML di Consigli in un elemento `<div>` quando utilizzato in un flusso di lavoro basato su moduli.
* Risolto un problema che causava il timeout dei calcoli di conflitti in presenza di numerose attività.
* Risolto un problema per cui il file CSV scaricabile mostrava il rapporto di riepilogo anziché quello delle metriche di successo.
* Rimosso il messaggio pop-up “ID univoco” che a volte compariva durante la modifica degli elementi.

**Problemi noti**

Sono stati segnalati i seguenti problemi:

* Quando “Disabilita JavaScript” è attivato per pageA in un’attività multipagina, JavaScript resta abilitato per tutte le pagine ma la funzionalità rimane disabilitata.
* Su Internet Explorer 10 potrebbero verificarsi alcuni problemi di interfaccia, tra cui visualizzazione momentanea di altri contenuti e possibile lentezza.
* L&#39;aggiornamento della versione 48 di Chrome ha generato un problema di malfunzionamento del Compositore esperienza visivo su Chrome. Google sta lavorando alla soluzione. Per informazioni, fai riferimento a [https://code.google.com/p/chromium/issues/detail?id=582603](https://code.google.com/p/chromium/issues/detail?id=582603). Per aggirare questo problema:

   * Utilizza Firefox o Internet Explorer.
   * Abilita il Compositore esperienza avanzato, che può essere configurato dalla scheda **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]**.

## Versione 2015 {#reference_8E940F500A374F9FBCD68CDE9E7E1A00}

### Adobe [!DNL Target] Standard/Premium 15.10.1 (2 novembre 2015) {#section_B5135D75FA0D42A1A3C2711CA3A1B812}

<!-- 

target/r_release-notes-2015.xml

 -->

Questa versione include i miglioramenti e le funzioni seguenti:

<table id="table_EE13D9B959DA4FB0AD6BC03FBF78AEF6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Allocazione automatica nei test A/B </p> </td> 
   <td colname="col2"> <p> Ora puoi allocare automaticamente il traffico per aumentare l’incremento complessivo della campagna e scoprire più velocemente le esperienze vincenti. Questo algoritmo aumenta le prestazioni complessive della campagna mantenendo l’integrità di un test A/B. </p> <p>L’algoritmo si basa su prestazioni misurate (ad esempio il tasso di conversione) e intervalli di attendibilità per produrre una distribuzione del traffico che viene modificata fino a due volte all’ora. </p> <p>Vantaggi chiave </p> <p> 
     <ul id="ul_A41C74C0C7C844F3A923CD6EA5D5D952"> 
      <li id="li_86D3C6A4993F4DC0907BF42986E6CCD1">Mantiene l’integrità di un test A/B assicurando che i visitatori rimangano nella stessa esperienza, come avviene in un test manuale. </li> 
      <li id="li_B849EB2709F84831A1B7A4F312EAFA7E">Trova un vincitore statisticamente significativo più velocemente rispetto a un test A/B manuale. </li> 
      <li id="li_3F258C6DEB7245E2924115C5628BC3C6">Fornisce un maggiore incremento medio della campagna rispetto a un test A/B manuale. </li> 
      <li id="li_C9E82388B93E4A298000984B69CBAEDE">Consente di passare a un test manuale in qualsiasi momento. </li> 
     </ul> </p> <p>Vedere <a href="/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4" format="dita" scope="local"> Allocazione traffico automatica </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Attributi del cliente </p> </td> 
   <td colname="col2"> <p> Carica i dati di prima parte, o Attributi del cliente, tramite il servizio di base Experience Cloud e scegli gli attributi da condividere con Target. Questa funzionalità è stata lanciata a marzo per Analytics e ora si integra direttamente con Target. </p> <p> Ad esempio, puoi utilizzare i dati del cliente quali lo stato di iscrizione (oro, argento ecc.), la cronologia degli acquisti, la destinazione preferita, il negozio di fiducia e così via nel tuo sistema CRM o POS/eCommerce. Ora puoi caricare tali dati su Experience Cloud. Dopo l’autenticazione dell’utente sul tuo sito, Target può abbinare quei dati alle sue abitudini in rete. </p> <p>Consulta <a href="https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/attributes.html?lang=it" format="https" scope="external">Attributi del cliente.</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Selezionando Analytics come origine per la generazione di rapporti per Target, sono disponibili più società. </p> </td> 
   <td colname="col2"> <p>Quando si seleziona Analytics come origine per la generazione di rapporti per Target, si seleziona la suite di rapporti di Analytics che dovrà ricevere i dati relativi all’attività di Target. Scegli innanzitutto una delle società Analytics associate al tuo account, quindi, seleziona la suite di rapporti idonea all’attività. Puoi selezionare solo le suite di rapporti impostate per la connessione ad Adobe Target. Se non visualizzi la suite di rapporti desiderata, disconnettiti, accedi di nuovo ad Adobe Experience Cloud e riprova. Se la suite di rapporti continua a non essere elencata, contatta l’Assistenza clienti. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Nuove opzioni integrate per la creazione di tipi di pubblico </p> </td> 
   <td colname="col2"> <p>Sono state integrate alcune nuove opzioni per i tipi di pubblico: </p> <p> 
     <ul id="ul_16E7B53E324B4FB79E1B1E97A1CE65AC"> 
      <li id="li_60B55A81119E48FE83639B9740A2FD21">Puoi selezionare i visitatori a cui rivolgerti in base alla lingua che usano sul browser. Questo metodo è più preciso del targeting della lingua in base ai dati geografici. </li> 
      <li id="li_84CAAE7E02CA48FA9C7C00C0415046B6">Puoi selezionare i visitatori a cui rivolgerti in base alla versione del browser utilizzato, non solo al browser. </li> 
      <li id="li_AAF8170CAF4C45BB965D1A9A4E9204D5">Ora puoi specificare come target più browser e non più uno solo. </li> 
     </ul> </p> <p>Vedere <a href="/help/main/c-target/c-audiences/c-target-rules/browser.md#concept_221D8EEF53CC45AEACEB17CF336A3658" format="dita" scope="local"> Opzioni browser </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Consigli </p> <p class="Premium">Esclusione degli acquisti passati </p> </td> 
   <td colname="col2"> <p>Target ora esclude automaticamente dagli articoli consigliati al visitatore quelli che ha già acquistato in precedenza. Questa opzione può essere disabilitata per qualsiasi criterio. </p> <p>Questa opzione è ora attiva per tutti i criteri predefiniti, compresi quelli utilizzati nelle attività in esecuzione prima di questa versione. Se non desideri escludere gli acquisti precedenti, modifica le attività in oggetto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Consigli </p> <p> Ponderazione degli attributi </p> </td> 
   <td colname="col2"> <p> Le regole di classificazione per i consigli sono cambiate per i criteri. Questa modifica interessa i consigli esistenti. </p> <p> Utilizza la ponderazione degli attributi per “indirizzare” l’algoritmo. L’addetto al marketing può influenzare l’algoritmo in base a descrizioni importanti o metadati relativi al catalogo dei contenuti. Attribuisci una ponderazione maggiore agli articoli in offerta affinché compaiano più spesso tra i prodotti consigliati. Gli articoli non in offerta non vengono esclusi del tutto, ma sono visualizzati con minore frequenza. È possibile applicare più coefficienti di ponderazione allo stesso algoritmo, e sottoporli a test con traffico suddiviso nel consiglio. </p> <p>Queste nuove ponderazioni sono automaticamente applicate a tutte le attività. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Consigli </p> <p>Impostazione dell’ora per l’elaborazione dei feed </p> </td> 
   <td colname="col2"> <p>Specifica l’orario in cui desidera aggiornare un feed. </p> <p>Consulta <a href="/help/main/c-recommendations/c-products/feeds.md#task_C6CD9EA905744C2CA0BB8259BB74C867" format="dita" scope="local">Creazione di un feed.</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Consigli </p> <p>Impostare un feed in modo che non venga mai eseguito </p> </td> 
   <td colname="col2"> <p>Se non desideri aggiornare un feed, nell’elenco dei feed puoi impostarlo in modo che non venga mai eseguito. </p> <p>Consulta <a href="/help/main/c-recommendations/c-products/feeds.md#task_C6CD9EA905744C2CA0BB8259BB74C867" format="dita" scope="local">Creazione di un feed.</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Consigli </p> <p>Impostare un nuovo tipo di criterio in base a Somiglianza contenuti </p> </td> 
   <td colname="col2"> <p>Criterio basato sugli articoli che può essere utilizzato nelle seguenti modalità: </p> <p> 
     <ul id="ul_86BDF2DE0FCE4665A2985D0C56E50A53"> 
      <li id="li_D83669F9019B431891E072C973B317D7">Articoli attuali con attributi simili </li> 
      <li id="li_4E45848423F2450999C699C64E0EE9E2">Ultimo articolo acquistato con attributi simili </li> 
      <li id="li_901D4AAF7BE244FCB9277DC7EDD91E32">Attributi personalizzati che corrispondono a un determinato entity.id e utilizzano articoli con attributi simili </li> 
      <li id="li_49D52B0182F346E982C11A0C2DA50B4F">Ultimo articolo visualizzato con attributi simili </li> 
      <li id="li_2DBAF32476AC435EB57D08D96CB55683">Articolo con attributi simili più visualizzato </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Nuovi filtri per l’elenco delle attività </td> 
   <td colname="col2"> <p>Sono stati aggiunti vari filtri per aiutarti a mettere in evidenza le attività che più ti interessa vedere nell’elenco delle attività. </p> <p>Vedi <a href="/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> attività </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Consigli </p> <p>Miglioramento: configurazione di criteri per specifici settori </p> </td> 
   <td colname="col2"> <p>Le opzioni irrilevanti in fase di configurazione sono state eliminate. In passato alcune opzioni di configurazione per settori verticali, come ad esempio Media, non erano sempre rilevanti. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Consigli </p> <p>Nuovi criteri predefiniti </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_47E67312A04E414EB797F9AE2A1F7599"> 
      <li id="li_5EDF9006145B4498B2EAD95D642057C5">Altri video come questo </li> 
      <li id="li_6A8DAACE7CD741D0BB766EBCB52BCD88">Altri articoli come questo </li> 
      <li id="li_1B44AB35B045416B8D8B72C428750822">Altri contenuti come questo </li> 
      <li id="li_FEC84CCF3DF3444DAB39F4764DE897B0">Altre presentazioni come questa </li> 
      <li id="li_5E874ACB5B004CACBDB4F8FF217BC593">Altri prodotti come questo </li> 
     </ul> </p> <p>Consulta <a href="/help/main/c-recommendations/c-algorithms/algorithms.md" format="dita" scope="local">Criteri.</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Miglioramento: maggiori dettagli visualizzati quando si usa Analytics come origine per la generazione di rapporti. </td> 
   <td colname="col2"> <p>Le informazioni visualizzate per impostazione predefinita in un rapporto Analytics utilizzando A4T corrispondono ora a quelle visualizzate nel rapporto Target. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Problemi risolti**

Questa versione include le seguenti correzioni:

* È stato risolto un problema in Compositore esperienza globale che impediva di trascinare un angolo per ridimensionare un riquadro di visualizzazione personalizzato.

**Problemi noti**

Sono stati segnalati i seguenti problemi:

* Quando “Disabilita JavaScript” è attivato per pageA in un’attività multipagina, JavaScript resta abilitato per tutte le pagine ma la funzionalità rimane disabilitata.

### Adobe [!DNL Target] Standard/Premium 15.9.1 (30 settembre 2015) {#section_A54204291A99476688E8C0BD8255F93C}

Questa versione include i miglioramenti e le funzioni seguenti:

<table id="table_907A952F54084C2A9C61F10E2B7A7BFF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Compositore di esperienza web mobile </td> 
   <td colname="col2"> <p> Visualizza il tuo sito come si presenta su vari dispositivi mobili e schermi di diverse dimensioni. Imposta i punti di interruzione del sito reattivo e utilizzali nelle attività di ottimizzazione per assicurarti che vengano visualizzate al meglio su tutti i dispositivi usati dai visitatori. </p> <p>Vedi <a href="/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md#concept_8E45527C4ABC41D59AA3553BEDC76FA5" format="dita" scope="local"> riquadri di visualizzazione mobili per esperienze reattive </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Targeting della posizione nella creazione di attività basate su moduli </td> 
   <td colname="col2"> <p> Applica il targeting alle posizioni mbox per limitare la visualizzazione dell’attività. </p> <p>Consulta <a href="/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Compositore esperienza basato su moduli </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Selezione dei colori di sfondo in Compositore esperienza visivo per attività di Automated Personalization e Test multivariati </td> 
   <td colname="col2"> <p>Un selettore di colori consente di impostare i colori di sfondo quando si modificano le attività di Automated Personalization e Test multivariati. </p> <p>Questa funzione era disponibile in precedenza solo per le attività A/B e Targeting esperienza. </p> <p>Consulta <a href="/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local">Opzioni del Compositore esperienza visivo.</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Modifica del testo HTML e Rich Text in Compositore esperienza visivo per le attività di Automated Personalization e Test multivariati </td> 
   <td colname="col2"> <p> Formattazione del testo e HTML in una finestra di tipo Word durante la modifica attività di Automated Personalization e Test multivariati. </p> <p> Questa funzione era disponibile in precedenza solo per le attività A/B e Targeting esperienza. </p> <p>Queste azioni offrono funzionalità di modifica di testo Rich Text mediante tag HTML o stili. Le modifiche apportate nell’editor Rich Text su ogni tipo di azione possono essere viste in visualizzazione sorgente, premendo il pulsante HTML nell’editor Rich Text. Gli stili aggiunti dall’editor Rich Text possono interferire con quelli del sito web del cliente. In questo caso l’utente può accedere alla visualizzazione sorgente e cambiare le modifiche per allinearle agli stili del sito. </p> <p>Consulta <a href="/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local">Opzioni del Compositore esperienza visivo.</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Consigli </p> <p class="Premium">Consigli basati su moduli </p> </td> 
   <td colname="col2"> <p> Puoi creare le attività di consigli per posizioni esterne al sito tra cui e-mail, console, chioschi ecc. </p> <p>Consulta <a href="/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Compositore esperienza basato su moduli </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Consigli </p> <p> Visualizza nel layout le informazioni sull’articolo chiave </p> </td> 
   <td colname="col2"> <p>Mostra l’articolo chiave nel layout di progettazione dei consigli. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Automated Personalization </p> <p>Rapporto basato sulla conversione </p> </td> 
   <td colname="col2"> <p> Se l’obiettivo di ottimizzazione è una metrica di conversione, il rapporto di Dettagli offerta mostra ora l’impatto delle maggiori variabili predittive negli incrementi e nelle conversioni incrementali. Questo rapporto era in precedenza basato soltanto sui ricavi; questa opzione assicura quindi che anche le attività prive di dati di ricavo possano produrre informazioni rilevanti e fruibili. </p> <p>Consulta <a href="/help/main/c-reports/personalization-reports/reports-ap.md" format="dita" scope="local"> rapporti Automated Personalization </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Integrazione e-mail di Adobe Campaign con Target Standard </td> 
   <td colname="col2"> <p> In precedenza era necessario usare Target Classic per impostare una campagna e-mail mirata tramite Adobe Campaign. Con le due nuove funzionalità disponibili in Target Standard (creazione di attività basate su moduli e offerte di reindirizzamento) è ora possibile impostare una campagna e-mail mirata tramite Adobe Campaign.</p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Offerte di reindirizzamento nella creazione di attività basate su moduli </td> 
   <td colname="col2"> <p> I flusso di creazione di attività basate su moduli di Target Standard supporta ora la funzionalità di offerte di reindirizzamento di Target Classic. </p> <p>Consulta <a href="/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Compositore esperienza basato su moduli </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Miglioramento: gli URL delle esperienze nelle attività non utilizzano più i cookie nel sito </td> 
   <td colname="col2"> <p> Gli URL per l’anteprima delle esperienze disponibili a livello di attività sono ora più affidabili. Puoi copiare facilmente gli URL e condividerli con altri membri del gruppo, anche con chi non utilizza Adobe Target. </p> <p> <p>Nota: gli URL aggiornati delle esperienze funzionano solo per le attività create dopo il 30 luglio 2015. Le attività precedenti continuano a utilizzare la funzionalità di anteprima basata su cookie. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> È stato migliorato il supporto per Analytics come origine per la generazione di rapporti per Target </p> </td> 
   <td colname="col2"> <p> Fai clic per visualizzare il rapporto completo di Analytics direttamente dalla pagina del rapporto delle attività. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Miglioramento delle prestazioni dell’elenco attività </td> 
   <td colname="col2"> <p>Il caricamento delle attività nell’elenco è molto più rapido. Le funzioni di ricerca e filtraggio sono molto più veloci, in particolare quando l’elenco contiene numerose attività. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Problemi risolti**

Questa versione include le seguenti correzioni:

* È stato risolto un problema che impediva la visualizzazione delle suite di rapporti di Target nel selettore, dopo essere stato abilitato per Analytics for Target.
* È stato risolto un problema che impediva la ricerca di attività per URL.

**Problemi noti**

Sono stati segnalati i seguenti problemi:

* Quando “Disabilita JavaScript” è attivato per pageA in un’attività multipagina, JavaScript resta abilitato per tutte le pagine ma la funzionalità rimane disabilitata.

### Adobe [!DNL Target] Standard/Premium 15.8.1 (20 agosto 2015) {#section_1C26CB72316A404DB655EBE655F5B8C1}

L’obiettivo di questa versione è quello di offrire pari funzionalità rispetto a Target Classic. Le funzionalità di Target Classic più comunemente usate sono ora disponibili in Target Standard.

Questa versione include i miglioramenti e le funzioni seguenti:

<table id="table_DF5B434D639345B4ACE2467B8966A908"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Creazione e modifica degli script di profilo </td> 
   <td colname="col2"> <p>Gli script di profilo eseguono dei “catcher” per acquisire attributi di profilo per ogni richiesta di mbox. Quando viene ricevuta una richiesta di mbox, Target esegue gli script di profilo pertinenti, determina quale attività deve essere eseguita e visualizza il contenuto appropriato per l’attività e l’esperienza, quindi tiene traccia del successo dell’attività. Questo consente di tenere traccia di informazioni sulla visita: la posizione del visitatore, l’ora del giorno, quante volte ha visitato il sito, se ha effettuato acquisti in passato e così via. Queste informazioni vengono poi aggiunte al profilo del visitatore, in modo da poter monitorare meglio la sua attività sul sito. </p> <p>Consulta <a href="/help/main/c-target/c-visitor-profile/profile-parameters.md#concept_01A30B4762D64CD5946B3AA38DC8A201" format="dita" scope="local">Attributi del profilo </a>. 
     <!--(Copy help from Classic)--> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Intervallo di affidabilità per metriche binarie </td> 
   <td colname="col2"> <p>I rapporti aggiornati che utilizzano i dati basati su Target mostrano l’intervallo di affidabilità dell’incremento rispetto a quello di controllo. </p> <p>Consulta <a href="/help/main/c-reports/statistical-methodology/statistical-calculations.md" format="dita" scope="local">Livello di affidabilità e intervallo di affidabilità.</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Download dei dati dei rapporti dell’attività per l’esportazione </td> 
   <td colname="col2"> <p>Scarica i dati in formato .csv per importarli rapidamente in Excel o in altri programmi di analisi dei dati. Questa funzione è compatibile con le attività A/B, Targeting esperienza e Test multivariato. </p> <p>Consulta <a href="/help/main/c-reports/reports.md#section_3099BC87DCAE46A2B075E1FF5B6552A6" format="dita" scope="local">Download dei rapporti.</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Modifica di testo Rich Text e HTML in Compositore esperienza visivo </td> 
   <td colname="col2"> <p>Sono disponibili opzioni di formattazione per modificare il testo e contenuti HTML per le attività A/B e Targeting esperienza nel Compositore esperienza visivo. Puoi scegliere font e stile, l’allineamento del testo e altre opzioni standard per la formattazione del testo. Quando modifichi l’HTML, puoi passare dalla visualizzazione del codice alla visualizzazione per modifica Rich Text dell’HTML. </p> <p>Consulta <a href="/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local">Opzioni del Compositore esperienza visivo.</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Selezione del colore di sfondo nel Compositore esperienza visivo </td> 
   <td colname="col2"> <p>Un selettore di colori consente di impostare i colori di sfondo quando si modificano le attività A/B e Targeting esperienza nel Compositore esperienza visivo. Questa opzione non è disponibile se è impostata un’immagine di sfondo. </p> <p>Consulta <a href="/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local">Opzioni del Compositore esperienza visivo.</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Archiviazione delle attività </td> 
   <td colname="col2"> <p>Puoi inviare un’attività all’archivio. Per renderla nuovamente attiva, puoi approvare un’attività archiviata. Per impostazione predefinita le attività archiviate non vengono visualizzate nell’elenco delle attività. </p> <p>Vedi <a href="/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> attività </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Automated Personalization </p> <p>Targeting a livello di offerta </p> </td> 
   <td colname="col2"> <p>Permette agli addetti al marketing di applicare regole di targeting alle offerte in Automated Personalization. Consente di non mostrare offerte specifiche a un determinato gruppo di persone. </p> <p>Vedi <a href="/help/main/c-activities/t-automated-personalization/ap-target-offers.md#task_F207ED7A41B84FD39BB6FCBFABF4B23E" format="dita" scope="local"> offerte AP di Target </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Funzione Premium Consigli </p> <p>Mostra il numero di attività che utilizzano una progettazione </p> </td> 
   <td colname="col2"> <p>Nella libreria delle progettazioni sono indicate quante attività attive e inattive utilizzano ciascuna progettazione. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Funzione Premium Consigli </p> <p>Visualizzazione del titolo dinamico personalizzato nella progettazione </p> </td> 
   <td colname="col2"> <p>Scegli un titolo da mostrare con una determinata progettazione. Questo titolo non deve necessariamente corrispondere al titolo visualizzato dai visitatori della pagina. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Funzione Premium Consigli </p> <p>Token API </p> </td> 
   <td colname="col2"> <p>Puoi impostare il token API client dalla funzione Premium Consigli. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Miglioramento: URL utilizzati di frequente </td> 
   <td colname="col2"> Quando si immette un URL per un’attività o una nuova pagina di un’attività, un menu mostra gli URL più recenti e più utilizzati. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Nuove opzioni di targeting per dispositivi mobili </td> 
   <td colname="col2"> <p>È ora possibile eseguire il targeting di più dispositivi mobili senza uno script di profilo. </p> <p>Vedere <a href="/help/main/c-target/c-audiences/c-target-rules/mobile.md#concept_2A794199DC1A4D349FFFBC7DCF1FEB89" format="dita" scope="local"> Mobile </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Adobe [!DNL Target] Standard/Premium 15.7.1 (30 luglio 2015) {#section_9C888BFD04A94DD58616D3F67D209CCC}

Questa versione include i miglioramenti e le funzioni seguenti:

<table id="table_46FF5AF77D824ADC941B1E472234F05C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Registro delle modifiche apportate alle attività </td> 
   <td colname="col2"> <p>Il registro elenca le modifiche apportate a un’attività. Per ogni modifica è riportata l’azione eseguita e l’utente che l’ha eseguita, con relativa marca temporale. </p> <p>Vedere <a href="/help/main/c-activities/change-log.md#task_D6F224E8CE8346699187D21CD9A2B4AB" format="dita" scope="local"> registro modifiche attività </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Attività multipagina </td> 
   <td colname="col2"> <p>Un’attività multipagina consente di creare una storia su più pagine, con una progettazione specifica per ogni pagina. </p> <p>Ad esempio, ti può essere utile per testare un’offerta di spedizione gratuita per acquisti superiori a un determinato importo. Vorresti che questa offerta venga visualizzata nella pagina di destinazione, in una pagina di categoria e in alcune pagine di prodotto, ma con dimensioni e posizione diverse in ciascun tipo di pagina. L’offerta dovrà essere prominente sulla home page, quindi proposta di nuovo ma più piccola su altre pagine correlate. </p> <p>Puoi anche utilizzare un’attività multipagina per definire layout diversi per i siti desktop e mobile non reattivi. </p> <p>Consulta <a href="/help/main/c-experiences/c-visual-experience-composer/multipage-activity.md#concept_277E096063E14813AC5D8EDFA1D2ED48" format="dita" scope="local">Attività multipagina.</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Creazione di attività basate su moduli </td> 
   <td colname="col2"> <p>Puoi creare un’attività senza usare il Compositore esperienza visivo. In alternativa, un modulo di permette di scegliere posizioni e offerte. In questo modo le attività di Target Standard possono essere distribuite per e-mail, applicazioni mobili, chioschi e altri luoghi non compatibili con il Compositore esperienza visivo. </p> <p>Consulta <a href="/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Compositore esperienza basato su moduli </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Metriche di successo configurabili </td> 
   <td colname="col2"> <p> Opzioni specifiche consentono di determinare come calcolare le metriche di successo. Le opzioni includono il conteggio della metrica per impression o una volta per visitatore, e la possibilità di scegliere se mantenere o meno l’utente nell’attività. Questo equivale alle “opzioni avanzate” per le metriche di successo disponibili in Target Classic. </p> <p>Vedere <a href="/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924" format="dita" scope="local"> metriche di successo </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Miglioramento: rimozione del limite di Targeting esperienza. </td> 
   <td colname="col2"> Il limite precedente di dieci esperienze in Targeting esperienza è stato rimosso. </td> 
  </tr>  
  <tr> 
   <td colname="col1"> Sincronizzazione dei profili in tempo reale per i dati 3rdPartyId </td> 
   <td colname="col2"> Quando un visitatore del sito accede a metà sessione e ottiene un 3rdpartyId, tutti gli attributi di profilo precedentemente caricati associati a tale 3rdpartyId sono immediatamente disponibili. Consulta <a href="/help/main/c-target/c-audiences/c-target-rules/visitor-profile.md#concept_E972690B9A4C4372A34229FA37EDA38E" format="dita" scope="local"> Profilo visitatore </a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Funzione Premium Consigli: ricerca per nome facet </td> 
   <td colname="col2"> È ora possibile eseguire una ricerca per nome facet. </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Automated Personalization: rilevamento metriche post-obiettivo </td> 
   <td colname="col2"> <p> In precedenza Target riavviava un’esperienza una volta raggiunto l’obiettivo di modellazione. Ora gli utenti possono essere mantenuti nell’attività per scopi di tracciamento anche dopo aver raggiunto l’obiettivo di modellazione. </p> <p> Ad esempio, spesso per aumentare il numero di clic si ricorre a un’attività di Automated Personalization che viene impostata come obiettivo di modellazione. Tuttavia è importante capire in che modo un maggior numero di clic porti alla conversione finale, perciò è essenziale effettuare il tracciamento fino alla conversione finale. </p> Consulta <a href="/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local">Automated Personalization</a>. </td> 
  </tr> 
 </tbody> 
</table>

**Problemi risolti**

Questa versione include le seguenti correzioni:

* Analytics come origine per la generazione di rapporti per Target è ora supportato per le attività XT.
* È stato risolto un problema a causa del quale l’esperienza di controllo visualizzata in Analytics veniva cambiata quando l’attività diventava attiva.
* È stato risolto un problema in cui i valori dopo # in un URL erano considerati parte del percorso durante la creazione del pubblico o segmento.

**Problemi noti**

Sono stati segnalati i seguenti problemi:

* Quando “Disabilita JavaScript” è attivato per pageA in un’attività multipagina, JavaScript resta abilitato per tutte le pagine ma la funzionalità rimane disabilitata.

### Adobe [!DNL Target] Standard/Premium 15.6.1 (25 giugno 2015) {#section_43FEA310830E4E8E853FAB56B12B1301}

Questa versione include i miglioramenti e le funzioni seguenti:

<table id="table_C0B37E1730014ADA8C36310093F5C43A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Miglioramenti di compatibilità per Compositore esperienza visivo </p> </td> 
   <td colname="col2"> <p> Una nuova impostazione a livello di account facilita la generazione dei selettori CSS giusti da parte di Target. Ad esempio si può specificare se Target deve utilizzare le classi o gli ID. Ciò migliora la compatibilità con AEM. Questa impostazione può essere disabilitata a seconda per singole attività. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Targeting esperienza supporta Analytics come origine per la generazione di rapporti </p> </td> 
   <td colname="col2"> <p>Ora si può utilizzare Analytics come origine per la generazione di rapporti per le attività Targeting esperienza. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Automated Personalization: indicazione visiva dello stato del modello </p> </td> 
   <td colname="col2"> <p> Quando un modello predittivo supera i criteri qualitativi richiesti ed è ritenuto valido, è considerato pronto e viene utilizzato per calcolare un punteggio personalizzato per le decisioni in merito alle offerte. Quando il modello è pronto, l’icona orologio è sostituita da un segno di spunta e Target può iniziare a consegnare contenuti personalizzati. Poiché l’incremento è previsto solo una volta che i modelli sono pronti, l’indicazione visiva consente di impostare la giusta aspettativa. Utilizza il Calcolatore di traffico di Compositore esperienza visivo per ottenere una stima di quando i modelli saranno pronti. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Funzione Premium Consigli: navigazione in Compositore esperienza visivo </p> </td> 
   <td colname="col2"> <p> Consente di aprire Compositore esperienza visivo in una pagina, quindi di seguire i collegamenti e l’invio di moduli per raggiungere altre pagine del sito, ad esempio il carrello. Una volta raggiunta la pagina da testare, puoi tornare alla modalità “Composizione” di Compositore esperienza visivo per crea le esperienze. Ad esempio, puoi modificare un messaggio nella pagina Spedizione, quindi testarlo rispetto al messaggio predefinito. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Funzione Premium Consigli: ricerca catalogo per facet </p> </td> 
   <td colname="col2"> <p> Una modalità di ricerca più efficace nel catalogo. Inoltre, consente di limitare più facilmente i risultati della ricerca a set di prodotti molto specifici. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Mostra le campagne esterne nell’elenco delle attività di Target Standard </p> </td> 
   <td colname="col2"> <p> Puoi visualizzare le campagne di Target Classic nell’elenco delle attività di Target Standard. Se desideri filtrare le campagne di Target Classic e visualizzare solo Target Standard, utilizza il filtro di ricerca “Origine”. Ad esempio, per visualizzare solo le attività di Adobe Target Standard, seleziona il filtro Origine e digita “Adobe Target”. La possibilità di visualizzare le attività create in Recommendations Classic o Adobe Mobile Services verrà aggiunta in una versione futura. </p> <p>È possibile attivare e disattivare le attività create in altre soluzioni tramite l’interfaccia utente di Target. Per tutte le altre modifiche dovrai modificare le attività nella soluzione di origine. </p> <p> Per le attività create in altre soluzioni, le informazioni sui tipi di pubblico non sono visibili nella pagina Panoramica. Puoi vedere le informazioni sul pubblico nella soluzione in cui è stata creata l’attività. </p> <p>Vedi <a href="/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> attività </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Problemi risolti**

Questa versione include le seguenti correzioni:

* Aggiunta di un messaggio per indicare che un’attività non visualizzabile è visibile in Target Classic.
* È stato risolto un problema che causava un lento reindirizzamento degli URL.
* È stato risolto un problema che interrompeva le metriche di successo del tracciamento dei clic se nella stessa attività venivano cancellate altre metriche di successo.
* È stato risolto un problema in cui l’immagine caricata nella progettazione di layout di Consigli non veniva visualizzata correttamente in Compositore esperienza visivo.
* È stato risolto un problema relativo al calcolatore del traffico nelle attività di Automated Personalization in cui veniva utilizzato il numero di combinazioni anziché la somma delle offerte per le varie posizioni.
* È stato risolto un problema in cui i parametri mbox non sempre venivano visualizzati nelle schermate di creazione del pubblico.
* È stato risolto un problema che bloccava gli aggiornamenti sull’anteprima delle progettazioni di layout di Consigli.

### Adobe [!DNL Target] Standard/Premium 15.5.1_Hotfix (28 maggio 2015) {#section_D751F55A3812417FAA72BD6872AE3C2A}

Questa versione hotfix include le seguenti correzioni:

* È stato risolto un problema che impediva la visualizzazione della casella Incremento stimato dei ricavi.
* È stato risolto un problema che impediva la corretta visualizzazione del pulsante Crea attività per alcuni utenti.
* È stato risolto un problema a causa del quale scompariva la casella di testo Nome attività nel Compositore esperienza visivo durante la modifica di attività A/B e Targeting esperienza.

### Adobe [!DNL Target] Standard/Premium 15.5.1 (21 maggio 2015) {#section_FF0F959908784AF0906EFB9E8324F207}

Questa versione include i miglioramenti e le funzioni seguenti:

<table id="table_3985F758176F4884A94AFDFB78B24209"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Inserimento e modifica di codice personalizzato in Compositore esperienza visivo </p> </td> 
   <td colname="col2"> <p>Consente di visualizzare, modificare e aggiungere nuove azioni tramite un editor di codice in Compositore esperienza visivo. </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md#concept_B3A6E9EE3A60406DB640E205EA1745B5" format="dita" scope="local">Editor di codice</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Aggiunta di JavaScript e CSS a inizio pagina </p> </td> 
   <td colname="col2"> <p> Puoi aggiungere codice JavaScript alla pagina sotto il tag <span class="codeph">&lt;body&gt;</span> senza selezionare alcun elemento nella pagina. </p> <p>Per ulteriori informazioni, consulta <a href="/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md#concept_B3A6E9EE3A60406DB640E205EA1745B5" format="dita" scope="local">Editor di codice</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Nuove opzioni di creazione pubblico </p> </td> 
   <td colname="col2"> <p>Ora hai a disposizioni le seguenti opzioni di targeting (nella sezione Geo durante la creazione di un pubblico): </p> <p> 
     <ul id="ul_FE1E3605FB8042E9B5E80C0DB0C6C2AD"> 
      <li id="li_6D112A4DB2344B4E9F1B84E943A43DD8">ISP </li> 
      <li id="li_5C95F3F55D194D81905F8138FB546288">Dominio di rete </li> 
      <li id="li_63E3606516BC4FFC8C91E49297542464">Velocità di connessione (opzioni disponibili: banda larga, dial-up, mobile, T1, T3, satellite) </li> 
     </ul> </p> <p>Vedi <a href="/help/main/c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271" format="dita" scope="local"> tipi di pubblico </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Nuove funzionalità della funzione Premium Consigli </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_6DC206CB52E34498BC762FCCF77807AA"> 
      <li id="li_B26568D642974F17B4B2D6E42CFDC5B9"> <p>Nuova modalità di anteprima per visualizzare le progettazioni di layout con JavaScript </p></li> 
      <li id="li_B8D1ADE874D244F198CBD3387ED3E310"> <p>La ricerca nel catalogo ora supporta la ricerca libera per la lingua inglese </p> </li> 
      <li id="li_EB8D595EA8A84B37A3262F76543E1B05"> <p>Supporto a livello di account per l’immissione di un URL di base statico da anteporre a tutti i valori <span class="codeph">entity.thumbnailUrl</span> </p></td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium"> Miglioramenti nella funzione Premium Consigli </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_1CF5F2D0CDE84DDC9C445B5CD878EEAA"> 
      <li id="li_EB225752776449C6B21C2B2514B508C5"> <p>Miglioramenti dell’anteprima progettazione in Compositore esperienza visivo </p> </li> 
      <li id="li_2CD8267EF166421DBB6EFBF704625848"> <p>Miglioramenti di layout nelle progettazioni predefinite </p> </li> 
      <li id="li_D737754C200844638B536A3BE02E9C5F"> Raccolta mostrata nel diagramma di targeting</li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium"> Funzionalità Recommendations Classic ora supportata nella funzione Premium Consigli </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_E0D6A9C12B514DE3B3EA753BB4D56662"> 
      <li id="li_2A728C8938834162A0C0C1C926AC5DD9"> Rendering di modelli parziale <p>Vedere <a href="/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content" format="dita" scope="local"> Impostazioni contenuto </a>. </p> </li> 
      <li id="li_B1DFC829D19B4570AB5A7F937C7EF2CC"> Specifica delle regole di backup per criterio </li> 
      <li id="li_F8C9690CEC974E37B72A85C2FACFAA6D"> Supporto FTPS per i feed di prodotto</li> 
      <li id="li_3C0FA493C87345E4BE994936DF0D0162"> Gli algoritmi personalizzati vengono ora visualizzati automaticamente come criteri</li> 
      <li id="li_5B074C9FB3CB46EBA6EB4D8B1098480E"> Reindicizzazione oraria automatica dei cataloghi di prodotti per clienti senza feed </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Automated Personalization: aggiunta di collegamenti per controllo qualità </p> </td> 
   <td colname="col2"> <p> Ora puoi visualizzare in anteprima come si presenteranno le tue esperienze ai visitatori. Puoi visualizzare e condividere collegamenti per le esperienze di AP sul tuo sito per ottenerne una “anteprima fedele” al di fuori di Compositore esperienza visivo di Target. </p> <p>Consulta <a href="/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local">Automated Personalization</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Test multivariati con Analytics: anteprima dell’esperienza dal rapporto Prestazioni </p> </td> 
   <td colname="col2"> <p>Utilizzando Analytics come origine per la generazione di rapporti per i test multivariati, puoi visualizzare in anteprima le attività di test multivariati dal rapporto Prestazioni. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Test A/B e Targeting esperienza: flusso di creazione attività in tre fasi </p> </td> 
   <td colname="col2"> <p> <a href="/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md" format="dita" scope="local"> Crea attività A/B </a>e <a href="/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md#task_D6B3429AC31549E1A70EDF04B3DDC765" format="dita" scope="local">di Targeting esperienza </a>in tre passaggi invece di quattro. Questa modifica rende il processo di creazione di queste attività più simile al flusso di lavoro di altre attività, come ad esempio Automated Personalization e Test multivariati. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Analytics come origine per la generazione di rapporti è disponibile con la maggior parte dei tipi di attività. </p> </td> 
   <td colname="col2"> <p> L’attività A/B con Analytics non esiste più. L’opzione di utilizzo di Analytics come origine per la generazione di rapporti è ora disponibile nella pagina Obiettivo e impostazioni per tutti i tipi di attività eccetto Automated Personalization e Targeting esperienza. Di conseguenza non esiste più un tipo separato di attività denominato Test A/B con dati Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Mostra le campagne esterne nell’elenco delle attività di Target Standard </p> </td> 
   <td colname="col2"> <p> Puoi visualizzare le campagne di Target Classic nell’elenco delle attività di Target Standard. Se desideri filtrare le campagne di Target Classic e visualizzare solo Target Standard, utilizza il filtro di ricerca “Origine”. Ad esempio, per visualizzare solo le attività di Adobe Target Standard, seleziona il filtro Origine e digita “Adobe Target”. La possibilità di visualizzare le attività create in Recommendations Classic o Adobe Mobile Services verrà aggiunta in una versione futura. </p> <p>Vedi <a href="/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> attività </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Esportazione del rapporto sugli ordini </p> </td> 
   <td colname="col2"> <p> Possibilità di esportare e scaricare il rapporto sugli ordini aggiunto ai rapporti di Target. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Beta: incremento e affidabilità in A4T </p> </td> 
   <td colname="col2"> <p> Incremento e affidabilità sono ora disponibili per metriche standard ed eventi personalizzati di Analytics. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Problemi risolti**

Questa versione include le seguenti correzioni:

* È stato risolto un problema nella creazione del pubblico in cui la modifica degli operatori provocava l’eliminazione di valori di attributi.
* Miglioramenti che consentono di selezionare in Compositore esperienza visivo le mbox regionali con codice personalizzato.
* È stato risolto un problema nella funzionalità Consigli in cui gli attributi con caratteri a doppio byte (per i casi multilingue) bypassavano le regole di inclusione.
* Tutti i tipi di attività ora supportano nomi di attività fino a 200 caratteri di lunghezza.

### Adobe [!DNL Target] Standard/Premium 15.3.1 (26 marzo 2015) {#section_591371851693496C820175753F588E73}

Questa versione include i miglioramenti e le funzioni seguenti:

<table id="table_5A2F2058ACFB455E9F69484CA0C8D3DE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Miglioramenti a Compositore esperienza visivo </p> </td> 
   <td colname="col2"> <p>I contenuti visualizzati al passaggio del mouse, come i menu a comparsa e i mini-carrelli, possono essere selezionati e modificati in Compositore esperienza visivo. </p> <p>Vedi <a href="/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D" format="dita" scope="local"> esperienze </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="premium">Automated Personalization: Calcolatore del traffico </p> </td> 
   <td colname="col2"> <p>Il Calcolatore del traffico, precedentemente disponibile solo per il tipo di attività Test multivariato, è ora disponibile per le attività di Automated Personalization. </p> <p>Consulta <a href="/help/main/c-activities/t-automated-personalization/ap-traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714" format="dita" scope="local">Stima del traffico necessario per il successo.</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="premium">Automated Personalization: anteprima visiva </p> </td> 
   <td colname="col2"> <p>Puoi visualizzare in anteprima ogni combinazione di contenuti in Compositore esperienza visivo. </p> <p>Vedere <a href="/help/main/c-activities/t-automated-personalization/ap-preview-experiences.md#task_21A700587E88453A9FC2210C0DE53A28" format="dita" scope="local"> esperienze di anteprima per un test Automated Personalization </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="premium">Consigli: miglioramento della visualizzazione del contenuto </p> </td> 
   <td colname="col2"> <p>Ora puoi visualizzare ogni elemento idoneo alla raccolta o all’esclusione durante la visualizzazione o la modifica della raccolta. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="premium">Consigli: miglioramento dei risultati di ricerca </p> </td> 
   <td colname="col2"> <p>Viene visualizzato il numero totale di elementi corrispondenti a ogni stringa di ricerca. </p>  </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Caricamento degli attributi cliente in Adobe Analytics </p> </td> 
   <td colname="col2"> <p>Gli utenti di Analytics che acquisiscono dati di clienti Enterprise in un database CRM (Customer Relationship Management) possono caricarli in Experience Cloud. </p> <p>Una volta salvati i dati in Experience Cloud, puoi ad esempio creare in Analytics un segmento di pubblico la cui definizione includa gli attributi cliente, e condividere tale pubblico con Target. </p> <p> <p>Nota: Target non è ancora in grado di utilizzare direttamente gli attributi clienti non elaborati. </p> </p></td> 
  </tr> 
 </tbody> 
</table>

**Problemi risolti**

Questa versione include le seguenti correzioni:

* Per le attività basate su Analytics for Target, le colonne Incremento e Affidabilità sono ora nascoste per le metriche di Analytics per le quali non è possibile eseguire i calcoli.
* È stato risolto un problema per cui il formato breve del metatag `charset` non veniva riconosciuto in Compositore esperienza avanzato

**Problemi noti**

* Gli eventi di conversione basati su Target per i test multivariati in Target Standard/Premium non vengono inseriti nei rapporti quando Analytics è utilizzato come origine per la generazione di rapporti per Target. Questo problema verrà risolto al più presto.

### Adobe [!DNL Target] 15.2.1 (19 febbraio 2015) {#section_9AA19B060D814E08A673FB752E21D0C3}

Questa versione include i miglioramenti e le funzioni seguenti:

<table id="table_1558E5A5BAB64CC281C193F5A49E2ECE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p class="premium">Nuovo tipo di attività: Consigli </p> </td> 
   <td colname="col2"> <p>Mediante le attività Consigli vengono visualizzati automaticamente prodotti o contenuti che potrebbero interessare ai clienti sulla base delle loro precedenti attività. I consigli aiutano a indirizzare i clienti verso elementi rilevanti di cui potrebbero non essere a conoscenza. </p> <p>La funzionalità Consigli è disponibile come parte della soluzione Target Premium. Non è disponibile in Target Standard senza una licenza Target Premium. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Problemi risolti**

Questa versione include le seguenti correzioni:

* È stato risolto un errore che causava il mancato funzionamento di un’offerta di reindirizzamento quando si rivisitava una pagina.

### Adobe [!DNL Target] 15.1.1 (22 gennaio 2015) {#section_059F9B41804B4FA58D05C4485EDF926D}

Questa versione include i miglioramenti e le funzioni seguenti:

<table id="table_5D4C3C5695BA4A88BC65E2721CFB073A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Nuovo tipo di attività: Test multivariato </td> 
   <td colname="col2"> <p> Un testo multivariato fattoriale completo confronta tutte le possibili combinazioni di offerte nelle aree dei contenuti per determinare la combinazione di contenuti ottimale. Nei test multivariati vengono anche indicati quali contenuti in quali aree contribuiscono maggiormente al successo dell’attività. Un uso comune dei test multivariati consiste nell’ottimizzare un’intera pagina dopo aver determinato il layout ottimale tramite un test A/B. Grazie al test multivariato puoi ottimizzare le singole risorse sulla pagina (ad esempio l’immagine principale, i titoli o i contenuti promozionali). </p> <p>Per un video introduttivo, visita <a href="https://my.adobeconnect.com/p2k6u8iiu6l/" format="https" scope="external">https://my.adobeconnect.com/p2k6u8iiu6l/.</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Possibilità di sfogliare pagine ed elementi di pagina in Compositore esperienza visivo </td> 
   <td colname="col2"> <p> Consente di aprire Compositore esperienza visivo in una pagina, quindi di seguire i collegamenti e l’invio di moduli per raggiungere altre pagine del sito, ad esempio il carrello. Una volta raggiunta la pagina da testare, puoi tornare alla modalità “Composizione” di Compositore esperienza visivo per crea le esperienze. Ad esempio, puoi modificare un messaggio nella pagina Spedizione, quindi testarlo rispetto al messaggio predefinito. </p> <p> Mediante la modalità di navigazione è inoltre possibile interagire con una pagina per arrivare allo stato giusto, ad esempio spostarsi all’interno di una sequenza di immagini, aprire un mini-carrello o chiudere un elemento a comparsa. Una volta che la pagina è nello stato desiderato, torna alla modalità “Composizione” e crea il test. </p> <p> Attualmente compatibile con test A/B, Targeting esperienza e test A/B con Analytics. </p> <p>Per ulteriori informazioni, vedere <a href="/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D" format="dita" scope="local"> esperienze </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Targeting di dispositivi mobili </td> 
   <td colname="col2"> Puoi selezionare le opzioni relative ai dispositivi mobili durante la creazione di un pubblico. <p>Per ulteriori informazioni, vedere <a href="/help/main/c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271" format="dita" scope="local"> tipi di pubblico </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Tracciamento dei clic (Automated Personalization) </td> 
   <td colname="col2"> <p>Ora puoi tenere traccia dei clic in Automated Personalization. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Utility di debugging mboxTrace </td> 
   <td colname="col2"> <p> Consente di esaminare i dettagli dell’implementazione della pagina di Target e lo stato di distribuzione dell’attività o esperienza, per una migliore risoluzione dei problemi. </p> <p>Per ulteriori informazioni, vedere <a href="/help/main/c-activities/c-troubleshooting-activities/content-trouble.md#concept_D2548B486C984B1E97ED7A72075B8EEA" format="dita" scope="local"> Risoluzione dei problemi relativi alla distribuzione dei contenuti </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Problemi risolti**

Questa versione include le seguenti correzioni:

* È stato risolto un problema di scorrimento in IE10.

## Versione 2014 {#reference_A841709C803C4ECEB236F62E6513EB0F}

### Adobe [!DNL Target] 14.10.2 (6 novembre 2014) {#section_E7036B45DF974FB7B81E67261357A01B}

<!-- 

target/r_release-notes-2014.xml

 -->

Questa versione è incentrata maggiormente sulla stabilità del server. Non sono disponibili nuove funzionalità per questo aggiornamento.

### Adobe [!DNL Target] 14.10.1 (30 ottobre 2014) {#section_D557CB331A004155B91CFE5B197076F3}

Questa versione include i miglioramenti e le funzioni seguenti:

| Funzione | Descrizione |
|---|---|
| Offerte di reindirizzamento | Reindirizzano un&#39;esperienza a un URL diverso consentendoti di sottoporre a test una pagina rispetto a un&#39;altra. Consulta [Crea un’offerta di reindirizzamento](/help/main/c-experiences/c-visual-experience-composer/redirect-offer.md#task_9578678D42784F5EB9638F8AC8C911FA). |
| Applicare il targeting alle metriche di successo | Scegli un pubblico già salvato da applicare a una metrica di successo. Con questa funzione puoi limitare ciò che viene conteggiato dalle azioni per un particolare evento di successo. Un esempio potrebbe essere la limitazione delle conversioni quando l&#39;ordine è superiore a $ 0, oppure il conteggio del successo solo quando un utente visualizza una data pagina nella stessa sessione di accesso all&#39;attività. |
| Automated Personalization: seleziona e genera rapporti relativi alle metriche RPV/AOV | Ora puoi selezionare le metriche RPV e AOV nel flusso di creazione delle esperienze di Automated Personalization. Per ulteriori informazioni sulla creazione di un&#39;attività Automated Personalization, vedere [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9). |
| Controlli delle autorizzazioni migliorati | Solo gli utenti con sufficienti autorizzazioni possono modificare i tipi di pubblico. |

Questa versione include i seguenti miglioramenti:

* La pagina della panoramica mostra l&#39;obiettivo dell&#39;attività.
* Viene visualizzato un avviso quando JavaScript è immesso nella casella di modifica HTML.

### Adobe [!DNL Target] 14.9.1 (19 settembre 2014) {#section_681F27FBFDFF46FE8A1A8E24A50A26F4}

Questa versione include i miglioramenti e le funzioni seguenti:

| Funzionalità/Miglioramento | Descrizione |
|---|---|
| Consentire l&#39;inserimento e la modifica di JavaScript | Aggiunta della possibilità di modificare e inserire JavaScript personalizzati nell&#39;editor esperienze quando si sceglie **[!UICONTROL Edit HTML]** dal menu azioni. |
| Importazione automatica dei tipi di pubblico | Quando un utente apre l&#39;elenco dei tipi di pubblico e i tipi di pubblico hanno una durata superiore a 10 minuti, questi vengono automaticamente importati in background. |
| Incremento della dimensione delle offerte in HTML rispetto a quelle sincronizzabili con [!DNL Target Classic] | Limite precedente incrementato da 64 KB a 256 KB. |

Questa versione include le seguenti correzioni:

* Risoluzione del problema che causava l&#39;invio errato di offerte video in Firefox.
* Risoluzione del problema che impediva a un&#39;azione annullata in Modifica collegamento di essere visualizzata come annullata nel Compositore esperienza visivo.
* Risoluzione del problema nell&#39;editor esperienze di Automated Personalization che impediva che un&#39;offerta video modificata venisse visualizzata come tale.
* Risoluzione dell&#39;errore che causava la visualizzazione come pagina bianca in Google Chrome della pagina Collisione di un&#39;attività.

### Adobe [!DNL Target] 14.8.1 (21 agosto 2014) {#section_02D0DFA7A8D145B2B3FEFF83591243E1}

Questa versione include le seguenti nuove funzionalità e miglioramenti:

| Funzionalità/Miglioramento | Descrizione |
|---|---|
| Migliore sincronizzazione delle offerte HTML in [!DNL Target Classic] grazie all’aumento del limite di caratteri | Limite di caratteri di un&#39;offerta HTML creata in Contenuto aumentato per allinearlo al limite di 256 KB delle offerte HTML, sincronizzato in [!DNL Target Classic]. |
| Migliorata l&#39;esperienza utente quando si genera un errore nell&#39;editor Esperienze. | L&#39;editor Esperienze mostra un messaggio quando le modifiche della struttura DOM nella pagina impediscono il funzionamento dei selettori. |

**Correzioni**

* Risoluzione di un problema che impediva la generazione del grafico di rapporto durante la navigazione tra attività.
* È stato risolto un problema a causa del quale i collegamenti selezionati non venivano contrassegnati come selezionati quando gli utenti facevano clic su **[!UICONTROL Select Link]** nella pagina [!UICONTROL Goals and Settings].

* È stato corretto un errore che impediva la visualizzazione di una nuova attività in [!UICONTROL Activity List] dopo l&#39;attivazione nella pagina [!UICONTROL Overview].

* Risoluzione di un problema che impediva ai clienti di selezionare un collegamento per il tracciamento dei clic.
* Risoluzione di un problema che consentiva a offerte duplicate di apparire nel rapporto livello dell&#39;offerta.
* Risoluzione di un problema che impediva l’inserimento di elementi mbox.
* Risoluzione di un problema che impediva il funzionamento delle conversioni dei clic sul collegamento.
* Risolto un errore di conversione del tracciamento dei clic che negava `target="_blank" functions.`
* Risoluzione di un problema in cui il tracciamento dei clic causava la navigazione fuori dalla pagina.

### Adobe [!DNL Target] 14.6.1 (25 giugno 2014) {#section_A520F01EEE0A4C2CBB3F2A37E6DD6F83}

Questa versione include le seguenti nuove funzionalità:

>[!NOTE]
>
>Alcune funzionalità in questa versione sono disponibili solo come parte della soluzione [!DNL Target Premium].

<table id="table_A2A978B157D54E17BD7366ADC04C8FC9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="keyword"> Automated Personalization (Target Premium) </span> </td> 
   <td colname="col2"> <p> <span class="keyword"> Automated Personalization</span> fornisce algoritmi di apprendimento automatico avanzati per distribuire esperienze personalizzate e migliorare i tassi di conversione per le esperienze digitali. </p> <p> <p>Nota:<span class="keyword"> Automated Personalization</span> è disponibile come parte della soluzione <span class="keyword">Target Premium</span>. Non è disponibile in <span class="keyword">Target Standard</span> senza una licenza <span class="keyword">Target Premium</span>. Se disponi di una licenza <span class="keyword">Target Standard</span> o <span class="keyword">Target Premium</span>, utilizza la scheda <span class="keyword">Target</span> in Adobe Experience Cloud. </p> </p> <p>Puoi implementare un file sul sito per abilitare la capacità di fare clic su qualsiasi contenuto e quindi di creare visivamente e selezionare opzioni di contenuto aggiuntive per quell'area. Quindi, il sistema di modellazione determina automaticamente quale contenuto distribuire a ogni individuo sulla base di tutti i dati comportamentali del visitatore di cui il sistema dispone. In questo modo è possibile fornire a ogni visitatore un'esperienza personalizzata. L'addetto al marketing non ha bisogno di eseguire un test, di analizzare i risultati e infine di distribuire l'esperienza vincente, prima di ottenere l'incremento derivato dall'ottimizzazione. </p> <p> <span class="keyword"> Automated Personalization</span> fornisce: </p> 
    <ul id="ul_9EF654B10FFA46169EE2E033683BA82E"> 
     <li id="li_8D201BF8F37B4B2489D039A0340E065E">Due algoritmi di apprendimento automatico: 
      <ul id="ul_E1DF69071C9047EEA692B5EF01176E4B"> 
       <li id="li_1F4ED87AB6D044C1BE04D0360F42D56F"> <span class="keyword"> Foresta casuale </span> </li> 
       <li id="li_BE6388BA88684501B741713CECF5AE91"> <span class="keyword"> Modello di varianza residua </span> </li> 
      </ul> </li> 
     <li id="li_36E18493A95B4C96BFA3133CDFD8826A">Implementazione mediante singola riga di codice con modifica del contenuto WYSIWYG </li> 
     <li id="li_79B1878FA64A40E88A973C57C39FC5FF">L'obiettivo principale per l'attività utilizza attualmente la Metrica di conversione. Entrate e coinvolgimento sono disponibili come metriche aggiuntive. </li> 
     <li id="li_FE94A79767EF4534BD02B2AFD7E27E1B">Connessione al <span class="keyword">Profilo di marketing principale</span> per una raccolta senza soluzione di continuità dei dati comportamentali anticipati dei visitatori </li> 
    </ul> <p>Consulta <a href="/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local">Automated Personalization</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Attività multiple su un'unica pagina </td> 
   <td colname="col2"> <p>Il contenuto da più attività di Target Standard può essere distribuito a una pagina da una chiamata al server di <span class="keyword">Target</span>. </p> <p> <p>Nota: questo non influisce sulla priorità di valutazione di Target Classic. </p> </p><p>Per informazioni sul modo in cui Target determina l’esperienza da visualizzare quando più attività sono impostate per il targeting della stessa posizione su una pagina, consulta <a href="/help/main/c-activities/priority.md#concept_1780C11FEA57440499F0047DD6900E0F" format="dita" scope="local">Priorità.</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Problemi risolti**

* È stato risolto un problema a causa del quale alcuni tipi di pubblico condivisi ed eliminati venivano comunque visualizzati nell&#39;elenco [!UICONTROL Audiences].
* È stato corretto un errore che causava la visualizzazione di una finestra di dialogo [!UICONTROL Save] imprevista in Internet Explorer 10.
* Correzione di un errore di sincronizzazione durante il salvataggio di una campagna.
* Risoluzione di un problema per cui il pubblico per un&#39;esperienza non veniva visualizzato nei rapporti.
* Risoluzione di un problema che impediva la corrispondenza tra elenchi delle metriche in [!DNL Target] e [!DNL Analytics].

* Risoluzione di un problema che consentiva agli utenti di specificare come mbox globale una mbox utilizzata da [!DNL Target Standard] per la distribuzione dei contenuti HTML. Questo utilizzo della mbox globale influisce negativamente sulla distribuzione dei contenuti e sulla capacità di [!DNL Target Classic] di distribuire più campagne a una singola pagina in una singola richiesta.

* Risoluzione di un problema per cui elementi rimossi continuavano a essere visualizzati.

### Adobe [!DNL Target] Standard 14.5 (28 maggio 2014) {#section_530EAB9376414D4989CA0740361DDCC2}

Questa versione include le seguenti correzioni di bug:

* Risoluzione di un problema per cui l&#39;anteprima di un&#39;esperienza non funzionava come previsto.

### Adobe [!DNL Target] Standard 1.7 (28 aprile 2014) {#section_2C2B9B6299ED4F48A3B983AB015F381A}

[Webinar su Target Standard versione 1.7](https://my.adobeconnect.com/p1oabaz3cxi/)

Questa versione include le seguenti nuove funzionalità:

<table id="table_11CD9EE0C9534FF19C9154784C4BFCF0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Reportistica migliorata basata su Adobe Analytics per Adobe Target </td> 
   <td colname="col2"> I clienti di Adobe Analytics possono selezionare Analytics come origine per la generazione di rapporti predefinita durante il <a href="/help/main/c-activities/t-test-ab/t-test-create-ab/create-a4t.md#task_FE48F7B077C44A5BA015B087428412EF" format="dita" scope="local">processo di configurazione dei test</a>. Non è più necessario selezionare tutte le metriche di successo o i tipi di pubblico che desideri utilizzare per filtrare i risultati. Nella funzione di reporting, puoi selezionare qualsiasi metrica di successo o segmento di pubblico definito in Analytics e applicarlo retroattivamente, per un filtraggio esteso e un'analisi drill-down dei risultati di ottimizzazione. <p> <p>Nota: per richiedere l'accesso a questa funzionalità, visitare <a href="https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y" format="http" scope="external"> https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y </a>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Tipi di pubblico in tempo reale con profilo marketing principale </td> 
   <td colname="col2"> Puoi sfruttare il profilo marketing principale che unifica gli ID visitatori e i dati in un unico profilo utilizzabile nelle diverse soluzioni. Una casella di controllo nel processo di creazione dei segmenti in Adobe Analytics consente di rendere disponibile il segmento nella libreria dei tipi di pubblico personalizzati di Adobe Target. Un segmento creato in Analytics o Audience Manager può essere utilizzato per il targeting dei visitatori in Target. <p> <p>Nota: per richiedere l'accesso a questa funzionalità, visitare <a href="https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y" format="http" scope="external"> https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y </a>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Tipo di attività targeting delle esperienze </td> 
   <td colname="col2"> <a href="/help/main/c-activities/t-experience-target/experience-target.md#task_A53DF336CB9F4D7BB87EF2106099EFC4" format="dita" scope="local"> Eseguire il targeting di esperienze diverse per tipi di pubblico diversi in una sola attività.</a> <p> <p>Nota: questo fornisce funzionalità simili alla campagna Pagina di destinazione in Target Advanced. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Test multipagina </td> 
   <td colname="col2"> <p> <a href="/help/main/c-experiences/c-visual-experience-composer/temtest.md#task_2539D51A18044F82B0D9895636546781" format="dita" scope="local">Scegli di eseguire un test o un'attività con targeting in una serie di pagine web</a>. Ora puoi distribuire test a ogni pagina di prodotto, o modificare la navigazione globale in ogni pagina del sito. Utilizza un semplice generatore di regole per specificare il gruppo di pagine interessato. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Correzioni di bug**

Questa versione include le seguenti correzioni di bug:

* Risoluzione di un problema che impediva la compressione di `target.js` da parte di Edge.
* Risoluzione di un problema nei rapporti che impediva la visualizzazione del conteggio di conversione nella riga Attività per le attività A/B.
* Risoluzione di un problema per cui un rapporto non più visualizzato dopo un&#39;esperienza con dati veniva eliminato.
* Creazione di una soluzione alternativa per ignorare in modo automatico un difetto della versione 34 di Chrome che impediva la visualizzazione di pagine con contenuti misti. È ora possibile utilizzare tutte le versioni di Chrome.

**Problemi noti**

Questa versione include i seguenti problemi noti. Questo problema verrà risolto in un prossimo aggiornamento.

* Il tracciamento dei clic non funziona sugli elementi che sono stati ridisposti con il Compositore esperienza visivo. Evita di configurare il tracciamento dei clic su elementi ridisposti fino alla correzione di questo bug.
* Se i tipi di pubblico Geo vengono creati in Target Standard quando la geolocalizzazione è disabilitata in Target Advanced, si verifica un errore di sincronizzazione.
* Non è possibile scambiare un&#39;immagine quando all&#39;immagine viene fatto riferimento in CSS.
* Se scambi un&#39;immagine, e quindi la ridimensioni, le esperienze nell&#39;Editor esperienze non vengono visualizzate correttamente.

### Adobe [!DNL Target] Standard 1.6 (17 marzo 2014) {#section_DB1319CDD8944F6FB749E525EB551017}

Questa versione include le seguenti nuove funzionalità:

| Funzione | Descrizione |
|---|---|
| Versioni localizzate disponibili | Target Standard è stato localizzato in francese, tedesco, giapponese e spagnolo |
| Implementazione semplificata | Target Standard è stato migliorato per facilitare l&#39;implementazione per gli utenti esistenti di Target Advanced. La nuova implementazione utilizza le mbox globali esistenti per eseguire le attività di Adobe Standard. |

**Correzioni di bug**

Questa versione include le seguenti correzioni di bug:

* Risoluzione di un problema che, in determinati casi, causava il mancato funzionamento di Rimuovi elemento e Modifica HTML.

**Problemi noti**

Questa versione include i seguenti problemi noti. Questo problema verrà risolto in un prossimo aggiornamento.

* Il vincitore funziona solo in base a un obiettivo e non si modifica in base alle metriche selezionate.
* Il tracciamento dei clic non funziona sugli elementi che sono stati ridisposti con il Compositore esperienza visivo. Evita di configurare il tracciamento dei clic su elementi ridisposti fino alla correzione di questo bug.
* Se i tipi di pubblico Geo vengono creati in Target Standard quando la geolocalizzazione è disabilitata in Target Advanced, si verifica un errore di sincronizzazione.
* Non è possibile scambiare un&#39;immagine quando all&#39;immagine viene fatto riferimento in CSS.
* Il nuovo tipo di mbox viztarget non funziona con l&#39;integrazione di Target Advanced/Adobe Analytics v4, la versione corrente.
* Nei rapporti, il formato numerico e la valuta indicati nel grafico non corrispondono alla tabella se nelle impostazioni internazionali è impostato un valore diverso dal dollaro.
* Nella casella di ricerca Tipi di pubblico non sono supportati caratteri non ASCII.
* Per gli utenti delle versioni spagnola e giapponese, il salvataggio di un&#39;attività dopo aver impostato le date di inizio e di fine determina un errore. È consigliabile salvare senza impostare date di inizio e di fine, e quindi di attivare e interrompere l&#39;attività dalla Panoramica Attività o dalla pagina Elenco attività quando necessario.

### Adobe [!DNL Target] Standard 1.5 (25 febbraio 2014) {#section_5E9E3DDBCB82494AA62A21AC9282063F}

Questa versione include le seguenti nuove funzionalità:

<table id="table_67115780726F48859DC8E46E34567DC3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Conflitti tra attività </td> 
   <td colname="col2"> <p> In Target Standard è ora incluso un elenco di collisioni tra attività. Un conflitto tra attività si verifica quando più attività sono configurate per distribuire contenuto alla stessa pagina. Se si verifica una collisione tra attività, è possibile che sulla pagina non venga visualizzato il contenuto atteso, in quanto è stata immessa una diversa attività. </p> <p> Sono indicate tutte le attività che fanno riferimento allo stesso URL, indipendentemente dall'eventuale targeting di un pubblico in ogni attività. </p> <p> Se l'attività include collisioni, la scheda <span class="wintitle">Collisioni</span> è disponibile nella pagina di panoramica dell'attività. Apri questa scheda per un elenco delle attività potenzialmente in collisione. Fai clic su un’attività nell’elenco per visualizzarne la pagina di panoramica. </p> <p>Vedere <a href="/help/main/c-experiences/c-visual-experience-composer/activity-collisions.md#concept_0BC6B929592744DFA7DA01FF4F91052E" format="dita" scope="local"> conflitti tra attività </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Nuove opzioni di targeting: Profilo, Utente </td> 
   <td colname="col2"> Ora puoi eseguire il targeting dei parametri di profilo e utente. Vedi <a href="/help/main/c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271" format="dita" scope="local"> tipi di pubblico </a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Inserimento di elementi </td> 
   <td colname="col2"> <p>Ora puoi aggiungere qualsiasi tipo di elemento alla pagina, oltre a modificare il contenuto esistente. Puoi aggiungere testo, codice, elenchi e così via per creare esperienze diverse da testare. </p> <p>Consulta <a href="/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local">Opzioni del Compositore esperienza visivo.</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

Questa versione include i seguenti problemi noti. Questo problema verrà risolto in un prossimo aggiornamento.

* Il vincitore funziona solo in base a un obiettivo e non si modifica in base alle metriche selezionate.
* Il tracciamento dei clic non funziona sugli elementi che sono stati ridisposti con il Compositore esperienza visivo. Evita di configurare il tracciamento dei clic su elementi ridisposti fino alla correzione di questo bug.
* Se i tipi di pubblico Geo vengono creati in Target Standard quando la geolocalizzazione è disabilitata in Target Advanced, si verifica un errore di sincronizzazione.
* Non è possibile scambiare un&#39;immagine quando all&#39;immagine viene fatto riferimento in CSS.

### Adobe [!DNL Target] Standard 1.4 (20 gennaio 2014) {#section_CD27AEE32B4F40BDAB422711B96739A5}

Questa versione include le seguenti nuove funzionalità e miglioramenti:

<table id="table_9E303FF0CD954795A29369A6D4166DB5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Incremento stimato delle entrate </td> 
   <td colname="col2"> <p>Con Target puoi stimare l’incremento dei ricavi potenziali se tutti gli utenti visualizzano l’esperienza vincente. </p> <p>Questa stima calcola il volume dell'incremento ottenuto dall'esperienza vincente e il numero totale di visitatori per tutta la durata del test, mostrando l'incremento potenzialmente realizzabile se ogni visitatore visualizza l'esperienza vincente, in caso di continuità delle tendenze come durante il test. </p> <p> La precisione della stima dipende da una serie di fattori, inclusi i dati previsionali basati sulla continuità delle tendenze correnti. Si tratta di stime basate sulle prestazioni passate e non devono essere utilizzate a scopo di orientamento finanziario. I risultati futuri possono variare. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Annulla/Ripristina </td> 
   <td colname="col2"> <p>Consente di annullare le modifiche apportate alle attività durante una sessione di modifica. Inoltre, puoi ripristinare le modifiche annullate. </p> <p>Consulta <a href="/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local">Opzioni del Compositore esperienza visivo.</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sposta elemento </td> 
   <td colname="col2"> <p>Consente di spostare elementi nella pagina. A differenza di Ridisponi, l'opzione Sposta non muove gli altri elementi per fare spazio all'elemento spostato. Utilizza i tasti freccia per perfezionare lo spostamento. </p> <p>Consulta <a href="/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local">Opzioni del Compositore esperienza visivo.</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ridimensiona elemento </td> 
   <td colname="col2"> <p>Consente di ridimensionare un elemento nella pagina. Quando selezioni Ridimensiona, una maniglia viene visualizzata in un angolo dell'elemento e consente di trascinare tale angolo per ridimensionare. </p> <p>Consulta <a href="/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local">Opzioni del Compositore esperienza visivo.</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Eseguire il targeting di una posizione durante la configurazione di un pubblico </td> 
   <td colname="col2"> <p>Durante la creazione di un pubblico, puoi selezionare una posizione (mbox) e specificarne i parametri. </p> <p>Vedere <a href="/help/main/c-target/c-audiences/create-audience.md#task_1D507519D3AD4390B507F188BD294DC1" format="dita" scope="local"> Creazione di un nuovo pubblico </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Collegamenti di anteprima (miglioramento) </td> 
   <td colname="col2"> <p>I collegamenti di anteprima funzionano come previsto. </p> </td> 
  </tr> 
 </tbody> 
</table>

Questa versione include le seguenti correzioni:

* Risoluzione dei problemi che impedivano la visualizzazione dei collegamenti di anteprima come previsto.

Questa versione include i seguenti problemi noti. Questi problemi verranno risolti in un prossimo aggiornamento.

* Se Incremento stimato è abilitato in Target Standard e Target Advanced è impostato su un fuso orario diverso rispetto al browser dell&#39;utente, è possibile che la visualizzazione del valore delle entrate previste nell&#39;elenco Attività o nella barra di stato Rapporti richieda fino a un giorno. Dato che in Visualizzazione rapporti viene utilizzata la data ma non l&#39;ora, i dati vengono visualizzati ma non per l&#39;incremento proiettato.
* Il tracciamento dei clic non funziona sugli elementi che sono stati ridisposti con il Compositore esperienza visivo. Evita di configurare il tracciamento dei clic su elementi ridisposti fino alla correzione di questo bug.
* Se i tipi di pubblico Geo vengono creati in Target Standard quando la geolocalizzazione è disabilitata in Target Advanced, si verifica un errore di sincronizzazione.
* Non è possibile scambiare un&#39;immagine quando all&#39;immagine viene fatto riferimento in CSS.

## Versione 2013

### Adobe [!DNL Target] Standard 1.3 (19 novembre 2013) {#section_D633ACA56FA941648219EB3748D814EC}

Questa versione include le seguenti nuove funzionalità e miglioramenti:

| Funzione | Descrizione |
|---|---|
| Geotargeting | Consente di eseguire il targeting per paese, stato, città, CAP o DMA. |
| Utilizza il Compositore esperienza visivo per ridisporre gli elementi. | Puoi ridisporre gli elementi figli all&#39;interno del relativo elemento padre utilizzando il Compositore esperienza visivo. |
| Visualizza l&#39;anteprima direttamente sul sito. | Dopo aver salvato un&#39;attività, puoi visualizzarla in anteprima direttamente sul sito, anche se l&#39;attività non è live. Questo consente di visualizzarne l&#39;aspetto senza distribuirla attraverso iFrame. Puoi copiare i collegamenti in ogni esperienza di test per visualizzare tali esperienze nel browser o per inviarle a membri del gruppo per la visualizzazione. Coloro che visualizzano queste pagine non saranno conteggiati nei rapporti. |

Questa versione include le seguenti correzioni:

* Risoluzione di un problema in cui la metrica di tracciamento dei clic non veniva eliminata da un&#39;attività se l&#39;URL esperienza era stato reimpostato.
* Risoluzione di un problema in Compositore esperienze che causava per un attimo la visualizzazione dell&#39;esperienza predefinita prima del nuovo contenuto alla navigazione tra le esperienze.

Questa versione include i seguenti problemi noti. Questi problemi verranno risolti in un prossimo aggiornamento.

* Se i tipi di pubblico Geo vengono creati in Target Standard quando la geolocalizzazione è disabilitata in Target Advanced, si verifica un errore di sincronizzazione.
* Non è possibile scambiare un&#39;immagine quando all&#39;immagine viene fatto riferimento in CSS.
* Il tracciamento dei clic non funziona sugli elementi che sono stati ridisposti con il Compositore esperienza visivo. Evita di configurare il tracciamento dei clic su elementi ridisposti fino alla correzione di questo bug.
* Gli utenti non possono selezionare l&#39;azione **[!UICONTROL Remove]** per il contenuto incluso in una mbox.

### Adobe [!DNL Target] Standard 1.2 (31 ottobre 2013) {#section_420B5E910D7341AA8DB059C8E1071D53}

Questa versione presenta quattro problemi noti. Questi problemi verranno risolti in un prossimo aggiornamento.

* In alcuni cluster, la modifica di un&#39;offerta riutilizzabile potrebbe non riflettersi sul sito del cliente per le attività che la utilizzano al di fuori di una mbox.
* Le immagini scambiate nell&#39;area di una pagina non controllata da una mbox potrebbero causare un errore 404.
* Quando crei un nuovo pubblico, o ne modifichi e salvi uno esistente, esso non viene visualizzato nell&#39;elenco dei tipi di pubblico fino all&#39;aggiornamento della schermata o alla ricerca del pubblico.
* Un&#39;offerta HTML eliminata da Target Standard non viene eliminata da Target Advanced.

Questa versione include le seguenti correzioni e miglioramenti:

* Risoluzione dei molteplici problemi che causavano la mancata sincronizzazione di alcune attività ed esperienze con Target Advanced.
* Risoluzione di un problema per cui [!DNL target.js] sposta altri script fuori dalla sezione `<head>` di una pagina.

* Risoluzione di un problema che causava la copia di alcune risorse di riferimento alla copia di un&#39;attività.
* Risoluzione di un problema che causava il mancato aggiornamento del contenuto di un&#39;offerta immagine aggiornata in Scene7 e Target Advanced.
* Risoluzione di un problema in cui l&#39;applicazione di un filtro di ricerca eliminava i tipi di pubblico selezionati in &quot;Audiences for Reporting&quot; (Tipi di pubblico per generazione di rapporti).
* Grafici migliorati: impostazione predefinita su risultati orari quando un test è live da meno di due giorni.
* Risoluzione di un problema che causava la mancata copia di un&#39;attività non sincronizzata.
* Aggiunta funzionalità di input da tastiera ai menu a discesa per la posizione.
* Miglioramento del messaggio di errore visualizzato all&#39;eliminazione di un&#39;offerta utilizzata in un&#39;attività.

### Adobe [!DNL Target] Standard 1.1 (18 ottobre 2013) {#section_79FA6A61D2284D41A34F00014A342F07}

Questa versione include le seguenti correzioni e miglioramenti:

* Risoluzione di un problema che causava la mancata sincronizzazione dell&#39;attività al primo tentativo di sincronizzazione dopo l&#39;aggiunta di esperienze valide a un&#39;attività parziale.
* Risoluzione di un problema che provocava un errore 500 nel rapporto di riepilogo dopo l&#39;eliminazione e l&#39;aggiunta di un&#39;esperienza.
* Risoluzione di un problema che causava dati visitatore non precisi quando un visitatore visualizzava più esperienze.
* L&#39;ora di inizio e di fine dell&#39;attività ora viene sincronizzata correttamente tra Standard e Advanced.
* Miglioramento della visualizzazione dei contenuti misti.
* Risoluzione di un problema che causava il malfunzionamento del Compositore esperienza visivo se JavaScript nel codice HTML sostituisce la definizione del browser dell&#39;oggetto JSON.
* Risoluzione di un problema per cui il numero di attività visualizzato non era corretto in caso di ordinamento in base allo stato.
* Risoluzione di un problema per cui lo spazio vuoto nel campo Obiettivo non veniva convalidato correttamente.
* Risoluzione di un problema che causava la creazione di offerte multiple per un singolo in Advanced in caso di scambio dell&#39;immagine.
* Risoluzione di un problema che causava il mancato funzionamento della ricerca sulle immagini nel selettore contenuto.
* Correzione di un difetto che invertiva l&#39;ordinamento dell&#39;elenco delle attività in caso di ordinamento per Nome o Stato.
* Risoluzione di un problema per cui le offerte anonime non venivano eliminate quando non più utilizzate in un&#39;attività.
* Correzione di un difetto che causava la visualizzazione di un nome di esperienza non corretto in una scheda condivisa durante la modifica di un&#39;attività.
* Correzione di un difetto cui un&#39;offerta immagine aggiornata non aggiornava correttamente il contenuto in Scene7 e Target Advanced.
* Risoluzione di un problema in cui la copia di una risorsa immagine includeva risorse collegate a Scene7 che non avrebbero dovuto essere copiate.
