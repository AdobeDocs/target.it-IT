---
keywords: pubblico;selezionare il pubblico;scegliere il pubblico;audience;selettori
description: Definire i visitatori del sito che partecipano all'attività di Adobe [!DNL Target] in base ai criteri di pubblico.
title: Come si seleziona un pubblico in un'attività A/B di [!DNL Target]?
feature: A/B Tests
exl-id: 281ae227-c593-4b71-ad12-865430b332be
TQID: 'https://experienceleague.adobe.com/7W8BrRxk4mKlYlgGb-GSOuc0kRMRWBvSochz9STYrTs'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ab2570eb-4844-49aa-8334-e91a345525e5
    internal-label: A/B Tests
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 4876228feee28031373f7e0abe62a66b05b15274
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 2%
---
# Selezionare il pubblico {#select-audience}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come selezionare, creare, combinare, visualizzare, modificare e copiare il pubblico di un&#39;attività A/B e come impostare la percentuale di visitatori da includere.

>[!ENDSHADEBOX]

Il pubblico determina quali visitatori idonei vengono inseriti nell&#39;attività [!DNL Adobe Target].

Il passaggio **[!UICONTROL Targeting]** del flusso di lavoro guidato in tre parti durante la [creazione di un&#39;attività](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) visualizza un diagramma di flusso che ti guida attraverso i passaggi per assegnare un pubblico e la relativa percentuale di traffico, selezionare il metodo di allocazione del traffico e specificare l&#39;allocazione del traffico per ogni esperienza nell&#39;attività.

![Passaggio Targeting per Test A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new-ui.png)

Per ulteriori informazioni su tutte le opzioni del diagramma di flusso, vedere [Creare un&#39;attività Test A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md).

## Selezionare un pubblico per l’attività

Il pubblico controlla chi vede la tua attività. Solo i visitatori che corrispondono al pubblico possono accedervi e puoi decidere a quale quota di tali visitatori partecipano. Per impostazione predefinita, l’attività esegue il targeting di tutti i visitatori.

1. Fare clic sul controllo **[!UICONTROL Tutti i visitatori]** per selezionare un altro pubblico per l&#39;attività.

   **[!UICONTROL Tutti i visitatori]** è il pubblico predefinito. Per un test A/B senza targeting di pubblico specifico, mantieni il valore predefinito. Se selezioni un altro pubblico, il suo nome viene visualizzato nel controllo più a sinistra.

1. Fai clic sull&#39;icona **[!UICONTROL Sostituisci]** ( ![Sostituisci icona](/help/main/assets/icons/Retweet.svg) ).

   ![](../../assets/audience_activity.png)

1. Nella finestra di dialogo **[!UICONTROL Aggiungi pubblico]**, sfoglia i tipi di pubblico selezionati dalla **[!UICONTROL Libreria tipi di pubblico]** oppure puoi creare un pubblico per sola attività.

   La **[!UICONTROL Libreria tipi di pubblico]** contiene tipi di pubblico definiti in precedenza, inclusi alcuni tipi di pubblico comuni predefiniti come parte di [!DNL Target].

   ![](../../assets/audience_activity_2.png)

1. Fai clic sull&#39;icona **[!UICONTROL Informazioni]** ( ![Icona Informazioni](/help/main/assets/icons/InfoOutline.svg) ) accanto a un pubblico per visualizzare i dettagli su tale pubblico, inclusi l&#39;origine e gli attributi.

   ![](../../assets/audience_activity_3.png)

   Puoi anche fare clic su **[!UICONTROL Visualizza dettagli completi]** per visualizzare ulteriori dettagli sul pubblico.

1. (Facoltativo) Fai clic su **[!UICONTROL Combina tipi di pubblico]** per [creare un pubblico che combini più tipi di pubblico](/help/main/c-target/combining-multiple-audiences.md).

   +++ Passaggi per creare un nuovo pubblico

   Per creare un nuovo pubblico che non sia già presente nella **[!UICONTROL Libreria pubblico]**, fai clic su **[!UICONTROL Crea pubblico]**, definisci il pubblico, quindi fai clic su **[!UICONTROL Fine]**.

   Durante il flusso di lavoro [create-audience](/help/main/c-target/c-audiences/audiences.md), puoi scegliere tra le seguenti opzioni:

   * **[!UICONTROL Libreria tipi di pubblico]**: crea un pubblico on-demand salvato nella **[!UICONTROL Libreria tipi di pubblico]** e riutilizzabile in altre attività.
   * **[!UICONTROL Solo per questa attività]**: crea un [pubblico specifico per l&#39;attività](/help/main/c-target/creating-activity-only-audience.md) che non viene salvato nella **[!UICONTROL Libreria tipi di pubblico]** e che può essere utilizzato solo nell&#39;attività corrente.

   +++

1. Puoi modificare o copiare un pubblico facendo clic sull&#39;icona **[!UICONTROL Altre azioni]** ( ![Altre azioni](/help/main/assets/icons/More.svg) ) accanto al pubblico desiderato.

1. Dopo aver selezionato il pubblico, fai clic su **[!UICONTROL Assegna pubblico]**.

1. Fai clic su **[!UICONTROL Percentuale visitatori]** nel riquadro a destra, quindi specifica la percentuale di visitatori idonei da includere nell&#39;attività.

1. Quando sei soddisfatto del pubblico, fai clic su **[!UICONTROL Avanti]** per passare al terzo passaggio del flusso di lavoro guidato in tre passaggi.

>[!NOTE]
>
>I tipi di pubblico vengono importati automaticamente in background quando si apre l&#39;elenco **[!UICONTROL Tipi di pubblico]** e i tipi di pubblico importati hanno più di 10 minuti.
