---
keyword: traffic estimate;traffic estimator;estimate;traffic;confidence;statistical power;lift;bonferroni;conversion rate;visitors per day;duration
description: Scopri come utilizzare il Calcolatore del traffico che ti consente di sapere se disponi di traffico sufficiente per il completamento dell'attività  [!DNL Adobe Target] [!UICONTROL Multivariate Test].
title: Quanto traffico è necessario per un'attività [!UICONTROL Multivariate Test] (MVT)?
feature: Multivariate Tests
exl-id: 2b32f4a7-b9b4-40bf-a17b-88225bc88787
source-git-commit: 8f9c0ea65197fd639d463628e54db79db993c2da
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 53%

---

# Stimare il traffico necessario per un&#39;attività [!UICONTROL Multivariate Test] completata

Dato che in un test multivariato vengono messe a confronto più esperienze, è importante sapere quanto traffico è necessario per generare risultati significativi. Il Calcolatore di traffico utilizza le statistiche sulla pagina e il numero di esperienze sottoposte al test per stimare la quantità di traffico e la durata del test necessarie per la sua riuscita.

Mediante il Calcolatore del traffico viene prevista la dimensione del campione necessaria per garantire quanto segue:

* 95% di affidabilità. Questa statistica significa che la probabilità di segnalare un falso positivo in assenza di un incremento reale è del 5% (livello di affidabilità del 100%).
* 80% di potenza statistica. Questa statistica significa che il test ha una probabilità dell’80% di individuare un incremento reale pari o superiore al 25%.
* 25% minimo rilevabile con affidabilità. [!DNL Target] calcola la quantità di traffico necessaria per avere una probabilità dell&#39;80% di rilevare un incremento reale pari o superiore al 25%.

Il test utilizza la correzione di Bonferroni in caso di confronti multipli. Questo metodo è noto per essere di tipo conservativo, il che risulta controbilanciato dall&#39;imposizione di un incremento rilevabile con affidabilità minima relativamente ampio.

Il Calcolatore del traffico fornisce un feedback che consente di sapere se disponi di traffico sufficiente affinché il test progettato abbia successo.

1. Da [!UICONTROL Visual Experience Composer], fare clic sull&#39;icona **[!UICONTROL Traffic]**.

   Viene visualizzato il Calcolatore del traffico. È possibile fare nuovamente clic sull&#39;icona **[!UICONTROL Traffic]** per nascondere il Calcolatore del traffico.

   ![stima immagine vuota](assets/estimatorempty.png)

1. Indica il tasso di conversione tipico, i visitatori stimati al giorno e la durata del test.

   * **[!UICONTROL Number of Content Combinations]**: calcolato automaticamente in base al numero di esperienze create come parte dell&#39;attività, dopo eventuali esclusioni.
   * **[!UICONTROL Typical Conversion Rate]**: il tasso di conversione è espresso in percentuale, in base alla stima o ai dati passati derivati dal sistema di analisi.
   * **[!UICONTROL Estimated Visitors Per Day]**: è il numero di visitatori che probabilmente visualizzeranno la pagina in base ai criteri di targeting. Può essere basato sui dati di analisi.
   * **[!UICONTROL Test Duration]**: il numero di giorni desiderati per l&#39;esecuzione dell&#39;attività.

   Nel Calcolatore del traffico questi dati statistici vengono utilizzati per determinare quali aggiustamenti sono necessari per eseguire un test di successo.

   Nella parte superiore del Calcolatore del traffico, vengono calcolati i valori inseriti e visualizzati i risultati.

   ![stimatorinsufficienti](assets/estimatorinsufficient.png)

   Modificando i valori, si modifica anche la stima. Ad esempio, se stai sottoponendo a test molte esperienze e il tasso di conversione e le impression sono troppo bassi, il Calcolatore del traffico mostra quanto deve durare l’esecuzione del test per avere successo. Oppure, se il traffico è limitato, nel Calcolatore del traffico potrebbe venire suggerito un numero inferiore di esperienze, in modo che sia possibile eseguire il test per il numero desiderato di giorni.

   Se il traffico non è sufficiente, puoi eseguire una o entrambe le operazioni seguenti:

   * Ridurre il numero di combinazioni di offerte e il numero di posizioni.
   * Impostare la durata del test.

   Adegua i valori finché il Calcolatore del traffico indica che il traffico è sufficiente, quindi progetta il test di conseguenza.

   ![immagine estimatorok](assets/estimatorok.png)
