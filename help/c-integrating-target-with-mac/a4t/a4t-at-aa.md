---
keywords: a4T;A4T;Analytics come fonte di origine per i rapporti per Target
description: Posso usare A4T con le attività di Auto-Target e Auto-Allocate?
title: Supporto A4T per le attività di allocazione automatica e di targeting automatico
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: 4f0f1df1bcb6baad0e20c4dc1ae7e12751080d91
workflow-type: tm+mt
source-wordcount: '838'
ht-degree: 2%

---


# Supporto A4T per le attività di allocazione automatica e di targeting automatico

L&#39;integrazione [!DNL Adobe Target]-to-[!DNL Adobe Analytics], nota come [Analytics for Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T) supporta le attività [!UICONTROL Auto-Allocate] e [!UICONTROL Auto-Target].

L’integrazione A4T consente di:

* Utilizzate la funzionalità multi-armata di [Allocazione automatica](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) per indirizzare il traffico verso esperienze vincenti.
* Utilizzate l&#39;algoritmo di apprendimento per computer di [Auto-Target](/help/c-activities/auto-target/auto-target-to-optimize.md) di Auto-Target per scegliere l&#39;esperienza migliore per ogni visitatore in base al profilo, al comportamento e al contesto in cui si trovano, utilizzando tutte le funzionalità di reporting e analisi [!DNL Adobe Analytics] di [!DNL Adobe Analytics]&quot;.

Assicuratevi di aver [implementato A4T per l&#39;utilizzo con attività Test A/B e Targeting delle esperienze](/help/c-integrating-target-with-mac/a4t/a4timplementation.md). Se si utilizza `analyticsLogging = client_side`, è necessario anche passare il valore `sessionId` a [!DNL Analytics]. Per ulteriori informazioni, vedi [Analytics for Target (A4T) reporting](https://adobetarget-sdks.gitbook.io/docs/integration-with-experience-cloud/analytics-for-target-a4t-reporting) nella *Adobe Target SDKs* guida.

Per iniziare:

1. Durante la creazione di un&#39;attività di test A/B, nella pagina **[!UICONTROL Targeting]**, selezionare una delle seguenti opzioni come **[!UICONTROL Metodo di allocazione traffico]**:

   * [!UICONTROL Assegnazione automatica per esperienze ottimali]
   * [!UICONTROL Targeting automatico per esperienze personalizzate]

   ![Opzioni Metodi di allocazione traffico: Allocazione manuale, automatica e destinazione automatica](/help/c-integrating-target-with-mac/a4t/assets/traffic-allocation-methods.png)

   Per ulteriori informazioni e istruzioni dettagliate, vedere [Creazione di un&#39;attività di allocazione automatica](/help/c-activities/automated-traffic-allocation/create-auto-allocate-activity.md) e [Creazione di un&#39;attività di targeting automatico](/help/c-activities/auto-target/create-auto-target.md).

1. Selezionare **[!UICONTROL Adobe Analytics]** per **[!UICONTROL Origine report]** nella pagina **[!UICONTROL Goals &amp; Settings]** (Obiettivi e impostazioni) e selezionare la suite di rapporti corrispondente all&#39;obiettivo di ottimizzazione desiderato.

1. Scegliere una metrica Obiettivo principale.

   * Scegliere **[!UICONTROL Conversion]** per utilizzare [!DNL Adobe Target] per specificare l&#39;obiettivo di ottimizzazione.
   * Scegliete **[!UICONTROL Usa una metrica Analytics]**, quindi selezionate una metrica da [!DNL Analytics] da utilizzare come obiettivo di ottimizzazione. È possibile utilizzare una metrica di conversione [!DNL Analytics] out-of-box o un evento personalizzato [!DNL Analytics].

1. Salvate e attivate l&#39;attività.

   [!UICONTROL Auto-] Allocateutilizzerà la metrica selezionata per ottimizzare l&#39;attività, portando i visitatori all&#39;esperienza che massimizza la metrica dell&#39;obiettivo.

   Oppure

   [!UICONTROL Il ] targeting automatico utilizzerà la metrica selezionata per ottimizzare l&#39;attività, portando i visitatori a un&#39;esperienza personalizzata.

1. Utilizzate la scheda **[!UICONTROL Reports]** per visualizzare i report dell&#39;attività in base alle metriche [!DNL Adobe Analytics] selezionate. Fai clic su **[!UICONTROL Visualizza in Analytics]** per approfondire e segmentare ulteriormente i dati di reporting.

## Metriche obiettivo supportate

[!UICONTROL A4] Per l&#39; [!UICONTROL allocazione ] automatica e l&#39; [!UICONTROL Auto-] Targetlet potete scegliere uno dei seguenti tipi di metriche come metrica di obiettivo principale per l&#39;ottimizzazione:

* [!DNL Adobe Target] metriche di conversione
* [!DNL Adobe Analytics] metriche di conversione
* [!DNL Adobe Analytics] eventi personalizzati

[!UICONTROL A4] Per l&#39; [!UICONTROL allocazione ] automatica e la   targeting automatico, è necessario scegliere una metrica basata su un evento binomiale, ovvero un evento che si verifica o meno, ad esempio un clic, una conversione, un ordine e così via. Questi tipi di eventi sono anche a volte denominati eventi Bernoulli, binari o discreti.

[!UICONTROL A4] Tfor  [!UICONTROL Auto-] Allocateand  [!UICONTROL Auto-] Targetnon supporta l&#39;ottimizzazione per metriche continue come le entrate, il numero di prodotti ordinati, la durata della sessione, il numero di visualizzazioni di pagina nella sessione, ecc. Questi tipi di metriche non supportati sono anche a volte denominate metriche non binomiali o non Bernoulli.

I seguenti tipi di metriche non sono supportati come metriche dell&#39;obiettivo primario:

* [!DNL Adobe Target] metriche di coinvolgimento e ricavi
* [!DNL Adobe Analytics] metriche di coinvolgimento e ricavi

   Potrebbe essere possibile selezionare una metrica di coinvolgimento o ricavi [!DNL Analytics] come metrica di obiettivo principale, perché [!DNL Target] non è in grado di identificare ed escludere tutte le metriche di coinvolgimento e ricavi da [!DNL Analytics]. Prestate attenzione a selezionare solo metriche di conversione binomiali o eventi personalizzati da [!DNL Analytics].

* [!DNL Adobe Analytics] metriche calcolate

## Limitazioni e note

Alcune limitazioni e note si applicano alle attività [!UICONTROL Auto-Allocate] e [!UICONTROL Auto-Target]. Altre limitazioni e note si applicano a un tipo di attività o all&#39;altro.

### Allocazione automatica e targeting automatico

* L&#39;origine di reporting non può essere modificata da [!DNL Analytics] a [!DNL Target] o viceversa dopo che un&#39;attività è stata attivata.
* Sebbene le metriche calcolate non siano supportate come metriche dell&#39;obiettivo principale, spesso è possibile ottenere il risultato desiderato selezionando invece un evento personalizzato come metrica dell&#39;obiettivo principale. Ad esempio, se si desidera ottimizzare per una metrica come &quot;completamenti del modulo per visitatore&quot;, selezionare un evento personalizzato corrispondente a &quot;completamento del modulo&quot; come metrica obiettivo principale. [!DNL Target] normalizza automaticamente le metriche di conversione in base a ogni visita per tenere conto della distribuzione del traffico non uniforme, quindi non è necessario utilizzare una metrica calcolata per eseguire la normalizzazione.
* [!DNL Target] utilizza il modello di attribuzione &quot;Stesso tocco&quot; nella funzione di  [!UICONTROL allocazione ] automatica: Analytics per Target (A4T).

### Allocazione automatica

* [!UICONTROL Gli ] allocatemodels automatici continuano a allenarsi ogni due ore, come al solito.

### Targeting automatico

* [!UICONTROL I modelli Auto-] Targetmodelli continuano a essere formati ogni 24 ore, come al solito. Tuttavia, i dati evento di conversione provenienti da [!DNL Analytics] vengono posticipati di ulteriori 6-24 ore. Questo ritardo significa che la distribuzione del traffico per [!DNL Target] seguirà gli ultimi eventi registrati in [!DNL Analytics]. Questo ha l&#39;effetto maggiore nelle prime 48 ore dopo l&#39;attivazione iniziale di un&#39;attività. Le prestazioni dell&#39;attività rispecchieranno più da vicino il comportamento di conversione [!DNL Analytics] dopo cinque giorni. È consigliabile utilizzare [!UICONTROL Auto-Allocate] invece di [!UICONTROL Auto-Target] per le attività di breve durata in cui il traffico si verifica nella maggior parte dei primi cinque giorni di vita dell&#39;attività.
* Quando si utilizza [!DNL Analytics] come origine dati per un&#39;attività [!UICONTROL Auto-Target], le sessioni vengono considerate come terminate dopo sei ore. Le conversioni che si verificano dopo sei ore non saranno conteggiate.

Per ulteriori informazioni, vedere [Modelli di attribuzione e finestre di lookback](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html) nella *Guida agli strumenti di Analytics*.
