---
keywords: url attività;url;url diverso
description: Scopri come specificare l'URL attività che determina la pagina utilizzata nel test e che viene visualizzata quando il test è progettato utilizzando  [!DNL Adobe Target].
title: Qual è l’URL attività in un’attività A/B?
feature: A/B Tests
exl-id: 7482ae10-fb7e-42ba-9ea0-97b82ed85bff
source-git-commit: 6bca763d24649349dbc7cdf6e5f2dbc4ac0a480d
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 44%

---

# URL attività

L’URL attività determina la pagina utilizzata nel test e che viene visualizzata quando il test viene progettato utilizzando Adobe Target.

Quando viene richiesto durante la creazione dell’attività, specifica l’URL attività. Digitare l&#39;URL completo (incluso `https://`), quindi fare clic su **[!UICONTROL Create]**.

>[!NOTE]
>
>[!DNL Target] non distingue tra protocolli URL ([!DNL https] e [!DNL http]). Di conseguenza, [!DNL `http://www.adobe.com`] e [!DNL `https://www.adobe.com`] corrispondono entrambi.

## Specificare un URL diverso

Per impostazione predefinita, [!UICONTROL Visual Experience Composer] apre la pagina specificata nelle [impostazioni del Compositore esperienza visivo](/help/main/administrating-target/visual-experience-composer-set-up.md). È possibile specificare una pagina diversa durante la creazione dell’attività.

1. Per visualizzare una pagina diversa dopo l&#39;apertura di [!UICONTROL Visual Experience Composer], nella pagina **[!UICONTROL Experiences]** fare clic sull&#39;icona ingranaggio **[!UICONTROL Configure]**, quindi selezionare **[!UICONTROL Page Delivery]**.

1. Specificare l&#39;URL nel campo **[!UICONTROL URL]**.

   ![Finestra di dialogo Consegna pagine](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/url-config-new.png)

1. (Condizionale) Fare clic su **[!UICONTROL Add Template Rule]** per aggiungere altre pagine o sezioni all&#39;attività.

   Le regole aggiuntive possono essere basate su uno dei seguenti elementi:

   * URL
   * Dominio
   * Percorso
   * Frammento hash (#)
   * Query
   * Parametro mbox

   È possibile aggiungere altre regole all’URL attività mediante l’operatore E oppure O. Tutte le regole aggiunte vengono valutate tra loro con E.

1. Al termine, fare clic su **[!UICONTROL Save]**.

Se hai inserito un URL per un sito che non include il codice JavaScript di [!DNL Target] Standard, non puoi selezionare elementi di pagina.

Per impostazione predefinita, [!UICONTROL Visual Experience Composer] non consente di modificare gli elementi contenenti JavaScript, ad esempio i banner rotanti. È possibile disattivare **[!UICONTROL Render using JavaScript]** se si desidera modificare tali elementi utilizzando [!UICONTROL Visual Experience Composer].

>[!NOTE]
>
>Se modifichi l’URL dopo aver apportato modifiche a una pagina per una o più esperienze, l’esperienza viene reimpostata utilizzando la nuova pagina e le modifiche apportate andranno perse.
