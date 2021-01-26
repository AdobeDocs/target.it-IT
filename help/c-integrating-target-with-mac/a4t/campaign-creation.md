---
keywords: a4t;A4T;Analytics as the reporting source for Target
description: È possibile configurare un’attività in Target Standard/Premium per utilizzare Adobe Analytics come origine per la generazione di rapporti (A4T).
title: Creare un'attività che utilizza A4T come origine di reporting
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: cf47b7f3625bb1c3430b9fba00c573f489efc448
workflow-type: tm+mt
source-wordcount: '1394'
ht-degree: 19%

---


# Creare un&#39;attività che utilizza Analytics come origine di reporting

Potete configurare un&#39;attività in [!DNL Target] per utilizzare [!DNL Adobe Analytics] come origine di reporting (A4T).

Prima di impostare un&#39;attività che utilizza [!DNL Analytics] come origine di reporting, stabilire l&#39;obiettivo per l&#39;attività, ad esempio migliorare le entrate per visitatore (RPV) o aumentare i clic sul carrello. Scegli una metrica di successo finale per l’attività. Sebbene sia possibile selezionare metriche aggiuntive in qualsiasi momento in [!DNL Analytics], è comunque necessario specificare una metrica specifica che si prevede verrà interessata dal test.

## Crea l&#39;attività

La creazione di un&#39;attività [!DNL Target] che utilizza [!DNL Analytics] come origine di reporting è simile alla configurazione di un&#39;attività [!DNL Target] regolare, con alcune importanti differenze. Ad esempio, non è possibile selezionare un segmento per il reporting durante la creazione dell&#39;attività, perché tutti i segmenti disponibili in [!DNL Analytics] possono essere applicati quando si visualizza un rapporto.

1. Fai clic su **[!UICONTROL Crea attività]**.

   >[!NOTE]
   >
   >Un nome di attività non può includere il carattere &quot;%&quot; se [!DNL Analytics] viene utilizzato come origine di reporting.

1. Seleziona il tipo di attività e inizia a impostarla.
1. Una volta nella sezione **[!UICONTROL Impostazioni]** del flusso di creazione dell’attività, scegli **[!UICONTROL Adobe Analytics]** e specifica la società.
1. Seleziona una suite di rapporti.

   Puoi scegliere qualsiasi suite di rapporti disponibile in [!DNL Analytics]. La suite di rapporti definisce dove trovare i dati raccolti disponibili. Le suite di rapporti virtuali non sono incluse nell&#39;elenco suite di rapporti.

   Possono verificarsi due eventuali errori durante la selezione della suite di rapporti:

   * Un errore che segnala che nessuna suite di rapporti è disponibile, ma l&#39;account è impostato correttamente.

      Potrebbe essere necessario controllare la società [!DNL Analytics]. Se l&#39;account [!DNL Adobe Experience Cloud] è associato a più società [!DNL Analytics], disconnettetevi da [!DNL Target] ed effettuate l&#39;accesso a [!DNL Analytics] nella società giusta. Quindi tornate a [!DNL Target] e le suite di rapporti verranno caricate.

   * Non è possibile visualizzare la suite di rapporti attesa.

      Solo le suite di rapporti per le quali è stato eseguito il provisioning per la connessione a [!DNL Target] saranno disponibili per la selezione. Se non visualizzi le suite di rapporti previste, prova prima a disconnettersi ed eseguire nuovamente il login a [!DNL Adobe Experience Cloud] per riprovare.
   Se le suite di rapporti non sono ancora presenti nell’elenco, [contatta l’assistenza clienti](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

1. Specifica il server di tracciamento.

   Consulta [Utilizzo di un server di tracciamento di Analytics](/help/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823).

1. Definite l&#39;esperienza.
1. Specifica l&#39;obiettivo dell&#39;attività.

   È necessario selezionare una metrica di successo da utilizzare come obiettivo per ogni attività. L&#39;obiettivo è l&#39;attività di conversione che indica un&#39;attività di successo. È buona norma non eseguire mai un test senza un obiettivo da migliorare in modo specifico. Potete scegliere qualsiasi metrica [!DNL Analytics] disponibile nel selettore delle metriche [!DNL Analytics].

   >[!NOTE]
   >
   >Puoi inviare una metrica personalizzata basata su Target a [!DNL Analytics] anziché affidarti solo ai dati [!DNL Analytics]. Ad esempio, è possibile monitorare i clic su una pagina, elemento solitamente non controllato da [!DNL Analytics]. Questa metrica personalizzata viene inviata automaticamente a [!DNL Analytics] dal server [!DNL Target] e viene visualizzata come metrica &quot;[!DNL Target] Conversion&quot; nel selettore delle metriche in [!DNL Analytics]. La metrica di conversione [!DNL Target] è vuota se si sceglie di utilizzare le metriche [!DNL Analytics].

   L&#39;impostazione di un obiettivo non impedisce di utilizzare un&#39;altra metrica per valutare i risultati dei test. L&#39;obiettivo, tuttavia, funge da promemoria rispetto all&#39;elemento da migliorare con l&#39;attività.

   Il visitatore resta nell&#39;attività dopo aver raggiunto l&#39;obiettivo. Il visitatore continua a visualizzare il contenuto dell&#39;attività ma non viene conteggiato come nuovo accesso all&#39;attività.

   >[!NOTE]
   >
   >Quando si configura un&#39;attività dopo aver configurato [!DNL Analytics] come origine di reporting, non è disponibile alcuna opzione per impostare audience per il reporting. [!DNL Analytics] i segmenti sono disponibili nel rapporto  [!DNL Target] Attività.

1. Fai clic su **[!UICONTROL Salva]**.

## Supporto di Analytics per Target (A4T) per le attività di allocazione automatica e di destinazione automatica {#a4t-aa}

È stata aggiornata l&#39;integrazione  Adobe Target- Adobe Analytics, nota come [Analytics for Target](/help/c-integrating-target-with-mac/a4t/a4t.md). Le attività di allocazione automatica e di targeting automatico ora supportano Analytics per Target.

Questa integrazione consente di:

* Utilizzate la funzionalità di allocazione automatica di [bandit multi-armate di Auto-Allocate](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) per indirizzare il traffico alle esperienze vincenti
* Utilizzate l&#39;algoritmo di apprendimento per computer di [Auto-Target](/help/c-activities/auto-target/auto-target-to-optimize.md) di Auto-Target per scegliere l&#39;esperienza migliore per ogni visitatore in base al profilo, al comportamento e al contesto in cui si trovano, utilizzando tutte le funzionalità di reporting e analisi [!DNL Adobe Analytics] di [!DNL Adobe Analytics]&quot;.

Assicuratevi di aver [implementato A4T per l&#39;utilizzo con attività Test A/B e Targeting delle esperienze](/help/c-integrating-target-with-mac/a4t/a4timplementation.md). Se si utilizza `analyticsLogging = client_side`, è necessario anche passare il valore `sessionId` a [!DNL Analytics]. Per ulteriori informazioni, vedi [Analytics for Target (A4T) reporting](https://adobetarget-sdks.gitbook.io/docs/integration-with-experience-cloud/analytics-for-target-a4t-reporting) nella *Adobe Target SDKs* guida.

Per iniziare:

1. Durante la creazione di un&#39;attività di test A/B, nella pagina **[!UICONTROL Targeting]**, selezionare una delle seguenti opzioni come **[!UICONTROL Metodo di allocazione traffico]**:

   * Assegnazione automatica per esperienze ottimali
   * Targeting automatico per esperienze personalizzate

1. Selezionare **[!UICONTROL Adobe Analytics]** per **[!UICONTROL Origine report]** nella pagina **[!UICONTROL Goals &amp; Settings]** (Obiettivi e impostazioni) e selezionare la suite di rapporti corrispondente all&#39;obiettivo di ottimizzazione desiderato.

1. Scegliere una metrica Obiettivo principale.

   * Scegliere **[!UICONTROL Conversion]** per utilizzare [!DNL Adobe Target] per specificare l&#39;obiettivo di ottimizzazione.
   * Scegliete **[!UICONTROL Usa una metrica Analytics]**, quindi selezionate una metrica da [!DNL Analytics] da utilizzare come obiettivo di ottimizzazione. È possibile utilizzare una metrica di conversione [!DNL Analytics] out-of-box o un evento personalizzato [!DNL Analytics].

1. Salvate e attivate l&#39;attività.

   [!UICONTROL Auto-] Allocateutilizzerà la metrica selezionata per ottimizzare l&#39;attività, portando i visitatori all&#39;esperienza che massimizza la metrica dell&#39;obiettivo.

   Oppure

   [!UICONTROL Il ] targeting automatico utilizzerà la metrica selezionata per ottimizzare l&#39;attività, portando i visitatori a un&#39;esperienza personalizzata.

1. Utilizzate la scheda **[!UICONTROL Reports]** per visualizzare i report dell&#39;attività in base alle metriche [!DNL Adobe Analytics] selezionate. Fai clic su **[!UICONTROL Visualizza in Analytics]** per approfondire e segmentare ulteriormente i dati di reporting.

### Metriche obiettivo supportate

[!UICONTROL A4] Tfor  [!UICONTROL Auto-] Allocateand  [!UICONTROL Auto-] Targetconsente di scegliere uno dei seguenti tipi di metriche come metrica di obiettivo principale per l’ottimizzazione:

* [!DNL Adobe Target] metriche di conversione
* [!DNL Adobe Analytics] metriche di conversione
* [!DNL Adobe Analytics] eventi personalizzati

[!UICONTROL A4] Per l&#39; [!UICONTROL allocazione ] automatica e la   targeting automatico, è necessario scegliere una metrica basata su un evento binomiale, ovvero un evento che si verifica o meno, ad esempio un clic, una conversione, un ordine e così via. (Questi tipi di eventi sono anche a volte denominati eventi Bernoulli, binari o discreti.)

[!UICONTROL A4] Tfor  [!UICONTROL Auto-] Allocateand  [!UICONTROL Auto-] Targetnon supporta l&#39;ottimizzazione per metriche continue come le entrate, il numero di prodotti ordinati, la durata della sessione, il numero di visualizzazioni di pagina nella sessione, ecc. (Questi tipi di metriche non supportati sono anche a volte denominate metriche non binomiali o non Bernoulli.)

I seguenti tipi di metriche non sono supportati come metriche dell&#39;obiettivo primario:

* [!DNL Adobe Target] metriche di coinvolgimento e ricavi
* [!DNL Adobe Analytics] metriche di coinvolgimento e ricavi

   Potrebbe essere possibile selezionare una metrica di coinvolgimento o ricavi [!DNL Analytics] come metrica di obiettivo principale, perché [!DNL Target] non è in grado di identificare ed escludere tutte le metriche di coinvolgimento e ricavi da [!DNL Analytics]. Prestate attenzione a selezionare solo metriche di conversione binomiali o eventi personalizzati da [!DNL Analytics].

* [!DNL Adobe Analytics] metriche calcolate

### Limitazioni e note

Alcune limitazioni e note si applicano sia all&#39;allocazione automatica che alla destinazione automatica. Altre limitazioni e note si applicano a un tipo di attività o all&#39;altro.

#### Allocazione automatica e targeting automatico

* L&#39;origine di reporting non può essere modificata da [!DNL Analytics] a [!DNL Target] o viceversa dopo che un&#39;attività è stata attivata.
* Sebbene le metriche calcolate non siano supportate come metriche dell&#39;obiettivo principale, spesso è possibile ottenere il risultato desiderato selezionando invece un evento personalizzato come metrica dell&#39;obiettivo principale. Ad esempio, se si desidera ottimizzare per una metrica come &quot;completamenti del modulo per visitatore&quot;, selezionare un evento personalizzato corrispondente a &quot;completamento del modulo&quot; come metrica obiettivo principale. [!DNL Target] normalizza automaticamente le metriche di conversione in base a ogni visita per tenere conto della distribuzione del traffico non uniforme, quindi non è necessario utilizzare una metrica calcolata per eseguire la normalizzazione.
* [!DNL Target] utilizza il modello di attribuzione &quot;Stesso tocco&quot; nella funzione di  [!UICONTROL allocazione ] automatica: Analytics per Target (A4T).

#### Allocazione automatica

* [!UICONTROL Gli ] allocatemodels automatici continuano a allenarsi ogni due ore, come al solito.

#### Targeting automatico

* [!UICONTROL I modelli Auto-] Targetmodelli continuano a essere formati ogni 24 ore, come al solito. Tuttavia, i dati evento di conversione provenienti da [!DNL Analytics] vengono posticipati di ulteriori 6-24 ore. Questo ritardo significa che la distribuzione del traffico per [!DNL Target] seguirà gli ultimi eventi registrati in [!DNL Analytics]. Questo avrà l&#39;effetto più grande nelle prime 48 ore dalla prima attivazione di un&#39;attività; le prestazioni dell&#39;attività rispecchieranno più da vicino il comportamento di conversione [!DNL Analytics] dopo cinque giorni. È consigliabile utilizzare [!UICONTROL Auto-Allocate] invece di [!UICONTROL Auto-Target] per attività di breve durata in cui il traffico si verifica nella maggior parte dei primi cinque giorni della vita dell&#39;attività.
* Quando si utilizza [!DNL Analytics] come origine dati per un&#39;attività [!UICONTROL Auto-Target], le sessioni vengono considerate come terminate dopo sei ore. Le conversioni che si verificano dopo sei ore non saranno conteggiate.

Per ulteriori informazioni, vedere [Modelli di attribuzione e finestre di lookback](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html) nella *Guida agli strumenti di Analytics*.
