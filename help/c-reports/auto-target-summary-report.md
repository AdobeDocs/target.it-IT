---
keywords: report;destinazione automatica;destinazione automatica;AT;report
description: Scoprite come interpretare il rapporto Riepilogo di Auto-Target in  Adobe Target. Da questo rapporto potete passare ai rapporti Segmenti automatizzati e Attributi importanti.
title: Come si utilizza il rapporto di riepilogo di Auto-Target?
feature: Reports
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '690'
ht-degree: 54%

---


# ![Report di riepilogo ](/help/assets/premium.png) PREMIUMAuto-Target{#auto-target-summary-report}

Informazioni su come interpretare i report [!UICONTROL Auto-Target Summary] in [!DNL Adobe Target].

>[!NOTE]
>
>La funzione di [!UICONTROL Targeting automatico] è disponibile come parte della soluzione [!DNL Target Premium]. Non è disponibile in [!DNL Target Standard] senza una licenza [Target Premium](/help/c-intro/intro.md#premium).

Per visualizzare i report [!UICONTROL Riepilogo destinazione automatica]:

1. Dalla pagina [!UICONTROL Activities], fare clic sull&#39;attività [!UICONTROL Auto-Target] desiderata.

   Se si dispone di numerose attività, è possibile filtrare l&#39;elenco selezionando le opzioni tra [!UICONTROL Tipo], [!UICONTROL Stato], [!UICONTROL Proprietà], [!UICONTROL Origine report], [!UICONTROL Experience Composer], [!UICONTROL Tipo metriche], e gli elenchi a discesa [!UICONTROL Origine attività].

1. Fare clic sulla scheda [!UICONTROL Report], quindi fare clic sull&#39;icona desiderata:

   * Vista tabella
   * Vista grafico
   * Segmenti automatizzati
   * Attributi importanti

## Vista tabella

L&#39;illustrazione seguente mostra l&#39;aspetto di un tipico rapporto di riepilogo in [!UICONTROL Visualizzazione tabella] quando si visualizza un report di attività [!UICONTROL Auto-Target]:

![Rapporto visualizzazione tabella di destinazione automatica](/help/c-reports/assets/at-table-view.png)

Alcuni suggerimenti e considerazioni durante l&#39;interpretazione dei report [!UICONTROL Auto-Target]:

* Le varie righe della tabella consentono di comprendere le prestazioni dell&#39;attività.

   * Le prime due righe della tabella nella pagina del rapporto mostrano i risultati di un test A/B tra i visitatori che sono stati assegnati al controllo (cioè esperienze servite in modo casuale) e i visitatori che sono stati assegnati all&#39;algoritmo di personalizzazione. Con queste informazioni è possibile misurare la modalità di esecuzione dell&#39;algoritmo di personalizzazione rispetto al controllo fornito in modo casuale.
   * Le righe restanti mostrano risultati a livello di esperienza. Per ogni esperienza, c&#39;è un confronto tra la risposta media dei visitatori di cui è stata mostrata l&#39;esperienza come un controllo fornito in modo casuale e la risposta media dei visitatori di cui è stata mostrata l&#39;esperienza utilizzando l&#39;algoritmo di personalizzazione.

* L&#39;icona di controllo verde accanto a ogni esperienza nel rapporto indica che per quell&#39;esperienza è stato generato un modello di apprendimento automatico personalizzato. L&#39;icona dell&#39;orologio indica che non è stato fornito abbastanza traffico per generare il modello.

   * Poiché il modello è generato a livello di esperienza, è possibile che un modello abbia il controllo verde per alcune esperienze e l&#39;icona dell&#39;orologio per altre.
   * In questo caso, per aumentare la velocità dell&#39;attività con modelli generati per tutte le esperienze, il traffico aggiuntivo viene inviato a esperienze con modelli non generati.
   * Ci devono essere almeno due esperienze con modelli generati (segno di spunta verde) affinché inizi la personalizzazione.

* Il confronto tra il tasso di conversione dell&#39;esperienza A e quello dell&#39;esperienza B non è il confronto corretto in [!UICONTROL Auto-Target]. La domanda è se l&#39;esperienza A funziona meglio quando viene fornita in modo intelligente rispetto a un modo casuale (in altre parole, rispetto al controllo). Gli addetti al marketing dovrebbero anche usare cautela nell&#39;interpretazione degli incrementi di esperienze individuali, perché l&#39;algoritmo di personalizzazione tenta di ottimizzare secondo la metrica di successo su tutta l&#39;attività, non su ogni singola esperienza.
* Le esperienze con l&#39;incremento maggiore possono essere considerate come quelle che presentano la più alta differenziazione all&#39;interno della popolazione. Questo è l&#39;algoritmo che ha trovato un segmento che piace di più a quella particolare esperienza.
* Le varie colonne della tabella mostrano il numero di visite, il tasso di conversione, il livello medio di incremento e confidenza e la confidenza. Per ulteriori informazioni, consulta [Incremento medio, limiti di incremento e intervallo di confidenza](/help/c-reports/c-report-settings/average-lift-bounds-and-confidence-interval.md).

## Vista grafico

L&#39;illustrazione seguente mostra l&#39;aspetto di un tipico rapporto di riepilogo in [!UICONTROL Visualizzazione grafico] quando si visualizza un report di attività [!UICONTROL Auto-Target]:

![Report visualizzazione grafico di destinazione automatica](/help/c-reports/assets/at-graph-view.png)

Come mostrato di seguito, potete utilizzare i due elenchi a discesa per scegliere le metriche desiderate, la metodologia di conteggio e altro ancora. Per ulteriori informazioni, vedere [Panoramica delle impostazioni dei report](/help/c-reports/c-report-settings/report-settings.md):

![Report visualizzazione grafico di destinazione automatica](/help/c-reports/assets/at-graph-view-2.png)

## Segmenti automatizzati

Fare clic sull&#39;icona [!UICONTROL Segmenti automatizzati]. Questo rapporto mostra il modo in cui i diversi visitatori rispondono in modo diverso alle offerte/esperienze nell&#39;attività AP/AT. Questo rapporto mostra come i diversi segmenti automatizzati definiti dai modelli di personalizzazione di Target rispondono alle offerte/esperienze dell&#39;attività.

![Icona segmenti automatizzati](/help/c-reports/assets/icon-automated-sements.png)

Per ulteriori informazioni, vedere [Rapporto Segmenti automatizzati](/help/c-reports/c-personalization-insights-reports/automated-segments-report.md).

## Attributi importanti

Fare clic sull&#39;icona [!UICONTROL Attributi importanti]. Questo rapporto mostra come, in attività diverse, attributi diversi siano più (o meno) importanti per il modo in cui il modello decide di personalizzare. Questo rapporto mostra gli attributi principali che hanno influenzato il modello e la loro importanza relativa.

![Icona importanti attributi](/help/c-reports/assets/icon-important-attributes.png)

Per ulteriori informazioni, vedere [Report Attributi importanti](/help/c-reports/c-personalization-insights-reports/important-attributes-report.md).
