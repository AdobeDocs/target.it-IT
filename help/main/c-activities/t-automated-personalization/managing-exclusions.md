---
keywords: deduplicare;consentire duplicati;escludere offerte duplicate;personalizzazione automatizzata;non consentire offerte duplicate;escludere;contenuto predefinito;
description: Gestire le esclusioni nelle attività di [!UICONTROL Automated Personalization] (AP).
title: Come posso gestire le esclusioni nelle attività [!UICONTROL Automated Personalization]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Automated Personalization
solution: Target,Analytics
exl-id: d9e9f2a2-5914-4b81-acae-eaf388646652
source-git-commit: e620cd189e2783ba3abbe93bb9c5000866c41b99
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 28%

---

# Gestire le esclusioni

Gestisci le esclusioni escludendo le offerte duplicate, esperienze specifiche e contenuti predefiniti nelle attività [!UICONTROL Automated Personalization] (AP) in [!DNL Adobe Target].

## Consentire o non consentire le offerte duplicate {#concept_4EF78013F80E48EFA024AE0274C9F037}

Impedisci la duplicazione delle offerte della libreria di offerte quando vengono utilizzate in posizioni diverse nelle attività [!UICONTROL Automated Personalization].

Si potrebbe avere un&#39;attività, ad esempio, con sei percorsi in una pagina con 12 offerte. Esiste la possibilità che la stessa offerta possa essere collocata in uno o più percorsi nell&#39;attività. Questa funzione consente di impedire la visualizzazione simultanea di offerte duplicate in posizioni diverse all’interno della stessa attività.

1. Durante la [creazione o modifica di un&#39;attività di Personalizzazione automatizzata](/help/main/c-activities/t-automated-personalization/create-ap-activity.md), fare clic sull&#39;icona **[!UICONTROL Configure]** ( ![icona Configura](/help/main/assets/icons/Setting.svg) ) > fare clic su **[!UICONTROL Allow Duplicate Offers]** per attivare e disattivare questa funzione, a seconda delle esigenze.

## Escludere esperienze specifiche {#task_C17D36EF58AF4908B17A3D84CA6DE85A}

Escludere esperienze specifiche se si desidera escludere determinate combinazioni di offerte dall&#39;attività [!UICONTROL Automated Personalization].

Potrebbero esserci alcune combinazioni che non funzionano insieme, oppure potresti limitare il numero di esperienze testate per ridurre i requisiti di traffico per l&#39;attività.

1. Durante la [creazione o modifica di un&#39;attività di Personalizzazione automatizzata](/help/main/c-activities/t-automated-personalization/create-ap-activity.md), fare clic sull&#39;icona **Gestione contenuto** ( ![Icona Gestione contenuto](/help/main/assets/icons/Experience.svg) ).

   L&#39;elenco [!UICONTROL Experiences] mostra ogni esperienza generata dalle permutazioni di tutte le opzioni di contenuto e percorso.

1. Escludi le esperienze, se lo desideri.

   Per escludere esperienze specifiche, fai clic sull&#39;icona [!UICONTROL **Altre azioni**] ( ![Altre azioni](/help/main/assets/icons/MoreSmall.svg) ), quindi fai clic su [!UICONTROL **Escludi**].

   Oppure è possibile escludere esperienze in blocco selezionando la casella di spunta per le esperienze rilevanti e quindi facendo clic su **[!UICONTROL Exclude]**. L&#39;icona [!UICONTROL Exclude] viene visualizzata quando si verificano una o più esperienze.

   ![Esclusione di più esperienze](/help/main/c-activities/t-automated-personalization/assets/exclude1.png)

   Le esperienze sono ora escluse dall&#39;attività e i relativi [!UICONTROL Status] vengono visualizzati come [!UICONTROL Excluded].

## Escludi contenuto predefinito {#task_DCB4528989DF4C05A3A4729E5891D18F}

Talvolta potrebbe non essere necessario includere il contenuto predefinito come parte dell&#39;attività [!UICONTROL Automated Personalization]. Puoi utilizzare questo metodo per avere una sola offerta (diversa dal contenuto predefinito) in una posizione come parte dell’attività di personalizzazione automatizzata.

L’esclusione del contenuto predefinito è molto utile per cambiare l’aspetto del resto della pagina a seconda delle offerte da testare con l’attività di personalizzazione automatizzata. Ad esempio, si supponga di voler corrispondere alla tavolozza dei colori delle offerte che si stanno testando, di modificare il colore di sfondo della pagina ed escludere il colore di sfondo predefinito.

**Per escludere il contenuto predefinito utilizzando [!UICONTROL Visual Experience Composer] (VEC):**

1. Durante la [creazione o modifica di un&#39;attività di Personalizzazione automatizzata](/help/main/c-activities/t-automated-personalization/create-ap-activity.md), selezionare il contenuto da sostituire e fare clic per accedere a **[!UICONTROL Change Text/HTML]**, **[!UICONTROL Change Image Offer]** o **[!UICONTROL Change Background Color]**. Le opzioni disponibili variano a seconda del tipo di contenuto.

   ![Modifica opzioni](/help/main/c-activities/t-automated-personalization/assets/options.png)

1. Crea il nuovo contenuto e deseleziona **Includi** a destra del contenuto predefinito (o deseleziona Immagine/video predefinito nella schermata [!UICONTROL Select Content]).

   <!-- Depending on the content or offer type, the [!UICONTROL Include] checkbox is in a slightly different place. 

   For Text/HTML content: 

   ![Include checkbox in Edit Text/HTML dialog box](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_1a.png)

   For Image/Video content: 

   ![Include checkbox in Select Content dialog box](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_2a.png)

   For background color: 

   ![Include checkbox in Edit Background Color dialog box](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_3a.png)-->

<!-- 1. Click **[!UICONTROL Save]**.

   You can see the experiences created from the offers you specified under [!UICONTROL Manage Content]. You notice that no experiences are created in [!UICONTROL Manage Content] using the default offer you excluded. 

   ![exclude_content_vec_4 image](assets/exclude_content_vec_4.png)

**To exclude default content using the [!UICONTROL Form-Based Experience Composer]:** 

1. While creating or editing an AP activity, click **[!UICONTROL Change Text/HTML]** or **[!UICONTROL Change Image Offer]** under **[!UICONTROL Content]**. 
1. In the dialog box, create your new content and uncheck **[!UICONTROL Include]** to the right of the default content (or uncheck the Default Image/Video in the [!UICONTROL Select Content] screen). 

   Depending on the content or offer type, the [!UICONTROL Include] checkbox is in a slightly different place. 

   For Text/HTML content: 

   ![exclude_content_form_1 image](assets/exclude_content_form_1.png)

   For Image/Video content: 

   ![exclude_content_form_2 image](assets/exclude_content_form_2.png)

1. Click **[!UICONTROL Save]**. 

   You can see the experiences created from the offers you specified under [!UICONTROL Manage Content]. You notice that no experiences are created in [!UICONTROL Manage Content] using the default offer you excluded. 

   ![exclude_content_form_3 image](assets/exclude_content_form_3.png)-->
