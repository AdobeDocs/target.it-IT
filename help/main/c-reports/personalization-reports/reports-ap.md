---
keywords: Targeting;AP reports;automated personalization reports;activity level report;offer level report;offer detail report;faq
description: Scopri come interpretare il rapporto di riepilogo di Automated Personalization in Adobe Target. Da questo rapporto puoi passare ai rapporti Segmenti automatizzati e Attributi importanti.
title: Come si utilizzano i rapporti di riepilogo di Automated Personalization?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Reports
exl-id: 2708eba4-72d5-4e6b-b01b-d27de03463b2
TQID: https://experienceleague.adobe.com/Gj9Jo0NHnSxGE4BpvFbd0SudYjbkP4yrV3GFHWHNPjw
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: e0eb8757-182f-49f3-94a4-1587d16f5094id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 702
ht-degree: 21%

---

# Rapporto di riepilogo per Automated Personalization

I report di riepilogo specializzati sono disponibili per gli utenti di [!UICONTROL attività Automated Personalization] in [!DNL Adobe Target].

>[!NOTE]
>
>[!UICONTROL Automated Personalization] è disponibile nella soluzione [!DNL Target Premium]. Non è disponibile in [!DNL Target Standard] senza una [licenza Target Premium](/help/main/c-intro/intro.md#premium).

1. Fai clic su **[!UICONTROL Attività]**, fai clic sull’attività di [!UICONTROL Personalizzazione automatica] desiderata dall’elenco, quindi fai clic sulla scheda **[!UICONTROL Rapporti]**.

   Se hai numerose attività, fai clic sull&#39;icona Filtro ( ![icona Filtro](/help/main/assets/icons/Filter.svg) ) per filtrare l&#39;elenco selezionando le opzioni dagli elenchi a discesa [!UICONTROL Tipo], [!UICONTROL Stato], [!UICONTROL Source per la generazione di rapporti], [!UICONTROL Compositore esperienza], [!UICONTROL Tipo di metrica] e [!UICONTROL Source attività].

1. (Facoltativo) Fai clic sull&#39;icona **[!UICONTROL Scarica]** ( ![Icona Scarica](/help/main/assets/icons/Download.svg) ) per scaricare la visualizzazione di riepilogo (ad esempio, confronto di traffico di controllo e di destinazione) suddivisa per tutte le metriche di successo disponibili.

La funzione [!UICONTROL Personalizzazione automatizzata] fornisce i seguenti rapporti:

* Livello di attività
* Livello di offerta
* Segmenti automatizzati
* Attributi importanti

## Report Activity Level (Livello di attività) {#section_6F72FC5C790B4492B3DCECBFFA971337}

Il rapporto a [!UICONTROL livello di attività] consente di confrontare le prestazioni di aggregazione dell&#39;utilizzo di un algoritmo di [!UICONTROL Personalizzazione automatizzata] per il contenuto fornito in modo casuale (controllo).

Si applicano comunque le regole standard di interpretazione dei risultati per il test A/B, tra cui incremento, affidabilità, trend, durata e così via. Per ulteriori informazioni sull&#39;interpretazione dei risultati, vedere [Calcoli statistici nei test A/Bn](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

## Report Offer Level (Livello di offerta) {#section_CAA6409879E349C6906E2BE8156D87A1}

Il rapporto a [!UICONTROL livello di offerta] per l’esperienza Foresta casuale confronta le prestazioni di ogni offerta applicata dall’algoritmo alla stessa offerta fornita casualmente (controllo). Pertanto, non devi confrontare le offerte tra loro in questa visualizzazione.

Fai clic sull&#39;algoritmo dell&#39;esperienza (Foresta casuale o controllo) per visualizzare il rapporto [!UICONTROL Livello offerta].

>[!NOTE]
>
>Un’icona dell’orologio indica che il modello dell’algoritmo è ancora in fase di generazione. Un’icona a forma di segno di spunta indica che l’algoritmo di base è stato stabilito.

Le offerte possono essere visualizzate all&#39;interno di [gruppi di reporting](/help/main/c-activities/t-automated-personalization/offer-reporting-groups-in-automated-personalization.md) e questi gruppi di reporting possono essere compressi ed espansi. Fare clic su **[!UICONTROL Controllo]** o **[!UICONTROL Destinato]** nella tabella per visualizzare le informazioni riportate per gruppi di reporting anziché per offerte.

## Segmenti automatizzati

Fai clic sull&#39;icona [!UICONTROL Segmenti automatizzati]. Questo rapporto mostra come i diversi visitatori rispondono in modo diverso alle offerte/esperienze nell&#39;attività di AP/AT. Questo rapporto mostra come i diversi segmenti automatizzati definiti dai modelli di personalizzazione di Target rispondono alle offerte/esperienze dell&#39;attività.

Per ulteriori informazioni, consulta [Rapporto Segmenti automatizzati](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md).

## Attributi importanti

Fai clic sull&#39;icona [!UICONTROL Attributi importanti]. Questo rapporto mostra come, nelle diverse attività, i diversi attributi sono più (o meno) importanti per il modo in cui il modello decide di personalizzare. Questo rapporto mostra gli attributi principali che hanno influenzato il modello e la loro importanza relativa.

Per ulteriori informazioni, vedere [Rapporto Attributi importanti](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md).

## Domande frequenti

### Perché esistono differenze nei dati tra i rapporti Livello di attività e Livello di offerta?

**[!UICONTROL Livello di attività] rapporto**: le visite registrate nel rapporto [!UICONTROL Livello di attività] acquisiscono il numero di visite alle esperienze di controllo rispetto al traffico &quot;mirato&quot;. Il traffico mirato include una combinazione di traffico di esplorazione e traffico personalizzato.

**Rapporto livello offerta**: le impression registrate nel rapporto [!UICONTROL Livello offerta] acquisiscono il numero di impression per ogni offerta. Pertanto, in un&#39;attività con più posizioni, il numero totale di visite registrate nel report [!UICONTROL Livello offerta] in tutti i gruppi di reporting è uguale al multiplo del numero di visite registrate per il traffico di controllo o di destinazione nel report [!UICONTROL Livello attività] per il numero totale di posizioni nell&#39;attività. Le impression del contenuto predefinito che si verificano nelle posizioni in cui il contenuto predefinito era un’opzione disponibile vengono registrate nel gruppo di offerte &quot;Contenuto predefinito&quot;. Le impression delle offerte non assegnate a un gruppo di reporting vengono registrate nel gruppo di offerte &quot;Non raggruppate&quot;.

>[!NOTE]
>
>Il numero di impression registrate nel report [!UICONTROL Livello offerta] potrebbe non essere un numero intero esatto multiplo del numero di visite registrate nel report [!UICONTROL Livello attività]. Ciò è dovuto a lievi discrepanze che si verificano nell’acquisizione del traffico di dati di segnalazione su Internet (il tasso di discrepanza tipico è inferiore al 5%). Pertanto, il numero di impression non sarà un multiplo esatto quando il numero di posizioni disponibili nell’attività è cambiato dopo l’attivazione dell’attività.
