---
keywords: Automated Personalization;ap;caricare dati;dati offline;algoritmo di personalizzazione;targeting automatico;targeting automatico;best practice
description: Scopri come caricare dati offline durante la creazione di modelli di personalizzazione nelle attività  [!DNL Adobe Target] [!UICONTROL Automated Personalization] (AP) e [!UICONTROL Targeting automatico].
title: Come posso caricare dati per gli algoritmi Personalization?
feature: Automated Personalization, Auto-Target
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
exl-id: c750e0e5-8ebd-49a2-9705-05f593aaf0b9
TQID: https://experienceleague.adobe.com/B1vwWrii4DfQzXftwcmgzbhBkDAZFo5mDRn3a7dULj0
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2: id: adee20bd-51f4-461d-b9db-d215f8756eebid: c93393a4-e558-47e1-992e-c91ed4d480ce
subfeature_v2: id: fff07a91-d479-45f4-ae95-9762e79b1b7c
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: d3cdead0-685a-4489-9250-4bb709942f66id: e0eb8757-182f-49f3-94a4-1587d16f5094id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 323
ht-degree: 12%

---

# Carica dati per gli algoritmi di personalizzazione [!DNL Target]

I dati offline, ad esempio le informazioni CRM o i punteggi di propensione di abbandono dei clienti, possono essere estremamente utili per la creazione di modelli di personalizzazione nelle attività [!DNL Adobe Target] [!UICONTROL Automated Personalization] (AP) e [!UICONTROL Targeting automatico].

Esistono diversi modi per immettere dati negli algoritmi di personalizzazione [!UICONTROL Automated Personalization] (AP) e [!UICONTROL Targeting automatico]. Oltre ai metodi in [Metodi per ottenere dati in Target](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html?lang=it){target=_blank}, [!DNL Experience Cloud] tipi di pubblico condivisi ([!UICONTROL Adobe Analytics], [!DNL Audience Manager]) e tipi di pubblico di reporting all&#39;interno delle attività sono utilizzati anche in [!DNL Target] algoritmi.

Per informazioni sui dati raccolti e utilizzati automaticamente dagli algoritmi di personalizzazione [!UICONTROL Automated Personalization] e [!UICONTROL Targeting automatico], vedi [Raccolta dati di Automated Personalization](/help/main/c-activities/t-automated-personalization/ap-data.md).

## Best practice {#section_DE96C7B7D114491DBB67FB5B7DA3D37B}

Nell&#39;elenco seguente vengono illustrate le best practice per il caricamento di dati per gli algoritmi di personalizzazione [!DNL Target]:

* Più dati di alta qualità sono disponibili per gli algoritmi di personalizzazione [!DNL Target], migliore è la qualità dei modelli risultanti nelle attività [!UICONTROL Automated Personalization] e [!UICONTROL Targeting automatico].
* Limita l&#39;uso di più script di profilo o attributi che hanno lo stesso scopo.
* Non trasmettere un ID univoco, ad esempio un ID sessione se non necessario.
* Esaminare i dati raccolti automaticamente da [!DNL Target] ( [Raccolta dati per gli algoritmi Personalization di Target](/help/main/c-activities/t-automated-personalization/ap-data.md)) in modo da non inviare informazioni duplicate. Ad esempio, [!DNL Target] utilizza indirizzi IP per determinare i codici postali dei visitatori. Non è necessario trasmettere queste informazioni come variabili separate.
* Non trasmettere più valori nello stesso attributo o variabile. Se vengono concatenate più variabili, gli algoritmi di personalizzazione [!DNL Target] considerano ogni stringa come un valore univoco, riducendo il valore delle informazioni per la personalizzazione.
* Utilizza una convenzione per i nomi facile da ricordare e significativa per rendere i tuoi [rapporti Personalization Insights](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767) più comprensibili.
