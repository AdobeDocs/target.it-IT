---
keywords: custom design;velocity;decimal;comma;customize design
description: Utilizza il linguaggio di progettazione open-source Velocity per personalizzare le progettazioni dei consigli.
title: Personalizzare una progettazione con Velocity
uuid: 80701a15-c5eb-4089-a92e-117eda11faa2
translation-type: tm+mt
source-git-commit: 32217a752574f671b790880667ac869443778f51
workflow-type: tm+mt
source-wordcount: '1010'
ht-degree: 65%

---


# ![PREMIUM](/help/assets/premium.png) Personalizzare una progettazione con Velocity{#customize-a-design-using-velocity}

Utilizza il linguaggio di progettazione open-source Velocity per personalizzare le progettazioni dei consigli.

## Panoramica di Velocity {#section_C431ACA940BC4210954C7AEFF6D03EA5}

Le informazioni su Velocity sono disponibili all’indirizzo [](https://velocity.apache.org)https://velocity.apache.org.

La logica, la sintassi e altro di Velocity possono essere utilizzati integralmente per la progettazione di un consiglio. Ciò significa che è possibile creare cicli *for*, istruzioni *If* e altro codice utilizzando Velocity anziché JavaScript.

È possibile visualizzare qualsiasi variabile inviata a [!DNL Recommendations] nella mbox `productPage` o il caricamento del file CSV in una progettazione. A questi valori viene fatto riferimento con la seguente sintassi:

```
$entityN.variable
```

I nomi delle variabili devono seguire la notazione abbreviata di Velocity, costituita da un carattere iniziale *$*, seguito da un identificatore VTL (Velocity Template Language). L&#39;identificatore VTL deve iniziare con un carattere alfabetico (a-z o A-Z).

I nomi delle variabili di Velocity sono limitati ai seguenti tipi di caratteri:

* Alfabetico (a-z, A-Z)
* Numerico (0-9)
* Trattino ( - )
* Sottolineatura (_)

Le seguenti variabili sono disponibili come array di Velocity. In quanto tali, possono essere iterati o referenziati tramite index.

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

Per ulteriori informazioni sulle variabili di Velocity, consulta [https://velocity.apache.org/engine/releases/velocity-1.7/user-guide.html#variables](https://velocity.apache.org/engine/releases/velocity-1.7/user-guide.html#variables).

Se utilizzi uno script di profilo nella progettazione, il $ che precede il nome dello script deve essere annullato con un \. Ad esempio, `\${user.script_name}`.

>[!NOTE]
>
>Il numero massimo di entità a cui puoi fare riferimento in una progettazione, tramite codifica fissa o cicli, è 99. La lunghezza dello script del modello può contenere fino a 65.000 caratteri.

Ad esempio, se desideri una progettazione che mostri qualcosa di simile a quanto segue:

![](assets/velocity_example.png)

puoi utilizzare il codice seguente:

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
>Se desiderate aggiungere del testo dopo il valore di una variabile prima che un tag che indichi che il nome della variabile è terminato, potete farlo utilizzando la notazione formale per racchiudere il nome della variabile. Ad esempio: `${entity1.thumbnailUrl}.gif`.

Puoi inoltre utilizzare `algorithm.name` e `algorithm.dayCount` come variabili nelle progettazioni, in modo che una progettazione possa essere utilizzata per testare più criteri e il nome dei criteri possa essere visualizzato in modo dinamico nella progettazione. Questo mostra al visitatore che sta guardando “articoli più venduti” o “persone che hanno visto questo hanno acquistato questo.” Puoi inoltre utilizzare queste variabili per visualizzare il `dayCount` (numero di giorni di dati utilizzati nel criterio, come “articoli più venduti negli ultimi 2 giorni” ecc.

## Utilizzo dei numeri nei modelli Velocity

Per impostazione predefinita, i modelli Velocity gestiscono tutti gli attributi di entità come valori stringa. Potrebbe essere utile trattare un attributo di entità come un valore numerico per eseguire un&#39;operazione matematica o confrontarlo con un altro valore numerico. Per gestire un attributo di entità come valore numerico, effettuate le seguenti operazioni:

1. Dichiarare una variabile fittizia e inizializzarla in un numero intero o doppio arbitrario
1. Assicuratevi che l&#39;attributo di entità che desiderate utilizzare non sia vuoto (richiesto per l&#39;analisi dei modelli di Target Recommendations per convalidare e salvare il modello)
1. Passate l&#39;attributo di entità nel `parseInt` metodo o `parseDouble` sulla variabile fittizia creata al punto 1 per trasformare la stringa in un numero intero o doppio
1. Eseguire l&#39;operazione o il confronto matematico sul nuovo valore numerico

**Esempio: Calcolo di un prezzo di sconto**

Si supponga di voler ridurre il prezzo visualizzato di un articolo di $ 0,99 per applicare uno sconto. Per ottenere questo risultato, potete usare il seguente approccio:

```
#set( $Double = 0.1 )

#if( $entity1.get('priceBeforeDiscount') != '' )
    #set( $discountedPrice = $Double.parseDouble($entity1.get('priceBeforeDiscount')) - 0.99 )
    Item price: $$discountedPrice
#else
    Item price unavailable
#end
```

**Esempio: Scelta del numero di stelle da visualizzare in base alla valutazione di un elemento**

Si supponga di voler visualizzare un numero appropriato di stelle in base alla media numerica del punteggio cliente di un articolo. Per ottenere questo risultato, potete usare il seguente approccio:

```
#set( $Double = 0.1 )

#if( $entity1.get('rating') != '' )
    #set( $rating = $Double.parseDouble($entity1.get('rating')) )
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

**Esempio: Calcolo del tempo in ore e minuti in base alla lunghezza in minuti di un elemento**

Si supponga di memorizzare la lunghezza di un filmato in minuti, ma si desidera visualizzarla in ore e minuti. Per ottenere questo risultato, potete usare il seguente approccio:

```
#if( $entity1.get('length_minutes') )
#set( $Integer = 1 )
#set( $nbr = $Integer.parseInt($entity1.get('length_minutes')) )
#set( $hrs = $nbr / 60)
#set( $mins = $nbr % 60)
#end
```

## Visualizzazione di un elemento chiave con i prodotti consigliati {#section_7F8D8C0CCCB0403FB9904B32D9E5EDDE}

Puoi modificare la progettazione per mostrare un elemento chiave accanto ad altri prodotti consigliati. Ad esempio, accanto ai consigli potresti voler mostrare l&#39;articolo corrente, come riferimento.

A tale scopo, crea una colonna nella progettazione che utilizzi l’attributo `$key` cui si basa il consiglio, anziché l’attributo `$entity`. Ad esempio, il codice per la colonna chiave potrebbe essere simile a:

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

![](assets/rec_key.png)

Quando si crea un’attività [!DNL Recommendations] e l’elemento chiave viene ricavato dal profilo del visitatore, ad esempio “ultimo articolo acquistato”, [!DNL Target] mostra un prodotto casuale nel [!UICONTROL Compositore esperienza visivo]. Questo perché non è disponibile un profilo mentre progetti l&#39;attività. Tuttavia, quando la pagina verrà visualizzata dai visitatori, ogni visitatore vedrà l&#39;elemento chiave previsto.

## Esecuzione di sostituzioni in un valore stringa {#section_01F8C993C79F42978ED00E39956FA8CA}

È possibile modificare la progettazione per sostituire i valori all&#39;interno di una stringa. Ad esempio, sostituire il delimitatore di punti decimali utilizzato negli Stati Uniti con il delimitatore di virgole utilizzato in Europa e in altri paesi.

Il codice seguente mostra una riga singola in un esempio di prezzo di vendita condizionale:

```
<span class="price">$entity1.value.replace(".", ",") €</span><br>
```

Il codice seguente è un esempio completo di prezzo di vendita:

```
<div class="price"> 
    #if($entity1.hasSalesprice==true) 
    <span class="old">Statt <s>$entity1.salesprice.replace(".", ",") €</s></span><br> 
    <span style="font-size: 10px; float: left;">jetzt nur</span> $entity1.value.replace(".", ",") €<br> #else 
    <span class="price">$entity1.value.replace(".", ",") €</span><br> #end 
    <span style="font-weight:normal; font-size:10px;"> 
                                        $entity1.vatclassDisplay 
                                        <br/> 
                                        $entity1.delivery 
                                        <br> 
                                    </span>
```

## Personalizzazione delle dimensioni del modello e controllo dei valori vuoti {#default}

Utilizzando uno script Velocity per controllare il ridimensionamento dinamico della visualizzazione dell’entità, il seguente modello gestisce un risultato “da 1 a molti” per evitare che vengano creati elementi HTML vuoti qualora non vi siano sufficienti entità restituite da [!DNL Recommendations]. Questo script è adatto per gli scenari in cui non avrebbe senso utilizzare consigli di backup ed è abilitata l’opzione [!UICONTROL Rendering di modelli parziale].

Il seguente snippet HTML sostituisce la porzione HTML esistente nella progettazione predefinita da 4x2 (qui non è stato incluso il CSS per motivi di brevità):

* Se esiste una quinta entità, lo script inserisce un div di chiusura e apre una nuova riga con `<div class="at-table-row">`.
* Per il formato 4x2, il numero massimo di risultati visualizzati sarà otto, ma questo può essere ridotto o aumentato modificando `$count <=8`.
* Tieni presente che la logica non bilancia le entità su più righe. Ad esempio, se devono essere visualizzate cinque o sei entità, queste non verranno disposte in modo dinamico tre in alto e due in basso (o tre in alto e tre in basso). Nella riga superiore verranno inseriti comunque quattro articoli prima di creare una seconda riga.

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
