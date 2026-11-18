---
keywords: deduplicare;consentire duplicati;escludere offerte duplicate;personalizzazione automatizzata;non consentire offerte duplicate;escludere;contenuto predefinito;
description: Gestire le esclusioni nelle attività di [!UICONTROL Automated Personalization] (AP).
title: Come posso gestire le esclusioni nelle [!UICONTROL attività Automated Personalization]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Automated Personalization
solution: Target,Analytics
exl-id: d9e9f2a2-5914-4b81-acae-eaf388646652
TQID: 'https://experienceleague.adobe.com/ERpNwQPsIRBmU0vTZbGa-lYg30BYl-uJxA8UT0f6060'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: f0055dd2-93f3-4ac8-9abc-d69d4ed2d977
    internal-label: Automated personalization
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 44c6bdd4ab818226e76477782d7e4238b49d5cdc
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 4%
---
# Gestire le esclusioni {#manage-exclusions}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come evitare le offerte duplicate, escludere esperienze specifiche ed escludere il contenuto predefinito nelle **[!UICONTROL attività Automated Personalization]**.

>[!ENDSHADEBOX]

Le esclusioni controllano quali offerte ed esperienze vengono servite da un&#39;attività di **[!UICONTROL Automated Personalization]** (AP). Impediscono che la stessa offerta venga visualizzata due volte, rimuovono combinazioni di offerte che non funzionano insieme e rimuovono il contenuto predefinito, in modo che l’attività fornisca esperienze più pulite e rilevanti in linea con i tuoi obiettivi e il tuo pubblico.

## Consentire o non consentire le offerte duplicate {#allow-duplicate-offers}

<a id="concept_4EF78013F80E48EFA024AE0274C9F037"></a>

Impedisci la duplicazione delle offerte della libreria di offerte quando vengono utilizzate in posizioni diverse nelle attività di Personalizzazione automatizzata.

Un’attività può avere, ad esempio, sei posizioni in una pagina con 12 offerte, pertanto la stessa offerta può essere posizionata in più posizioni. La disattivazione delle offerte duplicate impedisce la visualizzazione della stessa offerta contemporaneamente in posizioni diverse all’interno della stessa attività.

1. Durante la [creazione o modifica di un&#39;attività di Personalizzazione automatizzata](/help/main/c-activities/t-automated-personalization/create-ap-activity.md#create-ap-activity), fare clic sull&#39;icona **[!UICONTROL Configura]** ( ![icona Configura](/help/main/assets/icons/Setting.svg) ).

1. Fai clic su **[!UICONTROL Consenti offerte duplicate]** per attivare o disattivare questa funzione, a seconda delle tue esigenze.

   ![Icona Configura](../assets/exclusion-1.png)

## Escludere esperienze specifiche {#exclude-experiences}

<a id="task_C17D36EF58AF4908B17A3D84CA6DE85A"></a>

Escludi esperienze specifiche per rimuovere determinate combinazioni di offerte dall’attività di Personalizzazione automatizzata. Alcune combinazioni potrebbero non funzionare insieme oppure potresti limitare il numero di esperienze testate per ridurre i requisiti di traffico dell’attività.

1. Durante la [creazione o modifica di un&#39;attività di Personalizzazione automatizzata](/help/main/c-activities/t-automated-personalization/create-ap-activity.md#create-ap-activity), fare clic sull&#39;icona **[!UICONTROL Gestione contenuto]** ( ![Icona Gestione contenuto](/help/main/assets/icons/Experience.svg) ).

   L&#39;elenco **[!UICONTROL Esperienze]** mostra ogni esperienza generata dalle permutazioni di tutte le opzioni di contenuto e percorso.

1. Escludi le esperienze che non desideri testare.

   * Per escludere una singola esperienza, fai clic sull&#39;icona **[!UICONTROL Altre azioni]** ( ![Altre azioni](/help/main/assets/icons/MoreSmall.svg) ), quindi fai clic su **[!UICONTROL Escludi]**.
   * Per escludere più esperienze contemporaneamente, seleziona la casella di controllo di ogni esperienza, quindi fai clic su **[!UICONTROL Escludi]**. Quando si selezionano una o più esperienze, viene visualizzata l&#39;icona **[!UICONTROL Escludi]**.

   ![Esclusione di più esperienze](/help/main/c-activities/t-automated-personalization/assets/exclude1.png)

   Le esperienze sono ora escluse dall&#39;attività e il loro **[!UICONTROL Stato]** viene visualizzato come **[!UICONTROL Escluso]**.

## Escludi contenuto predefinito {#exclude-default-content}

<a id="task_DCB4528989DF4C05A3A4729E5891D18F"></a>

Escludi il contenuto predefinito quando non desideri che faccia parte dell&#39;attività di Personalizzazione automatizzata, in modo che una posizione contenga solo un&#39;offerta diversa dal contenuto predefinito. Questo approccio consente inoltre di modificare l’aspetto del resto della pagina in base alle offerte sottoposte a test. Ad esempio, per far corrispondere la palette di colori delle offerte, puoi modificare il colore di sfondo della pagina ed escludere il colore di sfondo predefinito.

1. Durante la [creazione o modifica di un&#39;attività di Personalizzazione automatizzata](/help/main/c-activities/t-automated-personalization/create-ap-activity.md#create-ap-activity), selezionare il contenuto da sostituire, quindi fare clic su **[!UICONTROL Cambia testo/HTML]**, **[!UICONTROL Cambia offerta immagine]** o **[!UICONTROL Cambia colore di sfondo]**. Le opzioni disponibili variano a seconda del tipo di contenuto.

   ![Modifica opzioni](../assets/exclusion-1.png)

1. Crea il nuovo contenuto.

1. Fai clic sull&#39;icona **[!UICONTROL Altre azioni]** ( ![Altre azioni](/help/main/assets/icons/Setting.svg) ), quindi fai clic sull&#39;interruttore **Escludi offerta predefinita/Includi offerta predefinita** per escludere o includere l&#39;offerta predefinita.

   <!--
   Depending on the content or offer type, the [!UICONTROL Include] checkbox is in a slightly different place. 

   For Text/HTML content: 

   ![Include checkbox in Edit Text/HTML dialog box](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_1a.png)

   For Image/Video content: 

   ![Include checkbox in Select Content dialog box](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_2a.png)

   For background color: 

   ![Include checkbox in Edit Background Color dialog box](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_3a.png)
   -->

<!--
1. Click **[!UICONTROL Save]**.

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

   ![exclude_content_form_3 image](assets/exclude_content_form_3.png)
-->
