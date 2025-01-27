---
keyword: traffic estimate;traffic estimator;estimate;traffic;confidence;statistical power;lift;bonferroni;conversion rate;visitors per day;duration
description: Scopri come utilizzare il Calcolatore del traffico che ti consente di sapere se disponi di traffico sufficiente per il completamento dell'attività  [!DNL Adobe Target] [!UICONTROL Multivariate Test].
title: Quanto traffico è necessario per un'attività [!UICONTROL Multivariate Test] (MVT)?
feature: Multivariate Tests
hide: true
hidefromtoc: true
source-git-commit: 4805da617962e29794bd3af16138f3887ad250d0
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 21%

---

# Stimare il traffico necessario per un&#39;attività [!UICONTROL Multivariate Test] completata

Dato che in un test multivariato vengono messe a confronto più esperienze, è importante sapere quanto traffico è necessario per generare risultati significativi. [!UICONTROL Traffic Estimator] utilizza le statistiche sulla pagina e sul numero di esperienze testate per stimare la quantità di traffico e la durata del test necessari per il successo del test.

[!UICONTROL Traffic Estimator] prevede la dimensione del campione necessaria per garantire quanto segue:

* 95% di affidabilità. Questa statistica significa che la probabilità di segnalare un falso positivo in assenza di un incremento reale è del 5% (livello di affidabilità del 100%).
* 80% di potenza statistica. Questa statistica significa che il test ha una probabilità dell’80% di individuare un incremento reale pari o superiore al 25%.
* 25% minimo rilevabile con affidabilità. [!DNL Target] calcola la quantità di traffico necessaria per avere una probabilità dell&#39;80% di rilevare un incremento reale pari o superiore al 25%.

Il test utilizza la correzione di Bonferroni in caso di confronti multipli. Questo metodo è noto per essere di tipo conservativo, il che risulta controbilanciato dall&#39;imposizione di un incremento rilevabile con affidabilità minima relativamente ampio.

[!UICONTROL Traffic Estimator] fornisce anche un feedback che ti consente di sapere se disponi di traffico sufficiente per il test che hai progettato per avere successo.

1. Dalla pagina [!UICONTROL Experiences] di [!UICONTROL Visual Experience Composer] in un&#39;attività [!UICONTROL Multivariate], fare clic sull&#39;icona **[!UICONTROL Traffic]** ( ![icona Calcolatore traffico](/help/main/assets/icons/Gauge2.svg) ) nell&#39;angolo superiore sinistro della pagina [!UICONTROL Experiences].

   Verrà aperto [!UICONTROL Traffic Estimator].

   ![Interfaccia utente Calcolatore traffico](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/mvt-est.png)

   Fare di nuovo clic sull&#39;icona per nascondere [!UICONTROL Traffic Estimator].

   Nella parte superiore di [!UICONTROL Traffic Estimator], i valori immessi vengono calcolati e vengono visualizzati i risultati.

1. (Condizionale) Fornisci il tasso di conversione tipico, i visitatori stimati al giorno e la durata del test.

   * **[!UICONTROL Number of Content Combinations]**: calcolato automaticamente in base al numero di esperienze create come parte dell&#39;attività, dopo eventuali esclusioni.
   * **[!UICONTROL Typical Conversion Rate]**: il tasso di conversione è espresso in percentuale, in base alla stima o ai dati passati derivati dal sistema di analisi.
   * **[!UICONTROL Estimated Visitors Per Day]**: è il numero di visitatori che probabilmente visualizzeranno la pagina in base ai criteri di targeting. Può essere basato sui dati di analisi.
   * **[!UICONTROL Test Duration]**: il numero di giorni desiderati per l&#39;esecuzione dell&#39;attività.

   [!UICONTROL Traffic Estimator] utilizza queste statistiche per determinare le regolazioni necessarie per eseguire un test di successo.

   Modificando i valori, si modifica anche la stima. Ad esempio, se stai sottoponendo a test molte esperienze e il tasso di conversione e le impression sono troppo bassi, [!UICONTROL Traffic Estimator] mostra quanto deve durare l&#39;esecuzione del test per avere successo. In alternativa, se il tuo traffico è basso, [!UICONTROL Traffic Estimator] potrebbe suggerire un numero inferiore di esperienze in modo da poter eseguire il test per il numero di giorni desiderato.

   Se il traffico non è sufficiente, puoi eseguire una o entrambe le operazioni seguenti:

   * Ridurre il numero di combinazioni di offerte e il numero di posizioni.
   * Impostare la durata del test.

   Regola i numeri finché [!UICONTROL Traffic Estimator] non indica che hai traffico sufficiente, quindi progetta il test di conseguenza.
