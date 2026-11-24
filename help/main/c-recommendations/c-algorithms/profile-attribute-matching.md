---
keywords: regole di inclusione;criteri di inclusione;consigli;promozione;promozioni;filtro dinamico;dinamico;corrispondenza attributo profilo
description: Scopri come filtrare dinamicamente in [!DNL Target Recommendations] confrontando gli elementi (entità) con un valore nel profilo dell'utente.
title: Corrispondenza degli attributi di profilo
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
exl-id: d4b837af-771b-41b4-982b-f9f08e4753f2
TQID: 'https://experienceleague.adobe.com/Gm91Mww5ylvNjUcmzp6KwxIG6LTibvI44LnW67KFzqk'
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
source-wordcount: '503'
ht-degree: 5%
---
# Corrispondenza degli attributi di profilo {#profile-attribute-matching}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come filtrare dinamicamente i consigli in [!DNL Adobe Target Recommendations] confrontando gli elementi (entità) con un valore nel profilo del visitatore.

>[!ENDSHADEBOX]

Utilizza **[!UICONTROL Corrispondenza attributo profilo]** per mostrare i consigli che corrispondono a un valore memorizzato nel profilo del visitatore, ad esempio le dimensioni o il marchio preferito. Le regole di inclusione per i criteri e le promozioni possono essere create e utilizzate con processi simili, così come sono simili i rispettivi casi ed esempi di utilizzo. Per ulteriori informazioni, vedere [Utilizzare regole di inclusione dinamiche e statiche](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md).

Gli scenari seguenti mostrano come utilizzare **[!UICONTROL Corrispondenza attributo profilo]**:

* Un&#39;azienda che vende occhiali memorizza il colore di cornice preferito di un visitatore come &quot;noce&quot;. Per quel visitatore, i consigli sono impostati per restituire solo fotogrammi di occhiali che corrispondono a &quot;noce&quot; a colori.
* È possibile definire un parametro di profilo per la dimensione dell’abbigliamento (ad esempio Piccolo, Medium o Grande) di un visitatore che naviga nel sito web dell’azienda. È possibile impostare un consiglio che corrisponda a tale parametro di profilo e che restituisca solo i prodotti con le dimensioni di abbigliamento preferite dal visitatore.

## Esempi di corrispondenza degli attributi di profilo

**[!UICONTROL Corrispondenza attributo profilo]** consiglia solo gli elementi che corrispondono a un attributo del profilo del visitatore, come negli esempi seguenti.

### Articoli consigliati dalla marca preferita dell’utente

L&#39;opzione **[!UICONTROL Corrispondenza attributo profilo]** può creare una regola che consiglia gli elementi solo se il brand è uguale al valore o al testo archiviato in `profile.favoritebrand`. Con tale regola, se un visitatore cerca dei pantaloncini da corsa di una data marca, vengono visualizzati solo i consigli che corrispondono alla marca preferita del visitatore (il valore memorizzato in `profile.favoritebrand` nel profilo del visitatore).

![Marchio preferito](/help/main/c-recommendations/c-algorithms/assets/favorite-brand-new.png)

```
Profile Attribute Matching
brand - equals - the value/text stored in - profile.favoritebrand
```

### Corrispondenza tra processi e persone in cerca di lavoro

Per far corrispondere le mansioni alle persone in cerca di lavoro, si consigliano solo le mansioni che si trovano nella stessa città della persona in cerca di lavoro. Le regole di inclusione possono far corrispondere la posizione di una persona in cerca di lavoro dal profilo del visitatore a un’inserzione di lavoro, come nell’esempio seguente:

![Città utente](/help/main/c-recommendations/c-algorithms/assets/city-new.png)

```
Profile Attribute Matching
jobCity - equals - the value/text stored in - profile.usersCity
```

### Articoli consigliati in base alle dimensioni

L’esempio seguente mostra come la corrispondenza degli attributi del profilo influisce sui consigli di un sito web che vende ventilatori elettrici.

Quando un visitatore fa clic su diverse immagini di ventole su questo sito Web, ogni pagina imposta il valore del parametro `entity.size` in base alle dimensioni della ventola nell&#39;immagine. Uno script di profilo tiene traccia e conta il numero di volte in cui il valore di `entity.size` è impostato su piccolo rispetto a grande.

Se il visitatore ritorna alla home page, i consigli filtrati vengono visualizzati in base al fatto che si sia fatto clic su un numero maggiore di ventole piccole o grandi.

Raccomandazioni basate sulla visualizzazione di più piccole ventole sul sito web:

![consigli per le piccole ventole](/help/main/c-recommendations/c-algorithms/assets/small-fans.png)

Raccomandazioni basate sulla visualizzazione di fan più grandi sul sito web:

![consigli per le ventole grandi](/help/main/c-recommendations/c-algorithms/assets/large-fans.png)
