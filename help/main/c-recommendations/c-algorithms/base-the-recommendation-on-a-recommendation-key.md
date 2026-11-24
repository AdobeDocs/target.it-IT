---
keywords: chiave consigli;logica consigli;categoria corrente;attributo personalizzato;ultimo articolo acquistato;ultimo articolo visualizzato;articolo più visualizzato;articolo più visualizzato;categoria preferita;popolarità;articolo visualizzato di recente;ultimo articolo acquistato;più visualizzato;preferito;visualizzato di recente
description: Scopri come utilizzare i consigli in base a chiavi che utilizzano il contesto del comportamento del visitatore per mostrare risultati rilevanti nelle attività [!UICONTROL Consigli].
title: Come posso basare il [!UICONTROL consiglio] su una [!UICONTROL chiave consiglio]?
feature: Recommendations
mini-toc-levels: 2
exl-id: 49764f18-88fb-41be-b2a0-e7ced9de742c
TQID: 'https://experienceleague.adobe.com/1gI3rMMf9s5ogc4BvBz4fMUqxed1Nqad0XoaR8SlU58'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f7c7de77-382f-4f48-8b36-61a170f06d3d
    internal-label: Integrations
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c4147b6e-073b-4d3c-9ab1-d60f2f4434ef
    internal-label: Behavioral data
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: e8a9b6be04169ea3024673babb62085667fe8990
workflow-type: tm+mt
source-wordcount: '3740'
ht-degree: 11%
---
# Basare il consiglio su una chiave consiglio {#base-on-recommendation-key}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri i tipi di algoritmo, gli algoritmi e le chiavi di consigli disponibili per basare i consigli nelle attività [!DNL Adobe Target Recommendations].

>[!ENDSHADEBOX]

I consigli basati su algoritmi utilizzano il contesto del comportamento del visitatore per mostrare risultati rilevanti nelle attività [!DNL Adobe Target] [!DNL Recommendations]. Ogni tipo di algoritmo offre il proprio set di algoritmi. Per un riepilogo dei tipi di algoritmo e dei relativi algoritmi, vedere [Introduzione ai criteri](/help/main/c-recommendations/c-algorithms/algorithms.md#section_885B3BB1B43048A88A8926F6B76FC482).

Ogni criterio è definito nella relativa scheda. Il traffico viene suddiviso in modo uniforme tra i test dei criteri: con due criteri, il traffico viene diviso in modo uniforme tra di essi e con due criteri e due progetti, il traffico viene suddiviso in modo uniforme tra le quattro combinazioni. È inoltre possibile impostare una percentuale di visitatori del sito in modo da visualizzare il contenuto predefinito per il confronto. In tal caso, la percentuale di visitatori specificata visualizza il contenuto predefinito e il resto viene suddiviso tra i criteri e le combinazioni di progettazione.

Per ulteriori informazioni sulla creazione di criteri e sulla definizione dei relativi tipi di algoritmi e algoritmi, vedere [Creare criteri](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md).

Algoritmi diversi si adattano a diversi tipi di pagine. Le sezioni seguenti descrivono ogni tipo di algoritmo e i relativi algoritmi.

## Basato su carrello {#cart-based}

Il tipo di algoritmo **[!UICONTROL Basato sul carrello]** consiglia gli elementi in base al contenuto del carrello corrente del visitatore. Le chiavi di consigli sono fornite come valori separati da virgole nel parametro [mbox `cartIds`](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank}. Vengono considerati solo i primi 10 valori.

La logica dei consigli basati sul carrello è simile all&#39;algoritmo basato sull&#39;utente &quot;**[!UICONTROL Consigliato per te]**&quot; e agli algoritmi basati sull&#39;elemento &quot;**[!UICONTROL Persone che hanno visualizzato questo, hanno acquistato quello]**&quot; e &quot;**[!UICONTROL Persone che hanno acquistato questo hanno acquistato quello]**&quot;.

[!DNL Target] utilizza tecniche di filtro collaborativo per determinare le somiglianze per ogni elemento nel carrello del visitatore, quindi combina le somiglianze comportamentali di tutti gli elementi in un elenco unito.

Gli addetti al marketing possono scegliere se [!DNL Target] esamina il comportamento dei visitatori all&#39;interno di una singola sessione o in più sessioni:

* **[!UICONTROL Sessione singola]**: in base a ciò che hanno fatto altri visitatori in una singola sessione.

  Una singola sessione è adatta ai prodotti che si &quot;accompagnano&quot; fortemente in base a un utilizzo, un’occasione o un evento. Ad esempio, un visitatore che acquista una stampante potrebbe anche aver bisogno di inchiostro e carta, mentre un visitatore che acquista burro di arachidi potrebbe avere bisogno anche di pane e gelatina.

* **[!UICONTROL Tra sessioni]**: in base a ciò che hanno fatto altri visitatori in più sessioni.

  Le sessioni multiple sono adatte a prodotti che si &quot;accompagnano&quot; fortemente in base alle preferenze o al gusto del visitatore. Ad esempio, a un visitatore a cui piace Star Wars potrebbe piacere anche Indiana Jones, anche se non desidera necessariamente guardare entrambi i film nella stessa sessione. Allo stesso modo, a un visitatore a cui piace il gioco da tavolo &quot;Codenames&quot; potrebbe piacere anche il gioco da tavolo &quot;Avalon&quot;, anche se il visitatore non può giocare entrambi i giochi contemporaneamente.

[!DNL Target] formula raccomandazioni per ogni visitatore in base agli elementi nel carrello corrente, indipendentemente dal fatto che il comportamento del visitatore venga considerato all&#39;interno di una singola sessione o in più sessioni.

I seguenti algoritmi sono disponibili con il tipo di algoritmo **[!UICONTROL Basato su carrello]**:

| Algoritmo | Come funziona | Quando utilizzare | Chiavi consiglio |
| --- | --- | --- | --- |
| **[!UICONTROL Persone Che Hanno Visualizzato Questi, Hanno Visualizzato Anche]** | Consiglia gli elementi che vengono visualizzati più spesso nella stessa sessione in cui viene visualizzato l’elemento specificato. Restituisce altri prodotti visualizzati dopo aver visualizzato questo. Il prodotto specificato non è incluso nel set di risultati. | Crea ulteriori opportunità di conversione consigliando gli articoli visualizzati anche dagli altri visitatori che hanno visualizzato un articolo. Ad esempio, i visitatori che visualizzano le bici da strada sul sito potrebbero anche guardare caschi, kit per il ciclismo, serrature e così via, quindi un consiglio può suggerire altri prodotti che contribuiscono ad aumentare i ricavi. | **[!UICONTROL Articolo corrente]**, **[!UICONTROL Ultimo articolo acquistato]**, **[!UICONTROL Ultimo articolo visualizzato]**, **[!UICONTROL Articolo più visualizzato]** |
| **[!UICONTROL Chi ha visualizzato questi elementi ha acquistato anche]** | Consiglia gli articoli che vengono acquistati più spesso nella stessa sessione in cui viene visualizzato l’articolo specificato. Restituisce altri prodotti acquistati dopo aver visualizzato questo. Il prodotto specificato non è incluso nel set di risultati. | Aumenta le opportunità di cross-selling visualizzando un consiglio in una pagina di prodotto, ad esempio, in cui vengono visualizzati gli articoli acquistati da altri visitatori. Se il visitatore sta visualizzando un palo da pesca, il consiglio potrebbe mostrare altri elementi acquistati da altri visitatori, come scatole per gli attrezzi, trampolieri e esche per la pesca. I visitatori che navigano nel sito ricevono consigli di acquisto aggiuntivi. | **[!UICONTROL Articolo corrente]**, **[!UICONTROL Ultimo articolo acquistato]**, **[!UICONTROL Ultimo articolo visualizzato]**, **[!UICONTROL Articolo più visualizzato]** |
| **[!UICONTROL Chi ha acquistato questi, ha acquistato anche]** | Consiglia gli articoli che sono acquistati più spesso dai clienti contemporaneamente all’articolo specificato. Restituisce altri prodotti acquistati dopo l&#39;acquisto di questo. Il prodotto specificato non è incluso nel set di risultati. | Aumenta le opportunità di cross-selling visualizzando un consiglio in una pagina di riepilogo del carrello, ad esempio, in cui vengono visualizzati gli articoli acquistati anche da altri acquirenti. Se il visitatore acquista un completo, il consiglio potrebbe mostrare altri articoli acquistati insieme all’indumento, come cravatte, scarpe e gemelli. Man mano che i visitatori esaminano i loro acquisti, ricevono consigli aggiuntivi. | **[!UICONTROL Articolo corrente]**, **[!UICONTROL Ultimo articolo acquistato]**, **[!UICONTROL Ultimo articolo visualizzato]**, **[!UICONTROL Articolo più visualizzato]** |

## [!UICONTROL Basato Sulla Popolarità]

Il tipo di algoritmo **[!UICONTROL Basato sulla popolarità]** consiglia gli elementi in base alla loro popolarità complessiva nel sito o alla loro popolarità all&#39;interno della categoria, del brand, del genere preferito o più visualizzato dell&#39;utente.

I seguenti algoritmi sono disponibili con il tipo di algoritmo **[!UICONTROL Basato sulla popolarità]**:

| Algoritmo | Come funziona | Quando utilizzare | Chiavi consiglio |
| --- | --- | --- | --- |
| **[!UICONTROL Più visualizzati nel sito]** | Il consiglio è determinato dall’elemento visualizzato più di frequente, in base ai criteri di recency/frequenza. Vedi [Più visualizzati nel punteggio del sito](#most-viewed). | Pagine generali, come la pagina principale o le pagine di destinazione e gli annunci offsite. | |
| **[!UICONTROL Più visualizzati per categoria]** | Il consiglio è determinato dalla categoria che ha ricevuto il maggior numero di attività, utilizzando lo stesso metodo utilizzato per l’elemento più visualizzato, con la differenza che il punteggio viene attribuito alle categorie anziché ai prodotti. Vedi [Più visualizzati per punteggio categoria](#most-viewed-category). | Pagine generali, come la pagina principale o le pagine di destinazione e gli annunci offsite. | **[!UICONTROL Categoria corrente]**, **[!UICONTROL Categoria preferita]** |
| **[!UICONTROL Più visualizzati per attributo elemento]** | Consiglia elementi o media simili a quelli più visualizzati sul sito. Viene selezionato l’attributo dell’elemento su cui basare il consiglio, ad esempio &quot;Nome&quot; o &quot;Marchio&quot;. Vengono quindi selezionati gli attributi di profilo memorizzati nel profilo del visitatore da associare, ad esempio &quot;Marchio preferito&quot;, &quot;Ultimo elemento aggiunto al carrello&quot; o &quot;Spettacolo più visualizzato&quot;. | | |
| **[!UICONTROL Più visualizzati per attributo profilo]** | Consiglia di raggruppare gli elementi più visualizzati in base a un attributo del profilo visitatore anziché in base alle informazioni sugli elementi, come avviene per **[!UICONTROL Articoli più visualizzati per categoria]** e **[!UICONTROL Attributi più visualizzati per elemento]**. [!DNL Target] mantiene un elenco di classificazione separato per valore di attributo e, al momento della consegna, mostra a ogni visitatore l&#39;elenco corrispondente al proprio valore memorizzato. Consulta [Algoritmi degli attributi di profilo](#profile-attribute-algorithms). | | |
| **[!UICONTROL Più venduti nel sito]** | Visualizza gli articoli inclusi nel maggior numero di ordini completati dall&#39;interno del sito. Più unità dello stesso articolo in un unico ordine vengono conteggiate come un ordine. | Crea consigli per gli articoli più venduti sul sito per aumentare la conversione e i ricavi. Questa logica è adatta per i nuovi visitatori del sito. | |
| **[!UICONTROL Più venduti per categoria]** | Visualizza gli articoli inclusi nel maggior numero di ordini completati per categoria. Più unità dello stesso articolo in un unico ordine vengono conteggiate come un ordine. | Crea consigli per gli articoli più venduti sul sito in base alla categoria per aumentare la conversione e i ricavi. Questa logica è adatta per i nuovi visitatori del sito. | **[!UICONTROL Categoria corrente]**, **[!UICONTROL Categoria preferita]** |
| **[!UICONTROL Più venduti per attributo articolo]** | Consiglia articoli o supporti simili agli articoli o ai supporti più acquistati sul sito. Viene selezionato l’attributo dell’elemento su cui basare il consiglio, ad esempio &quot;Nome&quot; o &quot;Marchio&quot;. Vengono quindi selezionati gli attributi di profilo memorizzati nel profilo del visitatore da associare, ad esempio &quot;Marchio preferito&quot;, &quot;Ultimo elemento aggiunto al carrello&quot; o &quot;Spettacolo più visualizzato&quot;. | | |
| **[!UICONTROL Più venduti per attributo profilo]** | Consiglia gli articoli più venduti raggruppati per un attributo del profilo visitatore anziché per informazioni sugli articoli, come fanno **[!UICONTROL i più venduti per categoria]** e **[!UICONTROL i più venduti per attributo articolo]**. [!DNL Target] mantiene un elenco dei più venduti separato per valore di attributo e, al momento della consegna, mostra a ogni visitatore l&#39;elenco corrispondente al proprio valore memorizzato. Consulta [Algoritmi degli attributi di profilo](#profile-attribute-algorithms). | | |
| **[!UICONTROL Primi per metrica di Analytics]** | Visualizza la &quot;X superiore&quot; in cui *x* è una metrica [!DNL Analytics] arbitraria. Quando si utilizzano dati comportamentali da mbox, è possibile utilizzare **[!UICONTROL I più venduti]** o **[!UICONTROL I più visualizzati]** (x = &quot;venduti&quot; o x = &quot;visualizzati&quot;). Quando si utilizzano i dati comportamentali di [!DNL Adobe Analytics], è possibile utilizzare x = &quot;Aggiunte al carrello&quot; o un&#39;altra metrica [!DNL Analytics]. | | |

### [!UICONTROL Punteggio più visualizzato nel sito] {#most-viewed}

Il consiglio è l’elemento che è stato visualizzato più spesso, determinato dai criteri di recency/frequenza come segue:

* 10 punti per la prima visualizzazione del prodotto
* 5 punti per ogni visualizzazione successiva
* Al termine di una sessione, dividi tutti i valori per 2

Ad esempio, visualizzando la tavola da surf A e poi la tavola da surf B in una sessione si ottengono A: 10, B: 5. Al termine della sessione, il risultato è A: 5, B: 2.5. Se gli stessi elementi vengono visualizzati nella sessione successiva, i valori cambiano in A: 15, B: 7.5.

### [!UICONTROL Punteggio più visualizzato per categoria] {#most-viewed-category}

Il consiglio è la categoria che ha ricevuto più attività. Utilizza lo stesso metodo dell’articolo più visualizzato, con la differenza che le categorie vengono valutate al posto dei prodotti, con i criteri di recency/frequenza seguenti:

* 10 punti per la prima visualizzazione della categoria
* 5 punti per ogni visualizzazione successiva

A ogni visita, il punteggio di ogni categoria non corrente visualizzata in precedenza è diminuito di 1.

Ad esempio, visualizzando la categoria A e la categoria B in una sessione si ottiene A: 9, B: 10. Se gli stessi elementi vengono visualizzati nella sessione successiva, i valori cambiano in A: 20, B: 9.

### Algoritmi degli attributi di profilo {#profile-attribute-algorithms}

>[!CONTEXTUALHELP]
>id="target_recommendations_profile_attribute"
>title="Attributo di profilo"
>abstract="Puoi creare un attributo del profilo utilizzando gli script di profilo. Una volta creato e attivato uno script di profilo, è possibile utilizzare il relativo attributo di profilo corrispondente con questo algoritmo."

**[!UICONTROL I più visualizzati per attributo profilo]** e **[!UICONTROL i più venduti per attributo profilo]** dipendono da uno script di profilo per compilare l&#39;attributo. Il nome dello script deve iniziare con il prefisso `recsAttribute` in modo che [!DNL Target] lo archivi come `user.recsAttribute<Name>`. È possibile scrivere uno script per qualsiasi caratteristica del visitatore pertinente al caso d’uso. Per ulteriori informazioni sull&#39;impostazione degli attributi di profilo con gli script di profilo, vedere [Parametri di profilo](https://experienceleague.adobe.com/en/docs/target/using/audiences/visitor-profiles/profile-parameters).

Ad esempio, il seguente script, denominato `recsAttributeRegion`, basa i consigli sulla regione del visitatore:

```
var region = mbox.param('userRegion');
if (region) return region;
```

Analogamente, il seguente script, denominato `recsAttributeLoyaltyTier`, basa i consigli sul livello di fedeltà del visitatore:

```
var tier = mbox.param('visitorLoyaltyTier');
if (tier) return tier;
```

Dopo la creazione e l&#39;attivazione dello script, la voce corrispondente del **[!UICONTROL Area]** o del **[!UICONTROL Livello fedeltà]** diventa disponibile nel menu a discesa degli attributi del profilo della finestra Crea criteri. Il prefisso `recsAttribute` stesso non viene visualizzato nel menu a discesa.

## [!UICONTROL Basato su elemento]

Il tipo di algoritmo **[!UICONTROL Basato su elemento]** consiglia elementi simili a quelli attualmente visualizzati dall&#39;utente o visualizzati di recente.

I seguenti algoritmi sono disponibili con il tipo di algoritmo **[!UICONTROL Basato su elemento]**:

| Algoritmo | Come funziona | Quando utilizzare | Chiavi consiglio |
| --- | --- | --- | --- |
| **[!UICONTROL Chi ha visualizzato questo ha visualizzato anche quello]** | Consiglia gli elementi che vengono visualizzati più spesso nella stessa sessione in cui viene visualizzato l’elemento specificato. Restituisce altri prodotti visualizzati dopo aver visualizzato questo. Il prodotto specificato non è incluso nel set di risultati. | Crea ulteriori opportunità di conversione consigliando gli articoli visualizzati anche dagli altri visitatori che hanno visualizzato un articolo. Ad esempio, i visitatori che visualizzano le bici da strada sul sito potrebbero anche guardare caschi, kit per il ciclismo, serrature e così via, quindi un consiglio può suggerire altri prodotti che contribuiscono ad aumentare i ricavi. | **[!UICONTROL Articolo corrente]**, **[!UICONTROL Ultimo articolo acquistato]**, **[!UICONTROL Ultimo articolo visualizzato]**, **[!UICONTROL Articolo più visualizzato]** |
| **[!UICONTROL Chi ha visualizzato questo ha acquistato anche quello]** | Consiglia gli articoli che vengono acquistati più spesso nella stessa sessione in cui viene visualizzato l’articolo specificato. Restituisce altri prodotti acquistati dopo aver visualizzato questo. Il prodotto specificato non è incluso nel set di risultati. | Aumenta le opportunità di cross-selling visualizzando un consiglio in una pagina di prodotto, ad esempio, in cui vengono visualizzati gli articoli acquistati da altri visitatori. Se il visitatore sta visualizzando un palo da pesca, il consiglio potrebbe mostrare altri elementi acquistati da altri visitatori, come scatole per gli attrezzi, trampolieri e esche per la pesca. I visitatori che navigano nel sito ricevono consigli di acquisto aggiuntivi. | **[!UICONTROL Articolo corrente]**, **[!UICONTROL Ultimo articolo acquistato]**, **[!UICONTROL Ultimo articolo visualizzato]**, **[!UICONTROL Articolo più visualizzato]** |
| **[!UICONTROL Chi ha acquistato questo ha acquistato anche quello]** | Consiglia gli articoli che sono acquistati più spesso dai clienti contemporaneamente all’articolo specificato. Restituisce altri prodotti acquistati dopo l&#39;acquisto di questo. Il prodotto specificato non è incluso nel set di risultati. | Aumenta le opportunità di cross-selling visualizzando un consiglio in una pagina di riepilogo del carrello, ad esempio, in cui vengono visualizzati gli articoli acquistati anche da altri acquirenti. Se il visitatore acquista un completo, il consiglio potrebbe mostrare altri articoli acquistati insieme all’indumento, come cravatte, scarpe e gemelli. Man mano che i visitatori esaminano i loro acquisti, ricevono consigli aggiuntivi. | **[!UICONTROL Articolo corrente]**, **[!UICONTROL Ultimo articolo acquistato]**, **[!UICONTROL Ultimo articolo visualizzato]**, **[!UICONTROL Articolo più visualizzato]** |
| **[!UICONTROL Elementi con attributi simili]** | Consiglia articoli o media simili in base all’attività corrente o al comportamento passato del visitatore. Se è selezionata l&#39;opzione **[!UICONTROL Elementi con attributi simili]** o **[!UICONTROL Elementi con attributi simili]**, è possibile impostare le regole di somiglianza del contenuto. Per ulteriori informazioni, vedere [Somiglianza contenuto](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#similarity). | La somiglianza dei contenuti è efficace per i nuovi elementi, che probabilmente non saranno visualizzati nei consigli utilizzando **[!UICONTROL Persone che hanno visualizzato questo]**, **[!UICONTROL Che hanno visualizzato]**, e altra logica basata sul comportamento passato. Può anche generare consigli per i nuovi visitatori, che non hanno acquisti precedenti o altri dati storici. | **[!UICONTROL Articolo corrente]**, **[!UICONTROL Ultimo articolo acquistato]**, **[!UICONTROL Ultimo articolo visualizzato]**, **[!UICONTROL Articolo più visualizzato]** |

## [!UICONTROL Basato su utente]

Il tipo di algoritmo **[!UICONTROL Basato sull&#39;utente]** consiglia gli elementi in base al comportamento dell&#39;utente.

I seguenti algoritmi sono disponibili con il tipo di algoritmo **[!UICONTROL Basato sull&#39;utente]**:

| Algoritmo | Come funziona | Quando utilizzare | Chiavi consiglio |
| --- | --- | --- | --- |
| **[!UICONTROL Elementi visualizzati di recente]** | Utilizza la cronologia del visitatore (nell&#39;arco delle sessioni) per presentare gli ultimi elementi *x* visualizzati, in base al numero di posizioni nella progettazione. Vedi [Dettagli sugli elementi visualizzati di recente](#recently-viewed). | Pagine generali, come la pagina principale o le pagine di destinazione e gli annunci offsite. | |
| **[!UICONTROL Consigliato per te]** | Consiglia gli articoli in base alla cronologia di navigazione, visualizzazione e acquisto di ogni visitatore. Sia le visualizzazioni che gli acquisti vengono utilizzati per determinare gli articoli consigliati. L’elenco dei consigli è ponderato rispetto all’attività più recente del visitatore, viene aggiornato nella sessione e diventa più personalizzato man mano che l’utente naviga sul sito. | Distribuisci contenuti ed esperienze personalizzati sia ai visitatori nuovi che a quelli di ritorno. La chiave di consiglio specificata (ad esempio, **[!UICONTROL Elemento corrente]**) viene utilizzata per applicare i filtri delle regole di inclusione selezionati, ad esempio per escludere gli elementi che non soddisfano determinati criteri (prodotti esauriti, articoli pubblicati più di 30 giorni fa, film classificati R e così via) o per limitare gli elementi inclusi a una singola categoria o alla categoria corrente. | Chiavi di filtro: **[!UICONTROL Articolo corrente]**, **[!UICONTROL Ultimo articolo acquistato]**, **[!UICONTROL Ultimo articolo visualizzato]**, **[!UICONTROL Articolo più visualizzato]** |

### [!UICONTROL Dettagli sugli elementi visualizzati di recente] {#recently-viewed}

L&#39;algoritmo **[!UICONTROL Elementi visualizzati di recente]** restituisce risultati specifici per un determinato [ambiente](/help/main/administrating-target/hosts.md). Se due siti appartengono ad ambienti diversi e un visitatore passa da un sito all’altro, ciascun sito mostra solo gli articoli visualizzati di recente per il sito appropriato. Se due siti si trovano nello stesso ambiente e un visitatore passa da un sito all’altro, il visitatore visualizza gli stessi elementi visualizzati di recente per entrambi i siti.

Impossibile utilizzare i criteri **[!UICONTROL Elementi visualizzati di recente]** per i consigli di backup.

**[!UICONTROL Gli elementi visualizzati di recente]** o **[!UICONTROL Elementi visualizzati di recente]** possono essere filtrati in modo che vengano visualizzati solo gli elementi con un attributo specifico.

* **[!UICONTROL I criteri visualizzati di recente]** sono configurabili, come altri criteri nei consigli.
* Le [raccolte](/help/main/c-recommendations/c-products/collections.md), [esclusioni](/help/main/c-recommendations/c-products/exclusions.md) e [inclusioni](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) (incluse le regole speciali per Prezzo e Inventario) possono essere utilizzate allo stesso modo di qualsiasi altro criterio.

Un caso d’uso è una società multinazionale con più aziende, in cui un visitatore potrebbe visualizzare gli elementi in più proprietà digitali. Gli elementi visualizzati di recente possono quindi essere limitati alla proprietà in cui sono stati visualizzati, pertanto non vengono visualizzati sul sito di un’altra proprietà.

>[!NOTE]
>
>**[!UICONTROL Elementi visualizzati di recente]** rispetta sia le impostazioni di esclusione globali che le impostazioni di raccolta selezionate per l&#39;attività. Se un elemento è escluso da un’esclusione globale o non è contenuto nella raccolta selezionata, non viene visualizzato. Pertanto, quando si utilizza il criterio **[!UICONTROL Articoli visualizzati di recente]**, in genere è necessario utilizzare l&#39;impostazione &quot;Tutte le raccolte&quot;.

## Criteri personalizzati {#custom}

Il tipo di algoritmo **[!UICONTROL Criteri personalizzati]** consiglia gli elementi in base a un file personalizzato caricato.

Il consiglio è determinato da un elemento memorizzato nel profilo di un visitatore, utilizzando gli attributi utente.*x* o profilo.*x*. Quando questa opzione è selezionata, il valore `entity.id` deve essere presente nell&#39;attributo profilo. Quando i consigli sono basati su attributi personalizzati, è necessario selezionare prima l’attributo personalizzato e quindi il tipo di consiglio.

È possibile applicare un filtro in tempo reale all’output dei criteri personalizzati. Ad esempio, gli articoli consigliati possono essere limitati a quelli della categoria o del marchio preferito di un visitatore. Questo combina calcoli offline con filtri in tempo reale, in modo che [!DNL Target] possa aggiungere la personalizzazione a consigli calcolati offline o elenchi personalizzati. La scienza dei dati e la ricerca dell’organizzazione vengono quindi combinate con la distribuzione, il filtraggio in fase di esecuzione, il test A/B, il targeting, il reporting e le integrazioni di Adobe.

Le regole di inclusione su **[!UICONTROL Criteri personalizzati]** trasformano i consigli non statici in consigli dinamici in base agli interessi del visitatore.

* I criteri personalizzati sono configurabili, come altri criteri nei consigli.
* Le [raccolte](/help/main/c-recommendations/c-products/collections.md), [esclusioni](/help/main/c-recommendations/c-products/exclusions.md) e [inclusioni](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) (incluse le regole speciali per Prezzo e Inventario) possono essere utilizzate allo stesso modo di qualsiasi altro criterio.

I possibili casi d’uso includono:

* Consiglia film da un elenco personalizzato, ma solo se il visitatore non li ha già guardati.
* Esegui un algoritmo offline e utilizza i risultati per abilitare i consigli, assicurandoti al contempo che gli elementi esauriti non vengano mai consigliati.
* Includi solo gli elementi della categoria preferita del visitatore.

## Chiavi consiglio {#keys}

Le seguenti chiavi di consigli sono disponibili dall&#39;elenco a discesa **[!UICONTROL Chiave consiglio]**:

| Chiave | Come viene determinato | Cosa trasmettere | Usa su | Non utilizzare su | Algoritmi |
| --- | --- | --- | --- | --- | --- |
| **[!UICONTROL Elemento corrente]** | L’elemento attualmente visualizzato dal visitatore. Il consiglio visualizzano altri elementi che potrebbero interessare i visitatori interessati all&#39;elemento specificato. | Il valore `entity.id` deve essere trasmesso come parametro nella mbox di visualizzazione. | Pagine a elemento singolo, ad esempio le pagine del prodotto. | Pagine dei risultati di ricerca nulle. | **[!UICONTROL Articoli con attributi simili]**, **[!UICONTROL Chi ha visualizzato questo ha visualizzato quello]**, **[!UICONTROL Chi ha visualizzato questo ha acquistato quello]**, **[!UICONTROL Chi ha acquistato questo ha acquistato quello]** |
| **[!UICONTROL Ultimo articolo acquistato]** | L’ultimo articolo acquistato da ogni visitatore univoco. | Niente. Questo viene acquisito automaticamente. | Pagina principale, pagina account, annunci fuori sede. | Pagine dei prodotti o pagine relative agli acquisti. | **[!UICONTROL Articoli con attributi simili]**, **[!UICONTROL Chi ha visualizzato questo ha visualizzato quello]**, **[!UICONTROL Chi ha visualizzato questo ha acquistato quello]**, **[!UICONTROL Chi ha acquistato questo ha acquistato quello]** |
| **[!UICONTROL Ultimo articolo visualizzato]** | L’ultimo elemento visualizzato da ogni visitatore univoco. | Niente. Questo viene acquisito automaticamente. | Pagina principale, pagina account, annunci fuori sede. | Pagine dei prodotti o pagine relative agli acquisti. | **[!UICONTROL Articoli con attributi simili]**, **[!UICONTROL Chi ha visualizzato questo ha visualizzato quello]**, **[!UICONTROL Chi ha visualizzato questo ha acquistato quello]**, **[!UICONTROL Chi ha acquistato questo ha acquistato quello]** |
| **[!UICONTROL Articolo più visualizzato]** | Gli elementi o i file multimediali visualizzati più di frequente sul sito. Questa logica visualizza i consigli in base agli elementi più visualizzati, per aumentare le conversioni per altri elementi. Ad esempio, un sito di contenuti multimediali potrebbe mostrare nella propria home page i consigli per i video più visualizzati, in modo da incoraggiare i visitatori a guardare altri video. | | | | **[!UICONTROL Articoli con attributi simili]**, **[!UICONTROL Chi ha visualizzato questo ha visualizzato quello]**, **[!UICONTROL Chi ha visualizzato questo ha acquistato quello]**, **[!UICONTROL Chi ha acquistato questo ha acquistato quello]** |
| **[!UICONTROL Categoria corrente]** | La categoria di prodotto attualmente visualizzata dal visitatore. I consigli mostrano gli elementi nella categoria di prodotto specificata. | Il valore `entity.categoryId` deve essere passato come parametro alla mbox di visualizzazione. | Pagine a categoria singola. | Pagine dei risultati di ricerca nulle. | **[!UICONTROL Articoli più venduti]**, **[!UICONTROL Articoli più visualizzati]** |
| **[!UICONTROL Categoria preferita]** | La categoria di prodotti preferita del visitatore. I consigli mostrano gli elementi nella categoria di prodotto specificata. | Il valore `entity.categoryId` deve essere passato come parametro alla mbox di visualizzazione. | Pagine a categoria singola. | Pagine dei risultati di ricerca nulle. | **[!UICONTROL Articoli più venduti]**, **[!UICONTROL Articoli più visualizzati]** |

### Chiave consiglio personalizzata

I consigli possono essere basati sul valore di un attributo di profilo personalizzato. Ad esempio, puoi visualizzare i film consigliati in base al filmato aggiunto più di recente da un visitatore alla coda.

1. Seleziona l&#39;attributo di profilo personalizzato dall&#39;elenco a discesa **[!UICONTROL Chiave consiglio]** (ad esempio, &quot;**[!UICONTROL Ultimo spettacolo aggiunto alla watchlist]**&quot;).

1. Seleziona la **[!UICONTROL Logica consigli]** (ad esempio, &quot;**[!UICONTROL Persone che hanno visualizzato questo, hanno visualizzato anche quello]**&quot;).

Se l&#39;attributo di profilo personalizzato non corrisponde direttamente a un singolo ID entità, specificare come [!DNL Recommendations] corrisponde a un&#39;entità. Ad esempio, per visualizzare gli articoli più venduti della marca preferita di un visitatore:

1. Seleziona l&#39;attributo di profilo personalizzato dall&#39;elenco a discesa **[!UICONTROL Chiave consiglio]** (ad esempio, &quot;Marchio preferito&quot;).

1. Seleziona la **[!UICONTROL Logica consigli]** da utilizzare con questa chiave (ad esempio, &quot;**[!UICONTROL Più venduti]**&quot;).

   Viene visualizzata l&#39;opzione **[!UICONTROL Raggruppa per valore univoco di]**.

1. Seleziona l’attributo di entità che corrisponde alla chiave scelta. In questo caso &quot;**[!UICONTROL Marchio preferito]**&quot; corrisponde a `entity.brand`.

   [!DNL Recommendations] ora genera un elenco &quot;**[!UICONTROL Più venduti]**&quot; per ogni marchio e mostra al visitatore l&#39;elenco &quot;**[!UICONTROL Più venduti]**&quot; appropriato in base al valore memorizzato nell&#39;attributo di profilo **[!UICONTROL Marchio preferito]** del visitatore.

### [!UICONTROL Affinità sito] {#site-affinity}

Consiglia gli articoli in base alla certezza di una relazione tra articoli diversi. Questo criterio può essere configurato per impostare la quantità di dati necessari prima della visualizzazione di un consiglio, utilizzando il cursore **[!UICONTROL Regole di inclusione]**. Ad esempio, quando viene selezionato molto forte, si consigliano i prodotti con la maggiore certezza di corrispondenza.

Ad esempio, se è impostata un’affinità molto forte e la progettazione include cinque elementi, tre dei quali soddisfano il livello di soglia di connessione, i due elementi che non soddisfano i requisiti di forza minima non vengono visualizzati nei consigli e vengono sostituiti dagli elementi di backup definiti. Gli elementi con affinità più elevata vengono visualizzati per primi.

Un altro esempio è dato dal fatto che un retailer online può consigliare elementi nelle visite successive a cui un visitatore ha mostrato interesse durante le sessioni precedenti. L’attività per ogni sessione del visitatore viene acquisita per calcolare un’affinità in base a un modello di frequenza e recency. Quando il visitatore ritorna sul sito, l’affinità viene utilizzata per visualizzare i consigli in base alle azioni passate eseguite sul sito.

Una debole affinità tra siti potrebbe fornire i risultati migliori per i clienti con diverse raccolte di prodotti e comportamenti diversi sui siti.

Questa logica può essere utilizzata con le seguenti chiavi di consigli: **[!UICONTROL Articolo corrente]**, **[!UICONTROL Ultimo articolo acquistato]**, **[!UICONTROL Ultimo articolo visualizzato]**, **[!UICONTROL Articolo più visualizzato]**.
