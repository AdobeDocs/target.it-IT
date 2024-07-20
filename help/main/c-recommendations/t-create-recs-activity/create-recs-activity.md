---
keywords: creare consigli;attività consigli;nuovi consigli;panoramica consigli
description: Scopri come utilizzare il Compositore esperienza visivo di Adobe [!DNL Target] per creare un'attività di Recommendations direttamente su una pagina abilitata per  [!DNL Target].
title: Come si crea un’attività Recommendations?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Vedi cosa è incluso in Target Premium."
feature: Recommendations
exl-id: c83073d5-f852-4f09-8343-e4658fbf6f43
source-git-commit: fe1e97710e7692ba7724103853ed7438c3f361b1
workflow-type: tm+mt
source-wordcount: '1252'
ht-degree: 54%

---

# Creare un’attività Consigli

Utilizza il Compositore esperienza visivo di Target per creare attività Consigli direttamente su una pagina abilitata per Target e modificare parti della pagina in Target.

1. Fare clic su **[!UICONTROL Create Activity]** > **[!UICONTROL Recommendations]**.

   ![Creare un’attività di Recommendations](/help/main/c-recommendations/t-create-recs-activity/assets/Menu_CreateActivity.png)

1. Selezionare **[!UICONTROL Visual (Default)]**, se necessario.

   ![Finestra di dialogo Crea attività di Recommendations](/help/main/c-recommendations/t-create-recs-activity/assets/DB_NewRecAct.png)

   Se preferisci utilizzare il Compositore esperienza basato su moduli, seleziona [!UICONTROL Form]. Per ulteriori informazioni, consulta [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md).

   >[!NOTE]
   >
   >Oltre al Compositore esperienza visivo e al Compositore esperienza basato su moduli, Target offre anche il Compositore esperienza visivo per applicazione a pagina singola e quello per app mobili. Per ulteriori informazioni sui vari moduli di composizione, consulta [Esperienze e offerte](/help/main/c-experiences/experiences.md).
   >
   >Per informazioni sulla risoluzione dei problemi relativi al Compositore esperienza visivo, consulta [Risoluzione dei problemi relativi al Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).
   >
   >L&#39;opzione [!UICONTROL [Choose Workplace]](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) nell&#39;illustrazione precedente è una funzionalità di [Target Premium](/help/main/c-intro/intro.md). Se la tua organizzazione dispone di una licenza Target Standard, questa opzione non è disponibile.

1. (Condizionale) Se sei un cliente [Target Premium](/help/main/c-intro/intro.md#premium), scegli un’[area di lavoro](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. Specificare un URL attività, quindi fare clic su **[!UICONTROL Next]**.

   >[!NOTE]
   >
   >[!DNL Target] non distingue tra protocolli URL ([!DNL https] e [!DNL http]). Di conseguenza, [!DNL `http://www.adobe.com`] e [!DNL `https://wwww.adobe.com`] corrispondono entrambi.

   L’URL dell’attività è la pagina in cui verranno visualizzati i consigli.

   Quando fai clic su [!UICONTROL Next], viene aperto il Compositore esperienza visivo e viene visualizzata la pagina. Puoi sostituire un elemento corrente con i consigli oppure inserirli.

1. Fai clic su un elemento nella pagina; quindi, se i consigli sono disponibili nella posizione in cui si trova l&#39;elemento, fai clic su **[!UICONTROL Replace w/ Recommendations]**, **[!UICONTROL Insert Recommendations Before]** o **[!UICONTROL Insert Recommendations After]**.

   I visitatori del tuo sito visualizzeranno il contenuto consigliato solo se sono idonei per il consiglio. I visitatori che non sono idonei per il consiglio visualizzeranno il contenuto predefinito.

   ![Opzioni per la funzione Consigli](/help/main/c-recommendations/t-create-recs-activity/assets/Menu_Replace-Insert.png)

   * **[!UICONTROL Replace w/ Recommendations]**: la sostituzione di un elemento con i consigli elimina il contenuto corrente e lo sostituisce con i consigli. Quando i visitatori visitano il tuo sito e si qualificano per il consiglio, visualizzano gli articoli consigliati nell&#39;area specificata invece che nel contenuto esistente.
   * **[!UICONTROL Insert Recommendations Before]**: l&#39;inserimento di consigli prima che l&#39;elemento selezionato inserisca il contenuto consigliato prima di tale elemento. A seconda della costruzione della pagina, il consiglio viene visualizzato sopra o a sinistra dell’elemento selezionato.
   * **[!UICONTROL Insert Recommendations After]**: l&#39;inserimento di consigli dopo che l&#39;elemento selezionato inserisce il contenuto consigliato dopo tale elemento. A seconda della costruzione della pagina, il consiglio viene visualizzato di seguito o a destra dell’elemento selezionato.

   L&#39;opzione **[!UICONTROL Expand Selection]** consente di espandere la posizione selezionata (contenitore padre) per identificare e includere più facilmente gli elementi di pagina desiderati.

1. Seleziona un tipo di pagina.

   I tipi di pagina possono includere:

   * Pagina del carrello
   * Pagina categoria
   * Home page
   * Pagina di destinazione
   * Pagina di prodotto
   * Pagina risultati di ricerca
   * Pagina di ringraziamento
   * Altro

   ![Opzioni per Seleziona tipo di pagina](/help/main/c-recommendations/t-create-recs-activity/assets/Menu_PageType.png)

1. Seleziona uno o più [criteri](/help/main/c-recommendations/c-algorithms/algorithms.md).

   I criteri vengono visualizzati sotto forma di schede contenenti informazioni su ciascun criterio. Per impostazione predefinita, nella schermata [!UICONTROL Select Criteria] sono visualizzati criteri compatibili con il settore verticale e il tipo di pagina selezionato nel passaggio precedente. Puoi modificare queste opzioni per visualizzare altri criteri.

   >[!NOTE]
   >
   >Non tutti i criteri vengono eseguiti correttamente su ogni pagina. La pagina o mbox deve passare `entity.id` o `entity.categoryId` per rendere compatibili i consigli per l’elemento o la categoria corrente. In generale, è consigliabile mostrare solo i criteri compatibili. Se tuttavia si desidera rendere disponibili criteri non compatibili per l&#39;attività, deselezionare la casella di controllo **[!UICONTROL Compatible]**. L&#39;opzione [!UICONTROL Compatible] potrebbe non essere visualizzata, a seconda delle impostazioni di Recommendations ( **[!UICONTROL Recommendations]** > **[!UICONTROL Settings]** > **[!UICONTROL Filter Incompatible Criteria]**). Per ulteriori informazioni, vedere [Impostazioni](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank}.

   ![Finestra di dialogo Seleziona criteri](/help/main/c-recommendations/t-create-recs-activity/assets/SCRN_SelectCriteria2.png)

   Se selezioni più criteri, il traffico viene suddiviso in modo uniforme tra i criteri selezionati. Ad esempio, se hai selezionato due criteri e l’attività è progettata per mostrare il contenuto predefinito al 20% dei partecipanti all’attività, il 40% dei partecipanti vedrà i consigli controllati da ogni criterio. Non c’è modo di modificare le percentuali per ogni criterio.

   * Per cercare un criterio esistente (ad esempio, se sono visualizzate numerose schede di criteri), digitare nel campo di ricerca fino a visualizzare i criteri desiderati, quindi selezionarli e fare clic su **[!UICONTROL Next]**.

     Alcuni criteri sono forniti con [!DNL Recommendations]. Con il tuo team puoi inoltre creare criteri personalizzati.

   * Per creare un nuovo criterio, fare clic su **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]**, quindi inserire le informazioni per il nuovo criterio. Per informazioni sulla creazione di un nuovo criterio, consulta [Creazione di criteri](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md).
   * È inoltre possibile raggruppare i criteri in sequenze. Per creare una nuova sequenza di criteri, fare clic su **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria Sequence]**. Per ulteriori informazioni, vedere [Crea sequenza criteri](/help/main/c-recommendations/c-algorithms/create-criteria-sequence.md).

1. Fare clic su **[!UICONTROL Next]**.
1. Seleziona un [design](/help/main/c-recommendations/c-design-overview/design-overview.md).

   Una progettazione è un modello che determina l’aspetto delle posizioni sulla pagina. [!DNL Target] include diverse progettazioni preconfigurate. Puoi anche creare progettazioni personalizzate. Per ulteriori informazioni, vedere [Creare una progettazione](/help/main/c-recommendations/c-design-overview/create-design.md#task_CC5BD28C364742218C1ACAF0D45E0E14) e [Personalizzare una progettazione](/help/main/c-recommendations/c-design-overview/customizing-a-template.md#concept_94F1554C3F2E4CDB9A2C3D78F10EDA59).

   ![Finestra di dialogo Seleziona design](/help/main/c-recommendations/t-create-recs-activity/assets/Card_SelectDesign.png)

   Ogni design, o progettazione, mostra una rappresentazione grafica di come apparirà; viene inoltre indicato da quante attività attive e inattive è attualmente utilizzato.

   * Per selezionare una o più progettazioni esistenti, fare clic sulle progettazioni e quindi su **[!UICONTROL Next]**.

     Se hai selezionato più criteri, puoi selezionare un solo design.

   * Per creare una progettazione personalizzata, fare clic su **[!UICONTROL Create Design]**, quindi immettere il nome e il codice per la nuova progettazione. Fai clic su **[!UICONTROL Next]**, quindi seleziona o carica un&#39;immagine e fai clic su **[!UICONTROL Done]** > **[!UICONTROL Done]**. Per informazioni sulla creazione di una nuova progettazione, consulta [Creare una progettazione](/help/main/c-recommendations/c-design-overview/create-design.md#task_CC5BD28C364742218C1ACAF0D45E0E14).

1. Fare clic su **[!UICONTROL Next]**.

   Puoi aggiungere delle promozioni ai consigli. Per ulteriori informazioni sull&#39;aggiunta di promozioni prima e dopo, vedere [Aggiunta di promozioni](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md#task_CC5BD28C364742218C1ACAF0D45E0E14).

1. Fare clic su **[!UICONTROL Save]**.

   La schermata del Compositore esperienza visivo mostra la progettazione dei consigli sulla tua pagina.

1. (Facoltativo) Fai clic su **[!UICONTROL Preview]** per vedere come verrà visualizzata l&#39;attività ai visitatori.

   La modalità [!UICONTROL Preview] consente di interagire con i consigli, proprio come farebbe un visitatore.

   Al termine della visualizzazione in anteprima dei consigli, fare clic su **[!UICONTROL Compose]**.

1. Rivedi i consigli nel Compositore esperienza visivo, quindi fai clic su **[!UICONTROL Next]**.

1. Rivedi l’attività di [!DNL Recommendations] nel diagramma di flusso e apporta le eventuali modifiche necessarie.

   ![Diagramma di flusso di Recommendations](/help/main/c-recommendations/t-create-recs-activity/assets/SCRN_Workflow.png)

   Il diagramma di flusso ti guida attraverso le fasi di selezione dell’audience per l’attività, configurazione delle esperienze e specifica delle metriche di successo.

   Nel diagramma di flusso puoi eseguire le operazioni seguenti:

   * Cambiare il pubblico che vedrà i consigli

     >[!NOTE]
     >
     >Oltre a selezionare un pubblico esistente, puoi [creare un pubblico per sola attività](/help/main/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483) o [combinare più tipi di pubblico](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) per creare tipi di pubblico ad hoc anziché crearne uno nuovo.

     Per impostazione predefinita, tutti gli utenti visualizzano i consigli. Tuttavia, puoi eseguire il targeting dei consigli per un pubblico specifico.

     Per un’attività di [!DNL Recommendations], il gruppo di controllo visualizza la pagina senza gli eventuali consigli.

   * Visualizzare i criteri
   * Cambia la raccolta (accanto all&#39;etichetta [!UICONTROL Criteria])
   * Modificare la percentuale di partecipanti che visualizzano l’esperienza di controllo
   * Visualizzare il codice di progettazione
   * Modificare o rimuovere una progettazione

1. Al termine, fare clic su **[!UICONTROL Next]**.
1. Specifica le impostazioni dell’attività.

   Digita, ad esempio, un nome (obbligatorio) e una finalità (facoltativa) per l’attività. Per informazioni sulle impostazioni, vedere [Impostazioni attività Recommendations](/help/main/c-recommendations/t-create-recs-activity/recs-activity-settings.md#reference_3FDA8388CEEC4159949151C1829E2FBB).

   >[!NOTE]
   >
   >Se specifichi un nome di attività di [!DNL Recommendation] già esistente per un’altra attività in [!DNL Recommendations Classic], la nuova attività viene risincronizzata con un nuovo nome. Il nuovo nome è composto dal nome originale più una marca temporale per renderlo univoco. Questo nuovo nome viene visualizzato in entrambi [!DNL Target Standard/Premium] e [!DNL Recommendations Classic].

1. Al termine, fare clic su **[!UICONTROL Save & Close]**.

   Viene visualizzata una panoramica dell’attività.

   Dalla pagina [!UICONTROL Overview] è possibile:

   * Attivare l’attività
   * Modificare l’attività
   * Condividi l’attività nel tuo feed Experience Cloud
   * Eseguire il controllo qualità dell’attività
   * Visualizzare gli URL dell’esperienza
   * Scaricare dati
   * Modificare la percentuale di partecipanti all’attività che visualizzano l’esperienza di controllo
   * Mostrare o nascondere i dettagli dei criteri
   * Visualizzare il codice delle progettazioni

1. (Facoltativo) Aprire la pagina [!UICONTROL Reports] per visualizzare il report che mostra le prestazioni dell&#39;attività [!DNL Recommendations].

1. (Facoltativo) Apri la pagina [!UICONTROL Collisions] per visualizzare eventuali [conflitti tra attività](/help/main/c-experiences/c-visual-experience-composer/activity-collisions.md) che potrebbero verificarsi.

   I conflitti tra attività si verificano quando più attività sono impostate per consegnare il contenuto sulla stessa pagina e possono causare la visualizzazione di contenuto imprevisto.

## Video di formazione: Crea un&#39;attività Recommendations (7:15) ![Icona esercitazione](/help/main/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/27688)
