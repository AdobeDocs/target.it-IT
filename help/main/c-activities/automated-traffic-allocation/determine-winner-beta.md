---
keywords: allocazione automatica del traffico;targeting;vincitore;garanzia statistica;affidabilità;determinare vincitore;incremento;affidabilità;impostazione predefinita;esperienza predefinita;allocazione automatica;allocazione automatica
description: Scopri come interpretare i risultati delle attività A/B di [!UICONTROL Auto-Allocate], concentrandoti su indicatori chiave come incremento e affidabilità.
title: Come posso interpretare [!UICONTROL Auto-Allocate] report?
feature: Auto-Allocate
hide: true
hidefromtoc: true
source-git-commit: 5fc18c6d3b493ea0a58048cc20ce3a6c2ffb7d14
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Interpreta [!UICONTROL Auto-Allocate] report

Interpretare i risultati di un&#39;attività A/B [!UICONTROL Auto-Allocate] in [!UICONTROL Adobe Target] esaminando indicatori importanti, inclusi incremento e affidabilità.

Molti addetti al marketing commettono l’errore di dichiarare un’esperienza vincente prima che i risultati indichino chiaramente quale sia l’esperienza migliore. [!DNL Target] facilita la determinazione del vincitore.

Per informazioni generali sulla dichiarazione di un vincitore, consulta [Dieci insidie frequenti per i test A/B e come evitarle](/help/main/c-activities/t-test-ab/common-ab-testing-pitfalls.md).

## Identificare l’esperienza vincente {#section_24007470CF5B4D30A06610CE8DD23CE3}

Quando si utilizza la funzione [!UICONTROL Auto-Allocate], [!DNL Target] visualizza un badge nella parte superiore della pagina dell&#39;attività che indica &quot;Ancora nessun vincitore&quot; finché l&#39;attività non raggiunge il numero minimo di conversioni con sufficiente affidabilità.

![Indicatore Nessun vincitore](/help/main/c-activities/automated-traffic-allocation/assets/no-winner-new.png)

Quando viene dichiarata l&#39;esperienza migliore, [!DNL Target] visualizza il badge &quot;Vincitore: esperienza *X*&quot;.

![Badge vincitore](/help/main/c-activities/automated-traffic-allocation/assets/winner-new.png)

>[!NOTE]
>
>[!UICONTROL Auto-Allocate] attività sono progettate per trovare la migliore esperienza tra tutte le opzioni e non solo per fare confronti in coppia con il controllo.

## Garanzie statistiche di [!UICONTROL Auto-Allocate] {#section_7AF3B93E90BA4B80BC9FC4783B6A389C}

Al termine di un&#39;attività A/B, [!UICONTROL Auto-Allocate] garantisce che il vincitore determinato abbia un tasso di falso positivo effettivo del 5%. Questo significa che solo per il 5% del tempo, il vincitore determinato non è in realtà la migliore esperienza tra tutte le esperienze nell&#39;attività. Per un test [A/A](/help/main/c-activities/t-test-ab/aa-testing.md) (con esperienze identiche), [!DNL Target] conclude un test per meno del 5% del tempo. Il comportamento previsto per un test A/A (con esperienze identiche) è l&#39;esecuzione indefinita e quindi il badge del vincitore non dovrebbe mai apparire.

[!DNL Target] non utilizza l&#39;affidabilità basata sul valore p per [!UICONTROL Auto-Allocate].

La colonna [!UICONTROL Confidence] in un&#39;attività [!UICONTROL Auto-Allocate] mostra la probabilità che un&#39;esperienza sia il vincitore entro l&#39;1% di margine di errore. L’algoritmo utilizza un effetto rilevabile minimo dell’1% tra i tassi di conversione migliori e quelli del secondo migliore. L&#39;algoritmo utilizza [la disuguaglianza di Bernstein](https://en.wikipedia.org/wiki/Bernstein_inequalities_%28probability_theory%29) per calcolare questa probabilità.

I test A/B normali calcolano l’affidabilità in base ai valori p. [!UICONTROL Auto-Allocate] non utilizza valori p. I valori p calcolano “liberamente” la probabilità che una determinata esperienza sia diversa dal controllo. Questi valori p possono essere utilizzati solo per determinare se un’esperienza è diversa dal controllo. Questi valori non possono essere utilizzati per determinare se un&#39;esperienza è diversa da un&#39;altra esperienza (non controllo).

>[!IMPORTANT]
>
>[!DNL Target] mostra un vincitore dopo un numero minimo predefinito di conversioni. Tuttavia, la decisione finale di scegliere il vincitore deve sempre basarsi sui risultati del Calcolatore dimensioni campione [!DNL Adobe Target]. [!DNL Target] non considera i tassi di conversione di base di un sito e altri aspetti importanti inseriti nel calcolatore per determinare la durata dell&#39;attività. Di conseguenza, [!DNL Target] potrebbe visualizzare un vincitore prima di quanto richiesto in base a un numero minimo di conversioni. Per ulteriori informazioni, vedere [Calcolatore dimensioni campione](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6).

## Comprendere il reporting di incremento e affidabilità nelle attività [!UICONTROL Auto-Allocate] {#lift-confidence}

Nelle attività di [!UICONTROL Auto-Allocate], la prima esperienza (per impostazione predefinita denominata Esperienza A) è sempre definita come esperienza di &quot;controllo&quot; nella scheda [!UICONTROL Reports]. Questa esperienza non viene trattata come un vero e proprio controllo statistico nella modellazione utilizzata per determinare le prestazioni delle esperienze, ma viene trattata come un riferimento o una base per alcune figure nel rapporto.

Il valore numerico di &quot;Incremento&quot; e i limiti del 95% per ogni esperienza vengono sempre calcolati in riferimento all’esperienza di &quot;Controllo&quot; definita. L&#39;esperienza &quot;Controllo&quot; definita non può avere un incremento relativo a se stessa, pertanto per questa esperienza viene segnalato un valore vuoto &quot;—&quot;. A differenza dei test A/B, nei test [!UICONTROL Auto-Allocate], se un&#39;esperienza funziona peggio del controllo definito, non viene segnalato un valore Lift negativo; viene invece visualizzato &quot;—&quot;.

Le [!UICONTROL Confidence Interval] barre visualizzate rappresentano l&#39;intervallo di affidabilità del 95% intorno alla stima media del tasso di conversione di un&#39;esperienza. Queste barre sono inoltre codificate in base al colore in relazione all’esperienza &quot;Controllo&quot; definita. La barra dell’esperienza &quot;Controllo&quot; è sempre di colore grigio. Le parti degli intervalli di affidabilità al di sotto dell’intervallo di affidabilità dell’esperienza &quot;Controllo&quot; sono di colore rosso, mentre le parti degli intervalli di affidabilità al di sopra dell’esperienza &quot;Controllo&quot; sono di colore verde.

Un vincitore si trova quando l&#39;esperienza principale con [!UICONTROL Confidence Interval] al 95% non si sovrappone ad altre esperienze. L’esperienza vincente è indicata da un contrassegno a stella verde a sinistra del nome dell’esperienza e nel banner &quot;Vincitore&quot;. Quando non è visibile alcuna stella, sullo striscione si legge &quot;Ancora nessun vincitore&quot; e non è stato ancora trovato un vincitore.

Viene inoltre riportato un numero di &quot;affidabilità&quot; accanto all’esperienza attualmente leader o vincente. Questa cifra viene segnalata solo fino a quando [!UICONTROL Confidence] dell&#39;esperienza principale non raggiunge almeno il 60%. Se nell&#39;attività [!UICONTROL Auto-Allocate] sono presenti due esperienze, questo numero rappresenta il livello di affidabilità con cui l&#39;esperienza sta ottenendo risultati migliori rispetto all&#39;altra esperienza. Se nell&#39;attività [!UICONTROL Auto-Allocate] sono presenti più di due esperienze, questo numero rappresenta il livello di affidabilità con cui le prestazioni dell&#39;esperienza sono migliori rispetto all&#39;esperienza di &quot;controllo&quot; definita. Se l’esperienza &quot;Controllo&quot; sta vincendo, non viene segnalato alcun valore &quot;Affidabilità&quot;.

## Domande frequenti {#section_C8E068512A93458D8C006760B1C0B6A2}

Considera le seguenti risposte alle domande frequenti:

### Sono passati alcuni giorni dall’inizio dell’attività. Perché tutti i valori di affidabilità mostrano ancora lo 0%?

Uno dei motivi seguenti descrive il motivo per cui lo 0% viene visualizzato nella colonna [!UICONTROL Confidence] del report per tutte le attività:

* I test A/B manuali e [!UICONTROL Auto-Allocate] utilizzano statistiche diverse per visualizzare i valori [!UICONTROL Confidence].

  I test A/B manuali utilizzano valori p basati sul test t di [Welch](https://en.wikipedia.org/wiki/Welch%27s_t-test). Un valore p rappresenta la probabilità di trovare la differenza osservata (o una differenza maggiore) tra un’esperienza e il controllo, dato che in realtà non esiste una differenza simile. Questi valori p possono essere utilizzati solo per determinare se i dati osservati sono coerenti quando un’esperienza specifica e il controllo sono uguali. Questi valori non possono essere utilizzati per determinare se un&#39;esperienza è diversa da un&#39;altra esperienza (non controllo).

  [!UICONTROL Auto-Allocate] mostra la probabilità che una determinata esperienza sia un vero vincitore in tutte le esperienze dell&#39;attività. Solo un’esperienza vincente (che è più probabile che sia il vincitore) ha un valore di affidabilità diverso da zero. Tutti gli altri elementi hanno maggiori probabilità di essere perdenti e visualizzano lo 0%.

* [!UICONTROL Auto-Allocate] inizia a mostrare un valore di affidabilità solo dopo che l&#39;esperienza vincente avrà raccolto il 60% di affidabilità. Questi livelli di affidabilità vengono generalmente visualizzati in circa la metà del tempo necessario per il completamento di un normale test A/B (anche se questo intervallo di tempo non è garantito). Per determinare la durata di un normale test A/B, utilizzare il [!DNL Adobe Target] [Calcolatore dimensioni campione](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6): inserire il tasso di conversione del controllo in &quot;Tasso di conversione di base&quot;, &quot;5%&quot; per &quot;Incremento&quot; e 95% per &quot;Affidabilità&quot;. In genere, i valori di affidabilità iniziano a comparire dopo che ogni esperienza ha accumulato almeno il 50% dei campioni richiesti per esperienza. Questo ti dà un’idea di quando inizia a comparire la fiducia.

* Se il rapporto presenta 0% per tutte le esperienze, è probabile che sia ancora troppo presto nel corso dell’attività.

### Sono disponibili i badge &quot;No Winner&quot;, &quot;Winner&quot; e &quot;star&quot; per le attività [!UICONTROL Auto-Allocate] che utilizzano [!UICONTROL Analytics as the reporting source] (A4T)?

I badge &quot;Ancora nessun vincitore&quot; e &quot;Vincitore&quot; non sono attualmente disponibili nel pannello [!UICONTROL A4T] in [!DNL Analysis Workspace]. Questi badge non sono disponibili neanche se lo stesso report viene visualizzato in [!DNL Target]. Un badge vincitore &quot;star&quot; visualizzato in un report [!DNL Target] per un&#39;attività [!UICONTROL Auto-Allocate] tramite A4T deve essere ignorato.

Per ulteriori informazioni su questa e altre limitazioni e note, vedere [Allocazione automatica](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md#aa) nel supporto di *A4T per [!UICONTROL Auto-Allocate] e [!UICONTROL Auto-Target] attività*.