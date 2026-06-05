---
keywords: ottimizzazione;personalizzazione;adobe percorsi optimizer;ajo;casi d'uso;scenari;cambiamento di contenuto/test ab;attributo profilo;cambiare immagine;scambiare immagine
description: Sblocca i segreti per le modifiche effettive al contenuto dei test A/B in Adobe Journey Optimizer
title: Modifiche al contenuto tramite test A/B in [!DNL Adobe Journey Optimizer]
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#beta newtab=true" tooltip="Cosa sono le funzioni beta in [!DNL Adobe Target]."
feature: Integrations
hide: true
hidefromtoc: true
exl-id: e5aed7cd-7701-4133-ac7c-98e528c8a763
TQID: https://experienceleague.adobe.com/IqNBAHefm8J-DEo2fU-Nj19AhcZg-FUPLccs2eC9yPQ
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
  - id: f7c7de77-382f-4f48-8b36-61a170f06d3d
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: fc314d1d-7cb9-4a38-8dbd-8f9b6478f40d
source-git-commit: 16fb7a1902ea76cab56a93fa141a32a3c6bc4467
workflow-type: tm+mt
source-wordcount: 954
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

* Una società di abbigliamento ha aumentato le conversioni testando varie immagini e personalizzando le pagine di destinazione della campagna con i nomi degli utenti nel testo di call-to-action.

* Una società di e-commerce ha riscontrato che i suoi membri fedeltà Gold avevano tassi di conversione più elevati testando varie descrizioni di prodotto e immagini su una pagina di destinazione della campagna, con conseguente aumento delle vendite.

## Passaggi

>[!NOTE]
>
>Le istruzioni in questa sezione evidenziano i passaggi necessari per modificare un’immagine e utilizzare gli attributi del profilo per personalizzare i messaggi di testo. Per ulteriori informazioni sulle opzioni disponibili nel Web Designer [!DNL Journey Optimizer], vedere [Utilizzare il Web Designer](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/channels/web/author-web-pages/web-visual-editor){target=_blank} nella *documentazione di Journey Optimizer*.
>
>Il video nella parte inferiore della pagina è particolarmente utile.

Per ottimizzare una pagina web sottoponendo a test varie immagini e personalizzando i messaggi con i nomi degli utenti utilizzando uno script di profilo:

1. In [!DNL Journey Optimizer], fai clic su **Campagne** nella barra a sinistra per visualizzare la pagina [!UICONTROL Campagne].

1. Fai clic su **[!UICONTROL Crea campagna]** nell&#39;angolo superiore destro della pagina [!UICONTROL Campagne].

1. Seleziona **[!UICONTROL Pianificato - Marketing]** (impostazione predefinita), quindi fai clic su **Crea** per visualizzare la pagina dei dettagli di [!UICONTROL Campaign].

1. Nella sezione **[!UICONTROL Proprietà]**, fornisci un nome descrittivo e una descrizione facoltativa per la campagna.

1. (Condizionale) Nella sezione **[!UICONTROL Pubblico]**, fai clic su **[!UICONTROL Seleziona pubblico]** e scegli il pubblico desiderato.

   Per questo caso d&#39;uso, puoi attivare la campagna per [!UICONTROL Tutti i visitatori] (impostazione predefinita).

1. Nella sezione **[!UICONTROL Azione]**, scegli **[!UICONTROL Web]** dall&#39;elenco a discesa **[!UICONTROL Azione]**, quindi seleziona o crea una nuova configurazione Web.

   Una configurazione web, o superficie di canale, è una configurazione definita da un amministratore di sistema. La configurazione web contiene tutti i parametri tecnici per l’invio del messaggio, ad esempio il parametro di intestazione, il sottodominio, le app mobili e così via.

   Per ulteriori informazioni, vedere [Configurare le superfici di canale](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/configuration/channel-surfaces#set-up-channel-surfaces){target=_blank} nella *documentazione di Journey Optimizer*.

1. Nella sezione **[!UICONTROL Azione]**, fai clic su **[!UICONTROL Modifica contenuto]** per aprire il sito Web nella finestra di progettazione Web [!DNL Journey Optimizer].

   Sono necessari due o più esperimenti per il test A/B. Puoi utilizzare la pagina Home esistente come primo esperimento. I passaggi successivi spiegano come impostare un secondo esperimento.

   ![Pagina di destinazione dello yoga sul sito Web LUMA](/help/main/c-integrating-target-with-mac/ajo/assets/luma-yoga-landing.png)

1. Per creare un esperimento per determinare quale contenuto funziona meglio, fai clic su **[!UICONTROL Crea esperimento]**.

   Gli esperimenti sul contenuto consentono di variare il contenuto del messaggio, l’oggetto o il mittente per definire più trattamenti e determinare la combinazione migliore per il pubblico. Per ulteriori informazioni, consulta [Creare un esperimento sui contenuti](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/content-management/content-experiment/content-experiment){target=_blank} nella *documentazione di Journey Optimizer*.

1. Seleziona una metrica di successo e fai clic su azione.

   Fare clic sulle icone della Guida per ulteriori informazioni e collegamenti agli articoli rilevanti.

1. Fai clic su **[!UICONTROL Aggiungi trattamento]**, quindi su **[!UICONTROL Crea]**.

   Per questo caso d’uso, puoi lasciare la distribuzione al 50% per ogni esperimento.

1. Nella pagina dei dettagli della [!UICONTROL campagna], in **[!UICONTROL Azione]**, fai clic su **[!UICONTROL Modifica contenuto]**.

1. Fare clic su Web in Trattamento B.

   Per questo caso d&#39;uso, mantieni [!UICONTROL il trattamento A] invariato per utilizzare l&#39;esperienza originale come prima esperienza nel test A/B.

1. Fare clic su **[!UICONTROL Modifica pagina Web]** nella barra a destra.

   ![Pagina Modifica contenuto nella pagina di destinazione Yoga](/help/main/c-integrating-target-with-mac/ajo/assets/edit-yoga-page.png)

1. Per modificare l&#39;immagine protagonista, fare clic sull&#39;immagine che si desidera modificare, quindi fare clic sul pulsante **[!UICONTROL Scegli immagine]**.

   ![Scegli il pulsante immagine](/help/main/c-integrating-target-with-mac/ajo/assets/choose-image.png)

1. Individua e seleziona l&#39;immagine desiderata, quindi fai clic su **[!UICONTROL Usa questa immagine]**.

   ![Nuova immagine protagonista sulla pagina Yoga](/help/main/c-integrating-target-with-mac/ajo/assets/new-hero-image.png)

1. Per personalizzare il messaggio con i nomi degli utenti utilizzando gli attributi del profilo, fare clic sul testo che si desidera personalizzare, quindi su **[!UICONTROL Aggiungi Personalization]** per visualizzare la pagina [!UICONTROL Aggiungi Personalization].

   ![Pulsante Aggiungi Personalization.](/help/main/c-integrating-target-with-mac/ajo/assets/add-personalization-button.png)

   Per ulteriori informazioni sugli attributi del profilo, consulta [Introduzione all&#39;editor di personalizzazione](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/content-management/personalization/expression-editor/personalization-build-expressions){target=_blank} nella *documentazione di Journey Optimizer*.

1. Cerca e fai clic sul segno più per aggiungere l&#39;attributo di profilo &quot;first name&quot;, regola il testo come desideri, quindi fai clic su **[!UICONTROL Salva]**.

   ![Aggiungi attributo profilo per nome](/help/main/c-integrating-target-with-mac/ajo/assets/add-profile-attribute-for-name.png)

   Per ulteriori informazioni, consulta [Introduzione all&#39;editor di personalizzazione](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/content-management/personalization/expression-editor/personalization-build-expressions){target=_blank} nella *documentazione di Journey Optimizer*.

1. Fare clic sulla freccia indietro nell&#39;angolo superiore sinistro per tornare al Web Designer.

   ![Freccia indietro](/help/main/c-integrating-target-with-mac/ajo/assets/back-arrow.png)

1. Fai clic su **[!UICONTROL Rivedi per attivare]**, verifica che tutto appaia come previsto, quindi fai clic su **Attiva**.

## Visualizzazione dei rapporti

Fai clic sul pulsante [!UICONTROL Rapporti], quindi fai clic sul periodo di reporting desiderato:

* [!UICONTROL Visualizza report completo]
* [!UICONTROL Visualizza report delle ultime 24 ore]

Per ulteriori informazioni, vedere [Introduzione alla nuova interfaccia di reporting](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/channel-report/report-gs-cja){target=_blank} nella *documentazione di Journey Optimizer*.

>[!MORELIKETHIS]
>
>[Utilizzare la finestra di progettazione Web](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/channels/web/author-web-pages/web-visual-editor){target=_blank} nella *documentazione di Journey Optimizer*
>[Creare una campagna](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/create-campaigns/create-a-campaign){target=_blank} in *Tutorial su Journey Optimizer*
