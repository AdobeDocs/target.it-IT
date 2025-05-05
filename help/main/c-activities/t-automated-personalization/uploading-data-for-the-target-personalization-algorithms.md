---
keywords: Automated Personalization;ap;caricare dati;dati offline;algoritmo di personalizzazione;targeting automatico;targeting automatico;best practice
description: Scopri come caricare dati offline durante la creazione di modelli di personalizzazione in  [!DNL Adobe Target] [!UICONTROL Automated Personalization] (AP) e [!UICONTROL Auto-Target] attività.
title: Come posso caricare dati per gli algoritmi Personalization?
feature: Automated Personalization, Auto-Target
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#premium newtab=true" tooltip="Vedi cosa è incluso in Target Premium."
exl-id: c750e0e5-8ebd-49a2-9705-05f593aaf0b9
source-git-commit: 3f64da1c9a1146e4d2d9389d6d5ce764764d2d9c
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 10%

---

# Carica dati per gli algoritmi di personalizzazione [!DNL Target]

I dati offline, ad esempio le informazioni CRM o i punteggi di propensione di abbandono dei clienti, possono essere estremamente utili per la creazione di modelli di personalizzazione nelle attività [!DNL Adobe Target] [!UICONTROL Automated Personalization] (AP) e [!UICONTROL Auto-Target].

Esistono diversi modi per immettere dati in algoritmi di personalizzazione [!UICONTROL Automated Personalization] (AP) e [!UICONTROL Auto-Target]. Oltre ai metodi in [Metodi per ottenere dati in Target](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html?lang=it){target=_blank}, [!DNL Experience Cloud] tipi di pubblico condivisi ([!UICONTROL Adobe Analytics], [!DNL Audience Manager]) e tipi di pubblico di reporting all&#39;interno delle attività sono utilizzati anche in [!DNL Target] algoritmi.

Per informazioni sui dati raccolti e utilizzati automaticamente dagli algoritmi di personalizzazione [!UICONTROL Automated Personalization] e [!UICONTROL Auto-Target], vedere [Raccolta dati di Automated Personalization](/help/main/c-activities/t-automated-personalization/ap-data.md).

## Best practice {#section_DE96C7B7D114491DBB67FB5B7DA3D37B}

Nell&#39;elenco seguente vengono illustrate le best practice per il caricamento di dati per gli algoritmi di personalizzazione [!DNL Target]:

* Maggiore è il numero di dati di alta qualità disponibili per gli algoritmi di personalizzazione [!DNL Target], migliore è la qualità dei modelli risultanti nelle attività [!UICONTROL Automated Personalization] e [!UICONTROL Auto-Target].
* Limita l&#39;uso di più script di profilo o attributi che hanno lo stesso scopo.
* Non trasmettere un ID univoco, ad esempio un ID sessione se non necessario.
* Esaminare i dati raccolti automaticamente da [!DNL Target] ( [Raccolta dati per gli algoritmi Personalization di Target](/help/main/c-activities/t-automated-personalization/ap-data.md)) in modo da non inviare informazioni duplicate. Ad esempio, [!DNL Target] utilizza indirizzi IP per determinare i codici postali dei visitatori. Non è necessario trasmettere queste informazioni come variabili separate.
* Non trasmettere più valori nello stesso attributo o variabile. Se vengono concatenate più variabili, gli algoritmi di personalizzazione [!DNL Target] considerano ogni stringa come un valore univoco, riducendo il valore delle informazioni per la personalizzazione.
* Utilizza una convenzione per i nomi facile da ricordare e significativa per rendere i tuoi [rapporti Personalization Insights](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767) più comprensibili.
