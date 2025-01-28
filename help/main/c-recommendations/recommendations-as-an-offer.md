---
keywords: Recommendations;consigli;offerta
description: Scopri come utilizzare Adobe Recommendations come offerta all’interno di test A/B (tra cui Allocazione automatica e Targeting automatico) e attività di Experience Targeting (XT).
title: Come si utilizza la funzione Recommendations (Consigli) come offerta in altri tipi di attività?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
exl-id: ec520555-b439-46a9-ab2d-f0981532bffb
source-git-commit: f848c79cb95009b5810a1707d04e548a57220e12
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 60%

---

# Consigli come offerta

È ora possibile includere i consigli nelle attività [!UICONTROL A/B Test] (inclusi [!UICONTROL Auto-Allocate] e [!UICONTROL Auto-Target]) e [!UICONTROL Experience Targeting] (XT).

Questo apre a funzionalità tutte nuove, ad esempio:

* Contenuto relativo e non relativo a consigli di test e targeting all’interno della stessa attività.
* Facile sperimentazione con il posizionamento di consigli sulla pagina, tra cui l’ordine di più consigli.
* Invio automatico di traffico all&#39;esperienza di consigli con le prestazioni migliori tramite [!UICONTROL Auto-Allocate].
* Assegnazione dinamica di visitatori a esperienze di consigli su misura in base al loro profilo tramite [!UICONTROL Auto-Target].

Per iniziare, crea un&#39;attività [!UICONTROL A/B Test] o [!UICONTROL Experience Targeting] utilizzando [!UICONTROL Visual Experience Composer] e utilizza l&#39;azione [!UICONTROL Insert Before], [!UICONTROL Insert After] o [!UICONTROL Replace With] per aggiungere consigli a un&#39;esperienza.

## Aggiungere un Consiglio come offerta in un’attività di test A/B o XT

1. Avvia il flusso di lavoro guidato in tre passaggi utilizzando il Compositore esperienza visivo per creare un’attività [Test A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) o [Targeting delle esperienze](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md) (XT).

   >[!NOTE]
   >
   >Per i test A/B, ricorda che puoi scegliere l’opzione [Allocazione automatica](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) per inviare automaticamente il traffico ai consigli con prestazioni migliori, oppure l’opzione [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md) per assegnare esperienze di consigli su misura ai visitatori in base ai loro profili.

1. Durante la creazione di una [esperienza](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md), fai clic sull&#39;elemento a cui desideri aggiungere un consiglio come offerta, fai clic su **[!UICONTROL Replace Content]**, quindi seleziona **[!UICONTROL Recommendation]**.

   ![Inserire un Consiglio come offerta](/help/main/c-recommendations/t-create-recs-activity/assets/recs-as-offer.png)

1. Seleziona tra le seguenti opzioni per visualizzare i criteri delle consigli più comuni per tipo di pagina:

   * Pagina del carrello
   * Pagina categoria
   * Home page
   * Pagina di destinazione
   * Pagina di prodotto
   * Pagina risultati di ricerca
   * Pagina di ringraziamento
   * Altro

1. Seleziona i [criteri](/help/main/c-recommendations/c-algorithms/algorithms.md) desiderati, quindi fai clic su [!UICONTROL Next].
1. Seleziona la [progettazione](/help/main/c-recommendations/c-design-overview/design-overview.md) desiderata, quindi fai clic su [!UICONTROL Next].
1. Nella finestra di dialogo [!UICONTROL Options], specificare quanto segue:

   * Scegli una [raccolta](/help/main/c-recommendations/c-products/collections.md).
   * Configura le opzioni [Promozione prima e Promozione dopo](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md), a seconda delle necessità.

1. Fare clic su [!UICONTROL Save].
1. Completa la configurazione dell’attività di test A/B o XT utilizzando il flusso di lavoro guidato in tre parti.

## Modificare la configurazione di un’offerta di consigli

Esistono due modi per modificare la configurazione di un’offerta:

* Utilizzo del menu [!UICONTROL Edit]
* Utilizzo del pannello [!UICONTROL Modifications]

### Modificare un’offerta di consigli tramite il menu Modifica

1. Fare clic sull&#39;offerta da modificare, quindi fare clic su **[!UICONTROL Edit]**.

   ![Modificare un’offerta di consigli](/help/main/c-recommendations/assets/recs-offer-edit.png)

1. Scegli una tra le opzioni seguenti:

   * [Cambia criterio](/help/main/c-recommendations/c-algorithms/algorithms.md)
   * [Cambia design](/help/main/c-recommendations/c-design-overview/design-overview.md)
   * [Cambia raccolta](/help/main/c-recommendations/c-products/collections.md)
   * [Modifica promozione](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md)

1. Apporta le modifiche necessarie.

### Modificare un’offerta di consigli tramite il pannello Modifiche

1. Fai clic sull&#39;icona [!UICONTROL Modifications] **( `</>` )** per visualizzare il riquadro [Modifiche](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md).
1. Passa il puntatore del mouse sull&#39;azione desiderata, quindi fai clic sull&#39;icona **[!UICONTROL Edit]**.

   ![Pannello delle modifiche](/help/main/c-recommendations/assets/recs-offer-modifications.png)

1. Apporta le modifiche necessarie.

## Eliminare un’offerta di consigli

Esistono due modi per eliminare un’offerta di consigli:

* Utilizzo del menu [!UICONTROL Edit]
* Utilizzo del pannello [!UICONTROL Modifications]

### Eliminare un’offerta di consigli tramite il menu Modifica

1. Fare clic sull&#39;offerta da rimuovere, quindi fare clic su **[!UICONTROL Layout > Remove]**.

   ![Rimuovi](/help/main/c-recommendations/assets/recs-offer-remove.png)

### Eliminare un’offerta di consigli tramite il pannello Modifiche

1. Fai clic sull&#39;icona [!UICONTROL Modifications] **( &lt;/> )** per visualizzare il riquadro [Modifiche](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md).
1. Passa il puntatore del mouse sull&#39;azione desiderata, quindi fai clic sull&#39;icona [!UICONTROL Delete].

   ![Icona Elimina](/help/main/c-recommendations/assets/recs-offer-delete.png)

### Visualizzazione dello stato di un’offerta Consigli {#status}

Lo stato di un&#39;offerta (algoritmo) di tipo Consigli viene visualizzato nella parte inferiore della pagina [!UICONTROL Overview] per le attività Test A/B e Targeting esperienze che contengono offerte Recommendations:

* Risultati pronti
* Risultati non pronti
* Errore di feed

![Stato di un’offerta Consigli](/help/main/c-recommendations/assets/recs-offer-status.png)

## Video di formazione: Recommendations (Consigli) come offerta ![Icona Panoramica](/help/main/assets/overview.png)

>[!VIDEO](https://video.tv.adobe.com/v/28878)
