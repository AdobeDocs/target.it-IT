---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease;early access
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di [!DNL Target].
title: Quali nuove funzioni e miglioramenti saranno inclusi nella prossima versione [!DNL Target] ?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 95d8bd994ffdb1d256b7eb0aea1a2462b40ce530
workflow-type: tm+mt
source-wordcount: '2221'
ht-degree: 7%

---

# Note sulla versione (prerelease) di [!DNL Target]

Questo articolo contiene informazioni prerelease per le prossime versioni di [!DNL Adobe Target], incluse SDK, API e librerie JavaScript.

**Ultimo aggiornamento: 21 agosto 2025**

>[!NOTE]
>
>* Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso. Le informazioni contenute in questo articolo vengono aggiornate frequentemente, soprattutto prima delle versioni di.
>
>* Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md).
>
>* I codici tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target Standard/Premium] 25.8.3 (21 agosto 2025)

Questa versione include i seguenti aggiornamenti e correzioni:

**[!UICONTROL Activities]**

+++Vedi i dettagli
* **È stato risolto un problema a causa del quale il salvataggio delle attività causava un errore di input dell&#39;utente non valido a causa di dati di proprietà non validi**: si è verificato un errore critico durante il tentativo di salvare le attività esistenti. Il messaggio di errore indica un input utente non valido, in particolare un riferimento a un contenuto di nome proprietà non riconosciuto nel payload JSON. In particolare, le nuove attività che utilizzano la stessa proprietà sono state salvate correttamente, suggerendo che il problema fosse isolato nei dati delle attività legacy. Il processo di creazione delle attività ora gestisce correttamente le configurazioni delle proprietà legacy, evitando errori di input non validi e garantendo un comportamento di salvataggio coerente tra le attività nuove ed esistenti. (TGT-53507)
* **È stato risolto un problema che impediva ai clienti di salvare un&#39;attività a causa di un errore InvalidProperty.Json**: si è verificato un errore durante il tentativo di salvare un&#39;attività nell&#39;interfaccia utente aggiornata, anche senza apportare modifiche. Il messaggio di errore indica una struttura JSON non valida: &quot;Json non valido. Nome di proprietà &#39;content&#39; non riconosciuto. Posizione: riga - 1, colonna - 432.&quot; Questo problema era causato da una proprietà non riconosciuta nel payload della richiesta ed è stato ora risolto. I clienti possono salvare le attività senza riscontrare questo errore. (TGT-53513)
* **È stato risolto un problema che causava la visualizzazione errata dello stato [!UICONTROL Live] da parte delle attività pianificate fino all&#39;aggiornamento della pagina**: I clienti osservavano che quando si pianificava l&#39;attivazione di un&#39;attività in una data e un&#39;ora future, lo stato appariva immediatamente come [!UICONTROL Live] invece di [!UICONTROL Scheduled]. Ciò causava confusione, anche se il messaggio di conferma indicava correttamente che l’attività era pianificata. L&#39;aggiornamento della pagina ha corretto la visualizzazione dello stato. Questo problema è stato risolto e le attività pianificate mostrano correttamente lo stato Pianificato senza richiedere un aggiornamento. (TGT-52937)

+++

**[!UICONTROL Analytics for Target](A4T)**

+++Vedi i dettagli
* **È stato risolto un problema che impediva ai clienti di digitare i nomi delle suite di rapporti durante il processo di creazione attività**: i clienti che utilizzavano [!DNL Adobe Analytics] come origine per la generazione di rapporti durante il processo di creazione attività non potevano digitare nell&#39;elenco a discesa [!UICONTROL Report Suite] per cercare suite di rapporti specifiche. Questo ha interessato i flussi di lavoro delle organizzazioni con un numero elevato di suite di rapporti, in cui lo scorrimento manuale ha ritardato notevolmente la configurazione. L’elenco a discesa non era ordinato alfabeticamente e non rispondeva in modo coerente all’input digitato, rendendo difficile individuare suite di rapporti come &quot;Office + Store - Web - Prod&quot;. Questo problema è stato risolto e i clienti possono ora eseguire ricerche in modo efficiente digitando i nomi delle suite di rapporti. (TGT-53345)

+++

**[!UICONTROL Audiences]**

+++Vedi i dettagli
* **È stato risolto un problema che impediva ai tipi di pubblico con &quot;intervallo di tempo&quot; scaduti di salvare le attività anche dopo la rimozione**: i clienti non potevano salvare le attività nell&#39;interfaccia utente aggiornata a causa di un errore relativo ai tipi di pubblico con &quot;intervallo di tempo&quot; scaduti. Anche dopo aver rimosso il pubblico interessato, il messaggio di errore persisteva: &quot;L’attività contiene un pubblico con un intervallo di tempo non valido&quot;. Questo problema si verificava perché il sistema continuava a convalidare il pubblico per sola attività, anche quando non era più in uso. Il comportamento è stato ulteriormente complicato dalle discrepanze di fuso orario. La logica di convalida è stata corretta e i clienti ora possono salvare le attività senza incontrare questo errore. (TGT-53517)

+++

**[!UICONTROL Experience Fragment]s**

+++Vedi i dettagli
* **È stato risolto un problema che impediva ai clienti di inserire frammenti di esperienza utilizzando [!UICONTROL Insert Before] o [!UICONTROL Insert After] nell&#39;interfaccia utente**. I clienti hanno riscontrato un errore durante il tentativo di inserire [!UICONTROL Experience Fragments] in un&#39;attività utilizzando le opzioni &quot;Inserisci prima&quot; o &quot;Inserisci dopo&quot; nell&#39;interfaccia utente aggiornata. Il messaggio di errore visualizzato era: &quot;Il contenuto dell’offerta deve contenere esattamente un elemento HTML&quot;. Questo problema era specifico dell’interfaccia utente aggiornata e non si verificava nella versione precedente. Il problema è stato risolto e i clienti possono inserire [!UICONTROL Experience Fragments] senza incontrare questo errore. (TGT-53442)

+++

**[!UICONTROL Offer decisions]**

+++Vedi i dettagli
* **È stato risolto un problema che impediva ai clienti di modificare le offerte decisionali e di selezionare elementi di pagina specifici nell&#39;interfaccia utente aggiornata**: Nel processo di creazione attività aggiornato, i clienti non potevano modificare le offerte decisionali esistenti o selezionare elementi di pagina specifici nel Compositore esperienza visivo. Le offerte relative alle decisioni non venivano visualizzate correttamente come offerte HTML e le modifiche apportate durante la modifica non venivano salvate. Inoltre, alcuni URL regionali, come il sito Giappone, non venivano caricati correttamente nel Compositore esperienza visivo, bloccando la creazione e gli aggiornamenti dell’attività. Le offerte decisionali ora vengono visualizzate correttamente, gli elementi di pagina sono selezionabili come previsto e gli URL regionali vengono caricati correttamente nel Compositore esperienza visivo, ripristinando la funzionalità di modifica completa. (TGT-53425)
* **È stato risolto un problema che impediva la modifica e la modifica imprevista di [!UICONTROL Offer Decision] selettori dopo il salvataggio**: nel processo di creazione attività aggiornato, i clienti non potevano modificare il selettore [!UICONTROL Offer Decision] come previsto. Tentativi di modifica del selettore non riusciti e il selettore è tornato a un valore errato dopo il salvataggio. Questo comportamento ha causato la scomparsa dell’offerta decisionale dal Compositore esperienza visivo, bloccando ulteriori modifiche. Le modifiche del selettore ora vengono mantenute correttamente e le offerte di decisione rimangono visibili e modificabili nel Compositore esperienza visivo dopo il salvataggio.(TGT-53433)
* **È stato risolto un problema che causava la scomparsa di [!UICONTROL Offer Decisions] dall&#39;attività dopo il salvataggio**: [!UICONTROL Offer Decisions] aggiunti durante il processo di creazione attività non venivano mantenuti dopo il salvataggio e la riapertura dell&#39;attività. Questo problema si verificava durante la modifica del contenuto dinamico e l&#39;inserimento di [!UICONTROL Offer Decisions] con selettori e proprietà specifici. [!UICONTROL Offer Decisions] persiste correttamente dopo il salvataggio e i selettori rimangono intatti, garantendo un comportamento di targeting e modifica coerente. (TGT-53434)

+++

**[!DNL Recommendations]**

+++Vedi i dettagli
* **È stato risolto un problema nell&#39;interfaccia utente di [!DNL Recommendations] a causa del quale il download del file CSV dei criteri personalizzati restituiva l&#39;errore 404**: è stato risolto un problema che impediva ai clienti di scaricare il file CSV dei criteri personalizzati nel processo di creazione delle attività. Il collegamento per il download ora funziona correttamente, consentendo ai clienti di esportare i criteri personalizzati come previsto. (TGT-51966)
* **È stato corretto il caricamento incoerente delle immagini in[!UICONTROL Catalog Search]**: è stato risolto un problema che impediva il caricamento coerente delle miniature e delle immagini in [!UICONTROL  Catalog Search] nel processo di creazione attività. Le immagini non venivano visualizzate a meno che la colonna &quot;URL miniatura&quot; non fosse visibile e alcune immagini di prodotto venivano caricate parzialmente o non completamente dopo le azioni di navigazione o ricerca. Il comportamento di caricamento delle immagini è stato stabilizzato e le miniature ora vengono visualizzate in modo affidabile, indipendentemente dalla visibilità delle colonne o dalle azioni di navigazione. (TGT-52778)
* **È stato risolto un problema a causa del quale la modifica di un consiglio in un&#39;esperienza duplicata influiva sull&#39;esperienza originale**: i clienti segnalavano che la modifica di un consiglio in un&#39;esperienza duplicata alterava involontariamente l&#39;esperienza originale. In particolare, dopo aver duplicato l’esperienza B nel processo di creazione delle attività e averne modificato la progettazione o i criteri, le stesse modifiche sono state applicate all’esperienza B originale, nonostante fossero entità separate. Le esperienze duplicate ora mantengono configurazioni separate, garantendo che le modifiche apportate a un’esperienza non influiscano sull’originale. (TGT-53369)
* **È stato risolto un problema a causa del quale le modifiche apportate a un&#39;esperienza duplicata influivano involontariamente sull&#39;esperienza originale in un&#39;attività**: i clienti hanno segnalato che quando si duplicava un&#39;esperienza all&#39;interno di un&#39;attività e si assegnava un nuovo pubblico, qualsiasi modifica apportata alla progettazione o ai criteri dell&#39;esperienza duplicata veniva riportata anche nell&#39;esperienza originale. Questo problema si verificava anche se non venivano apportate modifiche direttamente alla versione originale, con conseguente impatto sulla possibilità di creare varianti indipendenti all’interno della stessa attività. Il processo di creazione attività ora isola correttamente le esperienze duplicate, garantendo che le modifiche apportate a un’esperienza non influiscano sull’originale. (TGT-53361)
* **È stato risolto un problema che impediva a intermittenza a [!UICONTROL Recommendation Catalog] di visualizzare i dati completi degli attributi del prodotto**: nell&#39;interfaccia utente [!DNL Recommendations] aggiornata, si è verificato un problema a causa del quale alcuni attributi del prodotto, ad esempio il messaggio, non venivano visualizzati in modo coerente nei risultati [!UICONTROL Catalog Search], anche se i dati erano presenti nel feed. Questo problema richiedeva ai clienti di riconfigurare manualmente la visibilità delle colonne per recuperare i valori mancanti. [!UICONTROL Catalog Search] visualizza ora in modo affidabile tutti gli attributi configurati, eliminando la necessità di reimpostare manualmente le colonne. (TGT-52769)
* **È stato risolto un problema che impediva la disabilitazione di [!UICONTROL Front Promotion] in un&#39;attività live**: i tentativi di disabilitare [!UICONTROL Front Promotion] in un&#39;attività live non venivano salvati. Dopo aver selezionato [!UICONTROL Change Promotion] e averlo disabilitato, la promozione è rimasta attiva durante la modifica dell&#39;attività, impedendo gli aggiornamenti alle configurazioni dei consigli. Le impostazioni della promozione ora vengono salvate correttamente, consentendo ai clienti di disabilitare o modificare le promozioni nelle attività live come previsto. (TGT-53231)
* **È stato risolto un problema che causava l&#39;attivazione di [!DNL Recommendations] [!UICONTROL Promotion] senza dati e causava un messaggio di errore non chiaro**: se si abilitava [!UICONTROL Front] o [!UICONTROL Back Promotion] in un&#39;attività [!DNL Recommendations] senza specificare i valori richiesti, veniva visualizzato un messaggio generico di errore di input non valido. Il problema di base era un campo di configurazione mancante, ma il messaggio di errore non indicava chiaramente la causa, rendendo difficile la risoluzione dei problemi. Il processo di creazione attività fornisce ora un messaggio di errore chiaro e actionable quando mancano campi obbligatori, come `collectionId` o regole, che consente ai clienti di identificare e risolvere rapidamente i problemi di configurazione. (TGT-52616)
* **È stato risolto un problema che impediva la visualizzazione dell&#39;elenco [!UICONTROL Product] nella finestra modale [!UICONTROL Edit] nella scheda [!UICONTROL Recommendations]**: i clienti non potevano visualizzare l&#39;elenco di prodotti filtrato durante la modifica di un [!UICONTROL collection] o [!UICONTROL exclusion] nella scheda [!UICONTROL Recommendations]. L’elenco doveva essere aggiornato in tempo reale in base alle regole applicate, ma non veniva visualizzato come previsto. Questo problema è stato risolto e l’elenco dei prodotti ora viene visualizzato correttamente e viene aggiornato in modo dinamico man mano che le regole vengono modificate. (TGT-53481)
* **È stato risolto un problema con il layout della finestra di dialogo Visualizza dettagli nell&#39;interfaccia utente aggiornata**: il layout della finestra modale Visualizza dettagli nell&#39;interfaccia utente aggiornata è stato modificato per migliorarne la chiarezza e l&#39;usabilità. La finestra di dialogo ora include due schede:
   * Scheda [!UICONTROL Details]: visualizza tutte le informazioni rilevanti per l&#39;elemento selezionato.
   * Scheda [!UICONTROL Inventory]: mostra tutti i prodotti filtrati in base alle regole di raccolta ed esclusione correnti.

  Questo miglioramento consente ai clienti di navigare e comprendere più facilmente i dati specifici degli articoli e il contesto dell’inventario all’interno del processo di creazione delle attività. (TGT-53503)

   * **È stato risolto un problema che causava la ricomparsa delle promozioni rimosse nelle attività di consigli dopo il salvataggio**: i clienti hanno segnalato che quando [!UICONTROL front] o [!UICONTROL back] promozioni sono state rimosse dalle attività [!DNL Recommendations] e l&#39;attività è stata salvata, le promozioni continuavano a essere visualizzate alla riapertura. Questo problema si verificava sia negli ambienti di staging che in quelli di produzione e interessava il processo aggiornato di creazione delle attività. Il problema è stato risolto. Le promozioni rimosse da un&#39;attività ora persistono correttamente dopo il salvataggio. (TGT-53490)

+++

**Rapporti**

+++Vedi i dettagli
* **È stato risolto un problema che causava la visualizzazione di valori di pubblico nulli da parte del report [!UICONTROL Automated Segments]**: i clienti hanno segnalato che [!UICONTROL Automated Segments] nei report di attività mostravano valori nulli per i dati di pubblico, impedendo un&#39;analisi accurata delle prestazioni dei segmenti. Questo problema si verificava quando si accedeva alla sezione [!UICONTROL Reports] e si selezionava [!UICONTROL Automated Segments], anche se erano previsti dati di pubblico validi. [!UICONTROL Automated Segments] ora visualizza correttamente i valori del pubblico, garantendo report affidabili e informazioni sulla segmentazione. (TGT-52793)

+++

**Applicazioni a pagina singola (SPA)**

+++Vedi i dettagli
* **È stato risolto un problema che causava la reimpostazione dello stato dell&#39;applicazione a pagina singola nell&#39;interfaccia utente aggiornata[!UICONTROL Browse] quando si passava dalla modalità [!UICONTROL Design] alla modalità**: i clienti hanno segnalato che il passaggio dalla modalità [!UICONTROL Browse] alla modalità [!UICONTROL Design] nell&#39;interfaccia utente aggiornata causava il ricaricamento dell&#39;editor Web, reimpostando lo stato delle applicazioni a pagina singola. Questo problema ha interrotto i flussi di lavoro e ha richiesto ai clienti di inserire nuovamente le informazioni. Il problema è stato risolto. Lo stato di un’applicazione a pagina singola viene ora mantenuto quando si passa da una modalità all’altra, garantendo un’esperienza più fluida e coerente durante la creazione di attività. (TGT-53074)

+++

**[!UICONTROL Visual Experience Composer](VEC)**

+++Vedi i dettagli
* **È stato risolto un problema nel processo di creazione attività che bloccava la progressione al passaggio [!UICONTROL Targeting] nelle attività di Personalizzazione automatizzata**: è stato risolto un problema nel processo di creazione attività a causa del quale i clienti non potevano procedere al passaggio [!UICONTROL Targeting] nelle attività [!UICONTROL Automated Personalization] (Personalizzazione automatizzata) a meno che non fossero state aggiunte due posizioni. Questo comportamento era diverso dall’esperienza precedente, in cui era sufficiente una singola posizione con più offerte. Il requisito è stato corretto, consentendo ai clienti di continuare a utilizzare le impostazioni per una singola posizione come parte dei flussi di lavoro di Personalizzazione automatizzata. (TGT-53426)
* **È stato risolto un problema che impediva al nuovo processo di creazione attività di impostare il parametro fmt=png-alpha per le immagini trasparenti**: nell&#39;interfaccia utente aggiornata, le immagini inserite durante il processo di creazione attività non includevano più il parametro `fmt=png-alpha` per impostazione predefinita, con conseguente perdita di trasparenza. Questo comportamento era diverso dalla precedente interfaccia utente, che aggiungeva automaticamente il parametro agli URL delle immagini, mantenendo gli sfondi trasparenti. Il processo di creazione attività ora applica correttamente il parametro `fmt=png-alpha` agli URL immagine quando è richiesta la trasparenza, garantendo il rendering coerente delle risorse trasparenti. (TGT-52615)
* **È stato risolto un problema che impediva ai clienti di cercare le suite di rapporti nell&#39;interfaccia utente aggiornata**: nell&#39;interfaccia utente aggiornata, l&#39;elenco a discesa [!UICONTROL Report Suites] nella sezione [!UICONTROL Goals & Settings] non consentiva ai clienti di digitare e cercare, rendendo difficile individuare suite di rapporti specifiche, in particolare per i tenant con un numero elevato di voci. A differenza dell’interfaccia utente precedente, l’elenco non era ordinato e mancava di filtri basati sugli input. Questo problema è stato risolto. Ora i clienti possono digitare per cercare e filtrare le suite di rapporti, ripristinando le funzionalità disponibili nell’interfaccia utente legacy. (TGT-53514)

+++

**[!UICONTROL Workspaces]**

+++Vedi i dettagli
* **È stato risolto un problema che consentiva a un cliente limitato a una sola area di lavoro di visualizzare le attività di altre aree di lavoro**: i clienti con accesso limitato a una sola area di lavoro potevano visualizzare in modo imprevisto le attività di tutte le aree di lavoro selezionando [!UICONTROL All Workspaces] nel processo di creazione attività. Questa visibilità comportava il rischio di modifiche non intenzionali alle attività live in altre aree di lavoro, con un potenziale impatto sulle prestazioni del sito web. I controlli di accesso a Workspace sono stati rafforzati per garantire che i clienti possano visualizzare e interagire solo con le attività all’interno dell’area di lavoro assegnata. (TGT-53101)
* **È stato risolto un problema che consentiva a un cliente di visualizzare le attività da [!UICONTROL Default Workspace] senza avere accesso:** Un cliente con accesso limitato all&#39;area di lavoro di staging era in grado di visualizzare le attività da [!UICONTROL Default Workspace] tramite il processo di creazione attività. Questo comportamento si è verificato nonostante la configurazione di back-end e i diritti di accesso corretti. I controlli di accesso a Workspace sono stati rafforzati per garantire che i clienti possano visualizzare le attività solo all’interno dell’area di lavoro assegnata.(TGT-53297)

+++

## Note aggiuntive e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK]&#x200B;(https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js di [!DNL Adobe Target]. |

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud], iscriviti ad [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
