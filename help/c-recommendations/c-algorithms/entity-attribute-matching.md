---
keywords: inclusion rules;inclusion criteria;recommendations;promotion;promotions;dynamic filtering;dynamic;entity attribute matching
description: Filtrare in modo dinamico  Adobe Target Recommendations confrontando un insieme di potenziali elementi di raccomandazione con un elemento specifico con cui l'utente ha interagito.
title: Filtra per corrispondenza attributi entità nelle regole di inclusione dinamica in  Adobe Target Recommendations
feature: criteria
translation-type: tm+mt
source-git-commit: 60b71c426b61bb16a23976da9a03926f8e73cf6c
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---


# ![Corrispondenza attributo ](/help/assets/premium.png) PREMIUMEntity

Filtrare in modo dinamico in [!DNL Adobe Target] [!DNL Recommendations] confrontando un insieme di potenziali elementi delle raccomandazioni con un elemento specifico con cui l&#39;utente ha interagito.

>[!NOTE]
>
>Il processo [per la creazione e l&#39;utilizzo di regole di inclusione](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) per criteri e promozioni è simile, così come i casi di utilizzo e gli esempi.

Ad esempio, consigliamo solo gli elementi che corrispondono al marchio dell&#39;elemento corrente, come nell&#39;esempio seguente:

Se la mbox su una pagina di destinazione del marchio restituisce `entity.brand=brandA`, solo i prodotti del marchio A vengono restituiti e visualizzati sulla pagina. Analogamente, nella pagina di destinazione del marchio B, vengono restituiti solo i prodotti del marchio B. Con questo tipo di regola di inclusione dinamica, l&#39;utente deve specificare una sola regola di raccomandazione che restituisca risultati del marchio rilevanti in tutte le pagine del marchio, invece di specificare una raccolta o un filtro statico che corrisponda al nome del marchio.

Notate che dovete distribuire la `entity.brand` nella mbox su quelle pagine di destinazione per consentirne il funzionamento.

## Esempi di corrispondenza attributi entità

[!UICONTROL La ] corrispondenza attributi di entità consente di consigliare solo gli elementi che corrispondono, ad esempio:

* Un attributo dell’elemento che l’utente sta visualizzando
* L’elemento visualizzato più di recente dall’utente
* L’elemento acquistato più di recente dall’utente
* L’elemento visualizzato più frequentemente dall’utente
* Un elemento memorizzato in un attributo personalizzato nel profilo del visitatore

### Raccomanda articoli basati sul marchio

Una volta create le regole dell&#39;attributo di entità, queste filtreranno tutte le raccomandazioni con attributi che non corrispondono al valore di entità passato sulla pagina.

L&#39;esempio seguente mostra le raccomandazioni corrispondenti al marchio di prodotto visualizzato sulla pagina:

Quando visitate una pagina con un prodotto Marchio A, la pagina imposta il valore del parametro `entity.brand` su &quot;BrandA&quot;.

![Esempio di chiamata Target](/help/c-recommendations/c-algorithms/assets/example-target-call.png)

Nelle raccomandazioni sulla pagina, verranno visualizzati solo i prodotti del marchio A.

![Suggerimenti per il marchio A](/help/c-recommendations/c-algorithms/assets/brandA.png)

Se poi visualizzi una pagina di prodotto Brand B, il valore `entity.brand` verrà reimpostato su &quot;BrandB&quot; e vedrai i prodotti Brand B consigliati sulle pagine di prodotto del marchio B.

![Suggerimenti per il marchio B](/help/c-recommendations/c-algorithms/assets/brandB.png)

### Upselling per un prodotto più costoso

Supponiamo di essere un rivenditore di abbigliamento e di voler incoraggiare gli utenti a considerare articoli più costosi e, quindi, più redditizi. È possibile utilizzare gli operatori &quot;uguale&quot; e &quot;è tra&quot; per promuovere elementi più costosi appartenenti alla stessa categoria e allo stesso marchio. Ad esempio, un rivenditore di scarpe può promuovere scarpe da corsa più costose nel tentativo di vendere un visitatore che guarda scarpe da corsa, come nell&#39;esempio seguente:

![Upselling](/help/c-recommendations/c-algorithms/assets/upsell.png)

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

Potete combinare filtri dinamici e statici per promuovere i prodotti con etichette private. Ad esempio, una società di fornitura di uffici può promuovere le cartucce toner del marchio della casa della società per promuovere una vendita più redditizia per un visitatore che guarda il toner — e promuovere penne del marchio della casa della società per guidare una vendita più redditizia per un visitatore che guarda le penne, come nel seguente esempio:

![marchio House](/help/c-recommendations/c-algorithms/assets/housebrand.png)

```
Entity Attribute Matching
category - equals - current item's - category 
And
Static Filter
IsHouseBrand - equals - true
```
