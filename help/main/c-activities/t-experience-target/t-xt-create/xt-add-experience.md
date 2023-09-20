---
keywords: creare un’esperienza;creazione di esperienza;priorità;pubblico;esperienza;compositore esperienza visivo
description: Scopri come utilizzare il [!DNL Adobe Target] [!UICONTROL Compositore esperienza visivo] (VEC) per creare e modificare le esperienze sulla pagina in un [!UICONTROL Targeting esperienza] (XT) attività.
title: Come si creano le esperienze in un [!UICONTROL Targeting esperienza] Attività?
feature: Experience Targeting
exl-id: ec3fcd93-5557-4f69-8f9c-4d00569188ad
source-git-commit: 0dfdd995c00961ed2aed91ec03406e8493292af7
workflow-type: tm+mt
source-wordcount: '953'
ht-degree: 39%

---

# Creare esperienze in [!UICONTROL Targeting esperienza] Attività (XT)

Il [!UICONTROL Compositore esperienza visivo] (VEC) in [!DNL Adobe Target] fornisce un’interfaccia visiva per la modifica delle esperienze sulla pagina in un [!UICONTROL Targeting esperienza] (XT) attività.

1. Seleziona gli elementi da modificare e apporta le modifiche desiderate.

   Mentre [creazione di un [!UICONTROL Targeting esperienza] attività](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md), passaggio 1 del flusso di lavoro guidato in tre parti ([!UICONTROL Esperienze]) visualizza il valore predefinito [!UICONTROL Esperienza A] con un [!UICONTROL Tutti i visitatori] pubblico.

   ![Pubblico Tutti i visitatori](/help/main/c-activities/t-experience-target/t-xt-create/assets/all-visitors.png)

   Eventuali modifiche apportate ora vengono applicate a [!UICONTROL Esperienza A]. In un passaggio successivo, fai clic su **[!UICONTROL Aggiungi targeting esperienza]** per creare altre esperienze.

   Quando passi il cursore del mouse sugli elementi nella pagina, gli elementi vengono evidenziati. Qualsiasi elemento evidenziato può essere modificato utilizzando il Compositore esperienza visivo. Per un elenco delle azioni che possono essere eseguite su un elemento per modificare l’esperienza, consulta [Opzioni del Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

   >[!NOTE]
   >
   >Per impostazione predefinita, il Compositore esperienza visivo non consente di modificare gli elementi contenenti JavaScript, ad esempio i banner rotanti. Puoi disattivare JavaScript per modificare tali elementi utilizzando il Compositore esperienza visivo.

1. Per creare altre esperienze, fai clic su **[!UICONTROL Aggiungi targeting esperienza]**.

   ![Collegamento Aggiungi targeting esperienza](/help/main/c-activities/t-experience-target/t-xt-create/assets/add-experience-targeting.png)

   Il [!UICONTROL Aggiungi pubblico] viene visualizzata. Per indirizzare un’esperienza a un pubblico, selezionalo prima di aggiungerla.

   La libreria del pubblico include tipi di pubblico definiti in precedenza, inclusi alcuni di utilizzo comune già integrati in [!DNL Target]. È possibile selezionare un pubblico dalla libreria o [crearne uno nuovo](/help/main/c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271).

   Oltre a selezionare un pubblico esistente, puoi combinare più tipi di pubblico per creare un pubblico combinato ad hoc anziché crearne uno nuovo. Per ulteriori informazioni, consulta [Combinazione di più tipi di pubblico](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

   Durante la creazione di un pubblico, puoi selezionare una posizione e specificarne i parametri relativi. Sotto [!UICONTROL Personalizzato] ([!UICONTROL Crea pubblico] > [!UICONTROL Personalizzato]), seleziona la posizione, quindi specifica i parametri desiderati.

   >[!NOTE]
   >
   >I tipi di pubblico vengono importati automaticamente in background quando apri l’elenco dei tipi di pubblico e i tipi di pubblico importati hanno più di dieci minuti.

1. Seleziona uno o più tipi di pubblico per eseguire il targeting dell’esperienza, quindi fai clic su **[!UICONTROL Fine]**.

   ![Esperienza B](/help/main/c-activities/t-experience-target/t-xt-create/assets/experience-b.png)

   L’esperienza B ora viene visualizzata nell’illustrazione precedente ed è destinata al pubblico dei visitatori degli Stati Uniti.

1. Seleziona gli elementi da modificare per questa esperienza e apporta le modifiche desiderate, come spiegato nel precedente passaggio 1.

1. Ripeti i passaggi precedenti per creare altre esperienze con targeting, in base alle esigenze.

1. Al termine, fai clic su **[!UICONTROL Successivo]**.

   Il diagramma dell’attività mostra quanto segue:

   ![Diagramma di Targeting esperienza](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_diagram-new.png)

   >[!NOTE]
   >
   >Puoi distribuire un’immagine da un’origine diversa dalla pagina principale (ad esempio un’immagine in hosting su `akamai.net` e consegnato il `adobe.com`). Le immagini in hosting altrove non vengono visualizzate nella miniatura della pagina mostrata nel diagramma di flusso.

1. (Condizionale) Trascina e rilascia coppie di pubblico ed esperienza durante la creazione o la modifica [!UICONTROL Targeting esperienza] attività per disporre le coppie nell’ordine desiderato.

   I visitatori verranno valutati per le esperienze in ordine, dall’alto verso il basso.

   ![Spostare le esperienze](/help/main/c-activities/t-experience-target/t-xt-create/assets/move_experiences-new.png)

   Nel [!UICONTROL targeting delle esperienze] si presuppone che l’ordine sia rilevante. Se un visitatore rientra nella prima coppia di pubblico ed esperienza, viene distribuita la prima esperienza.

   Ad esempio, supponiamo che tu non sappia che l&#39;ordine è importante durante la creazione di un [!UICONTROL Targeting esperienza] attività. Successivamente, ti rendi conto durante i test che i visitatori che ritenevi più idonei per le esperienze B o C sono invece qualificati per l&#39;esperienza A. Questo potrebbe essere perché i tipi di pubblico non si escludono a vicenda e non sono nell&#39;ordine corretto (per esempio, esperienza A = Stati Uniti, esperienza B = San Francisco ed esperienza C = California). In questo scenario, tutti gli utenti degli Stati Uniti si qualificano per l&#39;esperienza A, anche se si trovano a San Francisco o altrove in California. Puoi riordinare le coppie di pubblico ed esperienza dalla più restrittiva alla meno restrittiva (San Francisco > California > Stati Uniti) senza ricreare l’intera attività.

   Se hai un pubblico [!UICONTROL Tutti i visitatori], assicurati che questo non sia il primo pubblico nel diagramma. Un’esperienza con targeting &quot;[!UICONTROL Tutti i visitatori]&quot; può essere utilizzato come ultima esperienza nel [!UICONTROL Targeting esperienza] attività per &quot;catturare&quot; i visitatori che non sono rientrati in nessun’altra esperienza.

## Rinominare o modificare un’esperienza

Puoi fare clic su [!UICONTROL Modifica] (puntini di sospensione verticali) in un’esperienza in un’esperienza [!UICONTROL Targeting esperienza] e scegliere tra le seguenti opzioni, a seconda delle necessità:

* [!UICONTROL Rinomina]
* [!UICONTROL Modifica]

![Opzioni Rinomina e Modifica](/help/main/c-activities/t-experience-target/t-xt-create/assets/experience_edit-new.png)

## Eliminare un’esperienza

Il giorno **[!UICONTROL Esperienze]** (il primo passaggio nel flusso di lavoro guidato in tre passaggi), fai clic sui puntini di sospensione verticali > **[!UICONTROL Elimina]**.

![Eliminare un’esperienza](/help/main/c-activities/t-experience-target/t-xt-create/assets/delete-experience.png)

## Duplicare un’esperienza

È possibile copiare un’esperienza in un [!UICONTROL Targeting esperienza] per apportare modifiche minori senza dover ricreare l’intera esperienza.

Il giorno **[!UICONTROL Esperienze]** (il primo passaggio nel flusso di lavoro guidato in tre passaggi), fai clic sui puntini di sospensione verticali > **[!UICONTROL Duplica]**.

![Duplicare un’esperienza](/help/main/c-activities/t-experience-target/t-xt-create/assets/duplicate_experience-new.png)

## Video di formazione:

I video seguenti contengono ulteriori informazioni sui concetti descritti in questo articolo.

### Da test A/B a [!UICONTROL Targeting esperienza]

Questo video descrive come portare il test A/B a un livello successivo con [!UICONTROL Targeting esperienza] (XT)

* Descrivi il flusso di lavoro guidato in tre passaggi per configurare una [!UICONTROL Targeting esperienza] attività
* Descrivi come distribuire contenuti specifici per la posizione a tipi di pubblico in diverse aree geografiche
* Descrivi come riordinare le esperienze per garantire che il contenuto corretto venga distribuito al pubblico giusto

>[!VIDEO](https://video.tv.adobe.com/v/22418/)

### Tipi di attività (9:03)

Questo video spiega i tipi di attività disponibili in [!DNL Target]. [!UICONTROL L&#39;esperienza di targeting è trattata a partire dal minuto 5:15.]

* Descrizione dei tipi di attività inclusi in [!DNL Adobe Target]
* Selezionare il tipo di attività appropriato per i tuoi obiettivi
* Descrizione del flusso di lavoro guidato in tre passaggi da applicare a tutti i tipi di attività

>[!VIDEO](https://video.tv.adobe.com/v/17386)

### Utilizzo di [!UICONTROL Compositore esperienza visivo]

Questo video fornisce informazioni sull’utilizzo di [!UICONTROL Targeting esperienza] (VEC).

* Modificare il contenuto di una pagina
* Modificare il layout di una pagina

>[!VIDEO](https://video.tv.adobe.com/v/17399)
