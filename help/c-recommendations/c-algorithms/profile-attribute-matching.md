---
keywords: regole di inclusione;criteri di inclusione;consigli;promozione;promozioni;filtro dinamico;dinamico;corrispondenza attributo profilo
description: Scopri come filtrare dinamicamente in Adobe [!DNL Target] Recommendations confrontando gli articoli (entità) con un valore presente nel profilo dell’utente.
title: Come Si Filtra Per Corrispondenza Attributo Profilo Nelle Attività Recommendations?
feature: Consigli
exl-id: d4b837af-771b-41b4-982b-f9f08e4753f2
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 7%

---

# ![](/help/assets/premium.png) Corrispondenza attributo PREMIUMProfile

Filtrare dinamicamente in [!DNL Adobe Target] [!DNL Recommendations] confrontando gli articoli (entità) con un valore presente nel profilo dell’utente.

Utilizza [!UICONTROL Corrispondenza attributo profilo] per mostrare i consigli che corrispondono a un valore memorizzato nel profilo del visitatore, ad esempio dimensione o marchio preferito.

>[!NOTE]
>
>Il processo [per la creazione e l&#39;utilizzo delle regole di inclusione](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) per i criteri e le promozioni è simile, così come i casi d&#39;uso e gli esempi.

Gli scenari seguenti mostrano come utilizzare [!UICONTROL Corrispondenza attributo profilo]:

* Un&#39;azienda che vende occhiali memorizza il colore di cornice preferito di un visitatore come &quot;noce&quot;. Per quel visitatore specifico, i consigli sono impostati per restituire solo i fotogrammi di occhiali che corrispondono a colore &quot;noce&quot;.
* È possibile definire un parametro di profilo per le dimensioni dell’abbigliamento (ad esempio, Piccolo, Medio o Grande) di un visitatore che naviga sul sito web dell’azienda. È possibile impostare una raccomandazione in modo che corrisponda al parametro di profilo e restituisca prodotti specifici solo per le dimensioni di abbigliamento preferite dall’utente.

## Esempi di corrispondenza degli attributi di profilo {#section_9873E2F22E094E479569D05AD5BB1D40}

[!UICONTROL La ] corrispondenza attributo profilo ti consente di consigliare solo gli elementi che corrispondono a un attributo del profilo del visitatore, come negli esempi seguenti.

### Consigli articoli del marchio preferito dell’utente

Ad esempio, puoi utilizzare l&#39;opzione [!UICONTROL Corrispondenza attributo profilo] per creare una regola che consigli solo gli articoli il cui marchio è uguale al valore o al testo memorizzato in `profile.favoritebrand`. Con tale regola, se un visitatore cerca dei pantaloncini da corsa di una data marca, i consigli che verranno visualizzati proporranno articoli della marca preferita dell’utente (in base al valore memorizzato in `profile.favoritebrand` nel profilo del visitatore).

![Marchio preferito](/help/c-recommendations/c-algorithms/assets/favorite-brand.png)

```
Profile Attribute Matching
brand - equals - the value/text stored in - profile.favoritebrand
```

### Corrispondenza di posti di lavoro a chi cerca lavoro

Supponiamo che tu stia cercando di abbinare i lavori a chi cerca lavoro. Vuoi consigliare solo i posti di lavoro che si trovano nella stessa città di chi cerca lavoro.

Puoi utilizzare le regole di inclusione per far corrispondere la posizione di un cercatore di lavoro dal profilo del visitatore a un elenco di lavori, come nell’esempio seguente:

![Città dell&#39;utente](/help/c-recommendations/c-algorithms/assets/city.png)

```
Profile Attribute Matching
jobCity - equals - the value/text stored in - profile.usersCity
```

### Articoli consigliati in base alle dimensioni

Per un esempio visivo di come la corrispondenza degli attributi del profilo influisce sui consigli, considera un sito web che vende ventole elettriche.

Quando un visitatore fa clic su varie immagini dei fan su questo sito web, ogni pagina imposta il valore del parametro `entity.size` in base al fatto che le dimensioni della ventola nell&#39;immagine siano piccole o grandi.

Supponiamo di aver creato uno script di profilo per tenere traccia e contare il numero di volte in cui il valore di `entity.size` è impostato su piccolo rispetto a grande.

Se il visitatore ritorna alla home page, visualizzerà i consigli filtrati in base al fatto che sia stato fatto clic su più fan di piccole dimensioni o grandi dimensioni.

Recommendations basato sulla visualizzazione di più piccoli fan sul sito web:

![consigli per piccoli appassionati](/help/c-recommendations/c-algorithms/assets/small-fans.png)

Recommendations basato sulla visualizzazione di più grandi fan sul sito web:

![consigli per gli appassionati di grandi dimensioni](/help/c-recommendations/c-algorithms/assets/large-fans.png)
