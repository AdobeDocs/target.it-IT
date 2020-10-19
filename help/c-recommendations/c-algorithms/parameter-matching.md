---
keywords: inclusion rules;inclusion criteria;recommendations;promotion;promotions;dynamic filtering;dynamic;parameter matching
description: Filtrare in modo dinamico  Adobe Target Recommendations confrontando elementi (entità) con un valore nella richiesta (API o mbox).
title: Filtrare per corrispondenza parametri nelle regole di inclusione dinamica in  Adobe Target Recommendations
feature: criteria
translation-type: tm+mt
source-git-commit: b51c980d8e7db3ee574350a04f9056fe5b00a703
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 27%

---


# ![Corrispondenza parametri PREMIUM](/help/assets/premium.png)

Filtrare in modo dinamico confrontando elementi (entità) con un valore nella richiesta (API o mbox).

Ad esempio, si consiglia solo il contenuto che corrisponde al parametro di pagina &quot;industria&quot; o ad altri parametri, come le dimensioni del dispositivo o la geolocalità, come negli esempi seguenti.

* I parametri Mbox per la larghezza e l&#39;altezza dello schermo possono essere utilizzati per i visitatori di dispositivi mobili e consigliamo solo dispositivi mobili e accessori.
* I parametri di geolocalizzazione regionali possono essere utilizzati per restituire raccomandazioni per gli strumenti durante l&#39;inverno. I soffiatori di neve e altri strumenti di riduzione della neve possono essere raccomandati per i visitatori in aree dove nevica ma non consigliato per i visitatori in aree dove non neve.

>[!NOTE]
>
>Se l&#39;attività è stata creata prima del 31 ottobre 2016, la sua distribuzione non riuscirà se utilizza il filtro &quot;Parametro Matching&quot;. Per risolvere questo problema:
>
>* Crea una nuova attività e aggiungi i relativi criteri.
>* Utilizza un criterio che non contenga il filtro “Corrispondenza parametro”.
>* Rimuovi il filtro “Corrispondenza parametro” dai criteri.


Operatori disponibili:

* è uguale a
* è diverso da
* contiene
* non contiene
* inizia con
* termina con
* è maggiore o uguale a
* è minore o uguale a
* è tra