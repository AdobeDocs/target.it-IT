---
keywords: automated traffic allocation;targeting;winner;statistical guarantee;confidence;determine winner;lift;confidence;default;default experience
description: Determinate un vincitore in un'attività di allocazione automatica A/B visualizzando gli indicatori nell'interfaccia  di Adobe Target.
title: Determinare un vincitore
feature: auto-allocate
translation-type: tm+mt
source-git-commit: c2769c0fcf7a05c10405ec855468c829aca785c0
workflow-type: tm+mt
source-wordcount: '1110'
ht-degree: 48%

---


# Interpretare i rapporti di allocazione automatica {#determine-a-winner}

Interpretate i risultati di un&#39;attività di allocazione automatica A/B esaminando indicatori importanti, inclusi incrementi e confidenza, nell&#39;interfaccia di Target.

Molti addetti al marketing commettono l’errore di dichiarare un’esperienza vincente prima che i risultati indichino chiaramente quale sia l’esperienza migliore. Ora abbiamo reso più facile determinare il vincitore.

>[!NOTE]
>
>Per informazioni generali sulla dichiarazione di un vincitore, vedere [Dieci comuni errori di test A/B e come evitarli](/help/c-activities/t-test-ab/common-ab-testing-pitfalls.md).

## Identificare l&#39;esperienza vincente {#section_24007470CF5B4D30A06610CE8DD23CE3}

Quando utilizzi la funzione di [!UICONTROL Allocazione automatica], [!DNL Target] mostra un badge nella parte superiore della pagina dell&#39;attività che indica “Ancora nessun vincitore” finché l&#39;attività non raggiunge il numero minimo di conversioni con sufficiente affidabilità.

![Indicatore Nessun vincitore](/help/c-activities/automated-traffic-allocation/assets/no-winner.png)

Quando viene dichiarata l&#39;esperienza migliore, in [!DNL Target] appare la scritta “Vincitore: esperienza X”.

![](assets/winner.png)

>[!NOTE]
>
>Le attività di Allocazione automatica sono progettate per trovare la migliore esperienza tra tutte le opzioni e non solo per fare confronti in coppia con il controllo.

## Garanzie statistiche di allocazione automatica {#section_7AF3B93E90BA4B80BC9FC4783B6A389C}

Al termine di un&#39;attività A/B, Allocazione automatica garantisce che il vincitore determinato abbia un tasso di falso positivo efficace del 5%. Questo significa che solo per il 5% del tempo, il vincitore determinato non è in realtà la migliore esperienza tra tutte le esperienze nell&#39;attività. Per un test A/A (con esperienze identiche), concludiamo un test inferiore al 5% del tempo. Il comportamento previsto per un test A/A (con esperienze identiche) è l&#39;esecuzione indefinita e quindi il badge del vincitore non dovrebbe mai apparire.

Non utilizziamo l’affidabilità basata sul valore p per l&#39;Allocazione automatica.

La colonna Affidabilità in un&#39;attività di Allocazione automatica (illustrata di seguito) visualizza la probabilità che un&#39;esperienza sia il vincitore entro l&#39;1% di margine di errore (cioè l&#39;algoritmo utilizza un effetto minimo rilevabile dell&#39;1% tra il tasso di conversione migliore e il secondo migliore). L&#39;algoritmo utilizza la [disuguaglianza di Bernstein](https://en.wikipedia.org/wiki/Bernstein_inequalities_(probability_theory)) per calcolare questa probabilità.

I test A/B normali calcolano l’affidabilità in base ai valori p. L&#39;Allocazione automatica non utilizza i valori p. I valori p calcolano “liberamente” la probabilità che una determinata esperienza sia diversa dal controllo. Questi valori p possono essere utilizzati solo per determinare se un’esperienza è diversa dal controllo. Questi valori non possono essere utilizzati per determinare se un&#39;esperienza è diversa da un&#39;altra esperienza (non controllo).

>[!IMPORTANT]
>
>Target mostra un vincitore dopo un numero minimo predefinito di conversioni; tuttavia, la decisione finale di scegliere il vincitore dovrebbe sempre essere sui risultati del  Adobe Target [calcolatore dimensioni campione](https://docs.adobe.com/content/target-microsite/testcalculator.html). In Target non vengono considerati i tassi di conversione di base di un sito e altri aspetti importanti inseriti nel calcolatore per determinare la durata dell&#39;attività. Di conseguenza, Target potrebbe visualizzare un vincitore prima del previsto sulla base di un numero minimo di conversioni. Per ulteriori informazioni, vedere [Calcolatore dimensioni campione](/help/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6).

## Comprendere i rapporti Lift and Confidence nelle attività Auto Allocate {#lift-confidence}

Nelle attività di allocazione automatica, la prima esperienza (per impostazione predefinita denominata Esperienza A) è sempre definita come esperienza di &quot;controllo&quot; nella scheda Rapporti. Questa esperienza non viene trattata come un vero controllo statistico nella modellazione utilizzata per determinare le prestazioni delle esperienze, ma viene trattata come riferimento o previsione per alcune figure del rapporto.

Il valore numerico &quot;Lift&quot; e i limiti del 95% per ogni esperienza vengono sempre calcolati con riferimento all&#39;esperienza &quot;Control&quot; definita. L&#39;esperienza &quot;Control&quot; definita non può avere un incremento relativo a se stessa, pertanto per questa esperienza viene segnalato un valore &quot;—&quot; vuoto. A differenza dei test A/B, nei test di allocazione automatica, se un&#39;esperienza ha prestazioni peggiori del controllo definito, non viene riportato un valore di incremento negativo; viene invece visualizzato &quot;—&quot;.

Le barre dell&#39;intervallo di confidenza visualizzato rappresentano l&#39;intervallo di confidenza del 95% intorno alla stima media del tasso di conversione di un&#39;esperienza. Sono anche codificati in base al colore rispetto all&#39;esperienza &quot;Control&quot; definita. La barra dell&#39;esperienza &quot;Control&quot; è sempre di colore grigio. Le porzioni di intervalli di confidenza al di sotto dell&#39;intervallo di confidenza dell&#39;esperienza &quot;Control&quot; sono colorate di rosso e le porzioni di intervalli di confidenza al di sopra dell&#39;esperienza &quot;Control&quot; sono colorate di verde.

Un vincitore si trova quando l&#39;intervallo di confidenza del 95% dell&#39;esperienza principale non si sovrappone ad altre esperienze. L&#39;esperienza vincente viene designata con un contrassegno a stella verde a sinistra del nome dell&#39;esperienza e nel banner &quot;Vincitore&quot;. Quando nessuna stella è visibile, il banner recita &quot;No Winner yet&quot; (Nessun vincitore ancora) e il vincitore non è ancora stato trovato.

Un numero &quot;Confidence&quot; viene riportato anche accanto all&#39;esperienza attualmente leader o vincente. Questa cifra viene riportata solo fino a quando la confidenza dell&#39;esperienza principale non raggiunge almeno il 60%. Se esattamente due esperienze sono presenti nell&#39;esperimento Allocazione automatica, questo numero rappresenta il livello di confidenza con cui l&#39;esperienza ha prestazioni migliori rispetto all&#39;altra esperienza. Se nell&#39;esperimento Auto-Allocate sono presenti più di due esperienze, questo numero rappresenta il livello di confidenza con cui l&#39;esperienza viene eseguita meglio dell&#39;esperienza &quot;Control&quot; definita. Se l&#39;esperienza &quot;Control&quot; è vincente, non viene segnalata alcuna figura &quot;Confidence&quot;.

## Domande frequenti {#section_C8E068512A93458D8C006760B1C0B6A2}

**L’attività è in corso da un paio di giorni. Perché tutti i valori di affidabilità mostrano ancora 0%?**

Nella colonna [!UICONTROL Affidabilità] del rapporto per tutte le attività viene visualizzato 0% per i seguenti motivi:

* I test A/B manuali e l&#39;allocazione automatica utilizzano statistiche diverse per visualizzare i valori di affidabilità.

   I test A/B manuali utilizzano valori p basati sul [test t di Student](https://en.wikipedia.org/wiki/Student%27s_t-test). Un valore p rappresenta la probabilità di trovare la differenza osservata (o una differenza maggiore) tra un’esperienza e il controllo, dato che in realtà non esiste una differenza simile. Questi valori p possono essere utilizzati solo per determinare se i dati osservati sono coerenti quando un’esperienza specifica e il controllo sono uguali. Questi valori non possono essere utilizzati per determinare se un&#39;esperienza è diversa da un&#39;altra esperienza (non controllo).

   L&#39;allocazione automatica mostra la probabilità che una determinata esperienza sia un vero vincitore in tutte le esperienze dell&#39;attività. Questo significa che solo un&#39;esperienza vincente (che è più probabile che sia il vincitore), avrà un valore di affidabilità diverso da zero. Tutte le altre hanno più probabilità di essere perdenti e presentano il valore 0%.

* L&#39;allocazione automatica inizia a mostrare un valore di affidabilità solo dopo che l&#39;esperienza vincente avrà raccolto il 60% di affidabilità. Questi livelli di confidenza vengono generalmente visualizzati in circa la metà del tempo necessario per completare un normale test A/B (anche se questo non è garantito). Per determinare per quanto tempo dovrebbe durare un normale test A/B, utilizzare un [calcolatore delle dimensioni del campione](https://docs.adobe.com/content/target-microsite/testcalculator.html): il tasso di conversione del controllo plug in &quot;Tasso di conversione previsto&quot;, &quot;5%&quot; per &quot;Lift&quot; e &quot;95% per &quot;Confidence&quot;. In genere, i valori di affidabilità iniziano a comparire dopo che ogni esperienza ha accumulato almeno il 50% dei campioni richiesti per esperienza. Questo ti dà un&#39;idea di quando potrai iniziare a vedere valori di affidabilità.
* Se il rapporto presenta 0% per tutte le esperienze, è probabile che sia ancora troppo presto nel corso dell’attività.

