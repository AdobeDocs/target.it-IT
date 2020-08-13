---
keywords: recommendations;recommendations activity;criteria;algorithm;recommendation key;custom key;industry vertical;retail;eccommerce;lead generation;b2b;financial services;media;publishing
description: I criteri di  Adobe Target Recommendations sono regole che determinano quali prodotti raccomandare in base a un insieme predeterminato di comportamenti dei visitatori.
title: Criteri in  Adobe Target Recommendations
feature: criteria
uuid: 738db164-174b-45b8-bb8a-778f6494f1d7
translation-type: tm+mt
source-git-commit: 3cf1f4fa56f86c106dccdc2c97c080c17c3982b4
workflow-type: tm+mt
source-wordcount: '1631'
ht-degree: 74%

---


# ![PREMIUM](/help/assets/premium.png) Criteri{#criteria}

I criteri sono regole che determinano i prodotti da consigliare in base a un set predeterminato di comportamenti dei visitatori.

I criteri determinano quale azione provocherà quale consiglio. È possibile sottoporre e test più tipi di consigli tra loro aggiungendo più criteri.

## Settore verticale {#section_936BCFCF234C49A2BEC1C38AAC2D71AF}

Seleziona un settore verticale in base agli obiettivi dell&#39;attività consigliata:

| Settore verticale | Obiettivo |
|--- |--- |
| Retail/E-commerce | Conversione con conseguente acquisto |
| Generazione di lead/B2B/servizi finanziari | Conversione senza acquisto |
| Media/Editoria | Coinvolgimento |

## Recommendation key {#section_885B3BB1B43048A88A8926F6B76FC482}

La chiave dei consigli selezionata determina il tipo di criterio. Esistono diversi tipi di criteri che vengono rappresentati come schede di criteri quando imposti un’attività di [!DNL Recommendations].

| Tipo di criteri | Chiavi |
|--- |--- |
| Attività sulla pagina corrente | Consiglia gli elementi o articoli in base alle azioni degli utenti sulla pagina corrente. Ad esempio, i visitatori che visualizzano un particolare elemento potrebbero volerne consultare altri della stessa categoria.<ul><li>Elemento corrente</li><li>Categoria corrente</li></ul> |
| Personalizzato | Consiglia gli elementi o articoli in base agli attributi personalizzati.<ul><li>Attributo personalizzato</li></ul>Quando basi i consigli su attributi personalizzati, seleziona l&#39;attributo personalizzato, quindi il tipo di consiglio.<br>Puoi eseguire il filtro in tempo reale all&#39;inizio dell&#39;output di criteri personalizzati. Ad esempio, puoi limitare gli articoli consigliati a quelli della categoria o del marchio preferito dal visitatore. Così puoi combinare calcoli offline e filtri in tempo reale.<br>Grazie a questa funzionalità è possibile utilizzare Target per aggiungere la personalizzazione ai consigli calcolati offline o agli elenchi personalizzati. Permette infatti di unire le compenze del personale addetto ai dati alle tecnonologie comprovate di Adobe per la distribuzione, l&#39;applicazione di filtri al momento dell&#39;esecuzione, i test A/B, il targeting, la generazione di rapporti, le integrazioni e altro.<br>Con l’aggiunta delle regole di inclusione ai Criteri personalizzati, i consigli non sono più statici ma diventano dinamici, in base agli interessi del visitatore.<ul><li>I criteri personalizzati sono configurabili, come altri criteri nei consigli.</li><li>È possibile utilizzare [raccolte](/help/c-recommendations/c-products/collections.md), [esclusioni](/help/c-recommendations/c-products/exclusions.md) e [inclusioni](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) (incluse le regole speciali per Prezzo e Inventario) proprio come per tutti gli altri criteri.</li></ul>Eventuali casi di utilizzo includono:<ul><li>Vuoi consigliare film da una lista personalizzata, ma solo se il visitatore non li ha già guardati.</li><li>Vuoi eseguire un algoritmo offline e utilizzare i risultati per la definizione dei consigli, ma vuoi anche che vengano sempre esclusi gli articoli non disponibili.</li><li>Vuoi includere solo gli articoli appartenenti alla categoria preferita del visitatore.</li></ul> |
| Comportamento passato | Consiglia gli articoli in base alle reazioni passate dei visitatori a un articolo. Per esempio, chi ha già acquistato un articolo di una data marca sarà più propenso ad acquistare un altro articolo della stessa marca.<ul><li>Ultimo articolo acquistato</li><li>Ultimo articolo visualizzato</li><li>Articolo più visualizzato</li><li>Categoria preferita</li></ul> |
| Popolarità | Consiglia gli articoli più popolari, ad esempio i video più popolari in una categoria correlata o i prodotti visualizzati più spesso sul sito.<ul><li>Popolarità</li></ul> |
| Articoli visualizzati di recente | Consiglia gli articoli che un visitatore ha visto più di recente, ad esempio gli articoli che ha guardato l&#39;ultima volta che ha visitato il tuo sito o gli articoli di tendenza in questo momento.<br>L’algoritmo di visualizzazione degli elementi visualizzati di recente restituisce i risultati specifici dell’attività di un visitatore in un [ambiente](/help/administrating-target/hosts.md). Se due siti appartengono a ambienti diversi e un visitatore passa tra i due siti, l&#39;algoritmo restituisce solo gli elementi visualizzati di recente dal sito appropriato.<br>Questo tipo di criteri non è limitato dalle raccolte.<ul><li>Articoli visualizzati di recente</li></ul>**Nota:** non è possibile utilizzare il criterio Articoli visualizzati di recente per i consigli di backup.<br>Puoi filtrare gli articoli o i file multimediali visualizzati di recente in modo che vengano visualizzati solo quelli con uno specifico attributo.<ul><li>I criteri “visualizzati di recente” sono configurabili, come altri criteri nei consigli.</li><li>È possibile utilizzare [raccolte](/help/c-recommendations/c-products/collections.md), [esclusioni](/help/c-recommendations/c-products/exclusions.md) e [inclusioni](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) (incluse le regole speciali per Prezzo e Inventario) proprio come per tutti gli altri criteri.</li></ul>Eventuali casi di utilizzo includono:<ul><li>Una società multinazionale con più business potrebbe avere un visitatore che visualizza elementi in più proprietà digitali. In questo caso, puoi limitare gli articoli visualizzati di recente al solo sito su cui sono stati visualizzati. In tal modo gli articoli visualizzati di recente non saranno visualizzati sugli altri siti della stessa società.</li></ul> |

## Utilizzo di una chiave di raccomandazione personalizzata {#custom-key}

Potete anche basare le raccomandazioni sul valore di un attributo di profilo personalizzato.

>[!NOTE]
>
>I parametri di profilo personalizzati possono essere passati a Target tramite JavaScript, API o integrazioni. Per ulteriori informazioni sugli attributi di profilo personalizzati, consulta Profili [](/help/c-target/c-visitor-profile/visitor-profile.md)visitatore.

Ad esempio, se desiderate visualizzare i filmati consigliati in base al filmato aggiunto più di recente da un utente alla coda,

1. Select your custom profile attribute from the [!UICONTROL Recommendation Key] drop-down list (for example, [!UICONTROL Last Show Added to Watchlist]).

1. Select your [!UICONTROL Recommendation Logic] (for example, [!UICONTROL People Who Viewed This, Viewed That]).

   ![Crea nuovo criterio, finestra di dialogo](/help/c-recommendations/c-algorithms/assets/custom-key1.png)

If your custom profile attribute does not directly match to a single entity ID, it is necessary to explain to [!DNL Recommendations] how you want the match to an entity to occur.

Ad esempio, se desiderate visualizzare gli elementi più venduti dal marchio preferito di un utente,

1. Select your custom profile attribute from the [!UICONTROL Recommendation Key] drop-down list (for example, [!UICONTROL Favorite Brand]).

1. Select the [!UICONTROL Recommendation Logic] you want to use with this key (for example, [!UICONTROL Top Sellers]).

   Viene visualizzata l’opzione [!UICONTROL Raggruppa per valore univoco di].

1. Seleziona l’attributo di entità che corrisponde alla chiave scelta. In this case [!UICONTROL Favorite Brand] matches to `entity.brand`.

   [!DNL Recommendations] genera ora un elenco &quot;Top Sellers&quot; (Venditori principali) per ogni marchio e mostra all&#39;utente l&#39;elenco &quot;Top Sellers&quot; appropriato in base al valore memorizzato nell&#39;attributo del profilo del marchio [!UICONTROL Preferiti] .

   ![Attributo Top Sellers](/help/c-recommendations/c-algorithms/assets/custom-key2.png)

## Criteria/algorithms {#criteria-algorithms}

[!DNL Target Recommendations]In sono utilizzati algoritmi sofisticati per determinare quando le azioni di un visitatore soddisfano i criteri impostati nell&#39;attività. La Chiave consiglio determina le opzioni di logica disponibili.

| Criteri | Descrizione |
|--- |--- |
| Articoli/Media con attributi simili | Consiglia articoli o media simili in base all’attività corrente o al comportamento passato del visitatore.<br>**Nota:** se selezioni Articoli/Media con attributi simili, avrai la possibilità di impostare regole di somiglianza del contenuto. |
| Chi ha visualizzato questo ha visualizzato anche quello | Consiglia gli elementi che vengono visualizzati più spesso nella stessa sessione in cui viene visualizzato l’elemento specificato. |
| Chi ha visualizzato questo ha acquistato anche quello | Consiglia gli articoli che vengono acquistati più spesso nella stessa sessione in cui viene visualizzato l’articolo specificato. Questo criterio restituisce gli altri prodotti acquistati dopo la visualizzazione dell’articolo corrente; il prodotto specificato non è incluso nell’insieme di risultati. |
| Chi ha comprato questo ha acquistato anche quello | Consiglia gli articoli che sono acquistati più spesso dai clienti contemporaneamente all’articolo specificato. |
| Affinità sito | Consiglia gli articoli in base alla certezza di una relazione tra articoli diversi. È possibile configurare questo criterio per determinare la quantità di dati necessari prima che venga presentato un consiglio utilizzando il cursore delle Regole di inclusione. Per esempio, se selezioni molto forte, vengono consigliati i prodotti con una maggiore certezza di corrispondenza.<br>Ad esempio, se imposti un’affinità molto forte e il progetto include cinque elementi, tre dei quali soddisfano il livello di soglia di connessione, i due elementi che non soddisfano i requisiti di forza minima non vengono visualizzati nei suggerimenti e vengono sostituiti dagli elementi di backup definiti. Gli elementi con affinità più elevata vengono visualizzati per primi.<br>Alcuni clienti con varie raccolte di prodotti e comportamenti diversi sui siti potrebbero ottenere risultati ottimali impostando un’affinità di sito debole. |
| Articoli più venduti | Articoli inclusi nella maggioranza degli ordini completati. Più unità dello stesso articolo in un unico ordine vengono conteggiate come un ordine. |
| Articoli più visualizzati | Articoli o elementi multimediali visualizzati più spesso. |
| Articoli/Media visualizzati di recente | Articoli che sono stati visualizzati di recente dal visitatore. Quando si utilizza questo criterio, è necessario aggiornare la progettazione di Target in modo da gestire i casi di visualizzazione di raccomandazioni vuote laddove gli elementi visualizzati in precedenza non siano sufficienti. |
| Recommendations basato su utente | Raccomanda gli elementi in base alla cronologia di navigazione, visualizzazione e acquisto di ogni visitatore. Tali elementi sono generalmente denominati &quot;Consigliati per l&#39;utente.&quot;<br>Questo criterio consente di fornire contenuti ed esperienze personalizzati sia ai visitatori nuovi che di ritorno. L&#39;elenco delle raccomandazioni è ponderato per l&#39;attività più recente del visitatore e viene aggiornato in sessione e diventa più personalizzato man mano che l&#39;utente naviga sul sito.<br>Sia le viste che gli acquisti vengono utilizzati per determinare gli elementi raccomandati. La chiave di raccomandazione specificata (ad es. Elemento corrente) viene utilizzata per applicare eventuali filtri di regole di inclusione selezionati. Sarà possibile, ad esempio:<ul><li>Escludere gli elementi che non soddisfano determinati criteri (prodotti esauriti, articoli pubblicati più di 30 giorni fa, film classificati R e così via)</li><li>Limita gli elementi inclusi a una singola categoria o alla categoria corrente</li></ul> |

>[!NOTE]
>
>Se modifichi i criteri di un consiglio attivo, i dati di rapporto relativi andranno persi.

Puoi anche utilizzare informazioni conosciute aggiuntive su un visitatore per migliorare i consigli.

Tutti i criteri di un giorno vengono eseguiti due volte al giorno. Tutti i criteri di una settimana e più vengono eseguiti una volta al giorno. I criteri di affinità per sito vengono eseguiti una volta al giorno. I criteri di backup vengono eseguiti due volte al giorno.

## Viewing criteria information {#section_7162DE58E4594FD688A4D7FDB829FD8B}

Per visualizzare i dettagli dei criteri su una scheda a comparsa, passa il mouse su una scheda e fai clic sull&#39;icona Informazioni sulla scheda dei criteri, senza aprirli.

![Passaggio del cursore sulla scheda Criteri](/help/c-recommendations/c-algorithms/assets/criteria_hover.png)

Fai clic sulla scheda **[!UICONTROL Informazioni algoritmo]** per visualizzare le informazioni generali sui criteri selezionati, tra cui Nome, Descrizione, Verticale, Tipo di pagina/e, Chiave/i, Logica Consiglio e ID algoritmo.

![Scheda Informazioni algoritmo](/help/c-recommendations/c-algorithms/assets/criteria_info.png)

Fai clic sulla scheda **[!UICONTROL Uso dell&#39;Algoritmo]** per visualizzare un elenco di attività che fanno riferimento ai criteri selezionati. La scheda elenca le attività attive e inattive. Fai clic sugli elenchi a discesa Attività o Inattività per visualizzare l&#39;intero elenco di attività che fanno riferimento a tali criteri. Puoi fare clic sul link dell&#39;attività per aprire quella da modificare.

![Utilizzo algoritmo, scheda](/help/c-recommendations/c-algorithms/assets/criteria_usage.png)

>[!NOTE]
>
>Al momento la funzione Utilizzo  algoritmo è supportata solo per le attività Recommendations. Al momento questa funzione non è supportata per le attività Test e Targeting delle esperienze A/B (XT) che includono [raccomandazioni come offerta](/help/c-recommendations/recommendations-as-an-offer.md).
