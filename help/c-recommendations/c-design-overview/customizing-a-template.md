---
description: Utilizza il linguaggio di progettazione open-source Velocity per personalizzare le progettazioni dei consigli.
keywords: progettazione personalizzata;velocity;decimale;virgola;personalizzare una progettazione
seo-description: Utilizza il linguaggio di progettazione open-source Velocity per personalizzare le progettazioni dei consigli.
seo-title: Personalizzare una progettazione con Velocity
solution: Target
title: Personalizzare una progettazione con Velocity
title-outputclass: premium
topic: Premium
uuid: 80701a15-c5eb-4089-a92e-117eda11faa2
badge: premium
translation-type: tm+mt
source-git-commit: 74a6f402bc0c9dae6f89cbdb632d7dbc53743593

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
* Trattino (-)
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

>[!NOTE] {class=“- topic/note ”}
>
>Per aggiungere le informazioni dopo il valore della variabile, utilizza la notazione formale. Ad esempio: `${entity1.thumbnailUrl}.gif`.

Puoi inoltre utilizzare `algorithm.name` e `algorithm.dayCount` come variabili nelle progettazioni, in modo che una progettazione possa essere utilizzata per testare più criteri e il nome dei criteri possa essere visualizzato in modo dinamico nella progettazione. Questo mostra al visitatore che sta guardando “articoli più venduti” o “persone che hanno visto questo hanno acquistato questo.” Puoi inoltre utilizzare queste variabili per visualizzare il `dayCount` (numero di giorni di dati utilizzati nel criterio, come “articoli più venduti negli ultimi 2 giorni” ecc.

## Scenario: visualizzare un elemento chiave con i prodotti consigliati {#section_7F8D8C0CCCB0403FB9904B32D9E5EDDE}

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

## Scenario: sostituisci il punto decimale con il delimitatore virgola in un prezzo di vendita  {#section_01F8C993C79F42978ED00E39956FA8CA}

Puoi modificare la progettazione per sostituire il punto, utilizzato come separatore decimale negli Stati Uniti, con la virgola, che invece è utilizzata in Europa e in altri paesi.

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

