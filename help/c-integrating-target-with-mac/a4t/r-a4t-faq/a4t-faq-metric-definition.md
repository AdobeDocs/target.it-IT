---
keywords: faq;frequently asked questions;analytics for target;a4T;metric;metric definitions
description: Questo argomento contiene le risposte alle domande più frequenti sulle definizioni metriche e sull’utilizzo di Analytics come origine per la creazione di rapporti per Target (A4T).
title: Definizioni delle metriche - Domande frequenti su A4T
feature: a4t troubleshooting
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 100%

---


# Definizioni delle metriche - Domande frequenti su A4T{#metric-definitions-a-t-faq}

Questo argomento contiene le risposte alle domande più frequenti sulle definizioni metriche e sull’utilizzo di Analytics come origine per la creazione di rapporti per Target (A4T).

## Qual è la scadenza per l’appartenenza all’attività? Per quanto tempo dopo che i visitatori accedono all’attività, le loro azioni vengono conteggiate nell’attività se non la visualizzano nuovamente? {#section_41B4958F33534E4B96DEE0C981227A79}

La scadenza predefinita per un’attività è di 90 giorni dopo l’ultima interazione di un visitatore con l’attività. Se necessario, questo valore può essere modificato dall’assistenza clienti. Tuttavia, questa impostazione è globale per tutte le attività, quindi non deve essere regolata per un solo caso.

## Le opzioni avanzate per le metriche di successo in Target funzionano con A4T? {#section_F060E3438F4144258BB95813EDEABDAA}

Queste opzioni non funzionano attualmente con A4T.

## Quali sono le metriche calcolate e come sostituiscono la mbox SiteCatalyst:Event che utilizzo abitualmente? {#section_D59F4719E6B94758A2187427C17F8EF3}

Le metriche calcolate consentono di creare metriche personalizzate derivate da segmenti o calcoli matematici. In passato, potresti aver utilizzato la mbox `SiteCatlayst:Event` dove `evar27=shoes` e l’evento è `purchase` (acquisto). Ora crei un segmento in cui `evar27=shoes` e quindi crei una metrica calcolata in cui l’evento è `purchase` (acquisto) con il segmento applicato. Il vantaggio è che queste metriche possono essere create in qualsiasi momento, anche quando l’attività è in corso. Possono quindi essere utilizzate in qualsiasi rapporto in Analytics.

## A4T attribuisce conversioni a più campagne? {#section_7F15C727206440CD86B3A8CE77087DF9}

Sì. Questa operazione viene eseguita utilizzando l’impostazione &quot;Allocazione completa&quot;.
