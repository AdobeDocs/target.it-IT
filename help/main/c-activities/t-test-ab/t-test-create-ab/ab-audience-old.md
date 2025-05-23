---
keywords: pubblico;selezionare il pubblico;scegliere il pubblico;audience;selettori
description: Il pubblico determina quali visitatori del sito vengono inseriti nell'attività di Adobe [!DNL Target] .
title: Come si seleziona un pubblico in un'attività  [!DNL Target] A/B?
feature: A/B Tests
exl-id: 281ae227-c593-4b71-ad12-865430b332be
source-git-commit: eb7e892a85fa3952ffc22172085d421756d0dfb5
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 64%

---

# Selezionare il pubblico

Il pubblico determina quali visitatori del sito vengono inseriti nell&#39;attività [!DNL Adobe Target].

>[!NOTE]
>
>Oltre a selezionare un pubblico esistente, puoi combinare più tipi di pubblico per creare un pubblico combinato ad hoc anziché crearne uno nuovo. Per ulteriori informazioni, consulta [Combinazione di più tipi di pubblico](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

1. Nella casella [!UICONTROL Audience], fai clic sull&#39;icona **[!UICONTROL Edit]** (puntini di sospensione verticali), quindi fai clic su **[!UICONTROL Replace Audience]**.

   ![Opzione Sostituisci pubblico](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/replace-audience.png)

   Per impostazione predefinita, il pubblico è composto da tutti i visitatori. Tuttavia, è possibile modificarlo. I tipi di pubblico vengono selezionati dalla libreria del pubblico oppure è possibile creare un pubblico per una sola attività. La libreria del pubblico contiene tipi di pubblico definiti in precedenza, inclusi alcuni di utilizzo comune già integrati in [!DNL Target].

1. Seleziona o crea il pubblico desiderato:

   * Selezionare un pubblico dalla libreria
   * [Combinare più tipi di pubblico](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5)
   * [Creare un nuovo pubblico](/help/main/c-target/c-audiences/create-audience.md#task_1D507519D3AD4390B507F188BD294DC1)
   * [Crea un pubblico per sola attività](/help/main/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483).

   Per un test A/B senza targeting di pubblico specifico, scegli il valore predefinito, [!UICONTROL All Visitors].

   È inoltre possibile modificare o copiare un pubblico passando il cursore sopra il pubblico desiderato nella finestra di dialogo [!UICONTROL Add Audience], come illustrato di seguito.

   È utile copiare un pubblico per crearne uno simile a un pubblico esistente. Puoi effettuare una copia del pubblico, apportarvi le modifiche desiderate, e quindi salvarlo come un nuovo pubblico. Questa funzionalità esiste anche in altri tipi di attività.

   ![Pubblico al passaggio del mouse](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/audience_picker_hover-new.png)

   Durante la creazione di un pubblico, puoi selezionare una posizione (mbox) e specificarne i parametri. In [!UICONTROL Custom Parameters], seleziona la mbox, quindi specifica i parametri desiderati.

   >[!NOTE]
   >
   >Quando apri l’elenco dei tipi di pubblico e questi sono stati importati da almeno 10 minuti, vengono importati automaticamente in background.

1. (Condizionale) Specifica la percentuale di visitatori idonei da includere nell’attività.

   Ad esempio, puoi scegliere di includere il 50% di tutti i visitatori.

   ![Percentuale di pubblico](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/audperc-new.png)

   Puoi anche scegliere di consentire a Target [di allocare automaticamente il traffico](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4).

## Video di formazione

I video seguenti contengono ulteriori informazioni sui concetti descritti in questo articolo.

### Utilizzo dei tipi di pubblico in Adobe Target (6:21) ![Icona Panoramica](/help/main/assets/overview.png)

Questo video spiega come utilizzare i tipi di pubblico in [!DNL Target Standard/Premium].

* Spiegazione del termine “pubblico”
* Spiegazione dei due modi in cui il pubblico viene utilizzato per lʼottimizzazione
* Trovare un pubblico nellʼelenco Tipi di pubblico
* Indirizzare unʼattività a un pubblico
* Utilizzare i tipi di pubblico per la reportistica passiva in un’attività

>[!VIDEO](https://video.tv.adobe.com/v/36328?captions=ita)

### Flusso di lavoro attività - Targeting (2:14) ![Icona esercitazione](/help/main/assets/tutorial.png)

Questo video contiene informazioni su come impostare i tipi di pubblico.

* Assegnare un pubblico all’attività
* Limitare il traffico verso l’alto o il basso
* Selezionare il metodo di allocazione del traffico
* Allocare il traffico tra diverse esperienze

>[!VIDEO](https://video.tv.adobe.com/v/17385)

Per informazioni dettagliate, consulta [Tipi di pubblico](/help/main/c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271).
