---
keywords: entità;attributi di entità;passare informazioni a Recommendations;dati comportamentali;contatore dati;definire URL relativo;visualizzare livello di inventario;definire prezzo;definire margine di profitto;attributi personalizzati
description: Scopri come utilizzare gli attributi di entità per trasmettere informazioni su prodotti o contenuti a [!DNL Target] Recommendations.
title: Come Si Utilizzano Gli Attributi Di Entità?
feature: Recommendations
exl-id: 4ed5fad3-b8b6-4675-a741-9f85cf73fcf1
source-git-commit: b1e8ea2370fc15f4bfcd960ab2960cafe2db92b8
workflow-type: tm+mt
source-wordcount: '1087'
ht-degree: 52%

---

# ![PREMIUM](/help/main/assets/premium.png) Attributi di entità

Utilizzare gli attributi di entità per trasmettere informazioni su prodotti o contenuti a [!DNL Adobe Target Recommendations].

Le entità si riferiscono agli elementi che desideri consigliare. Le entità possono includere prodotti, contenuti (articoli, presentazioni, immagini, filmati e programmi televisivi), annunci di lavoro, ristoranti e così via.

[!DNL Recommendations] invia `productId` o `productPurchasedId` (di cui `entity.id` nel codice) utilizzato negli algoritmi.

Considera i seguenti aspetti:

* `entity.id` deve corrispondere a `productPurchasedId` inviate alla pagina di conferma dell’ordine e al `productId` utilizzato in [!DNL Adobe Analytics] rapporti sui prodotti.
* Valori degli attributi di entità passati a [!DNL Recommendations] scadono dopo 61 giorni. L’Adobe consiglia di passare il valore più recente di ciascun attributo di entità a [!DNL Recommendations] almeno una volta al mese per ogni articolo del catalogo.

La maggior parte dei parametri predefiniti accetta un solo valore, con i nuovi valori che sovrascrivono i vecchi valori. Il parametro `categoryId` può accettare un elenco di valori delimitato da virgole per ogni categoria contenente quel prodotto. I nuovi valori `categoryId` non sovrascrivono quelli esistenti ma vengono aggiunti durante l’aggiornamento dell’entità (limite di 250 caratteri).

In generale, se utilizzi at.js 1, l’elemento mbox delle informazioni di visualizzazione ha l’aspetto seguente.*x* con `mboxCreate`. Tutti gli attributi dei parametri di entità fanno distinzione tra maiuscole e minuscole.

>[!NOTE]
>
>Se utilizzi at.js 2.*x*, `mboxCreate` (come utilizzato nell&#39;esempio seguente) non è più supportato. Per trasmettere informazioni su prodotti o contenuti a [!DNL Recommendations] utilizzo di at.js 2.*x*, utilizza [targetPageParams](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetpageparams/). Ad esempio, vedi [Pianificare e implementare Recommendations](https://developer.adobe.com/target/implement/recommendations/).

```javascript
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

La `entity.id` i valori devono *not* contengono barre, e commerciali, punti interrogativi, simboli percentuali, virgole o altri caratteri di punteggiatura che richiedono la codifica URL quando vengono trasmessi in una chiamata API REST. Sono consentiti trattini e trattini bassi. L’inclusione di punteggiatura non valida in un valore `entity.id` causerà il mancato funzionamento di alcune funzionalità di [!DNL Recommendations].

Esempio: `'entity.id=67833'`

### entity.name

Solo valore singolo.

Il nome del prodotto visualizzato sul sito Web quando il prodotto viene consigliato.

Esempio: `'entity.name=Giants& vs& Rockies& 5/12'`

### entity.categoryId

Supporta più valori (elenco delimitato da virgole).

Categoria della pagina corrente. entity.categoryID può includere più categorie, ad esempio una sottosezione cardigan (per esempio, donne, donne:maglie, donne):sweaters:cardigans). Le categorie multiple devono essere separate da virgole.

La `categoryId` è limitato a 250 caratteri.

>[!NOTE]
>
>Per mostrare un consiglio basato su una categoria in una pagina [!UICONTROL Categoria], un solo `categoryId` può essere trasmesso nell’elemento mbox utilizzato per visualizzare tale consiglio. Il valore di `categoryId` deve corrispondere esattamente al valore di `entity.categoryId` passato nella pagina [!UICONTROL Dettagli prodotto].

Esempi:

* Esempio di pagina dei dettagli del prodotto: donne, donne:maglioni, donne:sweaters:cardigan
* Esempio di pagina Categoria di Sweaters: womens:sweaters
* Cardiganti pagina di categoria di esempio: donne:sweaters:cardigan

Per i consigli basati su categorie, una virgola separa il valore della categoria. I valori separati da virgole diventano categorie. Puoi inoltre definire le sottocategorie usando un separatore diverso, ad esempio un segno di due punti (:), per separare le sottocategorie nel valore della categoria.

Ad esempio, nel codice seguente la categoria Donne è divisa in diverse sottocategorie:

```javascript
mboxCreate('mboxName', 'entity.id=343942-32', 'entity.categoryId= Womens, Womens:Outerwear, Womens:Outerwear:Jackets, Womens:Outerwear:Jackets:Parka, Womens:Outerwear:Jackets:Caban’, 'entity.thumbnailUrl=...', 'entity.message=...', );
```

Per la distribuzione mbox, viene utilizzato il nome di attributo più lungo per la chiave. Se c&#39;è un pareggio, viene utilizzato l&#39;ultimo attributo. Nell’esempio precedente, la chiave della categoria è Womens:Outerwear:Giacche:Caban.

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

Un messaggio relativo al prodotto che viene visualizzato nel consiglio, come ad esempio “in offerta” o “saldo”. Il messaggio è in genere più dettagliato rispetto al nome del prodotto. Utilizza entity.message per definire informazioni aggiuntive da visualizzare con il prodotto nel modello.

Esempio: `'entity.message=Family&nbsp;special'`

### entity.inventory

Solo valore singolo. Richiede un valore intero o lungo.

Visualizza il livello di inventario dell&#39;elemento.

Esempio: `'entity.inventory=1'`

**Gestione attributi inventario vuoti:** Per la consegna, se disponi di una regola di inclusione, una regola di raccolta o un&#39;impostazione di criteri con `entity.inventory` > 0 o `entity.inventory` = 0 e il prodotto non ha impostato l&#39;inventario, [!DNL Target] valuta questo valore in TRUE e include i prodotti in cui l’inventario non è impostato. Di conseguenza, i prodotti con inventario non impostati vengono visualizzati nei risultati dei consigli.

Analogamente, se si dispone di una regola di esclusione globale con `entity.inventory` = 0 e `entity.inventory` non è impostato, [!DNL Target] valuta questa regola in modo che sia TRUE ed esclude il prodotto.

**Problema noto:** La ricerca dei prodotti non è coerente con la distribuzione degli attributi dei valori di inventario non impostati. Ad esempio, per una regola con `entity.inventory` = 0 , la ricerca del prodotto non visualizza i prodotti in cui il valore di inventario non è impostato.

### entity.value

Solo valore singolo.

Definisce il prezzo o il valore dell&#39;elemento.

Esempio: `'entity.value=15.99'`

entity.value supporta solo il formato decimale (ad esempio, 15.99). Il formato della virgola (15.99) non è supportato.

### entity.margin

Solo valore singolo.

Il margine di profitto o altro valore dell&#39;elemento.

Esempio: `'entity.margin=1.00'`

### entity.*custom*

Supporta più valori (array JSON).

Definisci fino a 100 variabili personalizzate che forniscono informazioni aggiuntive sul prodotto. Puoi specificare qualsiasi nome di attributo non utilizzato per ogni attributo personalizzato. Ad esempio, puoi creare un attributo personalizzato denominato `entity.genre` definire un libro o un film. Un venditore di biglietti può creare attributi per un evento per un artista secondario, ad esempio una squadra ospite in un evento sportivo o un atto di apertura in un concerto.

Limitazioni:

* Non è possibile utilizzare nomi di attributi di entità predefiniti per attributi di entità personalizzati.
* L’attributo entity.environment è riservato dal sistema e non può essere utilizzato per gli attributi di entità personalizzati. I tentativi di passare entity.environment utilizzando targetPageParams, feed o API vengono ignorati.

Esempi:

`'entity.venue=AT&T&nbsp;Park'`

`'entity.secondary=Rockies'`

Gli attributi di entità personalizzati supportano più valori. Consulta [Attributi di entità personalizzata](/help/main/c-recommendations/c-products/custom-entity-attributes.md#limits) per i limiti di carattere e valore.

Esempio: `'entity.secondary=["band1",&nbsp;"band2"]'`

Gli attributi di entità personalizzati multivalore richiedono array JSON validi. Per informazioni sulla sintassi corretta, consulta [Attributi di entità personalizzati](/help/main/c-recommendations/c-products/custom-entity-attributes.md).

### entity.event.detailsOnly

Solo valore singolo.

Utilizzato per impedire che una chiamata mbox incrementi i contatori di dati comportamentali per un algoritmo.

Esempio: `'entity.event.detailsOnly=true'`

Negli esempi seguenti, la prima chiamata mbox aggiorna il catalogo e i dati comportamentali. La seconda chiamata mbox aggiorna solo il catalogo.

```javascript
mboxCreate('myMbox', 'profile.geo.city = new york', 'profile.geo.state = new york',  'entity.id = 'entity.inventory = 4' )
mboxCreate('myMbox',  'profile.geo.city = new york', 'profile.geo.state = new york',  'entity.id = 123', 'entity.inventory = 4' 'entity.event.detailsOnly=true' )
```

>[!MORELIKETHIS]
>
>* [Attributi di entità personalizzati](/help/main/c-recommendations/c-products/custom-entity-attributes.md#concept_E5CF39BCAC8140309A73828706288322)

