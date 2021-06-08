---
keywords: allocazione automatica del traffico;targeting;vincitore;garanzia statistica;affidabilità;determinare vincitore;incremento;affidabilità;impostazione predefinita;esperienza predefinita;allocazione automatica;allocazione automatica
description: Scopri come interpretare i risultati di un’attività di allocazione automatica A/B in Adobe [!DNL Target] esaminando importanti indicatori, tra cui incremento e affidabilità.
title: Come Interpreto I Rapporti Di Allocazione Automatica?
feature: Allocazione automatica
exl-id: 4ed00eee-8939-4958-9be6-b45a8c08afbc
source-git-commit: 4c696f55f56a116cff61c2c307f750e72cc0107c
workflow-type: tm+mt
source-wordcount: '1136'
ht-degree: 47%

---

# Interpretare i rapporti di allocazione automatica

Interpreta i risultati di un&#39;attività [!UICONTROL Allocazione automatica] A/B in [!UICONTROL Adobe Target] esaminando importanti indicatori, tra cui incremento e affidabilità.

Molti addetti al marketing commettono l’errore di dichiarare un’esperienza vincente prima che i risultati indichino chiaramente quale sia l’esperienza migliore. Ora abbiamo reso più facile determinare il vincitore.

>[!NOTE]
>
>Per informazioni generali sulla dichiarazione di un vincitore, consulta [Dieci insidie frequenti per i test A/B e come evitarle](/help/c-activities/t-test-ab/common-ab-testing-pitfalls.md).

## Identificare l’esperienza vincente {#section_24007470CF5B4D30A06610CE8DD23CE3}

Quando utilizzi la funzione di [!UICONTROL Allocazione automatica], [!DNL Target] mostra un badge nella parte superiore della pagina dell&#39;attività che indica “Ancora nessun vincitore” finché l&#39;attività non raggiunge il numero minimo di conversioni con sufficiente affidabilità.

![Indicatore Nessun vincitore](/help/c-activities/automated-traffic-allocation/assets/no-winner.png)

Quando viene dichiarata l&#39;esperienza migliore, in [!DNL Target] appare la scritta “Vincitore: esperienza X”.

![](assets/winner.png)

>[!NOTE]
>
>Le attività di Allocazione automatica sono progettate per trovare la migliore esperienza tra tutte le opzioni e non solo per fare confronti in coppia con il controllo.

## Garanzie statistiche di Allocazione automatica {#section_7AF3B93E90BA4B80BC9FC4783B6A389C}

Al termine di un&#39;attività A/B, Allocazione automatica garantisce che il vincitore determinato abbia un tasso di falso positivo efficace del 5%. Questo significa che solo per il 5% del tempo, il vincitore determinato non è in realtà la migliore esperienza tra tutte le esperienze nell&#39;attività. Per un test A/A (con esperienze identiche), concludiamo un test inferiore al 5% del tempo. Il comportamento previsto per un test A/A (con esperienze identiche) è l&#39;esecuzione indefinita e quindi il badge del vincitore non dovrebbe mai apparire.

Non utilizziamo l’affidabilità basata sul valore p per l&#39;Allocazione automatica.

La colonna Affidabilità in un&#39;attività di Allocazione automatica (illustrata di seguito) visualizza la probabilità che un&#39;esperienza sia il vincitore entro l&#39;1% di margine di errore (cioè l&#39;algoritmo utilizza un effetto minimo rilevabile dell&#39;1% tra il tasso di conversione migliore e il secondo migliore). L&#39;algoritmo utilizza la [disuguaglianza di Bernstein](https://en.wikipedia.org/wiki/Bernstein_inequalities_(probability_theory)) per calcolare questa probabilità.

I test A/B normali calcolano l’affidabilità in base ai valori p. L&#39;Allocazione automatica non utilizza i valori p. I valori p calcolano “liberamente” la probabilità che una determinata esperienza sia diversa dal controllo. Questi valori p possono essere utilizzati solo per determinare se un’esperienza è diversa dal controllo. Questi valori non possono essere utilizzati per determinare se un&#39;esperienza è diversa da un&#39;altra esperienza (non controllo).

>[!IMPORTANT]
>
>Target mostra un vincitore dopo un numero minimo predefinito di conversioni; tuttavia, la decisione finale di scegliere il vincitore dovrebbe sempre essere basata sui risultati del calcolatore delle dimensioni del campione Adobe Target [a1/>. ](https://experienceleague.adobe.com/tools/calculator/testcalculator.html) Target non considera i tassi di conversione di base di un sito e altri aspetti importanti inseriti nel calcolatore per determinare la durata dell’attività. Di conseguenza, Target potrebbe visualizzare un vincitore prima del previsto sulla base di un numero minimo di conversioni. Per ulteriori informazioni, consulta [Calcolatore dimensioni campione](/help/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6).

## Comprendere i rapporti Incremento e Affidabilità nelle attività di Allocazione automatica {#lift-confidence}

Nelle attività di allocazione automatica, la prima esperienza (per impostazione predefinita denominata Esperienza A) viene sempre definita come esperienza di controllo nella scheda Rapporti . Questa esperienza non viene trattata come un vero controllo statistico nella modellazione utilizzata per determinare le prestazioni delle esperienze, ma viene trattata come un riferimento o una linea di base per alcune figure nel rapporto.

Il valore numerico &quot;Incremento&quot; e i limiti del 95% per ogni esperienza vengono sempre calcolati con riferimento all’esperienza &quot;Controllo&quot; definita. L’esperienza definita &quot;Controllo&quot; non può avere un incremento relativo a se stessa, pertanto per questa esperienza viene riportato un valore &quot;—&quot; vuoto. A differenza dei test A/B, nei test di allocazione automatica, se un’esperienza funziona in modo peggiore del controllo definito, non viene riportato un valore di incremento negativo; viene invece visualizzato &quot;—&quot;.

Le barre dell’intervallo di affidabilità visualizzate rappresentano l’intervallo di affidabilità del 95% intorno alla stima media del tasso di conversione di un’esperienza. Questi vengono anche codificati in base al colore dell’esperienza definita di &quot;controllo&quot;. La barra dell’esperienza &quot;Controllo&quot; è sempre di colore grigio. Le parti degli intervalli di affidabilità al di sotto dell’intervallo di affidabilità dell’esperienza &quot;Controllo&quot; sono colorate di rosso e le parti degli intervalli di affidabilità al di sopra dell’esperienza &quot;Controllo&quot; sono colorate di verde.

Un vincitore si trova quando l’intervallo di affidabilità del 95% dell’esperienza principale non si sovrappone ad altre esperienze. L’esperienza vincente viene designata con un badge a stella verde a sinistra del nome dell’esperienza e nel banner &quot;Vincitore&quot;. Quando nessuna stella è visibile, lo striscione dice &quot;Ancora nessun vincitore&quot; e un vincitore non è ancora stato trovato.

Accanto all’esperienza attuale o vincente viene riportato anche un numero di &quot;Affidabilità&quot;. Questa cifra viene riportata solo fino a quando l’esperienza principale non raggiunge almeno il 60% di affidabilità. Se esattamente due esperienze sono presenti nell’esperimento di allocazione automatica, questo numero rappresenta il livello di affidabilità che l’esperienza sta ottenendo meglio rispetto all’altra esperienza. Se nell’esperimento di allocazione automatica sono presenti più di due esperienze, questo numero rappresenta il livello di affidabilità che l’esperienza sta ottenendo meglio dell’esperienza definita di controllo. Se l’esperienza &quot;Controllo&quot; è vincente, non viene segnalata alcuna figura di &quot;Affidabilità&quot;.

## Domande frequenti  {#section_C8E068512A93458D8C006760B1C0B6A2}

**L’attività è in corso da un paio di giorni. Perché tutti i valori di affidabilità mostrano ancora 0%?**

Nella colonna [!UICONTROL Affidabilità] del rapporto per tutte le attività viene visualizzato 0% per i seguenti motivi:

* I test A/B manuali e l&#39;allocazione automatica utilizzano statistiche diverse per visualizzare i valori di affidabilità.

   I test A/B manuali utilizzano valori p basati sul [test t di Student](https://en.wikipedia.org/wiki/Student%27s_t-test). Un valore p rappresenta la probabilità di trovare la differenza osservata (o una differenza maggiore) tra un’esperienza e il controllo, dato che in realtà non esiste una differenza simile. Questi valori p possono essere utilizzati solo per determinare se i dati osservati sono coerenti quando un’esperienza specifica e il controllo sono uguali. Questi valori non possono essere utilizzati per determinare se un&#39;esperienza è diversa da un&#39;altra esperienza (non controllo).

   L&#39;allocazione automatica mostra la probabilità che una determinata esperienza sia un vero vincitore in tutte le esperienze dell&#39;attività. Questo significa che solo un&#39;esperienza vincente (che è più probabile che sia il vincitore), avrà un valore di affidabilità diverso da zero. Tutte le altre hanno più probabilità di essere perdenti e presentano il valore 0%.

* L&#39;allocazione automatica inizia a mostrare un valore di affidabilità solo dopo che l&#39;esperienza vincente avrà raccolto il 60% di affidabilità. Questi livelli di affidabilità generalmente appaiono in circa la metà del tempo necessario per completare un normale test A/B (anche se questo non è garantito). Per determinare per quanto tempo deve essere eseguito un normale test A/B, utilizza un [calcolatore delle dimensioni del campione](https://experienceleague.adobe.com/tools/calculator/testcalculator.html): il tasso di conversione del controllo plug in &quot;Tasso di conversione di base&quot;, &quot;5%&quot; per &quot;Incremento&quot; e 95% per &quot;Affidabilità&quot;. In genere, i valori di affidabilità iniziano a comparire dopo che ogni esperienza ha accumulato almeno il 50% dei campioni richiesti per esperienza. Questo ti dà un&#39;idea di quando potrai iniziare a vedere valori di affidabilità.
* Se il rapporto presenta 0% per tutte le esperienze, è probabile che sia ancora troppo presto nel corso dell’attività.
