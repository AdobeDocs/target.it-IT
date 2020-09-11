---
keywords: recommendation key;recommendation logic;current category;custom attribute;last purchased item;last viewed item;most viewed item;most viewed item;favorite category;popularity;recently viewed item;last purchased;last viewed;most viewed;favorite;recently viewed
description: Recommendations basato sulle chiavi utilizza il contesto del comportamento del visitatore per mostrare risultati rilevanti nelle attività di Adobe Target Recommendations.
title: Basare il consiglio su una chiave consiglio
feature: criteria
mini-toc-levels: 2
translation-type: tm+mt
source-git-commit: 21c8e39669925e8fd26d7f64ea7dfe95f28795bf
workflow-type: tm+mt
source-wordcount: '2151'
ht-degree: 70%

---


# Basare il consiglio su una chiave consiglio

Recommendations based on keys use visitor behavior context to show relevant results in [!DNL Adobe Target] [!DNL Recommendations] activities.

Esistono due tipi di consigli:

* **Popolarità:** elenca gli elementi in base ai più visualizzati, i più venduti, e alla metrica migliore. La chiave dei criteri di popolarità è vuota.
* **Basato su chiave:** comprende il resto dei criteri. I consigli offrono una serie diversificata di scelte per quanto riguarda il tipo di chiave. Le opzioni variano da “elemento corrente” a “parametri profilo” e consentono di impostare la chiave dei valori da consigliare in modo sistematico. È possibile sottoporre a test più criteri confrontandoli uno con l&#39;altro e basando ogni criterio su una chiave diversa.

Ogni criterio è definito nella relativa scheda. Il traffico è suddiviso in modo uniforme tra i diversi test di criteri. In altre parole, in presenza di due criteri, il traffico viene suddiviso in modo uniforme tra di essi. In presenza di due criteri e di due progettazioni, il traffico viene suddiviso in modo uniforme tra le quattro combinazioni. Puoi inoltre specificare una percentuale di visitatori del sito che visualizzano il contenuto predefinito, a scopo di confronto. In tal caso, la percentuale specificata di visitatori visualizza il contenuto predefinito e gli altri sono suddivisi tra i criteri e le combinazioni di progettazione.

1. Create a new criteria, or select an existing criteria and click **[!UICONTROL Edit]**.
1. To change the recommendation key, select the new key from the [!UICONTROL Recommendation Key] drop-down list, then click **[!UICONTROL Save]** or **[!UICONTROL Update]**.

   Poiché diverse logiche sono associate a diverse chiavi di consigli, diversi consigli si prestano a posizionarsi su diversi tipi di pagine. Per ulteriori informazioni su ciascuna chiave di raccomandazione, consultate le sezioni seguenti.

## Chiavi di raccomandazione

Le seguenti chiavi di raccomandazione sono disponibili nell&#39;elenco a discesa [!UICONTROL Chiave] raccomandazione:

### Elemento corrente

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

### Categoria corrente

Il consiglio è determinato dalla categoria di prodotto attualmente visualizzata dal visitatore.

I consigli mostrano gli elementi nella categoria di prodotto specificata.

Quando questa opzione è selezionata, il valore `entity.categoryId` deve essere trasmesso come parametro alla mbox di visualizzazione.

#### Logica (criteri)

* Articoli più venduti
* Articoli più visualizzati

#### Dove utilizzare nel sito

* Pagine a categoria singola.
* NON utilizzare nelle pagine dei risultati di ricerca nulli.

### Attributo personalizzato {#custom}

Il consiglio è determinato da un elemento memorizzato nel profilo di un visitatore, utilizzando uno degli utenti.*x* o profilo.Attributi *x*.

Quando questa opzione è selezionata, il valore `entity.id` deve essere presente nell&#39;attributo profilo.

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

#### Chiave delle raccomandazioni personalizzate

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

### Ultimo articolo acquistato

Il consiglio è determinato in base all&#39;ultimo articolo acquistato da ogni visitatore. Tale dato viene acquisito automaticamente, quindi non è necessario trasmettere alcun valore alla pagina.

#### Logica (criteri)

* [!UICONTROL Articoli con attributi simili]
* [!UICONTROL Chi ha visualizzato questo ha visualizzato anche quello]
* [!UICONTROL Chi ha visualizzato questo ha acquistato anche quello]
* [!UICONTROL Chi ha comprato questo ha acquistato anche quello]
* [!UICONTROL Affinità sito]

#### Dove utilizzare nel sito

* Pagina principale, pagina account, annunci fuori sede.
* NON utilizzare su pagine di prodotti o pagine rilevanti per gli acquisti.

### Ultimo articolo visualizzato

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

### Articolo più visualizzato

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

### Categoria preferita

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

### Popolarità

Il consiglio è determinata dalla popolarità degli elementi sul sito. Il consiglio di tipo popolarità include gli elementi più venduti e i più visualizzati secondo i dati mbox e, se si utilizza Adobe Analytics, tutte le metriche disponibili nel rapporto del prodotto. Gli elementi vengono classificati in base alla logica del consiglio selezionato.

#### Logica (criteri)

* [!UICONTROL Articoli più venduti]
* [!UICONTROL Articoli più visualizzati]
* Metrica del rapporto del prodotto (se si utilizza Adobe Analytics)

#### Dove utilizzare nel sito

* Pagine generali, come la pagina principale o le pagine di destinazione e gli annunci offsite.

### Articoli visualizzati di recente {#recently-viewed}

Utilizza la cronologia del visitatore (nell&#39;arco delle sessioni) per presentare gli ultimi elementi *x* visualizzati, in base al numero di posizioni nella progettazione.

Il criterio Articoli visualizzati di recente ora restituisce risultati specifici per un dato [ambiente](/help/administrating-target/hosts.md). Se due siti appartengono ad ambienti diversi e un visitatore passa da un sito all’altro, ciascun sito mostra solo gli articoli visualizzati di recente per il sito appropriato. Se due siti si trovano nello stesso ambiente e un visitatore passa tra di essi, il visitatore vedrà gli stessi elementi visualizzati di recente per entrambi i siti.

#### Dove utilizzare nel sito

* Pagine generali, come la pagina principale o le pagine di destinazione e gli annunci offsite.

>[!NOTE]
>
>“Articoli visualizzati di recente” rispetta sia le impostazioni globali Esclusioni sia l’impostazione Raccolta selezionata per l’attività. Se un elemento è escluso da un’esclusione globale, o non è incluso nella raccolta selezionata, non verrà visualizzato; di conseguenza, quando si utilizza il criterio “Articoli visualizzati di recente”, viene solitamente utilizzata l’impostazione “Tutte le raccolte”.

## Logica raccomandazione

La seguente logica di raccomandazione (criteri) è disponibile dall&#39;elenco a discesa Logica  raccomandazione:

### Elementi con attributi simili

Le regole di somiglianza del contenuto confrontano le parole chiave dell&#39;attributo dell&#39;elemento e formulano consigli basati su quante parole chiave hanno in comune diversi elementi. I consigli basati sulla somiglianza del contenuto non richiedono dati precedenti per fornire risultati significativi.

L&#39;utilizzo della similarità dei contenuti per generare raccomandazioni è particolarmente efficace per i nuovi elementi, che probabilmente non verranno visualizzati nelle raccomandazioni utilizzando le persone che hanno visualizzato questo, l&#39;hanno visualizzato e altre logiche basate sul comportamento passato. È inoltre possibile utilizzare la somiglianza del contenuto per generare consigli utili per i nuovi visitatori, che non hanno effettuato acquisti in precedenza o non possiedono altri dati storici.

Per ulteriori informazioni, consultate [Somiglianza](/help/c-recommendations/c-algorithms/create-new-algorithm.md#similarity)contenuto.

Questa logica può essere utilizzata con le seguenti chiavi di raccomandazione:

* Elemento corrente
* Ultimo articolo acquistato
* Ultimo articolo visualizzato
* Articolo più visualizzato

### Articoli più visualizzati

Visualizza gli elementi più visualizzati sul sito.

Questa logica consente di visualizzare le raccomandazioni in base agli elementi più visualizzati sul sito per aumentare le conversioni per altri elementi. Ad esempio, un sito multimediale potrebbe visualizzare raccomandazioni nella propria pagina principale per i video più popolari per incoraggiare i visitatori a guardare altri video.

Questa logica può essere utilizzata con le seguenti chiavi di raccomandazione:

* Categoria corrente
* Attributo personalizzato
* Categoria preferita
* Popolarità

### Chi ha comprato questo ha acquistato anche quello

Visualizza gli elementi acquistati anche dagli altri visitatori che hanno acquistato l’elemento selezionato.

Questa logica consente di aumentare le opportunità di cross-selling mostrando una raccomandazione su una pagina di riepilogo del carrello, ad esempio, che mostra gli articoli acquistati anche da altri acquirenti. Ad esempio, se il visitatore sta acquistando una tuta, la raccomandazione potrebbe visualizzare altri elementi acquistati dai visitatori, come cravatte, scarpe da vestito e gemelli. Quando i visitatori rivedono i loro acquisti, gli potete fornire ulteriori raccomandazioni di acquisto.

Questa logica può essere utilizzata con le seguenti chiavi di raccomandazione:

* Elemento corrente
* Attributo personalizzato
* Ultimo articolo acquistato
* Ultimo articolo visualizzato
* Articolo più visualizzato

### Chi ha visualizzato questo ha acquistato anche quello

Visualizza altri elementi acquistati dai visitatori che hanno visualizzato l’elemento selezionato.

Questa logica consente di aumentare le opportunità di cross-selling mostrando una raccomandazione su una pagina di prodotto, ad esempio, che mostra gli elementi che altri visitatori hanno visualizzato l&#39;elemento acquistato. Ad esempio, se il visitatore sta visualizzando un polo di pesca, la raccomandazione potrebbe mostrare altri elementi che visualizzano l&#39;elemento acquistato, come ad esempio le caselle di controllo, i wader e gli lustri di pesca. Quando i visitatori consultano il sito, vengono loro fornite ulteriori raccomandazioni di acquisto.

Questa logica può essere utilizzata con le seguenti chiavi di raccomandazione:

* Elemento corrente
* Attributo personalizzato
* Ultimo articolo acquistato
* Ultimo articolo visualizzato
* Articolo più visualizzato

### Chi ha visualizzato questo ha visualizzato anche quello

Visualizza gli elementi visualizzati anche dagli altri visitatori che hanno visualizzato l’elemento selezionato.

Questa logica consente di creare ulteriori opportunità di conversione consigliando gli elementi visualizzati anche dagli altri visitatori che hanno visualizzato un elemento. Ad esempio, i visitatori che visualizzano le bici da strada sul sito possono anche guardare caschi ciclabili, kit ciclabili, serrature e così via. Potete creare una raccomandazione utilizzando questa logica che suggerisce altri prodotti.

Questa logica può essere utilizzata con le seguenti chiavi di raccomandazione:

* Elemento corrente
* Attributo personalizzato
* Ultimo articolo acquistato
* Ultimo articolo visualizzato
* Articolo più visualizzato

### Affinità sito

Visualizza gli elementi utilizzando un algoritmo proprietario  Adobe per raccomandare altri elementi in base a criteri, come visualizzazioni della pagina del prodotto, acquisti e attività del carrello (aggiunta o rimozione di elementi, visualizzazione del carrello, ecc.)

Ad esempio, un rivenditore online può raccomandare gli elementi che un visitatore ha mostrato interesse durante le sessioni passate nelle visite successive. L&#39;attività di ogni sessione del visitatore viene acquisita per calcolare un punteggio di affinità in base a un modello di recente e di frequenza. Quando il visitatore ritorna al sito, l&#39;affinità del sito viene utilizzata per visualizzare le raccomandazioni in base alle azioni passate sul sito.

Questa logica può essere utilizzata con le seguenti chiavi di raccomandazione:

* Elemento corrente
* Ultimo articolo acquistato
* Ultimo articolo visualizzato
* Articolo più visualizzato

### Articoli più venduti

Visualizza gli elementi più venduti sul sito in base alle conversioni dei visitatori.

Questa logica consente di creare raccomandazioni per elementi popolari sul sito per aumentare la conversione. Questa logica è particolarmente adatta per i nuovi visitatori del sito.

Questa logica può essere utilizzata con le seguenti chiavi di raccomandazione:

* Categoria preferita
* Popolarità
