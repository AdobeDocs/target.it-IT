---
keywords: test multivariato;mvt;fattoriale completo;mvt o a/b;multivariato a/b;calcolatore del traffico;quando utilizzare mvt;considerazioni mvt;multivariato;fattoriale parziale;fattoriale parziale;fattoriale completo
description: Scopri come utilizzare un [!UICONTROL test multivariato] (MVT) in [!DNL Adobe Target] per confrontare combinazioni di offerte negli elementi di una pagina per determinare quale combinazione funziona meglio.
title: Cos'è un [!UICONTROL test multivariato]?
feature: Multivariate Tests
exl-id: c8b60011-cb3a-4e28-b84f-06910687b14b
TQID: 'https://experienceleague.adobe.com/JKmjIHJuRxAXlhvUOrrmLMVLnJFhA3T4xkahgH-ozHE'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: b934e7cf-c07f-5a64-924b-3c9da8413e3d
    internal-label: Multivariate Tests
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 0ae6991a6a86854bd64a632070a1fcbe544cc606
workflow-type: tm+mt
source-wordcount: '1382'
ht-degree: 25%
---
# Introduzione a [!UICONTROL Test multivariato] {#get-started-mvt}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come funziona un **[!UICONTROL test multivariato]**, quali termini utilizza [!DNL Target], quando utilizzarlo al posto di un test A/B e come i test fattoriali parziali riducono i requisiti di traffico.

>[!ENDSHADEBOX]

Un&#39;attività **[!UICONTROL Test multivariato]** (MVT) in [!DNL Adobe Target] confronta le combinazioni di offerte negli elementi di una pagina per determinare quale combinazione funziona meglio per un pubblico specifico. Consente inoltre di identificare quale elemento influisce maggiormente sul successo dell’attività. Il test multivariato consente di scoprire l’influenza relativa di elementi specifici sulla conversione rispetto ad altri elementi della pagina, e può aiutarti a perfezionare una combinazione di elementi che si sono dimostrati efficaci.

Un **[!UICONTROL test multivariato]** offre due vantaggi rispetto a un test A/B:

* Mostra quali elementi sulla pagina hanno la maggiore influenza sulla conversione, ed è anche noto come &quot;effetto principale&quot;. Queste informazioni sono utili, ad esempio, per aiutarti a determinare dove posizionare il contenuto a cui desideri prestare maggiore attenzione.
* Consente di trovare effetti composti tra due o più elementi di una pagina, noti anche come &quot;effetto di interazione&quot;. Ad esempio, un particolare annuncio potrebbe produrre più conversioni quando viene combinato con un determinato banner o immagine protagonista.

In [!DNL Target] vengono utilizzati test multivariati fattoriali completi per facilitare l’ottimizzazione del contenuto. Un test multivariato fattoriale completo esamina tutte le possibili combinazioni di contenuto con uguale probabilità. Ad esempio, in presenza di due elementi di pagina con tre offerte ciascuno, le possibili combinazioni sono nove (3x3). Tre elementi, due dei quali includono tre offerte possibili e uno due offerte, offrono 18 opzioni (3x3x2).

In [!DNL Target], ogni combinazione è un&#39;esperienza. Il **[!UICONTROL test multivariato]** confronta ogni esperienza in modo da individuare le combinazioni più efficaci. Allo stesso tempo, [!DNL Target] raccoglie e analizza i dati per comprendere in che modo ogni posizione e le offerte influenzano la metrica di successo.

![Combinazioni test multivariato](assets/multivariate.png)

A causa del numero di combinazioni che possono essere generate, un **[!UICONTROL test multivariato]** richiede più tempo e traffico di un test A/B. La pagina deve ricevere abbastanza traffico per produrre risultati statisticamente significativi per ogni esperienza. Per ottenere risultati utili, scopri la quantità di traffico ricevuto dalla pagina e verifica il numero ottimale di combinazioni per il periodo di tempo corretto.

Il [Calcolatore del traffico](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md#traffic-estimator) può aiutarti a progettare un test che funzioni con il tuo traffico. Prima di utilizzarlo, è necessario disporre di statistiche valide che mostrino il numero di impression e di conversioni che il sito riceve normalmente e considerare i livelli di traffico giornalieri. Più esperienze ha un’attività, più traffico deve includere o più a lungo deve essere eseguita. Se la quantità di traffico non è elevata, prova alcune combinazioni. In caso contrario, il tempo necessario per produrre risultati significativi dei test potrebbe essere troppo lungo per essere utile.

## Terminologia MVT {#mvt-terminology}

Diversi termini sono utilizzati in modi diversi in tutto il settore. La tabella seguente definisce i termini utilizzati da [!DNL Target] per impostare un test multivariato.

| Termine | Definizione |
|--- |--- |
| Combinazione | Le varianti di contenuto create quando si sottopongono a test più opzioni di contenuto in più posizioni. Ad esempio, se stai sottoponendo a test tre posizioni, ciascuna con tre opzioni di contenuto, le possibili combinazioni sono 27 (3x3x3). Un visitatore del sito visualizza una combinazione, definita anche esperienza. |
| Contenuto | Testo o immagine che costituisce una variante di test all’interno di una posizione. In un test multivariato vengono confrontate diverse opzioni di contenuto all’interno di più posizioni. Nella metodologia MVT, il contenuto è a volte denominato *livello*. |
| Elemento | Elemento DOM contenente varianti di contenuto da testare nel test MVT. Vedi anche *Posizione*. |
| Posizione | Un&#39;area di contenuto specifica su una pagina, spesso inserita in un singolo elemento DOM. Nella metodologia MVT, una posizione è a volte indicata come *fattore*. Un testo multivariato fattoriale completo mette a confronto tutte le possibili combinazioni di offerte nelle posizioni. |

## Quando utilizzare [!UICONTROL Test multivariato] rispetto a A/B {#when-to-use-mvt}

La tabella seguente mostra quando utilizzare un **[!UICONTROL test multivariato]**, un test A/B o entrambi insieme per ottimizzare la pagina.

| Situazione | Cosa fare | Dettagli |
|--- |--- |--- |
| Hai meno di tre elementi da testare. | Esegui una serie di test A/B. | Utilizza un test MVT quando disponi di almeno tre elementi. |
| Desideri ottimizzare sia il layout che il contenuto della pagina. | Utilizza un test A/B per ottimizzare il layout della pagina, seguito da un test MVT per determinare il contenuto migliore in ciascun elemento della pagina. | Un test A/B può fornire un feedback importante sul layout, mentre i test MVT sono ideali per il test del contenuto all’interno degli elementi nella progettazione della pagina. L’esecuzione di un test A/B sul layout prima di sottoporre a test più opzioni di contenuto consente di determinare il layout migliore e il contenuto più incisivo. |
| Il numero di esperienze diverse supera i cinque e si estende su due o più elementi. | Utilizza un test MVT per determinare quale elemento è il più importante, facendolo seguire da un test A/B maggiormente concentrato su tale elemento. | I test multivariati mostrano quali aree della pagina hanno più probabilità di migliorare la conversione. Questi sono gli elementi sui quali un addetto al marketing dovrebbe concentrarsi. Ad esempio, il test MVT potrebbe indicare che l’invito all’azione è l’elemento più importante per soddisfare gli obiettivi. Puoi quindi eseguire un test A/B per perfezionare ulteriormente i risultati, ad esempio sottoponendo a test reciproco due immagini specifiche o confrontando il testo o i colori di un call to action. Seguendo un test MVT con uno o più test A/B, puoi determinare il contenuto migliore possibile per i risultati desiderati. |

Per ulteriori considerazioni, ad esempio quanti elementi includere e come pianificare il test, vedere [Best practice per test multivariato](/help/main/c-activities/c-multivariate-testing/best-practices.md).

## Test fattoriali parziali {#partial-factorial}

[!DNL Target] offre test multivariati fattoriali completi come opzione di attività incorporata. In statistica, &quot;Design of Experiments&quot; (progettazione di esperimenti) offre molti approcci, o design, per determinare quali fattori influenzano i risultati. Un approccio di questo tipo è il [metodo Taguchi](https://en.wikipedia.org/wiki/Taguchi_methods) per test fattoriali parziali. Il metodo Taguchi consente agli addetti al marketing di fare una serie di ipotesi che riducono il numero di permutazioni di esperienze da testare, il che a sua volta riduce i requisiti di traffico per un test multivariato. Puoi applicare questo approccio in [!DNL Target] utilizzando questo [foglio di calcolo offline](/help/main/assets/MVT-Taguchi-Partial-Factorial-Design-02102017.xlsx).

Se il team utilizza altri approcci di progettazione di esperimenti, puoi utilizzare il foglio di calcolo come implementazione di riferimento per le progettazioni di esperimenti personalizzate.

Quando utilizzi il foglio di calcolo per calcoli offline, considera i seguenti suggerimenti:

* Scegli gli elementi da modificare e il numero di versioni di ciascun elemento (3x2, 4x3 e così via).
* Manteni coerente la numerazione. Ad esempio, se il pulsante è l’Elemento 1 e le opzioni sono Blu, Verde e Giallo, il pulsante blu sarà 1-1, il pulsante verde 1-2 e il pulsante giallo 1-3.
* Il foglio di calcolo offline fornisce il numero adatto di esperienze necessarie (quattro per un 3x2, nove per un 4x3, e così via).
* Crea le esperienze nel flusso di lavoro A/B con il [Compositore esperienza visivo](/help/main/c-experiences/experiences.md). Puoi usare codice personalizzato, modificare l’HTML, la modalità WYSIWYG o qualsiasi combinazione di questi mezzi.
* Al termine dell’attività (in base al calcolatore delle dimensioni del campione), esegui i risultati nel foglio di calcolo per ottenere gli altri dettagli.

## Video di formazione {#training-videos}

I video seguenti contengono ulteriori informazioni sui concetti descritti in questa pagina.

### Tipi di attività (9:03) ![Icona panoramica](/help/main/assets/overview.png)

Questo video di panoramica spiega i tipi di attività disponibili in [!DNL Target]. Il test multivariato è trattato a partire dal minuto 4:20. Questo video spiega come:

* Descrivere i tipi di attività inclusi in [!DNL Adobe Target].
* Seleziona il tipo di attività appropriato per raggiungere gli obiettivi.
* Descrivi il flusso di lavoro guidato in tre passaggi applicabile a tutti i tipi di attività.

>[!VIDEO](https://video.tv.adobe.com/v/17386)

### Creazione di test multivariati (9:25) ![Icona esercitazione](/help/main/assets/tutorial.png)

Questo video spiega come comprendere, pianificare e creare un test multivariato utilizzando il flusso di lavoro guidato in tre passaggi di [!DNL Target]. Questo video spiega come:

* Definire e progettare un test multivariato.
* Creare un test multivariato.

>[!VIDEO](https://video.tv.adobe.com/v/17395)
