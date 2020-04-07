---
keywords: faq;frequently asked questions;analytics for target;a4T;lift;ad hoc;report builder;confidence
description: Questo argomento contiene le risposte alle domande che vengono spesso poste in merito ai concetti di incremento e affidabilità durante l’utilizzo di Analytics come origine per la creazione di rapporti per Target (A4T).
title: Incremento e affidabilità - Domande frequenti su A4T
topic: Standard
uuid: 7d0402f3-d6f2-422e-b69c-86e10120ac83
translation-type: tm+mt
source-git-commit: b5191230c76135d5299754e72c9651d018086e60

---


# Incremento e affidabilità - Domande frequenti su A4T{#lift-and-confidence-a-t-faq}

Questo argomento contiene le risposte alle domande che vengono spesso poste in merito ai concetti di incremento e affidabilità durante l’utilizzo di Analytics come origine per la creazione di rapporti per Target (A4T).

## Posso eseguire calcoli offline per A4T? {#section_55B5B750E17D414CAECBEECE27B15D81}

Puoi eseguire calcoli offline per A4T, ma è necessario un ulteriore passaggio di esportazione dei dati di [!DNL Analytics]. Per ulteriori informazioni, vedi “Esecuzione di calcoli offline per Analytics per Target” (A4T) in [Livello di affidabilità e intervallo di affidabilità](../../../c-reports/conversion-rate.md#concept_0D0002A1EBDF420E9C50E2A46F36629B).

## Come viene calcolato l’incremento? {#section_8CAE788EED5646C4B1D64A0D22070734}

L’incremento è la differenza percentuale tra i risultati della pagina di controllo e una variante di test riuscita.

## Come viene calcolata l’affidabilità? {#section_97DB24D833E742988318CA65DA65DAD9}

Il livello di affidabilità è la probabilità che il tasso di conversione misurato differisca dal tasso di conversione della pagina campione per ragioni diverse dalla sola casualità.

## Perché non riesco a vedere l’incremento e l’affidabilità sulle metriche calcolate? {#section_D3E44E24782A409DBD88AE4D1595CB58}

L&#39;incremento e la confidenza non sono attualmente supportati con le metriche calcolate. Tuttavia, nella maggior parte dei casi questo non dovrebbe essere un problema perché il tasso di conversione calcolato nel rapporto A4T è già una metrica calcolata in cui il denominatore è la metrica di normalizzazione (istanze, visite, visitatori). Ad esempio, se selezionate la metrica degli ordini e la metrica di normalizzazione sono visitatori, il tasso di conversione (ordini/visitatore) viene calcolato automaticamente tramite il reporting A4T. La metrica di incremento risultante riflette la differenza nel tasso di conversione tra le esperienze di testo rispetto a quella predefinita.

La maggior parte delle metriche calcolate per l&#39;ottimizzazione rientra in una delle due categorie: metriche aggregate e altri calcoli di conversione come Average Order Value (AOV).

Le metriche aggregate vengono utilizzate quando un&#39;organizzazione utilizza eventi univoci per acquisire &quot;sapori&quot; diversi della conversione del salvataggio. Ad esempio, se l’obiettivo è promuovere l’invio di moduli lead e si dispone di 10 moduli lead diversi, una società potrebbe creare eventi univoci per conteggiare ogni tipo di conversione. Per visualizzare la quantità totale di tutti i moduli lead inviati, è necessario creare una semplice metrica calcolata per aggiungerli tutti insieme. Un modo migliore e più moderno per tenere traccia di questo problema consiste nell’implementare un singolo evento di invio dei lead in Analytics e quindi utilizzare un’eVar per raccogliere il tipo di modulo lead. L’utilizzo di questo metodo richiede un numero minore di variabili ed elimina la necessità di aggregare singole metriche; inoltre, con l’eVar è ancora possibile visualizzare la conversione olistica dei moduli lead e suddividerla per tipo di modulo lead. Questo elimina anche la necessità di metriche aggregate per la valutazione delle prestazioni di un&#39;attività Target.

Un&#39;altra metrica calcolata comune, Valore ordine medio, attualmente non è supportata con incremento e confidenza perché la metrica di normalizzazione non è una metrica standard (istanze, visite, visitatori). Al contrario, la raccomandazione consiste nel tenere d&#39;occhio le due metriche influenti di AOV, Revenue per Visitors (Entrate per visitatore) e Conversion Rate (Tasso di conversione).

## Come gestisce A4T i calcoli di affidabilità? {#section_66115EAF1BA34F7A8FCED7B08DA4F99C}

A4T utilizza calcoli metrici non binari con la somma dei dati al quadrato. La varianza viene calcolata utilizzando la somma dei dati al quadrato. Gli ordini estremi non vengono presi in considerazione.

Qualsiasi segmento Analytics può essere applicato al rapporto. In questo modo è possibile ottenere “l&#39;ordine estremo” e altre opzioni di segmento. Una metrica potrebbe anche essere creata in modo da limitare aspetti quali quante volte un visitatore dà luogo a una conversione.

## L’incremento e l’affidabilità funzionano in Ad Hoc e Report Builder? Se non sono funzioni native, posso intervenire io? {#section_D8BB69AE700B4C5CB5FD28DB51F9A4E9}

Incremento e affidabilità non funzionano in Ad Hoc e Report Builder e non puoi calcolarli per variabili continue. È possibile calcolarli manualmente per metriche binarie.
