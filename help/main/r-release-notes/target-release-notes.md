---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease;early access
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di [!DNL Target].
title: Quali nuove funzioni e miglioramenti saranno inclusi nella prossima versione [!DNL Target] ?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: be371f3631d79c65c632a23776ab08de21b031eb
workflow-type: tm+mt
source-wordcount: '2610'
ht-degree: 7%

---

# Note sulla versione (prerelease) di [!DNL Target]

Questo articolo contiene informazioni prerelease per le prossime versioni di [!DNL Adobe Target], incluse SDK, API e librerie JavaScript.

**Ultimo aggiornamento: 27 agosto 2025**

>[!NOTE]
>
>* Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso. Le informazioni contenute in questo articolo vengono aggiornate frequentemente, soprattutto prima delle versioni di.
>
>* Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md).
>
>* I codici tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target Standard/Premium] 25.8.4 (28 agosto 2025)

Questa versione include i seguenti aggiornamenti e correzioni:

**[!UICONTROL Activities]**

+++Vedi i dettagli
* **È stato risolto un problema che impediva alle attività pianificate di visualizzare in modo errato lo stato &quot;[!UICONTROL Live]&quot; nell&#39;interfaccia utente aggiornata durante il processo di creazione attività**: le attività con date di attivazione future ora presentano correttamente lo stato &quot;[!UICONTROL Scheduled]&quot;. (TGT-53187)
* **Le attività pianificate visualizzavano erroneamente uno stato [!UICONTROL Live] fino a quando la pagina non veniva aggiornata**: I clienti segnalavano che quando si pianificava un&#39;attività per l&#39;attivazione in una data e un&#39;ora future, lo stato appariva inizialmente come [!UICONTROL Live] invece di [!UICONTROL Scheduled]. Ciò causava confusione nonostante il messaggio di conferma indicasse il comportamento di pianificazione corretto. Lo stato dell&#39;attività ora riflette accuratamente [!UICONTROL Scheduled] subito dopo il salvataggio, senza richiedere un aggiornamento della pagina. (TGT-52937)
* **Le modifiche apportate alle esperienze duplicate hanno involontariamente interessato l&#39;esperienza originale**: i clienti hanno segnalato che durante la duplicazione di un&#39;esperienza all&#39;interno di un&#39;attività e l&#39;assegnazione di un nuovo pubblico, tutte le modifiche apportate all&#39;esperienza duplicata, come la progettazione o i criteri, sono state riportate anche nell&#39;esperienza originale. Questo impediva la creazione di varianti indipendenti e interessava i flussi di lavoro di produzione. È ora possibile modificare in modo indipendente le esperienze duplicate senza influire sulla versione originale. (TGT-53361)
* **È stato risolto un problema che impediva ai clienti di salvare un&#39;attività a causa di un errore `InvalidProperty.Json`**: in precedenza, i clienti riscontravano un errore di tipo &quot;Input utente non valido&quot; quando tentavano di salvare un&#39;attività senza apportare modifiche. L’errore è stato causato da un nome di proprietà &quot;content&quot; non riconosciuto nel payload JSON. Questo problema è stato risolto e ora è possibile salvare correttamente le attività nell’interfaccia utente aggiornata, anche quando non vengono apportate modifiche. (TGT-53513)

+++

**Analytics for Target (A4T)**

+++Vedi i dettagli
* **Impossibile digitare i nomi delle suite di rapporti durante la creazione di attività A4T**: i clienti non sono stati in grado di digitare nel menu a discesa [!UICONTROL Report Suite] quando si seleziona [!UICONTROL Analytics] come origine per la generazione di rapporti nell&#39;interfaccia utente aggiornata.  Questo problema rendeva difficile individuare suite di rapporti specifiche, in particolare per le organizzazioni con elenchi di grandi dimensioni. L’elenco a discesa ora supporta la digitazione e la ricerca per nome, migliorando l’efficienza durante il processo di creazione delle attività. (TGT-53345)

+++

**[!UICONTROL Audiences]**

+++Vedi i dettagli
* **I tipi di pubblico &quot;con intervallo di tempo&quot; scaduti hanno bloccato il salvataggio dell&#39;attività anche dopo la rimozione**: in precedenza, i clienti non potevano salvare un&#39;attività se in precedenza aveva incluso un pubblico &quot;con intervallo di tempo&quot; scaduto, anche dopo la rimozione di tale pubblico. Questo problema era causato dalla convalida residua sul pubblico per sola attività, che continuava a causare errori. Una volta rimossi i tipi di pubblico scaduti, le attività possono ora essere salvate come previsto. (TGT-53517)
* **Pagine aggiuntive e più tipi di pubblico sono scomparsi dopo il salvataggio di un&#39;attività**: in precedenza, i clienti che creavano un&#39;attività [!UICONTROL A/B Test] nel processo di creazione attività hanno perso pagine aggiuntive configurate e più tipi di pubblico dopo il salvataggio. Questo comportamento è stato imprevisto e ha causato confusione durante la configurazione. Queste configurazioni ora persistono correttamente dopo il salvataggio dell’attività. (TGT-52357)

+++

**Offerte decisionali**

+++Vedi i dettagli
* **Impossibile modificare le offerte di decisione o selezionare elementi di pagina specifici nel Compositore esperienza visivo aggiornato**: nell&#39;interfaccia utente aggiornata sono stati riscontrati diversi problemi che impedivano di aggiornare le attività esistenti o crearne di nuove:

   * Le offerte basate su decisioni venivano visualizzate in modo errato come offerte HTML, impedendo così le modifiche.
   * Impossibile selezionare elementi di pagina specifici nel Compositore esperienza visivo.
   * Le modifiche apportate durante la modifica non sono state salvate.
   * Alcuni URL regionali non sono stati caricati correttamente nel Compositore esperienza visivo e richiedono modifiche manuali dei cookie.

  I clienti ora possono modificare le offerte di decisione, selezionare gli elementi di pagina con precisione e salvare le modifiche come previsto. Anche le pagine regionali vengono caricate correttamente nel Compositore esperienza visivo. (TGT-53425)

* **I selettori delle decisioni sulle offerte non hanno potuto essere modificati e modificati in modo imprevisto dopo il salvataggio**: i clienti hanno segnalato che quando si applicano decisioni sulle offerte nell&#39;interfaccia utente aggiornata, il selettore non poteva essere modificato dal suo valore predefinito. I tentativi di modificare il selettore (ad esempio, in `#tf-cq-hr or body`) sono stati ignorati e dopo il salvataggio dell&#39;attività, il selettore è stato sostituito con un valore generico come `#cdq_element_0`. Questo problema causava la scomparsa dell’offerta dal Compositore esperienza visivo e bloccava ulteriori modifiche. I clienti ora possono modificare i selettori di Offer Decision come previsto e i selettori salvati persistono correttamente senza modifiche impreviste. (TGT-53433)
* **Le decisioni sulle offerte sono scomparse dalle attività dopo il salvataggio**: i clienti hanno segnalato che le decisioni sulle offerte applicate agli elementi della pagina nell&#39;interfaccia utente aggiornata non erano più visibili dopo il salvataggio dell&#39;attività. In alcuni casi, il selettore è stato modificato in modo imprevisto e l’offerta non è stata riprodotta nel Compositore esperienza visivo al momento del re-editing. Le decisioni sulle offerte ora persistono correttamente dopo il salvataggio e i selettori rimangono stabili, garantendo che le offerte siano visibili e modificabili come previsto. (TGT-53434)

+++

**Frammenti esperienza**

+++Vedi i dettagli
* **I clienti hanno ricevuto un errore durante l&#39;inserimento di [!UICONTROL Experience Fragments] tramite [!UICONTROL Insert Before] o[!UICONTROL Insert After]**: Si è verificato un errore durante il tentativo di inserire [!UICONTROL Experience Fragments] in un&#39;attività tramite le opzioni [!UICONTROL Insert Before] o [!UICONTROL Insert After] nell&#39;interfaccia utente aggiornata. Il messaggio di errore visualizzato era:

  &quot;Il contenuto dell’offerta deve contenere esattamente un elemento HTML.&quot;

  Questo problema era specifico dell’interfaccia utente aggiornata e non si verificava nella versione precedente. Ora è stato risolto e i clienti possono inserire [!UICONTROL Experience Fragments] senza incontrare questo errore. (TGT-53432)

* **Messaggio di errore durante l&#39;aggiunta di un [!UICONTROL Experience Fragment] a un&#39;attività**: in precedenza, i clienti che tentavano di inserire un [!UICONTROL Experience Fragment] utilizzando l&#39;opzione [!UICONTROL Insert Before] o [!UICONTROL Insert After] riscontravano l&#39;errore: &quot;Il contenuto dell&#39;offerta deve contenere esattamente un elemento HTML&quot;. Questo errore si è verificato nonostante il frammento fosse valido e accettato nell’interfaccia utente legacy, che includeva un interruttore per supportare questa configurazione. Il problema è stato risolto nel Compositore esperienza visivo aggiornato. (TGT-53442)

+++

**Localizzazione**

+++Vedi i dettagli
* **I messaggi popup nel passaggio [!UICONTROL Goals & Settings] non erano localizzati**: in precedenza, i clienti avevano riscontrato un messaggio popup non localizzato durante l&#39;immissione di caratteri non supportati, ad esempio emoticon, nel campo [!UICONTROL Objective] durante il processo di creazione attività. I messaggi di avviso popup ora sono correttamente localizzati in tutte le lingue supportate, garantendo un’esperienza coerente e accessibile ai clienti globali. (TGT-52251)
* **Una stringa nella finestra di dialogo [!UICONTROL Create Audience] non è stata localizzata**: in precedenza, il messaggio &quot;Scegli almeno una data di inizio o di fine per &#39;non si ripete&#39;&quot; appariva non localizzato nel modale [!UICONTROL Create Audience] durante la configurazione degli attributi dell&#39;intervallo di tempo. La stringa ora è localizzata correttamente in tutte le lingue supportate, garantendo un&#39;esperienza coerente per i clienti globali nel flusso di lavoro [!UICONTROL Audiences]. (TGT-52253)
* **La descrizione comando nella finestra di dialogo [!UICONTROL Create Audience] non è stata localizzata**: in precedenza, quando i clienti passavano il puntatore del mouse sulla descrizione comando dell&#39;errore dopo aver immesso caratteri non supportati, ad esempio emoticon, nel campo del nome del pubblico, la descrizione comando appariva non localizzata. La descrizione comandi ora visualizza correttamente i messaggi localizzati in tutte le lingue supportate, garantendo un&#39;esperienza coerente e accessibile nel flusso di lavoro [!UICONTROL Audiences]. (TGT-52254)

+++

**[!DNL Recommendations]**

+++Vedi i dettagli
* **Impossibile disabilitare [!UICONTROL Front Promotion] nell&#39;attività live**: è stato risolto un problema che impediva ai clienti di disabilitare [!UICONTROL Front Promotion] nelle attività live utilizzando l&#39;interfaccia utente aggiornata. Le modifiche apportate nella sezione Promozione durante il processo di creazione attività ora persistono come previsto, garantendo una configurazione accurata delle attività live in [!UICONTROL Product Catalog Search]. (TGT-53231)
* **La modifica di un consiglio di un&#39;esperienza duplicata ha avuto un impatto sull&#39;esperienza originale**: i clienti hanno segnalato che quando si duplicava un&#39;esperienza all&#39;interno di un&#39;attività e si modificavano la progettazione o i criteri dei consigli nel duplicato, tali modifiche venivano applicate involontariamente all&#39;esperienza originale.  Questo problema impediva la creazione di varianti indipendenti e perturbava il comportamento previsto nel processo aggiornato di creazione delle attività. È ora possibile modificare in modo indipendente le esperienze duplicate senza influire sulla versione originale. (TGT-53369)
* **Impossibile visualizzare l&#39;elenco prodotti durante la modifica di una raccolta o di un&#39;esclusione nella scheda [!UICONTROL Recommendations]** In precedenza, l&#39;elenco prodotti filtrato in base alle regole applicate non era visibile nella finestra modale di modifica, rendendo difficile per i clienti confermare quali prodotti sono stati inclusi o esclusi. L&#39;elenco dei prodotti viene ora visualizzato correttamente e gli aggiornamenti in tempo reale, man mano che le regole vengono modificate, migliorando la visibilità e l&#39;usabilità nell&#39;interfaccia utente [!DNL Recommendations] aggiornata. (TGT-53481)
* **È stato aggiornato il layout della finestra di dialogo [!UICONTROL View Details] nella scheda [!UICONTROL Recommendations]**: in precedenza, la finestra di dialogo [!UICONTROL View Details] non disponeva di una struttura chiara, rendendo difficile l&#39;accesso alle informazioni specifiche dell&#39;elemento e relative all&#39;inventario. Il layout è stato aggiornato per includere due schede: una scheda visualizza i dettagli per l’elemento selezionato e la seconda scheda mostra l’inventario filtrato in base alle regole correnti della raccolta o dell’esclusione. Questo miglioramento migliora la chiarezza e l&#39;usabilità nell&#39;interfaccia utente [!DNL Recommendations] aggiornata. (TGT-53503)
* **I clienti non potevano cercare le suite di rapporti nel menu a discesa [!UICONTROL Goals & Settings]**: in precedenza, il menu a discesa delle suite di rapporti nella sezione [!UICONTROL Goals & Settings] del processo di creazione attività non supportava l&#39;input di testo per la ricerca, rendendo difficile per i clienti con un numero elevato di suite di rapporti individuare quella corretta. Questa funzionalità, disponibile nell’interfaccia utente legacy, è stata ripristinata. Ora i clienti possono digitare per cercare e selezionare le suite di rapporti in modo più efficiente. (TGT-53514)
* **I clienti non sono in grado di scaricare il file CSV dei criteri personalizzati nell&#39;interfaccia utente [!DNL Recommendations]**: in precedenza, facendo clic sul collegamento di download per i file CSV dei criteri personalizzati nella scheda [!UICONTROL Recommendations], veniva restituito un errore 404 e non era possibile aprirli in una nuova scheda. Il collegamento per il download ora si apre in una nuova scheda e distribuisce correttamente il file CSV, migliorando l’accessibilità e l’usabilità per i clienti che gestiscono criteri personalizzati. (TGT-51966)
* **L&#39;abilitazione di una promozione di [!UICONTROL Recommendations] senza dati di input ha generato un messaggio di errore generico**: in precedenza, i clienti che abilitavano una promozione prima o dopo in un&#39;attività Recommendendations senza specificare i campi obbligatori avevano riscontrato un &quot;errore di input non valido&quot; vago con il codice `error.restapi.missingFields`. Il sistema ora fornisce un messaggio di errore chiaro e actionable che indica quali campi mancano, migliorando l’usabilità e riducendo la confusione durante il processo di creazione di attività. (TGT-52616)
* **Le miniature e le immagini del prodotto non venivano caricate in modo coerente in[!UICONTROL Catalog Search]**: i clienti hanno segnalato che le miniature del prodotto e le immagini a dimensione intera in [!UICONTROL Catalog Search] risultavano mancanti o interrotte in modo intermittente, soprattutto dopo la navigazione o la modifica della visibilità delle colonne. Le miniature e le immagini ora vengono caricate in modo affidabile, indipendentemente dalle impostazioni delle colonne o dal comportamento di navigazione, migliorando l&#39;esperienza complessiva nel flusso di lavoro [!UICONTROL Recommendations]. (TGT-52778)
* **Impossibile creare [!UICONTROL Designs] e [!UICONTROL Criteria] nell&#39;ambiente [!UICONTROL Stage]**: si è verificato un errore &quot;Input utente non valido&quot; durante il tentativo di creare [!UICONTROL Designs] o [!UICONTROL Criteria] nella scheda [!UICONTROL Recommendations] nell&#39;ambiente [!UICONTROL Stage]. I clienti ora possono creare [!UICONTROL Designs] e [!UICONTROL Criteria] senza errori nell&#39;ambiente [!UICONTROL Stage]. (TGT-53205)
* **[!UICONTROL Promotions]non sono stati rimossi dalle attività [!UICONTROL Recommendations] dopo il salvataggio**: i clienti hanno segnalato che le promozioni aggiunte alle attività [!DNL Recommendation] continuavano a essere visualizzate anche dopo la rimozione e il salvataggio. Questo problema ha interessato sia gli ambienti di staging che quelli di produzione ed è persistito in più tentativi di salvataggio. Le promozioni ora riflettono correttamente le modifiche apportate durante la modifica dell’attività nel processo aggiornato di creazione delle attività. (TGT-53490)

+++

**[!UICONTROL Reports]**

+++Vedi i dettagli
* **[!UICONTROL Automated Segments]ha visualizzato un pubblico nullo nei report attività**: i clienti hanno osservato che quando visualizzavano [!UICONTROL Automated Segments] nella sezione [!UICONTROL Reports] di un&#39;attività, il campo del pubblico appariva nullo, anche se erano previsti dati di segmenti validi. Questo problema influiva sulla visibilità del targeting del pubblico e sulla precisione del reporting. [!UICONTROL Automated Segments] ora visualizza correttamente le informazioni sul pubblico associato nei rapporti delle attività. (TGT-52793)
* **Impossibile scaricare i report attività in formato CSV**: i clienti che tentavano di esportare i report attività dalla scheda [!UICONTROL Reports] hanno riscontrato un errore durante la selezione dell&#39;opzione di download CSV. Questo problema ha interessato sia i rapporti standard che le esportazioni dei dettagli dell’ordine. I rapporti ora vengono scaricati correttamente in formato CSV. (TGT-53464)

+++

**Applicazioni a pagina singola**

+++Vedi i dettagli
* **Il passaggio tra le modalità [!UICONTROL Browse] e [!UICONTROL Design] ha reimpostato gli stati dell&#39;applicazione a pagina singola nell&#39;editor Web**: i clienti hanno segnalato che il passaggio tra le modalità [!UICONTROL Browse] e [!UICONTROL Design] nel Compositore esperienza visivo ha causato il ricaricamento dell&#39;editor Web, il ripristino dello stato dell&#39;applicazione a pagina singola e l&#39;interruzione del processo di creazione delle attività. L’editor ora mantiene lo stato di navigazione dell’applicazione a pagina singola quando si passa da una modalità all’altra, garantendo un’esperienza di modifica più fluida e coerente. (TGT-53074)

+++

**[!UICONTROL Visual Experience Composer (VEC)]**

+++Vedi i dettagli
* **La ridenominazione di una posizione in un&#39;attività [!UICONTROL Automated Personalization] (AP) o [!UICONTROL Multivariate Test] (MVT) non è persistita dopo essere passati al passaggio [!UICONTROL Targeting] e aver restituito.** I clienti ora possono modificare e salvare correttamente i nomi delle posizioni e le modifiche rimangono visibili durante il processo di creazione attività. (TGT-52367)
* **L&#39;interfaccia utente VEC legacy visualizzata sui tenant nell&#39;ambiente [!UICONTROL Stage]**: è stato risolto un problema che si verificava durante l&#39;accesso a determinati tenant nell&#39;ambiente [!UICONTROL Stage]: l&#39;interfaccia utente legacy veniva visualizzata in modo errato al posto del Compositore esperienza visivo aggiornato. Questo problema era riproducibile in più percorsi di accesso e interessava la sezione [!UICONTROL Activities]. L&#39;interfaccia utente aggiornata ora viene visualizzata correttamente per entrambi i tenant nell&#39;ambiente [!UICONTROL Stage]. (TGT-52261)
* **La selezione di un colore di sfondo ha causato l&#39;arresto anomalo della pagina nel Compositore esperienza visivo aggiornato**:
È stato risolto un problema a causa del quale la selezione di un colore di sfondo dal pannello [!UICONTROL Style] nel Compositore esperienza visivo aggiornato causava l&#39;arresto anomalo della pagina e la visualizzazione di una pagina vuota. Gli errori della console indicano un errore durante la lettura delle proprietà da un elemento non definito, in particolare relativo a `querySelector`. I clienti possono ora selezionare in modo sicuro i colori di sfondo senza causare un arresto anomalo. (TGT-53561)
* **Impossibile salvare le attività a causa di un errore di input utente non valido**: è stato corretto un errore che si verificava durante il tentativo di salvare le attività esistenti nel Compositore esperienza visivo aggiornato. L’errore viene visualizzato solo durante le modifiche, non quando si creano nuove attività con la stessa proprietà. Il messaggio di errore includeva:

  `Invalid Json. Unrecognized property name 'content'. Location: line - 1, column - 432.`

  Le attività che utilizzano la proprietà interessata possono ora essere salvate correttamente dopo la modifica. (TGT-53507)

* **Le immagini trasparenti non includevano più il parametro &quot;fmt=png-alpha&quot; nel Compositore esperienza visivo aggiornato**: i clienti hanno segnalato che durante la sostituzione delle immagini nell&#39;interfaccia utente aggiornata, gli sfondi trasparenti non venivano più conservati. Gli URL dell&#39;immagine generati dal Compositore esperienza visivo aggiornato hanno omesso il parametro `fmt=png-alpha`, che in precedenza garantiva la trasparenza nella vecchia interfaccia utente. L&#39;interfaccia utente aggiornata ora aggiunge correttamente il parametro `fmt=png-alpha` per le immagini trasparenti, ripristinando il comportamento di rendering previsto. (TGT-52615)
* **I clienti non possono passare alla sezione targeting nelle attività di Personalizzazione automatizzata senza aggiungere due posizioni**: i clienti che creano [!UICONTROL Automated Personalization] attività di Personalizzazione automatizzata nell&#39;interfaccia utente aggiornata non possono passare alla sezione targeting se non vengono aggiunte due posizioni. Questo comportamento era diverso da quello della precedente interfaccia utente, in cui era sufficiente una singola posizione. Il problema bloccava la creazione e il salvataggio delle attività per i clienti che preferivano utilizzare una sola posizione. I clienti possono ora procedere al targeting e salvare le attività di Personalizzazione automatizzata con un&#39;unica posizione, ripristinando le funzionalità previste. (TGT-53426)
* **Offerte HTML duplicate nell&#39;area di lavoro quando si passa da un&#39;esperienza all&#39;altra**: in precedenza, i clienti che inserivano offerte HTML in contenuto duplicato con esperienza nell&#39;area di lavoro dopo il passaggio da un&#39;esperienza all&#39;altra. Questo problema causava anche la mancata possibilità di scorrimento dell’area di lavoro, con un conseguente impatto sull’usabilità. Le offerte di HTML non sono più duplicate e l’area di lavoro rimane scorrevole quando si passano da un’esperienza all’altra nel Compositore esperienza visivo aggiornato. (TGT-53487)
* **L&#39;aggiornamento manuale di un selettore CSS ha causato la visualizzazione della schermata del Compositore esperienza visivo**: i clienti hanno segnalato che durante la modifica di un&#39;offerta nel Compositore esperienza visivo, l&#39;aggiornamento manuale del selettore CSS ha attivato una schermata vuota, anche quando il selettore era valido e presente nella pagina. La schermata del Compositore esperienza visivo ora rimane stabile quando i selettori vengono aggiornati manualmente durante il processo di creazione dell’attività. (TGT-53553)
* **Problema di troncamento nel campo Data inizio quando si seleziona &#39;data e ora specificate&#39; in[!UICONTROL Goals & Settings]**: si è verificato un problema di troncamento nel campo [!DNL Start date] quando si sceglie l&#39;opzione data e ora specificata nella sezione durata della pagina [!UICONTROL Goals & Settings] durante la creazione dell&#39;attività. La data e l’ora complete vengono ora visualizzate correttamente nelle diverse lingue supportate. (TGT-47843)
* **L&#39;icona del filtro è scomparsa quando si riduce a icona il browser nella barra [!UICONTROL Manage Content]**: i clienti hanno segnalato che l&#39;icona del filtro nella barra [!UICONTROL Manage Content] del flusso di creazione attività [!UICONTROL Automated Personalization] è scomparsa quando la finestra del browser è stata ridimensionata o ridotta a icona. L’icona del filtro ora rimane visibile e accessibile indipendentemente dalle dimensioni del browser, migliorando l’usabilità nelle diverse risoluzioni dello schermo. (TGT-51449)

+++

**[!UICONTROL Workspaces]**

+++Vedi i dettagli
* **I clienti limitati a una sola area di lavoro potevano visualizzare le attività da altre aree di lavoro**: i clienti con accesso limitato a una specifica area di lavoro potevano ancora selezionare [!UICONTROL All Workspaces] nell&#39;interfaccia utente aggiornata e visualizzare le attività da altre aree di lavoro. Questo comportamento ha comportato il rischio di modifiche non intenzionali alle attività live al di fuori dell’ambito assegnato. Le restrizioni di Workspace ora vengono applicate correttamente e i clienti possono visualizzare le attività solo all’interno dell’area di lavoro assegnata. (TGT-53101)
* **I clienti potevano visualizzare le attività da [!UICONTROL Default Workspace] senza accesso**: i clienti potevano vedere le attività da [!UICONTROL Default Workspace] pur non avendone accesso. Le autorizzazioni di Workspace ora vengono applicate correttamente nell’interfaccia utente aggiornata, affinché i clienti possano visualizzare solo le attività associate all’area di lavoro a loro assegnata. (TGT-53297)

+++

## Note aggiuntive e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK]&#x200B;(https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js di [!DNL Adobe Target]. |

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud], iscriviti ad [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
