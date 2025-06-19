---
keywords: compositore esperienza visivo;vec;wysiwyg
description: Comprendere le modifiche introdotte nel Compositore esperienza visivo nella versione Adobe Target 25.2.1 (17 febbraio 2025).
title: Quali modifiche vengono introdotte nel nuovo Compositore esperienza visivo?
feature: Visual Experience Composer (VEC)
exl-id: 4c7a5657-93d9-4355-9d2b-c992b36bcb50
source-git-commit: b1bde455f686c34e7a5184868ce63db0b74e2af7
workflow-type: tm+mt
source-wordcount: '781'
ht-degree: 0%

---

# [!UICONTROL Visual Experience Composer] modifiche

La versione di [!DNL Adobe Target Standard/Premium] 25.2.1 (17 febbraio 2015) introduce una versione aggiornata di [!UICONTROL Visual Experience Composer] (VEC). Questo articolo spiega le differenze tra la versione precedente e quella aggiornata del Compositore esperienza visivo.

>[!IMPORTANT]
>
>Il [!UICONTROL Visual Editing Composer] aggiornato richiede l&#39;estensione [!DNL Adobe Experience Cloud] [[!UICONTROL Visual Editing Helper]](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) disponibile in [!DNL Chrome Web Store].

Il Compositore esperienza visivo viene visualizzato quando crei o modifichi un’attività esistente.

![Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/assets/vec-highlight-refresh.png)

## Modifiche principali al Compositore esperienza visivo

Nelle sezioni seguenti vengono illustrate le principali modifiche apportate al Compositore esperienza visivo aggiornato rispetto alla versione precedente.

### Barra [!UICONTROL Experiences]

Come nella versione precedente, la barra [!UICONTROL Experiences] rimane sul lato sinistro del Compositore esperienza visivo. Impossibile comprimere la barra [!UICONTROL Experiences].

![Barra delle esperienze](/help/main/c-experiences/c-visual-experience-composer/assets/experiences-panel.png)

È possibile creare, rinominare o rimuovere esperienze utilizzando la barra [!UICONTROL Experiences]. Fai clic sull&#39;icona **[!UICONTROL Add]** ( ![Icona Aggiungi](/help/main/assets/icons/Add.svg) ) per aggiungere una nuova esperienza. Fai clic sull&#39;icona [!UICONTROL More Actions] ( ![Icona Altre azioni](/help/main/assets/icons/MoreSmall.svg) ) per duplicare, eliminare o reindirizzare un&#39;esperienza.

### [!UICONTROL Components] barra (nuova)

È possibile aggiungere diversi componenti alla pagina Web e modificarli in base alle esigenze utilizzando la nuova barra [!UICONTROL Components].

![Barra dei componenti](/help/main/c-experiences/c-visual-experience-composer/assets/components-panel.png)

Per aggiungere un nuovo componente, trascinare il componente dalla barra [!UICONTROL Components] che si desidera inserire su un elemento di pagina esistente nell&#39;area di lavoro [!UICONTROL Design]. Quindi scegli di inserire il componente prima di dopo l’elemento selezionato.

### Barra [!UICONTROL Modifications]

Per aprire la barra [!UICONTROL Modifications], fai clic sull&#39;icona [!UICONTROL Show Modifications] ( ![Mostra barra delle modifiche](/help/main/assets/icons/History.svg) ) nella barra [!UICONTROL Components]. La barra di [!UICONTROL Modifications] ha cambiato posizione dal lato destro a quello sinistro dell&#39;area di modifica.

![Barra delle modifiche](/help/main/c-experiences/c-visual-experience-composer/assets/modifications-panel.png)

La barra [!UICONTROL Modifications] mostra tutte le modifiche apportate alla pagina nel Compositore esperienza visivo e consente di apportare ulteriori modifiche (come selettore CSS, Mbox e codice personalizzato).

Fai clic sull&#39;icona [!UICONTROL More Options] ( ![Icona Altre azioni](/help/main/assets/icons/MoreSmall.svg) ) per aggiungere una modifica, eliminare tutte le modifiche o eliminare tutte le modifiche non valide. Fare clic su [!UICONTROL Select] per eseguire operazioni in blocco: [!UICONTROL Apply to All Pages] o [!UICONTROL Delete].

Per visualizzare di nuovo la barra [!UICONTROL Modifications], fai clic sull&#39;icona [!UICONTROL Hide Modifications] ( ![Mostra barra delle modifiche](/help/main/assets/icons/History.svg) ) nella barra [!UICONTROL Modifications].

### [!UICONTROL Properties] barra (nuova)

La barra di [!UICONTROL Properties] consente di modificare le proprietà degli elementi selezionati nella pagina, sia che si tratti di elementi di HTML che di oggetti specifici di [!DNL Target], ad esempio consigli o offerte.

![Barra delle proprietà](/help/main/c-experiences/c-visual-experience-composer/assets/properties-panel.png)

Fai clic sulle icone nella parte superiore della barra per modificare il codice HTML o eliminare, duplicare o nascondere gli elementi. Le modifiche vengono visualizzate nella barra [!UICONTROL Modifications].

![Icone delle proprietà](/help/main/c-experiences/c-visual-experience-composer/assets/options-icons.png)

La barra [!UICONTROL Properties] è comprimibile nella barra a destra. Fai clic sull&#39;icona [!UICONTROL Show/Hide Properties] ( ![icona Proprietà](/help/main/assets/icons/Propertie.svg) ) a destra della barra per comprimere o visualizzare la barra [!UICONTROL Properties].

### Impostazioni/configurazione delle attività

Fai clic sull&#39;icona [!UICONTROL Configure] ( ![icona Configura](/help/main/assets/icons/Setting.svg) ) visualizzata nell&#39;area di progettazione per visualizzare il menu delle proprietà dell&#39;attività.

![Opzioni di configurazione attività](/help/main/c-experiences/c-visual-experience-composer/assets/configure-options.png)

Le diverse opzioni ti consentono di assegnare proprietà, modificare le regole di consegna delle pagine, specificare le preferenze del sito, aggiungere ulteriori pagine e abilitare o disabilitare attività con più pagine o tipi di pubblico. Assegnare [!UICONTROL Properties] è una funzionalità di [[!DNL Target Premium]](/help/main/c-intro/intro.md#premium).

La posizione e la funzionalità sono simili a quelle della precedente interfaccia utente del Compositore esperienza visivo.

### [!UICONTROL Design]/[!UICONTROL Browse] modalità

Utilizza gli interruttori [!UICONTROL Design]/[!UICONTROL Browse] visualizzati sopra la barra di [!UICONTROL Properties] per passare dalla modalità progettazione alla modalità sfoglia.

![Attiva/disattiva progettazione e navigazione](/help/main/c-experiences/c-visual-experience-composer/assets/design-browse-mode.png)

Utilizza la modalità [!UICONTROL Browse] per navigare nel tuo sito e scegliere la visualizzazione o la pagina che desideri aggiornare. Torna alla modalità [!UICONTROL Design] per aggiungere o modificare le modifiche.

### [!UICONTROL Undo]/[!UICONTROL Redo]

Per annullare le modifiche apportate, fare clic sull&#39;icona [!UICONTROL Undo] ( ![icona Annulla](/help/main/assets/icons/Undo.svg) ).

![Icona Annulla nel Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/assets/undo.png)

Per ripristinare un&#39;azione, espandere il gruppo di pulsanti Annulla/[!UICONTROL Redo] e scegliere [!UICONTROL Redo].

### [!UICONTROL Design] area di lavoro

L&#39;area di lavoro [!UICONTROL Design] consente di selezionare i riquadri di visualizzazione, inclusi quelli adatti allo schermo, [!UICONTROL Desktop], [!UICONTROL Tablet], [!UICONTROL Mobile Landscape] e [!UICONTROL Mobile Portrait].

![Opzioni riquadro di visualizzazione](/help/main/c-experiences/c-visual-experience-composer/assets/viewports.png)

Il Compositore esperienza visivo aggiornato consente inoltre di ingrandire o ridurre facendo clic sull&#39;icona appropriata ( ![icona Zoom avanti](/help/main/assets/icons/ZoomIn.svg) o ![icona Zoom indietro](/help/main/assets/icons/ZoomOut.svg) ).

## Illustrazione visiva delle modifiche apportate all’interfaccia utente

La figura seguente mostra le modifiche di alto livello apportate all’interfaccia utente del Compositore esperienza visivo aggiornato. Nella parte superiore dell’illustrazione viene mostrata l’interfaccia utente del Compositore esperienza visivo aggiornata, mentre nella parte inferiore viene mostrata l’interfaccia utente precedente. Le frecce indicano dove sono stati spostati i vari elementi.

(Fai clic sull’immagine per espanderla fino alla larghezza completa del browser).

![Confronto VEC-nuovo/i con interfaccia utente precedente](/help/main/c-experiences/c-visual-experience-composer/assets/vec-comparison.png){width="600" zoomable="yes"}

## Ulteriori informazioni sull’interfaccia utente aggiornata

* [[!DNL Target Standard/Premium] 25.2.1 (17 febbraio 2025) - Note sulla versione](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-2): fornisce un riepilogo delle modifiche principali apportate all&#39;interfaccia utente in [!DNL Target] per [!UICONTROL Activities], [!UICONTROL Recommendations] e [!UICONTROL Visual Experience Composer] (Compositore esperienza visivo).

* [[!DNL Target Standard/Premium] 25.1.1 (9 gennaio 2025) - Note sulla versione](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-1): fornisce un riepilogo delle modifiche principali apportate all&#39;interfaccia utente in [!DNL Target] per [!UICONTROL Offers Library].

* [Comprendere l&#39;interfaccia utente [!DNL Target] UI](/help/main/c-intro/understand-the-target-ui.md): fornisce una breve panoramica per acquisire familiarità con [!DNL Target] e fornisce collegamenti per informazioni più approfondite e istruzioni dettagliate.

* [[!UICONTROL Visual Experience Composer] modifiche](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md): la versione di [!DNL Adobe Target Standard/Premium] 25.2.1 (17 febbraio 2015) introduce una versione aggiornata di [!UICONTROL Visual Experience Composer] (VEC). Questo articolo spiega le differenze tra le versioni legacy e aggiornata del Compositore esperienza visivo.

* [[!UICONTROL Visual Experience Composer] opzioni](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md): questo articolo illustra l&#39;interfaccia utente del Compositore esperienza visivo aggiornata e le relative opzioni.

* [[!DNL Target] Domande frequenti sull&#39;aggiornamento dell&#39;interfaccia utente](/help/main/c-intro/updated-ui-faq.md): queste domande frequenti riguardano le domande comuni sulla nuova interfaccia utente [!DNL Target] e sul nuovo Compositore esperienza visivo [!UICONTROL Visual Experience Composer], incluse le modifiche alla navigazione, le posizioni delle funzioni e la rimozione dell&#39;opzione di versione temporanea dell&#39;interfaccia utente. Che tu sia un addetto marketing, uno sviluppatore o un amministratore, queste domande frequenti consentono una transizione fluida e di sfruttare al massimo l’interfaccia utente aggiornata.