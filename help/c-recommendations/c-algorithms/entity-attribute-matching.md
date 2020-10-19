---
keywords: inclusion rules;inclusion criteria;recommendations;promotion;promotions;dynamic filtering;dynamic;entity attribute matching
description: Filtrare in modo dinamico  Adobe Target Recommendations confrontando un insieme di potenziali elementi di raccomandazione con un elemento specifico con cui l'utente ha interagito.
title: Filtra per corrispondenza attributi entità nelle regole di inclusione dinamica in  Adobe Target Recommendations
feature: criteria
translation-type: tm+mt
source-git-commit: b51c980d8e7db3ee574350a04f9056fe5b00a703
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 0%

---


# ![Corrispondenza attributo entità PREMIUM](/help/assets/premium.png)

Filter dynamically in [!DNL Adobe Target] [!DNL Recommendations] by comparing a pool of potential recommendations items to a specific item that the user has interacted with.

Ad esempio, consigliamo solo gli elementi che corrispondono al marchio dell&#39;elemento corrente, come nell&#39;esempio seguente:

Se la mbox su una pagina di destinazione del marchio restituisce `entity.brand=Nike`, solo i prodotti Nike vengono restituiti e visualizzati sulla pagina. Analogamente, nella pagina di destinazione del marchio per Adidas, vengono restituiti solo i prodotti Adidas. Con questo tipo di regola di inclusione dinamica, l&#39;utente deve solo specificare una regola di raccomandazione che restituisca i risultati rilevanti del marchio in tutte le pagine del marchio, invece di specificare una raccolta o un filtro statico per corrispondere al nome del marchio.

## Esempi di corrispondenza attributi entità

[!UICONTROL La corrispondenza] attributi entità consente di consigliare solo gli elementi che corrispondono, ad esempio:

* Un attributo dell’elemento che l’utente sta visualizzando
* L’elemento visualizzato più di recente dall’utente
* L’elemento acquistato più di recente dall’utente
* L’elemento visualizzato più frequentemente dall’utente
* Un elemento memorizzato in un attributo personalizzato nel profilo del visitatore

### Upselling per un prodotto più costoso

Supponiamo di essere un rivenditore di abbigliamento e di voler incoraggiare gli utenti a considerare articoli più costosi e, quindi, più redditizi. È possibile utilizzare gli operatori &quot;uguale&quot; e &quot;è tra&quot; per promuovere elementi più costosi appartenenti alla stessa categoria e allo stesso marchio. Ad esempio, un rivenditore di scarpe può promuovere scarpe da ginnastica più costose nel tentativo di vendere un visitatore che guarda scarpe da corsa, come nel seguente esempio di codice:

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

### Promozione di prodotti con etichette private

Potete combinare filtri dinamici e statici per promuovere i prodotti con etichette private. Ad esempio, una società di fornitura di uffici può promuovere le cartucce toner del marchio della casa della società per promuovere una vendita più redditizia per un visitatore che guarda il toner — e promuovere penne del marchio della casa della società per promuovere una vendita più redditizia per un visitatore che guarda le penne, come nel seguente esempio di codice:

```
Entity Attribute Matching
category - equals - current item's - category 
And
Static Filter
IsHouseBrand - equals - true
```
