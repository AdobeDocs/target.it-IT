---
keywords: allocazione automatica del traffico;targeting;incrementa il conteggio e mantieni l'utente nell'attività;allocazione del traffico;allocazione automatica;allocazione automatica
description: Scopri come utilizzare un’attività di allocazione automatica in Adobe [!DNL Target] che identifica un vincitore tra due o più esperienze e ridistribuisce automaticamente più traffico per il vincitore.
title: Cos’è un’attività di allocazione automatica?
feature: Auto-Allocate
exl-id: 2d1ddd71-2ca6-4f00-9d0c-eb25ede8fdb8
source-git-commit: 393ab5b9e2b8fbdf0dcee0640775c73bf6899afe
workflow-type: tm+mt
source-wordcount: '3559'
ht-degree: 49%

---

# Panoramica dell’[!UICONTROL allocazione automatica]

Un [!UICONTROL Allocazione automatica] attività in [!DNL Adobe Target] identifica un vincitore tra due o più esperienze e, di conseguenza, ridistribuisce automaticamente più traffico per aumentare le conversioni, mentre il test continua a essere eseguito e ad apprendere.

Durante la creazione di un’attività A/B tramite il flusso di lavoro guidato in tre passaggi, puoi scegliere il [!UICONTROL Allocazione automatica all’esperienza migliore] opzione .

## La sfida {#section_85D5A03637204BACA75E19646162ACFF}

I test A/B standard hanno un costo intrinseco. Devi investire del traffico per misurare le prestazioni di ogni esperienza e capire quale sia l’esperienza vincente attraverso l’analisi. La distribuzione del traffico rimane fissa anche dopo aver compreso che alcune esperienze hanno prestazioni migliori di altre. Inoltre, è complicato calcolare la dimensione necessaria del campione, e l’attività deve essere eseguita completamente prima di poter intervenire in base al vincitore. E c&#39;è ancora una possibilità che il vincitore identificato non sia un vero vincitore.

## La soluzione: [!UICONTROL Allocazione automatica] {#section_98388996F0584E15BF3A99C57EEB7629}

[!UICONTROL L’allocazione automatica riduce il costo e il sovraccarico associati al determinare un’esperienza vincente. ] [!UICONTROL L’allocazione automatica monitora le prestazioni della metrica obiettivo di tutte le esperienze e invia in modo proporzionale un numero maggiore di nuovi partecipanti alle esperienze che hanno prestazioni migliori. ] Per l’esplorazione delle altre esperienze viene riservata una quantità adeguata di traffico. È possibile vedere i vantaggi del test nei risultati, anche se l’attività è ancora in esecuzione: l’ottimizzazione si verifica in parallelo all’apprendimento.

[!UICONTROL L’allocazione automatica sposta gradualmente i visitatori verso esperienze vincenti, invece di richiedere di attendere fino a quando un’attività finisce per determinare un vincitore. ] Puoi beneficiare di incrementi più rapidi perché potenziali esperienze vincenti vengono mostrate a partecipanti che sarebbero altrimenti stati destinati a esperienze di minor successo.

Un normale test A/B in [!DNL Target] mostra solo confronti in coppia di sfidanti con controllo. Ad esempio, se un’attività ha esperienze: A, B, C e D dove A è il controllo, una normale [!DNL Target] Il test A/B confronterebbe A con B, A con C e A con D.

In tali prove, la maggior parte dei prodotti, compresi [!DNL Target], utilizza un test t di Student per produrre un&#39;affidabilità basata sul valore p. Questo valore di affidabilità viene quindi utilizzato per determinare se lo sfidante è sufficientemente diverso dal controllo. Tuttavia, [!DNL Target] non esegue automaticamente i confronti impliciti (B con C, B con D e C con D) necessari per trovare l’esperienza &quot;migliore&quot;. Di conseguenza, l’addetto al marketing deve analizzare manualmente i risultati per determinare l’esperienza “migliore”.

[!UICONTROL L’allocazione automatica esegue tutti i confronti impliciti tra le esperienze e produce un vincitore “reale”. ] Non vi è alcuna nozione di esperienza di “controllo” nel test.

[!UICONTROL Allocazione automatica] assegna in modo intelligente nuovi visitatori alle esperienze fino a quando l’intervallo di affidabilità della migliore esperienza non si sovrappone all’intervallo di affidabilità di qualsiasi altra esperienza. Normalmente questo processo potrebbe produrre falsi positivi, ma [!UICONTROL Allocazione automatica] utilizza intervalli di affidabilità basati su [Disuguaglianza di Bernstein](https://en.wikipedia.org/wiki/Bernstein_inequalities_%28probability_theory%29) che compensa le valutazioni ripetute. A questo punto, c&#39;è un vero vincitore. Quando [!UICONTROL Allocazione automatica] si ferma, purché non vi sia una notevole dipendenza dal tempo per i visitatori che arrivano alla pagina, vi è almeno un 95% di probabilità che [!UICONTROL Allocazione automatica] restituisce un’esperienza la cui vera risposta non è inferiore all’1% (relativo) rispetto alla vera risposta dell’esperienza vincente.

## Quando utilizzare [!UICONTROL Allocazione automatica] A/B o [!UICONTROL Automated Personalization] {#section_3F73B0818A634E4AAAA60A37B502BFF9}

* Utilizza l&#39;**[!UICONTROL Allocazione automatica]** quando vuoi ottimizzare l&#39;attività fin dall&#39;inizio e identificare le esperienze vincenti il più rapidamente possibile. Fornendo con maggiore frequenza le esperienze che hanno prestazioni migliori, aumentano le prestazioni complessive di attività.
* Utilizza un **[Test A/B](/help/main/c-activities/t-test-ab/test-ab.md#task_05E33EB15C4D4459B5EAFF90A94A7977)** standard quando vuoi caratterizzare le prestazioni di tutte le esperienze prima di ottimizzare il sito. Un test A/B ti aiuta a classificare tutte le tue esperienze, mentre [!UICONTROL Allocazione automatica] trova i migliori performer ma non garantisce la differenziazione tra i più bassi performers.
* Utilizzo [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9) quando desideri algoritmi di ottimizzazione della complessità più elevata, ad esempio modelli di apprendimento automatico che generano previsioni basate su attributi di profilo individuali. [!UICONTROL Allocazione automatica] esamina il comportamento aggregato delle esperienze (come i test A/B standard) e non distingue tra i visitatori.

## Vantaggi principali {#section_0913BF06F73C4794862561388BBDDFF0}

* Mantiene la rigorosità di un test A/B
* Trova un vincitore statisticamente significativo più velocemente rispetto a un test A/B manuale.
* Fornisce un maggiore incremento medio della campagna rispetto a un test A/B manuale.

## Terminologia  {#section_670F8785BA894745B43B6D4BFF953188}

I seguenti termini sono utili quando si parla di [!UICONTROL Allocazione automatica]:

**Slot machine:** un approccio all’ottimizzazione ti tipo [slot machine](https://en.wikipedia.org/wiki/Multi-armed_bandit) compensa l’apprendimento esplorativo e il suo sfruttamento.

## Funzionamento dell’algoritmo {#section_ADB69A1C7352462D98849F2918D4FF7B}

La logica generale dietro [!UICONTROL Allocazione automatica] incorpora sia le prestazioni misurate (come il tasso di conversione) sia gli intervalli di affidabilità dei dati cumulativi. A differenza di un test A/B standard in cui il traffico è suddiviso in modo uniforme tra le esperienze, [!UICONTROL Allocazione automatica] cambia l’allocazione del traffico tra le esperienze.

* L&#39;80% dei visitatori è assegnato utilizzando la logica intelligente descritta di seguito.
* Il 20% dei visitatori è assegnato in modo casuale in tutte le esperienze, al fine di adattarsi al cambiamento del comportamento dei visitatori.

L&#39;approccio slot machine consente di riservare alcune esperienze all’esplorazione, sfruttando le esperienze che danno buoni risultati. Un numero maggiore di nuovi visitatori vedrà le esperienze migliori, ma sarà comunque possibile reagire in caso di condizioni mutevoli. Questi modelli si aggiornano almeno una volta all&#39;ora per assicurarsi che il modello reagisca ai dati più recenti.

Man mano che più visitatori accedono all’attività, alcune esperienze iniziano a dimostrarsi di maggior successo e viene quindi incrementato il traffico inviato a tali esperienze. Il 20% del traffico continua a contribuire casualmente all’esplorazione di tutte le esperienze. Se una delle esperienze dalle prestazioni peggiori inizia a ottenere risultati migliori, le viene allocato più traffico. Oppure se il successo di un’attività con ottime prestazioni diminuisce, le viene assegnato meno traffico. Questo si verifica ad esempio se i visitatori cercano informazioni diverse sul tuo sito multimediale a causo di un particolare evento oppure se le offerte speciali del fine settimana nel tuo sito retail generano risultati diversi.

Nell&#39;illustrazione seguente viene mostrato come potrebbe comportarsi l&#39;algoritmo durante un test con quattro esperienze:

![](assets/auto-allocate.png)

L&#39;illustrazione mostra come il traffico assegnato a ogni esperienza progredisca nell&#39;acro di parecchi turni della durata dell&#39;attività, finché non sia possibile determinare un chiaro vincitore.

| Turno | Descrizione |
|--- |--- |
| ![Turno di riscaldamento](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-0.png) | **Turno di riscaldamento (0)**: durante il turno di riscaldamento, ogni esperienza ottiene pari ripartizione del traffico fino a quando ogni esperienza in attività ha un minimo di 1.000 visitatori e 50 conversioni.<ul><li>Esperienza A=25%</li><li>Esperienza B=25%</li><li>Esperienza C=25%</li><li>Esperienza D=25%</li></ul>Dopo che ogni esperienza ottiene 1.000 visitatori e 50 conversioni, Target avvia l&#39;allocazione automatica del traffico. Tutte le allocazioni avvengono in turni e vengono raccolte due esperienze per ogni turno.<br>Solo due esperienze progrediscono al turno successivo: D e C.<br>Progredire significa che alle due esperienze è assegnato l’80% del traffico allo stesso modo. Le altre due esperienze continuano a partecipare, ma vengono servite solo come parte dell’allocazione casuale del 20% del traffico quando nuovi visitatori accedono all’attività.<br>Tutte le allocazioni vengono aggiornate ogni ora (mostrato in alto per turni lungo l&#39;asse x). Dopo ogni turno, i dati cumulativi vengono confrontati. |
| ![Turno 1](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-1.png) | **Turno 1**: durante questo turno, l’80% di traffico è assegnato alle esperienze C e D (40% ciascuna). Il 20% del traffico viene assegnato in modo casuale alle esperienze A, B, C e D (5% ciascuna). Durante questo turno, l&#39;esperienza A registra buoni risultati.<ul><li>L&#39;algoritmo sceglie l&#39;esperienza D per passare al turno successivo perché ha il più alto tasso di conversione (come indicato da sulla scala verticale di ogni attività).</li><li>L&#39;algoritmo sceglie anche l&#39;esperienza A per proseguire perché, tra le esperienze rimanenti, ha il limite superiore più alto dell&#39;intervallo di affidabilità Bernstein al 95%.</li></ul>Le esperienze D e A proseguono. |
| ![Turno 2](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-2.png) | **Turno 2**: durante questo turno, l’80% del traffico è assegnato alle esperienze A e D (40% ciascuna). Il 20% del traffico è allocato in modo casuale, quindi A, B, C e D ricevono rispettivamente il 5% del traffico. Durante questo turno, l’esperienza B registra buoni risultati.<ul><li>L&#39;algoritmo sceglie l&#39;esperienza D per passare al turno successivo perché ha il più alto tasso di conversione (come indicato da sulla scala verticale di ogni attività).</li><li>L&#39;algoritmo sceglie anche l&#39;esperienza B per proseguire perché, tra le esperienze rimanenti, ha il limite superiore più alto dell&#39;intervallo di affidabilità Bernstein al 95%.</li></ul>Le esperienze D e B proseguono. |
| ![Turno 3](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-3.png) | **Turno 3**: durante questo turno, l’80% di traffico è assegnato alle esperienze B e D (40% ciascuna). Il 20% del traffico è allocato in modo casuale, quindi A, B, C e D ricevono rispettivamente il 5% del traffico. Durante questo turno, l&#39;esperienza D continua a fornire buoni risultati, così come l&#39;esperienza C.<ul><li>L&#39;algoritmo sceglie l&#39;esperienza D per passare al turno successivo perché ha il più alto tasso di conversione (come indicato da sulla scala verticale di ogni attività).</li><li>L&#39;algoritmo sceglie anche l&#39;esperienza C per proseguire perché, tra le esperienze rimanenti, ha il limite superiore più alto dell&#39;intervallo di affidabilità Bernstein al 95%.</li></ul>Le esperienze D e C proseguono. |
| ![Turno 4](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-4.png) | **Turno 4**: durante questo turno, l’80% di traffico è assegnato alle esperienze C e D (40% ciascuna). Il 20% del traffico è allocato in modo casuale, quindi A, B, C e D ricevono rispettivamente il 5% del traffico. Durante questo turno, l&#39;esperienza C risulta avere buone prestazioni.<ul><li>L&#39;algoritmo sceglie l&#39;esperienza C per passare al turno successivo perché ha il più alto tasso di conversione (come indicato da sulla scala verticale di ogni attività).</li><li>L&#39;algoritmo sceglie anche l&#39;esperienza D per proseguire perché, tra le esperienze rimanenti, ha il limite superiore più alto dell&#39;intervallo di affidabilità Bernstein al 95%.</li></ul>Le esperienze C e D proseguono. |
| ![Turno n](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-n.png) | **Turno n**: mentre l&#39;attività progredisce, inizia a emergere un&#39;esperienza con prestazioni elevate e il processo continua fino a individuare un&#39;esperienza vincente. Quando l’intervallo di affidabilità dell’esperienza con il tasso di conversione più alto non si sovrappone all’intervallo di affidabilità di qualsiasi altra esperienza, questa viene etichettata come vincitrice. A [sulla pagina dell’attività vincente viene visualizzato un badge](/help/main/c-activities/automated-traffic-allocation/determine-winner.md) e [!UICONTROL Attività] elenco.<ul><li>L&#39;algoritmo sceglie l’esperienza C come chiaro vincitore</li></ul>A questo punto l&#39;algoritmo indirizza l’80% del traffico all’esperienza C, mentre il 20% del traffico continua a essere indirizzato casualmente a tutte le esperienze (A, B, C e D). In totale, C ottiene l’85% del traffico. Nel caso improbabile che l’intervallo di affidabilità del vincitore inizi a sovrapporsi di nuovo cpn quello di un’altra esperienza, l’algoritmo ritorna al comportamento del turno 4 di cui sopra.<br>**Importante**: se scegliessi manualmente un vincitore in una fase precedente del processo, rischieresti di scegliere l’esperienza sbagliata. Per questo motivo, è consigliabile attendere che l’algoritmo determini l’esperienza vincente. |

>[!NOTE]
>
>Se un’attività ha solo due esperienze, entrambe ottengono la stessa quantità di traffico fino a [!DNL Target] trova un’esperienza vincente con un’affidabilità del 75%. A quel punto, due terzi del traffico è assegnato al vincitore, e un terzo al perdente. In seguito, quando un’esperienza raggiunge il 95% di affidabilità, il 90% di traffico è assegnato al vincitore e il 10% al perdente. [!DNL Target] mantiene sempre del traffico inviato all’esperienza &quot;perdente&quot; per evitare falsi positivi alla fine (ovvero mantenere alcune esplorazioni).

Dopo un [!UICONTROL Allocazione automatica] L’attività è attivata e non sono consentite le seguenti operazioni dall’interfaccia utente:

* Impostazione della modalità di Allocazione traffico su Manuale
* Modifica del tipo di metrica obiettivo
* Modifica delle opzioni nel pannello “Impostazioni avanzate”

## Come funziona l’allocazione automatica

Per ulteriori informazioni, consulta [L’allocazione automatica può fornire risultati di test più rapidi e ricavi più elevati rispetto a un test manuale](/help/main/c-activities/automated-traffic-allocation/faster-results-higher-revenue.md)

## Avvertenze {#section_5C83F89F85C14FD181930AA420435E1D}

**La [!UICONTROL Allocazione automatica] funziona con una sola impostazione metrica avanzata: [!UICONTROL Incrementa il conteggio e mantieni l’utente attivo]**

Le seguenti impostazioni avanzate di metrica non sono supportate: [!UICONTROL Conteggio incremento], [!UICONTROL Rilascia utente], [!UICONTROL Consenti nuovo accesso e conteggio incremento]e [!UICONTROL Rilascia utente e impedisci nuovo accesso].

**I visitatori di ritorno frequenti possono gonfiare i tassi di conversione dell’esperienza.**

Se un visitatore che vede l’esperienza A torna frequentemente e la sua conversione si verifica più volte, il tasso di conversione (CR) dell’esperienza A aumenta artificialmente. Confronta questo risultato con l’esperienza B, in cui i visitatori si convertono ma non ritornano spesso. Di conseguenza, il CR dell&#39;esperienza A sembra migliore del CR dell&#39;esperienza B, in modo che i nuovi visitatori abbiano più probabilità di essere allocati a A che a B. Se scegli di contare una volta per partecipante, il CR di A e CR di B potrebbero essere identici.

Se i visitatori di ritorno sono distribuiti in modo casuale, è più probabile che il loro effetto sui tassi di conversione venga mitigato. Per attenuare questo effetto, è consigliabile modificare il metodo di conteggio della metrica obiettivo per conteggiare ogni partecipante una sola volta.

**Differenzia fra esperienze con prestazioni elevate, non fra quelle con prestazioni inferiori.**

[!UICONTROL La funzione Allocazione automatica è in grado di distinguere tra le esperienze dalle prestazioni migliori (e trovare un vincitore). ] Ci potrebbero essere momenti in cui non vi è abbastanza differenziazione tra le esperienze con prestazioni inferiori.

Se desideri produrre una differenziazione statisticamente significativa tra tutte le esperienze, puoi prendere in considerazione l’utilizzo della modalità di allocazione manuale del traffico.

**I tassi di conversione correlati al tempo (o contestualmente variabili) possono distorcere le proporzioni di allocazione.**

Alcuni fattori che possono essere ignorati durante un test A/B standard perché influiscono ugualmente su tutte le esperienze non possono essere ignorati in un [!UICONTROL Allocazione automatica] test. L&#39;algoritmo è sensibile ai tassi di conversione osservati. Di seguito sono riportati alcuni esempi di fattori che possono influenzare le prestazioni dell&#39;esperienza in modo disuguale:

* Esperienze con rilevanza contestuale diversa (tempo, posizione, genere e così via).

   Ad esempio:

   * “Grazie a Dio è venerdì” genera un maggior numero di conversioni il venerdì.
   * “Accendi il tuo lunedì” genera un maggior numero di conversioni il lunedì.
   * &quot;Prepararsi per un inverno sulla costa orientale&quot; offre una conversione più elevata in posti afflitti dalla costa orientale o dall&#39;inverno

L’utilizzo di esperienze con rilevanza contestuale diversa può distorcere i risultati in una [!UICONTROL Allocazione automatica] test più che in un test A/B perché il test A/B analizza i risultati su un periodo più lungo.

* Esperienze con ritardi diversi nella conversione possono essere dovute all’urgenza del messaggio.

   Ad esempio, “i saldi al 30% finiscono oggi” incita il visitatore ad eseguire oggi stesso la conversione, mentre “50% di sconto sul primo acquisto” non crea lo stesso senso di urgenza.

## Domande frequenti  {#section_0E72C1D72DE74F589F965D4B1763E5C3}

Consulta le seguenti domande frequenti e risposte mentre lavori con [!UICONTROL Allocazione automatica] attività:

### Does [!UICONTROL Analytics for Target] Supporto di (A4T) [!UICONTROL Allocazione automatica] attività?

Sì. Per ulteriori informazioni, consulta [Supporto di A4T per attività di allocazione automatica e targeting automatico](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md).

###  I visitatori di ritorno vengono riallocati automaticamente alle esperienze con prestazioni elevate?

No. Solo i nuovi visitatori vengono allocati automaticamente. I visitatori di ritorno continuano a vedere la loro esperienza originale per proteggere la validità del test A/B.

###  In che modo l’algoritmo tratta i falsi positivi?

L’algoritmo garantisce un&#39;affidabilità del 95% o un tasso di falsa positività del 5% se si attende che appaia il badge del vincitore.

### Quando fa [!UICONTROL Allocazione automatica] inizia ad allocare il traffico?

L’algoritmo inizia a funzionare dopo che tutte le esperienze nell’attività hanno un minimo di 1.000 visitatori e 50 conversioni.

### Quanto aggressivamente viene applicato l’algoritmo?

L’80% del traffico viene servito utilizzando [!UICONTROL Allocazione automatica] e il 20% del traffico viene servito in modo casuale. Quando viene identificato un vincitore, a tutto l&#39;80% del traffico viene veicolata l’esperienza vincente, mentre tutte le esperienze continuano a ricevere un certo traffico come parte del 20%, compresa quella vincente.

### Le esperienze perdenti vengono mostrate?

Sì. Con un approccio di tipo slot machine, almeno il 20% del traffico è riservato all’esplorazione di modifiche nei pattern o nei tassi di conversione in tutte le esperienze.

### Cosa succede alle attività con tempi di conversione lunghi?

Finché tutte le esperienze ottimizzate avranno ritardi simili, il comportamento sarà lo stesso di un’attività con un ciclo di conversione più veloce. Tuttavia, è necessario più tempo per raggiungere la soglia di conversione 50 prima che inizi il processo di allocazione del traffico.

### Come [!UICONTROL Allocazione automatica] diverso da [!UICONTROL Automated Personalization]?

[!UICONTROL La funzione Personalizzazione automatizzata utilizza gli attributi del profilo di ogni visitatore per determinare l&#39;esperienza migliore. ] In tal modo, non solo ottimizza, ma personalizza anche l’attività per quell’utente.

[!UICONTROL Allocazione automatica], invece, è un test A/B che produce un vincitore aggregato (l’esperienza più popolare, ma non necessariamente quella più efficace per ogni visitatore).

###  I visitatori di ritorno gonfiano il tasso di conversione sulla metrica di successo? 

Attualmente, la logica favorisce i visitatori che si convertono rapidamente o che visitano più spesso perché tali visitatori aumentano temporaneamente il tasso di conversione complessivo dell’esperienza a cui appartengono. L’algoritmo si regola frequentemente, quindi l’aumento del tasso di conversione viene amplificato in ogni istantanea. Se il sito riceve numerosi visitatori di ritorno, le loro conversioni possono potenzialmente aumentare il tasso di conversione complessivo per l’esperienza a cui appartengono. C&#39;è una buona probabilità che i visitatori di ritorno siano distribuiti in modo casuale, nel qual caso l’effetto aggregato (aumento dell’incremento) è mitigato. Per attenuare questo effetto, è consigliabile modificare il metodo di conteggio della metrica di sucesso per conteggiare ogni partecipante una sola volta.

### Posso usare il Calcolatore dimensione campione quando utilizzo [!UICONTROL Allocazione automatica] per stimare quanto tempo ci vuole per identificare il vincitore?

È possibile utilizzare [Calcolatore dimensione campione](https://experienceleague.adobe.com/tools/calculator/testcalculator.html?lang=it) per ottenere una stima di quanto tempo viene eseguito il test. (Come per il tradizionale test A/B, applica la correzione Bonferroni se stai testando più di due offerte o più di una metrica/ipotesi di conversione.) Questo calcolatore è progettato per i tradizionali test A/B a orizzonte fisso e fornisce solo una stima. Utilizzo del calcolatore per un [!UICONTROL Allocazione automatica] l’attività è facoltativa perché [!UICONTROL Allocazione automatica] dichiara un vincitore per te. Non è necessario scegliere un punto fisso per esaminare i risultati del test. I valori forniti sono sempre statisticamente validi. Nei nostri esperimenti, abbiamo trovato quanto segue:
* Quando si sottopongono a test esattamente due esperienze, [!UICONTROL Allocazione automatica] trova un vincitore più rapidamente del test a orizzonte fisso (ovvero l’intervallo temporale suggerito dal calcolatore delle dimensioni del campione) quando la differenza di prestazioni tra le esperienze è grande. Tuttavia, [!UICONTROL Allocazione automatica] potrebbe essere necessario più tempo per identificare un vincitore quando la differenza di prestazioni tra le esperienze è ridotta. In questi casi, i test a orizzonte fisso sarebbero generalmente terminati senza un risultato statisticamente significativo.
* Quando si sottopongono a test più di due esperienze, [!UICONTROL Allocazione automatica] trova un vincitore più rapidamente rispetto al test a orizzonte fisso (ovvero l’intervallo di tempo suggerito dal calcolatore delle dimensioni del campione) quando una singola esperienza esegue con maggiore efficienza tutte le altre esperienze. Quando due o più esperienze sono entrambe &quot;vincenti&quot; rispetto ad altre esperienze ma strettamente collegate tra loro, [!UICONTROL Allocazione automatica] potrebbe essere necessario più tempo per determinare quale sia superiore. In questi casi, i test a orizzonte fisso si sarebbero generalmente conclusi concludendo che le esperienze &quot;vincenti&quot; erano migliori delle esperienze con prestazioni peggiori, ma non hanno identificato quale fosse superiore.

### È necessario rimuovere un’esperienza insoddisfacente da un [!UICONTROL Allocazione automatica] attività per velocizzare il processo di determinazione di un vincitore?

Non c&#39;è alcun motivo per rimuovere un&#39;esperienza insoddisfacente. [!UICONTROL Allocazione automatica] fornisce automaticamente esperienze con prestazioni elevate più spesso e con minore frequenza quelle con prestazioni inferiori. Lasciare un’esperienza insoddisfacente nell’attività non influisce in modo significativo sulla velocità per determinare un vincitore.

Il 20% dei visitatori viene assegnato in modo casuale attraverso tutte le esperienze. La quantità di traffico destinata a un’esperienza con prestazioni inferiori è minima (20% diviso per il numero di esperienze).

### Posso cambiare la metrica dell’obiettivo a metà strada attraverso un [!UICONTROL Allocazione automatica] attività? {#change-metric}

[!DNL Adobe] non consiglia di modificare la metrica obiettivo a metà strada all’interno di un’attività. Anche se è possibile modificare la metrica dell’obiettivo durante un’attività utilizzando l’interfaccia utente [!DNL Target], è sempre necessario avviare una nuova attività. [!DNL Adobe] non garantisce cosa succede se modifichi la metrica di obiettivo in un&#39;attività dopo l&#39;esecuzione.

Questo consiglio si applica alle attività [!UICONTROL Allocazione automatica], [!UICONTROL Targeting automatico] e [!UICONTROL Automated Personalization] che utilizzano [!DNL Target] o [!DNL Analytics] (A4T) come origine per la generazione di rapporti.

### Posso cambiare l’origine per la generazione di rapporti nel corso di un’attività [!UICONTROL Allocazione automatica]? {#change-reporting}

[!DNL Adobe] non consiglia di modificare l’origine per la generazione di rapporti nel passaggio intermedio di un’attività . Sebbene sia possibile modificare l&#39;origine per la generazione di rapporti (da [!DNL Target] a A4T o viceversa) durante un’attività utilizzando [!DNL Target] Nell’interfaccia utente, dovresti sempre avviare una nuova attività. [!DNL Adobe] non garantisce cosa succede se modifichi l’origine per la generazione di rapporti in un’attività dopo l’esecuzione.

Questo consiglio si applica alle attività [!UICONTROL Allocazione automatica], [!UICONTROL Targeting automatico] e [!UICONTROL Automated Personalization] che utilizzano [!DNL Target] o [!DNL Analytics] (A4T) come origine per la generazione di rapporti.

### Posso utilizzare il [!UICONTROL Ripristina dati dei rapporti] durante l&#39;esecuzione di un [!UICONTROL Allocazione automatica] attività?

Utilizzo della [!UICONTROL Ripristina dati dei rapporti] opzione per [!UICONTROL Allocazione automatica] le attività non sono suggerite. Anche se rimuove i dati di reporting visibili, questa opzione non rimuove tutti i record di formazione dal [!UICONTROL Allocazione automatica] modello. Invece di utilizzare il [!UICONTROL Ripristina dati dei rapporti] opzione per [!UICONTROL Allocazione automatica] , crea una nuova attività e disattiva l’attività originale. (La presente guida si applica anche ai seguenti [!UICONTROL Targeting automatico] e [!UICONTROL Automated Personalization] attività).

### Come funziona [!UICONTROL Allocazione automatica] costruire modelli in relazione agli ambienti?

[!UICONTROL Allocazione automatica] crea modelli in base al comportamento di traffico e conversione registrato solo nell’ambiente predefinito. Per impostazione predefinita, [!UICONTROL Produzione] è l’ambiente predefinito, ma l’ambiente predefinito può essere modificato in [!DNL Target] [Amministrazione > Ambienti](/help/main/administrating-target/environments.md).

Se un hit si verifica in un altro ambiente (non predefinito), il traffico viene distribuito in base al comportamento di conversione osservato nell’ambiente predefinito. Il risultato di tale hit (conversione o non conversione) è registrato a scopo di reporting ma non è considerato nella variabile [!UICONTROL Allocazione automatica] modello.

Quando selezioni un altro ambiente, il rapporto mostra il traffico e le conversioni per tale ambiente. L’ambiente selezionato predefinito per un rapporto è l’impostazione predefinita a livello di account selezionata. L’ambiente predefinito non può essere impostato per attività.

### Può un [!UICONTROL Allocazione automatica] l’attività regola l’intervallo di lookback nel corso di un test per prendere in considerazione l’evoluzione delle tendenze nel tempo?

Ad esempio, l’attività può considerare il mese di dicembre per decidere come allocare il traffico, invece di esaminare i dati del visitatore di settembre (quando il test è iniziato)?

No, [!UICONTROL Allocazione automatica] considera le prestazioni dell&#39;intera attività.

### Does [!UICONTROL Allocazione automatica] mostrare un’esperienza vincente a un visitatore di ritorno se l’esperienza vincente è diversa da quella che il visitatore ha visto quando si qualifica per l’attività?

[!UICONTROL Allocazione automatica] utilizza decisioni permanenti per gli stessi motivi [!UICONTROL Test A/B] le attività sono appiccicose. L’allocazione del traffico funziona solo per i nuovi visitatori.

## Video di formazione {#section_893E5B36DC4A415C9B1D287F51FCCB83}

I video seguenti contengono ulteriori informazioni sui concetti descritti in questo articolo.

### Flusso di lavoro di un&#39;attività - Targeting (2:14) ![Icona Tutorial](/help/main/assets/tutorial.png)

Questo video include informazioni su come impostare l&#39;allocazione del traffico.

* Assegnare un pubblico all’attività
* Limitare il traffico verso l’alto o il basso
* Selezionare il metodo di allocazione del traffico
* Allocare il traffico tra diverse esperienze

>[!VIDEO](https://video.tv.adobe.com/v/17385)

### Creazione di test A/B (8:36) ![Badge tutorial](/help/main/assets/tutorial.png)

In questo video viene illustrato come creare un test A/A utilizzando il flusso di lavoro guidato in tre passaggi di Target. [!UICONTROL Allocazione automatica] viene discusso a partire dal minuto 4:45.

* Crea un’attività A/B in [!DNL Adobe Target]
* Allocare il traffico con suddivisione manuale o automatica del traffico

>[!VIDEO](https://video.tv.adobe.com/v/17391)
