---
keywords: Test multivariati;URL attività
description: Scopri come specificare l'URL attività che determina la pagina utilizzata nel test e che viene visualizzata quando l'attività [!UICONTROL Multivariate Test] è progettata utilizzando  [!DNL Adobe Target].
title: Qual è l'URL attività in un'attività [!UICONTROL Multivariate Test] (MVT)?
feature: Multivariate Tests
exl-id: 336169ae-7c8b-4fd5-9b1c-0bd3e9524425
source-git-commit: 8f9c0ea65197fd639d463628e54db79db993c2da
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 31%

---

# URL attività

L&#39;URL attività determina la pagina utilizzata in [!UICONTROL Multivariate Test] (MVT) e che viene aperta quando il test è progettato in [!DNL Adobe Target].

1. Quando viene richiesto durante la [creazione dell’attività](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md), specifica l’URL attività. Digitare l&#39;URL completo (incluso `https://`), quindi fare clic su **[!UICONTROL Create]**.

   >[!NOTE]
   >
   >[!DNL Target] non distingue tra protocolli URL ([!DNL https] e [!DNL http]). Di conseguenza, [!DNL `https://www.adobe.com`] e [!DNL `http://www.adobe.com`] corrispondono entrambi.

   Per impostazione predefinita, [!UICONTROL Visual Experience Composer] (VEC) apre la pagina specificata nelle [impostazioni del Compositore esperienza visivo](/help/main/administrating-target/visual-experience-composer-set-up.md). È possibile specificare una pagina diversa durante la creazione dell’attività.

1. (Condizionale) Per visualizzare una pagina diversa dopo l’apertura del Compositore esperienza visivo, fai clic sull’icona **[!UICONTROL Configure]**, seleziona **[!UICONTROL Page Delivery]**, quindi specifica l’URL.

1. (Condizionale) Fare clic su **[!UICONTROL Add Rule]** per aggiungere altre pagine o sezioni all&#39;attività.

   Le regole aggiuntive possono essere basate su uno dei seguenti elementi:

   * [!UICONTROL &#x200B; URL]
   * [!UICONTROL Domain]
   * [!UICONTROL Path]
   * [!UICONTROL Hash (#) Fragment]
   * [!UICONTROL Query]
   * [!UICONTROL Custom]

   È possibile unire ulteriori regole all’URL attività con AND o OR. Tutte le regole aggiunte vengono valutate l&#39;una rispetto all&#39;altra mediante l&#39;operatore AND.

   Al termine, fare clic su **[!UICONTROL Save]**.

>[!NOTE]
>
>Se è stato immesso un URL per un sito che non include il codice JavaScript [!DNL Target], non è possibile selezionare elementi di pagina.
>
>Per impostazione predefinita, il Compositore esperienza visivo non consente di modificare gli elementi contenenti JavaScript, ad esempio i banner rotanti. È possibile disattivare **[!UICONTROL Render using JavaScript]** se si desidera modificare tali elementi utilizzando [!UICONTROL Visual Experience Composer].

>[!NOTE]
>
>Se modifichi l’URL dopo aver apportato modifiche a una pagina per una o più esperienze, l’esperienza viene reimpostata utilizzando la nuova pagina e le modifiche apportate andranno perse.
