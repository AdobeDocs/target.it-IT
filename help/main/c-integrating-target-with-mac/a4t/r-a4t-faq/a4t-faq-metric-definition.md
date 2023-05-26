---
keywords: faq;domande frequenti;analytics for target;a4T;metriche;definizioni metriche
description: Risposte alle domande sulle definizioni delle metriche e sull’utilizzo di Analytics per [!DNL Target] (A4T). A4T consente di utilizzare il reporting di Analytics con Adobe [!DNL Target] attività.
title: Dove posso trovare informazioni sulle definizioni delle metriche con A4T?
feature: Analytics for Target (A4T)
exl-id: 97442622-ba6d-46f8-bfac-72638875d889
source-git-commit: aff96eca1380f4274dba0c1567f6e41d42f4b5ab
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 29%

---

# Definizioni delle metriche - Domande frequenti su A4T

Questo argomento contiene le risposte alle domande più frequenti sulle definizioni delle metriche e sull’utilizzo di [!DNL Adobe Analytics] come origine di reporting per [!DNL Adobe Target] (A4T).

## Qual è la scadenza per l’appartenenza all’attività? Per quanto tempo dopo che i visitatori accedono all’attività, le loro azioni vengono conteggiate nell’attività se non la visualizzano nuovamente? {#section_41B4958F33534E4B96DEE0C981227A79}

+++Risposta La scadenza predefinita per l’attività è di 90 giorni dopo l’ultima interazione del visitatore con l’attività. Se necessario, questa impostazione può essere regolata dall’assistenza clienti. Tuttavia, questa impostazione è globale per tutte le attività, quindi non deve essere regolata per un solo caso.

+++

## Perché non posso accedere alle opzioni Impostazioni avanzate durante la configurazione delle metriche dell’obiettivo? {#adv-settings}

+++Rispondi [!UICONTROL Impostazioni avanzate] non sono disponibili opzioni per le attività che utilizzano [!DNL Analytics] come origine per la generazione di rapporti (A4T)

Per le attività che utilizzano A4T, la metrica di obiettivo utilizza sempre il valore &quot;[!UICONTROL Incrementa il conteggio e mantieni l&#39;utente attivo]&quot; e &quot;[!UICONTROL A ogni impression]&quot;. Queste impostazioni sono *non* configurabile.

Per le attività non A4T, puoi utilizzare [Opzioni impostazioni avanzate](/help/main/c-activities/r-success-metrics/success-metrics.md#section_7CE95A2FA8F5438E936C365A6D43BC5B) per gestire come misurare il successo. Le opzioni includono l’aggiunta delle dipendenze, la scelta di mantenere l’utente nell’attività o rimuoverlo e se contare la metrica una volta per partecipante o su ogni impression. Accedi a [!UICONTROL Impostazioni avanzate] in un’attività non A4T facendo clic sui puntini di sospensione verticali > [!UICONTROL Impostazioni avanzate], come illustrato di seguito:

![Impostazioni avanzate](/help/main/c-activities/r-success-metrics/assets/advanced-settings.png)

+++

## Quali sono le metriche calcolate e come sostituiscono la mbox SiteCatalyst:Event che utilizzo abitualmente? {#section_D59F4719E6B94758A2187427C17F8EF3}

+++Rispondi alle metriche calcolate consente di creare metriche personalizzate derivate da segmenti o calcoli matematici. In passato, potresti aver utilizzato la mbox `SiteCatlayst:Event` dove `evar27=shoes` e l’evento è `purchase` (acquisto). Ora crei un segmento in cui `evar27=shoes` e quindi crei una metrica calcolata in cui l’evento è `purchase` (acquisto) con il segmento applicato. Queste metriche possono essere create in qualsiasi momento, anche dopo che l’attività è in corso. Possono quindi essere utilizzate in qualsiasi rapporto in Analytics.

+++

## A4T attribuisce conversioni a più campagne? {#section_7F15C727206440CD86B3A8CE77087DF9}

+++Rispondere Sì utilizzando l&#39;impostazione &quot;Allocazione completa&quot;.

+++