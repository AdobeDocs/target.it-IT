---
keywords: AB;A/B;AB...n;compare experiences;Targeting;compare content;auto-target;auto-allocate
description: Un'attività di test A/B manuale mette a confronto due o più versioni del contenuto del sito Web per vedere quale versione migliora maggiormente le conversioni durante un periodo di test preimpostato.
title: Panoramica del test A/B
feature: ab
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '754'
ht-degree: 38%

---


# Panoramica del test A/B

A manual [!UICONTROL A/B Test] activity compares two or more versions of your website content to see which version best improves your conversions during a pre-specified test period.

>[!NOTE]
>
>Oltre all&#39;attività di test [!UICONTROL A/B manuale (impostazione predefinita)] A/B (descritta in questa sezione), [!DNL Target] sono disponibili due tipi aggiuntivi di attività di test  A/B: [!UICONTROL Allocazione] automatica e destinazione [!UICONTROL automatica].
>
>Per ulteriori informazioni, consulta [Tipi di attività](#types) di test A/B di seguito.

A manual [!UICONTROL A/B Test] activity (sometimes referred to as an A/B...N test) compares two or more versions of your Web site content to see which best lifts your conversions, sales, or other metrics you identify. Un test A/B permette di confrontare le modifiche apportate alla pagina rispetto alla struttura di pagina predefinita, per determinare quale esperienza produce i risultati migliori.

I test A/B manuali sono particolarmente utili quando si dispone di un&#39;ipotesi chiara su come migliorare le prestazioni della pagina in base a metriche di successo o alla distribuzione alternativa dei contenuti.

I test A/B manuali sono particolarmente adatti per modifiche di grandi dimensioni che potrebbero comportare nuovi layout o trattamenti drasticamente diversi degli elementi. If your test design does not easily break down into individual page elements, you should run an A/B test before a [multivariate test](/help/c-activities/c-multivariate-testing/multivariate-testing.md).

Quando configurate il test A/B, potete determinare la percentuale di visitatori che visualizzano ogni esperienza. Ad esempio, è possibile suddividere il traffico in modo uniforme tra il controllo e una seconda esperienza, oppure è possibile testare un&#39;esperienza nuova e più rischiosa mostrandola a solo il 5% del pubblico.

>[!NOTE]
>
>Per informazioni dettagliate sulla determinazione delle dimensioni ottimali del campione per un test A/B, consulta [Pianificare il test A/B](/help/c-activities/t-test-ab/sample-size-determination.md).

Quando il numero di esperienze diverse supera le cinque e si estende su due o più posizioni, è consigliabile considerare un [test MVT](/help/c-activities/c-multivariate-testing/multivariate-testing.md) prima di eseguire i test A/B. I test multivariati mostrano quali aree della pagina hanno più probabilità di migliorare la conversione. Queste posizioni sono quelle sulle quali un addetto al marketing dovrebbe concentrarsi. Ad esempio, il test MVT potrebbe indicare che l&#39;invito all&#39;azione è la posizione più importante per soddisfare gli obiettivi. Una volta determinate le posizioni e il contenuto più utili per raggiungere gli obiettivi, potete eseguire un test A/B per perfezionare ulteriormente i risultati, ad esempio per sottoporre a test reciproco due immagini specifiche, o per confrontare il testo o i colori di un invito all&#39;azione. Facendo seguire un test MVT da uno o più test A/B, puoi determinare il contenuto migliore possibile per i risultati desiderati.

## Tipi di attività di test A/B {#types}

Oltre all&#39;attività manuale di test [!UICONTROL A/B (descritta in questa sezione),] [!DNL Target] fornisce due tipi aggiuntivi di attività di test A/B: [!UICONTROL Allocazione] automatica e destinazione [!UICONTROL automatica].

| Tipo di attività | Descrizione |
| --- | --- |
| [!UICONTROL Test A/B manuale] | Confronta due o più esperienze per vedere quale migliora in modo più efficace le conversioni durante un periodo di test pre-specificato. <br>Questa sezione descrive come impostare un&#39;attività di test [!UICONTROL A/B manuale, ma i passaggi per gli altri tipi di attività di test]  A/B sono simili. |
| [!UICONTROL Allocazione automatica] | Identifica un vincitore tra due o più esperienze, e reindirizza il traffico verso il vincitore, aumentando la conversione mentre il test continua a essere eseguito e ad apprendere. <br>Per informazioni sui vantaggi dell&#39;utilizzo di un&#39;attività di allocazione automatica, consultate Allocazione [automatica](/help/c-activities/t-test-ab/sample-size-determination.md#auto-allocate) in *quanto tempo eseguire un test* A/B e una panoramica [di allocazione](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)automatica. |
| ![badge](/help/assets/premium.png) Premium [!UICONTROL Auto-Target] | Utilizza l’apprendimento automatico avanzato per personalizzare i contenuti e favorire le conversioni individuando più esperienze ad alte prestazioni definite dall’addetto al marketing. Inoltre, indica l’esperienza più adatta per ogni visitatore in base al suo profilo cliente individuale e al comportamento dei visitatori precedenti con profili simili. <br>Per ulteriori informazioni, vedi [Destinazione](/help/c-activities/auto-target/auto-target-to-optimize.md)automatica. |

Per ulteriori informazioni su quale di queste attività di test [!UICONTROL A/B è adatta alle tue esigenze, consulta la Guida interattiva alle attività di] Adobe Target in formato PDF [](/help/c-activities/target-activities-guide.md).

I passaggi per la creazione dei tre tipi di attività di test  A/B sono simili. Per creare un&#39;attività di allocazione [!UICONTROL automatica] o [!UICONTROL targeting] automatico, iniziate [creando un&#39;attività](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)di test A/B, ma quando passate alla pagina [!UICONTROL Targeting] , scegliete il metodo di allocazione traffico desiderato, come illustrato di seguito:

* [!UICONTROL Assegnazione automatica per esperienze ottimali]
* [!UICONTROL Targeting automatico per esperienze personalizzate]

![Impostazioni metodo di allocazione traffico](/help/c-activities/t-test-ab/t-test-create-ab/assets/traffic-allocation-method.png)

## Video di formazione: Logo ![Panoramica sui tipi di attività (9:03)](/help/assets/overview.png)

Questo video spiega i tipi di attività disponibili in [!DNL Target Standard/Premium].

* Descrizione dei tipi di attività inclusi in [!DNL Adobe Target]
* Selezionare il tipo di attività appropriato per i tuoi obiettivi
* Descrizione del flusso di lavoro guidato in tre passaggi da applicare a tutti i tipi di attività

>[!VIDEO](https://video.tv.adobe.com/v/17386)
