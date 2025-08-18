---
keywords: contenuto;risorse;gestione contenuto;offerte;gestione risorse;inserire modalità selezione;modalità di selezione
description: Scopri come gestire le offerte di codice e immagini utilizzando la libreria Offerte di Adobe Target.
title: Come posso gestire le offerte di codice e immagini?
feature: Experiences and Offers
exl-id: d8c24656-64d6-4a4b-a5f2-bcde57180007
source-git-commit: e8201198dc6ac36e803153d5c6b345a30716204a
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 15%

---

# Offerte

Utilizza la libreria [!UICONTROL Offers] in [!DNL Adobe Target] per gestire il contenuto dell&#39;offerta codice e dell&#39;offerta immagine.

1. Fare clic su **[!UICONTROL Offers]** per aprire la libreria.

   La libreria contiene le offerte che sono state impostate tramite [!DNL Target Standard/Premium], [!DNL Target Classic], [!DNL Adobe Experience Manager] (AEM), [!DNL Adobe Mobile Services] (AMS) e API. Le offerte create in [!DNL Target Classic] o altre soluzioni sono modificabili in [!DNL Target Standard/Premium].

   La pagina [!UICONTROL Offers] presenta due schede lungo il lato destro: [!UICONTROL Code Offers] e [!UICONTROL Image Offers] che consentono di visualizzare le offerte per tipo.

   ![Pagina Offerte contenente le schede Offerte codice e Offerte immagine](/help/main/c-experiences/c-manage-content/assets/offers-page.png)

1. (Facoltativo) Fai clic sull&#39;elenco a discesa **[!UICONTROL Type]** per filtrare le offerte per tipo (Offerta HTML, [Frammenti di esperienza](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md), [Offerta di reindirizzamento](/help/main/c-experiences/c-manage-content/offer-redirect.md), [Offerta remota](/help/main/c-experiences/c-manage-content/about-remote-offers.md), [Offerte JSON](/help/main/c-experiences/c-manage-content/create-json-offer.md) e [Cartelle](/help/main/c-experiences/c-manage-content/create-content-folder.md)).

   ![immagine_filtro offerte](assets/offers_filter.png)

1. (Facoltativo) Fai clic sull&#39;elenco a discesa **[!UICONTROL Source]** per filtrare le offerte per origine (Adobe Target, Adobe Target Classic e Adobe Experience Manager).

1. (Facoltativo) Eseguire altre attività passando il mouse sull&#39;offerta o sulla cartella desiderata nella scheda [!UICONTROL Code Offers] e facendo clic sull&#39;icona desiderata.

   ![Opzioni offerte codice](assets/offer-picker-large.png)

   Le opzioni includono:

   * Visualizza (per ulteriori informazioni, vedi [Visualizzazione delle definizioni delle offerte](#section_6B059DD121434E6292CAB393507D010E) di seguito.)
   * Modifica
   * Copia
   * Sposta (ad esempio, per spostare uno o più elementi in una cartella, fare clic sull&#39;icona **[!UICONTROL Move]** dell&#39;elemento desiderato, fare clic sulla cartella desiderata, quindi fare clic su **[!UICONTROL Drop]**.)
   * Elimina

   A seconda delle autorizzazioni, è possibile che non vengano visualizzate le icone per tutte le opzioni. Ad esempio, un utente con autorizzazioni [!UICONTROL Observer] non dispone dei diritti per utilizzare l&#39;opzione [!UICONTROL Copy].

   Per informazioni dettagliate sulle attività che è possibile eseguire su offerte e cartelle, vedi [Operazioni con il contenuto della libreria di risorse](/help/main/c-experiences/c-manage-content/assets-working.md).

1. (Facoltativo) Eseguire altre attività passando il mouse sull&#39;offerta o sulla cartella di immagine desiderata nella scheda [!UICONTROL Image Offers] e facendo clic sull&#39;icona desiderata.

   ![Opzioni offerte immagini](/help/main/c-experiences/c-manage-content/assets/image-offers-icons.png)

   Le opzioni includono:

   * Seleziona
   * Scarica
   * View Properties (Visualizza proprietà)
   * Modifica
   * Annota
   * Copia

   Per informazioni dettagliate sulle attività che è possibile eseguire su offerte e cartelle, vedi [Operazioni con il contenuto della libreria di risorse](/help/main/c-experiences/c-manage-content/assets-working.md).

   >[!NOTE]
   >
   >Le offerte di immagini non fanno parte del modello [Autorizzazioni utente Enterprise](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).


## Visualizzazione delle definizioni delle offerte {#section_6B059DD121434E6292CAB393507D010E}

È possibile visualizzare i dettagli della definizione dell&#39;offerta in una scheda a comparsa nella libreria [!UICONTROL Offers] senza aprire l&#39;offerta.

Ad esempio, per accedere alla scheda di definizione dell’offerta seguente per un’offerta HTML, fai clic sull’icona delle informazioni:

![immagine html della scheda offerta](assets/offer-card-html-new.png)

Sono disponibili le seguenti informazioni:

* Nome
* ID offerta
* Tipo
* Ultima modifica

Fai clic sul collegamento [!UICONTROL View Full Details] per visualizzare il contenuto dell&#39;offerta e le attività che fanno riferimento a un&#39;offerta codice. In questo modo puoi evitare un impatto su altre attività mentre modifichi le offerte. Le informazioni includono [!UICONTROL Live Activities] e [!UICONTROL Inactive Activities].

Le informazioni disponibili su ogni scheda variano a seconda del tipo di offerta: Offerta HTML, [Frammenti di esperienza](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md), [Offerta di reindirizzamento](/help/main/c-experiences/c-manage-content/offer-redirect.md), [Offerta remota](/help/main/c-experiences/c-manage-content/about-remote-offers.md) o [Offerte JSON](/help/main/c-experiences/c-manage-content/create-json-offer.md).

La funzionalità dettagli offerta non è applicabile alle offerte di immagini.

<!--

## Training video: The Content Repository ![Overview badge](/help/main/assets/overview.png)

This video includes information about managing offers.

* Connection between the [Experience Cloud Asset Library](https://experienceleague.adobe.com/docs/core-services/interface/assets/creative-cloud.html) and the Target Content Library 
* Custom HTML Offers 
* Custom HTML Offer in the [!UICONTROL Visual Experience Composer]

>[!VIDEO](https://video.tv.adobe.com/v/17387)

-->
