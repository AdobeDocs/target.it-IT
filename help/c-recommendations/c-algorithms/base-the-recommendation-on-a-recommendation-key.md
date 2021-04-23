---
keywords: chiave di consiglio;logica di consiglio;categoria corrente;attributo personalizzato;ultimo articolo acquistato;ultimo articolo visualizzato;articolo più visualizzato;articolo più visualizzato;articolo più visualizzato;categoria preferita;popolarità;articolo visualizzato di recente;ultimo articolo acquistato;ultimo visualizzato;più visualizzato;preferito;visualizzato di recente
description: Scopri come utilizzare i consigli basati sulle chiavi che utilizzano il contesto di comportamento del visitatore per mostrare i risultati rilevanti nelle attività di Adobe [!DNL Target] Recommendations.
title: Come posso basare il consiglio su una Chiave consiglio?
feature: Consigli
mini-toc-levels: 2
exl-id: 49764f18-88fb-41be-b2a0-e7ced9de742c
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '2932'
ht-degree: 67%

---

# Basare il consiglio su una chiave consiglio

Recommendations basato sulle chiavi utilizza il contesto del comportamento del visitatore per mostrare i risultati rilevanti nelle attività [!DNL Adobe Target] [!DNL Recommendations] .

Esistono due tipi di consigli:

* **Popolarità:** elenca gli elementi in base ai più visualizzati, i più venduti, e alla metrica migliore. La chiave dei criteri di popolarità è vuota.
* **Basato su chiave:** comprende il resto dei criteri. I consigli offrono una serie diversificata di scelte per quanto riguarda il tipo di chiave. Le opzioni variano da “elemento corrente” a “parametri profilo” e consentono di impostare la chiave dei valori da consigliare in modo sistematico. È possibile sottoporre a test più criteri confrontandoli uno con l&#39;altro e basando ogni criterio su una chiave diversa.

Ogni criterio è definito nella relativa scheda. Il traffico è suddiviso in modo uniforme tra i diversi test di criteri. In altre parole, in presenza di due criteri, il traffico viene suddiviso in modo uniforme tra di essi. In presenza di due criteri e di due progettazioni, il traffico viene suddiviso in modo uniforme tra le quattro combinazioni. Puoi inoltre specificare una percentuale di visitatori del sito che visualizzano il contenuto predefinito, a scopo di confronto. In tal caso, la percentuale specificata di visitatori visualizza il contenuto predefinito e gli altri sono suddivisi tra i criteri e le combinazioni di progettazione.

1. Crea un nuovo criterio o seleziona un criterio esistente e fai clic su **[!UICONTROL Modifica]**.
1. Per modificare la chiave di raccomandazione, seleziona la nuova chiave dall&#39;elenco a discesa [!UICONTROL Chiave consiglio] , quindi fai clic su **[!UICONTROL Salva]** o **[!UICONTROL Aggiorna]**.

   Poiché diverse logiche sono associate a diverse chiavi di consigli, diversi consigli si prestano a posizionarsi su diversi tipi di pagine. Per ulteriori informazioni su ciascuna chiave di raccomandazione, consulta le sezioni seguenti.

## Chiavi dei consigli

Le seguenti chiavi di raccomandazione sono disponibili dall&#39;elenco a discesa [!UICONTROL Chiave consiglio] :

### Elemento corrente {#current-item}

Il consiglio è determinato dall&#39;elemento attualmente visualizzato dal visitatore.

Il consiglio visualizzano altri elementi che potrebbero interessare i visitatori interessati all&#39;elemento specificato.

Quando questa opzione è selezionata, il valore `entity.id` deve essere trasmesso come parametro alla mbox di visualizzazione.

#### Logica (criteri)

* [!UICONTROL Articoli con attributi simili]
* [!UICONTROL Chi ha visualizzato questo ha visualizzato anche quello]
* [!UICONTROL Chi ha visualizzato questo ha acquistato anche quello]
* [!UICONTROL Chi ha comprato questo ha acquistato anche quello]
* [!UICONTROL Affinità sito]

#### Dove utilizzare nel sito

* Pagine a elemento singolo, ad esempio le pagine del prodotto.
* NON utilizzare nelle pagine dei risultati di ricerca nulli.

### Categoria corrente {#current-category}

Il consiglio è determinato dalla categoria di prodotto attualmente visualizzata dal visitatore.

I consigli mostrano gli elementi nella categoria di prodotto specificata.

Quando questa opzione è selezionata, il valore `entity.categoryId` deve essere trasmesso come parametro alla mbox di visualizzazione.

#### Logica (criteri)

* Articoli più venduti
* Articoli più visualizzati

#### Dove utilizzare nel sito

* Pagine a categoria singola.
* NON utilizzare nelle pagine dei risultati di ricerca nulli.

### Attributo personalizzato  {#custom}

Il consiglio è determinato da un elemento memorizzato nel profilo di un visitatore, utilizzando uno degli utenti.*x* o profilo.Attributi *x*.

Quando questa opzione è selezionata, il valore `entity.id` deve essere presente nell&#39;attributo profilo.

Quando basi i consigli su attributi personalizzati, seleziona l&#39;attributo personalizzato, quindi il tipo di consiglio.

Puoi eseguire il filtro in tempo reale all&#39;inizio dell&#39;output di criteri personalizzati. Ad esempio, puoi limitare gli articoli consigliati a quelli della categoria o del marchio preferito dal visitatore. Così puoi combinare calcoli offline e filtri in tempo reale.

Grazie a questa funzionalità è possibile utilizzare [!DNL Target] per aggiungere la personalizzazione ai consigli calcolati offline o agli elenchi personalizzati. Permette infatti di unire le compenze del personale addetto ai dati alle tecnonologie comprovate di Adobe per la distribuzione, l&#39;applicazione di filtri al momento dell&#39;esecuzione, i test A/B, il targeting, la generazione di rapporti, le integrazioni e altro.

Con l’aggiunta delle regole di inclusione ai Criteri personalizzati, i consigli non sono più statici ma diventano dinamici, in base agli interessi del visitatore.

* I criteri personalizzati sono configurabili, come altri criteri nei consigli.
* È possibile utilizzare [raccolte](/help/c-recommendations/c-products/collections.md), [esclusioni](/help/c-recommendations/c-products/exclusions.md) e [inclusioni](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) (incluse le regole speciali per Prezzo e Inventario) proprio come per tutti gli altri criteri.

Eventuali casi di utilizzo includono:

* Vuoi consigliare film da una lista personalizzata, ma solo se il visitatore non li ha già guardati.
* Vuoi eseguire un algoritmo offline e utilizzare i risultati per la definizione dei consigli, ma vuoi anche che vengano sempre esclusi gli articoli non disponibili.
* Vuoi includere solo gli articoli appartenenti alla categoria preferita del visitatore.

#### Logica (criteri)

* [!UICONTROL Chi ha visualizzato questo ha visualizzato anche quello]
* [!UICONTROL Chi ha visualizzato questo ha acquistato anche quello]
* [!UICONTROL Chi ha comprato questo ha acquistato anche quello]
* [!UICONTROL Comportamento globale]
* [!UICONTROL Articoli più visualizzati]
* [!UICONTROL Articoli più venduti]

Se la chiave è un attributo di profilo personalizzato e il tipo di algoritmo è “Elementi più visualizzati o i più venduti”, viene visualizzato un nuovo elenco a discesa denominato “Raggruppa per valore univoco di” che dispone di una lista di attributi di entità noti (ad eccezione di ID, categoria, margine, valore, inventario e ambiente). Questo campo è obbligatorio.

#### Dove utilizzare nel sito

* Può essere utilizzato su qualsiasi pagina.

#### Chiave consiglio personalizzata

Puoi basare i consigli sul valore di un attributo di profilo personalizzato. Ad esempio, supponi di voler visualizzare filmati consigliati in base all’ultimo filmato che un visitatore ha aggiunto alla sua coda.

1. Seleziona l’attributo di profilo personalizzato dall’elenco a discesa **[!UICONTROL Chiave consigliata]** (ad esempio, “Ultimo filmato aggiunto alla watchlist”).
1. Seleziona quindi la **[!UICONTROL Logica consigliata]** (ad esempio “Persone che hanno visualizzato questo, hanno visualizzato anche quello”).

   ![Finestra di dialogo per creare un nuovo criterio](/help/c-recommendations/c-algorithms/assets/create-new-criteria-1.png)

Se l’attributo di profilo personalizzato non corrisponde direttamente a un singolo ID entità, devi spiegare a [!DNL Recommendations] come desideri che avvenga la corrispondenza a un’entità. Ad esempio, supponi di voler visualizzare gli articoli più venduti della marca preferita di un visitatore.

1. Seleziona l’attributo di profilo personalizzato dall’elenco a discesa **[!UICONTROL Chiave consiglio]** (ad esempio, “Marchio preferito”).

1. Quindi seleziona la **[!UICONTROL Logica consigli]** che desideri utilizzare con questa chiave (ad esempio, “Più venduti”).

   Viene visualizzata l’opzione [!UICONTROL Raggruppa per valore univoco di].

1. Seleziona l’attributo di entità che corrisponde alla chiave scelta. In questo caso “Marchio preferito” corrisponde a `entity.brand`.

   [!DNL Recommendations] ora genera un elenco “Più venduti” per ogni marchio e mostra al visitatore l’elenco “Più venduti” appropriato in base al valore memorizzato nell’attributo di profilo Marchio preferito del visitatore.

   ![Finestra di dialogo per creare un nuovo criterio 2](/help/c-recommendations/c-algorithms/assets/create-new-criteria-2.png)

### Categoria preferita {#favorite-category}

Il consiglio è determinato dalla categoria destinataria della maggioranza dell&#39;attività, con lo stesso metodo utilizzato per “articolo più visualizzato”, il punteggio però viene attribuito alle categorie anziché ai prodotti.

Tale metodo si basa sul criterio di attualità/frequenza, che si comporta come segue:

* 10 punti per la prima visualizzazione della categoria
* 5 punti per ogni visualizzazione successiva

Alle categorie visitate per la prima volta sono attribuiti 10 punti. Per le visite successive alla stessa categoria sono attribuiti 5 punti. A ogni visita, viene sottratto 1 punto alle categorie non correnti che sono state visualizzate in precedenza.

Ad esempio, la visualizzazione di “Categoria A” e poi di “Categoria B” in una sessione restituisce come risultato A: 9, B: 10. Se si visualizzano gli stessi elementi nella sessione successiva, i valori cambiano in A: 20, B: 9.

#### Logica (criteri)

* [!UICONTROL Articoli più venduti]
* [!UICONTROL Articoli più visualizzati]

#### Dove utilizzare nel sito

* Pagine generali, come la pagina principale o le pagine di destinazione e gli annunci offsite.

### Ultimo articolo acquistato {#last-purchased}

Il consiglio è determinato in base all&#39;ultimo articolo acquistato da ogni visitatore univoco. Tale dato viene acquisito automaticamente, quindi non è necessario trasmettere alcun valore alla pagina.

#### Logica (criteri)

* [!UICONTROL Articoli con attributi simili]
* [!UICONTROL Chi ha visualizzato questo ha visualizzato anche quello]
* [!UICONTROL Chi ha visualizzato questo ha acquistato anche quello]
* [!UICONTROL Chi ha comprato questo ha acquistato anche quello]
* [!UICONTROL Affinità sito]

#### Dove utilizzare nel sito

* Pagina principale, pagina account, annunci fuori sede.
* NON utilizzare su pagine di prodotti o pagine rilevanti per gli acquisti.

### Ultimo articolo visualizzato  {#last-viewed}

Il consiglio è determinato dall&#39;ultimo articolo visualizzato da ogni visitatore univoco. Tale dato viene acquisito automaticamente, quindi non è necessario trasmettere alcun valore alla pagina.

#### Logica (criteri)

* [!UICONTROL Articoli con attributi simili]
* [!UICONTROL Chi ha visualizzato questo ha visualizzato anche quello]
* [!UICONTROL Chi ha visualizzato questo ha acquistato anche quello]
* [!UICONTROL Chi ha comprato questo ha acquistato anche quello]
* [!UICONTROL Affinità sito]

#### Dove utilizzare nel sito

* Pagina principale, pagina account, annunci fuori sede.
* NON utilizzare su pagine di prodotti o pagine rilevanti per gli acquisti.

### Articolo più visualizzato  {#most-viewed}

Il consiglio è determinata in base all&#39;articolo visualizzato più frequentemente, attraverso lo stesso metodo impiegato per la categoria preferita.

Tale metodo si basa sul criterio di attualità/frequenza, che si comporta come segue:

* 10 punti per la prima visualizzazione del prodotto
* 5 punti per ogni visualizzazione successiva
* Alla fine della sessione tutti i valori vengono divisi per 2

Ad esempio, la visualizzazione di “tavola da surf A” e poi di “tavola da surf B” in una sessione restituisce come risultato A: 10, B: 5. Al termine della sessione, si otterrà A: 5, B: 2,5. Se si visualizzano gli stessi elementi nella sessione successiva, i valori si modificano in A: 15 B: 7,5.

#### Logica (criteri)

* [!UICONTROL Articoli con attributi simili]
* [!UICONTROL Chi ha visualizzato questo ha visualizzato anche quello]
* [!UICONTROL Chi ha visualizzato questo ha acquistato anche quello]
* [!UICONTROL Chi ha comprato questo ha acquistato anche quello]
* [!UICONTROL Affinità sito]

#### Dove utilizzare nel sito

* Pagine generali, come la pagina principale o le pagine di destinazione e gli annunci offsite.

### Popolarità  {#popularity}

Il consiglio è determinata dalla popolarità degli elementi sul sito. Il consiglio di tipo popolarità include gli elementi più venduti e i più visualizzati secondo i dati mbox e, se si utilizza Adobe Analytics, tutte le metriche disponibili nel rapporto del prodotto. Gli elementi vengono classificati in base alla logica del consiglio selezionato.

#### Logica (criteri)

* [!UICONTROL Articoli più venduti]
* [!UICONTROL Articoli più visualizzati]
* Metrica del rapporto del prodotto (se si utilizza Adobe Analytics)

#### Dove utilizzare nel sito

* Pagine generali, come la pagina principale o le pagine di destinazione e gli annunci offsite.

### Articoli visualizzati di recente  {#recently-viewed}

Utilizza la cronologia del visitatore (nell&#39;arco delle sessioni) per presentare gli ultimi elementi *x* visualizzati, in base al numero di posizioni nella progettazione.

Il criterio Articoli visualizzati di recente restituisce risultati specifici per un dato [ambiente](/help/administrating-target/hosts.md). Se due siti appartengono ad ambienti diversi e un visitatore passa da un sito all’altro, ciascun sito mostra solo gli articoli visualizzati di recente per il sito appropriato. Se due siti si trovano nello stesso ambiente e un visitatore passa tra di essi, il visitatore vedrà gli stessi elementi visualizzati di recente per entrambi i siti.

>[!NOTE]
>
>Non è possibile utilizzare i criteri [!UICONTROL Articoli visualizzati di recente] per i consigli di backup.

Puoi filtrare gli articoli o i file multimediali visualizzati di recente in modo che vengano visualizzati solo quelli con uno specifico attributo.

* I criteri “visualizzati di recente” sono configurabili, come altri criteri nei consigli.
* È possibile utilizzare [raccolte](/help/c-recommendations/c-products/collections.md), [esclusioni](/help/c-recommendations/c-products/exclusions.md) e [inclusioni](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) (incluse le regole speciali per Prezzo e Inventario) proprio come per tutti gli altri criteri.

Eventuali casi di utilizzo includono:

Una società multinazionale con più business potrebbe avere un visitatore che visualizza elementi in più proprietà digitali. In questo caso, puoi limitare gli articoli visualizzati di recente al solo sito su cui sono stati visualizzati. Questo impedisce la visualizzazione degli elementi visualizzati di recente sul sito di un&#39;altra proprietà digitale.

#### Dove utilizzare nel sito

* Pagine generali, come la pagina principale o le pagine di destinazione e gli annunci offsite.

>[!NOTE]
>
>[!UICONTROL Articoli visualizzati di recente ] rispetta sia le impostazioni globali di esclusioni sia l’impostazione di raccolta selezionata per l’attività. Se un elemento è escluso da un’esclusione globale o non è contenuto nella raccolta selezionata, non verrà visualizzato. Pertanto, quando si utilizza un criterio [!UICONTROL Articoli visualizzati di recente] , è consigliabile utilizzare in genere l’impostazione &quot;Tutte le raccolte&quot;.

## Logica consigli

[!DNL Target Recommendations]In sono utilizzati algoritmi sofisticati per determinare quando le azioni di un visitatore soddisfano i criteri impostati nell&#39;attività. La Chiave consiglio determina le opzioni di logica disponibili.

La seguente logica (criteri) per i consigli è disponibile dall’elenco a discesa [!UICONTROL Logica consigli] :

### Articoli/Media con attributi simili {#similar-attributes}

Consiglia articoli o media simili in base all’attività corrente o al comportamento passato del visitatore.

Se selezioni Articoli/Media con attributi simili, puoi impostare regole di somiglianza del contenuto.

L’utilizzo della somiglianza di contenuto per generare consigli è particolarmente efficace per i nuovi elementi, che probabilmente non verranno visualizzati nei consigli utilizzando le persone che hanno visualizzato questo, hanno visto quello e altre logiche in base al comportamento passato. È inoltre possibile utilizzare la somiglianza del contenuto per generare consigli utili per i nuovi visitatori, che non hanno effettuato acquisti in precedenza o non possiedono altri dati storici.

Per ulteriori informazioni, consulta [Somiglianza del contenuto](/help/c-recommendations/c-algorithms/create-new-algorithm.md#similarity).

Questa logica può essere utilizzata con le seguenti chiavi di raccomandazione:

* Elemento corrente
* Ultimo articolo acquistato
* Ultimo articolo visualizzato
* Articolo più visualizzato

### Articoli più visualizzati {#most-viewed-logic}

Visualizza gli elementi o i file multimediali visualizzati più spesso sul sito.

Questa logica consente di visualizzare consigli basati sugli elementi più visualizzati sul sito per aumentare le conversioni per altri elementi. Ad esempio, un sito multimediale potrebbe visualizzare consigli nella propria home page per i video più visualizzati per incoraggiare i visitatori a guardare altri video.

Questa logica può essere utilizzata con le seguenti chiavi di raccomandazione:

* Categoria corrente
* Attributo personalizzato
* Categoria preferita
* Popolarità

### Chi ha comprato questo ha acquistato anche quello {#bought-bought}

Consiglia gli articoli che sono acquistati più spesso dai clienti contemporaneamente all’articolo specificato.

Questa logica restituisce gli altri prodotti acquistati dopo l’acquisto di questo; il prodotto specificato non è incluso nel set di risultati.

Questa logica ti consente di aumentare le opportunità di vendita incrociata visualizzando una raccomandazione in una pagina di riepilogo del carrello, ad esempio, che mostra gli articoli acquistati anche da altri acquirenti. Ad esempio, se il visitatore sta acquistando un seme, la raccomandazione potrebbe visualizzare altri articoli acquistati insieme alla tuta, come cravatta, scarpe da vestito e gemelli. Man mano che i visitatori esaminano i loro acquisti, fornisci loro ulteriori consigli.

Questa logica può essere utilizzata con le seguenti chiavi di raccomandazione:

* Elemento corrente
* Attributo personalizzato
* Ultimo articolo acquistato
* Ultimo articolo visualizzato
* Articolo più visualizzato

### Chi ha visualizzato questo ha acquistato anche quello {#viewed-bought}

Consiglia gli articoli che vengono acquistati più spesso nella stessa sessione in cui viene visualizzato l’articolo specificato. Questo criterio restituisce gli altri prodotti acquistati dopo la visualizzazione dell’articolo corrente; il prodotto specificato non è incluso nell’insieme di risultati.

Questa logica restituisce gli altri prodotti acquistati dopo aver visualizzato questo; il prodotto specificato non è incluso nel set di risultati.

Questa logica consente di aumentare le opportunità di vendita incrociata visualizzando una raccomandazione su una pagina di prodotto, ad esempio, che mostra gli articoli che altri visitatori hanno visualizzato l’articolo acquistato. Ad esempio, se il visitatore sta visualizzando un palo da pesca, la raccomandazione potrebbe mostrare altri oggetti acquistati, come scatole di gestione, waders e lures da pesca. Quando i visitatori navigano nel sito, è possibile fornire loro ulteriori consigli di acquisto.

Questa logica può essere utilizzata con le seguenti chiavi di raccomandazione:

* Elemento corrente
* Attributo personalizzato
* Ultimo articolo acquistato
* Ultimo articolo visualizzato
* Articolo più visualizzato

### Chi ha visualizzato questo ha visualizzato anche quello {#viewed-viewed}

Consiglia gli elementi che vengono visualizzati più spesso nella stessa sessione in cui viene visualizzato l’elemento specificato.

Questa logica restituisce gli altri prodotti visualizzati dopo la visualizzazione di questo; il prodotto specificato non è incluso nel set di risultati.

Questa logica ti consente di creare ulteriori opportunità di conversione consigliando gli elementi visualizzati anche da altri visitatori che hanno visualizzato un elemento. Ad esempio, i visitatori che visualizzano le bici da strada sul tuo sito potrebbero anche guardare caschi da bicicletta, kit da ciclismo, serrature e così via. Potete creare una raccomandazione utilizzando questa logica che suggerisce altri prodotti per incrementare i ricavi.

Questa logica può essere utilizzata con le seguenti chiavi di raccomandazione:

* Elemento corrente
* Attributo personalizzato
* Ultimo articolo acquistato
* Ultimo articolo visualizzato
* Articolo più visualizzato

### Affinità sito {#site-affinity}

Consiglia gli articoli in base alla certezza di una relazione tra articoli diversi. È possibile configurare questo criterio per determinare la quantità di dati necessari prima che venga presentato un consiglio utilizzando il cursore delle Regole di inclusione. Per esempio, se selezioni molto forte, vengono consigliati i prodotti con una maggiore certezza di corrispondenza.

Ad esempio, se imposti un’affinità molto forte e il progetto include cinque elementi, tre dei quali soddisfano il livello di soglia di connessione, i due elementi che non soddisfano i requisiti di forza minima non vengono visualizzati nei suggerimenti e vengono sostituiti dagli elementi di backup definiti. Gli elementi con affinità più elevata vengono visualizzati per primi.

Ad esempio, un rivenditore online può consigliare gli articoli nelle visite successive di cui un visitatore ha mostrato interesse nelle sessioni precedenti. L&#39;attività per ogni sessione del visitatore viene acquisita per calcolare un&#39;affinità basata su un modello di aggiornamento e frequenza. Quando il visitatore ritorna al sito, viene utilizzata l&#39;affinità di sito per visualizzare i consigli in base alle azioni precedenti sul sito.

Alcuni clienti con varie raccolte di prodotti e comportamenti diversi sui siti potrebbero ottenere risultati ottimali impostando un’affinità di sito debole.

Questa logica può essere utilizzata con le seguenti chiavi di raccomandazione:

* Elemento corrente
* Ultimo articolo acquistato
* Ultimo articolo visualizzato
* Articolo più visualizzato

### Articoli più venduti {#top-sellers}

Visualizza gli elementi inclusi nella maggior parte degli ordini completati. Più unità dello stesso articolo in un unico ordine vengono conteggiate come un ordine.

Questa logica ti consente di creare consigli per gli articoli più venduti sul tuo sito per aumentare le conversioni e i ricavi. Questa logica è particolarmente adatta per i nuovi visitatori del sito.

Questa logica può essere utilizzata con le seguenti chiavi di raccomandazione:

* Categoria preferita
* Popolarità

### Recommendations basato su utente {#user-based}

Consiglia gli articoli in base alla cronologia di navigazione, visualizzazione e acquisto di ogni visitatore. Questi articoli sono generalmente denominati &quot;Consigliati per te&quot;.

Questi criteri ti consentono di fornire contenuti ed esperienze personalizzati sia ai visitatori nuovi che a quelli di ritorno. L’elenco dei consigli è ponderato rispetto all’attività più recente del visitatore, viene aggiornato in sessione e diventa più personalizzato quando l’utente naviga sul sito.

Per determinare gli elementi consigliati vengono utilizzate sia le viste che gli acquisti. La chiave di consiglio specificata (ad esempio Elemento corrente) viene utilizzata per applicare eventuali filtri di regole di inclusione selezionati.

Sarà possibile, ad esempio:

* Escludere gli articoli che non soddisfano determinati criteri (prodotti esauriti, articoli pubblicati più di 30 giorni fa, film classificati R e così via).
* Limita gli elementi inclusi a una singola categoria o alla categoria corrente.

Questa logica può essere utilizzata con le seguenti chiavi di raccomandazione:

* Elemento corrente
* Ultimo articolo acquistato
* Ultimo articolo visualizzato
* Articolo più visualizzato
