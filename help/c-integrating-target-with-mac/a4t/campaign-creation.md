---
keywords: a4t;A4T;Analytics as the reporting source for Target
description: È possibile configurare un’attività in Target Standard/Premium per utilizzare Adobe Analytics come origine per la generazione di rapporti (A4T).
title: Creazione di attività
feature: a4t general
topic: Advanced,Standard,Classic
uuid: b04ad535-62fb-4dd3-ab3f-23da60fbffbd
translation-type: tm+mt
source-git-commit: e203dc94e9bb34c4090f5795cbf73869808ada88
workflow-type: tm+mt
source-wordcount: '1130'
ht-degree: 24%

---


# Creazione di attività{#activity-creation}

You can configure an activity in [!DNL Target] to use [!DNL Adobe Analytics] as the reporting source (A4T).

Before you set up an activity that uses [!DNL Analytics] as the reporting source, establish the goal for the activity, such as improving revenue per visitor (RPV) or increasing clicks on your shopping cart. Scegli una metrica di successo finale per l’attività. Although you can select additional metrics at any time in [!DNL Analytics], you must still specify a particular metric you expect this test to affect.

## Creare un&#39;attività che utilizza Analytics come origine di reporting

Creating a [!DNL Target] activity that uses [!DNL Analytics] as the reporting source is similar to setting up a regular [!DNL Target] activity, with a few important differences. For example, you cannot select a segment for reporting while creating the activity because all segments available in [!DNL Analytics] can be applied when viewing a report.

1. Fai clic su **[!UICONTROL Crea attività]**.

   >[!NOTE]
   >
   >An activity name cannot include the &quot;%&quot; character if [!DNL Analytics] is used as the reporting source.

1. Seleziona il tipo di attività e inizia a impostarla.
1. Una volta nella sezione **[!UICONTROL Impostazioni]** del flusso di creazione dell’attività, scegli **[!UICONTROL Adobe Analytics]** e specifica la società.
1. Seleziona una suite di rapporti.

   Puoi scegliere qualsiasi suite di rapporti disponibile in [!DNL Analytics]. La suite di rapporti definisce dove trovare i dati raccolti disponibili. Le suite di rapporti virtuali non sono incluse nell&#39;elenco suite di rapporti.

   Possono verificarsi due eventuali errori durante la selezione della suite di rapporti:

   * Un errore che segnala che nessuna suite di rapporti è disponibile, ma l&#39;account è impostato correttamente.

      You might need to check your [!DNL Analytics] company. If your [!DNL Adobe Experience Cloud] account is tied to more than one [!DNL Analytics] company, log out of [!DNL Target], and log in to [!DNL Analytics] under the right company. Then return to [!DNL Target], and the report suites will load.

   * Non è possibile visualizzare la suite di rapporti attesa.

      Only report suites that are provisioned to connect to [!DNL Target] will be available for selection. If you don&#39;t see the report suite(s) you expect, first try logging out and logging back in to the [!DNL Adobe Experience Cloud] to try again.
   Se le suite di rapporti non sono ancora presenti nell’elenco, [contatta l’assistenza clienti](../../cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

1. Specifica il server di tracciamento.

   Consulta [Utilizzo di un server di tracciamento di Analytics](../../c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823).

1. Definite l&#39;esperienza.
1. Specifica l&#39;obiettivo dell&#39;attività.

   È necessario selezionare una metrica di successo da utilizzare come obiettivo per ogni attività. L&#39;obiettivo è l&#39;attività di conversione che indica un&#39;attività di successo. È buona norma non eseguire mai un test senza un obiettivo da migliorare in modo specifico. You can choose any [!DNL Analytics] metric available in the [!DNL Analytics] metric selector.

   >[!NOTE]
   >
   >You can send a custom Target-based metric to [!DNL Analytics] rather than relying only on [!DNL Analytics] data. Ad esempio, è possibile monitorare i clic su una pagina, elemento solitamente non controllato da [!DNL Analytics]. This custom metric is sent to [!DNL Analytics] automatically from the [!DNL Target] server, and appears as the &quot;[!DNL Target] Conversion&quot; metric in the metrics selector in [!DNL Analytics]. The [!DNL Target] Conversion metric is empty if you choose to use [!DNL Analytics] metrics.

   L&#39;impostazione di un obiettivo non impedisce di utilizzare un&#39;altra metrica per valutare i risultati dei test. L&#39;obiettivo, tuttavia, funge da promemoria rispetto all&#39;elemento da migliorare con l&#39;attività.

   Il visitatore resta nell&#39;attività dopo aver raggiunto l&#39;obiettivo. Il visitatore continua a visualizzare il contenuto dell&#39;attività ma non viene conteggiato come nuovo accesso all&#39;attività.

   >[!NOTE]
   >
   >When setting up an activity after setting up [!DNL Analytics] as your reporting source, there is no option to set up audiences for reporting. [!DNL Analytics] i segmenti sono disponibili nel rapporto [!DNL Target] Attività.

1. Fai clic su **[!UICONTROL Salva]**.

## Supporto di Analytics per Target (A4T) per le attività di allocazione automatica {#a4t-aa}

Abbiamo aggiornato l&#39;integrazione  Adobe Target- Adobe Analytics, nota come [Analytics for Target](/help/c-integrating-target-with-mac/a4t/a4t.md).

[!UICONTROL Le attività di allocazione] automatica ora supportano [!UICONTROL Analytics per Target]. Questa integrazione consente di utilizzare la funzionalità di allocazione automatica dei bandi con più braccia per indirizzare il traffico verso esperienze vincenti, utilizzando al tempo stesso una metrica di obiettivo e/o funzionalità di reporting e analisi [!DNL Adobe Analytics] o [!DNL Adobe Analytics] reporting. Se avete già [implementato A4T per l&#39;utilizzo con le attività](/help/c-integrating-target-with-mac/a4t/a4timplementation.md)Test A/B e Targeting delle esperienze, siete pronti!

Per iniziare:

1. Create un&#39;attività test A/B e selezionate l&#39;opzione di allocazione **[!UICONTROL automatica per una migliore esperienza]** come metodo **[!UICONTROL di allocazione del]** traffico nella pagina [!UICONTROL Targeting] .
1. Seleziona **[!UICONTROL Adobe Analytics]** per l&#39;origine **[!UICONTROL di]** reporting nella pagina **[!UICONTROL Obiettivi e impostazioni]** e seleziona la suite di rapporti corrispondente all&#39;obiettivo di ottimizzazione desiderato.
1. Scegliere una metrica Obiettivo principale.

   Scegliete **[!UICONTROL Conversione]** da utilizzare [!DNL Adobe Target] per specificare l&#39;obiettivo di ottimizzazione.

   Oppure

   Scegliete **[!UICONTROL Usa una metrica]** Analytics, quindi selezionate una metrica [!DNL Analytics] da usare come obiettivo di ottimizzazione. Potete utilizzare una metrica di conversione out-of-box [!DNL Analytics] o un evento [!DNL Analytics] personalizzato.

1. Salvate e attivate l&#39;attività.

   [!UICONTROL Allocazione] automatica utilizzerà la metrica selezionata per ottimizzare l&#39;attività, spingendo i visitatori verso un&#39;esperienza che massimizza la metrica dell&#39;obiettivo.

1. Utilizzate la scheda **[!UICONTROL Rapporti]** per visualizzare i rapporti dell&#39;attività in base alle [!DNL Adobe Analytics] metriche selezionate. Fai clic su **[!UICONTROL Visualizza in Analytics]** per approfondire e segmentare ulteriormente i dati di reporting.

### Metriche obiettivo supportate

A4T per l’allocazione [!UICONTROL automatica] consente di scegliere uno dei seguenti tipi di metriche come metrica obiettivo principale per l’ottimizzazione:

* [!DNL Adobe Target] metriche di conversione
* [!DNL Adobe Analytics] metriche di conversione
* [!DNL Adobe Analytics] eventi personalizzati

A4T per l&#39;allocazione [!UICONTROL automatica] richiede di scegliere una metrica basata su un evento binomiale, ovvero un evento che non si verifica o non si verifica, ad esempio un clic, una conversione, un ordine ecc. (Questi tipi di eventi sono anche a volte denominati eventi Bernoulli, binari o discreti.)

A4T per l&#39;allocazione [!UICONTROL automatica] non supporta l&#39;ottimizzazione per metriche continue come le entrate, il numero di prodotti ordinati, la durata della sessione, il numero di visualizzazioni di pagina nella sessione, ecc. (Questi tipi di metriche non supportati sono anche a volte denominate metriche non binomiali o non Bernoulli.)

I seguenti tipi di metriche non sono supportati come metriche dell&#39;obiettivo primario:

* [!DNL Adobe Target] metriche di coinvolgimento e ricavi
* [!DNL Adobe Analytics] metriche di coinvolgimento e ricavi

   >[!NOTE]
   >
   >Potrebbe essere possibile selezionare metriche [!DNL Analytics] di coinvolgimento e ricavi come metrica principale dell&#39;obiettivo, perché [!DNL Target] non è in grado di identificare tutte le metriche di coinvolgimento e ricavi da [!DNL Analytics]. Fai attenzione a selezionare solo metriche di conversione binomiali o eventi personalizzati da [!DNL Analytics].

*  metriche calcolate Adobe Analytics

### Limitazioni e note

* L&#39;origine di reporting non può essere modificata da [!DNL Analytics] a [!DNL Target] o viceversa dopo che un&#39;attività è stata attivata.
* Sebbene le metriche calcolate non siano supportate come metriche dell&#39;obiettivo principale, spesso è possibile ottenere il risultato desiderato selezionando invece un evento personalizzato come metrica dell&#39;obiettivo principale. Ad esempio, se si desidera ottimizzare per una metrica come &quot;completamenti del modulo per visitatore&quot;, selezionare un evento personalizzato corrispondente a &quot;completamento del modulo&quot; come metrica obiettivo principale. [!DNL Target] normalizza automaticamente le metriche di conversione in base a ogni visita per tenere conto della distribuzione del traffico non uniforme, quindi non è necessario utilizzare una metrica calcolata per eseguire la normalizzazione.
* [!DNL Target] utilizza il modello di attribuzione &quot;Same Touch&quot; nell’implementazione Allocazione automatica A4T.

Per ulteriori informazioni, consulta Panoramica [sull’](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/attribution/attribution.html) attribuzione nella guida *degli strumenti di* Analytics.
