---
keywords: Recommendations;consigli;offerta
description: Scopri come utilizzare Adobe Recommendations come offerta all’interno di test A/B (tra cui Allocazione automatica e Targeting automatico) e attività di targeting delle esperienze (XT).
title: Come si utilizza la funzione Recommendations (Consigli) come offerta in altri tipi di attività?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
hide: true
hidefromtoc: true
source-git-commit: f6034e83564a9a386e21e4e57279c66cc3c94537
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 42%

---

# Consigli come offerta

Ora puoi includere consigli all&#39;interno di [!UICONTROL Test A/B] (tra cui [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico]) e [!UICONTROL Attività Targeting esperienza] (XT).

Questo apre a funzionalità tutte nuove, ad esempio:

* Contenuto relativo e non relativo a consigli di test e targeting all’interno della stessa attività.
* Facile sperimentazione con il posizionamento di consigli sulla pagina, incluso l’ordine di più consigli.
* Invio automatico di traffico all&#39;esperienza di consigli con le prestazioni migliori tramite [!UICONTROL Allocazione automatica].
* Assegnazione dinamica di visitatori a esperienze di consigli su misura in base al loro profilo tramite [!UICONTROL Targeting automatico].

Per iniziare, crea un&#39;attività [!UICONTROL Test A/B] o [!UICONTROL Targeting esperienza] utilizzando [!UICONTROL Compositore esperienza visivo] e utilizza l&#39;azione [!UICONTROL Consiglia] per aggiungere consigli a un&#39;esperienza.

## Aggiungere un Consiglio come offerta in un’attività di test A/B o XT

1. Avvia il flusso di lavoro guidato in tre passaggi utilizzando il Compositore esperienza visivo per creare un’attività [Test A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) o [Targeting delle esperienze](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md) (XT).

   >[!NOTE]
   >
   >Per i test A/B, ricorda che puoi scegliere l’opzione [Allocazione automatica](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) per inviare automaticamente il traffico ai consigli con prestazioni migliori, oppure l’opzione [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md) per assegnare esperienze di consigli su misura ai visitatori in base ai loro profili.

1. Durante la creazione di una [esperienza](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md), fai clic sull&#39;elemento a cui desideri aggiungere un consiglio come offerta, fai clic su **[!UICONTROL Sostituisci contenuto]** ( ![Icona Sostituisci contenuto](/help/main/assets/icons/Switch.svg) ), quindi seleziona **[!UICONTROL Consiglio]**.

   ![Inserire un Consiglio come offerta](/help/main/c-recommendations/t-create-recs-activity/assets/recs-as-offer.png)

1. Dalla barra [!UICONTROL Consigli] sul lato destro, fai clic su **[!UICONTROL Seleziona un consiglio]** per visualizzare la finestra di dialogo [!UICONTROL Seleziona criteri].

1. Fai clic su **[!UICONTROL Crea criterio]** o seleziona un criterio esistente.

1. (Facoltativo) Fai clic sull&#39;icona **[!UICONTROL Filtro]** ( ![Icona Filtro](/help/main/assets/icons/Filter.svg) ) per scegliere tra le seguenti opzioni per visualizzare i criteri dei consigli più comuni per tipo di pagina:

   * Pagina del carrello
   * Pagina categoria
   * Home page
   * Pagina di destinazione
   * Pagina di prodotto
   * Pagina risultati di ricerca
   * Pagina di ringraziamento
   * Altro

1. Fai clic su **[!UICONTROL Crea criterio]** o seleziona un [criterio](/help/main/c-recommendations/c-algorithms/algorithms.md) esistente, quindi fai clic su **[!UICONTROL Successivo]** per visualizzare la finestra di dialogo [!UICONTROL Seleziona design].

1. Fai clic su **[!UICONTROL Crea progettazione]** o seleziona una [progettazione](/help/main/c-recommendations/c-design-overview/design-overview.md) esistente, quindi fai clic su **[!UICONTROL Avanti]**.

1. Nella finestra di dialogo [!UICONTROL Opzioni], specifica quanto segue:

   * Scegli una [raccolta](/help/main/c-recommendations/c-products/collections.md).
   * Configura le opzioni [Promozione prima e Promozione dopo](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md), a seconda delle necessità.

1. Fai clic su **[!UICONTROL Salva]**.
1. Completa la configurazione dell’attività di test A/B o XT utilizzando il flusso di lavoro guidato in tre parti.

## Modificare la configurazione di un’offerta di consigli

1. Dalla barra [!UICONTROL Recommendation], fai clic sull&#39;icona **[!UICONTROL Edit]** ( ![Edit icon](/help/main/assets/icons/Edit.svg) ) accanto a [!UICONTROL Criteria Name], [!UICONTROL Design Name] o [!UICONTROL Collection Name] per modificare l&#39;elemento.

## Eliminare un’offerta di consigli

1. Fai clic sull&#39;icona **[!UICONTROL Elimina]** ( ![Elimina icona](/help/main/assets/icons/Delete.svg) ) nella parte superiore del pannello [!UICONTROL Consigli].

### Visualizzazione dello stato di un’offerta Consigli {#status}

Lo stato di un&#39;offerta (algoritmo) di tipo Consigli viene visualizzato nella parte inferiore della pagina [!UICONTROL Panoramica] dell&#39;attività per le attività Test A/B e Targeting esperienze che contengono offerte di tipo Consigli:

* Risultati pronti
* Risultati non pronti
* Errore di feed
