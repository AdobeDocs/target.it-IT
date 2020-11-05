---
keywords: entity;entity attributes;pass information to Recommendations;behavioral data;data counter;define relative URL;display inventory level;define price;define profit margin;custom attributes
description: Utilizzate gli attributi di entità per trasmettere informazioni su prodotti o contenuti ad  Adobe Target Recommendations.
title: Attributi di entità
feature: entities
uuid: 27672881-a79c-4271-9a61-defddb9a5249
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '1019'
ht-degree: 88%

---


# ![PREMIUM](/help/assets/premium.png) Attributi di entità{#entity-attributes}

Use entity attributes to pass product or content information to [!DNL Adobe Target Recommendations].

[!DNL Recommendations] invia il `productId` o `productPurchasedId` (indicato come `entity.id` nel codice) utilizzato negli algoritmi.

>[!NOTE]
>
>* `entity.id` deve corrispondere alla pagina di conferma `productPurchasedId` inviata all&#39;ordine e `productId` utilizzata nei rapporti  prodotto Adobe Analytics.
   >
   >
* I valori degli attributi di entità specificati scadono dopo 61 giorni. Questo significa che devi assicurarti che il valore più recente di ogni attributo di entità sia passato a Target Recommendations almeno una volta al mese per ogni elemento del catalogo.


La maggior parte dei parametri predefiniti accetta un solo valore, con i nuovi valori che sovrascrivono i vecchi valori. Il parametro `categoryId` può accettare un elenco di valori delimitato da virgole per ogni categoria contenente quel prodotto. I nuovi valori `categoryId` non sovrascrivono quelli esistenti ma vengono aggiunti durante l’aggiornamento dell’entità (limite di 250 caratteri).

In generale, la mbox delle informazioni di visualizzazione potrebbe essere simile all&#39;esempio seguente se utilizzate at.js 1.*x* con `mboxCreate`.

>[!NOTE]
>
>* Se utilizzi at.js 2.*x*, `mboxCreate` (come utilizzato nell&#39;esempio seguente) non è più supportato. Per trasmettere informazioni su prodotti o contenuti ad Recommendations utilizzando at.js 2.*x*, utilizza [targetPageParams](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetpageparams.md). Per un esempio di questo tipo, consulta [Pianificare e implementare Recommendations](/help/c-recommendations/plan-implement.md).

>



Tutti gli attributi dei parametri di entità fanno distinzione tra maiuscole e minuscole.

```
<div class="mboxDefault"></div><script language="JavaScript1.2"> 
 
mboxCreate('productPage', 
 
'entity.id=67833', 
 
'entity.name=GIANTS VS ROCKIES 5/12', 
 
'entity.categoryId=BASEBALL, GIANTS, SF BAY AREA', 
 
'entity.pageUrl=/help/baseball/giants-tix/giantsvrockies5.12.2000-67833', 
 
'entity.venue=AT&T PARK', 
 
'entity.secondary=ROCKIES', 
 
'entity.thumbnailUrl=/help/baseball/giants-tix/giants-136px.gif', 
 
'entity.message=FAMILY SPECIAL', 
 
'entity.value=15.99', 
 
'entity.inventory=1' 
 
); 
 
</script>
```

>[!NOTE]
>
>Per `pageUrl` e `thumbnailUrl` gli URL relativi sono preferiti agli URL assoluti poiché i consigli ricevono i dati inviati da tutti gli ambienti sul sito. L&#39;utilizzo degli URL relativi evita collegamenti fissi a un server di preproduzione o di sviluppo.

Se l&#39;elemento mbox si trova su una pagina di prodotto, puoi includere sia l&#39;ID prodotto che l&#39;ID categoria. L&#39;algoritmo selezionato determina quale verrà visualizzato. L&#39;ID prodotto è utilizzato per gli algoritmi di affinità e l&#39;ID categoria per gli algoritmi di categoria.

## Variabili disponibili

Nell’elenco seguente sono illustrate le variabili disponibili.

### entity.id

Solo valore singolo.

Questo parametro richiesto identifica il prodotto. Questo ID alfanumerico deve essere lo stesso in tutti i prodotti [!DNL Adobe Experience Cloud] utilizzati, tra cui [!DNL Analytics], affinché i vari prodotti riconoscano l’elemento e ne condividano i dati.

I valori `entity.id` non devono contenere barre, simboli commerciali, punti interrogativi, simboli percentuali, virgole o altri caratteri di punteggiatura che richiedono la codifica URL quando vengono trasmessi in una chiamata API REST. Sono consentiti trattini e trattini bassi. L’inclusione di punteggiatura non valida in un valore `entity.id` causerà il mancato funzionamento di alcune funzionalità di [!DNL Recommendations].

Esempio: `'entity.id=67833'`

### entity.name

Solo valore singolo.

Il nome del prodotto visualizzato sul sito Web quando il prodotto viene consigliato.

Esempio: `'entity.name=Giants& vs& Rockies& 5/12'`

### entity.categoryId

Supporta più valori (elenco delimitato da virgole).

Categoria della pagina corrente. Può includere categorie multiple, ad esempio una sottosezione cardigan (ovvero donne, donne:maglie, donne:maglie:cardigan). Più categorie devono essere separate da virgole.

`categoryId` è limitato a 250 caratteri.

>[!NOTE]
>
>Per mostrare un consiglio basato su una categoria in una pagina [!UICONTROL Categoria], un solo `categoryId` può essere trasmesso nell’elemento mbox utilizzato per visualizzare tale consiglio. Il valore di `categoryId` deve corrispondere esattamente al valore di `entity.categoryId` passato nella pagina [!UICONTROL Dettagli prodotto].

Esempi:

* Esempio di pagina Dettagli prodotto: womens, womens:sweaters, womens:sweaters:cardigans
* Esempio di pagina Categoria di Sweaters: womens:sweaters
* Esempio di pagina Categoria di Cardigans: womens:sweaters:cardigans

Per i consigli basati su categorie, viene utilizzata una virgola per separare il valore della categoria. I valori separati da virgole diventano categorie. Puoi inoltre definire le sottocategorie usando un separatore diverso, ad esempio un segno di due punti (:), per separare le sottocategorie nel valore della categoria.

Ad esempio, nel codice seguente la categoria Womens viene divisa in varie sottocategorie:

```
mboxCreate('mboxName', 'entity.id=343942-32', 'entity.categoryId= Womens, Womens:Outerwear, Womens:Outerwear:Jackets, Womens:Outerwear:Jackets:Parka, Womens:Outerwear:Jackets:Caban’, 'entity.thumbnailUrl=...', 'entity.message=...', );
```

Per la distribuzione mbox, viene utilizzato il nome di attributo più lungo per la chiave. Se c&#39;è un pareggio, viene utilizzato l&#39;ultimo attributo. Nell&#39;esempio precedente, il tasto della categoria è Womens:Outerwear:Jackets:Caban.

### entity.brand

Solo valore singolo.

Visualizza il nome del marchio di un elemento.

Esempio: `'entity.brand=brandxyz'`

### entity.pageUrl

Solo valore singolo.

Definisce l&#39;URL relativo della pagina nella quale l&#39;elemento può essere acquistato.

Esempio: `'entity.pageUrl=baseball/giants-tix/giantsvrockies5.12.2000-67833'`

### entity.thumbnailUrl

Solo valore singolo.

Definisce l&#39;URL relativo all&#39;immagine di miniatura visualizzata con l&#39;elemento.

Esempio: `'entity.thumbnailUrl=baseball/giants-tix/giants-136px.gif'`

### entity.message

Solo valore singolo.

Un messaggio relativo al prodotto che viene visualizzato nel consiglio, come ad esempio “in offerta” o “saldo”. Il messaggio è in genere più dettagliato rispetto al nome del prodotto. Da utilizzare per definire informazioni aggiuntive da visualizzare con il prodotto nel modello.

Esempio: `'entity.message=Family&nbsp;special'`

### entity.inventory

Solo valore singolo. Richiede un valore intero o lungo.

Visualizza il livello di inventario dell&#39;elemento.

Esempio: `'entity.inventory=1'`

**Gestione attributi inventario vuoti:** per la consegna, se disponi di una regola di inclusione, una regola di raccolta o un’impostazione dei criteri con `entity.inventory` > 0 o `entity.inventory` = 0 e il prodotto non ha impostato l’inventario, [!DNL Target] restituisce il valore TRUE e include i prodotti in cui l’inventario non è impostato. Questa operazione è stata eseguita per impostazione predefinita, in modo che i prodotti con inventario non vengano visualizzati nei risultati di consigli.

Analogamente, se si dispone di una regola di esclusione globale con `entity.inventory` = 0 e `entity.inventory` non è impostato, [!DNL Target] valuta questa regola in modo che sia TRUE ed esclude il prodotto.

**Problema noto:** la ricerca dei prodotti non è coerente con la distribuzione non impostata per gli attributi dei valori di inventario. Ad esempio, per una regola con `entity.inventory` = 0, la ricerca del prodotto non visualizza i prodotti in cui il valore di inventario non è impostato.

### entity.value

Solo valore singolo.

Definisce il prezzo o il valore dell&#39;elemento.

Esempio: `'entity.value=15.99'`

### entity.margin

Solo valore singolo.

Il margine di profitto o altro valore dell&#39;elemento.

Esempio: `'entity.margin=1.00'`

### entity.*custom*

Supporta più valori (array JSON).

Definisci fino a 100 variabili personalizzate che forniscono informazioni aggiuntive sul prodotto. Puoi specificare qualsiasi nome di attributo non utilizzato per ogni attributo personalizzato. Ad esempio, puoi creare un attributo personalizzato denominato `entity.genre` per definire un libro o un film. In alternativa, un venditore di biglietti potrebbe creare attributi per il luogo di un evento per un artista secondario, ad esempio una squadra in visita in un evento sportivo o un atto di apertura in un concerto.

Limitazioni:

* Non è possibile utilizzare nomi di attributi di entità predefiniti per attributi di entità personalizzati.
* L’attributo entity.environment è riservato dal sistema e non può essere utilizzato per gli attributi di entità personalizzati. I tentativi di passare entity.environment utilizzando targetPageParams, feed o API verranno ignorati.

Esempi:

`'entity.venue=AT&T&nbsp;Park'`

`'entity.secondary=Rockies'`

Gli attributi di entità personalizzati supportano più valori. Consulta [Attributi di entità personalizzata](/help/c-recommendations/c-products/custom-entity-attributes.md#limits) per i limiti di carattere e valore.

Esempio: `'entity.secondary=["band1",&nbsp;"band2"]'`

>[!NOTE]
>
>Gli attributi di entità personalizzati multivalore richiedono array JSON validi. Per informazioni sulla sintassi corretta, consulta Attributi di entità personalizzati.

### entity.event.detailsOnly

Solo valore singolo.

Utilizzato per impedire che una chiamata mbox incrementi i contatori di dati comportamentali per un algoritmo.

Esempio: `'entity.event.detailsOnly=true'`

Negli esempi riportati di seguito, la prima chiamata mbox aggiornerà il catalogo e i dati comportamentali. La seconda chiamata mbox aggiornerà solo il catalogo.

```
mboxCreate('myMbox', 'profile.geo.city = new york', 'profile.geo.state = new york',  'entity.id = 'entity.inventory = 4' )
mboxCreate('myMbox',  'profile.geo.city = new york', 'profile.geo.state = new york',  'entity.id = 123', 'entity.inventory = 4' 'entity.event.detailsOnly=true' )
```

## Argomenti correlati:

* [Attributi di entità personalizzati](/help/c-recommendations/c-products/custom-entity-attributes.md#concept_E5CF39BCAC8140309A73828706288322)
