---
keywords: contenuto;risorse;gestione contenuto;offerte;gestione risorse;inserire modalità selezione;modalità di selezione
description: Scopri come gestire le offerte di codice e immagini utilizzando la libreria Offerte.
title: Come posso gestire le offerte di codice e immagini?
feature: Experiences and Offers
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#beta newtab=true" tooltip="Cosa sono le funzioni beta in [!DNL Adobe Target]."
hide: true
hidefromtoc: true
exl-id: f64aec3d-5f83-4bd1-8e64-df1779809812
source-git-commit: 646472f35ef4623666545f9945255d61bfe16073
workflow-type: tm+mt
source-wordcount: '600'
ht-degree: 29%

---

# Offerte

Utilizza il [!UICONTROL Offers] libreria in [!DNL Adobe Target] per gestire il contenuto delle offerte basate su codice e su immagine.

>[!NOTE]
>
>Questo articolo contiene informazioni sugli aggiornamenti di [!DNL Target] che fa attualmente parte di un programma beta. Il [!DNL Adobe Target] team abilita spesso nuove funzioni per determinati clienti a scopo di test e feedback. Al termine del periodo di test, queste funzioni saranno abilitate per tutti i clienti in futuro [!DNL Target Standard/Premium] e annunciate nelle note sulla versione.

1. Clic **[!UICONTROL Offers]** per aprire la libreria.

   La libreria contiene le offerte che sono state impostate tramite [!DNL Target Standard/Premium], [!DNL Target Classic], [!DNL Adobe Experience Manager] (AEM), [!DNL Adobe Mobile Services] (AMS) e API. Le offerte create in [!DNL Target Classic] o altre soluzioni sono modificabili in [!DNL Target Standard/Premium].

   Il [!UICONTROL Offers] La pagina presenta due schede lungo il lato destro: [!UICONTROL Code Offers] e [!UICONTROL Image Offers] che ti consente di visualizzare le offerte per tipo.

   ![Pagina Offerte con le schede Offerte codice e Offerte immagine](/help/main/c-experiences/c-manage-content/assets/offers-page.png)

1. (Facoltativo) Fai clic su **[!UICONTROL Type]** elenco a discesa per filtrare le offerte per tipo (Offerta HTML, [Frammenti esperienza](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md), [Offerta di reindirizzamento](/help/main/c-experiences/c-manage-content/offer-redirect.md), [Offerta remota](/help/main/c-experiences/c-manage-content/about-remote-offers.md), [Offerte JSON](/help/main/c-experiences/c-manage-content/create-json-offer.md), e [Cartelle](/help/main/c-experiences/c-manage-content/create-content-folder.md)).

   ![immagine offers_filter](assets/offers_filter.png)

1. (Facoltativo) Fai clic su **[!UICONTROL Source]** per filtrare le offerte per origine (Adobe Target, Adobe Target Classic e Adobe Experience Manager).

1. (Facoltativo) Esegui altre attività passando il cursore sull’offerta o sulla cartella desiderata nella sezione [!UICONTROL Code Offers] , quindi facendo clic sull&#39;icona desiderata.

   ![Opzioni Offerte codice](assets/offer-picker-large.png)

   Le opzioni includono:

   * Visualizza (per ulteriori informazioni, vedere [Visualizzazione delle definizioni delle offerte](#section_6B059DD121434E6292CAB393507D010E) di seguito.)
   * Modifica
   * Copia
   * Sposta (ad esempio, per spostare uno o più elementi in una cartella, fare clic sul pulsante **[!UICONTROL Move]** per l’elemento desiderato, fai clic sulla cartella desiderata, quindi fai clic su **[!UICONTROL Drop]**.)
   * Elimina

   A seconda delle autorizzazioni, è possibile che non vengano visualizzate le icone per tutte le opzioni. Ad esempio, un utente con [!UICONTROL Observer] autorizzazioni non dispone dei diritti per utilizzare il [!UICONTROL Copy] opzione.

   Per informazioni dettagliate sulle attività eseguibili su offerte e cartelle, consulta [Utilizzare i contenuti della libreria di risorse](/help/main/c-experiences/c-manage-content/assets-working.md).

1. (Facoltativo) Esegui altre attività passando il cursore sull&#39;offerta o la cartella di immagine desiderata sul [!UICONTROL Image Offers] , quindi facendo clic sull&#39;icona desiderata.

   ![Opzioni Offerte immagine](/help/main/c-experiences/c-manage-content/assets/image-offers-icons.png)

   Le opzioni includono:

   * Seleziona
   * Scarica
   * View Properties (Visualizza proprietà)
   * Modifica
   * Annota
   * Copia

   Per informazioni dettagliate sulle attività eseguibili su offerte e cartelle, consulta [Utilizzare i contenuti della libreria di risorse](/help/main/c-experiences/c-manage-content/assets-working.md).

   >[!NOTE]
   >
   >Le offerte di immagini non fanno parte del [Autorizzazioni per gli utenti Enterprise](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) modello.


## Visualizzazione delle definizioni delle offerte {#section_6B059DD121434E6292CAB393507D010E}

Puoi visualizzare i dettagli della definizione dell’offerta su una scheda a comparsa in [!UICONTROL Offers] senza aprire l’offerta.

Ad esempio, per accedere alla scheda di definizione dell’offerta seguente per un’offerta HTML, passa il puntatore del mouse su un’offerta nella [!UICONTROL Content] , quindi facendo clic sull&#39;icona delle informazioni:

![immagine offer-card-html](assets/offer-card-html.png)

Sono disponibili le seguenti informazioni:

* Nome
* Origine
* Tipo
* ID offerta
* Percorso offerta
* Ultima modifica

Fai clic su [!UICONTROL Offer Usage] per visualizzare le attività che fanno riferimento a un’offerta di codice nella scheda a comparsa di definizione di ogni offerta. Questa funzionalità non è applicabile alle offerte di immagine. In questo modo puoi evitare un impatto su altre attività mentre modifichi le offerte. Le informazioni includono [!UICONTROL Live Activities] e [!UICONTROL Inactive Activities].

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

## Video di formazione: L’archivio dei contenuti ![Badge panoramica](/help/main/assets/overview.png)

Questo video include informazioni sulla gestione delle offerte.

* Connessione tra la [libreria delle risorse di Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/assets/creative-cloud.html) e la libreria dei contenuti di Target
* Offerte HTML personalizzate
* Offerta HTML personalizzata nel Compositore esperienza visivo

>[!VIDEO](https://video.tv.adobe.com/v/17387)
