---
keywords: AB;A/B;AB..n;confrontare esperienze;targeting;confrontare contenuti;targeting automatico;allocazione automatica
description: Scopri i diversi tipi di attività di test A/B in Adobe [!DNL Target] - Manuale, Allocazione automatica e Targeting automatico. Scegli quello che è giusto per te.
title: Quale tipo di attività A/B è disponibile in Target?
feature: Test A/B
exl-id: e8ff8994-a0a9-4fc7-8fcb-e3a1b7697604
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 38%

---

# Panoramica del test A/B

Un&#39;attività manuale [!UICONTROL A/B Test] confronta due o più versioni del contenuto del sito web per vedere quale versione migliora maggiormente le conversioni durante un periodo di test pre-specificato.

>[!NOTE]
>
>Oltre all&#39;attività Manuale (Predefinito) [!UICONTROL Test A/B] (discussa in questa sezione), [!DNL Target] fornisce due tipi aggiuntivi di attività [!UICONTROL Test A/B]: [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico].
>
>Per ulteriori informazioni, consulta [Tipi di attività di test A/B](#types) di seguito.

Un&#39;attività manuale [!UICONTROL Test A/B] (a volte indicata come test A/B...N) confronta due o più versioni del contenuto del sito Web per vedere quale incrementa al meglio le conversioni, le vendite o altre metriche identificate. Un test A/B permette di confrontare le modifiche apportate alla pagina rispetto alla struttura di pagina predefinita, per determinare quale esperienza produce i risultati migliori.

I test A/B manuali sono particolarmente utili quando si dispone di un’ipotesi chiara su come migliorare le prestazioni della pagina in base a metriche di successo o a contenuti alternativi.

I test A/B manuali sono particolarmente adatti per modifiche di grandi dimensioni che potrebbero richiedere nuovi layout o un trattamento nettamente diverso degli elementi. Se la progettazione del test non si suddivide facilmente in singoli elementi di pagina, è necessario eseguire un test A/B prima di un [test multivariato](/help/c-activities/c-multivariate-testing/multivariate-testing.md).

Quando imposti il test A/B, puoi determinare la percentuale di visitatori che visualizzano ogni esperienza. Ad esempio, è possibile suddividere il traffico in modo uniforme tra il controllo e una seconda esperienza, oppure è possibile testare un&#39;esperienza nuova e più rischiosa mostrandola a solo il 5% del pubblico.

>[!NOTE]
>
>Per informazioni dettagliate sulla determinazione delle dimensioni ottimali del campione per un test A/B, consulta [Pianificare il test A/B](/help/c-activities/t-test-ab/sample-size-determination.md).

Quando il numero di esperienze diverse supera le cinque e si estende su due o più posizioni, è consigliabile considerare un [test MVT](/help/c-activities/c-multivariate-testing/multivariate-testing.md) prima di eseguire i test A/B. I test multivariati mostrano quali aree della pagina hanno più probabilità di migliorare la conversione. Queste posizioni sono quelle sulle quali un addetto al marketing dovrebbe concentrarsi. Ad esempio, il test MVT potrebbe indicare che l&#39;invito all&#39;azione è la posizione più importante per soddisfare gli obiettivi. Una volta determinati le posizioni e il contenuto più utili per raggiungere gli obiettivi, puoi eseguire un test A/B per perfezionare ulteriormente i risultati, ad esempio per sottoporre a test reciproco due immagini specifiche, o per confrontare il testo o i colori di un invito all’azione. Facendo seguire un test MVT da uno o più test A/B, puoi determinare il contenuto migliore possibile per i risultati desiderati.

## Tipi di attività di test A/B {#types}

Oltre all&#39;attività manuale [!UICONTROL Test A/B] (descritta in questa sezione), [!DNL Target] fornisce due tipi aggiuntivi di attività di test A/B: [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico].

| Tipo di attività | Descrizione |
| --- | --- |
| [!UICONTROL Test A/B manuale] | Confronta due o più esperienze per vedere quale migliora in modo più efficace le conversioni durante un periodo di test pre-specificato. <br>Questa sezione descrive come impostare un’attività  [!UICONTROL A/B ] Test manuale, ma i passaggi per gli altri tipi di attività  [!UICONTROL A/B ] Test sono simili. |
| [!UICONTROL Allocazione automatica] | Identifica un vincitore tra due o più esperienze, e reindirizza il traffico verso il vincitore, aumentando la conversione mentre il test continua a essere eseguito e ad apprendere. <br>Per informazioni sui vantaggi dell’utilizzo di un’attività di allocazione automatica, consulta  [Allocazione automatica ](/help/c-activities/t-test-ab/sample-size-determination.md#auto-allocate) in  *Per quanto tempo si deve eseguire una* panoramica Test A/B e Allocazione  [automatica](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md). |
| ![Badge Premium ](/help/assets/premium.png) [!UICONTROL Targeting automatico] | Utilizza l’apprendimento automatico avanzato per personalizzare i contenuti e favorire le conversioni individuando più esperienze ad alte prestazioni definite dall’addetto al marketing. Inoltre, indica l’esperienza più adatta per ogni visitatore in base al suo profilo cliente individuale e al comportamento dei visitatori precedenti con profili simili. <br>Per ulteriori informazioni, consulta  [Targeting automatico](/help/c-activities/auto-target/auto-target-to-optimize.md). |

Per ulteriori informazioni su quali di queste attività [!UICONTROL A/B Test] sono adatte alle tue esigenze, consulta la Guida interattiva alle attività di [Adobe Target Activities Guide PDF](/help/c-activities/target-activities-guide.md).

I passaggi per la creazione dei tre tipi di attività [!UICONTROL A/B Test] sono simili. Per creare un&#39;attività di [!UICONTROL Allocazione automatica] o [!UICONTROL Targeting automatico], inizia creando un&#39;attività di test A/B](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md), ma quando si accede alla pagina [!UICONTROL Targeting], scegli il metodo di allocazione del traffico desiderato, come illustrato di seguito:[

* [!UICONTROL Allocazione automatica all’esperienza migliore]
* [!UICONTROL Targeting automatico per esperienza personalizzata]

![Impostazioni del metodo di allocazione del traffico](/help/c-activities/t-test-ab/t-test-create-ab/assets/traffic-allocation-method.png)

## Video di formazione: Tipi di attività (9:03) ![Badge panoramica](/help/assets/overview.png)

Questo video spiega i tipi di attività disponibili in [!DNL Target Standard/Premium].

* Descrizione dei tipi di attività inclusi in [!DNL Adobe Target]
* Selezionare il tipo di attività appropriato per i tuoi obiettivi
* Descrizione del flusso di lavoro guidato in tre passaggi da applicare a tutti i tipi di attività

>[!VIDEO](https://video.tv.adobe.com/v/17386)
