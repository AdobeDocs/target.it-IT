---
keywords: faq;frequently asked questions;analytics for target;a4T;lift;ad hoc;report builder;confidence
description: Questo argomento contiene le risposte alle domande che vengono spesso poste in merito ai concetti di incremento e affidabilità durante l’utilizzo di Analytics come origine per la creazione di rapporti per Target (A4T).
title: Incremento e affidabilità - Domande frequenti su A4T
feature: a4t troubleshooting
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 50%

---


# Incremento e affidabilità - Domande frequenti su A4T{#lift-and-confidence-a-t-faq}

Questo argomento contiene le risposte alle domande che vengono spesso poste in merito ai concetti di incremento e affidabilità durante l’utilizzo di Analytics come origine per la creazione di rapporti per Target (A4T).

## Posso eseguire calcoli offline per A4T? {#section_55B5B750E17D414CAECBEECE27B15D81}

Puoi eseguire calcoli offline per A4T, ma è necessario un ulteriore passaggio di esportazione dei dati di [!DNL Analytics]. Per ulteriori informazioni, vedi “Esecuzione di calcoli offline per Analytics per Target” (A4T) in [Livello di affidabilità e intervallo di affidabilità](/help/c-reports/conversion-rate.md#concept_0D0002A1EBDF420E9C50E2A46F36629B).

## Come viene calcolato l’incremento? {#section_8CAE788EED5646C4B1D64A0D22070734}

L’incremento è la differenza percentuale tra i risultati della pagina di controllo e una variante di test riuscita.

## Come viene calcolata l’affidabilità? {#section_97DB24D833E742988318CA65DA65DAD9}

Il livello di affidabilità è la probabilità che il tasso di conversione misurato differisca dal tasso di conversione della pagina campione per ragioni diverse dalla sola casualità.

## Perché non riesco a vedere l’incremento e l’affidabilità sulle metriche calcolate?  {#lift-confidence}

Le metriche calcolate non sono attualmente supportate nelle funzioni di incremento e confidenza. Ciò è dovuto al fatto che Analytics calcola le metriche a livello di aggregato, anziché a livello di visitatore. La confidenza, in particolare, è un calcolo a livello di visitatore.

Gli eventi non calcolati (standard) sono supportati in incremento e confidenza. Diventano il numeratore nella funzione di sollevamento; il numeratore non può essere un calcolo stesso. Il denominatore è la normalizzazione delle metriche (impression, visite o visitatori). Alcuni esempi di eventi standard includono ordini, ricavi, conversioni di attività, eventi personalizzati 1-1000, ecc. Ciò significa che le metriche di ottimizzazione comuni, come il tasso di conversazione (Ordini/Visitatori) e RPV (Entrate/Visitatori) sono supportate in incremento e confidenza.

Esempi di metriche o casi di utilizzo non supportati:

* Valore ordine medio (ricavi/ordine, per visitatore). AOV non è supportato perché il numeratore è una metrica calcolata. Al contrario, la raccomandazione è di considerare le due metriche influenti di AOV - Revenue per Visitors (Entrate per visitatore) e Conversion Rate (Tasso di conversione).
* Metriche calcolate che rappresentano la somma degli eventi standard. Ad esempio, potete tenere traccia di dieci diversi moduli lead in dieci eventi separati, quindi aggiungerli insieme per ottenere il totale degli invii lead. Un metodo consigliato per tenere traccia di questi eventi consiste nell’implementare un singolo evento di invio dei lead in Analytics e quindi utilizzare un eVar  per raccogliere il tipo di modulo lead. L’utilizzo di questo metodo richiede un numero minore di variabili e garantisce l’utilizzo della metrica di invio dei lead nelle funzioni di incremento e confidenza.

## Come gestisce A4T i calcoli di affidabilità?  {#section_66115EAF1BA34F7A8FCED7B08DA4F99C}

A4T utilizza calcoli metrici non binari con la somma dei dati al quadrato. La varianza viene calcolata utilizzando la somma dei dati al quadrato. Gli ordini estremi non vengono presi in considerazione. Inoltre, il calcolo della confidenza non applica una correzione Bonferroni per offerte multiple.

## L’incremento e l’affidabilità funzionano in Ad Hoc e Report Builder? Se non sono funzioni native, posso intervenire io?  {#section_D8BB69AE700B4C5CB5FD28DB51F9A4E9}

Incremento e affidabilità non funzionano in Ad Hoc e Report Builder e non puoi calcolarli per variabili continue. È possibile calcolarli manualmente per metriche binarie.
