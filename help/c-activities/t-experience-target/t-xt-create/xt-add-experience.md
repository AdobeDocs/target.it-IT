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
source-git-commit: ca9639ccca286dac182728f7bbd43fac78217209

---


# Crea esperienza{#create-experience}

In Visual Experience Composer (Compositore esperienza visivo) è disponibile un&#39;interfaccia visiva per modificare le esperienze sulla pagina in un&#39;attività Experience Targeting (XT).

1. Seleziona gli elementi da modificare e apporta le modifiche desiderate.

   [Durante la creazione di un&#39;attività XT](/help/c-activities/t-experience-target/t-xt-create/xt-create.md), il passaggio uno del flusso di lavoro guidato in tre parti (Esperienze) mostra l&#39; [!UICONTROL Esperienza A predefinita] con un [!UICONTROL pubblico di tutti i visitatori] .

   ![Pubblico di tutti i visitatori](/help/c-activities/t-experience-target/t-xt-create/assets/all-visitors.png)

   Tutte le modifiche apportate ora si applicano all&#39;Esperienza A. In un passaggio seguente, fai clic **[!UICONTROL su Aggiungi targeting esperienza]** per creare esperienze aggiuntive.

   Quando passi il puntatore del mouse sopra gli elementi della pagina, gli elementi vengono evidenziati. Qualsiasi elemento evidenziato può essere modificato utilizzando la VEC. Per un elenco delle azioni che possono essere eseguite su un elemento per modificare l&#39;esperienza, consultate Opzioni [di Visual Experience Composer (Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/viztarget-options.md)).

   Se hai creato una mbox sulla pagina utilizzando Target Classic (in precedenza Test&amp;Target), questa viene visualizzata come un elemento che mostra il nome della mbox, e può essere modificata come qualsiasi altro elemento.

   >[!NOTE]
   >
   >Per impostazione predefinita, il Compositore esperienza visivo non consente di modificare gli elementi contenenti JavaScript, ad esempio i banner rotanti. Per modificare gli elementi mediante la VEC, è possibile selezionare javascript.

1. Per creare altre esperienze, fai clic **[!Asu Gg Experience Targeting (Impostazione destinazione esperienza)]**.

   ![Collegamento Aggiungi targeting esperienza](/help/c-activities/t-experience-target/t-xt-create/assets/add-experience-targeting.png)

   Viene visualizzata [!UICONTROL la finestra di] dialogo Choose Audience (Scegli audience). Per eseguire il targeting di un&#39;esperienza per un&#39;audience, dovete selezionare l&#39;audience prima di poter aggiungere un&#39;esperienza.

   La libreria del pubblico include tipi di pubblico definiti in precedenza, inclusi alcuni di utilizzo comune già integrati in Target. È possibile selezionare un pubblico dalla libreria, oppure [creare un nuovo pubblico](../../../c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271).

   >[!NOTE]
   >
   >Oltre a selezionare un pubblico esistente, puoi combinare più tipi di pubblico per creare un pubblico combinato ad hoc anziché crearne uno nuovo. Per ulteriori informazioni, consulta [Combinazione di più tipi di pubblico](../../../c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

   Durante la creazione di un pubblico, puoi selezionare una posizione (mbox) e specificarne i parametri. In [!UICONTROL Personalizzato] (Crea pubblico &gt; Aggiungi regola &gt; Personalizzato), selezionate la mbox, quindi specificate i parametri desiderati.

   >[!NOTE]
   >
   >Quando apri l’elenco dei tipi di pubblico e questi sono stati importati da almeno 10 minuti, vengono importati automaticamente in background.

1. Selezionate una o più audience per eseguire il targeting dell&#39;esperienza, quindi fate clic su **[!UICONTROL Done (Fine]**).

   ![Esperienza B](/help/c-activities/t-experience-target/t-xt-create/assets/experience-b.png)

   Noterai che l&#39;Esperienza B ora viene visualizzata nell&#39;illustrazione precedente e questa esperienza è destinata al pubblico dei visitatori degli Stati Uniti.

1. Selezionate gli elementi che desiderate modificare per questa esperienza e apportate le modifiche desiderate, come descritto al punto 1 precedente.

1. Ripetete i passaggi precedenti per creare esperienze con targeting aggiuntive, in base alle esigenze.

1. Fate clic **[!UICONTROL su Avanti]** quando avete terminato la progettazione delle esperienze.

   Il diagramma dell&#39;attività mostra quanto segue:

   ![Diagramma di targeting XT](/help/c-activities/t-experience-target/t-xt-create/assets/xt_diagram-new.png)

   >[!NOTE]
   >
   >Se distribuite un&#39;immagine da un&#39;origine diversa dalla pagina principale (ad esempio un&#39;immagine in hosting su akamai. net e distribuita in adobe.com), l&#39;immagine non viene visualizzata nella miniatura della pagina visualizzata nel diagramma di flusso.

1. (Condizionale) Trascina e rilascia le coppie di pubblico/esperienza durante la creazione o la modifica delle attività XT per disporre le coppie nell&#39;ordine desiderato.

   I visitatori vengono valutati per esperienze in ordine, dall&#39;alto verso il basso.

   ![Sposta esperienze](/help/c-activities/t-experience-target/t-xt-create/assets/move_experiences-new.png)

   Il targeting delle esperienze presuppone che l&#39;ordine sia importante. Se un visitatore rientra nella prima coppia Pubblico/Esperienza, viene consegnata la prima esperienza.

   Supponi, ad esempio, di non sapere che l’ordine è importante durante la creazione di un’attività di targeting esperienze. Successivamente, ti rendi conto durante i test che i visitatori che ritenevi più idonei per le esperienze B o C sono invece qualificati per l&#39;esperienza A. Questo potrebbe essere perché i tipi di pubblico non si escludono a vicenda e non sono nell&#39;ordine corretto (per esempio, esperienza A = Stati Uniti, esperienza B = San Francisco ed esperienza C = California). In questo scenario, tutti gli utenti degli Stati Uniti si qualificano per l&#39;esperienza A, sia che si trovino a San Francisco o altrove in California. È possibile riordinare le coppie Pubblico/Esperienza da più restrittive a meno restrittive (San Francisco &gt; California &gt; Stati Uniti) senza ricreare l&#39;intera attività.

   Se disponete di [!UICONTROL un pubblico di tutti i visitatori] , assicuratevi che non sia il primo pubblico nel diagramma. Un’esperienza rivolta a &quot;Tutti i visitatori&quot; può essere utilizzata come ultima esperienza nell’attività di targeting delle esperienze per includere i visitatori che non sono rientrati in nessun’altra esperienza.

## Rinominare o modificare un&#39;esperienza

Potete fare clic sull&#39;icona [!UICONTROL Modifica] (tre ellissi verticali) su un&#39;esperienza in un&#39;attività XT e scegliere tra le opzioni seguenti, a seconda delle necessità:

* Rinomina
* Modifica

![Opzioni Rinomina e Modifica](/help/c-activities/t-experience-target/t-xt-create/assets/experience_edit-new.png)

## Eliminare un&#39;esperienza

Nella pagina **[!UICONTROL Esperienze]** (il primo passaggio nel flusso di lavoro guidato in tre fasi), fate clic sulle tre ellissi verticali &gt; **[!UICONTROL Elimina]**.

![Elimina esperienza](/help/c-activities/t-experience-target/t-xt-create/assets/delete-experience.png)

## Duplicare un’esperienza

È possibile copiare un’esperienza in un’attività di Targeting esperienza (XT) così da poter apportare modifiche minori senza dover ricreare l’esperienza da zero.

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

Questo video spiega i tipi di attività disponibili in Target Standard/Premium. L&#39;esperienza di targeting è trattata a partire dal minuto 5:15.

* Descrizione dei tipi di attività inclusi in [!DNL Adobe Target]
* Selezionare il tipo di attività appropriato per i tuoi obiettivi
* Descrizione del flusso di lavoro guidato in tre passaggi da applicare a tutti i tipi di attività

>[!VIDEO](https://video.tv.adobe.com/v/17386?captions=ita)

### Utilizzo di Visual Experience Composer (Compositore esperienza visivo)

Questo video fornisce informazioni sull’utilizzo delle opzioni del Compositore esperienza visivo.

* Modificare il contenuto di una pagina
* Modificare il layout di una pagina

>[!VIDEO](https://video.tv.adobe.com/v/17399?captions=ita)