---
keywords: report;bloccare indirizzo ip;bloccare visitatore da indirizzo ip;scaricare report;csv;reporting;reports;block ip address;block visitor from ip address;download reports;csv;reporting
description: Ottimizza le tue attività grazie alla padronanza delle funzionalità di reporting di  [!DNL Adobe Target] per migliorare il processo decisionale e aumentare il ROI.
title: Come posso visualizzare i rapporti?
feature: Reports
exl-id: c5710eb3-0c72-47f8-870d-df50453ecf08
source-git-commit: bd65cb9339dbe4b79d26c314cfb81d1fc7226fd2
workflow-type: tm+mt
source-wordcount: '814'
ht-degree: 26%

---

# Rapporti

I report forniscono informazioni sull&#39;avanzamento e i risultati delle attività [!DNL Adobe Target] che consentono di prendere decisioni basate sui dati. I dati dei rapporti possono aiutarti a decidere quando terminare un’attività, a individuare l’esperienza o l’offerta vincente e a ottenere informazioni o risultati utili per determinare le azioni successive.

## Visualizzare un rapporto {#section_C4591A32F6D04C95A1AD5A377C27C28B}

1. Fai clic su **[!UICONTROL Activities]**, quindi sull’attività desiderata tra quelle elencate.

   Se hai numerose attività, puoi fare clic sull&#39;icona Filtro ( ![icona Filtro](/help/main/assets/icons/Filter.svg) ) per filtrare l&#39;elenco selezionando le opzioni dagli elenchi [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type], [!UICONTROL Decisioning Method] e [!UICONTROL Activity Source].

   Ad esempio, è possibile selezionare [!UICONTROL A/B Test] e [!UICONTROL Experience Targeting] dall&#39;elenco a discesa [!UICONTROL Type] e [!UICONTROL Live] dall&#39;elenco a discesa [!UICONTROL Status] per visualizzare solo le attività [!UICONTROL A/B Test] e [!UICONTROL Experience Targeting] in stato attivo.

   Nella figura seguente viene illustrato l&#39;elenco a discesa [!UICONTROL Type] con due tipi selezionati: [!UICONTROL A/B Test] e [!UICONTROL Experience Targeting]. I tre tipi di test A/B (Manuale, [Allocazione automatica](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) e [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md)) sono selezionati per impostazione predefinita. È possibile deselezionare uno o più tipi, in base alle esigenze.

   ![Filtrare i rapporti per tipo](/help/main/c-reports/assets/report-filters-refresh.png)

1. Fare clic sull&#39;attività desiderata dall&#39;elenco per visualizzare la relativa pagina [!UICONTROL Overview].

1. Fare clic sulla scheda **[!UICONTROL Reports]** nella barra a sinistra.

   ![Rapporto A/B](/help/main/c-reports/assets/reports-refresh.png)

   Ogni rapporto include una legenda che ne facilita la comprensione.

   Nella legenda vengono visualizzate le seguenti informazioni:

   * Lo stato dell’attività, compreso l’intervallo di date in cui l’attività è stata eseguita.
   * [esperienza vincente prevista](/help/main/c-activities/automated-traffic-allocation/determine-winner.md) (se disponibile).

   >[!NOTE]
   >
   >I risultati dell’esperienza compaiono dopo che questa è stata vista almeno da un partecipante.

1. (Facoltativo) [Configurare il report](/help/main/c-reports/c-report-settings/report-settings.md#concept_4BB6A7FDAB6F4806A632F9CD989B8BFA) facendo clic sull&#39;icona Impostazioni report ( ![icona Impostazioni report](/help/main/assets/icons/Setting.svg) ).
1. (Facoltativo) Fai clic sull&#39;icona Scarica rapporti ( ![icona Scarica rapporti](/help/main/assets/icons/Download.svg) ) per [scaricare il rapporto in formato CSV](/help/main/c-reports/c-report-settings/downloading-data-in-csv-file.md) per l&#39;analisi in Excel e altri strumenti.

   Sono disponibili le seguenti opzioni:

   * [!UICONTROL Export Report to CSV]
   * [!UICONTROL Export Order Details to CSV]

1. (Facoltativo) Fai clic sulle icone **[!UICONTROL Table View]** ( ![Vista tabella](/help/main/assets/icons/Table.svg) ) e **[!UICONTROL Graph View]** ( ![Vista grafico](/help/main/assets/icons/GraphTrend.svg) ) per passare da un formato di reporting all&#39;altro.

   A seconda del tipo di rapporto selezionato, potrebbero essere disponibili altre visualizzazioni e rapporti:

   | Tipo di report | Visualizzazione |
   | --- | --- |
   | [[!UICONTROL Auto-Target]](/help/main/c-activities/auto-target/auto-target-to-optimize.md) | Fai clic sulle icone **[!UICONTROL Automated Segments]** ( ![Rapporto Segmenti automatizzati](/help/main/assets/icons/AutomatedSegment.svg) ) o **[!UICONTROL Important Attributes]** ( ![Icona Attributi importanti](/help/main/assets/icons/ViewList.svg) ).<ul><li>Il report [[!UICONTROL Automated Segments]](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md) mostra in che modo i diversi visitatori rispondono in modo diverso alle offerte ed esperienze nell&#39;attività [!UICONTROL Automated Personalization] o [!UICONTROL Auto-Target]. Questo report mostra come i diversi segmenti automatizzati definiti dai modelli di personalizzazione [!DNL Target] hanno risposto alle offerte e alle esperienze dell&#39;attività.</li><li>Il report [[!UICONTROL Important Attributes]](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md) mostra come, nelle diverse attività, i diversi attributi sono più (o meno) importanti per il modo in cui il modello decide di personalizzare. Questo rapporto mostra gli attributi principali che hanno influenzato il modello e la loro importanza relativa.</li></ul> |
   | [[!UICONTROL Automated Personalization]](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) | Oltre ai [[!UICONTROL Automated Personalization Summary] report](/help/main/c-reports/personalization-reports/reports-ap.md), puoi fare clic sulle icone **[!UICONTROL Automated Segments]** ( ![report Segmenti automatizzati](/help/main/assets/icons/AutomatedSegment.svg) ) o **[!UICONTROL Important Attributes]** ( ![icona Attributi importanti](/help/main/assets/icons/ViewList.svg) ).<ul><li>Il report [[!UICONTROL Automated Segments]](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md) mostra in che modo i diversi visitatori rispondono in modo diverso alle offerte ed esperienze nell&#39;attività [!UICONTROL Automated Personalization] o [!UICONTROL Auto-Target]. Questo report mostra come i diversi segmenti automatizzati definiti dai modelli di personalizzazione [!DNL Target] hanno risposto alle offerte e alle esperienze dell&#39;attività.</li><li>Il report [[!UICONTROL Important Attributes]](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md) mostra come, nelle diverse attività, i diversi attributi sono più (o meno) importanti per il modo in cui il modello decide di personalizzare. Questo rapporto mostra gli attributi principali che hanno influenzato il modello e la loro importanza relativa.</li></ul> |
   | [[!UICONTROL Multivariate Test]](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT) | Oltre al report [[!UICONTROL Experience Performance]](/help/main/c-reports/multivariate-test-reports/experience-performance-report.md), è possibile fare clic sull&#39;icona [[!UICONTROL Location Contribution]](/help/main/c-reports/multivariate-test-reports/location-contribution-report.md) ( ![icona Contributo posizione](/help/main/assets/icons/LocationContribution.svg) ) per passare al report in modo che mostri il contributo in base alla posizione. |

## Informazioni di reporting aggiuntive per tipi di attività specifici {#section_DFE037B9E1C345D3B3BDFCB3AC0359CA}

Oltre alle informazioni di reporting generali presenti in questo argomento e nei relativi sottoargomenti, altrove nella guida sono disponibili ulteriori informazioni specifiche sui singoli tipi di attività:

| Tipo di attività | Dettagli |
|--- |--- |
| [[!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md) | Per comprendere l’incremento, l’affidabilità e gli approcci statistici utilizzati in [!DNL Target], consulta [Pianificare un test A/B](/help/main/c-activities/t-test-ab/sample-size-determination.md). |
| [Interpreta [!UICONTROL Auto-Allocate] report](/help/main/c-activities/automated-traffic-allocation/determine-winner.md) | Interpretare i risultati di un&#39;attività A/B di [!UICONTROL Auto-Allocate] esaminando indicatori importanti, inclusi incremento e affidabilità, nell&#39;interfaccia utente di [!DNL Target]. |
| [[!UICONTROL Auto-Target]](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT) | Informazioni sul report [!UICONTROL Summary] per le attività di AT. Per ulteriori informazioni, vedere [[!UICONTROL Auto-Target Summary] report](/help/main/c-reports/personalization-reports/auto-target-summary-report.md).<br>Informazioni sui due rapporti [!UICONTROL Personalization Insights] per le attività di AT e AP: [!UICONTROL Automated Segments] e [!UICONTROL Important Attributes]. Per ulteriori informazioni, consulta [Rapporti Approfondimenti personalizzazione](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md). |
| [[!UICONTROL Automated Personalization]](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) | Informazioni sui due rapporti [!UICONTROL Automated Personalization Summary] per le attività di Personalizzazione automatizzata: [!UICONTROL Activity Level] e [!UICONTROL Offer Level]. Per ulteriori informazioni, consulta [Rapporti di riepilogo per Personalizzazione automatizzata](/help/main/c-reports/personalization-reports/reports-ap.md).<br>Informazioni sui due rapporti [!UICONTROL Personalization Insights] per le attività di AT e AP: [!UICONTROL Automated Segments] e [!UICONTROL Important Attributes]. Per ulteriori informazioni, consulta [Rapporti Approfondimenti personalizzazione](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md). |
| [[!UICONTROL Multivariate Test]](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT) | Informazioni sui due report per attività MVT: [!UICONTROL Experience Performance] report e [!UICONTROL Location Contribution] report. Per ulteriori informazioni, vedere [Rapporto prestazioni esperienza](/help/main/c-reports/multivariate-test-reports/experience-performance-report.md) (MVT) e [Rapporto contributo posizione](/help/main/c-reports/multivariate-test-reports/location-contribution-report.md) (MVT). |
| [[!DNL Adobe Analytics] come Source di reporting per Adobe Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) | Informazioni sull&#39;utilizzo di [!DNL Adobe Analytics] come origine per la generazione di rapporti per [!DNL Target] (A4T). A4T consente di accedere ai rapporti di [!DNL Analytics] per le attività di [!DNL Target]. Per ulteriori informazioni, consulta [Creazione di rapporti di Analytics for Target (A4T)](/help/main/c-reports/analytics-for-target-a4t-reporting.md). |
| [[!DNL Target] generazione rapporti in [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md) | Informazioni sull&#39;integrazione tra [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/it/docs/customer-journey-analytics){target=_blank} e [!DNL Target] che fornisce potenti strumenti di analisi per il programma di ottimizzazione e consente di risparmiare tempo. |

## Blocca i dati di reporting dagli indirizzi IP specificati

Puoi fare in modo che i rapporti non conteggino i visitatori da indirizzi IP specificati. Questa opzione è utile, ad esempio, per bloccare i dati di reporting provenienti dai visitatori interni.

[Contattare l&#39;assistenza clienti](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) per configurare i filtri IP. Questo filtro non è applicabile quando si utilizza [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE) (A4T) come origine per la generazione di rapporti.
