---
keywords: pubblico;selezionare il pubblico;scegliere il pubblico;audience;selettori
description: Definisci i visitatori del sito che partecipano all'attività dell'Adobe [!DNL Target]  in base ai criteri di pubblico.
title: Come si seleziona un pubblico in un'attività  [!DNL Target] A/B?
feature: A/B Tests
hide: true
hidefromtoc: true
source-git-commit: cc823f84fb93cbe2e55d394d0f6f4fe48bbd5293
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 12%

---

# Selezionare il pubblico

Il pubblico determina quali visitatori idonei vengono inseriti nell&#39;attività [!DNL Adobe Target].

Il passaggio [!UICONTROL Targeting] del flusso di lavoro guidato in tre parti durante la [creazione di un&#39;attività](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab-beta.md) visualizza un diagramma di flusso che ti guida attraverso i passaggi per assegnare un pubblico e la relativa percentuale di traffico, selezionare il metodo di allocazione del traffico e specificare l&#39;allocazione del traffico per ogni esperienza nell&#39;attività.

![Passaggio Targeting per Test A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new-ui.png)

Per ulteriori informazioni su tutte le opzioni del diagramma di flusso, vedere [Creare un&#39;attività Test A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab-beta.md).

## Selezionare un pubblico per l’attività

1. Fare clic sul controllo **[!UICONTROL All Visitors]** per selezionare un altro pubblico per l&#39;attività.

   Il pubblico [!UICONTROL All Visitors] è impostato come predefinito. Se selezioni un altro pubblico, il suo nome viene visualizzato nel controllo più a sinistra.

   Per un test A/B senza targeting di pubblico specifico, scegli il valore predefinito, [!UICONTROL All Visitors].

   Viene visualizzato il frame a destra, che consente di aggiungere o eliminare un pubblico e di assegnare la percentuale di visitatori per l’attività.

1. Per cambiare il pubblico, fai clic sull&#39;icona **[!UICONTROL Replace]** ( ![Icona Sostituisci](/help/main/assets/icons/Retweet.svg) ) nel frame a destra.

1. Nella finestra di dialogo [!UICONTROL Add Audience], [seleziona il pubblico desiderato](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md), quindi fai clic su **[!UICONTROL Assign Audience]**.

   Per impostazione predefinita, il pubblico è composto da tutti i visitatori. Tuttavia, è possibile modificarlo. I tipi di pubblico sono selezionati da [!UICONTROL Audience Library] oppure è possibile creare un pubblico per sola attività. [!UICONTROL Audience Library] contiene tipi di pubblico definiti in precedenza, inclusi alcuni di utilizzo comune già integrati in [!DNL Target].

1. (Facoltativo) Fai clic su **Combina tipi di pubblico** per [creare un pubblico che combini più tipi di pubblico](/help/main/c-target/combining-multiple-audiences.md).

1. (Condizionale) Per creare un nuovo pubblico che non sia già presente in [!UICONTROL Audience Library], fai clic su **Crea pubblico**. Durante il flusso di lavoro [create-audience](/help/main/c-target/c-audiences/audiences.md), puoi scegliere tra le seguenti opzioni:

   * Crea un pubblico on-demand salvato in [!UICONTROL Audience Library] che può essere riutilizzato in altre attività
   * Crea un pubblico [specifico per l&#39;attività](/help/main/c-target/creating-activity-only-audience.md) che non è salvato in [!UICONTROL Audience Library] e può essere utilizzato solo nell&#39;attività corrente

1. Fai clic su **[!UICONTROL Visitor Percentage]** nel riquadro a destra, quindi specifica la percentuale di visitatori idonei da includere nell&#39;attività.

1. Quando si è soddisfatti del pubblico, fare clic su **[!UICONTROL Next]** per passare al terzo passaggio del flusso di lavoro guidato in tre passaggi.

>[!NOTE]
>
>Quando apri l’elenco dei tipi di pubblico e questi sono stati importati da almeno 10 minuti, vengono importati automaticamente in background.

## Visualizzare le informazioni di un pubblico

1. Nella finestra di dialogo [!UICONTROL Add Audiences], fai clic sull&#39;icona **[!UICONTROL Information]** ( ![icona Info](/help/main/assets/icons/InfoOutline.svg) ) accanto a un pubblico per visualizzare i dettagli su tale pubblico, inclusi l&#39;origine e gli attributi.

1. Fare clic su **[!UICONTROL View Full Details]** per visualizzare ulteriori dettagli sul pubblico. I dettagli includono gli attributi del pubblico, la descrizione, l’area di lavoro, il tipo e l’origine del pubblico e un elenco di attività che fanno riferimento a tale pubblico. Puoi visualizzare informazioni su ogni pubblico, tra cui il nome dell’attività, lo stato, l’area di lavoro, la data dell’ultima modifica apportata al pubblico e chi l’ha effettuata.

## Modificare o copiare un pubblico

È possibile modificare o copiare un pubblico facendo clic sull&#39;icona [!UICONTROL More Actions] ( ![Icona Altre azioni](/help/main/assets/icons/More.svg) ) accanto al pubblico desiderato nella finestra di dialogo [!UICONTROL Add Audience], quindi facendo clic su [!UICONTROL Edit] o [!UICONTROL Copy].

È utile copiare un pubblico per crearne uno simile a un pubblico esistente. Puoi effettuare una copia del pubblico, apportarvi le modifiche desiderate, quindi salvarlo come nuovo pubblico.

