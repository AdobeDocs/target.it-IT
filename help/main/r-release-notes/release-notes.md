---
keywords: note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti;aggiornamenti;aggiornamenti correnti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
short-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 1a5c47277bfd5eb1c90887728540bbc3b0433d77
workflow-type: tm+mt
source-wordcount: '3800'
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

## [!DNL Target Standard/Premium] 25.8.2 (14 agosto 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

**[!UICONTROL Activities]**

+++Vedi i dettagli
* **È stato risolto un problema relativo al caricamento delle attività nell&#39;interfaccia utente [!DNL Target] aggiornata**: è stato risolto un problema nell&#39;interfaccia utente [!DNL Target] aggiornata a causa del quale alcune attività non venivano caricate durante il tentativo di modifica. Questo problema causava la partenza degli utenti da una schermata di caricamento indefinita. Questo problema ha interessato più attività ed è stato segnalato come incoerente tra i clienti. Con questa correzione, le attività interessate ora vengono caricate correttamente, consentendo una modifica diretta e riducendo le interruzioni dei flussi di lavoro delle attività. (TGT-53209)
* **È stato corretto un errore di salvataggio nel processo di creazione attività a causa della convalida `optionLocalId`**: è stato risolto un problema nel processo di creazione attività che impediva ai clienti di salvare le modifiche a causa di un errore di convalida del back-end: `OptionLocalIdReferentialIntegrity.ABActivity - Invalid optionLocalIds:` Questo problema si verificava durante la modifica di elementi specifici all&#39;interno di un&#39;attività, causando un&#39;operazione di salvataggio non riuscita. La correzione assicura che `optionLocalId` riferimenti siano ora convalidati correttamente, consentendo ai clienti di salvare le attività senza incontrare questo errore. (TGT-53293)
* **È stato corretto un arresto anomalo nel processo di creazione attività causato da riferimenti di opzione non validi durante il passaggio da una pagina all&#39;altra**: è stato risolto un problema nel processo di creazione attività che causava l&#39;arresto anomalo dell&#39;interfaccia utente dopo il passaggio da una pagina all&#39;altra tre volte durante la modifica. L&#39;arresto anomalo è stato attivato da riferimenti di opzione non validi, causando errori della console quali &quot;Impossibile trovare l&#39;opzione con localId &#39;7&#39;.&quot; Con questo aggiornamento, i clienti possono passare da una pagina all’altra e applicare le modifiche senza incontrare errori o interruzioni del sistema. (TGT-53295)
* **È stato corretto un errore di salvataggio nel processo di creazione attività causato da un input utente non valido durante la modifica delle esperienze**: è stato risolto un problema nel processo di creazione attività a causa del quale i clienti non potevano salvare le modifiche apportate a un&#39;attività a causa di un errore di input utente non valido. L’errore si è verificato durante la modifica delle esperienze nell’interfaccia utente aggiornata, impedendo il commit degli aggiornamenti. L’attività ora può essere salvata correttamente, consentendo ai clienti di modificarla e pubblicarla senza interruzioni. (TGT-53267)
* **È stato risolto un problema di caricamento nel processo di creazione attività che impediva la modifica nell&#39;interfaccia utente aggiornata**: è stato risolto un problema nel processo di creazione attività a causa del quale i clienti non potevano modificare le attività nell&#39;interfaccia utente aggiornata a causa di una schermata di caricamento continuo. Ora i clienti possono aprire e modificare le attività senza riscontrare errori di caricamento. (TGT-53415)
* **È stato risolto un problema relativo ai requisiti di esperienza nel processo di creazione attività per le attività di Personalizzazione automatizzata nell&#39;interfaccia utente aggiornata**: è stato risolto un problema nel processo di creazione attività in cui le attività di [!UICONTROL Automated Personalization] (Personalizzazione automatizzata) richiedevano due posizioni invece di due esperienze nell&#39;interfaccia utente aggiornata. Questo comportamento ha bloccato i casi di utilizzo in cui i clienti configuravano una singola posizione con più offerte, precedentemente supportate. Il requisito è stato corretto per corrispondere alla funzionalità originale, consentendo ai clienti di procedere con le attività di Personalizzazione automatizzata utilizzando due esperienze indipendentemente dal conteggio delle posizioni. (TGT-53429)
* **È stato corretto il comportamento del campo degli elementi tracciati in modalità Traccia clic per evitare input non salvati e migliorare la chiarezza**: è stato risolto un problema nel processo di creazione attività a causa del quale il campo [!UICONTROL Tracked Element] in modalità [!DNL Click Track] era modificabile ma non manteneva il nome immesso, generando confusione per i clienti. Il campo è ora disabilitato per impedire l’input non salvato e la denominazione degli elementi selezionati è stata chiarita per migliorare la configurazione dell’obiettivo e la precisione del tracciamento.** (TGT-53458)
* **È stato risolto un problema nel processo di creazione attività che impediva la denominazione dei componenti tracciati in modalità [!UICONTROL Click Track]**: è stato risolto un problema nel processo di creazione attività a causa del quale i clienti non potevano assegnare un nome ai componenti tracciati in modalità [!UICONTROL Click Track]. Dopo aver immesso un nome, il campo appariva modificabile ma non manteneva l’input; in modalità di modifica venivano utilizzate per impostazione predefinita etichette generiche come &quot;OBIETTIVO PRIMARIO 0&quot;. Il campo degli elementi tracciati è ora disabilitato e il comportamento di denominazione è stato chiarito per migliorare la configurazione degli obiettivi e la precisione del tracciamento. (TGT-51396)

+++

**Frammenti esperienza (XF)**

+++Vedi i dettagli
* **È stato risolto un problema nel processo di creazione attività che consentiva la modifica non intenzionale da parte di HTML dei frammenti esportati da AEM**: è stato risolto un problema nel processo di creazione attività che consentiva ai clienti di modificare il HTML di [!DNL Experience Fragments] (XF) esportati da [!DNL Adobe Experience Manager] (AEM) in [!DNL Target]. Questo comportamento non era intenzionale, poiché gli XF dovrebbero rimanere bloccati per la modifica dopo la pubblicazione da AEM. La correzione assicura che l’opzione &quot;Modifica HTML&quot; non sia più disponibile per i frammenti esportati da AEM, mantenendo l’integrità dei contenuti e la governance prevista. (TGT-53286)
* **È stato risolto un problema di anteprima intermittente per il contenuto XF nel processo di creazione attività nell&#39;interfaccia utente aggiornata**: è stato risolto un problema nel processo di creazione attività a causa del quale il rendering del contenuto XF in modalità anteprima non riusciva a intermittenza nell&#39;interfaccia utente aggiornata. Anche se il contenuto consegnato correttamente, l’anteprima non veniva visualizzata in modo coerente, rendendo difficile per i clienti convalidare la configurazione delle offerte. Le anteprime XF ora vengono caricate in modo affidabile, migliorando l’affidabilità e l’efficienza durante la configurazione dell’attività. (TGT-53318)

+++

**Modalità Controllo di qualità**

+++Vedi i dettagli
* **È stato risolto un problema nel processo di creazione attività a causa del quale gli spazi iniziali negli URL causavano l&#39;interruzione dei collegamenti di controllo qualità**: è stato risolto un problema nel processo di creazione attività a causa del quale gli spazi iniziali nell&#39;URL attività non venivano tagliati correttamente durante il salvataggio. Questo causava collegamenti QA non validi e formattazione errata nel back-end. Dopo l’aggiornamento, gli URL vengono ora salvati correttamente, evitando collegamenti interrotti e migliorando l’affidabilità dei flussi di lavoro di controllo qualità per i clienti. (TGT-53427)

+++

**[!UICONTROL Recommendations]**

+++Vedi i dettagli
* **È stato risolto un problema nell&#39;interfaccia utente di ricerca del catalogo a causa del quale la ricerca avanzata non riusciva a fornire suggerimenti**: è stato risolto un problema nella nuova interfaccia utente di [!UICONTROL Catalog Search] a causa del quale la funzionalità [!UICONTROL Advanced Search] non riusciva a fornire suggerimenti. Gli utenti dovevano immettere valori esatti con un’ortografia precisa, rendendo l’esperienza di ricerca complicata e soggetta a errori. Con questa correzione, [!UICONTROL Advanced Search] offre ora suggerimenti rilevanti per la digitazione degli utenti, migliorando l&#39;usabilità e riducendo l&#39;attrito nella ricerca dei prodotti. (TGT-52008)
* **Sono stati risolti diversi problemi relativi all&#39;interfaccia utente e ai filtri per migliorare la reattività e l&#39;interazione dell&#39;entità**: sono stati risolti diversi problemi, tra cui la scarsa reattività dei dettagli dei criteri su dispositivi con schermo ridotto, la mancanza di risultati durante la selezione di &quot;Tutti i gruppi host&quot; nel filtro Ambiente e l&#39;impossibilità di interagire con entità senza nome. Queste correzioni migliorano l’usabilità tra le dimensioni dello schermo, garantiscono un filtraggio accurato e consentono la piena interazione con tutte le entità prodotto, migliorando l’esperienza complessiva per gli utenti. (TGT-52992)
* **Sono stati corretti gli ID di prodotto mancanti nella visualizzazione dei dettagli dei consigli durante la creazione dell&#39;attività**: è stato risolto un problema nel processo di creazione delle attività [!DNL Recommendations] a causa del quale gli ID di prodotto mancavano dalla schermata dei dettagli del prodotto, rendendo difficile per i clienti copiare o fare riferimento agli ID di prodotto durante i flussi di lavoro. Gli ID prodotto vengono ora visualizzati chiaramente nella visualizzazione dettagliata, migliorando la visibilità e supportando una gestione più efficiente dei prodotti per i clienti. (TGT-51964)
* **È stato risolto un problema nel processo di creazione attività a causa del quale i messaggi di prodotto non venivano visualizzati nella visualizzazione consigli**: è stato risolto un problema nel processo di creazione attività a causa del quale la colonna [!UICONTROL Message] nella visualizzazione [!DNL Recommendations] non visualizzava i dati di prodotto, anche se i messaggi erano presenti. I clienti hanno dovuto rimuovere manualmente e aggiungere nuovamente la colonna per visualizzare temporaneamente il contenuto, che spesso scompariva nuovamente durante lo scorrimento o la ricerca. Questo aggiornamento ripristina una visibilità coerente dei messaggi dei prodotti, migliorando la navigazione del catalogo e i flussi di lavoro di revisione. (TGT-52777)
* **È stato risolto un problema nel processo di creazione attività a causa del quale la selezione di &#39;Tutti i gruppi di host&#39; non restituiva alcun risultato nella visualizzazione Consigli**: è stato risolto un problema nel processo di creazione attività a causa del quale la selezione dell&#39;ambiente &quot;Tutti i gruppi di host&quot; nella visualizzazione [!DNL Recommendations] non restituiva alcun risultato. Ora i clienti possono visualizzare i dati dei prodotti in tutti i gruppi di host come previsto, migliorando la visibilità e la precisione dei filtri durante la configurazione dell’attività. (TGT-53006)
* **È stato risolto un problema nel processo di creazione attività a causa del quale l&#39;attivazione/disattivazione della promozione iniziale non persisteva dopo il salvataggio**: è stato risolto un problema nel processo di creazione attività a causa del quale la disattivazione dell&#39;attivazione/disattivazione della promozione iniziale nelle impostazioni attività non persisteva dopo il salvataggio. I clienti che tentavano di rimuovere la promozione iniziale hanno riscontrato che l’interruttore era stato riattivato al momento della revisione dell’attività, impedendo la corretta personalizzazione. Questo aggiornamento consente di salvare le modifiche in modo affidabile, offrendo ai clienti pieno controllo sulle impostazioni di promozione. (TGT-53215)
* **È stato corretto un ordinamento incoerente in base alla colonna [!UICONTROL Last Updated]:** È stato risolto un problema nel processo di creazione attività a causa del quale l&#39;ordinamento del catalogo in base alla colonna [!UICONTROL Last updated] generava risultati incoerenti. I clienti non erano in grado di organizzare in modo affidabile i dati dei prodotti in base alle marche temporali degli aggiornamenti, rendendo più difficile la revisione e la gestione del catalogo. L’ordinamento ora funziona come previsto, migliorando precisione e usabilità nell’interfaccia utente aggiornata. (TGT-53116)

+++

**Compositore esperienza visivo**

+++Vedi i dettagli
* **Sono stati risolti i problemi relativi al caricamento dell&#39;attività e al pulsante [!UICONTROL Cancel] nel processo di creazione attività**: è stato risolto un problema nel processo di creazione attività a causa del quale alcune attività non venivano caricate, impedendo ai clienti di accedere alle modifiche. Inoltre, il pulsante [!UICONTROL Cancel] non rispondeva, impedendo ai clienti di arrestare il processo di caricamento o uscire dalla visualizzazione di modifica. Questa correzione assicura che le attività ora vengano caricate in modo affidabile e che il pulsante [!UICONTROL Cancel] funzioni come previsto, migliorando la stabilità complessiva e l&#39;esperienza utente nel Compositore esperienza visivo. (VEC)(TGT-53218)
* **È stato risolto un problema di cambio di esperienza nell&#39;interfaccia utente del Compositore esperienza visivo aggiornata che impediva la modifica e disabilitava il pulsante [!UICONTROL Cancel]**: è stato risolto un problema nell&#39;interfaccia utente del Compositore esperienza visivo aggiornata in cui non veniva possibile caricare le modifiche quando si passava da un&#39;esperienza all&#39;altra in un&#39;attività Targeting esperienza. I clienti non sono stati in grado di modificare le esperienze oltre a quella inizialmente immessa e il pulsante [!UICONTROL Cancel] risulta mancante o non risponde. Questa correzione assicura che le modifiche ora vengano caricate correttamente in tutte le esperienze e che il pulsante [!UICONTROL Cancel] funzioni in modo affidabile, anche senza l&#39;estensione Helper, migliorando i flussi di lavoro di modifica e riducendo la frustrazione. (TGT-53256)
* **È stato risolto un problema relativo alla schermata bianca durante il passaggio tra più esperienze nel processo di creazione attività**: è stato risolto un problema che causava la visualizzazione di una schermata bianca durante il passaggio tra più esperienze. È stato inoltre risolto un problema nel processo di creazione delle attività a causa del quale i clienti riscontravano una schermata bianca durante il tentativo di modificare più esperienze all’interno di un’attività. Questo problema si verificava dopo aver applicato le modifiche a due esperienze e aver selezionato una terza esperienza, impedendo ulteriori modifiche. L’aggiornamento garantisce una transizione fluida tra le esperienze, consentendo ai clienti di apportare modifiche senza interruzioni. (TGT-53266)
* **È stato risolto un problema nel Compositore esperienza visivo a causa del quale le modifiche al codice personalizzato non venivano salvate in modo affidabile nelle sessioni di modifica**: è stato risolto un problema a causa del quale le modifiche al codice personalizzato apportate nel Compositore esperienza visivo non venivano salvate in modo affidabile in un singolo tentativo. I clienti hanno segnalato che le modifiche, come gli aggiornamenti degli stili o le modifiche di HTML, mancavano in modo intermittente dagli URL del sito Web e del controllo qualità, anche dopo aver utilizzato sia il pulsante [!UICONTROL Edit Content] che il pulsante [!UICONTROL Save] finale. Questa regressione è stata risolta, garantendo che tutte le modifiche al codice personalizzato persistano come previsto tra le sessioni di modifica.** (TGT-53418)
* **Correzione di `triggerViews` mancante nell&#39;interfaccia utente aggiornata durante la creazione dell&#39;attività**: è stato risolto un problema nel processo di creazione dell&#39;attività a causa del quale `triggerViews` non venivano visualizzati nell&#39;interfaccia utente aggiornata, anche se erano stati implementati correttamente nella pagina. Questo problema ha interessato più clienti e ha reso difficile convalidare i trigger basati sulla visualizzazione durante la configurazione dell’attività. `TriggerViews` ora viene visualizzato come previsto, consentendo ai clienti di completare e testare le proprie configurazioni in modo affidabile. (TGT-53239)
* **È stato risolto un problema nel caricamento delle visualizzazioni nel processo di creazione attività per pagine Web specifiche nell&#39;interfaccia utente aggiornata**: è stato risolto un problema nel processo di creazione attività a causa del quale le visualizzazioni non venivano caricate nell&#39;interfaccia utente aggiornata per pagine Web specifiche, nonostante fossero correttamente implementate e visibili nelle chiamate di consegna o di interazione. Questo problema interessava più clienti e rendeva difficile convalidare il targeting basato sulla visualizzazione. Le visualizzazioni ora si compilano in modo coerente tra le pagine supportate, migliorando l’affidabilità durante la configurazione dell’attività. (TGT-53246)
* **È stato risolto un problema relativo al caricamento intermittente delle visualizzazioni nel processo di creazione attività nell&#39;interfaccia utente aggiornata**: è stato risolto un problema nel processo di creazione attività a causa del quale le visualizzazioni non venivano visualizzate in modo intermittente nell&#39;interfaccia utente aggiornata durante la modifica delle attività. Anche se il nome della visualizzazione corretto era presente nel payload di rete, non veniva riconosciuto in modo coerente nell’interfaccia, influendo sulla capacità dei clienti di configurare la personalizzazione basata sulla visualizzazione. Le visualizzazioni ora vengono visualizzate in modo affidabile, supportando una configurazione e flussi di lavoro di convalida più fluidi. (TGT-53223)
* **È stato risolto un problema nel processo di creazione attività a causa del quale i nomi delle azioni tracciate non venivano salvati nell&#39;interfaccia utente aggiornata**: è stato risolto un problema nel processo di creazione attività a causa del quale le metriche delle azioni tracciate non potevano essere salvate nell&#39;interfaccia utente aggiornata. Dopo aver assegnato un nome a un elemento tracciato e aver salvato l’attività, quando viene riaperto il nome viene reimpostato su un’etichetta predefinita, creando confusione e interrompendo la configurazione dell’obiettivo. Le azioni tracciate ora mantengono i nomi assegnati, consentendo ai clienti di impostare e gestire con precisione le metriche di conversione. (TGT-53453)

+++

## [!DNL Target Standard/Premium] 25.8.1 (7 agosto 2025)

Questa versione di include i miglioramenti e le correzioni seguenti:

**Attività**

+++Vedi i dettagli
* Sono stati risolti diversi problemi relativi all’interfaccia utente aggiornata, tra cui errori durante l’eliminazione dei tipi di pagina a causa della spaziatura nei valori di input, della copia di attività inaffidabile tra aree di lavoro e del malfunzionamento delle regole di consegna pagine negli ambienti di controllo qualità. (TGT-52703)
* È stato risolto un problema nell&#39;interfaccia utente [!DNL Target] aggiornata a causa del quale gli utenti con il ruolo [!UICONTROL Editor] potevano accedere e tentare di modificare le attività live, che dovevano essere limitate. Le schermate elenco attività e panoramica mostravano erroneamente le opzioni di modifica per le attività live, con possibili modifiche non desiderate. (TGT-53055)
* È stato risolto un problema nell&#39;interfaccia utente [!UICONTROL Advanced Search] a causa del quale la selezione degli operatori &quot;il valore è presente&quot; o &quot;il valore non è presente&quot; richiedeva agli utenti di immettere un operando, che non dovrebbe essere richiesto per queste condizioni. (TGT-51961)
* È stato risolto un problema nell’interfaccia utente aggiornata a causa del quale i tentativi di copiare le attività dall’area di lavoro di staging all’area di lavoro di produzione continuavano a non riuscire, anche negli ambienti sandbox. I clienti hanno riscontrato diversi messaggi di errore, tra cui &quot;Pubblico anonimo già utilizzato dall’attività&quot; e &quot;ID pubblico non valido&quot;, nonostante l’utilizzo di configurazioni valide e l’esistenza di autorizzazioni Workspace appropriate. (TGT-52394)

+++

**Frammenti esperienza (XF)**

+++Vedi i dettagli
* È stato risolto un problema che impediva il rendering del contenuto del frammento di esperienza (XF) nell&#39;anteprima [!UICONTROL Visual Experience Composer] (VEC), nonostante il funzionamento corretto nella distribuzione dei contenuti. (TGT-53318)

+++

**Localizzazione**

+++Vedi i dettagli
* È stato risolto un problema di localizzazione a causa del quale il pulsante &quot;Aggiungi promozione&quot; nella sezione &quot;Promozioni&quot; appariva non localizzato in più ambienti di lingua nel tenant QA. (TGT-53263)

+++

**Offerte**

+++Vedi i dettagli
* È stato risolto un problema a causa del quale la modifica di un’offerta HTML esistente tramite il Compositore esperienza visivo causava la rimozione di tutte le modifiche dalla distribuzione del contenuto. Le modifiche vengono visualizzate in grigio nella scheda delle modifiche e non vengono riportate nelle anteprime di controllo qualità, anche se vengono applicate correttamente nell’interfaccia utente precedente. (TGT-52863)
* È stato risolto un problema nell&#39;interfaccia utente [!DNL Target] aggiornata a causa del quale le modifiche apportate alle offerte HTML nel [!UICONTROL Visual Experience Composer] (Compositore esperienza visivo) non persistevano dopo essere tornate dalla scheda [!UICONTROL Targeting] a [!UICONTROL Experiences]. (TGT-52874)
* È stato risolto un problema nell&#39;interfaccia utente [!DNL Target] aggiornata a causa del quale l&#39;inserimento di un&#39;offerta HTML prima e un&#39;offerta dopo lo stesso selettore causava una generazione errata della posizione. Quando i clienti sono tornati dalla scheda [!UICONTROL Targeting] alla scheda [!UICONTROL Experience], è stato mantenuto un solo selettore, con conseguente perdita di modifiche e consegna di contenuto interrotta. Questo comportamento è diverso dall’interfaccia utente legacy, che mantiene correttamente entrambe le modifiche con identificatori di posizione distinti. (TGT-52891)
* È stato risolto un problema nell&#39;interfaccia utente [!DNL Target] aggiornata a causa del quale facendo clic su un&#39;offerta aggiunta nella barra [!UICONTROL Modifications] il pannello [!UICONTROL Configuration] di destra veniva visualizzato e scompariva in modo intermittente, rendendo difficile l&#39;interazione con le impostazioni dell&#39;offerta. (TGT-53288)
* È stato risolto un problema a causa del quale le offerte HTML aggiunte alle varianti specifiche per il pubblico all’interno di un’attività non venivano salvate o visualizzate in modo coerente nella sezione delle modifiche. Dopo il passaggio da un pubblico all’altro durante la modifica, le offerte applicate in precedenza a volte scomparivano o non venivano riprodotte, interrompendo la convalida e ritardando la preparazione dell’attività. (TGT-53440)
* È stato risolto un problema che causava la creazione di offerte duplicate nella nuova attività durante la copia di un’attività che includeva offerte. Questo comportamento ha causato confusione e confusione inutili, in particolare durante lo spostamento di attività tra aree di lavoro. La correzione assicura che le offerte [!DNL Target] vengano ora copiate correttamente nell&#39;area di lavoro di destinazione senza duplicazioni, semplificando la gestione delle attività e migliorando l&#39;efficienza del flusso di lavoro. (TGT-53454)

+++

**Applicazioni a pagina singola**

+++Vedi i dettagli
* È stato risolto un problema nel Compositore esperienza visivo aggiornato che impediva ai clienti di applicare modifiche alle visualizzazioni [!UICONTROL Single Page Application] (SPA). Le attività create nella vecchia interfaccia supportavano il targeting specifico della vista, ma la nuova interfaccia non riusciva a rilevare o consentire modifiche a tali viste, con i controlli per il cambio di vista disabilitati. (TGT-52556)

+++

**Compositore esperienza visivo**

+++Vedi i dettagli
* È stato risolto un problema a causa del quale le modifiche apportate alle esperienze all&#39;interno di [!UICONTROL Visual Experience Composer] non erano visibili o venivano visualizzate in modo incoerente nell&#39;interfaccia utente. (TGT-TGT-53381)
* È stato risolto un problema nel Compositore esperienza visivo aggiornato a causa del quale nella sezione [!UICONTROL Manage Content] non veniva visualizzato il testo alternativo per le miniature delle esperienze. Questo problema rendeva difficile per gli utenti identificare i documenti, soprattutto quando i nomi dei file erano lunghi o troncati. (TGT-52291)
* È stato corretto un errore a causa del quale i clienti riscontravano errori di convalida non corretti durante la configurazione di [!UICONTROL page delivery] regole nelle attività del Compositore esperienza visivo. In particolare, operatori come &quot;è uguale a&quot; e &quot;è diverso da&quot; hanno attivato &quot;Input non valido per il tipo di operatore&quot; durante l’immissione di valori di testo, anche se il testo dovrebbe essere supportato. (TGT-52629)
* Sono stati risolti diversi problemi che causavano un comportamento incoerente nel pannello [!UICONTROL Modifications] dell&#39;interfaccia utente aggiornata quando si selezionavano le offerte utilizzando il pulsante &quot;Seleziona un&#39;offerta&quot;. Invece di sostituire l&#39;offerta esistente, l&#39;interfaccia utente ha aggiunto un duplicato e ha tentato di interagire con una delle offerte causando errori della console come `selectorNotFound`. Inoltre, alcune offerte non visualizzano il pulsante &quot;Seleziona un’offerta&quot;, che mostra solo le proprietà modificabili. (TGT-53321)
* È stato risolto un problema nell&#39;interfaccia utente [!DNL Target] aggiornata a causa del quale le modifiche al codice HTML apportate durante la configurazione dell&#39;attività non persistevano nelle pagine delle varianti, anche se venivano salvate correttamente per i gruppi di controllo. Nonostante diversi tentativi di ricreare i test senza raggruppamenti di pagine, le pagine delle varianti non sono riuscite a mantenere le modifiche, con un conseguente impatto sulla distribuzione dei contenuti e sulla convalida del controllo qualità. (TGT-53436)
* È stato risolto un problema nel Compositore esperienza visivo aggiornato a causa del quale l’operatore &quot;è uguale a qualsiasi di&quot; nelle regole di consegna pagina non accettava i valori di input. Durante la configurazione dei parametri del cliente in tutte le mbox, la selezione di questo operatore causava un errore di &quot;Input non valido&quot;, impedendo la creazione della regola. (TGT-52623)

+++

**Aree di lavoro**

+++Vedi i dettagli
* È stato migliorato il flusso di lavoro durante la copia delle attività tra aree di lavoro. Le attività di copia tra aree di lavoro prima causavano errori di sincronizzazione a causa di tipi di pubblico mancanti e proprietà non assegnate. Questo aggiornamento introduce un flusso di lavoro più intelligente e intuitivo che garantisce che le attività copiate siano configurate correttamente e pronte per la pubblicazione. (TGT-47094)
* È stato risolto un problema che impediva ai clienti di copiare le attività tra aree di lavoro a causa di un errore nella mutazione `copyActivityBatchOperations`. I tentativi di duplicare le attività hanno restituito un errore del server (500) e un payload di risposta nullo. (TGT-52405)
* È stato risolto un problema che impediva la sincronizzazione delle attività quando le offerte a cui si faceva riferimento nella configurazione non erano accessibili all’interno dell’area di lavoro selezionata. Ciò causava errori di pubblicazione e lasciava le attività in uno stato di errore. (TGT-52535)
* Sono stati risolti diversi problemi che si verificavano durante la copia di attività tra aree di lavoro nell&#39;interfaccia utente [!DNL Target] aggiornata. I clienti hanno riscontrato errori relativi all&#39;accesso ai tipi di pubblico, in particolare con le attività live, e una convalida dei privilegi non corretta, anche quando l&#39;utente aveva &quot;[!UICONTROL Approver]&quot; ruoli nelle aree di lavoro di origine e di destinazione. (TGT-53002)
* È stato risolto un problema nell’interfaccia utente aggiornata a causa del quale la copia delle attività all’interno della stessa area di lavoro duplicava inutilmente le offerte e i tipi di pubblico associati. (TGT-53457)
* È stato risolto un problema per risolvere i casi in cui i tipi di pubblico ad hoc (anonimi) non venivano copiati correttamente tra aree di lavoro non predefinite o da aree di lavoro non predefinite a predefinite. Anche se gli aggiornamenti precedenti garantivano la duplicazione corretta per gli scenari predefiniti-non-predefiniti e same-Workspace, questo miglioramento si concentra sul mantenimento di configurazioni di pubblico combinate che si estendono su più aree di lavoro. La correzione garantisce un comportamento coerente del pubblico e un targeting accurato in tutte le transizioni dell’area di lavoro. (TGT-53268)

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
