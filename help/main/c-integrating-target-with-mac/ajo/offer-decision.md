---
keywords: opzioni compositore esperienza visivo;opzioni compositore esperienza;opzioni esperienza;decisione offerta;offer decisioning;ajo;ottimizzatore percorso
description: Scopri come aggiungere a un'attività una decisione di offerta creata in [!DNL Adobe Journey Optimizer] .
title: Come Si Utilizzano Le Decisioni Sulle Offerte?
feature: Integrations
exl-id: cec46d5c-bb5e-4cc9-8785-370f158d3f8e
TQID: https://experienceleague.adobe.com/xEae4As4rNbPv-an3Iu8PCMzxftSAmN4iu0PEq6VDFQ
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2: id: adee20bd-51f4-461d-b9db-d215f8756eebid: c93393a4-e558-47e1-992e-c91ed4d480ceid: f7c7de77-382f-4f48-8b36-61a170f06d3d
subfeature_v2: id: fd0ff162-b6d3-4a11-8aeb-e165a01c0f0a
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 1017
ht-degree: 3%

---

# Utilizzare le decisioni sulle offerte

Utilizza [!DNL Adobe Target] con [!DNL Adobe Journey Optimizer] decisioni di offerta per determinare e consegnare la migliore offerta successiva per i visitatori su web e dispositivi mobili.

Aggiungi le decisioni sulle offerte create in [!DNL Adobe Journey Optimizer] alle attività [!DNL Target] (manuale [!UICONTROL Test A/B] o [!UICONTROL Targeting esperienza]) utilizzando il [!UICONTROL Compositore esperienza visivo] o il [!UICONTROL Compositore basato su moduli] per testare e consegnare offerte personalizzate ai visitatori sui tuoi canali in entrata basati su [!DNL Target].

Per ulteriori informazioni su [!DNL Adobe Journey Optimizer] e sulle decisioni sulle offerte, vedi i seguenti argomenti nella documentazione di *[!DNL Journey Optimizer]*:

* [Introduzione a Journey Optimizer](https://experienceleague.adobe.com/docs/journey-optimizer/using/get-started/get-started.html)

* [Informazioni sulla gestione delle decisioni](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/get-started-decision/starting-offer-decisioning.html?lang=it)

## Prerequisiti

Per utilizzare le decisioni sulle offerte in [!DNL Target], è necessario quanto segue:

* [!DNL Adobe Target Standard] o [!DNL Adobe Target Premium] implementati utilizzando [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=it){target=_blank}.

  La funzione non è disponibile quando si implementa [!DNL Target] con at.js o altri SDK [!DNL Target].

* [!DNL Adobe Journey Optimizer Ultimate] (AJO + Offer Decisioning) o [!DNL Adobe Experience Platform] e il componente aggiuntivo del servizio applicativo [!UICONTROL Offer Decisioning].

## Casi d’uso di esempio

Di seguito sono riportati alcuni esempi di utilizzo dell&#39;integrazione [!DNL Target]/[!DNL Adobe Journey Optimizer] per l&#39;utilizzo delle decisioni sulle offerte nelle attività [!DNL Target]:

### Merchandising sportivo

In qualità di addetto al marketing di un campionato sportivo, desideri personalizzare i contenuti nella tua home page (sul sito web desktop e mobile). Desideri personalizzare i contenuti in base a più dimensioni e presentare un’offerta per acquistare articoli in franchising. Sei interessato a:

* Il team preferito del visitatore
* Attività recente di atleta/giocatore (ad esempio, movimento della squadra, aggiornamenti del contratto o infortuni)

Ad esempio, desideri offrire un’esperienza personalizzata per ciascuna delle seguenti aree geografiche: Dortmund, Francoforte e Bochum e per gli utenti che sono fan impliciti ed espliciti di questi team. Come metriche, vuoi esaminare le visite e i clic sul sito di merchandising.

Desideri progettare un&#39;attività [!UICONTROL Test A/B] (50/50 suddivisi) tra l&#39;esperienza predefinita e l&#39;esperienza personalizzata (che include una decisione di offerta con offerte per ogni area geografica e team). Desideri utilizzare questa attività per determinare la conversione e l’incremento per l’esperienza personalizzata rispetto al controllo.

### Piattaforme di streaming di giochi

In qualità di addetto al marketing per un’organizzazione di giochi, desideri offrire un’offerta personalizzata per una piattaforma di streaming di giochi per utenti desktop e mobili da diverse aree geografiche: Germania, Francia, Messico e Brasile. Quando un visitatore accede al sito web desktop o mobile da una di queste aree geografiche, desideri fornire un’offerta per lo streaming di giochi nella lingua locale e con un prezzo corrispondente per la valuta locale.

In [!DNL Adobe Journey Optimizer], è possibile creare un&#39;offerta homepage hero personalizzata per ciascuna area geografica di destinazione più un&#39;offerta di fallback con un&#39;offerta homepage hero predefinita. Puoi quindi creare una decisione di offerta che incorpori queste offerte e le relative regole di idoneità. Quindi, in [!DNL Target], puoi creare un&#39;attività [!DNL Experience Targeting] (XT) e inserire tale decisione di offerta nel tuo sito Web desktop o mobile per fornire l&#39;esperienza personalizzata ai visitatori.

## Creare un’esperienza che utilizza una decisione di offerta:

1. Durante la modifica o la creazione di un&#39;attività [!UICONTROL Test A/B] o [!UICONTROL Targeting esperienza] (XT) manuale nel [!UICONTROL Compositore esperienza visivo], fare clic su un elemento di pagina per visualizzare il [menu opzioni](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

   ![Menu Opzioni nel Compositore esperienza visivo](assets/options-menu1.png)

   >[!NOTE]
   >
   >Puoi anche creare un&#39;esperienza che utilizza [!UICONTROL Decisioni di offerta] nel [[!UICONTROL Compositore esperienza basato su moduli]](/help/main/c-experiences/form-experience-composer.md).

1. Fai clic su **[!UICONTROL Sostituisci contenuto]**, quindi su **[!UICONTROL Decisione offerta]**.

   L&#39;opzione [!UICONTROL Decisione offerta] è disponibile solo per la modifica o la creazione di [attività manuali [!UICONTROL Test A/B]](/help/main/c-activities/t-test-ab/test-ab.md#types) o [[!UICONTROL Targeting esperienza]](/help/main/c-activities/t-experience-target/experience-target.md) (XT). Questa opzione non è disponibile per altri tipi di attività. Le opzioni disponibili nel menu variano a seconda dell’elemento selezionato.

   ![Menu Opzioni nel Compositore esperienza visivo](assets/options-menu.png)

1. Nella barra **[!UICONTROL Aggiungi decisione offerta]** sul lato destro del Compositore esperienza visivo, seleziona la sandbox desiderata, quindi fai clic su Seleziona decisione offerta.posizionamento.

   Una [sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/overview.html){target=_blank} in [!DNL Adobe Experience Platform] consente di suddividere l&#39;istanza in ambienti virtuali. Ad esempio, potresti avere un ambiente di produzione e un ambiente di staging. Un [posizionamento](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/create-components/creating-placements.html){target=_blank} in [!DNL Adobe Journey Optimizer] consente di garantire che il contenuto dell&#39;offerta corretta venga visualizzato nella posizione corretta.

   ![Elenchi a discesa Sandbox e Posizionamenti nella finestra di dialogo Aggiungi decisione offerta](/help/main/c-integrating-target-with-mac/ajo/assets/sandbox-placement.png)

1. Seleziona il posizionamento dell&#39;offerta e la decisione di offerta, quindi fai clic su **[!UICONTROL Aggiungi]**.

   ![Finestra di dialogo Seleziona decisione offerta](/help/main/c-integrating-target-with-mac/ajo/assets/select-offer-decision.png)

   Il sito Web viene visualizzato nel Compositore esperienza visivo dove puoi visualizzare la decisione di offerta appena creata nella barra [!UICONTROL Modifiche]. Puoi fare clic su un&#39;offerta in [!UICONTROL Anteprima offerta] nella parte inferiore della barra [!UICONTROL Decisione offerta] per esaminare la decisione sull&#39;offerta.

   <!--You can examine the various offers contained in the offer by clicking the appropriate icon at the bottom of the [!UICONTROL Offer Preview] dialog box, including the fallback offer. A fallback offer is the default offer displayed when a visitor is not eligible for any of the personalized offers in the collection.-->

   ![Anteprima offerta](assets/offer-preview2.png)

1. Completa la creazione dell&#39;attività completando i passaggi [!UICONTROL Targeting] e [!UICONTROL Obiettivi e impostazioni] del flusso di lavoro guidato in tre parti.

   >[!IMPORTANT]
   >
   >Per garantire che l&#39;attività [!DNL Target] sia personalizzata, assicurarsi che le date di inizio/fine dell&#39;attività corrente siano sincronizzate con le date di inizio/fine della decisione sull&#39;offerta in [!DNL Adobe Journey Optimizer]. Se le date di inizio/fine di [!DNL Target] non rientrano nell&#39;intervallo di date di inizio/fine della decisione sull&#39;offerta, il contenuto predefinito di [!DNL Target] viene visualizzato ai visitatori.

## Note e limitazioni

Considera le seguenti informazioni mentre lavori con le decisioni sulle offerte:

* L&#39;integrazione di Offer Decisioning funziona per le implementazioni [!DNL Target] basate su [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=it){target=_blank}. Questa funzione non è disponibile quando si implementa [!DNL Target] con at.js o altri SDK [!DNL Target].

* L&#39;integrazione di [!DNL Target]/[!DNL Adobe Journey Optimizer] supporta solo [attività manuali [!UICONTROL Test A/B]](/help/main/c-activities/t-test-ab/test-ab.md#types) e [[!UICONTROL Targeting esperienza]](/help/main/c-activities/t-experience-target/experience-target.md) (XT). Questa funzione non è disponibile per altri tipi di attività.

* Non puoi utilizzare [[!UICONTROL Analytics come origine per la generazione di rapporti]](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) se utilizzi decisioni sulle offerte in un&#39;attività. Scegli [!DNL Target] come origine per la generazione di rapporti nella pagina [!UICONTROL Obiettivi e impostazioni] durante la configurazione dell&#39;attività se utilizzi le decisioni sulle offerte nell&#39;attività.

* Le offerte con tipo di contenuto text/html non supportano la consegna di contenuti deliveryURL. DeliveryURL è supportato tramite [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md) solo se il client è responsabile del recupero e della composizione espliciti del contenuto.

* La generazione rapporti di [!DNL Target] non fornisce rapporti a livello di offerta.

* La visualizzazione di [collegamenti di controllo qualità](/help/main/c-activities/c-activity-qa/activity-qa.md) per [!DNL Target] esperienze che contengono decisioni sulle offerte influisce sui limiti di frequenza impostati in [!DNL Adobe Journey Optimizer] per tali decisioni sulle offerte.
