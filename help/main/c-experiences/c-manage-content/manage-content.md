---
keywords: contenuto;risorse;gestione contenuto;offerte;gestione risorse;inserire modalità selezione;modalità di selezione
description: Scopri come gestire il codice e le offerte di immagini utilizzando la libreria Offerte di Adobe Target.
title: Come posso gestire le offerte di codice e immagine?
feature: Experiences and Offers
exl-id: d8c24656-64d6-4a4b-a5f2-bcde57180007
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '552'
ht-degree: 37%

---

# Offerte

Utilizza la [!UICONTROL Offerte] libreria in [!DNL Adobe Target] per gestire il contenuto dell’offerta di codice e dell’immagine.

1. Fai clic su **[!UICONTROL Offerte]** per aprire la libreria.

   La libreria contiene le offerte che sono state impostate tramite [!DNL Target Standard/Premium], [!DNL Target Classic], [!DNL Adobe Experience Manager] (AEM), [!DNL Adobe Mobile Services] (AMS) e API. Le offerte create in [!DNL Target Classic] o altre soluzioni sono modificabili in [!DNL Target Standard/Premium].

   La [!UICONTROL Offerte] la pagina presenta due schede lungo il lato destro: [!UICONTROL Offerte di codice] e [!UICONTROL Offerte immagine] che consente di visualizzare le offerte per tipo.

   ![Pagina Offerte che mostra le schede Offerte di codice e Offerte di immagine](/help/main/c-experiences/c-manage-content/assets/offers-page.png)

1. (Facoltativo) Fai clic sul pulsante **[!UICONTROL Tipo]** elenco a discesa per filtrare le offerte per tipo (offerta HTML, [Frammenti esperienza](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md), [Offerta di reindirizzamento](/help/main/c-experiences/c-manage-content/offer-redirect.md), [Offerta remota](/help/main/c-experiences/c-manage-content/about-remote-offers.md), [Offerte JSON](/help/main/c-experiences/c-manage-content/create-json-offer.md)e [Cartelle](/help/main/c-experiences/c-manage-content/create-content-folder.md)).

   ![](assets/offers_filter.png)

1. (Facoltativo) Fai clic sul pulsante **[!UICONTROL Origine]** elenco a discesa per filtrare le offerte in base all’origine (Adobe Target, Adobe Target Classic e Adobe Experience Manager).

1. (Facoltativo) Esegui attività aggiuntive passando il cursore sull&#39;offerta o sulla cartella desiderata sul [!UICONTROL Offerte di codice] , quindi facendo clic sull’icona desiderata.

   ![Opzioni Offerte codice](assets/offer-picker-large.png)

   Le opzioni includono:

   * Visualizza (per ulteriori informazioni, consulta [Visualizzazione delle definizioni delle offerte](#section_6B059DD121434E6292CAB393507D010E) qui sotto.)
   * Modifica
   * Copia
   * Sposta (ad esempio, per spostare uno o più elementi in una cartella, fai clic sul pulsante **[!UICONTROL Sposta]** icona per l&#39;elemento desiderato, fare clic sulla cartella desiderata, quindi fare clic **[!UICONTROL Elimina]**.)
   * Elimina

   A seconda delle autorizzazioni, è possibile che non vengano visualizzate icone per tutte le opzioni. Ad esempio, un utente con [!UICONTROL Osservatore] le autorizzazioni non dispongono dei diritti per utilizzare [!UICONTROL Copia] opzione .

   Per informazioni dettagliate sulle attività eseguibili su offerte e cartelle, consulta [Utilizzare i contenuti della libreria Risorse](/help/main/c-experiences/c-manage-content/assets-working.md).

1. (Facoltativo) Esegui ulteriori attività passando il cursore sull&#39;offerta o sulla cartella di immagini desiderata sul [!UICONTROL Offerte immagine] , quindi facendo clic sull’icona desiderata.

   ![Opzioni Offerte immagine](/help/main/c-experiences/c-manage-content/assets/image-offers-icons.png)

   Le opzioni includono:

   * Seleziona
   * Scarica
   * View Properties (Visualizza proprietà)
   * Modifica
   * Annota
   * Copia

   Per informazioni dettagliate sulle attività eseguibili su offerte e cartelle, consulta [Utilizzare i contenuti della libreria Risorse](/help/main/c-experiences/c-manage-content/assets-working.md).

## Visualizzazione delle definizioni delle offerte {#section_6B059DD121434E6292CAB393507D010E}

Puoi visualizzare i dettagli della definizione di un’offerta su una scheda a comparsa nella [!UICONTROL Offerte] libreria senza aprire l’offerta.

Ad esempio, se passi il cursore del mouse su un’offerta nella pagina per accedere alla seguente scheda di definizione dell’offerta per un’offerta HTML [!UICONTROL Contenuto] , quindi facendo clic sull’icona delle informazioni:

![](assets/offer-card-html.png)

Sono disponibili le seguenti informazioni:

* Nome
* Origine
* Tipo
* ID offerta
* Percorso offerta
* Ultima modifica

Fai clic sulla scheda [!UICONTROL Utilizzo offerta] per visualizzare le attività che fanno riferimento a un’offerta di codice nella scheda a comparsa della definizione di ogni offerta. Questa funzionalità non è applicabile alle offerte di immagine. In questo modo puoi evitare un impatto su altre attività mentre modifichi le offerte. Informazioni [!UICONTROL Attività live] e [!UICONTROL Attività inattive].

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
* Passa l&#39;ID della sessione mbox (attivato o disattivato)

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

## Video di formazione: L’archivio dei contenuti ![Icona Panoramica](/help/main/assets/overview.png)

Questo video include informazioni sulla gestione delle offerte.

* Connessione tra la [libreria delle risorse di Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/assets/creative-cloud.html) e la libreria dei contenuti di Target
* Offerte HTML personalizzate
* Offerta HTML personalizzata nel Compositore esperienza visivo

>[!VIDEO](https://video.tv.adobe.com/v/17387)
