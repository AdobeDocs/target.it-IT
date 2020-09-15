---
keywords: a4t;analytics;analytics for target;analytics reporting source;adobe analytics as the reporting source for target
description: Adobe Analytics for Target (A4T) è un’integrazione tra soluzioni che consente di creare attività basate su metriche di conversione e segmenti di pubblico di Analytics. Questa integrazione consente di utilizzare i rapporti di Analytics per esaminare i risultati. Se utilizzi Analytics come origine per la generazione di rapporti per un’attività, tutti i rapporti e le segmentazioni per tale attività si basano sulla raccolta di dati di Analytics.
title: Adobe Analytics come origine per la generazione di rapporti per Adobe Target (A4T)
feature: a4t general
subtopic: Integrating
topic: Standard
uuid: 616798a6-1587-410f-9ac6-473beb39e3fc
translation-type: tm+mt
source-git-commit: b69a34023466fa2e348ed77ee41bc1cfdeb4e6ab
workflow-type: tm+mt
source-wordcount: '1271'
ht-degree: 47%

---


# Adobe Analytics come origine per la generazione di rapporti per Adobe Target (A4T){#adobe-analytics-as-the-reporting-source-for-adobe-target-a-t}

[!DNL Adobe Analytics for Target] (A4T) è un&#39;integrazione tra più soluzioni che consente di creare attività basate sulle metriche di [!DNL Analytics] conversione e sui segmenti di pubblico. The A4T integration lets you use [!DNL Analytics] reports to examine your results. If you use [!DNL Analytics] as the reporting source for an activity, all reporting and segmentation for that activity is based on [!DNL Analytics] data collection.

## Panoramica di A4T {#section_92B66069210C40DBA937790E8CC596CF}

The [!DNL Analytics for Target] integration between [!DNL Analytics] and [!DNL Target] provides powerful analysis and timesaving tools for your optimization program.

The three primary benefits of using [!DNL Analytics] data in [!DNL Target] are:

* Marketers can dynamically apply [!DNL Analytics] success metrics or reporting segments to [!DNL Target] activity reports at any time. Non è necessario specificare tutte le impostazioni prima di eseguire l’attività.
* Un’unica fonte di dati elimina la varianza che si verifica quando si raccolgono dati in due sistemi distinti.
* Your existing [!DNL Analytics] implementation collects all required data. Non è necessario implementare mbox sulle pagine al solo scopo di raccogliere dati per i rapporti. Although, it is still recommended that you implement an order confirmation mbox for [Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP) activities.

>[!IMPORTANT]
>
>Prima di iniziare a utilizzare A4T, è necessario richiedere che il tuo account sia predisposto per l’integrazione. Utilizza [questo modulo](https://www.adobe.com/go/audiences) per richiedere il provisioning.
>
>The integration that enables [!DNL Analytics] as the data source for [!DNL Target] (A4T) represents the next generation of the Test&amp;Target to SiteCatalyst plug-in. Questo plug-in è stato dichiarato obsoleto, ma rimane supportato per i clienti che già lo utilizzano.

If you use [!DNL Analytics] as the reporting source for an activity, all reporting and segmentation for that activity is based on [!DNL Analytics].

All [!DNL Analytics] metrics, including calculated metrics, are available in [!DNL Target] and the [!UICONTROL Target Activities] report in [!DNL Analytics]. Likewise, any segment available in [!DNL Analytics] can be applied to both solutions. You can apply the metric or audience to the report in [!DNL Target] after the activity has started, or even after the activity has completed.

Ogni metrica è inclusa, comprese quelle personalizzate o calcolate che sono integrate in [!DNL Analytics].

Dopo il periodo di classificazione, i dati sono visualizzati in questi rapporti circa un&#39;ora dopo essere stati raccolti dal sito. Tutte le metriche, i segmenti e i valori nei rapporti provengono dalla suite di rapporti selezionata quando si configura l’attività.

Considerazioni importanti per l’utilizzo di A4T:

* To use [!DNL Analytics] as the reporting source for [!DNL Target], both you and your company must have access to [!DNL Analytics] and to [!DNL Target]. [Contatta il rappresentante del tuo account](../../cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB) per accedere a queste soluzioni.
* L’origine per la generazione di rapporti è impostata per ogni attività. [!DNL Target] continua a raccogliere i dati da utilizzare nel reporting e [!DNL Target] i dati sono ancora disponibili se si preferisce basare un&#39;attività sui dati raccolti da [!DNL Target].
* Per la generazione dei rapporti, è necessario utilizzare un’origine o l’altra. Non è possibile raccogliere dati per una singola attività da entrambe le origini.
* When using A4T, all success metrics available to your activities are [!DNL Analytics] metrics. Tuttavia, la metrica obiettivo può essere basata su una chiamata mbox. For example, you can use Target&#39;s out-of-the-box click-tracking capabilities with A4T instead of having to implement [!DNL Analytics] click-tracking code.
* When viewing reporting of an A4T activity in the [!DNL Target] UI, you are viewing [!DNL Analytics] data. For example, if you use the [!UICONTROL Visitor] metric in [!DNL Target], you are using the [!DNL Analytics] [!UICONTROL Visitor] metric, not the [!DNL Target] [!UICONTROL Visitors] metric, which is now called [!UICONTROL Entrants]. This difference is especially important for basic traffic metrics ([!UICONTROL Visitors], [!UICONTROL Visits], [!UICONTROL Page Views]) and conversion metrics.
* Any existing [!DNL Target] activities continue to use [!DNL Target] data collection and are not affected by enabling A4T.
* Only one mbox-based metric is allowed when using [!DNL Analytics] as the reporting source.
* A server-to-server call from [!DNL Target] to [!DNL Analytics] sends activity and experience information to [!DNL Analytics]. This integration does not result in additional server calls for either [!DNL Target] or [!DNL Analytics].

   In alcune situazioni, la chiamata di classificazione da [!DNL Target] a [!DNL Analytics] potrebbe non riuscire e le attività non mostrano i dati in [!DNL Analytics]. In tal caso, consultate [Risoluzione dei problemi relativi all&#39;integrazione di Analytics e Target (A4T)](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md). Puoi anche [contattare Client Care](/help/cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB) per ulteriore assistenza.

## Supported activity types {#section_F487896214BF4803AF78C552EF1669AA}

The following table shows you which activity types support [!DNL Analytics] as the reporting source in [!DNL Target] (A4T):

| Tipi di attività | Compatibile con A4T? | Note, se applicabili |
|--- |--- |--- |
| Attività A/B con suddivisione manuale del traffico | Sì |  |
| Attività A/B con Allocazione automatica | Sì | Consultate Supporto di [Analytics per Target (A4T) per le attività](/help/c-integrating-target-with-mac/a4t/campaign-creation.md#a4t-aa)di allocazione automatica e di targeting automatico. |
| Attività A/B con Targeting automatico | Sì | Consultate Supporto di [Analytics per Target (A4T) per le attività](/help/c-integrating-target-with-mac/a4t/campaign-creation.md#a4t-aa)di allocazione automatica e di targeting automatico. |
| Targeting esperienza (XT) | Sì |  |
| Test multivariato (MVT) | Sì | Requires mbox-based goal metric goal to get the [!UICONTROL Element Contribution] report.  The [!UICONTROL Element Contribution] report does not currently support [!DNL Analytics] metrics. |
| Attività di Personalizzazione automatizzata (AP) | No |  |
| Attività di Consigli | Sì |  |
| App mobile | Sì | Supportato con l’SDK di Mobile Services, versione 4.13.1 o successiva.  Per ulteriori informazioni, consulta la [documentazione di Mobile Services](https://docs.adobe.com/content/help/en/mobile-services/using/home.html). |
| E-mail | No |  |
| API di consegna lato server | Sì | Per ulteriori informazioni, consulta [Lato server: implementare Target](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md). |
| SDK di NodeJS | Sì | Per ulteriori informazioni, consulta [Lato server: implementare Target](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md). |
| Integrazione del servizio Cloud di AEM 6.1 (o precedente) | No |  |
| Integrazione del servizio Cloud di AEM 6.2 (o successiva) | Sì | For more information, see [Integrating with Adobe Target](https://helpx.adobe.com/experience-manager/6-2/sites/administering/using/target.html) in the [!DNL Adobe Experience Manager] 6.2 documentation. |
| Qualsiasi attività che utilizza un&#39;offerta di reindirizzamento | Sì | Ci sono requisiti minimi più severi per le offerte di reindirizzamento con A4T. Per ulteriori informazioni, consulta [Offerte di reindirizzamento - Domande frequenti su A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md). |
| Node.JS | Sì |  |

Because all activity types do not yet support A4T, it is recommended that you keep or implement important conversion mboxes, such as the `orderConfirmPage` mbox.

## Examples of A4T reports {#section_F0A43A1CB2F04E8282B909E4D7034361}

To view A4T reports in [!DNL Target], click **[!UICONTROL Activities]**, click the desired activity from the list that uses [!DNL Analytics] as its reporting source, then click the **[!UICONTROL Reports]** tab.

>[!NOTE]
>
>È possibile utilizzare l’elenco a discesa [!UICONTROL Origine per la generazione di rapporti] nella parte superiore della pagina [!UICONTROL Attività] per visualizzare solo le attività che utilizzano [!DNL Analytics] come origine per la generazione di rapporti.

You can toggle between the [!UICONTROL Table View] and [!UICONTROL Graph View] of the report by clicking the appropriate icon at the top right side of the report.

La figura seguente illustra la [!UICONTROL Vista grafico] di un rapporto A4T con l’elenco a discesa [!UICONTROL Metrica rapporto] contenente le metriche obiettivo di [!DNL Analytics] disponibili:

![](assets/a4t_report_graph1.png)

La figura seguente illustra la [!UICONTROL Vista grafico] di un rapporto A4T con l’elenco a discesa [!UICONTROL Pubblico] contenente i tipi di pubblico di [!DNL Analytics] disponibili:

![](assets/a4t_report_graph2.png)

La figura seguente illustra la [!UICONTROL Vista tabella] di un rapporto A4T:

![](assets/a4t_report_table.png)

Per visualizzare il rapporto in [!DNL Analytics] anziché in [!DNL Target], fai clic su **[!UICONTROL Visualizza in Analytics]** nella parte superiore del rapporto.

## Analytics &amp; Target: esercitazione sulle best practice per l&#39;analisi {#section_3438E6E77A464424B717A4FD333B84B2}

Open the [Analytics &amp; Target: Best Practices for Analysis](https://spark.adobe.com/page/Lo3Spm4oBOvwF/) tutorial, provided by [!DNL Adobe Experience League].

## Video di formazione:

I seguenti video contengono ulteriori informazioni sui concetti trattati in questo argomento.

### Badge di ![panoramica di Analytics per Target (A4T) (4:32)](/help/assets/overview.png)

This video explains how to use [!DNL Analytics] as a reporting source in [!DNL Target] to drive the analysis of your optimization program.

* Cosa è A4T e perché utilizzarlo
* Come funziona A4T
* Prerequisiti necessari prima di utilizzare A4T

>[!VIDEO](https://video.tv.adobe.com/v/17384)

### Badge ![delle esercitazioni sull&#39;integrazione di Analytics/Target (A4T) (40:33)](/help/assets/tutorial.png)

Questo video è una registrazione di “ [Office Hours](../../cmp-resources-and-contact-information.md#concept_58EA30379D3B48C4848BA2A8C464A5B7)”, un’iniziativa condotta dal team di assistenza clienti Adobe.

* Configurare e convalidare il funzionamento dell&#39;integrazione
* Funzionamento dell&#39;integrazione
* Informazioni sui rapporti ideali da utilizzare in Analytics
* Risposte alle domande più frequenti su A4T

[Ore di ufficio integrazione Analytics/Target (A4T)](https://helpx.adobe.com/customer-care-office-hours/target/analytics-target-A4T-integration.html)