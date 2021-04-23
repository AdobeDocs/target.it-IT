---
keywords: rapporti;targeting automatico;AT;rapporto
description: Scopri come interpretare il rapporto di riepilogo del Targeting automatico in Adobe Target. Da questo rapporto puoi passare ai rapporti Segmenti automatizzati e Attributi importanti .
title: Come si utilizza il rapporto di riepilogo del Targeting automatico?
feature: Rapporti
exl-id: 098fcc0e-8e17-4898-ab2f-ec74472562ff
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '691'
ht-degree: 54%

---

# ![](/help/assets/premium.png) Report di riepilogo di PREMIUMAuto-Target

Informazioni su come interpretare i rapporti [!UICONTROL Riepilogo del Targeting automatico] in [!DNL Adobe Target].

>[!NOTE]
>
>La funzione di [!UICONTROL Targeting automatico] è disponibile come parte della soluzione [!DNL Target Premium]. Non è disponibile in [!DNL Target Standard] senza una licenza [Target Premium](/help/c-intro/intro.md#premium).

Per visualizzare i rapporti [!UICONTROL Riepilogo del Targeting automatico]:

1. Dalla pagina [!UICONTROL Attività], fai clic sull&#39;attività [!UICONTROL Targeting automatico] desiderata.

   Se hai numerose attività, puoi filtrare l’elenco selezionando le opzioni da [!UICONTROL Tipo], [!UICONTROL Stato], [!UICONTROL Proprietà], [!UICONTROL Origine per i rapporti], [!UICONTROL Compositore esperienza], [!UICONTROL Tipo di metriche], elenchi a discesa e [!UICONTROL Origine attività] .

1. Fai clic sulla scheda [!UICONTROL Rapporti] , quindi fai clic sull&#39;icona desiderata:

   * Vista tabella
   * Vista grafico
   * Segmenti automatizzati
   * Attributi importanti

## Vista tabella

L&#39;illustrazione seguente mostra l&#39;aspetto di un tipico rapporto di riepilogo in [!UICONTROL Vista tabella] quando si visualizza un rapporto di un&#39;attività [!UICONTROL Targeting automatico]:

![Rapporto di visualizzazione della tabella di Targeting automatico](/help/c-reports/assets/at-table-view.png)

Alcuni suggerimenti e considerazioni sull&#39;interpretazione dei rapporti di [!UICONTROL Targeting automatico]:

* Le varie righe della tabella consentono di comprendere le prestazioni dell’attività.

   * Le prime due righe della tabella nella pagina del rapporto mostrano i risultati di un test A/B tra i visitatori che sono stati assegnati al controllo (cioè esperienze servite in modo casuale) e i visitatori che sono stati assegnati all&#39;algoritmo di personalizzazione. Con queste informazioni è possibile misurare la modalità di esecuzione dell&#39;algoritmo di personalizzazione rispetto al controllo fornito in modo casuale.
   * Le righe restanti mostrano risultati a livello di esperienza. Per ogni esperienza, c&#39;è un confronto tra la risposta media dei visitatori di cui è stata mostrata l&#39;esperienza come un controllo fornito in modo casuale e la risposta media dei visitatori di cui è stata mostrata l&#39;esperienza utilizzando l&#39;algoritmo di personalizzazione.

* L&#39;icona di controllo verde accanto a ogni esperienza nel rapporto indica che per quell&#39;esperienza è stato generato un modello di apprendimento automatico personalizzato. L&#39;icona dell&#39;orologio indica che non è stato fornito abbastanza traffico per generare il modello.

   * Poiché il modello è generato a livello di esperienza, è possibile che un modello abbia il controllo verde per alcune esperienze e l&#39;icona dell&#39;orologio per altre.
   * In questo caso, per aumentare la velocità dell&#39;attività con modelli generati per tutte le esperienze, il traffico aggiuntivo viene inviato a esperienze con modelli non generati.
   * Ci devono essere almeno due esperienze con modelli generati (segno di spunta verde) affinché inizi la personalizzazione.

* Il confronto tra il tasso di conversione dell&#39;esperienza A e quello dell&#39;esperienza B non è corretto in [!UICONTROL Targeting automatico]. La domanda è se l&#39;esperienza A funziona meglio quando viene fornita in modo intelligente rispetto a un modo casuale (in altre parole, rispetto al controllo). Gli addetti al marketing dovrebbero anche usare cautela nell&#39;interpretazione degli incrementi di esperienze individuali, perché l&#39;algoritmo di personalizzazione tenta di ottimizzare secondo la metrica di successo su tutta l&#39;attività, non su ogni singola esperienza.
* Le esperienze con l&#39;incremento maggiore possono essere considerate come quelle che presentano la più alta differenziazione all&#39;interno della popolazione. Questo è l&#39;algoritmo che ha trovato un segmento che piace di più a quella particolare esperienza.
* Le varie colonne della tabella mostrano il numero di visite, il tasso di conversione, l’incremento medio e il livello di affidabilità e l’affidabilità. Per ulteriori informazioni, consulta [Incremento medio, limiti di incremento e intervallo di confidenza](/help/c-reports/c-report-settings/average-lift-bounds-and-confidence-interval.md).

## Vista grafico

L&#39;illustrazione seguente mostra l&#39;aspetto di un tipico rapporto di riepilogo in [!UICONTROL Vista grafico] durante la visualizzazione di un rapporto di attività [!UICONTROL Targeting automatico]:

![Rapporto di visualizzazione grafico del Targeting automatico](/help/c-reports/assets/at-graph-view.png)

Come mostrato di seguito, puoi utilizzare i due elenchi a discesa per scegliere le metriche desiderate, la metodologia di conteggio e altro ancora. Per ulteriori informazioni, consulta [Panoramica delle impostazioni dei rapporti](/help/c-reports/c-report-settings/report-settings.md) .

![Rapporto di visualizzazione grafico del Targeting automatico](/help/c-reports/assets/at-graph-view-2.png)

## Segmenti automatizzati

Fai clic sull&#39;icona [!UICONTROL Segmenti automatizzati] . Questo rapporto mostra come i diversi visitatori rispondono in modo diverso alle offerte/esperienze nell&#39;attività di AP/AT. Questo rapporto mostra come i diversi segmenti automatizzati definiti dai modelli di personalizzazione di Target rispondono alle offerte/esperienze dell&#39;attività.

![Icona Segmenti automatizzati](/help/c-reports/assets/icon-automated-sements.png)

Per ulteriori informazioni, consulta [Rapporto Segmenti automatizzati](/help/c-reports/c-personalization-insights-reports/automated-segments-report.md).

## Attributi importanti

Fai clic sull&#39;icona [!UICONTROL Attributi importanti] . Questo rapporto mostra come, nelle diverse attività, i diversi attributi siano più (o meno) importanti per il modo in cui il modello decide di effettuare la personalizzazione. Questo rapporto mostra gli attributi principali che hanno influenzato il modello e la loro importanza relativa.

![Icona Attributi importanti](/help/c-reports/assets/icon-important-attributes.png)

Per ulteriori informazioni, consulta [Rapporto Attributi importanti](/help/c-reports/c-personalization-insights-reports/important-attributes-report.md).
