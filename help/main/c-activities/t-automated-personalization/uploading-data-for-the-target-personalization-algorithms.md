---
keywords: Automated Personalization;ap;caricare dati;dati offline;algoritmo di personalizzazione;targeting automatico;targeting automatico;best practice
description: Scopri come caricare dati offline, come le informazioni CRM, durante la creazione di modelli di personalizzazione in Adobe [!DNL Target] Attività Automated Personalization (AP).
title: Come posso caricare i dati per gli algoritmi di personalizzazione?
feature: Automated Personalization
exl-id: c750e0e5-8ebd-49a2-9705-05f593aaf0b9
source-git-commit: 719eb95049dad3bee5925dff794871cd65969f79
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 63%

---

# Carica dati per [!DNL Target] algoritmi di personalizzazione

I dati offline, come le informazioni CRM o i punteggi di propensione di abbandono dei clienti, possono essere incredibilmente preziosi quando si creano modelli di personalizzazione in [!DNL Adobe Target] [!UICONTROL Automated Personalization] (AP) attività.

Sono disponibili diversi modi per immettere dati in algoritmi di [!UICONTROL Personalizzazione automatizzata] (AP) e [!UICONTROL Targeting automatico. ] Oltre ai metodi di [Metodi per immettere i dati in Target](https://developer.adobe.com/target/before-implement/methods-to-get-data-into-target/methods-to-get-data-into-target/)Nei nostri algoritmi vengono utilizzati anche {target=_blank}, i tipi di pubblico condivisi di Experience Cloud (Adobe Analytics, Gestione dell&#39;audience){target=_blank} e i tipi di pubblico per la generazione di rapporti in-attività.

Per informazioni sui dati raccolti e utilizzati automaticamente dagli algoritmi di Personalizzazione automatizzata e Targeting automatico, consulta [Raccolta dati di Personalizzazione automatizzata](/help/main/c-activities/t-automated-personalization/ap-data.md).

## Best practice {#section_DE96C7B7D114491DBB67FB5B7DA3D37B}

Nell&#39;elenco seguente sono riportate le procedure ottimali per caricare dati per gli algoritmi di personalizzazione di Target:

* Maggiore è la quantità di dati di alta qualità disponibili per gli algoritmi di personalizzazione di Target, migliore è la qualità dei modelli risultanti nelle attività personalizzazione automatizzata e di Auto Target.
* Limita l&#39;uso di più script di profilo o attributi che hanno lo stesso scopo.
* Non trasmettere un ID univoco, ad esempio un ID di sessione, se non necessario.
* Esamina i dati che Target raccoglie automaticamente ( [Raccolta di dati per gli algoritmi di personalizzazione di Target](/help/main/c-activities/t-automated-personalization/ap-data.md)) così da non inviare informazioni duplicate. Ad esempio, Target utilizza indirizzi IP per determinare i codici postali dei visitatori. Non è necessario trasmettere queste informazioni come variabili separate.
* Non trasmettere più valori nello stesso attributo/variabile. Se più variabili sono concatenate, gli algoritmi di personalizzazione di Target considerano ogni stringa come valore univoco, riducendo il valore delle informazioni per la personalizzazione.
* Utilizza una convenzione di denominazione facile da ricordare e significativa per rendere i tuoi [rapporti Approfondimenti personalizzazione](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767) più comprensibili.
