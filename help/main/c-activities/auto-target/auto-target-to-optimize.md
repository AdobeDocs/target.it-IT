---
keywords: targeting automatico;targeting;allocazione traffico;domande frequenti;faq;risoluzione dei problemi;risoluzione problemi
description: Scopri come [!UICONTROL Targeting automatico] attività in [!DNL Target] fornisce l’esperienza più personalizzata a ogni visitatore in base ai profili dei clienti e al comportamento di visitatori simili.
title: Cos’è un’ [!UICONTROL Targeting automatico] Attività?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Vedi cosa è incluso in Target Premium."
feature: Auto-Target
exl-id: 59ca30dc-45a0-4129-b832-84e1132d3b69
source-git-commit: 1b1b2271738d12f8da4e695900b70e280f50d8cf
workflow-type: tm+mt
source-wordcount: '1984'
ht-degree: 43%

---

# [!UICONTROL Panoramica del Targeting automatico]

[!UICONTROL Targeting automatico] attività in [!DNL Adobe Target] utilizza l’apprendimento automatico avanzato per scegliere tra più esperienze ad alte prestazioni definite dall’addetto al marketing per personalizzare i contenuti e favorire le conversioni. [!UICONTROL Targeting automatico] fornisce a ogni visitatore l’esperienza più personalizzata in base al suo profilo cliente individuale e al comportamento dei visitatori precedenti con profili simili.

>[!NOTE]
>
>* La funzione di [!UICONTROL Targeting automatico] è disponibile come parte della soluzione [!DNL Target Premium]. Questa funzione non è disponibile in [!DNL Target Standard] senza una licenza [!DNL Target Premium]. Per ulteriori informazioni sulle funzioni avanzate fornite da questa licenza, consulta [Target Premium](/help/main/c-intro/intro.md).
>
>* [!UICONTROL Analytics for Target] (A4T) supporta [!UICONTROL Targeting automatico] attività. Per ulteriori informazioni, consulta [Supporto di A4T per attività di allocazione automatica e targeting automatico](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md).

## Storia di successo nel mondo reale con l’utilizzo del Targeting automatico {#success}

Un grande rivenditore di abbigliamento ha recentemente utilizzato un [!UICONTROL Targeting automatico] attività con dieci esperienze basate su categorie di prodotti (più controllo randomizzato) per fornire il contenuto giusto a ogni visitatore. &quot;[!UICONTROL Aggiungi al carrello]&quot; è stato scelto come metrica di ottimizzazione primaria. Le esperienze mirate hanno avuto un incremento medio del 29,09%. Dopo aver generato [!UICONTROL Targeting automatico] modelli, l’attività era impostata su 90% di esperienze personalizzate.

In soli dieci giorni, è stato raggiunto un incremento di oltre 1.700.000 dollari.

Continua a leggere per imparare a utilizzare [!UICONTROL Targeting automatico] per aumentare l’incremento e i ricavi per la tua organizzazione.

## Panoramica {#section_972257739A2648AFA7E7556B693079C9}

Mentre [creazione di un’attività A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) utilizzando il flusso di lavoro guidato in tre passaggi, scegli **[!UICONTROL Targeting automatico per esperienze personalizzate]** opzione sul **[!UICONTROL Targeting]** pagina (passaggio 2).

![Opzione Targeting automatico per esperienze personalizzate](/help/main/c-activities/assets/auto-target-ui-new.png)

L’opzione di [!UICONTROL Targeting automatico] all’interno del flusso di attività A/B ti consente di sfruttare l’apprendimento automatico per personalizzare in base a una serie di esperienze definite dall’esperto di marketing in un clic. [!UICONTROL Targeting automatico] è progettato per fornire la massima ottimizzazione, rispetto ai tradizionali test A/B o [!UICONTROL Allocazione automatica], determinando quale esperienza visualizzare per ogni visitatore. A differenza di un’attività A/B in cui l’obiettivo è quello di trovare un singolo vincitore, [!UICONTROL Targeting automatico] determina automaticamente la migliore esperienza per un visitatore specifico. La migliore esperienza si basa sul profilo del visitatore e su altre informazioni contestuali, per fornire un’esperienza altamente personalizzata.

Simile a [!UICONTROL Automated Personalization], [!UICONTROL Targeting automatico] utilizza un [Algoritmo Foresta casuale](/help/main/c-activities/t-automated-personalization/algo-random-forest.md), uno dei principali metodi di raccolta di dati scientifici, per determinare l’esperienza migliore da mostrare a un visitatore. Perché [!UICONTROL Targeting automatico] può adattarsi ai cambiamenti nel comportamento del visitatore, può essere eseguito perennemente per fornire un incremento. Questo metodo è talvolta indicato come modalità &quot;sempre attiva&quot;.

A differenza di un’attività A/B in cui l’allocazione dell’esperienza per un determinato visitatore è definitiva, il [!UICONTROL Targeting automatico] ottimizza l’obiettivo di business specificato su ogni visita. Come nella [!UICONTROL Personalizzazione automatizzata], il [!UICONTROL Targeting automatico], per impostazione predefinita, riserva parte del traffico dell’attività come gruppo di controllo per misurare l’incremento. Ai visitatori del gruppo di controllo viene messa a disposizione un&#39;esperienza casuale nell&#39;attività.

## Considerazioni

Esistono alcune considerazioni importanti da tenere a mente quando si utilizza [!UICONTROL Targeting automatico]:

* Impossibile cambiare un’attività specifica da [!UICONTROL Targeting automatico] a [!UICONTROL Automated Personalization]e viceversa.
* Impossibile passare da [!UICONTROL Manuale] allocazione del traffico (tradizionale [!UICONTROL Test A/B]) a [!UICONTROL Targeting automatico]e, al contrario, dopo che un’attività è stata salvata come bozza.
* Un modello è progettato per identificare le prestazioni della strategia personalizzata rispetto al traffico servito in modo casuale rispetto all’invio di tutto il traffico all’esperienza vincente complessiva. Questo modello considera gli hit e le conversioni solo nell’ambiente predefinito.

  Il traffico proveniente da un secondo set di modelli viene generato per ciascun gruppo di modellazione (AP) o esperienza (AT). Per ciascuno di questi modelli, vengono considerati gli hit e le conversioni in tutti gli ambienti.

  Le richieste vengono distribuite con lo stesso modello, indipendentemente dall’ambiente, ma la pluralità di traffico deve provenire dall’ambiente predefinito per garantire che l’esperienza vincente complessiva identificata sia coerente con il comportamento reale.

* Utilizza almeno due esperienze.

## Terminologia  {#section_A309B7E0B258467789A5CACDC1D923F3}

I seguenti termini sono utili quando si parla di [!UICONTROL Targeting automatico]:

| Termine | Definizione |
|---|---|
| [Slot machine](https://en.wikipedia.org/wiki/Multi-armed_bandit){target=_blank} | Un approccio slot machine per l&#39;ottimizzazione equilibra l&#39;apprendimento esplorativo e lo sfruttamento di tale apprendimento. |
| [Foresta casuale](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) | Foresta casuale è uno dei principali metodi di apprendimento automatico. Nel linguaggio della scienza dei dati, si tratta di una classificazione di gruppo, o metodo di regressione, che funziona costruendo molti alberi decisionali basati su visitatori e attributi di visita. Entro [!DNL Target], Foresta casuale viene utilizzato per determinare quale esperienza dovrebbe avere la più alta probabilità di conversione (o il più alto ricavo per visita) per ogni visitatore specifico. |
| [Campionamento di Thompson](https://en.wikipedia.org/wiki/Thompson_sampling){target=_blank} | L’obiettivo del campionamento di Thompson è determinare quale esperienza è la migliore complessivamente (non personalizzata), riducendo al minimo il &quot;costo&quot; della ricerca di tale esperienza. Il campionamento di Thompson sceglie sempre un vincitore, anche in assenza di differenza statistica tra due esperienze. |

## Funzionamento di [!UICONTROL Targeting automatico] {#section_77240E2DEB7D4CD89F52BE0A85E20136}

Di seguito sono disponibili collegamenti a ulteriori informazioni sui dati e gli algoritmi di base di [!UICONTROL Targeting automatico] e Personalizzazione automatizzata:

| Termine | Dettagli |
|--- |--- |
| [Algoritmo Foresta casuale](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) | [!DNL Target]dell’algoritmo di personalizzazione principale utilizzato in entrambi [!UICONTROL Targeting automatico] e [!UICONTROL Automated Personalization] è Foresta casuale. I metodi di raggruppamento, come Foresta casuale, utilizzano più algoritmi di apprendimento per ottenere prestazioni predittive migliori rispetto a quelle ottenibili da uno qualsiasi degli algoritmi di apprendimento costituenti. Algoritmo Foresta casuale in [!UICONTROL Automated Personalization] e [!UICONTROL Targeting automatico] le attività sono una classificazione, o metodo di regressione, che opera costruendo una moltitudine di alberi decisionali al momento della formazione. |
| [Caricamento dati per [!DNL Target]Algoritmi di personalizzazione di](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) | Esistono diversi modi per immettere i dati per i modelli di [!UICONTROL Targeting automatico] e personalizzazione automatizzata. |
| [Raccolta dati per [!DNL Target]Algoritmi di personalizzazione di](/help/main/c-activities/t-automated-personalization/ap-data.md) | [!DNL Target]Gli algoritmi di personalizzazione di raccolgono automaticamente vari dati. |

## Determinazione dell’allocazione del traffico {#section_AB3656F71D2D4C67A55A24B38092958F}

A seconda dell&#39;obiettivo dell&#39;attività, puoi scegliere una diversa allocaizone del traffico tra il controllo e le esperienze personalizzate. Una buona pratica è di determinare questo obiettivo prima di attivare l&#39;attività.

L’elenco a discesa [!UICONTROL Personalizza allocazione] consente di scegliere tra le seguenti opzioni:

* [!UICONTROL Valuta l&#39;algoritmo di personalizzazione]
* [!UICONTROL Massimizza traffico di personalizzazione]
* [!UICONTROL Personalizza allocazione]

![Elenco a discesa Obiettivo di allocazione](/help/main/c-activities/assets/split-new.png)

| Obiettivo dell’attività | Allocazione del traffico consigliata | Compromessi |
|--- |--- |--- |
| **Valuta algoritmo di personalizzazione (50/50)**: se l’obiettivo è quello di testare l’algoritmo, assegna il 50% dei visitatori all’algoritmo di controllo e l’altro 50% a quello di destinazione. Questa suddivisione fornisce la stima più accurata dell’incremento. Consigliato per l’utilizzo con &quot;esperienze casuali&quot; come controllo. | 50% al controllo / 50% all’esperienza personalizzata. | <ul><li>Massimizza la precisione dell&#39;incremento tra controllo e personalizzazione</li><li>Un numero relativamente basso di visitatori ha un’esperienza personalizzata</li></ul> |
| **Massimizza traffico personalizzazione (90/10)**: se il tuo obiettivo è invece quello di creare un’attività &quot;sempre attiva&quot;, inserisci il 10% dei visitatori nel controllo affinché ci siano abbastanza dati per consentire agli algoritmi di continuare a imparare nel tempo. In questo caso, il compromesso è che, in cambio della personalizzazione di una proporzione maggiore del traffico, si ha meno precisione in cosa sia l’incremento esatto. Indipendentemente dall’obiettivo, questa è la suddivisione del traffico consigliata quando si utilizza come controllo un’esperienza specifica. | Una buona pratica è quella di allocare 10%-30% al controllo / 70%-90% all’esperienza personalizzata | <ul><li>Massimizza il numero di visitatori che ricevono un&#39;esperienza personalizzata</li><li>Massimizza l&#39;incremento</li><li>Meno precisione nel determinare l&#39;incremento per l&#39;attività</li></ul> |
| **Personalizza allocazione** | Suddividi manualmente la percentuale come desiderato. | <ul><li>Potresti non ottenere i risultati desiderati. Se non sei sicuro, segui i suggerimenti per una delle opzioni precedenti</li></ul> |

Per regolare [!UICONTROL Controllo] percentuale, fai clic sulle icone nella [!UICONTROL Allocazione] colonna. Non è possibile ridurre il gruppo di controllo sotto il 10%.

![Cambiare l’allocazione del traffico per Targeting automatico](/help/main/c-activities/assets/auto-target-control.png)

Puoi [selezionare un’esperienza specifica da usare come controllo](/help/main/c-activities/t-automated-personalization/experience-as-control.md) oppure utilizzare l’opzione Esperienza casuale.

## Quando scegliere il [!UICONTROL Targeting automatico][!UICONTROL  rispetto alla Personalizzazione automatizzata]? {#section_BBC4871C87944DD7A8B925811A30C633}

Esistono diversi scenari in cui si preferisce utilizzare [!UICONTROL Targeting automatico] oltre [!UICONTROL Automated Personalization]:

* Se vuoi definire l’intera esperienza anziché singole offerte che vengono combinate automaticamente per formare un’esperienza.
* Se desideri utilizzare il set completo di [!UICONTROL Compositore esperienza visivo] Funzioni di (VEC) non supportate da [!UICONTROL Personalizzazione automatica]: editor di codice personalizzato, più tipi di pubblico e altro ancora.
* Se desideri apportare modifiche strutturali alla pagina in diverse esperienze. Ad esempio, per ridisporre gli elementi nella home page, [!UICONTROL Targeting automatico] è più appropriato da utilizzare rispetto a [!UICONTROL Automated Personalization].

## Che cosa fa [!UICONTROL Targeting automatico] hanno in comune con [!UICONTROL Automated Personalization]? {#section_2A601F482F9A44E38D4B694668711319}

### L&#39;algoritmo è ottimizzato per ottenere un risultato favorevole per ogni visita.

* L’algoritmo prevede che il visitatore sia propenso alla conversione (o ai ricavi stimati dalla conversione) per fornire l’esperienza migliore.
* Un visitatore è idoneo per una nuova esperienza al termine di una sessione esistente (a meno che il visitatore non appartenga al gruppo di controllo, nel qual caso l’esperienza assegnata al visitatore alla prima visita rimane invariata per le visite successive).
* All’interno di una sessione, la previsione non cambia, per mantenere la coerenza visiva.

### L&#39;algoritmo si adatta alle modifiche nel comportamento dei visitatori.

* La slot machine assicura che il modello &quot;spenda&quot; sempre una piccola frazione di traffico per continuare a imparare per tutta la vita dell&#39;attività di apprendimento e per prevenire un eccessivo sfruttamento delle tendenze apprese in precedenza.
* I modelli sottostanti vengono ricreati ogni 24 ore utilizzando i dati di comportamento dei visitatori più recenti per garantire che [!DNL Target] sfrutta sempre la modifica delle preferenze del visitatore.
* Se l&#39;algoritmo non può determinare le esperienze vincenti per i singoli visitatori, mostra automaticamente quella con i migliori risultati a livello generale, mentre continua a cercare vincitori personalizzati. L’esperienza che offre prestazioni migliori viene individuata tramite il [campione di Thompson](https://en.wikipedia.org/wiki/Thompson_sampling).

### L’algoritmo esegue l’ottimizzazione continua per una singola metrica dell’obiettivo.

* Questa metrica potrebbe essere basata sulla conversione o sui ricavi (nello specifico [!UICONTROL Ricavo per visita]).

### [!DNL Target] raccoglie automaticamente informazioni sui visitatori per generare modelli di personalizzazione.

* Per ulteriori informazioni sui parametri utilizzati in [!UICONTROL Targeting automatico] e Personalizzazione automatizzata, consulta [Raccolta dati di Personalizzazione automatizzata](/help/main/c-activities/t-automated-personalization/ap-data.md).

### [!DNL Target] utilizza automaticamente tutti i tipi di [!DNL Adobe Experience Cloud] pubblico di condivisi, per generare i modelli di personalizzazione.

* Non è necessario eseguire alcuna operazione specifica per aggiungere i tipi di pubblico al modello. Per informazioni sull’utilizzo di [!DNL Experience Cloud Audiences] con [!DNL Target], consulta [Audience di Experience Cloud](/help/main/c-integrating-target-with-mac/mmp.md).

### Gli addetti al marketing possono caricare dati offline, punteggi di propensione o altri dati personalizzati per creare modelli di personalizzazione.

* Ulteriori informazioni sul [caricamento di dati per il Targeting automatico la Personalizzazione automatizzata[!UICONTROL .]](/help/main/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md)

## Quali sono le differenze tra il [!UICONTROL Targeting automatico][!UICONTROL  e la Personalizzazione automatizzata]? {#section_BA4D83BE40F14A96BE7CBC7C7CF2A8FB}

### [!UICONTROL Il Targeting automatico] richiede spesso meno traffico rispetto alla Personalizzazione automatizzata per generare un modello personalizzato.

Anche se la quantità di traffico *per esperienza* richiesta per la generazione dei modelli di [!UICONTROL Targeting automatico] o [!UICONTROL Personalizzazione automatizzata] è la stessa, ci sono di solito più esperienze in un&#39;attività di Personalizzazione automatizzata di un&#39;attività di [!UICONTROL Targeting automatico.]

Ad esempio, se è stato [!UICONTROL Personalizzazione automatica] attività in cui hai creato due offerte per posizione con due posizioni, ci sarebbero quattro (2 = 4) esperienze totali incluse nell’attività (senza esclusioni). Tramite il [!UICONTROL Targeting automatico] puoi impostare l’esperienza 1 per includere l’offerta 1 in posizione 1 e l’offerta 2 in posizione 2 e l’esperienza 2 per includere l’offerta 1 in posizione 1 e l’offerta 2 in posizione 2. Poiché il [!UICONTROL Targeting automatico] consente di avere più modifiche all’interno di un’esperienza, puoi ridurre il numero di esperienze totali nell’attività.

Per il [!UICONTROL Targeting automatico] è possibile utilizzare semplici regole generali per comprendere i requisiti del traffico:

* **Quando la Conversione è la metrica di successo:** 1.000 visite e almeno 50 conversioni al giorno per esperienza e in più l&#39;attività deve avere almeno 7.000 visite e 350 conversioni.
* **Quando il Ricavo per visita è la metrica di successo:** 1.000 visite e almeno 50 conversioni al giorno per esperienza e in più l&#39;attività deve avere almeno 1.000 conversioni per esperienza. RPV di solito richiede più dati per costruire modelli a causa della varianza più elevata dei dati che esiste in genere nei ricavi di visita rispetto al tasso di conversione.

### [!UICONTROL Il Targeting automatico] ha una funzionalità di installazione completa.

* Perché [!UICONTROL Targeting automatico] è incorporato nel flusso di lavoro di attività A/B, [!UICONTROL Targeting automatico] benefici di un&#39;organizzazione più matura e completa [!UICONTROL Compositore esperienza visivo] (VEC). Puoi anche utilizzare [Collegamenti QA](/help/main/c-activities/c-activity-qa/activity-qa.md) con [!UICONTROL Targeting automatico].

### [!UICONTROL Il Targeting automatico] fornisce un ampio framework di test online.

* La slot machine fa parte di un framework di test online più ampio che consente [!DNL Adobe] ai data scientist e ai ricercatori di comprendere i vantaggi dei loro continui miglioramenti delle condizioni reali.
* In futuro, questo banco di prova ci permetterà di aprire [!DNL Adobe] piattaforma di apprendimento automatico per client esperti di dati in modo che possano importare i propri modelli per aumentare il [!DNL Target] modelli.

## Creazione di rapporti e [!UICONTROL Targeting automatico] {#section_42EE7F5E65E84F89A872FE9921917F76}

Per ulteriori informazioni, consulta [Reporting e Targeting automatico](/help/main/c-activities/auto-target/reporting-and-auto-target.md).

## Video di formazione: Informazioni sulle attività di Targeting automatico

Questo video spiega come configurare un’attività di [!UICONTROL Targeting automatico] A/B.

Dopo aver completato questo training, sarai in grado di:

* Definire il test di [!UICONTROL Targeting automatico]
* Confrontare e contrastare il [!UICONTROL Targeting automatico][!UICONTROL  con la Personalizzazione automatizzata]
* Creare attività di [!UICONTROL Targeting automatico]

>[!VIDEO](https://video.tv.adobe.com/v/18558)
