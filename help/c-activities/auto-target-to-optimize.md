---
keywords: auto-target;targeting;traffic allocation;frequently aske questions;faq;troubleshooting;trouble shooting
title: Targeting automatico
topic: Standard
uuid: fce769d2-9e7f-4064-add7-76e1fc394b4f
translation-type: tm+mt
source-git-commit: 4695dbf2ecbd19be5589bfc63e2d947361d77fce
workflow-type: tm+mt
source-wordcount: '3517'
ht-degree: 91%

---


# ![PREMIUM](/help/assets/premium.png) Targeting automatico{#auto-target}

La funzione [!UICONTROL Targeting automatico] utilizza un apprendimento automatico avanzato per scegliere tra più esperienze definite dall’addetto al marketing al fine di personalizzare il contenuto e stimolare le conversioni. La funzione Targeting automatico consegna a ogni visitatore l’esperienza più personalizzata in base al suo profilo cliente e al comportamento dei visitatori precedenti con profili simili.

>[!NOTE]
>
>La funzione di [!UICONTROL Targeting automatico] è disponibile come parte della soluzione [!DNL Target Premium]. Questa funzione non è disponibile in [!DNL Target Standard] senza una licenza [!DNL Target Premium]. Per ulteriori informazioni sulle funzioni avanzate fornite da questa licenza, consulta [Target Premium](/help/c-intro/intro.md).

Durante la [creazione di un’attività A/B tramite il flusso di lavoro guidato in tre passaggi](../c-activities/t-test-ab/t-test-create-ab/test-create-ab.md#task_68C8079BF9FF4625A3BD6680D554BB72), è possibile scegliere di allocare il traffico utilizzando l’opzione [!UICONTROL Targeting automatico per esperienze personalizzate]:

![Opzione Targeting automatico per esperienze personalizzate](/help/c-activities/assets/auto-target-ui-new.png)

## Panoramica {#section_972257739A2648AFA7E7556B693079C9}

L’opzione di [!UICONTROL Targeting automatico] all’interno del flusso di attività A/B ti consente di sfruttare l’apprendimento automatico per personalizzare in base a una serie di esperienze definite dall’esperto di marketing in un clic. [!UICONTROL La funzionalità di Targeting automatico] è progettata per fornire la massima ottimizzazione, rispetto ai tradizionali test A/B o Allocazione automatica, determinando quale esperienza visualizzare per ogni visitatore. A differenza di un’attività A/B in cui la finalità è quella di trovare un singolo vincitore, il [!UICONTROL Targeting automatico] determina automaticamente la migliore esperienza per uno specifico visitatore (in base al suo profilo e altre informazioni contestuali) per fornire un’esperienza altamente personalizzata.

Similmente alla Personalizzazione automatizzata, il [!UICONTROL Targeting automatico] utilizza un algoritmo di Foresta casuale, uno dei principali metodi di raccolta di dati scientifici, per determinare l’esperienza migliore da mostrare ad un visitatore. Il [!UICONTROL Targeting automatico] è adattabile ai cambiamenti nel comportamento del visitatore, perciò può essere eseguito perennemente per fornire un incremento. Questo a volte è indicato come modalità “sempre attiva”.

A differenza di un’attività A/B in cui l’allocazione dell’esperienza per un determinato visitatore è definitiva, il [!UICONTROL Targeting automatico] ottimizza l’obiettivo di business specificato su ogni visita. Come nella [!UICONTROL Personalizzazione automatizzata], il [!UICONTROL Targeting automatico], per impostazione predefinita, riserva parte del traffico dell’attività come gruppo di controllo per misurare l’incremento. Ai visitatori del gruppo di controllo viene messa a disposizione un&#39;esperienza casuale nell&#39;attività.

## Considerazioni

There are a few important considerations to keep in mind when using [!UICONTROL Auto-Target]:

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
| Foresta casuale | Foresta casuale è uno dei principali metodi di apprendimento automatico. In termini di scienza dei dati, è una classificazione d raccolta, o metodo di regressione, che funziona costruendo un gran numero di alberi decisionali sulla base di visitatori e attributi di visita. In Target, l’algoritmo Foresta casuale determina quale esperienza possa avere la più alta probabilità di conversione (o il più alto ricavo per visita) per ogni visitatore specifico. Per ulteriori informazioni sulla foresta casuale in Target, consulta [Algoritmo Foresta casuale](../c-activities/t-automated-personalization/algo-random-forest.md#concept_48F3CDAA16A848D2A84CDCD19DAAE3AA). |
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

**L&#39;algoritmo non supporta[!DNL Analytics]come origine di dati o come endpoint per la generazione di rapporti.**

**Target raccoglie automaticamente informazioni sui visitatori per generare modelli di personalizzazione.**

* Per ulteriori informazioni sui parametri utilizzati in [!UICONTROL Targeting automatico] e Personalizzazione automatizzata, consulta [Raccolta dati di Personalizzazione automatizzata](../c-activities/t-automated-personalization/ap-data.md#reference_255BD3DE7AD04DC9B766E0BC78961058).

**Target utilizza automaticamente tutti i tipi di pubblico di Experience Cloud condivisi, per generare i modelli di personalizzazione.**

* Non è necessario eseguire alcuna operazione specifica per aggiungere i tipi di pubblico al modello. Per informazioni sull’utilizzo dei tipi di pubblico di Experience Cloud con Target, consulta [Experience Cloud Audiences](../c-integrating-target-with-mac/mmp.md#concept_F4863DE4C92D4805AB690B4B3D487969)

**Gli addetti al marketing possono caricare dati offline, punteggi di propensione o altri dati personalizzati per creare modelli di personalizzazione.**

* Ulteriori informazioni sul [caricamento di dati per il Targeting automatico la Personalizzazione automatizzata](../c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md#concept_85EA505B37E54514A1C8AB91553FEED6).

## Quali sono le differenze tra il [!UICONTROL Targeting automatico] e la Personalizzazione automatizzata? {#section_BA4D83BE40F14A96BE7CBC7C7CF2A8FB}

**[!UICONTROL Il Targeting automatico]richiede spesso meno traffico rispetto alla Personalizzazione automatizzata per generare un modello personalizzato.**

Anche se la quantità di traffico *per esperienza* richiesta per la generazione dei modelli di [!UICONTROL Targeting automatico] o [!UICONTROL Personalizzazione automatizzata] è la stessa, ci sono di solito più esperienze in un&#39;attività di Personalizzazione automatizzata di un&#39;attività di [!UICONTROL Targeting automatico]. Ad esempio, se disponessi di un’attività di [!UICONTROL Personalizzazione automatizzata] in cui sono state create due offerte per posizione con due posizioni, ci sarebbero quattro (2 = 4) esperienze totali incluse nell’attività (senza esclusioni). Tramite il [!UICONTROL Targeting automatico] puoi impostare l’esperienza 1 per includere l’offerta 1 in posizione 1 e l’offerta 2 in posizione 2 e l’esperienza 2 per includere l’offerta 1 in posizione 1 e l’offerta 2 in posizione 2. Poiché il [!UICONTROL Targeting automatico] consente di avere più modifiche all’interno di un’esperienza, puoi ridurre il numero di esperienze totali nell’attività.

Per il [!UICONTROL Targeting automatico] è possibile utilizzare semplici regole generali per comprendere i requisiti del traffico:

* **Quando la Conversione è la metrica di successo:** 1.000 visite e almeno 50 conversioni al giorno per esperienza e in più l&#39;attività deve avere almeno 7.000 visite e 350 conversioni.
* **Quando il Ricavo per visita è la metrica di successo:** 1.000 visite e almeno 50 conversioni al giorno per esperienza e in più l&#39;attività deve avere almeno 1.000 conversioni per esperienza. RPV di solito richiede più dati per costruire modelli a causa della varianza più elevata dei dati che esiste in genere nei ricavi di visita rispetto al tasso di conversione.

**[!UICONTROL Il Targeting automatico]ha una funzionalità di installazione completa.**

* Poiché è incorporato nel flusso di lavoro di attività A/B, il [!UICONTROL Targeting automatico] beneficia di un Compositore esperienza visivo molto maturo e completo.  Puoi anche sfruttare i [collegamenti di controllo qualità](../c-activities/c-activity-qa/activity-qa.md#concept_9329EF33DE7D41CA9815C8115DBC4E40) con il [!UICONTROL Targeting automatico].

**[!UICONTROL Il Targeting automatico]fornisce un ampio framework di test online.**

* La slot machine è parte di un quadro più ampio di test online che permette ai nostri scienziati e ricercatori di dati di comprendere i benefici dei loro continui miglioramenti nelle condizioni del mondo reale.
* In futuro, questo banco di prova ci permetterà di aprire la nostra piattaforma di apprendimento automatico per i nostri clienti esperti di dati in modo che possano portare i propri modelli per aumentare i modelli di Target.

## Creazione di rapporti e [!UICONTROL Targeting automatico] {#section_42EE7F5E65E84F89A872FE9921917F76}

Per ulteriori informazioni, consulta [Rapporto di riepilogo del Targeting automatico](../c-reports/auto-target-summary-report.md#concept_E2171F7B57C1417DAAD7E7909A3FB073) nella sezione [Rapporti](../c-reports/reports.md#concept_B5077F5503AA4C98901AA99EDCE6CDE6).

## Domande frequenti sul Targeting automatico {#section_5C120A2B11D14D9BAF767BBAB50FED23}

Consultate le seguenti domande frequenti e risposte mentre lavorate con le attività [!UICONTROL Auto-Target] :

### Quali sono le procedure consigliate per impostare un’attività di [!UICONTROL Targeting automatico]?

* Decidi se il valore aziendale di una metrica di uccesso di un Ricavo per visita (RPV) vale i requisiti di traffico aggiuntivi. RPV richiede in genere almeno 1.000 conversioni per esperienza perché un&#39;attività funzioni rispetto alla conversione.
* In base ai tuoi obiettivi, decidi la ripartizione tra il controllo e le esperienze personalizzate prima di iniziare l&#39;attività.
* Determina se disponi di traffico sufficiente per la pagina in cui l’attività di [!UICONTROL Targeting automatico] verrà eseguita affinché i modelli di personalizzazione compilino in un tempo ragionevole.
   * Se stai sopttoponendo a test l&#39;algoritmo di personalizzazione, non è consigliabile modificare le esperienze o aggiungere/rimuovere attributi di profilo mentre l&#39;attività è in esecuzione.

* È consigliabile completare un’attività A/B tra le offerte e le posizioni che prevedi di utilizzare nell’attività di [!UICONTROL Targeting automatico] per garantire che le posizioni e le offerte abbiano un impatto sull’obiettivo di ottimizzazione. Se un’attività A/B non riesce a dimostrare una differenza significativa, il [!UICONTROL Targeting automatico] probabilmente non riuscirà a generare incrementi.

   * Se un test A/B non mostra differenze statisticamente significative tra le esperienze, probabilmente le offerte che stai prendendo in considerazione non sono sufficientemente diverse tra loro, le posizioni selezionate non incidono sulla metrica successo o l&#39;obiettivo di ottimizzazione è troppo lontano nell&#39;imbuto di conversione per essere influenzato dalle offerte scelte.

* Cerca di non apportare modifiche sostanziali alle esperienze durante il corso dell&#39;attività.

### Se l&#39;intervallo di date del rapporto cambia, i segni di spunta che indicano che un modello è stato generato per l&#39;esperienza si aggiornano?

No, i segni di spunta per la generazione di modelli mostrano solo i modelli generati fino ad ora. Non c&#39;è modo di tornare indietro e vedere quando è stato completato un modello.

### Se un visitatore non vede l’attività di [!UICONTROL Targeting automatico] e converte, la conversione conta nella mia attività?

No, solo i visitatori che si qualificano e visualizzano l’attività di [!UICONTROL Targeting automatico] sono conteggiati nella creazione dei rapporti.

### La mia attività di [!UICONTROL Targeting automatico] non sembra generare alcun incremento. Cosa succede? 

Ci sono quattro fattori necessari affinché un’attività di [!UICONTROL Targeting automatico] generi incremento:

* Le offerte devono essere abbastanza diverse per influenzare i visitatori.
* Le Offerte devono essere tali da poter influenzare l’obiettivo di ottimizzazione.
* Il test deve avere traffico e potenza statistica tali da consentire il rilevamento di un incremento.
* L’algoritmo di personalizzazione deve funzionare bene.

La migliore linea di azione è di assicurarsi in primo luogo che i contenuti e le posizioni, che compongono le esperienze di attività, facciano davvero una differenza per i tassi di risposta generali tramite un semplice test A/B e non personalizzato. Calcola le dimensioni del campione in tempo per assicurarti che sia possibile visualizzare un incremento ragionevole ed esegui il test A/B per una durata fissa senza interruzioni né modifiche.

Se i risultati di test A/B mostrano un incremento statisticamente significativo su una o più esperienze, può funzionare un&#39;attività personalizzata. Naturalmente, la personalizzazione può funzionare anche se non ci sono differenze nei tassi di risposta complessiva delle esperienze. Il problema, solitamente, deriva dalle offerte/posizioni che non hanno un impatto sull’obiettivo di ottimizzazione tale da poter essere rilevato con rilevanza statistica.

### Quando devo interrompere l’attività di [!UICONTROL Targeting automatico]?

Il [!UICONTROL Targeting automatico] può essere utilizzato come personalizzazione “sempre attiva” che si ottimizza costantemente. Soprattutto per i contenuti fissi, non è necessario arrestare l’attività di [!UICONTROL Targeting automatico].

Se desideri apportare modifiche sostanziali al contenuto nell’attività di [!UICONTROL Targeting automatico], la procedura consigliata consiste nell’avviare una nuova attività in modo che gli altri utenti che revisionano i rapporti non confondano o riferiscano i risultati passati con contenuti diversi.

### Quanto tempo devo aspettare per la generazione dei modelli?

Il periodo di tempo necessario alla generazione dei modelli nell’attività di [!UICONTROL Targeting automatico] dipende in genere dal traffico delle posizioni dell’attività selezionate e dalla metrica di successo dell’attività.

Per il [!UICONTROL Targeting automatico] è possibile utilizzare semplici regole generali per comprendere i requisiti del traffico:

* **Quando la Conversione è la metrica di successo:** 1.000 visite e almeno 50 conversioni al giorno per esperienza e in più l&#39;attività deve avere almeno 7.000 visite e 350 conversioni.
* **Quando il Ricavo per visita è la metrica di successo:** 1.000 visite e almeno 50 conversioni al giorno per esperienza e in più l&#39;attività deve avere almeno 1.000 conversioni per esperienza. RPV di solito richiede più dati per costruire modelli a causa della varianza più elevata dei dati che esiste in genere nei ricavi di visita rispetto al tasso di conversione.

### L’attività contiene un modello generato. Le visite a quell’esperienza sono personalizzate? 

No, per iniziare la personalizzazione occorrono almeno due modelli generati nell’attività.

### Quando posso iniziare a esaminare i risultati della mia attività di [!UICONTROL Targeting automatico]?

Puoi iniziare a esaminare i risultati dei test di [!UICONTROL Targeting automatico] quando disponi di almeno due esperienze con modelli generati (segno di spunta verde) nell’attività che presenta modelli generati.

### Posso specificare un’esperienza particolare da usare come controllo?

Puoi selezionare un’esperienza da usare come controllo durante la creazione di un’attività [Personalizzazione automatizzata](/help/c-activities/t-automated-personalization/automated-personalization.md) oppure [Targeting automatico](/help/c-activities/auto-target-to-optimize.md).

Questa funzione ti permette di indirizzare tutto il traffico di controllo a una specifica esperienza, in base alla percentuale di allocazione del traffico configurata nell’attività. Puoi quindi valutare i rapporti sulle prestazioni del traffico personalizzato rispetto al traffico verso l’esperienza di controllo.

Per ulteriori informazioni, consulta [Utilizzare un’esperienza specifica come controllo](/help/c-activities/t-automated-personalization/experience-as-control.md).

### Posso cambiare la metrica obiettivo a metà strada attraverso un&#39;attività di Auto-Target? {#change-metric}

Non è consigliabile modificare la metrica obiettivo a metà di un&#39;attività. Anche se è possibile modificare la metrica dell&#39;obiettivo durante un&#39;attività utilizzando l&#39; [!DNL Target] interfaccia utente, è sempre necessario avviare una nuova attività. Non garantiamo cosa accade se si modifica la metrica di obiettivo in un&#39;attività dopo che è in esecuzione.

Questa raccomandazione si applica alle attività [!UICONTROL Auto-Allocate], [!UICONTROL Auto-Target]e [!UICONTROL Automated Personalization] che utilizzano [!DNL Target] o [!DNL Analytics] (A4T) come origine di reporting.

### È possibile utilizzare l&#39;opzione Reimposta dati rapporto durante l&#39;esecuzione di un&#39;attività di Target automatico?

Non è consigliabile utilizzare l&#39;opzione [!UICONTROL Ripristina dati] rapporto per le attività [!UICONTROL Auto-Target] . Anche se rimuove i dati di reporting visibili, questa opzione non rimuove tutti i record di formazione dal modello [!UICONTROL Auto-Target] . Invece di utilizzare l&#39;opzione [!UICONTROL Ripristina dati] rapporto per le attività di Target  automatico, create una nuova attività e disattivate l&#39;attività originale. (Nota: Questa guida si applica anche alle attività [!UICONTROL Auto-Allocate] e [!UICONTROL Automated Personalization] .

## Risoluzione dei problemi di [!UICONTROL Targeting automatico] {#section_23995AB813F24525AF294D20A20875C8}

A volte le attività non vanno come previsto. Di seguito sono elencate alcune potenziali sfide che potresti affrontare durante l’utilizzo del [!UICONTROL Targeting automatico] e alcune soluzioni suggerite.

**La mia attività di[!UICONTROL Targeting automatico]sta impiegando troppo tempo per generare i modelli.**

Sono disponibili diverse modifiche dell’impostazione dell’attività che possono ridurre il tempo previsto per la generazione di modelli, tra cui il numero di esperienze nell’attività di [!UICONTROL Targeting automatico], il traffico verso il sito e la metrica di successo selezionata.

**Soluzione:** esamina l’impostazione dell’attività e verifica se ci sono modifiche che intendi apportare per migliorare la velocità con cui i modelli vengono generati.

* Se la metrica di successo è impostata su RPV, è possibile modificare la conversione? Le attività di conversione tendono a richiedere meno traffico per la generazione dei modelli. Non perderai i dati di attività se modifichi la metrica di successo da RPV a conversione.
* La metrica del successo è molto in basso nel funnel di vendita dalle esperienze dell’attività? Con un tasso di conversione basso, la generazione dei modelli richiederà più traffico poiché è necessario un numero minimo di conversioni.
* È possibile eliminare alcune esperienze dall’attività? Diminuendo il numero di esperienze, diminuirà anche il tempo necessario alla generazione dei modelli.
* Esiste una pagina con traffico più alto in cui questa attività avrebbe più successo? Maggiori sono il traffico e le conversioni nelle posizioni dell’attività, più rapidamente verranno generati i modelli.

**La mia attività di[!UICONTROL Targeting automatico]non genera alcun incremento.**

Ci sono quattro fattori necessari affinché un’attività di Personalizzazione automatizzata generi incremento:

* Le offerte devono essere abbastanza diverse per influenzare i visitatori.
* Le Offerte devono essere tali da poter influenzare l’obiettivo di ottimizzazione.
* Il test deve avere traffico e potenza statistica tali da consentire il rilevamento di un incremento.
* L’algoritmo di personalizzazione deve funzionare bene.

**Soluzione:** in primo luogo, assicurati che l&#39;attività personalizzi il traffico. Se i modelli non sono generati per tutte le esperienze, l’attività di [!UICONTROL Targeting automatico] fornisce ancora in modo casuale una parte significativa di visite per tentare di generare tutti i modelli il più rapidamente possibile. Se i modelli non sono generati, il [!UICONTROL Targeting automatico] non personalizza il traffico.

Quindi, assicurati che le offerte e le posizioni di attività facciano realmente la differenza nei tassi di risposta complessiva tramite un semplice test A/B non personalizzato. Calcola le dimensioni del campione in tempo per assicurarti che sia possibile visualizzare un incremento ragionevole ed esegui il test A/B per una durata fissa senza interruzioni né modifiche. Se i risultati di un test A/B mostrano un incremento statisticamente significativo su una o più esperienze, è probabile che un’attività personalizzata funzioni. Naturalmente, la personalizzazione può funzionare anche se non ci sono differenze nei tassi di risposta complessiva delle esperienze. Il problema, solitamente, deriva dalle offerte/posizioni che non hanno un impatto sull’obiettivo di ottimizzazione tale da poter essere rilevato con rilevanza statistica.

**Qualsiasi metrica dipendente dalla metrica di conversione non consegue mai la conversione.**

Si tratta di un comportamento previsto.

In un’attività di [!UICONTROL Targeting automatico], una volta conseguita la conversione per una metrica di conversione (che si tratti di obiettivo di ottimizzazione o di corrispondenza), l’utente viene rilasciato dall’esperienza e l’attività viene riavviata.

Prendiamo ad esempio un’attività con una metrica di conversione (C1) e una metrica aggiuntiva (A1). A1 dipende da C1. Quando un visitatore accede all’attività per la prima volta e i criteri di conversione per A1 e C1 non vengono soddisfatti, la metrica A1 non consegue la conversione a causa della dipendenza dalla metrica di successo. Se il visitatore consegue la conversione per C1 e poi per A1, la conversione A1 non risulta perché, non appena ottenuta la conversione per C1, il visitatore viene rilasciato.

## Video di formazione: Informazioni sulle attività di Targeting automatico ![badge Panoramica](/help/assets/overview.png)

Questo video spiega come configurare un’attività di [!UICONTROL Targeting automatico] A/B.

Dopo aver completato questo training, sarai in grado di:

* Definire il test di [!UICONTROL Targeting automatico]
* Confrontare e contrastare il [!UICONTROL Targeting automatico] con la Personalizzazione automatizzata
* Creare attività di [!UICONTROL Targeting automatico]

>[!VIDEO](https://video.tv.adobe.com/v/18558)