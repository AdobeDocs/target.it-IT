---
keywords: regole di inclusione;criteri di inclusione;consigli;promozione;promozioni;filtro dinamico;dinamico;corrispondenza dei parametri
description: Scopri come filtrare dinamicamente in Adobe [!DNL Target] Recommendations confrontando elementi (entità) con un valore nella richiesta (API o mbox).
title: Come posso filtrare per corrispondenza dei parametri nelle attività Consigli?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
exl-id: 9ec161b9-1b37-4475-b508-af676126c817
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
source-git-commit: ed3d4b67c78791454c55a2cad4908a37a4d60e26
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 10%
---
# Corrispondenza parametro

Filtra dinamicamente confrontando gli elementi (entità) con un valore nella richiesta (API o mbox).

Ad esempio, per consigliare solo i contenuti che corrispondono al parametro di pagina &quot;settore&quot; o altri parametri, come le dimensioni del dispositivo o la geolocalizzazione, come negli esempi seguenti.

* I parametri mbox per la larghezza e l’altezza dello schermo possono essere utilizzati per rivolgersi ai visitatori mobili e consigliare solo dispositivi mobili e accessori.
* Crea una regola di consigli che restituisca solo i telefoni cellulari più venduti con altezza dello schermo superiore a quella del dispositivo mobile utilizzato dal visitatore per visualizzare la pagina.
* I parametri di geolocalizzazione regionali possono essere utilizzati per restituire consigli per gli strumenti durante l’inverno. I soffiatori di neve e altri strumenti di abbattimento della neve possono essere consigliati per i visitatori nelle aree in cui nevica, ma non consigliati per i visitatori nelle aree in cui non nevica.

>[!NOTE]
>
>Se l’attività è stata creata prima del 31 ottobre 2016, la sua consegna avrà esito negativo se si utilizza il filtro &quot;Corrispondenza parametro&quot;. Per risolvere questo problema:
>
>* Crea una nuova attività e aggiungi i relativi criteri.
>* Utilizza un criterio che non contenga il filtro “Corrispondenza parametro”.
>* Rimuovi il filtro “Corrispondenza parametro” dai criteri.

## Esempi di corrispondenza dei parametri

[!UICONTROL Corrispondenza parametro] consente di consigliare il contenuto che corrisponde ai parametri di pagina o ai parametri del visitatore, ad esempio le dimensioni del dispositivo o la geolocalizzazione, come nell&#39;esempio seguente:

[!DNL Recommendations] può corrispondere ai valori dei parametri inviati nella chiamata [!DNL Target]. In questa istanza, [!DNL Target] rileva che un visitatore sta utilizzando un dispositivo mobile, in base ai parametri di altezza e larghezza dello schermo inviati nella chiamata [!DNL Target], e consiglierà solo gli elementi che sono dispositivi mobili.

Prendi in considerazione la seguente chiamata di Target di esempio:

![Chiamata Target](/help/main/c-recommendations/c-algorithms/assets/example-target-call-2.png)

Nella pagina che un visitatore sta visualizzando, troverà i prodotti dei dispositivi mobili.

![Prodotti per dispositivi mobili](/help/main/c-recommendations/c-algorithms/assets/phones.png)
