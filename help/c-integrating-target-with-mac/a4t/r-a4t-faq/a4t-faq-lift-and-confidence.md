---
keywords: faq;domande frequenti;analytics for target;a4t;incremento;ad hoc;report builder;affidabilità
description: Trova risposte alle domande su incremento e affidabilità durante l’utilizzo di Analytics per [!DNL Target] (A4T). A4T lets you use Analytics reporting for [!DNL Target] attività.
title: Dove posso trovare informazioni su incremento e affidabilità con A4T?
feature: Analytics for Target (A4T)
exl-id: 42fd179b-944a-4a0a-b299-85ea4a7ea244
source-git-commit: 4e3a94554dd9c1e8cc6e98eda10d454536bc9b1f
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 29%

---

# Incremento e affidabilità - Domande frequenti su A4T

Questo argomento contiene le risposte alle domande più frequenti sull’incremento e l’affidabilità durante l’utilizzo [!DNL Adobe Analytics] come origine per la generazione di rapporti per [!DNL Adobe Target] (A4T).

## Posso eseguire calcoli offline per A4T? {#section_55B5B750E17D414CAECBEECE27B15D81}

Puoi eseguire calcoli offline per A4T, ma è necessario un ulteriore passaggio di esportazione dei dati di [!DNL Analytics]. Per ulteriori informazioni, vedi “Esecuzione di calcoli offline per Analytics per Target” (A4T) in [Livello di affidabilità e intervallo di affidabilità](/help/c-reports/conversion-rate.md#concept_0D0002A1EBDF420E9C50E2A46F36629B).

## Come viene calcolato l’incremento? {#section_8CAE788EED5646C4B1D64A0D22070734}

L’incremento è la differenza percentuale tra i risultati della pagina di controllo e una variante di test riuscita.

## Come viene calcolata l’affidabilità? {#section_97DB24D833E742988318CA65DA65DAD9}

Il livello di affidabilità è una probabilità, espressa in percentuale, pari a `1 - p-value`, dove `p-value` è calcolato da un test t. Vedi [Tasso di conversione](/help/c-reports/conversion-rate.md#concept_0D0002A1EBDF420E9C50E2A46F36629B).

## Perché non riesco a vedere l’incremento e l’affidabilità sulle metriche calcolate? {#lift-confidence}

Le metriche calcolate non sono attualmente supportate nelle funzioni di incremento e affidabilità. Analytics calcola le metriche a livello di aggregato, anziché a livello di visitatore. In particolare, Affidabilità è un calcolo a livello di visitatore.

Gli eventi non calcolati (standard) sono supportati in incremento e affidabilità. Diventano il numeratore nella funzione di incremento; il numeratore non può essere un calcolo stesso. Il denominatore è la normalizzazione delle metriche (impression, visite o visitatori). Alcuni esempi di eventi standard includono ordini, ricavi, conversioni di attività, eventi personalizzati 1-1000 e così via. Le metriche di ottimizzazione comuni, come il tasso di conversazione (Ordini/Visitatori) e RPV (Entrate/Visitatore) sono supportate in incremento e affidabilità.

Esempi di metriche o casi d’uso non supportati sono:

* Valore medio dell’ordine (ricavi/ordine, per visitatore). AOV non supportato perché il numeratore è una metrica calcolata. Invece, si consiglia di considerare le due metriche che influenzano l’AOV - Ricavo per visitatore e Tasso di conversione.
* Metriche calcolate che corrispondono alla somma degli eventi standard. Ad esempio, è possibile tenere traccia di dieci diversi moduli lead in dieci eventi distinti, quindi aggiungerli insieme per ottenere invii totali. Per tenere traccia di questi eventi, si consiglia di implementare un singolo evento di invio per lead in Analytics e quindi di utilizzare un eVar per raccogliere il tipo di modulo per lead. L’utilizzo di questo metodo richiede un numero inferiore di variabili e garantisce l’utilizzo della singola metrica di invio del lead nelle funzioni di incremento e affidabilità.

## Come gestisce A4T i calcoli di affidabilità? {#section_66115EAF1BA34F7A8FCED7B08DA4F99C}

A4T calcola valori di affidabilità/p in un modo diverso dai normali test t utilizzando metriche binarie. In particolare, i calcoli utilizzati da A4T consentono a ogni utente di ottenere un risultato metrico continuo (non solo 1 o 0 per ogni utente), in modo che la varianza (o, in modo relativo, la deviazione standard) per ogni esperienza debba essere calcolata esattamente. Gli ordini estremi non vengono considerati. Inoltre, il calcolo dell’affidabilità non applica una correzione Bonferroni per offerte multiple.

## L’incremento e l’affidabilità funzionano in Ad Hoc e Report Builder? Se non sono funzioni native, posso intervenire io? {#section_D8BB69AE700B4C5CB5FD28DB51F9A4E9}

Incremento e affidabilità non funzionano in Ad Hoc e Report Builder e non puoi calcolarli per variabili continue. È possibile calcolarli manualmente per metriche binarie.
