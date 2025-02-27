---
keywords: ottimizzazione;personalizzazione;adobe percorsi optimizer;ajo;casi d'uso;scenari;cambiamento di contenuto/test ab;attributo profilo;cambiare immagine;scambiare immagine
description: Sblocca i segreti per le modifiche effettive al contenuto dei test A/B in Adobe Journey Optimizer
title: Modifiche al contenuto tramite test A/B in [!DNL Adobe Journey Optimizer]
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#beta newtab=true" tooltip="Cosa sono le funzioni beta in [!DNL Adobe Target]."
feature: Integrations
hide: true
hidefromtoc: true
exl-id: e5aed7cd-7701-4133-ac7c-98e528c8a763
source-git-commit: b66abe9649f8c257891c1cd8e5736b7f91501c13
workflow-type: tm+mt
source-wordcount: '790'
ht-degree: 1%

---

# Modifiche al contenuto tramite test A/B in [!DNL Adobe Journey Optimizer]

Questo caso d&#39;uso consente di sbloccare i segreti per testare le modifiche effettive al contenuto A/B in [!DNL Adobe Journey Optimizer].

Questo caso d&#39;uso illustra come eseguire attività familiari, ad esempio test A/B con un&#39;attività Test [A/B](/help/main/c-activities/t-test-ab/test-ab.md) in [!DNL Adobe Target], utilizzando [!DNL Journey Optimizer] anziché [!DNL Adobe Target].

## Vantaggi e valore

* **Ottimizza l&#39;efficacia dei contenuti**: scopri quali varianti di contenuto ed elementi risuonano di più con i tuoi clienti, portando a un coinvolgimento e a conversioni più elevati.
* **Decisioni basate sui dati**: sfrutta i dati per prendere decisioni informate in tutta la strategia dei contenuti, garantendo il massimo impatto.
* **Esperienza utente personalizzata**: personalizza il contenuto per soddisfare le preferenze e le esigenze specifiche di tutti i segmenti di pubblico.

## Scenari possibili

* Un’azienda di abbigliamento ha incrementato le conversioni testando varie immagini e personalizzando le pagine di destinazione delle campagne con i nomi degli utenti nel testo dell’invito all’azione.

* Una società di e-commerce ha riscontrato che i suoi membri fedeltà Gold avevano tassi di conversione più elevati testando varie descrizioni di prodotto e immagini su una pagina di destinazione della campagna, con conseguente aumento delle vendite.

## Passaggi

>[!NOTE]
>
>Le istruzioni in questa sezione evidenziano i passaggi necessari per modificare un’immagine e utilizzare gli attributi del profilo per personalizzare i messaggi di testo. Per ulteriori informazioni sulle opzioni disponibili nel Web Designer [!DNL Journey Optimizer], vedere [Utilizzare il Web Designer](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/web/author-web-pages/web-visual-editor){target=_blank} nella *documentazione di Journey Optimizer*.
>
>Il video nella parte inferiore della pagina è particolarmente utile.

Per ottimizzare una pagina web sottoponendo a test varie immagini e personalizzando i messaggi con i nomi degli utenti utilizzando uno script di profilo:

1. In [!DNL Journey Optimizer], fai clic su **Campagne** nella barra a sinistra per visualizzare la pagina [!UICONTROL Campaigns].

1. Fare clic su **[!UICONTROL Create Campaign]** nell&#39;angolo superiore destro della pagina [!UICONTROL Campaigns].

1. Seleziona **[!UICONTROL Scheduled - Marketing]** (impostazione predefinita), quindi fai clic su **Crea** per visualizzare la pagina dei dettagli di [!UICONTROL Campaign].

1. Nella sezione **[!UICONTROL Properties]**, fornisci un nome descrittivo e una descrizione facoltativa per la campagna.

1. (Condizionale) Nella sezione **[!UICONTROL Audience]**, fai clic su **[!UICONTROL Select Audience]** e scegli il pubblico desiderato.

   Per questo caso d&#39;uso, puoi attivare la campagna per [!UICONTROL All Visitors] (impostazione predefinita).

1. Nella sezione **[!UICONTROL Action]**, scegli **[!UICONTROL Web]** dall&#39;elenco a discesa **[!UICONTROL Action]**, quindi seleziona o crea una nuova configurazione web.

   Una configurazione web, o superficie di canale, è una configurazione definita da un amministratore di sistema. La configurazione web contiene tutti i parametri tecnici per l’invio del messaggio, ad esempio il parametro di intestazione, il sottodominio, le app mobili e così via.

   Per ulteriori informazioni, vedere [Configurare le superfici di canale](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/configuration/channel-surfaces#set-up-channel-surfaces){target=_blank} nella *documentazione di Journey Optimizer*.

1. Nella sezione **[!UICONTROL Action]**, fare clic su **[!UICONTROL Edit Content]** per aprire il sito Web nel Web Designer [!DNL Journey Optimizer].

   Sono necessari due o più esperimenti per il test A/B. Puoi utilizzare la pagina Home esistente come primo esperimento. I passaggi successivi spiegano come impostare un secondo esperimento.

   ![Pagina di destinazione dello yoga sul sito Web LUMA](/help/main/c-integrating-target-with-mac/ajo/assets/luma-yoga-landing.png)

1. Per creare un esperimento per determinare quale contenuto funziona meglio, fare clic su **[!UICONTROL Create Experiment]**.

   Gli esperimenti sul contenuto consentono di variare il contenuto del messaggio, l’oggetto o il mittente per definire più trattamenti e determinare la combinazione migliore per il pubblico. Per ulteriori informazioni, consulta [Creare un esperimento sui contenuti](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-experiment/content-experiment){target=_blank} nella *documentazione di Journey Optimizer*.

1. Seleziona una metrica di successo e fai clic su azione.

   Fare clic sulle icone della Guida per ulteriori informazioni e collegamenti agli articoli rilevanti.

1. Fare clic su **[!UICONTROL Add Treatment]**, quindi su **[!UICONTROL Create]**.

   Per questo caso d’uso, puoi lasciare la distribuzione al 50% per ogni esperimento.

1. Nella pagina dei dettagli [!UICONTROL Campaign], in **[!UICONTROL Action]**, fare clic su **[!UICONTROL Edit Content]**.

1. Fare clic su Web in Trattamento B.

   Per questo caso d&#39;uso, mantieni [!UICONTROL Treatment A] invariato per utilizzare l&#39;esperienza originale come prima esperienza nel test A/B.

1. Fai clic su **[!UICONTROL Edit Web Page]** nella barra a destra.

   ![Pagina Modifica contenuto nella pagina di destinazione Yoga](/help/main/c-integrating-target-with-mac/ajo/assets/edit-yoga-page.png)

1. Per modificare l&#39;immagine protagonista, fare clic sull&#39;immagine che si desidera modificare, quindi fare clic sul pulsante **[!UICONTROL Choose Image]**.

   ![Scegli il pulsante immagine](/help/main/c-integrating-target-with-mac/ajo/assets/choose-image.png)

1. Individuare e selezionare l&#39;immagine desiderata, quindi fare clic su **[!UICONTROL Use This Image]**.

   ![Nuova immagine protagonista sulla pagina Yoga](/help/main/c-integrating-target-with-mac/ajo/assets/new-hero-image.png)

1. Per personalizzare il messaggio con i nomi degli utenti utilizzando gli attributi del profilo, fare clic sul testo che si desidera personalizzare, quindi fare clic su **[!UICONTROL Add Personalization]** per visualizzare la pagina [!UICONTROL Add Personalization].

   ![Pulsante Aggiungi Personalization.](/help/main/c-integrating-target-with-mac/ajo/assets/add-personalization-button.png)

   Per ulteriori informazioni sugli attributi del profilo, consulta [Introduzione all&#39;editor di personalizzazione](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/personalization/expression-editor/personalization-build-expressions){target=_blank} nella *documentazione di Journey Optimizer*.

1. Cercare e fare clic sul segno più per aggiungere l&#39;attributo di profilo &quot;first name&quot;, modificare il testo come desiderato, quindi fare clic su **[!UICONTROL Save]**.

   ![Aggiungi attributo profilo per nome](/help/main/c-integrating-target-with-mac/ajo/assets/add-profile-attribute-for-name.png)

   Per ulteriori informazioni, consulta [Introduzione all&#39;editor di personalizzazione](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/personalization/expression-editor/personalization-build-expressions){target=_blank} nella *documentazione di Journey Optimizer*.

1. Fare clic sulla freccia indietro nell&#39;angolo superiore sinistro per tornare al Web Designer.

   ![Freccia indietro](/help/main/c-integrating-target-with-mac/ajo/assets/back-arrow.png)

1. Fai clic su **[!UICONTROL Review to Activate]**, assicurati che tutto appaia come previsto, quindi fai clic su **Attiva**.

## Visualizzare i rapporti

Fare clic sul pulsante [!UICONTROL Reports], quindi fare clic sul periodo di reporting desiderato:

* [!UICONTROL View all time report]
* [!UICONTROL View last 24hrs report]

Per ulteriori informazioni, vedere [Introduzione alla nuova interfaccia di reporting](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channel-report/report-gs-cja){target=_blank} nella *documentazione di Journey Optimizer*.

>[!MORELIKETHIS]
>
>[Utilizzare la finestra di progettazione Web](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/web/author-web-pages/web-visual-editor){target=_blank} nella *documentazione di Journey Optimizer*
>[Crea una campagna](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/create-campaigns/create-a-campaign){target=_blank} in *Esercitazioni Journey Optimizer*
