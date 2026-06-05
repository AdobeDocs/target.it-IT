---
keywords: targeting automatico;targeting;allocazione traffico;domande frequenti;faq;risoluzione dei problemi;risoluzione problemi
description: Scopri in che modo un’attività di [!UICONTROL Targeting automatico] fornisce l’esperienza più personalizzata a ogni visitatore in base ai profili del cliente e al comportamento di visitatori simili.
title: Cos'è un'attività di [!UICONTROL Targeting automatico]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Auto-Target
exl-id: 59ca30dc-45a0-4129-b832-84e1132d3b69
TQID: https://experienceleague.adobe.com/uKmfIlOcT-tZgOjuvERXuif-Y5-2Jw3prtPbuBjv1is
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
subfeature_v2:
  - id: fff07a91-d479-45f4-ae95-9762e79b1b7c
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: c467f629596b37c334276d6f095f19b639a8518d
workflow-type: tm+mt
source-wordcount: 2157
ht-degree: 18%

---

# Panoramica di [!UICONTROL Targeting automatico]

Le attività di [!UICONTROL Targeting automatico] in [!DNL Adobe Target] utilizzano l&#39;apprendimento automatico avanzato per scegliere tra più esperienze ad alte prestazioni definite dall&#39;addetto al marketing per personalizzare i contenuti e favorire le conversioni. [!UICONTROL Targeting automatico] fornisce l&#39;esperienza più personalizzata a ogni visitatore in base al suo profilo cliente individuale e al comportamento dei visitatori precedenti con profili simili.

>[!NOTE]
>
>* [!UICONTROL Targeting automatico] è disponibile come parte della soluzione [!DNL Target Premium]. Questa funzione non è disponibile in [!DNL Target Standard] senza una licenza [!DNL Target Premium]. Per ulteriori informazioni sulle funzioni avanzate fornite da questa licenza, consulta [Target Premium](/help/main/c-intro/intro.md).
>
>* [!UICONTROL Analytics for Target] (A4T) supporta [!UICONTROL le attività Targeting automatico]. Per ulteriori informazioni, consulta [Supporto A4T per attività di allocazione automatica e targeting automatico](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md).

## Storia di successo nel mondo reale con l’utilizzo del Targeting automatico {#success}

Un importante retailer di abbigliamento ha recentemente utilizzato un&#39;attività [!UICONTROL Targeting automatico] con dieci esperienze basate su categorie di prodotti (più controllo randomizzato) per fornire il contenuto giusto a ogni visitatore. &quot;[!UICONTROL Aggiungi al carrello]&quot; è stato scelto come metrica di ottimizzazione primaria. Le esperienze mirate hanno avuto un incremento medio del 29,09%. Dopo aver generato i modelli [!UICONTROL Targeting automatico], l&#39;attività è stata impostata sul 90% di esperienze personalizzate.

In soli dieci giorni, è stato raggiunto un incremento di oltre 1.700.000 dollari.

Continua a leggere per scoprire come utilizzare [!UICONTROL Targeting automatico] per aumentare gli incrementi e i ricavi per la tua organizzazione.

## Panoramica {#section_972257739A2648AFA7E7556B693079C9}

Durante la [creazione di un&#39;attività A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) tramite il flusso di lavoro guidato in tre passaggi, scegli l&#39;opzione **[!UICONTROL Targeting automatico per esperienze personalizzate]** nella pagina **[!UICONTROL Targeting]** (passaggio 2).

![Impostazioni del metodo di allocazione traffico](/help/main/c-activities/automated-traffic-allocation/assets/auto-target.png)

L&#39;opzione [!UICONTROL Targeting automatico] all&#39;interno del flusso di attività A/B ti consente di sfruttare l&#39;apprendimento automatico per personalizzare in base a una serie di esperienze definite dall&#39;addetto al marketing in un clic. [!UICONTROL Targeting automatico] è progettato per fornire la massima ottimizzazione, rispetto ai tradizionali test A/B o [!UICONTROL Allocazione automatica], determinando quale esperienza visualizzare per ogni visitatore. A differenza di un&#39;attività A/B in cui l&#39;obiettivo è quello di trovare un singolo vincitore, [!UICONTROL Targeting automatico] determina automaticamente la migliore esperienza per un visitatore specifico. La migliore esperienza si basa sul profilo del visitatore e su altre informazioni contestuali, per fornire un’esperienza altamente personalizzata.

Analogamente a [!UICONTROL Automated Personalization], [!UICONTROL Targeting automatico] utilizza un algoritmo [Foresta casuale](/help/main/c-activities/t-automated-personalization/algo-random-forest.md), uno dei principali metodi di raccolta di dati scientifici, per determinare l&#39;esperienza migliore da mostrare a un visitatore. Poiché [!UICONTROL Targeting automatico] può adattarsi ai cambiamenti nel comportamento del visitatore, può essere eseguito perennemente per fornire un incremento. Questo metodo è talvolta indicato come modalità &quot;sempre attiva&quot;.

A differenza di un&#39;attività A/B in cui l&#39;allocazione dell&#39;esperienza per un dato visitatore è definitiva, [!UICONTROL Targeting automatico] ottimizza l&#39;obiettivo di business specificato su ogni visita. Come in [!UICONTROL Auto Personalization], [!UICONTROL Targeting automatico], per impostazione predefinita, riserva parte del traffico dell&#39;attività come gruppo di controllo per misurare l&#39;incremento. Ai visitatori del gruppo di controllo viene messa a disposizione un&#39;esperienza casuale nell&#39;attività.

## Considerazioni

Ci sono alcune considerazioni importanti da tenere a mente quando si utilizza [!UICONTROL Targeting automatico]:

* Presta attenzione alla forma dell’attività. Le prestazioni dipendono più dal numero di posizioni × offerte che dal conteggio delle esperienze non elaborate. Le grandi combinazioni cartesiane possono rallentare il caricamento e la modifica nel [!UICONTROL Compositore esperienza visivo], anche al di sotto dei limiti di esperienza documentati.

  Come best practice, mantieni [!UICONTROL le attività Targeting automatico] e [!UICONTROL Automated Personalization] in 4-6 posizioni con 4-6 offerte per posizione. Configurazioni più grandi non sono consigliate. Poiché queste attività vengono create direttamente nel passaggio [!UICONTROL Esperienze], l&#39;interfaccia utente [!DNL Target] potrebbe visualizzare avvisi in linea o bloccare il salvataggio quando la configurazione supera le soglie supportate.

* Non puoi cambiare un&#39;attività specifica da [!UICONTROL Targeting automatico] a [!UICONTROL Automated Personalization] e viceversa.
* Non puoi passare dall&#39;allocazione del traffico [!UICONTROL Manuale] (test [!UICONTROL A/B tradizionale]) a [!UICONTROL Targeting automatico] e viceversa dopo che un&#39;attività è stata salvata come bozza.
* Un modello è progettato per identificare le prestazioni della strategia personalizzata rispetto al traffico servito in modo casuale rispetto all’invio di tutto il traffico all’esperienza vincente complessiva. Questo modello considera gli hit e le conversioni solo nell’ambiente predefinito.

  Il traffico proveniente da un secondo set di modelli viene generato per ciascun gruppo di modellazione (AP) o esperienza (AT). Per ciascuno di questi modelli, vengono considerati gli hit e le conversioni in tutti gli ambienti.

  Le richieste vengono gestite con lo stesso modello, indipendentemente dall’ambiente. Tuttavia, la pluralità di traffico deve provenire dall’ambiente predefinito per garantire che l’esperienza vincente complessiva identificata sia coerente con il comportamento reale.

* Utilizza almeno due esperienze.

## Terminologia {#section_A309B7E0B258467789A5CACDC1D923F3}

I seguenti termini sono utili quando si parla di [!UICONTROL Targeting automatico]:

| Termine | Definizione |
|---|---|
| [Slot machine](https://en.wikipedia.org/wiki/Multi-armed_bandit){target=_blank} | Un approccio slot machine per l&#39;ottimizzazione equilibra l&#39;apprendimento esplorativo e lo sfruttamento di tale apprendimento. |
| [Foresta casuale](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) | Foresta casuale è uno dei principali metodi di apprendimento automatico. Nel linguaggio della scienza dei dati, si tratta di una classificazione di gruppo, o metodo di regressione, che funziona costruendo molti alberi decisionali basati su visitatori e attributi di visita. In [!DNL Target], Foresta casuale viene utilizzato per determinare quale esperienza dovrebbe avere la più alta probabilità di conversione (o il più alto ricavo per visita) per ogni visitatore specifico. |
| [Campionamento Thompson](https://en.wikipedia.org/wiki/Thompson_sampling){target=_blank} | L’obiettivo del campionamento di Thompson è determinare quale esperienza è la migliore complessivamente (non personalizzata), riducendo al minimo il &quot;costo&quot; della ricerca di tale esperienza. Il campionamento di Thompson sceglie sempre un vincitore, anche in assenza di differenza statistica tra due esperienze. |

## Funzionamento di [!UICONTROL Targeting automatico] {#section_77240E2DEB7D4CD89F52BE0A85E20136}

Ulteriori informazioni sui dati e gli algoritmi sottostanti [!UICONTROL Targeting automatico] e [!UICONTROL Automated Personalization] sono disponibili ai collegamenti seguenti:

| Termine | Dettagli |
|--- |--- |
| [Algoritmo Foresta casuale](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) | L&#39;algoritmo di personalizzazione principale di [!DNL Target] utilizzato in [!UICONTROL Targeting automatico] e [!UICONTROL Automated Personalization] è Foresta casuale. I metodi di raggruppamento, come Foresta casuale, utilizzano più algoritmi di apprendimento per ottenere prestazioni predittive migliori rispetto a quelle ottenibili da uno qualsiasi degli algoritmi di apprendimento costituenti. L&#39;algoritmo Foresta casuale nelle attività [!UICONTROL Automated Personalization] e [!UICONTROL Targeting automatico] è una classificazione, o metodo di regressione, che funziona costruendo una moltitudine di alberi decisionali al momento della formazione. |
| [Caricamento dei dati per gli algoritmi Personalization di [!DNL Target]](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) | Esistono diversi modi per immettere dati per i modelli [!UICONTROL Targeting automatico] e [!UICONTROL Automated Personalization]. |
| [Raccolta di dati per gli algoritmi Personalization di [!DNL Target]](/help/main/c-activities/t-automated-personalization/ap-data.md) | Gli algoritmi di personalizzazione di [!DNL Target] raccolgono automaticamente vari dati. |

## Determinazione dell’allocazione del traffico {#section_AB3656F71D2D4C67A55A24B38092958F}

A seconda dell&#39;obiettivo dell&#39;attività, puoi scegliere una diversa allocaizone del traffico tra il controllo e le esperienze personalizzate. Una buona pratica è di determinare questo obiettivo prima di attivare l&#39;attività.

L’elenco a discesa [!UICONTROL Personalizza allocazione] consente di scegliere tra le seguenti opzioni:

* [!UICONTROL Valuta algoritmo Personalization (50/50)]
* [!UICONTROL Massimizza traffico Personalization (90/10)]
* [!UICONTROL Personalizza allocazione]

![Elenco a discesa Obiettivo di allocazione](/help/main/c-activities/assets/split-new-ui.png)

Nella tabella seguente vengono illustrate le tre opzioni disponibili:

| Obiettivo dell’attività | Allocazione del traffico consigliata | Compromessi |
|--- |--- |--- |
| **[!UICONTROL Valuta algoritmo di personalizzazione (50/50)]**: se l’obiettivo è quello di testare l’algoritmo, assegna il 50% dei visitatori all’algoritmo di controllo e l’altro 50% a quello di destinazione. Questa suddivisione fornisce la stima più accurata dell’incremento. Consigliato per l’utilizzo con &quot;esperienze casuali&quot; come controllo. | 50% al controllo / 50% all’esperienza personalizzata. | <ul><li>Massimizza la precisione dell&#39;incremento tra controllo e personalizzazione</li><li>Un numero relativamente basso di visitatori ha un’esperienza personalizzata</li></ul> |
| **[!UICONTROL Massimizza traffico Personalization (90/10)]**: se il tuo obiettivo è invece quello di creare un&#39;attività &quot;sempre attiva&quot;, inserisci il 10% dei visitatori nel controllo affinché ci siano abbastanza dati per consentire agli algoritmi di continuare a imparare nel tempo. In questo caso, il compromesso è che, in cambio della personalizzazione di una proporzione maggiore del traffico, si ha meno precisione in cosa sia l’incremento esatto. Indipendentemente dall’obiettivo, questa è la suddivisione del traffico consigliata quando si utilizza come controllo un’esperienza specifica. | Una buona pratica è quella di allocare 10%-30% al controllo / 70%-90% all’esperienza personalizzata | <ul><li>Massimizza il numero di visitatori che hanno un’esperienza personalizzata</li><li>Massimizza l&#39;incremento</li><li>Meno precisione nel determinare l&#39;incremento per l&#39;attività</li></ul> |
| **Personalizza allocazione** | Suddividi manualmente la percentuale come desiderato. | <ul><li>Potresti non ottenere i risultati desiderati. Se non sei sicuro, segui i suggerimenti per una delle opzioni precedenti</li></ul> |

Per regolare la percentuale di [!UICONTROL controllo], fai clic su [!UICONTROL Esperienze] nel riquadro [!UICONTROL Allocazione traffico], quindi regola le percentuali come desiderato. Non è possibile ridurre il gruppo di controllo sotto il 10%.

Puoi [selezionare un’esperienza specifica da usare come controllo](/help/main/c-activities/t-automated-personalization/experience-as-control.md) oppure utilizzare l’opzione Esperienza casuale.

## Quando scegliere [!UICONTROL Targeting automatico] rispetto a [!UICONTROL Automated Personalization]? {#section_BBC4871C87944DD7A8B925811A30C633}

Esistono diversi scenari in cui si preferisce utilizzare [!UICONTROL Targeting automatico] rispetto a [!UICONTROL Automated Personalization]:

* Se vuoi definire l’intera esperienza anziché singole offerte che vengono combinate automaticamente per formare un’esperienza.
* Se si desidera utilizzare il set completo di [!UICONTROL funzionalità del Compositore esperienza visivo] non supportate da [!UICONTROL Auto Personalization]: l&#39;editor di codice personalizzato, più tipi di pubblico e altro ancora.
* Se desideri apportare modifiche strutturali alla pagina in diverse esperienze. Ad esempio, se desideri ridisporre gli elementi nella home page, [!UICONTROL Targeting automatico] è più appropriato da utilizzare di [!UICONTROL Automated Personalization].

## Cosa hanno in comune [!UICONTROL Targeting automatico] con [!UICONTROL Automated Personalization]? {#section_2A601F482F9A44E38D4B694668711319}

### L’algoritmo ottimizza per ottenere un risultato favorevole per ogni visita.

* L’algoritmo prevede che il visitatore sia propenso alla conversione (o ai ricavi stimati dalla conversione) per fornire l’esperienza migliore.
* Un visitatore è idoneo per una nuova esperienza al termine di una sessione esistente (a meno che il visitatore non appartenga al gruppo di controllo, nel qual caso l’esperienza che gli viene assegnata alla prima visita rimane invariata per le visite successive).
* All’interno di una sessione, la previsione non cambia, per mantenere la coerenza visiva.

### L’algoritmo si adatta ai cambiamenti nel comportamento del visitatore.

* La slot machine assicura che il modello &quot;spenda&quot; sempre una piccola frazione di traffico per continuare a imparare per tutta la vita dell&#39;attività di apprendimento e per prevenire un eccessivo sfruttamento delle tendenze apprese in precedenza.
* I modelli sottostanti vengono ricreati ogni 24 ore utilizzando i dati di comportamento dei visitatori più recenti per garantire che [!DNL Target] sfrutti sempre le preferenze dei visitatori in continua evoluzione.
* Se l&#39;algoritmo non può determinare le esperienze vincenti per i singoli visitatori, mostra automaticamente quella con i migliori risultati a livello generale, mentre continua a cercare vincitori personalizzati. L’esperienza che offre prestazioni migliori viene individuata tramite il [campione di Thompson](https://en.wikipedia.org/wiki/Thompson_sampling).

### L’algoritmo viene continuamente ottimizzato per una singola metrica di obiettivo.

* Questa metrica potrebbe essere basata sulla conversione o sui ricavi (nello specifico [!UICONTROL Ricavo per visita]).

### [!DNL Target] raccoglie automaticamente informazioni sui visitatori per generare i modelli di personalizzazione.

* Per ulteriori informazioni sui parametri utilizzati in [!UICONTROL Targeting automatico] e [!UICONTROL Automated Personalization], vedi [Raccolta dati di Automated Personalization](/help/main/c-activities/t-automated-personalization/ap-data.md).

### [!DNL Target] utilizza automaticamente tutti i [!DNL Adobe Experience Cloud] tipi di pubblico condivisi per generare i modelli di personalizzazione.

* Non è necessario eseguire alcuna operazione specifica per aggiungere i tipi di pubblico al modello. Per informazioni sull’utilizzo di [!DNL Experience Cloud Audiences] con [!DNL Target], consulta [Audience di Experience Cloud](/help/main/c-integrating-target-with-mac/mmp.md).

### Gli addetti al marketing possono caricare dati offline, punteggi di propensione o altri dati personalizzati per creare modelli di personalizzazione.

* Ulteriori informazioni sul [caricamento dei dati per [!UICONTROL Targeting automatico] e [!UICONTROL Automated Personalization]](/help/main/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md).

## Differenze tra [!UICONTROL Targeting automatico] e [!UICONTROL Automated Personalization] {#section_BA4D83BE40F14A96BE7CBC7C7CF2A8FB}

### [!UICONTROL Il Targeting automatico] richiede spesso meno traffico di [!UICONTROL Automated Personalization] per generare un modello personalizzato.

Anche se la quantità di traffico *per esperienza* richiesta per [!UICONTROL Targeting automatico] o [!UICONTROL Modelli Personalization] automatici da compilare è la stessa, ci sono in genere più esperienze in un&#39;attività [!UICONTROL Automated Personalization] rispetto a un&#39;attività [!UICONTROL Targeting automatico].

Se, ad esempio, si disponesse di un&#39;attività [!UICONTROL Auto Personalization] in cui sono state create due offerte per posizione con due posizioni, l&#39;attività includerebbe quattro (2 = 4) esperienze totali (senza esclusioni). Utilizzando [!UICONTROL Targeting automatico], puoi impostare l&#39;esperienza 1 per includere l&#39;offerta 1 in posizione 1 e l&#39;offerta 2 in posizione 2 e l&#39;esperienza 2 per includere l&#39;offerta 1 in posizione 1 e l&#39;offerta 2 in posizione 2. Poiché [!UICONTROL Targeting automatico] consente di avere più modifiche all&#39;interno di un&#39;esperienza, puoi ridurre il numero di esperienze totali nell&#39;attività.

Per [!UICONTROL Targeting automatico] è possibile utilizzare semplici regole generali per comprendere i requisiti del traffico:

* **Quando [!UICONTROL Conversione] è la metrica di successo:** 1.000 visite e almeno 50 conversioni al giorno per esperienza e inoltre l&#39;attività deve avere almeno 7.000 visite e 350 conversioni.
* **Quando [!UICONTROL Ricavo per visita] è la metrica di successo:** 1.000 visite e almeno 50 conversioni al giorno per esperienza e in più l&#39;attività deve avere almeno 1.000 conversioni per esperienza. RPV di solito richiede più dati per costruire modelli a causa della varianza più elevata dei dati che esiste in genere nei ricavi di visita rispetto al tasso di conversione.

### [!UICONTROL Targeting automatico] dispone di funzionalità di installazione complete.

* Poiché [!UICONTROL Targeting automatico] è incorporato nel flusso di lavoro di attività A/B, [!UICONTROL Targeting automatico] beneficia del [!UICONTROL Compositore esperienza visivo] (VEC) più maturo e completo. Puoi anche utilizzare [collegamenti di controllo qualità](/help/main/c-activities/c-activity-qa/activity-qa.md) con [!UICONTROL Targeting automatico].

### [!UICONTROL Targeting automatico] fornisce un ampio framework di test online.

* La slot machine fa parte di un framework di test online più ampio che consente a [!DNL Adobe] data scientist e ricercatori di comprendere i vantaggi dei continui miglioramenti delle condizioni reali.
* In futuro, questo banco di prova ci consentirà di aprire la piattaforma di apprendimento automatico [!DNL Adobe] ai client esperti in materia di dati in modo che possano inserire i propri modelli per incrementare i modelli [!DNL Target].

## Reporting e [!UICONTROL Targeting automatico] {#section_42EE7F5E65E84F89A872FE9921917F76}

Per ulteriori informazioni, vedere [Reporting and Auto-Target](/help/main/c-activities/auto-target/reporting-and-auto-target.md).

