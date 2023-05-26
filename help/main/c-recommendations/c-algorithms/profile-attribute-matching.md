---
keywords: regole di inclusione;criteri di inclusione;consigli;promozione;promozioni;filtro dinamico;dinamico;corrispondenza attributo profilo
description: Scopri come filtrare dinamicamente in Adobe [!DNL Target] Recommendations confrontando gli articoli (entità) con un valore nel profilo dell’utente.
title: Come posso filtrare per corrispondenza degli attributi di profilo nelle attività di Recommendations?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: d4b837af-771b-41b4-982b-f9f08e4753f2
source-git-commit: bde5506033fbca1577fad1cda1af203702fc4bb3
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 7%

---

# Corrispondenza attributo profilo

Filtrare dinamicamente in [!DNL Adobe Target] [!DNL Recommendations] confrontando gli articoli (entità) con un valore nel profilo dell’utente.

Utilizzare [!UICONTROL Corrispondenza attributo profilo] quando desideri mostrare consigli che corrispondono a un valore memorizzato nel profilo del visitatore, ad esempio dimensioni o marchio preferito.

>[!NOTE]
>
>Il [processo per la creazione e l’utilizzo delle regole di inclusione](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) per criteri e promozioni è simile, così come i casi d’uso e gli esempi.

Gli scenari seguenti mostrano come utilizzare [!UICONTROL Corrispondenza attributo profilo]:

* Un&#39;azienda che vende occhiali memorizza il colore preferito del frame del visitatore come &quot;noce&quot;. Per quel visitatore specifico, i consigli sono impostati per restituire solo cornici di occhiali che corrispondono a &quot;noce&quot; a colori.
* Un parametro di profilo può essere definito per la dimensione dell’abbigliamento (ad esempio, Piccolo, Medio o Grande) di un visitatore durante la navigazione nel sito web della tua azienda. È possibile impostare un consiglio che corrisponda a tale parametro di profilo e che restituisca prodotti specifici solo in base alla dimensione di abbigliamento preferita dall’utente.

## Esempi di corrispondenza degli attributi del profilo {#section_9873E2F22E094E479569D05AD5BB1D40}

[!UICONTROL Corrispondenza attributo profilo] ti consente di consigliare solo gli elementi che corrispondono a un attributo del profilo del visitatore, come negli esempi seguenti.

### Articoli consigliati dalla marca preferita dell’utente

Ad esempio, puoi utilizzare [!UICONTROL Corrispondenza attributo profilo] opzione per creare una regola che consigli solo gli articoli il cui marchio è uguale al valore o al testo memorizzato in `profile.favoritebrand`. Con tale regola, se un visitatore cerca dei pantaloncini da corsa di una data marca, i consigli che verranno visualizzati proporranno articoli della marca preferita dell’utente (in base al valore memorizzato in `profile.favoritebrand` nel profilo del visitatore).

![Marchio preferito](/help/main/c-recommendations/c-algorithms/assets/favorite-brand.png)

```
Profile Attribute Matching
brand - equals - the value/text stored in - profile.favoritebrand
```

### Corrispondenza tra processi e persone in cerca di lavoro

Supponiamo che tu stia cercando di mettere in pari i lavori con le persone in cerca di lavoro. Vuoi consigliare solo i lavori che si trovano nella stessa città della persona in cerca di lavoro.

È possibile utilizzare le regole di inclusione per far corrispondere la posizione di una persona in cerca di lavoro dal suo profilo visitatore a un’inserzione di lavoro, come nell’esempio seguente:

![Città dell&#39;utente](/help/main/c-recommendations/c-algorithms/assets/city.png)

```
Profile Attribute Matching
jobCity - equals - the value/text stored in - profile.usersCity
```

### Articoli consigliati in base alle dimensioni

Per un esempio visivo del modo in cui la corrispondenza degli attributi di profilo influisce sui consigli, considera un sito web che vende ventilatori elettrici.

Quando un visitatore fa clic su diverse immagini di ventole su questo sito web, ogni pagina imposta il valore di `entity.size` a seconda che le dimensioni della ventola nell&#39;immagine siano piccole o grandi.

Supponiamo di aver creato uno script di profilo per tenere traccia e contare il numero di volte in cui il valore di `entity.size` è impostato su piccolo rispetto a grande.

Se il visitatore ritorna alla home page, vedrà i consigli filtrati in base al fatto che si sia fatto clic su un numero maggiore di fan piccoli o grandi.

Recommendations basato sulla visualizzazione di più piccole ventole sul sito web:

![consigli per le piccole ventole](/help/main/c-recommendations/c-algorithms/assets/small-fans.png)

Recommendations basato sulla visualizzazione di più grandi fan sul sito web:

![consigli per le ventole grandi](/help/main/c-recommendations/c-algorithms/assets/large-fans.png)
