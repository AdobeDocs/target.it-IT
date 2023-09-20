---
keywords: AB;A/B;AB...n;confrontare esperienze;Targeting;confrontare contenuto;targeting automatico;allocazione automatica
description: Scopri i diversi tipi di attività di test A/B in Adobe [!DNL Target] - Manuale, Allocazione automatica e Targeting automatico. Scegli quello che fa per te.
title: Quale tipo di attività A/B è disponibile in Target?
feature: A/B Tests
exl-id: e8ff8994-a0a9-4fc7-8fcb-e3a1b7697604
source-git-commit: b5da2f5d41739af39d97e0ce9761006794c04d2b
workflow-type: tm+mt
source-wordcount: '809'
ht-degree: 25%

---

# Panoramica sui test A/B

Un manuale [!UICONTROL Test A/B] l’attività confronta due o più versioni del contenuto del sito web per vedere quale versione migliora meglio le conversioni durante un periodo di test predefinito.

>[!NOTE]
>
>Oltre al manuale (impostazione predefinita) [!UICONTROL Test A/B] attività (discussa in questa sezione), [!DNL Target] fornisce due tipi aggiuntivi di [!UICONTROL Test A/B] attività: [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico]. Consulta [Tipi di attività di test A/B](#types) per ulteriori informazioni.

Un manuale [!UICONTROL Test A/B] L’attività di (talvolta definita test A/B...N) confronta due o più versioni del contenuto del sito Web per vedere quale versione migliora le conversioni, le vendite o altre metriche identificate. Un test A/B permette di confrontare le modifiche apportate alla pagina rispetto alla struttura di pagina predefinita, per determinare quale esperienza produce i risultati migliori.

I test A/B manuali sono utili quando si dispone di un’ipotesi chiara di modi per migliorare le prestazioni della pagina in base a metriche di successo o alla distribuzione di contenuti alternativi.

I test A/B manuali sono particolarmente adatti per modifiche di grandi dimensioni che potrebbero includere nuovi layout o trattamenti drasticamente diversi degli elementi. Se la progettazione del test non si suddivide facilmente in singoli elementi di pagina, è necessario eseguire un test A/B prima di un [test multivariato](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md).

Quando imposti il test A/B, puoi determinare la percentuale di visitatori che visualizzano ogni esperienza. Ad esempio, è possibile suddividere il traffico in modo uniforme tra il controllo e una seconda esperienza, oppure è possibile testare un&#39;esperienza nuova e più rischiosa mostrandola a solo il 5% del pubblico.

>[!NOTE]
>
>Per informazioni dettagliate sulla determinazione delle dimensioni ottimali del campione per un test A/B, consulta [Pianificare il test A/B](/help/main/c-activities/t-test-ab/sample-size-determination.md).

Quando il numero di esperienze diverse supera le cinque e si estende su due o più posizioni, è consigliabile prendere in considerazione una [Test MVT](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) prima di eseguire i test A/B. I test multivariati mostrano quali aree della pagina hanno più probabilità di migliorare la conversione. Queste aree sono le posizioni sulle quali un addetto al marketing dovrebbe concentrarsi. Ad esempio, il test MVT potrebbe indicare che l&#39;invito all&#39;azione è la posizione più importante per soddisfare gli obiettivi. Dopo aver determinato le posizioni e il contenuto più utili per raggiungere gli obiettivi, puoi eseguire un test A/B per perfezionare ulteriormente i risultati. Ad esempio, per sottoporre a test reciproco due immagini specifiche o per confrontare il testo o i colori di un invito all’azione. Facendo seguire un test MVT da uno o più test A/B, puoi determinare il contenuto migliore possibile per i risultati desiderati.

## Tipi di attività di test A/B {#types}

Oltre al manuale [!UICONTROL Test A/B] attività (discussa in questa sezione), [!DNL Target] fornisce due ulteriori tipi di attività di test A/B: [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico].

| Tipo di attività | Descrizione |
| --- | --- |
| [!UICONTROL Test A/B manuale] | Confronta due o più esperienze per vedere quale migliore esperienza migliora le conversioni durante un periodo di test pre-specificato.<P>Questa sezione descrive come impostare un manuale [!UICONTROL Test A/B] attività, ma i passaggi per gli altri tipi di [!UICONTROL Test A/B] attività sono simili. |
| [!UICONTROL Allocazione automatica] | Identifica un vincitore tra due o più esperienze, quindi reindirizza il traffico verso il vincitore, aumentando la conversione mentre il test viene eseguito e appreso.<P>Per scoprire i vantaggi dell&#39;utilizzo di un&#39; [!UICONTROL Allocazione automatica] attività, vedi [Allocazione automatica](/help/main/c-activities/t-test-ab/sample-size-determination.md#auto-allocate) in *Per quanto tempo si deve eseguire un test A/B* e [Panoramica dell’allocazione automatica](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md). |
| ![Badge Premium](/help/main/assets/premium.png) [!UICONTROL Targeting automatico] | Utilizza l’apprendimento automatico avanzato per personalizzare i contenuti e favorire le conversioni identificando più esperienze ad alte prestazioni definite dall’addetto al marketing. L’esperienza più personalizzata viene quindi fornita ai visitatori in base ai loro profili cliente individuali e ai comportamenti passati di visitatori simili.<P>Per ulteriori informazioni, consulta [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md). |

Per ulteriori informazioni su quali di questi [!UICONTROL Test A/B] attività è la scelta giusta per te, consulta la sezione [Guida alle attività di Adobe Target PDF](/help/main/c-activities/target-activities-guide.md).

I passaggi per creare i tre tipi di [!UICONTROL Test A/B] attività sono simili. Per creare un [!UICONTROL Allocazione automatica] o [!UICONTROL Targeting automatico] attività, inizia per [creazione di un’attività Test A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md), ma quando si arriva al [!UICONTROL Targeting] , scegli il metodo di allocazione del traffico desiderato, come illustrato di seguito:

* [!UICONTROL Allocazione automatica all’esperienza migliore]
* [!UICONTROL Targeting automatico per esperienza personalizzata]

![Impostazioni del metodo di allocazione traffico](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/traffic-allocation-method.png)

## Includere consigli nelle attività A/B

Puoi includere i consigli in [!UICONTROL Test A/B], [!UICONTROL Allocazione automatica], e [!UICONTROL Targeting automatico] attività (e [!UICONTROL Targeting esperienza] (XT). Per ulteriori informazioni, consulta [Consigli come offerta](/help/main/c-recommendations/recommendations-as-an-offer.md).

Questa funzionalità richiede una [licenza di Target Premium](/help/main/c-intro/intro.md#premium)

## Video di formazione: Tipi di attività (9:03) ![Badge panoramica](/help/main/assets/overview.png)

Questo video spiega i tipi di attività disponibili in [!DNL Target Standard/Premium].

* Descrizione dei tipi di attività inclusi in [!DNL Adobe Target]
* Selezionare il tipo di attività appropriato per i tuoi obiettivi
* Descrizione del flusso di lavoro guidato in tre passaggi da applicare a tutti i tipi di attività

>[!VIDEO](https://video.tv.adobe.com/v/17386)
