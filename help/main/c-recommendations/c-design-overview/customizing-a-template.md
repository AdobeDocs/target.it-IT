---
keywords: progettazione personalizzata;velocity;decimale;virgola;personalizzare una progettazione
description: Scopri come utilizzare il linguaggio di progettazione open-source [!DNL Velocity] per personalizzare le progettazioni dei consigli in [!DNL Target] Recommendations.
title: Personalizzare una progettazione con Velocity
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
exl-id: 035d7988-80d8-4080-bb0d-1d0e9f8856d1
TQID: 'https://experienceleague.adobe.com/cccBRfwqqn-eL2hraSDAoJHPYSCkcA9tVne3OWDXxEU'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: f9c9c7b2b78ec020fcabae420686b8955e350a0e
workflow-type: tm+mt
source-wordcount: '1086'
ht-degree: 21%
---
# Personalizzare una progettazione utilizzando [!DNL Velocity] {#customize-design}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come utilizzare il linguaggio di progettazione [!DNL Velocity] open-source per personalizzare le progettazioni dei consigli in [!DNL Adobe Target Recommendations].

>[!ENDSHADEBOX]

## Panoramica di [!DNL Velocity] {#velocity-overview}

Le informazioni su [!DNL Velocity] sono disponibili all&#39;indirizzo [https://velocity.apache.org](https://velocity.apache.org).

Tutta la logica, la sintassi e così via di [!DNL Velocity] può essere utilizzata per la progettazione di un consiglio. È quindi possibile creare *per* cicli, *istruzioni if* e altro codice con [!DNL Velocity] anziché con JavaScript.

Gli attributi di entità inviati a [!DNL Recommendations] nella mbox `productPage` o il caricamento del file CSV possono essere visualizzati in una progettazione, ad eccezione degli attributi con più valori. È possibile inviare qualsiasi tipo di attributo; tuttavia, [!DNL Target] non passa attributi di tipo &quot;multivalore&quot; come array su cui una progettazione può iterare (ad esempio `entityN.categoriesList`).

A questi valori viene fatto riferimento con la seguente sintassi:

```
$entityN.variable
```

I nomi degli attributi di entità devono seguire la notazione abbreviata [!DNL Velocity], costituita da un carattere iniziale *$*, seguito da un identificatore VTL (Template Language) [!DNL Velocity]. L&#39;identificatore VTL deve iniziare con un carattere alfabetico (a-z o A-Z).

I nomi degli attributi di entità [!DNL Velocity] sono limitati ai seguenti tipi di caratteri:

* Alfabetico (a-z, A-Z)
* Numerico (0-9)
* Trattino ( - )
* Sottolineatura (_)

I seguenti attributi sono disponibili come array [!DNL Velocity]. Di conseguenza, possono essere iterati o referenziati tramite un indice.

* `entities`
* `entityN.categoriesList`

Ad esempio:

```
#foreach ($category in $entity1.categoriesList) 
<br/>$category 
#end
```

Oppure

```
#if ($entities[0].categoriesList.size() >= 3 ) 
$entities[0].categoriesList[2] 
#end
```

Per ulteriori informazioni sulle variabili (attributi) [!DNL Velocity], consulta la [documentazione Velocity](https://velocity.apache.org/engine/releases/velocity-1.7/user-guide.html#variables).

Se uno script di profilo viene utilizzato in una progettazione, il $ che precede il nome dello script deve essere preceduto da una barra rovesciata (`\`). Ad esempio:

`\${user.script_name}`

>[!NOTE]
>
>Il numero massimo di entità a cui è possibile fare riferimento in una progettazione, tramite codifica fissa o cicli, è 99. Lo script di progettazione può contenere fino a 65.000 caratteri.

Una progettazione che visualizza qualcosa di simile alla seguente illustrazione:

![Esempio di un design 4 x 1 intitolato &quot;Altre attività divertenti&quot;, con quattro elementi ciascuno dei quali mostra una foto, un nome, un prezzo, una valutazione e una distanza](/help/main/c-recommendations/c-design-overview/assets/velocity_example.png)

può utilizzare il seguente codice:

```
<table style="border:1px solid #CCCCCC;"> 
<tr> 
<td colspan="3" style="font-size: 130%; border-bottom:1px solid  
#CCCCCC;"> You May Also Like... </td> 
</tr> 
<tr> 
<td style="border-right:1px solid #CCCCCC;"> 
<div class="search_content_inner" style="border-bottom:0px;"> 
<div class="search_title"><a href="$entity1.pageUrl"  
style="color: rgb(112, 161, 0); font-weight: bold;"> 
$entity1.id</a></div> 
By $entity1.message <a href="?x14=brand;q14=$entity1.message"> 
(More)</a><br/> 
sku: $entity1.prodId<br/> Price: $$entity1.value 
<br/><br/> 
</div> 
</td> 
<td style="border-right:1px solid #CCCCCC; padding-left:10px;"> 
<div class="search_content_inner" style="border-bottom:0px;">  
<div class="search_title"><a href="$entity2.pageUrl"  
style="color: rgb(112, 161, 0); font-weight: bold;"> 
$entity2.id</a></div> 
By $entity2.message <a href="?x14=brand;q14=$entity2.message"> 
(More)</a><br/> 
sku: $entity2.prodId<br/> 
Price: $$entity2.value 
<br/><br/> 
</div> 
</td> 
<td style="padding-left:10px;"> 
<div class="search_content_inner" style="border-bottom:0px;"> 
<div class="search_title"><a href="$entity3.pageUrl"  
style="color: rgb(112, 161, 0); font-weight: bold;"> 
$entity3.id</a></div> 
By $entity3.message <a href="?x14=brand;q14=$entity3.message"> 
(More)</a><br/> 
sku: $entity3.prodId<br/> Price: $$entity3.value 
<br/><br/> 
</div> 
</td> 
</tr>  
</table>
```

>[!NOTE]
>
>Per aggiungere testo dopo il valore di un attributo, prima di un tag che indica che il nome dell’attributo è stato completato, utilizza la notazione formale per racchiudere il nome dell’attributo. Ad esempio: `${entity1.thumbnailUrl}.gif`.

`algorithm.name` e `algorithm.dayCount` possono essere utilizzati anche come attributi di entità nelle progettazioni, in modo che una progettazione possa essere utilizzata per testare più criteri e il nome dei criteri possa essere visualizzato dinamicamente nella progettazione. Questo mostra al visitatore che il visitatore sta guardando &quot;articoli più venduti&quot; o &quot;persone che hanno visto questo hanno acquistato anche quello&quot;. È inoltre possibile visualizzare `dayCount` (il numero di giorni di dati utilizzati nel criterio, ad esempio &quot;articoli più venduti negli ultimi 2 giorni&quot;).

## Utilizzo dei numeri nelle progettazioni di [!DNL Velocity] {#numbers}

Per impostazione predefinita, le progettazioni di [!DNL Velocity] trattano tutti gli attributi di entità come valori stringa. Un attributo di entità potrebbe dover essere trattato come un valore numerico per eseguire un’operazione matematica o per confrontarlo con un altro valore numerico. Per trattare un attributo di entità come valore numerico, effettua le seguenti operazioni:

1. Dichiara una variabile fittizia e inizializzala in un valore arbitrario intero (int) o con precisione doppia (double).
1. Verificare che l&#39;attributo di entità da utilizzare non sia vuoto (necessario affinché il parser di progettazione di [!DNL Target Recommendations] possa convalidare e salvare la progettazione).
1. Passa l&#39;attributo dell&#39;entità nel metodo `parseInt` o `parseDouble` della variabile fittizia creata nel passaggio 1 per trasformare la stringa in un valore intero o con precisione doppia.
1. Esegui l’operazione matematica o il confronto sul nuovo valore numerico.

### Esempio: calcolo di un prezzo scontato

Per ridurre il prezzo visualizzato di un articolo di $0,99 per applicare uno sconto, è possibile utilizzare il seguente approccio:

```
#set( $double = 0.1 )

#if( $entity1.get('priceBeforeDiscount') != '' )
    #set( $discountedPrice = $double.parseDouble($entity1.get('priceBeforeDiscount')) - 0.99 )
    Item price: $$discountedPrice
#else
    Item price unavailable
#end
```

### Esempio: scelta del numero di stelle da visualizzare in base alla valutazione di un elemento

Per visualizzare un numero appropriato di stelle in base alla valutazione numerica media dei clienti di un articolo, è possibile utilizzare il seguente approccio:

```
#set( $double = 0.1 )

#if( $entity1.get('rating') != '' )
    #set( $rating = $double.parseDouble($entity1.get('rating')) )
    #if( $rating >= 4.5 )
        <img src="5_stars.jpg">
    #elseif( $rating >= 3.5 )
        <img src="4_stars.jpg">
    #elseif( $rating >= 2.5 )
        <img src="3_stars.jpg">
    #elseif( $rating >= 1.5 )
        <img src="2_stars.jpg">
    #else
        <img src="1_star.jpg">
    #end
#else
    <img src="no_rating_default.jpg">
#end
```

### Esempio: calcolo del tempo in ore e minuti in base alla lunghezza in minuti di un elemento

Per visualizzare la lunghezza di un filmato in ore e minuti quando la lunghezza è memorizzata in minuti, è possibile utilizzare il seguente approccio:

```
#if( $entity1.get('length_minutes') )
#set( $Integer = 1 )
#set( $nbr = $Integer.parseInt($entity1.get('length_minutes')) )
#set( $hrs = $nbr / 60)
#set( $mins = $nbr % 60)
#end
```

## Visualizzazione di un elemento chiave con i prodotti consigliati {#key-item}

Una progettazione può mostrare l’elemento chiave insieme agli altri prodotti consigliati. Ad esempio, l’elemento corrente può essere visualizzato come riferimento accanto ai consigli.

A questo scopo, crea una colonna nella progettazione che utilizzi l&#39;attributo `$key` su cui si basa il consiglio, invece dell&#39;attributo `$entity`. Ad esempio, il codice per la colonna chiave potrebbe essere simile al seguente:

```
<div class="at-table-column"> 
   <a href="$key.pageURL"> 
      <img src=$key.thumbnailUrl" class="at-thumbnail"/> 
      <br/><h3>$key.name</h3> 
      <br/><p class="at-light">$key.message</p> 
      <br/><p class="at-light">$key.value</p> 
   </a> 
</div>
```

Il risultato è una progettazione come la seguente, dove una colonna mostra l&#39;elemento chiave.

![Progettare con quattro colonne, in cui la prima colonna mostra l&#39;elemento chiave contrassegnato come prodotto corrente](/help/main/c-recommendations/c-design-overview/assets/rec_key.png)

Quando viene creata un&#39;attività [!DNL Recommendations], se l&#39;elemento chiave viene ricavato dal profilo del visitatore, ad esempio &quot;ultimo articolo acquistato&quot;, [!DNL Target] visualizza un prodotto casuale nel **[!UICONTROL Compositore esperienza visivo]**. Questo perché un profilo non è disponibile mentre l’attività è progettata. Quando i visitatori visualizzano la pagina, visualizzano l’elemento chiave previsto.

## Esecuzione di sostituzioni in un valore stringa {#replacements}

Una progettazione può sostituire i valori all’interno di una stringa. Ad esempio, il delimitatore a punti decimali utilizzato negli Stati Uniti può essere sostituito con il delimitatore a virgola utilizzato in Europa e in altri paesi.

Il codice seguente mostra una riga singola in un esempio di prezzo di vendita condizionale:

```
<span class="price">$entity1.value.replace(".", ",") &euro;</span><br>
```

Il codice seguente è un esempio completo di prezzo di vendita:

```
<div class="price"> 
    #if($entity1.hasSalesprice==true) 
    <span class="old">Statt <s>$entity1.salesprice.replace(".", ",") &euro;</s></span><br> 
    <span style="font-size: 10px; float: left;">jetzt nur</span> $entity1.value.replace(".", ",") &euro;<br> #else 
    <span class="price">$entity1.value.replace(".", ",") &euro;</span><br> #end 
    <span style="font-weight:normal; font-size:10px;"> 
                                        $entity1.vatclassDisplay 
                                        <br/> 
                                        $entity1.delivery 
                                        <br> 
                                    </span>
</div>
```

## Personalizzazione delle dimensioni di progettazione e verifica della presenza di valori vuoti {#default}

Uno script [!DNL Velocity] può controllare il dimensionamento dinamico della visualizzazione dell&#39;entità. La progettazione seguente gestisce un risultato &quot;da 1 a molti&quot; per evitare la creazione di elementi HTML vuoti quando non vengono restituite abbastanza entità corrispondenti da [!DNL Recommendations]. Questo script è adatto per gli scenari in cui non avrebbe senso utilizzare consigli di backup e **[!UICONTROL È abilitato il rendering design parziale]**.

Il seguente snippet HTML sostituisce la porzione HTML esistente nella progettazione predefinita da 4x2 (qui non è stato incluso il CSS per motivi di brevità):

* Se esiste una quinta entità, lo script inserisce un div di chiusura e apre una nuova riga con `<div class="at-table-row">`.
* Con 4x2, il numero massimo di risultati visualizzati è otto, ma questo può essere personalizzato per elenchi più piccoli o più grandi modificando `$count <=8`.
* La logica non bilancia le entità su più righe. Ad esempio, se devono essere visualizzate cinque o sei entità, queste non diventano dinamicamente tre in alto e due in basso (o tre in alto e tre in basso). Nella riga superiore vengono visualizzati quattro elementi prima di iniziare una seconda riga.

```
<div class="at-table">
  <div class="at-table-row">
    #set($count=1) 
    #foreach($e in $entities)  
        #if($e.id != "" && $count < $entities.size() && $count <=8) 
            #if($count==5) 
                </div>
                <div class="at-table-row">
            #end
            <div class="at-table-column">
                <a href="$e.pageUrl"><img src="$e.thumbnailUrl" class="at-thumbnail" />
                    <br/>
                    <h3>$e.name</h3>
                    <br/>
                    <p class="at-light">$e.message</p>
                    <br/>
                    <p class="at-light">$$e.value</p>
                </a>
            </div>
            #set($count = $count + 1) 
        #end 
    #end
  </div>
</div>
```
