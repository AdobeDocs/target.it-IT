---
keywords: a4t;A4T;Analytics come origine per la generazione di rapporti per Target;Analytics for target
description: Scopri come creare [!UICONTROL Auto-Allocate] e [!UICONTROL Auto-Target] attività in [!DNL Target] che utilizzano [!DNL Analytics] come origine per la generazione di rapporti (A4T).
title: A4T supporta [!UICONTROL Auto-Allocate] e [!UICONTROL Auto-Target] attività?
feature: Analytics for Target (A4T)
exl-id: 3302f26d-c445-4779-8435-be142d5cea8c
source-git-commit: 99bd509988a7d1545a6a1fe59aa59f35ef0a7d11
workflow-type: tm+mt
source-wordcount: '1133'
ht-degree: 0%

---

# Supporto A4T per [!UICONTROL Auto-Allocate] e [!UICONTROL Auto-Target] attività

L&#39;integrazione da [!DNL Adobe Target] a [!DNL Adobe Analytics], nota come [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T), supporta [!UICONTROL Auto-Allocate] e [!UICONTROL Auto-Target] attività.

L’integrazione di A4T consente di:

* Utilizza la funzionalità multi-armed bandit di [Allocazione automatica](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) per indirizzare il traffico verso esperienze vincenti.
* Utilizza l&#39;algoritmo di machine learning [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md) per scegliere l&#39;esperienza migliore per ogni visitatore. [!UICONTROL Auto-Target] sceglie l&#39;esperienza migliore in base al profilo, al comportamento e al contesto di ogni utente, il tutto utilizzando una metrica di obiettivo [!DNL Adobe Analytics] e le funzionalità avanzate di reporting e analisi di [!DNL Adobe Analytics].

Assicurati di avere [implementato A4T per l&#39;utilizzo con attività di test A/B ed Experience Targeting](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md). Se si utilizza `analyticsLogging = client_side`, è necessario passare anche il valore `sessionId` a [!DNL Analytics]. Per ulteriori informazioni, consulta [Generazione rapporti di Analytics for Target (A4T)](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/integration/a4t-reporting.html){target=_blank} nella *Guida per gli sviluppatori di Adobe Target*.

Per iniziare:

1. Durante la [creazione di un&#39;attività [!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md), nella pagina **[!UICONTROL Targeting]** selezionare una delle opzioni seguenti come **[!UICONTROL Traffic Allocation Method]**:

   * [!UICONTROL Auto-Allocate to best experience]
   * [!UICONTROL Auto-Target for personalized experiences]

   ![Opzioni dei metodi di allocazione del traffico: Manuale, Allocazione automatica e Targeting automatico](/help/main/c-integrating-target-with-mac/a4t/assets/traffic-allocation-methods.png)

   Per ulteriori informazioni e istruzioni dettagliate, consulta [Creare un&#39;attività di allocazione automatica](/help/main/c-activities/automated-traffic-allocation/create-auto-allocate-activity.md) e [Creare un&#39;attività di targeting automatico](/help/main/c-activities/auto-target/create-auto-target.md).

1. Seleziona **[!UICONTROL Adobe Analytics]** per **[!UICONTROL Reporting Source]** nella pagina **[!UICONTROL Goals & Settings]** e seleziona la suite di rapporti corrispondente all&#39;obiettivo di ottimizzazione desiderato.

   ![Sezione di reporting su Source nella pagina Obiettivi e impostazioni](/help/main/c-integrating-target-with-mac/a4t/assets/a4t-select.png)

1. Scegliere una metrica [!UICONTROL Primary Goal].

   * Per utilizzare [!DNL Adobe Target] per specificare l&#39;obiettivo di ottimizzazione, scegliere **[!UICONTROL Conversion]**.
   * Scegliere **[!UICONTROL Use an Analytics metric]**, quindi selezionare una metrica da [!DNL Analytics] da utilizzare come obiettivo di ottimizzazione. È possibile utilizzare una metrica di conversione [!DNL Analytics] predefinita o un evento personalizzato [!DNL Analytics].

   Per ulteriori informazioni, vedi [Metriche obiettivo supportate](#supported) di seguito.

1. Salva e attiva l’attività.

   [!UICONTROL Auto-Allocate] utilizza la metrica selezionata per ottimizzare l&#39;attività, portando i visitatori all&#39;esperienza che massimizza la metrica obiettivo.

   Oppure

   [!UICONTROL Auto-Target] utilizza la metrica selezionata per ottimizzare l&#39;attività, indirizzando i visitatori a una migliore esperienza personalizzata.

1. Utilizza la scheda **[!UICONTROL Reports]** per visualizzare i rapporti dell&#39;attività in base alle metriche [!DNL Adobe Analytics] che hai scelto. Fai clic su **[!UICONTROL View in Analytics]** per approfondire e segmentare ulteriormente i dati di reporting.

## Metriche obiettivo supportate {#supported}

[!UICONTROL A4T] per [!UICONTROL Auto-Allocate] e [!UICONTROL Auto-Target] consente di scegliere uno qualsiasi dei seguenti tipi di metrica come metrica di obiettivo principale per l&#39;ottimizzazione:

* [!DNL Adobe Target] metriche di conversione
* [!DNL Adobe Analytics] metriche di conversione
* [!DNL Adobe Analytics] eventi personalizzati

[!DNL Target] consente di scegliere metriche basate su eventi binomiali o metriche basate su eventi continui quando si utilizza [!UICONTROL A4T] per le attività [!UICONTROL Auto-Allocate] e [!UICONTROL Auto-Target].

* **Metriche basate su eventi binomiali**: un evento binomiale si verifica o meno. Gli eventi binomiali includono un clic, una conversione, un ordine e così via. Questi tipi di eventi sono talvolta indicati anche come eventi di Bernoulli, binari o discreti.

* **Metriche basate su eventi continui**. Le metriche continue includono ricavi, numero di prodotti ordinati, durata della sessione, numero di visualizzazioni di pagina nella sessione e così via. Questi tipi di eventi sono a volte indicati anche come metriche non binomiali o non di Bernoulli.

>[!IMPORTANT]
>
>A partire dalla versione 22.15.1 di [!DNL Adobe Target Standard/Premium] (8 e 9 marzo 2023), [!DNL Target] continua a supportare le attività esistenti con le metriche non supportate (elencate nelle tabelle seguenti). Tuttavia, dopo il 9 settembre 2023 queste metriche non saranno più supportate nelle attività esistenti e tutte le attività che utilizzano metriche non supportate verranno interrotte per forzare la migrazione delle attività esistenti al nuovo comportamento.

### Impatto su [!UICONTROL Auto-Allocate] attività

| Nome della metrica | Non più supportato in: |
| --- | --- |
| [!UICONTROL averagepagedepth] | Tasso di conversione, massimizzare il valore della metrica |
| [!UICONTROL averagetimespentonsite] | Tasso di conversione, massimizzare il valore della metrica |
| [!UICONTROL bouncerate] | Tasso di conversione, massimizzare il valore della metrica |
| [!UICONTROL bounces] | Tasso di conversione, massimizzare il valore della metrica |
| [!UICONTROL entries] | Tasso di conversione, massimizzare il valore della metrica |
| [!UICONTROL exits] | Tasso di conversione, massimizzare il valore della metrica |
| [!UICONTROL pageviews] | Massimizzare il valore della metrica |
| [!UICONTROL reloads] | Massimizzare il valore della metrica |
| [!UICONTROL visitors] | Tasso di conversione, massimizzare il valore della metrica |
| [!UICONTROL visits] | Massimizzare il valore della metrica |

### Impatto su [!UICONTROL Auto-Target] attività

| Nome della metrica | Non più supportato in: |
| --- | --- |
| [!UICONTROL cartremovals] | Massimizzare il valore della metrica |
| [!UICONTROL pageviews] | Massimizzare il valore della metrica |
| [!UICONTROL visitors] | Tasso di conversione, massimizzare il valore della metrica |
| [!UICONTROL visits] | Massimizzare il valore della metrica |

## Limitazioni e note

Alcune limitazioni e note si applicano sia alle attività [!UICONTROL Auto-Allocate] che alle attività [!UICONTROL Auto-Target]. Altre limitazioni e note si applicano a un tipo di attività o all’altro.

### Allocazione automatica e targeting automatico {#both}

* Quando si utilizza [!DNL Adobe Analytics] come origine per la generazione di rapporti per [!UICONTROL Auto-Allocate] o [!UICONTROL Auto-Target], è sempre necessario visualizzare i rapporti in [!DNL Analytics].
* Impossibile cambiare l&#39;origine per la generazione di rapporti da [!DNL Analytics] a [!DNL Target] o viceversa dopo l&#39;attivazione di un&#39;attività.
* Anche se le metriche calcolate non sono supportate come metriche obiettivo primarie, spesso è possibile ottenere il risultato desiderato selezionando invece un evento personalizzato come metrica obiettivo principale. Ad esempio, se desideri ottimizzare per una metrica come &quot;completamenti modulo per visitatore&quot;, seleziona un evento personalizzato corrispondente a &quot;completamenti modulo&quot; come metrica di obiettivo principale. [!DNL Target] normalizza automaticamente le metriche di conversione in base alla visita per tenere conto della distribuzione irregolare del traffico, pertanto non è necessario utilizzare una metrica calcolata per eseguire la normalizzazione.

### Allocazione automatica {#aa}

* **Frequenza di formazione**: [!UICONTROL Auto-Allocate] modelli continuano ad allenarsi ogni ora, come al solito.
* **Modelli di attribuzione**: [!DNL Target] utilizza il modello di attribuzione predefinito [!DNL Adobe Analytics] per[!UICONTROL  Auto-Allocate] attività che utilizzano A4T.
* **Affidabilità**: la formula di affidabilità utilizzata dalle attività [!UICONTROL Auto-Allocate] è diversa dalla formula visualizzata per impostazione predefinita nel pannello [!DNL Adobe Analytics] [!UICONTROL A4T]. [Come descritto](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md), [!UICONTROL Auto-Allocate] utilizza intervalli di attendibilità più conservativi rispetto alle normali attività [!UICONTROL A/B Test]. Questi livelli di affidabilità conservativi compensano le valutazioni ripetute (peeks) ai dati. Di conseguenza, il report predefinito in [!DNL Adobe Analytics] mostra intervalli di attendibilità più limitati rispetto a quelli utilizzati dall&#39;algoritmo [!UICONTROL Auto-Allocate]. Tuttavia, puoi determinare quale esperienza è preferita dagli algoritmi in base all’esperienza con più visitatori univoci inviati.
* **Stato vincitore**: al momento i badge [&quot;Ancora nessun vincitore&quot; e &quot;Vincitore&quot;](/help/main/c-activities/automated-traffic-allocation/determine-winner.md) non sono disponibili nel pannello [!UICONTROL A4T] in [!DNL Analysis Workspace]. Questi badge non sono disponibili neanche se lo stesso report viene visualizzato in [!DNL Target]. Un badge vincitore &quot;star&quot; visualizzato in un report [!DNL Target] per un&#39;attività [!UICONTROL Auto-Allocate] tramite A4T deve essere ignorato. Questo badge riflette i normali calcoli di affidabilità e non i calcoli utilizzati da [!UICONTROL Auto-Allocate].

### Targeting automatico {#at}

* [!UICONTROL Auto-Target] modelli continuano ad addestrarsi ogni 24 ore, come al solito. Tuttavia, i dati dell&#39;evento di conversione provenienti da [!DNL Analytics] subiscono un ritardo di 6-24 ore. Questo ritardo indica che la distribuzione del traffico da parte di [!DNL Target] tiene traccia degli ultimi eventi registrati in [!DNL Analytics]. Questo ritardo ha l’effetto maggiore nelle prime 48 ore dopo l’attivazione iniziale di un’attività. Le prestazioni dell&#39;attività rispecchiano in modo più preciso il comportamento di conversione di [!DNL Analytics] dopo cinque giorni.

  Considera l&#39;utilizzo di [!UICONTROL Auto-Allocate] invece di [!UICONTROL Auto-Target] per attività di breve durata in cui la maggior parte del traffico si verifica entro i primi cinque giorni di vita dell&#39;attività.

* Quando si utilizza [!DNL Analytics] come origine dati per un&#39;attività [!UICONTROL Auto-Target], le sessioni terminano dopo sei ore. Le conversioni che si verificano dopo sei ore non vengono conteggiate.

Per ulteriori informazioni, consulta [Modelli di attribuzione e intervalli di lookback](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html) nella *Guida agli strumenti di Analytics*.

## Esercitazioni

Sebbene le funzionalità di analisi avanzate siano disponibili in [!DNL Adobe Analytics] [!UICONTROL Analysis Workspace], sono necessarie alcune modifiche al pannello predefinito [!UICONTROL Analytics for Target] per interpretare correttamente le attività [!UICONTROL Auto-Allocate] e [!UICONTROL Auto-Target]. Queste modifiche sono necessarie a causa delle differenze tra le attività di sperimentazione (manuale A/B e [!UICONTROL Auto-Allocate]) e le attività di personalizzazione ([!UICONTROL Auto-Target]).

### Configurazione dei rapporti A4T in [!DNL Analysis Workspace] per le attività [!UICONTROL Auto-Allocate]

Questo tutorial illustra le modifiche consigliate per l&#39;analisi delle attività di [!UICONTROL Auto-Allocate] in [!DNL Analysis Workspace].

Per ulteriori informazioni, consulta [Come impostare rapporti A4T in Analysis Workspace per attività di allocazione automatica](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-allocate-activities.html?lang=it){target=_blank} in *Tutorials Adobe Target*.

### Configurazione dei rapporti A4T in [!DNL Analysis Workspace] per le attività [!UICONTROL Auto-Target]

Questo tutorial illustra le modifiche consigliate per l&#39;analisi delle attività di [!UICONTROL Auto-Target] in [!DNL Analysis Workspace].

Per ulteriori informazioni, consulta [Come impostare rapporti A4T in Analysis Workspace per attività di Targeting automatico](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html?lang=it){target=_blank} in *Tutorials Adobe Target*.


