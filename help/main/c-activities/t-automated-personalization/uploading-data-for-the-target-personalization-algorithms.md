---
keywords: Automated Personalization;ap;caricare dati;dati offline;algoritmo di personalizzazione;targeting automatico;targeting automatico;best practice
description: Scopri come caricare dati offline, come le informazioni CRM, durante la creazione di modelli di personalizzazione in Adobe [!DNL Target] Attività di Automated Personalization (AP).
title: Come posso caricare dati per gli algoritmi di personalizzazione?
feature: Automated Personalization
exl-id: c750e0e5-8ebd-49a2-9705-05f593aaf0b9
source-git-commit: 7c15a0795e94b6c6317cb5b4018899be71f03a40
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 37%

---

# Carica dati per [!DNL Target] algoritmi di personalizzazione

I dati offline, come le informazioni CRM o i punteggi di propensione di abbandono dei clienti, possono essere incredibilmente utili quando si creano modelli di personalizzazione in [!DNL Adobe Target] [!UICONTROL Automated Personalization] attività (AP).

Sono disponibili diversi modi per immettere dati in algoritmi di [!UICONTROL Personalizzazione automatizzata] (AP) e [!UICONTROL Targeting automatico. ] Oltre ai metodi descritti in [Metodi per immettere i dati in Target](https://experienceleague.corp.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html){target=_blank}, Experience Cloud shared audiences (Adobe Analytics, Audience Management){target=_blank} e nei nostri algoritmi vengono utilizzati anche i tipi di pubblico di reporting all’interno delle attività.

Per informazioni sui dati raccolti e utilizzati automaticamente dagli algoritmi di Personalizzazione automatizzata e Targeting automatico, consulta [Raccolta dati di Personalizzazione automatizzata](/help/main/c-activities/t-automated-personalization/ap-data.md).

## Best practice {#section_DE96C7B7D114491DBB67FB5B7DA3D37B}

Nell&#39;elenco seguente sono riportate le procedure ottimali per caricare dati per gli algoritmi di personalizzazione di Target:

* Più dati di alta qualità sono disponibili per gli algoritmi di personalizzazione di Target, migliore sarà la qualità dei modelli risultanti nelle attività di AP e Targeting automatico.
* Limita l&#39;uso di più script di profilo o attributi che hanno lo stesso scopo.
* Non trasmettere un ID univoco, ad esempio un ID sessione se non necessario.
* Esamina i dati che Target raccoglie automaticamente ( [Raccolta di dati per gli algoritmi di personalizzazione di Target](/help/main/c-activities/t-automated-personalization/ap-data.md)) in modo da non inviare informazioni duplicate. Ad esempio, Target utilizza indirizzi IP per determinare i codici postali dei visitatori. Non è necessario trasmettere queste informazioni come variabili separate.
* Non trasmettere più valori nello stesso attributo/variabile. Se vengono concatenate più variabili, gli algoritmi di personalizzazione di Target considerano ogni stringa come un valore univoco, riducendo il valore delle informazioni per la personalizzazione.
* Utilizza una convenzione di denominazione facile da ricordare e significativa per rendere i tuoi [rapporti Approfondimenti personalizzazione](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767) più comprensibili.
