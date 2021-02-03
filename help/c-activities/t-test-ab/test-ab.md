---
keywords: AB;A/B;AB..n;confrontare esperienze;Targeting;confrontare contenuto;auto-target;auto-allocazione
description: Un'attività di test A/B manuale mette a confronto due o più versioni del contenuto del sito Web per vedere quale versione migliora maggiormente le conversioni durante un periodo di test preimpostato.
title: Panoramica dei test A/B
feature: A/B Tests
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 38%

---


# Panoramica del test A/B

Un&#39;attività manuale [!UICONTROL A/B Test] mette a confronto due o più versioni del contenuto del sito Web per vedere quale versione migliora maggiormente le conversioni durante un periodo di test preimpostato.

>[!NOTE]
>
>Oltre all&#39;attività Manuale (Predefinito) [!UICONTROL A/B Test] (descritta in questa sezione), [!DNL Target] fornisce due tipi aggiuntivi di attività [!UICONTROL A/B Test]: [!UICONTROL Allocazione automatica] e [!UICONTROL Auto-Target].
>
>Per ulteriori informazioni, vedere [Tipi di attività di test A/B](#types) di seguito.

Un&#39;attività manuale [!UICONTROL A/B Test] (a volte denominata test A/B...N) mette a confronto due o più versioni del contenuto del sito Web per vedere quale incrementa maggiormente le conversioni, le vendite o altre metriche identificate. Un test A/B permette di confrontare le modifiche apportate alla pagina rispetto alla struttura di pagina predefinita, per determinare quale esperienza produce i risultati migliori.

I test A/B manuali sono particolarmente utili quando si dispone di un&#39;ipotesi chiara su come migliorare le prestazioni della pagina in base a metriche di successo o alla distribuzione alternativa dei contenuti.

I test A/B manuali sono particolarmente adatti per modifiche di grandi dimensioni che potrebbero comportare nuovi layout o trattamenti drasticamente diversi degli elementi. Se la progettazione del test non può essere facilmente suddivisa in singoli elementi di pagina, è necessario eseguire un test A/B prima di un [test multivariato](/help/c-activities/c-multivariate-testing/multivariate-testing.md).

Quando configurate il test A/B, potete determinare la percentuale di visitatori che visualizzano ogni esperienza. Ad esempio, è possibile suddividere il traffico in modo uniforme tra il controllo e una seconda esperienza, oppure è possibile testare un&#39;esperienza nuova e più rischiosa mostrandola a solo il 5% del pubblico.

>[!NOTE]
>
>Per informazioni dettagliate sulla determinazione delle dimensioni ottimali del campione per un test A/B, consulta [Pianificare il test A/B](/help/c-activities/t-test-ab/sample-size-determination.md).

Quando il numero di esperienze diverse supera le cinque e si estende su due o più posizioni, è consigliabile considerare un [test MVT](/help/c-activities/c-multivariate-testing/multivariate-testing.md) prima di eseguire i test A/B. I test multivariati mostrano quali aree della pagina hanno più probabilità di migliorare la conversione. Queste posizioni sono quelle sulle quali un addetto al marketing dovrebbe concentrarsi. Ad esempio, il test MVT potrebbe indicare che l&#39;invito all&#39;azione è la posizione più importante per soddisfare gli obiettivi. Una volta determinate le posizioni e il contenuto più utili per raggiungere gli obiettivi, potete eseguire un test A/B per perfezionare ulteriormente i risultati, ad esempio per sottoporre a test reciproco due immagini specifiche, o per confrontare il testo o i colori di un invito all&#39;azione. Facendo seguire un test MVT da uno o più test A/B, puoi determinare il contenuto migliore possibile per i risultati desiderati.

## Tipi di attività di test A/B {#types}

Oltre all&#39;attività manuale [!UICONTROL A/B Test] (descritta in questa sezione), [!DNL Target] fornisce due tipi aggiuntivi di attività di test A/B: [!UICONTROL Allocazione automatica] e [!UICONTROL Auto-Target].

| Tipo di attività | Descrizione |
| --- | --- |
| [!UICONTROL Test A/B manuale] | Confronta due o più esperienze per vedere quale migliora in modo più efficace le conversioni durante un periodo di test pre-specificato. <br>In questa sezione viene illustrato come impostare un&#39;attività  [!UICONTROL A/B ] testactivity manuale, ma i passaggi per gli altri tipi di attività  [!UICONTROL A/B ] Test sono simili. |
| [!UICONTROL Allocazione automatica] | Identifica un vincitore tra due o più esperienze, e reindirizza il traffico verso il vincitore, aumentando la conversione mentre il test continua a essere eseguito e ad apprendere. <br>Per informazioni sui vantaggi derivanti dall&#39;utilizzo di un&#39;attività di allocazione automatica, consultate  [Allocazione automatica ](/help/c-activities/t-test-ab/sample-size-determination.md#auto-allocate) in  *Per quanto tempo è necessario eseguire un* test A/B e una panoramica [ sull&#39;allocazione ](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)automatica. |
| ![Premium ](/help/assets/premium.png) [!UICONTROL badgeAuto-Target] | Utilizza l’apprendimento automatico avanzato per personalizzare i contenuti e favorire le conversioni individuando più esperienze ad alte prestazioni definite dall’addetto al marketing. Inoltre, indica l’esperienza più adatta per ogni visitatore in base al suo profilo cliente individuale e al comportamento dei visitatori precedenti con profili simili. <br>Per ulteriori informazioni, vedi  [Destinazione](/help/c-activities/auto-target/auto-target-to-optimize.md) automatica. |

Per ulteriori informazioni su quale di queste attività [!UICONTROL A/B Test] è adatta alle proprie esigenze, vedere la [ Adobe Target Activities Guide PDF](/help/c-activities/target-activities-guide.md) interattiva.

I passaggi per la creazione dei tre tipi di attività [!UICONTROL A/B Test] sono simili. Per creare un&#39;attività [!UICONTROL Auto-Allocate] o [!UICONTROL Auto-Target], iniziate dalla [creazione di un&#39;attività test A/B](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md), ma quando arrivate alla pagina [!UICONTROL Targeting], scegliete il metodo di allocazione del traffico desiderato, come illustrato di seguito:

* [!UICONTROL Assegnazione automatica per esperienze ottimali]
* [!UICONTROL Targeting automatico per esperienze personalizzate]

![Impostazioni metodo di allocazione traffico](/help/c-activities/t-test-ab/t-test-create-ab/assets/traffic-allocation-method.png)

## Video di formazione: Tipi di attività (9:03) ![Logo Panoramica](/help/assets/overview.png)

Questo video spiega i tipi di attività disponibili in [!DNL Target Standard/Premium].

* Descrizione dei tipi di attività inclusi in [!DNL Adobe Target]
* Selezionare il tipo di attività appropriato per i tuoi obiettivi
* Descrizione del flusso di lavoro guidato in tre passaggi da applicare a tutti i tipi di attività

>[!VIDEO](https://video.tv.adobe.com/v/17386)
