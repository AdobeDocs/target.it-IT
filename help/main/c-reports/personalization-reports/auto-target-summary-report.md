---
keywords: report;targeting automatico;targeting automatico;AT;report
description: Scopri come interpretare il rapporto di riepilogo del Targeting automatico in Adobe Target. Da questo rapporto puoi passare ai rapporti Segmenti automatizzati e Attributi importanti.
title: Come si utilizza il rapporto di riepilogo del Targeting automatico?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Reports
exl-id: 098fcc0e-8e17-4898-ab2f-ec74472562ff
source-git-commit: c1a71d1fb6fa9b5c14e22fa3199358a4594bb4a1
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 37%

---

# [!UICONTROL Auto-Target Summary report]

Informazioni su come interpretare i report [!UICONTROL Auto-Target Summary] in [!DNL Adobe Target].

>[!NOTE]
>
>[!UICONTROL Auto-Target] è disponibile nella soluzione [!DNL Target Premium]. Non è disponibile in [!DNL Target Standard] senza una [licenza Target Premium](/help/main/c-intro/intro.md#premium).

Per visualizzare i report [!UICONTROL Auto-Target Summary]:

1. Dalla pagina [!UICONTROL Activities], fare clic sull&#39;attività [!UICONTROL Auto-Target] desiderata.

   Se hai numerose attività, fai clic sull&#39;icona Filtro ( ![icona Filtro](/help/main/assets/icons/Filter.svg) ) per filtrare l&#39;elenco selezionando le opzioni dagli elenchi a discesa [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type] e [!UICONTROL Activity Source].

1. Fare clic sulla scheda **[!UICONTROL Reports]**, quindi fare clic sull&#39;icona desiderata:

   * **[!UICONTROL Table View]** ( ![Icona Vista tabella](/help/main/assets/icons/Table.svg) )
   * **[!UICONTROL Graph View]** ( ![Icona Vista grafico](/help/main/assets/icons/GraphTrend.svg) )
   * **[!UICONTROL Automated Segments]** ( ![Rapporto Segmenti automatizzati](/help/main/assets/icons/AutomatedSegment.svg) )
   * [!UICONTROL Important Attributes]** ( ![Icona Attributi importanti](/help/main/assets/icons/ViewList.svg) )

## Vista tabella

Alcuni suggerimenti e considerazioni sull&#39;interpretazione dei report [!UICONTROL Auto-Target]:

* Le varie righe della tabella consentono di comprendere le prestazioni dell’attività.

   * Le prime due righe della tabella nella pagina del reporting mostrano i risultati di un test A/B tra i visitatori che sono stati assegnati al controllo (ovvero, esperienze servite in modo casuale) e i visitatori che sono stati assegnati all’algoritmo di personalizzazione. Queste informazioni possono essere utilizzate per misurare le prestazioni dell’algoritmo di personalizzazione rispetto al controllo fornito in modo casuale.
   * Le righe restanti mostrano risultati a livello di esperienza. Per ogni esperienza, c&#39;è un confronto tra la risposta media dei visitatori di cui è stata mostrata l&#39;esperienza come un controllo fornito in modo casuale e la risposta media dei visitatori di cui è stata mostrata l&#39;esperienza utilizzando l&#39;algoritmo di personalizzazione.

* L&#39;icona di controllo verde accanto a ogni esperienza nel rapporto indica che per quell&#39;esperienza è stato generato un modello di apprendimento automatico personalizzato. L&#39;icona dell&#39;orologio indica che non è stato fornito abbastanza traffico per generare il modello.

   * Poiché il modello è generato a livello di esperienza, è possibile che un modello abbia il controllo verde per alcune esperienze e l&#39;icona dell&#39;orologio per altre.
   * In questo caso, per aumentare la velocità dell&#39;attività con modelli generati per tutte le esperienze, il traffico aggiuntivo viene inviato a esperienze con modelli non generati.
   * Affinché la personalizzazione possa iniziare, devono essere presenti almeno due esperienze con modelli generati (segno di spunta verde).

* Confrontare il tasso di conversione dell&#39;esperienza A con quello dell&#39;esperienza B non è il confronto corretto in [!UICONTROL Auto-Target]. La domanda è se l&#39;esperienza A funziona meglio quando viene fornita in modo intelligente rispetto a un modo casuale (in altre parole, rispetto al controllo). Gli addetti al marketing dovrebbero anche usare cautela nell&#39;interpretazione degli incrementi di esperienze individuali, perché l&#39;algoritmo di personalizzazione tenta di ottimizzare secondo la metrica di successo su tutta l&#39;attività, non su ogni singola esperienza.
* Le esperienze con l&#39;incremento maggiore possono essere considerate come quelle che presentano la più alta differenziazione all&#39;interno della popolazione. In altre parole, l&#39;algoritmo ha trovato il segmento che più piace a quella particolare esperienza.
* Le varie colonne della tabella mostrano il numero di visite, il tasso di conversione, l’incremento medio e il livello di affidabilità e l’affidabilità. Per ulteriori informazioni, vedere [Calcoli statistici nei test A/B](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

## Vista grafico

Utilizza i due elenchi a discesa per scegliere le metriche desiderate, la metodologia di conteggio e altro ancora. Per ulteriori informazioni, vedere [Panoramica delle impostazioni dei report](/help/main/c-reports/c-report-settings/report-settings.md):

## Segmenti automatizzati

Questo rapporto mostra come i diversi visitatori rispondono in modo diverso alle offerte/esperienze nell&#39;attività di AP/AT. Questo report mostra come diversi segmenti automatizzati definiti dai modelli di personalizzazione [!DNL Target] hanno risposto alle offerte/esperienze nell&#39;attività.

Per ulteriori informazioni, consulta il [rapporto Segmenti automatizzati](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md).

## Attributi importanti

Questo rapporto mostra come, nelle diverse attività, i diversi attributi sono più (o meno) importanti per il modo in cui il modello decide di personalizzare. Questo rapporto mostra gli attributi principali che hanno influenzato il modello e la loro importanza relativa.

Per ulteriori informazioni, vedere il [report Attributi importanti](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md).
