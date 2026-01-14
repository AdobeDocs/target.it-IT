---
keywords: ottimizzazione;personalizzazione;adobe percorsi optimizer;ajo;casi d'uso;scenari;aggiungere contenuto;nascondere contenuto;aggiungere componenti;nascondere componenti;optimization;personalization;adobe optimizer;ajo;use case;scenarios;add content;hide content;add components;hide components
description: Scopri come aggiungere o nascondere componenti nella pagina Web utilizzando  [!DNL Adobe Journey Optimizer].
title: Aggiungere o nascondere componenti alla pagina Web in [!DNL Adobe Journey Optimizer]
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#beta newtab=true" tooltip="Cosa sono le funzioni beta in [!DNL Adobe Target]."
feature: Integrations
hide: true
hidefromtoc: true
exl-id: 8c4fba88-908e-4742-ac4b-bdf7f4c882db
source-git-commit: 122484056e73f8f679312a3e776e623d905701d5
workflow-type: tm+mt
source-wordcount: '585'
ht-degree: 1%

---

# Aggiungere o nascondere componenti alla pagina web

Questo caso d&#39;uso consente di sbloccare i segreti per testare le modifiche effettive al contenuto A/B in [!DNL Adobe Journey Optimizer].

In questo caso d&#39;uso viene illustrato come eseguire attività familiari, ad esempio test A/B con un&#39;attività Test [A/B](/help/main/c-activities/t-test-ab/test-ab.md), utilizzando [!DNL Journey Optimizer] anziché [!DNL Adobe Target].

Questo caso d&#39;uso è progettato per dimostrare come eseguire attività familiari che potrebbero essere state eseguite utilizzando [!DNL Adobe Target], test A/B utilizzando un&#39;[attività Test A/B](/help/main/c-activities/t-test-ab/test-ab.md), ma utilizzando [!DNL Journey Optimizer].

## Vantaggi e valore

* **Migliora il coinvolgimento degli utenti**: attira l&#39;attenzione degli utenti con una progettazione di pagina ottimizzata che evidenzia informazioni rilevanti, come le promozioni.
* **Migliore individuabilità**: posizionamento strategico di nuovi componenti o contenuti nelle app Web o mobili per semplificare le azioni e migliorare la navigazione.
* **Aumento di punti di contatto aggiuntivi**: guida efficacemente gli utenti verso eventi di conversione e obiettivi per accelerare l&#39;impatto aziendale.

## Scenari possibili

* Una società di servizi finanziari prevede di aggiungere una nuova sezione sulla sua homepage per accedere rapidamente al calcolatore del prestito, riducendo i tempi di ricerca e aumentando le applicazioni di prestito.

* Un’azienda di abbigliamento ha aumentato le conversioni aggiungendo un nuovo pulsante call-to-action sulla sua pagina web.

## Passaggi

>[!NOTE]
>
>Le istruzioni in questa sezione evidenziano i passaggi necessari per modificare un’immagine e utilizzare gli attributi del profilo per personalizzare i messaggi di testo. Per ulteriori informazioni sulle opzioni disponibili nel Web Designer [!DNL Journey Optimizer], vedere [Utilizzare il Web Designer](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/channels/web/author-web-pages/web-visual-editor){target=_blank} nella *documentazione di Journey Optimizer*.
>
>Il video nella parte inferiore della pagina è particolarmente utile.

Per aggiungere o nascondere componenti nella pagina Web, effettua le seguenti operazioni:

1. In [!DNL Adobe Journey Optimizer], fai clic su **Campagne** nella barra a sinistra per visualizzare la pagina [!UICONTROL Campaigns].

   ![Pagina di destinazione di Adobe Journey Optimizer con scheda Campagne evidenziata.](/help/main/c-integrating-target-with-mac/ajo/assets/ajo-landing-page.png)

1. Fare clic su **[!UICONTROL Create Campaign]** nell&#39;angolo superiore destro della pagina [!UICONTROL Campaigns].

1. Seleziona **[!UICONTROL Scheduled - Marketing]** (impostazione predefinita), quindi fai clic su **Crea** per visualizzare la pagina dei dettagli di [!UICONTROL Campaign].

   ![Pagina dettagli campagna in Adobe Journey Optimizer](/help/main/c-integrating-target-with-mac/ajo/assets/campaign-details.png)

1. Nella sezione **[!UICONTROL Properties]**, fornisci un nome descrittivo e una descrizione facoltativa per la campagna.

1. (Condizionale) Nella sezione **[!UICONTROL Audience]**, fai clic su **[!UICONTROL Select Audience]** e scegli il pubblico desiderato.

   Per questo caso d&#39;uso, puoi attivare la campagna per [!UICONTROL All Visitors] (impostazione predefinita).

1. Nella sezione **[!UICONTROL Action]**, scegli **[!UICONTROL Web]** dall&#39;elenco a discesa **[!UICONTROL Action]**, quindi seleziona o crea una nuova configurazione web.

   Una configurazione web, o superficie di canale, è una configurazione definita da un amministratore di sistema. La configurazione web contiene tutti i parametri tecnici per l’invio del messaggio, ad esempio il parametro di intestazione, il sottodominio, le app mobili e così via.

   Per ulteriori informazioni, vedere [Configurare le superfici di canale](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/configuration/channel-surfaces#set-up-channel-surfaces){target=_blank} nella *documentazione di Journey Optimizer*.

1. Nella sezione **[!UICONTROL Action]**, fare clic su **[!UICONTROL Edit Content]** per aprire il sito Web nel Web Designer [!DNL Journey Optimizer].

   ![Pagina di destinazione dello yoga sul sito Web LUMA](/help/main/c-integrating-target-with-mac/ajo/assets/luma-yoga-landing.png)

1. Per aggiungere un elemento, fare clic su **[!UICONTROL Edit Web Page]** nella barra a destra.

1. Fare clic sull&#39;elemento che si desidera nascondere, quindi fare clic sul pulsante [!UICONTROL Hide] nella barra a destra.

   Nella barra a destra viene visualizzata l’opzione che è possibile eseguire sull’elemento selezionato. Queste opzioni variano a seconda dell’elemento selezionato.

   ![Nascondi pulsante elemento](/help/main/c-integrating-target-with-mac/ajo/assets/hide-element.png)

1. Fare clic sulla freccia indietro nell&#39;angolo superiore sinistro per tornare al Web Designer.

   ![Freccia indietro](/help/main/c-integrating-target-with-mac/ajo/assets/back-arrow.png)

1. Fai clic su **[!UICONTROL Review to Activate]**, assicurati che tutto appaia come previsto, quindi fai clic su **Attiva**.

## Visualizzazione dei rapporti

Fare clic sul pulsante [!UICONTROL Reports], quindi fare clic sul periodo di reporting desiderato:

* [!UICONTROL View all time report]
* [!UICONTROL View last 24hrs report]

Per ulteriori informazioni, vedere [Introduzione alla nuova interfaccia di reporting](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/channel-report/report-gs-cja){target=_blank} nella *documentazione di Journey Optimizer*.

>[!MORELIKETHIS]
>
>[Utilizzare la finestra di progettazione Web](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/channels/web/author-web-pages/web-visual-editor){target=_blank} nella *documentazione di Journey Optimizer*
>[Crea una campagna](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/create-campaigns/create-a-campaign){target=_blank} in *Esercitazioni Journey Optimizer*
