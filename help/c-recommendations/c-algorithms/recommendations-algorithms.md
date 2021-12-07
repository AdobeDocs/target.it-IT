---
keywords: algoritmi di consigli;formazione del modello;distribuzione del modello;distribuzione del contenuto;basato su elementi;basato su utenti;basato sulla popolarità;basato su carrello;criteri personalizzati
description: Scopri gli algoritmi utilizzati in [!DNL Target Recommendations], compresi l'addestramento dei modelli e il servizio dei modelli.
title: Dove Posso Imparare La Scienza Dietro Gli Algoritmi Recommendations?
feature: Recommendations
mini-toc-levels: 2
source-git-commit: 7c84c22fe87ddb41587899438381e2dfd2801d86
workflow-type: tm+mt
source-wordcount: '2795'
ht-degree: 0%

---

# ![PREMIUM](/help/assets/premium.png) La scienza dietro gli algoritmi Recommendations

Una descrizione dettagliata degli algoritmi utilizzati in [!DNL Adobe Target Recommendations], compresi i dettagli logici e matematici della formazione dei modelli e il processo di elaborazione dei modelli.

La formazione modello è il processo di generazione dei consigli da parte di [!DNL Adobe Target] algoritmi di apprendimento. Il modello di servizio è il modo in cui [!DNL Target] fornisce consigli ai visitatori del tuo sito (noto anche come consegna di contenuti).

[!DNL Target] include i seguenti grandi tipi di algoritmi in [!DNL Recommendations]:

* **Algoritmi basati su elementi**: Includere algoritmi che seguono la logica &quot;Chi ha visualizzato/acquistato questo elemento ha visualizzato/acquistato anche questi elementi&quot;. Questi algoritmi sono raggruppati sotto il filtro collaborativo elemento-elemento ombrello, nonché [!UICONTROL Articoli con attributi simili] algoritmi.

* **Algoritmi basati su utente**: Includi il [!UICONTROL Visualizzato di recente] e [!UICONTROL Consigliato per te] algoritmi.

* **Algoritmi basati sulla popolarità**: Includere gli algoritmi che restituiscono gli elementi più visualizzati o più acquistati nel sito web oppure quelli più visualizzati o più acquistati per categoria o attributo di elemento.

* **Algoritmi basati su carrello**: Includere consigli basati su più elementi con la logica &quot;chi ha visualizzato/acquistato questi elementi, ha anche visualizzato/acquistato tali elementi&quot;.

* **Criteri personalizzati**: Includi consigli basati su file personalizzati caricati in [!DNL Target].

>[!NOTE]
>
>Per informazioni più generali su ciascun tipo di algoritmo e sui singoli algoritmi, consulta [Basare il consiglio su una chiave consiglio](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md).

Molti degli algoritmi elencati sopra sono basati sulla presenza di una o più chiavi. Queste chiavi vengono utilizzate per recuperare elementi simili al momento della distribuzione dei contenuti (quando vengono eseguiti i consigli). Le chiavi specificate dal cliente possono includere l&#39;articolo corrente visualizzato, l&#39;ultimo articolo visualizzato o acquistato, l&#39;articolo più visualizzato, la categoria corrente o la categoria preferita del visitatore. Altri algoritmi, come consigli basati su carrello o basati su utente, utilizzano chiavi implicite (che non possono essere configurate dal cliente). Per ulteriori informazioni, consulta *Chiavi dei consigli*, in [Basare il consiglio su una chiave consiglio](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#keys). Tuttavia, queste chiavi sono rilevanti solo per il tempo di trasmissione del modello (consegna del contenuto). Queste chiavi non influiscono sulla logica &quot;offline&quot; o del tempo di formazione del modello.

Le sezioni seguenti raggruppano gli algoritmi in modo leggermente diverso rispetto ai tipi di algoritmo descritti in precedenza. Il raggruppamento seguente si basa sulla somiglianza della logica di formazione del modello.

## Filtro collaborativo elemento

Gli algoritmi includono:

* [!UICONTROL Chi ha visualizzato questo ha visualizzato anche quello]
* [!UICONTROL Chi ha visualizzato questo ha acquistato anche quello]
* [!UICONTROL Chi ha comprato questo ha acquistato anche quello]

Gli algoritmi per i consigli di filtro collaborativo per elemento si basano sull’idea di utilizzare i modelli comportamentali di molti utenti (di conseguenza collaborativi) per fornire consigli utili per un dato elemento (ad esempio, filtrare il catalogo di possibili elementi da consigliare). Anche se ci sono molti algoritmi diversi che rientrano sotto l&#39;ombrello generale di [filtro collaborativo](https://en.wikipedia.org/wiki/Collaborative_filtering), questi algoritmi utilizzano universalmente origini di dati comportamentali come input. In [!DNL Target Recommendations], questi input sono le visualizzazioni e gli acquisti univoci di elementi da parte degli utenti.

Per le persone che hanno visualizzato/acquistato questo elemento hanno visualizzato/acquistato anche questi elementi, l&#39;obiettivo è quello di calcolare una somiglianza s(A,B) tra tutte le coppie di elementi. Per un dato elemento A, i consigli principali sono quindi ordinati in base alla loro somiglianza s(A,B).

Un esempio di tale somiglianza è la co-occorrenza tra gli elementi: un conteggio semplice del numero di utenti che hanno acquistato entrambi gli articoli. Anche se intuitivo, una tale metrica è ingenua in quanto è tendenziosa nel raccomandare elementi popolari. Ad esempio, se in un negozio di alimentari la maggior parte delle persone acquista il pane, il pane avrà un&#39;elevata co-occorrenza con tutti gli articoli, ma non è necessariamente una buona raccomandazione. [!DNL Target] utilizza invece una metrica di somiglianza più sofisticata nota come rapporto di probabilità del registro (LLR). Questa quantità è grande quando la probabilità che due articoli, A e B, si verifichino congiuntamente è molto diversa dalla probabilità che non si verifichino contemporaneamente. Per la concretezza, considera un caso di [!UICONTROL Chi ha visualizzato questo ha acquistato anche quello] algoritmo. La somiglianza LLR è grande quando la probabilità che B sia stato acquistato è indipendente dal fatto che qualcuno abbia visto o meno A.

Ad esempio, se

![Formula](assets/formula.png)

allora l&#39;articolo B non dovrebbe essere consigliato con l&#39;articolo A. Sono forniti i dettagli completi di questo calcolo della somiglianza del rapporto di probabilità del log [in questo PDF](/help/c-recommendations/c-algorithms/assets/log-likelihood-ratios-recommendation-algorithms.pdf).

Il flusso logico dell’implementazione effettiva dell’algoritmo è mostrato nel seguente diagramma schematico:

![Schema](assets/diagram1.png)

Di seguito sono riportati i dettagli relativi a questi passaggi:

* **Dati di input**: Dati comportamentali, sotto forma di visualizzazioni e acquisti di visitatori raccolti quando [implementare Target](/help/c-recommendations/plan-implement.md#pass-behavioral) o [Adobe Analytics](/help/c-recommendations/c-algorithms/use-adobe-analytics-with-recommendations.md).

* **Formazione modello**:

   * **Pulizia e campionamento dei dati**: Per gli algoritmi con un lookback di n giorni, i dati comportamentali vengono prima filtrati per includere solo i N giorni di dati. Le regole di raccolta e le esclusioni globali vengono quindi applicate per rimuovere eventuali elementi che non dovrebbero essere consigliati. Infine, per i visitatori che hanno interagito con più di 1.000 elementi i dati di utilizzo sono stati campionati a soli 1.000 elementi.
   * **Calcolo della somiglianza degli elementi**: Questo è il passaggio del calcolo principale: calcolando la somiglianza del rapporto di probabilità del registro tra tutte le coppie di articoli candidati e le coppie di classificazioni di articoli in base a questo punteggio di somiglianza.
   * **Filtro offline**: Infine, vengono applicati eventuali altri filtri dinamici applicabili (ad esempio, esclusioni di categorie dinamiche). Dopo questo passaggio, i consigli precalcolati vengono memorizzati nella cache globale per essere disponibili per il servizio.

* **Servizio del modello**: I contenuti Recommendations vengono consegnati da [!DNL Target]s [rete &quot;Edge&quot; globale](/help/c-intro/how-target-works.md#concept_0AE2ED8E9DE64288A8B30FCBF1040934). Quando vengono effettuate richieste mbox a [!DNL Target] ed è determinato che il contenuto delle raccomandazioni deve essere consegnato alla pagina, la richiesta di [chiave elemento](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#keys) per l’algoritmo di consigli viene analizzato dalla richiesta o cercato dal profilo utente, e quindi utilizzato per recuperare i consigli calcolati nei passaggi precedenti. In questo momento vengono applicati altri filtri dinamici, prima dell&#39;appropriato [progettazione](/help/c-recommendations/c-design-overview/create-design.md) viene eseguito il rendering.

## Somiglianza del contenuto

Algoritmo incluso:

* [!UICONTROL Articoli con attributi simili]

In questo tipo di algoritmo, due elementi sono considerati correlati se i loro nomi e le loro descrizioni testuali sono semanticamente simili. A differenza della maggior parte degli algoritmi di consigli in cui è necessario utilizzare le origini di dati comportamentali, gli algoritmi di somiglianza del contenuto utilizzano metadati provenienti dai cataloghi di prodotti per ricavare la somiglianza tra gli elementi. [!DNL Target] è quindi in grado di indirizzare i consigli in scenari di cosiddetto &quot;avviamento a freddo&quot;, in cui non sono stati raccolti dati comportamentali (ad esempio, all’inizio di un [!DNL Target] attività).

Anche se il modello di distribuzione e la distribuzione dei contenuti di [!DNL Target]Gli algoritmi di somiglianza del contenuto sono identici ad altri algoritmi basati su elementi, i passaggi di formazione del modello sono drasticamente diversi e comportano una serie di fasi di elaborazione e preelaborazione del linguaggio naturale, come illustrato nel diagramma seguente. Il nucleo del calcolo della somiglianza è l’utilizzo della somiglianza del coseno dei vettori tf-idf modificati che rappresentano ogni elemento del catalogo.

![Diagramma 2](assets/diagram2.png)

Di seguito sono riportati i dettagli relativi a questi passaggi:

* **Dati di input**: Come descritto in precedenza, questo algoritmo si basa esclusivamente sui dati del catalogo (acquisiti in [!DNL Target] tramite [Feed catalogo, API Entità o da aggiornamenti su pagina](/help/c-recommendations/plan-implement.md#rec-catalog).

* **Formazione modello**:

   * **Estrazione di attributi**: Dopo l’applicazione di filtri statici regolari, regole di catalogo ed esclusioni globali, questo algoritmo estrae i campi testuali pertinenti dallo schema delle entità. [!DNL Target] utilizza automaticamente i campi nome, messaggio e categoria dagli attributi di entità e tenta di estrarre qualsiasi campo stringa da campi personalizzati [attributi di entità](/help/c-recommendations/c-products/entity-attributes.md). Questo processo viene eseguito assicurando che la maggior parte dei valori per quel campo non siano analizzabili come numero, data o valore booleano.
   * **Rimozione di graffi e stop word**: Per una corrispondenza più precisa della somiglianza del testo, è prudente rimuovere le parole &quot;stop&quot; molto comuni che non alterano in modo significativo il significato di un elemento (ad esempio, &quot;era&quot;, &quot;è&quot;, &quot;e&quot; e così via). Allo stesso modo, stemming si riferisce al processo di riduzione delle parole con suffissi diversi alla loro parola principale, che ha un significato identico (per esempio, &quot;connect&quot;, &quot;connect&quot; e &quot;connection&quot; hanno tutte la stessa parola principale: &quot;connect&quot;). [!DNL Target] usa il grembiule Snowball. [!DNL Target] esegue il rilevamento automatico della lingua prima di tutto, e può interrompere la rimozione delle parole per un massimo di 50 lingue e può stemming per 18 lingue.
   * **creazione n-grammo**: Dopo i passaggi precedenti, ogni parola viene trattata come un token. Il processo di combinazione di sequenze contigue di token in un unico token è noto come creazione n-grammo. [!DNL Target]Gli algoritmi considerano fino a 2 grammi.
   * **calcolo tf-idf**: Il passaggio successivo prevede la creazione di vettori tf-idf per riflettere l’importanza relativa dei token nella descrizione dell’elemento. Per ogni token/termine t in un elemento i, in un catalogo D con |D| elementi, il termine TF(t, i) è calcolato per primo (il numero di volte in cui il termine appare nella voce i) e la frequenza del documento DF(t, D). In sostanza, il numero di elementi in cui il token esiste. La misura tf-idf viene quindi

      ![Formula](assets/formula2.png)

      [!DNL Target] utilizza Apache Spark&#39;s *tf-idf* implementazione di funzionalità, che sotto la cappa hash ogni token a uno spazio di 218 token. In questo passaggio, l&#39;incremento e la sottrazione degli attributi specificati dal cliente vengono applicati anche regolando le frequenze dei termini in ciascun vettore in base alle impostazioni specificate nel [criteri](/help/c-recommendations/c-algorithms/create-new-algorithm.md#similarity).

   * **Calcolo della somiglianza degli elementi**: Il calcolo della somiglianza dell’elemento finale viene effettuato utilizzando una somiglianza approssimativa del coseno. Per due elementi: *A* e *B*, con i vettori a e tB, la somiglianza del coseno è definita come:

      ![Formula](assets/formula3.png)

      Per evitare una complessità significativa nel calcolo delle somiglianze tra tutti gli elementi N x N, il *tf-idf* il vettore viene troncato per contenere solo le sue 500 voci più grandi, quindi calcola le somiglianze coseno tra gli elementi utilizzando questa rappresentazione vettoriale troncata. Questo approccio risulta più robusto per i calcoli con somiglianza vettoriale sparsa, rispetto ad altre tecniche di approssimazione del vicino più vicino (ANN), come l’hashing sensibile alla posizione.

* **Servizio del modello**: Questo processo è identico alle tecniche di filtro collaborativo articolo-elemento descritte nella sezione precedente.

## Raccomandazioni multi-chiave

Gli algoritmi includono:

* Raccomandazioni basate su carrello
* [!UICONTROL Consigliato]

Le ultime aggiunte alla [!DNL Target] suite di algoritmi di consigli [!UICONTROL Consigliato] e una serie di algoritmi di consigli basati su carrello. Entrambi i tipi di algoritmi utilizzano tecniche di filtro collaborativo per formare consigli basati su singoli elementi. Quindi, al momento del servizio, più elementi nella cronologia di navigazione dell&#39;utente (per [!UICONTROL Consigliato]) o il carrello corrente dell’utente (per i consigli basati su carrello) viene utilizzato per recuperare questi consigli basati su elementi, che vengono quindi uniti per formare l’elenco finale dei consigli. Tenete presente che esistono molti tipi di algoritmi di raccomandazione personalizzati. La scelta di un algoritmo chiave multipla significa che i consigli sono immediatamente disponibili dopo che un visitatore dispone di una cronologia di navigazione e i consigli possono essere aggiornati per rispondere al comportamento più recente dei visitatori.

Questi algoritmi si basano sulle tecniche di filtro collaborativo di base descritte nella sezione consigli basati su elementi, ma incorporano anche la regolazione degli iperparametri per determinare la metrica di somiglianza ottimale tra gli elementi. L&#39;algoritmo esegue una suddivisione cronologica dei dati comportamentali per ogni utente e prepara i modelli di raccomandazioni sui dati precedenti mentre tenta di prevedere gli elementi che un utente visualizza o acquista in un secondo momento. La metrica di somiglianza che produce l&#39;ottimale [Precisione media media media media](https://en.wikipedia.org/wiki/Evaluation_measures_(information_retrieval)#Mean_average_precision) viene quindi scelto.

La logica dei passaggi di formazione e valutazione del modello è mostrata nel diagramma seguente:

![Diagramma](assets/diagram3.png)

Di seguito sono riportati i dettagli relativi a questi passaggi:

* **Dati di input**: È identico ai metodi di filtro collaborativo (CF) per elemento. [!UICONTROL Entrambi Consigliati] e gli algoritmi basati su carrello utilizzano i dati comportamentali, sotto forma di visualizzazioni e acquisti di utenti raccolti quando [implementare Target](/help/c-recommendations/plan-implement.md#pass-behavioral) o [Adobe Analytics](/help/c-recommendations/c-algorithms/use-adobe-analytics-with-recommendations.md).

* **Formazione modello**:

   * **Pulizia e campionamento dei dati**: Anche in questo caso si tratta dei metodi di filtro collaborativo, in cui l’intervallo di lookback viene applicato per filtrare i dati comportamentali in base a un intervallo di date appropriato, seguiti dall’applicazione delle regole di catalogo ed esclusioni globali. I visitatori che hanno interagito con più di 1.000 elementi hanno preso in considerazione solo i più recenti 1.000 utilizzi.
   * **Divisione della prova del treno**: Effettua una suddivisione cronologica degli utilizzi per ogni utente, assegnando il primo 80% dei loro utilizzi ai dati di formazione, con il restante 20% assegnato ai dati di test.
   * **Formazione sul modello per similarità degli articoli**: Il calcolo della somiglianza dell&#39;elemento di base è diverso per [!UICONTROL Consigliato] algoritmi basati su carrello nel modo in cui vengono costruiti i vettori dell&#39;elemento candidato. Per [!UICONTROL Consigliato], i vettori di elementi hanno NUser di dimensione, in cui ogni voce rappresenta la somma delle valutazioni implicite per l’utente dell’elemento. Agli acquisti di un elemento viene assegnato un peso pari a 2 volte quello delle visualizzazioni dell’elemento. Per i consigli basati su carrello, i vettori di elementi hanno voci binarie; se il comportamento all’interno della sessione deve essere considerato solo, esiste una nuova voce per ogni sessione. In caso contrario, esiste una voce in questo vettore di elementi per ogni visitatore.

   La fase di formazione calcola diversi tipi di somiglianze vettoriali: Somiglianza LLR ([discusso qui](/help/c-recommendations/c-algorithms/assets/log-likelihood-ratios-recommendation-algorithms.pdf)), somiglianza del coseno (definita in precedenza) e similarità L2 normalizzata, definita come:

   ![Formula](assets/formula4.png)

   * **Valutazione modello similarità articolo**: La valutazione del modello viene effettuata prendendo le raccomandazioni generate nel passaggio precedente e facendo previsioni sul set di dati del test. La fase di punteggio online viene imitata ordinando cronologicamente gli utilizzi degli elementi di ogni utente nel set di dati di test, quindi formulando 100 raccomandazioni per i sottoinsiemi ordinati di elementi nel tentativo di prevedere visualizzazioni e acquisti successivi. Una metrica di recupero informazioni, la [Precisione media media media media](https://en.wikipedia.org/wiki/Evaluation_measures_(information_retrieval)#Mean_average_precision)), viene utilizzato per valutare la qualità di queste raccomandazioni. Questa metrica tiene conto dell’ordine dei consigli e favorisce gli elementi rilevanti più in alto nell’elenco dei consigli, una proprietà importante per i sistemi di classificazione.
   * **Selezione del modello**: Dopo la valutazione offline, viene selezionato il modello con la precisione media media più elevata e vengono calcolati tutti i consigli relativi ai singoli elementi.
   * **Filtro offline**: La fase finale della formazione del modello è l&#39;applicazione di eventuali filtri dinamici applicabili. Dopo questo passaggio, i consigli precalcolati vengono memorizzati nella cache globale per essere disponibili per il servizio.


* **Servizio del modello**: A differenza degli algoritmi precedenti in cui il servizio delle raccomandazioni comporta la specifica di una singola chiave per il recupero, seguita dall&#39;applicazione di regole di business, il [!UICONTROL Consigliato per te] e gli algoritmi basati su carrello utilizzano un processo di runtime più complesso.

   * **Recupero e unione di più chiavi**: Per i consigli basati su carrello, fino a dieci elementi passati nel carrello vengono considerati chiavi per il recupero e i consigli di ciascuno di essi sono ponderati in modo uniforme. Per [!UICONTROL Consigliato per te], fino agli ultimi cinque elementi visualizzati univoci e gli ultimi cinque elementi acquistati unici sono considerati chiavi per il recupero, con i consigli derivanti da articoli acquistati ponderati due volte tanto quanto i consigli derivanti dagli elementi visualizzati. Durante l’unione dei consigli, se un elemento viene visualizzato in più elenchi individuali di consigli, vengono aggiunti i relativi punteggi di somiglianza ponderati. L’elenco finale delle raccomandazioni in questa fase è l’elenco combinato delle raccomandazioni riponderate, ordinate in ordine decrescente.
   * **Filtro**: Vengono quindi applicate regole di filtro come la rimozione degli elementi visualizzati e/o acquistati in precedenza e altre regole di business dinamiche.

Questi processi sono illustrati nell’immagine seguente, in cui un visitatore ha visualizzato l’articolo A e l’articolo B acquistato. I singoli consigli vengono recuperati con i punteggi di similarità offline visualizzati sotto ogni etichetta di articolo. Dopo il recupero, i consigli vengono uniti con punteggi di somiglianza ponderati sommati. Infine, in uno scenario in cui il cliente ha specificato che gli articoli visualizzati e acquistati in precedenza devono essere filtrati, il passaggio di filtro rimuove gli elementi A e B dall’elenco dei consigli.

![Diagramma](assets/diagram4.png)

## Basato sulla popolarità

Gli algoritmi includono:

* [!UICONTROL Più visualizzati nel sito]
* [!UICONTROL Più visualizzate per categoria]
* [!UICONTROL Più visualizzato per attributo articolo]
* [!UICONTROL Articoli più venduti in tutto il sito]
* [!UICONTROL Più venduti per categoria]
* [!UICONTROL Principali venduti per attributo articolo]

[!DNL Target] fornisce algoritmi basati sulla popolarità sia per gli elementi più visualizzati, sia per gli elementi più venduti in un sito web, o suddivisi per un attributo di articolo o una categoria. Gli algoritmi basati sulla popolarità classificano gli elementi in base al numero di sessioni in cui l’elemento è stato visualizzato o acquistato in un determinato intervallo di tempo.

Tutti questi algoritmi combinano dati comportamentali aggregati in cui il numero totale di sessioni in cui gli elementi sono stati visualizzati e acquistati viene registrato a risoluzioni sia orarie che giornaliere. I singoli algoritmi individuano quindi gli elementi più visualizzati o più acquistati per l’intervallo di lookback configurato dal cliente.

Le singole sfumature dell’algoritmo sono le seguenti:

* [!UICONTROL Più visualizzati nel sito] e [!UICONTROL Articoli più venduti in tutto il sito] classifica gli elementi in base al numero aggregato di sessioni in cui questi elementi sono stati visualizzati o acquistati rispettivamente. L’output è un singolo elenco (senza chiave) di elementi consigliati.
* La maggior parte dei venditori visualizzati/più venduti per attributo categoria/elemento sono raccomandazioni in cui gli articoli sono ordinati dal numero aggregato di sessioni in cui questi articoli sono stati visualizzati o acquistati, ma raggruppati per la categoria di articoli o l&#39;attributo specifico dell&#39;articolo. Gli output sono elenchi di elementi consigliati, basati su valori di categorie o valori di attributi di elementi.

## Visualizzato di recente

L’algoritmo di raccomandazioni &quot;visualizzate di recente&quot; consente la personalizzazione in sessione dei consigli. Questo algoritmo non richiede una &quot;formazione modello&quot; offline. Invece, [!DNL Target] utilizza l&#39;univoco [Profilo visitatore](/help/c-target/c-visitor-profile/visitor-profile.md) per mantenere un elenco in esecuzione degli elementi visualizzati in una determinata sessione e in grado di includerli nelle attività di consigli. Questo consente aggiornamenti in tempo reale ai consigli e alla personalizzazione della pagina successiva.

## Criteri personalizzati

I criteri personalizzati consentono ai clienti di [caricare i propri consigli in [!DNL Target]](/help/c-recommendations/c-algorithms/recommendations-csv.md), offrendo un&#39;importante flessibilità e consentendo di realizzare il proprio modello. I criteri personalizzati sostituiscono la parte &quot;formazione offline&quot; di [!UICONTROL Basato su articolo] i consigli, ma si comportano in modo simile agli algoritmi basati su elementi durante la fase di distribuzione dei contenuti online, in quanto viene quindi applicata una singola chiave per il recupero dei consigli e delle regole/filtri aziendali.