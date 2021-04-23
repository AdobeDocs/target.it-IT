---
keywords: regole di inclusione;criteri di inclusione;consigli;promozione;promozioni;filtro dinamico;dinamico;corrispondenza dei parametri
description: Scopri come filtrare dinamicamente in Adobe [!DNL Target] Recommendations confrontando gli articoli (entità) con un valore nella richiesta (API o mbox).
title: Come Si Filtra Per Corrispondenza Parametro Nelle Attività Di Recommendations?
feature: Consigli
exl-id: 9ec161b9-1b37-4475-b508-af676126c817
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 10%

---

# ![](/help/assets/premium.png) Corrispondenza parametro PREMIUMP

Filtrare dinamicamente confrontando gli articoli (entità) con un valore nella richiesta (API o mbox).

Ad esempio, per consigliare solo i contenuti che corrispondono al parametro di pagina &quot;settore&quot; o ad altri parametri, come le dimensioni del dispositivo o la geolocalizzazione, come negli esempi seguenti.

* I parametri mbox per la larghezza e l’altezza dello schermo possono essere utilizzati per indirizzare i visitatori mobili e consigliare solo dispositivi e accessori mobili.
* Crea una regola di consigli che restituisce solo i telefoni cellulari più venduti che corrispondono o superano l’altezza dello schermo del dispositivo mobile che il visitatore sta utilizzando per visualizzare la pagina.
* I parametri di geolocalizzazione regionali possono essere utilizzati per restituire consigli sugli strumenti durante l’inverno. I soffiatori di neve e altri strumenti di abbattimento della neve possono essere consigliati per i visitatori in aree in cui nevica ma non consigliato per i visitatori in aree in cui non neve.

>[!NOTE]
>
>Se l’attività è stata creata prima del 31 ottobre 2016, la sua consegna avrà esito negativo se si utilizza il filtro &quot;Corrispondenza parametro&quot;. Per risolvere questo problema:
>
>* Crea una nuova attività e aggiungi i relativi criteri.
>* Utilizza un criterio che non contenga il filtro “Corrispondenza parametro”.
>* Rimuovi il filtro “Corrispondenza parametro” dai criteri.


## Esempi di corrispondenza dei parametri

[!UICONTROL La ] corrispondenza dei parametri consente di consigliare il contenuto che corrisponde ai parametri della pagina o ai parametri del visitatore, come le dimensioni del dispositivo o la geolocalizzazione, come nell’esempio seguente:

[!DNL Recommendations] può corrispondere ai valori dei parametri inviati nella  [!DNL Target] chiamata . In questa istanza, [!DNL Target] rileva che un visitatore sta utilizzando un dispositivo mobile, in base ai parametri di altezza e larghezza dello schermo inviati nella chiamata [!DNL Target] e consiglia solo gli elementi che sono dispositivi mobili.

Prendi in considerazione il seguente esempio di chiamata Target:

![Chiamata Target](/help/c-recommendations/c-algorithms/assets/example-target-call-2.png)

Sulla pagina che un visitatore sta visualizzando, vedrà i prodotti per dispositivi mobili.

![Prodotti per dispositivi mobili](/help/c-recommendations/c-algorithms/assets/phones.png)
