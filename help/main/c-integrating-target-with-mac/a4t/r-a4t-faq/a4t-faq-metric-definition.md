---
keywords: faq;domande frequenti;analytics for target;a4T;metriche;definizioni metriche
description: Risposte alle domande sulle definizioni delle metriche e sull'utilizzo di Analytics per  [!DNL Target]  (A4T). A4T consente di utilizzare il reporting di Analytics con le attività Adobe [!DNL Target] .
title: Dove posso trovare informazioni sulle definizioni delle metriche con A4T?
feature: Analytics for Target (A4T)
exl-id: 97442622-ba6d-46f8-bfac-72638875d889
source-git-commit: aff96eca1380f4274dba0c1567f6e41d42f4b5ab
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 31%

---

# Definizioni delle metriche - Domande frequenti su A4T

Questo argomento contiene le risposte alle domande più frequenti sulle definizioni delle metriche e sull&#39;utilizzo di [!DNL Adobe Analytics] come origine per la generazione di rapporti per [!DNL Adobe Target] (A4T).

## Qual è la scadenza per l’appartenenza all’attività? Per quanto tempo dopo che i visitatori accedono all’attività, le loro azioni vengono conteggiate nell’attività se non la visualizzano nuovamente? {#section_41B4958F33534E4B96DEE0C981227A79}

+++Risposta
La scadenza predefinita per l’attività è di 90 giorni dopo l’ultima interazione del visitatore con l’attività. Se necessario, questa impostazione può essere regolata dall’assistenza clienti. Tuttavia, questa impostazione è globale per tutte le attività, quindi non deve essere regolata per un solo caso.

+++

## Perché non posso accedere alle opzioni Impostazioni avanzate durante la configurazione delle metriche dell’obiettivo? {#adv-settings}

+++Risposta
Le opzioni [!UICONTROL Advanced Settings] non sono disponibili per le attività che utilizzano [!DNL Analytics] come origine per la generazione di rapporti (A4T).

Per le attività che utilizzano A4T, la metrica di obiettivo utilizza sempre le impostazioni &quot;[!UICONTROL Increment Count & Keep User in Activity]&quot; e &quot;[!UICONTROL On Every Impression]&quot;. Queste impostazioni sono *non* configurabili.

Per le attività non A4T, puoi utilizzare le [opzioni Impostazioni avanzate](/help/main/c-activities/r-success-metrics/success-metrics.md#section_7CE95A2FA8F5438E936C365A6D43BC5B) per gestire la modalità di misurazione del successo. Le opzioni includono l’aggiunta delle dipendenze, la scelta di mantenere l’utente nell’attività o rimuoverlo e se contare la metrica una volta per partecipante o su ogni impression. Per accedere alle opzioni [!UICONTROL Advanced Settings] in un&#39;attività non A4T, fai clic sui puntini di sospensione verticali > [!UICONTROL Advanced Settings], come illustrato di seguito:

![Impostazioni avanzate](/help/main/c-activities/r-success-metrics/assets/advanced-settings.png)

+++

## Quali sono le metriche calcolate e come sostituiscono la mbox SiteCatalyst:Event che utilizzo abitualmente? {#section_D59F4719E6B94758A2187427C17F8EF3}

+++Risposta
Le metriche calcolate consentono di creare metriche personalizzate derivate da segmenti o calcoli matematici. In passato, potresti aver utilizzato la mbox `SiteCatlayst:Event` dove `evar27=shoes` e l’evento è `purchase` (acquisto). Ora crei un segmento in cui `evar27=shoes` e quindi crei una metrica calcolata in cui l’evento è `purchase` (acquisto) con il segmento applicato. Queste metriche possono essere create in qualsiasi momento, anche dopo che l’attività è in corso. Possono quindi essere utilizzate in qualsiasi rapporto in Analytics.

+++

## A4T attribuisce conversioni a più campagne? {#section_7F15C727206440CD86B3A8CE77087DF9}

+++Risposta
Sì, utilizzando l&#39;impostazione &quot;Allocazione completa&quot;.

+++