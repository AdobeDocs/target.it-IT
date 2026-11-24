---
keywords: regole di inclusione;criteri di inclusione;consigli;promozione;promozioni;filtro dinamico;dinamico;corrispondenza attributo entità
description: Scopri come filtrare dinamicamente in [!DNL Target Recommendations] confrontando un pool di elementi potenziali con un elemento specifico con cui l'utente ha interagito.
title: Corrispondenza degli attributi di entità
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
exl-id: aadd3132-d590-4dc9-b01b-bedf41bc7441
TQID: 'https://experienceleague.adobe.com/2cBSfWXS96u7iumehPd7enxPjQcebkQCdSBSHWOUcJg'
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
source-git-commit: e8a9b6be04169ea3024673babb62085667fe8990
workflow-type: tm+mt
source-wordcount: '505'
ht-degree: 5%
---
# Corrispondenza degli attributi di entità {#entity-attribute-matching}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come filtrare dinamicamente i consigli in [!DNL Adobe Target Recommendations] confrontando un pool di potenziali elementi consigliati con un elemento specifico con cui il visitatore ha interagito.

>[!ENDSHADEBOX]

**[!UICONTROL Corrispondenza attributo entità]** consiglia solo gli elementi che corrispondono a un attributo di un elemento con cui il visitatore ha interagito. Le regole di inclusione per i criteri e le promozioni possono essere create e utilizzate con processi simili, così come sono simili i rispettivi casi ed esempi di utilizzo. Per ulteriori informazioni, vedere [Utilizzare regole di inclusione dinamiche e statiche](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md).

## Esempi di corrispondenza degli attributi di entità

**[!UICONTROL Corrispondenza attributo entità]** può consigliare solo gli elementi corrispondenti, ad esempio:

* Attributo dell’elemento attualmente visualizzato dal visitatore
* L’ultimo elemento visualizzato dal visitatore
* L’ultimo articolo acquistato dal visitatore
* L’elemento visualizzato più di frequente dal visitatore
* Elemento memorizzato in un attributo personalizzato nel profilo del visitatore

### Articoli consigliati in base al marchio

Una volta create le regole degli attributi di entità, queste filtrano tutti i consigli con attributi che non corrispondono al valore di entità trasmesso sulla pagina. Affinché il processo funzioni, il valore `entity.brand` deve essere consegnato nella mbox nelle pagine.

Con questo tipo di regola di inclusione dinamica, è necessario specificare una sola regola di consigli per restituire risultati di brand rilevanti in tutte le pagine del brand, invece di una raccolta o di un filtro statico per ogni nome di brand.

Ad esempio, quando viene visualizzata una pagina che presenta un prodotto di Marchio A, il valore del parametro `entity.brand` viene impostato su &quot;Marchio A&quot;. In una pagina di destinazione del marchio, la mbox restituisce `entity.brand=brandA`.

![Chiamata Target di esempio](/help/main/c-recommendations/c-algorithms/assets/example-target-call.png)

I consigli sulla pagina contengono quindi solo prodotti del marchio A.

![Consigli per il Marchio A](/help/main/c-recommendations/c-algorithms/assets/brandA.png)

Quando viene visualizzata la pagina di un prodotto del marchio B, il valore `entity.brand` viene reimpostato su &quot;BrandB&quot; e si consigliano solo i prodotti del marchio B. Analogamente, nella pagina di destinazione del marchio per il Marchio B vengono restituiti solo i prodotti del Marchio B.

![Consigli per il marchio B](/help/main/c-recommendations/c-algorithms/assets/brandB.png)

### Upselling per un prodotto più costoso

Per incoraggiare i visitatori a considerare gli articoli più costosi e, quindi, più redditizi, gli operatori &quot;è uguale a&quot; ed &quot;è tra&quot; possono promuovere articoli più costosi della stessa categoria e dello stesso marchio. Ad esempio, un retailer di scarpe può promuovere scarpe da corsa più costose per aumentare la vendita di un visitatore che cerca scarpe da corsa, come nell’esempio seguente:

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

È possibile combinare filtri dinamici e statici per promuovere prodotti con marchio privato. Ad esempio, un&#39;azienda di fornitura di ufficio può promuovere le cartucce di toner del marchio della casa dell&#39;azienda per promuovere una vendita più redditizia per un visitatore che sta esaminando il toner e le penne del marchio della casa dell&#39;azienda per un visitatore che sta esaminando le penne, come nel seguente esempio:

![Marchio casa](/help/main/c-recommendations/c-algorithms/assets/housebrand-new.png)

```
Entity Attribute Matching
category - equals - current item's - category 
And
Static Filter
IsHouseBrand - equals - true
```
