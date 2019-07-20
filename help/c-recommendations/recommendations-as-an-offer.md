---
description: Funzione Adobe Recommendations come offerta nelle attività di test A/B e Targeting delle esperienze.
keywords: Recommendations;consigli;offerta
seo-description: Funzione Adobe Recommendations come offerta all’interno di test A/B (tra cui Allocazione automatica e Targeting automatico) e attività di targeting delle esperienze (XT)
seo-title: Funzione Adobe Recommendations come offerta all’interno di test A/B (tra cui Allocazione automatica e Targeting automatico) e attività di targeting delle esperienze (XT)
solution: Target
title: Consigli come offerta
title-outputclass: premium
topic: Premium
translation-type: tm+mt
source-git-commit: e8e6dcadf307209abcc712798b714af0a5be2e7e

---


# ![PREMIUM](/help/assets/premium.png) Consigli come offerta

Ora puoi includere consigli all'interno di [!UICONTROL test A/B] (tra cui [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico]) e attività di [!UICONTROL targeting delle esperienze] (XT).

Questo apre a funzionalità tutte nuove, ad esempio:

* Contenuto relativo e non relativo a consigli di test e targeting all’interno della stessa attività.
* Facile sperimentazione con il posizionamento di consigli sulla pagina, tra cui l’ordine di più consigli.
* Invio automatico di traffico all'esperienza di consigli con le prestazioni migliori tramite [!UICONTROL Allocazione automatica].
* Assegnazione dinamica di visitatori a esperienze di consigli su misura in base al loro profilo tramite [!UICONTROL Targeting automatico].

Per iniziare, crea un’attività [!UICONTROL Test A/B] o [!UICONTROL Targeting delle esperienze] tramite il [!UICONTROL Compositore esperienza visivo] e utilizza l’azione [!UICONTROL Inserisci prima], [!UICONTROL Inserisci dopo] o [!UICONTROL Sostituisci con] per aggiungere consigli a un’esperienza.

## Aggiungere un Consiglio come offerta in un’attività di test A/B o XT

1. Avvia il flusso di lavoro guidato in tre passaggi utilizzando il Compositore esperienza visivo per creare un’attività [Test A/B](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) o [Targeting delle esperienze](/help/c-activities/t-experience-target/t-xt-create/xt-create.md) (XT).

   >[!NOTE]
   >
   >Per i test A/B, ricorda che puoi scegliere l’opzione [Allocazione automatica](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) per inviare automaticamente il traffico ai consigli con prestazioni migliori, oppure l’opzione [Targeting automatico](/help/c-activities/auto-target-to-optimize.md) per assegnare esperienze di consigli su misura ai visitatori in base ai loro profili.

1. While creating an [experience](/help/c-experiences/c-visual-experience-composer/viztarget-options.md), click the element you want to add a recommendation to as an offer, select the **[!UICONTROL Insert Before]**, **[!UICONTROL Insert After]**, or **[!UICONTROL Replace With]** action, then select [!UICONTROL Recommendation].

   Nell’illustrazione seguente viene mostrata l’opzione [!UICONTROL Inserisci dopo &gt; Consiglio].

   ![Inserire un Consiglio come offerta](/help/c-recommendations/assets/replace-after-recommendations.png)

1. Seleziona tra le seguenti opzioni per visualizzare i criteri delle consigli più comuni per tipo di pagina:

   * Pagina del carrello
   * Pagina categoria
   * Home page
   * Pagina di destinazione
   * Pagina di prodotto
   * Pagina risultati ricerca
   * Pagina di ringraziamento
   * Altre

1. Seleziona i [criteri](/help/c-recommendations/c-algorithms/algorithms.md) desiderati, quindi fai clic su [!UICONTROL Avanti].
1. Seleziona la [progettazione](/help/c-recommendations/c-design-overview/design-overview.md), quindi fai clic su [!UICONTROL Avanti].
1. Nella finestra di dialogo [!UICONTROL Opzioni], specifica quanto segue:

   * Scegli una [raccolta](/help/c-recommendations/c-products/collections.md).
   * Configura le opzioni [Promozione prima e Promozione dopo](/help/c-recommendations/t-create-recs-activity/adding-promotions.md), a seconda delle necessità.

1. Fai clic su [!UICONTROL Salva].
1. Completa la configurazione dell’attività di test A/B o XT utilizzando il flusso di lavoro guidato in tre parti.

## Modificare la configurazione di un’offerta di consigli

Esistono due modi per modificare la configurazione di un’offerta:

* Tramite il menu [!UICONTROL Modifica]
* Tramite il pannello delle [!UICONTROL Modifiche]

### Modificare un’offerta di consigli tramite il menu Modifica

1. Fai clic sull’offerta da modificare, quindi fai clic su Modifica.

   ![Menu Modifica](/help/c-recommendations/assets/recs-offer-edit.png)

1. Scegli una tra le opzioni seguenti:

   * [Modifica criteri](/help/c-recommendations/c-algorithms/algorithms.md)
   * [Modifica progettazione](/help/c-recommendations/c-design-overview/design-overview.md)
   * [Modifica raccolta](/help/c-recommendations/c-products/collections.md)
   * [Modifica promozione](/help/c-recommendations/t-create-recs-activity/adding-promotions.md)

1. Apporta le modifiche necessarie.

### Modificare un’offerta di consigli tramite il pannello Modifiche

1. Fai clic sull’icona [!UICONTROL Modifiche] *“&lt;/&gt;”* per visualizzare il riquadro [Modifiche](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md).
1. Passa il cursore del mouse sull’azione desiderata, quindi fai clic sull’icona [!UICONTROL Modifica].

   ![Pannello delle modifiche](/help/c-recommendations/assets/recs-offer-modifications.png)

1. Apporta le modifiche necessarie.

## Eliminare un’offerta di consigli

Esistono due modi per eliminare un’offerta di consigli:

* Tramite il menu [!UICONTROL Modifica]
* Tramite il pannello delle [!UICONTROL Modifiche]

### Eliminare un’offerta di consigli tramite il menu Modifica

1. Fai clic sull’offerta da rimuovere, quindi fai clic su [!UICONTROL Layout &gt; Rimuovi].

   ![Rimuovi](/help/c-recommendations/assets/recs-offer-remove.png)

### Eliminare un’offerta di consigli tramite il pannello Modifiche

1. Fai clic sull’icona [!UICONTROL Modifiche] *“&lt;/&gt;”* per visualizzare il riquadro [Modifiche](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md).
1. Passa il cursore del mouse sull’azione desiderata, quindi fai clic sull’icona [!UICONTROL Elimina].

   ![Icona Elimina](/help/c-recommendations/assets/recs-offer-delete.png)