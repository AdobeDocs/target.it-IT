---
keywords: contenuto;risorse;gestione contenuto;offerte;gestione risorse;inserire modalità selezione;modalità di selezione
description: Scopri come gestire le offerte di codice e immagini utilizzando la libreria Offerte di Adobe Target.
title: Come posso gestire le offerte di codice e immagini?
feature: Experiences and Offers
exl-id: d8c24656-64d6-4a4b-a5f2-bcde57180007
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '563'
ht-degree: 36%

---

# Offerte

Utilizza il [!UICONTROL Offerte] libreria in [!DNL Adobe Target] per gestire il contenuto delle offerte basate su codice e su immagine.

1. Fai clic su **[!UICONTROL Offerte]** per aprire la libreria.

   La libreria contiene le offerte che sono state impostate tramite [!DNL Target Standard/Premium], [!DNL Target Classic], [!DNL Adobe Experience Manager] (AEM), [!DNL Adobe Mobile Services] (AMS) e API. Le offerte create in [!DNL Target Classic] o altre soluzioni sono modificabili in [!DNL Target Standard/Premium].

   Il [!UICONTROL Offerte] La pagina presenta due schede lungo il lato destro: [!UICONTROL Offerte di codice] e [!UICONTROL Offerte immagine] che ti consente di visualizzare le offerte per tipo.

   ![Pagina Offerte con le schede Offerte codice e Offerte immagine](/help/main/c-experiences/c-manage-content/assets/offers-page.png)

1. (Facoltativo) Fai clic su **[!UICONTROL Tipo]** elenco a discesa per filtrare le offerte per tipo (Offerta HTML, [Frammenti esperienza](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md), [Offerta di reindirizzamento](/help/main/c-experiences/c-manage-content/offer-redirect.md), [Offerta remota](/help/main/c-experiences/c-manage-content/about-remote-offers.md), [Offerte JSON](/help/main/c-experiences/c-manage-content/create-json-offer.md), e [Cartelle](/help/main/c-experiences/c-manage-content/create-content-folder.md)).

   ![immagine offers_filter](assets/offers_filter.png)

1. (Facoltativo) Fai clic su **[!UICONTROL Sorgente]** per filtrare le offerte per origine (Adobe Target, Adobe Target Classic e Adobe Experience Manager).

1. (Facoltativo) Esegui altre attività passando il cursore sull’offerta o sulla cartella desiderata nella sezione [!UICONTROL Offerte di codice] , quindi facendo clic sull&#39;icona desiderata.

   ![Opzioni Offerte codice](assets/offer-picker-large.png)

   Le opzioni includono:

   * Visualizza (per ulteriori informazioni, vedere [Visualizzazione delle definizioni delle offerte](#section_6B059DD121434E6292CAB393507D010E) di seguito.)
   * Modifica
   * Copia
   * Sposta (ad esempio, per spostare uno o più elementi in una cartella, fare clic sul pulsante **[!UICONTROL Sposta]** per l’elemento desiderato, fai clic sulla cartella desiderata, quindi fai clic su **[!UICONTROL Rilascia]**.)
   * Elimina

   A seconda delle autorizzazioni, è possibile che non vengano visualizzate le icone per tutte le opzioni. Ad esempio, un utente con [!UICONTROL Osservatore] autorizzazioni non dispone dei diritti per utilizzare il [!UICONTROL Copia] opzione.

   Per informazioni dettagliate sulle attività eseguibili su offerte e cartelle, consulta [Utilizzare i contenuti della libreria di risorse](/help/main/c-experiences/c-manage-content/assets-working.md).

1. (Facoltativo) Esegui altre attività passando il cursore sull&#39;offerta o la cartella di immagine desiderata sul [!UICONTROL Offerte immagine] , quindi facendo clic sull&#39;icona desiderata.

   ![Opzioni Offerte immagine](/help/main/c-experiences/c-manage-content/assets/image-offers-icons.png)

   Le opzioni includono:

   * Seleziona
   * Scarica
   * View Properties (Visualizza proprietà)
   * Modifica
   * Annota
   * Copia

   Per informazioni dettagliate sulle attività eseguibili su offerte e cartelle, consulta [Utilizzare i contenuti della libreria di risorse](/help/main/c-experiences/c-manage-content/assets-working.md).

## Visualizzazione delle definizioni delle offerte {#section_6B059DD121434E6292CAB393507D010E}

Puoi visualizzare i dettagli della definizione dell’offerta su una scheda a comparsa in [!UICONTROL Offerte] senza aprire l’offerta.

Ad esempio, per accedere alla scheda di definizione dell’offerta seguente per un’offerta HTML, passa il puntatore del mouse su un’offerta nella [!UICONTROL Contenuto] , quindi facendo clic sull&#39;icona delle informazioni:

![immagine offer-card-html](assets/offer-card-html.png)

Sono disponibili le seguenti informazioni:

* Nome
* Origine
* Tipo
* ID offerta
* Percorso offerta
* Ultima modifica

Fai clic sulla scheda [!UICONTROL Utilizzo offerta] per visualizzare le attività che fanno riferimento a un’offerta di codice nella scheda a comparsa della definizione di ogni offerta. Questa funzionalità non è applicabile alle offerte di immagine. In questo modo puoi evitare un impatto su altre attività mentre modifichi le offerte. Le informazioni includono [!UICONTROL Attività live] e [!UICONTROL Attività inattive].

![immagine offer-card-usage](assets/offer-card-usage.png)

Di seguito è illustrata la scheda di definizione di un’offerta di reindirizzamento:

![immagine offer-card-redirect](assets/offer-card-redirect.png)

Sono disponibili le seguenti informazioni:

* Nome
* Origine
* Tipo
* ID offerta
* Percorso offerta
* Ultima modifica
* URL di reindirizzamento
* Includi tutti i parametri URL (attivato o disattivato)
* Passa ID sessione mbox (attivato o disattivato)

Di seguito è illustrata la scheda di definizione di un’offerta remota:

![immagine remota offer-card-remote](assets/offer-card-remote.png)

Sono disponibili le seguenti informazioni:

* Nome
* Origine
* Tipo
* ID offerta
* Percorso offerta
* Ultima modifica
* Tipo di URL di reindirizzamento
* URL assoluto o relativo

## Video di formazione: L’archivio dei contenuti ![Icona Panoramica](/help/main/assets/overview.png)

Questo video include informazioni sulla gestione delle offerte.

* Connessione tra la [libreria delle risorse di Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/assets/creative-cloud.html) e la libreria dei contenuti di Target
* Offerte HTML personalizzate
* Offerta HTML personalizzata nel Compositore esperienza visivo

>[!VIDEO](https://video.tv.adobe.com/v/17387)
