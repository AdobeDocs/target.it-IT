---
keywords: a4T;A4T;Analytics come fonte di origine per i rapporti per Target
description: Scopri come creare attività di allocazione automatica e targeting automatico in Adobe [!DNL Target] che utilizzano Analytics come origine per la generazione di rapporti (A4T).
title: A4T supporta le attività di allocazione automatica e targeting automatico?
feature: Analytics for Target (A4T)
exl-id: 3302f26d-c445-4779-8435-be142d5cea8c
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '963'
ht-degree: 2%

---

# Supporto A4T per attività di allocazione automatica e targeting automatico

L&#39;integrazione [!DNL Adobe Target]-to-[!DNL Adobe Analytics], nota come [Analytics for Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T) supporta le attività [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico].

L’integrazione A4T consente di:

* Utilizza la funzionalità slot machine di [Allocazione automatica](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) per indirizzare il traffico verso esperienze vincenti.
* Utilizza l’algoritmo di apprendimento automatico di [Targeting automatico](/help/c-activities/auto-target/auto-target-to-optimize.md) per l’insieme di macchine per scegliere un’esperienza migliore per ogni visitatore. La funzione Targeting automatico sceglie la migliore esperienza in base ai profili, ai comportamenti e al contesto degli utenti, utilizzando al tempo stesso una metrica di obiettivo [!DNL Adobe Analytics] e [!DNL Adobe Analytics]’ funzioni avanzate di reporting e analisi.

Assicurati di aver [implementato A4T per l&#39;utilizzo con attività di test A/B e targeting delle esperienze](/help/c-integrating-target-with-mac/a4t/a4timplementation.md). Se utilizzi `analyticsLogging = client_side`, devi anche passare il valore `sessionId` a [!DNL Analytics]. Per ulteriori informazioni, consulta [Reporting di Analytics for Target (A4T)](https://adobetarget-sdks.gitbook.io/docs/integration-with-experience-cloud/analytics-for-target-a4t-reporting) nella guida *SDK di Adobe Target* .

Per iniziare:

1. Durante la creazione di un&#39;attività di test A/B, nella pagina **[!UICONTROL Targeting]**, seleziona una delle seguenti opzioni come **[!UICONTROL Metodo di allocazione del traffico]**:

   * [!UICONTROL Allocazione automatica all’esperienza migliore]
   * [!UICONTROL Targeting automatico per esperienze personalizzate]

   ![Opzioni dei metodi di allocazione del traffico: Manuale, Allocazione automatica e Targeting automatico](/help/c-integrating-target-with-mac/a4t/assets/traffic-allocation-methods.png)

   Per ulteriori informazioni e istruzioni dettagliate, consulta [Creare un’attività di allocazione automatica](/help/c-activities/automated-traffic-allocation/create-auto-allocate-activity.md) e [Creare un’attività di targeting automatico](/help/c-activities/auto-target/create-auto-target.md).

1. Seleziona **[!UICONTROL Adobe Analytics]** per la tua **[!UICONTROL Origine per i rapporti]** nella pagina **[!UICONTROL Obiettivi e impostazioni]** e seleziona la suite di rapporti corrispondente all&#39;obiettivo di ottimizzazione desiderato.

   ![Sezione Origine per i rapporti nella pagina Obiettivi e impostazioni](/help/c-integrating-target-with-mac/a4t/assets/a4t-select.png)

1. Scegli una metrica di obiettivo primario.

   * Per utilizzare [!DNL Adobe Target] per specificare l&#39;obiettivo di ottimizzazione, scegli **[!UICONTROL Conversione]** .
   * Scegli **[!UICONTROL Utilizza una metrica Analytics]**, quindi seleziona una metrica da [!DNL Analytics] per l&#39;utilizzo come obiettivo di ottimizzazione. Puoi utilizzare una metrica di conversione preconfigurata [!DNL Analytics] o un evento personalizzato [!DNL Analytics] .

   Per ulteriori informazioni, consulta [Metriche dell’obiettivo supportate](#supported) di seguito.

1. Salva e attiva l’attività.

   [!UICONTROL L’] allocazione automatica utilizza la metrica selezionata per ottimizzare l’attività, indirizzando i visitatori all’esperienza che massimizza la metrica dell’obiettivo.

   Oppure

   [!UICONTROL Il ] Targeting automatico utilizza la metrica selezionata per ottimizzare l’attività, indirizzando i visitatori a una migliore esperienza personalizzata.

1. Utilizza la scheda **[!UICONTROL Rapporti]** per visualizzare i rapporti dell&#39;attività in base alle metriche [!DNL Adobe Analytics] selezionate. Fai clic su **[!UICONTROL Visualizza in Analytics]** per acquisire dati di reporting in profondità e segmentarli ulteriormente.

## Metriche dell&#39;obiettivo supportate {#supported}

[!UICONTROL A4] Tfor  [!UICONTROL Auto-] Allocateand  [!UICONTROL Auto-] Targetlet è possibile scegliere uno dei seguenti tipi di metriche come metrica di obiettivo principale per l’ottimizzazione:

* [!DNL Adobe Target] metriche di conversione
* [!DNL Adobe Analytics] metriche di conversione
* [!DNL Adobe Analytics] eventi personalizzati

[!UICONTROL A4] Tfor  [!UICONTROL Auto-] Allocateand  [!UICONTROL Auto-] Targetrichiede di scegliere una metrica basata su un evento binomiale. Un evento binomiale si verifica o non si verifica. Gli eventi binari includono un clic, una conversione, un ordine e così via. Questi tipi di eventi sono anche talvolta denominati eventi Bernoulli, binari o discreti.

[!UICONTROL A4] Tfor  [!UICONTROL Auto-] Allocateand  [!UICONTROL Auto-] Targeting non supporta l’ottimizzazione per le metriche continue. Le metriche continue includono ricavi, numero di prodotti ordinati, durata della sessione, numero di visualizzazioni di pagina nella sessione e così via. Questi tipi di metriche non supportati vengono talvolta definiti anche metriche non binomiali o non Bernoulli.

I seguenti tipi di metriche non sono supportati come metriche dell’obiettivo primario:

* [!DNL Adobe Target] metriche di coinvolgimento e ricavi
* [!DNL Adobe Analytics] metriche di coinvolgimento e ricavi

   È possibile selezionare una metrica di coinvolgimento o ricavi [!DNL Analytics] come metrica di obiettivo principale, perché [!DNL Target] non può identificare ed escludere tutte le metriche di coinvolgimento e ricavi da [!DNL Analytics]. Seleziona solo metriche di conversione binomiali o eventi personalizzati da [!DNL Analytics].

* [!DNL Adobe Analytics] metriche calcolate

## Limitazioni e note

Alcune limitazioni e note si applicano sia alle attività [!UICONTROL Allocazione automatica] che [!UICONTROL Targeting automatico]. Altre limitazioni e note si applicano a un tipo di attività o all’altro.

### Allocazione automatica e Targeting automatico

* L’origine per la generazione di rapporti non può essere modificata da [!DNL Analytics] a [!DNL Target] o viceversa dopo l’attivazione di un’attività.
* Sebbene le metriche calcolate non siano supportate come metriche dell’obiettivo primario, spesso è possibile ottenere il risultato desiderato selezionando invece un evento personalizzato come metrica dell’obiettivo principale. Ad esempio, se desideri ottimizzare per una metrica come &quot;completamenti del modulo per visitatore&quot;, seleziona un evento personalizzato corrispondente a &quot;completamenti del modulo&quot; come metrica di obiettivo principale. [!DNL Target] normalizza automaticamente le metriche di conversione per visita per tenere conto della distribuzione del traffico irregolare, quindi non è necessario utilizzare una metrica calcolata per eseguire la normalizzazione.
* [!DNL Target] utilizza il modello di attribuzione &quot;Same Touch&quot; (Stesso contatto) nella funzione di allocazione  [!UICONTROL automatica ] : Analytics for Target (A4T).

### Allocazione automatica

* [!UICONTROL L&#39;] Allocatemodels continua a allenarsi ogni due ore, come al solito.

### Targeting automatico

* [!UICONTROL I modelli ] di Targeting automatico continuano a essere in formazione ogni 24 ore, come di consueto. Tuttavia, i dati dell’evento di conversione provenienti da [!DNL Analytics] vengono ritardati di ulteriori 6-24 ore. Questo ritardo significa che la distribuzione del traffico per [!DNL Target] tiene traccia degli ultimi eventi registrati in [!DNL Analytics]. Questo ritardo ha l&#39;effetto più grande nelle prime 48 ore dopo l&#39;attivazione iniziale di un&#39;attività. Le prestazioni dell’attività rispecchieranno più strettamente il comportamento di conversione [!DNL Analytics] dopo cinque giorni. Prendi in considerazione l’utilizzo di [!UICONTROL Allocazione automatica] invece di [!UICONTROL Targeting automatico] per attività di breve durata in cui la maggior parte del traffico si verifica entro i primi cinque giorni della durata dell’attività.
* Quando utilizzi [!DNL Analytics] come origine dati per un&#39;attività [!UICONTROL Targeting automatico], le sessioni terminano dopo sei ore. Le conversioni che si verificano dopo sei ore non sono conteggiate.

Per ulteriori informazioni, consulta [Modelli di attribuzione e finestre di lookback](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html) nella *Guida agli strumenti di Analytics*.

## Esercitazione: Come impostare rapporti A4T in Analysis Workspace per le attività di Targeting automatico {#tutorial}

Sebbene le funzionalità di analisi avanzate siano disponibili in [!DNL Adobe Analytics] [!UICONTROL Analysis Workspace], per interpretare correttamente le attività di Targeting automatico sono necessarie alcune modifiche al pannello predefinito [!UICONTROL Analytics for Target] . Queste modifiche sono necessarie a causa delle differenze tra le attività di sperimentazione (manuale A/B e [!UICONTROL Allocazione automatica]) e le attività di personalizzazione ([!UICONTROL Targeting automatico]).

Questa esercitazione illustra le modifiche consigliate per l&#39;analisi delle attività di [!UICONTROL Targeting automatico] in [!UICONTROL Workspace].

Per ulteriori informazioni, consulta [Come impostare rapporti A4T in Analysis Workspace per le attività di Targeting automatico](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html) in *Tutorials Adobe Target*.
