---
keywords: opzioni compositore esperienza visivo;opzioni compositore esperienza;opzioni esperienza;decisione offerta;offer decisioning;ajo;ottimizzatore percorso
description: Scopri come aggiungere una decisione di offerta creata in [!DNL Adobe Journey Optimizer] a un’attività.
title: Come Si Utilizzano Le Decisioni Sulle Offerte?
feature: Integrations
exl-id: cec46d5c-bb5e-4cc9-8785-370f158d3f8e
source-git-commit: 3ac61272ee1ccd72a8670966f181e7798cbe9f76
workflow-type: tm+mt
source-wordcount: '979'
ht-degree: 2%

---

# Utilizzare le decisioni sulle offerte

Utilizzare [!DNL Adobe Target] con [!DNL Adobe Journey Optimizer] decisioni sulle offerte per determinare e fornire la migliore offerta successiva per i visitatori su web e dispositivi mobili.

Aggiungere decisioni di offerta create in [!DNL Adobe Journey Optimizer] a [!DNL Target] attività (manuale [!UICONTROL Test A/B] o [!UICONTROL Targeting esperienza]) utilizzando [!UICONTROL Compositore esperienza visivo] (VEC) o [!UICONTROL Compositore basato su moduli] per testare e consegnare offerte personalizzate ai visitatori sui tuoi canali in entrata basati su [!DNL Target].

Per ulteriori informazioni su [!DNL Adobe Journey Optimizer] e le decisioni sulle offerte, consulta i seguenti argomenti nella *[!DNL Journey Optimizer]* documentazione:

* [Introduzione a Journey Optimizer](https://experienceleague.adobe.com/docs/journey-optimizer/using/get-started/get-started.html)

* [Informazioni sulla gestione delle decisioni](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioniong/get-started/starting-offer-decisioning.html)

## Prerequisiti

Per utilizzare le decisioni sulle offerte in [!DNL Target], sono necessari i seguenti elementi:

* [!DNL Adobe Target Standard] o [!DNL Adobe Target Premium] implementato utilizzando [Adobe Experience Platform Web SDK](https://developer.adobe.com/target/implement/client-side/aep-web-sdk/){target=_blank}.

   La funzione non è disponibile quando si implementa [!DNL Target] con at.js o altro [!DNL Target] SDK.

* [!DNL Adobe Journey Optimizer Ultimate] (AJO + Offer decisioning) o [!DNL Adobe Experience Platform] e [!UICONTROL Offer decisioning] componente aggiuntivo del servizio applicativo.

## Casi d’uso di esempio

Gli esempi seguenti sono casi di utilizzo di come è possibile utilizzare [!DNL Target]/[!DNL Adobe Journey Optimizer] integrazione per utilizzare le decisioni sulle offerte in [!DNL Target] attività:

### Merchandising sportivo

In qualità di addetto al marketing di un campionato sportivo, desideri personalizzare i contenuti nella tua home page (sul sito web desktop e mobile). Desideri personalizzare i contenuti in base a più dimensioni e presentare un’offerta per acquistare articoli in franchising. Sei interessato a:

* Il team preferito del visitatore
* Attività recente di atleta/giocatore (ad esempio, movimento della squadra, aggiornamenti del contratto o infortuni)

Ad esempio, desideri offrire un’esperienza personalizzata per ciascuna delle seguenti aree geografiche: Dortmund, Francoforte e Bochum e per gli utenti che sono fan impliciti ed espliciti di questi team. Come metriche, vuoi esaminare le visite e i clic sul sito di merchandising.

Desideri progettare un’ [!UICONTROL Test A/B] attività (50/50 suddivisa) tra l’esperienza predefinita e quella personalizzata (che include una decisione di offerta con offerte per ogni area geografica e team). Desideri utilizzare questa attività per determinare la conversione e l’incremento per l’esperienza personalizzata rispetto al controllo.

### Piattaforme di streaming di giochi

In qualità di addetto al marketing per un’organizzazione di giochi, desideri offrire un’offerta personalizzata per una piattaforma di streaming di giochi per utenti desktop e mobili da diverse aree geografiche: Germania, Francia, Messico e Brasile. Quando un visitatore accede al sito web desktop o mobile da una di queste aree geografiche, desideri fornire un’offerta per lo streaming di giochi nella lingua locale e con un prezzo corrispondente per la valuta locale.

In entrata [!DNL Adobe Journey Optimizer], puoi creare un’offerta homepage hero personalizzata per ciascuna area geografica di destinazione e un’offerta di fallback con un’offerta homepage hero predefinita. Puoi quindi creare una decisione di offerta che incorpori queste offerte e le relative regole di idoneità. Quindi, in [!DNL Target], puoi creare un’ [!DNL Experience Targeting] (XT) e inserisci tale decisione di offerta nel sito web desktop o mobile per fornire ai visitatori l’esperienza personalizzata.

## Creare un’esperienza che utilizza una decisione di offerta:

1. Durante la modifica o la creazione di un manuale [!UICONTROL Test A/B] o [!UICONTROL Targeting esperienza] (XT) attività in [!UICONTROL Compositore esperienza visivo] (VEC), fai clic su un elemento di pagina per visualizzare [menu delle opzioni](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

   ![Menu Opzioni nel Compositore esperienza visivo](assets/options-menu1.png)

   >[!NOTE]
   >
   >Puoi anche creare un’esperienza che utilizza [!UICONTROL Decisioni di offerta] nel [[!UICONTROL Compositore esperienza basato su moduli]](/help/main/c-experiences/form-experience-composer.md).

1. Clic **[!UICONTROL Inserisci prima]**, **[!UICONTROL Inserisci dopo]**, o **[!UICONTROL Sostituisci contenuto]**, quindi fai clic su **[!UICONTROL Decisione offerta]**.

   Il [!UICONTROL Decisione offerta] è disponibile quando si modifica o si crea [manuale [!UICONTROL Test A/B]](/help/main/c-activities/t-test-ab/test-ab.md#types) o [[!UICONTROL Targeting esperienza]](/help/main/c-activities/t-experience-target/experience-target.md) (XT) solo attività. Questa opzione non è disponibile per altri tipi di attività. Le opzioni disponibili nel menu variano a seconda dell’elemento selezionato.

   ![Menu Opzioni nel Compositore esperienza visivo](assets/options-menu.png)

1. In **[!UICONTROL Aggiungi decisione di offerta]** , selezionare la sandbox e il posizionamento desiderati.

   A [sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/overview.html){target=_blank} in the [!DNL Adobe Experience Platform] lets you partition your instance into virtual environments. For example, you might have a production environment and a staging environment. A [placement](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioniong/create-components/creating-placements.html){target=_blank} in [!DNL Adobe Journey Optimizer] garantisce che il contenuto dell’offerta corretta venga visualizzato nella posizione giusta.

   ![Elenchi a discesa Sandbox e Posizionamenti nella finestra di dialogo Aggiungi decisione di offerta](/help/main/c-integrating-target-with-mac/ajo/assets/sandbox-placement.png)

1. Seleziona la decisione di offerta desiderata, quindi fai clic su **[!UICONTROL Crea]**.

   ![Decisione di offerta selezionata nella finestra di dialogo Aggiungi decisione di offerta](assets/offer-decision.png)

   Il sito web viene visualizzato nel Compositore esperienza visivo, dove puoi vedere la decisione di offerta appena creata nel [!UICONTROL Modifiche] sul lato destro. Passa il puntatore del mouse sulla modifica e fai clic sul pulsante [!UICONTROL Anteprima] per esaminare la decisione di offerta.

   ![Icona Anteprima](assets/preview-icon.png)

   Puoi esaminare le varie offerte contenute nell’offerta facendo clic sull’icona appropriata nella parte inferiore della [!UICONTROL Anteprima offerta] , inclusa l&#39;offerta di fallback. Un’offerta di fallback è l’offerta predefinita che viene visualizzata se un visitatore non è idoneo per nessuna delle offerte personalizzate nella raccolta.

   ![Anteprima offerta](assets/offer-preview.png)

1. Completa la creazione dell’attività completando la sezione [!UICONTROL Targeting] e [!UICONTROL Obiettivi e impostazioni] passaggi del flusso di lavoro guidato in tre parti.

   >[!IMPORTANT]
   >
   >Per garantire che [!DNL Target] l’attività è personalizzata, assicurati che le date di inizio/fine dell’attività corrente siano sincronizzate con le date di inizio/fine della decisione di offerta in [!DNL Adobe Journey Optimizer]. Se il [!DNL Target] le date di inizio/fine non rientrano nell’intervallo di date di inizio/fine della decisione di offerta, che è l’impostazione predefinita [!DNL Target] il contenuto viene visualizzato ai visitatori.

   ![Messaggio di avviso di decisione di offerta](/help/main/c-integrating-target-with-mac/ajo/assets/offer-decision-warning.png)

## Note e limitazioni

Considera le seguenti informazioni mentre lavori con le decisioni sulle offerte:

* L’integrazione di offer decisioning funziona per [!DNL Target] implementazioni basate su [Adobe Experience Platform Web SDK](https://developer.adobe.com/target/implement/client-side/aep-web-sdk/){target=_blank}. Questa funzione non è disponibile quando si implementa [!DNL Target] con at.js o altro [!DNL Target] SDK.

* L’integrazione di Target/Adobe Journey Optimizer supporta [manuale [!UICONTROL Test A/B]](/help/main/c-activities/t-test-ab/test-ab.md#types) e [[!UICONTROL Targeting esperienza]](/help/main/c-activities/t-experience-target/experience-target.md) (XT) solo attività. Questa funzione non è disponibile per altri tipi di attività.

* Le offerte con tipo di contenuto text/html non supportano la consegna di contenuti deliveryURL. L’URL di consegna è supportato tramite il Compositore esperienza basato su moduli solo se il client è responsabile del recupero e della composizione espliciti del contenuto.

* [!DNL Target] il reporting non fornisce rapporti a livello di offerta-decisione.

* Visualizzazione [Collegamenti QA](/help/main/c-activities/c-activity-qa/activity-qa.md) per [!DNL Target] le esperienze che contengono decisioni di offerta influiscono sui limiti di frequenza impostati in [!DNL Adobe Journey Optimizer] per le decisioni di offerta.
