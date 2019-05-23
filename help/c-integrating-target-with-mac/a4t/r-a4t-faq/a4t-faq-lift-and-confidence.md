---
description: Questo argomento contiene le risposte alle domande che vengono spesso poste in merito ai concetti di incremento e affidabilità durante l’utilizzo di Analytics come origine per la creazione di rapporti per Target (A4T).
keywords: faq;domande frequenti;analytics for target;a4t;incremento;ad hoc;report builder;affidabilità
seo-description: Questo argomento contiene le risposte alle domande che vengono spesso poste in merito ai concetti di incremento e affidabilità durante l’utilizzo di Analytics come origine per la creazione di rapporti per Target (A4T).
seo-title: Incremento e affidabilità - Domande frequenti su A4T
solution: Target
title: Incremento e affidabilità - Domande frequenti su A4T
topic: Standard
uuid: 7d0402f3-d6f2-422e-b69c-86e10120ac83
translation-type: tm+mt
source-git-commit: a6b0e69777b5a408b26f04992bb30cfa6d293de2

---


# Incremento e affidabilità - Domande frequenti su A4T{#lift-and-confidence-a-t-faq}

Questo argomento contiene le risposte alle domande che vengono spesso poste in merito ai concetti di incremento e affidabilità durante l’utilizzo di Analytics come origine per la creazione di rapporti per Target (A4T).

## Posso eseguire calcoli offline per A4T? {#section_55B5B750E17D414CAECBEECE27B15D81}

Puoi eseguire calcoli offline per A4T, ma è necessario un ulteriore passaggio di esportazione dei dati di [!DNL Analytics]. Per ulteriori informazioni, vedi “Esecuzione di calcoli offline per Analytics per Target” (A4T) in [Livello di affidabilità e intervallo di affidabilità](../../../c-reports/conversion-rate.md#concept_0D0002A1EBDF420E9C50E2A46F36629B).

## Come viene calcolato l’incremento? {#section_8CAE788EED5646C4B1D64A0D22070734}

L’incremento è la differenza percentuale tra i risultati della pagina di controllo e una variante di test riuscita.

## Come viene calcolata l’affidabilità?  {#section_97DB24D833E742988318CA65DA65DAD9}

Il livello di affidabilità è la probabilità che il tasso di conversione misurato differisca dal tasso di conversione della pagina campione per ragioni diverse dalla sola casualità.

## Perché non riesco a vedere l’incremento e l’affidabilità sulle metriche calcolate?  {#section_D3E44E24782A409DBD88AE4D1595CB58}

Per le metriche calcolate non è possibile generare incremento e affidabilità. Tuttavia, nella maggior parte dei casi, non dovrebbe essere un problema perché l’incremento è normalizzato dalla metrica di normalizzazione. Ad esempio, se si seleziona l’incremento per gli ordini e la metrica di normalizzazione sono le visite, l’incremento è calcolato sul rapporto tra i due, ossia il tasso di conversione.

## Come gestisce A4T i calcoli di affidabilità?  {#section_66115EAF1BA34F7A8FCED7B08DA4F99C}

A4T utilizza calcoli metrici non binari con la somma dei dati al quadrato. La varianza viene calcolata utilizzando la somma dei dati al quadrato. Gli ordini estremi non vengono presi in considerazione.

Qualsiasi segmento Analytics può essere applicato al rapporto. In questo modo è possibile ottenere “l&#39;ordine estremo” e altre opzioni di segmento. Una metrica potrebbe anche essere creata in modo da limitare aspetti quali quante volte un visitatore dà luogo a una conversione.

## L’incremento e l’affidabilità funzionano in Ad Hoc e Report Builder? Se non è una funzione nativa, posso intervenire io?  {#section_D8BB69AE700B4C5CB5FD28DB51F9A4E9}

Incremento e affidabilità non funzionano in Ad Hoc e Report Builder e non puoi calcolarli per variabili continue. È possibile calcolarli manualmente per metriche binarie.
