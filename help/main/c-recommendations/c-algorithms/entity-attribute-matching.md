---
keywords: regole di inclusione;criteri di inclusione;consigli;promozione;promozioni;filtro dinamico;dinamico;corrispondenza attributo entità
description: Scopri come filtrare dinamicamente in [!DNL Target Recommendations] confrontando un pool di elementi potenziali con un elemento specifico con cui l'utente ha interagito.
title: Come posso filtrare per corrispondenza degli attributi di entità nelle attività Consigli?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
exl-id: aadd3132-d590-4dc9-b01b-bedf41bc7441
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---

# Corrispondenza attributo entità

Filtrare dinamicamente in [!DNL Adobe Target Recommendations] confrontando un pool di potenziali elementi di consigli con un elemento specifico con cui l&#39;utente ha interagito.

>[!NOTE]
>
>Il processo [di creazione e utilizzo delle regole di inclusione](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) per criteri e promozioni è simile, così come i casi d&#39;uso e gli esempi.

Ad esempio, per consigliare solo gli articoli con lo stesso marchio dell’articolo corrente, come nell’esempio seguente:

Se la mbox su una pagina di destinazione del marchio restituisce `entity.brand=brandA`, in tale pagina vengono restituiti e visualizzati solo i prodotti del marchio A. Analogamente, nella pagina di destinazione del marchio per il Marchio B vengono restituiti solo i prodotti del Marchio B. Con questo tipo di regola di inclusione dinamica, l’utente deve specificare una sola regola di consigli che restituisca risultati di brand rilevanti in tutte le pagine del brand, anziché specificare una raccolta o un filtro statico che corrisponda a ciascun nome di brand.

Affinché questo processo funzioni, devi consegnare `entity.brand` nella mbox su tali pagine di destinazione.

## Esempi di corrispondenza attributo entità

[!UICONTROL Entity Attribute Matching] consente di consigliare solo gli elementi corrispondenti, ad esempio:

* Attributo dell&#39;elemento attualmente visualizzato dall&#39;utente
* L’ultimo elemento visualizzato dall’utente
* L&#39;ultimo articolo acquistato dall&#39;utente
* L’elemento visualizzato più di frequente dall’utente
* Elemento memorizzato in un attributo personalizzato nel profilo del visitatore

### Articoli consigliati in base al marchio

Una volta create le regole degli attributi di entità, queste filtreranno tutti i consigli con attributi che non corrispondono al valore di entità passato sulla pagina.

L’esempio seguente mostra i consigli che corrispondono al marchio del prodotto mostrato nella pagina:

Quando si visita una pagina che include un prodotto di un marchio A, il valore del parametro `entity.brand` viene impostato su &quot;BrandA&quot;.

![Chiamata Target di esempio](/help/main/c-recommendations/c-algorithms/assets/example-target-call.png)

Nei consigli sulla pagina, vedrai solo i prodotti del marchio A.

![Consigli per il Marchio A](/help/main/c-recommendations/c-algorithms/assets/brandA.png)

Se si visualizza la pagina di un prodotto del Marchio B, il valore `entity.brand` verrà reimpostato su &quot;Marchio B&quot; e verranno visualizzati i prodotti del Marchio B consigliati nelle pagine dei prodotti del Marchio B.

![Consigli per il marchio B](/help/main/c-recommendations/c-algorithms/assets/brandB.png)

### Upselling per un prodotto più costoso

Supponiamo di essere un retailer di abbigliamento e di voler incoraggiare gli utenti a considerare articoli più costosi e, quindi, più redditizi. Puoi utilizzare gli operatori &quot;è uguale a&quot; ed &quot;è tra&quot; per promuovere articoli più costosi della stessa categoria e dello stesso marchio. Ad esempio, un retailer di scarpe può promuovere scarpe da corsa più costose nel tentativo di vendere un visitatore che cerca scarpe da corsa, come nell’esempio seguente:

![Upselling](/help/main/c-recommendations/c-algorithms/assets/upsell-new.png)

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

### Promozione di prodotti con marchio privato

Puoi combinare filtri dinamici e statici per promuovere i prodotti con marchio privato. Ad esempio, un&#39;azienda di forniture per ufficio può promuovere le cartucce di toner del marchio del distributore per promuovere una vendita più redditizia per un visitatore che osserva il toner e promuovere le penne del marchio del distributore per promuovere una vendita più redditizia per un visitatore che osserva le penne, come nel seguente esempio:

![Marchio casa](/help/main/c-recommendations/c-algorithms/assets/housebrand-new.png)
)

```
Entity Attribute Matching
category - equals - current item's - category 
And
Static Filter
IsHouseBrand - equals - true
```
