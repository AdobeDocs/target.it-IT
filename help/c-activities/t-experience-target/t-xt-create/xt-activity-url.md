---
keywords: Targeting
description: L’URL attività determina la pagina utilizzata nell’attività Targeting esperienza e che viene aperta nel Compositore esperienza visivo o Compositore esperienza basato su moduli di Adobe Target quando l’attività viene progettata.
title: URL attività
uuid: 970de8ba-ab60-4339-866b-27889bec67f9
translation-type: tm+mt
source-git-commit: fdf75402a0283c3189952fb74997d4ab536d5098
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 92%

---


# URL attività{#activity-url}

L’URL attività determina la pagina utilizzata nell’attività Targeting esperienza e che viene aperta nel Compositore esperienza visivo o Compositore esperienza basato su moduli quando l’attività viene progettata.

1. Quando viene richiesto durante la [creazione di un’attività Targeting esperienza](/help/c-activities/t-experience-target/t-xt-create/xt-create.md), specifica l’URL dell’attività. Digita l’URL completo (comprensivo di `https://`), quindi fai clic su **[!UICONTROL Crea attività]**.

   >[!NOTE]
   >
   >[!DNL Target] non distingue tra protocolli URL ([!DNL https] e [!DNL http]). Di conseguenza, [!DNL `https://www.adobe.com`] e [!DNL `http://www.adobe.com`] sono entrambi validi.
   >
   >By default, the VEC or Form-Based Experience Composer opens the page that is specified in your [Visual Experience Composer settings](/help/administrating-target/visual-experience-composer-set-up.md). È possibile specificare una pagina diversa durante la creazione dell’attività.
   >
   >Se hai specificato un URL per un sito che non include il codice JavaScript di Target Standard, non puoi selezionare elementi di pagina.

1. (Condizionale) Per visualizzare una pagina diversa dopo l’apertura del Compositore esperienza visivo, fai clic su **[!UICONTROL Configura]**, seleziona **[!UICONTROL Consegna pagine]** e specifica l’URL nel campo [!UICONTROL URL].

   ![Finestra di dialogo Consegna pagine](/help/c-activities/t-experience-target/t-xt-create/assets/url-config-new.png)

   >[!NOTE]
   >
   >Se modifichi l’URL dopo aver apportato modifiche a una pagina per una o più esperienze, l’esperienza viene reimpostata utilizzando la nuova pagina e le modifiche apportate andranno perse.

1. (Condizionale) Fai clic su **[!UICONTROL Aggiungi regola modello]** per aggiungere più pagine o sezioni all’attività.

   Le regole aggiuntive possono essere basate su uno dei seguenti elementi:

   * URL
   * Dominio
   * Percorso
   * Frammento hash (#)
   * Query
   * Parametro mbox
   È possibile aggiungere altre regole all’URL attività mediante l’operatore E oppure O. Tutte le regole aggiunte vengono valutate tra loro con E.

1. Al termine, fai clic su **[!UICONTROL Salva]**.