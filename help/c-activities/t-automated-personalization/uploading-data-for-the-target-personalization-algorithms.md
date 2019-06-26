---
description: I dati offline, ad esempio le informazioni CRM o i punteggi di propensione di abbandono dei clienti, possono essere estremamente utili nella generazione di modelli di personalizzazione.
seo-description: I dati offline, ad esempio le informazioni CRM o i punteggi di propensione di abbandono dei clienti, possono essere estremamente utili nella generazione di modelli di personalizzazione.
seo-title: Caricare dati per gli algoritmi di personalizzazione di Target
solution: Target
title: Caricare dati per gli algoritmi di personalizzazione di Target
topic: Premium
uuid: eb0938b9-7f35-4bb5-ac4b-260b2144db5b
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Caricare dati per gli algoritmi di personalizzazione Target{#upload-data-for-target-s-personalization-algorithms}

I dati offline, ad esempio le informazioni CRM o i punteggi di propensione di abbandono dei clienti, possono essere estremamente utili nella generazione di modelli di personalizzazione.

Sono disponibili diversi modi per immettere dati in algoritmi di Personalizzazione automatizzata (AP) e Targeting automatico. Oltre ai metodi descritti in [Metodi per immettere i dati in Target](../../c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md#concept_0069C0EFB56C4700BB33F2F35C2B9B17), nei nostri algoritmi vengono utilizzati anche i tipi di pubblico condivisi in Experience Cloud (Adobe Analytics, Audience Management) e quelli di reporting all’interno delle attività.

Per informazioni sui dati raccolti e utilizzati automaticamente dagli algoritmi di Personalizzazione automatizzata e Targeting automatico, consulta [Raccolta dati di Personalizzazione automatizzata](../../c-activities/t-automated-personalization/ap-data.md#reference_255BD3DE7AD04DC9B766E0BC78961058).

## Best practice {#section_DE96C7B7D114491DBB67FB5B7DA3D37B}

Nell&#39;elenco seguente sono riportate le procedure ottimali per caricare dati per gli algoritmi di personalizzazione di Target:

* Maggiore è la quantità di dati di alta qualità disponibili per gli algoritmi di personalizzazione di Target, migliore è la qualità dei modelli risultanti nelle attività personalizzazione automatizzata e di Auto Target.
* Limita l&#39;uso di più script di profilo o attributi che hanno lo stesso scopo.
* Non trasmettere un ID univoco, ad esempio un ID di sessione, se non necessario.
* Esamina i dati che Target raccoglie automaticamente ( [Raccolta di dati per gli algoritmi di personalizzazione di Target](../../c-activities/t-automated-personalization/ap-data.md#reference_255BD3DE7AD04DC9B766E0BC78961058)) così da non inviare informazioni duplicate. Ad esempio, Target utilizza indirizzi IP per determinare i codici postali dei visitatori. Non è necessario trasmettere queste informazioni come variabili separate.
* Non trasmettere più valori nello stesso attributo/variabile. Se più variabili sono concatenate, gli algoritmi di personalizzazione di Target considerano ogni stringa come valore univoco, riducendo il valore delle informazioni per la personalizzazione.
* Utilizza una convenzione di denominazione facile da ricordare e significativa per rendere i tuoi [rapporti Approfondimenti personalizzazione](../../c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767) più comprensibili.

