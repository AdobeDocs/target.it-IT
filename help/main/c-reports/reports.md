---
keywords: report;bloccare indirizzo ip;bloccare visitatore da indirizzo ip;scaricare report;csv;reporting;reports;block ip address;block visitor from ip address;download reports;csv;reporting
description: Ottimizza le tue attività grazie alla padronanza delle funzionalità di reporting di  [!DNL Adobe Target] per migliorare il processo decisionale e aumentare il ROI.
title: Come posso visualizzare i rapporti?
feature: Reports
exl-id: c5710eb3-0c72-47f8-870d-df50453ecf08
TQID: https://experienceleague.adobe.com/aRp-t-Z-Hfu5O01RqfxnKyHHL2suM2ahkteDQJShGQI
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 947
ht-degree: 24%

---

# Rapporti

I report forniscono informazioni sull&#39;avanzamento e i risultati delle attività [!DNL Adobe Target] che consentono di prendere decisioni basate sui dati. I dati dei rapporti possono aiutarti a decidere quando terminare un’attività, a individuare l’esperienza o l’offerta vincente e a ottenere informazioni o risultati utili per determinare le azioni successive.

## Visualizzare un rapporto {#section_C4591A32F6D04C95A1AD5A377C27C28B}

1. Fai clic su **[!UICONTROL Attività]**, quindi sull’attività desiderata tra quelle elencate.

   Se hai numerose attività, puoi fare clic sull&#39;icona Filtro ( ![icona Filtro](/help/main/assets/icons/Filter.svg) ) per filtrare l&#39;elenco selezionando le opzioni dagli elenchi [!UICONTROL Tipo], [!UICONTROL Stato], [!UICONTROL Source per la generazione di rapporti], [!UICONTROL Compositore esperienza], [!UICONTROL Tipo di metrica], [!UICONTROL Metodo di decisione] e [!UICONTROL Source attività].

   Ad esempio, è possibile selezionare [!UICONTROL Test A/B] e [!UICONTROL Targeting esperienza] dall&#39;elenco a discesa [!UICONTROL Tipo] e [!UICONTROL Live] dall&#39;elenco a discesa [!UICONTROL Stato] per visualizzare solo le attività [!UICONTROL Test A/B] e [!UICONTROL Targeting esperienza] in stato attivo.

   Nella figura seguente viene illustrato l&#39;elenco a discesa [!UICONTROL Tipo] con due tipi selezionati: [!UICONTROL Test A/B] e [!UICONTROL Targeting esperienza]. I tre tipi di test A/B (Manuale, [Allocazione automatica](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) e [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md)) sono selezionati per impostazione predefinita. È possibile deselezionare uno o più tipi, in base alle esigenze.

   ![Filtrare i rapporti per tipo](/help/main/c-reports/assets/report-filters-refresh.png)

1. Fai clic sull&#39;attività desiderata dall&#39;elenco per visualizzarne la pagina [!UICONTROL Panoramica].

1. Fai clic sulla scheda **[!UICONTROL Rapporti]** nella barra a sinistra.

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

   * [!UICONTROL Esporta rapporto in CSV]
   * [!UICONTROL Esportare i dettagli ordine in CSV]

1. (Facoltativo) Fai clic sulle icone **[!UICONTROL Vista tabella]** ( ![Icona Vista tabella](/help/main/assets/icons/Table.svg) ) e **[!UICONTROL Vista grafico]** ( ![Icona Vista grafico](/help/main/assets/icons/GraphTrend.svg) ) per passare da un formato di reporting all&#39;altro.

   A seconda del tipo di rapporto selezionato, potrebbero essere disponibili altre visualizzazioni e rapporti:

   | Tipo di report | Visualizzazione |
   | --- | --- |
   | [[!UICONTROL Targeting automatico]](/help/main/c-activities/auto-target/auto-target-to-optimize.md) | Fai clic sulle icone **[!UICONTROL Segmenti automatizzati]** ( ![Rapporto Segmenti automatizzati](/help/main/assets/icons/AutomatedSegment.svg) ) o **[!UICONTROL Attributi importanti]** ( ![Icona Attributi importanti](/help/main/assets/icons/ViewList.svg) ).<ul><li>Il rapporto [[!UICONTROL Segmenti automatizzati]](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md) mostra in che modo i diversi visitatori rispondono in modo diverso alle offerte e alle esperienze nell&#39;attività [!UICONTROL Automated Personalization] o [!UICONTROL Targeting automatico]. Questo report mostra come i diversi segmenti automatizzati definiti dai modelli di personalizzazione [!DNL Target] hanno risposto alle offerte e alle esperienze dell&#39;attività.</li><li>Il report [[!UICONTROL Attributi importanti]](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md) mostra come, nelle diverse attività, i diversi attributi sono più (o meno) importanti per il modo in cui il modello decide di effettuare la personalizzazione. Questo rapporto mostra gli attributi principali che hanno influenzato il modello e la loro importanza relativa.</li></ul> |
   | [[!UICONTROL Automated Personalization]](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) | Oltre ai [[!UICONTROL report Riepilogo di Automated Personalization]](/help/main/c-reports/personalization-reports/reports-ap.md), puoi fare clic sulle icone **[!UICONTROL Segmenti automatizzati]** ( ![report Segmenti automatizzati](/help/main/assets/icons/AutomatedSegment.svg) ) o **[!UICONTROL Attributi importanti]** ( ![icona Attributi importanti](/help/main/assets/icons/ViewList.svg) ).<ul><li>Il rapporto [[!UICONTROL Segmenti automatizzati]](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md) mostra in che modo i diversi visitatori rispondono in modo diverso alle offerte e alle esperienze nell&#39;attività [!UICONTROL Automated Personalization] o [!UICONTROL Targeting automatico]. Questo report mostra come i diversi segmenti automatizzati definiti dai modelli di personalizzazione [!DNL Target] hanno risposto alle offerte e alle esperienze dell&#39;attività.</li><li>Il report [[!UICONTROL Attributi importanti]](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md) mostra come, nelle diverse attività, i diversi attributi sono più (o meno) importanti per il modo in cui il modello decide di effettuare la personalizzazione. Questo rapporto mostra gli attributi principali che hanno influenzato il modello e la loro importanza relativa.</li></ul> |
   | [[!UICONTROL Test multivariato]](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT) | Oltre al report [[!UICONTROL Prestazioni esperienza]](/help/main/c-reports/multivariate-test-reports/experience-performance-report.md), puoi fare clic sull&#39;icona [[!UICONTROL Contributo posizione]](/help/main/c-reports/multivariate-test-reports/location-contribution-report.md) ( ![Icona Contributo posizione](/help/main/assets/icons/LocationContribution.svg) ) per far sì che il report mostri il contributo in base alla posizione. |

## Informazioni di reporting aggiuntive per tipi di attività specifici {#section_DFE037B9E1C345D3B3BDFCB3AC0359CA}

Oltre alle informazioni di reporting generali presenti in questo argomento e nei relativi sottoargomenti, altrove nella guida sono disponibili ulteriori informazioni specifiche sui singoli tipi di attività:

| Tipo di attività | Dettagli |
|--- |--- |
| [[!UICONTROL Test A/B]](/help/main/c-activities/t-test-ab/test-ab.md) | Per comprendere l’incremento, l’affidabilità e gli approcci statistici utilizzati in [!DNL Target], consulta [Pianificare un test A/B](/help/main/c-activities/t-test-ab/sample-size-determination.md). |
| [Interpreta [!UICONTROL Allocazione automatica] report](/help/main/c-activities/automated-traffic-allocation/determine-winner.md) | Interpretare i risultati di un&#39;attività A/B [!UICONTROL Allocazione automatica] esaminando indicatori importanti, inclusi incremento e affidabilità, nell&#39;interfaccia utente [!DNL Target]. |
| [[!UICONTROL Targeting automatico]](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT) | Informazioni sul report [!UICONTROL Riepilogo] per le attività di AT. Per ulteriori informazioni, consulta [[!UICONTROL Riepilogo targeting automatico] Rapporto](/help/main/c-reports/personalization-reports/auto-target-summary-report.md).<br>Informazioni sui due rapporti [!UICONTROL Personalization Insights] per le attività di AT e AP: [!UICONTROL Rapporto Segmenti automatizzati] e [!UICONTROL Rapporto Attributi importanti]. Per ulteriori informazioni, consulta [Rapporti Approfondimenti personalizzazione](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md). |
| [[!UICONTROL Automated Personalization]](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) | Informazioni sui due rapporti [!UICONTROL Riepilogo Automated Personalization] per le attività di Personalizzazione automatizzata: [!UICONTROL Livello attività] e [!UICONTROL Livello offerta]. Per ulteriori informazioni, consulta [Rapporti di riepilogo di Automated Personalization](/help/main/c-reports/personalization-reports/reports-ap.md).<br>Informazioni sui due rapporti [!UICONTROL Personalization Insights] per le attività di AT e AP: [!UICONTROL Rapporto Segmenti automatizzati] e [!UICONTROL Rapporto Attributi importanti]. Per ulteriori informazioni, consulta [Rapporti Approfondimenti personalizzazione](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md). |
| [[!UICONTROL Test multivariato]](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT) | Informazioni sui due report per attività MVT: [!UICONTROL Prestazioni esperienza] e [!UICONTROL Contributo posizione]. Per ulteriori informazioni, vedere [Rapporto prestazioni esperienza](/help/main/c-reports/multivariate-test-reports/experience-performance-report.md) (MVT) e [Rapporto contributo posizione](/help/main/c-reports/multivariate-test-reports/location-contribution-report.md) (MVT). |
| [[!DNL Adobe Analytics] come Source di reporting per Adobe Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) | Informazioni sull&#39;utilizzo di [!DNL Adobe Analytics] come origine per la generazione di rapporti per [!DNL Target] (A4T). A4T consente di accedere ai rapporti di [!DNL Analytics] per le attività di [!DNL Target]. Per ulteriori informazioni, consulta [Creazione di rapporti di Analytics for Target (A4T)](/help/main/c-reports/analytics-for-target-a4t-reporting.md). |
| [[!DNL Target] generazione rapporti in [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md) | Informazioni sull&#39;integrazione tra [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/customer-journey-analytics){target=_blank} e [!DNL Target] che fornisce potenti strumenti di analisi per il programma di ottimizzazione che consentono di risparmiare tempo. |

## Blocca i dati di reporting dagli indirizzi IP specificati

Puoi fare in modo che i rapporti non conteggino i visitatori da indirizzi IP specificati. Questa opzione è utile, ad esempio, per bloccare i dati di reporting provenienti dai visitatori interni.

[Contattare l&#39;assistenza clienti](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) per configurare i filtri IP. Questo filtro non è applicabile quando si utilizza [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE) (A4T) come origine per la generazione di rapporti.
