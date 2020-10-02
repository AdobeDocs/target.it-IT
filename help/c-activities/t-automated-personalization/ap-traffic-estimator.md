---
keywords: traffic estimator;automated personalization;ap
description: Mediante Traffic Estimator (Utilità di stima traffico) viene fornito un feedback che consente di sapere se il traffico è sufficiente per garantire il successo dell'attività Adobe Target .
title: Stimare il traffico necessario per il successo
feature: ap
topic: Standard
uuid: 9961ebaa-8761-431d-9605-852025ca580f
translation-type: tm+mt
source-git-commit: fec7708ddb17ec5565bd3c5f00f0490c03ec0140
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 24%

---


# ![PREMIUM](/help/assets/premium.png) Stimare il traffico necessario per il successo{#estimate-the-traffic-required-for-success}

The [!UICONTROL Traffic Estimator] provides feedback that lets you know whether you have sufficient traffic for your [!DNL Adobe Target] activity to succeed.

Because an [!UICONTROL Automated Personalization] activity uses multiple offer combinations, it is important to know how much traffic is required to provide meaningful results. The [!UICONTROL Traffic Estimator] uses statistics about your page and the number of experiences being tested to estimate the amount of traffic and the test duration needed to make the activity successful.

The [!UICONTROL Traffic Estimator] determines if there is enough traffic to generate personalized models, by comparing the estimated page impressions and typical conversion rate for the pages. Idealmente, per il successo di un&#39;attività, la corretta dimensione del campione garantisce che il contenuto personalizzato sia pronto entro il 50% della durata dell&#39;attività o in 14 giorni, a seconda del minore tra questi due valori. In questo modo, si ha un tempo sufficiente per ottenere contenuti personalizzati e stabilire quale distribuire.

Remember that [!DNL Target] randomly serves experiences until the personalization algorithms are built. The checkmark icon beside each offer shows when the model for that offer is ready and [!DNL Target] is able to begin delivering personalized content. Poiché l&#39;incremento è previsto solo una volta che i modelli sono pronti, l&#39;indicazione visiva consente di stabilire la giusta previsione. Use the [!UICONTROL Traffic Estimator] in the [!UICONTROL Visual Experience Composer] (VEC) to get a guideline of when the models will be ready.

## Utilizzo di Traffic Estimator (Utilità di stima traffico)

1. From the [!UICONTROL Visual Experience Composer], click **[!UICONTROL Traffic]**.

   ![Icona Traffico](/help/c-activities/t-automated-personalization/assets/icon-traffic.png)

   The [!UICONTROL Traffic Estimator] opens. Fai di nuovo clic su **[!UICONTROL Traffico]**[!UICONTROL  per nascondere il Calcolatore del traffico].

   ![](assets/ap_est.png)

1. Indica il tasso di conversione tipico (o il tasso di conversione previsto per questa attività), le impression di attività stimate al giorno e la durata del test.

   * **Numero di offerte**: Calcolato automaticamente in base al numero di esperienze create come parte dell&#39;attività dopo eventuali esclusioni.
   * **Tasso** di conversione tipico: Il tasso di conversione è espresso come percentuale, in base alla stima o ai dati passati del sistema di analisi.
   * **Visite stimate al giorno**: È il numero di visite giornaliere da parte dei visitatori in grado di visualizzare l&#39;attività, in base ai criteri di targeting. Può essere basato sui dati di analisi. Questo numero dovrebbe indicare le visite, non i visitatori univoci.
   * **Durata del test**: il numero di giorni desiderati per l’esecuzione dell’attività.

   The [!UICONTROL Traffic Estimato]r uses these statistics to determine what adjustments are needed to run a successful test.

   Near the top of the [!UICONTROL Traffic Estimator], the values you entered are calculated and the results are shown.

   ![](assets/ap_est_no.png)

   Modificando i valori, si modifica anche la stima. For example, if you are testing a large number of combinations and your conversion rate and impressions are too low, the [!UICONTROL Traffic Estimator] shows how long the test will need to run to be successful. Or, if your traffic is low, the [!UICONTROL Traffic Estimator] might suggest a lower number of offer combinations so you can run the test the desired number of days.

   Se non disponi di traffico sufficiente, puoi eseguire una o tutte le operazioni seguenti:

   * Consider using an [Auto-Target](/help/c-activities/auto-target-to-optimize.md) activity instead of [!UICONTROL Automated Personalization] to create experiences with several offer changes in one experience variation.
   * Reduce the number of offer combinations within your [!UICONTROL Automated Personalization] activity.
   * Aumenta la durata dell&#39;attività.

   Adjust the numbers until the [!UICONTROL Traffic Estimator] says you have sufficient traffic, then design your test accordingly.

   ![](assets/ap_est_yes.png)

   If the traffic is sufficient, the [!UICONTROL Traffic] icon shows a green check. Se è insufficiente, l&#39;icona mostra un&#39;etichetta di avviso di colore rosso.

## Domande frequenti su Traffic Estimator (Utilità di stima traffico)

Quando lavorate con [!UICONTROL Traffic Estimator (Utilità di stima]traffico), prendete in considerazione le seguenti domande frequenti:

### Perché [!DNL Target] non creare modelli personalizzati quando l&#39;attività AP ha abbastanza traffico?

In alcune circostanze, il traffico potrebbe essere sufficientemente ampio da consentire la creazione di un modello personalizzato, ma tale traffico potrebbe informare [!DNL Target] che non esiste alcuna differenza significativa tra il modello personalizzato e quello casuale. Anche se il modello è incorporato [!DNL Target] e testato, non verrà distribuito perché il modello non è significativamente migliore di quello casuale.

Un possibile motivo per cui il modello non è migliore del casuale potrebbe essere che le offerte non sono significativamente diverse tra loro. In questo caso, potete provare ad aumentare le differenze nelle offerte rendendole più visivamente diverse o modificando il contenuto stesso.
