---
keywords: regole di inclusione;criteri di inclusione;consigli;promozione;promozioni;filtro dinamico;dinamico;corrispondenza attributo profilo
description: Scopri come filtrare dinamicamente in Adobe [!DNL Target] Recommendations confrontando gli articoli (entità) con un valore presente nel profilo dell’utente.
title: Come Si Filtra Per Corrispondenza Attributo Profilo Nelle Attività Recommendations?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: d4b837af-771b-41b4-982b-f9f08e4753f2
source-git-commit: bde5506033fbca1577fad1cda1af203702fc4bb3
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 7%

---

# Corrispondenza attributo profilo

Filtrare dinamicamente in [!DNL Adobe Target] [!DNL Recommendations] confrontando gli articoli (entità) con un valore presente nel profilo dell’utente.

Utilizzo [!UICONTROL Corrispondenza attributo profilo] quando desideri mostrare consigli che corrispondono a un valore memorizzato nel profilo del visitatore, ad esempio dimensioni o marchio preferito.

>[!NOTE]
>
>La [processo di creazione e utilizzo delle regole di inclusione](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) per criteri e promozioni è simile, così come i casi d’uso e gli esempi.

Gli scenari seguenti mostrano come utilizzare [!UICONTROL Corrispondenza attributo profilo]:

* Un&#39;azienda che vende occhiali memorizza il colore di cornice preferito di un visitatore come &quot;noce&quot;. Per quel visitatore specifico, i consigli sono impostati per restituire solo i fotogrammi di occhiali che corrispondono a colore &quot;noce&quot;.
* È possibile definire un parametro di profilo per le dimensioni dell’abbigliamento (ad esempio, Piccolo, Medio o Grande) di un visitatore che naviga sul sito web dell’azienda. È possibile impostare una raccomandazione in modo che corrisponda al parametro di profilo e restituisca prodotti specifici solo per le dimensioni di abbigliamento preferite dall’utente.

## Esempi di corrispondenza degli attributi di profilo {#section_9873E2F22E094E479569D05AD5BB1D40}

[!UICONTROL Corrispondenza attributo profilo] ti consente di consigliare solo gli elementi che corrispondono a un attributo del profilo del visitatore, come negli esempi seguenti.

### Consigli articoli del marchio preferito dell’utente

Ad esempio, puoi utilizzare il [!UICONTROL Corrispondenza attributo profilo] per creare una regola che consigli solo gli articoli il cui marchio è uguale al valore o al testo memorizzato in `profile.favoritebrand`. Con tale regola, se un visitatore cerca dei pantaloncini da corsa di una data marca, i consigli che verranno visualizzati proporranno articoli della marca preferita dell’utente (in base al valore memorizzato in `profile.favoritebrand` nel profilo del visitatore).

![Marchio preferito](/help/main/c-recommendations/c-algorithms/assets/favorite-brand.png)

```
Profile Attribute Matching
brand - equals - the value/text stored in - profile.favoritebrand
```

### Corrispondenza di posti di lavoro a chi cerca lavoro

Supponiamo che tu stia cercando di abbinare i lavori a chi cerca lavoro. Vuoi consigliare solo i posti di lavoro che si trovano nella stessa città di chi cerca lavoro.

Puoi utilizzare le regole di inclusione per far corrispondere la posizione di un cercatore di lavoro dal profilo del visitatore a un elenco di lavori, come nell’esempio seguente:

![Città dell&#39;utente](/help/main/c-recommendations/c-algorithms/assets/city.png)

```
Profile Attribute Matching
jobCity - equals - the value/text stored in - profile.usersCity
```

### Articoli consigliati in base alle dimensioni

Per un esempio visivo di come la corrispondenza degli attributi del profilo influisce sui consigli, considera un sito web che vende ventole elettriche.

Quando un visitatore fa clic su varie immagini dei fan su questo sito web, ogni pagina imposta il valore della `entity.size` a seconda che le dimensioni della ventola nell&#39;immagine siano piccole o grandi.

Supponi di aver creato uno script di profilo per tenere traccia e contare il numero di volte in cui il valore di `entity.size` è impostato su piccolo rispetto a grande.

Se il visitatore ritorna alla home page, visualizzerà i consigli filtrati in base al fatto che sia stato fatto clic su più fan di piccole dimensioni o grandi dimensioni.

Recommendations basato sulla visualizzazione di più piccoli fan sul sito web:

![consigli per piccoli appassionati](/help/main/c-recommendations/c-algorithms/assets/small-fans.png)

Recommendations basato sulla visualizzazione di più grandi fan sul sito web:

![consigli per i grandi fan](/help/main/c-recommendations/c-algorithms/assets/large-fans.png)
