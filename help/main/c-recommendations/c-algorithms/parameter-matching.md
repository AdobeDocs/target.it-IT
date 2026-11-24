---
keywords: regole di inclusione;criteri di inclusione;consigli;promozione;promozioni;filtro dinamico;dinamico;corrispondenza dei parametri
description: Scopri come filtrare dinamicamente in Adobe [!DNL Target] Recommendations confrontando elementi (entità) con un valore nella richiesta (API o mbox).
title: Corrispondenza dei parametri
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
exl-id: 9ec161b9-1b37-4475-b508-af676126c817
TQID: 'https://experienceleague.adobe.com/GTli-O1p4Gm2Fg9J-L0ukQ8dSw2t-da8OatFLP8Ks9g'
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
source-wordcount: '311'
ht-degree: 8%
---
# Corrispondenza dei parametri {#parameter-matching}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come filtrare dinamicamente i consigli in [!DNL Adobe Target Recommendations] confrontando elementi (entità) con un valore nella richiesta (API o mbox).

>[!ENDSHADEBOX]

**[!UICONTROL Corrispondenza parametro]** consiglia solo il contenuto che corrisponde ai parametri di pagina o ai parametri del visitatore, ad esempio le dimensioni del dispositivo o la geolocalizzazione. Ad esempio, è possibile consigliare solo i contenuti che corrispondono al parametro di pagina &quot;settore&quot;. Le regole di inclusione per i criteri e le promozioni possono essere create e utilizzate con processi simili, così come sono simili i rispettivi casi ed esempi di utilizzo. Per ulteriori informazioni, vedere [Utilizzare regole di inclusione dinamiche e statiche](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md).

Altri esempi includono:

* I parametri mbox per la larghezza e l’altezza dello schermo possono essere utilizzati per rivolgersi ai visitatori mobili e consigliare solo dispositivi mobili e accessori.
* Una regola di consigli può restituire solo i telefoni cellulari più venduti con un&#39;altezza dello schermo pari o superiore a quella del dispositivo mobile utilizzato dal visitatore per visualizzare la pagina.
* I parametri di geolocalizzazione regionali possono essere utilizzati per restituire consigli per gli strumenti durante l’inverno. I soffiatori di neve e altri strumenti di abbattimento della neve possono essere consigliati ai visitatori nelle aree in cui nevica, ma non ai visitatori nelle aree in cui non nevica.

## Esempi di corrispondenza dei parametri

[!DNL Recommendations] può corrispondere ai valori dei parametri inviati nella chiamata [!DNL Target]. Nell&#39;esempio seguente, [!DNL Target] rileva che un visitatore sta utilizzando un dispositivo mobile, in base ai parametri di altezza e larghezza dello schermo inviati nella chiamata [!DNL Target], e consiglia solo gli elementi che sono dispositivi mobili.

Considera la seguente chiamata di esempio [!DNL Target]:

![Chiamata Target](/help/main/c-recommendations/c-algorithms/assets/example-target-call-2.png)

Nella pagina visualizzata da un visitatore vengono visualizzati i prodotti per dispositivi mobili.

![Prodotti per dispositivi mobili](/help/main/c-recommendations/c-algorithms/assets/phones.png)
