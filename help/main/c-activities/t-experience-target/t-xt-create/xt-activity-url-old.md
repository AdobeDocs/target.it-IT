---
keywords: Targeting esperienza;xt;URL attività;url
description: Scopri come specificare [!UICONTROL Activity URL] che determina la pagina utilizzata nel test e che viene visualizzata quando l'attività [!UICONTROL Experience Targeting] è progettata utilizzando  [!DNL Adobe Target].
title: Cos'è [!UICONTROL Activity URL] in un'attività [!UICONTROL Experience Targeting] (XT)?
feature: Experience Targeting
exl-id: 8e3be814-6ad6-4ffa-be8d-68f0cb7857b5
source-git-commit: 3a44c05bea24c622292dd0b774f88f0c93be1d88
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 39%

---

# URL attività nelle attività [!UICONTROL Experience Targeting] (XT)

[!UICONTROL Activity URL] determina la pagina utilizzata in un&#39;attività [!DNL Adobe Target] [!UICONTROL Experience Targeting] (XT). Questa è la pagina che si apre nel [!UICONTROL Visual Experience Composer] (VEC) o [!UICONTROL Form-Based Experience Composer] quando l&#39;attività è progettata.

1. Quando viene richiesto durante la [creazione di un’attività Targeting esperienza](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md), specifica l’URL dell’attività. Digitare l&#39;URL completo (incluso `https://`), quindi fare clic su **[!UICONTROL Create Activity]**.

   >[!NOTE]
   >
   >[!DNL Target] non distingue tra protocolli URL ([!DNL https] e [!DNL http]). Di conseguenza, [!DNL `https://www.adobe.com`] e [!DNL `http://www.adobe.com`] corrispondono entrambi.
   >
   >Per impostazione predefinita, nel Compositore esperienza visivo o nel [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md) viene aperta la pagina specificata nelle [impostazioni del Compositore esperienza visivo](/help/main/administrating-target/visual-experience-composer-set-up.md). È possibile specificare una pagina diversa durante la creazione dell’attività.
   >
   >Se si specifica un URL per un sito che non include una libreria JavaScript di [[!DNL Target] at.js o  [!DNL Adobe Experience Platform Web SDK]](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/overview.html){target=_blank}, non è possibile selezionare elementi di pagina.

1. (Condizionale) Per visualizzare una pagina diversa dopo l’apertura del Compositore esperienza visivo, fai clic su **[!UICONTROL Configure]**, seleziona **[!UICONTROL Page Delivery]**, quindi specifica l’URL nel campo [!UICONTROL URL].

   ![Finestra di dialogo Consegna pagine](/help/main/c-activities/t-experience-target/t-xt-create/assets/url-config-new.png)

   >[!NOTE]
   >
   >Se modifichi l’URL dopo aver apportato modifiche a una pagina per una o più esperienze, l’esperienza viene reimpostata utilizzando la nuova pagina e le modifiche apportate andranno perse.

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
