---
description: In Visual Experience Composer (Compositore esperienza visivo) è disponibile un'interfaccia visiva per modificare le esperienze sulla pagina in un'attività Experience Targeting (XT).
keywords: creare un’esperienza;creazione di esperienza;priorità;pubblico;esperienza;compositore esperienza visivo
seo-description: Adobe Target Visual Experience Composer (VEC) offre un'interfaccia visiva per modificare le esperienze sulla pagina in un'attività di Targeting delle esperienze (XT).
seo-title: Creare esperienze
solution: Target
title: Creare esperienze
topic: Advanced,Standard,Classic
uuid: ce559c3c-5a16-46b8-b2a7-df696626c7c0
translation-type: tm+mt
source-git-commit: 6911a91aba8505e8f91a7ab9723c54bd8e7082b7

---


# Create experience{#create-experience}

The [!UICONTROL Visual Experience Composer] (VEC) provides a visual interface for editing the experiences on your page in an [!UICONTROL Experience Targeting] (XT) activity.

1. Seleziona gli elementi da modificare e apporta le modifiche desiderate.

   [Durante la creazione di un'attività XT](/help/c-activities/t-experience-target/t-xt-create/xt-create.md), il passaggio uno del flusso di lavoro guidato in tre parti ([!UICONTROL Esperienze]) mostra l' [!UICONTROL Esperienza A predefinita] con un [!UICONTROL pubblico di tutti i visitatori] .

   ![Pubblico di tutti i visitatori](/help/c-activities/t-experience-target/t-xt-create/assets/all-visitors.png)

   Any changes you make now apply to Experience A. In a step below, you'll click **[!UICONTROL Add Experience Targeting]** to create additional experiences.

   Quando passi il puntatore del mouse sopra gli elementi della pagina, gli elementi vengono evidenziati. Qualsiasi elemento evidenziato può essere modificato utilizzando la VEC. For a list of actions that can be performed on an element to change the experience, see [Visual Experience Composer Options](/help/c-experiences/c-visual-experience-composer/viztarget-options.md).

   If you created an mbox on the page using [!DNL Target Classic], that mbox appears as an element that shows the mbox name, and can be modified like any other element.

   >[!NOTE]
   >
   >Per impostazione predefinita, la VEC non consente modifiche agli elementi che contengono javascript, ad esempio i banner a rotazione. È possibile selezionare per disabilitare javascript per modificare questi elementi utilizzando la VEC.

1. To create additional experiences, click **[!UICONTROL Add Experience Targeting]**.

   ![Collegamento Aggiungi targeting esperienza](/help/c-activities/t-experience-target/t-xt-create/assets/add-experience-targeting.png)

   The [!UICONTROL Choose Audience] dialog box displays. Per eseguire il targeting di un'esperienza per un'audience, dovete selezionare l'audience prima di poter aggiungere un'esperienza.

   La libreria del pubblico include tipi di pubblico definiti in precedenza, inclusi alcuni di utilizzo comune già integrati in [!DNL Target]. You can select an audience from the library or [create a new audience](../../../c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271).

   >[!NOTE]
   >
   >Oltre a selezionare un pubblico esistente, puoi combinare più tipi di pubblico per creare un pubblico combinato ad hoc anziché crearne uno nuovo. Per ulteriori informazioni, consulta [Combinazione di più tipi di pubblico](../../../c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

   Durante la creazione di un pubblico, puoi selezionare una posizione (mbox) e specificarne i parametri. Under [!UICONTROL Custom] (Create Audience &gt; Add Rule &gt; Custom), select the mbox, then specify the desired parameters.

   >[!NOTE]
   >
   >Quando apri l’elenco dei tipi di pubblico e questi sono stati importati da almeno 10 minuti, vengono importati automaticamente in background.

1. Select one or more audiences to target with the experience, then click **[!UICONTROL Done]**.

   ![Esperienza B](/help/c-activities/t-experience-target/t-xt-create/assets/experience-b.png)

   Noterai che l'Esperienza B ora viene visualizzata nell'illustrazione precedente e questa esperienza è destinata al pubblico dei visitatori degli Stati Uniti.

1. Selezionate gli elementi che desiderate modificare per questa esperienza e apportate le modifiche desiderate, come descritto al punto 1 precedente.

1. Ripetete i passaggi precedenti per creare esperienze con targeting aggiuntive, in base alle esigenze.

1. Click **[!UICONTROL Next]** when you are finished designing your experiences.

   Il diagramma dell'attività mostra quanto segue:

   ![Diagramma di targeting XT](/help/c-activities/t-experience-target/t-xt-create/assets/xt_diagram-new.png)

   >[!NOTE]
   >
   >If you deliver an image from a source other than your main page (such as an image hosted on `akamai.net` and delivered on `adobe.com`), that image does not display in the thumbnail of the page shown in the flow diagram.

1. (Condizionale) Trascina e rilascia le coppie di pubblico/esperienza durante la creazione o la modifica delle attività XT per disporre le coppie nell'ordine desiderato.

   I visitatori vengono valutati per esperienze in ordine, dall'alto verso il basso.

   ![Sposta esperienze](/help/c-activities/t-experience-target/t-xt-create/assets/move_experiences-new.png)

   [!UICONTROL Il targeting delle esperienze presuppone che l'ordine sia importante. ] Se un visitatore rientra nella prima coppia Pubblico/Esperienza, viene consegnata la prima esperienza.

   Supponi, ad esempio, di non sapere che l’ordine è importante durante la creazione di un’attività di targeting esperienze. Successivamente, ti rendi conto durante i test che i visitatori che ritenevi più idonei per le esperienze B o C sono invece qualificati per l'esperienza A. Questo potrebbe essere perché i tipi di pubblico non si escludono a vicenda e non sono nell'ordine corretto (per esempio, esperienza A = Stati Uniti, esperienza B = San Francisco ed esperienza C = California). In questo scenario, tutti gli utenti degli Stati Uniti si qualificano per l'esperienza A, sia che si trovino a San Francisco o altrove in California. È possibile riordinare le coppie Pubblico/Esperienza da più restrittive a meno restrittive (San Francisco &gt; California &gt; Stati Uniti) senza ricreare l'intera attività.

   If you have an [!UICONTROL All Visitors] audience, ensure that it is not the first audience in the diagram. Un’esperienza rivolta a "Tutti i visitatori" può essere utilizzata come ultima esperienza nell’attività di targeting delle esperienze per includere i visitatori che non sono rientrati in nessun’altra esperienza.

## Rinominare o modificare un'esperienza

You can click the [!UICONTROL Edit] icon (three vertical ellipses) on an experience in an XT activity and choose from the following options, as necessary:

* Rinomina
* Modifica

![Opzioni Rinomina e Modifica](/help/c-activities/t-experience-target/t-xt-create/assets/experience_edit-new.png)

## Eliminare un'esperienza

On the **[!UICONTROL Experiences]** page (the first step in the three-step guided workflow), click the three vertical ellipses &gt; **[!UICONTROL Delete]**.

![Elimina esperienza](/help/c-activities/t-experience-target/t-xt-create/assets/delete-experience.png)

## Duplicazione di un'esperienza

Potete copiare un'esperienza in un'attività XT in modo da apportarvi modifiche minori senza dover ricreare l'esperienza da zero.

Nella pagina **[!UICONTROL Esperienze]** (il primo passaggio del flusso di lavoro guidato in tre passaggi), fai clic sui tre puntini di sospensione verticali &gt; **[!UICONTROL Duplica]**.

![Duplica esperienza](/help/c-activities/t-experience-target/t-xt-create/assets/duplicate_experience-new.png)

## Video di formazione:

I video seguenti contengono ulteriori informazioni sui concetti descritti in questo articolo.

### Da test A/B a targeting esperienza

Questo video descrive come effettuare un test A/B al livello successivo con il targeting esperienza (XT).

* Descrivi il flusso di lavoro guidato in tre fasi per configurare un attività XT
* Scopri come distribuire contenuti specifici per il sito a un pubblico che si trova in aree geografiche diverse
* Descrivi come riordinare le esperienze per garantire che il contenuto corretto venga distribuito al pubblico giusto

>[!VIDEO](https://video.tv.adobe.com/v/22418/?captions=ita)

### Tipi di attività (9:03)

Questo video spiega i tipi di attività disponibili in Target Standard/Premium. L'esperienza di targeting è trattata a partire dal minuto 5:15.

* Descrizione dei tipi di attività inclusi in [!DNL Adobe Target]
* Selezionare il tipo di attività appropriato per i tuoi obiettivi
* Descrizione del flusso di lavoro guidato in tre passaggi da applicare a tutti i tipi di attività

>[!VIDEO](https://video.tv.adobe.com/v/17386?captions=ita)

### Utilizzo di Visual Experience Composer (Compositore esperienza visivo)

Questo video fornisce informazioni sull’utilizzo delle opzioni del Compositore esperienza visivo.

* Modificare il contenuto di una pagina
* Modificare il layout di una pagina

>[!VIDEO](https://video.tv.adobe.com/v/17399?captions=ita)