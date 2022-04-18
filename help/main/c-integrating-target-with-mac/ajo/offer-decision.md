---
keywords: opzioni compositore esperienza visivo;opzioni compositore esperienza;opzioni esperienza;decisione offerta;offer decisioning;AJO;Ottimizzatore percorso
description: Scopri come aggiungere una decisione di offerta creata in [!DNL Adobe Journey Optimizer] a un’attività .
title: Come Si Utilizzano Le Decisioni Di Offerta?
feature: Visual Experience Composer (VEC)
exl-id: cec46d5c-bb5e-4cc9-8785-370f158d3f8e
source-git-commit: 4a2b0f52d00ca40609f3bfbddf7cb2b2bee6a33e
workflow-type: tm+mt
source-wordcount: '1003'
ht-degree: 0%

---

# Utilizzare le decisioni sulle offerte

Utilizzo [!DNL Adobe Target] con [!DNL Adobe Journey Optimizer] decide di offrire ai visitatori la possibilità di scegliere tra la migliore offerta disponibile sul web e la possibilità di scegliere tra quella successiva e quella successiva su dispositivi mobili.

Aggiungi le decisioni di offerta create in [!DNL Adobe Journey Optimizer] a [!DNL Target] attività (manuale [!UICONTROL Test A/B] o [!UICONTROL Targeting esperienza]) utilizzando [!UICONTROL Compositore esperienza visivo] (Compositore esperienza visivo) o [!UICONTROL Compositore basato su moduli] per testare e fornire offerte personalizzate ai visitatori sui tuoi canali in entrata alimentati da [!DNL Target].

Per ulteriori informazioni [!DNL Adobe Journey Optimizer], vedi [Guida introduttiva a Journey Optimizer](https://experienceleague.adobe.com/docs/journey-optimizer/using/get-started/get-started.html) in *Journey Optimizer* documentazione.

Per ulteriori informazioni sulle decisioni relative alle offerte, consulta [Informazioni sulla gestione delle decisioni](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioniong/get-started/starting-offer-decisioning.html) in *[!DNL Journey Optimizer]* documentazione.

## Prerequisiti

Per utilizzare le decisioni sulle offerte in [!DNL Target], è necessario quanto segue:

* [!DNL Adobe Target Standard] o [!DNL Adobe Target Premium] implementato utilizzando [Adobe Experience Platform Web SDK](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md).

   La funzione non è disponibile durante l’implementazione di [!DNL Target] con at.js o altro [!DNL Target] SDK.

* [!DNL Adobe Journey Optimizer Ultimate] (AJ0 + Offer decisioning) o [!DNL Adobe Experience Platform] e [!UICONTROL offer decisioning] componente aggiuntivo del servizio applicativo.

## Casi di utilizzo di esempio

Gli esempi seguenti sono casi d’uso su come utilizzare i [!DNL Target]/[!DNL Adobe Journey Optimizer] integrazione per utilizzare le decisioni sulle offerte in [!DNL Target] attività:

### Merchandising sportivo

In qualità di addetto al marketing per una lega sportiva, vuoi personalizzare i contenuti della tua homepage (sia sul sito web desktop che su quello mobile). Desideri personalizzare contenuti basati su più dimensioni e presentare un’offerta per i prodotti in franchising correlati al negozio. Sei interessato a:

* Il team preferito del visitatore
* Attività recente di atleta/giocatore (ad esempio, movimento di squadra, aggiornamenti del contratto o lesioni)

Ad esempio, desideri fornire un’esperienza personalizzata per ciascuna delle seguenti aree: Dortmund, Frankfurt e Bochum e per gli utenti che sono appassionati impliciti ed espliciti di queste squadre. In qualità di metriche, desideri esaminare visite e clic sul sito merci.

Desideri progettare un [!UICONTROL Test A/B] attività (50/50 diviso) tra l’esperienza predefinita e l’esperienza personalizzata (che include una decisione di offerta con offerte per ogni area geografica e team). Vuoi utilizzare questa attività per determinare la conversione e l’incremento per l’esperienza personalizzata rispetto al controllo.

### Piattaforme di streaming per giochi

In qualità di addetto al marketing per un’organizzazione di videogame, desideri offrire un’offerta personalizzata per una piattaforma di streaming per i giochi per utenti desktop e mobili provenienti da diverse aree geografiche: Germania, Francia, Messico e Brasile. Quando un visitatore accede al sito web desktop o mobile da una di queste aree geografiche, desideri fornire un’offerta per lo streaming dei giochi nella lingua locale e con un prezzo corrispondente per la valuta locale.

In [!DNL Adobe Journey Optimizer], puoi creare un’offerta protagonista per la homepage personalizzata per ciascuna delle aree geografiche target più un’offerta di fallback con un eroe della homepage predefinito. Puoi quindi creare una decisione di offerta che includa queste offerte e le relative regole di idoneità. Quindi, in [!DNL Target], puoi creare un’ [!DNL Experience Targeting] (XT) e inserisci la decisione dell’offerta nel sito web desktop o mobile per offrire ai visitatori l’esperienza personalizzata.

## Crea un’esperienza che utilizza una decisione di offerta:

1. Durante la modifica o la creazione di un manuale [!UICONTROL Test A/B] o [!UICONTROL Targeting esperienza] (XT) nell’ [!UICONTROL Compositore esperienza visivo] (Compositore esperienza visivo), fai clic su un elemento di pagina per visualizzare il [menu opzioni](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

   ![Menu Opzioni nel Compositore esperienza visivo](assets/options-menu1.png)

   >[!NOTE]
   >
   >Puoi anche creare un’esperienza che utilizza [!UICONTROL Decisioni di offerta] in [[!UICONTROL Compositore esperienza basato su moduli]](/help/main/c-experiences/form-experience-composer.md).

1. Fai clic su **[!UICONTROL Inserisci prima]**, **[!UICONTROL Inserisci dopo]** oppure **[!UICONTROL Sostituisci contenuto]**, quindi fai clic su **[!UICONTROL Decisione di offerta]**.

   La [!UICONTROL Decisione di offerta] è disponibile quando si modifica o si crea [manuale [!UICONTROL Test A/B]](/help/main/c-activities/t-test-ab/test-ab.md#types) o [[!UICONTROL Targeting esperienza]](/help/main/c-activities/t-experience-target/experience-target.md) Solo attività (XT). Questa opzione non è disponibile per altri tipi di attività. Le opzioni disponibili nel menu variano a seconda dell’elemento selezionato.

   ![Menu Opzioni nel Compositore esperienza visivo](assets/options-menu.png)

1. In **[!UICONTROL Aggiungi decisione offerta]** seleziona la sandbox e il posizionamento desiderati.

   A [sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/overview.html){target=_blank} nel [!DNL Adobe Experience Platform] consente di suddividere l’istanza in ambienti virtuali. Ad esempio, potresti avere un ambiente di produzione e un ambiente di staging. A [placement](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioniong/create-components/creating-placements.html){target=_blank} in [!DNL Adobe Journey Optimizer] garantisce che il contenuto dell’offerta corretta sia visualizzato nella posizione giusta.

   ![Elenchi a discesa Sandbox e Placements (Posizionamenti) nella finestra di dialogo Aggiungi decisione di offerta](/help/main/c-integrating-target-with-mac/ajo/assets/sandbox-placement.png)

1. Seleziona la decisione di offerta desiderata, quindi fai clic su **[!UICONTROL Crea]**.

   ![Decisione di offerta selezionata nella finestra di dialogo Aggiungi decisione offerta](assets/offer-decision.png)

   Il tuo sito web viene visualizzato nel Compositore esperienza visivo dove puoi vedere la decisione di offerta appena creata nel [!UICONTROL Modifiche] sul lato destro. Passa il puntatore del mouse sulla modifica e fai clic sul pulsante [!UICONTROL Anteprima] per esaminare la decisione di offerta.

   ![Icona Anteprima](assets/preview-icon.png)

   Per esaminare le varie offerte contenute nell’offerta, fai clic sull’icona appropriata nella parte inferiore della sezione [!UICONTROL Anteprima offerta] , inclusa l’offerta di fallback. Un’offerta di fallback è l’offerta predefinita visualizzata quando un visitatore non è idoneo per alcuna delle offerte personalizzate nella raccolta.

   ![Anteprima offerta](assets/offer-preview.png)

1. Completa la creazione dell’attività completando il [!UICONTROL Targeting] e [!UICONTROL Obiettivi e impostazioni] passaggi del flusso di lavoro guidato in tre parti.

   >[!IMPORTANT]
   >
   >Per garantire che [!DNL Target] l’attività è personalizzata, assicurati che le date di inizio/fine dell’attività correnti siano sincronizzate con le date di inizio/fine della decisione dell’offerta in [!DNL Adobe Journey Optimizer]. Se la [!DNL Target] le date di inizio/fine non rientrano nell’intervallo di date di inizio/fine della decisione dell’offerta, il valore predefinito [!DNL Target] il contenuto viene visualizzato ai visitatori.

   ![Messaggio di avviso relativo alla decisione dell’offerta](/help/main/c-integrating-target-with-mac/ajo/assets/offer-decision-warning.png)

## Note e limitazioni

Quando lavori con le decisioni relative alle offerte, prendi in considerazione le seguenti note e limitazioni:

* L’integrazione di offer decisioning funziona per [!DNL Target] implementazioni basate su [Adobe Experience Platform Web SDK](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md). Questa funzione non è disponibile durante l’implementazione di [!DNL Target] con at.js o altro [!DNL Target] SDK.

* L’integrazione di Target/Adobe Journey Optimizer supporta [manuale [!UICONTROL Test A/B]](/help/main/c-activities/t-test-ab/test-ab.md#types) e [[!UICONTROL Targeting esperienza]](/help/main/c-activities/t-experience-target/experience-target.md) Solo attività (XT). Questa funzione non è disponibile per altri tipi di attività.

* Le offerte con il tipo di contenuto text/html non supportano la consegna di contenuto deliveryURL. Il deliveryURL è supportato dal Compositore esperienza basato su moduli solo se il cliente è responsabile del recupero e della composizione esplicita del contenuto.

* [!DNL Target] il reporting non fornisce rapporti a livello di offerta-decisione.

* Visualizzazione [Collegamenti QA](/help/main/c-activities/c-activity-qa/activity-qa.md) per [!DNL Target] le esperienze che contengono decisioni sulle offerte hanno effetto sui limiti di frequenza impostati in [!DNL Adobe Journey Optimizer] per quelle decisioni di offerta.
