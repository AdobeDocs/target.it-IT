---
description: L'URL attività determina la pagina utilizzata nell'attività Experience Targeting (Targeting esperienza) e che viene aperta in Visual Experience Composer (Compositore esperienza visivo) o in Experience Composer (Compositore esperienza basato su modulo) quando l'attività è stata progettata.
keywords: Targeting
seo-description: L'URL attività determina la pagina utilizzata nell'attività Experience Targeting (Targeting esperienza) e che viene aperta in Adobe Target Visual Experience Composer (VEC) o Experience Composer (Compositore esperienza basato su modulo) quando l'attività è stata progettata.
seo-title: URL attività
solution: Target
title: URL attività
uuid: 970de8ba-ab60-4339-866b-27889bec67f9
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# URL attività{#activity-url}

L&#39;URL attività determina la pagina utilizzata nell&#39;attività Experience Targeting (XT), che viene aperta in Visual Experience Composer (Compositore esperienza visivo) o in Experience Experience Composer (Compositore esperienza basato su modulo) quando l&#39;attività è stata progettata.

1. When prompted while [creating an XT activity](/help/c-activities/t-experience-target/t-xt-create/xt-create.md), specify the activity URL. Digita l’URL completo (comprensivo di `https://`), quindi fai clic su **[!UICONTROL Crea attività]**.

   >[!NOTE]
   >
   >[!DNL Target] non distingue tra protocolli URL ([!DNL https] e [!DNL http]). Di conseguenza, [!DNL `https://www.adobe.com`] e [!DNL `http://www.adobe.com`] sono entrambi validi.
   >
   >By default, the VEC or Form-Based Experience Composer opens the page that is specified in your [Account Preferences](/help/administrating-target/r-target-account-preferences/target-account-preferences.md). È possibile specificare una pagina diversa durante la creazione dell’attività.
   >
   >Se specificate un URL per un sito che non include il codice javascript di Target Standard, non potete selezionare elementi di pagina.

1. (Conditional) To display a different page after the VEC opens, click **[!UICONTROL Configure]**, select **[!UICONTROL Page Delivery]**, and specify the URL in the [!UICONTROL URL] field.

   ![Consegna pagina, finestra di dialogo](/help/c-activities/t-experience-target/t-xt-create/assets/url-config-new.png)

   >[!NOTE]
   >
   >Se modifichi l’URL dopo aver apportato modifiche a una pagina per una o più esperienze, l’esperienza viene reimpostata utilizzando la nuova pagina e le modifiche apportate andranno perse.

1. (Conditional) Click **[!UICONTROL Add Template Rule]** to add more pages or sections to the activity.

   Le regole aggiuntive possono essere basate su uno dei seguenti elementi:

   * URL
   * Dominio
   * Percorso
   * Frammento hash (#)
   * Query
   * Parametro mbox
   È possibile aggiungere altre regole all’URL attività mediante l’operatore E oppure O. Tutte le regole aggiunte vengono valutate tra loro con E.

1. Al termine, fai clic su **[!UICONTROL Salva]**.