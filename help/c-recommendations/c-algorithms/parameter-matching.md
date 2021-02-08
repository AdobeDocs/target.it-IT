---
keywords: regole di inclusione;criteri di inclusione;raccomandazioni;promozione;promozioni;filtro dinamico;corrispondenza parametri
description: Scoprite come filtrare in modo dinamico in  Adobe Target Recommendations confrontando elementi (entità) con un valore presente nella richiesta (API o mbox).
title: In Che Modo È Possibile Filtrare In Base Ai Parametri Corrispondenti Nelle Attività Recommendations?
feature: Recommendations
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 10%

---


# ![Corrispondenza ](/help/assets/premium.png) PREMIUMParameter

Filtrare in modo dinamico confrontando elementi (entità) con un valore nella richiesta (API o mbox).

Ad esempio, si consiglia solo il contenuto che corrisponde al parametro di pagina &quot;industria&quot; o ad altri parametri, come le dimensioni del dispositivo o la geolocalità, come negli esempi seguenti.

* I parametri Mbox per la larghezza e l&#39;altezza dello schermo possono essere utilizzati per i visitatori di dispositivi mobili e consigliamo solo dispositivi mobili e accessori.
* Create una regola di Recommendations che restituisce solo i telefoni cellulari più venduti che corrispondono o superano l&#39;altezza dello schermo del dispositivo mobile su cui il visitatore utilizza la visualizzazione della pagina.
* I parametri di geolocalizzazione regionali possono essere utilizzati per restituire raccomandazioni per gli strumenti durante l&#39;inverno. I soffiatori di neve e altri strumenti di riduzione della neve possono essere raccomandati per i visitatori in aree dove nevica ma non consigliato per i visitatori in aree dove non neve.

>[!NOTE]
>
>Se l&#39;attività è stata creata prima del 31 ottobre 2016, la sua distribuzione non riuscirà se utilizza il filtro &quot;Parametro Matching&quot;. Per risolvere questo problema:
>
>* Crea una nuova attività e aggiungi i relativi criteri.
>* Utilizza un criterio che non contenga il filtro “Corrispondenza parametro”.
>* Rimuovi il filtro “Corrispondenza parametro” dai criteri.


## Esempi di corrispondenza dei parametri

[!UICONTROL La ] corrispondenza dei parametri consente di consigliare il contenuto che corrisponde ai parametri di pagina o ai parametri del visitatore, come le dimensioni del dispositivo o la geolocalità, come nell&#39;esempio seguente:

[!DNL Recommendations] può corrispondere ai valori dei parametri inviati nella  [!DNL Target] chiamata. In questa istanza, [!DNL Target] rileva che un visitatore utilizza un dispositivo mobile, in base ai parametri di altezza e larghezza dello schermo inviati nella chiamata [!DNL Target], e consiglia solo gli elementi che sono dispositivi mobili.

Prendete in considerazione l&#39;esempio seguente di chiamata Target:

![Chiamata Target](/help/c-recommendations/c-algorithms/assets/example-target-call-2.png)

Sulla pagina visualizzata da un visitatore, verranno visualizzati i prodotti per dispositivi mobili.

![Prodotti per dispositivi mobili](/help/c-recommendations/c-algorithms/assets/phones.png)
