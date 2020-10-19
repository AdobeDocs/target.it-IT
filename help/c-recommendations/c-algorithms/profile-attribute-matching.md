---
keywords: inclusion rules;inclusion criteria;recommendations;promotion;promotions;dynamic filtering;dynamic;profile attribute matching
description: Filtrare in modo dinamico  Adobe Target Recommendations confrontando elementi (entità) con un valore presente nel profilo dell'utente.
title: Filtrare per corrispondenza attributi profilo nelle regole di inclusione dinamica in  Adobe Target Recommendations
feature: criteria
translation-type: tm+mt
source-git-commit: c814215476ef6e40f4f175fe3f9dbb2c26b966eb
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 5%

---


# ![Corrispondenza attributo profilo PREMIUM](/help/assets/premium.png)

Filtrare in modo dinamico [!DNL Adobe Target] [!DNL Recommendations] confrontando elementi (entità) con un valore nel profilo dell&#39;utente.

Utilizzate la corrispondenza [!UICONTROL attributo] profilo per mostrare le raccomandazioni che corrispondono a un valore memorizzato nel profilo del visitatore, ad esempio dimensione o marchio preferito.

>[!NOTE]
>
>The [process for creating and using inclusion rules](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) for criteria and promotions is similar, as are the use cases and examples.

Gli scenari seguenti mostrano come utilizzare la corrispondenza attributi [!UICONTROL profilo]:

* Una società che vende occhiali memorizza il colore di fotogramma preferito di un visitatore come &quot;noce&quot;. Per quel visitatore specifico, le raccomandazioni sono configurate per restituire solo i fotogrammi della lente di occhio che corrispondono a &quot;noce&quot; nel colore.
* Un parametro di profilo può essere definito per la dimensione dell’abbigliamento (ad esempio, Piccolo, Medio o Grande) di un visitatore che naviga nel sito Web della società. È possibile impostare una raccomandazione in modo che corrisponda al parametro del profilo e restituire prodotti specifici solo per le dimensioni di abbigliamento preferite dall&#39;utente.

## Esempi di corrispondenza attributi profilo {#section_9873E2F22E094E479569D05AD5BB1D40}

[!UICONTROL La corrispondenza] attributi profilo consente di consigliare solo gli elementi che corrispondono a un attributo del profilo del visitatore, come negli esempi seguenti.

### Suggerimento di elementi dal marchio preferito dell&#39;utente

For example, you can use the [!UICONTROL Profile Attribute Matching] option to create a rule that recommends items only where the brand equals the value or text stored in `profile.favoritebrand`. Con tale regola, se un visitatore cerca dei pantaloncini da corsa di una data marca, i consigli che verranno visualizzati proporranno articoli della marca preferita dell’utente (in base al valore memorizzato in `profile.favoritebrand` nel profilo del visitatore).

```
Profile Attribute Matching
brand - equals - the value/text stored in - profile.favoritebrand
```

### Corrispondenza tra posti di lavoro e persone in cerca di lavoro

Supponiamo che tu stia cercando di abbinare i lavori a chi cerca lavoro. Si consiglia solo i lavori che si trovano nella stessa città di chi cerca lavoro.

Potete utilizzare le regole di inclusione per far corrispondere la posizione di un cercatore di lavoro dal profilo del visitatore a un elenco di processi, come nell&#39;esempio seguente:

```
Profile Attribute Matching
jobCity - equals - the value/text stored in - profile.usersCity
```

### Suggerimento di vestiti che corrispondono alle dimensioni di un visitatore

Vediamo un esempio per raccomandare vestiti che corrispondono alla dimensione dell&#39;abbigliamento impostata nel profilo del visitatore.

La pagina del prodotto invia `entity.size` nella chiamata mbox (freccia rossa nell&#39;illustrazione seguente).

Potete creare uno script [di](/help/c-target/c-visitor-profile/profile-parameters.md) profilo per acquisire gli attributi e i valori del profilo del visitatore dall&#39;ultima pagina visitata dal visitatore.

Ad esempio,

```
if ((mbox.name=="target-global-mbox") &&(mbox.param('entity.size') == 'small')) { return 'small';
}

else if ((mbox.name=="target-global-mbox") &&(mbox.param('entity.size') == 'medium')) { return 'medium';
}

else if ((mbox.name=="target-global-mbox") &&(mbox.param('entity.size') == 'large')) { return 'large';
}
```

Lo script di profilo acquisisce il `entity.size` valore dalla mbox denominata `target-global-mbox` e lo restituisce come attributo di profilo denominato `user.size` (freccia blu nell&#39;illustrazione seguente).

![chiamata mbox size](/help/c-recommendations/c-algorithms/assets/size.png)

Quando create i criteri di raccomandazione, fate clic su **[!UICONTROL Aggiungi regola]** di filtro, quindi selezionate Corrispondenza attributi **[!UICONTROL profilo]**.

![Attributo profilo corrispondente a illustrazione](/help/c-recommendations/c-algorithms/assets/profile-attribute-matching.png)

Se il `user.size` profilo è stato caricato in [!DNL Target], viene visualizzato nell&#39;elenco a discesa per la corrispondenza quando si imposta la regola in modo che corrisponda al valore passato nella chiamata mbox (`size`) al nome dello script di profilo (`user.size`).

Potete quindi selezionare &quot;size&quot; &quot;equals&quot; (uguale a) il valore/testo memorizzato in &quot;user.size&quot; per l&#39;attributo di profilo corrispondente.

![Esempio di dimensioni](/help/c-recommendations/c-algorithms/assets/example-size.png)

Una volta create le regole degli attributi di profilo, queste filtreranno tutte le raccomandazioni che hanno attributi che non corrispondono all&#39;attributo di profilo memorizzato del visitatore.

### Raccomanda gli elementi in base alle dimensioni

Per un esempio visivo di come la corrispondenza attributo profilo influisce sulle raccomandazioni, considerate un sito Web che vende ventole elettriche.

Quando un visitatore fa clic su diverse immagini dei fan su questo sito Web, ogni pagina imposta il valore del `entity.size` parametro in base al fatto che le dimensioni della ventola nell’immagine siano piccole o grandi.

Si supponga di aver creato uno script di profilo per tenere traccia e contare il numero di volte in cui il valore di `entity.size` è impostato su piccolo o su grande.

Se il visitatore ritorna quindi alla Home Page, visualizzerà le raccomandazioni filtrate in base al fatto che sia stato fatto clic su un maggior numero di fan piccoli o grandi.

Recommendations basato sulla visualizzazione di più piccole fan sul sito Web:

![raccomandazioni per i piccoli ventilatori](/help/c-recommendations/c-algorithms/assets/small-fans.png)

Recommendations basato sulla visualizzazione di più grandi fan sul sito Web:

![raccomandazioni per i fan di grandi dimensioni](/help/c-recommendations/c-algorithms/assets/large-fans.png)