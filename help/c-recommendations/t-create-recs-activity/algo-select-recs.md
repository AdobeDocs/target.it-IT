---
description: Seleziona i criteri da utilizzare nell’attività di Consigli.
keywords: consigli;attività di consigli;criteri
seo-description: Selezionate i criteri da utilizzare nell'attività di Adobe Target Recommendations.
seo-title: Selezionare criteri
solution: Target
title: Selezionare criteri
title-outputclass: premium
topic: Premium
uuid: 1a1e13e0-7fbd-4f86-80da-cd4e96748d30
badge: premium
translation-type: tm+mt
source-git-commit: e8e6dcadf307209abcc712798b714af0a5be2e7e

---


# ![PREMIUM](/help/assets/premium.png) Selezionare criteri{#select-criteria}

Select the [criteria](/help/c-recommendations/c-algorithms/algorithms.md) to use in your Recommendations activity. I criteri sono regole che determinano i prodotti da consigliare in base a un set predeterminato di comportamenti dei visitatori.

Puoi sottoporre reciprocamente a test più tipi di consigli aggiungendo più criteri.

Se selezioni più criteri, il traffico viene suddiviso in modo uniforme tra i criteri selezionati. Ad esempio, se hai selezionato due criteri e l’attività è progettata per mostrare il contenuto predefinito al 20% dei partecipanti all’attività, il 40% dei partecipanti vedrà i consigli controllati da ogni criterio. Non c’è modo di modificare le percentuali per ogni criterio.

* Per cercare un criterio esistente (ad esempio se sono visualizzate più schede di criteri), digita nel campo di ricerca fino a visualizzare il criterio desiderato, quindi selezionalo e fai clic su **[!UICONTROL Fine]**.

   Alcuni criteri sono forniti con [!DNL Recommendations]. Con il tuo team puoi inoltre creare criteri personalizzati.

* To create a new criteria, click **[!UICONTROL Create Criteria]**, then fill in the information for the new criteria. Per informazioni sulla creazione di un nuovo criterio, consulta [Creare un nuovo criterio](../../c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE).

**Per selezionare i criteri:**

1. [Quando create una nuova raccomandazione](../../c-recommendations/t-create-recs-activity/create-recs-activity.md#task_6874328773C64C44A73F0A130AD3F96F), nella finestra **[!UICONTROL di]** dialogo Criteri individuate e selezionate uno o più criteri.

   ![Seleziona criteri, finestra di dialogo](/help/c-recommendations/t-create-recs-activity/assets/filters.png)

   You can use the [!UICONTROL Industry Type] filter, [!UICONTROL Page Type] filter, and [!UICONTROL Compatible] checkbox to filter the list of criteria. Queste opzioni consentono di individuare i criteri desiderati.

   * **Tipo di settore:** il tipo di settore è utilizzato per aiutare a categorizzare i criteri di [!DNL Recommendations]. Per cambiare il settore verticale predefinito, fai clic su **[!UICONTROL Impostazioni]** e seleziona il **[!UICONTROL Settore verticale]** predefinito desiderato.
   * **Tipo di pagina:** il tipo di pagina consente di categorizzare i consigli. Sono inoltre disponibili criteri integrati che è possibile scegliere per ogni tipo di pagina.
   * **Compatibile:** mostra solo i criteri in cui la pagina selezionata trasmette i dati richiesti. Non tutti i criteri vengono eseguiti correttamente su ogni pagina. La pagina o mbox deve passare `entity.id` o `entity.categoryId` per rendere compatibili i consigli per l’elemento o la categoria corrente. In generale, è consigliabile mostrare solo i criteri compatibili. Tuttavia, se desideri che i criteri non compatibili siano disponibili per l’attività, deseleziona la casella di controllo **[!UICONTROL Compatibile]**. Questa opzione può essere disabilitata o abilitata nelle [!UICONTROL Preferenze] di [!DNL Target].

1. Click **[!UICONTROL Next]** to display the [Select Design](/help/c-recommendations/c-design-overview/design-overview.md) dialog box.
