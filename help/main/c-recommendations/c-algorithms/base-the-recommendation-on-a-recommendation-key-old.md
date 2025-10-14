---
keywords: chiave consigli;logica consigli;categoria corrente;attributo personalizzato;ultimo articolo acquistato;ultimo articolo visualizzato;articolo più visualizzato;articolo più visualizzato;categoria preferita;popolarità;articolo visualizzato di recente;ultimo articolo acquistato;più visualizzato;preferito;visualizzato di recente
description: Scopri come utilizzare i consigli in base a chiavi che utilizzano il contesto del comportamento del visitatore per mostrare risultati rilevanti nelle attività di Adobe [!DNL Target] Recommendations.
title: Come posso basare il consiglio su una Chiave consiglio?
feature: Recommendations
mini-toc-levels: 2
exl-id: 49764f18-88fb-41be-b2a0-e7ced9de742c
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '3845'
ht-degree: 33%

---

# Basare il consiglio su una chiave consiglio

I consigli basati su algoritmi utilizzano il contesto del comportamento del visitatore per mostrare risultati rilevanti nelle attività [!DNL Adobe Target] [!DNL Recommendations].

Ogni tipo di algoritmo fornisce diversi algoritmi appropriati al proprio tipo, come illustrato nella tabella seguente:

| Tipo di algoritmo | Quando utilizzare | Algoritmi disponibili |
| --- | --- | --- |
| [!UICONTROL Cart-Based] | Creare consigli in base al contenuto del carrello dell’utente. | <ul><li>Chi ha visualizzato questi ha visualizzato anche quelli</li><li>Chi ha visualizzato questi ha acquistato anche quelli</li><li>Chi ha comprato questi ha acquistato anche quelli</li></ul> |
| [!UICONTROL Popularity-Based] | Puoi formulare raccomandazioni in base alla popolarità complessiva di un elemento nel tuo sito o in base alla popolarità degli elementi nella categoria, nel brand, nel genere e così via preferiti o più visualizzati di un utente. | <ul><li>Articoli più visualizzati nel sito</li><li>Più visualizzati per categoria</li><li>Più visualizzati per attributo articolo</li><li>Articoli più venduti in tutto il sito</li><li>Articoli più venduti per categoria</li><li>Attributo Articoli più venduti</li><li>Primi per metrica di Analytics</li></ul> |
| [!UICONTROL Item-Based] | Creare consigli in base alla ricerca di elementi simili a quelli di un elemento attualmente visualizzato dall’utente o che è stato recentemente visualizzato. | <ul><li>Chi ha visualizzato questo ha visualizzato anche quello</li><li>Chi ha visualizzato questo ha acquistato anche quello</li><li>Chi ha comprato questo ha acquistato anche quello</li><li>Articoli con attributi simili</li></ul> |
| [!UICONTROL User-Based] | Creare consigli in base al comportamento dell’utente. | <ul><li>Articoli visualizzati di recente</li><li>Consigliato per te</li></ul> |
| [!UICONTROL Custom Criteria] | Formulare raccomandazioni in base a un file personalizzato caricato. | <ul><li>Algoritmo personalizzato</li></ul> |

Ogni criterio è definito nella relativa scheda. Il traffico è suddiviso in modo uniforme tra i diversi test di criteri. In altre parole, in presenza di due criteri, il traffico viene suddiviso in modo uniforme tra di essi. In presenza di due criteri e di due progettazioni, il traffico viene suddiviso in modo uniforme tra le quattro combinazioni. Puoi inoltre specificare una percentuale di visitatori del sito che visualizzano il contenuto predefinito, a scopo di confronto. In tal caso, la percentuale di visitatori specificata visualizza il contenuto predefinito e il resto viene suddiviso tra i criteri e le combinazioni di progettazione.

Per ulteriori informazioni sulla creazione di criteri e sulla definizione dei relativi tipi di algoritmi e algoritmi, vedere [Creare criteri](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md).

Diversi algoritmi di Recommendations si prestano a essere posizionati su diversi tipi di pagine. Per ulteriori informazioni su ciascun tipo di algoritmo e sui relativi algoritmi disponibili, consulta le sezioni seguenti.

## Basato su carrello {#cart-based}

Il tipo di algoritmo [!UICONTROL Cart-Based] consente di consigliare gli elementi in base al contenuto del carrello corrente del visitatore. Le chiavi di consigli sono fornite tramite il parametro [`cartIds` di &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html?lang=it){target=_blank}mbox in valori separati da virgola. Vengono considerati solo i primi 10 valori.

La logica dei consigli basati sul carrello è simile all&#39;algoritmo basato sull&#39;utente &quot;[!UICONTROL Recommended For You]&quot; e agli algoritmi basati sull&#39;elemento &quot;[!UICONTROL People Who Viewed These, Bought Those]&quot; e &quot;[!UICONTROL People Who Bought These, Bought Those]&quot;.

[!DNL Target] utilizza tecniche di filtro collaborativo per determinare le somiglianze per ogni elemento nel carrello del visitatore, quindi combina queste somiglianze comportamentali in ogni elemento per ottenere un elenco unito.

[!DNL Target] offre inoltre agli addetti al marketing la possibilità di osservare il comportamento dei visitatori all&#39;interno di una singola sessione o in più sessioni:

* **[!UICONTROL Single Session]**: in base a ciò che hanno fatto altri visitatori in una singola sessione.

  Osservare il comportamento all’interno di una singola sessione potrebbe avere senso quando si ha la sensazione che i prodotti vivamente si &quot;accompagnano&quot; l’uno con l’altro in base a un utilizzo, un’occasione o un evento. Ad esempio, un visitatore sta acquistando una stampante e potrebbe anche aver bisogno di carta e inchiostro. Oppure, un visitatore sta comprando burro di arachidi e potrebbe anche aver bisogno di pane e gelatina.

* **[!UICONTROL Across Sessions]**: in base alle azioni degli altri visitatori in più sessioni.

  Osservare il comportamento in più sessioni potrebbe avere senso quando si ha la sensazione che i prodotti vivamente &quot;vanno di pari passo&quot; l’uno con l’altro in base alle preferenze o al gusto dei visitatori. Ad esempio, a un visitatore piace Star Wars e potrebbe piacere anche Indiana Jones, anche se non desidera necessariamente guardare entrambi i film contemporaneamente. Oppure, a un visitatore piace il gioco da tavolo &quot;Codenames&quot; e potrebbe anche piacere il gioco da tavolo &quot;Avalon&quot;, anche se il visitatore non può giocare entrambi i giochi contemporaneamente. 

[!DNL Target] formula raccomandazioni per ogni visitatore in base agli elementi nel carrello corrente, indipendentemente dal fatto che si osservi il comportamento del visitatore all&#39;interno di una singola sessione o in più sessioni.

Con il tipo di algoritmo [!UICONTROL Cart-Based] sono disponibili i seguenti algoritmi:

### [!UICONTROL People Who Viewed This, Viewed Those]

Consiglia gli elementi che vengono visualizzati più spesso nella stessa sessione in cui viene visualizzato l’elemento specificato.

Questa logica restituisce altri prodotti visualizzati dopo aver visualizzato questo; il prodotto specificato non è incluso nel set di risultati.

Questa logica consente di creare opportunità di conversione aggiuntive consigliando gli articoli visualizzati anche dagli altri visitatori che hanno visualizzato un articolo. Ad esempio, i visitatori che visualizzano le bici da strada sul sito potrebbero anche guardare caschi, kit per ciclismo, serrature e così via. Utilizzando questa logica, puoi creare un consiglio che suggerisca ad altri prodotti di aiutarti ad aumentare i ricavi.

Se selezioni questo algoritmo, puoi selezionare le seguenti Chiavi consigli:

* Elemento corrente
* Ultimo articolo acquistato
* Ultimo articolo visualizzato
* Articolo più visualizzato

### Chi ha visualizzato questo ha acquistato anche quelli

Consiglia gli articoli che vengono acquistati più spesso nella stessa sessione in cui viene visualizzato l’articolo specificato. Questo criterio restituisce gli altri prodotti acquistati dopo la visualizzazione dell’articolo corrente; il prodotto specificato non è incluso nell’insieme di risultati.

Questa logica restituisce altri prodotti acquistati dopo aver visualizzato questo; il prodotto specificato non è incluso nel set di risultati.

Questa logica consente di aumentare le opportunità di cross-selling visualizzando un consiglio in una pagina di prodotto, ad esempio, in cui vengono visualizzati gli articoli acquistati da altri visitatori. Ad esempio, se il visitatore visualizza un palo da pesca, il consiglio potrebbe mostrare altri elementi acquistati da altri visitatori, come scatole per placcaggi, trampolieri e esche per pesca. Man mano che i visitatori navigano nel tuo sito, fornisci loro ulteriori consigli di acquisto.

Se selezioni questo algoritmo, puoi selezionare le seguenti Chiavi consigli:

* Elemento corrente
* Ultimo articolo acquistato
* Ultimo articolo visualizzato
* Articolo più visualizzato

### Chi ha comprato questo ha acquistato anche quelli

Consiglia gli articoli che sono acquistati più spesso dai clienti contemporaneamente all’articolo specificato.

Questa logica restituisce altri prodotti acquistati dopo l’acquisto di questo; il prodotto specificato non è incluso nel set di risultati.

Questa logica ti consente di aumentare le opportunità di cross-selling visualizzando un consiglio in una pagina di riepilogo del carrello, ad esempio, in cui vengono visualizzati gli articoli acquistati anche da altri acquirenti. Ad esempio, se il visitatore acquista un completo, il consiglio potrebbe mostrare altri articoli acquistati da altri visitatori insieme all’indumento, come cravatte, scarpe e gemelli. Man mano che i visitatori esaminano i loro acquisti, fornisci loro ulteriori consigli.

Se selezioni questo algoritmo, puoi selezionare le seguenti Chiavi consigli:

* Elemento corrente
* Ultimo articolo acquistato
* Ultimo articolo visualizzato
* Articolo più visualizzato

## [!UICONTROL Popularity-Based]

Il tipo di algoritmo [!UICONTROL Popularity-Based] consente di formulare raccomandazioni in base alla popolarità complessiva di un elemento nel sito o in base alla popolarità degli elementi nella categoria, nel marchio, nel genere e così via preferiti o più visualizzati dell&#39;utente.

Con il tipo di algoritmo [!UICONTROL Popularity-Based] sono disponibili i seguenti algoritmi:

### Articoli più visualizzati nel sito {#most-viewed}

Il consiglio è determinato dall’elemento visualizzato più di frequente. Tale metodo si basa sul criterio di attualità/frequenza, che si comporta come segue:

* 10 punti per la prima visualizzazione del prodotto
* 5 punti per ogni visualizzazione successiva
* Alla fine della sessione tutti i valori vengono divisi per 2

Ad esempio, la visualizzazione di “tavola da surf A” e poi di “tavola da surf B” in una sessione restituisce come risultato A: 10, B: 5. Al termine della sessione, avrai A: 5, B: 2.5. Se visualizzi gli stessi elementi nella sessione successiva, i valori diventano A: 15 B: 7.5.

Utilizza questo algoritmo nelle pagine generali, ad esempio home page o pagine di destinazione e annunci offsite.

### Più visualizzati per categoria {#most-viewed-category}

Il consiglio è determinato dalla categoria destinataria della maggioranza dell&#39;attività, con lo stesso metodo utilizzato per “articolo più visualizzato”, il punteggio però viene attribuito alle categorie anziché ai prodotti.

Tale metodo si basa sul criterio di attualità/frequenza, che si comporta come segue:

* 10 punti per la prima visualizzazione della categoria
* 5 punti per ogni visualizzazione successiva

Alle categorie visitate per la prima volta sono attribuiti 10 punti. Per le visite successive alla stessa categoria sono attribuiti 5 punti. A ogni visita, viene sottratto 1 punto alle categorie non correnti che sono state visualizzate in precedenza.

Ad esempio, la visualizzazione di “Categoria A” e poi di “Categoria B” in una sessione restituisce come risultato A: 9, B: 10. Se si visualizzano gli stessi elementi nella sessione successiva, i valori cambiano in A: 20, B: 9.

Utilizza questo algoritmo nelle pagine generali, ad esempio home page o pagine di destinazione e annunci offsite.

Se selezioni l’algoritmo Più visualizzato per categoria, puoi selezionare le seguenti chiavi di consigli:

* Categoria corrente
* Categoria preferita

### Più visualizzati per attributo articolo

Consiglia elementi o file multimediali simili a quelli più visualizzati sul sito.

Questo algoritmo consente di selezionare l’attributo dell’elemento su cui basare il consiglio, ad esempio &quot;Nome&quot; o &quot;Marchio&quot;.

Quindi seleziona gli attributi di profilo memorizzati nel profilo del visitatore da associare, ad esempio &quot;Marchio preferito&quot;, &quot;Ultimo elemento aggiunto al carrello&quot; o &quot;Spettacolo più visualizzato&quot;.

### Articoli più venduti in tutto il sito {#top-sellers}

Visualizza gli articoli inclusi nel maggior numero di ordini completati dall&#39;interno del sito. Più unità dello stesso articolo in un unico ordine vengono conteggiate come un ordine.

Questo algoritmo consente di creare consigli per gli articoli più venduti sul sito per aumentare la conversione e i ricavi. Questa logica è particolarmente adatta per i nuovi visitatori del sito.

### Articoli più venduti per categoria

Visualizza gli articoli inclusi nel maggior numero di ordini completati per categoria. Più unità dello stesso articolo in un unico ordine vengono conteggiate come un ordine.

Questo algoritmo ti consente di creare consigli per gli articoli più venduti sul sito in base alla categoria, per aumentare la conversione e i ricavi. Questa logica è particolarmente adatta per i nuovi visitatori del sito.

Se selezioni l’algoritmo Più visualizzato per categoria, puoi selezionare le seguenti chiavi di consigli:

* Categoria corrente
* Categoria preferita

### Attributo Articoli più venduti

Consiglia articoli o supporti simili a quelli acquistati di più sul sito.

Questo algoritmo consente di selezionare l’attributo dell’elemento su cui basare il consiglio, ad esempio &quot;Nome&quot; o &quot;Marchio&quot;.

Quindi seleziona gli attributi di profilo memorizzati nel profilo del visitatore da associare, ad esempio &quot;Marchio preferito&quot;, &quot;Ultimo elemento aggiunto al carrello&quot; o &quot;Spettacolo più visualizzato&quot;.

### Primi per metrica di Analytics

Visualizza la &quot;X superiore&quot; in cui *x* è una metrica [!DNL Analytics] arbitraria. Quando utilizzi dati comportamentali da mbox, puoi utilizzare i più venduti o i più visualizzati (x = &quot;venduti&quot; o x = &quot;visualizzati&quot;). Se utilizzi dati comportamentali di [!DNL Adobe Analytics], puoi utilizzare x = &quot;Aggiunte al carrello&quot; o un&#39;altra metrica [!DNL Analytics].

## [!UICONTROL Item-Based]

Il tipo di consiglio [!UICONTROL Item-Based] ti consente di formulare consigli in base alla ricerca di elementi simili a quelli di un elemento attualmente visualizzato dall&#39;utente o che è stato visualizzato di recente.

Con il tipo di algoritmo [!UICONTROL Item-Based] sono disponibili i seguenti algoritmi:

### Chi ha visualizzato questo ha visualizzato anche quello {#viewed-viewed}

Consiglia gli elementi che vengono visualizzati più spesso nella stessa sessione in cui viene visualizzato l’elemento specificato.

Questa logica restituisce altri prodotti visualizzati dopo aver visualizzato questo; il prodotto specificato non è incluso nel set di risultati.

Questa logica consente di creare opportunità di conversione aggiuntive consigliando gli articoli visualizzati anche dagli altri visitatori che hanno visualizzato un articolo. Ad esempio, i visitatori che visualizzano le bici da strada sul sito potrebbero anche guardare caschi, kit per ciclismo, serrature e così via. Utilizzando questa logica, puoi creare un consiglio che suggerisca ad altri prodotti di aiutarti ad aumentare i ricavi.

Se selezioni questo algoritmo, puoi selezionare le seguenti Chiavi consigli:

* Elemento corrente
* Ultimo articolo acquistato
* Ultimo articolo visualizzato
* Articolo più visualizzato

### Chi ha visualizzato questo ha acquistato anche quello {#viewed-bought}

Consiglia gli articoli che vengono acquistati più spesso nella stessa sessione in cui viene visualizzato l’articolo specificato. Questo criterio restituisce gli altri prodotti acquistati dopo la visualizzazione dell’articolo corrente; il prodotto specificato non è incluso nell’insieme di risultati.

Questa logica restituisce altri prodotti acquistati dopo aver visualizzato questo; il prodotto specificato non è incluso nel set di risultati.

Questa logica consente di aumentare le opportunità di cross-selling visualizzando un consiglio in una pagina di prodotto, ad esempio, in cui vengono visualizzati gli articoli acquistati da altri visitatori. Ad esempio, se il visitatore visualizza un palo da pesca, il consiglio potrebbe mostrare altri elementi acquistati da altri visitatori, come scatole per placcaggi, trampolieri e esche per pesca. Man mano che i visitatori navigano nel tuo sito, fornisci loro ulteriori consigli di acquisto.

Se selezioni questo algoritmo, puoi selezionare le seguenti Chiavi consigli:

* Elemento corrente
* Ultimo articolo acquistato
* Ultimo articolo visualizzato
* Articolo più visualizzato

### Chi ha comprato questo ha acquistato anche quello {#bought-bought}

Consiglia gli articoli che sono acquistati più spesso dai clienti contemporaneamente all’articolo specificato.

Questa logica restituisce altri prodotti acquistati dopo l’acquisto di questo; il prodotto specificato non è incluso nel set di risultati.

Questa logica ti consente di aumentare le opportunità di cross-selling visualizzando un consiglio in una pagina di riepilogo del carrello, ad esempio, in cui vengono visualizzati gli articoli acquistati anche da altri acquirenti. Ad esempio, se il visitatore acquista un completo, il consiglio potrebbe mostrare altri articoli acquistati da altri visitatori insieme all’indumento, come cravatte, scarpe e gemelli. Man mano che i visitatori esaminano i loro acquisti, fornisci loro ulteriori consigli.

Se selezioni questo algoritmo, puoi selezionare le seguenti Chiavi consigli:

* Elemento corrente
* Ultimo articolo acquistato
* Ultimo articolo visualizzato
* Articolo più visualizzato

### Articoli con attributi simili {#similar-attributes}

Consiglia articoli o media simili in base all’attività corrente o al comportamento passato del visitatore.

Se selezioni Articoli/Media con attributi simili, puoi impostare le regole di somiglianza del contenuto.

L’utilizzo di somiglianze di contenuti per generare consigli è particolarmente efficace per i nuovi elementi, che probabilmente non verranno visualizzati nei consigli utilizzando Persone che hanno visualizzato questo, Visualizzato quello e altre logiche basate sul comportamento passato. È inoltre possibile utilizzare la somiglianza del contenuto per generare consigli utili per i nuovi visitatori, che non hanno effettuato acquisti in precedenza o non possiedono altri dati storici.

Se selezioni questo algoritmo, puoi selezionare le seguenti Chiavi consigli:

* Elemento corrente
* Ultimo articolo acquistato
* Ultimo articolo visualizzato
* Articolo più visualizzato

Per ulteriori informazioni, vedere [Somiglianza contenuto](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#similarity).

## [!UICONTROL User-Based]

Il tipo di algoritmo basato sull’utente consente di formulare consigli in base al comportamento dell’utente.

Con il tipo di algoritmo [!UICONTROL User-Based] sono disponibili i seguenti algoritmi:

### Articoli visualizzati di recente {#recently-viewed}

Utilizza la cronologia del visitatore (nell&#39;arco delle sessioni) per presentare gli ultimi elementi *x* visualizzati, in base al numero di posizioni nella progettazione.

L&#39;algoritmo Elementi visualizzati di recente restituisce un risultato specifico per un determinato [ambiente](/help/main/administrating-target/hosts.md). Se due siti appartengono ad ambienti diversi e un visitatore passa da un sito all’altro, ciascun sito mostra solo gli articoli visualizzati di recente per il sito appropriato. Se due siti si trovano nello stesso ambiente e un visitatore passa da un sito all’altro, il visitatore visualizza gli stessi elementi visualizzati di recente per entrambi i siti.

>[!NOTE]
>
>Impossibile utilizzare i criteri [!UICONTROL Recently Viewed Items] per i consigli di backup.

È possibile filtrare [!UICONTROL Recently Viewed Items]/Media in modo che vengano visualizzati solo gli elementi con un attributo specifico.

* I criteri “visualizzati di recente” sono configurabili, come altri criteri nei consigli.
* Puoi utilizzare [raccolte](/help/main/c-recommendations/c-products/collections.md), [esclusioni](/help/main/c-recommendations/c-products/exclusions.md) e [inclusioni](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) (incluse le regole speciali per Prezzo e Inventario) allo stesso modo di qualsiasi altro criterio.

I possibili casi d’uso includono: un’azienda multinazionale con più aziende potrebbe avere un visitatore che visualizza gli articoli in più proprietà digitali. In questo caso, puoi limitare gli articoli visualizzati di recente al solo sito su cui sono stati visualizzati. Questo impedisce la visualizzazione degli elementi visualizzati di recente sul sito di un’altra proprietà digitale.

Utilizza questo algoritmo nelle pagine generali, ad esempio home page o pagine di destinazione e annunci offsite.

>[!NOTE]
>
>[!UICONTROL Recently Viewed Items] rispetta sia le impostazioni globali di esclusione che l&#39;impostazione di raccolta selezionata per l&#39;attività. Se un elemento è escluso da un’esclusione globale o non è contenuto nella raccolta selezionata, non verrà visualizzato. Pertanto, quando si utilizza un criterio [!UICONTROL Recently Viewed Items], in genere deve essere utilizzata l&#39;impostazione &quot;All Collections&quot;.

### Consigliato per te {#recommended-for-you}

Consiglia gli articoli in base alla cronologia di navigazione, visualizzazione e acquisto di ogni visitatore.

Questo algoritmo ti consente di fornire contenuti ed esperienze personalizzati sia ai visitatori nuovi che a quelli di ritorno. L’elenco dei consigli è ponderato rispetto all’attività più recente del visitatore, viene aggiornato durante la sessione e diventa più personalizzato man mano che l’utente naviga sul sito.

Sia le visualizzazioni che gli acquisti vengono utilizzati per determinare gli articoli consigliati. La chiave di consiglio specificata (ad esempio, Elemento corrente) viene utilizzata per applicare tutti i filtri selezionati per le regole di inclusione.

Sarà possibile, ad esempio:

* Escludi gli articoli che non soddisfano determinati criteri (prodotti esauriti, articoli pubblicati più di 30 giorni fa, film classificati R e così via).
* Limita gli elementi inclusi a una singola categoria o alla categoria corrente.

Se si seleziona questo algoritmo, è possibile selezionare le seguenti chiavi di filtro:

* Elemento corrente
* Ultimo articolo acquistato
* Ultimo articolo visualizzato
* Articolo più visualizzato

## Criteri personalizzati {#custom}

Il tipo di algoritmo Criteri personalizzati consente di formulare consigli in base a un file personalizzato caricato.

Il consiglio è determinato da un elemento memorizzato nel profilo di un visitatore, utilizzando uno degli utenti.*x* o profilo.Attributi *x*.

Quando questa opzione è selezionata, il valore `entity.id` deve essere presente nell&#39;attributo profilo.

Quando basi i consigli su attributi personalizzati, seleziona l&#39;attributo personalizzato, quindi il tipo di consiglio.

Puoi eseguire il filtro in tempo reale all&#39;inizio dell&#39;output di criteri personalizzati. Ad esempio, puoi limitare gli articoli consigliati a quelli della categoria o del marchio preferito dal visitatore. Così puoi combinare calcoli offline e filtri in tempo reale.

Questa funzionalità consente di utilizzare [!DNL Target] per aggiungere la personalizzazione ai consigli calcolati offline o agli elenchi personalizzati. Permette infatti di unire le compenze del personale addetto ai dati alle tecnonologie comprovate di Adobe per la distribuzione, l&#39;applicazione di filtri al momento dell&#39;esecuzione, i test A/B, il targeting, la generazione di rapporti, le integrazioni e altro.

Con l’aggiunta delle regole di inclusione ai Criteri personalizzati, i consigli non sono più statici ma diventano dinamici, in base agli interessi del visitatore.

* I criteri personalizzati sono configurabili, come altri criteri nei consigli.
* Puoi utilizzare [raccolte](/help/main/c-recommendations/c-products/collections.md), [esclusioni](/help/main/c-recommendations/c-products/exclusions.md) e [inclusioni](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) (incluse le regole speciali per Prezzo e Inventario) allo stesso modo di qualsiasi altro criterio.

Eventuali casi di utilizzo includono:

* Vuoi consigliare film da una lista personalizzata, ma solo se il visitatore non li ha già guardati.
* Desideri eseguire un algoritmo offline e utilizzare i risultati per alimentare i consigli, ma devi assicurarti che gli elementi esauriti non vengano mai consigliati.
* Vuoi includere solo gli articoli appartenenti alla categoria preferita del visitatore.

## Chiavi consiglio {#keys}

Le seguenti chiavi di consigli sono disponibili dall&#39;elenco a discesa [!UICONTROL Recommendation Key]:

### Elemento corrente {#current-item}

Il consiglio è determinato dall&#39;elemento attualmente visualizzato dal visitatore.

Il consiglio visualizzano altri elementi che potrebbero interessare i visitatori interessati all&#39;elemento specificato.

Quando questa opzione è selezionata, il valore `entity.id` deve essere trasmesso come parametro alla mbox di visualizzazione.

Può essere utilizzato con i seguenti algoritmi:

* [!UICONTROL Items with similar attributes]
* [!UICONTROL People Who Viewed This, Viewed That]
* [!UICONTROL People Who Viewed This, Bought That]
* [!UICONTROL People Who Bought This, Bought That]

Utilizza la chiave di consigli [!UICONTROL Current Item] sul tuo sito su:

* Pagine a elemento singolo, ad esempio le pagine del prodotto.
* NON utilizzare nelle pagine dei risultati di ricerca nulli.

### Ultimo articolo acquistato {#last-purchased}

Il consiglio è determinato in base all&#39;ultimo articolo acquistato da ogni visitatore univoco. Questo viene acquisito automaticamente, quindi non è necessario trasmettere valori sulla pagina.

Può essere utilizzato con i seguenti algoritmi:

* [!UICONTROL Items with similar attributes]
* [!UICONTROL People Who Viewed This, Viewed That]
* [!UICONTROL People Who Viewed This, Bought That]
* [!UICONTROL People Who Bought This, Bought That]

Utilizza la chiave di consigli [!UICONTROL Last Purchased Item] sul tuo sito su:

* Pagina principale, pagina account, annunci fuori sede.
* NON utilizzare su pagine di prodotti o pagine rilevanti per gli acquisti.

#### Chiave consigli personalizzata

Puoi basare i consigli sul valore di un attributo di profilo personalizzato. Ad esempio, supponi di voler visualizzare filmati consigliati in base all’ultimo filmato che un visitatore ha aggiunto alla sua coda.

1. Selezionare l&#39;attributo di profilo personalizzato dall&#39;elenco a discesa **[!UICONTROL Recommendation Key]**, ad esempio &quot;Ultimo filmato aggiunto alla watchlist&quot;.
1. Quindi seleziona **[!UICONTROL Recommendation Logic]** (ad esempio &quot;Persone che hanno visualizzato questo, hanno visualizzato anche quello&quot;).

   ![Finestra di dialogo per creare un nuovo criterio](/help/main/c-recommendations/c-algorithms/assets/create-new-criteria-1.png)

Se l’attributo di profilo personalizzato non corrisponde direttamente a un singolo ID entità, devi spiegare a [!DNL Recommendations] come desideri che avvenga la corrispondenza a un’entità. Ad esempio, supponi di voler visualizzare gli articoli più venduti della marca preferita di un visitatore.

1. Selezionare l&#39;attributo di profilo personalizzato dall&#39;elenco a discesa **[!UICONTROL Recommendation Key]**, ad esempio &quot;Marchio preferito&quot;.

1. Quindi seleziona **[!UICONTROL Recommendation Logic]** da utilizzare con questa chiave (ad esempio, &quot;Più venduti&quot;).

   Viene visualizzata l&#39;opzione [!UICONTROL Group By Unique Value Of].

1. Seleziona l’attributo di entità che corrisponde alla chiave scelta. In questo caso &quot;Marchio preferito&quot; corrisponde a `entity.brand`.

   [!DNL Recommendations] genera ora un elenco &quot;Più venduti&quot; per ogni marchio e mostra al visitatore l&#39;elenco &quot;Più venduti&quot; appropriato in base al valore memorizzato nell&#39;attributo di profilo Marchio preferito del visitatore.

   ![Finestra di dialogo per creare un nuovo criterio 2](/help/main/c-recommendations/c-algorithms/assets/create-new-criteria-2.png)

### Ultimo articolo visualizzato {#last-viewed}

Il consiglio è determinato dall&#39;ultimo articolo visualizzato da ogni visitatore univoco. Questo viene acquisito automaticamente, quindi non è necessario trasmettere valori sulla pagina.

Può essere utilizzato con i seguenti algoritmi:

* [!UICONTROL Items with similar attributes]
* [!UICONTROL People Who Viewed This, Viewed That]
* [!UICONTROL People Who Viewed This, Bought That]
* [!UICONTROL People Who Bought This, Bought That]

Utilizza la chiave di consigli [!UICONTROL Last Viewed Item] sul tuo sito su:

* Pagina principale, pagina account, annunci fuori sede.
* NON utilizzare su pagine di prodotti o pagine rilevanti per gli acquisti.

### Articolo più visualizzato {#most-viewed-logic}

Visualizza gli elementi o i supporti visualizzati più di frequente sul sito.

Questa logica consente di visualizzare i consigli in base agli elementi più visualizzati sul sito per aumentare le conversioni per altri elementi. Ad esempio, un sito di contenuti multimediali potrebbe mostrare nella propria home page i consigli per i video più visualizzati, in modo da incoraggiare i visitatori a guardare altri video.

Questa chiave di consigli può essere utilizzata con i seguenti algoritmi:

* [!UICONTROL Items with similar attributes]
* [!UICONTROL People Who Viewed This, Viewed That]
* [!UICONTROL People Who Viewed This, Bought That]
* [!UICONTROL People Who Bought This, Bought That]

### Categoria corrente {#current-category}

Il consiglio è determinato dalla categoria di prodotto attualmente visualizzata dal visitatore.

I consigli mostrano gli elementi nella categoria di prodotto specificata.

Quando questa opzione è selezionata, il valore `entity.categoryId` deve essere trasmesso come parametro alla mbox di visualizzazione.

Questa chiave di consigli può essere utilizzata con i seguenti algoritmi:

* Articoli più venduti
* Articoli più visualizzati

Utilizza la chiave di consigli [!UICONTROL Current Category] sul tuo sito su:

* Pagine a categoria singola.
* NON utilizzare nelle pagine dei risultati di ricerca nulli.

### Categoria preferita {#favorite-category}

Il consiglio è determinato dalla categoria di prodotto preferita del visitatore.

I consigli mostrano gli elementi nella categoria di prodotto specificata.

Quando questa opzione è selezionata, il valore `entity.categoryId` deve essere trasmesso come parametro alla mbox di visualizzazione.

Questa chiave di consigli può essere utilizzata con i seguenti algoritmi:

* Articoli più venduti
* Articoli più visualizzati

Utilizza la chiave di consigli [!UICONTROL Current Category] sul tuo sito su:

* Pagine a categoria singola.
* NON utilizzare nelle pagine dei risultati di ricerca nulli.

### Affinità sito {#site-affinity}

Consiglia gli articoli in base alla certezza di una relazione tra articoli diversi. Puoi configurare questo criterio per determinare la quantità di dati necessari prima che venga presentato un consiglio utilizzando il cursore delle Regole di inclusione. Ad esempio, se selezioni molto forte, vengono consigliati i prodotti con la maggiore certezza di corrispondenza.

Ad esempio, se imposti un’affinità molto forte e il progetto include cinque elementi, tre dei quali soddisfano il livello di soglia di connessione, i due elementi che non soddisfano i requisiti di forza minima non vengono visualizzati nei suggerimenti e vengono sostituiti dagli elementi di backup definiti. Gli elementi con affinità più elevata vengono visualizzati per primi.

Ad esempio, un retailer online può consigliare gli elementi nelle visite successive a cui un visitatore ha mostrato interesse durante le sessioni precedenti. L’attività per ogni sessione del visitatore viene acquisita per calcolare un’affinità in base a un modello di frequenza e recency. Quando il visitatore ritorna sul sito, l’affinità viene utilizzata per visualizzare i consigli in base alle azioni passate eseguite sul sito.

Alcuni clienti con varie raccolte di prodotti e comportamenti diversi sui siti potrebbero ottenere risultati ottimali impostando un’affinità di sito debole.

Questa logica può essere utilizzata con le seguenti chiavi di consigli:

* Elemento corrente
* Ultimo articolo acquistato
* Ultimo articolo visualizzato
* Articolo più visualizzato
