---
keywords: Recommendations;consigli;offerta
description: Scopri come utilizzare Adobe Recommendations come offerta all’interno di test A/B (tra cui Allocazione automatica e Targeting automatico) e attività di Experience Targeting (XT).
title: Come si utilizza la funzione Recommendations (Consigli) come offerta in altri tipi di attività?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
hide: true
hidefromtoc: true
source-git-commit: 3821d868f45b85d2f6f0e204f9828544b759067b
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 47%

---

# Consigli come offerta

È ora possibile includere i consigli nelle attività [!UICONTROL A/B Test] (inclusi [!UICONTROL Auto-Allocate] e [!UICONTROL Auto-Target]) e [!UICONTROL Experience Targeting] (XT).

Questo apre a funzionalità tutte nuove, ad esempio:

* Contenuto relativo e non relativo a consigli di test e targeting all’interno della stessa attività.
* Facile sperimentazione con il posizionamento di consigli sulla pagina, incluso l’ordine di più consigli.
* Invio automatico di traffico all&#39;esperienza di consigli con le prestazioni migliori tramite [!UICONTROL Auto-Allocate].
* Assegnazione dinamica di visitatori a esperienze di consigli su misura in base al loro profilo tramite [!UICONTROL Auto-Target].

Per iniziare, crea un&#39;attività [!UICONTROL A/B Test] o [!UICONTROL Experience Targeting] utilizzando [!UICONTROL Visual Experience Composer] e utilizza l&#39;azione [!UICONTROL Recommend] per aggiungere consigli a un&#39;esperienza.

## Aggiungere un Consiglio come offerta in un’attività di test A/B o XT

1. Avvia il flusso di lavoro guidato in tre passaggi utilizzando il Compositore esperienza visivo per creare un’attività [Test A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) o [Targeting delle esperienze](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md) (XT).

   >[!NOTE]
   >
   >Per i test A/B, ricorda che puoi scegliere l’opzione [Allocazione automatica](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) per inviare automaticamente il traffico ai consigli con prestazioni migliori, oppure l’opzione [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md) per assegnare esperienze di consigli su misura ai visitatori in base ai loro profili.

1. Durante la creazione di una [esperienza](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md), fai clic sull&#39;elemento a cui desideri aggiungere un consiglio come offerta, fai clic su **[!UICONTROL Replace Content]** ( ![icona Sostituisci contenuto](/help/main/assets/icons/Switch.svg) ), quindi seleziona **[!UICONTROL Recommendation]**.

   ![Inserire un Consiglio come offerta](/help/main/c-recommendations/t-create-recs-activity/assets/recs-as-offer.png)

1. Dalla barra [!UICONTROL Recommendation] sul lato destro, fare clic su **[!UICONTROL Select a Recommendation]** per visualizzare la finestra di dialogo [!UICONTROL Select Criteria].

1. Fare clic su **[!UICONTROL Create Criteria]** o selezionare un criterio esistente.

1. (Facoltativo) Fai clic sull&#39;icona **[!UICONTROL Filter]** ( ![icona Filtro](/help/main/assets/icons/Filter.svg) ) per selezionare una delle seguenti opzioni per visualizzare i criteri dei consigli più comuni per tipo di pagina:

   * Pagina del carrello
   * Pagina categoria
   * Home page
   * Pagina di destinazione
   * Pagina di prodotto
   * Pagina risultati di ricerca
   * Pagina di ringraziamento
   * Altro

1. Fai clic su **[!UICONTROL Create Criteria]** o seleziona un [criterio](/help/main/c-recommendations/c-algorithms/algorithms.md) esistente, quindi fai clic su **[!UICONTROL Next]** per visualizzare la finestra di dialogo [!UICONTROL Select Design].

1. Fai clic su **[!UICONTROL Create Design]** o seleziona una [progettazione](/help/main/c-recommendations/c-design-overview/design-overview.md) esistente, quindi fai clic su **[!UICONTROL &#x200B; Next]**.

1. Nella finestra di dialogo [!UICONTROL Options], specificare quanto segue:

   * Scegli una [raccolta](/help/main/c-recommendations/c-products/collections.md).
   * Configura le opzioni [Promozione prima e Promozione dopo](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md), a seconda delle necessità.

1. Fare clic su **[!UICONTROL Save]**.
1. Completa la configurazione dell’attività di test A/B o XT utilizzando il flusso di lavoro guidato in tre parti.

## Modificare la configurazione di un’offerta di consigli

1. Dalla barra [!UICONTROL Recommendation], fai clic sull&#39;icona **[!UICONTROL Edit]** ( ![icona Modifica](/help/main/assets/icons/Edit.svg) ) accanto a [!UICONTROL Criteria Name], [!UICONTROL Design Name] o [!UICONTROL Collection Name] per modificare l&#39;elemento.

## Eliminare un’offerta di consigli

1. Fai clic sull&#39;icona **[!UICONTROL Delete]** ( ![icona Elimina](/help/main/assets/icons/Delete.svg) ) nella parte superiore del pannello [!UICONTROL Recommendation].

### Visualizzazione dello stato di un’offerta Consigli {#status}

Lo stato di offerte (algoritmo) di tipo Consigli viene visualizzato nella parte inferiore della pagina [!UICONTROL Overview] dell&#39;attività per le attività Test A/B e Targeting esperienze che contengono offerte di tipo Consigli:

* Risultati pronti
* Risultati non pronti
* Errore di feed
