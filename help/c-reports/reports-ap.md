---
keywords: Targeting;report AP;report di personalizzazione automatizzata;report livello attività;report livello offerta;report dettagli offerta;faq
description: Come si utilizzano i rapporti di riepilogo di  Automated Personalization?
title: Report di riepilogo della Personalizzazione automatizzata
feature: Reports
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '649'
ht-degree: 42%

---


# ![PREMIUM](/help/assets/premium.png) Rapporti di riepilogo per Personalizzazione automatizzata

I rapporti di riepilogo specializzati sono disponibili per gli utenti di [!UICONTROL  attività Automated Personalization] in [!DNL Adobe Target].

>[!NOTE]
>
>La [!UICONTROL personalizzazione automatizzata] è disponibile come parte della soluzione [!DNL Target Premium]. Non è disponibile in [!DNL Target Standard] senza una licenza [Target Premium](/help/c-intro/intro.md#premium).

1. Fai clic su **[!UICONTROL Attività]**, fai clic sull’attività di [!UICONTROL Personalizzazione automatica] desiderata dall’elenco, quindi fai clic sulla scheda **[!UICONTROL Rapporti]**.

   Se hai numerose attività, puoi filtrare l’elenco selezionando [!UICONTROL Personalizzazione automatizzata] dall’elenco a discesa [!UICONTROL Tipo].

1. (Facoltativo) Fai clic sull&#39;icona **[!UICONTROL Scarica]** per scaricare il riepilogo (ad esempio, il confronto tra il Controllo e il Traffico mirato) con suddivisione in base a tutte le metriche di successo disponibili.

La funzione [!UICONTROL Personalizzazione automatizzata] fornisce i seguenti rapporti:

* Livello attività
* Livello offerta
* Segmenti automatizzati
* Attributi importanti

## Report Activity Level (Livello di attività){#section_6F72FC5C790B4492B3DCECBFFA971337}

Il rapporto a [!UICONTROL livello di attività] consente di confrontare le prestazioni di aggregazione dell&#39;utilizzo di un algoritmo di [!UICONTROL Personalizzazione automatizzata] per il contenuto fornito in modo casuale (controllo).

![Rapporto a livello di attività](/help/c-reports/assets/box_plot_ap.png)

Si applicano comunque le regole standard di interpretazione dei risultati per il test A/B, tra cui incremento, affidabilità, trend, durata e così via. Per ulteriori informazioni sull’interpretazione dei risultati, vedi [Tasso di conversione](/help/c-reports/conversion-rate.md#concept_2D9FEDE8F94A485DAC86D611BFBDC844).

## Report Offer Level (Livello di offerta){#section_CAA6409879E349C6906E2BE8156D87A1}

Il rapporto a [!UICONTROL livello di offerta] per l’esperienza Foresta casuale confronta le prestazioni di ogni offerta applicata dall’algoritmo alla stessa offerta fornita casualmente (controllo). Pertanto, non devi confrontare le offerte tra loro in questa visualizzazione.

Fate clic sull&#39;algoritmo dell&#39;esperienza (Foresta casuale o controllo) per visualizzare il rapporto [!UICONTROL Livello offerta].

![](assets/ap_OfferLevelRpt.png)

Le offerte possono essere visualizzate all’interno di gruppi di rapporti, che possono essere compressi e espansi. Seleziona [!UICONTROL Gruppo di rapporti] nell’elenco a discesa per visualizzare le informazioni aggregate da gruppi di rapporti, anziché da offerte.

>[!NOTE]
>
>L’icona dell’orologio indica che il modello dell’algoritmo è ancora in corso. L&#39;icona del segno di spunta indica che è stato stabilito l&#39;algoritmo di base.

## Segmenti automatizzati

Fare clic sull&#39;icona [!UICONTROL Segmenti automatizzati]. Questo rapporto mostra il modo in cui i diversi visitatori rispondono in modo diverso alle offerte/esperienze nell&#39;attività AP/AT. Questo rapporto mostra come i diversi segmenti automatizzati definiti dai modelli di personalizzazione di Target rispondono alle offerte/esperienze dell&#39;attività.

![Icona segmenti automatizzati](/help/c-reports/assets/icon-automated-sements-ap.png)

Per ulteriori informazioni, vedere [Rapporto Segmenti automatizzati](/help/c-reports/c-personalization-insights-reports/automated-segments-report.md).

## Attributi importanti

Fare clic sull&#39;icona [!UICONTROL Attributi importanti]. Questo rapporto mostra come, in attività diverse, attributi diversi siano più (o meno) importanti per il modo in cui il modello decide di personalizzare. Questo rapporto mostra gli attributi principali che hanno influenzato il modello e la loro importanza relativa.

![Icona importanti attributi](/help/c-reports/assets/icon-important-attributes-ap.png)

Per ulteriori informazioni, vedere [Report Attributi importanti](/help/c-reports/c-personalization-insights-reports/important-attributes-report.md).

## Domande frequenti 

### Perché ci sono differenze nei dati tra i rapporti Livello attività e Livello offerta?

**[!UICONTROL Report ] livello** attività: Le visite registrate nel report  [!UICONTROL Activity ] Levelreport acquisiscono il numero di visite alle esperienze di controllo rispetto a traffico &quot;mirato&quot;. Il traffico mirato include un mix di traffico di esplorazione e traffico personalizzato.

**Report** livello offerta: Le impression registrate nel report  [!UICONTROL Offer ] Levelreport acquisiscono il numero di impression per ogni offerta. Pertanto, in un&#39;attività con più di una posizione, il numero totale di visite registrate nel report [!UICONTROL Livello offerta] in tutti i gruppi di reporting è uguale al multiplo del numero di visite registrate per il traffico controllato o mirato nel report [!UICONTROL Livello attività] volte il numero totale di posizioni nell&#39;attività. Impression del contenuto predefinito che si verificano nelle posizioni in cui il contenuto predefinito era un&#39;opzione disponibile vengono registrate nel gruppo di offerte &quot;Contenuto predefinito&quot;. Le impression di offerte che non erano state assegnate a un gruppo di reporting sono registrate nel gruppo di offerte &quot;Non raggruppate&quot;.

>[!NOTE]
>
>Il numero di impression registrate nel report [!UICONTROL Livello offerta] potrebbe non essere un numero intero esatto multiplo del numero di visite registrate nel report [!UICONTROL Livello attività]. Ciò è dovuto a piccole discrepanze che si verificano nell&#39;acquisizione del traffico di dati di segnalazione via Internet (il tasso di discrepanza tipico è inferiore al 5%). Pertanto, il numero di impression non sarà un multiplo esatto quando il numero di posizioni disponibili nell&#39;attività cambierà dopo l&#39;attivazione dell&#39;attività.
