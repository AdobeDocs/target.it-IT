---
keywords: opzioni compositore esperienza visivo;opzioni compositore esperienza;opzioni esperienza;decisione offerta;offer decisioning;ajo;ottimizzatore percorso
description: Scopri come aggiungere a un'attività una decisione di offerta creata in [!DNL Adobe Journey Optimizer] .
title: Come Si Utilizzano Le Decisioni Sulle Offerte?
feature: Integrations
exl-id: cec46d5c-bb5e-4cc9-8785-370f158d3f8e
source-git-commit: d31c9a6f47ea73342cfb638600f351ade4be7013
workflow-type: tm+mt
source-wordcount: '887'
ht-degree: 0%

---

# Utilizzare le decisioni sulle offerte

Utilizza [!DNL Adobe Target] con [!DNL Adobe Journey Optimizer] decisioni di offerta per determinare e consegnare la migliore offerta successiva per i visitatori su web e dispositivi mobili.

Aggiungi le decisioni sulle offerte create in [!DNL Adobe Journey Optimizer] alle attività [!DNL Target] (manuale [!UICONTROL A/B Test] o [!UICONTROL Experience Targeting]) utilizzando [!UICONTROL Visual Experience Composer] (Compositore esperienza visivo) o [!UICONTROL Form-Based Composer] per testare e consegnare offerte personalizzate ai visitatori sui tuoi canali in entrata basati su [!DNL Target].

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

Desideri progettare un&#39;attività [!UICONTROL A/B Test] (50/50 suddivisa) tra l&#39;esperienza predefinita e l&#39;esperienza personalizzata (che include una decisione di offerta con offerte per ogni area geografica e team). Desideri utilizzare questa attività per determinare la conversione e l’incremento per l’esperienza personalizzata rispetto al controllo.

### Piattaforme di streaming di giochi

In qualità di addetto al marketing per un’organizzazione di giochi, desideri offrire un’offerta personalizzata per una piattaforma di streaming di giochi per utenti desktop e mobili da diverse aree geografiche: Germania, Francia, Messico e Brasile. Quando un visitatore accede al sito web desktop o mobile da una di queste aree geografiche, desideri fornire un’offerta per lo streaming di giochi nella lingua locale e con un prezzo corrispondente per la valuta locale.

In [!DNL Adobe Journey Optimizer], è possibile creare un&#39;offerta homepage hero personalizzata per ciascuna area geografica di destinazione più un&#39;offerta di fallback con un&#39;offerta homepage hero predefinita. Puoi quindi creare una decisione di offerta che incorpori queste offerte e le relative regole di idoneità. Quindi, in [!DNL Target], puoi creare un&#39;attività [!DNL Experience Targeting] (XT) e inserire tale decisione di offerta nel tuo sito Web desktop o mobile per fornire l&#39;esperienza personalizzata ai visitatori.

## Creare un’esperienza che utilizza una decisione di offerta:

1. Durante la modifica o la creazione di un&#39;attività manuale [!UICONTROL A/B Test] o [!UICONTROL Experience Targeting] (XT) nel [!UICONTROL Visual Experience Composer] (VEC), fare clic su un elemento di pagina per visualizzare il menu [opzioni](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

   ![Menu Opzioni nel Compositore esperienza visivo](assets/options-menu1.png)

   >[!NOTE]
   >
   >È inoltre possibile creare un&#39;esperienza che utilizza [!UICONTROL Offer Decisions] in [[!UICONTROL Form-Based Experience Composer]](/help/main/c-experiences/form-experience-composer.md).

1. Fare clic su **[!UICONTROL Replace Content]**, quindi su **[!UICONTROL Offer Decision]**.

   L&#39;opzione [!UICONTROL Offer Decision] è disponibile solo quando si modificano o si creano [attività manuali [!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md#types) o [[!UICONTROL Experience Targeting]](/help/main/c-activities/t-experience-target/experience-target.md) (XT). Questa opzione non è disponibile per altri tipi di attività. Le opzioni disponibili nel menu variano a seconda dell’elemento selezionato.

   ![Menu Opzioni nel Compositore esperienza visivo](assets/options-menu.png)

1. Nella barra **[!UICONTROL Add Offer Decision]** sul lato destro del Compositore esperienza visivo, seleziona la sandbox desiderata, quindi fai clic su Seleziona decisione offerta.posizionamento.

   Una [sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/overview.html){target=_blank} in [!DNL Adobe Experience Platform] consente di suddividere l&#39;istanza in ambienti virtuali. Ad esempio, potresti avere un ambiente di produzione e un ambiente di staging. Un [posizionamento](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/create-components/creating-placements.html){target=_blank} in [!DNL Adobe Journey Optimizer] consente di garantire che il contenuto dell&#39;offerta corretta venga visualizzato nella posizione corretta.

   ![Elenchi a discesa Sandbox e Posizionamenti nella finestra di dialogo Aggiungi decisione offerta](/help/main/c-integrating-target-with-mac/ajo/assets/sandbox-placement.png)

1. Selezionare il posizionamento dell&#39;offerta e la decisione di offerta desiderati, quindi fare clic su **[!UICONTROL Add]**.

   ![Finestra di dialogo Seleziona decisione offerta](/help/main/c-integrating-target-with-mac/ajo/assets/select-offer-decision.png)

   Il sito web viene visualizzato nel Compositore esperienza visivo dove puoi visualizzare la decisione di offerta appena creata nella barra [!UICONTROL Modifications]. Puoi fare clic su un&#39;offerta in [!UICONTROL Offer Preview] nella parte inferiore della barra [!UICONTROL Offer Decision] per esaminare la decisione sull&#39;offerta.

   <!--You can examine the various offers contained in the offer by clicking the appropriate icon at the bottom of the [!UICONTROL Offer Preview] dialog box, including the fallback offer. A fallback offer is the default offer displayed when a visitor is not eligible for any of the personalized offers in the collection.-->

   ![Anteprima offerta](assets/offer-preview2.png)

1. Completa la creazione dell&#39;attività completando i passaggi [!UICONTROL Targeting] e [!UICONTROL Goals & Settings] del flusso di lavoro guidato in tre parti.

   >[!IMPORTANT]
   >
   >Per garantire che l&#39;attività [!DNL Target] sia personalizzata, assicurarsi che le date di inizio/fine dell&#39;attività corrente siano sincronizzate con le date di inizio/fine della decisione sull&#39;offerta in [!DNL Adobe Journey Optimizer]. Se le date di inizio/fine di [!DNL Target] non rientrano nell&#39;intervallo di date di inizio/fine della decisione sull&#39;offerta, il contenuto predefinito di [!DNL Target] viene visualizzato ai visitatori.

## Note e limitazioni

Considera le seguenti informazioni mentre lavori con le decisioni sulle offerte:

* L&#39;integrazione di Offer Decisioning funziona per le implementazioni [!DNL Target] basate su [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=it){target=_blank}. Questa funzione non è disponibile quando si implementa [!DNL Target] con at.js o altri SDK [!DNL Target].

* L&#39;integrazione di [!DNL Target]/[!DNL Adobe Journey Optimizer] supporta solo [le attività manuali [!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md#types) e [[!UICONTROL Experience Targeting]](/help/main/c-activities/t-experience-target/experience-target.md) (XT). Questa funzione non è disponibile per altri tipi di attività.

* Non puoi utilizzare [[!UICONTROL Analytics as the reporting source]](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) se utilizzi decisioni sulle offerte in un&#39;attività. Scegli [!DNL Target] come origine per la generazione di rapporti nella pagina [!UICONTROL Goals and Settings] durante la configurazione dell&#39;attività se utilizzi le decisioni sulle offerte nell&#39;attività.

* Le offerte con tipo di contenuto text/html non supportano la consegna di contenuti deliveryURL. DeliveryURL è supportato tramite [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md) solo se il client è responsabile del recupero e della composizione espliciti del contenuto.

* La generazione rapporti di [!DNL Target] non fornisce rapporti a livello di offerta.

* La visualizzazione di [collegamenti di controllo qualità](/help/main/c-activities/c-activity-qa/activity-qa.md) per [!DNL Target] esperienze che contengono decisioni sulle offerte influisce sui limiti di frequenza impostati in [!DNL Adobe Journey Optimizer] per tali decisioni sulle offerte.
