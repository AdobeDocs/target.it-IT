---
keywords: targeting automatico;targeting;allocazione traffico;domande frequenti;faq;risoluzione dei problemi;risoluzione problemi
description: Scopri in che modo un'attività [!UICONTROL Auto-Target] fornisce l'esperienza più personalizzata a ogni visitatore in base ai profili cliente e al comportamento di visitatori simili.
title: Che cos'è un'attività [!UICONTROL Auto-Target]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Auto-Target
exl-id: 59ca30dc-45a0-4129-b832-84e1132d3b69
source-git-commit: 32a91a41cd182d3a55ded7dea8c1c6ea6f46aa71
workflow-type: tm+mt
source-wordcount: '1828'
ht-degree: 18%

---

# Panoramica di [!UICONTROL Auto-Target]

[!UICONTROL Auto-Target] attività in [!DNL Adobe Target] utilizzano l&#39;apprendimento automatico avanzato per scegliere tra più esperienze ad alte prestazioni definite dall&#39;addetto al marketing per personalizzare il contenuto e favorire le conversioni. [!UICONTROL Auto-Target] fornisce l&#39;esperienza più personalizzata a ogni visitatore in base al suo profilo cliente individuale e al comportamento dei visitatori precedenti con profili simili.

>[!NOTE]
>
>* [!UICONTROL Auto-Target] è disponibile nella soluzione [!DNL Target Premium]. Questa funzione non è disponibile in [!DNL Target Standard] senza una licenza [!DNL Target Premium]. Per ulteriori informazioni sulle funzioni avanzate fornite da questa licenza, consulta [Target Premium](/help/main/c-intro/intro.md).
>
>* [!UICONTROL Analytics for Target] (A4T) supporta [!UICONTROL Auto-Target] attività. Per ulteriori informazioni, consulta [Supporto A4T per attività di allocazione automatica e targeting automatico](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md).

## Storia di successo nel mondo reale con l’utilizzo del Targeting automatico {#success}

Un importante retailer di abbigliamento ha recentemente utilizzato un&#39;attività [!UICONTROL Auto-Target] con dieci esperienze basate su categorie di prodotti (più controllo randomizzato) per fornire il contenuto giusto a ogni visitatore. &quot;[!UICONTROL Add to Cart]&quot; è stato scelto come metrica di ottimizzazione primaria. Le esperienze mirate hanno avuto un incremento medio del 29,09%. Dopo aver generato i modelli [!UICONTROL Auto-Target], l&#39;attività è stata impostata sul 90% di esperienze personalizzate.

In soli dieci giorni, è stato raggiunto un incremento di oltre 1.700.000 dollari.

Continua a leggere per scoprire come utilizzare [!UICONTROL Auto-Target] per aumentare l&#39;incremento e i ricavi per la tua organizzazione.

## Panoramica {#section_972257739A2648AFA7E7556B693079C9}

Durante la [creazione di un&#39;attività A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) tramite il flusso di lavoro guidato in tre passaggi, scegliere l&#39;opzione **[!UICONTROL Auto-Target for personalized experiences]** nella pagina **[!UICONTROL Targeting]** (passaggio 2).

![Impostazioni del metodo di allocazione traffico](/help/main/c-activities/automated-traffic-allocation/assets/auto-target.png)

L&#39;opzione [!UICONTROL Auto-Target] all&#39;interno del flusso di attività A/B ti consente di sfruttare l&#39;apprendimento automatico per personalizzare in base a una serie di esperienze definite dall&#39;addetto al marketing in un clic. [!UICONTROL Auto-Target] è progettato per fornire la massima ottimizzazione, rispetto ai tradizionali test A/B o [!UICONTROL Auto Allocate], determinando quale esperienza visualizzare per ogni visitatore. A differenza di un&#39;attività A/B in cui l&#39;obiettivo è quello di trovare un singolo vincitore, [!UICONTROL Auto-Target] determina automaticamente la migliore esperienza per un determinato visitatore. La migliore esperienza si basa sul profilo del visitatore e su altre informazioni contestuali, per fornire un’esperienza altamente personalizzata.

Analogamente a [!UICONTROL Automated Personalization], [!UICONTROL Auto-Target] utilizza un [algoritmo Foresta casuale](/help/main/c-activities/t-automated-personalization/algo-random-forest.md), uno dei principali metodi di raccolta di dati scientifici, per determinare l&#39;esperienza migliore da mostrare a un visitatore. Poiché [!UICONTROL Auto-Target] può adattarsi ai cambiamenti nel comportamento del visitatore, può essere eseguito perennemente per fornire un incremento. Questo metodo è talvolta indicato come modalità &quot;sempre attiva&quot;.

A differenza di un&#39;attività A/B in cui l&#39;allocazione dell&#39;esperienza per un determinato visitatore è definitiva, [!UICONTROL Auto-Target] ottimizza l&#39;obiettivo di business specificato su ogni visita. Come in [!UICONTROL Auto Personalization], [!UICONTROL Auto-Target], per impostazione predefinita, riserva parte del traffico dell&#39;attività come gruppo di controllo per misurare l&#39;incremento. Ai visitatori del gruppo di controllo viene messa a disposizione un&#39;esperienza casuale nell&#39;attività.

## Considerazioni

Ci sono alcune considerazioni importanti da tenere a mente quando si utilizza [!UICONTROL Auto-Target]:

* Impossibile passare un&#39;attività specifica da [!UICONTROL Auto-Target] a [!UICONTROL Automated Personalization] e viceversa.
* Non è possibile passare dall&#39;allocazione del traffico [!UICONTROL Manual] (tradizionale [!UICONTROL A/B Test]) a [!UICONTROL Auto-Target] e viceversa dopo il salvataggio come bozza di un&#39;attività.
* Un modello è progettato per identificare le prestazioni della strategia personalizzata rispetto al traffico servito in modo casuale rispetto all’invio di tutto il traffico all’esperienza vincente complessiva. Questo modello considera gli hit e le conversioni solo nell’ambiente predefinito.

  Il traffico proveniente da un secondo set di modelli viene generato per ciascun gruppo di modellazione (AP) o esperienza (AT). Per ciascuno di questi modelli, vengono considerati gli hit e le conversioni in tutti gli ambienti.

  Le richieste vengono gestite con lo stesso modello, indipendentemente dall’ambiente. Tuttavia, la pluralità di traffico deve provenire dall’ambiente predefinito per garantire che l’esperienza vincente complessiva identificata sia coerente con il comportamento reale.

* Utilizza almeno due esperienze.

## Terminologia  {#section_A309B7E0B258467789A5CACDC1D923F3}

I seguenti termini sono utili quando si parla di [!UICONTROL Auto-Target]:

| Termine | Definizione |
|---|---|
| [Slot machine](https://en.wikipedia.org/wiki/Multi-armed_bandit){target=_blank} | Un approccio slot machine per l&#39;ottimizzazione equilibra l&#39;apprendimento esplorativo e lo sfruttamento di tale apprendimento. |
| [Foresta casuale](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) | Foresta casuale è uno dei principali metodi di apprendimento automatico. Nel linguaggio della scienza dei dati, si tratta di una classificazione di gruppo, o metodo di regressione, che funziona costruendo molti alberi decisionali basati su visitatori e attributi di visita. In [!DNL Target], Foresta casuale viene utilizzato per determinare quale esperienza dovrebbe avere la più alta probabilità di conversione (o il più alto ricavo per visita) per ogni visitatore specifico. |
| [Campionamento Thompson](https://en.wikipedia.org/wiki/Thompson_sampling){target=_blank} | L’obiettivo del campionamento di Thompson è determinare quale esperienza è la migliore complessivamente (non personalizzata), riducendo al minimo il &quot;costo&quot; della ricerca di tale esperienza. Il campionamento di Thompson sceglie sempre un vincitore, anche se non c’è differenza statistica tra due esperienze. |

## Come funziona [!UICONTROL Auto-Target] {#section_77240E2DEB7D4CD89F52BE0A85E20136}

Per ulteriori informazioni sui dati e gli algoritmi sottostanti a [!UICONTROL Auto-Target] e [!UICONTROL Automated Personalization], visitare i collegamenti seguenti:

| Termine | Dettagli |
|--- |--- |
| [Algoritmo Foresta casuale](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) | L&#39;algoritmo di personalizzazione principale di [!DNL Target] utilizzato in [!UICONTROL Auto-Target] e [!UICONTROL Automated Personalization] è Foresta casuale. I metodi di raggruppamento, come Foresta casuale, utilizzano più algoritmi di apprendimento per ottenere prestazioni predittive migliori rispetto a quelle ottenibili da uno qualsiasi degli algoritmi di apprendimento costituenti. L&#39;algoritmo Foresta casuale nelle attività [!UICONTROL Automated Personalization] e [!UICONTROL Auto-Target] è una classificazione, o metodo di regressione, che funziona costruendo una moltitudine di alberi decisionali al momento dell&#39;addestramento. |
| [Caricamento dei dati per gli algoritmi Personalization di [!DNL Target]](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) | Esistono diversi modi per immettere i dati per i modelli [!UICONTROL Auto-Target] e [!UICONTROL Automated Personalization]. |
| [Raccolta di dati per gli algoritmi Personalization di [!DNL Target]](/help/main/c-activities/t-automated-personalization/ap-data.md) | Gli algoritmi di personalizzazione di [!DNL Target] raccolgono automaticamente vari dati. |

## Determinazione dell’allocazione del traffico {#section_AB3656F71D2D4C67A55A24B38092958F}

A seconda dell&#39;obiettivo dell&#39;attività, puoi scegliere una diversa allocaizone del traffico tra il controllo e le esperienze personalizzate. Una buona pratica è di determinare questo obiettivo prima di attivare l&#39;attività.

L&#39;elenco a discesa [!UICONTROL Custom Allocation] consente di scegliere tra le opzioni seguenti:

* [!UICONTROL Evaluate Personalization Algorithm (50/50)]
* [!UICONTROL Maximize Personalization Traffic (90/10)]
* [!UICONTROL Custom Allocation]

![Elenco a discesa Obiettivo di allocazione](/help/main/c-activities/assets/split-new-ui.png)

Nella tabella seguente vengono illustrate le tre opzioni disponibili:

| Obiettivo dell’attività | Allocazione del traffico consigliata | Compromessi |
|--- |--- |--- |
| **[!UICONTROL Evaluate Personalization Algorithm (50/50)]**: se l&#39;obiettivo è quello di testare l&#39;algoritmo, assegna il 50% dei visitatori all&#39;algoritmo di controllo e l&#39;altro 50% a quello di destinazione. Questa suddivisione fornisce la stima più accurata dell’incremento. Consigliato per l’utilizzo con &quot;esperienze casuali&quot; come controllo. | 50% al controllo / 50% all’esperienza personalizzata. | <ul><li>Massimizza la precisione dell&#39;incremento tra controllo e personalizzazione</li><li>Un numero relativamente basso di visitatori ha un’esperienza personalizzata</li></ul> |
| **[!UICONTROL Maximize Personalization Traffic (90/10)]**: se il tuo obiettivo è invece quello di creare un&#39;attività &quot;sempre attiva&quot;, inserisci il 10% dei visitatori nel controllo affinché ci siano abbastanza dati per consentire agli algoritmi di continuare a imparare nel tempo. In questo caso, il compromesso è che, in cambio della personalizzazione di una proporzione maggiore del traffico, si ha meno precisione in cosa sia l’incremento esatto. Indipendentemente dall’obiettivo, questa è la suddivisione del traffico consigliata quando si utilizza come controllo un’esperienza specifica. | Una buona pratica è quella di allocare 10%-30% al controllo / 70%-90% all’esperienza personalizzata | <ul><li>Massimizza il numero di visitatori che hanno un’esperienza personalizzata</li><li>Massimizza l&#39;incremento</li><li>Meno precisione nel determinare l&#39;incremento per l&#39;attività</li></ul> |
| **Personalizza allocazione** | Suddividi manualmente la percentuale come desiderato. | <ul><li>Potresti non ottenere i risultati desiderati. Se non sei sicuro, segui i suggerimenti per una delle opzioni precedenti</li></ul> |

Per regolare la percentuale di [!UICONTROL Control], fare clic su [!UICONTROL Experiences] nel riquadro [!UICONTROL Traffic Allocation], quindi modificare le percentuali come desiderato. Non è possibile ridurre il gruppo di controllo sotto il 10%.

Puoi [selezionare un’esperienza specifica da usare come controllo](/help/main/c-activities/t-automated-personalization/experience-as-control.md) oppure utilizzare l’opzione Esperienza casuale.

## Quando scegliere [!UICONTROL Auto-Target] rispetto a [!UICONTROL Automated Personalization]? {#section_BBC4871C87944DD7A8B925811A30C633}

Esistono diversi scenari in cui si preferisce utilizzare [!UICONTROL Auto-Target] rispetto a [!UICONTROL Automated Personalization]:

* Se vuoi definire l’intera esperienza anziché singole offerte che vengono combinate automaticamente per formare un’esperienza.
* Se desideri utilizzare il set completo di funzionalità [!UICONTROL Visual Experience Composer] (VEC) non supportate da [!UICONTROL Auto Personalization]: l&#39;editor di codice personalizzato, più tipi di pubblico e altro ancora.
* Se desideri apportare modifiche strutturali alla pagina in diverse esperienze. Se ad esempio si desidera ridisporre gli elementi nella home page, [!UICONTROL Auto-Target] è più appropriato da utilizzare rispetto a [!UICONTROL Automated Personalization].

## Cosa ha in comune [!UICONTROL Auto-Target] con [!UICONTROL Automated Personalization]? {#section_2A601F482F9A44E38D4B694668711319}

### L’algoritmo ottimizza per ottenere un risultato favorevole per ogni visita.

* L’algoritmo prevede che il visitatore sia propenso alla conversione (o ai ricavi stimati dalla conversione) per fornire l’esperienza migliore.
* Un visitatore è idoneo per una nuova esperienza al termine di una sessione esistente (a meno che il visitatore non appartenga al gruppo di controllo, nel qual caso l’esperienza che gli viene assegnata alla prima visita rimane invariata per le visite successive).
* All’interno di una sessione, la previsione non cambia, per mantenere la coerenza visiva.

### L’algoritmo si adatta ai cambiamenti nel comportamento del visitatore.

* La slot machine assicura che il modello &quot;spenda&quot; sempre una piccola frazione di traffico per continuare a imparare per tutta la vita dell&#39;attività di apprendimento e per prevenire un eccessivo sfruttamento delle tendenze apprese in precedenza.
* I modelli sottostanti vengono ricreati ogni 24 ore utilizzando i dati di comportamento dei visitatori più recenti per garantire che [!DNL Target] sfrutti sempre le preferenze dei visitatori in continua evoluzione.
* Se l&#39;algoritmo non può determinare le esperienze vincenti per i singoli visitatori, mostra automaticamente quella con i migliori risultati a livello generale, mentre continua a cercare vincitori personalizzati. L’esperienza che offre prestazioni migliori viene individuata tramite il [campione di Thompson](https://en.wikipedia.org/wiki/Thompson_sampling).

### L’algoritmo viene continuamente ottimizzato per una singola metrica di obiettivo.

* Questa metrica potrebbe essere basata sulla conversione o sui ricavi (nello specifico [!UICONTROL Revenue per Visit]).

### [!DNL Target] raccoglie automaticamente informazioni sui visitatori per generare i modelli di personalizzazione.

* Per ulteriori informazioni sui parametri utilizzati in [!UICONTROL Auto-Target] e [!UICONTROL Automated Personalization], vedere [Raccolta dati di Automated Personalization](/help/main/c-activities/t-automated-personalization/ap-data.md).

### [!DNL Target] utilizza automaticamente tutti i [!DNL Adobe Experience Cloud] tipi di pubblico condivisi per generare i modelli di personalizzazione.

* Non è necessario eseguire alcuna operazione specifica per aggiungere i tipi di pubblico al modello. Per informazioni sull’utilizzo di [!DNL Experience Cloud Audiences] con [!DNL Target], consulta [Audience di Experience Cloud](/help/main/c-integrating-target-with-mac/mmp.md).

### Gli addetti al marketing possono caricare dati offline, punteggi di propensione o altri dati personalizzati per creare modelli di personalizzazione.

* Ulteriori informazioni sul caricamento di [&#x200B; dati per [!UICONTROL Auto-Target] e [!UICONTROL Automated Personalization]](/help/main/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md).

## Differenze tra [!UICONTROL Auto-Target] e [!UICONTROL Automated Personalization] {#section_BA4D83BE40F14A96BE7CBC7C7CF2A8FB}

### [!UICONTROL Auto-Target] richiede spesso meno traffico di [!UICONTROL Automated Personalization] per generare un modello personalizzato.

Anche se la quantità di traffico *per esperienza* richiesta per la generazione dei modelli [!UICONTROL Auto-Target] o [!UICONTROL Auto Personalization] è la stessa, in genere sono presenti più esperienze in un&#39;attività [!UICONTROL Automated Personalization] rispetto a un&#39;attività [!UICONTROL Auto-Target].

Ad esempio, se disponessi di un&#39;attività [!UICONTROL Auto Personalization] in cui sono state create due offerte per posizione con due posizioni, ci sarebbero quattro (2 = 4) esperienze totali incluse nell&#39;attività (senza esclusioni). Utilizzando [!UICONTROL Auto-Target], puoi impostare l&#39;esperienza 1 per includere l&#39;offerta 1 in posizione 1 e l&#39;offerta 2 in posizione 2 e l&#39;esperienza 2 per includere l&#39;offerta 1 in posizione 1 e l&#39;offerta 2 in posizione 2. Poiché [!UICONTROL Auto-Target] consente di avere più modifiche all&#39;interno di un&#39;esperienza, puoi ridurre il numero di esperienze totali nell&#39;attività.

Per [!UICONTROL Auto-Target] è possibile utilizzare semplici regole generali per comprendere i requisiti del traffico:

* **Quando [!UICONTROL Conversion] è la metrica di successo:** 1.000 visite e almeno 50 conversioni al giorno per esperienza e inoltre l&#39;attività deve avere almeno 7.000 visite e 350 conversioni.
* **Quando [!UICONTROL Revenue per Visit] è la metrica di successo:** 1.000 visite e almeno 50 conversioni al giorno per esperienza e inoltre l&#39;attività deve avere almeno 1.000 conversioni per esperienza. RPV di solito richiede più dati per costruire modelli a causa della varianza più elevata dei dati che esiste in genere nei ricavi di visita rispetto al tasso di conversione.

### [!UICONTROL Auto-Target] ha una funzionalità di installazione completa.

* Poiché [!UICONTROL Auto-Target] è incorporato nel flusso di lavoro di attività A/B, [!UICONTROL Auto-Target] beneficia di [!UICONTROL Visual Experience Composer] (VEC) più maturo e completo. È inoltre possibile utilizzare [collegamenti di controllo qualità](/help/main/c-activities/c-activity-qa/activity-qa.md) con [!UICONTROL Auto-Target].

### [!UICONTROL Auto-Target] fornisce un ampio framework di test online.

* La slot machine fa parte di un framework di test online più ampio che consente a [!DNL Adobe] data scientist e ricercatori di comprendere i vantaggi dei continui miglioramenti delle condizioni reali.
* In futuro, questo banco di prova ci consentirà di aprire la piattaforma di apprendimento automatico [!DNL Adobe] ai client esperti in materia di dati in modo che possano inserire i propri modelli per incrementare i modelli [!DNL Target].

## Reporting e [!UICONTROL Auto-Target] {#section_42EE7F5E65E84F89A872FE9921917F76}

Per ulteriori informazioni, vedere [Reporting and Auto-Target](/help/main/c-activities/auto-target/reporting-and-auto-target.md).
