---
description: Il Calcolatore del traffico fornisce un feedback che consente di sapere se disponi di traffico sufficiente affinché l’attività abbia successo.
title: Stimare il traffico necessario per il successo
feature: null
topic: Standard
uuid: 9961ebaa-8761-431d-9605-852025ca580f
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 100%

---


# ![PREMIUM](/help/assets/premium.png) Stimare il traffico necessario per il successo{#estimate-the-traffic-required-for-success}

Il Calcolatore del traffico fornisce un feedback che consente di sapere se disponi di traffico sufficiente affinché l’attività abbia successo.

Poiché un&#39;attività di personalizzazione automatizzata utilizza più combinazioni di offerte, è importante sapere quanto traffico è necessario per ottenere risultati significativi. Il Calcolatore del traffico utilizza le statistiche sulla pagina e il numero di esperienze sottoposte al test per stimare la quantità di traffico e la durata del test necessarie per la riuscita dell’attività.

Il Calcolatore del traffico determina se il traffico è sufficiente per generare modelli personalizzati, confrontando le impression di pagina stimate e il tasso di conversione tipico per le pagine. Idealmente, per il successo di un&#39;attività, la corretta dimensione del campione garantisce che il contenuto personalizzato sia pronto entro il 50% della durata dell&#39;attività o in 14 giorni, a seconda del minore tra questi due valori. In questo modo, si ha un tempo sufficiente per ottenere contenuti personalizzati e stabilire quale distribuire.

Ricorda che Target fornisce le esperienze in modo casuale, fino a quando non vengono stabiliti gli algoritmi di personalizzazione. L&#39;icona del segno di spunta accanto a ogni offerta mostra quando il modello per quell&#39;offerta è pronto e se Target è in grado di iniziare a fornire contenuti personalizzati. Poiché l&#39;incremento è previsto solo una volta che i modelli sono pronti, l&#39;indicazione visiva consente di stabilire la giusta previsione. Utilizza il Calcolatore del traffico di Compositore esperienza visivo per ottenere una stima di quando i modelli saranno pronti.

1. Nel Compositore esperienza, fai clic su **[!UICONTROL Traffico]**.

   ![Icona Traffico](/help/c-activities/t-automated-personalization/assets/icon-traffic.png)

   Viene visualizzato il Calcolatore del traffico. Fai di nuovo clic su **[!UICONTROL Traffico]** per nascondere il Calcolatore del traffico.

   ![](assets/ap_est.png)

1. Indica il tasso di conversione tipico (o il tasso di conversione previsto per questa attività), le impression di attività stimate al giorno e la durata del test.

   * Numero di combinazioni di contenuto: calcolato automaticamente in base al numero di esperienze create come parte dell&#39;attività, dopo eventuali esclusioni.
   * Tasso di conversione tipico: il tasso di conversione è espresso in percentuale, in base alla stima o ai dati passati derivati dal sistema di analisi.
   * Visite al giorno stimate: è il numero di visite al giorno effettuate dai visitatori che possono visualizzare l’attività, in base ai criteri di targeting. Può essere basato sui dati di analisi. Questo numero dovrebbe indicare le visite, non i visitatori univoci.
   * Durata del test: il numero di giorni desiderati per l’esecuzione dell’attività.

   Nel Calcolatore del traffico questi dati statistici vengono utilizzati per determinare quali aggiustamenti sono necessari per eseguire un test di successo.

   Nella parte superiore del Calcolatore del traffico, vengono calcolati i valori inseriti e visualizzati i risultati.

   ![](assets/ap_est_no.png)

   Modificando i valori, si modifica anche la stima. Ad esempio, se stai sottoponendo a test un numero elevato di combinazioni e il tasso di conversione e le impression sono troppo ridotti, il Calcolatore del traffico mostra quanto dovrà durare l&#39;esecuzione del test perché questo abbia successo. Oppure, se il traffico è limitato, nel Calcolatore del traffico potrebbe venire suggerito un numero inferiore di combinazioni di offerte, in modo che sia possibile eseguire il test per il numero desiderato di giorni.

   Se non disponi di traffico sufficiente, puoi eseguire una o tutte le operazioni seguenti:

   * Considera l&#39;utilizzo del targeting automatico invece della personalizzazione automatizzata per creare esperienze con diversi cambiamenti di offerta in una variante di esperienza.
   * Riduci il numero di combinazioni di offerta all&#39;interno dell&#39;attività di personalizzazione automatizzata.
   * Aumenta la durata dell&#39;attività.

   Adegua i valori finché il Calcolatore del traffico indica che il traffico è sufficiente, quindi progetta il test di conseguenza.

   ![](assets/ap_est_yes.png)

   Se il traffico è sufficiente, l&#39;icona Traffico mostra un segno di spunta verde. Se è insufficiente, l&#39;icona mostra un&#39;etichetta di avviso di colore rosso.
