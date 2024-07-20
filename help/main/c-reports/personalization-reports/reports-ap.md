---
keywords: Targeting;AP reports;automated personalization reports;activity level report;offer level report;offer detail report;faq
description: Scopri come interpretare il rapporto di riepilogo di Automated Personalization in Adobe Target. Da questo rapporto puoi passare ai rapporti Segmenti automatizzati e Attributi importanti.
title: Come si utilizzano i rapporti di riepilogo di Automated Personalization?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Vedi cosa è incluso in Target Premium."
feature: Reports
exl-id: 2708eba4-72d5-4e6b-b01b-d27de03463b2
source-git-commit: 07062b7df75300bd7558a24da5121df454520e42
workflow-type: tm+mt
source-wordcount: '647'
ht-degree: 12%

---

# Rapporto di riepilogo per Automated Personalization

I report di riepilogo specializzati sono disponibili per gli utenti di [!UICONTROL Automated Personalization] attività in [!DNL Adobe Target].

>[!NOTE]
>
>[!UICONTROL Automated Personalization] è disponibile nella soluzione [!DNL Target Premium]. Non è disponibile in [!DNL Target Standard] senza una [licenza Target Premium](/help/main/c-intro/intro.md#premium).

1. Fare clic su **[!UICONTROL Activities]**, selezionare l&#39;attività [!UICONTROL Automated Personalization] desiderata dall&#39;elenco, quindi fare clic sulla scheda **[!UICONTROL Reports]**.

   Se hai numerose attività, puoi filtrare l&#39;elenco selezionando [!UICONTROL Automated Personalization] dall&#39;elenco a discesa [!UICONTROL Type].

1. (Facoltativo) Fai clic sull&#39;icona **[!UICONTROL Download]** per scaricare la visualizzazione di riepilogo (ad esempio, confronto tra traffico di controllo e di destinazione) suddivisa per tutte le metriche di successo disponibili.

[!UICONTROL Automated Personalization] fornisce i seguenti rapporti:

* Livello di attività
* Livello di offerta
* Segmenti automatizzati
* Attributi importanti

## Report Activity Level (Livello di attività) {#section_6F72FC5C790B4492B3DCECBFFA971337}

Il report [!UICONTROL Activity Level] confronta le prestazioni aggregate dell&#39;utilizzo di un algoritmo [!UICONTROL Automated Personalization] con il contenuto (controllo) distribuito in modo casuale.

![Rapporto a livello di attività](/help/main/c-reports/assets/box_plot_ap.png)

Si applicano comunque le regole standard di interpretazione dei risultati per il test A/B, tra cui incremento, affidabilità, trend, durata e così via. Per ulteriori informazioni sull&#39;interpretazione dei risultati, vedere [Calcoli statistici nei test A/Bn](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

## Report Offer Level (Livello di offerta) {#section_CAA6409879E349C6906E2BE8156D87A1}

Il rapporto [!UICONTROL Offer Level] per l&#39;esperienza Foresta casuale confronta le prestazioni di ogni offerta applicata dall&#39;algoritmo con la stessa offerta distribuita in modo casuale (Controllo). Pertanto, in questa prospettiva, le offerte non devono essere confrontate tra loro.

Fare clic sull&#39;algoritmo dell&#39;esperienza (Foresta casuale o controllo) per visualizzare il report [!UICONTROL Offer Level].

![Rapporto a livello di offerta in Adobe Target](/help/main/c-reports/assets/ap_OfferLevelRpt.png)

>[!NOTE]
>
>Un’icona dell’orologio indica che il modello dell’algoritmo è ancora in fase di generazione. Un’icona a forma di segno di spunta indica che l’algoritmo di base è stato stabilito.

Le offerte possono essere visualizzate all&#39;interno di [gruppi di reporting](/help/main/c-activities/t-automated-personalization/offer-reporting-groups-in-automated-personalization.md) e questi gruppi di reporting possono essere compressi ed espansi. Fare clic su **[!UICONTROL Control]** o **[!UICONTROL Targeted]** nella tabella per visualizzare le informazioni riportate per gruppi di reporting anziché per offerte.

## Segmenti automatizzati

Fare clic sull&#39;icona [!UICONTROL Automated Segments]. Questo rapporto mostra come i diversi visitatori rispondono in modo diverso alle offerte/esperienze nell&#39;attività di AP/AT. Questo rapporto mostra come i diversi segmenti automatizzati definiti dai modelli di personalizzazione di Target rispondono alle offerte/esperienze dell&#39;attività.

![Icona Segmenti automatizzati](/help/main/c-reports/assets/icon-automated-sements-ap.png)

Per ulteriori informazioni, consulta [Rapporto Segmenti automatizzati](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md).

## Attributi importanti

Fare clic sull&#39;icona [!UICONTROL Important Attributes]. Questo rapporto mostra come, nelle diverse attività, i diversi attributi sono più (o meno) importanti per il modo in cui il modello decide di personalizzare. Questo rapporto mostra gli attributi principali che hanno influenzato il modello e la loro importanza relativa.

![Icona Attributi importanti](/help/main/c-reports/assets/icon-important-attributes-ap.png)

Per ulteriori informazioni, vedere [Rapporto Attributi importanti](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md).

## Domande frequenti

### Perché esistono differenze nei dati tra i rapporti Livello di attività e Livello di offerta?

Rapporto **[!UICONTROL Activity Level]**: le visite registrate nel rapporto [!UICONTROL Activity Level] acquisiscono il numero di visite alle esperienze di controllo rispetto al traffico &quot;mirato&quot;. Il traffico mirato include una combinazione di traffico di esplorazione e traffico personalizzato.

**Rapporto livello offerta**: le impression registrate nel rapporto [!UICONTROL Offer Level] acquisiscono il numero di impression per ogni offerta. Pertanto, in un&#39;attività con più posizioni, il numero totale di visite registrate nel rapporto [!UICONTROL Offer Level] in tutti i gruppi di reporting è uguale al multiplo del numero di visite registrate per il traffico di controllo o di destinazione nel rapporto [!UICONTROL Activity Level] per il numero totale di posizioni nell&#39;attività. Le impression del contenuto predefinito che si verificano nelle posizioni in cui il contenuto predefinito era un’opzione disponibile vengono registrate nel gruppo di offerte &quot;Contenuto predefinito&quot;. Le impression delle offerte non assegnate a un gruppo di reporting vengono registrate nel gruppo di offerte &quot;Non raggruppate&quot;.

>[!NOTE]
>
>Il numero di impression registrate nel report [!UICONTROL Offer Level] potrebbe non essere un numero intero esatto multiplo del numero di visite registrate nel report [!UICONTROL Activity Level]. Ciò è dovuto a lievi discrepanze che si verificano nell’acquisizione del traffico di dati di segnalazione su Internet (il tasso di discrepanza tipico è inferiore al 5%). Pertanto, il numero di impression non sarà un multiplo esatto quando il numero di posizioni disponibili nell’attività è cambiato dopo l’attivazione dell’attività.
