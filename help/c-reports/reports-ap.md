---
keywords: Targeting;AP reports;automated personalization reports;activity level report;offer level report;offer detail report
description: I rapporti specializzati sono disponibili per gli utenti  attività Automated Personalization in  Adobe Target.
title: Rapporto di riepilogo per Personalizzazione automatizzata
feature: reports
uuid: 959b6814-9686-4741-8a79-5957e64f6209
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 72%

---


# ![PREMIUM](/help/assets/premium.png) Rapporti di riepilogo per Personalizzazione automatizzata{#automated-personalization-summary-reports}

Specialized reports are available to users of [!UICONTROL Automated Personalization] activities in [!DNL Adobe Target].

>[!NOTE]
>
>La [!UICONTROL personalizzazione automatizzata] è disponibile come parte della soluzione [!DNL Target Premium]. Non è disponibile in [!DNL Target Standard] senza una licenza [Target Premium](/help/c-intro/intro.md#premium).

1. Fai clic su **[!UICONTROL Attività]**, fai clic sull’attività di [!UICONTROL Personalizzazione automatica] desiderata dall’elenco, quindi fai clic sulla scheda **[!UICONTROL Rapporti]**.

   Se hai numerose attività, puoi filtrare l’elenco selezionando [!UICONTROL Personalizzazione automatizzata] dall’elenco a discesa [!UICONTROL Tipo].

1. (Facoltativo) Fai clic sull&#39;icona [!UICONTROL Scarica] per scaricare il riepilogo (ad esempio, il confronto tra il Controllo e il Traffico mirato) con suddivisione in base a tutte le metriche di successo disponibili.

La funzione [!UICONTROL Personalizzazione automatizzata] fornisce i seguenti rapporti:

## Report Activity Level (Livello di attività){#section_6F72FC5C790B4492B3DCECBFFA971337}

Il rapporto a [!UICONTROL livello di attività] consente di confrontare le prestazioni di aggregazione dell&#39;utilizzo di un algoritmo di [!UICONTROL Personalizzazione automatizzata] per il contenuto fornito in modo casuale (controllo).

![Rapporto a livello di attività](/help/c-reports/assets/box_plot_ap.png)

Si applicano comunque le regole standard di interpretazione dei risultati per il test A/B, tra cui incremento, affidabilità, trend, durata e così via. Per ulteriori informazioni sull’interpretazione dei risultati, vedi [Tasso di conversione](/help/c-reports/conversion-rate.md#concept_2D9FEDE8F94A485DAC86D611BFBDC844).

## Report Offer Level (Livello di offerta){#section_CAA6409879E349C6906E2BE8156D87A1}

Il rapporto a [!UICONTROL livello di offerta] per l’esperienza Foresta casuale confronta le prestazioni di ogni offerta applicata dall’algoritmo alla stessa offerta fornita casualmente (controllo). Pertanto, non devi confrontare le offerte tra loro in questa visualizzazione.

Click the experience algorithm (Random Forest or control) to view the [!UICONTROL Offer Level] report.

![](assets/ap_OfferLevelRpt.png)

Le offerte possono essere visualizzate all’interno di gruppi di rapporti, che possono essere compressi e espansi. Seleziona [!UICONTROL Gruppo di rapporti] nell’elenco a discesa per visualizzare le informazioni aggregate da gruppi di rapporti, anziché da offerte.

>[!NOTE]
>
>L’icona dell’orologio indica che il modello dell’algoritmo è ancora in corso. L’icona di spunta indica che l’algoritmo di base è stato determinato.

## Segmenti automatizzati

Fare clic sull&#39;icona Segmenti  automatizzati. Questo rapporto mostra il modo in cui i diversi visitatori rispondono in modo diverso alle offerte/esperienze nell&#39;attività AP/AT. Questo rapporto mostra come i diversi segmenti automatizzati definiti dai modelli di personalizzazione di Target rispondono alle offerte/esperienze dell&#39;attività.

![Icona segmenti automatizzati](/help/c-reports/assets/icon-automated-sements-ap.png)

Per ulteriori informazioni, consulta Rapporto [Segmenti](/help/c-reports/c-personalization-insights-reports/automated-segments-report.md)automatizzati.

## Attributi importanti

Fate clic sull&#39;icona [!UICONTROL Attributi] importanti. Questo rapporto mostra come, in attività diverse, attributi diversi siano più (o meno) importanti per il modo in cui il modello decide di personalizzare. Questo rapporto mostra gli attributi principali che hanno influenzato il modello e la loro importanza relativa.

![Icona importanti attributi](/help/c-reports/assets/icon-important-attributes-ap.png)

Per ulteriori informazioni, consulta Rapporto [Attributi](/help/c-reports/c-personalization-insights-reports/important-attributes-report.md)importanti.