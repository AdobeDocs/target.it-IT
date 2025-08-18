---
keywords: AB;A/B;AB...n;confrontare esperienze;Targeting;confrontare contenuto;targeting automatico;allocazione automatica
description: Esplora le attività di test A/B in  [!DNL Target] - [!UICONTROL Manual], [!UICONTROL Auto-Allocate] e [!UICONTROL Auto-Target].
title: Scopri le attività di test A/B disponibili in [!DNL Target].
feature: A/B Tests
exl-id: e8ff8994-a0a9-4fc7-8fcb-e3a1b7697604
source-git-commit: 974746e25724abf0e5edd3884331ec0975e5352e
workflow-type: tm+mt
source-wordcount: '670'
ht-degree: 21%

---

# Panoramica sui test A/B

Un&#39;attività [!UICONTROL A/B Test] manuale (a volte definita test A/B...N) confronta due o più versioni del contenuto del sito Web per vedere quale versione meglio solleva le conversioni, le vendite o altre metriche identificate. Un test A/B permette di confrontare le modifiche apportate alla pagina rispetto alla struttura di pagina predefinita, per determinare quale esperienza produce i risultati migliori.

>[!TIP]
>
>Oltre all&#39;attività [!UICONTROL Manual] (predefinita) [!UICONTROL A/B Test] (discussa in questo articolo), [!DNL Target] fornisce altri due tipi di attività [!UICONTROL A/B Test]: [!UICONTROL Auto-Allocate] e [!UICONTROL Auto-Target]. Per ulteriori informazioni, consulta [Tipi di attività di test A/B](#types) di seguito.

I test A/B manuali sono utili quando si dispone di un’ipotesi chiara di modi per migliorare le prestazioni della pagina in base a metriche di successo o alla distribuzione di contenuti alternativi.

I test A/B manuali sono particolarmente adatti per modifiche di grandi dimensioni che potrebbero includere nuovi layout o trattamenti drasticamente diversi degli elementi. Se la progettazione del test non viene facilmente suddivisa in singoli elementi di pagina, è necessario eseguire un test A/B prima di eseguire un [test multivariato](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md).

Quando imposti il test A/B, puoi determinare la percentuale di visitatori che visualizzano ogni esperienza. Ad esempio, puoi suddividere il traffico in modo uniforme tra il controllo e una seconda esperienza, oppure puoi testare una nuova esperienza più rischiosa mostrandola a solo il 5% del pubblico.

>[!NOTE]
>
>Per informazioni dettagliate sulla determinazione delle dimensioni ottimali del campione per un test A/B, consulta [Pianificare il test A/B](/help/main/c-activities/t-test-ab/sample-size-determination.md).

Quando il numero di esperienze diverse supera le cinque e si estende su due o più posizioni, è consigliabile prendere in considerazione un [test MVT](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) prima di eseguire i test A/B. I test multivariati mostrano quali aree della pagina hanno più probabilità di migliorare la conversione. Queste aree sono le posizioni sulle quali un addetto al marketing dovrebbe concentrarsi. Ad esempio, il test MVT potrebbe indicare che l&#39;invito all&#39;azione è la posizione più importante per soddisfare gli obiettivi. Dopo aver determinato le posizioni e il contenuto più utili per raggiungere gli obiettivi, puoi eseguire un test A/B per perfezionare ulteriormente i risultati. Ad esempio, per sottoporre a test reciproco due immagini specifiche o per confrontare il testo o i colori di un call to action. Facendo seguire un test MVT da uno o più test A/B, puoi determinare il contenuto migliore possibile per i risultati desiderati.

## Tipi di attività di test A/B {#types}

Oltre all&#39;attività manuale [!UICONTROL A/B Test], [!DNL Target] fornisce altri due tipi di attività [!UICONTROL A/B Testing]: [!UICONTROL Auto-Allocate] e [!UICONTROL Auto-Target].

| Tipo di attività | Descrizione |
| --- | --- |
| [!UICONTROL Manual A/B Test] | Confronta due o più esperienze per vedere quale migliora in modo più efficace le conversioni durante un periodo di test pre-specificato.<P>In questa sezione viene descritto come impostare un&#39;attività [!UICONTROL A/B Test] manuale, ma i passaggi per gli altri tipi di attività [!UICONTROL A/B Test] sono simili. |
| [!UICONTROL Auto-Allocate] | Identifica un vincitore tra due o più esperienze, quindi reindirizza il traffico verso il vincitore, aumentando la conversione mentre il test viene eseguito e appreso.<P>Per informazioni sui vantaggi dell&#39;utilizzo di un&#39;attività [!UICONTROL Auto-Allocate], vedere [Allocazione automatica](/help/main/c-activities/t-test-ab/sample-size-determination.md#auto-allocate) in *Per quanto tempo si deve eseguire un test A/B* e [Panoramica dell&#39;allocazione automatica](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md). |
| ![Badge Premium](/help/main/assets/premium.png) [!UICONTROL Auto-Target] | Utilizza l’apprendimento automatico avanzato per personalizzare i contenuti e favorire le conversioni identificando più esperienze ad alte prestazioni definite dall’addetto al marketing. L’esperienza più personalizzata viene quindi fornita ai visitatori in base ai loro profili cliente individuali e ai comportamenti passati di visitatori simili.<P>Per ulteriori informazioni, vedere [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md). |

Per ulteriori informazioni sulle attività di [!UICONTROL A/B Test] più adatte all&#39;utente, vedere la [Guida delle attività di Adobe Target PDF](/help/main/c-activities/target-activities-guide.md) interattiva.

I passaggi per la creazione dei tre tipi di attività [!UICONTROL A/B Test] sono simili. Per creare un&#39;attività [!UICONTROL Auto-Allocate] o [!UICONTROL Auto-Target]:

1. Iniziare [creando un&#39;attività Test A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md).
1. Quando si arriva alla pagina [!UICONTROL Targeting], fare clic sul controllo [!UICONTROL Traffic Allocation], quindi scegliere il metodo di allocazione del traffico desiderato nel riquadro di destra, come illustrato di seguito:

   * [!UICONTROL Auto-Allocate to best experience]
   * [!UICONTROL Auto-Target for personalized experience]

   ![Impostazioni del metodo di allocazione traffico](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/traffic-allocation-method-new.png)

## Includere consigli nelle attività A/B

Puoi includere i consigli nelle attività [!UICONTROL A/B Test], [!UICONTROL Auto-Allocate] e [!UICONTROL Auto-Target] (e [!UICONTROL Experience Targeting] (XT)). Per ulteriori informazioni, consulta [Consigli come offerta](/help/main/c-recommendations/recommendations-as-an-offer.md).

Questa funzionalità richiede una [licenza di Target Premium](/help/main/c-intro/intro.md#premium).
