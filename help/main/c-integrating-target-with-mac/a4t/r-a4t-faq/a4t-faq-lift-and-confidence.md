---
keywords: faq;domande frequenti;analytics for target;a4t;incremento;ad hoc;report builder;affidabilità
description: Risposte alle domande su incremento e affidabilità quando si utilizza Analytics per [!DNL Target] (A4T). A4T consente di utilizzare il reporting di Analytics per [!DNL Target] attività.
title: Dove posso trovare informazioni su incremento e affidabilità con A4T?
feature: Analytics for Target (A4T)
exl-id: 42fd179b-944a-4a0a-b299-85ea4a7ea244
source-git-commit: aff96eca1380f4274dba0c1567f6e41d42f4b5ab
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 15%

---

# Incremento e affidabilità - Domande frequenti su A4T

Questo argomento contiene le risposte alle domande che vengono spesso poste in merito a incremento e affidabilità durante l’utilizzo di [!DNL Adobe Analytics] come origine di reporting per [!DNL Adobe Target] (A4T).

## Posso eseguire calcoli offline per A4T? {#section_55B5B750E17D414CAECBEECE27B15D81}

+++Risposta Puoi eseguire calcoli offline per A4T, ma è necessario un passaggio di esportazione dei dati in [!DNL Analytics]. Per ulteriori informazioni, consulta [Calcoli statistici nei test A/Bn](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

+++

## Come viene calcolato l’incremento? {#section_8CAE788EED5646C4B1D64A0D22070734}

+++Incremento risposta è la differenza percentuale tra i risultati della pagina di controllo e una variante di test riuscita.

+++

## Come viene calcolata l’affidabilità? {#section_97DB24D833E742988318CA65DA65DAD9}

+++Risposta Il livello di affidabilità è una probabilità, espressa in percentuale, che è uguale a `1 - p-value`, in cui `p-value` è calcolato da un test t. Consulta [Calcoli statistici nei test A/Bn](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

+++

## Perché non riesco a vedere l’incremento e l’affidabilità sulle metriche calcolate? {#lift-confidence}

+++Le metriche calcolate di risposta non sono attualmente supportate nelle funzioni di incremento e affidabilità. Analytics calcola le metriche a livello aggregato, anziché a livello di visitatore. Confidence, in particolare, è un calcolo a livello di visitatore.

Gli eventi non calcolati (standard) sono supportati in incremento e affidabilità. Essi diventano il numeratore nella funzione lift; il numeratore non può essere un calcolo di per sé. Il denominatore è la metrica di normalizzazione (impression, visite o visitatori). Alcuni esempi di eventi standard includono ordini, ricavi, conversioni di attività, eventi personalizzati da 1 a 1000 e così via. Le metriche di ottimizzazione comuni, come il tasso di conversazione (Ordini/Visitatore) e RPV (Ricavo/Visitatore), sono supportate in incremento e affidabilità.

Esempi di metriche o casi d’uso non supportati includono:

* Valore medio ordine (ricavi/ordine, per visitatore). AOV non è supportato perché il numeratore è una metrica calcolata. Al contrario, si consiglia di considerare le due metriche che influenzano l’AOV: Ricavo per visitatore e Tasso di conversione.
* Metriche calcolate che corrispondono alla somma degli eventi standard. Ad esempio, puoi tenere traccia di dieci diversi moduli lead in dieci eventi separati, quindi aggiungerli per ottenere l’invio totale di lead. Un metodo consigliato per tenere traccia di questi eventi consiste nell’implementare un singolo evento di invio di lead in Analytics, quindi utilizzare un eVar per raccogliere il tipo di modulo del lead. L’utilizzo di questo metodo richiede meno variabili e garantisce che sia possibile utilizzare la metrica di invio del singolo lead nelle funzioni di incremento e affidabilità.

+++

## Come gestisce A4T i calcoli di affidabilità? {#section_66115EAF1BA34F7A8FCED7B08DA4F99C}

+++Risposta
[!DNL Adobe Analytics] tratta tutte le metriche come non binarie e, pertanto, calcola i valori di affidabilità/p in modo diverso rispetto all’utilizzo di metriche binarie in un normale test t. In particolare, i calcoli utilizzati da A4T consentono a ogni utente di avere un risultato metrico continuo (non solo 1 o 0 per ogni utente), in modo che la varianza (o, in relazione, la deviazione standard) per ogni esperienza debba essere calcolata in modo appropriato. Gli ordini estremi non vengono considerati. Inoltre, il calcolo dell’affidabilità non applica una correzione Bonferroni per offerte multiple.

+++

## L’incremento e l’affidabilità funzionano in Ad Hoc e Report Builder? Se non sono funzioni native, posso intervenire io? {#section_D8BB69AE700B4C5CB5FD28DB51F9A4E9}

+++L’incremento e l’affidabilità della risposta non funzionano in Ad Hoc o Report Builder e non possono essere calcolati autonomamente per le variabili continue. È possibile calcolarli manualmente per metriche binarie.
+++
