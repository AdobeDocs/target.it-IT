---
keywords: a4t;analytics;analytics for target;analytics reporting source;adobe analytics as the reporting source for target
description: Adobe Analytics for Target (A4T) è un’integrazione tra soluzioni che consente di creare attività basate su metriche di conversione e segmenti di pubblico di Analytics. Questa integrazione consente di utilizzare i rapporti di Analytics per esaminare i risultati. Se utilizzi Analytics come origine per la generazione di rapporti per un’attività, tutti i rapporti e le segmentazioni per tale attività si basano sulla raccolta di dati di Analytics.
title: Adobe Analytics come origine per la generazione di rapporti per Adobe Target (A4T)
feature: a4t general
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '1269'
ht-degree: 47%

---


# Adobe Analytics come origine per la generazione di rapporti per Adobe Target (A4T){#adobe-analytics-as-the-reporting-source-for-adobe-target-a-t}

[!DNL Adobe Analytics for Target] (A4T) è un&#39;integrazione tra più soluzioni che consente di creare attività basate sulle metriche di  [!DNL Analytics] conversione e sui segmenti di pubblico. L&#39;integrazione A4T consente di utilizzare i report [!DNL Analytics] per esaminare i risultati. Se utilizzate [!DNL Analytics] come origine di reporting per un&#39;attività, tutti i reporting e la segmentazione per tale attività si basano sulla raccolta di dati [!DNL Analytics].

## Panoramica di A4T {#section_92B66069210C40DBA937790E8CC596CF}

L&#39;integrazione [!DNL Analytics for Target] tra [!DNL Analytics] e [!DNL Target] fornisce potenti strumenti di analisi e di risparmio di tempo per il programma di ottimizzazione.

I tre vantaggi principali dell&#39;utilizzo di dati [!DNL Analytics] in [!DNL Target] sono:

* Gli addetti al marketing possono applicare dinamicamente [!DNL Analytics] metriche di successo o segmenti di reporting ai report di attività [!DNL Target] in qualsiasi momento. Non è necessario specificare tutte le impostazioni prima di eseguire l’attività.
* Un’unica fonte di dati elimina la varianza che si verifica quando si raccolgono dati in due sistemi distinti.
* L&#39;implementazione [!DNL Analytics] esistente raccoglie tutti i dati richiesti. Non è necessario implementare mbox sulle pagine al solo scopo di raccogliere dati per i rapporti. Sebbene sia comunque consigliabile implementare una mbox di conferma dell&#39;ordine per le attività [ Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP).

>[!IMPORTANT]
>
>Prima di iniziare a utilizzare A4T, è necessario richiedere che il tuo account sia predisposto per l’integrazione. Utilizza [questo modulo](https://www.adobe.com/go/audiences) per richiedere il provisioning.
>
>L&#39;integrazione che abilita [!DNL Analytics] come origine dati per [!DNL Target] (A4T) rappresenta la generazione successiva del plug-in Test&amp;Target al SiteCatalyst. Questo plug-in è stato dichiarato obsoleto, ma rimane supportato per i clienti che già lo utilizzano.

Se utilizzate [!DNL Analytics] come origine di reporting per un&#39;attività, tutte le attività di reporting e segmentazione per tale attività si basano su [!DNL Analytics].

Tutte le metriche [!DNL Analytics], comprese le metriche calcolate, sono disponibili in [!DNL Target] e nel report [!UICONTROL Target Activities] in [!DNL Analytics]. Analogamente, qualsiasi segmento disponibile in [!DNL Analytics] può essere applicato a entrambe le soluzioni. Potete applicare la metrica o l&#39;audience al report in [!DNL Target] dopo l&#39;avvio dell&#39;attività, o anche dopo il completamento dell&#39;attività.

Ogni metrica è inclusa, comprese quelle personalizzate o calcolate che sono integrate in [!DNL Analytics].

Dopo il periodo di classificazione, i dati sono visualizzati in questi rapporti circa un&#39;ora dopo essere stati raccolti dal sito. Tutte le metriche, i segmenti e i valori nei rapporti provengono dalla suite di rapporti selezionata quando si configura l’attività.

Considerazioni importanti per l’utilizzo di A4T:

* Per utilizzare [!DNL Analytics] come origine di reporting per [!DNL Target], sia voi che la società dovete avere accesso a [!DNL Analytics] e a [!DNL Target]. [Contatta il rappresentante del tuo account](/help/cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB) per accedere a queste soluzioni.
* L’origine per la generazione di rapporti è impostata per ogni attività. [!DNL Target] continua a raccogliere i dati da utilizzare nel reporting e  [!DNL Target] i dati sono ancora disponibili se si preferisce basare un&#39;attività sui dati raccolti da  [!DNL Target].
* Per la generazione dei rapporti, è necessario utilizzare un’origine o l’altra. Non è possibile raccogliere dati per una singola attività da entrambe le origini.
* Quando si utilizza A4T, tutte le metriche di successo disponibili per le attività sono [!DNL Analytics] metriche. Tuttavia, la metrica obiettivo può essere basata su una chiamata mbox. Ad esempio, puoi utilizzare le funzionalità di tracciamento dei clic predefinite di Target con A4T invece di dover implementare il codice di tracciamento dei clic [!DNL Analytics].
* Quando visualizzate il reporting di un&#39;attività A4T nell&#39;interfaccia utente [!DNL Target], state visualizzando i dati [!DNL Analytics]. Ad esempio, se utilizzi la metrica [!UICONTROL Visitor] in [!DNL Target], utilizzi la metrica [!DNL Analytics] [!UICONTROL Visitor], non la metrica [!DNL Target] [!UICONTROL Visitors], che ora è denominata [!UICONTROL Entrants]. Questa differenza è particolarmente importante per le metriche di traffico di base ([!UICONTROL Visitatori], [!UICONTROL Visite], [!UICONTROL Visualizzazioni pagina]) e per le metriche di conversione.
* Tutte le attività [!DNL Target] esistenti continuano a utilizzare la raccolta di dati [!DNL Target] e non vengono influenzate dall&#39;attivazione di A4T.
* È consentita una sola metrica basata su mbox quando si utilizza [!DNL Analytics] come origine di reporting.
* Una chiamata server-to-server da [!DNL Target] a [!DNL Analytics] invia informazioni sull&#39;attività e sull&#39;esperienza a [!DNL Analytics]. Questa integrazione non comporta chiamate server aggiuntive per [!DNL Target] o [!DNL Analytics].

   In alcune situazioni, la chiamata di classificazione da [!DNL Target] a [!DNL Analytics] potrebbe non riuscire e le attività non mostrano i dati in [!DNL Analytics]. In tal caso, consultate [Risoluzione dei problemi relativi all&#39;integrazione di Analytics e Target (A4T)](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md). È inoltre possibile [contattare Client Care](/help/cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB) per ulteriore assistenza.

## Tipi di attività supportati {#section_F487896214BF4803AF78C552EF1669AA}

La tabella seguente mostra quali tipi di attività supportano [!DNL Analytics] come origine di reporting in [!DNL Target] (A4T):

| Tipi di attività | Compatibile con A4T? | Note, se applicabili |
|--- |--- |--- |
| Attività A/B con suddivisione manuale del traffico | Sì |  |
| Attività A/B con Allocazione automatica | Sì | Consultate il supporto di [Analytics for Target (A4T) per le attività di allocazione automatica e di destinazione automatica](/help/c-integrating-target-with-mac/a4t/campaign-creation.md#a4t-aa). |
| Attività A/B con Targeting automatico | Sì | Consultate il supporto di [Analytics for Target (A4T) per le attività di allocazione automatica e di destinazione automatica](/help/c-integrating-target-with-mac/a4t/campaign-creation.md#a4t-aa). |
| Targeting esperienza (XT) | Sì |  |
| Test multivariato (MVT) | Sì | Richiede un obiettivo di metrica obiettivo basato su mbox per ottenere il report [!UICONTROL Contributo elemento].  Il report [!UICONTROL Element Contribution] attualmente non supporta le metriche [!DNL Analytics]. |
| Attività di Personalizzazione automatizzata (AP) | No |  |
| Attività di Consigli | Sì |  |
| App mobile | Sì | Supportato con l’SDK di Mobile Services, versione 4.13.1 o successiva.  Per ulteriori informazioni, consulta la [documentazione di Mobile Services](https://experienceleague.adobe.com/docs/mobile-services/using/home.html). |
| E-mail | No |  |
| API di consegna lato server | Sì | Per ulteriori informazioni, consulta [Lato server: implementare Target](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md). |
| SDK di NodeJS | Sì | Per ulteriori informazioni, consulta [Lato server: implementare Target](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md). |
| Integrazione del servizio Cloud di AEM 6.1 (o precedente) | No |  |
| Integrazione del servizio Cloud di AEM 6.2 (o successiva) | Sì | Per ulteriori informazioni, vedere [Integrazione con  Adobe Target](https://helpx.adobe.com/experience-manager/6-2/sites/administering/using/target.html) nella [!DNL Adobe Experience Manager] 6.2 documentazione. |
| Qualsiasi attività che utilizza un&#39;offerta di reindirizzamento | Sì | Ci sono requisiti minimi più severi per le offerte di reindirizzamento con A4T. Per ulteriori informazioni, consulta [Offerte di reindirizzamento - Domande frequenti su A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md). |
| Node.JS | Sì |  |

Poiché tutti i tipi di attività non supportano ancora A4T, si consiglia di mantenere o implementare mbox di conversione importanti, come la mbox `orderConfirmPage`.

## Esempi di report A4T {#section_F0A43A1CB2F04E8282B909E4D7034361}

Per visualizzare i report A4T in [!DNL Target], fare clic su **[!UICONTROL Activities]**, fare clic sull&#39;attività desiderata dall&#39;elenco che utilizza [!DNL Analytics] come origine di reporting, quindi fare clic sulla scheda **[!UICONTROL Reports]**.

>[!NOTE]
>
>È possibile utilizzare l’elenco a discesa [!UICONTROL Origine per la generazione di rapporti] nella parte superiore della pagina [!UICONTROL Attività] per visualizzare solo le attività che utilizzano [!DNL Analytics] come origine per la generazione di rapporti.

Potete passare dalla [!UICONTROL Visualizzazione tabella] alla [!UICONTROL Visualizzazione grafico] del rapporto facendo clic sull&#39;icona appropriata nella parte superiore destra del rapporto.

La figura seguente illustra la [!UICONTROL Vista grafico] di un rapporto A4T con l’elenco a discesa [!UICONTROL Metrica rapporto] contenente le metriche obiettivo di [!DNL Analytics] disponibili:

![](assets/a4t_report_graph1.png)

La figura seguente illustra la [!UICONTROL Vista grafico] di un rapporto A4T con l’elenco a discesa [!UICONTROL Pubblico] contenente i tipi di pubblico di [!DNL Analytics] disponibili:

![](assets/a4t_report_graph2.png)

La figura seguente illustra la [!UICONTROL Vista tabella] di un rapporto A4T:

![](assets/a4t_report_table.png)

Per visualizzare il rapporto in [!DNL Analytics] anziché in [!DNL Target], fai clic su **[!UICONTROL Visualizza in Analytics]** nella parte superiore del rapporto.

## Analytics &amp; Target: esercitazione sulle best practice per l&#39;analisi {#section_3438E6E77A464424B717A4FD333B84B2}

Apri [Analytics &amp; Target: Tecniche consigliate per l&#39;esercitazione Analisi](https://spark.adobe.com/page/Lo3Spm4oBOvwF/), fornita da [!DNL Adobe Experience League].

## Video di formazione:

I seguenti video contengono ulteriori informazioni sui concetti trattati in questo argomento.

### Analytics for Target (A4T) (4:32) ![Logo Panoramica](/help/assets/overview.png)

Questo video spiega come utilizzare [!DNL Analytics] come origine di reporting in [!DNL Target] per eseguire l&#39;analisi del programma di ottimizzazione.

* Cosa è A4T e perché utilizzarlo
* Come funziona A4T
* Prerequisiti necessari prima di utilizzare A4T

>[!VIDEO](https://video.tv.adobe.com/v/17384)

### Integrazione di Analytics/Target (A4T) (40:33) ![Logo di esercitazione](/help/assets/tutorial.png)

Questo video è una registrazione di “ [Office Hours](/help/cmp-resources-and-contact-information.md#concept_58EA30379D3B48C4848BA2A8C464A5B7)”, un’iniziativa condotta dal team di assistenza clienti Adobe.

* Configurare e convalidare il funzionamento dell&#39;integrazione
* Funzionamento dell&#39;integrazione
* Informazioni sui rapporti ideali da utilizzare in Analytics
* Risposte alle domande più frequenti su A4T

[Ore di ufficio integrazione Analytics/Target (A4T)](https://helpx.adobe.com/customer-care-office-hours/target/analytics-target-A4T-integration.html)