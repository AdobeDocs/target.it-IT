---
keywords: chiave di consiglio;logica di consiglio;categoria corrente;attributo personalizzato;ultimo articolo acquistato;ultimo articolo visualizzato;articolo più visualizzato;articolo più visualizzato;articolo più visualizzato;categoria preferita;popolarità;articolo visualizzato di recente;ultimo articolo acquistato;ultimo visualizzato;più visualizzato;preferito;visualizzato di recente
description: Scopri come utilizzare i consigli basati sulle chiavi che utilizzano il contesto di comportamento del visitatore per mostrare risultati rilevanti in Adobe [!DNL Target] Attività Recommendations.
title: Come posso basare il consiglio su una Chiave consiglio?
feature: Recommendations
mini-toc-levels: 2
exl-id: 49764f18-88fb-41be-b2a0-e7ced9de742c
source-git-commit: f673a98b0fc61912b28d1e801e5e4b60c1b15b86
workflow-type: tm+mt
source-wordcount: '3894'
ht-degree: 40%

---

# Basare il consiglio su una chiave consiglio

Recommendations basato sugli algoritmi utilizza il contesto di comportamento del visitatore per mostrare i risultati rilevanti in [!DNL Adobe Target] [!DNL Recommendations] attività.

Ogni tipo di algoritmo fornisce algoritmi diversi appropriati per il relativo tipo, come illustrato nella tabella seguente:

| Tipo di algoritmo | Quando utilizzare | Algoritmi disponibili |
| --- | --- | --- |
| [!UICONTROL Basato sul carrello] | Effettua i consigli in base al contenuto del carrello dell’utente. | <ul><li>Chi ha visualizzato questi ha visualizzato quelli</li><li>Chi li ha visti, li ha comprati</li><li>Chi ha comprato questi ha acquistato quelli</li></ul> |
| [!UICONTROL Basato sulla popolarità] | Puoi formulare consigli in base alla popolarità complessiva di un elemento all’interno del tuo sito o in base alla popolarità degli articoli all’interno della categoria, del marchio, del genere e così via preferiti o più visualizzati da un utente. | <ul><li>Più visualizzati nel sito</li><li>Più visualizzate per categoria</li><li>Più visualizzato per attributo articolo</li><li>Articoli più venduti in tutto il sito</li><li>Più venduti per categoria</li><li>Principali venduti per attributo articolo</li><li>Metrica di Analytics in alto</li></ul> |
| [!UICONTROL Basato su articolo] | formulare raccomandazioni in base al risultato di elementi simili a un elemento che l’utente sta visualizzando o ha visualizzato di recente. | <ul><li>Chi ha visualizzato questo ha visualizzato anche quello</li><li>Chi ha visualizzato questo ha acquistato anche quello</li><li>Chi ha comprato questo ha acquistato anche quello</li><li>Articoli con attributi simili</li></ul> |
| [!UICONTROL Basato su utente] | Eseguite raccomandazioni in base al comportamento dell&#39;utente. | <ul><li>Articoli visualizzati di recente</li><li>Consigliato per te</li></ul> |
| [!UICONTROL Criteri personalizzati] | Crea consigli in base a un file personalizzato caricato. | <ul><li>Algoritmo personalizzato</li></ul> |

Ogni criterio è definito nella relativa scheda. Il traffico è suddiviso in modo uniforme tra i diversi test di criteri. In altre parole, in presenza di due criteri, il traffico viene suddiviso in modo uniforme tra di essi. In presenza di due criteri e di due progettazioni, il traffico viene suddiviso in modo uniforme tra le quattro combinazioni. Puoi inoltre specificare una percentuale di visitatori del sito che visualizzano il contenuto predefinito, a scopo di confronto. In tal caso, la percentuale specificata di visitatori visualizza il contenuto predefinito e gli altri sono suddivisi tra i criteri e le combinazioni di progettazione.

Per ulteriori informazioni sulla creazione dei criteri e sulla definizione dei relativi tipi e algoritmi, consulta [Creare criteri](/help/c-recommendations/c-algorithms/create-new-algorithm.md).

Diversi algoritmi di consigli si prestano a posizionarsi su diversi tipi di pagine. Per ulteriori informazioni su ciascun tipo di algoritmo e i relativi algoritmi disponibili, consulta le sezioni seguenti.

## Basato sul carrello {#cart-based}

La [!UICONTROL Basato sul carrello] Il tipo di algoritmo consente di consigliare gli elementi in base al contenuto del carrello corrente del visitatore. Le chiavi di raccomandazione sono fornite tramite il parametro mbox `cartIds` in valori separati da virgole. Vengono considerati solo i primi 10 valori.

La logica dei consigli basati sul carrello è simile alla &quot;[!UICONTROL Consigliato]&quot; algoritmo basato su utenti e al &quot;[!UICONTROL Chi li ha visti, li ha comprati]&quot; e &quot;[!UICONTROL Chi ha comprato questi ha acquistato quelli]&quot; algoritmi basati su elementi.

[!DNL Target] utilizza tecniche di filtro collaborativo per determinare le somiglianze per ogni elemento nel carrello del visitatore, quindi combina queste somiglianze comportamentali tra ciascun elemento per ottenere un elenco unito.

[!DNL Target] offre anche agli esperti di marketing la possibilità di osservare il comportamento dei visitatori in una singola sessione o in più sessioni:

* **[!UICONTROL Sessione singola]**: In base a ciò che hanno fatto altri visitatori all’interno di una singola sessione.

   Osservare il comportamento all’interno di una singola sessione potrebbe avere senso quando si ha la sensazione che i prodotti si &quot;incontrino&quot; fortemente in base a un utilizzo, un’occasione o un evento. Ad esempio, un visitatore sta acquistando una stampante e potrebbe anche aver bisogno di inchiostro e carta. Oppure, un visitatore sta comprando burro di arachidi e potrebbe anche avere bisogno di pane e gelatina.

* **[!UICONTROL Più sessioni]**: In base a ciò che altri visitatori hanno fatto in più sessioni.

   Osservare il comportamento in più sessioni potrebbe avere senso quando si ha la sensazione che i prodotti si &quot;incontrino&quot; fortemente in base alla preferenza o al gusto del visitatore. Ad esempio, a un visitatore piace Star Wars e potrebbe piacere anche Indiana Jones, anche se il visitatore non vuole necessariamente guardare entrambi i film nella stessa seduta. Oppure, a un visitatore piace il gioco della bacheca &quot;Codenames&quot; e potrebbe anche piacere il gioco della bacheca &quot;Avalon&quot;, anche se il visitatore non può giocare entrambi i giochi contemporaneamente. 

[!DNL Target] formula raccomandazioni per ogni visitatore in base agli elementi nel carrello corrente, indipendentemente dal fatto che osservi il comportamento del visitatore in una singola sessione o in più sessioni.

I seguenti algoritmi sono disponibili con [!UICONTROL Basato sul carrello] tipo di algoritmo:

### [!UICONTROL Chi ha visualizzato questo ha visualizzato anche quelli]

Consiglia gli elementi che vengono visualizzati più spesso nella stessa sessione in cui viene visualizzato l’elemento specificato.

Questa logica restituisce gli altri prodotti visualizzati dopo la visualizzazione di questo; il prodotto specificato non è incluso nel set di risultati.

Questa logica ti consente di creare ulteriori opportunità di conversione consigliando gli elementi visualizzati anche da altri visitatori che hanno visualizzato un elemento. Ad esempio, i visitatori che visualizzano le bici da strada sul tuo sito potrebbero anche guardare caschi da bicicletta, kit da ciclismo, serrature e così via. Potete creare una raccomandazione utilizzando questa logica che suggerisce che altri prodotti vi aiutino ad aumentare i ricavi.

Se selezioni questo algoritmo, puoi selezionare le seguenti chiavi Recommendations:

* Elemento corrente
* Ultimo articolo acquistato
* Ultimo articolo visualizzato
* Articolo più visualizzato

### Chi ha visualizzato questo ha acquistato anche quelli

Consiglia gli articoli che vengono acquistati più spesso nella stessa sessione in cui viene visualizzato l’articolo specificato. Questo criterio restituisce gli altri prodotti acquistati dopo la visualizzazione dell’articolo corrente; il prodotto specificato non è incluso nell’insieme di risultati.

Questa logica restituisce gli altri prodotti acquistati dopo aver visualizzato questo; il prodotto specificato non è incluso nel set di risultati.

Questa logica consente di aumentare le opportunità di vendita incrociata visualizzando una raccomandazione su una pagina di prodotto, ad esempio, che mostra gli articoli che altri visitatori hanno visualizzato l’articolo acquistato. Ad esempio, se il visitatore sta visualizzando un palo da pesca, la raccomandazione potrebbe mostrare altri oggetti acquistati, come scatole di gestione, waders e lures da pesca. Quando i visitatori navigano nel sito, è possibile fornire loro ulteriori consigli di acquisto.

Se selezioni questo algoritmo, puoi selezionare le seguenti chiavi Recommendations:

* Elemento corrente
* Ultimo articolo acquistato
* Ultimo articolo visualizzato
* Articolo più visualizzato

### Chi ha comprato questo ha acquistato anche quelli

Consiglia gli articoli che sono acquistati più spesso dai clienti contemporaneamente all’articolo specificato.

Questa logica restituisce gli altri prodotti acquistati dopo l’acquisto di questo; il prodotto specificato non è incluso nel set di risultati.

Questa logica ti consente di aumentare le opportunità di vendita incrociata visualizzando una raccomandazione in una pagina di riepilogo del carrello, ad esempio, che mostra gli articoli acquistati anche da altri acquirenti. Ad esempio, se il visitatore sta acquistando un seme, il consiglio potrebbe visualizzare altri articoli acquistati insieme alla tuta, come cravatta, scarpe da vestito e gemelli. Man mano che i visitatori esaminano i loro acquisti, fornisci loro ulteriori consigli.

Se selezioni questo algoritmo, puoi selezionare le seguenti chiavi Recommendations:

* Elemento corrente
* Ultimo articolo acquistato
* Ultimo articolo visualizzato
* Articolo più visualizzato

## [!UICONTROL Basato sulla popolarità]

La [!UICONTROL Basato sulla popolarità] il tipo di algoritmo consente di formulare raccomandazioni in base alla popolarità complessiva di un elemento nel sito o in base alla popolarità degli elementi all’interno della categoria, del marchio, del genere e così via preferita da un utente o più visualizzati.

I seguenti algoritmi sono disponibili con [!UICONTROL Basato sulla popolarità] tipo di algoritmo:

### Più visualizzati nel sito {#most-viewed}

Il consiglio è determinato dall&#39;elemento visualizzato più spesso. Tale metodo si basa sul criterio di attualità/frequenza, che si comporta come segue:

* 10 punti per la prima visualizzazione del prodotto
* 5 punti per ogni visualizzazione successiva
* Alla fine della sessione tutti i valori vengono divisi per 2

Ad esempio, la visualizzazione di “tavola da surf A” e poi di “tavola da surf B” in una sessione restituisce come risultato A: 10, B: 5. Al termine della sessione, hai A: 5, B: 2.5. Se visualizzi gli stessi elementi nella sessione successiva, i valori diventano A: 15 B: 7.5.

Utilizza questo algoritmo nelle pagine generali, ad esempio nelle pagine principali o di destinazione e negli annunci offsite.

### Più visualizzate per categoria {#most-viewed-category}

Il consiglio è determinato dalla categoria destinataria della maggioranza dell&#39;attività, con lo stesso metodo utilizzato per “articolo più visualizzato”, il punteggio però viene attribuito alle categorie anziché ai prodotti.

Tale metodo si basa sul criterio di attualità/frequenza, che si comporta come segue:

* 10 punti per la prima visualizzazione della categoria
* 5 punti per ogni visualizzazione successiva

Alle categorie visitate per la prima volta sono attribuiti 10 punti. Per le visite successive alla stessa categoria sono attribuiti 5 punti. A ogni visita, viene sottratto 1 punto alle categorie non correnti che sono state visualizzate in precedenza.

Ad esempio, la visualizzazione di “Categoria A” e poi di “Categoria B” in una sessione restituisce come risultato A: 9, B: 10. Se si visualizzano gli stessi elementi nella sessione successiva, i valori cambiano in A: 20, B: 9.

Utilizza questo algoritmo nelle pagine generali, ad esempio nelle pagine principali o di destinazione e negli annunci offsite.

Se selezionate l&#39;algoritmo Più visualizzato per categoria, potete selezionare le seguenti chiavi Recommendations:

* Categoria corrente
* Categoria preferita

### Più visualizzato per attributo articolo

Consiglia articoli o contenuti multimediali simili agli elementi o ai file multimediali più visualizzati sul sito.

Questo algoritmo consente di selezionare l&#39;attributo dell&#39;elemento su cui si desidera basare il consiglio, ad esempio, &quot;Nome&quot; o &quot;Marchio&quot;.

Seleziona quindi gli attributi di profilo memorizzati nel profilo del visitatore in base ai quali desideri confrontarli, ad esempio &quot;Marchio preferito&quot;, &quot;Ultimo elemento aggiunto al carrello&quot; o &quot;Mostra più visualizzata&quot;.

### Articoli più venduti in tutto il sito {#top-sellers}

Visualizza gli elementi inclusi nella maggior parte degli ordini completati da tutto il sito. Più unità dello stesso articolo in un unico ordine vengono conteggiate come un ordine.

Questo algoritmo consente di creare consigli per gli articoli più venduti sul sito per aumentare le conversioni e i ricavi. Questa logica è particolarmente adatta per i nuovi visitatori del sito.

### Più venduti per categoria

Visualizza gli elementi inclusi nella maggior parte degli ordini completati per categoria. Più unità dello stesso articolo in un unico ordine vengono conteggiate come un ordine.

Questo algoritmo consente di creare consigli per gli articoli più venduti sul sito in base alla categoria per aumentare le conversioni e i ricavi. Questa logica è particolarmente adatta per i nuovi visitatori del sito.

Se selezionate l&#39;algoritmo Più visualizzato per categoria, potete selezionare le seguenti chiavi Recommendations:

* Categoria corrente
* Categoria preferita

### Principali venduti per attributo articolo

(Informazioni disponibili a breve)

### Metrica di Analytics in alto

(Informazioni disponibili a breve)

## [!UICONTROL Basato su articolo]

La [!UICONTROL Basato su articolo] Il tipo di raccomandazione consente di formulare raccomandazioni in base al risultato di elementi simili a un elemento che l&#39;utente sta visualizzando o ha visualizzato di recente.

I seguenti algoritmi sono disponibili con [!UICONTROL Basato su articolo] tipo di algoritmo:

### Chi ha visualizzato questo ha visualizzato anche quello {#viewed-viewed}

Consiglia gli elementi che vengono visualizzati più spesso nella stessa sessione in cui viene visualizzato l’elemento specificato.

Questa logica restituisce gli altri prodotti visualizzati dopo la visualizzazione di questo; il prodotto specificato non è incluso nel set di risultati.

Questa logica ti consente di creare ulteriori opportunità di conversione consigliando gli elementi visualizzati anche da altri visitatori che hanno visualizzato un elemento. Ad esempio, i visitatori che visualizzano le bici da strada sul tuo sito potrebbero anche guardare caschi da bicicletta, kit da ciclismo, serrature e così via. Potete creare una raccomandazione utilizzando questa logica che suggerisce che altri prodotti vi aiutino ad aumentare i ricavi.

Se selezioni questo algoritmo, puoi selezionare le seguenti chiavi Recommendations:

* Elemento corrente
* Ultimo articolo acquistato
* Ultimo articolo visualizzato
* Articolo più visualizzato

### Chi ha visualizzato questo ha acquistato anche quello {#viewed-bought}

Consiglia gli articoli che vengono acquistati più spesso nella stessa sessione in cui viene visualizzato l’articolo specificato. Questo criterio restituisce gli altri prodotti acquistati dopo la visualizzazione dell’articolo corrente; il prodotto specificato non è incluso nell’insieme di risultati.

Questa logica restituisce gli altri prodotti acquistati dopo aver visualizzato questo; il prodotto specificato non è incluso nel set di risultati.

Questa logica consente di aumentare le opportunità di vendita incrociata visualizzando una raccomandazione su una pagina di prodotto, ad esempio, che mostra gli articoli che altri visitatori hanno visualizzato l’articolo acquistato. Ad esempio, se il visitatore sta visualizzando un palo da pesca, la raccomandazione potrebbe mostrare altri oggetti acquistati, come scatole di gestione, waders e lures da pesca. Quando i visitatori navigano nel sito, è possibile fornire loro ulteriori consigli di acquisto.

Se selezioni questo algoritmo, puoi selezionare le seguenti chiavi Recommendations:

* Elemento corrente
* Ultimo articolo acquistato
* Ultimo articolo visualizzato
* Articolo più visualizzato

### Chi ha comprato questo ha acquistato anche quello {#bought-bought}

Consiglia gli articoli che sono acquistati più spesso dai clienti contemporaneamente all’articolo specificato.

Questa logica restituisce gli altri prodotti acquistati dopo l’acquisto di questo; il prodotto specificato non è incluso nel set di risultati.

Questa logica ti consente di aumentare le opportunità di vendita incrociata visualizzando una raccomandazione in una pagina di riepilogo del carrello, ad esempio, che mostra gli articoli acquistati anche da altri acquirenti. Ad esempio, se il visitatore sta acquistando un seme, il consiglio potrebbe visualizzare altri articoli acquistati insieme alla tuta, come cravatta, scarpe da vestito e gemelli. Man mano che i visitatori esaminano i loro acquisti, fornisci loro ulteriori consigli.

Se selezioni questo algoritmo, puoi selezionare le seguenti chiavi Recommendations:

* Elemento corrente
* Ultimo articolo acquistato
* Ultimo articolo visualizzato
* Articolo più visualizzato

### Articoli con attributi simili {#similar-attributes}

Consiglia articoli o media simili in base all’attività corrente o al comportamento passato del visitatore.

Se selezioni Articoli/Media con attributi simili, puoi impostare regole di somiglianza del contenuto.

L’utilizzo della somiglianza di contenuto per generare consigli è particolarmente efficace per i nuovi elementi, che probabilmente non verranno visualizzati nei consigli utilizzando le persone che hanno visualizzato questo, hanno visto quello e altre logiche in base al comportamento passato. È inoltre possibile utilizzare la somiglianza del contenuto per generare consigli utili per i nuovi visitatori, che non hanno effettuato acquisti in precedenza o non possiedono altri dati storici.

Se selezioni questo algoritmo, puoi selezionare le seguenti chiavi Recommendations:

* Elemento corrente
* Ultimo articolo acquistato
* Ultimo articolo visualizzato
* Articolo più visualizzato

Per ulteriori informazioni, consulta [Somiglianza del contenuto](/help/c-recommendations/c-algorithms/create-new-algorithm.md#similarity).

## [!UICONTROL Basato su utente]

Il tipo di algoritmo basato su utente consente di formulare raccomandazioni in base al comportamento dell’utente.

I seguenti algoritmi sono disponibili con [!UICONTROL Basato su utente] tipo di algoritmo:

### Articoli visualizzati di recente {#recently-viewed}

Utilizza la cronologia del visitatore (nell&#39;arco delle sessioni) per presentare gli ultimi elementi *x* visualizzati, in base al numero di posizioni nella progettazione.

L’algoritmo di visualizzazione degli elementi visualizzati di recente restituisce un risultato specifico per un dato [ambiente](/help/administrating-target/hosts.md). Se due siti appartengono ad ambienti diversi e un visitatore passa da un sito all’altro, ciascun sito mostra solo gli articoli visualizzati di recente per il sito appropriato. Se due siti si trovano nello stesso ambiente e un visitatore passa tra i due siti, il visitatore visualizza gli stessi elementi visualizzati di recente per entrambi i siti.

>[!NOTE]
>
>Non è possibile utilizzare il [!UICONTROL Articoli visualizzati di recente] criteri per i consigli di backup.

Puoi filtrare gli articoli o i file multimediali visualizzati di recente in modo che vengano visualizzati solo quelli con uno specifico attributo.

* I criteri “visualizzati di recente” sono configurabili, come altri criteri nei consigli.
* È possibile utilizzare [raccolte](/help/c-recommendations/c-products/collections.md), [esclusioni](/help/c-recommendations/c-products/exclusions.md) e [inclusioni](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) (incluse le regole speciali per Prezzo e Inventario) proprio come per tutti gli altri criteri.

Eventuali casi d’uso includono: un’azienda multinazionale con più aziende potrebbe avere un visitatore che visualizza elementi su più proprietà digitali. In questo caso, puoi limitare gli articoli visualizzati di recente al solo sito su cui sono stati visualizzati. Questo impedisce la visualizzazione degli elementi visualizzati di recente sul sito di un&#39;altra proprietà digitale.

Utilizza questo algoritmo nelle pagine generali, ad esempio nelle pagine principali o di destinazione e negli annunci offsite.

>[!NOTE]
>
>[!UICONTROL Articoli visualizzati di recente] rispetta sia le impostazioni globali di esclusioni che l’impostazione di raccolta selezionata per l’attività. Se un elemento è escluso da un’esclusione globale o non è contenuto nella raccolta selezionata, non verrà visualizzato. Pertanto, quando si utilizza un [!UICONTROL Articoli visualizzati di recente] In genere, è necessario utilizzare l’impostazione &quot;Tutte le raccolte&quot;.

### Consigliato per te {#recommended-for-you}

Consiglia gli articoli in base alla cronologia di navigazione, visualizzazione e acquisto di ogni visitatore.

Questo algoritmo consente di fornire contenuti ed esperienze personalizzati sia ai visitatori nuovi che a quelli di ritorno. L’elenco dei consigli è ponderato rispetto all’attività più recente del visitatore, viene aggiornato in sessione e diventa più personalizzato quando l’utente naviga sul sito.

Per determinare gli elementi consigliati vengono utilizzate sia le viste che gli acquisti. La chiave di consiglio specificata (ad esempio, Elemento corrente) viene utilizzata per applicare eventuali filtri di regola di inclusione selezionati.

Sarà possibile, ad esempio:

* Escludere gli articoli che non soddisfano determinati criteri (prodotti esauriti, articoli pubblicati più di 30 giorni fa, film classificati R e così via).
* Limita gli elementi inclusi a una singola categoria o alla categoria corrente.

Se si seleziona questo algoritmo, è possibile selezionare le seguenti chiavi di filtro:

* Elemento corrente
* Ultimo articolo acquistato
* Ultimo articolo visualizzato
* Articolo più visualizzato

## Criteri personalizzati {#custom}

Il tipo di algoritmo Criteri personalizzati ti consente di formulare raccomandazioni in base a un file personalizzato caricato.

Il consiglio è determinato da un elemento memorizzato nel profilo di un visitatore, utilizzando uno degli utenti.*x* o profilo.Attributi *x*.

Quando questa opzione è selezionata, il valore `entity.id` deve essere presente nell&#39;attributo profilo.

Quando basi i consigli su attributi personalizzati, seleziona l&#39;attributo personalizzato, quindi il tipo di consiglio.

Puoi eseguire il filtro in tempo reale all&#39;inizio dell&#39;output di criteri personalizzati. Ad esempio, puoi limitare gli articoli consigliati a quelli della categoria o del marchio preferito dal visitatore. Così puoi combinare calcoli offline e filtri in tempo reale.

Questa funzionalità consente di utilizzare [!DNL Target] per aggiungere la personalizzazione ai consigli calcolati offline o agli elenchi personalizzati. Permette infatti di unire le compenze del personale addetto ai dati alle tecnonologie comprovate di Adobe per la distribuzione, l&#39;applicazione di filtri al momento dell&#39;esecuzione, i test A/B, il targeting, la generazione di rapporti, le integrazioni e altro.

Con l’aggiunta delle regole di inclusione ai Criteri personalizzati, i consigli non sono più statici ma diventano dinamici, in base agli interessi del visitatore.

* I criteri personalizzati sono configurabili, come altri criteri nei consigli.
* È possibile utilizzare [raccolte](/help/c-recommendations/c-products/collections.md), [esclusioni](/help/c-recommendations/c-products/exclusions.md) e [inclusioni](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) (incluse le regole speciali per Prezzo e Inventario) proprio come per tutti gli altri criteri.

Eventuali casi di utilizzo includono:

* Vuoi consigliare film da una lista personalizzata, ma solo se il visitatore non li ha già guardati.
* Desideri eseguire un algoritmo offline e utilizzare i risultati per abilitare i consigli, ma devi assicurarti che gli articoli esauriti non siano mai consigliati.
* Vuoi includere solo gli articoli appartenenti alla categoria preferita del visitatore.

## Chiavi dei consigli

Le seguenti chiavi di raccomandazione sono disponibili dal [!UICONTROL Chiave dei consigli] elenco a discesa:

### Elemento corrente {#current-item}

Il consiglio è determinato dall&#39;elemento attualmente visualizzato dal visitatore.

Il consiglio visualizzano altri elementi che potrebbero interessare i visitatori interessati all&#39;elemento specificato.

Quando questa opzione è selezionata, il valore `entity.id` deve essere trasmesso come parametro alla mbox di visualizzazione.

Può essere utilizzato con i seguenti algoritmi:

* [!UICONTROL Articoli con attributi simili]
* [!UICONTROL Chi ha visualizzato questo ha visualizzato anche quello]
* [!UICONTROL Chi ha visualizzato questo ha acquistato anche quello]
* [!UICONTROL Chi ha comprato questo ha acquistato anche quello]

Utilizza la [!UICONTROL Elemento corrente] chiave di consigli sul sito:

* Pagine a elemento singolo, ad esempio le pagine del prodotto.
* NON utilizzare nelle pagine dei risultati di ricerca nulli.

### Ultimo articolo acquistato {#last-purchased}

Il consiglio è determinato in base all&#39;ultimo articolo acquistato da ogni visitatore univoco. Questa viene acquisita automaticamente, pertanto non è necessario trasmettere alcun valore alla pagina.

Può essere utilizzato con i seguenti algoritmi:

* [!UICONTROL Articoli con attributi simili]
* [!UICONTROL Chi ha visualizzato questo ha visualizzato anche quello]
* [!UICONTROL Chi ha visualizzato questo ha acquistato anche quello]
* [!UICONTROL Chi ha comprato questo ha acquistato anche quello]

Utilizza la [!UICONTROL Ultimo articolo acquistato] chiave di consigli sul sito:

* Pagina principale, pagina account, annunci fuori sede.
* NON utilizzare su pagine di prodotti o pagine rilevanti per gli acquisti.

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

### Ultimo articolo visualizzato {#last-viewed}

Il consiglio è determinato dall&#39;ultimo articolo visualizzato da ogni visitatore univoco. Questa viene acquisita automaticamente, pertanto non è necessario trasmettere alcun valore alla pagina.

Può essere utilizzato con i seguenti algoritmi:

* [!UICONTROL Articoli con attributi simili]
* [!UICONTROL Chi ha visualizzato questo ha visualizzato anche quello]
* [!UICONTROL Chi ha visualizzato questo ha acquistato anche quello]
* [!UICONTROL Chi ha comprato questo ha acquistato anche quello]

Utilizza la [!UICONTROL Ultimo articolo visualizzato] chiave di consigli sul sito:

* Pagina principale, pagina account, annunci fuori sede.
* NON utilizzare su pagine di prodotti o pagine rilevanti per gli acquisti.

### Articolo più visualizzato {#most-viewed-logic}

Visualizza gli elementi o i file multimediali visualizzati più spesso sul sito.

Questa logica consente di visualizzare consigli basati sugli elementi più visualizzati sul sito per aumentare le conversioni per altri elementi. Ad esempio, un sito multimediale potrebbe visualizzare consigli nella propria home page per i video più visualizzati per incoraggiare i visitatori a guardare altri video.

Questa chiave di raccomandazione può essere utilizzata con i seguenti algoritmi:

* [!UICONTROL Articoli con attributi simili]
* [!UICONTROL Chi ha visualizzato questo ha visualizzato anche quello]
* [!UICONTROL Chi ha visualizzato questo ha acquistato anche quello]
* [!UICONTROL Chi ha comprato questo ha acquistato anche quello]

### Categoria corrente {#current-category}

Il consiglio è determinato dalla categoria di prodotto attualmente visualizzata dal visitatore.

I consigli mostrano gli elementi nella categoria di prodotto specificata.

Quando questa opzione è selezionata, il valore `entity.categoryId` deve essere trasmesso come parametro alla mbox di visualizzazione.

Questa chiave di raccomandazione può essere utilizzata con i seguenti algoritmi:

* Articoli più venduti
* Articoli più visualizzati

Utilizza la [!UICONTROL Categoria corrente] chiave di consigli sul sito:

* Pagine a categoria singola.
* NON utilizzare nelle pagine dei risultati di ricerca nulli.

### Categoria preferita {#favorite-category}

Il consiglio è determinato dalla categoria di prodotto preferita del visitatore.

I consigli mostrano gli elementi nella categoria di prodotto specificata.

Quando questa opzione è selezionata, il valore `entity.categoryId` deve essere trasmesso come parametro alla mbox di visualizzazione.

Questa chiave di raccomandazione può essere utilizzata con i seguenti algoritmi:

* Articoli più venduti
* Articoli più visualizzati

Utilizza la [!UICONTROL Categoria corrente] chiave di consigli sul sito:

* Pagine a categoria singola.
* NON utilizzare nelle pagine dei risultati di ricerca nulli.

### Affinità sito {#site-affinity}

Consiglia gli articoli in base alla certezza di una relazione tra articoli diversi. È possibile configurare questo criterio per determinare la quantità di dati necessari prima che venga presentato un consiglio utilizzando il cursore delle Regole di inclusione. Per esempio, se selezioni molto forte, vengono consigliati i prodotti con una maggiore certezza di corrispondenza.

Ad esempio, se imposti un’affinità molto forte e il progetto include cinque elementi, tre dei quali soddisfano il livello di soglia di connessione, i due elementi che non soddisfano i requisiti di forza minima non vengono visualizzati nei suggerimenti e vengono sostituiti dagli elementi di backup definiti. Gli elementi con affinità più elevata vengono visualizzati per primi.

Ad esempio, un rivenditore online può consigliare agli articoli in visite successive di cui un visitatore ha mostrato interesse durante le sessioni precedenti. L&#39;attività per ogni sessione del visitatore viene acquisita per calcolare un&#39;affinità basata su un modello di aggiornamento e frequenza. Quando il visitatore ritorna al sito, viene utilizzata l&#39;affinità di sito per visualizzare i consigli in base alle azioni precedenti sul sito.

Alcuni clienti con varie raccolte di prodotti e comportamenti diversi sui siti potrebbero ottenere risultati ottimali impostando un’affinità di sito debole.

Questa logica può essere utilizzata con le seguenti chiavi di raccomandazione:

* Elemento corrente
* Ultimo articolo acquistato
* Ultimo articolo visualizzato
* Articolo più visualizzato
