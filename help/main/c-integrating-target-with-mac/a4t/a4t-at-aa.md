---
keywords: a4t;A4T;Analytics come origine per la generazione di rapporti per Target;Analytics for target
description: Scopri come creare [!UICONTROL attività Allocazione automatica] e [!UICONTROL Targeting automatico] in [!DNL Target] che utilizzano [!DNL Analytics] come origine per la generazione di rapporti (A4T).
title: A4T supporta [!UICONTROL attività di allocazione automatica] e [!UICONTROL targeting automatico]?
feature: Analytics for Target (A4T)
exl-id: 3302f26d-c445-4779-8435-be142d5cea8c
TQID: https://experienceleague.adobe.com/VVbjMp7jYDyslZ8ubn8ntPufLK8nKGI9k3ZGh1DLWWs
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
  - id: f7c7de77-382f-4f48-8b36-61a170f06d3d
subfeature_v2:
  - id: df62f171-ac37-440f-8f0f-f41a72ebdd34
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 1509
ht-degree: 6%

---

# Supporto A4T per [!UICONTROL attività Allocazione automatica] e [!UICONTROL Targeting automatico]

L&#39;integrazione da [!DNL Adobe Target] a [!DNL Adobe Analytics], nota come [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T), supporta [!UICONTROL le attività Allocazione automatica] e [!UICONTROL Targeting automatico].

L’integrazione di A4T consente di:

* Utilizza la funzionalità multi-armed bandit di [Allocazione automatica](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) per indirizzare il traffico verso esperienze vincenti.
* Utilizza l&#39;algoritmo di machine learning [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md) per scegliere l&#39;esperienza migliore per ogni visitatore. [!UICONTROL Targeting automatico] sceglie l&#39;esperienza migliore in base al profilo, al comportamento e al contesto di ogni utente, il tutto utilizzando una metrica di obiettivo [!DNL Adobe Analytics] e le funzionalità avanzate di reporting e analisi di [!DNL Adobe Analytics].

Assicurati di avere [implementato A4T per l&#39;utilizzo con attività di test A/B ed Experience Targeting](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md). Se si utilizza `analyticsLogging = client_side`, è necessario passare anche il valore `sessionId` a [!DNL Analytics]. Per ulteriori informazioni, consulta [Generazione rapporti di Analytics for Target (A4T)](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/integration/a4t-reporting.html?lang=it){target=_blank} nella *Guida per gli sviluppatori di Adobe Target*.

Per iniziare:

1. Durante la [creazione di un&#39;attività [!UICONTROL Test A/B]](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md), nella pagina **[!UICONTROL Targeting]** fare clic sul controllo **[!UICONTROL Allocazione traffico]**, quindi scegliere il metodo di allocazione del traffico desiderato nel riquadro di destra.

   ![Impostazioni del metodo di allocazione traffico](/help/main/c-activities/assets/auto-target.png)

   Sono disponibili i seguenti metodi di allocazione del traffico:

   * **[!UICONTROL Manuale (impostazione predefinita)]**: specifica la percentuale di partecipanti che dovranno visualizzare ogni esperienza. Puoi suddividere le percentuali in modo uniforme tra tutte le esperienze, oppure specificare percentuali maggiori o minori per ogni esperienza. Il totale per tutte le esperienze deve essere uguale al 100%.

   * **[!UICONTROL Allocazione automatica all&#39;esperienza migliore]**: la maggior parte dei partecipanti all&#39;attività viene automaticamente indirizzata alle esperienze con prestazioni migliori. Alcuni visitatori sono assegnati a tutte le esperienze, per mantenere l’esplorazione delle esperienze e riconoscere eventuali cambiamenti nelle tendenze prestazionali. Per ulteriori informazioni, vedere [[!UICONTROL Cenni preliminari sull&#39;allocazione automatica]](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4).

   * **[!UICONTROL Targeting automatico per esperienze personalizzate]**: [!DNL Target] utilizza l&#39;apprendimento automatico avanzato per personalizzare i contenuti e favorire le conversioni identificando più esperienze ad alte prestazioni definite dall&#39;addetto al marketing e fornendo l&#39;esperienza più personalizzata ai visitatori in base ai loro profili cliente individuali e ai comportamenti passati di visitatori simili. Per ulteriori informazioni, consulta [Panoramica sul Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md).

   Per ulteriori informazioni e istruzioni dettagliate, consulta [Creare un&#39;attività di allocazione automatica](/help/main/c-activities/automated-traffic-allocation/create-auto-allocate-activity.md) e [Creare un&#39;attività di targeting automatico](/help/main/c-activities/auto-target/create-auto-target.md).

1. Seleziona **[!UICONTROL Adobe Analytics]** per il tuo **[!UICONTROL Source di reporting]** nella pagina **[!UICONTROL Obiettivi e impostazioni]**, seleziona la società e la suite di rapporti corrispondenti all&#39;obiettivo di ottimizzazione desiderato.

   ![Sezione di reporting su Source nella pagina Obiettivi e impostazioni](/help/main/c-integrating-target-with-mac/a4t/assets/a4t-select.png)

1. Specifica il server di tracciamento e la sandbox.

1. Scegli una metrica dell&#39;[!UICONTROL obiettivo principale].

   * Per utilizzare [!DNL Adobe Target] per specificare l&#39;obiettivo di ottimizzazione, scegliere **[!UICONTROL Conversione]**.
   * Scegliere **[!UICONTROL Utilizza una metrica di Analytics]**, quindi selezionare una metrica da [!DNL Analytics] da utilizzare come obiettivo di ottimizzazione. È possibile utilizzare una metrica di conversione [!DNL Analytics] predefinita o un evento personalizzato [!DNL Analytics].

   Per ulteriori informazioni, vedi [Metriche obiettivo supportate](#supported) di seguito.

1. Salva e attiva l’attività.

   [!UICONTROL L&#39;allocazione automatica] utilizza la metrica selezionata per ottimizzare l&#39;attività, spingendo i visitatori all&#39;esperienza che massimizza la metrica obiettivo.

   Oppure

   [!UICONTROL Targeting automatico] utilizza la metrica selezionata per ottimizzare l&#39;attività, portando i visitatori a una migliore esperienza personalizzata.

1. Utilizza la scheda **[!UICONTROL Rapporti]** per visualizzare i rapporti dell&#39;attività scegliendo [!DNL Adobe Analytics] metriche. Fai clic su **[!UICONTROL Visualizza in Analytics]** per approfondire e segmentare ulteriormente i dati di reporting.

## Metriche obiettivo supportate {#supported}

[!UICONTROL A4T] per [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico] ti consente di scegliere uno dei seguenti tipi di metrica come metrica di obiettivo principale per l&#39;ottimizzazione:

* [!DNL Adobe Target] metriche di conversione
* [!DNL Adobe Analytics] metriche di conversione
* [!DNL Adobe Analytics] eventi personalizzati

>[!NOTE]
>
>Dopo aver selezionato [!UICONTROL Utilizza una metrica di Analytics], seleziona [!UICONTROL Massimizza tasso di conversione visitatore univoco] per visualizzare le metriche di conversione [!DNL Adobe Analytics] disponibili e [!UICONTROL Massimizza valore metrica per visitatore] per esplorare [!DNL Adobe Analytics] eventi personalizzati.

[!DNL Target] consente di scegliere metriche basate su eventi binomiali o metriche basate su eventi continui quando si utilizzano [!UICONTROL A4T] per attività [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico].

* **Metriche basate su eventi binomiali**: un evento binomiale si verifica o meno. Gli eventi binomiali includono un clic, una conversione, un ordine e così via. Questi tipi di eventi sono talvolta indicati anche come eventi di Bernoulli, binari o discreti.

* **Metriche basate su eventi continui**. Le metriche continue includono ricavi, numero di prodotti ordinati, durata della sessione, numero di visualizzazioni di pagina nella sessione e così via. Questi tipi di eventi sono a volte indicati anche come metriche non binomiali o non di Bernoulli.

>[!IMPORTANT]
>
>A partire dalla versione 22.15.1 di [!DNL Adobe Target Standard/Premium] (8 e 9 marzo 2023), [!DNL Target] continua a supportare le attività esistenti con le metriche non supportate (elencate nelle tabelle seguenti). Tuttavia, dopo il 9 settembre 2023 queste metriche non saranno più supportate nelle attività esistenti e tutte le attività che utilizzano metriche non supportate verranno interrotte per forzare la migrazione delle attività esistenti al nuovo comportamento.

### Impatto sulle [!UICONTROL attività Allocazione automatica]

| Nome metrica | Non più supportato in: |
| --- | --- |
| [!UICONTROL averagepagedepth] | Tasso di conversione, massimizzare il valore della metrica |
| [!UICONTROL averagetimespentonsite] | Tasso di conversione, massimizzare il valore della metrica |
| [!UICONTROL rimbalzo] | Tasso di conversione, massimizzare il valore della metrica |
| [!UICONTROL mancati recapiti] | Tasso di conversione, massimizzare il valore della metrica |
| [!UICONTROL voci] | Tasso di conversione, massimizzare il valore della metrica |
| [!UICONTROL uscite] | Tasso di conversione, massimizzare il valore della metrica |
| [!UICONTROL visualizzazioni pagina] | Massimizzare il valore della metrica |
| [!UICONTROL ricarica] | Massimizzare il valore della metrica |
| [!UICONTROL visitatori] | Tasso di conversione, massimizzare il valore della metrica |
| [!UICONTROL visite] | Massimizzare il valore della metrica |

### Impatto sulle [!UICONTROL attività Targeting automatico]

| Nome metrica | Non più supportato in: |
| --- | --- |
| [!UICONTROL cartremovals] | Massimizzare il valore della metrica |
| [!UICONTROL visualizzazioni pagina] | Massimizzare il valore della metrica |
| [!UICONTROL visitatori] | Tasso di conversione, massimizzare il valore della metrica |
| [!UICONTROL visite] | Massimizzare il valore della metrica |

## Limitazioni e note

Alcune limitazioni e note si applicano sia alle attività [!UICONTROL Allocazione automatica] che alle attività [!UICONTROL Targeting automatico]. Altre limitazioni e note si applicano a un tipo di attività o all’altro.

### Allocazione automatica e targeting automatico {#both}

* Quando si utilizza [!DNL Adobe Analytics] come origine per la generazione di rapporti per [!UICONTROL Allocazione automatica] o [!UICONTROL Targeting automatico], è sempre necessario visualizzare i rapporti in [!DNL Analytics].
* Impossibile cambiare l&#39;origine per la generazione di rapporti da [!DNL Analytics] a [!DNL Target] o viceversa dopo l&#39;attivazione di un&#39;attività.
* Anche se le metriche calcolate non sono supportate come metriche obiettivo primarie, spesso è possibile ottenere il risultato desiderato selezionando invece un evento personalizzato come metrica obiettivo principale. Ad esempio, se desideri ottimizzare per una metrica come &quot;completamenti modulo per visitatore&quot;, seleziona un evento personalizzato corrispondente a &quot;completamenti modulo&quot; come metrica di obiettivo principale. [!DNL Target] normalizza automaticamente le metriche di conversione in base alla visita per tenere conto della distribuzione irregolare del traffico, pertanto non è necessario utilizzare una metrica calcolata per eseguire la normalizzazione.

### Allocazione automatica {#aa}

* **Frequenza di formazione**: [!UICONTROL I modelli di allocazione automatica] continuano ad addestrarsi ogni ora, come di consueto.
* **Modelli di attribuzione**: [!DNL Target] utilizza il modello di attribuzione predefinito [!DNL Adobe Analytics] per [!UICONTROL &#x200B; attività di allocazione automatica] che utilizzano A4T.
* **Affidabilità**: la formula di affidabilità utilizzata dalle attività [!UICONTROL Allocazione automatica] è diversa dalla formula visualizzata per impostazione predefinita nel pannello [!DNL Adobe Analytics] [!UICONTROL A4T]. [Come descritto](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md), [!UICONTROL L&#39;allocazione automatica] utilizza intervalli di attendibilità più prudenti rispetto alle normali attività di [!UICONTROL Test A/B]. Questi livelli di affidabilità conservativi compensano le valutazioni ripetute (peeks) ai dati. Di conseguenza, il report predefinito in [!DNL Adobe Analytics] mostra intervalli di attendibilità più ridotti rispetto a quelli utilizzati dall&#39;algoritmo [!UICONTROL Allocazione automatica]. Tuttavia, puoi determinare quale esperienza è preferita dagli algoritmi in base all’esperienza con più visitatori univoci inviati.
* **Stato vincitore**: al momento i badge [&quot;Ancora nessun vincitore&quot; e &quot;Vincitore&quot;](/help/main/c-activities/automated-traffic-allocation/determine-winner.md) non sono disponibili nel pannello [!UICONTROL A4T] in [!DNL Analysis Workspace]. Questi badge non sono disponibili neanche se lo stesso report viene visualizzato in [!DNL Target]. Un badge vincitore &quot;star&quot; visualizzato in un report [!DNL Target] per un&#39;attività [!UICONTROL Allocazione automatica] tramite A4T deve essere ignorato. Questo badge riflette i normali calcoli di affidabilità e non i calcoli utilizzati da [!UICONTROL Allocazione automatica].

### Targeting automatico {#at}

* I modelli di [!UICONTROL Targeting automatico] continuano ad addestrarsi ogni 24 ore, come al solito. Tuttavia, i dati dell&#39;evento di conversione provenienti da [!DNL Analytics] subiscono un ritardo di 6-24 ore. Questo ritardo indica che la distribuzione del traffico da parte di [!DNL Target] tiene traccia degli ultimi eventi registrati in [!DNL Analytics]. Questo ritardo ha l’effetto maggiore nelle prime 48 ore dopo l’attivazione iniziale di un’attività. Le prestazioni dell&#39;attività rispecchiano in modo più preciso il comportamento di conversione di [!DNL Analytics] dopo cinque giorni.

  Valuta di utilizzare [!UICONTROL Allocazione automatica] invece di [!UICONTROL Targeting automatico] per attività di breve durata in cui la maggior parte del traffico si verifica entro i primi cinque giorni di vita dell&#39;attività.

* Quando si utilizza [!DNL Analytics] come origine dati per un&#39;attività di [!UICONTROL Targeting automatico], le sessioni terminano dopo sei ore. Le conversioni che si verificano dopo sei ore non vengono conteggiate.

Per ulteriori informazioni, consulta [Modelli di attribuzione e intervalli di lookback](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html?lang=it) nella *Guida agli strumenti di Analytics*.

## Esercitazioni

Sebbene le funzionalità di analisi avanzate siano disponibili in [!DNL Adobe Analytics] [!UICONTROL Analysis Workspace], sono necessarie alcune modifiche al pannello predefinito [!UICONTROL Analytics for Target] per interpretare correttamente le attività [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico]. Queste modifiche sono necessarie a causa delle differenze tra le attività di sperimentazione (A/B manuale e [!UICONTROL Allocazione automatica]) e le attività di personalizzazione ([!UICONTROL Targeting automatico]).

### Configurazione dei rapporti A4T in [!DNL Analysis Workspace] per le attività [!UICONTROL Allocazione automatica]

Questo tutorial illustra le modifiche consigliate per l&#39;analisi delle attività di [!UICONTROL Allocazione automatica] in [!DNL Analysis Workspace].

Per ulteriori informazioni, consulta [Come impostare rapporti A4T in Analysis Workspace per attività di allocazione automatica](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-allocate-activities.html?lang=it){target=_blank} nelle *esercitazioni di Adobe Target*.

### Configurazione dei rapporti A4T in [!DNL Analysis Workspace] per le attività [!UICONTROL Targeting automatico]

Questo tutorial illustra le modifiche consigliate per l&#39;analisi delle attività di [!UICONTROL Targeting automatico] in [!DNL Analysis Workspace].

Per ulteriori informazioni, consulta [Come impostare rapporti A4T in Analysis Workspace per attività di Targeting automatico](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html?lang=it){target=_blank} nelle *esercitazioni di Adobe Target*.


