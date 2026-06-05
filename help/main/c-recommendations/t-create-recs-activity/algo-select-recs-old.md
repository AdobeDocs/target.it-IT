---
keywords: consigli;consigli;consigli;criteri;algoritmo;recommendations activity;criteria;algorithm
description: Scopri come selezionare i criteri (regole che determinano quali prodotti o contenuti consigliare) da utilizzare nell'attività di Adobe [!DNL Target] Recommendations.
title: Come Posso Selezionare Criteri per Un’Attività Consigli?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
exl-id: 119227ec-88c3-4de9-b2cf-f7d5fa2e98f6
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 63%

---

# Selezionare criteri

Seleziona i [criteri](/help/main/c-recommendations/c-algorithms/algorithms.md) da utilizzare nell&#39;attività [!DNL Adobe Target Recommendations]. I criteri sono regole che determinano i prodotti da consigliare in base a un set predeterminato di comportamenti dei visitatori.

Puoi sottoporre reciprocamente a test più tipi di consigli aggiungendo più criteri.

Se selezioni più criteri, il traffico viene suddiviso in modo uniforme tra i criteri selezionati. Ad esempio, se hai selezionato due criteri e l’attività è progettata per mostrare il contenuto predefinito al 20% dei partecipanti all’attività, il 40% dei partecipanti vedrà i consigli controllati da ogni criterio. Non c’è modo di modificare le percentuali per ogni criterio.

* Per cercare un criterio esistente (ad esempio se sono visualizzate più schede di criteri), digita nel campo di ricerca fino a visualizzare il criterio desiderato, quindi selezionalo e fai clic su **[!UICONTROL Fine]**.

  Alcuni criteri sono forniti con [!DNL Recommendations]. Con il tuo team puoi inoltre creare criteri personalizzati.

* Per creare un nuovo criterio, fai clic su **[!UICONTROL Crea criterio]** > **[!UICONTROL Crea criterio]**, quindi inserisci le informazioni per il nuovo criterio. Per informazioni sulla creazione di un nuovo criterio, consulta [Creare un nuovo criterio](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE).

**Per selezionare i criteri:**

1. Durante la [creazione di un nuovo consiglio](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md#task_6874328773C64C44A73F0A130AD3F96F), nella finestra di dialogo **[!UICONTROL Seleziona criteri]** individuare e selezionare uno o più criteri.

   ![Finestra di dialogo Seleziona criteri](/help/main/c-recommendations/t-create-recs-activity/assets/filters.png)

   Puoi utilizzare il filtro [!UICONTROL Tipo di settore], il filtro [!UICONTROL Tipo di pagina] e la casella di controllo [!UICONTROL Compatibile] per filtrare l&#39;elenco dei criteri. Queste opzioni consentono di individuare facilmente i criteri desiderati.

   * **Tipo di settore:** il tipo di settore è utilizzato per aiutare a categorizzare i criteri di [!DNL Recommendations]. Per cambiare il settore verticale predefinito, fai clic su **[!UICONTROL Consigli]** > **[!UICONTROL Impostazioni]** e seleziona il **[!UICONTROL Settore verticale]** predefinito desiderato.
   * **Tipo di pagina:** il tipo di pagina consente di categorizzare i consigli. Sono inoltre disponibili criteri incorporati che è possibile scegliere per ogni tipo di pagina.
   * **Compatibile:** mostra solo i criteri in cui la pagina selezionata trasmette i dati richiesti. Non tutti i criteri vengono eseguiti correttamente su ogni pagina. La pagina o mbox deve passare `entity.id` o `entity.categoryId` per rendere compatibili i consigli per l’elemento o la categoria corrente. In generale, è consigliabile mostrare solo i criteri compatibili. Tuttavia, se desideri che i criteri non compatibili siano disponibili per l’attività, deseleziona la casella di controllo **[!UICONTROL Compatibile]**. Questa opzione può essere disabilitata o abilitata nelle impostazioni: **[!UICONTROL Consigli]** > **[!UICONTROL Impostazioni]**.

1. Fai clic su **[!UICONTROL Avanti]** per visualizzare la finestra di dialogo [Seleziona design](/help/main/c-recommendations/c-design-overview/design-overview.md).
