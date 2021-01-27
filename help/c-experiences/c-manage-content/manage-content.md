---
keywords: content;assets;manage content;offers;manage assets;enter selection mode;selection mode
description: Come si gestiscono le offerte di codice e immagini?
title: Offerte
feature: Experiences and Offers
translation-type: tm+mt
source-git-commit: 70547a05155aa2909b0e66a1f26b0fd2cc730dd9
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 39%

---


# Offerte

Utilizzate la libreria [!UICONTROL Offerte] in [!DNL Adobe Target] per gestire l&#39;offerta di codice e il contenuto dell&#39;offerta di immagini.

1. Fai clic su **[!UICONTROL Offerte]** per aprire la libreria.

   La libreria contiene le offerte che sono state impostate tramite [!DNL Target Standard/Premium], [!DNL Target Classic], [!DNL Adobe Experience Manager] (AEM), [!DNL Adobe Mobile Services] (AMS) e API. Le offerte create in [!DNL Target Classic] o altre soluzioni sono modificabili in [!DNL Target Standard/Premium].

   La pagina [!UICONTROL Offerte] ha due schede sul lato destro: [!UICONTROL Offerte di codice] e [!UICONTROL Offerte di immagini] che consentono di visualizzare le offerte per tipo.

   ![Pagina delle offerte con le schede Offerte codice e Offerte immagine](/help/c-experiences/c-manage-content/assets/offers-page.png)

1. (Facoltativo) Fate clic sull&#39;elenco a discesa **[!UICONTROL Tipo]** per filtrare le offerte per tipo (Offerta HTML, [Frammenti esperienza](/help/c-experiences/c-manage-content/aem-experience-fragments.md), [Offerta di reindirizzamento](/help/c-experiences/c-manage-content/offer-redirect.md), [Offerta remota](/help/c-experiences/c-manage-content/about-remote-offers.md), [Offerte JSON](/help/c-experiences/c-manage-content/create-json-offer.md) e [Cartelle&lt;a 11/>).](/help/c-experiences/c-manage-content/create-content-folder.md)

   ![](assets/offers_filter.png)

1. (Facoltativo) Fate clic sull&#39;elenco a discesa **[!UICONTROL Origine]** per filtrare le offerte per origine ( Adobe Target,  Adobe Target Classic e Adobe Experience Manager).

1. (Facoltativo) Per eseguire altre attività, passare il puntatore sull&#39;offerta o sulla cartella desiderata nella scheda [!UICONTROL Code Offers], quindi fare clic sull&#39;icona desiderata.

   ![Opzioni Offerte codice](assets/offer-picker-large.png)

   Le opzioni includono:

   * Visualizza (per ulteriori informazioni, vedere [Visualizzazione delle definizioni delle offerte](#section_6B059DD121434E6292CAB393507D010E) di seguito.)
   * Modifica
   * Copia
   * Sposta (ad esempio, per spostare uno o più elementi in una cartella, fare clic sull&#39;icona **[!UICONTROL Sposta]** per l&#39;elemento desiderato, fare clic sulla cartella desiderata, quindi fare clic su **[!UICONTROL Rilascia]**).
   * Elimina

   A seconda delle autorizzazioni, potrebbero non essere visualizzate le icone per tutte le opzioni. Ad esempio, un utente con autorizzazioni [!UICONTROL Observer] non dispone dei diritti per utilizzare l&#39;opzione [!UICONTROL Copia].

1. (Facoltativo) Per eseguire ulteriori operazioni, passare il puntatore del mouse sull&#39;offerta o sulla cartella di immagini desiderata nella scheda [!UICONTROL Offerte immagine], quindi fare clic sull&#39;icona desiderata.

   ![Opzioni Offerte immagine](/help/c-experiences/c-manage-content/assets/image-offers-icons.png)

   Le opzioni includono:

   * Seleziona
   * Scarica
   * View Properties (Visualizza proprietà)
   * Modifica
   * Annota
   * Copia

## Visualizzazione delle definizioni delle offerte {#section_6B059DD121434E6292CAB393507D010E}

Potete visualizzare i dettagli delle definizioni delle offerte su una scheda a comparsa nella libreria [!UICONTROL Offerte] senza aprire l&#39;offerta.

Ad esempio, la seguente scheda di definizione delle offerte per un&#39;offerta HTML è accessibile passando il puntatore del mouse su un&#39;offerta nell&#39;elenco [!UICONTROL Content], quindi facendo clic sull&#39;icona delle informazioni:

![](assets/offer-card-html.png)

Sono disponibili le seguenti informazioni:

* Nome
* Origine
* Tipo
* ID offerta
* Percorso offerta
* Ultima modifica

Fai clic sulla scheda [!UICONTROL Utilizzo offerta] per visualizzare le attività che fanno riferimento a un’offerta di codice nella scheda a comparsa della definizione di ogni offerta. Questa funzionalità non è applicabile alle offerte di immagine. In questo modo puoi evitare un impatto su altre attività mentre modifichi le offerte. Le informazioni includono [!UICONTROL Live Activities] e [!UICONTROL Inactive Activities].

![](assets/offer-card-usage.png)

Di seguito è illustrata la scheda di definizione di un’offerta di reindirizzamento:

![](assets/offer-card-redirect.png)

Sono disponibili le seguenti informazioni:

* Nome
* Origine
* Tipo
* ID offerta
* Percorso offerta
* Ultima modifica
* URL di reindirizzamento
* Includi tutti i parametri URL (attivato o disattivato)
* ID sessione mbox trasmissione (attivato o disattivato)

Di seguito è illustrata la scheda di definizione di un’offerta remota:

![](assets/offer-card-remote.png)

Sono disponibili le seguenti informazioni:

* Nome
* Origine
* Tipo
* ID offerta
* Percorso offerta
* Ultima modifica
* Tipo di URL di reindirizzamento
* URL assoluto o relativo

## Video di formazione: L’archivio dei contenuti  ![badge Panoramica](/help/assets/overview.png)

Questo video include informazioni sulla gestione delle offerte.

* Connessione tra la [libreria delle risorse di Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/assets/creative-cloud.html) e la libreria dei contenuti di Target
* Offerte HTML personalizzate
* Offerta HTML personalizzata nel Compositore esperienza visivo

>[!VIDEO](https://video.tv.adobe.com/v/17387)