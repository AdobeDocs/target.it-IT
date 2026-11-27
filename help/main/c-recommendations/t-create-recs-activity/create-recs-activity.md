---
keywords: creare consigli;attività consigli;nuovi consigli;panoramica consigli
description: Scopri come utilizzare il [!DNL Target] [!UICONTROL Compositore esperienza visivo] (VEC) per creare un'attività [!DNL Recommendations].
title: Crea un'attività [!DNL Recommendations]
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
exl-id: c83073d5-f852-4f09-8343-e4658fbf6f43
TQID: 'https://experienceleague.adobe.com/rb9any1dsbk-E-ELV56A2D6X5f0z0cTziscrajmbYDA'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '1169'
ht-degree: 3%
---
# Crea un&#39;attività [!DNL Recommendations] {#create-recs-activity}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come creare un&#39;attività [!DNL Recommendations] nel [!DNL Target] **[!UICONTROL Compositore esperienza visivo]** (VEC), dalla selezione del percorso alla configurazione dell&#39;attività.

>[!ENDSHADEBOX]

Un&#39;attività [!DNL Recommendations] visualizza gli elementi consigliati in una pagina. La creazione dell&#39;attività nel [!DNL Target] **[!UICONTROL Compositore esperienza visivo]** consente di inserire i consigli direttamente in una pagina abilitata per [!DNL Target], nel percorso esatto in cui i visitatori dovrebbero visualizzarli.

## Crea l’attività e seleziona la posizione {#create-activity}

L’URL attività e la posizione definiscono la pagina e l’area della pagina in cui vengono visualizzati i consigli.

1. Dal menu **[!UICONTROL Attività]**, fai clic su **[!UICONTROL Crea attività]** > **[!UICONTROL Consigli]**.

   ![Pagina Tutte le attività con il menu Crea attività aperto e l&#39;opzione Consigli evidenziata](../assets/create_reco_1.png)

1. Selezionare **[!UICONTROL Visual]**, se necessario.

   Per utilizzare il **[!UICONTROL Compositore esperienza basato su moduli]**, selezionare **[!UICONTROL Modulo]**. Vedi [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md). Per un confronto tra i compositori, incluso il Compositore esperienza visivo **[!UICONTROL Applicazione a pagina singola]**, vedi [Esperienze e offerte](/help/main/c-experiences/experiences.md). Per i problemi relativi al Compositore esperienza visivo, vedi [Risoluzione dei problemi relativi al Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Condizionale) Scegli un&#39;[area di lavoro](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. Specifica l&#39;URL attività, quindi fai clic su **[!UICONTROL Crea]**.

   L’URL attività è la pagina in cui vengono visualizzati i consigli. [!DNL Target] non distingue tra protocolli URL ([!DNL https] e [!DNL http]), quindi `http://www.adobe.com/it` e `https://www.adobe.com/it` corrispondono entrambi.

   Viene aperto il Compositore esperienza visivo e viene visualizzata la pagina.

1. Fai clic sull&#39;elemento in cui devono essere visualizzati i consigli e seleziona **[!UICONTROL Sostituisci contenuto]** > **[!UICONTROL Consiglio]**.

   <!--
   * **[!UICONTROL Replace w/ Recommendations]**: Deletes the current content of the element and replaces it with the recommendations.
   * **[!UICONTROL Insert Recommendations Before]**: Places the recommendations before the element, above or to the left of it, depending on the page construction.
   * **[!UICONTROL Insert Recommendations After]**: Places the recommendations after the element, below or to the right of it, depending on the page construction.

   ![Visual Experience Composer with a selected container and the menu options Replace w/ Recommendations, Insert Recommendations Before, Insert Recommendations After, and Expand Selection](/help/main/c-recommendations/t-create-recs-activity/assets/Menu_Replace-Insert.png)

   Use **[!UICONTROL Expand Selection]** to expand the selection to the parent container, so that it includes the desired page elements.
   -->

   I visitatori che si qualificano per il consiglio visualizzano gli articoli consigliati nell’area specificata. I visitatori che non sono idonei visualizzano il contenuto predefinito.

   >[!NOTE]
   >
   >Le attività **[!UICONTROL Recommendations]** supportano una sola modifica o consiglio alla volta. Per visualizzare più consigli, crea diverse attività [!DNL Recommendations] oppure utilizza test A/B o XT.

   ![Compositore esperienza visivo con un&#39;immagine selezionata nella pagina e l&#39;opzione Consigli visualizzata nel menu](../assets/create_reco_2.png)

<!--
1. Select a page type: Cart Page, Category Page, Home Page, Landing Page, Product Page, Search Results Page, Thank You Page, or Other.

   ![Select Page Type dialog box with the list of page types open](/help/main/c-recommendations/t-create-recs-activity/assets/Menu_PageType.png)

   The page type determines which criteria are suggested in the next section.
-->

1. Accedi al menu **[!UICONTROL Mostra proprietà]** e fai clic su **[!UICONTROL Seleziona un consiglio]**.

   ![Pannello Consigli del Compositore esperienza visivo con il pulsante Seleziona un consiglio](../assets/create_reco_3.png)

## Seleziona i criteri {#select-criteria}

I criteri determinano quali articoli sono consigliati e come vengono scelti per ogni visitatore.

1. Selezionare la casella di controllo di uno o più [criteri](/help/main/c-recommendations/c-algorithms/algorithms.md).

   ![Finestra di dialogo Seleziona criteri con il campo di ricerca, l&#39;icona del filtro, il pulsante Crea criteri e l&#39;elenco dei criteri con un criterio selezionato](../assets/create_reco_4.png)

   Quando sono selezionati più criteri, il traffico viene suddiviso in modo uniforme tra di essi e le percentuali non possono essere modificate per ciascun criterio. Ad esempio, se selezioni due criteri e l’attività visualizza il contenuto predefinito al 20% dei partecipanti, il 40% di questi vede le raccomandazioni di ciascun criterio.

   >[!NOTE]
   >
   >Non tutti i criteri vengono eseguiti correttamente su ogni pagina. Affinché i consigli per l&#39;elemento corrente o la categoria corrente siano compatibili, la pagina o la mbox deve passare in `entity.id` o `entity.categoryId`. È consigliabile mostrare solo i criteri compatibili. Per rendere disponibili criteri incompatibili per l&#39;attività, deselezionare la casella di controllo **[!UICONTROL Compatibile]**. Questa casella di controllo potrebbe non essere visualizzata, a seconda dell&#39;impostazione **[!UICONTROL Amministrazione]** > **[!UICONTROL Consigli]** > **[!UICONTROL Filtra criteri incompatibili]**. Per ulteriori informazioni, consulta [Impostazioni](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html?lang=it){target=_blank}.

1. Se necessario, individua o crea i criteri:

   * Per cercare un criterio esistente quando l’elenco è lungo, digita nel campo di ricerca fino a visualizzare il criterio desiderato. Alcuni criteri sono forniti con [!DNL Recommendations] e il team può anche creare criteri personalizzati.
   * Per creare un nuovo criterio, fare clic su **[!UICONTROL Crea criterio]**, quindi immettere le informazioni per il nuovo criterio. Vedi [Creare i criteri](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md).
   * Per raggruppare i criteri in una sequenza, creane una. Consulta [Creare sequenze di criteri](/help/main/c-recommendations/c-algorithms/create-criteria-sequence.md).

1. Fai clic su **[!UICONTROL Avanti]**.

## Seleziona design e promozioni {#select-design}

Una progettazione è un modello che determina l’aspetto dei consigli nella posizione selezionata e una raccolta determina gli elementi idonei per la visualizzazione. Facoltativamente, le promozioni possono essere aggiunte alle raccomandazioni.

1. Seleziona un [design](/help/main/c-recommendations/c-design-overview/design-overview.md).

   ![Finestra di dialogo Seleziona design con il pulsante Crea design e l&#39;elenco dei design con il design 2 x 4 selezionato](../assets/create_reco_5.png)

   * Per utilizzare le progettazioni esistenti, seleziona la casella di controllo di una o più progettazioni, quindi fai clic su **[!UICONTROL Successivo]**. È possibile selezionare un solo design quando sono stati selezionati più criteri.
   * Per creare una progettazione personalizzata, fare clic su **[!UICONTROL Crea progettazione]** e immettere il nome e il codice della nuova progettazione. Fai clic su **[!UICONTROL Avanti]**, seleziona o carica un&#39;immagine, quindi fai clic su **[!UICONTROL Fine]** > **[!UICONTROL Fine]**.

   [!DNL Target] include diverse progettazioni preconfigurate. Per ulteriori informazioni sulle progettazioni personalizzate, vedere [Creare una progettazione](/help/main/c-recommendations/c-design-overview/create-design.md#create-design) e [Personalizzare una progettazione utilizzando Velocity](/help/main/c-recommendations/c-design-overview/customizing-a-template.md#customize-design).

1. Fai clic su **[!UICONTROL Avanti]**.

1. Nella pagina **[!UICONTROL Opzioni]**, seleziona la raccolta.

   La raccolta determina gli elementi idonei a essere visualizzati nei consigli. Per ulteriori informazioni, tra cui come creare una raccolta, vedere [Utilizzare una raccolta in un&#39;attività](/help/main/c-recommendations/c-products/collections.md#use-collection).

1. (Facoltativo) Aggiungi promozioni prima e dopo ai consigli. Consulta [Aggiungi promozioni](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md#add-promotions).

1. Fai clic su **[!UICONTROL Salva]**.

   Nella schermata del Compositore esperienza visivo viene visualizzata la progettazione dei consigli sulla pagina.

## Rivedi e completa l&#39;attività {#complete-activity}

Rivedere i consigli e il flusso di attività prima di salvarlo consente di confermare che siano presenti il pubblico, i criteri e la progettazione corretti.

1. (Facoltativo) Fai clic su **[!UICONTROL Anteprima]** per vedere come l&#39;attività viene visualizzata ai visitatori. Questa modalità consente l’interazione con i consigli, come farebbe un visitatore con loro. Fai clic su **[!UICONTROL Componi]** per tornare al Compositore esperienza visivo.

1. Rivedi il consiglio nel Compositore esperienza visivo, quindi fai clic su **[!UICONTROL Avanti]**.

1. Rivedi l’attività nel diagramma di flusso e apporta le eventuali modifiche necessarie. Al termine, fai clic su **[!UICONTROL Avanti]**.

   ![Diagramma di flusso dei consigli con tutti i visitatori suddivisi in un gruppo di controllo al 10% e un gruppo al 90% che conduce alla raccolta Tutte le raccolte, ai criteri selezionati e alla progettazione 2 x 4](../assets/create_reco_6.png)

   Il diagramma di flusso descrive il pubblico per l’attività, le esperienze e le metriche di successo. Dal diagramma è possibile apportare le seguenti modifiche:

   * **Pubblico**: per impostazione predefinita, tutti i visitatori visualizzano i consigli, ma è possibile selezionare un pubblico esistente. In alternativa alla creazione di un nuovo pubblico, è possibile creare un pubblico [per sola attività](/help/main/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483) oppure [per più tipi di pubblico](/help/main/c-target/combining-multiple-audiences.md#section_2F1CE9434CC04174B4BA2BFC89B85D77) per creare un pubblico ad hoc.
   * **Criteri**: visualizzare i criteri o modificare la raccolta (accanto all&#39;etichetta **[!UICONTROL Criteri]**).
   * **Gruppo di controllo**: modifica la percentuale di partecipanti che visualizzano l&#39;esperienza di controllo. In un&#39;attività [!DNL Recommendations], il gruppo di controllo visualizza la pagina senza alcun consiglio.
   * **Progettazione**: visualizza il codice di progettazione oppure modifica o rimuovi la progettazione.

1. Specifica le impostazioni dell’attività, ad esempio un nome (obbligatorio) e una finalità (facoltativa). Per le impostazioni, incluse le regole per il nome dell&#39;attività, vedere [Impostazioni attività Consigli](/help/main/c-recommendations/t-create-recs-activity/recs-activity-settings.md#recs-activity-settings).

1. Fai clic su **[!UICONTROL Salva e chiudi]**.

## Gestire l’attività {#manage-activity}

Dopo il salvataggio dell&#39;attività, nella pagina **[!UICONTROL Panoramica]** viene visualizzato un riepilogo dell&#39;attività. In questa pagina sono disponibili le azioni seguenti:

* Attiva, modifica o Esegue il controllo qualità dell’attività.
* Condividi l’attività nel feed di Experience Cloud.
* Visualizza gli URL dell’esperienza e scarica i dati.
* Modificate la percentuale di partecipanti all&#39;attività che visualizzano l&#39;esperienza di controllo.
* Mostrare o nascondere i dettagli dei criteri e visualizzare il codice per le progettazioni.

Sono disponibili due pagine aggiuntive dall’attività:

* **[!UICONTROL Report]**: mostra il report sulle prestazioni dell&#39;attività [!DNL Recommendations].
* **[!UICONTROL Conflitti]**: mostra eventuali [conflitti tra attività](/help/main/c-experiences/c-visual-experience-composer/activity-collisions.md) che potrebbero verificarsi. Le collisioni si verificano quando più attività distribuiscono contenuto alla stessa pagina e possono causare la visualizzazione di contenuto imprevisto.

## Video di formazione: Creare un’attività Consigli (7:15) ![Icona esercitazione](/help/main/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/27688)
