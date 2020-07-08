---
keywords: create experience;experience create;priority;audience;experience;visual experience composer
description: Il Compositore esperienza visivo di Adobe Target offre un’interfaccia visiva per la modifica delle esperienze sulla pagina in un’attività Targeting esperienza.
title: Creare esperienze
topic: Advanced,Standard,Classic
uuid: ce559c3c-5a16-46b8-b2a7-df696626c7c0
translation-type: tm+mt
source-git-commit: c7664f9674234565a3657f453541095811fa5aa6
workflow-type: tm+mt
source-wordcount: '962'
ht-degree: 93%

---


# Creare esperienze{#create-experience}

Il [!UICONTROL Compositore esperienza visivo] offre un’interfaccia visiva per la modifica delle esperienze sulla pagina in un’attività [!UICONTROL Targeting esperienza].

1. Seleziona gli elementi da modificare e apporta le modifiche desiderate.

   Durante la [creazione di un’attività Targeting esperienza](/help/c-activities/t-experience-target/t-xt-create/xt-create.md), il primo passaggio nel flusso di lavoro guidato in tre parti ([!UICONTROL Esperienze]) mostra l’[!UICONTROL Esperienza A] predefinita con un pubblico di tipo [!UICONTROL Tutti i visitatori].

   ![Pubblico Tutti i visitatori](/help/c-activities/t-experience-target/t-xt-create/assets/all-visitors.png)

   Eventuali modifiche apportate ora vengono applicate all’Esperienza A. In un passaggio successivo, fai clic su **[!UICONTROL Aggiungi targeting esperienza]** per creare altre esperienze.

   Quando passi il puntatore del mouse sopra gli elementi della pagina, gli elementi vengono evidenziati. Qualsiasi elemento evidenziato può essere modificato utilizzando il Compositore esperienza visivo. Per un elenco delle azioni che possono essere eseguite su un elemento per modificare l’esperienza, consulta [Opzioni del Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/viztarget-options.md).

   If you created a [!DNL Target] request on the page using [!DNL Target Classic], that [!DNL Target] request appears as an element that shows the request name, and can be modified like any other element.

   >[!NOTE]
   >
   >Per impostazione predefinita, il Compositore esperienza visivo non consente di modificare gli elementi contenenti JavaScript, ad esempio i banner rotanti. È possibile disattivare JavaScript per poter modificare tali elementi utilizzando il Compositore esperienza visivo.

1. Per creare altre esperienze, fai clic su **[!UICONTROL Aggiungi targeting esperienza]**.

   ![Collegamento Aggiungi targeting esperienza](/help/c-activities/t-experience-target/t-xt-create/assets/add-experience-targeting.png)

   Viene visualizzata la finestra di dialogo [!UICONTROL Scegli pubblico]. Per eseguire il targeting di un’esperienza per un pubblico, è necessario selezionare il pubblico prima di poter aggiungere un’esperienza.

   La libreria del pubblico include tipi di pubblico definiti in precedenza, inclusi alcuni di utilizzo comune già integrati in [!DNL Target]. È possibile selezionare un pubblico dalla libreria o [crearne uno nuovo](../../../c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271).

   >[!NOTE]
   >
   >Oltre a selezionare un pubblico esistente, puoi combinare più tipi di pubblico per creare un pubblico combinato ad hoc anziché crearne uno nuovo. Per ulteriori informazioni, consulta [Combinazione di più tipi di pubblico](../../../c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

   Quando create un&#39;audience, potete selezionare una posizione e specificare i parametri per tale posizione. Under [!UICONTROL Custom] (Create Audience > Add Rule > Custom), select the location, then specify the desired parameters.

   >[!NOTE]
   >
   >Quando apri l’elenco dei tipi di pubblico e questi sono stati importati da almeno 10 minuti, vengono importati automaticamente in background.

1. Seleziona uno o più tipi di pubblico per eseguire il targeting dell’esperienza, quindi fai clic su **[!UICONTROL Fine]**.

   ![Esperienza B](/help/c-activities/t-experience-target/t-xt-create/assets/experience-b.png)

   Osserva che l’Esperienza B è ora visualizzata nell’illustrazione precedente ed è destinata al pubblico dei visitatori degli Stati Uniti.

1. Seleziona gli elementi da modificare per questa esperienza e apporta le modifiche desiderate, come descritto per il precedente passaggio 1.

1. Ripeti i passaggi precedenti per creare altre esperienze con targeting, in base alle esigenze.

1. Al termine, fai clic su **[!UICONTROL Successivo]**.

   Il diagramma dell’attività mostra quanto segue:

   ![Diagramma di Targeting esperienza](/help/c-activities/t-experience-target/t-xt-create/assets/xt_diagram-new.png)

   >[!NOTE]
   >
   >Se distribuisci un’immagine da un’origine che non corrisponde alla pagina principale (ad esempio un’immagine in hosting su `akamai.net` e distribuita su `adobe.com`), l’immagine non viene visualizzata nella miniatura della pagina mostrata nel diagramma di flusso.

1. (Condizionale) È possibile trascinare e rilasciare le coppie Pubblico/Esperienza durante la creazione o la modifica di attività di Targeting esperienza per disporre le coppie nell’ordine desiderato.

   I visitatori verranno valutati per le esperienze in ordine, dall’alto verso il basso.

   ![Spostare le esperienze](/help/c-activities/t-experience-target/t-xt-create/assets/move_experiences-new.png)

   Nel [!UICONTROL targeting delle esperienze] si presuppone che l’ordine sia rilevante. Se un visitatore rientra nella prima coppia Pubblico/Esperienza, viene consegnata la prima esperienza.

   Supponi, ad esempio, di non sapere che l’ordine è importante durante la creazione di un’attività di targeting esperienze. Successivamente, ti rendi conto durante i test che i visitatori che ritenevi più idonei per le esperienze B o C sono invece qualificati per l&#39;esperienza A. Questo potrebbe essere perché i tipi di pubblico non si escludono a vicenda e non sono nell&#39;ordine corretto (per esempio, esperienza A = Stati Uniti, esperienza B = San Francisco ed esperienza C = California). In questo scenario, tutti gli utenti degli Stati Uniti si qualificano per l&#39;esperienza A, sia che si trovino a San Francisco o altrove in California. È possibile riordinare le coppie Pubblico/Esperienza da più restrittive a meno restrittive (San Francisco > California > Stati Uniti) senza ricreare l&#39;intera attività.

   Se hai un pubblico [!UICONTROL Tutti i visitatori], assicurati che questo non sia il primo pubblico nel diagramma. Un’esperienza rivolta a “Tutti i visitatori” può essere utilizzata come ultima esperienza nell’attività di targeting delle esperienze in modo da includere i visitatori che non sono rientrati in nessun’altra esperienza.

## Rinominare o modificare un’esperienza

Fai clic sull’icona [!UICONTROL Modifica] (tre puntini di sospensione verticali) in un’esperienza in un’attività di Targeting esperienza e scegli tra le seguenti opzioni, a seconda delle necessità:

* Rinomina
* Modifica

![Opzioni Rinomina e Modifica](/help/c-activities/t-experience-target/t-xt-create/assets/experience_edit-new.png)

## Eliminare un’esperienza

Nella pagina **[!UICONTROL Esperienze]** (il primo passaggio del flusso di lavoro guidato in tre passaggi), fai clic sui tre puntini di sospensione verticali e scegli **[!UICONTROL Elimina]**.

![Eliminare un’esperienza](/help/c-activities/t-experience-target/t-xt-create/assets/delete-experience.png)

## Duplicare un’esperienza

È possibile copiare un’esperienza in un’attività di Targeting esperienza (XT) così da poter apportare modifiche minori senza dover ricreare l’esperienza da zero.

Nella pagina **[!UICONTROL Esperienze]** (il primo passaggio del flusso di lavoro guidato in tre passaggi), fai clic sui tre puntini di sospensione verticali > **[!UICONTROL Duplica]**.

![Duplicare un’esperienza](/help/c-activities/t-experience-target/t-xt-create/assets/duplicate_experience-new.png)

## Video di formazione:

I video seguenti contengono ulteriori informazioni sui concetti descritti in questo articolo.

### Da test A/B a targeting esperienza

Questo video descrive come effettuare un test A/B al livello successivo con il targeting esperienza (XT).

* Descrivi il flusso di lavoro guidato in tre fasi per configurare un attività XT
* Scopri come distribuire contenuti specifici per il sito a un pubblico che si trova in aree geografiche diverse
* Descrivi come riordinare le esperienze per garantire che il contenuto corretto venga distribuito al pubblico giusto

>[!VIDEO](https://video.tv.adobe.com/v/22418/)

### Tipi di attività (9:03)

Questo video spiega i tipi di attività disponibili in Target Standard/Premium. L&#39;esperienza di targeting è trattata a partire dal minuto 5:15.

* Descrizione dei tipi di attività inclusi in [!DNL Adobe Target]
* Selezionare il tipo di attività appropriato per i tuoi obiettivi
* Descrizione del flusso di lavoro guidato in tre passaggi da applicare a tutti i tipi di attività

>[!VIDEO](https://video.tv.adobe.com/v/17386)

### Utilizzo del Compositore esperienza visivo

Questo video fornisce informazioni sull’utilizzo delle opzioni del Compositore esperienza visivo.

* Modificare il contenuto di una pagina
* Modificare il layout di una pagina

>[!VIDEO](https://video.tv.adobe.com/v/17399)