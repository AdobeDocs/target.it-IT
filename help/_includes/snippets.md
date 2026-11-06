---
source-git-commit: 87c0d2aa67d54dcbc2963be63d2d7ad9c02b6aa9
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 5%
---
# Frammenti

## Funzioni di Target Premium {#premium-note}

>[!NOTE]
>
>Questa funzionalità è disponibile con la licenza [Target Premium](/help/main/c-intro/intro.md#premium). Questa funzionalità non è disponibile in [!DNL Target Standard].

## Aggiornamento delle autorizzazioni di Target {#permissions-update}

>[!IMPORTANT]
>
>[!DNL Target] utenti con i diritti di [!UICONTROL Amministratore di prodotto] e [!UICONTROL Amministratore di sistema] possono modificare tutte le impostazioni nelle pagine [!UICONTROL Amministrazione], indipendentemente dal loro ruolo in [!DNL Target]. Gli utenti senza queste autorizzazioni dispongono di accesso in sola lettura a queste impostazioni.

## Interfaccia utente di Target aggiornata {#updated-ui}

>[!NOTE]
>
>Nel 2025, [!DNL Target] ha introdotto un&#39;interfaccia utente aggiornata e [!UICONTROL il Compositore esperienza visivo] (VEC). Per ulteriori informazioni, fai clic sui seguenti collegamenti:
>
>* [[!DNL Target Standard/Premium] 25.2.1 (17 febbraio 2025) - Note sulla versione](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-2): fornisce un riepilogo delle modifiche chiave apportate all&#39;interfaccia utente in [!DNL Target] per [!UICONTROL Attività], [!UICONTROL Consigli] e [!UICONTROL Compositore esperienza visivo].
>
>* [[!DNL Target Standard/Premium] 25.1.1 (9 gennaio 2025) note sulla versione](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-1): fornisce un riepilogo delle modifiche all&#39;interfaccia utente chiave in [!DNL Target] per la [!UICONTROL Libreria offerte].
>
>* [Comprendere l&#39;interfaccia utente [!DNL Target] UI](/help/main/c-intro/understand-the-target-ui.md): fornisce una breve panoramica per acquisire familiarità con [!DNL Target] e fornisce collegamenti per informazioni più approfondite e istruzioni dettagliate.
>
>* [[!UICONTROL Modifiche al Compositore esperienza visivo]](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md): la versione [!DNL Adobe Target Standard/Premium] 25.2.1 (17 febbraio 2015) introduce una versione aggiornata del [!UICONTROL Compositore esperienza visivo]. Questo articolo spiega le differenze tra le versioni legacy e aggiornata del Compositore esperienza visivo.
>
>* [[!UICONTROL Opzioni del Compositore esperienza visivo]](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md): questo articolo illustra l&#39;interfaccia utente del Compositore esperienza visivo aggiornata e le relative opzioni.
>
>* [[!DNL Target] Domande frequenti sull&#39;aggiornamento dell&#39;interfaccia utente](/help/main/c-intro/updated-ui-faq.md): queste domande frequenti riguardano le domande comuni sulla nuova interfaccia utente [!DNL Target] e sul [!UICONTROL Compositore esperienza visivo], incluse le modifiche alla navigazione, le posizioni delle funzionalità e l&#39;attivazione/disattivazione della versione temporanea dell&#39;interfaccia utente. Che tu sia un addetto marketing, uno sviluppatore o un amministratore, queste domande frequenti consentono una transizione fluida e di sfruttare al massimo l’interfaccia utente aggiornata.

## Regole del nome attività {#activity-name-rules}

Il nome attività non può iniziare con `=`, `+`, `-` o `@`. Il nome dell&#39;attività non può inoltre contenere nessuna delle seguenti sequenze di caratteri: `;=`, `;+`, `;-`, `;@`, `,=`, `,+`, `,-`, `,@`, `["` o `"]`.

## Selezionare un pubblico nel passaggio Targeting {#audience-selection-steps}

1. Per cambiare il pubblico, fai clic sull&#39;icona **[!UICONTROL Sostituisci]** ( ![Sostituisci](/help/main/assets/icons/Retweet.svg) ) nel riquadro a destra.

1. Nella finestra di dialogo **[!UICONTROL Aggiungi pubblico]**, [seleziona il pubblico desiderato](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md), quindi fai clic su **[!UICONTROL Assegna pubblico]**.

   Per creare un pubblico che combina più tipi di pubblico, fare clic su **[!UICONTROL Combina tipi di pubblico]**. Per ulteriori dettagli, vedere [Combinare più tipi di pubblico](/help/main/c-target/combining-multiple-audiences.md).

   Per creare un nuovo pubblico che non sia già presente nella [!UICONTROL Libreria pubblico], fai clic su **[!UICONTROL Crea pubblico]**. Nel flusso di lavoro [create-audience](/help/main/c-target/c-audiences/audiences.md), scegli una delle seguenti opzioni:

   * **[!UICONTROL Libreria tipi di pubblico]**: crea un pubblico on-demand salvato nella [!UICONTROL Libreria tipi di pubblico] e riutilizzabile in altre attività.
   * **[!UICONTROL Solo per questa attività]**: crea un [pubblico specifico per l&#39;attività](/help/main/c-target/creating-activity-only-audience.md) che non viene salvato nella [!UICONTROL Libreria tipi di pubblico] e che può essere utilizzato solo nell&#39;attività corrente.

1. Fai clic su **[!UICONTROL Percentuale visitatori]** nel frame a destra, quindi scegli la percentuale di visitatori idonei che desideri inserire nell&#39;attività.


