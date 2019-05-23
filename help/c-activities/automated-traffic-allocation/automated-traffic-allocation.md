---
description: L’allocazione automatica identifica un vincitore tra due o più esperienze e, di conseguenza, ridistribuisce automaticamente più traffico per aumentare le conversioni, mentre il test continua a essere eseguito e ad apprendere.
keywords: allocazione automatica del traffico;targeting; incrementa il conteggio e mantieni l’utente nell’attività;allocazione del traffico
seo-description: L’allocazione automatica identifica un vincitore tra due o più esperienze e, di conseguenza, ridistribuisce automaticamente più traffico per aumentare le conversioni, mentre il test continua a essere eseguito e ad apprendere.
seo-title: Allocazione automatica
solution: Target
title: Allocazione automatica
topic: Standard
uuid: e8aee4d7-2b99-4e1f-8004-2efc820658b5
translation-type: tm+mt
source-git-commit: 5405e95cf516f973b69834ac114a1e351cd3040a

---


# Allocazione automatica{#auto-allocate}

L&#39;attribuzione automatica identifica un vincitore tra due o più esperienze e rende automaticamente più effettive il traffico verso il vincitore per aumentare le conversioni, mentre il test continua a essere eseguito e impara.

>[!IMPORTANT]
>
>L’allocazione automatica non supporta la creazione di rapporti per [!DNL Target for Analytics] (A4T).

Quando [crei un’attività A/B tramite il flusso di lavoro guidato in tre passaggi](../../c-activities/t-test-ab/t-test-create-ab/test-create-ab.md#task_68C8079BF9FF4625A3BD6680D554BB72), puoi scegliere l’opzione [!UICONTROL Allocazione automatica all’esperienza migliore].

## La sfida {#section_85D5A03637204BACA75E19646162ACFF}

I test A/B standard hanno un costo intrinseco. Devi investire del traffico per misurare le prestazioni di ogni esperienza e capire quale sia l’esperienza vincente attraverso l’analisi. La distribuzione del traffico rimane fissa anche dopo aver compreso che alcune esperienze hanno prestazioni migliori di altre. Inoltre, è complicato calcolare la dimensione necessaria del campione, e l’attività deve essere eseguita completamente prima di poter intervenire in base al vincitore. Dopo aver fatto tutto questo, c&#39;è ancora una possibilità che il vincitore identificato non sia un vero vincitore.

## La soluzione: Allocazione automatica  {#section_98388996F0584E15BF3A99C57EEB7629}

L’allocazione automatica riduce il costo e il sovraccarico associati al determinare un’esperienza vincente. L’allocazione automatica monitora le prestazioni della metrica obiettivo di tutte le esperienze e invia in modo proporzionale un numero maggiore di nuovi partecipanti alle esperienze che hanno prestazioni migliori. Per l’esplorazione delle altre esperienze viene riservata una quantità adeguata di traffico. È possibile vedere i vantaggi del test nei risultati, anche se l’attività è ancora in esecuzione: l’ottimizzazione si verifica in parallelo all’apprendimento.

L’allocazione automatica sposta gradualmente i visitatori verso esperienze vincenti, invece di richiedere di attendere fino a quando un’attività finisce per determinare un vincitore. Puoi beneficiare di incrementi più rapidi perché potenziali esperienze vincenti vengono mostrate a partecipanti che sarebbero altrimenti stati destinati a esperienze di minor successo.

Un normale test A/B in Target mostra solo confronti a coppie sfidante/controllo. Ad esempio, se un’attività ha le esperienze A, B, C e D, dove A è il controllo, un normale test A/B di Target confronterebbe A con B, A con C e A con D.

In tali test, la maggior parte dei prodotti, tra cui Target, utilizzano il calcolo del test t di Student per ottenere un indice di affidabilità basato sul valore p. Questo valore di affidabilità viene quindi utilizzato per determinare se lo sfidante è sufficientemente diverso dal controllo. Tuttavia, Target non esegue automaticamente i confronti impliciti (B con C, B con D e C con D) necessari per trovare l’esperienza effettivamente “migliore”. Di conseguenza, l’addetto al marketing deve analizzare manualmente i risultati per determinare l’esperienza “migliore”.

L’allocazione automatica esegue tutti i confronti impliciti tra le esperienze e produce un vincitore “reale”. Non vi è alcuna nozione di esperienza di “controllo” nel test.

L’allocazione automatica assegna nuovi visitatori alle esperienze fino a quando l’intervallo di affidabilità della migliore esperienza non si sovrappone a quello di qualsiasi altra esperienza. Normalmente questo processo potrebbe produrre falsi positivi, ma l’allocazione automatica utilizza intervalli di affidabilità in base alla [disuguaglianza di Bernstein](https://en.wikipedia.org/wiki/Bernstein_inequalities_(probability_theory)) che compensa le valutazioni ripetute. A questo punto, abbiamo un vincitore reale. Quando si interrompe automaticamente l&#39;allocazione, a condizione che non esista una dipendenza temporale sostanziale per i visitatori che arrivano alla pagina, esiste almeno una probabilità del 95% che restituisce un&#39;esperienza la cui risposta effettiva non è peggiore di 1% (relativo) rispetto alla risposta effettiva dell&#39;esperienza vincente.

## Quando utilizzare Allocazione automatica, A/B o Personalizzazione automatizzata  {#section_3F73B0818A634E4AAAA60A37B502BFF9}

* Utilizza l&#39;**Allocazione automatica** quando vuoi ottimizzare l&#39;attività fin dall&#39;inizio e identificare le esperienze vincenti il più rapidamente possibile. Fornendo con maggiore frequenza le esperienze che hanno prestazioni migliori, aumentano le prestazioni complessive di attività.
* Utilizza un **[Test A/B](../../c-activities/t-test-ab/test-ab.md#task_05E33EB15C4D4459B5EAFF90A94A7977)** standard quando vuoi caratterizzare le prestazioni di tutte le esperienze prima di ottimizzare il sito. Un test A/B ti aiuta a classificare tutte le tue esperienze, mentre l&#39;Allocazione automatica del traffico trova i migliori risultati ma non garantisce la differenziazione fra quelli minori.
* Usa la [Personalizzazione automatizzata](../../c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9) quando desideri algoritmi di ottimizzazione della complessità più elevata, ad esempio modelli di apprendimento automatico che generano stime basate su attributi di profilo individuali. L’Allocazione automatica del traffico esamina il comportamento aggregato delle esperienze (proprio come i test A/B standard) e non distingue tra i visitatori.

## Vantaggi chiave  {#section_0913BF06F73C4794862561388BBDDFF0}

* Mantiene la rigorosità di un test A/B
* Trova un vincitore statisticamente significativo più velocemente rispetto a un test A/B manuale.
* Fornisce un maggiore incremento medio della campagna rispetto a un test A/B manuale.

## Terminologia {#section_670F8785BA894745B43B6D4BFF953188}

I seguenti termini sono utili quando si parla di Allocazione automatica:

**Slot machine:** un approccio all’ottimizzazione ti tipo [slot machine](https://en.wikipedia.org/wiki/Multi-armed_bandit) compensa l’apprendimento esplorativo e il suo sfruttamento.

## Funzionamento dell’algoritmo {#section_ADB69A1C7352462D98849F2918D4FF7B}

La logica complessiva alla base dell&#39;allocazione automatica incorpora sia le prestazioni misurate (come il tasso di conversione) sia intervalli di affidabilità dei dati cumulativi. A differenza di un test A/B standard in cui il traffico è diviso in modo uniforme tra le esperienze, l&#39;allocazione automatica alloca le modifiche del traffico tra le esperienze.

* L&#39;80% dei visitatori è assegnato utilizzando la logica intelligente descritta di seguito.
* Il 20% dei visitatori è assegnato in modo casuale in tutte le esperienze, al fine di adattarsi al cambiamento del comportamento dei visitatori.

L&#39;approccio slot machine consente di riservare alcune esperienze all’esplorazione, sfruttando le esperienze che danno buoni risultati. Un numero maggiore di nuovi visitatori vedrà le esperienze migliori, ma sarà comunque possibile reagire in caso di condizioni mutevoli. Questi modelli si aggiornano almeno una volta all&#39;ora per assicurarsi che il modello reagisca ai dati più recenti.

Man mano che più visitatori accedono all’attività, alcune esperienze iniziano a dimostrarsi di maggior successo e viene quindi incrementato il traffico inviato a tali esperienze. Il 20% del traffico continua a contribuire casualmente all’esplorazione di tutte le esperienze. Se una delle esperienze dalle prestazioni peggiori inizia a ottenere risultati migliori, le viene allocato più traffico. Oppure se il successo di un’attività con ottime prestazioni diminuisce, le viene assegnato meno traffico. Questo si verifica ad esempio se i visitatori cercano informazioni diverse sul tuo sito multimediale a causo di un particolare evento oppure se le offerte speciali del fine settimana nel tuo sito retail generano risultati diversi.

Nell&#39;illustrazione seguente viene mostrato come potrebbe comportarsi l&#39;algoritmo durante un test con quattro esperienze:

![](assets/auto-allocate.png)

L&#39;illustrazione mostra come il traffico assegnato a ogni esperienza progredisca nell&#39;acro di parecchi turni della durata dell&#39;attività, finché non sia possibile determinare un chiaro vincitore.

| Turno | Descrizione |
|--- |--- |
| ![Turno di riscaldamento](/help/c-activities/automated-traffic-allocation/assets/aa-phase-0.png) | **Turno di riscaldamento (0)**: durante il turno di riscaldamento, ogni esperienza ottiene pari ripartizione del traffico fino a quando ogni esperienza in attività ha un minimo di 1.000 visitatori e 50 conversioni.<ul><li>Esperienza A=25%</li><li>Esperienza B=25%</li><li>Esperienza C=25%</li><li>Esperienza D=25%</li></ul>Dopo che ogni esperienza ottiene 1.000 visitatori e 50 conversioni, Target avvia l&#39;allocazione automatica del traffico. Tutte le allocazioni avvengono in turni e vengono raccolte due esperienze per ogni turno.<br>Solo due esperienze progrediscono al turno successivo: D e C.<br>Progredire significa che alle due esperienze è assegnato l’80% del traffico equamente, mentre le altre due esperienze continuano a partecipare ma con solo il 20% dell’allocazione casuale del traffico generato da nuovi visitatori che accedono all’attività.<br>Tutte le allocazioni vengono aggiornate ogni ora (mostrato in alto per turni lungo l&#39;asse x). Dopo ogni turno, i dati cumulativi vengono confrontati. |
| ![Turno 1](/help/c-activities/automated-traffic-allocation/assets/aa-phase-1.png) | **Turno 1**: durante questo turno, l’80% di traffico è assegnato alle esperienze C e D (40% ciascuna). Il 20% del traffico viene assegnato in modo casuale alle esperienze A, B, C e D (5% ciascuna). Durante questo turno, l&#39;esperienza A registra buoni risultati.<ul><li>L&#39;algoritmo sceglie l&#39;esperienza D per passare al turno successivo perché ha il più alto tasso di conversione (come indicato da sulla scala verticale di ogni attività).</li><li>L&#39;algoritmo sceglie anche l&#39;esperienza A per proseguire perché, tra le esperienze rimanenti, ha il limite superiore più alto dell&#39;intervallo di affidabilità Bernstein al 95%.</li></ul>Le esperienze D e A proseguono. |
| ![Turno 2](/help/c-activities/automated-traffic-allocation/assets/aa-phase-2.png) | **Turno 2**: durante questo turno, l’80% del traffico è assegnato alle esperienze A e D (40% ciascuna). Il 20% del traffico è allocato in modo casuale, quindi A, B, C e D ricevono rispettivamente il 5% del traffico. Durante questo turno, l’esperienza B registra buoni risultati.<ul><li>L&#39;algoritmo sceglie l&#39;esperienza D per passare al turno successivo perché ha il più alto tasso di conversione (come indicato da sulla scala verticale di ogni attività).</li><li>L&#39;algoritmo sceglie anche l&#39;esperienza B per proseguire perché, tra le esperienze rimanenti, ha il limite superiore più alto dell&#39;intervallo di affidabilità Bernstein al 95%.</li></ul>Le esperienze D e B proseguono. |
| ![Turno 3](/help/c-activities/automated-traffic-allocation/assets/aa-phase-3.png) | **Turno 3**: durante questo turno, l’80% di traffico è assegnato alle esperienze B e D (40% ciascuna). Il 20% del traffico è allocato in modo casuale, quindi A, B, C e D ricevono rispettivamente il 5% del traffico. Durante questo turno, l&#39;esperienza D continua a fornire buoni risultati, così come l&#39;esperienza C.<ul><li>L&#39;algoritmo sceglie l&#39;esperienza D per passare al turno successivo perché ha il più alto tasso di conversione (come indicato da sulla scala verticale di ogni attività).</li><li>L&#39;algoritmo sceglie anche l&#39;esperienza C per proseguire perché, tra le esperienze rimanenti, ha il limite superiore più alto dell&#39;intervallo di affidabilità Bernstein al 95%.</li></ul>Le esperienze D e C proseguono. |
| ![Turno 4](/help/c-activities/automated-traffic-allocation/assets/aa-phase-4.png) | **Turno 4**: durante questo turno, l’80% di traffico è assegnato alle esperienze C e D (40% ciascuna). Il 20% del traffico è allocato in modo casuale, quindi A, B, C e D ricevono rispettivamente il 5% del traffico. Durante questo turno, l&#39;esperienza C risulta avere buone prestazioni.<ul><li>L&#39;algoritmo sceglie l&#39;esperienza C per passare al turno successivo perché ha il più alto tasso di conversione (come indicato da sulla scala verticale di ogni attività).</li><li>L&#39;algoritmo sceglie anche l&#39;esperienza D per proseguire perché, tra le esperienze rimanenti, ha il limite superiore più alto dell&#39;intervallo di affidabilità Bernstein al 95%.</li></ul>Le esperienze C e D proseguono. |
| ![Turno n](/help/c-activities/automated-traffic-allocation/assets/aa-phase-n.png) | **Turno n**: mentre l&#39;attività progredisce, inizia a emergere un&#39;esperienza con prestazioni elevate e il processo continua fino a individuare un&#39;esperienza vincente. Quando l’intervallo di confidenza dell’esperienza con il tasso di conversione più elevato non si sovrappone all’intervallo di confidenza di qualsiasi altra esperienza, questa viene contrassegnata come vincitrice e un [badge compare nella pagina dell’attività](/help/c-activities/automated-traffic-allocation/determine-winner.md) e nell’elenco Attività.<ul><li>L&#39;algoritmo sceglie l’esperienza C come chiaro vincitore</li></ul>A questo punto l&#39;algoritmo indirizza l’80% del traffico all’esperienza C, mentre il 20% del traffico continua a essere indirizzato casualmente a tutte le esperienze (A, B, C e D). In totale, C ottiene l’85% del traffico. Nel caso improbabile che l’intervallo di affidabilità del vincitore inizi a sovrapporsi di nuovo cpn quello di un’altra esperienza, l’algoritmo ritorna al comportamento del turno 4 di cui sopra.<br>**Importante**: se scegliessi manualmente un vincitore in una fase precedente del processo, rischieresti di scegliere l’esperienza sbagliata. Per questo motivo, è consigliabile attendere che l’algoritmo determini l’esperienza vincente. |

Se l’attività ha solo due esperienze, entrambe ottengono la stessa quantità di traffico fino a quando Target trova un’esperienza con il 90% di affidabilità. A quel punto, il 70% del traffico viene assegnato all’esperienza vincente e il 30% a quella perdente. Quando l’esperienza raggiunge il 95% di affidabilità, viene assegnato il 100% del traffico all’esperienza vincente e lo 0% a quella perdente.

Una volta pronto il modello per un’attività di allocazione automatica (ogni esperienza ha un minimo di 1.000 visitatori e 50 conversioni), non sono consentite le seguenti operazioni dall’interfaccia utente:

* Impostazione della modalità di Allocazione traffico su Manuale
* Modifica del tipo di metrica obiettivo
* Modifica delle opzioni nel pannello “Impostazioni avanzate”

## Avvertenze {#section_5C83F89F85C14FD181930AA420435E1D}

**Le attività di allocazione automatica A/B non sono più supportate in Analytics for Target (A4T).**

A partire dalla versione 16.10.1.0 (25 ottobre 2016), Target non supporta Analytics come origine dei rapporti per le attività A/B con Allocazione automatica. Tutte le attività A/B con Allocazione automatica attive con A4T abilitato passeranno alla modalità Manuale (allocazione del traffico in parti uguali).

**La funzione Allocazione automatica funziona con una sola impostazione di metriche avanzate: Incrementa il conteggio e mantieni l’utente nell’attività**

Le seguenti impostazioni di metriche avanzate non sono supportate: “Incrementa il conteggio, rilascia l’utente e consenti nuovo accesso” e “Incrementa il conteggio, rilascia l’utente e impedisci nuovo accesso”.

**I visitatori di ritorno frequenti possono gonfiare i tassi di conversione dell’esperienza.**

Se un visitatore che vede l’esperienza A torna frequentemente e la sua conversione si verifica più volte, il tasso di conversione (CR) dell’esperienza A aumenta artificialmente. Confronta con questo caso con l’esperienza B, dove si verifica la conversione dei visitatori ma questi non tornano spesso. Di conseguenza, il tasso di conversione di A sembra migliore rispetto al tasso di conversione di B, e i nuovi visitatori hanno quindi maggiori probabilità di essere assegnati ad A anziché a B. Se scegli di eseguire il conteggio una volta per partecipante, il tasso di conversione di A e quello di B potrebbero risultare identici.

Se i visitatori di ritorno sono distribuiti in modo casuale, è più probabile che il loro effetto sui tassi di conversione venga mitigato. Per attenuare questo effetto, è consigliabile modificare il metodo di conteggio della metrica obiettivo per conteggiare ogni partecipante una sola volta.

**Differenzia fra esperienze con prestazioni elevate, non fra quelle con prestazioni inferiori.**

La funzione Allocazione automatica è in grado di distinguere tra le esperienze dalle prestazioni migliori (e trovare un vincitore). Ci potrebbero essere momenti in cui non vi è abbastanza differenziazione tra le esperienze con prestazioni inferiori.

Se desideri produrre una differenziazione statisticamente significativa tra tutte le esperienze, considera l&#39;utilizzo della modalità di Allocazione traffico manuale.

**I tassi di conversione correlati al tempo (o contestualmente variabili) possono distorcere le proporzioni di allocazione.**

Alcuni fattori che possono essere ignorati durante un test A/B standard perché influiscono ugualmente su tutte le esperienze non possono essere ignorati in un test di Allocazione automatica. L&#39;algoritmo è sensibile ai tassi di conversione osservati. Di seguito sono riportati alcuni esempi di fattori che possono influenzare le prestazioni dell&#39;esperienza in modo disuguale:

* Esperienze con rilevanza contestuale (fattore temporale, posizione, genere, ecc.) variabile.

   Ad esempio:

   * “Grazie a Dio è venerdì” genera un maggior numero di conversioni il venerdì.
   * “Accendi il tuo lunedì” genera un maggior numero di conversioni il lunedì.
   * “Preparati per un inverno in montagna” genera un maggior numero di conversioni nelle regioni di montagna o in quelle con inverni più rigorosi.

Queste situazioni possono sfalsare i risultati di un test di Allocazione automatica più che quelli di un test A/B, perché il test A/B analizza i risultati su un periodo più lungo.

* Esperienze con ritardi diversi nella conversione possono essere dovute all’urgenza del messaggio.

   Ad esempio, “i saldi al 30% finiscono oggi” incita il visitatore ad eseguire oggi stesso la conversione, mentre “50% di sconto sul primo acquisto” non crea lo stesso senso di urgenza.

## Domande frequenti {#section_0E72C1D72DE74F589F965D4B1763E5C3}

**I visitatori di ritorno vengono riallocati automaticamente alle esperienze con prestazioni elevate?**

No. Solo i nuovi visitatori vengono allocati automaticamente. I visitatori di ritorno continuano a vedere la loro esperienza originale. Questo protegge la validità del test A/B.

**In che modo l’algoritmo tratta i falsi positivi?**

L’algoritmo garantisce un&#39;affidabilità del 95% o un tasso di falsa positività del 5% se si attende che appaia il badge del vincitore.

**Quando Allocazione automatica inizia ad allocare il traffico?**

L’algoritmo inizia a funzionare dopo che tutte le esperienze nell’attività hanno un minimo di 1.000 visitatori e 50 conversioni.

**Quanto aggressivamente viene applicato l’algoritmo?**

L’80% del traffico viene servito con Allocazione automatica e il 20% del traffico viene servito in modo casuale. Quando viene identificato un vincitore, a tutto l&#39;80% del traffico viene veicolata l’esperienza vincente, mentre tutte le esperienze continuano a ricevere un certo traffico come parte del 20%, compresa quella vincente.

**Le esperienze perdenti vengono mostrate?**

Sì. Con un approccio di tipo slot machine, almeno il 20% del traffico è riservato all’esplorazione di modifiche nei pattern o nei tassi di conversione in tutte le esperienze.

**Cosa succede alle attività con tempi di conversione lunghi?**

Fintanto che tutte le esperienze ottimizzate avranno ritardi simili, il comportamento è lo stesso di un&#39;attività con un ciclo di conversione più veloce. Tuttavia sarà necessario più tempo per raggiungere la soglia di 50 conversiono superata la quale inizierà il processo di allocazione del traffico.

**Quali sono le differenze tra Allocazione automatica e Personalizzazione automatizzata?**

La funzione Personalizzazione automatizzata utilizza gli attributi del profilo di ogni visitatore per determinare l&#39;esperienza migliore. In tal modo, non solo ottimizza, ma personalizza anche l’attività per quell’utente.

La funzione Allocazione automatica, invece, è un test A/B che produce un vincitore aggregato (l’esperienza più popolare, ma non necessariamente più efficace per ogni visitatore).

**I visitatori di ritorno gonfiano il tasso di conversione sulla metrica di successo?**

Attualmente, la logica favorisce i visitatori che si convertono rapidamente o che effettuano visite frequenti. Questo perché tali visitatori aumentano temporaneamente il tasso di conversione complessivo dell’esperienza a cui appartengono. L’algoritmo si regola frequentemente, quindi l’aumento del tasso di conversione viene amplificato in ogni istantanea. Se il sito riceve molti di visitatori di ritorno, le loro conversioni possono potenzialmente aumentare il tasso di conversione globale per l’esperienza a cui appartengono. C&#39;è una buona probabilità che i visitatori di ritorno siano distribuiti in modo casuale, nel qual caso l’effetto aggregato (aumento dell’incremento) è mitigato. Per attenuare questo effetto, è consigliabile modificare il metodo di conteggio della metrica di sucesso per conteggiare ogni partecipante una sola volta.

**È possibile utilizzare l&#39;utilità di calcolo delle dimensioni del campione quando si utilizza Auto-Allocation (Allocazione automatica) per valutare il tempo necessario per identificare il vincitore?**

Puoi utilizzare il [Calcolatore dimensione campione](https://docs.adobe.com/content/target-microsite/testcalculator.html) esistente con la correzione Bonferroni applicata in modo appropriato per stimare la durata del test. Nei nostri esperimenti, abbiamo visto che l’attività Allocazione automatica finisce molto prima di questa dimensione campione.

**È necessario rimuovere un&#39;esperienza insoddisfacente da un&#39;attività di allocazione automatica per velocizzare il processo di determinazione di un vincitore?**

Non esiste alcun motivo per rimuovere un&#39;esperienza insoddisfacente. L&#39;allocazione automatica fornisce esperienze ad alto prestazioni più spesso e rende meno performanti le esperienze meno performanti. L&#39;utilizzo di un&#39;esperienza insoddisfacente nell&#39;attività non influisce in modo significativo sulla velocità per determinare una vincente.

Il 20% dei visitatori viene assegnato in modo casuale in tutte le esperienze. La quantità di traffico utilizzata per un&#39;esperienza insoddisfacente è limitata (20% per il numero di esperienze).

## Video di formazione {#section_893E5B36DC4A415C9B1D287F51FCCB83}

I video seguenti contengono ulteriori informazioni sui concetti descritti in questo articolo.

### Flusso di lavoro di un&#39;attività - Targeting (2:14)

Questo video include informazioni su come impostare l&#39;allocazione del traffico.

* Assegnare un pubblico all’attività
* Limitare il traffico verso l’alto o il basso
* Selezionare il metodo di allocazione del traffico
* Allocare il traffico tra diverse esperienze

>[!VIDEO](https://video.tv.adobe.com/v/17385)

### Creazione di test A/B (8:36)

In questo video viene illustrato come creare un test A/A utilizzando il flusso di lavoro guidato in tre passaggi di Target. L’allocazione automatica del traffico è trattata a partire dal minuto 4:45.

* Creare un’attività A/B in Adobe Target
* Allocare il traffico con suddivisione manuale o automatica del traffico

>[!VIDEO](https://video.tv.adobe.com/v/17391)