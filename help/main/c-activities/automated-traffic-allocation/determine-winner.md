---
keywords: allocazione automatica del traffico;targeting;vincitore;garanzia statistica;affidabilità;determinare vincitore;incremento;affidabilità;impostazione predefinita;esperienza predefinita;allocazione automatica;allocazione automatica
description: Scopri come interpretare i risultati di una [!UICONTROL Allocazione automatica] Attività A/B in Adobe [!DNL Target] esaminando indicatori importanti, compresi l'incremento e l'affidabilità.
title: Come posso interpretare [!UICONTROL Allocazione automatica] Rapporti?
feature: Auto-Allocate
exl-id: 4ed00eee-8939-4958-9be6-b45a8c08afbc
source-git-commit: e9976135c46f6658030b07fce384364f0c9ff0ed
workflow-type: tm+mt
source-wordcount: '1206'
ht-degree: 29%

---

# Interpretare i rapporti di allocazione automatica

Interpretare i risultati di un [!UICONTROL Allocazione automatica] Attività A/B in [!UICONTROL Adobe Target] esaminando indicatori importanti, compresi l&#39;incremento e l&#39;affidabilità.

Molti addetti al marketing commettono l’errore di dichiarare un’esperienza vincente prima che i risultati indichino chiaramente quale sia l’esperienza migliore. [!DNL Target] consente di determinare più facilmente il vincitore.

Per informazioni generali sulla dichiarazione di un vincitore, consulta [Dieci insidie frequenti per i test A/B e come evitarle](/help/main/c-activities/t-test-ab/common-ab-testing-pitfalls.md).

## Identificare l’esperienza vincente {#section_24007470CF5B4D30A06610CE8DD23CE3}

Quando utilizzi la funzione di [!UICONTROL Allocazione automatica], [!DNL Target] mostra un badge nella parte superiore della pagina dell&#39;attività che indica “Ancora nessun vincitore” finché l&#39;attività non raggiunge il numero minimo di conversioni con sufficiente affidabilità.

![Indicatore Nessun vincitore](/help/main/c-activities/automated-traffic-allocation/assets/no-winner.png)

Quando viene dichiarato un vincitore chiaro, [!DNL Target] visualizza &quot;Vincitore: esperienza *X*.&quot;

![immagine vincitore](assets/winner.png)

>[!NOTE]
>
>Le attività di Allocazione automatica sono progettate per trovare la migliore esperienza tra tutte le opzioni e non solo per fare confronti in coppia con il controllo.

## Garanzie statistiche di Allocazione automatica {#section_7AF3B93E90BA4B80BC9FC4783B6A389C}

Al termine di un’attività A/B, [!UICONTROL Allocazione automatica] garantisce che il vincitore determinato abbia un tasso di falso positivo effettivo del 5%. Questo significa che solo per il 5% del tempo, il vincitore determinato non è in realtà la migliore esperienza tra tutte le esperienze nell&#39;attività. Per un [Test A/A](/help/main/c-activities/t-test-ab/aa-testing.md) (con esperienze identiche), [!DNL Target] conclude un test per meno del 5% del tempo. Il comportamento previsto per un test A/A (con esperienze identiche) è l&#39;esecuzione indefinita e quindi il badge del vincitore non dovrebbe mai apparire.

[!DNL Target] non utilizza l’affidabilità basata sul valore p per [!UICONTROL Allocazione automatica].

Il [!UICONTROL Affidabilità] colonna in un [!UICONTROL Allocazione automatica] L’attività (illustrata di seguito) mostra la probabilità che un’esperienza sia il vincitore entro l’1% di margine di errore. L’algoritmo utilizza un effetto rilevabile minimo dell’1% tra i tassi di conversione migliori e quelli del secondo migliore. L’algoritmo utilizza [Disuguaglianza di Bernstein](https://en.wikipedia.org/wiki/Bernstein_inequalities_%28probability_theory%29) per calcolare questa probabilità.

I test A/B normali calcolano l’affidabilità in base ai valori p. [!UICONTROL L&#39;Allocazione automatica non utilizza i valori p. ] I valori p calcolano “liberamente” la probabilità che una determinata esperienza sia diversa dal controllo. Questi valori p possono essere utilizzati solo per determinare se un’esperienza è diversa dal controllo. Questi valori non possono essere utilizzati per determinare se un&#39;esperienza è diversa da un&#39;altra esperienza (non controllo).

>[!IMPORTANT]
>
>[!DNL Target] mostra un vincitore dopo un numero minimo predefinito di conversioni; tuttavia, la decisione finale di scegliere il vincitore dovrebbe sempre essere sui risultati del [!DNL Adobe Target] Calcolatore dimensioni campione. [!DNL Target] non considera i tassi di conversione di base di un sito e altri aspetti importanti che vengono inseriti nel calcolatore per determinare la durata dell’attività. Di conseguenza, [!DNL Target] potrebbe visualizzare un vincitore prima di quanto giustificato in base a un numero minimo di conversioni. Per ulteriori informazioni, consulta [Calcolatore dimensioni campione](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6).

## Comprendere il reporting di incremento e affidabilità in [!UICONTROL Allocazione automatica] attività {#lift-confidence}

In entrata [!UICONTROL Allocazione automatica] attività, la prima esperienza (per impostazione predefinita denominata Esperienza A) è sempre definita come esperienza di &quot;controllo&quot; sulla [!UICONTROL Rapporti] scheda. Questa esperienza non viene trattata come un vero e proprio controllo statistico nella modellazione utilizzata per determinare le prestazioni delle esperienze, ma viene trattata come un riferimento o una base per alcune figure nel rapporto.

Il valore numerico di &quot;Incremento&quot; e i limiti del 95% per ogni esperienza vengono sempre calcolati in riferimento all’esperienza di &quot;Controllo&quot; definita. L&#39;esperienza &quot;Controllo&quot; definita non può avere un incremento relativo a se stessa, pertanto per questa esperienza viene segnalato un valore vuoto &quot;—&quot;. A differenza dei test A/B, in [!UICONTROL Allocazione automatica] test, se un&#39;esperienza ha risultati peggiori rispetto al controllo definito, non viene riportato un valore Lift negativo; viene invece visualizzato &quot;—&quot;.

Il visualizzato [!UICONTROL Intervallo di affidabilità] le barre rappresentano l’intervallo di affidabilità del 95% intorno alla stima media del tasso di conversione di un’esperienza. Queste barre sono inoltre codificate in base al colore in relazione all’esperienza &quot;Controllo&quot; definita. La barra dell’esperienza &quot;Controllo&quot; è sempre di colore grigio. Le parti degli intervalli di affidabilità al di sotto dell’intervallo di affidabilità dell’esperienza &quot;Controllo&quot; sono di colore rosso, mentre le parti degli intervalli di affidabilità al di sopra dell’esperienza &quot;Controllo&quot; sono di colore verde.

Un vincitore si trova quando l&#39;esperienza principale è al 95% [!UICONTROL Intervallo di affidabilità] non si sovrappone ad altre esperienze. L’esperienza vincente è indicata da un contrassegno a stella verde a sinistra del nome dell’esperienza e nel banner &quot;Vincitore&quot;. Quando non è visibile alcuna stella, sullo striscione si legge &quot;Ancora nessun vincitore&quot; e non è stato ancora trovato un vincitore.

Viene inoltre riportato un numero di &quot;affidabilità&quot; accanto all’esperienza attualmente leader o vincente. Questa figura viene riportata solo fino a quando l’esperienza principale non [!UICONTROL Affidabilità] raggiunge almeno il 60%. Se sono presenti due esperienze in [!UICONTROL Allocazione automatica] attività, questo numero rappresenta il livello di affidabilità delle prestazioni dell’esperienza rispetto all’altra esperienza. Se sono presenti più di due esperienze nel [!UICONTROL Allocazione automatica] attività, questo numero rappresenta il livello di affidabilità che l’esperienza sta ottenendo meglio rispetto all’esperienza di &quot;controllo&quot; definita. Se l’esperienza &quot;Controllo&quot; sta vincendo, non viene segnalato alcun valore &quot;Affidabilità&quot;.

## Domande frequenti {#section_C8E068512A93458D8C006760B1C0B6A2}

Considera le seguenti risposte alle domande frequenti:

### L’attività è in corso da un paio di giorni. Perché tutti i valori di affidabilità mostrano ancora 0%?

Nella colonna [!UICONTROL Affidabilità] del rapporto per tutte le attività viene visualizzato 0% per i seguenti motivi:

* test A/B manuali e [!UICONTROL Allocazione automatica] utilizzare statistiche diverse per la visualizzazione [!UICONTROL Affidabilità] valori.

  I test A/B manuali utilizzano valori p basati su [Test t di Welch](https://en.wikipedia.org/wiki/Welch%27s_t-test). Un valore p rappresenta la probabilità di trovare la differenza osservata (o una differenza maggiore) tra un’esperienza e il controllo, dato che in realtà non esiste una differenza simile. Questi valori p possono essere utilizzati solo per determinare se i dati osservati sono coerenti quando un’esperienza specifica e il controllo sono uguali. Questi valori non possono essere utilizzati per determinare se un&#39;esperienza è diversa da un&#39;altra esperienza (non controllo).

  [!UICONTROL Allocazione automatica] mostra la probabilità che una determinata esperienza sia un vero vincitore in tutte le esperienze dell’attività. Solo un’esperienza vincente (che è più probabile che sia il vincitore) ha un valore di affidabilità diverso da zero. Tutti gli altri elementi hanno maggiori probabilità di essere perdenti e visualizzano lo 0%.

* [!UICONTROL L&#39;allocazione automatica inizia a mostrare un valore di affidabilità solo dopo che l&#39;esperienza vincente avrà raccolto il 60% di affidabilità. ] Questi livelli di affidabilità vengono generalmente visualizzati in circa la metà del tempo necessario per il completamento di un normale test A/B (anche se questo intervallo di tempo non è garantito). Per determinare per quanto tempo deve essere eseguito un normale test A/B, utilizza [!DNL Adobe Target] [Calcolatore dimensioni campione](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6): inserisci il tasso di conversione del controllo in &quot;Tasso di conversione di base&quot;, &quot;5%&quot; per &quot;Incremento&quot; e 95% per &quot;Affidabilità&quot;. In genere, i valori di affidabilità iniziano a comparire dopo che ogni esperienza ha accumulato almeno il 50% dei campioni richiesti per esperienza. Questo ti dà un’idea di quando inizia a comparire la fiducia.

* Se il rapporto presenta 0% per tutte le esperienze, è probabile che sia ancora troppo presto nel corso dell’attività.

### Sono disponibili i badge (distintivi) “No Winner”, “Winner” e “star” per le attività di [!UICONTROL Allocazione automatica] che utilizzano [!UICONTROL Analytics come origine di reporting] (A4T)?

I badge &quot;Ancora nessun vincitore&quot; e &quot;Vincitore&quot; non sono attualmente disponibili nel [!UICONTROL A4T] pannello in [!DNL Analysis Workspace]. Questi badge non sono disponibili neanche se lo stesso rapporto viene visualizzato in [!DNL Target]. Un badge vincitore &quot;stella&quot; mostrato in una [!DNL Target] rapporto per un [!UICONTROL Allocazione automatica] L’attività che utilizza A4T deve essere ignorata.

Per ulteriori informazioni su questa e altre limitazioni e note, consulta [Allocazione automatica](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md#aa) in *Supporto A4T per [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico] attività*.


