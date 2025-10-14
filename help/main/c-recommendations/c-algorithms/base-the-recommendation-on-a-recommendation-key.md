---
keywords: chiave consigli;logica consigli;categoria corrente;attributo personalizzato;ultimo articolo acquistato;ultimo articolo visualizzato;articolo più visualizzato;articolo più visualizzato;categoria preferita;popolarità;articolo visualizzato di recente;ultimo articolo acquistato;più visualizzato;preferito;visualizzato di recente
description: Scopri come utilizzare i consigli basati su chiavi che utilizzano il contesto del comportamento del visitatore per mostrare risultati rilevanti nelle attività [!UICONTROL Recommendations].
title: Come si basa [!UICONTROL Recommendation] su [!UICONTROL Recommendation Key]?
feature: Recommendations
mini-toc-levels: 2
exl-id: 49764f18-88fb-41be-b2a0-e7ced9de742c
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '3463'
ht-degree: 27%

---

# Basare il consiglio su una chiave consiglio

I consigli basati su algoritmi utilizzano il contesto del comportamento del visitatore per mostrare risultati rilevanti nelle attività [!DNL Adobe Target] [!DNL Recommendations].

Ogni tipo di algoritmo fornisce diversi algoritmi appropriati al proprio tipo, come illustrato nella tabella seguente:

| Tipo di algoritmo | Quando utilizzare / Algoritmi disponibili |
| --- | --- |
| [!UICONTROL Cart-Based] | Creare consigli in base al contenuto del carrello dell’utente.<ul><li>[!UICONTROL People Who Viewed These, Also Viewed]</li><li>[!UICONTROL People Who Viewed These, Also Bought]</li><li>[!UICONTROL People Who Bought These, Also Bought]</li></ul> |
| [!UICONTROL Popularity-Based] | Puoi formulare raccomandazioni in base alla popolarità complessiva di un elemento nel tuo sito o in base alla popolarità degli elementi nella categoria, nel brand, nel genere e così via preferiti o più visualizzati di un utente. <ul><li>[!UICONTROL Most Viewed Across the Site]</li><li>[!UICONTROL Most Viewed by Category]</li><li>[!UICONTROL Most Viewed by Item Attribute]</li><li>[!UICONTROL Top Sellers Across the Site]</li><li>[!UICONTROL Top Sellers by Category]</li><li>[!UICONTROL Top Sellers by Item Attribute]</li><li>[!UICONTROL Top by Analytics Metric]</li></ul> |
| [!UICONTROL Item-Based] | Creare consigli in base alla ricerca di elementi simili a quelli di un elemento attualmente visualizzato dall’utente o che è stato recentemente visualizzato. <ul><li>[!UICONTROL People Who Viewed This, Viewed That]</li><li>[!UICONTROL People Who Viewed This, Bought That]</li><li>[!UICONTROL People Who Bought This, Bought That]</li><li>[!UICONTROL Items with Similar Attributes]</li></ul> |
| [!UICONTROL User-Based] | Creare consigli in base al comportamento dell’utente. <ul><li>[!UICONTROL Recently Viewed Items]</li><li>[!UICONTROL Recommended for You]</li></ul> |
| [!UICONTROL Custom Criteria] | Formulare raccomandazioni in base a un file personalizzato caricato. <ul><li>Algoritmo personalizzato</li></ul> |

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

### [!UICONTROL People Who Viewed This, Also Viewed]

Consiglia gli elementi che vengono visualizzati più spesso nella stessa sessione in cui viene visualizzato l’elemento specificato.

Questa logica restituisce altri prodotti visualizzati dalle persone dopo aver visualizzato questo. Il prodotto specificato non è incluso nel set di risultati.

Questa logica consente di creare opportunità di conversione aggiuntive consigliando gli articoli visualizzati anche dagli altri visitatori che hanno visualizzato un articolo. Ad esempio, i visitatori che visualizzano le bici da strada sul sito potrebbero anche guardare caschi, kit per ciclismo, serrature e così via. Utilizzando questa logica, puoi creare un consiglio che suggerisca ad altri prodotti di aiutarti ad aumentare i ricavi.

Se selezioni questo algoritmo, puoi selezionare le seguenti Chiavi consigli:

* [!UICONTROL Current Item]
* [!UICONTROL Last Purchased Item]
* [!UICONTROL Last Viewed Item]
* [!UICONTROL Most Viewed Item]

### [!UICONTROL People Who Viewed This, Also Bought]

Consiglia gli articoli che vengono acquistati più spesso nella stessa sessione in cui viene visualizzato l’articolo specificato.

Questa logica restituisce altri prodotti che le persone hanno acquistato dopo aver visualizzato questo. Il prodotto specificato non è incluso nel set di risultati.

Questa logica consente di aumentare le opportunità di cross-selling visualizzando un consiglio in una pagina di prodotto, ad esempio, in cui vengono visualizzati gli articoli acquistati da altri visitatori. Ad esempio, se il visitatore visualizza un palo da pesca, il consiglio potrebbe mostrare altri elementi acquistati da altri visitatori, come scatole per placcaggi, trampolieri e esche per pesca. Man mano che i visitatori navigano nel tuo sito, fornisci loro ulteriori consigli di acquisto.

Se selezioni questo algoritmo, puoi selezionare le seguenti Chiavi consigli:

* [!UICONTROL Current Item]
* [!UICONTROL Last Purchased Item]
* [!UICONTROL Last Viewed Item]
* [!UICONTROL Most Viewed Item]

### [!UICONTROL People Who Bought This, Also Bought]

Consiglia gli articoli che sono acquistati più spesso dai clienti contemporaneamente all’articolo specificato.

Questa logica restituisce altri prodotti acquistati dopo l’acquisto di questo. Il prodotto specificato non è incluso nel set di risultati.

Questa logica ti consente di aumentare le opportunità di cross-selling visualizzando un consiglio in una pagina di riepilogo del carrello, ad esempio, in cui vengono visualizzati gli articoli acquistati anche da altri acquirenti. Ad esempio, se il visitatore acquista un completo, il consiglio potrebbe mostrare altri articoli acquistati da altri visitatori insieme all’indumento, come cravatte, scarpe e gemelli. Man mano che i visitatori esaminano i loro acquisti, fornisci loro ulteriori consigli.

Se selezioni questo algoritmo, puoi selezionare le seguenti Chiavi consigli:

* [!UICONTROL Current Item]
* [!UICONTROL Last Purchased Item]
* [!UICONTROL Last Viewed Item]
* [!UICONTROL Most Viewed Item]

## [!UICONTROL Popularity-Based]

Il tipo di algoritmo [!UICONTROL Popularity-Based] consente di formulare raccomandazioni in base alla popolarità complessiva di un elemento nel sito o in base alla popolarità degli elementi nella categoria, nel marchio, nel genere e così via preferiti o più visualizzati dell&#39;utente.

Con il tipo di algoritmo [!UICONTROL Popularity-Based] sono disponibili i seguenti algoritmi:

### [!UICONTROL Most Viewed Across the Site] {#most-viewed}

Il consiglio è determinato dall’elemento visualizzato più di frequente. Tale metodo si basa sul criterio di attualità/frequenza, che si comporta come segue:

* 10 punti per la prima visualizzazione del prodotto
* 5 punti per ogni visualizzazione successiva
* Alla fine della sessione tutti i valori vengono divisi per 2

Ad esempio, visualizzando la tavola da surf A e poi la tavola da surf B in una sessione si ottengono A: 10, B: 5. Al termine della sessione, avrai A: 5, B: 2.5. Se visualizzi gli stessi elementi nella sessione successiva, i valori diventano A: 15 B: 7.5.

Utilizza questo algoritmo nelle pagine generali, ad esempio home page o pagine di destinazione e annunci offsite.

### [!UICONTROL Most Viewed by Category] {#most-viewed-category}

Il consiglio è determinato dalla categoria destinataria della maggioranza dell&#39;attività, con lo stesso metodo utilizzato per “articolo più visualizzato”, il punteggio però viene attribuito alle categorie anziché ai prodotti.

Tale metodo si basa sul criterio di attualità/frequenza, che si comporta come segue:

* 10 punti per la prima visualizzazione della categoria
* 5 punti per ogni visualizzazione successiva

Alle categorie visitate per la prima volta sono attribuiti 10 punti. Per le visite successive alla stessa categoria sono attribuiti 5 punti. A ogni visita, viene sottratto 1 punto alle categorie non correnti che sono state visualizzate in precedenza.

Ad esempio, visualizzando la categoria A e la categoria B in una sessione si ottiene A: 9, B: 10. Se si visualizzano gli stessi elementi nella sessione successiva, i valori cambiano in A: 20, B: 9.

Utilizza questo algoritmo nelle pagine generali, ad esempio home page o pagine di destinazione e annunci offsite.

Se selezioni l’algoritmo Più visualizzato per categoria, puoi selezionare le seguenti chiavi di consigli:

* [!UICONTROL Current Category]
* [!UICONTROL Favorite Category]

### [!UICONTROL Most Viewed by Item Attribute]

Consiglia elementi o file multimediali simili a quelli più visualizzati sul sito.

Questo algoritmo consente di selezionare l’attributo dell’elemento su cui basare il consiglio, ad esempio &quot;Nome&quot; o &quot;Marchio&quot;.

Quindi seleziona gli attributi di profilo memorizzati nel profilo del visitatore da associare, ad esempio &quot;Marchio preferito&quot;, &quot;Ultimo elemento aggiunto al carrello&quot; o &quot;Spettacolo più visualizzato&quot;.

### [!UICONTROL Top Sellers Across the Site] {#top-sellers}

Visualizza gli articoli inclusi nel maggior numero di ordini completati dall&#39;interno del sito. Più unità dello stesso articolo in un unico ordine vengono conteggiate come un ordine.

Questo algoritmo consente di creare consigli per gli articoli più venduti sul sito per aumentare la conversione e i ricavi. Questa logica è particolarmente adatta per i nuovi visitatori del sito.

### [!UICONTROL Top Sellers by Category]

Visualizza gli articoli inclusi nel maggior numero di ordini completati per categoria. Più unità dello stesso articolo in un unico ordine vengono conteggiate come un ordine.

Questo algoritmo ti consente di creare consigli per gli articoli più venduti sul sito in base alla categoria, per aumentare la conversione e i ricavi. Questa logica è particolarmente adatta per i nuovi visitatori del sito.

Se si seleziona l&#39;algoritmo [!UICONTROL Most Viewed by Category], è possibile selezionare [!UICONTROL Recommendations Keys]:

* [!UICONTROL Current Category]
* [!UICONTROL Favorite Category]

### [!UICONTROL Top Sellers by Item Attribute]

Consiglia articoli o supporti simili a quelli acquistati di più sul sito.

Questo algoritmo consente di selezionare l’attributo dell’elemento su cui basare il consiglio, ad esempio &quot;Nome&quot; o &quot;Marchio&quot;.

Quindi seleziona gli attributi di profilo memorizzati nel profilo del visitatore da associare, ad esempio &quot;Marchio preferito&quot;, &quot;Ultimo elemento aggiunto al carrello&quot; o &quot;Spettacolo più visualizzato&quot;.

### [!UICONTROL Top by Analytics Metric]

Visualizza la &quot;X superiore&quot; in cui *x* è una metrica [!DNL Analytics] arbitraria. Quando si utilizzano dati comportamentali da mbox, è possibile utilizzare [!UICONTROL Top Sold] o [!UICONTROL Top Viewed] (x = &quot;Venduto&quot; o x = &quot;Visualizzato&quot;). Se utilizzi dati comportamentali di [!DNL Adobe Analytics], puoi utilizzare x = &quot;Aggiunte al carrello&quot; o un&#39;altra metrica [!DNL Analytics].

## [!UICONTROL Item-Based]

Il tipo di consiglio [!UICONTROL Item-Based] ti consente di formulare consigli in base alla ricerca di elementi simili a quelli di un elemento attualmente visualizzato dall&#39;utente o che è stato visualizzato di recente.

Con il tipo di algoritmo [!UICONTROL Item-Based] sono disponibili i seguenti algoritmi:

### [!UICONTROL People Who Viewed This, Viewed That] {#viewed-viewed}

Consiglia gli elementi che vengono visualizzati più spesso nella stessa sessione in cui viene visualizzato l’elemento specificato.

Questa logica restituisce altri prodotti visualizzati dopo aver visualizzato questo; il prodotto specificato non è incluso nel set di risultati.

Questa logica consente di creare opportunità di conversione aggiuntive consigliando gli articoli visualizzati anche dagli altri visitatori che hanno visualizzato un articolo. Ad esempio, i visitatori che visualizzano le bici da strada sul sito potrebbero anche guardare caschi, kit per ciclismo, serrature e così via. Utilizzando questa logica, puoi creare un consiglio che suggerisca ad altri prodotti di aiutarti ad aumentare i ricavi.

Se si seleziona questo algoritmo, è possibile selezionare [!UICONTROL Recommendations Keys]:

* [!UICONTROL Current Item]
* [!UICONTROL Last Purchased Item]
* [!UICONTROL Last Viewed Item]
* [!UICONTROL Most Viewed Item]

### [!UICONTROL People Who Viewed This, Bought That] {#viewed-bought}

Consiglia gli articoli che vengono acquistati più spesso nella stessa sessione in cui viene visualizzato l’articolo specificato. Questo criterio restituisce gli altri prodotti acquistati dopo la visualizzazione dell’articolo corrente; il prodotto specificato non è incluso nell’insieme di risultati.

Questa logica restituisce altri prodotti acquistati dopo aver visualizzato questo; il prodotto specificato non è incluso nel set di risultati.

Questa logica consente di aumentare le opportunità di cross-selling visualizzando un consiglio in una pagina di prodotto, ad esempio, in cui vengono visualizzati gli articoli acquistati da altri visitatori. Ad esempio, se il visitatore visualizza un palo da pesca, il consiglio potrebbe mostrare altri elementi acquistati da altri visitatori, come scatole per placcaggi, trampolieri e esche per pesca. Man mano che i visitatori navigano nel tuo sito, fornisci loro ulteriori consigli di acquisto.

Se si seleziona questo algoritmo, è possibile selezionare [!UICONTROL Recommendations Keys]:

* [!UICONTROL Current Item]
* [!UICONTROL Last Purchased Item]
* [!UICONTROL Last Viewed Item]
* [!UICONTROL Most Viewed Item]

### [!UICONTROL People Who Bought This, Bought That] {#bought-bought}

Consiglia gli articoli che sono acquistati più spesso dai clienti contemporaneamente all’articolo specificato.

Questa logica restituisce altri prodotti acquistati dopo l’acquisto di questo. Il prodotto specificato non è incluso nel set di risultati.

Questa logica ti consente di aumentare le opportunità di cross-selling visualizzando un consiglio in una pagina di riepilogo del carrello, ad esempio, in cui vengono visualizzati gli articoli acquistati anche da altri acquirenti. Ad esempio, se il visitatore acquista un completo, il consiglio potrebbe mostrare altri articoli acquistati da altri visitatori insieme all’indumento, come cravatte, scarpe e gemelli. Man mano che i visitatori esaminano i loro acquisti, fornisci loro ulteriori consigli.

Se si seleziona questo algoritmo, è possibile selezionare [!UICONTROL Recommendations Keys]:

* [!UICONTROL Current Item]
* [!UICONTROL Last Purchased Item]
* [!UICONTROL Last Viewed Item]
* [!UICONTROL Most Viewed Item]

### [!UICONTROL Items with Similar Attributes] {#similar-attributes}

Consiglia articoli o media simili in base all’attività corrente o al comportamento passato del visitatore.

Se si seleziona [!UICONTROL Items with Similar Attributes] o [!UICONTROL Media with Similar Attributes], è possibile impostare le regole di somiglianza del contenuto.

L&#39;utilizzo di somiglianze di contenuto per generare consigli è particolarmente efficace per i nuovi elementi, che probabilmente non verranno visualizzati nei consigli utilizzando [!UICONTROL People Who Viewed This], [!UICONTROL Viewed That] e altra logica basata sui comportamenti passati. È inoltre possibile utilizzare la somiglianza del contenuto per generare consigli utili per i nuovi visitatori, che non hanno effettuato acquisti in precedenza o non possiedono altri dati storici.

Se si seleziona questo algoritmo, è possibile selezionare [!UICONTROL Recommendations Keys]:

* [!UICONTROL Current Item]
* [!UICONTROL Last Purchased Item]
* [!UICONTROL Last Viewed Item]
* [!UICONTROL Most Viewed Item]

Per ulteriori informazioni, vedere [Somiglianza contenuto](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#similarity).

## [!UICONTROL User-Based]

Il tipo di algoritmo [!UICONTROL User-Based] consente di formulare raccomandazioni in base al comportamento dell&#39;utente.

Con il tipo di algoritmo [!UICONTROL User-Based] sono disponibili i seguenti algoritmi:

### [!UICONTROL Recently Viewed Items] {#recently-viewed}

Utilizza la cronologia del visitatore (nell&#39;arco delle sessioni) per presentare gli ultimi elementi *x* visualizzati, in base al numero di posizioni nella progettazione.

L&#39;algoritmo [!UICONTROL Recently Viewed Items] restituisce un risultato specifico per un dato [ambiente](/help/main/administrating-target/hosts.md). Se due siti appartengono ad ambienti diversi e un visitatore passa da un sito all’altro, ciascun sito mostra solo gli articoli visualizzati di recente per il sito appropriato. Se due siti si trovano nello stesso ambiente e un visitatore passa da un sito all’altro, il visitatore visualizza gli stessi elementi visualizzati di recente per entrambi i siti.

>[!NOTE]
>
>Impossibile utilizzare i criteri [!UICONTROL Recently Viewed Items] per i consigli di backup.

È possibile filtrare [!UICONTROL Recently Viewed Items] o [!UICONTROL Recently Viewed Media] in modo che vengano visualizzati solo gli elementi con un attributo specifico.

* I criteri [!UICONTROL Recently Viewed] sono configurabili, come altri criteri nei consigli.
* Puoi utilizzare [raccolte](/help/main/c-recommendations/c-products/collections.md), [esclusioni](/help/main/c-recommendations/c-products/exclusions.md) e [inclusioni](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) (incluse le regole speciali per Prezzo e Inventario) allo stesso modo di qualsiasi altro criterio.

I possibili casi d’uso includono: un’azienda multinazionale con più aziende potrebbe avere un visitatore che visualizza gli articoli in più proprietà digitali. In questo caso, puoi limitare gli articoli visualizzati di recente al solo sito su cui sono stati visualizzati. Questo impedisce la visualizzazione degli elementi visualizzati di recente sul sito di un’altra proprietà digitale.

Utilizza questo algoritmo nelle pagine generali, ad esempio home page o pagine di destinazione e annunci offsite.

>[!NOTE]
>
>[!UICONTROL Recently Viewed Items] rispetta sia le impostazioni globali di esclusione che l&#39;impostazione di raccolta selezionata per l&#39;attività. Se un elemento è escluso da un’esclusione globale o non è contenuto nella raccolta selezionata, non viene visualizzato. Pertanto, quando si utilizza un criterio [!UICONTROL Recently Viewed Items], in genere deve essere utilizzata l&#39;impostazione &quot;All Collections&quot;.

### [!UICONTROL Recommended for You] {#recommended-for-you}

Consiglia gli articoli in base alla cronologia di navigazione, visualizzazione e acquisto di ogni visitatore.

Questo algoritmo ti consente di fornire contenuti ed esperienze personalizzati sia ai visitatori nuovi che a quelli di ritorno. L’elenco dei consigli è ponderato rispetto all’attività più recente del visitatore, viene aggiornato durante la sessione e diventa più personalizzato man mano che l’utente naviga sul sito.

Sia le visualizzazioni che gli acquisti vengono utilizzati per determinare gli articoli consigliati. La chiave di consiglio specificata (ad esempio, [!UICONTROL Current Item]) viene utilizzata per applicare tutti i filtri selezionati per le regole di inclusione.

Sarà possibile, ad esempio:

* Escludi gli articoli che non soddisfano determinati criteri (prodotti esauriti, articoli pubblicati più di 30 giorni fa, film classificati R e così via).
* Limita gli elementi inclusi a una singola categoria o alla categoria corrente.

Se si seleziona questo algoritmo, è possibile selezionare le seguenti chiavi di filtro:

* [!UICONTROL Current Item]
* [!UICONTROL Last Purchased Item]
* [!UICONTROL Last Viewed Item]
* [!UICONTROL Most Viewed Item]

## Criteri personalizzati {#custom}

Il tipo di algoritmo [!UICONTROL Custom Criteria] ti consente di formulare raccomandazioni in base a un file personalizzato caricato.

Il consiglio è determinato da un elemento memorizzato nel profilo di un visitatore, utilizzando uno degli utenti.*x* o profilo.Attributi *x*.

Quando questa opzione è selezionata, il valore `entity.id` deve essere presente nell&#39;attributo profilo.

Quando basi i consigli su attributi personalizzati, seleziona l&#39;attributo personalizzato, quindi il tipo di consiglio.

Puoi eseguire il filtro in tempo reale all&#39;inizio dell&#39;output di criteri personalizzati. Ad esempio, puoi limitare gli articoli consigliati a quelli della categoria o del marchio preferito dal visitatore. Così puoi combinare calcoli offline e filtri in tempo reale.

Questa funzionalità consente di utilizzare [!DNL Target] per aggiungere la personalizzazione ai consigli calcolati offline o agli elenchi personalizzati. Permette infatti di unire le compenze del personale addetto ai dati alle tecnonologie comprovate di Adobe per la distribuzione, l&#39;applicazione di filtri al momento dell&#39;esecuzione, i test A/B, il targeting, la generazione di rapporti, le integrazioni e altro.

Con l&#39;aggiunta delle regole di inclusione in [!UICONTROL Custom Criteria], i consigli non sono più statici ma diventano dinamici, in base agli interessi del visitatore.

* I criteri personalizzati sono configurabili, come altri criteri nei consigli.
* Puoi utilizzare [raccolte](/help/main/c-recommendations/c-products/collections.md), [esclusioni](/help/main/c-recommendations/c-products/exclusions.md) e [inclusioni](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) (incluse le regole speciali per Prezzo e Inventario) allo stesso modo di qualsiasi altro criterio.

Eventuali casi di utilizzo includono:

* Vuoi consigliare film da una lista personalizzata, ma solo se il visitatore non li ha già guardati.
* Desideri eseguire un algoritmo offline e utilizzare i risultati per alimentare i consigli, ma devi assicurarti che gli elementi esauriti non vengano mai consigliati.
* Vuoi includere solo gli articoli appartenenti alla categoria preferita del visitatore.

## Chiavi consiglio {#keys}

Le seguenti chiavi di consigli sono disponibili dall&#39;elenco a discesa [!UICONTROL Recommendation Key]:

### [!UICONTROL Current Item] {#current-item}

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

### [!UICONTROL Last Purchased Item] {#last-purchased}

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

Puoi basare i consigli sul valore di un attributo di profilo personalizzato. Ad esempio, supponi di voler visualizzare filmati consigliati in base all’ultimo filmato aggiunto alla coda da un visitatore.

1. Selezionare l&#39;attributo di profilo personalizzato dall&#39;elenco a discesa **[!UICONTROL Recommendation Key]**, ad esempio &quot;[!UICONTROL Last Show Added to Watchlist]&quot;.
1. Selezionare quindi **[!UICONTROL Recommendation Logic]** (ad esempio &quot;[!UICONTROL People Who Viewed This, Viewed That]&quot;).

Se l’attributo di profilo personalizzato non corrisponde direttamente a un singolo ID entità, devi spiegare a [!DNL Recommendations] come desideri che avvenga la corrispondenza a un’entità. Ad esempio, supponi di voler visualizzare gli articoli più venduti della marca preferita di un visitatore.

1. Selezionare l&#39;attributo di profilo personalizzato dall&#39;elenco a discesa **[!UICONTROL Recommendation Key]**, ad esempio &quot;Marchio preferito&quot;.

1. Selezionare quindi **[!UICONTROL Recommendation Logic]** da utilizzare con questa chiave (ad esempio, &quot;[!UICONTROL Top Sellers]&quot;).

   Viene visualizzata l&#39;opzione [!UICONTROL Group By Unique Value Of].

1. Seleziona l’attributo di entità che corrisponde alla chiave scelta. In questo caso &quot;[!UICONTROL Favorite Brand]&quot; corrisponde a `entity.brand`.

   [!DNL Recommendations] ora genera un elenco &quot;[!UICONTROL Top Sellers]&quot; per ogni marchio e mostra al visitatore l&#39;elenco &quot;[!UICONTROL Top Sellers]&quot; appropriato in base al valore memorizzato nell&#39;attributo di profilo [!UICONTROL Favorite Brand] del visitatore.

### [!UICONTROL Last Viewed Item] {#last-viewed}

Il consiglio è determinato dall&#39;ultimo articolo visualizzato da ogni visitatore univoco. Questo viene acquisito automaticamente, quindi non è necessario trasmettere valori sulla pagina.

Può essere utilizzato con i seguenti algoritmi:

* [!UICONTROL Items with similar attributes]
* [!UICONTROL People Who Viewed This, Viewed That]
* [!UICONTROL People Who Viewed This, Bought That]
* [!UICONTROL People Who Bought This, Bought That]

Utilizza la chiave di consigli [!UICONTROL Last Viewed Item] sul tuo sito su:

* Pagina principale, pagina account, annunci fuori sede.
* NON utilizzare su pagine di prodotti o pagine rilevanti per gli acquisti.

### [!UICONTROL Most Viewed Item] {#most-viewed-logic}

Visualizza gli elementi o i supporti visualizzati più di frequente sul sito.

Questa logica consente di visualizzare i consigli in base agli elementi più visualizzati sul sito per aumentare le conversioni per altri elementi. Ad esempio, un sito di contenuti multimediali potrebbe mostrare nella propria home page i consigli per i video più visualizzati, in modo da incoraggiare i visitatori a guardare altri video.

Questa chiave di consigli può essere utilizzata con i seguenti algoritmi:

* [!UICONTROL Items with similar attributes]
* [!UICONTROL People Who Viewed This, Viewed That]
* [!UICONTROL People Who Viewed This, Bought That]
* [!UICONTROL People Who Bought This, Bought That]

### [!UICONTROL Current Category] {#current-category}

Il consiglio è determinato dalla categoria di prodotto attualmente visualizzata dal visitatore.

I consigli mostrano gli elementi nella categoria di prodotto specificata.

Quando questa opzione è selezionata, il valore `entity.categoryId` deve essere trasmesso come parametro alla mbox di visualizzazione.

Questa chiave di consigli può essere utilizzata con i seguenti algoritmi:

* [!UICONTROL Top Sellers]
* [!UICONTROL Most Viewed]

Utilizza la chiave di consigli [!UICONTROL Current Category] sul tuo sito su:

* Pagine a categoria singola.
* NON utilizzare nelle pagine dei risultati di ricerca nulli.

### [!UICONTROL Favorite Category] {#favorite-category}

Il consiglio è determinato dalla categoria di prodotto preferita del visitatore.

I consigli mostrano gli elementi nella categoria di prodotto specificata.

Quando questa opzione è selezionata, il valore `entity.categoryId` deve essere trasmesso come parametro alla mbox di visualizzazione.

Questa chiave di consigli può essere utilizzata con i seguenti algoritmi:

* [!UICONTROL Top Sellers]
* [!UICONTROL Most Viewed]

Utilizza la chiave di consigli [!UICONTROL Current Category] sul tuo sito su:

* Pagine a categoria singola.
* NON utilizzare nelle pagine dei risultati di ricerca nulli.

### [!UICONTROL Site Affinity] {#site-affinity}

Consiglia gli articoli in base alla certezza di una relazione tra articoli diversi. È possibile configurare questo criterio per determinare la quantità di dati necessari prima della presentazione di un consiglio utilizzando il cursore [!UICONTROL Inclusion Rules]. Ad esempio, se selezioni molto forte, vengono consigliati i prodotti con la maggiore certezza di corrispondenza.

Ad esempio, se imposti un’affinità molto forte e il progetto include cinque elementi, tre dei quali soddisfano il livello di soglia di connessione, i due elementi che non soddisfano i requisiti di forza minima non vengono visualizzati nei suggerimenti e vengono sostituiti dagli elementi di backup definiti. Gli elementi con affinità più elevata vengono visualizzati per primi.

Ad esempio, un retailer online può consigliare gli elementi nelle visite successive a cui un visitatore ha mostrato interesse durante le sessioni precedenti. L’attività per ogni sessione del visitatore viene acquisita per calcolare un’affinità in base a un modello di frequenza e recency. Quando il visitatore ritorna sul sito, l’affinità viene utilizzata per visualizzare i consigli in base alle azioni passate eseguite sul sito.

Alcuni clienti con varie raccolte di prodotti e comportamenti diversi sui siti potrebbero ottenere risultati ottimali impostando un’affinità di sito debole.

Questa logica può essere utilizzata con le seguenti chiavi di consigli:

* [!UICONTROL Current Item]
* [!UICONTROL Last Purchased Item]
* [!UICONTROL Last Viewed Item]
* [!UICONTROL Most Viewed Item]
