---
keywords: AB;A/B;AB...n;confrontare esperienze;Targeting;confrontare contenuto;targeting automatico;allocazione automatica
description: Esplora le attività di test A/B in [!DNL Target] - [!UICONTROL Manuale], [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico].
title: Scopri le attività di test A/B disponibili in [!DNL Target].
feature: A/B Tests
exl-id: e8ff8994-a0a9-4fc7-8fcb-e3a1b7697604
TQID: 'https://experienceleague.adobe.com/wcflYDj0VB7dJODNO6XjFHB0PPIhN4aUrBJxbKPoNdg'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ab2570eb-4844-49aa-8334-e91a345525e5
    internal-label: A/B Tests
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
    internal-label: Machine learning
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
    internal-label: Customer profiles
source-git-commit: d887712962ad4e3cecd6b3b86ee33a4bcb99f2a8
workflow-type: tm+mt
source-wordcount: '667'
ht-degree: 19%
---
# Panoramica sui test A/B {#test-ab}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri cos&#39;è un test A/B manuale, quando utilizzarlo al posto di un test multivariato e come si relaziona ai tipi di attività Allocazione automatica e Targeting automatico.

>[!ENDSHADEBOX]

Un&#39;attività **[!UICONTROL Test A/B]** manuale (a volte definita test A/B...N) confronta due o più versioni del contenuto del sito Web per vedere quale versione meglio solleva le conversioni, le vendite o altre metriche identificate. Un test A/B permette di confrontare le modifiche apportate alla pagina rispetto alla struttura di pagina predefinita, per determinare quale esperienza produce i risultati migliori.

## Quando utilizzare un test A/B manuale {#when-to-use}

Utilizza un test A/B manuale quando:

* Hai una chiara ipotesi di modi per migliorare le prestazioni della pagina, in base a metriche di successo o alla distribuzione di contenuti alternativi.
* Desideri testare modifiche di grandi dimensioni, ad esempio nuovi layout o trattamenti drasticamente diversi degli elementi. Se la progettazione del test non viene facilmente suddivisa in singoli elementi di pagina, è necessario eseguire un test A/B prima di eseguire un [test multivariato](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md).
* Vuoi decidere la percentuale di visitatori che visualizzano ogni esperienza. Ad esempio, puoi suddividere il traffico in modo uniforme tra il controllo e una seconda esperienza, oppure puoi testare una nuova esperienza più rischiosa mostrandola a solo il 5% del pubblico.

Per informazioni dettagliate sulla determinazione delle dimensioni ottimali del campione per un test A/B, consulta [Pianificare il test A/B](/help/main/c-activities/t-test-ab/sample-size-determination.md).

### Combinare un test multivariato e test A/B

Quando il numero di esperienze diverse supera le cinque e si estende su due o più posizioni, è consigliabile prendere in considerazione un [test MVT](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) prima di eseguire i test A/B:

1. **Esegui un test multivariato** per vedere quali aree della pagina hanno più probabilità di migliorare la conversione. Queste aree sono le posizioni sulle quali un addetto al marketing dovrebbe concentrarsi. Ad esempio, il test MVT potrebbe indicare che l&#39;invito all&#39;azione è la posizione più importante per soddisfare gli obiettivi.

1. **Esegui uno o più test A/B** in tali posizioni per perfezionare ulteriormente i risultati. Ad esempio, per sottoporre a test reciproco due immagini specifiche o per confrontare il testo o i colori di un call to action.

Facendo seguire un test MVT da uno o più test A/B, puoi determinare il contenuto migliore possibile per i risultati desiderati.

## Tipi di attività di test A/B {#types}

Oltre all&#39;attività manuale **[!UICONTROL Test A/B]**, [!DNL Target] fornisce altri due tipi di attività **[!UICONTROL Test A/B]**: **[!UICONTROL Allocazione automatica]** e **[!UICONTROL Targeting automatico]**.

| Tipo di attività | Descrizione |
| --- | --- |
| **[!UICONTROL Test A/B manuale]** | Confronta due o più esperienze per vedere quale migliora in modo più efficace le conversioni durante un periodo di test pre-specificato.<P>In questa sezione viene descritto come impostare un&#39;attività **[!UICONTROL Test A/B]** manuale, ma i passaggi per gli altri tipi di attività **[!UICONTROL Test A/B]** sono simili. |
| **[!UICONTROL Allocazione automatica]** | Identifica un vincitore tra due o più esperienze, quindi reindirizza il traffico verso il vincitore, aumentando la conversione mentre il test viene eseguito e appreso.<P>Per informazioni sui vantaggi dell&#39;utilizzo di un&#39;attività **[!UICONTROL Allocazione automatica]**, vedere [Allocazione automatica](/help/main/c-activities/t-test-ab/sample-size-determination.md#auto-allocate) in *Per quanto tempo si deve eseguire un test A/B* e [Panoramica dell&#39;allocazione automatica](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md). |
| ![Badge Premium](/help/main/assets/premium.png) **[!UICONTROL Targeting automatico]** | Utilizza l’apprendimento automatico avanzato per personalizzare i contenuti e favorire le conversioni identificando più esperienze ad alte prestazioni definite dall’addetto al marketing. L’esperienza più personalizzata viene quindi fornita ai visitatori in base ai loro profili cliente individuali e ai comportamenti passati di visitatori simili.<P>Per ulteriori informazioni, vedere [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md). |

Per ulteriori informazioni su quali di queste **[!UICONTROL attività Test A/B]** sono più adatte alle tue esigenze, consulta la [Guida delle attività di Adobe Target PDF](/help/main/c-activities/target-activities-guide.md) interattiva.

>[!NOTE]
>
>Puoi includere i consigli nelle attività **[!UICONTROL Test A/B]**, **[!UICONTROL Allocazione automatica]** e **[!UICONTROL Targeting automatico]** (e **[!UICONTROL Targeting esperienza]** (XT). Per ulteriori informazioni, consulta [Consigli come offerta](/help/main/c-recommendations/recommendations-as-an-offer.md). Questa funzionalità richiede una [licenza di Target Premium](/help/main/c-intro/intro.md#premium).
