---
keywords: faq;frequently asked questions;analytics for target;a4T;metric;metric definitions
description: Questo argomento contiene le risposte alle domande più frequenti sulle definizioni metriche e sull’utilizzo di Analytics come origine per la creazione di rapporti per Target (A4T).
title: Definizioni delle metriche - Domande frequenti su A4T
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: cf47b7f3625bb1c3430b9fba00c573f489efc448
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 65%

---


# Definizioni delle metriche - Domande frequenti su A4T

Questo argomento contiene le risposte alle domande più frequenti sulle definizioni metriche e sull’utilizzo di Analytics come origine per la creazione di rapporti per Target (A4T).

## Qual è la scadenza per l’appartenenza all’attività? Per quanto tempo dopo che i visitatori accedono all’attività, le loro azioni vengono conteggiate nell’attività se non la visualizzano nuovamente? {#section_41B4958F33534E4B96DEE0C981227A79}

La scadenza predefinita per un’attività è di 90 giorni dopo l’ultima interazione di un visitatore con l’attività. Se necessario, questo valore può essere modificato dall’assistenza clienti. Tuttavia, questa impostazione è globale per tutte le attività, quindi non deve essere regolata per un solo caso.

## Durante la configurazione delle metriche degli obiettivi, perché non è possibile accedere alle opzioni delle impostazioni avanzate? {#adv-settings}

Le opzioni [!UICONTROL Impostazioni avanzate] non sono disponibili per le attività che utilizzano [!DNL Analytics] come origine di reporting (A4T).

Per le attività che utilizzano A4T, la metrica obiettivo utilizzerà sempre le impostazioni &quot;[!UICONTROL Increment Count &amp; Keep User in Activity]&quot; e &quot;[!UICONTROL On Every Impression]&quot;. È possibile configurare *not*.

Per le attività non A4T, potete utilizzare le [opzioni Impostazioni avanzate](/help/c-activities/r-success-metrics/success-metrics.md#section_7CE95A2FA8F5438E936C365A6D43BC5B) per gestire il modo in cui misurate il successo. Le opzioni includono l&#39;aggiunta di dipendenze, la scelta se mantenere l&#39;utente nell&#39;attività o rimuoverli, e se contare la metrica una volta per partecipante o su ogni impressione. Per accedere alle opzioni [!UICONTROL Impostazioni avanzate] in un&#39;attività non A4T, fare clic sulle ellissi verticali > [!UICONTROL Impostazioni avanzate], come illustrato di seguito:

![Impostazioni avanzate](/help/c-activities/r-success-metrics/assets/advanced-settings.png)

## Quali sono le metriche calcolate e come sostituiscono la mbox SiteCatalyst:Event che utilizzo abitualmente?  {#section_D59F4719E6B94758A2187427C17F8EF3}

Le metriche calcolate consentono di creare metriche personalizzate derivate da segmenti o calcoli matematici. In passato, potresti aver utilizzato la mbox `SiteCatlayst:Event` dove `evar27=shoes` e l’evento è `purchase` (acquisto). Ora crei un segmento in cui `evar27=shoes` e quindi crei una metrica calcolata in cui l’evento è `purchase` (acquisto) con il segmento applicato. Il vantaggio è che queste metriche possono essere create in qualsiasi momento, anche quando l’attività è in corso. Possono quindi essere utilizzate in qualsiasi rapporto in Analytics.

## A4T attribuisce conversioni a più campagne?  {#section_7F15C727206440CD86B3A8CE77087DF9}

Sì. Questa operazione viene eseguita utilizzando l’impostazione &quot;Allocazione completa&quot;.
