---
keywords: a4T;A4T;Analytics come fonte di origine per i rapporti per Target
description: Scopri come creare [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico] attività [!DNL Target] che utilizzano [!DNL Analytics] come origine per la generazione di rapporti (A4T).
title: È supportato da A4T [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico] Attività?
feature: Analytics for Target (A4T)
exl-id: 3302f26d-c445-4779-8435-be142d5cea8c
source-git-commit: 1c9728b447ee1402cc133d38845a25da3038d0ca
workflow-type: tm+mt
source-wordcount: '1265'
ht-degree: 7%

---

# Supporto A4T per [!UICONTROL attività di allocazione] automatica e [!UICONTROL targeting automatico]

La [!DNL Adobe Target]-to-[!DNL Adobe Analytics] integrazione, nota come [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) supporta [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico] attività.

L’integrazione A4T consente di:

* Utilizzo [Allocazione automatica](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)Capacità di slot machine per indirizzare il traffico verso esperienze vincenti.
* Utilizzo [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md)L&#39;algoritmo di apprendimento automatico del gruppo di scegliere una migliore esperienza per ogni visitatore. [!UICONTROL Targeting automatico] sceglie l’esperienza migliore in base ai profili, ai comportamenti e al contesto degli utenti durante l’utilizzo di un’ [!DNL Adobe Analytics] metrica di obiettivo e [!DNL Adobe Analytics]Funzionalità avanzate di reporting e analisi.

Assicurati di [implementato A4T per l’utilizzo con attività di test A/B e targeting delle esperienze](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md). Se utilizzi `analyticsLogging = client_side`, è inoltre necessario trasmettere `sessionId` valore a [!DNL Analytics]. Per ulteriori informazioni, consulta [Reporting di Analytics for Target (A4T)](https://developer.adobe.com/target/implement/server-side/sdk-guides/integration-with-experience-cloud/a4t-reporting/){target=_blank} in *SDK per Adobe Target* guida.

Per iniziare:

1. Durante la creazione di un’ [!UICONTROL Test A/B] sull&#39;attività **[!UICONTROL Targeting]** seleziona una delle seguenti opzioni come **[!UICONTROL Metodo di allocazione traffico]**:

   * [!UICONTROL Allocazione automatica all’esperienza migliore]
   * [!UICONTROL Targeting automatico per esperienze personalizzate]

   ![Opzioni dei metodi di allocazione del traffico: Manuale, Allocazione automatica e Targeting automatico](/help/main/c-integrating-target-with-mac/a4t/assets/traffic-allocation-methods.png)

   Per ulteriori informazioni e istruzioni dettagliate, consulta [Creare un’attività di allocazione automatica](/help/main/c-activities/automated-traffic-allocation/create-auto-allocate-activity.md) e [Creare un’attività di Targeting automatico](/help/main/c-activities/auto-target/create-auto-target.md).

1. Seleziona **[!UICONTROL Adobe Analytics]** per **[!UICONTROL Origine per i rapporti]** sulla **[!UICONTROL Obiettivi e impostazioni]** e seleziona la suite di rapporti corrispondente all’obiettivo di ottimizzazione desiderato.

   ![Sezione Origine per i rapporti nella pagina Obiettivi e impostazioni](/help/main/c-integrating-target-with-mac/a4t/assets/a4t-select.png)

1. Scegli un [!UICONTROL Obiettivo principale] metrica.

   * Per utilizzare [!DNL Adobe Target] per specificare l&#39;obiettivo di ottimizzazione, scegli **[!UICONTROL Conversione]** .
   * Scegli **[!UICONTROL Utilizzare una metrica di Analytics]** quindi seleziona una metrica da [!DNL Analytics] da utilizzare come obiettivo di ottimizzazione. Puoi utilizzare un [!DNL Analytics] metrica di conversione o [!DNL Analytics] evento personalizzato.

   Vedi [Metriche dell’obiettivo supportate](#supported) qui sotto per ulteriori informazioni.

1. Salva e attiva l’attività.

   [!UICONTROL Allocazione automatica] utilizza la metrica selezionata per ottimizzare l’attività, indirizzando i visitatori all’esperienza che massimizza la metrica di obiettivo.

   Oppure

   [!UICONTROL Targeting automatico] utilizza la metrica selezionata per ottimizzare l’attività, indirizzando i visitatori a una migliore esperienza personalizzata.

1. Utilizza la **[!UICONTROL Rapporti]** per visualizzare i rapporti dell’attività in base alla scelta di [!DNL Adobe Analytics] metriche. Fai clic su **[!UICONTROL Visualizzazione in Analytics]** per acquisire e segmentare ulteriormente i dati di reporting.

## Metriche dell’obiettivo supportate {#supported}

[!UICONTROL A4T] per [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico] consente di scegliere uno dei seguenti tipi di metriche come metrica di obiettivo principale per l’ottimizzazione:

* [!DNL Adobe Target] metriche di conversione
* [!DNL Adobe Analytics] metriche di conversione
* [!DNL Adobe Analytics] eventi personalizzati

[!DNL Target] consente di scegliere le metriche basate su eventi binomiali o le metriche basate su eventi continui quando si utilizza [!UICONTROL A4T] per attività di [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico].

* **Metriche basate su eventi binomiali**: Un evento binomiale si verifica o non si verifica. Gli eventi binari includono un clic, una conversione, un ordine e così via. Questi tipi di eventi sono anche talvolta denominati eventi Bernoulli, binari o discreti.

* **Metriche basate su eventi continui**. Le metriche continue includono ricavi, numero di prodotti ordinati, durata della sessione, numero di visualizzazioni di pagina nella sessione e così via. Questi tipi di eventi vengono talvolta definiti anche metriche non binomiali o non Bernoulli.

>[!IMPORTANT]
>
>A partire dal [!DNL Adobe Target Standard/Premium] versione 22.15.1 (8 e 9 marzo 2023), [!DNL Target] continua a supportare le attività esistenti con le metriche non supportate (elencate nelle tabelle seguenti). Tuttavia, dopo il 9 settembre 2023, queste metriche non saranno più supportate nelle attività esistenti e tutte le attività che utilizzano metriche non supportate verranno interrotte per forzare la migrazione delle attività esistenti al nuovo comportamento.

### Impatto su [!UICONTROL Allocazione automatica] attività

| Nome della metrica | Non più supportato in: |
| --- | --- |
| [!UICONTROL media agepagedepth] | Tasso di conversione, Massimizza valore della metrica |
| [!UICONTROL averagetimespentonsite] | Tasso di conversione, Massimizza valore della metrica |
| [!UICONTROL rimbalzare] | Tasso di conversione, Massimizza valore della metrica |
| [!UICONTROL rimbalzo] | Tasso di conversione, Massimizza valore della metrica |
| [!UICONTROL voci] | Tasso di conversione, Massimizza valore della metrica |
| [!UICONTROL uscite] | Tasso di conversione, Massimizza valore della metrica |
| [!UICONTROL pageviews] | Massimizza valore della metrica |
| [!UICONTROL ricarica] | Massimizza valore della metrica |
| [!UICONTROL visitatori] | Tasso di conversione, Massimizza valore della metrica |
| [!UICONTROL visite] | Massimizza valore della metrica |

### Impatto su [!UICONTROL Targeting automatico] attività

| Nome della metrica | Non più supportato in: |
| --- | --- |
| [!UICONTROL spedizioni] | Massimizza valore della metrica |
| [!UICONTROL pageviews] | Massimizza valore della metrica |
| [!UICONTROL visitatori] | Tasso di conversione, Massimizza valore della metrica |
| [!UICONTROL visite] | Massimizza valore della metrica |

## Limitazioni e note

Alcune limitazioni e note si applicano a entrambi [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico] attività. Altre limitazioni e note si applicano a un tipo di attività o all’altro.

### Allocazione automatica e targeting automatico {#both}

* Quando utilizzi [!DNL Adobe Analytics] come origine per la generazione di rapporti per [!UICONTROL Allocazione automatica] o [!UICONTROL Targeting automatico], dovresti sempre visualizzare i rapporti in [!DNL Analytics].
* Impossibile modificare l&#39;origine per la generazione di rapporti da [!DNL Analytics] a [!DNL Target] o viceversa dopo l’attivazione di un’attività.
* Sebbene le metriche calcolate non siano supportate come metriche dell’obiettivo primario, spesso è possibile ottenere il risultato desiderato selezionando invece un evento personalizzato come metrica dell’obiettivo principale. Ad esempio, se desideri ottimizzare per una metrica come &quot;completamenti del modulo per visitatore&quot;, seleziona un evento personalizzato corrispondente a &quot;completamenti del modulo&quot; come metrica di obiettivo principale. [!DNL Target] normalizza automaticamente le metriche di conversione per visita per tenere conto della distribuzione del traffico irregolare, quindi non è necessario utilizzare una metrica calcolata per eseguire la normalizzazione.

### Allocazione automatica {#aa}

* **Frequenza di formazione**: [!UICONTROL Allocazione automatica] i modelli continuano a allenarsi ogni ora, come al solito.
* **Modelli di attribuzione**: [!DNL Target] utilizza [!DNL Adobe Analytics] modello di attribuzione predefinito per[!UICONTROL  Allocazione automatica] attività che utilizzano A4T.
* **Affidabilità**: Formula di affidabilità utilizzata da [!UICONTROL Allocazione automatica] le attività sono diverse dalla formula mostrata per impostazione predefinita nel [!DNL Adobe Analytics] [!UICONTROL A4T] pannello. [Come descritto qui](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md), [!UICONTROL Allocazione automatica] utilizza intervalli di affidabilità più conservativi rispetto a quelli regolari [!UICONTROL Test A/B] attività. Questi livelli di affidabilità conservativi compensano le valutazioni ripetute (sbirce) ai dati. Di conseguenza, il rapporto predefinito in [!DNL Adobe Analytics] mostra intervalli di affidabilità più stretti rispetto a quelli utilizzati dal [!UICONTROL Allocazione automatica] algoritmo. Tuttavia, puoi determinare quale esperienza è preferita dagli algoritmi in base ai quali l’esperienza ha più visitatori univoci che vengono inviati a essa.
* **Stato vincitore**: Attualmente, il [Badge &quot;Ancora nessun vincitore&quot; e &quot;Vincitore&quot;](/help/main/c-activities/automated-traffic-allocation/determine-winner.md) non sono disponibili nel [!UICONTROL A4T] pannello in [!DNL Analysis Workspace]. Anche questi badge non sono disponibili se lo stesso rapporto viene visualizzato in [!DNL Target]. Un badge &quot;stella&quot; vincitore mostrato in un [!DNL Target] rapporto per un [!UICONTROL Allocazione automatica] le attività che utilizzano A4T devono essere ignorate. Questo badge riflette i calcoli di affidabilità regolari e non quelli utilizzati da [!UICONTROL Allocazione automatica].

### Targeting automatico {#at}

* [!UICONTROL Targeting automatico] I modelli continuano a allenarsi ogni 24 ore, come al solito. Tuttavia, i dati evento di conversione provenienti da [!DNL Analytics] è ritardato di sei a 24 ore in più. Questo ritardo significa la distribuzione del traffico per [!DNL Target] segue gli ultimi eventi registrati in [!DNL Analytics]. Questo ritardo ha l&#39;effetto più grande nelle prime 48 ore dopo l&#39;attivazione iniziale di un&#39;attività. Le prestazioni dell&#39;attività si riflettono più strettamente [!DNL Analytics] comportamento di conversione dopo cinque giorni.

   Considera l&#39;utilizzo di [!UICONTROL Allocazione automatica] anziché [!UICONTROL Targeting automatico] per le attività a breve termine in cui la maggior parte del traffico si verifica entro i primi cinque giorni della vita dell’attività.

* Quando utilizzi [!DNL Analytics] come origine dati per un [!UICONTROL Targeting automatico] attività, le sessioni terminano dopo sei ore. Le conversioni che si verificano dopo sei ore non sono conteggiate.

Per ulteriori informazioni, consulta [Modelli di attribuzione e finestre di lookback](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html) in *Guida agli strumenti di Analytics*.

## Esercitazioni

Sebbene siano disponibili funzionalità avanzate di analisi in [!DNL Adobe Analytics] [!UICONTROL Analysis Workspace], alcune modifiche all&#39;impostazione predefinita [!UICONTROL Analytics for Target] Il pannello è necessario per interpretare correttamente [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico] attività. Queste modifiche sono necessarie a causa delle differenze tra le attività di sperimentazione (manuale A/B e [!UICONTROL Allocazione automatica]) e attività di personalizzazione ([!UICONTROL Targeting automatico]).

### Configurazione dei rapporti A4T in [!DNL Analysis Workspace] per le attività di [!UICONTROL Allocazione automatica] 

Questa esercitazione illustra le modifiche consigliate per l’analisi [!UICONTROL Allocazione automatica] attività [!DNL Analysis Workspace].

Per ulteriori informazioni, consulta [Come impostare rapporti A4T in Analysis Workspace per le attività di allocazione automatica](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-allocate-activities.html?lang=it){target=_blank} in *Tutorials Adobe Target*.

### Configurazione dei rapporti A4T in [!DNL Analysis Workspace] per le attività di [!UICONTROL Targeting automatico] 

Questa esercitazione illustra le modifiche consigliate per l’analisi [!UICONTROL Targeting automatico] attività [!DNL Analysis Workspace].

Per ulteriori informazioni, consulta [Come impostare rapporti A4T in Analysis Workspace per le attività di Targeting automatico](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html?lang=it){target=_blank} in *Tutorials Adobe Target*.


