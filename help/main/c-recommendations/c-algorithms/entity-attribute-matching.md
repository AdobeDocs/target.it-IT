---
keywords: regole di inclusione;criteri di inclusione;consigli;promozione;promozioni;filtro dinamico;dinamico;corrispondenza attributo entità
description: Scopri come filtrare dinamicamente in Adobe [!DNL Target] Recommendations confrontando un pool di elementi potenziali con un elemento specifico con cui l’utente ha interagito.
title: Come posso filtrare in base alla corrispondenza degli attributi di entità nelle attività Recommendations?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: aadd3132-d590-4dc9-b01b-bedf41bc7441
source-git-commit: bde5506033fbca1577fad1cda1af203702fc4bb3
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 0%

---

# Corrispondenza attributo entità

Filtrare dinamicamente in [!DNL Adobe Target] [!DNL Recommendations] confrontando un pool di potenziali elementi di consigli con un elemento specifico con cui l’utente ha interagito.

>[!NOTE]
>
>Il [processo per la creazione e l’utilizzo delle regole di inclusione](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) per criteri e promozioni è simile, così come i casi d’uso e gli esempi.

Ad esempio, per consigliare solo gli articoli con lo stesso marchio dell’articolo corrente, come nell’esempio seguente:

Se la mbox su una pagina di destinazione del marchio restituisce `entity.brand=brandA`, quindi sulla pagina vengono restituiti e visualizzati solo i prodotti del Marchio A. Analogamente, nella pagina di destinazione del marchio per il Marchio B vengono restituiti solo i prodotti del Marchio B. Con questo tipo di regola di inclusione dinamica, l’utente deve specificare una sola regola di consigli che restituisca risultati di marchio rilevanti in tutte le pagine del marchio, invece di specificare una raccolta o un filtro statico che corrisponda a ciascun nome di marchio.

Tieni presente che devi fornire `entity.brand` nella mbox sulle pagine di destinazione affinché questo funzioni.

## Esempi di corrispondenza attributo entità

[!UICONTROL Corrispondenza attributo entità] ti consente di consigliare solo gli elementi corrispondenti, ad esempio:

* Attributo dell&#39;elemento attualmente visualizzato dall&#39;utente
* L’ultimo elemento visualizzato dall’utente
* L&#39;ultimo articolo acquistato dall&#39;utente
* L’elemento visualizzato più di frequente dall’utente
* Elemento memorizzato in un attributo personalizzato nel profilo del visitatore

### Articoli consigliati in base al marchio

Una volta create le regole degli attributi di entità, queste filtreranno tutti i consigli con attributi che non corrispondono al valore di entità passato sulla pagina.

L’esempio seguente mostra i consigli che corrispondono al marchio del prodotto mostrato nella pagina:

Quando visiti una pagina che presenta un prodotto di Marchio A, la pagina imposta il valore di `entity.brand` a &quot;BrandA&quot;.

![Esempio di chiamata Target](/help/main/c-recommendations/c-algorithms/assets/example-target-call.png)

Nei consigli sulla pagina, vedrai solo i prodotti del marchio A.

![Raccomandazioni per il marchio A](/help/main/c-recommendations/c-algorithms/assets/brandA.png)

Se poi visualizzi la pagina di un prodotto del Marchio B, il `entity.brand` Il valore verrà reimpostato su &quot;BrandB&quot; e nelle pagine dei prodotti del Brand B verranno visualizzati i prodotti consigliati.

![Raccomandazioni per il marchio B](/help/main/c-recommendations/c-algorithms/assets/brandB.png)

### Upselling per un prodotto più costoso

Supponiamo di essere un rivenditore di abbigliamento e di voler incoraggiare gli utenti a considerare articoli più costosi e, quindi, più redditizi. Puoi utilizzare gli operatori &quot;è uguale a&quot; ed &quot;è tra&quot; per promuovere articoli più costosi della stessa categoria e dello stesso marchio. Ad esempio, un rivenditore di calzature può promuovere scarpe da corsa più costose nel tentativo di vendere un visitatore che cerca scarpe da corsa, come nell’esempio seguente:

![Upselling](/help/main/c-recommendations/c-algorithms/assets/upsell.png)

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

![Marchio della casa](/help/main/c-recommendations/c-algorithms/assets/housebrand.png)

```
Entity Attribute Matching
category - equals - current item's - category 
And
Static Filter
IsHouseBrand - equals - true
```
