---
keywords: inclusion rules;inclusion criteria;recommendations;create new criteria;promotion;promotions;dynamic filtering;dynamic;empty values;ignore filtering rule;static filter;filter by value;entity attribute matching;profile attribute matching;parameter matching;filter by value;static filter
description: Informazioni sulla creazione di regole di inclusione in  Adobe Target Recommendations per criteri e promozioni e sull'aggiunta di ulteriori regole di filtro dinamiche o statiche per ottenere risultati migliori.
title: Utilizzare regole di inclusione dinamiche e statiche in  Adobe Target Recommendations
feature: criteria
mini-toc-levels: 3
uuid: f0ee2086-1126-44a4-9379-aa897dc0e06b
translation-type: tm+mt
source-git-commit: 2d7435c420326a7eb1a59c95befa87b06c7614c8
workflow-type: tm+mt
source-wordcount: '2125'
ht-degree: 34%

---


# ![PREMIUM](/help/assets/premium.png) Utilizzare regole di inclusione dinamiche e statiche{#use-dynamic-and-static-inclusion-rules}

Informazioni sulla creazione di regole di inclusione per criteri e promozioni in  Adobe Target e sull&#39;aggiunta di ulteriori regole di filtro dinamiche o statiche per ottenere risultati migliori per le raccomandazioni.

Le regole di inclusione per i criteri e le promozioni possono essere create e utilizzate con processi simili, così come sono simili i rispettivi casi ed esempi di utilizzo. Questo argomento tratta i criteri e le promozioni, nonché l’utilizzo delle regole di inclusione.

## Aggiunta di regole di filtro ai criteri {#section_CD0D74B8D3BE4A75A78C36CF24A8C57F}

Durante la [creazione di criteri](../../c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE), fai clic su **[!UICONTROL Aggiungi regola di filtro]** in **[!UICONTROL Regole di inclusione]**.

![](assets/inclusion_options_new.png)

Le opzioni disponibili dipendono dal settore verticale selezionato e della chiave consiglio.

## Aggiunta di regole di filtro alle promozioni {#section_D59AFB62E2EE423086281CF5D18B1076}

Durante la [creazione di una promozione](../../c-recommendations/t-create-recs-activity/adding-promotions.md#task_CC5BD28C364742218C1ACAF0D45E0E14), seleziona **[!UICONTROL Promuovi per attributo]**, quindi fai clic su **[!UICONTROL Aggiungi regola filtro]**.

![](assets/inclusion_options.png)

## Tipi di filtro {#section_0125F1ED10A84C0EB45325122460EBCD}

Nella tabella seguente sono elencati i tipi di opzioni di filtro per criteri e promozioni:

### Filtraggio dinamico

Le regole di inclusione dinamica sono più potenti delle regole di inclusione statica e producono risultati e coinvolgimento migliori. Considera i seguenti aspetti:

* Le regole di inclusione dinamica distribuiscono le raccomandazioni facendo corrispondere un attributo nel parametro di profilo di un utente o in una chiamata mbox.

   Ad esempio, potete creare una raccomandazione Criteri più popolari e quindi del set di raccomandazioni restituite, escluderne una in tempo reale rispetto a un attributo passato quando l&#39;utente accede a una pagina in cui vengono visualizzate le raccomandazioni.

* Utilizzate le regole statiche per limitare gli elementi inclusi nella raccomandazione (invece delle raccolte).

* Potete creare tutte le regole di inclusione dinamica necessarie. Le regole di inclusione vengono collegate mediante un operatore E. Gli articoli verranno inclusi in un consiglio solo se vengono soddisfatte tutte le regole.

Per il filtro dinamico sono disponibili le seguenti opzioni:

#### Corrispondenza attributo entità

Filtrare in modo dinamico confrontando un insieme di potenziali elementi delle raccomandazioni con un elemento specifico con cui gli utenti hanno interagito.

Ad esempio, consigliamo solo gli elementi che corrispondono al marchio dell&#39;elemento corrente, come nell&#39;esempio seguente:

Se la mbox su una pagina di destinazione del marchio restituisce `entity.brand=Nike`, solo i prodotti Nike vengono restituiti e visualizzati sulla pagina. Analogamente, nella pagina di destinazione del marchio per gli Adidas, vengono restituiti solo i prodotti Adidas. Con questo tipo di regola di inclusione dinamica, l&#39;utente deve solo specificare una regola di raccomandazione che restituisca i risultati rilevanti del marchio in tutte le pagine del marchio, invece di specificare una raccolta o un filtro statico per corrispondere al nome del marchio.

#### Corrispondenza attributo profilo

Filtrare in modo dinamico confrontando elementi (entità) con un valore nel profilo dell&#39;utente.

Utilizzate la corrispondenza [!UICONTROL attributo] profilo per mostrare le raccomandazioni che corrispondono a un valore memorizzato nel profilo del visitatore, ad esempio dimensione o marchio preferito.

Gli scenari seguenti mostrano come utilizzare la corrispondenza attributi [!UICONTROL profilo]:

* Una società che vende occhiali memorizza il colore di fotogramma preferito di un visitatore come &quot;noce&quot;. Per quel visitatore specifico, le raccomandazioni sono configurate per restituire solo i fotogrammi della lente di occhio che corrispondono a &quot;noce&quot; nel colore.
* Un parametro di profilo può essere definito per la dimensione dell’abbigliamento (ad esempio, Piccolo, Medio o Grande) di un visitatore che naviga nel sito Web della società. È possibile impostare una raccomandazione in modo che corrisponda al parametro del profilo e restituire prodotti specifici solo per le dimensioni di abbigliamento preferite dall&#39;utente.

Per ulteriori esempi e istruzioni, consulta Esempi [di corrispondenza attributi](#section_9873E2F22E094E479569D05AD5BB1D40) profilo di seguito.

#### Corrispondenza parametro

Filtrare in modo dinamico confrontando elementi (entità) con un valore nella richiesta (API o mbox).

Ad esempio, si consiglia solo il contenuto che corrisponde al parametro di pagina &quot;industria&quot; o ad altri parametri, come le dimensioni del dispositivo o la geolocalità, come negli esempi seguenti.

* I parametri Mbox per la larghezza e l&#39;altezza dello schermo possono essere utilizzati per i visitatori di dispositivi mobili e consigliamo solo dispositivi mobili e accessori.
* I parametri di geolocalizzazione regionali possono essere utilizzati per restituire raccomandazioni per gli strumenti durante l&#39;inverno. I soffiatori di neve e altri strumenti di riduzione della neve possono essere raccomandati per i visitatori in aree dove nevica ma non consigliato per i visitatori in aree dove non neve.

>[!NOTE]
>
>Se l&#39;attività è stata creata prima del 31 ottobre 2016, la sua distribuzione non riuscirà se utilizza il filtro &quot;Parametro Matching&quot;. Per risolvere questo problema:
>
>* Crea una nuova attività e aggiungi i relativi criteri.
>* Utilizza un criterio che non contenga il filtro “Corrispondenza parametro”.
>* Rimuovi il filtro “Corrispondenza parametro” dai criteri.


Operatori disponibili:

* è uguale a
* è diverso da
* contiene
* non contiene
* inizia con
* termina con
* è maggiore o uguale a
* è minore o uguale a
* è tra

### Filtra per valore

L&#39;opzione seguente è disponibile per il filtro dinamico:

#### Filtro statico

Immettere manualmente uno o più valori statici da filtrare.

Ad esempio, per consigliare solo i contenuti con una classificazione MPAA di “G” o “PG”.

Operatori disponibili:

* è uguale a
* è diverso da
* contiene
* non contiene
* inizia con
* termina con
* è presente un valore
* il valore non è presente
* è maggiore o uguale a
* è minore o uguale a

>[!NOTE]
>
>Se hai dimestichezza con la configurazione delle regole di inclusione prima della versione di Target 17.6.1 (giugno 2017), noterai che alcune delle opzioni e degli operatori sono cambiati. Vengono visualizzati solo gli operatori applicabili all’opzione selezionata; alcuni altri operatori sono stati rinominati (“corrisponde a” è ora “è uguale a”), per maggiore coerenza e intuitività. Tutte le regole di esclusione esistenti create prima di questa versione sono state automaticamente convertite nella nuova struttura. Non è necessaria alcuna modifica da parte dell’utente.

È possibile creare tutte le regole di inclusione necessarie. Le regole di inclusione vengono collegate mediante un operatore E. Gli articoli verranno inclusi in un consiglio solo se vengono soddisfatte tutte le regole.

## Criteri dinamici ed esempi di promozione

I criteri e le promozioni dinamici sono molto più potenti dei criteri e delle promozioni statici; producono risultati migliore e un maggiore coinvolgimento del visitatore.

I seguenti esempi ti daranno idee su come utilizzare le promozioni dinamiche nelle tue attività di marketing:

### È uguale a

Utilizzando l&#39;operatore &quot;uguale&quot; nelle promozioni dinamiche, quando un visitatore visualizza un elemento sul sito Web (ad esempio un prodotto, un articolo o un filmato) potete promuovere altri elementi da:

* lo stesso marchio
* la stessa categoria
* la stessa categoria E lo stesso marchio
* lo stesso store

### Non uguale

Utilizzando l&#39;operatore &quot;non uguale&quot; nelle promozioni dinamiche, quando un visitatore visualizza un elemento sul sito Web (ad esempio un prodotto, un articolo o un filmato) potete promuovere altri elementi da:

* una serie TV diversa
* un genere diverso
* una serie di prodotti diversi
* un ID di stile diverso

### È tra

Utilizzando l&#39;operatore &quot;è compreso&quot; nelle promozioni dinamiche, quando un visitatore visualizza un elemento sul sito Web (ad esempio un prodotto, un articolo o un filmato) potete promuovere altri elementi:

* più costosi
* meno costosi
* più o meno costosi del 30%
* episodi successivi nella stessa stagione
* libri precedenti in una collana

## Handling empty values when filtering by Entity Attribute Matching, Profile Attribute Matching, and Parameter Matching {#section_7D30E04116DB47BEA6FF840A3424A4C8}

You can choose several options to handle empty values when filtering by [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching], and [!UICONTROL Parameter Matching] for exit criteria and promotions.

In precedenza, non veniva restituito alcun risultato se un valore era vuoto. L&#39;elenco a discesa “Se *x* è vuoto” consente di scegliere l&#39;azione da eseguire se i criteri hanno valori vuoti, come illustrato di seguito:

![](assets/empty_value.png)

Per selezionare l’azione desiderata, passa il puntatore sull’icona ingranaggio (![](assets/icon_gear.png)), quindi scegli l’azione desiderata:

| Azione | Disponibile per | Dettagli |
|--- |--- |--- |
| Ignora questa regola di filtro | Corrispondenza attributo profilo<br>Corrispondenza parametro | Questa è l&#39;azione predefinita per Corrispondenza attributo profilo e Corrispondenza parametro.<br>Questa opzione specifica che la regola viene ignorata. Ad esempio, se sono presenti tre regole di filtro e la terza regola non passa alcun valore, invece di non restituire alcun risultato si può semplicemente ignorare la terza regola con valori vuoti. |
| Non promuovere alcun elemento | Corrispondenza attributo di entità<br>con attributo<br>di profilo di profilo | Questa è l&#39;azione predefinita per Corrispondenza attributo entità.<br>[!DNL Target]Corrisponde al modo in cui gestiva i valori vuoti prima dell’aggiunta di questa opzione, ossia non verrà visualizzato alcun risultato per questo criterio. |
| Usa un valore statico | Corrispondenza attributo entità<br>Corrispondenza attributo profilo<br>Corrispondenza parametro | Se un valore è vuoto, è possibile scegliere di utilizzare un valore statico. |

## Esempi di corrispondenza attributi profilo {#section_9873E2F22E094E479569D05AD5BB1D40}

[!UICONTROL La corrispondenza] attributi profilo consente di consigliare solo gli elementi che corrispondono a un attributo del profilo del visitatore, come negli esempi seguenti.

### Esempio 1: Suggerimento di elementi dal marchio preferito dell&#39;utente

For example, you can use the [!UICONTROL Profile Attribute Matching] option to create a rule that recommends items only where the brand equals the value or text stored in `profile.favoritebrand`. Con tale regola, se un visitatore cerca dei pantaloncini da corsa di una data marca, i consigli che verranno visualizzati proporranno articoli della marca preferita dell’utente (in base al valore memorizzato in `profile.favoritebrand` nel profilo del visitatore).

```
Profile Attribute Matching
brand - equals - the value/text stored in - profile.favoritebrand
```

### Esempio 2: Corrispondenza tra posti di lavoro e persone in cerca di lavoro

Supponiamo che tu stia cercando di abbinare i lavori a chi cerca lavoro. Si consiglia solo i lavori che si trovano nella stessa città di chi cerca lavoro.

Potete utilizzare le regole di inclusione per far corrispondere la posizione di un cercatore di lavoro dal profilo del visitatore a un elenco di processi, come nell&#39;esempio seguente:

```
Profile Attribute Matching
jobCity - equals - the value/text stored in - profile.usersCity
```

### Esempio 3: Suggerimento di vestiti che corrispondono alle dimensioni di un visitatore

Vediamo un esempio per raccomandare vestiti che corrispondono alla dimensione dell&#39;abbigliamento impostata nel profilo del visitatore.

La pagina del prodotto invia `entity.size` nella chiamata mbox (freccia rossa nell&#39;illustrazione seguente).

Potete creare uno script [di](/help/c-target/c-visitor-profile/profile-parameters.md) profilo per acquisire gli attributi e i valori del profilo del visitatore dall&#39;ultima pagina visitata dal visitatore.

Ad esempio,

```
if ((mbox.name=="target-global-mbox") &&(mbox.param('entity.size') == 'small')) { return 'small';
}

else if ((mbox.name=="target-global-mbox") &&(mbox.param('entity.size') == 'medium')) { return 'medium';
}

else if ((mbox.name=="target-global-mbox") &&(mbox.param('entity.size') == 'large')) { return 'large';
}
```

Lo script di profilo acquisisce il `entity.size` valore dalla mbox denominata `target-global-mbox` e lo restituisce come attributo di profilo denominato `user.size` (freccia blu nell&#39;illustrazione seguente).

![chiamata mbox size](/help/c-recommendations/c-algorithms/assets/size.png)

Quando create i criteri di raccomandazione, fate clic su [!UICONTROL Aggiungi regola]di filtro, quindi selezionate Corrispondenza attributi [!UICONTROL profilo].

![Attributo profilo corrispondente a illustrazione](/help/c-recommendations/c-algorithms/assets/profile-attribute-matching.png)

Se il `user.size` profilo è stato caricato in [!DNL Target], viene visualizzato nell&#39;elenco a discesa per la corrispondenza quando si imposta la regola in modo che corrisponda al valore passato nella chiamata mbox (`size`) al nome dello script di profilo (`user.size`).

Potete quindi selezionare &quot;size&quot; &quot;equals&quot; (uguale a) il valore/testo memorizzato in &quot;user.size&quot; per l&#39;attributo di profilo corrispondente.

Una volta create le regole degli attributi di profilo, queste filtreranno tutte le raccomandazioni che hanno attributi che non corrispondono all&#39;attributo di profilo memorizzato del visitatore.

### Esempio 4: Raccomanda gli elementi in base alle dimensioni

Per un esempio visivo del modo in cui la corrispondenza dell&#39;attributo di profilo influisce sulle raccomandazioni, prendete in considerazione un sito Web che vende fan.

Quando un visitatore fa clic su diverse immagini dei fan su questo sito Web, ogni pagina imposta il valore del `entity.size` parametro in base al fatto che le dimensioni della ventola nell’immagine siano piccole o grandi.

Si supponga di aver creato uno script di profilo per tenere traccia e contare il numero di volte in cui il valore di `entity.size` è impostato su piccolo o su grande.

Se il visitatore ritorna quindi alla Home Page, visualizzerà le raccomandazioni filtrate in base al fatto che sia stato fatto clic su un maggior numero di fan piccoli o grandi.

Recommendations basato sulla visualizzazione di più piccole fan sul sito Web:

![raccomandazioni per i piccoli ventilatori](/help/c-recommendations/c-algorithms/assets/small-fans.png)

Recommendations basato sulla visualizzazione di più grandi fan sul sito Web:

![raccomandazioni per i fan di grandi dimensioni](/help/c-recommendations/c-algorithms/assets/large-fans.png)

## Esempi di corrispondenza attributi entità

[!UICONTROL La corrispondenza] attributi entità consente di consigliare solo gli elementi che corrispondono a un attributo dell&#39;elemento che l&#39;utente sta visualizzando, l&#39;elemento visualizzato più di recente dall&#39;utente, l&#39;elemento acquistato più di recente dall&#39;utente, l&#39;elemento visualizzato più di frequente dall&#39;utente o da un elemento memorizzato in un attributo personalizzato nel profilo del visitatore, come negli esempi seguenti.

### Esempio 5: Upselling per un prodotto più costoso

Supponiamo di essere un rivenditore di abbigliamento e di voler incoraggiare gli utenti a considerare articoli più costosi e, quindi, più redditizi. È possibile utilizzare gli operatori &quot;uguale&quot; e &quot;è tra&quot; per promuovere elementi più costosi appartenenti alla stessa categoria e allo stesso marchio. Ad esempio, un rivenditore di scarpe può promuovere scarpe da ginnastica più costose nel tentativo di up-sell di un visitatore che guarda scarpe da corsa.

```
Entity Attribute Matching
category - equals - current item's - category 
And 
Entity Attribute Matching
brand - equals - current item's - brand 
And 
Entity Attribute Matching
value - is between - 100% and 1000% of - current item's - value
```

### Esempio 6: Promozione di prodotti con etichette private

Potete combinare filtri dinamici e statici per promuovere i prodotti con etichette private. Ad esempio, una società di fornitura di uffici può promuovere le cartucce toner del marchio della casa dell&#39;azienda per condurre una vendita più redditizia per un visitatore che guarda il toner — e promuovere penne del marchio della casa dell&#39;azienda per guidare una vendita più redditizia per un visitatore che guarda le penne.

```
Entity Attribute Matching
category - equals - current item's - category 
And
Static Filter
IsHouseBrand - equals - true
```

## Avvertenze {#section_A889FAF794B7458CA074DEE06DD0E345}

>[!IMPORTANT]
>
>Gli attributi di tipi di dati diversi potrebbero non essere compatibili nelle promozioni o nei criteri dinamici in fase di esecuzione con gli operatori “è uguale a” e “è diverso da”. You should use [!UICONTROL Value], [!UICONTROL Margin], [!UICONTROL Inventory], and [!UICONTROL Environment] values wisely on the right hand side if the left hand side has predefined attributes or custom attributes.

![](assets/left_right.png)

Nella tabella seguente vengono mostrate regole efficaci e regole che potrebbero invece non essere compatibili in fase di esecuzione:

| Regole compatibili | Regole potenzialmente non compatibili |
|--- |--- |
| value - è tra - 90% e 110% dell’articolo corrente - salesValue | salesValue - è tra - 90% e 110% dell’articolo corrente - value |
| value - è tra - 90% e 110% dell’articolo corrente - value | clearancePrice - è tra - 90% e 110% dell’articolo corrente - margin |
| margin - è tra - 90% e 110% dell’articolo corrente - margin | storeInventory - è uguale a - dell’articolo corrente - inventory |
| inventory - è uguale a - dell’articolo corrente - inventory |  |
