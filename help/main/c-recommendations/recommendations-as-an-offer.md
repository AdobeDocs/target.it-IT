---
keywords: Recommendations;consigli;offerta
description: Scopri come utilizzare Adobe Recommendations come offerta all’interno di test A/B (tra cui Allocazione automatica e Targeting automatico) e attività di targeting delle esperienze (XT).
title: Come si utilizza la funzione Recommendations (Consigli) come offerta in altri tipi di attività?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
exl-id: ec520555-b439-46a9-ab2d-f0981532bffb
TQID: 'https://experienceleague.adobe.com/ZMOb5RdY6bES331INSM7VF-w4be-5Xmjqon0YvfuNG4'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 12%
---
# Consigli come offerta {#recommendations-as-an-offer}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come aggiungere, modificare ed eliminare un consiglio come offerta nelle attività [!UICONTROL Test A/B] e [!UICONTROL Targeting esperienza] (XT).

>[!ENDSHADEBOX]

Oltre alle attività [!UICONTROL Consigli], i consigli possono essere inclusi nelle attività [!UICONTROL Test A/B] (tra cui [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico]) e [!UICONTROL Targeting esperienza] (XT). Ciò consente di:

* Contenuto relativo e non relativo a consigli di test e targeting all’interno della stessa attività.
* Prova a inserire i consigli nella pagina, incluso l’ordine di più consigli.
* Invio automatico di traffico all&#39;esperienza di consigli con le prestazioni migliori con **[!UICONTROL Allocazione automatica]**.
* Assegnazione dinamica di visitatori a esperienze di consigli su misura in base al loro profilo con **[!UICONTROL Targeting automatico]**.

## Aggiungere un consiglio come offerta {#add-recs-offer}

Un consiglio viene aggiunto come offerta durante la creazione di un&#39;esperienza con il [!UICONTROL Compositore esperienza visivo] in un&#39;attività [!UICONTROL Test A/B] o XT.

1. Avvia il flusso di lavoro guidato in tre passaggi del Compositore esperienza visivo per creare un&#39;attività [Test A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) o [Targeting esperienza](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md) (XT).

   >[!NOTE]
   >
   >Per i test A/B, l&#39;opzione [Allocazione automatica](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) invia automaticamente il traffico ai consigli con prestazioni migliori e l&#39;opzione [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md) assegna esperienze di consigli su misura ai visitatori in base al loro profilo.

1. Durante la creazione di una [esperienza](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md), aggiungi il consiglio come offerta in uno dei seguenti modi:

   * Fai clic sull&#39;elemento a cui viene aggiunto il consiglio, fai clic su **[!UICONTROL Sostituisci contenuto]**, quindi seleziona **[!UICONTROL Consiglio]**.

     ![Compositore esperienza visivo con un&#39;intestazione selezionata e l&#39;opzione Consiglio evidenziata nel menu, accanto alle opzioni Offerta HTML e Frammento esperienza](/help/main/c-recommendations/t-create-recs-activity/assets/recs-as-offer.png)

   * Nella barra **[!UICONTROL Componenti]**, seleziona **[!UICONTROL Consiglio]** in **[!UICONTROL Dinamico]**, passa il puntatore del mouse su un elemento esistente nella pagina, quindi fai clic su **[!UICONTROL Inserisci prima]** o **[!UICONTROL Inserisci dopo]** per inserire il consiglio prima o dopo tale elemento.

1. Accedi al menu **[!UICONTROL Mostra proprietà]** e fai clic su **[!UICONTROL Seleziona un consiglio]**.

1. Seleziona i [criteri](/help/main/c-recommendations/c-algorithms/algorithms.md) desiderati, quindi fai clic su **[!UICONTROL Successivo]**.

1. Seleziona la [progettazione](/help/main/c-recommendations/c-design-overview/design-overview.md) desiderata, quindi fai clic su **[!UICONTROL Avanti]**.

1. Nella finestra di dialogo **[!UICONTROL Opzioni]**, specifica quanto segue:

   * Scegli una [raccolta](/help/main/c-recommendations/c-products/collections.md).
   * Se necessario, configura le opzioni [Promozione prima e Promozione dopo](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md).

1. Fai clic su **[!UICONTROL Salva]**.

1. Completa la configurazione dell&#39;attività [!UICONTROL Test A/B] o XT con il flusso di lavoro guidato in tre passaggi.

## Modificare un’offerta di consigli {#edit-recs-offer}

Dopo l&#39;aggiunta dell&#39;offerta è possibile modificare i criteri, la progettazione, la raccolta e le promozioni di un&#39;offerta di consigli dal riquadro **[!UICONTROL Consigli]**.

1. Fai clic sull’offerta da modificare e sfoglia le opzioni nel menu del riquadro a destra.

   ![Riquadro dei consigli con i nomi dei criteri, della struttura e della raccolta e il pulsante Aggiungi promozione dell&#39;offerta selezionata](assets/create_reco_7.png)

1. Selezionare una delle opzioni seguenti:

   * [Cambia criterio](/help/main/c-recommendations/c-algorithms/algorithms.md)
   * [Cambia design](/help/main/c-recommendations/c-design-overview/design-overview.md)
   * [Cambia raccolta](/help/main/c-recommendations/c-products/collections.md)
   * [Modifica promozione](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md)

1. Apporta le modifiche necessarie.

## Eliminare un’offerta di consigli {#delete-recs-offer}

È possibile eliminare un&#39;offerta di consigli non più necessaria dal riquadro **[!UICONTROL Consigli]**.

Fai clic sull&#39;offerta da rimuovere, quindi fai clic sull&#39;icona del raccoglitore ( ![Icona raccoglitore](assets/Smock_Delete_18_N.svg) ) nel riquadro **[!UICONTROL Consiglio]**.

![Riquadro consigli con l&#39;icona raccoglitore evidenziata](assets/create_reco_8.png)

## Visualizzare lo stato di un’offerta di consigli {#status}

Lo stato dell&#39;offerta (algoritmo) di consigli viene visualizzato nella parte inferiore della pagina **[!UICONTROL Panoramica]** per le attività [!UICONTROL Test A/B] e Targeting esperienze che contengono offerte di consigli. Lo stato è uno dei seguenti:

* **[!UICONTROL Risultati pronti]**
* **[!UICONTROL Risultati non pronti]**
* **[!UICONTROL Errore di feed]**

## Video di formazione: Recommendations (Consigli) come offerta ![Icona Panoramica](/help/main/assets/overview.png)

>[!VIDEO](https://video.tv.adobe.com/v/28878)
