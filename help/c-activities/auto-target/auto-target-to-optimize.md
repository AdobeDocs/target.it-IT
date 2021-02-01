---
keywords: auto-target;targeting;traffic allocation;frequently aske questions;faq;troubleshooting;trouble shooting
description: Il targeting automatico in  Adobe Target utilizza l'apprendimento automatico avanzato per selezionare tra più esperienze definite dall'esperto di marketing ad alte prestazioni per personalizzare i contenuti e stimolare le conversioni. La funzione Targeting automatico consegna a ogni visitatore l’esperienza più personalizzata in base al suo profilo cliente e al comportamento dei visitatori precedenti con profili simili.
title: Panoramica di AutoTarget
feature: Auto-Target
translation-type: tm+mt
source-git-commit: 95e2ed4d9ca22e18b91533365624bcc001d09c34
workflow-type: tm+mt
source-wordcount: '2016'
ht-degree: 85%

---


# ![Panoramica di ](/help/assets/premium.png) PREMIUMAuto-Target

[!UICONTROL Le attività di ] targeting automatico in  Adobe Target utilizzano l&#39;apprendimento automatico avanzato per selezionare tra più esperienze definite dagli esperti di marketing ad alte prestazioni per personalizzare i contenuti e stimolare le conversioni. La funzione Targeting automatico consegna a ogni visitatore l’esperienza più personalizzata in base al suo profilo cliente e al comportamento dei visitatori precedenti con profili simili.

>[!NOTE]
>
>La funzione di [!UICONTROL Targeting automatico] è disponibile come parte della soluzione [!DNL Target Premium]. Questa funzione non è disponibile in [!DNL Target Standard] senza una licenza [!DNL Target Premium]. Per ulteriori informazioni sulle funzioni avanzate fornite da questa licenza, consulta [Target Premium](/help/c-intro/intro.md).
>
>[!UICONTROL Analytics for Target] (A4T) supporta le attività  [!UICONTROL Auto-] Target. Per ulteriori informazioni, consultate [A4T support for Auto-Allocate and Auto-Target activity](/help/c-integrating-target-with-mac/a4t/a4t-at-aa.md) (Supporto per l&#39;allocazione automatica e la destinazione automatica).

## Successo reale utilizzando Auto-Target {#success}

Un importante rivenditore di abbigliamento ha recentemente utilizzato un&#39;attività [!UICONTROL Auto-Target] con dieci esperienze basate su categorie di prodotti (più controllo casuale) per fornire il contenuto giusto a ogni visitatore. &quot;[!UICONTROL Aggiungi al carrello]&quot; è stata scelta come metrica di ottimizzazione principale. Le esperienze mirate hanno registrato un incremento medio del 29,09%. Dopo aver creato i modelli [!UICONTROL Auto-Target], l&#39;attività è stata impostata su 90% esperienze personalizzate.

In soli dieci giorni, è stato raggiunto più di 1.700.000 dollari in incremento.

Continua a leggere per apprendere come utilizzare [!UICONTROL Auto-Target] per aumentare l&#39;incremento e le entrate per la tua organizzazione.

## Panoramica {#section_972257739A2648AFA7E7556B693079C9}

Durante la [creazione di un’attività A/B tramite il flusso di lavoro guidato in tre passaggi](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md), è possibile scegliere di allocare il traffico utilizzando l’opzione [!UICONTROL Targeting automatico per esperienze personalizzate]:

![Opzione Targeting automatico per esperienze personalizzate](/help/c-activities/assets/auto-target-ui-new.png)

L’opzione di [!UICONTROL Targeting automatico] all’interno del flusso di attività A/B ti consente di sfruttare l’apprendimento automatico per personalizzare in base a una serie di esperienze definite dall’esperto di marketing in un clic. [!UICONTROL La funzionalità di Targeting automatico] è progettata per fornire la massima ottimizzazione, rispetto ai tradizionali test A/B o Allocazione automatica, determinando quale esperienza visualizzare per ogni visitatore. A differenza di un’attività A/B in cui la finalità è quella di trovare un singolo vincitore, il [!UICONTROL Targeting automatico] determina automaticamente la migliore esperienza per uno specifico visitatore (in base al suo profilo e altre informazioni contestuali) per fornire un’esperienza altamente personalizzata.

Similmente alla Personalizzazione automatizzata, il [!UICONTROL Targeting automatico] utilizza un algoritmo di Foresta casuale, uno dei principali metodi di raccolta di dati scientifici, per determinare l’esperienza migliore da mostrare ad un visitatore. Il [!UICONTROL Targeting automatico] è adattabile ai cambiamenti nel comportamento del visitatore, perciò può essere eseguito perennemente per fornire un incremento. Questo a volte è indicato come modalità “sempre attiva”.

A differenza di un’attività A/B in cui l’allocazione dell’esperienza per un determinato visitatore è definitiva, il [!UICONTROL Targeting automatico] ottimizza l’obiettivo di business specificato su ogni visita. Come nella [!UICONTROL Personalizzazione automatizzata], il [!UICONTROL Targeting automatico], per impostazione predefinita, riserva parte del traffico dell’attività come gruppo di controllo per misurare l’incremento. Ai visitatori del gruppo di controllo viene messa a disposizione un&#39;esperienza casuale nell&#39;attività.

## Considerazioni

Quando si utilizza [!UICONTROL Auto-Target] è necessario tenere presenti alcune considerazioni importanti:

* Non puoi passare un’attività specifica dal [!UICONTROL Targeting automatico] alla Personalizzazione automatizzata e viceversa.
* Non puoi passare dall’Allocazione manuale del traffico (test A/B tradizionale) al [!UICONTROL Targeting automatico] e viceversa durante un’attività in corso.
* Un modello è costruito per identificare le prestazioni della strategia personalizzata rispetto al traffico servito in modo casuale rispetto all&#39;invio di tutto il traffico all&#39;esperienza vincente complessiva. Questo modello considera gli hit e le conversioni solo nell’ambiente predefinito.

   Il traffico da un secondo set di modelli è costruito per ciascun gruppo di modellazione (AP) o esperienza (AT). Per ciascuno di questi modelli, vengono presi in considerazione hit e conversioni in tutti gli ambienti.

   Le richieste saranno quindi servite con lo stesso modello, indipendentemente dall&#39;ambiente, ma la pluralità di traffico dovrebbe provenire dall&#39;ambiente predefinito per garantire che l&#39;esperienza vincente complessiva identificata sia coerente con il comportamento del mondo reale.

* Sono necessarie un minimo di due esperienze.

## Terminologia {#section_A309B7E0B258467789A5CACDC1D923F3}

I seguenti termini sono utili quando si parla di [!UICONTROL Targeting automatico]:

| Termine | Definizione |
|---|---|
| Slot machine | Un approccio slot machine per l&#39;ottimizzazione equilibra l&#39;apprendimento esplorativo e lo sfruttamento di tale apprendimento. |
| Foresta casuale | Foresta casuale è uno dei principali metodi di apprendimento automatico. In termini di scienza dei dati, è una classificazione d raccolta, o metodo di regressione, che funziona costruendo un gran numero di alberi decisionali sulla base di visitatori e attributi di visita. In Target, l’algoritmo Foresta casuale determina quale esperienza possa avere la più alta probabilità di conversione (o il più alto ricavo per visita) per ogni visitatore specifico. Per ulteriori informazioni sulla foresta casuale in Target, consulta [Algoritmo Foresta casuale](/help/c-activities/t-automated-personalization/algo-random-forest.md). |
| Campionamento di Thompson | L’obiettivo del campionamento di Thompson è quello di determinare quale esperienza è la migliore complessivamente (non personalizzata), minimizzando il “costo” della ricerca dell’esperienza. Il campionamento di Thompson sceglie sempre un vincitore, anche in assenza di differenza statistica tra due esperienze. Per ulteriori informazioni, consulta [Campionamento di Thompson](https://en.wikipedia.org/wiki/Thompson_sampling). |

## Funzionamento di [!UICONTROL Targeting automatico] {#section_77240E2DEB7D4CD89F52BE0A85E20136}

Di seguito sono disponibili collegamenti a ulteriori informazioni sui dati e gli algoritmi di base di [!UICONTROL Targeting automatico] e Personalizzazione automatizzata:

| Termine | Dettagli |
|--- |--- |
| [Algoritmo Foresta casuale](/help/c-activities/t-automated-personalization/algo-random-forest.md) | L’algoritmo di personalizzazione principale di Target utilizzato sia nel [!UICONTROL Targeting automatico] sia nella Personalizzazione automatizzata è quello di Foresta casuale. I metodi di raggruppamento come Foresta casuale si basano su più algoritmi di apprendimento per ottenere prestazioni predittive migliori rispetto agli algoritmi di apprendimento costituenti. L&#39;algoritmo Foresta casuale nel sistema di personalizzazione automatizzata è un metodo di classificazione o regressione che si basa sulla costruzione di un elevato numero di alberi decisionali durante la fase di apprendimento. |
| [Caricamento di dati per gli algoritmi di personalizzazione di Target](/help/c-activities/t-automated-personalization/algo-random-forest.md) | Esistono diversi modi per immettere i dati per i modelli di [!UICONTROL Targeting automatico] e personalizzazione automatizzata. |
| [Raccolta di dati per gli algoritmi di personalizzazione di Target](/help/c-activities/t-automated-personalization/ap-data.md) | Gli algoritmi di personalizzazione di Target raccolgono automaticamente una varietà di dati. |

## Determinazione dell’allocazione del traffico {#section_AB3656F71D2D4C67A55A24B38092958F}

A seconda dell&#39;obiettivo dell&#39;attività, puoi scegliere una diversa allocaizone del traffico tra il controllo e le esperienze personalizzate. Una buona pratica è di determinare questo obiettivo prima di attivare l&#39;attività.

L’elenco a discesa [!UICONTROL Personalizza allocazione] consente di scegliere tra le seguenti opzioni:

* Valuta l&#39;algoritmo di personalizzazione
* Massimizza traffico di personalizzazione
* Personalizza allocazione

![Elenco a discesa Obiettivo di allocazione](/help/c-activities/assets/split-new.png)

| Obiettivo dell’attività | Allocazione del traffico consigliata | Compromessi |
|--- |--- |--- |
| **Valuta algoritmo di personalizzazione (50/50)**: se l’obiettivo è quello di testare l’algoritmo, assegna il 50% dei visitatori all’algoritmo di controllo e l’altro 50% a quello di destinazione. Questa suddivisione fornisce la stima più accurata dell’incremento. È consigliata quando il controllo è impostato su “Esperienze casuali”. | 50% al controllo / 50% all’esperienza personalizzata. | <ul><li>Massimizza la precisione dell&#39;incremento tra controllo e personalizzazione</li><li>Un numero relativamente inferiore di visitatori avrà un&#39;esperienza personalizzata</li></ul> |
| **Massimizza traffico personalizzazione (90/10)**: se il tuo obiettivo è invece quello di creare un’attività “sempre attiva”, inserisci il 10% dei visitatori nel controllo affinché ci siano abbastanza dati per consentire agli algoritmi di continuare a imparare nel tempo. In questo caso, considera che la personalizzazione di una proporzione maggiore del traffico va a scapito della precisione nell’incremento rilevato. Indipendentemente dall’obiettivo, questa è la suddivisione del traffico consigliata quando si utilizza come controllo un’esperienza specifica. | Una buona pratica è quella di allocare 10%-30% al controllo / 70%-90% all’esperienza personalizzata | <ul><li>Massimizza il numero di visitatori che ricevono un&#39;esperienza personalizzata</li><li>Massimizza l&#39;incremento</li><li>Meno precisione nel determinare l&#39;incremento per l&#39;attività</li></ul> |
| **Personalizza allocazione** | Suddividi manualmente la percentuale come desiderato. | <ul><li>Potresti non ottenere i risultati desiderati. Se non sei sicuro, segui i suggerimenti per una delle opzioni precedenti</li></ul> |

Per regolare la percentuale di controllo, fai clic sulle icone nella colonna Allocazione. Non è possibile ridurre il gruppo di controllo sotto il 10%.

![Cambiare l’allocazione del traffico per Targeting automatico](/help/c-activities/assets/auto-target-control.png)

Puoi [selezionare un’esperienza specifica da usare come controllo](/help/c-activities/t-automated-personalization/experience-as-control.md) oppure utilizzare l’opzione Esperienza casuale.

## Quando scegliere il [!UICONTROL Targeting automatico] rispetto alla Personalizzazione automatizzata? {#section_BBC4871C87944DD7A8B925811A30C633}

Esistono diversi scenari in cui si preferisce il [!UICONTROL Targeting automatico] rispetto alla Personalizzazione automatizzata:

* Se vuoi definire l&#39;intera esperienza spetto alle singole offerte, queste verranno combinate automaticamente per formare un&#39;esperienza.
* Se desideri sfruttare l’insieme completo di funzioni del Compositore esperienza visivo non supportate dalla [!UICONTROL Personalizzazione automatizzata]: l’editor di codice personalizzato, più tipi di pubblico e altro ancora.
* Se desideri apportare modifiche strutturali alla pagina in diverse esperienze. Ad esempio, per riorganizzare l’ordine degli elementi nella pagina principale, il [!UICONTROL Targeting automatico] sarebbe più appropriato da utilizzare rispetto alla Personalizzazione automatizzata.

## Che cosa hanno in comune il [!UICONTROL Targeting automatico] e la Personalizzazione automatizzata? {#section_2A601F482F9A44E38D4B694668711319}

**L&#39;algoritmo è ottimizzato per ottenere un risultato favorevole per ogni visita.**

* L&#39;algoritmo prevede la propensione di un visitatore per la conversione (o i ricavi stimati dalla conversione) al fine di offrire la migliore esperienza.
* Un visitatore ha diritto a una nuova esperienza al termine di una sessione esistente (a meno che il visitatore sia nel gruppo di controllo, nel qual caso l&#39;esperienza a cui il visitatore è assegnato sulla sua prima visita rimane la stessa per le visite successive).
* All&#39;interno di una sessione, la stima non cambia, per mantenere la coerenza visiva.

**L&#39;algoritmo si adatta alle modifiche nel comportamento dei visitatori.**

* La slot machine assicura che il modello “spenda” sempre una piccola frazione di traffico per continuare ad apprendere per tutta la durata dell&#39;attività di apprendimento e per prevenire lo sfruttamento eccessivo delle tendenze precedentemente apprese.
* I modelli sottostanti vengono rigenerati ogni 24 ore utilizzando i dati di comportamento dei visitatori più recenti per garantire che Target sfrutti sempre le preferenze mutevoli dei visitatori.
* Se l&#39;algoritmo non può determinare le esperienze vincenti per i singoli visitatori, mostra automaticamente quella con i migliori risultati a livello generale, mentre continua a cercare vincitori personalizzati. L’esperienza che offre prestazioni migliori viene individuata tramite il [campione di Thompson](https://en.wikipedia.org/wiki/Thompson_sampling).

**L’algoritmo esegue l’ottimizzazione continua per una singola metrica dell’obiettivo.**

* Questa metrica potrebbe essere basata sulla conversione o i ricavi (più specificamente ricavi per visita).

**Target raccoglie automaticamente informazioni sui visitatori per generare modelli di personalizzazione.**

* Per ulteriori informazioni sui parametri utilizzati in [!UICONTROL Targeting automatico] e Personalizzazione automatizzata, consulta [Raccolta dati di Personalizzazione automatizzata](/help/c-activities/t-automated-personalization/ap-data.md).

**Target utilizza automaticamente tutti i tipi di pubblico di Experience Cloud condivisi, per generare i modelli di personalizzazione.**

* Non è necessario eseguire alcuna operazione specifica per aggiungere i tipi di pubblico al modello. Per informazioni sull’utilizzo dei tipi di pubblico di Experience Cloud con Target, consulta [Experience Cloud Audiences](/help/c-integrating-target-with-mac/mmp.md)

**Gli addetti al marketing possono caricare dati offline, punteggi di propensione o altri dati personalizzati per creare modelli di personalizzazione.**

* Ulteriori informazioni sul [caricamento di dati per il Targeting automatico la Personalizzazione automatizzata](/help/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md).

## Quali sono le differenze tra il [!UICONTROL Targeting automatico] e la Personalizzazione automatizzata? {#section_BA4D83BE40F14A96BE7CBC7C7CF2A8FB}

**[!UICONTROL Il Targeting automatico] richiede spesso meno traffico rispetto alla Personalizzazione automatizzata per generare un modello personalizzato.**

Anche se la quantità di traffico *per esperienza* richiesta per la generazione dei modelli di [!UICONTROL Targeting automatico] o [!UICONTROL Personalizzazione automatizzata] è la stessa, ci sono di solito più esperienze in un&#39;attività di Personalizzazione automatizzata di un&#39;attività di [!UICONTROL Targeting automatico]. Ad esempio, se disponessi di un’attività di [!UICONTROL Personalizzazione automatizzata] in cui sono state create due offerte per posizione con due posizioni, ci sarebbero quattro (2 = 4) esperienze totali incluse nell’attività (senza esclusioni). Tramite il [!UICONTROL Targeting automatico] puoi impostare l’esperienza 1 per includere l’offerta 1 in posizione 1 e l’offerta 2 in posizione 2 e l’esperienza 2 per includere l’offerta 1 in posizione 1 e l’offerta 2 in posizione 2. Poiché il [!UICONTROL Targeting automatico] consente di avere più modifiche all’interno di un’esperienza, puoi ridurre il numero di esperienze totali nell’attività.

Per il [!UICONTROL Targeting automatico] è possibile utilizzare semplici regole generali per comprendere i requisiti del traffico:

* **Quando la Conversione è la metrica di successo:** 1.000 visite e almeno 50 conversioni al giorno per esperienza e in più l&#39;attività deve avere almeno 7.000 visite e 350 conversioni.
* **Quando il Ricavo per visita è la metrica di successo:** 1.000 visite e almeno 50 conversioni al giorno per esperienza e in più l&#39;attività deve avere almeno 1.000 conversioni per esperienza. RPV di solito richiede più dati per costruire modelli a causa della varianza più elevata dei dati che esiste in genere nei ricavi di visita rispetto al tasso di conversione.

**[!UICONTROL Il Targeting automatico] ha una funzionalità di installazione completa.**

* Poiché è incorporato nel flusso di lavoro di attività A/B, il [!UICONTROL Targeting automatico] beneficia di un Compositore esperienza visivo molto maturo e completo.  Puoi anche sfruttare i [collegamenti di controllo qualità](/help/c-activities/c-activity-qa/activity-qa.md) con il [!UICONTROL Targeting automatico].

**[!UICONTROL Il Targeting automatico] fornisce un ampio framework di test online.**

* La slot machine è parte di un quadro più ampio di test online che permette ai nostri scienziati e ricercatori di dati di comprendere i benefici dei loro continui miglioramenti nelle condizioni del mondo reale.
* In futuro, questo banco di prova ci permetterà di aprire la nostra piattaforma di apprendimento automatico per i nostri clienti esperti di dati in modo che possano portare i propri modelli per aumentare i modelli di Target.

## Creazione di rapporti e [!UICONTROL Targeting automatico] {#section_42EE7F5E65E84F89A872FE9921917F76}

Per ulteriori informazioni, consulta [Rapporto di riepilogo del Targeting automatico](/help/c-reports/auto-target-summary-report.md) nella sezione [Rapporti](/help/c-reports/reports.md).

## Video di formazione: Informazioni sulle attività di targeting automatico ![badge Panoramica](/help/assets/overview.png)

Questo video spiega come configurare un’attività di [!UICONTROL Targeting automatico] A/B.

Dopo aver completato questo training, sarai in grado di:

* Definire il test di [!UICONTROL Targeting automatico]
* Confrontare e contrastare il [!UICONTROL Targeting automatico] con la Personalizzazione automatizzata
* Creare attività di [!UICONTROL Targeting automatico]

>[!VIDEO](https://video.tv.adobe.com/v/18558)