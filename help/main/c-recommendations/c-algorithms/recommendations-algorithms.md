---
keywords: algoritmi consigli;formazione modello;server modelli;distribuzione contenuti;basato su elementi;basato su utenti;basato su popolarità;basato su carrello;criteri personalizzati;recommendations algorithms;model training;model serving;content delivery;item-based;user-based;popularity-based;cart-based;custom criteria
description: Scopri gli algoritmi utilizzati in [!DNL Target Recommendations], tra cui formazione su modelli e servizi di assistenza su modelli.
title: Dove posso scoprire la scienza alla base degli algoritmi Recommendations di Target?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
mini-toc-levels: 2
exl-id: c156952b-8eda-491d-a68e-d3d09846f640
source-git-commit: 2a25fdb42ce4470f9126b7e0e7f6fd9e60c350e5
workflow-type: tm+mt
source-wordcount: '2842'
ht-degree: 1%

---

# La scienza alla base degli algoritmi di Recommendations di Target

Una descrizione dettagliata degli algoritmi utilizzati in [!DNL Adobe Target Recommendations], compresi i dettagli logici e matematici dell&#39;addestramento al modello e del processo di modellazione.

L’apprendimento del modello è il processo con cui i consigli vengono generati dal [!DNL Adobe Target] algoritmi di apprendimento. Model serving: come [!DNL Target] fornisce consigli ai visitatori del sito (noti anche come consegna dei contenuti).

[!DNL Target] include i seguenti tipi generali di algoritmi in [!DNL Recommendations]:

* **Algoritmi basati su elementi**: includi algoritmi che seguono la logica &quot;Chi ha visualizzato/acquistato questo oggetto ha anche visualizzato/acquistato questi elementi&quot;. Questi algoritmi sono raggruppati sotto il termine generale &quot;item-item&quot; (filtraggio collaborativo elemento-elemento), così come [!UICONTROL Articoli con attributi simili] algoritmi.

* **Algoritmi basati sugli utenti**: Includi [!UICONTROL Visualizzato di recente] e [!UICONTROL Consigliato per te] algoritmi.

* **Algoritmi basati sulla popolarità**: include algoritmi che restituiscono gli articoli più visualizzati o acquistati in tutto il sito web, oppure più visualizzati o acquistati per categoria o attributo di articolo.

* **Algoritmi basati su carrello**: includi consigli basati su più elementi con la logica &quot;persone che hanno visualizzato/acquistato questi elementi, hanno anche visualizzato/acquistato tali elementi&quot;.

* **Criteri personalizzati**: include consigli basati su file personalizzati caricati in [!DNL Target].

>[!NOTE]
>
>Per informazioni più generali su ciascun tipo di algoritmo e sui singoli algoritmi, consulta [Basare il consiglio su una chiave consiglio](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md).

Molti degli algoritmi elencati sopra sono basati sulla presenza di una o più chiavi. Queste chiavi vengono utilizzate per recuperare elementi simili al momento della consegna del contenuto (quando vengono creati i consigli). Le chiavi specificate dal cliente possono includere l’articolo corrente che un utente sta visualizzando, l’ultimo articolo visualizzato o acquistato, l’articolo più visualizzato, la categoria corrente o la categoria preferita per quel visitatore. Altri algoritmi, come i consigli basati su carrello o su utente, utilizzano chiavi implicite (che il cliente non può configurare). Per ulteriori informazioni, consulta *Chiavi consiglio*, in [Basare il consiglio su una chiave consiglio](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#keys). Tieni presente, tuttavia, che queste chiavi sono rilevanti solo al momento della distribuzione del modello (consegna dei contenuti). Queste chiavi non influiscono sulla logica dei tempi di apprendimento &quot;offline&quot; o del modello.

Le sezioni seguenti raggruppano gli algoritmi in modo leggermente diverso rispetto ai tipi di algoritmo descritti in precedenza. Il seguente raggruppamento si basa sulla somiglianza della logica di apprendimento del modello.

## Filtro collaborativo elemento-elemento

Gli algoritmi includono:

* [!UICONTROL Chi ha visualizzato questo ha visualizzato anche quello]
* [!UICONTROL Chi ha visualizzato questo ha acquistato anche quello]
* [!UICONTROL Chi ha comprato questo ha acquistato anche quello]

Gli algoritmi per la generazione di consigli con filtro collaborativo elemento-elemento si basano sull’idea che si debbano utilizzare i modelli comportamentali di molti utenti (quindi collaborativi) per fornire consigli utili per un dato elemento (ad esempio, filtrare il catalogo di possibili elementi da consigliare). Anche se ci sono molti algoritmi diversi che rientrano sotto l&#39;ombrello generale di [filtro collaborativo](https://en.wikipedia.org/wiki/Collaborative_filtering), questi algoritmi utilizzano universalmente origini di dati comportamentali come input. In entrata [!DNL Target Recommendations], questi input sono le visualizzazioni e gli acquisti univoci di articoli da parte degli utenti.

Per l’algoritmo &quot;chi ha visualizzato/acquistato questo articolo ha anche visualizzato/acquistato questi articoli&quot;, l’obiettivo è calcolare una somiglianza s(A,B) tra tutte le coppie di articoli. Per un dato articolo A, i consigli principali sono quindi ordinati in base alle somiglianze (A,B).

Un esempio di tale somiglianza è la co-occorrenza tra gli articoli: un conteggio semplice del numero di utenti che hanno acquistato entrambi gli articoli. Anche se intuitiva, tale metrica è ingenua in quanto tende a consigliare articoli popolari. Ad esempio, se presso un rivenditore di alimentari la maggior parte delle persone acquista il pane, il pane avrà un&#39;elevata co-occorrenza con tutti gli articoli, ma non è necessariamente una buona raccomandazione. [!DNL Target] utilizza invece una metrica di somiglianza più sofisticata nota come log likelihood ratio (LLR). Questa quantità è grande quando la probabilità che due articoli, A e B, si verifichino contemporaneamente è molto diversa dalla probabilità che non si verifichino contemporaneamente. Per concretezza, considera un caso di [!UICONTROL Chi ha visualizzato questo ha acquistato anche quello] algoritmo. La somiglianza LLR è grande quando la probabilità che B sia stato acquistato è *non* indipendentemente dal fatto che qualcuno abbia visualizzato O.

Ad esempio, se

![Formula per l’algoritmo visualizzato/acquistato](assets/formula.png)

l’elemento B non deve essere consigliato con l’elemento A. Vengono forniti i dettagli completi di questo calcolo di similarità del rapporto di probabilità del registro [in questo PDF](/help/main/c-recommendations/c-algorithms/assets/log-likelihood-ratios-recommendation-algorithms.pdf).

Il flusso logico dell’implementazione effettiva dell’algoritmo è mostrato nel diagramma schematico seguente:

![Diagramma schematico di un algoritmo visualizzato/acquistato](assets/diagram1.png)

Di seguito sono riportati i dettagli di questi passaggi:

* **Dati di input**: dati comportamentali, sotto forma di visualizzazioni e acquisti di visitatori raccolti quando [implementare Target](https://experienceleague.corp.adobe.com/docs/target-dev/developer/recommendations.html?lang=it){target=_blank} or from [Adobe Analytics](/help/main/c-recommendations/c-algorithms/use-adobe-analytics-with-recommendations.md){target=_blank}.

* **Formazione sui modelli**:

   * **Pulizia dei dati e campionamento**: per gli algoritmi con un lookback di N giorni, i dati comportamentali vengono prima filtrati per includere solo tali N giorni di dati. Le regole di raccolta e le esclusioni globali vengono quindi applicate per rimuovere tutti gli elementi che non devono essere consigliati. Infine, per i visitatori che hanno interagito con più di 1.000 elementi, i dati di utilizzo sono stati campionati in soli 1.000 elementi.
   * **Calcolo per somiglianza elemento**: questo è il passaggio di calcolo principale: calcolo della somiglianza del rapporto di probabilità del registro tra tutte le coppie di elementi candidati e classificazione delle coppie di elementi in base a questo punteggio di somiglianza.
   * **Filtro offline**: vengono infine applicati eventuali altri filtri dinamici applicabili (ad esempio, esclusioni di categorie dinamiche). Dopo questo passaggio, i consigli precalcolati vengono memorizzati nella cache a livello globale per essere disponibili per il servizio.

* **Model serving**: il contenuto Recommendations viene distribuito da [!DNL Target]di [rete globale &quot;Edge&quot;](/help/main/c-intro/how-target-works.md#concept_0AE2ED8E9DE64288A8B30FCBF1040934). Quando vengono effettuate richieste mbox a [!DNL Target] ed è determinato che il contenuto dei consigli deve essere consegnato alla pagina, la richiesta dell’appropriata [chiave elemento](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#keys) per l’algoritmo Recommendations viene analizzato dalla richiesta o cercato dal profilo utente, e quindi utilizzato per recuperare i consigli calcolati nei passaggi precedenti. Ulteriori filtri dinamici vengono applicati in questo momento, prima dell’appropriato [progettazione](/help/main/c-recommendations/c-design-overview/create-design.md) è sottoposto a rendering.

## Somiglianza dei contenuti

Algoritmo incluso:

* [!UICONTROL Articoli con attributi simili]

In questo tipo di algoritmo, due elementi sono considerati correlati se i loro nomi e le descrizioni testuali sono semanticamente simili. A differenza della maggior parte degli algoritmi di consigli in cui devono essere utilizzate origini di dati comportamentali, gli algoritmi di somiglianza dei contenuti utilizzano metadati dei cataloghi di prodotti per derivare la somiglianza tra gli elementi. [!DNL Target] è quindi in grado di indirizzare le raccomandazioni in scenari cosiddetti di &quot;avviamento a freddo&quot;, in cui non sono stati raccolti dati comportamentali (ad esempio, all’inizio di un’ [!DNL Target] attività).

Anche se gli aspetti relativi alla distribuzione dei modelli e dei contenuti di [!DNL Target]gli algoritmi di somiglianza dei contenuti di sono identici ad altri algoritmi basati su elementi, i passaggi di formazione del modello sono drasticamente diversi e coinvolgono una serie di fasi di elaborazione e pre-elaborazione del linguaggio naturale, come illustrato nel diagramma seguente. Il nucleo del calcolo della somiglianza è l&#39;uso della somiglianza coseno dei vettori tf-idf modificati che rappresentano ogni elemento del catalogo.

![Diagramma che mostra il flusso del processo di somiglianza dei contenuti](assets/diagram2.png)

Di seguito sono riportati i dettagli di questi passaggi:

* **Dati di input**: come descritto in precedenza, questo algoritmo si basa esclusivamente sui dati di catalogo (acquisiti in [!DNL Target] tramite un [Feed di catalogo, API di entità o da aggiornamenti su pagina](https://experienceleague.corp.adobe.com/docs/target-dev/developer/recommendations.html?lang=it){target=_blank}.

* **Formazione sui modelli**:

   * **Estrazione attributo**: dopo l’applicazione di filtri statici regolari, regole di catalogo ed esclusioni globali, questo algoritmo estrae campi testuali rilevanti dallo schema di entità. [!DNL Target] utilizza automaticamente i campi nome, messaggio e categoria dagli attributi di entità e tenta di estrarre qualsiasi campo stringa da personalizzato [attributi di entità](/help/main/c-recommendations/c-products/entity-attributes.md). Questo processo viene eseguito assicurandosi che la maggior parte dei valori per quel campo non sia analizzabile come numero, data o booleano.
   * **Stemming e rimozione di parole non significative**: per una corrispondenza più accurata della somiglianza del testo, è prudente rimuovere le parole &quot;stop&quot; molto comuni che non alterano in modo significativo il significato di un elemento (ad esempio, &quot;era&quot;, &quot;è&quot;, &quot;e&quot;, &quot;e così via). Allo stesso modo, il termine stemming si riferisce al processo di riduzione delle parole con suffissi diversi alla loro parola principale, che ha un significato identico (ad esempio, &quot;connect&quot;, &quot;connect&quot; e &quot;connection&quot; hanno tutti la stessa parola principale: &quot;connect&quot;). [!DNL Target] usa lo stemmer Snowball. [!DNL Target] esegue prima il rilevamento automatico della lingua e può interrompere la rimozione delle parole per un massimo di 50 lingue e la creazione di stemming per 18 lingue.
   * **creazione n-grammi**: dopo i passaggi precedenti, ogni parola viene trattata come un token. Il processo di combinazione di sequenze contigue di token in un singolo token è definito creazione di n grammi. [!DNL Target]Gli algoritmi di considerano fino a 2 grammi.
   * **calcolo tf-idf**: il passaggio successivo prevede la creazione di vettori tf-idf per riflettere l’importanza relativa dei token nella descrizione dell’elemento. Per ogni token/termine t in un elemento i, in un catalogo D con |D| elementi, il termine frequenza TF(t, i) viene calcolato per primo (il numero di volte che il termine appare nella voce i), nonché la frequenza del documento DF(t, D). In sostanza, il numero di elementi in cui esiste il token. La misura tf-idf è quindi

      ![Formula che mostra la misura tf-idf](assets/formula2.png)

      [!DNL Target] utilizza Apache Spark *tf-idf* implementazione di funzionalità, che fornisce l’hash di ogni token su uno spazio di 218 token. In questo passaggio, vengono applicati anche il potenziamento degli attributi specificati dal cliente, regolando le frequenze dei termini in ciascun vettore in base alle impostazioni specificate nella [criteri](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#similarity).

   * **Calcolo per somiglianza elemento**: il calcolo della somiglianza dell’elemento finale viene eseguito utilizzando una somiglianza approssimativa con il coseno. Per due voci, *A* e *B*, con i vettori tA e tB, la somiglianza coseno è definita come:

      ![Formula che mostra il calcolo della somiglianza dell&#39;articolo](assets/formula3.png)

      Per evitare complessità significative nel calcolo delle somiglianze tra tutti gli elementi N x N, *tf-idf* il vettore è troncato per contenere solo le sue 500 voci più grandi, e quindi calcolare le somiglianze coseno tra gli elementi utilizzando questa rappresentazione vettoriale troncata. Questo approccio si dimostra più robusto per i calcoli di somiglianza vettoriale sparsa, rispetto ad altre tecniche approssimate più vicine (ANN), come l&#39;hashing sensibile alla località.

   * **Model serving**: questo processo è identico alle tecniche di filtro collaborativo elemento-elemento descritte nella sezione precedente.

## Consigli multichiave

Gli algoritmi includono:

* Consigli basati su carrello
* [!UICONTROL Consigliato per te]

Le ultime aggiunte al [!DNL Target] La suite di algoritmi di Recommendations è [!UICONTROL Consigliato per te] e una serie di algoritmi di raccomandazioni basati sul carrello. Entrambi i tipi di algoritmi utilizzano tecniche di filtro collaborativo per formare singoli consigli basati su elementi. Quindi, al momento del server, più elementi nella cronologia di navigazione dell’utente (per [!UICONTROL Consigliato per te]), o il carrello corrente dell’utente (per i consigli basati su carrello) vengono utilizzati per recuperare questi consigli basati su elementi, che vengono quindi uniti per formare l’elenco finale dei consigli. Tieni presente che esistono molti aromi di algoritmi di consigli personalizzati. La scelta di un algoritmo multi-chiave significa che i consigli sono immediatamente disponibili dopo che un visitatore ha una cronologia di navigazione e che possono essere aggiornati per rispondere al comportamento del visitatore più recente.

Questi algoritmi si basano sulle tecniche di filtraggio collaborativo fondamentale descritte nella sezione Consigli basati su elementi, ma incorporano anche la regolazione hyperparameter per determinare la metrica di somiglianza ottimale tra gli elementi. L’algoritmo esegue una suddivisione cronologica dei dati comportamentali per ogni utente e forma modelli di consigli sui dati precedenti durante il tentativo di prevedere gli elementi che un utente visualizzerà o acquisterà in un secondo momento. La metrica di somiglianza che produce il risultato ottimale [Precisione media](Viene quindi scelto https://en.wikipedia.org/wiki/Evaluation_measures_(information_retrieval).

La logica dei passaggi di apprendimento del modello e del punteggio è illustrata nel diagramma seguente:

![Diagramma che mostra la logica dei passaggi di apprendimento del modello e del punteggio](assets/diagram3.png)

Di seguito sono riportati i dettagli di questi passaggi:

* **Dati di input**: è identico ai metodi di filtro collaborativo elemento-elemento (CF). [!UICONTROL Entrambi Consigliati Per Te] e gli algoritmi basati sul carrello utilizzano dati comportamentali, sotto forma di visualizzazioni e acquisti di utenti raccolti quando [implementare Target](https://experienceleague.corp.adobe.com/docs/target-dev/developer/recommendations.html?lang=it){target=_blank} or from [Adobe Analytics](/help/main/c-recommendations/c-algorithms/use-adobe-analytics-with-recommendations.md){target=_blank}.

* **Formazione sui modelli**:

   * **Pulizia dei dati e campionamento**: questo è nuovamente lo stesso dei metodi di filtro collaborativi, in cui l’intervallo di lookback viene applicato per filtrare i dati comportamentali in un intervallo di date appropriato, seguito dall’applicazione di regole di catalogo ed esclusioni globali. I visitatori che hanno interagito con più di 1.000 elementi vengono considerati solo i 1.000 utilizzi più recenti.
   * **Divisione di prova del treno**: esegui una suddivisione cronologica degli utilizzi per ogni utente, allocando il primo 80% dei suoi utilizzi ai dati di addestramento, con il restante 20% assegnato ai dati di test.
   * **Formazione per modello similarità articolo**: il calcolo della somiglianza dell’elemento core è diverso per [!UICONTROL Consigliato per te] e algoritmi basati su carrello nel modo in cui vengono costruiti i vettori degli elementi candidati. Per [!UICONTROL Consigliato per te], i vettori di articolo hanno dimensioni NUser, in cui ogni voce rappresenta la somma delle valutazioni implicite per l’utente dell’articolo. Agli acquisti di un articolo viene assegnato un peso pari al doppio delle visualizzazioni dell’articolo. Per i consigli basati su carrello, i vettori di elementi dispongono di voci binarie; se il comportamento all’interno della sessione deve essere considerato solo, esiste una nuova voce per ogni sessione. In caso contrario, esiste una voce in questo vettore elemento per ogni visitatore.

   Il passaggio di apprendimento calcola diversi tipi di somiglianze vettoriali: LLR similarity ([discussi qui](/help/main/c-recommendations/c-algorithms/assets/log-likelihood-ratios-recommendation-algorithms.pdf)), somiglianza coseno (definita in precedenza) e somiglianza L2 normalizzata, definita come:

   ![Formula che mostra il calcolo dell’addestramento](assets/formula4.png)

   * **Valutazione modello similarità articolo**: la valutazione del modello viene eseguita prendendo i consigli generati nel passaggio precedente e facendo previsioni sul set di dati di test. La fase di punteggio online viene imitata ordinando in modo cronologico gli utilizzi degli articoli di ogni utente nel set di dati di test, quindi eseguendo 100 consigli per sottoinsiemi di articoli ordinati nel tentativo di prevedere visualizzazioni e acquisti successivi. Una metrica di recupero delle informazioni, la [Precisione media](https://en.wikipedia.org/wiki/Evaluation_measures_(information_retrieval), viene utilizzato per valutare la qualità di questi consigli. Questa metrica prende in considerazione l’ordine dei consigli e favorisce gli elementi pertinenti più in alto nell’elenco dei consigli, che è una proprietà importante per i sistemi di classificazione.
   * **Selezione modello**: dopo la valutazione offline, viene selezionato il modello con la precisione media più elevata e vengono calcolati tutti i singoli consigli articolo-articolo.
   * **Filtro offline**: la fase finale dell’apprendimento del modello consiste nell’applicazione di eventuali filtri dinamici applicabili. Dopo questo passaggio, i consigli precalcolati vengono memorizzati nella cache a livello globale per essere disponibili per il servizio.


* **Model serving**: a differenza dei precedenti algoritmi in cui i consigli richiedono di specificare una singola chiave per il recupero, seguita dall’applicazione di regole di business, il [!UICONTROL Consigliato per te] Gli algoritmi basati su carrello utilizzano un processo di runtime più complesso.

   * **Recupero e unione di più chiavi**: per i consigli basati sul carrello, fino a dieci elementi passati nel carrello vengono considerati chiavi per il recupero e i consigli di ciascuno di essi vengono ponderati in modo uniforme. Per [!UICONTROL Consigliato per te], fino agli ultimi cinque articoli visualizzati e gli ultimi cinque articoli acquistati univoci vengono considerati chiavi per il recupero; i consigli derivanti dagli articoli acquistati vengono ponderati due volte rispetto ai consigli derivanti dagli articoli visualizzati. Quando si uniscono i consigli, se un elemento viene visualizzato in più elenchi di consigli singoli, vengono aggiunti i punteggi di somiglianza ponderati. L’elenco finale dei consigli in questa fase è quindi l’elenco unito dei consigli riponderati, ordinati in ordine decrescente.
   * **Filtraggio**: vengono quindi applicate le regole di filtro, ad esempio la rimozione degli articoli visualizzati e/o acquistati in precedenza, e altre regole aziendali dinamiche.

Questi processi sono illustrati nell’immagine seguente, dove un visitatore ha visualizzato l’articolo A e ha acquistato l’articolo B. I singoli consigli vengono recuperati con i punteggi di somiglianza offline riportati sotto l’etichetta di ciascun articolo. Dopo il recupero, i consigli vengono uniti con la somma dei punteggi di somiglianza ponderati. Infine, in uno scenario in cui il cliente ha specificato che gli articoli visualizzati e acquistati in precedenza devono essere esclusi dal filtro, il passaggio di filtro rimuove gli articoli A e B dall’elenco dei consigli.

![Diagramma che mostra l’elaborazione degli algoritmi a più chiavi](assets/diagram4.png)

## Basato sulla popolarità

Gli algoritmi includono:

* [!UICONTROL Articoli più visualizzati nel sito]
* [!UICONTROL Più visualizzati per categoria]
* [!UICONTROL Più visualizzati per attributo articolo]
* [!UICONTROL Articoli più venduti in tutto il sito]
* [!UICONTROL Articoli più venduti per categoria]
* [!UICONTROL Attributo Articoli più venduti]

[!DNL Target] fornisce algoritmi basati sulla popolarità sia per gli articoli più visualizzati che per quelli più venduti su un sito web o suddivisi per un attributo o una categoria di articoli. Gli algoritmi basati sulla popolarità classificano gli elementi in base al numero di sessioni in cui l’elemento è stato visualizzato o acquistato in un determinato intervallo di tempo.

Tutti questi algoritmi combinano dati comportamentali aggregati in cui il numero totale di sessioni in cui gli elementi sono stati visualizzati e acquistati viene registrato sia con risoluzione oraria che giornaliera. I singoli algoritmi individuano quindi gli articoli più visualizzati o acquistati per l’intervallo di lookback configurato dal cliente.

Le singole sfumature dell’algoritmo sono le seguenti:

* [!UICONTROL Articoli più visualizzati nel sito] e [!UICONTROL Articoli più venduti in tutto il sito] classifica gli articoli in base al numero aggregato di sessioni in cui questi articoli sono stati rispettivamente visualizzati o acquistati. L’output è un singolo elenco (senza chiave) di elementi consigliati.
* Più visualizzati/Articoli più venduti per categoria/attributo articolo sono consigli in cui gli articoli vengono ordinati in base ai conteggi aggregati delle sessioni in cui tali articoli sono stati visualizzati o acquistati, ma raggruppati per categoria articolo o attributo articolo specifico. Gli output sono elenchi di articoli consigliati, in base ai valori delle categorie o ai valori degli attributi degli articoli.

## Visualizzato di recente

L’algoritmo per consigli &quot;visualizzato di recente&quot; consente la personalizzazione dei consigli nella sessione. Questo algoritmo non richiede alcun &quot;apprendimento del modello&quot; offline. Invece, [!DNL Target] utilizza il codice univoco [Profilo visitatore](/help/main/c-target/c-visitor-profile/visitor-profile.md) per mantenere in esecuzione un elenco di elementi che sono stati visualizzati in una determinata sessione e che possono far emergere questi elementi nelle attività di consigli. Questo consente di aggiornare in tempo reale i consigli e la personalizzazione della pagina successiva.

## Criteri personalizzati

I criteri personalizzati consentono ai clienti di: [caricare i propri consigli in [!DNL Target]](/help/main/c-recommendations/c-algorithms/recommendations-csv.md), offrendo una flessibilità importante e consentendo funzionalità personalizzate. I criteri personalizzati sostituiscono la sezione &quot;apprendimento offline&quot; di [!UICONTROL Basato su articolo] i consigli, ma si comportano in modo simile agli algoritmi di consigli basati su elementi durante la fase di distribuzione dei contenuti online, in quanto viene utilizzata un’unica chiave per recuperare i consigli e vengono quindi applicati regole/filtri di business.
