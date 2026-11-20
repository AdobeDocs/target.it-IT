---
keywords: allocazione automatica del traffico;targeting;vincitore;garanzia statistica;affidabilità;determinare vincitore;incremento;affidabilità;impostazione predefinita;esperienza predefinita;allocazione automatica;allocazione automatica
description: Scopri come interpretare i risultati delle attività A/B di [!UICONTROL Allocazione automatica], concentrandoti su indicatori chiave come incremento e affidabilità.
title: Come posso interpretare [!UICONTROL i report Allocazione automatica]?
feature: Auto-Allocate
exl-id: 4ed00eee-8939-4958-9be6-b45a8c08afbc
TQID: 'https://experienceleague.adobe.com/o4mFGMk-M5QUvJ57kYnfjMPvVZL8l6YegJQSJyHjAxc'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: f2d0aafb-18af-41a0-a32e-2788eafacc2b
    internal-label: Auto-allocate
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 7eede3484d524e87127de9147aa786484fc87c7d
workflow-type: tm+mt
source-wordcount: '1357'
ht-degree: 3%
---
# Interpreta [!UICONTROL Allocazione automatica] report {#interpret-auto-allocate-reports}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come identificare l&#39;esperienza vincente di un&#39;attività **[!UICONTROL Allocazione automatica]**, che garantisce a livello statistico la disponibilità di **[!UICONTROL Allocazione automatica]**, e come leggere i dati relativi all&#39;incremento e all&#39;affidabilità nel rapporto.

>[!ENDSHADEBOX]

Il report di un&#39;attività A/B di **[!UICONTROL Allocazione automatica]** in [!DNL Adobe Target] mostra se l&#39;attività ha trovato un vincitore e quanto [!DNL Target] sia sicuro in tale risultato. Indicatori come il badge vincitore, l’incremento e l’affidabilità ti aiutano a interpretare i risultati.

Molti esperti di marketing commettono l’errore di dichiarare un’esperienza vincente prima che i risultati indichino chiaramente quale sia l’esperienza migliore. [!DNL Target] facilita la determinazione del vincitore. Per informazioni generali sulla dichiarazione di un vincitore, consulta [Dieci insidie frequenti per i test A/B e come evitarle](/help/main/c-activities/t-test-ab/common-ab-testing-pitfalls.md).

## Identificare l’esperienza vincente {#identify-winner}

Quando utilizzi la funzione **[!UICONTROL Allocazione automatica]**, [!DNL Target] visualizza un badge nella parte superiore della pagina dell&#39;attività. Il badge indica &quot;Ancora nessun vincitore&quot; finché l’attività non raggiunge il numero minimo di conversioni con sufficiente affidabilità.

![Indicatore Nessun vincitore](/help/main/c-activities/automated-traffic-allocation/assets/no-winner-new.png)

Quando viene dichiarata l&#39;esperienza migliore, [!DNL Target] visualizza il badge &quot;Vincitore: esperienza *X*&quot;.

![Badge vincitore](/help/main/c-activities/automated-traffic-allocation/assets/winner-new.png)

Il badge vincitore viene visualizzato anche nel pop-up di informazioni di un&#39;attività nell&#39;elenco **[!UICONTROL Attività]**, in modo da visualizzare lo stato di un&#39;attività **[!UICONTROL Allocazione automatica]** senza aprirla.

>[!NOTE]
>
>Le attività **[!UICONTROL Allocazione automatica]** sono progettate per trovare la migliore esperienza tra tutte le opzioni, non solo per effettuare confronti in coppia con il controllo.

## Garanzie statistiche di [!UICONTROL Allocazione automatica] {#statistical-guarantees}

Al termine di un&#39;attività A/B, **[!UICONTROL Allocazione automatica]** garantisce che il vincitore determinato abbia un tasso di falso positivo effettivo del 5%. Questo significa che solo per il 5% del tempo, il vincitore determinato non è in realtà la migliore esperienza tra tutte le esperienze nell&#39;attività.

Per un test [A/A](/help/main/c-activities/t-test-ab/aa-testing.md) (con esperienze identiche), [!DNL Target] conclude un test per meno del 5% del tempo. Il comportamento previsto per un test A/A deve essere eseguito a tempo indefinito, pertanto il badge del vincitore non dovrebbe mai essere visualizzato.

### Affidabilità e valori p {#confidence-p-values}

[!DNL Target] non utilizza l&#39;affidabilità basata sul valore p per **[!UICONTROL Allocazione automatica]**. La colonna **[!UICONTROL Affidabilità]** in un&#39;attività **[!UICONTROL Allocazione automatica]** mostra la probabilità che un&#39;esperienza sia il vincitore entro un margine di errore dell&#39;1%. L&#39;algoritmo utilizza un effetto rilevabile minimo dell&#39;1% tra il tasso di conversione migliore e il secondo migliore e utilizza la [disuguaglianza di Bernstein](https://en.wikipedia.org/wiki/Bernstein_inequalities_%28probability_theory%29) per calcolare questa probabilità.

I test A/B normali calcolano l’affidabilità in base ai valori p, che calcolano &quot;liberamente&quot; la probabilità che una determinata esperienza sia diversa dal controllo. Questi valori p possono essere utilizzati solo per determinare se un’esperienza è diversa dal controllo. Non possono essere utilizzati per determinare se un’esperienza è diversa da un’altra esperienza (non il controllo).

>[!IMPORTANT]
>
>[!DNL Target] mostra un vincitore dopo un numero minimo predefinito di conversioni. Tuttavia, la decisione finale di scegliere il vincitore deve sempre essere basata sui risultati del calcolatore delle dimensioni del campione [!DNL Adobe Target]. [!DNL Target] non considera i tassi di conversione di base di un sito e altri aspetti importanti inseriti nel calcolatore per determinare la durata dell&#39;attività. Di conseguenza, [!DNL Target] potrebbe visualizzare un vincitore prima di quanto richiesto in base a un numero minimo di conversioni. Per ulteriori informazioni, vedere [Calcolatore dimensioni campione](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6).

## Rapporti relativi all’incremento e all’affidabilità {#lift-confidence}

La scheda **[!UICONTROL Rapporti]** di un&#39;attività **[!UICONTROL Allocazione automatica]** mostra le cifre seguenti:

| Figura | Descrizione |
|---|---|
| **Esperienza di controllo** | La prima esperienza (denominata Esperienza A per impostazione predefinita) è sempre definita come esperienza di &quot;controllo&quot; nella scheda **[!UICONTROL Rapporti]**. Questa esperienza non viene trattata come un vero e proprio controllo statistico nella modellazione utilizzata per determinare le prestazioni delle esperienze, ma viene trattata come un riferimento o una base per alcune figure nel rapporto. |
| **Incremento** | Il valore di &quot;Incremento&quot; e i limiti del 95% di ogni esperienza vengono sempre calcolati in riferimento all’esperienza di &quot;Controllo&quot; definita. L&#39;esperienza &quot;Controllo&quot; non può avere un incremento relativo a se stessa, pertanto il rapporto mostra un valore &quot;—&quot; vuoto per questa esperienza.<br>A differenza dei test A/B, nei test **[!UICONTROL Allocazione automatica]**, se un&#39;esperienza ha prestazioni peggiori del controllo definito, non viene segnalato un valore di incremento negativo. Viene invece visualizzato &quot;—&quot;. |
| **Intervalli di affidabilità** | Le barre **[!UICONTROL Intervallo di affidabilità]** visualizzate rappresentano l&#39;intervallo di affidabilità del 95% intorno alla stima media del tasso di conversione di un&#39;esperienza. Le barre sono codificate in base al colore in base all’esperienza &quot;Controllo&quot; definita:<ul><li>La barra dell’esperienza &quot;Controllo&quot; è sempre grigia.</li><li>Le porzioni di intervalli di confidenza al di sotto dell’intervallo di confidenza dell’esperienza &quot;Controllo&quot; sono rosse.</li><li>Le porzioni di intervalli di affidabilità al di sopra dell’intervallo di affidabilità dell’esperienza &quot;Controllo&quot; sono verdi.</li></ul> |
| **Vincitore** | Un vincitore viene trovato quando l&#39;intervallo di affidabilità **[!UICONTROL del 95%]** dell&#39;esperienza principale non si sovrappone ad altre esperienze. L’esperienza vincente è indicata da un contrassegno a stella verde a sinistra del nome dell’esperienza e nel banner &quot;Vincitore&quot;. Quando non è visibile alcuna stella, sullo striscione si legge &quot;Ancora nessun vincitore&quot; e non è stato ancora trovato un vincitore. |
| **Numero di affidabilità** | Viene inoltre riportato un numero di &quot;affidabilità&quot; accanto all’esperienza attualmente leader o vincente. Questa cifra viene segnalata solo finché l&#39;**[!UICONTROL affidabilità]** dell&#39;esperienza principale non raggiunge almeno il 60%.<ul><li>Se nell&#39;attività **[!UICONTROL Allocazione automatica]** sono presenti due esperienze, il numero rappresenta il livello di affidabilità con cui l&#39;esperienza sta ottenendo risultati migliori rispetto all&#39;altra.</li><li>Se sono presenti più di due esperienze, il numero rappresenta il livello di affidabilità con cui le prestazioni dell’esperienza sono migliori rispetto all’esperienza di &quot;controllo&quot; definita.</li><li>Se l’esperienza &quot;Controllo&quot; sta vincendo, non viene segnalato alcun valore &quot;Affidabilità&quot;.</li></ul> |

## Domande frequenti {#faq}

Considera le seguenti risposte alle domande frequenti.

+++ Sono passati alcuni giorni dall’inizio dell’attività. Perché tutti i valori di affidabilità mostrano ancora lo 0%?

Uno dei seguenti motivi descrive il motivo per cui lo 0% viene visualizzato nella colonna **[!UICONTROL Affidabilità]** del rapporto per tutte le esperienze:

* I test A/B manuali e **[!UICONTROL Allocazione automatica]** utilizzano statistiche diverse per visualizzare i valori di **[!UICONTROL Affidabilità]**.

  I test A/B manuali utilizzano valori p basati sul test t di [Welch](https://en.wikipedia.org/wiki/Welch%27s_t-test). Un valore p è la probabilità di trovare la differenza osservata (o una differenza più estrema) tra un’esperienza e il controllo, dato che in realtà non esiste una differenza di questo tipo. Questi valori p possono essere utilizzati solo per determinare se i dati osservati sono coerenti con una determinata esperienza e se il controllo è lo stesso. Non possono essere utilizzati per determinare se un’esperienza è diversa da un’altra esperienza (non il controllo).

  **[!UICONTROL Allocazione automatica]** mostra la probabilità che una determinata esperienza sia un vero vincitore in tutte le esperienze dell&#39;attività. Solo un’esperienza vincente (che è più probabile che sia il vincitore) ha un valore di affidabilità diverso da zero. Tutti gli altri elementi hanno maggiori probabilità di essere perdenti e visualizzano lo 0%.

* **[!UICONTROL L&#39;allocazione automatica]** inizia a mostrare un valore di affidabilità solo dopo che l&#39;esperienza vincente avrà raccolto il 60% di affidabilità. Questi livelli di affidabilità vengono generalmente visualizzati in circa la metà del tempo necessario per il completamento di un normale test A/B (anche se questo intervallo di tempo non è garantito). Per determinare la durata di un normale test A/B, utilizzare il [!DNL Adobe Target] [Calcolatore dimensioni campione](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6): immettere il tasso di conversione del controllo in &quot;Tasso di conversione di base&quot;, &quot;5%&quot; per &quot;Incremento&quot; e 95% per &quot;Affidabilità&quot;. In genere, l’affidabilità inizia a comparire dopo che ogni esperienza ha accumulato almeno il 50% dei campioni richiesti per esperienza. Questo ti dà un’idea di quando inizia a comparire la fiducia.

* Se il rapporto mostra lo 0% in generale, è probabile che sia troppo presto per iniziare l’attività.

+++

+++ Sono disponibili i badge &quot;No Winner&quot;, &quot;Winner&quot; e &quot;star&quot; per le attività [!UICONTROL Allocazione automatica] che utilizzano [!UICONTROL Analytics] come origine per la generazione di rapporti (A4T)?

I badge &quot;Ancora nessun vincitore&quot; e &quot;Vincitore&quot; vengono visualizzati nella finestra a comparsa delle informazioni sull&#39;attività nell&#39;elenco **[!UICONTROL Attività]**. Non vengono visualizzati nel pannello **[!UICONTROL A4T]** in [!DNL Analysis Workspace] o quando visualizzi lo stesso rapporto in [!DNL Target]. Se un report [!DNL Target] per un&#39;attività A4T **[!UICONTROL Allocazione automatica]** mostra un badge vincitore, ignoralo.

Per ulteriori informazioni su questa e altre limitazioni e note, consulta [Allocazione automatica](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md#aa) in *Supporto A4T per [!UICONTROL Attività di allocazione automatica] e [!UICONTROL Attività di targeting automatico]*.

+++
