---
keywords: faq;domande frequenti;analytics for target;a4T;metriche;definizioni metriche
description: Trova le risposte alle domande sulle definizioni delle metriche e sull’utilizzo di Analytics per le attività [!DNL Target] (A4T). A4T lets you use Analytics reporting with Adobe [!DNL Target] .
title: Dove posso trovare informazioni sulle definizioni delle metriche con A4T?
feature: Analytics for Target (A4T)
exl-id: 97442622-ba6d-46f8-bfac-72638875d889
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 40%

---

# Definizioni delle metriche - Domande frequenti su A4T

Questo argomento contiene le risposte alle domande più frequenti sulle definizioni metriche e sull’utilizzo di [!DNL Adobe Analytics] come origine per la generazione di rapporti per [!DNL Adobe Target] (A4T).

## Qual è la scadenza per l’appartenenza all’attività? Per quanto tempo dopo che i visitatori accedono all’attività, le loro azioni vengono conteggiate nell’attività se non la visualizzano nuovamente? {#section_41B4958F33534E4B96DEE0C981227A79}

La scadenza predefinita per un’attività è di 90 giorni dopo l’ultima interazione di un visitatore con l’attività. Se necessario, questa impostazione può essere regolata da ClientCare. Tuttavia, questa impostazione è globale per tutte le attività, quindi non deve essere regolata per un solo caso.

## Durante la configurazione delle metriche dell’obiettivo, perché non posso accedere alle opzioni Impostazioni avanzate? {#adv-settings}

Le opzioni [!UICONTROL Impostazioni avanzate] non sono disponibili per le attività che utilizzano [!DNL Analytics] come origine per la generazione di rapporti (A4T).

Per le attività che utilizzano A4T, la metrica obiettivo utilizza sempre le impostazioni &quot;[!UICONTROL Incrementa il conteggio e mantieni l’utente in attività]&quot; e &quot;[!UICONTROL Su ogni impression]&quot;. Queste impostazioni sono *non* configurabili.

Per le attività non A4T, puoi utilizzare le [opzioni Impostazioni avanzate](/help/c-activities/r-success-metrics/success-metrics.md#section_7CE95A2FA8F5438E936C365A6D43BC5B) per gestire il modo in cui misurare il successo. Le opzioni includono l’aggiunta di dipendenze, la scelta se mantenere o rimuovere l’utente nell’attività e se contare la metrica una volta per partecipante o su ogni impression. Per accedere alle opzioni [!UICONTROL Impostazioni avanzate] in un’attività non A4T, fai clic sui puntini di sospensione verticali > [!UICONTROL Impostazioni avanzate], come illustrato di seguito:

![Impostazioni avanzate](/help/c-activities/r-success-metrics/assets/advanced-settings.png)

## Quali sono le metriche calcolate e come sostituiscono la mbox SiteCatalyst:Event che utilizzo abitualmente? {#section_D59F4719E6B94758A2187427C17F8EF3}

Le metriche calcolate consentono di creare metriche personalizzate derivate da segmenti o calcoli matematici. In passato, potresti aver utilizzato la mbox `SiteCatlayst:Event` dove `evar27=shoes` e l’evento è `purchase` (acquisto). Ora crei un segmento in cui `evar27=shoes` e quindi crei una metrica calcolata in cui l’evento è `purchase` (acquisto) con il segmento applicato. Queste metriche possono essere create in qualsiasi momento, anche dopo che l’attività è in corso. Possono quindi essere utilizzate in qualsiasi rapporto in Analytics.

## A4T attribuisce conversioni a più campagne?  {#section_7F15C727206440CD86B3A8CE77087DF9}

Sì, utilizzando l’impostazione &quot;Allocazione completa&quot;.
