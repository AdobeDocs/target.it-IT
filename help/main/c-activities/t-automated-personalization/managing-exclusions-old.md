---
keywords: deduplicare;consentire duplicati;escludere offerte duplicate;personalizzazione automatizzata;non consentire offerte duplicate;escludere;contenuto predefinito;gruppo di esclusione;
description: Gestisci esclusioni nelle attività di  [!DNL Adobe Target] [!UICONTROL Automated Personalization] (AP). Crea gruppi di esclusione ed escludi le offerte duplicate, esperienze specifiche e contenuti predefiniti.
title: Come posso gestire le esclusioni nelle attività [!UICONTROL Automated Personalization]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Automated Personalization
solution: Target,Analytics
exl-id: d9e9f2a2-5914-4b81-acae-eaf388646652
source-git-commit: 3a44c05bea24c622292dd0b774f88f0c93be1d88
workflow-type: tm+mt
source-wordcount: '922'
ht-degree: 41%

---

# Gestire le esclusioni

Gestisci le esclusioni creando gruppi di esclusione ed escludendo le offerte duplicate, esperienze specifiche e contenuti predefiniti nelle attività di [!UICONTROL Automated Personalization] (AP) in [!DNL Adobe Target].

## Creare gruppi di esclusione {#task_AAAA6C7239A84F7696C8492F04B575A2}

Crea gruppi di esclusione nelle attività di [!UICONTROL Automated Personalization] (AP) per garantire che le esperienze con le offerte designate siano escluse automaticamente.

I gruppi di esclusione sono un ottimo modo per garantire che le offerte incompatibili non siano presentate nella stessa esperienza in percorsi diversi. Ad esempio, supponiamo di avere due offerte: una è per uno sconto del 20% per tutte le merci e l’altra è per uno sconto del 15%. Non vorrai mai che queste due offerte vengano presentate ai visitatori nella stessa esperienza. Se aggiungi queste due offerte a un gruppo di esclusione, puoi assicurarti che questa situazione non si verifichi mai.

Puoi anche limitare quali tipi di pubblico possono vedere offerte specifiche nelle attività di Personalizzazione automatizzata. Per ulteriori informazioni, consulta [Targeting delle offerte di Personalizzazione automatizzata](/help/main/c-activities/t-automated-personalization/ap-target-offers.md).

**Per creare un gruppo di esclusione:**

1. Durante la [creazione o modifica di un&#39;attività di Personalizzazione automatizzata](/help/main/c-activities/t-automated-personalization/create-ap-activity.md), fare clic su **[!UICONTROL Manage Content]** nella barra dell&#39;intestazione.

   ![Collegamento Gestione contenuto](/help/main/c-activities/t-automated-personalization/assets/manage-content.png)

1. Nella finestra di dialogo [!UICONTROL Manage Content] fare clic su **[!UICONTROL Exclusion Groups]**.

   ![Finestra di dialogo Gestione contenuto > Gruppi di esclusione](/help/main/c-activities/t-automated-personalization/assets/exclusion_group_create-new.png)

   Se sono stati precedentemente creati gruppi di esclusione, questi vengono visualizzati nell&#39;elenco. Se non è stato ancora creato un gruppo di esclusione, viene richiesto di crearne uno.

1. Fai clic su **[!UICONTROL Create Exclusion Group.]**

   ![Finestra di dialogo Crea gruppo di esclusione](/help/main/c-activities/t-automated-personalization/assets/exclusion_group_create_dialog-new.png)

1. (Obbligatorio) Specifica un nome descrittivo per il gruppo di esclusione.

   Un nome descrittivo aiuta te od altri ad individuare rapidamente e capire lo scopo di un gruppo.

1. Individua e seleziona le offerte desiderate da aggiungere al gruppo di esclusione.

   È possibile selezionare più offerte dalla stessa posizione in un gruppo di esclusione.

1. Fare clic su **[!UICONTROL Save]**.

Le offerte del gruppo di esclusione vengono escluse automaticamente dalle stesse esperienze in corso.

## Escludere le offerte duplicate {#concept_4EF78013F80E48EFA024AE0274C9F037}

Impedisci la duplicazione delle offerte della libreria di offerte quando vengono utilizzate in posizioni diverse nelle attività [!UICONTROL Automated Personalization].

Si potrebbe avere un&#39;attività, ad esempio, con sei percorsi in una pagina con 12 offerte. Esiste la possibilità che la stessa offerta possa essere collocata in uno o più percorsi nell&#39;attività. Questa funzionalità impedisce la visualizzazione di offerte duplicate contemporaneamente in percorsi diversi all&#39;interno della stessa attività.

Fai clic sull&#39;opzione ingranaggio **[!UICONTROL Configure]** > **[!UICONTROL Duplicate Offers]**, quindi fai clic su **[!UICONTROL Allow Duplicates]** o **[!UICONTROL Disallow Duplicates]**.

![Opzioni Offerte duplicate](/help/main/c-activities/t-automated-personalization/assets/duplicate_offers-new.png)

## Escludere esperienze specifiche {#task_C17D36EF58AF4908B17A3D84CA6DE85A}

Escludere esperienze specifiche se si desidera escludere determinate combinazioni di offerte dall&#39;attività [!UICONTROL Automated Personalization].

Potrebbero esserci alcune combinazioni che non funzionano insieme, oppure potresti limitare il numero di esperienze testate per ridurre i requisiti di traffico per l&#39;attività.

1. Durante la [creazione o la modifica di un’attività di Personalizzazione automatizzata](/help/main/c-activities/t-automated-personalization/create-ap-activity.md), fai clic su **Gestione contenuto** nella barra dell’intestazione.

   ![Collegamento Gestione contenuto](/help/main/c-activities/t-automated-personalization/assets/manage-content.png)

   L&#39;elenco [!UICONTROL Experiences] mostra ogni esperienza generata dalle permutazioni di tutte le opzioni di contenuto e percorso.

1. Escludi le esperienze, se lo desideri.

   Per escludere esperienze specifiche, passa il cursore sopra l’esperienza desiderata e fai clic sull’icona Escludi.

   ![Opzione Escludi esperienza visibile al passaggio del mouse](/help/main/c-activities/t-automated-personalization/assets/exclude_exp_1a.png)

   Oppure è possibile escludere esperienze in blocco selezionando la casella di spunta per le esperienze rilevanti e quindi facendo clic sull&#39;icona **[!UICONTROL Exclude]** nell&#39;angolo in alto a destra della finestra di dialogo. L&#39;icona [!UICONTROL Exclude] viene visualizzata quando si verificano una o più esperienze.

   ![Esclusione di più esperienze](/help/main/c-activities/t-automated-personalization/assets/exclude_exp_2a.png)

   Per filtrare questo elenco in modo da visualizzare solo le attività escluse o incluse, fare clic sull&#39;elenco a discesa [!UICONTROL Status].

   Le esperienze sono ora escluse dall&#39;attività e i relativi [!UICONTROL Status] vengono visualizzati come [!UICONTROL Excluded].

   ![Esperienze escluse](/help/main/c-activities/t-automated-personalization/assets/exclude_exp_3a.png)

## Escludi contenuto predefinito {#task_DCB4528989DF4C05A3A4729E5891D18F}

Talvolta potrebbe non essere necessario includere il contenuto predefinito come parte dell&#39;attività [!UICONTROL Automated Personalization]. La modalità di accesso a questa impostazione è diversa dalla creazione dei gruppi di esclusione. Puoi utilizzare questo metodo per avere una sola offerta (diversa dal contenuto predefinito) in una posizione come parte dell’attività di personalizzazione automatizzata.

L’esclusione del contenuto predefinito è molto utile per cambiare l’aspetto del resto della pagina a seconda delle offerte da testare con l’attività di personalizzazione automatizzata. Ad esempio, si supponga di voler corrispondere alla tavolozza dei colori delle offerte che si stanno testando, di modificare il colore di sfondo della pagina ed escludere il colore di sfondo predefinito.

**Per escludere il contenuto predefinito utilizzando [!UICONTROL Visual Experience Composer] (VEC):**

1. Durante la [creazione o modifica di un&#39;attività di Personalizzazione automatizzata](/help/main/c-activities/t-automated-personalization/create-ap-activity.md), selezionare il contenuto da sostituire e fare clic per accedere a **[!UICONTROL Change Text/HTML]**, **[!UICONTROL Change Image]** o **[!UICONTROL Change Background Color]**.
1. Nella finestra di dialogo, crea il nuovo contenuto e deseleziona **Includi** a destra del contenuto predefinito (oppure deseleziona Immagine/video predefinito nella schermata [!UICONTROL Select Content]).

   A seconda del tipo di contenuto o di offerta, la casella di controllo [!UICONTROL Include] si trova in una posizione leggermente diversa.

   Per contenuto testo/HTML:

   ![Casella di controllo Includi nella finestra di dialogo Modifica testo/HTML](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_1a.png)

   Per contenuto immagine/video:

   ![Casella di controllo Includi nella finestra di dialogo Seleziona contenuto](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_2a.png)

   Per colore dello sfondo:

   ![Casella di controllo Includi nella finestra di dialogo Modifica colore di sfondo](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_3a.png)

1. Fare clic su **[!UICONTROL Save]**.

   Puoi vedere le esperienze create dalle offerte specificate in [!UICONTROL Manage Content]. Si nota che non viene creata alcuna esperienza in [!UICONTROL Manage Content] utilizzando l&#39;offerta predefinita che è stata esclusa.

   ![escludi_contenuto_vec_4 immagine](assets/exclude_content_vec_4.png)

**Per escludere il contenuto predefinito utilizzando [!UICONTROL Form-Based Experience Composer]:**

1. Durante la creazione o la modifica di un&#39;attività di Personalizzazione automatizzata, fare clic su **[!UICONTROL Change Text/HTML]** o **[!UICONTROL Change Image Offer]** in **[!UICONTROL Content]**.
1. Nella finestra di dialogo, crea il nuovo contenuto e deseleziona **[!UICONTROL Include]** a destra del contenuto predefinito (o deseleziona Immagine/video predefinito nella schermata [!UICONTROL Select Content]).

   A seconda del tipo di contenuto o di offerta, la casella di controllo [!UICONTROL Include] si trova in una posizione leggermente diversa.

   Per contenuto testo/HTML:

   ![escludi_contenuto_modulo_1 immagine](assets/exclude_content_form_1.png)

   Per contenuto immagine/video:

   ![escludi_contenuto_modulo_2 immagine](assets/exclude_content_form_2.png)

1. Fare clic su **[!UICONTROL Save]**.

   Puoi vedere le esperienze create dalle offerte specificate in [!UICONTROL Manage Content]. Si nota che non viene creata alcuna esperienza in [!UICONTROL Manage Content] utilizzando l&#39;offerta predefinita che è stata esclusa.

   ![escludi_contenuto_modulo_3 immagine](assets/exclude_content_form_3.png)
