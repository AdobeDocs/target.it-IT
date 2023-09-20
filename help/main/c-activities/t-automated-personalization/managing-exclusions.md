---
keywords: deduplicare;consentire duplicati;escludere offerte duplicate;personalizzazione automatizzata;non consentire offerte duplicate;escludere;contenuto predefinito;gruppo di esclusione;
description: Gestire le esclusioni in [!DNL Adobe Target] [!UICONTROL Automated Personalization] attività (AP). Crea gruppi di esclusione ed escludi le offerte duplicate, esperienze specifiche e contenuti predefiniti.
title: Come posso gestire le esclusioni in [!UICONTROL Automated Personalization] Attività?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Vedi cosa è incluso in Target Premium."
feature: Automated Personalization
solution: Target,Analytics
exl-id: d9e9f2a2-5914-4b81-acae-eaf388646652
source-git-commit: b5f06878a6ca8b4c571bfe05a52bfb3f471a697e
workflow-type: tm+mt
source-wordcount: '1011'
ht-degree: 58%

---

# Gestire le esclusioni

Gestisci le esclusioni creando gruppi di esclusione, escludendo le offerte duplicate, esperienze specifiche e contenuti predefiniti in [!UICONTROL Automated Personalization] Attività di (AP) in [!DNL Adobe Target].

## Creare gruppi di esclusione {#task_AAAA6C7239A84F7696C8492F04B575A2}

Creare gruppi di esclusione in [!UICONTROL Automated Personalization] attività per garantire che le esperienze con le offerte designate siano escluse automaticamente.

I gruppi di esclusione sono un ottimo modo per garantire che le offerte incompatibili non siano presentate nella stessa esperienza in percorsi diversi. Ad esempio, supponiamo di avere due offerte: una è per uno sconto del 20% per tutte le merci e l’altra è per uno sconto del 15%. Non vorrai mai che queste due offerte vengano presentate ai visitatori nella stessa esperienza. Se aggiungi queste due offerte a un gruppo di esclusione, puoi assicurarti che questa situazione non si verifichi mai.

Puoi anche limitare quali tipi di pubblico possono vedere offerte specifiche nelle attività di Personalizzazione automatizzata. Per ulteriori informazioni, consulta [Targeting delle offerte di Personalizzazione automatizzata](/help/main/c-activities/t-automated-personalization/ap-target-offers.md).

**Per creare un gruppo di esclusione:**

1. Durante la [creazione o la modifica di un’attività di Personalizzazione automatizzata](/help/main/c-activities/t-automated-personalization/create-ap-activity.md), fai clic su **[!UICONTROL Gestione contenuto]** nella barra dell’intestazione.

   ![Collegamento Gestione contenuto](/help/main/c-activities/t-automated-personalization/assets/manage-content.png)

1. In [!UICONTROL Gestione contenuto] , fare clic su **[!UICONTROL Gruppi di esclusione]**.

   ![Finestra di dialogo Gestione contenuto > Gruppi di esclusione](/help/main/c-activities/t-automated-personalization/assets/exclusion_group_create-new.png)

   Se sono stati precedentemente creati gruppi di esclusione, questi vengono visualizzati nell&#39;elenco. Se non è stato ancora creato un gruppo di esclusione, viene richiesto di crearne uno.

1. Fai clic su **[!UICONTROL Crea gruppo di esclusione.]**

   ![Finestra di dialogo Crea gruppo di esclusione](/help/main/c-activities/t-automated-personalization/assets/exclusion_group_create_dialog-new.png)

1. (Obbligatorio) Specifica un nome descrittivo per il gruppo di esclusione.

   Un nome descrittivo aiuta te od altri ad individuare rapidamente e capire lo scopo di un gruppo.

1. Individua e seleziona le offerte desiderate da aggiungere al gruppo di esclusione.

   È possibile selezionare più offerte dalla stessa posizione in un gruppo di esclusione.

1. Fai clic su **[!UICONTROL Salva]**.

Le offerte del gruppo di esclusione vengono escluse automaticamente dalle stesse esperienze in corso.

## Escludere le offerte duplicate {#concept_4EF78013F80E48EFA024AE0274C9F037}

Evita che le offerte della libreria vengano duplicate quando sono utilizzate in posizioni diverse nelle attività di [!UICONTROL Personalizzazione automatizzata].

Si potrebbe avere un&#39;attività, ad esempio, con sei percorsi in una pagina con 12 offerte. Esiste la possibilità che la stessa offerta possa essere collocata in uno o più percorsi nell&#39;attività. Questa funzionalità impedisce la visualizzazione di offerte duplicate contemporaneamente in percorsi diversi all&#39;interno della stessa attività.

Fai clic su **[!UICONTROL Configura]** opzione ingranaggio > **[!UICONTROL Offerte duplicate]**, quindi fai clic su **[!UICONTROL Consenti duplicati]** o **[!UICONTROL Non consentire duplicati]**.

![Opzioni Offerte duplicate](/help/main/c-activities/t-automated-personalization/assets/duplicate_offers-new.png)

## Escludere esperienze specifiche {#task_C17D36EF58AF4908B17A3D84CA6DE85A}

Escludi esperienze specifiche se desideri escludere determinate combinazioni di offerte dal tuo [!UICONTROL Automated Personalization] attività.

Potrebbero esserci alcune combinazioni che non funzionano insieme, oppure potresti limitare il numero di esperienze testate per ridurre i requisiti di traffico per l&#39;attività.

1. Durante la [creazione o la modifica di un’attività di Personalizzazione automatizzata](/help/main/c-activities/t-automated-personalization/create-ap-activity.md), fai clic su **Gestione contenuto** nella barra dell’intestazione.

   ![Collegamento Gestione contenuto](/help/main/c-activities/t-automated-personalization/assets/manage-content.png)

   L&#39;elenco [!UICONTROL Esperienze] mostra ogni esperienza generata dalle permutazioni di tutte le opzioni di contenuto e percorso.

1. Escludi le esperienze, se lo desideri.

   Per escludere esperienze specifiche, passa il cursore sopra l’esperienza desiderata e fai clic sull’icona Escludi.

   ![Opzione Escludi esperienza visibile al passaggio del mouse](/help/main/c-activities/t-automated-personalization/assets/exclude_exp_1a.png)

   Oppure è possibile escludere esperienze in blocco selezionando la casella di spunta per le esperienze rilevanti e quindi facendo clic su **[!UICONTROL Escludi]** nell&#39;angolo superiore destro della finestra di dialogo. Il [!UICONTROL Escludi] viene visualizzata quando si selezionano una o più esperienze.

   ![Esclusione di più esperienze](/help/main/c-activities/t-automated-personalization/assets/exclude_exp_2a.png)

   Per filtrare l’elenco in modo da visualizzare solo le attività escluse o incluse, fai clic sull’elenco a discesa [!UICONTROL Stato].

   Le esperienze sono ora escluse dall’attività e [!UICONTROL Stato] mostra come [!UICONTROL Escluso].

   ![Esperienze escluse](/help/main/c-activities/t-automated-personalization/assets/exclude_exp_3a.png)

## Escludere il contenuto predefinito {#task_DCB4528989DF4C05A3A4729E5891D18F}

Talvolta potresti non voler includere il contenuto predefinito come parte del [!UICONTROL Automated Personalization] attività. La modalità di accesso a questa impostazione è diversa dalla creazione dei gruppi di esclusione. Puoi utilizzare questo metodo per avere una sola offerta (diversa dal contenuto predefinito) in una posizione come parte dell’attività di personalizzazione automatizzata.

L’esclusione del contenuto predefinito è molto utile per cambiare l’aspetto del resto della pagina a seconda delle offerte da testare con l’attività di personalizzazione automatizzata. Ad esempio, si supponga di voler corrispondere alla tavolozza dei colori delle offerte che si stanno testando, di modificare il colore di sfondo della pagina ed escludere il colore di sfondo predefinito.

**Per escludere il contenuto predefinito utilizzando il Compositore di esperienza visiva:**

1. Mentre [creazione o modifica di un’attività di Personalizzazione automatizzata](/help/main/c-activities/t-automated-personalization/create-ap-activity.md), seleziona il contenuto che desideri sostituire e fai clic per accedere **[!UICONTROL Cambia testo/HTML]**, **[!UICONTROL Cambia immagine]**, o **[!UICONTROL Cambia colore di sfondo]**.
1. Nella finestra di dialogo, crea il nuovo contenuto e deseleziona **Includi** a destra del contenuto predefinito (oppure deseleziona Immagine/video predefinito nella schermata Seleziona contenuto).

   A seconda del tipo di contenuto o di offerta, il [!UICONTROL Includi] la casella di controllo si trova in una posizione leggermente diversa.

   Per contenuto testo/HTML:

   ![Casella di controllo Includi nella finestra di dialogo Modifica testo/HTML](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_1a.png)

   Per contenuto immagine/video:

   ![Casella di controllo Includi nella finestra di dialogo Seleziona contenuto](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_2a.png)

   Per colore dello sfondo:

   ![Casella di controllo Includi nella finestra di dialogo Modifica colore di sfondo](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_3a.png)

1. Fai clic su **[!UICONTROL Salva]**.

   È possibile visualizzare le esperienze create dalle offerte specificate in [!UICONTROL Gestione contenuto]. Non viene creata alcuna esperienza in [!UICONTROL Gestione contenuto] utilizzando l’offerta predefinita che hai escluso.

   ![immagine exclude_content_vec_4](assets/exclude_content_vec_4.png)

**[!UICONTROL Per escludere il contenuto predefinito utilizzando il Compositore esperienza basato su moduli]:**

1. Durante la creazione o la modifica di un’attività di Personalizzazione automatizzata, clicca su **[!UICONTROL Modifica testo/HTML]** o **[!UICONTROL Modifica offerta immagine]** in **[!UICONTROL Contenuto]**.
1. Nella finestra di dialogo, crea il nuovo contenuto e deseleziona **[!UICONTROL Includi]** a destra del contenuto predefinito (oppure deseleziona Immagine/video predefinito nella schermata Seleziona contenuto).

   A seconda del tipo di contenuto o di offerta, il [!UICONTROL Includi] la casella di controllo si trova in una posizione leggermente diversa.

   Per contenuto testo/HTML:

   ![immagine exclude_content_form_1](assets/exclude_content_form_1.png)

   Per contenuto immagine/video:

   ![immagine exclude_content_form_2](assets/exclude_content_form_2.png)

1. Fai clic su **[!UICONTROL Salva]**.

   È possibile visualizzare le esperienze create dalle offerte specificate in [!UICONTROL Gestione contenuto]. Non viene creata alcuna esperienza in [!UICONTROL Gestione contenuto] utilizzando l’offerta predefinita che hai escluso.

   ![immagine exclude_content_form_3](assets/exclude_content_form_3.png)
