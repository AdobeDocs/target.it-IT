---
keywords: AB;A/B;AB...n;compare experiences;Targeting;compare content
description: Il test A/B confronta due o più versioni del contenuto del sito web per vedere quale versione migliora maggiormente le conversioni durante un dato periodo di test.
title: Test A/B
feature: ab
uuid: 154559cf-58bb-425d-bb2e-4eaf34c89451
translation-type: tm+mt
source-git-commit: 130edc89b2c324a0d892a4221f644248e23357a4
workflow-type: tm+mt
source-wordcount: '722'
ht-degree: 58%

---


# Test A/B

Mediante un test A/B manuale potete mettere a confronto due o più versioni del contenuto del sito Web per vedere quale versione migliora maggiormente le conversioni durante un periodo di test preimpostato.

>[!NOTE]
>
>Oltre all&#39;attività di test A/B manuale (impostazione predefinita) (descritta in questa sezione), [!DNL Target] sono disponibili due tipi aggiuntivi di attività di test A/B: [!UICONTROL Allocazione] automatica e destinazione [!UICONTROL automatica].
>
>Per ulteriori informazioni, consulta [Tipi di attività](#types) di test A/B di seguito.

Un test A/B manuale (a volte denominato test A/B...N) mette a confronto due o più versioni del contenuto del sito Web per vedere quale incrementa maggiormente le conversioni, le vendite o altre metriche identificate. Un test A/B permette di confrontare le modifiche apportate alla pagina rispetto alla struttura di pagina predefinita, per determinare quale esperienza produce i risultati migliori.

I test A/B manuali sono particolarmente utili quando si dispone di un&#39;ipotesi chiara su come migliorare le prestazioni della pagina in base a metriche di successo o alla distribuzione alternativa dei contenuti.

I test A/B manuali sono particolarmente adatti per modifiche di grandi dimensioni che potrebbero comportare nuovi layout o trattamenti drasticamente diversi degli elementi. Se la progettazione del test non può essere facilmente suddivisa in elementi di pagina singoli, è necessario eseguire un test A/B prima di un test multivariato.

Quando viene configurato il test, è possibile determinare la percentuale di visitatori che visualizzano ogni esperienza. Ad esempio, è possibile suddividere il traffico in modo uniforme tra il controllo e una seconda esperienza, oppure è possibile testare un&#39;esperienza nuova e più rischiosa mostrandola a solo il 5% del pubblico.

>[!NOTE]
>
>Per informazioni dettagliate sulla determinazione delle dimensioni ottimali del campione per un test A/B, consulta [Pianificare il test A/B](../../c-activities/t-test-ab/sample-size-determination.md#concept_2801F552DB874C20B8A17C1B774C0383).

Quando il numero di esperienze diverse supera le cinque e si estende su due o più posizioni, è consigliabile considerare un [test MVT](/help/c-activities/c-multivariate-testing/multivariate-testing.md) prima di eseguire i test A/B. I test multivariati mostrano quali aree della pagina hanno più probabilità di migliorare la conversione. Queste posizioni sono quelle sulle quali un addetto al marketing dovrebbe concentrarsi. Ad esempio, il test MVT potrebbe indicare che l&#39;invito all&#39;azione è la posizione più importante per soddisfare gli obiettivi. Una volta determinati le posizioni e il contenuto più utili per raggiungere gli obiettivi, puoi eseguire un test A/B per perfezionare ulteriormente i risultati, ad esempio per sottoporre a test reciproco due immagini specifiche, o confrontare il testo o colori di un invito all&#39;azione. Facendo seguire un test MVT da uno o più test A/B, puoi determinare il contenuto migliore possibile per i risultati desiderati.

## Tipi di attività di test A/B {#types}

Oltre all&#39;attività di test A/B manuale (impostazione predefinita) (descritta in questa sezione), [!DNL Target] sono disponibili due tipi aggiuntivi di attività di test A/B: [!UICONTROL Allocazione] automatica e destinazione [!UICONTROL automatica].

| Tipo di attività | Descrizione |
| --- | --- |
| Test A/B manuale | Confronta due o più esperienze per vedere quale migliora in modo più efficace le conversioni durante un periodo di test pre-specificato. <br>Questa sezione descrive come impostare un&#39;attività di test A/B manuale, ma i passaggi per gli altri tipi di attività di test A/B sono simili. |
| [!UICONTROL Allocazione automatica] | Identifica un vincitore tra due o più esperienze, e reindirizza il traffico verso il vincitore, aumentando la conversione mentre il test continua a essere eseguito e ad apprendere. <br>Per ulteriori informazioni, consulta [Allocazione automatica](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md). |
| ![badge](/help/assets/premium.png) Premium [!UICONTROL Auto-Target] | Utilizza l’apprendimento automatico avanzato per personalizzare i contenuti e favorire le conversioni individuando più esperienze ad alte prestazioni definite dall’addetto al marketing. Inoltre, indica l’esperienza più adatta per ogni visitatore in base al suo profilo cliente individuale e al comportamento dei visitatori precedenti con profili simili. <br>Per ulteriori informazioni, vedi [Destinazione](/help/c-activities/auto-target-to-optimize.md)automatica. |

Per ulteriori informazioni su quale di queste attività di test A/B è più adatta alle proprie esigenze, consulta la Guida interattiva alle attività di [Adobe Target in formato PDF](/help/c-activities/target-activities-guide.md).

I passaggi per creare i tre tipi di attività di test A/B sono simili. Per creare un&#39;attività di allocazione [!UICONTROL automatica] o [!UICONTROL targeting] automatico, iniziate [creando un&#39;attività](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)di test A/B, ma quando passate alla pagina [!UICONTROL Targeting] , scegliete il metodo di allocazione traffico desiderato:

* [!UICONTROL Assegnazione automatica per esperienze ottimali]
* [!UICONTROL Targeting automatico per esperienze personalizzate]

![Impostazioni metodo di allocazione traffico](/help/c-activities/t-test-ab/t-test-create-ab/assets/traffic-allocation-method.png)

## Video di formazione: Logo ![Panoramica sui tipi di attività (9:03)](/help/assets/overview.png)

Questo video spiega i tipi di attività disponibili in [!DNL Target Standard/Premium].

* Descrizione dei tipi di attività inclusi in [!DNL Adobe Target]
* Selezionare il tipo di attività appropriato per i tuoi obiettivi
* Descrizione del flusso di lavoro guidato in tre passaggi da applicare a tutti i tipi di attività

>[!VIDEO](https://video.tv.adobe.com/v/17386)
