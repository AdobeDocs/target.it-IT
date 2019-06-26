---
description: Informazioni su come interpretare il rapporto di riepilogo del Targeting automatico.
keywords: report;targeting automatico;AT
seo-description: Informazioni su come interpretare il rapporto di riepilogo del Targeting automatico.
seo-title: Rapporto di riepilogo del Targeting automatico
solution: Target
subtopic: Test multivariato
title: Rapporto di riepilogo del Targeting automatico
topic: Standard
uuid: a30fa886-e8df-408f-bbc9-11a917a592d8
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Rapporto di riepilogo del Targeting automatico{#auto-target-summary-report}

Informazioni su come interpretare il rapporto di riepilogo del Targeting automatico.

Nella figura seguente viene illustrato l&#39;aspetto di un rapporto di riepilogo tipico quando si utilizza il Targeting automatico:

![](assets/autotarget.png)

Alcuni suggerimenti e considerazioni sull&#39;interpretazione dei rapporti di Targeting automatico:

* Le varie righe della tabella consentono di comprendere le prestazioni dell&#39;attività.

   * Le prime due righe della tabella nella pagina del rapporto mostrano i risultati di un test A/B tra i visitatori che sono stati assegnati al controllo (cioè esperienze servite in modo casuale) e i visitatori che sono stati assegnati all&#39;algoritmo di personalizzazione. Con queste informazioni è possibile misurare la modalità di esecuzione dell&#39;algoritmo di personalizzazione rispetto al controllo fornito in modo casuale.
   * Le righe restanti mostrano risultati a livello di esperienza. Per ogni esperienza, c&#39;è un confronto tra la risposta media dei visitatori di cui è stata mostrata l&#39;esperienza come un controllo fornito in modo casuale e la risposta media dei visitatori di cui è stata mostrata l&#39;esperienza utilizzando l&#39;algoritmo di personalizzazione.

* L&#39;icona di controllo verde accanto a ogni esperienza nel rapporto indica che per quell&#39;esperienza è stato generato un modello di apprendimento automatico personalizzato. L&#39;icona dell&#39;orologio indica che non è stato fornito abbastanza traffico per generare il modello.

   * Poiché il modello è generato a livello di esperienza, è possibile che un modello abbia il controllo verde per alcune esperienze e l&#39;icona dell&#39;orologio per altre.
   * In questo caso, per aumentare la velocità dell&#39;attività con modelli generati per tutte le esperienze, il traffico aggiuntivo viene inviato a esperienze con modelli non generati.
   * Ci devono essere almeno due esperienze con modelli generati (segno di spunta verde) affinché inizi la personalizzazione.

* Il confronto tra il tasso di conversione di esperienza A e quello di esperienza B non è corretto nel Targeting automatico. La domanda è se l&#39;esperienza A funziona meglio quando viene fornita in modo intelligente rispetto a un modo casuale (in altre parole, rispetto al controllo). Gli addetti al marketing dovrebbero anche usare cautela nell&#39;interpretazione degli incrementi di esperienze individuali, perché l&#39;algoritmo di personalizzazione tenta di ottimizzare secondo la metrica di successo su tutta l&#39;attività, non su ogni singola esperienza.
* Le esperienze con l&#39;incremento maggiore possono essere considerate come quelle che presentano la più alta differenziazione all&#39;interno della popolazione. Questo è l&#39;algoritmo che ha trovato un segmento che piace di più a quella particolare esperienza.

