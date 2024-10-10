---
keywords: url attività;url;url diverso
description: Scopri come impostare [!UICONTROL Activity URL] per definire le pagine di test e garantire una progettazione accurata.
title: Qual è l’URL attività in un’attività A/B?
feature: A/B Tests
hide: true
hidefromtoc: true
source-git-commit: 6e9d18b8347d8ae68be699640c4cde91bdec762c
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 40%

---

# URL attività

L&#39;URL attività determina la pagina utilizzata nel test e che viene aperta quando il test viene progettato utilizzando [!DNL Adobe Target].

Quando viene richiesto durante la creazione dell’attività, specifica l’URL attività. Digitare l&#39;URL completo (incluso `https://`), quindi fare clic su **[!UICONTROL Create]**.

>[!NOTE]
>
>[!DNL Target] non distingue tra protocolli URL ([!DNL https] e [!DNL http]). Di conseguenza, [!DNL `http://www.adobe.com`] e [!DNL `https://www.adobe.com`] corrispondono entrambi.

## Specificare un URL diverso

Per impostazione predefinita, [!UICONTROL Visual Experience Composer] apre la pagina specificata nelle [impostazioni del Compositore esperienza visivo](/help/main/administrating-target/visual-experience-composer-set-up.md). È possibile specificare una pagina diversa durante la creazione dell’attività.

1. Per visualizzare una pagina diversa dopo l&#39;apertura di [!UICONTROL Visual Experience Composer], nella pagina **[!UICONTROL Experiences]** fare clic su **[!UICONTROL Configure]** nella parte superiore della pagina, quindi selezionare **[!UICONTROL Page Delivery]**.

1. Specificare l&#39;URL nel campo **[!UICONTROL URL]**.

1. (Condizionale) Fare clic su **[!UICONTROL Add Rule]** per aggiungere altre pagine o sezioni all&#39;attività.

   Le regole aggiuntive possono essere basate su uno dei seguenti elementi:

   * URL
   * Dominio
   * Percorso
   * Frammento hash (#)
   * Query
   * Parametro mbox

   È possibile unire ulteriori regole all’URL attività con AND o OR. Tutte le regole aggiunte vengono valutate tra loro con E.

1. Al termine, fare clic su **[!UICONTROL Save]**.

<!-- If you entered a URL for a site that does not include the [!DNL Target]s JavaScript code, you cannot select page elements.

By default, the [!UICONTROL Visual Experience Composer] does not allow changes to elements containing JavaScript, such as rotating banners. You can toggle off **[!UICONTROL Render using JavaScript]** if you want to be able to alter those elements using the [!UICONTROL Visual Experience Composer].-->

>[!NOTE]
>
>Se modifichi l’URL dopo aver apportato modifiche a una pagina per una o più esperienze, l’esperienza viene reimpostata utilizzando la nuova pagina e le modifiche apportate andranno perse.