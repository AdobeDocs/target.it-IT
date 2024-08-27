---
keywords: ottimizzazione;personalizzazione;adobe percorsi optimizer;ajo;casi d'uso;scenari;cambiamento di contenuto/test ab;attributo profilo;cambiare immagine;scambiare immagine
description: Sblocca i segreti per le modifiche effettive al contenuto dei test A/B in Adobe Journey Optimizer
title: Modifiche al contenuto tramite test A/B in [!DNL Adobe Journey Optimizer]
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#beta newtab=true" tooltip="Cosa sono le funzioni beta in [!DNL Adobe Target]."
feature: Integrations
hide: true
hidefromtoc: true
source-git-commit: 7cf9a9425b9fb17c6e9595cedb7395f6610006ec
workflow-type: tm+mt
source-wordcount: '743'
ht-degree: 1%

---

# Modifiche al contenuto tramite test A/B in [!DNL Adobe Journey Optimizer]

Questo caso d&#39;uso consente di sbloccare i segreti per testare le modifiche effettive al contenuto A/B in [!DNL Adobe Journey Optimizer].

Questo caso d&#39;uso è progettato per dimostrare come eseguire attività familiari in [!DNL Adobe Target], test A/B utilizzando un&#39;attività Test [A/B](/help/main/c-activities/t-test-ab/test-ab.md), ma utilizzando [!DNL Journey Optimizer].

## Scenari possibili

* Una società di abbigliamento ha incrementato le conversioni testando varie immagini e personalizzando le pagine di destinazione delle campagne con i nomi degli utenti dai loro attributi di profilo.

* Testando varie descrizioni di prodotti e immagini su una pagina di destinazione della campagna, una società di e-commerce ha scoperto che i suoi membri fidelizzati avevano tassi di conversione più elevati, con conseguente aumento delle vendite.

## Vantaggi e valore

* **Ottimizza l&#39;efficacia dei contenuti**: scopri quali varianti di contenuto ed elementi risuonano di più con i tuoi clienti, portando a un coinvolgimento e a conversioni più elevati.
* **Decisioni basate sui dati**: sfrutta i dati per prendere decisioni informate in tutta la strategia dei contenuti, garantendo il massimo impatto.
* **Esperienza utente personalizzata**: personalizza il contenuto per soddisfare le preferenze e le esigenze specifiche di tutti i segmenti di pubblico.

## Passaggi

>[!NOTE]
>
>Le istruzioni in questa sezione evidenziano i passaggi necessari per modificare un’immagine e utilizzare gli attributi del profilo per personalizzare i messaggi di testo. Per ulteriori informazioni sulle opzioni disponibili nel Web Designer [!DNL Journey Optimizer], vedere [Modifica contenuto Web](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/web/author-web-pages/edit-web-content){target=_blank} nella *documentazione di Journey Optimizer*. Il video nella parte inferiore della pagina è particolarmente utile.

Per ottimizzare una pagina web sottoponendo a test varie immagini e personalizzando i messaggi con i nomi degli utenti mediante uno script di profilo, effettua le seguenti operazioni:

1. In [!DNL Adobe Journey Optimizer], fai clic su **Campagne** nella barra a sinistra per visualizzare la pagina [!UICONTROL Campaigns].

   ![Pagina di destinazione di Adobe Journey Optimizer con scheda Campagne evidenziata.](/help/main/c-integrating-target-with-mac/ajo/assets/ajo-landing-page.png)

1. Fare clic su **[!UICONTROL Create Campaign]** nell&#39;angolo superiore destro della pagina [!UICONTROL Campaigns].

1. Seleziona **[!UICONTROL Scheduled - Marketing]** (impostazione predefinita), quindi fai clic su **Crea** per visualizzare la pagina dei dettagli di [!UICONTROL Campaign].

   ![Pagina dettagli campagna in Adobe Journey Optimizer](/help/main/c-integrating-target-with-mac/ajo/assets/campaign-details.png)

1. Nella sezione **[!UICONTROL Properties]**, fornisci un nome descrittivo e una descrizione facoltativa per la campagna.

1. (Condizionale) Nella sezione **[!UICONTROL Audience]**, fai clic su **[!UICONTROL Select Audience]** e scegli il pubblico desiderato.

   Per questo caso d&#39;uso, abbiamo scelto di attivare la campagna per [!UICONTROL All Visitors] (impostazione predefinita).

1. Nella sezione **[!UICONTROL Action]**, scegli **[!UICONTROL Web]** dall&#39;elenco a discesa **[!UICONTROL Action]**, quindi seleziona o crea una nuova configurazione web.

   Una configurazione web, o superficie di canale, è una configurazione definita da un amministratore di sistema. La configurazione web contiene tutti i parametri tecnici per l’invio del messaggio, ad esempio il parametro di intestazione, il sottodominio, le app mobili e così via.

   Per ulteriori informazioni, vedere [Configurare le superfici di canale](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/configuration/channel-surfaces#set-up-channel-surfaces){target=_blank} nella *documentazione di Journey Optimizer*.

1. Nella sezione **[!UICONTROL Action]**, fare clic su **[!UICONTROL Edit Content]** per aprire il sito Web nel Web Designer [!DNL Journey Optimizer].

   Sono necessari due o più esperimenti per il test A/B. Puoi utilizzare la pagina Home esistente come primo esperimento. I passaggi successivi spiegano come impostare un secondo esperimento.

   ![Pagina di destinazione dello yoga sul sito Web LUMA](/help/main/c-integrating-target-with-mac/ajo/assets/luma-yoga-landing.png)

1. Per creare un esperimento per verificare quale contenuto funziona meglio, fare clic su **[!UICONTROL Create Experiment]**.

   Gli esperimenti sul contenuto consentono di variare il contenuto del messaggio, l’oggetto o il mittente per definire più trattamenti e determinare la combinazione migliore per il pubblico. Per ulteriori informazioni, consulta [Creare un esperimento sui contenuti](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-experiment/content-experiment){target=_blank} nella *documentazione di Journey Optimizer*.

1. Fai clic su **[!UICONTROL Edit Web Page]** nella barra a destra.

   ![Pagina Modifica contenuto nella pagina di destinazione Yoga](/help/main/c-integrating-target-with-mac/ajo/assets/edit-yoga-page.png)

1. Per modificare l&#39;immagine protagonista, fare clic sull&#39;immagine che si desidera modificare, quindi fare clic sul pulsante **[!UICONTROL Choose Image]**.

   ![Scegli il pulsante immagine](/help/main/c-integrating-target-with-mac/ajo/assets/choose-image.png)

1. Individuare e selezionare l&#39;immagine desiderata, quindi fare clic su **[!UICONTROL Use This Image]**.

   ![Nuova immagine protagonista sulla pagina Yoga](/help/main/c-integrating-target-with-mac/ajo/assets/new-hero-image.png)

1. Per personalizzare il messaggio con i nomi degli utenti utilizzando gli attributi del profilo, fare clic sul testo che si desidera personalizzare, quindi fare clic su **[!UICONTROL Add Personalization]** per visualizzare la pagina [!UICONTROL Add Personalization].

   ![Pulsante Aggiungi Personalization.](/help/main/c-integrating-target-with-mac/ajo/assets/add-personalization-button.png)

   Per ulteriori informazioni sugli attributi del profilo, consulta [Introduzione all&#39;editor di personalizzazione](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/personalization/expression-editor/personalization-build-expressions){target=_blank} nella *documentazione di Journey Optimizer*.

1. Cercare e selezionare l&#39;attributo di profilo &quot;first name&quot;, regolare il testo come desiderato, quindi fare clic su **[!UICONTROL Save]**.

   ![Aggiungi attributo profilo per nome](/help/main/c-integrating-target-with-mac/ajo/assets/add-profile-attribute-for-name.png)

   Per ulteriori informazioni, consulta [Introduzione all&#39;editor di personalizzazione](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/personalization/expression-editor/personalization-build-expressions){target=_blank} nella *documentazione di Journey Optimizer*.

1. Fare clic sulla freccia indietro nell&#39;angolo superiore sinistro per tornare al Web Designer.

   ![Freccia indietro](/help/main/c-integrating-target-with-mac/ajo/assets/back-arrow.png)

1. Fai clic su **[!UICONTROL Review to Activate]**, assicurati che tutto appaia come previsto, quindi fai clic su **Attiva**.

## Visualizzare i rapporti

Fai clic sul pulsante Rapporti, quindi fai clic sul periodo di reporting desiderato:

* [!UICONTROL View all time report]
* [!UICONTROL View last 24hrs report]

Per ulteriori informazioni, vedere [Introduzione alla nuova interfaccia di reporting](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channel-report/report-gs-cja){target=_blank} nella *documentazione di Journey Optimizer*.

>[!MORELIKETHIS]
>
>[Modifica contenuto Web](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/web/author-web-pages/edit-web-content){target=_blank} nella *documentazione di Journey Optimizer*
>[Video](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/web/author-web-pages/edit-web-content#video){target=_blank} nella *documentazione di Journey Optimizer*
>[Crea una campagna](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/create-campaigns/create-a-campaign){target=_blank} in *Tutorials Journey Optimizer*

