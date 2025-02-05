---
keywords: url attività;url;url diverso
description: Scopri come impostare [!UICONTROL Activity URL] per definire le pagine di test e garantire una progettazione accurata.
title: Qual è l’URL attività in un’attività A/B?
feature: A/B Tests
hide: true
hidefromtoc: true
exl-id: 7f1b8364-790d-4767-bff3-4217ced1a77b
source-git-commit: eb7e892a85fa3952ffc22172085d421756d0dfb5
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 32%

---

# URL attività

L&#39;URL attività determina la pagina utilizzata nel test e che viene aperta quando il test viene progettato utilizzando [!DNL Adobe Target].

Quando viene richiesto durante la creazione dell’attività, specifica l’URL attività. Digitare l&#39;URL completo (incluso `https://`), quindi fare clic su **[!UICONTROL Create]**.

>[!NOTE]
>
>[!DNL Target] non distingue tra protocolli URL ([!DNL https] e [!DNL http]). Di conseguenza, [!DNL `http://www.adobe.com`] e [!DNL `https://www.adobe.com`] corrispondono entrambi.

## Specificare un URL diverso

Per impostazione predefinita, [!UICONTROL Visual Experience Composer] apre la pagina specificata nelle [impostazioni del Compositore esperienza visivo](/help/main/administrating-target/visual-experience-composer-set-up.md). È possibile specificare una pagina diversa durante la creazione dell’attività.

1. (Condizionale) Per visualizzare una pagina diversa dopo l&#39;apertura di [!UICONTROL Visual Experience Composer], nella pagina **[!UICONTROL Experiences]** fare clic su **[!UICONTROL Configure]** nella parte superiore della pagina, quindi selezionare **[!UICONTROL Page Delivery]**.

1. Specificare l&#39;URL nel campo **[!UICONTROL URL]**.

1. (Condizionale) Fare clic su **[!UICONTROL Add Rule]** per aggiungere altre pagine o sezioni all&#39;attività.

   Le regole aggiuntive possono essere basate su uno dei seguenti elementi:

   * URL
   * Dominio
   * Percorso
   * Frammento hash (#)
   * Query
   * Parametro mbox
   * Personalizzato

   È possibile unire ulteriori regole all’URL attività con AND o OR. Tutte le regole aggiunte vengono valutate tra loro con E.

1. Al termine, fare clic su **[!UICONTROL Save]**.

   Se hai inserito un URL per un sito che non include il codice JavaScript di [!DNL Target], non puoi selezionare elementi di pagina.

   Per impostazione predefinita, [!UICONTROL Visual Experience Composer] non consente di modificare gli elementi contenenti JavaScript, ad esempio i banner rotanti. È possibile disattivare **[!UICONTROL Render using JavaScript]** se si desidera modificare tali elementi utilizzando [!UICONTROL Visual Experience Composer].—>

>[!NOTE]
>
>Se modifichi l’URL dopo aver apportato modifiche a una pagina per una o più esperienze, l’esperienza viene reimpostata utilizzando la nuova pagina e le modifiche apportate andranno perse.
