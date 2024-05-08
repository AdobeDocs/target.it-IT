---
keywords: report;bloccare indirizzo ip;bloccare visitatore da indirizzo ip;scaricare report;csv;reporting;reports;block ip address;block visitor from ip address;download reports;csv;reporting
description: Scopri come utilizzare le funzioni di reporting di Adobe [!DNL Target] per esaminare le prestazioni delle attività. Prendere decisioni migliori in base ai dati per aumentare il ROI.
title: Come posso visualizzare i rapporti?
feature: Reports
exl-id: c5710eb3-0c72-47f8-870d-df50453ecf08
source-git-commit: a7a03cba466fbe7abfc8eb1f80292e1a2de7fe2d
workflow-type: tm+mt
source-wordcount: '807'
ht-degree: 41%

---

# Rapporti

I rapporti forniscono informazioni sull’avanzamento e i risultati del [!DNL Adobe Target] attività che consentono di prendere decisioni basate sui dati. I dati dei rapporti possono aiutarti a decidere quando terminare un’attività, a individuare l’esperienza o l’offerta vincente e a ottenere informazioni o risultati utili per determinare le azioni successive.

## Visualizzare un rapporto {#section_C4591A32F6D04C95A1AD5A377C27C28B}

1. Fai clic su **[!UICONTROL Activities]**, quindi sull’attività desiderata tra quelle elencate.

   Se hai numerose attività, puoi filtrare l’elenco selezionando le opzioni dalla [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type], e [!UICONTROL Activity Source] elenchi a discesa.

   Ad esempio, puoi selezionare [!UICONTROL A/B Test] e [!UICONTROL Experience Targeting] dal [!UICONTROL Type] e [!UICONTROL Live] dal [!UICONTROL Status] per visualizzare solo i test A/B e le attività di Targeting esperienza in stato attivo.

   La figura seguente illustra [!UICONTROL Type] con due tipi selezionati: [!UICONTROL A/B Test] e [!UICONTROL Experience Targeting]. I tre tipi di test A/B (Manuale, [Allocazione automatica](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) e [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md)) sono selezionati per impostazione predefinita. È possibile deselezionare uno o più tipi, in base alle esigenze.

   ![Filtrare i rapporti per tipo](/help/main/c-reports/assets/report_filters-new.png)

1. Fai clic su **[!UICONTROL Reports]** scheda.

   Ogni rapporto include una legenda che ne facilita la comprensione.

   ![Legenda del rapporto](/help/main/c-reports/assets/report_menu_bar-new.png)

   Nella legenda vengono visualizzate le seguenti informazioni:

   * Lo stato dell’attività, compreso l’intervallo di date in cui l’attività è stata eseguita.
   * Il [esperienza vincente prevista](/help/main/c-activities/automated-traffic-allocation/determine-winner.md) (se disponibile).

   >[!NOTE]
   >
   >I risultati dell’esperienza compaiono dopo che questa è stata vista almeno da un partecipante.

1. (Facoltativo) [Configura il rapporto](/help/main/c-reports/c-report-settings/report-settings.md#concept_4BB6A7FDAB6F4806A632F9CD989B8BFA) come desideri.
1. (Facoltativo) [Scarica il rapporto in formato CSV](/help/main/c-reports/c-report-settings/downloading-data-in-csv-file.md) per l&#39;analisi in Excel e altri programmi.

   Sono disponibili le seguenti opzioni:

   * [!UICONTROL Export Report to CSV]
   * [!UICONTROL Export Order Details to CSV]

1. (Facoltativo) Fai clic su **[!UICONTROL Table View]** e **[!UICONTROL Graph View]** icone per passare da un formato di reporting all’altro.

   ![Icone della vista Tabella e Grafico](/help/main/c-reports/assets/table-and-graph-icons.png)

   A seconda del tipo di rapporto selezionato, potrebbero essere disponibili altre visualizzazioni e rapporti:

   | Tipo di report | Visualizzazione |
   | --- | --- |
   | [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md) | Fai clic su **[!UICONTROL Automated Segments]** o **[!UICONTROL Important Attributes]** icone.<ul><li>Il [Rapporto Segmenti automatizzati](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md) mostra in che modo i diversi visitatori rispondono in modo diverso alle offerte/esperienze nell’attività di AP/AT. Questo rapporto mostra come i diversi segmenti automatizzati definiti dai modelli di personalizzazione di Target rispondono alle offerte/esperienze dell&#39;attività.</li><li>Il [Rapporto Attributi importanti](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md) mostra come, nelle diverse attività, i diversi attributi sono più (o meno) importanti per il modo in cui il modello decide di personalizzare. Questo rapporto mostra gli attributi principali che hanno influenzato il modello e la loro importanza relativa.</li></ul> |
   | [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) | Oltre al [Rapporti di riepilogo di Automated Personalization](/help/main/c-reports/personalization-reports/reports-ap.md), è possibile fare clic su **[!UICONTROL Automated Segments]** o **[!UICONTROL Important Attributes]** icone.<ul><li>Il [Rapporto Segmenti automatizzati](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md) mostra in che modo i diversi visitatori rispondono in modo diverso alle offerte/esperienze nell’attività di AP/AT. Questo rapporto mostra come i diversi segmenti automatizzati definiti dai modelli di personalizzazione di Target rispondono alle offerte/esperienze dell&#39;attività.</li><li>Il [Rapporto Attributi importanti](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md) mostra come, nelle diverse attività, i diversi attributi sono più (o meno) importanti per il modo in cui il modello decide di personalizzare. Questo rapporto mostra gli attributi principali che hanno influenzato il modello e la loro importanza relativa.</li></ul> |
   | [Test multivariato](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT) | Oltre al [Rapporto Prestazioni esperienza](/help/main/c-reports/multivariate-test-reports/experience-performance-report.md), è possibile fare clic su [Contributo posizione](/help/main/c-reports/multivariate-test-reports/location-contribution-report.md) per far sì che il rapporto mostri il contributo in base alla posizione. |

## Informazioni di reporting aggiuntive per tipi di attività specifici {#section_DFE037B9E1C345D3B3BDFCB3AC0359CA}

Oltre alle informazioni di reporting generali presenti in questo argomento e nei relativi sottoargomenti, altrove nella guida sono disponibili ulteriori informazioni specifiche sui singoli tipi di attività:

| Tipo di attività | Dettagli |
|--- |--- |
| [Test A/B](/help/main/c-activities/t-test-ab/test-ab.md) | Per comprendere l’incremento, l’affidabilità e gli approcci statistici utilizzati in [!DNL Target], consulta [Pianificare un test A/B](/help/main/c-activities/t-test-ab/sample-size-determination.md). |
| [Interpretare i rapporti di allocazione automatica](/help/main/c-activities/automated-traffic-allocation/determine-winner.md) | Interpretare i risultati di un [!UICONTROL Auto-Allocate] attività A/B esaminando indicatori importanti, tra cui l&#39;incremento e l&#39;affidabilità, nel [!DNL Target] UI. |
| [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT) | Informazioni su [!UICONTROL Summary] rapporto per le attività di AT. Per ulteriori informazioni, consulta [Rapporto di riepilogo del Targeting automatico](/help/main/c-reports/personalization-reports/auto-target-summary-report.md).<br>Informazioni sui due [!UICONTROL Personalization Insights] rapporti per le attività di AT e AP: [!UICONTROL Automated Segments] rapporto e [!UICONTROL Important Attributes] rapporto. Per ulteriori informazioni, consulta [Rapporti Approfondimenti personalizzazione](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md). |
| [Personalizzazione automatizzata](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) | Informazioni sui due [!UICONTROL Automated Personalization Summary] rapporti per le attività di AP: [!UICONTROL Activity Level] rapporto e [!UICONTROL Offer Level] rapporto. Per ulteriori informazioni, consulta [Rapporti di riepilogo per Personalizzazione automatizzata](/help/main/c-reports/personalization-reports/reports-ap.md).<br>Informazioni sui due [!UICONTROL Personalization Insights] rapporti per le attività di AT e AP: [!UICONTROL Automated Segments] rapporto e [!UICONTROL Important Attributes] rapporto. Per ulteriori informazioni, consulta [Rapporti Approfondimenti personalizzazione](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md). |
| [Test multivariato](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT) | Informazioni sui due rapporti per le attività di MVT: [!UICONTROL Experience Performance] rapporto e [!UICONTROL Location Contribution] rapporto. Per ulteriori informazioni, consulta [Rapporto Prestazioni esperienza](/help/main/c-reports/multivariate-test-reports/experience-performance-report.md) (MVT) e [Rapporto Contributo posizione](/help/main/c-reports/multivariate-test-reports/location-contribution-report.md) (MVT). |
| [Adobe Analytics come origine per la generazione di rapporti per Adobe Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) | Informazioni sull’utilizzo di [!DNL Adobe Analytics] come origine per la generazione di rapporti per [!DNL Target]. A4T consente di accedere ai rapporti di [!DNL Analytics] per le attività di [!DNL Target]. Per ulteriori informazioni, consulta [Creazione di rapporti di Analytics for Target (A4T)](/help/main/c-reports/analytics-for-target-a4t-reporting.md). |
| [[!DNL Target] creazione di rapporti in [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md) | Informazioni sull’integrazione tra [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/customer-journey-analytics){target=_blank} e [!DNL Target] che offre potenti strumenti di analisi per il programma di ottimizzazione, garantendo tempi ridotti. |

## Blocca i dati di reporting dagli indirizzi IP specificati

Puoi fare in modo che i rapporti non conteggino i visitatori da indirizzi IP specificati. È utile, ad esempio, per bloccare i dati di reporting provenienti dai visitatori interni.

[Contatta l’Assistenza clienti](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) per impostare i filtri IP. Questo filtro non si applica quando si utilizza [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE) (A4T) come origine per la generazione di rapporti.
