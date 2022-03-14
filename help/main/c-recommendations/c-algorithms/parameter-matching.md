---
keywords: regole di inclusione;criteri di inclusione;consigli;promozione;promozioni;filtro dinamico;dinamico;corrispondenza dei parametri
description: Scopri come filtrare dinamicamente in Adobe [!DNL Target] Recommendations confrontando gli articoli (entità) con un valore nella richiesta (API o mbox).
title: Come Si Filtra Per Corrispondenza Parametro Nelle Attività Di Recommendations?
feature: Recommendations
exl-id: 9ec161b9-1b37-4475-b508-af676126c817
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 10%

---

# ![PREMIUM](/help/main/assets/premium.png) Corrispondenza parametro

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

[!UICONTROL Corrispondenza parametro] consente di consigliare contenuti che corrispondono ai parametri della pagina o ai parametri del visitatore, come dimensioni del dispositivo o geolocalizzazione, come nell’esempio seguente:

[!DNL Recommendations] può corrispondere ai valori dei parametri inviati in [!DNL Target] chiama. In questo caso, [!DNL Target] rileva che un visitatore utilizza un dispositivo mobile in base ai parametri di altezza e larghezza dello schermo inviati nel [!DNL Target] chiama e consiglia solo gli elementi che sono dispositivi mobili.

Prendi in considerazione il seguente esempio di chiamata Target:

![Chiamata Target](/help/main/c-recommendations/c-algorithms/assets/example-target-call-2.png)

Sulla pagina che un visitatore sta visualizzando, vedrà i prodotti per dispositivi mobili.

![Prodotti per dispositivi mobili](/help/main/c-recommendations/c-algorithms/assets/phones.png)
