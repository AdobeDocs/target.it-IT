---
keywords: rapporti;bloccare indirizzo ip;bloccare visitatore da indirizzo ip;scaricare rapporti;csv;reporting
description: Scopri come utilizzare le funzioni di reporting in Adobe [!DNL Target] per esaminare le prestazioni delle attività. Prendere decisioni migliori basate sui dati per aumentare il ROI.
title: Come Si Visualizzano I Rapporti?
feature: Rapporti
exl-id: c5710eb3-0c72-47f8-870d-df50453ecf08
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '860'
ht-degree: 63%

---

# Rapporti

I rapporti forniscono informazioni sull’avanzamento e i risultati delle attività [!DNL Adobe Target] che consentono di prendere decisioni basate sui dati. I dati dei rapporti possono aiutarti a decidere quando terminare un’attività, a individuare l’esperienza di offerta vincente e a ottenere informazioni o insegnamenti necessari per determinare le azioni successive.

## Visualizzare un rapporto {#section_C4591A32F6D04C95A1AD5A377C27C28B}

1. Fai clic su **[!UICONTROL Attività]**, quindi sull’attività desiderata tra quelle elencate.

   Se hai numerose attività, puoi filtrare l’elenco selezionando le opzioni che ti interessano dagli elenchi a discesa [!UICONTROL Tipo], [!UICONTROL Stato], [!UICONTROL Origine per i rapporti], [!UICONTROL Compositore esperienza], [!UICONTROL Tipo di metrica] e [!UICONTROL Origine attività].

   Ad esempio, puoi selezionare [!UICONTROL Test A/B] e [!UICONTROL Targeting esperienza] dall’elenco a discesa [!UICONTROL Tipo] e [!UICONTROL Live] dall’elenco a discesa [!UICONTROL Stato] per visualizzare solo i test A/B e le attività di targeting di esperienza che si trovano in uno stato attivo.

   Nella figura seguente viene mostrato l’elenco a discesa [!UICONTROL Tipo] con due tipi selezionati:  [!UICONTROL Test A/B ] e targeting delle  [!UICONTROL esperienze]. I tre tipi di test A/B (Manuale, [Allocazione automatica](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) e [Targeting automatico](/help/c-activities/auto-target/auto-target-to-optimize.md)) sono selezionati per impostazione predefinita. È possibile deselezionare uno o più tipi, in base alle esigenze.

   ![Filtrare i rapporti per tipo](/help/c-reports/assets/report_filters-new.png)

1. Fai clic sulla scheda **[!UICONTROL Rapporti]**.

   Ogni rapporto include una legenda che ne facilita la comprensione.

   ![Legenda del rapporto](/help/c-reports/assets/report_menu_bar-new.png)

   Nella legenda vengono visualizzate le seguenti informazioni:

   * Lo stato dell’attività, compreso l’intervallo di date in cui l’attività è stata eseguita.
   * L’ [esperienza vincente proiettata](/help/c-activities/automated-traffic-allocation/determine-winner.md) (se disponibile).

   >[!NOTE]
   >
   >I risultati dell’esperienza compaiono dopo che questa è stata vista almeno da un partecipante.

1. (Facoltativo) [Configura il rapporto](/help/c-reports/c-report-settings/report-settings.md#concept_4BB6A7FDAB6F4806A632F9CD989B8BFA) come desideri.
1. (Facoltativo) [Scarica il rapporto in formato CSV](/help/c-reports/downloading-data-in-csv-file.md#concept_3F276FF2BBB2499388F97451D6DE2E75) per l&#39;analisi in Excel e altri programmi.

   Sono disponibili le seguenti opzioni:

   * [!UICONTROL Esportare un rapporto in formato CSV]
   * [!UICONTROL Esportare i dettagli ordine in CSV]

1. (Facoltativo) Fai clic su **[!UICONTROL Vista tabella]** e **[!UICONTROL Vista grafico]** per passare da un formato di reporting all’altro.

   ![Icone della vista Tabella e grafico](/help/c-reports/assets/table-and-graph-icons.png)

   A seconda del tipo di rapporto selezionato, potrebbero essere disponibili altre viste e rapporti:

   | Tipo di report | Visualizzazione |
   | --- | --- |
   | [Targeting automatico](/help/c-activities/auto-target/auto-target-to-optimize.md) | Fai clic sulle icone **[!UICONTROL Segmenti automatizzati]** o **[!UICONTROL Attributi importanti]** .<ul><li>Il rapporto [Segmenti automatizzati](/help/c-reports/c-personalization-insights-reports/automated-segments-report.md) mostra come i diversi visitatori rispondono in modo diverso alle offerte/esperienze nell&#39;attività di AP/AT. Questo rapporto mostra come i diversi segmenti automatizzati definiti dai modelli di personalizzazione di Target rispondono alle offerte/esperienze dell&#39;attività.</li><li>Il rapporto [Attributi importanti](/help/c-reports/c-personalization-insights-reports/important-attributes-report.md) mostra come, nelle diverse attività, i diversi attributi siano più (o meno) importanti per il modo in cui il modello decide di effettuare la personalizzazione. Questo rapporto mostra gli attributi principali che hanno influenzato il modello e la loro importanza relativa.</li></ul> |
   | [Personalizzazione automatizzata](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP) | Oltre ai [rapporti di riepilogo di Automated Personalization](/help/c-reports/reports-ap.md), puoi fare clic sulle icone **[!UICONTROL Segmenti automatizzati]** o **[!UICONTROL Attributi importanti]**.<ul><li>Il rapporto [Segmenti automatizzati](/help/c-reports/c-personalization-insights-reports/automated-segments-report.md) mostra come i diversi visitatori rispondono in modo diverso alle offerte/esperienze nell&#39;attività di AP/AT. Questo rapporto mostra come i diversi segmenti automatizzati definiti dai modelli di personalizzazione di Target rispondono alle offerte/esperienze dell&#39;attività.</li><li>Il rapporto [Attributi importanti](/help/c-reports/c-personalization-insights-reports/important-attributes-report.md) mostra come, nelle diverse attività, i diversi attributi siano più (o meno) importanti per il modo in cui il modello decide di effettuare la personalizzazione. Questo rapporto mostra gli attributi principali che hanno influenzato il modello e la loro importanza relativa.</li></ul> |
   | [Test multivariato](/help/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT) | Oltre al [Rapporto Prestazioni esperienza](/help/c-reports/experience-performance-report.md), puoi fare clic sull&#39;icona [Contributo posizione](/help/c-reports/location-contribution-report.md) per far sì che il rapporto mostri il contributo in base alla posizione. |

## Informazioni aggiuntive di reporting per tipi di attività specifici {#section_DFE037B9E1C345D3B3BDFCB3AC0359CA}

Oltre alle informazioni di reporting generali presenti in questo argomento e nei relativi sottoargomenti, altrove nella guida sono disponibili ulteriori informazioni specifiche sui singoli tipi di attività:

| Tipo di attività | Dettagli |
|--- |--- |
| [Test A/B](/help/c-activities/t-test-ab/test-ab.md) | Per comprendere l’incremento, l’affidabilità e gli approcci statistici utilizzati in [!DNL Target], consulta [Pianificare un test A/B](/help/c-activities/t-test-ab/sample-size-determination.md). |
| [Interpretare i rapporti di allocazione automatica](/help/c-activities/automated-traffic-allocation/determine-winner.md) | Interpreta i risultati di un’attività A/B [!UICONTROL Allocazione automatica] esaminando importanti indicatori, tra cui incremento e affidabilità, nell’ interfaccia utente di [!DNL Target] . |
| [Targeting automatico](/help/c-activities/auto-target/auto-target-to-optimize.md) (AT) | Informazioni sul rapporto di [!UICONTROL Riepilogo] per le attività di AT. Per ulteriori informazioni, consulta [Rapporto di riepilogo del Targeting automatico](/help/c-reports/auto-target-summary-report.md).<br>Informazioni sui due rapporti [!UICONTROL Approfondimenti personalizzazione] per le attività di AT e AP: [!UICONTROL Segmenti automatizzati] e [!UICONTROL Attributi importanti]. Per ulteriori informazioni, consulta [Rapporti Approfondimenti personalizzazione](/help/c-reports/c-personalization-insights-reports/personalization-insights-reports.md). |
| [Personalizzazione automatizzata](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP) | Informazioni sui due [!UICONTROL rapporti di riepilogo per Personalizzazione automatizzata] per le attività di AP: [!UICONTROL Livello di attività ] [!UICONTROL Livello di offerta]. Per ulteriori informazioni, consulta [Rapporti di riepilogo per Personalizzazione automatizzata](/help/c-reports/reports-ap.md).<br>Informazioni sui due rapporti [!UICONTROL Approfondimenti personalizzazione] per le attività di AT e AP: [!UICONTROL Segmenti automatizzati] e [!UICONTROL Attributi importanti]. Per ulteriori informazioni, consulta [Rapporti Approfondimenti personalizzazione](/help/c-reports/c-personalization-insights-reports/personalization-insights-reports.md). |
| [Test multivariato](/help/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT) | Informazioni sui due rapporti per attività di MVT: [!UICONTROL Prestazioni esperienza] e [!UICONTROL Contributo posizione]. Per ulteriori informazioni, consulta [Rapporto Prestazioni esperienza](/help/c-reports/experience-performance-report.md) (MVT) e [Rapporto Contributo posizione](/help/c-reports/location-contribution-report.md) (MVT). |
| [Adobe Analytics come origine per la generazione di rapporti per Adobe Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T) | Informazioni sull’utilizzo di [!DNL Adobe Analytics] come origine per la generazione di rapporti per [!DNL Target]. A4T consente di accedere ai rapporti di [!DNL Analytics] per le attività di [!DNL Target]. Per ulteriori informazioni, consulta [Creazione di rapporti di Analytics for Target (A4T)](/help/c-reports/analytics-for-target-a4t-reporting.md). |

## Blocca dati di reporting da indirizzi IP specifici

Puoi fare in modo che i rapporti non conteggino i visitatori da indirizzi IP specificati. Questo è utile, ad esempio, per bloccare i dati di reporting dai visitatori interni.

[Contatta il Client Care per impostare i filtri IP. ](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) Questo filtro non si applica quando utilizzi [Analytics for Target](/help/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE) (A4T) come fonte dei rapporti.
