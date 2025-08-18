---
keywords: allocazione automatica del traffico;targeting;Incrementa il conteggio e mantieni l'utente nell'attività;allocazione automatica;allocazione automatica
description: Scopri come utilizzare un'attività [!UICONTROL Auto-Allocate] in [!DNL Adobe Target] che identifica un vincitore tra due o più esperienze e ridistribuisce automaticamente più traffico per il vincitore.
title: Cos'è un'attività [!UICONTROL Auto-Allocate]?
feature: Auto-Allocate
exl-id: 2d1ddd71-2ca6-4f00-9d0c-eb25ede8fdb8
source-git-commit: 1b1b2271738d12f8da4e695900b70e280f50d8cf
workflow-type: tm+mt
source-wordcount: '3502'
ht-degree: 35%

---

# Panoramica di [!UICONTROL Auto-Allocate]

Un&#39;attività [!UICONTROL Auto-Allocate] in [!DNL Adobe Target] identifica un vincitore tra due o più esperienze e ridistribuisce automaticamente più traffico per aumentare le conversioni, mentre il test continua a essere eseguito e ad apprendere.

Durante la [creazione di un&#39;attività A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) tramite il flusso di lavoro guidato in tre passaggi, scegliere l&#39;opzione **[!UICONTROL Auto-Allocate to best experience]** nella pagina **[!UICONTROL Targeting]** (passaggio 2).

## La sfida {#section_85D5A03637204BACA75E19646162ACFF}

I test A/B standard hanno un costo intrinseco. Devi investire del traffico per misurare le prestazioni di ogni esperienza e capire quale sia l’esperienza vincente attraverso l’analisi. La distribuzione del traffico rimane fissa anche dopo aver compreso che alcune esperienze hanno prestazioni migliori di altre. Inoltre, è complicato calcolare la dimensione necessaria del campione, e l’attività deve essere eseguita completamente prima di poter intervenire in base al vincitore. E c&#39;è ancora la possibilità che il vincitore identificato non sia un vero vincitore.

## Soluzione: [!UICONTROL Auto-Allocate] {#section_98388996F0584E15BF3A99C57EEB7629}

Un&#39;attività [!UICONTROL Auto-Allocate] riduce il costo e il sovraccarico associati alla determinazione di un&#39;esperienza vincente. [!UICONTROL Auto-Allocate] monitora le prestazioni della metrica obiettivo di tutte le esperienze e invia in modo proporzionale un numero maggiore di nuovi partecipanti alle esperienze con prestazioni migliori. Per l’esplorazione delle altre esperienze viene riservata una quantità adeguata di traffico. È possibile vedere i vantaggi del test nei risultati, anche se l’attività è ancora in esecuzione: l’ottimizzazione si verifica in parallelo all’apprendimento.

[!UICONTROL Auto-Allocate] sposta gradualmente i visitatori verso esperienze vincenti, invece di richiedere di attendere che un&#39;attività finisca per determinare un vincitore. Puoi beneficiare di incrementi più rapidi perché potenziali esperienze vincenti vengono mostrate a partecipanti che sarebbero altrimenti stati destinati a esperienze di minor successo.

Un normale test A/B in [!DNL Target] mostra solo confronti a coppie di sfidanti con il controllo. Ad esempio, se un&#39;attività ha esperienze: A, B, C e D dove A è il controllo, un normale test A/B [!DNL Target] confronterebbe A con B, A con C e A con D.

In questi test, la maggior parte dei prodotti, incluso [!DNL Target], utilizza un test t di [Welch](https://en.wikipedia.org/wiki/Welch%27s_t-test){target=_blank} per produrre un&#39;affidabilità basata sul valore p. Questo valore di affidabilità viene quindi utilizzato per determinare se lo sfidante è sufficientemente diverso dal controllo. Tuttavia, [!DNL Target] non esegue automaticamente i confronti impliciti (B con C, B con D e C con D) necessari per trovare l&#39;esperienza &quot;migliore&quot;. Di conseguenza, l’addetto al marketing deve analizzare manualmente i risultati per determinare l’esperienza “migliore”.

[!UICONTROL Auto-Allocate] esegue tutti i confronti impliciti tra le esperienze e produce un vincitore &quot;vero&quot;. Non vi è alcuna nozione di esperienza di “controllo” nel test.

[!UICONTROL Auto-Allocate] alloca in modo intelligente nuovi visitatori alle esperienze finché l&#39;intervallo di affidabilità della migliore esperienza non si sovrappone all&#39;intervallo di affidabilità di qualsiasi altra esperienza. Normalmente questo processo potrebbe produrre falsi positivi, ma [!UICONTROL Auto-Allocate] utilizza intervalli di affidabilità in base alla [disuguaglianza di Bernstein](https://en.wikipedia.org/wiki/Bernstein_inequalities_%28probability_theory%29){target=_blank} che compensa le valutazioni ripetute. A questo punto, c&#39;è un vero vincitore. Quando [!UICONTROL Auto-Allocate] si arresta, purché non vi sia una dipendenza sostanziale dal tempo per i visitatori che arrivano alla pagina, c&#39;è almeno un 95% di probabilità che [!UICONTROL Auto-Allocate] restituisca un&#39;esperienza la cui vera risposta non sia peggiore dell&#39;1% (relativo) inferiore alla vera risposta dell&#39;esperienza vincente.

## Quando utilizzare [!UICONTROL Auto-Allocate] rispetto a [!UICONTROL A/B Test] o [!UICONTROL Automated Personalization] attività {#section_3F73B0818A634E4AAAA60A37B502BFF9}

* Utilizza **[!UICONTROL Auto-Allocate]** per ottimizzare l&#39;attività fin dall&#39;inizio e identificare le esperienze vincenti il più rapidamente possibile. Rendendo più frequenti le esperienze ad alte prestazioni, le prestazioni complessive dell’attività aumentano.
* Utilizza un **[test A/B](/help/main/c-activities/t-test-ab/test-ab.md#task_05E33EB15C4D4459B5EAFF90A94A7977)** standard quando vuoi caratterizzare le prestazioni di tutte le esperienze prima di ottimizzare il sito. Un test A/B consente di classificare tutte le esperienze, mentre [!UICONTROL Auto-Allocate] trova le migliori prestazioni ma non garantisce la differenziazione tra le prestazioni più basse.
* Utilizza [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9) quando desideri algoritmi di ottimizzazione della complessità più elevata, ad esempio modelli di apprendimento automatico che generano previsioni basate su attributi di profilo individuali. [!UICONTROL Auto-Allocate] esamina il comportamento aggregato delle esperienze (proprio come i test A/B standard) e non distingue tra visitatori.

## Vantaggi chiave di [!UICONTROL Auto-Allocate] {#section_0913BF06F73C4794862561388BBDDFF0}

* Mantiene la rigorosità di un test A/B
* Trova un vincitore statisticamente significativo più velocemente rispetto a un test A/B manuale.
* Fornisce un maggiore incremento medio della campagna rispetto a un test A/B manuale.

## Terminologia  {#section_670F8785BA894745B43B6D4BFF953188}

I seguenti termini sono utili quando si parla di [!UICONTROL Auto-Allocate]:

**Slot machine:** un approccio all’ottimizzazione ti tipo [slot machine](https://en.wikipedia.org/wiki/Multi-armed_bandit){target=_blank} compensa l’apprendimento esplorativo e il suo sfruttamento.

## Funzionamento dell’algoritmo {#section_ADB69A1C7352462D98849F2918D4FF7B}

La logica complessiva alla base di [!UICONTROL Auto-Allocate] include sia le prestazioni misurate (come il tasso di conversione) che gli intervalli di affidabilità dei dati cumulativi. A differenza di un test A/B standard in cui il traffico viene suddiviso in modo uniforme tra le esperienze, [!UICONTROL Auto-Allocate] modifica l&#39;allocazione del traffico tra le esperienze.

* L&#39;80% dei visitatori è assegnato utilizzando la logica intelligente descritta di seguito.
* Il 20% dei visitatori viene assegnato in modo casuale in tutte le esperienze per adattarsi al cambiamento del comportamento del visitatore.

L&#39;approccio slot machine consente di riservare alcune esperienze all’esplorazione, sfruttando le esperienze che danno buoni risultati. Un numero maggiore di nuovi visitatori vedrà le esperienze migliori, ma sarà comunque possibile reagire in caso di condizioni mutevoli. Questi modelli si aggiornano almeno una volta all&#39;ora per assicurarsi che il modello reagisca ai dati più recenti.

Man mano che più visitatori accedono all’attività, alcune esperienze iniziano a dimostrarsi di maggior successo e viene quindi incrementato il traffico inviato a tali esperienze. Il 20% del traffico continua a contribuire casualmente all’esplorazione di tutte le esperienze. Se una delle esperienze dalle prestazioni peggiori inizia a ottenere risultati migliori, le viene allocato più traffico. Oppure se il successo di un’attività con ottime prestazioni diminuisce, le viene assegnato meno traffico. Questo si verifica ad esempio se i visitatori cercano informazioni diverse sul tuo sito multimediale a causo di un particolare evento oppure se le offerte speciali del fine settimana nel tuo sito retail generano risultati diversi.

L’illustrazione seguente rappresenta il comportamento dell’algoritmo durante un test con quattro esperienze (fai clic per espandere l’illustrazione):

![immagine allocata automaticamente](assets/auto-allocate.png){width="600" zoomable="yes"}

L&#39;illustrazione mostra come il traffico assegnato a ogni esperienza progredisca nell&#39;acro di parecchi turni della durata dell&#39;attività, finché non sia possibile determinare un chiaro vincitore.

| Arrotondamento | Descrizione |
|--- |--- |
| ![Turno di riscaldamento](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-0.png){width="200" zoomable="yes"} | **Turno di riscaldamento (0)**: durante il turno di riscaldamento, ogni esperienza ottiene pari ripartizione del traffico fino a quando ogni esperienza in attività ha un minimo di 1.000 visitatori e 50 conversioni.<ul><li>Esperienza A=25%</li><li>Esperienza B=25%</li><li>Esperienza C=25%</li><li>Esperienza D=25%</li></ul>Dopo che ogni esperienza ottiene 1.000 visitatori e 50 conversioni, [!DNL Target] avvia l&#39;allocazione automatica del traffico. Tutte le allocazioni avvengono in turni e vengono raccolte due esperienze per ogni turno.<br>Solo due esperienze progrediscono al turno successivo: D e C.<br>Progredire significa che alle due esperienze è assegnato l&#39;80% del traffico equamente. Le altre due esperienze continuano a partecipare, ma vengono gestite solo come parte dell’allocazione casuale del traffico del 20% quando nuovi visitatori accedono all’attività.<br>Tutte le allocazioni vengono aggiornate ogni ora (mostrato in alto per turni lungo l&#39;asse x). Dopo ogni turno, i dati cumulativi vengono confrontati. |
| ![Turno 1](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-1.png){width="200" zoomable="yes"} | **Turno 1**: durante questo turno, l’80% di traffico è assegnato alle esperienze C e D (40% ciascuna). Il 20% del traffico viene assegnato in modo casuale alle esperienze A, B, C e D (5% ciascuna). Durante questo turno, l&#39;esperienza A registra buoni risultati.<ul><li>L&#39;algoritmo sceglie l&#39;esperienza D per passare al turno successivo perché ha il più alto tasso di conversione (come indicato dalla scala verticale di ogni attività).</li><li>L&#39;algoritmo sceglie anche l&#39;esperienza A per proseguire perché, tra le esperienze rimanenti, ha il limite superiore più alto dell&#39;intervallo di affidabilità Bernstein al 95%.</li></ul>Le esperienze D e A proseguono. |
| ![Turno 2](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-2.png){width="200" zoomable="yes"} | **Turno 2**: durante questo turno, l’80% del traffico è assegnato alle esperienze A e D (40% ciascuna). Il 20% del traffico è allocato in modo casuale, quindi A, B, C e D ricevono rispettivamente il 5% del traffico. Durante questo turno, l’esperienza B registra buoni risultati.<ul><li>L&#39;algoritmo sceglie l&#39;esperienza D per passare al turno successivo perché ha il più alto tasso di conversione (come indicato dalla scala verticale di ogni attività).</li><li>L&#39;algoritmo sceglie anche l&#39;esperienza B per proseguire perché, tra le esperienze rimanenti, ha il limite superiore più alto dell&#39;intervallo di affidabilità Bernstein al 95%.</li></ul>Le esperienze D e B proseguono. |
| ![Turno 3](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-3.png){width="200" zoomable="yes"} | **Turno 3**: durante questo turno, l’80% di traffico è assegnato alle esperienze B e D (40% ciascuna). Il 20% del traffico è allocato in modo casuale, quindi A, B, C e D ricevono rispettivamente il 5% del traffico. Durante questo turno, l&#39;esperienza D continua a fornire buoni risultati, così come l&#39;esperienza C.<ul><li>L&#39;algoritmo sceglie l&#39;esperienza D per passare al turno successivo perché ha il più alto tasso di conversione (come indicato dalla scala verticale di ogni attività).</li><li>L&#39;algoritmo sceglie anche l&#39;esperienza C per proseguire perché, tra le esperienze rimanenti, ha il limite superiore più alto dell&#39;intervallo di affidabilità Bernstein al 95%.</li></ul>Le esperienze D e C proseguono. |
| ![Turno 4](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-4.png){width="200" zoomable="yes"} | **Turno 4**: durante questo turno, l’80% di traffico è assegnato alle esperienze C e D (40% ciascuna). Il 20% del traffico è allocato in modo casuale, quindi A, B, C e D ricevono rispettivamente il 5% del traffico. Durante questo turno, l&#39;esperienza C risulta avere buone prestazioni.<ul><li>L&#39;algoritmo sceglie l&#39;esperienza C per passare al turno successivo perché ha il più alto tasso di conversione (come indicato dalla scala verticale di ogni attività).</li><li>L&#39;algoritmo sceglie anche l&#39;esperienza D per proseguire perché, tra le esperienze rimanenti, ha il limite superiore più alto dell&#39;intervallo di affidabilità Bernstein al 95%.</li></ul>Le esperienze C e D proseguono. |
| ![Turno n](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-n.png){width="200" zoomable="yes"} | **Turno *n***: mentre l&#39;attività progredisce, inizia a emergere un&#39;esperienza con prestazioni elevate e il processo continua fino a quando non si verifica un&#39;esperienza vincente. Quando l’intervallo di affidabilità dell’esperienza con il tasso di conversione più alto non si sovrappone all’intervallo di affidabilità di qualsiasi altra esperienza, viene etichettato come vincitore. Un distintivo [ viene visualizzato nella pagina dell&#39;attività vincente](/help/main/c-activities/automated-traffic-allocation/determine-winner.md) e nell&#39;elenco [!UICONTROL Activity].<ul><li>L&#39;algoritmo sceglie l’esperienza C come chiaro vincitore.</li></ul>A questo punto l&#39;algoritmo indirizza l’80% del traffico all’esperienza C, mentre il 20% del traffico continua a essere indirizzato casualmente a tutte le esperienze (A, B, C e D). In totale, C ottiene l’85% del traffico. Nel caso improbabile che l’intervallo di affidabilità del vincitore inizi a sovrapporsi di nuovo cpn quello di un’altra esperienza, l’algoritmo ritorna al comportamento del turno 4 di cui sopra.<P>**Importante**: se hai scelto manualmente un vincitore in una fase precedente del processo, sarebbe stato facile scegliere l&#39;esperienza sbagliata. Per questo motivo, è consigliabile attendere che l’algoritmo determini l’esperienza vincente. |

>[!NOTE]
>
>Se un&#39;attività ha solo due esperienze, entrambe ottengono la stessa quantità di traffico fino a quando [!DNL Target] trova un&#39;esperienza vincente con il 75% di affidabilità. A quel punto, due terzi del traffico vengono assegnati al vincitore e un terzo al perdente. Successivamente, quando un’esperienza raggiunge il 95% di affidabilità, il 90% del traffico viene assegnato al vincitore e il 10% al perdente. [!DNL Target] invia sempre del traffico all&#39;esperienza &quot;perdente&quot; per evitare falsi positivi alla fine (ovvero, mantieni alcune esplorazioni).

Dopo l&#39;attivazione di un&#39;attività [!UICONTROL Auto-Allocate], le seguenti operazioni dall&#39;interfaccia utente Target non sono consentite:

* Impostazione della modalità di Allocazione traffico su Manuale
* Modifica del tipo di metrica obiettivo
* Modifica delle opzioni nel pannello &quot;[!UICONTROL Advanced Settings]&quot;

## Scopri come funziona l’allocazione automatica

Per ulteriori informazioni, vedere [L&#39;allocazione automatica può fornire risultati di test più rapidi e ricavi più elevati rispetto a un test manuale](/help/main/c-activities/automated-traffic-allocation/faster-results-higher-revenue.md).

## Avvertenze {#section_5C83F89F85C14FD181930AA420435E1D}

Considera le seguenti informazioni mentre lavori con [!UICONTROL Auto-Allocate]:

### La funzionalità [!UICONTROL Auto-Allocate] funziona con una sola impostazione metrica avanzata: [!UICONTROL Increment Count and Keep User in Activity]

Le impostazioni di metrica avanzate seguenti non sono supportate: [!UICONTROL Increment Count], [!UICONTROL Release User], [!UICONTROL Allow Reentry and Increment Count] e [!UICONTROL Release User and Bar from Reentry].

### I visitatori di ritorno frequenti possono gonfiare i tassi di conversione dell’esperienza.

Se un visitatore che vede l’esperienza A torna frequentemente e la sua conversione si verifica più volte, il tasso di conversione (CR) dell’esperienza A aumenta artificialmente. Confronta questo risultato con l’esperienza B, dove i visitatori si convertono ma non tornano spesso. Di conseguenza, il CR dell’esperienza A ha un aspetto migliore del CR dell’esperienza B, pertanto è più probabile che i nuovi visitatori vengano assegnati ad A che a B. Se scegli di contare una volta per partecipante, il CR di A e CR di B potrebbero essere identici.

Se i visitatori di ritorno sono distribuiti in modo casuale, è più probabile che il loro effetto sui tassi di conversione venga mitigato. Per attenuare questo effetto, è consigliabile modificare il metodo di conteggio della metrica obiettivo per conteggiare ogni partecipante una sola volta.

### Differenzia tra i migliori e non tra i peggiori.

[!UICONTROL Auto-Allocate] è in grado di distinguere tra esperienze dalle prestazioni migliori (e trovare un vincitore). Ci potrebbero essere momenti in cui non vi è abbastanza differenziazione tra le esperienze con prestazioni inferiori.

Se desideri produrre una differenziazione statisticamente significativa tra tutte le esperienze, puoi utilizzare la modalità di allocazione manuale del traffico.

### I tassi di conversione correlati al tempo (o contestualmente variabili) possono distorcere le quantità di allocazione.

Alcuni fattori che possono essere ignorati durante un test A/B standard perché influiscono ugualmente su tutte le esperienze non possono essere ignorati in un&#39;attività [!UICONTROL Auto-Allocate]. L’algoritmo è sensibile ai tassi di conversione osservati.

Di seguito sono riportati alcuni esempi di fattori che possono influenzare le prestazioni dell&#39;esperienza in modo disuguale:

* Esperienze con diversa rilevanza contestuale (tempo, posizione, genere e così via).

  Ad esempio:

   * &quot;Grazie a Dio è venerdì&quot; ha fatto aumentare le conversioni di venerdì.
   * &quot;Jump-start your Monday&quot; ha una conversione più alta il lunedì.
   * &quot;Prepararsi per un inverno della costa orientale&quot; fornisce una maggiore conversione nelle zone della costa orientale o in quelle afflitte dall&#39;inverno.

  L&#39;utilizzo di esperienze con rilevanza contestuale variabile può distorcere i risultati in un test [!UICONTROL Auto-Allocate] più che in un test A/B perché il test A/B analizza i risultati su un periodo più lungo.

* Esperienze con ritardi diversi nella conversione possono essere dovute all’urgenza del messaggio.

  Ad esempio, “i saldi al 30% finiscono oggi” incita il visitatore ad eseguire oggi stesso la conversione, mentre “50% di sconto sul primo acquisto” non crea lo stesso senso di urgenza.

## Domande frequenti  {#section_0E72C1D72DE74F589F965D4B1763E5C3}

Consulta le seguenti domande frequenti e risposte mentre lavori con [!UICONTROL Auto-Allocate] attività:

### [!UICONTROL Analytics for Target] (A4T) supporta [!UICONTROL Auto-Allocate] attività?

Sì. Per ulteriori informazioni, consulta [Supporto A4T per attività di allocazione automatica e targeting automatico](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md).

### I visitatori di ritorno vengono riallocati automaticamente alle esperienze con prestazioni elevate?

No. Solo i nuovi visitatori vengono allocati automaticamente. I visitatori di ritorno continuano a vedere la loro esperienza originale per proteggere la validità del test A/B.

### In che modo l’algoritmo tratta i falsi positivi?

L’algoritmo garantisce un&#39;affidabilità del 95% o un tasso di falsa positività del 5% se si attende che appaia il badge del vincitore.

### Quando [!UICONTROL Auto-Allocate] inizia ad allocare il traffico?

L’algoritmo inizia a funzionare dopo che tutte le esperienze nell’attività hanno un minimo di 1.000 visitatori e 50 conversioni.

### Quanto aggressivamente viene applicato l’algoritmo?

L&#39;80% del traffico viene servito con [!UICONTROL Auto-Allocate] e il 20% del traffico viene servito in modo casuale. Quando viene identificato un vincitore, l&#39;80% del traffico viene indirizzato a tale vincitore, mentre tutte le esperienze continuano a ricevere una parte del traffico come parte del 20%, inclusa l&#39;esperienza vincente.

### Le esperienze perdenti vengono mostrate?

Sì. Con un approccio di tipo slot machine, almeno il 20% del traffico è riservato all’esplorazione di modifiche nei pattern o nei tassi di conversione in tutte le esperienze.

### Cosa succede alle attività con tempi di conversione lunghi?

Finché tutte le esperienze ottimizzate avranno ritardi simili, il comportamento sarà lo stesso di un’attività con un ciclo di conversione più veloce. Tuttavia, il raggiungimento della soglia di conversione di 50 richiede più tempo prima dell’inizio del processo di allocazione del traffico.

### Differenze tra [!UICONTROL Auto-Allocate] e [!UICONTROL Automated Personalization]

[!UICONTROL Automated Personalization] utilizza gli attributi del profilo di ogni visitatore per determinare l&#39;esperienza migliore. In tal modo, non solo ottimizza, ma personalizza anche l’attività per quell’utente.

[!UICONTROL Auto-Allocate] è invece un test A/B che produce un vincitore aggregato (l&#39;esperienza più popolare, ma non necessariamente quella più efficace per ogni visitatore).

### I visitatori di ritorno gonfiano il tasso di conversione sulla metrica di successo?

Attualmente, la logica favorisce i visitatori che si convertono rapidamente o che effettuano visite più frequenti, perché tali visitatori aumentano temporaneamente il tasso di conversione complessivo dell’esperienza a cui appartengono. L’algoritmo si regola frequentemente, quindi l’aumento del tasso di conversione viene amplificato in ogni istantanea. Se il sito riceve numerosi visitatori di ritorno, le loro conversioni possono potenzialmente aumentare il tasso di conversione complessivo per l’esperienza a cui appartengono. C&#39;è una buona probabilità che i visitatori di ritorno siano distribuiti in modo casuale, nel qual caso l’effetto aggregato (aumento dell’incremento) è mitigato. Per attenuare questo effetto, è consigliabile modificare il metodo di conteggio della metrica di sucesso per conteggiare ogni partecipante una sola volta.

### Posso utilizzare il Calcolatore dimensione campione quando utilizzo [!UICONTROL Auto-Allocate] per stimare il tempo necessario all&#39;attività per identificare il vincitore?

È possibile utilizzare il [!DNL Adobe Target] [Calcolatore dimensioni campione](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6) esistente per ottenere una stima della durata di esecuzione del test. (Come con i tradizionali test A/B, applica la correzione Bonferroni se stai sottoponendo a test più di due offerte o più di una metrica/ipotesi di conversione.) Questo calcolatore è progettato per il tradizionale test A/B a orizzonte fisso e fornisce solo una stima. L&#39;utilizzo del calcolatore per un&#39;attività [!UICONTROL Auto-Allocate] è facoltativo perché [!UICONTROL Auto-Allocate] dichiara un vincitore. Non è necessario scegliere un punto fisso nel tempo per esaminare i risultati del test. I valori forniti sono sempre statisticamente validi.

[!DNL Adobe] esperimenti interni hanno rilevato quanto segue:

* Quando esegue il test esattamente di due esperienze, [!UICONTROL Auto-Allocate] trova un vincitore più rapidamente del test a orizzonte fisso (ovvero l&#39;intervallo di tempo suggerito dal calcolatore delle dimensioni del campione) quando la differenza di prestazioni tra le esperienze è grande. Tuttavia, [!UICONTROL Auto-Allocate] potrebbe richiedere più tempo per identificare un vincitore quando la differenza di prestazioni tra le esperienze è ridotta. In questi casi, i test a orizzonte fisso si sarebbero in genere conclusi senza un risultato statisticamente significativo.
* Quando si sottopongono a test più di due esperienze, [!UICONTROL Auto-Allocate] trova un vincitore più rapidamente del test a orizzonte fisso (ovvero l&#39;intervallo di tempo suggerito dal calcolatore delle dimensioni del campione) quando una singola esperienza supera nettamente tutte le altre esperienze. Quando due o più esperienze sono entrambe &quot;vincenti&quot; rispetto ad altre ma strettamente correlate tra loro, [!UICONTROL Auto-Allocate] potrebbe richiedere più tempo per determinare quale sia superiore. In questi casi, i test a orizzonte fisso in genere si sarebbero conclusi concludendo che le esperienze &quot;vincenti&quot; erano migliori rispetto a quelle con prestazioni inferiori, ma non avevano identificato quale era superiore.

### È necessario rimuovere un&#39;esperienza insoddisfacente da un&#39;attività [!UICONTROL Auto-Allocate] per velocizzare il processo di determinazione di un vincitore?

Non c’è motivo di rimuovere un’esperienza insoddisfacente. [!UICONTROL Auto-Allocate] fornisce automaticamente esperienze con prestazioni elevate più spesso e fornisce esperienze con prestazioni inferiori con minore frequenza. Lasciare un’esperienza insoddisfacente nell’attività non influisce in modo significativo sulla velocità per determinare un vincitore.

Il 20% dei visitatori viene assegnato in modo casuale attraverso tutte le esperienze. La quantità di traffico utilizzata per un’esperienza insoddisfacente è minima (20% diviso per il numero di esperienze).

### Posso cambiare la metrica obiettivo a metà strada attraverso un&#39;attività [!UICONTROL Auto-Allocate]? {#change-metric}

[!DNL Adobe] non consiglia di modificare la metrica obiettivo a metà strada in un&#39;attività. Anche se è possibile modificare la metrica dell’obiettivo durante un’attività utilizzando l’interfaccia utente [!DNL Target], è sempre necessario avviare una nuova attività. [!DNL Adobe] non garantisce ciò che accade se si modifica la metrica obiettivo in un&#39;attività dopo che è in esecuzione.

Questo consiglio si applica alle attività [!UICONTROL Auto-Allocate], [!UICONTROL Auto-Target] e [!UICONTROL Automated Personalization] che utilizzano [!DNL Target] o [!DNL Analytics] (A4T) come origine per la generazione di rapporti.

### Posso cambiare l&#39;origine per la generazione di rapporti nel corso di un&#39;attività [!UICONTROL Auto-Allocate]? {#change-reporting}

[!DNL Adobe] non consiglia di cambiare l&#39;origine per la generazione di rapporti a metà strada attraverso un&#39;attività. Anche se è possibile modificare l&#39;origine per la generazione di rapporti (da [!DNL Target] a A4T o in modo opposto) durante un&#39;attività utilizzando l&#39;interfaccia utente di [!DNL Target], è sempre necessario avviare una nuova attività. [!DNL Adobe] non garantisce ciò che accade se si modifica l&#39;origine per la generazione di rapporti in un&#39;attività dopo che è in esecuzione.

Questo consiglio si applica alle attività [!UICONTROL Auto-Allocate], [!UICONTROL Auto-Target] e [!UICONTROL Automated Personalization] che utilizzano [!DNL Target] o [!DNL Analytics] (A4T) come origine per la generazione di rapporti.

### È possibile utilizzare l&#39;opzione [!UICONTROL Reset Report Data] durante l&#39;esecuzione di un&#39;attività [!UICONTROL Auto-Allocate]?

L&#39;utilizzo dell&#39;opzione [!UICONTROL Reset Report Data] per le attività [!UICONTROL Auto-Allocate] non è consigliato. Anche se rimuove i dati di reporting visibili, questa opzione non rimuove tutti i record di formazione dal modello [!UICONTROL Auto-Allocate]. Invece di utilizzare l&#39;opzione [!UICONTROL Reset Report Data] per le attività [!UICONTROL Auto-Allocate], crea una nuova attività e disattiva l&#39;attività originale. Questa guida si applica anche alle attività [!UICONTROL Auto-Target] e [!UICONTROL Automated Personalization].

### In che modo [!UICONTROL Auto-Allocate] genera i modelli rispetto agli ambienti?

[!UICONTROL Auto-Allocate] crea modelli in base al comportamento di traffico e conversione registrato solo nell&#39;ambiente predefinito. Per impostazione predefinita, [!UICONTROL Production] è l&#39;ambiente predefinito, ma l&#39;ambiente predefinito può essere modificato in [!DNL Target] ([Amministrazione > Ambienti](/help/main/administrating-target/environments.md)).

Se un hit si verifica in un altro ambiente (non predefinito), il traffico viene distribuito in base al comportamento di conversione osservato nell’ambiente predefinito. Il risultato di tale hit (conversione o non conversione) viene registrato a scopo di reporting ma non considerato nel modello [!UICONTROL Auto-Allocate].

Quando selezioni un altro ambiente, il rapporto mostra il traffico e le conversioni per tale ambiente. L’ambiente selezionato predefinito per un rapporto è l’ambiente predefinito a livello di account selezionato. L’ambiente predefinito non può essere impostato in base alle singole attività.

### Un&#39;attività [!UICONTROL Auto-Allocate] può modificare l&#39;intervallo di lookback nel corso di un test per considerare la possibilità di modificare le tendenze nel tempo?

Ad esempio, l’attività può considerare il mese di dicembre per decidere come allocare il traffico, anziché esaminare i dati dei visitatori di settembre (quando è iniziato il test)?

No, [!UICONTROL Auto-Allocate] considera le prestazioni dell&#39;intera attività.

### [!UICONTROL Auto-Allocate] mostra un&#39;esperienza vincente a un visitatore che ritorna, se l&#39;esperienza vincente è diversa da quella che ha visto quando si è qualificato per l&#39;attività?

[!UICONTROL Auto-Allocate] utilizza le decisioni permanenti per gli stessi motivi per cui le attività [!UICONTROL A/B Test] sono permanenti. L’allocazione del traffico funziona solo per i nuovi visitatori.

## Video di formazione {#section_893E5B36DC4A415C9B1D287F51FCCB83}

I video seguenti contengono ulteriori informazioni sui concetti descritti in questo articolo.

### Flusso di lavoro attività - Targeting (2:14) ![Icona esercitazione](/help/main/assets/tutorial.png)

Questo video include informazioni su come impostare l&#39;allocazione del traffico.

* Assegnare un pubblico all’attività
* Limitare il traffico verso l’alto o il basso
* Selezionare il metodo di allocazione del traffico
* Allocare il traffico tra diverse esperienze

>[!VIDEO](https://video.tv.adobe.com/v/17385)

### Creazione di test A/B (8:36) ![Icona esercitazione](/help/main/assets/tutorial.png)

In questo video viene illustrato come creare un test A/A utilizzando il flusso di lavoro guidato in tre passaggi di Target. [!UICONTROL Auto-Allocate] è discusso a partire dal 4:45.

* Crea un&#39;attività A/B in [!DNL Adobe Target]
* Allocare il traffico con suddivisione manuale o automatica del traffico

>[!VIDEO](https://video.tv.adobe.com/v/36325?captions=ita)
