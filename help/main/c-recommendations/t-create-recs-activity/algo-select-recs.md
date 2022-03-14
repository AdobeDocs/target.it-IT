---
keywords: consigli;attività consigli;criteri;algoritmo
description: Scopri come selezionare i criteri (regole che determinano quali prodotti o contenuti consigliare) da utilizzare nel tuo Adobe [!DNL Target] Attività Recommendations.
title: Come si selezionano i criteri per un’attività Recommendations?
feature: Recommendations
exl-id: 119227ec-88c3-4de9-b2cf-f7d5fa2e98f6
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 72%

---

# ![PREMIUM](/help/main/assets/premium.png) Selezionare criteri

Seleziona la [criteri](/help/main/c-recommendations/c-algorithms/algorithms.md) per utilizzare [!DNL Adobe Target Recommendations] attività. I criteri sono regole che determinano i prodotti da consigliare in base a un set predeterminato di comportamenti dei visitatori.

Puoi sottoporre reciprocamente a test più tipi di consigli aggiungendo più criteri.

Se selezioni più criteri, il traffico viene suddiviso in modo uniforme tra i criteri selezionati. Ad esempio, se hai selezionato due criteri e l’attività è progettata per mostrare il contenuto predefinito al 20% dei partecipanti all’attività, il 40% dei partecipanti vedrà i consigli controllati da ogni criterio. Non c’è modo di modificare le percentuali per ogni criterio.

* Per cercare un criterio esistente (ad esempio se sono visualizzate più schede di criteri), digita nel campo di ricerca fino a visualizzare il criterio desiderato, quindi selezionalo e fai clic su **[!UICONTROL Fine]**.

   Alcuni criteri sono forniti con [!DNL Recommendations]. Con il tuo team puoi inoltre creare criteri personalizzati.

* Per creare un nuovo criterio, fai clic su **[!UICONTROL Creare criteri]** > **[!UICONTROL Creare criteri]**, quindi compila le informazioni per i nuovi criteri. Per informazioni sulla creazione di un nuovo criterio, consulta [Creare un nuovo criterio](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE).

**Per selezionare i criteri:**

1. Quando [creazione di una nuova raccomandazione](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md#task_6874328773C64C44A73F0A130AD3F96F), nella **[!UICONTROL Seleziona criteri]** individuare e selezionare uno o più criteri.

   ![Finestra di dialogo Seleziona criteri](/help/main/c-recommendations/t-create-recs-activity/assets/filters.png)

   Per filtrare l’elenco dei criteri puoi usare i filtri [!UICONTROL Tipo di settore] e [!UICONTROL Tipo di pagina] nonché la casella di controllo [!UICONTROL Compatibile]. Queste opzioni consentono di individuare facilmente i criteri desiderati.

   * **Tipo di settore:** il tipo di settore è utilizzato per aiutare a categorizzare i criteri di [!DNL Recommendations]. Per modificare il settore verticale predefinito, fai clic su **[!UICONTROL Recommendations]** > **[!UICONTROL Impostazioni]** e seleziona il valore predefinito desiderato **[!UICONTROL Settore verticale]** impostazione.
   * **Tipo di pagina:** il tipo di pagina consente di categorizzare i consigli. Sono inoltre disponibili criteri integrati che è possibile scegliere per ogni tipo di pagina.
   * **Compatibile:** mostra solo i criteri in cui la pagina selezionata trasmette i dati richiesti. Non tutti i criteri vengono eseguiti correttamente su ogni pagina. La pagina o mbox deve passare `entity.id` o `entity.categoryId` per rendere compatibili i consigli per l’elemento o la categoria corrente. In generale, è consigliabile mostrare solo i criteri compatibili. Tuttavia, se desideri che i criteri non compatibili siano disponibili per l’attività, deseleziona la casella di controllo **[!UICONTROL Compatibile]**. Questa opzione può essere disabilitata o abilitata nelle impostazioni: **[!UICONTROL Recommendations]** > **[!UICONTROL Impostazioni]**.

1. Fai clic su **[!UICONTROL Successivo]** per visualizzare la finestra di dialogo [Seleziona design](/help/main/c-recommendations/c-design-overview/design-overview.md).
