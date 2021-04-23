---
keywords: regole di inclusione;criteri di inclusione;consigli;promozione;promozioni;filtro dinamico;dinamico;corrispondenza attributo entità
description: Scopri come filtrare dinamicamente in Adobe [!DNL Target] Recommendations confrontando un pool di articoli potenziali con un articolo specifico con cui l’utente ha interagito.
title: Come Si Filtra Per Corrispondenza Attributo Entità Nelle Attività Recommendations?
feature: Consigli
exl-id: aadd3132-d590-4dc9-b01b-bedf41bc7441
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 0%

---

# ![](/help/assets/premium.png) Corrispondenza attributo PREMIUMEntity

Filtrare dinamicamente in [!DNL Adobe Target] [!DNL Recommendations] confrontando un pool di potenziali articoli consigliati con un articolo specifico con cui l’utente ha interagito.

>[!NOTE]
>
>Il processo [per la creazione e l&#39;utilizzo delle regole di inclusione](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) per i criteri e le promozioni è simile, così come i casi d&#39;uso e gli esempi.

Ad esempio, per consigliare solo gli articoli che corrispondono al marchio dell’articolo corrente, come nell’esempio seguente:

Se la mbox su una pagina di destinazione di un marchio restituisce `entity.brand=brandA`, in tale pagina vengono restituiti e visualizzati solo i prodotti del marchio A. Analogamente, nella pagina di destinazione del marchio B vengono restituiti solo i prodotti del marchio B. Con questo tipo di regola di inclusione dinamica, l’utente deve specificare solo una regola di raccomandazione che restituisce risultati rilevanti del marchio in tutte le pagine del marchio, anziché specificare una raccolta o un filtro statico per far corrispondere ciascun nome del marchio.

Per far sì che questo funzioni, devi consegnare il file `entity.brand` nella mbox nelle pagine di destinazione.

## Esempi di corrispondenza degli attributi di entità

[!UICONTROL La ] corrispondenza attributo entità consente di consigliare solo gli elementi corrispondenti, ad esempio:

* Attributo dell&#39;elemento attualmente visualizzato dall&#39;utente
* L’elemento visualizzato più di recente dall’utente
* L&#39;articolo acquistato più di recente dall&#39;utente
* L’elemento visualizzato più frequentemente dall’utente
* Elemento memorizzato in un attributo personalizzato nel profilo del visitatore

### Articoli consigliati in base al marchio

Una volta create, le regole dell’attributo di entità filtreranno tutti i consigli con attributi che non corrispondono al valore di entità passato nella pagina.

L’esempio seguente mostra i consigli che corrispondono al marchio del prodotto visualizzato nella pagina:

Quando visiti una pagina che presenta un prodotto Marchio A, la pagina imposta il valore del parametro `entity.brand` su &quot;BrandA&quot;.

![Esempio di chiamata Target](/help/c-recommendations/c-algorithms/assets/example-target-call.png)

Nei consigli sulla pagina , vedrai solo i prodotti del marchio A.

![Raccomandazioni per il marchio A](/help/c-recommendations/c-algorithms/assets/brandA.png)

Se poi visualizzi una pagina di prodotto del marchio B, il valore `entity.brand` verrà reimpostato su &quot;BrandB&quot; e vedrai i prodotti del marchio B consigliati nelle pagine di prodotto del marchio B.

![Raccomandazioni per il marchio B](/help/c-recommendations/c-algorithms/assets/brandB.png)

### Upselling a un prodotto più costoso

Supponiamo che tu sia un rivenditore di abbigliamento e desideri incoraggiare gli utenti a considerare articoli più costosi e, quindi, più redditizi. Puoi utilizzare gli operatori &quot;è uguale a&quot; ed &quot;è tra&quot; per promuovere articoli più costosi della stessa categoria e dello stesso marchio. Ad esempio, un rivenditore di scarpe può promuovere scarpe da corsa più costose nel tentativo di vendere un visitatore che cerca scarpe da corsa, come nel seguente esempio:

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

### Promozione dei prodotti con etichetta privata

Puoi combinare filtri dinamici e statici per promuovere i prodotti con etichetta privata. Ad esempio, una società di fornitura di uffici può promuovere cartucce toner del marchio della casa dell&#39;azienda per guidare una vendita più redditizia per un visitatore che guarda il toner — e promuovere penne del marchio della casa dell&#39;azienda per guidare una vendita più redditizia per un visitatore che guarda le penne, come nel seguente esempio:

![Marca casa](/help/c-recommendations/c-algorithms/assets/housebrand.png)

```
Entity Attribute Matching
category - equals - current item's - category 
And
Static Filter
IsHouseBrand - equals - true
```
