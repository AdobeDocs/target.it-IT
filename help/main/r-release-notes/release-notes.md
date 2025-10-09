---
keywords: note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti;aggiornamenti;aggiornamenti correnti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
short-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: f0536e466d59fc4e3cccd61c25b7fe7f48f03954
workflow-type: tm+mt
source-wordcount: '4858'
ht-degree: 7%

---

# Note sulla versione (corrente) di [!DNL Target]

Esplora le funzioni, i miglioramenti e le correzioni più recenti in [!DNL Adobe Target]. Queste note sulla versione descrivono anche gli aggiornamenti alle API [!DNL Target], agli SDK, a [!DNL Adobe Experience Platform Web SDK], at.js e ad altri componenti della piattaforma, se applicabili.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## Aggiornamenti urgenti da conoscere {#time-sensitive}

[!BADGE Importante]{type=Informative}

Per gli aggiornamenti sensibili al tempo relativi a [!DNL Adobe Target] e alla tua implementazione, [!DNL Adobe] fornisce note dettagliate sulla versione e documentazione tramite [!UICONTROL Experience League]. Di seguito sono riportate alcune caratteristiche principali relative all’implementazione:

### La versione dell&#39;interfaccia utente [!DNL Target] è deprecata

Per ulteriori informazioni, vedere [[!DNL Target] Domande frequenti sull&#39;aggiornamento dell&#39;interfaccia utente](/help/main/c-intro/updated-ui-faq.md).

## [!DNL Target Standard/Premium] 25.9.3 (30 settembre 2025)

Questa versione include i miglioramenti e le correzioni seguenti.

+++[!UICONTROL Audiences]

* **Le regole di esclusione del pubblico non venivano visualizzate correttamente come inclusione nell&#39;interfaccia utente di [!DNL Target].** i tipi di pubblico configurati con regole di esclusione venivano visualizzati come inclusi durante la modifica del targeting all&#39;interno di un&#39;attività. Anche se la logica di esclusione è stata applicata correttamente durante l’esecuzione, l’interfaccia utente non è riuscita a riflettere la regola in modo preciso, omettendo l’etichetta &quot;esclusione&quot;. L&#39;interfaccia utente di [!DNL Target] visualizza ora correttamente le regole di esclusione sia nella configurazione del pubblico che nei flussi di lavoro di targeting, garantendo chiarezza e coerenza per la configurazione della campagna. (TGT-53808)
* **La sezione [!UICONTROL Targeting] non indica che è stata impostata una regola di pubblico da escludere.** tipi di pubblico configurati con logica di esclusione non venivano visualizzati correttamente come inclusi nella sezione [!UICONTROL Targeting] dell&#39;interfaccia utente per la creazione di attività. Sebbene il backend abbia applicato correttamente la regola di esclusione, l’interfaccia utente non è riuscita a rappresentarla visivamente, omettendo l’etichetta &quot;Escludi&quot; e creando confusione durante la configurazione della campagna. Nella sezione [!UICONTROL Targeting] sono ora visualizzate chiaramente le regole di esclusione, garantendo la coerenza tra la configurazione del pubblico e la visualizzazione del targeting. (TGT-53809)

+++

+++Localizzazione

* **È stata risolta un&#39;incoerenza terminologica nella traduzione in cinese semplificato della visualizzazione Dettagli completi.**
In precedenza, il termine &quot;Dettagli&quot; veniva erroneamente tradotto come &quot;详情&quot; nella lingua cinese semplificato (zh_CN), violando le linee guida terminologiche stabilite. Questo è stato corretto in &quot;详细信息&quot; per garantire la coerenza con il database terminologico. (TGT-53741)

+++

+++[!UICONTROL Recommendations]

* **Impossibile individuare e selezionare le caselle dei consigli nel Compositore esperienza visivo.** Dopo aver aggiunto un&#39;offerta di consigli nel (VEC), facendo clic sulla modifica nel pannello a sinistra non è stato possibile evidenziarla o scorrere fino alla casella di consiglio corrispondente nella pagina. Questo rendeva difficile individuare e modificare l’offerta, soprattutto se nascosta sotto i selettori o con uno stile minimo. Facendo clic su una modifica dei consigli, ora viene evidenziato e scorre correttamente l’elemento associato, migliorando l’usabilità e l’efficienza nella modifica del processo aggiornato di creazione delle attività. (TGT-52571)
* **I selettori di consigli non sono stati riscritti correttamente dopo il salvataggio di un&#39;attività.** Quando si aggiungeva un consiglio a un elemento nel Compositore esperienza visivo, il selettore era inizialmente corretto, ma dopo aver salvato e riaperto l&#39;attività, è stato modificato in un selettore generico. I tentativi di ripristinare manualmente il selettore originale hanno generato errori di convalida. I selettori per consigli ora persistono accuratamente dopo il salvataggio, garantendo un targeting e una modificabilità affidabili nel processo aggiornato di creazione delle attività. (TGT-53709)
* **Impossibile modificare il contenuto dei criteri durante la modifica di un&#39;attività esistente.** Durante la modifica di un&#39;attività, la sezione del contenuto [!UICONTROL Criteria] è apparsa disabilitata, con i pulsanti disattivati e che non rispondono. Questo problema è stato risolto assicurandosi che [!UICONTROL Criteria] configurazioni siano completamente modificabili durante gli aggiornamenti dell&#39;attività. I clienti possono ora modificare il contenuto di [!UICONTROL Criteria] senza dover cambiare le selezioni o utilizzare soluzioni alternative, migliorando la flessibilità e l&#39;usabilità nel processo aggiornato di creazione delle attività. (TGT-53812)
* **Impossibile modificare i criteri all&#39;interno di un&#39;attività.** Le opzioni [!UICONTROL Edit Criteria] e [!UICONTROL Remove Criteria] sono state disabilitate durante l&#39;accesso ai criteri dall&#39;interno di un&#39;attività. Tuttavia, è possibile modificare gli stessi criteri tramite la scheda [!UICONTROL Recommendations]. I criteri sono ora completamente modificabili sia dal flusso di lavoro di modifica delle attività che dalla scheda [!UICONTROL Recommendations], garantendo un&#39;esperienza di modifica coerente ed efficiente. (TGT-53814)

+++

+++[!UICONTROL Reports]

* **La generazione di offerte ad hoc nelle attività A[!UICONTROL utomated Personalization] ha causato incongruenze nei rapporti.** L&#39;utilizzo della funzionalità Genera offerte ad hoc nelle attività di [!UICONTROL Automated Personalization] (AP) ha portato a rapporti non accurati. In particolare, gli ID offerta venivano riutilizzati tra le posizioni, causando l’erronea attribuzione o la sovrascrittura dei dati di reporting. Le offerte ad hoc ora vengono generate con identificatori distinti per posizione, garantendo un tracciamento e un reporting accurati per tutte le esperienze configurate. (TGT-53757)
* **Impossibile caricare i report attività a causa di un errore JavaScript.** I clienti hanno riscontrato un messaggio di errore durante l&#39;accesso alla scheda [!UICONTROL Reports] per alcune attività. L&#39;errore è stato causato da un&#39;eccezione JavaScript: impossibile leggere le proprietà di non definito (lettura di &#39;indexOf&#39;), attivato durante la chiamata GraphQL `getAnalyticsReportSummary`. I rapporti ora vengono caricati correttamente e la gestione degli errori è stata migliorata per evitare errori simili nel flusso di lavoro aggiornato per la creazione di attività. (TGT-53797)
* **Si è verificato un arresto anomalo dei report dopo l&#39;interazione con la barra di scorrimento.** Facendo clic sulla barra di scorrimento nella scheda [!UICONTROL Reports] si è verificato un arresto anomalo della pagina, accompagnato da un errore di JavaScript:
  `SyntaxError: Failed to execute 'querySelector' on 'Element': '[data-key="a-currentcopy"hiretalent""]' is not a valid selector.` I report ora vengono caricati e scorrono correttamente senza generare errori o arresti anomali. (TGT-53828)
* **Nei rapporti non è stata visualizzata la metrica principale.** La metrica principale, configurata come metrica di conversione utilizzando una mbox, non era presente nei rapporti di attività. La ricerca per nome metrica o nome mbox non ha prodotto risultati, impedendo la visibilità nei dati delle prestazioni chiave. Le metriche primarie ora vengono visualizzate correttamente nella scheda [!UICONTROL Reports], garantendo un tracciamento e un&#39;analisi accurati delle prestazioni della campagna. (TGT-53773)
* **La scheda [!UICONTROL Reports] nell&#39;interfaccia utente aggiornata si è bloccata durante l&#39;interazione con la barra di scorrimento orizzontale.** La visualizzazione [!UICONTROL Reports] si è bloccata in modo intermittente con un errore &quot;Si è verificato un errore&quot; quando si utilizza la barra di scorrimento orizzontale per accedere alle metriche fuori visualizzazione. La barra di scorrimento ora funziona in modo affidabile, consentendo ai clienti di visualizzare e analizzare tutte le metriche senza necessità di soluzioni quali ingrandire o utilizzare lo scorrimento con spostamento. (TGT-53824)

+++

+++[!UICONTROL Visual Experience Composer] (VEC)

* **Se si fa clic su breadcrumb nel Compositore esperienza visivo, il menu Modifica non veniva visualizzato in modo coerente.**
Quando si selezionano gli elementi di HTML tramite le breadcrumb nel Compositore esperienza visivo, il menu Modifica a intermittenza non viene visualizzato o scompare rapidamente, rendendo la selezione degli elementi inaffidabile. Il menu Modifica ora viene visualizzato in modo coerente quando si naviga tramite breadcrumb, migliorando il flusso di lavoro di selezione degli elementi nel processo aggiornato di creazione delle attività. (TGT-52873)
* **Impossibile visualizzare in modo intermittente il menu di scelta rapida nel Compositore esperienza visivo.** Il menu di scelta rapida nell&#39;interfaccia utente VEC aggiornata non veniva visualizzato in modo coerente quando si faceva clic sugli elementi, rendendo difficile l&#39;accesso alle opzioni di modifica. Il menu di scelta rapida ora viene visualizzato in modo affidabile sulla selezione degli elementi, migliorando il flusso di lavoro di modifica e l’usabilità complessiva nel processo aggiornato di creazione delle attività. (TGT-53015)
* **Impossibile visualizzare il menu di scelta rapida per alcuni elementi nel Compositore esperienza visivo.** Il menu di scelta rapida non veniva visualizzato quando si selezionavano elementi specifici nel Compositore esperienza visivo aggiornato, rendendo difficile l&#39;applicazione delle modifiche. Il menu di scelta rapida ora viene visualizzato in modo coerente per tutti gli elementi supportati, migliorando l’affidabilità e la facilità d’uso dell’esperienza di modifica nel flusso di lavoro aggiornato per la creazione di attività. (TGT-53248)
* **Il menu di scelta rapida è scomparso al primo clic quando si utilizzano breadcrumb nel Compositore esperienza visivo.** La selezione di un elemento padre tramite le breadcrumb nel Compositore esperienza visivo ha causato la visualizzazione breve del menu di scelta rapida, che è quindi scomparso, rendendo difficile l&#39;accesso alle opzioni di modifica. Il menu di scelta rapida ora rimane visibile e funzionale durante la navigazione degli elementi attraverso le breadcrumb, migliorando l’affidabilità del flusso di lavoro di selezione degli elementi nel processo aggiornato di creazione delle attività. (TGT-53424)
* **Il menu di scelta rapida non è stato visualizzato per gli elementi di primo livello nel Compositore esperienza visivo.** La selezione di elementi di primo livello, ad esempio i tag `<div>` o `<main>`, tramite le breadcrumb nel Compositore esperienza visivo non ha attivato il menu di scelta rapida, impedendo ulteriori azioni di modifica. Il menu di scelta rapida ora viene visualizzato in modo coerente per tutti gli elementi supportati, inclusi i contenitori di primo livello, migliorando la flessibilità e l’usabilità del flusso di lavoro per la creazione di attività. (TGT-53770)
* **Impossibile modificare gli elementi in una pagina specifica nel Compositore esperienza visivo.** Impossibile selezionare o modificare alcuni elementi nella pagina nel Compositore esperienza visivo aggiornato. Questo problema era isolato in quella pagina e non interessava altre pagine all’interno dello stesso account. Tutti gli elementi della pagina ora sono selezionabili e modificabili come previsto, ripristinando la funzionalità completa nel flusso di lavoro per la creazione di attività. (TGT-53353)
* **È stato migliorato il flusso di lavoro durante la visualizzazione degli elementi figlio durante la selezione dell&#39;elemento nel Compositore esperienza visivo.** Per migliorare l&#39;usabilità e la precisione durante la creazione dell&#39;attività, il Compositore esperienza visivo visualizza ora gli elementi secondari quando si passa il puntatore del mouse su un elemento HTML principale o lo si seleziona. Questo miglioramento consente ai clienti di comprendere meglio la struttura della pagina e apportare modifiche più precise, semplificando il flusso di lavoro di modifica nell’interfaccia utente aggiornata. (TGT-53416)
* **Impossibile modificare gli elementi nelle attività esistenti utilizzando la barra delle modifiche.** Durante la modifica di attività create in precedenza, non è stato possibile attivare la barra di modifica per alcuni elementi della pagina, impedendo gli aggiornamenti. Questo problema è stato osservato principalmente nelle attività modificate ed era difficile riprodurlo in quelle di nuova creazione. La barra di modifica ora mostra in modo coerente e consente di modificare tutti gli elementi supportati, migliorando l’affidabilità e la facilità d’uso nel flusso di lavoro aggiornato per la creazione di attività. (TGT-53013)

+++

+++[!UICONTROL Workspaces]

* **La clonazione di un&#39;attività in un&#39;area di lavoro diversa ha provocato un errore di tipo &quot;Input utente non valido&quot;.** Il tentativo di clonare un&#39;attività da un&#39;area di lavoro a un&#39;altra ha restituito un errore: &quot;InvalidProperty.Json - Nome di proprietà non riconosciuto &#39;content&#39;.&quot; Questo problema è stato causato da una gestione non corretta dei metadati dell’attività durante il processo di clonazione. È ora possibile clonare correttamente le attività in più aree di lavoro senza attivare errori di convalida, garantendo flussi di lavoro di distribuzione delle attività più fluidi. (TGT-53731 e TGT-53736)

+++

## [!DNL Target Standard/Premium] 25.9.2 (22 settembre 2025)

Questa versione include le seguenti correzioni e miglioramenti:

**[!UICONTROL Audiences]**

+++Vedi i dettagli
* **È stato risolto un problema che impediva la copia delle attività a causa di ID di pubblico non validi.** I clienti che tentavano di copiare le attività nel processo di creazione attività aggiornato hanno riscontrato un errore causato da ID di pubblico non validi (ad esempio, -1752722444307). Questo problema di convalida del back-end impediva la duplicazione delle attività all’interno della stessa area di lavoro. Questo problema è stato risolto e le attività possono essere copiate correttamente senza errori relativi al pubblico. (TGT-53717)
* **È stato risolto un problema che causava la visualizzazione di errori di input utente non validi per i tipi di pubblico per sola attività nelle attività [!UICONTROL Automated Personalization] e nel modale [!UICONTROL Manage Content].** Clienti hanno riscontrato errori di input utente non validi durante la configurazione dei tipi di pubblico per sola attività nella finestra modale [!UICONTROL &#x200B; Manage Content] per le attività di Personalizzazione automatizzata. Questo problema si verificava nonostante il pubblico fosse stato precedentemente utilizzato correttamente. Le configurazioni del pubblico combinato ora vengono salvate correttamente senza attivare errori di convalida. (TGT-53749)

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
* **Tracciamento dei clic ripristinato per [!UICONTROL Recommendations] attività create nell&#39;interfaccia utente aggiornata.** È stato risolto un problema che impediva alle attività [!UICONTROL Recommendations] create nell&#39;interfaccia utente aggiornata di registrare il tracciamento dei clic, causando la mancata segnalazione di conversioni. Le attività create nell’interfaccia utente legacy hanno tracciato correttamente i clic e segnalato le conversioni come previsto. Questa correzione assicura che le attività Consigli create nell’interfaccia utente aggiornata includano ora gli attributi di tracciamento corretti, il ripristino dei rapporti di conversione e l’allineamento con le metriche A4T. (TGT-53287)
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
