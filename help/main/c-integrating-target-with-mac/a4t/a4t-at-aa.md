---
keywords: a4t;A4T;Analytics come origine per la generazione di rapporti per Target;Analytics for target
description: Scopri come creare [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico] attività in [!DNL Target] che usano [!DNL Analytics] come origine per la generazione di rapporti (A4T)
title: A4T supporta [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico] Attività?
feature: Analytics for Target (A4T)
exl-id: 3302f26d-c445-4779-8435-be142d5cea8c
source-git-commit: 99bd509988a7d1545a6a1fe59aa59f35ef0a7d11
workflow-type: tm+mt
source-wordcount: '1271'
ht-degree: 6%

---

# Supporto A4T per attività di [!UICONTROL allocazione automatica] e [!UICONTROL targeting automatico]

Il [!DNL Adobe Target]-a-[!DNL Adobe Analytics] integrazione, nota come [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T), supporta [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico] attività.

L’integrazione di A4T consente di:

* Utilizza il [Allocazione automatica](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) funzionalità slot machine per indirizzare il traffico verso esperienze vincenti.
* Utilizza il [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md) assembla l’algoritmo di apprendimento automatico per scegliere l’esperienza migliore per ogni visitatore. [!UICONTROL Targeting automatico] sceglie l’esperienza migliore in base al profilo, al comportamento e al contesto di ogni utente, il tutto mentre utilizza un’ [!DNL Adobe Analytics] metrica di obiettivo e funzionalità avanzate di reporting e analisi di [!DNL Adobe Analytics].

Assicurati di avere [A4T implementato per l’utilizzo con attività di test A/B e Targeting esperienza](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md). Se usa `analyticsLogging = client_side`, è inoltre necessario trasmettere `sessionId` valore per [!DNL Analytics]. Per ulteriori informazioni, consulta [Generazione di rapporti di Analytics for Target (A4T)](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/integration/a4t-reporting.html){target=_blank} nel *Guida per gli sviluppatori di Adobe Target*.

Per iniziare:

1. Mentre [creazione di un [!UICONTROL Test A/B] attività](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md), sulla **[!UICONTROL Targeting]** , selezionare una delle opzioni seguenti come **[!UICONTROL Metodo di allocazione traffico]**:

   * [!UICONTROL Allocazione automatica all’esperienza migliore]
   * [!UICONTROL Targeting automatico per esperienze personalizzate]

   ![Opzioni dei metodi di allocazione del traffico: manuale, allocazione automatica e targeting automatico](/help/main/c-integrating-target-with-mac/a4t/assets/traffic-allocation-methods.png)

   Per ulteriori informazioni e istruzioni dettagliate, consulta [Creare un’attività di allocazione automatica](/help/main/c-activities/automated-traffic-allocation/create-auto-allocate-activity.md) e [Creare un’attività](/help/main/c-activities/auto-target/create-auto-target.md).

1. Seleziona **[!UICONTROL Adobe Analytics]** per **[!UICONTROL Origine per la generazione di rapporti]** il **[!UICONTROL Obiettivi e impostazioni]** e seleziona la suite di rapporti corrispondente all’obiettivo di ottimizzazione desiderato.

   ![Sezione Origine per la generazione di rapporti sulla pagina Obiettivi e impostazioni](/help/main/c-integrating-target-with-mac/a4t/assets/a4t-select.png)

1. Scegli un [!UICONTROL Obiettivo principale] metrica.

   * Da utilizzare [!DNL Adobe Target] per specificare l’obiettivo di ottimizzazione, scegli **[!UICONTROL Conversione]** .
   * Scegli **[!UICONTROL Utilizzare una metrica di Analytics]** e quindi seleziona una metrica da [!DNL Analytics] da utilizzare come obiettivo di ottimizzazione. È possibile utilizzare una [!DNL Analytics] metrica di conversione o un [!DNL Analytics] evento personalizzato.

   Consulta [Metriche obiettivo supportate](#supported) per ulteriori informazioni.

1. Salva e attiva l’attività.

   [!UICONTROL Allocazione automatica] utilizza la metrica selezionata per ottimizzare l’attività, portando i visitatori all’esperienza che massimizza la metrica dell’obiettivo.

   Oppure

   [!UICONTROL Targeting automatico] utilizza la metrica selezionata per ottimizzare l’attività, portando i visitatori a una migliore esperienza personalizzata.

1. Utilizza il **[!UICONTROL Rapporti]** per visualizzare i rapporti dell’attività in base alla scelta di [!DNL Adobe Analytics] metriche. Clic **[!UICONTROL Visualizza in Analytics]** per approfondire e segmentare ulteriormente i dati di reporting.

## Metriche obiettivo supportate {#supported}

[!UICONTROL A4T] per [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico] consente di scegliere uno dei seguenti tipi di metrica come metrica di obiettivo principale per l’ottimizzazione:

* [!DNL Adobe Target] metriche di conversione
* [!DNL Adobe Analytics] metriche di conversione
* [!DNL Adobe Analytics] eventi personalizzati

[!DNL Target] consente di scegliere le metriche basate su eventi binomiali o le metriche basate su eventi continui quando si utilizza [!UICONTROL A4T] per attività di [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico].

* **Metriche basate su eventi binomiali**: un evento binomiale si verifica o meno. Gli eventi binomiali includono un clic, una conversione, un ordine e così via. Questi tipi di eventi sono talvolta indicati anche come eventi di Bernoulli, binari o discreti.

* **Metriche basate su eventi continui**. Le metriche continue includono ricavi, numero di prodotti ordinati, durata della sessione, numero di visualizzazioni di pagina nella sessione e così via. Questi tipi di eventi sono a volte indicati anche come metriche non binomiali o non di Bernoulli.

>[!IMPORTANT]
>
>A partire dal [!DNL Adobe Target Standard/Premium] versione 22.15.1 (8 e 9 marzo 2023), [!DNL Target] continua a supportare le attività esistenti con metriche non supportate (elencate nelle tabelle seguenti). Tuttavia, dopo il 9 settembre 2023 queste metriche non saranno più supportate nelle attività esistenti e tutte le attività che utilizzano metriche non supportate verranno interrotte per forzare la migrazione delle attività esistenti al nuovo comportamento.

### Impatto su [!UICONTROL Allocazione automatica] attività

| Nome della metrica | Non più supportato in: |
| --- | --- |
| [!UICONTROL averagepagedepth] | Tasso di conversione, massimizzare il valore della metrica |
| [!UICONTROL averagetimespentonsite] | Tasso di conversione, massimizzare il valore della metrica |
| [!UICONTROL rimbalzo] | Tasso di conversione, massimizzare il valore della metrica |
| [!UICONTROL mancati recapiti] | Tasso di conversione, massimizzare il valore della metrica |
| [!UICONTROL voci] | Tasso di conversione, massimizzare il valore della metrica |
| [!UICONTROL uscite] | Tasso di conversione, massimizzare il valore della metrica |
| [!UICONTROL visualizzazioni pagina] | Massimizzare il valore della metrica |
| [!UICONTROL ricaricamenti] | Massimizzare il valore della metrica |
| [!UICONTROL visitatori] | Tasso di conversione, massimizzare il valore della metrica |
| [!UICONTROL visite] | Massimizzare il valore della metrica |

### Impatto su [!UICONTROL Targeting automatico] attività

| Nome della metrica | Non più supportato in: |
| --- | --- |
| [!UICONTROL rimozioni cartone] | Massimizzare il valore della metrica |
| [!UICONTROL visualizzazioni pagina] | Massimizzare il valore della metrica |
| [!UICONTROL visitatori] | Tasso di conversione, massimizzare il valore della metrica |
| [!UICONTROL visite] | Massimizzare il valore della metrica |

## Limitazioni e note

Alcune limitazioni e note si applicano a entrambi [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico] attività. Altre limitazioni e note si applicano a un tipo di attività o all’altro.

### Allocazione automatica e targeting automatico {#both}

* Quando si utilizza [!DNL Adobe Analytics] come origine di reporting per [!UICONTROL Allocazione automatica] o [!UICONTROL Targeting automatico], è sempre necessario visualizzare i rapporti in [!DNL Analytics].
* Impossibile modificare l&#39;origine per la generazione di rapporti da [!DNL Analytics] a [!DNL Target] o viceversa, dopo l&#39;attivazione di un&#39;attività.
* Anche se le metriche calcolate non sono supportate come metriche obiettivo primarie, spesso è possibile ottenere il risultato desiderato selezionando invece un evento personalizzato come metrica obiettivo principale. Ad esempio, se desideri ottimizzare per una metrica come &quot;completamenti modulo per visitatore&quot;, seleziona un evento personalizzato corrispondente a &quot;completamenti modulo&quot; come metrica di obiettivo principale. [!DNL Target] normalizza automaticamente le metriche di conversione per visita in modo da tenere conto di una distribuzione del traffico irregolare; pertanto, non è necessario utilizzare una metrica calcolata per eseguire la normalizzazione.

### Allocazione automatica {#aa}

* **Frequenza del corso di formazione**: [!UICONTROL Allocazione automatica] I modelli continuano ad allenarsi ogni ora, come al solito.
* **Modelli di attribuzione**: [!DNL Target] utilizza [!DNL Adobe Analytics] modello di attribuzione predefinito per[!UICONTROL  Allocazione automatica] attività che utilizzano A4T.
* **Affidabilità**: formula di affidabilità utilizzata da [!UICONTROL Allocazione automatica] attività è diversa dalla formula visualizzata per impostazione predefinita nella [!DNL Adobe Analytics] [!UICONTROL A4T] pannello. [Come descritto qui](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md), [!UICONTROL Allocazione automatica] utilizza intervalli di attendibilità più prudenti rispetto a quelli regolari [!UICONTROL Test A/B] attività. Questi livelli di affidabilità conservativi compensano le valutazioni ripetute (peeks) ai dati. Di conseguenza, il rapporto predefinito in [!DNL Adobe Analytics] mostra intervalli di affidabilità più ravvicinati rispetto agli intervalli utilizzati dal [!UICONTROL Allocazione automatica] algoritmo. Tuttavia, puoi determinare quale esperienza è preferita dagli algoritmi in base all’esperienza con più visitatori univoci inviati.
* **Stato del vincitore**: attualmente, il [Badge &quot;Ancora nessun vincitore&quot; e &quot;Vincitore&quot;](/help/main/c-activities/automated-traffic-allocation/determine-winner.md) non sono disponibili in [!UICONTROL A4T] pannello in [!DNL Analysis Workspace]. Questi badge non sono disponibili neanche se lo stesso rapporto viene visualizzato in [!DNL Target]. Un badge vincitore &quot;stella&quot; mostrato in una [!DNL Target] rapporto per un [!UICONTROL Allocazione automatica] L’attività che utilizza A4T deve essere ignorata. Questo badge riflette i normali calcoli di affidabilità e non i calcoli utilizzati da [!UICONTROL Allocazione automatica].

### Targeting automatico {#at}

* [!UICONTROL Targeting automatico] I modelli continuano ad allenarsi ogni 24 ore, come al solito. Tuttavia, i dati dell’evento di conversione provenienti da [!DNL Analytics] subisce un ritardo di 6-24 ore. Questo ritardo comporta la distribuzione del traffico da parte di [!DNL Target] traccia gli ultimi eventi registrati in [!DNL Analytics]. Questo ritardo ha l’effetto maggiore nelle prime 48 ore dopo l’attivazione iniziale di un’attività. Le prestazioni dell’attività si riflettono più da vicino [!DNL Analytics] comportamento di conversione dopo cinque giorni.

   Valuta l’utilizzo di [!UICONTROL Allocazione automatica] invece di [!UICONTROL Targeting automatico] per attività di breve durata in cui la maggior parte del traffico si verifica entro i primi cinque giorni di vita dell’attività.

* Quando si utilizza [!DNL Analytics] come origine di dati per un [!UICONTROL Targeting automatico] attività, le sessioni terminano dopo sei ore. Le conversioni che si verificano dopo sei ore non vengono conteggiate.

Per ulteriori informazioni, consulta [Modelli di attribuzione e intervalli di lookback](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html) nel *Guida agli strumenti di Analytics*.

## Esercitazioni

Sebbene le funzionalità di analisi avanzate siano disponibili in [!DNL Adobe Analytics] [!UICONTROL Analysis Workspace], alcune modifiche al valore predefinito [!UICONTROL Analytics for Target] sono necessari per interpretare correttamente [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico] attività. Tali modifiche sono necessarie a causa delle differenze tra le attività di sperimentazione (manuale A/B e [!UICONTROL Allocazione automatica]) e attività di personalizzazione ([!UICONTROL Targeting automatico]).

### Configurazione dei rapporti A4T in [!DNL Analysis Workspace] per le attività di [!UICONTROL Allocazione automatica] 

Questo tutorial illustra le modifiche consigliate per l’analisi [!UICONTROL Allocazione automatica] attività in [!DNL Analysis Workspace].

Per ulteriori informazioni, consulta [Impostare rapporti A4T in Analysis Workspace per le attività di allocazione automatica](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-allocate-activities.html?lang=it){target=_blank} in *Tutorials Adobe Target*.

### Configurazione dei rapporti A4T in[!DNL Analysis Workspace]per le attività di [!UICONTROL Targeting automatico]

Questo tutorial illustra le modifiche consigliate per l’analisi [!UICONTROL Targeting automatico] attività in [!DNL Analysis Workspace].

Per ulteriori informazioni, consulta [Impostare rapporti A4T in Analysis Workspace per le attività di Targeting automatico](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html?lang=it){target=_blank} in *Tutorials Adobe Target*.


