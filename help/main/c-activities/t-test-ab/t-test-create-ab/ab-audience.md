---
keywords: pubblico;selezionare il pubblico;scegliere il pubblico;audience;selettori
description: Il pubblico determina quali visitatori del sito vengono inseriti nell’Adobe [!DNL Target] attività.
title: Come si seleziona un pubblico in un [!DNL Target] Attività A/B?
feature: A/B Tests
exl-id: 281ae227-c593-4b71-ad12-865430b332be
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 91%

---

# Selezionare il pubblico

Il pubblico determina quali visitatori del sito vengono inseriti nel tuo [!DNL Adobe Target] attività.

>[!NOTE]
>
>Oltre a selezionare un pubblico esistente, puoi combinare più tipi di pubblico per creare un pubblico combinato ad hoc anziché crearne uno nuovo. Per ulteriori informazioni, consulta [Combinazione di più tipi di pubblico](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

Fai clic sull’icona Modifica (tre puntini di sospensione verticali) nella casella [!UICONTROL Pubblico], quindi fai clic su **[!UICONTROL Sostituisci pubblico]**.

![Opzione Sostituisci pubblico](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/replace-audience.png)

Per impostazione predefinita, il pubblico è composto da tutti i visitatori. Tuttavia, è possibile modificarlo. I tipi di pubblico vengono selezionati dalla libreria del pubblico oppure è possibile creare un pubblico per una sola attività. La libreria del pubblico include tipi di pubblico definiti in precedenza, inclusi alcuni di utilizzo comune già integrati in Target. È possibile selezionare un pubblico dalla libreria, [crearne uno nuovo](/help/main/c-target/c-audiences/create-audience.md#task_1D507519D3AD4390B507F188BD294DC1) o [creare un pubblico per la sola attività](/help/main/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483). Per un test A/B senza targeting per uno specifico pubblico, scegli l&#39;impostazione predefinita, Tutti i visitatori.

È anche possibile modificare o copiare un pubblico passando il cursore sopra il pubblico desiderato nella finestra di dialogo [!UICONTROL Scegli il pubblico], come illustrato di seguito. È utile copiare un pubblico per crearne uno simile a un pubblico esistente. Puoi effettuare una copia del pubblico, apportarvi le modifiche desiderate, e quindi salvarlo come un nuovo pubblico. Questa funzionalità esiste anche in altri tipi di attività.

![Pubblico al passaggio del mouse](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/audience_picker_hover-new.png)

Durante la creazione di un pubblico, puoi selezionare una posizione (mbox) e specificarne i parametri. In Parametri personalizzati, seleziona la mbox e specifica i parametri desiderati.

>[!NOTE]
>
>Quando apri l’elenco dei tipi di pubblico e questi sono stati importati da almeno 10 minuti, vengono importati automaticamente in background.

Fai clic sulla freccia rivolta verso il basso per rimuovere il pubblico esistente o per cambiare pubblico.

Puoi specificare la percentuale di visitatori idonei da includere nell’attività. Ad esempio, puoi scegliere di includere il 50% di tutti i visitatori.

![Percentuale di pubblico](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/audperc-new.png)

Puoi anche scegliere di lasciare che Target [allochi automaticamente il traffico](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4).

## Video di formazione

I video seguenti contengono ulteriori informazioni sui concetti descritti in questo articolo.

### Utilizzo dei tipi di pubblico in Adobe Target (6:21) ![Icona Panoramica](/help/main/assets/overview.png)

Questo video spiega come utilizzare i tipi di pubblico in [!DNL Target Standard/Premium].

* Spiegazione del termine “pubblico”
* Spiegazione dei due modi in cui il pubblico viene utilizzato per lʼottimizzazione
* Trovare un pubblico nellʼelenco Tipi di pubblico
* Indirizzare unʼattività a un pubblico
* Utilizzare i tipi di pubblico per la reportistica passiva in un’attività

>[!VIDEO](https://video.tv.adobe.com/v/17398)

### Flusso di lavoro di un’attività - Targeting (2:14) ![Badge tutorial](/help/main/assets/tutorial.png)

Questo video contiene informazioni su come impostare i tipi di pubblico.

* Assegnare un pubblico all’attività
* Limitare il traffico verso l’alto o il basso
* Selezionare il metodo di allocazione del traffico
* Allocare il traffico tra diverse esperienze

>[!VIDEO](https://video.tv.adobe.com/v/17385)

Per informazioni dettagliate, consulta [Tipi di pubblico](/help/main/c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271).