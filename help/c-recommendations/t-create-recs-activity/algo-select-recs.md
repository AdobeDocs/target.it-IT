---
description: Seleziona i criteri da utilizzare nell’attività di Consigli.
keywords: consigli;attività di consigli;criteri
seo-description: Seleziona i criteri da utilizzare nell’attività di Consigli.
seo-title: Selezionare criteri
solution: Target
title: Selezionare criteri
title-outputclass: premium
topic: Premium
uuid: 1a1e13e0-7fbd-4f86-80da-cd4e96748d30
badge: premium
translation-type: ht
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# ![PREMIUM](/help/assets/premium.png) Selezionare criteri{#select-criteria}

Seleziona i criteri da utilizzare nell’attività di Consigli.

Puoi sottoporre reciprocamente a test più tipi di consigli aggiungendo più criteri.

Se selezioni più criteri, il traffico viene suddiviso in modo uniforme tra i criteri selezionati. Ad esempio, se hai selezionato due criteri e l’attività è progettata per mostrare il contenuto predefinito al 20% dei partecipanti all’attività, il 40% dei partecipanti vedrà i consigli controllati da ogni criterio. Non c’è modo di modificare le percentuali per ogni criterio.

* Per cercare un criterio esistente (ad esempio se sono visualizzate più schede di criteri), digita nel campo di ricerca fino a visualizzare il criterio desiderato, quindi selezionalo e fai clic su **[!UICONTROL Fine]**.

   Alcuni criteri sono forniti con [!DNL Recommendations]. Con il tuo team puoi inoltre creare criteri personalizzati.

* Per creare un nuovo criterio, fai clic su **[!UICONTROL Crea nuovo]**, quindi inserisci le informazioni per il nuovo criterio. Per informazioni sulla creazione di un nuovo criterio, consulta [Creare un nuovo criterio](../../c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE).

1. [Crea un nuovo consigli](../../c-recommendations/t-create-recs-activity/create-recs-activity.md#task_6874328773C64C44A73F0A130AD3F96F) o trova il consiglio di cui desideri impostare i criteri e fai clic su **[!UICONTROL Modifica]**.
1. Seleziona un tipo di azienda e un tipo di pagina.

* **Tipo di settore:** il tipo di settore è utilizzato per aiutare a categorizzare i criteri di [!DNL Recommendations]. Per cambiare il settore verticale predefinito, fai clic su **[!UICONTROL Impostazioni]** e seleziona il **[!UICONTROL Settore verticale]** predefinito desiderato.
* **Tipo di pagina:** il tipo di pagina consente di categorizzare i consigli. Sono inoltre disponibili criteri integrati che è possibile scegliere per ogni tipo di pagina.
* **Compatibile:** mostra solo i criteri in cui la pagina selezionata trasmette i dati richiesti. Non tutti i criteri vengono eseguiti correttamente su ogni pagina. La pagina o mbox deve passare `entity.id` o [!DNL entity.categoryId] per rendere compatibili i consigli per l’elemento o la categoria corrente. In generale, è consigliabile mostrare solo i criteri compatibili. Tuttavia, se desideri che i criteri non compatibili siano disponibili per l’attività, deseleziona la casella di controllo **[!UICONTROL Compatibile]**. Questa opzione può essere disabilitata o abilitata nelle [!UICONTROL Preferenze] di [!DNL Target].

1. Fai clic su **[!UICONTROL Aggiungi]**.
