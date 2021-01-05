---
keywords: dedupe;allow duplicates;exclude duplicate offers;automated personalization;disallow duplicate offers;exclude;default content;exclusion group;
description: Gestisci le esclusioni creando gruppi di esclusione o escludendo le offerte duplicate, esperienze specifiche e contenuti predefiniti nelle attività di Personalizzazione automatizzata in Adobe Target.
title: Gestire le esclusioni
feature: Automated Personalization
solution: Target,Analytics
translation-type: tm+mt
source-git-commit: 4adade56529fb95e4400e06d04d3c6c69e120edc
workflow-type: tm+mt
source-wordcount: '965'
ht-degree: 94%

---


# ![Badge Premium](/help/assets/premium.png) Gestire le esclusioni

Gestire le esclusioni creando gruppi di esclusione, escludendo le offerte duplicate, escludendo esperienze specifiche ed escludendo il contenuto predefinito nelle attività di [!UICONTROL  Automated Personalization] (AP) in [!DNL Adobe Target] [!UICONTROL  Automated Personalization] (AP).

## Creare gruppi di esclusione {#task_AAAA6C7239A84F7696C8492F04B575A2}

Crea dei gruppi di esclusione nelle attività di Personalizzazione automatizzata per escludere automaticamente esperienze con specifiche offerte.

I gruppi di esclusione sono un ottimo modo per garantire che le offerte incompatibili non siano presentate nella stessa esperienza in percorsi diversi. Ad esempio, supponiamo di avere due offerte: una è per il 20% di sconto di tutte le merci e l&#39;altro è per il 15% di sconto. Non vorresti mai che queste due offerte fossero presentate ai visitatori nella stessa esperienza. Se si aggiungono queste due offerte a un gruppo di esclusione, è possibile assicurarsi che questo non sarà mai il caso.

Puoi anche limitare quali tipi di pubblico possono vedere offerte specifiche nelle attività di Personalizzazione automatizzata. Per ulteriori informazioni, consulta [Targeting delle offerte di Personalizzazione automatizzata](/help/c-activities/t-automated-personalization/ap-target-offers.md).

**Per creare un gruppo di esclusione:**

1. Durante la [creazione o la modifica di un’attività di Personalizzazione automatizzata](/help/c-activities/t-automated-personalization/create-ap-activity.md), fai clic su **[!UICONTROL Gestione contenuto]** nella barra dell’intestazione.

   ![Collegamento Gestione contenuto](/help/c-activities/t-automated-personalization/assets/manage-content.png)

1. Nella finestra di dialogo [!UICONTROL Gestione contenuto] fai clic su **[!UICONTROL Gruppi di esclusione]**.

   ![Finestra di dialogo Gestione contenuto > Gruppi di esclusione](/help/c-activities/t-automated-personalization/assets/exclusion_group_create-new.png)

   Se sono stati precedentemente creati gruppi di esclusione, questi vengono visualizzati nell&#39;elenco. Se non è stato ancora creato un gruppo di esclusione, viene richiesto di crearne uno.

1. Fai clic su **[!UICONTROL Crea gruppo di esclusione.]**

   ![Finestra di dialogo Crea gruppo di esclusione](/help/c-activities/t-automated-personalization/assets/exclusion_group_create_dialog-new.png)

1. (Obbligatorio) Specifica un nome descrittivo per il gruppo di esclusione.

   Un nome descrittivo aiuta te od altri ad individuare rapidamente e capire lo scopo di un gruppo.

1. Individua e seleziona le offerte desiderate da aggiungere al gruppo di esclusione.

   È possibile selezionare più offerte dalla stessa posizione in un gruppo di esclusione.

1. Fai clic su **[!UICONTROL Salva]**.

Le offerte del gruppo di esclusione saranno escluse in maniera automatizzata dalle stesse esperienze in corso.

## Escludere le offerte duplicate {#concept_4EF78013F80E48EFA024AE0274C9F037}

Evita che le offerte della libreria vengano duplicate quando sono utilizzate in posizioni diverse nelle attività di [!UICONTROL Personalizzazione automatizzata].

Si potrebbe avere un&#39;attività, ad esempio, con sei percorsi in una pagina con 12 offerte. Esiste la possibilità che la stessa offerta possa essere collocata in uno o più percorsi nell&#39;attività. Questa funzionalità impedisce la visualizzazione di offerte duplicate contemporaneamente in percorsi diversi all&#39;interno della stessa attività.

Clicca su **[!UICONTROL Configura]** > **[!UICONTROL Offerte duplicate]**, quindi clicca su **[!UICONTROL Consenti duplicati]** o **[!UICONTROL Non consentire duplicati]**.

![Opzioni Offerte duplicate](/help/c-activities/t-automated-personalization/assets/duplicate_offers-new.png)

## Escludere esperienze specifiche {#task_C17D36EF58AF4908B17A3D84CA6DE85A}

Escludi specifiche esperienze se desideri escludere dall’attività di Personalizzazione automatizzata determinate combinazioni di offerte.

Ci potrebbero essere alcune combinazioni che non funzionano bene insieme, o si potrebbe limitare il numero di esperienze testate per ridurre i requisiti di traffico per l&#39;attività.

1. Durante la [creazione o la modifica di un’attività di Personalizzazione automatizzata](/help/c-activities/t-automated-personalization/create-ap-activity.md), fai clic su **Gestione contenuto** nella barra dell’intestazione.

   ![Collegamento Gestione contenuto](/help/c-activities/t-automated-personalization/assets/manage-content.png)

   L&#39;elenco [!UICONTROL Esperienze] mostra ogni esperienza generata dalle permutazioni di tutte le opzioni di contenuto e percorso.

1. Escludi le esperienze, se lo desideri.

   Per escludere esperienze specifiche, passa il cursore sopra l’esperienza desiderata e fai clic sull’icona Escludi.

   ![Opzione Escludi esperienza visibile al passaggio del mouse](/help/c-activities/t-automated-personalization/assets/exclude_exp_1a.png)

   Oppure, per escludere e includere esperienze in blocco, seleziona la casella di controllo per le esperienze rilevanti e fai clic su **[!UICONTROL Escludi]** in alto a destra nella finestra di dialogo. Quando si selezionano una o più esperienze, viene visualizzata l’icona [!UICONTROL Escludi].

   ![Esclusione di più esperienze](/help/c-activities/t-automated-personalization/assets/exclude_exp_2a.png)

   Per filtrare questo elenco in modo da visualizzare solo le attività escluse o incluse, fai clic sul menu a discesa [!UICONTROL Stato].

   Le esperienze saranno ora escluse dall&#39;attività e il loro [!UICONTROL Stato] appare come [!UICONTROL Escluso].

   ![Esperienze escluse](/help/c-activities/t-automated-personalization/assets/exclude_exp_3a.png)

## Escludere il contenuto predefinito {#task_DCB4528989DF4C05A3A4729E5891D18F}

In alcuni casi, potrebbe non essere necessario includere il contenuto predefinito come parte dell’attività di Personalizzazione automatizzata. La modalità di accesso a questa impostazione è diversa dalla creazione dei gruppi di esclusione. Puoi utilizzare questo metodo per avere una sola offerta (diversa dal contenuto predefinito) in una posizione come parte dell’attività di personalizzazione automatizzata.

L’esclusione del contenuto predefinito è molto utile per cambiare l’aspetto del resto della pagina a seconda delle offerte da testare con l’attività di personalizzazione automatizzata. Ad esempio, si supponga di voler corrispondere alla tavolozza dei colori delle offerte che si stanno testando, di modificare il colore di sfondo della pagina ed escludere il colore di sfondo predefinito.

**Per escludere il contenuto predefinito utilizzando il Compositore di esperienza visiva:**

1. Durante la creazione o la modifica di un&#39;attività AP](/help/c-activities/t-automated-personalization/create-ap-activity.md), selezionare il contenuto da sostituire e fare clic per accedere a **[!UICONTROL Change Text/HTML]**, **[!UICONTROL Change Image]** o **[!UICONTROL Change Background Color]**.[
1. Nella finestra di dialogo, crea il nuovo contenuto e deseleziona **Includi** a destra del contenuto predefinito (oppure deseleziona Immagine/video predefinito nella schermata Seleziona contenuto).

   A seconda del tipo di contenuto/offerta, la casella di controllo [!UICONTROL Includi] è in un percorso leggermente diverso.

   Per contenuto testo/HTML:

   ![Casella di controllo Includi nella finestra di dialogo Modifica testo/HTML](/help/c-activities/t-automated-personalization/assets/exclude_content_vec_1a.png)

   Per contenuto immagine/video:

   ![Casella di controllo Includi nella finestra di dialogo Seleziona contenuto](/help/c-activities/t-automated-personalization/assets/exclude_content_vec_2a.png)

   Per colore dello sfondo:

   ![Casella di controllo Includi nella finestra di dialogo Modifica colore di sfondo](/help/c-activities/t-automated-personalization/assets/exclude_content_vec_3a.png)

1. Fai clic su **[!UICONTROL Salva]**.

   È possibile visualizzare le esperienze create dalle offerte specificate in [!UICONTROL Gestione contenuto]. Noterai che non vengono create esperienze in [!UICONTROL Gestione contenuto] utilizzando l&#39;offerta predefinita esclusa.

   ![](assets/exclude_content_vec_4.png)

**Per escludere il contenuto predefinito utilizzando il Compositore esperienza basato su moduli:**

1. Durante la creazione o la modifica di un’attività di Personalizzazione automatizzata, clicca su **[!UICONTROL Modifica testo/HTML]** o **[!UICONTROL Modifica offerta immagine]** in **[!UICONTROL Contenuto]**.
1. Nella finestra di dialogo, crea il nuovo contenuto e deseleziona **[!UICONTROL Includi]** a destra del contenuto predefinito (oppure deseleziona Immagine/video predefinito nella schermata Seleziona contenuto).

   A seconda del tipo di contenuto od offerta, la casella di controllo Includi sarà in un luogo leggermente diverso.

   Per contenuto testo/HTML:

   ![](assets/exclude_content_form_1.png)

   Per contenuto immagine/video:

   ![](assets/exclude_content_form_2.png)

1. Fai clic su **[!UICONTROL Salva]**.

   È possibile visualizzare le esperienze create dalle offerte specificate in [!UICONTROL Gestione contenuto]. Noterai che non vengono create esperienze in [!UICONTROL Gestione contenuto] utilizzando l&#39;offerta predefinita esclusa.

   ![](assets/exclude_content_form_3.png)
