---
keywords: allocazione automatica del traffico;targeting;Incrementa il conteggio e mantieni l'utente nell'attività;allocazione automatica;allocazione automatica
description: Scopri come utilizzare un’ [!UICONTROL Allocazione automatica] attività in [!DNL Adobe Target] che identifica un vincitore tra due o più esperienze e ridistribuisce automaticamente più traffico per il vincitore.
title: Che cos’è un’ [!UICONTROL Allocazione automatica] Attività?
feature: Auto-Allocate
exl-id: 2d1ddd71-2ca6-4f00-9d0c-eb25ede8fdb8
source-git-commit: 1b1b2271738d12f8da4e695900b70e280f50d8cf
workflow-type: tm+mt
source-wordcount: '3574'
ht-degree: 42%

---

# Panoramica sulla funzione [!UICONTROL Allocazione automatica]

Un [!UICONTROL Allocazione automatica] attività in [!DNL Adobe Target] identifica un vincitore tra due o più esperienze e ridistribuisce automaticamente più traffico per aumentare le conversioni, mentre il test continua a essere eseguito e ad apprendere.

Mentre [creazione di un’attività A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) utilizzando il flusso di lavoro guidato in tre passaggi, scegli **[!UICONTROL Allocazione automatica all’esperienza migliore]** opzione sul **[!UICONTROL Targeting]** pagina (passaggio 2).

## La sfida {#section_85D5A03637204BACA75E19646162ACFF}

I test A/B standard hanno un costo intrinseco. Devi investire del traffico per misurare le prestazioni di ogni esperienza e capire quale sia l’esperienza vincente attraverso l’analisi. La distribuzione del traffico rimane fissa anche dopo aver compreso che alcune esperienze hanno prestazioni migliori di altre. Inoltre, è complicato calcolare la dimensione necessaria del campione, e l’attività deve essere eseguita completamente prima di poter intervenire in base al vincitore. E c&#39;è ancora la possibilità che il vincitore identificato non sia un vero vincitore.

## La soluzione: [!UICONTROL Allocazione automatica] {#section_98388996F0584E15BF3A99C57EEB7629}

Un [!UICONTROL Allocazione automatica] L’attività di riduce questo costo e il sovraccarico associati al determinare un’esperienza vincente. [!UICONTROL L’allocazione automatica monitora le prestazioni della metrica obiettivo di tutte le esperienze e invia in modo proporzionale un numero maggiore di nuovi partecipanti alle esperienze che hanno prestazioni migliori. ] Per l’esplorazione delle altre esperienze viene riservata una quantità adeguata di traffico. È possibile vedere i vantaggi del test nei risultati, anche se l’attività è ancora in esecuzione: l’ottimizzazione si verifica in parallelo all’apprendimento.

[!UICONTROL L’allocazione automatica sposta gradualmente i visitatori verso esperienze vincenti, invece di richiedere di attendere fino a quando un’attività finisce per determinare un vincitore. ] Puoi beneficiare di incrementi più rapidi perché potenziali esperienze vincenti vengono mostrate a partecipanti che sarebbero altrimenti stati destinati a esperienze di minor successo.

Un normale test A/B in [!DNL Target] mostra solo confronti a coppie di sfidanti con il controllo. Ad esempio, se un’attività dispone di esperienze: A, B, C e D dove A è il controllo, un normale [!DNL Target] Il test A/B confronta A con B, A con C e A con D.

In tali test, la maggior parte dei prodotti, tra cui [!DNL Target], utilizza un [Test t di Welch](https://en.wikipedia.org/wiki/Welch%27s_t-test){target=_blank} per ottenere un livello di affidabilità basato sul valore p. Questo valore di affidabilità viene quindi utilizzato per determinare se lo sfidante è sufficientemente diverso dal controllo. Tuttavia, [!DNL Target] non esegue automaticamente i confronti impliciti (B con C, B con D e C con D) necessari per trovare l’esperienza &quot;migliore&quot;. Di conseguenza, l’addetto al marketing deve analizzare manualmente i risultati per determinare l’esperienza “migliore”.

[!UICONTROL L’allocazione automatica esegue tutti i confronti impliciti tra le esperienze e produce un vincitore “reale”. ] Non vi è alcuna nozione di esperienza di “controllo” nel test.

[!UICONTROL Allocazione automatica] assegna in modo intelligente nuovi visitatori alle esperienze fino a quando l’intervallo di affidabilità della migliore esperienza non si sovrappone a quello di qualsiasi altra esperienza. Normalmente questo processo potrebbe produrre falsi positivi, ma [!UICONTROL Allocazione automatica] utilizza intervalli di affidabilità basati su [Disuguaglianza di Bernstein](https://en.wikipedia.org/wiki/Bernstein_inequalities_%28probability_theory%29){target=_blank} che compensa le valutazioni ripetute. A questo punto, c&#39;è un vero vincitore. Quando [!UICONTROL Allocazione automatica] si ferma, purché non vi sia una dipendenza sostanziale dal tempo per i visitatori che arrivano alla pagina, c’è almeno un 95% di possibilità che [!UICONTROL Allocazione automatica] restituisce un’esperienza la cui vera risposta non è peggiore dell’1% (relativo) rispetto alla vera risposta dell’esperienza vincente.

## Quando utilizzare [!UICONTROL Allocazione automatica] rispetto a [!UICONTROL Test A/B] o [!UICONTROL Automated Personalization] attività {#section_3F73B0818A634E4AAAA60A37B502BFF9}

* Utilizza l&#39;**[!UICONTROL Allocazione automatica]** quando vuoi ottimizzare l&#39;attività fin dall&#39;inizio e identificare le esperienze vincenti il più rapidamente possibile. Rendendo più frequenti le esperienze ad alte prestazioni, le prestazioni complessive dell’attività aumentano.
* Utilizza uno standard **[Test A/B](/help/main/c-activities/t-test-ab/test-ab.md#task_05E33EB15C4D4459B5EAFF90A94A7977)** quando desideri caratterizzare le prestazioni di tutte le esperienze prima di ottimizzare il sito. Un test A/B ti aiuta a classificare tutte le esperienze, mentre [!UICONTROL Allocazione automatica] trova i migliori esecutori, ma non garantisce la differenziazione tra gli esecutori inferiori.
* Utilizzare [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9) quando desideri algoritmi di ottimizzazione della complessità più elevata, ad esempio modelli di apprendimento automatico che generano previsioni basate su attributi di profilo individuali. [!UICONTROL Allocazione automatica] esamina il comportamento aggregato delle esperienze (proprio come i test A/B standard) e non distingue tra visitatori.

## Vantaggi chiave di [!UICONTROL Allocazione automatica] {#section_0913BF06F73C4794862561388BBDDFF0}

* Mantiene la rigorosità di un test A/B
* Trova un vincitore statisticamente significativo più velocemente rispetto a un test A/B manuale.
* Fornisce un maggiore incremento medio della campagna rispetto a un test A/B manuale.

## Terminologia  {#section_670F8785BA894745B43B6D4BFF953188}

I seguenti termini sono utili quando si parla di [!UICONTROL Allocazione automatica]:

**Slot machine:** un approccio all’ottimizzazione ti tipo [slot machine](https://en.wikipedia.org/wiki/Multi-armed_bandit){target=_blank} compensa l’apprendimento esplorativo e il suo sfruttamento.

## Funzionamento dell’algoritmo {#section_ADB69A1C7352462D98849F2918D4FF7B}

La logica complessiva alla base di [!UICONTROL Allocazione automatica] incorpora sia le prestazioni misurate (come il tasso di conversione) che gli intervalli di affidabilità dei dati cumulativi. A differenza di un test A/B standard in cui il traffico viene suddiviso in modo uniforme tra le esperienze, [!UICONTROL Allocazione automatica] modifica l’allocazione del traffico tra le esperienze.

* L&#39;80% dei visitatori è assegnato utilizzando la logica intelligente descritta di seguito.
* Il 20% dei visitatori viene assegnato in modo casuale in tutte le esperienze per adattarsi al cambiamento del comportamento del visitatore.

L&#39;approccio slot machine consente di riservare alcune esperienze all’esplorazione, sfruttando le esperienze che danno buoni risultati. Un numero maggiore di nuovi visitatori vedrà le esperienze migliori, ma sarà comunque possibile reagire in caso di condizioni mutevoli. Questi modelli si aggiornano almeno una volta all&#39;ora per assicurarsi che il modello reagisca ai dati più recenti.

Man mano che più visitatori accedono all’attività, alcune esperienze iniziano a dimostrarsi di maggior successo e viene quindi incrementato il traffico inviato a tali esperienze. Il 20% del traffico continua a contribuire casualmente all’esplorazione di tutte le esperienze. Se una delle esperienze dalle prestazioni peggiori inizia a ottenere risultati migliori, le viene allocato più traffico. Oppure se il successo di un’attività con ottime prestazioni diminuisce, le viene assegnato meno traffico. Questo si verifica ad esempio se i visitatori cercano informazioni diverse sul tuo sito multimediale a causo di un particolare evento oppure se le offerte speciali del fine settimana nel tuo sito retail generano risultati diversi.

L’illustrazione seguente rappresenta il comportamento dell’algoritmo durante un test con quattro esperienze (fai clic per espandere l’illustrazione):

![allocazione automatica immagine](assets/auto-allocate.png){width="600" zoomable="yes"}

L&#39;illustrazione mostra come il traffico assegnato a ogni esperienza progredisca nell&#39;acro di parecchi turni della durata dell&#39;attività, finché non sia possibile determinare un chiaro vincitore.

| Turno | Descrizione |
|--- |--- |
| ![Turno di riscaldamento](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-0.png){width="200" zoomable="yes"} | **Turno di riscaldamento (0)**: durante il turno di riscaldamento, ogni esperienza ottiene pari ripartizione del traffico fino a quando ogni esperienza in attività ha un minimo di 1.000 visitatori e 50 conversioni.<ul><li>Esperienza A=25%</li><li>Esperienza B=25%</li><li>Esperienza C=25%</li><li>Esperienza D=25%</li></ul>Dopo che ogni esperienza ottiene 1.000 visitatori e 50 conversioni, [!DNL Target] avvia l&#39;allocazione automatica del traffico. Tutte le allocazioni avvengono in turni e vengono raccolte due esperienze per ogni turno.<br>Solo due esperienze progrediscono al turno successivo: D e C.<br>Progredire significa che alle due esperienze è assegnato l’80% del traffico in parti uguali. Le altre due esperienze continuano a partecipare, ma vengono gestite solo come parte dell’allocazione casuale del traffico del 20% quando nuovi visitatori accedono all’attività.<br>Tutte le allocazioni vengono aggiornate ogni ora (mostrato in alto per turni lungo l&#39;asse x). Dopo ogni turno, i dati cumulativi vengono confrontati. |
| ![Turno 1](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-1.png){width="200" zoomable="yes"} | **Turno 1**: durante questo turno, l’80% di traffico è assegnato alle esperienze C e D (40% ciascuna). Il 20% del traffico viene assegnato in modo casuale alle esperienze A, B, C e D (5% ciascuna). Durante questo turno, l&#39;esperienza A registra buoni risultati.<ul><li>L&#39;algoritmo sceglie l&#39;esperienza D per passare al turno successivo perché ha il più alto tasso di conversione (come indicato dalla scala verticale di ogni attività).</li><li>L&#39;algoritmo sceglie anche l&#39;esperienza A per proseguire perché, tra le esperienze rimanenti, ha il limite superiore più alto dell&#39;intervallo di affidabilità Bernstein al 95%.</li></ul>Le esperienze D e A proseguono. |
| ![Turno 2](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-2.png){width="200" zoomable="yes"} | **Turno 2**: durante questo turno, l’80% del traffico è assegnato alle esperienze A e D (40% ciascuna). Il 20% del traffico è allocato in modo casuale, quindi A, B, C e D ricevono rispettivamente il 5% del traffico. Durante questo turno, l’esperienza B registra buoni risultati.<ul><li>L&#39;algoritmo sceglie l&#39;esperienza D per passare al turno successivo perché ha il più alto tasso di conversione (come indicato dalla scala verticale di ogni attività).</li><li>L&#39;algoritmo sceglie anche l&#39;esperienza B per proseguire perché, tra le esperienze rimanenti, ha il limite superiore più alto dell&#39;intervallo di affidabilità Bernstein al 95%.</li></ul>Le esperienze D e B proseguono. |
| ![Turno 3](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-3.png){width="200" zoomable="yes"} | **Turno 3**: durante questo turno, l’80% di traffico è assegnato alle esperienze B e D (40% ciascuna). Il 20% del traffico è allocato in modo casuale, quindi A, B, C e D ricevono rispettivamente il 5% del traffico. Durante questo turno, l&#39;esperienza D continua a fornire buoni risultati, così come l&#39;esperienza C.<ul><li>L&#39;algoritmo sceglie l&#39;esperienza D per passare al turno successivo perché ha il più alto tasso di conversione (come indicato dalla scala verticale di ogni attività).</li><li>L&#39;algoritmo sceglie anche l&#39;esperienza C per proseguire perché, tra le esperienze rimanenti, ha il limite superiore più alto dell&#39;intervallo di affidabilità Bernstein al 95%.</li></ul>Le esperienze D e C proseguono. |
| ![Turno 4](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-4.png){width="200" zoomable="yes"} | **Turno 4**: durante questo turno, l’80% di traffico è assegnato alle esperienze C e D (40% ciascuna). Il 20% del traffico è allocato in modo casuale, quindi A, B, C e D ricevono rispettivamente il 5% del traffico. Durante questo turno, l&#39;esperienza C risulta avere buone prestazioni.<ul><li>L&#39;algoritmo sceglie l&#39;esperienza C per passare al turno successivo perché ha il più alto tasso di conversione (come indicato dalla scala verticale di ogni attività).</li><li>L&#39;algoritmo sceglie anche l&#39;esperienza D per proseguire perché, tra le esperienze rimanenti, ha il limite superiore più alto dell&#39;intervallo di affidabilità Bernstein al 95%.</li></ul>Le esperienze C e D proseguono. |
| ![Turno n](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-n.png){width="200" zoomable="yes"} | ***Turno n***: mentre l&#39;attività progredisce, inizia a emergere un&#39;esperienza con prestazioni elevate e il processo continua fino a individuare un&#39;esperienza vincente. Quando l’intervallo di affidabilità dell’esperienza con il tasso di conversione più alto non si sovrappone all’intervallo di affidabilità di qualsiasi altra esperienza, viene etichettato come vincitore. A [il badge viene visualizzato sulla pagina dell’attività vincente](/help/main/c-activities/automated-traffic-allocation/determine-winner.md) e nella [!UICONTROL Attività] elenco.<ul><li>L&#39;algoritmo sceglie l’esperienza C come chiaro vincitore.</li></ul>A questo punto l&#39;algoritmo indirizza l’80% del traffico all’esperienza C, mentre il 20% del traffico continua a essere indirizzato casualmente a tutte le esperienze (A, B, C e D). In totale, C ottiene l’85% del traffico. Nel caso improbabile che l’intervallo di affidabilità del vincitore inizi a sovrapporsi di nuovo cpn quello di un’altra esperienza, l’algoritmo ritorna al comportamento del turno 4 di cui sopra.<P>**Importante**: se scegliessi manualmente un vincitore in una fase precedente del processo, rischieresti di scegliere l’esperienza sbagliata. Per questo motivo, è consigliabile attendere che l’algoritmo determini l’esperienza vincente. |

>[!NOTE]
>
>Se un’attività ha solo due esperienze, entrambe ottengono lo stesso traffico fino al [!DNL Target] trova un’esperienza vincente con un’affidabilità del 75%. A quel punto, due terzi del traffico vengono assegnati al vincitore e un terzo al perdente. Successivamente, quando un’esperienza raggiunge il 95% di affidabilità, il 90% del traffico viene assegnato al vincitore e il 10% al perdente. [!DNL Target] invia sempre del traffico all’esperienza &quot;perdente&quot; per evitare falsi positivi alla fine (ovvero, mantieni un po’ di esplorazione).

Dopo un [!UICONTROL Allocazione automatica] l&#39;attività è attivata, le seguenti operazioni dal Tar[!DNL]Ottieni interfaccia utente non consentita:

* Impostazione della modalità di Allocazione traffico su Manuale
* Modifica del tipo di metrica obiettivo
* Modifica delle opzioni in &quot;[!UICONTROL Impostazioni avanzate]Pannello &quot;

## Scopri come funziona l’allocazione automatica

Per ulteriori informazioni, consulta [L’allocazione automatica può fornire risultati di test più rapidi e ricavi più elevati rispetto a un test manuale](/help/main/c-activities/automated-traffic-allocation/faster-results-higher-revenue.md).

## Avvertenze {#section_5C83F89F85C14FD181930AA420435E1D}

Considera le seguenti informazioni mentre lavori con [!UICONTROL Allocazione automatica]:

### Il [!UICONTROL Allocazione automatica] Questa funzione funziona con una sola impostazione metrica avanzata: [!UICONTROL Incrementa il conteggio e mantieni l&#39;utente attivo]

Le seguenti impostazioni di metrica avanzate non sono supportate: [!UICONTROL Incrementa il conteggio], [!UICONTROL Rilascia utente], [!UICONTROL Consenti reinserimento e conteggio incrementi], e [!UICONTROL Rilascia utente e impedisci nuovo accesso].

### I visitatori di ritorno frequenti possono gonfiare i tassi di conversione dell’esperienza.

Se un visitatore che vede l’esperienza A torna frequentemente e la sua conversione si verifica più volte, il tasso di conversione (CR) dell’esperienza A aumenta artificialmente. Confronta questo risultato con l’esperienza B, dove i visitatori si convertono ma non tornano spesso. Di conseguenza, il CR dell’esperienza A ha un aspetto migliore del CR dell’esperienza B, pertanto è più probabile che i nuovi visitatori vengano assegnati ad A che a B. Se scegli di contare una volta per partecipante, il CR di A e CR di B potrebbero essere identici.

Se i visitatori di ritorno sono distribuiti in modo casuale, è più probabile che il loro effetto sui tassi di conversione venga mitigato. Per attenuare questo effetto, è consigliabile modificare il metodo di conteggio della metrica obiettivo per conteggiare ogni partecipante una sola volta.

### Differenzia fra esperienze con prestazioni elevate, non fra quelle con prestazioni inferiori.

[!UICONTROL La funzione Allocazione automatica è in grado di distinguere tra le esperienze dalle prestazioni migliori (e trovare un vincitore). ] Ci potrebbero essere momenti in cui non vi è abbastanza differenziazione tra le esperienze con prestazioni inferiori.

Se desideri produrre una differenziazione statisticamente significativa tra tutte le esperienze, puoi utilizzare la modalità di allocazione manuale del traffico.

### I tassi di conversione correlati al tempo (o contestualmente variabili) possono distorcere le proporzioni di allocazione.

Alcuni fattori che possono essere ignorati durante un test A/B standard perché influiscono ugualmente su tutte le esperienze non possono essere ignorati in un [!UICONTROL Allocazione automatica] attività. L&#39;algoritmo è sensibile ai tassi di conversione osservati.

Di seguito sono riportati alcuni esempi di fattori che possono influenzare le prestazioni dell&#39;esperienza in modo disuguale:

* Esperienze con diversa rilevanza contestuale (tempo, posizione, genere e così via).

  Ad esempio:

   * “Grazie a Dio è venerdì” genera un maggior numero di conversioni il venerdì. 
   * &quot;Jump-start your Monday&quot; ha una conversione più alta il lunedì.
   * &quot;Prepararsi per un inverno della costa orientale&quot; fornisce una maggiore conversione nelle zone della costa orientale o in quelle afflitte dall&#39;inverno.

  L’utilizzo di esperienze con rilevanza contestuale variabile può distorcere i risultati in un [!UICONTROL Allocazione automatica] più che in un test A/B, perché analizza i risultati su un periodo più lungo.

* Esperienze con ritardi diversi nella conversione possono essere dovute all’urgenza del messaggio.

  Ad esempio, “i saldi al 30% finiscono oggi” incita il visitatore ad eseguire oggi stesso la conversione, mentre “50% di sconto sul primo acquisto” non crea lo stesso senso di urgenza.

## Domande frequenti  {#section_0E72C1D72DE74F589F965D4B1763E5C3}

Consulta le seguenti domande frequenti e risposte mentre lavori con [!UICONTROL Allocazione automatica] attività:

### Does [!UICONTROL Analytics for Target] Supporto (A4T) [!UICONTROL Allocazione automatica] attività?

Sì. Per ulteriori informazioni, consulta [Supporto di A4T per attività di allocazione automatica e targeting automatico](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md).

###  I visitatori di ritorno vengono riallocati automaticamente alle esperienze con prestazioni elevate?

No. Solo i nuovi visitatori vengono allocati automaticamente. I visitatori di ritorno continuano a vedere la loro esperienza originale per proteggere la validità del test A/B.

###  In che modo l’algoritmo tratta i falsi positivi?

L’algoritmo garantisce un&#39;affidabilità del 95% o un tasso di falsa positività del 5% se si attende che appaia il badge del vincitore.

### Quando [!UICONTROL Allocazione automatica] iniziare ad allocare il traffico?

L’algoritmo inizia a funzionare dopo che tutte le esperienze nell’attività hanno un minimo di 1.000 visitatori e 50 conversioni.

### Quanto aggressivamente viene applicato l’algoritmo?

L’80% del traffico viene gestito tramite [!UICONTROL Allocazione automatica] e il 20% del traffico viene servito in modo casuale. Quando viene identificato un vincitore, l&#39;80% del traffico viene indirizzato a tale vincitore, mentre tutte le esperienze continuano a ricevere una parte del traffico come parte del 20%, inclusa l&#39;esperienza vincente.

### Le esperienze perdenti vengono mostrate?

Sì. Con un approccio di tipo slot machine, almeno il 20% del traffico è riservato all’esplorazione di modifiche nei pattern o nei tassi di conversione in tutte le esperienze.

### Cosa succede alle attività con tempi di conversione lunghi?

Finché tutte le esperienze ottimizzate avranno ritardi simili, il comportamento sarà lo stesso di un’attività con un ciclo di conversione più veloce. Tuttavia, il raggiungimento della soglia di conversione di 50 richiede più tempo prima dell’inizio del processo di allocazione del traffico.

### Com’è [!UICONTROL Allocazione automatica] diverso da [!UICONTROL Automated Personalization]?

[!UICONTROL La funzione Personalizzazione automatizzata utilizza gli attributi del profilo di ogni visitatore per determinare l&#39;esperienza migliore. ] In tal modo, non solo ottimizza, ma personalizza anche l’attività per quell’utente.

[!UICONTROL Allocazione automatica]D’altra parte, è un test A/B che produce un vincitore aggregato (l’esperienza più popolare, ma non necessariamente quella più efficace per ogni visitatore).

###  I visitatori di ritorno gonfiano il tasso di conversione sulla metrica di successo? 

Attualmente, la logica favorisce i visitatori che si convertono rapidamente o che effettuano visite più frequenti, perché tali visitatori aumentano temporaneamente il tasso di conversione complessivo dell’esperienza a cui appartengono. L’algoritmo si regola frequentemente, quindi l’aumento del tasso di conversione viene amplificato in ogni istantanea. Se il sito riceve numerosi visitatori di ritorno, le loro conversioni possono potenzialmente aumentare il tasso di conversione complessivo per l’esperienza a cui appartengono. C&#39;è una buona probabilità che i visitatori di ritorno siano distribuiti in modo casuale, nel qual caso l’effetto aggregato (aumento dell’incremento) è mitigato. Per attenuare questo effetto, è consigliabile modificare il metodo di conteggio della metrica di sucesso per conteggiare ogni partecipante una sola volta.

### È possibile utilizzare il Calcolatore dimensione campione quando si utilizza [!UICONTROL Allocazione automatica] per stimare quanto tempo ci vuole per identificare il vincitore?

È possibile utilizzare il [!DNL Adobe Target] [Calcolatore dimensioni campione](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6) per ottenere una stima della durata dell’esecuzione del test. (Come con i tradizionali test A/B, applica la correzione Bonferroni se stai sottoponendo a test più di due offerte o più di una metrica/ipotesi di conversione.) Questo calcolatore è progettato per il tradizionale test A/B a orizzonte fisso e fornisce solo una stima. Utilizzo della calcolatrice per un [!UICONTROL Allocazione automatica] l’attività è facoltativa perché [!UICONTROL Allocazione automatica] dichiara un vincitore per te. Non è necessario scegliere un punto fisso nel tempo per esaminare i risultati del test. I valori forniti sono sempre statisticamente validi.

Interno [!DNL Adobe] gli esperimenti hanno rilevato quanto segue:

* Quando si sottopongono a test esattamente due esperienze, [!UICONTROL Allocazione automatica] trova un vincitore più rapidamente del test a orizzonte fisso (ovvero, l’intervallo di tempo suggerito dal calcolatore delle dimensioni del campione) quando la differenza di prestazioni tra le esperienze è elevata. Tuttavia, [!UICONTROL Allocazione automatica] potrebbe richiedere più tempo per identificare un vincitore quando la differenza di prestazioni tra le esperienze è ridotta. In questi casi, i test a orizzonte fisso si sarebbero in genere conclusi senza un risultato statisticamente significativo.
* Quando si sottopongono a test più di due esperienze, [!UICONTROL Allocazione automatica] trova un vincitore più rapidamente del test a orizzonte fisso (ovvero, l’intervallo di tempo suggerito dal calcolatore delle dimensioni del campione) quando una singola esperienza supera fortemente tutte le altre esperienze. Quando due o più esperienze sono entrambe &quot;vincenti&quot; rispetto ad altre ma strettamente correlate, [!UICONTROL Allocazione automatica] potrebbe richiedere più tempo per determinare quale sia superiore. In questi casi, i test a orizzonte fisso in genere si sarebbero conclusi concludendo che le esperienze &quot;vincenti&quot; erano migliori rispetto a quelle con prestazioni inferiori, ma non avevano identificato quale era superiore.

### È necessario rimuovere un’esperienza insoddisfacente da un [!UICONTROL Allocazione automatica] attività per accelerare il processo di determinazione di un vincitore?

Non c’è motivo di rimuovere un’esperienza insoddisfacente. [!UICONTROL Allocazione automatica] trasmette automaticamente le esperienze con prestazioni migliori più spesso e fornisce quelle con prestazioni inferiori con minore frequenza. Lasciare un’esperienza insoddisfacente nell’attività non influisce in modo significativo sulla velocità per determinare un vincitore.

Il 20% dei visitatori viene assegnato in modo casuale attraverso tutte le esperienze. La quantità di traffico utilizzata per un’esperienza insoddisfacente è minima (20% diviso per il numero di esperienze).

### Posso cambiare la metrica di obiettivo a metà strada attraverso un [!UICONTROL Allocazione automatica] attività? {#change-metric}

[!DNL Adobe] sconsiglia di modificare la metrica obiettivo a metà strada attraverso un’attività. Anche se è possibile modificare la metrica dell’obiettivo durante un’attività utilizzando l’interfaccia utente [!DNL Target], è sempre necessario avviare una nuova attività. [!DNL Adobe] non garantisce ciò che accade se modifichi la metrica di obiettivo in un’attività dopo l’esecuzione.

Questo consiglio si applica alle attività [!UICONTROL Allocazione automatica], [!UICONTROL Targeting automatico] e [!UICONTROL Automated Personalization] che utilizzano [!DNL Target] o [!DNL Analytics] (A4T) come origine per la generazione di rapporti.

### Posso cambiare l’origine per la generazione di rapporti nel corso di un’attività [!UICONTROL Allocazione automatica]? {#change-reporting}

[!DNL Adobe] sconsiglia di modificare l’origine per la generazione di rapporti nel corso di un’attività. Anche se è possibile modificare l’origine per la generazione di rapporti (da [!DNL Target] a A4T o in modo opposto) durante un’attività utilizzando [!DNL Target] Dovresti sempre avviare una nuova attività. [!DNL Adobe] non garantisce ciò che accade se si modifica l&#39;origine per la generazione di rapporti in un&#39;attività dopo l&#39;esecuzione.

Questo consiglio si applica alle attività [!UICONTROL Allocazione automatica], [!UICONTROL Targeting automatico] e [!UICONTROL Automated Personalization] che utilizzano [!DNL Target] o [!DNL Analytics] (A4T) come origine per la generazione di rapporti.

### Posso utilizzare il [!UICONTROL Ripristina dati rapporto] durante l&#39;esecuzione di un [!UICONTROL Allocazione automatica] attività?

Utilizzo di [!UICONTROL Ripristina dati rapporto] opzione per [!UICONTROL Allocazione automatica] attività non è consigliato. Anche se rimuove i dati di reporting visibili, questa opzione non rimuove tutti i record di formazione dal [!UICONTROL Allocazione automatica] modello. Invece di utilizzare [!UICONTROL Ripristina dati rapporto] opzione per [!UICONTROL Allocazione automatica] , crea una nuova attività e disattiva l&#39;attività originale. (Questa guida si applica anche a [!UICONTROL Targeting automatico] e [!UICONTROL Automated Personalization] attività.)

### In che modo [!UICONTROL Allocazione automatica] creare modelli per quanto riguarda gli ambienti?

[!UICONTROL Allocazione automatica] crea modelli in base al comportamento di traffico e conversione registrato solo nell’ambiente predefinito. Per impostazione predefinita, [!UICONTROL Produzione] è l’ambiente predefinito, ma è possibile modificarlo in [!DNL Target] ([Amministrazione > Ambienti](/help/main/administrating-target/environments.md)).

Se un hit si verifica in un altro ambiente (non predefinito), il traffico viene distribuito in base al comportamento di conversione osservato nell’ambiente predefinito. Il risultato di tale hit (conversione o non conversione) è registrato a scopo di reporting ma non è considerato nella [!UICONTROL Allocazione automatica] modello.

Quando selezioni un altro ambiente, il rapporto mostra il traffico e le conversioni per tale ambiente. L’ambiente selezionato predefinito per un rapporto è l’ambiente predefinito a livello di account selezionato. L’ambiente predefinito non può essere impostato in base alle singole attività.

### Can an [!UICONTROL Allocazione automatica] attività di regolare l’intervallo di lookback nel corso di un test per considerare l’eventualità di modificare le tendenze nel tempo?

Ad esempio, l’attività può considerare il mese di dicembre per decidere come allocare il traffico, anziché esaminare i dati dei visitatori di settembre (quando è iniziato il test)?

No, [!UICONTROL Allocazione automatica] considera le prestazioni dell’intera attività.

### La funzione [!UICONTROL Allocazione automatica] mostra un’esperienza vincente a un visitatore che ritorna, se l’esperienza vincente è diversa da quella che aveva visto quando si è qualificato per l’attività?

[!UICONTROL Allocazione automatica] utilizza le decisioni permanenti per gli stessi motivi che [!UICONTROL Test A/B] Le attività sono permanenti. L’allocazione del traffico funziona solo per i nuovi visitatori.

## Video di formazione {#section_893E5B36DC4A415C9B1D287F51FCCB83}

I video seguenti contengono ulteriori informazioni sui concetti descritti in questo articolo.

### Flusso di lavoro di un&#39;attività - Targeting (2:14) ![Icona Tutorial](/help/main/assets/tutorial.png)

Questo video include informazioni su come impostare l&#39;allocazione del traffico.

* Assegnare un pubblico all’attività
* Limitare il traffico verso l’alto o il basso
* Selezionare il metodo di allocazione del traffico
* Allocare il traffico tra diverse esperienze

>[!VIDEO](https://video.tv.adobe.com/v/17385)

### Creazione di test A/B (8:36) ![Icona esercitazione](/help/main/assets/tutorial.png)

In questo video viene illustrato come creare un test A/A utilizzando il flusso di lavoro guidato in tre passaggi di Target. [!UICONTROL Allocazione automatica] L’argomento di è trattato a partire dal minuto 4:45.

* Creare un’attività A/B in [!DNL Adobe Target]
* Allocare il traffico con suddivisione manuale o automatica del traffico

>[!VIDEO](https://video.tv.adobe.com/v/17391)
