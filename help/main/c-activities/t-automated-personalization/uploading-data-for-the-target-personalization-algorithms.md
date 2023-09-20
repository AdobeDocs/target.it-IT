---
keywords: Automated Personalization;ap;caricare dati;dati offline;algoritmo di personalizzazione;targeting automatico;targeting automatico;best practice
description: Scopri come caricare dati offline durante la creazione di modelli di personalizzazione in [!DNL Adobe Target] [!UICONTROL Automated Personalization] (AP) [!UICONTROL Targeting automatico] attività.
title: Come posso caricare dati per gli algoritmi di personalizzazione?
feature: Automated Personalization, Auto-Target
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Vedi cosa è incluso in Target Premium."
exl-id: c750e0e5-8ebd-49a2-9705-05f593aaf0b9
source-git-commit: 3f64da1c9a1146e4d2d9389d6d5ce764764d2d9c
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 25%

---

# Carica dati per [!DNL Target] algoritmi di personalizzazione

I dati offline, come le informazioni CRM o i punteggi di propensione di abbandono dei clienti, possono essere incredibilmente utili quando si creano modelli di personalizzazione in [!DNL Adobe Target] [!UICONTROL Automated Personalization] (AP) [!UICONTROL Targeting automatico] attività.

Sono disponibili diversi modi per immettere dati in algoritmi di [!UICONTROL Personalizzazione automatizzata] (AP) e [!UICONTROL Targeting automatico. ] Oltre ai metodi descritti in [Metodi per immettere i dati in Target](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html){target=_blank}, [!DNL Experience Cloud] pubblici condivisi ([!UICONTROL Adobe Analytics], [!DNL Audience Manager]) e i tipi di pubblico per i rapporti all’interno delle attività sono utilizzati anche in [!DNL Target] algoritmi.

Per informazioni sui dati raccolti e utilizzati automaticamente dagli algoritmi di [!UICONTROL personalizzazione automatizzata] e [!UICONTROL targeting automatico], consulta [Raccolta dati di Personalizzazione automatizzata](/help/main/c-activities/t-automated-personalization/ap-data.md).

## Best practice {#section_DE96C7B7D114491DBB67FB5B7DA3D37B}

L’elenco seguente presenta le best practice per il caricamento di dati per [!DNL Target] algoritmi di personalizzazione:

* Maggiore è il numero di dati di alta qualità disponibili per [!DNL Target] algoritmi di personalizzazione, migliore è la qualità dei modelli risultanti nei [!UICONTROL Automated Personalization] e [!UICONTROL Targeting automatico] attività.
* Limita l&#39;uso di più script di profilo o attributi che hanno lo stesso scopo.
* Non trasmettere un ID univoco, ad esempio un ID sessione se non necessario.
* Esamina i dati [!DNL Target] raccoglie automaticamente ( [Raccolta di dati per gli algoritmi di personalizzazione di Target](/help/main/c-activities/t-automated-personalization/ap-data.md)) in modo da non inviare informazioni duplicate. Ad esempio: [!DNL Target] utilizza gli indirizzi IP per determinare i codici postali dei visitatori. Non è necessario trasmettere queste informazioni come variabili separate.
* Non trasmettere più valori nello stesso attributo o variabile. Se sono concatenate più variabili, [!DNL Target] gli algoritmi di personalizzazione considerano ogni stringa come un valore univoco, riducendo il valore delle informazioni per la personalizzazione.
* Utilizza una convenzione di denominazione facile da ricordare e significativa per rendere i tuoi [rapporti Approfondimenti personalizzazione](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767) più comprensibili.
