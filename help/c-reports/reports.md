---
keywords: reports;block ip address;block visitor from ip address;download reports;csv;reporting
description: 'I report forniscono informazioni sulle prestazioni delle attività Adobe Target '
title: Rapporti
feature: reports
topic: Standard
uuid: 8d20f4e7-72fd-4872-a21f-54ce16a2d2ab
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '827'
ht-degree: 66%

---


# Rapporti{#reports}

Reports provide information about the progress and results of your [!DNL Adobe Target] activities that help you make decisions based on your data. I dati dei rapporti possono aiutarti a decidere quando terminare un&#39;attività, mostrare quale esperienza dell&#39;offerta è vincente e fornire informazioni o informazioni necessarie per determinare le azioni successive.

## Visualizzazione di un rapporto {#section_C4591A32F6D04C95A1AD5A377C27C28B}

1. Fai clic su **[!UICONTROL Attività]**, quindi sull’attività desiderata tra quelle elencate.

   Se hai numerose attività, puoi filtrare l’elenco selezionando le opzioni che ti interessano dagli elenchi a discesa [!UICONTROL Tipo], [!UICONTROL Stato], [!UICONTROL Origine per i rapporti], [!UICONTROL Compositore esperienza], [!UICONTROL Tipo di metrica] e [!UICONTROL Origine attività].

   Ad esempio, puoi selezionare [!UICONTROL Test A/B] e [!UICONTROL Targeting esperienza] dall’elenco a discesa [!UICONTROL Tipo] e [!UICONTROL Live] dall’elenco a discesa [!UICONTROL Stato] per visualizzare solo i test A/B e le attività di targeting di esperienza che si trovano in uno stato attivo.

   Nella figura seguente viene mostrato l’elenco a discesa [!UICONTROL Tipo] con due tipi selezionati: [!UICONTROL A/B Test] and [!UICONTROL Experience Targeting]. I tre tipi di test A/B (Manuale, [Allocazione automatica](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) e [Targeting automatico](/help/c-activities/auto-target/auto-target-to-optimize.md)) sono selezionati per impostazione predefinita. È possibile deselezionare uno o più tipi, in base alle esigenze.

   ![Filtrare i rapporti per tipo](/help/c-reports/assets/report_filters-new.png)

1. Fai clic sulla scheda **[!UICONTROL Rapporti]**.

   Ogni rapporto include una legenda che ne facilita la comprensione.

   ![Legenda del rapporto](/help/c-reports/assets/report_menu_bar-new.png)

   Nella legenda vengono visualizzate le seguenti informazioni:

   * Lo stato dell’attività, compreso l’intervallo di date in cui l’attività è stata eseguita.
   * The [projected winning experience](/help/c-activities/automated-traffic-allocation/determine-winner.md) (if available).

   >[!NOTE]
   >
   >I risultati dell’esperienza compaiono dopo che questa è stata vista almeno da un partecipante.

1. (Facoltativo) [Configura il rapporto](/help/c-reports/c-report-settings/report-settings.md#concept_4BB6A7FDAB6F4806A632F9CD989B8BFA) come desideri.
1. (Facoltativo) [Scarica il rapporto in formato CSV](/help/c-reports/downloading-data-in-csv-file.md#concept_3F276FF2BBB2499388F97451D6DE2E75) per l&#39;analisi in Excel e altri programmi.

   Sono disponibili le seguenti opzioni:

   * [!UICONTROL Esportare un rapporto in formato CSV]
   * [!UICONTROL Esportare i dettagli ordine in CSV]

1. (Facoltativo) Fai clic su **[!UICONTROL Vista tabella]** e **[!UICONTROL Vista grafico]** per passare da un formato di reporting all’altro.

   ![Icone di visualizzazione Tabella e Grafico](/help/c-reports/assets/table-and-graph-icons.png)

   A seconda del tipo di rapporto selezionato, potrebbero essere disponibili altre viste e rapporti:

   | Tipo di report | Visualizzazione |
   | --- | --- |
   | [Targeting automatico](/help/c-activities/auto-target/auto-target-to-optimize.md) | Fate clic sulle icone Segmenti **** automatizzati o Attributi **** importanti.<ul><li>The [Automated Segments report](/help/c-reports/c-personalization-insights-reports/automated-segments-report.md) shows how different visitors respond differently to the offers/experiences in your AP/AT activity. Questo rapporto mostra come i diversi segmenti automatizzati definiti dai modelli di personalizzazione di Target rispondono alle offerte/esperienze dell&#39;attività.</li><li>The [Important Attributes report](/help/c-reports/c-personalization-insights-reports/important-attributes-report.md) shows how, in different activities, different attributes are more (or less) important to how the model decides to personalize. Questo rapporto mostra gli attributi principali che hanno influenzato il modello e la loro importanza relativa.</li></ul> |
   | [Personalizzazione automatizzata](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP) | Oltre ai [rapporti](/help/c-reports/reports-ap.md)di riepilogo di Automated Personalization, puoi fare clic sulle icone Segmenti **** automatizzati o Attributi **** importanti.<ul><li>The [Automated Segments report](/help/c-reports/c-personalization-insights-reports/automated-segments-report.md) shows how different visitors respond differently to the offers/experiences in your AP/AT activity. Questo rapporto mostra come i diversi segmenti automatizzati definiti dai modelli di personalizzazione di Target rispondono alle offerte/esperienze dell&#39;attività.</li><li>The [Important Attributes report](/help/c-reports/c-personalization-insights-reports/important-attributes-report.md) hows how, in different activities, different attributes are more (or less) important to how the model decides to personalize. Questo rapporto mostra gli attributi principali che hanno influenzato il modello e la loro importanza relativa.</li></ul> |
   | [Test multivariato](/help/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT) | Oltre al rapporto [](/help/c-reports/experience-performance-report.md)Experience Performance, puoi fare clic sull’icona [Location Contribution (Contributo](/help/c-reports/location-contribution-report.md) posizione) per cambiare il rapporto e mostrare il contributo per posizione. |

## Additional reporting information for specific activity types {#section_DFE037B9E1C345D3B3BDFCB3AC0359CA}

Oltre alle informazioni di reporting generali presenti in questo argomento e nei relativi sottoargomenti, altrove nella guida sono disponibili ulteriori informazioni specifiche sui singoli tipi di attività:

| Tipo di attività | Dettagli |
|--- |--- |
| [Test A/B](/help/c-activities/t-test-ab/test-ab.md) | Per comprendere l’incremento, l’affidabilità e gli approcci statistici utilizzati in [!DNL Target], consulta [Pianificare un test A/B](/help/c-activities/t-test-ab/sample-size-determination.md). |
| [Interpretare i rapporti di allocazione automatica](/help/c-activities/automated-traffic-allocation/determine-winner.md) | Interpretate i risultati di un&#39;attività di allocazione [!UICONTROL automatica] A/B esaminando indicatori importanti, inclusi incrementi e confidenza, nell&#39; [!DNL Target] interfaccia utente. |
| [Targeting automatico](/help/c-activities/auto-target/auto-target-to-optimize.md) (AT) | Informazioni sul rapporto di [!UICONTROL Riepilogo] per le attività di AT. Per ulteriori informazioni, consulta [Rapporto di riepilogo del Targeting automatico](/help/c-reports/auto-target-summary-report.md).<br>Informazioni sui due rapporti [!UICONTROL Approfondimenti personalizzazione] per le attività di AT e AP: [!UICONTROL Segmenti automatizzati] e [!UICONTROL Attributi importanti]. Per ulteriori informazioni, consulta [Rapporti Approfondimenti personalizzazione](/help/c-reports/c-personalization-insights-reports/personalization-insights-reports.md). |
| [Personalizzazione automatizzata](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP) | Informazioni sui due [!UICONTROL rapporti di riepilogo per Personalizzazione automatizzata] per le attività di AP: [!UICONTROL Livello di attività ] [!UICONTROL Livello di offerta]. Per ulteriori informazioni, consulta [Rapporti di riepilogo per Personalizzazione automatizzata](/help/c-reports/reports-ap.md).<br>Informazioni sui due rapporti [!UICONTROL Approfondimenti personalizzazione] per le attività di AT e AP: [!UICONTROL Segmenti automatizzati] e [!UICONTROL Attributi importanti]. Per ulteriori informazioni, consulta [Rapporti Approfondimenti personalizzazione](/help/c-reports/c-personalization-insights-reports/personalization-insights-reports.md). |
| [Test multivariato](/help/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT) | Informazioni sui due rapporti per attività di MVT: [!UICONTROL Prestazioni esperienza] e [!UICONTROL Contributo posizione]. Per ulteriori informazioni, consulta [Rapporto Prestazioni esperienza](/help/c-reports/experience-performance-report.md) (MVT) e [Rapporto Contributo posizione](/help/c-reports/location-contribution-report.md) (MVT). |
| [Adobe Analytics come origine per la generazione di rapporti per Adobe Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T) | Informazioni sull’utilizzo di [!DNL Adobe Analytics] come origine per la generazione di rapporti per [!DNL Target]. A4T consente di accedere ai rapporti di [!DNL Analytics] per le attività di [!DNL Target]. Per ulteriori informazioni, consulta [Creazione di rapporti di Analytics for Target (A4T)](/help/c-reports/analytics-for-target-a4t-reporting.md). |

## Blocca dati di reporting da indirizzi IP specificati

Puoi fare in modo che i rapporti non conteggino i visitatori da indirizzi IP specificati. Questo è utile, ad esempio, per bloccare i dati di reporting dai visitatori interni.

[Contatta il Client Care per impostare i filtri IP. ](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) Questo filtro non si applica quando utilizzi [Analytics for Target](/help/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE) (A4T) come fonte dei rapporti.
