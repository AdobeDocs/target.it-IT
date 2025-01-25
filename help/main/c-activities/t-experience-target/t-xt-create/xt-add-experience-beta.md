---
keywords: creare un’esperienza;creazione di esperienza;priorità;pubblico;esperienza;compositore esperienza visivo
description: Scopri come utilizzare il  [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) per creare e modificare le esperienze sulla pagina in un'attività [!UICONTROL Experience Targeting] (XT).
title: Come si creano le esperienze in un'attività [!UICONTROL Experience Targeting]?
feature: Experience Targeting
hide: true
hidefromtoc: true
source-git-commit: 269ab2df7538d7e93774e3687bb931c9aaac27b6
workflow-type: tm+mt
source-wordcount: '897'
ht-degree: 23%

---

# Crea esperienza nelle attività [!UICONTROL Experience Targeting] (XT)

Il Compositore esperienza visivo [!UICONTROL Visual Experience Composer] in [!DNL Adobe Target] fornisce un&#39;interfaccia visiva per la modifica delle esperienze sulla pagina in un&#39;attività [!UICONTROL Experience Targeting] (XT).

1. Seleziona gli elementi da modificare e apporta le modifiche desiderate.

   Durante la [creazione di un&#39;attività [!UICONTROL Experience Targeting]](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md), il primo passaggio del flusso di lavoro guidato in tre parti ([!UICONTROL Experiences]) visualizza il [!UICONTROL Experience A] predefinito con un pubblico [!UICONTROL All Visitors].

   ![Pubblico Tutti i visitatori](/help/main/c-activities/t-experience-target/t-xt-create/assets/all-visitors-new.png)

   Tutte le modifiche apportate ora vengono applicate a [!UICONTROL Experience A]. In un passaggio successivo, fai clic su **[!UICONTROL Add Experience Targeting]** per creare altre esperienze.

   Quando passi il cursore del mouse sugli elementi nella pagina, gli elementi vengono evidenziati. Qualsiasi elemento evidenziato può essere modificato utilizzando il Compositore esperienza visivo. Per un elenco delle azioni che possono essere eseguite su un elemento per modificare l’esperienza, consulta [Opzioni del Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

   >[!NOTE]
   >
   >Per impostazione predefinita, il Compositore esperienza visivo non consente di modificare gli elementi contenenti JavaScript, ad esempio i banner rotanti. Puoi disattivare JavaScript per modificare tali elementi utilizzando il Compositore esperienza visivo.

1. Per creare altre esperienze, fai clic su **[!UICONTROL Add]** ( ![Aggiungi pulsante](/help/main/assets/icons/Add.svg) ).

   Viene visualizzata la finestra di dialogo [!UICONTROL Add Audience]. Per indirizzare un’esperienza a un pubblico, selezionalo prima di aggiungerla.

   La libreria del pubblico include tipi di pubblico definiti in precedenza, inclusi alcuni di utilizzo comune già integrati in [!DNL Target]. È possibile selezionare un pubblico dalla libreria o [crearne uno nuovo](/help/main/c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271).

   Oltre a selezionare un pubblico esistente, puoi combinare più tipi di pubblico per creare un pubblico combinato su richiesta anziché crearne uno nuovo. Per ulteriori informazioni, consulta [Combinazione di più tipi di pubblico](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

   Durante la creazione di un pubblico, puoi selezionare una posizione e specificarne i parametri relativi. In [!UICONTROL Custom] ([!UICONTROL Create Audience] > [!UICONTROL Custom]), selezionare il percorso, quindi specificare i parametri desiderati.

   >[!NOTE]
   >
   >I tipi di pubblico vengono importati automaticamente in background quando apri l’elenco dei tipi di pubblico e i tipi di pubblico importati hanno più di dieci minuti.

1. Seleziona uno o più tipi di pubblico per eseguire il targeting dell&#39;esperienza, quindi fai clic su **[!UICONTROL Assign Audience]**.

   L’esperienza B ora viene visualizzata nell’illustrazione precedente ed è destinata al pubblico appropriato.

1. Seleziona gli elementi da modificare per questa esperienza e apporta le modifiche desiderate, come spiegato nel precedente passaggio 1.

1. Ripeti i passaggi precedenti per creare altre esperienze con targeting, in base alle esigenze.

1. Fare clic su **[!UICONTROL Next]** al termine della progettazione delle esperienze.

   Il diagramma dell’attività mostra quanto segue:

   ![Diagramma di Targeting esperienza](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_diagram-refresh.png)

   >[!NOTE]
   >
   >È possibile consegnare un&#39;immagine da un&#39;origine diversa dalla pagina principale (ad esempio un&#39;immagine ospitata su `akamai.net` e consegnata il `adobe.com`). Le immagini in hosting altrove non vengono visualizzate nella miniatura della pagina mostrata nel diagramma di flusso.

1. (Facoltativo) Trascina e rilascia le coppie di pubblico ed esperienza durante la creazione o la modifica di [!UICONTROL Experience Targeting] attività per disporre le coppie nell&#39;ordine desiderato.

   Fai clic sull&#39;icona Riordina ( ![icona Riordina](/help/main/assets/icons/Reorder.svg) ) per visualizzare la colonna [!UICONTROL Experiences] a destra, quindi ridisponi le esperienze come desiderato.

   I visitatori verranno valutati per le esperienze in ordine, dall’alto verso il basso.

   [!UICONTROL Experience Targeting] presuppone che l&#39;ordine sia importante. Se un visitatore rientra nella prima coppia di pubblico ed esperienza, viene distribuita la prima esperienza.

   Si supponga, ad esempio, di non sapere che l&#39;ordine è importante durante la creazione di un&#39;attività [!UICONTROL Experience Targeting]. Successivamente, ti rendi conto durante i test che i visitatori che ritieni debbano qualificarsi per le esperienze B o C sono invece qualificati per l&#39;esperienza A. Questa situazione potrebbe essere dovuta al fatto che i tipi di pubblico non si escludono a vicenda e non sono nell’ordine corretto (ad esempio, esperienza A = Stati Uniti, esperienza B = San Francisco ed esperienza C = California). In questo scenario, tutti gli utenti degli Stati Uniti si qualificano per l&#39;esperienza A, anche se si trovano a San Francisco o altrove in California. Puoi riordinare le coppie di pubblico ed esperienza dalla più restrittiva alla meno restrittiva (San Francisco > California > Stati Uniti) senza ricreare l’intera attività.

   Se hai un pubblico [!UICONTROL All Visitors], assicurati che non sia il primo pubblico nel diagramma. Un&#39;esperienza con targeting &quot;[!UICONTROL All Visitors]&quot; può essere utilizzata come ultima esperienza nell&#39;attività [!UICONTROL Experience Targeting] per &quot;catturare&quot; i visitatori che non sono rientrati in nessun&#39;altra esperienza.

## Rinominare, modificare, duplicare o eliminare un’esperienza

Fare clic su un&#39;esperienza nel diagramma di un&#39;attività [!UICONTROL Experience Targeting] per visualizzare la colonna [!UICONTROL Experiences] sul lato destro.

![Opzioni Rinomina e Modifica](/help/main/c-activities/t-experience-target/t-xt-create/assets/experience_edit-refresh.png)

Scegli una delle seguenti opzioni, a seconda delle necessità:

* **[!UICONTROL Rename]**: digitare il nome desiderato nel campo [!UICONTROL Name].
* **[!UICONTROL Edit]**: fai clic sull&#39;icona Modifica ( ![icona Modifica](/help/main/assets/icons/Edit.svg) ), quindi apporta le modifiche desiderate.
* **[!UICONTROL Duplicate]**: copia un&#39;esperienza in un&#39;attività [!UICONTROL Experience Targeting] in modo da poter apportare modifiche minori senza dover ricreare l&#39;intera esperienza. Fai clic sull&#39;icona [!UICONTROL Duplicate] ( ![icona Duplica](/help/main/assets/icons/Duplicate.svg) ), quindi modifica l&#39;esperienza in base alle esigenze.
* **[!UICONTROL Delete]**: fai clic sull&#39;icona [!UICONTROL Delete] (![icona Elimina](/help/main/assets/icons/Delete.svg) ), quindi conferma l&#39;eliminazione.

## Video di formazione:

I video seguenti contengono ulteriori informazioni sui concetti descritti in questo articolo.

### Da test A/B a [!UICONTROL Experience Targeting]

Questo video descrive come portare il test A/B al livello successivo con [!UICONTROL Experience Targeting] (XT).

* Descrivi il flusso di lavoro guidato in tre passaggi per configurare un&#39;attività [!UICONTROL Experience Targeting]
* Descrivi come distribuire contenuti specifici per la posizione a tipi di pubblico in diverse aree geografiche
* Descrivi come riordinare le esperienze per garantire che il contenuto corretto venga distribuito al pubblico giusto

>[!VIDEO](https://video.tv.adobe.com/v/22418/)

### Tipi di attività (9:03)

Questo video spiega i tipi di attività disponibili in [!DNL Target]. [!UICONTROL Experience Targeting] è discusso a partire dalle 5:15.

* Descrizione dei tipi di attività inclusi in [!DNL Adobe Target]
* Selezionare il tipo di attività appropriato per i tuoi obiettivi
* Descrizione del flusso di lavoro guidato in tre passaggi da applicare a tutti i tipi di attività

>[!VIDEO](https://video.tv.adobe.com/v/17386)

### Utilizzo di [!UICONTROL Visual Experience Composer]

Questo video fornisce informazioni sull&#39;utilizzo delle opzioni [!UICONTROL Experience Targeting] (VEC).

* Modificare il contenuto di una pagina
* Modificare il layout di una pagina

>[!VIDEO](https://video.tv.adobe.com/v/17399)
