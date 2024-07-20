---
keywords: a4t;analytics;analytics for target;origine per la generazione di rapporti analytics;adobe analytics come origine per la generazione di rapporti per target;atjs;at.js;adobe experience platform web sdk;platform web sdk;platform sdk
description: Utilizza  [!DNL Analytics]  for  [!DNL Target]  (A4T) per creare attività basate su metriche di conversione di  [!DNL Analytics]  e segmenti di pubblico e utilizza i rapporti di  [!DNL Analytics]  per esaminare i risultati.
title: Cos’è  [!DNL Analytics]  for  [!DNL Target]  (A4T)?
feature: Analytics for Target (A4T)
exl-id: 5bb80b03-8209-4932-a838-0e11c5865133
source-git-commit: f7bb9b5d6e96095a31f50f1976b87d9ee7b7eb51
workflow-type: tm+mt
source-wordcount: '1046'
ht-degree: 81%

---

# [!DNL Adobe Analytics] come origine per la generazione di rapporti per [!DNL Adobe Target] (A4T)

[!DNL Adobe Analytics for Target] (A4T) è un’integrazione tra soluzioni che consente di creare attività basate su metriche di conversione e segmenti di pubblico di [!DNL Analytics]. L’integrazione di A4T consente di utilizzare i rapporti di [!DNL Analytics] per esaminare i risultati. Se utilizzi [!DNL Analytics] come origine per la generazione di rapporti per un’attività, tutti i rapporti e le segmentazioni per tale attività si basano sulla raccolta di dati di [!DNL Analytics].

## Panoramica {#section_92B66069210C40DBA937790E8CC596CF}

L’integrazione [!DNL Analytics for Target] tra [!DNL Analytics] e [!DNL Target] fornisce potenti strumenti di analisi per il programma di ottimizzazione, che consentono di risparmiare tempo prezioso.

L’utilizzo dei dati di [!DNL Analytics] in [!DNL Target] offre i tre vantaggi principali seguenti:

* Gli addetti al marketing possono applicare dinamicamente le metriche di successo di [!DNL Analytics] o i segmenti di reporting ai rapporti delle attività di [!DNL Target] in qualsiasi momento. Non è necessario specificare tutte le impostazioni prima di eseguire l’attività.
* Un’unica fonte di dati elimina la varianza che si verifica quando si raccolgono dati in due sistemi distinti.
* L’implementazione di [!DNL Analytics] esistente raccoglie tutti i dati necessari. Non è necessario implementare mbox sulle pagine al solo scopo di raccogliere dati per i rapporti.

Se utilizzi [!DNL Analytics] come origine per la generazione di rapporti per un’attività, tutti i rapporti e le segmentazioni per tale attività si basano su [!DNL Analytics].

Tutte le metriche di [!DNL Analytics], comprese quelle calcolate, sono disponibili in [!DNL Target] e nel report [!UICONTROL Target Activities] in [!DNL Analytics], con una eccezione. Le metriche calcolate per [!UICONTROL Lift & Confidence] non sono supportate. Allo stesso modo, qualsiasi segmento disponibile in [!DNL Analytics] può essere applicato a entrambe le soluzioni. Puoi applicare la metrica o il pubblico al rapporto in [!DNL Target] dopo che l’attività è iniziata o anche dopo che è stata completata.

Ogni metrica è inclusa, comprese quelle personalizzate o calcolate che sono integrate in [!DNL Analytics].

Dopo il periodo di classificazione, i dati sono visualizzati in questi rapporti circa un&#39;ora dopo essere stati raccolti dal sito. Tutte le metriche, i segmenti e i valori nei rapporti provengono dalla suite di rapporti selezionata quando si configura l’attività.

Considerazioni importanti per l’utilizzo di A4T:

* Per utilizzare [!DNL Analytics] come origine per la generazione di rapporti per [!DNL Target], sia tu che la tua società dovete avere accesso ad [!DNL Analytics] e a [!DNL Target]. [Contatta il rappresentante del tuo account](/help/main/cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB) per accedere a queste soluzioni.
* L’origine per la generazione di rapporti è impostata per ogni attività. [!DNL Target] continua a raccogliere dati da utilizzare nelle attività di reportistica. I dati di [!DNL Target] restano disponibili per consentirti di basare un’attività sui dati raccolti da [!DNL Target].
* Per la generazione dei rapporti, utilizza un’origine o l’altra. Non è possibile raccogliere dati per una singola attività da entrambe le origini.
* Quando si utilizza A4T, tutte le metriche di successo disponibili per le attività sono metriche di [!DNL Analytics]. Tuttavia, se utilizzi at.js, la metrica di obiettivo può essere basata su una chiamata mbox. Ad esempio, puoi utilizzare le funzionalità di tracciamento dei clic predefinite di Target con A4T invece di implementare il codice di tracciamento dei clic di [!DNL Analytics]
* I rapporti di un’attività A4T visualizzati nell’interfaccia utente di [!DNL Target] contengono i dati di [!DNL Analytics]. Se ad esempio si utilizza la metrica [!UICONTROL Visitor] in [!DNL Target], si utilizza la metrica [!DNL Analytics] [!UICONTROL Visitor] e non la metrica [!DNL Target] [!UICONTROL Visitors], che ora è denominata [!UICONTROL Entrants]. Questa differenza è particolarmente importante per le metriche relative al traffico di base ([!UICONTROL Visitors], [!UICONTROL Visits], [!UICONTROL Page Views]) e per le metriche di conversione.
* Tutte le attività di [!DNL Target] esistenti continuano a utilizzare la raccolta dati di [!DNL Target] e non sono influenzate dall’abilitazione di A4T.
* È consentita una sola metrica basata su mbox quando si utilizza A4T.
* Una chiamata da server a server da [!DNL Target] ad [!DNL Analytics] invia informazioni sulle attività e sulle esperienze ad [!DNL Analytics]. Questa integrazione non comporta chiamate server aggiuntive per [!DNL Target] o [!DNL Analytics].

  In alcune situazioni, le classificazioni da [!DNL Target] ad [!DNL Analytics] non vanno a buon fine e le attività non mostrano i dati in [!DNL Analytics]. Consulta [Risoluzione di problemi relativi all’integrazione di Analytics e Target (A4T)](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md). Puoi inoltre [contattare l’Assistenza clienti](/help/main/cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB) per ulteriore supporto.

## Implementazione di A4T

Per informazioni sull’implementazione di A4T con at.js e [!DNL Adobe Experience Platform Web SDK], consulta [Implementazione di Analytics for  [!DNL Target] ](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md).

## Tipi di attività supportati {#section_F487896214BF4803AF78C552EF1669AA}

Le sezioni seguenti contengono informazioni sui tipi di attività supportati quando si utilizza [!DNL Adobe Experience Platform Web SDK] o at.js:

| Tipi di attività | Compatibile con A4T? | Note, se applicabili |
|--- |--- |--- |
| [Attività A/B con suddivisione manuale del traffico](/help/main/c-activities/t-test-ab/test-ab.md) | Sì |  |
| [Attività A/B con allocazione automatica](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | Sì | Consulta [Supporto A4T per attività di allocazione automatica e targeting automatico](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md). |
| [Attività A/B con targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md) | Sì | Il supporto A4T per le attività di Targeting automatico è ora supportato sia per [!DNL Platform Web SDK] che per at.js. |
| [Targeting delle esperienze (XT)](/help/main/c-activities/t-experience-target/experience-target.md) | Sì |  |
| [Test multivariato (MVT)](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) | Sì | Richiede metriche obiettivo basate su mbox per ottenere il rapporto [!UICONTROL Element Contribution]. Il report [!UICONTROL Element Contribution] non supporta attualmente le metriche [!DNL Analytics]. |
| [Attività di Automated Personalization (AP)](/help/main/c-activities/t-automated-personalization/automated-personalization.md) | No |  |
| [Attività di Consigli](/help/main/c-recommendations/recommendations.md) | Sì |  |
| [Qualsiasi attività con un’offerta di reindirizzamento](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md) | Sì |

Poiché tutti i tipi di attività non supportano ancora A4T, è consigliabile mantenere o implementare importanti mbox di conversione, ad esempio la mbox `orderConfirmPage`.

## Esempi di rapporti A4T {#section_F0A43A1CB2F04E8282B909E4D7034361}

Per visualizzare i report A4T in [!DNL Target], fai clic su **[!UICONTROL Activities]**, fai clic sull&#39;attività desiderata dall&#39;elenco che utilizza [!DNL Analytics] come origine per la generazione di rapporti, quindi fai clic sulla scheda **[!UICONTROL Reports]**.

>[!NOTE]
>
>È possibile utilizzare l&#39;elenco a discesa [!UICONTROL Reporting Source] nella parte superiore della pagina [!UICONTROL Activities] per visualizzare solo le attività che utilizzano A4T.

Per passare da [!UICONTROL Table View] a [!UICONTROL Graph View] del report, fai clic sull&#39;icona appropriata in alto a destra nel report.

La figura seguente mostra [!UICONTROL Graph View] di un report A4T con l&#39;elenco a discesa [!UICONTROL Report Metric] contenente le metriche obiettivo di [!DNL Analytics] disponibili:

![immagine a4t_report_graph1](assets/a4t_report_graph1.png)

La figura seguente mostra [!UICONTROL Graph View] di un report A4T con l&#39;elenco a discesa [!UICONTROL Audience] che mostra i tipi di pubblico [!DNL Analytics] disponibili:

![immagine a4t_report_graph2](assets/a4t_report_graph2.png)

La figura seguente mostra il [!UICONTROL Table View] di un rapporto A4T:

![immagine a4t_report_table](assets/a4t_report_table.png)

Per visualizzare il report in [!DNL Analytics] anziché in [!DNL Target], fare clic su **[!UICONTROL View in Analytics]** nella parte superiore del report.

## Esercitazione Analytics &amp; Target: Best Practices for Analysis {#section_3438E6E77A464424B717A4FD333B84B2}

Apri l’esercitazione [Analytics e Target: best practice per l&#39;analisi](https://spark.adobe.com/page/Lo3Spm4oBOvwF/), fornita da [!DNL Adobe Experience League].

## Video di formazione:

I video seguenti contengono ulteriori informazioni sui concetti descritti in questo argomento.

### Analytics for Adobe Target (A4T) (4:32) ![Icona panoramica](/help/main/assets/overview.png)

Questo video spiega come usare [!DNL Analytics] come origine per la generazione di rapporti in [!DNL Target] per l’analisi del tuo programma di ottimizzazione.

* Cosa è A4T e perché utilizzarlo
* Come funziona A4T
* Prerequisiti necessari prima di utilizzare A4T

>[!VIDEO](https://video.tv.adobe.com/v/17384)

### Integrazione di Analytics e Adobe Target (A4T) (40:33) ![Icona esercitazione](/help/main/assets/tutorial.png)

Questo video è una registrazione di “ [Office Hours](/help/main/cmp-resources-and-contact-information.md#concept_58EA30379D3B48C4848BA2A8C464A5B7)”, un’iniziativa condotta dal team di assistenza clienti Adobe.

* Configurare e convalidare il funzionamento dell&#39;integrazione
* Funzionamento dell&#39;integrazione
* Informazioni sui rapporti ideali da utilizzare in Analytics
* Risposte alle domande più frequenti su A4T

[Integrazione di Analytics e Adobe Target (A4T), Office Hours](https://helpx.adobe.com/it/customer-care-office-hours/target/analytics-target-A4T-integration.html)

>[!MORELIKETHIS]
>
>* [Implementazione di Analytics for  [!DNL Target] ](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md): contiene informazioni sull’implementazione per at.js e Platform Web SDK.
>* [Offerte di reindirizzamento: domande frequenti su A4T](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md)
>* [Cos’è Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=it): contiene informazioni generali su Platform Web SDK.
>* [Panoramica di Target](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/adobe-target/target-overview.html?lang=it): contiene informazioni specifiche di [!DNL Target] e [!DNL Platform Web SDK].
